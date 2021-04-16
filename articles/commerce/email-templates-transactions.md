---
title: สร้างเท็มเพลตอีเมลสำหรับเหตุการณ์ของธุรกรรม
description: หัวข้อนี้จะอธิบายวิธีการสร้าง อัปโหลด และกำหนดค่าเท็มเพลตอีเมลสำหรับเหตุการณ์ทางธุรกรรมใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 55597e83a930fc7d8bcc4c0cf09abc82cb666b25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792642"
---
# <a name="create-email-templates-for-transactional-events"></a><span data-ttu-id="57f64-103">สร้างเท็มเพลตอีเมลสำหรับเหตุการณ์ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="57f64-103">Create email templates for transactional events</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57f64-104">หัวข้อนี้จะอธิบายวิธีการสร้าง อัปโหลด และกำหนดค่าเท็มเพลตอีเมลสำหรับเหตุการณ์ทางธุรกรรมใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="57f64-104">This topic describes how to create, upload, and configure email templates for transactional events in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="57f64-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="57f64-105">Overview</span></span>

<span data-ttu-id="57f64-106">Dynamics 365 Commerce มีโซลูชันสำเร็จรูปสำหรับการส่งอีเมลที่แจ้งเตือนลูกค้าเกี่ยวกับเหตุการณ์ของธุรกรรม (ตัวอย่างเช่น เมื่อทำการสั่งซื้อ การสั่งซื้อจะพร้อมสำหรับการเบิกสินค้า หรือการจัดส่งสินค้าตามใบสั่ง)</span><span class="sxs-lookup"><span data-stu-id="57f64-106">Dynamics 365 Commerce provides an out-of-box solution for sending emails that alert customers about transactional events (for example, when an order is placed, an order is ready for pickup, or an order has been shipped).</span></span> <span data-ttu-id="57f64-107">หัวข้อนี้จะอธิบายขั้นตอนสำหรับการสร้าง อัปโหลด และกำหนดค่าเท็มเพลตอีเมลที่ใช้ในการส่งอีเมลของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="57f64-107">This topic describes the steps for creating, uploading, and configuring the email templates that are used to send transactional emails.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="57f64-108">สร้างเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-108">Create an email template</span></span>

<span data-ttu-id="57f64-109">ก่อนที่คุณจะสามารถแม็ปเหตุการณ์ของธุรกรรมเฉพาะกับเท็มเพลตอีเมลได้ คุณต้องสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="57f64-109">Before you can map a specific transactional event to an email template, you must create the template.</span></span>

<span data-ttu-id="57f64-110">ทำตามขั้นตอนเหล่านี้เพื่อสร้างแม่แบบอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-110">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="57f64-111">ในศูนย์ควบคุม Commerce ไปยัง **การค้าปลีกและการพาณิชย์ \> การตั้งค่าศูนย์ควบคุม \> เทมเพลตอีเมลขององค์กร** หรือ **การจัดการองค์กร \> การตั้งค่า \> เทมเพลตอีเมลขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="57f64-111">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates** or **Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="57f64-112">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="57f64-112">Select **New**.</span></span>
1. <span data-ttu-id="57f64-113">ภายใต้ **ทั่วไป** ให้ตั้งค่าฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="57f64-113">Under **General**, set the following fields:</span></span>

    - <span data-ttu-id="57f64-114">**รหัสอีเมล** – รหัสอีเมลเป็นรหัสเฉพาะสำหรับเท็มเพลตและเป็นค่าที่แสดงเมื่อคุณเลือกเท็มเพลตที่จะแม็ปกับเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="57f64-114">**Email ID** – The email ID is the unique identifier for a template, and it's the value that is shown when you select a template to map to an event.</span></span>
    - <span data-ttu-id="57f64-115">**คำอธิบายอีเมล์** – คุณสามารถใช้ฟิลด์ทางเลือกนี้เพื่อระบุคำอธิบายของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="57f64-115">**Email description** – You can use this optional field to provide a description of the template.</span></span> <span data-ttu-id="57f64-116">ค่าที่คุณป้อนจะปรากฏเฉพาะในศูนย์ควบคุม Commerce เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="57f64-116">The value that you enter appears only in Commerce headquarters.</span></span>
    - <span data-ttu-id="57f64-117">**ชื่อผู้ส่ง** – ชื่อที่คุณป้อนจะปรากฏในฟิลด์ "เริ่มต้น" ของไคลเอนต์อีเมลที่มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="57f64-117">**Sender name** – The name that you enter appears in the "from" field of most email clients.</span></span>
    - <span data-ttu-id="57f64-118">**อีเมลของผู้ส่ง** – ป้อนที่อยู่อีเมลที่ควรใช้สำหรับอีเมลที่ส่งโดยใช้เท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="57f64-118">**Sender email** – Enter the email address that should be used for emails that are sent by using this template.</span></span>
    - <span data-ttu-id="57f64-119">**รหัสภาษาเริ่มต้น** – ฟิลด์นี้จะระบุเวอร์ชันที่แปลเป็นภาษาท้องถิ่นของอีเมลที่ส่งโดยค่าเริ่มต้น ถ้าไม่ได้ระบุภาษาโดยช่องทางที่เรียกใช้เท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="57f64-119">**Default language code** – This field specifies the localized version of the email that is sent by default, if no language is provided by the channel that invokes this template.</span></span>

