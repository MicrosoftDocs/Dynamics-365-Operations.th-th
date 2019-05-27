---
title: สร้างคำขอใบเสนอราคา
description: 'กระบวนงานนี้แสดงให้คุณเห็นถึงวิธีการสร้างคำขอใบเสนอราคา '
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c09149fcbe5731126c2e48a37fafdf71c1d49df
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552964"
---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="7c8ad-103">สร้างคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="7c8ad-103">Create a request for quotation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7c8ad-104">กระบวนงานนี้แสดงให้คุณเห็นถึงวิธีการสร้างคำขอใบเสนอราคา </span><span class="sxs-lookup"><span data-stu-id="7c8ad-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="7c8ad-105">โดยทั่วไปจะถูกดำเนินการโดยตัวแทนขาย</span><span class="sxs-lookup"><span data-stu-id="7c8ad-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="7c8ad-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="7c8ad-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="7c8ad-107">คุณต้องตั้งค่าชนิดการร้องขอ ก่อนที่คุณจะเริ่ม</span><span class="sxs-lookup"><span data-stu-id="7c8ad-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="7c8ad-108">เมื่อคุณได้ดำเนินงานนี้เสร็จสมบูรณ์แล้วและคุณได้สร้างและส่ง RFQ แล้ว จากนั้นคุณสามารถป้อนการตอบต่อหนึ่งผู้จัดจำหน่าย เปรียบเทียบ และให้สัญญา</span><span class="sxs-lookup"><span data-stu-id="7c8ad-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="7c8ad-109">เตรียม RFQ ใหม่</span><span class="sxs-lookup"><span data-stu-id="7c8ad-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="7c8ad-110">ไปที่การจัดซื้อและการจัดหา > คำขอใบเสนอราคา > คำขอใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7c8ad-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="7c8ad-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7c8ad-111">Click New.</span></span>
    * <span data-ttu-id="7c8ad-112">ชนิดการซื้อที่พร้อมใช้งานมีดังนี้: ใบสั่งซื้อ (เป็นค่าเริ่มต้น): เอกสารที่ยืนยันข้อเสนอการซื้อผลิตภัณฑ์ หรือการยอมรับข้อเสนอการขายผลิตภัณฑ์ในการแลกเปลี่ยนกับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7c8ad-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="7c8ad-113">ข้อตกลงการซื้อ: ชนิดนี้ถูกเลือกโดยอัตโนมัติถ้าคุณสร้าง RFQ โดยตรงจากใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="7c8ad-114">ถ้าคุณเลือกการซื้อชนิดนี้ด้วยตนเอง คุณจะได้รับข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="7c8ad-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="7c8ad-115">ข้อตกลงการซื้อ: ข้อตกลงเพื่อการซื้อปริมาณเฉพาะหรือมูลค่าของผลิตภัณฑ์ตลอดช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="7c8ad-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="7c8ad-116">ถ้าคุณเลือกตัวเลือกนี้ คุณต้องเลือกช่วงวันที่ใช้กับข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="7c8ad-117">ในฟิลด์หัวข้อเอกสาร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7c8ad-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="7c8ad-118">ในฟิลด์ชนิดการร้องขอ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="7c8ad-119">ถ้าวิธีการให้คะแนนเชื่อมโยงกับชนิดการร้องขอ วิธีการนั้นจะเป็นวิธีการให้คะแนนเริ่มต้นสำหรับ RFQ ที่คุณกำลังสร้าง </span><span class="sxs-lookup"><span data-stu-id="7c8ad-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="7c8ad-120">คุณสามารถเปลี่ยนวิธีการให้คะแนนได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="7c8ad-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="7c8ad-121">ในฟิลด์วันที่การจัดส่ง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="7c8ad-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="7c8ad-122">เลือกวันที่ที่คุณต้องการได้รับสินค้าที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="7c8ad-123">ในฟิลด์วันที่และเวลาหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="7c8ad-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="7c8ad-124">ระบุวันที่และเวลา โดยที่ผู้จัดจำหน่ายต้องตอบสนองต่อ RFQ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="7c8ad-125">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7c8ad-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7c8ad-126">ที่อยู่การจัดส่งจะเป็นค่าเริ่มต้นให้กับที่อยู่คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="7c8ad-127">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7c8ad-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="7c8ad-128">เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-128">Add lines</span></span>
    * <span data-ttu-id="7c8ad-129">หลังจากที่คุณได้ระบุข้อมูลพื้นฐานเกี่ยวกับ RFQ ของคุณ คุณระบุสินค้าหรือบริการที่คุณต้องการให้ผู้จัดจำหน่ายประมูล </span><span class="sxs-lookup"><span data-stu-id="7c8ad-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="7c8ad-130">สินค้าเป็นชนิดรายการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7c8ad-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="7c8ad-131">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7c8ad-132">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก 'T0020' ได้</span><span class="sxs-lookup"><span data-stu-id="7c8ad-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="7c8ad-133">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7c8ad-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="7c8ad-134">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-134">Click Add line.</span></span>
