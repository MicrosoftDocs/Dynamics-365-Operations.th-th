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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596282"
---
# <a name="country-of-origin"></a><span data-ttu-id="45f88-105">ประเทศของผู้ผลิต</span><span class="sxs-lookup"><span data-stu-id="45f88-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45f88-106">องค์กรจำนวนมากออกใบรับรองให้กับผู้จัดจำหน่ายของพวกเขา เพื่อให้มั่นใจว่าผลิตภัณฑ์ตรงตามมาตรฐานการรับรองเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="45f88-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="45f88-107">ใบรับรองเหล่านี้มักจะขึ้นอยู่กับประเทศต้นทาง</span><span class="sxs-lookup"><span data-stu-id="45f88-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="45f88-108">คุณลักษณะประเทศต้นทางช่วยให้คุณสามารถเชื่อมโยงผลิตภัณฑ์ไปยังประเทศต้นทางและติดตามการรับรองผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45f88-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="45f88-109">ตั้งค่าคอนฟิกประเทศต้นทางและประเทศปลายทาง</span><span class="sxs-lookup"><span data-stu-id="45f88-109">Configure source and destination countries</span></span>

<span data-ttu-id="45f88-110">ก่อนที่คุณจะออกใบรับรองสำหรับผลิตภัณฑ์ คุณต้องเชื่อมโยงผลิตภัณฑ์ไปยังประเทศปลายทางและประเทศต้นทาง</span><span class="sxs-lookup"><span data-stu-id="45f88-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="45f88-111">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> การตั้งค่า \> การปฏิบัติตามกฎระเบียบด้านผลิตภัณฑ์ \> ประเทศต้นทาง \> กฎของประเทศต้นทาง**</span><span class="sxs-lookup"><span data-stu-id="45f88-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="45f88-112">เลือกการตั้งค่าประเทศที่มีอยู่เพื่อแก้ไข หรือเลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อสร้างการตั้งค่าประเทศใหม่</span><span class="sxs-lookup"><span data-stu-id="45f88-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="45f88-113">ตั้งค่าค่าต่อไปนี้สำหรับประเทศที่เลือกหรือประเทศใหม่</span><span class="sxs-lookup"><span data-stu-id="45f88-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="45f88-114">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="45f88-114">Field</span></span> | <span data-ttu-id="45f88-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="45f88-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="45f88-116">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="45f88-116">Item number</span></span> | <span data-ttu-id="45f88-117">เลือกหมายเลขสินค้าของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45f88-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="45f88-118">ประเทศปลายทาง</span><span class="sxs-lookup"><span data-stu-id="45f88-118">Destination country</span></span> | <span data-ttu-id="45f88-119">เลือกประเทศที่คุณกำลังส่งผลิตภัณฑ์ไป</span><span class="sxs-lookup"><span data-stu-id="45f88-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="45f88-120">ประเทศต้นทาง</span><span class="sxs-lookup"><span data-stu-id="45f88-120">Origin country</span></span> | <span data-ttu-id="45f88-121">เลือกประเทศที่คุณกำลังจัดส่งผลิตภัณฑ์มา</span><span class="sxs-lookup"><span data-stu-id="45f88-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="45f88-122">วัตถุประสงค์ของการตั้งค่านี้คือเพื่อช่วยคุณในการสร้างรายงานสูตรการผลิต (BOM) ที่คุณสามารถรวมประเทศต้นทางสำหรับแต่ละส่วนที่มีการระบุประเทศต้นทางและประเทศปลายทางให้</span><span class="sxs-lookup"><span data-stu-id="45f88-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="45f88-123">รายงานนี้จะช่วยให้คุณได้รับภาพรวมของสถานที่ที่วัตถุดิบของคุณมาและสถานที่ที่จะไป</span><span class="sxs-lookup"><span data-stu-id="45f88-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="45f88-124">ติดตามใบรับรองของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="45f88-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="45f88-125">คุณสามารถใช้หน้า **ใบรับรองของผู้จัดจำหน่ายของประเทศต้นทาง** เพื่อติดตามใบรับรองที่คุณออกให้กับผู้จัดจำหน่ายได้</span><span class="sxs-lookup"><span data-stu-id="45f88-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="45f88-126">คุณต้องตัดสินใจว่าเอกสารใบรับรองใดที่คุณกำลังออกและคุณจะรายงานใบรับรองเหล่านั้นให้กับลูกค้าอย่างไร</span><span class="sxs-lookup"><span data-stu-id="45f88-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="45f88-127">คุณลักษณะนี้จะช่วยให้คุณติดตามใบรับรองของคุณได้</span><span class="sxs-lookup"><span data-stu-id="45f88-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="45f88-128">นอกจากนี้ คุณยังสามารถเลือกได้ว่าจะให้หมายเลขใบรับรองที่เกี่ยวข้องปรากฏบนใบแจ้งหนี้ บันทึกการจัดส่ง และ/หรือ การยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="45f88-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="45f88-129">ถ้าต้องการตั้งค่าข้อมูลใบรับรองของคุณ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="45f88-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="45f88-130">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> การตั้งค่า \> การปฏิบัติตามกฎระเบียบด้านผลิตภัณฑ์ \> ประเทศต้นทาง \> ใบรับรองของผู้จัดจำหน่ายของประเทศต้นทาง**</span><span class="sxs-lookup"><span data-stu-id="45f88-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="45f88-131">เลือกการตั้งค่าใบรับรองที่มีอยู่เพื่อแก้ไข หรือเลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อสร้างการตั้งค่าใบรับรองใหม่</span><span class="sxs-lookup"><span data-stu-id="45f88-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="45f88-132">กำหนดการตั้งค่าต่อไปนี้สำหรับใบรับรองที่เลือกหรือใบรับรองใหม่</span><span class="sxs-lookup"><span data-stu-id="45f88-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="45f88-133">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="45f88-133">Field</span></span> | <span data-ttu-id="45f88-134">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="45f88-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="45f88-135">บัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="45f88-135">Vendor account</span></span> | <span data-ttu-id="45f88-136">เลือกผู้จัดจำหน่ายที่คุณออกใบรับรองให้</span><span class="sxs-lookup"><span data-stu-id="45f88-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="45f88-137">หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="45f88-137">Item number</span></span> | <span data-ttu-id="45f88-138">เลือกสินค้าที่คุณออกใบรับรองให้</span><span class="sxs-lookup"><span data-stu-id="45f88-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="45f88-139">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="45f88-139">Country/region</span></span> | <span data-ttu-id="45f88-140">ประเทศหรือภูมิภาคปลายทางที่คุณต้องใช้ใบรับรองนี้</span><span class="sxs-lookup"><span data-stu-id="45f88-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="45f88-141">หมายเลขใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="45f88-141">Certificate number</span></span> | <span data-ttu-id="45f88-142">ป้อนหมายเลขการระบุรหัสประจำตัวของใบรับรองที่คุณออก</span><span class="sxs-lookup"><span data-stu-id="45f88-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="45f88-143">มีผล</span><span class="sxs-lookup"><span data-stu-id="45f88-143">Effective</span></span> | <span data-ttu-id="45f88-144">เลือกวันที่เริ่มต้นที่ใบรับรองปัจจุบันมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="45f88-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="45f88-145">การหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="45f88-145">Expiration</span></span> | <span data-ttu-id="45f88-146">เลือกวันที่สุดท้ายที่ใบรับรองปัจจุบันมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="45f88-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="45f88-147">พิมพ์บนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="45f88-147">Print on invoice</span></span> | <span data-ttu-id="45f88-148">เลือกกล่องกาเครื่องหมายนี้เพื่อพิมพ์หมายเลขใบรับรองในใบแจ้งหนี้ที่ระบุให้กับประเทศที่ระบุในระหว่างช่วงวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="45f88-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="45f88-149">พิมพ์ในบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="45f88-149">Print on packing slip</span></span> | <span data-ttu-id="45f88-150">เลือกกล่องกาเครื่องหมายนี้เพื่อพิมพ์หมายเลขใบรับรองในบันทึกการจัดส่งที่ระบุให้กับประเทศที่ระบุในระหว่างช่วงวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="45f88-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="45f88-151">พิมพ์ในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="45f88-151">Print on sales order</span></span> | <span data-ttu-id="45f88-152">เลือกกล่องกาเครื่องหมายนี้เพื่อพิมพ์หมายเลขใบรับรองในใบสั่งขายที่ระบุให้กับประเทศที่ระบุในระหว่างช่วงวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="45f88-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="45f88-153">รวมประเทศต้นทางในรายงาน BOM</span><span class="sxs-lookup"><span data-stu-id="45f88-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="45f88-154">เมื่อคุณสร้างรายงาน BOM คุณสามารถรวมประเทศต้นทางสำหรับแต่ละส่วนที่คุณได้ระบุแหล่งที่มาและประเทศปลายทางให้บนหน้า **กฎของประเทศต้นทาง**</span><span class="sxs-lookup"><span data-stu-id="45f88-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="45f88-155">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="45f88-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="45f88-156">เลือกหรือสร้างผลิตภัณฑ์เพื่อเปิดหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="45f88-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="45f88-157">ในบานหน้าต่างการดำเนินการ บนแท็บ **วิศวกรรม** ในกลุ่ม **BOM** ให้เลือก **โปรแกรมออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="45f88-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="45f88-158">ในหน้าที่ปรากฏ บนบานหน้าต่างการดำเนินการ เลือก **BOM \> พิมพ์**</span><span class="sxs-lookup"><span data-stu-id="45f88-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="45f88-159">ในกล่องโต้ตอบ **รายการสูตรการผลิต** ให้ตั้งค่าฟิลด์ **ประเทศปลายทาง** เป็นประเทศปลายทางที่คุณต้องการดูในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="45f88-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="45f88-160">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="45f88-160">Select **OK**.</span></span>

<span data-ttu-id="45f88-161">รายงานที่แสดงข้อมูลเกี่ยวกับประเทศต้นทางของแต่ละส่วนจะถูกสร้างและแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="45f88-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="45f88-162">นี่เป็นตัวอย่างของรายงาน</span><span class="sxs-lookup"><span data-stu-id="45f88-162">Here is an example of the report.</span></span>

<span data-ttu-id="45f88-163">![รายงานประเทศต้นทาง](media/country-of-origin-report.png "รายงานประเทศต้นทาง")</span><span class="sxs-lookup"><span data-stu-id="45f88-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
