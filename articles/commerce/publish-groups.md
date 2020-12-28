---
title: ทำงานกับกลุ่มการเผยแพร่
description: หัวข้อนี้อธิบายคุณลักษณะของกลุ่มการเผยแพร่ใน Microsoft Dynamics 365 Commerce
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a83affb5b383b50317ddf53de4d3bf565f0d9439
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416238"
---
# <a name="work-with-publish-groups"></a><span data-ttu-id="5a0b8-103">ทำงานกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-103">Work with publish groups</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5a0b8-104">หัวข้อนี้อธิบายคุณลักษณะของกลุ่มการเผยแพร่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5a0b8-104">This topic describes the publish groups feature in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5a0b8-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="5a0b8-105">Overview</span></span>

<span data-ttu-id="5a0b8-106">เว็บไซต์อีคอมเมิร์ซมีการปรับปรุงอย่างต่อเนื่องด้วยเนื้อหาใหม่ตลอดทั้งปี</span><span class="sxs-lookup"><span data-stu-id="5a0b8-106">E-commerce websites are constantly updated with new content throughout the year.</span></span> <span data-ttu-id="5a0b8-107">การปรับปรุงมักจะถูกเผยแพร่ในชุดงานรอบเหตุการณ์อีคอมเมิร์ซที่ไม่ว่าง เช่น วันหยุด การส่งเสริมการขายตามฤดูกาล หรือการเปิดตัวโปรโมชัน</span><span class="sxs-lookup"><span data-stu-id="5a0b8-107">Updates are often published in batches around busy e-commerce events such as holidays, seasonal marketing campaigns, or promotional launches.</span></span> <span data-ttu-id="5a0b8-108">การปรับปรุงเหล่านี้มักจะต้องใช้กลุ่มของเนื้อหาเว็บไซต์ (ตัวอย่างเช่น หน้า รูปภาพ ชิ้นส่วน และเท็มเพลต) จะถูกจัดฉาก ตรวจสอบ และเผยแพร่ พร้อมกันในการดำเนินการเดียว</span><span class="sxs-lookup"><span data-stu-id="5a0b8-108">These updates often require that groups of website content (for examples, pages, images, fragments, and templates) be staged, validated, and published concurrently in a single action.</span></span>

<span data-ttu-id="5a0b8-109">ความสามารถในการจัดกลุ่มสินค้าลงในชุดเชิงตรรกะที่เผยแพร่สินค้าด้วยกัน ที่ซึ่งแต่ละชุดจะมีวงจรชีวิตของตัวเอง มีข้อดีมากมายให้กับผู้สร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="5a0b8-109">The ability to group items into logical sets that publish items together, where each set has its own lifecycle, provides many advantages to site authors.</span></span> <span data-ttu-id="5a0b8-110">ใน Commerce ชุดเชิงตรรกะเหล่านี้เรียกว่า กลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-110">In Commerce, these logical sets are known as publish groups.</span></span> <span data-ttu-id="5a0b8-111">ซึ่งยอมให้ผู้เขียนไซต์สามารถติดตามชุดของการปรับปรุงเป็นเอนทิตีของตัวเองที่สามารถตั้งค่าคอนฟิกได้ สามารถทดสอบได้ และสามารถเผยแพร่ได้</span><span class="sxs-lookup"><span data-stu-id="5a0b8-111">They let site authors track sets of updates as their own configurable, testable, and publishable entities.</span></span>

