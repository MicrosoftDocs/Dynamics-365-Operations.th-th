---
title: เปิด URL ใน POS
description: หัวข้อนี้ให้ภาพรวมของการพัฒนาที่ได้ถูกทำไปยังผลิตภัณฑ์และฟังก์ชันการค้นหาลูกค้าใน Dynamics 365 Commerce
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 91d10ac383ed860a69d2d62f4a246c5ca8690b3c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206810"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="3ff14-103">เปิด URL ใน POS</span><span class="sxs-lookup"><span data-stu-id="3ff14-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ff14-104">หัวข้อนี้อธิบายถึงวิธีการที่คุณตั้งค่าคอนฟิกปุ่มในการขายหน้าร้าน (POS) ของการขายปลีก เพื่อเปิด URL</span><span class="sxs-lookup"><span data-stu-id="3ff14-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="3ff14-105">ลักษณะการทำงานนี้ไม่จำเป็นต้องมีการกำหนดรหัสเอง และคุณสามารถตั้งค่าคอนฟิกได้โดยผู้ที่อยู่ในบทบาทที่ไม่ใช่นักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="3ff14-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="3ff14-106">คุณลักษณะนี้อนุญาตการตั้งค่าคอนฟิกของปุ่มใน POS โดยใช้โปรแกรมออกแบบกริดปุ่มเพื่อเปิด URL</span><span class="sxs-lookup"><span data-stu-id="3ff14-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="3ff14-107">ในปัจจุบัน นี่ได้รับการสนับสนุนในการตั้งค่าคอนฟิกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3ff14-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="3ff14-108">เปิดในหน้าต่างใหม่</span><span class="sxs-lookup"><span data-stu-id="3ff14-108">Open in new window.</span></span>
- <span data-ttu-id="3ff14-109">เปิดภายใน POS</span><span class="sxs-lookup"><span data-stu-id="3ff14-109">Open within POS.</span></span>
- <span data-ttu-id="3ff14-110">เปิดแอปแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="3ff14-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="3ff14-111">เปิดในหน้าต่างใหม่</span><span class="sxs-lookup"><span data-stu-id="3ff14-111">Open in new window</span></span>

<span data-ttu-id="3ff14-112">การตั้งค่าคอนฟิกนี้กำหนดว่าจะเปิด URL ในหน้าต่างใหม่ หรือภายในแอป</span><span class="sxs-lookup"><span data-stu-id="3ff14-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="3ff14-113">เมื่อมีการตั้งค่าคอนฟิกเพื่อเปิด URL ของเว็บภายในแอป แผงการนำทางด้านข้างและแถบด้านบนของ POS จะสามารถมองเห็นได้ และพร้อมใช้งานสำหรับการโต้ตอบของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3ff14-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="3ff14-114">เมื่อตั้งค่าคอนฟิกเพื่อเปิดในหน้าต่างใหม่ URL จะเปิดในหน้าต่างแอปใหม่บน Modern POS for Windows และในแท็บเบราเซอร์ใหม่ในไคลเอนต์ POS อื่นๆ ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3ff14-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="3ff14-115">ในการเปิดใช้งานรายการนี้ คุณต้องตั้งค่าคอนฟิก URL ด้วยตัวเลือก **เปิดในหน้าต่างใหม่** ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3ff14-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="3ff14-116">เปิดภายใน POS</span><span class="sxs-lookup"><span data-stu-id="3ff14-116">Open within POS</span></span>

<span data-ttu-id="3ff14-117">การเปิด URL ของเว็บภายใน POS ได้รับการสนับสนุนเฉพาะสำหรับ Modern POS บน Windows</span><span class="sxs-lookup"><span data-stu-id="3ff14-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="3ff14-118">บนไคลเอนต์อื่นๆ ความสามารถนี้อยู่ภายใต้การพัฒนา และวางแผนไว้สำหรับการนำออกใช้ในการปรับปรุงในอนาคต</span><span class="sxs-lookup"><span data-stu-id="3ff14-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="3ff14-119">ในการเปิดใช้งานรายการนี้ คุณต้องตั้งค่าคอนฟิก URL ด้วยตัวเลือก **เปิดในหน้าต่างใหม่** ที่ไม่ได้เลือก</span><span class="sxs-lookup"><span data-stu-id="3ff14-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="3ff14-120">เปิดแอปแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="3ff14-120">Open a native app</span></span>

