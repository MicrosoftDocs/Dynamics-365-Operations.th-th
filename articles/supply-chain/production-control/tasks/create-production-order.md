---
title: สร้างใบสั่งผลิต
description: 'กระบวนงานนี้แสดงวิธีการสร้างใบสั่งผลิต '
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dec447302da3a3bbca7d9c3e783af54bc77dfe70
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259829"
---
# <a name="create-a-production-order"></a><span data-ttu-id="eea15-103">สร้างใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-103">Create a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eea15-104">กระบวนงานนี้แสดงวิธีการสร้างใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="eea15-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="eea15-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="eea15-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="eea15-106">นี่เป็นกระบวนงานแรกจากเจ็ดกระบวนงานซึ่งอธิบายวงจรชีวิตของใบสั่งการผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="eea15-107">สร้างใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-107">Create a production order</span></span>
1. <span data-ttu-id="eea15-108">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="eea15-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="eea15-109">คลิกใบสั่งผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="eea15-109">Click New production order.</span></span>
3. <span data-ttu-id="eea15-110">ในฟิลด์ หมายเลขสินค้า ให้พิมพ์ 'D0001'</span><span class="sxs-lookup"><span data-stu-id="eea15-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="eea15-111">ในฟิลด์การจัดส่ง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="eea15-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="eea15-112">วันที่จัดส่งบ่งชี้เวลาที่ใบสั่งผลิตควรสิ้นสุดเพื่อจะได้จัดส่งตรงเวลา </span><span class="sxs-lookup"><span data-stu-id="eea15-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="eea15-113">วันที่นี้สามารถใช้ในกระบวนการจัดกำหนดการได้ </span><span class="sxs-lookup"><span data-stu-id="eea15-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="eea15-114">ตัวอย่างเช่น คุณสามารถจัดกำหนดการใบสั่งย้อนหลังจากวันจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="eea15-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="eea15-115">กำหนดปริมาณเป็น '20'</span><span class="sxs-lookup"><span data-stu-id="eea15-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="eea15-116">หมายเหตุ: ฟิลด์หมายเลข BOM จะแสดงหมายเลขของ BOM ที่ใช้งานอยู่ใดๆสำหรับสินค้าปัจจุบันโดยอัตโนมัติ แต่คุณสามารถเปลี่ยน BOM สำหรับใบสั่งผลิตโดยการเลือก BOM ที่ใช้งานอยู่จากรายการของเวอร์ชัน BOM ที่อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="eea15-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="eea15-117">ฟิลด์หมายเลขกระบวนการผลิตแสดงหมายเลขของกระบวนการผลิตที่ใช้งานอยู่ใดๆ สำหรับสินค้าปัจจุบันโดยอัตโนมัติ แต่คุณสามารถเปลี่ยนกระบวนการผลิตสำหรับใบสั่งผลิตได้ โดยการเลือกกระบวนการผลิตที่ใช้งานอยู่จากรายการของเวอร์ชันกระบวนการผลิตที่อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="eea15-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="eea15-118">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="eea15-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="eea15-119">ตรวจสอบใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-119">Validate the production order</span></span>
1. <span data-ttu-id="eea15-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="eea15-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="eea15-121">คลิกลิงค์สำหรับหมายเลขใบสั่งผลิตที่คุณเพิ่งสร้าง </span><span class="sxs-lookup"><span data-stu-id="eea15-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="eea15-122">ซึ่งจะเปิดหน้ารายละเอียดสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="eea15-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="eea15-123">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="eea15-123">Click Edit.</span></span>
3. <span data-ttu-id="eea15-124">ในฟิลด์การจัดส่ง ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="eea15-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="eea15-125">ตัวอย่างเช่น คุณสามารถเปลี่ยนวันที่จัดส่งสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="eea15-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="eea15-126">Click Save.</span></span>
5. <span data-ttu-id="eea15-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="eea15-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="eea15-128">อัพเดต BOM</span><span class="sxs-lookup"><span data-stu-id="eea15-128">Update the BOM</span></span>
1. <span data-ttu-id="eea15-129">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="eea15-130">คลิก BOM</span><span class="sxs-lookup"><span data-stu-id="eea15-130">Click BOM.</span></span>
    * <span data-ttu-id="eea15-131">เปิดหน้า BOM เพื่อตรวจสอบข้อมูล BOM ที่ถูกคัดลอกจากข้อมูลเริ่มต้นเมื่อมีการสร้างใบสั่งผลิต </span><span class="sxs-lookup"><span data-stu-id="eea15-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="eea15-132">ในกระบวนงานนี้ คุณต้องอัพเดตปริมาณสำหรับ BOM</span><span class="sxs-lookup"><span data-stu-id="eea15-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="eea15-133">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="eea15-133">Click Edit.</span></span>
4. <span data-ttu-id="eea15-134">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="eea15-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="eea15-135">การเปลี่ยนแปลงปริมาณในรายการ BOM มีผลกระทบต่อการประเมินต้นทุนของปริมาณการใช้วัสดุสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="eea15-136">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="eea15-136">Click Save.</span></span>
6. <span data-ttu-id="eea15-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="eea15-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="eea15-138">อัพเดตกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-138">Update the production route</span></span>
1. <span data-ttu-id="eea15-139">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="eea15-140">คลิกกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-140">Click Route.</span></span>
    * <span data-ttu-id="eea15-141">เปิดหน้ากระบวนการผลิตเพื่อตรวจสอบข้อมูลของกระบวนการผลิตที่มีการคัดลอกมาจากข้อมูลเริ่มต้นเมื่อสร้างใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="eea15-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="eea15-142">ในกระบวนงานนี้ คุณต้องอัพเดตปริมาณสำหรับการดำเนินงานในกระบวนการผลิตอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="eea15-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="eea15-143">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="eea15-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="eea15-144">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="eea15-144">Click Edit.</span></span>
5. <span data-ttu-id="eea15-145">ในฟิลด์ปริมาณกระบวนการ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="eea15-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="eea15-146">การเปลี่ยนเวลาการประมวลผลที่ส่งผลต่อปริมาณการใช้วัสดุของกระบวนการผลิตที่ประเมินได้และต้นทุนของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="eea15-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="eea15-147">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="eea15-147">Click Save.</span></span>
7. <span data-ttu-id="eea15-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="eea15-148">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]