<span data-ttu-id="5a0b8-112">ผู้สร้างสามารถแสดงตัวอย่างการปรับปรุงในกลุ่มการเผยแพร่ที่จัดฉากได้โดยไม่ส่งผลกระทบต่อไซต์สดหรือกลุ่มการเผยแพร่ที่มีความสมบูรณ์ในตัวเองอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-112">Authors can preview updates in a staged publish group without affecting the live site or other self-contained publish groups.</span></span> <span data-ttu-id="5a0b8-113">จากนั้น ผู้สร้างสามารถจัดกำหนดการดำเนินการเผยแพร่เพื่อเผยแพร่สินค้าทั้งหมดในกลุ่มการเผยแพร่ไปยังไซต์ที่ถ่ายทอดสดพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="5a0b8-113">Authors can then schedule the publish action to simultaneously publish all the items in the publish group to the live site.</span></span> <span data-ttu-id="5a0b8-114">ความสามารถในการจัดกลุ่ม แสดงตัวอย่าง และจัดกำหนดการปรับปรุงสำหรับการเผยแพร่ เป็นสิ่งสำคัญสำหรับบริษัทระดับองค์กรจำนวนมากที่สร้างรายได้ประจำปีอย่างมากในการปรับปรุงเหตุการณ์สำคัญพื้นฐานของไซต์</span><span class="sxs-lookup"><span data-stu-id="5a0b8-114">The ability to group, preview, and schedule updates for publishing is important for many enterprise-level companies that generate considerable annual revenue around event-based site update milestones.</span></span>

<span data-ttu-id="5a0b8-115">บริษัทสามารถก่อให้เกิดค่าใช้จ่ายจากการเปิดตัวที่ช้าหรือเนื้อหาที่ไม่ได้รับการตรวจสอบที่ไม่เป็นไปอย่างราบรื่น</span><span class="sxs-lookup"><span data-stu-id="5a0b8-115">Companies can incur costs from slow or invalidated content rollouts that don't go smoothly.</span></span> <span data-ttu-id="5a0b8-116">กลุ่มการเผยแพร่ช่วยรับประกันว่าการเปิดตัวจะถูกจัดระเบียบ ตรวจสอบ และเผยแพร่ตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="5a0b8-116">Publish groups help guarantee that launches are organized, validated, and published on time.</span></span> <span data-ttu-id="5a0b8-117">ไม่ว่าจะมีขนาดใหญ่หรือเล็ก กลุ่มการเผยแพร่ให้ชุดเครื่องมือที่มีคุณค่าที่ช่วยให้ผู้สร้างสามารถจัดระเบียบและทำให้งานการปรับปรุงไซต์อย่างต่อเนื่องเป็นไปได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="5a0b8-117">Whether they are large or small, publish groups provide a valuable toolset that helps authors organize and simplify ongoing site update tasks.</span></span>

## <a name="when-to-use-publish-groups"></a><span data-ttu-id="5a0b8-118">เมื่อใดที่ควรใช้กลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-118">When to use publish groups</span></span>

<span data-ttu-id="5a0b8-119">คุณสามารถใช้กลุ่มการเผยแพร่เมื่อใดก็ตามที่คุณต้องจัดลำดับและเผยแพร่เอกสารหลายฉบับเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="5a0b8-119">You can use publish groups whenever you must stage and publish multiple documents together.</span></span> <span data-ttu-id="5a0b8-120">ตัวอย่างเช่น หากเว็บไซต์ของคุณปรับปรุงเนื้อหาทุกฤดูกาล คุณสามารถสร้างกลุ่มการเผยแพร่สำหรับการเคลื่อนไหวทางการตลาดตามฤดูกาลเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="5a0b8-120">For example, if your website updates content every season, you can create publish groups for these seasonal marketing motions.</span></span> <span data-ttu-id="5a0b8-121">กลุ่มการเผยแพร่ "การปรับปรุงตามฤดูกาลในฤดูใบไม้ร่วง" ของคุณ อาจประกอบด้วยภาพตามฤดูกาลใหม่ ชิ้นส่วนที่มีข้อความการตลาดตามฤดูกาล หน้าที่รวมคอลเลกชันผลิตภัณฑ์ตามฤดูกาล หรือการปรับปรุงเว็บไซต์ตามฤดูกาลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-121">Your "Autumn Seasonal Update" publish group might contain new seasonal images, fragments that have seasonal marketing messages, pages that include seasonal product collections, or other seasonal website updates.</span></span>

