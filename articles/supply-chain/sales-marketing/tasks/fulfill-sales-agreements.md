---
title: ปฏิบัติตามข้อตกลงการขาย
description: 'กระบวนงานนี้แสดงวิธีการเติมสินค้าตามข้อตกลงการขายโดยการเชื่อมโยงกับใบสั่งขาย '
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51ea8afc7c2f683790f697185d6637e0d24462fc
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204320"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="93063-103">ปฏิบัติตามข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="93063-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93063-104">กระบวนงานนี้แสดงวิธีการเติมสินค้าตามข้อตกลงการขายโดยการเชื่อมโยงกับใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="93063-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="93063-105">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="93063-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="93063-106">ก่อนที่จะเริ่มคู่มือนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อตกลงการขายที่มีผลบังคับใช้ชนิด "ข้อผูกมัดมูลค่าผลิตภัณฑ์" </span><span class="sxs-lookup"><span data-stu-id="93063-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="93063-107">หรืออีกทางหนึ่งคือ คุณสามารถดำเนินงานคู่มือที่เรียกว่า "สร้างข้อตกลงการขาย"</span><span class="sxs-lookup"><span data-stu-id="93063-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="93063-108">นำใบสั่งขายออกใช้จากข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="93063-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="93063-109">ไปที่ การขายและการตลาด > ข้อตกลงการขาย > ข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="93063-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="93063-110">ในรายการ ให้เปิดข้อตกลงที่คุณต้องการนำใบสั่งออกใช้</span><span class="sxs-lookup"><span data-stu-id="93063-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="93063-111">ในบานหน้าต่างการดำเนินการ คลิกที่ข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="93063-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="93063-112">คลิกการนำใบสั่งออกใช้</span><span class="sxs-lookup"><span data-stu-id="93063-112">Click Release order.</span></span>
    * <span data-ttu-id="93063-113">ดังที่ข้อความด้านบนของหน้าการสร้างใบสั่งย่อยชี้ให้เห็นว่า รายละเอียดที่จำเป็นสำหรับรายการใบสั่งขายจะแตกต่างกันขึ้นอยู่กับข้อตกลงเป็นตามปริมาณหรือตามมูลค่า</span><span class="sxs-lookup"><span data-stu-id="93063-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="93063-114">ข้อตกลงในคู่มือนี้เป็นชนิด "ข้อผูกมัดมูลค่าผลิตภัณฑ์" </span><span class="sxs-lookup"><span data-stu-id="93063-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="93063-115">นี่คือสาเหตุที่ส่วนรายการของหน้านี้ไม่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="93063-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="93063-116">ถ้าข้อผูกมัดเป็นไปตามปริมาณ ข้อมูลรายการจะถูกคัดลอกจากข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="93063-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="93063-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="93063-117">Click Create.</span></span>
    * <span data-ttu-id="93063-118">ข้อความแจ้งให้คุณทราบว่ามีการสร้างใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="93063-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="93063-119">เนื่องจากใบสั่งไม่มีรายการใด คุณต้องเพิ่มรายละเอียดของรายการใบสั่งเพื่อดำเนินขั้นตอนการนำออกใช้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="93063-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="93063-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93063-120">Close the page.</span></span>
