---
title: คำขอประเภทจากผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีการที่ผู้จัดจำหน่ายสามารถร้องขอประเภทการจัดซื้อให้กับบัญชีของพวกเขา และยังอธิบายกระบวนการอนุมัติที่เสร็จสมบูรณ์โดยเจ้าหน้าที่จัดซื้อด้วย
author: kamaybac
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fb3555e6d923fe37479c3204f0b78f7cdf510118
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938557"
---
# <a name="category-requests-from-vendors"></a><span data-ttu-id="88ffb-104">คำขอประเภทจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="88ffb-104">Category requests from vendors</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88ffb-105">กระบวนการร้องขอประเภทให้ผู้จัดจำหน่ายร้องขอที่ระเภทการจัดซื้อใหม่เชื่อมโยงกับบัญชีของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="88ffb-105">The category request process lets vendors request that new procurement categories be associated with their account.</span></span> <span data-ttu-id="88ffb-106">จากนั้นประเภทการจัดซื้อดังกล่าวสามารถใช้โดยกระบวนการจัดหาและการจัดซื้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="88ffb-106">Those procurement categories can then be used by the related procurement and sourcing processes.</span></span> <span data-ttu-id="88ffb-107">(สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของแค็ตตาล็อกการจัดซื้อ](procurement-catalogs.md))</span><span class="sxs-lookup"><span data-stu-id="88ffb-107">(For more information, see [Procurement catalogs overview](procurement-catalogs.md).)</span></span>

<span data-ttu-id="88ffb-108">คำขอประเภทเริ่มต้นโดยผู้จัดจำหน่ายในพื้นที่ทำงาน **ข้อมูลผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="88ffb-108">Category requests are initiated by vendors in the **Vendor information** workspace.</span></span> <span data-ttu-id="88ffb-109">จากนั้นกระบวนการเหล่านี้จะถูกส่งไปยังตัวแทนของคุณ เพื่อตรวจทานและอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="88ffb-109">They are then submitted to your agency for review and approval.</span></span> <span data-ttu-id="88ffb-110">ประเภทที่อนุมัติแล้วจะถูกเพิ่มเข้าในรายการประเภทการจัดซื้อของบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="88ffb-110">Approved categories are added to the list of procurement categories for the vendor's account.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="88ffb-111">เปิดใช้งานคุณลักษณะการทำงานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="88ffb-111">Turn on the feature in your system</span></span>

<span data-ttu-id="88ffb-112">ถ้าระบบของคุณยังไม่ได้รวมคุณลักษณะที่อธิบายไว้ในหัวข้อนี้ ให้ไปที่ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดคุณลักษณะ *อนุญาตให้ผู้จัดจำหน่ายสามารถใช้ประเภทการจัดซื้อผ่านการทำงานร่วมกันกับผู้จัดจำหน่าย*</span><span class="sxs-lookup"><span data-stu-id="88ffb-112">If your system doesn't already include the feature that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Allow vendors to apply for procurement categories through vendor collaboration* feature.</span></span>

<span data-ttu-id="88ffb-113">หลังจากที่เปิดคุณลักษณะแล้ว คุณยังคงสามารถเพิ่มประเภทการจัดซื้อในบัญชีผู้จัดจำหน่ายได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="88ffb-113">After the feature is turned on, you can still manually add procurement categories to vendor accounts.</span></span> <span data-ttu-id="88ffb-114">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [อนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อเฉพาะ](tasks/approve-vendors-specific-procurement-categories.md)</span><span class="sxs-lookup"><span data-stu-id="88ffb-114">For information, see [Approve vendors for specific procurement categories](tasks/approve-vendors-specific-procurement-categories.md).</span></span>

## <a name="vendor-collaboration-requirements"></a><span data-ttu-id="88ffb-115">ความต้องการของการทำงานร่วมกันกับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="88ffb-115">Vendor collaboration requirements</span></span>

<span data-ttu-id="88ffb-116">ต้องตั้งค่าการทำงานร่วมกันของผู้จัดจำหน่ายก่อนที่ผู้จัดจำหน่ายจะสามารถโต้ตอบกับการร้องขอประเภทได้</span><span class="sxs-lookup"><span data-stu-id="88ffb-116">Before a vendor can interact with category requests, it must be set up for vendor collaboration.</span></span>

<span data-ttu-id="88ffb-117">ผู้จัดจำหน่ายต้องมีผู้ใช้การทำงานร่วมงานกับผู้จัดจำหน่ายอย่างน้อยหนึ่งราย</span><span class="sxs-lookup"><span data-stu-id="88ffb-117">The vendor must have at least one vendor collaboration user.</span></span> <span data-ttu-id="88ffb-118">เฉพาะผู้ใช้ผู้จัดจำหน่ายที่มีบทบาทความปลอดภัยหนึ่งบทบาทหรือทั้งสองบทบาทต่อไปนี้เท่านั้น ที่สามารถสร้างและส่งการร้องขอประเภท:</span><span class="sxs-lookup"><span data-stu-id="88ffb-118">Only vendor users who have one or both of the following security roles can create and submit category requests:</span></span>

- <span data-ttu-id="88ffb-119">ผู้ติดต่อของผู้จัดจำหน่าย (ภายนอก)</span><span class="sxs-lookup"><span data-stu-id="88ffb-119">Vendor contact (external)</span></span>
- <span data-ttu-id="88ffb-120">ผู้ดูแลระบบผู้จัดจำหน่าย (ภายนอก)</span><span class="sxs-lookup"><span data-stu-id="88ffb-120">Vendor admin (external)</span></span>

<span data-ttu-id="88ffb-121">สำหรับข้อมูลเพิ่มเติม ดู [ตั้งค่าและรักษาการทำงานร่วมกันกับผู้จัดจำหน่าย](set-up-maintain-vendor-collaboration.md)</span><span class="sxs-lookup"><span data-stu-id="88ffb-121">For more information, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span>

