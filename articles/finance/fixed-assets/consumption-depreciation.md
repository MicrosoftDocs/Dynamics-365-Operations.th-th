---
title: การคิดค่าเสื่อมราคาตามปริมาณการใช้
description: บทความนี้แสดงภาพรวมของวิธีปริมาณการใช้ค่าเสื่อมราคา
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187325"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="1e352-103">การคิดค่าเสื่อมราคาตามปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="1e352-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e352-104">บทความนี้แสดงภาพรวมของวิธีปริมาณการใช้ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="1e352-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="1e352-105">ถ้าคุณตั้งค่าโพรไฟล์ค่าเสื่อมราคาสำหรับสินทรัพย์ถาวรและเลือก **ปริมาณการใช้** ใน **ฟิลด์วิธีการ** บน **หน้าโพรไฟล์ค่าเสื่อมราคา** สินทรัพย์ถาวรที่มีการกำหนดไปยังโพรไฟล์ค่าเสื่อมราคาตามการใช้</span><span class="sxs-lookup"><span data-stu-id="1e352-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="1e352-106">คุณไม่จำเป็นต้องตั้งค่าเปอร์เซ็นต์และช่วงเวลาใน **หน้าโพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="1e352-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="1e352-107">หลังจากที่คุณสร้างโพรไฟล์ค่าเสื่อมราคาที่ใช้วิธีปริมาณการใช้ คุณสามารถตั้งค่าวิธีการได้ในลักษณะต่างๆ</span><span class="sxs-lookup"><span data-stu-id="1e352-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="1e352-108">การตั้งค่าและใช้ค่าเสื่อมราคาตามปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="1e352-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="1e352-109">ในหน้า **โพรไฟล์ค่าเสื่อมราคา** สร้างโพรไฟล์ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="1e352-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="1e352-110">สำหรับการคำนวณปริมาณการใช้ โพรไฟล์ค่าเสื่อมราคาต้องมีรหัสและชื่อ และ **ปริมาณการใช้** จะต้องถูกเลือกในฟิลด์**วิธีการ**</span><span class="sxs-lookup"><span data-stu-id="1e352-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="1e352-111">ในหน้า **สัดส่วนของปริมาณการใช้วัสดุ** ตั้งค่าสัดส่วนของปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="1e352-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="1e352-112">สัดส่วนของปริมาณการใช้วัสดุแต่ละรายการต้องมีรหัส และชื่อ และสัดส่วนของปริมาณการใช้วัสดุที่ระบุตามปริมาณหรือเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="1e352-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="1e352-113">ในหน้า **สัดส่วนของปริมาณการใช้วัสดุ** ตั้งค่าสัดส่วนของปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="1e352-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="1e352-114">แต่ละหน่วยปริมาณการใช้วัสดุต้องมีรหัสและชื่อ</span><span class="sxs-lookup"><span data-stu-id="1e352-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="1e352-115">หน่วยการคิดค่าเสื่อมราคาจะใช้เพื่อคำนวณค่าเสื่อมราคาปริมาณการใช้ในหน้า **ค่าเสื่อมราคาปริมาณการใช้วัสดุ**</span><span class="sxs-lookup"><span data-stu-id="1e352-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="1e352-116">ตัวอย่างของหน่วยได้แก่กิโลเมตร(กม.) กิโลกรัม(กก.) และชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="1e352-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="1e352-117">ในหน้า **สินทรัพย์ถาวร** ตั้งค่าสินทรัพย์ถาวรแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="1e352-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="1e352-118">สำหรับแต่ละสินทรัพย์ถาวร เลือกรูปแบบมูลค่าและสมุดบัญชีค่าเสื่อมราคาที่มีโพรไฟล์การคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="1e352-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="1e352-119">คุณต้องตั้งค่ารูปแบบมูลค่าหรือสมุดบัญชีค่าเสื่อมราคาสำหรับค่าเสื่อมราคาปริมาณการใช้ ถ้ามีสินทรัพย์ถาวรของคุณใช้โพรไฟล์การคิดค่าเสื่อมราคาที่ขึ้นอยู่กับวิธีปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="1e352-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="1e352-120">การตั้งค่านี้จะทำอย่างใดอย่างหนึ่งบนแท็บ **ค่าเสื่อมราคา** ของหน้า **รูปแบบมูลค่า** หรือบนแท็บด่วน **ทั่วไป** ของ **หน้าโพรไฟล์การคิดค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="1e352-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="1e352-121">คุณสามารถใช้รูปแบบมูลค่าเดียวกันสำหรับสินทรัพย์ถาวรหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="1e352-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="1e352-122">โพรไฟล์ค่าเสื่อมราคาที่เป็นส่วนของรูปแบบมูลค่าหรือสมุดบัญชีค่าเสื่อมราคาที่คุณเลือกไว้สำหรับแต่ละสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="1e352-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="1e352-123">คุณไม่สามารถเพิ่มหรือปรับเปลี่ยนโพรไฟล์ค่าเสื่อมราคาได้โดยตรงบนหน้า **สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="1e352-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="1e352-124">คุณสามารถปรับเปลี่ยนโพรไฟล์ค่าเสื่อมราคาในหน้า **สมุดบัญชีค่าเสื่อมราคาเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="1e352-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="1e352-125">บนหน้า **รูปแบบมูลค่า** หรือหน้า **สมุดบัญชีค่าเสื่อมราคา** ในกลุ่มฟิลด์ **การคิดค่าเสื่อมราคาตามปริมาณการใช้**  ป้อนข้อมูลในฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1e352-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="1e352-126">สัดส่วนของปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="1e352-126">Consumption factor</span></span>
    -   <span data-ttu-id="1e352-127">หน่วย</span><span class="sxs-lookup"><span data-stu-id="1e352-127">Unit</span></span>
    -   <span data-ttu-id="1e352-128">ค่าเสื่อมราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="1e352-128">Unit depreciation</span></span>
    -   <span data-ttu-id="1e352-129">ปริมาณการใช้วัสดุที่ประเมิน</span><span class="sxs-lookup"><span data-stu-id="1e352-129">Estimated consumption</span></span>

    <span data-ttu-id="1e352-130">ฟิลด์**ปริมาณการใช้วัสดุที่ลงรายการบัญชี** จะแสดงการคิดค่าเสื่อมราคาตามปริมาณการใช้ ในหน่วย ซึ่งมีการลงรายการบัญชีแล้วสำหรับชุดของสินทรัพย์ถาวรและรูปแบบมูลค่าหรือสมุดบัญชีค่าเสื่อมราคาสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="1e352-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="1e352-131">คุณไม่สามารถปรับปรุงค่าในฟิลด์นั้นด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="1e352-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="1e352-132">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="1e352-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="1e352-133">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="1e352-133">Example 1</span></span>

