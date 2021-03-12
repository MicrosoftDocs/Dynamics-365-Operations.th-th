---
title: โมดูลโปรแกรมเล่นวิดีโอ
description: หัวข้อนี้ครอบคลุมถึงโมดูลโปรแกรมเล่นวิดีโอ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 712e9359e31be96c426d6f16c878f18f05cc1bd2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980118"
---
# <a name="video-player-module"></a><span data-ttu-id="d3893-103">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="d3893-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d3893-104">หัวข้อนี้ครอบคลุมถึงโมดูลโปรแกรมเล่นวิดีโอ และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d3893-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d3893-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="d3893-105">Overview</span></span>

<span data-ttu-id="d3893-106">โมดูลโปรแกรมเล่นวิดีโอใช้เพื่อสนับสนุนการเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="d3893-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="d3893-107">คุณสามารถเพิ่มเข้าในหน้าใดก็ได้ ซึ่งกำหนดให้เนื้อหาวิดีโอมีการอัพโหลดและมีอยู่ในระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="d3893-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="d3893-108">โมดูลของโปรแกรมเล่นวิดีโอสนับสนุนสื่อชนิด .mp4</span><span class="sxs-lookup"><span data-stu-id="d3893-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="d3893-109">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="d3893-109">Video player module</span></span>

<span data-ttu-id="d3893-110">โมดูลโปรแกรมเล่นวิดีโอสามารถใช้ในการแสดงวิดีโอบนไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="d3893-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="d3893-111">สนับสนุนความสามารถในการเล่นทั้งหมด เช่น การเล่น การหยุดชั่วคราว โหมดขนาดเต็ม คำอธิบายเสียง และคำอธิบายที่ปิด</span><span class="sxs-lookup"><span data-stu-id="d3893-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="d3893-112">โมดูลโปรแกรมเล่นวิดีโอยังสนับสนุนการกำหนดคำอธิบายที่ปิด เพื่อให้เป็นไปตามมาตรฐานการเข้าถึงของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="d3893-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="d3893-113">ตัวอย่างเช่น คุณสามารถเลือกกำหนดขนาดแบบอักษรและสีพื้นหลังได้</span><span class="sxs-lookup"><span data-stu-id="d3893-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="d3893-114">โมดูลโปรแกรมเล่นวิดีโอยังสนับสนุนแทร็คเสียงรอง</span><span class="sxs-lookup"><span data-stu-id="d3893-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="d3893-115">เมื่ออัปโหลดวิดีโอไปยัง CMS จะสามารถอัปโหลดแทร็กเสียงรองได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d3893-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="d3893-116">โมดูลโปรแกรมเล่นวิดีโอสามารถเล่นแทร็กเสียงรองได้ถ้าผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="d3893-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="d3893-117">ตัวอย่างของโมดูลโปรแกรมเล่นวิดีโอในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="d3893-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="d3893-118">วิดีโอคำแนะนำบนเพจรายละเอียดผลิตภัณฑ์หรือเพจการตลาด</span><span class="sxs-lookup"><span data-stu-id="d3893-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="d3893-119">วิดีโอโปรโมชันหรือวิดีโอเกี่ยวกับนโยบายบนเพจการตลาดใดๆ</span><span class="sxs-lookup"><span data-stu-id="d3893-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="d3893-120">วิดีโอการตลาดที่เน้นคุณลักษณะผลิตภัณฑ์บนเพจรายละเอียดผลิตภัณฑ์หรือเพจการตลาด</span><span class="sxs-lookup"><span data-stu-id="d3893-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="d3893-121">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลโปรแกรมเล่นวิดีโอบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="d3893-121">The following image shows an example of a video player module on a home page.</span></span>

