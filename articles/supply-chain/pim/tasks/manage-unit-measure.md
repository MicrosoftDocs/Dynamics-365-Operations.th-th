---
title: จัดการหน่วยวัด
description: หัวข้อนี้อธิบายวิธีการกำหนดหน่วยวัด ระบุการแปลและคำอธิบายสำหรับหน่วย และกำหนดกฎการแปลงสำหรับหน่วยที่เกี่ยวข้อง
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921352"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="800dc-103">จัดการหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="800dc-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="800dc-104">หัวข้อนี้อธิบายวิธีการกำหนดหน่วยวัด ระบุการแปลและคำอธิบายสำหรับหน่วย และกำหนดกฎการแปลงสำหรับหน่วยที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="800dc-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="800dc-105">เปิดหน้าหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="800dc-105">Open the Units page</span></span>

<span data-ttu-id="800dc-106">เมื่อต้องการสร้างและใช้งานหน่วยวัดที่พร้อมใช้งานในระบบของคุณ ให้ไปที่ **การจัดการองค์กร \> การตั้งค่า \> หน่วย \> หน่วย**</span><span class="sxs-lookup"><span data-stu-id="800dc-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="800dc-107">ส่วนที่เหลือของหัวข้อนี้อธิบายสิ่งที่คุณสามารถบนหน้า **หน่วย**</span><span class="sxs-lookup"><span data-stu-id="800dc-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="800dc-108">สร้างหน่วยมาตรฐานและการแปลง</span><span class="sxs-lookup"><span data-stu-id="800dc-108">Create standard units and conversions</span></span>