1. <span data-ttu-id="57f64-120">ใต้ **เนื้อหาข้อความอีเมล** ให้เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="57f64-120">Under **Email message content**, select **New**.</span></span>
1. <span data-ttu-id="57f64-121">ในฟิลด์ **ภาษา** ให้ป้อนภาษาสำหรับเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-121">In the **Language** field, enter the language for the email template.</span></span> <span data-ttu-id="57f64-122">คุณสามารถเพิ่มภาษาและเท็มเพลตที่มีการแปลได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="57f64-122">You can add more languages and localized templates later.</span></span>
1. <span data-ttu-id="57f64-123">ใน **ฟิลด์ชื่อเรื่อง** ให้ป้อนชื่อเรื่องของอีเมลที่ควรปรากฏในฟิลด์ชื่อเรื่องของอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-123">In the **Subject** field, enter the email subject that should appear in the subject field of the email.</span></span>
1. <span data-ttu-id="57f64-124">เลือก **แก้ไข** เพื่ออัปโหลดเท็มเพลตอีเมลของคุณ</span><span class="sxs-lookup"><span data-stu-id="57f64-124">Select **Edit** to upload your email template.</span></span>

## <a name="create-an-email-message-body-by-using-html"></a><span data-ttu-id="57f64-125">สร้างเนื้อหาของข้อความอีเมลโดยใช้ HTML</span><span class="sxs-lookup"><span data-stu-id="57f64-125">Create an email message body by using HTML</span></span>

<span data-ttu-id="57f64-126">เนื้อหาของข้อความของอีเมลของคุณจะประกอบด้วย HTML</span><span class="sxs-lookup"><span data-stu-id="57f64-126">The message body of your email is composed in HTML.</span></span> <span data-ttu-id="57f64-127">คุณสามารถใช้โครงร่าง การกำหนดลักษณะ และการสร้างแบรนด์ที่มี Cascading Style Sheet แบบ HTML (CSS) และแบบอินไลน์ให้</span><span class="sxs-lookup"><span data-stu-id="57f64-127">You can use any layout, styling, and branding that HTML and inline Cascading Style Sheets (CSS) allow for.</span></span> <span data-ttu-id="57f64-128">นอกจากนี้คุณยังสามารถใช้รูปภาพได้เช่นกัน ถ้าคุณโฮสต์ไว้บนปลายทางเว็บที่พร้อมใช้งานโดยสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="57f64-128">You can also use images, if you host them on a publicly available web endpoint.</span></span> <span data-ttu-id="57f64-129">เมื่อต้องการเพิ่มรูปภาพ ให้ป้อน URL ของรูปภาพในแอททริบิวต์ **src** ของแท็ก HTML **&lt;img&gt;**</span><span class="sxs-lookup"><span data-stu-id="57f64-129">To add an image, enter the image's URL in the **src** attribute of the HTML **&lt;img&gt;** tag.</span></span>

> [!NOTE]
> <span data-ttu-id="57f64-130">ไคลเอนต์อีเมลที่กำหนดโครงร่างและข้อจำกัดการกำหนดลักษณะซึ่งอาจจำเป็นต้องมีการปรับปรุง HTML และ CSS ที่คุณใช้สำหรับเนื้อหาของข้อความ</span><span class="sxs-lookup"><span data-stu-id="57f64-130">Email clients impose layout and style limitations that might require adjustments to the HTML and CSS that you use for the message body.</span></span> <span data-ttu-id="57f64-131">เราขอแนะนำให้คุณทำความคุ้นเคยกับแนวทางปฏิบัติที่ดีที่สุดสำหรับการสร้าง HTML ซึ่งจะได้รับการสนับสนุนโดยไคลเอนต์อีเมลที่ได้รับความนิยมมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="57f64-131">We recommend that you familiarize yourself with the best practices for creating HTML that will be supported by the most popular email clients.</span></span>

## <a name="add-placeholders-to-the-email-message-body"></a><span data-ttu-id="57f64-132">เพิ่มตัวยึดลงในเนื้อหาของข้อความอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-132">Add placeholders to the email message body</span></span>

