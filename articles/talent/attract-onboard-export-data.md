---
title: ส่งออกข้อมูลจาก Attract และ Onboard
description: ส่งออกข้อมูลจาก Dynamics 365 Talent - Attract และ Onboard
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975945"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="9d961-103">ส่งออกข้อมูลจาก Attract และ Onboard</span><span class="sxs-lookup"><span data-stu-id="9d961-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d961-104">ตามที่ประกาศใน [Dynamics 365 Talent: Attract ที่กำลังหมดอายุ และแอป Dynamics 365 Talent: Onboard](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) เรากำลังเลิกใช้ Dynamics 365 Talent: Attract และ Dynamics 365 Talent: Onboard ในวันที่ 1 กุมภาพันธ์ 2022</span><span class="sxs-lookup"><span data-stu-id="9d961-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="9d961-105">ในการการช่วยเหลือในการย้ายข้อมูลไปยังผลิตภัณฑ์อื่น ทั้งสองแอปมีความสามารถในการส่งออกข้อมูลแล้ว</span><span class="sxs-lookup"><span data-stu-id="9d961-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="9d961-106">ส่งออกข้อมูลจาก Attract</span><span class="sxs-lookup"><span data-stu-id="9d961-106">Export data from Attract</span></span>

<span data-ttu-id="9d961-107">คุณสามารถส่งออกข้อมูลของคุณได้โดยไม่ต้องจำกัดการเข้าถึงสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="9d961-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="9d961-108">คุณอาจต้องการทำเช่นนี้ เพื่อวัตถุประสงค์ในการทดสอบ หรือเพื่อให้เข้าใจถึงโครงสร้างข้อมูลของเรา</span><span class="sxs-lookup"><span data-stu-id="9d961-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="9d961-109">เมื่อคุณพร้อมที่จะย้าย ให้จำกัดการเข้าถึงสภาพแวดล้อม Attract ของคุณโดยใช้คำสั่งหลังจากขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="9d961-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="9d961-110">ตรวจสอบให้แน่ใจว่าได้ส่งออกข้อมูลของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="9d961-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="9d961-111">ไปที่ [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport)</span><span class="sxs-lookup"><span data-stu-id="9d961-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="9d961-112">ภายใต้ **การส่งออกข้อมูล** ให้เลือก **การร้องขอการส่งออกข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="9d961-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="9d961-113">ร้องขอการส่งออกข้อมูลจาก Attract</span><span class="sxs-lookup"><span data-stu-id="9d961-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="9d961-114">เมื่อมีกล่องข้อความปรากฏ **การประมวลผลคำขอของคุณกำลังถูกจัดการ** ขึ้น **ให้เลือกตกลง**</span><span class="sxs-lookup"><span data-stu-id="9d961-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="9d961-115">การส่งออกข้อมูลอาจใช้เวลานานถึง 20 นาที ทั้งนี้ขึ้นอยู่กับขนาดของการส่งออกของคุณ</span><span class="sxs-lookup"><span data-stu-id="9d961-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="9d961-116">เมื่อการส่งออกของคุณเสร็จสมบูรณ์ ให้เลือกปุ่ม **ดาวน์โหลด** ที่อยู่ถัดไป</span><span class="sxs-lookup"><span data-stu-id="9d961-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="9d961-117">การส่งออกข้อมูลทั้งหมดจะพร้อมใช้งานเป็นเวลาเจ็ดวัน ซึ่งหลังจากนั้นลิงก์ **ดาวน์โหลด** จะหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="9d961-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="9d961-118">การดาวน์โหลดจะมีไฟล์ .zip ที่มีข้อมูล Attract รวมถึงโฟลเดอร์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9d961-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="9d961-119">ชื่อโฟลเดอร์</span><span class="sxs-lookup"><span data-stu-id="9d961-119">Folder name</span></span> | <span data-ttu-id="9d961-120">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="9d961-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="9d961-121">การตั้งค่าการดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="9d961-121">Admin settings</span></span> | <span data-ttu-id="9d961-122">การตั้งค่าคอนฟิกศูนย์ดูแล Attract</span><span class="sxs-lookup"><span data-stu-id="9d961-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="9d961-123">ผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="9d961-123">Candidates</span></span> | <span data-ttu-id="9d961-124">ผู้สมัครทั้งหมดที่ได้รับการเพิ่มเข้าในกลุ่มงานหรือกลุ่มผู้มีความสามารถพิเศษ</span><span class="sxs-lookup"><span data-stu-id="9d961-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="9d961-125">เท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="9d961-125">Email templates</span></span> | <span data-ttu-id="9d961-126">แม่แบบอีเมลทั้งหมดที่ได้รับการตั้งค่าคอนฟิกสำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9d961-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="9d961-127">แม่แบบในแพคเกจข้อเสนองาน</span><span class="sxs-lookup"><span data-stu-id="9d961-127">Job offer package templates</span></span> | <span data-ttu-id="9d961-128">แม่แบบของแพคเกจนำเสนองานทั้งหมดที่สร้างขึ้น รวมทั้งการตั้งค่าคอนฟิกที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="9d961-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="9d961-129">ชุดกฎข้อเสนองาน</span><span class="sxs-lookup"><span data-stu-id="9d961-129">Job offer rule sets</span></span> |  <span data-ttu-id="9d961-130">ไฟล์ชุดกฎทั้งหมดที่ได้รับการอัพโหลดสำหรับการจัดการข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="9d961-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="9d961-131">แม่แบบข้อเสนองาน</span><span class="sxs-lookup"><span data-stu-id="9d961-131">Job offer templates</span></span> | <span data-ttu-id="9d961-132">แม่แบบเอกสารข้อเสนองานทั้งหมด ที่สร้างขึ้นสำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9d961-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="9d961-133">งานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="9d961-133">Job openings</span></span> | <span data-ttu-id="9d961-134">งานที่สร้างทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9d961-134">All created jobs.</span></span> <span data-ttu-id="9d961-135">ไม่มีการส่งออกงานที่ถูกลบไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="9d961-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="9d961-136">โฟลเดอร์ย่อยจะมีใบสมัครของผู้สมัคร พร้อมกับโฟลเดอร์ย่อยสำหรับไฟล์แนบของใบสมัคร และข้อเสนอของแพคเกจที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9d961-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="9d961-137">แม่แบบงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="9d961-137">Job opening templates</span></span> | <span data-ttu-id="9d961-138">แม่แบบแม่แบบกระบวนการงานที่ได้รับการตั้งค่าคอนฟิกในสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9d961-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="9d961-139">กลุ่มผู้มีความสามารถพิเศษ</span><span class="sxs-lookup"><span data-stu-id="9d961-139">Talent pools</span></span> | <span data-ttu-id="9d961-140">กลุ่มผู้มีความสามารถพิเศษทั้งหมดที่สร้างขึ้น รายชื่อผู้สนับสนุน และรายชื่อผู้สมัครสำหรับกลุ่มผู้มีความสามารถพิเศษ</span><span class="sxs-lookup"><span data-stu-id="9d961-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="9d961-141">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9d961-141">Workers</span></span> | <span data-ttu-id="9d961-142">รายชื่อผู้ปฏิบัติงานทั้งหมดที่มีอยู่ในสภาพแวดล้อม รวมถึงบทบาทของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9d961-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="9d961-143">(โฟลเดอร์ราก)</span><span class="sxs-lookup"><span data-stu-id="9d961-143">(root folder)</span></span> | <span data-ttu-id="9d961-144">ไฟล์เค้าร่าง JSON ที่อธิบายถึงฟิลด์โครงสร้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9d961-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="9d961-145">จำกัดการเข้าถึง Attract</span><span class="sxs-lookup"><span data-stu-id="9d961-145">Restrict access to Attract</span></span>

