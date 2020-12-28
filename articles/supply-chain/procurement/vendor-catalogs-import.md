---
title: นำเข้าแค็ตตาล็อกของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายกระบวนการในการนำเข้าข้อมูลแค็ตตาล็อกของผู้จัดจำหน่าย
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 7ed2c50b28fdbd1baf4caa0a8a7f2f05d6a53fd6
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438904"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="616c8-103">นำเข้าแค็ตตาล็อกของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="616c8-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="616c8-104">การนำเข้าแค็ตตาล็อกของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="616c8-104">Vendor catalogs import</span></span>

<span data-ttu-id="616c8-105">Dynamics 365 Supply Chain Management ผู้เชี่ยวชาญการซื้อสามารถสร้างและรักษาแค็ตตาล็อกสำหรับพนักงานบริษัทเพื่อใช้ เมื่อพวกเขาสั่งสินค้าและบริการสำหรับการใช้ภายใน</span><span class="sxs-lookup"><span data-stu-id="616c8-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="616c8-106">เพื่อสร้างแค็ตตาล็อกการจัดซื้อ คุณสามารถเพิ่มสินค้าและบริการที่คุณต้องการให้พร้อมใช้งานสำหรับพนักงานได้ โดยการนำเข้าข้อมูลแค็ตตาล็อกผลิตภัณฑ์หรือ โดยการเพิ่มข้อมูลแค็ตตาล็อกผลิตภัณฑ์ไปยังผลิตภัณฑ์หลักด้วยตนเอง อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="616c8-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="616c8-107">คุณสามารถอัปโหลดข้อมูลแค็ตตาล็อกที่ส่งโดยผู้จัดจำหน่ายจากไคลเอ็นต์ Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="616c8-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="616c8-108">ข้อมูลผลิตภัณฑ์ที่ผู้จัดจำหน่ายที่ส่งถึงคุณ ในรูปของไฟล์คำขอบำรุงรักษาแค็ตตาล็อก (CMR) ต้องอยู่ในรูปแบบไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="616c8-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="616c8-109">ไฟล์ CMR ควรประกอบด้วยรายละเอียดสำหรับผลิตภัณฑ์ที่ผู้จัดจำหน่ายให้กับบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="616c8-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="616c8-110">นำเข้าข้อมูลแค็ตตาล็อกของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="616c8-110">Import vendor catalog data</span></span>

