---
title: สร้างเท็มเพลตอีเมลสำหรับเหตุการณ์ของธุรกรรม
description: หัวข้อนี้จะอธิบายวิธีการสร้าง อัปโหลด และกำหนดค่าเท็มเพลตอีเมลสำหรับเหตุการณ์ทางของธุรกรรมใน Microsoft Dynamics 365 Commerce
author: stuharg
manager: annbe
ms.date: 06/01/2020
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
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a02839088addfa9b405af486f3b795eace1671cc
ms.sourcegitcommit: 4db8c30c2f26af1896938dd3ece3756577374ecb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/01/2020
ms.locfileid: "3416590"
---
# <a name="create-email-templates-for-transactional-events"></a><span data-ttu-id="ca8df-103">สร้างเท็มเพลตอีเมลสำหรับเหตุการณ์ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ca8df-103">Create email templates for transactional events</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ca8df-104">หัวข้อนี้จะอธิบายวิธีการสร้าง อัปโหลด และกำหนดค่าเท็มเพลตอีเมลสำหรับเหตุการณ์ทางของธุรกรรมใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ca8df-104">This topic describes how to create, upload, and configure email templates for transactional events in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ca8df-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="ca8df-105">Overview</span></span>

<span data-ttu-id="ca8df-106">Dynamics 365 Commerce มีโซลูชันสำเร็จรูปสำหรับการส่งอีเมลที่แจ้งเตือนลูกค้าเกี่ยวกับเหตุการณ์ของธุรกรรม (ตัวอย่างเช่น เมื่อทำการสั่งซื้อ การสั่งซื้อจะพร้อมสำหรับการเบิกสินค้า หรือการจัดส่งสินค้าตามใบสั่ง)</span><span class="sxs-lookup"><span data-stu-id="ca8df-106">Dynamics 365 Commerce provides an out-of-box solution for sending emails that alert customers about transactional events (for example, when an order is placed, an order is ready for pickup, or an order has been shipped).</span></span> <span data-ttu-id="ca8df-107">หัวข้อนี้จะอธิบายขั้นตอนสำหรับการสร้าง อัปโหลด และกำหนดค่าเท็มเพลตอีเมลที่ใช้ในการส่งอีเมลของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ca8df-107">This topic describes the steps for creating, uploading, and configuring the email templates that are used to send transactional emails.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="ca8df-108">สร้างเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-108">Create an email template</span></span>

<span data-ttu-id="ca8df-109">ก่อนที่คุณจะสามารถแม็ปเหตุการณ์ของธุรกรรมเฉพาะกับเท็มเพลตอีเมลได้ คุณต้องสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="ca8df-109">Before you can map a specific transactional event to an email template, you must create the template.</span></span>

<span data-ttu-id="ca8df-110">ทำตามขั้นตอนเหล่านี้เพื่อสร้างแม่แบบอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-110">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="ca8df-111">ในสำนักงานใหญ่ Commerce ไปยัง **แม่แบบอีเมลขององค์กร** ซึ่งอยู่ภายใต้ **Retail และ Commerce \> การตั้งค่าสำนักงานใหญ่ \> แม่แบบอีเมลขององค์กร** หรือ **การจัดการองค์กร \> การตั้งค่า \> แม่แบบอีเมลขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="ca8df-111">In Commerce headquarters, go to **Organization email templates**, which is under **Retail and Commerce \> Headquarters setup \> Organization email templates** or **Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="ca8df-112">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ca8df-112">Select **New**.</span></span>
1. <span data-ttu-id="ca8df-113">ภายใต้ **ทั่วไป** ให้ตั้งค่าฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ca8df-113">Under **General**, set the following fields:</span></span>

    - <span data-ttu-id="ca8df-114">**รหัสอีเมล** – รหัสอีเมลเป็นรหัสเฉพาะสำหรับเท็มเพลตและเป็นค่าที่แสดงเมื่อคุณเลือกเท็มเพลตที่จะแม็ปกับเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="ca8df-114">**Email ID** – The email ID is the unique identifier for a template, and it's the value that is shown when you select a template to map to an event.</span></span>
    - <span data-ttu-id="ca8df-115">**คำอธิบายอีเมล์** – คุณสามารถใช้ฟิลด์ทางเลือกนี้เพื่อระบุคำอธิบายของเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="ca8df-115">**Email description** – You can use this optional field to provide a description of the template.</span></span> <span data-ttu-id="ca8df-116">ค่าที่คุณป้อนจะปรากฏเฉพาะในศูนย์ควบคุม Commerce เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ca8df-116">The value that you enter appears only in Commerce headquarters.</span></span>
    - <span data-ttu-id="ca8df-117">**ชื่อผู้ส่ง** – ชื่อที่คุณป้อนจะปรากฏในฟิลด์ "เริ่มต้น" ของไคลเอนต์อีเมลที่มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="ca8df-117">**Sender name** – The name that you enter appears in the "from" field of most email clients.</span></span>
    - <span data-ttu-id="ca8df-118">**อีเมลของผู้ส่ง** – ป้อนที่อยู่อีเมลที่ควรใช้สำหรับอีเมลที่ส่งโดยใช้เท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="ca8df-118">**Sender email** – Enter the email address that should be used for emails that are sent by using this template.</span></span>
    - <span data-ttu-id="ca8df-119">**รหัสภาษาเริ่มต้น** – ฟิลด์นี้จะระบุเวอร์ชันที่แปลเป็นภาษาท้องถิ่นของอีเมลที่ส่งโดยค่าเริ่มต้น ถ้าไม่ได้ระบุภาษาโดยช่องทางที่เรียกใช้เท็มเพลตนี้</span><span class="sxs-lookup"><span data-stu-id="ca8df-119">**Default language code** – This field specifies the localized version of the email that is sent by default, if no language is provided by the channel that invokes this template.</span></span>

