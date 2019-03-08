---
title: จัดการการระงับใบสั่ง
description: กระบวนงานนี้อธิบายวิธีการระงับใบสั่งขายของลูกค้า วิธีการทำงานกับการเช็คเอาท์ที่ระงับใบสั่ง และวิธีการลบใบสั่งที่ระงับ
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad19ff166c15748b7bbb4b82ef71dbf3e1e8ebd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "323973"
---
# <a name="manage-order-holds"></a><span data-ttu-id="850a7-103">จัดการการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="850a7-103">Manage order holds</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="850a7-104">กระบวนงานนี้อธิบายวิธีการระงับใบสั่งขายของลูกค้า วิธีการทำงานกับการเช็คเอาท์ที่ระงับใบสั่ง และวิธีการลบใบสั่งที่ระงับ</span><span class="sxs-lookup"><span data-stu-id="850a7-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="850a7-105">ใบสั่งอาจถูกระงับสำหรับเหตุผลต่างๆ</span><span class="sxs-lookup"><span data-stu-id="850a7-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="850a7-106">ตัวอย่างเช่น คุณอาจระงับใบสั่งจนกระทั่งคุณสามารถตรวจสอบที่อยู่หรือการชำระเงินของลูกค้า หรือจนกว่าผู้จัดการสามารถตรวจสอบวงเงินสินเชื่อของลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="850a7-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="850a7-107">ในขณะที่ใบสั่งถูกระงับ จะไม่สามารถประมวลผลตามคลังสินค้าสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="850a7-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="850a7-108">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="850a7-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="850a7-109">ตั้งค่าการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="850a7-109">Set up order holds</span></span>
1. <span data-ttu-id="850a7-110">ไปที่ การขายและการตลาด > การตั้งค่า > ใบสั่งขาย > รหัสการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="850a7-110">Go to Sales and marketing > Setup > Sales orders > Order hold codes.</span></span>
2. <span data-ttu-id="850a7-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="850a7-111">Click New.</span></span>
3. <span data-ttu-id="850a7-112">ในฟิลด์รหัสการระงับ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="850a7-112">In the Hold code field, type a value.</span></span>
    * <span data-ttu-id="850a7-113">ตัวอย่างเช่น พิมพ์ โทรกลับ</span><span class="sxs-lookup"><span data-stu-id="850a7-113">For example, type Call back.</span></span>  
4. <span data-ttu-id="850a7-114">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="850a7-114">In the Description field, type a value.</span></span>
    * <span data-ttu-id="850a7-115">ตัวอย่างเช่น ใบสั่งที่ถูกระงับเพื่อรอลูกค้าโทรกลับ</span><span class="sxs-lookup"><span data-stu-id="850a7-115">For example, Order held waiting for customer callback.</span></span>  
    * <span data-ttu-id="850a7-116">หรือเลือกกล่องกาเครื่องหมายลบการจอง เพื่อลบการจองทางกายภาพจากใบสั่งเมื่อมีการเพิ่มรหัสการระงับนี้</span><span class="sxs-lookup"><span data-stu-id="850a7-116">Optionally, select the Remove reservations check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="850a7-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="850a7-117">Click Save.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="850a7-118">ระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="850a7-118">Place order on hold</span></span>
