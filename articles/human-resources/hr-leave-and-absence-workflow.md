---
title: สร้างลำดับงานคำขอลางาน
description: สร้างลำดับงานคำขอลางานและขาดงานเพื่อจัดการคำขอในการลาอย่างสม่ำเสมอใน Dynamics 365 Human Resources
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5580b4b07b2d335ad9444a064c726bc4aca1db6a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056551"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="8ee1f-103">สร้างลำดับงานคำขอลางาน</span><span class="sxs-lookup"><span data-stu-id="8ee1f-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8ee1f-104">คุณสามารถสร้างลำดับงานใน Dynamics 365 Human Resources เพื่อจัดการคำขอลางานและขาดงานอย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="8ee1f-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="8ee1f-105">ลำดับงาน **การลางานและการขาดงาน** ช่วยให้คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="8ee1f-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="8ee1f-106">กำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="8ee1f-106">Define tasks</span></span>
- <span data-ttu-id="8ee1f-107">กำหนดว่าใครต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8ee1f-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="8ee1f-108">ระบุว่าใครสามารถอนุมัติหรือปฏิเสธคำขอได้</span><span class="sxs-lookup"><span data-stu-id="8ee1f-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="8ee1f-109">สร้างลำดับงานคำขอลางานและขาดงาน</span><span class="sxs-lookup"><span data-stu-id="8ee1f-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="8ee1f-110">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="8ee1f-111">ภายใต้ **ตั้งค่า** โปรดเลือก **ลำดับงานของฝ่ายทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="8ee1f-112">โปรดเลือก **สร้าง** แล้วเลือก **คำขอลางานและขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="8ee1f-113">เมื่อกล่องข้อความ **เปิดไฟล์นี้หรือไม่** ปรากฏขึ้น โปรดเลือก **เปิด** และล็อกอินด้วยข้อมูลประจำตัวของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="8ee1f-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="8ee1f-114">ใช้โปรแกรมแก้ไขลำดับงานเพื่อสร้างลำดับงานสำหรับคำขอลางานของคุณ</span><span class="sxs-lookup"><span data-stu-id="8ee1f-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="8ee1f-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการทำงานกับลำดับงาน โปรดดูที่ [ภาพรวมของการสร้างลำดับงาน](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="8ee1f-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="8ee1f-116">องค์ประกอบข้อมูลลำดับงานคำขอลางานและขาดงาน</span><span class="sxs-lookup"><span data-stu-id="8ee1f-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="8ee1f-117">คุณสามารถใช้องค์ประกอบข้อมูลต่อไปนี้ในการสร้างการอนุมัติแบบมีเงื่อนไขหรือการอนุมัติโดยอัตโนมัติในลำดับงานสำหรับคำขอลางานและขาดงานได้:</span><span class="sxs-lookup"><span data-stu-id="8ee1f-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="8ee1f-118">**จำนวนเงิน**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-118">**Amount**</span></span>
- <span data-ttu-id="8ee1f-119">**ข้อคิดเห็น**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-119">**Comment**</span></span>
- <span data-ttu-id="8ee1f-120">**บริษัท**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-120">**Company**</span></span>
- <span data-ttu-id="8ee1f-121">**สร้างโดย**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-121">**Created by**</span></span>
- <span data-ttu-id="8ee1f-122">**วันที่และเวลาที่สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-122">**Created date and time**</span></span>
- <span data-ttu-id="8ee1f-123">**วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-123">**End date**</span></span>
- <span data-ttu-id="8ee1f-124">**ชนิดของการลางาน**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-124">**Leave type**</span></span>
- <span data-ttu-id="8ee1f-125">**แก้ไขโดย**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-125">**Modified by**</span></span>
- <span data-ttu-id="8ee1f-126">**วันที่และเวลาที่แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-126">**Modified date and time**</span></span>
- <span data-ttu-id="8ee1f-127">**รหัสเหตุผล**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-127">**Reason code**</span></span>
- <span data-ttu-id="8ee1f-128">**รหัสคำขอ**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-128">**Request ID**</span></span>
- <span data-ttu-id="8ee1f-129">**วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-129">**Start date**</span></span>
- <span data-ttu-id="8ee1f-130">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-130">**Status**</span></span> 
- <span data-ttu-id="8ee1f-131">**วันที่ส่ง**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-131">**Submission date**</span></span>
- <span data-ttu-id="8ee1f-132">**ส่งโดย**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-132">**Submitted by**</span></span>
- <span data-ttu-id="8ee1f-133">**ส่งโดยฝ่ายทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="8ee1f-134">**ส่งโดยผู้จัดการ**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="8ee1f-135">**ส่งในนามของ**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="8ee1f-136">**ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-136">**Worker**</span></span>
- <span data-ttu-id="8ee1f-137">**ชนิดผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="8ee1f-137">**Worker type**</span></span>

<span data-ttu-id="8ee1f-138">ตัวอย่างเหล่านี้แสดงวิธีการที่คุณสามารถสร้างเงื่อนไขลำดับงานชนิดต่างๆ โดยใช้องค์ประกอบข้อมูลเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="8ee1f-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="8ee1f-139">ใช้ **รหัสเหตุผล** ในรายงานแบบมีเงื่อนไขเพื่อกำหนดเส้นทางคำขอการลาป่วยที่มีรหัสเหตุผล **การผ่าตัด** ให้กับ HR เพื่อการอนุมัติ ในขณะที่กำหนดเส้นทางรหัสเหตุผลอื่นๆ ให้กับผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="8ee1f-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="8ee1f-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายงานแบบมีเงื่อนไข ให้ดู [ตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไขในลำดับงาน](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="8ee1f-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md).</span></span> 

- <span data-ttu-id="8ee1f-141">ใช้ **ส่งโดยทรัพยากรบุคคล** และ **ส่งโดยผู้จัดการ** ในการดำเนินการอัตโนมัติ เพื่ออนุมัติคำขอลางานโดยอัตโนมัติซึ่งบทบาทเหล่านี้ส่งในนามของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="8ee1f-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="8ee1f-142">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการดำเนินการอัตโนมัติ ให้ดู [ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="8ee1f-142">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="8ee1f-143">ใช้ **ชนิดการลางาน** ในรายงานแบบมีเงื่อนไข หรือการดำเนินการอัตโนมัติ เพื่อควบคุมวิธีลำดับงานกำหนดเส้นทางคำขอที่มีชนิดการลางานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8ee1f-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ee1f-144">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="8ee1f-144">See also</span></span>

- [<span data-ttu-id="8ee1f-145">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="8ee1f-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]