<span data-ttu-id="616c8-111">หากต้องการนำเข้าข้อมูลแค็ตตาล็อกของผู้จัดจำหน่าย คุณต้องดำเนินการงานต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="616c8-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="616c8-112">ตั้งค่าโครงการในพื้นที่ทำงานการจัดการข้อมูลที่คุณได้กำหนดกฎการแม็ปข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="616c8-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="616c8-113">เลือก **การจัดการข้อมูล** แล้วจากนั้น เลือก **ตั้งค่าบทบาทสำหรับโครงการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="616c8-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="616c8-114">ตั้งค่าประเภทการจัดซื้อตามลำดับชั้น และกำหนดผู้จัดจำหน่ายให้กับประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="616c8-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="616c8-115">ถ้าคุณใช้รหัสโภคภัณฑ์ เพิ่มรหัสโภคภัณฑ์ไปยังประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="616c8-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="616c8-116">สำหรับข้อมูลเกี่ยวกับประเภทการจัดซื้อตามลำดับชั้น ดู [ตั้งค่าประเภทการจัดซื้อตามลำดับชั้น](../procurement/tasks/set-up-procurement-category-hierarchy.md)</span><span class="sxs-lookup"><span data-stu-id="616c8-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="616c8-117">ตั้งค่าคอนฟิกผู้จัดจำหน่ายสำหรับการนำเข้าแค็ตตาล็อก </span><span class="sxs-lookup"><span data-stu-id="616c8-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="616c8-118">เลือกผู้จัดจำหน่าย และจากนั้นเลือก **การจัดซื้อ** > **ตั้งค่า** > **ตั้งค่าคอนฟิกผู้จัดจำหน่ายสำหรับการนำเข้าแค็ตตาล็อก**</span><span class="sxs-lookup"><span data-stu-id="616c8-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="616c8-119">ตั้งค่าคอนฟิกลำดับงานสำหรับการนำเข้าแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="616c8-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="616c8-120">สร้างไฟล์เท็มเพลต CMR และใช้ไฟล์ร่วมกันนี้กับผู้จัดจำหน่ายของคุณ</span><span class="sxs-lookup"><span data-stu-id="616c8-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="616c8-121">เลือก **การจัดซื้อและการจัดหา** \> **ทั่วไป** \> **แค็ตตาล็อก** \> **แค็ตตาล็อกของผู้จัดจำหน่าย** เพื่อสร้างแค็ตตาล็อกของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="616c8-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="616c8-122">ไฟล์คำขอบำรุงรักษาแค็ตตาล็อก (CMR) ที่คุณได้รับจากผู้จัดจำหน่ายของคุณ จะถูกจัดกลุ่มในแค็ตตาล็อกนี้</span><span class="sxs-lookup"><span data-stu-id="616c8-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="616c8-123">อัปโหลดไฟล์ CMR</span><span class="sxs-lookup"><span data-stu-id="616c8-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="616c8-124">ตรวจทาน อนุมัติ หรือปฏิเสธผลิตภัณฑ์ในแค็ตตาล็อกของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="616c8-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="616c8-125">ผลิตภัณฑ์ถูกแม็ปโดยอัตโนมัติไปยังประเภทแผนกจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="616c8-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="616c8-126">ซึ่งผลิตภัณฑ์ที่คุณอนุมัติจะถูกรวมเข้ากับผลิตภัณฑ์หลักและนำออกใช้ไปยังนิติบุคคลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="616c8-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="616c8-127">ผลิตภัณฑ์ที่ได้รับอนุมัติเท่านั้นที่สามารถถูกเพิ่มไปยังแค็ตตาล็อกการจัดซื้อได้</span><span class="sxs-lookup"><span data-stu-id="616c8-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="616c8-128">สร้างเท็มเพลตไฟล์นำเข้าแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="616c8-128">Generate a catalog import file template</span></span>

<span data-ttu-id="616c8-129">เท็มเพลตของไฟล์นำเข้าแค็ตตาล็อกจะเป็นไฟล์ XSD ที่คุณใช้ในการสร้างไฟล์ CMR สำหรับผลิตภัณฑ์ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="616c8-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="616c8-130">คุณสามารถใช้ไฟล์ CMR เพื่อสร้างแค็ตตาล็อกใหม่แทนแค็ตตาล็อกมีอยู่หรือปรับเปลี่ยนแค็ตตาล็อกมีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="616c8-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="616c8-131">เลือก **การจัดซื้อและการจัดหา** \> **แค็ตตาล็อก** \> **แค็ตตาล็อกของผู้จัดจำหน่าย** และดับเบิลคลิกที่แค็ตตาล็อกที่คุณต้องการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="616c8-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="616c8-132">ดาวน์โหลดเท็มเพลตการนำเข้าแค็ตตาล็อกปัจจุบัน (ไฟล์ XSD)</span><span class="sxs-lookup"><span data-stu-id="616c8-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="616c8-133">ในหน้า **อัพเดตแค็ตตาล็อก** บน **บานหน้าต่างการดำเนินการ** บนแท็บ **แค็ตตาล็อก** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** คลิก **สร้างเท็มเพลตแค็ตตาล็อก** และเลือก **ประเภทการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="616c8-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="616c8-134">ด้วยตัวเลือก **ประเภทการจัดซื้อ** คุณสามารถสร้างเท็มเพลตแค็ตตาล็อกที่มีประเภทการจัดซื้อซึ่งผู้จัดจำหน่ายได้รับอนุญาตให้จัดหาผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="616c8-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="616c8-135">ในกล่องโต้ตอบ **บันทึกเป็น** ให้เลือกที่ตั้งที่คุณต้องการจัดเก็บเท็มเพลตไฟล์แค็ตตาล็อก และบันทึกไฟล์</span><span class="sxs-lookup"><span data-stu-id="616c8-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="616c8-136">สำหรับข้อมูลเพิ่มเติมและตัวอย่าง อ้างอิงถึงโพสต์บล็อกนี้: [แค็ตตาล็อกของผู้จัดจำหน่ายใน Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)</span><span class="sxs-lookup"><span data-stu-id="616c8-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>
