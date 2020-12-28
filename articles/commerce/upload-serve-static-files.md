---
title: อัปโหลดและให้บริการไฟล์แบบคงที่
description: หัวข้อนี้จะอธิบายวิธีการอัพโหลดไฟล์แบบคงที่ไปยังตัวสร้างไซต์ Microsoft Dynamics 365 Commerce และวิธีสร้าง URL ที่กำหนดเองและชื่อไฟล์ที่สามารถใช้ในการร้องขอไฟล์นั้นได้
author: StuHarg
manager: annbe
ms.date: 11/16/2020
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
ms.openlocfilehash: 981bbf03480abfd812b4020173b7acfdad0fef14
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595003"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="e016b-103">อัปโหลดและให้บริการไฟล์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="e016b-103">Upload and serve static files</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e016b-104">หัวข้อนี้จะอธิบายวิธีการอัพโหลดไฟล์แบบคงที่ไปยังตัวสร้างไซต์ Microsoft Dynamics 365 Commerce และวิธีสร้าง URL ที่กำหนดเองและชื่อไฟล์ที่สามารถใช้ในการร้องขอไฟล์นั้นได้</span><span class="sxs-lookup"><span data-stu-id="e016b-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="e016b-105">ตัวเชื่อมต่อของบุคคลที่สามบางรายจำเป็นต้องมีไฟล์โฮสต์และทำหน้าที่จากไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="e016b-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="e016b-106">ตัวเชื่อมต่อเหล่านี้คาดว่าไฟล์จะถูกส่งคืนโดยการร้องขอไปยังพาธและชื่อไฟล์ที่โทรกลับเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="e016b-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="e016b-107">หัวข้อนี้จะอธิบายถึงวิธีการอัพโหลดและทำหน้าที่ไฟล์แบบคงที่ที่มี URL ของผู้ใช้ที่ระบุได้และชื่อไฟล์บนไซต์อีคอมเมิร์ซ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e016b-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="e016b-108">สร้าง URL ของไซต์ที่ส่งคืนไฟล์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="e016b-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="e016b-109">เมื่อต้องการสร้าง URL ของไซต์ที่ส่งคืนไฟล์แบบคงที่ในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e016b-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e016b-110">ไปยังไลบรารีสื่อของไซต์ของคุณ และอัปโหลดไฟล์ที่ควรได้รับการดำเนินการโดยการร้องขอไปยัง URL ที่คุณจะกำหนด</span><span class="sxs-lookup"><span data-stu-id="e016b-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="e016b-111">ถ้าคุณอัพโหลดไฟล์แล้ว คุณสามารถข้ามขั้นตอนนี้ได้</span><span class="sxs-lookup"><span data-stu-id="e016b-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="e016b-112">ไปที่ **URL** สำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e016b-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="e016b-113">เลือก **สร้าง \> URL ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e016b-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="e016b-114">ในกล่องโต้ตอบ **URL ใหม่** ให้เลือก **สินทรัพย์ของไลบรารีสื่อ**</span><span class="sxs-lookup"><span data-stu-id="e016b-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="e016b-115">ในฟิลด์ **พาธ URL** ป้อนพาธ URL</span><span class="sxs-lookup"><span data-stu-id="e016b-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="e016b-116">รวมชื่อไฟล์ในพาธ</span><span class="sxs-lookup"><span data-stu-id="e016b-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="e016b-117">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="e016b-117">Select **Next**.</span></span> <span data-ttu-id="e016b-118">ไลบรารีสื่อเปิดอยู่และแสดงสินทรัพย์สื่อทั้งหมดของชนิด **เอกสาร** ที่มีการอัพโหลดแล้ว</span><span class="sxs-lookup"><span data-stu-id="e016b-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="e016b-119">เลือกไฟล์ที่ควรมีให้สำหรับคำขอไปยัง URL ที่คุณกำหนดไว้ในขั้นตอนที่ 5</span><span class="sxs-lookup"><span data-stu-id="e016b-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="e016b-120">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e016b-120">Select **Save**.</span></span>