![ตัวอย่างโมดูลโปรแกรมเล่นวิดีโอ](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="d3893-123">คุณสมบัติโมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="d3893-123">Video player module properties</span></span>

| <span data-ttu-id="d3893-124">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="d3893-124">Property name</span></span>         | <span data-ttu-id="d3893-125">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="d3893-125">Value</span></span>                               | <span data-ttu-id="d3893-126">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d3893-126">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="d3893-127">เล่นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d3893-127">Auto play</span></span>             | <span data-ttu-id="d3893-128">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d3893-128">**True** or **False**</span></span>               | <span data-ttu-id="d3893-129">เมื่อมีการตั้งค่าเป็น **จริง** จะมีการเล่นวิดีโอดังกล่าวโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d3893-129">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="d3893-130">ปิดเสียง</span><span class="sxs-lookup"><span data-stu-id="d3893-130">Mute</span></span>                  | <span data-ttu-id="d3893-131">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d3893-131">**True** or **False**</span></span>               | <span data-ttu-id="d3893-132">เมื่อมีการตั้งค่าเป็น **จริง** เสียงจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d3893-132">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="d3893-133">สำหรับโปรแกรมเล่นนี้ ค่าเริ่มต้นเป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d3893-133">For this player, the default value is **False**.</span></span> <span data-ttu-id="d3893-134">ในเบราเซอร์ของ Chrome วิดีโอแบบเล่นอัตโนมัติจะถูกปิดใช้งานโดยค่าเริ่มต้น และจะมีการเล่นเสียงเฉพาะเมื่อผู้ใช้เล่นวิดีโอด้วยตนเองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d3893-134">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="d3893-135">วน</span><span class="sxs-lookup"><span data-stu-id="d3893-135">Loop</span></span>                  | <span data-ttu-id="d3893-136">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d3893-136">**True** or **False**</span></span>               | <span data-ttu-id="d3893-137">เมื่อมีการตั้งค่าเป็น **จริง** วิดีโอจะเล่นซ้ำแบบวน</span><span class="sxs-lookup"><span data-stu-id="d3893-137">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="d3893-138">สื่อ</span><span class="sxs-lookup"><span data-stu-id="d3893-138">Media</span></span>                 | <span data-ttu-id="d3893-139">พาธและชื่อของไฟล์วิดีโอ</span><span class="sxs-lookup"><span data-stu-id="d3893-139">Video file path and name</span></span> | <span data-ttu-id="d3893-140">ไฟล์วิดีโอที่เล่นในโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="d3893-140">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="d3893-141">เล่นเต็มหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="d3893-141">Play fullscreen</span></span>       | <span data-ttu-id="d3893-142">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d3893-142">**True** or **False**</span></span>               | <span data-ttu-id="d3893-143">เมื่อมีการตั้งค่าเป็น **จริง** จะมีการเล่นวิดีโอในโหมดหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="d3893-143">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="d3893-144">เล่นทริกเกอร์หยุดชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="d3893-144">Play pause trigger</span></span>    | <span data-ttu-id="d3893-145">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d3893-145">**True** or **False**</span></span>               | <span data-ttu-id="d3893-146">เมื่อมีการตั้งค่าเป็น **จริง** ปุ่มเล่น/หยุดชั่วคราว จะแสดงอยู่บนวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="d3893-146">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="d3893-147">ตัวควบคุมโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="d3893-147">Video player controls</span></span> | <span data-ttu-id="d3893-148">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d3893-148">**True** or **False**</span></span>               | <span data-ttu-id="d3893-149">เมื่อมีการตั้งค่าเป็น **จริง** ตัวควบคุมของโปรแกรมเล่นวีดีโอทั้งหมดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="d3893-149">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="d3893-150">ตัวควบคุมเหล่านี้ได้แก่ ตัวเลือกปุ่มเล่น และปุ่มหยุดชั่วคราว ตัวบ่งชี้ความก้าวหน้า และคำอธิบายที่ปิด</span><span class="sxs-lookup"><span data-stu-id="d3893-150">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="d3893-151">ซ่อนภาพโปสเตอร์</span><span class="sxs-lookup"><span data-stu-id="d3893-151">Hide poster image</span></span>     | <span data-ttu-id="d3893-152">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="d3893-152">**True** or **False**</span></span>               | <span data-ttu-id="d3893-153">วิดีโอสามารถมีเฟรมโปสเตอร์</span><span class="sxs-lookup"><span data-stu-id="d3893-153">A video can have a poster frame.</span></span> <span data-ttu-id="d3893-154">เมื่อมีการตั้งค่าของคุณสมบัตินี้เป็น **จริง** เฟรมโปสเตอร์จะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="d3893-154">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="d3893-155">ระดับตัวพราง</span><span class="sxs-lookup"><span data-stu-id="d3893-155">Mask level</span></span>            | <span data-ttu-id="d3893-156">ตัวเลขตั้งแต่ **0** ถึง **100**</span><span class="sxs-lookup"><span data-stu-id="d3893-156">A number from **0** through **100**</span></span> | <span data-ttu-id="d3893-157">ตัวพรางที่ใช้กับวิดีโอสำหรับการกำหนดลักษณะ</span><span class="sxs-lookup"><span data-stu-id="d3893-157">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="d3893-158">เพิ่มโมดูลโปรแกรมเล่นวิดีโอไปที่เพจ</span><span class="sxs-lookup"><span data-stu-id="d3893-158">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="d3893-159">ก่อนที่คุณจะสร้างโมดูลของโปรแกรมเล่นวิดีโอคุณต้องอัปโหลดวิดีโอไปยังไลบรารีสื่อก่อน</span><span class="sxs-lookup"><span data-stu-id="d3893-159">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="d3893-160">การเพิ่มโมดูลโปรแกรมเล่นวิดีโอไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d3893-160">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d3893-161">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="d3893-161">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d3893-162">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อน **เท็มเพลตโปรแกรมเล่นวิดีโอ** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d3893-162">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="d3893-163">ในช่อง **เนื้อหา** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="d3893-163">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3893-164">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **หน้าเริ่มต้น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d3893-164">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d3893-165">ในช่อง **หลัก** ของโมดูล **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="d3893-165">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3893-166">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d3893-166">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d3893-167">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="d3893-167">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3893-168">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **โปรแกรมเล่นวิดีโอ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d3893-168">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d3893-169">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d3893-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="d3893-170">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="d3893-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="d3893-171">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือกเท็มเพลตของโปรแกรมเล่นวิดีโอที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="d3893-171">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="d3893-172">ใต้ **ชื่อของหน้า** ให้ป้อน **หน้าโปรแกรมเล่นวิดีโอ** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d3893-172">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="d3893-173">ในช่อง **หลัก** ของหน้าใหม่ เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="d3893-173">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3893-174">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d3893-174">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d3893-175">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="d3893-175">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3893-176">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **โปรแกรมเล่นวิดีโอ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d3893-176">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d3893-177">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลโปรแกรมเล่นวิดีโอ ให้เลือก **เพิ่มวิดีโอ**</span><span class="sxs-lookup"><span data-stu-id="d3893-177">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="d3893-178">ในกล่องโต้ตอบ **ตัวเลือกสื่อ** เลือกวิดีโอ แล้วเลือก **อัพโหลดรายการสื่อใหม่**</span><span class="sxs-lookup"><span data-stu-id="d3893-178">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="d3893-179">ในตัวสำรวจไฟล์ ให้เลือกไฟล์วิดีโอ แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="d3893-179">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="d3893-180">ในกล่องโต้ตอบ **อัปโหลดรายการสื่อ** ให้ป้อนชื่อเรื่องและข้อมูลอื่นๆ ตามต้องการแล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d3893-180">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="d3893-181">ในกล่องโต้ตอบ **ตัวเลือกสื่อ** ให้เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="d3893-181">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="d3893-182">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="d3893-182">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="d3893-183">คุณควรเห็นโมดูลวิดีโอบนเพจ</span><span class="sxs-lookup"><span data-stu-id="d3893-183">You should see the video module on the page.</span></span> <span data-ttu-id="d3893-184">คุณสามารถเปลี่ยนการตั้งค่าเพิ่มเติม เพื่อกำหนดลักษณะการทำงานของโมดูลได้</span><span class="sxs-lookup"><span data-stu-id="d3893-184">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="d3893-185">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d3893-185">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d3893-186">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d3893-186">Additional resources</span></span>

[<span data-ttu-id="d3893-187">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="d3893-187">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d3893-188">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="d3893-188">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="d3893-189">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="d3893-189">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="d3893-190">โมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="d3893-190">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="d3893-191">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="d3893-191">Content block module</span></span>](add-hero-module.md)
