--- 
title: "สร้างข้อตกลงการซื้อ"
description: "ขั้นตอนนี้นำคุณผ่านการสร้างข้อตกลงการซื้อ "
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c547f825c567848b06b84ac1baaa5ae3bc6c2860
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="575de-103">สร้างข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="575de-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="575de-104">ขั้นตอนนี้นำคุณผ่านการสร้างข้อตกลงการซื้อ </span><span class="sxs-lookup"><span data-stu-id="575de-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="575de-105">ซึ่งโดยทั่วไปสามารถทำได้โดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="575de-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="575de-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="575de-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="575de-107">คุณต้องตั้งค่าการจัดประเภทข้อตกลงการซื้อก่อนที่คุณเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="575de-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="575de-108">เมื่อคุณสร้างข้อตกลงแล้ว คุณสามารถใช้เมื่อคุณสร้างใบสั่งซื้อ และนี่จะคัดลอกเงื่อนไขข้อตกลงการซื้อไปยังหัวข้อและรายการที่อยู่ในใบสั่งที่ได้รับผลกระทบโดยข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="575de-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="575de-109">สร้างข้อตกลงการซื้อใหม่</span><span class="sxs-lookup"><span data-stu-id="575de-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="575de-110">ไปที่การจัดซื้อและการจัดหา > ข้อตกลงการซื้อ > ข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="575de-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="575de-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="575de-111">Click New.</span></span>
3. <span data-ttu-id="575de-112">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="575de-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="575de-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="575de-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="575de-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="575de-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="575de-115">ในฟิลด์การจัดประเภทข้อตกลงการสั่งซื้อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="575de-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="575de-116">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="575de-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="575de-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="575de-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="575de-118">ขยายส่วน ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="575de-118">Expand the General section.</span></span>
10. <span data-ttu-id="575de-119">ในฟิลด์วันที่สิ้นสุด ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="575de-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="575de-120">วันหมดอายุนี้จะเป็นค่าเริ่มต้นสำหรับรายการข้อผูกมัดทั้งหมด และจะกำหนดระยะเวลาที่ข้อผูกมัดเฉพาะแต่ละรายการจะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="575de-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="575de-121">ในฟิลด์ชื่อเอกสาร ให้พิมพ์ชื่อข้อตกลงการซื้อของคุณ</span><span class="sxs-lookup"><span data-stu-id="575de-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="575de-122">ปล่อยให้ฟิลด์การตั้งค่าเริ่มต้นข้อผูกมัดตั้งค่าไปที่ข้อผูกมัดปริมาณผลิตภัณฑ์ (หรือเปลี่ยนถ้าไม่มีการตั้งค่านี้)</span><span class="sxs-lookup"><span data-stu-id="575de-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="575de-123">ค่าเริ่มต้นข้อผูกมัดกำหนดตัวเลือกรายการข้อตกลง </span><span class="sxs-lookup"><span data-stu-id="575de-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="575de-124">ถ้าคุณต้องการชนิดข้อผูกมัดใหม่เมื่อคุณกำลังสร้างข้อตกลง คุณจำเป็นต้องเปลี่ยนข้อผูกมัดเริ่มต้นบนส่วนหัว </span><span class="sxs-lookup"><span data-stu-id="575de-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="575de-125">มีข้อผูกมัด 4 ชนิด: ข้อผูกมัดปริมาณผลิตภัณฑ์ - สำหรับระบุปริมาณแต่ละผลิตภัณฑ์ ข้อผูกมัดมูลค่าผลิตภัณฑ์ - สำหรับระบุจำนวนสกุลเงินของแต่ละผลิตภัณฑ์ ข้อผูกมัดมูลค่าประเภทผลิตภัณฑ์ - สำหรับระบุจำนวนสกุลเงินในแต่ละประเภทการจัดซื้อที่จำนวนเงินสามารถเป็นยอดเงินสำหรับแค็ตตาล็อกสินค้าหรือสินค้าไม่มีในแค็ตตาล็อก ข้อผูกมัดมูลค่า - สำหรับระบุจำนวนสกุลเงินซึ่งสามารถดำเนินการตามผลิตภัณฑ์ใดๆหรือตามประเภทการจัดซื้อใดๆ</span><span class="sxs-lookup"><span data-stu-id="575de-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="575de-126">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="575de-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="575de-127">เพิ่มข้อผูกมัด</span><span class="sxs-lookup"><span data-stu-id="575de-127">Add a commitment</span></span>
1. <span data-ttu-id="575de-128">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="575de-128">Click Add line.</span></span>
2. <span data-ttu-id="575de-129">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="575de-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="575de-130">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="575de-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="575de-131">เลือกผลิตภัณฑ์คุณต้องการเพิ่มข้อผูกมัด</span><span class="sxs-lookup"><span data-stu-id="575de-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="575de-132">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="575de-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="575de-133">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="575de-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="575de-134">นี่คือปริมาณรวมที่คุณได้ตกลงที่จะซื้อจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="575de-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="575de-135">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="575de-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="575de-136">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="575de-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="575de-137">ตั้งค่าตัวเลือกค่าสูงสุดที่ถูกบังคับใช้เป็นใช่</span><span class="sxs-lookup"><span data-stu-id="575de-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="575de-138">ค่าสูงสุดจะบังคับตัวเลือกที่จะใช้ข้อผูกมัด </span><span class="sxs-lookup"><span data-stu-id="575de-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="575de-139">คุณสามารถซื้อจนถึงปริมาณที่ระบุในฟิลด์ปริมาณสำหรับรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="575de-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="575de-140">ยุบส่วนรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="575de-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="575de-141">เพิ่มเงื่อนไขส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="575de-141">Add header conditions</span></span>
1. <span data-ttu-id="575de-142">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="575de-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="575de-143">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="575de-143">Click Change view.</span></span>
3. <span data-ttu-id="575de-144">คลิกมุมมองหัวข้อ </span><span class="sxs-lookup"><span data-stu-id="575de-144">Click Header view.</span></span>
4. <span data-ttu-id="575de-145">ขยายส่วน ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="575de-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="575de-146">ในฟิลด์วิธีการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="575de-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="575de-147">เงื่อนไขการชำระเงินจากบัญชีผู้จัดจำหน่ายจะแสดงไว้ที่นี่โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="575de-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="575de-148">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="575de-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="575de-149">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="575de-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="575de-150">ในฟิลด์วิธีการจัดส่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="575de-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="575de-151">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="575de-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="575de-152">ในฟิลด์เงื่อนไขการจัดส่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="575de-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="575de-153">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="575de-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="575de-154">ยืนยันและเรียกใช้ข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="575de-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="575de-155">ในบานหน้าต่างการดำเนินการ คลิกที่ข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="575de-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="575de-156">คลิกการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="575de-156">Click Confirmation.</span></span>
    * <span data-ttu-id="575de-157">ตั้งค่าข้อตกลงโดยทำเครื่องหมายมีผลบังคับใช้เป็นใช่</span><span class="sxs-lookup"><span data-stu-id="575de-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="575de-158">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="575de-158">Click OK.</span></span>
4. <span data-ttu-id="575de-159">ในบานหน้าต่างการดำเนินการ คลิกที่ข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="575de-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="575de-160">คลิกยืนยันข้อตกลงการซื้อ</span><span class="sxs-lookup"><span data-stu-id="575de-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="575de-161">ตัวเลือกการแสดงตัวอย่าง/พิมพ์อนุญาตให้คุณสร้างเอกสารสำหรับข้อตกลงการซื้อซึ่งคุณสามารถพิมพ์ หรือส่งไปยังผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="575de-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="575de-162">ถ้าคุณอัพเดตข้อตกลงในภายหลัง และยืนยันอีกครั้ง เวอร์ชันทั้งสองจะถูกแสดงที่นี่</span><span class="sxs-lookup"><span data-stu-id="575de-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="575de-163">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="575de-163">Close the page.</span></span>


