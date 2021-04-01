---
title: การแบ่งงาน
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับฟังก์ชันการแบ่งงาน ฟังก์ชันนี้ช่วยให้คุณสามารถแบ่งใบสั่งงานที่มีขนาดใหญ่เป็นใบสั่งงานที่มีขนาดเล็กซึ่งคุณสามารถกำหนดให้กับผู้ปฏิบัติงานคลังสินค้าได้หลายคน ด้วยวิธีนี้ งานเดียวกันสามารถถูกเลือกได้พร้อม ๆ กันโดยผู้ปฏิบัติงานคลังสินค้าหลายแห่ง
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6dbf0f6dd0c691db74eaad2174d8f9849b4cb26a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245093"
---
# <a name="work-split"></a><span data-ttu-id="d02e6-105">การแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-105">Work split</span></span>

<span data-ttu-id="d02e6-106">ฟังก์ชันการแบ่งงานช่วยให้คุณสามารถแบ่งใบสั่งงานที่มีขนาดใหญ่ (คือใบสั่งงานที่มีหลายรายการ) เป็นรหัสงานที่มีขนาดเล็กซึ่งคุณสามารถกำหนดให้กับผู้ปฏิบัติงานคลังสินค้าได้หลายคน</span><span class="sxs-lookup"><span data-stu-id="d02e6-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="d02e6-107">ด้วยวิธีนี้ หมายเลขการสร้างงานเดียวกันสามารถถูกเลือกได้พร้อม ๆ กันโดยผู้ปฏิบัติงานคลังสินค้าหลายแห่ง</span><span class="sxs-lookup"><span data-stu-id="d02e6-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d02e6-108">คุณสามารถแบ่งได้เฉพาะใบสั่งงานที่มีสถานะ *เปิด* หรือ *อยู่ระหว่างดำเนินการ*</span><span class="sxs-lookup"><span data-stu-id="d02e6-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="d02e6-109">เปิดฟังก์ชันแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-109">Turn on the work split functionality</span></span>

