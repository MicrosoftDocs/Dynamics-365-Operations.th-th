---
title: สร้างลำดับงานคำขอซื้อและขายวันลา
description: สร้างลำดับงานคำขอซื้อและขายวันลาเพื่อจัดการคำขอซื้อและขายวันลาอย่างสอดคล้องกันใน Dynamics 365 Human Resources
author: andreabichsel
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ec21cda4779fea8c28b73d25842219da900da9d
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271504"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="01b60-103">สร้างลำดับงานคำขอซื้อและขายวันลา</span><span class="sxs-lookup"><span data-stu-id="01b60-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="01b60-104">คุณสามารถสร้างลำดับงานใน Dynamics 365 Human Resources เพื่อจัดการคำขอซื้อและขายวันลาอย่างสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="01b60-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="01b60-105">ลำดับงาน **ซื้อและขายวันลา** ให้คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="01b60-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="01b60-106">กำหนดงาน</span><span class="sxs-lookup"><span data-stu-id="01b60-106">Define tasks</span></span>
- <span data-ttu-id="01b60-107">กำหนดว่าใครต้องทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="01b60-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="01b60-108">ระบุว่าใครสามารถอนุมัติหรือปฏิเสธคำขอได้</span><span class="sxs-lookup"><span data-stu-id="01b60-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="01b60-109">สร้างลำดับงานคำขอซื้อและขายวันลา</span><span class="sxs-lookup"><span data-stu-id="01b60-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="01b60-110">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="01b60-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="01b60-111">ภายใต้ **ตั้งค่า** โปรดเลือก **ลำดับงานของฝ่ายทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="01b60-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="01b60-112">โปรดเลือก **สร้าง** แล้วเลือก **คำขอซื้อและขายวันลา**</span><span class="sxs-lookup"><span data-stu-id="01b60-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="01b60-113">เมื่อกล่องข้อความ **เปิดไฟล์นี้หรือไม่** ปรากฏขึ้น โปรดเลือก **เปิด** และล็อกอินด้วยข้อมูลประจำตัวของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="01b60-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="01b60-114">ใช้โปรแกรมแก้ไขลำดับงานเพื่อสร้างลำดับงานสำหรับคำขอลางานของคุณ</span><span class="sxs-lookup"><span data-stu-id="01b60-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="01b60-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการทำงานกับลำดับงาน โปรดดูที่ [ภาพรวมของการสร้างลำดับงาน](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="01b60-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="01b60-116">องค์ประกอบข้อมูลลำดับงานคำขอลางานและขาดงาน</span><span class="sxs-lookup"><span data-stu-id="01b60-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="01b60-117">คุณสามารถใช้องค์ประกอบข้อมูลต่อไปนี้ในการสร้างการอนุมัติแบบมีเงื่อนไขหรือการอนุมัติโดยอัตโนมัติในลำดับงานสำหรับคำขอซื้อและขายวันลา:</span><span class="sxs-lookup"><span data-stu-id="01b60-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="01b60-118">**จำนวนเงิน**</span><span class="sxs-lookup"><span data-stu-id="01b60-118">**Amount**</span></span>
- <span data-ttu-id="01b60-119">**นโยบายการซื้อและขายวันลางาน**</span><span class="sxs-lookup"><span data-stu-id="01b60-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="01b60-120">**บริษัท**</span><span class="sxs-lookup"><span data-stu-id="01b60-120">**Company**</span></span>
- <span data-ttu-id="01b60-121">**สร้างโดย**</span><span class="sxs-lookup"><span data-stu-id="01b60-121">**Created by**</span></span>
- <span data-ttu-id="01b60-122">**วันที่และเวลาที่สร้าง**</span><span class="sxs-lookup"><span data-stu-id="01b60-122">**Created date and time**</span></span>
- <span data-ttu-id="01b60-123">**วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="01b60-123">**End date**</span></span>
- <span data-ttu-id="01b60-124">**ชนิดของการลางาน**</span><span class="sxs-lookup"><span data-stu-id="01b60-124">**Leave type**</span></span>
- <span data-ttu-id="01b60-125">**ปรับเปลี่ยนโดย**</span><span class="sxs-lookup"><span data-stu-id="01b60-125">**Modified by**</span></span>
- <span data-ttu-id="01b60-126">**วันที่และเวลาที่แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="01b60-126">**Modified date and time**</span></span>
- <span data-ttu-id="01b60-127">**รหัสคำขอ**</span><span class="sxs-lookup"><span data-stu-id="01b60-127">**Request ID**</span></span>
- <span data-ttu-id="01b60-128">**วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="01b60-128">**Start date**</span></span>
- <span data-ttu-id="01b60-129">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="01b60-129">**Status**</span></span> 
- <span data-ttu-id="01b60-130">**วันที่ส่ง**</span><span class="sxs-lookup"><span data-stu-id="01b60-130">**Submission date**</span></span>
- <span data-ttu-id="01b60-131">**ส่งโดย**</span><span class="sxs-lookup"><span data-stu-id="01b60-131">**Submitted by**</span></span>
- <span data-ttu-id="01b60-132">**ส่งโดยฝ่ายทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="01b60-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="01b60-133">**ส่งโดยผู้จัดการ**</span><span class="sxs-lookup"><span data-stu-id="01b60-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="01b60-134">**ส่งในนามของ**</span><span class="sxs-lookup"><span data-stu-id="01b60-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="01b60-135">**ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="01b60-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="01b60-136">ตัวอย่างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="01b60-136">Workflow examples</span></span>

<span data-ttu-id="01b60-137">ตัวอย่างเหล่านี้แสดงวิธีการที่คุณสามารถสร้างเงื่อนไขลำดับงานชนิดต่างๆ โดยใช้องค์ประกอบข้อมูลเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="01b60-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="01b60-138">ใช้ **ส่งโดยฝ่ายทรัพยากรบุคคล** และ **ส่งโดยผู้จัดการ** ในการดำเนินการอัตโนมัติ เพื่ออนุมัติคำขอซื้อและขายวันลาโดยอัตโนมัติซึ่งบทบาทเหล่านี้ส่งในนามของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="01b60-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="01b60-139">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการดำเนินการอัตโนมัติ ให้ดู [ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="01b60-139">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="01b60-140">ใช้ **ชนิดการลางาน** ในรายงานแบบมีเงื่อนไข หรือการดำเนินการอัตโนมัติ เพื่อควบคุมวิธีลำดับงานกำหนดเส้นทางคำขอที่มีชนิดการลางานเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="01b60-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="01b60-141">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="01b60-141">See also</span></span>

[<span data-ttu-id="01b60-142">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="01b60-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="01b60-143">จัดการนโยบายซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="01b60-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[<span data-ttu-id="01b60-144">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="01b60-144">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
