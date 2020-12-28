---
title: ตั้งค่าช่องทางการขายปลีก
description: หัวข้อนี้จะอธิบายวิธีการสร้างช่องทางการขายปลีกใหม่ใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: a9291dddf7d4dc080b6eb1ec60702de32a761f45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416091"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="31557-103">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="31557-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="31557-104">หัวข้อนี้จะอธิบายวิธีการสร้างช่องทางการขายปลีกใหม่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="31557-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="31557-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="31557-105">Overview</span></span>

<span data-ttu-id="31557-106">Dynamics 365 Commerce รองรับช่องทางการขายปลีกที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="31557-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="31557-107">ช่องทางการขายปลีกเหล่านี้รวมร้านค้าออนไลน์ ศูนย์บริการ และร้านค้าปลีก (เรียกอีกอย่างหนึ่งว่า ร้านค้าที่ให้บริการจริง)</span><span class="sxs-lookup"><span data-stu-id="31557-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="31557-108">ช่องทางของร้านค้าปลีกแต่ละช่องสามารถมีวิธีการชำระเงินของตัวเอง กลุ่มราคา การลงทะเบียนรวมระบบขายหน้าร้าน (POS) บัญชีรายได้ และบัญชีรายจ่าย และพนักงาน</span><span class="sxs-lookup"><span data-stu-id="31557-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="31557-109">คุณต้องตั้งค่าองค์ประกอบเหล่านี้ทั้งหมดก่อนคุณจึงจะสามารถสร้างช่องทางร้านค้าปลีกได้</span><span class="sxs-lookup"><span data-stu-id="31557-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="31557-110">ก่อนที่จะมีการสร้างช่องทางการขายปลีก ตรวจสอบให้แน่ใจว่าคุณได้ปฏิบัติตาม [ข้อกำหนดเบื้องต้นของช่องทาง](channels-prerequisites.md)</span><span class="sxs-lookup"><span data-stu-id="31557-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="31557-111">สร้างและกำหนดค่าของช่องทางการขายปลีกใหม่</span><span class="sxs-lookup"><span data-stu-id="31557-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="31557-112">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> ช่องทาง \> ร้านค้า \> ร้านค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="31557-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="31557-113">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="31557-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="31557-114">ในฟิลด์ **ชื่อ** ให้ระบุชื่อสำหรับช่องทางใหม่</span><span class="sxs-lookup"><span data-stu-id="31557-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="31557-115">ในฟิลด์ **หมายเลขร้านค้า** ให้ระบุหมายเลขร้านค้าที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="31557-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="31557-116">หมายเลขสามารถเป็นอักขระตัวอักษรและตัวเลขสูงสุดไม่เกิน 10 ตัว</span><span class="sxs-lookup"><span data-stu-id="31557-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="31557-117">ในรายการแบบหล่นลงของ **นิติบุคคล** ให้ป้อนนิติบุคคลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="31557-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="31557-118">ในรายการแบบหล่นลงของ **คลังสินค้า** ให้ป้อนคลังสินค้าที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="31557-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="31557-119">ในฟิลด์ **โซนเวลาร้านค้า** ให้เลือกโซนเวลาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="31557-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="31557-120">ในรายการแบบหล่นลงของ **กลุ่มภาษีขาย** ให้เลือกกลุ่มภาษีขายที่เหมาะสมสำหรับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="31557-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="31557-121">ในฟิลด์ **สกุลเงิน** ให้เลือกสกุลเงินที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="31557-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="31557-122">ในฟิลด์ **สมุดที่อยู่ของลูกค้า** ให้ระบุสมุดที่อยู่ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="31557-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="31557-123">ในฟิลด์ **ลูกค้าเริ่มต้น** ให้ระบุลูกค้าเริ่มต้นที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="31557-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="31557-124">ในฟิลด์ **โปรไฟล์ฟังก์ชัน** ให้เลือกโปรไฟล์ฟังก์ชันถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="31557-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="31557-125">ในฟิลด์ **โปรไฟล์การแจ้งเตือนทางอีเมล** ให้ระบุโปรไฟล์การแจ้งเตือนทางอีเมลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="31557-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="31557-126">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="31557-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="31557-127">รูปภาพต่อไปนี้แสดงการสร้างช่องทางการขายปลีกใหม่</span><span class="sxs-lookup"><span data-stu-id="31557-127">The following image shows the creation of a new retail channel.</span></span>

![ช่องทางการขายปลีกใหม่](media/channel-setup-retail-1.png)

<span data-ttu-id="31557-129">รูปภาพต่อไปนี้แสดงตัวอย่างของช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="31557-129">The following image shows an example retail channel.</span></span>

