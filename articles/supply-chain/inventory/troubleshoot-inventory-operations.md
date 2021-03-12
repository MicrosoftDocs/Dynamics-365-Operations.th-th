---
title: แก้ไขปัญหาการดําเนินงานสินค้าคงคลัง
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับการดําเนินงานสินค้าคงคลัง
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3a22229106753d265a90f0ef05f5ac82dc745bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967166"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="28289-103">แก้ไขปัญหาการดําเนินงานสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="28289-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28289-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับการดําเนินงานสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="28289-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="28289-105">ฉันไม่พบกล่องโต้ตอบแบบหล่นลง "ลำดับงาน" ของสมุดรายวันสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="28289-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="28289-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-106">Issue description</span></span>

<span data-ttu-id="28289-107">คุณไม่พบกล่องโต้ตอบแบบหล่นลง **ลำดับงาน** บนหน้าสมุดรายวัน หรือการดําเนินงานที่เกี่ยวข้องไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="28289-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="28289-108">ปัญหานี้อาจเกิดขึ้นได้สามเหตุผล ตามที่อธิบายไว้ในส่วนย่อยต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="28289-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="28289-109">การแก้ไขปัญหา 1</span><span class="sxs-lookup"><span data-stu-id="28289-109">Issue resolution 1</span></span>

<span data-ttu-id="28289-110">หากปัญหามีผลกับผู้ใช้ทั้งหมด ระบบอาจเกิดปัญหาขึ้นเนื่องจากลำดับงานของการอนุมัติไม่ได้ถูกมอบหมายให้กับชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="28289-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="28289-111">เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="28289-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="28289-112">ไปที่ **การจัดการสินค้าคงคลัง &gt; การตั้งค่า &gt; รายชื่อสมุดรายวัน &gt; สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="28289-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="28289-113">ในบานหน้าต่างรายการ เลือกชื่อสมุดรายวันเพื่อเปิดการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="28289-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="28289-114">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **ลำดับงานการอนุมัติ** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="28289-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="28289-115">ยืนยันหากคุณได้รับพร้อมท์ให้ยืนยันการเปลี่ยนแปลง ให้เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="28289-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="28289-116">ในฟิลด์ **ลำดับงาน** เลือกลำดับงานที่คุณต้องการใช้สำหรับชื่อสมุดรายวันที่เลือก</span><span class="sxs-lookup"><span data-stu-id="28289-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="28289-117">การแก้ไขปัญหา 2</span><span class="sxs-lookup"><span data-stu-id="28289-117">Issue resolution 2</span></span>

<span data-ttu-id="28289-118">ถ้าลำดับงานของคุณใช้รหัสที่เลือกเอง ปัญหาอาจเกิดขึ้นหลังจากที่คุณอัปเกรดระบบ</span><span class="sxs-lookup"><span data-stu-id="28289-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="28289-119">ตัวอย่างเช่น ในลำดับงานในสมุดรายวัน ปุ่ม **ส่ง** อาจเป็นสีเทา ดังนั้นคุณจึงไม่สามารถเลือกเพื่ออนุมัติการส่งได้</span><span class="sxs-lookup"><span data-stu-id="28289-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="28289-120">ถ้าปุ่ม **ส่ง** เป็นสีเทา ลำดับงานของคุณอาจมีการปรับแต่งเอง ซึ่งหมายความว่าวิธีการของลำดับงาน `canSubmitToWorkflow()` ใน `FormDataUtil` ถูกขยายออกไป</span><span class="sxs-lookup"><span data-stu-id="28289-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="28289-121">เมื่อต้องการแก้ไขปัญหานี้ ให้เปลี่ยนวิธีการที่คุณขยายวิธีการ `canSubmitToWorkflow()` เพื่อใช้โครงสร้างในตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="28289-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="28289-122">การแก้ไขปัญหา 3</span><span class="sxs-lookup"><span data-stu-id="28289-122">Issue resolution 3</span></span>