<span data-ttu-id="57f64-133">อีเมลของคุณสามารถมีตัวยึดที่จะถูกแทนที่ด้วยค่าเฉพาะของลูกค้าและค่าเฉพาะทางธุรกรรมเมื่อมีการสร้างอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-133">Your email can contain placeholders that are replaced with customer-specific and transaction-specific values when the email is generated.</span></span> <span data-ttu-id="57f64-134">ตัวยึดล้อมรอบด้วยสัญลักษณ์เปอร์เซ็นต์ (%) เสมอและถูกแทรกลงในเอกสาร HTML โดยตรง</span><span class="sxs-lookup"><span data-stu-id="57f64-134">Placeholders are always surrounded by percent signs (%) and are inserted directly into the HTML document.</span></span>

<span data-ttu-id="57f64-135">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="57f64-135">Here is an example.</span></span>

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a><span data-ttu-id="57f64-136">ตัวยึดใบสั่ง (ระดับใบสั่งขาย)</span><span class="sxs-lookup"><span data-stu-id="57f64-136">Order placeholders (sales order level)</span></span>

<span data-ttu-id="57f64-137">ตัวยึดต่อไปนี้จะดึงข้อมูลและแสดงข้อมูลที่กำหนดที่ระดับใบสั่งขาย (เมื่อเทียบกับระดับของบรรทัดการขาย)</span><span class="sxs-lookup"><span data-stu-id="57f64-137">The following placeholders retrieve and show data that is defined at the sales order level (as opposed to the sales line level).</span></span>