<span data-ttu-id="9d961-146">เมื่อคุณพร้อมที่จะย้ายแล้ว ให้จำกัดการเข้าถึงที่ไม่ใช่ผู้ดูแลระบบไปยังสภาพแวดล้อม Attract ของคุณ แล้วส่งออกข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="9d961-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="9d961-147">การจำกัดการเข้าถึงสภาพแวดล้อมที่ Attract ของคุณเป็นแบบถาวรและไม่สามารถยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="9d961-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="9d961-148">ถ้าคุณต้องการให้ผู้ใช้ที่ไม่ใช่ผู้ดูแลระบบเข้าถึงสภาพแวดล้อมของคุณต่อไป ให้ข้ามขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="9d961-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="9d961-149">ไปที่ [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport)</span><span class="sxs-lookup"><span data-stu-id="9d961-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="9d961-150">เมื่อต้องการจำกัดการเข้าถึงที่ไม่ใช่ผู้ดูแลระบบจากการเข้าถึงสภาพแวดล้อม Attract ของคุณ ภายใต้ **จำกัดการเข้าถึงแอปนี้** เลือกที่ **จำกัดการเข้าถึงเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="9d961-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="9d961-151">การจำกัดการเข้าถึงยัง ยกเลิกการลงประกาศงานที่ใช้งานอยู่ใด ๆ ที่มีการประกาศแล้ว</span><span class="sxs-lookup"><span data-stu-id="9d961-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="9d961-152">จำกัดการเข้าถึง Attract จากผู้ที่ไม่ใช่ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="9d961-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="9d961-153">เมื่อคุณเห็นคำเตือน **นี้เป็นการเปลี่ยนแปลงถาวร** ให้เลือก **จำกัดการเข้าถึง** เพื่อจำกัดผู้ใช้ที่ไม่ใช่ผู้ดูแลระบบจากสภาพแวดล้อมนี้อย่างถาวร</span><span class="sxs-lookup"><span data-stu-id="9d961-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="9d961-154">หากคุณยังไม่พร้อมที่จะทำขั้นตอนนี้ให้เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="9d961-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="9d961-155">คำเตือนว่าการจำกัดการเข้าถึงเป็นการเปลี่ยนแปลงโดยถาวร</span><span class="sxs-lookup"><span data-stu-id="9d961-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="9d961-156">ผู้ดูแลระบบสามารถเข้าถึงหน้ารายงานการส่งออก และการส่งออกข้อมูลของบุคคลหลังจากที่คุณจำกัดการเข้าถึงสภาพแวดล้อม Attract</span><span class="sxs-lookup"><span data-stu-id="9d961-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="9d961-157">ส่งออกข้อมูลจาก Onboard</span><span class="sxs-lookup"><span data-stu-id="9d961-157">Export data from Onboard</span></span>

