---
title: บันทึกสัญญาเช่าในสกุลเงินต่างประเทศ
description: หัวข้อนี้จะอธิบายวิธีการบันทึกการเช่าในสกุลเงินอื่นที่ไม่ใช่สกุลเงินทางบัญชีหรือการรายงาน
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 92177d4f808bfec88dabe9277c3d584ed02e401e
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4448605"
---
# <a name="record-leases-in-foreign-currencies"></a><span data-ttu-id="79b89-103">บันทึกสัญญาเช่าในสกุลเงินต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="79b89-103">Record leases in foreign currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79b89-104">บัญชีการเช่าสินทรัพย์สำหรับการเช่าที่อยู่ในสกุลเงินอื่นที่ไม่ใช่สกุลเงินทางบัญชีหรือสกุลเงินการรายงานมีการตั้งค่าในหน้า **การตั้งค่าบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="79b89-104">Asset leasing accounts for leases that are in currencies other than the accounting currency or the reporting currency are established on the **Ledger setup** page.</span></span> <span data-ttu-id="79b89-105">ควรป้อนการเช่าทั้งหมดในสกุลเงินของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="79b89-105">All leases should be entered in their transaction currency.</span></span> <span data-ttu-id="79b89-106">กล่าวคือ ควรป้อนในสกุลเงินที่ระบุไว้ในสัญญาการเช่า</span><span class="sxs-lookup"><span data-stu-id="79b89-106">In other words, they should be entered in the currency that is specified in the lease contract.</span></span> <span data-ttu-id="79b89-107">หัวข้อนี้จะอธิบายวิธีการบันทึกการเช่าในสกุลเงินอื่นที่ไม่ใช่สกุลเงินทางบัญชีหรือการรายงาน</span><span class="sxs-lookup"><span data-stu-id="79b89-107">This topic explains how to record leases in currencies other than the accounting or reporting currency.</span></span>

<span data-ttu-id="79b89-108">ถ้าคุณป้อนค่าเช่าในสกุลเงินต่างประเทศ สิทธิ์การใช้สินทรัพย์ (ROU) จะถูกคิดค่าเสื่อมราคาทั้งในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="79b89-108">If you enter a lease in a foreign currency, the right-of-use (ROU) asset is depreciated in both the accounting currency and the reporting currency.</span></span> <span data-ttu-id="79b89-109">สกุลเงินเหล่านี้มีการตั้งค่าคอนฟิกในหน้า **การตั้งค่าบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="79b89-109">These currencies are configured on the **Ledger setup** page.</span></span> <span data-ttu-id="79b89-110">ลักษณะการทำงานนี้ยังใช้ในสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="79b89-110">This behavior is also used in Fixed assets.</span></span> <span data-ttu-id="79b89-111">เมื่อคุณสร้างการเช่าในสกุลเงินต่างประเทศ ให้เลือกสกุลเงินของธุรกรรมในฟิลด์ **สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="79b89-111">When you create a lease in a foreign currency, select the transaction currency in the **Currency** field.</span></span>

<span data-ttu-id="79b89-112">อัตราแลกเปลี่ยนของสกุลเงินทางบัญชี คือค่าเริ่มต้นในฟิลด์ **อัตราแลกเปลี่ยนสกุลเงินทางบัญชี**</span><span class="sxs-lookup"><span data-stu-id="79b89-112">The exchange rate of the accounting currency is the default value in **Accounting currency exchange rate** field.</span></span> <span data-ttu-id="79b89-113">อัตราแลกเปลี่ยนของสกุลเงินการรายงาน คือค่าเริ่มต้นในฟิลด์ **อัตราแลกเปลี่ยนสกุลเงินการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="79b89-113">The exchange rate of the reporting currency is the default value in the **Reporting currency exchange rate** field.</span></span> <span data-ttu-id="79b89-114">อัตราแลกเปลี่ยนเหล่านี้มีผลบังคับใช้ในวันที่เริ่มต้นการเช่า</span><span class="sxs-lookup"><span data-stu-id="79b89-114">These exchange rates were effective on the commencement date of the lease.</span></span> <span data-ttu-id="79b89-115">ฟิลด์ **อัตราแลกเปลี่ยนสกุลเงินทางบัญชี** และ **อัตราแลกเปลี่ยนสกุลเงินการรายงาน** จะอยู่ในแท็บด่วน **ข้อมูลการแลกเปลี่ยนทางการเงินและการรายงาน** บนหน้า **รายละเอียดการเช่า**</span><span class="sxs-lookup"><span data-stu-id="79b89-115">The **Accounting currency exchange rate** and **Reporting currency exchange rate** fields, are in the **Financial and reporting exchange information** FastTab, on the **Lease details** page.</span></span>

