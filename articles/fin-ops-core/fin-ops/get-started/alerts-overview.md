---
title: ภาพรวมของการแจ้งเตือน
description: หัวข้อนี้ให้ข้อมูลทั่วไปเกี่ยวกับการแจ้งเตือน คุณสามารถใช้การแจ้งเตือนเพื่อรับข่าวสารเกี่ยวกับเหตุการณ์ที่คุณต้องการติดตามในระหว่างวันทำงาน
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 755181e956a3d93d87e9e5d57622283ff7bf4944
ms.sourcegitcommit: f62c2151be477acfaeace73878471abb9b1b832d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/17/2020
ms.locfileid: "3602540"
---
# <a name="alerts-overview"></a><span data-ttu-id="edb21-104">ภาพรวมการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="edb21-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="edb21-105">เกี่ยวกับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="edb21-105">About alerts</span></span>
<span data-ttu-id="edb21-106">การแจ้งเตือนจากระบบการแจ้งเตือนสำหรับเหตุการณ์ในระบบ</span><span class="sxs-lookup"><span data-stu-id="edb21-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="edb21-107">คุณสามารถใช้การแจ้งเตือนเพื่อรับข่าวสารเกี่ยวกับเหตุการณ์ที่คุณต้องการติดตามในระหว่างวันทำงาน</span><span class="sxs-lookup"><span data-stu-id="edb21-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="edb21-108">คุณสามารถสร้างชุดกฎของตนเองได้อย่างง่ายดาย เพื่อให้ได้รับการแจ้งเตือนเกี่ยวกับการจัดส่งที่เกินกำหนด ใบสั่งที่ถูกลบ ราคาที่เปลี่ยนแปลง หรือเหตุการณ์อื่นๆ ที่คุณจำเป็นต้องตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="edb21-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="edb21-109">ในการวางแผนทรัพยากรองค์กร (ERP) มีสถานการณ์ทั่วไปมากมายที่สามารถใช้ลักษณะการทำงานการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="edb21-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="edb21-110">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="edb21-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="edb21-111">สถานการณ์จำลองที่ 1: สร้างกฎการแจ้งเตือนสำหรับใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="edb21-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="edb21-112">เปิดหน้า **ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="edb21-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="edb21-113">บนบานหน้าต่างการดำเนินการ บนแท็บ **ตัวเลือก** ในกลุ่ม **แบ่งปัน** เลือก **สร้างการแจ้งเตือนที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="edb21-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="edb21-114">ในกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** บน FastTab **แจ้งเตือนฉันเมื่อ** ในฟิลด์ **เหตุการณ์** เลือก **เรกคอร์ดได้ถูกสร้างแล้ว**</span><span class="sxs-lookup"><span data-stu-id="edb21-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="edb21-115">สถานการณ์จำลองที่ 2: สร้างกฎการแจ้งเตือนสำหรับการเลื่อนวันจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="edb21-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="edb21-116">เปิดหน้า **ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="edb21-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="edb21-117">เลือกรหัสใบสั่งซื้อเพื่อเข้าถึงรายละเอียดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="edb21-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="edb21-118">ขยาย FastTab **ส่วนหัวของใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="edb21-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="edb21-119">บนบานหน้าต่างการดำเนินการ บนแท็บ **ตัวเลือก** ในกลุ่ม **แบ่งปัน** เลือก **สร้างการแจ้งเตือนที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="edb21-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="edb21-120">ในกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** บน FastTab **แจ้งเตือนฉันเมื่อ** ในฟิลด์ **ฟิลด์** เลือก **วันที่จัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="edb21-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="edb21-121">ในฟิลด์ **เหตุการณ์** เลือก **ได้ถูกเลื่อนออกไป**</span><span class="sxs-lookup"><span data-stu-id="edb21-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="edb21-122">หลังจากที่คุณปิดกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** กฎของคุณจะปรากฏขึ้นบนหน้า **จัดการกฎการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="edb21-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="edb21-123">คุณสามารถใช้หน้า **จัดการกฎการแจ้งเตือน** เพื่ออัพเดตกฎการแจ้งเตือนที่มีอยู่ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="edb21-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="edb21-124">ตัวอย่างเช่น คุณสามารถปรับเปลี่ยนทริกเกอร์เหตุการณ์ อัพเดตการแจ้งเตือนเหตุการณ์ และอัพเดตวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="edb21-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="edb21-125">เพื่อเปิดหน้า **จัดการกฎการแจ้งเตือน** ใช้ปุ่ม **แจ้งเตือนฉัน** บนแท็บ **ตัวเลือก** ของบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="edb21-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="edb21-126">จะเกิดอะไรขึ้นเมื่อกฎการแจ้งเตือนถูกสร้างขึ้น?</span><span class="sxs-lookup"><span data-stu-id="edb21-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="edb21-127">เมื่อคุณสร้างกฎการแจ้งเตือน คุณสามารถเชื่อมโยงเหตุการณ์ที่กำหนดไว้ล่วงหน้ากับฟิลด์เฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="edb21-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="edb21-128">ตัวอย่างเช่น วันที่ที่ระบุไว้ในฟิลด์มาถึง หรือเนื้อหาของฟิลด์เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="edb21-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="edb21-129">อีกทางหนึ่งคือ คุณสามารถเชื่อมโยงเหตุการณ์กับเรกคอร์ดในหน้าเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="edb21-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="edb21-130">ตัวอย่างเช่น มีการสร้างเรกคอร์ด หรือมีการลบเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="edb21-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="edb21-131">เมื่อเหตุการณ์ที่เลือกเกิดขึ้นสำหรับฟิลด์หรือสำหรับเรกคอร์ดในหน้า คุณจะได้รับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="edb21-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="edb21-132">ตัวอย่างเช่น คุณสร้างกฎซึ่งคุณเชื่อมโยงฟิลด์ **วันที่จัดส่ง** บนรายการใบสั่งซื้อที่ระบุด้วยเหตุการณ์ **ครบกำหนดเมื่อจำนวนเวลาที่ผ่านมาแล้วนี้**</span><span class="sxs-lookup"><span data-stu-id="edb21-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="edb21-133">คุณตั้งค่ากรอบเวลาเป็นห้าวัน</span><span class="sxs-lookup"><span data-stu-id="edb21-133">You set the time frame to five days.</span></span> <span data-ttu-id="edb21-134">ในกรณีนี้ ข้อความแจ้งเตือนถูกส่งห้าวัน หลังจากวันที่จัดส่งของรายการใบสั่งซื้อนั้น</span><span class="sxs-lookup"><span data-stu-id="edb21-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="edb21-135">นอกจากนี้ คุณสามารถกำหนดกฎการแจ้งเตือนได้โดยการตั้งค่าเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="edb21-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="edb21-136">ตัวอย่างเช่น คุณสามารถได้รับการแจ้งเตือนเกี่ยวกับใบสั่งซื้อใหม่ที่สร้างขึ้นสำหรับบัญชีผู้จัดจำหน่ายเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="edb21-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="edb21-137">การเตรียมการสำหรับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="edb21-137">Preparing for an alert</span></span>