| <span data-ttu-id="57f64-138">ชื่อของตัวยึด</span><span class="sxs-lookup"><span data-stu-id="57f64-138">Placeholder name</span></span>     | <span data-ttu-id="57f64-139">ค่าของตัวยึด</span><span class="sxs-lookup"><span data-stu-id="57f64-139">Placeholder value</span></span>                                            |
| -------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="57f64-140">customername</span><span class="sxs-lookup"><span data-stu-id="57f64-140">customername</span></span>         | <span data-ttu-id="57f64-141">ชื่อของลูกค้าที่วางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-141">The name of the customer who placed the order.</span></span>               |
| <span data-ttu-id="57f64-142">salesid</span><span class="sxs-lookup"><span data-stu-id="57f64-142">salesid</span></span>              | <span data-ttu-id="57f64-143">รหัสการขายของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-143">The sales ID of the order.</span></span>                                   |
| <span data-ttu-id="57f64-144">deliveryaddress</span><span class="sxs-lookup"><span data-stu-id="57f64-144">deliveryaddress</span></span>      | <span data-ttu-id="57f64-145">ที่อยู่ที่จัดส่งสำหรับใบสั่งที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-145">The delivery address for shipped orders.</span></span>                     |
| <span data-ttu-id="57f64-146">customeraddress</span><span class="sxs-lookup"><span data-stu-id="57f64-146">customeraddress</span></span>      | <span data-ttu-id="57f64-147">ที่อยู่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="57f64-147">The address of the customer.</span></span>                                 |
| <span data-ttu-id="57f64-148">customermailaddress</span><span class="sxs-lookup"><span data-stu-id="57f64-148">customeremailaddress</span></span> | <span data-ttu-id="57f64-149">ที่อยู่ที่ลูกค้าป้อนเมื่อชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="57f64-149">The email address that the customer entered at checkout.</span></span>     |
| <span data-ttu-id="57f64-150">deliverydate</span><span class="sxs-lookup"><span data-stu-id="57f64-150">deliverydate</span></span>         | <span data-ttu-id="57f64-151">วันที่จัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="57f64-151">The delivery date.</span></span>                                           |
| <span data-ttu-id="57f64-152">shipdate</span><span class="sxs-lookup"><span data-stu-id="57f64-152">shipdate</span></span>             | <span data-ttu-id="57f64-153">วันที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-153">The ship date.</span></span>                                               |
| <span data-ttu-id="57f64-154">modeofdelivery</span><span class="sxs-lookup"><span data-stu-id="57f64-154">modeofdelivery</span></span>       | <span data-ttu-id="57f64-155">วิธีการจัดส่งของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-155">The delivery mode of the order.</span></span>                              |
| <span data-ttu-id="57f64-156">ค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="57f64-156">charges</span></span>              | <span data-ttu-id="57f64-157">ค่าธรรมเนียมรวมสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-157">The total charges for the order.</span></span>                             |
| <span data-ttu-id="57f64-158">ภาษี</span><span class="sxs-lookup"><span data-stu-id="57f64-158">tax</span></span>                  | <span data-ttu-id="57f64-159">ภาษีรวมสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-159">The total tax for the order.</span></span>                                 |
| <span data-ttu-id="57f64-160">ยอดรวม</span><span class="sxs-lookup"><span data-stu-id="57f64-160">total</span></span>                | <span data-ttu-id="57f64-161">ยอดเงินรวมสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-161">The total amount for the order.</span></span>                              |
| <span data-ttu-id="57f64-162">ordernetamount</span><span class="sxs-lookup"><span data-stu-id="57f64-162">ordernetamount</span></span>       | <span data-ttu-id="57f64-163">ยอดเงินรวมสำหรับใบสั่ง ลบด้วยภาษีรวม</span><span class="sxs-lookup"><span data-stu-id="57f64-163">The total amount for the order, minus the total tax.</span></span>         |
| <span data-ttu-id="57f64-164">discount / ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="57f64-164">discount</span></span>             | <span data-ttu-id="57f64-165">ส่วนลดรวมสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-165">The total discount for the order.</span></span>                            |
| <span data-ttu-id="57f64-166">storename</span><span class="sxs-lookup"><span data-stu-id="57f64-166">storename</span></span>            | <span data-ttu-id="57f64-167">ชื่อของร้านค้าที่มีการวางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-167">The name of the store where the order was placed.</span></span>            |
| <span data-ttu-id="57f64-168">storeaddress</span><span class="sxs-lookup"><span data-stu-id="57f64-168">storeaddress</span></span>         | <span data-ttu-id="57f64-169">ที่อยู่ของร้านค้าที่วางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-169">The address of the store that placed the order.</span></span>              |
| <span data-ttu-id="57f64-170">storeopenfrom</span><span class="sxs-lookup"><span data-stu-id="57f64-170">storeopenfrom</span></span>        | <span data-ttu-id="57f64-171">เวลาเปิดของร้านค้าที่วางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-171">The opening time of the store that placed the order.</span></span>         |
| <span data-ttu-id="57f64-172">storeopento</span><span class="sxs-lookup"><span data-stu-id="57f64-172">storeopento</span></span>          | <span data-ttu-id="57f64-173">เวลาปิดของร้านค้าที่วางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-173">The closing time of the store that placed the order.</span></span>         |
| <span data-ttu-id="57f64-174">pickupstorename</span><span class="sxs-lookup"><span data-stu-id="57f64-174">pickupstorename</span></span>      | <span data-ttu-id="57f64-175">ชื่อของร้านค้าที่จะมีการจัดส่งใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-175">The name of the store where the order will be picked up.</span></span>     |
| <span data-ttu-id="57f64-176">pickupstoreaddress</span><span class="sxs-lookup"><span data-stu-id="57f64-176">pickupstoreaddress</span></span>   | <span data-ttu-id="57f64-177">ที่อยู่ของร้านค้าที่จะมีการจัดส่งใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-177">The address of the store where the order will be picked up.</span></span>  |
| <span data-ttu-id="57f64-178">pickupopenstorefrom</span><span class="sxs-lookup"><span data-stu-id="57f64-178">pickupopenstorefrom</span></span>  | <span data-ttu-id="57f64-179">เวลาเปิดของร้านค้าที่จะมีการจัดส่งใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-179">The opening time of the store where the order will be picked up.</span></span> |
| <span data-ttu-id="57f64-180">pickupopenstoreto</span><span class="sxs-lookup"><span data-stu-id="57f64-180">pickupopenstoreto</span></span>    | <span data-ttu-id="57f64-181">เวลาปิดของร้านค้าที่จะมีการจัดส่งใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-181">The closing time of the store where the order will be picked up.</span></span> |

### <a name="order-line-placeholders-sales-line-level"></a><span data-ttu-id="57f64-182">ตัวยึดบรรทัดใบสั่ง (ระดับบรรทัดการขาย)</span><span class="sxs-lookup"><span data-stu-id="57f64-182">Order line placeholders (sales line level)</span></span>

<span data-ttu-id="57f64-183">ตัวยึดตำแหน่งต่อไปนี้จะดึงข้อมูลและแสดงข้อมูลสำหรับผลิตภัณฑ์แต่ละรายการ (บรรทัด) ในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="57f64-183">The following placeholders retrieve and show data for individual products (lines) in the sales order.</span></span>

