---
title: จัดการการระงับใบสั่ง
description: กระบวนงานนี้อธิบายวิธีการระงับใบสั่งขายของลูกค้า วิธีการทำงานกับการเช็คเอาท์ที่ระงับใบสั่ง และวิธีการลบใบสั่งที่ระงับ
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27a5149812a8e478dae1d2385e6c139c9f635202
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010758"
---
# <a name="manage-order-holds"></a><span data-ttu-id="be24a-103">จัดการการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="be24a-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be24a-104">กระบวนงานนี้อธิบายวิธีการระงับใบสั่งขายของลูกค้า วิธีการทำงานกับการเช็คเอาท์ที่ระงับใบสั่ง และวิธีการลบใบสั่งที่ระงับ</span><span class="sxs-lookup"><span data-stu-id="be24a-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="be24a-105">ใบสั่งอาจถูกระงับสำหรับเหตุผลต่างๆ</span><span class="sxs-lookup"><span data-stu-id="be24a-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="be24a-106">ตัวอย่างเช่น คุณอาจระงับใบสั่งจนกระทั่งคุณสามารถตรวจสอบที่อยู่หรือการชำระเงินของลูกค้า หรือจนกว่าผู้จัดการสามารถตรวจสอบวงเงินสินเชื่อของลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="be24a-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="be24a-107">ในขณะที่ใบสั่งถูกระงับ จะไม่สามารถประมวลผลตามคลังสินค้าสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="be24a-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="be24a-108">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="be24a-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="be24a-109">ตั้งค่าการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="be24a-109">Set up order holds</span></span>
1. <span data-ttu-id="be24a-110">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การขายและการตลาด > การตั้งค่า > ใบสั่งขาย > รหัสการระงับใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="be24a-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="be24a-111">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="be24a-111">Click **New**.</span></span>
3. <span data-ttu-id="be24a-112">ในฟิลด์ **รหัสการระงับ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="be24a-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="be24a-113">ตัวอย่างเช่น พิมพ์ โทรกลับ</span><span class="sxs-lookup"><span data-stu-id="be24a-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="be24a-114">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="be24a-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="be24a-115">ตัวอย่างเช่น ใบสั่งที่ถูกระงับเพื่อรอลูกค้าโทรกลับ</span><span class="sxs-lookup"><span data-stu-id="be24a-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="be24a-116">หรือเลือกกล่องกาเครื่องหมาย **ลบการจอง** เพื่อลบการจองทางกายภาพจากใบสั่งเมื่อมีการเพิ่มรหัสการระงับนี้</span><span class="sxs-lookup"><span data-stu-id="be24a-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="be24a-117">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="be24a-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="be24a-118">ระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="be24a-118">Place order on hold</span></span>
1. <span data-ttu-id="be24a-119">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="be24a-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="be24a-120">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="be24a-120">Click **New**.</span></span>
3. <span data-ttu-id="be24a-121">ในฟิลด์ **บัญชีลูกค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="be24a-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="be24a-122">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="be24a-122">Click **OK**.</span></span>
5. <span data-ttu-id="be24a-123">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="be24a-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="be24a-124">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="be24a-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="be24a-125">ใน **บานหน้าต่างการดำเนินการ** ให้คลิก **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="be24a-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="be24a-126">คลิก **การระงับใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="be24a-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="be24a-127">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="be24a-127">Click **New**.</span></span>
10. <span data-ttu-id="be24a-128">ในฟิลด์ **รหัสการระงับ** เลือกรหัสที่คุณสร้างในงานย่อยก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="be24a-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="be24a-129">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="be24a-129">Click **Save**.</span></span>
12. <span data-ttu-id="be24a-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="be24a-130">Close the page.</span></span>
13. <span data-ttu-id="be24a-131">ไปยัง **การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="be24a-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="be24a-132">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be24a-132">In the list, mark the selected row.</span></span> <span data-ttu-id="be24a-133">ใบสั่งที่ถูกระงับอยู่ในขณะนี้มีการทำเครื่องหมายฟิลด์ "ไม่ต้องประมวลผล" และ "ระงับ" อยู่</span><span class="sxs-lookup"><span data-stu-id="be24a-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="be24a-134">บนบานหน้าต่างการดำเนินการ คลิก **เบิกสินค้าและจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="be24a-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="be24a-135">จัดการการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="be24a-135">Manage order holds</span></span>
1. <span data-ttu-id="be24a-136">ไปที่ **การขายและการตลาด > ใบสั่งขาย > ใบสั่งที่เปิด > การระงับใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="be24a-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="be24a-137">หน้า **การระงับใบสั่ง** ทำหน้าที่เป็นเวิร์กเบนซ์ ซึ่งคุณสามารถดูภาพรวมของการระงับปัจจุบันและที่ประมวลผลแล้ว และจัดการการระงับเหล่านั้นและใบสั่งขายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="be24a-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="be24a-138">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be24a-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="be24a-139">ใน **บานหน้าต่างการดำเนินการ** คลิก **เช็คเอาท์การระงับ**</span><span class="sxs-lookup"><span data-stu-id="be24a-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="be24a-140">คลิก **เช็คเอาท์**</span><span class="sxs-lookup"><span data-stu-id="be24a-140">Click **Check out**.</span></span>
5. <span data-ttu-id="be24a-141">ในรายการนี้ ให้ยกเลิกการทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be24a-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="be24a-142">ขณะนี้ฟิลด์ **เช็คเอาท์ไปยัง** จะแสดงรหัสผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="be24a-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="be24a-143">คลิก **ล้างข้อมูลเช็คเอาท์t**</span><span class="sxs-lookup"><span data-stu-id="be24a-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="be24a-144">ใน **บานหน้าต่างการดำเนินการ** คลิก **ล้างข้อมูลการระงับ**</span><span class="sxs-lookup"><span data-stu-id="be24a-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="be24a-145">เมื่อคุณพร้อมที่จะลบการระงับและอนุญาตให้ดำเนินการใบสั่งไปยังขั้นตอนการเติมเต็มถัดไป คุณจะต้องล้างข้อมูลการระงับ</span><span class="sxs-lookup"><span data-stu-id="be24a-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="be24a-146">ถ้าไม่จำเป็นต้องเปลี่ยนแปลงใบสั่ง คุณสามารถรันการดำเนินการล้างข้อมูลการระงับได้</span><span class="sxs-lookup"><span data-stu-id="be24a-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="be24a-147">อย่างไรก็ตาม คุณสามารถใช้การดำเนินการล้างข้อมูลและปรับเปลี่ยนได้ ถ้าจำเป็นต้องอัพเดตใบสั่งเมื่อทำการล้างข้อมูลการระงับ</span><span class="sxs-lookup"><span data-stu-id="be24a-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="be24a-148">การดำเนินการ **ล้างข้อมูลและส่ง** จะใช้ได้เฉพาะเมื่อคุณใช้ฟังก์ชันข้อมูลศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="be24a-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="be24a-149">คลิก **ล้างข้อมูลการระงับ**</span><span class="sxs-lookup"><span data-stu-id="be24a-149">Click **Clear holds**.</span></span> <span data-ttu-id="be24a-150">ขณะนี้การระงับได้ถูกล้างข้อมูลออกจากใบสั่งและลบออกจากรายการการระงับที่ใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="be24a-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="be24a-151">เมื่อต้องการดูการระงับทั้งหมดหรือเซ็ตย่อยของการระงับตามสถานะหนึ่งๆ ให้เปลี่ยนค่าในฟิลด์แสดง</span><span class="sxs-lookup"><span data-stu-id="be24a-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

