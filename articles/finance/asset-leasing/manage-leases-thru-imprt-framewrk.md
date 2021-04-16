---
title: จัดการสัญญาเช่าผ่านกรอบงานการนำเข้าสัญญาเช่า
description: หัวข้อนี้อธิบายวิธีการใช้กรอบงานการนำเข้าสัญญาเช่าเพื่อปรับปรุงสัญญาเช่าหลายสัญญาในเวลาเดียวกัน
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
ms.openlocfilehash: 26fb195ff18dc0c86d3546b782265043c2c78bf4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819805"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="60f00-103">จัดการสัญญาเช่าผ่านกรอบงานการนำเข้าสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="60f00-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60f00-104">หัวข้อนี้อธิบายวิธีการใช้กรอบงานการนำเข้าสัญญาเช่าเพื่อปรับปรุงสัญญาเช่าหลายสัญญาในขั้นตอนกัน</span><span class="sxs-lookup"><span data-stu-id="60f00-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="60f00-105">เมื่อใช้ความสามารถนี้ คุณจะสามารถประหยัดเวลาได้ และคุณยังสามารถตรวจสอบความถูกต้องของการปรับปรุงที่แม่นยำมากขึ้นได้โดยการลดโอกาสของข้อผิดพลาดของบุคคล</span><span class="sxs-lookup"><span data-stu-id="60f00-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="60f00-106">นอกจากนี้ ความสามารถนี้สามารถเชื่อมต่อ Microsoft Dynamics 365 Finance กับเอนทิตีข้อมูลจากภายนอกเพื่ออัปโหลดข้อมูลได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="60f00-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="60f00-107">คุณสามารถใช้เอนทิตีข้อมูลต่อไปนี้เพื่อรวมการเช่าสินทรัพย์กับระบบจากภายนอก:</span><span class="sxs-lookup"><span data-stu-id="60f00-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="60f00-108">การจัดเตรียมสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="60f00-108">Lease staging</span></span>
- <span data-ttu-id="60f00-109">การจัดเตรียมสัญญาการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="60f00-109">Payment contract staging</span></span>
- <span data-ttu-id="60f00-110">การจัดเตรียมสัญญาการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="60f00-110">Executory contract staging</span></span>

