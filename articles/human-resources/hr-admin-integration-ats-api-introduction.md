---
title: บทนํา API การรวมระบบการติดตามผู้สมัคร
description: 'หัวข้อนี้อธิบายระบบติดตามผู้สมัคร (ATS) Dynamics 365 Human Resources การรวม API '
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f70e377d6844b5c4f9201f0a561ad9cfcab2eda1
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890136"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="ba79f-103">บทนํา API การรวมระบบการติดตามผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="ba79f-103">Applicant Tracking System integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ba79f-104">หัวข้อนี้อธิบายระบบติดตามผู้สมัคร (ATS) Dynamics 365 Human Resources การรวม API </span><span class="sxs-lookup"><span data-stu-id="ba79f-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="ba79f-105">วัตถุประสงค์ของ API คือการเปิดใช้งานการรวมอย่างมีประสิทธิภาพระหว่าง Dynamics 365 Human Resources และการเป็นพันธมิตร ATS</span><span class="sxs-lookup"><span data-stu-id="ba79f-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ลำดับการรวม ATS](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="ba79f-107">ประสบการณ์แบบรวมจะเริ่มต้นในทรัพยากรบุคคลเมื่อผู้จัดการการว่าจ้างสร้างคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ba79f-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="ba79f-108">เมื่อคำขอถูกเปิดใช้งาน ATS จะดึงรายละเอียดสำหรับคำขอเพื่อสร้างโครงการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ba79f-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="ba79f-109">จากนั้นจะติดตามไปป์ไลน์การสรรหาบุคลากรเพื่อเลือกและจ้างผู้สมัครสำหรับตําแหน่งงานต่างๆ</span><span class="sxs-lookup"><span data-stu-id="ba79f-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="ba79f-110">ในขั้นตอนสุดท้าย ATS จะทำการรวมแบบไปกลับให้เสร็จสมบูรณ์โดยการส่งเรกคอร์ดของผู้สมัครที่เลือกไปยังฝ่ายทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="ba79f-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="ba79f-111">จากนั้นเรกคอร์ดผู้สมัครจะสามารถผ่านการตรวจสอบความถูกต้องและการจัดเรียงลำดับงานเพื่อสร้างเรกคอร์ดพนักงานได้</span><span class="sxs-lookup"><span data-stu-id="ba79f-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="ba79f-112">เมื่อต้องการเปิดใช้งานการรวม ทรัพยากรบุคคลได้เพิ่มส่วนประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba79f-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="ba79f-113">ฟังก์ชันในการสร้างคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ba79f-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="ba79f-114">โพรไฟล์ผู้สมัครที่ขยายและที่เกี่ยวข้องกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="ba79f-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="ba79f-115">API การรวมจะเปิดฟังก์ชันใหม่เพื่อรวมใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="ba79f-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="ba79f-116">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าและการใช้คำขอการสรรหาบุคลากรและฟังก์ชันผู้สมัคร โปรดดูที่ [สรรหาผู้สมัครงาน](hr-personnel-recruit.md)</span><span class="sxs-lookup"><span data-stu-id="ba79f-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="ba79f-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="ba79f-117">Microsoft Dataverse</span></span>

<span data-ttu-id="ba79f-118">API นี้จะสร้างขึ้นบน Microsoft Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service)</span><span class="sxs-lookup"><span data-stu-id="ba79f-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="ba79f-119">การโต้ตอบ RESTful ทั้งหมดกับ API นี้กระทำผ่าน Microsoft Dataverse Web API ที่ใช้ OData</span><span class="sxs-lookup"><span data-stu-id="ba79f-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="ba79f-120">API นี้เป็นเซ็ตย่อยของ Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="ba79f-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="ba79f-121">Dataverse Web API จะกําหนดลักษณะต่างๆ เช่น การพิสูจน์ตัวจริง SLAs ชุดงาน การควบคุมการเกิดพร้อมกัน และการจัดการข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="ba79f-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="ba79f-122">สำหรับข้อมูลเพิ่มเติมทั่วไปเกี่ยวกับ Microsoft Dataverse Web API ให้ดูที่</span><span class="sxs-lookup"><span data-stu-id="ba79f-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="ba79f-123">Microsoft Dataverse คืออะไร</span><span class="sxs-lookup"><span data-stu-id="ba79f-123">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="ba79f-124">ใช้ Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="ba79f-124">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="ba79f-125">Microsoft Dataverse คู่มือสำหรับนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="ba79f-125">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="ba79f-126">เอกสารข้างต้นจะประกอบด้วยรายละเอียดและแนวทางของนักพัฒนาในการใช้ Dataverse Web API เช่น [การจัดการการพิสูจน์ตัวจริง](/powerapps/developer/data-platform/webapi/authenticate-web-api) [การดำเนินงาน](/powerapps/developer/data-platform/webapi/perform-operations-web-api) [การใช้บุรุษไปรษณีย์กับ API](/powerapps/developer/data-platform/webapi/use-postman-web-api) และ [การใช้การเปลี่ยนแปลงการติดตามหรือโทเคนที่ว่างเปล่า](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) กับ the API</span><span class="sxs-lookup"><span data-stu-id="ba79f-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="ba79f-127">ชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ba79f-127">Option sets</span></span>

