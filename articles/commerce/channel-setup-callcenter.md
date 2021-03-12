---
title: ตั้งค่าช่องทางศูนย์บริการ
description: หัวข้อนี้จะอธิบายวิธีการสร้างช่องทางศูนย์บริการใหม่ใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b25626dafc07d576699ceba3cc9ca691db45cb9f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997761"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="8ba12-103">ตั้งค่าช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8ba12-104">หัวข้อนี้จะอธิบายวิธีการสร้างช่องทางศูนย์บริการใหม่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8ba12-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8ba12-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="8ba12-105">Overview</span></span>


<span data-ttu-id="8ba12-106">ใน Dynamics 365 Commerce ศูนย์บริการคือประเภทของช่องทาง Commerce ที่สามารถถูกกำหนดในแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="8ba12-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="8ba12-107">การกำหนดช่องทางสำหรับเอนทิตี้ศูนย์บริการของคุณ ช่วยให้ระบบสามารถผูกข้อมูล และการประมวลผลใบสั่งที่เฉพาะเจาะจงไปยังใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="8ba12-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="8ba12-108">ในขณะที่บริษัทสามารถกำหนดช่องทางของศูนย์บริการที่หลากหลายใน Commerce จำเป็นต้องทราบว่าผู้ใช้แต่ละคนอาจเชื่อมโยงกับช่องทางศูนย์บริการเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8ba12-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="8ba12-109">ก่อนที่คุณจะสร้างช่องทางศูนย์บริการใหม่ ให้ตรวจสอบให้แน่ใจว่าคุณได้ดำเนินการ [ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง](channels-prerequisites.md) เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="8ba12-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="8ba12-110">สร้างและกำหนดค่าของช่องทางศูนย์บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="8ba12-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="8ba12-111">เมื่อต้องการสร้างและตั้งค่าคอนฟิกช่องทางศูนย์บริการใหม่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8ba12-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="8ba12-112">ในบานหน้าต่างนำทาง ไปที่ **Retail และ Commerce \> ช่องทาง \> ศูนย์บริการ \> ศูนย์บริการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8ba12-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="8ba12-113">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8ba12-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8ba12-114">ในฟิลด์ **ชื่อ** ให้ระบุชื่อสำหรับช่องทางใหม่</span><span class="sxs-lookup"><span data-stu-id="8ba12-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="8ba12-115">เลือก **นิติบุคคล** ที่เหมาะสมจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8ba12-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="8ba12-116">เลือกสถานที่ **นิติบุคคล** ที่เหมาะสมจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8ba12-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="8ba12-117">สถานที่นี้จะใช้เป็นค่าเริ่มต้นในใบสั่งขายที่สร้างขึ้นสำหรับช่องทางศูนย์บริการนี้ ยกเว้นว่าจะมีการกำหนดค่าเริ่มต้นอื่นๆ ที่ระดับลูกค้าหรือสินค้า</span><span class="sxs-lookup"><span data-stu-id="8ba12-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="8ba12-118">ในฟิลด์ **ลูกค้าเริ่มต้น** ให้ระบุลูกค้าเริ่มต้นที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8ba12-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="8ba12-119">ข้อมูลนี้จะใช้เพื่อช่วยในการเติมค่าเริ่มต้นโดยอัตโนมัติ เมื่อมีการสร้างเรกคอร์ดลูกค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="8ba12-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="8ba12-120">เมื่อสร้างใบสั่งศูนย์บริการ จะไม่แนะนำให้สร้างใบสั่งสำหรับลูกค้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ba12-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="8ba12-121">ในฟิลด์ **โปรไฟล์การแจ้งเตือนทางอีเมล** ให้ระบุโปรไฟล์การแจ้งเตือนทางอีเมลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8ba12-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="8ba12-122">เมื่อสร้างและประมวลผลใบสั่งศูนย์การบริการ จะมีการใช้โพรไฟล์การแจ้งเตือนทางอีเมลเพื่อทริกเกอร์ข้อความแจ้งเตือนทางอีเมลแบบอัตโนมัติให้ไปยังลูกค้าที่มีข้อมูลเกี่ยวกับสถานะใบสั่งของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="8ba12-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="8ba12-123">ระบุรหัสข้อมูล **การแทนที่ราคา**</span><span class="sxs-lookup"><span data-stu-id="8ba12-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="8ba12-124">คุณอาจต้องสร้างรหัสข้อมูลสำหรับรายการนี้ก่อน</span><span class="sxs-lookup"><span data-stu-id="8ba12-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="8ba12-125">รหัสข้อมูลนี้จะให้ชุดของรหัสเหตุผลที่ผู้ใช้จะได้รับพร้อมท์ให้เลือก เมื่อใช้ฟังก์ชันการแทนที่ราคาในใบสั่งศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="8ba12-126">ระบุรหัสข้อมูล **การระงับ**</span><span class="sxs-lookup"><span data-stu-id="8ba12-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="8ba12-127">คุณอาจต้องสร้างรหัสข้อมูลสำหรับรายการนี้ก่อน</span><span class="sxs-lookup"><span data-stu-id="8ba12-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="8ba12-128">รหัสข้อมูลนี้จะให้ชุดของรหัสเหตุผลที่ไม่จำเป็นต้องระบุที่ผู้ใช้จะได้รับพร้อมท์ให้เลือก เมื่อระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="8ba12-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="8ba12-129">ระบุรหัสข้อมูล **เครดิต**</span><span class="sxs-lookup"><span data-stu-id="8ba12-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="8ba12-130">คุณอาจต้องสร้างรหัสข้อมูลสำหรับรายการนี้ก่อน</span><span class="sxs-lookup"><span data-stu-id="8ba12-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="8ba12-131">รหัสข้อมูลนี้จะให้ชุดของรหัสเหตุผลที่ผู้ใช้สามารถเลือกได้ เมื่อใช้ฟังก์ชันเครดิตของใบสั่งของศูนย์บริการเพื่อให้มีการขอคืนเงินเบ็ดเตล็ดแก่ลูกค้าสำหรับเหตุผลของการบริการลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8ba12-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="8ba12-132">ไม่จำเป็นต้องระบุ: ตั้งค่ามิติทางการเงินบน FastTab **มิติทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="8ba12-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="8ba12-133">มิติที่ป้อนที่นี่จะเป็นค่าเริ่มต้นในใบสั่งขายใดๆ ที่สร้างขึ้นในช่องทางของศูนย์บริการนี้</span><span class="sxs-lookup"><span data-stu-id="8ba12-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="8ba12-134">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8ba12-134">Click **Save**.</span></span>