## <a name="set-up-the-vendor-category-request-workflow"></a><span data-ttu-id="88ffb-122">ตั้งค่าเวิร์กโฟลว์การร้องขอประเภทของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="88ffb-122">Set up the Vendor category request workflow</span></span>

<span data-ttu-id="88ffb-123">เวิร์กโฟลว์ *การร้องขอประเภทของผู้จัดจำหน่าย* ต้องตั้งค่าในเวิร์กโฟลว์การจัดซื้อและการจัดหา</span><span class="sxs-lookup"><span data-stu-id="88ffb-123">The *Vendor category request* workflow must be set up in the procurement and sourcing workflows.</span></span> <span data-ttu-id="88ffb-124">ผู้จัดจำหน่ายจะส่งการขอประเภทใหม่ที่คุณสามารถตรวจทานและอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="88ffb-124">Vendors will submit new category requests that you can review and approve.</span></span> <span data-ttu-id="88ffb-125">มีการเพิ่มประเภทการจัดซื้อที่ร้องขอในบัญชีผู้จัดจำหน่ายหลังจากที่อนุมัติประเภทแล้ว</span><span class="sxs-lookup"><span data-stu-id="88ffb-125">Requested procurement categories are added to a vendor account after a category request is approved.</span></span>

<span data-ttu-id="88ffb-126">ตัวอย่างต่อไปนี้แสดงวิธีการตั้งค่าเวิร์กโฟลว์ *คำขอประเภทของผู้จัดจำหน่าย* ตัวอย่าง ที่มีผู้อนุมัติเพียงรายเดียว</span><span class="sxs-lookup"><span data-stu-id="88ffb-126">The following example shows how to set up a simple *Vendor category request* workflow that has a single approver.</span></span> <span data-ttu-id="88ffb-127">คุณต้องทบทวนกระบวนการภายในเพื่อระบุการตั้งค่าเวริ์กโฟลว์ที่เหมาะสมสำหรับตัวแทนของคุณ</span><span class="sxs-lookup"><span data-stu-id="88ffb-127">You must review your internal processes to determine the appropriate workflow setup for your agency.</span></span>

1. <span data-ttu-id="88ffb-128">ไปที่ **การจัดซื้อและการจัดหา \> การตั้งค่า \> เวิร์กโฟลว์การจัดซื้อและการจัดหา**</span><span class="sxs-lookup"><span data-stu-id="88ffb-128">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing workflows**.</span></span>
1. <span data-ttu-id="88ffb-129">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="88ffb-129">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="88ffb-130">ในกล่องโต้ตอบ ให้เลือก **เวิร์กโฟลว์คำขอประเภทของผู้จัดจำหน่าย** เพื่อเปิดโปรแกรมแก้ไขเวิร์กโฟลว์</span><span class="sxs-lookup"><span data-stu-id="88ffb-130">In the dialog box, select **Vendor category request workflow** to open the workflow editor.</span></span>
1. <span data-ttu-id="88ffb-131">ล็อกอินเข้าสู่โปรแกรมแก้ไขเวิร์กโฟลว์</span><span class="sxs-lookup"><span data-stu-id="88ffb-131">Sign in to the workflow editor.</span></span>
1. <span data-ttu-id="88ffb-132">บนบานหน้าต่างการดำเนินการ เลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-132">On the Action Pane, select **Properties**.</span></span>
1. <span data-ttu-id="88ffb-133">บนหน้า **คุณสมบัติ** สำหรับเวิร์กโฟลว์ในฟิลด์คําแนะ **คำแนะนำในการส่ง** ให้ป้อนข้อความคําแนะนํา</span><span class="sxs-lookup"><span data-stu-id="88ffb-133">On the **Properties** page for the workflow, in the **Submission instructions** field, enter instruction text.</span></span> <span data-ttu-id="88ffb-134">คําแนะนําจะปรากฏต่อผู้จัดจำหน่าย เมื่อส่งคําขอประเภท</span><span class="sxs-lookup"><span data-stu-id="88ffb-134">The instructions will be visible to vendors when they submit a category request.</span></span>
1. <span data-ttu-id="88ffb-135">ปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-135">Close the **Properties** page.</span></span>
1. <span data-ttu-id="88ffb-136">ลากองค์ประกอบลำดับงาน **อนุมัติคำขอประเภทใหม่** ไปยังพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="88ffb-136">Drag the **Approve new category request** workflow element onto the canvas.</span></span>
1. <span data-ttu-id="88ffb-137">ลากลิงค์จากองค์ประกอบลำดับงาน **เริ่มต้น** ไปยังองค์ประกอบลำดับงาน **อนุมัติคำขอประเภทใหม่**</span><span class="sxs-lookup"><span data-stu-id="88ffb-137">Drag a link from the **Start** workflow element to the **Approve new category request** workflow element.</span></span>
1. <span data-ttu-id="88ffb-138">ลากลิงค์จากองค์ประกอบลำดับงาน **อนุมัติคำขอประเภทใหม่** ไปยังองค์ประกอบลำดับงาน **สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="88ffb-138">Drag a link from the **Approve new category request** workflow element to the **End** workflow element.</span></span>
1. <span data-ttu-id="88ffb-139">ดับเบิลแท็บ (หรือดับเบิลคลิก) องค์ประกอบลำดับงาน **อนุมัติคำขอประเภทใหม่**</span><span class="sxs-lookup"><span data-stu-id="88ffb-139">Double-tap (or double-click) the **Approve new category request** workflow element.</span></span>
1. <span data-ttu-id="88ffb-140">เลือกและระงับ (หรือคลิกขวา) องค์ประกอบลำดับงาน **ขั้นตอนที่ 1** แล้วเลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-140">Select and hold (or right-click) the **Step 1** workflow element, and then select **Properties**.</span></span>
1. <span data-ttu-id="88ffb-141">บนหน้า **คุณสมบัติ** สำหรับองค์ประกอบลำดับงาน ในฟิลด์ **ชื่อเรื่องรายการงาน** ให้ป้อนข้อความชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="88ffb-141">On the **Properties** page for the workflow element, in the **Work item subject** field, enter subject text.</span></span> <span data-ttu-id="88ffb-142">ข้อความนี้จะแสดงเป็นค่าของฟิลด์ **ชื่อเรื่อง** ในหน้า **รายการงานที่มอบหมายให้กับฉัน**</span><span class="sxs-lookup"><span data-stu-id="88ffb-142">This text will be shown as the value of the **Subject** field on the **Work items assigned to me** page.</span></span>
1. <span data-ttu-id="88ffb-143">ในฟิลด์ **คำแนะนำรายการงาน** ให้ป้อนข้อความคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="88ffb-143">In the **Work item instructions** field, enter instruction text.</span></span> <span data-ttu-id="88ffb-144">คําแนะนําจะมองเห็นได้ต่อผู้อนุมัติ เมื่อผู้อนุมัติเลือก **ลำดับงาน** ในบานหน้าต่างการดำเนินการของคําขอประเภท</span><span class="sxs-lookup"><span data-stu-id="88ffb-144">The instructions will be visible to approvers when they select **Workflow** on the Action Pane of a category request.</span></span>
1. <span data-ttu-id="88ffb-145">ในบานหน้าต่างด้านซ้าย ให้เลือก **การกำหนด**</span><span class="sxs-lookup"><span data-stu-id="88ffb-145">In the left pane, select **Assignment**.</span></span>
1. <span data-ttu-id="88ffb-146">บนแท็บ **ชนิดการกําหนด** ให้ตั้งค่า **กําหนดผู้ใช้ให้กับองค์ประกอบลำดับงานนี้** เป็น *ผู้ใช้*</span><span class="sxs-lookup"><span data-stu-id="88ffb-146">On the **Assignment type** tab, set **Assign users to this workflow element** to *User*.</span></span>
1. <span data-ttu-id="88ffb-147">บนแท็บ **ผู้ใช้** ในรายการ **ผู้ใช้ที่พร้อมใช้งาน** ให้เลือกผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="88ffb-147">On the **User** tab, in the **Available users** list, select an approver.</span></span> <span data-ttu-id="88ffb-148">ตัวอย่างเช่น เลือกผู้ใช้ในแผนกจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="88ffb-148">For example, select a user in the Procurement department.</span></span>
1. <span data-ttu-id="88ffb-149">เลือกปุ่มลูกศรขวา (**\>**) เพื่อย้ายการอนุมัติไปยังรายการ **ผู้ใช้ที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="88ffb-149">Select the right arrow button (**\>**) to move the approver to the **Selected users** list.</span></span>
1. <span data-ttu-id="88ffb-150">ปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-150">Close the **Properties** page.</span></span>
1. <span data-ttu-id="88ffb-151">เลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="88ffb-151">Select **Save and close**.</span></span>
1. <span data-ttu-id="88ffb-152">ในฟิลด์ **หมายเหตุเวอร์ชัน** ให้ป้อนหมายเหตุเกี่ยวลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="88ffb-152">In the **Version notes** field, enter notes about the workflow.</span></span>
1. <span data-ttu-id="88ffb-153">เลือก **ตกลง** เพื่อบันทึกลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="88ffb-153">Select **OK** to save the workflow.</span></span>
1. <span data-ttu-id="88ffb-154">ถ้าคุณพร้อมจะเริ่มต้นทดสอบลำดับงาน ให้เลือก **เปิดใช้งานเวอร์ชันใหม่**</span><span class="sxs-lookup"><span data-stu-id="88ffb-154">If you're ready to start to test the workflow, select **Activate the new version**.</span></span> <span data-ttu-id="88ffb-155">มิฉะนั้น เลือก **ไม่ต้องเรียกใช้เวอร์ชันใหม่**</span><span class="sxs-lookup"><span data-stu-id="88ffb-155">Otherwise, select **Do not activate the new version**.</span></span>
1. <span data-ttu-id="88ffb-156">ให้เลือก **ตกลง** เพื่อเสร็จสิ้นการตั้งค่าลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="88ffb-156">Select **OK** to complete the workflow setup.</span></span>