1. <span data-ttu-id="ca8df-120">ใต้ **เนื้อหาข้อความอีเมล** ให้เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ca8df-120">Under **Email message content**, select **New**.</span></span>
1. <span data-ttu-id="ca8df-121">ในฟิลด์ **ภาษา** ให้ป้อนภาษาสำหรับเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-121">In the **Language** field, enter the language for the email template.</span></span> <span data-ttu-id="ca8df-122">คุณสามารถเพิ่มภาษาและเท็มเพลตที่มีการแปลได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="ca8df-122">You can add more languages and localized templates later.</span></span>
1. <span data-ttu-id="ca8df-123">ใน **ฟิลด์ชื่อเรื่อง** ให้ป้อนชื่อเรื่องของอีเมลที่ควรปรากฏในฟิลด์ชื่อเรื่องของอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-123">In the **Subject** field, enter the email subject that should appear in the subject field of the email.</span></span>
1. <span data-ttu-id="ca8df-124">เลือก **แก้ไข** เพื่ออัปโหลดเท็มเพลตอีเมลของคุณ</span><span class="sxs-lookup"><span data-stu-id="ca8df-124">Select **Edit** to upload your email template.</span></span>

## <a name="create-an-email-message-body-by-using-html"></a><span data-ttu-id="ca8df-125">สร้างเนื้อหาของข้อความอีเมลโดยใช้ HTML</span><span class="sxs-lookup"><span data-stu-id="ca8df-125">Create an email message body by using HTML</span></span>

<span data-ttu-id="ca8df-126">เนื้อหาของข้อความของอีเมลของคุณจะประกอบด้วย HTML</span><span class="sxs-lookup"><span data-stu-id="ca8df-126">The message body of your email is composed in HTML.</span></span> <span data-ttu-id="ca8df-127">คุณสามารถใช้โครงร่าง การกำหนดลักษณะ และการสร้างแบรนด์ที่มี Cascading Style Sheet แบบ HTML (CSS) และแบบอินไลน์ให้</span><span class="sxs-lookup"><span data-stu-id="ca8df-127">You can use any layout, styling, and branding that HTML and inline Cascading Style Sheets (CSS) allow for.</span></span> <span data-ttu-id="ca8df-128">นอกจากนี้คุณยังสามารถใช้รูปภาพได้เช่นกัน ถ้าคุณโฮสต์ไว้บนปลายทางเว็บที่พร้อมใช้งานโดยสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="ca8df-128">You can also use images, if you host them on a publicly available web endpoint.</span></span> <span data-ttu-id="ca8df-129">เมื่อต้องการเพิ่มรูปภาพ ให้ป้อน URL ของรูปภาพในแอททริบิวต์ **src** ของแท็ก HTML **&lt;img&gt;**</span><span class="sxs-lookup"><span data-stu-id="ca8df-129">To add an image, enter the image's URL in the **src** attribute of the HTML **&lt;img&gt;** tag.</span></span>

> [!NOTE]
> <span data-ttu-id="ca8df-130">ไคลเอนต์อีเมลที่กำหนดโครงร่างและข้อจำกัดการกำหนดลักษณะซึ่งอาจจำเป็นต้องมีการปรับปรุง HTML และ CSS ที่คุณใช้สำหรับเนื้อหาของข้อความ</span><span class="sxs-lookup"><span data-stu-id="ca8df-130">Email clients impose layout and style limitations that might require adjustments to the HTML and CSS that you use for the message body.</span></span> <span data-ttu-id="ca8df-131">เราขอแนะนำให้คุณทำความคุ้นเคยกับแนวทางปฏิบัติที่ดีที่สุดสำหรับการสร้าง HTML ซึ่งจะได้รับการสนับสนุนโดยไคลเอนต์อีเมลที่ได้รับความนิยมมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="ca8df-131">We recommend that you familiarize yourself with the best practices for creating HTML that will be supported by the most popular email clients.</span></span>

