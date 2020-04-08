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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af6ddc86bb6313387aa9c6ccc347d2a1c5fac50a
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154493"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="9ffac-103">สิทธิ์การเข้าถึงสำหรับตัวควบคุมออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9ffac-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ffac-104">พื้นที่ทำงาน **การควบคุมต้นทุน** เป็นจุดศูนย์กลางที่ผู้จัดการสามารถดูประสิทธิภาพของออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9ffac-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="9ffac-105">พื้นที่ทำงานนี้ช่วยให้ผู้จัดการใช้ข้อมูลการบัญชีต้นทุน แม้ว่าจะไม่ได้เป็นผู้จัดการบัญชีต้นทุนก็ตาม</span><span class="sxs-lookup"><span data-stu-id="9ffac-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="9ffac-106">สำหรับเหตุผลด้านความปลอดภัย ผู้จัดการควรได้รับอนุญาตให้ดูเฉพาะข้อมูลบัญชีต้นทุนที่เกี่ยวข้องกับออบเจ็กต์เฉพาะต้นทุนที่จะรับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="9ffac-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="9ffac-107">บทบาทเฉพาะในการบัญชีต้นทุนมีอยู่สี่บทบาท</span><span class="sxs-lookup"><span data-stu-id="9ffac-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="9ffac-108">ชื่อบทบาท</span><span class="sxs-lookup"><span data-stu-id="9ffac-108">Role name</span></span>               | <span data-ttu-id="9ffac-109">ใบอนุญาต</span><span class="sxs-lookup"><span data-stu-id="9ffac-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="9ffac-110">ผู้จัดการการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9ffac-110">Cost accounting manager</span></span> | <span data-ttu-id="9ffac-111">กิจกรรม</span><span class="sxs-lookup"><span data-stu-id="9ffac-111">Activity</span></span>     |
| <span data-ttu-id="9ffac-112">นักบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9ffac-112">Cost accountant</span></span>         | <span data-ttu-id="9ffac-113">Operations</span><span class="sxs-lookup"><span data-stu-id="9ffac-113">Operations</span></span>   |
| <span data-ttu-id="9ffac-114">เสมียนบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9ffac-114">Cost accountant clerk</span></span>   | <span data-ttu-id="9ffac-115">Operations</span><span class="sxs-lookup"><span data-stu-id="9ffac-115">Operations</span></span>   |
| <span data-ttu-id="9ffac-116">ตัวควบคุมออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9ffac-116">Cost object controller</span></span>  | <span data-ttu-id="9ffac-117">สมาชิกทีมงาน</span><span class="sxs-lookup"><span data-stu-id="9ffac-117">Team members</span></span> |

<span data-ttu-id="9ffac-118">หัวข้อนี้อธิบายวิธีการกำหนดบทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** ให้กับผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="9ffac-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="9ffac-119">เมื่อบทบาทของ **ตัวควบคุมออบเจ็กต์ต้นทุน** กำหนดบทบาทให้กับผู้จัดการ ผู้จัดการสามารถดำเนินงานดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9ffac-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="9ffac-120">การเข้าถึงพื้นที่ทำงาน **การควบคุมต้นทุน** (ในไคลเอนต์)</span><span class="sxs-lookup"><span data-stu-id="9ffac-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="9ffac-121">เจาะลึกและมีสิทธิ์เข้าดูหน้าที่สนับสนุนประสบการณ์แบบลงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="9ffac-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="9ffac-122">เข้าถึงพื้นที่ทำงาน **การควบคุมต้นทุน** (ในอุปกรณ์เคลื่อนที่)</span><span class="sxs-lookup"><span data-stu-id="9ffac-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="9ffac-123">บทบาท **ตัวควบคุมออบเจ็กต์ต้นทุน** ไม่ควบคุมออบเจ็กต์ต้นทุนที่ผู้ใช้สามารถเข้าถึงและดูข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="9ffac-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="9ffac-124">มีการจัดให้มีความปลอดภัยระดับแถวผ่านลำดับชั้นของมิติและลำดับชั้นรายการการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="9ffac-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="9ffac-125">การให้สิทธิการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="9ffac-125">Grant access rights</span></span>
<span data-ttu-id="9ffac-126">ตัวอย่างต่อไปนี้แสดงว่าลำดับชั้นมิติมีลักษณะอย่างไร</span><span class="sxs-lookup"><span data-stu-id="9ffac-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="9ffac-127">**รายละเอียดลำดับชั้นมิติ**</span><span class="sxs-lookup"><span data-stu-id="9ffac-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="9ffac-128">ชื่อลำดับชั้นมิติ</span><span class="sxs-lookup"><span data-stu-id="9ffac-128">Dimension hierarchy name</span></span> | <span data-ttu-id="9ffac-129">มิติ</span><span class="sxs-lookup"><span data-stu-id="9ffac-129">Dimension</span></span>    | <span data-ttu-id="9ffac-130">ชื่อชนิดลำดับชั้นมิติ</span><span class="sxs-lookup"><span data-stu-id="9ffac-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="9ffac-131">ลำดับชั้นรายการการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="9ffac-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="9ffac-132">องค์กร</span><span class="sxs-lookup"><span data-stu-id="9ffac-132">Organization</span></span>             | <span data-ttu-id="9ffac-133">ศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9ffac-133">Cost centers</span></span> | <span data-ttu-id="9ffac-134">ลำดับชั้นการจัดประเภทมิติ</span><span class="sxs-lookup"><span data-stu-id="9ffac-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="9ffac-135">**ใช่**</span><span class="sxs-lookup"><span data-stu-id="9ffac-135">**Yes**</span></span>               |

