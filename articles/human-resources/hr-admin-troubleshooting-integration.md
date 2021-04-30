---
title: การรวมกับคำถามที่พบบ่อยเกี่ยวกับ Finance
description: บทความนี้อธิบายว่าข้อมูลใดจะถูกซิงโครไนส์ในการรวม Human Resources และ Finance
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a5befac6c72153332319eefc1aaeab30c33f4c69
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892262"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="6141f-103">การรวมกับคำถามที่พบบ่อยเกี่ยวกับ Finance</span><span class="sxs-lookup"><span data-stu-id="6141f-103">Integration with Finance FAQ</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6141f-104">หัวข้อนี้ตอบคำถามสำหรับคำถามทั่วไปที่เกี่ยวข้องเกี่ยวกับว่าข้อมูลใดจะถูกซิงโครไนส์เมื่อ Dynamics 365 Human Resources ถูกรวมกับ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="6141f-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a><span data-ttu-id="6141f-105">ฉันสามารถแก้ไขผู้ใช้แอปพลิเคชัน Dynamics 365 Talent ใน Power Apps ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-105">Can I edit the Dynamics 365 Talent application user in Power Apps?</span></span>

<span data-ttu-id="6141f-106">ลำดับที่</span><span class="sxs-lookup"><span data-stu-id="6141f-106">No.</span></span> <span data-ttu-id="6141f-107">ถ้าคุณแก้ไขผู้ใช้แอปพลิเคชัน Human Resources การรวมระหว่างทรัพยากรบุคคลและ Dataverse อาจล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="6141f-107">If you edit the Human Resources application user, the integration between Human Resources and Dataverse might fail.</span></span> <span data-ttu-id="6141f-108">ตารางต่อไปนี้จะแสดงการตั้งค่าเริ่มต้นสำหรับผู้ใช้แอปพลิเคชัน Talent</span><span class="sxs-lookup"><span data-stu-id="6141f-108">The following table shows the default settings for the Talent application user.</span></span>

| <span data-ttu-id="6141f-109">ชื่อเต็ม</span><span class="sxs-lookup"><span data-stu-id="6141f-109">Full Name</span></span> | <span data-ttu-id="6141f-110">รหัสแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="6141f-110">Application ID</span></span> | <span data-ttu-id="6141f-111">รหัสออบเจ็กต์ Azure AD</span><span class="sxs-lookup"><span data-stu-id="6141f-111">Azure AD Object ID</span></span> | <span data-ttu-id="6141f-112">URI รหัสแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="6141f-112">Application ID URI</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="6141f-113">Dynamics365 for Talent</span><span class="sxs-lookup"><span data-stu-id="6141f-113">Dynamics365 for Talent</span></span> | <span data-ttu-id="6141f-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="6141f-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> | <span data-ttu-id="6141f-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span><span class="sxs-lookup"><span data-stu-id="6141f-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span></span> | <span data-ttu-id="6141f-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="6141f-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> |

