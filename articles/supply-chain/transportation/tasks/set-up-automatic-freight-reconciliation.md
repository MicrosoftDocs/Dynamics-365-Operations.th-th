---
title: ตั้งค่าการกระทบยอดค่าขนส่งโดยอัตโนมัติ
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าข้อมูลสำหรับการกระทบยอดการขนส่งโดยอัตโนมัติ '
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 057d1b3a1b5294c75f02f4ed443ae6f525ac6b83
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837625"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="ef11f-103">ตั้งค่าการกระทบยอดค่าขนส่งโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ef11f-103">Set up automatic freight reconciliation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef11f-104">กระบวนงานนี้แสดงวิธีการตั้งค่าข้อมูลสำหรับการกระทบยอดการขนส่งโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="ef11f-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="ef11f-105">ซึ่งปกติจะดำเนินการโดยผู้จัดการคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="ef11f-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="ef11f-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="ef11f-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="ef11f-107">ตั้งค่าชนิดการกระทบยอดบิลค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="ef11f-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="ef11f-108">ไปที่ การจัดการการขนส่ง > การตั้งค่า > การกระทบยอดการขนส่ง > ชนิดบิลการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="ef11f-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="ef11f-109">ชนิดบิลการขนส่งจะกำหนดว่าควรจับคู่บิลการขนส่งและใบแจ้งหนี้ของผู้ขนส่งอย่างไร</span><span class="sxs-lookup"><span data-stu-id="ef11f-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="ef11f-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ef11f-110">Click New.</span></span>
3. <span data-ttu-id="ef11f-111">ในฟิลด์ชนิดบิลการขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ef11f-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="ef11f-112">ในฟิลด์แอสเซมบลีกลไกจัดการ พิมพ์ 'Microsoft.Dynamics.Ax.Tms.dll'</span><span class="sxs-lookup"><span data-stu-id="ef11f-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="ef11f-113">นี่คือไลบรารีรหัสกลไกการจับคู่การจัดการการขนส่งมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ef11f-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="ef11f-114">ในคลาสแอสเซมบลีกลไกจัดการ พิมพ์ 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'</span><span class="sxs-lookup"><span data-stu-id="ef11f-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="ef11f-115">นี่คือคลาสกลไกการจับคู่การจัดการการขนส่งมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ef11f-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="ef11f-116">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ef11f-116">Click New.</span></span>
7. <span data-ttu-id="ef11f-117">ในฟิลด์คำอธิบาย เลือกค่าที่ควรตรงกับในบิลการขนส่งและใบแจ้งหนี้ของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="ef11f-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="ef11f-118">ในฟิลด์ ต้องตรงกัน เลือก 'ใช่'</span><span class="sxs-lookup"><span data-stu-id="ef11f-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="ef11f-119">ถ้าคุณกำหนดฟิลด์นี้เป็น ใช่ หมายความว่าค่าที่เลือกไว้ในฟิลด์คำอธิบายจะต้องตรงกับทั้งบิลการขนส่งและใบแจ้งหนี้ของผู้ขนส่ง </span><span class="sxs-lookup"><span data-stu-id="ef11f-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="ef11f-120">ถ้าคุณตั้งค่าเป็น ไม่ ฟิลด์ใดฟิลด์หนึ่งอาจเว้นว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="ef11f-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="ef11f-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ef11f-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="ef11f-122">ตั้งค่าการกำหนดชนิดบิลค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="ef11f-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="ef11f-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ef11f-123">Close the page.</span></span>
2. <span data-ttu-id="ef11f-124">ไปที่ การจัดการการขนส่ง > การตั้งค่า > การกระทบยอดการขนส่ง > การกำหนดชนิดบิลการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="ef11f-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="ef11f-125">การกำหนดชนิดบิลการขนส่งจะถูกใช้ในการระบุชนิดบิลการขนส่งที่ใช้สำหรับผู้ขนส่งที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="ef11f-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="ef11f-126">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ef11f-126">Click New.</span></span>
4. <span data-ttu-id="ef11f-127">ในฟิลด์โหมด ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ef11f-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="ef11f-128">ในฟิลด์ผู้ขนส่งสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ef11f-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="ef11f-129">ในฟิลด์ชนิดการขนส่ง เลือกชนิดการขนส่งที่คุณสร้างขึ้นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="ef11f-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="ef11f-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ef11f-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="ef11f-131">ตั้งค่าต้นแบบการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="ef11f-131">Set up the audit master</span></span>
1. <span data-ttu-id="ef11f-132">ไปที่ การจัดการการขนส่ง > การตั้งค่า > การกระทบยอดการขนส่ง > ต้นแบบการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="ef11f-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="ef11f-133">ต้นแบบการตรวจสอบจะกำหนดขีดจำกัดการยอมรับสำหรับการกระทบยอดการขนส่งโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="ef11f-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="ef11f-134">ซึ่งจะระบุว่ายอดเงินในบิลการขนส่งและใบแจ้งหนี้ของผู้ขนส่งสามารถแตกต่างกันได้เท่าไหร่ และยังอนุญาตให้มีการกระทบยอดเกิดขึ้นได้ </span><span class="sxs-lookup"><span data-stu-id="ef11f-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="ef11f-135">นอกจากนี้ยังกำหนดวิธีการจัดการความขัดแย้งอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="ef11f-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="ef11f-136">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ef11f-136">Click New.</span></span>
3. <span data-ttu-id="ef11f-137">ในฟิลด์รหัสต้นแบบการตรวจสอบ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ef11f-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="ef11f-138">ในฟิลด์ผู้ขนส่งสินค้า เลือกผู้ขนส่งสินค้าเดียวกับที่คุณเลือกก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="ef11f-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="ef11f-139">ในฟิลด์ชนิดการขนส่ง เลือกชนิดการขนส่งที่คุณสร้างขึ้นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="ef11f-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="ef11f-140">ขยายส่วน ขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="ef11f-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="ef11f-141">ในฟิลด์ระดับขีดจำกัดต่ำสุด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ef11f-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="ef11f-142">ในฟิลด์ระดับขีดจำกัดสูงสุด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ef11f-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="ef11f-143">ขยายส่วน ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="ef11f-143">Expand the Result section.</span></span>
10. <span data-ttu-id="ef11f-144">ในฟิลด์เหตุผลการชำระมากเกิน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ef11f-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="ef11f-145">ถ้ายอดเงินในบิลการขนส่งและใบแจ้งหนี้ของผู้ขนส่งแตกต่างกัน รหัสเหตุผลของการชำระมากเกินหรือน้อยเกินจะระบุบัญชีที่ควรลงทะเบียนความแตกต่าง ถ้าผลต่างอยู่ภายในระดับขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="ef11f-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="ef11f-146">ในฟิลด์เหตุผลการชำระน้อยเกิน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ef11f-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="ef11f-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ef11f-147">Close the page.</span></span>

