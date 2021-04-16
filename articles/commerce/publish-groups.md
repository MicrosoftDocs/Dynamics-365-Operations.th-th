---
title: ทำงานกับกลุ่มการเผยแพร่
description: หัวข้อนี้อธิบายคุณลักษณะของกลุ่มการเผยแพร่ใน Microsoft Dynamics 365 Commerce
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 15ac04721e440dcd7c0f8984c14e86aa0f68963e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792326"
---
# <a name="work-with-publish-groups"></a><span data-ttu-id="2c223-103">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-103">Work with publish groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2c223-104">หัวข้อนี้อธิบายคุณลักษณะของกลุ่มการเผยแพร่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2c223-104">This topic describes the publish groups feature in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2c223-105">เว็บไซต์อีคอมเมิร์ซมีการปรับปรุงอย่างต่อเนื่องด้วยเนื้อหาใหม่ตลอดทั้งปี</span><span class="sxs-lookup"><span data-stu-id="2c223-105">E-commerce websites are constantly updated with new content throughout the year.</span></span> <span data-ttu-id="2c223-106">การปรับปรุงมักจะถูกเผยแพร่ในชุดงานรอบเหตุการณ์อีคอมเมิร์ซที่ไม่ว่าง เช่น วันหยุด การส่งเสริมการขายตามฤดูกาล หรือการเปิดตัวโปรโมชัน</span><span class="sxs-lookup"><span data-stu-id="2c223-106">Updates are often published in batches around busy e-commerce events such as holidays, seasonal marketing campaigns, or promotional launches.</span></span> <span data-ttu-id="2c223-107">การปรับปรุงเหล่านี้มักจะต้องใช้กลุ่มของเนื้อหาเว็บไซต์ (ตัวอย่างเช่น หน้า รูปภาพ ชิ้นส่วน และเท็มเพลต) จะถูกจัดฉาก ตรวจสอบ และเผยแพร่ พร้อมกันในการดำเนินการเดียว</span><span class="sxs-lookup"><span data-stu-id="2c223-107">These updates often require that groups of website content (for examples, pages, images, fragments, and templates) be staged, validated, and published concurrently in a single action.</span></span>

<span data-ttu-id="2c223-108">ความสามารถในการจัดกลุ่มสินค้าลงในชุดเชิงตรรกะที่เผยแพร่สินค้าด้วยกัน ที่ซึ่งแต่ละชุดจะมีวงจรชีวิตของตัวเอง มีข้อดีมากมายให้กับผู้สร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="2c223-108">The ability to group items into logical sets that publish items together, where each set has its own lifecycle, provides many advantages to site authors.</span></span> <span data-ttu-id="2c223-109">ใน Commerce ชุดเชิงตรรกะเหล่านี้เรียกว่า กลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-109">In Commerce, these logical sets are known as publish groups.</span></span> <span data-ttu-id="2c223-110">ซึ่งยอมให้ผู้เขียนไซต์สามารถติดตามชุดของการปรับปรุงเป็นเอนทิตีของตัวเองที่สามารถตั้งค่าคอนฟิกได้ สามารถทดสอบได้ และสามารถเผยแพร่ได้</span><span class="sxs-lookup"><span data-stu-id="2c223-110">They let site authors track sets of updates as their own configurable, testable, and publishable entities.</span></span>