<span data-ttu-id="800dc-109">ถ้าระบบของคุณยังไม่ได้รวมหน่วยวัดที่ใช้กันมากที่สุดในระบบเมตริกและ/หรือระบบตามศุลกากรของสหรัฐอเมริกา (USCS) วิซาร์ดการตั้งค่าหน่วยสามารถช่วยคุณในการเริ่มต้นข้อมูลพื้นฐานของหน่วยและการแปลงข้อมูลอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="800dc-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="800dc-110">หากต้องการเสร็จสิ้นวิซาร์ด ให้เลือก **วิซาร์ดการสร้างหน่วย** ในบานหน้าต่างการดำเนินการ แล้วปฏิบัติตามคําแนะนําบนหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="800dc-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="800dc-111">สร้างหรือแก้ไขหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="800dc-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="800dc-112">หากต้องการสร้างหรือแก้ไขหน่วยวัด ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="800dc-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="800dc-113">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="800dc-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="800dc-114">เมื่อต้องการแก้ไขหน่วยที่มีอยู่ ให้เลือกหน่วยในบานหน้าต่างรายการ</span><span class="sxs-lookup"><span data-stu-id="800dc-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="800dc-115">หากต้องการสร้างหน่วยใหม่ เลือก **สร้าง** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="800dc-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="800dc-116">บนส่วนหัวของเรกคอร์ด ให้ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="800dc-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="800dc-117">**หน่วย** – ป้อนรหัสหรือสัญลักษณ์ที่จะใช้เพื่ออ้างอิงถึงหน่วยในภาษาของระบบ</span><span class="sxs-lookup"><span data-stu-id="800dc-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="800dc-118">รหัสหรือสัญลักษณ์นี้โดยปกติแล้วจะเป็นตัวย่อทั่วไปที่ใช้กับหน่วย เช่น *ea* ของแต่ละชิ้น หรือ *cm* เป็นเซนติเมตร</span><span class="sxs-lookup"><span data-stu-id="800dc-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="800dc-119">**คำอธิบาย** – ป้อนชื่ออธิบายสำหรับหน่วยในภาษาของระบบ</span><span class="sxs-lookup"><span data-stu-id="800dc-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="800dc-120">โดยปกติชื่อนี้จะเป็นชื่อเต็มของหน่วย เช่น *แต่ละ* หรือ *เซนติเมตร*</span><span class="sxs-lookup"><span data-stu-id="800dc-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="800dc-121">บน FastTab **ทั่วไป** ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="800dc-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="800dc-122">**คลาสหน่วย** – เลือกคุณสมบัติที่หน่วยวัด (เช่น ความยาว พื้นที่ มวล หรือปริมาณ)</span><span class="sxs-lookup"><span data-stu-id="800dc-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="800dc-123">**ระบบของหน่วย** – เลือกระบบการวัดที่หน่วยนี้เป็นสมาชิก (*หน่วยเมตริก* หรือ *หน่วยวัดตามศุลกากรของสหรัฐอเมริกา*)</span><span class="sxs-lookup"><span data-stu-id="800dc-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="800dc-124">**หน่วยพื้นฐาน** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อใช้หน่วยปัจจุบันเป็นหน่วยพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="800dc-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="800dc-125">ในกรณีนี้ คุณต้องระบุตัวแปลงหน่วยระหว่างหน่วยพื้นฐานและหน่วยเพิ่มเติมแต่ละหน่วยในคลาสของหน่วยเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="800dc-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="800dc-126">จากนั้นระบบจะสามารถแปลงระหว่างหน่วยทั้งหมดในคลาสหน่วยนั้น</span><span class="sxs-lookup"><span data-stu-id="800dc-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="800dc-127">ดังนั้น คุณจึงควรตั้งค่าการแปลงได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="800dc-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="800dc-128">ตัวอย่างเช่น ถ้าแกลลอนเป็นหน่วยพื้นฐานในคลาสหน่วย *ปริมาตร* คุณจะต้องตั้งค่าตัวแปลงจากควอร์ตเป็นแกลลอน และจากไพนต์เป็นแกลลอนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="800dc-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="800dc-129">จากนั้นระบบยังสามารถแปลงจากควอร์ตเป็นไพนต์</span><span class="sxs-lookup"><span data-stu-id="800dc-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="800dc-130">คุณสามารถมีหน่วยพื้นฐานได้เพียงหน่วยเดียวต่อคลาสหน่วย</span><span class="sxs-lookup"><span data-stu-id="800dc-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="800dc-131">**หน่วยระบบ** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อใช้หน่วยปัจจุบันเป็นหน่วยสมมติสำหรับการวัดที่ไม่ระบุทั้งหมดในคลาสหน่วยนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="800dc-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="800dc-132">ตัวอย่างเช่น ถ้าฟิลด์ที่ใช้ในการป้อนปริมาณไม่อนุญาตให้ระบุหน่วย (หากผู้ใช้ไม่ได้เลือกหน่วย) ระบบจะใช้หน่วยที่ตั้งค่าเป็นหน่วยระบบของคลาสหน่วย *ปริมาณ*</span><span class="sxs-lookup"><span data-stu-id="800dc-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="800dc-133">คุณสามารถมีหน่วยระบบเพียงหน่วยเดียวต่อคลาสหน่วย</span><span class="sxs-lookup"><span data-stu-id="800dc-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="800dc-134">**จํานวนทศนิยม** – ระบุจํานวนของทศนิยมที่จะวางค่าที่ระบุไว้ให้กับหน่วยปัจจุบัน หรือแปลงเป็นจํานวนเงินที่ควรจะปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="800dc-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="800dc-135">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="800dc-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="800dc-136">กำหนดการแปลหน่วย</span><span class="sxs-lookup"><span data-stu-id="800dc-136">Define unit translations</span></span>