1. <span data-ttu-id="850a7-119">ไปยัง การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="850a7-119">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="850a7-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="850a7-120">Click New.</span></span>
3. <span data-ttu-id="850a7-121">ในฟิลด์บัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="850a7-121">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="850a7-122">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="850a7-122">Click OK.</span></span>
5. <span data-ttu-id="850a7-123">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="850a7-123">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="850a7-124">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="850a7-124">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="850a7-125">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="850a7-125">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="850a7-126">คลิกการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="850a7-126">Click Order holds.</span></span>
9. <span data-ttu-id="850a7-127">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="850a7-127">Click New.</span></span>
10. <span data-ttu-id="850a7-128">ในฟิลด์รหัสการระงับ เลือกรหัสที่คุณสร้างในงานย่อยก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="850a7-128">In the Hold code field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="850a7-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="850a7-129">Click Save.</span></span>
12. <span data-ttu-id="850a7-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="850a7-130">Close the page.</span></span>
13. <span data-ttu-id="850a7-131">ไปยัง การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="850a7-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
14. <span data-ttu-id="850a7-132">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="850a7-132">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="850a7-133">ใบสั่งที่ถูกระงับอยู่ในขณะนี้มีการทำเครื่องหมายฟิลด์ "ไม่ต้องประมวลผล" และ "ระงับ" อยู่</span><span class="sxs-lookup"><span data-stu-id="850a7-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>    
15. <span data-ttu-id="850a7-134">ในบานหน้าต่างการดำเนินการ ให้คลิก เบิกสินค้าและจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="850a7-134">On the Action Pane, click Pick and pack.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="850a7-135">จัดการการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="850a7-135">Manage order holds</span></span>
1. <span data-ttu-id="850a7-136">ไปที่ การขายและการตลาด > ใบสั่งขาย > ใบสั่งที่เปิด > การระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="850a7-136">Go to Sales and marketing > Sales orders > Open orders > Order holds.</span></span>
    * <span data-ttu-id="850a7-137">หน้าการระงับใบสั่งทำหน้าที่เป็นเวิร์กเบนซ์ ซึ่งคุณสามารถดูภาพรวมของการระงับปัจจุบันและที่ประมวลผลแล้ว และจัดการการระงับเหล่านั้นและใบสั่งขายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="850a7-137">Order holds page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>      
2. <span data-ttu-id="850a7-138">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="850a7-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="850a7-139">ในบานหน้าต่างการดำเนินการ คลิก เช็คเอาท์การระงับ</span><span class="sxs-lookup"><span data-stu-id="850a7-139">On the Action Pane, click Hold checkout.</span></span>
4. <span data-ttu-id="850a7-140">คลิก เช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="850a7-140">Click Check out.</span></span>
5. <span data-ttu-id="850a7-141">ในรายการนี้ ให้ยกเลิกการทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="850a7-141">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="850a7-142">ขณะนี้ฟิลด์เช็คเอาท์ไปยังจะแสดงรหัสผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="850a7-142">The Checkout out to field now shows your user ID.</span></span>   
6. <span data-ttu-id="850a7-143">คลิก ล้างข้อมูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="850a7-143">Click Clear checkout.</span></span>
7. <span data-ttu-id="850a7-144">ในบานหน้าต่างการดำเนินการ คลิก ล้างข้อมูลการระงับ</span><span class="sxs-lookup"><span data-stu-id="850a7-144">On the Action Pane, click Clear hold.</span></span>
    * <span data-ttu-id="850a7-145">เมื่อคุณพร้อมที่จะลบการระงับและอนุญาตให้ดำเนินการใบสั่งไปยังขั้นตอนการเติมเต็มถัดไป คุณจะต้องล้างข้อมูลการระงับ</span><span class="sxs-lookup"><span data-stu-id="850a7-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="850a7-146">ถ้าไม่จำเป็นต้องเปลี่ยนแปลงใบสั่ง คุณสามารถรันการดำเนินการล้างข้อมูลการระงับได้</span><span class="sxs-lookup"><span data-stu-id="850a7-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="850a7-147">อย่างไรก็ตาม คุณสามารถใช้การดำเนินการล้างข้อมูลและปรับเปลี่ยนได้ ถ้าจำเป็นต้องอัพเดตใบสั่งเมื่อทำการล้างข้อมูลการระงับ</span><span class="sxs-lookup"><span data-stu-id="850a7-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    * <span data-ttu-id="850a7-148">การดำเนินการล้างข้อมูลและส่งจะใช้ได้เฉพาะเมื่อคุณใช้ฟังก์ชันข้อมูลศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="850a7-148">The Clear and submit action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="850a7-149">คลิก ล้างข้อมูลการระงับ</span><span class="sxs-lookup"><span data-stu-id="850a7-149">Click Clear holds.</span></span>
    * <span data-ttu-id="850a7-150">ขณะนี้การระงับได้ถูกล้างข้อมูลออกจากใบสั่งและลบออกจากรายการการระงับที่ใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="850a7-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="850a7-151">เมื่อต้องการดูการระงับทั้งหมดหรือเซ็ตย่อยของการระงับตามสถานะหนึ่งๆ ให้เปลี่ยนค่าในฟิลด์แสดง</span><span class="sxs-lookup"><span data-stu-id="850a7-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