| <span data-ttu-id="57f64-184">ชื่อของตัวยึด</span><span class="sxs-lookup"><span data-stu-id="57f64-184">Placeholder name</span></span>               | <span data-ttu-id="57f64-185">ค่าของตัวยึด</span><span class="sxs-lookup"><span data-stu-id="57f64-185">Placeholder value</span></span> |
|--------------------------------|-------------------|
| <span data-ttu-id="57f64-186">productid</span><span class="sxs-lookup"><span data-stu-id="57f64-186">productid</span></span>                      | <span data-ttu-id="57f64-187">รหัสผลิตภัณฑ์ของบรรทัด</span><span class="sxs-lookup"><span data-stu-id="57f64-187">The product ID for the line.</span></span> |
| <span data-ttu-id="57f64-188">lineproductname</span><span class="sxs-lookup"><span data-stu-id="57f64-188">lineproductname</span></span>                | <span data-ttu-id="57f64-189">ชื่อของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="57f64-189">The name of the product.</span></span> |
| <span data-ttu-id="57f64-190">lineproductdescription</span><span class="sxs-lookup"><span data-stu-id="57f64-190">lineproductdescription</span></span>         | <span data-ttu-id="57f64-191">คำอธิบายเกี่ยวกับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="57f64-191">The description of the product.</span></span> |
| <span data-ttu-id="57f64-192">linequantity</span><span class="sxs-lookup"><span data-stu-id="57f64-192">linequantity</span></span>                   | <span data-ttu-id="57f64-193">จำนวนของหน่วยที่สั่งสำหรับบรรทัด รวมถึงหน่วยวัด (ตัวอย่างเช่น **ชิ้น** หรือ **คู่**)</span><span class="sxs-lookup"><span data-stu-id="57f64-193">The number of units that were ordered for the line, plus the unit of measure (for example, **ea**, or **pair**).</span></span> |
| <span data-ttu-id="57f64-194">lineunit</span><span class="sxs-lookup"><span data-stu-id="57f64-194">lineunit</span></span>                       | <span data-ttu-id="57f64-195">หน่วยวัดสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="57f64-195">The unit of measure for the line.</span></span> |
| <span data-ttu-id="57f64-196">linequantity_withoutunit</span><span class="sxs-lookup"><span data-stu-id="57f64-196">linequantity_withoutunit</span></span>       | <span data-ttu-id="57f64-197">จำนวนของหน่วยที่สั่งสำหรับบรรทัด โดยไม่มีหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="57f64-197">The number of units that were ordered for the line, without the unit of measure.</span></span> |
| <span data-ttu-id="57f64-198">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="57f64-198">linequantitypicked</span></span>             | <span data-ttu-id="57f64-199">เมื่อมีการใช้เหตุการณ์ **PickOrder** จำนวนหน่วยจะถูกจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="57f64-199">When the **PickOrder** event is used, the number of units that were picked.</span></span> <span data-ttu-id="57f64-200">มิฉะนั้นจะเป็น **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="57f64-200">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="57f64-201">linequantitypicked_withoutunit</span><span class="sxs-lookup"><span data-stu-id="57f64-201">linequantitypicked_withoutunit</span></span> | <span data-ttu-id="57f64-202">เมื่อมีการใช้ **เหตุการณ์** จำนวนหน่วยที่จัดส่ง โดยไม่มีหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="57f64-202">When the **PickOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="57f64-203">มิฉะนั้นจะเป็น **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="57f64-203">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="57f64-204">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="57f64-204">linequantitypacked</span></span>             | <span data-ttu-id="57f64-205">เมื่อมีการใช้เหตุการณ์ **PackOrder** และ **ใบสั่งที่พร้อมสำหรับจัดส่ง** จำนวนหน่วยที่บรรจุ</span><span class="sxs-lookup"><span data-stu-id="57f64-205">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed.</span></span> <span data-ttu-id="57f64-206">มิฉะนั้นจะเป็น **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="57f64-206">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="57f64-207">linequantitypacked_withoutuom</span><span class="sxs-lookup"><span data-stu-id="57f64-207">linequantitypacked_withoutuom</span></span>  | <span data-ttu-id="57f64-208">เมื่อมีการใช้เหตุการณ์ **PackOrder** และ **ใบสั่งที่พร้อมสำหรับจัดส่ง** จำนวนหน่วยที่บรรจุ โดยไม่มีหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="57f64-208">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed, without the unit of measure.</span></span> <span data-ttu-id="57f64-209">มิฉะนั้นจะเป็น **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="57f64-209">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="57f64-210">linequantityshipped</span><span class="sxs-lookup"><span data-stu-id="57f64-210">linequantityshipped</span></span>            | <span data-ttu-id="57f64-211">**0** เสมอ ยกเว้นเมื่อมีการใช้เหตุการณ์เฉพาะดังที่อธิบายไว้ในแถวถัดไป</span><span class="sxs-lookup"><span data-stu-id="57f64-211">Always **0**, except when specific events are used, as described in the next row.</span></span> |
| <span data-ttu-id="57f64-212">linequantityshipped_withoutuom</span><span class="sxs-lookup"><span data-stu-id="57f64-212">linequantityshipped_withoutuom</span></span> | <span data-ttu-id="57f64-213">เมื่อมีการใช้เหตุการณ์ **ShipOrder** จำนวนหน่วยที่จัดส่ง โดยไม่มีหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="57f64-213">When the **ShipOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="57f64-214">มิฉะนั้นจะเป็น **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="57f64-214">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="57f64-215">lineprice</span><span class="sxs-lookup"><span data-stu-id="57f64-215">lineprice</span></span>                      | <span data-ttu-id="57f64-216">ราคาของการขายต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="57f64-216">The price of a single unit.</span></span> |
| <span data-ttu-id="57f64-217">linenetamount</span><span class="sxs-lookup"><span data-stu-id="57f64-217">linenetamount</span></span>                  | <span data-ttu-id="57f64-218">ราคาของรายการหลังจากที่มีการใช้จำนวนหน่วยและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="57f64-218">The price of the line after the number of units and discount are applied.</span></span> |
| <span data-ttu-id="57f64-219">linediscount</span><span class="sxs-lookup"><span data-stu-id="57f64-219">linediscount</span></span>                   | <span data-ttu-id="57f64-220">ส่วนลดสำหรับแต่ละหน่วย</span><span class="sxs-lookup"><span data-stu-id="57f64-220">The discount for an individual unit.</span></span> |
| <span data-ttu-id="57f64-221">lineshipdate</span><span class="sxs-lookup"><span data-stu-id="57f64-221">lineshipdate</span></span>                   | <span data-ttu-id="57f64-222">วันที่จัดส่งสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="57f64-222">The ship date for the line.</span></span> |
| <span data-ttu-id="57f64-223">linedeliverydate</span><span class="sxs-lookup"><span data-stu-id="57f64-223">linedeliverydate</span></span>               | <span data-ttu-id="57f64-224">วันที่จัดส่งสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="57f64-224">The delivery date for the line.</span></span> |
| <span data-ttu-id="57f64-225">linedeliverymode</span><span class="sxs-lookup"><span data-stu-id="57f64-225">linedeliverymode</span></span>               | <span data-ttu-id="57f64-226">วิธีการจัดส่งสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="57f64-226">The delivery mode for the line.</span></span> |
| <span data-ttu-id="57f64-227">linedeliveryaddress</span><span class="sxs-lookup"><span data-stu-id="57f64-227">linedeliveryaddress</span></span>            | <span data-ttu-id="57f64-228">ที่อยู่ที่จัดส่งสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="57f64-228">The delivery address for the line.</span></span> |
| <span data-ttu-id="57f64-229">giftcardnumber</span><span class="sxs-lookup"><span data-stu-id="57f64-229">giftcardnumber</span></span>                 | <span data-ttu-id="57f64-230">หมายเลขบัตรของขวัญสำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="57f64-230">The gift card number, for products of the gift card type.</span></span> |
| <span data-ttu-id="57f64-231">giftcardbalance</span><span class="sxs-lookup"><span data-stu-id="57f64-231">giftcardbalance</span></span>                | <span data-ttu-id="57f64-232">งบของบัตรของขวัญสำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="57f64-232">The gift card balance, for products of the gift card type.</span></span> |
| <span data-ttu-id="57f64-233">giftcardmessage</span><span class="sxs-lookup"><span data-stu-id="57f64-233">giftcardmessage</span></span>                | <span data-ttu-id="57f64-234">ข้อความของบัตรของขวัญสำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="57f64-234">The gift card message, for products of the gift card type.</span></span> |
| <span data-ttu-id="57f64-235">giftcardpin</span><span class="sxs-lookup"><span data-stu-id="57f64-235">giftcardpin</span></span>                    | <span data-ttu-id="57f64-236">หมายเลขรหัสประจำตัวของบัตรของขวัญ สำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="57f64-236">The personal identification number (PIN) of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="57f64-237">(ตัวยึดตำแหน่งนี้จะใช้กับบัตรของขวัญภายนอกโดยเฉพาะ)</span><span class="sxs-lookup"><span data-stu-id="57f64-237">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="57f64-238">giftcardexpiration</span><span class="sxs-lookup"><span data-stu-id="57f64-238">giftcardexpiration</span></span>             | <span data-ttu-id="57f64-239">วันหมดอายุของบัตรของขวัญ สำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="57f64-239">The expiration date of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="57f64-240">(ตัวยึดตำแหน่งนี้จะใช้กับบัตรของขวัญภายนอกโดยเฉพาะ)</span><span class="sxs-lookup"><span data-stu-id="57f64-240">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="57f64-241">giftcardrecipientname</span><span class="sxs-lookup"><span data-stu-id="57f64-241">giftcardrecipientname</span></span>          | <span data-ttu-id="57f64-242">ชื่อของผู้รับบัตรของขวัญ สำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="57f64-242">The name of the gift card recipient, for products of the gift card type.</span></span> |
| <span data-ttu-id="57f64-243">giftcardbuyername</span><span class="sxs-lookup"><span data-stu-id="57f64-243">giftcardbuyername</span></span>              | <span data-ttu-id="57f64-244">ชื่อของผู้ซื้อบัตรของขวัญ สำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="57f64-244">The name of the gift card buyer, for products of the gift card type.</span></span> |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a><span data-ttu-id="57f64-245">รูปแบบของตัวยึดบรรทัดใบสั่งในเนื้อหาของข้อความอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-245">Format of order line placeholders in the email message body</span></span>