## <a name="add-placeholders-to-the-email-message-body"></a><span data-ttu-id="ca8df-132">เพิ่มตัวยึดลงในเนื้อหาของข้อความอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-132">Add placeholders to the email message body</span></span>

<span data-ttu-id="ca8df-133">อีเมลของคุณสามารถมีตัวยึดที่จะถูกแทนที่ด้วยค่าเฉพาะของลูกค้าและค่าเฉพาะทางธุรกรรมเมื่อมีการสร้างอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-133">Your email can contain placeholders that are replaced with customer-specific and transaction-specific values when the email is generated.</span></span> <span data-ttu-id="ca8df-134">ตัวยึดล้อมรอบด้วยสัญลักษณ์เปอร์เซ็นต์ (%) เสมอและถูกแทรกลงในเอกสาร HTML โดยตรง</span><span class="sxs-lookup"><span data-stu-id="ca8df-134">Placeholders are always surrounded by percent signs (%) and are inserted directly into the HTML document.</span></span>

<span data-ttu-id="ca8df-135">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ca8df-135">Here is an example.</span></span>

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a><span data-ttu-id="ca8df-136">ตัวยึดใบสั่ง (ระดับใบสั่งขาย)</span><span class="sxs-lookup"><span data-stu-id="ca8df-136">Order placeholders (sales order level)</span></span>

<span data-ttu-id="ca8df-137">ตัวยึดต่อไปนี้จะดึงข้อมูลและแสดงข้อมูลที่กำหนดที่ระดับใบสั่งขาย (เมื่อเทียบกับระดับของบรรทัดการขาย)</span><span class="sxs-lookup"><span data-stu-id="ca8df-137">The following placeholders retrieve and show data that is defined at the sales order level (as opposed to the sales line level).</span></span>

