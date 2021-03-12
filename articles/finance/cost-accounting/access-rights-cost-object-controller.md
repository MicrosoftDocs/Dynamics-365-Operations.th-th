---
title: สิทธิ์การเข้าถึงสำหรับตัวควบคุมออบเจ็กต์ต้นทุน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับสิทธิ์การเข้าถึงสำหรับตัวควบคุมออบเจ็กต์ต้นทุน
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 68fc97ed27460ac0a2bee9c10cb9bda67d506e78
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978900"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="9cb68-103">สิทธิ์การเข้าถึงสำหรับตัวควบคุมออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cb68-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cb68-104">พื้นที่ทำงาน **การควบคุมต้นทุน** เป็นจุดศูนย์กลางที่ผู้จัดการสามารถดูประสิทธิภาพของออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cb68-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="9cb68-105">พื้นที่ทำงานนี้ช่วยให้ผู้จัดการใช้ข้อมูลการบัญชีต้นทุน แม้ว่าจะไม่ได้เป็นผู้จัดการบัญชีต้นทุนก็ตาม</span><span class="sxs-lookup"><span data-stu-id="9cb68-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="9cb68-106">สำหรับเหตุผลด้านความปลอดภัย ผู้จัดการควรได้รับอนุญาตให้ดูเฉพาะข้อมูลบัญชีต้นทุนที่เกี่ยวข้องกับออบเจ็กต์เฉพาะต้นทุนที่จะรับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="9cb68-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="9cb68-107">บทบาทเฉพาะในการบัญชีต้นทุนมีอยู่สี่บทบาท</span><span class="sxs-lookup"><span data-stu-id="9cb68-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="9cb68-108">ชื่อบทบาท</span><span class="sxs-lookup"><span data-stu-id="9cb68-108">Role name</span></span>               | <span data-ttu-id="9cb68-109">ใบอนุญาต</span><span class="sxs-lookup"><span data-stu-id="9cb68-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="9cb68-110">ผู้จัดการการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cb68-110">Cost accounting manager</span></span> | <span data-ttu-id="9cb68-111">กิจกรรม</span><span class="sxs-lookup"><span data-stu-id="9cb68-111">Activity</span></span>     |
| <span data-ttu-id="9cb68-112">นักบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cb68-112">Cost accountant</span></span>         | <span data-ttu-id="9cb68-113">Operations</span><span class="sxs-lookup"><span data-stu-id="9cb68-113">Operations</span></span>   |
| <span data-ttu-id="9cb68-114">เสมียนบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cb68-114">Cost accountant clerk</span></span>   | <span data-ttu-id="9cb68-115">Operations</span><span class="sxs-lookup"><span data-stu-id="9cb68-115">Operations</span></span>   |
| <span data-ttu-id="9cb68-116">ตัวควบคุมออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cb68-116">Cost object controller</span></span>  | <span data-ttu-id="9cb68-117">สมาชิกทีมงาน</span><span class="sxs-lookup"><span data-stu-id="9cb68-117">Team members</span></span> |

<span data-ttu-id="9cb68-118">หัวข้อนี้อธิบายวิธีการกำหนดบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** ให้กับผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="9cb68-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="9cb68-119">เมื่อบทบาทของ **ตัวควบคุมออบเจ็กต์ต้นทุน** กำหนดบทบาทให้กับผู้จัดการ ผู้จัดการสามารถดำเนินงานดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cb68-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="9cb68-120">การเข้าถึงพื้นที่ทำงาน **การควบคุมต้นทุน** (ในไคลเอนต์)</span><span class="sxs-lookup"><span data-stu-id="9cb68-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="9cb68-121">เจาะลึกและมีสิทธิ์เข้าดูหน้าที่สนับสนุนประสบการณ์แบบลงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="9cb68-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="9cb68-122">เข้าถึงพื้นที่ทำงาน **การควบคุมต้นทุน** (ในอุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="9cb68-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="9cb68-123">บทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** ไม่ควบคุมออบเจ็กต์ต้นทุนที่ผู้ใช้สามารถเข้าถึงและดูข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="9cb68-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="9cb68-124">มีการจัดให้มีความปลอดภัยระดับแถวผ่านลำดับชั้นของมิติและลำดับชั้นรายการการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="9cb68-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="9cb68-125">การให้สิทธิการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="9cb68-125">Grant access rights</span></span>
<span data-ttu-id="9cb68-126">ตัวอย่างต่อไปนี้แสดงว่าลำดับชั้นมิติมีลักษณะอย่างไร</span><span class="sxs-lookup"><span data-stu-id="9cb68-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="9cb68-127">**รายละเอียดลำดับชั้นมิติ**</span><span class="sxs-lookup"><span data-stu-id="9cb68-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="9cb68-128">ชื่อลำดับชั้นมิติ</span><span class="sxs-lookup"><span data-stu-id="9cb68-128">Dimension hierarchy name</span></span> | <span data-ttu-id="9cb68-129">มิติ</span><span class="sxs-lookup"><span data-stu-id="9cb68-129">Dimension</span></span>    | <span data-ttu-id="9cb68-130">ชื่อชนิดลำดับชั้นมิติ</span><span class="sxs-lookup"><span data-stu-id="9cb68-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="9cb68-131">ลำดับชั้นรายการการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="9cb68-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="9cb68-132">องค์กร</span><span class="sxs-lookup"><span data-stu-id="9cb68-132">Organization</span></span>             | <span data-ttu-id="9cb68-133">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cb68-133">Cost centers</span></span> | <span data-ttu-id="9cb68-134">ลำดับชั้นการจัดประเภทมิติ</span><span class="sxs-lookup"><span data-stu-id="9cb68-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="9cb68-135">**ใช่**</span><span class="sxs-lookup"><span data-stu-id="9cb68-135">**Yes**</span></span>               |

