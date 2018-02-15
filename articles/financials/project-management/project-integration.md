---
title: "การรวม Microsoft Project client"
description: "การวางแผนและการรักษากำหนดการโครงการอาจซับซ้อน ดังนั้นผู้จัดการโครงการต้องใช้เครื่องมือที่ช่วยในการจัดการงานนี้ การรวมกับ Microsoft Project Client ให้การสนับสนุนในการเปิดและจัดการโครงสร้างการแบ่งงานของโครงการ"
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: a72963f755f8eddb19b8526d2938eff039ab7df2
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---

# <a name="microsoft-project-client-integration"></a><span data-ttu-id="f8b2d-104">การรวม Microsoft Project client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-104">Microsoft Project client integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f8b2d-105">การวางแผนและการรักษากำหนดการโครงการอาจซับซ้อน ดังนั้นผู้จัดการโครงการต้องใช้เครื่องมือที่ช่วยในการจัดการงานนี้</span><span class="sxs-lookup"><span data-stu-id="f8b2d-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="f8b2d-106">การรวมกับ Microsoft Project Client ให้การสนับสนุนในการเปิดและจัดการโครงสร้างการแบ่งงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="f8b2d-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="f8b2d-107">ผู้จัดการโครงการสามารถประกาศการเปลี่ยนแปลงใดๆ กลับไปยังโครงสร้างการแบ่งงานของโครงการ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f8b2d-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="f8b2d-108">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition การอัพเดตเดือนกรกฎาคม 2017 คุณต้องติดตั้ง KB 4054797 และ 4055884</span><span class="sxs-lookup"><span data-stu-id="f8b2d-108">If you are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="f8b2d-109">ตั้งค่าคอนฟิก add-in ของไคลเอนต์ Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="f8b2d-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="f8b2d-110">ในการเปิดใช้งานการรวมกับ Microsoft Project Client จะต้องติดตั้ง add-in ของ Microsoft Dynamics 365 ในแอพลิเคชัน Microsoft Project ของไคลเอนต์ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f8b2d-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="f8b2d-111">ซึ่งทำได้โดยการเปิด **พื้นที่ทำงานการจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="f8b2d-112">•   คลิก **ตั้งค่าคอนฟิกadd-in ไคลเอนต์ของโครงการ** จากส่วน **ลิงค์** > **การตั้งค่า** ของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f8b2d-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="f8b2d-113">•   คลิก **เปิด** แล้วคลิก **รัน** เมื่อได้รับการพร้อมท์</span><span class="sxs-lookup"><span data-stu-id="f8b2d-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="f8b2d-114">เปิดและแก้ไขโครงสร้างการแบ่งงานแบบร่างที่มีอยู่ใน Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="f8b2d-115">ถ้าโครงการใน Finance and Operations ได้สร้างโครงสร้างการแบ่งงานขึ้นแล้ว โครงสร้างการแบ่งงานสามารถถูกเปิดได้ในแอพลิเคชัน Microsoft Project Client ถ้าโครงสร้างการแบ่งงานอยู่ในสถานะร่าง</span><span class="sxs-lookup"><span data-stu-id="f8b2d-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="f8b2d-116">เมื่อต้องการเปิดจากหน้า **โครงการ** คลิกลิงค์ **เปิดใน Microsoft Project** จากแท็บ **แผน** หน้านี้ยังสามารถเปิดได้จากภายในแอพลิเคชัน Microsoft Project Client โดยการคลิก **เปิด** ในแท็บ **Microsoft Dynamics 365** เลือก **นิติบุคคล** และ **โครงการ** จากรายการ</span><span class="sxs-lookup"><span data-stu-id="f8b2d-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="f8b2d-117">ถ้าคุณกำลังใช้ Internet Explorer เป็นเบราเซอร์ของคุณ คุณจะต้องคลิก **บันทึก** เพื่อเปิดจากตำแหน่งที่มีการดาวน์โหลดแฟ้มด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="f8b2d-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="f8b2d-118">หรือ คลิก **บันทึก และเปิด** เพื่อเปิดไฟล์ใน Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="f8b2d-119">ห้ามเปลี่ยนชื่อแฟ้ม เมื่อบันทึก</span><span class="sxs-lookup"><span data-stu-id="f8b2d-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="f8b2d-120">ก่อนที่จะทำการแก้ไขใดๆ ไปยังไฟล์โดยใช้ Microsoft Project Client คุณจำเป็นต้องตรวจสอบ คลิก **ตรวจสอบ** ในแท็บ **Microsoft Dynamics 365** นี่จะป้องกันไม่ให้ผู้ใช้คนอื่นแก้ไขโครงสร้างการแบ่งจากภายใน Finance and Operations ได้ในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f8b2d-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="f8b2d-121">ในการเผยแพร่โครงสร้างการแบ่งงานหลังจากเสร็จสิ้นการแก้ไขใดๆ คลิก **เช็คอิน** ในแท็บ **Microsoft Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="f8b2d-122">ถ้ามีการเพิ่มทีมโครงการกับโครงการไปยัง Finance and Operations เรียบร้อยแล้ว รายการทรัพยากรจะถูกเติมด้วยสมาชิกทีมงาน</span><span class="sxs-lookup"><span data-stu-id="f8b2d-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="f8b2d-123">ถ้าทีมโครงการยังไม่ได้ถูกเพิ่มไปยังโครงการ คุณสามารถเลือกทรัพยากรและสร้างทีมงานภายใน Microsoft Project Client ได้โดยการคลิกที่ปุ่ม **ทรัพยากร** บนแท็บ **Microsoft Dynamics 365** ได้</span><span class="sxs-lookup"><span data-stu-id="f8b2d-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="f8b2d-124">ข้อมูลต่อไปนี้จะถูกซิงค์กลับไปยัง Finance and Operations โดยเป็นส่วนหนึ่งของกระบวนการเช็คอิน:</span><span class="sxs-lookup"><span data-stu-id="f8b2d-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="f8b2d-125">•   ชื่องาน</span><span class="sxs-lookup"><span data-stu-id="f8b2d-125">•   Task name</span></span>

