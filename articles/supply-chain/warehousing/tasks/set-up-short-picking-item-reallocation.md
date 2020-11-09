---
title: ตั้งค่าการปันส่วนใหม่ของสินค้าสำหรับการเบิกสินค้าที่ขาด
description: หัวข้อนี้แสดงวิธีการเปิดใช้งานให้ผู้ปฏิบัติงานคลังสินค้าสามารถค้นหาสถานที่สำรองได้อย่างรวดเร็ว ถ้ามีสินค้าคงคลังไม่เพียงพอที่สถานที่ที่พวกเขาได้รับการสั่งการให้ไป
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8f5c23f82e96145f411ec993f766a90137b5b8
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015975"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="def5e-103">ตั้งค่าการปันส่วนใหม่ของสินค้าสำหรับการเบิกสินค้าที่ขาด</span><span class="sxs-lookup"><span data-stu-id="def5e-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="def5e-104">กระบวนงานนี้แสดงวิธีการเปิดใช้งานให้ผู้ปฏิบัติงานคลังสินค้าสามารถค้นหาสถานที่สำรองได้อย่างรวดเร็ว ถ้ามีสินค้าคงคลังไม่เพียงพอที่สถานที่ที่พวกเขาได้รับการสั่งการให้ไป</span><span class="sxs-lookup"><span data-stu-id="def5e-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="def5e-105">กระบวนการปันส่วนใหม่จะถูกควบคุมโดย **ข้อยกเว้นของงาน** และใช้โดย **ผู้ปฏิบัติงาน** คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="def5e-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="def5e-106">คุณสามารถใช้กระบวนการปันส่วนใหม่แบบอัตโนมัติ ด้วยตนเอง หรือทั้งสองกระบวนการ:</span><span class="sxs-lookup"><span data-stu-id="def5e-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="def5e-107">การปันส่วนใหม่แบบอัตโนมัติ - คำสั่งสถานที่ถูกใช้เพื่อกำหนดว่าสินค้าพร้อมใช้งานที่สถานที่อื่นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="def5e-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="def5e-108">ถ้าเป็นไปได้ จะมีการปรับปรุงงานและผู้ใช้คลังสินค้าจะถูกสั่งการไปยังสถานที่อื่น</span><span class="sxs-lookup"><span data-stu-id="def5e-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="def5e-109">การปันส่วนด้วยตนเอง - อนุญาตให้ผู้ใช้คลังสินค้าสามารถเลือกจากสถานที่หนึ่งแห่งขึ้นไปที่มีปริมาณของสินค้าที่ไม่ได้จอง</span><span class="sxs-lookup"><span data-stu-id="def5e-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="def5e-110">แบบอัตโนมัติและด้วยตนเอง - ถ้าระบบไม่สามารถดำเนินการปันส่วนใหม่แบบอัตโนมัติ และสถานที่พร้อมใช้งานโดยมีปริมาณที่ไม่ได้จอง ผู้ใช้จะได้รับการแจ้งเตือนให้เลือกสถานที่</span><span class="sxs-lookup"><span data-stu-id="def5e-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="def5e-111">ตั้งค่าข้อยกเว้นของงาน</span><span class="sxs-lookup"><span data-stu-id="def5e-111">Set up work exceptions</span></span>
<span data-ttu-id="def5e-112">สามารถกำหนดข้อยกเว้นของงานต่างๆ ด้วยนโยบายการปันส่วนใหม่ของสินค้าที่แตกต่างกัน เพื่อให้ผู้ปฏิบัติงานคลังสินค้าสามารถเลือกได้ตามความจำเป็นในการจัดส่งสินค้าที่กำลังประมวลผลอยู่</span><span class="sxs-lookup"><span data-stu-id="def5e-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="def5e-113">บริษัทข้อมูลสาธิต USMF ถูกนำมาใช้ในการสร้างกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="def5e-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="def5e-114">ใน **บานหน้าต่างนำทาง** ไปที่ **การจัดการคลังสินค้า > การตั้งค่า > งาน > ข้อยกเว้นของงาน**</span><span class="sxs-lookup"><span data-stu-id="def5e-114">In the **Navigation pane** , go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="def5e-115">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="def5e-115">Click **New**</span></span> 
3. <span data-ttu-id="def5e-116">ในฟิลด์ **รหัสข้อยกเว้นของงาน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="def5e-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="def5e-117">นี่จะเป็นชื่อเรื่องของข้อยกเว้นนี้</span><span class="sxs-lookup"><span data-stu-id="def5e-117">This will be the title of this exception .</span></span> <span data-ttu-id="def5e-118">ตัวอย่างเช่น การเบิกสินค้าที่ขาดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="def5e-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="def5e-119">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="def5e-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="def5e-120">นี่จะเป็นคำอธิบายโดยย่อของการใช้งานข้อยกเว้นนี้</span><span class="sxs-lookup"><span data-stu-id="def5e-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="def5e-121">ตัวอย่างเช่น การเบิกสินค้าที่ขาด - สินค้าไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="def5e-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="def5e-122">ในฟิลด์ชนิด **ข้อยกเว้น** เลือก **การเบิกสินค้าที่ขาด**</span><span class="sxs-lookup"><span data-stu-id="def5e-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="def5e-123">เลือกกล่องกาเครื่องหมาย **ปรับปรุงสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="def5e-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="def5e-124">ถ้ามีการเลือก สินค้าคงคลังจะถูกปรับปรุงเป็น 0 ที่สถานที่ที่มีการเบิกสินค้าที่ขาด</span><span class="sxs-lookup"><span data-stu-id="def5e-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="def5e-125">ในฟิลด์ **รหัสชนิดการปรับปรุงค่าเริ่มต้น** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="def5e-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="def5e-126">ตัวอย่างเช่น ใน USMF คุณสามารถเลือก **Remove Res Adj Out** รหัสชนิดการปรับปรุงแต่ละรหัสมีลักษณะสี่อย่าง ได้แก่ ชื่อ คำอธิบาย ชื่อสมุดรายวันสินค้าคงคลัง และ **ลบการจอง**</span><span class="sxs-lookup"><span data-stu-id="def5e-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="def5e-127">ถ้า **ลบการจอง** ถูกเปิดใช้งาน การจองของรายการใบสั่งที่มีการเบิกสินค้าที่ขาดจะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="def5e-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="def5e-128">ในฟิลด์ **การปันส่วนสินค้าใหม่** เลือกค่า เช่น ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="def5e-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="def5e-129">ถ้าคุณเลือก ด้วยตนเอง หรือ โดยอัตโนมัติและด้วยตนเอง จะต้องอนุญาตให้ผู้ปฏิบัติงานคลังสินค้าสามารถใช้การปันส่วนด้วยตนเองใหม่</span><span class="sxs-lookup"><span data-stu-id="def5e-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="def5e-130">ตั้งค่าผู้ปฏิบัติงานที่จะใช้การปันส่วนสินค้าด้วยตนเองใหม่</span><span class="sxs-lookup"><span data-stu-id="def5e-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="def5e-131">บริษัทข้อมูลสาธิต USMF ถูกนำมาใช้ในการสร้างกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="def5e-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="def5e-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="def5e-132">Close the page.</span></span>
2. <span data-ttu-id="def5e-133">ใน **บานหน้าต่างนำทาง** ไปที่ **การจัดการคลังสินค้า > การตั้งค่า > งาน > ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="def5e-133">In the **Navigation pane** , go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="def5e-134">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="def5e-134">Click **Edit**.</span></span>
4. <span data-ttu-id="def5e-135">ในรายการนี้ ให้เลือกผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="def5e-135">In the list, select worker.</span></span> <span data-ttu-id="def5e-136">ตัวอย่างเช่น Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="def5e-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="def5e-137">ขยาย FastTab **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="def5e-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="def5e-138">ในรายการ เลือก **รหัสผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="def5e-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="def5e-139">ตัวอย่างเช่น 24</span><span class="sxs-lookup"><span data-stu-id="def5e-139">For example, 24.</span></span>
7. <span data-ttu-id="def5e-140">ขยาย FastTab **งาน**</span><span class="sxs-lookup"><span data-stu-id="def5e-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="def5e-141">เลือก **ใช่** ในฟิลด์ **อนุญาตการปันส่วนสินค้าด้วยตนเองใหม่**</span><span class="sxs-lookup"><span data-stu-id="def5e-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
