---
title: ใช้พื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดสินทรัพย์ถาวร
author: josaw1
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 65b3261367243b747b790c4a9ce5b4189aca85c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260141"
---
# <a name="use-the-asset-management-mobile-workspace"></a><span data-ttu-id="5ba56-103">ใช้พื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="5ba56-103">Use the Asset management mobile workspace</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ba56-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับ **การจัดสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5ba56-104">This topic provides information about the **Asset management** mobile workspace.</span></span> <span data-ttu-id="5ba56-105">พื้นที่ทำงานนี้จะช่วยให้ผู้ใช้สามารถดูและสร้างคำขอการบำรุงรักษาและใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="5ba56-105">This workspace lets users view and create maintenance requests and work orders.</span></span> <span data-ttu-id="5ba56-106">นอกจากนี้ผู้ใช้ยังสามารถดูงานในใบสั่งงานที่กำหนดไว้ในปฏิทินหรือมุมมองรายการได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="5ba56-106">Users can also view the assigned work order jobs in a calendar or list view.</span></span> <span data-ttu-id="5ba56-107">นอกจากนี้คุณยังสามารถดูและค้นหาสินทรัพย์และสถานที่ทำงานได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="5ba56-107">Assets and functional locations can also be viewed and searched for.</span></span>

## <a name="overview"></a><span data-ttu-id="5ba56-108">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="5ba56-108">Overview</span></span>

<span data-ttu-id="5ba56-109">การจัดการสินทรัพย์เป็นโมดูลขั้นสูงสำหรับการจัดการสินทรัพและงานใบสั่งงานใน Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ba56-109">Asset Management is an advanced module for managing assets and work order jobs in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5ba56-110">พื้นที่การทำงานบนอุปกรณ์เคลื่อนที่ **การจัดการสินทรัพย์** ช่วยให้ผู้ใช้สามารถดูงานใบสั่งงานที่มอบหมายให้กับผู้ใช้ได้จากอุปกรณ์เคลื่อนที่ตามตัวเลือกของผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="5ba56-110">The **Asset management** mobile workspace lets users quickly view assigned work order jobs on the mobile device of their choice.</span></span> <span data-ttu-id="5ba56-111">นอกจากนี้ ผู้ใช้ยังสามารถสร้างและจัดการคำขอการบำรุงรักษา อัพเดตสถานะของวงจรการใช้ ดูสินทรัพย์ และรายละเอียดตำแหน่งที่ทำงานโดยใช้อุปกรณ์เคลื่อนที่ของผู้ใช้เอง</span><span class="sxs-lookup"><span data-stu-id="5ba56-111">Users can also create and manage maintenance requests, update lifecycle state, and view asset and functional location details by using their mobile device.</span></span>

<span data-ttu-id="5ba56-112">โดยเฉพาะอย่างยิ่ง พื้นที่ทำงานบนอุปกรณ์เคลื่อนที่ **การจัดการสินทรัพย์** ช่วยให้ผู้ใช้ดำเนินงานต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="5ba56-112">Specifically, the **Asset management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="5ba56-113">สร้าง ดู และแก้ไขคำขอการบำรุงรักษา ถ่ายรูป หรือแนบรูปภาพที่มีอยู่ไปยังคำขอบำรุงรักษา เปลี่ยนสถานะของวงจรการใช้ของคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="5ba56-113">Create, view, and edit maintenance requests, take a photo or attach an existing image to the maintenance request, change the maintenance request lifecycle state.</span></span> 
- <span data-ttu-id="5ba56-114">สร้าง ดู และแก้ไขใบสั่งงาน ถ่ายรูป หรือแนบรูปภาพที่มีอยู่ไปยังใบสั่งงาน เปลี่ยนสถานะของวงจรการใช้ของใบสั่งงาน ดูงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-114">Create, view, and edit work orders, take a photo or attach an existing image to the work order, change the work order lifecycle state, view work order jobs.</span></span>
- <span data-ttu-id="5ba56-115">ดูงานของใบสั่งงานที่มอบหมายในมุมมองปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="5ba56-115">View assigned work order jobs in a calendar view.</span></span>
- <span data-ttu-id="5ba56-116">สร้าง ดู และแก้ไขงานงานใบสั่งงาน อัพเดตตัวนับสินทรัพย์ ดูรายการตรวจสอบการบำรุงรักษา ดูและแก้ไขบันทึกงานใบสั่งงาน ดูเครื่องมือที่จำเป็นสำหรับงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-116">Create, view, and edit work order job, update asset counters, view maintenance checklist, view and edit work order job notes, view the tools required for the work order job.</span></span>
- <span data-ttu-id="5ba56-117">ดูหรือค้นหาสินทรัพย์เฉพาะหรือตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-117">View or search for a specific asset or functional location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5ba56-118">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="5ba56-118">Prerequisites</span></span>

