---
title: ภาพรวมของ MyLeaveRequests
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010727"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="88372-102">ภาพรวมของ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="88372-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="88372-103">เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม</span><span class="sxs-lookup"><span data-stu-id="88372-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="88372-104">คีย์</span><span class="sxs-lookup"><span data-stu-id="88372-104">Key</span></span>

  | <span data-ttu-id="88372-105">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="88372-105">Property Name</span></span> | <span data-ttu-id="88372-106">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="88372-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="88372-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="88372-107">dataAreaId</span></span>    | <span data-ttu-id="88372-108">สตริง</span><span class="sxs-lookup"><span data-stu-id="88372-108">String</span></span>    |
  | <span data-ttu-id="88372-109">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="88372-109">RequestId</span></span>     | <span data-ttu-id="88372-110">สตริง</span><span class="sxs-lookup"><span data-stu-id="88372-110">String</span></span>    |
  | <span data-ttu-id="88372-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="88372-111">LeaveType</span></span>     | <span data-ttu-id="88372-112">สตริง</span><span class="sxs-lookup"><span data-stu-id="88372-112">String</span></span>    |
  | <span data-ttu-id="88372-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="88372-113">LeaveDate</span></span>     | <span data-ttu-id="88372-114">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="88372-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="88372-115">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="88372-115">Properties</span></span>

  | <span data-ttu-id="88372-116">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="88372-116">Property Name</span></span>     | <span data-ttu-id="88372-117">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="88372-117">Data Type</span></span> | <span data-ttu-id="88372-118">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="88372-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="88372-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="88372-119">dataAreaId</span></span>        | <span data-ttu-id="88372-120">สตริง</span><span class="sxs-lookup"><span data-stu-id="88372-120">String</span></span>    | <span data-ttu-id="88372-121">X</span><span class="sxs-lookup"><span data-stu-id="88372-121">X</span></span>        |
  | <span data-ttu-id="88372-122">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="88372-122">RequestId</span></span>         | <span data-ttu-id="88372-123">สตริง</span><span class="sxs-lookup"><span data-stu-id="88372-123">String</span></span>    | <span data-ttu-id="88372-124">X</span><span class="sxs-lookup"><span data-stu-id="88372-124">X</span></span>        |
  | <span data-ttu-id="88372-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="88372-125">LeaveType</span></span>         | <span data-ttu-id="88372-126">สตริง</span><span class="sxs-lookup"><span data-stu-id="88372-126">String</span></span>    | <span data-ttu-id="88372-127">X</span><span class="sxs-lookup"><span data-stu-id="88372-127">X</span></span>        |
  | <span data-ttu-id="88372-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="88372-128">LeaveDate</span></span>         | <span data-ttu-id="88372-129">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="88372-129">Date</span></span>      | <span data-ttu-id="88372-130">X</span><span class="sxs-lookup"><span data-stu-id="88372-130">X</span></span>        |
  | <span data-ttu-id="88372-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="88372-131">ReasonCodeId</span></span>      | <span data-ttu-id="88372-132">สตริง</span><span class="sxs-lookup"><span data-stu-id="88372-132">String</span></span>    |          |
  | <span data-ttu-id="88372-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="88372-133">PersonnelNumber</span></span>   | <span data-ttu-id="88372-134">สตริง</span><span class="sxs-lookup"><span data-stu-id="88372-134">String</span></span>    | <span data-ttu-id="88372-135">X</span><span class="sxs-lookup"><span data-stu-id="88372-135">X</span></span>        |
  | <span data-ttu-id="88372-136">วันที่คำขอ</span><span class="sxs-lookup"><span data-stu-id="88372-136">RequestDate</span></span>       | <span data-ttu-id="88372-137">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="88372-137">Date</span></span>      | <span data-ttu-id="88372-138">X</span><span class="sxs-lookup"><span data-stu-id="88372-138">X</span></span>        |
  | <span data-ttu-id="88372-139">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="88372-139">Comment</span></span>           | <span data-ttu-id="88372-140">สตริง</span><span class="sxs-lookup"><span data-stu-id="88372-140">String</span></span>    |          |
  | <span data-ttu-id="88372-141">สถานะ</span><span class="sxs-lookup"><span data-stu-id="88372-141">Status</span></span>            | <span data-ttu-id="88372-142">Enum</span><span class="sxs-lookup"><span data-stu-id="88372-142">Enum</span></span>      | <span data-ttu-id="88372-143">X</span><span class="sxs-lookup"><span data-stu-id="88372-143">X</span></span>        |
  | <span data-ttu-id="88372-144">จำนวน</span><span class="sxs-lookup"><span data-stu-id="88372-144">Amount</span></span>            | <span data-ttu-id="88372-145">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="88372-145">Real</span></span>      |          |
  | <span data-ttu-id="88372-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="88372-146">HalfDayDefinition</span></span> | <span data-ttu-id="88372-147">Enum</span><span class="sxs-lookup"><span data-stu-id="88372-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="88372-148">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88372-148">Actions</span></span>

 | <span data-ttu-id="88372-149">ชื่อการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="88372-149">Action Name</span></span>                               | <span data-ttu-id="88372-150">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="88372-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="88372-151">ส่ง</span><span class="sxs-lookup"><span data-stu-id="88372-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="88372-152">ส่งคำขอที่จะประมวลผลโดยลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="88372-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="88372-153">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="88372-153">See also</span></span>

- [<span data-ttu-id="88372-154">ส่งคำขอลางานไปที่ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="88372-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="88372-155">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="88372-155">Authentication</span></span>](hr-developer-api-authentication.md)