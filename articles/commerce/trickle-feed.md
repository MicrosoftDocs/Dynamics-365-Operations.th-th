---
title: การสร้างใบสั่งตามฟีดแบบต่อเนื่องสำหรับธุรกรรมร้านค้าปลีก
description: หัวข้อนี้จะอธิบายถึงการสร้างใบสั่งตามฟีดแบบต่อเนื่องสำหรับธุรกรรมร้านค้าปลีกใน Microsoft Dynamics 365 Commerce
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3f691017ad06d3416e4ba0e86d7a0bc207aba5bd
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004285"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="1426e-103">การสร้างใบสั่งตามฟีดแบบต่อเนื่องสำหรับธุรกรรมร้านค้าปลีก (รุ่นพรีวิวสำหรับสาธารณะ)</span><span class="sxs-lookup"><span data-stu-id="1426e-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="1426e-104">ใน Dynamics 365 Retail รุ่น 10.0.4 และก่อนหน้า การลงรายการบัญชีใบแจ้งยอดจะมีการดำเนินงานเมื่อสิ้นสุดวันและธุรกรรมทั้งหมดจะมีการลงรายการบัญชีในสมุดบัญชีเมื่อสิ้นสุดวัน</span><span class="sxs-lookup"><span data-stu-id="1426e-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="1426e-105">ธุรกรรมจำนวนมากต้องมีการประมวลผลในกรอบเวลาที่จำกัด บางครั้งอาจทำให้การโหลดล้มเหลวและมีการล็อคการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="1426e-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="1426e-106">นอกจากนี้ ผู้ขายปลีกยังไม่สามารถรับรู้รายได้และการชำระเงินในสมุดบัญชีของตนตลอดทั้งวันได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="1426e-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="1426e-107">เมื่อมีการนำพรีวิวสำหรับสาธารณะของการสร้างใบสั่งตามฟีดแบบต่อเนื่องมาใช้ใน Retail รุ่น 10.0.5 ธุรกรรมจะมีการประมวลผลตลอดทั้งวัน และจะมีการประมวลผลการกระทบยอดการชำระเงินของการชำระเงินและธุรกรรมการจัดการเงินสดอื่นๆ เมื่อสิ้นสุดวัน</span><span class="sxs-lookup"><span data-stu-id="1426e-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="1426e-108">ฟังก์ชันนี้จะแบ่งจำนวนของโหลดการสร้างใบสั่งขาย ใบแจ้งหนี้ และการชำระเงินตลอดทั้งวัน เพื่อให้มีประสิทธิภาพการรับรู้ที่ดียิ่งขึ้นและมีความสามารถในการรับรู้รายได้และการชำระเงินในสมุดบัญชีใกล้เคียงกับในเวลาจริง</span><span class="sxs-lookup"><span data-stu-id="1426e-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="1426e-109">วิธีการใช้การลงรายการบัญชีตามฟีดแบบต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="1426e-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="1426e-110">เมื่อต้องการเปิดใช้งานการลงรายการบัญชีธุรกรรมโดยใช้ฟีดแบบต่อเนื่อง ไปที่ **การจัดการระบบ > ตั้งค่า > การตั้งค่าคอนฟิกลิขสิทธิ์** และปิดใช้งานคีย์ **ใบแจ้งยอด**</span><span class="sxs-lookup"><span data-stu-id="1426e-110">To enable trickle feed-based posting of transactions, go to **System administration > Set up > License configuration** and disable the the **Statements** key.</span></span>

