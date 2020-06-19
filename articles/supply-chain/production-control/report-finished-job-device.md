---
title: รายงานการเสร็จงานจากอุปกรณ์บัตรงาน
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกระบบเพื่อให้ผู้ใช้ของอุปกรณ์บัตรงานสามารถรายงานผลิตภัณฑ์ที่เสร็จสมบูรณ์จากใบสั่งผลิตไปยังสินค้าคงคลังได้
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403273"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="81d50-103">รายงานการเสร็จงานจากอุปกรณ์บัตรงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81d50-104">ผู้ปฏิบัติงานใช้หน้า **ความคืบหน้าของรายงาน** บนอุปกรณ์บัตรงานเพื่อรายงานปริมาณที่เสร็จสมบูรณ์แล้วสำหรับงานการผลิต</span><span class="sxs-lookup"><span data-stu-id="81d50-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="81d50-105">ควบคุมว่าจะเพิ่มปริมาณที่รายงานการเสร็จงานในสินค้าคงคลังหรือไม่</span><span class="sxs-lookup"><span data-stu-id="81d50-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="81d50-106">เมื่อต้องการควบคุมว่าจะเพิ่มปริมาณที่รายงานการเสร็จงานในการดำเนินการครั้งล่าสุดอย่างไรให้กับสินค้าคงคลัง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="81d50-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="81d50-107">ไปที่ **การควบคุมการผลิต \> การตั้งค่า \> การดำเนินการผลิต \> รายละเอียดของใบสั่งผลิต**</span><span class="sxs-lookup"><span data-stu-id="81d50-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="81d50-108">บนแท็บ **รายงานการเสร็จงาน** ให้ตั้งค่าฟิลด์ **อัปเดตรายงานที่เสร็จเรียบร้อยแล้วของรายงานออนไลน์** เป็นหนึ่งในค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="81d50-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="81d50-109">**ไม่** – ไม่มีการเพิ่มปริมาณในสินค้าคงคลังเมื่อมีการรายงานปริมาณในการดำเนินงานครั้งสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="81d50-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="81d50-110">สถานะของใบสั่งผลิตไม่สามารถเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="81d50-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="81d50-111">**สถานะ + ปริมาณ** – สถานะของใบสั่งผลิตจะเปลี่ยนเป็น *รายงานการเสร็จงาน* และจะมีการรายงานการเสร็จงานของปริมาณในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="81d50-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="81d50-112">**ปริมาณ** – จะมีการรายงานการเสร็จงานของปริมาณในสินค้าคงคลัง แต่สถานะของใบสั่งผลิตจะไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="81d50-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="81d50-113">**สถานะ** – เฉพาะสถานะของใบสั่งผลิตเท่านั้นที่เปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="81d50-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="81d50-114">ไม่มีการเพิ่มปริมาณในสินค้าคงคลังเมื่อมีการรายงานปริมาณในการดำเนินงานครั้งสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="81d50-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="81d50-115">ปริมาณที่ไม่มีการติดตามในสินค้าคงคลัง ถ้ามีการดำเนินงานที่มีการรายงานการเสร็จงานแล้วในขณะที่ไม่ได้กำหนดเป็นการดำเนินงานครั้งสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="81d50-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="81d50-116">อย่างไรก็ตาม สามารถใช้ปริมาณดังกล่าวเพื่อดูความคืบหน้าได้</span><span class="sxs-lookup"><span data-stu-id="81d50-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="81d50-117">นอกจากนี้ยังสามารถรวมไว้ในกฎซึ่งควบคุมว่าผู้ปฏิบัติงานสามารถเริ่มต้นการดำเนินงานถัดไปก่อนที่จะถึงขีดจำกัดที่กำหนดของปริมาณที่รายงานในการดำเนินงานก่อนหน้านี้ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="81d50-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="81d50-118">คุณสามารถกำหนดกฎเหล่านี้บนแท็บ **การตรวจสอบความถูกต้องของปริมาณ** ของหน้า **ค่าเริ่มต้นของใบสั่งผลิต**</span><span class="sxs-lookup"><span data-stu-id="81d50-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="81d50-119">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำงานกับหน้า **ค่าเริ่มต้นของใบสั่งผลิต** โปรดดู [พารามิเตอร์การผลิตในการดำเนินการผลิต](production-parameters-manufacturing-execution.md)</span><span class="sxs-lookup"><span data-stu-id="81d50-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="81d50-120">รายงานสินค้าที่ควบคุมชุดงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="81d50-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="81d50-121">อุปกรณ์บัตรงานสนับสนุนสถานการณ์จำลองสามสถานการณ์สำหรับการรายงานเกี่ยวกับสินค้าในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="81d50-122">สถานการณ์เหล่านี้ใช้ทั้งสำหรับสินค้าที่เปิดใช้งานสำหรับกระบวนการคลังสินค้าขั้นสูง ไปจนถึงสินค้าที่ไม่ได้เปิดใช้งานสำหรับกระบวนการคลังสินค้าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="81d50-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="81d50-123">**หมายเลขชุดงานที่กำหนดด้วยตนเอง:** ผู้ปฏิบัติงานป้อนหมายเลขชุดงานที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="81d50-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="81d50-124">หมายเลขชุดงานนี้อาจมาจากแหล่งภายนอกที่ไม่เป็นที่รู้จักในระบบ</span><span class="sxs-lookup"><span data-stu-id="81d50-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="81d50-125">**หมายเลขชุดงานที่กำหนดไว้ล่วงหน้า:** ผู้ปฏิบัติงานเลือกหมายเลขชุดงานในรายการของหมายเลขชุดงานที่ระบบสร้างขึ้นโดยอัตโนมัติก่อนที่ใบสั่งผลิตจะถูกนำออกใช้กับอุปกรณ์บัตรงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="81d50-126">**แก้ไขหมายเลขชุดงาน:** ผู้ปฏิบัติงานไม่ได้ป้อนหรือเลือกหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="81d50-127">ระบบจะกำหนดหมายเลขชุดงานให้กับใบสั่งผลิตก่อนที่จะนำออกใช้โดยอัตโนมัติแทน</span><span class="sxs-lookup"><span data-stu-id="81d50-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="81d50-128">หากต้องการเปิดใช้งานแต่ละสถานการณ์จำลอง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="81d50-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="81d50-129">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="81d50-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="81d50-130">เลือกผลิตภัณฑ์ที่ต้องการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="81d50-130">Select the product to configure.</span></span>
1. <span data-ttu-id="81d50-131">บนแท็บด่วน **จัดการสินค้าคงคลัง** ในฟิลด์ **กลุ่มหมายเลขชุดงาน** ให้เลือกกลุ่มหมายเลขการติดตามที่ตั้งค่าไว้เพื่อสนับสนุนสถานการณ์จำลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="81d50-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="81d50-132">ตามค่าเริ่มต้นถ้าไม่มีการกำหนดกลุ่มหมายเลขชุดงานให้กับผลิตภัณฑ์ควบคุมชุดงาน อุปกรณ์บัตรงานจะมีการป้อนข้อมูลด้วยตนเองสำหรับหมายเลขชุดงานในระหว่างการรายงานการเสร็จงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="81d50-133">ส่วนย่อยต่อไปนี้จะอธิบายวิธีการตั้งค่ากลุ่มหมายเลขการติดตามเพื่อสนับสนุนสถานการณ์สามรายการสำหรับการรายงานเกี่ยวกับรายการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="81d50-134">เปิดใช้งานการรายงานหมายเลขชุดงานบนอุปกรณ์บัตรงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="81d50-135">เมื่อต้องการเปิดใช้งานอุปกรณ์บัตรงานของคุณเพื่อยอมรับหมายเลขชุดงานในระหว่างการรายงานการเสร็จงาน คุณต้องใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อเปิดใช้งานคุณลักษณะต่อไปนี้ (ในใบสั่งนี้):</span><span class="sxs-lookup"><span data-stu-id="81d50-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="81d50-136">ปรับปรุงประสบการณ์การใช้งานของผู้ใช้สำหรับกล่องโต้ตอบรายงานความคืบหน้าในอุปกรณ์สำหรับบัตรงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="81d50-137">เปิดใช้งานการป้อนชุดงานและหมายเลขลำดับประจำสินค้าขณะมีการรายงานการเสร็จงานจากอุปกรณ์บัตรงาน (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="81d50-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="81d50-138">ตั้งค่ากลุ่มหมายเลขการติดตามที่ให้ผู้ปฏิบัติงานกำหนดหมายเลขชุดงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="81d50-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="81d50-139">ในการอนุญาตให้มีการกำหนดหมายเลขงานด้วยตนเองได้ ให้ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่ากลุ่มหมายเลขการติดตาม</span><span class="sxs-lookup"><span data-stu-id="81d50-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="81d50-140">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> มิติ \> กลุ่มหมายเลขการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="81d50-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="81d50-141">สร้างหรือเลือกกลุ่มหมายเลขการติดตามที่จะตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="81d50-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="81d50-142">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **ด้วยตนเอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="81d50-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="81d50-143">![หน้ากลุ่มหมายเลขการติดตาม](media/tracking-number-group-manual.png "หน้ากลุ่มหมายเลขการติดตาม")</span><span class="sxs-lookup"><span data-stu-id="81d50-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="81d50-144">ตั้งค่าอื่นๆ ตามที่คุณต้องการ แล้วเลือกกลุ่มหมายเลขการติดตามนี้เป็นกลุ่มหมายเลขชุดงานสำหรับผลิตภัณฑ์ที่นำออกใช้ที่คุณต้องการใช้สถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="81d50-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="81d50-145">เมื่อคุณใช้สถานการณ์นี้ ฟิลด์ **หมายเลขชุดงาน** ที่หน้า **ความคืบหน้าของรายงาน** บนอุปกรณ์บัตรงานมีกล่องข้อความที่ผู้ปฏิบัติงานสามารถป้อนค่าใดๆ ก็ได้</span><span class="sxs-lookup"><span data-stu-id="81d50-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="81d50-146">![หน้าความคืบหน้าการรายงานโดยมีฟิลด์สำหรับหมายเลขชุดงานด้วยตนเอง](media/job-card-device-batch-manual.png "หน้าความคืบหน้าการรายงานโดยมีฟิลด์สำหรับหมายเลขชุดงานด้วยตนเอง")</span><span class="sxs-lookup"><span data-stu-id="81d50-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="81d50-147">ตั้งค่ากลุ่มหมายเลขการติดตามซึ่งแสดงรายการของหมายเลขชุดงานที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="81d50-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="81d50-148">ในการให้รายการหมายเลขงานที่กำหนดล่วงหน้าด้วยตนเอง ให้ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่ากลุ่มหมายเลขการติดตาม</span><span class="sxs-lookup"><span data-stu-id="81d50-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="81d50-149">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า > มิติ \> กลุ่มหมายเลขการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="81d50-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="81d50-150">สร้างหรือเลือกกลุ่มหมายเลขการติดตามที่จะตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="81d50-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="81d50-151">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **เฉพาะรายการความเคลื่อนไหวของสินค้าคงคลังเท่านั้น** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="81d50-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="81d50-152">ใช้ฟิลด์ **ต่อปริมาณ** เพื่อแบ่งหมายเลขชุดงานสำหรับแต่ละปริมาณ โดยใช้ค่าที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="81d50-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="81d50-153">ตัวอย่างเช่น คุณมีใบสั่งผลิตสำหรับสิบชิ้นและฟิลด์ **ต่อปริมาณ** ถูกตั้งค่าเป็น *2*</span><span class="sxs-lookup"><span data-stu-id="81d50-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="81d50-154">ในกรณีนี้จะมีการกำหนดหมายเลขชุดงานห้าหมายเลขสำหรับใบสั่งผลิตเมื่อสร้างใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="81d50-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="81d50-155">![หน้ากลุ่มหมายเลขการติดตาม](media/tracking-number-group-predefined.png "หน้ากลุ่มหมายเลขการติดตาม")</span><span class="sxs-lookup"><span data-stu-id="81d50-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="81d50-156">ตั้งค่าอื่นๆ ตามที่คุณต้องการ แล้วเลือกกลุ่มหมายเลขการติดตามนี้เป็นกลุ่มหมายเลขชุดงานสำหรับผลิตภัณฑ์ที่นำออกใช้ที่คุณต้องการใช้สถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="81d50-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="81d50-157">เมื่อคุณใช้สถานการณ์นี้ ฟิลด์ **หมายเลขชุดงาน** ที่หน้า **ความคืบหน้าของรายงาน** บนอุปกรณ์บัตรงานมีรายการแบบหล่นลงที่ผู้ปฏิบัติงานต้องเลือกค่าไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="81d50-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="81d50-158">![หน้าความคืบหน้าการรายงานโดยมีรายการหมายเลขชุดงานที่กำหนดไว้ล่วงหน้า](media/job-card-device-batch-predefined.png "หน้าความคืบหน้าการรายงานโดยมีรายการหมายเลขชุดงานที่กำหนดไว้ล่วงหน้า")</span><span class="sxs-lookup"><span data-stu-id="81d50-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="81d50-159">ตั้งค่ากลุ่มหมายเลขการติดตามที่กำหนดหมายเลขชุดงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="81d50-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="81d50-160">ถ้าควรมีการกำหนดหมายเลขชุดงานโดยอัตโนมัติโดยไม่มีค่าที่ป้อนของผู้ปฏิบัติงาน ให้ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่ากลุ่มหมายเลขการติดตาม</span><span class="sxs-lookup"><span data-stu-id="81d50-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="81d50-161">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> มิติ \> กลุ่มหมายเลขการติดตาม**</span><span class="sxs-lookup"><span data-stu-id="81d50-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="81d50-162">สร้างหรือเลือกกลุ่มหมายเลขการติดตามที่จะตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="81d50-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="81d50-163">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าตัวเลือก **เฉพาะรายการความเคลื่อนไหวของสินค้าคงคลังเท่านั้น** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="81d50-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="81d50-164">ตั้งค่าตัวเลือก **ด้วยตนเอง** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="81d50-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="81d50-165">![หน้ากลุ่มหมายเลขการติดตาม](media/tracking-number-group-fixed.png "หน้ากลุ่มหมายเลขการติดตาม")</span><span class="sxs-lookup"><span data-stu-id="81d50-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="81d50-166">ตั้งค่าอื่นๆ ตามที่คุณต้องการ แล้วเลือกกลุ่มหมายเลขการติดตามนี้เป็นกลุ่มหมายเลขชุดงานสำหรับผลิตภัณฑ์ที่นำออกใช้ที่คุณต้องการใช้สถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="81d50-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="81d50-167">เมื่อคุณใช้สถานการณ์นี้ ฟิลด์ **หมายเลขชุดงาน** ที่หน้า **ความคืบหน้าของรายงาน** บนอุปกรณ์บัตรงานแสดงค่า แต่ผู้ปฏิบัติงานสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="81d50-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="81d50-168">![หน้าความคืบหน้าการรายงานที่มีหมายเลขชุดงานที่แก้ไข](media/job-card-device-batch-fixed.png "หน้าความคืบหน้าการรายงานที่มีหมายเลขชุดงานที่แก้ไข")</span><span class="sxs-lookup"><span data-stu-id="81d50-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="81d50-169">รายงานการเสร็จงานไปยังป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="81d50-169">Report as finished to a license plate</span></span>

<span data-ttu-id="81d50-170">กระบวนการคลังสินค้าขั้นสูงสามารถใช้มิติป้ายทะเบียนที่จะติดตามสินค้าคงคลังในที่ตั้งคลังสินค้าที่ตั้งค่าไว้สำหรับวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="81d50-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="81d50-171">ในกรณีนี้ จำเป็นต้องใช้หมายเลขป้ายทะเบียนเมื่อผู้ปฏิบัติงานรายงานการเสร็จงานของปริมาณ</span><span class="sxs-lookup"><span data-stu-id="81d50-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="81d50-172">เปิดใช้งานการรายงานและการพิมพ์ป้ายชื่อของป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="81d50-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="81d50-173">เมื่อต้องการใช้คุณลักษณะที่อธิบายไว้ในส่วนนี้ คุณต้องใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อเปิดใช้งานคุณลักษณะต่อไปนี้ (ในใบสั่งนี้):</span><span class="sxs-lookup"><span data-stu-id="81d50-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="81d50-174">ป้ายทะเบียนสำหรับการรายงานเมื่อเสร็จสิ้นที่เพิ่มในอุปกรณ์สำหรับบัตรงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="81d50-175">เปิดใช้งานการสร้างหมายเลขป้ายทะเบียนอัตโนมัติเมื่อมีการรายงานการเสร็จงานในอุปกรณ์บัตรงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="81d50-176">พิมพ์ป้ายฉลากจากอุปกรณ์สำหรับบัตรงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="81d50-177">ตั้งค่ารายงานการเสร็จงานไปยังป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="81d50-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="81d50-178">เมื่อต้องการควบคุมว่าผู้ปฏิบัติงานควรใช้ป้ายทะเบียนที่มีอยู่หรือสร้างป้ายทะเบียนใหม่เมื่อรายงานการเสร็จงานของปริมาณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="81d50-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="81d50-179">ไปที่ **การควบคุมการผลิต \> การตั้งค่า \> การดำเนินการผลิต \> ตั้งค่าคอนฟิกบัตรงานอุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="81d50-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="81d50-180">ตั้งค่าตัวเลือกต่อไปนี้สำหรับอุปกรณ์แต่ละรายการ:</span><span class="sxs-lookup"><span data-stu-id="81d50-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="81d50-181">**สร้างป้ายทะเบียน** – ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อสร้างป้ายทะเบียนใหม่สำหรับแต่ละรายงานการเสร็จงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="81d50-182">ตั้งค่าเป็น **ไม่** ถ้าควรใช้ป้ายทะเบียนที่มีอยู่สำหรับรายงานการเสร็จงานแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="81d50-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="81d50-183">**พิมพ์ป้ายชื่อ** – ตั้งค่าตัวเลือกนี้เป็น **ใช่** หากผู้ปฏิบัติงานต้องพิมพ์ป้ายชื่อป้ายทะเบียนสำหรับแต่ละรายงานการเสร็จงาน</span><span class="sxs-lookup"><span data-stu-id="81d50-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="81d50-184">ตั้งค่าเป็น **ไม่** ถ้าไม่จำเป็นต้องระบุป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="81d50-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="81d50-185">![ตั้งค่าคอนฟิกบัตรงานสำหรับหน้าอุปกรณ์](media/config-job-card-raf.png "ตั้งค่าคอนฟิกบัตรงานสำหรับหน้าอุปกรณ์")</span><span class="sxs-lookup"><span data-stu-id="81d50-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="81d50-186">ในการตั้งค่าป้ายชื่อ ไปที่ **การบริหารคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> การกำหนดเส้นทางเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="81d50-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="81d50-187">สำหรับข้อมูลเพิ่มเติมให้ดูที่ [เปิดใช้งานการพิมพ์ป้ายชื่อป้ายทะเบียน](../warehousing/tasks/license-plate-label-printing.md)</span><span class="sxs-lookup"><span data-stu-id="81d50-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