<span data-ttu-id="1e352-134">สัดส่วนของปริมาณการใช้วัสดุต่อไปนี้ตั้งค่าไว้สำหรับวันที่ 31 มกราคม</span><span class="sxs-lookup"><span data-stu-id="1e352-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="1e352-135">ปริมาณต่ำสุดคือ 1,000</span><span class="sxs-lookup"><span data-stu-id="1e352-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="1e352-136">ราคาค่าเสื่อมราคาต่อหน่วยที่ระบุไว้สำหรับสินทรัพย์ถาวรคือ 1.5</span><span class="sxs-lookup"><span data-stu-id="1e352-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="1e352-137">ข้อเสนอค่าเสื่อมราคาในวันที่ 31 มกราคมเป็นดังนี้: ปริมาณ × การคิดค่าเสื่อมราคาต่อหน่วย 1000 × 1.5 = 1500 ถ้าตัวคูณที่ระบุไว้สำหรับสินทรัพย์ถาวรเป็นสัดส่วนเปอร์เซ็นต์ ปริมาณที่ประเมินในฟิลด์ **ปริมาณการใช้วัสดุที่ประเมิน** สำหรับรูปแบบมูลค่าของสินทรัพย์ถาวรถูกคูณด้วยเปอร์เซ็นต์ที่ตั้งค่าไว้สำหรับวันสิ้นสุดที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1e352-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="1e352-138">ปริมาณผลลัพธ์จะแนะนำตามปริมาณค่าเสื่อมราคาสำหรับรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="1e352-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="1e352-139">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="1e352-139">Example 2</span></span>

<span data-ttu-id="1e352-140">ตัวคูณต่อไปนี้สำหรับการคิดค่าเสื่อมราคาตามปริมาณการใช้วัสดุตั้งค่าไว้สำหรับวันที่ 31 มกราคม</span><span class="sxs-lookup"><span data-stu-id="1e352-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="1e352-141">เปอร์เซ็นต์คือ 10 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="1e352-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="1e352-142">ราคาค่าเสื่อมราคาต่อหน่วยที่ระบุไว้สำหรับสินทรัพย์ถาวรคือ 1.5</span><span class="sxs-lookup"><span data-stu-id="1e352-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="1e352-143">ปริมาณที่ประเมินของสินทรัพย์ถาวรคือ 2000</span><span class="sxs-lookup"><span data-stu-id="1e352-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="1e352-144">ข้อเสนอค่าเสื่อมราคาในวันที่ 31 มกราคมเป็นดังนี้:ปริมาณที่ประเมิน × เปอร์เซ็นต์ × ค่าเสื่อมราคาต่อหน่วย 2000 × .10 × 1.5 = 300</span><span class="sxs-lookup"><span data-stu-id="1e352-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>