<span data-ttu-id="2c223-111">ผู้สร้างสามารถแสดงตัวอย่างการปรับปรุงในกลุ่มการเผยแพร่ที่จัดฉากได้โดยไม่ส่งผลกระทบต่อไซต์สดหรือกลุ่มการเผยแพร่ที่มีความสมบูรณ์ในตัวเองอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2c223-111">Authors can preview updates in a staged publish group without affecting the live site or other self-contained publish groups.</span></span> <span data-ttu-id="2c223-112">จากนั้น ผู้สร้างสามารถจัดกำหนดการดำเนินการเผยแพร่เพื่อเผยแพร่สินค้าทั้งหมดในกลุ่มการเผยแพร่ไปยังไซต์ที่ถ่ายทอดสดพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="2c223-112">Authors can then schedule the publish action to simultaneously publish all the items in the publish group to the live site.</span></span> <span data-ttu-id="2c223-113">ความสามารถในการจัดกลุ่ม แสดงตัวอย่าง และจัดกำหนดการปรับปรุงสำหรับการเผยแพร่ เป็นสิ่งสำคัญสำหรับบริษัทระดับองค์กรจำนวนมากที่สร้างรายได้ประจำปีอย่างมากในการปรับปรุงเหตุการณ์สำคัญพื้นฐานของไซต์</span><span class="sxs-lookup"><span data-stu-id="2c223-113">The ability to group, preview, and schedule updates for publishing is important for many enterprise-level companies that generate considerable annual revenue around event-based site update milestones.</span></span>

<span data-ttu-id="2c223-114">บริษัทสามารถก่อให้เกิดค่าใช้จ่ายจากการเปิดตัวที่ช้าหรือเนื้อหาที่ไม่ได้รับการตรวจสอบที่ไม่เป็นไปอย่างราบรื่น</span><span class="sxs-lookup"><span data-stu-id="2c223-114">Companies can incur costs from slow or invalidated content rollouts that don't go smoothly.</span></span> <span data-ttu-id="2c223-115">กลุ่มการเผยแพร่ช่วยรับประกันว่าการเปิดตัวจะถูกจัดระเบียบ ตรวจสอบ และเผยแพร่ตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="2c223-115">Publish groups help guarantee that launches are organized, validated, and published on time.</span></span> <span data-ttu-id="2c223-116">ไม่ว่าจะมีขนาดใหญ่หรือเล็ก กลุ่มการเผยแพร่ให้ชุดเครื่องมือที่มีคุณค่าที่ช่วยให้ผู้สร้างสามารถจัดระเบียบและทำให้งานการปรับปรุงไซต์อย่างต่อเนื่องเป็นไปได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="2c223-116">Whether they are large or small, publish groups provide a valuable toolset that helps authors organize and simplify ongoing site update tasks.</span></span>

## <a name="when-to-use-publish-groups"></a><span data-ttu-id="2c223-117">เมื่อใดที่ควรใช้กลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-117">When to use publish groups</span></span>

<span data-ttu-id="2c223-118">คุณสามารถใช้กลุ่มการเผยแพร่เมื่อใดก็ตามที่คุณต้องจัดลำดับและเผยแพร่เอกสารหลายฉบับเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="2c223-118">You can use publish groups whenever you must stage and publish multiple documents together.</span></span> <span data-ttu-id="2c223-119">ตัวอย่างเช่น หากเว็บไซต์ของคุณปรับปรุงเนื้อหาทุกฤดูกาล คุณสามารถสร้างกลุ่มการเผยแพร่สำหรับการเคลื่อนไหวทางการตลาดตามฤดูกาลเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="2c223-119">For example, if your website updates content every season, you can create publish groups for these seasonal marketing motions.</span></span> <span data-ttu-id="2c223-120">กลุ่มการเผยแพร่ "การปรับปรุงตามฤดูกาลในฤดูใบไม้ร่วง" ของคุณ อาจประกอบด้วยภาพตามฤดูกาลใหม่ ชิ้นส่วนที่มีข้อความการตลาดตามฤดูกาล หน้าที่รวมคอลเลกชันผลิตภัณฑ์ตามฤดูกาล หรือการปรับปรุงเว็บไซต์ตามฤดูกาลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2c223-120">Your "Autumn Seasonal Update" publish group might contain new seasonal images, fragments that have seasonal marketing messages, pages that include seasonal product collections, or other seasonal website updates.</span></span>