<span data-ttu-id="28289-123">หากปัญหามีผลกับผู้ใช้บางรายเท่านั้น ผู้ใช้ดังกล่าวอาจไม่มีสิทธิ์ความปลอดภัยที่ต้องใช้ในการรันการดําเนินงานของลำดับงานในสมุดรายวันสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="28289-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="28289-124">ตรวจสอบว่าผู้ใช้ที่ได้รับผลแต่ละรายมีสิทธิ์ความปลอดภัยของ *การรักษาลำดับงานของสมุดรายวันสินค้าคงคลัง* หรือไม่</span><span class="sxs-lookup"><span data-stu-id="28289-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="28289-125">โดยค่าเริ่มต้น สิทธิ์นี้จะได้รับมอบหมายเป็นหน้าที่ที่มีชื่อเดียวกัน และภาษีจะถูกใช้กับบทบาท *ผู้ปฏิบัติงานคลังสินค้า* และ *ผู้จัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="28289-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="28289-126">สมุดรายวันสินค้าคงคลังของฉันยังคงอยู่ในสถานะที่ล็อคโดยระบบ และชุดงานของลำดับงานไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="28289-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="28289-127">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-127">Issue description</span></span>

<span data-ttu-id="28289-128">หนึ่งในสมุดรายวันสินค้าคงคลังของคุณถูกล็อคไว้โดยการดําเนินงานบางอย่างและยังไม่ถูกปล่อยออกใช้</span><span class="sxs-lookup"><span data-stu-id="28289-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="28289-129">ตัวอย่างเช่น ถ้าเกิดข้อผิดพลาดที่ไม่รู้จักระหว่างการลงรายการบัญชี (ซึ่งเป็นการดําเนินการล็อคระบบ) สมุดรายวันอาจยังคงอยู่ในสถานะที่ระบบล็อค</span><span class="sxs-lookup"><span data-stu-id="28289-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="28289-130">ในกรณีนี้ ตัวจัดการรายการงานของลำดับงานจะส่งข้อผิดพลาดขณะตรวจสอบความถูกต้องของการล็อค</span><span class="sxs-lookup"><span data-stu-id="28289-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="28289-131">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-131">Issue resolution</span></span>

<span data-ttu-id="28289-132">เข้าสู่ระบบอินสแตนซ์ SQL Server ของ Supply Chain Management และตรวจสอบว่า **InventJournalTable.SystemBlocked** ถูกตั้งค่าเป็น *1* หรือไม่</span><span class="sxs-lookup"><span data-stu-id="28289-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="28289-133">ถ้าใช่ ให้ตรวจสอบให้แน่ใจว่าสมุดรายวันไม่ควรอยู่ในสถานะล็อค แล้วรีเซ็ต **InventJournalTable.SystemBlocked** เป็น *0*</span><span class="sxs-lookup"><span data-stu-id="28289-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="28289-134">ลำดับงานของสมุดรายวันสินค้าคงคลังของฉันจะไม่มีวันเสร็จสมบูรณ์ และสมุดรายวันไม่สามารถแก้ไขหรือลงรายการบัญชีได้</span><span class="sxs-lookup"><span data-stu-id="28289-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="28289-135">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-135">Issue description</span></span>

<span data-ttu-id="28289-136">หลังจากที่คุณส่งลำดับงานการอนุมัติสมุดรายวัน ลำดับงานจะหยุดตอบสนอง และคุณไม่สามารถแก้ไขหรือประมวลผลสมุดรายวันของคุณ</span><span class="sxs-lookup"><span data-stu-id="28289-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="28289-137">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-137">Issue resolution</span></span>

<span data-ttu-id="28289-138">มีหลายเหตุผลว่าเพราะเหตุใดการประมวลผลลำดับงานจึงอาจไม่สามารถเสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="28289-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="28289-139">ตรวจสอบปัญหาต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="28289-139">Check for the following issues:</span></span>

