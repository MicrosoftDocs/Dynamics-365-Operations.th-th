---
title: "การสร้างกฎการแจ้งเตือน"
description: "หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแจ้งเตือน และอธิบายวิธีการสร้างกฎการแจ้งเตือน เพื่อให้คุณได้รับแจ้งเกี่ยวกับเหตุการณ์ เช่น วันที่ที่มาถึง หรือการเปลี่ยนแปลงเฉพาะที่เกิดขึ้น"
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: cbf4917424e72a70a6d513b5daf45f6bf9cd57c7
ms.contentlocale: th-th
ms.lasthandoff: 12/18/2018

---

# <a name="create-alert-rules"></a><span data-ttu-id="c572d-103">การสร้างกฎการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c572d-103">Create alert rules</span></span>

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a><span data-ttu-id="c572d-104">การเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c572d-104">Getting started</span></span>

<span data-ttu-id="c572d-105">ก่อนที่คุณจะตั้งค่ากฎการแจ้งเตือน ควรตัดสินใจว่าคุณต้องการรับข้อความแจ้งเตือนเมื่อใดหรือในสถานการณ์ใดบ้าง</span><span class="sxs-lookup"><span data-stu-id="c572d-105">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="c572d-106">เมื่อคุณทราบว่าเหตุการณ์ใดที่คุณต้องได้รับการแจ้งเตือน ใน Microsoft Dynamics 365 for Finance and Operations ให้ค้นหาหน้าที่ซึ่งข้อมูลที่ทำให้เกิดเหตุการณ์นั้นแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="c572d-106">When you know which event you want to be notified about, in Microsoft Dynamics 365 for Finance and Operations find the page where the data that causes that event appears.</span></span> <span data-ttu-id="c572d-107">เหตุการณ์อาจเป็นวันที่ที่มาถึง หรือการเปลี่ยนแปลงบางอย่างที่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="c572d-107">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="c572d-108">ดังนั้น คุณต้องค้นหาหน้าที่ซึ่งมีการระบุวันที่ หรือที่ซึ่งฟิลด์ที่เปลี่ยนแปลงหรือเรกคอร์ดใหม่ที่ถูกสร้างขึ้น ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="c572d-108">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="c572d-109">หลังจากที่คุณมีข้อมูลดังกล่าวแล้ว คุณก็สามารถสร้างกฎการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="c572d-109">After you have this information, you can create the alert rule.</span></span>

<span data-ttu-id="c572d-110">เมื่อคุณสร้างกฎการแจ้งเตือน คุณกำหนดเงื่อนไขที่ต้องปฏิบัติตาม ก่อนที่ข้อความแจ้งเตือนจะถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="c572d-110">When you create an alert rule, you define the criteria that must be met before an alert is triggered.</span></span> <span data-ttu-id="c572d-111">คุณอาจนึกถึงเงื่อนไขในรูปของการจับคู่ระหว่างการเกิดขึ้นของเหตุการณ์หนึ่งและการตอบสนองเงื่อนไขบางอย่าง </span><span class="sxs-lookup"><span data-stu-id="c572d-111">You can think of criteria as a match between the occurrence of an event and the fulfillment of specific conditions.</span></span> <span data-ttu-id="c572d-112">เมื่อเหตุการณ์เกิดขึ้น ระบบจะเริ่มต้นทำการตรวจสอบตามเงื่อนไขที่ถูกตั้งค่าไว้ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c572d-112">When an event occurs, the system starts to perform a check according to the conditions that are set up in Finance and Operations.</span></span>

## <a name="events"></a><span data-ttu-id="c572d-113">เหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="c572d-113">Events</span></span>

<span data-ttu-id="c572d-114">เหตุการณ์ที่ทริกเกอร์กฎการแจ้งเตือนอาจเป็นวันที่ที่มาถึงหรือการเปลี่ยนแปลงเฉพาะที่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="c572d-114">The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="c572d-115">ทริกเกอร์สำหรับเหตุการณ์ถูกกำหนดไว้บน FastTab **แจ้งเตือนฉันเมื่อ** ของกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="c572d-115">Triggers for events are defined on the **Alert me when** FastTab of the **Create alert rule** dialog box.</span></span> <span data-ttu-id="c572d-116">เหตุการณ์ที่พร้อมใช้งานสำหรับฟิลด์เฉพาะ จะขึ้นอยู่กับทริกเกอร์ที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="c572d-116">The events that are available for a particular field depend on the trigger that is selected.</span></span>

