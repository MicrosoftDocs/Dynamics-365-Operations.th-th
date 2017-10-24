--- 
title: "ลงทะเบียนสินค้าเป็นสินค้าที่เปิดใช้งานคลังสินค้าพื้นฐานโดยใช้สมุดรายวันการมาถึงของสินค้า"
description: "ขั้นตอนนี้แสดงวิธีการลงทะเบียนสินค้าโดยใช้สมุดรายวันการมาถึงของสินค้า เมื่อคุณใช้ \"คลังสินค้าพื้นฐาน\" ในโมดูลการจัดการสินค้าคงคลัง ซึ่งโดยปกติแล้ว "
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 184f38347e2525f3efef9b0d55003a94a75380d4
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="8432b-103">ลงทะเบียนสินค้าเป็นสินค้าที่เปิดใช้งานคลังสินค้าพื้นฐานโดยใช้สมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="8432b-103">Register items for a basic warehousing enabled item using an item arrival journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8432b-104">ขั้นตอนนี้แสดงวิธีการลงทะเบียนสินค้าโดยใช้สมุดรายวันการมาถึงของสินค้า เมื่อคุณใช้ "คลังสินค้าพื้นฐาน" ในโมดูลการจัดการสินค้าคงคลัง ซึ่งโดยปกติแล้ว </span><span class="sxs-lookup"><span data-stu-id="8432b-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="8432b-105">ซึ่งโดยปกติแล้ว เจ้าหน้าที่ส่วนรับสินค้าจะเป็นผู้ดำเนินการในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="8432b-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="8432b-106">คุณสามารถรันกระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF ที่มีค่าตัวอย่างตามที่แสดงไว้</span><span class="sxs-lookup"><span data-stu-id="8432b-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="8432b-107">ถ้าคุณไม่ได้ใช้ USMF คุณต้องมีใบสั่งซื้อที่ยืนยันแล้วที่มีบรรทัดใบสั่งซื้อที่เปิดอยู่ก่อนที่คุณเริ่มคำแนะนำนี้</span><span class="sxs-lookup"><span data-stu-id="8432b-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="8432b-108">สินค้าในรายการต้องถูกสต็อกก่อน และจะต้องไม่ใช้ผลิตภัณฑ์ย่อย และต้องไม่มีมิติการติดตาม</span><span class="sxs-lookup"><span data-stu-id="8432b-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="8432b-109">และสินค้าต้องเชื่อมโยงกับกลุ่มมิติการจัดเก็บ ที่ไซต์และคลังสินค้าเปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="8432b-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="8432b-110">สร้างหัวข้อสมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="8432b-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="8432b-111">ไปยัง การบริหารสินค้าคงคลัง > รายการสมุดรายวัน > การมาถึงของสินค้า > การมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="8432b-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="8432b-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8432b-112">Click New.</span></span>
3. <span data-ttu-id="8432b-113">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="8432b-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="8432b-114">ถ้าคุณกำลังใช้ USMF คุณสามารถพิมพ์ WHS.</span><span class="sxs-lookup"><span data-stu-id="8432b-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="8432b-115">ถ้าคุณกำลังใช้ข้อมูลอื่นๆ สมุดรายวันที่มีชื่อที่คุณเลือกจะต้องมีคุณสมบัติดังต่อไปนี้: ตรวจสอบดูว่าสถานเบิกสินค้าต้องถูกตั้งค่าเป็น No และการบริหารการตรวจสอบสินค้าต้องถูกตั้งค่าเป็น No</span><span class="sxs-lookup"><span data-stu-id="8432b-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="8432b-116">ในฟิลด์ บันทึกการจัดส่ง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8432b-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="8432b-117">นี่คือรหัสบันทึกการจัดส่งจากบันทึกการจัดส่งที่ออกโดยผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="8432b-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="8432b-118">เพิ่มหมายเลขเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8432b-118">Add a unique number.</span></span>  
5. <span data-ttu-id="8432b-119">ในฟิลด์ตัวเลข ในฟิลด์ตัวเลข เลือกใบสั่งซื้อ...</span><span class="sxs-lookup"><span data-stu-id="8432b-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="8432b-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8432b-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="8432b-121">เพิ่มบรรทัดรายไปยังสมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="8432b-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="8432b-122">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="8432b-122">Click Functions.</span></span>
2. <span data-ttu-id="8432b-123">คลิกสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="8432b-123">Click Create lines.</span></span>
    * <span data-ttu-id="8432b-124">บรรทัดต่างๆ สามารถถูกป้อนลงในสมุดรายวันนี้ด้วยตนเองหรือสร้างขึ้นโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="8432b-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="8432b-125">นี่จะเป็นการแสดงวิธีการสร้างมันขึ้นมาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8432b-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="8432b-126">ทำเครื่องหมายหรือถอดเครื่องหมายเริ่มปริมาณกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="8432b-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="8432b-127">นี่จะเริ่มต้นปริมาณบนบรรทัดในสมุดรายวัน กับปริมาณไม่ได้ลงทะเบียนจากบรรทัดในใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="8432b-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="8432b-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8432b-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="8432b-129">ลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8432b-129">Post the journal</span></span>
1. <span data-ttu-id="8432b-130">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="8432b-130">Click Post.</span></span>
2. <span data-ttu-id="8432b-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8432b-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="8432b-132">สร้างใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="8432b-132">Generate the product receipt</span></span>
1. <span data-ttu-id="8432b-133">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="8432b-133">Click Functions.</span></span>
2. <span data-ttu-id="8432b-134">คลิก ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="8432b-134">Click Product receipt.</span></span>
3. <span data-ttu-id="8432b-135">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8432b-135">Click OK.</span></span>


