---
title: เพิ่มหรือคัดลอกการเช่า (การแสดงตัวอย่าง)
description: หัวข้อนี้จะอธิบายวิธีการสร้างการเช่าใหม่ โดยการป้อนข้อมูลในการเช่าสินทรัพย์หรือการคัดลอกข้อมูลจากการเช่าที่มีอยู่
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b495c9a02a872d4b360b5f7216b1db3f7d366daf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814163"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="0f854-103">เพิ่มหรือคัดลอกการเช่า (การแสดงตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="0f854-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f854-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างการเช่าตั้งแต่การเริ่มต้นในการเช่าสินทรัพย์ และวิธีการสร้างการเช่าโดยคัดลอกการเช่าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="0f854-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="0f854-105">กระบวนการในการสร้างการเช่าตั้งแต่เริ่มต้นเกี่ยวข้องกับการป้อนข้อมูลสำหรับการเช่าใหม่ แล้วสร้างกำหนดการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="0f854-106">หลังจากที่มีการตั้งค่าการเช่าอย่างน้อยหนึ่งรายการแล้ว คุณอาจพบว่าเป็นการง่ายกว่าในการคัดลอกข้อมูลจากการเช่าที่มีอยู่แล้ว และแก้ไขข้อมูลนั้นเมื่อคุณต้องการสร้างการเช่าใหม่</span><span class="sxs-lookup"><span data-stu-id="0f854-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="0f854-107">สร้างการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-107">Create a lease</span></span>

<span data-ttu-id="0f854-108">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างการเช่าในการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="0f854-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="0f854-109">บนหน้า **สรุปการเช่า** บนบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0f854-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="0f854-110">ป้อนข้อมูลการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-110">Enter the lease information.</span></span> <span data-ttu-id="0f854-111">ฟิลด์ที่จำเป็นต้องมีเส้นขอบสีแดง</span><span class="sxs-lookup"><span data-stu-id="0f854-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="0f854-112">สร้างกำหนดการการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-112">Create a lease schedule</span></span>

<span data-ttu-id="0f854-113">หลังจากที่คุณป้อนข้อมูลสำหรับการเช่าเสร็จแล้ว ให้ทำตามขั้นตอนต่อไปนี้เพื่อสร้างกำหนดการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="0f854-114">มิติทางการเงินอาจเปลี่ยนแปลงได้ตามมิติทางการเงินที่กำหนดเองใดๆ</span><span class="sxs-lookup"><span data-stu-id="0f854-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="0f854-115">เลือก **สร้างกำหนดการ** เพื่อสร้างสมุดบัญชีการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="0f854-116">สมุดบัญชีเช่ารวมถึงกำหนดการ การชำระเงิน ค่าตัดบัญชี ยค่าเสื่อมราคา และค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0f854-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="0f854-117">ถ้าต้องการเข้าถึงสมุดบัญชีการเช่าและดูกำหนดการที่สร้างขึ้นใหม่ ให้เลือกแท็บ **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="0f854-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="0f854-118">หน้า **รายละเอียดของสมุดบัญชี** แสดงวิธีการลงบัญชีการเช่าโดยเรียงตามสมุดบัญชีที่มีการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="0f854-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="0f854-119">จากที่นี่ คุณสามารถดูกำหนดการเช่าได้</span><span class="sxs-lookup"><span data-stu-id="0f854-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="0f854-120">กำหนดการชำระเงินจะประกอบด้วยอินพุตจากแท็บ **รายการกำหนดการชำระเงิน** บนหน้า **เพิ่มการเช่า**</span><span class="sxs-lookup"><span data-stu-id="0f854-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="0f854-121">คุณยังสามารถเปลี่ยนยอดการชำระเงินและการชำระเงินตามตัวแปรได้</span><span class="sxs-lookup"><span data-stu-id="0f854-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="0f854-122">หนี้สินสัญญาเช่าคำนวณตามกำหนดการชำระเงินที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="0f854-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="0f854-123">หลังจากที่คุณตรวจสอบกำหนดการชำระเงินเสร็จแล้ว ให้เลือก **ยืนยันกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="0f854-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="0f854-124">หลังจากที่ได้รับการยืนยันกำหนดการ การเช่าจะไม่สามารถแก้ไขได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="0f854-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f854-125">ระบบจะคำนวณเงื่อนไขการให้เช่าโดยอัตโนมัติจากรายการกำหนดการชำระเงินในหน้า **เพิ่มการเช่า**</span><span class="sxs-lookup"><span data-stu-id="0f854-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="0f854-126">เมื่อต้องการคำนวณเงื่อนไขการเช่าเป็นรายเดือน ระบบจะค้นหาผลต่างระหว่างวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับรายการกำหนดการชำระเงินที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="0f854-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="0f854-127">หลังจากนั้นให้ย้ายไปที่รายการกำหนดการชำระเงินครั้งถัดไป และค้นหาความแตกต่างอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="0f854-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="0f854-128">ในขั้นสุดท้าย ระบบจะรวมยอดเงินทั้งหมดเพื่อกำหนดเงื่อนไขการเช่ารายเดือน</span><span class="sxs-lookup"><span data-stu-id="0f854-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="0f854-129">เมื่อต้องการดอกเบี้ยจ่ายของรอบระยะเวลาที่คำนวณได้ ให้เปิดหน้า **กำหนดการตัดบัญชีหนี้สิน**</span><span class="sxs-lookup"><span data-stu-id="0f854-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="0f854-130">เมื่อต้องการดูค่าเสื่อมราคาแบบเส้นตรงที่คำนวณได้ ให้เปิดหน้า **กำหนดการคิดค่าเสื่อมราคาสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="0f854-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="0f854-131">หลังจากที่คุณได้ตรวจทานยอดเงินที่คำนวณแล้ว คุณสามารถสร้างรายการสมุดรายวันการรับรู้เมื่อเริ่มแรก บนหน้า **การรับรู้เมื่อเริ่มแรก**</span><span class="sxs-lookup"><span data-stu-id="0f854-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="0f854-132">คุณได้รับข้อความแจ้งว่ามีการสร้างสมุดรายวันแล้ว</span><span class="sxs-lookup"><span data-stu-id="0f854-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f854-133">รายการสมุดรายวันไม่ได้ลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไปจนกว่าคุณจะลงรายการบัญชีรายการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="0f854-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="0f854-134">ถ้าต้องการตรวจสอบรายการการรับรู้เริ่มต้นที่นำเสนอก่อนที่คุณจะลงรายการบัญชี ให้เลือก **สมุดรายวันการเช่าสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="0f854-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f854-135">ไม่สามารถสร้างสมุดรายวันการเช่าสินทรัพย์ด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="0f854-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="0f854-136">จะมีการสร้างขึ้นโดยอัตโนมัติเมื่อมีการสร้างกำหนดการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="0f854-137">เมื่อคุณตรวจสอบรายการสมุดรายวันการรับรู้เริ่มต้นแล้ว และพร้อมที่จะลงรายการบัญชี ให้เลือก **ลงรายการบัญชี** เพื่อจดจำสิทธิ์การใช้สินทรัพย์ (ROU) และหนี้สินสัญญาเช่าในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="0f854-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="0f854-138">คัดลอกการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-138">Copy a lease</span></span>

