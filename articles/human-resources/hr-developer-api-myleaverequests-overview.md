---
title: ภาพรวมของ MyLeaveRequests
description: เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115547"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="8f2b9-103">ภาพรวมของ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="8f2b9-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="8f2b9-104">เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม</span><span class="sxs-lookup"><span data-stu-id="8f2b9-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="8f2b9-105">คีย์</span><span class="sxs-lookup"><span data-stu-id="8f2b9-105">Key</span></span>

  | <span data-ttu-id="8f2b9-106">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="8f2b9-106">Property Name</span></span> | <span data-ttu-id="8f2b9-107">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8f2b9-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="8f2b9-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8f2b9-108">dataAreaId</span></span>    | <span data-ttu-id="8f2b9-109">สตริง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-109">String</span></span>    |
  | <span data-ttu-id="8f2b9-110">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="8f2b9-110">RequestId</span></span>     | <span data-ttu-id="8f2b9-111">สตริง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-111">String</span></span>    |
  | <span data-ttu-id="8f2b9-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="8f2b9-112">LeaveType</span></span>     | <span data-ttu-id="8f2b9-113">สตริง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-113">String</span></span>    |
  | <span data-ttu-id="8f2b9-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8f2b9-114">LeaveDate</span></span>     | <span data-ttu-id="8f2b9-115">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="8f2b9-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="8f2b9-116">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="8f2b9-116">Properties</span></span>

  | <span data-ttu-id="8f2b9-117">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="8f2b9-117">Property Name</span></span>     | <span data-ttu-id="8f2b9-118">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8f2b9-118">Data Type</span></span> | <span data-ttu-id="8f2b9-119">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="8f2b9-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="8f2b9-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8f2b9-120">dataAreaId</span></span>        | <span data-ttu-id="8f2b9-121">สตริง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-121">String</span></span>    | <span data-ttu-id="8f2b9-122">X</span><span class="sxs-lookup"><span data-stu-id="8f2b9-122">X</span></span>        |
  | <span data-ttu-id="8f2b9-123">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="8f2b9-123">RequestId</span></span>         | <span data-ttu-id="8f2b9-124">สตริง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-124">String</span></span>    | <span data-ttu-id="8f2b9-125">X</span><span class="sxs-lookup"><span data-stu-id="8f2b9-125">X</span></span>        |
  | <span data-ttu-id="8f2b9-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="8f2b9-126">LeaveType</span></span>         | <span data-ttu-id="8f2b9-127">สตริง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-127">String</span></span>    | <span data-ttu-id="8f2b9-128">X</span><span class="sxs-lookup"><span data-stu-id="8f2b9-128">X</span></span>        |
  | <span data-ttu-id="8f2b9-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8f2b9-129">LeaveDate</span></span>         | <span data-ttu-id="8f2b9-130">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="8f2b9-130">Date</span></span>      | <span data-ttu-id="8f2b9-131">X</span><span class="sxs-lookup"><span data-stu-id="8f2b9-131">X</span></span>        |
  | <span data-ttu-id="8f2b9-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="8f2b9-132">ReasonCodeId</span></span>      | <span data-ttu-id="8f2b9-133">สตริง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-133">String</span></span>    |          |
  | <span data-ttu-id="8f2b9-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="8f2b9-134">PersonnelNumber</span></span>   | <span data-ttu-id="8f2b9-135">สตริง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-135">String</span></span>    | <span data-ttu-id="8f2b9-136">X</span><span class="sxs-lookup"><span data-stu-id="8f2b9-136">X</span></span>        |
  | <span data-ttu-id="8f2b9-137">วันที่คำขอ</span><span class="sxs-lookup"><span data-stu-id="8f2b9-137">RequestDate</span></span>       | <span data-ttu-id="8f2b9-138">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="8f2b9-138">Date</span></span>      | <span data-ttu-id="8f2b9-139">X</span><span class="sxs-lookup"><span data-stu-id="8f2b9-139">X</span></span>        |
  | <span data-ttu-id="8f2b9-140">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="8f2b9-140">Comment</span></span>           | <span data-ttu-id="8f2b9-141">สตริง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-141">String</span></span>    |          |
  | <span data-ttu-id="8f2b9-142">สถานะ</span><span class="sxs-lookup"><span data-stu-id="8f2b9-142">Status</span></span>            | <span data-ttu-id="8f2b9-143">Enum</span><span class="sxs-lookup"><span data-stu-id="8f2b9-143">Enum</span></span>      | <span data-ttu-id="8f2b9-144">X</span><span class="sxs-lookup"><span data-stu-id="8f2b9-144">X</span></span>        |
  | <span data-ttu-id="8f2b9-145">จำนวน</span><span class="sxs-lookup"><span data-stu-id="8f2b9-145">Amount</span></span>            | <span data-ttu-id="8f2b9-146">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-146">Real</span></span>      |          |
  | <span data-ttu-id="8f2b9-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="8f2b9-147">HalfDayDefinition</span></span> | <span data-ttu-id="8f2b9-148">Enum</span><span class="sxs-lookup"><span data-stu-id="8f2b9-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="8f2b9-149">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="8f2b9-149">Actions</span></span>

 | <span data-ttu-id="8f2b9-150">ชื่อการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="8f2b9-150">Action Name</span></span>                               | <span data-ttu-id="8f2b9-151">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8f2b9-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="8f2b9-152">ส่ง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="8f2b9-153">ส่งคำขอที่จะประมวลผลโดยลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="8f2b9-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8f2b9-154">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="8f2b9-154">See also</span></span>

- [<span data-ttu-id="8f2b9-155">ส่งคำขอลางานไปที่ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="8f2b9-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="8f2b9-156">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8f2b9-156">Authentication</span></span>](hr-developer-api-authentication.md)