---
title: จัดการไฟล์ robots.txt
description: หัวข้อนี้จะอธิบายวิธีจัดการไฟล์ robots.txt ใน Microsoft Dynamics 365 Commerce
author: BrianShook
manager: annbe
ms.date: 01/08/2020
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
ms.openlocfilehash: d0ce49f2968030ca4656a01c7646819c01635e12
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003498"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="37f71-103">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="37f71-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="37f71-104">หัวข้อนี้จะอธิบายวิธีจัดการไฟล์ robots.txt ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="37f71-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="37f71-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="37f71-105">Overview</span></span>

<span data-ttu-id="37f71-106">มาตรฐานการแยก robots หรือ robots.txt เป็นมาตรฐานที่เว็บไซต์ใช้ในการสื่อสารกับ robots บนเว็บ</span><span class="sxs-lookup"><span data-stu-id="37f71-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="37f71-107">ซึ่งแนะนำ robots บนเว็บเกี่ยวกับพื้นที่ใดๆ ของเว็บไซต์ที่ไม่ควรไปเยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="37f71-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="37f71-108">Robots มักจะถูกใช้โดยเครื่องมือค้นหาเพื่อทำดัชนีเว็บไซต์</span><span class="sxs-lookup"><span data-stu-id="37f71-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="37f71-109">เมื่อต้องการแยก robots จากเซิร์ฟเวอร์ ให้คุณสร้างแฟ้มบนเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="37f71-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="37f71-110">ในแฟ้มนี้ คุณสามารถระบุนโยบายการเข้าถึงสำหรับ robots</span><span class="sxs-lookup"><span data-stu-id="37f71-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="37f71-111">แฟ้มต้องสามารถเข้าถึงได้ผ่านทาง HTTP ที่ URL เฉพาะที่ **/robots.txt**</span><span class="sxs-lookup"><span data-stu-id="37f71-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="37f71-112">ไฟล์ robots.txt ช่วยเครื่องมือค้นหาในการจัดดัชนีเนื้อหาบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="37f71-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="37f71-113">Dynamics 365 Commerce ช่วยให้คุณสามารถอัปโหลดไฟล์ robots.txt สำหรับโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="37f71-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="37f71-114">สำหรับแต่ละโดเมนในสภาพแวดล้อม Commerce คุณสามารถอัปโหลดไฟล์ robots.txt และเชื่อมโยงกับโดเมนนั้นได้</span><span class="sxs-lookup"><span data-stu-id="37f71-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="37f71-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับไฟล์ robots.txt ให้ไปที่ [หน้า robots บนเว็บ](https://www.robotstxt.org/)</span><span class="sxs-lookup"><span data-stu-id="37f71-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="37f71-116">อัปโหลดไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="37f71-116">Upload a robots.txt file</span></span>

<span data-ttu-id="37f71-117">หลังจากที่คุณได้สร้างและแก้ไขไฟล์ robots.txt ตาม [มาตรฐานการแยก robots](https://www.robotstxt.org/orig.html) ตรวจสอบให้แน่ใจว่าแฟ้มนั้นสามารถเข้าถึงได้บนคอมพิวเตอร์ที่คุณจะใช้เครื่องมือการสร้าง Commerce</span><span class="sxs-lookup"><span data-stu-id="37f71-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="37f71-118">แฟ้มต้องมีชื่อว่า **robots.txt**</span><span class="sxs-lookup"><span data-stu-id="37f71-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="37f71-119">เพื่อให้ได้ผลลัพธ์ที่ดีที่สุด จะต้องอยู่ในรูปแบบที่ระบุไว้ในมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="37f71-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="37f71-120">ลูกค้า Commerce แต่ละรายรับผิดชอบในการตรวจสอบและรักษาเนื้อหาของไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="37f71-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="37f71-121">เมื่อต้องการอัพโหลดไฟล์ robots.txt คุณต้องลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="37f71-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="37f71-122">หากต้องการอัพโหลดไฟล์ robots.txt ใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="37f71-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="37f71-123">ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="37f71-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="37f71-124">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="37f71-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="37f71-125">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **Robots.txt**</span><span class="sxs-lookup"><span data-stu-id="37f71-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="37f71-126">รายการของโดเมนทั้งหมดที่เชื่อมโยงกับสภาพแวดล้อมของคุณจะปรากฏในส่วนหลักของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="37f71-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="37f71-127">เลือก **จัดการ** เพื่ออัพโหลดไฟล์ robots.txt สำหรับโดเมนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="37f71-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="37f71-128">บนเมนูทางด้านขวา ให้เลือกปุ่ม **อัพโหลด** (ลูกศรชี้ขึ้น) ถัดจากโดเมนที่เชื่อมโยงกับไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="37f71-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="37f71-129">กล่องโต้ตอบเบราว์เซอร์ของแฟ้มปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="37f71-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="37f71-130">ในกล่องโต้ตอบ ให้เรียกดูและเลือกไฟล์ robots.txt ที่คุณต้องการอัพโหลดสำหรับโดเมนที่เชื่อมโยง และจากนั้น เลือก **เปิด** เพื่อทำให้การอัพโหลดเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="37f71-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="37f71-131">ในระหว่างการอัพโหลด Commerce จะตรวจสอบว่าแฟ้มนั้นเป็นแฟ้มข้อความ แต่จะไม่มีการยืนยันเนื้อหาของแฟ้ม</span><span class="sxs-lookup"><span data-stu-id="37f71-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="37f71-132">ดาวน์โหลดไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="37f71-132">Download a robots.txt file</span></span>

<span data-ttu-id="37f71-133">หากต้องการดาวน์โหลดไฟล์ robots.txt ใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="37f71-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="37f71-134">ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="37f71-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="37f71-135">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="37f71-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="37f71-136">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **Robots.txt**</span><span class="sxs-lookup"><span data-stu-id="37f71-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="37f71-137">รายการของโดเมนทั้งหมดที่เชื่อมโยงกับสภาพแวดล้อมของคุณจะปรากฏในส่วนหลักของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="37f71-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="37f71-138">เลือก **จัดการ** เพื่อดาวน์โหลดไฟล์ robots.txt สำหรับโดเมนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="37f71-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="37f71-139">บนเมนูทางด้านขวา ให้เลือกปุ่ม **ดาวน์โหลด** (ลูกศรชี้ลง) ถัดจากโดเมนที่เชื่อมโยงกับไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="37f71-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="37f71-140">กล่องโต้ตอบเบราว์เซอร์ของแฟ้มปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="37f71-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="37f71-141">ในกล่องโต้ตอบ ให้ไปที่ตำแหน่งที่ต้องการบนไดรฟ์ภายในเครื่องของคุณ ให้ยืนยันหรือป้อนชื่อแฟ้ม และจากนั้น เลือก **บันทึก** เพื่อทำการดาวน์โหลดให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="37f71-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="37f71-142">กระบวนงานนี้สามารถใช้เพื่อดาวน์โหลดเฉพาะไฟล์ robots.txt ที่อัปโหลดไว้ก่อนหน้านี้ผ่านทางเครื่องมือการสร้าง Commerce</span><span class="sxs-lookup"><span data-stu-id="37f71-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="37f71-143">ลบไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="37f71-143">Delete a robots.txt file</span></span>

<span data-ttu-id="37f71-144">หากต้องการลบไฟล์ robots.txt ใน Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="37f71-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="37f71-145">ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="37f71-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="37f71-146">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="37f71-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="37f71-147">ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **Robots.txt**</span><span class="sxs-lookup"><span data-stu-id="37f71-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="37f71-148">รายการของโดเมนทั้งหมดที่เชื่อมโยงกับสภาพแวดล้อมของคุณจะปรากฏในส่วนหลักของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="37f71-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="37f71-149">เลือก **จัดการ** เพื่อลบไฟล์ robots.txt สำหรับโดเมนในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="37f71-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="37f71-150">บนเมนูทางด้านขวา ให้เลือกปุ่ม **ลบ** (สัญลักษณ์ถังขยะ) ถัดจากโดเมนที่เชื่อมโยงกับไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="37f71-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="37f71-151">หน้าต่างเบราว์เซอร์ไฟล์จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="37f71-151">A file browser window appears.</span></span>
6. <span data-ttu-id="37f71-152">ในหน้าต่างเบราว์เซอร์ไฟล์ ให้เรียกดูและเลือกไฟล์ robots.txt ที่คุณต้องการลบสำหรับโดเมน และจากนั้น เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="37f71-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="37f71-153">กล่องข้อความเตือนปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="37f71-153">A warning message box appears.</span></span>
7. <span data-ttu-id="37f71-154">ในกล่องข้อความ ให้เลือก **ลบ** เพื่อยืนยันการลบไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="37f71-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="37f71-155">กระบวนงานนี้สามารถใช้เพื่อลบเฉพาะไฟล์ robots.txt ที่อัปโหลดไว้ก่อนหน้านี้ผ่านทางเครื่องมือการสร้าง Commerce</span><span class="sxs-lookup"><span data-stu-id="37f71-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37f71-156">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="37f71-156">Additional resources</span></span>

[<span data-ttu-id="37f71-157">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="37f71-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="37f71-158">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="37f71-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="37f71-159">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="37f71-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="37f71-160">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="37f71-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="37f71-161">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="37f71-161">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="37f71-162">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="37f71-162">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="37f71-163">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="37f71-163">Enable location-based store detection</span></span>](enable-store-detection.md)