<span data-ttu-id="60f00-111">คุณสามารถใช้กระบวนการนำเข้าเพื่อปรับปรุงสัญญาเช่า อัปเดตข้อมูลที่ไม่ใช่ทางการเงิน หรือเพิ่มสัญญาเช่าใหม่</span><span class="sxs-lookup"><span data-stu-id="60f00-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="60f00-112">คุณสามารถดูและแก้ไขข้อมูลการเช่าได้ก่อนที่คุณจะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="60f00-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="60f00-113">ระบบสามารถรันกระบวนการสามขั้นตอนต่อไปนี้ผ่านชุดการนำเข้าสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="60f00-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="60f00-114">ชนิดของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="60f00-114">Process type</span></span>  | <span data-ttu-id="60f00-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="60f00-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="60f00-116">เพิ่มเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="60f00-116">Add record</span></span>    | <span data-ttu-id="60f00-117">สัญญาเช่าที่ย้ายที่มีชนิดของกระบวนการนี้สร้างสัญญาเช่าในระบบ</span><span class="sxs-lookup"><span data-stu-id="60f00-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="60f00-118">กำหนดการชำระเงินต้องยืนยันด้วยตนเอง และต้องลงรายการบัญชีสมุดรายวันการรับรู้เริ่มต้นด้วยตนเองหลังจากการโยกย้าย</span><span class="sxs-lookup"><span data-stu-id="60f00-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="60f00-119">อัพเดตเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="60f00-119">Update record</span></span> | <span data-ttu-id="60f00-120">สัญญาเช่าที่โยกย้ายซึ่งมีค่าฟิลด์การอัปเดตชนิดของกระบวนการนี้สำหรับสัญญาเช่าที่มีอยู่แล้วในระบบ</span><span class="sxs-lookup"><span data-stu-id="60f00-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="60f00-121">ฟิลด์ที่เลือกไว้บนหน้า **อัปเดตการเลือกฟิลด์** มีการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="60f00-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="60f00-122">เราขอแนะนำให้คุณเลือกฟิลด์ที่ไม่ใช่ทางการเงินบนหน้า **อัปเดตการเลือกฟิลด์** เนื่องจากชนิดของกระบวนการนี้จะไม่ปรับปรุงสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="60f00-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="60f00-123">ปรับปรุงเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="60f00-123">Adjust record</span></span> | <span data-ttu-id="60f00-124">สัญญาเช่าที่ย้ายที่มีชนิดของกระบวนการนี้ปรับปรุงสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="60f00-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="60f00-125">การปรับปรุงนี้ทำให้เกิดการปรับเปลี่ยนสัญญาเช่าทางการเงินของสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="60f00-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="60f00-126">หลังจากดำเนินการเช่าแล้ว ระบบจะสร้างกำหนดการชำระเงินใหม่โดยใช้ข้อมูลใหม่จากชุดการนำเข้าสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="60f00-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="60f00-127">ระบบไม่ได้ยืนยันกำหนดการชำระเงินหรือลงรายการบัญชีรายการสมุดรายวันการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="60f00-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="60f00-128">หลังจากที่อัพโหลดข้อมูลผ่าน พื้นที่ทำงาน **การจัดการข้อมูล** แล้ว ให้เปิดหน้า **นำเข้าส่วนหัว** (**การเช่าสินทรัพย์ \> กรอบงานการนำเข้าสัญญาเช่า \> นำเข้าส่วนหัว**)</span><span class="sxs-lookup"><span data-stu-id="60f00-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="60f00-129">หน้านี้จะแสดงรายการการนำเข้าทั้งหมดของเอนทิตีข้อมูลทั้งหมดที่แสดงรายการไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="60f00-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="60f00-130">ถ้าต้องการดูข้อมูลการแบ่งระยะสัญญาเช่าก่อนเรียกใช้การประมวลผล ให้เลือก **ข้อมูลการแบ่งระยะ**</span><span class="sxs-lookup"><span data-stu-id="60f00-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="60f00-131">ฟังก์ชันการเปรียบเทียบช่วยให้คุณสามารถเปรียบเทียบเรกคอร์ดที่คุณกำลังนำเข้ากับเรกคอร์ดที่เกี่ยวข้องซึ่งมีอยู่แล้วในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="60f00-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="60f00-132">ถ้าต้องการเปรียบเทียบเรกคอร์ดสัญญาเช่าแต่ละเรกคอร์ด ให้เลือกสัญญาเช่า แล้วเลือก **เปรียบเทียบ**</span><span class="sxs-lookup"><span data-stu-id="60f00-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="60f00-133">คุณควรทำขั้นตอนนี้ให้เสร็จสมบูรณ์เพื่อสร้างรายงาน **ความแตกต่าง** ก่อนที่คุณจะโอนย้ายเรกคอร์ดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="60f00-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="60f00-134">ฟังก์ชันเปรียบเทียบจะเปรียบเทียบค่าในข้อมูลการแบ่งระยะไปยังค่าสำหรับสัญญาเช่าที่อยู่ในระบบในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="60f00-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="60f00-135">ฟังก์ชันการเปรียบเทียบไม่ทำงานสำหรับสัญญาเช่าที่มีชนิดของกระบวนการ **เพิ่มเรกคอร์ด** เนื่องจากไม่มีสิ่งใดที่จะเปรียบเทียบกับสัญญาเช่านั้น</span><span class="sxs-lookup"><span data-stu-id="60f00-135">The Compare functionality doesn't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="60f00-136">ถ้าต้องการเปรียบเทียบสัญญาเช่าหลายสัญญาในเวลาเดียวกัน ไปที่ **การเช่าสินทรัพย์ \> กรอบงานการนำเข้าสัญญาเช่า \> เป็นระยะ \> เปรียบเทียบ**  และเลือก **เปรียบเทียบ**</span><span class="sxs-lookup"><span data-stu-id="60f00-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Compare**, and select **Compare**.</span></span>