<span data-ttu-id="57f64-246">เมื่อคุณสร้าง HTML สำหรับบรรทัดใบสั่งแต่ละบรรทัดในเนื้อหาของข้อความอีเมล ให้ใช้บล็อกที่ซ้ำกันของ HTML และตัวยึดสำหรับบรรทัดที่มีตัวยึดตำแหน่งต่อไปนี้ที่จะใส่ไว้ภายในแท็กข้อคิดเห็นของ HTML</span><span class="sxs-lookup"><span data-stu-id="57f64-246">When you create the HTML for the individual order lines in the email message body, surround the repeating block of HTML and placeholders for the lines with the following placeholders that are put inside HTML comment tags.</span></span>

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

<span data-ttu-id="57f64-247">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="57f64-247">Here is an example.</span></span>

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a><span data-ttu-id="57f64-248">สร้างเท็มเพลตสำหรับใบเสร็จรับเงินที่ส่งทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-248">Create a template for emailed receipts</span></span>

<span data-ttu-id="57f64-249">ใบเสร็จรับเงินสามารถส่งอีเมลถึงลูกค้าที่ทำการซื้อสินค้าที่การขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="57f64-249">Receipts can be emailed to customers who make purchases at a retail point of sale (POS).</span></span> <span data-ttu-id="57f64-250">โดยทั่วไปขั้นตอนสำหรับการสร้างเท็มเพลตใบเสร็จรับเงินที่ส่งทางอีเมลนั้นจะเหมือนกับขั้นตอนสำหรับการสร้างเท็มเพลตสำหรับเหตุการณ์ของธุรกรรมอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="57f64-250">In general, the steps for creating the emailed receipt template are the same as the steps for creating templates for other transactional events.</span></span> <span data-ttu-id="57f64-251">อย่างไรก็ตามต้องมีการเปลี่ยนแปลงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="57f64-251">However, the following changes are required:</span></span>

