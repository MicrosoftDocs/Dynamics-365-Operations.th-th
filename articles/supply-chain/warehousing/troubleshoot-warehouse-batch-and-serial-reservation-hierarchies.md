---
title: การแก้ไขปัญหาเกี่ยวกับชุดงานคลังสินค้าและลำดับชั้นการจองหมายเลขลำดับประจำสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการจองในลำดับชั้นการจองที่ใช่มิติชุดงานหรือหมายเลขลำดับประจำสินค้า
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022557"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="0e7b6-103">การแก้ไขปัญหาเกี่ยวกับชุดงานคลังสินค้าและลำดับชั้นการจองหมายเลขลำดับประจำสินค้า</span><span class="sxs-lookup"><span data-stu-id="0e7b6-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e7b6-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการจองในลำดับชั้นการจองที่ใช่มิติชุดงานหรือหมายเลขลำดับประจำสินค้า</span><span class="sxs-lookup"><span data-stu-id="0e7b6-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="0e7b6-105">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [นโยบายการจองในมิติระดับคลังสินค้าที่ยืดหยุ่น](flexible-warehouse-level-dimension-reservation.md)</span><span class="sxs-lookup"><span data-stu-id="0e7b6-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="0e7b6-106">ลำดับชั้นการจองของสินค้าระบุความต้องการของมิติการจัดเก็บที่ต้องเติมเต็มเพื่อกำหนดที่ตั้งให้กับใบสั่งความตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="0e7b6-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="0e7b6-107">คุณสามารถอธิบายมิติเหล่านี้เป็น *มิติเหนือสถานที่* ได้ เนื่องจากมิติทั้งหมดที่ต้องเติมสินค้าก่อนที่จะมีการมอบหมายสถานที่และ *มิติที่อยู่ต่ำกว่าที่ตั้ง* ซึ่งสามารถปันส่วนได้หลังจากมีการมอบหมายสถานที่ให้กับใบสั่งความต้องการแล้ว</span><span class="sxs-lookup"><span data-stu-id="0e7b6-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="0e7b6-108">ลำระดับชั้นการจองเหล่านี้เรียกอีกอย่างว่า ลำดับชั้นการจอง *เหนือชุดงาน* และ *ต่ำกว่าชุดงาน* หรือ *เหนือหมายเลขลำดับประจำสินค้า* และ *ต่ำกว่าหมายเลขลำดับประจำสินค้า*</span><span class="sxs-lookup"><span data-stu-id="0e7b6-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="0e7b6-109">สินค้าคงคลังสามารถปันส่วนเสร็จเรียบร้อย เฉพาะเมื่อไม่มีช่องว่างในมิติเหนือสถานที่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0e7b6-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="0e7b6-110">ตัวอย่างเช่น ในลำดับชั้นการจอง *เหนือชุดงาน* คุณคาดหวังให้ต้องระบุมิติ **ไซต์** **คลังสินค้า** และ **หมายเลขชุดงาน** บนใบสั่งตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="0e7b6-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="0e7b6-111">หากมิติใด ๆ ดังกล่าวขาดหายไป กระบวนการปันส่วนจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="0e7b6-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="0e7b6-112">ในทางกลับกัน ลำดับชั้นการจอง *ต่ำกว่าชุดงาน* หรือ *ต่ำกว่าหมายเลขลำดับประจำสินค้า* หมายเลขลำดับประจำสินค้าหรือชุดงานอาจมีการระบุบนใบสั่งความต้องการ แต่กระบวนการปันส่วนไม่ต้องการหมายเลขดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="0e7b6-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="0e7b6-113">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "หากต้องการให้กำหนดให้กับเวฟ บรรทัดการโหลดต้องระบุมิติเหนือสถานที่</span><span class="sxs-lookup"><span data-stu-id="0e7b6-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="0e7b6-114">ถ้าต้องการกำหนดมิติเหล่านี้ ให้จองและสร้างรายการจำนวนงานในศูนย์การผลิตใหม่"</span><span class="sxs-lookup"><span data-stu-id="0e7b6-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0e7b6-115">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="0e7b6-115">Issue description</span></span>

<span data-ttu-id="0e7b6-116">เมื่อคุณใช้สินค้าที่มีลำดับชั้นการจอง *เหนือชุดงาน* คำสั่ง **นำออกใช้ไปยังคลังสินค้า** บนหน้า **เวิร์กเบนช์การวางแผนการบรรทุก** สำหรับปริมาณบางส่วนไม่ทำงาน หากคุณพยายามนำโหลดออกใช้</span><span class="sxs-lookup"><span data-stu-id="0e7b6-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="0e7b6-117">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้และไม่มีการสร้างงานสำหรับปริมาณบางส่วน</span><span class="sxs-lookup"><span data-stu-id="0e7b6-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="0e7b6-118">อย่างไรก็ตาม เมื่อคุณใช้สินค้าที่มีลำดับชั้นการจอง *ต่ำกว่าชุดงาน* คุณสามารถนำโหลดออกใช้ได้สำหรับปริมาณบางส่วนจากหน้า **เวิร์กเบนช์การวางแผน**</span><span class="sxs-lookup"><span data-stu-id="0e7b6-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="0e7b6-119">สาเหตุปัญหา</span><span class="sxs-lookup"><span data-stu-id="0e7b6-119">Issue cause</span></span>

