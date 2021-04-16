---
title: ตั้งค่าช่องทางออนไลน์
description: หัวข้อนี้จะอธิบายวิธีการสร้างช่องทางออนไลน์ใหม่ใน Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b6bf158361f95b6551b29f195616cf21f908b802
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800650"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="7344a-103">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="7344a-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7344a-104">หัวข้อนี้จะอธิบายวิธีการสร้างช่องทางออนไลน์ใหม่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7344a-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7344a-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="7344a-105">Overview</span></span>

<span data-ttu-id="7344a-106">Dynamics 365 Commerce รองรับช่องทางการขายปลีกที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="7344a-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="7344a-107">ช่องทางการขายปลีกเหล่านี้รวมร้านค้าออนไลน์ ศูนย์บริการ และร้านค้าปลีก (เรียกอีกอย่างหนึ่งว่า ร้านค้าที่ให้บริการจริง)</span><span class="sxs-lookup"><span data-stu-id="7344a-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="7344a-108">ร้านค้าออนไลน์ให้มีตัวเลือกการซื้อเพื่อให้ลูกค้าสามารถซื้อผลิตภัณฑ์จากร้านค้าออนไลน์ของผู้ค้าปลีกได้ นอกเหนือจากร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="7344a-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="7344a-109">เมื่อต้องการสร้างร้านค้าออนไลน์ใน Commerce คุณต้องสร้างช่องทางออนไลน์ก่อน</span><span class="sxs-lookup"><span data-stu-id="7344a-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="7344a-110">ก่อนที่คุณจะสร้างช่องทางออนไลน์ใหม่ให้ตรวจสอบให้แน่ใจว่าคุณได้เตรียม [ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง](channels-prerequisites.md) เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="7344a-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="7344a-111">ก่อนที่คุณจะสามารถสร้างไซต์ใหม่ได้ ต้องสร้างร้านค้าออนไลน์ใน Commerce อย่างน้อยหนึ่งร้าน</span><span class="sxs-lookup"><span data-stu-id="7344a-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="7344a-112">สำหรับข้อมูลเพิ่มเติมให้ดูที่ [สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="7344a-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="7344a-113">สร้างและกำหนดค่าของช่องทางออนไลน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="7344a-113">Create and configure a new online channel</span></span>

<span data-ttu-id="7344a-114">เมื่อต้องการสร้างและตั้งค่าคอนฟิกช่องทางออนไลน์ใหม่ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7344a-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="7344a-115">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> ช่องทาง \> ร้านค้าออนไลน์**</span><span class="sxs-lookup"><span data-stu-id="7344a-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="7344a-116">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7344a-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7344a-117">ในฟิลด์ **ชื่อ** ให้ระบุชื่อสำหรับช่องทางใหม่</span><span class="sxs-lookup"><span data-stu-id="7344a-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="7344a-118">ในรายการแบบหล่นลงของ **นิติบุคคล** ให้ป้อนนิติบุคคลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7344a-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="7344a-119">ในรายการแบบหล่นลงของ **คลังสินค้า** ให้ป้อนคลังสินค้าที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7344a-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="7344a-120">ในฟิลด์ **โซนเวลาร้านค้า** ให้เลือกโซนเวลาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7344a-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="7344a-121">ในฟิลด์ **สกุลเงิน** ให้เลือกสกุลเงินที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7344a-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="7344a-122">ในฟิลด์ **ลูกค้าเริ่มต้น** ให้ระบุลูกค้าเริ่มต้นที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7344a-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="7344a-123">ในฟิลด์ **สมุดที่อยู่ของลูกค้า** ให้ระบุสมุดที่อยู่ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7344a-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="7344a-124">ในฟิลด์ **โปรไฟล์ฟังก์ชัน** ให้เลือกโปรไฟล์ฟังก์ชันถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="7344a-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="7344a-125">ในฟิลด์ **โปรไฟล์การแจ้งเตือนทางอีเมล** ให้ระบุโปรไฟล์การแจ้งเตือนทางอีเมลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7344a-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="7344a-126">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7344a-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7344a-127">รูปภาพต่อไปนี้แสดงการสร้างช่องทางออนไลน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="7344a-127">The following image shows the creation of a new online channel.</span></span>

![ช่องทางออนไลน์ใหม่](media/channel-setup-online-1.png)

<span data-ttu-id="7344a-129">รูปภาพต่อไปนี้แสดงตัวอย่างของช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="7344a-129">The following image shows an example online channel.</span></span>

![ตัวอย่างช่องทางออนไลน์](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="7344a-131">ตั้งค่าภาษา</span><span class="sxs-lookup"><span data-stu-id="7344a-131">Set up languages</span></span>

<span data-ttu-id="7344a-132">ถ้าไซต์อีคอมเมิร์ซของคุณจะสนับสนุนหลายภาษา ให้ขยาย **ภาษา** และเพิ่มภาษาเพิ่มเติมตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="7344a-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="7344a-133">การตั้งค่าบัญชีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7344a-133">Set up payment account</span></span>

<span data-ttu-id="7344a-134">จากส่วน **บัญชีการชำระเงิน** คุณสามารถเพิ่มผู้ให้บริการชำระเงินภายนอกได้</span><span class="sxs-lookup"><span data-stu-id="7344a-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="7344a-135">สำหรับข้อมูลเกี่ยวกับการตั้งค่าตัวเชื่อมต่อการชำระเงิน Adyen ดู [ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen](../retail/dev-itpro/adyen-connector.md)</span><span class="sxs-lookup"><span data-stu-id="7344a-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="7344a-136">การตั้งค่าช่องทางเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7344a-136">Additional channel setup</span></span>

<span data-ttu-id="7344a-137">งานเพิ่มเติมที่จำเป็นสำหรับการตั้งค่าช่องทางออนไลน์ รวมถึงการตั้งค่าวิธีการชำระเงิน โหมดการจัดส่ง และการกำหนดกลุ่มการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="7344a-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="7344a-138">รูปภาพต่อไปนี้แสดงตัวเลือกการตั้งค่า **วิธีการจัดส่ง** **วิธีการชำระเงิน** และ **การกำหนดกลุ่มการเติมสินค้า** บนแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="7344a-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![การดำเนินการตั้งค่าช่องทางออนไลน์เพิ่มเติม](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="7344a-140">การตั้งค่าวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7344a-140">Set up payment methods</span></span>

<span data-ttu-id="7344a-141">เมื่อต้องการตั้งค่าวิธีการชำระเงิน สำหรับชนิดการชำระเงินแต่ละชนิดที่สนับสนุนบนช่องทางนี้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7344a-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="7344a-142">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** จากนั้นเลือก **วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="7344a-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="7344a-143">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7344a-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7344a-144">ในบานหน้าต่างนำทาง ให้เลือกวิธีการชำระเงินที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7344a-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="7344a-145">ในส่วน **ทั่วไป** ให้ระบุ **ชื่อการดำเนินงาน** และตั้งค่าคอนฟิกการตั้งค่าที่ต้องการอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="7344a-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="7344a-146">ตั้งค่าคอนฟิกการตั้งค่าเพิ่มเติมใด ๆ ตามต้องการสำหรับชนิดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7344a-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="7344a-147">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7344a-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7344a-148">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการชำระเงินสด</span><span class="sxs-lookup"><span data-stu-id="7344a-148">The following image shows an example of a cash payment method.</span></span>

![ตัวอย่างวิธีการชำระเงิน](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="7344a-150">ตั้งค่าวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7344a-150">Set up modes of delivery</span></span>

<span data-ttu-id="7344a-151">คุณสามารถดูวิธีการจัดส่งที่ตั้งค่าคอนฟิกได้โดยการเลือก **วิธีการจัดส่ง** จากแท็บ **การตั้งค่า** ใน **บานหน้าต่างการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="7344a-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="7344a-152">เมื่อต้องการเปลี่ยนหรือเพิ่มวิธีการจัดส่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7344a-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="7344a-153">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การบริหารสินค้าคงคลัง \> วิธีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="7344a-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="7344a-154">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างวิธีการจัดส่งใหม่ หรือเลือกโหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="7344a-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="7344a-155">ในส่วน **ช่องทางการขายปลีก** ให้เลือก **เพิ่มบรรทัด** เพื่อเพิ่มช่องทาง</span><span class="sxs-lookup"><span data-stu-id="7344a-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="7344a-156">การเพิ่มช่องทางโดยใช้โหนดขององค์กรแทนที่การเพิ่มช่องทางแต่ละช่องสามารถเพิ่มประสิทธิภาพการเพิ่มช่อง</span><span class="sxs-lookup"><span data-stu-id="7344a-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="7344a-157">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7344a-157">The following image shows an example of a mode of delivery.</span></span>

![ตั้งค่าวิธีการจัดส่ง](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="7344a-159">ตั้งค่าการกำหนดกลุ่มการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="7344a-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="7344a-160">ในการตั้งค่าการกำหนดกลุ่มการเติมสินค้า ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7344a-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="7344a-161">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** จากนั้นเลือก **การกำหนดกลุ่มการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="7344a-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="7344a-162">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7344a-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7344a-163">ในรายการแบบหล่นลง **กลุ่มการเติมสินค้า** ให้เลือกกลุ่มการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="7344a-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="7344a-164">ในรายการแบบหล่นลง **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7344a-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="7344a-165">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7344a-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7344a-166">รูปภาพต่อไปนี้แสดงตัวอย่างของการตั้งค่าการกำหนดกลุ่มการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="7344a-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![ตั้งค่าการกำหนดกลุ่มการเติมสินค้า](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="7344a-168">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7344a-168">Additional resources</span></span>

[<span data-ttu-id="7344a-169">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="7344a-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7344a-170">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="7344a-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7344a-171">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="7344a-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="7344a-172">ตั้งค่าช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="7344a-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="7344a-173">ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen</span><span class="sxs-lookup"><span data-stu-id="7344a-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]