---
title: ฝังแอปของบุคคลที่สาม
description: หัวข้อนี้อธิบายวิธีการฝังแอปของบุคคลที่สามเพื่อเสริมฟังก์ชันของผลิตภัณฑ์
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d348683e0a2ed35f26830a6ce05c0bf9ca5970bd
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944860"
---
# <a name="embed-third-party-apps"></a><span data-ttu-id="adac3-103">ฝังแอปของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="adac3-103">Embed third-party apps</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="adac3-104">ลูกค้าหลายคนใช้ช่วงของแอปพลิเคชันเพื่อรันธุรกิจของตน</span><span class="sxs-lookup"><span data-stu-id="adac3-104">Many customers use a range of applications to run their business.</span></span> <span data-ttu-id="adac3-105">แอปพลิเคชันเหล่านั้นบางรายการเป็นแอปเว็บของบุคคลที่สามที่ร่วมกับแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adac3-105">Some of those applications are third-party web apps that work in conjunction with Finance and Operations apps.</span></span> <span data-ttu-id="adac3-106">เพื่อให้ประสบการณ์ของผู้ใช้ที่ต่อเนื่องมากขึ้น คุณสามารถใช้คุณลักษณะ **แอปแบบเต็มหน้า (พรีวิว)** เพื่อฝังแอปของบุคคลที่สามเหล่านั้นลงในแอป Finance and Operations ของคุณโดยตรง (หากแอปของบุคคลที่สามอนุญาตให้ฝังตัวเองอยู่ได้)</span><span class="sxs-lookup"><span data-stu-id="adac3-106">To provide a more seamless user experience, you can use the **(Preview) Full page apps** feature to embed those third-party apps directly into your Finance and Operations apps (provided that the third-party apps allow themselves to be embedded).</span></span> <span data-ttu-id="adac3-107">ด้วยวิธีนี้ ผู้ใช้สามารถเข้าถึงเว็บไซต์และแอปที่ต้องการโดยไม่ต้องสลับแท็บหรือหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="adac3-107">In this way, users can access the websites and apps that they require without having to switch tabs or windows.</span></span>

<span data-ttu-id="adac3-108">ก่อนที่คุณจะสามารถฝังแอปของบุคคลที่สามลงในผลิตภัณฑ์ได้ คุณต้องเปิดคุณลักษณะ **แอปแบบเต็มหน้า (พรีวิว)** ในการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="adac3-108">Before you can embed third-party apps into the product, you must turn on the **(Preview) Full page apps** feature in Feature management.</span></span> <span data-ttu-id="adac3-109">จากนั้น คุณสามารถใช้วิธีใดวิธีหนึ่งต่อไปนี้เพื่อฝังแอปหรือเว็บไซต์ของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="adac3-109">You can then use one of the following methods to embed a third-party app or website.</span></span> <span data-ttu-id="adac3-110">วิธีการเหล่านี้คล้ายคลึงกับวิธีการที่ใช้ในการฝังแอปพื้นที่ทำงานจาก Microsoft Power Apps ลงในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adac3-110">These methods are analogous to the methods that are used to embed canvas apps from Microsoft Power Apps into Finance and Operations apps.</span></span>

- <span data-ttu-id="adac3-111">ฝังแอปหรือเว็บไซต์ในหน้าที่มีอยู่เป็นหน้าแท็บใหม่ (แท็บ Pivot, FastTab, เบลด หรือส่วนพื้นที่ทำงาน)</span><span class="sxs-lookup"><span data-stu-id="adac3-111">Embed the app or website on an existing page as a new tab page (pivot tab, FastTab, blade, or workspace section).</span></span>
- <span data-ttu-id="adac3-112">สร้างประสบการณ์การใช้งานแอปหรือเว็บไซต์แบบเต็มหน้าใหม่จากแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="adac3-112">Create a new full-page experience for the app or website from the dashboard.</span></span>

## <a name="embed-a-website-on-an-existing-page"></a><span data-ttu-id="adac3-113">ฝังเว็บไซต์ในหน้าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="adac3-113">Embed a website on an existing page</span></span>