![ตัวอย่างของช่องทางการขายปลีก](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="31557-131">การตั้งค่าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="31557-131">Other settings</span></span>

<span data-ttu-id="31557-132">มีการตั้งค่าที่เลือกกำหนดได้มากมายซึ่งสามารถตั้งค่าได้ในส่วน **ใบแจ้งยอด/การปิดบัญชี** และ **เบ็ดเตล็ด** ตามความต้องการของร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="31557-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="31557-133">นอกจากนี้ โปรดดู [โครงร่างหน้าจอสำหรับการขายหน้าร้าน (POS)](pos-screen-layouts.md) สำหรับข้อมูลเกี่ยวกับการตั้งค่าโครงร่างหน้าจอเริ่มต้นในส่วน **โครงร่างหน้าจอ** และ [ตั้งค่าคอนฟิกและติดตั้งสถานีฮาร์ดแวร์ของ Retail](retail-hardware-station-configuration-installation.md) สำหรับข้อมูลการตั้งค่าเกี่ยวกับส่วนของ **สถานีฮาร์ดแวร์**</span><span class="sxs-lookup"><span data-stu-id="31557-133">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="31557-134">รูปภาพต่อไปนี้แสดงตัวอย่างของการตั้งค่าคอนฟิกของการตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="31557-134">The following image shows an example retail channel setup configuration.</span></span>

![ตัวอย่างของการตั้งค่าคอนฟิกช่องทางการขายปลีก](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="31557-136">การตั้งค่าช่องทางเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="31557-136">Additional channel set up</span></span>

<span data-ttu-id="31557-137">มีรายการเพิ่มเติมที่จำเป็นต้องมีการตั้งค่าสำหรับช่องทางที่สามารถพบได้ใน **บานหน้าต่างการดำเนินการ** ที่อยู่ภายใต้ส่วน **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="31557-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="31557-138">งานเพิ่มเติมที่จำเป็นสำหรับการตั้งค่าช่องทางออนไลน์ รวมถึงการตั้งค่าวิธีการชำระเงิน การตรวจนับเงินสด วิธีการจัดส่ง บัญชีรายได้/ค่าใช้จ่าย ส่วน การกำหนดกลุ่มการเติมสินค้าและตู้นิรภัย</span><span class="sxs-lookup"><span data-stu-id="31557-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="31557-139">รูปภาพต่อไปนี้จะแสดงตัวเลือกการตั้งค่าช่องทางการขายปลีกเพิ่มเติมต่าง ๆ บนแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="31557-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![ตั้งค่าช่องทาง](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="31557-141">การตั้งค่าวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="31557-141">Set up payment methods</span></span>

<span data-ttu-id="31557-142">เมื่อต้องการตั้งค่าวิธีการชำระเงิน สำหรับชนิดการชำระเงินแต่ละชนิดที่สนับสนุนบนช่องทางนี้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="31557-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="31557-143">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** จากนั้นเลือก **วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="31557-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="31557-144">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="31557-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="31557-145">ในบานหน้าต่างนำทาง ให้เลือกวิธีการชำระเงินที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="31557-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="31557-146">ในส่วน **ทั่วไป** ให้ระบุ **ชื่อการดำเนินงาน** และตั้งค่าคอนฟิกการตั้งค่าที่ต้องการอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="31557-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="31557-147">ตั้งค่าคอนฟิกการตั้งค่าเพิ่มเติมใด ๆ ตามต้องการสำหรับชนิดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="31557-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="31557-148">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="31557-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="31557-149">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการชำระเงินสด</span><span class="sxs-lookup"><span data-stu-id="31557-149">The following image shows an example of a cash payment method.</span></span>

![วิธีการชำระเงินตัวอย่าง](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="31557-151">ตั้งค่าการตรวจนับเงินสด</span><span class="sxs-lookup"><span data-stu-id="31557-151">Set up cash declaration</span></span>

1. <span data-ttu-id="31557-152">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และจากนั้นเลือก **การตรวจนับเงินสด**</span><span class="sxs-lookup"><span data-stu-id="31557-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="31557-153">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** และจากนั้นสร้างหน่วยเงินของ **เหรียญ** และ **ธนบัตร** ทั้งหมดที่สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="31557-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="31557-154">รูปภาพต่อไปนี้แสดงตัวอย่างของการตรวจนับเงินสด</span><span class="sxs-lookup"><span data-stu-id="31557-154">The following image shows an example of a cash declaration.</span></span>

![ตั้งค่าการตรวจนับเงินสด](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="31557-156">ตั้งค่าวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="31557-156">Set up modes of delivery</span></span>

<span data-ttu-id="31557-157">คุณสามารถดูวิธีการจัดส่งที่ตั้งค่าคอนฟิกได้โดยการเลือก **วิธีการจัดส่ง** จากแท็บ **การตั้งค่า** ใน **บานหน้าต่างการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="31557-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="31557-158">เมื่อต้องการเปลี่ยนหรือเพิ่มวิธีการจัดส่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="31557-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="31557-159">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การบริหารสินค้าคงคลัง \> วิธีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="31557-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="31557-160">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างวิธีการจัดส่งใหม่ หรือเลือกโหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="31557-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="31557-161">ในส่วน **ช่องทางการขายปลีก** ให้เลือก **เพิ่มบรรทัด** เพื่อเพิ่มช่องทาง</span><span class="sxs-lookup"><span data-stu-id="31557-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="31557-162">การเพิ่มช่องทางโดยใช้โหนดขององค์กรแทนที่การเพิ่มช่องทางแต่ละช่องสามารถเพิ่มประสิทธิภาพการเพิ่มช่อง</span><span class="sxs-lookup"><span data-stu-id="31557-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="31557-163">รูปภาพต่อไปนี้แสดงตัวอย่างของวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="31557-163">The following image shows an example of a mode of delivery.</span></span>

![ตั้งค่าวิธีการจัดส่ง](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="31557-165">ตั้งค่าบัญชีรายได้/ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="31557-165">Set up income/expense account</span></span>

<span data-ttu-id="31557-166">ถ้าต้องการตั้งค่าบัญชีรายได้/ค่าใช้จ่าย ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="31557-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="31557-167">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และจากนั้นเลือก **บัญชีรายได้/ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="31557-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="31557-168">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="31557-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="31557-169">ภายใต้ **ชื่อ** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="31557-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="31557-170">ภายใต้ **ชื่อสำหรับค้นหา** ให้ป้อนชื่อสำหรับค้นหา</span><span class="sxs-lookup"><span data-stu-id="31557-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="31557-171">ภายใต้ **ชนิดบัญชี** ให้ป้อนชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="31557-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="31557-172">ป้อนข้อความสำหรับ **รายการข้อความ 1** **รายการข้อความ 2** **ข้อความในสลิป 1** และ **ข้อความในสลิป 2** ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="31557-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="31557-173">ภายใตเ **การลงรายการบัญชี** ให้ป้อนข้อมูลการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="31557-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="31557-174">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="31557-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="31557-175">รูปภาพต่อไปนี้แสดงตัวอย่างของบัญชีรายได้/ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="31557-175">The following image shows an example of an income/expense account.</span></span>

![ตั้งค่าบัญชีรายได้/ค่าใช้จ่าย](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="31557-177">ตั้งค่าส่วน</span><span class="sxs-lookup"><span data-stu-id="31557-177">Set up sections</span></span>

<span data-ttu-id="31557-178">หากต้องการตั้งค่าส่วน ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="31557-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="31557-179">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และคลิก **ส่วน**</span><span class="sxs-lookup"><span data-stu-id="31557-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="31557-180">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="31557-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="31557-181">ภายใต้ **หมายเลขส่วน** ให้ป้อนหมายเลขส่วน</span><span class="sxs-lookup"><span data-stu-id="31557-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="31557-182">ภายใต้ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="31557-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="31557-183">ภายใต้ **ขนาดส่วน** ให้ป้อนขนาดส่วน</span><span class="sxs-lookup"><span data-stu-id="31557-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="31557-184">ตั้งค่าคอนฟิกการตั้งค่าเพิ่มเติมสำหรับ **ทั่วไป** และ **สถิติการขาย** ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="31557-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="31557-185">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="31557-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="31557-186">ตั้งค่าการกำหนดกลุ่มการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="31557-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="31557-187">ในการตั้งค่าการกำหนดกลุ่มการเติมสินค้า ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="31557-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="31557-188">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** จากนั้นเลือก **การกำหนดกลุ่มการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="31557-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="31557-189">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="31557-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="31557-190">ในรายการแบบหล่นลง **กลุ่มการเติมสินค้า** ให้เลือกกลุ่มการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="31557-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="31557-191">ในรายการแบบหล่นลง **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="31557-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="31557-192">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="31557-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="31557-193">รูปภาพต่อไปนี้แสดงตัวอย่างของการตั้งค่าการกำหนดกลุ่มการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="31557-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![ตั้งค่าการกำหนดกลุ่มการเติมสินค้า](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="31557-195">ตั้งค่าตู้นิรภัย</span><span class="sxs-lookup"><span data-stu-id="31557-195">Set up safes</span></span>

<span data-ttu-id="31557-196">หากต้องการตั้งค่าตู้นิรภัย ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="31557-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="31557-197">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และคลิก **ตู้นิรภัย**</span><span class="sxs-lookup"><span data-stu-id="31557-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="31557-198">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="31557-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="31557-199">ป้อนชื่อสำหรับตู้นิรภัย</span><span class="sxs-lookup"><span data-stu-id="31557-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="31557-200">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="31557-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31557-201">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="31557-201">Additional resources</span></span>

[<span data-ttu-id="31557-202">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="31557-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="31557-203">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="31557-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="31557-204">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="31557-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="31557-205">ตั้งค่าช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="31557-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)

