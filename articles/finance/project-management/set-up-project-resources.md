---
title: ตั้งค่าทรัพยากรโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตั้งค่าหรือการร้องขอทรัพยากรโครงการ
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760678"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="67bdb-103">ตั้งค่าทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="67bdb-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67bdb-104">คุณต้องตั้งค่าปฏิทินและเชื่อมโยงกับพนักงานหรือผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="67bdb-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="67bdb-105">ปฏิทินจะถูกใช้เพื่อจัดกำหนดการโครงการ และเวลาการทำงานของทรัพยากรที่ถูกจองให้กับโครงการ</span><span class="sxs-lookup"><span data-stu-id="67bdb-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="67bdb-106">ในระหว่างการตั้งค่าปฏิทิน ผู้จัดการโครงการสามารถดำเนินการจัดระดับทรัพยากรให้เป็นส่วนหนึ่งของการเพิ่มประสิทธิภาพของทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="67bdb-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="67bdb-107">ตามกำหนดการปฏิทิน ข้อจำกัดสามารถถูกวางไว้ในทรัพยากรได้ </span><span class="sxs-lookup"><span data-stu-id="67bdb-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="67bdb-108">คุณสามารถตั้งค่าปฏิทินได้ในหน้า **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="67bdb-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="67bdb-109">เมื่อคุณตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรโครงการ คุณสามารถเลือกจากผู้ปฏิบัติงานที่ทำงานในบริษัทที่คุณกำลังตั้งค่าทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="67bdb-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="67bdb-110">หรือคุณสามารถเลือกผู้ปฏิบัติงานจากบริษัทอื่น ๆ ภายในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="67bdb-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="67bdb-111">ผู้ปฏิบัติงานเหล่านี้ถูกเรียกว่าทรัพยากรระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="67bdb-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="67bdb-112">ขั้นตอนต่อไปนี้อธิบายวิธีการตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรโครงการภายในบริษัทของคุณและวิธีการตั้งค่าทรัพยากรโครงการระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="67bdb-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="67bdb-113">ตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="67bdb-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="67bdb-114">ในหน้า **ผู้ปฏิบัติงาน** ในรายการ **ผู้ปฏิบัติงาน** เลือกผู้ปฏิบัติงานที่คุณกำลังเพิ่มให้เป็นทรัพยากรโครงการ และเปิดเรกคอร์ดผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="67bdb-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="67bdb-115">ในบานหน้าต่างการดำเนินการ เลือก **โครงการ** &gt; **การตั้งค่า** &gt; **การตั้งค่าโครงการ**</span><span class="sxs-lookup"><span data-stu-id="67bdb-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="67bdb-116">เลือกปฏิทิน และจากนั้นให้ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="67bdb-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="67bdb-117">คุณยังสามารถระบุโครงการเริ่มต้นสำหรับทรัพยากร ให้เป็นชนิดของการกำหนดล่วงหน้า </span><span class="sxs-lookup"><span data-stu-id="67bdb-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="67bdb-118">การกำหนดล่วงหน้าสามารถถูกใช้เมื่อผู้จัดการทรัพยากร หรือผู้จัดการโครงการรู้ว่าโครงการใดทรัพยากรจะทำงานด้วยก่อนล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="67bdb-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="67bdb-119">การกำหนดล่วงหน้าอาจยังขึ้นอยู่กับคำขอของผู้สนับสนุนโครงการหรือลูกค้าอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="67bdb-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="67bdb-120">เพื่อกำหนดโครงการ ในหน้า **กำหนดโครงการ** บนแท็บ **โครงการ** ในรายการ **โครงการคงเหลือ** ให้เลือกโครงการที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="67bdb-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="67bdb-121">ตั้งค่าทรัพยากรระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="67bdb-121">Set up an intercompany resource</span></span>

<span data-ttu-id="67bdb-122">เมื่อคุณตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรระหว่างบริษัท คุณต้องดำเนินการตั้งค่าในบริษัทที่ให้ยืมและบริษัทที่ขอยืมให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="67bdb-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="67bdb-123">ในบริษัทที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="67bdb-123">In the lending company</span></span>

