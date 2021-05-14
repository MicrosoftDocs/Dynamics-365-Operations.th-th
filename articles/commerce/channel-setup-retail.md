---
title: ตั้งค่าช่องทางการขายปลีก
description: หัวข้อนี้จะอธิบายวิธีการสร้างช่องทางการขายปลีกใหม่ใน Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 04/23/2021
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
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937545"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="dac4e-103">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="dac4e-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dac4e-104">หัวข้อนี้จะอธิบายวิธีการสร้างช่องทางการขายปลีกใหม่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dac4e-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dac4e-105">Dynamics 365 Commerce รองรับช่องทางการขายปลีกที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="dac4e-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="dac4e-106">ช่องทางการขายปลีกเหล่านี้รวมร้านค้าออนไลน์ ศูนย์บริการ และร้านค้าปลีก (เรียกอีกอย่างหนึ่งว่า ร้านค้าที่ให้บริการจริง)</span><span class="sxs-lookup"><span data-stu-id="dac4e-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="dac4e-107">ช่องทางของร้านค้าปลีกแต่ละช่องสามารถมีวิธีการชำระเงินของตัวเอง กลุ่มราคา การลงทะเบียนรวมระบบขายหน้าร้าน (POS) บัญชีรายได้ และบัญชีรายจ่าย และพนักงาน</span><span class="sxs-lookup"><span data-stu-id="dac4e-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="dac4e-108">คุณต้องตั้งค่าองค์ประกอบเหล่านี้ทั้งหมดก่อนคุณจึงจะสามารถสร้างช่องทางร้านค้าปลีกได้</span><span class="sxs-lookup"><span data-stu-id="dac4e-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="dac4e-109">ก่อนที่จะมีการสร้างช่องทางการขายปลีก ตรวจสอบให้แน่ใจว่าคุณได้ปฏิบัติตาม [ข้อกำหนดเบื้องต้นของช่องทาง](channels-prerequisites.md)</span><span class="sxs-lookup"><span data-stu-id="dac4e-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="dac4e-110">สร้างและกำหนดค่าของช่องทางการขายปลีกใหม่</span><span class="sxs-lookup"><span data-stu-id="dac4e-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="dac4e-111">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> ช่องทาง \> ร้านค้า \> ร้านค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="dac4e-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="dac4e-112">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="dac4e-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dac4e-113">ในฟิลด์ **ชื่อ** ให้ระบุชื่อสำหรับช่องทางใหม่</span><span class="sxs-lookup"><span data-stu-id="dac4e-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="dac4e-114">ในฟิลด์ **หมายเลขร้านค้า** ให้ระบุหมายเลขร้านค้าที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="dac4e-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="dac4e-115">หมายเลขสามารถเป็นอักขระตัวอักษรและตัวเลขสูงสุดไม่เกิน 10 ตัว</span><span class="sxs-lookup"><span data-stu-id="dac4e-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="dac4e-116">ในรายการแบบหล่นลงของ **นิติบุคคล** ให้ป้อนนิติบุคคลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="dac4e-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="dac4e-117">ในรายการแบบหล่นลงของ **คลังสินค้า** ให้ป้อนคลังสินค้าที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="dac4e-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="dac4e-118">ในฟิลด์ **โซนเวลาร้านค้า** ให้เลือกโซนเวลาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="dac4e-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="dac4e-119">ในรายการแบบหล่นลงของ **กลุ่มภาษีขาย** ให้เลือกกลุ่มภาษีขายที่เหมาะสมสำหรับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="dac4e-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="dac4e-120">ในฟิลด์ **สกุลเงิน** ให้เลือกสกุลเงินที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="dac4e-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="dac4e-121">ในฟิลด์ **สมุดที่อยู่ของลูกค้า** ให้ระบุสมุดที่อยู่ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="dac4e-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="dac4e-122">ในฟิลด์ **ลูกค้าเริ่มต้น** ให้ระบุลูกค้าเริ่มต้นที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="dac4e-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="dac4e-123">ในฟิลด์ **โปรไฟล์ฟังก์ชัน** ให้เลือกโปรไฟล์ฟังก์ชันถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="dac4e-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="dac4e-124">ในฟิลด์ **โปรไฟล์การแจ้งเตือนทางอีเมล** ให้ระบุโปรไฟล์การแจ้งเตือนทางอีเมลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="dac4e-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="dac4e-125">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dac4e-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="dac4e-126">รูปภาพต่อไปนี้แสดงการสร้างช่องทางการขายปลีกใหม่</span><span class="sxs-lookup"><span data-stu-id="dac4e-126">The following image shows the creation of a new retail channel.</span></span>