> [!TIP]
> <span data-ttu-id="88ffb-157">ถ้าตัวแทนของคุณไม่ต้องการอนุมัติคำร้องขอประเภท คุณควรตั้งค่าคอนฟิกลำดับงานเพื่อการอนุมัติอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="88ffb-157">If your agency doesn't require approval of category requests, you should configure the workflow for automatic approval.</span></span>

<span data-ttu-id="88ffb-158">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าลำดับงาน โปรดดูที่ [ภาพรวมของระบบลำดับงาน](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md)</span><span class="sxs-lookup"><span data-stu-id="88ffb-158">For more information about how to set up workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).</span></span>

## <a name="create-and-submit-a-category-request"></a><span data-ttu-id="88ffb-159">การสร้างและส่งคำร้องขอประเภท</span><span class="sxs-lookup"><span data-stu-id="88ffb-159">Create and submit a category request</span></span>

<span data-ttu-id="88ffb-160">ส่วนนี้อธิบายวิธีการที่ผู้จัดจำหน่ายสามารถใช้พื้นที่ทำงาน **ข้อมูลของผู้จัดจำหน่าย** เพื่อสร้าง แก้ไข ดู และส่งคำขอประเภทได้</span><span class="sxs-lookup"><span data-stu-id="88ffb-160">This section describes how vendors can use the **Vendor information** workspace to create, edit, view, and submit category requests.</span></span>

### <a name="start-a-new-request"></a><span data-ttu-id="88ffb-161">เริ่มต้นคำขอใหม่</span><span class="sxs-lookup"><span data-stu-id="88ffb-161">Start a new request</span></span>

<span data-ttu-id="88ffb-162">การเริ่มคำขอประเภทใหม่ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-162">To start a new category request, follow these steps.</span></span>

