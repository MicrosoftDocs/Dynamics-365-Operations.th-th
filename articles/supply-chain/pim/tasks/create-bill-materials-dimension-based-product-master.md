---
title: สร้างสูตรการผลิตสำหรับผลิตภัณฑ์หลักตามมิติ
description: 'สำหรับกระบวนงานนี้ คุณควรดำเนินงานคู่มือ 4 รายการก่อนหน้าให้เสร็จสมบูรณ์แล้วในลำดับของการบันทึกแปดรายการ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920716"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="ff820-103">สร้างสูตรการผลิตสำหรับผลิตภัณฑ์หลักตามมิติ</span><span class="sxs-lookup"><span data-stu-id="ff820-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff820-104">สำหรับกระบวนงานนี้ คุณควรดำเนินงานคู่มือ 4 รายการก่อนหน้าให้เสร็จสมบูรณ์แล้วในลำดับของการบันทึกแปดรายการ </span><span class="sxs-lookup"><span data-stu-id="ff820-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="ff820-105">การบันทึก 4 รายการแรกจะตั้งค่าข้อมูลที่ต้องการเพื่อดำเนินกระบวนงานนี้ให้สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ff820-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="ff820-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="ff820-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ff820-107">โดยทั่วไปงานนี้จะถูกจัดการโดยผู้ออกแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ff820-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="ff820-108">เลือกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ff820-108">Select the product</span></span>

1. <span data-ttu-id="ff820-109">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="ff820-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ff820-110">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff820-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ff820-111">หาผลิตภัณฑ์หลักที่ได้นำออกใช้ ซึ่งมีเทคโนโลยีการจัดโครงแบบตามมิติ ที่คุณสร้างขึ้นในคู่มืองานแรกในลำดับงานนี้</span><span class="sxs-lookup"><span data-stu-id="ff820-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="ff820-112">บนบานหน้าต่างการดำเนินการ เลือก **วิศวกร**</span><span class="sxs-lookup"><span data-stu-id="ff820-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="ff820-113">เลือก **รุ่น BOM**</span><span class="sxs-lookup"><span data-stu-id="ff820-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="ff820-114">สร้าง BOM และเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="ff820-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="ff820-115">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ff820-115">Select **New**.</span></span>
1. <span data-ttu-id="ff820-116">เลือก **BOM และรุ่น BOM**</span><span class="sxs-lookup"><span data-stu-id="ff820-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="ff820-117">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff820-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="ff820-118">การตั้งค่าไซต์</span><span class="sxs-lookup"><span data-stu-id="ff820-118">Setting a site</span></span>  
    * <span data-ttu-id="ff820-119">ในกระบวนงานนี้ เราไม่ตั้งค่าไซต์เฉพาะสำหรับ BOM</span><span class="sxs-lookup"><span data-stu-id="ff820-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="ff820-120">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ff820-120">Select **OK**.</span></span>
1. <span data-ttu-id="ff820-121">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ff820-121">Select **New**.</span></span>
    * <span data-ttu-id="ff820-122">ในกระบวนงานนี้ เราจะเพิ่มรายการสี่รายการไปยัง BOM </span><span class="sxs-lookup"><span data-stu-id="ff820-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="ff820-123">สองรายการจะแสดงตัวเลือกเคเบิล และอีกสองรายการจะแสดงตัวเลือก cabinet</span><span class="sxs-lookup"><span data-stu-id="ff820-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="ff820-124">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff820-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ff820-125">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff820-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="ff820-126">เลือกหมายเลขสินค้า เคเบิล A0001 HDMI 6'</span><span class="sxs-lookup"><span data-stu-id="ff820-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="ff820-127">ในฟิลด์ **กลุ่มการตั้งค่าคอนฟิก** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff820-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="ff820-128">เลือกกลุ่มการตั้งค่าคอนฟิกเคเบิลที่สร้างไว้ในคู่มือ 4 ในลำดับงานนี้</span><span class="sxs-lookup"><span data-stu-id="ff820-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="ff820-129">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ff820-129">Select **New**.</span></span>
    * <span data-ttu-id="ff820-130">เลือกหมายเลขสินค้า เคเบิล A0002 HDMI 12'</span><span class="sxs-lookup"><span data-stu-id="ff820-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="ff820-131">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff820-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ff820-132">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff820-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="ff820-133">ในฟิลด์ **กลุ่มการตั้งค่าคอนฟิก** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff820-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="ff820-134">เลือกกลุ่มการตั้งค่าคอนฟิกเคเบิลอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ff820-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="ff820-135">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ff820-135">Select **New**.</span></span>
1. <span data-ttu-id="ff820-136">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff820-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ff820-137">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff820-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="ff820-138">เลือกหมายเลขสินค้า Cabinet D0002</span><span class="sxs-lookup"><span data-stu-id="ff820-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="ff820-139">ในฟิลด์ **กลุ่มการตั้งค่าคอนฟิก** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff820-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="ff820-140">เลือกกลุ่มการตั้งค่าคอนฟิก Cabinet สำหรับรายการ BOM นี้</span><span class="sxs-lookup"><span data-stu-id="ff820-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="ff820-141">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ff820-141">Select **New**.</span></span>
1. <span data-ttu-id="ff820-142">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff820-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ff820-143">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff820-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="ff820-144">เลือกหมายเลขสินค้า StandardCabinet M0007 ให้เป็นรายการ BOM สุดท้าย</span><span class="sxs-lookup"><span data-stu-id="ff820-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="ff820-145">ในฟิลด์ **กลุ่มการตั้งค่าคอนฟิก** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff820-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="ff820-146">เลือกกลุ่มการตั้งค่าคอนฟิก Cabinet สำหรับรายการ BOM สุดท้าย</span><span class="sxs-lookup"><span data-stu-id="ff820-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="ff820-147">อนุมัติและเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="ff820-147">Approve and activate</span></span>

1. <span data-ttu-id="ff820-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ff820-148">Close the page.</span></span>
1. <span data-ttu-id="ff820-149">เลือก **อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="ff820-149">Select **Approve**.</span></span>
1. <span data-ttu-id="ff820-150">ในฟิลด์ **อนุมัติโดย** ให้ป้อน หรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff820-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="ff820-151">เลือก *ใช่* ในฟิลด์ **คุณยังต้องการอนุมัติสูตรการผลิตด้วยหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="ff820-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="ff820-152">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ff820-152">Select **OK**.</span></span>
1. <span data-ttu-id="ff820-153">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="ff820-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]