---
title: ตั้งค่าช่องทางศูนย์บริการ
description: หัวข้อนี้จะอธิบายวิธีการสร้างช่องทางศูนย์บริการใหม่ใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057890"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="fb74f-103">ตั้งค่าช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="fb74f-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fb74f-104">หัวข้อนี้จะอธิบายวิธีการสร้างช่องทางศูนย์บริการใหม่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fb74f-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fb74f-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="fb74f-105">Overview</span></span>

<span data-ttu-id="fb74f-106">ใน Dynamics 365 Commerce ศูนย์บริการคือประเภทของช่องทางที่สามารถถูกกำหนดได้ในแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="fb74f-106">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="fb74f-107">การกำหนดช่องทางสำหรับเอนทิตี้ศูนย์บริการของคุณ ช่วยให้ระบบสามารถผูกข้อมูล และการประมวลผลใบสั่งที่เฉพาะเจาะจงไปยังใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="fb74f-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="fb74f-108">บริษัทสามารถกำหนดช่องทางศูนย์บริการที่หลากหลายได้ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="fb74f-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="fb74f-109">ก่อนที่คุณจะสร้างช่องทางศูนย์บริการใหม่ให้ตรวจสอบให้แน่ใจว่าคุณได้เตรียม [ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง](channels-prerequisites.md) เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="fb74f-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="fb74f-110">สร้างและกำหนดค่าของช่องทางศูนย์บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="fb74f-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="fb74f-111">เมื่อต้องการสร้างและตั้งค่าคอนฟิกช่องทางศูนย์บริการใหม่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fb74f-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="fb74f-112">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> ช่องทาง \> ศูนย์บริการ \> ศูนย์บริการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="fb74f-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="fb74f-113">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="fb74f-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fb74f-114">ในฟิลด์ **ชื่อ** ให้ระบุชื่อสำหรับช่องทางใหม่</span><span class="sxs-lookup"><span data-stu-id="fb74f-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="fb74f-115">เลือก **นิติบุคคล** ที่เหมาะสมจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="fb74f-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="fb74f-116">เลือกสถานที่ **นิติบุคคล** ที่เหมาะสมจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="fb74f-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="fb74f-117">ในฟิลด์ **ลูกค้าเริ่มต้น** ให้ระบุลูกค้าเริ่มต้นที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fb74f-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="fb74f-118">ในฟิลด์ **โปรไฟล์การแจ้งเตือนทางอีเมล** ให้ระบุโปรไฟล์การแจ้งเตือนทางอีเมลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fb74f-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="fb74f-119">ระบุรหัสข้อมูล **การแทนที่ราคา**</span><span class="sxs-lookup"><span data-stu-id="fb74f-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="fb74f-120">หมายเหตุ คุณอาจต้องสร้างรหัสข้อมูลก่อน</span><span class="sxs-lookup"><span data-stu-id="fb74f-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="fb74f-121">ระบุรหัสข้อมูล **การระงับ**</span><span class="sxs-lookup"><span data-stu-id="fb74f-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="fb74f-122">หมายเหตุ คุณอาจต้องสร้างรหัสข้อมูลก่อน</span><span class="sxs-lookup"><span data-stu-id="fb74f-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="fb74f-123">ระบุรหัสข้อมูล **เครดิต**</span><span class="sxs-lookup"><span data-stu-id="fb74f-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="fb74f-124">หมายเหตุ คุณอาจต้องสร้างรหัสข้อมูลก่อน</span><span class="sxs-lookup"><span data-stu-id="fb74f-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="fb74f-125">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fb74f-125">Select **Save**.</span></span>

<span data-ttu-id="fb74f-126">รูปภาพต่อไปนี้แสดงการสร้างช่องทางศูนย์บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="fb74f-126">The following image shows the creation of a new call center channel.</span></span>

![ช่องทางศูนย์บริการใหม่](media/channel-setup-callcenter-1.png)

<span data-ttu-id="fb74f-128">รูปภาพต่อไปนี้แสดงตัวอย่างของช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="fb74f-128">The following image shows an example call center channel.</span></span>

