---
title: FAQ เกี่ยวกับการรวม Dynamics 365 Talent ไปยัง Dynamics 365 Finance
description: หัวข้อนี้อธิบายว่าข้อมูลใดจะถูกซิงโครไนส์ในการรวม Talent และ Finance
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5bb855e6dd7ff236b7bda9e59e12ed8cc8ab9bc9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251026"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a><span data-ttu-id="dd964-103">FAQ เกี่ยวกับการรวม Dynamics 365 Talent ไปยัง Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="dd964-103">Dynamics 365 Talent to Dynamics 365 Finance integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dd964-104">หัวข้อนี้ตอบคำถามสำหรับคำถามทั่วไปที่เกี่ยวข้องเกี่ยวกับว่าข้อมูลใดจะถูกซิงโครไนส์เมื่อ Dynamics 365 Talent ถูกรวมกับ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="dd964-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Talent is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="dd964-105">คือข้อมูลที่ซิงโครไนซ์ทั้งหมด หรือเพียงแค่เอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dd964-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="dd964-106">สำหรับ Core HR ชุดย่อยของข้อมูลจะมีการซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="dd964-106">For Core HR, a subset of the data is synchronized.</span></span> <span data-ttu-id="dd964-107">สำหรับรายการของเอนทิตี้ทั้งหมด ดู [การรวมจาก Dynamics 365 Talent ไปยัง Dynamics 365 Finance](talent-financeandoperations-integration.md)</span><span class="sxs-lookup"><span data-stu-id="dd964-107">For a list of all the entities, see [Integration from Dynamics 365 Talent to Dynamics 365 Finance](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="dd964-108">สำหรับ Attract และ Onboard ข้อมูลทั้งหมดเป็นข้อมูลหลักของ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dd964-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="dd964-109">ฉันสามารถสร้างการแม็ปใหม่โดยไม่ใช้เท็มเพลได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="dd964-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="dd964-110">เท็มเพลตเป็นจุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd964-110">Templates are the starting point.</span></span> <span data-ttu-id="dd964-111">คุณสามารถสร้างเท็มเพลตของคุณเอง แต่จำเป็นต้องใช้เท็มเพลเสมอเมื่อสร้างโครงการการรวม</span><span class="sxs-lookup"><span data-stu-id="dd964-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="dd964-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวรวมข้อมูล (DI) เท็มเพลต และโครงการ ดูที่ [รวมข้อมูลลงใน Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="dd964-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a><span data-ttu-id="dd964-113">ฉันสามารถแม็ปมิติทางการเงินที่จะโอนย้ายระหว่าง Talent และ Finance ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="dd964-113">Can I map financial dimensions to transfer between Talent and Finance?</span></span>

<span data-ttu-id="dd964-114">ในปัจจุบันมิติทางการเงินไม่ได้อยู่ใน Common Data Service สำหรับแอป และผลลัพธ์ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="dd964-114">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="dd964-115">เอนทิตี้นี้มีการวางแผน แต่ไม่มีเส้นเวลาการนำออกใช้ที่พร้อมใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="dd964-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="dd964-116">สำหรับข้อมูลที่อยู่ใน Finance แต่ไม่มีอยู่ใน Talent ให้เชื่อมโยงสองระบบเข้าด้วยกันโดยใช้ **ตั้งค่าคอนฟิกลิงค์** ใน Talent</span><span class="sxs-lookup"><span data-stu-id="dd964-116">For data that resides in Finance but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="dd964-117">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกการเชื่อมโยงระหว่าง Talent และ Finance ดูที่ [มีอะไรใหม่หรือมีการเปลี่ยนแปลงใน Dynamics 365 Talent: Core HR (31 ตุลาคม 2018)](whats-new-talent-october-31.md)</span><span class="sxs-lookup"><span data-stu-id="dd964-117">For more information about how to configure links between Talent and Finance, see [What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![แม็ปมิติทางการเงิน](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="dd964-119">ในบางครั้งเมื่อฉันนำเข้าพนักงาน รายการจะไปอยู่ที่พนักงานที่ไม่ได้ใช้งานใน Finance</span><span class="sxs-lookup"><span data-stu-id="dd964-119">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="dd964-120">เพราะเหตุใด?</span><span class="sxs-lookup"><span data-stu-id="dd964-120">Why?</span></span>

