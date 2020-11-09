---
title: ตั้งค่าและใช้การพิมพ์ป้ายชื่อเวฟ
description: หัวข้อนี้จะอธิบายการพิมพ์ป้ายชื่อเวฟ และอธิบายวิธีการตั้งค่า
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: configure-wave-label-printing
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
ms.openlocfilehash: 1f51ed9f05caede3d4f320ddb6b705e67df9aa1f
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016970"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="756cb-103">ตั้งค่าและใช้การพิมพ์ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="756cb-104">การพิมพ์ป้ายชื่อเวฟมีแนวทางอื่นในการพิมพ์ป้ายชื่อโดยการแนะนำวิธีการขั้นตอนของเวฟใหม่ ซึ่งช่วยให้คุณสามารถสร้างและพิมพ์ป้ายชื่อได้โดยตรงจากเท็มเพลตของเวฟในระหว่างการดำเนินการเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="756cb-105">ดังนั้น ป้ายชื่อดังกล่าวจะพร้อมใช้งานอยู่แล้ว ก่อนที่ผู้ปฏิบัติงานจะรันใบสั่งงานบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="756cb-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="756cb-106">จากนั้น ผู้ปฏิบัติงานจึงสามารถแนบป้ายชื่อที่ต้องการได้ในระหว่างการเบิกสินค้า แทนที่จะเป็นหลังจากการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="756cb-107">การพิมพ์ป้ายชื่อเวฟใช้ Zebra Programming Language (ZPL) เพื่อสร้างโครงร่างป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="756cb-108">โครงร่างป้ายชื่อถูกแบ่งออกเป็นสามส่วน (ส่วนหัว เนื้อหา และท้ายกระดาษ) เพื่ออนุญาตป้ายชื่อที่มีโครงสร้างการทำซ้ำ</span><span class="sxs-lookup"><span data-stu-id="756cb-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="756cb-109">เท็มเพลตของป้ายชื่อเวฟจะบอกให้ระบบทราบถึงโครงร่างป้ายชื่อที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="756cb-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="756cb-110">ผู้ใช้สามารถระบุเครื่องพิมพ์ที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="756cb-110">Users can specify which printer is used.</span></span> <span data-ttu-id="756cb-111">นอกจากนี้ พวกเขายังสามารถพิมพ์ป้ายชื่อบนเครื่องพิมพ์หลายเครื่องพร้อมกันได้ตามที่พวกเขาต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="756cb-112">หน้า **ประวัติป้ายชื่อเวฟ** แสดงเรกคอร์ดของป้ายชื่อทั้งหมดที่สร้างขึ้นโดยใช้การตั้งค่านี้</span><span class="sxs-lookup"><span data-stu-id="756cb-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="756cb-113">คุณสามารถพิมพ์และเรียงป้ายชื่อตามส่วนหัวของงาน คุณสามารถพิมพ์ป้ายชื่อการแบ่งสำหรับส่วนหัวของงานแต่ละส่วน และคุณสามารถพิมพ์ป้ายชื่อเนื้อหาของคอนเทนเนอร์ ป้ายชื่อกรณี และป้ายชื่อที่คล้ายกันอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="756cb-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="756cb-114">ฟังก์ชันนี้ไม่ได้แทนที่ฟังก์ชันการพิมพ์ป้ายชื่อที่มีอยู่ซึ่งยึดตามการกำหนดเส้นทางเอกสาร</span><span class="sxs-lookup"><span data-stu-id="756cb-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="756cb-115">การพิมพ์ป้ายชื่อเวฟให้การปรับปรุงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="756cb-116">พิมพ์ป้ายชื่อตามจำนวนของกล่องบนบรรทัดงานหนึ่งๆ โดยไม่ใช้การบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="756cb-117">("กล่อง" เป็นหน่วยที่กำหนดไว้ในบรรทัดกลุ่มลำดับของหน่วย)</span><span class="sxs-lookup"><span data-stu-id="756cb-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="756cb-118">พิมพ์ลำดับป้ายชื่อที่แตกต่างกันหลายรายการ (ตัวอย่างเช่น ป้ายชื่อกล่องและแท่นวางสินค้า)</span><span class="sxs-lookup"><span data-stu-id="756cb-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="756cb-119">ประกอบด้วยการแจงนับป้ายชื่อ (ตัวอย่างเช่น 1/124, 2/124, ... 124/124) และกำหนดช่วงของการแจงนับ (ตัวอย่างเช่น รายการงาน รายการโหลด หรือการจัดส่ง)</span><span class="sxs-lookup"><span data-stu-id="756cb-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="756cb-120">สร้างและพิมพ์รหัสใบตราส่งบนป้ายชื่อ ก่อนที่จะมีการสร้างใบตราส่ง</span><span class="sxs-lookup"><span data-stu-id="756cb-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="756cb-121">สร้างรหัสคอนเทนเนอร์การจัดส่งสินค้าที่ไม่ซ้ำกัน (SSCC) สำหรับแต่ละกล่อง และรวมไว้ในป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="756cb-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="756cb-122">สร้างลำดับหมายเลขที่สอดคล้องกับ GS1 สำหรับรหัสใบตราส่งและ SSCCs</span><span class="sxs-lookup"><span data-stu-id="756cb-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="756cb-123">พิมพ์ป้ายชื่อใหม่จากทั้งอุปกรณ์เคลื่อนที่และไคลเอนต์ที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="756cb-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="756cb-124">ยกเลิกป้ายชื่อ (ตัวอย่างเช่น ในสถานการณ์การเบิกสินค้าที่ขาด) และพิมพ์ใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="756cb-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="756cb-125">ล้างข้อมูลประวัติป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="756cb-126">การปรับปรุงไปยังโครงร่างการกำหนดเส้นทางเอกสารถูกใช้ร่วมกันระหว่างโครงร่างการกำหนดเส้นทางเอกสารและโครงร่างป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="756cb-127">(สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [โครงร่างการกำหนดเส้นทางเอกสารสำหรับป้ายทะเบียน](../warehousing/document-routing-layout-for-license-plates.md))</span><span class="sxs-lookup"><span data-stu-id="756cb-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="756cb-128">การปรับปรุงเหล่านี้ทำให้มีประสิทธิภาพมากขึ้นในการติดป้ายชื่อกล่องก่อนการวางบนแท่นวางสินค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="756cb-129">โดยเฉพาะอย่างยิ่ง เป็นประโยชน์สำหรับบริษัทที่จัดส่งไปยังร้านค้าปลีกขนาดใหญ่ที่ยืนยันการรับสินค้าตามใบสั่งโดยอัตโนมัติโดยการสแกนกล่องแต่ละกล่องโดยแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="756cb-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="756cb-130">คุณสามารถใช้สถานการณ์จำลองการตั้งค่าคอนฟิกที่อธิบายไว้ในหัวข้อนี้โดยแยกต่างหากหรือใช้ร่วมกันได้ ทั้งนี้ขึ้นอยู่กับความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="756cb-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="756cb-131">คุณสามารถออกแบบเท็มเพลตป้ายชื่อเวฟต่างๆ ที่ทำงานอยู่ในลำดับ (ดังที่แสดงในสถานการณ์จำลอง 3)</span><span class="sxs-lookup"><span data-stu-id="756cb-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="756cb-132">ตัวอย่างเช่น คุณสามารถใช้สถานการณ์จำลอง 1 เพื่อพิมพ์ป้ายชื่อกล่อง และสถานการณ์จำลอง 2 เพื่อพิมพ์ป้ายชื่อแท่นวางสินค้า (ถ้าแท่นวางสินค้าในสต็อกแตกต่างกันในขนาดและองค์ประกอบ)</span><span class="sxs-lookup"><span data-stu-id="756cb-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="756cb-133">เปิดคุณลักษณะการพิมพ์ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="756cb-134">ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การพิมพ์ป้ายชื่อเวฟ* ต้องมีการเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="756cb-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="756cb-135">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="756cb-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="756cb-136">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="756cb-137">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="756cb-138">**ชื่อคุณลักษณะ:** *การพิมพ์ป้ายชื่อเวฟ*</span><span class="sxs-lookup"><span data-stu-id="756cb-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="756cb-139">สถานการณ์จำลอง 1: การพิมพ์ป้ายชื่อเวฟที่มีการสร้างป้ายชื่อเวฟเดียว</span><span class="sxs-lookup"><span data-stu-id="756cb-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="756cb-140">สถานการณ์นี้แสดงวิธีการที่บริษัทสามารถพิมพ์ป้ายชื่อการจัดส่งสำหรับผู้ค้าปลีกขนาดใหญ่ที่ยืนยันการรับสินค้าตามใบสั่งโดยอัตโนมัติโดยการสแกนกล่องแต่ละกล่องโดยแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="756cb-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="756cb-141">สถานการณ์จำลองนี้แสดงลำดับตั้งแต่ต้นจนจบ</span><span class="sxs-lookup"><span data-stu-id="756cb-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="756cb-142">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="756cb-142">Make demo data available</span></span>

<span data-ttu-id="756cb-143">เพื่อติดตามสถานการณ์จำลองนี้ คุณต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องเลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="756cb-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="756cb-144">ตรวจสอบให้แน่ใจว่าวิธีการป้ายชื่อเวฟพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="756cb-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="756cb-145">คุณอาจต้องสร้างวิธีการประมวลผลเวฟของคุณใหม่เพื่อทำให้วิธีการพิมพ์ป้ายชื่อเวฟพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="756cb-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="756cb-146">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> วิธีการประมวลผลเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="756cb-147">ยืนยันว่า **waveLabelPrinting** อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="756cb-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="756cb-148">ถ้าไม่มีอยู่ ให้เลือก **สร้างวิธีการใหม่** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="756cb-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="756cb-149">ตั้งค่าคอนฟิกเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-149">Configure a wave template</span></span>