<span data-ttu-id="adac3-114">ใช้กระบวนงานนี้ ถ้าคุณต้องการเพิ่มเติมหน้าที่มีอยู่ในระบบที่มีแอปที่ฝังอยู่</span><span class="sxs-lookup"><span data-stu-id="adac3-114">Use this procedure if you want to supplement an existing page in the system with an embedded app.</span></span>

1. <span data-ttu-id="adac3-115">เปิดหน้าที่คุณต้องการฝังแอป</span><span class="sxs-lookup"><span data-stu-id="adac3-115">Open the page where you want to embed the app.</span></span>
2. <span data-ttu-id="adac3-116">เปิดบานหน้าต่าง **เพิ่มแอป**:</span><span class="sxs-lookup"><span data-stu-id="adac3-116">Open the **Add an app** pane:</span></span>

    1. <span data-ttu-id="adac3-117">เลือก **การตั้งค่า** และจากนั้น **กำหนดเป็นแบบส่วนบุคคล** เพื่อเปิดแถบเครื่องมือ **การกำหนดเป็นแบบส่วนบุคคล**</span><span class="sxs-lookup"><span data-stu-id="adac3-117">Select **Settings** and then **Personalize** to open the **Personalization** toolbar.</span></span>
    2. <span data-ttu-id="adac3-118">เลือก **เพิ่มเติม \> เพิ่มแอป**</span><span class="sxs-lookup"><span data-stu-id="adac3-118">Select **More \> Add an app**.</span></span>

3. <span data-ttu-id="adac3-119">เลือกขอบเขตของหน้าที่คุณต้องการเพิ่มแอป</span><span class="sxs-lookup"><span data-stu-id="adac3-119">Select the region of the page where you want to add the app.</span></span> <span data-ttu-id="adac3-120">ขอบเขตนี้ต้องเป็น *คอนเทนเนอร์แท็บ* สำหรับแท็บ Pivot, FastTab, เบลด หรือส่วนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="adac3-120">This region must be a *tab container* for a pivot tab, FastTab, blade, or workspace section.</span></span>
4. <span data-ttu-id="adac3-121">เลือก **เว็บไซต์**</span><span class="sxs-lookup"><span data-stu-id="adac3-121">Select **Website**.</span></span>
5. <span data-ttu-id="adac3-122">กำหนดค่าแอปที่ฝังไว้:</span><span class="sxs-lookup"><span data-stu-id="adac3-122">Configure the embedded app:</span></span>

    - <span data-ttu-id="adac3-123">**ชื่อ** – ป้อนข้อความที่ควรแสดงไว้สำหรับแท็บที่มีแอปที่ฝังอยู่</span><span class="sxs-lookup"><span data-stu-id="adac3-123">**Name** – Enter the text that should be shown for the tab that contains the embedded app.</span></span> <span data-ttu-id="adac3-124">บ่อยครั้งที่คุณจะต้องการให้ข้อความนี้เป็นชื่อของแอป</span><span class="sxs-lookup"><span data-stu-id="adac3-124">Often, you will want this text to be the name of the app.</span></span>
    - <span data-ttu-id="adac3-125">**URL** – ระบุที่ตั้งของแอป</span><span class="sxs-lookup"><span data-stu-id="adac3-125">**URL** – Specify the location of the app.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="adac3-126">เพื่อเหตุผลด้านความปลอดภัย URL ต้องใช้ Hypertext Transfer Protocol Secure (HTTPS)</span><span class="sxs-lookup"><span data-stu-id="adac3-126">For security reasons, the URL must use Hypertext Transfer Protocol Secure (HTTPS).</span></span>
    > - <span data-ttu-id="adac3-127">ต้องตั้งค่าคอนฟิกแอปหรือเว็บไซต์เพื่ออนุญาตให้ฝังตัวเองได้</span><span class="sxs-lookup"><span data-stu-id="adac3-127">The app or website must be configured to allow itself to be embedded.</span></span>