<span data-ttu-id="5ba56-119">ก่อนที่คุณจะสามารถใช้พื้นที่ทำงานแบบเคลื่อนที่ **การจัดการสินทรัพย์** ผู้ดูแลระบบของคุณต้องตั้งค่าบัญชีผู้ใช้และผู้ปฏิบัติงานที่จำเป็น และเผยแพร่พื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-119">Before you can use the **Asset management** mobile workspace, your admin must set up the required user and worker accounts, and publish the workspace.</span></span> <span data-ttu-id="5ba56-120">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ตั้งค่าพื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์](set-up-asset-management-mobile.md)</span><span class="sxs-lookup"><span data-stu-id="5ba56-120">For more information, see [Set up the Asset management mobile workspace](set-up-asset-management-mobile.md).</span></span>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="5ba56-121">ดาวน์โหลดและติดตั้งแอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="5ba56-121">Download and install the mobile app</span></span>

<span data-ttu-id="5ba56-122">ดาวน์โหลดและติดตั้งแอพบนมือถือ Dynamics 365 for Unified Operations</span><span class="sxs-lookup"><span data-stu-id="5ba56-122">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="5ba56-123">สำหรับโทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="5ba56-123">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="5ba56-124">สำหรับ iPhone</span><span class="sxs-lookup"><span data-stu-id="5ba56-124">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="5ba56-125">ล็อกอินเข้าสู่แอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="5ba56-125">Sign in to the mobile app</span></span>

1. <span data-ttu-id="5ba56-126">เริ่มการทำงานแอพบนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ba56-126">Start the app on your mobile device.</span></span>

1. <span data-ttu-id="5ba56-127">ป้อน URL ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5ba56-127">Enter your Dynamics 365 URL.</span></span>

1. <span data-ttu-id="5ba56-128">ในครั้งแรกที่คุณเข้าสู่ระบบ ระบบจะขอให้คุณป้อนชื่อผู้ใช้และรหัสผ่านของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ba56-128">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="5ba56-129">ป้อนข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ba56-129">Enter your credentials.</span></span>

1. <span data-ttu-id="5ba56-130">หลังจากที่คุณลงชื่อเข้าใช้แล้ว พื้นที่ทำงานที่พร้อมใช้งานสำหรับบริษัทของคุณจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="5ba56-130">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="5ba56-131">โปรดทราบว่า ถ้าผู้ดูแลระบบของคุณเผยแพร่พื้นที่ทำงานใหม่ในภายหลัง คุณจะต้องรีเฟรชรายการของพื้นที่ทำงานแบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="5ba56-131">Note that if your system administrator publishes a new workspace later, you'll have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="5ba56-132">![เลือกพื้นที่ทำงาน](media/am-mobile-01.png "เลือกพื้นที่ทำงาน")</span><span class="sxs-lookup"><span data-stu-id="5ba56-132">![Select a workspace](media/am-mobile-01.png "Select a workspace")</span></span>

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a><span data-ttu-id="5ba56-133">ดูงานใบสั่งงานที่มอบหมายในมุมมองปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="5ba56-133">View assigned work order jobs in calendar view</span></span>

1. <span data-ttu-id="5ba56-134">บนอุปกรณ์เคลื่อนที่ของคุณ เปิดพื้นที่ทำงาน **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5ba56-134">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="5ba56-135">เลือก **ปฏิทินงานใบสั่งงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="5ba56-135">Select **My work order jobs calendar**.</span></span>

1. <span data-ttu-id="5ba56-136">เลือกวันที่ที่คุณต้องการดูงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-136">Select the date you want to view work order jobs for.</span></span> <span data-ttu-id="5ba56-137">ในรายการ คุณจะเห็นรหัสสินทรัพย์และรหัสตำแหน่งที่ทำงานสำหรับแต่ละงานในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-137">In the list, you'll see the asset ID and functional location ID for each work order job.</span></span>