<span data-ttu-id="d02e6-110">ก่อนที่คุณจะสามารถใช้ฟังก์ชันการแบ่งทำงานได้ คุณต้องเปิดใช้งานลักษณะการทำงานและลักษณะการทำงานของข้อกำหนดเบื้องต้นในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="d02e6-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="d02e6-111">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d02e6-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="d02e6-112">อันดับแรก ให้เปิดลักษณะการทำงาน *การบล็อคงานทั่วทั้งองค์กร* ข้อกำหนดเบื้องต้น ถ้าไม่ได้เปิดอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="d02e6-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="d02e6-113">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะนี้ในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d02e6-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="d02e6-114">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="d02e6-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d02e6-115">**ชื่อคุณลักษณะ:** *การบล็อคงานทั่วทั้งองค์กร*</span><span class="sxs-lookup"><span data-stu-id="d02e6-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="d02e6-116">เมื่อเปิดใช้งานลักษณะการทำงานนี้ จะมีการใช้การอัพเกรดข้อมูลโดยอัตโนมัติหลังจากที่เปิดใช้งานลักษณะการทำงานระหว่างนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d02e6-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="d02e6-117">ถัดไป ให้เปิดใช้งานคุณลักษณะ *การแบ่งงาน* ซึ่งแสดงรายการอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d02e6-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="d02e6-118">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="d02e6-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d02e6-119">**ชื่อลักษณะการทำงาน:** *การแบ่งงาน*</span><span class="sxs-lookup"><span data-stu-id="d02e6-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="d02e6-120">การเพิ่มประสิทธิภาพให้กับรายละเอียดงานและหน้างานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d02e6-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="d02e6-121">ลักษณะการทำงาน *การแบ่งงาน* จะเพิ่มปุ่มสองปุ่มต่อไปนี้ลงในแท็บ **งาน** ในบานหน้าต่างการดำเนินการของหน้า **รายละเอียดงาน** และ **งานนทั้งหมด**:</span><span class="sxs-lookup"><span data-stu-id="d02e6-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="d02e6-122">**แบ่งงาน** – แบ่งรหัสงานปัจจุบันออกเป็นรหัสงานขนาดเล็กหลายรหัสที่สามารถดำเนินการได้โดยผู้ปฏิบัติงานที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="d02e6-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="d02e6-123">**ยกเลิกรอบเวลาการแบ่งงาน** – ยกเลิกรอบเวลาการแบ่งงาน และทำให้งานนี้พร้อมใช้งานสำหรับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="d02e6-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="d02e6-124">![ปุ่มแบ่งงานและยกเลิกรอบเวลาการแบ่งงาน](media/Work_split_buttons.png "ปุ่มแบ่งงานและยกเลิกรอบเวลาการแบ่งงาน")</span><span class="sxs-lookup"><span data-stu-id="d02e6-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d02e6-125">ปุ่ม **แบ่งงาน** จะไม่พร้อมใช้งานถ้าเป็นไปตามเงื่อนไขใด ๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d02e6-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="d02e6-126">สถานะของงานเป็นสิ่งอื่นที่ไม่ใช่ *เปิด* หรือ *อยู่ระหว่างดำเนินการ*</span><span class="sxs-lookup"><span data-stu-id="d02e6-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="d02e6-127">รหัสคอนเทนเนอร์เชื่อมโยงกับรหัสงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="d02e6-128">(ไม่สามารถแยกคอนเทนเนอร์ได้ เนื่องจากจำเป็นต้องมีการดำเนินการทางกายภาพ)</span><span class="sxs-lookup"><span data-stu-id="d02e6-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="d02e6-129">งานเชื่อมโยงกับคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="d02e6-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="d02e6-130">ชนิดของใบสั่งงานเป็นสิ่งอื่นที่ไม่ใช่ชนิดใดชนิดหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d02e6-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="d02e6-131">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="d02e6-131">Sales orders</span></span>
>    - <span data-ttu-id="d02e6-132">การเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="d02e6-132">Raw material picking</span></span>
>    - <span data-ttu-id="d02e6-133">โอนย้ายการตัดสินค้า</span><span class="sxs-lookup"><span data-stu-id="d02e6-133">Transfer issue</span></span>
>
> - <span data-ttu-id="d02e6-134">งานกำลังถูกแบ่งโดยผู้ใช้รายอื่นอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="d02e6-134">The work is currently being split by another user.</span></span> <span data-ttu-id="d02e6-135">ถ้าคุณพยายามเปิดหน้าที่กำลังแบ่งสำหรับงานที่แบ่งโดยผู้ใช้รายอื่นอยู่แล้ว คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "งานที่มีรหัส \#\#\#\# ถูกแบ่งอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="d02e6-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="d02e6-136">ลองอีกครั้งในอีกสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="d02e6-136">Retry in a few minutes.</span></span> <span data-ttu-id="d02e6-137">ถ้าคุณได้รับข้อความนี้ต่อไป โปรดติดต่อผู้ควบคุมงาน"</span><span class="sxs-lookup"><span data-stu-id="d02e6-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="d02e6-138">เหตุผลการบล็อคงานใหม่ *การแบ่งงาน* บ่งชี้ว่ารหัสงานกำลังอยู่ระหว่างการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="d02e6-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="d02e6-139">ซึ่งแสดงทั้งบนหน้า **แบ่งงาน** และในแอปคลังสินค้าถ้าผู้ใช้พยายามทำงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="d02e6-140">เมื่อมีการใช้เหตุผลการบล็อค ชื่อของฟิลด์ **เวฟที่ถูกบล็อค** จากรหัสงานจะถูกเปลี่ยนเป็น **บล็อค**</span><span class="sxs-lookup"><span data-stu-id="d02e6-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="d02e6-141">เริ่มต้นการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-141">Initiate a work split</span></span>

<span data-ttu-id="d02e6-142">ลักษณะการทำงานนี้จะเพิ่มหน้า **แบ่งงาน** ใหม่ซึ่งช่วยให้ผู้ใช้สามารถแบ่งรายการงานจากรหัสงานได้</span><span class="sxs-lookup"><span data-stu-id="d02e6-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="d02e6-143">เมื่อมีการเปิดหน้าแรก แสดงว่าบรรทัดที่มีสถานะงาน *เปิด* และพร้อมสำหรับการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="d02e6-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="d02e6-144">ในบานหน้าต่างการดำเนินการ ให้เลือก **แบ่งงาน** เพื่อประมวลผลงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d02e6-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="d02e6-145">เมื่อต้องการแบ่งงาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d02e6-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="d02e6-146">เปิดหน้างานใดหน้าหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d02e6-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="d02e6-147">**รายละเอียดงาน** (**การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน**)</span><span class="sxs-lookup"><span data-stu-id="d02e6-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="d02e6-148">**งานทั้งหมด** (**การจัดการคลังสินค้า \> งาน \> งานทั้งหมด**)</span><span class="sxs-lookup"><span data-stu-id="d02e6-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="d02e6-149">ในกริด ให้เลือกรหัสงานที่จะแบ่ง</span><span class="sxs-lookup"><span data-stu-id="d02e6-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="d02e6-150">ฟิลด์ **ชนิดของใบสั่งงาน** ต้องถูกตั้งค่าเป็นค่าอย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d02e6-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="d02e6-151">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="d02e6-151">Sales orders</span></span>
    - <span data-ttu-id="d02e6-152">การเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="d02e6-152">Raw material picking</span></span>
    - <span data-ttu-id="d02e6-153">โอนย้ายการตัดสินค้า</span><span class="sxs-lookup"><span data-stu-id="d02e6-153">Transfer issue</span></span>