![ตัวอย่างช่องทางศูนย์บริการ](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="fb74f-130">การตั้งค่าช่องทางเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fb74f-130">Additional channel setup</span></span>

<span data-ttu-id="fb74f-131">งานเพิ่มเติมที่จำเป็นสำหรับการตั้งค่าช่องทางศูนย์บริการ รวมถึงการตั้งค่าวิธีการชำระเงิน และวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fb74f-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="fb74f-132">รูปภาพต่อไปนี้แสดงตัวเลือกการตั้งค่า **วิธีการจัดส่ง** และ **วิธีการชำระเงิน** บนแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="fb74f-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![การดำเนินการตั้งค่าช่องทางศูนย์บริการเพิ่มเติม](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="fb74f-134">การตั้งค่าวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="fb74f-134">Set up payment methods</span></span>

<span data-ttu-id="fb74f-135">เมื่อต้องการตั้งค่าวิธีการชำระเงิน สำหรับชนิดการชำระเงินแต่ละชนิดที่สนับสนุนบนช่องทางนี้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fb74f-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="fb74f-136">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และจากนั้นเลือก **วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="fb74f-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="fb74f-137">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="fb74f-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fb74f-138">ในบานหน้าต่างนำทาง ให้เลือกวิธีการชำระเงินที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fb74f-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="fb74f-139">ในส่วน **ทั่วไป** ให้ระบุ **ชื่อการดำเนินงาน** และตั้งค่าคอนฟิกการตั้งค่าที่ต้องการอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="fb74f-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="fb74f-140">ตั้งค่าคอนฟิกการตั้งค่าเพิ่มเติมใด ๆ ตามต้องการสำหรับชนิดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="fb74f-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="fb74f-141">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="fb74f-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="fb74f-142">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการชำระเงินสด</span><span class="sxs-lookup"><span data-stu-id="fb74f-142">The following image shows an example of a cash payment method.</span></span>

![ตัวอย่างวิธีการชำระเงิน](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="fb74f-144">ตั้งค่าวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fb74f-144">Set up modes of delivery</span></span>

<span data-ttu-id="fb74f-145">คุณสามารถดูวิธีการจัดส่งที่ตั้งค่าคอนฟิกได้โดยการเลือก **วิธีการจัดส่ง** จากแท็บ **การตั้งค่า** ใน **บานหน้าต่างการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="fb74f-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="fb74f-146">เมื่อต้องการเปลี่ยนหรือเพิ่มวิธีการจัดส่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fb74f-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="fb74f-147">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การบริหารสินค้าคงคลัง \> วิธีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="fb74f-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="fb74f-148">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างวิธีการจัดส่งใหม่ หรือเลือกโหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="fb74f-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="fb74f-149">ในส่วน **ช่องทางการขายปลีก** ให้เลือก **เพิ่มบรรทัด** เพื่อเพิ่มช่องทาง</span><span class="sxs-lookup"><span data-stu-id="fb74f-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="fb74f-150">การเพิ่มช่องทางโดยใช้โหนดขององค์กรแทนที่การเพิ่มช่องทางแต่ละช่องสามารถเพิ่มประสิทธิภาพการเพิ่มช่อง</span><span class="sxs-lookup"><span data-stu-id="fb74f-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="fb74f-151">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fb74f-151">The following image shows an example of a mode of delivery.</span></span>

![ตั้งค่าวิธีการจัดส่ง](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="fb74f-153">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fb74f-153">Additional resources</span></span>

[<span data-ttu-id="fb74f-154">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="fb74f-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="fb74f-155">ฟังก์ชันการขายของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="fb74f-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="fb74f-156">ตั้งค่าตัวเลือกการประมวลผลศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="fb74f-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="fb74f-157">แค็ตตาล็อกของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="fb74f-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="fb74f-158">ตั้งค่าและทำงานกับข้อความแจ้งเตือนการฉ้อโกง</span><span class="sxs-lookup"><span data-stu-id="fb74f-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="fb74f-159">ตั้งค่าโปรแกรมความต่อเนื่องสำหรับศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="fb74f-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
