---
title: ยกเลิกงานการวางแผนหลัก
description: หัวข้อนี้จะอธิบายถึงวิธีการยกเลิกงานการวางแผนที่ใช้งานอยู่ ซึ่งใช้ฟังก์ชันการวางแผนในตัว
author: ChristianRytt
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 513aee3b9475506e28db4bffe90df58567b6b281
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816615"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="d50c0-103">ยกเลิกงานการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="d50c0-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d50c0-104">ใน Microsoft Dynamics 365 Supply Chain Management มีหลายตัวเลือกสำหรับการยกเลิกงานการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="d50c0-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="d50c0-105">ตัวอย่างเช่น คุณอาจต้องการยกเลิกงานการวางแผนหลัก ถ้ามีการเริ่มต้นโดยไม่ได้ตั้งใจหรือทำงานนานกว่าที่คาดไว้และคุณต้องการที่จะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="d50c0-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="d50c0-106">วิธีที่ดีที่สุดในการยกเลิกงานการวางแผนคือจากหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="d50c0-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="d50c0-107">ตัวเลือกอื่นจากหน้า **ชุดงาน** และ **ชุดงานที่ปรับปรุง** ควรจะใช้เฉพาะเมื่อยกเลิกงานการวางแผนหลักจาหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสมบูรณ์** ไม่เสร็จภายในไม่กี่นาที</span><span class="sxs-lookup"><span data-stu-id="d50c0-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="d50c0-108">ตัวเลือกการยกเลิกที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d50c0-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="d50c0-109">ยกเลิกงานการวางแผนหลักจากหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="d50c0-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="d50c0-110">ไปยัง **การวางแผนหลัก > การสอบถามและรายงาน > การวางแผนหลัก > กระบวนการวางแผนที่ยังไม่เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="d50c0-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="d50c0-111">เลือกบรรทัดที่กระบวนการวางแผนที่คุณต้องการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="d50c0-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="d50c0-112">คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="d50c0-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="d50c0-113">ตัวเลือกยกเลิกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d50c0-113">Additional cancel options</span></span>
<span data-ttu-id="d50c0-114">รายการเหล่านี้ควรถูกใช้ เมื่อยกเลิกงานการวางแผนหลักจากหน้า **กระบวนการวางแผนที่ยังไม่เสร็จสิ้น** ไม่เสร็จสมบูรณ์ภายในสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="d50c0-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="d50c0-115">ลบงานการวางแผนหลักออกจากหน้า **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="d50c0-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="d50c0-116">ไปที่ **การดูแลระบบ > การสอบถาม > ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="d50c0-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="d50c0-117">เลือกบรรทัดที่กระบวนการวางแผนงานที่คุณต้องการลบ</span><span class="sxs-lookup"><span data-stu-id="d50c0-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="d50c0-118">คลิก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="d50c0-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="d50c0-119">ยกเลิกงานการวางแผนหลักออกจากหน้า **ชุดงานที่ปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="d50c0-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="d50c0-120">ไปที่ **การดูแลระบบ > การสอบถาม > ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="d50c0-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="d50c0-121">ถ้าไม่มีการแสดงรหัสงานในรายการให้คลิก **สลับไปยังแบบฟอร์มที่ปรับปรุงแล้ว** มิฉะนั้นดำเนินการขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="d50c0-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="d50c0-122">เปิดชุดงาน</span><span class="sxs-lookup"><span data-stu-id="d50c0-122">Open the batch job.</span></span> <span data-ttu-id="d50c0-123">คลิก **รหัสงาน** สำหรับชุดงานที่มีงานที่คุณต้องการสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="d50c0-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="d50c0-124">ใน **ชุดงาน** เลือกงานที่จะสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="d50c0-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="d50c0-125">คลิก **เปลี่ยนแปลงสถานะ** เลือก **การยกเลิก** และคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d50c0-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="d50c0-126">บนแท็บ **ชุดงาน** ให้คลิก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="d50c0-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]