1. <span data-ttu-id="d02e6-154">บนบานหน้าต่างการดำเนินการในแท็บ **งาน** ในกลุ่ม **งาน** เลือก **แบ่งงาน**</span><span class="sxs-lookup"><span data-stu-id="d02e6-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="d02e6-155">หน้า **แบ่งงาน** จะปรากฏขึ้นและแสดงบรรทัดงานที่เปิดอยู่และพร้อมสำหรับการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="d02e6-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="d02e6-156">โดยค่าเริ่มต้น จะมีการแสดงเฉพาะรายการงานที่พร้อมใช้งานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d02e6-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="d02e6-157">ถ้าต้องการดูบรรทัดทั้งหมดสำหรับรหัสงาน (ตัวอย่างเช่น บรรทัดที่มีชนิดงานเป็น *วาง*) ให้เลือกกล่องกาเครื่องหมาย **แสดงบรรทัดทั้งหมด** เหนือกริด</span><span class="sxs-lookup"><span data-stu-id="d02e6-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="d02e6-158">ข้อความต่อไปนี้จะแสดงขึ้น: "ผู้ใช้ไม่สามารถประมวลผลรายการของงานได้จนกว่าคุณจะแบ่งและปิดหน้านี้เสร็จเรียบร้อยแล้ว"</span><span class="sxs-lookup"><span data-stu-id="d02e6-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="d02e6-159">ฟิลด์ **เหตุผลการบล็อคของงาน** สำหรับงานปัจจุบันจะถูกตั้งค่าเป็น *แบ่งงาน* และงานจะถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="d02e6-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="d02e6-160">![เหตุผลการบล็อค](media/Blocking_reason.png "เหตุผลการบล็อค")</span><span class="sxs-lookup"><span data-stu-id="d02e6-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="d02e6-161">เลือกบรรทัดที่จะลบออกจากรหัสงานปัจจุบันและเพิ่มไปยังรหัสงานใหม่</span><span class="sxs-lookup"><span data-stu-id="d02e6-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="d02e6-162">เหตุการณ์ต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="d02e6-162">The following events occur:</span></span>

    - <span data-ttu-id="d02e6-163">เมื่อคุณแบ่งงาน บรรทัดหรือบรรทัดที่เลือกจากรหัสงานดั้งเดิมจะถูกยกเลิกและคัดลอกไปยังรหัสงานใหม่</span><span class="sxs-lookup"><span data-stu-id="d02e6-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="d02e6-164">โครงสร้างแม่แบบงานที่มีอยู่และที่ตั้งของการสำรอง (และคู่การเบิกสินค้า/การสำรองในอนาคต) จะถูกรักษาไว้</span><span class="sxs-lookup"><span data-stu-id="d02e6-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="d02e6-165">ค่าสำหรับฟิลด์รหัสงานต่อไปนี้จะถูกคัดลอกจากงานดั้งเดิมไปยังงานใหม่:</span><span class="sxs-lookup"><span data-stu-id="d02e6-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="d02e6-166">รหัสจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="d02e6-166">Load ID</span></span>
        - <span data-ttu-id="d02e6-167">รหัสการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d02e6-167">Shipment ID</span></span>
        - <span data-ttu-id="d02e6-168">ชนิดใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-168">Work order type</span></span>
        - <span data-ttu-id="d02e6-169">หมายเลขใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="d02e6-169">Order number</span></span>
        - <span data-ttu-id="d02e6-170">ไซต์</span><span class="sxs-lookup"><span data-stu-id="d02e6-170">Site</span></span>
        - <span data-ttu-id="d02e6-171">คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="d02e6-171">Warehouse</span></span>
        - <span data-ttu-id="d02e6-172">ระดับความสำคัญของงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-172">Work priority</span></span>
        - <span data-ttu-id="d02e6-173">รหัสกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-173">Work pool ID</span></span>
        - <span data-ttu-id="d02e6-174">รหัสเวฟ</span><span class="sxs-lookup"><span data-stu-id="d02e6-174">Wave ID</span></span>
        - <span data-ttu-id="d02e6-175">หมายเลขการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-175">Work creation number</span></span>

    - <span data-ttu-id="d02e6-176">ฟิลด์ต่อไปนี้จะไม่ถูกคัดลอกไปยังรหัสงานใหม่:</span><span class="sxs-lookup"><span data-stu-id="d02e6-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="d02e6-177">**รหัสงาน** – สร้างรหัสงานใหม่จากลำดับหมายเลขที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="d02e6-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="d02e6-178">**สถานะงาน** - ฟิลด์นี้จะถูกตั้งค่าเป็น *เปิด*</span><span class="sxs-lookup"><span data-stu-id="d02e6-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="d02e6-179">**ล็อคโดย** – ฟิลด์นี้จะถูกตั้งค่าเป็นว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="d02e6-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="d02e6-180">**รหัสป้ายทะเบียนเป้าหมาย** – ฟิลด์นี้จะถูกปล่อยว่างไว้</span><span class="sxs-lookup"><span data-stu-id="d02e6-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="d02e6-181">**วันที่และเวลาที่สร้าง** - ฟิลด์นี้จะถูกตั้งค่าเป็นวันที่และเวลาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d02e6-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="d02e6-182">**เวฟ/การหยุดที่ถูกบล็อค** – ฟิลด์นี้จะคำนวณอีกครั้งสำหรับรหัสงานดั้งเดิมและรหัสงานใหม่</span><span class="sxs-lookup"><span data-stu-id="d02e6-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="d02e6-183">ในบานหน้าต่างการดำเนินการ ให้เลือก **แบ่งงาน**</span><span class="sxs-lookup"><span data-stu-id="d02e6-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="d02e6-184">ในขณะที่กำลังแบ่งงาน ข้อความต่อไปนี้จะแสดงขึ้น: "การประมวลผลการดำเนินงาน - แบ่งงาน"</span><span class="sxs-lookup"><span data-stu-id="d02e6-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="d02e6-185">ในขณะที่แสดงข้อความนี้ คุณสามารถยกเลิกการดำเนินงานได้ โดยการเลือก **ยกเลิก** ในกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="d02e6-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="d02e6-186">ถ้ากล่องกาเครื่องหมาย **แสดงบรรทัดทั้งหมด** ถูกล้าง บรรทัดที่ถูกแบ่งออกและยกเลิกจะไม่ปรากฏในกริดอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="d02e6-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="d02e6-187">ถ้าเลือกกล่องกาเครื่องหมายไว้ คุณจะเห็นว่าค่าของฟิลด์ **สถานะของงาน** สำหรับบรรทัดนั้นมีการเปลี่ยนแปลงเป็น *ยกเลิก* แล้ว</span><span class="sxs-lookup"><span data-stu-id="d02e6-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="d02e6-188">การแจ้งเตือนต่อไปนี้จะแสดงขึ้นเพื่อบ่งชี้ว่ามีการสร้างรหัสงานใหม่: "งาน \#\#\#\# สร้างขึ้นโดยการแบ่งออกจากงานต้นฉบับ \#\#\#\#"</span><span class="sxs-lookup"><span data-stu-id="d02e6-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="d02e6-189">รายการงานอื่น ๆ จากรหัสงานดั้งเดิม (เช่น รายการ *สำรอง*) มีการปรับปรุงตามต้องการเพื่อให้สะท้อนถึงรายการของงานที่ถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="d02e6-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="d02e6-190">ตัวอย่างเช่น ถ้ารหัสงานดั้งเดิมมีรายการ *สำรอง* สำหรับปริมาณ 15 รายการ และรายการ *การเบิกสินค้า* ที่มีปริมาณรวม 10 รายการถูกยกเลิก ปริมาณ *สำรอง* ใหม่ในรหัสงานดั้งเดิมในขณะนี้จะเป็น 5</span><span class="sxs-lookup"><span data-stu-id="d02e6-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="d02e6-191">งานใหม่จะไม่ถูกกำหนดให้กับผู้ใช้ใด ๆ ในทันที</span><span class="sxs-lookup"><span data-stu-id="d02e6-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="d02e6-192">อย่างไรก็ตาม คุณสามารถกำหนดให้กับผู้ใช้ในขณะนี้ ได้ตามความจำเป็น โดยใช้ฟังก์ชันมาตรฐานของหน้า **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="d02e6-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d02e6-193">คุณสามารถแบ่งได้เฉพาะรหัสงานที่มีรายการงานที่พร้อมใช้งานสองรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="d02e6-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="d02e6-194">ถ้าคุณเลือก **แบ่งงาน** เมื่อมีรายการงานเพียงรายการเดียว คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "รายการงานอย่างน้อยหนึ่งรายการต้องยังคงอยู่ในงานเริ่มต้น"</span><span class="sxs-lookup"><span data-stu-id="d02e6-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="d02e6-195">ในกรณีนี้ ไม่มีการแบ่งเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="d02e6-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="d02e6-196">จบการแบ่งงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-196">Finish a work split</span></span>