<span data-ttu-id="e016b-121">ณ จุดนี้ URL ที่คุณสร้างจะอยู่ในสถานะร่าง</span><span class="sxs-lookup"><span data-stu-id="e016b-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="e016b-122">ไฟล์ที่ URL ชี้ไปยังไม่มีการส่งคืนจนกว่าคุณจะเผยแพร่ URL</span><span class="sxs-lookup"><span data-stu-id="e016b-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="e016b-123">ก่อนที่คุณจะเผยแพร่ URL คุณสามารถตรวจสอบความถูกต้องว่าจะส่งคืนข้อมูลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e016b-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="e016b-124">ตรวจสอบและเผยแพร่ URL</span><span class="sxs-lookup"><span data-stu-id="e016b-124">Validate and publish a URL</span></span>

<span data-ttu-id="e016b-125">หากต้องการตรวจสอบความถูกต้องของ URL ก่อนคุณเผยแพร่ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="e016b-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="e016b-126">ไปที่ **URL** สำหรับไซต์ของคุณแล้วเลือก URL เพื่อดูตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e016b-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="e016b-127">ในบานหน้าต่างคุณสมบัติทางด้านขวา ด้านล่างปุ่ม **แก้ไข** เลือกลิงค์ URL ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e016b-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="e016b-128">เปิดหน้าต่างเบราเซอร์ใหม่ และคุณควรได้รับข้อผิดพลาด 404</span><span class="sxs-lookup"><span data-stu-id="e016b-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="e016b-129">ผนวกสตริงการสอบถาม **?preview=inprogress** ไปยัง URL (ตัวอย่างเช่น `https://yoursite.com/callback.html?preview=inprogress`), และโหลดหน้านี้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="e016b-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="e016b-130">ไฟล์ที่คุณอัพโหลดไปยังไลบรารีสื่อควรถูกส่งคืนในการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="e016b-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="e016b-131">หลังจากที่คุณตรวจสอบความถูกต้องของ URL แล้ว คุณสามารถเผยแพร่ URL ดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="e016b-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="e016b-132">ไปที่ **URL** สำหรับไซต์ของคุณแล้วเลือก URL</span><span class="sxs-lookup"><span data-stu-id="e016b-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="e016b-133">ให้เลือก **เผยแพร่** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="e016b-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="e016b-134">ปรับปรุงไฟล์ที่ชี้ไปยัง URL</span><span class="sxs-lookup"><span data-stu-id="e016b-134">Update the file that a URL points to</span></span>

