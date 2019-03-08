---
title: จัดการวงจรชีวิตการตั้งค่าคอนฟิกรายงานทางอิเล็กทรอนิกส์ (ER)
description: หัวข้อนี้อธิบายวิธีการจัดการการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับโซลูชัน Microsoft Dynamics 365 for Finance and Operations Lifecycle Services (LCS)
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5724ba62bfb2c6e75ae895dc9285966c25f387a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "344811"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="adb1c-103">จัดการวงจรชีวิตการตั้งค่าคอนฟิกรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="adb1c-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adb1c-104">หัวข้อนี้อธิบายวิธีการจัดการการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับโซลูชัน Microsoft Dynamics 365 for Finance and Operations Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="adb1c-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for the Microsoft Dynamics 365 for Finance and Operations solution.</span></span>

## <a name="overview"></a><span data-ttu-id="adb1c-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="adb1c-105">Overview</span></span>

<span data-ttu-id="adb1c-106">การรายงานทางอิเล็กทรอนิกส์ (ER) เป็นกลไกที่สนับสนุนตามกฎหมายที่ต้องการและเอกสารทางอิเล็กทรอนิกส์เฉพาะประเทศใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adb1c-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="adb1c-107">โดยทั่วไป ER ถือว่ามีความสามารถในการทำงานต่อไปนี้ สำหรับเอกสารอิเล็กทรอนิกส์เดี่ยว </span><span class="sxs-lookup"><span data-stu-id="adb1c-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="adb1c-108">สำหรับรายละเอียดเพิ่มเติม ดู [ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)</span><span class="sxs-lookup"><span data-stu-id="adb1c-108">For more details, see [Electronic reporting overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="adb1c-109">ออกแบบเท็มเพลตสำหรับเอกสารอิเล็กทรอนิกส์:</span><span class="sxs-lookup"><span data-stu-id="adb1c-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="adb1c-110">ระบุแหล่งข้อมูลที่จำเป็นที่สามารถแสดงในเอกสารได้:</span><span class="sxs-lookup"><span data-stu-id="adb1c-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="adb1c-111">ข้อมูล Finance and Operations พื้นฐาน เช่น ตารางข้อมูล เอนทิตี้้ข้อมูล และคลาส</span><span class="sxs-lookup"><span data-stu-id="adb1c-111">Underlying Finance and Operations data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="adb1c-112">คุณสมบัติของกระบวนการเฉพาะ เช่น วันที่ดำเนินการและเวลา และโซนเวลา</span><span class="sxs-lookup"><span data-stu-id="adb1c-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="adb1c-113">พารามิเตอร์ที่ผู้ใช้ป้อนถูกระบุโดยผู้ใช้ปลายทางที่เวลาการรัน</span><span class="sxs-lookup"><span data-stu-id="adb1c-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="adb1c-114">กำหนดองค์ประกอบของเอกสารที่จำเป็น และโทโพโลยีเพื่อระบุรูปแบบของเอกสารขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="adb1c-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="adb1c-115">ตั้งค่าคอนฟิกการไหลของข้อมูลที่ต้องการ จากแหล่งข้อมูลที่ถูกเลือกไปยังองค์ประกอบของเอกสารที่กำหนด (ผ่านทางแหล่งข้อมูลที่รวมกับส่วนประกอบของรูปแบบของเอกสาร) และระบุตรรกะการควบคุมกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="adb1c-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="adb1c-116">ทำให้เท็มเพลตพร้อมใช้งาน เพื่อให้สามารถใช้ในอินสแตนซ์อื่นของ Finance and Operations ได้:</span><span class="sxs-lookup"><span data-stu-id="adb1c-116">Make a template available so that it can be used in other Finance and Operations instances:</span></span>

    - <span data-ttu-id="adb1c-117">แปลงเท็มเพลตเอกสารที่ถูกสร้างขึ้นใน Finance and Operations ลงในการตั้งค่าคอนฟิก ER และส่งออกการตั้งค่าคอนฟิกจากอินสแตนซ์ของ Finance and Operations ปัจจุบัน เป็นแพคเกจ XML ที่สามารถถูกจัดเก็บเฉพาะที่ หรือใน LCS ได้</span><span class="sxs-lookup"><span data-stu-id="adb1c-117">Transform a document template that was created in Finance and Operations into an ER configuration, and export the configuration from the current Finance and Operations instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="adb1c-118">แปลงการตั้งค่าคอนฟิก ER ลงในเท็มเพลตเอกสาร Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adb1c-118">Transform an ER configuration into a Finance and Operations document template.</span></span>
    - <span data-ttu-id="adb1c-119">นำเข้าแพคเกจ XML ที่ถูกจัดเก็บเฉพาะที่ หรือใน LCS ลงในอินสแตนซ์ Finance and Operations ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="adb1c-119">Import an XML package that is stored either locally or in LCS into the current Finance and Operations instance.</span></span>

