---
title: ข้อความตัวประมวลผลข้อความ
description: หัวข้อนี้มีข้อมูลเกี่ยวกับคุณลักษณะข้อความตัวประมวลผลข้อความของปริมาณงานของ scale unit
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 86f15831f11dc9fdcada9639858fd3b18cdc7503
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271112"
---
# <a name="message-processor-messages"></a><span data-ttu-id="b99aa-103">ข้อความตัวประมวลผลข้อความ</span><span class="sxs-lookup"><span data-stu-id="b99aa-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b99aa-104">จะมีการใช้ข้อความตัวประมวลผลข้อความ เมื่อรัน scale unit ของระบบคลาวด์และ edge สำหรับ [ปริมาณงานการผลิต](cloud-edge-workload-manufacturing.md) และ [ปริมาณงานการจัดการคลังสินค้า](cloud-edge-workload-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="b99aa-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="b99aa-105">มีการแลกเปลี่ยนข้อมูลจํานวนมากระหว่างสภาพแวดล้อมการปรับใช้ฮับและ scale unit เพื่อให้มีการซิงค์กันเสมอ แต่การแลกเปลี่ยนข้อมูลเหล่านี้เพียงสองสามรายการจะได้รับการประมวลผลโดย *ตัวประมวลผลข้อความ*</span><span class="sxs-lookup"><span data-stu-id="b99aa-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="b99aa-106">คุณสามารถดูข้อความที่ประมวลผลโดยตัวประมวลผลข้อความได้โดยไปที่ **การจัดการระบบ > ตัวประมวลผลข้อความ > ข้อความตัวประมวลผลข้อความ**</span><span class="sxs-lookup"><span data-stu-id="b99aa-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="b99aa-107">คอลัมน์และตัวกรองกริดข้อความ</span><span class="sxs-lookup"><span data-stu-id="b99aa-107">Message grid columns and filters</span></span>