<span data-ttu-id="edb21-138">ก่อนที่คุณจะตั้งค่ากฎการแจ้งเตือน ควรตัดสินใจว่าคุณต้องการรับข้อความแจ้งเตือนเมื่อใดหรือในสถานการณ์ใดบ้าง</span><span class="sxs-lookup"><span data-stu-id="edb21-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="edb21-139">เมื่อคุณทราบแล้วว่าเหตุการณ์ใดที่คุณต้องการได้รับการแจ้งเตือน ให้ค้นหาหน้าของข้อมูลที่ทำให้เกิดการปรากฎของเหตุการณ์นั้น</span><span class="sxs-lookup"><span data-stu-id="edb21-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="edb21-140">เหตุการณ์อาจเป็นวันที่ที่มาถึง หรือการเปลี่ยนแปลงบางอย่างที่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="edb21-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="edb21-141">ดังนั้น คุณต้องค้นหาหน้าที่ซึ่งมีการระบุวันที่ หรือที่ซึ่งฟิลด์ที่เปลี่ยนแปลงหรือเรกคอร์ดใหม่ที่ถูกสร้างขึ้น ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="edb21-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="edb21-142">หลังจากที่คุณมีข้อมูลดังกล่าวแล้ว คุณก็สามารถสร้างกฎการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="edb21-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="edb21-143">ส่วนประกอบของกฎการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="edb21-143">Components of an alert rule</span></span>

