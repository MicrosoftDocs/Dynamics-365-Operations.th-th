---
title: การปรับรูปแบบ ER เพื่อสร้างเอกสารอิเล็กทรอนิกส์ที่กำหนดเอง
description: หัวข้อนี้จะอธิบายถึงวิธีการปรับรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่ Microsoft จัดเตรียมไว้เพื่อให้สร้างเอกสารอิเล็กทรอนิกส์แบบกำหนดเอง
author: NickSelin
ms.date: 06/22/2020
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
ms.openlocfilehash: 60b318ab03bc1bb47517a206e8b2afd9c13cf273
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891730"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="ea3dd-103">การปรับรูปแบบ ER เพื่อสร้างเอกสารอิเล็กทรอนิกส์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ea3dd-104">ขั้นตอนในหัวข้อนี้จะอธิบายวิธีการที่ผู้ใช้ในบทบาทของผู้ดูแลระบบหรือที่ปรึกษาด้านการรายงานทางอิเล็กทรอนิกส์สามารถดำเนินงานเหล่านี้ได้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="ea3dd-105">ตั้งค่าคอนฟิกพารามิเตอร์สำหรับ [กรอบงานการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="ea3dd-106">นำเข้าการตั้งค่าคอนฟิก ER ซึ่งจัดหาโดย Microsoft และใช้เพื่อสร้างไฟล์การชำระเงินในขณะที่กำลังประมวลผล [การชำระเงินให้แก่ผู้จัดจำหน่าย](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="ea3dd-107">สร้างเวอร์ชันที่กำหนดเองของการตั้งค่าคอนฟิกรูปแบบ ER มาตรฐานที่มีให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="ea3dd-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="ea3dd-108">ปรับเปลี่ยนการตั้งค่าคอนฟิกรูปแบบ ER แบบกำหนดเองเพื่อให้สร้างไฟล์การชำระเงินที่ตรงกับความต้องการของธนาคารหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="ea3dd-109">ใช้การเปลี่ยนแปลงที่เกิดขึ้นกับการตั้งค่าคอนฟิกรูปแบบ ER มาตรฐานในการตั้งค่าคอนฟิกรูปแบบ ER แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="ea3dd-110">ขั้นตอนต่อไปนี้ทั้งหมดสามารถทำได้ในบริษัท **GBSI**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="ea3dd-111">ไม่จำเป็นต้องมีการเขียนโค้ด</span><span class="sxs-lookup"><span data-stu-id="ea3dd-111">No coding is required.</span></span>

- [<span data-ttu-id="ea3dd-112">ตั้งค่าคอนฟิกกรอบงาน ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="ea3dd-113">ตั้งค่าคอนฟิกพารามิเตอร์ ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="ea3dd-114">เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="ea3dd-115">ตรวจทานรายการของผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="ea3dd-116">เพิ่มผู้ให้บริการการตั้งค่าคอนฟิก ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="ea3dd-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="ea3dd-117">เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="ea3dd-118">นำเข้าไฟล์การตั้งค่าคอนฟิกรูปแบบ ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="ea3dd-119">นำเข้าไฟล์การตั้งค่าคอนฟิก ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="ea3dd-120">ตรวจทานและนำเข้าการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="ea3dd-121">เตรียมการชําระเงินให้แก่ผู้จัดจําหน่ายสําหรับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="ea3dd-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="ea3dd-122">เพิ่มข้อมูลธนาคารสำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="ea3dd-123">ป้อนการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="ea3dd-124">ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบ ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="ea3dd-125">ตั้งค่าวิธีการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ea3dd-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="ea3dd-126">ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="ea3dd-127">การเลือกกำหนดรูปแบบ ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="ea3dd-128">สร้างรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="ea3dd-129">แก้ไขรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="ea3dd-130">ทำเครื่องหมายรูปแบบที่กำหนดเองเป็นที่สามารถรันได้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="ea3dd-131">ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบ ER ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="ea3dd-132">ตั้งค่าวิธีการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ea3dd-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="ea3dd-133">ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="ea3dd-134">นำเข้ารุ่นใหม่ของการตั้งค่าคอนฟิกรูปแบบ ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="ea3dd-135">นำเข้ารุ่นใหม่ของการตั้งค่าคอนฟิก ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="ea3dd-136">ตรวจทานการตั้งค่าคอนฟิกรูปแบบ ER ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="ea3dd-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="ea3dd-137">ใช้การเปลี่ยนแปลงในรุ่นใหม่ของรูปแบบที่นำเข้าในรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="ea3dd-138">ทำรุ่นแบบร่างของรูปแบบที่กำหนดเองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ea3dd-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="ea3dd-139">ปรับใช้รูปแบบที่กำหนดเองซ้ำให้เป็นรุ่นพื้นฐานใหม่</span><span class="sxs-lookup"><span data-stu-id="ea3dd-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="ea3dd-140">ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบ ER ที่ปรับใช้ซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="ea3dd-141">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ea3dd-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="ea3dd-142">ตั้งค่าคอนฟิกกรอบงาน ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-142">Configure the ER framework</span></span>

<span data-ttu-id="ea3dd-143">ในฐานะผู้ใช้ในบทบาทที่ปรึกษาการทำงานของการรายงานทางอิเล็กทรอนิกส์ คุณต้องตั้งค่าคอนฟิกชุดพารามิเตอร์ ER ที่ น้อยที่สุดก่อนที่คุณจะสามารถเริ่มต้นการใช้กรอบงาน ER เพื่อออกแบบรุ่นที่กำหนดเองของรูปแบบ ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="ea3dd-144">ตั้งค่าคอนฟิกพารามิเตอร์ ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-144">Configure ER parameters</span></span>

1. <span data-ttu-id="ea3dd-145">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ea3dd-146">บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="ea3dd-147">ในหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์** บนแท็บ **ทั่วไป** ตั้งค่าตัวเลือก **เปิดใช้งานโหมดการออกแบบ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="ea3dd-148">บนแท็บ **เอกสารแนบ** ให้ตั้งค่าพารามิเตอร์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="ea3dd-149">ในฟิลด์ **การตั้งค่าคอนฟิก** ให้เลือกชนิด **ไฟล์** สำหรับบริษัท **USMF**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="ea3dd-150">ในฟิลด์ **ที่เก็บงานถาวร** **ชั่วคราว** **พื้นฐาน** และ **อื่นๆ** ให้เลือกชนิด **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="ea3dd-151">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับพารามิเตอร์ ER ให้ดูที่ [ตั้งค่าคอนฟิกกรอบงาน ER](electronic-reporting-er-configure-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="ea3dd-152">เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="ea3dd-153">มีการทำเครื่องหมายการตั้งค่าคอนฟิก ER ทั้งหมดที่มีการเพิ่มเป็นเจ้าของโดยผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="ea3dd-154">ผู้ให้บริการการตั้งค่าคอนฟิก ER ที่เปิดใช้งานในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** จะใช้เพื่อวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="ea3dd-155">ดังนั้นคุณต้องเรียกใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ก่อนที่คุณจะเริ่มต้นการเพิ่มหรือแก้ไขการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="ea3dd-156">เฉพาะเจ้าของที่มีการตั้งค่าคอนฟิก ER เท่านั้นที่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="ea3dd-157">ดังนั้นก่อนที่จะแก้ไขการตั้งค่าคอนฟิก ER ต้องมีการเรียกใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="ea3dd-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="ea3dd-158">ตรวจทานรายการของผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="ea3dd-159">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ea3dd-160">บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **ผู้ให้บริการการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="ea3dd-161">บนหน้า **ตารางของผู้ให้บริการการตั้งค่าคอนฟิก** แต่ละเรกคอร์ดผู้ให้บริการจะมีชื่อและ URL ที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="ea3dd-162">ตรวจทานเนื้อหาของหน้านี้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-162">Review the contents of this page.</span></span> <span data-ttu-id="ea3dd-163">ถ้ามีเรกคอร์ดสำหรับ **Litware, inc.** (`https://www.litware.com`) อยู่แล้ว ให้ข้ามขั้นตอนถัดไป [เพิ่มผู้ให้บริการการตั้งค่าคอนฟิก ER ใหม่](#ActivateProvider)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="ea3dd-164">เพิ่มผู้ให้บริการการตั้งค่าคอนฟิก ER ใหม่</span><span class="sxs-lookup"><span data-stu-id="ea3dd-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="ea3dd-165">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ea3dd-166">บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **ผู้ให้บริการการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="ea3dd-167">ในหน้า **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="ea3dd-168">ในฟิลด์ **ชื่อ** ให้ป้อน **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="ea3dd-169">ในฟิลด์ **ที่อยู่อินเทอร์เน็ต** ให้ป้อน `https://www.litware.com`</span><span class="sxs-lookup"><span data-stu-id="ea3dd-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="ea3dd-170">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="ea3dd-171">เปิดใช้งานผู้ให้บริการการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="ea3dd-172">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ea3dd-173">ในหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือกไทล์ **Litware, inc.** แล้วเลือก **กำหนดเป็นใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="ea3dd-174">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับผู้ให้บริการการตั้งค่าคอนฟิก ER ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="ea3dd-175">นำเข้าไฟล์การตั้งค่าคอนฟิกรูปแบบ ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="ea3dd-176">นำเข้าการตั้งค่าคอนฟิก ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-176">Import the standard ER configurations</span></span>

<span data-ttu-id="ea3dd-177">เมื่อต้องการเพิ่มการตั้งค่าคอนฟิก ER มาตรฐานให้กับอินสแตนซ์ปัจจุบันของ Microsoft Dynamics 365 Finance คุณต้องนำเข้าจาก [ที่เก็บ](general-electronic-reporting.md#Repository) ER ที่ได้รับการตั้งค่าคอนฟิกสำหรับอินสแตนซ์นั้น</span><span class="sxs-lookup"><span data-stu-id="ea3dd-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="ea3dd-178">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ea3dd-179">ในหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือกไทล์ **Microsoft** แล้วเลือก **ที่เก็บ** เพื่อดูรายการของที่เก็บสำหรับผู้ให้บริการ Microsoft</span><span class="sxs-lookup"><span data-stu-id="ea3dd-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="ea3dd-180">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** เลือกที่เก็บของชนิด **ส่วนกลาง** และจากนั้นเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="ea3dd-181">ถ้าคุณได้รับพร้อมต์ให้ตรวจสอบเพื่อเชื่อมต่อกับ Regulatory Configuration Service ให้ทำตามคำแนะนำการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="ea3dd-182">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิกรูปแบบ **BACS (UK)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="ea3dd-183">บนแท็บด่วน **รุ่น** เลือกรุ่น **1.1** ของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ea3dd-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="ea3dd-184">เลือก **นำเข้า** เพื่อดาวน์โหลดเวอร์ชันที่เลือกจากที่เก็บส่วนกลางไปยังอินสแตนซ์การเงินปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="ea3dd-186">ถ้าคุณมีปัญหาในการเข้าถึง [ที่เก็บส่วนกลาง](er-download-configurations-global-repo.md) คุณสามารถ [ดาวน์โหลดการตั้งค่าคอนฟิก](download-electronic-reporting-configuration-lcs.md) จาก Microsoft Dynamics Lifecycle Services (LCS) แทน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="ea3dd-187">ตรวจทานและนำเข้าการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="ea3dd-188">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ea3dd-189">บนหน้า **การตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น** ในส่วน **การตั้งค่าคอนฟิก** เลือกไทล์ **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="ea3dd-190">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **แบบจำลองการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="ea3dd-191">โปรดสังเกตว่านอกเหนือจากรูปแบบ ER **BACS (UK)** ที่เลือก มีการนำเข้าการตั้งค่าคอนฟิก ER ที่จำเป็นอื่นๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="ea3dd-192">ตรวจสอบให้แน่ใจว่าการตั้งค่าคอนฟิก ER ต่อไปนี้จะพร้อมใช้งานในแผนภูมิการตั้งค่าคอนฟิก:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="ea3dd-193">**แบบจำลองการชำระเงิน** - การตั้งค่าคอนฟิกนี้มีส่วนประกอบ ER ของ [แบบจำลองข้อมูล](general-electronic-reporting.md#data-model-and-model-mapping-components) ซึ่งแสดงถึงโครงสร้างข้อมูลของโดเมนธุรกิจของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="ea3dd-194">**การแม็ปแบบจำลองการชำระเงิน 1611** – การตั้งค่าคอนฟิกนี้มีส่วนประกอบ ER [การแม็ปแบบจำลอง](general-electronic-reporting.md#data-model-and-model-mapping-components) ที่อธิบายวิธีการกรอกข้อมูลแบบจำลองข้อมูลด้วยข้อมูลของแอปพลิเคชันที่รันไทม์</span><span class="sxs-lookup"><span data-stu-id="ea3dd-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="ea3dd-195">**BACS (UK)** - การตั้งค่าคอนฟิกนี้มี [รูปแบบ](general-electronic-reporting.md#FormatComponentOutbound) และการแม็ปส่วนประกอบ ER</span><span class="sxs-lookup"><span data-stu-id="ea3dd-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="ea3dd-196">ส่วนประกอบรูปแบบระบุโครงร่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-196">The format component specifies the report layout.</span></span> <span data-ttu-id="ea3dd-197">ส่วนประกอบการแม็ปรูปแบบมีแหล่งข้อมูลแบบจำลองและระบุวิธีการกรอกข้อมูลโครงร่างรายงานโดยใช้แหล่งข้อมูลนี้ในขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="ea3dd-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![เพจการตั้งค่าคอนฟิก](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="ea3dd-199">เตรียมการชําระเงินให้แก่ผู้จัดจําหน่ายสําหรับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="ea3dd-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="ea3dd-200">เพิ่มข้อมูลธนาคารสำหรับบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="ea3dd-201">คุณต้องเพิ่มข้อมูลธนาคารสำหรับบัญชีผู้จัดจำหน่ายที่จะถูกอ้างอิงถึงในภายหลังในการชำระเงินที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="ea3dd-202">ไปที่ **บัญชีของเจ้าหนี้** \> **ผู้จัดจำหน่าย** \> **ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="ea3dd-203">บนหน้า **ผู้จัดจำหน่ายทั้งหมด** ให้เลือกบัญชีผู้จัดจำหน่าย **GB_SI_000001** จากนั้นในบานหน้าต่างการดำเนินการบนแท็บ **ผู้จัดจำหน่าย** ในกลุ่ม **ตั้งค่า** ให้เลือก **บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="ea3dd-204">บนหน้า **บัญชีธนาคารของผู้จัดจำหน่าย** ให้เลือก **สร้าง** แล้วป้อนข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="ea3dd-205">ในฟิลด์ **บัญชีธนาคาร** ให้ป้อน **GBP OPER**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="ea3dd-206">ในฟิลด์ **กลุ่มธนาคาร** ให้เลือก **BankGBP**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="ea3dd-207">ในฟิลด์ **หมายเลขบัญชีธนาคาร** ให้ป้อน **202015**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="ea3dd-208">ในฟิลด์ **รหัส SWIFT** ให้ป้อน <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="ea3dd-209">ในฟิลด์ **IBAN** ให้ป้อน **GB33BUKB20201555555555**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="ea3dd-210">ในฟิลด์ **หมายเลขเส้นทาง** ให้คงค่าเริ่มต้น <a id="DefineRoutingNumber"></a>**123456**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![หน้าบัญชีธนาคารของผู้จัดจำหน่าย](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="ea3dd-212">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-212">Select **Save**.</span></span>
5. <span data-ttu-id="ea3dd-213">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ea3dd-213">Close the page.</span></span>
6. <span data-ttu-id="ea3dd-214">บนหน้า **ผู้จัดจำหน่ายทั้งหมด** ให้เปิดบัญชีผู้จัดจำหน่าย **GB_SI_000001**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="ea3dd-215">บนหน้ารายละเอียดผู้จัดจำหน่าย ให้เลือก **แก้ไข** เพื่อทำให้หน้าสามารถแก้ไขได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ea3dd-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="ea3dd-216">ในแท็บด่วน **การชำระเงิน** ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **GBP OPER**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![หน้ารายละเอียดผู้จัดจำหน่าย](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="ea3dd-218">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-218">Select **Save**.</span></span>
10. <span data-ttu-id="ea3dd-219">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ea3dd-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="ea3dd-220">ป้อนการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-220">Enter a vendor payment</span></span>

<span data-ttu-id="ea3dd-221">คุณต้องสร้างการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้ [ข้อเสนอการชำระเงิน](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-221">You must enter a new vendor payment by using a [payment proposal](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).</span></span>

1. <span data-ttu-id="ea3dd-222">ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงินผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="ea3dd-223">ในหน้า **สมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่าย** ให้เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="ea3dd-224">ในฟิลด์ **ชื่อ** ให้เลือก **VendPay**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="ea3dd-225">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-225">Select **Lines**.</span></span>
5. <span data-ttu-id="ea3dd-226">เลือก **ข้อเสนอการชำระเงิน** \> **สร้างข้อเสนอการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="ea3dd-227">ในกล่องโต้ตอบ **ข้อเสนอการชำระเงินของผู้จัดจำหน่าย** ให้ตั้งค่าคอนฟิกเงื่อนไขเพื่อกรองข้อมูลเรกคอร์ดสำหรับบัญชีผู้จัดจำหน่าย **GB_SI_000001** เท่านั้น แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="ea3dd-228">เลือกบรรทัดสำหรับใบแจ้งหนี้ **00000007_Inv** แล้วเลือก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![กล่องโต้ตอบข้อเสนอการชำระเงินของผู้จัดจำหน่าย](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="ea3dd-230">ตรวจสอบว่ามีการตั้งค่าคอนฟิกการชำระเงินที่ป้อนไว้เพื่อใช้วิธีการชำระเงิน **ทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![หน้าการชำระเงินให้แก่ผู้จัดจำหน่าย](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="ea3dd-232">ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบ ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="ea3dd-233">ตั้งค่าวิธีการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ea3dd-233">Set up the electronic payment method</span></span>

<span data-ttu-id="ea3dd-234">คุณต้องตั้งค่าคอนฟิกวิธีการชำระเงินทางอิเล็กทรอนิกส์เพื่อให้ใช้การตั้งค่าคอนฟิกรูปแบบ ER ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="ea3dd-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="ea3dd-235">ไปที่ **บัญชีเจ้าหนี้** \> **การตั้งค่าการชำระเงิน** \> **วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="ea3dd-236">บนหน้า **วิธีการชำระเงิน - ผู้จัดจำหน่าย** ให้เลือกวิธีการชำระเงิน **ทางอิเล็กทรอนิกส์** ในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="ea3dd-237">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-237">Select **Edit**.</span></span>
4. <span data-ttu-id="ea3dd-238">บนแท็บด่วน **รูปแบบไฟล์** ให้ตั้งค่าตัวเลือก **รูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="ea3dd-239">ในฟิลด์ **การตั้งค่าคอนฟิกรูปแบบการส่งออก** ให้เลือกการตั้งค่าคอนฟิกรูปแบบ **BACS (UK)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![วิธีการชำระเงิน - หน้าผู้จัดจำหน่าย](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="ea3dd-241">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="ea3dd-242">ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-242">Process a vendor payment</span></span>

1. <span data-ttu-id="ea3dd-243">ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงินผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="ea3dd-244">บนหน้า **สมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่าย** เลือกสมุดรายวันการชำระเงินที่คุณเพิ่งเพิ่ม และจากนั้นเลือก **บรรทัด**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="ea3dd-245">บนหน้า **การชำระเงินให้แก่ผู้จัดจำหน่าย** เลือก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="ea3dd-246">ในกล่องโต้ตอบ **สร้างการชำระเงิน** ให้ป้อนข้อมูลดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="ea3dd-247">เลือกฟิลด์ **วิธีการชำระเงิน** เลือก **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="ea3dd-248">ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **GBSI OPER**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="ea3dd-249">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-249">Select **OK**.</span></span>
6. <span data-ttu-id="ea3dd-250">ในกล่องโต้ตอบ **พารามิเตอร์ของรายงานทางอิเล็กทรอนิกส์** ให้ตั้งค่าตัวเลือก **พิมพ์รายงานการควบคุม** เป็น **ใช่** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![หน้ากล่องโต้ตอบพารามิเตอร์รายงานทางอิเล็กทรอนิกส์](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="ea3dd-252">นอกจากไฟล์การชำระเงินแล้ว คุณยังสามารถสร้างรายงานการควบคุมได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="ea3dd-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="ea3dd-253">ดาวน์โหลดไฟล์ zip แล้วแยกไฟล์ต่อไปนี้จากไฟล์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="ea3dd-254">รายงานการควบคุมในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="ea3dd-254">The control report in Excel format</span></span>
    - <span data-ttu-id="ea3dd-255">ไฟล์การชำระเงินในรูปแบบ TXT</span><span class="sxs-lookup"><span data-stu-id="ea3dd-255">The payment file in TXT format</span></span>

        <span data-ttu-id="ea3dd-256">โปรดสังเกตว่าโดยสอดคล้องกับ [โครงสร้าง](#PositionRoutingNumber) ของรูปแบบ ER ที่ระบุ บรรทัดการชำระเงินในไฟล์ที่สร้างขึ้นจะเริ่มต้นด้วยหมายเลขเส้นทางที่ [กำหนดไว้](#DefineRoutingNumber) สำหรับบัญชีธนาคารที่มีการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="ea3dd-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![ไฟล์การชำระเงินในรูปแบบ TXT](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="ea3dd-258">การเลือกกำหนดรูปแบบ ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-258">Customize the standard ER format</span></span>

<span data-ttu-id="ea3dd-259">สำหรับตัวอย่างที่แสดงในส่วนนี้ คุณต้องการใช้การตั้งค่าคอนฟิก ER ซึ่งจัดหาโดย Microsoft เพื่อสร้างไฟล์การชำระเงินของผู้จัดจำหน่ายในรูปแบบ BACS แต่คุณต้องเพิ่มการกำหนดเองเพื่อสนับสนุนความต้องการของธนาคารที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="ea3dd-260">คุณต้องการให้สามารถอัปเกรดรูปแบบที่กำหนดเองของคุณเมื่อมีการตั้งค่าคอนฟิก ER รุ่นใหม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="ea3dd-261">อย่างไรก็ตามคุณต้องการให้สามารถอัปเกรดด้วยต้นทุนที่ต่ำที่สุด</span><span class="sxs-lookup"><span data-stu-id="ea3dd-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="ea3dd-262">ในกรณีนี้ ในฐานะตัวแทนของ Litware, Inc. คุณต้องสร้าง (ที่ได้รับมา) การตั้งค่าคอนฟิกรูปแบบ ER ใหม่โดยใช้ **BACS (UK)** Microsoft- มีการตั้งค่าคอนฟิกเป็นฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="ea3dd-263">สร้างรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-263">Create a custom format</span></span>

1. <span data-ttu-id="ea3dd-264">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ea3dd-265">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **แบบจำลองการชำระเงิน** จากนั้นเลือก **BACS (UK)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="ea3dd-266">Litware, Inc. จะใช้รุ่น 1.1 ของการตั้งค่าคอนฟิกรูปแบบ ER นี้เป็นพื้นฐานสำหรับรุ่นที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="ea3dd-267">เลือก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="ea3dd-268">คุณสามารถใช้กล่องโต้ตอบนี้ในการสร้างการตั้งค่าคอนฟิกใหม่สำหรับรูปแบบการชำระเงินที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="ea3dd-269">ในกลุ่มฟิลด์ **สร้าง** ให้เลือกตัวเลือก **ได้รับมาจากชื่อ: BACS (UK), Microsoft**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="ea3dd-270">ในฟิลด์ **ชื่อ** ให้ป้อน **BACS (UK แบบกำหนดเอง)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![สร้างกล่องโต้ตอบการตั้งค่าคอนฟิกแบบหล่นลง](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="ea3dd-272">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-272">Select **Create configuration**.</span></span>

<span data-ttu-id="ea3dd-273">รุ่น 1.1.1 ของการตั้งค่าคอนฟิกรูปแบบ ER **BACS (UK แบบกำหนดเอง)** ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ea3dd-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="ea3dd-274">รุ่นนี้มี [สถานะ](general-electronic-reporting.md#component-versioning) ของ **แบบร่าง** และสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="ea3dd-275">เนื้อหาปัจจุบันของรูปแบบ ER แบบกำหนดเองของคุณตรงกับเนื้อหาของรูปแบบที่ Microsoft ให้ไว้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![เพจการตั้งค่าคอนฟิก](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="ea3dd-277">แก้ไขรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-277">Edit a custom format</span></span>

<span data-ttu-id="ea3dd-278">คุณต้องตั้งค่าคอนฟิกรูปแบบที่กำหนดเองของคุณเพื่อให้ตรงกับความต้องการเฉพาะธนาคาร</span><span class="sxs-lookup"><span data-stu-id="ea3dd-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="ea3dd-279">ตัวอย่างเช่น ธนาคารอาจกำหนดให้ไฟล์การชำระเงินที่สร้างขึ้นรวมถึงสังคมสำหรับรหัสโทรคมนาคมทางการเงินระหว่างธนาคารทั่วโลก (SWIFT) ของธนาคารที่ได้รับการกำหนดบทบาทของตัวแทนในการชำระเงินให้แก่ผู้จัดจำหน่ายที่ประมวลผลแล้ว</span><span class="sxs-lookup"><span data-stu-id="ea3dd-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="ea3dd-280">รหัส SWIFT คือรหัสธนาคารระหว่างประเทศที่ระบุธนาคารที่ระบุทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="ea3dd-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="ea3dd-281">เรียกอีกอย่างว่ารหัสตัวระบุธนาคาร (BICs)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="ea3dd-282">รหัส SWIFT ต้องมีความยาว 11 อักขระและต้องป้อนที่จุดเริ่มต้นของบรรทัดการชำระเงินแต่ละบรรทัดในไฟล์การชำระเงินที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ea3dd-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="ea3dd-283">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ea3dd-284">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **แบบจำลองการชำระเงิน** จากนั้นเลือก **BACS (UK แบบกำหนดเอง)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="ea3dd-285">บนแท็บด่วน **รุ่น** เลือกรุ่น **1.1.1** ของการตั้งค่าคอนฟิกที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ea3dd-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="ea3dd-286">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-286">Select **Designer**.</span></span>
5. <span data-ttu-id="ea3dd-287">บนหน้า **ตัวออกแบบรูปแบบ** ให้เลือก **แสดงรายละเอียด** เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับองค์ประกอบรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="ea3dd-288">ขยายและตรวจทานองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="ea3dd-289">องค์ประกอบ **BACSReportsFolder** ของชนิด **โฟลเดอร์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="ea3dd-290">มีการใช้องค์ประกอบนี้เพื่อสร้างผลลัพธ์ในรูปแบบ ZIP</span><span class="sxs-lookup"><span data-stu-id="ea3dd-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="ea3dd-291">องค์ประกอบ **ไฟล์** ของชนิด **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="ea3dd-292">มีการใช้องค์ประกอบนี้เพื่อสร้างไฟล์การชำระเงินในรูปแบบ TXT</span><span class="sxs-lookup"><span data-stu-id="ea3dd-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="ea3dd-293">องค์ประกอบ **ธุรกรรม** ของชนิด **ลำดับ**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="ea3dd-294">มีการใช้องค์ประกอบนี้เพื่อสร้างบรรทัดการชำระเงินเดียวในไฟล์การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="ea3dd-295">องค์ประกอบ **ธุรกรรม** ของชนิด **ลำดับ**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="ea3dd-296">มีการใช้องค์ประกอบนี้เพื่อสร้างแต่ละฟิลด์ของบรรทัดการชำระเงินเดียว</span><span class="sxs-lookup"><span data-stu-id="ea3dd-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="ea3dd-297">เลือกองค์ประกอบของ **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-297">Select the **transaction** element.</span></span>

    ![องค์ประกอบธุรกรรมในโปรแกรมออกแบบการดำเนินงาน ER](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="ea3dd-299">มีการตั้งค่าคอนฟิกรายงานที่ระบุเพื่อให้ <a id="PositionRoutingNumber"></a>บรรทัดการชำระเงินทั้งหมดเริ่มต้นด้วยหมายเลขเส้นทางธนาคาร</span><span class="sxs-lookup"><span data-stu-id="ea3dd-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="ea3dd-300">องค์ประกอบรูปแบบ **vendBankRouteNum** ใช้สำหรับวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="ea3dd-301">เลือก **เพิ่ม** แล้วเลือกชนิดของ **ข้อความ\\สตริง** ขององค์ประกอบรูปแบบที่คุณกำลังเพิ่ม:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="ea3dd-302">ในฟิลด์ **ชื่อ** ให้ป้อน **vendBankSWIFT**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="ea3dd-303">ในฟิลด์ **ความยาวต่ำสุด** ให้ป้อน **11**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="ea3dd-304">ในฟิลด์ **ความยาวสูงสุด** ให้ป้อน **11**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="ea3dd-305">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ea3dd-306">จะมีการใช้องค์ประกอบ **vendBankSWIFT** เพื่อป้อนรหัส SWIFT ของธนาคารผู้จัดจำหน่ายในไฟล์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ea3dd-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="ea3dd-307">ในแผนภูมิโครงสร้างรูปแบบ ให้เลือก **vendBankSWIFT**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="ea3dd-308">เลือก **ย้ายขึ้น** เพื่อย้ายองค์ประกอบรูปแบบที่เลือกขึ้นหนึ่งระดับ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="ea3dd-309">ทำซ้ำขั้นตอนนี้จนกว่าจะมีองค์ประกอบ **vendBankSWIFT** เป็น <a id="PositionSWIFTCode"></a>องค์ประกอบแรกภายใต้องค์ประกอบ **ธุรกรรม** หลัก</span><span class="sxs-lookup"><span data-stu-id="ea3dd-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT เป็นองค์ประกอบแรกภายใต้ธุรกรรมในตัวออกแบบการดำเนินงาน ER](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="ea3dd-311">ในขณะที่ **vendBankSWIFT** ยังคงถูกเลือกในแผนภูมิโครงสร้างรูปแบบ ให้เลือกแท็บ **การแม็ป** แล้วขยายแหล่งข้อมูล **แบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="ea3dd-312">ขยาย **model.Payment** \> **model.Payment.CreditorAgent** และเลือกฟิลด์แหล่งข้อมูล **model.Payment.CreditorAgent.BICFI**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="ea3dd-313">ฟิลด์แหล่งข้อมูลนี้แสดงถึงรหัส SWIFT ของธนาคารผู้จัดจำหน่ายที่ได้รับการกำหนดบทบาทของตัวแทนในการชำระเงินให้แก่ผู้จัดจำหน่ายที่ประมวลผล</span><span class="sxs-lookup"><span data-stu-id="ea3dd-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="ea3dd-314">เลือก **ผูก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-314">Select **Bind**.</span></span> <span data-ttu-id="ea3dd-315">ขณะนี้มีการผูกองค์ประกอบรูปแบบ **vendBankSWIFT** กับฟิลด์แหล่งที่มาของข้อมูล **model.Payment.CreditorAgent.BICFI** เพื่อให้รหัส SWIFT จะถูกป้อนลงในไฟล์การชำระเงินที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ea3dd-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![องค์ประกอบรูปแบบ vendBankSWIFT ที่ผูกกับฟิลด์แหล่งข้อมูล model.Payment.CreditorAgent.BICFI ในตัวออกแบบการดำเนินงาน ER](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="ea3dd-317">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-317">Select **Save**.</span></span>
15. <span data-ttu-id="ea3dd-318">ปิดหน้าโปรแกรมออกแบบ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="ea3dd-319">ทำเครื่องหมายรูปแบบที่กำหนดเองเป็นที่สามารถรันได้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="ea3dd-320">หลังจากที่มีการสร้างรูปแบบที่กำหนดเองของคุณรุ่นแรกแล้วและมีสถานะเป็น **แบบร่าง** คุณสามารถรันงานนี้เพื่อวัตถุประสงค์ในการทดสอบได้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="ea3dd-321">เมื่อต้องการรันรายงาน คุณต้องประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้วิธีการชำระเงินที่อ้างอิงถึงรูปแบบ ER แบบกำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="ea3dd-322">โดยค่าเริ่มต้น เมื่อคุณเรียกใช้รูปแบบ ER จากแอปพลิเคชัน จะมีเฉพาะรุ่นที่มีสถานะเป็น **เสร็จสมบูรณ์** หรือ **ใช้ร่วมกัน** เท่านั้นที่ [ได้รับการพิจารณา](general-electronic-reporting.md#component-versioning)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="ea3dd-323">ลักษณะการทำงานนี้ช่วยป้องกันไม่ให้มีการใช้รูปแบบ ER ที่มีการออกแบบที่ยังไม่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="ea3dd-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="ea3dd-324">อย่างไรก็ตามสำหรับการรันการทดสอบของคุณ คุณสามารถบังคับให้แอปพลิเคชันใช้เวอร์ชันของรูปแบบ ER ของคุณที่มีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="ea3dd-325">ด้วยวิธีนี้คุณสามารถปรับรุ่นของรูปแบบปัจจุบันถ้าจำเป็นต้องมีการปรับเปลี่ยนใดๆ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="ea3dd-326">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การใช้งาน](electronic-reporting-destinations.md#applicability)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="ea3dd-327">หากต้องการใช้รุ่นแบบร่างของรูปแบบ ER คุณต้องทำเครื่องหมายรูปแบบ ER ให้ชัดเจน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="ea3dd-328">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ea3dd-329">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="ea3dd-330">ในกล่องโต้ตอบ **พารามิเตอร์ผู้ใช้** ให้ตั้งค่าตัวเลือก **เรียกใช้การตั้งค่า** เป็น **ใช่** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="ea3dd-331">ให้เลือก **แก้ไข้** เพื่อทำให้หน้าปัจจุบันพร้อมสำหรับการแก้ไข หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ea3dd-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="ea3dd-332">ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือก **BACS (UK แบบกำหนดเอง)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="ea3dd-333">ตั้งค่าตัวเลือก **เรียกใช้แบบร่าง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![รันตัวเลือกแบบร่างบนหน้าการตั้งค่าคอนฟิก](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="ea3dd-335">ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบ ER ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="ea3dd-336">ตั้งค่าวิธีการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ea3dd-336">Set up the electronic payment method</span></span>

<span data-ttu-id="ea3dd-337">คุณต้องตั้งค่าคอนฟิกวิธีการชำระเงินทางอิเล็กทรอนิกส์เพื่อให้รูปแบบ ER ที่กำหนดเองของคุณใช้ในการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="ea3dd-338">ไปที่ **บัญชีเจ้าหนี้** \> **การตั้งค่าการชำระเงิน** \> **วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="ea3dd-339">บนหน้า **วิธีการชำระเงิน - ผู้จัดจำหน่าย** ให้เลือกวิธีการชำระเงิน **ทางอิเล็กทรอนิกส์** ในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="ea3dd-340">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-340">Select **Edit**.</span></span>
4. <span data-ttu-id="ea3dd-341">บนแท็บด่วน **รูปแบบไฟล์** ให้ตั้งค่าตัวเลือก **รูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="ea3dd-342">ในฟิลด์ **การตั้งค่าคอนฟิกรูปแบบการส่งออก** ให้เลือกการตั้งค่าคอนฟิกรูปแบบ **BACS (UK แบบกำหนดเอง)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![วิธีการชำระเงิน - หน้าผู้จัดจำหน่าย](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="ea3dd-344">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="ea3dd-345">ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-345">Process a vendor payment</span></span>

1. <span data-ttu-id="ea3dd-346">ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงินผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="ea3dd-347">บนหน้า **สมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่าย** เลือกสมุดรายวันการชำระเงินที่คุณเพิ่งสร้าง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="ea3dd-348">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-348">Select **Lines**.</span></span>
4. <span data-ttu-id="ea3dd-349">บนหน้า **การชำระเงินให้แก่ผู้จัดจำหน่าย** ด้านบนกริด ให้เลือก **สถานะการชำระเงิน** \> **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="ea3dd-350">เลือก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="ea3dd-351">ในกล่องโต้ตอบ **สร้างการชำระเงิน** ให้ป้อนข้อมูลดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="ea3dd-352">เลือกฟิลด์ **วิธีการชำระเงิน** เลือก **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="ea3dd-353">ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **GBSI OPER**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="ea3dd-354">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-354">Select **OK**.</span></span>
8. <span data-ttu-id="ea3dd-355">ในกล่องโต้ตอบ **พารามิเตอร์ของรายงานทางอิเล็กทรอนิกส์** ให้ตั้งค่าตัวเลือก **พิมพ์รายงานการควบคุม** เป็น **ใช่** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ea3dd-356">นอกจากไฟล์การชำระเงินแล้ว คุณสามารถสร้างรายงานการควบคุมได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ea3dd-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="ea3dd-357">ดาวน์โหลดไฟล์ zip แล้วแยกไฟล์ต่อไปนี้จากไฟล์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="ea3dd-358">รายงานการควบคุมในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="ea3dd-358">The control report in Excel format</span></span>
    - <span data-ttu-id="ea3dd-359">ไฟล์การชำระเงินในรูปแบบ TXT</span><span class="sxs-lookup"><span data-stu-id="ea3dd-359">The payment file in TXT format</span></span>

        <span data-ttu-id="ea3dd-360">โปรดสังเกตว่าโดยสอดคล้องกับโครงสร้างของรูปแบบ ER แบบกำหนดเอง บรรทัดการชำระเงินในไฟล์ที่สร้างขึ้นในขณะนี้จะ [เริ่มต้น](#PositionSWIFTCode) ด้วยรหัส SWIFT ที่ [ป้อนไว้](#DefineSWIFTCode) สำหรับบัญชีธนาคารของผู้จัดจำหน่ายที่มีการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![ไฟล์การชำระเงินในรูปแบบ TXT](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="ea3dd-362">นำเข้ารุ่นใหม่ของการตั้งค่าคอนฟิกรูปแบบ ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="ea3dd-363">สำหรับตัวอย่างที่แสดงในส่วนนี้ คุณจะได้รับการแจ้งเตือนเกี่ยวกับบทความฐานข้อมูลองค์ความรู้ [KB 3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="ea3dd-364">การแจ้งเตือนนี้จะแจ้งให้คุณทราบเกี่ยวกับรูปแบบ ER ของ **BACS (UK)** รุ่นใหม่ที่เผยแพร่โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="ea3dd-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="ea3dd-365">นอกจากรายงานการควบคุม เวอร์ชันใหม่นี้ยังช่วยให้ผู้ใช้สามารถสร้างรายงานใบแจ้งการชำระเงินและรายงานบันทึกการเข้าร่วมในขณะที่มีการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="ea3dd-366">คุณต้องการเริ่มต้นที่จะใช้ฟังก์ชันดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="ea3dd-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="ea3dd-367">นำเข้ารุ่นใหม่ของการตั้งค่าคอนฟิก ER มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="ea3dd-368">เมื่อต้องการเพิ่มการตั้งค่าคอนฟิก ER มาตรฐานเวอร์ชันใหม่ให้กับอินสแตนซ์การเงินปัจจุบันของ Microsoft คุณต้องนำเข้าจาก [ที่เก็บ](general-electronic-reporting.md#Repository) ER ที่คุณได้ตั้งค่าคอนฟิกไว้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="ea3dd-369">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ea3dd-370">ในหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือกไทล์ **Microsoft** แล้วเลือก **ที่เก็บ** เพื่อดูรายการของที่เก็บสำหรับผู้ให้บริการ Microsoft</span><span class="sxs-lookup"><span data-stu-id="ea3dd-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="ea3dd-371">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** เลือกที่เก็บของชนิด **ส่วนกลาง** และจากนั้นเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="ea3dd-372">ถ้าคุณได้รับพร้อมต์ให้ตรวจสอบเพื่อเชื่อมต่อกับ Regulatory Configuration Service ให้ทำตามคำแนะนำการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="ea3dd-373">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิกรูปแบบ **BACS (UK)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="ea3dd-374">บนแท็บด่วน **รุ่น** เลือกรุ่น **3.3** ของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ea3dd-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="ea3dd-375">เลือก **นำเข้า** เพื่อดาวน์โหลดเวอร์ชันที่เลือกจากที่เก็บส่วนกลางไปยังอินสแตนซ์การเงินปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="ea3dd-377">ถ้าคุณมีปัญหาในการเข้าถึง [ที่เก็บส่วนกลาง](er-download-configurations-global-repo.md) คุณสามารถ [ดาวน์โหลดการตั้งค่าคอนฟิก](download-electronic-reporting-configuration-lcs.md) จาก LCS แทน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="ea3dd-378">ตรวจทานการตั้งค่าคอนฟิกรูปแบบ ER ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="ea3dd-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="ea3dd-379">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ea3dd-380">บนหน้า **การตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น** ในส่วน **การตั้งค่าคอนฟิก** เลือกไทล์ **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="ea3dd-381">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **แบบจำลองการชำระเงิน** จากนั้นเลือก **BACS (UK)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="ea3dd-382">บน FastTab **รุ่น** เลือกรุ่น **3.3**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="ea3dd-383">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-383">Select **Designer**.</span></span>
6. <span data-ttu-id="ea3dd-384">บนหน้า **ตัวออกแบบรูปแบบ** ให้ขยายองค์ประกอบรูปแบบ **BACSReportsFolder**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="ea3dd-385">โปรดสังเกตว่ารุ่น 3.3 ประกอบด้วยองค์ประกอบรูปแบบ **PaymentAdviceReport** ที่ใช้ในการสร้างรายงานใบแจ้งการชำระเงินเมื่อมีการประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea3dd-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![องค์ประกอบรูปแบบ PaymentAdviceReport ในโปรแกรมออกแบบการดำเนินงาน ER](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="ea3dd-387">ปิดหน้าโปรแกรมออกแบบ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="ea3dd-388">ใช้การเปลี่ยนแปลงในรุ่นใหม่ของรูปแบบที่นำเข้าในรูปแบบที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="ea3dd-389">ทำรุ่นแบบร่างของรูปแบบที่กำหนดเองให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ea3dd-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="ea3dd-390">ถ้าคุณต้องการเก็บสถานะปัจจุบันของรูปแบบที่กำหนดเองของคุณ ให้ดำเนินการรุ่นแบบร่าง 1.1.1 ให้เสร็จสมบูรณ์โดยการเปลี่ยนสถานะของ **แบบร่าง** เป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="ea3dd-391">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ea3dd-392">บนหน้า **การตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น** ในส่วน **การตั้งค่าคอนฟิก** เลือกไทล์ **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="ea3dd-393">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **แบบจำลองการชำระเงิน** ขยาย **BACS (UK)** จากนั้นเลือก **BACS (UK แบบกำหนดเอง)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="ea3dd-394">บนแท็บด่วน **รุ่น** เลือก **เปลี่ยนสถานะ** \> **เสร็จสมบูรณ์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="ea3dd-395">สถานะของรุ่น 1.1.1 มีการเปลี่ยนแปลงจาก **แบบร่าง** เป็น **เสร็จสมบูรณ์** แล้วและรุ่นจะกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="ea3dd-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="ea3dd-396">รุ่นที่แก้ไขใหม่ได้ 1.1.2 ถูกเพิ่มและมีสถานะเป็น **แบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="ea3dd-397">คุณสามารถใช้รุ่นนี้เพื่อทำการเปลี่ยนแปลงเพิ่มเติมในรูปแบบ ER แบบกำหนดเองของคุณได้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="ea3dd-398">ปรับใช้รูปแบบที่กำหนดเองให้เป็นรุ่นพื้นฐานใหม่ซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="ea3dd-399">เมื่อต้องการเริ่มต้นที่จะใช้ฟังก์ชันใหม่ของรุ่น 3.3 ของรูปแบบ **BACS (UK)** ในการกำหนดเองของคุณ คุณต้องเปลี่ยนรุ่นการตั้งค่าคอนฟิกพื้นฐานสำหรับการตั้งค่าคอนฟิกที่กำหนดเอง **BACS (UK แบบกำหนดเอง)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="ea3dd-400">กระบวนการนี้เรียกว่า [การปรับใช้ซ้ำ](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="ea3dd-401">แทนที่รุ่น 1.1 ของ **BACS (UK)** ให้ใช้รุ่น 3.3</span><span class="sxs-lookup"><span data-stu-id="ea3dd-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="ea3dd-402">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ea3dd-403">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **แบบจำลองการชำระเงิน** จากนั้นเลือก **BACS (UK แบบกำหนดเอง)**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="ea3dd-404">บนแท็บด่วน **รุ่น** ให้เลือกรุ่น **1.1.2** แล้วเลือก **ปรับใช้ซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="ea3dd-405">ในกล่องโต้ตอบ **ปรับใช้ซ้ำ** ในฟิลด์ **เวอร์ชันเป้าหมาย** ให้เลือกรุ่น **3.3** ของการตั้งค่าคอนฟิกพื้นฐานที่จะใช้เป็นฐานใหม่และใช้เพื่ออัปเดตการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="ea3dd-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![กล่องโต้ตอบการปรับใช้ซ้ำ](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="ea3dd-407">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-407">Select **OK**.</span></span>
6. <span data-ttu-id="ea3dd-408">โปรดสังเกตว่ามีการเปลี่ยนแปลงหมายเลขของรุ่นแบบร่างจาก **1.1.2** เป็น **3.3.2** เพื่อให้สะท้อนถึงการเปลี่ยนแปลงในรุ่นพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="ea3dd-409">เมื่อมีการการผสานรุ่นที่กำหนดเองและรุ่นฐานใหม่ อาจพบข้อขัดข้องบางอย่างเนื่องจากการเปลี่ยนแปลงรูปแบบที่ไม่สามารถผสานได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![การตั้งค่าคอนฟิกที่ปรับใช้ซ้ำที่มีความขัดแย้งในหน้าการตั้งค่าคอนฟิก](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="ea3dd-411">ถ้ามีการตรวจพบความขัดแย้ง ต้องแก้ไขด้วยตนเองในตัวออกแบบรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="ea3dd-412">บน FastTab **รุ่น** เลือกรุ่น **3.3.2**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="ea3dd-413">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-413">Select **Designer**.</span></span>
9. <span data-ttu-id="ea3dd-414">บนหน้า **ตัวออกแบบรูปแบบ** บนแท็บด่วน **รายละเอียด** ให้เลือกเรกคอร์ดความขัดแย้งที่ปรับใช้ซ้ำ แล้วเลือก **ใช้ค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![ปรับใช้เรกคอร์ดความขัดแย้งซ้ำในโปรแกรมออกแบบการดำเนินงาน ER](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="ea3dd-416">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-416">Select **Save**.</span></span>

    <span data-ttu-id="ea3dd-417">เรกคอร์ดความขัดแย้งที่ปรับใช้ซ้ำไม่ควรปรากฏบนแท็บด่วน **รายละเอียด** อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="ea3dd-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![แก้ไขความขัดแย้งในโปรแกรมออกแบบการดำเนินงาน ER แล้ว](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="ea3dd-419">คุณได้แก้ไขความขัดแย้งโดยการยืนยันรุ่น 3 ของแบบจำลองพื้นฐานต้องใช้ในรูปแบบ ER นี้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="ea3dd-420">ขยาย **BACSReportsFolder** \> **ไฟล์** \> **ธุรกรรม** \> **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="ea3dd-421">บนแท็บ **การแม็ป** ให้สังเกตว่ารุ่น 3.3.2 ของรูปแบบ ER แบบกำหนดเองของคุณมีทั้งการกำหนดเองของคุณ (องค์ประกอบของรูปแบบ **vendBankSWIFT** และการผูกข้อมูล) และฟังก์ชันการทำงานใหม่ของรุ่น 3.3 ของรูปแบบ ER พื้นฐานที่ให้ไว้โดย Microsoft (องค์ประกอบรูปแบบ **PaymentAdviceReport** พร้อมกับองค์ประกอบmujซ้อนกันและการรวมที่ตั้งค่าคอนฟิก)</span><span class="sxs-lookup"><span data-stu-id="ea3dd-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="ea3dd-422">ในการคลิกเมาส์เพียงไม่กี่ครั้ง คุณจะปรับใช้การปรับเปลี่ยนรุ่นพื้นฐานใหม่โดยการผสานเข้ากับการเลือกกำหนดของคุณ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![รูปแบบที่ผสานในตัวออกแบบการดำเนินงาน ER](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="ea3dd-424">ปิดหน้าโปรแกรมออกแบบ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="ea3dd-425">การดำเนินการปรับใช้ซ้ำย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-425">The rebase action is reversible.</span></span> <span data-ttu-id="ea3dd-426">ถ้าต้องการยกเลิกการปรับใช้ซ้ำนี้ ให้เลือกรุ่น **1.1.1** ของรูปแบบ **BACS (UK แบบกำหนดเอง)** ในแท็บด่วน **รุ่น** แล้วเลือก **เรียกใช้รุ่นนี้**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="ea3dd-427">จากนั้นรุ่น 3.3.2 จะกำหนดหมายเลข 1.1.2 และเนื้อหาของรุ่นแบบร่าง 1.1.2 จะจับคู่เนื้อหาของรุ่น 1.1.1</span><span class="sxs-lookup"><span data-stu-id="ea3dd-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="ea3dd-428">ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบ ER ที่ปรับใช้ซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ea3dd-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="ea3dd-429">ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงินผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="ea3dd-430">บนหน้า **สมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่าย** เลือกสมุดรายวันการชำระเงินที่คุณเพิ่งสร้าง</span><span class="sxs-lookup"><span data-stu-id="ea3dd-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="ea3dd-431">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-431">Select **Lines**.</span></span>
4. <span data-ttu-id="ea3dd-432">บนหน้า **การชำระเงินให้แก่ผู้จัดจำหน่าย** ด้านบนกริด ให้เลือก **สถานะการชำระเงิน** \> **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="ea3dd-433">เลือก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="ea3dd-434">ในกล่องโต้ตอบ **สร้างการชำระเงิน** ให้ป้อนข้อมูลดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="ea3dd-435">เลือกฟิลด์ **วิธีการชำระเงิน** เลือก **อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="ea3dd-436">ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **GBSI OPER**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="ea3dd-437">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-437">Select **OK**.</span></span>
8. <span data-ttu-id="ea3dd-438">ในกล่องโต้ตอบ **พารามิเตอร์รายงานทางอิเล็กทรอนิกส์** ให้ป้อนข้อมูลดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="ea3dd-439">ตั้งค่าตัวเลือก **พิมพ์รายงานควบคุม** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="ea3dd-440">ตั้งค่าตัวเลือก **พิมพ์ใบแจ้งการชำระเงิน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![กล่องโต้ตอบพารามิเตอร์รายงานทางอิเล็กทรอนิกส์](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="ea3dd-442">นอกจากไฟล์การชำระเงินแล้ว คุณยังสามารถสร้างรายงานการควบคุมและรายงานใบแจ้งการชำระเงินได้แล้วในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="ea3dd-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="ea3dd-443">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ea3dd-443">Select **OK**.</span></span>
10. <span data-ttu-id="ea3dd-444">ดาวน์โหลดไฟล์ zip แล้วแยกไฟล์ต่อไปนี้จากไฟล์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ea3dd-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="ea3dd-445">รายงานการควบคุมในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="ea3dd-445">The control report in Excel format</span></span>
    - <span data-ttu-id="ea3dd-446">รายงานใบแจ้งการชำระเงินในรูปแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="ea3dd-446">The payment advice report in Excel format</span></span>

        ![รายงานใบแจ้งการชำระเงินในรูปแบบ Excel](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="ea3dd-448">ไฟล์การชำระเงินในรูปแบบ TXT</span><span class="sxs-lookup"><span data-stu-id="ea3dd-448">The payment file in TXT format</span></span>

        <span data-ttu-id="ea3dd-449">โปรดสังเกตว่าบรรทัดการชำระเงินในไฟล์ที่สร้างขึ้นในขณะนี้จะเริ่มต้นด้วยรหัส SWIFT ที่ป้อนไว้สำหรับบัญชีธนาคารของผู้จัดจำหน่ายที่มีการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ea3dd-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![ไฟล์การชำระเงินในรูปแบบ TXT](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="ea3dd-451">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ea3dd-451">Additional resources</span></span>

- [<span data-ttu-id="ea3dd-452">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ea3dd-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="ea3dd-453">ดาวน์โหลดการตั้งค่าคอนฟิก ER จาก Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ea3dd-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="ea3dd-454">ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="ea3dd-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]