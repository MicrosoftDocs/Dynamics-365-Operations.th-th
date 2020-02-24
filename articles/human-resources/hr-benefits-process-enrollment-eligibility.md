---
title: ประมวลผลการมีสิทธิ์ในการลงทะเบียน
description: บทความนี้อธิบายถึงวิธีการรันกระบวนการมีสิทธิ์ในการลงทะเบียน
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010677"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="bcd67-103">ประมวลผลการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="bcd67-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="bcd67-104">บทความนี้อธิบายถึงวิธีการรันกระบวนการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="bcd67-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="bcd67-105">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **กำลังประมวลผลการมีสิทธิ์ในการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="bcd67-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="bcd67-106">ในกล่องโต้ตอบ **ดำเนินการประมวลผลสวัสดิการการลงทะเบียน** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bcd67-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="bcd67-107">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="bcd67-107">Field</span></span> | <span data-ttu-id="bcd67-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bcd67-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bcd67-109">รอบระยะเวลาการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="bcd67-109">Enrollment period</span></span> | <span data-ttu-id="bcd67-110">รอบระยะเวลาการลงทะเบียนที่จะประมวลผลการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="bcd67-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="bcd67-111">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="bcd67-111">Legal entity</span></span> | <span data-ttu-id="bcd67-112">นิติบุคคลที่จะประมวลผลการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="bcd67-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="bcd67-113">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="bcd67-113">Worker</span></span> | <span data-ttu-id="bcd67-114">ผู้ปฏิบัติงานที่จะประมวลผลการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="bcd67-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="bcd67-115">ถ้าคุณปล่อยฟิลด์นี้ว่างไว้ การมีสิทธิ์ในการลงทะเบียนจะมีการดำเนินการสำหรับผู้ปฏิบัติงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bcd67-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="bcd67-116">แผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bcd67-116">Benefit plan</span></span> | <span data-ttu-id="bcd67-117">แผนสวัสดิการที่จะประมวลผลการมีสิทธิ์ในการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="bcd67-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="bcd67-118">ถ้าคุณต้องการดำเนินการกระบวนการในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bcd67-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="bcd67-119">ป้อนข้อมูลสำหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="bcd67-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="bcd67-120">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bcd67-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="bcd67-121">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bcd67-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="bcd67-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bcd67-122">Select **OK**.</span></span> <span data-ttu-id="bcd67-123">กระบวนการจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="bcd67-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="bcd67-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bcd67-124">Select **OK**.</span></span>
