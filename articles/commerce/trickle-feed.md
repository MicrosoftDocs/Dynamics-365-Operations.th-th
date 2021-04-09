---
title: การสร้างใบสั่งตามฟีดแบบต่อเนื่องสำหรับธุรกรรมร้านค้าปลีก
description: หัวข้อนี้จะอธิบายถึงการสร้างใบสั่งตามฟีดแบบต่อเนื่องสำหรับธุรกรรมของร้านค้าใน Microsoft Dynamics 365 Commerce
author: josaw1
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0686b1b3113440808ea195683e15fb2c66b4558
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801854"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="54321-103">การสร้างใบสั่งตามฟีดแบบต่อเนื่องสำหรับธุรกรรมร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="54321-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="54321-104">ใน Dynamics 365 Retail รุ่น 10.0.4 และก่อนหน้า การลงรายการบัญชีใบแจ้งยอดจะมีการดำเนินงานเมื่อสิ้นสุดวันและธุรกรรมทั้งหมดจะมีการลงรายการบัญชีในสมุดบัญชีเมื่อสิ้นสุดวัน</span><span class="sxs-lookup"><span data-stu-id="54321-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="54321-105">ธุรกรรมจำนวนมากต้องมีการประมวลผลในกรอบเวลาที่จำกัด บางครั้งอาจทำให้การโหลดล้มเหลวและมีการล็อคการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="54321-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="54321-106">นอกจากนี้ ผู้ขายปลีกยังไม่สามารถรับรู้รายได้และการชำระเงินในสมุดบัญชีของตนตลอดทั้งวันได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="54321-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="54321-107">เมื่อมีการนำการสร้างใบสั่งตามฟีดแบบต่อเนื่องมาใช้ใน Retail รุ่น 10.0.5 ธุรกรรมจะมีการประมวลผลตลอดทั้งวัน และจะมีการประมวลผลการกระทบยอดการชำระเงินของการชำระเงินและธุรกรรมการจัดการเงินสดอื่นๆ เมื่อสิ้นสุดวัน</span><span class="sxs-lookup"><span data-stu-id="54321-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="54321-108">ฟังก์ชันนี้จะแบ่งจำนวนของโหลดการสร้างใบสั่งขาย ใบแจ้งหนี้ และการชำระเงินตลอดทั้งวัน เพื่อให้มีประสิทธิภาพการรับรู้ที่ดียิ่งขึ้นและมีความสามารถในการรับรู้รายได้และการชำระเงินในสมุดบัญชีใกล้เคียงกับในเวลาจริง</span><span class="sxs-lookup"><span data-stu-id="54321-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="54321-109">วิธีการใช้การลงรายการบัญชีตามฟีดแบบต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="54321-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="54321-110">เมื่อต้องการเปิดการใช้งานการลงรายการบัญชีตามฟีดแบบต่อเนื่องของธุรกรรมการขายปลึก ให้เปิดการใช้งานคุณลักษณะที่ชื่อ **ใบแจ้งยอดการขายปลีก - ฟีดแบบต่อเนื่อง** โดยใช้การจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="54321-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="54321-111">ก่อนเปิดใช้งานคุณลักษณะนี้ โปรดตรวจสอบให้แน่ใจว่าไม่มีการลงรายการบัญชีใบแจ้งยอดที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="54321-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="54321-112">เอกสารใบแจ้งยอดปัจจุบันจะถูกแบ่งออกเป็นสองชนิด คือ ใบแจ้งยอดธุรกรรมและงบการเงิน</span><span class="sxs-lookup"><span data-stu-id="54321-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="54321-113">ใบแจ้งยอดธุรกรรมจะเลือกธุรกรรมที่ยังไม่ได้ลงรายการบัญชีและตรวจสอบความถูกต้องทั้งหมด และสร้างใบสั่งขาย ใบแจ้งหนี้การขาย สมุดรายวันการชำระเงินและส่วนลด และธุรกรรมรายได้-ค่าใช้จ่ายตามระยะความถี่ที่คุณตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="54321-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="54321-114">คุณควรตั้งค่าคอนฟิกกระบวนการนี้เพื่อเรียกใช้ที่ความถี่สูง เพื่อให้เอกสารถูกสร้างขึ้นเมื่อมีการอัพโหลดธุรกรรมลงในศูนย์ควบคุมผ่านงาน P</span><span class="sxs-lookup"><span data-stu-id="54321-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="54321-115">เมื่อมีใบแจ้งยอดธุรกรรมที่สร้างใบสั่งขายและใบแจ้งหนี้การขายอยู่แล้ว คุณก็ไม่จำเป็นต้องตั้งค่าคอนฟิกชุดงาน **ลงรายการบัญชีสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="54321-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="54321-116">อย่างไรก็ตาม คุณยังคงสามารถใช้ชุดงานดังกล่าวเพื่อตอบสนองความต้องการทางธุรกิจเฉพาะที่คุณอาจมีได้</span><span class="sxs-lookup"><span data-stu-id="54321-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="54321-117">งบการเงินได้รับการออกแบบมาให้มีการสร้างเมื่อสิ้นสุดวันและรองรับวิธีการปิด **กะ** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="54321-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="54321-118">ใบแจ้งยอดนี้จะถูกจำกัดไว้สำหรับการกระทบยอดทางการเงินและจะสร้างเฉพาะสมุดรายวันของยอดเงินผลต่างระหว่างยอดเงินที่ตรวจนับและยอดเงินธุรกรรมสำหรับการชำระเงินต่างๆ พร้อมกับสมุดรายวันของธุรกรรมการจัดการเงินสดอื่นๆ เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="54321-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="54321-119">เมื่อต้องการคำนวณใบแจ้งยอดธุรกรรม ให้ไปที่ **Retail และ Commerce > ข้อมูลไอทีสำหรับ Retail และ Commerce > การลงรายการบัญชี POS > คำนวณใบแจ้งยอดธุรกรรมเป็นชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="54321-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="54321-120">เมื่อต้องการลงรายการบัญชีใบแจ้งยอดธุรกรรมเป็นชุดงาน ให้ไปที่ **Retail และ Commerce > ข้อมูลไอทีสำหรับ Retail และ Commerce > การลงรายการบัญชี POS > ลงรายการบัญชีใบแจ้งยอดธุรกรรมเป็นชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="54321-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="54321-121">เมื่อต้องการคำนวณงบการเงิน ให้ไปที่ **Retail และ Commerce > ข้อมูลไอทีสำหรับ Retail และ Commerce > การลงรายการบัญชี POS > คำนวณงบการเงินเป็นชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="54321-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="54321-122">เมื่อต้องการลงรายการบัญชีงบการเงินเป็นชุดงาน ให้ไปที่ **Retail และ Commerce > ข้อมูลไอทีสำหรับ Retail และ Commerce > การลงรายการบัญชี POS > ลงรายการบัญชีงบการเงินเป็นชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="54321-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="54321-123">รายการเมนู **Retail และ Commerce > ข้อมูลไอทีสำหรับ Retail และ Commerce > การลงรายการบัญชี POS > คำนวณใบแจ้งยอดเป็นชุดงาน** และ **Retail และ Commerce > ข้อมูลไอทีสำหรับ Retail และ Commerce > การลงรายการบัญชี POS > ลงรายการบัญชีใบแจ้งยอดเป็นชุดงาน** จะถูกเอาออกสำหรับคุณลักษณะใหม่นี้</span><span class="sxs-lookup"><span data-stu-id="54321-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="54321-124">อีกทางหนึ่งคือ คุณสามารถสร้างชนิดของใบแจ้งยอดธุรกรรมและงบการเงินด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="54321-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="54321-125">ไปที่ **Retail และ Commerce > ช่องทาง > ร้านค้า** และคลิก **ใบแจ้งยอด**</span><span class="sxs-lookup"><span data-stu-id="54321-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="54321-126">คลิก **สร้าง** แล้วเลือกชนิดของใบแจ้งยอดที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="54321-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="54321-127">ฟิลด์บนหน้า **ใบแจ้งยอด** และการดำเนินการภายใต้ **กลุ่มใบแจ้งยอด** ของหน้าจะแสดงข้อมูลที่เกี่ยวข้องและการดำเนินการตามชนิดของใบแจ้งยอดที่เลือก</span><span class="sxs-lookup"><span data-stu-id="54321-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]