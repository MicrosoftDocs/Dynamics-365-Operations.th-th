---
title: กำหนดอีเมลของธุรกรรมตามวิธีการจัดส่ง
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าเท็มเพลตอีเมลที่กำหนดเองสำหรับชนิดการแจ้งเตือนและวิธีการจัดส่งที่เฉพาะเจาะจงใน Microsoft Dynamics 365 Commerce
author: stuharg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 411e694b33e0443a336f6a8cdad78714630e4bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799384"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="76e83-103">ปรับแต่งอีเมลของธุรกรรมตามวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="76e83-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="76e83-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าเท็มเพลตอีเมลที่กำหนดเองสำหรับชนิดการแจ้งเตือนและวิธีการจัดส่งที่เฉพาะเจาะจงใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="76e83-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="76e83-105">ตอนนี้อีเมลของธุรกรรมสามารถกำหนดเองได้สำหรับการรวมกันของชนิดการแจ้งเตือน (ตัวอย่างเช่น **ใบสั่งที่สร้าง** **ใบสั่งที่บรรจุ** หรือ  **ใบสั่งที่ออกใบแจ้งหนี้แล้ว**) และวิธีการจัดส่ง (ตัวอย่างเช่น ข้ามคืน การรับสินค้าในร้านค้า หรือการรับสินค้าหน้าร้านค้า)</span><span class="sxs-lookup"><span data-stu-id="76e83-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="76e83-106">อีเมล์ธุรกรรมที่กำหนดเองช่วยให้ร้านค้าปลีกสามารถให้คำสั่งของลูกค้าของตนมีประสบการณ์การทำงานที่เหมาะสมกับวิธีการจัดส่งของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="76e83-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="76e83-107">ตัวอย่างเช่น เหตุการณ์ "ใบสั่งบรรจุ" สามารถกำหนดเองเพื่อให้มีคำแนะนำในการรับสินค้าหน้าร้าน สำหรับลูกค้าที่เลือกรับสินค้าหน้าร้าน</span><span class="sxs-lookup"><span data-stu-id="76e83-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="76e83-108">อีกทางหนึ่งคือ ผู้ขนส่งและข้อมูลการจัดส่งสำหรับลูกค้าที่เลือกว่าจะจัดส่งสินค้าตามใบสั่งซื้อไปให้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="76e83-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="76e83-109">เมื่อต้องการใช้ฟังก์ชันสำหรับอีเมล์ธุรกรรมที่กำหนดเอง คุณต้องเปิดใช้งานคุณลักษณะ **การกำหนดเท็มเพลตอีเมลธุรกรรมตามโหมดการจัดส่ง** โดยไปที่ **พื้นที่ทำงาน \> การจัดการคุณลักษณะ** ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="76e83-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="76e83-110">อีเมลอาจถูกปรับแต่งตามวิธีการจัดส่งสำหรับชนิดการแจ้งเตือนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="76e83-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="76e83-111">**การยกเลิกใบสั่ง** – ชนิดการแจ้งเตือนทางอีเมลนี้เป็นชนิดใหม่</span><span class="sxs-lookup"><span data-stu-id="76e83-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="76e83-112">**สร้างใบสั่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="76e83-112">**Order created**</span></span>
- <span data-ttu-id="76e83-113">**ยืนยันใบสั่งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="76e83-113">**Order confirmed**</span></span>
- <span data-ttu-id="76e83-114">**ใบแจ้งหนี้ใบสั่ง** – ชนิดการแจ้งเตือนทางอีเมลนี้เป็นชนิดใหม่</span><span class="sxs-lookup"><span data-stu-id="76e83-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="76e83-115">คุณสามารถใช้แทนชนิดของการแจ้งเตือน **การจัดส่งสินค้าตามใบสั่ง** ที่จะส่งการแจ้งเตือนสำหรับเหตุการณ์ใบแจ้งหนี้ที่มีวิธีการจัดส่งของการจัดส่ง (ไม่ใช่การเบิกสินค้า การดำเนินการ หรือโหมดอิเล็กทรอนิกส์ของการจัดส่ง)</span><span class="sxs-lookup"><span data-stu-id="76e83-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="76e83-116">**การเบิกสินค้าตามใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="76e83-116">**Order picked**</span></span>
- <span data-ttu-id="76e83-117">**ใบสั่งที่บรรจุ**</span><span class="sxs-lookup"><span data-stu-id="76e83-117">**Order packed**</span></span>
- <span data-ttu-id="76e83-118">**ใบสั่งที่พร้อมสำหรับการเบิกสินค้า** – ชนิดการแจ้งเตือนนี้สามารถกำหนดตามวิธีการจัดส่งได้เฉพาะเมื่อคุณลักษณะ **สนับสนุนสำหรับคุณลักษณะการจัดส่งสินค้าในการจัดส่งหลายครั้ง** มีการเปิดใช้งานการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="76e83-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="76e83-119">ในกรณีนี้ ชนิดการแจ้งเตือนนี้มีหน้าที่เทียบเท่ากับชนิดของการแจ้งเตือน **ใบสั่งที่บรรจุ**</span><span class="sxs-lookup"><span data-stu-id="76e83-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="76e83-120">**การชำระเงินล้มเหลว**</span><span class="sxs-lookup"><span data-stu-id="76e83-120">**Payment failed**</span></span>
- <span data-ttu-id="76e83-121">**สร้างใบสั่งเปลี่ยนสินค้าแล้ว**</span><span class="sxs-lookup"><span data-stu-id="76e83-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="76e83-122">ตั้งค่าคอนฟิกเท็มเพลตอีเมลสำหรับการจัดส่งเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="76e83-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="76e83-123">สำหรับขั้นตอนนี้ สมมติฐานคือคุณสร้างเท็มเพลตอีเมลที่กำหนดเองใหม่ของคุณใหม่ และเพิ่มเท็มเพลตในหน้า **เท็มเพลตอีเมลขององค์กรแล้ว**</span><span class="sxs-lookup"><span data-stu-id="76e83-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="76e83-124">สำหรับข้อมูลเกี่ยวกับวิธีการสร้างและการอัปโหลดเท็มเพลตอีเมล โปรดดูที่ [การสร้างเท็มเพลตอีเมล์สำหรับเหตุการณ์ธุรกรรม](email-templates-transactions.md)</span><span class="sxs-lookup"><span data-stu-id="76e83-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="76e83-125">เมื่อต้องการตั้งค่าคอนฟิกเท็มเพลตอีเมลสำหรับการจัดส่งที่เฉพาะเจาะจงในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="76e83-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="76e83-126">ไปที่ **โพรไฟล์การแจ้งเตือนทางอีเมลของ Commerce**</span><span class="sxs-lookup"><span data-stu-id="76e83-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="76e83-127">ภายใต้ **การตั้งค่าการแจ้งเตือนเหตุการณ์การขายปลีก** ให้เลือกชนิดของการแจ้งเตือนที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="76e83-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="76e83-128">ในขณะที่ชนิดการแจ้งเตือนยังคงถูกเลือกอยู่ ให้เลือก **ตั้งค่าคอนฟิกวิธีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="76e83-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="76e83-129">ในกล่องโต้ตอบ **วิธีการจัดส่ง** เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="76e83-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="76e83-130">ในแถวใหม่ ในฟิลด์ **วิธีการจัดส่ง** เลือกวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="76e83-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="76e83-131">ในฟิลด์ **รหัสอีเมล์** เลือกเท็มเพลตอีเมลเพื่อแม็ปกับวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="76e83-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="76e83-132">เลือกกล่องกาเครื่องหมาย **ใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="76e83-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="76e83-133">ทำซ้ำขั้นตอนที่ 4 ถึง 7 เพื่อเพิ่มวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="76e83-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="76e83-134">เมื่อคุณได้ทำเสร็จสิ้นแล้ว เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="76e83-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="76e83-135">เมื่อมีการจัดส่งสินค้ามากกว่าหนึ่งโหมดอยู่ระหว่างรายการในใบสั่งขาย จะมีการใช้เท็มเพลตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="76e83-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="76e83-136">เท็มเพลตเริ่มต้นคือเท็มเพลตที่แม็ปกับชนิดของการแจ้งเตือนบนหน้า **โพรไฟล์การแจ้งเตือนทางอีเมลของ Commerce**</span><span class="sxs-lookup"><span data-stu-id="76e83-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="76e83-137">ถ้าใบสั่งขายมีวิธีการจัดส่งที่ยังไม่ได้ตั้งค่าคอนฟิกสำหรับเท็มเพลตอีเมลที่กำหนดเอง จะมีการใช้เท็มเพลตอีเมล์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="76e83-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="76e83-138">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="76e83-138">Additional resources</span></span>

[<span data-ttu-id="76e83-139">สร้างใบสั่งของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="76e83-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="76e83-140">เปลี่ยนวิธีการจัดส่งใน POS</span><span class="sxs-lookup"><span data-stu-id="76e83-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]