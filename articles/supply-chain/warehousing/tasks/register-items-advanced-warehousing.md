---
title: ลงทะเบียนสินค้าเป็นสินค้าที่เปิดใช้งานคลังสินค้าขั้นสูงโดยใช้สมุดรายวันการมาถึงของสินค้า
description: 'กระบวนงานนี้แสดงวิธีการลงทะเบียนสินค้าโดยใช้สมุดรายวันการมาถึงของสินค้า เมื่อคุณใช้กระบวนการจัดการคลังสินค้าขั้นสูง '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2550e32db8b0d769f62c13654aa1dc1d201388ff
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148342"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="e12b1-103">ลงทะเบียนสินค้าเป็นสินค้าที่เปิดใช้งานคลังสินค้าขั้นสูงโดยใช้สมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="e12b1-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e12b1-104">กระบวนงานนี้แสดงวิธีการลงทะเบียนสินค้าโดยใช้สมุดรายวันการมาถึงของสินค้า เมื่อคุณใช้กระบวนการจัดการคลังสินค้าขั้นสูง </span><span class="sxs-lookup"><span data-stu-id="e12b1-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="e12b1-105">ซึ่งมักจะดำเนินการโดยเจ้าหน้าที่การรับสินค้า </span><span class="sxs-lookup"><span data-stu-id="e12b1-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="e12b1-106">คุณสามารถเรียกใช้ขั้นตอนนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง </span><span class="sxs-lookup"><span data-stu-id="e12b1-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="e12b1-107">คุณต้องมีใบสั่งซื้อที่ได้รับการยืนยันที่มีรายการใบสั่งซื้อที่เปิดอยู่ก่อนที่คุณเริ่มคู่มือนี้ </span><span class="sxs-lookup"><span data-stu-id="e12b1-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="e12b1-108">ต้องมีการเก็บสต็อกสินค้าในรายการ และจะต้องไม่ใช้ผลิตภัณฑ์ย่อย และต้องไม่มีมิติการติดตาม </span><span class="sxs-lookup"><span data-stu-id="e12b1-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="e12b1-109">และสินค้าจะต้องเชื่อมโยงกับกระบวนการการจัดการคลังสินค้าที่จะเปิดใช้งานกลุ่มมิติคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="e12b1-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="e12b1-110">ต้องเปิดใช้คลังสินค้าที่จะใช้สำหรับกระบวนการจัดการคลังสินค้า และสถานที่ที่คุณใช้สำหรับการรับสินค้าต้องมีการควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="e12b1-110">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="e12b1-111">ถ้าคุณกำลังใช้ USMF คุณสามารถใช้บัญชีบริษัท 1001 คลังสินค้า 51 และสินค้า M9200 เพื่อสร้าง PO ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e12b1-111">If you're using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="e12b1-112">จดบันทึกหมายเลขของใบสั่งซื้อที่คุณสร้าง และบันทึกหมายเลขสินค้าและไซต์ที่คุณใช้สำหรับรายการใบสั่งซื้อของคุณด้วย</span><span class="sxs-lookup"><span data-stu-id="e12b1-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="e12b1-113">สร้างหัวข้อสมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="e12b1-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="e12b1-114">ไปที่การมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="e12b1-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="e12b1-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e12b1-115">Click New.</span></span>
3. <span data-ttu-id="e12b1-116">ในฟิลด์ชื่อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e12b1-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="e12b1-117">ถ้าคุณกำลังใช้ USMF คุณสามารถพิมพ์ WHS.</span><span class="sxs-lookup"><span data-stu-id="e12b1-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="e12b1-118">ถ้าคุณกำลังใช้ข้อมูลอื่นๆ สมุดรายวันที่มีชื่อที่คุณเลือกจะต้องมีคุณสมบัติดังต่อไปนี้: ตรวจสอบดูว่าสถานที่เบิกสินค้าต้องถูกตั้งค่าเป็น ไม่ และการบริหารการตรวจสอบสินค้าต้องถูกตั้งค่าเป็น ไม่</span><span class="sxs-lookup"><span data-stu-id="e12b1-118">If you're using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="e12b1-119">ในฟิลด์หมายเลข ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e12b1-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="e12b1-120">ในฟิลด์ไซต์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e12b1-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="e12b1-121">เลือกไซต์ที่คุณใช้สำหรับรายการใบสั่งซื้อของคุณ </span><span class="sxs-lookup"><span data-stu-id="e12b1-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="e12b1-122">ซึ่งจะทำหน้าที่เป็นค่าเริ่มต้น ซึ่งจะเป็นค่าเริ่มต้นให้กับรายการทั้งหมดในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e12b1-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="e12b1-123">ถ้าคุณใช้คลังสินค้า 51 ใน USMF ให้เลือกไซต์ 5</span><span class="sxs-lookup"><span data-stu-id="e12b1-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="e12b1-124">ในฟิลด์คลังสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e12b1-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="e12b1-125">เลือกคลังสินค้าที่ถูกต้องสำหรับไซต์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="e12b1-125">Select a valid warehouse for the site that you've selected.</span></span> <span data-ttu-id="e12b1-126">ซึ่งจะทำหน้าที่เป็นค่าเริ่มต้น ซึ่งจะเป็นค่าเริ่มต้นให้กับรายการทั้งหมดในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e12b1-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="e12b1-127">ถ้าคุณกำลังใช้ค่าตัวอย่างใน USMF ให้เลือก 51</span><span class="sxs-lookup"><span data-stu-id="e12b1-127">If you're using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="e12b1-128">ในฟิลด์ตำแหน่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e12b1-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="e12b1-129">เลือกสถานที่ที่ถูกต้องในคลังสินค้าที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="e12b1-129">Select a valid location in the warehouse that you've selected.</span></span> <span data-ttu-id="e12b1-130">สถานที่เก็บที่จะต้องเชื่อมโยงกับโพรไฟล์ที่ตั้ง ซึ่งเป็นถูกควบคุมโดยป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="e12b1-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="e12b1-131">ซึ่งจะทำหน้าที่เป็นค่าเริ่มต้น ซึ่งจะเป็นค่าเริ่มต้นให้กับรายการทั้งหมดในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e12b1-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="e12b1-132">ถ้าคุณกำลังใช้ค่าตัวอย่างใน USMF ให้เลือก Bulk-008</span><span class="sxs-lookup"><span data-stu-id="e12b1-132">If you're using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="e12b1-133">คลิกขวาที่ลูกศรแบบหล่นลงในฟิลด์ป้ายทะเบียน และจากนั้นให้เลือกการดูรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="e12b1-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="e12b1-134">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e12b1-134">Click New.</span></span>
10. <span data-ttu-id="e12b1-135">ในฟิลด์แผ่นป้ายทะเบียน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e12b1-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="e12b1-136">จดบันทึกค่า</span><span class="sxs-lookup"><span data-stu-id="e12b1-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="e12b1-137">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e12b1-137">Click Save.</span></span>
12. <span data-ttu-id="e12b1-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e12b1-138">Close the page.</span></span>
13. <span data-ttu-id="e12b1-139">ในฟิลด์แผ่นป้ายทะเบียน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e12b1-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="e12b1-140">ป้อนมูลค่าของป้ายทะเบียนที่คุณเพิ่งสร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="e12b1-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="e12b1-141">ซึ่งจะทำหน้าที่เป็นค่าเริ่มต้น ซึ่งจะเป็นค่าเริ่มต้นให้กับรายการทั้งหมดในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e12b1-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="e12b1-142">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e12b1-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="e12b1-143">เพิมรายการ</span><span class="sxs-lookup"><span data-stu-id="e12b1-143">Add a line</span></span>
1. <span data-ttu-id="e12b1-144">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="e12b1-144">Click Add line.</span></span>
2. <span data-ttu-id="e12b1-145">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e12b1-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="e12b1-146">ป้อนหมายเลขสินค้าที่คุณใช้บนรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e12b1-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="e12b1-147">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="e12b1-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e12b1-148">ป้อนปริมาณที่คุณต้องการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="e12b1-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="e12b1-149">ฟิลด์วันที่จะกำหนดวันที่ที่ปริมาณคงเหลือของสินค้านี้จะถูกลงทะเบียนในสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="e12b1-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="e12b1-150">รหัสล็อตจะถูกเติมโดยระบบ ถ้ามีการระบุเฉพาะจากข้อมูลที่ให้ไว้ </span><span class="sxs-lookup"><span data-stu-id="e12b1-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="e12b1-151">มิฉะนั้น คุณจะต้องเพิ่มรายการนี้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="e12b1-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="e12b1-152">นี่เป็นฟิลด์บังคับที่ลิงค์การลงทะเบียนนี้กับรายการเอกสารต้นทางเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="e12b1-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="e12b1-153">ดำเนินงานการลงทะเบียนให้สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e12b1-153">Complete the registration</span></span>
1. <span data-ttu-id="e12b1-154">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e12b1-154">Click Validate.</span></span>
    * <span data-ttu-id="e12b1-155">มีการตรวจสอบว่า สมุดรายวันพร้อมที่จะถูกลงรายการบัญชีหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="e12b1-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="e12b1-156">หากการตรวจสอบจะล้มเหลวคุณ คุณจำเป็นต้องแก้ไขข้อผิดพลาดก่อนที่คุณจะสามารถลงรายการบัญชีสมุดรายวันได้</span><span class="sxs-lookup"><span data-stu-id="e12b1-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="e12b1-157">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e12b1-157">Click OK.</span></span>
    * <span data-ttu-id="e12b1-158">หลังจากที่คุณคลิกตกลง ตรวจสอบข้อความ </span><span class="sxs-lookup"><span data-stu-id="e12b1-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="e12b1-159">ควรมีข้อความแจ้งว่า สมุดรายวันเรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="e12b1-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="e12b1-160">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="e12b1-160">Click Post.</span></span>
4. <span data-ttu-id="e12b1-161">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e12b1-161">Click OK.</span></span>
    * <span data-ttu-id="e12b1-162">หลังจากที่คุณคลิกตกลง ตรวจสอบแถบข้อความ </span><span class="sxs-lookup"><span data-stu-id="e12b1-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="e12b1-163">ควรมีข้อความแจ้งว่า การดำเนินงานสำเร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="e12b1-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="e12b1-164">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e12b1-164">Close the page.</span></span>

