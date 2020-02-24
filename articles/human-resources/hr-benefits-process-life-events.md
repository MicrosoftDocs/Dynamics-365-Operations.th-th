---
title: ประมวลผลเหตุการณ์ของชีวิต
description: ในระหว่างววงจรชีวิตของพนักงานใน Microsoft Dynamics 365 Human Resources พนักงานแต่ละคนอาจพบการเปลี่ยนแปลงเหตุการณ์ของชีวิตต่าง ๆ
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
ms.openlocfilehash: 91812432ead4b0afccfba30f8023f014e216236a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010742"
---
# <a name="process-life-events"></a><span data-ttu-id="4d7d8-103">ประมวลผลเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="4d7d8-103">Process life events</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="4d7d8-104">ในระหว่างววงจรชีวิตของพนักงานใน Microsoft Dynamics 365 Human Resources พนักงานแต่ละคนอาจพบการเปลี่ยนแปลงเหตุการณ์ของชีวิตต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="4d7d8-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="4d7d8-105">ตัวอย่างเช่น การแต่งงาน การเปลี่ยนแปลงในการจ้างงาน หรือการเปลี่ยนแปลงของผู้รับผลประโยชน์/ผู้รับผลประโยชน์</span><span class="sxs-lookup"><span data-stu-id="4d7d8-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="4d7d8-106">เมื่อต้องการใช้เหตุการณ์ของชีวิต คุณต้องเปิดใช้งานเหตุการณ์ของชีวิตในฟอร์มพารามิเตอร์สวัสดิ ตั้งค่าชนิดเหตุการณ์ของชีวิต และตั้งค่าตัวเลือกเหตุการณ์ของชีวิตสำหรับชนิดของแผน</span><span class="sxs-lookup"><span data-stu-id="4d7d8-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="4d7d8-107">ก่อนที่คุณจะสามารถประมวลผลเหตุการณ์ของชีวิต คุณต้องรันการลงทะเบียนที่เปิดค้างไว้แล้วอย่างน้อยหนึ่งครั้งในระหว่างกรอบเวลาการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="4d7d8-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="4d7d8-108">ในสหรัฐอเมริกา การลงทะเบียนแบบเปิดโดยทั่วไปจะทำหนึ่งครั้งในแต่ละปี</span><span class="sxs-lookup"><span data-stu-id="4d7d8-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="4d7d8-109">นอกสหรัฐอเมริกา การลงทะเบียนแบบเปิดอาจรันในเวลาของการจ้าง</span><span class="sxs-lookup"><span data-stu-id="4d7d8-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="4d7d8-110">ผู้ปฏิบัติงานไม่จำเป็นต้องเลือกแผนสวัสดิการเพื่อให้สามารถประมวลผลเหตุการณ์ของชีวิตต่าง ๆ ได้ แต่ผู้ปฏิบัติงานต้องรวมอยู่ในการประมวลผลการลงทะเบียนที่เปิดค้างไว้</span><span class="sxs-lookup"><span data-stu-id="4d7d8-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="4d7d8-111">ใช้การประมวลผลเหตุการณ์ของชีวิต เมื่อคุณมีผู้ปฏิบัติงานที่มีเหตุการณ์ของชีวิตที่เกิดขึ้นในอนาคต</span><span class="sxs-lookup"><span data-stu-id="4d7d8-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="4d7d8-112">เหตุการณ์นี้จะประมวลผลเหตุการณ์ของชีวิตทั้งหมดที่ยังไม่ได้รับการประมวลผล (เช่น เหตุการณ์ของชีวิตในอนาคต หรือเหตุการณ์ของชีวิตที่มีการเพิ่มที่ไม่เกี่ยวข้องกับผู้ปฏิบัติงานหนึ่งคนขึ้นไป – ตัวอย่างหนึ่งคือสวัสดิการใหม่)</span><span class="sxs-lookup"><span data-stu-id="4d7d8-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="4d7d8-113">เหตุการณ์ของชีวิตแบบเวลาจริงจะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="4d7d8-113">Real time life events are hidden.</span></span>

<span data-ttu-id="4d7d8-114">ตัวอย่างเช่น ถ้าวันนี้เป็นวันที่ 1 กุมภาพันธ์ และเมื่อวันที่ 14 กุมภาพันธ์ ผู้ปฏิบัติงาน โจ สมิธ ได้รับการจัดกำหนดการให้เปลี่ยนนิติบุคคล ถ้าคุณรันการประมวลผลเหตุการณ์ของชีวิตสำหรับวันที่ 15 กุมภาพันธ์ ระบบจะประมวลผลเหตุการณ์ทั้งหมดจนถึงวันที่ 15 กุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="4d7d8-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="4d7d8-115">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **กำลังประมวลผลในเหตุการณ์ของชีวิต**</span><span class="sxs-lookup"><span data-stu-id="4d7d8-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="4d7d8-116">ในกล่องโต้ตอบ **ดำเนินการประมวลผลในเหตุการณ์ของชีวิต** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4d7d8-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="4d7d8-117">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="4d7d8-117">Field</span></span> | <span data-ttu-id="4d7d8-118">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4d7d8-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4d7d8-119">รอบระยะเวลาการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="4d7d8-119">Enrollment period</span></span> | <span data-ttu-id="4d7d8-120">รอบระยะเวลาการลงทะเบียนที่จะประมวลผลเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="4d7d8-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="4d7d8-121">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="4d7d8-121">Legal entity</span></span> | <span data-ttu-id="4d7d8-122">นิติบุคคลที่จะประมวลผลเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="4d7d8-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="4d7d8-123">วันที่เหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="4d7d8-123">Life event date</span></span> | <span data-ttu-id="4d7d8-124">ระบบประมวลผลเหตุการณ์ทั้งหมดในระหว่างรอบระยะเวลาของการลงทะเบียนที่เกิดขึ้นจนถึงวันนี้</span><span class="sxs-lookup"><span data-stu-id="4d7d8-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="4d7d8-125">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4d7d8-125">Worker</span></span> | <span data-ttu-id="4d7d8-126">ผู้ปฏิบัติงานที่จะประมวลผลเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="4d7d8-126">The worker to process life events for.</span></span> <span data-ttu-id="4d7d8-127">ถ้าคุณปล่อยฟิลด์นี้ว่างไว้ เหตุการณ์ของชีวิตจะมีการดำเนินการสำหรับผู้ปฏิบัติงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4d7d8-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="4d7d8-128">ถ้าคุณต้องการดำเนินการกระบวนการในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4d7d8-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="4d7d8-129">ป้อนข้อมูลสำหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="4d7d8-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="4d7d8-130">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4d7d8-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="4d7d8-131">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4d7d8-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="4d7d8-132">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4d7d8-132">Select **OK**.</span></span> <span data-ttu-id="4d7d8-133">กระบวนการจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="4d7d8-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="4d7d8-134">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4d7d8-134">Select **OK**.</span></span>