<span data-ttu-id="f8b2d-126">•   วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f8b2d-126">•   Start date</span></span>

<span data-ttu-id="f8b2d-127">•   วันที่เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="f8b2d-127">•   Finish date</span></span>

<span data-ttu-id="f8b2d-128">•   รายการก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="f8b2d-128">•   Predecessors</span></span>

<span data-ttu-id="f8b2d-129">•   ชื่อทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="f8b2d-129">•   Resource names</span></span>

<span data-ttu-id="f8b2d-130">•   ประเภท</span><span class="sxs-lookup"><span data-stu-id="f8b2d-130">•   Category</span></span>

<span data-ttu-id="f8b2d-131">•   ประเภททรัพยากร</span><span class="sxs-lookup"><span data-stu-id="f8b2d-131">•   Resource category</span></span>

<span data-ttu-id="f8b2d-132">•   ชั่วโมงทำงาน</span><span class="sxs-lookup"><span data-stu-id="f8b2d-132">•   Work hours</span></span>

<span data-ttu-id="f8b2d-133">•   บันทึก</span><span class="sxs-lookup"><span data-stu-id="f8b2d-133">•   Notes</span></span>

<span data-ttu-id="f8b2d-134">•   ระดับความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="f8b2d-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="f8b2d-135">ถ้าคุณเพิ่มคอลัมน์อื่นใดๆ ไปยังแฟ้ม Microsoft Project Client ของคุณ รายการเหล่านั้นจะไม่ถูกบันทึกในไฟล์ และจะไม่ถูกแสดงเมื่อมีการเปิดไฟล์อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="f8b2d-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="f8b2d-136">สร้างโครงสร้างการแบ่งงานสำหรับโครงการที่มีอยู่โดยใช้ Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="f8b2d-137">ในการสร้างโครงสร้างการแบ่งงานใหม่โดยใช้ Microsoft Project Client ให้ดำเนินการตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f8b2d-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="f8b2d-138">เปิด Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f8b2d-139">ในแท็บ **Microsoft Dynamics 365** คลิก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="f8b2d-140">เลือก **นิติบุคคล** สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="f8b2d-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="f8b2d-141">เลือก **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="f8b2d-142">คลิก **ตรวจสอบ** บนแท็บ **Microsoft Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="f8b2d-143">เมื่อพร้อมที่จะเผยแพร่ไปยัง Finance and Operations คลิก **เช็คอิน** บนแท็บ **Microsoft Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="f8b2d-144">แทนที่โครงสร้างการแบ่งงานที่มีอยู่สำหรับโครงการที่มีอยู่โดยใช้ Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="f8b2d-145">ในการสร้างโครงสร้างการแบ่งงานใหม่โดยใช้ Microsoft Project Client และแทนที่โครงสร้างการแบ่งงานที่มีอยู่สำหรับโครงการที่มีอยู่ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f8b2d-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="f8b2d-146">เปิด Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f8b2d-147">สร้างกำหนดการใน Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="f8b2d-148">บนแท็บ **Microsoft Dynamics 365** คลิก **บันทึกการเปลี่ยนแปลง** > **แทนที่โครงการที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="f8b2d-149">เลือก **นิติบุคคล** สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="f8b2d-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="f8b2d-150">เลือก **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="f8b2d-151">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="f8b2d-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="f8b2d-152">สร้างโครงการใหม่จากภายใน Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="f8b2d-153">เปิด Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f8b2d-154">สร้างกำหนดการใน Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f8b2d-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="f8b2d-155">บนแท็บ **Microsoft Dynamics 365** คลิก **บันทึกการเปลี่ยนแปลง** > **บันทึกไปยังโครงการใหม่**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="f8b2d-156">เลือก **นิติบุคคล** สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="f8b2d-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="f8b2d-157">ป้อน **รหัสโครงการ** ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="f8b2d-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="f8b2d-158">ป้อน **ชื่อโครงการ**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="f8b2d-159">เลือก **ชนิดโครงการ** **กลุ่มโครงการ** และ **รหัสสัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="f8b2d-160">อีกทางหนึ่งคือ คุณสามารถสร้างสัญญาโครงการใหม่ได้ โดยการคลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f8b2d-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="f8b2d-161">เลือก **ปฏิทิน** ที่จะใช้สำหรับการจัดหาทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="f8b2d-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="f8b2d-162">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="f8b2d-162">Click **OK**.</span></span>