1. <span data-ttu-id="5ba56-138">เลือกงานใบสั่งงานจากในรายการเพื่อดูรายละเอียดงาน: รายละเอียดสินทรัพย์ และตำแหน่งที่ทำงานรวมไปถึงลิงก์นำทางอื่น ๆ เพื่อดู **ไฟล์แนบ** **รายการตรวจสอบ** **เครื่องมือ** **ตัวนับสินทรัพย์** **บันทึก** **สมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="5ba56-138">Select a work order job in the list to see job details: Asset and functional location details as well as other navigation links to view **Attachments**, **Checklists**, **Tools**, **Asset counters**, **Notes**, **Journals**.</span></span>

    <span data-ttu-id="5ba56-139">![ดูงานใบสั่งงานที่มอบหมายในมุมมองปฏิทิน](media/am-mobile-02.png "ดูงานใบสั่งงานที่มอบหมายในมุมมองปฏิทิน")</span><span class="sxs-lookup"><span data-stu-id="5ba56-139">![View assigned work order jobs in calendar view](media/am-mobile-02.png "View assigned work order jobs in calendar view")</span></span>

## <a name="create-a-work-order-job"></a><span data-ttu-id="5ba56-140">สร้างงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-140">Create a work order job</span></span>

1. <span data-ttu-id="5ba56-141">บนอุปกรณ์เคลื่อนที่ของคุณ เปิดพื้นที่ทำงาน **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5ba56-141">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="5ba56-142">เลือก **ใบสั่งงานการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5ba56-142">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="5ba56-143">เลือกใบสั่งงานที่คุณต้องการสร้างงานใบสั่งงานให้</span><span class="sxs-lookup"><span data-stu-id="5ba56-143">Select the work order you want to create a new work order job for.</span></span>

1. <span data-ttu-id="5ba56-144">เลือกปุ่ม **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="5ba56-144">Select the **Add line** button.</span></span>

1. <span data-ttu-id="5ba56-145">เลือก **สินทรัพย์** ที่คุณต้องการสร้างงานใบสั่งงานให้</span><span class="sxs-lookup"><span data-stu-id="5ba56-145">Select the **Asset** you want to create a work order job for.</span></span>

1. <span data-ttu-id="5ba56-146">เลือก **ชนิดงานการบำรุงรักษา** **ตัวแปรชนิดงานการบำรุงรักษา** และ **การค้า**</span><span class="sxs-lookup"><span data-stu-id="5ba56-146">Select **Maintenance job type**, **Maintenance job type variant** and **Trade**.</span></span>

1. <span data-ttu-id="5ba56-147">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="5ba56-147">Select **Done**.</span></span>

    <span data-ttu-id="5ba56-148">![หน้าจอเพิ่มรายการ](media/am-mobile-03.png "หน้าจอเพิ่มรายการ")</span><span class="sxs-lookup"><span data-stu-id="5ba56-148">![The Add line screen](media/am-mobile-03.png "The Add line screen")</span></span>


## <a name="add-attachment-to-a-work-order-job"></a><span data-ttu-id="5ba56-149">เพิ่มไฟล์แนบให้กับงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-149">Add attachment to a work order job</span></span>

1. <span data-ttu-id="5ba56-150">บนอุปกรณ์เคลื่อนที่ของคุณ เปิดพื้นที่ทำงาน **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5ba56-150">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="5ba56-151">เลือก **ใบสั่งงานการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5ba56-151">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="5ba56-152">เลือกใบสั่งงาน > งานใบสั่งงานที่คุณต้องการเพิ่มไฟล์แนบให้</span><span class="sxs-lookup"><span data-stu-id="5ba56-152">Select the work order > work order job you want to add an attachment to.</span></span>
    - <span data-ttu-id="5ba56-153">อีกทางเลือกหนึ่ง คุณยังสามารถเลือก **ปฏิทินงานใบสั่งงานของฉัน** หรือ **รายการงานใบสั่งงานของฉัน** บนหน้าแรกเพื่อนำทางไปยังเพจ **รายละเอียดงานใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="5ba56-153">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **Work order job details** page.</span></span>