<span data-ttu-id="2c223-121">ข้อได้เปรียบของกลุ่มการเผยแพร่คือ คุณสามารถจัดลำดับการปรับปรุงหลายรายการควบคู่กันได้</span><span class="sxs-lookup"><span data-stu-id="2c223-121">An advantage of publish groups is that you can stage multiple updates in parallel.</span></span> <span data-ttu-id="2c223-122">ตัวอย่างเช่น ในไม่ช้าหลังจากการปรับปรุงสำหรับกลุ่มการเผยแพร่ "การปรับปรุงตามฤดูกาลในฤดูใบไม้ร่วง" อาจมีการปรับปรุงเนื้อหาสำหรับวันหยุดสุดสัปดาห์ที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="2c223-122">For example, soon after the update for the "Autumn Seasonal Update" publish group, there might be a content update for a specific holiday weekend.</span></span> <span data-ttu-id="2c223-123">ในกรณีนี้ คุณสามารถจัดลำดับเนื้อหาสำหรับกลุ่มการเผยแพร่ "การปรับปรุงตามฤดูกาลในฤดูใบไม้ร่วง" ในเวลาเดียวกันกับที่คุณจัดลำดับเนื้อหาสำหรับกลุ่มการเผยแพร่ "การปรับปรุงในวันหยุดของฤดูใบไม้ร่วง" ในเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="2c223-123">In this case, you can stage content for the "Autumn Seasonal Update" publish group at the same time that you stage content for a subsequent "Autumn Holiday Update" publish group.</span></span> <span data-ttu-id="2c223-124">กลุ่มการเผยแพร่แต่ละกลุ่มมีชุดที่ไม่ซ้ำกันของหน้า รูปภาพ ชิ้นส่วน เท็มเพลต และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2c223-124">Each publish group contains its own unique set of pages, images, fragments, templates, and so on.</span></span> <span data-ttu-id="2c223-125">คุณสามารถจัดลำดับ แสดงตัวอย่าง และตรวจสอบความถูกต้องของกลุ่มการเผยแพร่สองกลุ่มนี้ได้โดยอิสระ แต่บนเส้นเวลาที่เกิดขึ้นพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="2c223-125">You can stage, preview, and validate these two publish groups independently but on a concurrent timeline.</span></span> <span data-ttu-id="2c223-126">กลุ่มการเผยแพร่แต่ละกลุ่มสามารถถูกจัดตารางเวลาให้มีการถ่ายทอดสดบนไซต์ของคุณในวันที่และเวลาที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="2c223-126">Each publish group can then be scheduled to go live on your site at specific dates and times.</span></span>

## <a name="turn-on-the-publish-groups-feature"></a><span data-ttu-id="2c223-127">เปิดคุณลักษณะกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-127">Turn on the publish groups feature</span></span>

<span data-ttu-id="2c223-128">คุณลักษณะกลุ่มการเผยแพร่เป็นตัวเลือก และต้องถูกเปิดสำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2c223-128">The publish groups feature is optional and must be turned for your site.</span></span>

<span data-ttu-id="2c223-129">เมื่อต้องการเปิดคุณลักษณะกลุ่มการเผยแพร่สำหรับไซต์ของคุณในเครื่องมือการสร้าง Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2c223-129">To turn on the publish groups feature for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="2c223-130">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าไซต์** เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="2c223-130">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="2c223-131">ภายใต้ **การตั้งค่าไซต์** ให้เลือก **คุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="2c223-131">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="2c223-132">ตั้งค่าตัวเลือก **กลุ่มการเผยแพร่** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="2c223-132">Set the **Publish groups** option to **On**.</span></span>

## <a name="create-a-publish-group"></a><span data-ttu-id="2c223-133">สร้างกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-133">Create a publish group</span></span>

<span data-ttu-id="2c223-134">เมื่อต้องการสร้างกลุ่มการเผยแพร่สำหรับไซต์ของคุณในเครื่องมือการสร้าง Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2c223-134">To create a publish group for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="2c223-135">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **กลุ่มการเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="2c223-135">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="2c223-136">ในแถบคำสั่งด้านบน ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="2c223-136">In the top command bar, select **New**.</span></span>
1. <span data-ttu-id="2c223-137">ในกล่องโต้ตอบ **สร้างกลุ่มการเผยแพร่** ภายใต้ **ชื่อกลุ่มการเผยแพร่** ให้ป้อนชื่อที่เป็นคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2c223-137">In the **Create Publish Group** dialog box, under **Publish Group Name**, enter a descriptive name.</span></span> <span data-ttu-id="2c223-138">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2c223-138">Then select **OK**.</span></span>