7. <span data-ttu-id="93063-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93063-121">Close the page.</span></span>
8. <span data-ttu-id="93063-122">ไปยัง การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="93063-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="93063-123">ในรายการ ให้ค้นหาและเปิดใบสั่งที่สร้างขึ้นจากผลลัพธ์ของการออกใช้ใบสั่งในงานก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="93063-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="93063-124">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="93063-124">Click Add line.</span></span>
11. <span data-ttu-id="93063-125">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="93063-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="93063-126">ในฟิลด์หมายเลขสินค้า ให้พิมพ์หรือเลือกสินค้าที่ระบุไว้ในข้อตกลงการขายที่เชื่อมโยงกัน</span><span class="sxs-lookup"><span data-stu-id="93063-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="93063-127">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="93063-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="93063-128">ตรวจสอบให้แน่ใจว่าคุณได้ป้อนปริมาณที่นำยอดเงินสุทธิภายใต้ค่าของข้อตกลงการขายที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="93063-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="93063-129">โปรดสังเกตว่า เนื่องจากใบสั่งขายนั้นเชื่อมโยงกับข้อตกลง เปอร์เซ็นต์ส่วนลดที่เจรจาไว้จะถูกใช้กับรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="93063-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="93063-130">คลิก อัพเดตรายการ</span><span class="sxs-lookup"><span data-stu-id="93063-130">Click Update line.</span></span>
15. <span data-ttu-id="93063-131">คลิก ที่แนบมา</span><span class="sxs-lookup"><span data-stu-id="93063-131">Click Attached.</span></span>
    * <span data-ttu-id="93063-132">หน้าข้อตกลงที่แนบแสดงรหัสและเงื่อนไขของข้อตกลงที่รายการถูกนำออกมาใช้</span><span class="sxs-lookup"><span data-stu-id="93063-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="93063-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93063-133">Close the page.</span></span>
17. <span data-ttu-id="93063-134">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="93063-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="93063-135">คลิกข้อตกลงการขายที่แนบ</span><span class="sxs-lookup"><span data-stu-id="93063-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="93063-136">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="93063-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="93063-137">คลิกแท็บการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="93063-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="93063-138">แท็บการเติมสินค้าแสดงข้อสรุปของรายการใบสั่งขายทั้งหมดที่เชื่อมโยงกับข้อผูกมัดนี้ และสถานะการเติมสินค้า ตลอดจนยอดเงินหรือปริมาณที่ยังไม่ได้นำออกมาใช้</span><span class="sxs-lookup"><span data-stu-id="93063-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="93063-139">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93063-139">Close the page.</span></span>
22. <span data-ttu-id="93063-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93063-140">Close the page.</span></span>
23. <span data-ttu-id="93063-141">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="93063-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="93063-142">ใช้ข้อตกลงการขายในกระบวนการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="93063-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="93063-143">ไปยัง การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="93063-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="93063-144">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="93063-144">Click New.</span></span>
3. <span data-ttu-id="93063-145">ในฟิลด์บัญชีลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="93063-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="93063-146">ในรายการ ให้ค้นหาและเลือกลูกค้าที่ระบุในข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="93063-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="93063-147">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="93063-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="93063-148">ขยายส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="93063-148">Expand the General section.</span></span>
7. <span data-ttu-id="93063-149">ในฟิลด์รหัสข้อตกลงการขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="93063-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="93063-150">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="93063-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="93063-151">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="93063-151">Click Yes.</span></span>
10. <span data-ttu-id="93063-152">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="93063-152">Click OK.</span></span>
11. <span data-ttu-id="93063-153">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="93063-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="93063-154">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="93063-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="93063-155">ในฟิลด์หมายเลขสินค้า ให้พิมพ์หรือเลือกสินค้าที่ระบุไว้ในข้อตกลงการขายที่เชื่อมโยงกัน</span><span class="sxs-lookup"><span data-stu-id="93063-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="93063-156">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="93063-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="93063-157">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="93063-157">Click Save.</span></span>
16. <span data-ttu-id="93063-158">ในบานหน้าต่างการดำเนินการ ให้คลิก เบิกสินค้าและจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="93063-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="93063-159">คลิก ลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="93063-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="93063-160">ขยายส่วน พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="93063-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="93063-161">เลือก ใช่ ในฟิลด์การลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="93063-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="93063-162">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="93063-162">Click OK.</span></span>
21. <span data-ttu-id="93063-163">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="93063-163">Click OK.</span></span>
22. <span data-ttu-id="93063-164">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="93063-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="93063-165">คลิกข้อตกลงการขายที่แนบ</span><span class="sxs-lookup"><span data-stu-id="93063-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="93063-166">คลิกแท็บการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="93063-166">Click the Fulfillment tab.</span></span>