- <span data-ttu-id="adb1c-120">เลือกกำหนดเท็มเพลตของเอกสารอิเล็กทรอนิกส์:</span><span class="sxs-lookup"><span data-stu-id="adb1c-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="adb1c-121">นำเท็มเพลตจาก LCS ไปยังอินสแตนซ์ Finance and Operations ปัจจุบัน เป็นการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="adb1c-121">Bring a template from LCS into the current Finance and Operations instance as an ER configuration.</span></span>
    - <span data-ttu-id="adb1c-122">ออกแบบเวอร์ชันที่กำหนดเองของการตั้งค่าคอนฟิก ER และเก็บการอ้างอิงไปยังเวอร์ชันพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="adb1c-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="adb1c-123">รวมเท็มเพลตกับกระบวนการทางธุรกิจเฉพาะ เพื่อให้พร้อมใช้งานใน Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="adb1c-123">Integrate a template with a particular business process, so that it's available in Finance and Operations:</span></span>

    - <span data-ttu-id="adb1c-124">ตั้งค่าคอนฟิกการตั้งค่าเพื่อให้ Finance and Operations เริ่มใช้การตั้งค่าคอนฟิก ER โดยอ้างอิงถึงการตั้งค่าคอนฟิกในพารามิเตอร์ที่เกี่ยวข้องกับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="adb1c-124">Configure settings so that Finance and Operations starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="adb1c-125">ตัวอย่างเช่น อ้างอิงการตั้งค่าคอนฟิก ER ในวิธีการชำระเงินบัญชีเจ้าหนี้บัญชีหนึ่งๆ เพื่อสร้างข้อความการชำระเงินทางอิเล็กทรอนิกส์สำหรับใบแจ้งหนี้ที่ประมวลผล</span><span class="sxs-lookup"><span data-stu-id="adb1c-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="adb1c-126">ใช้เท็มเพลตในกระบวนการทางธุรกิจเฉพาะ:</span><span class="sxs-lookup"><span data-stu-id="adb1c-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="adb1c-127">รันการตั้งค่าคอนฟิก ER ในกระบวนการทางธุรกิจเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="adb1c-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="adb1c-128">ตัวอย่างเช่น เพื่อสร้างข้อความการชำระเงินทางอิเล็กทรอนิกส์สำหรับการประมวลผลใบแจ้งหนี้ เมื่อมีการเลือกวิธีการชำระเงินที่อ้างอิงถึงการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="adb1c-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="adb1c-129">แนวคิด</span><span class="sxs-lookup"><span data-stu-id="adb1c-129">Concepts</span></span>