<span data-ttu-id="800dc-137">เมื่อต้องการกําหนดการแปลให้กับรหัสหรือสัญลักษณ์ และข้อความอธิบายของหน่วยวัด ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="800dc-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="800dc-138">สร้างหรือเลือกหน่วยที่จะสร้างการแปล</span><span class="sxs-lookup"><span data-stu-id="800dc-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="800dc-139">บนบานหน้าต่างการดำเนินการ เลือก **ข้อความหน่วย**</span><span class="sxs-lookup"><span data-stu-id="800dc-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="800dc-140">หน้า **ข้อความหน่วย** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="800dc-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="800dc-141">คุณใช้หน้านี้เพื่อกําหนดการแปลให้กับรหัสหรือสัญลักษณ์ของหน่วยที่เลือก</span><span class="sxs-lookup"><span data-stu-id="800dc-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="800dc-142">จากนั้นคุณสามารถใช้การแปลเหล่านั้นบนเอกสารภายนอกในภาษาเฉพาะลูกค้าหรือเฉพาะผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="800dc-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="800dc-143">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="800dc-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="800dc-144">ในฟิลด์ **ภาษา** เลือกภาษาเพื่อแปลรหัสหน่วยหรือสัญลักษณ์</span><span class="sxs-lookup"><span data-stu-id="800dc-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="800dc-145">ในฟิลด์ **ข้อความ** ให้ป้อนการแปลของรหัสหน่วยหรือสัญลักษณ์ในภาษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="800dc-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="800dc-146">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="800dc-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="800dc-147">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="800dc-147">Close the page.</span></span>
1. <span data-ttu-id="800dc-148">ใน **บานหน้าต่างการดำเนินการ** เลือก **คำอธิบายหน่วยที่แปล**</span><span class="sxs-lookup"><span data-stu-id="800dc-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="800dc-149">หน้า **คำอธิบายหน่วยที่แปลแล้ว** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="800dc-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="800dc-150">คุณใช้หน้านี้เพื่อกําหนดข้อความอธิบายเฉพาะภาษาของหน่วยที่เลือก</span><span class="sxs-lookup"><span data-stu-id="800dc-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="800dc-151">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="800dc-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="800dc-152">ในฟิลด์ **ภาษา** เลือกภาษาเพื่อแปลคำอธิบายหน่วย</span><span class="sxs-lookup"><span data-stu-id="800dc-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="800dc-153">ในฟิลด์ **คำอธิบาย** ให้ป้อนการแปลของคำอธิบายหน่วยในภาษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="800dc-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="800dc-154">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="800dc-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="800dc-155">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="800dc-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="800dc-156">กำหนดกฎการแปลงหน่วย</span><span class="sxs-lookup"><span data-stu-id="800dc-156">Define unit conversion rules</span></span>

