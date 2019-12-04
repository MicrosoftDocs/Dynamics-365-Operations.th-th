---
title: สร้างฟอร์ม FTI ที่สามารถพิมพ์ได้
description: หัวข้อนี้อธิบายวิธีการใช้กรอบงานการรายงานอิเล็กทรอนิกส์ (ER) เพื่อสร้างฟอร์มของใบแจ้งหนี้ข้อความอิสระที่สามารถพิมพ์ได้ (FTI) เป็นเอกสาร Microsoft Office
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0bb817de583c231aa55fa81b9e28d788505e0a1f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771294"
---
# <a name="generate-printable-fti-forms"></a><span data-ttu-id="eb74f-103">สร้างแบบฟอร์ม FTI ที่สามารถพิมพ์ได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-103">Generate printable FTI forms</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="eb74f-104">กรอบงานการรายงานอิเล็กทรอนิกส์ (ER) ช่วยให้คุณสามารถสร้างฟอร์มของใบแจ้งหนี้ข้อความอิสระที่สามารถพิมพ์ได้ (FTI) เป็นเอกสาร Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="eb74f-104">The Electronic reporting (ER) framework lets you generate printable free text invoice (FTI) forms as Microsoft Office documents.</span></span> <span data-ttu-id="eb74f-105">หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการสร้างการตั้งค่าคอนฟิกของคุณเอง ตลอดจนรายละเอียดของเท็มเพลตการตั้งค่าคอนฟิกที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="eb74f-105">This topic provides information about how to build your own configurations as well as details of available configuration templates.</span></span>

## <a name="overview"></a><span data-ttu-id="eb74f-106">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="eb74f-106">Overview</span></span>

<span data-ttu-id="eb74f-107">นอกเหนือจากความสามารถที่มีอยู่ของการสร้างแบบฟอร์ม FTI ที่สามารถพิมพ์ได้โดยใช้ Microsoft SQL Server Reporting Services (SSRS) ขณะนี้คุณสามารถใช้กรอบงาน ER ได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-107">In addition to the existing capability of generating printable FTI forms by using Microsoft SQL Server Reporting Services (SSRS), you can now use the ER framework.</span></span> <span data-ttu-id="eb74f-108">คุณสามารถจัดการฟอร์ม FTI ที่สามารถพิมพ์ได้ใน Microsoft Office Excel และ Word</span><span class="sxs-lookup"><span data-stu-id="eb74f-108">You can manage printable FTI forms in Microsoft Office Excel and Word.</span></span> <span data-ttu-id="eb74f-109">คุณยังสามารถปรับเปลี่ยนโครงร่าง ลำดับข้อมูล และการจัดรูปแบบได้ เพื่อให้ตรงกับข้อกำหนดเฉพาะโดยไม่ทำการเปลี่ยนแปลงรหัส</span><span class="sxs-lookup"><span data-stu-id="eb74f-109">You can also modify the layout, data flow, and formatting to meet specific requirements without making code changes.</span></span>

> [!NOTE]
> <span data-ttu-id="eb74f-110">ถ้าคุณต้องการเริ่มต้นด้วยภาพรวมของการตั้งค่าคอนฟิก ER ที่มีอยู่ สำหรับตัวอย่างนี้ของโซลูชันฟอร์ม FTI ที่สามารถพิมพ์ได้ คุณสามารถไปยังส่วน **ดาวน์โหลดการตั้งค่าคอนฟิก ER ตัวอย่างเพื่อสร้างแบบฟอร์ม FTI ที่สามารถพิมพ์ได้** ในภายหลังในหัวข้อนี้ได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-110">If you want to start with an overview of existing ER configurations for this sample of the printable FTI forms solution, you can go directly to section **Download sample ER configurations to generate printable FTI forms** later in this topic.</span></span>

## <a name="create-customized-configurations-for-fti-printable-forms"></a><span data-ttu-id="eb74f-111">สร้างการตั้งค่าคอนฟิกแบบกำหนดเองสำหรับฟอร์ม FTI ที่สามารถพิมพ์ได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-111">Create customized configurations for FTI printable forms</span></span>
<span data-ttu-id="eb74f-112">ในฐานะที่เป็นส่วนหนึ่งของโซลูชันแบบกำหนดเองของคุณสำหรับฟอร์ม FTI ที่สามารถพิมพ์ได้ คุณต้องสร้างชุดของการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="eb74f-112">As part of your customized solution for printable FTI forms, you must create a set of ER configurations.</span></span>