<span data-ttu-id="756cb-150">เท็มเพลตเวฟช่วยให้คุณสามารถเชื่อมโยงอินสแตนซ์ที่เฉพาะเจาะจงของวิธีการเวฟไปยังเท็มเพลตป้ายชื่อเวฟที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="756cb-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="756cb-151">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="756cb-152">เลือกเท็มเพลต เช่น **62 ค่าเริ่มต้นของการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="756cb-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="756cb-153">บน FastTab **วิธีการ** ให้ย้ายวิธีการ **การพิมพ์ป้ายชื่อเวฟ** ไปที่คอลัมน์ **วิธีการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="756cb-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="756cb-154">ในคอลัมน์ **วิธีการที่เลือก** ให้เลือกวิธีการ **การพิมพ์ป้ายชื่อเวฟ** และตั้งค่าฟิลด์ **รหัสขั้นตอนของเวฟ** เป็น *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="756cb-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="756cb-155">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสขั้นตอนของเวฟ ให้ดูที่ [รหัสขั้นตอนของเวฟ](wave-step-codes.md)</span><span class="sxs-lookup"><span data-stu-id="756cb-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="756cb-156">สร้างโครงร่างป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-156">Create a wave label layout</span></span>

<span data-ttu-id="756cb-157">โครงร่างป้ายชื่อจะควบคุมข้อมูลที่จะพิมพ์บนป้ายชื่อและวิธีการจัดวางข้อมูลของป้ายชื่อ ที่นี่ คุณป้อนรหัส ZPL ที่ส่งไปยังเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="756cb-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="756cb-158">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> โครงร่างป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="756cb-159">สร้างเรกคอร์ดที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="756cb-160">**รหัสโครงร่างป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="756cb-161">**คำอธิบาย:** *กล่อง (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="756cb-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="756cb-162">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="756cb-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="756cb-163">ในบานหน้าต่างการดำเนินการ ให้เลือก **การตั้งค่าแถวของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="756cb-164">หน้า **การตั้งค่าแถวของป้ายชื่อเวฟ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="756cb-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="756cb-165">ที่นี่ คุณสามารถตั้งค่าคอนฟิกส่วนไดนามิกของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="756cb-166">เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-167">**รหัสแถว:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="756cb-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="756cb-168">**ชื่อตารางแถว:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="756cb-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="756cb-169">**ตำแหน่งเริ่มต้นของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="756cb-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="756cb-170">ฟิลด์นี้จะกำหนดตำแหน่งในแนวตั้งที่ซึ่งแถวจะเริ่มต้นบนป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="756cb-171">**ความสูงของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="756cb-171">**Row height:** *0*</span></span>

        <span data-ttu-id="756cb-172">ฟิลด์นี้จะกำหนดความสูงของแต่ละแถว (ตามจุด) ตามมาตรฐาน ZPL</span><span class="sxs-lookup"><span data-stu-id="756cb-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="756cb-173">ความสูงของแถวเป็นค่าบวกสำหรับป้ายชื่อแนวนอน และค่าลบสำหรับป้ายชื่อแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="756cb-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="756cb-174">เนื่องจากมีเพียงหนึ่งแถวเท่านั้นในตัวอย่างนี้ คุณสามารถตั้งค่าเป็น *0* (ศูนย์) ได้</span><span class="sxs-lookup"><span data-stu-id="756cb-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="756cb-175">**แถวต่อหน้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="756cb-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="756cb-176">ฟิลด์นี้จะกำหนดจำนวนของแถวที่สามารถพิมพ์บนป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="756cb-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="756cb-177">การตั้งค่านี้จะทำให้ป้ายชื่อ ZPL ที่แยกต่างหากถูกพิมพ์สำหรับเรกคอร์ดแต่ละรายการในตารางป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="756cb-178">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="756cb-178">Close the page.</span></span>
1. <span data-ttu-id="756cb-179">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="756cb-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="756cb-180">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-181">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-182">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-183">**ฟิลด์:** *ชนิดงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="756cb-184">**เงื่อนไข:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="756cb-185">การสอบถามนี้ช่วยให้มั่นใจว่า จะมีการพิมพ์เฉพาะรายการงานชนิดการเบิกสินค้าบนป้ายชื่อ ไม่ใช่รายการงานชนิดการส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="756cb-186">ถ้าคุณต้องการสามารถพิมพ์รหัสใบตราส่ง บนแท็บ **รวม** เลือกตาราง **รายการงาน** และรวมตาราง **การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="756cb-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="756cb-187">ปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="756cb-188">FastTab **โครงร่างข้อความของเครื่องพิมพ์** มีส่วนสามส่วนที่ซึ่งคุณสามารถเขียนรหัสเครื่องพิมพ์: **ส่วนของส่วนหัว** **ส่วนของเนื้อหา** และ **ส่วนของท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="756cb-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="756cb-189">ใน **ส่วนของส่วนหัว** ในฟิลด์ **ส่วนหัวของป้ายชื่อ** ป้อนรหัสสำหรับส่วนหัวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="756cb-190">ตัวอย่างเช่น ถ้าคุณกำลังใช้เครื่องพิมพ์ Zebra คุณสามารถใช้รหัสดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="756cb-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

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

1. <span data-ttu-id="756cb-191">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **เนื้อหาของป้ายชื่อ** ป้อนรหัส ZPL สำหรับเนื้อหาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="756cb-192">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="756cb-192">Here is an example.</span></span>

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

1. <span data-ttu-id="756cb-193">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **ส่วนท้ายของป้ายชื่อ** ป้อนรหัส ZPL สำหรับส่วนท้ายที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="756cb-194">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="756cb-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="756cb-195">การตั้งค่านี้จะพิมพ์สำเนาหนึ่งฉบับของป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="756cb-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="756cb-196">ถ้าคุณต้องการสำเนาเพิ่มเติม (ตัวอย่างเช่น สำเนาหนึ่งฉบับสำหรับแต่ละด้านของแท่นวางสินค้า) ให้ตั้งค่า **n** สำหรับส่วน **\^PQn** ในส่วนท้ายเป็นจำนวนสำเนาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="756cb-197">ตัวอย่างเช่น ถ้าต้องการพิมพ์สำเนาสี่ฉบับของป้ายชื่อแต่ละป้าย ให้ระบุ **\^PQ4**</span><span class="sxs-lookup"><span data-stu-id="756cb-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="756cb-198">ในขณะนี้ป้ายชื่อของคุณพร้อมที่จะใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="756cb-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="756cb-199">สร้างชนิดป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-199">Create a wave label type</span></span>

<span data-ttu-id="756cb-200">ชนิดป้ายชื่อเวฟถูกใช้เพื่อลิงค์เท็มเพลตของป้ายชื่อเวฟกับหน่วยในรายการกลุ่มลำดับหน่วย</span><span class="sxs-lookup"><span data-stu-id="756cb-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="756cb-201">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> ชนิดป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="756cb-202">เพิ่มชนิดป้ายชื่อเวฟที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="756cb-203">**ชนิดป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="756cb-204">**คำอธิบาย:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="756cb-205">ตั้งค่ากลุ่มลำดับหน่วย</span><span class="sxs-lookup"><span data-stu-id="756cb-205">Set up unit sequence groups</span></span>

<span data-ttu-id="756cb-206">ถัดไป ให้ตั้งค่ากลุ่มลำดับของหน่วยสำหรับชนิดป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="756cb-207">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> กลุ่มลำดับของหน่วย**</span><span class="sxs-lookup"><span data-stu-id="756cb-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="756cb-208">เลือกกลุ่ม **Ea Box PL**</span><span class="sxs-lookup"><span data-stu-id="756cb-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="756cb-209">สำหรับรายการ **กล่อง** ให้ตั้งค่าฟิลด์ **ชนิดระดับเวฟ** เป็น *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="756cb-210">สร้างเท็มเพลตของป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-210">Create a wave label template</span></span>

<span data-ttu-id="756cb-211">ถัดไป ให้สร้างเท็มเพลตของป้ายชื่อเวฟสำหรับชนิดป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="756cb-212">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> เท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="756cb-213">เพิ่มเท็มเพลตของระดับเวฟ และตั้งค่าค่าต่อไปนี้ในส่วนหัว:</span><span class="sxs-lookup"><span data-stu-id="756cb-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="756cb-214">**ชื่อเท็มเพลตของป้ายชื่อ:** *ป้ายชื่อกล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="756cb-215">**คำอธิบาย:** *ป้ายชื่อกล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="756cb-216">**รหัสขั้นตอนของเวฟ:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="756cb-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="756cb-217">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="756cb-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="756cb-218">บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **ชนิดป้ายชื่อเวฟ** เป็น *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="756cb-219">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เพิ่มแถวใหม่ที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-220">**รหัสโครงร่างป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="756cb-221">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์ ZPL ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="756cb-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="756cb-222">**รันการสอบถาม:** *ใช่* (การตั้งค่านี้ไม่จำเป็นต้องระบุ แต่ขอแนะนำให้ใช้ประสิทธิภาพสูงสุด)</span><span class="sxs-lookup"><span data-stu-id="756cb-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="756cb-223">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="756cb-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="756cb-224">ไม่จำเป็นต้องระบุ: ถ้าคุณกำลังตั้งค่าการออกแบบป้ายชื่อเฉพาะลูกค้า คุณต้องสร้างการสอบถามเพื่อค้นหาบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="756cb-225">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="756cb-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="756cb-226">จากนั้น ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-227">**ตาราง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="756cb-228">**ตารางสืบทอด:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="756cb-229">**ฟิลด์:** *หมายเลขบัญชี*</span><span class="sxs-lookup"><span data-stu-id="756cb-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="756cb-230">**เงื่อนไข:** ให้ป้อนหมายเลขบัญชีลูกค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="756cb-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="756cb-231">เมื่อคุณดำเนินการเสร็จสิ้น ให้เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="756cb-232">ในบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไขการสอบถาม** เพื่อเปิดกล่องโต้ตอบตัวแก้ไขการสอบถามสำหรับเท็มเพลตป้ายชื่อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="756cb-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="756cb-233">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **การเรียงลำดับ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-234">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-235">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-236">**ฟิลด์:** *รหัสรายการของโหลดอ้างอิง (รหัสเรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="756cb-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="756cb-237">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="756cb-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="756cb-238">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="756cb-239">กล่องข้อความจะพร้อมท์ให้คุณยืนยันการดำเนินการรีเซ็ตการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="756cb-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="756cb-240">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="756cb-241">ในบานหน้าต่างการดำเนินการ ให้เลือก **กลุ่มเท็มเพลตป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="756cb-242">ในกล่องโต้ตอบ **กลุ่มเท็มเพลตป้ายชื่อเวฟ** ให้เลือกแถวที่มีการตั้งค่าฟิลด์ **ชื่อฟิลด์การอ้างอิง** เป็น *รหัสรายการโหลดอ้างอิง* และจากนั้น เลือกกล่องกาเครื่องหมาย **รหัสการสร้างป้ายชื่อ** สำหรับแถวนี้</span><span class="sxs-lookup"><span data-stu-id="756cb-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id* , and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="756cb-243">การตั้งค่านี้จะสร้างลำดับป้ายชื่อหนึ่งลำดับ ("กล่อง 1 จาก X") สำหรับแต่ละรายการโหลดทั่วทั้งเวฟ โดยไม่คำนึงถึงการตั้งค่าการจัดกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="756cb-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="756cb-244">คุณสามารถพิมพ์ลำดับป้ายชื่อนี้บนโครงร่างป้ายชื่อได้</span><span class="sxs-lookup"><span data-stu-id="756cb-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="756cb-245">ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="756cb-245">Configure number sequence extensions</span></span>