2. <span data-ttu-id="1426e-111">ในหน้าเดียวกัน ให้เปิดใช้คีย์ลิขสิทธิ์ **งานใบแจ้งยอด (ฟีดแบบต่อเนื่อง) – พรีวิว**</span><span class="sxs-lookup"><span data-stu-id="1426e-111">On the same page, enable the **Statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="1426e-112">เมื่อคุณเปิดใช้งานคีย์นี้ โปรดตรวจสอบให้แน่ใจว่าไม่มีการลงรายการบัญชีใบแจ้งยอดที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="1426e-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

    > [!Important]
    > <span data-ttu-id="1426e-113">ก่อนที่คุณจะเปิดใช้งานคีย์ลิขสิทธิ์ **ใบแจ้งยอด (ฟีดแบบต่อเนื่อง) – พรีวิว** โปรดตรวจสอบให้แน่ใจว่าไม่มีการลงรายการบัญชีใบแจ้งยอดที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="1426e-113">Before you enable the **Statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="1426e-114">เอกสารใบแจ้งยอดปัจจุบันจะถูกแบ่งออกเป็นสองชนิด คือ ใบแจ้งยอดธุรกรรมและงบการเงิน</span><span class="sxs-lookup"><span data-stu-id="1426e-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="1426e-115">ใบแจ้งยอดธุรกรรมจะเลือกธุรกรรมที่ยังไม่ได้ลงรายการบัญชีและตรวจสอบความถูกต้องทั้งหมด และสร้างใบสั่งขาย ใบแจ้งหนี้การขาย สมุดรายวันการชำระเงินและส่วนลด และธุรกรรมรายได้-ค่าใช้จ่ายตามระยะความถี่ที่คุณตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="1426e-115">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="1426e-116">คุณควรตั้งค่าคอนฟิกกระบวนการนี้เพื่อเรียกใช้ที่ความถี่สูง เพื่อให้เอกสารถูกสร้างขึ้นเมื่อมีการอัพโหลดธุรกรรมลงในศูนย์ควบคุมผ่านงาน P</span><span class="sxs-lookup"><span data-stu-id="1426e-116">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="1426e-117">เมื่อมีใบแจ้งยอดธุรกรรมที่สร้างใบสั่งขายและใบแจ้งหนี้การขายอยู่แล้ว คุณก็ไม่จำเป็นต้องตั้งค่าคอนฟิกชุดงาน **ลงรายการบัญชีสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="1426e-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="1426e-118">อย่างไรก็ตาม คุณยังคงสามารถใช้ชุดงานดังกล่าวเพื่อตอบสนองความต้องการทางธุรกิจเฉพาะที่คุณอาจมีได้</span><span class="sxs-lookup"><span data-stu-id="1426e-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="1426e-119">งบการเงินได้รับการออกแบบมาให้มีการสร้างเมื่อสิ้นสุดวันและรองรับวิธีการปิด **กะ** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1426e-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="1426e-120">ใบแจ้งยอดนี้จะถูกจำกัดไว้สำหรับการกระทบยอดทางการเงินและจะสร้างเฉพาะสมุดรายวันของยอดเงินผลต่างระหว่างยอดเงินที่ตรวจนับและยอดเงินธุรกรรมสำหรับการชำระเงินต่างๆ พร้อมกับสมุดรายวันของธุรกรรมการจัดการเงินสดอื่นๆ เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1426e-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="1426e-121">เมื่อต้องการคำนวณใบแจ้งยอดธุรกรรม ให้คลิก **การขายปลีกและการค้า > ข้อมูลไอทีสำหรับการขายปลีกและการค้า > การลงรายการบัญชี POS > คำนวณใบแจ้งยอดธุรกรรมเป็นชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="1426e-121">To calculate the transactional statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="1426e-122">เมื่อต้องการลงรายการบัญชีใบแจ้งยอดธุรกรรมเป็นชุดงาน ให้คลิก **การขายปลีกและการค้า > ข้อมูลไอทีสำหรับการขายปลีกและการค้า > การลงรายการบัญชี POS > ลงรายการบัญชีใบแจ้งยอดธุรกรรมเป็นชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="1426e-122">To post the transactional statement statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="1426e-123">เมื่อต้องการคำนวณงบการเงิน ให้คลิก **การขายปลีกและการค้า > ข้อมูลไอทีสำหรับการขายปลีกและการค้า > การลงรายการบัญชี POS > คำนวณงบการเงินเป็นชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="1426e-123">To calculate the financial statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="1426e-124">เมื่อต้องการลงรายการบัญชีงบการเงินเป็นชุดงาน ให้คลิก **การขายปลีกและการค้า > ข้อมูลไอทีสำหรับการขายปลีกและการค้า > การลงรายการบัญชี POS > ลงรายการบัญชีงบการเงินเป็นชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="1426e-124">To post the financial statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="1426e-125">รายการเมนู **การขายปลีกและการค้า > ข้อมูลไอทีสำหรับการขายปลีกและการค้า > การลงรายการบัญชี POS > คำนวณใบแจ้งยอดเป็นชุดงาน** และ **การขายปลีกและการค้า > ข้อมูลไอทีสำหรับการขายปลีกและการค้า > การลงรายการบัญชี POS > ลงรายการบัญชีใบแจ้งยอดเป็นชุดงาน** จะถูกเอาออกสำหรับคุณลักษณะใหม่นี้</span><span class="sxs-lookup"><span data-stu-id="1426e-125">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="1426e-126">อีกทางหนึ่งคือ คุณสามารถสร้างชนิดของใบแจ้งยอดธุรกรรมและงบการเงินด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="1426e-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="1426e-127">ไปที่ **การขายปลีกและการค้า > ช่องทาง > ร้านค้า** และคลิก **ใบแจ้งยอด**</span><span class="sxs-lookup"><span data-stu-id="1426e-127">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="1426e-128">คลิก **สร้าง** แล้วเลือกชนิดของใบแจ้งยอดที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="1426e-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="1426e-129">ฟิลด์บนหน้า **ใบแจ้งยอด** และการดำเนินการภายใต้ **กลุ่มใบแจ้งยอด** ของหน้าจะแสดงข้อมูลที่เกี่ยวข้องและการดำเนินการตามชนิดของใบแจ้งยอดที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1426e-129">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
