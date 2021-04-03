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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465521"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="b43fc-103">ภาพรวมของ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="b43fc-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b43fc-104">เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม</span><span class="sxs-lookup"><span data-stu-id="b43fc-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="b43fc-105">คีย์</span><span class="sxs-lookup"><span data-stu-id="b43fc-105">Key</span></span>

  | <span data-ttu-id="b43fc-106">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="b43fc-106">Property Name</span></span> | <span data-ttu-id="b43fc-107">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b43fc-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="b43fc-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="b43fc-108">dataAreaId</span></span>    | <span data-ttu-id="b43fc-109">สตริง</span><span class="sxs-lookup"><span data-stu-id="b43fc-109">String</span></span>    |
  | <span data-ttu-id="b43fc-110">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="b43fc-110">RequestId</span></span>     | <span data-ttu-id="b43fc-111">สตริง</span><span class="sxs-lookup"><span data-stu-id="b43fc-111">String</span></span>    |
  | <span data-ttu-id="b43fc-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="b43fc-112">LeaveType</span></span>     | <span data-ttu-id="b43fc-113">สตริง</span><span class="sxs-lookup"><span data-stu-id="b43fc-113">String</span></span>    |
  | <span data-ttu-id="b43fc-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="b43fc-114">LeaveDate</span></span>     | <span data-ttu-id="b43fc-115">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="b43fc-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="b43fc-116">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="b43fc-116">Properties</span></span>

  | <span data-ttu-id="b43fc-117">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="b43fc-117">Property Name</span></span>     | <span data-ttu-id="b43fc-118">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b43fc-118">Data Type</span></span> | <span data-ttu-id="b43fc-119">ต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="b43fc-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="b43fc-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="b43fc-120">dataAreaId</span></span>        | <span data-ttu-id="b43fc-121">สตริง</span><span class="sxs-lookup"><span data-stu-id="b43fc-121">String</span></span>    | <span data-ttu-id="b43fc-122">X</span><span class="sxs-lookup"><span data-stu-id="b43fc-122">X</span></span>        |
  | <span data-ttu-id="b43fc-123">รหัสคำขอ</span><span class="sxs-lookup"><span data-stu-id="b43fc-123">RequestId</span></span>         | <span data-ttu-id="b43fc-124">สตริง</span><span class="sxs-lookup"><span data-stu-id="b43fc-124">String</span></span>    | <span data-ttu-id="b43fc-125">X</span><span class="sxs-lookup"><span data-stu-id="b43fc-125">X</span></span>        |
  | <span data-ttu-id="b43fc-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="b43fc-126">LeaveType</span></span>         | <span data-ttu-id="b43fc-127">สตริง</span><span class="sxs-lookup"><span data-stu-id="b43fc-127">String</span></span>    | <span data-ttu-id="b43fc-128">X</span><span class="sxs-lookup"><span data-stu-id="b43fc-128">X</span></span>        |
  | <span data-ttu-id="b43fc-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="b43fc-129">LeaveDate</span></span>         | <span data-ttu-id="b43fc-130">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="b43fc-130">Date</span></span>      | <span data-ttu-id="b43fc-131">X</span><span class="sxs-lookup"><span data-stu-id="b43fc-131">X</span></span>        |
  | <span data-ttu-id="b43fc-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="b43fc-132">ReasonCodeId</span></span>      | <span data-ttu-id="b43fc-133">สตริง</span><span class="sxs-lookup"><span data-stu-id="b43fc-133">String</span></span>    |          |
  | <span data-ttu-id="b43fc-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="b43fc-134">PersonnelNumber</span></span>   | <span data-ttu-id="b43fc-135">สตริง</span><span class="sxs-lookup"><span data-stu-id="b43fc-135">String</span></span>    | <span data-ttu-id="b43fc-136">X</span><span class="sxs-lookup"><span data-stu-id="b43fc-136">X</span></span>        |
  | <span data-ttu-id="b43fc-137">วันที่คำขอ</span><span class="sxs-lookup"><span data-stu-id="b43fc-137">RequestDate</span></span>       | <span data-ttu-id="b43fc-138">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="b43fc-138">Date</span></span>      | <span data-ttu-id="b43fc-139">X</span><span class="sxs-lookup"><span data-stu-id="b43fc-139">X</span></span>        |
  | <span data-ttu-id="b43fc-140">ข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="b43fc-140">Comment</span></span>           | <span data-ttu-id="b43fc-141">สตริง</span><span class="sxs-lookup"><span data-stu-id="b43fc-141">String</span></span>    |          |
  | <span data-ttu-id="b43fc-142">สถานะ</span><span class="sxs-lookup"><span data-stu-id="b43fc-142">Status</span></span>            | <span data-ttu-id="b43fc-143">Enum</span><span class="sxs-lookup"><span data-stu-id="b43fc-143">Enum</span></span>      | <span data-ttu-id="b43fc-144">X</span><span class="sxs-lookup"><span data-stu-id="b43fc-144">X</span></span>        |
  | <span data-ttu-id="b43fc-145">จำนวน</span><span class="sxs-lookup"><span data-stu-id="b43fc-145">Amount</span></span>            | <span data-ttu-id="b43fc-146">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="b43fc-146">Real</span></span>      |          |
  | <span data-ttu-id="b43fc-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="b43fc-147">HalfDayDefinition</span></span> | <span data-ttu-id="b43fc-148">Enum</span><span class="sxs-lookup"><span data-stu-id="b43fc-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="b43fc-149">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b43fc-149">Actions</span></span>

 | <span data-ttu-id="b43fc-150">ชื่อการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b43fc-150">Action Name</span></span>                               | <span data-ttu-id="b43fc-151">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b43fc-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="b43fc-152">ส่ง</span><span class="sxs-lookup"><span data-stu-id="b43fc-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="b43fc-153">ส่งคำขอที่จะประมวลผลโดยลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="b43fc-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b43fc-154">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="b43fc-154">See also</span></span>

- [<span data-ttu-id="b43fc-155">ส่งคำขอลางานไปที่ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="b43fc-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="b43fc-156">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b43fc-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]