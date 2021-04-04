---
title: จัดการการลางานของพนักงาน
description: จัดการการลางานของพนักงานใน Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42d51ffe14442e076bafc99035dbd68a555e5b92
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468070"
---
# <a name="manage-employee-leave"></a><span data-ttu-id="dd011-103">จัดการการลางานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="dd011-103">Manage employee leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dd011-104">คุณสามารถจัดการการลางานของพนักงานตามชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="dd011-104">You can manage an employee's leave by leave type.</span></span> <span data-ttu-id="dd011-105">การทำเช่นนี้รวมถึงการลงทะเบียนการลาที่หมดอายุ และการปรับปรุงยอดดุลชนิดของการลางาน</span><span class="sxs-lookup"><span data-stu-id="dd011-105">This includes expiring leave enrollment and adjusting leave type balances.</span></span> 

## <a name="adjust-leave-balances"></a><span data-ttu-id="dd011-106">การปรับปรุงยอดดุลการลางาน</span><span class="sxs-lookup"><span data-stu-id="dd011-106">Adjust leave balances</span></span>

1. <span data-ttu-id="dd011-107">บนเรกคอร์ดของพนักงาน ให้เลือก **ลา**</span><span class="sxs-lookup"><span data-stu-id="dd011-107">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="dd011-108">ให้เลือก **ตั้งค่าการลางานและขาดงาน**</span><span class="sxs-lookup"><span data-stu-id="dd011-108">Select **Leave and absence setup**.</span></span>

3. <span data-ttu-id="dd011-109">เลือก **ปรับปรุงยอดดุล**</span><span class="sxs-lookup"><span data-stu-id="dd011-109">Select **Adjust balance**.</span></span>

4. <span data-ttu-id="dd011-110">เลือก **ชนิดการลางาน**</span><span class="sxs-lookup"><span data-stu-id="dd011-110">Select the **Leave type**.</span></span>

5. <span data-ttu-id="dd011-111">ป้อน **จำนวนการปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="dd011-111">Enter an **Adjustment amount**.</span></span> 

6. <span data-ttu-id="dd011-112">หรือคุณสามารถเลือก **วันที่** ได้</span><span class="sxs-lookup"><span data-stu-id="dd011-112">Optionally, you can select a **Date**.</span></span> 

<span data-ttu-id="dd011-113">คุณสามารถรวมรหัสเหตุผลและข้อคิดเห็นเมื่อทำการปรับปรุงยอดดุลการลางานของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="dd011-113">You can include a reason code and comment when adjusting an employee's leave balance.</span></span> 

>[!IMPORTANT]
><span data-ttu-id="dd011-114">การดูข้อมูลเพิ่มเติมเกี่ยวกับยอดดุลการลางานอยู่ในพรีวิว</span><span class="sxs-lookup"><span data-stu-id="dd011-114">Viewing additional information about leave balances is in preview.</span></span> <span data-ttu-id="dd011-115">คุณจำเป็นต้องเปิดใช้งานในสภาพแวดล้อม **Sandbox** ของคุณ</span><span class="sxs-lookup"><span data-stu-id="dd011-115">You'll need to enable it in your **Sandbox** environment.</span></span> <span data-ttu-id="dd011-116">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปิดใช้งานคุณลักษณะรุ่นพรีวิว ดูที่ [จัดการคุณลักษณะ](hr-admin-manage-features.md)</span><span class="sxs-lookup"><span data-stu-id="dd011-116">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br>
><span data-ttu-id="dd011-117">เมื่อวางเมาส์เหนือยอดดุลการลางานใดๆ ตอนนี้คุณจะเห็น:</span><span class="sxs-lookup"><span data-stu-id="dd011-117">When hovering over any leave balance, you will now see:</span></span><br>
>- <span data-ttu-id="dd011-118">**พร้อมใช้งาน**: ยอดรวมปีนี้ - ใช้ในปีนี้</span><span class="sxs-lookup"><span data-stu-id="dd011-118">**Available**: Total this year - Take this year</span></span>
>- <span data-ttu-id="dd011-119">**ยอดรวมของปีนี้**: การรับรู้ การปรับปรุง และการยกยอดไปสำหรับปีทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="dd011-119">**Total this year**: All accruals, adjustments, and carry forward for the year</span></span>
>- <span data-ttu-id="dd011-120">**ดำเนินการในปีนี้**: การหยุดพักที่อนุมัติทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="dd011-120">**Taken this year**: All approved time off</span></span>

## <a name="see-also"></a><span data-ttu-id="dd011-121">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="dd011-121">See also</span></span>

- [<span data-ttu-id="dd011-122">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="dd011-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="dd011-123">จัดการกับคำขอการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="dd011-123">Manage leave and absence requests</span></span>](hr-employee-self-service-manage-requests.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]