<span data-ttu-id="9ffac-136">คุณสามารถใช้แท็บด่วน **ผู้ใช้** ในโปรแกรมออกแบบลำดับชั้นเพื่อแทรกรหัสผู้ใช้หนึ่งรหัสหรือมากกว่าในแต่ละโหนด</span><span class="sxs-lookup"><span data-stu-id="9ffac-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="9ffac-137">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9ffac-137">Users</span></span>            | <span data-ttu-id="9ffac-138">ช่วงสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="9ffac-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="9ffac-139">**โหนด**</span><span class="sxs-lookup"><span data-stu-id="9ffac-139">**Nodes**</span></span>                         | <span data-ttu-id="9ffac-140">**รหัสผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="9ffac-140">**User ID**</span></span>      | <span data-ttu-id="9ffac-141">**สมาชิกมิติเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="9ffac-141">**From dimension member**</span></span> | <span data-ttu-id="9ffac-142">**สมาชิกมิติสิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="9ffac-142">**To dimension member**</span></span> |
| <span data-ttu-id="9ffac-143">องค์กร</span><span class="sxs-lookup"><span data-stu-id="9ffac-143">Organization</span></span>                      | <span data-ttu-id="9ffac-144">เบนจามิน แคลร์</span><span class="sxs-lookup"><span data-stu-id="9ffac-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="9ffac-145">&nbsp;&nbsp;ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="9ffac-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="9ffac-146">เมษายน</span><span class="sxs-lookup"><span data-stu-id="9ffac-146">April</span></span>            |                           |                         |
| <span data-ttu-id="9ffac-147">&nbsp;&nbsp;&nbsp;&nbsp;การเงิน</span><span class="sxs-lookup"><span data-stu-id="9ffac-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="9ffac-148">อลิเซีย</span><span class="sxs-lookup"><span data-stu-id="9ffac-148">Alicia</span></span>           | <span data-ttu-id="9ffac-149">CC002</span><span class="sxs-lookup"><span data-stu-id="9ffac-149">CC002</span></span>                     | <span data-ttu-id="9ffac-150">CC003</span><span class="sxs-lookup"><span data-stu-id="9ffac-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="9ffac-151">CC007</span><span class="sxs-lookup"><span data-stu-id="9ffac-151">CC007</span></span>                     | <span data-ttu-id="9ffac-152">CC007</span><span class="sxs-lookup"><span data-stu-id="9ffac-152">CC007</span></span>                   |
| <span data-ttu-id="9ffac-153">&nbsp;&nbsp;&nbsp;&nbsp;ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="9ffac-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="9ffac-154">อาร์นี</span><span class="sxs-lookup"><span data-stu-id="9ffac-154">Arnie</span></span>            | <span data-ttu-id="9ffac-155">CC001</span><span class="sxs-lookup"><span data-stu-id="9ffac-155">CC001</span></span>                     | <span data-ttu-id="9ffac-156">CC001</span><span class="sxs-lookup"><span data-stu-id="9ffac-156">CC001</span></span>                   |
| <span data-ttu-id="9ffac-157">&nbsp;&nbsp;การผลิต</span><span class="sxs-lookup"><span data-stu-id="9ffac-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="9ffac-158">เดวิด</span><span class="sxs-lookup"><span data-stu-id="9ffac-158">David</span></span>            |                           |                         |
| <span data-ttu-id="9ffac-159">&nbsp;&nbsp;&nbsp;&nbsp;บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9ffac-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="9ffac-160">เอลเลน</span><span class="sxs-lookup"><span data-stu-id="9ffac-160">Ellen</span></span>            | <span data-ttu-id="9ffac-161">CC005</span><span class="sxs-lookup"><span data-stu-id="9ffac-161">CC005</span></span>                     | <span data-ttu-id="9ffac-162">CC005</span><span class="sxs-lookup"><span data-stu-id="9ffac-162">CC005</span></span>                   |
| <span data-ttu-id="9ffac-163">&nbsp;&nbsp;&nbsp;&nbsp;ชิ้นส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="9ffac-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="9ffac-164">คริส</span><span class="sxs-lookup"><span data-stu-id="9ffac-164">Chris</span></span>            | <span data-ttu-id="9ffac-165">CC006</span><span class="sxs-lookup"><span data-stu-id="9ffac-165">CC006</span></span>                     | <span data-ttu-id="9ffac-166">CC006</span><span class="sxs-lookup"><span data-stu-id="9ffac-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="9ffac-167">ควรกำหนดให้ผู้จัดทำบัญชีต้นทุนอยู่ระดับบนสุดของลำดับชั้น เพื่อให้สามารถดูรายการทั้งหมดในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9ffac-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="9ffac-168">ก่อนที่จะใช้ลำดับชั้นรายการเข้าถึงและการตั้งค่าความปลอดภัย ตัวเลือก **เปิดใช้งานการเข้าถึงเพื่อดูสำหรับสมาชิกมิติออบเจ็กต์ต้นทุน** ต้องตั้งค่าตัวเลือกเป็น **ใช่** บนแท็บ **ทั่วไป** ของหน้า **พารามิเตอร์การบัญชีต้นทุน** (**การบัญชีต้นทุน** > **ตั้งค่า** > **พารามิเตอร์**)</span><span class="sxs-lookup"><span data-stu-id="9ffac-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="9ffac-169">การตั้งค่าสำหรับลำดับชั้นรายการการเข้าถึงใช้เพื่อควบคุมข้อมูลที่แสดงในพื้นที่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9ffac-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="9ffac-170">พื้นที่ทำงาน **การควบคุมต้นทุน** (ในไคลเอนต์):</span><span class="sxs-lookup"><span data-stu-id="9ffac-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="9ffac-171">ข้อมูลบนเพจที่ใช้สำหรับการเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="9ffac-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="9ffac-172">พื้นที่ทำงาน **การควบคุมต้นทุน** (ในอุปกรณ์เคลื่อนที่):</span><span class="sxs-lookup"><span data-stu-id="9ffac-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="9ffac-173">ยอดดุลในบัตร</span><span class="sxs-lookup"><span data-stu-id="9ffac-173">Balances in cards</span></span>