<span data-ttu-id="3ff14-121">คุณลักษณะนี้ยังช่วยคุณในการระบุ URLs ที่ไม่ใช่เว็บ เพื่อเปิดแอปแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="3ff14-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="3ff14-122">ตัวอย่างเช่น คุณสามารถระบุโพรโทคอล URL ได้ เช่น MailTo, SIP, IM หรือ MSTEAMS ซึ่งจะสามารถจัดการได้โดยแอปแม่แบบที่สอดคล้องกันบนอุปกรณ์โฮสต์</span><span class="sxs-lookup"><span data-stu-id="3ff14-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="3ff14-123">ในการเปิดใช้งานรายการนี้ คุณต้องตั้งค่าคอนฟิก URL ด้วยตัวเลือก **เปิดในหน้าต่างใหม่** ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3ff14-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="3ff14-124">สำหรับคอมพิวเตอร์ที่ใช้ Windows ดู [ส่งออกหรือนำเข้าการเชื่อมโยงแอพลิเคชันเริ่มต้น](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) เพื่อตั้งค่าการเชื่อมโยงโพรโทคอลเริ่มต้น ถ้าคุณกำลังตั้งค่าคอมพิวเตอร์ของคุณโดยใช้การบริการรูปภาพของการปรับใช้และการจัดการ (DISM)</span><span class="sxs-lookup"><span data-stu-id="3ff14-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="3ff14-125">ถ้าคุณกำลังใช้ MDM เช่น Intune ในการจัดการคอมพิวเตอร์ Windows ของคุณ ดู [CSP นโยบาย - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults)</span><span class="sxs-lookup"><span data-stu-id="3ff14-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="3ff14-126">ถ้าคุณเป็นนักพัฒนาที่สร้างเว็บไซต์แบบกำหนดเอง ดู [เปิดใช้แอปเริ่มต้นสำหรับ URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app)</span><span class="sxs-lookup"><span data-stu-id="3ff14-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="3ff14-127">เปิดแอปแม่แบบอย่างราบรื่น</span><span class="sxs-lookup"><span data-stu-id="3ff14-127">Open a native app seamlessly</span></span>