## <a name="set-the-publish-group-authoring-context"></a><span data-ttu-id="2c223-139">ตั้งค่าบริบทการสร้างกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-139">Set the publish group authoring context</span></span>

<span data-ttu-id="2c223-140">ใน Commerce บริบทการสร้างเริ่มต้นคือ บริบทของไซต์ที่ถ่ายทอดสด</span><span class="sxs-lookup"><span data-stu-id="2c223-140">In Commerce, the default authoring context is the live site context.</span></span> <span data-ttu-id="2c223-141">บริบทการสร้างไซต์ที่ถ่ายทอดสดเป็นมุมมองเริ่มต้นที่คุณสามารถดูและทำการเปลี่ยนแปลงโดยตรงไปยังเว็บไซต์ของคุณโดยไม่ต้องใช้กลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-141">The live site authoring context is the default view where you can view and make changes directly to your website without using a publish group.</span></span> <span data-ttu-id="2c223-142">ซึ่งแสดงการปรับปรุงโดยตรงล่าสุดไปยังรุ่นที่มีการเผยแพร่ของไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2c223-142">It represents the latest direct updates to the published version of your site.</span></span> <span data-ttu-id="2c223-143">ถ้าตัวควบคุมบริบทภายใต้ **กลุ่มการเผยแพร่** ในบานหน้าต่างนำทางด้านซ้าย จะแสดงชื่อว่า **ไซต์ที่ถ่ายทอดสด** คุณกำลังทำงานอยู่ในบริบทการสร้างไซต์ที่ถ่ายทอดสด</span><span class="sxs-lookup"><span data-stu-id="2c223-143">If the context control under **Publish Groups** in the left navigation pane shows the name **Live site**, you're working in the live site authoring context.</span></span> <span data-ttu-id="2c223-144">**ไซต์ที่ถ่ายทอดสด** เป็นชื่อเริ่มต้นของการควบคุมบริบท</span><span class="sxs-lookup"><span data-stu-id="2c223-144">**Live site** is the default name of the context control.</span></span> <span data-ttu-id="2c223-145">มิฉะนั้น การควบคุมบริบทจะแสดงชื่อของกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-145">Otherwise, the context control shows the name of a publish group.</span></span>

<span data-ttu-id="2c223-146">เพื่อทำงานในกลุ่มการเผยแพร่ คุณต้องสลับไปยังกลุ่มการเผยแพร่ที่สร้างบริบทให้</span><span class="sxs-lookup"><span data-stu-id="2c223-146">To work in a publish group, you must switch to the publish group authoring context for it.</span></span> <span data-ttu-id="2c223-147">หากต้องการตั้งค่าบริบทของกลุ่มการเผยแพร่ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2c223-147">To set the publish group context, follow one of these steps.</span></span>

- <span data-ttu-id="2c223-148">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือกตัวควบคุมบริบทภายใต้ **กลุ่มการเผยแพร่** โดยตรง และจากนั้น เลือกชื่อของกลุ่มการเผยแพร่ในรายการของตัวเลือกที่ปรากฏ</span><span class="sxs-lookup"><span data-stu-id="2c223-148">In the left navigation pane, select the context control directly under **Publish Groups**, and then select the name of the publish group in the list of options that appears.</span></span> <span data-ttu-id="2c223-149">การควบคุมบริบทจะถูกตั้งชื่อใหม่ และแสดงชื่อของกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-149">The context control is renamed and shows the name of the publish group.</span></span>
- <span data-ttu-id="2c223-150">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **กลุ่มการเผยแพร่** และจากนั้น ภายใต้ **กลุ่มการเผยแพร่** ให้เลือกชื่อของกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-150">In the left navigation pane, select **Publish Groups**, and then, under **Publish Groups**, select the name of the publish group.</span></span> <span data-ttu-id="2c223-151">การควบคุมบริบทจะถูกตั้งชื่อใหม่ และแสดงชื่อของกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-151">The context control is renamed and shows the name of the publish group.</span></span>

