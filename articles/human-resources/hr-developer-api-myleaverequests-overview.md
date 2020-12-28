---
title: ภาพรวมของ MyLeaveRequests
description: เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420695"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="d95fd-103">ภาพรวมของ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="d95fd-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="d95fd-104">เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม</span><span class="sxs-lookup"><span data-stu-id="d95fd-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="d95fd-105">คีย์</span><span class="sxs-lookup"><span data-stu-id="d95fd-105">Key</span></span>

  | <span data-ttu-id="d95fd-106">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="d95fd-106">Property Name</span></span> | <span data-ttu-id="d95fd-107">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d95fd-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="d95fd-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="d95fd-108">dataAreaId</span></span>    | <span data-ttu-id="d95fd-109">สตริง</span><span class="sxs-lookup"><span data-stu-id="d95fd-109">String</span></span>    |
  | <span data-ttu-id="d95fd-110">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="d95fd-110">RequestId</span></span>     | <span data-ttu-id="d95fd-111">สตริง</span><span class="sxs-lookup"><span data-stu-id="d95fd-111">String</span></span>    |
  | <span data-ttu-id="d95fd-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="d95fd-112">LeaveType</span></span>     | <span data-ttu-id="d95fd-113">สตริง</span><span class="sxs-lookup"><span data-stu-id="d95fd-113">String</span></span>    |
  | <span data-ttu-id="d95fd-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="d95fd-114">LeaveDate</span></span>     | <span data-ttu-id="d95fd-115">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="d95fd-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="d95fd-116">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="d95fd-116">Properties</span></span>

  | <span data-ttu-id="d95fd-117">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="d95fd-117">Property Name</span></span>     | <span data-ttu-id="d95fd-118">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d95fd-118">Data Type</span></span> | <span data-ttu-id="d95fd-119">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="d95fd-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="d95fd-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="d95fd-120">dataAreaId</span></span>        | <span data-ttu-id="d95fd-121">สตริง</span><span class="sxs-lookup"><span data-stu-id="d95fd-121">String</span></span>    | <span data-ttu-id="d95fd-122">X</span><span class="sxs-lookup"><span data-stu-id="d95fd-122">X</span></span>        |
  | <span data-ttu-id="d95fd-123">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="d95fd-123">RequestId</span></span>         | <span data-ttu-id="d95fd-124">สตริง</span><span class="sxs-lookup"><span data-stu-id="d95fd-124">String</span></span>    | <span data-ttu-id="d95fd-125">X</span><span class="sxs-lookup"><span data-stu-id="d95fd-125">X</span></span>        |
  | <span data-ttu-id="d95fd-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="d95fd-126">LeaveType</span></span>         | <span data-ttu-id="d95fd-127">สตริง</span><span class="sxs-lookup"><span data-stu-id="d95fd-127">String</span></span>    | <span data-ttu-id="d95fd-128">X</span><span class="sxs-lookup"><span data-stu-id="d95fd-128">X</span></span>        |
  | <span data-ttu-id="d95fd-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="d95fd-129">LeaveDate</span></span>         | <span data-ttu-id="d95fd-130">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="d95fd-130">Date</span></span>      | <span data-ttu-id="d95fd-131">X</span><span class="sxs-lookup"><span data-stu-id="d95fd-131">X</span></span>        |
  | <span data-ttu-id="d95fd-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="d95fd-132">ReasonCodeId</span></span>      | <span data-ttu-id="d95fd-133">สตริง</span><span class="sxs-lookup"><span data-stu-id="d95fd-133">String</span></span>    |          |
  | <span data-ttu-id="d95fd-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="d95fd-134">PersonnelNumber</span></span>   | <span data-ttu-id="d95fd-135">สตริง</span><span class="sxs-lookup"><span data-stu-id="d95fd-135">String</span></span>    | <span data-ttu-id="d95fd-136">X</span><span class="sxs-lookup"><span data-stu-id="d95fd-136">X</span></span>        |
  | <span data-ttu-id="d95fd-137">วันที่คำขอ</span><span class="sxs-lookup"><span data-stu-id="d95fd-137">RequestDate</span></span>       | <span data-ttu-id="d95fd-138">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="d95fd-138">Date</span></span>      | <span data-ttu-id="d95fd-139">X</span><span class="sxs-lookup"><span data-stu-id="d95fd-139">X</span></span>        |
  | <span data-ttu-id="d95fd-140">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="d95fd-140">Comment</span></span>           | <span data-ttu-id="d95fd-141">สตริง</span><span class="sxs-lookup"><span data-stu-id="d95fd-141">String</span></span>    |          |
  | <span data-ttu-id="d95fd-142">สถานะ</span><span class="sxs-lookup"><span data-stu-id="d95fd-142">Status</span></span>            | <span data-ttu-id="d95fd-143">Enum</span><span class="sxs-lookup"><span data-stu-id="d95fd-143">Enum</span></span>      | <span data-ttu-id="d95fd-144">X</span><span class="sxs-lookup"><span data-stu-id="d95fd-144">X</span></span>        |
  | <span data-ttu-id="d95fd-145">จำนวน</span><span class="sxs-lookup"><span data-stu-id="d95fd-145">Amount</span></span>            | <span data-ttu-id="d95fd-146">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="d95fd-146">Real</span></span>      |          |
  | <span data-ttu-id="d95fd-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="d95fd-147">HalfDayDefinition</span></span> | <span data-ttu-id="d95fd-148">Enum</span><span class="sxs-lookup"><span data-stu-id="d95fd-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="d95fd-149">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d95fd-149">Actions</span></span>

 | <span data-ttu-id="d95fd-150">ชื่อการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="d95fd-150">Action Name</span></span>                               | <span data-ttu-id="d95fd-151">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d95fd-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="d95fd-152">ส่ง</span><span class="sxs-lookup"><span data-stu-id="d95fd-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="d95fd-153">ส่งคำขอที่จะประมวลผลโดยลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="d95fd-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d95fd-154">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="d95fd-154">See also</span></span>

- [<span data-ttu-id="d95fd-155">ส่งคำขอลางานไปที่ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="d95fd-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="d95fd-156">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d95fd-156">Authentication</span></span>](hr-developer-api-authentication.md)