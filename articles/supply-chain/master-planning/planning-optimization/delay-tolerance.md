---
title: การยอมรับความล่าช้า (วันค่าลบ)
description: หัวข้อนี้มีข้อมูลเกี่ยวกับการคํานวณการยอมรับความล่าช้าและมีผลกระทบต่อการสร้างแผนการใบสั่งในการเพิ่มประสิทธิภาพการวางแผน
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306474"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="45783-103">การยอมรับความล่าช้า (วันค่าลบ)</span><span class="sxs-lookup"><span data-stu-id="45783-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="45783-104">ฟังก์ชันการยอมรับความล่าช้าช่วยให้การเพิ่มประสิทธิภาพการวางแผนควรพิจารณาค่า **วันค่าลบ** ที่ตั้งค่าไว้ให้กับกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="45783-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="45783-105">ใช้เพื่อขยายรอบระยะเวลาการยอมรับความล่าช้าที่ใช้ในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="45783-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="45783-106">ด้วยวิธีนี้ คุณสามารถหลีกเลี่ยงการสร้างใบสั่งจัดหาวัสดุใหม่ได้ ถ้าการจัดหาวัสดุที่มีอยู่จะสามารถครอบคลุมความต้องการได้หลังจากความล่าช้าสั้นๆ</span><span class="sxs-lookup"><span data-stu-id="45783-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="45783-107">วัตถุประสงค์ของฟังก์ชันคือเพื่อระบุว่าควรสร้างใบสั่งจัดหาวัสดุใหม่ให้กับความต้องการที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="45783-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="45783-108">เปิดใช้งานคุณลักษณะการทำงานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="45783-108">Turn on the feature in your system</span></span>

