--- 
title: "การสร้างบัญชีผู้จัดจำหน่าย"
description: "ขั้นตอนนี้แสดงวิธีการสร้างบัญชีผู้จัดจำหน่าย และเพิ่มอยู่และข้อมูลผู้ติดต่อ "
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 22c7a1a2b7468f00aa25a67a2c5f62b088e2fe7c
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-vendor-account"></a><span data-ttu-id="00339-103">การสร้างบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="00339-103">Create a vendor account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00339-104">ขั้นตอนนี้แสดงวิธีการสร้างบัญชีผู้จัดจำหน่าย และเพิ่มอยู่และข้อมูลผู้ติดต่อ </span><span class="sxs-lookup"><span data-stu-id="00339-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="00339-105">ขั้นตอนจะไม่แสดงวิธีการเติมข้อมูลในฟิลด์ทั้งหมดสำหรับการซื้อ และวัตถุประสงค์ทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="00339-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="00339-106">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับฟิลด์ดังกล่าว โปรดอ่านคำอธิบายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="00339-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="00339-107">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="00339-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="00339-108">บัญชีผู้จัดจำหน่ายโดยทั่วไปจะสร้างขึ้นโดยผู้เชี่ยวชาญด้านการจัดซื้อจัดหาหรือบุคลากรลูกหนี้บัญชี</span><span class="sxs-lookup"><span data-stu-id="00339-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="00339-109">การสร้างบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="00339-109">Create a vendor account</span></span>
1. <span data-ttu-id="00339-110">ไปที่การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="00339-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="00339-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="00339-111">Click New.</span></span>
3. <span data-ttu-id="00339-112">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="00339-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="00339-113">ค่าอาจถูกเติมโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="00339-113">The value may be populated automatically.</span></span> <span data-ttu-id="00339-114">ถ้าเป็นเช่นนั้นคุณสามารถข้ามขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="00339-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="00339-115">คุณสามารถสร้างบัญชีผู้จัดจำหน่ายสำหรับบุคคลหรือองค์กร </span><span class="sxs-lookup"><span data-stu-id="00339-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="00339-116">สิ่งนี้จะกระทบฟิลด์ที่พร้อมใช้งานอยู่ </span><span class="sxs-lookup"><span data-stu-id="00339-116">This will affect which fields are available.</span></span> <span data-ttu-id="00339-117">ในตัวอย่างนี้ เราจะสร้างบัญชีผู้จัดจำหน่ายสำหรับองค์กร</span><span class="sxs-lookup"><span data-stu-id="00339-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="00339-118">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="00339-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="00339-119">ถ้าผู้จัดจำหน่ายของคุณเป็นบุคคลลงทะเบียนไว้ในระบบของคุณอยู่แล้ว คุณสามารถใช้ดร็อปดาวน์และเลือกไว้ในฟิลด์นี้ และบัญชีผู้จัดจำหน่ายใหม่จะรับช่วงข้อมูลที่อยู่และข้อมูลผู้ติดต่อที่ลงทะเบียนไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="00339-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="00339-120">ในฟิลด์กลุ่ม ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="00339-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="00339-121">กลุ่มผู้จัดจำหน่ายถูกใช้เพื่อจัดกลุ่มผู้จัดจำหน่ายที่มีพารามิเตอร์ต่อไปนี้ร่วมกัน: เงื่อนไขการชำระเงิน รอบระยะเวลาชำระ บัญชีแยกประเภทของการลงรายการสินค้าคงคลัง ซึ่งรวมถึงกลุ่มภาษีขาย บัญชีแยกประเภทเริ่มต้น รหัสตัวกรองผลิตภัณฑ์ หรือการตั้งค่าคอนฟิกการคาดการณ์การจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="00339-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="00339-122">ในฟิลด์จำนวนพนักงาน ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="00339-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="00339-123">ในฟิลด์หมายเลของค์กร ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="00339-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="00339-124">เพิ่มที่อยู่</span><span class="sxs-lookup"><span data-stu-id="00339-124">Add an address</span></span>
1. <span data-ttu-id="00339-125">ขยายส่วนที่อยู่</span><span class="sxs-lookup"><span data-stu-id="00339-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="00339-126">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="00339-126">Click Add.</span></span>
3. <span data-ttu-id="00339-127">ในฟิลด์วัตถุประสงค์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="00339-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="00339-128">คุณสามารถเลือกวัตถุประสงค์หนึ่งรายการหรือมากกว่า </span><span class="sxs-lookup"><span data-stu-id="00339-128">You can select one or more purposes.</span></span> <span data-ttu-id="00339-129">ซึ่งจะถูกใช้เพื่อเลือกที่อยู่ที่ถูกต้องสำหรับวัตถุประสงค์ที่กำหนดไว้ </span><span class="sxs-lookup"><span data-stu-id="00339-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="00339-130">ตัวอย่างเช่น ถ้าวัตถุประสงค์คือ "ใบแจ้งหนี้" ซึ่งที่อยู่ที่จะถูกใช้ เมื่อคุณส่งใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="00339-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="00339-131">ในฟิลด์ชื่อหรือคำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="00339-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="00339-132">ในฟิลด์ประเทศ/ภูมิภาค ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="00339-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="00339-133">ป้อนรายละเอียดที่อยู่ </span><span class="sxs-lookup"><span data-stu-id="00339-133">Enter the address details.</span></span> <span data-ttu-id="00339-134">ประเทศ/ภูมิภาคที่คุณเลือกจะกำหนดว่าฟิลด์คุณจะถูกแสดงอยู่ด้วย สอดคล้องกับรูปแบบที่อยู่สำหรับประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="00339-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="00339-135">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="00339-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="00339-136">เพิ่มข้อมูลผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="00339-136">Add contact information</span></span>
1. <span data-ttu-id="00339-137">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="00339-137">Click Add.</span></span>
2. <span data-ttu-id="00339-138">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="00339-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="00339-139">ในฟิลด์ชนิด ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="00339-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="00339-140">ในฟิลด์หมายเลข/ที่อยู่ผู้ติดต่อ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="00339-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="00339-141">คุณสามารถเลือกกล่องกาเครื่องหมายหลักได้ ถ้านี่เป็นผู้ติดต่อหลัก</span><span class="sxs-lookup"><span data-stu-id="00339-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="00339-142">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="00339-142">Click Save.</span></span>
6. <span data-ttu-id="00339-143">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="00339-143">Close the page.</span></span>
7. <span data-ttu-id="00339-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="00339-144">Close the page.</span></span>


