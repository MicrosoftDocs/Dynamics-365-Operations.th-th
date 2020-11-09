---
title: ตั้งค่าผู้ขนส่ง
description: หัวข้อนี้แสดงวิธีการตั้งค่าผู้ขนส่งสินค้าและกำหนดรายละเอียด เช่น บริการ โหมดการจัดส่ง วิธีการชำระเงินการขนส่ง ข้อจำกัดขนส่ง และอัตราการจัดส่ง
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a71ea3983018b136d4fe3b22eadc0c332d2a698
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016458"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="c23ff-103">ตั้งค่าผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="c23ff-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c23ff-104">หัวข้อนี้แสดงวิธีการตั้งค่าผู้ขนส่งสินค้าและกำหนดรายละเอียด เช่น บริการ โหมดการจัดส่ง วิธีการชำระเงินการขนส่ง ข้อจำกัดขนส่ง และอัตราการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="c23ff-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="c23ff-105">ผู้ประสานงานขนส่งสามารถกำหนดผู้ขนส่งสินค้าทั้งโหลดขาเข้าหรือขาออก</span><span class="sxs-lookup"><span data-stu-id="c23ff-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="c23ff-106">สร้างผู้ขนส่งสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="c23ff-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="c23ff-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการการขนส่ง > การตั้งค่า > ผู้ขนส่ง > ผู้ขนส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="c23ff-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="c23ff-108">เลือก **สร้าง** บนหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="c23ff-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="c23ff-109">ในฟิลด์ **ผู้ขนส่งสินค้า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c23ff-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="c23ff-110">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c23ff-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c23ff-111">ในฟิลด์ **โหมด** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c23ff-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="c23ff-112">กรอกข้อมูลทั่วไปสำหรับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="c23ff-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="c23ff-113">สลับการขยายของส่วน **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="c23ff-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="c23ff-114">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **เรียกใช้ผู้ขนส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="c23ff-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="c23ff-115">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c23ff-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="c23ff-116">เลือกบัญชีผู้จัดจำหน่ายเพื่อมอบหมายให้กับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="c23ff-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="c23ff-117">ในฟิลด์ **ชนิดการชำระเงินการขนส่ง** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c23ff-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="c23ff-118">เลือก **ด้วยตัวเอง** เพื่อใช้หน้าวิธีการชำระเงินการขนส่ง หรือเลือก **EDI** เพื่อปรับปรุงการชำระเงินโดยใช้การแลกเปลี่ยนข้อมูลทางอิเล็กทรอนิกส์ (EDI)</span><span class="sxs-lookup"><span data-stu-id="c23ff-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="c23ff-119">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **เรียกใช้การจัดอันดับของผู้ขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="c23ff-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="c23ff-120">สร้างบริการที่จำเป็นสำหรับการขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="c23ff-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="c23ff-121">สลับการขยายของส่วน **บริการ**</span><span class="sxs-lookup"><span data-stu-id="c23ff-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="c23ff-122">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c23ff-122">Select **New**.</span></span>
3. <span data-ttu-id="c23ff-123">ในฟิลด์ **บริการขนส่ง** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c23ff-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="c23ff-124">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c23ff-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c23ff-125">ในฟิลด์ **วิธีการขนส่ง** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c23ff-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="c23ff-126">ตั้งค่าอยู่สำหรับผู้ขนส่ง (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="c23ff-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="c23ff-127">สลับการขยายของส่วน **ที่อยู่**</span><span class="sxs-lookup"><span data-stu-id="c23ff-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="c23ff-128">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c23ff-128">Select **New**.</span></span>
3. <span data-ttu-id="c23ff-129">ในฟิลด์ **ชื่อหรือคำอธิบาย** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c23ff-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="c23ff-130">ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c23ff-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="c23ff-131">ในฟิลด์ **รหัสไปรษณีย์** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c23ff-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="c23ff-132">ในฟิลด์ **ถนน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c23ff-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="c23ff-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c23ff-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="c23ff-134">ตั้งค่าโพรไฟล์การจัดอันดับสำหรับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="c23ff-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="c23ff-135">สลับการขยายของส่วน **การจัดอันดับโพรไฟล์**</span><span class="sxs-lookup"><span data-stu-id="c23ff-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="c23ff-136">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c23ff-136">Select **New**.</span></span>
3. <span data-ttu-id="c23ff-137">ในฟิลด์ **การจัดอันดับโพรไฟล์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c23ff-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="c23ff-138">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c23ff-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c23ff-139">ในฟิลด์ **ไซต์** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c23ff-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="c23ff-140">ในฟิลด์ **คลังสินค้า** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c23ff-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="c23ff-141">ในฟิลด์ **กลไกจัดการอัตรา** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c23ff-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="c23ff-142">เลือกกลไกจัดการอัตราที่สอดคล้องกับสัญญากับผู้ขนส่งที่คุณมี</span><span class="sxs-lookup"><span data-stu-id="c23ff-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="c23ff-143">ในฟิลด์ **ต้นแบบอัตรา** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c23ff-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="c23ff-144">ในฟิลด์ **กลไกจัดการเวลาในการส่งต่อ** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="c23ff-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="c23ff-145">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c23ff-145">Select **Save**.</span></span>