<span data-ttu-id="e016b-135">หลังจากเผยแพร่ URL แล้ว คุณสามารถอัพเดตได้เพื่อให้ชี้ไปที่ไฟล์อื่น</span><span class="sxs-lookup"><span data-stu-id="e016b-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="e016b-136">อีกทางหนึ่งคือ คุณสามารถอัพเดต URL เพื่อชี้ไปยังชนิดของทรัพยากรที่แตกต่างกัน ตามที่อธิบายไว้ในหัวข้อถัดไป</span><span class="sxs-lookup"><span data-stu-id="e016b-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="e016b-137">ตัวอย่างเช่น คุณสามารถชี้ URL ไปยังหน้าภายในหรือเปลี่ยนเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="e016b-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="e016b-138">เมื่อต้องการอัพเดตไฟล์ที่ URL ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e016b-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="e016b-139">ไปที่ **URL** สำหรับไซต์ของคุณแล้วเลือก URL เพื่ออัปเดต</span><span class="sxs-lookup"><span data-stu-id="e016b-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="e016b-140">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="e016b-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="e016b-141">ภายใต้ **การกำหนด URL** ให้เลือกกล่อง **ขั้นตอนที่ 2** แล้วเลือกเอกสารใหม่จากไลบรารีสื่อ</span><span class="sxs-lookup"><span data-stu-id="e016b-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="e016b-142">เลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="e016b-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="e016b-143">ปรับปรุงชนิดสินทรัพย์ที่ชี้ไปยัง URL</span><span class="sxs-lookup"><span data-stu-id="e016b-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="e016b-144">นอกจากนี้คุณยังสามารถอัพเดตเป็น URL เพื่อให้ชี้ไปยังสินทรัพย์ชนิดอื่น (ทรัพยากร) เช่น หน้าภายในหรือเปลี่ยนเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="e016b-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="e016b-145">เมื่อต้องการอัพเดตชนิดสินทรัพย์ที่ URL ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e016b-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="e016b-146">ไปที่ **URL** สำหรับไซต์ของคุณแล้วเลือก URL เพื่ออัปเดต</span><span class="sxs-lookup"><span data-stu-id="e016b-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="e016b-147">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="e016b-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="e016b-148">ภายใต้ **การกำหนด URL** ภายใต้ **ขั้นตอนที่ 1** ให้เลือกชนิดสินทรัพย์อื่น</span><span class="sxs-lookup"><span data-stu-id="e016b-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="e016b-149">เลือกกล่อง **ขั้นตอนที่ 2** แล้วเลือกสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="e016b-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="e016b-150">เลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="e016b-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="e016b-151">เปลี่ยนพาธ URL</span><span class="sxs-lookup"><span data-stu-id="e016b-151">Change the URL path</span></span>

<span data-ttu-id="e016b-152">หลังจากที่สร้าง URL แล้ว คุณจะไม่สามารถเปลี่ยนเส้นทางของข้อความนี้ได้</span><span class="sxs-lookup"><span data-stu-id="e016b-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="e016b-153">ถ้าคุณต้องเปลี่ยนเส้นทาง URL ที่ทำหน้าที่เป็นไฟล์หรือทรัพยากรชนิดอื่น คุณต้องสร้าง URL ใหม่ แม็ปกับไฟล์ที่มีอยู่หรือทรัพยากรอื่น แล้วยกเลิกการเผยแพร่และลบ URL เก่า</span><span class="sxs-lookup"><span data-stu-id="e016b-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="e016b-154">เมื่อต้องการเปลี่ยนพาธ URL ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="e016b-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="e016b-155">เมื่อต้องการสร้าง URL ใหม่และแม็ปกับไฟล์ที่มีอยู่หรือทรัพยากรอื่น ให้ทำตามคำแนะนำใน [สร้าง URL ของไซต์ที่ส่งคืนส่วนไฟล์แบบคงที่](#create-a-site-url-that-returns-a-static-file) ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="e016b-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="e016b-156">เลือก URL ใหม่ และเลือก **เผยแพร่** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="e016b-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="e016b-157">มีการเผยแพร่ URL ใหม่</span><span class="sxs-lookup"><span data-stu-id="e016b-157">The new URL is published.</span></span>
1. <span data-ttu-id="e016b-158">เมื่อต้องการยกเลิกการเผยแพร่ URL เก่า ให้เลือก URL นั้น แล้วเลือก **ยกเลิกการเผยแพร่** บนแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="e016b-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="e016b-159">ขณะนี้คุณสามารถลบ URL เก่าได้ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="e016b-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e016b-160">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e016b-160">Additional resources</span></span>

[<span data-ttu-id="e016b-161">ภาพรวมของการจัดการสินทรัพย์ดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="e016b-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="e016b-162">อัพโหลดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="e016b-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="e016b-163">อัพโหลดวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="e016b-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="e016b-164">อัพโหลดไฟล์นอกเหนือจากรูปภาพและวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="e016b-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="e016b-165">ครอบตัดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="e016b-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="e016b-166">ปรับแต่งจุดโฟกัสของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="e016b-166">Customize image focal points</span></span>](dam-custom-focal-point.md)