<span data-ttu-id="edb21-144">กฎการแจ้งเตือนมีส่วนประกอบห้าส่วน:</span><span class="sxs-lookup"><span data-stu-id="edb21-144">An alert rule has five components:</span></span>

- <span data-ttu-id="edb21-145">**เหตุการณ์** – เหตุการณ์ที่ทริกเกอร์กฎการแจ้งเตือนอาจเป็นวันที่ที่มาถึงหรือการเปลี่ยนแปลงเฉพาะที่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="edb21-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="edb21-146">คุณกำหนดเหตุการณ์บน FastTab **ส่งข้อความแจ้งเตือนอีเมลสำหรับการเปลี่ยนสถานะของงาน** ของกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="edb21-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="edb21-147">**เงื่อนไข** – บน FastTab **แจ้งเตือนฉันสำหรับ** ของกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** คุณสามารถเลือกขอบเขตของเงื่อนไข เพื่อควบคุม เมื่อคุณได้รับการแจ้งเตือนเกี่ยวกับเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="edb21-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="edb21-148">คุณสามารถใช้กฎกับเรกคอร์ดปัจจุบัน หรือเรกคอร์ดที่มองเห็นได้ทั้งหมดบนหน้า อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="edb21-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="edb21-149">ถ้ากฎจะใช้ระหว่างนิติบุคคล คุณสามารถตั้งค่าตัวเลือก **ทั่วทั้งองค์กร** เป็น **ใช่** ได้</span><span class="sxs-lookup"><span data-stu-id="edb21-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="edb21-150">**วันหมดอายุของกฎ** – บน FastTab **แจ้งเตือนฉันจนกว่า** ของกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** คุณสามารถระบุระยะเวลาที่ควรเปิดใช้งานกฎการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="edb21-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="edb21-151">**เนื้อหา** – บน FastTab **แจ้งเตือนฉันด้วย** ของกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** คุณสามารถระบุข้อความชื่อเรื่องและข้อความข่าวสารที่ข้อความแจ้งเตือนควรใช้</span><span class="sxs-lookup"><span data-stu-id="edb21-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="edb21-152">**ผู้ใช้** – บน FastTab **แจ้งเตือนผู้ที่** ของกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** คุณสามารถระบุผู้ใช้ที่ควรได้รับข้อความแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="edb21-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="edb21-153">โดยค่าเริ่มต้น มีการเลือกรหัสผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="edb21-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="edb21-154">ตัวเลือกนี้ถูกจำกัดแก่ผู้ดูแลระบบขององค์กร</span><span class="sxs-lookup"><span data-stu-id="edb21-154">This option is restricted to organization administrators.</span></span>

## <a name="videos"></a><span data-ttu-id="edb21-155">วิดีโอ</span><span class="sxs-lookup"><span data-stu-id="edb21-155">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="edb21-156">วิธีการใช้การแจ้งเตือนเพื่อตรวจสอบความถูกต้องของข้อมูลที่กรอง</span><span class="sxs-lookup"><span data-stu-id="edb21-156">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="edb21-157">[วิธีการใช้การแจ้งเตือนเพื่อตรวจสอบข้อมูลที่ถูกกรอง](https://youtu.be/ZYKMcv6kl9s) วิดีโอ (แสดงอยู่ด้านบน) จะรวมอยู่ใน [เพลย์ลิสต์ Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) มีให้รับชมบน YouTube</span><span class="sxs-lookup"><span data-stu-id="edb21-157">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="edb21-158">ตัวเลือกกฎการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="edb21-158">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

<span data-ttu-id="edb21-159">[ตัวเลือกกฎการแจ้งเตือน](https://youtu.be/cpzimwOjicM) วิดีโอ (แสดงอยู่ด้านบน) จะรวมอยู่ใน [เพลย์ลิสต์ Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) มีให้รับชมบน YouTube</span><span class="sxs-lookup"><span data-stu-id="edb21-159">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>