- <span data-ttu-id="28289-140">ไปที่ **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; ลำดับงานการบริหารสินค้าคงคลัง** และตรวจทานการตั้งค่าคอนฟิกของลำดับงานที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="28289-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="28289-141">สำหรับข้อมูลเพิ่มเติม ให้ดู [ลำดับงานการอนุมัติสมุดรายวันสินค้าคงคลัง](inventory-journal-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="28289-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="28289-142">ลำดับงานอาจพบข้อยกเว้นหรือข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="28289-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="28289-143">ทบทวนประวัติรายการงานของลำดับงานที่มีผลต่อการดูว่ารายการงานนั้นรวมข้อผิดพลาดของแอปพลิเคชันที่ยกเลิกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="28289-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="28289-144">สามารถอัพเดตหรือแก้ไขสมุดรายวันสินค้าคงคลังได้เฉพาะถ้าสมุดรายวันได้รับอนุมัติแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="28289-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="28289-145">ถ้าการเรียกคืนเปิดใช้งานอยู่ คุณสามารถลองเรียกคืนสมุดรายวันได้</span><span class="sxs-lookup"><span data-stu-id="28289-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="28289-146">การรันชุดงานลำดับงานอาจถูกระงับด้วยเหตุผลหลายประการ</span><span class="sxs-lookup"><span data-stu-id="28289-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="28289-147">เหตุผลบางเหตุผลเหล่านี้อาจเกิดจากปัญหากรอบงานลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="28289-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="28289-148">เงื่อนไขลำดับงานของสมุดรายวันสินค้าคงคลังใช้เฉพาะที่ระดับสมุดรายวันเท่านั้น ไม่ใช่ในระดับรายการ</span><span class="sxs-lookup"><span data-stu-id="28289-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="28289-149">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-149">Issue description</span></span>

<span data-ttu-id="28289-150">คุณอาจประสบกับปัญหานี้ตัวอย่างเช่น ถ้าคุณพยายามตั้งค่าเงื่อนไขลำดับงานของสมุดรายวันสินค้าคงคลังในยอดเงินต้นทุน</span><span class="sxs-lookup"><span data-stu-id="28289-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="28289-151">คุณตั้งค่าเงื่อนไขเพื่อให้รันขั้นตอนที่ 1 เฉพาะเมื่อยอดต้นทุนน้อยกว่า 100 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="28289-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="28289-152">จากนั้นคุณตั้งค่าเงื่อนไขอื่นเพื่อให้รันขั้นตอนที่ 2 เฉพาะเมื่อยอดต้นทุนมากกว่าหรือเท่ากับ 100 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="28289-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="28289-153">จากนั้นเมื่อรันลำดับงาน ประวัติลำดับงานบรรทัดจะแสดงเพียงรายการเดียว และเงื่อนไขแรกจะมีการประเมินเป็น *จริง* เสมอ ไม่ว่าค่าที่ถูกส่งจะเป็นอย่างไรก็ตาม</span><span class="sxs-lookup"><span data-stu-id="28289-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="28289-154">วิธีการแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-154">Issue workaround</span></span>

<span data-ttu-id="28289-155">ในรุ่นปัจจุบัน เงื่อนไขลำดับงานของสมุดรายวันสินค้าคงคลังใช้เฉพาะที่ระดับสมุดรายวันเท่านั้น ไม่ใช่ในระดับรายการ</span><span class="sxs-lookup"><span data-stu-id="28289-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="28289-156">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="28289-156">This behavior is by design.</span></span> <span data-ttu-id="28289-157">ขอแนะนาว่าคุณควรตั้งค่าเงื่อนไขของคุณบนแอททริบิวต์ระดับสมุดรายวันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="28289-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="28289-158">บานหน้าต่างตัวกรองในหน้ารายการคงเหลือไม่ได้กรองข้อมูลผลลัพธ์ตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="28289-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="28289-159">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-159">Issue description</span></span>

<span data-ttu-id="28289-160">ตัวกรองในบานหน้าต่างตัวกรองในหน้า **รายการคงเหลือ** ไม่ได้กรองข้อมูลผลลัพธ์ตามที่คุณคาดไว้</span><span class="sxs-lookup"><span data-stu-id="28289-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="28289-161">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-161">Issue resolution</span></span>