1. <span data-ttu-id="5ba56-154">เลือก **ไฟล์แนบ** ในเพจ **รายละเอียดงานใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="5ba56-154">Select **Attachments** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="5ba56-155">คุณจะเห็นไฟล์แนบที่มีอยู่ในงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-155">You'll see existing attachments on the work order job.</span></span> <span data-ttu-id="5ba56-156">เลือก **เพิ่มไฟล์แนบ**</span><span class="sxs-lookup"><span data-stu-id="5ba56-156">Select **Add attachment**.</span></span>

1. <span data-ttu-id="5ba56-157">ป้อน **ชื่อ** และ **บันทึกย่อ** สำหรับไฟล์แนบ</span><span class="sxs-lookup"><span data-stu-id="5ba56-157">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="5ba56-158">เลือก **เลือกรูปภาพ** เพื่อเลือกรูปภาพจากแกลเลอรีบนอุปกรณ์เคลื่อนที่ หรือเลือก **ถ่ายรูป** เพื่อถ่ายรูป</span><span class="sxs-lookup"><span data-stu-id="5ba56-158">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="5ba56-159">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="5ba56-159">Select **Done**.</span></span>

    <span data-ttu-id="5ba56-160">![ดูและเพิ่มเอกสารแนบสำหรับงานใบสั่งงาน](media/am-mobile-04.png "ดูและเพิ่มเอกสารแนบสำหรับงานใบสั่งงาน")</span><span class="sxs-lookup"><span data-stu-id="5ba56-160">![View and add attachments for a work order job](media/am-mobile-04.png "View and add attachments for a work order job")</span></span>

## <a name="view-maintenance-checklist-on-a-work-order-job"></a><span data-ttu-id="5ba56-161">ดูรายการตรวจสอบการบำรุงรักษาบนงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-161">View maintenance checklist on a work order job</span></span>

1. <span data-ttu-id="5ba56-162">บนอุปกรณ์เคลื่อนที่ของคุณ เปิดพื้นที่ทำงาน **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5ba56-162">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="5ba56-163">เลือก **ใบสั่งงานการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5ba56-163">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="5ba56-164">เลือกใบสั่งงาน > งานใบสั่งงาน ที่คุณต้องการดูรายการตรวจสอบของงานนั้น</span><span class="sxs-lookup"><span data-stu-id="5ba56-164">Select the work order > work order job you want to view checklists for.</span></span>
    - <span data-ttu-id="5ba56-165">อีกทางเลือกหนึ่ง คุณยังสามารถเลือก **ปฏิทินงานใบสั่งงานของฉัน** หรือ **รายการงานใบสั่งงานของฉัน** บนหน้าแรกเพื่อนำทางไปยังเพจ **รายละเอียดงานใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="5ba56-165">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="5ba56-166">เลือก **รายการตรวจสอบ** ในเพจ **รายละเอียดงานใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="5ba56-166">Select **Checklists** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="5ba56-167">คุณจะเห็นรายการตรวจสอบที่เกี่ยวข้องกับงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-167">You'll see a list of checklist lines related to the work order job.</span></span> <span data-ttu-id="5ba56-168">เลือกรายการตรวจสอบเพื่อดู **คำแนะนำ** และเพิ่ม **บันทึกย่อ**</span><span class="sxs-lookup"><span data-stu-id="5ba56-168">Select a checklist line to view **Instructions** and add **Notes**.</span></span>

1. <span data-ttu-id="5ba56-169">เลือกปุ่มย้อนกลับ (**<**) เพื่อกลับไปยังเพจก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="5ba56-169">Select the back button (**<**) to return to the previous page.</span></span>

    <span data-ttu-id="5ba56-170">![รายการตรวจสอบการบํารุงรักษาและรายละเอียดรายการ](media/am-mobile-05.png "รายการตรวจสอบการบํารุงรักษาและรายละเอียดรายการ")</span><span class="sxs-lookup"><span data-stu-id="5ba56-170">![Maintenance checklist and line details](media/am-mobile-05.png "Maintenance checklist and line details")</span></span>

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a><span data-ttu-id="5ba56-171">ดูและอัพเดตตัวนับสินทรัพย์บนงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-171">View and update asset counters on a work order job</span></span>