<span data-ttu-id="2c223-152">หลังจากที่คุณตั้งค่าบริบทการสร้างของกลุ่มการเผยแพร่ คุณกำลังทำงานอยู่ในบริบทของกลุ่มการเผยแพร่เมื่อคุณดูตัวอย่างและแก้ไขเนื้อหาของไซต์</span><span class="sxs-lookup"><span data-stu-id="2c223-152">After you set your publish group authoring context, you're working in that publish group context when you preview and edit site content.</span></span>

<span data-ttu-id="2c223-153">หากต้องการกลับไปยังบริบทการสร้างไซต์ที่ถ่ายทอดสดเริ่มต้น ให้เลือกตัวควบคุมบริบท และจากนั้น เลือก **ไซต์ที่ถ่ายทอดสด**</span><span class="sxs-lookup"><span data-stu-id="2c223-153">To return to the default live site authoring context, select the context control, and then select **Live site**.</span></span>

## <a name="add-pages-or-other-items-to-a-publish-group"></a><span data-ttu-id="2c223-154">เพิ่มหน้าหรือรายการอื่นๆ ลงในกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-154">Add pages or other items to a publish group</span></span>

<span data-ttu-id="2c223-155">หลังจากที่คุณได้เลือกบริบทการสร้างของกลุ่มการเผยแพร่แล้ว และตัวควบคุมบริบทในบานหน้าต่างนำทางด้านซ้ายแสดงชื่อ คุณสามารถสร้างเนื้อหาได้เช่นเดียวกับที่คุณทำในบริบทของไซต์ที่ถ่ายทอดสดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2c223-155">After you've selected a publish group authoring context, and the context control in the left navigation pane shows its name, you can create content just as you do in the default live site context.</span></span> <span data-ttu-id="2c223-156">นอกจากนี้ คุณยังสามารถเพิ่มเพจที่มีอยู่หรือสินค้าอื่นๆ ได้จากกลุ่มการเผยแพร่อื่นๆ หรือจากบริบทของไซต์ที่ถ่ายทอดสดได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="2c223-156">You can also add existing pages or other items from other publish groups, or from the live site context.</span></span>

<span data-ttu-id="2c223-157">หากต้องการคัดลอกเพจที่มีอยู่ไปยังกลุ่มการเผยแพร่ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2c223-157">To copy existing pages to a publish group, follow these steps.</span></span>

1. <span data-ttu-id="2c223-158">เลือกบริบทการสร้างเพื่อคัดลอก และจากนั้น ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **เพจ**</span><span class="sxs-lookup"><span data-stu-id="2c223-158">Select the authoring context to copy from, and then, in the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="2c223-159">เลือกเพจที่จะเพิ่มลงในกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-159">Select the page to add to a publish group.</span></span>
1. <span data-ttu-id="2c223-160">ในแถบคำสั่ง ให้เลือก **คัดลอกไปยังกลุ่มการเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="2c223-160">In the command bar, select **Copy to Publish group**.</span></span>
1. <span data-ttu-id="2c223-161">ในกล่องโต้ตอบ **เลือกกลุ่มการเผยแพร่** เลือกกลุ่มการเผยแพร่เพื่อเพิ่มหน้า และจากนั้น ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2c223-161">In the **Select a Publish Group** dialog box, select the publish group to add the page to, and then select **OK**.</span></span>

<span data-ttu-id="2c223-162">คุณสามารถใช้ขั้นตอนพื้นฐานเดียวกันในการสร้างหน้าผลิตภัณฑ์ที่กำหนดเอง URL เท็มเพลต เค้าโครง ชิ้นส่วน และสินทรัพย์ไลบรารีสื่อ หรือเพื่อเพิ่มสินค้าที่มีอยู่ของประเภทเหล่านี้ไปยังกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-162">You can use the same basic steps to create customized product pages, URLs, templates, layouts, fragments, and media library assets, or to add existing items of these types to a publish group.</span></span>