<span data-ttu-id="8ba12-135">รูปภาพต่อไปนี้แสดงการสร้างช่องทางศูนย์บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="8ba12-135">The following image shows the creation of a new call center channel.</span></span>

![ช่องทางศูนย์บริการใหม่](media/channel-setup-callcenter-1.png)

<span data-ttu-id="8ba12-137">รูปภาพต่อไปนี้แสดงตัวอย่างของช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-137">The following image shows an example call center channel.</span></span>

![ตัวอย่างช่องทางศูนย์บริการ](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="8ba12-139">การตั้งค่าช่องทางเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8ba12-139">Additional channel setup</span></span>

<span data-ttu-id="8ba12-140">งานเพิ่มเติมที่จำเป็นสำหรับการตั้งค่าช่องทางศูนย์บริการ รวมถึงการตั้งค่าวิธีการชำระเงิน และวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="8ba12-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="8ba12-141">รูปภาพต่อไปนี้แสดงตัวเลือกการตั้งค่า **โหมดการจัดส่ง** และ **วิธีการชำระเงิน** บนแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="8ba12-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![การดำเนินการตั้งค่าช่องทางศูนย์บริการเพิ่มเติม](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="8ba12-143">การตั้งค่าวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="8ba12-143">Set up payment methods</span></span>

<span data-ttu-id="8ba12-144">เมื่อต้องการตั้งค่าวิธีการชำระเงิน ให้ทำตามขั้นตอนต่อไปนี้สำหรับชนิดการชำระเงินแต่ละชนิดที่สนับสนุนบนช่องทางนี้</span><span class="sxs-lookup"><span data-stu-id="8ba12-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="8ba12-145">ผู้ใช้จะต้องเลือกจากวิธีการชำระเงินที่กำหนดไว้ล่วงหน้าเพื่อเชื่อมโยงกับช่องทางของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="8ba12-146">ก่อนที่จะตั้งค่าวิธีการชำระเงินของศูนย์บริการของคุณ ก่อนอื่นให้ตั้งค่าวิธีการชำระเงินหลักใน **Retail และ Commerce \> การตั้งค่าช่องทาง \> วิธีการชำระเงิน \> วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="8ba12-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="8ba12-147">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และจากนั้นเลือก **วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="8ba12-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="8ba12-148">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8ba12-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8ba12-149">ในบานหน้าต่างนำทาง ให้เลือกวิธีการชำระเงินจากการชำระเงินที่กำหนดไว้ล่วงหน้าที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8ba12-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="8ba12-150">ตั้งค่าคอนฟิกการตั้งค่าเพิ่มเติมใด ๆ ตามต้องการสำหรับชนิดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="8ba12-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="8ba12-151">สำหรับบัตรเครดิต บัตรของขวัญ หรือบัตรสมาชิก ต้องมีการตั้งค่าเพิ่มเติมโดยการเลือกฟังก์ชัน **การตั้งค่าบัตร**</span><span class="sxs-lookup"><span data-stu-id="8ba12-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="8ba12-152">ตั้งค่าคอนฟิกบัญชีการลงรายการบัญชีที่เหมาะสมสำหรับชนิดการชำระเงินในส่วน **การลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="8ba12-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="8ba12-153">บนบานหน้าต่างการดำเนินการ คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8ba12-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="8ba12-154">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการชำระเงินสด</span><span class="sxs-lookup"><span data-stu-id="8ba12-154">The following image shows an example of a cash payment method.</span></span>

![ตัวอย่างวิธีการชำระเงิน](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="8ba12-156">ตั้งค่าวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="8ba12-156">Set up modes of delivery</span></span>

<span data-ttu-id="8ba12-157">คุณสามารถดูวิธีการจัดส่งที่ตั้งค่าคอนฟิกได้โดยการเลือก **วิธีการจัดส่ง** จากแท็บ **การตั้งค่า** ใน **บานหน้าต่างการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="8ba12-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="8ba12-158">เมื่อต้องการเปลี่ยนแปลงหรือเพิ่มโหมดการจัดส่งที่จะเชื่อมโยงกับช่องทางของศูนย์บริการ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8ba12-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="8ba12-159">จากฟอร์มโหมดการจัดส่งของศูนย์บริการ เลือก **จัดการโหมดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="8ba12-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="8ba12-160">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างวิธีการจัดส่งใหม่ หรือเลือกโหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="8ba12-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="8ba12-161">ในส่วน **ช่องทางการขายปลีก** ให้คลิก **เพิ่มรายการ** เพื่อเพิ่มช่องทางของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="8ba12-162">การเพิ่มช่องทางโดยใช้โหนดขององค์กรแทนที่การเพิ่มช่องทางแต่ละช่องสามารถเพิ่มประสิทธิภาพการเพิ่มช่อง</span><span class="sxs-lookup"><span data-stu-id="8ba12-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="8ba12-163">ตรวจสอบให้แน่ใจว่าได้ตั้งค่าคอนฟิกโหมดการจัดส่งด้วยข้อมูลบน FastTab **ผลิตภัณฑ์** และ FastTab **ที่อยู่**</span><span class="sxs-lookup"><span data-stu-id="8ba12-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="8ba12-164">ถ้าไม่มีผลิตภัณฑ์หรือที่อยู่ในการจัดส่งที่ถูกต้องสำหรับโหมดการจัดส่ง การเลือกในระหว่างการป้อนข้อมูลใบสั่งจะทำให้เกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="8ba12-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="8ba12-165">หลังจากที่มีการทำการเปลี่ยนแปลงใดๆ ไปยังการตั้งค่าคอนฟิกโหมดการจัดส่งของศูนย์บริการ งาน **ประมวลผลโหมดการจัดส่ง** ต้องถูกรันเพื่อกระจายเมทริกซ์การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="8ba12-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="8ba12-166">งานนี้สามารถหาได้โดยการนำทางไปยัง **Retail และ Commerce \> Retail และ Commerce IT \> ประมวลผลโหมดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="8ba12-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="8ba12-167">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="8ba12-167">The following image shows an example of a mode of delivery.</span></span>

![ตั้งค่าวิธีการจัดส่ง](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="8ba12-169">ตั้งค่าผู้ใช้ช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8ba12-169">Set up channel users</span></span>

<span data-ttu-id="8ba12-170">เมื่อต้องการสร้างใบสั่งขายที่เชื่อมโยงกับช่องทางของศูนย์บริการจากศูนย์ควบคุม Commerce ผู้ใช้ที่สร้างใบสั่งขายจะต้องเชื่อมโยงกับช่องทางของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="8ba12-171">ผู้ใช้ไม่สามารถเชื่อมโยงใบสั่งขายที่สร้างขึ้นในศูนย์ควบคุม Commerce ไปยังช่องทางของศูนย์บริการได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="8ba12-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="8ba12-172">ลิงค์เป็นระบบ และขึ้นอยู่กับผู้ใช้และความสัมพันธ์ของผู้ใช้ไปยังช่องทางของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="8ba12-173">ผู้ใช้สามารถเชื่อมโยงกับช่องทางศูนย์บริการได้เพียงช่องทางเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8ba12-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="8ba12-174">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **ช่องทาง** และจากนั้นเลือก **ผู้ใช้ช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="8ba12-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="8ba12-175">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8ba12-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8ba12-176">เลือก **รหัสผู้ใช้** ที่มีอยู่จากรายการเลือกแบบหล่นลงเพื่อลิงค์ผู้ใช้นี้ไปยังช่องทางของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="8ba12-177">หลังจากที่การตั้งค่าผู้ใช้ช่องทางเสร็จสิ้น และผู้ใช้สร้างใบสั่งขายใหม่ในศูนย์ควบคุม Commerce ใบสั่งขายจะต้องเชื่อมโยงกับช่องทางของศูนย์บริการที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="8ba12-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="8ba12-178">การตั้งค่าคอนฟิกใดๆ ของช่องทางนี้จะนำไปใช้กับใบสั่งขายอย่างเป็นระบบ</span><span class="sxs-lookup"><span data-stu-id="8ba12-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="8ba12-179">ผู้ใช้สามารถยืนยันช่องทางของศูนย์บริการที่จะเชื่อมโยงกับใบสั่งขาย โดยการดูข้อมูลอ้างอิงชื่อช่องทางบนส่วนหัวของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="8ba12-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="8ba12-180">ตั้งค่ากลุ่มราคา</span><span class="sxs-lookup"><span data-stu-id="8ba12-180">Set up price groups</span></span>

<span data-ttu-id="8ba12-181">กลุ่มราคาไม่จำเป็นต้องระบุ แต่ถ้ามีการใช้ สามารถควบคุมราคาขายที่จะนำเสนอให้แก่ลูกค้าที่วางใบสั่งในช่องทางของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="8ba12-182">ถ้ากลุ่มราคายังไม่ได้รับการตั้งค่าคอนฟิกสำหรับลูกค้าห รือถ้ากลุ่มราคาในแค็ตตาล็อกไม่ได้ใช้กับใบสั่งขาย (โดยใช้ฟิลด์ **รหัสต้นทาง** บนส่วนหัวของใบสั่งของศูนย์บริการ) จากนั้น จะมีการใช้กลุ่มราคาของช่องทางในการค้นหาราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="8ba12-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="8ba12-183">ถ้าไม่พบกลุ่มราคาบนช่องทางของศูนย์บริการ จะมีการใช้ราคาหลักของสินค้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ba12-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="8ba12-184">เมื่อต้องการตั้งค่ากลุ่มราคา ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8ba12-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="8ba12-185">บนบานหน้าต่างการดำเนินการ ให้คลิกแท็บ **ช่องทาง** และจากนั้น เลือก **กลุ่มราคา**</span><span class="sxs-lookup"><span data-stu-id="8ba12-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="8ba12-186">บนหน้าต่างการดำเนินการ คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8ba12-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="8ba12-187">เลือก **กลุ่มราคาขายปลีก** จากรายการเลือกเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8ba12-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ba12-188">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8ba12-188">Additional resources</span></span>

[<span data-ttu-id="8ba12-189">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8ba12-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="8ba12-190">ฟังก์ชันการขายของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="8ba12-191">ตั้งค่าตัวเลือกการประมวลผลศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="8ba12-192">แค็ตตาล็อกของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="8ba12-193">ตั้งค่าและทำงานกับข้อความแจ้งเตือนการฉ้อโกง</span><span class="sxs-lookup"><span data-stu-id="8ba12-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="8ba12-194">ตั้งค่าโปรแกรมความต่อเนื่องสำหรับศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8ba12-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