<span data-ttu-id="ba79f-128">แบบจำลองข้อมูลสำหรับการรวม ATS API อธิบายไว้ในเอกสารนี้รวมถึงชุดตัวเลือกที่ระบุค่าที่ระบุหมายเลขที่สัมพันธ์กับคุณสมบัติเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="ba79f-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="ba79f-129">สำหรับรายละเอียดเกี่ยวกับชุดตัวเลือกใน Dataverse Web API ให้ดูที่ [ชุดตัวเลือกการสร้างและการอัพเดตโดยใช้ Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets)</span><span class="sxs-lookup"><span data-stu-id="ba79f-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="ba79f-130">ชุดตัวเลือกถูกกําหนดไว้ให้กับ Dataverse แต่ละสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="ba79f-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="ba79f-131">ตารางเสมือนสำหรับทรัพยากรบุคคล Dataverse</span><span class="sxs-lookup"><span data-stu-id="ba79f-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="ba79f-132">ปลายทางสำหรับ API การรวม ATS ใช้ความสามารถของแพลตฟอร์มตารางเสมือนของ Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="ba79f-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="ba79f-133">โดยค่าเริ่มต้น ตารางเสมือนและปลายทาง API ที่เกี่ยวข้องจะไม่ปรับใช้กับสภาพแวดล้อมของทรัพยากรบุคคล การเปิดใช้งานองค์กรเพื่อระบุว่าปลายทาง OData ใดจะแสดงต่อสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="ba79f-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="ba79f-134">เมื่อต้องการใช้ API ตารางเสมือนของเอนทิตี้ทรัพยากรบุคคลจะต้องสร้างให้กับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="ba79f-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="ba79f-135">สำหรับข้อมูลเกี่ยวกับการสร้างตารางเสมือนของ API ให้ดูที่ [การตั้งค่าคอนฟิกตารางเสมือน Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="ba79f-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="ba79f-136">แบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ba79f-136">Data model</span></span>

