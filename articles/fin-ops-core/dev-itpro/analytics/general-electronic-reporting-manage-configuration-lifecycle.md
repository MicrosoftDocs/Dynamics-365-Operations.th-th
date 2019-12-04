---
title: จัดการวงจรชีวิตการตั้งค่าคอนฟิกรายงานทางอิเล็กทรอนิกส์ (ER)
description: หัวข้อนี้อธิบายวิธีการจัดการการตั้งค่าคอนฟิกของวงจรการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับโซลูชัน Microsoft Dynamics 365 Finance
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
ms.openlocfilehash: ecaeb80f3cda2ee24533ed263df63cc10c5ffc65
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771107"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="812ed-103">จัดการวงจรชีวิตการตั้งค่าคอนฟิกรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="812ed-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="812ed-104">หัวข้อนี้อธิบายวิธีการจัดการการตั้งค่าคอนฟิกวงจรการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="812ed-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="812ed-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="812ed-105">Overview</span></span>

<span data-ttu-id="812ed-106">การรายงานทางอิเล็กทรอนิกส์ (ER) เป็นกลไกที่สนับสนุนให้เป็นไปตามกฎหมายและข้อกำหนดเฉพาะประเทศเกี่ยวกับเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="812ed-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="812ed-107">โดยทั่วไป ER ถือว่ามีความสามารถในการทำงานต่อไปนี้ สำหรับเอกสารอิเล็กทรอนิกส์เดี่ยว </span><span class="sxs-lookup"><span data-stu-id="812ed-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="812ed-108">สำหรับรายละเอียดเพิ่มเติม ดู [ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md)</span><span class="sxs-lookup"><span data-stu-id="812ed-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="812ed-109">ออกแบบเท็มเพลตสำหรับเอกสารอิเล็กทรอนิกส์:</span><span class="sxs-lookup"><span data-stu-id="812ed-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="812ed-110">ระบุแหล่งข้อมูลที่จำเป็นที่สามารถแสดงในเอกสารได้:</span><span class="sxs-lookup"><span data-stu-id="812ed-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="812ed-111">ข้อมูลพื้นฐาน เช่น ตารางข้อมูล เอนทิตี้้ข้อมูล และลำดับชั้นของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="812ed-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="812ed-112">คุณสมบัติของกระบวนการเฉพาะ เช่น วันที่ดำเนินการและเวลา และโซนเวลา</span><span class="sxs-lookup"><span data-stu-id="812ed-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="812ed-113">พารามิเตอร์ที่ผู้ใช้ป้อนถูกระบุโดยผู้ใช้ปลายทางที่เวลาการรัน</span><span class="sxs-lookup"><span data-stu-id="812ed-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="812ed-114">กำหนดองค์ประกอบของเอกสารที่จำเป็น และโทโพโลยีเพื่อระบุรูปแบบของเอกสารขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="812ed-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="812ed-115">ตั้งค่าคอนฟิกการไหลของข้อมูลที่ต้องการ จากแหล่งข้อมูลที่ถูกเลือกไปยังองค์ประกอบของเอกสารที่กำหนด (ผ่านทางแหล่งข้อมูลที่รวมกับส่วนประกอบของรูปแบบของเอกสาร) และระบุตรรกะการควบคุมกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="812ed-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="812ed-116">ทำให้เท็มเพลตพร้อมใช้งาน เพื่อให้สามารถใช้ในอินสแตนซ์อื่นได้:</span><span class="sxs-lookup"><span data-stu-id="812ed-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="812ed-117">แปลงเท็มเพลตของเอกสารที่ถูกสร้างขึ้นในการตั้งค่าคอนฟิก ER และส่งออกการตั้งค่าคอนฟิกจากอินสแตนซ์ของแอพพลิเคชั่นปัจจุบันเป็นแพคเกจ XML ที่สามารถถูกจัดเก็บเฉพาะที่หรือใน LCS ได้</span><span class="sxs-lookup"><span data-stu-id="812ed-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="812ed-118">แปลงการตั้งค่าคอนฟิก ER ลงในเท็มเพลตเอกสารของแอพพลิเคชั่น</span><span class="sxs-lookup"><span data-stu-id="812ed-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="812ed-119">นำเข้าแพคเกจ XML ที่ถูกจัดเก็บเฉพาะที่ หรือใน LCS ลงในอินสแตนซ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="812ed-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="812ed-120">เลือกกำหนดเท็มเพลตของเอกสารอิเล็กทรอนิกส์:</span><span class="sxs-lookup"><span data-stu-id="812ed-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="812ed-121">นำเท็มเพลตจาก LCS ไปยังอินสแตนซ์ปัจจุบัน เพื่อเป็นการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="812ed-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="812ed-122">ออกแบบเวอร์ชันที่กำหนดเองของการตั้งค่าคอนฟิก ER และเก็บการอ้างอิงไปยังเวอร์ชันพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="812ed-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="812ed-123">รวมเท็มเพลตกับกระบวนการเฉพาะทางธุรกิจ เพื่อให้พร้อมใช้งานในแอพพลิเคชั่น:</span><span class="sxs-lookup"><span data-stu-id="812ed-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="812ed-124">ตั้งค่าคอนฟิกเพื่อให้แอพพลิเคชั่นเริ่มใช้การตั้งค่าคอนฟิก ER โดยอ้างอิงถึงการตั้งค่าคอนฟิกในพารามิเตอร์ที่เกี่ยวข้องกับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="812ed-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="812ed-125">ตัวอย่างเช่น อ้างอิงการตั้งค่าคอนฟิก ER ในวิธีการชำระเงินบัญชีเจ้าหนี้บัญชีหนึ่งๆ เพื่อสร้างข้อความการชำระเงินทางอิเล็กทรอนิกส์สำหรับใบแจ้งหนี้ที่ประมวลผล</span><span class="sxs-lookup"><span data-stu-id="812ed-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="812ed-126">ใช้เท็มเพลตในกระบวนการทางธุรกิจเฉพาะ:</span><span class="sxs-lookup"><span data-stu-id="812ed-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="812ed-127">รันการตั้งค่าคอนฟิก ER ในกระบวนการทางธุรกิจเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="812ed-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="812ed-128">ตัวอย่างเช่น เพื่อสร้างข้อความการชำระเงินทางอิเล็กทรอนิกส์สำหรับการประมวลผลใบแจ้งหนี้ เมื่อมีการเลือกวิธีการชำระเงินที่อ้างอิงถึงการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="812ed-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="812ed-129">แนวคิด</span><span class="sxs-lookup"><span data-stu-id="812ed-129">Concepts</span></span>
<span data-ttu-id="812ed-130">บทบาทและกิจกรรมที่เกี่ยวข้องต่อไปนี้ เชื่อมโยงกับวงจรการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="812ed-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="812ed-131">บทบาท</span><span class="sxs-lookup"><span data-stu-id="812ed-131">Role</span></span>                                       | <span data-ttu-id="812ed-132">กิจกรรม</span><span class="sxs-lookup"><span data-stu-id="812ed-132">Activities</span></span>                                                      | <span data-ttu-id="812ed-133">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="812ed-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="812ed-134">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="812ed-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="812ed-135">สร้างและจัดการส่วนประกอบ ER (แบบจำลองและรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="812ed-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="812ed-136">นักธุรกิจผู้ออกแบบโดเมน ER– แบบจำลองข้อมูลเฉพาะ ออกแบบเท็มเพลตที่จำเป็นสำหรับเอกสารอิเล็กทรอนิกส์ และผูกให้สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="812ed-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="812ed-137">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="812ed-137">Electronic reporting developer</span></span>             | <span data-ttu-id="812ed-138">สร้างและจัดการการแม็ปแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="812ed-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="812ed-139">ผู้เชี่ยวชาญที่เลือกแหล่งข้อมูลทางการเงินที่จำเป็น และผูกเข้ากับแบบจำลองข้อมูลเฉพาะ – โดเมน ER</span><span class="sxs-lookup"><span data-stu-id="812ed-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="812ed-140">หัวหน้างานฝ่ายบัญชี</span><span class="sxs-lookup"><span data-stu-id="812ed-140">Accounting supervisor</span></span>                      | <span data-ttu-id="812ed-141">ตั้งค่าคอนฟิกการตั้งค่าที่เกี่ยวข้องกับกระบวนการ ซึ่งอ้างอิงวัตถุ ER</span><span class="sxs-lookup"><span data-stu-id="812ed-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="812ed-142">ตัวอย่างเช่น บทบาท **ผู้ดูแลบัญชี** ที่ช่วยให้การตั้งค่าของการตั้งค่าคอนฟิก ER สามารถที่จะใช้ได้ในวิธีการชำระเงินบัญชีเจ้าหนี้ของบัญชีหนึ่งๆ เพื่อสร้างข้อความการชำระเงินทางอิเล็กทรอนิกส์สำหรับการประมวลผลใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="812ed-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="812ed-143">เจ้าหน้าที่ฝ่ายชำระเงินบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="812ed-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="812ed-144">ใช้วัตถุ ER ในกระบวนการทางธุรกิจเฉพาะ:</span><span class="sxs-lookup"><span data-stu-id="812ed-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="812ed-145">ตัวอย่างเช่น บทบาท **เจ้าหน้าที่ฝ่ายชำระเงินบัญชีเจ้าหนี้** ที่อนุญาตให้ข้อความการชำระเงินทางอิเล็กทรอนิกส์สามารถถูกสร้างขึ้นได้ สำหรับการประมวลผลใบแจ้งหนี้ โดยขึ้นอยู่กับรูปแบบ ER ที่ถูกตั้งค่าคอนฟิกสำหรับวิธีการชำระเงินเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="812ed-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="812ed-146">วงจรชีวิตพัฒนาการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="812ed-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="812ed-147">สำหรับเหตุผลที่เกี่ยวข้องกับ ER ต่อไปนี้ ขอแนะนำให้คุณออกแบบการตั้งค่าคอนฟิก ER ใน สิ่งแวดล้อมการพัฒนา เป็นอินสแตนซ์ที่แยกต่างหากของ Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="812ed-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="812ed-148">ผู้ใช้ในบทบาท **นักพัฒนารายงานทางอิเล็กทรอนิกส์** หรือบทบาท **ที่ปรึกษาฟังก์ชันรายงานอิเล็กทรอนิกส์** อย่างใดอย่างหนึ่งสามารถแก้ไขการตั้งค่าคอนฟิก และรันเพื่อทดสอบวัตถุประสงค์ได้</span><span class="sxs-lookup"><span data-stu-id="812ed-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="812ed-149">สถานการณ์จำลองนี้อาจทำให้การเรียกชื่อวิธีการของลำดับชั้นของข้อมูลและตารางที่อาจเป็นอันตรายสำหรับข้อมูลธุรกิจและประสิทธิภาพการทำงานของอินสแตนซ์</span><span class="sxs-lookup"><span data-stu-id="812ed-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="812ed-150">ชื่อวิธีการของลำดับชั้นของข้อมูลและตารางที่เป็นแหล่งข้อมูล ER ของการตั้งค่าคอนฟิก ER ไม่ได้ถูกจำกัดโดยการเข้าใช้งานและการระบุเนื้อหาของบริษัท</span><span class="sxs-lookup"><span data-stu-id="812ed-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="812ed-151">ดังนั้น ข้อมูลในบทบาท **นักพัฒนารายงานทางอิเล็กทรอนิกส์** หรือบทบาท **ที่ปรึกษาฟังก์ชันรายงานอิเล็กทรอนิกส์** อย่างใดอย่างหนึ่งสามารถเข้าถึงข้อมูลที่อ่อนไหวทางธุรกิจได้</span><span class="sxs-lookup"><span data-stu-id="812ed-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="812ed-152">การตั้งค่าคอนฟิก ER ที่ถูกออกแบบใน สภาพแวดล้อมการพัฒนา สามารถถูกอัพโหลดไปที่ สภาพแวดล้อมการทดสอบ สำหรับการประเมินการตั้งค่าคอนฟิก (การรวมกระบวนการที่เหมาะสม ความถูกต้องของผลลัพธ์ และประสิทธิภาพ) และการรับรองคุณภาพ เช่น ความถูกต้องของสิทธิการเข้าถึงซึ่งควบคุมโดยบทบาท และการแบ่งแยกหน้าที่ได้</span><span class="sxs-lookup"><span data-stu-id="812ed-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="812ed-153">คุณลักษณะที่เปิดใช้งานการแลกเปลี่ยนการตั้งค่าคอนฟิก ER สามารถถูกใช้สำหรับวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="812ed-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="812ed-154">ในตอนท้าย การตั้งค่าคอนฟิก ER ที่ได้รับการพิสูจน์แล้วสามารถถูกอัพโหลดไปยัง LCS ที่สามารถถูกใช้ร่วมกันกับสมาชิกการบริการ หรือไปยัง สภาพแวดล้อมการผลิต สำหรับการใช้ภายใน ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="812ed-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![วงจรการตั้งค่าคอนฟิก ER](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="812ed-156">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="812ed-156">Additional resources</span></span>

[<span data-ttu-id="812ed-157">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="812ed-157">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