<span data-ttu-id="c572d-117">ตัวอย่างเช่น ถ้าคุณกำลังตั้งค่ากฎการแจ้งเตือนสำหรับฟิลด์ **วันที่เริ่มต้น** เหตุการณ์ตามวันครบกำหนดจะเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="c572d-117">For example, if you're setting up an alert rule for the **Start date** field, due date events are appropriate.</span></span> <span data-ttu-id="c572d-118">ดังนั้น ชนิดเหตุการณ์ **จะครบกำหนดใน** จะพร้อมใช้งานสำหรับฟิลด์นั้น</span><span class="sxs-lookup"><span data-stu-id="c572d-118">Therefore, the **is due in** event type is available for that field.</span></span> <span data-ttu-id="c572d-119">อย่างไรก็ตาม สำหรับฟิลด์ เช่น **ศูนย์ต้นทุน** เหตุการณ์ตามวันครบกำหนดจะไม่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="c572d-119">However, for a field such as **Cost center**, a due date event isn't appropriate.</span></span> <span data-ttu-id="c572d-120">ดังนั้น ชนิดเหตุการณ์ **จะครบกำหนดใน** จะไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c572d-120">Therefore, the **is due in** event type isn't available.</span></span> <span data-ttu-id="c572d-121">ชนิดเหตุการณ์ **ได้เปลี่ยนแปลง** จะพร้อมใช้งานแทน</span><span class="sxs-lookup"><span data-stu-id="c572d-121">Instead, the **has changed** event type is available.</span></span>

## <a name="event-types"></a><span data-ttu-id="c572d-122">ชนิดของเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="c572d-122">Event types</span></span>

<span data-ttu-id="c572d-123">ชนิดเหตุการณ์สามชนิดสามารถเกิดขึ้นได้:</span><span class="sxs-lookup"><span data-stu-id="c572d-123">Three types of events can occur:</span></span>

- <span data-ttu-id="c572d-124">**เหตุการณ์ชนิดการสร้างและชนิดการลบ** – เหตุการณ์เหล่านี้ทริกเกอร์ข้อความแจ้งเตือน เมื่อมีการสร้างหรือการลบเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c572d-124">**Create-type and delete-type events** – These events trigger an alert when a record is created or deleted.</span></span>
- <span data-ttu-id="c572d-125">**เหตุการณ์ชนิดการอัพเดต** – เหตุการณ์เหล่านี้ทริกเกอร์ข้อความแจ้งเตือน เมื่อข้อมูลในฟิลด์เฉพาะเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="c572d-125">**Update-type events** – These events trigger an alert when the data in a specific field changes.</span></span>
- <span data-ttu-id="c572d-126">**เหตุการณ์ชนิดวันครบกำหนด** – เหตุการณ์เหล่านี้ทริกเกอร์ข้อความแจ้งเตือน เมื่อวันที่มาถึง</span><span class="sxs-lookup"><span data-stu-id="c572d-126">**Due date-type events** – These events trigger an alert when a date arrives.</span></span>
    
<span data-ttu-id="c572d-127">สามารถเริ่มต้นการเปลี่ยนแปลงที่เกิดขึ้นได้โดยผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c572d-127">Changes that occur can be initiated by a user.</span></span> <span data-ttu-id="c572d-128">ตัวอย่างเช่น ผู้ใช้เปลี่ยนวันที่จัดส่งของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="c572d-128">For example, a user changes the delivery date of a purchase order.</span></span> <span data-ttu-id="c572d-129">อีกทางหนึ่งคือ การเปลี่ยนแปลงอาจเกิดขึ้นเป็นส่วนหนึ่งของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="c572d-129">Alternatively, changes can occur as part of a process.</span></span> <span data-ttu-id="c572d-130">ตัวอย่างเช่น ฟิลด์ **สถานะ** ในหน้า เปลี่ยนแปลงเพื่อสะท้อนวงจรชีวิตของกระบวนการต่างๆ ในระบบ</span><span class="sxs-lookup"><span data-stu-id="c572d-130">For example, the **Status** field on a page changes to reflect the life cycle of various processes in the system.</span></span>

## <a name="conditions"></a><span data-ttu-id="c572d-131">เงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="c572d-131">Conditions</span></span>