<span data-ttu-id="ba79f-137">แบบจำลองข้อมูลมีศูนย์กลางอยู่ประมาณเอนทิตี้หลักสองเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="ba79f-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="ba79f-138">**RecruitingRequest** แสดงถึงคำขอของ ATS เพื่อสรรหาบุคลากรในตําแหน่งที่เปิดรับอย่างน้อยหนึ่งตําแหน่ง ตัวอย่างเช่นการสอบถาม ให้ดูที่ [ตัวอย่างการสอบถามสำหรับคำขอการสรรหาบุคคลากร](hr-admin-integration-ats-api-recruiting-request-example-query.md)</span><span class="sxs-lookup"><span data-stu-id="ba79f-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="ba79f-139">**CandidateToHire** แสดงถึงรายละเอียดของผู้สมัครที่ได้ยอมรับข้อเสนอในตําแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="ba79f-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="ba79f-140">**บุคคล** แสดงถึงบุคคลที่เป็นผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="ba79f-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="ba79f-141">บุคคลสามารถมีบทบาทในบริษัทได้หลายบทบาท เช่น ผู้สมัคร ผู้ปฏิบัติงาน พนักงาน หรือผู้รับเหมา</span><span class="sxs-lookup"><span data-stu-id="ba79f-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="ba79f-142">สำหรับตัวอย่างการสอบถาม ให้ดูที่ [ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)</span><span class="sxs-lookup"><span data-stu-id="ba79f-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="ba79f-143">แผนภาพต่อไปนี้แสดงความสัมพันธ์ภายใน API</span><span class="sxs-lookup"><span data-stu-id="ba79f-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="ba79f-144">หลายชนิดมีคีย์นอกไปยังเป็นเอนทิตี้ที่มีอยู่ก่อนอื่นๆในทรัพยากรบุคคลที่ไม่ได้แสดงที่นี่</span><span class="sxs-lookup"><span data-stu-id="ba79f-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="ba79f-145">เอกสารนี้แสดงข้อมูลเกี่ยวกับเอนทิตี้ที่เฉพาะเจาะจงให้กับสถานการณ์การรวมการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ba79f-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="ba79f-146">อย่างไรก็ตาม มีเอนทิตี้อื่นหลายเอนทิตี้ใน Dataverse Web API สำหรับ Dynamics 365 Human Resources ซึ่งอาจเกี่ยวข้องกับการรวมของคุณด้วย</span><span class="sxs-lookup"><span data-stu-id="ba79f-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="ba79f-147">ตัวอย่างเช่น คุณอาจต้องการรายละเอียดเกี่ยวกับผู้ปฏิบัติงาน งาน ตําแหน่งงาน หรือเอนทิตี้อื่นๆที่ไม่ได้กําหนดที่นี่ด้วย</span><span class="sxs-lookup"><span data-stu-id="ba79f-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="ba79f-148">เอนทิตี้จากเอนทิตี้เหล่านี้ถูกอ้างอิงในความสัมพันธ์คีย์นอกหรือคุณสมบัติการนําทาง</span><span class="sxs-lookup"><span data-stu-id="ba79f-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![แบบจำลองข้อมูล API การรวม ATS](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="ba79f-150">คำขอการสรรหาบุคลากรและเอนทิตี้และชุดตัวเลือกที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ba79f-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="ba79f-151">ตัวอย่างการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="ba79f-151">Example query:</span></span> 