<span data-ttu-id="9cb68-136">คุณสามารถใช้แท็บด่วน **ผู้ใช้** ในโปรแกรมออกแบบลำดับชั้นเพื่อแทรกรหัสผู้ใช้หนึ่งรหัสหรือมากกว่าในแต่ละโหนด</span><span class="sxs-lookup"><span data-stu-id="9cb68-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="9cb68-137">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9cb68-137">Users</span></span>            | <span data-ttu-id="9cb68-138">ช่วงสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="9cb68-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="9cb68-139">**โหนด**</span><span class="sxs-lookup"><span data-stu-id="9cb68-139">**Nodes**</span></span>                         | <span data-ttu-id="9cb68-140">**รหัสผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="9cb68-140">**User ID**</span></span>      | <span data-ttu-id="9cb68-141">**สมาชิกมิติเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="9cb68-141">**From dimension member**</span></span> | <span data-ttu-id="9cb68-142">**สมาชิกมิติสิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="9cb68-142">**To dimension member**</span></span> |
| <span data-ttu-id="9cb68-143">องค์กร</span><span class="sxs-lookup"><span data-stu-id="9cb68-143">Organization</span></span>                      | <span data-ttu-id="9cb68-144">เบนจามิน แคลร์</span><span class="sxs-lookup"><span data-stu-id="9cb68-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="9cb68-145">&nbsp;&nbsp;ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="9cb68-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="9cb68-146">เมษายน</span><span class="sxs-lookup"><span data-stu-id="9cb68-146">April</span></span>            |                           |                         |
| <span data-ttu-id="9cb68-147">&nbsp;&nbsp;&nbsp;&nbsp;การเงิน</span><span class="sxs-lookup"><span data-stu-id="9cb68-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="9cb68-148">อลิเซีย</span><span class="sxs-lookup"><span data-stu-id="9cb68-148">Alicia</span></span>           | <span data-ttu-id="9cb68-149">CC002</span><span class="sxs-lookup"><span data-stu-id="9cb68-149">CC002</span></span>                     | <span data-ttu-id="9cb68-150">CC003</span><span class="sxs-lookup"><span data-stu-id="9cb68-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="9cb68-151">CC007</span><span class="sxs-lookup"><span data-stu-id="9cb68-151">CC007</span></span>                     | <span data-ttu-id="9cb68-152">CC007</span><span class="sxs-lookup"><span data-stu-id="9cb68-152">CC007</span></span>                   |
| <span data-ttu-id="9cb68-153">&nbsp;&nbsp;&nbsp;&nbsp;ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="9cb68-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="9cb68-154">อาร์นี</span><span class="sxs-lookup"><span data-stu-id="9cb68-154">Arnie</span></span>            | <span data-ttu-id="9cb68-155">CC001</span><span class="sxs-lookup"><span data-stu-id="9cb68-155">CC001</span></span>                     | <span data-ttu-id="9cb68-156">CC001</span><span class="sxs-lookup"><span data-stu-id="9cb68-156">CC001</span></span>                   |
| <span data-ttu-id="9cb68-157">&nbsp;&nbsp;การผลิต</span><span class="sxs-lookup"><span data-stu-id="9cb68-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="9cb68-158">เดวิด</span><span class="sxs-lookup"><span data-stu-id="9cb68-158">David</span></span>            |                           |                         |
| <span data-ttu-id="9cb68-159">&nbsp;&nbsp;&nbsp;&nbsp;บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9cb68-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="9cb68-160">เอลเลน</span><span class="sxs-lookup"><span data-stu-id="9cb68-160">Ellen</span></span>            | <span data-ttu-id="9cb68-161">CC005</span><span class="sxs-lookup"><span data-stu-id="9cb68-161">CC005</span></span>                     | <span data-ttu-id="9cb68-162">CC005</span><span class="sxs-lookup"><span data-stu-id="9cb68-162">CC005</span></span>                   |
| <span data-ttu-id="9cb68-163">&nbsp;&nbsp;&nbsp;&nbsp;ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="9cb68-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="9cb68-164">คริส</span><span class="sxs-lookup"><span data-stu-id="9cb68-164">Chris</span></span>            | <span data-ttu-id="9cb68-165">CC006</span><span class="sxs-lookup"><span data-stu-id="9cb68-165">CC006</span></span>                     | <span data-ttu-id="9cb68-166">CC006</span><span class="sxs-lookup"><span data-stu-id="9cb68-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="9cb68-167">ควรกำหนดให้ผู้จัดทำบัญชีต้นทุนอยู่ระดับบนสุดของลำดับชั้น เพื่อให้สามารถดูรายการทั้งหมดในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cb68-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="9cb68-168">ก่อนที่จะใช้ลำดับชั้นรายการเข้าถึงและการตั้งค่าความปลอดภัย ตัวเลือก **เปิดใช้งานการเข้าถึงเพื่อดูสำหรับสมาชิกมิติออบเจ็กต์ต้นทุน** ต้องตั้งค่าตัวเลือกเป็น **ใช่** บนแท็บ **ทั่วไป** ของหน้า **พารามิเตอร์การบัญชีต้นทุน** (**การบัญชีต้นทุน** > **ตั้งค่า** > **พารามิเตอร์**)</span><span class="sxs-lookup"><span data-stu-id="9cb68-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="9cb68-169">การตั้งค่าสำหรับลำดับชั้นรายการการเข้าถึงใช้เพื่อควบคุมข้อมูลที่แสดงในพื้นที่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cb68-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="9cb68-170">พื้นที่ทำงาน **การควบคุมต้นทุน** (ในไคลเอนต์):</span><span class="sxs-lookup"><span data-stu-id="9cb68-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="9cb68-171">ข้อมูลบนเพจที่ใช้สำหรับการเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="9cb68-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="9cb68-172">พื้นที่ทำงาน **การควบคุมต้นทุน** (ในอุปกรณ์เคลื่อนที่):</span><span class="sxs-lookup"><span data-stu-id="9cb68-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="9cb68-173">ยอดดุลในบัตร</span><span class="sxs-lookup"><span data-stu-id="9cb68-173">Balances in cards</span></span>