1. <span data-ttu-id="88ffb-163">ในพื้นที่ทำงาน **ข้อมูลของผู้จัดจำหน่าย** ให้เลือกไทล์ **คำร้องขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-163">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="88ffb-164">บนหน้า **คำขอประเภท** บนบานหน้าต่างการดำเนินการ ให้เลือก **คำขอประเภทใหม่**</span><span class="sxs-lookup"><span data-stu-id="88ffb-164">On the **Category requests** page, on the Action Pane, select **New category request**.</span></span>
1. <span data-ttu-id="88ffb-165">ในกล่องโต้ตอบ **คำขอประเภทใหม่** ให้ค้นหาประเภทที่คุณต้องการใช้โดยการนําทางแผนภูมิ และ/หรือ การใช้ตัวกรองข้อมูลที่ด้านบนของรายการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-165">In the **New category request** dialog box, find the category that you want to apply for by navigating the tree and/or using the filter at the top of the list.</span></span> <span data-ttu-id="88ffb-166">เลือกกล่องกาเครื่องหมายของแต่ละประเภทที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="88ffb-166">Select the checkbox for each relevant category.</span></span>

    <span data-ttu-id="88ffb-167">บันทึกคะแนนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88ffb-167">Note the following points:</span></span>

    - <span data-ttu-id="88ffb-168">ประเภทที่ใช้งานอยู่ในบัญชีผู้จัดจำหน่ายของคุณในปัจจุบันจะแสดงเป็นเลือกไว้ ไม่สามารถลบออกได้</span><span class="sxs-lookup"><span data-stu-id="88ffb-168">Categories that are currently active on your vendor account are shown as selected and can't be removed.</span></span>
    - <span data-ttu-id="88ffb-169">คุณสามารถร้องขอประเภทการจัดซื้อได้หลายประเภท ในหนึ่งประเภทที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="88ffb-169">You can request multiple procurement categories in a single category request.</span></span>

1. <span data-ttu-id="88ffb-170">เลือก **ตกลง** เพื่อสร้างดราฟท์คำขอ</span><span class="sxs-lookup"><span data-stu-id="88ffb-170">Select **OK** to create the draft request.</span></span>

    <span data-ttu-id="88ffb-171">ขณะนี้ ดราฟท์คำขอใหม่จะปรากฏขึ้นบนหน้า **คำขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-171">The new draft request now appears on the **Category requests** page.</span></span>

1. <span data-ttu-id="88ffb-172">เปิดคำขอแบบร่างใหม่เพื่อตรวจสอบและแก้ไขได้ตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-172">Open the new draft request to review and edit it as required.</span></span>

    - <span data-ttu-id="88ffb-173">เมื่อต้องการดูรายการของประเภทที่ปัจจุบันรวมอยู่ในคำงขอ ให้เลือกแท็บด่วน **ประเภทที่ขอ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-173">To view the list of categories that are currently included in the request, select the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="88ffb-174">เมื่อต้องการดูประเภทที่ใช้งานอยู่ของคุณ ให้เปิดกล่องแสดงข้อมูลย่อ **ประเภทที่ใช้งานอยู่** ทางด้านขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="88ffb-174">To view your active categories, open the **Active categories** FactBox on the right side of the page.</span></span>
    - <span data-ttu-id="88ffb-175">เมื่อต้องการเพิ่มประเภทในคำขอ ให้เลือก **เพิ่ม** บนแถบเครื่องมือบนแท็บด่วน **ประเภทที่ร้องขอ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-175">To add a category to the request, select **Add** on the toolbar on the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="88ffb-176">เมื่อต้องการลบประเภทออกจากคำงขอ ให้เลือกประเภทบนแท็บด่วน **ประเภทที่ร้องขอ** แล้วเลือก **ลบ** บนแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="88ffb-176">To remove a category from the request, select the category on the **Requested categories** FastTab, and then select **Remove** on the toolbar.</span></span>
    - <span data-ttu-id="88ffb-177">ถ้าต้องการแนบเอกสารกับคำขอ ให้เลือก **เอกสารแนบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-177">To attach a document to the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="88ffb-178">เอกสารที่แนบจะพร้อมใช้งานเพื่อให้ผู้อนุมัติ เมื่อตรวจทานคำขอประเภท</span><span class="sxs-lookup"><span data-stu-id="88ffb-178">Attached documents will be available to approvers when they review the category request.</span></span>
    - <span data-ttu-id="88ffb-179">ถ้าต้องการลบเอกสารแนบจากคำขอ ให้เลือก **เอกสารแนบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-179">To remove an attached document from the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="88ffb-180">เลือกเอกสารที่ต้องการลบ แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-180">Select the document to remove, and then select **Delete** on the Action Pane.</span></span>

1. <span data-ttu-id="88ffb-181">ถ้าคุณพร้อมที่จะส่งคำขอ ให้เลือก **ส่ง** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-181">If you're ready to submit the request, select **Submit** on the Action Pane.</span></span> <span data-ttu-id="88ffb-182">หรือ เพียงปิดหน้าและข้ามขั้นตอนที่เหลือของขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-182">Otherwise, just close the page and skip the remaining steps of this procedure.</span></span> <span data-ttu-id="88ffb-183">จากนั้นคุณสามารถกลับไปที่การร้องขอในภายหลังได้</span><span class="sxs-lookup"><span data-stu-id="88ffb-183">You can then return to the request later.</span></span>
1. <span data-ttu-id="88ffb-184">อ่านคําแนะนําในการส่งที่ปรากฏ แล้วเลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="88ffb-184">Read any submission instructions that appear, and then select **Submit**.</span></span>
1. <span data-ttu-id="88ffb-185">ในกล่อง **ความคิดเห็น** ป้อนข้อมูลเพิ่มเติมใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="88ffb-185">In the **Comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="88ffb-186">จากนั้น ให้เลือก **ส่ง** เพื่อเสร็จสิ้นคำขอ</span><span class="sxs-lookup"><span data-stu-id="88ffb-186">Then select **Submit** to complete the request.</span></span>

### <a name="edit-a-draft-or-recalled-request"></a><span data-ttu-id="88ffb-187">แก้ไขแบบร่างหรือที่เรียกคืนคำขอ</span><span class="sxs-lookup"><span data-stu-id="88ffb-187">Edit a draft or recalled request</span></span>

