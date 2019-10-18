---
title: รหัสขั้นตอนของเวฟ
description: หัวข้อนี้แสดงภาพรวมของรหัสขั้นตอนของเวฟและวิธีการใช้
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992368"
---
# <a name="wave-step-codes"></a><span data-ttu-id="93282-103">รหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="93282-104">เกี่ยวกับรหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-104">About wave step codes</span></span>

<span data-ttu-id="93282-105">รหัสขั้นตอนของเวฟคือรหัสที่ผู้ใช้สามารถตั้งค่า และใช้เพื่อลิงค์อินสแตนซ์เฉพาะของวิธีการของเวฟไปยังเท็มเพลตที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="93282-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="93282-106">เท็มเพลตจะรวมเท็มเพลตสำหรับการเติมสินค้า การบรรจุลงตู้บรรจุสินค้า การพิมพ์ป้ายชื่อ อาคารจำนวนงานในศูนย์การผลิต และการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="93282-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="93282-107">เมื่อไม่มีการใช้รหัสขั้นตอนเวฟ ผู้ใช้ต้องป้อนข้อความอิสระเพื่ออ้างอิงถึงเท็มเพลตที่ระบุจากอินสแตนซ์วิธีการของเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="93282-108">ข้อความอิสระมีแนวโน้มที่จะเกิดข้อผิดพลาด เนื่องจากผู้ใช้ต้องตรวจสอบให้แน่ใจว่าข้อความขั้นตอนเวฟที่มีการเพิ่มสำหรับวิธีการขั้นตอนของเวฟเฉพาะในเท็มเพลตเวฟ ตรงกับข้อความขั้นตอนของเวฟในเท็มเพลตเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="93282-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="93282-109">รหัสขั้นตอนเวฟสำหรับชนิดขั้นตอนเวฟที่ระบุจะถูกตั้งค่าไว้บนหน้าแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="93282-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="93282-110">สำหรับอินสแตนซ์วิธีการขั้นตอนของเวฟทั้งหมดในเท็มเพลตเวฟที่ต้องมีรหัสขั้นตอนของเวฟ ต้องเลือกรหัสขั้นตอนของเวฟในรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="93282-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="93282-111">การเลือกในรายการแบบหล่นลงจะแทนที่การป้อนข้อความอิสระ และช่วยลดความเสี่ยงและผลกระทบของข้อผิดพลาดของบุคคล</span><span class="sxs-lookup"><span data-stu-id="93282-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="93282-112">รหัสการตั้งค่าใช้เพื่อเชื่อมโยงวิธีการขั้นตอนของเวฟในเท็มเพลตเวฟ ไปยังเท็มเพลตปลายทางสำหรับวิธีการ</span><span class="sxs-lookup"><span data-stu-id="93282-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="93282-113">การใช้คุณลักษณะของรหัสขั้นตอนของเวฟเป็นตัวเลือก และการใช้เป็นไปตามนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="93282-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="93282-114">ดังนั้น ถ้านิติบุคคลเฉพาะใช้คุณลักษณะ รหัสขั้นตอนเวฟที่มีอยู่ทั้งหมดในนิติบุคคลดังกล่าวจะถูกอัพเกรดเป็นโครงสร้างใหม่</span><span class="sxs-lookup"><span data-stu-id="93282-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="93282-115">ตั้งค่าการสาธิต</span><span class="sxs-lookup"><span data-stu-id="93282-115">Setup demo</span></span> 

<span data-ttu-id="93282-116">สำหรับการสาธิตนี้ ต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องใช้บริษัทข้อมูลสาธิต **USMF**</span><span class="sxs-lookup"><span data-stu-id="93282-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="93282-117">เปิดใช้งานรหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-117">Enable wave step codes</span></span>

<span data-ttu-id="93282-118">ทำตามขั้นตอนเหล่านี้เพื่อเปิดใช้งานคุณลักษณะรหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="93282-119">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> พารามิเตอร์การจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="93282-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="93282-120">บนแท็บ **ทั่วไป** บน FastTab **การประมวลผลเวฟ** ตั้งค่าตัวเลือก **เปิดใช้งานรหัสขั้นตอนของเวฟ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="93282-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="93282-121">ข้อความอิสระของขั้นตอนเวฟที่มีอยู่ทั้งหมดจะได้รับการอัพเกรดเป็นโครงสร้างใหม่</span><span class="sxs-lookup"><span data-stu-id="93282-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="93282-122">หลังจากที่การปรับรุ่นนี้เสร็จสมบูรณ์สำหรับนิติบุคคลแล้ว ตัวเลือก **เปิดใช้งานรหัสขั้นตอนของเวฟ** จะไม่มีอยู่ในหน้า **พารามิเตอร์การจัดการคลังสินค้า** อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="93282-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="93282-123">การตรวจสอบความถูกต้องจะดำเนินการในระหว่างการปรับรุ่น และถ้าการปรับรุ่นล้มเหลว คุณจะได้รับข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="93282-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="93282-124">การปรับรุ่นอาจล้มเหลวเนื่องจากความขัดแย้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="93282-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="93282-125">ทำซ้ำขั้นตอนของเวฟที่มีข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="93282-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="93282-126">มีการเลือกกำหนดอยู่</span><span class="sxs-lookup"><span data-stu-id="93282-126">Customizations exist.</span></span>
- <span data-ttu-id="93282-127">ข้อความอิสระของขั้นตอนของเวฟที่สัมพันธ์กับอินสแตนซ์วิธีการขั้นตอนของเวฟ ไม่ตรงกับชนิดของเท็มเพลตที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="93282-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="93282-128">หลังจากที่คุณได้แก้ไขความขัดแย้งใดๆ ที่ระบุในระหว่างการตรวจสอบแล้ว คุณสามารถรันกระบวนการอัพเกรดอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="93282-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="93282-129">เมื่อการอัพเกรดสำเร็จ หน้า **รหัสขั้นตอนเวฟ** (**การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> รหัสขั้นตอนเวฟ**) จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="93282-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="93282-130">หน้านี้จะแสดงรายการรหัสขั้นตอนเวฟที่ถูกอัพเกรด เมื่อมีการเปิดใช้งานคุณลักษณะรหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="93282-131">สร้างรหัสขั้นตอนของเวฟใหม่</span><span class="sxs-lookup"><span data-stu-id="93282-131">Create new wave step codes</span></span>

