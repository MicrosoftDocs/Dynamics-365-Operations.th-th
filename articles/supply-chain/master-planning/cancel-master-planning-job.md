---
title: ยกเลิกงานการวางแผนหลัก
description: หัวข้อนี้จะอธิบายถึงวิธีการยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการวางแผนในตัว
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 40d657a02df0cba66918a6853ec62621501cfdfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989804"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="f137c-103">ยกเลิกงานการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="f137c-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f137c-104">ใน Microsoft Dynamics 365 Supply Chain Management มีหลายตัวเลือกสำหรับการยกเลิกงานการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="f137c-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="f137c-105">ตัวอย่างเช่น คุณอาจต้องการยกเลิกงานการวางแผนหลัก ถ้ามีการเริ่มต้นโดยไม่ได้ตั้งใจหรือทำงานนานกว่าที่คาดไว้และคุณต้องการที่จะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="f137c-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="f137c-106">วิธีที่ดีที่สุดในการยกเลิกงานการวางแผนคือจากหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="f137c-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="f137c-107">ตัวเลือกอื่นจากหน้า **ชุดงาน** และ **ชุดงานที่ปรับปรุง** ควรจะใช้เฉพาะเมื่อยกเลิกงานการวางแผนหลักจาหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสมบูรณ์** ไม่เสร็จภายในไม่กี่นาที</span><span class="sxs-lookup"><span data-stu-id="f137c-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="f137c-108">ตัวเลือกการยกเลิกที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f137c-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="f137c-109">ยกเลิกงานการวางแผนหลักจากหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="f137c-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="f137c-110">ไปยัง **การวางแผนหลัก > การสอบถามและรายงาน > การวางแผนหลัก > กระบวนการวางแผนที่ยังไม่เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="f137c-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="f137c-111">เลือกบรรทัดที่กระบวนการวางแผนที่คุณต้องการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="f137c-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="f137c-112">คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="f137c-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="f137c-113">ตัวเลือกยกเลิกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f137c-113">Additional cancel options</span></span>
<span data-ttu-id="f137c-114">รายการเหล่านี้ควรถูกใช้ เมื่อยกเลิกงานการวางแผนหลักจากหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสิ้น** ไม่เสร็จสมบูรณ์ภายในสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="f137c-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="f137c-115">ลบงานการวางแผนหลักออกจากหน้า **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="f137c-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="f137c-116">ไปที่ **การดูแลระบบ > การสอบถาม > ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="f137c-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="f137c-117">เลือกบรรทัดที่กระบวนการวางแผนงานที่คุณต้องการลบ</span><span class="sxs-lookup"><span data-stu-id="f137c-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="f137c-118">คลิก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="f137c-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="f137c-119">ยกเลิกงานการวางแผนหลักออกจากหน้า **ชุดงานที่ปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="f137c-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="f137c-120">ไปที่ **การดูแลระบบ > การสอบถาม > ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="f137c-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="f137c-121">ถ้าไม่มีการแสดงรหัสงานในรายการให้คลิก **สลับไปยังแบบฟอร์มที่ปรับปรุงแล้ว** มิฉะนั้นดำเนินการขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="f137c-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="f137c-122">เปิดชุดงาน</span><span class="sxs-lookup"><span data-stu-id="f137c-122">Open the batch job.</span></span> <span data-ttu-id="f137c-123">คลิก **รหัสงาน** สำหรับชุดงานที่มีงานที่คุณต้องการสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="f137c-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="f137c-124">ใน **ชุดงาน** เลือกงานที่จะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="f137c-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="f137c-125">คลิก **เปลี่ยนแปลงสถานะ** เลือก **การยกเลิก** และคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f137c-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="f137c-126">บนแท็บ **ชุดงาน** ให้คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="f137c-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>