4. <span data-ttu-id="7c8ad-135">ในฟิลด์ชนิดรายการ เลือก 'ประเภท'</span><span class="sxs-lookup"><span data-stu-id="7c8ad-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="7c8ad-136">คุณสามารถใช้ชนิดรายการของประเภท เพื่อสร้าง RFQ สำหรับสินค้าหรือบริการที่ไม่มีสินค้าคงคลัง </span><span class="sxs-lookup"><span data-stu-id="7c8ad-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="7c8ad-137">จากนั้นคุณต้องเลือกชนิดของสินค้าหรือบริการจากลำดับของประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="7c8ad-138">ในฟิลด์การจัดซื้อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7c8ad-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="7c8ad-139">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="7c8ad-140">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7c8ad-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="7c8ad-141">ในฟิลด์หน่วย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="7c8ad-142">เพิ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7c8ad-142">Add vendors</span></span>
1. <span data-ttu-id="7c8ad-143">คลิกส่วนหัวเพื่อเปลี่ยนจากมุมมองรายการ เป็นมุมมองส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="7c8ad-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="7c8ad-144">ขยายส่วนผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7c8ad-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="7c8ad-145">คลิกเพิ่มผู้จัดจำหน่ายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="7c8ad-146">คุณสามารถเพิ่มผู้จัดจำหน่ายไปยัง RFQ ได้โดยอัตโนมัติ ตามประเภทการจัดซื้อของสินค้าที่ร้องขอได้ </span><span class="sxs-lookup"><span data-stu-id="7c8ad-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="7c8ad-147">ถ้าไม่มีผู้จัดจำหน่ายใดได้รับอนุมัติสำหรับชนิด ซึ่งรวมถึงรายการที่คุณเพิ่มให้กับผู้จัดจำหน่ายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="7c8ad-148">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="7c8ad-148">Click Add.</span></span>
5. <span data-ttu-id="7c8ad-149">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="7c8ad-150">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="7c8ad-150">Click Add.</span></span>
7. <span data-ttu-id="7c8ad-151">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="7c8ad-152">เมื่อคุณได้เลือกผู้จัดจำหน่าย สถานะจะเป็น สร้างแล้ว </span><span class="sxs-lookup"><span data-stu-id="7c8ad-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="7c8ad-153">ซึ่งหมายความว่า ข้อมูลของผู้จัดจำหน่ายที่ได้รับการบันทึกใน RFQ แล้ว แต่คุณยังไม่ได้ส่ง RFQ ไปยังผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7c8ad-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="7c8ad-154">คุณสามารถเพิ่มผู้จัดจำหน่ายให้กับ RFQ ได้โดยไม่ต้องคำนึงถึงสถานะของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7c8ad-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="7c8ad-155">ส่ง RFQ ไปยังผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7c8ad-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="7c8ad-156">คลิก ส่ง</span><span class="sxs-lookup"><span data-stu-id="7c8ad-156">Click Send.</span></span>
    * <span data-ttu-id="7c8ad-157">ในหน้าการส่งคำขอใบเสนอราคา คลิกผู้จัดจำหน่ายในรายการซึ่งเป็นผู้จัดจำหน่ายที่คุณต้องการได้รับ RFQ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="7c8ad-158">คลิก พิมพ์</span><span class="sxs-lookup"><span data-stu-id="7c8ad-158">Click Print.</span></span>
    * <span data-ttu-id="7c8ad-159">กล่องโต้ตอบนี้อนุญาตให้คุณพิมพ์ RFQ ได้ </span><span class="sxs-lookup"><span data-stu-id="7c8ad-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="7c8ad-160">ถ้าคุณเลือกที่จะพิมพ์แผ่นงานการตอบ เนื้อหาของแผ่นงานนี้จะถูกกำหนดไว้ในพารามิเตอร์การจัดซื้อและการจัดหา </span><span class="sxs-lookup"><span data-stu-id="7c8ad-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="7c8ad-161">เพื่อเลือกวิธีการพิมพ์แผ่นงานการตอบ เมื่อคุณได้เปิดกล่องโต้ตอบการพิมพ์ คลิกตัวเลือกการพิมพ์ขั้นสูง RFQ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="7c8ad-162">หนึ่งรายการจะถูกพิมพ์สำหรับผู้จัดจำหน่ายแต่ละราย ซึ่งประกอบด้วยรายการที่มีสถานะเป็น สร้างแล้วหรือถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="7c8ad-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="7c8ad-163">ระบบจะไม่พิมพ์บรรทัดที่ถูกยกเลิกและบรรทัดที่มีการตอบที่ลงทะเบียนแล้ว</span><span class="sxs-lookup"><span data-stu-id="7c8ad-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="7c8ad-164">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="7c8ad-164">Click Cancel.</span></span>
4. <span data-ttu-id="7c8ad-165">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7c8ad-165">Click OK.</span></span>
5. <span data-ttu-id="7c8ad-166">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-166">Close the page.</span></span>
6. <span data-ttu-id="7c8ad-167">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="7c8ad-168">ดูสมุดรายวัน RFQ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-168">View the RFQ journal</span></span>
1. <span data-ttu-id="7c8ad-169">ไปที่การจัดซื้อและการจัด > คำขอใบเสนอราคา > การติดตามผลคำขอใบเสนอราคาทั้งหมด > สมุดรายวันคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="7c8ad-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="7c8ad-170">คลิกตัวอย่างก่อนพิมพ์/พิมพ์</span><span class="sxs-lookup"><span data-stu-id="7c8ad-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="7c8ad-171">คลิกการแสดงตัวอย่างต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="7c8ad-171">Click Original preview.</span></span>
4. <span data-ttu-id="7c8ad-172">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-172">Close the page.</span></span>
5. <span data-ttu-id="7c8ad-173">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7c8ad-173">Close the page.</span></span>