<span data-ttu-id="3ff14-128">Windows iOS และ Android ยังอนุญาตให้เปิดแอปได้อย่างราบรื่นมากขึ้น โดยขึ้นอยู่กับการเชื่อมโยงโพรโทคอลแอป</span><span class="sxs-lookup"><span data-stu-id="3ff14-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="3ff14-129">ถ้าแอปของคุณไม่ได้ถูกตั้งค่าคอนฟิกเพื่อจัดการเปิดจากเว็บเบราเซอร์อยู่แล้ว คุณอาจต้องการนักพัฒนาเพื่อตั้งค่าคอนฟิกนี้</span><span class="sxs-lookup"><span data-stu-id="3ff14-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="3ff14-130">สำหรับ Windows ดู [เปิดใช้แอปสำหรับเว็บไซต์โดยใช้ตัวจัดการ URI แอป](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking)</span><span class="sxs-lookup"><span data-stu-id="3ff14-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="3ff14-131">สำหรับ iOS ดู [ลิงค์สากลสำหรับนักพัฒนา](https://developer.apple.com/ios/universal-links/)</span><span class="sxs-lookup"><span data-stu-id="3ff14-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="3ff14-132">สำหรับ Android ดู [การจัดการลิงค์แอป Android](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="3ff14-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="3ff14-133">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3ff14-133">Client</span></span>                | <span data-ttu-id="3ff14-134">เปิดในหน้าต่างใหม่</span><span class="sxs-lookup"><span data-stu-id="3ff14-134">Open in new window</span></span> | <span data-ttu-id="3ff14-135">เปิดแอปแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="3ff14-135">Open native app</span></span> | <span data-ttu-id="3ff14-136">เปิดภายใน POS</span><span class="sxs-lookup"><span data-stu-id="3ff14-136">Open within POS</span></span> | <span data-ttu-id="3ff14-137">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="3ff14-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="3ff14-138">Modern POS ใน Windows</span><span class="sxs-lookup"><span data-stu-id="3ff14-138">Modern POS on Windows</span></span> | <span data-ttu-id="3ff14-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="3ff14-139">✓\*</span></span>                | <span data-ttu-id="3ff14-140">✓</span><span class="sxs-lookup"><span data-stu-id="3ff14-140">✓</span></span>               | <span data-ttu-id="3ff14-141">✓</span><span class="sxs-lookup"><span data-stu-id="3ff14-141">✓</span></span>              | <span data-ttu-id="3ff14-142">\* เปิดในหน้าต่าง Modern POS ใหม่</span><span class="sxs-lookup"><span data-stu-id="3ff14-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="3ff14-143">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="3ff14-143">Cloud POS</span></span>             | <span data-ttu-id="3ff14-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="3ff14-144">✓\*</span></span>                | <span data-ttu-id="3ff14-145">✓</span><span class="sxs-lookup"><span data-stu-id="3ff14-145">✓</span></span>               | <span data-ttu-id="3ff14-146">X</span><span class="sxs-lookup"><span data-stu-id="3ff14-146">X</span></span>              | <span data-ttu-id="3ff14-147">\* เปิดในแท็บเบราเซอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="3ff14-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="3ff14-148">Modern POS ใน iOS</span><span class="sxs-lookup"><span data-stu-id="3ff14-148">Modern POS on iOS</span></span>     | <span data-ttu-id="3ff14-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="3ff14-149">✓\*</span></span>                | <span data-ttu-id="3ff14-150">✓</span><span class="sxs-lookup"><span data-stu-id="3ff14-150">✓</span></span>               | <span data-ttu-id="3ff14-151">X</span><span class="sxs-lookup"><span data-stu-id="3ff14-151">X</span></span>              | <span data-ttu-id="3ff14-152">\* เปิดในแท็บเบราเซอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="3ff14-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="3ff14-153">POS สมัยใหม่ใน Android</span><span class="sxs-lookup"><span data-stu-id="3ff14-153">Modern POS on Android</span></span> | <span data-ttu-id="3ff14-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="3ff14-154">✓\*</span></span>                | <span data-ttu-id="3ff14-155">✓</span><span class="sxs-lookup"><span data-stu-id="3ff14-155">✓</span></span>               | <span data-ttu-id="3ff14-156">X</span><span class="sxs-lookup"><span data-stu-id="3ff14-156">X</span></span>              | <span data-ttu-id="3ff14-157">\* เปิดในแท็บเบราเซอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="3ff14-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="3ff14-158">ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3ff14-158">Before you begin</span></span>

<span data-ttu-id="3ff14-159">ก่อนที่คุณจะเริ่มต้น ตรวจทานวิธีการตั้งค่าคอนฟิก [โครงร่างหน้าจอสำหรับการขายหน้าร้าน (POS)](pos-screen-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="3ff14-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="3ff14-160">เปิด URL ใน POS</span><span class="sxs-lookup"><span data-stu-id="3ff14-160">Open URL in POS</span></span>

<span data-ttu-id="3ff14-161">ในการตั้งค่าคอนฟิก URL ให้เปิดใน POS ดำเนินการขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3ff14-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="3ff14-162">ในสำนักงานใหญ่ ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> POS \> เค้าโครงหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="3ff14-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="3ff14-163">เลือก **กริดปุ่ม \> ผู้ออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="3ff14-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="3ff14-164">สร้างปุ่มใหม่</span><span class="sxs-lookup"><span data-stu-id="3ff14-164">Create a new button.</span></span>
4. <span data-ttu-id="3ff14-165">เลือกคุณสมบัติ **ปุ่ม**</span><span class="sxs-lookup"><span data-stu-id="3ff14-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="3ff14-166">เลือก **เปิด URL** เป็นการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="3ff14-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="3ff14-167">ป้อน URL ที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="3ff14-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="3ff14-168">ตั้งค่าคอนฟิกว่าจะเปิด URL ในหน้าต่างใหม่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3ff14-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]