![การตั้งค่าเริ่มต้นสำหรับผู้ใช้แอปพลิเคชัน Talent](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="6141f-118">คือข้อมูลที่ซิงโครไนซ์ทั้งหมด หรือเพียงแค่เอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6141f-118">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="6141f-119">ชุดย่อยของข้อมูลจะมีการซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="6141f-119">A subset of the data is synchronized.</span></span> <span data-ttu-id="6141f-120">สำหรับรายการของเอนทิตีทั้งหมด ดูที่ [การรวมกับ Dynamics 365 Finance](hr-admin-integration-finance.md)</span><span class="sxs-lookup"><span data-stu-id="6141f-120">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a><span data-ttu-id="6141f-121">เพราะเหตุใดฉันจึงไม่เห็นข้อมูลใดๆ ที่มีการซิงค์กับ Dataverse</span><span class="sxs-lookup"><span data-stu-id="6141f-121">Why don't I see any data synced to Dataverse?</span></span>

<span data-ttu-id="6141f-122">โดยค่าเริ่มต้น การรวม Dataverse จะถูกปิดใช้งานในสภาพแวดล้อมใหม่ที่ไม่มีข้อมูลสาธิตที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="6141f-122">By default, the Dataverse integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="6141f-123">โดยค่าเริ่มต้น จะมีการเปิดใช้งานในสภาพแวดล้อมใหม่ซึ่งรวมถึงข้อมูลสาธิต และการซิงโครไนส์ข้อมูลจะเริ่มต้นขึ้นเมื่อมีการจัดเตรียมสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="6141f-123">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="6141f-124">หลังจากที่สภาพแวดล้อมของคุณพร้อมที่จะซิงค์ข้อมูลแล้ว คุณสามารถเปิดใช้งานการรวมได้</span><span class="sxs-lookup"><span data-stu-id="6141f-124">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="6141f-125">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกการรวม Dataverse](hr-admin-integration-common-data-service.md)</span><span class="sxs-lookup"><span data-stu-id="6141f-125">For more information, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="6141f-126">ฉันสามารถสร้างการแม็ปใหม่โดยไม่ใช้เท็มเพลได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-126">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="6141f-127">เท็มเพลตเป็นจุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6141f-127">Templates are the starting point.</span></span> <span data-ttu-id="6141f-128">คุณสามารถสร้างเท็มเพลตของคุณเอง แต่จำเป็นต้องใช้เท็มเพลเสมอเมื่อสร้างโครงการการรวม</span><span class="sxs-lookup"><span data-stu-id="6141f-128">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="6141f-129">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวรวมข้อมูล (DI) เท็มเพลต และโครงการ ดูที่ [รวมข้อมูลลงใน Microsoft Dataverse](/powerapps/administrator/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="6141f-129">For more information about data integrator (DI), templates, and projects, see [Integrate data into Microsoft Dataverse](/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="6141f-130">ฉันสามารถแม็ปมิติทางการเงินที่จะโอนย้ายระหว่าง Human Resources และ Finance ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-130">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="6141f-131">ในปัจจุบันมิติทางการเงินไม่ได้อยู่ใน Dataverse สำหรับแอป และผลลัพธ์ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6141f-131">Financial dimensions aren’t currently in Dataverse and as a result aren’t part of the default template.</span></span> <span data-ttu-id="6141f-132">เอนทิตี้นี้มีการวางแผน แต่ไม่มีเส้นเวลาการนำออกใช้ที่พร้อมใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="6141f-132">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="6141f-133">สำหรับข้อมูลที่อยู่ใน Finance แต่ไม่มีอยู่ใน Human Resources ให้เชื่อมโยงสองระบบเข้าด้วยกันโดยใช้ **ตั้งค่าคอนฟิกลิงค์** ใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="6141f-133">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![แม็ปมิติทางการเงิน](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="6141f-135">ในบางครั้งเมื่อฉันนำเข้าพนักงาน รายการจะไปอยู่ที่พนักงานที่ไม่ได้ใช้งานใน Finance</span><span class="sxs-lookup"><span data-stu-id="6141f-135">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="6141f-136">เพราะเหตุใด?</span><span class="sxs-lookup"><span data-stu-id="6141f-136">Why?</span></span>

<span data-ttu-id="6141f-137">คุณอาจได้รับข้อผิดพลาดนี้ถ้าพนักงานไม่มีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่ใน Human Resources</span><span class="sxs-lookup"><span data-stu-id="6141f-137">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="6141f-138">เมื่อต้องการแก้ไขปัญหานี้ ไปที่ **การจัดการบุคลากร \> พนักงาน \> ประวัติการจ้างงาน \> ตัวจัดการวันที่** และตรวจสอบว่ามีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-138">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="6141f-139">ถ้าฉันเลือกที่จะแม็ปเฉพาะชุดย่อยของฟิลด์ การเปลี่ยนแปลงของฟิลด์ที่ไม่ได้แม็ปจะทริกเกอร์การซิงค์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-139">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="6141f-140">ซิงค์ข้อมูลเป็นไปตามกำหนดการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="6141f-140">Data sync follows the execution schedule.</span></span> <span data-ttu-id="6141f-141">การรวมจะเบิกสินค้าเรกคอร์ดถ้าฟิลด์ใดๆ ในเรกคอร์ดเปลี่ยนแปลง โดยไม่คำนึงถึงว่าฟิลด์ดังกล่าวเป็นส่วนหนึ่งของการแม็ปการรวม</span><span class="sxs-lookup"><span data-stu-id="6141f-141">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="6141f-142">ฉันจะส่งการเปลี่ยนแปลงของพนักงานที่ใช้งานอยู่เท่านั้น ไม่ใช่เรกคอร์ดที่สิ้นสุดการจ้างงานได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="6141f-142">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="6141f-143">ด้วยการใช้ "การสอบถามขั้นสูง" คุณสามารถกรองและปรับรูปร่างแหล่งข้อมูลก่อนที่จะส่งผ่านไปยังปลายทาง</span><span class="sxs-lookup"><span data-stu-id="6141f-143">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![การสอบถามขั้นสูงของผู้ปฏิบัติงานที่ใช้งานอยู่](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="6141f-145">ฉันสามารถระบุฟิลด์ที่จะส่งไปยัง Finance สำหรับเอนทิตีที่เฉพาะเจาะจงได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-145">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="6141f-146">คุณสามารถเพิ่มหรือลบฟิลด์ออกจากงานรวม</span><span class="sxs-lookup"><span data-stu-id="6141f-146">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="6141f-147">ไม่ใช่ฟิลด์ข้อมูลทั้งหมดที่มีอยู่ในตาราง Dataverse ที่จะถูกเติมข้อมูลจาก Human Resources</span><span class="sxs-lookup"><span data-stu-id="6141f-147">Not all data fields that exist on the Dataverse table will be populated from Human Resources.</span></span>
<span data-ttu-id="6141f-148">คุณสามารถเติมข้อมูลเพิ่มเติมได้ผ่าน Power Apps</span><span class="sxs-lookup"><span data-stu-id="6141f-148">Additional data can be populated via Power Apps.</span></span>

![เพิ่มหรือลบฟิลด์ไปยังและออกจากงานการรวม](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="6141f-150">ฉันตั้งค่าการรวมเป็นชุดงาน แต่ Human Resources สูญเสียการเชื่อมต่อไปกับระบบปลายทาง</span><span class="sxs-lookup"><span data-stu-id="6141f-150">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="6141f-151">ฉันจะส่งชุดการเปลี่ยนแปลงเดียวกันไปยังระบบปลายทางได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="6141f-151">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="6141f-152">ไม่จำเป็นต้องมีการตั้งค่าพิเศษสำหรับการจัดการข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="6141f-152">No special setup is required for exception handling.</span></span> <span data-ttu-id="6141f-153">ตัวรวมข้อมูลจะตรวจจับและรายงานข้อผิดพลาดที่เกิดขึ้นที่ต้นทางและปลายทางโดยอัตโนมัติ และจะอนุญาตให้ลองใหม่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="6141f-153">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="6141f-154">อย่างไรก็ตาม คุณไม่สามารถแก้ไขข้อมูลด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="6141f-154">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="6141f-155">ถ้าจำเป็นต้องปรับปรุงข้อมูล ควรทำที่ต้นทางหรือปลายทางอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6141f-155">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="6141f-156">ฉันสามารถตั้งค่าการรวมสองทิศทางได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-156">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="6141f-157">ไม่ใช่ การรวมในปัจจุบันเป็นทางเดียว (Human Resources ไปยัง Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="6141f-157">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="6141f-158">อย่างไรก็ตาม มีเท็มเพลตเริ่มต้นที่มีอยู่เพื่อส่งข้อมูลจาก Human Resources ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="6141f-158">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="6141f-159">ฉันจะอนุญาตให้ลบเรกคอร์ดโดยเป็นส่วนหนึ่งของการรวมของฉันได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-159">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="6141f-160">ไม่ได้ ตัวรวมข้อมูลจะไม่รวบรวมเรกคอร์ดที่ถูกลบสำหรับการโอนย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6141f-160">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="6141f-161">มีเฉพาะการสร้างข้อมูลและการปรับปรุง (UPSERT) ถูกรวมอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="6141f-161">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="6141f-162">ฉันสามารถเรียกใช้การดำเนินการที่มีข้อผิดพลาดได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-162">Can I rerun the errored execution?</span></span> <span data-ttu-id="6141f-163">ถ้าเป็นเช่นนั้น จะส่งไฟล์ทั้งหมดหรือเฉพาะที่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="6141f-163">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="6141f-164">การเรียกใช้ครั้งแรกของตัวรวมข้อมูลจะรันแบบเต็มเสมอ</span><span class="sxs-lookup"><span data-stu-id="6141f-164">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="6141f-165">การเรียกใช้ในเวลาต่อมาขึ้นอยู่กับการติดตามการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="6141f-165">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="6141f-166">เมื่อดำเนินการการรันข้อผิดพลาด จะแยกเรกคอร์ดในขอบเขตของการรัน และส่งการเปลี่ยนแปลงล่าสุดจาก Dataverse</span><span class="sxs-lookup"><span data-stu-id="6141f-166">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Dataverse.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="6141f-167">เมื่อฉันบันทึกโครงการ ฉันได้รับข้อผิดพลาด: "โครงการมีข้อผิดพลาดในการแม็ป"</span><span class="sxs-lookup"><span data-stu-id="6141f-167">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="6141f-168">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="6141f-168">What do I do?</span></span>

<span data-ttu-id="6141f-169">ตรวจสอบการตั้งค่าของคีย์รวมของคุณ ทำการเปลี่ยนแปลงที่จำเป็นเพื่อตั้งค่า แล้วรีเฟรชเอนทิตี้ในโครงการ</span><span class="sxs-lookup"><span data-stu-id="6141f-169">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="6141f-170">เมื่อมีการใช้เท็มเพลตเริ่มต้น คีย์รวมจะถูกนำเข้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6141f-170">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="6141f-171">ปัญหานี้อาจเกิดขึ้นเมื่อมีการเพิ่มงานใหม่ไปยังเท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="6141f-171">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="6141f-172">ถ้าฉันมีนิติบุคคลซึ่งเป็นพนักงานที่มีการจ้างงานจำนวน N ราย ฉันต้องสร้างการแม็ปสำหรับแต่ละคนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-172">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="6141f-173">ใช่ สำหรับแต่ละนิติบุคคลใน Finance คุณจำเป็นต้องมีโครงการรวมที่แยกต่างหากในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6141f-173">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="6141f-174">ฉันต้องการถ่ายโอนข้อมูลที่ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้นที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="6141f-174">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="6141f-175">ฉันสามารถทำได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6141f-175">Can I do this?</span></span>

<span data-ttu-id="6141f-176">ได้ คุณสามารถเพิ่มหรือลบฟิลด์ออกจากเท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="6141f-176">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="6141f-177">คุณสามารถปรับเปลี่ยนแม่แบบเพื่อรวมข้อมูลเพิ่มเติมจากตาราง Dataverse อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="6141f-177">The template can be modified to include additional data from other Dataverse tables.</span></span> <span data-ttu-id="6141f-178">เอนทิตีต้องอยู่ใน Dataverse สำหรับแอปเพื่อให้รวมอยู่ในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="6141f-178">The entity must be in Dataverse for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="6141f-179">ฉันเพิ่งสร้างสภาพแวดล้อม Finance และ Human Resources ใหม่ และฉันได้รับข้อผิดพลาด "ค่าข้อมูลละเมิดข้อจำกัดความถูกต้อง"</span><span class="sxs-lookup"><span data-stu-id="6141f-179">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="6141f-180">เพราะเหตุใด?</span><span class="sxs-lookup"><span data-stu-id="6141f-180">Why?</span></span>

<span data-ttu-id="6141f-181">สาเหตุของข้อผิดพลาดนี้อาจรวม:</span><span class="sxs-lookup"><span data-stu-id="6141f-181">Reasons for this error can include:</span></span>

- <span data-ttu-id="6141f-182">การโอนย้ายข้อมูลที่เป็นผลลัพธ์ในเรกคอร์ดที่ซ้ำกันในการแยกข้อมูลลที่ต้นทาง (Dataverse)</span><span class="sxs-lookup"><span data-stu-id="6141f-182">The data transfer resulted in duplicate records extraction at the source (Dataverse).</span></span>

- <span data-ttu-id="6141f-183">การโอนย้ายข้อมูลมีค่า null สำหรับฟิลด์ที่จำเป็นใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6141f-183">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="6141f-184">ตรวจสอบข้อมูลที่อยู่ใน Dataverse และตรงตามข้อกำหนดของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6141f-184">Verify the data that is in Dataverse and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="6141f-185">ถ้ามีข้อผิดพลาดการดำเนินการ และรหัสพนักงานยังไม่ได้ซิงค์ ฉันจะค้นหาประวัติงานที่มีเรกคอร์ดพนักงานที่ล้มเหลวได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="6141f-185">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="6141f-186">ตัวรวมข้อมูลจะสร้างหลายโครงการใน Finance</span><span class="sxs-lookup"><span data-stu-id="6141f-186">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="6141f-187">ความสัมพันธ์ระหว่างงานตัวรวมข้อมูลและโครงการ Finance คือหนึ่งต่อหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6141f-187">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="6141f-188">ติดตามเวลาจากประวัติการดำเนินการตัวรวมข้อมูลและค้นหาโครงการดัชนี -1 ใน Finance</span><span class="sxs-lookup"><span data-stu-id="6141f-188">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="6141f-189">ถ้าหมายเลขงานคือ 9 ในตัวรวมข้อมูล ดัชนีใน Finance คือ 8</span><span class="sxs-lookup"><span data-stu-id="6141f-189">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="6141f-190">จัดดัชนีงานจากตัวรวมข้อมูล (ในตัวอย่างนี้คือ "9")</span><span class="sxs-lookup"><span data-stu-id="6141f-190">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![จับดัชนีงานจากตัวรวมข้อมูล](media/CaptureTaskIndex.png)

2. <span data-ttu-id="6141f-192">ติดตามเวลาการดำเนินการของโครงการ</span><span class="sxs-lookup"><span data-stu-id="6141f-192">Track the execution time of the project.</span></span>

    ![ติดตามเวลาการดำเนินการของโครงการ](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="6141f-194">ใน Finance ให้ระบุดัชนี - 1</span><span class="sxs-lookup"><span data-stu-id="6141f-194">In Finance, identify index - 1.</span></span> <span data-ttu-id="6141f-195">ในตัวอย่างนี้ โครงการที่มีคำเสริมท้ายเป็น "8" และเวลาการดำเนินการของดัชนีเป็น "0" โครงการจะสอดคล้องกับเวลาการดำเนินการในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="6141f-195">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![ระบุดัชนี](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="6141f-197">หลังจากการรวม Human Resources และ Finance แล้ว ฉันไม่เห็นข้อมูล Human Resources ของฉันใน Finance</span><span class="sxs-lookup"><span data-stu-id="6141f-197">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="6141f-198">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="6141f-198">What do I do?</span></span>

<span data-ttu-id="6141f-199">การรวมกับ Finance มีสองขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="6141f-199">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="6141f-200">ก่อนอื่น ตรวจสอบว่าข้อมูล Human Resources ถูกปรับปรุงแล้ว และพร้อมใช้งานใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="6141f-200">First, verify that the Human Resources data is updated and available in Dataverse.</span></span> <span data-ttu-id="6141f-201">นี่เป็นการซิงค์แบบเรียลไทม์แบบใกล้ และสามารถตรวจสอบใน Power Apps โดยดูข้อมูลภายในตารางข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6141f-201">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data tables.</span></span>

![ข้อมูลใน Dataverse](media/DataInCDS.png)

<span data-ttu-id="6141f-203">ถ้าข้อมูลไม่ปรากฏตามที่คาดไว้ใน Dataverse ให้ตรวจสอบว่าเอนทิตีได้รับการสนับสนุนในการรวม</span><span class="sxs-lookup"><span data-stu-id="6141f-203">If the data is not appearing as expected in Dataverse, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="6141f-204">เพื่อรวมข้อมูลเพิ่มเติมใน Dataverse จะต้องทำการเปลี่ยนแปลงทางฝั่ง Microsoft</span><span class="sxs-lookup"><span data-stu-id="6141f-204">To include additional data in Dataverse, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="6141f-205">ถ้าเอนทิตีได้รับการสนับสนุน และข้อมูลมีอยู่ใน Dataverse ให้ตรวจสอบว่าการแม็ปถูกต้องในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6141f-205">If the entity is supported and the data is available in Dataverse, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="6141f-206">ถ้าการค้นหาการแม็ปตัวรวมเป็นปกติ ให้ตรวจสอบมีการรันงานการจัดการข้อมูลเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="6141f-206">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="6141f-207">ข้อผิดพลาดอาจเกิดขึ้นในระหว่างการดำเนินการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="6141f-207">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="6141f-208">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการข้อมูล ดู [การจัดการข้อมูล](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="6141f-208">For more information about Data Management, see [Data management](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="6141f-209">ที่อยู่สำหรับพนักงานของฉันไม่ถูกต้อง หลังจากที่ฉันนำเข้าไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="6141f-209">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="6141f-210">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="6141f-210">What should I do?</span></span>

<span data-ttu-id="6141f-211">ลำดับหมายเลขสำหรับ **รหัสสถานที่** ใช้รูปแบบเดียวกันในทั้ง Human Resources และ Finance</span><span class="sxs-lookup"><span data-stu-id="6141f-211">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="6141f-212">ลำดับหมายเลขต้องไม่ซ้ำกันทั้งสองด้าน เพื่อให้ไม่มีการชนกันของที่อยู่เมื่อรวมข้อมูลจาก Dataverse ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6141f-212">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Dataverse to Finance and Operations.</span></span>

<span data-ttu-id="6141f-213">ในระหว่างการใช้งานของ Human Resources ให้ตรวจสอบว่าลำดับหมายเลขไม่เหมือนกันใน Human Resources และ Finance</span><span class="sxs-lookup"><span data-stu-id="6141f-213">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="6141f-214">ตรวจสอบว่าลำดับหมายเลขทั้งหมดไม่เหมือนกันซึ่งอาจจะรักษาข้อมูลในทั้งสองระบบ</span><span class="sxs-lookup"><span data-stu-id="6141f-214">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="6141f-215">เมื่อสร้างชุดการเชื่อมต่อของฉัน ฉันไม่เห็นการเชื่อมต่อในรายการแบบหล่นลงของ Connection</span><span class="sxs-lookup"><span data-stu-id="6141f-215">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="6141f-216">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="6141f-216">What do I do?</span></span>

<span data-ttu-id="6141f-217">ตรวจสอบว่าขณะที่สร้างการเชื่อมต่อของคุณ คุณเลือก Dynamics 365 Finance และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="6141f-217">Make sure when creating your connections, you choose Dynamics 365 Finance and Dataverse.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="6141f-218">เมื่อซิงค์การจ้างงาน ฉันได้รับข้อผิดพลาด "ไม่มี CompanyInfo_FK"หรือ "ไม่พบค่า '12/31/2154 11:59:59 pm' ในฟิลด์ 'วันที่สิ้นสุดการจ้างงาน' ในตารางที่เกี่ยวข้อง 'การจ้างงาน'" ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="6141f-218">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="6141f-219">ให้แน่ใจว่าคุณกำลังแม็ปกับนิติบุคคลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6141f-219">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="6141f-220">การซิงค์นิติบุคคลไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น จึงคาดว่าแต่ละนิติบุคคลที่ปรากฏใน Human Resources และ Dataverse มีอยู่ใน Finance เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="6141f-220">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Dataverse is also present in Finance.</span></span>
<span data-ttu-id="6141f-221">นอกจากนี้ ให้ตรวจสอบให้แน่ใจว่าคุณกำลังเลือกนิติบุคคลที่ถูกต้องสำหรับชุดการเชื่อมต่อที่มีการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="6141f-221">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="6141f-222">หลังจากการตั้งค่าโครงการของฉัน การแม็ปฟิลด์สำหรับ Finance จะกลายเป็นว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6141f-222">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="6141f-223">ฉันควรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="6141f-223">What should I do?</span></span>

<span data-ttu-id="6141f-224">รีเฟรชเอนทิตีข้อมูลใน Finance โดยไปที่ **การจัดการข้อมูล \> พารามิเตอร์กรอบงาน \> การตั้งค่าเอนทิตี \> รีเฟรชรายการเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="6141f-224">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="6141f-225">ซึ่งควรใช้เวลาสองสามนาทีในการทำให้เสร็จสมบูรณ์ จากนั้นคุณควรเห็นแมปเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="6141f-225">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="6141f-226">ปัญหานี้เกิดขึ้นเมื่อมีการสร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="6141f-226">This issue occurs when new projects are created.</span></span>

![ไม่มีการแม็ปฟิลด์](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="6141f-228">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6141f-228">Additional resources</span></span>

- <span data-ttu-id="6141f-229">ตัวรวมข้อมูล (DI):</span><span class="sxs-lookup"><span data-stu-id="6141f-229">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="6141f-230">รวมข้อมูลลงใน Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="6141f-230">Integrate data into Microsoft Dataverse</span></span>](/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="6141f-231">การจัดการข้อผิดพลาดตัวรวมข้อมูลและการแก้ไขปัญหาเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6141f-231">Data Integrator error management and troubleshooting</span></span>](/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="6141f-232">การตอบสนองคำขอ DSR สำหรับล็อกที่ระบบสร้างขึ้นใน Power Apps Microsoft Power Automate และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="6141f-232">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Dataverse</span></span>](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="6141f-233">การจัดการข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="6141f-233">Data Management:</span></span>

  - [<span data-ttu-id="6141f-234">การจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6141f-234">Data management</span></span>](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]