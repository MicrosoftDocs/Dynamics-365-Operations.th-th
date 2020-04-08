---
title: ข้อมูลใบแจ้งหนี้ที่สำคัญใน AP ที่ใช้ใบแจ้งหนี้ของผู้จัดจำหน่าย
description: คู่มืองานนี้จะช่วยคุณสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายจากใบสั่งซื้อ และดูผลลัพธ์ของการจับคู่ใบสั่งซื้อ ใบรับ และใบแจ้งหนี้ (วิธีการจับคู่ 3 ทาง)
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f80c88b7fb3542f624d233f670cd7cd6ccd48b94
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143937"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="5727d-103">ข้อมูลใบแจ้งหนี้ที่สำคัญใน AP ที่ใช้ใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5727d-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5727d-104">คู่มืองานนี้จะช่วยคุณสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายจากใบสั่งซื้อ และดูผลลัพธ์ของการจับคู่ใบสั่งซื้อ ใบรับ และใบแจ้งหนี้ (วิธีการจับคู่ 3 ทาง)</span><span class="sxs-lookup"><span data-stu-id="5727d-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="5727d-105">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="5727d-105">Create a purchase order</span></span>
1. <span data-ttu-id="5727d-106">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5727d-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="5727d-107">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="5727d-107">Click **New**.</span></span>
3. <span data-ttu-id="5727d-108">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5727d-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5727d-109">ค้นหาผู้จัดจำหน่ายเพื่อเลือก </span><span class="sxs-lookup"><span data-stu-id="5727d-109">Find a vendor to select.</span></span> <span data-ttu-id="5727d-110">ตัวอย่างเช่น เลื่อนลงไปที่ US-104</span><span class="sxs-lookup"><span data-stu-id="5727d-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="5727d-111">เลือกผู้จัดจำหน่าย US-104</span><span class="sxs-lookup"><span data-stu-id="5727d-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="5727d-112">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5727d-112">Click **OK**.</span></span>
7. <span data-ttu-id="5727d-113">ในฟิลด์ **หมายเลขสินค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5727d-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5727d-114">เลือกสินค้าในสินค้าคงคลัง </span><span class="sxs-lookup"><span data-stu-id="5727d-114">Select an inventory item.</span></span> <span data-ttu-id="5727d-115">ตัวอย่างเช่น เลือกสินค้าหมายเลข 1000</span><span class="sxs-lookup"><span data-stu-id="5727d-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="5727d-116">ขยาย fastTab **รายละเอียดรายการ**</span><span class="sxs-lookup"><span data-stu-id="5727d-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="5727d-117">คลิกแท็บ **การตั้งค่า** คุณสามารถแทนที่นโยบายการจับคู่เพื่อใช้ไม่มีการจับคู่ การจับคู่ 2 ทาง หรือการจับคู่ 3 ทาง</span><span class="sxs-lookup"><span data-stu-id="5727d-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="5727d-118">บนบานหน้าต่างการดำเนินการ คลิก **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="5727d-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="5727d-119">คลิก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="5727d-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="5727d-120">รับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5727d-120">Receive the products</span></span>
1. <span data-ttu-id="5727d-121">บนบานหน้าต่างการดำเนินการ คลิก **รับ**</span><span class="sxs-lookup"><span data-stu-id="5727d-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="5727d-122">คลิก **ใบรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="5727d-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="5727d-123">ในฟิลด์ **ใบรับผลิตภัณฑ์** ให้ป้อนหมายเลขใบรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5727d-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="5727d-124">ตัวอย่างเช่น ป้อน PR123</span><span class="sxs-lookup"><span data-stu-id="5727d-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="5727d-125">คลิก **ตกลง** เพื่อลงรายการบัญชีใบรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5727d-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="5727d-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5727d-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="5727d-127">สร้างใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5727d-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="5727d-128">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อที่ได้รับแต่ยังไม่ได้ออกใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="5727d-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="5727d-129">เลือกใบสั่งซื้อที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="5727d-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="5727d-130">บนบานหน้าต่างการดำเนินการ คลิก **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="5727d-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="5727d-131">คลิก **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="5727d-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="5727d-132">ในฟิลด์ **หมายเลข** ให้ป้อนหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="5727d-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="5727d-133">ในฟิลด์ **คำอธิบายใบแจ้งหนี้** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5727d-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="5727d-134">ในฟิลด์ **วันที่ของใบแจ้งหนี้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="5727d-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="5727d-135">ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อน 1200</span><span class="sxs-lookup"><span data-stu-id="5727d-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="5727d-136">คลิก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="5727d-136">Click **Add line**.</span></span>
10. <span data-ttu-id="5727d-137">ในฟิลด์ **หมายเลขสินค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5727d-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5727d-138">ในรายการ ให้ค้นหาหมายเลขสินค้าที่มีค่าธรรมเนียมการติดตั้ง </span><span class="sxs-lookup"><span data-stu-id="5727d-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="5727d-139">ตัวอย่างเช่น S0001</span><span class="sxs-lookup"><span data-stu-id="5727d-139">For example, S0001</span></span>
12. <span data-ttu-id="5727d-140">เลือกหมายเลขสินค้าที่มีค่าธรรมเนียมการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="5727d-140">Select the installation charge item number.</span></span> <span data-ttu-id="5727d-141">โปรดทราบว่า การจับคู่จะไม่เกิดขึ้นหลังจากที่คุณทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="5727d-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="5727d-142">คลิก **ปรับปรุงสถานะการจับคู่**</span><span class="sxs-lookup"><span data-stu-id="5727d-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="5727d-143">บนบานหน้าต่างการดำเนินการ ให้คลิก **ทบทวน**</span><span class="sxs-lookup"><span data-stu-id="5727d-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="5727d-144">คลิก **รายละเอียดการจับคู่**</span><span class="sxs-lookup"><span data-stu-id="5727d-144">Click **Matching details**.</span></span> <span data-ttu-id="5727d-145">การบริการรายการใหม่ไม่จำเป็นต้องถูกจับคู่ ดังนั้นสถานะคงอยู่ที่ "ไม่ดำเนินการ"</span><span class="sxs-lookup"><span data-stu-id="5727d-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="5727d-146">เลือกใบรับสินค้าสำหรับสินค้าคงคลังที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="5727d-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="5727d-147">รายการที่มีใบรับสินค้าได้รับการจับคู่ แต่ปริมาณหรือราคาไม่ตรงกัน ดังนั้นการจับคู่จึงไม่สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="5727d-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="5727d-148">ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="5727d-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="5727d-149">หลังจากที่มีการจับคู่ราคาต่อหน่วย สถานะจะถูกอัพเดตเป็นผ่าน</span><span class="sxs-lookup"><span data-stu-id="5727d-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="5727d-150">ถ้านโยบายของคุณอนุญาตมีความขัดแย้งหรือถ้าการจับคู่เป็นเพียงแค่คำเตือน คุณยังคงสามารถลงรายการใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="5727d-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="5727d-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5727d-151">Close the page.</span></span>
19. <span data-ttu-id="5727d-152">คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="5727d-152">Click **Post**.</span></span>
20. <span data-ttu-id="5727d-153">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="5727d-153">Close the form.</span></span> <span data-ttu-id="5727d-154">โปรดทราบว่า จะไม่มีใบสั่งซื้อที่ถูกระบุเป็นได้รับแล้วแต่ไม่ได้ออกใบแจ้งหนี้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="5727d-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

