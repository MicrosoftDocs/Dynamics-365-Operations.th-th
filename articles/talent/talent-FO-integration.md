---
title: FAQ เกี่ยวกับการรวม Dynamics 365 for Talent ไปยัง Dynamics 365 for Finance and Operations
description: หัวข้อนี้อธิบายว่าข้อมูลใดจะถูกซิงโครไนส์ในการรวม Talent และ Finance and Operations
author: negudava
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aea025bc4898d6399e82030cf1f52b21949e014f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306453"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a><span data-ttu-id="f048f-103">FAQ เกี่ยวกับการรวม Dynamics 365 for Talent ไปยัง Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-103">Dynamics 365 for Talent to Dynamics 365 for Finance and Operations integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f048f-104">หัวข้อนี้ตอบคำถามสำหรับคำถามทั่วไปที่เกี่ยวข้องเกี่ยวกับว่าข้อมูลใดจะถูกซิงโครไนส์เมื่อ Dynamics 365 for Talent ถูกรวมกับ Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 for Talent is integrated with Dynamics 365 for Finance and Operations.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="f048f-105">คือข้อมูลที่ซิงโครไนซ์ทั้งหมด หรือเพียงแค่เอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f048f-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="f048f-106">ด้วยทรัพยากรบุคคลหลัก (ทรัพยากรบุคคล) ชุดย่อยของข้อมูลจะมีการซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="f048f-106">With Core Human Resources (HR), a subset of the data is synchronized.</span></span> <span data-ttu-id="f048f-107">สำหรับรายการของเอนทิตี้ทั้งหมด ดู [การรวมจาก Dynamics 365 for Talent ไปยัง Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md)</span><span class="sxs-lookup"><span data-stu-id="f048f-107">For a list of all the entities, see [Integration from Dynamics 365 for Talent to Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="f048f-108">สำหรับ Attract และ Onboard ข้อมูลทั้งหมดเป็นข้อมูลหลักของ Common Data Service (CDS) สำหรับแอป</span><span class="sxs-lookup"><span data-stu-id="f048f-108">For Attract and Onboard, all data is native to Common Data Services (CDS) for Apps.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="f048f-109">ฉันสามารถสร้างการแม็ปใหม่โดยไม่ใช้เท็มเพลได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f048f-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="f048f-110">เท็มเพลตเป็นจุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f048f-110">Templates are the starting point.</span></span> <span data-ttu-id="f048f-111">คุณสามารถสร้างเท็มเพลตของคุณเอง แต่จำเป็นต้องใช้เท็มเพลเสมอเมื่อสร้างโครงการการรวม</span><span class="sxs-lookup"><span data-stu-id="f048f-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="f048f-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวรวมข้อมูล (DI) เท็มเพลต และโครงการ ดูที่ [รวมข้อมูลลงใน Common Data Service สำหรับแอป](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="f048f-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a><span data-ttu-id="f048f-113">ฉันสามารถแม็ปมิติทางการเงินที่จะโอนย้ายระหว่าง Talent และ Finance and Operations ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f048f-113">Can I map financial dimensions to transfer between Talent and Finance and Operations?</span></span>

<span data-ttu-id="f048f-114">ในปัจจุบันมิติทางการเงินไม่ได้อยู่ใน CDS สำหรับแอป และผลลัพธ์ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f048f-114">Financial dimensions aren’t currently in CDS for Apps and as a result aren’t part of the default template.</span></span> <span data-ttu-id="f048f-115">เอนทิตี้นี้มีการวางแผน แต่ไม่มีเส้นเวลาการนำออกใช้ที่พร้อมใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f048f-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="f048f-116">สำหรับข้อมูลที่อยู่ใน Finance and Operations แต่ไม่มีอยู่ใน Talent ให้เชื่อมโยงสองระบบเข้าด้วยกันโดยใช้ **ตั้งค่าคอนฟิกลิงค์** ใน Talent</span><span class="sxs-lookup"><span data-stu-id="f048f-116">For data that resides in Finance and Operations but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="f048f-117">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกการเชื่อมโยงระหว่าง Talent และ Finance and Operations ดูที่ [มีอะไรใหม่หรือมีการเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (31 ตุลาคม 2018)](whats-new-talent-october-31.md)</span><span class="sxs-lookup"><span data-stu-id="f048f-117">For more information about how to configure links between Talent and Finance and Operations, see [What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a><span data-ttu-id="f048f-118">ในบางครั้งเมื่อฉันนำเข้าพนักงาน รายการจะไปอยู่ที่พนักงานที่ไม่ได้ใช้งานใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-118">Sometimes when I import employees, they go into inactive workers in Finance and Operations.</span></span> <span data-ttu-id="f048f-119">เพราะเหตุใด?</span><span class="sxs-lookup"><span data-stu-id="f048f-119">Why?</span></span>

<span data-ttu-id="f048f-120">คุณอาจได้รับข้อผิดพลาดนี้ถ้าพนักงานไม่มีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่ใน Talent</span><span class="sxs-lookup"><span data-stu-id="f048f-120">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="f048f-121">เมื่อต้องการแก้ไขปัญหานี้ ไปที่ **การจัดการบุคลากร \> พนักงาน \> ประวัติการจ้างงาน \> ตัวจัดการวันที่** และตรวจสอบว่ามีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f048f-121">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="f048f-122">ถ้าฉันเลือกที่จะแม็ปเฉพาะชุดย่อยของฟิลด์ การเปลี่ยนแปลงของฟิลด์ที่ไม่ได้แม็ปจะทริกเกอร์การซิงค์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f048f-122">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="f048f-123">ซิงค์ข้อมูลเป็นไปตามกำหนดการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="f048f-123">Data sync follows the execution schedule.</span></span> <span data-ttu-id="f048f-124">การรวมจะเบิกสินค้าเรกคอร์ดถ้าฟิลด์ใดๆ ในเรกคอร์ดเปลี่ยนแปลง โดยไม่คำนึงถึงว่าฟิลด์ดังกล่าวเป็นส่วนหนึ่งของการแม็ปการรวม</span><span class="sxs-lookup"><span data-stu-id="f048f-124">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="f048f-125">ฉันจะส่งการเปลี่ยนแปลงของพนักงานที่ใช้งานอยู่เท่านั้น ไม่ใช่เรกคอร์ดที่สิ้นสุดการจ้างงานได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="f048f-125">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="f048f-126">ด้วยการใช้ "การสอบถามขั้นสูง" คุณสามารถกรองและปรับรูปร่างแหล่งข้อมูลก่อนที่จะส่งผ่านไปยังปลายทาง</span><span class="sxs-lookup"><span data-stu-id="f048f-126">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a><span data-ttu-id="f048f-127">ฉันสามารถระบุฟิลด์ที่จะส่งไปยัง Finance and Operations สำหรับเอนทิตี้ที่เฉพาะเจาะจงได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f048f-127">Can I specify which fields to send to Finance and Operations for a specific entity?</span></span>

<span data-ttu-id="f048f-128">คุณสามารถเพิ่มหรือลบฟิลด์ออกจากงานรวม</span><span class="sxs-lookup"><span data-stu-id="f048f-128">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="f048f-129">ไม่ใช่ฟิลด์ข้อมูลทั้งหมดที่มีอยู่ใน CDS สำหรับเอนทิตี้แอป (CDS 2.0) ที่จะถูกเติมข้อมูลจาก Core HR</span><span class="sxs-lookup"><span data-stu-id="f048f-129">Not all data fields that exist on the CDS for Apps (CDS 2.0) entity will be populated from Core HR.</span></span>
<span data-ttu-id="f048f-130">คุณสามารถเติมข้อมูลเพิ่มเติมได้ผ่าน PowerApps</span><span class="sxs-lookup"><span data-stu-id="f048f-130">Additional data can be populated via PowerApps.</span></span>

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="f048f-131">ฉันตั้งค่าการรวมเป็นชุดงาน แต่ Talent สูญเสียการเชื่อมต่อไปกับระบบปลายทาง</span><span class="sxs-lookup"><span data-stu-id="f048f-131">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="f048f-132">ฉันจะส่งชุดการเปลี่ยนแปลงเดียวกันไปยังระบบปลายทางได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="f048f-132">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="f048f-133">ไม่จำเป็นต้องมีการตั้งค่าพิเศษสำหรับการจัดการข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="f048f-133">No special setup is required for exception handling.</span></span> <span data-ttu-id="f048f-134">ตัวรวมข้อมูลจะตรวจจับและรายงานข้อผิดพลาดที่เกิดขึ้นที่ต้นทางและปลายทางโดยอัตโนมัติ และจะอนุญาตให้ลองใหม่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="f048f-134">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="f048f-135">อย่างไรก็ตาม คุณไม่สามารถแก้ไขข้อมูลด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="f048f-135">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="f048f-136">ถ้าจำเป็นต้องปรับปรุงข้อมูล ควรทำที่ต้นทางหรือปลายทางอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f048f-136">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="f048f-137">ฉันสามารถตั้งค่าการรวมสองทิศทางได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f048f-137">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="f048f-138">ไม่ได้ การรวมเป็นแบบทิศทางเดียวในขณะนี้ (Talent ไปยัง Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="f048f-138">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="f048f-139">อย่างไรก็ตาม มีเท็มเพลตเริ่มต้นที่มีอยู่เพื่อส่งข้อมูลจาก Talent ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-139">However, there is a default template available to send data from Talent to Finance and Operations.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="f048f-140">ฉันจะอนุญาตให้ลบเรกคอร์ดโดยเป็นส่วนหนึ่งของการรวมของฉันได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f048f-140">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="f048f-141">ไม่ได้ ตัวรวมข้อมูลจะไม่รวบรวมเรกคอร์ดที่ถูกลบสำหรับการโอนย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f048f-141">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="f048f-142">มีเฉพาะการสร้างข้อมูลและการปรับปรุง (UPSERT) ถูกรวมอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="f048f-142">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="f048f-143">ฉันสามารถเรียกใช้การดำเนินการที่มีข้อผิดพลาดได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f048f-143">Can I rerun the errored execution?</span></span> <span data-ttu-id="f048f-144">ถ้าเป็นเช่นนั้น จะส่งไฟล์ทั้งหมดหรือเฉพาะที่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="f048f-144">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="f048f-145">การเรียกใช้ครั้งแรกของตัวรวมข้อมูลจะรันแบบเต็มเสมอ</span><span class="sxs-lookup"><span data-stu-id="f048f-145">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="f048f-146">การเรียกใช้ในเวลาต่อมาขึ้นอยู่กับการติดตามการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="f048f-146">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="f048f-147">เมื่อดำเนินการการรันข้อผิดพลาด จะแยกเรกคอร์ดในขอบเขตของการรัน และส่งการเปลี่ยนแปลงล่าสุดจาก CDS</span><span class="sxs-lookup"><span data-stu-id="f048f-147">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from CDS.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="f048f-148">เมื่อฉันบันทึกโครงการ ฉันได้รับข้อผิดพลาด: "โครงการมีข้อผิดพลาดในการแม็ป"</span><span class="sxs-lookup"><span data-stu-id="f048f-148">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="f048f-149">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="f048f-149">What do I do?</span></span>

<span data-ttu-id="f048f-150">ตรวจสอบการตั้งค่าของคีย์รวมของคุณ ทำการเปลี่ยนแปลงที่จำเป็นเพื่อตั้งค่า แล้วรีเฟรชเอนทิตี้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="f048f-150">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="f048f-151">เมื่อมีการใช้เท็มเพลตเริ่มต้น คีย์รวมจะถูกนำเข้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f048f-151">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="f048f-152">ปัญหานี้อาจเกิดขึ้นเมื่อมีการเพิ่มงานใหม่ไปยังเท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f048f-152">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="f048f-153">ถ้าฉันมีนิติบุคคลซึ่งเป็นพนักงานที่มีการจ้างงานจำนวน N ราย ฉันต้องสร้างการแม็ปสำหรับแต่ละคนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f048f-153">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="f048f-154">ใช่ สำหรับแต่ละนิติบุคคลใน Finance and Operations คุณจำเป็นต้องมีโครงการรวมที่แยกต่างหากในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f048f-154">Yes, for each legal entity in Finance and Operations, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="f048f-155">ฉันต้องการถ่ายโอนข้อมูลที่ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้นที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="f048f-155">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="f048f-156">ฉันสามารถทำได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f048f-156">Can I do this?</span></span>

<span data-ttu-id="f048f-157">ได้ คุณสามารถเพิ่มหรือลบฟิลด์ออกจากเท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f048f-157">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="f048f-158">คุณสามารถปรับเปลี่ยนเท็มเพลตเพื่อรวมข้อมูลเพิ่มเติมจาก CDS อื่น ๆ สำหรับเอนทิตีแอป</span><span class="sxs-lookup"><span data-stu-id="f048f-158">The template can be modified to include additional data from other CDS for Apps entities.</span></span> <span data-ttu-id="f048f-159">เอนทิตีต้องอยู่ใน CDS สำหรับแอปเพื่อให้รวมอยู่ในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f048f-159">The entity must be in CDS for Apps for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="f048f-160">ฉันเพิ่งสร้างสภาพแวดล้อม Finance and Operations และ Talent ใหม่ และฉันได้รับข้อผิดพลาด "ค่าข้อมูลละเมิดข้อจำกัดความถูกต้อง"</span><span class="sxs-lookup"><span data-stu-id="f048f-160">I just created new Finance and Operations and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="f048f-161">เพราะเหตุใด?</span><span class="sxs-lookup"><span data-stu-id="f048f-161">Why?</span></span>

<span data-ttu-id="f048f-162">สาเหตุของข้อผิดพลาดนี้อาจรวม:</span><span class="sxs-lookup"><span data-stu-id="f048f-162">Reasons for this error can include:</span></span>

- <span data-ttu-id="f048f-163">การโอนย้ายข้อมูลที่เป็นผลลัพธ์ในเรกคอร์ดที่ซ้ำกันในการแยกข้อมูลลที่ต้นทาง (CDS)</span><span class="sxs-lookup"><span data-stu-id="f048f-163">The data transfer resulted in duplicate records extraction at the source (CDS).</span></span>

- <span data-ttu-id="f048f-164">การโอนย้ายข้อมูลมีค่า null สำหรับฟิลด์ที่จำเป็นใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-164">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="f048f-165">ตรวจสอบข้อมูลที่อยู่ใน CDS และตรงตามข้อกำหนดของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-165">Verify the data that is in CDS and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="f048f-166">ถ้ามีข้อผิดพลาดการดำเนินการ และรหัสพนักงานยังไม่ได้ซิงค์ ฉันจะค้นหาประวัติงานที่มีเรกคอร์ดพนักงานที่ล้มเหลวได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="f048f-166">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="f048f-167">ตัวรวมข้อมูลจะสร้างหลายโครงการใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-167">Data Integrator will create multiple projects in Finance and Operations.</span></span> <span data-ttu-id="f048f-168">ความสัมพันธ์ระหว่างงานตัวรวมข้อมูลและโครงการ Finance and Operations คือหนึ่งต่อหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f048f-168">The relationship between the Data Integrator task and the Finance and Operations project is one to one.</span></span>

<span data-ttu-id="f048f-169">ติดตามเวลาจากประวัติการดำเนินการตัวรวมข้อมูลและค้นหาโครงการดัชนี -1 ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-169">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance and Operations.</span></span> <span data-ttu-id="f048f-170">ถ้าหมายเลขงานคือ 9 ในตัวรวมข้อมูล ดัชนีใน Finance and Operations คือ 8</span><span class="sxs-lookup"><span data-stu-id="f048f-170">If the task number is 9 in Data Integrator, the index in Finance and Operations is 8.</span></span>

1. <span data-ttu-id="f048f-171">จัดดัชนีงานจากตัวรวมข้อมูล (ในตัวอย่างนี้คือ "9")</span><span class="sxs-lookup"><span data-stu-id="f048f-171">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![จับดัชนีงานจากตัวรวมข้อมูล](media/CaptureTaskIndex.png)

2. <span data-ttu-id="f048f-173">ติดตามเวลาการดำเนินการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="f048f-173">Track the execution time of the project.</span></span>

![ติดตามเวลาการดำเนินการของโครงการ](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="f048f-175">ใน Finance and Operations ระบุดัชนี - 1</span><span class="sxs-lookup"><span data-stu-id="f048f-175">In Finance and Operations, identify index - 1.</span></span> <span data-ttu-id="f048f-176">ในตัวอย่างนี้ โครงการที่มีคำเสริมท้ายเป็น "8" และเวลาการดำเนินการของดัชนีเป็น "0" โครงการจะสอดคล้องกับเวลาการดำเนินการในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="f048f-176">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![ระบุดัชนี](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a><span data-ttu-id="f048f-178">หลังจากการรวม Talent และ Finance and Operations ฉันไม่เห็นข้อมูล Talent ของฉันใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-178">After integrating Talent and Finance and Operations, I don’t see my Talent data in Finance and Operations.</span></span> <span data-ttu-id="f048f-179">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="f048f-179">What do I do?</span></span>

<span data-ttu-id="f048f-180">การรวมกับ Finance and Operations มีสองขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="f048f-180">The integration to Finance and Operations is a two-step process.</span></span> <span data-ttu-id="f048f-181">ก่อนอื่น ตรวจสอบว่ ข้อมูล Talent ถูกปรับปรุงแล้ว และพร้อมใช้งานใน CDS</span><span class="sxs-lookup"><span data-stu-id="f048f-181">First, verify that the Talent data is updated and available in CDS.</span></span> <span data-ttu-id="f048f-182">นี่เป็นการซิงค์แบบเรียลไทม์แบบใกล้ และสามารถตรวจสอบใน PowerApps โดยดูข้อมูลภายในเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f048f-182">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![ข้อมูลใน CDS](media/DataInCDS.png)

<span data-ttu-id="f048f-184">ถ้าข้อมูลไม่ปรากฏตามที่คาดไว้ใน CDS ให้ตรวจสอบว่าเอนทิตีได้รับการสนับสนุนในการรวม</span><span class="sxs-lookup"><span data-stu-id="f048f-184">If the data is not appearing as expected in CDS, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="f048f-185">เพื่อรวมข้อมูลเพิ่มเติมใน CDS จะต้องทำการเปลี่ยนแปลงทางฝั่ง Microsoft</span><span class="sxs-lookup"><span data-stu-id="f048f-185">To include additional data in CDS, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="f048f-186">ถ้าเอนทิตีได้รับการสนับสนุน และข้อมูลมีอยู่ใน CDS ให้ตรวจสอบว่าการแม็ปถูกต้องในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f048f-186">If the entity is supported and the data is available in CDS, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="f048f-187">ถ้าการค้นหาการแม็ปตัวรวมเป็นปกติ ให้ตรวจสอบมีการรันงานการจัดการข้อมูลเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="f048f-187">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="f048f-188">ข้อผิดพลาดอาจเกิดขึ้นในระหว่างการดำเนินการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="f048f-188">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="f048f-189">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการข้อมูล ดู [การจัดการข้อมูล](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)</span><span class="sxs-lookup"><span data-stu-id="f048f-189">For more information about Data Management, see [Data management](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a><span data-ttu-id="f048f-190">ที่อยู่สำหรับพนักงานของฉันไม่ถูกต้องหลังจากที่ฉันนำเข้าไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-190">The addresses for my employees are incorrect after I import them into Finance and Operations.</span></span> <span data-ttu-id="f048f-191">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="f048f-191">What should I do?</span></span>

<span data-ttu-id="f048f-192">ลำดับหมายเลขสำหรับ **รหัสที่ตั้ง** ใช้รูปแบบเดียวกันในทั้ง Talent และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-192">The number sequence for **Location ID** uses the same pattern in both Talent and Finance and Operations.</span></span> <span data-ttu-id="f048f-193">ลำดับหมายเลขต้องไม่ซ้ำกันทั้งสองด้าน เพื่อให้ไม่มีการชนกันของที่อยู่เมื่อรวมข้อมูลจาก CDS ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-193">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from CDS to Finance and Operations.</span></span>

<span data-ttu-id="f048f-194">ในระหว่างการใช้งานของ Talent ให้ตรวจสอบว่าลำดับหมายเลขไม่เหมือนกันใน Talent และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f048f-194">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance and Operations.</span></span> <span data-ttu-id="f048f-195">ตรวจสอบว่าลำดับหมายเลขทั้งหมดไม่เหมือนกันซึ่งอาจจะรักษาข้อมูลในทั้งสองระบบ</span><span class="sxs-lookup"><span data-stu-id="f048f-195">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="f048f-196">เมื่อสร้างชุดการเชื่อมต่อของฉัน ฉันไม่เห็นการเชื่อมต่อในรายการแบบหล่นลงของ Connection</span><span class="sxs-lookup"><span data-stu-id="f048f-196">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="f048f-197">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="f048f-197">What do I do?</span></span>

<span data-ttu-id="f048f-198">ตรวจสอบว่าขณะที่สร้างการเชื่อมต่อของคุณ ให้เลือก Dynamics 365 for Finance and Operations (อยู่ในการแสดงตัวอย่าง) และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f048f-198">Make sure when creating your connections, you choose Dynamics 365 for Finance and Operations (currently in preview) and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="f048f-199">เมื่อซิงค์การจ้างงาน ฉันได้รับข้อผิดพลาด "ไม่มี CompanyInfo_FK"หรือ "ไม่พบค่า '12/31/2154 11:59:59 pm' ในฟิลด์ 'วันที่สิ้นสุดการจ้างงาน' ในตารางที่เกี่ยวข้อง 'การจ้างงาน'" ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="f048f-199">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="f048f-200">ให้แน่ใจว่าคุณกำลังแม็ปกับนิติบุคคลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f048f-200">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="f048f-201">การซิงค์นิติบุคคลไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น จึงคาดว่าแต่ละนิติบุคคลที่ปรากฏใน Talent และ CDS มีอยู่ใน Finance and Operations เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="f048f-201">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and CDS is also present in Finance and Operations.</span></span>
<span data-ttu-id="f048f-202">นอกจากนี้ ให้ตรวจสอบให้แน่ใจว่าคุณกำลังเลือกนิติบุคคลที่ถูกต้องสำหรับชุดการเชื่อมต่อที่มีการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="f048f-202">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="f048f-203">หลังจากการตั้งค่าโครงการของฉัน การแม็ปฟิลด์สำหรับ Finance and Operations จะกลายเป็นว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f048f-203">After setting up my project, the field mapping for Finance and Operations appears to be empty.</span></span> <span data-ttu-id="f048f-204">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="f048f-204">What should I do?</span></span>

<span data-ttu-id="f048f-205">รีเฟรชเอนทิตี้ข้อมูลใน Finance and Operations โดยไปที่ **การจัดการข้อมูล \> พารามิเตอร์กรอบงาน \> การตั้งค่าเอนทิตี้ \> รีเฟรชรายการเอนทิตี้**</span><span class="sxs-lookup"><span data-stu-id="f048f-205">Refresh the data entities in Finance and Operations by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="f048f-206">ซึ่งควรใช้เวลาสองสามนาทีในการทำให้เสร็จสมบูรณ์ จากนั้นคุณควรเห็นแมปเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="f048f-206">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="f048f-207">ปัญหานี้เกิดขึ้นเมื่อมีการสร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="f048f-207">This issue occurs when new projects are created.</span></span>

![ไม่มีการแม็ปฟิลด์](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="f048f-209">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f048f-209">Additional resources</span></span>

- <span data-ttu-id="f048f-210">ตัวรวมข้อมูล (DI):</span><span class="sxs-lookup"><span data-stu-id="f048f-210">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="f048f-211">รวมข้อมูลลงใน Common Data Service สำหรับแอป</span><span class="sxs-lookup"><span data-stu-id="f048f-211">Integrate data into Common Data Service for Apps</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="f048f-212">การจัดการข้อผิดพลาดตัวรวมข้อมูลและการแก้ไขปัญหาเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="f048f-212">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="f048f-213">การตอบสนองคำขอ DSR สำหรับล็อกที่ระบบสร้างขึ้นใน PowerApps Microsoft Flow และ Common Data Service สำหรับแอป</span><span class="sxs-lookup"><span data-stu-id="f048f-213">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service for Apps</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="f048f-214">การจัดการข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="f048f-214">Data Management:</span></span>

  - [<span data-ttu-id="f048f-215">การจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f048f-215">Data management</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
