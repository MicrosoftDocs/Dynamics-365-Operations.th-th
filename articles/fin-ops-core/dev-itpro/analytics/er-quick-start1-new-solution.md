---
title: ออกแบบโซลูชัน ER ใหม่เพื่อพิมพ์รายงานแบบกำหนดเอง
description: หัวข้อนี้จะอธิบายวิธีการออกแบบโซลูชันการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อพิมพ์รายงานแบบกำหนดเอง
author: NickSelin
manager: AnnBe
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5bbfae36fb15437f2baadc66663cbfdb28691e8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562622"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="92213-103">ออกแบบโซลูชัน ER ใหม่เพื่อพิมพ์รายงานแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="92213-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="92213-104">ขั้นตอนต่อไปนี้อธิบายถึงวิธีการที่ผู้ใช้ในบทบาทผู้ดูแลระบบ ผู้พัฒนาการรายงานทางอิเล็กทรอนิกส์ หรือผู้ที่ปรึกษาด้านการรายงานทางอิเล็กทรอนิกส์ สามารถตั้งค่าคอนฟิกพารามิเตอร์ของกรอบงาน ER การออกแบบการตั้งค่าคอนฟิก ER ที่จำเป็นต้องใช้ของโซลูชัน ER ใหม่เพื่อเข้าถึงข้อมูลของโดเมนธุรกิจเฉพาะ และสร้างรายงานแบบกำหนดเองในรูปแบบ Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="92213-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="92213-105">คุณสามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท **USMF**</span><span class="sxs-lookup"><span data-stu-id="92213-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="92213-106">ตั้งค่าคอนฟิกกรอบงาน ER</span><span class="sxs-lookup"><span data-stu-id="92213-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="92213-107">ตั้งค่าคอนฟิกพารามิเตอร์ ER</span><span class="sxs-lookup"><span data-stu-id="92213-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="92213-108">เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="92213-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="92213-109">ตรวจทานรายการของผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="92213-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="92213-110">เพิ่มผู้ให้บริการการตั้งค่าคอนฟิก ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="92213-111">เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="92213-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="92213-112">ออกแบบรูปแบบข้อมูลเฉพาะโดเมน</span><span class="sxs-lookup"><span data-stu-id="92213-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="92213-113">นำเข้าการตั้งค่าคอนฟิกรูปแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="92213-114">สร้างการตั้งค่าคอนฟิกรูปแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="92213-115">ตั้งชื่อรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="92213-116">เพิ่มฟิลด์รูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="92213-117">ทำการออกแบบของรูปแบบข้อมูลให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="92213-118">ออกแบบการแม็ปรูปแบบสำหรับรูปแบบข้อมูลที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="92213-119">นำเข้าการตั้งค่าคอนฟิกการแม็ปรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="92213-120">สร้างการตั้งค่าคอนฟิกการแม็ปรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="92213-121">ออกแบบส่วนประกอบการแม็ปรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="92213-122">เพิ่มแหล่งข้อมูลที่จะเข้าถึงตารางแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="92213-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="92213-123">เพิ่มแหล่งข้อมูลที่จะเข้าถึงการแจงนับแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="92213-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="92213-124">เพิ่มป้ายชื่อ ER เพื่อสร้างรายงานในภาษาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="92213-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="92213-125">เพิ่มแหล่งข้อมูลเพื่อแปลงผลลัพธ์ของการเปรียบเทียบค่าการแจงนับเป็นค่าข้อความ</span><span class="sxs-lookup"><span data-stu-id="92213-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="92213-126">ผูกแหล่งข้อมูลเข้ากับฟิลด์รูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="92213-127">ทำการออกแบบการแม็ปรูปแบบให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="92213-128">ออกแบบเท็มเพลตสำหรับรายงานแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="92213-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="92213-129">ออกแบบรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="92213-130">นำเข้าการตั้งค่าคอนฟิกรูปแบบที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="92213-131">สร้างการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="92213-132">นำเข้าเท็มเพลตของรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="92213-133">ตั้งค่าคอนฟิกรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="92213-134">กำหนดการผูกข้อมูลสำหรับชื่อรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="92213-135">ตรวจสอบแหล่งข้อมูลรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="92213-136">ผูกองค์ประกอบของรูปแบบกับฟิลด์แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="92213-137">เรียกใช้รูปแบบที่ออกแบบจาก ER</span><span class="sxs-lookup"><span data-stu-id="92213-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="92213-138">ปรับแต่งรูปแบบที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="92213-139">แก้ไขรูปแบบที่จะเปลี่ยนชื่อของเอกสารที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="92213-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="92213-140">ปรับเปลี่ยนรูปแบบที่จะเปลี่ยนลำดับของคำถาม</span><span class="sxs-lookup"><span data-stu-id="92213-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="92213-141">เรียกใช้รูปแบบที่ปรับเปลี่ยนจาก ER</span><span class="sxs-lookup"><span data-stu-id="92213-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="92213-142">ทำการออกแบบรูปแบบให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="92213-143">พัฒนาอาร์ทิแฟกต์ของแอปพลิเคชันเพื่อเรียกรายงานที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="92213-144">ปรับเปลี่ยนโค้ดต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="92213-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="92213-145">เพิ่มคลาสสัญญาข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="92213-146">เพิ่มคลาสตัวสร้าง UI</span><span class="sxs-lookup"><span data-stu-id="92213-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="92213-147">เพิ่มคลาสผู้ให้บริการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="92213-148">เพิ่มไฟล์ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="92213-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="92213-149">เพิ่มคลาสบริการรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="92213-150">เพิ่มคลาสตัวควบคุมรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="92213-151">เพิ่มรายการเมนู</span><span class="sxs-lookup"><span data-stu-id="92213-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="92213-152">เพิ่มรายการเมนูลงในเมนู</span><span class="sxs-lookup"><span data-stu-id="92213-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="92213-153">สร้างโครงการ Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92213-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="92213-154">เรียกใช้รูปแบบจากแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="92213-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="92213-155">ปรับแต่งโซลูชัน ER ที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="92213-156">ปรับเปลี่ยนการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="92213-157">เพิ่มแหล่งข้อมูลที่จะเข้าถึงออบเจ็กต์สัญญาข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="92213-158">เพิ่มแหล่งข้อมูลที่จะเข้าถึงเรกคอร์ดการแม็ปรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="92213-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="92213-159">เพิ่มแหล่งข้อมูลที่จะเข้าถึงเรกคอร์ดการแม็ปรูปแบบของรูปแบบ ER ที่เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="92213-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="92213-160">ป้อนชื่อของรูปแบบ ER ที่กำลังทำงานอยู่ในรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="92213-161">ทำการออกแบบการแม็ปรูปแบบให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="92213-162">ปรับเปลี่ยนรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="92213-163">เพิ่มองค์ประกอบรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="92213-164">ผูกองค์ประกอบรูปแบบที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="92213-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="92213-165">ทำการออกแบบรูปแบบให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="92213-166">เรียกใช้รูปแบบจากแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="92213-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="92213-167">เรียกใช้รูปแบบจาก ER</span><span class="sxs-lookup"><span data-stu-id="92213-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="92213-168">ตั้งค่าคอนฟิกปลายทางรูปแบบสำหรับการแสดงตัวอย่างบนหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="92213-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="92213-169">เรียกใช้รูปแบบจากแอปพลิเคชันเพื่อแสดงตัวอย่างเป็นเอกสาร PDF</span><span class="sxs-lookup"><span data-stu-id="92213-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="92213-170">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="92213-170">Additional resources</span></span>](#References)

<span data-ttu-id="92213-171">ในตัวอย่างนี้ คุณจะสร้างโซลูชัน ER ใหม่สำหรับโมดูล [แบบสอบถาม](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires)</span><span class="sxs-lookup"><span data-stu-id="92213-171">In this example, you will create a new ER solution for the [Questionnaire](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires) module.</span></span> <span data-ttu-id="92213-172">โซลูชัน ER ใหม่นี้ช่วยให้คุณสามารถออกแบบรายงานโดยใช้เวิร์กชีต Microsoft Excel เป็นเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="92213-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="92213-173">จากนั้น คุณจะสามารถสร้างรายงาน **แบบสอบถาม** ในรูปแบบ Excel หรือ PDF นอกจากนี้ เมื่อต้องการสร้างรายงาน SQL Server Reporting Services (SSRS) ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="92213-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="92213-174">นอกจากนี้ คุณยังสามารถปรับเปลี่ยนรายงานใหม่ได้ในภายหลังเมื่อมีการร้องขอ</span><span class="sxs-lookup"><span data-stu-id="92213-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="92213-175">ไม่จำเป็นต้องมีการเขียนโค้ด</span><span class="sxs-lookup"><span data-stu-id="92213-175">No coding is required.</span></span>

1. <span data-ttu-id="92213-176">เมื่อต้องการเรียกใช้รายงานที่มีอยู่ ให้ไปที่ **แบบสอบถาม** \> **ออกแบบ** \> **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![การเลือกรายการเมนูรายงานแบบสอบถามในโมดูลแบบสอบถามเพื่อเรียกใช้รายงาน SSRS ที่มีอยู่](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="92213-178">ในกล่องโต้ตอบ **รายงานแบบสอบถาม** ให้ระบุเงื่อนไขการเลือก</span><span class="sxs-lookup"><span data-stu-id="92213-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="92213-179">ใช้ตัวกรองเพื่อให้รายงานรวมเฉพาะแบบสอบถาม **SBCCrsExam** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92213-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![การระบุเงื่อนไขการเลือกในกล่องโต้ตอบรายงานแบบสอบถาม](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="92213-181">ภาพประกอบต่อไปนี้แสดงรุ่นที่สร้างขึ้นของรายงาน SSRS สำหรับแบบสอบถาม **SBCCrsExam**</span><span class="sxs-lookup"><span data-stu-id="92213-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![รายงาน SSRS ที่สร้าง](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="92213-183">ตั้งค่าคอนฟิกกรอบงาน ER</span><span class="sxs-lookup"><span data-stu-id="92213-183">Configure the ER framework</span></span>

<span data-ttu-id="92213-184">ในฐานะผู้ใช้ในบทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ คุณต้องตั้งค่าคอนฟิกชุดพารามิเตอร์ ER ที่ น้อยที่สุดก่อนที่คุณจะสามารถเริ่มต้นการใช้กรอบงาน ER เพื่อออกแบบโซลูชัน ER ใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="92213-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="92213-185">ตั้งค่าคอนฟิกพารามิเตอร์ ER</span><span class="sxs-lookup"><span data-stu-id="92213-185">Configure ER parameters</span></span>

1. <span data-ttu-id="92213-186">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="92213-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="92213-187">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="92213-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="92213-188">ในหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์** บนแท็บ **ทั่วไป** ตั้งค่าตัวเลือก **เปิดใช้งานโหมดการออกแบบ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="92213-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="92213-189">บนแท็บ **เอกสารแนบ** ให้ตั้งค่าพารามิเตอร์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="92213-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="92213-190">ตั้งค่าฟิลด์ **การตั้งค่าคอนฟิก** เป็น **ไฟล์** สำหรับบริษัท **USMF**</span><span class="sxs-lookup"><span data-stu-id="92213-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="92213-191">ตั้งค่าฟิลด์ **ที่เก็บงานถาวร** **ชั่วคราว** **พื้นฐาน** และ **อื่นๆ** เป็น **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="92213-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="92213-192">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับพารามิเตอร์ ER ให้ดูที่ [ตั้งค่าคอนฟิกกรอบงาน ER](electronic-reporting-er-configure-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="92213-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="92213-193">เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="92213-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="92213-194">มีการทำเครื่องหมายการตั้งค่าคอนฟิก ER ทั้งหมดที่เป็นเจ้าของโดยผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="92213-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="92213-195">ดังนั้นคุณต้องเรียกใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ก่อนที่คุณจะเริ่มต้นการเพิ่มหรือแก้ไขการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="92213-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="92213-196">เฉพาะเจ้าของที่มีการตั้งค่าคอนฟิก ER เท่านั้นที่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="92213-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="92213-197">ดังนั้นก่อนที่จะแก้ไขการตั้งค่าคอนฟิก ER ต้องมีการเรียกใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="92213-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="92213-198">ตรวจทานรายการของผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="92213-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="92213-199">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="92213-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="92213-200">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ในส่วน **ลิงค์ที่เกี่ยวข้อง** ให้เลือก **ผู้ให้บริการการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="92213-201">บนหน้า **ผู้ให้บริการการตั้งค่าคอนฟิก** แต่ละเรกคอร์ดผู้ให้บริการการตั้งค่าคอนฟิกจะมีชื่อและ URL ที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="92213-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="92213-202">ตรวจทานเนื้อหาของหน้านี้</span><span class="sxs-lookup"><span data-stu-id="92213-202">Review the contents of this page.</span></span> <span data-ttu-id="92213-203">ถ้ามีเรกคอร์ดสำหรับ **Litware, inc.** (`https://www.litware.com`) อยู่แล้ว ให้ข้ามขั้นตอนถัดไป [เพิ่มผู้ให้บริการการตั้งค่าคอนฟิก ER ใหม่](#ActivateProvider)</span><span class="sxs-lookup"><span data-stu-id="92213-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="92213-204">เพิ่มผู้ให้บริการการตั้งค่าคอนฟิก ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="92213-205">ในหน้า **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="92213-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="92213-206">ในฟิลด์ **ชื่อ** ให้ป้อน **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="92213-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="92213-207">ในฟิลด์ **ที่อยู่อินเทอร์เน็ต** ให้ป้อน `https://www.litware.com`</span><span class="sxs-lookup"><span data-stu-id="92213-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="92213-208">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="92213-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="92213-209">เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="92213-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="92213-210">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="92213-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="92213-211">ในพื้นที่ทำงาน **การรายงานอิเล็กทรอนิกส์** ให้เลือกผู้ให้บริการการตั้งค่าคอนฟิก **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="92213-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="92213-212">เลือก **กำหนดเป็นใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="92213-212">Select **Set active**.</span></span>

<span data-ttu-id="92213-213">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับผู้ให้บริการการตั้งค่าคอนฟิก ER ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="92213-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="92213-214">ออกแบบรูปแบบข้อมูลเฉพาะโดเมน</span><span class="sxs-lookup"><span data-stu-id="92213-214">Design a domain-specific data model</span></span>

<span data-ttu-id="92213-215">คุณต้องสร้างการตั้งค่าคอนฟิก ER ใหม่ที่มีส่วนประกอบ [รูปแบบข้อมูลl](general-electronic-reporting.md#data-model-and-model-mapping-components) สำหรับโดเมนธุรกิจ **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="92213-216">รูปแบบข้อมูลนี้จะใช้เป็นแหล่งข้อมูลในภายหลังเมื่อคุณออกแบบรูปแบบ ER เพื่อสร้างรายงาน **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="92213-217">เมื่อดำเนินการขั้นตอนนี้ในส่วน [นำเข้าการตั้งค่าคอนฟิกรูปแบบข้อมูลใหม่](#ImportDataModel) แล้ว คุณสามารถนำเข้ารูปแบบข้อมูลที่จำเป็นจากไฟล์ XML ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="92213-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="92213-218">อีกทางหนึ่งคือ คุณสามารถทำขั้นตอนนี้ให้เสร็จสมบูรณ์ได้ในส่วน [สร้างการตั้งค่าคอนฟิกรูปแบบข้อมูลใหม่](#DesignDataModel) เพื่อออกแบบรูปแบบข้อมูลนี้ตั้งแต่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="92213-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="92213-219">นำเข้าการตั้งค่าคอนฟิกรูปแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="92213-220">ดาวน์โหลดไฟล์ [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) และบันทึกไปยังคอมพิวเตอร์เฉพาะที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="92213-220">Download the [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="92213-221">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="92213-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="92213-222">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="92213-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="92213-223">ในบานหน้าต่างการดำเนินการ เลือก **แลกเปลี่ยน** \> **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="92213-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="92213-224">เลือก **เรียกดู** แล้วค้นหาและเลือกไฟล์ **Questionnaires model.version.1.xml**</span><span class="sxs-lookup"><span data-stu-id="92213-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="92213-225">เลือก **ตกลง** เพื่อนำเข้าการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="92213-226">เมื่อต้องการดำเนินการต่อ ให้ข้ามขั้นตอนถัดไป [สร้างการตั้งค่าคอนฟิกรูปแบบข้อมูลใหม่](#DesignDataModel)</span><span class="sxs-lookup"><span data-stu-id="92213-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="92213-227">สร้างการตั้งค่าคอนฟิกรูปแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="92213-228">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="92213-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="92213-229">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="92213-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="92213-230">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="92213-231">ในกล่องโต้ตอบรายการแบบหล่นลง ในฟิลด์ **ชื่อ** ให้ป้อน **รูปแบบแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="92213-232">เลือก **สร้างการตั้งค่าคอนฟิก** เพื่อสร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="92213-233">ตั้งชื่อรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-233">Name the data model</span></span>

1. <span data-ttu-id="92213-234">ในหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="92213-235">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="92213-235">Select **Designer**.</span></span>
3. <span data-ttu-id="92213-236">บนหน้า **ตัวออกแบบรูปแบบข้อมูล** บนแท็บด่วน **ทั่วไป** ในฟิลด์ **ชื่อ** ให้ป้อน <a name="DataModeName"></a>**แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="92213-237">เพิ่มฟิลด์รูปแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-237">Add new data model fields</span></span>

1. <span data-ttu-id="92213-238">ในหน้า **ตัวออกแบบรูปแบบข้อมูล** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="92213-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="92213-239">ในกล่องโต้ตอบแบบหล่นลงสำหรับการเพิ่มโหนดรูปแบบข้อมูล ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="92213-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="92213-240">เลือก **รากของรูปแบบ** เป็นชนิดโหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="92213-241">ในฟิลด์ **ชื่อ** ให้ป้อน <a name="RootDefinitionName"></a>**ราก**</span><span class="sxs-lookup"><span data-stu-id="92213-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="92213-242">เลือก **เพิ่ม** เพื่อเพิ่มโหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="92213-243">ตัวอธิบายรากนี้จะใช้เพื่อให้ข้อมูลสำหรับรายงาน **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="92213-244">รูปแบบข้อมูลเดียวสามารถมีตัวอธิบายได้หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="92213-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="92213-245">คุณสามารถระบุตัวอธิบายแต่ละตัวสำหรับรูปแบบ ER เดียวเพื่อระบุข้อมูลที่จำเป็นในการสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="92213-246">เลือก **สร้าง** อีกครั้ง จากนั้นในกล่องโต้ตอบแบบหล่นลงสำหรับการเพิ่มโหนดรูปแบบข้อมูล ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="92213-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="92213-247">เลือก **รายการรองของโหนดที่ใช้งานอยู่** เป็นชนิดโหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="92213-248">ในฟิลด์ **ชื่อ** ให้ป้อน **ชื่อบริษัท**</span><span class="sxs-lookup"><span data-stu-id="92213-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="92213-249">ในฟิลด์ **ประเภทรายการ** ให้เลือก **สตริง**</span><span class="sxs-lookup"><span data-stu-id="92213-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="92213-250">เลือก **เพิ่ม** เพื่อเพิ่มฟิลด์ใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="92213-251">ฟิลด์นี้จำเป็นต้องใช้ในการส่งชื่อของบริษัทปัจจุบันไปยังรายงาน ER ซึ่งจะใช้รูปแบบข้อมูลนี้เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="92213-252">เลือก **สร้าง** อีกครั้ง จากนั้นในกล่องโต้ตอบแบบหล่นลงสำหรับการเพิ่มโหนดรูปแบบข้อมูล ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="92213-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="92213-253">เลือก **รายการรองของโหนดที่ใช้งานอยู่** เป็นชนิดโหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="92213-254">ในฟิลด์ **ชื่อ** ให้ป้อน **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="92213-255">ในฟิลด์ **ประเภทรายการ** ให้เลือก **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="92213-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="92213-256">เลือก **เพิ่ม** เพื่อเพิ่มฟิลด์ใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="92213-257">ฟิลด์นี้จะต้องใช้ในการส่งรายการของแบบสอบถามไปยังรายงาน ER ซึ่งจะใช้รูปแบบข้อมูลนี้เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="92213-258">เลือกโหนด **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="92213-259">ดำเนินการต่อเพื่อเพิ่มฟิลด์ที่จำเป็นของรูปแบบข้อมูลที่สามารถแก้ไขได้ในลักษณะเดียวกันจนกว่าคุณจะกรอกข้อมูลโครงสร้างรูปแบบข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="92213-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="92213-260">พาธของฟิลด์</span><span class="sxs-lookup"><span data-stu-id="92213-260">Field path</span></span>                                                    | <span data-ttu-id="92213-261">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-261">Data type</span></span>   | <span data-ttu-id="92213-262">การกำหนดฟิลด์/ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="92213-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="92213-263">ราก</span><span class="sxs-lookup"><span data-stu-id="92213-263">Root</span></span>                                                          |             | <span data-ttu-id="92213-264">จุดอ้างอิงที่จะร้องขอข้อมูลแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="92213-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="92213-265">Root\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="92213-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="92213-266">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-266">String</span></span>      | <span data-ttu-id="92213-267">ชื่อของบริษัทปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-267">The name of the current company.</span></span> |
    | <span data-ttu-id="92213-268">Root\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="92213-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="92213-269">เรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="92213-269">Record</span></span>      | <span data-ttu-id="92213-270">รายละเอียดการดำเนินการรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-270">Format execution details.</span></span> |
    | <span data-ttu-id="92213-271">Root\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="92213-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="92213-272">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-272">String</span></span>      | <span data-ttu-id="92213-273">ชื่อของรูปแบบ ER ที่กำลังทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="92213-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="92213-274">Root\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="92213-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="92213-275">รายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="92213-275">Record list</span></span> | <span data-ttu-id="92213-276">รายการของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="92213-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="92213-277">Root\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="92213-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="92213-278">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-278">String</span></span>      | <span data-ttu-id="92213-279">สถานะของแบบสอบถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="92213-280">Root\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="92213-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="92213-281">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-281">String</span></span>      | <span data-ttu-id="92213-282">โค้ดของแบบสอบถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="92213-283">Root\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="92213-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="92213-284">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-284">String</span></span>      | <span data-ttu-id="92213-285">คำอธิบายของแบบสอบถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="92213-286">Root\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="92213-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="92213-287">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-287">String</span></span>      | <span data-ttu-id="92213-288">ชนิดของแบบสอบถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="92213-289">Root\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="92213-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="92213-290">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-290">String</span></span>      | <span data-ttu-id="92213-291">ลำดับตัวเลขของแบบสอบถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="92213-292">Root\\Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="92213-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="92213-293">เรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="92213-293">Record</span></span>      | <span data-ttu-id="92213-294">พารามิเตอร์ที่เป็นผลลัพธ์ของแบบสอบถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="92213-295">Root\\Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="92213-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="92213-296">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-296">String</span></span>      | <span data-ttu-id="92213-297">รหัสระบุของกลุ่มผลลัพธ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="92213-298">Root\\Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="92213-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="92213-299">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-299">String</span></span>      | <span data-ttu-id="92213-300">คำอธิบายของกลุ่มผลลัพธ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="92213-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="92213-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="92213-302">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="92213-302">Real</span></span>        | <span data-ttu-id="92213-303">จำนวนคะแนนสูงสุดที่สามารถได้รับ</span><span class="sxs-lookup"><span data-stu-id="92213-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="92213-304">Root\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="92213-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="92213-305">รายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="92213-305">Record list</span></span> | <span data-ttu-id="92213-306">รายการของคำถามสำหรับแบบสอบถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="92213-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="92213-308">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="92213-308">Integer</span></span>     | <span data-ttu-id="92213-309">หมายเลขลำดับของชุดคำตอบปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="92213-310">Root\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="92213-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="92213-311">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-311">String</span></span>      | <span data-ttu-id="92213-312">รหัสระบุของคำถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="92213-313">Root\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="92213-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="92213-314">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-314">String</span></span>      | <span data-ttu-id="92213-315">แฟล็กที่แสดงว่าต้องมีการตอบคำถามปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="92213-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="92213-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="92213-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="92213-317">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-317">String</span></span>      | <span data-ttu-id="92213-318">แฟล็กที่แสดงว่าต้องคำถามปัจจุบันเป็นรายการหลักหรือไม่</span><span class="sxs-lookup"><span data-stu-id="92213-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="92213-319">Root\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="92213-320">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="92213-320">Integer</span></span>     | <span data-ttu-id="92213-321">หมายเลขลำดับของคำถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="92213-322">Root\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="92213-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="92213-323">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-323">String</span></span>      | <span data-ttu-id="92213-324">ข้อความของคำถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-324">The text of the current question.</span></span> |
    | <span data-ttu-id="92213-325">Root\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="92213-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="92213-326">รายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="92213-326">Record list</span></span> | <span data-ttu-id="92213-327">รายการของคำตอบสำหรับคำถามปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="92213-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="92213-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="92213-329">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-329">String</span></span>      | <span data-ttu-id="92213-330">แฟล็กที่แสดงว่าคำตอบปัจจุบันถูกต้องหรือไม่</span><span class="sxs-lookup"><span data-stu-id="92213-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="92213-331">Root\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="92213-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="92213-332">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="92213-332">Real</span></span>        | <span data-ttu-id="92213-333">คะแนนที่ทำได้เมื่อมีการเลือกคำตอบปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="92213-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="92213-335">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="92213-335">Integer</span></span>     | <span data-ttu-id="92213-336">หมายเลขลำดับของคำตอบปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="92213-337">Root\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="92213-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="92213-338">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-338">String</span></span>      | <span data-ttu-id="92213-339">ข้อความของคำตอบปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-339">The text of the current answer.</span></span> |

    <span data-ttu-id="92213-340">ภาพประกอบต่อไปนี้แสดงรูปแบบข้อมูลที่สามารถแก้ไขที่เสร็จสมบูรณ์บนหน้า **ตัวออกแบบรูปแบบข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="92213-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![รูปแบบข้อมูลที่ตั้งค่าคอนฟิกในตัวออกแบบรูปแบบข้อมูล ER](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="92213-342">บันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="92213-342">Save your changes.</span></span>
8. <span data-ttu-id="92213-343">ปิดหน้า **ตัวออกแบบรูปแบบข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="92213-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="92213-344">ทำการออกแบบของรูปแบบข้อมูลให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="92213-345">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="92213-346">ในหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="92213-347">บนแท็บด่วน **รุ่น** ให้เลือกรุ่นการตั้งค่าคอนฟิกที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="92213-348">เลือก **เปลี่ยนแปลงสถานะ** \> **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="92213-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="92213-349">สถานะของรุ่น 1 ของการตั้งค่าคอนฟิกนี้มีการเปลี่ยนแปลงจาก **แบบร่าง** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="92213-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="92213-350">รุ่น 1 ไม่สามารถเปลี่ยนแปลงได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="92213-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="92213-351">รุ่นนี้มีรูปแบบข้อมูลที่ตั้งค่าคอนฟิกและสามารถใช้เป็นข้อมูลพื้นฐานสำหรับการตั้งค่าคอนฟิก ER อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="92213-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="92213-352">รุ่น 2 ของการตั้งค่าคอนฟิกนี้จะถูกสร้างขึ้นและมีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="92213-353">คุณสามารถแก้ไขรุ่นนี้เพื่อปรับปรุงรูปแบบข้อมูล **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![รุ่นของการตั้งค่าคอนฟิก ER ที่แก้ไขได้บนหน้าการตั้งค่าคอนฟิก](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="92213-355">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการกำหนดรุ่นสำหรับการตั้งค่าคอนฟิก ER โปรดดู [ภาพรวมของการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md#component-versioning)</span><span class="sxs-lookup"><span data-stu-id="92213-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="92213-356">รูปแบบข้อมูลที่ตั้งค่าคอนฟิกเป็นการแสดงเชิงนามธรรมของโดเมนธุรกิจ **แบบสอบถาม** และไม่มีความสัมพันธ์กับอาร์ทิแฟกต์ที่เกี่ยวข้องกับ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="92213-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="92213-357">ออกแบบการแม็ปรูปแบบสำหรับรูปแบบข้อมูลที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="92213-358">ในฐานะผู้ใช้ในบทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ คุณต้องสร้างการตั้งค่าคอนฟิก ER ใหม่ที่มีส่วนประกอบของ [การแม็ปรูปแบบ](general-electronic-reporting.md#data-model-and-model-mapping-components) สำหรับรูปแบบข้อมูล **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="92213-359">เนื่องจากส่วนประกอบนี้ใช้รูปแบบข้อมูลที่ตั้งค่าคอนฟิกสำหรับ Finance จึงใช้เฉพาะกับ Finance</span><span class="sxs-lookup"><span data-stu-id="92213-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="92213-360">คุณต้องตั้งค่าคอนฟิกส่วนประกอบของการแม็ปรูปแบบเพื่อระบุออบเจ็กต์ของแอปพลิเคชันที่ต้องใช้ในการกรอกข้อมูลในรูปแบบข้อมูลที่ตั้งค่าคอนฟิกด้วยข้อมูลแอปพลิเคชันขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="92213-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="92213-361">เมื่อต้องการทำงานนี้ให้เสร็จสมบูรณ์ คุณต้องทราบรายละเอียดการดำเนินการของโครงสร้างข้อมูลของโดเมนธุรกิจ **แบบสอบถาม** ใน Finance</span><span class="sxs-lookup"><span data-stu-id="92213-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="92213-362">เมื่อดำเนินการขั้นตอนนี้ในส่วน [นำเข้าการตั้งค่าคอนฟิกการแม็ปรูปแบบใหม่](#ImportModelMapping) แล้ว คุณสามารถนำเข้าการตั้งค่าคอนฟิกการแม็ปรูปแบบที่จำเป็นจากไฟล์ XML ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="92213-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="92213-363">อีกทางหนึ่งคือ คุณสามารถทำขั้นตอนนี้ให้เสร็จสมบูรณ์ได้ในส่วน [สร้างการตั้งค่าคอนฟิกการแม็ปรูปแบบใหม่](#CreateModelMapping) เพื่อออกแบบการแม็ปรูปแบบนี้ตั้งแต่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="92213-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="92213-364">นำเข้าการตั้งค่าคอนฟิกการแม็ปรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="92213-365">ดาวน์โหลดไฟล์ [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) และบันทึกไปยังคอมพิวเตอร์เฉพาะที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="92213-365">Download the [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="92213-366">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="92213-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="92213-367">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="92213-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="92213-368">ในบานหน้าต่างการดำเนินการ เลือก **แลกเปลี่ยน** \> **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="92213-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="92213-369">เลือก **เรียกดู** แล้วค้นหาและเลือกไฟล์ **Questionnaires mapping.version.1.1.xml**</span><span class="sxs-lookup"><span data-stu-id="92213-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="92213-370">เลือก **ตกลง** เพื่อนำเข้าการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="92213-371">เมื่อต้องการดำเนินการต่อ ให้ข้ามขั้นตอนถัดไป [สร้างการตั้งค่าคอนฟิกการแม็ปรูปแบบใหม่](#CreateModelMapping)</span><span class="sxs-lookup"><span data-stu-id="92213-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="92213-372">สร้างการตั้งค่าคอนฟิกการแม็ปรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="92213-373">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="92213-374">ในหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="92213-375">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="92213-376">ในกล่องโต้ตอบรายการแบบหล่นลง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="92213-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="92213-377">ในฟิลด์ **สร้าง** เลือก **การแม็ปรูปแบบตามแบบสอบถามรูปแบบข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="92213-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="92213-378">ในฟิลด์ **ชื่อ** ให้ป้อน **การแม็ปแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="92213-379">ในฟิลด์ **ข้อกำหนดของรูปแบบข้อมูล** ให้เลือกข้อกำหนด **ราก**</span><span class="sxs-lookup"><span data-stu-id="92213-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="92213-380">เลือก **สร้างการตั้งค่าคอนฟิก** เพื่อสร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="92213-381">ออกแบบส่วนประกอบการแม็ปรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="92213-382">ในหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ปแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="92213-383">เลือก **ตัวออกแบบ** เพื่อเปิดรายการของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="92213-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="92213-384">เลือก **การแม็ปแบบสอบถาม** ที่ถูกเพิ่มโดยอัตโนมัติสำหรับข้อกำหนด **ราก**</span><span class="sxs-lookup"><span data-stu-id="92213-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="92213-385">เลือก **ตัวออกแบบ** เพื่อเริ่มต้นการตั้งค่าคอนฟิกการแม็ปที่เลือก</span><span class="sxs-lookup"><span data-stu-id="92213-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="92213-386">การแม็ปใหม่จะถูกเพิ่มโดยอัตโนมัติสำหรับข้อกำหนด **ราก**</span><span class="sxs-lookup"><span data-stu-id="92213-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="92213-387">การแม็ปนี้มีทิศทาง **ไปยังรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="92213-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="92213-388">การแม็ปนี้สามารถใช้ในการกรอกข้อมูลในรูปแบบข้อมูลด้วยข้อมูลที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="92213-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="92213-389">เพิ่มแหล่งข้อมูลที่จะเข้าถึงตารางแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="92213-389">Add data sources to access application tables</span></span>

<span data-ttu-id="92213-390">คุณต้องตั้งค่าคอนฟิกแหล่งข้อมูลที่จะเข้าถึงตารางแอปพลิเคชันที่มีรายละเอียดของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="92213-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="92213-391">บนหน้า **ตัวออกแบบการแม็ปรูปแบบ** ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** เลือก **Dynamics 365 for Operations\\เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="92213-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="92213-392">เพิ่มแหล่งข้อมูลใหม่ที่จะใช้ในการเข้าถึงตาราง KMCollection ซึ่งเรกคอร์ดทั้งหมดแสดงถึงแบบสอบถามเดียว:</span><span class="sxs-lookup"><span data-stu-id="92213-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="92213-393">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="92213-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="92213-394">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="92213-395">ในฟิลด์ **ตาราง** ให้ป้อน **KMCollection**</span><span class="sxs-lookup"><span data-stu-id="92213-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="92213-396">ตั้งค่าตัวเลือก **ขอการสอบถาม** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="92213-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="92213-397">จากนั้นคุณจะสามารถระบุตัวเลือก [การกรอง](../../fin-ops/get-started/advanced-filtering-query-options.md) สำหรับตารางนี้ในกล่องโต้ตอบการสอบถามระบบขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="92213-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="92213-398">เลือก **ตกลง** เพื่อเพิ่มแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="92213-399">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้เลือก **Dynamics 365 for Operations\\เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="92213-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="92213-400">เพิ่มแหล่งข้อมูลใหม่ที่จะใช้ในการเข้าถึงตาราง KMQuestion ซึ่งเรกคอร์ดทั้งหมดแสดงถึงคำถามเดียวในแบบสอบถาม:</span><span class="sxs-lookup"><span data-stu-id="92213-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="92213-401">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="92213-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="92213-402">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **คำถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="92213-403">ในฟิลด์ **ตาราง** ให้ป้อน **KMQuestion**</span><span class="sxs-lookup"><span data-stu-id="92213-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="92213-404">เลือก **ตกลง** เพื่อเพิ่มแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="92213-405">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้เลือก **Dynamics 365 for Operations\\เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="92213-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="92213-406">เพิ่มแหล่งข้อมูลใหม่ที่จะใช้ในการเข้าถึงตาราง KMAnswer ซึ่งเรกคอร์ดทั้งหมดแสดงถึงคำตอบเดียวของคำถามในแบบสอบถาม:</span><span class="sxs-lookup"><span data-stu-id="92213-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="92213-407">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="92213-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="92213-408">ในฟิลด์ **ชื่อ** ให้ป้อน **คำตอบ**</span><span class="sxs-lookup"><span data-stu-id="92213-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="92213-409">ในฟิลด์ **ตาราง** ให้ป้อน **KMAnswer**</span><span class="sxs-lookup"><span data-stu-id="92213-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="92213-410">เลือก **ตกลง** เพื่อเพิ่มแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="92213-411">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** เลือก **ฟังก์ชัน\\ฟิลด์ที่คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="92213-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="92213-412">เพิ่มฟิลด์ที่คำนวณใหม่ซึ่งจะใช้ในการเข้าถึงเรกคอร์ดของตาราง KMQuestionResultGroup จากเรกคอร์ดทั้งหมดของตาราง KMCollection หลัก:</span><span class="sxs-lookup"><span data-stu-id="92213-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="92213-413">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="92213-414">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="92213-414">Select **Add**.</span></span>
    3. <span data-ttu-id="92213-415">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ป้อน **\$ResultGroup**</span><span class="sxs-lookup"><span data-stu-id="92213-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="92213-416">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="92213-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="92213-417">ใน [ตัวแก้ไขสูตร ER](general-electronic-reporting-formula-designer.md) ในฟิลด์ **สูตร** ป้อน **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** เพื่อใช้ [พาธ](er-formula-language.md#paths) ของความสัมพันธ์แบบหนึ่งต่อกลุ่มระหว่างตาราง KMCollection และ KMQuestionResultGroup</span><span class="sxs-lookup"><span data-stu-id="92213-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="92213-418">เลือก **ตกลง** และปิดตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="92213-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="92213-419">เลือก **ตกลง** เพื่อเพิ่มฟิลด์ที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="92213-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="92213-420">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** เลือก **ฟังก์ชัน\\ฟิลด์ที่คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="92213-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="92213-421">เพิ่มฟิลด์ที่คำนวณใหม่ซึ่งจะใช้ในการเข้าถึงเรกคอร์ดขคำถามองตาราง KMQuestion จากเรกคอร์ดทั้งหมดของตาราง KMCollectionQuestion หลัก:</span><span class="sxs-lookup"><span data-stu-id="92213-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="92213-422">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="92213-423">ขยายโหนด **\<ความสัมพันธ์** ที่มีความสัมพันธ์แบบหนึ่งต่อกลุ่มของตาราง KMCollection</span><span class="sxs-lookup"><span data-stu-id="92213-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="92213-424">เลือกตาราง **KMCollectionQuestion** ที่เกี่ยวข้อง และเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="92213-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="92213-425">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ป้อน **\$คำถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="92213-426">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="92213-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="92213-427">ในตัวแก้ไขสูตร ในฟิลด์ **สูตร** ป้อน **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** เพื่อส่งคืนเรกคอร์ดคำถามที่เหมาะสมจากตาราง KMQuestion</span><span class="sxs-lookup"><span data-stu-id="92213-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="92213-428">เลือก **ตกลง** และปิดตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="92213-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="92213-429">เลือก **ตกลง** เพื่อเพิ่มฟิลด์ที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="92213-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="92213-430">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** เลือก **ฟังก์ชัน\\ฟิลด์ที่คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="92213-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="92213-431">เพิ่มฟิลด์ที่คำนวณใหม่ซึ่งจะใช้ในการเข้าถึงเรกคอร์ดคำตอบของตาราง KMAnswer จากเรกคอร์ดทั้งหมดของตาราง KMQuestion หลัก:</span><span class="sxs-lookup"><span data-stu-id="92213-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="92213-432">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **แบบสอบถาม\<Relations.KMCollectionQuestion.\$คำถาม** แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="92213-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="92213-433">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ป้อน **\$คำตอบ**</span><span class="sxs-lookup"><span data-stu-id="92213-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="92213-434">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="92213-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="92213-435">ในตัวแก้ไขสูตร ในฟิลด์ **สูตร** ป้อน **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** เพื่อส่งคืนเรกคอร์ดคำตอบที่เหมาะสมจากตาราง KMAnswer</span><span class="sxs-lookup"><span data-stu-id="92213-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="92213-436">เลือก **ตกลง** และปิดตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="92213-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="92213-437">เลือก **ตกลง** เพื่อเพิ่มฟิลด์ที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="92213-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="92213-438">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้เลือก **Dynamics 365 for Operations\\ตาราง**</span><span class="sxs-lookup"><span data-stu-id="92213-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="92213-439">เพิ่มแหล่งข้อมูลใหม่ที่จะใช้ในการเข้าถึงวิธีการของตาราง CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="92213-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="92213-440">โปรดสังเกตว่าเมธอด **find()** ของตารางนี้จะส่งคืนเรกคอร์ดซึ่งแสดงถึงบริษัทของอินสแตนซ์ Finance ปัจจุบันที่มีการเรียกการแม็ปนี้ไว้ในบริบท</span><span class="sxs-lookup"><span data-stu-id="92213-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="92213-441">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="92213-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="92213-442">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **CompanyInfo**</span><span class="sxs-lookup"><span data-stu-id="92213-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="92213-443">ในฟิลด์ **ตาราง** ให้ป้อน **CompanyInfo**</span><span class="sxs-lookup"><span data-stu-id="92213-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="92213-444">เลือก **ตกลง** เพื่อเพิ่มแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="92213-445">เพิ่มแหล่งข้อมูลที่จะเข้าถึงการแจงนับแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="92213-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="92213-446">คุณต้องตั้งค่าคอนฟิกแหล่งข้อมูลในการเข้าถึงการแจงนับของแอปพลิเคชันและเปรียบเทียบค่ากับค่าของฟิลด์ชนิด **การแจงนับ** ในตารางของแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="92213-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="92213-447">คุณต้องใช้ผลลัพธ์ของการเปรียบเทียบเพื่อกรอกข้อมูลในฟิลด์ที่เหมาะสมของรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="92213-448">บนหน้า **ตัวออกแบบการแม็ปรูปแบบ** ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** เลือก **Dynamics 365 for Operations\\การแจงนับ**</span><span class="sxs-lookup"><span data-stu-id="92213-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="92213-449">เพิ่มแหล่งข้อมูลใหม่ที่จะใช้ในการเข้าถึงค่าของการแจงนับ **EnumAppNoYes**:</span><span class="sxs-lookup"><span data-stu-id="92213-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="92213-450">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="92213-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="92213-451">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **EnumAppNoYes**</span><span class="sxs-lookup"><span data-stu-id="92213-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="92213-452">ในฟิลด์ **การแจงนับ** ป้อน **NoYes**</span><span class="sxs-lookup"><span data-stu-id="92213-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="92213-453">เลือก **ตกลง** เพื่อเพิ่มแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="92213-454">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้เลือก **Dynamics 365 for Operations\\การแจงนับ**</span><span class="sxs-lookup"><span data-stu-id="92213-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="92213-455">เพิ่มแหล่งข้อมูลใหม่ที่จะใช้ในการเข้าถึงค่าของการแจงนับ **KMCollectionQuestionMode**:</span><span class="sxs-lookup"><span data-stu-id="92213-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="92213-456">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="92213-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="92213-457">ในกล่องโต้ตอบรายการแบบหล่นลง ในฟิลด์ **ชื่อ** ให้ป้อน **EnumAppQuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="92213-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="92213-458">ในฟิลด์ **การแจงนับ** ป้อน **KMCollectionQuestionMode**</span><span class="sxs-lookup"><span data-stu-id="92213-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="92213-459">เลือก **ตกลง** เพื่อเพิ่มแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="92213-460">เพิ่มป้ายชื่อ ER เพื่อสร้างรายงานในภาษาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="92213-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="92213-461">คุณสามารถเพิ่มป้ายชื่อ ER เพื่อตั้งค่าคอนฟิกแหล่งข้อมูลบางอย่างที่จะส่งคืนค่าที่ขึ้นอยู่กับภาษาที่กำหนดไว้ในบริบทของการเรียกของการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="92213-462">บนหน้า **วออกแบบการแม็ปรูปแบบ** ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **คำตอบ** แล้วเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="92213-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="92213-463">เปิดใช้งานฟิลด์ **ป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="92213-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="92213-464">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="92213-464">Select **Translate**.</span></span>
4. <span data-ttu-id="92213-465">ในกล่องโต้ตอบ **การแปลข้อความ** ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="92213-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="92213-466">ในฟิลด์ **รหัสป้ายชื่อ** ป้อน **PositiveAnswer**</span><span class="sxs-lookup"><span data-stu-id="92213-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="92213-467">ในฟิลด์ **ข้อความในภาษาเริ่มต้น** ให้ป้อน **ใช่**</span><span class="sxs-lookup"><span data-stu-id="92213-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="92213-468">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="92213-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="92213-469">ในฟิลด์ **รหัสป้ายชื่อ** ป้อน **NegativeAnswer**</span><span class="sxs-lookup"><span data-stu-id="92213-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="92213-470">ในฟิลด์ **ข้อความในภาษาเริ่มต้น** ให้ป้อน **ไม่**</span><span class="sxs-lookup"><span data-stu-id="92213-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="92213-471">เลือก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="92213-471">Select **Translate**.</span></span>

5. <span data-ttu-id="92213-472">ปิดกล่องโต้ตอบ **การแปลข้อความ**</span><span class="sxs-lookup"><span data-stu-id="92213-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="92213-473">เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="92213-473">Select **Cancel**.</span></span>

![การเพิ่มป้ายชื่อ ER สำหรับการแม็ปรูปแบบที่แก้ไขได้](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="92213-475">คุณได้ป้อนป้ายชื่อ ER เฉพาะสำหรับภาษาเริ่มต้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92213-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="92213-476">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการแปลป้ายชื่อ ER เป็นภาษาอื่นๆ ให้ดูที่ [ออกแบบรายงานหลายภาษา](er-design-multilingual-reports.md)</span><span class="sxs-lookup"><span data-stu-id="92213-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="92213-477">เพิ่มแหล่งข้อมูลเพื่อแปลงผลลัพธ์ของการเปรียบเทียบค่าการแจงนับเป็นค่าข้อความ</span><span class="sxs-lookup"><span data-stu-id="92213-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="92213-478">เนื่องจากคุณต้องแปลงผลลัพธ์ของการเปรียบเทียบระหว่างค่าการแจงนับและค่าข้อความหลายครั้งสำหรับแหล่งที่มาของความแตกต่าง จึงควรตั้งค่าคอนฟิกตรรกะนี้เป็นแหล่งข้อมูลเดียว</span><span class="sxs-lookup"><span data-stu-id="92213-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="92213-479">อย่างไรก็ตาม เมื่อต้องการทำให้แหล่งข้อมูลนี้ใช้ใหม่ได้ คุณต้องตั้งค่าคอนฟิกให้เป็นแหล่งข้อมูลที่กำหนดเป็นพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="92213-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="92213-480">สำหรับข้อมูลเพิ่มเติม ดูที่ [สนับสนุนการเรียกแบบใช้พารามิเตอร์ของแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ของชนิดฟิลด์ที่คำนวณได้](er-calculated-field-type.md)</span><span class="sxs-lookup"><span data-stu-id="92213-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="92213-481">บนหน้า **ตัวออกแบบการแม็ปรูปแบบ** ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** เลือก **ทั่วไป\\คอนเทนเนอร์ที่ว่างเปล่า**</span><span class="sxs-lookup"><span data-stu-id="92213-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="92213-482">เพิ่มแหล่งข้อมูลคอนเทนเนอร์ใหม่:</span><span class="sxs-lookup"><span data-stu-id="92213-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="92213-483">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="92213-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="92213-484">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **ตัวช่วย**</span><span class="sxs-lookup"><span data-stu-id="92213-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="92213-485">เลือก **ตกลง** เพื่อเพิ่มแหล่งข้อมูลคอนเทนเนอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="92213-486">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** เลือก **ฟังก์ชัน\\ฟิลด์ที่คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="92213-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="92213-487">เพิ่มแหล่งข้อมูลใหม่:</span><span class="sxs-lookup"><span data-stu-id="92213-487">Add a new data source:</span></span>

    1. <span data-ttu-id="92213-488">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **ตัวช่วย**</span><span class="sxs-lookup"><span data-stu-id="92213-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="92213-489">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="92213-489">Select **Add**.</span></span>
    3. <span data-ttu-id="92213-490">ในกล่องโต้ตอบรายการแบบหล่นลง ในฟิลด์ **ชื่อ** ให้ป้อน **NoYesEnumToString**</span><span class="sxs-lookup"><span data-stu-id="92213-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="92213-491">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="92213-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="92213-492">ในตัวแก้ไขสูตร ให้เลือก **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="92213-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="92213-493">ทำตามขั้นตอนเหล่านี้เพื่อระบุพารามิเตอร์สำหรับนิพจน์ที่ตั้งค่าคอนฟิก:</span><span class="sxs-lookup"><span data-stu-id="92213-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="92213-494">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="92213-494">Select **New**.</span></span>
        2. <span data-ttu-id="92213-495">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **อาร์กิวเมนต์**</span><span class="sxs-lookup"><span data-stu-id="92213-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="92213-496">ในฟิลด์ **ชนิด** เลือกชนิดข้อมูล **แบบบูลีน**</span><span class="sxs-lookup"><span data-stu-id="92213-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="92213-497">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="92213-497">Select **OK**.</span></span>

    7. <span data-ttu-id="92213-498">ในฟิลด์ **สูตร** ป้อน **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** เพื่อส่งคืนข้อความของป้ายชื่อ ER ที่เหมาะสม ทั้งนี้ขึ้นอยู่กับภาษาของบริบทการดำเนินการและค่าของพารามิเตอร์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="92213-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="92213-499">เลือก **ตกลง** และปิดตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="92213-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="92213-500">เลือก **ตกลง** เพื่อเพิ่มแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-500">Select **OK** to add the new data source.</span></span>

![การแม็ปรูปแบบที่ตั้งค่าคอนฟิกในตัวออกแบบการแม็ปรูปแบบ ER](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="92213-502">ผูกแหล่งข้อมูลเข้ากับฟิลด์รูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="92213-503">คุณต้องผูกแหล่งข้อมูลที่ตั้งค่าคอนฟิกเข้ากับฟิลด์ของรูปแบบข้อมูลเพื่อระบุวิธีการกรอกข้อมูลของรูปแบบข้อมูลโดยใช้ข้อมูลในแอปพลิเคชันขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="92213-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="92213-504">บนหน้า **ตัวออกแบบการแม็ปรูปแบบ** ในบานหน้าต่าง **รูปแบบข้อมูล** เลือก **CompanyName**</span><span class="sxs-lookup"><span data-stu-id="92213-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="92213-505">ในบานหน้าต่าง **แหล่งข้อมูล** ให้ขยาย **CompanyInfo** แล้วปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="92213-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="92213-506">ขยายโหนด **CompanyInfo()** ที่แสดงถึงเมธอด **find()** ของตาราง CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="92213-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="92213-507">เลือก **CompanyInfo.find().Name**</span><span class="sxs-lookup"><span data-stu-id="92213-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="92213-508">เลือก **ผูก** เพื่อกรอกชื่อของบริษัทที่มีการเรียกการแม็ปรูปแบบที่ตั้งค่าคอนฟิกไว้ในบริบทของขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="92213-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="92213-509">ในบานหน้าต่าง **รูปแบบข้อมูล** เลือก **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="92213-510">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **แบบสอบถาม** และเลือก **ผูก** เพื่อกรอกข้อมูลในเรกคอร์ดแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="92213-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="92213-511">ในบานหน้าต่าง **รูปแบบข้อมูล** ให้ขยาย **แบบสอบถาม** แล้วปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="92213-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="92213-512">ในบานหน้าต่าง **รูปแบบข้อมูล** เลือก **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="92213-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="92213-513">ในบานหน้าต่าง **รูปแบบข้อมูล** เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="92213-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="92213-514">ในฟิลด์ **สูตร** ป้อน **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** เพื่อกรอกข้อมูลผลลัพธ์ที่อิงกับข้อความและอิงกับภาษาของการเปรียบเทียบระหว่างค่าการแจงนับ</span><span class="sxs-lookup"><span data-stu-id="92213-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="92213-515">ดำเนินการผูกแหล่งข้อมูลเข้ากับฟิลด์รูปแบบข้อมูลในลักษณะเดียวกันจนกว่าคุณจะได้รับผลลัพธ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="92213-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="92213-516">พาธของฟิลด์</span><span class="sxs-lookup"><span data-stu-id="92213-516">Field path</span></span>                                              | <span data-ttu-id="92213-517">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-517">Data type</span></span>   | <span data-ttu-id="92213-518">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="92213-518">Action</span></span> | <span data-ttu-id="92213-519">นิพจน์การผูก</span><span class="sxs-lookup"><span data-stu-id="92213-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="92213-520">CompanyName</span><span class="sxs-lookup"><span data-stu-id="92213-520">CompanyName</span></span>                                             | <span data-ttu-id="92213-521">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-521">String</span></span>      | <span data-ttu-id="92213-522">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-522">Bind</span></span>   | <span data-ttu-id="92213-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="92213-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="92213-524">แบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="92213-524">Questionnaire</span></span>                                           | <span data-ttu-id="92213-525">รายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="92213-525">Record list</span></span> | <span data-ttu-id="92213-526">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-526">Bind</span></span>   | <span data-ttu-id="92213-527">แบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="92213-527">Questionnaire</span></span> |
    | <span data-ttu-id="92213-528">Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="92213-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="92213-529">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-529">String</span></span>      | <span data-ttu-id="92213-530">แก้ไข</span><span class="sxs-lookup"><span data-stu-id="92213-530">Edit</span></span>   | <span data-ttu-id="92213-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="92213-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="92213-532">Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="92213-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="92213-533">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-533">String</span></span>      | <span data-ttu-id="92213-534">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-534">Bind</span></span>   | <span data-ttu-id="92213-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="92213-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="92213-536">Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="92213-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="92213-537">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-537">String</span></span>      | <span data-ttu-id="92213-538">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-538">Bind</span></span>   | <span data-ttu-id="92213-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="92213-539">\@.Description</span></span> |
    | <span data-ttu-id="92213-540">Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="92213-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="92213-541">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-541">String</span></span>      | <span data-ttu-id="92213-542">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-542">Bind</span></span>   | <span data-ttu-id="92213-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="92213-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="92213-544">Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="92213-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="92213-545">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-545">String</span></span>      | <span data-ttu-id="92213-546">แก้ไข</span><span class="sxs-lookup"><span data-stu-id="92213-546">Edit</span></span>   | <span data-ttu-id="92213-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="92213-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="92213-548">EnumAppQuestionOrder.Conditional, "แบบมีเงื่อนไข",</span><span class="sxs-lookup"><span data-stu-id="92213-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="92213-549">EnumAppQuestionOrder.Random, "แบบสุ่ม (เปอร์เซ็นต์ในแบบสอบถาม)",</span><span class="sxs-lookup"><span data-stu-id="92213-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="92213-550">EnumAppQuestionOrder.RandomGroup, "แบบสุ่ม (เปอร์เซ็นต์ในกลุ่มผลลัพธ์)",</span><span class="sxs-lookup"><span data-stu-id="92213-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="92213-551">EnumAppQuestionOrder.Sequence, "แบบเรียงตามลำดับ",</span><span class="sxs-lookup"><span data-stu-id="92213-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="92213-552">"")</span><span class="sxs-lookup"><span data-stu-id="92213-552">"")</span></span> |
    | <span data-ttu-id="92213-553">Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="92213-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="92213-554">เรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="92213-554">Record</span></span>      |        | |
    | <span data-ttu-id="92213-555">Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="92213-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="92213-556">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-556">String</span></span>      | <span data-ttu-id="92213-557">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-557">Bind</span></span>   | <span data-ttu-id="92213-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="92213-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="92213-559">Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="92213-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="92213-560">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-560">String</span></span>      | <span data-ttu-id="92213-561">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-561">Bind</span></span>   | <span data-ttu-id="92213-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="92213-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="92213-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="92213-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="92213-564">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="92213-564">Real</span></span>        | <span data-ttu-id="92213-565">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-565">Bind</span></span>   | <span data-ttu-id="92213-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="92213-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="92213-567">Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="92213-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="92213-568">รายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="92213-568">Record list</span></span> | <span data-ttu-id="92213-569">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-569">Bind</span></span>   | <span data-ttu-id="92213-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="92213-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="92213-571">Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="92213-572">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="92213-572">Integer</span></span>     | <span data-ttu-id="92213-573">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-573">Bind</span></span>   | <span data-ttu-id="92213-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="92213-575">Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="92213-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="92213-576">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-576">String</span></span>      | <span data-ttu-id="92213-577">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-577">Bind</span></span>   | <span data-ttu-id="92213-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="92213-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="92213-579">Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="92213-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="92213-580">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-580">String</span></span>      | <span data-ttu-id="92213-581">แก้ไข</span><span class="sxs-lookup"><span data-stu-id="92213-581">Edit</span></span>   | <span data-ttu-id="92213-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="92213-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="92213-583">Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="92213-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="92213-584">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-584">String</span></span>      | <span data-ttu-id="92213-585">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-585">Bind</span></span>   | <span data-ttu-id="92213-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="92213-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="92213-587">Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="92213-588">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="92213-588">Integer</span></span>     | <span data-ttu-id="92213-589">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-589">Bind</span></span>   | <span data-ttu-id="92213-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="92213-591">Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="92213-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="92213-592">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-592">String</span></span>      | <span data-ttu-id="92213-593">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-593">Bind</span></span>   | <span data-ttu-id="92213-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="92213-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="92213-595">Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="92213-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="92213-596">รายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="92213-596">Record list</span></span> | <span data-ttu-id="92213-597">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-597">Bind</span></span>   | <span data-ttu-id="92213-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="92213-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="92213-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="92213-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="92213-600">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-600">String</span></span>      | <span data-ttu-id="92213-601">แก้ไข</span><span class="sxs-lookup"><span data-stu-id="92213-601">Edit</span></span>   | <span data-ttu-id="92213-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="92213-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="92213-603">Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="92213-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="92213-604">จำนวนจริง</span><span class="sxs-lookup"><span data-stu-id="92213-604">Real</span></span>        | <span data-ttu-id="92213-605">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-605">Bind</span></span>   | <span data-ttu-id="92213-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="92213-606">\@.point</span></span> |
    | <span data-ttu-id="92213-607">Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="92213-608">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="92213-608">Integer</span></span>     | <span data-ttu-id="92213-609">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-609">Bind</span></span>   | <span data-ttu-id="92213-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="92213-611">Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="92213-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="92213-612">สตริง</span><span class="sxs-lookup"><span data-stu-id="92213-612">String</span></span>      | <span data-ttu-id="92213-613">ผูก</span><span class="sxs-lookup"><span data-stu-id="92213-613">Bind</span></span>   | <span data-ttu-id="92213-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="92213-614">\@.text</span></span> |

    <span data-ttu-id="92213-615">ภาพประกอบต่อไปนี้แสดงสถานะขั้นสุดท้ายของการแม็ปรูปแบบที่ตั้งค่าคอนฟิกบนหน้า **ตัวออกแบบการแม็ปรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="92213-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![การแม็ปรูปแบบที่ตั้งค่าคอนฟิกทั้งหมดในตัวออกแบบการแม็ปรูปแบบ ER](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="92213-617">บันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="92213-617">Save your changes.</span></span>
8. <span data-ttu-id="92213-618">ปิดหน้า **ตัวออกแบบการแม็ปรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="92213-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="92213-619">ทำการออกแบบการแม็ปรูปแบบให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="92213-620">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="92213-621">ในหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การแม็ปแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="92213-622">บนแท็บด่วน **รุ่น** ให้เลือกรุ่นการตั้งค่าคอนฟิกที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="92213-623">เลือก **เปลี่ยนแปลงสถานะ** \> **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="92213-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="92213-624">สถานะของรุ่น 1.1 ของการตั้งค่าคอนฟิกนี้มีการเปลี่ยนแปลงจาก **แบบร่าง** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="92213-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="92213-625">รุ่น 1.1 ไม่สามารถเปลี่ยนแปลงได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="92213-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="92213-626">รุ่นนี้มีการแม็ปรูปแบบที่ตั้งค่าคอนฟิกและสามารถใช้เป็นข้อมูลพื้นฐานสำหรับการตั้งค่าคอนฟิก ER อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="92213-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="92213-627">รุ่น 1.2 ของการตั้งค่าคอนฟิกนี้จะถูกสร้างขึ้นและมีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="92213-628">คุณสามารถแก้ไขรุ่นนี้เพื่อปรับปรุงการตั้งค่าคอนฟิก **การแม็ปแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![รุ่นของการตั้งค่าคอนฟิก ER ที่แก้ไขได้บนหน้าการตั้งค่าคอนฟิก](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="92213-630">การแม็ปรูปแบบที่ตั้งค่าคอนฟิกเป็นการใช้งานเฉพาะทางการเงินของรูปแบบข้อมูลเชิงนามธรรมซึ่งแสดงถึงโดเมนธุรกิจ **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="92213-631">ออกแบบเท็มเพลตสำหรับรายงานแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="92213-631">Design a template for a custom report</span></span>

<span data-ttu-id="92213-632">กรอบงาน ER ใช้เท็มเพลตที่กำหนดล่วงหน้าเพื่อสร้างรายงานในรูปแบบ Microsoft Office (สมุดงาน Excel หรือเอกสาร Word)</span><span class="sxs-lookup"><span data-stu-id="92213-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="92213-633">ในขณะที่มีการสร้างรายงานที่ต้องการ จะมีการกรอกเท็มเพลตด้วยข้อมูลที่จำเป็นตามกระแสข้อมูลที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="92213-634">ดังนั้น คุณต้องออกแบบเท็มเพลตสำหรับรายงานแบบกำหนดเองของคุณก่อน</span><span class="sxs-lookup"><span data-stu-id="92213-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="92213-635">เท็มเพลตนี้ต้องออกแบบเป็นสมุดงาน Excel โดยโครงสร้างแสดงถึงโครงร่างของรายงานแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="92213-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="92213-636">คุณต้องกำหนดชื่อทุกรายการของ Excel ที่คุณวางแผนจะกรอกโดยใช้ข้อมูลที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="92213-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="92213-637">ดาวน์โหลดไฟล์ [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) และบันทึกไปยังคอมพิวเตอร์เฉพาะที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="92213-637">Download the [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="92213-638">เปิดไฟล์ใน Excel และตรวจสอบโครงสร้างของสมุดงาน</span><span class="sxs-lookup"><span data-stu-id="92213-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="92213-639">เมื่อแสดงภาพต่อไปนี้ เท็มเพลตที่ดาวน์โหลดได้ออกแบบให้พิมพ์แบบสอบถามที่ระบุ ซึ่งแสดงคำถามของแบบสอบถามพร้อมกับคำตอบที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="92213-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![เท็มเพลต Excel ที่จะพิมพ์แบบสอบถามที่ระบุ](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="92213-641">มีการเพิ่มชื่อ Excel เข้าในเท็มเพลตนี้ ให้กรอกรายละเอียดของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="92213-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="92213-642">คุณสามารถใช้ตัวจัดการชื่อเพื่อตรวจสอบชื่อ Excel</span><span class="sxs-lookup"><span data-stu-id="92213-642">You can use Name Manager to review the Excel names.</span></span>

![การใช้ตัวจัดการชื่อเพื่อตรวจสอบชื่อ Excel ในเท็มเพลต Excel ที่ระบุ](./media/er-quick-start1-template-names.png)

<span data-ttu-id="92213-644">มีการเพิ่มป้ายชื่อรายงานเป็นข้อความแบบคงที่ในภาษาอังกฤษ</span><span class="sxs-lookup"><span data-stu-id="92213-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="92213-645">คุณสามารถแทนที่ป้ายชื่อของรายงานด้วยชื่อ Excel ใหม่ที่กรอกในป้ายชื่อด้วยข้อความที่ขึ้นอยู่กับภาษาโดยใช้ [ป้ายชื่อ](#AddMmLabels) รูปแบบ ER ตามที่คุณใช้สำหรับนิพจน์ที่อิงกับภาษาในการแม็ปรูปแบบที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="92213-646">ในกรณีนี้ ป้ายชื่อ ER ต้องมีการเพิ่มในรูปแบบ ER ที่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="92213-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="92213-647">ในภาพประกอบต่อไปนี้แสดงว่ามีการระบุหัวข้อรายงานแบบกำหนดเองเพื่อเปิดใช้งาน Excel เพื่อทำการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="92213-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![ส่วนหัวของรายงานแบบกำหนดเองในเท็มเพลต Excel ที่ระบุ](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="92213-649">ออกแบบรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-649">Design a format</span></span>

<span data-ttu-id="92213-650">ในฐานะผู้ใช้ในบทบาทที่ปรึกษาการทำงานของการรายงานทางอิเล็กทรอนิกส์ คุณต้องสร้างการตั้งค่าคอนฟิก ER ใหม่ที่มีส่วนประกอบของ [รูปแบบ](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="92213-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="92213-651">คุณต้องตั้งค่าคอนฟิกส่วนประกอบของรูปแบบเพื่อระบุว่าจะมีการกรอกเท็มเพลตรายงานด้วยข้อมูลที่จำเป็นขณะรันไทม์อย่างไร</span><span class="sxs-lookup"><span data-stu-id="92213-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="92213-652">เมื่อดำเนินการขั้นตอนนี้ในส่วน [นำเข้าการตั้งค่าคอนฟิกรูปแบบที่ออกแบบ](#FormatImport) แล้ว คุณสามารถนำเข้ารูปแบบที่จำเป็นจากไฟล์ XML ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="92213-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="92213-653">อีกทางหนึ่งคือ คุณสามารถทำขั้นตอนนี้ให้เสร็จสมบูรณ์ได้ในส่วน [สร้างการตั้งค่าคอนฟิกรูปแบบใหม่](#FormatCreate) เพื่อออกแบบรูปแบบนี้ตั้งแต่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="92213-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="92213-654">นำเข้าการตั้งค่าคอนฟิกรูปแบบที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="92213-655">ดาวน์โหลดไฟล์ [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) และบันทึกไปยังคอมพิวเตอร์เฉพาะที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="92213-655">Download the [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="92213-656">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="92213-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="92213-657">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="92213-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="92213-658">ในบานหน้าต่างการดำเนินการ เลือก **แลกเปลี่ยน** \> **โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="92213-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="92213-659">เลือก **เรียกดู** แล้วค้นหาและเลือกไฟล์ **Questionnaires format.version.1.1.xml**</span><span class="sxs-lookup"><span data-stu-id="92213-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="92213-660">เลือก **ตกลง** เพื่อนำเข้าการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="92213-661">เมื่อต้องการดำเนินการต่อ ให้ข้ามขั้นตอนถัดไป [สร้างการตั้งค่าคอนฟิกรูปแบบใหม่](#FormatCreate)</span><span class="sxs-lookup"><span data-stu-id="92213-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="92213-662">สร้างการตั้งค่าคอนฟิกรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="92213-663">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="92213-664">ในหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รูปแบบแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="92213-665">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="92213-666">ในกล่องโต้ตอบรายการแบบหล่นลง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="92213-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="92213-667">ในฟิลด์ **สร้าง** เลือก **รูปปแบบตามแบบสอบถามรูปแบบข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="92213-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="92213-668">ในฟิลด์ **ชื่อ** ให้ป้อน **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="92213-669">ในฟิลด์ **รุ่นของรูปแบบข้อมูล** เลือก **1**</span><span class="sxs-lookup"><span data-stu-id="92213-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="92213-670">ถ้าคุณเลือกรุ่นเฉพาะของรูปแบบข้อมูลพื้นฐาน โครงสร้างขอรุ่นที่สัมพันธ์กันของรูปแบบข้อมูลจะแสดงให้คุณเป็นโครงสร้างของแหล่งข้อมูล **รูปแบบ** ในรูปแบบที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="92213-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="92213-671">คุณสามารถปล่อยฟิลด์นี้ว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="92213-671">You can leave this field blank.</span></span> <span data-ttu-id="92213-672">ในกรณีดังกล่าว โครงสร้างของรุ่น **แบบร่าง** ของรูปแบบข้อมูลจะแสดงให้คุณเป็นโครงสร้างของแหล่งข้อมูล **รูปแบบ** ในรูปแบบที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="92213-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="92213-673">จากนั้น คุณสามารถปรับปรุงรูปแบบของคุณและดูการปรับปรุงดังกล่าวในรูปแบบของคุณได้ทันที</span><span class="sxs-lookup"><span data-stu-id="92213-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="92213-674">วิธีการนี้อาจปรับปรุงประสิทธิภาพการทำงานของการออกแบบโซลูชัน ER เมื่อคุณตั้งค่าคอนฟิกรูปแบบข้อมูล การแม็ปรูปแบบ และรูปแบบพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="92213-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="92213-675">ถ้าคุณเลือกรุ่นเฉพาะของรูปแบบข้อมูลพื้นฐาน คุณสามารถสลับไปใช้รุ่น **แบบร่าง** ในภายหลังได้ เมื่อคุณเริ่มแก้ไขรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="92213-676">ในฟิลด์ **ข้อกำหนดของรูปแบบข้อมูล** ให้เลือกข้อกำหนด **ราก**</span><span class="sxs-lookup"><span data-stu-id="92213-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="92213-677">เลือก **สร้างการตั้งค่าคอนฟิก** เพื่อสร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="92213-678">นำเข้าเท็มเพลตของรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-678">Import a report template</span></span>

1. <span data-ttu-id="92213-679">ในหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="92213-680">เลือก **ตัวออกแบบ** เพื่อเริ่มต้นการตั้งค่าคอนฟิกรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="92213-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="92213-681">บนหน้า **ตัวออกแบบรูปแบบ** บนบานหน้าต่างการดำเนินการ เลือก **นำเข้า** \> **นำเข้าจาก Excel**</span><span class="sxs-lookup"><span data-stu-id="92213-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="92213-682">ในกล่องโต้ตอบ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="92213-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="92213-683">เลือก **เพิ่มเท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="92213-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="92213-684">ค้นหาและเลือกไฟล์ **Questionnaires report template.xslx** ที่บันทึกไว้ในเครื่อง แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="92213-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="92213-685">เลือก **ตกลง** เพื่อนำเข้าเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="92213-685">Select **OK** to import the template.</span></span>

    ![การนำเข้าเท็มเพลตของรายงาน](./media/er-quick-start1-template-import.png)

<span data-ttu-id="92213-687">องค์ประกอบรูปแบบ **Excel\\File** จะถูกเพิ่มลงในรูปแบบที่แก้ไขได้โดยอัตโนมัติเป็นองค์ประกอบราก</span><span class="sxs-lookup"><span data-stu-id="92213-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="92213-688">นอกจากนี้ องค์ประกอบรูปแบบ **Excel\\Range** หรือองค์ประกอบรูปแบบ **Excel\\Cell** จะถูกเพิ่มโดยอัตโนมัติสำหรับชื่อ Excel ที่ได้รับการยอมรับทั้งหมดของเท็มเพลตที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="92213-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="92213-689">องค์ประกอบรูปแบบ **Excel\\Header** ที่มีองค์ประกอบของ **สตริง** ที่ซ้อนกันจะถูกเพิ่มโดยอัตโนมัติเพื่อให้สะท้อนถึงการตั้งค่าหัวข้อของเท็มเพลตที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="92213-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![จัดรูปแบบโครงสร้างที่มีองค์ประกอบเพิ่มโดยอัตโนมัติในตัวออกแบบการดำเนินงานของ ER](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="92213-691">ตั้งค่าคอนฟิกรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-691">Configure a format</span></span>

1. <span data-ttu-id="92213-692">บนหน้า **ตัวออกแบบรูปแบบ** ในแผนผังรูปแบบ เลือกองค์ประกอบราก **Excel**</span><span class="sxs-lookup"><span data-stu-id="92213-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="92213-693">บนแท็บ **รูปแบบ** ทางด้านขวาของหน้า ในฟิลด์ **ชื่อ** ป้อน <a name="AddFormatRootElement"></a>**รายงาน**</span><span class="sxs-lookup"><span data-stu-id="92213-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="92213-694">ในฟิลด์ **การกำหนดลักษณะภาษา** เลือก **การกำหนดลักษณะของผู้ใช้** เพื่อเรียกใช้รายงานในภาษาที่ต้องการของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="92213-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="92213-695">ในฟิลด์ **การกำหนดลักษณะวัฒนธรรม** เลือก **การกำหนดลักษณะของผู้ใช้** เพื่อเรียกใช้รายงานในวัฒนธรรมที่ต้องการของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="92213-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="92213-696">สำหรับข้อมูลเกี่ยวกับวิธีการระบุบริบทภาษาและวัฒนธรรมสำหรับกระบวนการ ER ให้ดูที่[ออกแบบรายงานหลายภาษา](er-design-multilingual-reports.md)</span><span class="sxs-lookup"><span data-stu-id="92213-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![ตั้งค่าคอนฟิกการตั้งค่าภาษาและวัฒนธรรมสำหรับรายงานที่ออกแบบในตัวออกแบบการดำเนินงานของ ER](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="92213-698">ในแผนภูมิรูปแบบ ให้ขยายโหนดราก แล้วเลือก **ResultsGroup**</span><span class="sxs-lookup"><span data-stu-id="92213-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="92213-699">บนแท็บ **รูปแบบ** ในฟิลด์ **ทิศทางการจำลอง** ให้เลือก **ไม่มีการจำลอง** เนื่องจากคุณไม่คาดว่าจะมีกลุ่มผลลัพธ์จำนวนมากสำหรับแบบสอบถามเดียว</span><span class="sxs-lookup"><span data-stu-id="92213-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![การกำหนดทิศทางการจำลองสำหรับองค์ประกอบรูปแบบช่วงในตัวออกแบบการดำเนินงานของ ER](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="92213-701">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="92213-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="92213-702">กำหนดการผูกข้อมูลสำหรับชื่อรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-702">Define the data binding for a report title</span></span>

<span data-ttu-id="92213-703">คุณต้องระบุการผูกข้อมูลสำหรับองค์ประกอบรูปแบบที่ใช้ในการกรอกชื่อเรื่องของรายงานที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="92213-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="92213-704">บนหน้า **ตัวออกแบบรูปแบบ** บนแท็บ **การแม็ป** ที่อยู่ทางขวา เลือกองค์ประกอบ **Report\\ReportTitle**</span><span class="sxs-lookup"><span data-stu-id="92213-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="92213-705">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="92213-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="92213-706">ในตัวแก้ไขสูตร ให้เลือก **แปล**</span><span class="sxs-lookup"><span data-stu-id="92213-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="92213-707">ในกล่องโต้ตอบ **การแปลข้อความ** ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="92213-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="92213-708">ในฟิลด์ **รหัสป้ายชื่อ** ป้อน **ReportTitle**</span><span class="sxs-lookup"><span data-stu-id="92213-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="92213-709">ในฟิลด์ **ข้อความในภาษาเริ่มต้น** ให้ป้อน **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="92213-710">เลือก **แปล** แล้วจากนั้น เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="92213-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="92213-711">เลือก **แปล** เพื่อปิดกล่องโต้ตอบ **การแปลข้อความ**</span><span class="sxs-lookup"><span data-stu-id="92213-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="92213-712">ปิดตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="92213-712">Close the formula editor.</span></span>

    ![การตั้งค่าคอนฟิกการผูกข้อมูลที่จะกรอกในชื่อเรื่องของรายงานที่สร้าง](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="92213-714">คุณสามารถใช้เทคนิคนี้เพื่อทำให้ป้ายชื่ออื่นๆ ทั้งหมดของเท็มเพลตเป็นแบบอิงกับภาษาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="92213-715">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการแปลป้ายชื่อของการตั้งค่าคอนฟิก ER แบบครั้งเดียวเป็นภาษาที่ได้รับการสนับสนุนทั้งหมด ให้ดูที่ [ออกแบบรายงานหลายภาษา](er-design-multilingual-reports.md)</span><span class="sxs-lookup"><span data-stu-id="92213-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="92213-716">ตรวจทานแหล่งข้อมูลรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-716">Review model data source</span></span>

1. <span data-ttu-id="92213-717">บนหน้า **ตัวอกแบบรูปแบบ** บนแท็บ **การแม็ป** เลือกแหล่งข้อมูล <a name="ModelDSName"></a>**รูปแบบ** ที่แสดงถึงรูปแบบข้อมูลพื้นฐานของรูปแบบ ER นี้</span><span class="sxs-lookup"><span data-stu-id="92213-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="92213-718">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="92213-718">Select **Edit**.</span></span>
3. <span data-ttu-id="92213-719">ตรวจทานข้อมูลในกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="92213-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="92213-720">แหล่งข้อมูลนี้หมายถึงรุ่น 1 ของส่วนประกอบรูปแบบข้อมูล **แบบสอบถาม** ที่อยู่ในการตั้งค่าคอนฟิก ER ของ **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![คุณสมบัติของแหล่งข้อมูลรูปแบบในตัวออกแบบการดำเนินงานของ ER](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="92213-722">ผูกองค์ประกอบของรูปแบบกับฟิลด์แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="92213-723">ถ้าต้องการระบุวิธีการกรอกข้อมูลเท็มเพลตขณะรันไทม์ คุณต้องผูกองค์ประกอบรูปแบบทั้งหมดที่เชื่อมโยงกับชื่อ Excel ที่เหมาะสมกับฟิลด์เดียวของแหล่งข้อมูลของรูปแบบนี้</span><span class="sxs-lookup"><span data-stu-id="92213-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="92213-724">บนหน้า **ตัวออกแบบรูปแบบ** ในแผนผังรูปแบบ เลือกองค์ประกอบรูปแบบ **Report\\CompanyName**</span><span class="sxs-lookup"><span data-stu-id="92213-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="92213-725">บนแท็บ **การแม็ป** เลือกฟิลด์แหล่งข้อมูล **model.CompanyName** ของชนิด **ชนิด**</span><span class="sxs-lookup"><span data-stu-id="92213-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="92213-726">เลือก **ผูก** เพื่อป้อนชื่อบริษัทในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="92213-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="92213-727">ในแผนผังรูปแบบ ให้เลือกองค์ประกอบ **Report\\Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="92213-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="92213-728">บนแท็บ **การแม็ป** เลือกฟิลด์แหล่งข้อมูล **model.Questionnaire** ของชนิด **รายการเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="92213-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="92213-729">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="92213-729">Select **Bind**.</span></span>
7. <span data-ttu-id="92213-730">เลือก **แสดงรายละเอียด** เพื่อดูรายละเอียดเพิ่มเติมสำหรับองค์ประกอบรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="92213-731">องค์ประกอบรูปแบบช่วง **แบบสอบถาม** ถูกตั้งค่าคอนฟิกเป็นการจำลองตามแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="92213-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="92213-732">เมื่อมีการผูกกับแหล่งข้อมูลของชนิด **รายการเรกคอร์ด** ช่วง **แบบสอบถาม** ที่เหมาะสมของเท็มเพลต Excel จะถูกทำซ้ำสำหรับเรกคอร์ดทั้งหมดของแหล่งข้อมูลที่ผูกไว้</span><span class="sxs-lookup"><span data-stu-id="92213-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![การผูกองค์ประกอบรูปแบบช่วงแบบสอบถามกับแหล่งข้อมูลรายการเรกคอร์ดที่เหมาะสมในตัวออกแบบการดำเนินงาน ER](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="92213-734">เนื่องจากช่วง **แบบสอบถาม** ของเท็มเพลต Excel จะถูกกำหนดระหว่างแถวที่ 5 ถึง 14 แถวเหล่านี้จะถูกทำซ้ำสำหรับแบบสอบถามที่รายงานทุกครั้ง</span><span class="sxs-lookup"><span data-stu-id="92213-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![แถวในเท็มเพลต Excel ที่จะทำซ้ำในรายงานที่สร้างสำหรับเรกคอร์ดทั้งหมดของแหล่งข้อมูลของรายการเรกคอร์ด](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="92213-736">ตั้งค่าคอนฟิกการผูกที่คล้ายกันสำหรับองค์ประกอบรูปแบบที่เหลือ ดังที่อธิบายไว้ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="92213-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92213-737">ในตารางนี้ ข้อมูลในคอลัมน์ "พาธแหล่งข้อมูล" สันนิษฐานว่า [พาธที่สัมพันธ์กัน](relative-path-data-bindings-er-models-format.md) คุณลักษณะ ER เปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="92213-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="92213-738">พาธองค์ประกอบรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-738">Format element path</span></span>                                      | <span data-ttu-id="92213-739">พาธแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="92213-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="92213-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="92213-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="92213-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="92213-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="92213-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="92213-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="92213-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="92213-744">Excel\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="92213-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="92213-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="92213-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="92213-746">Excel\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="92213-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="92213-747">**\@.Active** โดยที่ **\@** คือ **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="92213-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="92213-748">Excel\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="92213-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="92213-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="92213-749">**\@.Code**</span></span> |
    | <span data-ttu-id="92213-750">Excel\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="92213-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="92213-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="92213-751">**\@.Description**</span></span> |
    | <span data-ttu-id="92213-752">Excel\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="92213-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="92213-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="92213-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="92213-754">Excel\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="92213-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="92213-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="92213-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="92213-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span><span class="sxs-lookup"><span data-stu-id="92213-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="92213-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="92213-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="92213-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span><span class="sxs-lookup"><span data-stu-id="92213-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="92213-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="92213-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="92213-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="92213-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="92213-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="92213-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="92213-762">Excel\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="92213-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="92213-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="92213-763">**\@.Question**</span></span> |
    | <span data-ttu-id="92213-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="92213-765">**\@.CollectionSequenceNumber** โดยที่ **\@** คือ **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="92213-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="92213-766">Excel\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="92213-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="92213-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="92213-767">**\@.Id**</span></span> |
    | <span data-ttu-id="92213-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="92213-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="92213-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="92213-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="92213-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="92213-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="92213-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="92213-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="92213-772">Excel\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="92213-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="92213-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="92213-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="92213-774">Excel\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="92213-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="92213-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="92213-775">**\@.Text**</span></span> |
    | <span data-ttu-id="92213-776">Excel\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="92213-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="92213-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="92213-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="92213-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="92213-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="92213-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="92213-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="92213-780">Excel\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="92213-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="92213-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="92213-781">**\@.Points**</span></span> |
    | <span data-ttu-id="92213-782">Excel\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="92213-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="92213-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="92213-783">**\@.Text**</span></span> |

9. <span data-ttu-id="92213-784">เมื่อคุณได้ทำเสร็จสิ้นแล้ว เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="92213-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="92213-785">ภาพประกอบต่อไปนี้แสดงสถานะขั้นสุดท้ายของการผูกข้อมูลที่ตั้งค่าคอนฟิกบนหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="92213-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![การผูกข้อมูลที่ตั้งค่าคอนฟิกในตัวออกแบบการดำเนินงานของ ER](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="92213-787">คอลเลกชันทั้งหมดของแหล่งข้อมูลที่ระบุและการผูกแสดงถึงส่วนประกอบการแม็ปรูปแบบของรูปแบบที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="92213-788">การแม็ปรูปแบบนี้ถูกเรียกเมื่อคุณเรียกใช้รูปแบบที่ตั้งค่าคอนฟิกสำหรับการสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="92213-789">เรียกใช้รูปแบบที่ออกแบบจาก ER</span><span class="sxs-lookup"><span data-stu-id="92213-789">Run a designed format from ER</span></span>

<span data-ttu-id="92213-790">ขณะนี้ คุณสามารถเรียกใช้รูปแบบที่ออกแบบมาเพื่อวัตถุประสงค์ในการทดสอบจากหน้า **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="92213-791">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="92213-792">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **รูปแบบแบบสอบถาม** จากนั้นเลือก **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="92213-793">เลือก **ตัวออกแบบ** สำหรับรุ่นของรูปแบบที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="92213-794">ในหน้า **ตัวออกแบบรูปแบบ** เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="92213-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="92213-795">ในกล่องโต้ตอบ **พารามิเตอร์ ER** บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้ตั้งค่าคอนฟิกตัวเลือกการกรองเพื่อให้รวมเฉพาะแบบสอบถาม **SBCCrsExam** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92213-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="92213-796">เลือก **ตกลง** เพื่อยืนยันตัวเลือกการกรอง</span><span class="sxs-lookup"><span data-stu-id="92213-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="92213-797">เลือก **ตกลง** เพื่อเรียกใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="92213-798">ตรวจสอบรายงานที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="92213-798">Review the generated report.</span></span>

<span data-ttu-id="92213-799">ตาม [ค่าเริ่มต้น ](electronic-reporting-destinations.md#default-behavior) จะมีการจัดส่งรายงานที่สร้างเป็นไฟล์ Excel ที่คุณสามารถดาวน์โหลดได้</span><span class="sxs-lookup"><span data-stu-id="92213-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="92213-800">ภาพประกอบต่อไปนี้แสดงสองหน้าของรายงานที่สร้างขึ้นในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="92213-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![ตัวอย่างของรายงานที่สร้างขึ้นในรูปแบบ Excel, หน้าที่ 1](./media/er-quick-start1-report1a.png)

![ตัวอย่างของรายงานที่สร้างขึ้นในรูปแบบ Excel, หน้าที่ 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="92213-803">ปรับแต่งรูปแบบที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="92213-804">แก้ไขรูปแบบที่จะเปลี่ยนชื่อของเอกสารที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="92213-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="92213-805">ตามค่าเริ่มต้น เอกสารที่สร้างขึ้นจะถูกตั้งชื่อโดยใช้นามแฝงของผู้ใช้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="92213-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="92213-806">ด้วยการปรับเปลี่ยนรูปแบบ คุณสามารถเปลี่ยนลักษณะการทำงานนี้เพื่อให้เอกสารที่สร้างขึ้นมีการตั้งชื่อตามตรรกะที่กำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="92213-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="92213-807">ตัวอย่างเช่น ชื่อของเอกสารที่สร้างขึ้นสามารถอิงตามวันที่และเวลาของรอบเวลาปัจจุบันและในชื่อของรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="92213-808">บนหน้า **ตัวออกแบบรูปแบบ** ให้เลือกรายการราก **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="92213-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="92213-809">บนแท็บ **การแม็ป** ให้เลือก **แก้ไขชื่อไฟล์**</span><span class="sxs-lookup"><span data-stu-id="92213-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="92213-810">ในฟิลด์ **สูตร** ป้อน **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**</span><span class="sxs-lookup"><span data-stu-id="92213-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="92213-811">เลือก **ตกลง** และปิดตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="92213-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="92213-812">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="92213-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="92213-813">ปรับเปลี่ยนรูปแบบที่จะเปลี่ยนลำดับของคำถาม</span><span class="sxs-lookup"><span data-stu-id="92213-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="92213-814">คำถามไม่ได้รับการจัดลำดับอย่างถูกต้องในรายงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="92213-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="92213-815">คุณสามารถเปลี่ยนลำดับโดยการแก้ไขรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="92213-816">บนหน้า **ตัวออกแบบรูปแบบ** ให้เลือกรายการราก **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="92213-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="92213-817">บนแท็บ **การแม็ป** ในแผนผังรูปแบบ ให้ขยาย **Report\\Questionnaire\\Question**</span><span class="sxs-lookup"><span data-stu-id="92213-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![องค์ประกอบรูปแบบคำถามของชนิดช่วงในตัวออกแบบการดำเนินงานของ ER](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="92213-819">บนแท็บ **การแม็ป** ให้เลือก **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="92213-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="92213-820">เลือก **เพิ่ม** \> **Functions\\Calculated field** จากนั้นในฟิลด์ **ชื่อ** ให้ป้อน **OrderedQuestions**</span><span class="sxs-lookup"><span data-stu-id="92213-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="92213-821">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="92213-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="92213-822">ในตัวแก้ไขสูตร ในฟิลด์ **สูตร** ป้อน **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** เพื่อจัดลำดับของรายการคำถามของแบบสอบถามปัจจุบันตามหมายเลขลำดับ</span><span class="sxs-lookup"><span data-stu-id="92213-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="92213-823">เลือก **ตกลง** และปิดตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="92213-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="92213-824">เลือก **ตกลง** เพื่อทำให้รายการของฟิลด์ที่คำนวณใหม่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="92213-825">บนแท็บ **การแม็ป** เลือก **model.Questionnaire.OrderedQuestions**</span><span class="sxs-lookup"><span data-stu-id="92213-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="92213-826">ในแผนผังรูปแบบ เลือก **Excel\\Questionnaire\\Question**</span><span class="sxs-lookup"><span data-stu-id="92213-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="92213-827">เลือก **ผูก** แล้วยืนยันว่าพาธ **model.Questionnaire.Questions** ปัจจุบันมีการแทนที่ด้วยพาธ **model.Questionnaire.OrderedQuestions** ใหม่ในการผูกขององค์ประกอบที่ซ้อนกันทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="92213-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="92213-828">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="92213-828">Select **Save**.</span></span>

![การผูกองค์ประกอบรูปแบบคำถามกับแหล่งข้อมูล OrderedQuestions ที่ตั้งค่าคอนฟิกในตัวออกแบบการดำเนินงานของ ER](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="92213-830">เรียกใช้รูปแบบที่ปรับเปลี่ยนจาก ER</span><span class="sxs-lookup"><span data-stu-id="92213-830">Run a modified format from ER</span></span>

<span data-ttu-id="92213-831">ขณะนี้คุณสามารถเรียกใช้รูปแบบที่แก้ไขสำหรับวัตถุประสงค์ในการทดสอบจากกรอบงาน ER</span><span class="sxs-lookup"><span data-stu-id="92213-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="92213-832">ในหน้า **ตัวออกแบบรูปแบบ** เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="92213-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="92213-833">ในกล่องโต้ตอบ **พารามิเตอร์ ER** บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้ตั้งค่าคอนฟิกตัวเลือกการกรองเพื่อให้รวมเฉพาะแบบสอบถาม **SBCCrsExam** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92213-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="92213-834">เลือก **ตกลง** เพื่อยืนยันตัวเลือกการกรอง</span><span class="sxs-lookup"><span data-stu-id="92213-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="92213-835">เลือก **ตกลง** เพื่อเรียกใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="92213-836">ตรวจสอบรายงานที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="92213-836">Review the generated report.</span></span>

<span data-ttu-id="92213-837">ภาพประกอบต่อไปนี้แสดงรายงานที่สร้างขึ้นในรูปแบบ Excel ซึ่งมีการจัดลำดับคำถามอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="92213-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![รายงานที่สร้างขึ้นในรูปแบบ Excel ซึ่งมีคำถามที่จัดลำดับอย่างถูกต้อง](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="92213-839">ทำการออกแบบรูปแบบให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-839">Complete the format design</span></span>

1. <span data-ttu-id="92213-840">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="92213-841">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **รูปแบบแบบสอบถาม** จากนั้นเลือก **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="92213-842">บนแท็บด่วน **รุ่น** ให้เลือกรุ่นการตั้งค่าคอนฟิกที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="92213-843">เลือก **เปลี่ยนแปลงสถานะ** \> **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="92213-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="92213-844">สถานะของรุ่น 1.1 ของการตั้งค่าคอนฟิกนี้มีการเปลี่ยนแปลงจาก **แบบร่าง** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="92213-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="92213-845">รุ่น 1.1 ไม่สามารถเปลี่ยนแปลงได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="92213-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="92213-846">รุ่นนี้มีรูปแบบที่ตั้งค่าคอนฟิกและสามารถใช้เพื่อพิมพ์รายงานที่กำหนดเองของคุณได้</span><span class="sxs-lookup"><span data-stu-id="92213-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="92213-847">รุ่น 1.2 ของการตั้งค่าคอนฟิกนี้จะถูกสร้างขึ้นและมีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="92213-848">คุณสามารถแก้ไขรุ่นนี้เพื่อปรับปรุงรูปแบบของรายงาน **แบบสอบถาม** ของคุณ</span><span class="sxs-lookup"><span data-stu-id="92213-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![รุ่นของการตั้งค่าคอนฟิก ER ที่แก้ไขได้บนหน้าการตั้งค่าคอนฟิก](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="92213-850">รูปแบบที่ตั้งค่าคอนฟิกเป็นการออกแบบรายงาน **แบบสอบถาม** ของคุณ และไม่มีความสัมพันธ์กับอาร์ทิแฟกต์เฉพาะทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="92213-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="92213-851">พัฒนาอาร์ทิแฟกต์ของแอปพลิเคชันเพื่อเรียกรายงานที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="92213-852">ในฐานะผู้ใช้ในบทบาทผู้ดูแลระบบ คุณต้องพัฒนาตรรกะใหม่เพื่อให้สามารถเรียกใช้รูปแบบ ER ที่ตั้งค่าคอนฟิกจากส่วนติดต่อผู้ใช้ (UI) ของแอปพลิเคชันเพื่อสร้างรายงานที่กำหนดเองของคุณได้</span><span class="sxs-lookup"><span data-stu-id="92213-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="92213-853">ปัจจุบัน ER ไม่มีความสามารถในการตั้งค่าคอนฟิกตรรกะชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="92213-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="92213-854">ดังนั้น จึงจำเป็นต้องใช้งานวิศวกรรมบางส่วน</span><span class="sxs-lookup"><span data-stu-id="92213-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="92213-855">เพื่อพัฒนาตรรกะใหม่ คุณต้องปรับใช้โทโพโลยีที่สนับสนุนการสร้างแบบต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="92213-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="92213-856">สำหรับข้อมูลเพิ่มเติม ดู [ปรับใช้โทโพโลยีซึ่งสนับสนุนการสร้างอย่างต่อเนื่องและระบบอัตโนมัติของการทดสอบ](../perf-test/continuous-build-test-automation.md)</span><span class="sxs-lookup"><span data-stu-id="92213-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="92213-857">คุณต้องมีการเข้าถึงไปยังสภาพแวดล้อมการพัฒนาสำหรับโทโพโลยีนี้</span><span class="sxs-lookup"><span data-stu-id="92213-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="92213-858">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ ER API ที่มีอยู่ ให้ดูที่ [API กรอบงาน ER](er-apis-app73.md)</span><span class="sxs-lookup"><span data-stu-id="92213-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="92213-859">ปรับเปลี่ยนโค้ดต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="92213-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="92213-860">เพิ่มคลาสสัญญาข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-860">Add a data contract class</span></span>

<span data-ttu-id="92213-861">เพิ่มคลาส **QuestionnairesErReportContract** ใหม่ลงในโครงการ Microsoft Visual Studio ของคุณ และเขียนโค้ดที่ระบุสัญญาข้อมูลที่ควรใช้ในการเรียกใช้รูปแบบ ER ที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="92213-862">เพิ่มคลาสตัวสร้าง UI</span><span class="sxs-lookup"><span data-stu-id="92213-862">Add a UI builder class</span></span>

<span data-ttu-id="92213-863">เพิ่มคลาส **QuestionnairesErReportUIBuilder** ใหม่ลงในโครงการ Visual Studio ของคุณ และเขียนโค้ดเพื่อสร้างกลองโต้ตอบรันไทม์ที่จะใช้ค้นหารหัสการแม็ปรูปแบบของรูปแบบ ER ที่ต้องเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="92213-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="92213-864">โค้ดที่ระบุจะค้นหาเฉพาะรูปแบบ ER ที่มีแหล่งข้อมูลชนิด **รูปแบบข้อมูล** ที่อ้างถึงรูปแบบข้อมูล **[แบบสอบถาม](#DataModeName)** โดยใช้ข้อกำหนด **[ราก](#RootDefinitionName)**</span><span class="sxs-lookup"><span data-stu-id="92213-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="92213-865">อีกทางหนึ่งคือ คุณสามารถใช้จุดการรวม ER เพื่อกรองข้อมูลรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="92213-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="92213-866">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [API ที่จะแสดงการค้นหาการแม็ปรูปแบบ](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup)</span><span class="sxs-lookup"><span data-stu-id="92213-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="92213-867">เพิ่มคลาสผู้ให้บริการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-867">Add a data provider class</span></span>

<span data-ttu-id="92213-868">เพิ่มคลาส **QuestionnairesErReportDP** ใหม่ลงในโครงการ Visual Studio ของคุณ และเขียนโค้ดที่แนะนำผู้ให้บริการข้อมูลที่ควรใช้ในการเรียกใช้รูปแบบ ER ที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="92213-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="92213-869">โค้ดที่ระบุรวมเฉพาะสัญญาข้อมูลสำหรับผู้ให้บริการข้อมูลนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92213-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="92213-870">เพิ่มไฟล์ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="92213-870">Add a labels file</span></span>

<span data-ttu-id="92213-871">เพิ่มไฟล์ป้ายชื่อ **QuestionnairesErReportLabels\_en-US** ใหม่ลงในโครงการ Visual Studio ของคุณ และระบุป้ายชื่อต่อไปนี้สำหรับทรัพยากร UI ใหม่:</span><span class="sxs-lookup"><span data-stu-id="92213-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="92213-872">ป้ายชื่อ **\@QuestionnairesReport** สำหรับรายการเมนูใหม่ที่มีข้อความต่อไปนี้ในภาษาอังกฤษแบบสหรัฐ (en-US): **รายงานแบบสอบถาม (ให้บริการโดย ER)**</span><span class="sxs-lookup"><span data-stu-id="92213-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="92213-873">ป้ายชื่อ **\@QuestionnairesReportBatchJobDescription** สำหรับชื่อชุดงานหากรูปแบบ ER ที่เลือกมีการจัดกำหนดการสำหรับการดำเนินการเป็นแบบชุดงาน</span><span class="sxs-lookup"><span data-stu-id="92213-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="92213-874">เพิ่มคลาสบริการรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-874">Add a report service class</span></span>

<span data-ttu-id="92213-875">เพิ่มคลาส **QuestionnairesErReportService** ใหม่ลงในโครงการ Visual Studio ของคุณ และเขียนโค้ดที่เรียกรูปแบบ ER ระบุตามรหัสการแม็ปรูปแบบ และระบุสัญญาข้อมูลเป็นพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="92213-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="92213-876">เมื่อคุณต้องใช้รูปแบบ ER ซึ่งรันข้อมูลของแอปพลิเคชัน คุณต้องตั้งค่าคอนฟิกแหล่งข้อมูลชนิด **รูปแบบข้อมูล** ในการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="92213-877">แหล่งข้อมูลนี้อ้างงถึงส่วนใดส่วนหนึ่งของรูปแบบข้อมูลที่ระบุโดยใช้ข้อกำหนดรากเดียว</span><span class="sxs-lookup"><span data-stu-id="92213-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="92213-878">เมื่อเรียกใช้รูปแบบ ER จะเป็นการเรียกแหล่งข้อมูลนี้เพื่อเข้าถึงการแม็ปรูปแบบ ER ที่เหมาะสมที่มีการตั้งค่าคอนฟิกสำหรับรูปแบบและข้อกำหนดรากที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="92213-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="92213-879">ข้อมูลทั้งหมดที่คุณอาจต้องเตรียมในซอร์สโค้ดและที่เก็บซึ่งเป็นส่วนหนึ่งของสัญญาข้อมูลสามารถส่งผ่านไปยังรูปแบบ ER ที่เรียกใช้โดยใช้การแม็ปรูปแบบ ER ของชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="92213-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="92213-880">ในการแม็ปรูปแบบ ER คุณต้องตั้งค่าคอนฟิกแหล่งข้อมูลชนิด **ออบเจ็กต์** ที่อ้างอิงถึงคลาส **[QuestionnairesErReportContract](#DataContractClass)**</span><span class="sxs-lookup"><span data-stu-id="92213-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="92213-881">เมื่อต้องการระบุการแม็ปรูปแบบ คุณต้องระบุแหล่งข้อมูลที่เรียกการแม็ปรูปแบบนี้</span><span class="sxs-lookup"><span data-stu-id="92213-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="92213-882">ในโค้ดที่ระบุ แหล่งข้อมูลนี้ที่ระบุโดยค่าคงที่ **ERModelDataSourceName** ที่มีค่า **[รูปแบบ](#ModelDSName)**</span><span class="sxs-lookup"><span data-stu-id="92213-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="92213-883">เมื่อต้องการระบุแหล่งข้อมูลที่จะใช้ในการแสดงสัญญาข้อมูลในการแม็ปรูปแบบ คุณต้องระบุชื่อแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="92213-884">ในโค้ดที่ระบุ ชื่อนี้มีการระบุโดยค่าคงคงที่ **ParametersDataSourceName** ที่มีค่า <a name="DataContractDSName"></a>**RunTimeParameters**</span><span class="sxs-lookup"><span data-stu-id="92213-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="92213-885">ในสภาพแวดล้อมใหม่ คุณอาจต้องรีเฟรชข้อมูลเมตาของ ER เพื่อให้คลาสชนิดนี้พร้อมใช้งานในตัวออกแบบการแม็ปรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="92213-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="92213-886">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าคอนฟิกกรอบงาน ER](electronic-reporting-er-configure-parameters.md#frequently-asked-questions)</span><span class="sxs-lookup"><span data-stu-id="92213-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="92213-887">เพิ่มคลาสตัวควบคุมรายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-887">Add a report controller class</span></span>

<span data-ttu-id="92213-888">เพิ่มคลาส **QuestionnairesErReportController** ใหม่ลงในโครงการ Visual Studio ของคุณ และเขียนโค้ดที่เรียกใช้รูปแบบ ER ในโหมดซิงโครนัสหรือโหมดชุดงานตามที่คุณต้องการ ในกล่องโต้ตอบที่สร้างขึ้นตามตรรกะของคลาส **QuestionnairesErReportUIBuilder** ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="92213-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="92213-889">เพิ่มรายการเมนู</span><span class="sxs-lookup"><span data-stu-id="92213-889">Add a menu item</span></span>

<span data-ttu-id="92213-890">เพิ่มรายการเมนู **QuestionnairesErReport** ใหม่ลงในโครงการ Visual Studio ของคุณ</span><span class="sxs-lookup"><span data-stu-id="92213-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="92213-891">ในคุณสมบัติ **ออบเจ็กต์** รายการเมนูนี้อ้างอิงถึงคลาส **QuestionnairesErReportController** และมีการใช้เพื่อระบุสิทธิ์ของผู้ใช้ในการเลือกและเรียกใช้รูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="92213-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="92213-892">ในคุณสมบัติ **ป้ายชื่อ** รายการเมนูนี้อ้างอิงถึงป้ายชื่อ **\@QuestionnairesReport** ที่คุณสร้างไว้ก่อนหน้านี้เพื่อให้มีการแสดงข้อความที่ถูกต้องใน UI ของแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="92213-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="92213-893">เพิ่มรายการเมนูลงในเมนู</span><span class="sxs-lookup"><span data-stu-id="92213-893">Add a menu item to a menu</span></span>

<span data-ttu-id="92213-894">เพิ่มเมนู **KM** ที่มีอยู่ลงในโครงการ Visual Studio ของคุณ</span><span class="sxs-lookup"><span data-stu-id="92213-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="92213-895">คุณต้องเพิ่มรายการ **QuestionnairesErReport** ใหม่ของชนิด **ผลลัพธ์** ลงในเมนูนี้</span><span class="sxs-lookup"><span data-stu-id="92213-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="92213-896">รายการนี้ต้องออ้างอิงถึงรายการเมนู **QuestionnairesErReport** ที่อธิบายไว้ในหัวข้อก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="92213-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="92213-897">สร้างโครงการ Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92213-897">Build a Visual Studio project</span></span>

<span data-ttu-id="92213-898">สร้างโครงการของคุณเพื่อทำให้รายการเมนูใหม่พร้อมใช้งานสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="92213-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="92213-899">เรียกใช้รูปแบบจากแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="92213-899">Run a format from the application</span></span>

1. <span data-ttu-id="92213-900">ไปที่ **แบบสอบถาม** \> **ออกแบบ** \> **รายงานแบบสอบถาม (ที่ให้บริการโดย ER)**</span><span class="sxs-lookup"><span data-stu-id="92213-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![การเลือกรายการเมนูรายงานแบบสอบถาม (ที่ให้บริการโดย ER) ในโมดูลแบบสอบถามเพื่อเรียกใช้รูปแบบ ER ที่ตั้งค่าคอนฟิก](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="92213-902">ในกล่องโต้ตอบ ในฟิลด์ **การแม็ปรูปแบบ** เลือก **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="92213-903">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="92213-903">Select **OK**.</span></span>
4. <span data-ttu-id="92213-904">ในกล่องโต้ตอบ **พารามิเตอร์รายงานทางอิเล็กทรอนิกส์** บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้ตั้งค่าคอนฟิกตัวเลือกการกรองเพื่อให้รวมเฉพาะแบบสอบถาม **SBCCrsExam** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92213-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="92213-905">เลือก **ตกลง** เพื่อยืนยันตัวเลือกการกรอง</span><span class="sxs-lookup"><span data-stu-id="92213-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="92213-906">เลือก **ตกลง** เพื่อเรียกใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-906">Select **OK** to run the report.</span></span>

    ![การระบุเงื่อนไขการเลือกในกล่องโต้ตอบรายงานทางอิเล็กทรอนิกส์](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="92213-908">ตรวจสอบรายงานที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="92213-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="92213-909">ปรับแต่งโซลูชัน ER ที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-909">Tune a designed ER solution</span></span>

<span data-ttu-id="92213-910">คุณสามารถปรับแต่งโซลูชัน ER ที่ตั้งค่าคอนฟิกไว้เพื่อให้ใช้คลาสตัวให้บริการข้อมูลที่คุณพัฒนาเพื่อเข้าถึงรายละเอียดของรูปแบบ ER ที่กำลังทำงานอยู่ และเพื่อให้ป้อนชื่อของรูปแบบ ER นี้ในรายงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="92213-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="92213-911">ปรับเปลี่ยนการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="92213-912">เพิ่มแหล่งข้อมูลที่จะเข้าถึงออบเจ็กต์สัญญาข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="92213-913">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="92213-914">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **รูปแบบแบบสอบถาม** จากนั้นเลือก **การแม็ปแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="92213-915">เลือก **ตัวออกแบบ** เพื่อเปิดหน้า **การแม็ปรูปแบบกับแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="92213-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="92213-916">เลือก **ตัวออกแบบ** เพื่อเปิดการแม็ปที่เลือกในตัวออกแบบการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="92213-917">บนหน้า **ตัวออกแบบการแม็ปรูปแบบ** ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** เลือก **Dynamics 365 for Operations\\ออบเจ็กต์**</span><span class="sxs-lookup"><span data-stu-id="92213-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="92213-918">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="92213-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="92213-919">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ป้อน **[RunTimeParameters](#DataContractDSName)** ตามที่กำหนดในซอร์สโค้ดของคลาส **QuestionnairesErReportService**</span><span class="sxs-lookup"><span data-stu-id="92213-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="92213-920">ในฟิลด์ **คลาส** ป้อน **[QuestionnairesErReportContract](#DataContractClass)** ซึ่งเขียนโค้ดไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="92213-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="92213-921">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="92213-921">Select **OK**.</span></span>
10. <span data-ttu-id="92213-922">ขยาย **RunTimeParameters**</span><span class="sxs-lookup"><span data-stu-id="92213-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="92213-923">แหล่งข้อมูลที่เพิ่มเข้ามาจะให้ข้อมูลเกี่ยวกับรหัสเรกคอร์ดของการแม็ปรูปแบบ ER ที่กำลังทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="92213-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![เพิ่มแหล่งข้อมูลในตัวออกแบบการแม็ปรูปแบบ ER](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="92213-925">เพิ่มแหล่งข้อมูลที่จะเข้าถึงเรกคอร์ดการแม็ปรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="92213-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="92213-926">ดำเนินการต่อเพื่อแก้ไขการแม็ปรูปแบบที่เลือกโดยการเพิ่มแหล่งข้อมูลที่จะเข้าถึงเรกคอร์ดการแม็ปรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="92213-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="92213-927">บนหน้า **ตัวออกแบบการแม็ปรูปแบบ** ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** เลือก **Dynamics 365 for Operations\\เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="92213-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="92213-928">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="92213-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="92213-929">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **ER1**</span><span class="sxs-lookup"><span data-stu-id="92213-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="92213-930">ในฟิลด์ **ตาราง** ให้ป้อน **ERFormatMappingTable**</span><span class="sxs-lookup"><span data-stu-id="92213-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="92213-931">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="92213-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="92213-932">เพิ่มแหล่งข้อมูลที่จะเข้าถึงเรกคอร์ดการแม็ปรูปแบบของรูปแบบ ER ที่กำลังทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="92213-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="92213-933">ดำเนินการต่อเพื่อแก้ไขการแม็ปรูปแบบที่เลือกโดยการเพิ่มแหล่งข้อมูลที่จะเข้าถึงเรกคอร์ดการแม็ปรูปแบบของรูปแบบ ER ที่กำลังทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="92213-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="92213-934">บนหน้า **ตัวออกแบบการแม็ปรูปแบบ** ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** เลือก **Functions\\Calculated field**</span><span class="sxs-lookup"><span data-stu-id="92213-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="92213-935">ในบานหน้าต่าง **แหล่งข้อมูล** เลือก **เพิ่มราก**</span><span class="sxs-lookup"><span data-stu-id="92213-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="92213-936">ในกล่องโต้ตอบ ในฟิลด์ **ชื่อ** ให้ป้อน **ER2**</span><span class="sxs-lookup"><span data-stu-id="92213-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="92213-937">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="92213-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="92213-938">ในตัวแก้ไขสูตร ในฟิลด์ **สูตร** ป้อน **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**</span><span class="sxs-lookup"><span data-stu-id="92213-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="92213-939">เลือก **ตกลง** และปิดตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="92213-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="92213-940">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="92213-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="92213-941">ป้อนชื่อของรูปแบบ ER ที่กำลังทำงานอยู่ในรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="92213-942">ดำเนินการต่อเพื่อแก้ไขการแม็ปรูปแบบที่เลือกเพื่อให้มีการป้อนชื่อของรูปแบบ ER ที่กำลังทำงานอยู่ในรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="92213-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="92213-943">บนหน้า **ตัวออกแบบการแม็ปรูปแบบ** ในบานหน้าต่าง **รูปแบบข้อมูล** ขยาย **ExecutionContext** แล้วเลือก **ExecutionContext\\FormatName**</span><span class="sxs-lookup"><span data-stu-id="92213-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="92213-944">ในบานหน้าต่าง **รูปแบบข้อมูล** ให้เลือก **แก้ไข** เพื่อตั้งค่าคอนฟิกการผูกข้อมูลสำหรับฟิลด์ของรูปแบบข้อมูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="92213-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="92213-945">ในตัวแก้ไขสูตร ในฟิลด์ **สูตร** ป้อน **FIRSTORNULL (ER2.'\>Relations'.Format).Name**</span><span class="sxs-lookup"><span data-stu-id="92213-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="92213-946">เลือก **ตกลง** และปิดตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="92213-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="92213-947">เนื่องจากคุณใช้ฟิลด์ **FormatName** การแม็ปรูปแบบที่ได้รับการตั้งค่าคอนฟิกในตอนนี้จะแสดงชื่อของรูปแบบ ER ซึ่งเรียกการแม็ปรูปแบบนี้ในระหว่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="92213-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![ผูกฟิลด์รูปแบบข้อมูลกับวิธีการของแหล่งข้อมูลที่เพิ่มในตัวออกแบบการแม็ปรูปแบบ ER](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="92213-949">ทำการออกแบบการแม็ปรูปแบบให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="92213-950">บนหน้า **ตัวออกแบบการแม็ปรูปแบบ** เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="92213-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="92213-951">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="92213-951">Close the page.</span></span>
3. <span data-ttu-id="92213-952">ปิดหน้าการแม็ปรูปแบบง</span><span class="sxs-lookup"><span data-stu-id="92213-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="92213-953">บนหน้า **การตั้งค่าคอนฟิก** ในแผนผังการตั้งค่าคอนฟิก ตรวจสอบให้แน่ใจว่าการตั้งค่าคอนฟิก **การแม็ปแบบสอบถาม** ยังคงมีการเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="92213-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="92213-954">จากนั้น บนแท็บด่วน **รุ่น** ให้เลือกรุ่นการตั้งค่าคอนฟิกที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="92213-955">เลือก **เปลี่ยนแปลงสถานะ** \> **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="92213-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="92213-956">สถานะของรุ่น 1.2 ของการตั้งค่าคอนฟิกนี้มีการเปลี่ยนแปลงจาก **แบบร่าง** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="92213-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="92213-957">รุ่น 1.2 ไม่สามารถเปลี่ยนแปลงได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="92213-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="92213-958">รุ่นนี้มีการแม็ปรูปแบบที่ตั้งค่าคอนฟิกและสามารถใช้เป็นข้อมูลพื้นฐานสำหรับการตั้งค่าคอนฟิก ER อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="92213-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="92213-959">รุ่น 1.3 ของการตั้งค่าคอนฟิกนี้จะถูกสร้างขึ้นและมีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="92213-960">คุณสามารถแก้ไขรุ่นนี้เพื่อปรับปรุงการแม็ปรูปแบบ **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="92213-961">ปรับเปลี่ยนรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="92213-961">Modify a format</span></span>

<span data-ttu-id="92213-962">คุณสามารถปรับเปลี่ยนรูปแบบ ER ที่ตั้งค่าคอนฟิกไว้เพื่อให้ชื่อแสดงอยู่ในส่วนท้ายของรายงานที่สร้างขึ้นเมื่อมีการเรียกใช้รูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="92213-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="92213-963">เพิ่มองค์ประกอบรูปแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="92213-963">Add a new format element</span></span>

1. <span data-ttu-id="92213-964">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="92213-965">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **รูปแบบแบบสอบถาม** จากนั้นเลือก **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="92213-966">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="92213-966">Select **Designer**.</span></span>
4. <span data-ttu-id="92213-967">บนหน้า **ตัวออกแบบรูปแบบ** ให้เลือกรายการราก **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="92213-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="92213-968">เลือก **เพิ่ม** เพื่อเพิ่มองค์ประกอบรูปแบบที่ซ้อนกันใหม่สำหรับรายการรากของ **รายงาน** ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="92213-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="92213-969">เลือก **Excel\\Footer**</span><span class="sxs-lookup"><span data-stu-id="92213-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="92213-970">ในฟิลด์ **ชื่อ** ให้ป้อน **ส่วนท้าย**</span><span class="sxs-lookup"><span data-stu-id="92213-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="92213-971">เลือก **Report\Footer** แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="92213-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="92213-972">เลือก **Text\\String**</span><span class="sxs-lookup"><span data-stu-id="92213-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="92213-973">ผูกองค์ประกอบรูปแบบที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="92213-973">Bind the added format element</span></span>

1. <span data-ttu-id="92213-974">บนหน้า **ตัวออกแบบรูปแบบ** บนแท็บ **การแม็ป** ในแผนผังรูปแบบ สำหรับองค์ประกอบ **Footer\\String** ที่ใช้งานอยู่ เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="92213-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="92213-975">ในตัวแก้ไขสูตร ในฟิลด์ **สูตร** ป้อน **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**</span><span class="sxs-lookup"><span data-stu-id="92213-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="92213-976">เลือก **ตกลง** และปิดตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="92213-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="92213-977">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="92213-977">Select **Save**.</span></span>

<span data-ttu-id="92213-978">ตอนนี้มีการปรับเปลี่ยนรูปแบบที่ตั้งค่าคอนฟิกไว้เพื่อให้ชื่อถูกป้อนลงในส่วนท้ายของรายงานที่สร้างโดยใช้องค์ประกอบ **Footer\\String**</span><span class="sxs-lookup"><span data-stu-id="92213-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![การเพิ่มองค์ประกอบรูปแบบส่วนท้ายให้กับรูปแบบที่ตั้งค่าคอนฟิกไว้ในตัวออกแบบการดำเนินงานของ ER](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="92213-980">ทำการออกแบบรูปแบบให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="92213-980">Complete the format design</span></span>

1. <span data-ttu-id="92213-981">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="92213-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="92213-982">บนหน้า **การตั้งค่าคอนฟิก** ในแผนผังการตั้งค่าคอนฟิก ตรวจสอบให้แน่ใจว่าการตั้งค่าคอนฟิก **รายงานแบบสอบถาม** ยังคงมีการเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="92213-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="92213-983">จากนั้น บนแท็บด่วน **รุ่น** ให้เลือกรุ่นการตั้งค่าคอนฟิกที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="92213-984">เลือก **เปลี่ยนแปลงสถานะ** \> **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="92213-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="92213-985">สถานะของรุ่น 1.2 ของการตั้งค่าคอนฟิกนี้มีการเปลี่ยนแปลงจาก **แบบร่าง** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="92213-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="92213-986">รุ่น 1.2 ไม่สามารถเปลี่ยนแปลงได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="92213-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="92213-987">รุ่นนี้มีรูปแบบที่ตั้งค่าคอนฟิกและสามารถใช้เป็นข้อมูลพื้นฐานสำหรับการตั้งค่าคอนฟิก ER อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="92213-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="92213-988">รุ่น 1.3 ของการตั้งค่าคอนฟิกนี้จะถูกสร้างขึ้นและมีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="92213-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="92213-989">คุณสามารถแก้ไขรุ่นนี้เพื่อปรับปรุงรายงาน **แบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="92213-990">เรียกใช้รูปแบบจากแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="92213-990">Run a format from the application</span></span>

1. <span data-ttu-id="92213-991">ไปที่ **แบบสอบถาม** \> **ออกแบบ** \> **รายงานแบบสอบถาม (ที่ให้บริการโดย ER)**</span><span class="sxs-lookup"><span data-stu-id="92213-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="92213-992">ในกล่องโต้ตอบ ในฟิลด์ **การแม็ปรูปแบบ** เลือก **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="92213-993">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="92213-993">Select **OK**.</span></span>
4. <span data-ttu-id="92213-994">ในกล่องโต้ตอบ **พารามิเตอร์ ER** บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้ตั้งค่าคอนฟิกตัวเลือกการกรองเพื่อให้รวมเฉพาะแบบสอบถาม **SBCCrsExam** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92213-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="92213-995">เลือก **ตกลง** เพื่อยืนยันตัวเลือกการกรอง</span><span class="sxs-lookup"><span data-stu-id="92213-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="92213-996">เลือก **ตกลง** เพื่อเรียกใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="92213-997">ตรวจทานรายงานที่สร้างในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="92213-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="92213-998">โปรดสังเกตว่าส่วนท้ายของรายงานที่สร้างจะมีชื่อของรูปแบบ ER ซึ่งใช้ในการสร้าง</span><span class="sxs-lookup"><span data-stu-id="92213-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![รายงานที่สร้างในรูปแบบ Excel](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="92213-1000">เรียกใช้รูปแบบจาก ER</span><span class="sxs-lookup"><span data-stu-id="92213-1000">Run a format from ER</span></span>

1. <span data-ttu-id="92213-1001">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="92213-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="92213-1002">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **รูปแบบแบบสอบถาม** จากนั้นเลือก **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="92213-1003">บนบานหน้าต่างการดำเนินการ เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="92213-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="92213-1004">ในกล่องโต้ตอบ **พารามิเตอร์รายงานทางอิเล็กทรอนิกส์** บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้ตั้งค่าคอนฟิกตัวเลือกการกรองเพื่อให้รวมเฉพาะแบบสอบถาม **SBCCrsExam** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92213-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="92213-1005">เลือก **ตกลง** เพื่อยืนยันตัวเลือกการกรอง</span><span class="sxs-lookup"><span data-stu-id="92213-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="92213-1006">เลือก **ตกลง** เพื่อเรียกใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="92213-1007">ตรวจทานรายงานที่สร้างในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="92213-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="92213-1008">โปรดสังเกตว่าส่วนท้ายของรายงานที่สร้างขึ้นไม่มีชื่อของรูปแบบ ER ซึ่งใช้ในการสร้าง เนื่องจากไม่ได้ส่งผ่านอ็อบเจกต์สัญญาข้อมูลไปยังการแม็ปรูปแบบที่กำลังทำงานอยู่เมื่อมีการเรียกใช้โดยรูปแบบ ER ซึ่งเรียกใช้จาก ER</span><span class="sxs-lookup"><span data-stu-id="92213-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="92213-1009">ตั้งค่าคอนฟิกปลายทางรูปแบบสำหรับการแสดงตัวอย่างบนหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="92213-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="92213-1010">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **ปลายทางการรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="92213-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="92213-1011">บนหน้า **ปลายทางการรายงานทางอิเล็กทรอนิกส์** ให้เพิ่มเรกคอร์ดปลายทางสำหรับรูปแบบ ER ของ **รายงานแบบสอบถาม** ที่ตั้งค่าคอนฟิกไว้</span><span class="sxs-lookup"><span data-stu-id="92213-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="92213-1012">บนแท็บด่วน **ปลายทางของไฟล์** ตั้งค่า **หน้าจอ** [ปลายทาง](er-destination-type-screen.md) สำหรับส่วนประกอบรูปแบบ **รายงาน** ที่มี [การเพิ่มไว้](#AddFormatRootElement) เป็นองค์ประกอบรากของรูปแบบ ER ของ **รายงานแบบสอบถาม** ที่ตั้งค่าคอนฟิกไว้</span><span class="sxs-lookup"><span data-stu-id="92213-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="92213-1013">บนแท็บด่วน **การตั้งค่าการแปลง PDF** ให้ตั้งค่าคอนฟิกปลายทางที่จะแปลงรายงานเป็น [รูปแบบ PDF](electronic-reporting-destinations.md#OutputConversionToPDF) ที่ใช้การจัดวางหน้า **แนวนอน**</span><span class="sxs-lookup"><span data-stu-id="92213-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![การตั้งค่าคอนฟิกปลายทางของหน้าจอที่กำหนดเองสำหรับรูปแบบ ER บนหน้าปลายทางการรายงานทางอิเล็กทรอนิกส์](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="92213-1015">เรียกใช้รูปแบบจากแอปพลิเคชันเพื่อแสดงตัวอย่างเป็นเอกสาร PDF</span><span class="sxs-lookup"><span data-stu-id="92213-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="92213-1016">ไปที่ **แบบสอบถาม** \> **ออกแบบ** \> **รายงานแบบสอบถาม (ที่ให้บริการโดย ER)**</span><span class="sxs-lookup"><span data-stu-id="92213-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="92213-1017">ในกล่องโต้ตอบ ในฟิลด์ **การแม็ปรูปแบบ** เลือก **รายงานแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="92213-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="92213-1018">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="92213-1018">Select **OK**.</span></span>
4. <span data-ttu-id="92213-1019">ในกล่องโต้ตอบ **พารามิเตอร์รายงานทางอิเล็กทรอนิกส์** บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้ตั้งค่าคอนฟิกตัวเลือกการกรองเพื่อให้รวมเฉพาะแบบสอบถาม **SBCCrsExam** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="92213-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="92213-1020">เลือก **ตกลง** เพื่อยืนยันตัวเลือกการกรอง</span><span class="sxs-lookup"><span data-stu-id="92213-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="92213-1021">บนแท็บด่วน **ปลายทาง** สังเกตว่าฟิลด์ **ผลลัพธ์** ตั้งค่าเป็น **หน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="92213-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="92213-1022">ถ้าคุณต้องการเปลี่ยนปลายทางที่ตั้งค่าคอนฟิกไว้ ให้เลือก **เปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="92213-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![กล่องโต้ตอบรันไทม์ของรายงาน ER ซึ่งคุณสามารถเปลี่ยนปลายทางที่ตั้งค่าคอนฟิกได้](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="92213-1024">เลือก **ตกลง** เพื่อเรียกใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="92213-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="92213-1025">ตรวจทานรายงานที่สร้างในรูปแบบ PDF</span><span class="sxs-lookup"><span data-stu-id="92213-1025">Review the generated report in PDF format.</span></span>

    ![การแสดงตัวอย่างบนหน้าจอของรายงานที่สร้างในรูปแบบ PDF](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="92213-1027">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="92213-1027">Additional resources</span></span>

- [<span data-ttu-id="92213-1028">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="92213-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="92213-1029">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="92213-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="92213-1030">ออกแบบรายงานหลายภาษา</span><span class="sxs-lookup"><span data-stu-id="92213-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="92213-1031">API กรอบงานการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="92213-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="92213-1032">ฟังก์ชัน CASE</span><span class="sxs-lookup"><span data-stu-id="92213-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="92213-1033">ฟังก์ชัน CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="92213-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="92213-1034">ฟังก์ชัน DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="92213-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="92213-1035">ฟังก์ชัน FILTER</span><span class="sxs-lookup"><span data-stu-id="92213-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="92213-1036">ฟังก์ชัน FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="92213-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="92213-1037">ฟังก์ชัน FORMAT</span><span class="sxs-lookup"><span data-stu-id="92213-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="92213-1038">ฟังก์ชัน IF</span><span class="sxs-lookup"><span data-stu-id="92213-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="92213-1039">ฟังก์ชัน ORDERBY</span><span class="sxs-lookup"><span data-stu-id="92213-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="92213-1040">ฟังก์ชัน SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="92213-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]