![ช่องทางการขายปลีกใหม่](media/channel-setup-retail-1.png)

<span data-ttu-id="dac4e-128">รูปภาพต่อไปนี้แสดงตัวอย่างของช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="dac4e-128">The following image shows an example retail channel.</span></span>

![ตัวอย่างของช่องทางการขายปลีก](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="dac4e-130">การตั้งค่าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="dac4e-130">Other settings</span></span>

<span data-ttu-id="dac4e-131">มีการตั้งค่าที่เลือกกำหนดได้มากมายซึ่งสามารถตั้งค่าได้ในส่วน **ใบแจ้งยอด/การปิดบัญชี** และ **เบ็ดเตล็ด** ตามความต้องการของร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="dac4e-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="dac4e-132">นอกจากนี้ โปรดดู [โครงร่างหน้าจอสำหรับการขายหน้าร้าน (POS)](pos-screen-layouts.md) สำหรับข้อมูลเกี่ยวกับการตั้งค่าโครงร่างหน้าจอเริ่มต้นในส่วน **โครงร่างหน้าจอ** และ [ตั้งค่าคอนฟิกและติดตั้งสถานีฮาร์ดแวร์ของ Retail](retail-hardware-station-configuration-installation.md) สำหรับข้อมูลการตั้งค่าเกี่ยวกับส่วนของ **สถานีฮาร์ดแวร์**</span><span class="sxs-lookup"><span data-stu-id="dac4e-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="dac4e-133">รูปภาพต่อไปนี้แสดงตัวอย่างของการตั้งค่าคอนฟิกของการตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="dac4e-133">The following image shows an example retail channel setup configuration.</span></span>

![ตัวอย่างของการตั้งค่าคอนฟิกช่องทางการขายปลีก](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="dac4e-135">การตั้งค่าช่องทางเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="dac4e-135">Additional channel set up</span></span>

<span data-ttu-id="dac4e-136">มีรายการเพิ่มเติมที่จำเป็นต้องมีการตั้งค่าสำหรับช่องทางที่สามารถพบได้ในบานหน้าต่างการดำเนินการ ที่อยู่ภายใต้ส่วน **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="dac4e-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="dac4e-137">งานเพิ่มเติมที่จำเป็นสำหรับการตั้งค่าช่องทางออนไลน์ รวมถึงการตั้งค่าวิธีการชำระเงิน การตรวจนับเงินสด วิธีการจัดส่ง บัญชีรายได้/ค่าใช้จ่าย ส่วน การกำหนดกลุ่มการเติมสินค้าและตู้นิรภัย</span><span class="sxs-lookup"><span data-stu-id="dac4e-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="dac4e-138">รูปภาพต่อไปนี้จะแสดงตัวเลือกการตั้งค่าช่องทางการขายปลีกเพิ่มเติมต่าง ๆ บนแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="dac4e-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![ตั้งค่าช่องทาง](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="dac4e-140">การตั้งค่าวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="dac4e-140">Set up payment methods</span></span>

<span data-ttu-id="dac4e-141">เมื่อต้องการตั้งค่าวิธีการชำระเงิน สำหรับชนิดการชำระเงินแต่ละชนิดที่สนับสนุนบนช่องทางนี้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="dac4e-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="dac4e-142">ในบานหน้าต่างการดำเนินการ ให้เลือก แท็บ **การตั้งค่า** จากนั้นเลือก **วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="dac4e-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="dac4e-143">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="dac4e-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dac4e-144">ในบานหน้าต่างนำทาง ให้เลือกวิธีการชำระเงินที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="dac4e-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="dac4e-145">ในส่วน **ทั่วไป** ให้ระบุ **ชื่อการดำเนินงาน** และตั้งค่าคอนฟิกการตั้งค่าที่ต้องการอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="dac4e-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="dac4e-146">ตั้งค่าคอนฟิกการตั้งค่าเพิ่มเติมใด ๆ ตามต้องการสำหรับชนิดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="dac4e-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="dac4e-147">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dac4e-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="dac4e-148">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการชำระเงินสด</span><span class="sxs-lookup"><span data-stu-id="dac4e-148">The following image shows an example of a cash payment method.</span></span>

![วิธีการชำระเงินตัวอย่าง](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="dac4e-150">ตั้งค่าการตรวจนับเงินสด</span><span class="sxs-lookup"><span data-stu-id="dac4e-150">Set up cash declaration</span></span>

1. <span data-ttu-id="dac4e-151">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และจากนั้นเลือก **การตรวจนับเงินสด**</span><span class="sxs-lookup"><span data-stu-id="dac4e-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="dac4e-152">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** และจากนั้นสร้างหน่วยเงินของ **เหรียญ** และ **ธนบัตร** ทั้งหมด ที่สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="dac4e-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="dac4e-153">รูปภาพต่อไปนี้แสดงตัวอย่างของการตรวจนับเงินสด</span><span class="sxs-lookup"><span data-stu-id="dac4e-153">The following image shows an example of a cash declaration.</span></span>

![ตั้งค่าการตรวจนับเงินสด](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="dac4e-155">ตั้งค่าวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="dac4e-155">Set up modes of delivery</span></span>

<span data-ttu-id="dac4e-156">คุณสามารถดูวิธีการจัดส่งที่ตั้งค่าคอนฟิกได้โดยการเลือก **วิธีการจัดส่ง** จากแท็บ **การตั้งค่า** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="dac4e-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="dac4e-157">เมื่อต้องการเปลี่ยนหรือเพิ่มวิธีการจัดส่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="dac4e-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="dac4e-158">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การบริหารสินค้าคงคลัง \> วิธีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="dac4e-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="dac4e-159">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างวิธีการจัดส่งใหม่ หรือเลือกโหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="dac4e-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="dac4e-160">ในส่วน **ช่องทางการขายปลีก** ให้เลือก **เพิ่มบรรทัด** เพื่อเพิ่มช่องทาง</span><span class="sxs-lookup"><span data-stu-id="dac4e-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="dac4e-161">การเพิ่มช่องทางโดยใช้โหนดขององค์กรแทนที่การเพิ่มช่องทางแต่ละช่องสามารถเพิ่มประสิทธิภาพการเพิ่มช่อง</span><span class="sxs-lookup"><span data-stu-id="dac4e-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="dac4e-162">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="dac4e-162">The following image shows an example of a mode of delivery.</span></span>

![ตั้งค่าวิธีการจัดส่ง](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="dac4e-164">ตั้งค่าบัญชีรายได้/ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="dac4e-164">Set up income/expense account</span></span>

<span data-ttu-id="dac4e-165">ถ้าต้องการตั้งค่าบัญชีรายได้/ค่าใช้จ่าย ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="dac4e-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="dac4e-166">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และจากนั้นเลือก **บัญชีรายได้/ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="dac4e-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="dac4e-167">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="dac4e-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dac4e-168">ภายใต้ **ชื่อ** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="dac4e-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="dac4e-169">ภายใต้ **ชื่อสำหรับค้นหา** ให้ป้อนชื่อสำหรับค้นหา</span><span class="sxs-lookup"><span data-stu-id="dac4e-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="dac4e-170">ภายใต้ **ชนิดบัญชี** ให้ป้อนชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="dac4e-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="dac4e-171">ป้อนข้อความสำหรับ **รายการข้อความ 1** **รายการข้อความ 2** **ข้อความในสลิป 1** และ **ข้อความในสลิป 2** ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="dac4e-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="dac4e-172">ภายใตเ **การลงรายการบัญชี** ให้ป้อนข้อมูลการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="dac4e-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="dac4e-173">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dac4e-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="dac4e-174">รูปภาพต่อไปนี้แสดงตัวอย่างของบัญชีรายได้/ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="dac4e-174">The following image shows an example of an income/expense account.</span></span>

![ตั้งค่าบัญชีรายได้/ค่าใช้จ่าย](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="dac4e-176">ตั้งค่าส่วน</span><span class="sxs-lookup"><span data-stu-id="dac4e-176">Set up sections</span></span>

<span data-ttu-id="dac4e-177">หากต้องการตั้งค่าส่วน ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="dac4e-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="dac4e-178">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และคลิก **ส่วน**</span><span class="sxs-lookup"><span data-stu-id="dac4e-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="dac4e-179">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="dac4e-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dac4e-180">ภายใต้ **หมายเลขส่วน** ให้ป้อนหมายเลขส่วน</span><span class="sxs-lookup"><span data-stu-id="dac4e-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="dac4e-181">ภายใต้ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="dac4e-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="dac4e-182">ภายใต้ **ขนาดส่วน** ให้ป้อนขนาดส่วน</span><span class="sxs-lookup"><span data-stu-id="dac4e-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="dac4e-183">ตั้งค่าคอนฟิกการตั้งค่าเพิ่มเติมสำหรับ **ทั่วไป** และ **สถิติการขาย** ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="dac4e-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="dac4e-184">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dac4e-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="dac4e-185">ตั้งค่าการกำหนดกลุ่มการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="dac4e-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="dac4e-186">ในการตั้งค่าการกำหนดกลุ่มการเติมสินค้า ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="dac4e-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="dac4e-187">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** จากนั้นเลือก **การกำหนดกลุ่มการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="dac4e-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="dac4e-188">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="dac4e-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dac4e-189">ในรายการแบบหล่นลง **กลุ่มการเติมสินค้า** ให้เลือกกลุ่มการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="dac4e-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="dac4e-190">ในรายการแบบหล่นลง **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="dac4e-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="dac4e-191">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dac4e-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="dac4e-192">รูปภาพต่อไปนี้แสดงตัวอย่างของการตั้งค่าการกำหนดกลุ่มการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="dac4e-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![ตั้งค่าการกำหนดกลุ่มการเติมสินค้า](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="dac4e-194">ตั้งค่าตู้นิรภัย</span><span class="sxs-lookup"><span data-stu-id="dac4e-194">Set up safes</span></span>

<span data-ttu-id="dac4e-195">หากต้องการตั้งค่าตู้นิรภัย ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="dac4e-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="dac4e-196">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และคลิก **ตู้นิรภัย**</span><span class="sxs-lookup"><span data-stu-id="dac4e-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="dac4e-197">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="dac4e-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dac4e-198">ป้อนชื่อสำหรับตู้นิรภัย</span><span class="sxs-lookup"><span data-stu-id="dac4e-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="dac4e-199">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dac4e-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="dac4e-200">ตรวจสอบว่ารหัสธุรกรรมเฉพาะให้ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="dac4e-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="dac4e-201">Commerce เวอร์ชัน 10.0.18 รหัสธุรกรรมที่สร้างขึ้นสำหรับการขายหน้าร้าน (POS) เป็นลำดับ และรวมส่วนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="dac4e-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="dac4e-202">ส่วนที่คงที่ ซึ่งเป็นการเรียงต่อกันของรหัสร้านค้า และรหัสเทอร์มินัล</span><span class="sxs-lookup"><span data-stu-id="dac4e-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="dac4e-203">ส่วนตามลำดับ ซึ่งเป็นลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="dac4e-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="dac4e-204">โดยเฉพาะ รูปแบบคือ *{store}-{terminal}-{numbersequence}*</span><span class="sxs-lookup"><span data-stu-id="dac4e-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="dac4e-205">เนื่องจากรหัสธุรกรรมสามารถสร้างขึ้นในโหมดออฟไลน์และโหมดออนไลน์ จึงมีอินสแตนซ์ของรหัสธุรกรรมที่คัดลอกมาซึ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="dac4e-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="dac4e-206">การตัดรหัสธุรกรรมที่ซ้อนกันออกต้องมีการแก้ไขข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="dac4e-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="dac4e-207">ด้วย Commerce เวอร์ชัน 10.0.19 รูปแบบรหัสธุรกรรมจะได้รับการอัพเดตเพื่อลบส่วนตามลดับแล้ว และใช้หมายเลข 13 หลักที่สร้างโดยการคํานวณเวลาในหน่วยมิลลิวินาทีตั้งแต่ 1970 แทน</span><span class="sxs-lookup"><span data-stu-id="dac4e-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="dac4e-208">ด้วยการเปลี่ยนแปลงนี้ รูปแบบรหัสธุรกรรมใหม่คือ *{store}-{terminal}-{millisecondsSince1970}*</span><span class="sxs-lookup"><span data-stu-id="dac4e-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="dac4e-209">การอัปเดตนี้ช่วยให้รหัสธุรกรรมเป็นรหัสที่ไม่ต่อเนื่องกัน และตรวจสอบให้แน่ใจว่ารหัสธุรกรรมมีเอกลักษณ์เฉพาะเสมอ</span><span class="sxs-lookup"><span data-stu-id="dac4e-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="dac4e-210">รหัสธุรกรรมจะใช้เพื่อระบบภายในเท่านั้น ดังนั้น รหัสธุรกรรมจึงไม่ควรจะต่อเนื่องกัน</span><span class="sxs-lookup"><span data-stu-id="dac4e-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="dac4e-211">อย่างไรก็ตาม ในหลายประเทศกำหนดให้รหัสใบเสร็จต้องเป็นตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="dac4e-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="dac4e-212">คุณสามารถเปิดใช้งานคุณลักษณะรูปแบบรหัสธุรกรรมใหม่ได้จากพื้นที่ทำงาน **การจัดการคุณลักษณะ** ได้</span><span class="sxs-lookup"><span data-stu-id="dac4e-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="dac4e-213">เมื่อต้องการเปิดใช้งานการใช้รหัสธุรกรรมใหม่ ให้ปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="dac4e-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="dac4e-214">ในศูนย์ควบคุม Commerce ไปที่ **การจัดการระบบ \> พื้นที่ทำงาน \> การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="dac4e-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="dac4e-215">ตัวกรองสำหรับโมดูล "Retail และ Commerce"</span><span class="sxs-lookup"><span data-stu-id="dac4e-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="dac4e-216">ค้นหาชื่อคุณลักษระ **เปิดใช้งานรหัสธุรกรรมใหม่ เพื่อหลีกเลี่ยงรหัสธุรกรรมที่ซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="dac4e-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="dac4e-217">เลือกคุณลักษณะ และจากนั้น เลือก **เปิดใช้งานตอนนี้** ในบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="dac4e-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="dac4e-218">ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="dac4e-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="dac4e-219">รันงาน **การตั้งค่าคอนฟิก 1070 Channel** และ **ตัวบันทึกงาน 1170 POS** เพื่อซิงโครไนส์คุณลักษณะที่เปิดใช้งานไปยังร้านค้า</span><span class="sxs-lookup"><span data-stu-id="dac4e-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="dac4e-220">หลังจากที่ส่งการเปลี่ยนแปลงไปยังร้านค้าแล้ว ต้องปิดและเปิดเทอร์มินัล POS อีกครั้ง เพื่อใช้รูปแบบรหัสธุรกรรมใหม่</span><span class="sxs-lookup"><span data-stu-id="dac4e-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="dac4e-221">หลังจากที่เปิดใช้งานคุณลักษณะรูปแบบรหัสธุรกรรมใหม่แล้ว คุณจะไม่สามารถปิดใช้งานคุณลักษณะนี้ได้</span><span class="sxs-lookup"><span data-stu-id="dac4e-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="dac4e-222">ถ้าต้องปิดใช้งาน โปรดติดต่อ Commerce Suppor</span><span class="sxs-lookup"><span data-stu-id="dac4e-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dac4e-223">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="dac4e-223">Additional resources</span></span>

[<span data-ttu-id="dac4e-224">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="dac4e-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="dac4e-225">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="dac4e-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="dac4e-226">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="dac4e-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="dac4e-227">ตั้งค่าช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="dac4e-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
