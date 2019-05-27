---
title: ตรวจสอบความพร้อมของสินค้าคงคลัง
description: 'กระบวนงานนี้จะแสดงวิธีการตรวจสอบสินค้าคงคลังคงเหลือและสินค้าคงคลังคงเหลือที่มีอยู่จริงสำหรับจำนวนสินค้าเฉพาะ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26a8f51eda1f4249862a23fa0103b7a144d974a1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549905"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="c9234-103">ตรวจสอบความพร้อมของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="c9234-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9234-104">กระบวนงานนี้จะแสดงวิธีการตรวจสอบสินค้าคงคลังคงเหลือและสินค้าคงคลังคงเหลือที่มีอยู่จริงสำหรับจำนวนสินค้าเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="c9234-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="c9234-105">นอกจากนี้ยังแสดงให้เห็นวืธีการจัดหาข้อมูลที่เกี่ยวข้องกับสินค้า</span><span class="sxs-lookup"><span data-stu-id="c9234-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="c9234-106">สินค้าคงคลังคงเหลือที่มีอยู่จริงคือปริมาณคงคลังคงเหลือที่พร้อมใช้งาน นั่นคือสินค้าที่ซื้อแล้ว ได้รับ และลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="c9234-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="c9234-107">สินค้าคงคลังคงเหลือรวมถึงสินค้าคงคลังคงเหลือที่พร้อมใช้งาน แต่ด้วยสินค้าคงคลังที่ได้รับการสั่งซื้อและคาดไว้ แต่ยังไม่ได้รับ หรือลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="c9234-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="c9234-108">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="c9234-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="c9234-109">ถ้าคุณกำลังใช้ USMF คุณสามารถใช้ตัวอย่างมูลค่าที่แสดงอยู่</span><span class="sxs-lookup"><span data-stu-id="c9234-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="c9234-110">งานเหล่านี้โดยทั่วไปจะถูกดำเนินการโดยผู้ปฏิบัติงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="c9234-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="c9234-111">ตรวจสอบสินค้าคงคลังคงเหลือสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="c9234-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="c9234-112">ไปยัง การบริหารสินค้าคงคลัง > การสอบถาม และรายงาน > ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="c9234-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="c9234-113">เลือกแถวจำนวนสินค้า</span><span class="sxs-lookup"><span data-stu-id="c9234-113">Select the Item number row.</span></span>
    * <span data-ttu-id="c9234-114">เพื่อสอบถามปริมาณสินค้าคงคลังโดยหมายเลขสินค้า เลือกแถวที่ตารางที่ตั้งค่าไปยังปริมาณสินค้าคงเหลือและฟิลด์ถูกตั้งค่าไปยังหมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="c9234-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="c9234-115">ในฟิลด์เงื่อนไข เลือกสินค้าที่คุณต้องการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="c9234-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="c9234-116">ถ้าคุณกำลังใช้การข้อมูลสาธิตของบริษัท USMF คุณสามารถเลือก 'M9201'</span><span class="sxs-lookup"><span data-stu-id="c9234-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="c9234-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c9234-117">Click OK.</span></span>
5. <span data-ttu-id="c9234-118">คลิกที่มิติ</span><span class="sxs-lookup"><span data-stu-id="c9234-118">Click Dimensions.</span></span>
    * <span data-ttu-id="c9234-119">แท็บมิติช่วยให้คุณเลือกจำนวนรายละเอียดที่คุณต้องการดูเกี่ยวกับปริมาณสิ้นค้าคงคลัง </span><span class="sxs-lookup"><span data-stu-id="c9234-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="c9234-120">ถ้าคุณต้องการข้อมูลที่เกี่ยวข้องกับการจองสินค้า คุณต้องแสดงมิติสินค้าคงคลังทั้งหมดสำหรับสินค้านั้นใช้กระบวนการคลังสินค้าขึ้นสูงสุด (WHS)</span><span class="sxs-lookup"><span data-stu-id="c9234-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="c9234-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c9234-121">Click OK.</span></span>
7. <span data-ttu-id="c9234-122">ในบานหน้าต่างการดำเนินการ คลิกข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c9234-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="c9234-123">ถ้าคุณไม่เห็นนี่ คุณอาจะต้องคลิกที่ปุ่มจุดไข่ปลา (...) เพื่อดูตัวเลือกบานหน้าต่างตัวเลือกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c9234-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="c9234-124">คลิกดูภาพรวมการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="c9234-124">Click Supply overview.</span></span>
    * <span data-ttu-id="c9234-125">แท็บภาพรวมการจัดหาวัสดุให้จัดหาข้อมูลสำหรับสินค้าเฉพาะ เช่น ปริมาณคงคลังคงเหลือ เวลารอคอยสินค้า และข้อมูลผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c9234-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="c9234-126">ขยายส่วนคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="c9234-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="c9234-127">ขยายส่วนผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c9234-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="c9234-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9234-128">Close the page.</span></span>
12. <span data-ttu-id="c9234-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9234-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="c9234-130">ตรวจสอบสินค้าคงคลังคงเหลือที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="c9234-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="c9234-131">ไปยัง การจัดการคลังสินค้า > การสอบถาม และรายงาน > ปริมาณคงคลังคงเหลือที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="c9234-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="c9234-132">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c9234-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c9234-133">คุณสามารถใช้ไซต์และฟิลด์คลังสินค้าเพื่อกรองรายการของสินค้า</span><span class="sxs-lookup"><span data-stu-id="c9234-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="c9234-134">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="c9234-134">Refresh the page.</span></span>
4. <span data-ttu-id="c9234-135">คลิกแสดงมิติ</span><span class="sxs-lookup"><span data-stu-id="c9234-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="c9234-136">แท็บแสดงมิติช่วยให้คุณเลือกจำนวนรายละเอียดที่คุณต้องการดูเกี่ยวกับปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="c9234-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="c9234-137">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c9234-137">Click OK.</span></span>
6. <span data-ttu-id="c9234-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9234-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="c9234-139">ตรวจสอบปริมาณคงคลังคงเหลือโดยสถานที่</span><span class="sxs-lookup"><span data-stu-id="c9234-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="c9234-140">ไปยัง การจัดการคลังสินค้า > การสอบถาม และรายงาน > ปริมาณคงคลังคงเหลือโดยสถานที่</span><span class="sxs-lookup"><span data-stu-id="c9234-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="c9234-141">ในฟิลด์คลังสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c9234-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="c9234-142">ถ้าคุณกำลังใช้การข้อมูลสาธิตของบริษัท USMF คุณสามารถใช้ '51'</span><span class="sxs-lookup"><span data-stu-id="c9234-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="c9234-143">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="c9234-143">Refresh the page.</span></span>
4. <span data-ttu-id="c9234-144">คลิกแสดงมิติ</span><span class="sxs-lookup"><span data-stu-id="c9234-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="c9234-145">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c9234-145">Click OK.</span></span>
6. <span data-ttu-id="c9234-146">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c9234-146">Close the page.</span></span>

