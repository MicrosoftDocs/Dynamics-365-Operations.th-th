---
title: มีอะไรใหม่หรือที่เปลี่ยนแปลงในแอป Warehouse Management บนมือถือ
description: หัวข้อนี้จะแสดงรายการคุณลักษณะใหม่และคุณลักษณะที่เปลี่ยนแปลงของแอป Warehouse Management บนมือถือแต่ละรุ่นที่ปล่อยของ Microsoft Dynamics 365 Supply Chain Management
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261802"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="ce8bb-103">มีอะไรใหม่หรือที่เปลี่ยนแปลงในแอป Warehouse Management บนมือถือ</span><span class="sxs-lookup"><span data-stu-id="ce8bb-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce8bb-104">หัวข้อนี้จะแสดงรายการคุณลักษณะ การแก้ไข การปรับปรุง และปัญหาที่พบใหม่ของแอป Warehouse Management บนมือถือแต่ละรุ่นที่ปล่อยของ Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ce8bb-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="ce8bb-105">รุ่น 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="ce8bb-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="ce8bb-106">คุณลักษณะใหม่ การแก้ไข และการปรับปรุงในรุ่น 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="ce8bb-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="ce8bb-107">รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:</span><span class="sxs-lookup"><span data-stu-id="ce8bb-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="ce8bb-108">ตอนนี้ โหมดสาธิตจะแสดงป้ายชื่อทั้งหมดในภาษาของอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="ce8bb-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="ce8bb-109">คุณมีโอกาสน้อยที่จะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ไม่พบมุมมองที่เหมาะสมเกี่ยวกับขนาดที่ระบุ"</span><span class="sxs-lookup"><span data-stu-id="ce8bb-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="ce8bb-110">เพิ่มความสูงต่ำสุดของบัตรงานแล้ว (ในกรณีที่มีการตั้งค่าคอนฟิกฟิลด์สามฟิลด์ขึ้นไปให้ปรากฏในรายการงาน)</span><span class="sxs-lookup"><span data-stu-id="ce8bb-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="ce8bb-111">ปรับปรุงค่าเผื่อ (เลือน) ที่ด้านล่างของบัตรรายละเอียดแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="ce8bb-112">ขณะนี้สัญลักษณ์ในไฟล์ XML ที่ถูกแลกเปลี่ยนกับเซิร์ฟเวอร์ได้รับการจัดการอย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="ce8bb-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="ce8bb-113">(ตัวอย่างเช่น ขณะนี้การจัดการอักขระที่ไม่สามารถพิมพ์ได้แสดงขึ้นในขณะนี้จะไม่ทําให้แอปหยุดตอบสนองอีกต่อไป)</span><span class="sxs-lookup"><span data-stu-id="ce8bb-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="ce8bb-114">ข้อผิดพลาด HTTP (เช่น "ข้อผิดพลาด 503") เมื่อส่งคำขอเซิร์ฟเวอร์ได้รับการจัดการอย่างง่ายดายแล้วในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="ce8bb-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="ce8bb-115">ในขณะที่มีข้อผิดพลาดแสดงอยู่ รายการตัวเลือกจะไม่แสดงขึ้นโดยอัตโนมัติอีกต่อไปในตัวควบคุมกล่องคำสั่งผสม</span><span class="sxs-lookup"><span data-stu-id="ce8bb-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="ce8bb-116">แอปไม่หยุดตอบสนองอีกต่อไปเนื่องจากการวางแนวการแสดงผลที่เลือกไว้ในการตั้งค่าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ce8bb-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="ce8bb-117">ขณะนี้ รูปภาพผลิตภัณฑ์จะแสดงอยู่ในสภาพแวดล้อมระบบบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="ce8bb-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="ce8bb-118">(การเปลี่ยนแปลงนี้จะใช้กับรุ่นความละเอียดต่ำเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ce8bb-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="ce8bb-119">บริการจัดการไฟล์ไม่สนับสนุนรูปภาพขนาดเต็มในสภาพแวดล้อมระบบบริการตนเอง)</span><span class="sxs-lookup"><span data-stu-id="ce8bb-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="ce8bb-120">ปัญหาที่เกี่ยวข้องการเบิกสินค้าที่ขาดที่เป็นปริมาณศูนย์ถูกแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="ce8bb-121">แอปไม่หยุดตอบสนองอีกต่อไปเมื่อบัตรรายละเอียดแสดงฟิลด์ที่เหมือนกันหลายฟิลด์</span><span class="sxs-lookup"><span data-stu-id="ce8bb-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="ce8bb-122">ปัญหาที่ทราบในรุ่น 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="ce8bb-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="ce8bb-123">เกิดปัญหาที่ทราบต่อไปนี้อยู่ในรุ่นนี้:</span><span class="sxs-lookup"><span data-stu-id="ce8bb-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="ce8bb-124">แอป (โดยเฉพาะรายการงาน) จะช้าลงในช่วงเวลาหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ce8bb-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="ce8bb-125">**รุ่นของ Windows:** เมื่อมีการใช้ IND ในการสแกนบน Windows ผลลัพธ์ที่ไม่สอดคล้องกันจะทําให้สัญลักษณ์ที่สแกนผสมกัน</span><span class="sxs-lookup"><span data-stu-id="ce8bb-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="ce8bb-126">รุ่น 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="ce8bb-126">Version 2.0.5.0</span></span>