<span data-ttu-id="c572d-132">บน FastTab **แจ้งเตือนฉันสำหรับ** ของกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** คุณสามารถใช้เงื่อนไขเพื่อควบคุมได้ เมื่อคุณได้รับการแจ้งเตือนเกี่ยวกับเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="c572d-132">On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can use conditions to control when you're alerted about events.</span></span>

<span data-ttu-id="c572d-133">ตัวอย่างเช่น คุณสามารถระบุว่า ระบบควรแจ้งเตือนคุณเมื่อสถานะของใบสั่งซื้อเปลี่ยนแปลง แต่ก็ต่อเมื่อสถานะตรงกับชุดเงื่อนไขที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="c572d-133">For example, you can specify that the system should alert you when the status of purchase orders changes, but only if the status matches a specific set of conditions.</span></span> <span data-ttu-id="c572d-134">กล่าวคือ คุณต้องการได้รับการแจ้งเตือน เมื่อสถานะของใบสั่งซื้อถูกตั้งค่าเป็น **ได้รับแล้ว**</span><span class="sxs-lookup"><span data-stu-id="c572d-134">Specifically, you want to be alerted when the status of a purchase order is set to **Received**.</span></span> <span data-ttu-id="c572d-135">การเปลี่ยนแปลงนี้ในสถานะเป็นเหตุการณ์ที่ทริกเกอร์การแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c572d-135">This change in status is the event that triggers the alert.</span></span>

<span data-ttu-id="c572d-136">ถัดไป คุณต้องตัดสินใจว่า ใบสั่งซื้อใดที่คุณต้องการจะรับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c572d-136">Next, you must decide which purchase orders you want to be alerted about.</span></span> <span data-ttu-id="c572d-137">ตัวอย่างเช่น คุณสามารถเลือกตัวเลือกใดตัวเลือกหนึ่งได้ดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c572d-137">For example, you can select one of the following options.</span></span> <span data-ttu-id="c572d-138">ตัวเลือกเหล่านี้กำหนดเงื่อนไขสำหรับกฎการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c572d-138">These options define the conditions for the alert rule.</span></span>

- <span data-ttu-id="c572d-139">**เรกคอร์ดที่เลือกปัจจุบัน** – คุณได้รับข้อความแจ้งเตือน เมื่อสถานะของใบสั่งซื้อเฉพาะเปลี่ยนเป็น **ได้รับแล้ว**</span><span class="sxs-lookup"><span data-stu-id="c572d-139">**Current selected record** – You receive an alert when the status of a specific purchase order changes to **Received**.</span></span>
- <span data-ttu-id="c572d-140">**เรกคอร์ดทั้งหมด** – คุณได้รับข้อความแจ้งเตือน เมื่อสถานะของใบสั่งซื้อถูกเปลี่ยนสำหรับสินค้าในมุมมองเพจที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="c572d-140">**All records** – You receive an alert when the status of a purchase order is changed for an item in the active page view.</span></span> <span data-ttu-id="c572d-141">คุณสามารถใช้การกรองขั้นสูงที่มีอยู่บนหน้าเพื่อสร้างกฎสำหรับชุดของเรกคอร์ดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c572d-141">You can use the advanced filtering that is available on the page to create rules for a specific set of records.</span></span> <span data-ttu-id="c572d-142">ตัวอย่างเช่น คุณสามารถสร้างข้อความแจ้งเตือนที่ถูกทริกเกอร์สำหรับใบสั่งซื้อทั้งหมดสำหรับลูกค้าในกลุ่มลูกค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c572d-142">For example, you can create an alert that is triggered for all purchase orders for the customers in a specific customer group.</span></span>
    
## <a name="expiry-of-rule"></a><span data-ttu-id="c572d-143">วันหมดอายุของกฎ</span><span class="sxs-lookup"><span data-stu-id="c572d-143">Expiry of rule</span></span>

<span data-ttu-id="c572d-144">บน FastTab **แจ้งเตือนฉันจนกว่า** ของกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** คุณสามารถระบุระยะเวลาที่ควรเปิดใช้งานกฎการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="c572d-144">On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>

## <a name="alert-contents"></a><span data-ttu-id="c572d-145">แจ้งเตือนเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="c572d-145">Alert contents</span></span>