- [<span data-ttu-id="ba79f-152">ตัวอย่างการสอบถามเกี่ยวกับคำขอการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ba79f-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="ba79f-153">เอนทิตี้:</span><span class="sxs-lookup"><span data-stu-id="ba79f-153">Entities:</span></span>

- [<span data-ttu-id="ba79f-154">คำขอสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ba79f-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="ba79f-155">ตำแหน่งของคำขอสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ba79f-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="ba79f-156">การสรรหาบุคลากรที่มีคำขอทักษะ</span><span class="sxs-lookup"><span data-stu-id="ba79f-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="ba79f-157">การสรรหาบุคลากรที่มีคำขอการศึกษา</span><span class="sxs-lookup"><span data-stu-id="ba79f-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="ba79f-158">ที่ตั้งของคำขอสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ba79f-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="ba79f-159">ชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ba79f-159">Option sets:</span></span>

- [<span data-ttu-id="ba79f-160">สถานะยกเว้นงาน</span><span class="sxs-lookup"><span data-stu-id="ba79f-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="ba79f-161">สถานะการสรรหาบุคลากรที่มีคำขอตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="ba79f-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="ba79f-162">สถานะคำขอขการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="ba79f-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="ba79f-163">ประเภทงานตามระเบียบบังคับ</span><span class="sxs-lookup"><span data-stu-id="ba79f-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="ba79f-164">ผู้สมัครที่จะว่าจ้างและเอนทิตี้และชุดตัวเลือกที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ba79f-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="ba79f-165">ตัวอย่างการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="ba79f-165">Example query:</span></span>

- [<span data-ttu-id="ba79f-166">ตัวอย่างการสอบถามสำหรับผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="ba79f-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="ba79f-167">เอนทิตี้:</span><span class="sxs-lookup"><span data-stu-id="ba79f-167">Entities:</span></span>

- [<span data-ttu-id="ba79f-168">ผู้สมัครที่จะจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="ba79f-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="ba79f-169">บุคคล</span><span class="sxs-lookup"><span data-stu-id="ba79f-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="ba79f-170">การศึกษาของบุคคล</span><span class="sxs-lookup"><span data-stu-id="ba79f-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="ba79f-171">ประสบการณ์การทำงานของบุคคล</span><span class="sxs-lookup"><span data-stu-id="ba79f-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="ba79f-172">ที่อยู่ของบุคคล</span><span class="sxs-lookup"><span data-stu-id="ba79f-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="ba79f-173">ผู้ติดต่อฝ่าย</span><span class="sxs-lookup"><span data-stu-id="ba79f-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="ba79f-174">ทักษะของบุคคล</span><span class="sxs-lookup"><span data-stu-id="ba79f-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="ba79f-175">ระดับการประเมิน</span><span class="sxs-lookup"><span data-stu-id="ba79f-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="ba79f-176">ใบรับรองของบุคคล</span><span class="sxs-lookup"><span data-stu-id="ba79f-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="ba79f-177">ชนิดของประกาศนียบัตร</span><span class="sxs-lookup"><span data-stu-id="ba79f-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="ba79f-178">การคัดเลือกบุคคล</span><span class="sxs-lookup"><span data-stu-id="ba79f-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="ba79f-179">ชนิดการคัดเลือก</span><span class="sxs-lookup"><span data-stu-id="ba79f-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="ba79f-180">หมายเลขการระบุรหัสประจำตัวบุคคล</span><span class="sxs-lookup"><span data-stu-id="ba79f-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="ba79f-181">ชุดตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ba79f-181">Option sets:</span></span>

- [<span data-ttu-id="ba79f-182">ผลการรวมผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="ba79f-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="ba79f-183">ว่าง ใช่ ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="ba79f-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="ba79f-184">สถานะการเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ba79f-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="ba79f-185">ชนิดผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="ba79f-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="ba79f-186">เกณฑ์หน่วยกิตการศึกษา</span><span class="sxs-lookup"><span data-stu-id="ba79f-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="ba79f-187">เพศ</span><span class="sxs-lookup"><span data-stu-id="ba79f-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="ba79f-188">สถานภาพการสมรส</span><span class="sxs-lookup"><span data-stu-id="ba79f-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="ba79f-189">เดือนของปี</span><span class="sxs-lookup"><span data-stu-id="ba79f-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="ba79f-190">ไม่ ใช่</span><span class="sxs-lookup"><span data-stu-id="ba79f-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="ba79f-191">หน่วยของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="ba79f-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="ba79f-192">ความถี่ในการคัดกรอง</span><span class="sxs-lookup"><span data-stu-id="ba79f-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="ba79f-193">ความถี่ในการคัดกรองที่สร้างจาก</span><span class="sxs-lookup"><span data-stu-id="ba79f-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="ba79f-194">ชนิดระดับทักษะ</span><span class="sxs-lookup"><span data-stu-id="ba79f-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="ba79f-195">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="ba79f-195">See also</span></span>

[<span data-ttu-id="ba79f-196">สรรหาผู้สมัครงาน</span><span class="sxs-lookup"><span data-stu-id="ba79f-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="ba79f-197">Microsoft Dataverse คืออะไร</span><span class="sxs-lookup"><span data-stu-id="ba79f-197">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="ba79f-198">ใช้ Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="ba79f-198">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="ba79f-199">สร้างและอัพเดตชุดตัวเลือกโดยใช้ Web API</span><span class="sxs-lookup"><span data-stu-id="ba79f-199">Create and update option sets using the Web API</span></span>](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]