1. <span data-ttu-id="5ba56-172">บนอุปกรณ์เคลื่อนที่ของคุณ เปิดพื้นที่ทำงาน **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5ba56-172">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="5ba56-173">เลือก **ใบสั่งงานการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5ba56-173">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="5ba56-174">เลือกใบสั่งงาน > งานใบสั่งงาน ที่คุณต้องการดูตัวนับสินทรัพย์ของงานนั้น</span><span class="sxs-lookup"><span data-stu-id="5ba56-174">Select the work order > work order job you want to view asset counters for.</span></span>
    - <span data-ttu-id="5ba56-175">อีกทางเลือกหนึ่ง คุณยังสามารถเลือก **ปฏิทินงานใบสั่งงานของฉัน** หรือ **รายการงานใบสั่งงานของฉัน** บนหน้าแรกเพื่อนำทางไปยังเพจ **รายละเอียดงานใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="5ba56-175">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="5ba56-176">เลือก **ตัวนับสินทรัพย์** ในเพจ **รายละเอียดงานใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="5ba56-176">Select **Asset counters** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="5ba56-177">คุณจะเห็นตัวนับสินทรัพย์ที่เกี่ยวข้องกับงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-177">You see a list of asset counters related to the work order job.</span></span> <span data-ttu-id="5ba56-178">เลือกไอคอนดินสอบนรายการตัวนับสินทรัพย์เพื่ออัพเดตค่าตัวนับ</span><span class="sxs-lookup"><span data-stu-id="5ba56-178">Select the pencil icon on an asset counter line to update the counter value.</span></span>

1. <span data-ttu-id="5ba56-179">ป้อนค่าตัวนับใหม่แล้วเลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="5ba56-179">Enter a new counter value, and select **Done**.</span></span>

    <span data-ttu-id="5ba56-180">![ดูและอัพเดตตัวนับสินทรัพย์](media/am-mobile-06.png "ดูและอัพเดตตัวนับสินทรัพย์")</span><span class="sxs-lookup"><span data-stu-id="5ba56-180">![View and update asset counters](media/am-mobile-06.png "View and update asset counters")</span></span>

## <a name="register-consumption-on-a-work-order-job"></a><span data-ttu-id="5ba56-181">ลงทะเบียนปริมาณการใช้ในงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-181">Register consumption on a work order job</span></span>

1. <span data-ttu-id="5ba56-182">บนอุปกรณ์เคลื่อนที่ของคุณ เปิดพื้นที่ทำงาน **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5ba56-182">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="5ba56-183">เลือก **ใบสั่งงานการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5ba56-183">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="5ba56-184">เลือกใบสั่งงาน > งานใบสั่งงานที่คุณต้องการเพิ่มการลงทะเบียนปริมาณการใช้ให้</span><span class="sxs-lookup"><span data-stu-id="5ba56-184">Select the work order > work order job you want to add consumption registrations for.</span></span>
    - <span data-ttu-id="5ba56-185">อีกทางเลือกหนึ่ง คุณยังสามารถเลือก **ปฏิทินงานใบสั่งงานของฉัน** หรือ **รายการงานใบสั่งงานของฉัน** บนหน้าแรกเพื่อนำทางไปยังเพจ **รายละเอียดงานใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="5ba56-185">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="5ba56-186">เลือก **บันทึกรายวัน** ในเพจ **รายละเอียดงานใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="5ba56-186">Select **Journals** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="5ba56-187">เลือก **เพิ่มชั่วโมง** เพื่อสร้างการลงทะเบียนชั่วโมงทำงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-187">Select **Add hours** to create work hour registrations.</span></span>
    1. <span data-ttu-id="5ba56-188">เลือก **ประเภท** จากการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5ba56-188">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="5ba56-189">ในฟิลด์ **ชั่วโมง** ให้ป้อนจำนวนชั่วโมงทำงานที่ใช้ในงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-189">In the **Hours** field, enter the number of work hours spent on the work order job.</span></span>
    1. <span data-ttu-id="5ba56-190">เลือก **คุณสมบัติของรายการ** ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="5ba56-190">Select the appropriate **Line property**.</span></span>
    1. <span data-ttu-id="5ba56-191">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="5ba56-191">Select **Done**.</span></span>