<span data-ttu-id="c572d-146">บน FastTab **แจ้งเตือนฉันด้วย** ของกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** คุณสามารถระบุข้อความชื่อเรื่องและข้อความข่าวสารที่ข้อความแจ้งเตือนควรใช้</span><span class="sxs-lookup"><span data-stu-id="c572d-146">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>

## <a name="user-id"></a><span data-ttu-id="c572d-147">รหัสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c572d-147">User ID</span></span>

<span data-ttu-id="c572d-148">บน FastTab **แจ้งเตือนฉันด้วย** ของกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** คุณสามารถระบุผู้ใช้ที่ควรได้รับข้อความแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="c572d-148">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="c572d-149">โดยค่าเริ่มต้น มีการเลือกรหัสผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c572d-149">By default, your user ID is selected.</span></span> <span data-ttu-id="c572d-150">ตัวเลือกนี้ถูกจำกัดแก่ผู้ดูแลระบบขององค์กร</span><span class="sxs-lookup"><span data-stu-id="c572d-150">This option is restricted to organization administrators.</span></span>

## <a name="create-an-alert-rule"></a><span data-ttu-id="c572d-151">สร้างกฎการแจ้งเตือน </span><span class="sxs-lookup"><span data-stu-id="c572d-151">Create an alert rule</span></span>

1. <span data-ttu-id="c572d-152">เปิดหน้าที่มีข้อมูลที่จะตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="c572d-152">Open the page that contains the data to monitor.</span></span>
2. <span data-ttu-id="c572d-153">บนบานหน้าต่างการดำเนินการ บนแท็บ **ตัวเลือก** ในกลุ่ม **แบ่งปัน** เลือก **สร้างกฎการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="c572d-153">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create alert rule**.</span></span>
3. <span data-ttu-id="c572d-154">ในกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** ในฟิลด์ **ฟิลด์** ให้เลือกฟิลด์ที่จะตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="c572d-154">In the **Create alert rule** dialog box, in the **Field** field, select the field to monitor.</span></span>
4. <span data-ttu-id="c572d-155">ในฟิลด์ **เหตุการณ์** เลือกชนิดของเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="c572d-155">In the **Event** field, select the type of event.</span></span>
5. <span data-ttu-id="c572d-156">บน FastTab **แจ้งเตือนฉันสำหรับ** เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c572d-156">On the **Alert me for** FastTab, select an option.</span></span>
6. <span data-ttu-id="c572d-157">ถ้ากฎการแจ้งเตือนควรกลายเป็นปิดใช้งานในวันที่หนึ่งๆ บน FastTab **แจ้งเตือนฉันจนกว่า** ให้เลือกวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="c572d-157">If the alert rule should become inactive on a specific date, on the **Alert me until** FastTab, select an end date.</span></span>
7. <span data-ttu-id="c572d-158">บน FastTab **แจ้งเตือนฉันด้วย** ในฟิลด์ **ชื่อเรื่อง** ยอมรับหัวข้อเรื่องค่าเริ่มต้นสำหรับข้อความอีเมล หรือป้อนชื่อเรื่องใหม่</span><span class="sxs-lookup"><span data-stu-id="c572d-158">On the **Alert me with** FastTab, in the **Subject** field, accept the default subject heading for the email message, or enter a new subject.</span></span> <span data-ttu-id="c572d-159">ข้อความจะใช้เป็นหัวข้อเรื่องสำหรับข้อความอีเมลที่คุณได้รับเมื่อการแจ้งเตือนถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="c572d-159">The text is used as the subject heading for the email message that you receive when an alert is triggered.</span></span>
8. <span data-ttu-id="c572d-160">ในฟิลด์ **ข้อความ** ป้อนข้อความที่ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="c572d-160">In the **Message** field, enter an optional message.</span></span> <span data-ttu-id="c572d-161">ใบสั่งซื้อย่อยเป็นใบสั่งซื้อที่ถูกนำออกใช้จากข้อตกลงการซื้อที่มีอยู่ เมื่อคุณนำรายการใบสั่งจากข้อตกลงการซื้อออกใช้ เงื่อนไขข้อผูกมัดที่ระบุไว้ในข้อตกลงการซื้อจะถูกนำไปใช้กับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="c572d-161">The text is used as the message that you receive when an alert is triggered.</span></span>
9. <span data-ttu-id="c572d-162">เลือก **ตกลง** เพื่อบันทึกการตั้งค่าและสร้างกฎการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c572d-162">Select **OK** to save the settings and create the alert rule.</span></span>