| <span data-ttu-id="ca8df-138">ชื่อของตัวยึด</span><span class="sxs-lookup"><span data-stu-id="ca8df-138">Placeholder name</span></span>    | <span data-ttu-id="ca8df-139">ค่าของตัวยึด</span><span class="sxs-lookup"><span data-stu-id="ca8df-139">Placeholder value</span></span>                                                |
|---------------------|------------------------------------------------------------------|
| <span data-ttu-id="ca8df-140">customername</span><span class="sxs-lookup"><span data-stu-id="ca8df-140">customername</span></span>        | <span data-ttu-id="ca8df-141">ชื่อของลูกค้าที่วางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-141">The name of the customer who placed the order.</span></span>                   |
| <span data-ttu-id="ca8df-142">salesid</span><span class="sxs-lookup"><span data-stu-id="ca8df-142">salesid</span></span>             | <span data-ttu-id="ca8df-143">รหัสการขายของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-143">The sales ID of the order.</span></span>                                       |
| <span data-ttu-id="ca8df-144">deliveryaddress</span><span class="sxs-lookup"><span data-stu-id="ca8df-144">deliveryaddress</span></span>     | <span data-ttu-id="ca8df-145">ที่อยู่ที่จัดส่งสำหรับใบสั่งที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-145">The delivery address for shipped orders.</span></span>                         |
| <span data-ttu-id="ca8df-146">customeraddress</span><span class="sxs-lookup"><span data-stu-id="ca8df-146">customeraddress</span></span>     | <span data-ttu-id="ca8df-147">ที่อยู่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ca8df-147">The address of the customer.</span></span>                                     |
| <span data-ttu-id="ca8df-148">deliverydate</span><span class="sxs-lookup"><span data-stu-id="ca8df-148">deliverydate</span></span>        | <span data-ttu-id="ca8df-149">วันที่จัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="ca8df-149">The delivery date.</span></span>                                               |
| <span data-ttu-id="ca8df-150">shipdate</span><span class="sxs-lookup"><span data-stu-id="ca8df-150">shipdate</span></span>            | <span data-ttu-id="ca8df-151">วันที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-151">The ship date.</span></span>                                                   |
| <span data-ttu-id="ca8df-152">modeofdelivery</span><span class="sxs-lookup"><span data-stu-id="ca8df-152">modeofdelivery</span></span>      | <span data-ttu-id="ca8df-153">วิธีการจัดส่งของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-153">The delivery mode of the order.</span></span>                                  |
| <span data-ttu-id="ca8df-154">ค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="ca8df-154">charges</span></span>             | <span data-ttu-id="ca8df-155">ค่าธรรมเนียมรวมสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-155">The total charges for the order.</span></span>                                 |
| <span data-ttu-id="ca8df-156">ภาษี</span><span class="sxs-lookup"><span data-stu-id="ca8df-156">tax</span></span>                 | <span data-ttu-id="ca8df-157">ภาษีรวมสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-157">The total tax for the order.</span></span>                                     |
| <span data-ttu-id="ca8df-158">ยอดรวม</span><span class="sxs-lookup"><span data-stu-id="ca8df-158">total</span></span>               | <span data-ttu-id="ca8df-159">ยอดเงินรวมสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-159">The total amount for the order.</span></span>                                  |
| <span data-ttu-id="ca8df-160">ordernetamount</span><span class="sxs-lookup"><span data-stu-id="ca8df-160">ordernetamount</span></span>      | <span data-ttu-id="ca8df-161">ยอดเงินรวมสำหรับใบสั่ง ลบด้วยภาษีรวม</span><span class="sxs-lookup"><span data-stu-id="ca8df-161">The total amount for the order, minus the total tax.</span></span>             |
| <span data-ttu-id="ca8df-162">discount / ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="ca8df-162">discount</span></span>            | <span data-ttu-id="ca8df-163">ส่วนลดรวมสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-163">The total discount for the order.</span></span>                                |
| <span data-ttu-id="ca8df-164">storename</span><span class="sxs-lookup"><span data-stu-id="ca8df-164">storename</span></span>           | <span data-ttu-id="ca8df-165">ชื่อของร้านค้าที่มีการวางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-165">The name of the store where the order was placed.</span></span>                |
| <span data-ttu-id="ca8df-166">storeaddress</span><span class="sxs-lookup"><span data-stu-id="ca8df-166">storeaddress</span></span>        | <span data-ttu-id="ca8df-167">ที่อยู่ของร้านค้าที่วางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-167">The address of the store that placed the order.</span></span>                  |
| <span data-ttu-id="ca8df-168">storeopenfrom</span><span class="sxs-lookup"><span data-stu-id="ca8df-168">storeopenfrom</span></span>       | <span data-ttu-id="ca8df-169">เวลาเปิดของร้านค้าที่วางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-169">The opening time of the store that placed the order.</span></span>             |
| <span data-ttu-id="ca8df-170">storeopento</span><span class="sxs-lookup"><span data-stu-id="ca8df-170">storeopento</span></span>         | <span data-ttu-id="ca8df-171">เวลาปิดของร้านค้าที่วางใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-171">The closing time of the store that placed the order.</span></span>             |
| <span data-ttu-id="ca8df-172">pickupstorename</span><span class="sxs-lookup"><span data-stu-id="ca8df-172">pickupstorename</span></span>     | <span data-ttu-id="ca8df-173">ชื่อของร้านค้าที่จะมีการจัดส่งใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-173">The name of the store where the order will be picked up.</span></span>         |
| <span data-ttu-id="ca8df-174">pickupstoreaddress</span><span class="sxs-lookup"><span data-stu-id="ca8df-174">pickupstoreaddress</span></span>  | <span data-ttu-id="ca8df-175">ที่อยู่ของร้านค้าที่จะมีการจัดส่งใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-175">The address of the store where the order will be picked up.</span></span>      |
| <span data-ttu-id="ca8df-176">pickupopenstorefrom</span><span class="sxs-lookup"><span data-stu-id="ca8df-176">pickupopenstorefrom</span></span> | <span data-ttu-id="ca8df-177">เวลาเปิดของร้านค้าที่จะมีการจัดส่งใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-177">The opening time of the store where the order will be picked up.</span></span> |
| <span data-ttu-id="ca8df-178">pickupopenstoreto</span><span class="sxs-lookup"><span data-stu-id="ca8df-178">pickupopenstoreto</span></span>   | <span data-ttu-id="ca8df-179">เวลาปิดของร้านค้าที่จะมีการจัดส่งใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-179">The closing time of the store where the order will be picked up.</span></span> |

### <a name="order-line-placeholders-sales-line-level"></a><span data-ttu-id="ca8df-180">ตัวยึดบรรทัดใบสั่ง (ระดับบรรทัดการขาย)</span><span class="sxs-lookup"><span data-stu-id="ca8df-180">Order line placeholders (sales line level)</span></span>

<span data-ttu-id="ca8df-181">ตัวยึดตำแหน่งต่อไปนี้จะดึงข้อมูลและแสดงข้อมูลสำหรับผลิตภัณฑ์แต่ละรายการ (บรรทัด) ในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="ca8df-181">The following placeholders retrieve and show data for individual products (lines) in the sales order.</span></span>