<span data-ttu-id="60f00-137">สำหรับแต่ละเอนทิตี คุณสามารถดูความแตกต่างระหว่างสิ่งที่อยู่ในระบบในปัจจุบันและในตารางการแบ่งระยะ</span><span class="sxs-lookup"><span data-stu-id="60f00-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="60f00-138">สำหรับแต่ละเอนทิตีในตารางการแบ่งระยะ ให้เลือก **ดูความแตกต่าง**</span><span class="sxs-lookup"><span data-stu-id="60f00-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="60f00-139">กล่องโต้ตอบที่ปรากฏจะแสดงค่าปัจจุบันและค่าการแบ่งระยะที่นำเสนอ</span><span class="sxs-lookup"><span data-stu-id="60f00-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="60f00-140">นอกจากนี้คุณยังสามารถอัปเดตค่าการแบ่งระยะได้ด้วยการเปลี่ยนแปลงค่าในคอลัมน์ **ค่าใหม่** แล้วเลือก **อัปเดตการแบ่งระยะ**</span><span class="sxs-lookup"><span data-stu-id="60f00-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="60f00-141">คุณสามารถตรวจสอบความถูกต้องของสัญญาเช่าเพื่อให้แน่ใจว่าสามารถนำเรกคอร์ดลงในระบบได้โดยไม่มีการแนะนำข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="60f00-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="60f00-142">ก่อนที่จะมีการย้ายเรกคอร์ดสัญญาเช่า ระบบจะรันการตรวจสอบความถูกต้องหลายอย่างเพื่อให้แน่ใจว่ามีการนำเข้าเรกคอร์ดเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="60f00-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="60f00-143">ถ้าต้องการตรวจสอบความถูกต้องของสัญญาเช่าแต่ละรายการ ให้เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="60f00-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="60f00-144">ถ้าต้องการตรวจสอบความถูกต้องสัญญาเช่าหลายสัญญาในเวลาเดียวกัน ไปที่ **การเช่าสินทรัพย์ \> กรอบงานการนำเข้าสัญญาเช่า \> เป็นระยะ \> ตรวจสอบความถูกต้อง**  และเลือก **เปรียบเทียบ**</span><span class="sxs-lookup"><span data-stu-id="60f00-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="60f00-145">เมื่อต้องการประมวลผลสัญญาเช่าแต่ละรายการ ให้เลือก **โยกย้ายเรกคอร์ดสัญญาเช่า** ในหน้า **นำเข้าส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="60f00-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="60f00-146">เมื่อมีการโอนย้ายสัญญาเช่า ระบบจะดำเนินการการดำเนินการที่ระบุไว้ในฟิลด์ **ชนิดของกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="60f00-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="60f00-147">ถ้าต้องการตรวจสอบความถูกต้องสัญญาเช่าหลายสัญญาในเวลาเดียวกัน ไปที่ **การเช่าสินทรัพย์ \> กรอบงานการนำเข้าสัญญาเช่า \> เป็นระยะ \> ตรวจสอบความถูกต้อง**  และเลือก **เปรียบเทียบ**</span><span class="sxs-lookup"><span data-stu-id="60f00-147">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="60f00-148">หลังจากที่มีการเปรียบเทียบสัญญาเช่าแล้ว คุณสามารถรันรายงานเพื่อดูความแตกต่างของสัญญาเช่าแต่ละรายการที่รวมอยู่ในรหัสการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="60f00-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="60f00-149">ถ้าต้องการรันรายงานสำหรับสัญญาเช่าหนึ่ง ให้เลือกสัญญาเช่านั้นในข้อมูลการแบ่งระยะ แล้วเลือก **เปรียบเทียบและดูรายงาน \> รายงานความแตกต่าง**</span><span class="sxs-lookup"><span data-stu-id="60f00-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="60f00-150">ถ้าต้องการตรวจสอบความถูกต้องสัญญาเช่าหลายสัญญาในเวลาเดียวกัน ไปที่ **การเช่าสินทรัพย์ \> การสอบถามและรายงาน \> รายงานความแตกต่าง** และเลือก **เปรียบเทียบ**</span><span class="sxs-lookup"><span data-stu-id="60f00-150">To validate multiple leases at the same time, go to **Asset leasing \> Inquiries and reports \> Differences report**, and select **Compare**.</span></span>

## <a name="set-up-update-fields"></a><span data-ttu-id="60f00-151">ตั้งค่าฟิลด์อัปเดต</span><span class="sxs-lookup"><span data-stu-id="60f00-151">Set up update fields</span></span>

<span data-ttu-id="60f00-152">ถ้าคุณกำลังใช้กรอบงานการนำเข้าสัญญาเช่าเพื่ออัพเดตสัญญาเช่า และชนิดของกระบวนการคือ **อัปเดตเรกคอร์ด** คุณสามารถเลือกฟิลด์ที่ต้องการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="60f00-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="60f00-153">ไปที่การ **การเช่าสินทรัพย์ \> กรอบงานการนำเข้าสัญญาเช่า \> การตั้งค่า \> อัปเดตการเลือกฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="60f00-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="60f00-154">บนหน้าเว็บที่ปรากฏขึ้น ให้เลือกฟิลด์ที่จะอัปเดต แล้วเลือกลูกศรสีเขียวเพื่อย้ายไปยังรายการ **ฟิลด์ที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="60f00-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="60f00-155">เฉพาะฟิลด์ในรายการ **ฟิลด์ที่เลือก** สามารถอัปเดตได้โดยใช้ชุดการนำเข้าสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="60f00-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]