<span data-ttu-id="93282-132">คุณสามารถใช้หน้า **รหัสขั้นตอนของเวฟ** เพื่อสร้างและลบรหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="93282-133">รหัสขั้นตอนของเวฟใหม่ทุกรายการและรหัสที่เชื่อมโยง จะต้องไม่ซ้ำกันระหว่างชนิดของขั้นตอนเวฟทั้งหมด และต้องมีการกำหนดสำหรับชนิดของขั้นตอนของเวฟเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="93282-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="93282-134">ใช้รหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-134">Apply wave step codes</span></span>

<span data-ttu-id="93282-135">หลังจากที่คุณได้กำหนดรหัสขั้นตอนเวฟที่เหมาะสมแล้ว คุณสามารถใช้ได้กับกระบวนการของเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="93282-136">เมื่อต้องการใช้รหัสขั้นตอนของเวฟ ให้ไปที่เท็มเพลตเป้าหมายที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="93282-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="93282-137">ต่อไปนี้เป็นเท็มเพลตปลายทางที่มีการกำหนดรหัสขั้นตอนของเวฟให้ชี้ไปที่:</span><span class="sxs-lookup"><span data-stu-id="93282-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="93282-138">**เท็มเพลตการเติมสินค้า:** การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> เท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="93282-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="93282-139">**เท็มเพลตการสร้างโหลด:** การจัดการคลังสินค้า \> การตั้งค่า \> โหลด \> เท็มเพลตการสร้างโหลด</span><span class="sxs-lookup"><span data-stu-id="93282-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="93282-140">**จัดเรียงเท็มเพลต:** การจัดการคลังสินค้า \> การตั้งค่า \> การบรรจุ \> เท็มเพลตการเรียงลำดับขาออก</span><span class="sxs-lookup"><span data-stu-id="93282-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="93282-141">**เท็มเพลตการบรรจุลงตู้บรรจุสินค้า:** การจัดการคลังสินค้า \> การตั้งค่า \> คอนเทนเนอร์ \> เท็มเพลตการสร้างคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="93282-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="93282-142">**เท็มเพลตการพิมพ์ป้ายชื่อ:** การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> เท็มเพลตป้ายชื่อของเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="93282-143">จะมีการใช้เท็มเพลตในรายการนี้ เมื่อมีการอ้างอิงจากวิธีการในการประมวลผลเวฟที่เลือกในเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="93282-144">เมื่อรหัสขั้นตอนของเวฟในวิธีการประมวลผลเวฟในเท็มเพลตเวฟ ตรงกับรหัสขั้นตอนของเวฟในเท็มเพลตชนิดใดชนิดหนึ่ง จะมีการใช้เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="93282-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="93282-145">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="93282-145">Sample scenario</span></span>

<span data-ttu-id="93282-146">กระบวนงานต่อไปนี้ช่วยรับประกันว่าเท็มเพลตการเติมสินค้าที่คุณสร้างขึ้น จะถูกนำไปใช้กับเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="93282-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="93282-147">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> รหัสขั้นตอนของเวฟ** และสร้างรหัสขั้นตอนเวฟสำหรับชนิด **การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="93282-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="93282-148">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเพิ่มเติมสินค้า \> เท็มเพลตการเติมสินค้า** และสร้างเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="93282-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="93282-149">ในเท็มเพลตการเติมสินค้า ให้เลือกรหัสขั้นตอนเวฟที่คุณสร้างไว้สำหรับชนิด **การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="93282-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="93282-150">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ** และเลือกเวฟที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="93282-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="93282-151">ในเท็มเพลต บน FastTab **วิธีการ** ให้เลือกวิธีการ **การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="93282-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="93282-152">ในฟิลด์ **รหัสขั้นตอนเวฟ** ให้เลือกรหัสขั้นตอนเวฟที่คุณเลือกไว้ในเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="93282-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