- <span data-ttu-id="9cb68-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="9cb68-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="9cb68-175">ข้อมูลที่แสดงในการจัดรูปแบบการแสดง Power BI</span><span class="sxs-lookup"><span data-stu-id="9cb68-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="9cb68-176">การจัดรูปแบบการแสดง Power BI ของข้อมูลที่ถูกฝังในไคลเอ็นต์ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9cb68-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="9cb68-177">ก่อนที่ลำดับชั้นของรายการการเข้าถึงสามารถส่งผลต่อข้อมูลใน Power BI ลำดับชั้นของรายการการเข้าถึงและความปลอดภัยระดับแถวใน Power BI ต้องถูกจับคู่</span><span class="sxs-lookup"><span data-stu-id="9cb68-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="9cb68-178">สำหรับข้อมูลเพิ่มเติมดูที่ [การตั้งค่าความปลอดภัยสำหรับชุดเนื้อหาการบัญชีต้นทุน](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)</span><span class="sxs-lookup"><span data-stu-id="9cb68-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="9cb68-179">หัวข้อนี้แสดงข้อกำหนดเบื้องต้นที่ต้องมีอยู่ในตำแหน่งก่อนที่คุณสามารถใช้การพื้นที่ทำงาน **ควบคุมต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="9cb68-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="9cb68-180">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9cb68-180">Additional resources</span></span>

- [<span data-ttu-id="9cb68-181">พื้นที่ทำงานการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cb68-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="9cb68-182">ลำดับชั้นของมิติ</span><span class="sxs-lookup"><span data-stu-id="9cb68-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="9cb68-183">การตั้งค่าความปลอดภัยสำหรับชุดเนื้อหาการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9cb68-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