<span data-ttu-id="28289-162">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="28289-162">This behavior is by design.</span></span>

<span data-ttu-id="28289-163">หน้า **รายการปริมาณคงคลังคงเหลือ** ประกอบด้วยตารางปริมาณคงคลังคงเหลือที่มีรายละเอียด ซึ่งรวมมิติที่มีอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="28289-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="28289-164">อย่างไรก็ตาม รายการบนหน้านี้เป็นข้อมูลสรุป</span><span class="sxs-lookup"><span data-stu-id="28289-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="28289-165">ดังนั้น จึงอาจรวมแถวจากตารางต้นทางตามค่ารวมตามมิติที่แสดง</span><span class="sxs-lookup"><span data-stu-id="28289-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="28289-166">ตัวกรองที่ตั้งค่าบานหน้าต่างตัวกรองจะนำไปใช้กับตารางต้นทาง ไม่ใช่รายการที่รวม</span><span class="sxs-lookup"><span data-stu-id="28289-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="28289-167">ในบางครั้ง ลักษณะการดําเนินการนี้สามารถให้ผลลัพธ์ที่ไม่คาดคิดได้ ดังที่แสดงใน [ตัวอย่างเหล่านี้](inventory-on-hand-list.md#examples)</span><span class="sxs-lookup"><span data-stu-id="28289-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="28289-168">อย่างไรก็ตาม [ตัวกรองที่ระบุไว้ในกริด](inventory-on-hand-list.md#grid-filters) *จะถูก* ใช้กับรายการแบบรวม</span><span class="sxs-lookup"><span data-stu-id="28289-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="28289-169">ตัวกรองเหล่านี้รวมทั้ง QuickFilter ที่ด้านบนของกริด และตัวกรองสำหรับแต่ละส่วนหัวของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="28289-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="28289-170">หน่วยและปริมาณหน่วยไม่ถูกต้องในสมุดรายวันสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="28289-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="28289-171">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-171">Issue description</span></span>

<span data-ttu-id="28289-172">คุณอาจพบปัญหาอย่างใดอย่างหนึ่งหรือทั้งสองอย่างต่อไปนี้ เมื่อคุณใช้งานหน่วยและปริมาณในสมุดรายวันสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="28289-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="28289-173">คุณไม่เห็นหน่วยหรือปริมาณต่อหน่วยในสมุดรายวันสินค้าคงคลังขณะที่ตั้งค่าหน่วยของการแปลงไว้เกี่ยวกับผลิตภัณฑ์ที่ปล่อยแล้ว และคุณไม่สามารถเปลี่ยนหน่วยในสมุดรายวันสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="28289-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="28289-174">คุณจะเห็นฟิลด์ **ปริมาณ** และ **หน่วย** ในสมุดรายวันสินค้าคงคลัง แต่คุณไม่เห็นฟิลด์ **ปริมาณหน่วย**</span><span class="sxs-lookup"><span data-stu-id="28289-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="28289-175">ถ้าคุณเปลี่ยนหน่วย ป้อนปริมาณ และลงรายการบัญชีสมุดรายวัน สมุดรายวันจะยังคงแสดงหน่วยวัดเดิมของปริมาณนั้น</span><span class="sxs-lookup"><span data-stu-id="28289-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="28289-176">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-176">Issue resolution</span></span>

<span data-ttu-id="28289-177">เพื่อแก้ไขปัญหานี้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="28289-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="28289-178">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** โปรดตรวจสอบให้แน่ใจว่าคุณลักษณะ *การใช้หน่วยวัดและปริมาณหน่วยในสมุดรายวันสินค้าคงคลัง* เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="28289-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="28289-179">ลักษณะการเช่นนี้จะเพิ่มฟิลด์ **หน่วย** และ **ปริมาณหน่วย** ลงในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="28289-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="28289-180">หลังจากที่เปิดคุณลักษณะ แล้ว ให้ใช้ฟิลด์ **ปริมาณ** **ปริมาณหน่วย** และ **หน่วย** ในลักษณะต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="28289-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="28289-181">**ปริมาณ** – ระบุปริมาณโดยใช้หน่วยเริ่มต้นที่กําหนดไว้เกี่ยวกับผลิตภัณฑ์ที่ปล่อย</span><span class="sxs-lookup"><span data-stu-id="28289-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="28289-182">อย่างไรก็ตาม ตัวหน่วยเริ่มต้นเองไม่ได้แสดงไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="28289-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="28289-183">ถ้ามีการตั้งค่าการแปลงระหว่างหน่วยเริ่มต้นและหน่วยที่เลือกในฟิลด์ **หน่วย** ฟิลด์ **ปริมาณ** จะถูกอัปเดตโดยอัตโนมัติ ตามการเลือกในฟิลด์ **ปริมาณหน่วย** และ **หน่วย**</span><span class="sxs-lookup"><span data-stu-id="28289-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="28289-184">**ปริมาณหน่วย** – ระบุปริมาณโดยใช้หน่วยที่เลือกไว้ในฟิลด์ **หน่วย**</span><span class="sxs-lookup"><span data-stu-id="28289-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="28289-185">**หน่วย** – เลือกหน่วยที่จะใช้กับค่าในฟิลด์ **ปริมาณหน่วย**</span><span class="sxs-lookup"><span data-stu-id="28289-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="28289-186">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "จํานวนทศนิยมสูงสุดที่หน่วยการเก็บสินค้าคงคลังเป็น 0"</span><span class="sxs-lookup"><span data-stu-id="28289-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="28289-187">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-187">Issue description</span></span>

<span data-ttu-id="28289-188">เมื่อคุณพยายามลงรายการบัญชีรายการความเคลื่อนไหวของสินค้าคงคลังหรือการจองสินค้าคงคลัง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "จํานวนทศนิยมสูงสุดในหน่วยการเก็บสต็อกคือ 0"</span><span class="sxs-lookup"><span data-stu-id="28289-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="28289-189">ปัญหานี้จะเกิดขึ้นเมื่อปริมาณรายการความเคลื่อนไหวของสินค้าคงคลังถูกระบุเป็นค่าทศนิยมที่ตด้านล่างระดับความแน่นอนที่ฟิลด์นี้สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="28289-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="28289-190">ตัวอย่างเช่น มีการระบุปริมาณเป็น *0.5* สำหรับธุรกรรมสินค้าคงคลัง แต่มีการสนับสนุนเฉพาะปริมาณจํานวนเต็มเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="28289-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="28289-191">ดังนั้น ค่าควรเป็น *1* แทน *0.5*</span><span class="sxs-lookup"><span data-stu-id="28289-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="28289-192">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="28289-192">Issue resolution</span></span>

1. <span data-ttu-id="28289-193">รันสคริปต์ต่อไปนี้บนอินสแตนซ์ SQL Server ของคุณเพื่อปัดเศษปริมาณในธุรกรรมสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="28289-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="28289-194">สคริปต์นี้จะแก้ไขค่าในตาราง **inventTrans**</span><span class="sxs-lookup"><span data-stu-id="28289-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="28289-195">รันการตรวจสอบความสอดคล้องกันของปริมาณคงเหลือเมื่อตัวเลือก **แก้ไขข้อผิดพลาด** เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="28289-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="28289-196">การตรวจสอบนี้จะแก้ไขค่าในตาราง **inventSum**</span><span class="sxs-lookup"><span data-stu-id="28289-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28289-197">เราขอแนะนาเป็นอย่างยิ่งให้คุณแก้ไขสคริปต์อย่างถี่ถ้วนตามความต้องการของสภาพแวดล้อมของคุณ ทดสอบสคริปต์ในสภาพแวดล้อมการทดสอบ แล้วตรวจสอบข้อมูลที่เป็นผลลัพธ์ก่อนที่คุณจะรันสคริปต์ในสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="28289-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>