<span data-ttu-id="0f854-139">การเช่าสินทรัพย์ช่วยให้คุณสามารถคัดลอกรายละเอียดของการเช่าเพื่อสร้างการเช่าใหม่ที่มีรายละเอียดเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="0f854-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="0f854-140">จากนั้นคุณก็สามารถเปลี่ยนฟิลด์การเช่า ก่อนที่คุณจะสร้างกำหนดการสำหรับการเช่าที่คัดลอก</span><span class="sxs-lookup"><span data-stu-id="0f854-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="0f854-141">บนหน้า **สรุปการเช่า** เลือกการเช่าที่จะคัดลอก แล้วจากนั้น บนบานหน้าต่างการดำเนินการ ให้เลือก **คัดลอกการเช่า**</span><span class="sxs-lookup"><span data-stu-id="0f854-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f854-142">ถ้าพารามิเตอร์ **ด้วยตนเอง** ถูกปิดสำหรับลำดับหมายเลขสำหรับรหัสการเช่า หมายเลขถัดไปในลำดับจะถูกสร้างขึ้นโดยอัตโนมัติเป็นรหัสการเช่าของการเช่าที่คัดลอก</span><span class="sxs-lookup"><span data-stu-id="0f854-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="0f854-143">ถ้ามีการเปิดใช้งานพารามิเตอร์ **ด้วยตนเอง** คุณจะได้รับข้อความแจ้งให้คุณป้อนรหัสการเช่าก่อนที่คุณจะดำเนินการคัดลอกการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="0f854-144">เลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="0f854-144">Select **Copy**.</span></span> <span data-ttu-id="0f854-145">รายละเอียดการเช่าจากการเช่าที่เลือกจะถูกคัดลอกไปยังการเช่าใหม่</span><span class="sxs-lookup"><span data-stu-id="0f854-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="0f854-146">คุณสามารถแก้ไขรายละเอียดของการเช่าใหม่ ก่อนที่คุณจะบันทึกและสร้างกำหนดการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="0f854-147">สมุดรายวันการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="0f854-147">Asset leasing journal</span></span>

<span data-ttu-id="0f854-148">รายการสมุดรายวันทั้งหมดที่สร้างขึ้นในการเช่าสินทรัพย์มีอยู่ในสมุดรายวันการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="0f854-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="0f854-149">ในหน้า **สมุดรายวันการเช่าสินทรัพย์** (**การเช่าสินทรัพย์ \> รายการสมุดรายวัน \> สมุดรายวันการเช่าสินทรัพย์**) คุณสามารถกรองข้อมูลโดยใช้สถานะการลงรายการบัญชี ดูรายการสมุดรายวันเฉพาะและใบสำคัญ และลงรายการบัญชีรายการสมุดรายวันที่ยังไม่ได้ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="0f854-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="0f854-150">ไม่สามารถสร้างสมุดรายวันการเช่าสินทรัพย์ด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="0f854-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="0f854-151">จะมีการสร้างขึ้นโดยอัตโนมัติเมื่อมีการสร้างกำหนดการเช่า</span><span class="sxs-lookup"><span data-stu-id="0f854-151">It's automatically created when lease schedules are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]