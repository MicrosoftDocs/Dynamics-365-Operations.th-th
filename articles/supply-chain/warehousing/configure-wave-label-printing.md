---
title: ตั้งค่าและใช้การพิมพ์ป้ายชื่อเวฟ
description: หัวข้อนี้จะอธิบายการพิมพ์ป้ายชื่อเวฟ และอธิบายวิธีการตั้งค่า
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 6314fd25d8d8a0013984d484f57a832c26f82b5a
ms.sourcegitcommit: a26e4963d40796da21ce6581cfb2f4d9db4f6776
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/27/2020
ms.locfileid: "4438924"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="54aaf-103">ตั้งค่าและใช้การพิมพ์ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54aaf-104">การพิมพ์ป้ายชื่อเวฟมีแนวทางอื่นในการพิมพ์ป้ายชื่อโดยการแนะนำวิธีการขั้นตอนของเวฟใหม่ ซึ่งช่วยให้คุณสามารถสร้างและพิมพ์ป้ายชื่อได้โดยตรงจากเท็มเพลตของเวฟในระหว่างการดำเนินการเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="54aaf-105">ดังนั้น ป้ายชื่อดังกล่าวจะพร้อมใช้งานอยู่แล้ว ก่อนที่ผู้ปฏิบัติงานจะรันใบสั่งงานบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="54aaf-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="54aaf-106">จากนั้น ผู้ปฏิบัติงานจึงสามารถแนบป้ายชื่อที่ต้องการได้ในระหว่างการเบิกสินค้า แทนที่จะเป็นหลังจากการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="54aaf-107">การพิมพ์ป้ายชื่อเวฟใช้ Zebra Programming Language (ZPL) เพื่อสร้างโครงร่างป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="54aaf-108">โครงร่างป้ายชื่อถูกแบ่งออกเป็นสามส่วน (ส่วนหัว เนื้อหา และท้ายกระดาษ) เพื่ออนุญาตป้ายชื่อที่มีโครงสร้างการทำซ้ำ</span><span class="sxs-lookup"><span data-stu-id="54aaf-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="54aaf-109">เท็มเพลตของป้ายชื่อเวฟจะบอกให้ระบบทราบถึงโครงร่างป้ายชื่อที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="54aaf-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="54aaf-110">ผู้ใช้สามารถระบุเครื่องพิมพ์ที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="54aaf-110">Users can specify which printer is used.</span></span> <span data-ttu-id="54aaf-111">นอกจากนี้ พวกเขายังสามารถพิมพ์ป้ายชื่อบนเครื่องพิมพ์หลายเครื่องพร้อมกันได้ตามที่พวกเขาต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="54aaf-112">หน้า **ประวัติป้ายชื่อเวฟ** แสดงเรกคอร์ดของป้ายชื่อทั้งหมดที่สร้างขึ้นโดยใช้การตั้งค่านี้</span><span class="sxs-lookup"><span data-stu-id="54aaf-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="54aaf-113">คุณสามารถพิมพ์และเรียงป้ายชื่อตามส่วนหัวของงาน คุณสามารถพิมพ์ป้ายชื่อการแบ่งสำหรับส่วนหัวของงานแต่ละส่วน และคุณสามารถพิมพ์ป้ายชื่อเนื้อหาของคอนเทนเนอร์ ป้ายชื่อกรณี และป้ายชื่อที่คล้ายกันอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="54aaf-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="54aaf-114">ฟังก์ชันนี้ไม่ได้แทนที่ฟังก์ชันการพิมพ์ป้ายชื่อที่มีอยู่ซึ่งยึดตามการกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="54aaf-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="54aaf-115">การพิมพ์ป้ายชื่อเวฟให้การปรับปรุงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="54aaf-116">พิมพ์ป้ายชื่อตามจำนวนของกล่องบนบรรทัดงานหนึ่งๆ โดยไม่ใช้การบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="54aaf-117">("กล่อง" เป็นหน่วยที่กำหนดไว้ในบรรทัดกลุ่มลำดับของหน่วย)</span><span class="sxs-lookup"><span data-stu-id="54aaf-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="54aaf-118">พิมพ์ลำดับป้ายชื่อที่แตกต่างกันหลายรายการ (ตัวอย่างเช่น ป้ายชื่อกล่องและแท่นวางสินค้า)</span><span class="sxs-lookup"><span data-stu-id="54aaf-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="54aaf-119">ประกอบด้วยการแจงนับป้ายชื่อ (ตัวอย่างเช่น 1/124, 2/124, ... 124/124) และกำหนดช่วงของการแจงนับ (ตัวอย่างเช่น รายการงาน รายการโหลด หรือการจัดส่ง)</span><span class="sxs-lookup"><span data-stu-id="54aaf-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="54aaf-120">สร้างและพิมพ์รหัสใบตราส่งบนป้ายชื่อ ก่อนที่จะมีการสร้างใบตราส่ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="54aaf-121">สร้างรหัสคอนเทนเนอร์การจัดส่งสินค้าที่ไม่ซ้ำกัน (SSCC) สำหรับแต่ละกล่อง และรวมไว้ในป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="54aaf-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="54aaf-122">สร้างลำดับหมายเลขที่สอดคล้องกับ GS1 สำหรับรหัสใบตราส่งและ SSCCs</span><span class="sxs-lookup"><span data-stu-id="54aaf-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="54aaf-123">พิมพ์ป้ายชื่อใหม่จากทั้งอุปกรณ์เคลื่อนที่และไคลเอนต์ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="54aaf-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="54aaf-124">ยกเลิกป้ายชื่อ (ตัวอย่างเช่น ในสถานการณ์การเบิกสินค้าที่ขาด) และพิมพ์ใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="54aaf-125">ล้างข้อมูลประวัติป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="54aaf-126">การปรับปรุงไปยังโครงร่างการกำหนดเส้นทางเอกสารถูกใช้ร่วมกันระหว่างโครงร่างการกำหนดเส้นทางเอกสารและโครงร่างป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="54aaf-127">(สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โครงร่างการกำหนดเส้นทางเอกสารสำหรับป้ายทะเบียน](../warehousing/document-routing-layout-for-license-plates.md))</span><span class="sxs-lookup"><span data-stu-id="54aaf-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="54aaf-128">การปรับปรุงเหล่านี้ทำให้มีประสิทธิภาพมากขึ้นในการติดป้ายชื่อกล่องก่อนการวางบนแท่นวางสินค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="54aaf-129">โดยเฉพาะอย่างยิ่ง เป็นประโยชน์สำหรับบริษัทที่จัดส่งไปยังร้านค้าปลีกขนาดใหญ่ที่ยืนยันการรับสินค้าตามใบสั่งโดยอัตโนมัติโดยการสแกนกล่องแต่ละกล่องโดยแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="54aaf-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="54aaf-130">คุณสามารถใช้สถานการณ์จำลองการตั้งค่าคอนฟิกที่อธิบายไว้ในหัวข้อนี้โดยแยกต่างหากหรือใช้ร่วมกันได้ ทั้งนี้ขึ้นอยู่กับความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="54aaf-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="54aaf-131">คุณสามารถออกแบบเท็มเพลตป้ายชื่อเวฟต่างๆ ที่ทำงานอยู่ในลำดับ (ดังที่แสดงในสถานการณ์จำลอง 3)</span><span class="sxs-lookup"><span data-stu-id="54aaf-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="54aaf-132">ตัวอย่างเช่น คุณสามารถใช้สถานการณ์จำลอง 1 เพื่อพิมพ์ป้ายชื่อกล่อง และสถานการณ์จำลอง 2 เพื่อพิมพ์ป้ายชื่อแท่นวางสินค้า (ถ้าแท่นวางสินค้าในสต็อกแตกต่างกันในขนาดและองค์ประกอบ)</span><span class="sxs-lookup"><span data-stu-id="54aaf-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="54aaf-133">เปิดคุณลักษณะการพิมพ์ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="54aaf-134">ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การพิมพ์ป้ายชื่อเวฟ* ต้องมีการเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="54aaf-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="54aaf-135">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="54aaf-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="54aaf-136">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="54aaf-137">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="54aaf-138">**ชื่อคุณลักษณะ:** *การพิมพ์ป้ายชื่อเวฟ*</span><span class="sxs-lookup"><span data-stu-id="54aaf-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="54aaf-139">สถานการณ์จำลอง 1: การพิมพ์ป้ายชื่อเวฟที่มีการสร้างป้ายชื่อเวฟเดียว</span><span class="sxs-lookup"><span data-stu-id="54aaf-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="54aaf-140">สถานการณ์นี้แสดงวิธีการที่บริษัทสามารถพิมพ์ป้ายชื่อการจัดส่งสำหรับผู้ค้าปลีกขนาดใหญ่ที่ยืนยันการรับสินค้าตามใบสั่งโดยอัตโนมัติโดยการสแกนกล่องแต่ละกล่องโดยแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="54aaf-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="54aaf-141">สถานการณ์จำลองนี้แสดงลำดับตั้งแต่ต้นจนจบ</span><span class="sxs-lookup"><span data-stu-id="54aaf-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="54aaf-142">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="54aaf-142">Make demo data available</span></span>

<span data-ttu-id="54aaf-143">เพื่อติดตามสถานการณ์จำลองนี้ คุณต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องเลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="54aaf-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="54aaf-144">ตรวจสอบให้แน่ใจว่าวิธีการป้ายชื่อเวฟพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="54aaf-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="54aaf-145">คุณอาจต้องสร้างวิธีการประมวลผลเวฟของคุณใหม่เพื่อทำให้วิธีการพิมพ์ป้ายชื่อเวฟพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="54aaf-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="54aaf-146">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> วิธีการประมวลผลเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="54aaf-147">ยืนยันว่า **waveLabelPrinting** อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="54aaf-148">ถ้าไม่มีอยู่ ให้เลือก **สร้างวิธีการใหม่** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="54aaf-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="54aaf-149">ตั้งค่าคอนฟิกเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-149">Configure a wave template</span></span>

