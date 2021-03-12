---
title: เชื่อมโยงดัชนีเชื้อเพลิงกับผู้ขนส่งเป็นค่าธรรมเนียมอุปกรณ์เสริม
description: คำแนะนำนี้แสดงวิธีการสร้างการกำหนดอุปกรณ์เสริม ค่าธรรมเนียมอุปกรณ์เสริมผู้ขนส่ง ต้นแบบอุปกรณ์เสริมสำหรับค่าธรรมเนียมเชื้อเพลิง และเชื่อมโยงกับดัชนีเชื้อเพลิงของผู้ขนส่งกับผู้ขนส่ง
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f69a6350a5a84ed19dcb37e174c25b112c16bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974146"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="5b99d-103">เชื่อมโยงดัชนีเชื้อเพลิงกับผู้ขนส่งเป็นค่าธรรมเนียมอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="5b99d-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b99d-104">คำแนะนำนี้แสดงวิธีการสร้างการกำหนดอุปกรณ์เสริม ค่าธรรมเนียมอุปกรณ์เสริมผู้ขนส่ง ต้นแบบอุปกรณ์เสริมสำหรับค่าธรรมเนียมเชื้อเพลิง และเชื่อมโยงกับดัชนีเชื้อเพลิงของผู้ขนส่งกับผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="5b99d-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="5b99d-105">คุณต้องมีการตั้งค่าดัชนีเชื้อเพลิงของผู้ขนส่งก่อนที่คุณรันคำแนะนำนี้</span><span class="sxs-lookup"><span data-stu-id="5b99d-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="5b99d-106">คุณสามารถใช้คำแนะนำ "ตั้งค่าดัชนีเชื้อเพลิงของผู้ขนส่ง" เพื่อดำเนินการนี้</span><span class="sxs-lookup"><span data-stu-id="5b99d-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="5b99d-107">การตั้งค่าเหล่านี้มักจะกระทำโดยผู้จัดการลอจิสติกส์ </span><span class="sxs-lookup"><span data-stu-id="5b99d-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="5b99d-108">ข้อมูลสาธิตที่เคยสร้างขั้นตอนนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="5b99d-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="5b99d-109">สร้างต้นแบบอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="5b99d-109">Create an accessorial master</span></span>
1. <span data-ttu-id="5b99d-110">ไปที่การจัดการการขนส่ง > การตั้งค่า > การจัดอันดับ > ต้นแบบอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="5b99d-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="5b99d-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b99d-111">Click New.</span></span>
3. <span data-ttu-id="5b99d-112">ในฟิลด์ต้นแบบอุปกรณ์เสริม ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5b99d-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="5b99d-113">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="5b99d-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5b99d-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="5b99d-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="5b99d-115">สร้างค่าธรรมเนียมอุปกรณ์เสริมของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="5b99d-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="5b99d-116">ไปที่การจัดการการขนส่ง > การตั้งค่า > การจัดอันดับ > ค่าธรรมเนียมอุปกรณ์เสริมของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="5b99d-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="5b99d-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b99d-117">Click New.</span></span>
3. <span data-ttu-id="5b99d-118">ในฟิลด์ ID อุปกรณ์เสริมของผู้ขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5b99d-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="5b99d-119">ในฟิลด์ผู้ขนส่งสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5b99d-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5b99d-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5b99d-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5b99d-121">ในตัวอย่างนี้ เลือกผู้ขนส่งโดยรถบรรทุก</span><span class="sxs-lookup"><span data-stu-id="5b99d-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="5b99d-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5b99d-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5b99d-123">ในฟิลด์การบริการผู้ขนส่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5b99d-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5b99d-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5b99d-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5b99d-125">ในฟิลด์ต้นแบบอุปกรณ์เสริม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5b99d-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="5b99d-126">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5b99d-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5b99d-127">ในตัวอย่างนี้ เลือกต้นแบบอุปกรณ์เสริมที่เพิ่งสร้างขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="5b99d-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="5b99d-128">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="5b99d-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="5b99d-129">สร้างการกำหนดอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="5b99d-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="5b99d-130">คลิกการกำหนดอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="5b99d-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="5b99d-131">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b99d-131">Click New.</span></span>
3. <span data-ttu-id="5b99d-132">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="5b99d-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="5b99d-133">สลับการขยายส่วนเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="5b99d-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="5b99d-134">ในเกณฑ์นี้ คุณสามารถเลือกได้ว่าจะใช้ค่าธรรมเนียมเชื้อเพลิงเสมอหรือสำหรับตัวอย่างนี้เลือกว่าจะใช้เฉพาะภายในภูมิภาคที่แน่นอน</span><span class="sxs-lookup"><span data-stu-id="5b99d-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="5b99d-135">ในฟิลด์รหัสไปรษณีย์จาก ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5b99d-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="5b99d-136">ในฟิลด์รหัสไปรษณีย์ถึง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="5b99d-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="5b99d-137">สลับการขยายส่วนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="5b99d-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="5b99d-138">ในส่วนการคำนวณ คุณสามารถระบุวิธีการคำนวณค่าธรรมเนียมเชื้อเพลิง </span><span class="sxs-lookup"><span data-stu-id="5b99d-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="5b99d-139">การคำนวณนี้ขึ้นอยู่กับหน่วยอุปกรณ์เสริมที่คุณเลือกให้เป็นฐานสำหรับการคำนวณของคุณ</span><span class="sxs-lookup"><span data-stu-id="5b99d-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="5b99d-140">ในฟิลด์ชนิดค่าธรรมเนียมอุปกรณ์เสริม ให้เลือก 'ค่าธรรมเนียมเชื้อเพลิง'</span><span class="sxs-lookup"><span data-stu-id="5b99d-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="5b99d-141">ในฟิลด์หน่วยอุปกรณ์เสริม ให้เลือก 'ไมล์เลจ'</span><span class="sxs-lookup"><span data-stu-id="5b99d-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="5b99d-142">ในฟิลด์ภูมิภาค ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5b99d-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5b99d-143">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5b99d-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="5b99d-144">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="5b99d-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="5b99d-145">อัพเดตโพรไฟล์การจัดอันดับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="5b99d-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="5b99d-146">ไปที่การจัดการการขนส่ง > การตั้งค่า > ผู้ขนส่ง > ผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="5b99d-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="5b99d-147">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5b99d-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5b99d-148">สลับการขยายส่วนของการจัดอันดับโพรไฟล์</span><span class="sxs-lookup"><span data-stu-id="5b99d-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="5b99d-149">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="5b99d-149">Click Edit.</span></span>
5. <span data-ttu-id="5b99d-150">ในฟิลด์ดัชนีเชื้อเพลิงของผู้ขนส่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5b99d-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5b99d-151">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5b99d-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5b99d-152">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="5b99d-152">Click Save.</span></span>