<span data-ttu-id="88ffb-188">เมื่อต้องการแก้ไขแบบร้างหรือเรียกคืนคำขอประเภท ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-188">To edit a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="88ffb-189">ในพื้นที่ทำงาน **ข้อมูลของผู้จัดจำหน่าย** ให้เลือกไทล์ **คำร้องขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-189">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="88ffb-190">เลือกคำขอแบบร่างหรือคำขอที่เรียกคืน เพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="88ffb-190">Select the draft or recalled request to open it.</span></span>
1. <span data-ttu-id="88ffb-191">แก้ไขคำขอตามที่ต้องการ แล้วปิดหรือส่งตามที่อธิบายไว้ในขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="88ffb-191">Edit the request as required, and then either close it or submit it as described in the previous procedure.</span></span>

### <a name="submit-a-draft-or-recalled-request"></a><span data-ttu-id="88ffb-192">ส่งแบบร่างคำขอหรือตำชอที่เรียกคืน</span><span class="sxs-lookup"><span data-stu-id="88ffb-192">Submit a draft or recalled request</span></span>

<span data-ttu-id="88ffb-193">เมื่อต้องการส่งแบบร้างหรือคำขอประเภทที่เรียกคืน ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-193">To submit a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="88ffb-194">ในพื้นที่ทำงาน **ข้อมูลของผู้จัดจำหน่าย** ให้เลือกไทล์ **คำร้องขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-194">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="88ffb-195">เลือกแบบร่างหรือคำขอที่เรียกคืนที่คุณต้องการส่ง</span><span class="sxs-lookup"><span data-stu-id="88ffb-195">Select the draft or recalled request that you want to submit.</span></span>
1. <span data-ttu-id="88ffb-196">บนบานหน้าต่างการดำเนินการ เลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="88ffb-196">On the Action Pane, select **Submit**.</span></span>
1. <span data-ttu-id="88ffb-197">อ่านคําแนะนําในการส่งที่ปรากฏ แล้วเลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="88ffb-197">Read any submission instructions that appear, and then select **Submit**.</span></span>
1. <span data-ttu-id="88ffb-198">ในกล่อง **ความคิดเห็น** ป้อนข้อมูลเพิ่มเติมใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="88ffb-198">In the **Comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="88ffb-199">จากนั้น ให้เลือก **ส่ง** เพื่อเสร็จสิ้นคำขอ</span><span class="sxs-lookup"><span data-stu-id="88ffb-199">Then select **Submit** to complete the request.</span></span>

    <span data-ttu-id="88ffb-200">สถานะของคำขอประเภทจะเปลี่ยนเป็นหนึ่งในค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88ffb-200">The status of the category request is changed to one of the following values:</span></span>

    - <span data-ttu-id="88ffb-201">_การตรวจทานที่ค้างอยู่_ – คำขออยู่ในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="88ffb-201">_Pending review_ – The request is in the workflow.</span></span>
    - <span data-ttu-id="88ffb-202">_การอนุมัติที่ค้างอยู่_ – จำเป็นต้องมีการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="88ffb-202">_Pending approval_ – Approval is required.</span></span>

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a><span data-ttu-id="88ffb-203">เรียกคืนคำขอที่ส่งแล้วที่ยังไม่ได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="88ffb-203">Recall a submitted request that hasn't yet been approved</span></span>

<span data-ttu-id="88ffb-204">เมื่อต้องการเรียกคืนคำขอประเภทที่ส่งแล้วแต่ยังไม่ได้รับการอนุมัติ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-204">To recall a category request that has been submitted but hasn't yet been approved, follow these steps.</span></span>

1. <span data-ttu-id="88ffb-205">ในพื้นที่ทำงาน **ข้อมูลของผู้จัดจำหน่าย** ให้เลือกไทล์ **คำร้องขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-205">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="88ffb-206">เลือกคำขอที่ค้างอยู่ที่คุณต้องการเรียกคืน</span><span class="sxs-lookup"><span data-stu-id="88ffb-206">Select the pending request that you want to recall.</span></span>
1. <span data-ttu-id="88ffb-207">บนบานหน้าต่างการดำเนินการ เลือก **เรียกคืน**</span><span class="sxs-lookup"><span data-stu-id="88ffb-207">On the Action Pane, select **Recall**.</span></span>
1. <span data-ttu-id="88ffb-208">ในกล่อง **ป้อนความคิดเห็น** ป้อนข้อมูลเพิ่มเติมใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="88ffb-208">In the **Enter a comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="88ffb-209">จากนั้น ให้เลือก **ส่ง** เพื่อเสร็จสิ้นคำขอ</span><span class="sxs-lookup"><span data-stu-id="88ffb-209">Then select **Submit** to complete the request.</span></span>

    <span data-ttu-id="88ffb-210">สถานะของคำขอประเภทจะเปลี่ยนเป็น _ยกเลิกแล้ว_</span><span class="sxs-lookup"><span data-stu-id="88ffb-210">The status of the category request is changed to _Canceled_.</span></span> <span data-ttu-id="88ffb-211">คำขอจะยังคงอยู่ในสถานะนี้จนกว่าคุณจะลบหรือส่งใหม่</span><span class="sxs-lookup"><span data-stu-id="88ffb-211">The request will remain in this status until you delete or resubmit it.</span></span>

### <a name="delete-a-draft-or-recalled-request"></a><span data-ttu-id="88ffb-212">ลบแบบร่างคำขอหรือตำชอที่เรียกคืน</span><span class="sxs-lookup"><span data-stu-id="88ffb-212">Delete a draft or recalled request</span></span>

<span data-ttu-id="88ffb-213">เมื่อต้องการลบแบบร้างหรือคำขอประเภทที่เรียกคืน ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-213">To delete a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="88ffb-214">ในพื้นที่ทำงาน **ข้อมูลของผู้จัดจำหน่าย** ให้เลือกไทล์ **คำร้องขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-214">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="88ffb-215">เลือกแบบร่างหรือคำขอที่เรียกคืนที่คุณต้องการลบ</span><span class="sxs-lookup"><span data-stu-id="88ffb-215">Select the draft or recalled request that you want to delete.</span></span>
1. <span data-ttu-id="88ffb-216">บนบานหน้าต่างการดำเนินการ ให้เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-216">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="88ffb-217">เลือก **ใช่** เพื่อยืนยันการลบ</span><span class="sxs-lookup"><span data-stu-id="88ffb-217">Select **Yes** to confirm the deletion.</span></span>

