---
title: สร้างเท็มเพลตกระบวนการใน Attract
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการสร้างเท็มเพลตกระบวนการใน Attract
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 2b9cac68093be65584192757229c20b1a1546342
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2019
ms.locfileid: "306419"
---
# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="d6747-103">สร้างเท็มเพลตกระบวนการใน Attract</span><span class="sxs-lookup"><span data-stu-id="d6747-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6747-104">*เท็มเพลตกระบวนการว่าจ้าง* ประกอบด้วยกิจกรรมทั้งหมดที่ควรจะรวมเป็นส่วนหนึ่งของกระบวนการว่าจ้างสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="d6747-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="d6747-105">หัวข้อนี้อธิบายองค์ประกอบของเท็มเพลตกระบวนการใน Microsoft Dynamics 365 for Talent: Attract</span><span class="sxs-lookup"><span data-stu-id="d6747-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="d6747-106">และยังอธิบายถึงวิธีการสร้างเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="d6747-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="d6747-107">การสร้างเท็มเพลเป็นส่วนหนึ่งของ Add-On การจ้างงานแบบครอบคลุมสำหรับ Attract</span><span class="sxs-lookup"><span data-stu-id="d6747-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="d6747-108">การจัดการเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="d6747-108">Template management</span></span>

<span data-ttu-id="d6747-109">องค์กรสามารถตัดสินใจได้ว่า สมาชิกทีมงานหรือผู้ดูแลระบบเท่านั้นที่สามารถสร้างเท็มเพลตกระบวนการใน Attract ได้</span><span class="sxs-lookup"><span data-stu-id="d6747-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="d6747-110">เมื่อต้องการตั้งค่าคอนฟิกการจัดการเท็มเพลต ไปที่ **ศูนย์การจัดการ** \> **การจัดการเท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="d6747-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="d6747-111">เมื่อต้องการให้สมาชิกในทีมสร้างเท็มเพลตของตนเอง เปิดการจัดการเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="d6747-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="d6747-112">ถ้าคุณไม่เปิดใช้งานการจัดการเท็มเพลต เฉพาะผู้ดูแลระบบเท่านั้นจะสามารถสร้างเท็มเพลตได้</span><span class="sxs-lookup"><span data-stu-id="d6747-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="d6747-113">เท็มเพลตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d6747-113">Default template</span></span>

<span data-ttu-id="d6747-114">เฉพาะผู้ดูแลระบบเท่านั้นที่สามารถตั้งค่าเท็มเพลตเริ่มต้นได้</span><span class="sxs-lookup"><span data-stu-id="d6747-114">Only admins can set the default template.</span></span> <span data-ttu-id="d6747-115">มีการใช้เท็มเพลตเริ่มต้น ถ้าไม่ได้เลือกเท็มเพลต เมื่อมีการสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="d6747-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="d6747-116">เมื่อต้องการตั้งค่าเท็มเพลตเริ่มต้น ไปที่ **ศูนย์การจัดการ** \> **การจัดการเท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="d6747-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="d6747-117">บนบัตรสำหรับเท็มเพลตที่ควรเป็นเท็มเพลตเริ่มต้น เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **ตั้งเป็นค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="d6747-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="d6747-118">สร้างเท็มเพลตกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="d6747-118">Create a process template</span></span>

<span data-ttu-id="d6747-119">ผู้ดูแลระบบ ผู้สรรหา และผู้จัดการว่าจ้าง สามารถสร้างเท็มเพลตกระบวนการได้</span><span class="sxs-lookup"><span data-stu-id="d6747-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="d6747-120">เท็มเพลตการกระบวนการประกอบด้วย *ขั้น* และ *กิจกรรม*</span><span class="sxs-lookup"><span data-stu-id="d6747-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="d6747-121">ขั้นจัดกลุ่มกิจกรรมหนึ่งหรือหลายกิจกรรมเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="d6747-121">Stages group together one or more activities.</span></span> <span data-ttu-id="d6747-122">โดยค่าเริ่มต้น เท็มเพลตกระบวนการทั้งหมดมีกิจกรรมผู้ที่มีแนวโน้มจะเป็นลูกค้า แอพลิเคชัน และข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="d6747-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="d6747-123">ขั้นที่ประกอบด้วยกิจกรรมเหล่านี้สามารถเปลี่ยนชื่อได้</span><span class="sxs-lookup"><span data-stu-id="d6747-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="d6747-124">คุณสามารถเพิ่มขั้นตอนเพิ่มเติมได้ โดยการเลือก **+ ขั้นใหม่**ได้</span><span class="sxs-lookup"><span data-stu-id="d6747-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="d6747-125">คุณสามารถเพิ่มกิจกรรมไปยังขั้นตอน โดยการลากไปยังขั้นที่เหมาะสม หรือโดยการคลิกสองครั้งในรายการกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="d6747-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="d6747-126">ชื่อขั้นสามารถมองเห็นได้โดยผู้สมัครในหน้า **สถานะใบสมัคร**</span><span class="sxs-lookup"><span data-stu-id="d6747-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="d6747-127">คุณควรพิจารณาข้อเท็จจริงนี้ เมื่อคุณเลือกชื่อสำหรับขั้น</span><span class="sxs-lookup"><span data-stu-id="d6747-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="d6747-128">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับกิจกรรม ดู [กิจกรรมกระบวนการว่าจ้างใน Attract](./activities-attract.md)</span><span class="sxs-lookup"><span data-stu-id="d6747-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="d6747-129">ทำตามขั้นตอนเหล่านี้ เมื่อต้องการสร้างเท็มเพลตกระบวนการว่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="d6747-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="d6747-130">ไปที่ **เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="d6747-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="d6747-131">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="d6747-131">Select **New**.</span></span>
3. <span data-ttu-id="d6747-132">ในฟิลด์ **ชื่อเท็มเพลต** ป้อนชื่อสำหรับเท็มเพลต และจากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d6747-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="d6747-133">ในรายการ **เลือกกระบวนการอนุมัติ** เลือก **เริ่มต้น** เพื่อขอการอนุมัติสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="d6747-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="d6747-134">เลือกเพื่อเปิดใช้งาน หรือปิดใช้งานผู้ที่มีแนวโน้มจะเป็นลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d6747-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="d6747-135">ไม่จำเป็นต้องระบุ: เพิ่ม หรือลบขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="d6747-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="d6747-136">ในการเพิ่มขั้น เลือก **+ ขั้นใหม่**</span><span class="sxs-lookup"><span data-stu-id="d6747-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="d6747-137">ในการลบขั้น โฮเวอร์ตัวชี้เหนือขั้น แล้วเลือกปุ่มถังขยะที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="d6747-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d6747-138">ไม่สามารถลบขั้นผู้ที่มีแนวโน้มจะเป็นลูกค้า ใบสมัคร และข้อเสนอได้ แต่สามารถตั้งชื่อใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="d6747-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="d6747-139">ไม่จำเป็นต้องระบุ: เพิ่ม หรือลบกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="d6747-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="d6747-140">ในการเพิ่มกิจกรรม ลากจากรายชื่อกิจกรรมทางขวาไปยังขั้นที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="d6747-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="d6747-141">อีกทางหนึ่งคือ ดับเบิลคลิกที่กิจกรรม และจากนั้น เลือกระยะที่จะเพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="d6747-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="d6747-142">ในการลบกิจกรรม ขยาย และจากนั้นเลือกปุ่มถังขยะบนหัวข้อกิจกรรมนั้น</span><span class="sxs-lookup"><span data-stu-id="d6747-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="d6747-143">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d6747-143">Select **Save**.</span></span>
