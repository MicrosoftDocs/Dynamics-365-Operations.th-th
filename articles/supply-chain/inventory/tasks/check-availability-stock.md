---
title: ตรวจสอบความพร้อมของสินค้าคงคลัง
description: 'กระบวนงานนี้จะแสดงวิธีการตรวจสอบสินค้าคงคลังคงเหลือและสินค้าคงคลังคงเหลือที่มีอยู่จริงสำหรับจำนวนสินค้าเฉพาะ '
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2153117d9c921b43658edeade49a8403553e371
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238073"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="56122-103">ตรวจสอบความพร้อมของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="56122-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56122-104">กระบวนงานนี้จะแสดงวิธีการตรวจสอบสินค้าคงคลังคงเหลือและสินค้าคงคลังคงเหลือที่มีอยู่จริงสำหรับจำนวนสินค้าเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="56122-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="56122-105">นอกจากนี้ยังแสดงให้เห็นวืธีการจัดหาข้อมูลที่เกี่ยวข้องกับสินค้า</span><span class="sxs-lookup"><span data-stu-id="56122-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="56122-106">สินค้าคงคลังคงเหลือที่มีอยู่จริงคือ ปริมาณคงคลังคงเหลือที่พร้อมใช้งาน – นั่นคือสินค้าที่ซื้อ ได้รับ และลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="56122-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="56122-107">สินค้าคงคลังคงเหลือรวมถึงสินค้าคงคลังคงเหลือที่พร้อมใช้งาน และรวมถึงสินค้าคงคลังที่ได้รับการสั่งซื้อและถูกคาดไว้ แต่ยังไม่ได้รับ หรือยังไม่ได้ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="56122-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="56122-108">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="56122-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="56122-109">ถ้าคุณกำลังใช้ USMF คุณสามารถใช้ตัวอย่างมูลค่าที่แสดงอยู่</span><span class="sxs-lookup"><span data-stu-id="56122-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="56122-110">งานเหล่านี้โดยทั่วไปจะถูกดำเนินการโดยผู้ปฏิบัติงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="56122-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="56122-111">ตรวจสอบสินค้าคงคลังคงเหลือสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="56122-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="56122-112">ไปที่ **แถบหน้าต่างนำทาง > โมดูล > การจัดการสินค้าคงคลัง > การสอบถามและรายงาน > ปริมาณสินค้าคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="56122-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="56122-113">เลือกแถว **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="56122-113">Select the **Item number** row.</span></span> <span data-ttu-id="56122-114">เพื่อสอบถามปริมาณสินค้าคงคลังโดยหมายเลขสินค้า เลือกแถวที่ตารางที่ตั้งค่าไปยัง **ปริมาณสินค้าคงเหลือ** และฟิลด์ถูกตั้งค่าเป็นหมายเลข **สินค้า**</span><span class="sxs-lookup"><span data-stu-id="56122-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="56122-115">ในฟิลด์ **เงื่อนไข** เลือกสินค้าที่คุณต้องการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="56122-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="56122-116">ถ้าคุณกำลังใช้การข้อมูลสาธิตของบริษัท USMF คุณสามารถเลือก 'M9201'</span><span class="sxs-lookup"><span data-stu-id="56122-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="56122-117">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="56122-117">Click **OK**.</span></span>
5. <span data-ttu-id="56122-118">บน **บานหน้าต่างการดำเนินการ** คลิก **มิติ**</span><span class="sxs-lookup"><span data-stu-id="56122-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="56122-119">แท็บ **มิติ** ช่วยให้คุณเลือกจำนวนรายละเอียดที่คุณต้องการดูเกี่ยวกับปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="56122-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="56122-120">ถ้าคุณต้องการข้อมูลที่เกี่ยวข้องกับการจองสินค้า คุณต้องแสดงมิติสินค้าคงคลังทั้งหมดสำหรับสินค้านั้นใช้กระบวนการคลังสินค้าขึ้นสูงสุด (WMS)</span><span class="sxs-lookup"><span data-stu-id="56122-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="56122-121">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="56122-121">Click **OK**.</span></span>
7. <span data-ttu-id="56122-122">ใน **บานหน้าต่างการดำเนินการ** คลิก **ข้อมูลที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="56122-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="56122-123">ถ้าคุณไม่เห็นตัวเลือกนี้ คุณอาจะต้องคลิกที่ปุ่มจุดไข่ปลา (...) เพื่อดูตัวเลือกบานหน้าต่างการดำเนินการเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="56122-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="56122-124">คลิก **ดูภาพรวมการจัดหาวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="56122-124">Click **Supply overview**.</span></span> <span data-ttu-id="56122-125">แท็บ **ภาพรวมการจัดหาวัสดุ** ให้จัดหาข้อมูลสำหรับสินค้าเฉพาะ เช่น ปริมาณคงคลังคงเหลือ เวลารอคอยสินค้า และข้อมูลผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="56122-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="56122-126">ขยายส่วน **คงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="56122-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="56122-127">ขยายส่วน **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="56122-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="56122-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="56122-128">Close the page.</span></span>
12. <span data-ttu-id="56122-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="56122-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="56122-130">ตรวจสอบสินค้าคงคลังคงเหลือที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="56122-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="56122-131">ไปที่ **แถบหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การสอบถามและรายงาน > ปริมาณสินค้าคงคลังคงเหลือที่มีอยู่จริง**</span><span class="sxs-lookup"><span data-stu-id="56122-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="56122-132">ในฟิลด์ **หมายเลขสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="56122-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="56122-133">คุณสามารถใช้ไซต์และฟิลด์คลังสินค้าเพื่อกรองรายการของสินค้า</span><span class="sxs-lookup"><span data-stu-id="56122-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="56122-134">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="56122-134">Refresh the page.</span></span>
4. <span data-ttu-id="56122-135">บน **บานหน้าต่างการดำเนินการ** คลิก **แสดงมิติ**</span><span class="sxs-lookup"><span data-stu-id="56122-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="56122-136">แท็บแสดงมิติช่วยให้คุณเลือกจำนวนรายละเอียดที่คุณต้องการดูเกี่ยวกับปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="56122-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="56122-137">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="56122-137">Click **OK**.</span></span>
6. <span data-ttu-id="56122-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="56122-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="56122-139">ตรวจสอบปริมาณคงคลังคงเหลือโดยสถานที่</span><span class="sxs-lookup"><span data-stu-id="56122-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="56122-140">ไปที่ **แถบหน้าต่างนำทาง > โมดูล > การจัดการคลังสินค้า > การสอบถามและรายงาน > คงเหลือจามสถานที่**</span><span class="sxs-lookup"><span data-stu-id="56122-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="56122-141">ในฟิลด์ **คลังสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="56122-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="56122-142">ถ้าคุณกำลังใช้การข้อมูลสาธิตของบริษัท USMF คุณสามารถใช้ '51'</span><span class="sxs-lookup"><span data-stu-id="56122-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="56122-143">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="56122-143">Refresh the page.</span></span>
4. <span data-ttu-id="56122-144">คลิก **แสดงมิติ**</span><span class="sxs-lookup"><span data-stu-id="56122-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="56122-145">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="56122-145">Click **OK**.</span></span>
6. <span data-ttu-id="56122-146">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="56122-146">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]