### <a name="view-completed-requests"></a><span data-ttu-id="88ffb-218">ดูคำขอที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88ffb-218">View completed requests</span></span>

<span data-ttu-id="88ffb-219">เมื่อต้องการดูคำขอที่เสร็จสมบูรณ์ ให้เปิดพื้นที่ทำงาน **ข้อมูลของผู้จัดจำหน่าย** และเลือกไทล์ **คำขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-219">To view completed requests, open the **Vendor information** workspace and select the **Category requests** tile.</span></span> <span data-ttu-id="88ffb-220">คำขอประเภทที่เสร็จสมบูรณ์แล้วจะมีสถานะใดสถานะหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88ffb-220">Category requests that have been completed will have one of the following statuses:</span></span>

- <span data-ttu-id="88ffb-221">_อนุมัติ_ - คำขอได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="88ffb-221">_Approved_ – The request was approved.</span></span> <span data-ttu-id="88ffb-222">เมื่อต้องการดูประเภทที่เพิ่มใหม่ ให้กลับไปยังพื้นที่งาน **ข้อมูลผู้จัดจำหน่าย** เปิดรายการแบบหล่นลง **รายละเอียดเพิ่มเติม** ในบานหน้าต่างด้านซ้าย แล้วเลือก **ประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-222">To view the newly added categories, go back to the **Vendor information** workspace, open the **More details** drop-down list in the left pane, and then select **Categories**.</span></span>
- <span data-ttu-id="88ffb-223">_ถูกปฏิเสธ_ – การร้องขอถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="88ffb-223">_Rejected_ – The request was rejected.</span></span> <span data-ttu-id="88ffb-224">คุณสามารถสร้างคำขอประเภทใหม่ได้ตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-224">You can create a new category request as required.</span></span>

## <a name="review-category-requests"></a><span data-ttu-id="88ffb-225">ตรวจทานคำขอประเภท</span><span class="sxs-lookup"><span data-stu-id="88ffb-225">Review category requests</span></span>

<span data-ttu-id="88ffb-226">ส่วนนี้อธิบายวิธีการอนุมัติ ปฏิเสธ และมอบหมายคำขอประเภทที่ผู้จัดจำหน่ายส่ง และวิธีการดูคำขอที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88ffb-226">This section explains how to approve, reject, and delegate category requests that vendors submitted, and how to view completed requests.</span></span> <span data-ttu-id="88ffb-227">การดำเนินการลำดับงานเหล่านี้ใช้คำขอประเภททั้งหมด</span><span class="sxs-lookup"><span data-stu-id="88ffb-227">These workflow actions are for the whole category request.</span></span>

### <a name="view-category-requests"></a><span data-ttu-id="88ffb-228">ดูคำขอประเภท</span><span class="sxs-lookup"><span data-stu-id="88ffb-228">View category requests</span></span>

<span data-ttu-id="88ffb-229">การดูคำขอประเภท ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-229">To view category requests, follow these steps.</span></span>

1. <span data-ttu-id="88ffb-230">ไปที่ **การจัดซื้อและการจัดหา \> ผู้จัดจำหน่าย \> คำขอการทำงานร่วมกันกับผู้จัดจำหน่าย \> คำขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-230">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>

    <span data-ttu-id="88ffb-231">หน้า **คำขอประเภท** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="88ffb-231">The **Category requests** page appears.</span></span> <span data-ttu-id="88ffb-232">มุมมองหน้าเริ่มต้นแสดงคภขอประเภทที่มีสถานะ *การดำเนินการที่ค้างอยู่*</span><span class="sxs-lookup"><span data-stu-id="88ffb-232">The default page view shows category requests that have a status of *Pending action*.</span></span>

1. <span data-ttu-id="88ffb-233">เมื่อต้องการดูคำขอทั้งหมด ให้เลือก *ทั้งหมด* ในฟิลด์ **แสดงคำขอ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-233">To view all requests, select *All* in the **Show requests** field.</span></span>
1. <span data-ttu-id="88ffb-234">เปิดคำขอเพื่อตรวจสอบและแก้ไขได้ตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-234">Open a request to review and edit it as required.</span></span>

    - <span data-ttu-id="88ffb-235">เมื่อต้องการดูรายการของประเภทที่ปัจจุบันรวมอยู่ในคำงขอ ให้เลือกแท็บด่วน **ประเภทที่ขอ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-235">To view the list of categories that are currently included in the request, select the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="88ffb-236">เมื่อต้องการดูประเภทที่ใช้งานอยู่ ให้เปิดกล่องแสดงข้อมูลย่อ **ประเภทที่ใช้งานอยู่** ทางด้านขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="88ffb-236">To view the active categories, open the **Active categories** FactBox on the right side of the page.</span></span>
    - <span data-ttu-id="88ffb-237">ถ้ามีการส่งเอกสารแล้ว ปุ่ม  **สิ่งที่แนบ** (คลิปหนึบกระดาษ) ในบานหน้าต่างการดำเนินการจะแสดงการตรวจนับของเอกสารที่แนบ</span><span class="sxs-lookup"><span data-stu-id="88ffb-237">If documents were submitted, the  **Attachments** (paper clip) button on the Action Pane shows a count of the attached documents.</span></span> <span data-ttu-id="88ffb-238">เมื่อต้องการดูเอกสารที่แนบ ให้เลือกปุ่ม **เอกสารแนบ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-238">To view attached documents, select the **Attachments** button.</span></span> <span data-ttu-id="88ffb-239">แล้วเลือกเอกสารที่จะดู และเลือก **เปิด** เพื่อดู</span><span class="sxs-lookup"><span data-stu-id="88ffb-239">Then select the document to view and select **Open** to view it.</span></span>
    - <span data-ttu-id="88ffb-240">ถ้าต้องการแนบเอกสารกับคำขอ ให้เลือก **เอกสารแนบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-240">To attach a document to the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="88ffb-241">เอกสารที่แนบจะพร้อมใช้งานเพื่อให้ผู้อนุมัติ เมื่อตรวจทานคำขอประเภท</span><span class="sxs-lookup"><span data-stu-id="88ffb-241">Attached documents will be available to approvers when they review the category request.</span></span>
    - <span data-ttu-id="88ffb-242">ถ้าต้องการลบเอกสารแนบจากคำขอ ให้เลือก **เอกสารแนบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-242">To remove an attached document from the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="88ffb-243">เลือกเอกสารที่ต้องการลบ แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-243">Select the document to remove, and then select **Delete** on the Action Pane.</span></span>
    - <span data-ttu-id="88ffb-244">การดูประวัติลำดับงาน ให้เลือก **ลำดับงาน** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-244">To view the workflow history, select **Workflow** on the Action Pane.</span></span> <span data-ttu-id="88ffb-245">ในตัวเลือกลำดับงาน ให้เลือก **เพิ่มเติม** จากนั้น **ประวัติลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="88ffb-245">In the workflow options, select **More** and then **Workflow history**.</span></span> <span data-ttu-id="88ffb-246">หน้า **ประวัติลำดับงาน** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="88ffb-246">The **Workflow history** page appears.</span></span>

