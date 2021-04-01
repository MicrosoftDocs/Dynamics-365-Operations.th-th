---
title: ประเทศของผู้ผลิต
description: องค์กรจำนวนมากออกใบรับรองให้กับผู้จัดจำหน่ายของพวกเขา เพื่อให้มั่นใจว่าผลิตภัณฑ์ตรงตามมาตรฐานการรับรองเฉพาะ ใบรับรองเหล่านี้มักจะขึ้นอยู่กับประเทศต้นทาง หัวข้อนี้จะให้ข้อมูลเกี่ยวกับคุณลักษณะประเทศต้นทาง ซึ่งช่วยให้คุณสามารถเชื่อมโยงผลิตภัณฑ์ไปยังประเทศต้นทางและติดตามการรับรองผลิตภัณฑ์
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: bb35770f32c21a685b21a41dc7c369ee01fe3891
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243308"
---
# <a name="country-of-origin"></a><span data-ttu-id="a5b35-105">ประเทศของผู้ผลิต</span><span class="sxs-lookup"><span data-stu-id="a5b35-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a5b35-106">องค์กรจำนวนมากออกใบรับรองให้กับผู้จัดจำหน่ายของพวกเขา เพื่อให้มั่นใจว่าผลิตภัณฑ์ตรงตามมาตรฐานการรับรองเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="a5b35-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="a5b35-107">ใบรับรองเหล่านี้มักจะขึ้นอยู่กับประเทศต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a5b35-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="a5b35-108">คุณลักษณะประเทศต้นทางช่วยให้คุณสามารถเชื่อมโยงผลิตภัณฑ์ไปยังประเทศต้นทางและติดตามการรับรองผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a5b35-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="a5b35-109">เปิดคุณลักษณะประเทศต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a5b35-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="a5b35-110">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="a5b35-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a5b35-111">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a5b35-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="a5b35-112">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a5b35-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a5b35-113">**โมดูล:** *การจัดการข้อมูลผลิตภัณฑ์*</span><span class="sxs-lookup"><span data-stu-id="a5b35-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="a5b35-114">**ชื่อคุณลักษณะ:** *คุณลักษณะการจัดการประเทศต้นทาง*</span><span class="sxs-lookup"><span data-stu-id="a5b35-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="a5b35-115">ตั้งค่าคอนฟิกประเทศต้นทางและประเทศปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a5b35-115">Configure source and destination countries</span></span>