| <span data-ttu-id="ca8df-182">ชื่อของตัวยึด</span><span class="sxs-lookup"><span data-stu-id="ca8df-182">Placeholder name</span></span>               | <span data-ttu-id="ca8df-183">ค่าของตัวยึด</span><span class="sxs-lookup"><span data-stu-id="ca8df-183">Placeholder value</span></span> |
|--------------------------------|-------------------|
| <span data-ttu-id="ca8df-184">productid</span><span class="sxs-lookup"><span data-stu-id="ca8df-184">productid</span></span>                      | <span data-ttu-id="ca8df-185">รหัสผลิตภัณฑ์ของบรรทัด</span><span class="sxs-lookup"><span data-stu-id="ca8df-185">The product ID for the line.</span></span> |
| <span data-ttu-id="ca8df-186">lineproductname</span><span class="sxs-lookup"><span data-stu-id="ca8df-186">lineproductname</span></span>                | <span data-ttu-id="ca8df-187">ชื่อของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ca8df-187">The name of the product.</span></span> |
| <span data-ttu-id="ca8df-188">lineproductdescription</span><span class="sxs-lookup"><span data-stu-id="ca8df-188">lineproductdescription</span></span>         | <span data-ttu-id="ca8df-189">คำอธิบายเกี่ยวกับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ca8df-189">The description of the product.</span></span> |
| <span data-ttu-id="ca8df-190">linequantity</span><span class="sxs-lookup"><span data-stu-id="ca8df-190">linequantity</span></span>                   | <span data-ttu-id="ca8df-191">จำนวนของหน่วยที่สั่งสำหรับบรรทัด รวมถึงหน่วยวัด (ตัวอย่างเช่น **ชิ้น** หรือ **คู่**)</span><span class="sxs-lookup"><span data-stu-id="ca8df-191">The number of units that were ordered for the line, plus the unit of measure (for example, **ea**, or **pair**).</span></span> |
| <span data-ttu-id="ca8df-192">lineunit</span><span class="sxs-lookup"><span data-stu-id="ca8df-192">lineunit</span></span>                       | <span data-ttu-id="ca8df-193">หน่วยวัดสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="ca8df-193">The unit of measure for the line.</span></span> |
| <span data-ttu-id="ca8df-194">linequantity_withoutunit</span><span class="sxs-lookup"><span data-stu-id="ca8df-194">linequantity_withoutunit</span></span>       | <span data-ttu-id="ca8df-195">จำนวนของหน่วยที่สั่งสำหรับบรรทัด โดยไม่มีหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="ca8df-195">The number of units that were ordered for the line, without the unit of measure.</span></span> |
| <span data-ttu-id="ca8df-196">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="ca8df-196">linequantitypicked</span></span>             | <span data-ttu-id="ca8df-197">เมื่อมีการใช้เหตุการณ์ **PickOrder** จำนวนหน่วยจะถูกจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-197">When the **PickOrder** event is used, the number of units that were picked.</span></span> <span data-ttu-id="ca8df-198">มิฉะนั้นจะเป็น **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="ca8df-198">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="ca8df-199">linequantitypicked_withoutunit</span><span class="sxs-lookup"><span data-stu-id="ca8df-199">linequantitypicked_withoutunit</span></span> | <span data-ttu-id="ca8df-200">เมื่อมีการใช้ **เหตุการณ์** จำนวนหน่วยที่จัดส่ง โดยไม่มีหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="ca8df-200">When the **PickOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="ca8df-201">มิฉะนั้นจะเป็น **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="ca8df-201">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="ca8df-202">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="ca8df-202">linequantitypacked</span></span>             | <span data-ttu-id="ca8df-203">เมื่อมีการใช้เหตุการณ์ **PackOrder** และ **ใบสั่งที่พร้อมสำหรับจัดส่ง** จำนวนหน่วยที่บรรจุ</span><span class="sxs-lookup"><span data-stu-id="ca8df-203">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed.</span></span> <span data-ttu-id="ca8df-204">มิฉะนั้นจะเป็น **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="ca8df-204">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="ca8df-205">linequantitypacked_withoutuom</span><span class="sxs-lookup"><span data-stu-id="ca8df-205">linequantitypacked_withoutuom</span></span>  | <span data-ttu-id="ca8df-206">เมื่อมีการใช้เหตุการณ์ **PackOrder** และ **ใบสั่งที่พร้อมสำหรับจัดส่ง** จำนวนหน่วยที่บรรจุ โดยไม่มีหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="ca8df-206">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed, without the unit of measure.</span></span> <span data-ttu-id="ca8df-207">มิฉะนั้นจะเป็น **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="ca8df-207">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="ca8df-208">linequantityshipped</span><span class="sxs-lookup"><span data-stu-id="ca8df-208">linequantityshipped</span></span>            | <span data-ttu-id="ca8df-209">**0** เสมอ ยกเว้นเมื่อมีการใช้เหตุการณ์เฉพาะดังที่อธิบายไว้ในแถวถัดไป</span><span class="sxs-lookup"><span data-stu-id="ca8df-209">Always **0**, except when specific events are used, as described in the next row.</span></span> |
| <span data-ttu-id="ca8df-210">linequantityshipped_withoutuom</span><span class="sxs-lookup"><span data-stu-id="ca8df-210">linequantityshipped_withoutuom</span></span> | <span data-ttu-id="ca8df-211">เมื่อมีการใช้เหตุการณ์ **ShipOrder** จำนวนหน่วยที่จัดส่ง โดยไม่มีหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="ca8df-211">When the **ShipOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="ca8df-212">มิฉะนั้นจะเป็น **0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="ca8df-212">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="ca8df-213">lineprice</span><span class="sxs-lookup"><span data-stu-id="ca8df-213">lineprice</span></span>                      | <span data-ttu-id="ca8df-214">ราคาของการขายต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="ca8df-214">The price of a single unit.</span></span> |
| <span data-ttu-id="ca8df-215">linenetamount</span><span class="sxs-lookup"><span data-stu-id="ca8df-215">linenetamount</span></span>                  | <span data-ttu-id="ca8df-216">ราคาของรายการหลังจากที่มีการใช้จำนวนหน่วยและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="ca8df-216">The price of the line after the number of units and discount are applied.</span></span> |
| <span data-ttu-id="ca8df-217">linediscount</span><span class="sxs-lookup"><span data-stu-id="ca8df-217">linediscount</span></span>                   | <span data-ttu-id="ca8df-218">ส่วนลดสำหรับแต่ละหน่วย</span><span class="sxs-lookup"><span data-stu-id="ca8df-218">The discount for an individual unit.</span></span> |
| <span data-ttu-id="ca8df-219">lineshipdate</span><span class="sxs-lookup"><span data-stu-id="ca8df-219">lineshipdate</span></span>                   | <span data-ttu-id="ca8df-220">วันที่จัดส่งสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="ca8df-220">The ship date for the line.</span></span> |
| <span data-ttu-id="ca8df-221">linedeliverydate</span><span class="sxs-lookup"><span data-stu-id="ca8df-221">linedeliverydate</span></span>               | <span data-ttu-id="ca8df-222">วันที่จัดส่งสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="ca8df-222">The delivery date for the line.</span></span> |
| <span data-ttu-id="ca8df-223">linedeliverymode</span><span class="sxs-lookup"><span data-stu-id="ca8df-223">linedeliverymode</span></span>               | <span data-ttu-id="ca8df-224">วิธีการจัดส่งสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="ca8df-224">The delivery mode for the line.</span></span> |
| <span data-ttu-id="ca8df-225">linedeliveryaddress</span><span class="sxs-lookup"><span data-stu-id="ca8df-225">linedeliveryaddress</span></span>            | <span data-ttu-id="ca8df-226">ที่อยู่ที่จัดส่งสำหรับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="ca8df-226">The delivery address for the line.</span></span> |
| <span data-ttu-id="ca8df-227">giftcardnumber</span><span class="sxs-lookup"><span data-stu-id="ca8df-227">giftcardnumber</span></span>                 | <span data-ttu-id="ca8df-228">หมายเลขบัตรของขวัญสำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="ca8df-228">The gift card number, for products of the gift card type.</span></span> |
| <span data-ttu-id="ca8df-229">giftcardbalance</span><span class="sxs-lookup"><span data-stu-id="ca8df-229">giftcardbalance</span></span>                | <span data-ttu-id="ca8df-230">งบของบัตรของขวัญสำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="ca8df-230">The gift card balance, for products of the gift card type.</span></span> |
| <span data-ttu-id="ca8df-231">giftcardmessage</span><span class="sxs-lookup"><span data-stu-id="ca8df-231">giftcardmessage</span></span>                | <span data-ttu-id="ca8df-232">ข้อความของบัตรของขวัญสำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="ca8df-232">The gift card message, for products of the gift card type.</span></span> |
| <span data-ttu-id="ca8df-233">giftcardpin</span><span class="sxs-lookup"><span data-stu-id="ca8df-233">giftcardpin</span></span>                    | <span data-ttu-id="ca8df-234">หมายเลขรหัสประจำตัวของบัตรของขวัญ สำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="ca8df-234">The personal identification number (PIN) of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="ca8df-235">(ตัวยึดตำแหน่งนี้จะใช้กับบัตรของขวัญภายนอกโดยเฉพาะ)</span><span class="sxs-lookup"><span data-stu-id="ca8df-235">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="ca8df-236">giftcardexpiration</span><span class="sxs-lookup"><span data-stu-id="ca8df-236">giftcardexpiration</span></span>             | <span data-ttu-id="ca8df-237">วันหมดอายุของบัตรของขวัญ สำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="ca8df-237">The expiration date of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="ca8df-238">(ตัวยึดตำแหน่งนี้จะใช้กับบัตรของขวัญภายนอกโดยเฉพาะ)</span><span class="sxs-lookup"><span data-stu-id="ca8df-238">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="ca8df-239">giftcardrecipientname</span><span class="sxs-lookup"><span data-stu-id="ca8df-239">giftcardrecipientname</span></span>          | <span data-ttu-id="ca8df-240">ชื่อของผู้รับบัตรของขวัญ สำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="ca8df-240">The name of the gift card recipient, for products of the gift card type.</span></span> |
| <span data-ttu-id="ca8df-241">giftcardbuyername</span><span class="sxs-lookup"><span data-stu-id="ca8df-241">giftcardbuyername</span></span>              | <span data-ttu-id="ca8df-242">ชื่อของผู้ซื้อบัตรของขวัญ สำหรับผลิตภัณฑ์ของชนิดบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="ca8df-242">The name of the gift card buyer, for products of the gift card type.</span></span> |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a><span data-ttu-id="ca8df-243">รูปแบบของตัวยึดบรรทัดใบสั่งในเนื้อหาของข้อความอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-243">Format of order line placeholders in the email message body</span></span>