<span data-ttu-id="dd964-121">คุณอาจได้รับข้อผิดพลาดนี้ถ้าพนักงานไม่มีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่ใน Talent</span><span class="sxs-lookup"><span data-stu-id="dd964-121">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="dd964-122">เมื่อต้องการแก้ไขปัญหานี้ ไปที่ **การจัดการบุคลากร \> พนักงาน \> ประวัติการจ้างงาน \> ตัวจัดการวันที่** และตรวจสอบว่ามีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="dd964-122">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="dd964-123">ถ้าฉันเลือกที่จะแม็ปเฉพาะชุดย่อยของฟิลด์ การเปลี่ยนแปลงของฟิลด์ที่ไม่ได้แม็ปจะทริกเกอร์การซิงค์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="dd964-123">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="dd964-124">ซิงค์ข้อมูลเป็นไปตามกำหนดการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="dd964-124">Data sync follows the execution schedule.</span></span> <span data-ttu-id="dd964-125">การรวมจะเบิกสินค้าเรกคอร์ดถ้าฟิลด์ใดๆ ในเรกคอร์ดเปลี่ยนแปลง โดยไม่คำนึงถึงว่าฟิลด์ดังกล่าวเป็นส่วนหนึ่งของการแม็ปการรวม</span><span class="sxs-lookup"><span data-stu-id="dd964-125">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="dd964-126">ฉันจะส่งการเปลี่ยนแปลงของพนักงานที่ใช้งานอยู่เท่านั้น ไม่ใช่เรกคอร์ดที่สิ้นสุดการจ้างงานได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="dd964-126">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="dd964-127">ด้วยการใช้ "การสอบถามขั้นสูง" คุณสามารถกรองและปรับรูปร่างแหล่งข้อมูลก่อนที่จะส่งผ่านไปยังปลายทาง</span><span class="sxs-lookup"><span data-stu-id="dd964-127">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![การสอบถามขั้นสูงของผู้ปฏิบัติงานที่ใช้งานอยู่](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="dd964-129">ฉันสามารถระบุฟิลด์ที่จะส่งไปยัง Finance สำหรับเอนทิตีที่เฉพาะเจาะจงได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="dd964-129">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="dd964-130">คุณสามารถเพิ่มหรือลบฟิลด์ออกจากงานรวม</span><span class="sxs-lookup"><span data-stu-id="dd964-130">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="dd964-131">ไม่ใช่ฟิลด์ข้อมูลทั้งหมดที่มีอยู่ในเอนทิตี้ Common Data Service ที่จะถูกเติมข้อมูลจาก Core HR</span><span class="sxs-lookup"><span data-stu-id="dd964-131">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="dd964-132">คุณสามารถเติมข้อมูลเพิ่มเติมได้ผ่าน PowerApps</span><span class="sxs-lookup"><span data-stu-id="dd964-132">Additional data can be populated via PowerApps.</span></span>

![เพิ่มหรือลบฟิลด์ไปยังและออกจากงานการรวม](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="dd964-134">ฉันตั้งค่าการรวมเป็นชุดงาน แต่ Talent สูญเสียการเชื่อมต่อไปกับระบบปลายทาง</span><span class="sxs-lookup"><span data-stu-id="dd964-134">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="dd964-135">ฉันจะส่งชุดการเปลี่ยนแปลงเดียวกันไปยังระบบปลายทางได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="dd964-135">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="dd964-136">ไม่จำเป็นต้องมีการตั้งค่าพิเศษสำหรับการจัดการข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="dd964-136">No special setup is required for exception handling.</span></span> <span data-ttu-id="dd964-137">ตัวรวมข้อมูลจะตรวจจับและรายงานข้อผิดพลาดที่เกิดขึ้นที่ต้นทางและปลายทางโดยอัตโนมัติ และจะอนุญาตให้ลองใหม่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="dd964-137">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="dd964-138">อย่างไรก็ตาม คุณไม่สามารถแก้ไขข้อมูลด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="dd964-138">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="dd964-139">ถ้าจำเป็นต้องปรับปรุงข้อมูล ควรทำที่ต้นทางหรือปลายทางอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dd964-139">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="dd964-140">ฉันสามารถตั้งค่าการรวมสองทิศทางได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="dd964-140">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="dd964-141">ไม่ได้ การรวมเป็นแบบทิศทางเดียวในขณะนี้ (Talent ไปยัง Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="dd964-141">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="dd964-142">อย่างไรก็ตาม มีเท็มเพลตเริ่มต้นที่มีอยู่เพื่อส่งข้อมูลจาก Talent ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="dd964-142">However, there is a default template available to send data from Talent to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="dd964-143">ฉันจะอนุญาตให้ลบเรกคอร์ดโดยเป็นส่วนหนึ่งของการรวมของฉันได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="dd964-143">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="dd964-144">ไม่ได้ ตัวรวมข้อมูลจะไม่รวบรวมเรกคอร์ดที่ถูกลบสำหรับการโอนย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dd964-144">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="dd964-145">มีเฉพาะการสร้างข้อมูลและการปรับปรุง (UPSERT) ถูกรวมอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="dd964-145">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="dd964-146">ฉันสามารถเรียกใช้การดำเนินการที่มีข้อผิดพลาดได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="dd964-146">Can I rerun the errored execution?</span></span> <span data-ttu-id="dd964-147">ถ้าเป็นเช่นนั้น จะส่งไฟล์ทั้งหมดหรือเฉพาะที่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="dd964-147">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="dd964-148">การเรียกใช้ครั้งแรกของตัวรวมข้อมูลจะรันแบบเต็มเสมอ</span><span class="sxs-lookup"><span data-stu-id="dd964-148">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="dd964-149">การเรียกใช้ในเวลาต่อมาขึ้นอยู่กับการติดตามการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="dd964-149">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="dd964-150">เมื่อดำเนินการการรันข้อผิดพลาด จะแยกเรกคอร์ดในขอบเขตของการรัน และส่งการเปลี่ยนแปลงล่าสุดจาก Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dd964-150">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="dd964-151">เมื่อฉันบันทึกโครงการ ฉันได้รับข้อผิดพลาด: "โครงการมีข้อผิดพลาดในการแม็ป"</span><span class="sxs-lookup"><span data-stu-id="dd964-151">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="dd964-152">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="dd964-152">What do I do?</span></span>

<span data-ttu-id="dd964-153">ตรวจสอบการตั้งค่าของคีย์รวมของคุณ ทำการเปลี่ยนแปลงที่จำเป็นเพื่อตั้งค่า แล้วรีเฟรชเอนทิตี้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="dd964-153">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="dd964-154">เมื่อมีการใช้เท็มเพลตเริ่มต้น คีย์รวมจะถูกนำเข้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="dd964-154">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="dd964-155">ปัญหานี้อาจเกิดขึ้นเมื่อมีการเพิ่มงานใหม่ไปยังเท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="dd964-155">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="dd964-156">ถ้าฉันมีนิติบุคคลซึ่งเป็นพนักงานที่มีการจ้างงานจำนวน N ราย ฉันต้องสร้างการแม็ปสำหรับแต่ละคนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="dd964-156">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="dd964-157">ใช่ สำหรับแต่ละนิติบุคคลใน Finance คุณจำเป็นต้องมีโครงการรวมที่แยกต่างหากในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dd964-157">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="dd964-158">ฉันต้องการถ่ายโอนข้อมูลที่ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้นที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="dd964-158">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="dd964-159">ฉันสามารถทำได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="dd964-159">Can I do this?</span></span>

<span data-ttu-id="dd964-160">ได้ คุณสามารถเพิ่มหรือลบฟิลด์ออกจากเท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="dd964-160">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="dd964-161">คุณสามารถปรับเปลี่ยนเท็มเพลตเพื่อรวมข้อมูลเพิ่มเติมจาก Common Data Service อื่น ๆ สำหรับเอนทิตีแอป</span><span class="sxs-lookup"><span data-stu-id="dd964-161">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="dd964-162">เอนทิตีต้องอยู่ใน Common Data Service สำหรับแอปเพื่อให้รวมอยู่ในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="dd964-162">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="dd964-163">ฉันเพิ่งสร้างสภาพแวดล้อม Finance และ Talent ใหม่ และฉันได้รับข้อผิดพลาด "ค่าข้อมูลละเมิดข้อจำกัดความถูกต้อง"</span><span class="sxs-lookup"><span data-stu-id="dd964-163">I just created new Finance and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="dd964-164">เพราะเหตุใด?</span><span class="sxs-lookup"><span data-stu-id="dd964-164">Why?</span></span>

<span data-ttu-id="dd964-165">สาเหตุของข้อผิดพลาดนี้อาจรวม:</span><span class="sxs-lookup"><span data-stu-id="dd964-165">Reasons for this error can include:</span></span>

- <span data-ttu-id="dd964-166">การโอนย้ายข้อมูลที่เป็นผลลัพธ์ในเรกคอร์ดที่ซ้ำกันในการแยกข้อมูลลที่ต้นทาง (Common Data Service)</span><span class="sxs-lookup"><span data-stu-id="dd964-166">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="dd964-167">การโอนย้ายข้อมูลมีค่า null สำหรับฟิลด์ที่จำเป็นใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dd964-167">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="dd964-168">ตรวจสอบข้อมูลที่อยู่ใน Common Data Service และตรงตามข้อกำหนดของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dd964-168">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="dd964-169">ถ้ามีข้อผิดพลาดการดำเนินการ และรหัสพนักงานยังไม่ได้ซิงค์ ฉันจะค้นหาประวัติงานที่มีเรกคอร์ดพนักงานที่ล้มเหลวได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="dd964-169">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="dd964-170">ตัวรวมข้อมูลจะสร้างหลายโครงการใน Finance</span><span class="sxs-lookup"><span data-stu-id="dd964-170">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="dd964-171">ความสัมพันธ์ระหว่างงานตัวรวมข้อมูลและโครงการ Finance คือหนึ่งต่อหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dd964-171">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="dd964-172">ติดตามเวลาจากประวัติการดำเนินการตัวรวมข้อมูลและค้นหาโครงการดัชนี -1 ใน Finance</span><span class="sxs-lookup"><span data-stu-id="dd964-172">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="dd964-173">ถ้าหมายเลขงานคือ 9 ในตัวรวมข้อมูล ดัชนีใน Finance คือ 8</span><span class="sxs-lookup"><span data-stu-id="dd964-173">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="dd964-174">จัดดัชนีงานจากตัวรวมข้อมูล (ในตัวอย่างนี้คือ "9")</span><span class="sxs-lookup"><span data-stu-id="dd964-174">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![จับดัชนีงานจากตัวรวมข้อมูล](media/CaptureTaskIndex.png)

2. <span data-ttu-id="dd964-176">ติดตามเวลาการดำเนินการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="dd964-176">Track the execution time of the project.</span></span>

![ติดตามเวลาการดำเนินการของโครงการ](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="dd964-178">ใน Finance ให้ระบุดัชนี - 1</span><span class="sxs-lookup"><span data-stu-id="dd964-178">In Finance, identify index - 1.</span></span> <span data-ttu-id="dd964-179">ในตัวอย่างนี้ โครงการที่มีคำเสริมท้ายเป็น "8" และเวลาการดำเนินการของดัชนีเป็น "0" โครงการจะสอดคล้องกับเวลาการดำเนินการในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="dd964-179">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![ระบุดัชนี](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a><span data-ttu-id="dd964-181">หลังจากการรวม Talent และ Finance ฉันไม่เห็นข้อมูล Talent ของฉันใน Finance</span><span class="sxs-lookup"><span data-stu-id="dd964-181">After integrating Talent and Finance, I don’t see my Talent data in Finance.</span></span> <span data-ttu-id="dd964-182">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="dd964-182">What do I do?</span></span>

<span data-ttu-id="dd964-183">การรวมกับ Finance มีสองขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="dd964-183">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="dd964-184">ก่อนอื่น ตรวจสอบว่ ข้อมูล Talent ถูกปรับปรุงแล้ว และพร้อมใช้งานใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dd964-184">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="dd964-185">นี่เป็นการซิงค์แบบเรียลไทม์แบบใกล้ และสามารถตรวจสอบใน PowerApps โดยดูข้อมูลภายในเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dd964-185">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![ข้อมูลใน Common Data Service](media/DataInCDS.png)

<span data-ttu-id="dd964-187">ถ้าข้อมูลไม่ปรากฏตามที่คาดไว้ใน Common Data Service ให้ตรวจสอบว่าเอนทิตีได้รับการสนับสนุนในการรวม</span><span class="sxs-lookup"><span data-stu-id="dd964-187">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="dd964-188">เพื่อรวมข้อมูลเพิ่มเติมใน Common Data Service จะต้องทำการเปลี่ยนแปลงทางฝั่ง Microsoft</span><span class="sxs-lookup"><span data-stu-id="dd964-188">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="dd964-189">ถ้าเอนทิตีได้รับการสนับสนุน และข้อมูลมีอยู่ใน Common Data Service ให้ตรวจสอบว่าการแม็ปถูกต้องในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dd964-189">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="dd964-190">ถ้าการค้นหาการแม็ปตัวรวมเป็นปกติ ให้ตรวจสอบมีการรันงานการจัดการข้อมูลเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="dd964-190">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="dd964-191">ข้อผิดพลาดอาจเกิดขึ้นในระหว่างการดำเนินการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="dd964-191">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="dd964-192">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการข้อมูล ดู [การจัดการข้อมูล](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)</span><span class="sxs-lookup"><span data-stu-id="dd964-192">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="dd964-193">ที่อยู่สำหรับพนักงานของฉันไม่ถูกต้อง หลังจากที่ฉันนำเข้าไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="dd964-193">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="dd964-194">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="dd964-194">What should I do?</span></span>

<span data-ttu-id="dd964-195">ลำดับหมายเลขสำหรับ **รหัสที่ตั้ง** ใช้รูปแบบเดียวกันในทั้ง Talent และ Finance</span><span class="sxs-lookup"><span data-stu-id="dd964-195">The number sequence for **Location ID** uses the same pattern in both Talent and Finance.</span></span> <span data-ttu-id="dd964-196">ลำดับหมายเลขต้องไม่ซ้ำกันทั้งสองด้าน เพื่อให้ไม่มีการชนกันของที่อยู่เมื่อรวมข้อมูลจาก Common Data Service ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dd964-196">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="dd964-197">ในระหว่างการใช้งานของ Talent ให้ตรวจสอบว่าลำดับหมายเลขไม่เหมือนกันใน Talent และ Finance</span><span class="sxs-lookup"><span data-stu-id="dd964-197">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance.</span></span> <span data-ttu-id="dd964-198">ตรวจสอบว่าลำดับหมายเลขทั้งหมดไม่เหมือนกันซึ่งอาจจะรักษาข้อมูลในทั้งสองระบบ</span><span class="sxs-lookup"><span data-stu-id="dd964-198">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="dd964-199">เมื่อสร้างชุดการเชื่อมต่อของฉัน ฉันไม่เห็นการเชื่อมต่อในรายการแบบหล่นลงของ Connection</span><span class="sxs-lookup"><span data-stu-id="dd964-199">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="dd964-200">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="dd964-200">What do I do?</span></span>

<span data-ttu-id="dd964-201">ตรวจสอบว่าขณะที่สร้างการเชื่อมต่อของคุณ คุณเลือก Dynamics 365 Finance และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dd964-201">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="dd964-202">เมื่อซิงค์การจ้างงาน ฉันได้รับข้อผิดพลาด "ไม่มี CompanyInfo_FK"หรือ "ไม่พบค่า '12/31/2154 11:59:59 pm' ในฟิลด์ 'วันที่สิ้นสุดการจ้างงาน' ในตารางที่เกี่ยวข้อง 'การจ้างงาน'" ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="dd964-202">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="dd964-203">ให้แน่ใจว่าคุณกำลังแม็ปกับนิติบุคคลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="dd964-203">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="dd964-204">การซิงค์นิติบุคคลไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น จึงคาดว่าแต่ละนิติบุคคลที่ปรากฏใน Talent และ Common Data Service มีอยู่ใน Finance เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="dd964-204">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="dd964-205">นอกจากนี้ ให้ตรวจสอบให้แน่ใจว่าคุณกำลังเลือกนิติบุคคลที่ถูกต้องสำหรับชุดการเชื่อมต่อที่มีการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="dd964-205">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="dd964-206">หลังจากการตั้งค่าโครงการของฉัน การแม็ปฟิลด์สำหรับ Finance จะกลายเป็นว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="dd964-206">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="dd964-207">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="dd964-207">What should I do?</span></span>

<span data-ttu-id="dd964-208">รีเฟรชเอนทิตีข้อมูลใน Finance โดยไปที่ **การจัดการข้อมูล \> พารามิเตอร์กรอบงาน \> การตั้งค่าเอนทิตี \> รีเฟรชรายการเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="dd964-208">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="dd964-209">ซึ่งควรใช้เวลาสองสามนาทีในการทำให้เสร็จสมบูรณ์ จากนั้นคุณควรเห็นแมปเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="dd964-209">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="dd964-210">ปัญหานี้เกิดขึ้นเมื่อมีการสร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="dd964-210">This issue occurs when new projects are created.</span></span>

![ไม่มีการแม็ปฟิลด์](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="dd964-212">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="dd964-212">Additional resources</span></span>

- <span data-ttu-id="dd964-213">ตัวรวมข้อมูล (DI):</span><span class="sxs-lookup"><span data-stu-id="dd964-213">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="dd964-214">รวมข้อมูลลงใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dd964-214">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="dd964-215">การจัดการข้อผิดพลาดตัวรวมข้อมูลและการแก้ไขปัญหาเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="dd964-215">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="dd964-216">การตอบสนองคำขอ DSR สำหรับล็อกที่ระบบสร้างขึ้นใน PowerApps Microsoft Flow และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dd964-216">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="dd964-217">การจัดการข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="dd964-217">Data Management:</span></span>

  - [<span data-ttu-id="dd964-218">การจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dd964-218">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