<span data-ttu-id="a5b35-116">ก่อนที่คุณจะออกใบรับรองสำหรับผลิตภัณฑ์ คุณต้องเชื่อมโยงผลิตภัณฑ์ไปยังประเทศปลายทางและประเทศต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a5b35-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="a5b35-117">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> การตั้งค่า \> การปฏิบัติตามกฎระเบียบด้านผลิตภัณฑ์ \> ประเทศต้นทาง \> กฎของประเทศต้นทาง**</span><span class="sxs-lookup"><span data-stu-id="a5b35-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="a5b35-118">เลือกการตั้งค่าประเทศที่มีอยู่เพื่อแก้ไข หรือเลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อสร้างการตั้งค่าประเทศใหม่</span><span class="sxs-lookup"><span data-stu-id="a5b35-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="a5b35-119">ตั้งค่าค่าต่อไปนี้สำหรับประเทศที่เลือกหรือประเทศใหม่</span><span class="sxs-lookup"><span data-stu-id="a5b35-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="a5b35-120">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="a5b35-120">Field</span></span> | <span data-ttu-id="a5b35-121">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a5b35-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="a5b35-122">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="a5b35-122">Item number</span></span> | <span data-ttu-id="a5b35-123">เลือกหมายเลขสินค้าของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a5b35-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="a5b35-124">ประเทศปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a5b35-124">Destination country</span></span> | <span data-ttu-id="a5b35-125">เลือกประเทศที่คุณกำลังส่งผลิตภัณฑ์ไป</span><span class="sxs-lookup"><span data-stu-id="a5b35-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="a5b35-126">ประเทศต้นทาง</span><span class="sxs-lookup"><span data-stu-id="a5b35-126">Origin country</span></span> | <span data-ttu-id="a5b35-127">เลือกประเทศที่คุณกำลังจัดส่งผลิตภัณฑ์มา</span><span class="sxs-lookup"><span data-stu-id="a5b35-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="a5b35-128">วัตถุประสงค์ของการตั้งค่านี้คือเพื่อช่วยคุณในการสร้างรายงานสูตรการผลิต (BOM) ที่คุณสามารถรวมประเทศต้นทางสำหรับแต่ละส่วนที่มีการระบุประเทศต้นทางและประเทศปลายทางให้</span><span class="sxs-lookup"><span data-stu-id="a5b35-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="a5b35-129">รายงานนี้จะช่วยให้คุณได้รับภาพรวมของสถานที่ที่วัตถุดิบของคุณมาและสถานที่ที่จะไป</span><span class="sxs-lookup"><span data-stu-id="a5b35-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="a5b35-130">ติดตามใบรับรองของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a5b35-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="a5b35-131">คุณสามารถใช้หน้า **ใบรับรองของผู้จัดจำหน่ายของประเทศต้นทาง** เพื่อติดตามใบรับรองที่คุณออกให้กับผู้จัดจำหน่ายได้</span><span class="sxs-lookup"><span data-stu-id="a5b35-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="a5b35-132">คุณต้องตัดสินใจว่าเอกสารใบรับรองใดที่คุณกำลังออกและคุณจะรายงานใบรับรองเหล่านั้นให้กับลูกค้าอย่างไร</span><span class="sxs-lookup"><span data-stu-id="a5b35-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="a5b35-133">คุณลักษณะนี้จะช่วยให้คุณติดตามใบรับรองของคุณได้</span><span class="sxs-lookup"><span data-stu-id="a5b35-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="a5b35-134">นอกจากนี้ คุณยังสามารถเลือกได้ว่าจะให้หมายเลขใบรับรองที่เกี่ยวข้องปรากฏบนใบแจ้งหนี้ บันทึกการจัดส่ง และ/หรือ การยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="a5b35-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="a5b35-135">ถ้าต้องการตั้งค่าข้อมูลใบรับรองของคุณ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a5b35-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="a5b35-136">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> การตั้งค่า \> การปฏิบัติตามกฎระเบียบด้านผลิตภัณฑ์ \> ประเทศต้นทาง \> ใบรับรองของผู้จัดจำหน่ายของประเทศต้นทาง**</span><span class="sxs-lookup"><span data-stu-id="a5b35-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="a5b35-137">เลือกการตั้งค่าใบรับรองที่มีอยู่เพื่อแก้ไข หรือเลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อสร้างการตั้งค่าใบรับรองใหม่</span><span class="sxs-lookup"><span data-stu-id="a5b35-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="a5b35-138">กำหนดการตั้งค่าต่อไปนี้สำหรับใบรับรองที่เลือกหรือใบรับรองใหม่</span><span class="sxs-lookup"><span data-stu-id="a5b35-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="a5b35-139">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="a5b35-139">Field</span></span> | <span data-ttu-id="a5b35-140">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a5b35-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="a5b35-141">บัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a5b35-141">Vendor account</span></span> | <span data-ttu-id="a5b35-142">เลือกผู้จัดจำหน่ายที่คุณออกใบรับรองให้</span><span class="sxs-lookup"><span data-stu-id="a5b35-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="a5b35-143">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="a5b35-143">Item number</span></span> | <span data-ttu-id="a5b35-144">เลือกสินค้าที่คุณออกใบรับรองให้</span><span class="sxs-lookup"><span data-stu-id="a5b35-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="a5b35-145">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="a5b35-145">Country/region</span></span> | <span data-ttu-id="a5b35-146">ประเทศหรือภูมิภาคปลายทางที่คุณต้องใช้ใบรับรองนี้</span><span class="sxs-lookup"><span data-stu-id="a5b35-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="a5b35-147">หมายเลขใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="a5b35-147">Certificate number</span></span> | <span data-ttu-id="a5b35-148">ป้อนหมายเลขการระบุรหัสประจำตัวของใบรับรองที่คุณออก</span><span class="sxs-lookup"><span data-stu-id="a5b35-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="a5b35-149">มีผล</span><span class="sxs-lookup"><span data-stu-id="a5b35-149">Effective</span></span> | <span data-ttu-id="a5b35-150">เลือกวันที่เริ่มต้นที่ใบรับรองปัจจุบันมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="a5b35-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="a5b35-151">การหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="a5b35-151">Expiration</span></span> | <span data-ttu-id="a5b35-152">เลือกวันที่สุดท้ายที่ใบรับรองปัจจุบันมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="a5b35-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="a5b35-153">พิมพ์บนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a5b35-153">Print on invoice</span></span> | <span data-ttu-id="a5b35-154">เลือกกล่องกาเครื่องหมายนี้เพื่อพิมพ์หมายเลขใบรับรองในใบแจ้งหนี้ที่ระบุให้กับประเทศที่ระบุในระหว่างช่วงวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a5b35-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="a5b35-155">พิมพ์ในบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="a5b35-155">Print on packing slip</span></span> | <span data-ttu-id="a5b35-156">เลือกกล่องกาเครื่องหมายนี้เพื่อพิมพ์หมายเลขใบรับรองในบันทึกการจัดส่งที่ระบุให้กับประเทศที่ระบุในระหว่างช่วงวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a5b35-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="a5b35-157">พิมพ์ในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="a5b35-157">Print on sales order</span></span> | <span data-ttu-id="a5b35-158">เลือกกล่องกาเครื่องหมายนี้เพื่อพิมพ์หมายเลขใบรับรองในใบสั่งขายที่ระบุให้กับประเทศที่ระบุในระหว่างช่วงวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a5b35-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="a5b35-159">รวมประเทศต้นทางในรายงาน BOM</span><span class="sxs-lookup"><span data-stu-id="a5b35-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="a5b35-160">เมื่อคุณสร้างรายงาน BOM คุณสามารถรวมประเทศต้นทางสำหรับแต่ละส่วนที่คุณได้ระบุแหล่งที่มาและประเทศปลายทางให้บนหน้า **กฎของประเทศต้นทาง**</span><span class="sxs-lookup"><span data-stu-id="a5b35-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="a5b35-161">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="a5b35-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="a5b35-162">เลือกหรือสร้างผลิตภัณฑ์เพื่อเปิดหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="a5b35-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="a5b35-163">ในบานหน้าต่างการดำเนินการ บนแท็บ **วิศวกรรม** ในกลุ่ม **BOM** ให้เลือก **โปรแกรมออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="a5b35-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="a5b35-164">ในหน้าที่ปรากฏ บนบานหน้าต่างการดำเนินการ เลือก **BOM \> พิมพ์**</span><span class="sxs-lookup"><span data-stu-id="a5b35-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="a5b35-165">ในกล่องโต้ตอบ **รายการสูตรการผลิต** ให้ตั้งค่าฟิลด์ **ประเทศปลายทาง** เป็นประเทศปลายทางที่คุณต้องการดูในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="a5b35-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="a5b35-166">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a5b35-166">Select **OK**.</span></span>

<span data-ttu-id="a5b35-167">รายงานที่แสดงข้อมูลเกี่ยวกับประเทศต้นทางของแต่ละส่วนจะถูกสร้างและแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="a5b35-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="a5b35-168">นี่เป็นตัวอย่างของรายงาน</span><span class="sxs-lookup"><span data-stu-id="a5b35-168">Here is an example of the report.</span></span>

<span data-ttu-id="a5b35-169">![รายงานประเทศต้นทาง](media/country-of-origin-report.png "รายงานประเทศต้นทาง")</span><span class="sxs-lookup"><span data-stu-id="a5b35-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]