<span data-ttu-id="ce8bb-127">รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:</span><span class="sxs-lookup"><span data-stu-id="ce8bb-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="ce8bb-128">ข้อมูลลับของไคลเอนต์ไม่ซ่อนอยู่ในการตั้งค่าการเชื่อมต่ออีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="ce8bb-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="ce8bb-129">ขณะนี้คุณสามารถกดข้อความยาวใดๆ เพื่อดูข้อความทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="ce8bb-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="ce8bb-130">ข้อความแสดงข้อผิดพลาดเมื่อสิทธิ์การจัดเก็บขาดหายไปปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="ce8bb-131">มีการเพิ่มลำดับการควบคุมใหม่ให้กับบางโฟลว์</span><span class="sxs-lookup"><span data-stu-id="ce8bb-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="ce8bb-132">ปุ่มส่งไม่พร้อมใช้งานอีกต่อไปอย่างไม่ถูกต้องเนื่องจากขนาดของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="ce8bb-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="ce8bb-133">ขณะนี้ตัวเลือกสามารถดําเนินการต่อบนหน้าจอที่เล็กลงเมื่อมีการใช้ปุ่มที่ใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="ce8bb-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="ce8bb-134">การมีปุ่มวางทับสี่ปุ่มไม่ถูกตัดออกอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="ce8bb-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="ce8bb-135">ขณะนี้แป้นพิมพ์สนับสนุนปุ่มลบ</span><span class="sxs-lookup"><span data-stu-id="ce8bb-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="ce8bb-136">ปัญหาความสว่างที่อาจเกิดขึ้นเมื่อกดแป้นพิมพ์ได้รับการแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="ce8bb-137">ปัญหาข้อมูลสาธิตต่างๆ ได้รับการแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="ce8bb-138">ปัญหาที่ฟิลด์ตัวเลขได้รับผลกระทบในหน้ารายละเอียดมีการแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="ce8bb-139">แป้นพิมพ์หน้าจอจะไม่หายไปอีกต่อไปในบางอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="ce8bb-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="ce8bb-140">อินเทอร์เฟสผู้ใช้ (UI) ต่างๆ ได้รับการแก้ไขแล้ว เช่น การตั้งค่าภายนอกที่ได้รับผลกระทบจากสีพื้นหลังและการวางตําแหน่ง</span><span class="sxs-lookup"><span data-stu-id="ce8bb-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="ce8bb-141">UI ภาษารัสเซียได้รับการปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="ce8bb-142">ปัญหาต่างๆ ที่เป็นสาเหตุให้ระบบหยุดตอบสนองได้รับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="ce8bb-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="ce8bb-143">ปัญหาที่เกี่ยวข้องกับการเปิดเครื่องคิดเลขอีกครั้งได้รับการแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="ce8bb-144">**รุ่น Android:** ปัญหาที่ทำให้ Android 4.4 หยุดตอบสนองเมื่อเริ่มต้นได้รับการแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="ce8bb-145">**รุ่น Android:** การปรับสเกลขั้นต่ำลดลงเป็น 50 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="ce8bb-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="ce8bb-146">รุ่น 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="ce8bb-146">Version 2.0.4.0</span></span>