### <a name="approve-a-pending-category-request"></a><span data-ttu-id="88ffb-247">อนุมัติคำขอประเภทที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="88ffb-247">Approve a pending category request</span></span>

<span data-ttu-id="88ffb-248">เพื่ออนุมัติคำขอประเภทที่ค้างอยู่ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-248">To approve a pending category request, follow these steps.</span></span>

1. <span data-ttu-id="88ffb-249">ไปที่ **การจัดซื้อและการจัดหา \> ผู้จัดจำหน่าย \> คำขอการทำงานร่วมกันกับผู้จัดจำหน่าย \> คำขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-249">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="88ffb-250">เลือกคำขอที่ค้างอยู่ที่จะอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="88ffb-250">Select the pending request to approve.</span></span>
1. <span data-ttu-id="88ffb-251">ตรวจทานคำขอประเภท</span><span class="sxs-lookup"><span data-stu-id="88ffb-251">Review the category request.</span></span>
1. <span data-ttu-id="88ffb-252">ไม่บังคับ: บนแท็บด่วน **ทั่วไป** ในฟิลด์ **รหัสเหตุผล** ให้เลือกรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="88ffb-252">Optional: On the **General** FastTab, in the **Reason code** field, select a reason code.</span></span> <span data-ttu-id="88ffb-253">จากนั้น ในฟิลด์ **ข้อคิดเห็นเกี่ยวกับเหตุผล** ให้ป้อนข้อคิดเห็นเกี่ยวกับรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="88ffb-253">Then, in the **Reason comment** field, enter a comment about the reason code.</span></span>
1. <span data-ttu-id="88ffb-254">บนบานหน้าต่างการดำเนินการ เลือก **ลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="88ffb-254">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="88ffb-255">ในตัวเลือกลำดับงาน ให้เลือก **อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-255">In the workflow options, select **Approve**.</span></span>
1. <span data-ttu-id="88ffb-256">ในฟิลด์ **ความคิดเห็น** ป้อนข้อมูลเพิ่มเติมใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="88ffb-256">In the **Comment** field, enter any additional information that is required.</span></span> <span data-ttu-id="88ffb-257">จากนั้น ให้เลือก **อนุมัติ** เพื่อเสร็จสิ้นคำขอ</span><span class="sxs-lookup"><span data-stu-id="88ffb-257">Then select **Approve** to complete the request.</span></span>

    <span data-ttu-id="88ffb-258">สถานะของคำขอประเภทเปลี่ยนเป็น  _อนุมัติแล้ว_ และเพิ่มประเภทการจัดซื้อในบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="88ffb-258">The status of the category request is changed to _Approved_, and the procurement categories are added to the vendor account.</span></span>

### <a name="reject-a-pending-category-request"></a><span data-ttu-id="88ffb-259">ปฏิเสธคำขอประเภทที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="88ffb-259">Reject a pending category request</span></span>

<span data-ttu-id="88ffb-260">เพื่อปฏิเสธคำขอประเภทที่ค้างอยู่ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-260">To reject a pending category request, follow these steps.</span></span>

1. <span data-ttu-id="88ffb-261">ไปที่ **การจัดซื้อและการจัดหา \> ผู้จัดจำหน่าย \> คำขอการทำงานร่วมกันกับผู้จัดจำหน่าย \> คำขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-261">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="88ffb-262">เลือกคำขอที่ค้างอยู่ที่จะปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="88ffb-262">Select the pending request to reject.</span></span>
1. <span data-ttu-id="88ffb-263">ตรวจทานคำขอประเภท</span><span class="sxs-lookup"><span data-stu-id="88ffb-263">Review the category request.</span></span>
1. <span data-ttu-id="88ffb-264">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="88ffb-264">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="88ffb-265">บนแท็บด่วน **ทั่วไป** ในฟิลด์ **รหัสเหตุผล** ให้เลือกรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="88ffb-265">On the **General** FastTab, in the **Reason code** field, select a reason code.</span></span> <span data-ttu-id="88ffb-266">จากนั้น ในฟิลด์ **ข้อคิดเห็นเกี่ยวกับเหตุผล** ให้ป้อนข้อคิดเห็นเกี่ยวกับรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="88ffb-266">Then, in the **Reason comment** field, enter a comment about the reason code.</span></span>
1. <span data-ttu-id="88ffb-267">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="88ffb-267">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="88ffb-268">บนบานหน้าต่างการดำเนินการ เลือก **ลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="88ffb-268">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="88ffb-269">ในตัวเลือกลำดับงาน ให้เลือก **เพิ่มเติม** จากนั้น **ปฏิเสธ**</span><span class="sxs-lookup"><span data-stu-id="88ffb-269">In the workflow options, select **More** and then **Reject**.</span></span>
1. <span data-ttu-id="88ffb-270">ในฟิลด์ **ความคิดเห็น** ป้อนข้อมูลเพิ่มเติมใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="88ffb-270">In the **Comment** field, enter any additional information that is required.</span></span> <span data-ttu-id="88ffb-271">จากนั้น ให้เลือก **ปฏิเสธ** เพื่อเสร็จสิ้นคำขอ</span><span class="sxs-lookup"><span data-stu-id="88ffb-271">Then select **Reject** to complete the request.</span></span>

    <span data-ttu-id="88ffb-272">สถานะของคำขอประเภทจะเปลี่ยนเป็น _ปฏิเสธแล้ว_</span><span class="sxs-lookup"><span data-stu-id="88ffb-272">The status of the category request is changed to _Rejected_.</span></span> <span data-ttu-id="88ffb-273">ที่จุดนี้ ผู้จัดจำหน่ายสามารถสร้างคำขอประเภทใหม่ได้ ตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-273">At this point, the vendor can create a new category request as required.</span></span>