- <span data-ttu-id="9ffac-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="9ffac-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="9ffac-175">ข้อมูลที่แสดงในการจัดรูปแบบการแสดง Power BI</span><span class="sxs-lookup"><span data-stu-id="9ffac-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="9ffac-176">การจัดรูปแบบการแสดง Power BI ของข้อมูลที่ถูกฝังในไคลเอ็นต์ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9ffac-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="9ffac-177">ก่อนที่ลำดับชั้นของรายการการเข้าถึงสามารถส่งผลต่อข้อมูลใน Power BI ลำดับชั้นของรายการการเข้าถึงและความปลอดภัยระดับแถวใน Power BI ต้องถูกจับคู่</span><span class="sxs-lookup"><span data-stu-id="9ffac-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="9ffac-178">สำหรับข้อมูลเพิ่มเติมดูที่ [การตั้งค่าความปลอดภัยสำหรับชุดเนื้อหาการบัญชีต้นทุน](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)</span><span class="sxs-lookup"><span data-stu-id="9ffac-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="9ffac-179">หัวข้อนี้แสดงข้อกำหนดเบื้องต้นที่ต้องมีอยู่ในตำแหน่งก่อนที่คุณสามารถใช้การพื้นที่ทำงาน **ควบคุมต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="9ffac-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="9ffac-180">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9ffac-180">Additional resources</span></span>

- [<span data-ttu-id="9ffac-181">พื้นที่ทำงานการควบคุมต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9ffac-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="9ffac-182">ลำดับชั้นของมิติ</span><span class="sxs-lookup"><span data-stu-id="9ffac-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="9ffac-183">การตั้งค่าความปลอดภัยสำหรับชุดเนื้อหาการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9ffac-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
