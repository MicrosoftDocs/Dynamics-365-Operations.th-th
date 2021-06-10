---
title: บทนำ API การรวมบัญชีเงินเดือน
description: หัวข้อนี้อธิบายAPI การรวมบัญชีเงินเดือน Dynamics 365 Human Resources
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6d8a1cb9619a863184460a74e472af3f06934b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058571"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="5504f-103">บทนำ API การรวมบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5504f-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5504f-104">เอกสารนี้อธิบายAPI การรวมบัญชีเงินเดือน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="5504f-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="5504f-105">API จะเปิดใช้งานการรวมแบบครอบคลุมที่มีประสิทธิภาพระหว่างทรัพยากรบุคคลและระบบบัญชีเงินเดือนที่เป็นคู่ค้า</span><span class="sxs-lookup"><span data-stu-id="5504f-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="5504f-106">ประสบการณ์รวมจะเริ่มต้นในทรัพยากรบุคคลพร้อมด้วยโปรไฟล์พนักงาน เงินเดือนและการหักลด และข้อมูลเงินสมทบ</span><span class="sxs-lookup"><span data-stu-id="5504f-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="5504f-107">เมื่อคุณจ้างงานพนักงานและป้อนโปรไฟล์ที่ต้องใช้และจ่ายข้อมูลเข้าในทรัพยากรบุคคล ระบบบัญชีเงินเดือนจะดึงข้อมูลนี้เพื่อใช้เมื่อประมวลผลค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5504f-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="5504f-108">การอัปเดตใด ๆ ที่พนักงานหรือข้อมูลค่าจ้างจะถูกดึงไว้เพื่อใช้ในการรันค่าจ้างในภายหลังด้วย</span><span class="sxs-lookup"><span data-stu-id="5504f-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![โฟลว์การรวมบัญชีเงินเดือน](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="5504f-110">เมื่อต้องการเปิดใช้งานการรวม ทรัพยากรบุคคลได้รวมส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5504f-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="5504f-111">ฟังก์ชันในการทำเครื่องหมายพนักงานเป็นพร้อมจ่าย</span><span class="sxs-lookup"><span data-stu-id="5504f-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="5504f-112">API การรวมจะเปิดฟังก์ชันใหม่เพื่อรวมใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="5504f-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="5504f-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="5504f-113">Microsoft Dataverse</span></span>

<span data-ttu-id="5504f-114">API นี้จะสร้างขึ้นบน Microsoft Dataverse (ซึ่งก่อนหน้านี้เรียกว่า Common Data Service)</span><span class="sxs-lookup"><span data-stu-id="5504f-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="5504f-115">การโต้ตอบ RESTful ทั้งหมดกับ API นี้กระทำผ่าน Microsoft Dataverse Web API ที่ใช้ OData</span><span class="sxs-lookup"><span data-stu-id="5504f-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="5504f-116">API นี้เป็นเซ็ตย่อยของ Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="5504f-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="5504f-117">Dataverse Web API จะกําหนดลักษณะต่างๆ เช่น การพิสูจน์ตัวจริง SLAs ชุดงาน การควบคุมการเกิดพร้อมกัน และการจัดการข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="5504f-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="5504f-118">สำหรับข้อมูลเพิ่มเติมทั่วไปเกี่ยวกับ Microsoft Dataverse Web API ให้ดูที่</span><span class="sxs-lookup"><span data-stu-id="5504f-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="5504f-119">Microsoft Dataverse คืออะไร</span><span class="sxs-lookup"><span data-stu-id="5504f-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="5504f-120">ใช้ Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="5504f-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="5504f-121">Microsoft Dataverse คู่มือสำหรับนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="5504f-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="5504f-122">คู่มือนี้รวมรายละเอียดและแนวทางของนักพัฒนาในการใช้ Dataverse Web API รวมถึงหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5504f-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="5504f-123">รวจสอบความถูกต้อง Microsoft Dataverse กับ Web API</span><span class="sxs-lookup"><span data-stu-id="5504f-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="5504f-124">ดําเนินงานโดยใช้ Web API</span><span class="sxs-lookup"><span data-stu-id="5504f-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="5504f-125">ใช้ Postman กับ Web API</span><span class="sxs-lookup"><span data-stu-id="5504f-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="5504f-126">ใช้การติดตามการเปลี่ยนแปลงเพื่อซิงโครไนส์ข้อมูลกับระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="5504f-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="5504f-127">ตารางเสมือนสำหรับทรัพยากรบุคคล Dataverse</span><span class="sxs-lookup"><span data-stu-id="5504f-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="5504f-128">ปลายทางสำหรับ API การรวมค่าจ้างใช้ความสามารถของแพลตฟอร์มตารางเสมือนของ Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="5504f-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="5504f-129">โดยค่าเริ่มต้น ตารางเสมือนและปลายทาง API ที่เกี่ยวข้องจะไม่ปรับใช้กับสภาพแวดล้อมของทรัพยากรบุคคล การเปิดใช้งานองค์กรเพื่อระบุว่าปลายทาง OData ใดจะแสดงต่อสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="5504f-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="5504f-130">เมื่อต้องการใช้ API ตารางเสมือนของเอนทิตี้ทรัพยากรบุคคลจะต้องสร้างให้กับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="5504f-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="5504f-131">สำหรับข้อมูลเกี่ยวกับการสร้างตารางเสมือนของ API ให้ดูที่ [การตั้งค่าคอนฟิกตารางเสมือน Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="5504f-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="5504f-132">แบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5504f-132">Data model</span></span>

<span data-ttu-id="5504f-133">แผนภาพต่อไปนี้แสดงความสัมพันธ์ภายใน API</span><span class="sxs-lookup"><span data-stu-id="5504f-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="5504f-134">หลายชนิดมีคีย์นอกไปยังเป็นเอนทิตี้ที่มีอยู่ก่อนอื่นๆในทรัพยากรบุคคลที่ไม่ได้แสดงที่นี่</span><span class="sxs-lookup"><span data-stu-id="5504f-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="5504f-135">เอกสารนี้แสดงข้อมูลเกี่ยวกับเอนทิตี้ที่เฉพาะเจาะจงให้กับสถานการณ์การรวมระบบค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="5504f-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="5504f-136">อย่างไรก็ตาม มีเอนทิตีอื่นหลายเอนทิตีใน Dataverse Web API สำหรับทรัพยากรบุคคลซึ่งอาจเกี่ยวข้องกับการรวมของคุณด้วย</span><span class="sxs-lookup"><span data-stu-id="5504f-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="5504f-137">บางเอนทิตีจากเอนทิตีเหล่านี้ถูกอ้างอิงในความสัมพันธ์คีย์นอกหรือคุณสมบัติการนําทาง</span><span class="sxs-lookup"><span data-stu-id="5504f-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![แบบจำลองข้อมูล API การรวมระบบค่าจ้าง](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="5504f-139">พนักงานค่าจ้างและเอนทิตีที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="5504f-139">Payroll employee and related entities</span></span>

<span data-ttu-id="5504f-140">เอนทิตี้:</span><span class="sxs-lookup"><span data-stu-id="5504f-140">Entities:</span></span>

- [<span data-ttu-id="5504f-141">พนักงานในบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5504f-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="5504f-142">ที่อยู่ผู้ปฏิบัติงานในบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5504f-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="5504f-143">แผนค่าตอบแทนคงที่ของบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5504f-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="5504f-144">งานของตําแหน่งในบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5504f-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="5504f-145">ตําแหน่งในบัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5504f-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="5504f-146">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="5504f-146">See also</span></span>

[<span data-ttu-id="5504f-147">สร้างและตรวจทานเอนทิตี้บัญชีเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="5504f-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="5504f-148">ตั้งค่าคอนฟิกพารามิเตอร์ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5504f-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="5504f-149">ตั้งค่าคอนฟิกพารามิเตอร์ที่ใช้ร่วมกันของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="5504f-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="5504f-150">Microsoft Dataverse คืออะไร</span><span class="sxs-lookup"><span data-stu-id="5504f-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="5504f-151">ใช้ Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="5504f-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]