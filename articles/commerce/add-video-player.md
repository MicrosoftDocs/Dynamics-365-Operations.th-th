---
title: โมดูลโปรแกรมเล่นวิดีโอ
description: หัวข้อนี้ครอบคลุมถึงโมดูลโปรแกรมเล่นวิดีโอและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: aa1efa6ce959439c49983553edfaf247c8e8dcd5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797418"
---
# <a name="video-player-module"></a><span data-ttu-id="700ff-103">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="700ff-103">Video player module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="700ff-104">หัวข้อนี้ครอบคลุมถึงโมดูลโปรแกรมเล่นวิดีโอและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="700ff-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="700ff-105">โมดูลโปรแกรมเล่นวิดีโอใช้เพื่อสนับสนุนการเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="700ff-105">The video player module is used to support video playback.</span></span> <span data-ttu-id="700ff-106">คุณสามารถเพิ่มเข้าในหน้าใดก็ได้ ซึ่งกำหนดให้เนื้อหาวิดีโอมีการอัพโหลดและมีอยู่ในระบบการจัดการเนื้อหา (CMS)</span><span class="sxs-lookup"><span data-stu-id="700ff-106">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="700ff-107">โมดูลของโปรแกรมเล่นวิดีโอสนับสนุนสื่อชนิด .mp4</span><span class="sxs-lookup"><span data-stu-id="700ff-107">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="700ff-108">โมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="700ff-108">Video player module</span></span>

<span data-ttu-id="700ff-109">โมดูลโปรแกรมเล่นวิดีโอสามารถใช้ในการแสดงวิดีโอบนไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="700ff-109">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="700ff-110">สนับสนุนความสามารถในการเล่นทั้งหมด เช่น การเล่น การหยุดชั่วคราว โหมดขนาดเต็ม คำอธิบายเสียง และคำอธิบายที่ปิด</span><span class="sxs-lookup"><span data-stu-id="700ff-110">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="700ff-111">โมดูลโปรแกรมเล่นวิดีโอยังสนับสนุนการกำหนดคำอธิบายที่ปิด เพื่อให้เป็นไปตามมาตรฐานการเข้าถึงของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="700ff-111">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="700ff-112">ตัวอย่างเช่น คุณสามารถเลือกกำหนดขนาดแบบอักษรและสีพื้นหลังได้</span><span class="sxs-lookup"><span data-stu-id="700ff-112">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="700ff-113">โมดูลโปรแกรมเล่นวิดีโอยังสนับสนุนแทร็คเสียงรอง</span><span class="sxs-lookup"><span data-stu-id="700ff-113">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="700ff-114">เมื่ออัปโหลดวิดีโอไปยัง CMS จะสามารถอัปโหลดแทร็กเสียงรองได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="700ff-114">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="700ff-115">โมดูลโปรแกรมเล่นวิดีโอสามารถเล่นแทร็กเสียงรองได้ถ้าผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="700ff-115">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="700ff-116">ตัวอย่างของโมดูลโปรแกรมเล่นวิดีโอในอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="700ff-116">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="700ff-117">วิดีโอคำแนะนำบนเพจรายละเอียดผลิตภัณฑ์หรือเพจการตลาด</span><span class="sxs-lookup"><span data-stu-id="700ff-117">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="700ff-118">วิดีโอโปรโมชันหรือวิดีโอเกี่ยวกับนโยบายบนเพจการตลาดใดๆ</span><span class="sxs-lookup"><span data-stu-id="700ff-118">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="700ff-119">วิดีโอการตลาดที่เน้นคุณลักษณะผลิตภัณฑ์บนเพจรายละเอียดผลิตภัณฑ์หรือเพจการตลาด</span><span class="sxs-lookup"><span data-stu-id="700ff-119">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="700ff-120">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลโปรแกรมเล่นวิดีโอบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="700ff-120">The following image shows an example of a video player module on a home page.</span></span>