<span data-ttu-id="5a0b8-122">ข้อได้เปรียบของกลุ่มการเผยแพร่คือ คุณสามารถจัดลำดับการปรับปรุงหลายรายการควบคู่กันได้</span><span class="sxs-lookup"><span data-stu-id="5a0b8-122">An advantage of publish groups is that you can stage multiple updates in parallel.</span></span> <span data-ttu-id="5a0b8-123">ตัวอย่างเช่น ในไม่ช้าหลังจากการปรับปรุงสำหรับกลุ่มการเผยแพร่ "การปรับปรุงตามฤดูกาลในฤดูใบไม้ร่วง" อาจมีการปรับปรุงเนื้อหาสำหรับวันหยุดสุดสัปดาห์ที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="5a0b8-123">For example, soon after the update for the "Autumn Seasonal Update" publish group, there might be a content update for a specific holiday weekend.</span></span> <span data-ttu-id="5a0b8-124">ในกรณีนี้ คุณสามารถจัดลำดับเนื้อหาสำหรับกลุ่มการเผยแพร่ "การปรับปรุงตามฤดูกาลในฤดูใบไม้ร่วง" ในเวลาเดียวกันกับที่คุณจัดลำดับเนื้อหาสำหรับกลุ่มการเผยแพร่ "การปรับปรุงในวันหยุดของฤดูใบไม้ร่วง" ในเวลาต่อมา</span><span class="sxs-lookup"><span data-stu-id="5a0b8-124">In this case, you can stage content for the "Autumn Seasonal Update" publish group at the same time that you stage content for a subsequent "Autumn Holiday Update" publish group.</span></span> <span data-ttu-id="5a0b8-125">กลุ่มการเผยแพร่แต่ละกลุ่มมีชุดที่ไม่ซ้ำกันของหน้า รูปภาพ ชิ้นส่วน เท็มเพลต และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-125">Each publish group contains its own unique set of pages, images, fragments, templates, and so on.</span></span> <span data-ttu-id="5a0b8-126">คุณสามารถจัดลำดับ แสดงตัวอย่าง และตรวจสอบความถูกต้องของกลุ่มการเผยแพร่สองกลุ่มนี้ได้โดยอิสระ แต่บนเส้นเวลาที่เกิดขึ้นพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="5a0b8-126">You can stage, preview, and validate these two publish groups independently but on a concurrent timeline.</span></span> <span data-ttu-id="5a0b8-127">กลุ่มการเผยแพร่แต่ละกลุ่มสามารถถูกจัดตารางเวลาให้มีการถ่ายทอดสดบนไซต์ของคุณในวันที่และเวลาที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="5a0b8-127">Each publish group can then be scheduled to go live on your site at specific dates and times.</span></span>

## <a name="turn-on-the-publish-groups-feature"></a><span data-ttu-id="5a0b8-128">เปิดคุณลักษณะกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-128">Turn on the publish groups feature</span></span>

<span data-ttu-id="5a0b8-129">คุณลักษณะกลุ่มการเผยแพร่เป็นตัวเลือก และต้องถูกเปิดสำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-129">The publish groups feature is optional and must be turned for your site.</span></span>

<span data-ttu-id="5a0b8-130">เมื่อต้องการเปิดคุณลักษณะกลุ่มการเผยแพร่สำหรับไซต์ของคุณในเครื่องมือการสร้าง Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5a0b8-130">To turn on the publish groups feature for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="5a0b8-131">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าไซต์** เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="5a0b8-131">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="5a0b8-132">ภายใต้ **การตั้งค่าไซต์** ให้เลือก **คุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-132">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="5a0b8-133">ตั้งค่าตัวเลือก **กลุ่มการเผยแพร่** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-133">Set the **Publish groups** option to **On**.</span></span>

## <a name="create-a-publish-group"></a><span data-ttu-id="5a0b8-134">สร้างกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-134">Create a publish group</span></span>

