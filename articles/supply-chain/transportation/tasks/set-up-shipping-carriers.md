---
title: ตั้งค่าผู้ขนส่ง
description: หัวข้อนี้แสดงวิธีการตั้งค่าผู้ขนส่งสินค้าและกำหนดรายละเอียด เช่น บริการ โหมดการจัดส่ง วิธีการชำระเงินการขนส่ง ข้อจำกัดขนส่ง และอัตราการจัดส่ง
author: ShylaThompson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c292470e6c70af4dfe11bbe324ebcf93438e29d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840472"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="8e5cd-103">ตั้งค่าผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e5cd-104">หัวข้อนี้แสดงวิธีการตั้งค่าผู้ขนส่งสินค้าและกำหนดรายละเอียด เช่น บริการ โหมดการจัดส่ง วิธีการชำระเงินการขนส่ง ข้อจำกัดขนส่ง และอัตราการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="8e5cd-105">ผู้ประสานงานขนส่งสามารถกำหนดผู้ขนส่งสินค้าทั้งโหลดขาเข้าหรือขาออก</span><span class="sxs-lookup"><span data-stu-id="8e5cd-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="8e5cd-106">สร้างผู้ขนส่งสินค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="8e5cd-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="8e5cd-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการการขนส่ง > การตั้งค่า > ผู้ขนส่ง > ผู้ขนส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="8e5cd-108">เลือก **สร้าง** บนหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="8e5cd-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="8e5cd-109">ในฟิลด์ **ผู้ขนส่งสินค้า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="8e5cd-110">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="8e5cd-111">ในฟิลด์ **โหมด** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="8e5cd-112">กรอกข้อมูลทั่วไปสำหรับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="8e5cd-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="8e5cd-113">สลับการขยายของส่วน **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="8e5cd-114">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **เรียกใช้ผู้ขนส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="8e5cd-115">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="8e5cd-116">เลือกบัญชีผู้จัดจำหน่ายเพื่อมอบหมายให้กับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="8e5cd-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="8e5cd-117">ในฟิลด์ **ชนิดการชำระเงินการขนส่ง** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8e5cd-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="8e5cd-118">เลือก **ด้วยตัวเอง** เพื่อใช้หน้าวิธีการชำระเงินการขนส่ง หรือเลือก **EDI** เพื่อปรับปรุงการชำระเงินโดยใช้การแลกเปลี่ยนข้อมูลทางอิเล็กทรอนิกส์ (EDI)</span><span class="sxs-lookup"><span data-stu-id="8e5cd-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="8e5cd-119">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **เรียกใช้การจัดอันดับของผู้ขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="8e5cd-120">สร้างบริการที่จำเป็นสำหรับการขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="8e5cd-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="8e5cd-121">สลับการขยายของส่วน **บริการ**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="8e5cd-122">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-122">Select **New**.</span></span>
3. <span data-ttu-id="8e5cd-123">ในฟิลด์ **บริการขนส่ง** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="8e5cd-124">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="8e5cd-125">ในฟิลด์ **วิธีการขนส่ง** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="8e5cd-126">ตั้งค่าอยู่สำหรับผู้ขนส่ง (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="8e5cd-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="8e5cd-127">สลับการขยายของส่วน **ที่อยู่**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="8e5cd-128">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-128">Select **New**.</span></span>
3. <span data-ttu-id="8e5cd-129">ในฟิลด์ **ชื่อหรือคำอธิบาย** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8e5cd-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="8e5cd-130">ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="8e5cd-131">ในฟิลด์ **รหัสไปรษณีย์** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="8e5cd-132">ในฟิลด์ **ถนน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="8e5cd-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="8e5cd-134">ตั้งค่าโพรไฟล์การจัดอันดับสำหรับผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="8e5cd-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="8e5cd-135">สลับการขยายของส่วน **การจัดอันดับโพรไฟล์**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="8e5cd-136">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-136">Select **New**.</span></span>
3. <span data-ttu-id="8e5cd-137">ในฟิลด์ **การจัดอันดับโพรไฟล์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8e5cd-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="8e5cd-138">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="8e5cd-139">ในฟิลด์ **ไซต์** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="8e5cd-140">ในฟิลด์ **คลังสินค้า** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="8e5cd-141">ในฟิลด์ **กลไกจัดการอัตรา** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="8e5cd-142">เลือกกลไกจัดการอัตราที่สอดคล้องกับสัญญากับผู้ขนส่งที่คุณมี</span><span class="sxs-lookup"><span data-stu-id="8e5cd-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="8e5cd-143">ในฟิลด์ **ต้นแบบอัตรา** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="8e5cd-144">ในฟิลด์ **กลไกจัดการเวลาในการส่งต่อ** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8e5cd-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="8e5cd-145">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-145">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]