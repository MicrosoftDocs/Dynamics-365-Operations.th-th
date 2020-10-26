---
title: การลงทะเบียนการรับสินค้าที่ส่งคืน
description: คุณสามารถลงทะเบียนการรับสินค้าที่ส่งคืนได้โดยใช้แบบฟอร์มภาพรวมของการมาถึง หรือแบบฟอร์มการลงทะเบียน
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42ca1d4d2d9b45d79cf479833f83e498e3b73540
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975643"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="d5208-103">การลงทะเบียนการรับสินค้าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="d5208-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d5208-104">มีวิธีสำหรับการลงทะเบียนการรับสินค้าที่ส่งคืนอยู่สองวิธี</span><span class="sxs-lookup"><span data-stu-id="d5208-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="d5208-105">วิธีการแรกคือ กระบวนการที่ใช้ในการรับคลังสินค้าที่ใช้แบบฟอร์ม **ภาพรวมการมาถึง**</span><span class="sxs-lookup"><span data-stu-id="d5208-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="d5208-106">วิธีการที่สองใช้แบบฟอร์ม **การลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="d5208-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="d5208-107">ลงทะเบียนการรับสินค้าที่ส่งคืนในแบบฟอร์มภาพรวมของการมาถึง</span><span class="sxs-lookup"><span data-stu-id="d5208-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="d5208-108">คุณสามารถใช้แบบฟอร์ม **ภาพรวมการมาถึง** เพื่อระบุการจัดส่งคืนได้โดยหมายเลขอนุมัติการคืนสินค้า (RMA)</span><span class="sxs-lookup"><span data-stu-id="d5208-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="d5208-109">ถ้าชื่อสมุดรายวันถูกกำหนดในแท็บ **ตั้งค่า** และมีรายการสมุดรายวันที่สอดคล้องกับรายการที่เลือกไว้ในแบบฟอร์ม **ภาพรวมการมาถึง** อยู่ จะมีการสร้างส่วนหัวของสมุดรายวัน เมื่อคุณคลิก **เริ่มต้นการมาถึง**</span><span class="sxs-lookup"><span data-stu-id="d5208-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="d5208-110">คลิก **การบริหารสินค้าคงคลัง** \> **งานประจำงวด** \> **ภาพรวมของการมาถึง**</span><span class="sxs-lookup"><span data-stu-id="d5208-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="d5208-111">ในฟิลด์ **ชื่อการตั้งค่า** เลือก **ใบสั่งส่งคืน** แล้วคลิก **การอัพเดต**</span><span class="sxs-lookup"><span data-stu-id="d5208-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="d5208-112">คุณสามารถใช้ฟิลด์ <STRONG>ช่วง</STRONG> เพื่อจำกัดผลการค้นหาให้แคบลงได้</span><span class="sxs-lookup"><span data-stu-id="d5208-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="d5208-113">คุณสามารถพิมพ์หรือเลือกหมายเลข RMA ในฟิลด์ <STRONG>หมายเลข RMA</STRONG> ได้ เพื่อให้ได้ผลลัพธ์ที่แม่นยำ</span><span class="sxs-lookup"><span data-stu-id="d5208-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="d5208-114">เพื่อกำหนดและบันทึกชุดของตัวกรองข้อมูลที่จะจำกัดการมาถึงในอนาคตที่จะถูกแสดง คลิกแท็บ <STRONG>ตั้งค่า</STRONG> ตัวกรองข้อมูลที่พร้อมใช้งานประกอบด้วย ชนิด คลังสินค้า และนาฬิกา</span><span class="sxs-lookup"><span data-stu-id="d5208-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="d5208-115">ไม่สามารถผสมใบสั่งส่งคืนสินค้ากับชนิดการมาถึงอื่นได้ในแบบฟอร์ม <STRONG>ภาพรวมการมาถึง</STRONG></span><span class="sxs-lookup"><span data-stu-id="d5208-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="d5208-116">ดังนั้น การอ้างอิงจะรวมใบสั่งขายเสมอ แต่ไม่มีการระบุรหัสใบสั่งขายในส่วนหัวของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="d5208-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="d5208-117">ในกริด **การรับสินค้า** ให้ค้นหารายการที่ตรงกับสินค้าที่จะถูกส่งคืน แล้วเลือกกล่องกาเครื่องหมายในคอลัมน์ **เลือกสำหรับการมาถึง**</span><span class="sxs-lookup"><span data-stu-id="d5208-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="d5208-118">ถ้าคุณต้องการแยกรายการบางรายการออกจากการรับสินค้าที่ส่งคืน เช่น สินค้าจากใบสั่งต้นฉบับที่ไม่ได้ถูกรวมไว้ในการจัดส่งคืน ให้ยกเลิกการเลือกกล่องกาเครื่องหมาย **เลือกสำหรับการมาถึง** ในตาราง **รายการ** ในส่วนด้านล่างของแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="d5208-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="d5208-119">คลิกปุ่ม **เริ่มต้นการมาถึง** เพื่อสร้างสมุดรายวันการมาถึง</span><span class="sxs-lookup"><span data-stu-id="d5208-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="d5208-120">คุณสามารถเลือกใบสั่งส่งคืนสินค้าได้หลายใบ และรวมใบสั่งที่เลือกทั้งหมดไว้ในกระบวนการมาถึงเพียงกระบวนการเดียว </span><span class="sxs-lookup"><span data-stu-id="d5208-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="d5208-121">ระบบจะคัดลอกบรรทัดใบสั่งส่งคืนสินค้าแต่ละบรรทัดเข้าไปในบรรทัดสมุดรายวันการมาถึงของสินค้าที่สอดคล้องกัน </span><span class="sxs-lookup"><span data-stu-id="d5208-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="d5208-122">นอกจากนี้ คุณยังสามารถสร้างสมุดรายวันการมาถึงได้ด้วยตนเองโดยใช้แบบฟอร์ม <STRONG>การมาถึงของสินค้า</STRONG></span><span class="sxs-lookup"><span data-stu-id="d5208-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="d5208-123">คลิก **การบริหารสินค้าคงคลัง** \> **สมุดรายวัน** \> **การมาถึงของสินค้า** \> **การมาถึงของสินค้า**</span><span class="sxs-lookup"><span data-stu-id="d5208-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="d5208-124">เลือกสมุดรายวันการมาถึงที่คุณเพิ่งสร้าง จากนั้นคลิก **รายการ** เพื่อเปิดแบบฟอร์ม **รายการสมุดรายวัน, สถานที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="d5208-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="d5208-125">ในแท็บ **ทั่วไป** ให้ปรับปรุงหมายเลขในฟิลด์ **ปริมาณ** ถ้าจำเป็น และจากนั้นให้กำหนดรหัสการโอนการครอบครองในฟิลด์ **รหัสการโอนการครอบครอง**</span><span class="sxs-lookup"><span data-stu-id="d5208-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="d5208-126">อีกวิธีหนึ่งคือ คุณสามารถเลือกกล่องกาเครื่องหมาย **การบริหารการตรวจสอบสินค้า** เพื่อส่งสินค้าที่ส่งคืนผ่านทางกระบวนการตรวจสอบในบริบทของใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="d5208-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="d5208-127">ถ้าคุณส่งสินค้าที่ส่งคืนผ่านการตรวจสอบสินค้า คุณจะไม่สามารถระบุรหัสการโอนการครอบครอง</span><span class="sxs-lookup"><span data-stu-id="d5208-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="d5208-128">คลิกปุ่ม **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="d5208-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="d5208-129">ถ้าไม่มีข้อผิดพลาดในกระบวนการตรวจสอบความถูกต้อง ให้คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="d5208-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="d5208-130">ลงทะเบียนการรับสินค้าที่ส่งคืนในแบบฟอร์มการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="d5208-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="d5208-131">ในฐานะที่เป็นทางเลือกในการใช้แบบฟอร์ม **ภาพรวมการมาถึง** คุณสามารถใช้แบบฟอร์ม **การลงทะเบียน** เพื่อลงทะเบียนการมาถึงของสินค้าที่ส่งคืนได้</span><span class="sxs-lookup"><span data-stu-id="d5208-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="d5208-132">คลิก **การขายและการตลาด** \> **ทั่วไป** \> **ใบสั่งส่งคืนสินค้า** \> **ใบสั่งส่งคืนสินค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d5208-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="d5208-133">สร้างใบสั่งส่งคืนสินค้าใหม่ หรือเปิดใบสั่งส่งคืนสินค้าจากรายการ</span><span class="sxs-lookup"><span data-stu-id="d5208-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="d5208-134">บน FastTab **รายการ** ให้เลือกรายการใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="d5208-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="d5208-135">คลิก **อัพเดตรายการ** และจากนั้นคลิก **การลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="d5208-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="d5208-136">กำหนดรหัสการโอนการครอบครองในฟิลด์ **รหัสการโอนการครอบครอง** และจากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d5208-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="d5208-137">คุณไม่สามารถส่งสินค้าสำหรับการตรวจสอบเป็นใบสั่งตรวจสอบสินค้าโดยใช้แบบฟอร์ม <STRONG>การลงทะเบียน</STRONG> ได้</span><span class="sxs-lookup"><span data-stu-id="d5208-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="d5208-138">ในกริด **ธุรกรรม** ให้เลือกธุรกรรมที่จะลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="d5208-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="d5208-139">ในกริด **ลงทะเบียนทันที** คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="d5208-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="d5208-140">ทำซ้ำสองขั้นตอนก่อนหน้านี้ จนกว่าสินค้าที่ส่งคืนทั้งหมดจะปรากฏในกริด **ลงทะเบียนทันที**</span><span class="sxs-lookup"><span data-stu-id="d5208-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="d5208-141">คลิก **ลงรายการบัญชีทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d5208-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5208-142">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="d5208-142">See also</span></span>

<span data-ttu-id="d5208-143">[ภาพรวมการมาถึง (แบบฟอร์ม)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="d5208-143">[Arrival overview (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span></span>

  