<span data-ttu-id="5a0b8-135">เมื่อต้องการสร้างกลุ่มการเผยแพร่สำหรับไซต์ของคุณในเครื่องมือการสร้าง Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5a0b8-135">To create a publish group for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="5a0b8-136">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **กลุ่มการเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-136">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="5a0b8-137">ในแถบคำสั่งด้านบน ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-137">In the top command bar, select **New**.</span></span>
1. <span data-ttu-id="5a0b8-138">ในกล่องโต้ตอบ **สร้างกลุ่มการเผยแพร่** ภายใต้ **ชื่อกลุ่มการเผยแพร่** ให้ป้อนชื่อที่เป็นคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5a0b8-138">In the **Create Publish Group** dialog box, under **Publish Group Name**, enter a descriptive name.</span></span> <span data-ttu-id="5a0b8-139">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-139">Then select **OK**.</span></span>

## <a name="set-the-publish-group-authoring-context"></a><span data-ttu-id="5a0b8-140">ตั้งค่าบริบทการสร้างกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-140">Set the publish group authoring context</span></span>

<span data-ttu-id="5a0b8-141">ใน Commerce บริบทการสร้างเริ่มต้นคือ บริบทของไซต์ที่ถ่ายทอดสด</span><span class="sxs-lookup"><span data-stu-id="5a0b8-141">In Commerce, the default authoring context is the live site context.</span></span> <span data-ttu-id="5a0b8-142">บริบทการสร้างไซต์ที่ถ่ายทอดสดเป็นมุมมองเริ่มต้นที่คุณสามารถดูและทำการเปลี่ยนแปลงโดยตรงไปยังเว็บไซต์ของคุณโดยไม่ต้องใช้กลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-142">The live site authoring context is the default view where you can view and make changes directly to your website without using a publish group.</span></span> <span data-ttu-id="5a0b8-143">ซึ่งแสดงการปรับปรุงโดยตรงล่าสุดไปยังรุ่นที่มีการเผยแพร่ของไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-143">It represents the latest direct updates to the published version of your site.</span></span> <span data-ttu-id="5a0b8-144">ถ้าตัวควบคุมบริบทภายใต้ **กลุ่มการเผยแพร่** ในบานหน้าต่างนำทางด้านซ้าย จะแสดงชื่อว่า **ไซต์ที่ถ่ายทอดสด** คุณกำลังทำงานอยู่ในบริบทการสร้างไซต์ที่ถ่ายทอดสด</span><span class="sxs-lookup"><span data-stu-id="5a0b8-144">If the context control under **Publish Groups** in the left navigation pane shows the name **Live site**, you're working in the live site authoring context.</span></span> <span data-ttu-id="5a0b8-145">**ไซต์ที่ถ่ายทอดสด** เป็นชื่อเริ่มต้นของการควบคุมบริบท</span><span class="sxs-lookup"><span data-stu-id="5a0b8-145">**Live site** is the default name of the context control.</span></span> <span data-ttu-id="5a0b8-146">มิฉะนั้น การควบคุมบริบทจะแสดงชื่อของกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-146">Otherwise, the context control shows the name of a publish group.</span></span>

<span data-ttu-id="5a0b8-147">เพื่อทำงานในกลุ่มการเผยแพร่ คุณต้องสลับไปยังกลุ่มการเผยแพร่ที่สร้างบริบทให้</span><span class="sxs-lookup"><span data-stu-id="5a0b8-147">To work in a publish group, you must switch to the publish group authoring context for it.</span></span> <span data-ttu-id="5a0b8-148">หากต้องการตั้งค่าบริบทของกลุ่มการเผยแพร่ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5a0b8-148">To set the publish group context, follow one of these steps.</span></span>

- <span data-ttu-id="5a0b8-149">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือกตัวควบคุมบริบทภายใต้ **กลุ่มการเผยแพร่** โดยตรง และจากนั้น เลือกชื่อของกลุ่มการเผยแพร่ในรายการของตัวเลือกที่ปรากฏ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-149">In the left navigation pane, select the context control directly under **Publish Groups**, and then select the name of the publish group in the list of options that appears.</span></span> <span data-ttu-id="5a0b8-150">การควบคุมบริบทจะถูกตั้งชื่อใหม่ และแสดงชื่อของกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-150">The context control is renamed and shows the name of the publish group.</span></span>
- <span data-ttu-id="5a0b8-151">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **กลุ่มการเผยแพร่** และจากนั้น ภายใต้ **กลุ่มการเผยแพร่** ให้เลือกชื่อของกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-151">In the left navigation pane, select **Publish Groups**, and then, under **Publish Groups**, select the name of the publish group.</span></span> <span data-ttu-id="5a0b8-152">การควบคุมบริบทจะถูกตั้งชื่อใหม่ และแสดงชื่อของกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-152">The context control is renamed and shows the name of the publish group.</span></span>