![ตัวอย่างโมดูลโปรแกรมเล่นวิดีโอ](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="700ff-122">คุณสมบัติโมดูลโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="700ff-122">Video player module properties</span></span>

| <span data-ttu-id="700ff-123">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="700ff-123">Property name</span></span>         | <span data-ttu-id="700ff-124">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="700ff-124">Value</span></span>                               | <span data-ttu-id="700ff-125">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="700ff-125">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="700ff-126">เล่นอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="700ff-126">Auto play</span></span>             | <span data-ttu-id="700ff-127">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="700ff-127">**True** or **False**</span></span>               | <span data-ttu-id="700ff-128">เมื่อมีการตั้งค่าเป็น **จริง** จะมีการเล่นวิดีโอดังกล่าวโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="700ff-128">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="700ff-129">ปิดเสียง</span><span class="sxs-lookup"><span data-stu-id="700ff-129">Mute</span></span>                  | <span data-ttu-id="700ff-130">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="700ff-130">**True** or **False**</span></span>               | <span data-ttu-id="700ff-131">เมื่อมีการตั้งค่าเป็น **จริง** เสียงจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="700ff-131">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="700ff-132">สำหรับโปรแกรมเล่นนี้ ค่าเริ่มต้นเป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="700ff-132">For this player, the default value is **False**.</span></span> <span data-ttu-id="700ff-133">ในเบราเซอร์ของ Chrome วิดีโอแบบเล่นอัตโนมัติจะถูกปิดใช้งานโดยค่าเริ่มต้น และจะมีการเล่นเสียงเฉพาะเมื่อผู้ใช้เล่นวิดีโอด้วยตนเองเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="700ff-133">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="700ff-134">วน</span><span class="sxs-lookup"><span data-stu-id="700ff-134">Loop</span></span>                  | <span data-ttu-id="700ff-135">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="700ff-135">**True** or **False**</span></span>               | <span data-ttu-id="700ff-136">เมื่อมีการตั้งค่าเป็น **จริง** วิดีโอจะเล่นซ้ำแบบวน</span><span class="sxs-lookup"><span data-stu-id="700ff-136">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="700ff-137">สื่อ</span><span class="sxs-lookup"><span data-stu-id="700ff-137">Media</span></span>                 | <span data-ttu-id="700ff-138">พาธและชื่อของไฟล์วิดีโอ</span><span class="sxs-lookup"><span data-stu-id="700ff-138">Video file path and name</span></span> | <span data-ttu-id="700ff-139">ไฟล์วิดีโอที่เล่นในโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="700ff-139">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="700ff-140">เล่นเต็มหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="700ff-140">Play fullscreen</span></span>       | <span data-ttu-id="700ff-141">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="700ff-141">**True** or **False**</span></span>               | <span data-ttu-id="700ff-142">เมื่อมีการตั้งค่าเป็น **จริง** จะมีการเล่นวิดีโอในโหมดหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="700ff-142">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="700ff-143">เล่นทริกเกอร์หยุดชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="700ff-143">Play pause trigger</span></span>    | <span data-ttu-id="700ff-144">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="700ff-144">**True** or **False**</span></span>               | <span data-ttu-id="700ff-145">เมื่อมีการตั้งค่าเป็น **จริง** ปุ่มเล่น/หยุดชั่วคราว จะแสดงอยู่บนวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="700ff-145">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="700ff-146">ตัวควบคุมโปรแกรมเล่นวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="700ff-146">Video player controls</span></span> | <span data-ttu-id="700ff-147">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="700ff-147">**True** or **False**</span></span>               | <span data-ttu-id="700ff-148">เมื่อมีการตั้งค่าเป็น **จริง** ตัวควบคุมของโปรแกรมเล่นวีดีโอทั้งหมดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="700ff-148">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="700ff-149">ตัวควบคุมเหล่านี้ได้แก่ ตัวเลือกปุ่มเล่น และปุ่มหยุดชั่วคราว ตัวบ่งชี้ความก้าวหน้า และคำอธิบายที่ปิด</span><span class="sxs-lookup"><span data-stu-id="700ff-149">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="700ff-150">ซ่อนภาพโปสเตอร์</span><span class="sxs-lookup"><span data-stu-id="700ff-150">Hide poster image</span></span>     | <span data-ttu-id="700ff-151">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="700ff-151">**True** or **False**</span></span>               | <span data-ttu-id="700ff-152">วิดีโอสามารถมีเฟรมโปสเตอร์</span><span class="sxs-lookup"><span data-stu-id="700ff-152">A video can have a poster frame.</span></span> <span data-ttu-id="700ff-153">เมื่อมีการตั้งค่าของคุณสมบัตินี้เป็น **จริง** เฟรมโปสเตอร์จะถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="700ff-153">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="700ff-154">ระดับตัวพราง</span><span class="sxs-lookup"><span data-stu-id="700ff-154">Mask level</span></span>            | <span data-ttu-id="700ff-155">ตัวเลขตั้งแต่ **0** ถึง **100**</span><span class="sxs-lookup"><span data-stu-id="700ff-155">A number from **0** through **100**</span></span> | <span data-ttu-id="700ff-156">ตัวพรางที่ใช้กับวิดีโอสำหรับการกำหนดลักษณะ</span><span class="sxs-lookup"><span data-stu-id="700ff-156">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="700ff-157">เพิ่มโมดูลโปรแกรมเล่นวิดีโอไปที่เพจ</span><span class="sxs-lookup"><span data-stu-id="700ff-157">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="700ff-158">ก่อนที่คุณจะสร้างโมดูลของโปรแกรมเล่นวิดีโอคุณต้องอัปโหลดวิดีโอไปยังไลบรารีสื่อก่อน</span><span class="sxs-lookup"><span data-stu-id="700ff-158">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="700ff-159">การเพิ่มโมดูลโปรแกรมเล่นวิดีโอไปยังหน้าใหม่ และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="700ff-159">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="700ff-160">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="700ff-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="700ff-161">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อน **เท็มเพลตโปรแกรมเล่นวิดีโอ** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="700ff-161">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="700ff-162">ในช่อง **เนื้อหา** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="700ff-162">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="700ff-163">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **หน้าเริ่มต้น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="700ff-163">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="700ff-164">ในช่อง **หลัก** ของโมดูล **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="700ff-164">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="700ff-165">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="700ff-165">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="700ff-166">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="700ff-166">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="700ff-167">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **โปรแกรมเล่นวิดีโอ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="700ff-167">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="700ff-168">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="700ff-168">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="700ff-169">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="700ff-169">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="700ff-170">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือกเท็มเพลตของโปรแกรมเล่นวิดีโอที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="700ff-170">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="700ff-171">ใต้ **ชื่อของหน้า** ให้ป้อน **หน้าโปรแกรมเล่นวิดีโอ** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="700ff-171">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="700ff-172">ในช่อง **หลัก** ของหน้าใหม่ เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="700ff-172">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="700ff-173">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="700ff-173">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="700ff-174">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="700ff-174">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="700ff-175">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **โปรแกรมเล่นวิดีโอ** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="700ff-175">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="700ff-176">ในบานหน้าต่างคุณสมบัติสำหรับโมดูลโปรแกรมเล่นวิดีโอ ให้เลือก **เพิ่มวิดีโอ**</span><span class="sxs-lookup"><span data-stu-id="700ff-176">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="700ff-177">ในกล่องโต้ตอบ **ตัวเลือกสื่อ** เลือกวิดีโอ แล้วเลือก **อัพโหลดรายการสื่อใหม่**</span><span class="sxs-lookup"><span data-stu-id="700ff-177">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="700ff-178">ในตัวสำรวจไฟล์ ให้เลือกไฟล์วิดีโอ แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="700ff-178">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="700ff-179">ในกล่องโต้ตอบ **อัปโหลดรายการสื่อ** ให้ป้อนชื่อเรื่องและข้อมูลอื่นๆ ตามต้องการแล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="700ff-179">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="700ff-180">ในกล่องโต้ตอบ **ตัวเลือกสื่อ** ให้เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="700ff-180">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="700ff-181">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="700ff-181">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="700ff-182">คุณควรเห็นโมดูลวิดีโอบนเพจ</span><span class="sxs-lookup"><span data-stu-id="700ff-182">You should see the video module on the page.</span></span> <span data-ttu-id="700ff-183">คุณสามารถเปลี่ยนการตั้งค่าเพิ่มเติม เพื่อกำหนดลักษณะการทำงานของโมดูลได้</span><span class="sxs-lookup"><span data-stu-id="700ff-183">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="700ff-184">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="700ff-184">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="700ff-185">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="700ff-185">Additional resources</span></span>

[<span data-ttu-id="700ff-186">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="700ff-186">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="700ff-187">โมดูลแบนเนอร์โปรโมชั่น</span><span class="sxs-lookup"><span data-stu-id="700ff-187">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="700ff-188">โมดูลวงล้อ</span><span class="sxs-lookup"><span data-stu-id="700ff-188">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="700ff-189">โมดูลบล็อกข้อความ</span><span class="sxs-lookup"><span data-stu-id="700ff-189">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="700ff-190">โมดูลบล็อกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="700ff-190">Content block module</span></span>](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]