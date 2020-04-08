---
title: สร้างแค็ตตาล็อกการจัดซื้อ
description: หัวข้อนี้อธิบายวิธีการสร้างแค็ตตาล็อกการจัดซื้อ
author: mkirknel
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 94d5c3f6677ec10ea1b9ac3c488c3b8d7dc6856f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147491"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="668fc-103">สร้างแค็ตตาล็อกการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="668fc-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="668fc-104">หัวข้อนี้อธิบายวิธีการสร้างแค็ตตาล็อกการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="668fc-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="668fc-105">โดยทั่วไปงานเหล่านี้จะดำเนินการโดยผู้เชี่ยวชาญด้านการจัดซื้อจัดหา </span><span class="sxs-lookup"><span data-stu-id="668fc-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="668fc-106">คุณจะทราบว่าพนักงานสามารถใช้แค็ตตาล็อกเมื่อสร้างใบสั่งได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="668fc-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="668fc-107">ก่อนที่คุณจะสามารถสร้างแค็ตตาล็อก จะต้องมีประเภทการจัดซื้อตามลำดับชั้นในระบบของคุณก่อน</span><span class="sxs-lookup"><span data-stu-id="668fc-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="668fc-108">ลำดับชั้นจะสืบทอดโดยแค็ตตาล็อกใหม่ พร้อมกับผลิตภัณฑ์ทั้งหมดที่อยู่ในลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="668fc-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="668fc-109">คุณสามารถใช้คำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF ที่ประเภทการจัดซื้อตามลำดับชั้นพร้อมใช้งาน ตลอดจนตัวอย่างที่ใช้ในกระบวนงาน</span><span class="sxs-lookup"><span data-stu-id="668fc-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="668fc-110">ตรวจสอบให้แน่ใจว่ามีประเภทการจัดซื้อตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="668fc-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="668fc-111">ไปที่ **บานหน้าต่างการนำทาง > โมดูล > การจัดซื้อและการจัดหา > แค็ตตาล็อกการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="668fc-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="668fc-112">ประเภทการจัดซื้อตามลำดับชั้นจะพร้อมใช้งานในบริษัทข้อมูลสาธิต USMF และมีการเพิ่มผลิตภัณฑ์ในประเภท **เครื่องจักร/คอมพิวเตอร์สำนักงาน**</span><span class="sxs-lookup"><span data-stu-id="668fc-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="668fc-113">ถ้าคุณกำลังใช้งานกระบวนงานนี้เป็นคู่มืองาน คุณจะต้องปลดล็อคคำแนะนำ ถ้าคุณต้องการเรียกดูผ่านประเภท</span><span class="sxs-lookup"><span data-stu-id="668fc-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="668fc-114">ถ้าลำดับชั้นไม่พร้อมใช้งาน คุณจะสร้างขึ้นโดยการคลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="668fc-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="668fc-115">การดำเนินการนี้สามารถทำได้เพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="668fc-115">This can only be done once.</span></span>  
2. <span data-ttu-id="668fc-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="668fc-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="668fc-117">สร้างแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="668fc-117">Create a catalog</span></span>
1. <span data-ttu-id="668fc-118">ไปที่ **บานหน้าต่างการนำทาง > โมดูล > การจัดซื้อและการจัดหา > แค็ตตาล็อก > แค็ตตาล็อกการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="668fc-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="668fc-119">เลือก **แค็ตตาล็อกการจัดซื้อใหม่** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="668fc-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="668fc-120">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="668fc-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="668fc-121">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="668fc-121">Select **OK**.</span></span>
5. <span data-ttu-id="668fc-122">ในแผนภูมิ ขยาย **ประเภทการจัดซื้อขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="668fc-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="668fc-123">ในแผนภูมิ ขยาย **เครื่องจักรสำนักงาน**</span><span class="sxs-lookup"><span data-stu-id="668fc-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="668fc-124">ในแผนภูมิ เลือก **คอมพิวเตอร์**</span><span class="sxs-lookup"><span data-stu-id="668fc-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="668fc-125">ผลิตภัณฑ์จากประเภทการจัดซื้อจะแสดงในรายการ </span><span class="sxs-lookup"><span data-stu-id="668fc-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="668fc-126">ถ้าคุณต้องการเพิ่มผลิตภัณฑ์ในประเภทที่คุณต้องการทำเช่นนี้ในหน้า **ประเภทการจัดซื้อตามลำดับชั้น** หรือในหน้า **รายละเอียดสินค้า**</span><span class="sxs-lookup"><span data-stu-id="668fc-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="668fc-127">ชนิดการปรับปรุง **เริ่มต้น** กำหนดว่าผลิตภัณฑ์ใหม่ที่ถูกเพิ่มลงในประเภทการจัดซื้อตามลำดับชั้นจะปรากฏทันทีในแค็ตตาล็อกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="668fc-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="668fc-128">ถ้าชนิดการปรับปรุงถูกตั้งค่าเป็น **ไดนามิก** การเปลี่ยนแปลงจะมองเห็นได้ในทันที</span><span class="sxs-lookup"><span data-stu-id="668fc-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="668fc-129">ถ้าชนิดการปรับปรุงเป็น **คงที่** ผลิตภัณฑ์ใหม่จะสามารถมองเห็นได้เฉพาะสำหรับผู้ที่ใช้แค็ตตาล็อกหลังจากที่แค็ตตาล็อกได้รับการเผยแพร่ใหม่</span><span class="sxs-lookup"><span data-stu-id="668fc-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="668fc-130">การดำเนินการ **เผยแพร่** จะพร้อมใช้งานบนบานหน้าต่างการดำเนินการที่อยู่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="668fc-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="668fc-131">ถ้าผลิตภัณฑ์ถูกลบออกจากประเภทการจัดซื้อตามลำดับชั้น การเปลี่ยนแปลงจะปรากฏทันที โดยไม่คำนึงถึงค่าในฟิลด์ชนิดการปรับปรุง **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="668fc-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="668fc-132">ในบานหน้าต่างการดำเนินการ ให้เลือก **ประเภทการนำทาง** และตรวจสอบให้แน่ใจว่ามีการเลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="668fc-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="668fc-133">เลือก **เรียกใช้แค็ตตาล็อก**</span><span class="sxs-lookup"><span data-stu-id="668fc-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="668fc-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="668fc-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="668fc-135">กำหนดให้เรียกดูแค็ตตาล็อกได้</span><span class="sxs-lookup"><span data-stu-id="668fc-135">Make the catalog visible</span></span>
1. <span data-ttu-id="668fc-136">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดซื้อและการจัดหา > การตั้งค่า > นโยบาย > นโยบายการจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="668fc-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="668fc-137">เลือก **นโยบายการจัดซื้อ USMF**</span><span class="sxs-lookup"><span data-stu-id="668fc-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="668fc-138">คุณต้องเลือกนโยบายการจัดซื้อสำหรับนิติบุคคลที่ผู้ปฏิบัติงานเชื่อมโยงกับโพรไฟล์ผู้ใช้ของคุณได้รับอนุญาตให้สั่งผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="668fc-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="668fc-139">ในข้อมูลสาธิต USMF ผู้ดูแลระบบจะถูกเชื่อมต่อกับผู้ปฏิบัติงานที่ชื่อว่า **Julia Funderburk** และเธอจะสั่งผลิตภัณฑ์ใน USMF ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="668fc-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="668fc-140">เลือกแค็ตตาล็อกที่คุณเพิ่งสร้าง</span><span class="sxs-lookup"><span data-stu-id="668fc-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="668fc-141">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="668fc-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="668fc-142">ใช้แค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="668fc-142">Use the catalog</span></span>
1. <span data-ttu-id="668fc-143">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดซื้อและการจัดหา > ใบขอซื้อ > ใบขอซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="668fc-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="668fc-144">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="668fc-144">Select **New**.</span></span>
3. <span data-ttu-id="668fc-145">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="668fc-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="668fc-146">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="668fc-146">Select **OK**.</span></span>
5. <span data-ttu-id="668fc-147">เลือก **เพิ่มผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="668fc-147">Select **Add products**.</span></span>
6. <span data-ttu-id="668fc-148">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="668fc-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="668fc-149">คุณสามารถใช้ประเภทตามลำดับชั้นที่ด้านซ้ายหรือตัวกรองที่อยู่ด้านบนของรายการเพื่อกรองข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="668fc-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="668fc-150">เลือก **เพิ่มลงในรายการ**</span><span class="sxs-lookup"><span data-stu-id="668fc-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="668fc-151">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="668fc-151">Select **OK**.</span></span>