<span data-ttu-id="5a0b8-153">หลังจากที่คุณตั้งค่าบริบทการสร้างของกลุ่มการเผยแพร่ คุณกำลังทำงานอยู่ในบริบทของกลุ่มการเผยแพร่เมื่อคุณดูตัวอย่างและแก้ไขเนื้อหาของไซต์</span><span class="sxs-lookup"><span data-stu-id="5a0b8-153">After you set your publish group authoring context, you're working in that publish group context when you preview and edit site content.</span></span>

<span data-ttu-id="5a0b8-154">หากต้องการกลับไปยังบริบทการสร้างไซต์ที่ถ่ายทอดสดเริ่มต้น ให้เลือกตัวควบคุมบริบท และจากนั้น เลือก **ไซต์ที่ถ่ายทอดสด**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-154">To return to the default live site authoring context, select the context control, and then select **Live site**.</span></span>

## <a name="add-pages-or-other-items-to-a-publish-group"></a><span data-ttu-id="5a0b8-155">เพิ่มหน้าหรือรายการอื่นๆ ลงในกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-155">Add pages or other items to a publish group</span></span>

<span data-ttu-id="5a0b8-156">หลังจากที่คุณได้เลือกบริบทการสร้างของกลุ่มการเผยแพร่แล้ว และตัวควบคุมบริบทในบานหน้าต่างนำทางด้านซ้ายแสดงชื่อ คุณสามารถสร้างเนื้อหาได้เช่นเดียวกับที่คุณทำในบริบทของไซต์ที่ถ่ายทอดสดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5a0b8-156">After you've selected a publish group authoring context, and the context control in the left navigation pane shows its name, you can create content just as you do in the default live site context.</span></span> <span data-ttu-id="5a0b8-157">นอกจากนี้ คุณยังสามารถเพิ่มเพจที่มีอยู่หรือสินค้าอื่นๆ ได้จากกลุ่มการเผยแพร่อื่นๆ หรือจากบริบทของไซต์ที่ถ่ายทอดสดได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="5a0b8-157">You can also add existing pages or other items from other publish groups, or from the live site context.</span></span>

<span data-ttu-id="5a0b8-158">หากต้องการคัดลอกเพจที่มีอยู่ไปยังกลุ่มการเผยแพร่ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5a0b8-158">To copy existing pages to a publish group, follow these steps.</span></span>

1. <span data-ttu-id="5a0b8-159">เลือกบริบทการสร้างเพื่อคัดลอก และจากนั้น ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **เพจ**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-159">Select the authoring context to copy from, and then, in the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="5a0b8-160">เลือกเพจที่จะเพิ่มลงในกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-160">Select the page to add to a publish group.</span></span>
1. <span data-ttu-id="5a0b8-161">ในแถบคำสั่ง ให้เลือก **คัดลอกไปยังกลุ่มการเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-161">In the command bar, select **Copy to Publish group**.</span></span>
1. <span data-ttu-id="5a0b8-162">ในกล่องโต้ตอบ **เลือกกลุ่มการเผยแพร่** เลือกกลุ่มการเผยแพร่เพื่อเพิ่มหน้า และจากนั้น ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-162">In the **Select a Publish Group** dialog box, select the publish group to add the page to, and then select **OK**.</span></span>

<span data-ttu-id="5a0b8-163">คุณสามารถใช้ขั้นตอนพื้นฐานเดียวกันในการสร้างหน้าผลิตภัณฑ์ที่กำหนดเอง URL เท็มเพลต เค้าโครง ชิ้นส่วน และสินทรัพย์ไลบรารีสื่อ หรือเพื่อเพิ่มสินค้าที่มีอยู่ของประเภทเหล่านี้ไปยังกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-163">You can use the same basic steps to create customized product pages, URLs, templates, layouts, fragments, and media library assets, or to add existing items of these types to a publish group.</span></span>