<span data-ttu-id="ca8df-244">เมื่อคุณสร้าง HTML สำหรับบรรทัดใบสั่งแต่ละบรรทัดในเนื้อหาของข้อความอีเมล ให้ใช้บล็อกที่ซ้ำกันของ HTML และตัวยึดสำหรับบรรทัดที่มีตัวยึดตำแหน่งต่อไปนี้ที่จะใส่ไว้ภายในแท็กข้อคิดเห็นของ HTML</span><span class="sxs-lookup"><span data-stu-id="ca8df-244">When you create the HTML for the individual order lines in the email message body, surround the repeating block of HTML and placeholders for the lines with the following placeholders that are put inside HTML comment tags.</span></span>

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

<span data-ttu-id="ca8df-245">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ca8df-245">Here is an example.</span></span>

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

## <a name="create-a-template-for-emailed-receipts"></a><span data-ttu-id="ca8df-246">สร้างเท็มเพลตสำหรับใบเสร็จรับเงินที่ส่งทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-246">Create a template for emailed receipts</span></span>

<span data-ttu-id="ca8df-247">ใบเสร็จรับเงินสามารถส่งอีเมลถึงลูกค้าที่ทำการซื้อสินค้าที่การขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="ca8df-247">Receipts can be emailed to customers who make purchases at a retail point of sale (POS).</span></span> <span data-ttu-id="ca8df-248">โดยทั่วไปขั้นตอนสำหรับการสร้างเท็มเพลตใบเสร็จรับเงินที่ส่งทางอีเมลนั้นจะเหมือนกับขั้นตอนสำหรับการสร้างเท็มเพลตสำหรับเหตุการณ์ของธุรกรรมอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="ca8df-248">In general, the steps for creating the emailed receipt template are the same as the steps for creating templates for other transactional events.</span></span> <span data-ttu-id="ca8df-249">อย่างไรก็ตามต้องมีการเปลี่ยนแปลงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ca8df-249">However, the following changes are required:</span></span>

