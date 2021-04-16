---
title: จัดการไฟล์ robots.txt
description: หัวข้อนี้อธิบายวิธีจัดการไฟล์ robots.txt ใน Microsoft Dynamics 365 Commerce
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9b832d6714447f8957095c8c87d48527087f12d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794246"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="77799-103">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="77799-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77799-104">หัวข้อนี้อธิบายวิธีจัดการไฟล์ robots.txt ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="77799-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="77799-105">มาตรฐานการแยก robots หรือ robots.txt เป็นมาตรฐานที่เว็บไซต์ใช้ในการสื่อสารกับ robots บนเว็บ</span><span class="sxs-lookup"><span data-stu-id="77799-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="77799-106">ซึ่งแนะนำ robots บนเว็บเกี่ยวกับพื้นที่ใดๆ ของเว็บไซต์ที่ไม่ควรไปเยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="77799-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="77799-107">Robots มักจะถูกใช้โดยเครื่องมือค้นหาเพื่อทำดัชนีเว็บไซต์</span><span class="sxs-lookup"><span data-stu-id="77799-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="77799-108">เมื่อต้องการแยก robots จากเซิร์ฟเวอร์ ให้คุณสร้างแฟ้มบนเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="77799-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="77799-109">ในแฟ้มนี้ คุณสามารถระบุนโยบายการเข้าถึงสำหรับ robots</span><span class="sxs-lookup"><span data-stu-id="77799-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="77799-110">แฟ้มต้องสามารถเข้าถึงได้ผ่านทาง HTTP ที่ URL เฉพาะที่ **/robots.txt**</span><span class="sxs-lookup"><span data-stu-id="77799-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="77799-111">ไฟล์ robots.txt ช่วยเครื่องมือค้นหาในการจัดดัชนีเนื้อหาบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="77799-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="77799-112">Dynamics 365 Commerce ช่วยให้คุณสามารถอัปโหลดไฟล์ robots.txt สำหรับโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="77799-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="77799-113">สำหรับแต่ละโดเมนในสภาพแวดล้อม Commerce คุณสามารถอัปโหลดไฟล์ robots.txt และเชื่อมโยงกับโดเมนนั้นได้</span><span class="sxs-lookup"><span data-stu-id="77799-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="77799-114">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับไฟล์ robots.txt ให้ไปที่ [หน้า robots บนเว็บ](https://www.robotstxt.org/)</span><span class="sxs-lookup"><span data-stu-id="77799-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="77799-115">อัปโหลดไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="77799-115">Upload a robots.txt file</span></span>

