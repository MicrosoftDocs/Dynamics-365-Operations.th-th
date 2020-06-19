---
title: การเปลี่ยนแปลงอัตราของกระบวนการ
description: การเปลี่ยนแปลงอัตราของกระบวนการใน Microsoft Dynamics 365 Human Resources เมื่อแผนสวัสดิการใหม่หรือที่มีอยู่มีการเปลี่ยนแปลงการตั้งค่ากฎการมีสิทธิ์
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b12c845b92b29063f3b0b2f6a9d98143b7f10eff
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429208"
---
# <a name="process-rate-changes"></a><span data-ttu-id="d170a-103">การเปลี่ยนแปลงอัตราของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="d170a-103">Process rate changes</span></span>

<span data-ttu-id="d170a-104">การเปลี่ยนแปลงอัตราของกระบวนการใน Microsoft Dynamics 365 Human Resources เมื่อแผนสวัสดิการใหม่หรือที่มีอยู่มีการเปลี่ยนแปลงการตั้งค่ากฎการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="d170a-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="d170a-105">ถ้ากฎการมีสิทธิ์ใหม่ถูกสร้างขึ้นและกำหนดให้กับแผน จะมีการแจ้งให้ระบบดำเนินการให้สิทธิ์ผู้ปฏิบัติงานใหม่อีกครั้ง เพื่อตรวจสอบว่าผู้ปฏิบัติงานอาจมีสิทธิ์สำหรับแผนตามตัวเลือกการมีสิทธิ์ใหม่นี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="d170a-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="d170a-106">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **การประมวลผลอัพเดตการเปลี่ยนแปลงอัตรา**</span><span class="sxs-lookup"><span data-stu-id="d170a-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="d170a-107">ในกล่องโต้ตอบ **ดำเนินกระบวนการอัพเดตอัตราของสวัสดิการ** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d170a-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="d170a-108">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="d170a-108">Field</span></span> | <span data-ttu-id="d170a-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d170a-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d170a-110">**รอบระยะเวลาการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="d170a-110">**Enrollment period**</span></span> | <span data-ttu-id="d170a-111">รอบระยะเวลาการลงทะเบียนที่จะประมวลผลการเปลี่ยนแปลงอัตรา</span><span class="sxs-lookup"><span data-stu-id="d170a-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="d170a-112">ถ้าคุณต้องการดำเนินการกระบวนการในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d170a-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="d170a-113">ป้อนข้อมูลสำหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="d170a-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="d170a-114">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d170a-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="d170a-115">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d170a-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="d170a-116">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d170a-116">Select **OK**.</span></span> <span data-ttu-id="d170a-117">กระบวนการจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="d170a-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="d170a-118">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d170a-118">Select **OK**.</span></span>