## <a name="validate-a-publish-group"></a><span data-ttu-id="2c223-163">ตรวจสอบกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-163">Validate a publish group</span></span>

<span data-ttu-id="2c223-164">เพื่อให้แน่ใจว่าคุณพึงพอใจกับการขึ้นต่อกันทั้งหมดในเนื้อหากลุ่มการเผยแพร่ และการตรวจสอบความถูกต้องผ่านทั้งหมด คุณสามารถเรียกใช้การตรวจสอบเพื่อระบุปัญหาใดๆ ที่ต้องได้รับการแก้ไข ก่อนที่คุณจะจัดกำหนดการการดำเนินการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-164">To make sure that all dependencies in publish group content are satisfied, and that all validations are passed, you can run validation to identify any issues that must be addressed before you schedule a publish action.</span></span>

<span data-ttu-id="2c223-165">หากต้องการตรวจสอบความถูกต้องของกลุ่มการเผยแพร่ของคุณ ก่อนที่คุณจะจัดกำหนดการ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2c223-165">To validate your publish group before you schedule it, follow these steps.</span></span>

1. <span data-ttu-id="2c223-166">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **กลุ่มการเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="2c223-166">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="2c223-167">เลือกกลุ่มการเผยแพร่ที่จะตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="2c223-167">Select the publish group to validate.</span></span>
1. <span data-ttu-id="2c223-168">ในแถบคำสั่ง ให้เลือก **ตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="2c223-168">In the command bar, select **Validate**.</span></span>

<span data-ttu-id="2c223-169">การตรวจสอบความถูกต้องถูกเรียกใช้บนเนื้อหาทั้งหมดในกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-169">Validation is run on all content in the publish group.</span></span> <span data-ttu-id="2c223-170">ปัญหาใดๆ ที่จะป้องกันการดำเนินการประกาศที่ประสบความสำเร็จจะแสดงในช่องการแจ้งเตือนที่ปรากฏที่ด้านขวาบน</span><span class="sxs-lookup"><span data-stu-id="2c223-170">Any issues that will prevent a successful publish action are shown in a notification box that appears in the upper right.</span></span>

> [!NOTE]
> <span data-ttu-id="2c223-171">การตรวจสอบจะรันโดยอัตโนมัติเสมอ เมื่อมีการจัดกำหนดการกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-171">Validation is always run automatically when a publish group is scheduled.</span></span> <span data-ttu-id="2c223-172">อย่างไรก็ตาม ปุ่ม **ตรวจสอบ** ในแถบคำสั่งมีประโยชน์เนื่องจากจะช่วยระบุปัญหาที่คุณต้องแก้ไข ก่อนที่คุณจะพยายามจัดกำหนดการกลุ่มการเผยแพร่ที่จะถ่ายทอดสด</span><span class="sxs-lookup"><span data-stu-id="2c223-172">However, the **Validate** button in the command bar is useful because it helps identify issues that you must fix before you try to schedule a publish group to go live.</span></span>

## <a name="schedule-a-publish-group-to-go-live"></a><span data-ttu-id="2c223-173">จัดกำหนดการกลุ่มการเผยแพร่ที่จะถ่ายทอดสด</span><span class="sxs-lookup"><span data-stu-id="2c223-173">Schedule a publish group to go live</span></span>

<span data-ttu-id="2c223-174">หากต้องการจัดกำหนดการกลุ่มการเผยแพร่ให้ถ่ายทอดสดบนไซต์ของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2c223-174">To schedule a publish group to go live on your site, follow these steps.</span></span>