<span data-ttu-id="45783-109">เมื่อต้องการให้ฟังก์ชันการยอมรับความล่าช้าพร้อมใช้งานในระบบของคุณ ให้ไปที่ [การจัดการคุณลักษณะ](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดใช้งานคุณลักษณะ *วันค่าลบสำหรับการเพิ่มประสิทธิภาพการวางแผน*</span><span class="sxs-lookup"><span data-stu-id="45783-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="45783-110">การยอมรับความล่าช้าในการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="45783-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="45783-111">การยอมรับความล่าช้าแสดงจํานวนวันที่นอกเหนือจากระยะเวลารอคอยสินค้าที่คุณเต็มใจรอก่อนที่คุณจะสั่งการเติมสินค้าใหม่เมื่อมีการวางแผนการจัดหาวัสดุที่มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="45783-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="45783-112">กําหนดการยอมรับความล่าช้าโดยใช้วันปฏิทิน ไม่ใช่วันธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="45783-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="45783-113">ในเวลาที่วางแผนหลัก เมื่อระบบคํานวณการยอมรับความล่าช้า จะถือว่ามีการตั้งค่า **วันค่าลบ**</span><span class="sxs-lookup"><span data-stu-id="45783-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="45783-114">คุณสามารถตั้งค่า **วันค่าลบ** ทั้งในหน้า **กลุ่มความครอบคลุม** หรือหน้า **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="45783-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="45783-115">ระบบเชื่อมโยงการคํานวณการยอมรับความล่าช้ากับ *วันที่เติมสินค้าแรกสุด* ซึ่งเท่ากับวันที่ของวันนี้บวกระยะเวลารอคอยสินค้า</span><span class="sxs-lookup"><span data-stu-id="45783-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="45783-116">การยอมรับความล่าช้าจะคํานวณโดยใช้สูตรต่อไปนี้ โดยที่ *max()* จะค้นหาค่ามากกว่าสองค่าดังนี้</span><span class="sxs-lookup"><span data-stu-id="45783-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="45783-117">*max(วันที่เติมสินค้าแรกสุด, วันที่ครบกําหนดของความต้องการ)* – *วันที่ครบกําหนดของความต้องการ* + *วันค่าลบ*</span><span class="sxs-lookup"><span data-stu-id="45783-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="45783-118">สูตรนี้ช่วยให้มั่นใจว่าการวางแผนหลักจะไม่สร้างใบสั่งจัดหาวัสดุใหม่ เมื่อมีการจัดหาวัสดุเพียงพอในระหว่างระยะเวลารอคอยผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45783-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="45783-119">การคํานวณการยอมรับความล่าช้าในการเพิ่มประสิทธิภาพการวางแผนจะใช้การคํานวณวันที่เป็นค่าลบแบบไดนามิกจากการวางแผนหลักในตัวเสมอ</span><span class="sxs-lookup"><span data-stu-id="45783-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="45783-120">การตั้งค่า **ใช้การตั้งค่าวันที่เป็นค่าลบแบบไดนามิก** บนหน้า **พารามิเตอร์การวางแผนหลัก** จะไม่มีผลกับลักษณะการทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="45783-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="45783-121">ถ้าการจัดหาวัสดุที่มีอยู่แสดงถึงความล่าช้าความต้องการที่น้อยกว่าหรือเท่ากับการยอมรับความล่าช้าที่คํานวณไว้ การเพิ่มประสิทธิภาพการวางแผนจะเชื่อมโยงการจัดหาวัสดุที่มีอยู่กับความต้องการ</span><span class="sxs-lookup"><span data-stu-id="45783-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="45783-122">ในบางกรณี การหน่วงเวลาความต้องการย่อมดีกว่าการจบด้วยการจัดหาวัสดุมากเกิน</span><span class="sxs-lookup"><span data-stu-id="45783-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="45783-123">ส่วนย่อยต่อไปนี้แสดงตัวอย่างที่แสดงความล่าช้าส่งผลกระทบต่อการสร้างแผนการใบสั่งในการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="45783-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="45783-124">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="45783-124">Example 1</span></span>

<span data-ttu-id="45783-125">ผลิตภัณฑ์มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45783-125">A product has the following configuration:</span></span>

- <span data-ttu-id="45783-126">**ระยะเวลารอคอยสินค้า:** *10*</span><span class="sxs-lookup"><span data-stu-id="45783-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="45783-127">**จำนวนวันค่าลบ:** *2*</span><span class="sxs-lookup"><span data-stu-id="45783-127">**Negative days:** *2*</span></span>

<span data-ttu-id="45783-128">มีการจัดหาวัสดุและความต้องการต่อไปนี้อยู่สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45783-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="45783-129">**ความต้องการวันนี้:** ใบสั่งขายสำหรับปริมาณเท่ากับ 10</span><span class="sxs-lookup"><span data-stu-id="45783-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="45783-130">**จัดหาวัสดุภายใน 12 วัน:** ใบสั่งซื้อสำหรับปริมาณเท่ากับ 10</span><span class="sxs-lookup"><span data-stu-id="45783-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="45783-131">การจัดหาวัสดุที่มีอยู่สามารถครอบคลุมความต้องการภายใน 12 วัน และรอบระยะเวลาดังกล่าวเท่ากับการยอมรับความล่าช้า</span><span class="sxs-lookup"><span data-stu-id="45783-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="45783-132">ดังนั้นจึงไม่มีการสร้างแผนการใบสั่งเมื่อรันการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="45783-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="45783-133">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="45783-133">Example 2</span></span>

<span data-ttu-id="45783-134">ผลิตภัณฑ์มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45783-134">A product has the following configuration:</span></span>

- <span data-ttu-id="45783-135">**ระยะเวลารอคอยสินค้า:** *10*</span><span class="sxs-lookup"><span data-stu-id="45783-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="45783-136">**จำนวนวันค่าลบ:** *0*</span><span class="sxs-lookup"><span data-stu-id="45783-136">**Negative days:** *0*</span></span>

<span data-ttu-id="45783-137">มีการจัดหาวัสดุและความต้องการต่อไปนี้อยู่สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45783-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="45783-138">**ความต้องการวันนี้:** ใบสั่งขายสำหรับปริมาณเท่ากับ 10</span><span class="sxs-lookup"><span data-stu-id="45783-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="45783-139">**จัดหาวัสดุภายใน 12 วัน:** ใบสั่งซื้อสำหรับปริมาณเท่ากับ 10</span><span class="sxs-lookup"><span data-stu-id="45783-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="45783-140">การจัดหาวัสดุที่มีอยู่สามารถครอบคลุมความต้องการได้หลังจาก 12 วันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="45783-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="45783-141">อย่างไรก็ตาม การยอมรับความล่าช้าคือ 10 วัน</span><span class="sxs-lookup"><span data-stu-id="45783-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="45783-142">ดังนั้นเมื่อการวางแผนหลักรัน แผนการใบสั่งปริมาณเท่ากับ 10 จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="45783-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="45783-143">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="45783-143">Example 3</span></span>

<span data-ttu-id="45783-144">ผลิตภัณฑ์มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45783-144">A product has the following configuration:</span></span>

- <span data-ttu-id="45783-145">**ระยะเวลารอคอยสินค้า:** *10*</span><span class="sxs-lookup"><span data-stu-id="45783-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="45783-146">**จำนวนวันค่าลบ:** *2*</span><span class="sxs-lookup"><span data-stu-id="45783-146">**Negative days:** *2*</span></span>

<span data-ttu-id="45783-147">มีการจัดหาวัสดุและความต้องการต่อไปนี้อยู่สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45783-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="45783-148">**ความต้องการใน 11 วัน:** ใบสั่งขายสำหรับปริมาณเท่ากับ 10</span><span class="sxs-lookup"><span data-stu-id="45783-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="45783-149">**จัดหาวัสดุภายใน 14 วัน:** ใบสั่งซื้อสำหรับปริมาณเท่ากับ 10</span><span class="sxs-lookup"><span data-stu-id="45783-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="45783-150">การจัดหาวัสดุที่มีอยู่สามารถครอบคลุมความต้องการได้หลังจากสามวันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="45783-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="45783-151">อย่างไรก็ตาม การยอมรับความล่าช้าคือสองวัน</span><span class="sxs-lookup"><span data-stu-id="45783-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="45783-152">(ในกรณีนี้ การยอมรับความล่าช้าจะรวมเฉพาะสองวันที่ติดลบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="45783-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="45783-153">วันที่ความต้องการไม่ได้รวมอยู่ด้วย เนื่องจากอยู่หลังจากระยะเวลารอคอยผลิตภัณฑ์) ดังนั้นเมื่อการวางแผนหลักรัน แผนการใบสั่งปริมาณเท่ากับ 10 จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="45783-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
