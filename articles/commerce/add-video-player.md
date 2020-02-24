---
title: โมดูลโปรแกรมเล่นวิดีโอ
description: หัวข้อนี้ครอบคลุมถึงโมดูลโปรแกรมเล่นวิดีโอ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025690"
---
# <a name="video-player-module"></a><span data-ttu-id="b4828-103">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="b4828-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b4828-104">หัวข้อนี้ครอบคลุมถึงโมดูลโปรแกรมเล่นวิดีโอ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b4828-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b4828-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="b4828-105">Overview</span></span>

<span data-ttu-id="b4828-106">โมดูลโปรแกรมเล่นวิดีโอใช้เพื่อสนับสนุนการเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="b4828-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="b4828-107">คุณสามารถเพิ่มเข้าในหน้าใดก็ได้ ซึ่งกำหนดให้เนื้อหาวิดีโอมีการอัพโหลดและมีอยู่ในระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="b4828-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="b4828-108">โมดูลของโปรแกรมเล่นวิดีโอสนับสนุนสื่อชนิด .mp4</span><span class="sxs-lookup"><span data-stu-id="b4828-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="b4828-109">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="b4828-109">Video player module</span></span>

<span data-ttu-id="b4828-110">โมดูลโปรแกรมเล่นวิดีโอสามารถใช้ในการแสดงวิดีโอบนไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="b4828-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="b4828-111">สนับสนุนความสามารถในการเล่นทั้งหมด เช่น การเล่น การหยุดชั่วคราว โหมดขนาดเต็ม คำอธิบายเสียง และคำอธิบายที่ปิด</span><span class="sxs-lookup"><span data-stu-id="b4828-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="b4828-112">โมดูลโปรแกรมเล่นวิดีโอยังสนับสนุนการกำหนดคำอธิบายที่ปิด เพื่อให้เป็นไปตามมาตรฐานการเข้าถึงของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="b4828-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="b4828-113">ตัวอย่างเช่น คุณสามารถเลือกกำหนดขนาดแบบอักษรและสีพื้นหลังได้</span><span class="sxs-lookup"><span data-stu-id="b4828-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="b4828-114">โมดูลโปรแกรมเล่นวิดีโอยังสนับสนุนแทร็คเสียงรอง</span><span class="sxs-lookup"><span data-stu-id="b4828-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="b4828-115">เมื่ออัปโหลดวิดีโอไปยัง CMS จะสามารถอัปโหลดแทร็กเสียงรองได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="b4828-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="b4828-116">โมดูลโปรแกรมเล่นวิดีโอสามารถเล่นแทร็กเสียงรองได้ถ้าผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="b4828-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="b4828-117">ตัวอย่างของโมดูลโปรแกรมเล่นวิดีโอในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="b4828-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="b4828-118">วิดีโอคำแนะนำบนเพจรายละเอียดผลิตภัณฑ์หรือเพจการตลาด</span><span class="sxs-lookup"><span data-stu-id="b4828-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="b4828-119">วิดีโอโปรโมชันหรือวิดีโอเกี่ยวกับนโยบายบนเพจการตลาดใดๆ</span><span class="sxs-lookup"><span data-stu-id="b4828-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="b4828-120">วิดีโอการตลาดที่เน้นคุณลักษณะผลิตภัณฑ์บนเพจรายละเอียดผลิตภัณฑ์หรือเพจการตลาด</span><span class="sxs-lookup"><span data-stu-id="b4828-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="b4828-121">คุณสมบัติโมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="b4828-121">Video player module properties</span></span>