## <a name="validate-a-publish-group"></a><span data-ttu-id="5a0b8-164">ตรวจสอบกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-164">Validate a publish group</span></span>

<span data-ttu-id="5a0b8-165">เพื่อให้แน่ใจว่าคุณพึงพอใจกับการขึ้นต่อกันทั้งหมดในเนื้อหากลุ่มการเผยแพร่ และการตรวจสอบความถูกต้องผ่านทั้งหมด คุณสามารถเรียกใช้การตรวจสอบเพื่อระบุปัญหาใดๆ ที่ต้องได้รับการแก้ไข ก่อนที่คุณจะจัดกำหนดการการดำเนินการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-165">To make sure that all dependencies in publish group content are satisfied, and that all validations are passed, you can run validation to identify any issues that must be addressed before you schedule a publish action.</span></span>

<span data-ttu-id="5a0b8-166">หากต้องการตรวจสอบความถูกต้องของกลุ่มการเผยแพร่ของคุณ ก่อนที่คุณจะจัดกำหนดการ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5a0b8-166">To validate your publish group before you schedule it, follow these steps.</span></span>

1. <span data-ttu-id="5a0b8-167">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **กลุ่มการเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-167">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="5a0b8-168">เลือกกลุ่มการเผยแพร่ที่จะตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-168">Select the publish group to validate.</span></span>
1. <span data-ttu-id="5a0b8-169">ในแถบคำสั่ง ให้เลือก **ตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-169">In the command bar, select **Validate**.</span></span>

<span data-ttu-id="5a0b8-170">การตรวจสอบความถูกต้องถูกเรียกใช้บนเนื้อหาทั้งหมดในกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-170">Validation is run on all content in the publish group.</span></span> <span data-ttu-id="5a0b8-171">ปัญหาใดๆ ที่จะป้องกันการดำเนินการประกาศที่ประสบความสำเร็จจะแสดงในช่องการแจ้งเตือนที่ปรากฏที่ด้านขวาบน</span><span class="sxs-lookup"><span data-stu-id="5a0b8-171">Any issues that will prevent a successful publish action are shown in a notification box that appears in the upper right.</span></span>

> [!NOTE]
> <span data-ttu-id="5a0b8-172">การตรวจสอบจะรันโดยอัตโนมัติเสมอ เมื่อมีการจัดกำหนดการกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-172">Validation is always run automatically when a publish group is scheduled.</span></span> <span data-ttu-id="5a0b8-173">อย่างไรก็ตาม ปุ่ม **ตรวจสอบ** ในแถบคำสั่งมีประโยชน์เนื่องจากจะช่วยระบุปัญหาที่คุณต้องแก้ไข ก่อนที่คุณจะพยายามจัดกำหนดการกลุ่มการเผยแพร่ที่จะถ่ายทอดสด</span><span class="sxs-lookup"><span data-stu-id="5a0b8-173">However, the **Validate** button in the command bar is useful because it helps identify issues that you must fix before you try to schedule a publish group to go live.</span></span>

## <a name="schedule-a-publish-group-to-go-live"></a><span data-ttu-id="5a0b8-174">จัดกำหนดการกลุ่มการเผยแพร่ที่จะถ่ายทอดสด</span><span class="sxs-lookup"><span data-stu-id="5a0b8-174">Schedule a publish group to go live</span></span>

<span data-ttu-id="5a0b8-175">หากต้องการจัดกำหนดการกลุ่มการเผยแพร่ให้ถ่ายทอดสดบนไซต์ของคุณ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5a0b8-175">To schedule a publish group to go live on your site, follow these steps.</span></span>