1. <span data-ttu-id="79b89-116">เลือกกล่องกาเครื่องหมาย **อัตราคงที่** เพื่อแทนที่อัตราแลกเปลี่ยนที่ป้อนโดยอัตโนมัติ แล้วป้อนอัตราใหม่</span><span class="sxs-lookup"><span data-stu-id="79b89-116">Select the **Fixed rate** check box to override the exchange rate that was automatically entered, and then enter the new rate.</span></span>
2. <span data-ttu-id="79b89-117">ในฟิลด์อื่นๆ ให้ป้อนข้อมูลที่จำเป็นสำหรับการเช่า แล้วเลือก **สร้างกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="79b89-117">In the other fields, enter the information that is required for the lease, and then select **Create schedules**.</span></span>
3. <span data-ttu-id="79b89-118">บนหน้า **รายละเอียดการเช่า** ใหม่ ให้เลือก **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="79b89-118">On the new **Lease details** page, select **Books**.</span></span>
4. <span data-ttu-id="79b89-119">บนหน้า **สมุดบัญชีการเช่า** บนแท็บ **ข้อมูลการแลกเปลี่ยนทางการเงินและการรายงาน** ให้ตรวจสอบค่าของ **สิทธิ์การใช้สินทรัพย์เริ่มต้นของสกุลเงินทางบัญชี** และฟิลด์ **สิทธิ์การใช้สินทรัพย์เริ่มต้นของสกุลเงินการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="79b89-119">On the **Lease book** page, on the **Financial and reporting exchange information** tab, verify the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span> <span data-ttu-id="79b89-120">แต่ละฟิลด์เหล่านี้จะแสดงยอดดุลสินทรัพย์ ROU ที่แปลแล้วในสกุลเงินที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="79b89-120">Each of these fields shows the translated ROU asset balance in the corresponding currency.</span></span> <span data-ttu-id="79b89-121">ฟิลด์เหล่านี้จะถูกอัปเดตเมื่อใดก็ตามที่คุณเปลี่ยนข้อมูลทางการเงินใดๆ</span><span class="sxs-lookup"><span data-stu-id="79b89-121">These fields are updated whenever you change any financial information.</span></span> <span data-ttu-id="79b89-122">เลือก **สร้างกำหนดการ** ก่อนที่คุณจะยืนยันกำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="79b89-122">Select **Create schedules** before you confirm the payment schedule.</span></span>

    <span data-ttu-id="79b89-123">รายการสมุดรายวันการรับรู้เริ่มต้นจะบันทึกสินทรัพย์ ROU ที่ใช้อัตราแลกเปลี่ยนสกุลเงินที่แสดงรายการอยู่ในการเช่า</span><span class="sxs-lookup"><span data-stu-id="79b89-123">The initial recognition journal entry records the ROU asset that uses the currency exchange rates that are listed on the lease.</span></span> <span data-ttu-id="79b89-124">รายการสมุดรายวันยังรวมถึงค่าของฟิลด์ **สิทธิ์การใช้สินทรัพย์เริ่มต้นของสกุลเงินทางบัญชี** และ **สิทธิ์การใช้สินทรัพย์เริ่มต้นของสกุลเงินการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="79b89-124">The journal entry also includes the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

## <a name="subsequent-measurement-for-foreign-currency-leases"></a><span data-ttu-id="79b89-125">การประเมินในเวลาต่อมาสำหรับการเช่าสกุลเงินต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="79b89-125">Subsequent measurement for foreign currency leases</span></span>

<span data-ttu-id="79b89-126">กำหนดการคิดค่าเสื่อมราคาจะแสดงยอดค่าใช้จ่ายค่าเสื่อมราคาที่คาดไว้ในสกุลเงินการรายงาน สกุลเงินทางบัญชี และสกุลเงินของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="79b89-126">The depreciation schedule shows the expected depreciation expense amounts in the reporting currency, the accounting currency, and the transaction currency.</span></span>

<span data-ttu-id="79b89-127">การดูยอดดุลสินทรัพย์ ROU และยอดค่าเสื่อมราคา ในสกุลเงินการรายงานหรือสกุลเงินทางบัญชี ให้เปิดหน้า **กำหนดการคิดค่าเสื่อมราคาสินทรัพย** และเลือกกล่องกาเครื่องหมาย **แสดงยอดเงินในสกุลเงินทางบัญชี** หรือ **แสดงยอดเงินในสกุลเงินการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="79b89-127">To view the ROU asset balances and depreciation amounts in either the reporting currency or the accounting currency, open the **Asset depreciation schedule** page, and select the **Show accounting currency amounts** or **Show reporting currency amounts** check box.</span></span>

<span data-ttu-id="79b89-128">เมื่อคุณสร้างรายการสมุดรายวันค่าใช้จ่ายค่าเสื่อมราคากับการเช่าที่กำหนดไว้ในสกุลเงินต่างประเทศ รายการจะใช้อัตราแลกเปลี่ยนที่แสดงรายการอยู่ในการเช่า</span><span class="sxs-lookup"><span data-stu-id="79b89-128">When you create the depreciation expense journal entries against a lease that is denominated in a foreign currency, the entry uses the exchange rates that are listed on the lease.</span></span> <span data-ttu-id="79b89-129">และยังใช้ค่าของฟิลด์ **สิทธิ์การใช้สินทรัพย์เริ่มต้นของสกุลเงินทางบัญชี** และ **สิทธิ์การใช้สินทรัพย์เริ่มต้นของสกุลเงินการรายงาน** อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="79b89-129">It also uses the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

<span data-ttu-id="79b89-130">ยอดค่าใช้จ่ายค่าเสื่อมราคาขั้นสุดท้ายสามารถคำนวณได้โดยใช้อัตราแลกเปลี่ยนที่แตกต่างกันเล็กน้อย เพื่อให้สินทรัพย์ ROU เต็มจำนวนทั้งในสกุลเงินทางบัญชีและสกุลเงินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="79b89-130">The final depreciation expense amount can be calculated by using a slightly different exchange rate, so that the ROU asset is fully depreciated in both the accounting currency and the reporting currency.</span></span>

<span data-ttu-id="79b89-131">ถ้ามีการจัดประเภทการเช่าใหม่ เป็น **ค่าเช่ารอตัดบัญชี** ระบบจะล้างข้อมูลอัตราแลกเปลี่ยนของสกุลเงินทางบัญชีและการรายงานให้โดยอัตโนมัติ ถ้ามีการกำหนดค่าเช่าแล้ว</span><span class="sxs-lookup"><span data-stu-id="79b89-131">If the lease has been reclassified as **Deferred rent**, the system automatically clears the exchange rates of the accounting and reporting currencies, if they have already been defined.</span></span>