- <span data-ttu-id="ca8df-250">รหัสอีเมลของเท็มเพลตอีเมลจะต้องเป็น **emailRecpt**</span><span class="sxs-lookup"><span data-stu-id="ca8df-250">The email ID of the email template must be **emailRecpt**.</span></span>
- <span data-ttu-id="ca8df-251">ข้อความของใบเสร็จถูกแทรกลงในอีเมลโดยใช้ตัวยึด **%message%**</span><span class="sxs-lookup"><span data-stu-id="ca8df-251">The text of the receipt is inserted into the email by using the **%message%** placeholder.</span></span> <span data-ttu-id="ca8df-252">เมื่อต้องการตรวจสอบให้แน่ใจว่ามีการแสดงเนื้อหาของใบเสร็จอย่างถูกต้อง ให้ล้อมรอบตัวยึด **%message%** ด้วยแท็ก HTML **&lt;pre&gt;** และ **&lt;/pre&gt;**</span><span class="sxs-lookup"><span data-stu-id="ca8df-252">To ensure that the receipt body is correctly rendered, surround the **%message%** placeholder with HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tags.</span></span>
- <span data-ttu-id="ca8df-253">การแบ่งบรรทัดใน HTML สำหรับส่วนหัวและส่วนท้ายของอีเมลจะถูกแปลงเป็นแท็ก HTML **&lt;br /&gt;** เพื่อให้เนื้อหาของใบเสร็จแสดงผลได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ca8df-253">Line breaks in the HTML for the header and footer of the email are converted to HTML **&lt;br /&gt;** tags so that the receipt body is rendered correctly.</span></span> <span data-ttu-id="ca8df-254">ถ้าต้องการกำจัดพื้นที่แนวตั้งที่ไม่พึงประสงค์ในอีเมลใยเสร็จรับเงินของคุณ ให้ลบตัวแบ่งบรรทัดออกจากพื้นที่ใดๆ ใน HTML ซึ่งไม่จำเป็นต้องใช้พื้นที่แนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="ca8df-254">To eliminate unwanted vertical space in your receipt emails, remove line breaks from any place in the HTML where vertical space isn't required.</span></span>

<span data-ttu-id="ca8df-255">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนดค่าใบเสร็จทางอีเมล ดูที่ [กำหนดค่าใบเสร็จทางอีเมล](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)</span><span class="sxs-lookup"><span data-stu-id="ca8df-255">For more information about how to configure email receipts, see [Set up email receipts](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts).</span></span>

## <a name="upload-the-email-html"></a><span data-ttu-id="ca8df-256">อัปโหลด HTML ของอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-256">Upload the email HTML</span></span>