1. <span data-ttu-id="5a0b8-176">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **กลุ่มการเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-176">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="5a0b8-177">ภายใต้ **กลุ่มการเผยแพร่** ให้เลือกกลุ่มการเผยแพร่ที่จะจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-177">Under **Publish Groups**, select the publish group to schedule.</span></span>
1. <span data-ttu-id="5a0b8-178">ในแถบคำสั่ง ให้เลือก **แก้ไขกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-178">In the command bar, select **Edit Schedule**.</span></span> <span data-ttu-id="5a0b8-179">กล่องโต้ตอบ **แก้ไขกำหนดการ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="5a0b8-179">The **Edit Schedule** dialog box appears.</span></span>
1. <span data-ttu-id="5a0b8-180">เลือกวันที่และเวลาที่กลุ่มการเผยแพร่ของคุณควรจะถ่ายทอดสด และจากนั้น ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-180">Select the date and time when your publish group should go live, and then select **OK**.</span></span>

<span data-ttu-id="5a0b8-181">หากต้องการยกเลิกการจัดกำหนดการกลุ่มการเผยแพร่ ให้ทำตามขั้นตอนที่เหมือนกัน แต่เลือก **ยกเลิกการจัดกำหนดการกลุ่มการเผยแพร่** ในกล่องโต้ตอบ **แก้ไขกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-181">To unschedule a publish group, follow the same steps, but select **Unschedule publish group** in the **Edit Schedule** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="5a0b8-182">กลุ่มการเผยแพร่ที่มีขนาดใหญ่มากอาจใช้เวลาถึงหนึ่งนาทีหรือสองนาทีในการเผยแพร่ เมื่อเวลาในการจัดกำหนดการมาถึง</span><span class="sxs-lookup"><span data-stu-id="5a0b8-182">Very large publish groups might take up to a minute or two to be published when their scheduled time arrives.</span></span> <span data-ttu-id="5a0b8-183">โปรดทราบว่าการดำเนินการเผยแพร่ไม่ใช่แบบทันที และกลุ่มการเผยแพร่ที่มีขนาดเล็กกว่าจะได้รับการเผยแพร่ที่เร็วกว่า</span><span class="sxs-lookup"><span data-stu-id="5a0b8-183">Be aware that a publish action isn't instantaneous, and that smaller publish groups will be published faster.</span></span>

## <a name="publish-groups-faq"></a><span data-ttu-id="5a0b8-184">FAQ เกี่ยวกับกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-184">Publish groups FAQ</span></span>

<span data-ttu-id="5a0b8-185">**สินค้าสามารถอยู่ในกลุ่มการเผยแพร่ได้กี่รายการ**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-185">**How many items can be in a publish group?**</span></span>

<span data-ttu-id="5a0b8-186">ขณะนี้มีขีดจำกัดของสินค้าเป็น 2,000 รายการต่อกลุ่มการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-186">Currently, there is a limit of 2,000 items per publish group.</span></span> <span data-ttu-id="5a0b8-187">โปรดทราบว่ากลุ่มการเผยแพร่ที่มีขนาดใหญ่มากอาจใช้เวลาหลายนาทีในการเผยแพร่ เมื่อเวลาในการจัดกำหนดการมาถึง</span><span class="sxs-lookup"><span data-stu-id="5a0b8-187">Be aware that very large publish groups might take several minutes to be published when their scheduled time arrives.</span></span>

<span data-ttu-id="5a0b8-188">**มีการเผยแพร่กลุ่ม เช่น รหัส "สาขา" ในคำศัพท์การพัฒนาซอฟต์แวร์หรือไม่**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-188">**Are publish groups like code "branches" in software development terminology?**</span></span>