<span data-ttu-id="ce8bb-147">รุ่น 2.0.4.0 เป็นรายการนำออกใช้แรกที่พร้อมใช้งานแอป Warehouse Management บนมือถือ</span><span class="sxs-lookup"><span data-stu-id="ce8bb-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="ce8bb-148">คุณลักษณะใหม่ การแก้ไข และการปรับปรุงในรุ่น 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="ce8bb-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="ce8bb-149">รุ่นนี้จะแนะนำคุณลักษณะ การแก้ไข และการปรับปรุงใหม่ต่อไปนี้ซึ่งไม่พร้อมใช้งานในรุ่นการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ce8bb-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="ce8bb-150">ถ้าบัตรรายละเอียดมีป้ายชื่อสองตัวที่มีข้อมูลเหมือนกัน ป้ายชื่อใดป้ายชื่อหนึ่งจะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="ce8bb-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="ce8bb-151">ขณะนี้อักขระพิเศษจะแสดงขึ้นตามค่าเริ่มต้น และตัวเลือกเพื่อซ่อนอักขระเหล่านั้นถูกลบออกจากการตั้งค่าผู้ใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="ce8bb-152">ขณะนี้ปุ่มส่งที่ปิดใช้งานอยู่จะแสดงเป็นไม่พร้อมใช้งานในมุมมองที่ยกแบบย่อ</span><span class="sxs-lookup"><span data-stu-id="ce8bb-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="ce8bb-153">การเปลี่ยนแปลงตรรกะการจัดลำดับของตัวควบคุมช่วยให้มั่นใจว่ามาตราส่วนมีความต่อเนื่องมากขึ้นระหว่างอุปกรณ์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="ce8bb-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="ce8bb-154">ดังนั้นจึงมีความต้องการน้อยกว่าในการปรับสเกลแบบอักษรหรือปุ่ม</span><span class="sxs-lookup"><span data-stu-id="ce8bb-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="ce8bb-155">ธีมรูปแบบสีเริ่มต้นเปลี่ยนเป็น *เข้ม*</span><span class="sxs-lookup"><span data-stu-id="ce8bb-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="ce8bb-156">ไอคอนที่ขาดหายไปของปุ่มส่งที่ปิดใช้งานได้ถูกเพิ่มในมุมมอง ribbon แล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="ce8bb-157">ขณะนี้ข้อยกเว้นการหมดเวลาจะพาคุณไปยังหน้าการเชื่อมต่อแทนการแสดงข้อผิดพลาดในรายการ</span><span class="sxs-lookup"><span data-stu-id="ce8bb-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="ce8bb-158">หากไม่มีการดำเนินการการส่ง (เช่น **ตกลง** **ใช่** **ยอมรับ** **ทำแล้ว** หรือ **เสร็จสิ้น**) ปุ่มส่งจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ce8bb-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="ce8bb-159">ปรับปรุงเสถียรภาพของแอปแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-159">App stability has been improved.</span></span>
- <span data-ttu-id="ce8bb-160">มีการแก้ไขความเสี่ยงด้านความปลอดภัย [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701)</span><span class="sxs-lookup"><span data-stu-id="ce8bb-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="ce8bb-161">**รุ่นของ Windows:** ปัญหาใน Windows ซึ่งเมนูไม่ตอบสนองหลังจากที่ปรับขนาดหน้าต่างใหม่ได้รับการแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="ce8bb-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="ce8bb-162">ปัญหาที่ทราบในรุ่น 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="ce8bb-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="ce8bb-163">เกิดปัญหาที่ทราบต่อไปนี้อยู่ในรุ่นนี้:</span><span class="sxs-lookup"><span data-stu-id="ce8bb-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="ce8bb-164">รุ่นนี้มีปัญหากับอุปกรณ์ที่ใช้ Android 4.4</span><span class="sxs-lookup"><span data-stu-id="ce8bb-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="ce8bb-165">คุณอาจพบปัญหาเมื่อคุณใช้แอปใน Android รุ่นนี้</span><span class="sxs-lookup"><span data-stu-id="ce8bb-165">You might experience issues when you use the app on this Android version.</span></span>
