---
title: ลงทะเบียนสินค้าเป็นสินค้าที่เปิดใช้งานคลังสินค้าพื้นฐานโดยใช้สมุดรายวันการมาถึงของสินค้า
description: กระบวนงานนี้แสดงวิธีการลงทะเบียนสินค้าโดยใช้สมุดรายวันการมาถึงของสินค้า เมื่อคุณใช้ "คลังสินค้าพื้นฐาน" ในโมดูลการจัดการสินค้าคงคลัง
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec8c1912435cf822db6eaecc5fff3dbcac793f77
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977074"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="4bfd4-103">ลงทะเบียนสินค้าเป็นสินค้าที่เปิดใช้งานคลังสินค้าพื้นฐานโดยใช้สมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="4bfd4-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4bfd4-104">กระบวนงานนี้แสดงวิธีการลงทะเบียนสินค้าโดยใช้สมุดรายวันการมาถึงของสินค้า เมื่อคุณใช้ "คลังสินค้าพื้นฐาน" ในโมดูลการจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4bfd4-104">This procedure shows you how to register items using the item arrival journal when you are using "basic warehousing" in the Inventory management module.</span></span> <span data-ttu-id="4bfd4-105">ซึ่งโดยปกติแล้ว เจ้าหน้าที่ส่วนรับสินค้าจะเป็นผู้ดำเนินการในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="4bfd4-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="4bfd4-106">คุณสามารถรันกระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF ที่มีค่าตัวอย่างตามที่แสดงไว้</span><span class="sxs-lookup"><span data-stu-id="4bfd4-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="4bfd4-107">ถ้าคุณไม่ได้ใช้ USMF คุณต้องมีใบสั่งซื้อที่ยืนยันแล้วที่มีบรรทัดใบสั่งซื้อที่เปิดอยู่ก่อนที่คุณเริ่มคำแนะนำนี้</span><span class="sxs-lookup"><span data-stu-id="4bfd4-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="4bfd4-108">ต้องเก็บสินค้าในรายการในคลัง</span><span class="sxs-lookup"><span data-stu-id="4bfd4-108">The item on the line must be stocked.</span></span> <span data-ttu-id="4bfd4-109">และสินค้าต้องเชื่อมโยงกับกลุ่มมิติการจัดเก็บ ที่ไซต์และคลังสินค้าเปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="4bfd4-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="4bfd4-110">สร้างหัวข้อสมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="4bfd4-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="4bfd4-111">ไปยัง การบริหารสินค้าคงคลัง > รายการสมุดรายวัน > การมาถึงของสินค้า > การมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="4bfd4-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="4bfd4-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4bfd4-112">Click New.</span></span>
3. <span data-ttu-id="4bfd4-113">ในฟิลด์ชื่อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4bfd4-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="4bfd4-114">ถ้าคุณกำลังใช้ USMF คุณสามารถพิมพ์ WHS.</span><span class="sxs-lookup"><span data-stu-id="4bfd4-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="4bfd4-115">ถ้าคุณกำลังใช้ข้อมูลอื่นๆ สมุดรายวันที่มีชื่อที่คุณเลือกจะต้องมีคุณสมบัติดังต่อไปนี้: สถานที่เบิกเช็คต้องถูกตั้งค่าเป็น ไม่ และการบริหารการตรวจสอบสินค้าต้องถูกตั้งค่าเป็น ไม่</span><span class="sxs-lookup"><span data-stu-id="4bfd4-115">If you're using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="4bfd4-116">ในฟิลด์ บันทึกการจัดส่ง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4bfd4-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="4bfd4-117">นี่คือรหัสบันทึกการจัดส่งจากบันทึกการจัดส่งที่ออกโดยผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="4bfd4-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="4bfd4-118">เพิ่มหมายเลขเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="4bfd4-118">Add a unique number.</span></span>  
5. <span data-ttu-id="4bfd4-119">ในฟิลด์ตัวเลข ในฟิลด์ตัวเลข เลือกใบสั่งซื้อ...</span><span class="sxs-lookup"><span data-stu-id="4bfd4-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="4bfd4-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4bfd4-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="4bfd4-121">เพิ่มบรรทัดรายไปยังสมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="4bfd4-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="4bfd4-122">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="4bfd4-122">Click Functions.</span></span>
2. <span data-ttu-id="4bfd4-123">คลิกสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="4bfd4-123">Click Create lines.</span></span>
    * <span data-ttu-id="4bfd4-124">บรรทัดต่างๆ สามารถถูกป้อนลงในสมุดรายวันนี้ด้วยตนเองหรือสร้างขึ้นโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="4bfd4-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="4bfd4-125">นี่จะเป็นการแสดงวิธีการสร้างมันขึ้นมาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4bfd4-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="4bfd4-126">ทำเครื่องหมายหรือถอดเครื่องหมายเริ่มปริมาณกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="4bfd4-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="4bfd4-127">นี่จะเริ่มต้นปริมาณบนบรรทัดในสมุดรายวัน กับปริมาณไม่ได้ลงทะเบียนจากบรรทัดในใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4bfd4-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="4bfd4-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4bfd4-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="4bfd4-129">ลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="4bfd4-129">Post the journal</span></span>
1. <span data-ttu-id="4bfd4-130">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="4bfd4-130">Click Post.</span></span>
2. <span data-ttu-id="4bfd4-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4bfd4-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="4bfd4-132">สร้างใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4bfd4-132">Generate the product receipt</span></span>
1. <span data-ttu-id="4bfd4-133">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="4bfd4-133">Click Functions.</span></span>
2. <span data-ttu-id="4bfd4-134">คลิก ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4bfd4-134">Click Product receipt.</span></span>
3. <span data-ttu-id="4bfd4-135">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4bfd4-135">Click OK.</span></span>