<span data-ttu-id="5a0b8-189">ใช่และไม่</span><span class="sxs-lookup"><span data-stu-id="5a0b8-189">Yes and no.</span></span> <span data-ttu-id="5a0b8-190">อาจพิจารณาได้ว่ากลุ่มการเผยแพร่เป็นรุ่นที่แยกออกมาของไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-190">Publish groups can be thought of as forked versions of your site.</span></span> <span data-ttu-id="5a0b8-191">ด้วยวิธีนั้น รายการเหล่านั้นทำหน้าที่เหมือนสาขา</span><span class="sxs-lookup"><span data-stu-id="5a0b8-191">In that way, they do act like branches.</span></span> <span data-ttu-id="5a0b8-192">อย่างไรก็ตาม ไม่มีแนวคิดของการผสานในระดับของสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-192">However, there is no concept of a merge at the level of individual items.</span></span> <span data-ttu-id="5a0b8-193">สินค้าที่ถูกประกาศล่าสุดเพียงแค่เขียนทับสิ่งที่มีอยู่ก่อนหน้านี้ และการดำเนินการประกาศล่าสุดมักจะแทนที่การดำเนินการประกาศก่อนหน้านี้เสมอ</span><span class="sxs-lookup"><span data-stu-id="5a0b8-193">The item that is published last just overwrites what previously existed, and the most recent publish action always supersedes previous publish actions.</span></span>

<span data-ttu-id="5a0b8-194">**ฉันสามารถจัดกำหนดการกลุ่มการเผยแพร่สองกลุ่มที่จะถ่ายทอดสดในเวลาเดียวกันได้หรือไม่**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-194">**Can I schedule two publish groups to go live at the same time?**</span></span>

<span data-ttu-id="5a0b8-195">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="5a0b8-195">No.</span></span> <span data-ttu-id="5a0b8-196">สำหรับเหตุผลด้านประสิทธิภาพและความขัดแย้ง ระบบจะบังคับให้คุณย้ายกลุ่มการเผยแพร่ที่มีการจัดกำหนดการไว้ให้ห่างกันอย่างน้อยห้านาที</span><span class="sxs-lookup"><span data-stu-id="5a0b8-196">For performance and conflict reasons, the system will force you to stagger scheduled publish groups at least five minutes apart.</span></span>

<span data-ttu-id="5a0b8-197">**ฉันสามารถใช้กลุ่มการเผยแพร่เพื่อจัดกำหนดการสินค้าฝ่ายสนับสนุนของช่องทาง Omni เช่น ส่วนลด และการปรับปรุงผลิตภัณฑ์ได้หรือไม่**</span><span class="sxs-lookup"><span data-stu-id="5a0b8-197">**Can I use publish groups to schedule omnichannel back-office items, such as discounts and product updates?**</span></span>

<span data-ttu-id="5a0b8-198">ขณะนี้คุณลักษณะกลุ่มการเผยแพร่สนับสนุนเฉพาะเนื้อหาของเว็บไซต์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5a0b8-198">Currently, the publish groups feature supports only website content.</span></span> <span data-ttu-id="5a0b8-199">อย่างไรก็ตาม Microsoft ตระหนักว่าการรวมกับสถานการณ์การจัดซื้อสินค้าของฝ่ายสนับสนุนอาจมีคุณค่าสำหรับการประสานงานและการทำงานอัตโนมัติของการเปิดตัวการส่งเสริมการขายของช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="5a0b8-199">However, Microsoft is aware that integration with back-office merchandising scenarios could be valuable for the coordination and automation of omnichannel campaign launches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a0b8-200">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5a0b8-200">Additional resources</span></span>

[<span data-ttu-id="5a0b8-201">วิธีการเพิ่มเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="5a0b8-201">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="5a0b8-202">อภิธานศัพท์ของรูปแบบหน้า</span><span class="sxs-lookup"><span data-stu-id="5a0b8-202">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="5a0b8-203">สถานะและระยะเวลาใช้งานของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="5a0b8-203">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="5a0b8-204">เปิดใช้งานและใช้การใช้ร่วมกันข้ามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="5a0b8-204">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="5a0b8-205">ใช้งานโมดูล</span><span class="sxs-lookup"><span data-stu-id="5a0b8-205">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="5a0b8-206">ใช้งานส่วนย่อย</span><span class="sxs-lookup"><span data-stu-id="5a0b8-206">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="5a0b8-207">ภาพรวมของเท็มเพลตและเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="5a0b8-207">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="5a0b8-208">เลือกกำหนดการนำทางของไซต์</span><span class="sxs-lookup"><span data-stu-id="5a0b8-208">Customize site navigation</span></span>](customize-site-navigation.md)
