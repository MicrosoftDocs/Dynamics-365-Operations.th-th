---
title: " กำหนดการความต่อเนื่อง"
description: 'หัวข้อนี้แนะนำเกี่ยวกับการตั้งค่าโปรแกรมความต่อเนื่อง (หรือเรียกว่าใบสั่งที่เกิดซ้ำ) '
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8414377ddec0e001f003f842866725eb58bd75a3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791618"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="bc2c0-103"> กำหนดการความต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="bc2c0-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc2c0-104">หัวข้อนี้แนะนำเกี่ยวกับการตั้งค่าโปรแกรมความต่อเนื่อง (หรือเรียกว่าใบสั่งที่เกิดซ้ำ) </span><span class="sxs-lookup"><span data-stu-id="bc2c0-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="bc2c0-105">หัวข้อนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="bc2c0-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="bc2c0-106">สร้างโปรแกรมความต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="bc2c0-106">Create continuity program</span></span>
1. <span data-ttu-id="bc2c0-107">ไปยัง การขายปลีกและการค้า > ความต่อเนื่อง > โปรแกรมต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="bc2c0-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="bc2c0-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="bc2c0-108">Click New.</span></span>
3. <span data-ttu-id="bc2c0-109">ในฟิลด์รหัสกำหนดการ พิมพ์รหัสกำหนดการความต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="bc2c0-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="bc2c0-110">ในฟิลด์การเริ่มต้นใบสั่ง ให้เลือก 'เหตุการณ์แรก'</span><span class="sxs-lookup"><span data-stu-id="bc2c0-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="bc2c0-111">ถ้าลูกค้าวางใบสั่งใหม่สำหรับโปรแกรมความต่อเนื่อง จะมีสองตัวเลือกสำหรับการจัดส่งผลิตภัณฑ์:  1.</span><span class="sxs-lookup"><span data-stu-id="bc2c0-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="bc2c0-112">เหตุการณ์แรก: ผลิตภัณฑ์แรกในโปรแกรมความต่อเนื่องจะถูกจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="bc2c0-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="bc2c0-113">2</span><span class="sxs-lookup"><span data-stu-id="bc2c0-113">2.</span></span> <span data-ttu-id="bc2c0-114">เหตุการณ์ปัจจุบัน: จะถูกจัดส่งผลิตภัณฑ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bc2c0-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="bc2c0-115">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="bc2c0-115">For example.</span></span> <span data-ttu-id="bc2c0-116">เมื่ออยู่ในโปรแกรมสามเดือนแล้ว ลูกค้าจะได้รับลำดับที่สามในโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="bc2c0-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="bc2c0-117">เลือก 'ใช่' เพื่อแสดงกล่องโต้ตอบสำหรับใบสั่งวันที่เริ่มต้นใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="bc2c0-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="bc2c0-118">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="bc2c0-118">Click Add line.</span></span>
7. <span data-ttu-id="bc2c0-119">ในฟิลด์หมายเลขสินค้า ให้ป้อนหมายเลขสินค้าสำหรับผลิตภัณฑ์แรก ('0013')</span><span class="sxs-lookup"><span data-stu-id="bc2c0-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="bc2c0-120">พิมพ์ 'CP'</span><span class="sxs-lookup"><span data-stu-id="bc2c0-120">Type 'CP'.</span></span>
9. <span data-ttu-id="bc2c0-121">ป้อนวันที่ที่ผลิตภัณฑ์แรกจะพร้อมใช้งานสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="bc2c0-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="bc2c0-122">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="bc2c0-122">Click Add line.</span></span>
11. <span data-ttu-id="bc2c0-123">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ '0014'</span><span class="sxs-lookup"><span data-stu-id="bc2c0-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="bc2c0-124">ในฟิลด์รหัสช่วงวันที่ ให้ล้างค่าเพื่อให้ฟิลด์ว่าง</span><span class="sxs-lookup"><span data-stu-id="bc2c0-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="bc2c0-125">สำหรับกระบวนงานนี้ ให้ยกเลิกช่วงวันที่ </span><span class="sxs-lookup"><span data-stu-id="bc2c0-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="bc2c0-126">คุณสามารถกำหนดวันที่เป็นส่วนเพิ่มจากวันที่เริ่มต้นของรายการแรกได้</span><span class="sxs-lookup"><span data-stu-id="bc2c0-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="bc2c0-127">ที่นี่คุณจะป้อนช่วงเวลาที่ผลิตภัณฑ์มีการจัดส่ง </span><span class="sxs-lookup"><span data-stu-id="bc2c0-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="bc2c0-128">พิมพ์ '30'</span><span class="sxs-lookup"><span data-stu-id="bc2c0-128">Type '30'.</span></span>
    * <span data-ttu-id="bc2c0-129">สำหรับโปรแกรมรายเดือน คุณจะป้อน 30 วันสำหรับช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="bc2c0-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="bc2c0-130">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="bc2c0-130">Click Add line.</span></span>
15. <span data-ttu-id="bc2c0-131">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ '0015'</span><span class="sxs-lookup"><span data-stu-id="bc2c0-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="bc2c0-132">พิมพ์ 'สิ้นสุด'</span><span class="sxs-lookup"><span data-stu-id="bc2c0-132">Type 'End'.</span></span>
17. <span data-ttu-id="bc2c0-133">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bc2c0-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="bc2c0-134">กำหนดให้กับสินค้าที่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="bc2c0-134">Assign to continuity item</span></span>
1. <span data-ttu-id="bc2c0-135">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="bc2c0-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="bc2c0-136">เลือกสินค้า '0016'</span><span class="sxs-lookup"><span data-stu-id="bc2c0-136">Select item '0016'.</span></span>
    * <span data-ttu-id="bc2c0-137">สำหรับกระบวนงานนี้ คุณจะเลือกหมายเลขสินค้า 0016</span><span class="sxs-lookup"><span data-stu-id="bc2c0-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="bc2c0-138">โดยปกติแล้ว คุณจะสร้างผลิตภัณฑ์ที่นำออกใช้ที่มีตรรกะทางธุรกิจความต่อเนื่องเพิ่มเติมที่ใช้เมื่อมีการวางในใบสั่งขายในศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="bc2c0-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="bc2c0-139">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bc2c0-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bc2c0-140">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="bc2c0-140">Click Edit.</span></span>
5. <span data-ttu-id="bc2c0-141">ขยายหรือยุบส่วนขาย</span><span class="sxs-lookup"><span data-stu-id="bc2c0-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="bc2c0-142">ที่นี่คุณจะป้อนโปรแกรมความต่อเนื่องที่แสดงโดยสินค้านี้ </span><span class="sxs-lookup"><span data-stu-id="bc2c0-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="bc2c0-143">พิมพ์รหัสกำหนดการที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="bc2c0-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="bc2c0-144">เมื่อมีการขายสินค้านี้ในศูนย์บริการ ตรรกะทางธุรกิจเพิ่มเติมจะถูกนำไปใช้จากโปรแกรมความต่อเนื่องที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bc2c0-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="bc2c0-145">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bc2c0-145">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]