<span data-ttu-id="800dc-157">เมื่อต้องการกําหนดกฎเกี่ยวกับการแปลงระหว่างหน่วยวัด ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="800dc-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="800dc-158">สร้างหรือเลือกหน่วยที่จะกำหนดกฎการแปลง</span><span class="sxs-lookup"><span data-stu-id="800dc-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="800dc-159">บนบานหน้าต่างการดำเนินการ เลือก **การแปลงหน่วย**</span><span class="sxs-lookup"><span data-stu-id="800dc-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="800dc-160">หน้า **การแปลงหน่วย** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="800dc-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="800dc-161">คุณใช้หน้านี้เพื่อกำหนดกฎสำหรับการแปลงหน่วยที่เลือกและจากหน่วยวัดอื่นในคลาสของหน่วย</span><span class="sxs-lookup"><span data-stu-id="800dc-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="800dc-162">เลือกแท็บใดแท็บหนึ่งต่อไปนี้ โดยขึ้นอยู่กับชนิดการแปลงที่คุณต้องการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="800dc-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="800dc-163">**การแปลงมาตรฐาน** – ตั้งค่ากฎการแปลงมาตรฐานของผลิตภัณฑ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="800dc-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="800dc-164">**การแปลงภายในคลาส** – ตั้งค่ากฎการแปลงเฉพาะผลิตภัณฑ์ของหน่วยในคลาสหน่วยเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="800dc-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="800dc-165">**การแปลงต่างคลาส** – ตั้งค่ากฎการแปลงเฉพาะผลิตภัณฑ์ของหน่วยในคลาสหน่วยต่างกัน</span><span class="sxs-lookup"><span data-stu-id="800dc-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="800dc-166">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="800dc-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="800dc-167">หากต้องการสร้างการแปลงใหม่ เลือก **สร้าง** ในแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="800dc-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="800dc-168">เมื่อต้องการแก้ไขการแปลงที่มีอยู่ ให้เลือกการแปลงในกริด แล้วเลือก **แก้ไข** บนแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="800dc-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="800dc-169">ในกล่องโต้ตอบแบบหล่นลงที่ปรากฏขึ้น ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="800dc-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="800dc-170">**ผลิตภัณฑ์** – เลือกผลิตภัณฑ์เฉพาะที่จะใช้การแปลง</span><span class="sxs-lookup"><span data-stu-id="800dc-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="800dc-171">ฟิลด์นี้จะพร้อมใช้งานเฉพาะกับการแปลงภายในคลาสและระหว่างคลาสเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="800dc-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="800dc-172">**โครงร่างสูตร** – ปล่อยฟิลด์นี้ให้ตั้งค่าเป็น *แบบง่าย* เพื่อระบุการแปลงแบบง่ายที่มีปัจจัยเดียว</span><span class="sxs-lookup"><span data-stu-id="800dc-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="800dc-173">ตั้งค่าเป็น *ขั้นสูง* เพื่อตั้งค่าสมการที่ซับซ้อนมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="800dc-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="800dc-174">รูปแบบสมการขั้นสูงแตกต่างกันไป ขึ้นอยู่กับคลาสของหน่วย</span><span class="sxs-lookup"><span data-stu-id="800dc-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="800dc-175">**หน่วยเริ่มต้น** – ฟิลด์นี้จะแสดงหน่วยที่เลือก</span><span class="sxs-lookup"><span data-stu-id="800dc-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="800dc-176">โดยปกติ คุณไม่ควรเปลี่ยนค่า</span><span class="sxs-lookup"><span data-stu-id="800dc-176">Usually, you should not change the value.</span></span> <span data-ttu-id="800dc-177">(ถ้าคุณเปลี่ยนค่า คุณต้องเปิดหน้า **การแปลงหน่วย** ของหน่วยที่เลือกเพื่อดูการแปลงใหม่ของคุณหลังจากที่คุณบันทึก)</span><span class="sxs-lookup"><span data-stu-id="800dc-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="800dc-178">**หน่วยปลายทาง** – เลือกหน่วยที่จะแปลงไปเป็น</span><span class="sxs-lookup"><span data-stu-id="800dc-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="800dc-179">**การปัดเศษ** – เลือกว่าควรปัดเศษเศษส่วนอย่างไร โดยขึ้นอยู่กับค่า **ความละเอียดของทศนิยม** ของหน่วยที่เลือก (*เป็นค่าที่ใกล้ที่สุด* *ขึ้น* หรือ *ลง*)</span><span class="sxs-lookup"><span data-stu-id="800dc-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="800dc-180">**สูตรการแปลง** – ใช้ฟิลด์ที่เหลือที่ด้านบนของกล่องโต้ตอบแบบหล่นลง เพื่อระบุสูตรที่จะแปลงระหว่างสองหน่วย</span><span class="sxs-lookup"><span data-stu-id="800dc-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="800dc-181">ฟิลด์ที่พร้อมใช้งานจะแตกต่างกันไป ขึ้นอยู่กับคลาสหน่วยและโครงร่างสูตรที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="800dc-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="800dc-182">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="800dc-182">Select **OK**.</span></span>
1. <span data-ttu-id="800dc-183">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="800dc-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="800dc-184">คุณยังสามารถตั้งค่าการแปลงหน่วยต่อผลิตภัณฑ์ย่อยได้</span><span class="sxs-lookup"><span data-stu-id="800dc-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="800dc-185">สำหรับข้อมูลเพิ่มเติม ให้ดู [การแปลงหน่วยวัดต่อผลิตภัณฑ์ย่อย](../uom-conversion-per-product-variant.md)</span><span class="sxs-lookup"><span data-stu-id="800dc-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