<span data-ttu-id="d02e6-197">ถ้าต้องการจบการแบ่งงาน เหตุผลการบล็อค *การแบ่งงาน* ต้องถูกนำออก</span><span class="sxs-lookup"><span data-stu-id="d02e6-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="d02e6-198">มีวิธีสองวิธีในการทำขั้นตอนนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="d02e6-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="d02e6-199">ผู้ใช้ที่เป็นผู้แบ่งงานจะปิดหน้า **การแบ่งงาน** โดยการเลือกปุ่ม **ปิด** (**X**) ในมุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="d02e6-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="d02e6-200">เมื่อปิดหน้า เหตุผลการบล็อค *การแบ่งงาน* ต้องถูกนำออก</span><span class="sxs-lookup"><span data-stu-id="d02e6-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="d02e6-201">สถานะ *ถูกบล็อค* ของงานนี้จะได้รับการคำนวณอีกครั้ง และถ้าไม่มีเหตุผลการบล็อคที่เหลืออยู่สำหรับงานนี้ งานจะไม่ถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="d02e6-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="d02e6-202">ผู้ใช้ใด ๆ เปิดรหัสงานและเลือกปุ่ม **ยกเลิกรอบเวลาการแบ่งงาน** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d02e6-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="d02e6-203">เหตุผลการบล็อค *การแบ่งงาน* จะถูกลบออกและสถานะ *ถูกบล็อค* ของงานนี้ได้รับการคำนวณอีกครั้ง เช่นเดียวกับเมื่อหน้า **แบ่งงาน** ปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="d02e6-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="d02e6-204">หลังจากเหตุผลการบล็อค *การแบ่งงาน* ถูกลบออก งานที่แบ่งแล้วสามารถเรียกใช้งานบนอุปกรณ์เคลื่อนที่ได้ ซึ่งกำหนดว่าสถานะ **ถูกบล็อค** ตั้งค่าเป็น *ไม่* บนรหัสงาน</span><span class="sxs-lookup"><span data-stu-id="d02e6-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="d02e6-205">การบล็อคผู้ใช้บนแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="d02e6-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="d02e6-206">ถ้าคุณพยายามใช้แอปคลังสินค้าเพื่อเรียกใช้งานการเบิกสินค้ากับรหัสงานที่กำลังแบ่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "งานที่มีรหัส \#\#\#\# ถูกแบ่งอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="d02e6-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="d02e6-207">ถ้าคุณได้รับข้อความนี้ ให้เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="d02e6-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="d02e6-208">คุณสามารถดำเนินการต่อเพื่อดำเนินการงานอื่น</span><span class="sxs-lookup"><span data-stu-id="d02e6-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="d02e6-209">การดำเนินงานที่ถูกบล็อคอื่น</span><span class="sxs-lookup"><span data-stu-id="d02e6-209">Other blocked operations</span></span>

<span data-ttu-id="d02e6-210">การดำเนินงานใด ๆ ที่ปรับเปลี่ยนรายการงาน ธุรกรรมสินค้าคงคลังของงาน หรือลิงค์การเติมสินค้าที่เกี่ยวข้องกับงานที่กำลังแบ่งจะล้มเหลว และจะมีการแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้: "งานที่มีรหัส \#\#\#\# ถูกแบ่งอยู่ในปัจจุบัน"</span><span class="sxs-lookup"><span data-stu-id="d02e6-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]