1. <span data-ttu-id="67bdb-124">ใน Finance ตรวจสอบว่าบริษัทที่ให้ยืมได้ถูกเลือกแล้วแล้วดำเนินการขั้นตอนในส่วนก่อนหน้าให้เสร็จสมบูรณ์ "ตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรโครงการ"</span><span class="sxs-lookup"><span data-stu-id="67bdb-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="67bdb-125">ในหน้า **การจัดทำบัญชีระหว่างบริษัท** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="67bdb-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="67bdb-126">ในฟิลด์ **รหัสนิติบุคคล** เลือกบริษัทที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="67bdb-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="67bdb-127">กรอกข้อมูลในฟิลด์ที่เหลือตามความเหมาะสม และจากนั้น เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="67bdb-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="67bdb-128">ในหน้า **ราคาโอน** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="67bdb-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="67bdb-129">ในฟิลด์ **นิติบุคคลที่ขอยืม** เลือกบริษัทที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="67bdb-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="67bdb-130">เมื่อต้องการให้บริษัทที่ขอยืมยืมเฉพาะทรัพยากรที่คุณสร้างไว้ในตอนต้นของส่วนนี้ ในฟิลด์ **ทรัพยากร** เลือกชื่อของทรัพยากรที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="67bdb-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="67bdb-131">เมื่อต้องการทำให้ทรัพยากรทั้งหมดในบริษัทที่ให้ยืมพร้อมใช้งานสำหรับบริษัทที่ขอยืม ให้เว้นฟิลด์ **ทรัพยากร** ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="67bdb-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="67bdb-132">ในหน้า **พารามิเตอร์การจัดการและการบัญชีโครงการ** บนแท็บ **ระหว่างบริษัท** ตั้งค่าตัวเลือก **เปิดใช้งานการจัดกำหนดการและแผ่นเวลาสำหรับพนักงานระหว่างบริษัท** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="67bdb-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="67bdb-133">ในบริษัทที่ขอยืม</span><span class="sxs-lookup"><span data-stu-id="67bdb-133">In the borrowing company</span></span>

- <span data-ttu-id="67bdb-134">ในหน้า **รายการทรัพยากร** ในตัวกรองการค้นหา ป้อนชื่อของทรัพยากรที่คุณสร้างไว้สำหรับบริษัทที่ให้ยืมเพื่อตรวจสอบว่าชื่อถูกรวมอยู่ในรายการทรัพยากรสำหรับบริษัทที่ขอยืม</span><span class="sxs-lookup"><span data-stu-id="67bdb-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="67bdb-135">ร้องขอทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="67bdb-135">Request project resources</span></span>
<span data-ttu-id="67bdb-136">ฟังก์ชันการจัดกำหนดการทรัพยากรโครงการอนุญาตให้เฉพาะผู้จัดการทรัพยากรสามารถกระจายทรัพยากรที่วางแผนไว้ในการมีส่วนร่วมหรือโครงการ</span><span class="sxs-lookup"><span data-stu-id="67bdb-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="67bdb-137">เมื่อต้องการเปิดใช้งานฟังก์ชันนี้ ให้ทำงานต่อไปนี้ให้เสร็จสมบูรณ์ หรือตรวจสอบว่าได้ทำเสร็จสมบูรณ์แล้ว:</span><span class="sxs-lookup"><span data-stu-id="67bdb-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="67bdb-138">ตั้งค่าลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="67bdb-138">Set up number sequences.</span></span>
- <span data-ttu-id="67bdb-139">ตั้งค่าลำดับงานสำหรับการจัดการและการบัญชีโครงการ</span><span class="sxs-lookup"><span data-stu-id="67bdb-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="67bdb-140">เปิดใช้งานลำดับงานคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="67bdb-140">Enable resource request workflows.</span></span>

<span data-ttu-id="67bdb-141">หลังจากที่คุณได้ตรวจสอบหรือทำเสร็จสมบูรณ์แล้ว คุณสามารถทำงานต่อไปนี้ให้เสร็จสมบูรณ์ได้ตามความจำเป็น:</span><span class="sxs-lookup"><span data-stu-id="67bdb-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="67bdb-142">สร้างคำขอทรัพยากรจากทรัพยากรที่วางแผนไว้แบบไม่ตายตัว</span><span class="sxs-lookup"><span data-stu-id="67bdb-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="67bdb-143">ตรวจสอบคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="67bdb-143">Monitor resource requests.</span></span>
- <span data-ttu-id="67bdb-144">เติมสินค้าตามคำขอทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="67bdb-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="67bdb-145">ร้องขอทรัพยากรที่วางแผนไว้จาก WBS</span><span class="sxs-lookup"><span data-stu-id="67bdb-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="67bdb-146">จองทรัพยากรให้กับโครงการโดยไม่มีคำขอสำหรับทรัพยากรที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="67bdb-146">Book resources to a project without having a request for a staffed resource.</span></span>
