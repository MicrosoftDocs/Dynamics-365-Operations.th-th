---
title: รหัสขั้นตอนของเวฟ
description: หัวข้อนี้แสดงภาพรวมของรหัสขั้นตอนของเวฟและวิธีการใช้
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 08b40c076e288592f6a4cd628b9acd8a2eaedb7e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998414"
---
# <a name="wave-step-codes"></a><span data-ttu-id="30d47-103">รหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="30d47-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30d47-104">รหัสขั้นตอนของเวฟคือรหัสที่ผู้ใช้สามารถตั้งค่า และใช้เพื่อลิงค์อินสแตนซ์เฉพาะของวิธีการของเวฟไปยังเท็มเพลตที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="30d47-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="30d47-105">เท็มเพลตจะรวมเท็มเพลตสำหรับการเติมสินค้า การบรรจุลงตู้บรรจุสินค้า การพิมพ์ป้ายชื่อ อาคารจำนวนงานในศูนย์การผลิต และการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="30d47-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="30d47-106">เมื่อไม่มีการใช้รหัสขั้นตอนเวฟ ผู้ใช้ต้องป้อนข้อความอิสระเพื่ออ้างอิงถึงเท็มเพลตที่ระบุจากอินสแตนซ์วิธีการของเวฟ</span><span class="sxs-lookup"><span data-stu-id="30d47-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="30d47-107">ข้อความอิสระมีแนวโน้มที่จะเกิดข้อผิดพลาด เนื่องจากผู้ใช้ต้องตรวจสอบให้แน่ใจว่าข้อความขั้นตอนเวฟที่มีการเพิ่มสำหรับวิธีการขั้นตอนของเวฟเฉพาะในเท็มเพลตเวฟ ตรงกับข้อความขั้นตอนของเวฟในเท็มเพลตเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="30d47-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="30d47-108">รหัสขั้นตอนเวฟสำหรับชนิดขั้นตอนเวฟที่ระบุจะถูกตั้งค่าไว้บนหน้าแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="30d47-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="30d47-109">สำหรับอินสแตนซ์วิธีการขั้นตอนของเวฟทั้งหมดในเท็มเพลตเวฟที่ต้องมีรหัสขั้นตอนของเวฟ ต้องเลือกรหัสขั้นตอนของเวฟในรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="30d47-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="30d47-110">การเลือกในรายการแบบหล่นลงจะแทนที่การป้อนข้อความอิสระ และช่วยลดความเสี่ยงและผลกระทบของข้อผิดพลาดของบุคคล</span><span class="sxs-lookup"><span data-stu-id="30d47-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="30d47-111">รหัสการตั้งค่าใช้เพื่อเชื่อมโยงวิธีการขั้นตอนของเวฟในเท็มเพลตเวฟ ไปยังเท็มเพลตปลายทางสำหรับวิธีการ</span><span class="sxs-lookup"><span data-stu-id="30d47-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="30d47-112">การใช้คุณลักษณะรหัสขั้นตอนของเวฟเป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="30d47-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="30d47-113">มีการเปิดใช้งานทั่วทั้งองค์กรสำหรับนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="30d47-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="30d47-114">ตั้งค่าการสาธิต</span><span class="sxs-lookup"><span data-stu-id="30d47-114">Setup demo</span></span> 

<span data-ttu-id="30d47-115">สำหรับการสาธิตนี้ ต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องใช้บริษัทข้อมูลสาธิต **USMF**</span><span class="sxs-lookup"><span data-stu-id="30d47-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="30d47-116">เปิดใช้งานรหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="30d47-116">Enable wave step codes</span></span>

<span data-ttu-id="30d47-117">ทำตามขั้นตอนเหล่านี้เพื่อเปิดใช้งานคุณลักษณะรหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="30d47-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="30d47-118">ไปที่ **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="30d47-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="30d47-119">เลือกเพื่อเปิดใช้งานคุณลักษณะที่เรียกว่า **รหัสขั้นตอนของเวฟทั่วทั้งองค์กร**</span><span class="sxs-lookup"><span data-stu-id="30d47-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="30d47-120">ข้อความอิสระของขั้นตอนเวฟที่มีอยู่ทั้งหมดในนิติบุคคลทั้งหมดจะได้รับการปรับรุ่นเป็นโครงสร้างใหม่</span><span class="sxs-lookup"><span data-stu-id="30d47-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="30d47-121">หลังจากการปรับรุ่นนี้เสร็จสมบูรณ์แล้วสำหรับนิติบุคคลทั้งหมด จากนั้นคุณลักษณะนี้จะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="30d47-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="30d47-122">ถ้าไม่สามารถเปิดใช้งานคุณลักษณะสำหรับนิติบุคคลหนึ่งรายขึ้นไป คุณลักษณะจะไม่ถูกเปิดใช้งานสำหรับนิติบุคคลใดๆ</span><span class="sxs-lookup"><span data-stu-id="30d47-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="30d47-123">ในระหว่างการเปิดใช้งาน จะมีการทำการตรวจสอบในระหว่างการปรับรุ่นข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30d47-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="30d47-124">ถ้าการปรับปรุงล้มเหลว คุณจะได้รับข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="30d47-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="30d47-125">การปรับรุ่นอาจล้มเหลวเนื่องจากความขัดแย้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="30d47-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="30d47-126">ทำซ้ำขั้นตอนของเวฟที่มีข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="30d47-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="30d47-127">มีการเลือกกำหนดอยู่</span><span class="sxs-lookup"><span data-stu-id="30d47-127">Customizations exist.</span></span>
- <span data-ttu-id="30d47-128">ข้อความอิสระของขั้นตอนของเวฟที่สัมพันธ์กับอินสแตนซ์วิธีการขั้นตอนของเวฟ ไม่ตรงกับชนิดของเท็มเพลตที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="30d47-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="30d47-129">หลังจากที่คุณได้แก้ไขความขัดแย้งใดๆ ที่ระบุในระหว่างการตรวจสอบแล้ว คุณสามารถลองเปิดใช้งานคุณลักษณะอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="30d47-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="30d47-130">เมื่อมีการเปิดใช้งานคุณลักษณะ หน้า **รหัสขั้นตอนเวฟ** (**การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> รหัสขั้นตอนเวฟ**) จะกลายเป็นพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="30d47-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="30d47-131">หน้านี้จะแสดงรายการรหัสขั้นตอนเวฟที่ถูกปรับรุ่น เมื่อมีการเปิดใช้งานคุณลักษณะรหัสขั้นตอนของเวฟทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="30d47-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="30d47-132">สร้างรหัสขั้นตอนของเวฟใหม่</span><span class="sxs-lookup"><span data-stu-id="30d47-132">Create new wave step codes</span></span>

