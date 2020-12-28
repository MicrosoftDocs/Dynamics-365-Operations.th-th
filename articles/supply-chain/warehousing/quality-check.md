---
title: การตรวจสอบคุณภาพ
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับคุณลักษณะการตรวจสอบคุณภาพ ลักษณะการทำงานนี้อนุญาตให้ผู้ปฏิบัติงานคลังสินค้าทำการตรวจสอบคุณภาพตามจุดอย่างรวดเร็วในขณะที่ได้รับสินค้าไปยังพื้นที่ท่าสินค้าขาเข้า
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dfb71f74732d65409003c4f6f74145442a1efa3f
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438881"
---
# <a name="quality-check"></a><span data-ttu-id="f0f6c-104">การตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0f6c-105">คุณลักษณะ *การตรวจสอบคุณภาพ* ช่วยให้ผู้ปฏิบัติงานคลังสินค้าทำการตรวจสอบคุณภาพตามจุดอย่างรวดเร็วในขณะที่ได้รับสินค้าไปยังพื้นที่ท่าสินค้าขาเข้า</span><span class="sxs-lookup"><span data-stu-id="f0f6c-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="f0f6c-106">การตรวจสอบตามจุดเหล่านี้มีประโยชน์เมื่อผู้ปฏิบัติงานตรวจสอบบรรจุภัณฑ์หรือส่วนอื่นๆ ที่จดจำได้ง่ายของสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0f6c-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="f0f6c-107">คุณลักษณะนี้ช่วยแนะนำให้ผู้ปฏิบัติงานตรวจสอบอย่างรวดเร็วเพื่อดูว่ามีข้อผิดพลาดหรือความเสียหายใดๆ เกิดขึ้นก่อนที่จะสต็อกสินค้าคงคลังในสถานที่สำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0f6c-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="f0f6c-108">คุณลักษณะนี้เป็นทางเลือกสำหรับกระบวนการตรวจสอบคุณภาพมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="f0f6c-109">มีการประมวลผลที่ยืดหยุ่นและรวดเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="f0f6c-110">เมื่อคุณใช้ลักษณะนี้ การตรวจสอบการมาถึงและการตรวจสอบคุณภาพจะเกิดขึ้นในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="f0f6c-111">เมื่อมีการจัดส่งสินค้ามาถึง ผู้ปฏิบัติงานคลังสินค้าจะลงทะเบียนการมาถึง</span><span class="sxs-lookup"><span data-stu-id="f0f6c-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="f0f6c-112">ผู้ปฏิบัติงานยังสแกนป้ายทะเบียนเพื่อลงทะเบียนที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="f0f6c-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="f0f6c-113">ผู้ปฏิบัติงานตรวจสอบคุณภาพอย่างรวดเร็วและบันทึกผลลัพธ์ (ผ่านหรือล้มเหลว) สำหรับป้ายทะเบียนนั้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="f0f6c-114">หนึ่งในการดำเนินการต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="f0f6c-115">ถ้ามีการส่งผ่านการตรวจสอบคุณภาพแล้ว ป้ายทะเบียนจะได้รับการยอมรับและนำทางไปยังที่ตั้งที่ได้รับตามปกติ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="f0f6c-116">ถ้าการตรวจสอบคุณภาพล้มเหลว ป้ายทะเบียนถูกปฏิเสธและงานการสำรองสินค้าที่มีอยู่สำหรับรายการนั้นจะถูกเปลี่ยนเส้นทางไปยังที่ตั้งอื่นสำหรับการตรวจสอบเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f0f6c-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="f0f6c-117">จะมีการสร้างใบสั่งตรวจสอบคุณภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="f0f6c-117">A new quality order is created.</span></span> <span data-ttu-id="f0f6c-118">เมื่อต้องการดูใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นจากการตรวจสอบคุณภาพที่ล้มเหลว ให้ไปที่ **การบริหารสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ใบสั่งตรวจสอบคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="f0f6c-119">นอกจากนี้คุณยังสามารถตั้งค่ากระบวนการนี้เพื่อให้แผ่นป้ายทะเบียนที่สแกนทั้งหมดได้รับการโยกย้ายไปยังสถานที่ตรวจสอบคุณภาพทันที</span><span class="sxs-lookup"><span data-stu-id="f0f6c-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="f0f6c-120">เปิดใช้งานคุณลักษณะการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="f0f6c-121">ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การตรวจสอบคุณภาพ* ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="f0f6c-122">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f0f6c-123">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f0f6c-124">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f0f6c-125">**ชื่อคุณลักษณะ:** *การตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="f0f6c-126">ตั้งค่าคุณลักษณะสำหรับสถานการณ์ตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="f0f6c-127">ส่วนนี้ให้คำแนะนำและตัวอย่างที่แสดงวิธีการตั้งค่าคุณลักษณะ *การตรวจสอบคุณภาพ* และจัดเตรียมข้อมูลตัวอย่างสำหรับสถานการณ์ตัวอย่างที่ให้ไว้ในภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="f0f6c-128">ทำให้ข้อมูลตัวอย่างพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-128">Make sample data available</span></span>