- <span data-ttu-id="57f64-252">ข้อความของใบเสร็จจะถูกแทรกลงในอีเมลโดยใช้ตัวยึด **%message%**</span><span class="sxs-lookup"><span data-stu-id="57f64-252">The text of the receipt is inserted into the email by using the **%message%** placeholder.</span></span> <span data-ttu-id="57f64-253">เพื่อให้แน่ใจว่ามีการแสดงผลเนื้อหาของใบเสร็จอย่างถูกต้อง ให้ล้อมรอบตัวยึดตำแหน่ง **%message%** ด้วยแท็ก HTML **&lt;pre&gt;** และ **&lt;/pre&gt;**</span><span class="sxs-lookup"><span data-stu-id="57f64-253">To ensure that the receipt body is correctly rendered, surround the **%message%** placeholder with HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tags.</span></span>
- <span data-ttu-id="57f64-254">ตัวยึด **%receiptid%** สามารถใช้เพื่อแสดง QR code หรือบาร์โค้ดที่แสดงรหัสใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="57f64-254">The **%receiptid%** placeholder can be used to show a QR code or bar code that represents the receipt ID.</span></span> <span data-ttu-id="57f64-255">(QR codes และบาร์โค้ดจะถูกสร้างขึ้นแบบไดนามิกและให้บริการโดยบริการของบุคคลที่สาม) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีแสดง QR code หรือบาร์โค้ดในใบเสร็จทางงอีเมล โปรดดูที่ [เพิ่ม QR code หรือบาร์โค้ดในการทำธุรกรรมและใบเสร็จทางอีเมล](add-qr-code-barcode-email.md)</span><span class="sxs-lookup"><span data-stu-id="57f64-255">(QR codes and bar codes are dynamically generated and served by a third-party service.) For more information about how to show a QR code or bar code in an emailed receipt, see [Add a QR code or bar code to transactional and receipt emails](add-qr-code-barcode-email.md).</span></span>

## <a name="upload-the-email-html"></a><span data-ttu-id="57f64-256">อัปโหลด HTML ของอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-256">Upload the email HTML</span></span>