<span data-ttu-id="30d47-133">คุณสามารถใช้หน้า **รหัสขั้นตอนของเวฟ** เพื่อสร้างและลบรหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="30d47-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="30d47-134">รหัสขั้นตอนของเวฟใหม่ทุกรายการและรหัสที่เชื่อมโยง จะต้องไม่ซ้ำกันระหว่างชนิดของขั้นตอนเวฟทั้งหมด และต้องมีการกำหนดสำหรับชนิดของขั้นตอนของเวฟเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="30d47-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="30d47-135">ใช้รหัสขั้นตอนของเวฟ</span><span class="sxs-lookup"><span data-stu-id="30d47-135">Apply wave step codes</span></span>

<span data-ttu-id="30d47-136">หลังจากที่คุณได้กำหนดรหัสขั้นตอนเวฟที่เหมาะสมแล้ว คุณสามารถใช้ได้กับกระบวนการของเวฟ</span><span class="sxs-lookup"><span data-stu-id="30d47-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="30d47-137">เมื่อต้องการใช้รหัสขั้นตอนของเวฟ ให้ไปที่เท็มเพลตเป้าหมายที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="30d47-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="30d47-138">ต่อไปนี้เป็นเท็มเพลตปลายทางที่มีการกำหนดรหัสขั้นตอนของเวฟให้ชี้ไปที่:</span><span class="sxs-lookup"><span data-stu-id="30d47-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="30d47-139">**เท็มเพลตการเติมสินค้า:** การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> เท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="30d47-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="30d47-140">**เท็มเพลตการสร้างโหลด:** การจัดการคลังสินค้า \> การตั้งค่า \> โหลด \> เท็มเพลตการสร้างโหลด</span><span class="sxs-lookup"><span data-stu-id="30d47-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="30d47-141">**จัดเรียงเท็มเพลต:** การจัดการคลังสินค้า \> การตั้งค่า \> การบรรจุ \> เท็มเพลตการเรียงลำดับขาออก</span><span class="sxs-lookup"><span data-stu-id="30d47-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="30d47-142">**เท็มเพลตการบรรจุลงตู้บรรจุสินค้า:** การจัดการคลังสินค้า \> การตั้งค่า \> คอนเทนเนอร์ \> เท็มเพลตการสร้างคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="30d47-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="30d47-143">**เท็มเพลตการพิมพ์ป้ายชื่อ:** การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> เท็มเพลตป้ายชื่อของเวฟ</span><span class="sxs-lookup"><span data-stu-id="30d47-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="30d47-144">จะมีการใช้เท็มเพลตในรายการนี้ เมื่อมีการอ้างอิงจากวิธีการในการประมวลผลเวฟที่เลือกในเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="30d47-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="30d47-145">เมื่อรหัสขั้นตอนของเวฟในวิธีการประมวลผลเวฟในเท็มเพลตเวฟ ตรงกับรหัสขั้นตอนของเวฟในเท็มเพลตชนิดใดชนิดหนึ่ง จะมีการใช้เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="30d47-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="30d47-146">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="30d47-146">Sample scenario</span></span>

<span data-ttu-id="30d47-147">กระบวนงานต่อไปนี้ช่วยรับประกันว่าเท็มเพลตการเติมสินค้าที่คุณสร้างขึ้น จะถูกนำไปใช้กับเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="30d47-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="30d47-148">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> รหัสขั้นตอนของเวฟ** และสร้างรหัสขั้นตอนเวฟสำหรับชนิด **การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="30d47-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="30d47-149">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเพิ่มเติมสินค้า \> เท็มเพลตการเติมสินค้า** และสร้างเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="30d47-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="30d47-150">ในเท็มเพลตการเติมสินค้า ให้เลือกรหัสขั้นตอนเวฟที่คุณสร้างไว้สำหรับชนิด **การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="30d47-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="30d47-151">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ** และเลือกเวฟที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="30d47-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="30d47-152">ในเท็มเพลต บน FastTab **วิธีการ** ให้เลือกวิธีการ **การเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="30d47-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="30d47-153">ในฟิลด์ **รหัสขั้นตอนเวฟ** ให้เลือกรหัสขั้นตอนเวฟที่คุณเลือกไว้ในเท็มเพลตการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="30d47-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="30d47-154">คุณทำตามขั้นตอนเหล่านี้สำหรับแต่ละนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="30d47-154">You perform these steps for each legal entity.</span></span>