1. <span data-ttu-id="5ba56-192">เลือก **เพิ่มสินค้า** เพื่อสร้างการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="5ba56-192">Select **Add items** to create item registrations.</span></span>
    1. <span data-ttu-id="5ba56-193">เลือก **หมายเลขสินค้า** จากการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5ba56-193">Select the **Item number** from the lookup.</span></span>
    1. <span data-ttu-id="5ba56-194">เลือก **ไซต์** จากการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5ba56-194">Select the **Site** from the lookup.</span></span>
    1. <span data-ttu-id="5ba56-195">ป้อน **ปริมาณ** ของสินค้าที่ใช้</span><span class="sxs-lookup"><span data-stu-id="5ba56-195">Enter the **Quantity** of items consumed.</span></span>
    1. <span data-ttu-id="5ba56-196">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="5ba56-196">Select **Done**.</span></span>

1. <span data-ttu-id="5ba56-197">เลือก **เพิ่มค่าใช้จ่าย** เพื่อสร้างการลงทะเบียนค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="5ba56-197">Select **Add expense** to create expense registrations.</span></span>
    1. <span data-ttu-id="5ba56-198">เลือก **ประเภท** จากการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5ba56-198">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="5ba56-199">ป้อนปริมาณสำหรับการลงทะเบียนค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="5ba56-199">Enter the quantity for the expense registration.</span></span>
    1. <span data-ttu-id="5ba56-200">เลือก **สกุลเงินที่ใช้ในการขาย** จากการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5ba56-200">Select the **Sales currency** from the lookup.</span></span>
    1. <span data-ttu-id="5ba56-201">ป้อน **ราคาต้นทุน** สำหรับการลงทะเบียนค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="5ba56-201">Enter the **Cost price** for the expense registration.</span></span>
    1. <span data-ttu-id="5ba56-202">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="5ba56-202">Select **Done**.</span></span>

    <span data-ttu-id="5ba56-203">![อัพเดตสมุดรายวันใบสั่งงาน](media/am-mobile-07.png "อัพเดตสมุดรายวันใบสั่งงาน")</span><span class="sxs-lookup"><span data-stu-id="5ba56-203">![Update a work order journal](media/am-mobile-07.png "Update a work order journal")</span></span>

## <a name="update-lifecycle-state-on-a-work-order"></a><span data-ttu-id="5ba56-204">อัพเดตสถานะของวงจรการใช้ในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="5ba56-204">Update lifecycle state on a work order</span></span>

1. <span data-ttu-id="5ba56-205">บนอุปกรณ์เคลื่อนที่ของคุณ เปิดพื้นที่ทำงาน **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5ba56-205">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="5ba56-206">เลือก **ใบสั่งงานการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5ba56-206">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="5ba56-207">เลือกใบสั่งงาน ที่คุณต้องการอัพเดตสถานะของวงจรการใช้ให้</span><span class="sxs-lookup"><span data-stu-id="5ba56-207">Select the work order you want to update lifecycle state for.</span></span>

1. <span data-ttu-id="5ba56-208">เลือกปุ่ม **อัพเดตสถานะ** ที่อยู่ด้านล่างของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="5ba56-208">Select the **Update state** button at the bottom of the screen.</span></span>

1. <span data-ttu-id="5ba56-209">เลือกสถานะของวงจนการใช้ใหม่จากในรายการ</span><span class="sxs-lookup"><span data-stu-id="5ba56-209">Select a new lifecycle state from the list.</span></span>

1. <span data-ttu-id="5ba56-210">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="5ba56-210">Select **Done**.</span></span>

    <span data-ttu-id="5ba56-211">![อัพเดตสถานะของวงจรการใช้ในใบสั่งงาน](media/am-mobile-08.png "อัพเดตสถานะของวงจรการใช้ในใบสั่งงาน")</span><span class="sxs-lookup"><span data-stu-id="5ba56-211">![Update lifecycle state on a work order](media/am-mobile-08.png "Update lifecycle state on a work order")</span></span>

## <a name="create-a-maintenance-request"></a><span data-ttu-id="5ba56-212">สร้างคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="5ba56-212">Create a maintenance request</span></span>

1. <span data-ttu-id="5ba56-213">บนอุปกรณ์เคลื่อนที่ของคุณ เปิดพื้นที่ทำงาน **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5ba56-213">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="5ba56-214">เลือก **คำขอการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5ba56-214">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="5ba56-215">เลือก **การดำเนินการ** ที่ด้านล่างของหน้าจอ และเลือก **สร้างคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="5ba56-215">Select **Actions** at the bottom of the screen, and select **Create maintenance request**.</span></span>