<span data-ttu-id="f0f6c-129">เมื่อต้องการดำเนินการ [สถานการณ์ตัวอย่าง](#example-scenario) โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="f0f6c-130">นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="f0f6c-131">เท็มเพลตการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-131">Quality check template</span></span>

<span data-ttu-id="f0f6c-132">เท็มเพลตการตรวจสอบคุณภาพจะกำหนดกฎสำหรับการตรวจสอบจุดด่วนสำหรับคุณภาพในขณะที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="f0f6c-133">ไปที่ **การบริหารคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตการตรวจสอบคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="f0f6c-134">เลือก **สร้าง** เพื่อเพิ่มเท็มเพลตลงในกริด</span><span class="sxs-lookup"><span data-stu-id="f0f6c-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="f0f6c-135">ตั้งค่าค่าต่อไปนี้เพื่อกำหนดเท็มเพลตใหม่:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="f0f6c-136">**ชื่อเท็มเพลตการตรวจสอบคุณภาพ:** *ตรวจสอบศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="f0f6c-137">ป้อนชื่อที่ระบุนโยบายที่ใช้สำหรับเท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="f0f6c-138">**นโยบายการยอมรับ:** *พร้อมต์ผู้ใช้*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="f0f6c-139">ระบุว่าควรได้รับการแจ้งเตือนให้ผู้ใช้ยอมรับหรือปฏิเสธคุณภาพของสินค้าคงคลังในขณะที่ประมวลผลงานหรือไม่ หรือควรปฏิเสธคุณภาพโดยอัตโนมัติหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f0f6c-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="f0f6c-140">ตัวเลือกที่มีอยู่จะถูก *ปฏิเสธโดยอัตโนมัติ* และ *พร้อมต์ผู้ใช้*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="f0f6c-141">**นโยบายการประมวลผลคุณภาพ:** *สร้างใบสั่งตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="f0f6c-142">เลือกนโยบายที่ควรใช้เมื่อมีการปฏิเสธคุณภาพของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="f0f6c-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="f0f6c-143">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-143">The following options are available:</span></span>

        - <span data-ttu-id="f0f6c-144">*สร้างงานเท่านั้น* – สร้างแค่งานเพื่ออำนวยความสะดวกในการเคลื่อนย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="f0f6c-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="f0f6c-145">*สร้างใบสั่งตรวจสอบคุณภาพ* – สร้างใบสั่งตรวจสอบคุณภาพเพื่ออำนวยความสะดวกในการทดสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="f0f6c-146">**กลุ่มทดสอบ:** *สิ่งที่แนบมา*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="f0f6c-147">ระบุกลุ่มการทดสอบที่ควรใช้ในใบสั่งตรวจสอบคุณภาพที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="f0f6c-148">กลุ่มการทดสอบถูกตั้งค่าในโมดูล **การบริหารสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="f0f6c-149">ปิดใช้งานตัวเลือก **ข้อความที่ถูกทำลาย** สำหรับกลุ่มการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="f0f6c-150">ตัวเลือกนี้กำหนดว่าตัวอย่างจะถูกทำลายโดยเป็นส่วนหนึ่งของการทดสอบในกลุ่มการทดสอบหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f0f6c-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="f0f6c-151">ถ้ามีการใช้การทดสอบโดยการทำลาย ระบบจะสร้างรายการความเคลื่อนไหวของสินค้าคงคลังเมื่อมีการสร้างใบสั่งตรวจสอบคุณภาพสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0f6c-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="f0f6c-152">รายการความเคลื่อนไหวของสินค้าคงคลังใหม่ทำนายการลดสินค้าคงคลังสำหรับปริมาณการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="f0f6c-153">การลดลงของสินค้าคงคลังเกิดขึ้นเมื่อใบสั่งตรวจสอบคุณภาพเสร็จสมบูรณ์ผ่านขั้นตอนการทดสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f0f6c-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="f0f6c-154">รายการความเคลื่อนไหวของสินค้าคงคลังจะระบุเป็นใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="f0f6c-155">คลาสงานสำ – การตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-155">Work class – Quality check</span></span>

<span data-ttu-id="f0f6c-156">คลาสงานถูกใช้เพื่อกำหนดและ/หรือจำกัดชนิดของรายการใบสั่งงานที่ผู้ปฏิบัติงานคลังสินค้าสามารถประมวลผลบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f0f6c-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="f0f6c-157">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> คลาสงาน**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="f0f6c-158">เลือก **สร้าง** เพื่อสร้างคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="f0f6c-159">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="f0f6c-160">**รหัสคลาสงาน:** *การตรวจสอบ QC*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="f0f6c-161">ป้อนชื่อที่ระบุคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="f0f6c-162">**คำอธิบาย:** *การตรวจสอบ QC*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="f0f6c-163">ป้อนคำอธิบายโดยย่อที่บ่งชี้ว่ามีการใช้คลาสของงานเพื่ออะไร</span><span class="sxs-lookup"><span data-stu-id="f0f6c-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="f0f6c-164">**ชนิดของใบสั่งงาน:** *คุณภาพในการตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="f0f6c-165">เลือกชนิดของใบสั่งงานที่สร้างขึ้นโดยคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="f0f6c-166">เมื่อคุณตั้งค่างานการควบคุมคุณภาพ โปรดเลือก *คุณภาพในการตรวจสอบคุณภาพ* เสมอ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="f0f6c-167">บนแท็บด่วน **ชนิดสถานที่เก็บที่ถูกต้อง** ปล่อยฟิลด์ **ชนิดของสถานที่เก็บ** ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="f0f6c-168">ถ้าคุณเลือกชนิดของสถานที่เก็บ คุณจำกัดสถานที่ที่สามารถวางสินค้าได้หลังจากที่เบิกสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="f0f6c-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="f0f6c-169">ฟิลด์นี้จะใช้เมื่อคำสั่งสถานที่พยายามแก้ไขสถานที่เก็บ หรือเมื่อผู้ปฏิบัติงานคลังสินค้าระบุสถานที่จัดเก็บสินค้าสำหรับรายการเมนูอุปกรณ์เคลื่อนที่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="f0f6c-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="f0f6c-170">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคลาสงานและวิธีการสร้างคลาสงาน ให้ดูที่ [สร้างคลาสงาน](tasks/create-work-class.md)</span><span class="sxs-lookup"><span data-stu-id="f0f6c-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="f0f6c-171">เท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-171">Work template</span></span>

<span data-ttu-id="f0f6c-172">หน้าเท็มเพลตงานช่วยให้คุณสามารถกำหนดการดำเนินงานที่ต้องดำเนินการในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0f6c-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="f0f6c-173">โดยปกติ การดำเนินงานคลังสินค้าประกอบด้วยสองการดำเนินการ: ผู้ปฏิบัติงานคลังสินค้าเบิกสินค้าคงคลังคงเหลือในสถานที่เก็บหนึ่งและหลังจากนั้นก็ส่งสินค้าคงคลังที่เลือกมาไปลงไว้อีกสถานที่เก็บหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f0f6c-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="f0f6c-174">เท็มเพลตงานสำหรับการควบคุมคุณภาพกำหนดการดำเนินงานสำหรับการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="f0f6c-175">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-175">Purchase orders</span></span>

1. <span data-ttu-id="f0f6c-176">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="f0f6c-177">ในส่วนหัส ให้ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *ใบสั่งซื้อ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="f0f6c-178">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f0f6c-179">เลือกเท็มเพลตงานที่ควรมีขั้นตอนการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="f0f6c-180">ในส่วน **ภาพรวม** ในฟิลด์ **เท็มเพลตงาน** ให้เลือก *ใบเสร็จรับเงิน 51 PO*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="f0f6c-181">ในส่วน **รายละเอียดเท็มเพลตงาน** สังเกตว่ากริดมีบรรทัดที่มีอยู่สองบรรทัด: บรรทัดหนึ่งสำหรับการ *เบิกสินค้า* และอีกบรรทัดสำหรับ *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="f0f6c-182">ในส่วน **รายละเอียดเท็มเพลตงาน** ให้เลือก **สร้าง** เพื่อเพิ่มแถวสำหรับการควบคุมคุณภาพให้กับกริด</span><span class="sxs-lookup"><span data-stu-id="f0f6c-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="f0f6c-183">โปรดสังเกตว่าฟิลด์ **หมายเลขบรรทัด** สำหรับบรรทัดใหม่ถูกตั้งค่าเป็น *3*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="f0f6c-184">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-184">On the new line, set the following values.</span></span> <span data-ttu-id="f0f6c-185">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="f0f6c-186">**ชนิดงาน:** *การตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="f0f6c-187">**รหัสคลาสงาน:** *การซื้อ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="f0f6c-188">**ชื่อเท็มเพลตการตรวจสอบคุณภาพ:** *ตรวจสอบศูนย์เปลี่ยนถ่ายสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="f0f6c-189">เลือกรหัสเฉพาะสำหรับคลาสงาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="f0f6c-190">คุณสามารถใช้ค่านี้เพื่อกำหนดค่ารายการเมนูบนอุปกรณ์เคลื่อนที่และชนิดของงานที่รายการเมนูดังกล่าวสามารถประมวลผล</span><span class="sxs-lookup"><span data-stu-id="f0f6c-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="f0f6c-191">ในบานหน้าต่างการดำเนินการ ให้เลือก **บันทึก** เพื่อบันทึกงานของคุณจนถึงขณะนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="f0f6c-192">คุณได้รับข้อความแสดงข้อความแจ้งว่า "ต้องตรวจสอบคุณภาพที่ไม่ถูกต้องโดยตรงหลังจากการเบิกสินค้า"</span><span class="sxs-lookup"><span data-stu-id="f0f6c-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="f0f6c-193">ดังนั้นคุณต้องเปลี่ยนค่า **หมายเลขบรรทัด** สำหรับบรรทัดที่คุณเพิ่งเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f0f6c-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="f0f6c-194">ทำตามขั้นตอนต่อไปนี้เพื่อเปลี่ยนค่า **หมายเลขบรรทัด** สำหรับบรรทัดใหม่:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="f0f6c-195">ในส่วน **รายละเอียดเท็มเพลตงาน** ให้เลือกบรรทัดที่มีการตั้งค่าฟิลด์ **ชนิดงาน** ให้กับ *การตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="f0f6c-196">เลือกปุ่ม **เลื่อนขึ้น** หรือ **เลื่อนลง** เพื่อย้ายบรรทัด *ตรวจสอบคุณภาพ* เพื่อให้อยู่ตามหลังจากบรรทัด *การเบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="f0f6c-197">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="f0f6c-198">คุณภาพในการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-198">Quality in quality check</span></span>

<span data-ttu-id="f0f6c-199">ขั้นตอนถัดไปให้สร้างเท็มเพลตงานสำหรับการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="f0f6c-200">ในส่วนหัวของหน้า **เท็มเพลตงาน** ให้เปลี่ยนค่าของฟิลด์ **ชนิดของใบสั่งงาน** ให้เป็น *คุณภาพในการตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="f0f6c-201">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริดในส่วน **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="f0f6c-202">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="f0f6c-203">**เท็มเพลตงาน:** *51 การตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="f0f6c-204">ป้อนชื่อสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f0f6c-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="f0f6c-205">**คำอธิบายเท็มเพลตงาน:** *51 การตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="f0f6c-206">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก** เพื่อทำให้ส่วน **รายละเอียดเท็มเพลตงาน** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="f0f6c-207">ในขณะที่เท็มเพลตใหม่ยังคงถูกเลือกในส่วน **ภาพรวม** ให้เลือก **ใหม่** ในส่วน **รายละเอียดเท็มเพลตงาน** เพื่อเพิ่มแถวให้กับกริด</span><span class="sxs-lookup"><span data-stu-id="f0f6c-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="f0f6c-208">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="f0f6c-209">**ชนิดงาน:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="f0f6c-210">**รหัสคลาสงาน:** *การตรวจสอบ QC*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="f0f6c-211">เลือกชื่อของ [คลาสงาน](#work-class) ที่คุณสร้างไว้ก่อนหน้านี้สำหรับงานการควบคุมคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="f0f6c-212">ในส่วน **รายละเอียดเท็มเพลตงาน** ให้เลือก **สร้าง** อีกครั้งเพื่อเพิ่มแถวอีกแถวหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f0f6c-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="f0f6c-213">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="f0f6c-214">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="f0f6c-215">**รหัสคลาสงาน:** *การตรวจสอบ QC*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="f0f6c-216">เลือกชื่อของ [คลาสงาน](#work-class) ที่คุณสร้างไว้ก่อนหน้านี้สำหรับงานการควบคุมคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="f0f6c-217">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="f0f6c-218">ดูข้อมูลเพิ่มเติมเกี่ยวกับเท็มเพลตงานที่ [ควบคุมงานคลังสินค้าโดยใช้เท็มเพลตงานและคำสั่งสถานที่](control-warehouse-location-directives.md)</span><span class="sxs-lookup"><span data-stu-id="f0f6c-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="f0f6c-219">คำสั่งสถานที่ – ความล้มเหลวในการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-219">Location directive – Quality failures</span></span>

<span data-ttu-id="f0f6c-220">คำสั่งสถานที่มีกฎซึ่งช่วยให้ระบุการเบิกสินค้าและกำหนดสถานที่เก็บสำหรับการย้ายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="f0f6c-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="f0f6c-221">ตัวอย่างเช่น ในธุรกรรมใบสั่งขาย คำสั่งสถานที่จะกำหนดจุดที่จะเบิกสินค้า และจุดที่จะส่งสินค้าที่เบิก</span><span class="sxs-lookup"><span data-stu-id="f0f6c-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="f0f6c-222">คุณต้องตั้งค่าคอนฟิกกฎของคำสั่งสถานที่เพื่อกำหนดว่าจะจัดการการตรวจสอบคุณภาพที่ล้มเหลวอย่างไร</span><span class="sxs-lookup"><span data-stu-id="f0f6c-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="f0f6c-223">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="f0f6c-224">ในบานหน้าต่างด้านซ้าย ให้ตั้งค่าฟิลด์ **ชนิดของใบสั่งงาน** เป็น *ใบสั่งซื้อ* เพื่อทำงานกับคำสั่งของสถานที่เก็บของชนิดนั้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="f0f6c-225">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างคำสั่งสถานที่สำหรับการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="f0f6c-226">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="f0f6c-227">**หมายเลขลำดับ:** ยอมรับค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="f0f6c-228">**ชื่อ:** *51 เพื่อตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="f0f6c-229">บน FastTab **คำสั่งสถานที่** ให้กำหนดค่าดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="f0f6c-230">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="f0f6c-231">**ชนิดงาน:** *ส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="f0f6c-232">**ไซต์:** *5*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-232">**Site:** *5*</span></span>
    - <span data-ttu-id="f0f6c-233">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="f0f6c-234">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก** เพื่อบันทึกคำสั่งของคุณและทำให้แท็บด่วน **บรรทัด** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="f0f6c-235">บนแท็บด่วน **บรรทัด** ให้เลือก **สร้าง** เพื่อเพิ่มบรรทัดไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="f0f6c-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="f0f6c-236">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-236">On the new line, set the following values.</span></span> <span data-ttu-id="f0f6c-237">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="f0f6c-238">**ปริมาณเริ่มต้น:** *1*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="f0f6c-239">**ปริมาณสิ้นสุด:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="f0f6c-240">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก** เพื่อบันทึกบรรทัดใหม่และทำให้แท็บด่วน **การดำเนินการคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="f0f6c-241">ในขณะที่บรรทัดใหม่ยังคงถูกเลือกบนแท็บด่วน **บรรทัด** ให้เลือก **สร้าง** บนแท็บด่วน **การดำเนินการคำสั่งสถานที่** เพื่อเพิ่มแถวให้กับกริด ดังนั้นคุณจึงสามารถตั้งค่าการดำเนินการสำหรับบรรทัดนั้นได้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="f0f6c-242">ในแถวใหม่ ตั้งค่าฟิลด์ **ชื่อ** เป็น *คุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="f0f6c-243">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="f0f6c-244">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก** เพื่อทำให้ปุ่ม **แก้ไขการสอบถาม** บนแท็บด่วน **การดำเนินการคำสั่งสถานที่** พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="f0f6c-245">ในขณะที่รายการที่คุณเพิ่งเพิ่มยังคงถูกเลือกอยู่บนแท็บด่วน **การดำเนินการคำสั่งสถานที่** ให้เลือก **แก้ไขการสอบถาม** เพื่อเปิดกล่องโต้ตอบที่คุณสามารถแก้ไขการสอบถามสำหรับการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="f0f6c-246">บนแท็บ **ช่วง** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถวไปยังการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="f0f6c-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="f0f6c-247">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="f0f6c-248">**ตาราง:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="f0f6c-249">**ตารางสืบทอด:** *สถานที่*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="f0f6c-250">**ฟิลด์:** *สถานที่ตั้ง*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="f0f6c-251">**เกณฑ์:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="f0f6c-252">สถานที่เก็บ *QMS* เป็นสถานที่เก็บคลังสินค้าสำหรับคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="f0f6c-253">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="f0f6c-254">คุณต้องเปลี่ยนลำดับของคำสั่งสถานที่ของใบสั่งซื้อสำหรับคลังสินค้า *51*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="f0f6c-255">บันทึกคำสั่งสถานที่ *51 เพื่อตรวจสอบคุณภาพ* รีเฟรชหน้าและเลือกคำสั่งของสถานที่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="f0f6c-256">หลังจากนั้นให้ใช้ปุ่ม **เลื่อนขึ้น** และ **เลื่อนลง** ในบานหน้าต่างการดำเนินการเพื่อใส่คำสั่งสถานที่สำหรับคลังสินค้า *51* ตามลำดับต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="f0f6c-257">(ก่อนที่คุณจะเลือก **เลื่อนขึ้น** หรือ **เลื่อนลง** คุณต้องเลือกคำสั่งของสถานที่ในรายการ)</span><span class="sxs-lookup"><span data-stu-id="f0f6c-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="f0f6c-258">51 เพื่อตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-258">51 To Quality</span></span>
    2. <span data-ttu-id="f0f6c-259">51 PO Direct</span><span class="sxs-lookup"><span data-stu-id="f0f6c-259">51 PO Direct</span></span>
    3. <span data-ttu-id="f0f6c-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="f0f6c-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="f0f6c-261">รายการเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f0f6c-261">Mobile device menu items</span></span>

<span data-ttu-id="f0f6c-262">ตั้งค่าคอนฟิกรายการเมนูเพื่อให้อุปกรณ์เคลื่อนที่สามารถดำเนินการฟังก์ชัน **ตรวจสอบคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="f0f6c-263">การสำรองการซื้อ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-263">Purchase putaway</span></span>

1. <span data-ttu-id="f0f6c-264">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="f0f6c-265">ในรายการ เลือกรายการเมนู **การสำรองการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="f0f6c-266">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f0f6c-267">ในส่วน **คลาสงาน** ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="f0f6c-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="f0f6c-268">บนแถวใหม่ ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="f0f6c-269">**รหัสคลาสงาน:** *การตรวจสอบ QC*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="f0f6c-270">ป้อนชื่อของ [คลาสงาน](#work-class) ที่คุณสร้างไว้ก่อนหน้านี้สำหรับงานการควบคุมคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="f0f6c-271">**ชนิดของใบสั่งงาน:** *คุณภาพในการตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="f0f6c-272">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="f0f6c-273">การรับรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="f0f6c-274">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="f0f6c-275">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f0f6c-276">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="f0f6c-277">**ชื่อรายการในเมนู:** *การรับรายการ PO*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="f0f6c-278">**ชื่อเรื่อง:** *การรับรายการ PO*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="f0f6c-279">**โหมด:** *งาน*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="f0f6c-280">**ใช้งานที่มีอยู่:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="f0f6c-281">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="f0f6c-282">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ ที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="f0f6c-283">**กระบวนการสร้างงาน:** *การรับรายการของใบสั่งซื้อและการสำรองสินค้า*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="f0f6c-284">**สร้างป้ายทะเบียน:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="f0f6c-285">**เท็มเพลตงาน:** *51 PO Receipt*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="f0f6c-286">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="f0f6c-287">เพิ่มรายการเมนูที่เมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f0f6c-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="f0f6c-288">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> เมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="f0f6c-289">ในบานหน้าต่างด้านซ้าย ให้เลือกเมนู **ขาเข้า**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="f0f6c-290">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="f0f6c-291">ในคอลัมน์ **เมนูและรายการเมนูที่พร้อมใช้งาน** ให้เลือกรายการเมนู **การรับรายการ PO**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="f0f6c-292">เลือกปุ่มลูกศรขวาเพื่อย้าย **การรับรายการ PO** ไปยังคอลัมน์ **โครงสร้างเมนู**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="f0f6c-293">ในคอลัมน์ **โครงสร้างเมนู** ให้เลือก **การรับรายการ PO** แล้วเลือกปุ่มลูกศรขึ้นหรือปุ่มลูกศรลงเพื่อย้ายรายการเมนูไปยังตำแหน่งที่ต้องการบนเมนูของอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f0f6c-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="f0f6c-294">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="f0f6c-295">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="f0f6c-295">Example scenario</span></span>

<span data-ttu-id="f0f6c-296">หลังจากที่คุณได้ทำให้ข้อมูลตัวอย่างที่อธิบายไว้ก่อนหน้านี้ทั้งหมดพร้อมใช้งานแล้ว และตั้งค่าแล้ว คุณสามารถทำงานกับสถานการณ์จำลองนี้เพื่อลองใช้คุณลักษณะ *การตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="f0f6c-297">ค่าที่แสดงในสถานการณ์สมมตินี้สมมติว่าคุณกำลังทำงานกับข้อมูลสาธิตมาตรฐาน ซึ่งคุณเลือกนิติบุคคล **USMF** และคุณได้เตรียมเรกคอร์ดตัวอย่างที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="f0f6c-298">นอกจากนี้สถานการณ์จำลองนี้ยังทำหน้าที่เป็นตัวอย่างที่แสดงว่าคุณลักษณะนี้สามารถใช้ในการตั้งค่าการผลิตได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="f0f6c-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="f0f6c-299">สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-299">Create a purchase order</span></span>

1. <span data-ttu-id="f0f6c-300">ไปที่ **การจัดซื้อและการจัดหา \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="f0f6c-301">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f0f6c-302">ในกล่องโต้ตอบ **สร้างใบสั่งซื้อ** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f0f6c-303">**บัญชีผู้จัดจำหน่าย:** *104*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="f0f6c-304">**คลังสินค้า:** *51*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="f0f6c-305">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบและเปิดใบสั่งซื้อใหม่</span><span class="sxs-lookup"><span data-stu-id="f0f6c-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="f0f6c-306">บนแท็บด่วน **บรรทัดใบซื้อ** กริดมีบรรทัดว่างใหม่</span><span class="sxs-lookup"><span data-stu-id="f0f6c-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="f0f6c-307">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="f0f6c-308">**หมายเลขสินค้า:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="f0f6c-309">**ปริมาณ:** *3*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="f0f6c-310">**หน่วย:** *PL*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="f0f6c-311">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="f0f6c-312">ประมวลผลการรับการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-312">Process quality check receiving</span></span>

<span data-ttu-id="f0f6c-313">หลังจากที่สร้างใบสั่งซื้อแล้วคุณสามารถรับใบสั่งซื้อได้โดยใช้รายการเมนู **การรับสินค้าในรายการ PO** และฟังก์ชันของคุณลักษณะของ *การตรวจสอบคุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="f0f6c-314">ได้รับแท่นวางสินค้า 1</span><span class="sxs-lookup"><span data-stu-id="f0f6c-314">Receive pallet 1</span></span>

1. <span data-ttu-id="f0f6c-315">ลงชื่อเข้าใช้แอปคลังสินค้าในฐานะผู้ใช้ของคลังสินค้า *51*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="f0f6c-316">(ป้อน *51* เป็นรหัสผู้ใช้และ *1* เป็นรหัสผ่าน)</span><span class="sxs-lookup"><span data-stu-id="f0f6c-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="f0f6c-317">ไปที่ **ขาเข้า \> การรับรายการ PO**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="f0f6c-318">ในฟิลด์ **PONUM** ให้ป้อนหมายเลขใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="f0f6c-319">ยืนยันหมายเลขใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="f0f6c-320">ในฟิลด์ **LINENUM** ป้อนหมายเลขรายการใบสั่งซื้อที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="f0f6c-321">เนื่องจากใบสั่งมีเพียงบรรทัดเดียวในสถานการณ์นี้ คุณจะป้อน *1* ในฟิลด์ **LINENUM** สำหรับแต่ละขั้นตอนการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0f6c-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="f0f6c-322">ยืนยันหมายเลขรายการ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-322">Confirm the line number.</span></span>
1. <span data-ttu-id="f0f6c-323">ในฟิลด์ **QTY** ป้อนปริมาณที่ต้องได้รับ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="f0f6c-324">เนื่องจากใบสั่งซื้อมีไว้สำหรับสามแท่นวางสินค้า (*PL*) ในสถานการณ์นี้และมีขั้นตอนการรับสินค้าสามขั้น คุณจะป้อน *1* ในฟิลด์ **QTY** สำหรับแต่ละขั้นตอนการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0f6c-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="f0f6c-325">ยืนยันปริมาณ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-325">Confirm the quantity.</span></span>

    <span data-ttu-id="f0f6c-326">หน้า **ตรวจสอบคุณภาพ** ที่ปรากฏไม่มีฟิลด์ป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f0f6c-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="f0f6c-327">มีเพียงปุ่มยืนยัน (เครื่องหมาย) เท่านั้นที่ด้านล่างและปุ่มเมนู (**≡**) ที่ด้านบน</span><span class="sxs-lookup"><span data-stu-id="f0f6c-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="f0f6c-328">(ปุ่มเมนูบางครั้งเรียกว่าแฮมเบอร์เกอร์หรือปุ่มแฮมเบอร์เกอร์) เมื่อต้องการเร่งกระบวนการตรวจสอบคุณภาพ เมื่อแท่นวางสินค้าผ่านการตรวจสอบคุณภาพ ผู้ใช้เพียงยืนยันหน้า **ตรวจสอบคุณภาพ** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="f0f6c-329">![หน้าตรวจสอบคุณภาพ](media/quality-check.png "หน้าตรวจสอบคุณภาพ")</span><span class="sxs-lookup"><span data-stu-id="f0f6c-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="f0f6c-330">เลือกปุ่มยืนยันเพื่อส่งผ่านการตรวจสอบคุณภาพสำหรับแท่นวางสินค้า 1 จากบรรทัด 1</span><span class="sxs-lookup"><span data-stu-id="f0f6c-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="f0f6c-331">หน้า **ใบสั่งซื้อ: ส่งสินค้า** ซึ่งแสดงรายละเอียดของงานการส่งสินค้า:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="f0f6c-332">**LOC:** ที่ตั้งที่ระบบกำหนด</span><span class="sxs-lookup"><span data-stu-id="f0f6c-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="f0f6c-333">สถานที่นี้คือที่ตั้งการสำรองสินค้าที่กำหนดสำหรับการรับสินค้าตามใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="f0f6c-334">**LP:** รหัสป้ายทะเบียนที่ระบบสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="f0f6c-335">**สินค้า:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="f0f6c-336">**ปริมาณ:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="f0f6c-337">คำอธิบายสินค้าจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-337">The item description is also shown.</span></span>

1. <span data-ttu-id="f0f6c-338">ยืนยันงานการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0f6c-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="f0f6c-339">บนหน้า **งาน** สำหรับการได้รับบรรทัดใบสั่งซื้อ คุณจะได้รับข้อความ "ทำงานสำเร็จ"</span><span class="sxs-lookup"><span data-stu-id="f0f6c-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="f0f6c-340">ฟิลด์ **LINENUM** จะพร้อมใช้งานเพื่อให้คุณสามารถเริ่มต้นการรับแท่นวางสินค้าถัดไป</span><span class="sxs-lookup"><span data-stu-id="f0f6c-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="f0f6c-341">ได้รับแท่นวางสินค้า 2</span><span class="sxs-lookup"><span data-stu-id="f0f6c-341">Receive pallet 2</span></span>

<span data-ttu-id="f0f6c-342">สำหรับสถานการณ์จำลองนี้ แท่นวางสินค้า 2 จะถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="f0f6c-343">ในฟิลด์ **LINENUM** ให้ป้อน *1* และยืนยันหมายเลขบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f0f6c-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="f0f6c-344">ฟิลด์ **QTY** พร้อมใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="f0f6c-344">The **QTY** field is now available.</span></span> <span data-ttu-id="f0f6c-345">ป้อน *1* และยืนยันปริมาณ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="f0f6c-346">หน้า **ตรวจสอบคุณภาพ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-346">The **Quality check** page appears.</span></span> <span data-ttu-id="f0f6c-347">สำหรับใบเสร็จรับเงินนี้ แท่นวางสินค้าจะถูกปฏิเสธสำหรับคุณภาพ และจะถูกนำไปใส่ไว้ในสถานที่ที่มีคุณภาพ *QMS*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="f0f6c-348">เลือกปุ่มเมนู (**≡**) ที่ด้านบนของหน้า จากนั้นบนเมนูให้เลือก **ปฏิเสธ**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="f0f6c-349">บนหน้า **งาน** ที่ปรากฏขึ้นให้ป้อน **QMS** เป็นที่ตั้ง *การส่งสินค้า* ที่ใช้ในการส่งแท่นวางสินค้าเพื่อตรวจสอบเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f0f6c-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="f0f6c-350">หน้า **คุณภาพในการตรวจสอบคุณภาพ** ซึ่งแสดงรายละเอียดของงานการส่งสินค้า:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="f0f6c-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="f0f6c-352">สถานที่นี้คือที่ตั้งการสำรองสินค้าที่กำหนดสำหรับการรับคุณภาพที่ถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="f0f6c-353">**LP:** รหัสป้ายทะเบียนที่ระบบสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="f0f6c-354">**สินค้า:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="f0f6c-355">**ปริมาณ:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="f0f6c-356">คำอธิบายสินค้าจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-356">The item description is also shown.</span></span>

1. <span data-ttu-id="f0f6c-357">ยืนยันงานการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0f6c-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="f0f6c-358">บนหน้า **งาน** สำหรับการได้รับบรรทัดใบสั่งซื้อ คุณจะได้รับข้อความ "ทำงานสำเร็จ"</span><span class="sxs-lookup"><span data-stu-id="f0f6c-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="f0f6c-359">ฟิลด์ **LINENUM** จะพร้อมใช้งานเพื่อให้คุณสามารถเริ่มต้นการรับแท่นวางสินค้าถัดไป</span><span class="sxs-lookup"><span data-stu-id="f0f6c-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="f0f6c-360">ขณะนี้คุณได้ทำการตรวจสอบคุณภาพแล้วและสร้างใบสั่งตรวจสอบคุณภาพสำหรับแท่นวางสินค้าที่ถูกปฏิเสธแล้ว</span><span class="sxs-lookup"><span data-stu-id="f0f6c-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="f0f6c-361">เมื่อต้องการดูใบสั่งที่สร้างขึ้น ให้ไปที่ **การบริหารสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ใบสั่งตรวจสอบคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="f0f6c-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="f0f6c-362">การทดสอบใบสั่งตรวจสอบคุณภาพสามารถประมวลผลได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="f0f6c-363">การทดสอบคุณภาพไม่ครอบคลุมอยู่ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="f0f6c-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="f0f6c-364">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการคุณภาพ ดูที่ [ภาพรวมของการจัดการคุณภาพ](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="f0f6c-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="f0f6c-365">ได้รับแท่นวางสินค้า 3</span><span class="sxs-lookup"><span data-stu-id="f0f6c-365">Receive pallet 3</span></span>

<span data-ttu-id="f0f6c-366">สำหรับสถานการณ์จำลองนี้ แท่นวางสินค้า 3 จะถูกยอมรับ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="f0f6c-367">ในฟิลด์ **LINENUM** ให้ป้อน *1* และยืนยันหมายเลขบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f0f6c-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="f0f6c-368">ฟิลด์ **QTY** พร้อมใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="f0f6c-368">The **QTY** field is now available.</span></span> <span data-ttu-id="f0f6c-369">ป้อน *1* และยืนยันปริมาณ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="f0f6c-370">หน้า **ตรวจสอบคุณภาพ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-370">The **Quality check** page appears.</span></span> <span data-ttu-id="f0f6c-371">สำหรับการรับสินค้านี้ แท่นวางสินค้าจะถูกยอมรับสำหรับคุณภาพ และจะถูกนำไปใส่ไว้ในสถานที่การสำรองสินค้าจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="f0f6c-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="f0f6c-372">เลือกปุ่มยืนยันเพื่อส่งผ่านการตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="f0f6c-373">หน้า **ใบสั่งซื้อ: ส่งสินค้า** ซึ่งแสดงรายละเอียดของงานการส่งสินค้า:</span><span class="sxs-lookup"><span data-stu-id="f0f6c-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="f0f6c-374">**LOC:** ที่ตั้งที่ระบบกำหนด</span><span class="sxs-lookup"><span data-stu-id="f0f6c-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="f0f6c-375">สถานที่นี้คือที่ตั้งการสำรองสินค้าที่กำหนดสำหรับการรับสินค้าตามใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f0f6c-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="f0f6c-376">**LP:** รหัสป้ายทะเบียนที่ระบบสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="f0f6c-377">**สินค้า:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="f0f6c-378">**ปริมาณ:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="f0f6c-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="f0f6c-379">คำอธิบายสินค้าจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0f6c-379">The item description is also shown.</span></span>

1. <span data-ttu-id="f0f6c-380">ยืนยันงานการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="f0f6c-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="f0f6c-381">บนหน้า **งาน** สำหรับการได้รับบรรทัดใบสั่งซื้อ คุณจะได้รับข้อความ "ทำงานสำเร็จ"</span><span class="sxs-lookup"><span data-stu-id="f0f6c-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="f0f6c-382">ฟิลด์ **LINENUM** จะพร้อมใช้งานเพื่อให้คุณสามารถเริ่มต้นการรับแท่นวางสินค้าถัดไป</span><span class="sxs-lookup"><span data-stu-id="f0f6c-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="f0f6c-383">เลือกปุ่มเมนู (**≡**) ที่ด้านบนของหน้า จากนั้นบนเมนูให้เลือก **ยกเลิก** เพื่อกลับไปยังเมนู</span><span class="sxs-lookup"><span data-stu-id="f0f6c-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="f0f6c-384">ขณะนี้คุณสามารถปิดแอปมือถือได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="f0f6c-384">You can now close the mobile app.</span></span>