<span data-ttu-id="9d961-158">เมื่อคุณพร้อมแล้ว คุณสามารถดาวน์โหลดแม่แบบ คู่มือ และข้อมูลผู้สมัครจากบน Onboard</span><span class="sxs-lookup"><span data-stu-id="9d961-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="9d961-159">ไปที่ [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport)</span><span class="sxs-lookup"><span data-stu-id="9d961-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="9d961-160">ภายใต้ **การส่งออกข้อมูล** ให้เลือก **การร้องขอการส่งออกข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="9d961-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="9d961-161">ร้องขอการส่งออกข้อมูลจาก Onboard</span><span class="sxs-lookup"><span data-stu-id="9d961-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="9d961-162">เมื่อมีกล่องข้อความปรากฏ **การประมวลผลคำขอของคุณกำลังถูกจัดการ** ขึ้น **ให้เลือกตกลง**</span><span class="sxs-lookup"><span data-stu-id="9d961-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="9d961-163">การส่งออกข้อมูลอาจใช้เวลานานถึง 20 นาที ทั้งนี้ขึ้นอยู่กับขนาดของการส่งออกของคุณ</span><span class="sxs-lookup"><span data-stu-id="9d961-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="9d961-164">เมื่อการส่งออกของคุณเสร็จสมบูรณ์ ให้เลือกปุ่ม **ดาวน์โหลด** ที่อยู่ถัดไป</span><span class="sxs-lookup"><span data-stu-id="9d961-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="9d961-165">ดาวน์โหลดข้อมูลที่ส่งออกจาก Onboard</span><span class="sxs-lookup"><span data-stu-id="9d961-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="9d961-166">การส่งออกข้อมูลของคุณจะใช้งานได้เจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="9d961-166">Your data export is available for seven days.</span></span> <span data-ttu-id="9d961-167">หลังจากวันที่เจ็ดวันลิงก์ **ดาวน์โหลด** จะหมดอายุ และคุณต้องร้องขอการส่งออกใหม่ ถ้าคุณต้องการดาวน์โหลดข้อมูลของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="9d961-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="9d961-168">เมื่อคุณเริ่มต้นการส่งออกข้อมูลใหม่ การดาวน์โหลดใด ๆ ที่มีอยู่จะหมดอายุ หลังจากการส่งออกใหม่สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="9d961-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="9d961-169">ไฟล์ดาวน์โหลดเป็นไฟล์ .zip ที่มี:</span><span class="sxs-lookup"><span data-stu-id="9d961-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="9d961-170">โฟลเดอร์ **แม่แบบ** ที่มีแม่แบบ Onboard ของคุณในรูปแบบเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="9d961-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="9d961-171">โฟลเดอร์ **คู่มือ** ที่มีคู่มือ Onboard ของคุณในรูปแบบเอกสาร Word</span><span class="sxs-lookup"><span data-stu-id="9d961-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d961-172">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="9d961-172">See also</span></span>

[<span data-ttu-id="9d961-173">การเลิกใช้แอป Dynamics 365 Talent: Attract และ Dynamics 365 Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="9d961-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)