<span data-ttu-id="756cb-246">ส่วนขยายของลำดับหมายเลขจะควบคุมการปฏิบัติตาม GS1 ของลำดับหมายเลขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="756cb-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="756cb-247">ไม่จำเป็นต้องระบุการตั้งค่าคอนฟิกนี้สำหรับสถานการณ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="756cb-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="756cb-248">สำหรับข้อมูลเพิ่มเติมและคำแนะนำในการตั้งค่าคอนฟิก ให้ดู [ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข](../warehousing/configure-number-sequence-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="756cb-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="756cb-249">สร้างใบสั่งขายและนำใบสั่งขายออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="756cb-250">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="756cb-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="756cb-251">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="756cb-252">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="756cb-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="756cb-253">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="756cb-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="756cb-254">เพิ่มรายการขายสองรายการที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="756cb-255">รายการใบสั่งขายที่ 1:</span><span class="sxs-lookup"><span data-stu-id="756cb-255">Sales order line 1:</span></span>

        - <span data-ttu-id="756cb-256">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="756cb-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="756cb-257">**ปริมาณ:** *9024*</span><span class="sxs-lookup"><span data-stu-id="756cb-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="756cb-258">**หน่วย:** *ชิ้น* (9024 ชิ้น = 376 กล่อง = 47 แท่นวางสินค้า)</span><span class="sxs-lookup"><span data-stu-id="756cb-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="756cb-259">รายการใบสั่งขายที่ 2:</span><span class="sxs-lookup"><span data-stu-id="756cb-259">Sales order line 2:</span></span>

        - <span data-ttu-id="756cb-260">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="756cb-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="756cb-261">**ปริมาณ:** *9016*</span><span class="sxs-lookup"><span data-stu-id="756cb-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="756cb-262">**หน่วย:** *ชิ้น* (9016 ชิ้น = 322 กล่อง = 46 แท่นวางสินค้า)</span><span class="sxs-lookup"><span data-stu-id="756cb-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="756cb-263">สินค้าและปริมาณที่ให้ไว้ที่นี่คือตัวอย่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="756cb-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="756cb-264">พวกเขาต้องใช้กลุ่มลำดับหน่วยที่คุณได้กำหนดไว้ก่อนหน้านี้ การแปลงหน่วยที่เหมาะสมจาก *ชิ้น* เป็น *กล่อง* เป็น *แท่นวางสินค้า* ต้องถูกกำหนด และต้องมีสินค้าคงคลังในคลังสินค้า *62*</span><span class="sxs-lookup"><span data-stu-id="756cb-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="756cb-265">สำหรับข้อมูลเพิ่มเติม ให้ดู [นโยบายหน่วยวัดและการเก็บสต็อก](unit-measure-stocking-policies.md)</span><span class="sxs-lookup"><span data-stu-id="756cb-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="756cb-266">เลือกรายการในใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="756cb-266">Select sales order line 1.</span></span> <span data-ttu-id="756cb-267">จากนั้น ในส่วน **รายการใบสั่งขาย** บนเมนู **สินค้าคงคลัง** เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="756cb-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="756cb-268">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** และจากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="756cb-268">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="756cb-269">ทำซ้ำขั้นตอนที่ 4 และ 5 สำหรับรายการใบสั่งขายที่ 2</span><span class="sxs-lookup"><span data-stu-id="756cb-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="756cb-270">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="756cb-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="756cb-271">เหตุการณ์ต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="756cb-271">The following events occur:</span></span>

    - <span data-ttu-id="756cb-272">ระบบจะประมวลผลการจัดส่งที่สร้างขึ้นโดยใช้เท็มเพลตที่มีขั้นตอนการพิมพ์ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="756cb-273">โครงร่างป้ายชื่อจะถูกใช้เพื่อกำหนดรูปแบบของป้ายชื่อ และผลลัพธ์จะเป็นป้ายชื่อที่พิมพ์บนเครื่องพิมพ์ที่เลือกในเท็มเพลตของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="756cb-274">มีการสร้างและพิมพ์ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="756cb-275">จำนวนของป้ายชื่อจะเท่ากับจำนวนของกล่อง (ในตัวอย่างนี้ ป้ายชื่อของกล่อง 376 ป้ายสำหรับรายการที่ 1 และป้ายชื่อกล่อง 322 ป้ายสำหรับรายการที่ 2)</span><span class="sxs-lookup"><span data-stu-id="756cb-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="756cb-276">รหัสใบตราส่งใหม่จะถูกสร้างขึ้นสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="756cb-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="756cb-277">ถ้าคุณได้ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข รหัสป้ายชื่อเวฟจะเป็นไปตามรูปแบบหมายเลข **SSCC-18**</span><span class="sxs-lookup"><span data-stu-id="756cb-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="756cb-278">คุณสามารถดูและพิมพ์ป้ายชื่อเวฟอีกครั้งจากหน้าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="756cb-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="756cb-279">บนบานหน้าต่างการดำเนินการของหน้าแต่ละหน้า บนแท็บ **การจัดส่ง** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **ป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="756cb-280">การจัดส่งทั้งหมด \> รายละเอียดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="756cb-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="756cb-281">โหลดทั้งหมด \> รายละเอียดโหลด</span><span class="sxs-lookup"><span data-stu-id="756cb-281">All loads \> Load details</span></span>
- <span data-ttu-id="756cb-282">เวฟทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="756cb-282">All waves</span></span>
- <span data-ttu-id="756cb-283">ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-283">Wave labels</span></span>
- <span data-ttu-id="756cb-284">ประวัติป้ายชื่อของเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="756cb-285">สถานการณ์จำลองที่ 2: การพิมพ์ป้ายชื่อเวฟสำหรับการบรรจุลงตู้บรรจุสินค้า (โดยไม่มีเรกคอร์ดป้ายชื่อเวฟ)</span><span class="sxs-lookup"><span data-stu-id="756cb-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="756cb-286">สถานการณ์นี้ช่วยให้คุณสามารถพิมพ์ป้ายชื่อเวฟได้ เมื่อคุณใช้การบรรจุลงตู้บรรจุสินค้าเพื่อแบ่งสินค้าลงในกล่องโดยอัตโนมัติ และดังนั้นจึงไม่ต้องใช้เรกคอร์ดของป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="756cb-287">ในกรณีนี้ รหัสคอนเทนเนอร์ทำหน้าที่เป็นตัวยึดตำแหน่งสำหรับ SSCC</span><span class="sxs-lookup"><span data-stu-id="756cb-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="756cb-288">ต่อไปนี้คือความแตกต่างที่สำคัญระหว่างสถานการณ์จำลองนี้และสถานการณ์จำลอง 1:</span><span class="sxs-lookup"><span data-stu-id="756cb-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="756cb-289">**เท็มเพลตของป้ายชื่อเวฟ:** คุณจะไม่เลือกชนิดป้ายชื่อเวฟบนเท็มเพลตของป้ายชื่อเวฟ และคุณไม่จำเป็นต้องมีการจัดกลุ่มการสร้างป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="756cb-290">มิฉะนั้น คุณจะตั้งค่าคอนฟิกเท็มเพลตของป้ายชื่อเวฟ และลิงค์ไปยังเท็มเพลตเวฟในลักษณะเดียวกับที่อธิบายไว้ในสถานการณ์จำลอง 1</span><span class="sxs-lookup"><span data-stu-id="756cb-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="756cb-291">คุณต้องปล่อยชนิดป้ายชื่อเวฟให้ว่างไว้ เพื่อป้องกันไม่ให้มีการสร้างป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="756cb-292">**โครงร่างป้ายชื่อเวฟ:** คุณจะตั้งค่าคอนฟิกการตั้งค่าแถวของโครงร่างป้ายชื่อเวฟสำหรับรายการงาน แทนที่จะเป็นเรกคอร์ดของป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="756cb-293">คุณต้องตั้งค่าคอนฟิกการตั้งค่าแถวสำหรับโครงร่างป้ายชื่อโดยใช้ตาราง **WHSWorkLine** แทนตาราง **WHSWaveLabel**</span><span class="sxs-lookup"><span data-stu-id="756cb-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="756cb-294">การตั้งค่า **แถวต่อหน้า** จะควบคุมจำนวนของแถวที่ส่วนเนื้อหาจะมี</span><span class="sxs-lookup"><span data-stu-id="756cb-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="756cb-295">นอกจากนี้ การตั้งค่าคอนฟิกนี้ยังเหมาะสำหรับสถานการณ์จำลองทางธุรกิจ ที่ซึ่งสินค้าที่แตกต่างกันหลายรายการถูกบรรจุอยู่ในกล่องที่มีการระบุชื่อหนึ่งกล่องหรือในแท่นวางสินค้า และสามารถกำหนดกระบวนการบรรจุนี้ได้โดยการสร้างงาน (ตัวอย่างเช่น งานที่จัดกลุ่มตามการจัดส่ง)</span><span class="sxs-lookup"><span data-stu-id="756cb-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="756cb-296">สถานการณ์จำลองนี้แสดงลำดับตั้งแต่ต้นจนจบ</span><span class="sxs-lookup"><span data-stu-id="756cb-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="756cb-297">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="756cb-297">Make demo data available</span></span>

<span data-ttu-id="756cb-298">เพื่อติดตามสถานการณ์จำลองนี้ คุณต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องเลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="756cb-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="756cb-299">ตรวจสอบให้แน่ใจว่าวิธีการป้ายชื่อเวฟพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="756cb-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="756cb-300">คุณอาจต้องสร้างวิธีการประมวลผลเวฟของคุณใหม่เพื่อทำให้วิธีการพิมพ์ป้ายชื่อเวฟพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="756cb-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="756cb-301">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> วิธีการประมวลผลเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="756cb-302">ยืนยันว่า **waveLabelPrinting** อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="756cb-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="756cb-303">ถ้าไม่มีอยู่ ให้เลือก **สร้างวิธีการใหม่** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="756cb-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="756cb-304">การตั้งค่าเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-304">Set up a wave template</span></span>

<span data-ttu-id="756cb-305">เท็มเพลตเวฟช่วยให้คุณสามารถเชื่อมโยงอินสแตนซ์ที่เฉพาะเจาะจงของวิธีการเวฟไปยังเท็มเพลตป้ายชื่อเวฟที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="756cb-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="756cb-306">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="756cb-307">เลือกเท็มเพลต เช่น **63 การบรรจุลงตู้บรรจุสินค้า**</span><span class="sxs-lookup"><span data-stu-id="756cb-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="756cb-308">บน FastTab **วิธีการ** ให้ย้ายวิธีการ **การพิมพ์ป้ายชื่อเวฟ** ไปที่คอลัมน์ **วิธีการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="756cb-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="756cb-309">ในคอลัมน์ **วิธีการที่เลือก** ให้เลือกวิธีการ **การพิมพ์ป้ายชื่อเวฟ** และตั้งค่าฟิลด์ **รหัสขั้นตอนของเวฟ** เป็น *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="756cb-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="756cb-310">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสขั้นตอนของเวฟ ให้ดูที่ [รหัสขั้นตอนของเวฟ](wave-step-codes.md)</span><span class="sxs-lookup"><span data-stu-id="756cb-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="756cb-311">สร้างโครงร่างป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-311">Create a wave label layout</span></span>

1. <span data-ttu-id="756cb-312">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> โครงร่างป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="756cb-313">สร้างเรกคอร์ดที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="756cb-314">**รหัสโครงร่างป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="756cb-315">**คำอธิบาย:** *กล่อง (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="756cb-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="756cb-316">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="756cb-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="756cb-317">ในบานหน้าต่างการดำเนินการ ให้เลือก **การตั้งค่าแถวของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="756cb-318">หน้า **การตั้งค่าแถวของป้ายชื่อเวฟ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="756cb-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="756cb-319">ที่นี่ คุณสามารถตั้งค่าคอนฟิกส่วนไดนามิกของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="756cb-320">เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-321">**รหัสแถว:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="756cb-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="756cb-322">**ชื่อตารางแถว:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="756cb-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="756cb-323">**ตำแหน่งเริ่มต้นของแถว:** *500*</span><span class="sxs-lookup"><span data-stu-id="756cb-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="756cb-324">ฟิลด์นี้จะกำหนดตำแหน่งในแนวตั้งที่ซึ่งแถวจะเริ่มต้นบนป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="756cb-325">**ความสูงของแถว:** *-50*</span><span class="sxs-lookup"><span data-stu-id="756cb-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="756cb-326">ฟิลด์นี้จะกำหนดความสูงของแต่ละแถว</span><span class="sxs-lookup"><span data-stu-id="756cb-326">This field defines the height of each row.</span></span> <span data-ttu-id="756cb-327">ความสูงของแถวเป็นค่าบวกสำหรับป้ายชื่อแนวนอน และค่าลบสำหรับป้ายชื่อแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="756cb-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="756cb-328">**แถวต่อหน้า:** *5*</span><span class="sxs-lookup"><span data-stu-id="756cb-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="756cb-329">ฟิลด์นี้จะกำหนดจำนวนของแถวที่สามารถพิมพ์บนป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="756cb-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="756cb-330">การตั้งค่านี้จะพิมพ์ป้ายชื่อ ZPL หลายป้ายสำหรับแต่ละงาน โดยที่แต่ละหน้าสามารถจัดเก็บรายการงานได้สูงสุดห้ารายการ</span><span class="sxs-lookup"><span data-stu-id="756cb-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="756cb-331">ตัวอย่างเช่น ถ้ามีการพิมพ์ป้ายชื่อสำหรับคอนเทนเนอร์ที่มี 12 รายการ จะมีการพิมพ์ป้ายชื่อสามป้าย</span><span class="sxs-lookup"><span data-stu-id="756cb-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="756cb-332">ถ้าคุณต้องการพิมพ์ป้ายชื่อแยกต่างหากสำหรับรายการเบิกสินค้าแต่ละรายการ ให้ตั้งค่านี้เป็น *1*</span><span class="sxs-lookup"><span data-stu-id="756cb-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="756cb-333">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="756cb-333">Close the page.</span></span>
1. <span data-ttu-id="756cb-334">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="756cb-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="756cb-335">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-336">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-337">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-338">**ฟิลด์:** *ชนิดงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="756cb-339">**เงื่อนไข:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="756cb-340">ถ้าคุณต้องการสามารถพิมพ์รหัสใบตราส่ง บนแท็บ **รวม** เลือกตาราง **รายการงาน** และรวมตาราง **การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="756cb-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="756cb-341">ปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="756cb-342">FastTab **โครงร่างข้อความของเครื่องพิมพ์** มีส่วนสามส่วนที่ซึ่งคุณสามารถเขียนรหัสเครื่องพิมพ์: **ส่วนของส่วนหัว** **ส่วนของเนื้อหา** และ **ส่วนของท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="756cb-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="756cb-343">ใน **ส่วนของส่วนหัว** ในฟิลด์ **ส่วนหัวของป้ายชื่อ** ป้อนรหัสสำหรับส่วนหัวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="756cb-344">ตัวอย่างเช่น ถ้าคุณกำลังใช้เครื่องพิมพ์ Zebra คุณสามารถใช้รหัสดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="756cb-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="756cb-345">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **เนื้อหาของป้ายชื่อ** ป้อนรหัส ZPL สำหรับเนื้อหาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="756cb-346">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="756cb-346">Here is an example.</span></span>

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

1. <span data-ttu-id="756cb-347">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **ส่วนท้ายของป้ายชื่อ** ป้อนรหัส ZPL สำหรับส่วนท้ายที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="756cb-348">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="756cb-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="756cb-349">การตั้งค่านี้จะพิมพ์สำเนาหนึ่งฉบับของป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="756cb-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="756cb-350">ถ้าคุณต้องการสำเนาเพิ่มเติม (ตัวอย่างเช่น สำเนาหนึ่งฉบับสำหรับแต่ละด้านของแท่นวางสินค้า) ให้ตั้งค่า **n** สำหรับส่วน **\^PQn** ในส่วนท้ายเป็นจำนวนสำเนาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="756cb-351">ตัวอย่างเช่น ถ้าต้องการพิมพ์สำเนาสี่ฉบับของป้ายชื่อแต่ละป้าย ให้ระบุ **\^PQ4**</span><span class="sxs-lookup"><span data-stu-id="756cb-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="756cb-352">ในขณะนี้ป้ายชื่อของคุณพร้อมที่จะใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="756cb-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="756cb-353">สร้างเท็มเพลตของป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-353">Create a wave label template</span></span>

1. <span data-ttu-id="756cb-354">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> เท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="756cb-355">เพิ่มเท็มเพลตของระดับเวฟ และตั้งค่าค่าต่อไปนี้ในส่วนหัว:</span><span class="sxs-lookup"><span data-stu-id="756cb-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="756cb-356">**ชื่อเท็มเพลตของป้ายชื่อ:** *ป้ายชื่อคอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="756cb-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="756cb-357">**คำอธิบาย:** *ป้ายชื่อคอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="756cb-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="756cb-358">**รหัสขั้นตอนของเวฟ:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="756cb-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="756cb-359">**คลังสินค้า:** *63*</span><span class="sxs-lookup"><span data-stu-id="756cb-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="756cb-360">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-361">**รหัสโครงร่างป้ายชื่อ:** *คอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="756cb-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="756cb-362">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์ ZPL ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="756cb-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="756cb-363">**รันการสอบถาม:** *ใช่* (การตั้งค่านี้ไม่จำเป็นต้องระบุ แต่ขอแนะนำให้ใช้ประสิทธิภาพสูงสุด)</span><span class="sxs-lookup"><span data-stu-id="756cb-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="756cb-364">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="756cb-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="756cb-365">ไม่จำเป็นต้องระบุ: ถ้าคุณกำลังตั้งค่าการออกแบบป้ายชื่อเฉพาะลูกค้า คุณต้องสร้างการสอบถามเพื่อค้นหาบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="756cb-366">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="756cb-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="756cb-367">จากนั้น ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-368">**ตาราง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="756cb-369">**ตารางสืบทอด:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="756cb-370">**ฟิลด์:** *หมายเลขบัญชี*</span><span class="sxs-lookup"><span data-stu-id="756cb-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="756cb-371">**เงื่อนไข:** ให้ป้อนหมายเลขบัญชีลูกค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="756cb-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="756cb-372">เมื่อคุณดำเนินการเสร็จสิ้น ให้เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="756cb-373">ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="756cb-373">Configure number sequence extensions</span></span>

<span data-ttu-id="756cb-374">ส่วนขยายของลำดับหมายเลขจะควบคุมการปฏิบัติตาม GS1 ของลำดับหมายเลขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="756cb-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="756cb-375">ไม่จำเป็นต้องระบุการตั้งค่าคอนฟิกนี้สำหรับสถานการณ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="756cb-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="756cb-376">สำหรับข้อมูลเพิ่มเติมและคำแนะนำในการตั้งค่าคอนฟิก ให้ดู [ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข](../warehousing/configure-number-sequence-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="756cb-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="756cb-377">สร้างใบสั่งขายและนำใบสั่งขายออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="756cb-378">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="756cb-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="756cb-379">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="756cb-380">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="756cb-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="756cb-381">**คลังสินค้า:** *63*</span><span class="sxs-lookup"><span data-stu-id="756cb-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="756cb-382">เพิ่มรายการใบสั่งขายห้ารายการ:</span><span class="sxs-lookup"><span data-stu-id="756cb-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="756cb-383">รายการใบสั่งขายที่ 1:</span><span class="sxs-lookup"><span data-stu-id="756cb-383">Sales order line 1:</span></span>

        - <span data-ttu-id="756cb-384">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="756cb-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="756cb-385">**ปริมาณ:** *10*</span><span class="sxs-lookup"><span data-stu-id="756cb-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="756cb-386">รายการใบสั่งขายที่ 2:</span><span class="sxs-lookup"><span data-stu-id="756cb-386">Sales order line 2:</span></span>

        - <span data-ttu-id="756cb-387">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="756cb-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="756cb-388">**ปริมาณ:** *20*</span><span class="sxs-lookup"><span data-stu-id="756cb-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="756cb-389">รายการใบสั่งขายที่ 3:</span><span class="sxs-lookup"><span data-stu-id="756cb-389">Sales order line 3:</span></span>

        - <span data-ttu-id="756cb-390">**หมายเลขสินค้า:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="756cb-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="756cb-391">**ปริมาณ:** *20*</span><span class="sxs-lookup"><span data-stu-id="756cb-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="756cb-392">รายการใบสั่งขายที่ 4:</span><span class="sxs-lookup"><span data-stu-id="756cb-392">Sales order line 4:</span></span>

        - <span data-ttu-id="756cb-393">**หมายเลขสินค้า:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="756cb-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="756cb-394">**ปริมาณ:** *40*</span><span class="sxs-lookup"><span data-stu-id="756cb-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="756cb-395">รายการใบสั่งขายที่ 5:</span><span class="sxs-lookup"><span data-stu-id="756cb-395">Sales order line 5:</span></span>

        - <span data-ttu-id="756cb-396">**หมายเลขสินค้า:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="756cb-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="756cb-397">**ปริมาณ:** *50*</span><span class="sxs-lookup"><span data-stu-id="756cb-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="756cb-398">สินค้าและปริมาณที่ให้ไว้ที่นี่คือตัวอย่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="756cb-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="756cb-399">ต้องมีสินค้าคงคลังในคลังสินค้าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="756cb-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="756cb-400">เลือกรายการในใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="756cb-400">Select sales order line 1.</span></span> <span data-ttu-id="756cb-401">จากนั้น ในส่วน **รายการใบสั่งขาย** บนเมนู **สินค้าคงคลัง** เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="756cb-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="756cb-402">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** และจากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="756cb-402">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="756cb-403">ทำซ้ำขั้นตอนที่ 4 และ 5 สำหรับรายการใบสั่งขายเพิ่มเติมแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="756cb-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="756cb-404">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="756cb-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="756cb-405">เหตุการณ์ต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="756cb-405">The following events occur:</span></span>

    - <span data-ttu-id="756cb-406">ระบบจะประมวลผลการจัดส่งที่สร้างขึ้นโดยใช้เท็มเพลตที่มีขั้นตอนการพิมพ์ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="756cb-407">โครงร่างป้ายชื่อจะถูกใช้เพื่อกำหนดรูปแบบของป้ายชื่อ และผลลัพธ์สุดท้ายจะเป็นป้ายชื่อที่มีห้ารายการและที่พิมพ์บนเครื่องพิมพ์ที่เลือกในเท็มเพลตของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="756cb-408">รหัสใบตราส่งใหม่จะถูกสร้างขึ้นสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="756cb-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="756cb-409">ถ้าคุณได้ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข รหัสป้ายชื่อเวฟจะเป็นไปตามรูปแบบหมายเลข **SSCC-18**</span><span class="sxs-lookup"><span data-stu-id="756cb-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="756cb-410">คุณสามารถพิมพ์ป้ายชื่อเวฟเหล่านี้ใหม่ได้โดยไปที่ **การจัดการคลังสินค้า \> การสอบถามและรายงาน \> ประวัติป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="756cb-411">สถานการณ์จำลอง 3: การพิมพ์ป้ายชื่อเวฟสำหรับป้ายชื่อแบบหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="756cb-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="756cb-412">สถานการณ์นี้แสดงวิธีการใช้ฟังก์ชันการพิมพ์ป้ายชื่อเวฟ เมื่อกระบวนการคลังสินค้าต้องมีป้ายชื่อการจัดส่งหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="756cb-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="756cb-413">ตัวอย่างเช่น อาจต้องพิมพ์ป้ายชื่อที่แยกต่างหากสำหรับกล่องและแท่นวางสินค้า และอาจต้องพิมพ์ป้ายชื่อการแบ่งสำหรับการจัดส่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="756cb-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="756cb-414">ป้ายชื่อการแบ่งเป็นชนิดที่แยกต่างหากของป้ายชื่อที่สามารถใช้เป็นตัวแบ่งระหว่างม้วนและคอนเทนเนอร์ เช่น ป้ายชื่อสำหรับรหัสการจัดส่งและบาร์โค้ด เพื่อให้สามารถเรียงลำดับป้ายชื่อได้ง่าย หลังจากที่มีการพิมพ์</span><span class="sxs-lookup"><span data-stu-id="756cb-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="756cb-415">ความแตกต่างที่สำคัญระหว่างการตั้งค่าคอนฟิกของสถานการณ์จำลองนี้และการตั้งค่าคอนฟิกของสถานการณ์จำลอง 1 นอกจากข้อเท็จจริงที่ว่ามีการเปิดใช้งานป้ายชื่อการแบ่ง คือชนิดป้ายชื่อเวฟหลายชนิดต้องเชื่อมโยงกับเท็มเพลตของป้ายชื่อเวฟและรายการกลุ่มลำดับหน่วย</span><span class="sxs-lookup"><span data-stu-id="756cb-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="756cb-416">เมื่อต้องการทำให้การตั้งค่าคอนฟิกนี้เสร็จสิ้น คุณจะตั้งค่าองค์ประกอบต่อไปนี้สำหรับสถานการณ์จำลองนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="756cb-417">**วิธีการประมวลผลเวฟ:** คุณจะทำเครื่องหมายวิธีการป้ายชื่อเวฟเป็น "สามารถทำซ้ำได้" ให้เพิ่มสองครั้ง (หรือมากกว่า) ไปยังเท็มเพลตเวฟ และกำหนดรหัสขั้นตอนเวฟที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="756cb-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="756cb-418">**เท็มเพลตของป้ายชื่อเวฟ:** คุณจะตั้งค่าคอนฟิกเท็มเพลตของป้ายชื่อเวฟ และเชื่อมโยงกับเท็มเพลตของเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="756cb-419">เท็มเพลตของป้ายชื่อเวฟแต่ละรายการมีชนิดป้ายชื่อเวฟของตนเอง</span><span class="sxs-lookup"><span data-stu-id="756cb-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="756cb-420">**โครงร่างป้ายชื่อเวฟ:** คุณจะสร้างโครงร่างป้ายชื่อเวฟหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="756cb-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="756cb-421">จะมีโครงร่างป้ายชื่อที่แยกต่างหากสำหรับแต่ละ "ระดับ" ของป้ายชื่อ และจะมีโครงร่างป้ายชื่อการแบ่งด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="756cb-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="756cb-422">สถานการณ์จำลองนี้แสดงลำดับตั้งแต่ต้นจนจบ</span><span class="sxs-lookup"><span data-stu-id="756cb-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="756cb-423">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="756cb-423">Make demo data available</span></span>

<span data-ttu-id="756cb-424">เพื่อติดตามสถานการณ์จำลองนี้ คุณต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องเลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="756cb-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="756cb-425">ตั้งค่าวิธีการประมวลผลเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-425">Set up a wave process method</span></span>

1. <span data-ttu-id="756cb-426">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> วิธีการประมวลผลเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="756cb-427">ยืนยันว่า **waveLabelPrinting** อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="756cb-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="756cb-428">ถ้าไม่มีอยู่ ให้เลือก **สร้างวิธีการใหม่** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="756cb-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="756cb-429">สำหรับวิธีการ **waveLabelPrinting** เลือกกล่องกาเครื่องหมาย **ทำให้วิธีการสามารถทำซ้ำได้**</span><span class="sxs-lookup"><span data-stu-id="756cb-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="756cb-430">การตั้งค่าเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-430">Set up a wave template</span></span>

1. <span data-ttu-id="756cb-431">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="756cb-432">เลือกเท็มเพลต เช่น **62 ค่าเริ่มต้นของการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="756cb-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="756cb-433">บน FastTab **วิธีการ** ให้ย้ายวิธีการ **การพิมพ์ป้ายชื่อเวฟ** ไปที่คอลัมน์ **วิธีการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="756cb-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="756cb-434">ในคอลัมน์ **วิธีการที่เลือก** ให้กำหนดค่า **รหัสขั้นตอนของเวฟ** เช่น *กล่อง* ให้กับวิธีการ **การพิมพ์ป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton* , to the **Wave label printing** method.</span></span> <span data-ttu-id="756cb-435">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสขั้นตอนของเวฟ ให้ดูที่ [รหัสขั้นตอนของเวฟ](wave-step-codes.md)</span><span class="sxs-lookup"><span data-stu-id="756cb-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="756cb-436">ย้ายวิธีการ **การพิมพ์ป้ายชื่อเวฟ** ไปที่คอลัมน์ **วิธีการที่เลือก** ครั้งที่สอง</span><span class="sxs-lookup"><span data-stu-id="756cb-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="756cb-437">ในคอลัมน์ **วิธีการที่เลือก** ให้กำหนดค่า **รหัสขั้นตอนของเวฟ** ที่แตกต่างกัน เช่น *แท่นวางสินค้า* ให้กับวิธีการ **การพิมพ์ป้ายชื่อเวฟ** ที่สอง</span><span class="sxs-lookup"><span data-stu-id="756cb-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet* , to the second **Wave label printing** method.</span></span> <span data-ttu-id="756cb-438">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสขั้นตอนของเวฟ ให้ดูที่ [รหัสขั้นตอนของเวฟ](wave-step-codes.md)</span><span class="sxs-lookup"><span data-stu-id="756cb-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="756cb-439">สร้างโครงร่างป้ายชื่อเวฟสามรายการ</span><span class="sxs-lookup"><span data-stu-id="756cb-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="756cb-440">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> โครงร่างป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="756cb-441">สร้างเรกคอร์ดที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="756cb-442">**รหัสโครงร่างป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="756cb-443">**คำอธิบาย:** *กล่อง (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="756cb-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="756cb-444">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="756cb-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="756cb-445">ในบานหน้าต่างการดำเนินการ ให้เลือก **การตั้งค่าแถวของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="756cb-446">หน้า **การตั้งค่าแถวของป้ายชื่อเวฟ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="756cb-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="756cb-447">ที่นี่ คุณสามารถตั้งค่าคอนฟิกส่วนไดนามิกของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="756cb-448">เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-449">**รหัสแถว:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="756cb-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="756cb-450">**ชื่อตารางแถว:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="756cb-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="756cb-451">**ตำแหน่งเริ่มต้นของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="756cb-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="756cb-452">ฟิลด์นี้จะกำหนดตำแหน่งในแนวตั้งที่ซึ่งแถวจะเริ่มต้นบนป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="756cb-453">**ความสูงของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="756cb-453">**Row height:** *0*</span></span>

        <span data-ttu-id="756cb-454">ฟิลด์นี้จะกำหนดความสูงของแต่ละแถว (ตามจุด) ตามมาตรฐาน ZPL</span><span class="sxs-lookup"><span data-stu-id="756cb-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="756cb-455">ความสูงของแถวเป็นค่าบวกสำหรับป้ายชื่อแนวนอน และค่าลบสำหรับป้ายชื่อแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="756cb-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="756cb-456">เนื่องจากมีเพียงหนึ่งแถวเท่านั้นในตัวอย่างนี้ คุณสามารถตั้งค่าเป็น *0* (ศูนย์) ได้</span><span class="sxs-lookup"><span data-stu-id="756cb-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="756cb-457">**แถวต่อหน้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="756cb-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="756cb-458">ฟิลด์นี้จะกำหนดจำนวนของแถวที่สามารถพิมพ์บนป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="756cb-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="756cb-459">การตั้งค่านี้จะทำให้ป้ายชื่อ ZPL ที่แยกต่างหากถูกพิมพ์สำหรับเรกคอร์ดแต่ละรายการในตารางป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="756cb-460">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="756cb-460">Close the page.</span></span>
1. <span data-ttu-id="756cb-461">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="756cb-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="756cb-462">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-463">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-464">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-465">**ฟิลด์:** *ชนิดงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="756cb-466">**เงื่อนไข:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="756cb-467">การสอบถามนี้ช่วยให้มั่นใจว่า จะมีการพิมพ์เฉพาะรายการงานชนิดการเบิกสินค้าบนป้ายชื่อ ไม่ใช่รายการงานชนิดการส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="756cb-468">ถ้าคุณต้องการสามารถพิมพ์รหัสใบตราส่ง บนแท็บ **รวม** เลือกตาราง **รายการงาน** และรวมตาราง **การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="756cb-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="756cb-469">ปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="756cb-470">FastTab **โครงร่างข้อความของเครื่องพิมพ์** มีส่วนสามส่วนที่ซึ่งคุณสามารถเขียนรหัสเครื่องพิมพ์: **ส่วนของส่วนหัว** **ส่วนของเนื้อหา** และ **ส่วนของท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="756cb-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="756cb-471">ใน **ส่วนของส่วนหัว** ในฟิลด์ **ส่วนหัวของป้ายชื่อ** ป้อนรหัสสำหรับส่วนหัวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="756cb-472">ตัวอย่างเช่น ถ้าคุณกำลังใช้เครื่องพิมพ์ Zebra คุณสามารถใช้รหัสดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="756cb-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


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

1. <span data-ttu-id="756cb-473">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **เนื้อหาของป้ายชื่อ** ป้อนรหัส ZPL สำหรับเนื้อหาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="756cb-474">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="756cb-474">Here is an example.</span></span>

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

1. <span data-ttu-id="756cb-475">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **ส่วนท้ายของป้ายชื่อ** ป้อนรหัส ZPL สำหรับส่วนท้ายที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="756cb-476">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="756cb-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="756cb-477">การตั้งค่านี้จะพิมพ์สำเนาหนึ่งฉบับของป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="756cb-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="756cb-478">ถ้าคุณต้องการสำเนาเพิ่มเติม (ตัวอย่างเช่น สำเนาหนึ่งฉบับสำหรับแต่ละด้านของแท่นวางสินค้า) ให้ตั้งค่า **n** สำหรับส่วน **\^PQn** ในส่วนท้ายเป็นจำนวนสำเนาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="756cb-479">ตัวอย่างเช่น ถ้าต้องการพิมพ์สำเนาสี่ฉบับของป้ายชื่อแต่ละป้าย ให้ระบุ **\^PQ4**</span><span class="sxs-lookup"><span data-stu-id="756cb-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="756cb-480">ในขณะนี้ป้ายชื่อแรกพร้อมที่จะใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="756cb-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="756cb-481">สร้างเรกคอร์ดโครงร่างที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="756cb-482">**รหัสโครงร่างป้ายชื่อ:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="756cb-483">**คำอธิบาย:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="756cb-484">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="756cb-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="756cb-485">ในบานหน้าต่างการดำเนินการ ให้เลือก **การตั้งค่าแถวของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="756cb-486">หน้า **การตั้งค่าแถวของป้ายชื่อเวฟ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="756cb-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="756cb-487">ที่นี่ คุณสามารถตั้งค่าคอนฟิกส่วนไดนามิกของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="756cb-488">เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-489">**รหัสแถว:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="756cb-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="756cb-490">**ชื่อตารางแถว:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="756cb-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="756cb-491">**ตำแหน่งเริ่มต้นของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="756cb-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="756cb-492">ฟิลด์นี้จะกำหนดตำแหน่งในแนวตั้งที่ซึ่งแถวจะเริ่มต้นบนป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="756cb-493">**ความสูงของแถว:** *0*</span><span class="sxs-lookup"><span data-stu-id="756cb-493">**Row height:** *0*</span></span>

        <span data-ttu-id="756cb-494">ฟิลด์นี้จะกำหนดความสูงของแต่ละแถว (ตามจุด) ตามมาตรฐาน ZPL</span><span class="sxs-lookup"><span data-stu-id="756cb-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="756cb-495">ความสูงของแถวเป็นค่าบวกสำหรับป้ายชื่อแนวนอน และค่าลบสำหรับป้ายชื่อแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="756cb-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="756cb-496">เนื่องจากมีเพียงหนึ่งแถวเท่านั้นในตัวอย่างนี้ คุณสามารถตั้งค่าเป็น *0* (ศูนย์) ได้</span><span class="sxs-lookup"><span data-stu-id="756cb-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="756cb-497">**แถวต่อหน้า:** *1*</span><span class="sxs-lookup"><span data-stu-id="756cb-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="756cb-498">ฟิลด์นี้จะกำหนดจำนวนของแถวที่สามารถพิมพ์บนป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="756cb-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="756cb-499">การตั้งค่านี้จะทำให้ป้ายชื่อ ZPL ที่แยกต่างหากถูกพิมพ์ สำหรับเรกคอร์ดแต่ละรายการในตารางป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="756cb-500">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="756cb-500">Close the page.</span></span>
1. <span data-ttu-id="756cb-501">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="756cb-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="756cb-502">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-503">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-504">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-505">**ฟิลด์:** *ชนิดงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="756cb-506">**เงื่อนไข:** *เบิกสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="756cb-507">การสอบถามนี้ช่วยให้มั่นใจว่า จะมีการพิมพ์เฉพาะรายการงานชนิดการเบิกสินค้าบนป้ายชื่อ ไม่ใช่รายการงานชนิดการส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="756cb-508">ถ้าคุณต้องการสามารถพิมพ์รหัสใบตราส่ง บนแท็บ **รวม** เลือกตาราง **รายการงาน** และรวมตาราง **การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="756cb-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="756cb-509">ปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="756cb-510">FastTab **โครงร่างข้อความของเครื่องพิมพ์** มีส่วนสามส่วนที่ซึ่งคุณสามารถเขียนรหัสเครื่องพิมพ์: **ส่วนของส่วนหัว** **ส่วนของเนื้อหา** และ **ส่วนของท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="756cb-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="756cb-511">ใน **ส่วนของส่วนหัว** ในฟิลด์ **ส่วนหัวของป้ายชื่อ** ป้อนรหัสสำหรับส่วนหัวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="756cb-512">ตัวอย่างเช่น ถ้าคุณกำลังใช้เครื่องพิมพ์ Zebra คุณสามารถใช้รหัสดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="756cb-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="756cb-513">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **เนื้อหาของป้ายชื่อ** ป้อนรหัส ZPL สำหรับเนื้อหาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="756cb-514">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="756cb-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="756cb-515">ในส่วน **ส่วนของเนื้อหา** ในฟิลด์ **ส่วนท้ายของป้ายชื่อ** ป้อนรหัส ZPL สำหรับส่วนท้ายที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="756cb-516">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="756cb-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="756cb-517">การตั้งค่านี้จะพิมพ์สำเนาหนึ่งฉบับของป้ายชื่อแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="756cb-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="756cb-518">ถ้าคุณต้องการสำเนาเพิ่มเติม (ตัวอย่างเช่น สำเนาหนึ่งฉบับสำหรับแต่ละด้านของแท่นวางสินค้า) ให้ตั้งค่า **n** สำหรับส่วน **\^PQn** ในส่วนท้ายเป็นจำนวนสำเนาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="756cb-519">ตัวอย่างเช่น ถ้าต้องการพิมพ์สำเนาสี่ฉบับของป้ายชื่อแต่ละป้าย ให้ระบุ **\^PQ4**</span><span class="sxs-lookup"><span data-stu-id="756cb-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="756cb-520">ในขณะนี้ป้ายชื่อที่สองพร้อมที่จะใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="756cb-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="756cb-521">สร้างเรกคอร์ดโครงร่างที่สามที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="756cb-522">**รหัสโครงร่างป้ายชื่อ:** *การแบ่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="756cb-523">**คำอธิบาย:** *ป้ายชื่อการแบ่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="756cb-524">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="756cb-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="756cb-525">FastTab **โครงร่างข้อความของเครื่องพิมพ์** มีส่วนสามส่วนที่ซึ่งคุณสามารถเขียนรหัสเครื่องพิมพ์: **ส่วนของส่วนหัว** **ส่วนของเนื้อหา** และ **ส่วนของท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="756cb-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="756cb-526">ในส่วน **ส่วนของส่วนหัว** ในฟิลด์ **ส่วนหัวของป้ายชื่อ** ป้อนรหัส ZPL สำหรับส่วนหัวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="756cb-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="756cb-527">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="756cb-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="756cb-528">คราวนี้ ไม่ต้องการใครเลย</span><span class="sxs-lookup"><span data-stu-id="756cb-528">This time, no body is required.</span></span> <span data-ttu-id="756cb-529">ดังนั้น เพียงป้อนข้อความที่จำเป็นในส่วน **ส่วนท้ายกระดาษ**</span><span class="sxs-lookup"><span data-stu-id="756cb-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="756cb-530">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="756cb-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="756cb-531">ในขณะนี้ป้ายชื่อที่สามพร้อมที่จะใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="756cb-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="756cb-532">ป้ายชื่อที่สามนี้เป็นป้ายชื่อการแบ่งที่จะใช้เป็นตัวแบ่งระหว่างม้วนป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="756cb-533">สร้างชนิดป้ายชื่อเวฟสองชนิด</span><span class="sxs-lookup"><span data-stu-id="756cb-533">Create two wave label types</span></span>

1. <span data-ttu-id="756cb-534">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> ชนิดป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="756cb-535">สร้างเรกคอร์ดที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="756cb-536">**ชนิดป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="756cb-537">**คำอธิบาย:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="756cb-538">สร้างเรกคอร์ดที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="756cb-539">**ชนิดป้ายชื่อ:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="756cb-540">**คำอธิบาย:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="756cb-541">ตั้งค่ากลุ่มลำดับหน่วย</span><span class="sxs-lookup"><span data-stu-id="756cb-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="756cb-542">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> กลุ่มลำดับของหน่วย**</span><span class="sxs-lookup"><span data-stu-id="756cb-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="756cb-543">เลือกหรือสร้างกลุ่ม **ชิ้น กล่อง แท่นวางสินค้า**</span><span class="sxs-lookup"><span data-stu-id="756cb-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="756cb-544">สำหรับรายการ **กล่อง** ให้ตั้งค่าฟิลด์ **ชนิดระดับเวฟ** เป็น *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="756cb-545">สำหรับรายการ **แท่นวางสินค้า** ให้ตั้งค่าฟิลด์ **ชนิดระดับเวฟ** เป็น *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="756cb-546">สร้างเท็มเพลตของป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-546">Create wave label templates</span></span>

1. <span data-ttu-id="756cb-547">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การกำหนดเส้นทางเอกสาร \> เท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="756cb-548">สร้างเท็มเพลตของป้ายชื่อที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="756cb-549">**ชื่อเท็มเพลตของป้ายชื่อ:** *ป้ายชื่อกล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="756cb-550">**คำอธิบาย:** *ป้ายชื่อกล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="756cb-551">**รหัสขั้นตอนของเวฟ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="756cb-552">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="756cb-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="756cb-553">บน FastTab **ทั่วไป** ในฟิลด์ **ชนิดป้ายชื่อเวฟ** เลือกค่า เช่น *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="756cb-554">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-555">**รหัสโครงร่างป้ายชื่อ:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="756cb-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="756cb-556">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์ ZPL ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="756cb-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="756cb-557">**รันการสอบถาม:** *ใช่* (การตั้งค่านี้ไม่จำเป็นต้องระบุ แต่ขอแนะนำให้ใช้ประสิทธิภาพสูงสุด)</span><span class="sxs-lookup"><span data-stu-id="756cb-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="756cb-558">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="756cb-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="756cb-559">ไม่จำเป็นต้องระบุ: ถ้าคุณกำลังตั้งค่าการออกแบบป้ายชื่อเฉพาะลูกค้า คุณต้องสร้างการสอบถามเพื่อค้นหาบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="756cb-560">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="756cb-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="756cb-561">จากนั้น ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-562">**ตาราง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="756cb-563">**ตารางสืบทอด:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="756cb-564">**ฟิลด์:** *หมายเลขบัญชี*</span><span class="sxs-lookup"><span data-stu-id="756cb-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="756cb-565">**เงื่อนไข:** ให้ป้อนหมายเลขบัญชีลูกค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="756cb-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="756cb-566">เมื่อคุณดำเนินการเสร็จสิ้น ให้เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="756cb-567">ในบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไขการสอบถาม** เพื่อเปิดกล่องโต้ตอบตัวแก้ไขการสอบถามสำหรับเท็มเพลตป้ายชื่อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="756cb-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="756cb-568">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **การเรียงลำดับ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-569">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-570">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-571">**ฟิลด์:** *รหัสรายการของโหลดอ้างอิง (รหัสเรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="756cb-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="756cb-572">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="756cb-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="756cb-573">เพิ่มแถวที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-574">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-575">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-576">**ฟิลด์:** *รหัสการจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="756cb-577">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="756cb-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="756cb-578">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="756cb-579">กล่องข้อความจะพร้อมท์ให้คุณยืนยันการดำเนินการรีเซ็ตการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="756cb-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="756cb-580">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="756cb-581">ในบานหน้าต่างการดำเนินการ ให้เลือก **กลุ่มเท็มเพลตป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="756cb-582">ในกล่องโต้ตอบ **กลุ่มเท็มเพลตของป้ายชื่อเวฟ** สำหรับแถวที่มีการตั้งค่าฟิลด์ **ชื่อฟิลด์การอ้างอิง** เป็น *รหัสการจัดส่ง* ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID* , set the following values:</span></span>

    - <span data-ttu-id="756cb-583">**พิมพ์ป้ายชื่อการแบ่ง:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="756cb-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="756cb-584">**รหัสโครงร่างป้ายชื่อ:** เลือกป้ายชื่อการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="756cb-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="756cb-585">(ตัวอย่างเช่น เลือกโครงร่างป้ายชื่อ *การแบ่ง* ที่คุณสร้างไว้ก่อนหน้านี้ในสถานการณ์นี้)</span><span class="sxs-lookup"><span data-stu-id="756cb-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="756cb-586">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์สำหรับป้ายชื่อการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="756cb-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="756cb-587">(โดยทั่วไป สำหรับวัตถุประสงค์ของการแยกม้วนป้ายชื่อ คุณควรเลือกเครื่องพิมพ์เดียวกันกับที่เลือกบน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="756cb-588">อย่างไรก็ตาม สถานการณ์อื่นๆ อาจเป็นไปได้)</span><span class="sxs-lookup"><span data-stu-id="756cb-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="756cb-589">สำหรับแถวที่ฟิลด์ **ชื่อฟิลด์การอ้างอิง** ถูกตั้งค่าเป็น *รหัสรายการโหลดอ้างอิง* ให้เลือกกล่องกาเครื่องหมาย **รหัสการสร้างป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="756cb-589">For the row where the **Reference field name** field is set to *Reference load line id* , select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="756cb-590">การตั้งค่านี้จะสร้างลำดับป้ายชื่อหนึ่งลำดับ ("กล่อง 1 จาก X") สำหรับแต่ละรายการโหลดทั่วทั้งเวฟ โดยไม่คำนึงถึงการตั้งค่าการจัดกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="756cb-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="756cb-591">คุณสามารถพิมพ์ลำดับป้ายชื่อนี้บนโครงร่างป้ายชื่อได้</span><span class="sxs-lookup"><span data-stu-id="756cb-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="756cb-592">นอกจากนี้ ป้ายชื่อสำหรับการจัดส่งที่แตกต่างกันจะถูกแยกด้วยป้ายชื่อการแบ่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="756cb-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="756cb-593">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **กลุ่มเท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="756cb-594">สร้างเท็มเพลตของป้ายชื่อที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="756cb-595">**ชื่อเท็มเพลตของป้ายชื่อ:** *ป้ายชื่อแท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="756cb-596">**คำอธิบาย:** *ป้ายชื่อแท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="756cb-597">**รหัสขั้นตอนของเวฟ:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="756cb-598">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="756cb-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="756cb-599">บน FastTab **ทั่วไป** ในฟิลด์ **ชนิดป้ายชื่อเวฟ** เลือกค่า เช่น *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="756cb-600">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-601">**รหัสโครงร่างป้ายชื่อ:** *แท่นวางสินค้า*</span><span class="sxs-lookup"><span data-stu-id="756cb-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="756cb-602">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์ ZPL ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="756cb-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="756cb-603">**รันการสอบถาม:** *ใช่* (การตั้งค่านี้ไม่จำเป็นต้องระบุ แต่ขอแนะนำให้ใช้ประสิทธิภาพสูงสุด)</span><span class="sxs-lookup"><span data-stu-id="756cb-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="756cb-604">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="756cb-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="756cb-605">ไม่จำเป็นต้องระบุ: ถ้าคุณกำลังตั้งค่าการออกแบบป้ายชื่อเฉพาะลูกค้า คุณต้องสร้างการสอบถามเพื่อค้นหาบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="756cb-606">บน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ** เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="756cb-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="756cb-607">จากนั้น ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-608">**ตาราง:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="756cb-609">**ตารางสืบทอด:** *การจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="756cb-610">**ฟิลด์:** *หมายเลขบัญชี*</span><span class="sxs-lookup"><span data-stu-id="756cb-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="756cb-611">**เงื่อนไข:** ให้ป้อนหมายเลขบัญชีลูกค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="756cb-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="756cb-612">เมื่อคุณดำเนินการเสร็จสิ้น ให้เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="756cb-613">ในบานหน้าต่างการดำเนินการ ให้เลือก **แก้ไขการสอบถาม** เพื่อเปิดกล่องโต้ตอบตัวแก้ไขการสอบถามสำหรับเท็มเพลตป้ายชื่อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="756cb-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="756cb-614">ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **การเรียงลำดับ** เพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-615">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-616">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-617">**ฟิลด์:** *รหัสรายการของโหลดอ้างอิง (รหัสเรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="756cb-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="756cb-618">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="756cb-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="756cb-619">เพิ่มแถวที่สองที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="756cb-620">**ตาราง:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-621">**ตารางสืบทอด:** *รายการงาน*</span><span class="sxs-lookup"><span data-stu-id="756cb-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="756cb-622">**ฟิลด์:** *รหัสการจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="756cb-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="756cb-623">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="756cb-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="756cb-624">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="756cb-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="756cb-625">กล่องข้อความจะพร้อมท์ให้คุณยืนยันการดำเนินการรีเซ็ตการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="756cb-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="756cb-626">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="756cb-627">ในบานหน้าต่างการดำเนินการ ให้เลือก **กลุ่มเท็มเพลตป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="756cb-628">ในกล่องโต้ตอบ **กลุ่มเท็มเพลตของป้ายชื่อเวฟ** สำหรับแถวที่มีการตั้งค่าฟิลด์ **ชื่อฟิลด์การอ้างอิง** เป็น *รหัสการจัดส่ง* ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID* , set the following values:</span></span>

    - <span data-ttu-id="756cb-629">**พิมพ์ป้ายชื่อการแบ่ง:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="756cb-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="756cb-630">**รหัสโครงร่างป้ายชื่อ:** เลือกป้ายชื่อการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="756cb-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="756cb-631">(ตัวอย่างเช่น เลือกโครงร่างป้ายชื่อ *การแบ่ง* ที่คุณสร้างไว้ก่อนหน้านี้ในสถานการณ์นี้)</span><span class="sxs-lookup"><span data-stu-id="756cb-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="756cb-632">**ชื่อเครื่องพิมพ์:** เลือกเครื่องพิมพ์สำหรับป้ายชื่อการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="756cb-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="756cb-633">(โดยทั่วไป สำหรับวัตถุประสงค์ของการแยกม้วนป้ายชื่อ คุณควรเลือกเครื่องพิมพ์เดียวกันกับที่เลือกบน FastTab **รายละเอียดเท็มเพลตของป้ายชื่อเวฟ**</span><span class="sxs-lookup"><span data-stu-id="756cb-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="756cb-634">อย่างไรก็ตาม สถานการณ์อื่นๆ อาจเป็นไปได้)</span><span class="sxs-lookup"><span data-stu-id="756cb-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="756cb-635">สำหรับแถวที่ฟิลด์ **ชื่อฟิลด์การอ้างอิง** ถูกตั้งค่าเป็น *รหัสรายการโหลดอ้างอิง* ให้เลือกกล่องกาเครื่องหมาย **รหัสการสร้างป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="756cb-635">For the row where the **Reference field name** field is set to *Reference load line id* , select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="756cb-636">การตั้งค่านี้จะสร้างลำดับป้ายชื่อหนึ่งลำดับ ("กล่อง 1 จาก X") สำหรับแต่ละรายการโหลดทั่วทั้งเวฟ โดยไม่คำนึงถึงการตั้งค่าการจัดกลุ่มงาน</span><span class="sxs-lookup"><span data-stu-id="756cb-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="756cb-637">คุณสามารถพิมพ์ลำดับป้ายชื่อนี้บนโครงร่างป้ายชื่อได้</span><span class="sxs-lookup"><span data-stu-id="756cb-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="756cb-638">นอกจากนี้ ป้ายชื่อสำหรับการจัดส่งที่แตกต่างกันจะถูกแยกด้วยป้ายชื่อการแบ่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="756cb-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="756cb-639">ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="756cb-639">Configure number sequence extensions</span></span>

<span data-ttu-id="756cb-640">ส่วนขยายของลำดับหมายเลขจะควบคุมการปฏิบัติตาม GS1 ของลำดับหมายเลขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="756cb-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="756cb-641">ไม่จำเป็นต้องระบุการตั้งค่าคอนฟิกนี้สำหรับสถานการณ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="756cb-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="756cb-642">สำหรับข้อมูลเพิ่มเติมและคำแนะนำในการตั้งค่าคอนฟิก ให้ดู [ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข](../warehousing/configure-number-sequence-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="756cb-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="756cb-643">สร้างใบสั่งขายและนำใบสั่งขายออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="756cb-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="756cb-644">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="756cb-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="756cb-645">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="756cb-646">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="756cb-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="756cb-647">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="756cb-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="756cb-648">เพิ่มรายการใบสั่งขายสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="756cb-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="756cb-649">รายการใบสั่งขายที่ 1:</span><span class="sxs-lookup"><span data-stu-id="756cb-649">Sales order line 1:</span></span>

        - <span data-ttu-id="756cb-650">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="756cb-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="756cb-651">**ปริมาณ:** *9024*</span><span class="sxs-lookup"><span data-stu-id="756cb-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="756cb-652">**หน่วย:** *ชิ้น* (9024 ชิ้น = 376 กล่อง = 47 แท่นวางสินค้า)</span><span class="sxs-lookup"><span data-stu-id="756cb-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="756cb-653">รายการใบสั่งขายที่ 2:</span><span class="sxs-lookup"><span data-stu-id="756cb-653">Sales order line 2:</span></span>

        - <span data-ttu-id="756cb-654">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="756cb-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="756cb-655">**ปริมาณ:** *9016*</span><span class="sxs-lookup"><span data-stu-id="756cb-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="756cb-656">**หน่วย:** *ชิ้น* (9016 ชิ้น = 322 กล่อง = 46 แท่นวางสินค้า)</span><span class="sxs-lookup"><span data-stu-id="756cb-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="756cb-657">สินค้าและปริมาณที่ให้ไว้ที่นี่คือตัวอย่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="756cb-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="756cb-658">พวกเขาต้องใช้กลุ่มลำดับหน่วยที่คุณได้กำหนดไว้ก่อนหน้านี้ การแปลงหน่วยที่เหมาะสมจาก *ชิ้น* เป็น *กล่อง* เป็น *แท่นวางสินค้า* ต้องถูกกำหนด และต้องมีสินค้าคงคลังในคลังสินค้า *62*</span><span class="sxs-lookup"><span data-stu-id="756cb-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="756cb-659">สำหรับข้อมูลเพิ่มเติม ให้ดู [นโยบายหน่วยวัดและการเก็บสต็อก](unit-measure-stocking-policies.md)</span><span class="sxs-lookup"><span data-stu-id="756cb-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="756cb-660">เลือกรายการในใบสั่งขายที่ 1</span><span class="sxs-lookup"><span data-stu-id="756cb-660">Select sales order line 1.</span></span> <span data-ttu-id="756cb-661">จากนั้น ในส่วน **รายการใบสั่งขาย** บนเมนู **สินค้าคงคลัง** เลือก **การจอง**</span><span class="sxs-lookup"><span data-stu-id="756cb-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="756cb-662">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** และจากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="756cb-662">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="756cb-663">ทำซ้ำขั้นตอนที่ 4 และ 5 สำหรับรายการใบสั่งขายที่ 2</span><span class="sxs-lookup"><span data-stu-id="756cb-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="756cb-664">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="756cb-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="756cb-665">เหตุการณ์ต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="756cb-665">The following events occur:</span></span> 

    - <span data-ttu-id="756cb-666">ระบบจะประมวลผลการจัดส่งที่สร้างขึ้นโดยใช้เท็มเพลตที่มีขั้นตอนการพิมพ์ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="756cb-667">โครงร่างป้ายชื่อจะถูกใช้เพื่อกำหนดรูปแบบของป้ายชื่อ และผลลัพธ์จะเป็นป้ายชื่อที่พิมพ์บนเครื่องพิมพ์ที่เลือกในเท็มเพลตของป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="756cb-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="756cb-668">มีการสร้างและพิมพ์ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="756cb-669">จำนวนของป้ายชื่อจะเท่ากับจำนวนของกล่อง (ในตัวอย่างนี้ ป้ายชื่อกล่อง 376 ป้ายสำหรับรายการที่ 1 ป้ายชื่อกล่อง 322 ป้ายสำหรับรายการที่่ 2 ป้ายชื่อแท่นวางสินค้า 47 ป้ายสำหรับรายการที่ 1 ป้ายชื่อแท่นวางสินค้า 47 ป้ายสำหรับรายการที่ 2 และป้ายชื่อการแบ่งสองป้ายที่มีรหัสการจัดส่ง)</span><span class="sxs-lookup"><span data-stu-id="756cb-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="756cb-670">รหัสใบตราส่งใหม่จะถูกสร้างขึ้นสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="756cb-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="756cb-671">ถ้าคุณได้ตั้งค่าคอนฟิกส่วนขยายของลำดับหมายเลข รหัสป้ายชื่อเวฟจะเป็นไปตามรูปแบบหมายเลข **SSCC-18**</span><span class="sxs-lookup"><span data-stu-id="756cb-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="756cb-672">คุณสามารถดูและพิมพ์ป้ายชื่อเวฟอีกครั้งจากหน้าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="756cb-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="756cb-673">การจัดส่งทั้งหมด \> รายละเอียดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="756cb-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="756cb-674">โหลดทั้งหมด \> รายละเอียดโหลด</span><span class="sxs-lookup"><span data-stu-id="756cb-674">All loads \> Load details</span></span>
- <span data-ttu-id="756cb-675">เวฟทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="756cb-675">All waves</span></span>
- <span data-ttu-id="756cb-676">ป้ายชื่อเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-676">Wave labels</span></span>
- <span data-ttu-id="756cb-677">ประวัติป้ายชื่อของเวฟ</span><span class="sxs-lookup"><span data-stu-id="756cb-677">Wave label history</span></span>

<span data-ttu-id="756cb-678">สำหรับหน้าเหล่านี้ส่วนใหญ่ คุณสามารถค้นหาฟังก์ชันที่เกี่ยวข้องโดยการเลือก **ป้ายชื่อเวฟ** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** บนแท็บ **การจัดส่ง** ของบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="756cb-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