<span data-ttu-id="ca8df-257">หลังจากที่คุณได้สร้างและทดสอบ HTML สำหรับเนื้อหาของข้อความของคุณแล้ว คุณต้องอัปโหลด HTML ไปที่ศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="ca8df-257">After you've created and tested the HTML for your message body, it must be uploaded to Commerce headquarters.</span></span> <span data-ttu-id="ca8df-258">ในขณะนี้ไม่สามารถส่งออกอีเมล HTML ได้</span><span class="sxs-lookup"><span data-stu-id="ca8df-258">Currently, email HTML can't be exported.</span></span> <span data-ttu-id="ca8df-259">ดังนั้นคุณต้องรักษาสำเนาของหลักของ HTML ภายนอกศูนย์ควบคุม Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ca8df-259">Therefore, you must maintain the master copy of your HTML outside Commerce headquarters.</span></span>

<span data-ttu-id="ca8df-260">เมื่อต้องการอัปโหลด HTML เท็มเพลตอีเมลใหม่หรือที่แก้ไข ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ca8df-260">To upload a new or edited email template HTML, follow these steps.</span></span>

1. <span data-ttu-id="ca8df-261">ในศูนย์ควบคุมของ Commerce ให้ไปที่ **การขายปลีกและ Commerce \> การตั้งค่าศูนย์ควบคุม \> เท็มเพลตอีเมลขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="ca8df-261">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="ca8df-262">เลือกแถวสำหรับภาษาที่คุณต้องการเพิ่มหรือแทนที่ HTML</span><span class="sxs-lookup"><span data-stu-id="ca8df-262">Select the row for the language that you want to add or replace HTML for.</span></span> <span data-ttu-id="ca8df-263">อีกทางหนึ่งคือเลือก **สร้าง** เพื่อสร้างแถวสำหรับภาษาใหม่</span><span class="sxs-lookup"><span data-stu-id="ca8df-263">Alternatively, select **New** to create a row for a new language.</span></span>
1. <span data-ttu-id="ca8df-264">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="ca8df-264">Select **Edit**.</span></span>
1. <span data-ttu-id="ca8df-265">ในกล่องโต้ตอบที่ปรากฏ เลือก **เรียกดู**</span><span class="sxs-lookup"><span data-stu-id="ca8df-265">In the dialog box that appears, select **Browse**.</span></span> <span data-ttu-id="ca8df-266">เรียกดูเอกสาร HTML ที่คุณต้องการอัปโหลด เลือกเอกสาร แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="ca8df-266">Browse to the HTML document that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="ca8df-267">เลือก **อัปโหลด**</span><span class="sxs-lookup"><span data-stu-id="ca8df-267">Select **Upload**.</span></span>
1. <span data-ttu-id="ca8df-268">หลังจากที่ HTML ของอีเมลของคุณปรากฏในหน้าต่างแสดงตัวอย่าง ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ca8df-268">After your email HTML appears in the preview window, select **OK**.</span></span>
1. <span data-ttu-id="ca8df-269">ตรวจสอบให้แน่ใจว่ามีการเลือกกล่องกาเครื่องหมาย **มีเนื้อหา** สำหรับแถว</span><span class="sxs-lookup"><span data-stu-id="ca8df-269">Make sure that the **Has body** check box is selected for the row.</span></span>

<span data-ttu-id="ca8df-270">ถ้าคุณได้ตั้งกำหนดค่าศูนย์ควบคุม Commerce ไว้แล้วเพื่อส่งอีเมล อีเมลใหม่หรือที่อัปเดตแล้วของคุณจะถูกส่งไปยังลูกค้าทั้งหมดที่ทำธุรกรรมที่เรียกใช้เหตุการณ์ที่ถูกแม็ปกับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="ca8df-270">If you've already configured Commerce headquarters to send email, your new or updated email will be sent to all customers who perform a transaction that invokes the event that is mapped to the template.</span></span>

<span data-ttu-id="ca8df-271">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนดค่าอีเมลใน Dynamics 365 Commerce ดูที่ [กำหนดค่าและส่งอีเมล](../fin-ops-core/fin-ops/organization-administration/configure-email.md)</span><span class="sxs-lookup"><span data-stu-id="ca8df-271">For more information about how to configure emails in Dynamics 365 Commerce, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca8df-272">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ca8df-272">Additional resources</span></span> 

[<span data-ttu-id="ca8df-273">ตั้งค่าโพรไฟล์การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-273">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="ca8df-274">ตั้งค่าคอนฟิกและส่งอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-274">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[<span data-ttu-id="ca8df-275">ตั้งค่าใบเสร็จทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="ca8df-275">Set up email receipts</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[<span data-ttu-id="ca8df-276">ส่งใบเสร็จทางอีเมลจาก Modern POS</span><span class="sxs-lookup"><span data-stu-id="ca8df-276">Send email receipts from Modern POS </span></span>](email-receipts.md)
