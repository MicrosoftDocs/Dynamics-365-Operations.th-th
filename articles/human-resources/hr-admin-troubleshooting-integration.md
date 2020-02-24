---
title: การรวมกับคำถามที่พบบ่อยเกี่ยวกับ Finance
description: บทความนี้อธิบายว่าข้อมูลใดจะถูกซิงโครไนส์ในการรวม Human Resources และ Finance
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b9cfc0964a532cd32dda029419c892fa8ae55e02
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010699"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="7d961-103">การรวมกับคำถามที่พบบ่อยเกี่ยวกับ Finance</span><span class="sxs-lookup"><span data-stu-id="7d961-103">Integration with Finance FAQ</span></span>

<span data-ttu-id="7d961-104">หัวข้อนี้ตอบคำถามสำหรับคำถามทั่วไปที่เกี่ยวข้องเกี่ยวกับว่าข้อมูลใดจะถูกซิงโครไนส์เมื่อ Dynamics 365 Human Resources ถูกรวมกับ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="7d961-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="7d961-105">คือข้อมูลที่ซิงโครไนซ์ทั้งหมด หรือเพียงแค่เอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7d961-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="7d961-106">ชุดย่อยของข้อมูลจะมีการซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="7d961-106">A subset of the data is synchronized.</span></span> <span data-ttu-id="7d961-107">สำหรับรายการของเอนทิตีทั้งหมด ดูที่ [การรวมกับ Dynamics 365 Finance](hr-admin-integration-finance.md)</span><span class="sxs-lookup"><span data-stu-id="7d961-107">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a><span data-ttu-id="7d961-108">เพราะเหตุใดฉันจึงไม่เห็นข้อมูลใดๆ ที่มีการซิงค์กับ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7d961-108">Why don't I see any data synced to Common Data Service?</span></span>