### <a name="delegate-a-pending-category-request"></a><span data-ttu-id="88ffb-274">การมอบหมายคำขอประเภทที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="88ffb-274">Delegate a pending category request</span></span>

<span data-ttu-id="88ffb-275">เพื่อมอบหมายคำขอประเภทที่ค้างอยู่ให้กับผู้ใช้อื่น ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-275">To delegate a pending category request to another user, follow these steps.</span></span>

1. <span data-ttu-id="88ffb-276">ไปที่ **การจัดซื้อและการจัดหา \> ผู้จัดจำหน่าย \> คำขอการทำงานร่วมกันกับผู้จัดจำหน่าย \> คำขอประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-276">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="88ffb-277">เลือกคำขอที่ค้างอยู่ที่คุณต้องการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="88ffb-277">Select the pending request that you want to approve.</span></span>
1. <span data-ttu-id="88ffb-278">บนบานหน้าต่างการดำเนินการ เลือก **ลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="88ffb-278">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="88ffb-279">ในตัวเลือกลำดับงาน ให้เลือก **เพิ่มเติม** จากนั้น **มอบหมาย**</span><span class="sxs-lookup"><span data-stu-id="88ffb-279">In the workflow options, select **More** and then **Delegate**.</span></span>
1. <span data-ttu-id="88ffb-280">ในฟิลด์ **ผู้ใช้** ให้เลือกผู้ใช้ที่จะมอบหมายคำขอประเภทเพื่อตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="88ffb-280">In the **User** field, select the user to assign the category request to for review.</span></span>
1. <span data-ttu-id="88ffb-281">ในฟิลด์ **ความคิดเห็น** ป้อนข้อมูลเพิ่มเติมใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="88ffb-281">In the **Comment** field, enter any additional information that is required.</span></span>
1. <span data-ttu-id="88ffb-282">เลือก **มอบหมาย** เพื่อดําเนินการมอบหมายให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88ffb-282">Select **Delegate** to complete the delegation.</span></span> <span data-ttu-id="88ffb-283">ขณะนี้ ผู้ใช้ที่เลือกสามารถตรวจทานคำขอประเภทได้</span><span class="sxs-lookup"><span data-stu-id="88ffb-283">The selected user can now review the category request.</span></span>

### <a name="view-procurement-categories-for-a-vendor"></a><span data-ttu-id="88ffb-284">ดูประเภทการจัดซื้อของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="88ffb-284">View procurement categories for a vendor</span></span>

<span data-ttu-id="88ffb-285">การดูประเภทการจัดซื้อสำหรับผู้จัดจำหน่ายหลังจากที่อนุมัติคำขอประเภทแล้ว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="88ffb-285">To view procurement categories for a vendor after a category request is approved, follow these steps.</span></span>

1. <span data-ttu-id="88ffb-286">ไปที่ **การจัดซื้อและการจัดหา \> ผู้จัดจำหน่าย \> ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="88ffb-286">Go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="88ffb-287">บนหน้า **ผู้จัดจำหน่ายทั้งหมด** ให้เลือกผู้จัดจำหน่ายที่คุณต้องการดูประเภทการจัดซื้อให้</span><span class="sxs-lookup"><span data-stu-id="88ffb-287">On the **All vendors** page, select the vendor that you want to view procurement categories for.</span></span>
1. <span data-ttu-id="88ffb-288">ในบานหน้าต่างการดำเนินการ ให้เปิดแท็บ **ทั่วไป** และ จากกลุ่ม **ตั้งค่า** ให้เลือก **ประเภท**</span><span class="sxs-lookup"><span data-stu-id="88ffb-288">On the Action Pane, open the **General** tab and, from the **Set up** group, select **Categories**.</span></span>

    <span data-ttu-id="88ffb-289">หน้า **ประเภท** ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="88ffb-289">The **Categories** page appears.</span></span> <span data-ttu-id="88ffb-290">แท็บด่วน **การจัดซื้อ** แสดงประเภทการจัดซื้อที่เพิ่ม ผ่านคำขอประเภท</span><span class="sxs-lookup"><span data-stu-id="88ffb-290">The **Procurement** FastTab shows procurement categories that were added through the category request.</span></span>

1. <span data-ttu-id="88ffb-291">บนแท็บด่วน **การจัดซื้อ** คุณสามารถเปลี่ยนแปลงได้ ถ้าต้องการ</span><span class="sxs-lookup"><span data-stu-id="88ffb-291">On the **Procurement** FastTab, you can make changes if needed.</span></span> <span data-ttu-id="88ffb-292">ตัวอย่างเช่น คุณสามารถตั้งค่าฟิลด์ **สถานะประเภทผุ้จัดจำหน่าย** เป็น _ที่ต้องการ_</span><span class="sxs-lookup"><span data-stu-id="88ffb-292">For example, you can set the **Vendor category status** field to _Preferred_.</span></span>