1. <span data-ttu-id="2c223-175">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **กลุ่มการเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="2c223-175">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="2c223-176">ภายใต้ **กลุ่มการเผยแพร่** ให้เลือกกลุ่มการเผยแพร่ที่จะจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="2c223-176">Under **Publish Groups**, select the publish group to schedule.</span></span>
1. <span data-ttu-id="2c223-177">ในแถบคำสั่ง ให้เลือก **แก้ไขกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="2c223-177">In the command bar, select **Edit Schedule**.</span></span> <span data-ttu-id="2c223-178">กล่องโต้ตอบ **แก้ไขกำหนดการ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="2c223-178">The **Edit Schedule** dialog box appears.</span></span>
1. <span data-ttu-id="2c223-179">เลือกวันที่และเวลาที่กลุ่มการเผยแพร่ของคุณควรจะถ่ายทอดสด และจากนั้น ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2c223-179">Select the date and time when your publish group should go live, and then select **OK**.</span></span>

<span data-ttu-id="2c223-180">หากต้องการยกเลิกการจัดกำหนดการกลุ่มการเผยแพร่ ให้ทำตามขั้นตอนที่เหมือนกัน แต่เลือก **ยกเลิกการจัดกำหนดการกลุ่มการเผยแพร่** ในกล่องโต้ตอบ **แก้ไขกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="2c223-180">To unschedule a publish group, follow the same steps, but select **Unschedule publish group** in the **Edit Schedule** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="2c223-181">กลุ่มการเผยแพร่ที่มีขนาดใหญ่มากอาจใช้เวลาถึงหนึ่งนาทีหรือสองนาทีในการเผยแพร่ เมื่อเวลาในการจัดกำหนดการมาถึง</span><span class="sxs-lookup"><span data-stu-id="2c223-181">Very large publish groups might take up to a minute or two to be published when their scheduled time arrives.</span></span> <span data-ttu-id="2c223-182">โปรดทราบว่าการดำเนินการเผยแพร่ไม่ใช่แบบทันที และกลุ่มการเผยแพร่ที่มีขนาดเล็กกว่าจะได้รับการเผยแพร่ที่เร็วกว่า</span><span class="sxs-lookup"><span data-stu-id="2c223-182">Be aware that a publish action isn't instantaneous, and that smaller publish groups will be published faster.</span></span>

## <a name="publish-groups-faq"></a><span data-ttu-id="2c223-183">FAQ เกี่ยวกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-183">Publish groups FAQ</span></span>

<span data-ttu-id="2c223-184">**สินค้าสามารถอยู่ในกลุ่มการเผยแพร่ได้กี่รายการ**</span><span class="sxs-lookup"><span data-stu-id="2c223-184">**How many items can be in a publish group?**</span></span>

<span data-ttu-id="2c223-185">ขณะนี้มีขีดจำกัดของสินค้าเป็น 2,000 รายการต่อกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="2c223-185">Currently, there is a limit of 2,000 items per publish group.</span></span> <span data-ttu-id="2c223-186">โปรดทราบว่ากลุ่มการเผยแพร่ที่มีขนาดใหญ่มากอาจใช้เวลาหลายนาทีในการเผยแพร่ เมื่อเวลาในการจัดกำหนดการมาถึง</span><span class="sxs-lookup"><span data-stu-id="2c223-186">Be aware that very large publish groups might take several minutes to be published when their scheduled time arrives.</span></span>

<span data-ttu-id="2c223-187">**มีการเผยแพร่กลุ่ม เช่น รหัส "สาขา" ในคำศัพท์การพัฒนาซอฟต์แวร์หรือไม่**</span><span class="sxs-lookup"><span data-stu-id="2c223-187">**Are publish groups like code "branches" in software development terminology?**</span></span>