6. <span data-ttu-id="adac3-128">เลือก **บันทึก** เพื่อฝังแอปบนหน้า</span><span class="sxs-lookup"><span data-stu-id="adac3-128">Select **Save** to embed the app on the page.</span></span> <span data-ttu-id="adac3-129">แอปนี้จะถูกเพิ่มเป็นแท็บหรือส่วนสุดท้ายในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="adac3-129">The app is added as the last tab or section in the group.</span></span>
7. <span data-ttu-id="adac3-130">ยืนยันว่าแอปปรากฏตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="adac3-130">Confirm that the app appears as expected.</span></span> <span data-ttu-id="adac3-131">ถ้าแอปไม่แสดง ให้ดูส่วน [การแก้ไขปัญหาเบื้องต้น](#troubleshooting) ในหัวข้อนี้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="adac3-131">If the app isn't rendered, see the [Troubleshooting](#troubleshooting) section later in this topic.</span></span>
8. <span data-ttu-id="adac3-132">เปิดตัวเลือกมุมมอง แล้วเลือก **บันทึก** (ถ้าควรเชื่อมโยงแอปกับมุมมองปัจจุบัน) หรือ **บันทึกเป็น** (เพื่อบันทึกแอปไปที่มุมมองอื่น)</span><span class="sxs-lookup"><span data-stu-id="adac3-132">Open the view selector, and select either **Save** (if the app should be associated with the current view) or **Save as** (to save the app to a different view).</span></span>

    <span data-ttu-id="adac3-133">ถ้าหน้าไม่มีตัวเลือกมุมมอง (ตัวอย่างเช่น ถ้าหน้าเป็นกล่องโต้ตอบหรือพื้นที่ทำงาน) คุณสามารถข้ามขั้นตอนนี้ได้</span><span class="sxs-lookup"><span data-stu-id="adac3-133">If the page doesn't have a view selector (for example, if the page is a dialog box or a workspace), you can skip this step.</span></span>

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a><span data-ttu-id="adac3-134">ฝังเว็บไซต์เป็นประสบการณ์แบบเต็มหน้าจากแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="adac3-134">Embed a website as a full-page experience from the dashboard</span></span>

<span data-ttu-id="adac3-135">ใช้กระบวนงานนี้ ถ้าแอปที่คุณต้องการฝังไม่เกี่ยวข้องกับหน้าที่มีอยู่ หรือถ้าคุณเพียงต้องการประสบการณ์แบบเต็มหน้าสำหรับแอปภายในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adac3-135">Use this procedure if the app that you want to embed isn't related to an existing page, or if you just want a full-page experience for the app inside the Finance and Operations app.</span></span>

1. <span data-ttu-id="adac3-136">เปิดแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="adac3-136">Open the dashboard.</span></span>
2. <span data-ttu-id="adac3-137">เลือกหน้าค้างไว้ (หรือคลิกขวา) เลือก **กำหนดเป็นแบบส่วนบุคคล** แล้วจากนั้น เลือก **เพิ่มหน้า**</span><span class="sxs-lookup"><span data-stu-id="adac3-137">Select and hold (or right-click) the page, select **Personalize**, and then select **Add a page**.</span></span>
3. <span data-ttu-id="adac3-138">ในบานหน้าต่าง **เพิ่มหน้า** ให้เลือก **เว็บไซต์**</span><span class="sxs-lookup"><span data-stu-id="adac3-138">In the **Add a page** pane, select **Website**.</span></span>
4. <span data-ttu-id="adac3-139">กำหนดค่าแอปที่ฝังไว้:</span><span class="sxs-lookup"><span data-stu-id="adac3-139">Configure the embedded app:</span></span>

    - <span data-ttu-id="adac3-140">**ชื่อ** – ป้อนข้อความที่ควรแสดงบนไทล์ที่เพิ่มไว้ให้สำหรับแอปแบบฝังบนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="adac3-140">**Name** – Enter the text that should be shown on the tile that is added for the embedded app on the dashboard.</span></span> <span data-ttu-id="adac3-141">บ่อยครั้งที่คุณจะต้องการให้ข้อความนี้เป็นชื่อของแอป</span><span class="sxs-lookup"><span data-stu-id="adac3-141">Often, you will want this text to be the name of the app.</span></span>
    - <span data-ttu-id="adac3-142">**URL** – ระบุที่ตั้งของแอป</span><span class="sxs-lookup"><span data-stu-id="adac3-142">**URL** – Specify the location of the app.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="adac3-143">เพื่อเหตุผลด้านความปลอดภัย URL ต้องใช้ HTTPS</span><span class="sxs-lookup"><span data-stu-id="adac3-143">For security reasons, the URL must use HTTPS.</span></span>
    > - <span data-ttu-id="adac3-144">ต้องตั้งค่าคอนฟิกแอปหรือเว็บไซต์เพื่ออนุญาตให้ฝังตัวเองได้</span><span class="sxs-lookup"><span data-stu-id="adac3-144">The app or website must be configured to allow itself to be embedded.</span></span>

5. <span data-ttu-id="adac3-145">เลือก **บันทึก** เพื่อเพิ่มแอปลงในแดชบอร์ดเป็นไทล์ใหม่</span><span class="sxs-lookup"><span data-stu-id="adac3-145">Select **Save** to add the app to the dashboard as a new tile.</span></span>
6. <span data-ttu-id="adac3-146">เลือกไทล์ใหม่บนแดชบอร์ด และยืนยันว่าแอปปรากฏตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="adac3-146">Select the new tile on the dashboard, and confirm that the app appears as expected.</span></span> <span data-ttu-id="adac3-147">ถ้าแอปไม่แสดง ให้ดูส่วน [การแก้ไขปัญหาเบื้องต้น](#troubleshooting) ในหัวข้อนี้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="adac3-147">If the app isn't rendered, see the [Troubleshooting](#troubleshooting) section later in this topic.</span></span>

## <a name="sharing-embedded-apps"></a><span data-ttu-id="adac3-148">การใช้แอปที่ฝังไว้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="adac3-148">Sharing embedded apps</span></span>

<span data-ttu-id="adac3-149">หลังจากที่คุณฝังแอปโดยใช้วิธีใดวิธีหนึ่งที่อธิบายไว้ในส่วนก่อนหน้านี้ คุณอาจต้องการแบ่งปันมุมมองนั้นกับผู้ใช้รายอื่นในระบบ</span><span class="sxs-lookup"><span data-stu-id="adac3-149">After you've embedded an app by using one of the methods that are described in the previous sections, you might want to share the view with other users in the system.</span></span> <span data-ttu-id="adac3-150">เมื่อต้องการใช้แอปที่ฝังอยู่ร่วมกัน ให้ใช้วิธีการใดวิธีการหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="adac3-150">To share an embedded app, use one of the following methods:</span></span>

- <span data-ttu-id="adac3-151">**เผยแพร่มุมมอง (แนะนำ):** ถ้ามีการบันทึกแอปที่ฝังอยู่ลงในมุมมองแล้ว วิธีการที่แนะนาและที่ต้องการในการใช้ร่วมกันคือ การเผยแพร่มุมมองไปยังผู้ใช้ที่มีบทบาทความปลอดภัยที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="adac3-151">**Publish the view (Recommended):** If the embedded app has been saved to a view, the recommended and preferred way to share it is to publish the view to users who have the appropriate security roles.</span></span> <span data-ttu-id="adac3-152">จากนั้น ผู้ใช้ทั้งหมดที่มีบทบาทความปลอดภัยที่กำหนดเป้าหมายโดยมุมมองที่เผยแพร่ จะเห็นแอปในแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="adac3-152">Then, all users who have the security roles that are targeted by the published view will see the app in Finance and Operations apps.</span></span> <span data-ttu-id="adac3-153">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเผยแพร่มุมมอง ดู [การเผยแพร่มุมมอง](saved-views.md#publishing-views)</span><span class="sxs-lookup"><span data-stu-id="adac3-153">For more information about how to publish a view, see [Publishing views](saved-views.md#publishing-views).</span></span>

    <span data-ttu-id="adac3-154">นอกจากนี้ คุณยังสามารถเผยแพร่แอปที่ถูกฝังอยู่เป็นประสบการณ์แบบเต็มหน้าจากแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="adac3-154">You can also publish an app that has been embedded as a full-page experience from the dashboard.</span></span> <span data-ttu-id="adac3-155">บนแดชบอร์ด ให้เลือกไทล์ที่เชื่อมโยงกับแอปค้างไว้ (หรือคลิกขวา) เลือก **กำหนดเป็นแบบส่วนบุคคล** แล้วจากนั้น เลือก **เผยแพร่หน้า**</span><span class="sxs-lookup"><span data-stu-id="adac3-155">On the dashboard, select and hold (or right-click) the tile that is associated with the app, select **Personalize**, and then select **Publish page**.</span></span> <span data-ttu-id="adac3-156">ในขณะนี้ คุณสามารถเผยแพร่ไปยังบทบาทความปลอดภัยได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="adac3-156">Currently, you can publish only to security roles.</span></span> <span data-ttu-id="adac3-157">อย่างไรก็ตาม ความสามารถที่จะเผยแพร่ไปยังนิติบุคคลจะถูกเพิ่ม ก่อนที่คุณลักษณะจะพร้อมใช้งานโดยทั่วไป</span><span class="sxs-lookup"><span data-stu-id="adac3-157">However, the capability to publish to legal entities will be added before the feature becomes generally available.</span></span>

- <span data-ttu-id="adac3-158">**คัดลอกการกำหนดเป็นแบบส่วนบุคคล:** สําหรับหน้าที่ไม่สนับสนุนมุมมอง (ตัวอย่างเช่น กล่องโต้ตอบ หรือพื้นที่เก็บงาน) หรือเพื่อประสบการณ์การแอปแบบเต็มหน้า คุณสามารถคัดลอกการกำหนดเป็นแบบส่วนบุคคลไปยังผู้ใช้ที่เหมาะสมได้</span><span class="sxs-lookup"><span data-stu-id="adac3-158">**Copy the personalization:** For pages that don't support views (for example, dialog boxes or workspaces), or for the full-page app experience, you can copy the personalization to the appropriate users.</span></span> <span data-ttu-id="adac3-159">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การตั้งค่าส่วนบุคคลที่ใช้ร่วมกัน](personalize-user-experience.md#sharing-personalizations)</span><span class="sxs-lookup"><span data-stu-id="adac3-159">For more information, see [Sharing personalizations](personalize-user-experience.md#sharing-personalizations).</span></span>

## <a name="viewing-embedded-apps"></a><span data-ttu-id="adac3-160">การดูแอปที่ฝังไว้</span><span class="sxs-lookup"><span data-stu-id="adac3-160">Viewing embedded apps</span></span>

<span data-ttu-id="adac3-161">ในการดูแอปที่ฝังในหน้าในแอป Finance and Operations ให้เปิดหน้าที่มีแอปที่ฝังไว้</span><span class="sxs-lookup"><span data-stu-id="adac3-161">To view an embedded app on a page in Finance and Operations apps, open the page that has the embedded app.</span></span> <span data-ttu-id="adac3-162">โปรดจำไว้ว่า บนหน้าบางหน้า แอปที่ฝังไว้สามารถเข้าถึงได้โดยใช้ปุ่ม **Power Apps** ในบานหน้าต่างการดำเนินการมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="adac3-162">Remember that, on some pages, embedded apps can be accessed by using the **Power Apps** button on the standard Action Pane.</span></span> <span data-ttu-id="adac3-163">อีกทางเลือกหนึ่ง อาจปรากฎบนหน้าโดยตรงเป็นแท็บใหม่, FastTab หรือเบลด หรือเป็นส่วนใหม่ในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="adac3-163">Alternatively, they might appear directly on the page as a new tab, FastTab, or blade, or as a new section in a workspace.</span></span>

## <a name="editing-or-removing-embedded-apps"></a><span data-ttu-id="adac3-164">การแก้ไขหรือการลบแอปที่ฝังอยู่</span><span class="sxs-lookup"><span data-stu-id="adac3-164">Editing or removing embedded apps</span></span>

<span data-ttu-id="adac3-165">หลังจากที่ฝังแอปบนหน้าแล้ว คุณอาจต้องแก้ไขการตั้งค่าคอนฟิกของแอปนั้น (ตัวอย่างเช่น โดยการเปลี่ยนป้ายชื่อส่วนหรือ URL)</span><span class="sxs-lookup"><span data-stu-id="adac3-165">After an app has been embedded on a page, you might have to edit its configuration (for example, by changing the section label or the URL).</span></span> <span data-ttu-id="adac3-166">อีกทางเลือกหนึ่ง คุณอาจต้องลบออกจากหน้า</span><span class="sxs-lookup"><span data-stu-id="adac3-166">Alternatively, you might have to remove it from the page.</span></span> <span data-ttu-id="adac3-167">ใช้หนึ่งในกระบวนงานต่อไปนี้เพื่อแก้ไขการตั้งค่าคอนฟิกของแอปที่ฝังอยู่ หรือลบออกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="adac3-167">Use one of the following procedures to edit the configuration of an embedded app or remove it completely.</span></span>

### <a name="apps-that-are-embedded-on-existing-pages"></a><span data-ttu-id="adac3-168">แอปที่ถูกฝังอยู่ในหน้าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="adac3-168">Apps that are embedded on existing pages</span></span>

1. <span data-ttu-id="adac3-169">เปิดหน้าที่มีการฝังแอป</span><span class="sxs-lookup"><span data-stu-id="adac3-169">Open the page where the app is embedded.</span></span>
2. <span data-ttu-id="adac3-170">เลือก **การตั้งค่า** และจากนั้น **กำหนดเป็นแบบส่วนบุคคล** เพื่อเปิดแถบเครื่องมือ **การกำหนดเป็นแบบส่วนบุคคล**</span><span class="sxs-lookup"><span data-stu-id="adac3-170">Select **Settings** and then **Personalize** to open the **Personalization** toolbar.</span></span>
3. <span data-ttu-id="adac3-171">เลือกเครื่องมือ **เลือก** แล้วจากนั้น เลือกแอปที่ฝังอยู่</span><span class="sxs-lookup"><span data-stu-id="adac3-171">Select the **Select** tool, and then select the embedded app.</span></span>
4. <span data-ttu-id="adac3-172">เมื่อต้องการแก้ไขแอป ให้ทำการเปลี่ยนแปลงที่ต้องการไปยังการตั้งค่าคอนฟิก แล้วจากนั้น เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="adac3-172">To edit the app, make the required changes to its configuration, and then select **Save**.</span></span>

    <span data-ttu-id="adac3-173">อีกทางเลือกหนึ่ง เมื่อต้องการลบแอป ให้เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="adac3-173">Alternatively, to remove the app, select **Delete**.</span></span>

5. <span data-ttu-id="adac3-174">บันทึกใหม่ หรือเผยแพร่มุมมองใหม่</span><span class="sxs-lookup"><span data-stu-id="adac3-174">Re-save or republish the view.</span></span> <span data-ttu-id="adac3-175">โปรดทราบว่าหากคุณออกจากหน้าโดยไม่บันทึกมุมมองอย่างชัดแจ้ง ระบบจะไม่รักษาการดำเนินการใดๆ ที่คุณดำเนินการในบานหน้าต่าง **แก้ไขเว็บไซต์**</span><span class="sxs-lookup"><span data-stu-id="adac3-175">Note that if you leave the page without explicitly saving the view, none of the actions that you performed in the **Edit website** pane will be maintained.</span></span>

### <a name="apps-that-are-embedded-from-the-dashboard"></a><span data-ttu-id="adac3-176">แอปที่ถูกฝังอยู่ในแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="adac3-176">Apps that are embedded from the dashboard</span></span>

1. <span data-ttu-id="adac3-177">เปิดแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="adac3-177">Open the dashboard.</span></span>
2. <span data-ttu-id="adac3-178">เลือกไทล์ที่เชื่อมโยงกับแอปที่ฝังอยู่ค้างไว้ (หรือคลิกขวา) แล้วจากนั้น เลือก **กำหนดให้เป็นแบบส่วนตัว**</span><span class="sxs-lookup"><span data-stu-id="adac3-178">Select and hold (or right-click) the tile that is associated with the embedded app, and then select **Personalize**.</span></span>
3. <span data-ttu-id="adac3-179">เมื่อต้องการแก้ไขแอป ให้เลือก **แก้ไขหน้า**</span><span class="sxs-lookup"><span data-stu-id="adac3-179">To edit the app, select **Edit page**.</span></span> <span data-ttu-id="adac3-180">ในบานหน้าต่าง **แก้ไขเว็บไซต์** ให้ทำการเปลี่ยนแปลงที่ต้องการไปยังการตั้งค่าคอนฟิกแอป แล้วจากนั้น เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="adac3-180">In the **Edit website** pane, make the required changes to the app configuration, and then select **Save**.</span></span>

    <span data-ttu-id="adac3-181">อีกทางเลือกหนึ่ง เมื่อต้องการลบแอป ให้เลือก **ลบหน้า**</span><span class="sxs-lookup"><span data-stu-id="adac3-181">Alternatively, to remove the app, select **Remove page**.</span></span>

## <a name="appendix"></a><span data-ttu-id="adac3-182">ภาคผนวก</span><span class="sxs-lookup"><span data-stu-id="adac3-182">Appendix</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="adac3-183">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="adac3-183">Troubleshooting</span></span>

<span data-ttu-id="adac3-184">ถ้าเว็บไซต์แสดงผลไม่ถูกต้องหลังจากที่ฝังอยู่ในแอป Finance and Operation หรือหากคุณได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่า URL ถูกปฏิเสธการเชื่อมต่อ เว็บไซต์อาจได้รับการตั้งค่าคอนฟิกเพื่อป้องกันไม่ให้ตัวเองฝังอยู่ใน iframe</span><span class="sxs-lookup"><span data-stu-id="adac3-184">If a website isn't rendered correctly after it's embedded in a Finance and Operation app, or if you receive an error message that states that the URL was denied a connection, the website is probably configured to prevent itself from being embedded in an iframe.</span></span> <span data-ttu-id="adac3-185">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อระบุว่าสามารถฝังเว็บไซต์ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="adac3-185">Follow these steps to determine whether the website can be embedded.</span></span>

1. <span data-ttu-id="adac3-186">เปิดเครื่องมือนักพัฒนาสำหรับเบราเซอร์ที่คุณใช้งาน</span><span class="sxs-lookup"><span data-stu-id="adac3-186">Open the developer tools for the browser that you're using.</span></span>
2. <span data-ttu-id="adac3-187">บนแท็บ **เครือข่าย** ให้ค้นหาและเลือกการตอบสนองจากไซต์ที่ฝังอยู่</span><span class="sxs-lookup"><span data-stu-id="adac3-187">On the **Network** tab, find and select the response from the embedded site.</span></span>
3. <span data-ttu-id="adac3-188">บนแท็บ **หัวข้อ** ภายใต้ **หัวข้อการตอบสนอง** ให้ค้นหา **x-frame-options**</span><span class="sxs-lookup"><span data-stu-id="adac3-188">On the **Headers** tab, under **Response Headers**, look for **x-frame-options**.</span></span> <span data-ttu-id="adac3-189">ถ้ามี **x-frame-options** อยู่ในหัวข้อการตอบสนอง และมีค่าเป็น **DENY** หรือ **SAMEORIGIN** จะไม่สามารถฝังเว็บไซต์ได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="adac3-189">If **x-frame-options** exists in the response headers, and has a value of **DENY** or **SAMEORIGIN**, the website can't currently be embedded.</span></span> <span data-ttu-id="adac3-190">คุณจะต้องทำงานกับเจ้าของแอปเพื่อเปิดใช้งานให้มีการฝังอย่างปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="adac3-190">You will have to work with the owner of the app to enable it to be safely embedded.</span></span>

### <a name="developer-modeling-a-website-on-a-form"></a><span data-ttu-id="adac3-191">[นักพัฒนา] การสร้างโมเดลเว็บไซต์บนฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="adac3-191">[Developer] Modeling a website on a form</span></span>

<span data-ttu-id="adac3-192">ถึงแม้ว่าหัวข้อนี้จะเน้นที่แอปหรือเว็บไซต์ของบุคคลที่สามแบบฝังผ่านการกำหนดเป็นแบบส่วนบุคคล แต่นักพัฒนายังสามารถฝังแอปหรือเว็บไซต์เหล่านั้นในฟอร์มได้โดยการใช้ประสบการณ์การพัฒนา Visual Studio</span><span class="sxs-lookup"><span data-stu-id="adac3-192">Although this topic is focused on embedding third-party apps or websites through personalization, developers can also embed them in a form by using the Visual Studio development experience.</span></span> <span data-ttu-id="adac3-193">เพียงเพิ่มตัวควบคุม **WebsiteHostControl** ลงในฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="adac3-193">Just add a **WebsiteHostControl** control to the form.</span></span> <span data-ttu-id="adac3-194">คุณสมบัติข้อมูลเมตาที่พร้อมใช้งานสำหรับตัวควบคุม มีความสามารถเหมือนกับประสบการณ์การกำหนดเป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="adac3-194">The metadata properties that are available for the control provide the same capabilities as the personalization experience.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
