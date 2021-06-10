---
title: ภาพรวมของ MyLeaveRequests
description: เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054967"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="65b0a-103">ภาพรวมของ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="65b0a-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="65b0a-104">เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม</span><span class="sxs-lookup"><span data-stu-id="65b0a-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="65b0a-105">คีย์</span><span class="sxs-lookup"><span data-stu-id="65b0a-105">Key</span></span>

  | <span data-ttu-id="65b0a-106">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="65b0a-106">Property Name</span></span> | <span data-ttu-id="65b0a-107">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="65b0a-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="65b0a-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="65b0a-108">dataAreaId</span></span>    | <span data-ttu-id="65b0a-109">สตริง</span><span class="sxs-lookup"><span data-stu-id="65b0a-109">String</span></span>    |
  | <span data-ttu-id="65b0a-110">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="65b0a-110">RequestId</span></span>     | <span data-ttu-id="65b0a-111">สตริง</span><span class="sxs-lookup"><span data-stu-id="65b0a-111">String</span></span>    |
  | <span data-ttu-id="65b0a-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="65b0a-112">LeaveType</span></span>     | <span data-ttu-id="65b0a-113">สตริง</span><span class="sxs-lookup"><span data-stu-id="65b0a-113">String</span></span>    |
  | <span data-ttu-id="65b0a-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="65b0a-114">LeaveDate</span></span>     | <span data-ttu-id="65b0a-115">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="65b0a-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="65b0a-116">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="65b0a-116">Properties</span></span>

  | <span data-ttu-id="65b0a-117">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="65b0a-117">Property Name</span></span>     | <span data-ttu-id="65b0a-118">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="65b0a-118">Data Type</span></span> | <span data-ttu-id="65b0a-119">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="65b0a-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="65b0a-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="65b0a-120">dataAreaId</span></span>        | <span data-ttu-id="65b0a-121">สตริง</span><span class="sxs-lookup"><span data-stu-id="65b0a-121">String</span></span>    | <span data-ttu-id="65b0a-122">X</span><span class="sxs-lookup"><span data-stu-id="65b0a-122">X</span></span>        |
  | <span data-ttu-id="65b0a-123">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="65b0a-123">RequestId</span></span>         | <span data-ttu-id="65b0a-124">สตริง</span><span class="sxs-lookup"><span data-stu-id="65b0a-124">String</span></span>    | <span data-ttu-id="65b0a-125">X</span><span class="sxs-lookup"><span data-stu-id="65b0a-125">X</span></span>        |
  | <span data-ttu-id="65b0a-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="65b0a-126">LeaveType</span></span>         | <span data-ttu-id="65b0a-127">สตริง</span><span class="sxs-lookup"><span data-stu-id="65b0a-127">String</span></span>    | <span data-ttu-id="65b0a-128">X</span><span class="sxs-lookup"><span data-stu-id="65b0a-128">X</span></span>        |
  | <span data-ttu-id="65b0a-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="65b0a-129">LeaveDate</span></span>         | <span data-ttu-id="65b0a-130">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="65b0a-130">Date</span></span>      | <span data-ttu-id="65b0a-131">X</span><span class="sxs-lookup"><span data-stu-id="65b0a-131">X</span></span>        |
  | <span data-ttu-id="65b0a-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="65b0a-132">ReasonCodeId</span></span>      | <span data-ttu-id="65b0a-133">สตริง</span><span class="sxs-lookup"><span data-stu-id="65b0a-133">String</span></span>    |          |
  | <span data-ttu-id="65b0a-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="65b0a-134">PersonnelNumber</span></span>   | <span data-ttu-id="65b0a-135">สตริง</span><span class="sxs-lookup"><span data-stu-id="65b0a-135">String</span></span>    | <span data-ttu-id="65b0a-136">X</span><span class="sxs-lookup"><span data-stu-id="65b0a-136">X</span></span>        |
  | <span data-ttu-id="65b0a-137">วันที่คำขอ</span><span class="sxs-lookup"><span data-stu-id="65b0a-137">RequestDate</span></span>       | <span data-ttu-id="65b0a-138">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="65b0a-138">Date</span></span>      | <span data-ttu-id="65b0a-139">X</span><span class="sxs-lookup"><span data-stu-id="65b0a-139">X</span></span>        |
  | <span data-ttu-id="65b0a-140">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="65b0a-140">Comment</span></span>           | <span data-ttu-id="65b0a-141">สตริง</span><span class="sxs-lookup"><span data-stu-id="65b0a-141">String</span></span>    |          |
  | <span data-ttu-id="65b0a-142">สถานะ</span><span class="sxs-lookup"><span data-stu-id="65b0a-142">Status</span></span>            | <span data-ttu-id="65b0a-143">Enum</span><span class="sxs-lookup"><span data-stu-id="65b0a-143">Enum</span></span>      | <span data-ttu-id="65b0a-144">X</span><span class="sxs-lookup"><span data-stu-id="65b0a-144">X</span></span>        |
  | <span data-ttu-id="65b0a-145">จำนวน</span><span class="sxs-lookup"><span data-stu-id="65b0a-145">Amount</span></span>            | <span data-ttu-id="65b0a-146">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="65b0a-146">Real</span></span>      |          |
  | <span data-ttu-id="65b0a-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="65b0a-147">HalfDayDefinition</span></span> | <span data-ttu-id="65b0a-148">Enum</span><span class="sxs-lookup"><span data-stu-id="65b0a-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="65b0a-149">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="65b0a-149">Actions</span></span>

 | <span data-ttu-id="65b0a-150">ชื่อการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="65b0a-150">Action Name</span></span>                               | <span data-ttu-id="65b0a-151">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="65b0a-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="65b0a-152">ส่ง</span><span class="sxs-lookup"><span data-stu-id="65b0a-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="65b0a-153">ส่งคำขอที่จะประมวลผลโดยลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="65b0a-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="65b0a-154">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="65b0a-154">See also</span></span>

- [<span data-ttu-id="65b0a-155">ส่งคำขอลางานไปที่ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="65b0a-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="65b0a-156">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="65b0a-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]