<span data-ttu-id="77799-116">หลังจากที่คุณได้สร้างและแก้ไขไฟล์ robots.txt ตาม [มาตรฐานการแยก robots](https://www.robotstxt.org/orig.html) ตรวจสอบให้แน่ใจว่าแฟ้มนั้นสามารถเข้าถึงได้บนคอมพิวเตอร์ที่คุณจะใช้เครื่องมือการสร้าง Commerce</span><span class="sxs-lookup"><span data-stu-id="77799-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="77799-117">แฟ้มต้องมีชื่อว่า **robots.txt**</span><span class="sxs-lookup"><span data-stu-id="77799-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="77799-118">เพื่อให้ได้ผลลัพธ์ที่ดีที่สุด จะต้องอยู่ในรูปแบบที่ระบุไว้ในมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="77799-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="77799-119">ลูกค้า Commerce แต่ละรายรับผิดชอบในการตรวจสอบและรักษาเนื้อหาของไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="77799-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="77799-120">เมื่อต้องการอัพโหลดไฟล์ robots.txt คุณต้องลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="77799-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="77799-121">หากต้องการอัพโหลดไฟล์ robots.txt ใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="77799-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="77799-122">ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="77799-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="77799-123">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="77799-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="77799-124">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **Robots.txt**</span><span class="sxs-lookup"><span data-stu-id="77799-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="77799-125">รายการของโดเมนทั้งหมดที่เชื่อมโยงกับสภาพแวดล้อมของคุณจะปรากฏในส่วนหลักของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="77799-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="77799-126">เลือก **จัดการ** เพื่ออัพโหลดไฟล์ robots.txt สำหรับโดเมนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="77799-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="77799-127">บนเมนูทางด้านขวา ให้เลือกปุ่ม **อัพโหลด** (ลูกศรชี้ขึ้น) ถัดจากโดเมนที่เชื่อมโยงกับไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="77799-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="77799-128">กล่องโต้ตอบเบราว์เซอร์ของแฟ้มปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="77799-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="77799-129">ในกล่องโต้ตอบ ให้เรียกดูและเลือกไฟล์ robots.txt ที่คุณต้องการอัพโหลดสำหรับโดเมนที่เชื่อมโยง และจากนั้น เลือก **เปิด** เพื่อทำให้การอัพโหลดเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="77799-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="77799-130">ในระหว่างการอัพโหลด Commerce จะตรวจสอบว่าแฟ้มนั้นเป็นแฟ้มข้อความ แต่จะไม่มีการยืนยันเนื้อหาของแฟ้ม</span><span class="sxs-lookup"><span data-stu-id="77799-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="77799-131">ดาวน์โหลดไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="77799-131">Download a robots.txt file</span></span>

<span data-ttu-id="77799-132">หากต้องการดาวน์โหลดไฟล์ robots.txt ใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="77799-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="77799-133">ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="77799-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="77799-134">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="77799-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="77799-135">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **Robots.txt**</span><span class="sxs-lookup"><span data-stu-id="77799-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="77799-136">รายการของโดเมนทั้งหมดที่เชื่อมโยงกับสภาพแวดล้อมของคุณจะปรากฏในส่วนหลักของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="77799-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="77799-137">เลือก **จัดการ** เพื่อดาวน์โหลดไฟล์ robots.txt สำหรับโดเมนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="77799-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="77799-138">บนเมนูทางด้านขวา ให้เลือกปุ่ม **ดาวน์โหลด** (ลูกศรชี้ลง) ถัดจากโดเมนที่เชื่อมโยงกับไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="77799-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="77799-139">กล่องโต้ตอบเบราว์เซอร์ของแฟ้มปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="77799-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="77799-140">ในกล่องโต้ตอบ ให้ไปที่ตำแหน่งที่ต้องการบนไดรฟ์ภายในเครื่องของคุณ ให้ยืนยันหรือป้อนชื่อแฟ้ม และจากนั้น เลือก **บันทึก** เพื่อทำการดาวน์โหลดให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="77799-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="77799-141">กระบวนงานนี้สามารถใช้เพื่อดาวน์โหลดเฉพาะไฟล์ robots.txt ที่อัปโหลดไว้ก่อนหน้านี้ผ่านทางเครื่องมือการสร้าง Commerce</span><span class="sxs-lookup"><span data-stu-id="77799-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="77799-142">ลบไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="77799-142">Delete a robots.txt file</span></span>

<span data-ttu-id="77799-143">หากต้องการลบไฟล์ robots.txt ใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="77799-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="77799-144">ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="77799-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="77799-145">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="77799-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="77799-146">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **Robots.txt**</span><span class="sxs-lookup"><span data-stu-id="77799-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="77799-147">รายการของโดเมนทั้งหมดที่เชื่อมโยงกับสภาพแวดล้อมของคุณจะปรากฏในส่วนหลักของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="77799-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="77799-148">เลือก **จัดการ** เพื่อลบไฟล์ robots.txt สำหรับโดเมนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="77799-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="77799-149">บนเมนูทางด้านขวา ให้เลือกปุ่ม **ลบ** (สัญลักษณ์ถังขยะ) ถัดจากโดเมนที่เชื่อมโยงกับไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="77799-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="77799-150">หน้าต่างเบราว์เซอร์ไฟล์จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="77799-150">A file browser window appears.</span></span>
6. <span data-ttu-id="77799-151">ในหน้าต่างเบราว์เซอร์ไฟล์ ให้เรียกดูและเลือกไฟล์ robots.txt ที่คุณต้องการลบสำหรับโดเมน และจากนั้น เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="77799-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="77799-152">กล่องข้อความเตือนปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="77799-152">A warning message box appears.</span></span>
7. <span data-ttu-id="77799-153">ในกล่องข้อความ ให้เลือก **ลบ** เพื่อยืนยันการลบไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="77799-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="77799-154">กระบวนงานนี้สามารถใช้เพื่อลบเฉพาะไฟล์ robots.txt ที่อัปโหลดไว้ก่อนหน้านี้ผ่านทางเครื่องมือการสร้าง Commerce</span><span class="sxs-lookup"><span data-stu-id="77799-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77799-155">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="77799-155">Additional resources</span></span>

[<span data-ttu-id="77799-156">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="77799-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="77799-157">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="77799-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="77799-158">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="77799-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="77799-159">เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="77799-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="77799-160">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="77799-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="77799-161">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="77799-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="77799-162">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="77799-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="77799-163">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="77799-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="77799-164">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="77799-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="77799-165">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="77799-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