<span data-ttu-id="b99aa-108">คุณสามารถใช้ฟิลด์ที่ด้านบนของหน้า **ข้อความตัวประมวลผลข้อความ** เพื่อช่วยค้นหาข้อความเฉพาะใดๆ ที่คุณกำลังค้นหา</span><span class="sxs-lookup"><span data-stu-id="b99aa-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="b99aa-109">ตัวกรองข้อมูลส่วนใหญ่เหล่านี้ตรงกับหัวข้อคอลัมน์ในกริดข้อความ</span><span class="sxs-lookup"><span data-stu-id="b99aa-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="b99aa-110">ตัวกรองข้อมูลและหัวข้อคอลัมน์ต่อไปนี้พร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="b99aa-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="b99aa-111">**ชนิดข้อความ** – ระบุชนิดของข้อความ</span><span class="sxs-lookup"><span data-stu-id="b99aa-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="b99aa-112">**คิวข้อความ** – ระบุชื่อของคิวที่จะประมวลผลข้อความ</span><span class="sxs-lookup"><span data-stu-id="b99aa-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="b99aa-113">มีการระบุคิวต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b99aa-113">The following queues are provided:</span></span>
  - <span data-ttu-id="b99aa-114">*สเกลยูนิตกับฮับ*</span><span class="sxs-lookup"><span data-stu-id="b99aa-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="b99aa-115">*ฮับไปยัง Scale Unit ที่มีการดำเนินการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="b99aa-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="b99aa-116">*ฮับไปยัง Scale Unit การดำเนินการผลิต*</span><span class="sxs-lookup"><span data-stu-id="b99aa-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="b99aa-117">**สถานะข้อความ** – ระบุสถานะของข้อความ</span><span class="sxs-lookup"><span data-stu-id="b99aa-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="b99aa-118">มีสถานะต่อไปนี้อยู่:</span><span class="sxs-lookup"><span data-stu-id="b99aa-118">The following states exists:</span></span>
  - <span data-ttu-id="b99aa-119">*จัดคิวแล้ว* – ข้อความพร้อมแล้วที่จะถูกประมวลผลโดยตัวประมวลผลข้อความ</span><span class="sxs-lookup"><span data-stu-id="b99aa-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="b99aa-120">*ประมวลผลแล้ว* – ข้อความถูกประมวลผลเสร็จเรียบร้อยแล้วโดยตัวประมวลผลข้อความ</span><span class="sxs-lookup"><span data-stu-id="b99aa-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="b99aa-121">*ยกเลิกแล้ว* – มีการประมวลผลข้อความแล้ว แต่การประมวลผลล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="b99aa-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="b99aa-122">**เนื้อหาข้อความ** – ตัวกรองนี้ทำการค้นหาข้อความแบบเต็มของเนื้อหาข้อความ</span><span class="sxs-lookup"><span data-stu-id="b99aa-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="b99aa-123">(เนื้อหาข้อความไม่ถูกแสดงในกริด) ตัวกรองจะถือว่าสัญลักษณ์พิเศษส่วนใหญ่ (เช่น "-") เป็นช่องว่าง และถือว่าอักขระพื้นที่ทั้งหมดเป็นตัวปฏิบัติการ OR แบบบูลีน</span><span class="sxs-lookup"><span data-stu-id="b99aa-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="b99aa-124">T=ตัวอย่างเช่น นี่หมายความว่า ถ้าคุณค้นหาค่า `journalid` เฉพาะที่เท่ากับ "USMF-123456" ระบบจะค้นหาข้อความทั้งหมดที่มี "USMF" หรือ "123456" ซึ่งมีแนวโน้มที่จะเป็นรายการยาว</span><span class="sxs-lookup"><span data-stu-id="b99aa-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="b99aa-125">ดังนั้น ควรป้อนเพียง "123456" อย่างเดียว เนื่องจากจะส่งคืนผลลัพธ์ที่เฉพาะเจาะจงมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="b99aa-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="b99aa-126">ชนิดข้อความตัวอย่าง: ร้องขอการอัพเดตทางการเงินของการปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b99aa-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="b99aa-127">ตัวอย่างเช่น **ชนิดข้อความ** *ร้องขอการอัพเดตทางการเงินของการปรับปรุงสินค้าคงคลัง* ถูกใช้ในการสร้างและลงรายการบัญชีสมุดรายวันการตรวจนับบนฮับ เมื่อผู้ปฏิบัติงานใช้แอปคลังสินค้าเพื่อ [ลงทะเบียนการปรับปรุงสินค้าคงคลัง](cloud-edge-warehouse-inventory-adjustment.md) บนปริมาณงานการจัดการคลังสินค้าของ scale unit</span><span class="sxs-lookup"><span data-stu-id="b99aa-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="b99aa-128">เนื่องจากกระบวนการเฉพาะนี้มาจาก scale unit ฟิลด์ **คิวข้อความ** จะแสดงค่า *Scale unit ไปยังฮับ*</span><span class="sxs-lookup"><span data-stu-id="b99aa-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="b99aa-129">สำหรับชนิดข้อความนี้ ปริมาณงาน scale unit จะบันทึกข้อความเป็นส่วนหนึ่งของการดําเนินงานปรับปรุงสินค้าคงคลังของแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="b99aa-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="b99aa-130">จากนั้น ข้อมูลข้อความจะถูกโอนย้ายไปยังฮับเป็นส่วนหนึ่งของกระบวนการเดียวกันที่ใช้กับ [สถาปัตยกรรมของ Commerce Data Exchange](../../commerce/commerce-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="b99aa-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="b99aa-131">จะมีการอัพเดตข้อความเพื่อแสดง **สถานะข้อความ** เป็น *จัดคิวแล้ว*</span><span class="sxs-lookup"><span data-stu-id="b99aa-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="b99aa-132">จากนั้น ตัวประมวลผลข้อความจะพยายามประมวลผลข้อความและอัพเดต **สถานะข้อความ** เป็น *ประมวลผลแล้ว* เมื่อสำเร็จ หรือ *ยกเลิกแล้ว* เมื่อล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="b99aa-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="b99aa-133">ดูล็อกข้อความ เนื้อหาข้อความ และรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="b99aa-133">View the message log, message content, and details</span></span>

<span data-ttu-id="b99aa-134">คุณสามารถค้นหารายละเอียดเกี่ยวกับข้อความได้โดยเลือกข้อความนั้นในกริด แล้วจากนั้น เปิดแท็บ **ล็อก** หรือ **เนื้อหาข้อความ** ภายใต้กริดข้อความ โดยที่เหตุการณ์การประมวลผลแต่ละเหตุการณ์จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="b99aa-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="b99aa-135">**เนื้อหาของข้อความ** จะขึ้นอยู่กับ **ชนิดของข้อความ** และดังนั้นจึงมีความยาวข้อความที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b99aa-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="b99aa-136">ข้อความเนื้อหาของข้อความทั่วไปจะขึ้นต้นด้วย **{** และลงท้ายด้วย **}** และในระหว่างนั้น มีชื่อฟิลด์ เช่น `journalId` ซึ่งตามด้วย **:** และค่า เช่น *USMF-123456*</span><span class="sxs-lookup"><span data-stu-id="b99aa-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="b99aa-137">แถบเครื่องมือบนแท็บ **ล็อก** จะรวมปุ่มต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b99aa-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="b99aa-138">**ล็อก** – แสดงผลลัพธ์ของการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="b99aa-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="b99aa-139">ซึ่งมีประโยชน์โดยเฉพาะอย่างยิ่งในการเข้าใจเหตุผลสำหรับการประมวลผลความล้มเหลวสำหรับข้อความที่มี **ผลลัพธ์ของการประมวลผล** เป็น *ล้มเหลว*</span><span class="sxs-lookup"><span data-stu-id="b99aa-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="b99aa-140">**กลุ่มงาน** – การดําเนินการประมวลผลข้อความหลายรายการสามารถรันเป็นส่วนหนึ่งของกระบวนการชุดงานเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="b99aa-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="b99aa-141">เลือกปุ่มนี้เพื่อดูข้อมูลโดยละเอียดนี้</span><span class="sxs-lookup"><span data-stu-id="b99aa-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="b99aa-142">ตัวอย่างเช่น คุณสามารถดูว่ามีการอ้างอิงที่ต้องการให้ระบบประมวลผลข้อความบางข้อความในลำดับเฉพาะหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b99aa-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="b99aa-143">งานของชุดงานตัวประมวลผลข้อความ</span><span class="sxs-lookup"><span data-stu-id="b99aa-143">Message processor batch job</span></span>

<span data-ttu-id="b99aa-144">เมื่อรันการปรับใช้ระบบคลาวด์และ edge ชุดงาน *ตัวประมวลผลข้อความ* จะได้รับการเริ่มต้นโดยอัตโนมัติ เมื่อมีการสร้างข้อความใหม่เพื่อการประมวลผล ดังนั้นคุณจึงไม่ควรจะต้องจัดกำหนดการงานนี้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b99aa-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="b99aa-145">ถ้าจําเป็น คุณสามารถเข้าถึงชุดงานได้โดยไปที่ **การจัดการระบบ > ตัวประมวลผลข้อความ > ตัวประมวลผลข้อความ**</span><span class="sxs-lookup"><span data-stu-id="b99aa-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="b99aa-146">ประมวลผลหรือยกเลิกข้อความด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b99aa-146">Manually process or cancel a message</span></span>

<span data-ttu-id="b99aa-147">ถ้าจําเป็น คุณสามารถประมวลผลหรือยกเลิกข้อความด้วยตนเองได้ตามสถานะปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b99aa-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="b99aa-148">เมื่อต้องการทำเช่นนั้น ให้เลือกข้อความในกริด แล้วจากนั้น เลือก **กระบวนการ** หรือ **ยกเลิก** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b99aa-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="b99aa-149">ตั้งค่าเหตุการณ์ทางธุรกิจเพื่อจัดส่งข้อความแจ้งเตือนสำหรับผลลัพธ์ของการประมวลผลที่ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="b99aa-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="b99aa-150">นอกจากการกรองค่า **สถานะข้อความ** *ยกเลิกแล้ว* เพื่อสอบถามข้อความที่ล้มเหลว คุณสามารถตั้งค่า [เหตุการณ์ทางธุรกิจ](../../fin-ops-core/dev-itpro/business-events/home-page.md) บนฮับ เพื่อแจ้งเตือนคุณเรื่องผลลัพธ์ของการประมวลผลที่ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="b99aa-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="b99aa-151">เมื่อต้องการทำเช่นนั้น ให้เรียกใช้เหตุการณ์ทางธุรกิจที่ชื่อ *ข้อความของตัวประมวลผลข้อความที่ประมวลผล*  บนหน้า **แค็ตตาล็อกเหตุการณ์ทางธุรกิจ** (**การจัดการระบบ > การตั้งค่า > เหตุการณ์ทางธุรกิจ > แค็ตตาล็อกเหตุการณ์ทางธุรกิจ**)</span><span class="sxs-lookup"><span data-stu-id="b99aa-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="b99aa-152">เนื่องจากเป็นส่วนหนึ่งของกระบวนการเรียกใช้ คุณจะได้รับการแนะนำให้ระบุว่าเหตุการณ์นี้เฉพาะเจาะจงสำหรับนิติบุคคลหนึ่งรายหรือนิติบุคคลทั้งหมด และระบุ **ชื่อปลายทาง** ซึ่งต้องถูกกําหนดไว้ก่อน</span><span class="sxs-lookup"><span data-stu-id="b99aa-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="b99aa-153">หาก **เมื่อเหตุการณ์ทางธุรกิจเกิดขึ้น** ถูกตั้งค่าเป็น *Microsoft Power Automate* (ตัวอย่างเช่น แทนที่จะเป็น *HTTPS*) **ชื่อปลายทาง** จะถูกสร้างขึ้นโดยอัตโนมัติใน Supply Chain Management ตามการตั้งค่า *Microsoft Power Automate*</span><span class="sxs-lookup"><span data-stu-id="b99aa-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="b99aa-154">ตัวอย่าง Microsoft Power Automate</span><span class="sxs-lookup"><span data-stu-id="b99aa-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="b99aa-155">ในตัวอย่างนี้ ใช้ **เมื่อเกิดเหตุการณ์ทางธุรกิจเกิดขึ้น** กับ *Microsoft Power Automate* ส่งอีเมลที่มีข้อความ InfoLog และไฮเปอร์ลิงค์ เพื่อเปิดหน้า **ข้อความตัวประมวลผลข้อความ** สำหรับข้อความที่ล้มเหลวเฉพาะในการปรับใช้ฮับ</span><span class="sxs-lookup"><span data-stu-id="b99aa-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="b99aa-156">หากจำเป็น คุณสามารถเพิ่มตรรกะพิเศษเพื่อส่งการแจ้งเตือนพร้อมกันโดยใช้ช่องทางต่างๆ และควบคุมผู้รับตามข้อมูลเหตุการณ์ได้</span><span class="sxs-lookup"><span data-stu-id="b99aa-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="b99aa-157">ใน [Power Automate](https://preview.flow.microsoft.com) ให้สร้างโฟลว์ระบบคลาวด์แบบอัตโนมัติใหม่เพื่อทริกเกอร์โฟลว์ **เมื่อเหตุการณ์ทางธุรกิจเกิดขึ้น - Fin & Ops App (Dynamics 365)** ตามด้วย **แยกวิเคราะห์ JSON** และ **ส่งอีเมล** ดังที่แสดงในภาพอธิบายต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b99aa-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate โฟลว์ระบบคลาวด์แบบอัตโนมัติ":::

1. <span data-ttu-id="b99aa-159">ในขั้นตอน **เมื่อเหตุการณ์ทางธุรกิจเกิดขึ้น** คุณสามารถค้นหาหรือป้อน **อินสแตนซ์** ของฮับที่ตามด้วย **ประเภท** แล้วจากนั้น **เหตุการณ์ทางธุรกิจ** *ประมวลผลข้อความตัวประมวลผลข้อความแล้ว* ตามที่แสดงไว้ในภาพอธิบายต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b99aa-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate ขั้นตอนเมื่อเหตุการณ์ทางธุรกิจเกิดขึ้น":::

1. <span data-ttu-id="b99aa-161">สำหรับขั้นตอน **แยกวิเคราะห์ JSON** ป้อน **เค้าร่าง** ที่กำหนดฟิลด์แบบขยาย</span><span class="sxs-lookup"><span data-stu-id="b99aa-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="b99aa-162">คุณสามารถใช้ตัวเลือก *ดาวน์โหลดเค้าร่าง* ในหน้า **แค็ตตาล็อกเหตุการณ์ทางธุรกิจ** ใน Supply Chain Management หรือเริ่มต้นโดยการวางในข้อความเค้าร่างตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b99aa-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="b99aa-163">ข้อความตัวอย่างนี้จะให้ไว้หลังจากภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b99aa-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate ขั้นตอนแยกวิเคราะห์ JSON":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="b99aa-165">ในขั้นตอน **ส่งอีเมล** คุณสามารถเลือกฟิลด์แต่ละฟิลด์ หรือเริ่มต้นโดยการวางตัวอย่างเนื้อหาอีเมลลงในฟิลด์ **เนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="b99aa-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="b99aa-166">ตัวอย่างนี้จะให้ไว้หลังจากภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b99aa-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate ขั้นตอนส่งอีเมล":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="b99aa-168">เมื่อคุณบันทึกเหตุการณ์ทางธุรกิจ เหตุการณ์ทางธุรกิจนั้นจะถูกเรียกใช้งานโดยอัตโนมัติและพร้อมใช้งานโดยเป็นส่วนหนึ่งของ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b99aa-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