<span data-ttu-id="54aaf-150">เท็มเพลตเวฟช่วยให้คุณสามารถเชื่อมโยงอินสแตนซ์ที่เฉพาะเจาะจงของวิธีการเวฟไปยังเท็มเพลตป้ายชื่อเวฟที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="54aaf-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="54aaf-151">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="54aaf-152">เลือกเท็มเพลต เช่น **62 ค่าเริ่มต้นของการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="54aaf-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="54aaf-153">บน FastTab **วิธีการ** ให้ย้ายวิธีการ **การพิมพ์ป้ายชื่อเวฟ** ไปที่คอลัมน์ **วิธีการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="54aaf-154">ในคอลัมน์ **วิธีการที่เลือก** ให้เลือกวิธีการ **การพิมพ์ป้ายชื่อเวฟ** และตั้งค่าฟิลด์ **รหัสขั้นตอนของเวฟ** เป็น *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="54aaf-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="54aaf-155">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสขั้นตอนของเวฟ ให้ดูที่ [รหัสขั้นตอนของเวฟ](wave-step-codes.md)</span><span class="sxs-lookup"><span data-stu-id="54aaf-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="54aaf-156">สร้างโครงร่างป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-156">Create a wave label layout</span></span>

<span data-ttu-id="54aaf-157">โครงร่างป้ายชื่อจะควบคุมข้อมูลที่จะพิมพ์บนป้ายชื่อและวิธีการจัดวางข้อมูลของป้ายชื่อ ที่นี่ คุณป้อนรหัส ZPL ที่ส่งไปยังเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="54aaf-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="54aaf-158">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> โครงร่างป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="54aaf-159">สร้างเรกคอร์ดที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-160">**รหัสโครงร่างป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="54aaf-161">**คำอธิบาย:** *กล่อง (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="54aaf-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="54aaf-162">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="54aaf-163">ในบานหน้าต่างการดำเนินการ ให้เลือก **การตั้งค่าแถวของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="54aaf-164">หน้า **การตั้งค่าแถวของป้ายชื่อเวฟ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="54aaf-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="54aaf-165">ที่นี่ คุณสามารถตั้งค่าคอนฟิกส่วนไดนามิกของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="54aaf-166">เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-167">**รหัสแถว:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="54aaf-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="54aaf-168">**ชื่อตารางแถว:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="54aaf-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="54aaf-169">**ตำแหน่งเริ่มต้นของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="54aaf-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="54aaf-170">ฟิลด์นี้จะกำหนดตำแหน่งในแนวตั้งที่ซึ่งแถวจะเริ่มต้นบนป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="54aaf-171">**ความสูงของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="54aaf-171">**Row height:** *0*</span></span>

        <span data-ttu-id="54aaf-172">ฟิลด์นี้จะกำหนดความสูงของแต่ละแถว (ตามจุด) ตามมาตรฐาน ZPL</span><span class="sxs-lookup"><span data-stu-id="54aaf-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="54aaf-173">ความสูงของแถวเป็นค่าบวกสำหรับป้ายชื่อแนวนอน และค่าลบสำหรับป้ายชื่อแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="54aaf-174">เนื่องจากมีเพียงหนึ่งแถวเท่านั้นในตัวอย่างนี้ คุณสามารถตั้งค่าเป็น *0* (ศูนย์) ได้</span><span class="sxs-lookup"><span data-stu-id="54aaf-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="54aaf-175">**แถวต่อหน้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="54aaf-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="54aaf-176">ฟิลด์นี้จะกำหนดจำนวนของแถวที่สามารถพิมพ์บนป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="54aaf-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="54aaf-177">การตั้งค่านี้จะทำให้ป้ายชื่อ ZPL ที่แยกต่างหากถูกพิมพ์สำหรับเรกคอร์ดแต่ละรายการในตารางป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="54aaf-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-178">Close the page.</span></span>
1. <span data-ttu-id="54aaf-179">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="54aaf-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="54aaf-180">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-181">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-182">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-183">**ฟิลด์:** *ชนิดงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="54aaf-184">**เงื่อนไข:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="54aaf-185">การสอบถามนี้ช่วยให้มั่นใจว่า จะมีการพิมพ์เฉพาะรายการงานชนิดการเบิกสินค้าบนป้ายชื่อ ไม่ใช่รายการงานชนิดการส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="54aaf-186">ถ้าคุณต้องการสามารถพิมพ์รหัสใบตราส่ง บนแท็บ **รวม** เลือกตาราง **รายการงาน** และรวมตาราง **การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="54aaf-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="54aaf-187">ปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="54aaf-188">FastTab **โครงร่างข้อความของเครื่องพิมพ์** มีส่วนสามส่วนที่ซึ่งคุณสามารถเขียนรหัสเครื่องพิมพ์: **ส่วนของส่วนหัว** **ส่วนของเนื้อหา** และ **ส่วนของท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="54aaf-189">ใน **ส่วนของส่วนหัว** ในฟิลด์ **ส่วนหัวของป้ายชื่อ** ป้อนรหัสสำหรับส่วนหัวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="54aaf-190">ตัวอย่างเช่น ถ้าคุณกำลังใช้เครื่องพิมพ์ Zebra คุณสามารถใช้รหัสดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="54aaf-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="54aaf-191">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **เนื้อหาของป้ายชื่อ** ป้อนรหัส ZPL สำหรับเนื้อหาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="54aaf-192">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="54aaf-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="54aaf-193">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **ส่วนท้ายของป้ายชื่อ** ป้อนรหัส ZPL สำหรับส่วนท้ายที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="54aaf-194">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="54aaf-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="54aaf-195">การตั้งค่านี้จะพิมพ์สำเนาหนึ่งฉบับของป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="54aaf-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="54aaf-196">ถ้าคุณต้องการสำเนาเพิ่มเติม (ตัวอย่างเช่น สำเนาหนึ่งฉบับสำหรับแต่ละด้านของแท่นวางสินค้า) ให้ตั้งค่า **n** สำหรับส่วน **\^PQn** ในส่วนท้ายเป็นจำนวนสำเนาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="54aaf-197">ตัวอย่างเช่น ถ้าต้องการพิมพ์สำเนาสี่ฉบับของป้ายชื่อแต่ละป้าย ให้ระบุ **\^PQ4**</span><span class="sxs-lookup"><span data-stu-id="54aaf-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="54aaf-198">ในขณะนี้ป้ายชื่อของคุณพร้อมที่จะใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="54aaf-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="54aaf-199">สร้างชนิดป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-199">Create a wave label type</span></span>

<span data-ttu-id="54aaf-200">ชนิดป้ายชื่อเวฟถูกใช้เพื่อลิงค์เท็มเพลตของป้ายชื่อเวฟกับหน่วยในรายการกลุ่มลำดับหน่วย</span><span class="sxs-lookup"><span data-stu-id="54aaf-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="54aaf-201">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> ชนิดป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="54aaf-202">เพิ่มชนิดป้ายชื่อเวฟที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-203">**ชนิดป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="54aaf-204">**คำอธิบาย:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="54aaf-205">ตั้งค่ากลุ่มลำดับหน่วย</span><span class="sxs-lookup"><span data-stu-id="54aaf-205">Set up unit sequence groups</span></span>

<span data-ttu-id="54aaf-206">ถัดไป ให้ตั้งค่ากลุ่มลำดับของหน่วยสำหรับชนิดป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="54aaf-207">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> กลุ่มลำดับของหน่วย**</span><span class="sxs-lookup"><span data-stu-id="54aaf-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="54aaf-208">เลือกกลุ่ม **Ea Box PL**</span><span class="sxs-lookup"><span data-stu-id="54aaf-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="54aaf-209">สำหรับรายการ **กล่อง** ให้ตั้งค่าฟิลด์ **ชนิดระดับเวฟ** เป็น *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="54aaf-210">สร้างเท็มเพลตของป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-210">Create a wave label template</span></span>

<span data-ttu-id="54aaf-211">ถัดไป ให้สร้างเท็มเพลตของป้ายชื่อเวฟสำหรับชนิดป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="54aaf-212">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> เท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="54aaf-213">เพิ่มเท็มเพลตของระดับเวฟ และตั้งค่าค่าต่อไปนี้ในส่วนหัว:</span><span class="sxs-lookup"><span data-stu-id="54aaf-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="54aaf-214">**ชื่อเท็มเพลตของป้ายชื่อ:** *ป้ายชื่อกล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="54aaf-215">**คำอธิบาย:** *ป้ายชื่อกล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="54aaf-216">**รหัสขั้นตอนของเวฟ:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="54aaf-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="54aaf-217">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="54aaf-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="54aaf-218">บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **ชนิดป้ายชื่อเวฟ** เป็น *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="54aaf-219">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เพิ่มแถวใหม่ที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-220">**รหัสโครงร่างป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="54aaf-221">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์ ZPL ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="54aaf-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="54aaf-222">**รันการสอบถาม:** *ใช่* (การตั้งค่านี้ไม่จำเป็นต้องระบุ แต่ขอแนะนำให้ใช้ประสิทธิภาพสูงสุด)</span><span class="sxs-lookup"><span data-stu-id="54aaf-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="54aaf-223">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="54aaf-224">ไม่จำเป็นต้องระบุ: ถ้าคุณกำลังตั้งค่าการออกแบบป้ายชื่อเฉพาะลูกค้า คุณต้องสร้างการสอบถามเพื่อค้นหาบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="54aaf-225">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="54aaf-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="54aaf-226">จากนั้น ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-227">**ตาราง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="54aaf-228">**ตารางสืบทอด:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="54aaf-229">**ฟิลด์:** *หมายเลขบัญชี*</span><span class="sxs-lookup"><span data-stu-id="54aaf-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="54aaf-230">**เงื่อนไข:** ให้ป้อนหมายเลขบัญชีลูกค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="54aaf-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="54aaf-231">เมื่อคุณดำเนินการเสร็จสิ้น ให้เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="54aaf-232">ในบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไขการสอบถาม** เพื่อเปิดกล่องโต้ตอบตัวแก้ไขการสอบถามสำหรับเท็มเพลตป้ายชื่อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="54aaf-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="54aaf-233">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **การเรียงลำดับ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-234">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-235">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-236">**ฟิลด์:** *รหัสรายการของโหลดอ้างอิง (รหัสเรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="54aaf-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="54aaf-237">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="54aaf-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="54aaf-238">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="54aaf-239">กล่องข้อความจะพร้อมท์ให้คุณยืนยันการดำเนินการรีเซ็ตการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="54aaf-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="54aaf-240">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="54aaf-241">ในบานหน้าต่างการดำเนินการ ให้เลือก **กลุ่มเท็มเพลตป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="54aaf-242">ในกล่องโต้ตอบ **กลุ่มเท็มเพลตป้ายชื่อเวฟ** ให้เลือกแถวที่มีการตั้งค่าฟิลด์ **ชื่อฟิลด์การอ้างอิง** เป็น *รหัสรายการโหลดอ้างอิง* และจากนั้น เลือกกล่องกาเครื่องหมาย **รหัสการสร้างป้ายชื่อ** สำหรับแถวนี้</span><span class="sxs-lookup"><span data-stu-id="54aaf-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="54aaf-243">การตั้งค่านี้จะสร้างลำดับป้ายชื่อหนึ่งลำดับ ("กล่อง 1 จาก X") สำหรับแต่ละรายการโหลดทั่วทั้งเวฟ โดยไม่คำนึงถึงการตั้งค่าการจัดกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="54aaf-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="54aaf-244">คุณสามารถพิมพ์ลำดับป้ายชื่อนี้บนโครงร่างป้ายชื่อได้</span><span class="sxs-lookup"><span data-stu-id="54aaf-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="54aaf-245">ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="54aaf-245">Configure number sequence extensions</span></span>

<span data-ttu-id="54aaf-246">ส่วนขยายของลำดับหมายเลขจะควบคุมการปฏิบัติตาม GS1 ของลำดับหมายเลขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="54aaf-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="54aaf-247">ไม่จำเป็นต้องระบุการตั้งค่าคอนฟิกนี้สำหรับสถานการณ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="54aaf-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="54aaf-248">สำหรับข้อมูลเพิ่มเติมและคำแนะนำในการตั้งค่าคอนฟิก ให้ดู [ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข](../warehousing/configure-number-sequence-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="54aaf-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="54aaf-249">สร้างใบสั่งขายและนำใบสั่งขายออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="54aaf-250">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="54aaf-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="54aaf-251">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-252">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="54aaf-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="54aaf-253">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="54aaf-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="54aaf-254">เพิ่มรายการขายสองรายการที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="54aaf-255">รายการใบสั่งขายที่ 1:</span><span class="sxs-lookup"><span data-stu-id="54aaf-255">Sales order line 1:</span></span>

        - <span data-ttu-id="54aaf-256">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="54aaf-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="54aaf-257">**ปริมาณ:** *9024*</span><span class="sxs-lookup"><span data-stu-id="54aaf-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="54aaf-258">**หน่วย:** *ชิ้น* (9024 ชิ้น = 376 กล่อง = 47 แท่นวางสินค้า)</span><span class="sxs-lookup"><span data-stu-id="54aaf-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="54aaf-259">รายการใบสั่งขายที่ 2:</span><span class="sxs-lookup"><span data-stu-id="54aaf-259">Sales order line 2:</span></span>

        - <span data-ttu-id="54aaf-260">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="54aaf-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="54aaf-261">**ปริมาณ:** *9016*</span><span class="sxs-lookup"><span data-stu-id="54aaf-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="54aaf-262">**หน่วย:** *ชิ้น* (9016 ชิ้น = 322 กล่อง = 46 แท่นวางสินค้า)</span><span class="sxs-lookup"><span data-stu-id="54aaf-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="54aaf-263">สินค้าและปริมาณที่ให้ไว้ที่นี่คือตัวอย่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="54aaf-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="54aaf-264">พวกเขาต้องใช้กลุ่มลำดับหน่วยที่คุณได้กำหนดไว้ก่อนหน้านี้ การแปลงหน่วยที่เหมาะสมจาก *ชิ้น* เป็น *กล่อง* เป็น *แท่นวางสินค้า* ต้องถูกกำหนด และต้องมีสินค้าคงคลังในคลังสินค้า *62*</span><span class="sxs-lookup"><span data-stu-id="54aaf-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="54aaf-265">สำหรับข้อมูลเพิ่มเติม ให้ดู [นโยบายหน่วยวัดและการเก็บสต็อก](unit-measure-stocking-policies.md)</span><span class="sxs-lookup"><span data-stu-id="54aaf-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="54aaf-266">เลือกรายการในใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="54aaf-266">Select sales order line 1.</span></span> <span data-ttu-id="54aaf-267">จากนั้น ในส่วน **รายการใบสั่งขาย** บนเมนู **สินค้าคงคลัง** เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="54aaf-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="54aaf-268">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** และจากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="54aaf-269">ทำซ้ำขั้นตอนที่ 4 และ 5 สำหรับรายการใบสั่งขายที่ 2</span><span class="sxs-lookup"><span data-stu-id="54aaf-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="54aaf-270">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="54aaf-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="54aaf-271">เหตุการณ์ต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="54aaf-271">The following events occur:</span></span>

    - <span data-ttu-id="54aaf-272">ระบบจะประมวลผลการจัดส่งที่สร้างขึ้นโดยใช้เท็มเพลตที่มีขั้นตอนการพิมพ์ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="54aaf-273">โครงร่างป้ายชื่อจะถูกใช้เพื่อกำหนดรูปแบบของป้ายชื่อ และผลลัพธ์จะเป็นป้ายชื่อที่พิมพ์บนเครื่องพิมพ์ที่เลือกในเท็มเพลตของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="54aaf-274">มีการสร้างและพิมพ์ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="54aaf-275">จำนวนของป้ายชื่อจะเท่ากับจำนวนของกล่อง (ในตัวอย่างนี้ ป้ายชื่อของกล่อง 376 ป้ายสำหรับรายการที่ 1 และป้ายชื่อกล่อง 322 ป้ายสำหรับรายการที่ 2)</span><span class="sxs-lookup"><span data-stu-id="54aaf-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="54aaf-276">รหัสใบตราส่งใหม่จะถูกสร้างขึ้นสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="54aaf-277">ถ้าคุณได้ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข รหัสป้ายชื่อเวฟจะเป็นไปตามรูปแบบหมายเลข **SSCC-18**</span><span class="sxs-lookup"><span data-stu-id="54aaf-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="54aaf-278">คุณสามารถดูและพิมพ์ป้ายชื่อเวฟอีกครั้งจากหน้าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="54aaf-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="54aaf-279">บนบานหน้าต่างการดำเนินการของหน้าแต่ละหน้า บนแท็บ **การจัดส่ง** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **ป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="54aaf-280">การจัดส่งทั้งหมด \> รายละเอียดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="54aaf-281">โหลดทั้งหมด \> รายละเอียดโหลด</span><span class="sxs-lookup"><span data-stu-id="54aaf-281">All loads \> Load details</span></span>
- <span data-ttu-id="54aaf-282">เวฟทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="54aaf-282">All waves</span></span>
- <span data-ttu-id="54aaf-283">ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-283">Wave labels</span></span>
- <span data-ttu-id="54aaf-284">ประวัติป้ายชื่อของเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="54aaf-285">สถานการณ์จำลองที่ 2: การพิมพ์ป้ายชื่อเวฟสำหรับการบรรจุลงตู้บรรจุสินค้า (โดยไม่มีเรกคอร์ดป้ายชื่อเวฟ)</span><span class="sxs-lookup"><span data-stu-id="54aaf-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="54aaf-286">สถานการณ์นี้ช่วยให้คุณสามารถพิมพ์ป้ายชื่อเวฟได้ เมื่อคุณใช้การบรรจุลงตู้บรรจุสินค้าเพื่อแบ่งสินค้าลงในกล่องโดยอัตโนมัติ และดังนั้นจึงไม่ต้องใช้เรกคอร์ดของป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="54aaf-287">ในกรณีนี้ รหัสคอนเทนเนอร์ทำหน้าที่เป็นตัวยึดตำแหน่งสำหรับ SSCC</span><span class="sxs-lookup"><span data-stu-id="54aaf-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="54aaf-288">ต่อไปนี้คือความแตกต่างที่สำคัญระหว่างสถานการณ์จำลองนี้และสถานการณ์จำลอง 1:</span><span class="sxs-lookup"><span data-stu-id="54aaf-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="54aaf-289">**เท็มเพลตของป้ายชื่อเวฟ:** คุณจะไม่เลือกชนิดป้ายชื่อเวฟบนเท็มเพลตของป้ายชื่อเวฟ และคุณไม่จำเป็นต้องมีการจัดกลุ่มการสร้างป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="54aaf-290">มิฉะนั้น คุณจะตั้งค่าคอนฟิกเท็มเพลตของป้ายชื่อเวฟ และลิงค์ไปยังเท็มเพลตเวฟในลักษณะเดียวกับที่อธิบายไว้ในสถานการณ์จำลอง 1</span><span class="sxs-lookup"><span data-stu-id="54aaf-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="54aaf-291">คุณต้องปล่อยชนิดป้ายชื่อเวฟให้ว่างไว้ เพื่อป้องกันไม่ให้มีการสร้างป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="54aaf-292">**โครงร่างป้ายชื่อเวฟ:** คุณจะตั้งค่าคอนฟิกการตั้งค่าแถวของโครงร่างป้ายชื่อเวฟสำหรับรายการงาน แทนที่จะเป็นเรกคอร์ดของป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="54aaf-293">คุณต้องตั้งค่าคอนฟิกการตั้งค่าแถวสำหรับโครงร่างป้ายชื่อโดยใช้ตาราง **WHSWorkLine** แทนตาราง **WHSWaveLabel**</span><span class="sxs-lookup"><span data-stu-id="54aaf-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="54aaf-294">การตั้งค่า **แถวต่อหน้า** จะควบคุมจำนวนของแถวที่ส่วนเนื้อหาจะมี</span><span class="sxs-lookup"><span data-stu-id="54aaf-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="54aaf-295">นอกจากนี้ การตั้งค่าคอนฟิกนี้ยังเหมาะสำหรับสถานการณ์จำลองทางธุรกิจ ที่ซึ่งสินค้าที่แตกต่างกันหลายรายการถูกบรรจุอยู่ในกล่องที่มีการระบุชื่อหนึ่งกล่องหรือในแท่นวางสินค้า และสามารถกำหนดกระบวนการบรรจุนี้ได้โดยการสร้างงาน (ตัวอย่างเช่น งานที่จัดกลุ่มตามการจัดส่ง)</span><span class="sxs-lookup"><span data-stu-id="54aaf-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="54aaf-296">สถานการณ์จำลองนี้แสดงลำดับตั้งแต่ต้นจนจบ</span><span class="sxs-lookup"><span data-stu-id="54aaf-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="54aaf-297">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="54aaf-297">Make demo data available</span></span>

<span data-ttu-id="54aaf-298">เพื่อติดตามสถานการณ์จำลองนี้ คุณต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องเลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="54aaf-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="54aaf-299">ตรวจสอบให้แน่ใจว่าวิธีการป้ายชื่อเวฟพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="54aaf-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="54aaf-300">คุณอาจต้องสร้างวิธีการประมวลผลเวฟของคุณใหม่เพื่อทำให้วิธีการพิมพ์ป้ายชื่อเวฟพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="54aaf-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="54aaf-301">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> วิธีการประมวลผลเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="54aaf-302">ยืนยันว่า **waveLabelPrinting** อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="54aaf-303">ถ้าไม่มีอยู่ ให้เลือก **สร้างวิธีการใหม่** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="54aaf-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="54aaf-304">การตั้งค่าเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-304">Set up a wave template</span></span>

<span data-ttu-id="54aaf-305">เท็มเพลตเวฟช่วยให้คุณสามารถเชื่อมโยงอินสแตนซ์ที่เฉพาะเจาะจงของวิธีการเวฟไปยังเท็มเพลตป้ายชื่อเวฟที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="54aaf-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="54aaf-306">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="54aaf-307">เลือกเท็มเพลต เช่น **63 การบรรจุลงตู้บรรจุสินค้า**</span><span class="sxs-lookup"><span data-stu-id="54aaf-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="54aaf-308">บน FastTab **วิธีการ** ให้ย้ายวิธีการ **การพิมพ์ป้ายชื่อเวฟ** ไปที่คอลัมน์ **วิธีการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="54aaf-309">ในคอลัมน์ **วิธีการที่เลือก** ให้เลือกวิธีการ **การพิมพ์ป้ายชื่อเวฟ** และตั้งค่าฟิลด์ **รหัสขั้นตอนของเวฟ** เป็น *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="54aaf-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="54aaf-310">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสขั้นตอนของเวฟ ให้ดูที่ [รหัสขั้นตอนของเวฟ](wave-step-codes.md)</span><span class="sxs-lookup"><span data-stu-id="54aaf-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="54aaf-311">สร้างโครงร่างป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-311">Create a wave label layout</span></span>

1. <span data-ttu-id="54aaf-312">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> โครงร่างป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="54aaf-313">สร้างเรกคอร์ดที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-314">**รหัสโครงร่างป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="54aaf-315">**คำอธิบาย:** *กล่อง (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="54aaf-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="54aaf-316">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="54aaf-317">ในบานหน้าต่างการดำเนินการ ให้เลือก **การตั้งค่าแถวของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="54aaf-318">หน้า **การตั้งค่าแถวของป้ายชื่อเวฟ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="54aaf-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="54aaf-319">ที่นี่ คุณสามารถตั้งค่าคอนฟิกส่วนไดนามิกของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="54aaf-320">เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-321">**รหัสแถว:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="54aaf-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="54aaf-322">**ชื่อตารางแถว:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="54aaf-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="54aaf-323">**ตำแหน่งเริ่มต้นของแถว:** *500*</span><span class="sxs-lookup"><span data-stu-id="54aaf-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="54aaf-324">ฟิลด์นี้จะกำหนดตำแหน่งในแนวตั้งที่ซึ่งแถวจะเริ่มต้นบนป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="54aaf-325">**ความสูงของแถว:** *-50*</span><span class="sxs-lookup"><span data-stu-id="54aaf-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="54aaf-326">ฟิลด์นี้จะกำหนดความสูงของแต่ละแถว</span><span class="sxs-lookup"><span data-stu-id="54aaf-326">This field defines the height of each row.</span></span> <span data-ttu-id="54aaf-327">ความสูงของแถวเป็นค่าบวกสำหรับป้ายชื่อแนวนอน และค่าลบสำหรับป้ายชื่อแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="54aaf-328">**แถวต่อหน้า:** *5*</span><span class="sxs-lookup"><span data-stu-id="54aaf-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="54aaf-329">ฟิลด์นี้จะกำหนดจำนวนของแถวที่สามารถพิมพ์บนป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="54aaf-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="54aaf-330">การตั้งค่านี้จะพิมพ์ป้ายชื่อ ZPL หลายป้ายสำหรับแต่ละงาน โดยที่แต่ละหน้าสามารถจัดเก็บรายการงานได้สูงสุดห้ารายการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="54aaf-331">ตัวอย่างเช่น ถ้ามีการพิมพ์ป้ายชื่อสำหรับคอนเทนเนอร์ที่มี 12 รายการ จะมีการพิมพ์ป้ายชื่อสามป้าย</span><span class="sxs-lookup"><span data-stu-id="54aaf-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="54aaf-332">ถ้าคุณต้องการพิมพ์ป้ายชื่อแยกต่างหากสำหรับรายการเบิกสินค้าแต่ละรายการ ให้ตั้งค่านี้เป็น *1*</span><span class="sxs-lookup"><span data-stu-id="54aaf-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="54aaf-333">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-333">Close the page.</span></span>
1. <span data-ttu-id="54aaf-334">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="54aaf-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="54aaf-335">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-336">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-337">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-338">**ฟิลด์:** *ชนิดงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="54aaf-339">**เงื่อนไข:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="54aaf-340">ถ้าคุณต้องการสามารถพิมพ์รหัสใบตราส่ง บนแท็บ **รวม** เลือกตาราง **รายการงาน** และรวมตาราง **การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="54aaf-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="54aaf-341">ปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="54aaf-342">FastTab **โครงร่างข้อความของเครื่องพิมพ์** มีส่วนสามส่วนที่ซึ่งคุณสามารถเขียนรหัสเครื่องพิมพ์: **ส่วนของส่วนหัว** **ส่วนของเนื้อหา** และ **ส่วนของท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="54aaf-343">ใน **ส่วนของส่วนหัว** ในฟิลด์ **ส่วนหัวของป้ายชื่อ** ป้อนรหัสสำหรับส่วนหัวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="54aaf-344">ตัวอย่างเช่น ถ้าคุณกำลังใช้เครื่องพิมพ์ Zebra คุณสามารถใช้รหัสดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="54aaf-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="54aaf-345">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **เนื้อหาของป้ายชื่อ** ป้อนรหัส ZPL สำหรับเนื้อหาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="54aaf-346">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="54aaf-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="54aaf-347">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **ส่วนท้ายของป้ายชื่อ** ป้อนรหัส ZPL สำหรับส่วนท้ายที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="54aaf-348">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="54aaf-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="54aaf-349">การตั้งค่านี้จะพิมพ์สำเนาหนึ่งฉบับของป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="54aaf-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="54aaf-350">ถ้าคุณต้องการสำเนาเพิ่มเติม (ตัวอย่างเช่น สำเนาหนึ่งฉบับสำหรับแต่ละด้านของแท่นวางสินค้า) ให้ตั้งค่า **n** สำหรับส่วน **\^PQn** ในส่วนท้ายเป็นจำนวนสำเนาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="54aaf-351">ตัวอย่างเช่น ถ้าต้องการพิมพ์สำเนาสี่ฉบับของป้ายชื่อแต่ละป้าย ให้ระบุ **\^PQ4**</span><span class="sxs-lookup"><span data-stu-id="54aaf-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="54aaf-352">ในขณะนี้ป้ายชื่อของคุณพร้อมที่จะใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="54aaf-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="54aaf-353">สร้างเท็มเพลตของป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-353">Create a wave label template</span></span>

1. <span data-ttu-id="54aaf-354">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> เท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="54aaf-355">เพิ่มเท็มเพลตของระดับเวฟ และตั้งค่าค่าต่อไปนี้ในส่วนหัว:</span><span class="sxs-lookup"><span data-stu-id="54aaf-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="54aaf-356">**ชื่อเท็มเพลตของป้ายชื่อ:** *ป้ายชื่อคอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="54aaf-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="54aaf-357">**คำอธิบาย:** *ป้ายชื่อคอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="54aaf-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="54aaf-358">**รหัสขั้นตอนของเวฟ:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="54aaf-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="54aaf-359">**คลังสินค้า:** *63*</span><span class="sxs-lookup"><span data-stu-id="54aaf-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="54aaf-360">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-361">**รหัสโครงร่างป้ายชื่อ:** *คอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="54aaf-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="54aaf-362">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์ ZPL ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="54aaf-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="54aaf-363">**รันการสอบถาม:** *ใช่* (การตั้งค่านี้ไม่จำเป็นต้องระบุ แต่ขอแนะนำให้ใช้ประสิทธิภาพสูงสุด)</span><span class="sxs-lookup"><span data-stu-id="54aaf-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="54aaf-364">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="54aaf-365">ไม่จำเป็นต้องระบุ: ถ้าคุณกำลังตั้งค่าการออกแบบป้ายชื่อเฉพาะลูกค้า คุณต้องสร้างการสอบถามเพื่อค้นหาบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="54aaf-366">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="54aaf-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="54aaf-367">จากนั้น ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-368">**ตาราง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="54aaf-369">**ตารางสืบทอด:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="54aaf-370">**ฟิลด์:** *หมายเลขบัญชี*</span><span class="sxs-lookup"><span data-stu-id="54aaf-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="54aaf-371">**เงื่อนไข:** ให้ป้อนหมายเลขบัญชีลูกค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="54aaf-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="54aaf-372">เมื่อคุณดำเนินการเสร็จสิ้น ให้เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="54aaf-373">ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="54aaf-373">Configure number sequence extensions</span></span>

<span data-ttu-id="54aaf-374">ส่วนขยายของลำดับหมายเลขจะควบคุมการปฏิบัติตาม GS1 ของลำดับหมายเลขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="54aaf-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="54aaf-375">ไม่จำเป็นต้องระบุการตั้งค่าคอนฟิกนี้สำหรับสถานการณ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="54aaf-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="54aaf-376">สำหรับข้อมูลเพิ่มเติมและคำแนะนำในการตั้งค่าคอนฟิก ให้ดู [ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข](../warehousing/configure-number-sequence-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="54aaf-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="54aaf-377">สร้างใบสั่งขายและนำใบสั่งขายออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="54aaf-378">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="54aaf-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="54aaf-379">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-380">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="54aaf-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="54aaf-381">**คลังสินค้า:** *63*</span><span class="sxs-lookup"><span data-stu-id="54aaf-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="54aaf-382">เพิ่มรายการใบสั่งขายห้ารายการ:</span><span class="sxs-lookup"><span data-stu-id="54aaf-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="54aaf-383">รายการใบสั่งขายที่ 1:</span><span class="sxs-lookup"><span data-stu-id="54aaf-383">Sales order line 1:</span></span>

        - <span data-ttu-id="54aaf-384">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="54aaf-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="54aaf-385">**ปริมาณ:** *10*</span><span class="sxs-lookup"><span data-stu-id="54aaf-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="54aaf-386">รายการใบสั่งขายที่ 2:</span><span class="sxs-lookup"><span data-stu-id="54aaf-386">Sales order line 2:</span></span>

        - <span data-ttu-id="54aaf-387">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="54aaf-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="54aaf-388">**ปริมาณ:** *20*</span><span class="sxs-lookup"><span data-stu-id="54aaf-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="54aaf-389">รายการใบสั่งขายที่ 3:</span><span class="sxs-lookup"><span data-stu-id="54aaf-389">Sales order line 3:</span></span>

        - <span data-ttu-id="54aaf-390">**หมายเลขสินค้า:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="54aaf-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="54aaf-391">**ปริมาณ:** *20*</span><span class="sxs-lookup"><span data-stu-id="54aaf-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="54aaf-392">รายการใบสั่งขายที่ 4:</span><span class="sxs-lookup"><span data-stu-id="54aaf-392">Sales order line 4:</span></span>

        - <span data-ttu-id="54aaf-393">**หมายเลขสินค้า:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="54aaf-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="54aaf-394">**ปริมาณ:** *40*</span><span class="sxs-lookup"><span data-stu-id="54aaf-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="54aaf-395">รายการใบสั่งขายที่ 5:</span><span class="sxs-lookup"><span data-stu-id="54aaf-395">Sales order line 5:</span></span>

        - <span data-ttu-id="54aaf-396">**หมายเลขสินค้า:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="54aaf-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="54aaf-397">**ปริมาณ:** *50*</span><span class="sxs-lookup"><span data-stu-id="54aaf-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="54aaf-398">สินค้าและปริมาณที่ให้ไว้ที่นี่คือตัวอย่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="54aaf-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="54aaf-399">ต้องมีสินค้าคงคลังในคลังสินค้าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="54aaf-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="54aaf-400">เลือกรายการในใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="54aaf-400">Select sales order line 1.</span></span> <span data-ttu-id="54aaf-401">จากนั้น ในส่วน **รายการใบสั่งขาย** บนเมนู **สินค้าคงคลัง** เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="54aaf-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="54aaf-402">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** และจากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="54aaf-403">ทำซ้ำขั้นตอนที่ 4 และ 5 สำหรับรายการใบสั่งขายเพิ่มเติมแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="54aaf-404">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="54aaf-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="54aaf-405">เหตุการณ์ต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="54aaf-405">The following events occur:</span></span>

    - <span data-ttu-id="54aaf-406">ระบบจะประมวลผลการจัดส่งที่สร้างขึ้นโดยใช้เท็มเพลตที่มีขั้นตอนการพิมพ์ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="54aaf-407">โครงร่างป้ายชื่อจะถูกใช้เพื่อกำหนดรูปแบบของป้ายชื่อ และผลลัพธ์สุดท้ายจะเป็นป้ายชื่อที่มีห้ารายการและที่พิมพ์บนเครื่องพิมพ์ที่เลือกในเท็มเพลตของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="54aaf-408">รหัสใบตราส่งใหม่จะถูกสร้างขึ้นสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="54aaf-409">ถ้าคุณได้ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข รหัสป้ายชื่อเวฟจะเป็นไปตามรูปแบบหมายเลข **SSCC-18**</span><span class="sxs-lookup"><span data-stu-id="54aaf-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="54aaf-410">คุณสามารถพิมพ์ป้ายชื่อเวฟเหล่านี้ใหม่ได้โดยไปที่ **การจัดการคลังสินค้า \> การสอบถามและรายงาน \> ประวัติป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="54aaf-411">สถานการณ์จำลอง 3: การพิมพ์ป้ายชื่อเวฟสำหรับป้ายชื่อแบบหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="54aaf-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="54aaf-412">สถานการณ์นี้แสดงวิธีการใช้ฟังก์ชันการพิมพ์ป้ายชื่อเวฟ เมื่อกระบวนการคลังสินค้าต้องมีป้ายชื่อการจัดส่งหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="54aaf-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="54aaf-413">ตัวอย่างเช่น อาจต้องพิมพ์ป้ายชื่อที่แยกต่างหากสำหรับกล่องและแท่นวางสินค้า และอาจต้องพิมพ์ป้ายชื่อการแบ่งสำหรับการจัดส่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="54aaf-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="54aaf-414">ป้ายชื่อการแบ่งเป็นชนิดที่แยกต่างหากของป้ายชื่อที่สามารถใช้เป็นตัวแบ่งระหว่างม้วนและคอนเทนเนอร์ เช่น ป้ายชื่อสำหรับรหัสการจัดส่งและบาร์โค้ด เพื่อให้สามารถเรียงลำดับป้ายชื่อได้ง่าย หลังจากที่มีการพิมพ์</span><span class="sxs-lookup"><span data-stu-id="54aaf-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="54aaf-415">ความแตกต่างที่สำคัญระหว่างการตั้งค่าคอนฟิกของสถานการณ์จำลองนี้และการตั้งค่าคอนฟิกของสถานการณ์จำลอง 1 นอกจากข้อเท็จจริงที่ว่ามีการเปิดใช้งานป้ายชื่อการแบ่ง คือชนิดป้ายชื่อเวฟหลายชนิดต้องเชื่อมโยงกับเท็มเพลตของป้ายชื่อเวฟและรายการกลุ่มลำดับหน่วย</span><span class="sxs-lookup"><span data-stu-id="54aaf-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="54aaf-416">เมื่อต้องการทำให้การตั้งค่าคอนฟิกนี้เสร็จสิ้น คุณจะตั้งค่าองค์ประกอบต่อไปนี้สำหรับสถานการณ์จำลองนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="54aaf-417">**วิธีการประมวลผลเวฟ:** คุณจะทำเครื่องหมายวิธีการป้ายชื่อเวฟเป็น "สามารถทำซ้ำได้" ให้เพิ่มสองครั้ง (หรือมากกว่า) ไปยังเท็มเพลตเวฟ และกำหนดรหัสขั้นตอนเวฟที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="54aaf-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="54aaf-418">**เท็มเพลตของป้ายชื่อเวฟ:** คุณจะตั้งค่าคอนฟิกเท็มเพลตของป้ายชื่อเวฟ และเชื่อมโยงกับเท็มเพลตของเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="54aaf-419">เท็มเพลตของป้ายชื่อเวฟแต่ละรายการมีชนิดป้ายชื่อเวฟของตนเอง</span><span class="sxs-lookup"><span data-stu-id="54aaf-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="54aaf-420">**โครงร่างป้ายชื่อเวฟ:** คุณจะสร้างโครงร่างป้ายชื่อเวฟหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="54aaf-421">จะมีโครงร่างป้ายชื่อที่แยกต่างหากสำหรับแต่ละ "ระดับ" ของป้ายชื่อ และจะมีโครงร่างป้ายชื่อการแบ่งด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="54aaf-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="54aaf-422">สถานการณ์จำลองนี้แสดงลำดับตั้งแต่ต้นจนจบ</span><span class="sxs-lookup"><span data-stu-id="54aaf-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="54aaf-423">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="54aaf-423">Make demo data available</span></span>

<span data-ttu-id="54aaf-424">เพื่อติดตามสถานการณ์จำลองนี้ คุณต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องเลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="54aaf-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="54aaf-425">ตั้งค่าวิธีการประมวลผลเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-425">Set up a wave process method</span></span>

1. <span data-ttu-id="54aaf-426">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> วิธีการประมวลผลเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="54aaf-427">ยืนยันว่า **waveLabelPrinting** อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="54aaf-428">ถ้าไม่มีอยู่ ให้เลือก **สร้างวิธีการใหม่** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="54aaf-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="54aaf-429">สำหรับวิธีการ **waveLabelPrinting** เลือกกล่องกาเครื่องหมาย **ทำให้วิธีการสามารถทำซ้ำได้**</span><span class="sxs-lookup"><span data-stu-id="54aaf-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="54aaf-430">การตั้งค่าเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-430">Set up a wave template</span></span>

1. <span data-ttu-id="54aaf-431">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="54aaf-432">เลือกเท็มเพลต เช่น **62 ค่าเริ่มต้นของการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="54aaf-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="54aaf-433">บน FastTab **วิธีการ** ให้ย้ายวิธีการ **การพิมพ์ป้ายชื่อเวฟ** ไปที่คอลัมน์ **วิธีการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="54aaf-434">ในคอลัมน์ **วิธีการที่เลือก** ให้กำหนดค่า **รหัสขั้นตอนของเวฟ** เช่น *กล่อง* ให้กับวิธีการ **การพิมพ์ป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="54aaf-435">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสขั้นตอนของเวฟ ให้ดูที่ [รหัสขั้นตอนของเวฟ](wave-step-codes.md)</span><span class="sxs-lookup"><span data-stu-id="54aaf-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="54aaf-436">ย้ายวิธีการ **การพิมพ์ป้ายชื่อเวฟ** ไปที่คอลัมน์ **วิธีการที่เลือก** ครั้งที่สอง</span><span class="sxs-lookup"><span data-stu-id="54aaf-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="54aaf-437">ในคอลัมน์ **วิธีการที่เลือก** ให้กำหนดค่า **รหัสขั้นตอนของเวฟ** ที่แตกต่างกัน เช่น *แท่นวางสินค้า* ให้กับวิธีการ **การพิมพ์ป้ายชื่อเวฟ** ที่สอง</span><span class="sxs-lookup"><span data-stu-id="54aaf-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="54aaf-438">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสขั้นตอนของเวฟ ให้ดูที่ [รหัสขั้นตอนของเวฟ](wave-step-codes.md)</span><span class="sxs-lookup"><span data-stu-id="54aaf-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="54aaf-439">สร้างโครงร่างป้ายชื่อเวฟสามรายการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="54aaf-440">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> โครงร่างป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="54aaf-441">สร้างเรกคอร์ดที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-442">**รหัสโครงร่างป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="54aaf-443">**คำอธิบาย:** *กล่อง (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="54aaf-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="54aaf-444">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="54aaf-445">ในบานหน้าต่างการดำเนินการ ให้เลือก **การตั้งค่าแถวของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="54aaf-446">หน้า **การตั้งค่าแถวของป้ายชื่อเวฟ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="54aaf-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="54aaf-447">ที่นี่ คุณสามารถตั้งค่าคอนฟิกส่วนไดนามิกของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="54aaf-448">เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-449">**รหัสแถว:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="54aaf-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="54aaf-450">**ชื่อตารางแถว:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="54aaf-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="54aaf-451">**ตำแหน่งเริ่มต้นของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="54aaf-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="54aaf-452">ฟิลด์นี้จะกำหนดตำแหน่งในแนวตั้งที่ซึ่งแถวจะเริ่มต้นบนป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="54aaf-453">**ความสูงของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="54aaf-453">**Row height:** *0*</span></span>

        <span data-ttu-id="54aaf-454">ฟิลด์นี้จะกำหนดความสูงของแต่ละแถว (ตามจุด) ตามมาตรฐาน ZPL</span><span class="sxs-lookup"><span data-stu-id="54aaf-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="54aaf-455">ความสูงของแถวเป็นค่าบวกสำหรับป้ายชื่อแนวนอน และค่าลบสำหรับป้ายชื่อแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="54aaf-456">เนื่องจากมีเพียงหนึ่งแถวเท่านั้นในตัวอย่างนี้ คุณสามารถตั้งค่าเป็น *0* (ศูนย์) ได้</span><span class="sxs-lookup"><span data-stu-id="54aaf-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="54aaf-457">**แถวต่อหน้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="54aaf-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="54aaf-458">ฟิลด์นี้จะกำหนดจำนวนของแถวที่สามารถพิมพ์บนป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="54aaf-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="54aaf-459">การตั้งค่านี้จะทำให้ป้ายชื่อ ZPL ที่แยกต่างหากถูกพิมพ์สำหรับเรกคอร์ดแต่ละรายการในตารางป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="54aaf-460">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-460">Close the page.</span></span>
1. <span data-ttu-id="54aaf-461">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="54aaf-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="54aaf-462">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-463">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-464">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-465">**ฟิลด์:** *ชนิดงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="54aaf-466">**เงื่อนไข:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="54aaf-467">การสอบถามนี้ช่วยให้มั่นใจว่า จะมีการพิมพ์เฉพาะรายการงานชนิดการเบิกสินค้าบนป้ายชื่อ ไม่ใช่รายการงานชนิดการส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="54aaf-468">ถ้าคุณต้องการสามารถพิมพ์รหัสใบตราส่ง บนแท็บ **รวม** เลือกตาราง **รายการงาน** และรวมตาราง **การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="54aaf-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="54aaf-469">ปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="54aaf-470">FastTab **โครงร่างข้อความของเครื่องพิมพ์** มีส่วนสามส่วนที่ซึ่งคุณสามารถเขียนรหัสเครื่องพิมพ์: **ส่วนของส่วนหัว** **ส่วนของเนื้อหา** และ **ส่วนของท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="54aaf-471">ใน **ส่วนของส่วนหัว** ในฟิลด์ **ส่วนหัวของป้ายชื่อ** ป้อนรหัสสำหรับส่วนหัวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="54aaf-472">ตัวอย่างเช่น ถ้าคุณกำลังใช้เครื่องพิมพ์ Zebra คุณสามารถใช้รหัสดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="54aaf-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="54aaf-473">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **เนื้อหาของป้ายชื่อ** ป้อนรหัส ZPL สำหรับเนื้อหาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="54aaf-474">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="54aaf-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="54aaf-475">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **ส่วนท้ายของป้ายชื่อ** ป้อนรหัส ZPL สำหรับส่วนท้ายที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="54aaf-476">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="54aaf-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="54aaf-477">การตั้งค่านี้จะพิมพ์สำเนาหนึ่งฉบับของป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="54aaf-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="54aaf-478">ถ้าคุณต้องการสำเนาเพิ่มเติม (ตัวอย่างเช่น สำเนาหนึ่งฉบับสำหรับแต่ละด้านของแท่นวางสินค้า) ให้ตั้งค่า **n** สำหรับส่วน **\^PQn** ในส่วนท้ายเป็นจำนวนสำเนาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="54aaf-479">ตัวอย่างเช่น ถ้าต้องการพิมพ์สำเนาสี่ฉบับของป้ายชื่อแต่ละป้าย ให้ระบุ **\^PQ4**</span><span class="sxs-lookup"><span data-stu-id="54aaf-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="54aaf-480">ในขณะนี้ป้ายชื่อแรกพร้อมที่จะใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="54aaf-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="54aaf-481">สร้างเรกคอร์ดโครงร่างที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-482">**รหัสโครงร่างป้ายชื่อ:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="54aaf-483">**คำอธิบาย:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="54aaf-484">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="54aaf-485">ในบานหน้าต่างการดำเนินการ ให้เลือก **การตั้งค่าแถวของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="54aaf-486">หน้า **การตั้งค่าแถวของป้ายชื่อเวฟ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="54aaf-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="54aaf-487">ที่นี่ คุณสามารถตั้งค่าคอนฟิกส่วนไดนามิกของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="54aaf-488">เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-489">**รหัสแถว:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="54aaf-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="54aaf-490">**ชื่อตารางแถว:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="54aaf-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="54aaf-491">**ตำแหน่งเริ่มต้นของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="54aaf-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="54aaf-492">ฟิลด์นี้จะกำหนดตำแหน่งในแนวตั้งที่ซึ่งแถวจะเริ่มต้นบนป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="54aaf-493">**ความสูงของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="54aaf-493">**Row height:** *0*</span></span>

        <span data-ttu-id="54aaf-494">ฟิลด์นี้จะกำหนดความสูงของแต่ละแถว (ตามจุด) ตามมาตรฐาน ZPL</span><span class="sxs-lookup"><span data-stu-id="54aaf-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="54aaf-495">ความสูงของแถวเป็นค่าบวกสำหรับป้ายชื่อแนวนอน และค่าลบสำหรับป้ายชื่อแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="54aaf-496">เนื่องจากมีเพียงหนึ่งแถวเท่านั้นในตัวอย่างนี้ คุณสามารถตั้งค่าเป็น *0* (ศูนย์) ได้</span><span class="sxs-lookup"><span data-stu-id="54aaf-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="54aaf-497">**แถวต่อหน้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="54aaf-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="54aaf-498">ฟิลด์นี้จะกำหนดจำนวนของแถวที่สามารถพิมพ์บนป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="54aaf-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="54aaf-499">การตั้งค่านี้จะทำให้ป้ายชื่อ ZPL ที่แยกต่างหากถูกพิมพ์ สำหรับเรกคอร์ดแต่ละรายการในตารางป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="54aaf-500">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-500">Close the page.</span></span>
1. <span data-ttu-id="54aaf-501">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="54aaf-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="54aaf-502">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-503">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-504">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-505">**ฟิลด์:** *ชนิดงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="54aaf-506">**เงื่อนไข:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="54aaf-507">การสอบถามนี้ช่วยให้มั่นใจว่า จะมีการพิมพ์เฉพาะรายการงานชนิดการเบิกสินค้าบนป้ายชื่อ ไม่ใช่รายการงานชนิดการส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="54aaf-508">ถ้าคุณต้องการสามารถพิมพ์รหัสใบตราส่ง บนแท็บ **รวม** เลือกตาราง **รายการงาน** และรวมตาราง **การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="54aaf-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="54aaf-509">ปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="54aaf-510">FastTab **โครงร่างข้อความของเครื่องพิมพ์** มีส่วนสามส่วนที่ซึ่งคุณสามารถเขียนรหัสเครื่องพิมพ์: **ส่วนของส่วนหัว** **ส่วนของเนื้อหา** และ **ส่วนของท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="54aaf-511">ใน **ส่วนของส่วนหัว** ในฟิลด์ **ส่วนหัวของป้ายชื่อ** ป้อนรหัสสำหรับส่วนหัวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="54aaf-512">ตัวอย่างเช่น ถ้าคุณกำลังใช้เครื่องพิมพ์ Zebra คุณสามารถใช้รหัสดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="54aaf-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="54aaf-513">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **เนื้อหาของป้ายชื่อ** ป้อนรหัส ZPL สำหรับเนื้อหาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="54aaf-514">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="54aaf-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="54aaf-515">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **ส่วนท้ายของป้ายชื่อ** ป้อนรหัส ZPL สำหรับส่วนท้ายที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="54aaf-516">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="54aaf-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="54aaf-517">การตั้งค่านี้จะพิมพ์สำเนาหนึ่งฉบับของป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="54aaf-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="54aaf-518">ถ้าคุณต้องการสำเนาเพิ่มเติม (ตัวอย่างเช่น สำเนาหนึ่งฉบับสำหรับแต่ละด้านของแท่นวางสินค้า) ให้ตั้งค่า **n** สำหรับส่วน **\^PQn** ในส่วนท้ายเป็นจำนวนสำเนาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="54aaf-519">ตัวอย่างเช่น ถ้าต้องการพิมพ์สำเนาสี่ฉบับของป้ายชื่อแต่ละป้าย ให้ระบุ **\^PQ4**</span><span class="sxs-lookup"><span data-stu-id="54aaf-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="54aaf-520">ในขณะนี้ป้ายชื่อที่สองพร้อมที่จะใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="54aaf-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="54aaf-521">สร้างเรกคอร์ดโครงร่างที่สามที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-522">**รหัสโครงร่างป้ายชื่อ:** *การแบ่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="54aaf-523">**คำอธิบาย:** *ป้ายชื่อการแบ่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="54aaf-524">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="54aaf-525">FastTab **โครงร่างข้อความของเครื่องพิมพ์** มีส่วนสามส่วนที่ซึ่งคุณสามารถเขียนรหัสเครื่องพิมพ์: **ส่วนของส่วนหัว** **ส่วนของเนื้อหา** และ **ส่วนของท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="54aaf-526">ในส่วน **ส่วนของส่วนหัว** ในฟิลด์ **ส่วนหัวของป้ายชื่อ** ป้อนรหัส ZPL สำหรับส่วนหัวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="54aaf-527">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="54aaf-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="54aaf-528">คราวนี้ ไม่ต้องการใครเลย</span><span class="sxs-lookup"><span data-stu-id="54aaf-528">This time, no body is required.</span></span> <span data-ttu-id="54aaf-529">ดังนั้น เพียงป้อนข้อความที่จำเป็นในส่วน **ส่วนท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="54aaf-530">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="54aaf-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="54aaf-531">ในขณะนี้ป้ายชื่อที่สามพร้อมที่จะใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="54aaf-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="54aaf-532">ป้ายชื่อที่สามนี้เป็นป้ายชื่อการแบ่งที่จะใช้เป็นตัวแบ่งระหว่างม้วนป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="54aaf-533">สร้างชนิดป้ายชื่อเวฟสองชนิด</span><span class="sxs-lookup"><span data-stu-id="54aaf-533">Create two wave label types</span></span>

1. <span data-ttu-id="54aaf-534">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> ชนิดป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="54aaf-535">สร้างเรกคอร์ดที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-536">**ชนิดป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="54aaf-537">**คำอธิบาย:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="54aaf-538">สร้างเรกคอร์ดที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-539">**ชนิดป้ายชื่อ:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="54aaf-540">**คำอธิบาย:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="54aaf-541">ตั้งค่ากลุ่มลำดับหน่วย</span><span class="sxs-lookup"><span data-stu-id="54aaf-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="54aaf-542">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> กลุ่มลำดับของหน่วย**</span><span class="sxs-lookup"><span data-stu-id="54aaf-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="54aaf-543">เลือกหรือสร้างกลุ่ม **ชิ้น กล่อง แท่นวางสินค้า**</span><span class="sxs-lookup"><span data-stu-id="54aaf-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="54aaf-544">สำหรับรายการ **กล่อง** ให้ตั้งค่าฟิลด์ **ชนิดระดับเวฟ** เป็น *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="54aaf-545">สำหรับรายการ **แท่นวางสินค้า** ให้ตั้งค่าฟิลด์ **ชนิดระดับเวฟ** เป็น *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="54aaf-546">สร้างเท็มเพลตของป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-546">Create wave label templates</span></span>

1. <span data-ttu-id="54aaf-547">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> เท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="54aaf-548">สร้างเท็มเพลตของป้ายชื่อที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-549">**ชื่อเท็มเพลตของป้ายชื่อ:** *ป้ายชื่อกล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="54aaf-550">**คำอธิบาย:** *ป้ายชื่อกล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="54aaf-551">**รหัสขั้นตอนของเวฟ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="54aaf-552">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="54aaf-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="54aaf-553">บน FastTab **ทั่วไป** ในฟิลด์ **ชนิดป้ายชื่อเวฟ** เลือกค่า เช่น *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="54aaf-554">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-555">**รหัสโครงร่างป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="54aaf-556">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์ ZPL ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="54aaf-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="54aaf-557">**รันการสอบถาม:** *ใช่* (การตั้งค่านี้ไม่จำเป็นต้องระบุ แต่ขอแนะนำให้ใช้ประสิทธิภาพสูงสุด)</span><span class="sxs-lookup"><span data-stu-id="54aaf-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="54aaf-558">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="54aaf-559">ไม่จำเป็นต้องระบุ: ถ้าคุณกำลังตั้งค่าการออกแบบป้ายชื่อเฉพาะลูกค้า คุณต้องสร้างการสอบถามเพื่อค้นหาบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="54aaf-560">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="54aaf-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="54aaf-561">จากนั้น ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-562">**ตาราง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="54aaf-563">**ตารางสืบทอด:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="54aaf-564">**ฟิลด์:** *หมายเลขบัญชี*</span><span class="sxs-lookup"><span data-stu-id="54aaf-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="54aaf-565">**เงื่อนไข:** ให้ป้อนหมายเลขบัญชีลูกค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="54aaf-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="54aaf-566">เมื่อคุณดำเนินการเสร็จสิ้น ให้เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="54aaf-567">ในบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไขการสอบถาม** เพื่อเปิดกล่องโต้ตอบตัวแก้ไขการสอบถามสำหรับเท็มเพลตป้ายชื่อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="54aaf-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="54aaf-568">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **การเรียงลำดับ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-569">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-570">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-571">**ฟิลด์:** *รหัสรายการของโหลดอ้างอิง (รหัสเรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="54aaf-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="54aaf-572">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="54aaf-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="54aaf-573">เพิ่มแถวที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-574">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-575">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-576">**ฟิลด์:** *รหัสการจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="54aaf-577">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="54aaf-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="54aaf-578">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="54aaf-579">กล่องข้อความจะพร้อมท์ให้คุณยืนยันการดำเนินการรีเซ็ตการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="54aaf-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="54aaf-580">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="54aaf-581">ในบานหน้าต่างการดำเนินการ ให้เลือก **กลุ่มเท็มเพลตป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="54aaf-582">ในกล่องโต้ตอบ **กลุ่มเท็มเพลตของป้ายชื่อเวฟ** สำหรับแถวที่มีการตั้งค่าฟิลด์ **ชื่อฟิลด์การอ้างอิง** เป็น *รหัสการจัดส่ง* ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="54aaf-583">**พิมพ์ป้ายชื่อการแบ่ง:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="54aaf-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="54aaf-584">**รหัสโครงร่างป้ายชื่อ:** เลือกป้ายชื่อการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="54aaf-585">(ตัวอย่างเช่น เลือกโครงร่างป้ายชื่อ *การแบ่ง* ที่คุณสร้างไว้ก่อนหน้านี้ในสถานการณ์นี้)</span><span class="sxs-lookup"><span data-stu-id="54aaf-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="54aaf-586">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์สำหรับป้ายชื่อการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="54aaf-587">(โดยทั่วไป สำหรับวัตถุประสงค์ของการแยกม้วนป้ายชื่อ คุณควรเลือกเครื่องพิมพ์เดียวกันกับที่เลือกบน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="54aaf-588">อย่างไรก็ตาม สถานการณ์อื่นๆ อาจเป็นไปได้)</span><span class="sxs-lookup"><span data-stu-id="54aaf-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="54aaf-589">สำหรับแถวที่ฟิลด์ **ชื่อฟิลด์การอ้างอิง** ถูกตั้งค่าเป็น *รหัสรายการโหลดอ้างอิง* ให้เลือกกล่องกาเครื่องหมาย **รหัสการสร้างป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="54aaf-590">การตั้งค่านี้จะสร้างลำดับป้ายชื่อหนึ่งลำดับ ("กล่อง 1 จาก X") สำหรับแต่ละรายการโหลดทั่วทั้งเวฟ โดยไม่คำนึงถึงการตั้งค่าการจัดกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="54aaf-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="54aaf-591">คุณสามารถพิมพ์ลำดับป้ายชื่อนี้บนโครงร่างป้ายชื่อได้</span><span class="sxs-lookup"><span data-stu-id="54aaf-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="54aaf-592">นอกจากนี้ ป้ายชื่อสำหรับการจัดส่งที่แตกต่างกันจะถูกแยกด้วยป้ายชื่อการแบ่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="54aaf-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="54aaf-593">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **กลุ่มเท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="54aaf-594">สร้างเท็มเพลตของป้ายชื่อที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-595">**ชื่อเท็มเพลตของป้ายชื่อ:** *ป้ายชื่อแท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="54aaf-596">**คำอธิบาย:** *ป้ายชื่อแท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="54aaf-597">**รหัสขั้นตอนของเวฟ:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="54aaf-598">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="54aaf-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="54aaf-599">บน FastTab **ทั่วไป** ในฟิลด์ **ชนิดป้ายชื่อเวฟ** เลือกค่า เช่น *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="54aaf-600">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-601">**รหัสโครงร่างป้ายชื่อ:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="54aaf-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="54aaf-602">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์ ZPL ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="54aaf-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="54aaf-603">**รันการสอบถาม:** *ใช่* (การตั้งค่านี้ไม่จำเป็นต้องระบุ แต่ขอแนะนำให้ใช้ประสิทธิภาพสูงสุด)</span><span class="sxs-lookup"><span data-stu-id="54aaf-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="54aaf-604">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="54aaf-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="54aaf-605">ไม่จำเป็นต้องระบุ: ถ้าคุณกำลังตั้งค่าการออกแบบป้ายชื่อเฉพาะลูกค้า คุณต้องสร้างการสอบถามเพื่อค้นหาบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="54aaf-606">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="54aaf-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="54aaf-607">จากนั้น ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-608">**ตาราง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="54aaf-609">**ตารางสืบทอด:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="54aaf-610">**ฟิลด์:** *หมายเลขบัญชี*</span><span class="sxs-lookup"><span data-stu-id="54aaf-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="54aaf-611">**เงื่อนไข:** ให้ป้อนหมายเลขบัญชีลูกค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="54aaf-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="54aaf-612">เมื่อคุณดำเนินการเสร็จสิ้น ให้เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="54aaf-613">ในบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไขการสอบถาม** เพื่อเปิดกล่องโต้ตอบตัวแก้ไขการสอบถามสำหรับเท็มเพลตป้ายชื่อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="54aaf-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="54aaf-614">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **การเรียงลำดับ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-615">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-616">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-617">**ฟิลด์:** *รหัสรายการของโหลดอ้างอิง (รหัสเรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="54aaf-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="54aaf-618">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="54aaf-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="54aaf-619">เพิ่มแถวที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-620">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-621">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="54aaf-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="54aaf-622">**ฟิลด์:** *รหัสการจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="54aaf-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="54aaf-623">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="54aaf-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="54aaf-624">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="54aaf-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="54aaf-625">กล่องข้อความจะพร้อมท์ให้คุณยืนยันการดำเนินการรีเซ็ตการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="54aaf-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="54aaf-626">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="54aaf-627">ในบานหน้าต่างการดำเนินการ ให้เลือก **กลุ่มเท็มเพลตป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="54aaf-628">ในกล่องโต้ตอบ **กลุ่มเท็มเพลตของป้ายชื่อเวฟ** สำหรับแถวที่มีการตั้งค่าฟิลด์ **ชื่อฟิลด์การอ้างอิง** เป็น *รหัสการจัดส่ง* ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="54aaf-629">**พิมพ์ป้ายชื่อการแบ่ง:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="54aaf-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="54aaf-630">**รหัสโครงร่างป้ายชื่อ:** เลือกป้ายชื่อการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="54aaf-631">(ตัวอย่างเช่น เลือกโครงร่างป้ายชื่อ *การแบ่ง* ที่คุณสร้างไว้ก่อนหน้านี้ในสถานการณ์นี้)</span><span class="sxs-lookup"><span data-stu-id="54aaf-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="54aaf-632">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์สำหรับป้ายชื่อการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="54aaf-633">(โดยทั่วไป สำหรับวัตถุประสงค์ของการแยกม้วนป้ายชื่อ คุณควรเลือกเครื่องพิมพ์เดียวกันกับที่เลือกบน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="54aaf-634">อย่างไรก็ตาม สถานการณ์อื่นๆ อาจเป็นไปได้)</span><span class="sxs-lookup"><span data-stu-id="54aaf-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="54aaf-635">สำหรับแถวที่ฟิลด์ **ชื่อฟิลด์การอ้างอิง** ถูกตั้งค่าเป็น *รหัสรายการโหลดอ้างอิง* ให้เลือกกล่องกาเครื่องหมาย **รหัสการสร้างป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="54aaf-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="54aaf-636">การตั้งค่านี้จะสร้างลำดับป้ายชื่อหนึ่งลำดับ ("กล่อง 1 จาก X") สำหรับแต่ละรายการโหลดทั่วทั้งเวฟ โดยไม่คำนึงถึงการตั้งค่าการจัดกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="54aaf-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="54aaf-637">คุณสามารถพิมพ์ลำดับป้ายชื่อนี้บนโครงร่างป้ายชื่อได้</span><span class="sxs-lookup"><span data-stu-id="54aaf-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="54aaf-638">นอกจากนี้ ป้ายชื่อสำหรับการจัดส่งที่แตกต่างกันจะถูกแยกด้วยป้ายชื่อการแบ่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="54aaf-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="54aaf-639">ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="54aaf-639">Configure number sequence extensions</span></span>

<span data-ttu-id="54aaf-640">ส่วนขยายของลำดับหมายเลขจะควบคุมการปฏิบัติตาม GS1 ของลำดับหมายเลขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="54aaf-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="54aaf-641">ไม่จำเป็นต้องระบุการตั้งค่าคอนฟิกนี้สำหรับสถานการณ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="54aaf-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="54aaf-642">สำหรับข้อมูลเพิ่มเติมและคำแนะนำในการตั้งค่าคอนฟิก ให้ดู [ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข](../warehousing/configure-number-sequence-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="54aaf-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="54aaf-643">สร้างใบสั่งขายและนำใบสั่งขายออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="54aaf-644">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="54aaf-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="54aaf-645">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="54aaf-646">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="54aaf-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="54aaf-647">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="54aaf-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="54aaf-648">เพิ่มรายการใบสั่งขายสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="54aaf-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="54aaf-649">รายการใบสั่งขายที่ 1:</span><span class="sxs-lookup"><span data-stu-id="54aaf-649">Sales order line 1:</span></span>

        - <span data-ttu-id="54aaf-650">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="54aaf-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="54aaf-651">**ปริมาณ:** *9024*</span><span class="sxs-lookup"><span data-stu-id="54aaf-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="54aaf-652">**หน่วย:** *ชิ้น* (9024 ชิ้น = 376 กล่อง = 47 แท่นวางสินค้า)</span><span class="sxs-lookup"><span data-stu-id="54aaf-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="54aaf-653">รายการใบสั่งขายที่ 2:</span><span class="sxs-lookup"><span data-stu-id="54aaf-653">Sales order line 2:</span></span>

        - <span data-ttu-id="54aaf-654">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="54aaf-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="54aaf-655">**ปริมาณ:** *9016*</span><span class="sxs-lookup"><span data-stu-id="54aaf-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="54aaf-656">**หน่วย:** *ชิ้น* (9016 ชิ้น = 322 กล่อง = 46 แท่นวางสินค้า)</span><span class="sxs-lookup"><span data-stu-id="54aaf-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="54aaf-657">สินค้าและปริมาณที่ให้ไว้ที่นี่คือตัวอย่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="54aaf-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="54aaf-658">พวกเขาต้องใช้กลุ่มลำดับหน่วยที่คุณได้กำหนดไว้ก่อนหน้านี้ การแปลงหน่วยที่เหมาะสมจาก *ชิ้น* เป็น *กล่อง* เป็น *แท่นวางสินค้า* ต้องถูกกำหนด และต้องมีสินค้าคงคลังในคลังสินค้า *62*</span><span class="sxs-lookup"><span data-stu-id="54aaf-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="54aaf-659">สำหรับข้อมูลเพิ่มเติม ให้ดู [นโยบายหน่วยวัดและการเก็บสต็อก](unit-measure-stocking-policies.md)</span><span class="sxs-lookup"><span data-stu-id="54aaf-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="54aaf-660">เลือกรายการในใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="54aaf-660">Select sales order line 1.</span></span> <span data-ttu-id="54aaf-661">จากนั้น ในส่วน **รายการใบสั่งขาย** บนเมนู **สินค้าคงคลัง** เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="54aaf-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="54aaf-662">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** และจากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="54aaf-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="54aaf-663">ทำซ้ำขั้นตอนที่ 4 และ 5 สำหรับรายการใบสั่งขายที่ 2</span><span class="sxs-lookup"><span data-stu-id="54aaf-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="54aaf-664">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="54aaf-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="54aaf-665">เหตุการณ์ต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="54aaf-665">The following events occur:</span></span> 

    - <span data-ttu-id="54aaf-666">ระบบจะประมวลผลการจัดส่งที่สร้างขึ้นโดยใช้เท็มเพลตที่มีขั้นตอนการพิมพ์ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="54aaf-667">โครงร่างป้ายชื่อจะถูกใช้เพื่อกำหนดรูปแบบของป้ายชื่อ และผลลัพธ์จะเป็นป้ายชื่อที่พิมพ์บนเครื่องพิมพ์ที่เลือกในเท็มเพลตของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="54aaf-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="54aaf-668">มีการสร้างและพิมพ์ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="54aaf-669">จำนวนของป้ายชื่อจะเท่ากับจำนวนของกล่อง (ในตัวอย่างนี้ ป้ายชื่อกล่อง 376 ป้ายสำหรับรายการที่ 1 ป้ายชื่อกล่อง 322 ป้ายสำหรับรายการที่่ 2 ป้ายชื่อแท่นวางสินค้า 47 ป้ายสำหรับรายการที่ 1 ป้ายชื่อแท่นวางสินค้า 47 ป้ายสำหรับรายการที่ 2 และป้ายชื่อการแบ่งสองป้ายที่มีรหัสการจัดส่ง)</span><span class="sxs-lookup"><span data-stu-id="54aaf-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="54aaf-670">รหัสใบตราส่งใหม่จะถูกสร้างขึ้นสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="54aaf-671">ถ้าคุณได้ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข รหัสป้ายชื่อเวฟจะเป็นไปตามรูปแบบหมายเลข **SSCC-18**</span><span class="sxs-lookup"><span data-stu-id="54aaf-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="54aaf-672">คุณสามารถดูและพิมพ์ป้ายชื่อเวฟอีกครั้งจากหน้าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="54aaf-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="54aaf-673">การจัดส่งทั้งหมด \> รายละเอียดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="54aaf-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="54aaf-674">โหลดทั้งหมด \> รายละเอียดโหลด</span><span class="sxs-lookup"><span data-stu-id="54aaf-674">All loads \> Load details</span></span>
- <span data-ttu-id="54aaf-675">เวฟทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="54aaf-675">All waves</span></span>
- <span data-ttu-id="54aaf-676">ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-676">Wave labels</span></span>
- <span data-ttu-id="54aaf-677">ประวัติป้ายชื่อของเวฟ</span><span class="sxs-lookup"><span data-stu-id="54aaf-677">Wave label history</span></span>

<span data-ttu-id="54aaf-678">สำหรับหน้าเหล่านี้ส่วนใหญ่ คุณสามารถค้นหาฟังก์ชันที่เกี่ยวข้องโดยการเลือก **ป้ายชื่อเวฟ** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** บนแท็บ **การจัดส่ง** ของบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="54aaf-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