<span data-ttu-id="2c223-188">ใช่และไม่</span><span class="sxs-lookup"><span data-stu-id="2c223-188">Yes and no.</span></span> <span data-ttu-id="2c223-189">อาจพิจารณาได้ว่ากลุ่มการเผยแพร่เป็นรุ่นที่แยกออกมาของไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2c223-189">Publish groups can be thought of as forked versions of your site.</span></span> <span data-ttu-id="2c223-190">ด้วยวิธีนั้น รายการเหล่านั้นทำหน้าที่เหมือนสาขา</span><span class="sxs-lookup"><span data-stu-id="2c223-190">In that way, they do act like branches.</span></span> <span data-ttu-id="2c223-191">อย่างไรก็ตาม ไม่มีแนวคิดของการผสานในระดับของสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="2c223-191">However, there is no concept of a merge at the level of individual items.</span></span> <span data-ttu-id="2c223-192">สินค้าที่ถูกประกาศล่าสุดเพียงแค่เขียนทับสิ่งที่มีอยู่ก่อนหน้านี้ และการดำเนินการประกาศล่าสุดมักจะแทนที่การดำเนินการประกาศก่อนหน้านี้เสมอ</span><span class="sxs-lookup"><span data-stu-id="2c223-192">The item that is published last just overwrites what previously existed, and the most recent publish action always supersedes previous publish actions.</span></span>

<span data-ttu-id="2c223-193">**ฉันสามารถจัดกำหนดการกลุ่มการเผยแพร่สองกลุ่มที่จะถ่ายทอดสดในเวลาเดียวกันได้หรือไม่**</span><span class="sxs-lookup"><span data-stu-id="2c223-193">**Can I schedule two publish groups to go live at the same time?**</span></span>

<span data-ttu-id="2c223-194">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="2c223-194">No.</span></span> <span data-ttu-id="2c223-195">สำหรับเหตุผลด้านประสิทธิภาพและความขัดแย้ง ระบบจะบังคับให้คุณย้ายกลุ่มการเผยแพร่ที่มีการจัดกำหนดการไว้ให้ห่างกันอย่างน้อยห้านาที</span><span class="sxs-lookup"><span data-stu-id="2c223-195">For performance and conflict reasons, the system will force you to stagger scheduled publish groups at least five minutes apart.</span></span>

<span data-ttu-id="2c223-196">**ฉันสามารถใช้กลุ่มการเผยแพร่เพื่อจัดกำหนดการสินค้าฝ่ายสนับสนุนของช่องทาง Omni เช่น ส่วนลด และการปรับปรุงผลิตภัณฑ์ได้หรือไม่**</span><span class="sxs-lookup"><span data-stu-id="2c223-196">**Can I use publish groups to schedule omnichannel back-office items, such as discounts and product updates?**</span></span>

<span data-ttu-id="2c223-197">ขณะนี้คุณลักษณะกลุ่มการเผยแพร่สนับสนุนเฉพาะเนื้อหาของเว็บไซต์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2c223-197">Currently, the publish groups feature supports only website content.</span></span> <span data-ttu-id="2c223-198">อย่างไรก็ตาม Microsoft ตระหนักว่าการรวมกับสถานการณ์การจัดซื้อสินค้าของฝ่ายสนับสนุนอาจมีคุณค่าสำหรับการประสานงานและการทำงานอัตโนมัติของการเปิดตัวการส่งเสริมการขายของช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="2c223-198">However, Microsoft is aware that integration with back-office merchandising scenarios could be valuable for the coordination and automation of omnichannel campaign launches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c223-199">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2c223-199">Additional resources</span></span>

[<span data-ttu-id="2c223-200">วิธีการเพิ่มเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="2c223-200">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="2c223-201">อภิธานศัพท์ของรูปแบบหน้า</span><span class="sxs-lookup"><span data-stu-id="2c223-201">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="2c223-202">สถานะและระยะเวลาใช้งานของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="2c223-202">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="2c223-203">เปิดใช้งานและใช้การใช้ร่วมกันข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="2c223-203">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="2c223-204">ใช้งานโมดูล</span><span class="sxs-lookup"><span data-stu-id="2c223-204">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="2c223-205">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="2c223-205">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="2c223-206">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="2c223-206">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2c223-207">เลือกกำหนดการนำทางของไซต์</span><span class="sxs-lookup"><span data-stu-id="2c223-207">Customize site navigation</span></span>](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