### <a name="configure-the-er-data-model"></a><span data-ttu-id="eb74f-113">ตั้งค่าคอนฟิกแบบจำลองข้อมูล ER</span><span class="sxs-lookup"><span data-stu-id="eb74f-113">Configure the ER data model</span></span>
<span data-ttu-id="eb74f-114">แอพลิเคชันของคุณต้องมีการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER ที่ประกอบด้วยแบบจำลองข้อมูลที่อธิบายโดเมนธุรกิจการออกใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="eb74f-114">Your application must include the ER data model configuration that contains a data model that describes the customer invoicing business domain.</span></span> <span data-ttu-id="eb74f-115">ตามข้อกำหนด ชื่อของแบบจำลองข้อมูลต้องเป็น **CustomersInvoicing**</span><span class="sxs-lookup"><span data-stu-id="eb74f-115">As a requirement, the name of the data model must be **CustomersInvoicing**.</span></span> <span data-ttu-id="eb74f-116">สำหรับข้อมูลเกี่ยวกับวิธีการออกแบบแบบจำลองข้อมูล ER ดู [ออกแบบโดเมนของรูปแบบที่เฉพาะเจาะจงของ ER](tasks/er-design-domain-specific-data-model-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="eb74f-116">For information about how to design ER data models, see [ER Design domain specific data model](tasks/er-design-domain-specific-data-model-2016-11.md).</span></span>

### <a name="configure-the-er-model-mapping"></a><span data-ttu-id="eb74f-117">ตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="eb74f-117">Configure the ER model mapping</span></span>
<span data-ttu-id="eb74f-118">แอพลิเคชันของคุณต้องมีการแม็ปแบบจำลอง ER สำหรับแบบจำลองข้อมูล CustomersInvoicing</span><span class="sxs-lookup"><span data-stu-id="eb74f-118">Your application must include the ER model mapping for the CustomersInvoicing data model.</span></span> <span data-ttu-id="eb74f-119">การแม็ปแบบจำลองสามารถอยู่ในการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER หรือการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="eb74f-119">The model mapping can be in either the ER data model configuration or the ER model mapping configuration.</span></span> <span data-ttu-id="eb74f-120">อย่างไรก็ตาม ชื่อของตัวอธิบายรากของการแม็ปแบบจำลองต้องเป็น **FreeTextInvoice**</span><span class="sxs-lookup"><span data-stu-id="eb74f-120">However, the name of the root descriptor of the model mapping must be **FreeTextInvoice**.</span></span>

<span data-ttu-id="eb74f-121">การแม็ปต้องประกอบด้วยแหล่งข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="eb74f-121">The mapping must contain the following data sources:</span></span>

- <span data-ttu-id="eb74f-122">ชนิดแหล่งข้อมูล: **เรกคอร์ดตาราง**</span><span class="sxs-lookup"><span data-stu-id="eb74f-122">Data source type: **Table records**</span></span>

    - <span data-ttu-id="eb74f-123">ต้องตั้งชื่อแหล่งข้อมูลนี้เป็น **CustInvoiceJour**</span><span class="sxs-lookup"><span data-stu-id="eb74f-123">This data source must be named **CustInvoiceJour**.</span></span>
    - <span data-ttu-id="eb74f-124">ต้องอ้างอิงไปยังตารางแอพลิเคชัน CustInvoiceJour</span><span class="sxs-lookup"><span data-stu-id="eb74f-124">It must refer to the CustInvoiceJour application table.</span></span>
    - <span data-ttu-id="eb74f-125">มีการใช้ขณะรันไทม์เพื่อส่งผ่านจากแอพลิเคชันไปยังแบบจำลอง ER ที่แม็ปรายการของใบแจ้งหนี้ที่ได้ถูกเลือกสำหรับการพิมพ์</span><span class="sxs-lookup"><span data-stu-id="eb74f-125">It's used at runtime to pass from the application to the ER model mapping the list of invoices that have been selected for printing.</span></span>

- <span data-ttu-id="eb74f-126">ชนิดแหล่งข้อมูล: **ออบเจ็กต์**</span><span class="sxs-lookup"><span data-stu-id="eb74f-126">Data source type: **Object**</span></span>

    - <span data-ttu-id="eb74f-127">ต้องตั้งชื่อแหล่งข้อมูลนี้เป็น **PrintMgmtPrintSettingDetail**</span><span class="sxs-lookup"><span data-stu-id="eb74f-127">This data source must be named **PrintMgmtPrintSettingDetail**.</span></span>
    - <span data-ttu-id="eb74f-128">ต้องอ้างอิงไปยังคลาสแอพลิเคชัน **PrintMgmtPrintSettingDetail**</span><span class="sxs-lookup"><span data-stu-id="eb74f-128">It must refer to the **PrintMgmtPrintSettingDetail** application class.</span></span>
    - <span data-ttu-id="eb74f-129">มีการใช้ขณะรันไทม์เพื่อส่งผ่านจากแอพลิเคชันไปยังรายละเอียดการแม็ปแบบจำลอง ER ของการตั้งค่าการจัดการการพิมพ์สำหรับรูปแบบ ER ที่กำลังรันอยู่</span><span class="sxs-lookup"><span data-stu-id="eb74f-129">It's used at runtime to pass from the application to the ER model mapping details of the print management settings for the ER format that is running.</span></span>

<span data-ttu-id="eb74f-130">รายละเอียดของการรวมแอพลิเคชันกับกรอบงาน ER สามารถพบได้ในคลาส **ERPrintMgmtReportFormatSubscriber** (แบบจำลองการรวมชุดแอพลิเคชัน ER) ในรหัสแหล่งที่มาของแอพลิเคชันได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-130">The details of the application integration with the ER framework can be found in the **ERPrintMgmtReportFormatSubscriber** class (ER Application Suite integration model) in the source code of the application.</span></span>

<span data-ttu-id="eb74f-131">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการออกแบบของการแม็ปแบบจำลอง ER ดู [กำหนดการแม็ปแบบจำลอง ER และเลือกแหล่งข้อมูลสำหรับรายการเหล่านั้น](tasks/er-define-model-mapping-select-data-sources-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="eb74f-131">For more information about the design of ER model mappings, see [Define ER model mappings and select data sources for them](tasks/er-define-model-mapping-select-data-sources-2016-11.md).</span></span>

### <a name="configure-the-er-format"></a><span data-ttu-id="eb74f-132">ตั้งค่าคอนฟิกรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="eb74f-132">Configure the ER format</span></span>
<span data-ttu-id="eb74f-133">ในอินสแตนซ์แอพลิเคชันของคุณ คุณต้องมีการตั้งค่าคอนฟิกรูปแบบ ER ที่จะใช้ในการสร้างแบบฟอร์ม FTI</span><span class="sxs-lookup"><span data-stu-id="eb74f-133">In your application instance, you must have the ER format configuration that will be used to generate FTI forms.</span></span> 

> [!NOTE]
> <span data-ttu-id="eb74f-134">ต้องมีการสร้างการตั้งค่าคอนฟิกรูปแบบนี้สำหรับรูปแบบจำลองข้อมูล CustomersInvoicing และจะต้องใช้การแม็ปแบบจำลองที่มีตัวอธิบายราก **FreeTextInvoice**</span><span class="sxs-lookup"><span data-stu-id="eb74f-134">This format configuration must be created for the CustomersInvoicing data model, and it must use the model mapping that has the **FreeTextInvoice** root descriptor.</span></span>

<span data-ttu-id="eb74f-135">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกรูปแบบ ER ดู [สร้างการตั้งค่าคอนฟิกรูปแบบของ ER (พฤศจิกายน 2016)](tasks/er-format-configuration-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="eb74f-135">For information about how to configure ER formats, see [ER Create a format configuration (November 2016)](tasks/er-format-configuration-2016-11.md).</span></span> <span data-ttu-id="eb74f-136">สำหรับข้อมูลเกี่ยวกับวิธีการออกแบบรูปแบบ ER ที่จะสร้างรายงานในรูปแบบ OpenXML ดู [ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML ของ ER (พฤศจิกายน 2016)](tasks/er-design-reports-openxml-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="eb74f-136">For information about how to design ER formats to generate reports in OpenXML format, see [ER Design a configuration for generating reports in OPENXML format (November 2016)](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="configure-print-management"></a><span data-ttu-id="eb74f-137">ตั้งค่าคอนฟิกการจัดการการพิมพ์</span><span class="sxs-lookup"><span data-stu-id="eb74f-137">Configure print management</span></span>
<span data-ttu-id="eb74f-138">เมื่อต้องการสร้างฟอร์ม FTI โดยใช้กรอบงาน ER คุณสามารถกำหนดรูปแบบ ER ได้ในลักษณะเดียวกับที่คุณกำหนดรายงาน SSRS</span><span class="sxs-lookup"><span data-stu-id="eb74f-138">To generate FTI forms by using the ER framework, you can assign ER formats in the same way that you assign SSRS reports.</span></span> <span data-ttu-id="eb74f-139">เมื่อต้องการเชื่อมโยงรูปแบบ ER กับ FTIs ของลูกหนี้บัญชีทั้งหมด ไปที่ **บัญชีลูกหนี้** \> **การตั้งค่า** \> **ฟอร์ม** \> **การตั้งค่าแบบฟอร์ม** \> **ทั่วไป** \> **การจัดการการพิมพ์** \> **ใบแจ้งหนี้ข้อความอิสระ** \> **ดั้งเดิม**</span><span class="sxs-lookup"><span data-stu-id="eb74f-139">To associate the ER format with all Accounts receivable FTIs, go to **Accounts receivable** \> **Setup** \> **Forms** \> **Form setup** \> **General** \> **Print management** \> **Free text invoice** \> **Original**.</span></span> <span data-ttu-id="eb74f-140">เพื่อเชื่อมโยงรูปแบบ ER กับใบแจ้งหนี้หรือลูกค้าเฉพาะ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="eb74f-140">To associate the ER format with a specific customer or invoice, follow these steps.</span></span>

1. <span data-ttu-id="eb74f-141">ไปที่ **บัญชีลูกหนี้** \> **ใบแจ้งหนี้** \> **ใบแจ้งหนี้ข้อความอิสระทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="eb74f-141">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="eb74f-142">เลือก FTI เพื่อเชื่อมโยงกับรูปแบบ ER และเปิดหน้า **การตั้งค่าการจัดการการพิมพ์**</span><span class="sxs-lookup"><span data-stu-id="eb74f-142">Select the FTI to associate the ER format with, and open the **Print management setup** page.</span></span>
3. <span data-ttu-id="eb74f-143">เลือกระดับเอกสารเพื่อระบุขอบเขตของใบแจ้งหนี้สำหรับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="eb74f-143">Select the document level to specify the scope of invoices for processing.</span></span>
4. <span data-ttu-id="eb74f-144">เลือกรูปแบบ ER สำหรับระดับเอกสารที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="eb74f-144">Select the ER format for the specified document level.</span></span>

![การตั้งค่าการจัดการงานพิมพ์](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> <span data-ttu-id="eb74f-146">เฉพาะรูปแบบ ER ที่ใช้ตัวอธิบายราก **FreeTextInvoice** ของแบบจำลองข้อมูล **CustomersInvoicing** ปรากฏขึ้นในฟิลด์ **การค้นหารูปแบบรายงาน** สำหรับรูปแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="eb74f-146">Only ER formats that use the **FreeTextInvoice** root descriptor of the **CustomersInvoicing** data model appear in the **Report format lookup** field for the selected format.</span></span>

## <a name="generate-fti-forms"></a><span data-ttu-id="eb74f-147">สร้างแบบฟอร์ม FTI</span><span class="sxs-lookup"><span data-stu-id="eb74f-147">Generate FTI forms</span></span>
<span data-ttu-id="eb74f-148">แบบฟอร์ม FTI ถูกสร้างในกรอบงาน ER ในลักษณะเดียวกับที่รายงาน SSRS ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="eb74f-148">FTI forms are generated in the ER framework in the same way that SSRS reports are generated.</span></span>

<span data-ttu-id="eb74f-149">ในการสร้างแบบฟอร์ม FTI คุณสามารถเลือกใบแจ้งหนี้โดยช่วง หรือโดยการเลือก อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="eb74f-149">To generate FTI forms, you can select invoices either by range or by selection.</span></span> 

![การเลือกใบแจ้งหนี้](media/FTIbyGER-InvoiceSelection.png)

![การแสดงตัวอย่างใบแจ้งหนี้](media/FTIbyGER-InvoiceExcelPreview.png)

<span data-ttu-id="eb74f-152">เมื่อคุณใช้รูปแบบ ER เพื่อพิมพ์แบบฟอร์ม FTI ด้วยวิธีนี้ ปลายทางไฟล์ ER เริ่มต้นจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="eb74f-152">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="eb74f-153">คุณไม่สามารถเปลี่ยนปลายทางได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-153">You can't change the destination.</span></span> <span data-ttu-id="eb74f-154">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกปลายทาง ER สำหรับรูปแบบ ER ดู [ปปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-destinations.md)</span><span class="sxs-lookup"><span data-stu-id="eb74f-154">For more information about how to configure the ER destinations for ER formats, see [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span>

<span data-ttu-id="eb74f-155">นอกจากนี้ คุณยังสามารถสร้างฟอร์ม FTI ได้ เมื่อคุณลงรายการบัญชี FTI ด้วยการเปิดใช้งาน **พิมพ์ใบแจ้งหนี้** และปิดใช้งาน **ใช้ปลายทางการจัดการการพิมพ์** ได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-155">You can also generate FTI forms when you post an FTI, by turning **Print invoice** on and turning **Use print management destinations** off.</span></span>

> [!NOTE]
> <span data-ttu-id="eb74f-156">เมื่อคุณใช้รูปแบบ ER เพื่อพิมพ์แบบฟอร์ม FTI ด้วยวิธีนี้ ปลายทางไฟล์ ER เริ่มต้นจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="eb74f-156">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="eb74f-157">คุณสามารถเปลี่ยนปลายทางเริ่มต้นในช่วงรันไทม์ได้ ถ้ามีการตั้งค่าคอนฟิกปลายทางแล้ว</span><span class="sxs-lookup"><span data-stu-id="eb74f-157">You can change the default destination at runtime if the destination has already been configured.</span></span> <span data-ttu-id="eb74f-158">เพื่อเปลี่ยนปลายทาง คุณต้องมีสิทธิ์ความปลอดภัยต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="eb74f-158">To change the destination, you must have the following security privilege:</span></span>
>
> - <span data-ttu-id="eb74f-159">**ชื่อ:** ERFormatDestinationRuntimeMaintain</span><span class="sxs-lookup"><span data-stu-id="eb74f-159">**Name:** ERFormatDestinationRuntimeMaintain</span></span>
> - <span data-ttu-id="eb74f-160">**ป้ายชื่อ:** รักษาปลายทางรูปแบบการรายงานทางอิเล็กทรอนิกส์ระหว่างรันไทม์</span><span class="sxs-lookup"><span data-stu-id="eb74f-160">**Label:** Maintain electronic reporting format destination during runtime</span></span>

![ปลายทางการรายงานทางอิเล็กทรอนิกส์](media/FTIbyGER-ERFileDestinationSetting.png)

![ปลายทางของรูปแบบการรายงานทางอิเล็กทรอนิกส์](media/FTIbyGER-ERFileDestinationUsage.png)

<span data-ttu-id="eb74f-163">ในปัจจุบัน กรอบงาน ER สนับสนุนปลายทางต่อไปนี้สำหรับเอกสารที่สร้างขึ้น:</span><span class="sxs-lookup"><span data-stu-id="eb74f-163">The ER framework currently supports the following destinations for generated documents:</span></span>

- <span data-ttu-id="eb74f-164">**ไฟล์ที่ดาวน์โหลด** – แบบฟอร์มที่สร้างถูกเสนอเป็นการดาวน์โหลดที่คุณสามารถบันทึกได้โดยใช้เบราเซอร์</span><span class="sxs-lookup"><span data-stu-id="eb74f-164">**Downloaded file** – Generated forms are offered as downloads that you can save by using the browser.</span></span>
- <span data-ttu-id="eb74f-165">**หน้าจอ** – Microsoft Office 365 Excel ถูกใช้ในการแสดงตัวอย่างฟอร์ม FTI ที่สร้างขึ้นในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="eb74f-165">**Screen** – Microsoft Office 365 Excel is used to preview generated FTI forms in Excel format.</span></span>
- <span data-ttu-id="eb74f-166">**โฟลเดอร์ SharePoint** – แบบฟอร์มที่สร้างขึ้นจะถูกเก็บไว้ตามการตั้งค่าของกรอบงานการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="eb74f-166">**SharePoint folder** – Generated forms are stored based on the settings of the Document management framework.</span></span>
- <span data-ttu-id="eb74f-167">**ที่เก็บถาวรของแอพลิเคชัน** – แบบฟอร์มที่สร้างขึ้นจะถูกเก็บเป็นสิ่งที่แนบมาของเรกคอร์ดล็อกการดำเนินการในที่จัดเก็บ Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="eb74f-167">**Application archive** – Generated forms are stored as attachments of execution log records in the Microsoft Azure Storage.</span></span>
- <span data-ttu-id="eb74f-168">**อีเมล** – แบบฟอร์มที่สร้างขึ้นจะถูกส่งเป็นสิ่งที่แนบทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="eb74f-168">**Email** – Generated forms are sent as email attachments.</span></span>

> [!NOTE]
> <span data-ttu-id="eb74f-169">คุณไม่สามารถส่งฟอร์ม FTI ที่สร้างขึ้นโดยตรงไปยังเครื่องพิมพ์ได้ เนื่องจากการพิมพ์โดยตรงที่ใช้ Dynamics Printer Routing Agent ไม่ได้รับการสนับสนุนในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="eb74f-169">You can't send the FTI forms that are generated directly to the printer, because direct printing that uses the Dynamics Printer Routing Agent isn't currently supported.</span></span>

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a><span data-ttu-id="eb74f-170">ดาวน์โหลดการตั้งค่าคอนฟิก ER ตัวอย่าง เพื่อสร้างฟอร์ม FTI ที่สามารถพิมพ์ได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-170">Download sample ER configurations to generate printable FTI forms</span></span>
<span data-ttu-id="eb74f-171">คุณสามารถดาวน์โหลดการตั้งค่าคอนฟิก ER ตัวอย่าง เพื่อใช้เป็นเท็มเพลตสำหรับโซลูชัน FTI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="eb74f-171">You can download sample ER configurations to use as a template for your FTI solution.</span></span> <span data-ttu-id="eb74f-172">การตั้งค่าคอนฟิกจะถูกจัดเก็บอยู่ในไลบรารีสินทรัพย์ที่ใช้ร่วมกันใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="eb74f-172">The configurations are stored in the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="eb74f-173">การตั้งค่าคอนฟิกรวม:</span><span class="sxs-lookup"><span data-stu-id="eb74f-173">The configurations include:</span></span>

- <span data-ttu-id="eb74f-174">การตั้งค่าคอนฟิก **แบบจำลองการออกใบแจ้งหนี้ของลูกค้า** ประกอบด้วย รูปแบบแบบจำลองข้อมูลที่จำเป็นและการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="eb74f-174">The **Customer invoicing model** configuration contains the required data model and model mapping.</span></span>
- <span data-ttu-id="eb74f-175">การตั้งค่าคอนฟิก **รายงาน FTI ของลูกค้า (GER)** ประกอบด้วย รูปแบบตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="eb74f-175">The **Customer FTI report (GER)** configuration contains the sample format.</span></span>

> [!NOTE]
> <span data-ttu-id="eb74f-176">มีการสร้างการตั้งค่าคอนฟิกเหล่านี้เป็นตัวอย่างเพื่อช่วยในการอธิบายสถานการณ์ที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-176">These configurations have been created as samples to help clarify possible scenarios.</span></span> <span data-ttu-id="eb74f-177">อนาคตของการตั้งค่าคอนฟิกเหล่านี้ขึ้นอยู่กับผลลัพธ์ของการประเมินนี้ และข้อคิดเห็นใดๆ ที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="eb74f-177">The future of these configurations depends on the results of this evaluation and any feedback that is received.</span></span>

### <a name="features-that-are-implemented-in-the-sample-er-format"></a><span data-ttu-id="eb74f-178">ลักษณะการทำงานที่ถูกใช้อยู่ในรูปแบบ ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="eb74f-178">Features that are implemented in the sample ER format</span></span>
<span data-ttu-id="eb74f-179">ในการตั้งค่าคอนฟิกรูปแบบ ER ตัวอย่าง แฟ้ม Excel จะถูกใช้เป็นเท็มเพลตเพื่อสร้างแบบฟอร์ม FTI</span><span class="sxs-lookup"><span data-stu-id="eb74f-179">In the sample ER format configuration, an Excel file is used as a template to generate FTI forms.</span></span>

![ตัวออกแบบรูปแบบ](media/FTIbyGER-ERFormat.png)

<span data-ttu-id="eb74f-181">ในปัจจุบัน รูปแบบ ER ตัวอย่างนี้สนับสนุนลักษณะการทำงานต่อไปนี้ในการสร้างแบบฟอร์ม FTI:</span><span class="sxs-lookup"><span data-stu-id="eb74f-181">Currently, this sample ER format supports the following features to generate FTI forms:</span></span>

- <span data-ttu-id="eb74f-182">แบบฟอร์ม FTI จะถูกสร้างขึ้นสำหรับทั้งใบแจ้งหนี้เดิมที่มีการลงรายการบัญชี และใบแจ้งหนี้ต้นฉบับที่ยังไม่ได้ถูกลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="eb74f-182">FTI forms are generated for both original invoices that have been posted and original invoices that haven't yet been posted.</span></span> <span data-ttu-id="eb74f-183">ใบแจ้งหนี้และใบลดหนี้ที่แก้ไขจะไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="eb74f-183">Corrected invoices and credit notes aren't supported.</span></span>
- <span data-ttu-id="eb74f-184">แบบฟอร์ม FTI ถูกสร้างขึ้นในภาษาของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="eb74f-184">FTI forms are generated in the invoice language.</span></span> <span data-ttu-id="eb74f-185">รูปแบบของค่าและวันที่ในแบบฟอร์มที่สร้างขึ้น ขึ้นอยู่กับการตั้งค่าของตำแหน่งที่ตั้งไคลเอนต์ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="eb74f-185">The format of values and dates in the generated forms is based on the settings of the user's client locale.</span></span>
- <span data-ttu-id="eb74f-186">ใบแจ้งหนี้ที่สร้างแสดงการแจ้งเตือนความไม่พร้อมใช้งานของข้อมูล ถ้าไม่มีรายการในใบแจ้งหนี้ที่ถูกประมวลผล</span><span class="sxs-lookup"><span data-stu-id="eb74f-186">Generated invoices show data unavailability notifications if there are no lines in the invoices that are processed.</span></span>
- <span data-ttu-id="eb74f-187">ส่วนหัวของใบแจ้งหนี้ที่สร้างขึ้นเป็นไปตามรูปแบบกระดาษที่ถูกเลือกสำหรับแบบฟอร์ม FTI ในหน้า **พารามิเตอร์ลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="eb74f-187">Generated invoice headers are based on the paper format that has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="eb74f-188">รายละเอียดของบริษัทปรากฏขึ้นในส่วนหัวของแบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้นเท่านั้น ถ้ารูปแบบกระดาษว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="eb74f-188">Company details appear in the header of the generated invoice form only if the paper format is blank.</span></span>
- <span data-ttu-id="eb74f-189">แบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้นแสดงบริษัทและเลขยกเว้นภาษีของลูกค้า เมื่อมีการเลือกตัวเลือกที่เหมาะสมสำหรับแบบฟอร์ม FTI ในหน้า **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="eb74f-189">Generated invoice forms show company and customer tax exempt numbers when the appropriate option has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="eb74f-190">ส่วนของรายการใบแจ้งหนี้และยอดรวมใบแจ้งหนี้ที่สร้างขึ้น แสดงค่าเริ่มต้นรายละเอียดจำนวนเงินของใบแจ้งหนี้ในสกุลเงินการลงทะเบียนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="eb74f-190">The generated invoice lines and invoice totals sections show the default invoice's monetary details in the invoice registration currency.</span></span>
- <span data-ttu-id="eb74f-191">ส่วนของผลรวมใบแจ้งหนี้ที่สร้างขึ้นสามารถแสดงรายละเอียดจำนวนเงินในสกุลเงินยูโรและสกุลเงินการลงทะเบียนใบแจ้งหนี้ เมื่อตัวเลือก **พิมพ์ยอดเงินในสกุลเงินที่แสดงเป็นยูโร** ถูกเปิดใช้ในหน้า  **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="eb74f-191">The generated invoice totals section can show monetary details in the euro currency and the invoice registration currency when the **Print amount in currency representing the euro** option is enabled on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="eb74f-192">ฟอร์มใบแจ้งหนี้ที่สร้างขึ้นแสดงบันทึกย่อใบแจ้งหนี้ของกระบวนการใดๆ ที่พร้อมใช้งาน ตามการตั้งค่าในหน้า **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="eb74f-192">Generated invoice forms show any process invoice notes that are available, based on settings on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="eb74f-193">บันทึกย่อถูกรวมสำหรับทั้งใบแจ้งหนี้ทั้งหมดและรายการใบแจ้งหนี้แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="eb74f-193">Notes are included for both the whole invoice and each invoice line.</span></span>
- <span data-ttu-id="eb74f-194">แบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้นรวมบันทึกย่อสำหรับแบบฟอร์ม FTI ของลูกค้า และภาษาใบแจ้งหนี้ที่ประมวลผล เมื่อมีการตั้งค่าคอนฟิกในรายการบันทึกย่อของแบบฟอร์ม AR</span><span class="sxs-lookup"><span data-stu-id="eb74f-194">Generated invoice forms include notes for the customer FTI form and the processing invoice language when they have been configured in the AR form notes list.</span></span>
- <span data-ttu-id="eb74f-195">โดยขึ้นอยู่กับการตั้งค่าการจัดการการพิมพ์ ใบแจ้งหนี้ที่สร้างขึ้นรวมข้อความท้ายกระดาษที่กำหนดเอง เมื่อมีการตั้งค่าคอนฟิกสำหรับภาษาใบแจ้งหนี้ รูปแบบ ER และขอบเขตเอกสาร FTI</span><span class="sxs-lookup"><span data-stu-id="eb74f-195">Depending on the Print management settings, generated invoices include custom footer text when it has been configured for the invoice language, the ER format, and the FTI document scope.</span></span>
- <span data-ttu-id="eb74f-196">ส่วนผลรวมของแบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้นรวมข้อมูลส่วนลดเงินสดใดๆ ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="eb74f-196">The totals section of generated invoice forms includes any cash discount information that is available.</span></span>
- <span data-ttu-id="eb74f-197">ส่วนของกำหนดการชำระเงินของแบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้นรวมรายละเอียดกำหนดการชำระเงินใดๆ ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="eb74f-197">The payment schedule section of generated invoice forms includes any payment schedule details that are available.</span></span>
- <span data-ttu-id="eb74f-198">ส่วนเพิ่มราคาของแบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้นรวมธุรกรรมค่าธรรมเนียมใดๆ ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="eb74f-198">The markup section of generated invoice forms includes any charges transactions that are available.</span></span>
- <span data-ttu-id="eb74f-199">แบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้นมีรายละเอียดภาษีขาย ซึ่งขึ้นอยู่กับการตั้งค่า **ข้อมูลจำเพาะเกี่ยวกับภาษีขาย** บนหน้า **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="eb74f-199">Generated invoice forms include sales tax details, based on the **Sales tax specification** setting on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="eb74f-200">ส่วนนี้สามารถแสดงรายละเอียดภาษีได้ในสกุลเงินการลงทะเบียนใบแจ้งหนี้เท่านั้น หรือในสกุลเงินการลงทะเบียนใบแจ้งหนี้และสกุลเงินทางบัญชีของบริษัทในเวลาเดียวกัน อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="eb74f-200">This section can show tax details either in the invoice registration currency only, or in the invoice registration currency and the company accounting currency at the same time.</span></span>
- <span data-ttu-id="eb74f-201">แบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้นแสดงรายละเอียดการแจ้งเตือนเดบิตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="eb74f-201">Generated invoice forms show direct debit notification details.</span></span> <span data-ttu-id="eb74f-202">ตัวอย่างเช่น จะแสดงเมื่อมีการเลือกวิธีการชำระเงินที่มีรหัสข้อบังคับการหักบัญชีเงินฝากอัตโนมัติแบบบังคับสำหรับใบแจ้งหนี้ เมื่อมีการลงทะเบียนใบแจ้งหนี้ที่ประมวลผลในสกุลเงินยูโร และเมื่อมีการกำหนดข้อบังคับการหักบัญชีเงินฝากอัตโนมัติสำหรับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="eb74f-202">For example, they show when the method of payment that has the mandatory direct debit mandate ID was selected for the invoice, when the processing invoice was registered in the euro currency, and when the direct debit mandate ID was defined for the invoice.</span></span>
- <span data-ttu-id="eb74f-203">ใบแจ้งหนี้ที่สร้างขึ้นแสดงรายละเอียดการชำระเงินล่วงหน้าใดๆ ที่พร้อมใช้งานสำหรับใบแจ้งหนี้ที่ลงรายการบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="eb74f-203">Generated invoices show any prepayment details that are available for posted invoices.</span></span>
- <span data-ttu-id="eb74f-204">แบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้นสามารถส่งให้ลูกค้าในใบแจ้งหนี้เป็นสิ่งที่แนบทางอีเมลได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-204">Generated invoice forms can be sent to an invoice customer as an email attachment.</span></span> <span data-ttu-id="eb74f-205">ควรตั้งค่าคอนฟิกปลายทางไฟล์ ER ที่เหมาะสมสำหรับรูปแบบ ER ที่กำลังถูกใช้</span><span class="sxs-lookup"><span data-stu-id="eb74f-205">The appropriate ER file destination should be configured for the ER format that is being used.</span></span>

### <a name="countryregion-specific-features"></a><span data-ttu-id="eb74f-206">ลักษณะการทำงานเฉพาะประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="eb74f-206">Country/region-specific features</span></span> 
<span data-ttu-id="eb74f-207">ลักษณะการทำงานเฉพาะประเทศ/ภูมิภาคดังต่อไปนี้ถูกรวมในรูปแบบ ER ตัวอย่าง ที่จะแสดงวิธีการจัดการความต้องการเฉพาะในการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="eb74f-207">The following country/region-specific features are included in the sample ER format to show how specific requirements can be handled in ER configurations.</span></span>

#### <a name="norway"></a><span data-ttu-id="eb74f-208">นอร์เวย์</span><span class="sxs-lookup"><span data-stu-id="eb74f-208">Norway</span></span>
<span data-ttu-id="eb74f-209">เงื่อนไขการทะเบียนองค์กรปรากฏอยู่บนส่วนหัวของแบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้น เมื่อมีการประมวลผลใบแจ้งหนี้สำหรับนิติบุคคลที่มีการตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="eb74f-209">The Enterprise register term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="eb74f-210">มีการใช้บริบทประเทศ/ภูมิภาคสำหรับนอร์เวย์</span><span class="sxs-lookup"><span data-stu-id="eb74f-210">The country/region context for Norway is used.</span></span>
- <span data-ttu-id="eb74f-211">พารามิเตอร์ **พิมพ์ Foretaksregisteret** ใช้งานอยู่ในเอกสาร Sales</span><span class="sxs-lookup"><span data-stu-id="eb74f-211">The **Print Foretaksregisteret** parameter is active on sales documents.</span></span>

#### <a name="spain"></a><span data-ttu-id="eb74f-212">สเปน</span><span class="sxs-lookup"><span data-stu-id="eb74f-212">Spain</span></span>
<span data-ttu-id="eb74f-213">เงื่อนไข **กฎเกณฑ์พิเศษสำหรับวิธีการจัดทำบัญชีเงินสด** ถูกใส่บนส่วนหัวของแบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้น เมื่อมีการประมวลผลใบแจ้งหนี้สำหรับนิติบุคคลที่มีการตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="eb74f-213">The **Special regime for cash accounting method** term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="eb74f-214">มีการใช้บริบทประเทศ/ภูมิภาคสำหรับสเปน</span><span class="sxs-lookup"><span data-stu-id="eb74f-214">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="eb74f-215">กฎเกณฑ์พิเศษสำหรับวิธีการจัดทำบัญชีเงินสดถูกเปิดใช้ในวันที่ประมวลผลใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="eb74f-215">The special regime for the cash accounting method is enabled on the invoice processing date.</span></span>

<span data-ttu-id="eb74f-216">เมื่อรายละเอียดส่วนลดเงินสด เช่น ยอดส่วนลดเงินสด และยอดเงินสุทธิของรายการในใบแจ้งหนี้ พร้อมใช้งาน จะมีการแสดงไว้ในส่วนผลรวมใบแจ้งหนี้ของฟอร์มใบแจ้งหนี้ที่สร้างขึ้น เมื่อมีการประมวลผลสำหรับนิติบุคคลที่มีการตั้งค่าคอนฟิกในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="eb74f-216">When cash discount details, such as the cash discount amount and invoice line net amount, are available, they are presented in the invoice totals section of the generated invoice form when it has been processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="eb74f-217">มีการใช้บริบทประเทศ/ภูมิภาคสำหรับสเปน</span><span class="sxs-lookup"><span data-stu-id="eb74f-217">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="eb74f-218">**มีการใช้ส่วนลดเงินสดในใบแจ้งหนี้** ถูกเปิดอยู่ในตัวเลือกใบแจ้งหนี้ (**พารามิเตอร์บัญชีแยกประเภททั่วไป** \> **ส่วนของภาษีขาย**)</span><span class="sxs-lookup"><span data-stu-id="eb74f-218">**Cash discount is applied in the invoice** is turned on in the invoice option (**General ledger parameters** \> **Sales tax section**).</span></span>

#### <a name="italy"></a><span data-ttu-id="eb74f-219">อิตาลี</span><span class="sxs-lookup"><span data-stu-id="eb74f-219">Italy</span></span>
<span data-ttu-id="eb74f-220">เครื่องหมายส่วนลดสินค้าจะถูกรวมอยู่ในรายการใบแจ้งหนี้ของใบแจ้งหนี้สร้างขึ้น เมื่อมีการประมวลผลสำหรับนิติบุคคลที่มีการจัดตั้งค่าคอนฟิกโดยใช้บริบทประเทศ/ภูมิภาคสำหรับอิตาลี</span><span class="sxs-lookup"><span data-stu-id="eb74f-220">The goods discount mark is included on the invoice lines of the generated invoice when it's being processed for a legal entity that is configured using the country/region context for Italy.</span></span>

#### <a name="finland"></a><span data-ttu-id="eb74f-221">ฟินแลนด์</span><span class="sxs-lookup"><span data-stu-id="eb74f-221">Finland</span></span>
<span data-ttu-id="eb74f-222">นอกเหนือจากแบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้น สลิปการโอนเงิน Giro ก็สามารถสร้างดังนี้:</span><span class="sxs-lookup"><span data-stu-id="eb74f-222">In addition to the generated invoice form, Giro money transfer slips can be generated as follows:</span></span>

- <span data-ttu-id="eb74f-223">สำหรับนิติบุคคลที่ใช้บริบทประเทศ/ภูมิภาคสำหรับฟินแลนด์ และที่มีบัญชีธนาคารอย่างน้อยหนึ่งรายการที่ถูกทำเครื่องหมายเป็น **บัญชี Giro** และ **บาร์โค้ดของธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="eb74f-223">For the legal entity that uses the country/region context for Finland, and that has at least one bank account that is marked as **Giro account** and **Bank bar code**.</span></span> 
- <span data-ttu-id="eb74f-224">สำหรับใบแจ้งหนี้ที่ถูกทำเครื่องหมายตามความจำเป็นสำหรับเอกสารแนบการชำระเงินที่เกี่ยวข้อง **ฟินนิช**</span><span class="sxs-lookup"><span data-stu-id="eb74f-224">For an invoice that is marked as required for the **Finnish** associated payment attachment.</span></span>

![สลิประบบโอนเงิน](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> <span data-ttu-id="eb74f-226">รูปแบบ ER ตัวอย่างได้ถูกตั้งค่าคอนฟิกในการเลือกที่จะสร้างสลิปการโอน Giro ในแผ่นงานที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="eb74f-226">The sample ER format has been configured to optionally generate the Giro money transfer slips in the separate worksheet.</span></span>

> [!NOTE]
> <span data-ttu-id="eb74f-227">อันดับแรกคุณต้องติดตั้งแบบอักษรที่ใช้ในการสร้างบาร์โค้ดบนเครื่องเฉพาะ ที่จะสามารถแสดงตัวอย่างแบบฟอร์มใบแจ้งหนี้ที่สร้างขึ้นในรูปแบบ Excel ได้</span><span class="sxs-lookup"><span data-stu-id="eb74f-227">You must first install the font that is used to generate the bar code on the local machine where the generated invoice form in Excel format will be previewed.</span></span>

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a><span data-ttu-id="eb74f-228">ใช้รูปแบบ ER ตัวอย่างเพื่อตั้งค่าคอนฟิกปลายทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="eb74f-228">Use the sample ER format to configure email destinations</span></span>
<span data-ttu-id="eb74f-229">ใช้องค์ประกอบต่อไปนี้ของรูปแบบ ER ตัวอย่าง เพื่อตั้งค่าคอนฟิกปลายทางอีเมล:</span><span class="sxs-lookup"><span data-stu-id="eb74f-229">Use the following elements of the sample ER format to configure email destinations:</span></span>

- <span data-ttu-id="eb74f-230">ที่อยู่อีเมลของผู้ติดต่อของลูกค้าสามารถเข้าถึงได้ผ่านนิพจน์ ER ต่อไปนี้: **model.InvoiceBase.Contact.ElectronicMail**</span><span class="sxs-lookup"><span data-stu-id="eb74f-230">The email address of a customer contact can be accessed through the following ER expression: **model.InvoiceBase.Contact.ElectronicMail**.</span></span>
- <span data-ttu-id="eb74f-231">ข้อความชื่อเรื่องอีเมลสามารถเข้าถึงได้ผ่านนิพจน์ ER ต่อไปนี้: **Emailing.TxtToUse.Subject**</span><span class="sxs-lookup"><span data-stu-id="eb74f-231">The email subject text can be accessed through the following ER expression: **Emailing.TxtToUse.Subject**.</span></span>
- <span data-ttu-id="eb74f-232">ข้อความเนื้อหาอีเมลสามารถเข้าถึงได้ผ่านนิพจน์ ER ต่อไปนี้: **Emailing.TxtToUse.Body**</span><span class="sxs-lookup"><span data-stu-id="eb74f-232">The email body text can be accessed through the following ER expression: **Emailing.TxtToUse.Body**.</span></span>

![การตั้งค่าปลายทาง](media/FTIbyGER-ERFileDestinationSettingEmail.png)

<span data-ttu-id="eb74f-234">มีการกำหนดข้อความเริ่มต้นของชื่อเรื่องของอีเมลและเนื้อหาในรูปแบบ ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="eb74f-234">The default text of the email's subject and body is defined in the sample ER format.</span></span> <span data-ttu-id="eb74f-235">ภาษาขึ้นอยู่กับป้ายชื่อของรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="eb74f-235">The language depends on the format's labels.</span></span> <span data-ttu-id="eb74f-236">ข้อความเริ่มต้นนี้จะใช้สำหรับอีเมล หากเท็มเพลตอีเมลขององค์กรที่กำหนดเองที่มีรหัส **ERFTITMP** ที่กำหนดไว้ล่วงหน้า ยังไม่ได้ถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="eb74f-236">This default text will be used for emails if a custom organization email template that has the predefined **ERFTITMP** ID hasn't been added.</span></span>

> [!NOTE]
> <span data-ttu-id="eb74f-237">รหัสเท็มเพลตอีเมล **ERFTITMP** ได้ถูกกำหนดในรูปแบบ ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="eb74f-237">The **ERFTITMP** email template ID has been defined in the sample ER format.</span></span> <span data-ttu-id="eb74f-238">คุณสามารถเปลี่ยนได้ตามความจำเป็นในรูปแบบ ER ใหม่ที่สร้างขึ้นจากรูปแบบตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="eb74f-238">It can be changed as required in a new ER format that is created from this sample format.</span></span>

<span data-ttu-id="eb74f-239">ถ้าเท็มเพลตอีเมลขององค์กรที่มีรหัส **ERFTITMP** ซึ่งกำหนดไว้ล่วงหน้า ได้ถูกเพิ่มสำหรับนิติบุคคลที่คุณกำลังประมวลผลใบแจ้งหนี้ให้ เท็มเพลตอีเมลสำหรับชื่อเรื่องและเนื้อหาของข้อความจะถูกใช้ในการสร้างอีเมล</span><span class="sxs-lookup"><span data-stu-id="eb74f-239">If the organization email template that has the predefined **ERFTITMP** ID has been added for the legal entity that you're processing the invoice for, the template for the email subject and body text will be used to generate the email.</span></span> 

![เท็มเพลตอีเมลขององค์กร](media/FTIbyGER-EmailTemplate.png)

![อัพโหลดเท็มเพลตอีเมล](media/FTIbyGER-EmailTemplateBody.png)

<span data-ttu-id="eb74f-242">นิพจน์ ER **Emailing.TxtToUse.Subject** ของรูปแบบ ER ตัวอย่าง ถูกตั้งค่าคอนฟิกเพื่อแทนที่เหตุการณ์ใดๆ ของตัวยึดตำแหน่ง %1 ตามรหัสใบแจ้งหนี้ที่ประมวลผล</span><span class="sxs-lookup"><span data-stu-id="eb74f-242">The **Emailing.TxtToUse.Subject** ER expression of the sample ER format is configured to replace any occurrences of the placeholder %1 by the processing invoice ID.</span></span>

<span data-ttu-id="eb74f-243">นิพจน์ **Emailing.TxtToUse.Body** ในรูปแบบตัวอย่าง ถูกตั้งค่าคอนฟิกสำหรับการทดแทนต่อไปนี้สำหรับตัวยึดตำแหน่ง:</span><span class="sxs-lookup"><span data-stu-id="eb74f-243">The **Emailing.TxtToUse.Body** expression of the sample format is configured for the following substitutions for placeholders:</span></span>

- <span data-ttu-id="eb74f-244">"%1" ถูกแทนที่ด้วยชื่อของผู้ติดต่อของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="eb74f-244">"%1" is replaced with the name of the customer's contact person.</span></span>
- <span data-ttu-id="eb74f-245">"%2" ถูกแทนที่ด้วยชื่อบริษัท</span><span class="sxs-lookup"><span data-stu-id="eb74f-245">"%2" is replaced with the company name.</span></span>
- <span data-ttu-id="eb74f-246">"%3" ถูกแทนที่ด้วยชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="eb74f-246">"%3" is replaced with the customer name.</span></span>
- <span data-ttu-id="eb74f-247">"%4" ถูกแทนที่ด้วยชื่อของผู้ติดต่อของบริษัท</span><span class="sxs-lookup"><span data-stu-id="eb74f-247">"%4" is replaced with the name of the company's contact person.</span></span>
- <span data-ttu-id="eb74f-248">"%5" ถูกแทนที่ด้วยตำแหน่งงานของผู้ติดต่อของบริษัท</span><span class="sxs-lookup"><span data-stu-id="eb74f-248">"%5" is replaced with the job title of the company's contact person.</span></span>
- <span data-ttu-id="eb74f-249">"%6" ถูกแทนที่ด้วยที่อยู่อีเมลของผู้ติดต่อของบริษัท</span><span class="sxs-lookup"><span data-stu-id="eb74f-249">"%6" is replaced with the email address of the company's contact person.</span></span>

![อีเมล](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a><span data-ttu-id="eb74f-251">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="eb74f-251">Additional resources</span></span>
[<span data-ttu-id="eb74f-252">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="eb74f-252">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