<span data-ttu-id="57f64-257">หลังจากที่คุณได้สร้างและทดสอบ HTML สำหรับเนื้อหาของข้อความของคุณแล้ว คุณต้องอัปโหลด HTML ไปที่ศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="57f64-257">After you've created and tested the HTML for your message body, it must be uploaded to Commerce headquarters.</span></span> <span data-ttu-id="57f64-258">ในขณะนี้ไม่สามารถส่งออกอีเมล HTML ได้</span><span class="sxs-lookup"><span data-stu-id="57f64-258">Currently, email HTML can't be exported.</span></span> <span data-ttu-id="57f64-259">ดังนั้นคุณต้องรักษาสำเนาของหลักของ HTML ภายนอกศูนย์ควบคุม Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="57f64-259">Therefore, you must maintain the master copy of your HTML outside Commerce headquarters.</span></span>

<span data-ttu-id="57f64-260">เมื่อต้องการอัปโหลด HTML เท็มเพลตอีเมลใหม่หรือที่แก้ไข ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="57f64-260">To upload a new or edited email template HTML, follow these steps.</span></span>

1. <span data-ttu-id="57f64-261">ในศูนย์ควบคุมของ Commerce ให้ไปที่ **การขายปลีกและ Commerce \> การตั้งค่าศูนย์ควบคุม \> เท็มเพลตอีเมลขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="57f64-261">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="57f64-262">เลือกแถวสำหรับภาษาที่คุณต้องการเพิ่มหรือแทนที่ HTML</span><span class="sxs-lookup"><span data-stu-id="57f64-262">Select the row for the language that you want to add or replace HTML for.</span></span> <span data-ttu-id="57f64-263">อีกทางหนึ่งคือเลือก **สร้าง** เพื่อสร้างแถวสำหรับภาษาใหม่</span><span class="sxs-lookup"><span data-stu-id="57f64-263">Alternatively, select **New** to create a row for a new language.</span></span>
1. <span data-ttu-id="57f64-264">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="57f64-264">Select **Edit**.</span></span>
1. <span data-ttu-id="57f64-265">ในกล่องโต้ตอบที่ปรากฏ เลือก **เรียกดู**</span><span class="sxs-lookup"><span data-stu-id="57f64-265">In the dialog box that appears, select **Browse**.</span></span> <span data-ttu-id="57f64-266">เรียกดูเอกสาร HTML ที่คุณต้องการอัปโหลด เลือกเอกสาร แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="57f64-266">Browse to the HTML document that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="57f64-267">เลือก **อัปโหลด**</span><span class="sxs-lookup"><span data-stu-id="57f64-267">Select **Upload**.</span></span>
1. <span data-ttu-id="57f64-268">หลังจากที่ HTML ของอีเมลของคุณปรากฏในหน้าต่างแสดงตัวอย่าง ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="57f64-268">After your email HTML appears in the preview window, select **OK**.</span></span>
1. <span data-ttu-id="57f64-269">ตรวจสอบให้แน่ใจว่ามีการเลือกกล่องกาเครื่องหมาย **มีเนื้อหา** สำหรับแถว</span><span class="sxs-lookup"><span data-stu-id="57f64-269">Make sure that the **Has body** check box is selected for the row.</span></span>

<span data-ttu-id="57f64-270">ถ้าคุณได้ตั้งกำหนดค่าศูนย์ควบคุม Commerce ไว้แล้วเพื่อส่งอีเมล อีเมลใหม่หรือที่อัปเดตแล้วของคุณจะถูกส่งไปยังลูกค้าทั้งหมดที่ทำธุรกรรมที่เรียกใช้เหตุการณ์ที่ถูกแม็ปกับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="57f64-270">If you've already configured Commerce headquarters to send email, your new or updated email will be sent to all customers who perform a transaction that invokes the event that is mapped to the template.</span></span>

<span data-ttu-id="57f64-271">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนดค่าอีเมลใน Dynamics 365 Commerce ดูที่ [กำหนดค่าและส่งอีเมล](../fin-ops-core/fin-ops/organization-administration/configure-email.md)</span><span class="sxs-lookup"><span data-stu-id="57f64-271">For more information about how to configure emails in Dynamics 365 Commerce, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57f64-272">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="57f64-272">Additional resources</span></span> 

[<span data-ttu-id="57f64-273">ตั้งค่าโพรไฟล์การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-273">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="57f64-274">ตั้งค่าคอนฟิกและส่งอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-274">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[<span data-ttu-id="57f64-275">ตั้งค่าใบเสร็จทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="57f64-275">Set up email receipts</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[<span data-ttu-id="57f64-276">ส่งใบเสร็จทางอีเมลจาก Modern POS</span><span class="sxs-lookup"><span data-stu-id="57f64-276">Send email receipts from Modern POS </span></span>](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