| <span data-ttu-id="b4828-122">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="b4828-122">Property name</span></span>         | <span data-ttu-id="b4828-123">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="b4828-123">Value</span></span>                               | <span data-ttu-id="b4828-124">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b4828-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="b4828-125">เล่นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b4828-125">Auto play</span></span>             | <span data-ttu-id="b4828-126">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="b4828-126">**True** or **False**</span></span>               | <span data-ttu-id="b4828-127">เมื่อมีการตั้งค่าเป็น **จริง** จะมีการเล่นวิดีโอดังกล่าวโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b4828-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="b4828-128">ปิดเสียง</span><span class="sxs-lookup"><span data-stu-id="b4828-128">Mute</span></span>                  | <span data-ttu-id="b4828-129">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="b4828-129">**True** or **False**</span></span>               | <span data-ttu-id="b4828-130">เมื่อมีการตั้งค่าเป็น **จริง** เสียงจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b4828-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="b4828-131">สำหรับโปรแกรมเล่นนี้ ค่าเริ่มต้นเป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="b4828-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="b4828-132">ในเบราเซอร์ของ Chrome วิดีโอแบบเล่นอัตโนมัติจะถูกปิดใช้งานโดยค่าเริ่มต้น และจะมีการเล่นเสียงเฉพาะเมื่อผู้ใช้เล่นวิดีโอด้วยตนเองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b4828-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="b4828-133">วน</span><span class="sxs-lookup"><span data-stu-id="b4828-133">Loop</span></span>                  | <span data-ttu-id="b4828-134">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="b4828-134">**True** or **False**</span></span>               | <span data-ttu-id="b4828-135">เมื่อมีการตั้งค่าเป็น **จริง** วิดีโอจะเล่นซ้ำแบบวน</span><span class="sxs-lookup"><span data-stu-id="b4828-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="b4828-136">สื่อ</span><span class="sxs-lookup"><span data-stu-id="b4828-136">Media</span></span>                 | <span data-ttu-id="b4828-137">พาธและชื่อของไฟล์วิดีโอ</span><span class="sxs-lookup"><span data-stu-id="b4828-137">Video file path and name</span></span> | <span data-ttu-id="b4828-138">ไฟล์วิดีโอที่เล่นในโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="b4828-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="b4828-139">เล่นเต็มหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="b4828-139">Play fullscreen</span></span>       | <span data-ttu-id="b4828-140">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="b4828-140">**True** or **False**</span></span>               | <span data-ttu-id="b4828-141">เมื่อมีการตั้งค่าเป็น **จริง** จะมีการเล่นวิดีโอในโหมดหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="b4828-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="b4828-142">เล่นทริกเกอร์หยุดชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="b4828-142">Play pause trigger</span></span>    | <span data-ttu-id="b4828-143">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="b4828-143">**True** or **False**</span></span>               | <span data-ttu-id="b4828-144">เมื่อมีการตั้งค่าเป็น **จริง** ปุ่มเล่น/หยุดชั่วคราว จะแสดงอยู่บนวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="b4828-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="b4828-145">ตัวควบคุมโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="b4828-145">Video player controls</span></span> | <span data-ttu-id="b4828-146">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="b4828-146">**True** or **False**</span></span>               | <span data-ttu-id="b4828-147">เมื่อมีการตั้งค่าเป็น **จริง** ตัวควบคุมของโปรแกรมเล่นวีดีโอทั้งหมดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="b4828-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="b4828-148">ตัวควบคุมเหล่านี้ได้แก่ ตัวเลือกปุ่มเล่น และปุ่มหยุดชั่วคราว ตัวบ่งชี้ความก้าวหน้า และคำอธิบายที่ปิด</span><span class="sxs-lookup"><span data-stu-id="b4828-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="b4828-149">ซ่อนภาพโปสเตอร์</span><span class="sxs-lookup"><span data-stu-id="b4828-149">Hide poster image</span></span>     | <span data-ttu-id="b4828-150">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="b4828-150">**True** or **False**</span></span>               | <span data-ttu-id="b4828-151">วิดีโอสามารถมีเฟรมโปสเตอร์</span><span class="sxs-lookup"><span data-stu-id="b4828-151">A video can have a poster frame.</span></span> <span data-ttu-id="b4828-152">เมื่อมีการตั้งค่าของคุณสมบัตินี้เป็น **จริง** เฟรมโปสเตอร์จะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="b4828-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="b4828-153">ระดับตัวพราง</span><span class="sxs-lookup"><span data-stu-id="b4828-153">Mask level</span></span>            | <span data-ttu-id="b4828-154">ตัวเลขตั้งแต่ **0** ถึง **100**</span><span class="sxs-lookup"><span data-stu-id="b4828-154">A number from **0** through **100**</span></span> | <span data-ttu-id="b4828-155">ตัวพรางที่ใช้กับวิดีโอสำหรับการกำหนดลักษณะ</span><span class="sxs-lookup"><span data-stu-id="b4828-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="b4828-156">เพิ่มโมดูลโปรแกรมเล่นวิดีโอไปที่เพจ</span><span class="sxs-lookup"><span data-stu-id="b4828-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="b4828-157">ก่อนที่คุณจะสร้างโมดูลของโปรแกรมเล่นวิดีโอคุณต้องอัปโหลดวิดีโอไปยังไลบรารีสื่อก่อน</span><span class="sxs-lookup"><span data-stu-id="b4828-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="b4828-158">การเพิ่มโมดูลโปรแกรมเล่นวิดีโอไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b4828-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b4828-159">สร้างเท็มเพลตของหน้าซึ่งชื่อ **แม่แบบโปรแกรมเล่นวิดีโอ**</span><span class="sxs-lookup"><span data-stu-id="b4828-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="b4828-160">ในช่อง **หลัก** ของหน้าเริ่มต้น ให้เพิ่มโมดูลคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="b4828-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="b4828-161">ในโมดูลคอนเทนเนอร์ เพิ่มโมดูลโปรแกรมเล่นวิดีโอ และโมดูลโปรแกรมเล่นวิดีโอรอบข้าง</span><span class="sxs-lookup"><span data-stu-id="b4828-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="b4828-162">แก้ไขแม่แบบให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="b4828-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="b4828-163">ใช้แม่แบบโปรแกรมเล่นวิดีโอที่คุณสร้างขึ้น เพื่อสร้างเพจที่ชื่อ **เพจโปรแกรมเล่นวิดีโอ**</span><span class="sxs-lookup"><span data-stu-id="b4828-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="b4828-164">ในช่อง **หลัก** ของเพจใหม่ ให้เพิ่มโมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="b4828-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="b4828-165">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลของผู้เล่นวิดีโอ **ให้เลือกเพิ่ม** วิดีโอ</span><span class="sxs-lookup"><span data-stu-id="b4828-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="b4828-166">ในกล่องโต้ตอบ **ตัวเลือกสื่อ** เลือกวิดีโอ แล้วเลือก **อัพโหลดรายการสื่อใหม่**</span><span class="sxs-lookup"><span data-stu-id="b4828-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="b4828-167">บันทึกและแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="b4828-167">Save and preview the page.</span></span> <span data-ttu-id="b4828-168">คุณควรเห็นโมดูลวิดีโอบนเพจ</span><span class="sxs-lookup"><span data-stu-id="b4828-168">You should see the video module on the page.</span></span> <span data-ttu-id="b4828-169">คุณสามารถเปลี่ยนการตั้งค่าเพิ่มเติม เพื่อกำหนดลักษณะการทำงานของโมดูลได้</span><span class="sxs-lookup"><span data-stu-id="b4828-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="b4828-170">แก้ไขหน้าให้เสร็จสิ้น และเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="b4828-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4828-171">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b4828-171">Additional resources</span></span>

[<span data-ttu-id="b4828-172">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b4828-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b4828-173">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="b4828-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="b4828-174">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="b4828-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="b4828-175">โมดูลบล็อคข้อความ</span><span class="sxs-lookup"><span data-stu-id="b4828-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="b4828-176">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="b4828-176">Content block module</span></span>](add-hero-module.md)
