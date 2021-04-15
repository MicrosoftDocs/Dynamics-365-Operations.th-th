---
title: ภาพรวมการลางานและการขาดงาน
description: ใน Dynamics 365 Human Resources พื้นที่ทำงานการลางานและการขาดงานจะแสดงกรอบงานที่มีความยืดหยุ่นสำหรับการสร้างแผนการลางานใหม่ นอกจากนี้ ยังมีลำดับงานสำหรับการจัดการคำขอและหน้าระบบบริการตนเองที่ใช้งานง่ายสำหรับพนักงานเพื่อส่งคำขอลาหยุด
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 827d0325fc9a97cf2b143e1c2705232dfd8a7ab2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794672"
---
# <a name="leave-and-absence-overview"></a><span data-ttu-id="93621-104">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="93621-104">Leave and absence overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="93621-105">Dynamics 365 Human Resources ช่วยให้คุณสามารถทำให้ผลประโยชน์การลางานที่ดีแก่ผู้ปฏิบัติงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="93621-105">Dynamics 365 Human Resources helps you provide great leave benefits to your workers.</span></span> <span data-ttu-id="93621-106">พื้นที่ทำงาน **การลางานและการขาดงาน** จะแสดงกรอบงานที่มีความยืดหยุ่นสำหรับการสร้างแผนการลางานใหม่</span><span class="sxs-lookup"><span data-stu-id="93621-106">The **Leave and absence** workspace provides a flexible framework for creating new leave plans.</span></span> <span data-ttu-id="93621-107">นอกจากนี้ ยังมีลำดับงานสำหรับการจัดการคำขอและหน้าระบบบริการตนเองที่ใช้งานง่ายสำหรับพนักงานเพื่อส่งคำขอลาหยุด</span><span class="sxs-lookup"><span data-stu-id="93621-107">It also provides workflows for managing requests and an intuitive self service page for employees to request time off.</span></span> <span data-ttu-id="93621-108">การวิเคราะห์จะช่วยองค์กรของคุณวัดและตรวจสอบยอดดุลและการใช้งานสำหรับแผนการลางานของคุณ</span><span class="sxs-lookup"><span data-stu-id="93621-108">Analytics help your organization measure and monitor leave balances and usage for your leave plans.</span></span>

## <a name="set-up-leave-and-absence"></a><span data-ttu-id="93621-109">ตั้งค่าการลางานและขาดงาน</span><span class="sxs-lookup"><span data-stu-id="93621-109">Set up Leave and absence</span></span>

<span data-ttu-id="93621-110">ก่อนที่จะสร้างแผนการลางานสำหรับพนักงานของคุณ คุณต้องทำขั้นตอนการตั้งค่าสองสามข้อดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="93621-110">Before creating leave plans for your employees, you need to do a few setup steps:</span></span>

- [<span data-ttu-id="93621-111">ตั้งค่าคอนฟิกพารามิเตอร์การลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="93621-111">Configure leave and absence parameters</span></span>](hr-leave-and-absence-parameters.md)
- [<span data-ttu-id="93621-112">สร้างปฏิทินเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="93621-112">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="93621-113">สร้างลำดับงานการร้องขอลางาน</span><span class="sxs-lookup"><span data-stu-id="93621-113">Create a leave request workflow</span></span>](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a><span data-ttu-id="93621-114">สร้างและจัดการแผนการลา</span><span class="sxs-lookup"><span data-stu-id="93621-114">Create and manage leave plans</span></span>

<span data-ttu-id="93621-115">ก่อนที่จะสร้างแผนการลางานสำหรับผู้ปฏิบัติงานของคุณ คุณต้องสร้างชนิดของการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="93621-115">Before creating leave plans for your workers, you need to create leave and absence types.</span></span> <span data-ttu-id="93621-116">หลังจากที่คุณสร้างแผนการลางานแล้ว คุณก็สามารถลงทะเบียนผู้ปฏิบัติงานเข้าในแผนได้</span><span class="sxs-lookup"><span data-stu-id="93621-116">After you create a leave plan, you can then enroll workers into the plan.</span></span> <span data-ttu-id="93621-117">นอกจากนี้คุณยังสามารถดำเนินการกระบวนการค้างจ่าย สร้างข้อความแจ้งเตือน และดูการวิเคราะห์สำหรับแผนของคุณได้</span><span class="sxs-lookup"><span data-stu-id="93621-117">You can also run the accrue process, create alerts, and view analytics for your plans.</span></span>

- [<span data-ttu-id="93621-118">ตั้งค่าคอนฟิกชนิดการลางานและการหยุดงาน</span><span class="sxs-lookup"><span data-stu-id="93621-118">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
- [<span data-ttu-id="93621-119">การสร้างแผนการลางานและขาดงาน</span><span class="sxs-lookup"><span data-stu-id="93621-119">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="93621-120">กำหนดผู้ปฏิบัติงานให้กับแผนการลางาน</span><span class="sxs-lookup"><span data-stu-id="93621-120">Assign workers to a leave plan</span></span>](hr-leave-and-absence-enroll.md)
- [<span data-ttu-id="93621-121">การรับรู้แผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="93621-121">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)
- [<span data-ttu-id="93621-122">ดูการวิเคราะห์สำหรับการลางานและขาดงาน</span><span class="sxs-lookup"><span data-stu-id="93621-122">View analytics for leave and absence</span></span>](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a><span data-ttu-id="93621-123">ร้องขอการปิดและจัดการคำขอ</span><span class="sxs-lookup"><span data-stu-id="93621-123">Request time off and manage requests</span></span>

<span data-ttu-id="93621-124">พนักงานของคุณสามารถส่งคำขอปิดเวลาได้ และคุณสามารถจัดการกับพนักงาน ในพื้นที่การทำงาน **การบริการตัวเองของพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="93621-124">Your employees can submit time off requests, and you can manage them, in the **Employee self service** workspace.</span></span>

<span data-ttu-id="93621-125">[ส่งคำขอลาหยุด](hr-employee-self-service-request-time-off.md)
[จัดการคำขอการลางานและการขาดงาน](hr-employee-self-service-manage-requests.md)</span><span class="sxs-lookup"><span data-stu-id="93621-125">[Request time off](hr-employee-self-service-request-time-off.md)
[Manage leave and absence requests](hr-employee-self-service-manage-requests.md)</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]