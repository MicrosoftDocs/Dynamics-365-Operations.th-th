---
title: จัดการไฟล์ robots.txt
description: หัวข้อนี้จะอธิบายวิธีจัดการไฟล์ robots.txt ใน Microsoft Dynamics 365 Commerce
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: d248dae36e6e038749ee17a5a6ccb32f1dde0aed
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096855"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="037d7-103">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="037d7-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="037d7-104">หัวข้อนี้จะอธิบายวิธีจัดการไฟล์ robots.txt ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="037d7-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="037d7-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="037d7-105">Overview</span></span>

<span data-ttu-id="037d7-106">มาตรฐานการแยก robots หรือ robots.txt เป็นมาตรฐานที่เว็บไซต์ใช้ในการสื่อสารกับ robots บนเว็บ</span><span class="sxs-lookup"><span data-stu-id="037d7-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="037d7-107">ซึ่งแนะนำ robots บนเว็บเกี่ยวกับพื้นที่ใดๆ ของเว็บไซต์ที่ไม่ควรไปเยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="037d7-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="037d7-108">Robots มักจะถูกใช้โดยเครื่องมือค้นหาเพื่อทำดัชนีเว็บไซต์</span><span class="sxs-lookup"><span data-stu-id="037d7-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="037d7-109">เมื่อต้องการแยก robots จากเซิร์ฟเวอร์ ให้คุณสร้างแฟ้มบนเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="037d7-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="037d7-110">ในแฟ้มนี้ คุณสามารถระบุนโยบายการเข้าถึงสำหรับ robots</span><span class="sxs-lookup"><span data-stu-id="037d7-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="037d7-111">แฟ้มต้องสามารถเข้าถึงได้ผ่านทาง HTTP ที่ URL เฉพาะที่ **/robots.txt**</span><span class="sxs-lookup"><span data-stu-id="037d7-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="037d7-112">ไฟล์ robots.txt ช่วยเครื่องมือค้นหาในการจัดดัชนีเนื้อหาบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="037d7-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="037d7-113">Dynamics 365 Commerce ช่วยให้คุณสามารถอัปโหลดไฟล์ robots.txt สำหรับโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="037d7-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="037d7-114">สำหรับแต่ละโดเมนในสภาพแวดล้อม Commerce คุณสามารถอัปโหลดไฟล์ robots.txt และเชื่อมโยงกับโดเมนนั้นได้</span><span class="sxs-lookup"><span data-stu-id="037d7-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="037d7-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับไฟล์ robots.txt ให้ไปที่ [หน้า robots บนเว็บ](https://www.robotstxt.org/)</span><span class="sxs-lookup"><span data-stu-id="037d7-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="037d7-116">อัปโหลดไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="037d7-116">Upload a robots.txt file</span></span>

<span data-ttu-id="037d7-117">หลังจากที่คุณได้สร้างและแก้ไขไฟล์ robots.txt ตาม [มาตรฐานการแยก robots](https://www.robotstxt.org/orig.html) ตรวจสอบให้แน่ใจว่าแฟ้มนั้นสามารถเข้าถึงได้บนคอมพิวเตอร์ที่คุณจะใช้เครื่องมือการสร้าง Commerce</span><span class="sxs-lookup"><span data-stu-id="037d7-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="037d7-118">แฟ้มต้องมีชื่อว่า **robots.txt**</span><span class="sxs-lookup"><span data-stu-id="037d7-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="037d7-119">เพื่อให้ได้ผลลัพธ์ที่ดีที่สุด จะต้องอยู่ในรูปแบบที่ระบุไว้ในมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="037d7-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="037d7-120">ลูกค้า Commerce แต่ละรายรับผิดชอบในการตรวจสอบและรักษาเนื้อหาของไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="037d7-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="037d7-121">เมื่อต้องการอัพโหลดไฟล์ robots.txt คุณต้องลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="037d7-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="037d7-122">หากต้องการอัพโหลดไฟล์ robots.txt ใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="037d7-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="037d7-123">ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="037d7-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="037d7-124">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="037d7-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="037d7-125">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **Robots.txt**</span><span class="sxs-lookup"><span data-stu-id="037d7-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="037d7-126">รายการของโดเมนทั้งหมดที่เชื่อมโยงกับสภาพแวดล้อมของคุณจะปรากฏในส่วนหลักของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="037d7-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="037d7-127">เลือก **จัดการ** เพื่ออัพโหลดไฟล์ robots.txt สำหรับโดเมนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="037d7-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="037d7-128">บนเมนูทางด้านขวา ให้เลือกปุ่ม **อัพโหลด** (ลูกศรชี้ขึ้น) ถัดจากโดเมนที่เชื่อมโยงกับไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="037d7-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="037d7-129">กล่องโต้ตอบเบราว์เซอร์ของแฟ้มปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="037d7-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="037d7-130">ในกล่องโต้ตอบ ให้เรียกดูและเลือกไฟล์ robots.txt ที่คุณต้องการอัพโหลดสำหรับโดเมนที่เชื่อมโยง และจากนั้น เลือก **เปิด** เพื่อทำให้การอัพโหลดเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="037d7-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="037d7-131">ในระหว่างการอัพโหลด Commerce จะตรวจสอบว่าแฟ้มนั้นเป็นแฟ้มข้อความ แต่จะไม่มีการยืนยันเนื้อหาของแฟ้ม</span><span class="sxs-lookup"><span data-stu-id="037d7-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="037d7-132">ดาวน์โหลดไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="037d7-132">Download a robots.txt file</span></span>

<span data-ttu-id="037d7-133">หากต้องการดาวน์โหลดไฟล์ robots.txt ใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="037d7-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="037d7-134">ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="037d7-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="037d7-135">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="037d7-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="037d7-136">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **Robots.txt**</span><span class="sxs-lookup"><span data-stu-id="037d7-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="037d7-137">รายการของโดเมนทั้งหมดที่เชื่อมโยงกับสภาพแวดล้อมของคุณจะปรากฏในส่วนหลักของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="037d7-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="037d7-138">เลือก **จัดการ** เพื่อดาวน์โหลดไฟล์ robots.txt สำหรับโดเมนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="037d7-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="037d7-139">บนเมนูทางด้านขวา ให้เลือกปุ่ม **ดาวน์โหลด** (ลูกศรชี้ลง) ถัดจากโดเมนที่เชื่อมโยงกับไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="037d7-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="037d7-140">กล่องโต้ตอบเบราว์เซอร์ของแฟ้มปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="037d7-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="037d7-141">ในกล่องโต้ตอบ ให้ไปที่ตำแหน่งที่ต้องการบนไดรฟ์ภายในเครื่องของคุณ ให้ยืนยันหรือป้อนชื่อแฟ้ม และจากนั้น เลือก **บันทึก** เพื่อทำการดาวน์โหลดให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="037d7-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="037d7-142">กระบวนงานนี้สามารถใช้เพื่อดาวน์โหลดเฉพาะไฟล์ robots.txt ที่อัปโหลดไว้ก่อนหน้านี้ผ่านทางเครื่องมือการสร้าง Commerce</span><span class="sxs-lookup"><span data-stu-id="037d7-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="037d7-143">ลบไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="037d7-143">Delete a robots.txt file</span></span>

<span data-ttu-id="037d7-144">หากต้องการลบไฟล์ robots.txt ใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="037d7-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="037d7-145">ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="037d7-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="037d7-146">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="037d7-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="037d7-147">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **Robots.txt**</span><span class="sxs-lookup"><span data-stu-id="037d7-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="037d7-148">รายการของโดเมนทั้งหมดที่เชื่อมโยงกับสภาพแวดล้อมของคุณจะปรากฏในส่วนหลักของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="037d7-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="037d7-149">เลือก **จัดการ** เพื่อลบไฟล์ robots.txt สำหรับโดเมนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="037d7-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="037d7-150">บนเมนูทางด้านขวา ให้เลือกปุ่ม **ลบ** (สัญลักษณ์ถังขยะ) ถัดจากโดเมนที่เชื่อมโยงกับไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="037d7-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="037d7-151">หน้าต่างเบราว์เซอร์ไฟล์จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="037d7-151">A file browser window appears.</span></span>
6. <span data-ttu-id="037d7-152">ในหน้าต่างเบราว์เซอร์ไฟล์ ให้เรียกดูและเลือกไฟล์ robots.txt ที่คุณต้องการลบสำหรับโดเมน และจากนั้น เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="037d7-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="037d7-153">กล่องข้อความเตือนปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="037d7-153">A warning message box appears.</span></span>
7. <span data-ttu-id="037d7-154">ในกล่องข้อความ ให้เลือก **ลบ** เพื่อยืนยันการลบไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="037d7-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="037d7-155">กระบวนงานนี้สามารถใช้เพื่อลบเฉพาะไฟล์ robots.txt ที่อัปโหลดไว้ก่อนหน้านี้ผ่านทางเครื่องมือการสร้าง Commerce</span><span class="sxs-lookup"><span data-stu-id="037d7-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="037d7-156">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="037d7-156">Additional resources</span></span>

[<span data-ttu-id="037d7-157">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="037d7-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="037d7-158">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="037d7-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="037d7-159">ตั้งค่าช่องทางร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="037d7-159">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="037d7-160">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="037d7-160">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="037d7-161">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="037d7-161">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="037d7-162">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="037d7-162">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="037d7-163">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="037d7-163">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="037d7-164">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="037d7-164">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="037d7-165">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="037d7-165">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="037d7-166">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="037d7-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="037d7-167">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="037d7-167">Enable location-based store detection</span></span>](enable-store-detection.md)