<span data-ttu-id="adb1c-130">บทบาทและกิจกรรมที่เกี่ยวข้องต่อไปนี้ เชื่อมโยงกับวงจรการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="adb1c-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="adb1c-131">บทบาท</span><span class="sxs-lookup"><span data-stu-id="adb1c-131">Role</span></span>                                       | <span data-ttu-id="adb1c-132">กิจกรรม</span><span class="sxs-lookup"><span data-stu-id="adb1c-132">Activities</span></span>                                                      | <span data-ttu-id="adb1c-133">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="adb1c-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="adb1c-134">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="adb1c-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="adb1c-135">สร้างและจัดการส่วนประกอบ ER (แบบจำลองและรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="adb1c-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="adb1c-136">นักธุรกิจผู้ออกแบบโดเมน ER– แบบจำลองข้อมูลเฉพาะ ออกแบบเท็มเพลตที่จำเป็นสำหรับเอกสารอิเล็กทรอนิกส์ และผูกให้สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="adb1c-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="adb1c-137">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="adb1c-137">Electronic reporting developer</span></span>             | <span data-ttu-id="adb1c-138">สร้างและจัดการการแม็ปแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="adb1c-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="adb1c-139">ผู้เชี่ยวชาญ Finance and Operations ที่เลือกแหล่งข้อมูล Finance and Operations ที่จำเป็น และผูกเข้ากับแบบจำลองข้อมูลเฉพาะโดเมน ER</span><span class="sxs-lookup"><span data-stu-id="adb1c-139">A Finance and Operations specialist who selects the required Finance and Operations data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="adb1c-140">หัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="adb1c-140">Accounting supervisor</span></span>                      | <span data-ttu-id="adb1c-141">ตั้งค่าคอนฟิกการตั้งค่าที่เกี่ยวข้องกับกระบวนการ ซึ่งอ้างอิงวัตถุ ER</span><span class="sxs-lookup"><span data-stu-id="adb1c-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="adb1c-142">ตัวอย่างเช่น บทบาท **ผู้ดูแลบัญชี** ที่ช่วยให้การตั้งค่าของการตั้งค่าคอนฟิก ER สามารถที่จะใช้ได้ในวิธีการชำระเงินบัญชีเจ้าหนี้ของบัญชีหนึ่งๆ เพื่อสร้างข้อความการชำระเงินทางอิเล็กทรอนิกส์สำหรับการประมวลผลใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="adb1c-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="adb1c-143">เจ้าหน้าที่ฝ่ายชำระเงินบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="adb1c-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="adb1c-144">ใช้วัตถุ ER ในกระบวนการทางธุรกิจเฉพาะ:</span><span class="sxs-lookup"><span data-stu-id="adb1c-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="adb1c-145">ตัวอย่างเช่น บทบาท **เจ้าหน้าที่ฝ่ายชำระเงินบัญชีเจ้าหนี้** ที่อนุญาตให้ข้อความการชำระเงินทางอิเล็กทรอนิกส์สามารถถูกสร้างขึ้นได้ สำหรับการประมวลผลใบแจ้งหนี้ โดยขึ้นอยู่กับรูปแบบ ER ที่ถูกตั้งค่าคอนฟิกสำหรับวิธีการชำระเงินเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="adb1c-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="adb1c-146">วงจรชีวิตพัฒนาการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="adb1c-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="adb1c-147">สำหรับเหตุผลที่เกี่ยวข้องกับ ER ต่อไปนี้ ขอแนะนำให้คุณออกแบบการตั้งค่าคอนฟิก ER ใน สิ่งแวดล้อมการพัฒนา เป็นอินสแตนซ์ที่แยกต่างหากของ Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="adb1c-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="adb1c-148">ผู้ใช้ในบทบาท **นักพัฒนารายงานทางอิเล็กทรอนิกส์** หรือบทบาท **ที่ปรึกษาฟังก์ชันรายงานอิเล็กทรอนิกส์** อย่างใดอย่างหนึ่งสามารถแก้ไขการตั้งค่าคอนฟิก และรันเพื่อทดสอบวัตถุประสงค์ได้</span><span class="sxs-lookup"><span data-stu-id="adb1c-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="adb1c-149">สถานการณ์จำลองนี้สามารถทำให้เกิดการเรียกของวิธีการของคลาสและตารางที่อาจเป็นอันตรายสำหรับข้อมูลธุรกิจและประสิทธิภาพการทำงานของการใช้อินสแตนซ์ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adb1c-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the Finance and Operations instance.</span></span>
- <span data-ttu-id="adb1c-150">การเรียกวิธีการของคลาสและตารางที่เป็นแหล่งข้อมูล ER ของการตั้งค่าคอนฟิก ER ไม่ได้ถูกจำกัดโดยจุดเข้าใช้งาน Finance and Operations และล็อกเนื้อหาของบริษัท</span><span class="sxs-lookup"><span data-stu-id="adb1c-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by Finance and Operations entry points and logged company content.</span></span> <span data-ttu-id="adb1c-151">ดังนั้น ข้อมูลในบทบาท **นักพัฒนารายงานทางอิเล็กทรอนิกส์** หรือบทบาท **ที่ปรึกษาฟังก์ชันรายงานอิเล็กทรอนิกส์** อย่างใดอย่างหนึ่งสามารถเข้าถึงข้อมูลที่อ่อนไหวทางธุรกิจได้</span><span class="sxs-lookup"><span data-stu-id="adb1c-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="adb1c-152">การตั้งค่าคอนฟิก ER ที่ถูกออกแบบใน สภาพแวดล้อมการพัฒนา สามารถถูกอัพโหลดไปที่ สภาพแวดล้อมการทดสอบ สำหรับการประเมินการตั้งค่าคอนฟิก (การรวมกระบวนการที่เหมาะสม ความถูกต้องของผลลัพธ์ และประสิทธิภาพ) และการรับรองคุณภาพ เช่น ความถูกต้องของสิทธิการเข้าถึงซึ่งควบคุมโดยบทบาท และการแบ่งแยกหน้าที่ได้</span><span class="sxs-lookup"><span data-stu-id="adb1c-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="adb1c-153">คุณลักษณะที่เปิดใช้งานการแลกเปลี่ยนการตั้งค่าคอนฟิก ER สามารถถูกใช้สำหรับวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="adb1c-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="adb1c-154">ในตอนท้าย การตั้งค่าคอนฟิก ER ที่ได้รับการพิสูจน์แล้วสามารถถูกอัพโหลดไปยัง LCS ที่สามารถถูกใช้ร่วมกันกับสมาชิกการบริการ หรือไปยัง สภาพแวดล้อมการผลิต สำหรับการใช้ภายใน ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="adb1c-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![วงจรการตั้งค่าคอนฟิก ER](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="adb1c-156">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="adb1c-156">Additional resources</span></span>

[<span data-ttu-id="adb1c-157">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="adb1c-157">Electronic reporting overview</span></span>](general-electronic-reporting.md)