1. <span data-ttu-id="5ba56-216">หากลำดับหมายเลขถูกเปิดใช้งานสำหรับคำขอการบำรุงรักษาใน **การจัดการสินทรัพย์** ฟิลด์ **คำขอการบำรุงรักษา** จะถูกซ่อนไว้ เนื่องจากจะถูกป้อนข้อมูลโดยอัตโนมัติ หากฟิลด์ **คำขอการบำรุงรักษา** สามารถมองเห็นได้ ให้ป้อนรหัสคำขอการบำรุงรักษาลงในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="5ba56-216">If number sequence is enabled for maintenance requests in **Asset management**, the **Maintenance request** field is hidden because it is automatically filled out. If the **Maintenance request** field is visible, enter a maintenance request ID.</span></span>

1. <span data-ttu-id="5ba56-217">เลือก **ชนิดคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="5ba56-217">Select a **Maintenance request type**.</span></span>

1. <span data-ttu-id="5ba56-218">ป้อน **คำอธิบาย** สำหรับคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="5ba56-218">Enter a **Description** for the maintenance request.</span></span>

1. <span data-ttu-id="5ba56-219">เลือก **สินทรัพย์** ที่คุณต้องการสร้างคำขอให้</span><span class="sxs-lookup"><span data-stu-id="5ba56-219">Select the **Asset** you want to create the request for.</span></span>

1. <span data-ttu-id="5ba56-220">เลือก **ระดับการบริการ** สำหรับคำขอขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="5ba56-220">Select the **Service level** for the maintenance request.</span></span>

1. <span data-ttu-id="5ba56-221">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="5ba56-221">Select **Done**.</span></span>

    <span data-ttu-id="5ba56-222">![สร้างคำขอการบำรุงรักษา](media/am-mobile-09.png "สร้างคำขอการบำรุงรักษา")</span><span class="sxs-lookup"><span data-stu-id="5ba56-222">![Create a maintenance request](media/am-mobile-09.png "Create a maintenance request")</span></span>

## <a name="add-attachment-to-a-maintenance-request"></a><span data-ttu-id="5ba56-223">เพิ่มไฟลแนบไปยังคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="5ba56-223">Add attachment to a maintenance request</span></span>

1. <span data-ttu-id="5ba56-224">บนอุปกรณ์เคลื่อนที่ของคุณ เปิดพื้นที่ทำงาน **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="5ba56-224">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="5ba56-225">เลือก **คำขอการบำรุงรักษาทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5ba56-225">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="5ba56-226">เลือกคำขอการบำรุงรักษาที่คุณต้องการเพิ่มไฟล์แนบ</span><span class="sxs-lookup"><span data-stu-id="5ba56-226">Select the maintenance request you want to add an attachment to.</span></span>

1. <span data-ttu-id="5ba56-227">เลือก **ไฟล์แนบ** ที่ด้านล่างของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="5ba56-227">Select **Attachments** at the bottom of the screen.</span></span>

1. <span data-ttu-id="5ba56-228">เลือก **เพิ่มไฟล์แนบ**</span><span class="sxs-lookup"><span data-stu-id="5ba56-228">Select **Add attachments**.</span></span>

1. <span data-ttu-id="5ba56-229">ป้อน **ชื่อ** และ **บันทึกย่อ** สำหรับไฟล์แนบ</span><span class="sxs-lookup"><span data-stu-id="5ba56-229">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="5ba56-230">เลือก **เลือกรูปภาพ** เพื่อเลือกรูปภาพจากแกลเลอรีบนอุปกรณ์เคลื่อนที่ หรือ **ถ่ายรูป** เพื่อถ่ายรูป</span><span class="sxs-lookup"><span data-stu-id="5ba56-230">Select **Choose image** to select a photo from the mobile gallery or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="5ba56-231">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="5ba56-231">Select **Done**.</span></span>

    <span data-ttu-id="5ba56-232">![เพิ่มไฟล์แนบไปยังคำขอการบำรุงรักษา](media/am-mobile-10.png "เพิ่มไฟล์แนบไปยังคำขอการบำรุงรักษา")</span><span class="sxs-lookup"><span data-stu-id="5ba56-232">![Add an attachment to a maintenance request](media/am-mobile-10.png "Add an attachment to a maintenance request")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]