<span data-ttu-id="0e7b6-120">เมื่อมิติที่อยู่ด้านบนของมิติ **สถานที่** ในลำดับชั้นการจอง ต้องระบุก่อนการนำออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0e7b6-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="0e7b6-121">ไม่สามารถปล่อยปริมาณบางส่วนได้ ถ้าไม่ได้ระบุอย่างน้อยหนึ่งมิติข้างบน **สถานที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="0e7b6-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="0e7b6-122">พร้อมต์การจองอัตโนมัติที่จะทริกเกอร์หมายเลขชุดงาน แม้ว่าจะมีสินค้าคงคลังที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0e7b6-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0e7b6-123">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="0e7b6-123">Issue description</span></span>

<span data-ttu-id="0e7b6-124">เมื่อคุณใช้สินค้าที่มีลำดับชั้นการจองแบบ *เหนือชุดงาน* ในคลังสินค้าซึ่งยังไม่ได้เปิดใช้งานกระบวนการคลังสินค้า และการจองสินค้าโดยอัตโนมัติจะเปิดใช้งาน พร้อมต์การจองสินค้าอัตโนมัติเพื่อให้มีหมายเลขชุดงานแสดงขึ้น แม้ว่าจะมีชุดงานเพียงชุดเดียวที่สามารถเบิกสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="0e7b6-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="0e7b6-125">อย่างไรก็ตาม เมื่อคุณใช้สินค้าเดียวกันในคลังสินค้าที่มีการเปิดใช้งานกระบวนการคลังสินค้า พร้อมต์การจองอัตโนมัติจะไม่แสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="0e7b6-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="0e7b6-126">สาเหตุปัญหา</span><span class="sxs-lookup"><span data-stu-id="0e7b6-126">Issue cause</span></span>

<span data-ttu-id="0e7b6-127">ถ้าลระดับชั้นการจองถูกกําหนดเป็น *เหนือชุดงาน* หรือ *เหนือหมายเลขลำดับประจำสินค้า* ต้องระบุมิติที่อ้างอิง (**หมายเลขชุดงาน** หรือ **หมายเลขลำดับประจำสินค้า**) เสมอบนใบสั่งความต้องการ</span><span class="sxs-lookup"><span data-stu-id="0e7b6-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="0e7b6-128">กระบวนการของคลังสินค้าอาจสามารถกรอกข้อมูลได้หากมีชุดงานหรือหมายเลขลำดับประจำสินค้าเพียงหมายเลขเดียว</span><span class="sxs-lookup"><span data-stu-id="0e7b6-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="0e7b6-129">อย่างไรก็ตาม เนื่องจากคลังสินค้าไม่มีการเปิดใช้งานกระบวนการคลังสินค้า ผู้ใช้จะต้องระบุมิติทั้งหมดเหนือ **สถานที่** เสมอ</span><span class="sxs-lookup"><span data-stu-id="0e7b6-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="0e7b6-130">แม่แบบการป้อนช่องที่มีเกณฑ์ช่องแสดงปริมาณคงคลังคงเหลือของพิจารณา จะไม่พิจารณาปริมาณคงคลังคงเหลือปัจจุบันของสินค้าที่มีการเปิดใช้งานชุดงาน</span><span class="sxs-lookup"><span data-stu-id="0e7b6-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="0e7b6-131">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การแบ่งช่วงเวลาของคลังสินค้า](warehouse-slotting.md)</span><span class="sxs-lookup"><span data-stu-id="0e7b6-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="0e7b6-132">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="0e7b6-132">Issue description</span></span>

<span data-ttu-id="0e7b6-133">แม่แบบการป้อนช่องที่มีเกณฑ์ช่อง *พิจารณาปริมาณคงคลังคงเหลือ* จะไม่พิจารณาปริมาณคงคลังคงเหลือปัจจุบันของสินค้าที่มีการเปิดใช้งาน *เหนือชุดงาน*</span><span class="sxs-lookup"><span data-stu-id="0e7b6-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="0e7b6-134">พิจารณาเฉพาะเมื่อระบุหมายเลขชุดงานบนบรรทัดใบสั่งขายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0e7b6-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="0e7b6-135">อย่างไรก็ตาม เมื่อคุณใช้สินค้าที่มี *ต่ำกว่าชุดงาน* ปริมาณคงคลังคงเหลือปัจจุบันจะถือเป็นสิ่งที่คาด</span><span class="sxs-lookup"><span data-stu-id="0e7b6-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="0e7b6-136">สาเหตุปัญหา</span><span class="sxs-lookup"><span data-stu-id="0e7b6-136">Issue cause</span></span>

<span data-ttu-id="0e7b6-137">คุณสามารถกําหนดหัวข้อแม่แบบช่องได้เพื่อกลยุทธ์ความต้องการ *ที่สั่ง* *จองแล้ว* หรือ *นำออกใช้* ลงในระบบแล้วได้</span><span class="sxs-lookup"><span data-stu-id="0e7b6-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="0e7b6-138">หากต้องการใช้กลยุทธ์ความต้องการ *ที่สั่ง* ข้อบังคับลำดับชั้นการจองเดียวกันจะมีผลบังคับกับการจองหรือปล่อยกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0e7b6-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="0e7b6-139">ดังนั้น สำหรับสินค้าที่มีลำดับชั้นการจอง *เหนือชุดงาน* และ *ต่ำกว่าหมายเลขลำดับประจำสินค้า* หมายเลขชุเงานหรือลำดับประจำสินค้าต้องระบุบนใบสั่งความต้องการ (การขายหรือการโอนย้าย)</span><span class="sxs-lookup"><span data-stu-id="0e7b6-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="0e7b6-140">หรือสามารถใช้กลยุทธ์ความต้องการ *ที่จองไว้* เพื่อเลือกหมายเลขชุดงานหรือหมายเลขลำดับประจำสินค้าก่อนที่จะสร้างความต้องการช่องข้อมูลคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="0e7b6-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