<span data-ttu-id="7d961-109">โดยค่าเริ่มต้น การรวม Common Data Service จะถูกปิดใช้งานในสภาพแวดล้อมใหม่ที่ไม่มีข้อมูลสาธิตที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="7d961-109">By default, the Common Data Service integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="7d961-110">โดยค่าเริ่มต้น จะมีการเปิดใช้งานในสภาพแวดล้อมใหม่ซึ่งรวมถึงข้อมูลสาธิต และการซิงโครไนส์ข้อมูลจะเริ่มต้นขึ้นเมื่อมีการจัดเตรียมสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="7d961-110">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="7d961-111">หลังจากที่สภาพแวดล้อมของคุณพร้อมที่จะซิงค์ข้อมูลแล้ว คุณสามารถเปิดใช้งานการรวมได้</span><span class="sxs-lookup"><span data-stu-id="7d961-111">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="7d961-112">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกการรวม Common Data Service](hr-admin-integration-common-data-service.md)</span><span class="sxs-lookup"><span data-stu-id="7d961-112">For more information, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="7d961-113">ฉันสามารถสร้างการแม็ปใหม่โดยไม่ใช้เท็มเพลได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d961-113">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="7d961-114">เท็มเพลตเป็นจุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7d961-114">Templates are the starting point.</span></span> <span data-ttu-id="7d961-115">คุณสามารถสร้างเท็มเพลตของคุณเอง แต่จำเป็นต้องใช้เท็มเพลเสมอเมื่อสร้างโครงการการรวม</span><span class="sxs-lookup"><span data-stu-id="7d961-115">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="7d961-116">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวรวมข้อมูล (DI) เท็มเพลต และโครงการ ดูที่ [รวมข้อมูลลงใน Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="7d961-116">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="7d961-117">ฉันสามารถแม็ปมิติทางการเงินที่จะโอนย้ายระหว่าง Human Resources และ Finance ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d961-117">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="7d961-118">ในปัจจุบันมิติทางการเงินไม่ได้อยู่ใน Common Data Service สำหรับแอป และผลลัพธ์ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7d961-118">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="7d961-119">เอนทิตี้นี้มีการวางแผน แต่ไม่มีเส้นเวลาการนำออกใช้ที่พร้อมใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="7d961-119">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="7d961-120">สำหรับข้อมูลที่อยู่ใน Finance แต่ไม่มีอยู่ใน Human Resources ให้เชื่อมโยงสองระบบเข้าด้วยกันโดยใช้ **ตั้งค่าคอนฟิกลิงค์** ใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="7d961-120">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![แม็ปมิติทางการเงิน](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="7d961-122">ในบางครั้งเมื่อฉันนำเข้าพนักงาน รายการจะไปอยู่ที่พนักงานที่ไม่ได้ใช้งานใน Finance</span><span class="sxs-lookup"><span data-stu-id="7d961-122">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="7d961-123">เพราะเหตุใด?</span><span class="sxs-lookup"><span data-stu-id="7d961-123">Why?</span></span>

<span data-ttu-id="7d961-124">คุณอาจได้รับข้อผิดพลาดนี้ถ้าพนักงานไม่มีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่ใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="7d961-124">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="7d961-125">เมื่อต้องการแก้ไขปัญหานี้ ไปที่ **การจัดการบุคลากร \> พนักงาน \> ประวัติการจ้างงาน \> ตัวจัดการวันที่** และตรวจสอบว่ามีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d961-125">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="7d961-126">ถ้าฉันเลือกที่จะแม็ปเฉพาะชุดย่อยของฟิลด์ การเปลี่ยนแปลงของฟิลด์ที่ไม่ได้แม็ปจะทริกเกอร์การซิงค์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d961-126">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="7d961-127">ซิงค์ข้อมูลเป็นไปตามกำหนดการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7d961-127">Data sync follows the execution schedule.</span></span> <span data-ttu-id="7d961-128">การรวมจะเบิกสินค้าเรกคอร์ดถ้าฟิลด์ใดๆ ในเรกคอร์ดเปลี่ยนแปลง โดยไม่คำนึงถึงว่าฟิลด์ดังกล่าวเป็นส่วนหนึ่งของการแม็ปการรวม</span><span class="sxs-lookup"><span data-stu-id="7d961-128">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="7d961-129">ฉันจะส่งการเปลี่ยนแปลงของพนักงานที่ใช้งานอยู่เท่านั้น ไม่ใช่เรกคอร์ดที่สิ้นสุดการจ้างงานได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="7d961-129">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="7d961-130">ด้วยการใช้ "การสอบถามขั้นสูง" คุณสามารถกรองและปรับรูปร่างแหล่งข้อมูลก่อนที่จะส่งผ่านไปยังปลายทาง</span><span class="sxs-lookup"><span data-stu-id="7d961-130">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![การสอบถามขั้นสูงของผู้ปฏิบัติงานที่ใช้งานอยู่](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="7d961-132">ฉันสามารถระบุฟิลด์ที่จะส่งไปยัง Finance สำหรับเอนทิตีที่เฉพาะเจาะจงได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d961-132">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="7d961-133">คุณสามารถเพิ่มหรือลบฟิลด์ออกจากงานรวม</span><span class="sxs-lookup"><span data-stu-id="7d961-133">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="7d961-134">ไม่ใช่ฟิลด์ข้อมูลทั้งหมดที่มีอยู่ในเอนทิตี Common Data Service ที่จะถูกเติมข้อมูลจาก Human Resources</span><span class="sxs-lookup"><span data-stu-id="7d961-134">Not all data fields that exist on the Common Data Service entity will be populated from Human Resources.</span></span>
<span data-ttu-id="7d961-135">คุณสามารถเติมข้อมูลเพิ่มเติมได้ผ่าน Power Apps</span><span class="sxs-lookup"><span data-stu-id="7d961-135">Additional data can be populated via Power Apps.</span></span>

![เพิ่มหรือลบฟิลด์ไปยังและออกจากงานการรวม](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="7d961-137">ฉันตั้งค่าการรวมเป็นชุดงาน แต่ Human Resources สูญเสียการเชื่อมต่อไปกับระบบปลายทาง</span><span class="sxs-lookup"><span data-stu-id="7d961-137">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="7d961-138">ฉันจะส่งชุดการเปลี่ยนแปลงเดียวกันไปยังระบบปลายทางได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="7d961-138">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="7d961-139">ไม่จำเป็นต้องมีการตั้งค่าพิเศษสำหรับการจัดการข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="7d961-139">No special setup is required for exception handling.</span></span> <span data-ttu-id="7d961-140">ตัวรวมข้อมูลจะตรวจจับและรายงานข้อผิดพลาดที่เกิดขึ้นที่ต้นทางและปลายทางโดยอัตโนมัติ และจะอนุญาตให้ลองใหม่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="7d961-140">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="7d961-141">อย่างไรก็ตาม คุณไม่สามารถแก้ไขข้อมูลด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="7d961-141">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="7d961-142">ถ้าจำเป็นต้องปรับปรุงข้อมูล ควรทำที่ต้นทางหรือปลายทางอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7d961-142">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="7d961-143">ฉันสามารถตั้งค่าการรวมสองทิศทางได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d961-143">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="7d961-144">ไม่ใช่ การรวมในปัจจุบันเป็นทางเดียว (Human Resources ไปยัง Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="7d961-144">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="7d961-145">อย่างไรก็ตาม มีเท็มเพลตเริ่มต้นที่มีอยู่เพื่อส่งข้อมูลจาก Human Resources ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="7d961-145">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="7d961-146">ฉันจะอนุญาตให้ลบเรกคอร์ดโดยเป็นส่วนหนึ่งของการรวมของฉันได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d961-146">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="7d961-147">ไม่ได้ ตัวรวมข้อมูลจะไม่รวบรวมเรกคอร์ดที่ถูกลบสำหรับการโอนย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7d961-147">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="7d961-148">มีเฉพาะการสร้างข้อมูลและการปรับปรุง (UPSERT) ถูกรวมอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="7d961-148">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="7d961-149">ฉันสามารถเรียกใช้การดำเนินการที่มีข้อผิดพลาดได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d961-149">Can I rerun the errored execution?</span></span> <span data-ttu-id="7d961-150">ถ้าเป็นเช่นนั้น จะส่งไฟล์ทั้งหมดหรือเฉพาะที่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="7d961-150">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="7d961-151">การเรียกใช้ครั้งแรกของตัวรวมข้อมูลจะรันแบบเต็มเสมอ</span><span class="sxs-lookup"><span data-stu-id="7d961-151">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="7d961-152">การเรียกใช้ในเวลาต่อมาขึ้นอยู่กับการติดตามการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="7d961-152">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="7d961-153">เมื่อดำเนินการการรันข้อผิดพลาด จะแยกเรกคอร์ดในขอบเขตของการรัน และส่งการเปลี่ยนแปลงล่าสุดจาก Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7d961-153">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="7d961-154">เมื่อฉันบันทึกโครงการ ฉันได้รับข้อผิดพลาด: "โครงการมีข้อผิดพลาดในการแม็ป"</span><span class="sxs-lookup"><span data-stu-id="7d961-154">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="7d961-155">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="7d961-155">What do I do?</span></span>

<span data-ttu-id="7d961-156">ตรวจสอบการตั้งค่าของคีย์รวมของคุณ ทำการเปลี่ยนแปลงที่จำเป็นเพื่อตั้งค่า แล้วรีเฟรชเอนทิตี้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="7d961-156">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="7d961-157">เมื่อมีการใช้เท็มเพลตเริ่มต้น คีย์รวมจะถูกนำเข้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7d961-157">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="7d961-158">ปัญหานี้อาจเกิดขึ้นเมื่อมีการเพิ่มงานใหม่ไปยังเท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="7d961-158">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="7d961-159">ถ้าฉันมีนิติบุคคลซึ่งเป็นพนักงานที่มีการจ้างงานจำนวน N ราย ฉันต้องสร้างการแม็ปสำหรับแต่ละคนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d961-159">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="7d961-160">ใช่ สำหรับแต่ละนิติบุคคลใน Finance คุณจำเป็นต้องมีโครงการรวมที่แยกต่างหากในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7d961-160">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="7d961-161">ฉันต้องการถ่ายโอนข้อมูลที่ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้นที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d961-161">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="7d961-162">ฉันสามารถทำได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7d961-162">Can I do this?</span></span>

<span data-ttu-id="7d961-163">ได้ คุณสามารถเพิ่มหรือลบฟิลด์ออกจากเท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="7d961-163">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="7d961-164">คุณสามารถปรับเปลี่ยนเท็มเพลตเพื่อรวมข้อมูลเพิ่มเติมจาก Common Data Service อื่น ๆ สำหรับเอนทิตีแอป</span><span class="sxs-lookup"><span data-stu-id="7d961-164">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="7d961-165">เอนทิตีต้องอยู่ใน Common Data Service สำหรับแอปเพื่อให้รวมอยู่ในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7d961-165">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="7d961-166">ฉันเพิ่งสร้างสภาพแวดล้อม Finance และ Human Resources ใหม่ และฉันได้รับข้อผิดพลาด "ค่าข้อมูลละเมิดข้อจำกัดความถูกต้อง"</span><span class="sxs-lookup"><span data-stu-id="7d961-166">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="7d961-167">เพราะเหตุใด?</span><span class="sxs-lookup"><span data-stu-id="7d961-167">Why?</span></span>

<span data-ttu-id="7d961-168">สาเหตุของข้อผิดพลาดนี้อาจรวม:</span><span class="sxs-lookup"><span data-stu-id="7d961-168">Reasons for this error can include:</span></span>

- <span data-ttu-id="7d961-169">การโอนย้ายข้อมูลที่เป็นผลลัพธ์ในเรกคอร์ดที่ซ้ำกันในการแยกข้อมูลลที่ต้นทาง (Common Data Service)</span><span class="sxs-lookup"><span data-stu-id="7d961-169">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="7d961-170">การโอนย้ายข้อมูลมีค่า null สำหรับฟิลด์ที่จำเป็นใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7d961-170">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="7d961-171">ตรวจสอบข้อมูลที่อยู่ใน Common Data Service และตรงตามข้อกำหนดของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7d961-171">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="7d961-172">ถ้ามีข้อผิดพลาดการดำเนินการ และรหัสพนักงานยังไม่ได้ซิงค์ ฉันจะค้นหาประวัติงานที่มีเรกคอร์ดพนักงานที่ล้มเหลวได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="7d961-172">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="7d961-173">ตัวรวมข้อมูลจะสร้างหลายโครงการใน Finance</span><span class="sxs-lookup"><span data-stu-id="7d961-173">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="7d961-174">ความสัมพันธ์ระหว่างงานตัวรวมข้อมูลและโครงการ Finance คือหนึ่งต่อหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7d961-174">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="7d961-175">ติดตามเวลาจากประวัติการดำเนินการตัวรวมข้อมูลและค้นหาโครงการดัชนี -1 ใน Finance</span><span class="sxs-lookup"><span data-stu-id="7d961-175">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="7d961-176">ถ้าหมายเลขงานคือ 9 ในตัวรวมข้อมูล ดัชนีใน Finance คือ 8</span><span class="sxs-lookup"><span data-stu-id="7d961-176">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="7d961-177">จัดดัชนีงานจากตัวรวมข้อมูล (ในตัวอย่างนี้คือ "9")</span><span class="sxs-lookup"><span data-stu-id="7d961-177">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![จับดัชนีงานจากตัวรวมข้อมูล](media/CaptureTaskIndex.png)

2. <span data-ttu-id="7d961-179">ติดตามเวลาการดำเนินการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="7d961-179">Track the execution time of the project.</span></span>

    ![ติดตามเวลาการดำเนินการของโครงการ](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="7d961-181">ใน Finance ให้ระบุดัชนี - 1</span><span class="sxs-lookup"><span data-stu-id="7d961-181">In Finance, identify index - 1.</span></span> <span data-ttu-id="7d961-182">ในตัวอย่างนี้ โครงการที่มีคำเสริมท้ายเป็น "8" และเวลาการดำเนินการของดัชนีเป็น "0" โครงการจะสอดคล้องกับเวลาการดำเนินการในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="7d961-182">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![ระบุดัชนี](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="7d961-184">หลังจากการรวม Human Resources และ Finance แล้ว ฉันไม่เห็นข้อมูล Human Resources ของฉันใน Finance</span><span class="sxs-lookup"><span data-stu-id="7d961-184">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="7d961-185">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="7d961-185">What do I do?</span></span>

<span data-ttu-id="7d961-186">การรวมกับ Finance มีสองขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="7d961-186">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="7d961-187">ก่อนอื่น ตรวจสอบว่าข้อมูล Human Resources ถูกปรับปรุงแล้ว และพร้อมใช้งานใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7d961-187">First, verify that the Human Resources data is updated and available in Common Data Service.</span></span> <span data-ttu-id="7d961-188">นี่เป็นการซิงค์แบบเรียลไทม์แบบใกล้ และสามารถตรวจสอบใน Power Apps โดยดูข้อมูลภายในเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7d961-188">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data entities.</span></span>

![ข้อมูลใน Common Data Service](media/DataInCDS.png)

<span data-ttu-id="7d961-190">ถ้าข้อมูลไม่ปรากฏตามที่คาดไว้ใน Common Data Service ให้ตรวจสอบว่าเอนทิตีได้รับการสนับสนุนในการรวม</span><span class="sxs-lookup"><span data-stu-id="7d961-190">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="7d961-191">เพื่อรวมข้อมูลเพิ่มเติมใน Common Data Service จะต้องทำการเปลี่ยนแปลงทางฝั่ง Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d961-191">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="7d961-192">ถ้าเอนทิตีได้รับการสนับสนุน และข้อมูลมีอยู่ใน Common Data Service ให้ตรวจสอบว่าการแม็ปถูกต้องในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7d961-192">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="7d961-193">ถ้าการค้นหาการแม็ปตัวรวมเป็นปกติ ให้ตรวจสอบมีการรันงานการจัดการข้อมูลเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="7d961-193">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="7d961-194">ข้อผิดพลาดอาจเกิดขึ้นในระหว่างการดำเนินการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="7d961-194">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="7d961-195">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการข้อมูล ดู [การจัดการข้อมูล](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)</span><span class="sxs-lookup"><span data-stu-id="7d961-195">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="7d961-196">ที่อยู่สำหรับพนักงานของฉันไม่ถูกต้อง หลังจากที่ฉันนำเข้าไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="7d961-196">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="7d961-197">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="7d961-197">What should I do?</span></span>

<span data-ttu-id="7d961-198">ลำดับหมายเลขสำหรับ **รหัสสถานที่** ใช้รูปแบบเดียวกันในทั้ง Human Resources และ Finance</span><span class="sxs-lookup"><span data-stu-id="7d961-198">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="7d961-199">ลำดับหมายเลขต้องไม่ซ้ำกันทั้งสองด้าน เพื่อให้ไม่มีการชนกันของที่อยู่เมื่อรวมข้อมูลจาก Common Data Service ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7d961-199">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="7d961-200">ในระหว่างการใช้งานของ Human Resources ให้ตรวจสอบว่าลำดับหมายเลขไม่เหมือนกันใน Human Resources และ Finance</span><span class="sxs-lookup"><span data-stu-id="7d961-200">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="7d961-201">ตรวจสอบว่าลำดับหมายเลขทั้งหมดไม่เหมือนกันซึ่งอาจจะรักษาข้อมูลในทั้งสองระบบ</span><span class="sxs-lookup"><span data-stu-id="7d961-201">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="7d961-202">เมื่อสร้างชุดการเชื่อมต่อของฉัน ฉันไม่เห็นการเชื่อมต่อในรายการแบบหล่นลงของ Connection</span><span class="sxs-lookup"><span data-stu-id="7d961-202">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="7d961-203">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="7d961-203">What do I do?</span></span>

<span data-ttu-id="7d961-204">ตรวจสอบว่าขณะที่สร้างการเชื่อมต่อของคุณ คุณเลือก Dynamics 365 Finance และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7d961-204">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="7d961-205">เมื่อซิงค์การจ้างงาน ฉันได้รับข้อผิดพลาด "ไม่มี CompanyInfo_FK"หรือ "ไม่พบค่า '12/31/2154 11:59:59 pm' ในฟิลด์ 'วันที่สิ้นสุดการจ้างงาน' ในตารางที่เกี่ยวข้อง 'การจ้างงาน'" ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="7d961-205">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="7d961-206">ให้แน่ใจว่าคุณกำลังแม็ปกับนิติบุคคลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7d961-206">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="7d961-207">การซิงค์นิติบุคคลไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น จึงคาดว่าแต่ละนิติบุคคลที่ปรากฏใน Human Resources และ Common Data Service มีอยู่ใน Finance เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="7d961-207">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="7d961-208">นอกจากนี้ ให้ตรวจสอบให้แน่ใจว่าคุณกำลังเลือกนิติบุคคลที่ถูกต้องสำหรับชุดการเชื่อมต่อที่มีการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="7d961-208">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="7d961-209">หลังจากการตั้งค่าโครงการของฉัน การแม็ปฟิลด์สำหรับ Finance จะกลายเป็นว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="7d961-209">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="7d961-210">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="7d961-210">What should I do?</span></span>

<span data-ttu-id="7d961-211">รีเฟรชเอนทิตีข้อมูลใน Finance โดยไปที่ **การจัดการข้อมูล \> พารามิเตอร์กรอบงาน \> การตั้งค่าเอนทิตี \> รีเฟรชรายการเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="7d961-211">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="7d961-212">ซึ่งควรใช้เวลาสองสามนาทีในการทำให้เสร็จสมบูรณ์ จากนั้นคุณควรเห็นแมปเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="7d961-212">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="7d961-213">ปัญหานี้เกิดขึ้นเมื่อมีการสร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="7d961-213">This issue occurs when new projects are created.</span></span>

![ไม่มีการแม็ปฟิลด์](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="7d961-215">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7d961-215">Additional resources</span></span>

- <span data-ttu-id="7d961-216">ตัวรวมข้อมูล (DI):</span><span class="sxs-lookup"><span data-stu-id="7d961-216">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="7d961-217">รวมข้อมูลลงใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7d961-217">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="7d961-218">การจัดการข้อผิดพลาดตัวรวมข้อมูลและการแก้ไขปัญหาเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="7d961-218">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="7d961-219">การตอบสนองคำขอ DSR สำหรับล็อกที่ระบบสร้างขึ้นใน Power Apps Microsoft Power Automate และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7d961-219">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="7d961-220">การจัดการข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="7d961-220">Data Management:</span></span>

  - [<span data-ttu-id="7d961-221">การจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7d961-221">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
