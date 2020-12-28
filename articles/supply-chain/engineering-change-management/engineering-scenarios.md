---
title: การฝึกปฏิบัติของคุณลักษณะการจัดการการเปลี่ยนแปลงทางวิศวกรรม
description: หัวข้อนี้จะให้การฝึกปฏิบัติที่ครอบคลุมที่แสดงวิธีการทำงานกับการจัดการการเปลี่ยนแปลงทางวิศวกรรม
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b6270bbb6780786ed4535ca2987ed44448bd81ad
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/29/2020
ms.locfileid: "4438943"
---
# <a name="engineering-change-management-feature-walkthrough"></a><span data-ttu-id="85f18-103">การฝึกปฏิบัติของคุณลักษณะการจัดการการเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-103">Engineering change management feature walkthrough</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85f18-104">หัวข้อนี้จะให้การฝึกปฏิบัติที่ครอบคลุมที่แสดงวิธีการทำงานกับการจัดการการเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-104">This topic provides an end-to-end walkthrough that shows how to work with engineering change management.</span></span> <span data-ttu-id="85f18-105">โดยผ่านแต่ละสถานการณ์ที่สำคัญที่สุด:</span><span class="sxs-lookup"><span data-stu-id="85f18-105">It goes through each of the most important scenarios:</span></span>

- <span data-ttu-id="85f18-106">การตั้งค่าคอนฟิกคุณลักษณะพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="85f18-106">Basic feature configuration</span></span>
- <span data-ttu-id="85f18-107">บริษัทวิศวกรรมสร้างผลิตภัณฑ์วิศวกรรมใหม่อย่างไร</span><span class="sxs-lookup"><span data-stu-id="85f18-107">How an engineering company creates a new engineering product</span></span>
- <span data-ttu-id="85f18-108">วิธีการที่บริษัทวิศวกรรมเผยแพร่ผลิตภัณฑ์วิศวกรรมให้กับบริษัทเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="85f18-108">How an engineering company releases an engineering product to a local company</span></span>
- <span data-ttu-id="85f18-109">วิธีการที่บริษัทในพื้นที่สามารถรีวิวและยอมรับผลิตภัณฑ์ที่นำออกใช้โดยบริษัทวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-109">How a local company can review and accept a product that has been released to it by an engineering company</span></span>
- <span data-ttu-id="85f18-110">วิธีการที่บริษัทในพื้นที่สามารถใช้ผลิตภัณฑ์วิศวกรรมในธุรกรรมมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="85f18-110">How a local company can use an engineering product in standard transactions</span></span>
- <span data-ttu-id="85f18-111">วิธีการเพิ่มผลิตภัณฑ์วิศวกรรมลงในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="85f18-111">How to add an engineering product to a sales order</span></span>
- <span data-ttu-id="85f18-112">วิธีการร้องขอการเปลี่ยนแปลงไปยังผลิตภัณฑ์วิศวกรรมโดยการสร้างคำขอเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-112">How to request changes to an engineering product by creating an engineering change request</span></span>
- <span data-ttu-id="85f18-113">วิธีการจัดกำหนดการและดำเนินการเปลี่ยนแปลงที่ร้องขอโดยการสร้างใบสั่งเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-113">How to schedule and implement requested changes by creating an engineering change order</span></span>
- <span data-ttu-id="85f18-114">วิธีการนำออกใช้ผลิตภัณฑ์ที่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="85f18-114">How to release a product that has been changed</span></span>

<span data-ttu-id="85f18-115">แบบฝึกหัดทั้งหมดในหัวข้อนี้จะใช้ข้อมูลตัวอย่างมาตรฐานที่ระบุไว้สำหรับ Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="85f18-115">All the exercises in this topic use the standard sample data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="85f18-116">นอกจากนี้ แต่ละแบบฝึกหัดจะขึ้นอยู่กับแบบฝึกหัดก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="85f18-116">Additionally, each exercise builds on the previous exercise.</span></span> <span data-ttu-id="85f18-117">ดังนั้น เราขอแนะนำให้คุณทำแบบฝึกหัดตามลำดับ ตั้งแต่เริ่มต้นจนสิ้นสุด โดยเฉพาะอย่างยิ่งถ้าคุณไม่เคยใช้คุณลักษณะการจัดการการเปลี่ยนแปลงทางวิศวกรรมมาก่อน</span><span class="sxs-lookup"><span data-stu-id="85f18-117">Therefore, we recommend that you work through the exercises in order, from beginning to end, especially if you've never used the engineering change management feature before.</span></span> <span data-ttu-id="85f18-118">ด้วยวิธีนี้ คุณจะได้เข้าใจถึงคุณลักษณะโดยสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="85f18-118">In this way, you will gain a complete understanding of the feature.</span></span>

## <a name="set-up-for-the-sample-scenario"></a><span data-ttu-id="85f18-119">การตั้งค่าสำหรับสถานการณ์ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="85f18-119">Set up for the sample scenario</span></span>

<span data-ttu-id="85f18-120">เมื่อต้องการติดตามสถานการณ์จำลองตัวอย่างที่ระบุไว้ในหัวข้อนี้ คุณต้องเตรียมคุณลักษณะด้วยการทำให้ข้อมูลสาธิตพร้อมใช้งานและเพิ่มเรกคอร์ดที่กำหนดเองสองสามเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="85f18-120">To follow the sample scenario that is provided in this topic, you must first prepare the feature by making demo data available and adding a few custom records.</span></span>

<span data-ttu-id="85f18-121">ก่อนที่คุณจะพยายามทำแบบฝึกหัดใดๆ ในส่วนที่เหลือของหัวข้อนี้ ให้ปฏิบัติตามคำแนะนำในส่วนย่อยต่อไปนี้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="85f18-121">Before you try to do any of the exercises in the rest of this topic, follow the instructions in all the following subsections.</span></span> <span data-ttu-id="85f18-122">นอกจากนี้ ส่วนย่อยเหล่านี้จะแนะนำหน้าการตั้งค่าที่สำคัญหลายหน้า ที่ซึ่งคุณจะใช้เมื่อคุณตั้งค่าการจัดการการเปลี่ยนแปลงทางวิศวกรรมสำหรับองค์กรของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="85f18-122">These subsections also introduce several important settings pages that you will use when you set up engineering change management for your own organization.</span></span>

### <a name="make-standard-demo-data-available"></a><span data-ttu-id="85f18-123">ทำให้ข้อมูลสาธิตมาตรฐานพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="85f18-123">Make standard demo data available</span></span>

<span data-ttu-id="85f18-124">ทำงานบนระบบที่ซึ่ง [มีการติดตั้งข้อมูลสาธิตมาตรฐาน](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)</span><span class="sxs-lookup"><span data-stu-id="85f18-124">Work on a system where the [standard demo data is installed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span></span> <span data-ttu-id="85f18-125">ข้อมูลสาธิตมาตรฐานจะเพิ่มข้อมูลสำหรับนิติบุคคลสาธิตหลายราย (บริษัทและองค์กร)</span><span class="sxs-lookup"><span data-stu-id="85f18-125">The standard demo data adds data for several demo legal entities (companies and organizations).</span></span> <span data-ttu-id="85f18-126">เมื่อคุณทำแบบฝึกหัด คุณจะใช้ตัวเลือกบริษัทที่ด้านขวาของแถบนำทางเพื่อสลับระหว่างบริษัทหนึ่ง (*DEMF*) ที่ตั้งค่าไว้เป็น *องค์กรวิศวกรรม* และบริษัทอื่น (*USMF*) ที่ตั้งค่าไว้เป็น *องค์กรที่ดำเนินงาน*</span><span class="sxs-lookup"><span data-stu-id="85f18-126">As you work through the exercises, you will use the company picker on the right side of the navigation bar to switch between one company (*DEMF*) that is set up as an *engineering organization* and another company (*USMF*) that is set up as an *operational organization*.</span></span>

### <a name="set-up-an-engineering-organization"></a><span data-ttu-id="85f18-127">ตั้งค่าองค์กรวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-127">Set up an engineering organization</span></span>

<span data-ttu-id="85f18-128">องค์กรวิศวกรรมเป็นเจ้าของข้อมูลทางวิศวกรรม และรับผิดชอบการออกแบบผลิตภัณฑ์และการเปลี่ยนแปลงผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="85f18-128">An engineering organization owns the engineering data, and is responsible for product design and product changes.</span></span> <span data-ttu-id="85f18-129">ถ้าต้องการตั้งค่าองค์กรวิศวกรรมของคุณ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="85f18-129">To set up your engineering organizations, follow these steps.</span></span>

1. <span data-ttu-id="85f18-130">ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม &gt; การตั้งค่า &gt; แอททริบิวต์ทางวิศวกรรม**</span><span class="sxs-lookup"><span data-stu-id="85f18-130">Go to **Engineering change management &gt; Setup &gt; Engineering organizations**.</span></span>
1. <span data-ttu-id="85f18-131">เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด และตั้งค่าค่าต่อไปนี้สำหรับแถวนั้น:</span><span class="sxs-lookup"><span data-stu-id="85f18-131">Select **New** to add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="85f18-132">**องค์กรทางวิศวกรรม:** *DEMF*</span><span class="sxs-lookup"><span data-stu-id="85f18-132">**Engineering organization:** *DEMF*</span></span>
    - <span data-ttu-id="85f18-133">**ชื่อองค์กร:** *ระบบความบันเทิง Contoso ในเยอรมนี*</span><span class="sxs-lookup"><span data-stu-id="85f18-133">**Organization name:** *Contoso Entertainment System Germany*</span></span>

    <span data-ttu-id="85f18-134">![การเพิ่มองค์กรวิศวกรรม](media/engineering-org.png "การเพิ่มองค์กรวิศวกรรม")</span><span class="sxs-lookup"><span data-stu-id="85f18-134">![Adding an engineering organization](media/engineering-org.png "Adding an engineering organization")</span></span>

### <a name="set-up-the-version-product-dimension-group"></a><span data-ttu-id="85f18-135">ตั้งค่ากลุ่มมิติผลิตภัณฑ์ของรุ่น</span><span class="sxs-lookup"><span data-stu-id="85f18-135">Set up the version product dimension group</span></span>

1. <span data-ttu-id="85f18-136">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ &gt; การตั้งค่า &gt; มิติและกลุ่มตัวแปร &gt; กลุ่มมิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="85f18-136">Go to **Product information management &gt; Setup &gt; Dimensions and variant groups &gt; Product dimension groups**.</span></span>
1. <span data-ttu-id="85f18-137">เลือก **สร้าง** เพื่อสร้างกลุ่มมิติผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="85f18-137">Select **New** to create a product dimension group.</span></span>
1. <span data-ttu-id="85f18-138">ตั้งค่าฟิลด์ **ชื่อ** เป็น *รุ่น*</span><span class="sxs-lookup"><span data-stu-id="85f18-138">Set the **Name** field to *Version*.</span></span>
1. <span data-ttu-id="85f18-139">เลือก **บันทึก** เพื่อบันทึกค่ามิติและโหลดใหม่ลงใน FastTab **มิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="85f18-139">Select **Save** to save the new dimension and load values onto the **Product dimensions** FastTab.</span></span>
1. <span data-ttu-id="85f18-140">บน FastTab **มิติของผลิตภัณฑ์** ให้ตั้งค่า **รุ่น** เป็นมิติของผลิตภัณฑ์ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="85f18-140">On the **Product dimensions** FastTab, set **Version** as an active product dimension.</span></span>

    <span data-ttu-id="85f18-141">![การเพิ่มกลุ่มมิติผลิตภัณฑ์](media/product-dimension-groups.png "การเพิ่มกลุ่มมิติผลิตภัณฑ์")</span><span class="sxs-lookup"><span data-stu-id="85f18-141">![Adding a product dimension group](media/product-dimension-groups.png "Adding a product dimension group")</span></span>

### <a name="set-up-product-lifecycle-states"></a><span data-ttu-id="85f18-142">ตั้งค่าสถานะของวงจรการใช้ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="85f18-142">Set up product lifecycle states</span></span>

<span data-ttu-id="85f18-143">เนื่องจากผลิตภัณฑ์วิศวกรรมจะผ่านสถานะของวงจรการใช้ จึงเป็นเรื่องสำคัญที่คุณสามารถควบคุมว่าจะอนุญาตให้มีธุรกรรมใดสำหรับสถานะของวงจรการใช้แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="85f18-143">As an engineering product goes through its lifecycle, it's important that you be able to control which transactions are allowed for each lifecycle state.</span></span> <span data-ttu-id="85f18-144">หากต้องการตั้งค่าสถานะของวงจรการใช้ของผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="85f18-144">To set up the product lifecycle states, follow these steps.</span></span>

1. <span data-ttu-id="85f18-145">ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม &gt; การตั้งค่า &gt; สถานะของวงจรการใช้ของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="85f18-145">Go to **Engineering change management &gt; Setup &gt; Product lifecycle state**.</span></span>
1. <span data-ttu-id="85f18-146">เลือก **สร้าง** เพื่อเพิ่มสถานะของวงจรการใช้ และตั้งค่าค่าต่อไปนี้สำหรับสถานะนั้น:</span><span class="sxs-lookup"><span data-stu-id="85f18-146">Select **New** to add a lifecycle state, and set the following values for it:</span></span>

    - <span data-ttu-id="85f18-147">**สถานะ:** *เกี่ยวกับการดำเนินงาน*</span><span class="sxs-lookup"><span data-stu-id="85f18-147">**State:** *Operational*</span></span>
    - <span data-ttu-id="85f18-148">**คำอธิบาย:** *เกี่ยวกับการดำเนินงาน*</span><span class="sxs-lookup"><span data-stu-id="85f18-148">**Description:** *Operational*</span></span>

1. <span data-ttu-id="85f18-149">เลือก **บันทึก** เพื่อบันทึกค่าสถานะของวงจรการใช้และโหลดใหม่ลงใน FastTab **กระบวนการทางธุรกิจที่เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="85f18-149">Select **Save** to save the new lifecycle state and load values onto the **Enabled business processes** FastTab.</span></span>
1. <span data-ttu-id="85f18-150">บน FastTab **กระบวนการทางธุรกิจที่เปิดใช้งาน** ให้เลือกกระบวนการทางธุรกิจที่ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="85f18-150">On the **Enabled business processes** FastTab, select the business processes that should be available.</span></span> <span data-ttu-id="85f18-151">สำหรับตัวอย่างนี้ ให้เว้นฟิลด์ **นโยบาย** ที่ตั้งค่าเป็น *เปิดใช้งาน* สำหรับกระบวนการทางธุรกิจทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="85f18-151">For this example, leave the **Policy** field set to *Enabled* for all business processes.</span></span>

    <span data-ttu-id="85f18-152">![การเปิดใช้งานกระบวนการธุรกิจสำหรับสถานะของวงจรการใช้](media/product-lifecycle-states-1.png "การเปิดใช้งานกระบวนการธุรกิจสำหรับสถานะของวงจรการใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-152">![Enabling business processes for a lifecycle state](media/product-lifecycle-states-1.png "Enabling business processes for a lifecycle state")</span></span>

1. <span data-ttu-id="85f18-153">เลือก **สร้าง** เพื่อเพิ่มสถานะของวงจรการใช้อื่น และตั้งค่าค่าต่อไปนี้สำหรับสถานะนั้น:</span><span class="sxs-lookup"><span data-stu-id="85f18-153">Select **New** to add another lifecycle state, and set the following values for it:</span></span>

    - <span data-ttu-id="85f18-154">**สถานะ:** *ต้นแบบ*</span><span class="sxs-lookup"><span data-stu-id="85f18-154">**State:** *Prototype*</span></span>
    - <span data-ttu-id="85f18-155">**คำอธิบาย:** *ต้นแบบ*</span><span class="sxs-lookup"><span data-stu-id="85f18-155">**Description:** *Prototype*</span></span>

1. <span data-ttu-id="85f18-156">เลือก **บันทึก** เพื่อบันทึกค่าสถานะของวงจรการใช้และโหลดใหม่ลงใน FastTab **กระบวนการทางธุรกิจที่เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="85f18-156">Select **Save** to save the new lifecycle state and load values onto the **Enabled business processes** FastTab.</span></span>
1. <span data-ttu-id="85f18-157">บน FastTab **กระบวนการทางธุรกิจที่เปิดใช้งาน** ให้เลือกกระบวนการทางธุรกิจที่ควรพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="85f18-157">On the **Enabled business processes** FastTab, select the business processes that should be available.</span></span> <span data-ttu-id="85f18-158">สำหรับตัวอย่างนี้ ให้ตั้งค่าฟิลด์ **นโยบาย** ที่ตั้งค่าเป็น *เปิดใช้งานพร้อมคำเตือน* สำหรับกระบวนการทางธุรกิจทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="85f18-158">For this example, set the **Policy** field to *Enabled with warning* for all business processes.</span></span>

    <span data-ttu-id="85f18-159">![การเปิดใช้งาน (พร้อมคำเตือน) กระบวนการธุรกิจสำหรับสถานะของวงจรการใช้](media/product-lifecycle-states-2.png "การเปิดใช้งาน (พร้อมคำเตือน) กระบวนการธุรกิจสำหรับสถานะของวงจรการใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-159">![Enabling (with warnings) business processes for a lifecycle state](media/product-lifecycle-states-2.png "Enabling (with warnings) business processes for a lifecycle state")</span></span>

### <a name="set-up-a-version-number-rule"></a><span data-ttu-id="85f18-160">ตั้งค่ากฎหมายเลขรุ่น</span><span class="sxs-lookup"><span data-stu-id="85f18-160">Set up a version number rule</span></span>

1. <span data-ttu-id="85f18-161">ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม &gt; การตั้งค่า &gt; กฎหมายเลขรุ่นของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="85f18-161">Go to **Engineering change management &gt; Setup &gt; Product version number rule**.</span></span>
1. <span data-ttu-id="85f18-162">เลือก **สร้าง** เพื่อเพิ่มกฎ และตั้งค่าค่าต่อไปนี้สำหรับกฎนั้น:</span><span class="sxs-lookup"><span data-stu-id="85f18-162">Select **New** to add a rule, and set the following values for it:</span></span>

    - <span data-ttu-id="85f18-163">**ชื่อ:** *อัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="85f18-163">**Name:** *Auto*</span></span>
    - <span data-ttu-id="85f18-164">**กฎหมายเลข:** *อัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="85f18-164">**Number rule:** *Auto*</span></span>
    - <span data-ttu-id="85f18-165">**รูปแบบ:** *V-\#\#*</span><span class="sxs-lookup"><span data-stu-id="85f18-165">**Format:** *V-\#\#*</span></span>

    <span data-ttu-id="85f18-166">![การเพิ่มกฎหมายเลขรุ่นของผลิตภัณฑ์](media/version-number-rule.png "การเพิ่มกฎหมายเลขรุ่นของผลิตภัณฑ์")</span><span class="sxs-lookup"><span data-stu-id="85f18-166">![Adding a product version number rule](media/version-number-rule.png "Adding a product version number rule")</span></span>

### <a name="set-up-a-product-release-policy"></a><span data-ttu-id="85f18-167">ตั้งค่านโยบายการนำผลิตภัณฑ์ออกใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-167">Set up a product release policy</span></span>

1. <span data-ttu-id="85f18-168">ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม &gt; การตั้งค่า &gt; นโยบายการนำผลิตภัณฑ์ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-168">Go to **Engineering change management &gt; Setup &gt; Product release policies**.</span></span>
1. <span data-ttu-id="85f18-169">เลือก **สร้าง** เพื่อเพิ่มนโยบายการนำออกใช้ และตั้งค่าค่าต่อไปนี้สำหรับนโยบายนั้น:</span><span class="sxs-lookup"><span data-stu-id="85f18-169">Select **New** to add a release policy, and set the following values for it:</span></span>

    - <span data-ttu-id="85f18-170">**ชื่อ:** *ส่วนประกอบ*</span><span class="sxs-lookup"><span data-stu-id="85f18-170">**Name:** *Components*</span></span>
    - <span data-ttu-id="85f18-171">**คำอธิบาย:** *ส่วนประกอบ*</span><span class="sxs-lookup"><span data-stu-id="85f18-171">**Description:** *Components*</span></span>

1. <span data-ttu-id="85f18-172">บนแท็บด่วน **ทั่วไป** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-172">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="85f18-173">**ชนิดผลิตภัณฑ์:** *สินค้า*</span><span class="sxs-lookup"><span data-stu-id="85f18-173">**Product type:** *Item*</span></span>
    - <span data-ttu-id="85f18-174">**ใช้เท็มเพลต:** *เสมอ*</span><span class="sxs-lookup"><span data-stu-id="85f18-174">**Apply templates:** *Always*</span></span>
    - <span data-ttu-id="85f18-175">**ใช้งานอยู่:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="85f18-175">**Active:** *Yes*</span></span>

1. <span data-ttu-id="85f18-176">บน FastTab **ผลิตภัณฑ์ทั้งหมด** ให้เลือก **เพิ่ม** เพื่อเพิ่มบรรทัด และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-176">On the **All products** FastTab, select **Add** to add a line, and set the following values for it:</span></span>

    - <span data-ttu-id="85f18-177">**บริษัท:** *DEMF*</span><span class="sxs-lookup"><span data-stu-id="85f18-177">**Company:** *DEMF*</span></span>
    - <span data-ttu-id="85f18-178">**ผลิตภัณฑ์ที่นำออกใช้ในเท็มเพลต:** *D0006*</span><span class="sxs-lookup"><span data-stu-id="85f18-178">**Template released product:** *D0006*</span></span>

1. <span data-ttu-id="85f18-179">เลือก **เพิ่ม** เพื่อเพิ่มอีกหนึ่งบรรทัด และตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-179">Select **Add** to add another line, and set the following values for it:</span></span>

    - <span data-ttu-id="85f18-180">**รหัสบัญชีบริษัท:** *USMF*</span><span class="sxs-lookup"><span data-stu-id="85f18-180">**Company accounts ID:** *USMF*</span></span>
    - <span data-ttu-id="85f18-181">**ผลิตภัณฑ์ที่นำออกใช้ในเท็มเพลต:** *D0006*</span><span class="sxs-lookup"><span data-stu-id="85f18-181">**Template released product:** *D0006*</span></span>
    - <span data-ttu-id="85f18-182">**รับ BOM:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="85f18-182">**Receive BOM:** Select this check box.</span></span>
    - <span data-ttu-id="85f18-183">**คัดลอกการอนุมัติ BOM:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="85f18-183">**Copy BOM approval:** Select this check box.</span></span>
    - <span data-ttu-id="85f18-184">**คัดลอกการเรียกใช้งาน BOM:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="85f18-184">**Copy BOM activation:** Select this check box.</span></span>
    - <span data-ttu-id="85f18-185">**รับกระบวนการผลิต:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="85f18-185">**Receive route:** Select this check box.</span></span>
    - <span data-ttu-id="85f18-186">**คัดลอกการอนุมัติกระบวนการผลิต:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="85f18-186">**Copy route approval:** Select this check box.</span></span>
    - <span data-ttu-id="85f18-187">**คัดลอกการเรียกใช้งานกระบวนการผลิต:** เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="85f18-187">**Copy route activation:** Select this check box.</span></span>

    <span data-ttu-id="85f18-188">![การเพิ่มนโยบายการนำผลิตภัณฑ์ออกใช้](media/product-release-policy.png "การเพิ่มนโยบายการนำผลิตภัณฑ์ออกใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-188">![Adding a product release policy](media/product-release-policy.png "Adding a product release policy")</span></span>

### <a name="set-up-an-engineering-product-category"></a><span data-ttu-id="85f18-189">ตั้งค่าประเภทผลิตภัณฑ์วิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-189">Set up an engineering product category</span></span> 

<span data-ttu-id="85f18-190">ประเภทผลิตภัณฑ์วิศวกรรมมีพื้นฐานสำหรับการสร้างผลิตภัณฑ์วิศวกรรม (นั่นคือ ผลิตภัณฑ์ที่มีการกำหนดรุ่นและควบคุมผ่านการจัดการการเปลี่ยนแปลงทางวิศวกรรม)</span><span class="sxs-lookup"><span data-stu-id="85f18-190">Engineering product categories provide the basis for creating engineering products (that is, products that are versioned and controlled through engineering change management).</span></span> <span data-ttu-id="85f18-191">ถ้าต้องการตั้งค่าประเภทผลิตภัณฑ์วิศวกรรม ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="85f18-191">To set up engineering product categories, follow these steps.</span></span>

1. <span data-ttu-id="85f18-192">ไปที่ **การจัดการการเปลี่ยนแปลงทางวิศวกรรม &gt; รายละเอียดประเภทผลิตภัณฑ์วิศวกรรม**</span><span class="sxs-lookup"><span data-stu-id="85f18-192">Go to **Engineering change management &gt; Engineering product category details**.</span></span>
1. <span data-ttu-id="85f18-193">เลือก **สร้าง** เพื่อสร้างประเภท</span><span class="sxs-lookup"><span data-stu-id="85f18-193">Select **New** to create a category.</span></span>
1. <span data-ttu-id="85f18-194">บน FastTab **รายละเอียด** ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-194">On the **Details** FastTab, set the following values:</span></span>

    - <span data-ttu-id="85f18-195">**ชื่อ:** *ส่วนประกอบ*</span><span class="sxs-lookup"><span data-stu-id="85f18-195">**Name:** *Components*</span></span>
    - <span data-ttu-id="85f18-196">**องค์กรทางวิศวกรรม:** *DEMF*</span><span class="sxs-lookup"><span data-stu-id="85f18-196">**Engineering organization:** *DEMF*</span></span>
    - <span data-ttu-id="85f18-197">**ชนิดผลิตภัณฑ์:** *สินค้า*</span><span class="sxs-lookup"><span data-stu-id="85f18-197">**Product type:** *Item*</span></span>
    - <span data-ttu-id="85f18-198">**ติดตามรุ่นในธุรกรรม:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="85f18-198">**Track version in transactions:** *Yes*</span></span>
    - <span data-ttu-id="85f18-199">**กลุ่มมิติของผลิตภัณฑ์:** *รุ่น*</span><span class="sxs-lookup"><span data-stu-id="85f18-199">**Product dimension group:** *Version*</span></span>
    - <span data-ttu-id="85f18-200">**สถานะของวงจรการใช้ของผลิตภัณฑ์เมื่อสร้าง:** *เกี่ยวกับการดำเนินงาน*</span><span class="sxs-lookup"><span data-stu-id="85f18-200">**Product lifecycle state at creation:** *Operational*</span></span>
    - <span data-ttu-id="85f18-201">**กฎหมายเลขรุ่น:** *อัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="85f18-201">**Version number rule:** *Auto*</span></span>
    - <span data-ttu-id="85f18-202">**บังคับใช้การมีผลบังคับใช้:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="85f18-202">**Enforce effectivity:** *No*</span></span>
    - <span data-ttu-id="85f18-203">**ใช้ระบบการตั้งชื่อกฎของหมายเลข:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="85f18-203">**Use number rule nomenclature:** *No*</span></span>
    - <span data-ttu-id="85f18-204">**ใช้ระบบการตั้งชื่อกฎของชื่อ:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="85f18-204">**Use name rule nomenclature:** *No*</span></span>
    - <span data-ttu-id="85f18-205">**ใช้ระบบการตั้งชื่อกฎของคำอธิบาย:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="85f18-205">**Use description rule nomenclature:** *No*</span></span>

1. <span data-ttu-id="85f18-206">บน FastTab **นโยบายการนำออกใช้** ให้ตั้งค่าฟิลด์ **นโยบายการนำผลิตภัณฑ์ออกใช้** เป็น *ส่วนประกอบ*</span><span class="sxs-lookup"><span data-stu-id="85f18-206">On the **Release policy** FastTab, set the **Product release policy** field to *Components*.</span></span>
1. <span data-ttu-id="85f18-207">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="85f18-207">Select **Save**.</span></span>

    <span data-ttu-id="85f18-208">![การเพิ่มประเภทผลิตภัณฑ์วิศวกรรม](media/product-category-details.png "การเพิ่มประเภทผลิตภัณฑ์วิศวกรรม")</span><span class="sxs-lookup"><span data-stu-id="85f18-208">![Adding an engineering product category](media/product-category-details.png "Adding an engineering product category")</span></span>

### <a name="set-up-product-acceptance-conditions"></a><span data-ttu-id="85f18-209">ตั้งค่าเงื่อนไขการยอมรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="85f18-209">Set up product acceptance conditions</span></span>

1. <span data-ttu-id="85f18-210">ใช้ตัวเลือกบริษัทที่ด้านขวาของแถบนำทางเพื่อสลับไปยังนิติบุคคล *USMF* (บริษัท)</span><span class="sxs-lookup"><span data-stu-id="85f18-210">Use the company picker on the right side of the navigation bar to switch to the *USMF* legal entity (company).</span></span>
1. <span data-ttu-id="85f18-211">ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม &gt; การตั้งค่า &gt; พารามิเตอร์การจัดการการเปลี่ยนแปลงวิศวกรรม**</span><span class="sxs-lookup"><span data-stu-id="85f18-211">Go to **Engineering change management &gt; Setup &gt; Engineering change management parameters**.</span></span>
1. <span data-ttu-id="85f18-212">บนแท็บ **การควบคุมการนำออกใช้** ในส่วน **การยอมรับผลิตภัณฑ์** ให้ตั้งค่าฟิลด์ **การยอมรับผลิตภัณฑ์** เป็น *ด้วยตนเอง*</span><span class="sxs-lookup"><span data-stu-id="85f18-212">On the **Release control** tab, in the **Product acceptance** section, set the **Product acceptance** field to *Manual*.</span></span>

    <span data-ttu-id="85f18-213">![การตั้งค่าเงื่อนไขการยอมรับผลิตภัณฑ์](media/engineering-change-management-parameters.png "การตั้งค่าเงื่อนไขการยอมรับผลิตภัณฑ์")</span><span class="sxs-lookup"><span data-stu-id="85f18-213">![Setting up product acceptance conditions](media/engineering-change-management-parameters.png "Setting up product acceptance conditions")</span></span>

## <a name="create-a-new-engineering-product"></a><span data-ttu-id="85f18-214">สร้างผลิตภัณฑ์วิศวกรรมใหม่</span><span class="sxs-lookup"><span data-stu-id="85f18-214">Create a new engineering product</span></span>

<span data-ttu-id="85f18-215">ผลิตภัณฑ์วิศวกรรมเป็นผลิตภัณฑ์ที่มีการกำหนดเวอร์ชันและควบคุมผ่านทางการจัดการการเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-215">An engineering product is a product that is versioned and controlled through engineering change management.</span></span> <span data-ttu-id="85f18-216">กล่าวอีกอย่างหนึ่งคือ คุณสามารถควบคุมการเปลี่ยนแปลงในระหว่างอายุการใช้งาน และข้อมูลการเปลี่ยนแปลงจะถูกบันทึกโดยใช้ใบสั่งเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-216">In other words, you can control the changes during its life, and the change information will be saved using engineering change orders.</span></span> <span data-ttu-id="85f18-217">เมื่อต้องการสร้างผลิตภัณฑ์วิศวกรรม ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="85f18-217">To create engineering products, follow these steps.</span></span>

1. <span data-ttu-id="85f18-218">ตรวจสอบให้แน่ใจว่าคุณกำลังอยู่ในนิติบุคคลขององค์กรวิศวกรรมของคุณ (*DEMF* สำหรับตัวอย่างนี้)</span><span class="sxs-lookup"><span data-stu-id="85f18-218">Make sure that you're in the legal entity of your engineering organization (*DEMF* for this example).</span></span> <span data-ttu-id="85f18-219">ใช้ตัวเลือกบริษัททางด้านขวาของแถบนำทางตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="85f18-219">Use the company picker on the right side of the navigation bar as required.</span></span>
1. <span data-ttu-id="85f18-220">เปิดหน้า **ผลิตภัณฑ์ที่นำออกใช้** โดยทำตามหนึ่งในขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-220">Open the **Released products** page by following one of these steps:</span></span>

    - <span data-ttu-id="85f18-221">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์ &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-221">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
    - <span data-ttu-id="85f18-222">ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม &gt; ทั่วไป &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-222">Go to **Engineering change management &gt; Common &gt; Released products**.</span></span>

1. <span data-ttu-id="85f18-223">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **สร้าง** ให้เลือก **ผลิตภัณฑ์วิศวกรรม**</span><span class="sxs-lookup"><span data-stu-id="85f18-223">On the Action Pane, on the **Product** tab, in the **New** group, select **Engineering product**.</span></span>
1. <span data-ttu-id="85f18-224">ในกล่องโต้ตอบ **ผลิตภัณฑ์ใหม่** ให้ตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-224">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="85f18-225">**ประเภทผลิตภัณฑ์วิศวกรรม:** *ส่วนประกอบ*</span><span class="sxs-lookup"><span data-stu-id="85f18-225">**Engineering Product Category:** *Components*</span></span>
    - <span data-ttu-id="85f18-226">**หมายเลขของผลิตภัณฑ์:** *Z0001*</span><span class="sxs-lookup"><span data-stu-id="85f18-226">**Product number:** *Z0001*</span></span>
    - <span data-ttu-id="85f18-227">**ชื่อผลิตภัณฑ์:** *ชุดลำโพง*</span><span class="sxs-lookup"><span data-stu-id="85f18-227">**Product name:** *Speaker set*</span></span>

    <span data-ttu-id="85f18-228">![การเพิ่มผลิตภัณฑ์วิศวกรรม](media/new-product-dialog.png "การเพิ่มผลิตภัณฑ์วิศวกรรม")</span><span class="sxs-lookup"><span data-stu-id="85f18-228">![Adding an engineering product](media/new-product-dialog.png "Adding an engineering product")</span></span>

    <span data-ttu-id="85f18-229">โปรดสังเกตว่ามีการตั้งค่าฟิลด์ **รุ่น** โดยอัตโนมัติโดยใช้กฎหมายเลขรุ่นของผลิตภัณฑ์ที่คุณตั้งค่าไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="85f18-229">Note that the **Version** field is automatically set by using the product version number rule that you set up earlier.</span></span>

1. <span data-ttu-id="85f18-230">เลือก **ตกลง** เพื่อสร้างผลิตภัณฑ์ และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="85f18-230">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="85f18-231">หน้ารายละเอียดสำหรับผลิตภัณฑ์ใหม่ถูกเปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="85f18-231">The details page for the new product is opened.</span></span> <span data-ttu-id="85f18-232">โปรดสังเกตว่ามีการเติมค่าในฟิลด์บางฟิลด์ไว้แล้ว เช่น **กลุ่มมิติการจัดเก็บ** **กลุ่มมิติการติดตาม** และ/หรือ **กลุ่มแบบจำลองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="85f18-232">Notice that values are already filled in for some fields, such as **Storage dimension group**, **Tracking dimension group**, and/or **Item model group**.</span></span> <span data-ttu-id="85f18-233">ฟิลด์เหล่านี้ได้รับการตั้งค่าโดยอัตโนมัติ เนื่องจากมีการนำผลิตภัณฑ์ออกใช้ในนิติบุคคล *DEMF* และใช้นโยบายการนำผลิตภัณฑ์ออกใช้ของ *ส่วนประกอบ* ซึ่งสัมพันธ์กับประเภทผลิตภัณฑ์วิศวกรรมของ *ส่วนประกอบ*</span><span class="sxs-lookup"><span data-stu-id="85f18-233">These fields were automatically set because the product is being released in the *DEMF* legal entity and uses the *Components* product release policy, which is associated with the *Components* engineering product category.</span></span> <span data-ttu-id="85f18-234">เนื่องจากคุณเคยใช้สินค้า *D0006* เป็นเท็มเพลตเพื่อตั้งค่าบรรทัดสำหรับนิติบุคคล *DEMF* ค่าที่ถูกกรอกข้อมูลแล้วถูกนำมาจากสินค้า *D0006*</span><span class="sxs-lookup"><span data-stu-id="85f18-234">Because you previously used item *D0006* as a template to set up a line for the *DEMF* legal entity, the values that were filled in were taken from item *D0006*.</span></span>

    <span data-ttu-id="85f18-235">![รายละเอียดผลิตภัณฑ์ที่นำออกใช้](media/product-details.png "รายละเอียดผลิตภัณฑ์ที่นำออกใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-235">![Released product details](media/product-details.png "Released product details")</span></span>

1. <span data-ttu-id="85f18-236">บนบานหน้าต่างการดำเนินการ บนแท็บ **วิศวกร** ในกลุ่ม **การจัดการการเปลี่ยนแปลงทางวิศวกรรม** ให้เลือก **รุ่นวิศวกรรม** เพื่อดูรุ่นของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="85f18-236">On the Action Pane, on the **Engineer** tab, in the **Engineering change management** group, select **Engineering versions** to view the versions of the product.</span></span>

    <span data-ttu-id="85f18-237">![รุ่นทางวิศวกรรม](media/engineering-versions-list.png "รุ่นทางวิศวกรรม")</span><span class="sxs-lookup"><span data-stu-id="85f18-237">![Engineering versions](media/engineering-versions-list.png "Engineering versions")</span></span>

1. <span data-ttu-id="85f18-238">บนหน้า **รุ่นวิศวกรรม** โปรดสังเกตว่ามีเพียงรุ่นเดียวสำหรับผลิตภัณฑ์ และใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="85f18-238">On the **Engineering versions** page, notice that there is only one version for the product, and it's active.</span></span>
1. <span data-ttu-id="85f18-239">เลือกรุ่นเพื่อดูรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="85f18-239">Select the version to view its details.</span></span>

    <span data-ttu-id="85f18-240">![รายละเอียดรุ่นวิศวกรรม](media/engineering-version-details.png "รายละเอียดรุ่นวิศวกรรม")</span><span class="sxs-lookup"><span data-stu-id="85f18-240">![Engineering version details](media/engineering-version-details.png "Engineering version details")</span></span>

1. <span data-ttu-id="85f18-241">บนหน้า **รุ่นวิศวกรรม** บน FastTab **สูตรการผลิต** ให้เลือก **สร้าง BOM**</span><span class="sxs-lookup"><span data-stu-id="85f18-241">On the **Engineering version** page, on the **Bill of material** FastTab, select **Create BOM**.</span></span>
1. <span data-ttu-id="85f18-242">ในกล่องโต้ตอบ **สร้าง BOM** ให้ตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-242">In the **Create BOM** dialog box, set the following values:</span></span>

    - <span data-ttu-id="85f18-243">**หมายเลข BOM:** Z0001</span><span class="sxs-lookup"><span data-stu-id="85f18-243">**BOM number:** Z0001</span></span>
    - <span data-ttu-id="85f18-244">**ชื่อ:** ชุดลำโพง</span><span class="sxs-lookup"><span data-stu-id="85f18-244">**Name:** Speaker set</span></span>
    - <span data-ttu-id="85f18-245">**ไซต์:** 1</span><span class="sxs-lookup"><span data-stu-id="85f18-245">**Site:** 1</span></span>

    <span data-ttu-id="85f18-246">![กำลังสร้าง BOM](media/create-bom.png "กำลังสร้าง BOM")</span><span class="sxs-lookup"><span data-stu-id="85f18-246">![Creating a BOM](media/create-bom.png "Creating a BOM")</span></span>

1. <span data-ttu-id="85f18-247">เลือก **ตกลง** เพื่อเพิ่ม BOM และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="85f18-247">Select **OK** to add the BOM and close the dialog box.</span></span>
1. <span data-ttu-id="85f18-248">บน FastTab **สูตรการผลิต** ให้เลือก **สูตรการผลิต**</span><span class="sxs-lookup"><span data-stu-id="85f18-248">On the **Bill of materials** FastTab, select **Bill of material**.</span></span>
1. <span data-ttu-id="85f18-249">บนหน้า **สูตรการผลิต** บน FastTab **สูตรการผลิต** เพิ่มบรรทัดสามบรรทัด แต่ละบรรทัดสำหรับหมายเลขสินค้า *D0001* *D0003* และ *D0006*</span><span class="sxs-lookup"><span data-stu-id="85f18-249">On the **Bill of materials** page, on the **Bill of materials lines** FastTab, add three lines, one each for item numbers *D0001*, *D0003*, and *D0006*.</span></span>

    <span data-ttu-id="85f18-250">![การเพิ่มบรรทัด BOM](media/bom.png "การเพิ่มบรรทัด BOM")</span><span class="sxs-lookup"><span data-stu-id="85f18-250">![Adding BOM lines](media/bom.png "Adding BOM lines")</span></span>

1. <span data-ttu-id="85f18-251">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="85f18-251">Select **Save**.</span></span>
1. <span data-ttu-id="85f18-252">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="85f18-252">Close the page.</span></span>
1. <span data-ttu-id="85f18-253">บนหน้า **รุ่นวิศวกรรม** บน FastTab **สูตรการผลิต** ให้เลือก **อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="85f18-253">On the **Engineering version** page, on the **Bill of material** FastTab, select **Approve**.</span></span>
1. <span data-ttu-id="85f18-254">ในกล่องโต้ตอบที่ปรากฏ เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="85f18-254">In the dialog box that appears, select **OK**.</span></span>

    <span data-ttu-id="85f18-255">![การอนุมัติ BOM](media/approve-dialog.png "การอนุมัติ BOM")</span><span class="sxs-lookup"><span data-stu-id="85f18-255">![Approving the BOM](media/approve-dialog.png "Approving the BOM")</span></span>

1. <span data-ttu-id="85f18-256">บนหน้า **รุ่นวิศวกรรม** บน FastTab **สูตรการผลิต** ให้เลือก **เรียกใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="85f18-256">On the **Engineering version** page, on the **Bill of material** FastTab, select **Activate**.</span></span>
1. <span data-ttu-id="85f18-257">โปรดสังเกตว่า มีการเลือกกล่องกาเครื่องหมาย **ใช้งานอยู่** และ **ได้รับการอนุมัติ** สำหรับ BOM</span><span class="sxs-lookup"><span data-stu-id="85f18-257">Notice that the **Active** and **Approved** check boxes are selected for the BOM.</span></span>

    <span data-ttu-id="85f18-258">![BOM ที่ใช้งานอยู่และที่อนุมัติ](media/approved-bom.png "BOM ที่ใช้งานอยู่และที่อนุมัติ")</span><span class="sxs-lookup"><span data-stu-id="85f18-258">![Active and approved BOM](media/approved-bom.png "Active and approved BOM")</span></span>

1. <span data-ttu-id="85f18-259">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="85f18-259">Close the page.</span></span>

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a><span data-ttu-id="85f18-260">นำผลิตภัณฑ์วิศวกรรมออกใช้ไปยังบริษัทเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="85f18-260">Release an engineering product to a local company</span></span>

<span data-ttu-id="85f18-261">ขณะนี้ผลิตภัณฑ์ได้รับการออกแบบโดยแผนกวิศวกรรมแล้ว</span><span class="sxs-lookup"><span data-stu-id="85f18-261">The product has now been designed by the Engineering department.</span></span> <span data-ttu-id="85f18-262">สำหรับตัวอย่างนี้ ผลิตภัณฑ์เป็นต้นแบบที่วิศวกรรมได้ออกแบบมาสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="85f18-262">For this example, the product is a prototype that engineering has designed for a customer.</span></span> <span data-ttu-id="85f18-263">เนื่องจากลูกค้าเป็นลูกค้าของนิติบุคคล *USMF* ต้องนำผลิตภัณฑ์ออกใช้ไปยังนิติบุคคลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="85f18-263">Because the customer is a customer of the *USMF* legal entity, the product must be released to that legal entity.</span></span>

1. <span data-ttu-id="85f18-264">รักษาการตั้งค่านิติบุคคลเป็น *DEMF*</span><span class="sxs-lookup"><span data-stu-id="85f18-264">Keep the legal entity set to *DEMF*.</span></span> <span data-ttu-id="85f18-265">(ใช้ตัวเลือกบริษัททางด้านขวาของแถบนำทางตามต้องการ)</span><span class="sxs-lookup"><span data-stu-id="85f18-265">(Use the company picker on the right side of the navigation bar as required.)</span></span>
1. <span data-ttu-id="85f18-266">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์ &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-266">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
1. <span data-ttu-id="85f18-267">เลือกผลิตภัณฑ์ *Z0001*</span><span class="sxs-lookup"><span data-stu-id="85f18-267">Select product *Z0001*.</span></span>
1. <span data-ttu-id="85f18-268">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **รักษา** ให้เลือก **นำโครงสร้างผลิตภัณฑ์ออกใช้** เพื่อเปิดวิซาร์ด **นำผลิตภัณฑ์ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-268">On the Action Pane, on the **Product** tab, in the **Maintain** group, select **Release product structure** to open the **Release products** wizard.</span></span>
1. <span data-ttu-id="85f18-269">บนหน้า **เลือกผลิตภัณฑ์วิศวกรรมที่จะนำออกใช้** ให้เลือกกล่องกาเครื่องหมาย **เลือก** สำหรับผลิตภัณฑ์ *Z0001*</span><span class="sxs-lookup"><span data-stu-id="85f18-269">On the **Select engineering products to release** page, select the **Select** check box for product *Z0001*.</span></span>

    <span data-ttu-id="85f18-270">![การเลือกผลิตภัณฑ์วิศวกรรมเพื่อนำออกใช้](media/select-eng-product-to-release.png "การเลือกผลิตภัณฑ์วิศวกรรมเพื่อนำออกใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-270">![Selecting the engineering products to release](media/select-eng-product-to-release.png "Selecting the engineering products to release")</span></span>

1. <span data-ttu-id="85f18-271">เลือก **รายละเอียดการนำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-271">Select **Release details**.</span></span>
1. <span data-ttu-id="85f18-272">หน้า **รายละเอียดของการนำผลิตภัณฑ์ออกใช้** จะปรากฏขึ้น ซึ่งคุณสามารถรีวิวรายละเอียดของผลิตภัณฑ์ที่จะนำออกใช้และโครงสร้างผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="85f18-272">The **Product release details** page appears, where you can review the details of the product that will be released, and its product structure.</span></span> <span data-ttu-id="85f18-273">โปรดทราบว่าตัวเลือก **ส่ง BOM** ถูกตั้งค่าเป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="85f18-273">Notice that the **Send BOM** option is set to *Yes*.</span></span> <span data-ttu-id="85f18-274">ดังนั้น จึงมีการนำผลิตภัณฑ์ *Z0001* ออกใช้ และรายการรองทั้งหมดจาก BOM จะถูกนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-274">Therefore, both product *Z0001* and all its child items from the BOM will be released.</span></span>

    <span data-ttu-id="85f18-275">คุณสามารถเลือกรายการรองใดก็ได้ในบานหน้าต่างด้านซ้ายเพื่อรีวิวรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="85f18-275">You can select any child item in the left pane to review its details.</span></span> <span data-ttu-id="85f18-276">ถ้ารายการรองใดๆ มี BOM คุณยังสามารถเลือกที่จะนำออกใช้ BOM ของรายการรองนั้นได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="85f18-276">If any child item has a BOM, you can also select to release the BOM of that child item.</span></span>

    <span data-ttu-id="85f18-277">![การตรวจทานรายละเอียดการนำผลิตภัณฑ์ออกใช้](media/product-release-details.png "การตรวจทานรายละเอียดการนำผลิตภัณฑ์ออกใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-277">![Reviewing the product release details](media/product-release-details.png "Reviewing the product release details")</span></span>

1. <span data-ttu-id="85f18-278">ปิดหน้าเพื่อกลับไปยังวิซาร์ด **นำผลิตภัณฑ์ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-278">Close the page to return to the **Release products** wizard.</span></span>
1. <span data-ttu-id="85f18-279">เลือก **ถัดไป** เพื่อเปิดหน้า **เลือกผลิตภัณฑ์ที่จะนำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-279">Select **Next** to open the **Select products to release** page.</span></span> <span data-ttu-id="85f18-280">ถ้าคุณได้เลือกผลิตภัณฑ์มาตรฐานใดๆ (ไม่ใช่วิศวกรรม) จะปรากฏขึ้นบนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="85f18-280">If you had selected any standard (non-engineering) products, they would appear on this page.</span></span> <span data-ttu-id="85f18-281">โปรดทราบว่าเมื่อคุณนำผลิตภัณฑ์มาตรฐานออกใช้โดยการเลือก **นำโครงสร้างผลิตภัณฑ์ออกใช้** BOM และกระบวนการผลิตจะถูกนำออกใช้ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="85f18-281">Note that when you release a standard product by selecting **Release product structure**, its BOM and route are also released.</span></span>

    <span data-ttu-id="85f18-282">![การเลือกผลิตภัณฑ์มาตรฐานเพื่อนำออกใช้](media/select-std-product-to-release.png "การเลือกผลิตภัณฑ์มาตรฐานเพื่อนำออกใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-282">![Selecting the standard products to release](media/select-std-product-to-release.png "Selecting the standard products to release")</span></span>

1. <span data-ttu-id="85f18-283">เลือก **ถัดไป** เพื่อเปิดหน้า **เลือกผลิตภัณฑ์ย่อยที่จะนำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-283">Select **Next** to open the **Select product variants to release** page.</span></span> <span data-ttu-id="85f18-284">สำหรับตัวอย่างนี้ ไม่มีตัวแปรใดๆ</span><span class="sxs-lookup"><span data-stu-id="85f18-284">For this example, there aren't any variants.</span></span>
1. <span data-ttu-id="85f18-285">เลือก **ถัดไป** เพื่อเปิดหน้า **เลือกบริษัท**</span><span class="sxs-lookup"><span data-stu-id="85f18-285">Select **Next** to open the **Select companies** page.</span></span>
1. <span data-ttu-id="85f18-286">เลือกบริษัทที่ผลิตภัณฑ์ควรถูกนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-286">Select the companies that the product should be released to.</span></span> <span data-ttu-id="85f18-287">สำหรับตัวอย่างนี้ ให้เลือกกล่องกาเครื่องหมายสำหรับ **USMF**</span><span class="sxs-lookup"><span data-stu-id="85f18-287">For this example, select the check box for **USMF**.</span></span>

    <span data-ttu-id="85f18-288">![การเลือกบริษัทที่จะนำออกใช้](media/select-release-companies.png "การเลือกบริษัทที่จะนำออกใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-288">![Selecting the companies to release to](media/select-release-companies.png "Selecting the companies to release to")</span></span>

1. <span data-ttu-id="85f18-289">เลือก **ถัดไป** เพื่อเปิดหน้า **ยืนยันการเลือก**</span><span class="sxs-lookup"><span data-stu-id="85f18-289">Select **Next** to open the **Confirm selection** page.</span></span>
1. <span data-ttu-id="85f18-290">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="85f18-290">Select **Finish**.</span></span>

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a><span data-ttu-id="85f18-291">รีวิวและยอมรับผลิตภัณฑ์ ก่อนที่คุณจะนำออกใช้ในบริษัทเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="85f18-291">Review and accept the product before you release it in the local company</span></span>

<span data-ttu-id="85f18-292">ปัจจุบันแผนกวิศวกรรมได้เผยแพร่ข้อมูลไปยังบริษัทเฉพาะที่ซึ่งผลิตภัณฑ์จะถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-292">The Engineering department has now released the information to the local companies where the product will be used.</span></span> <span data-ttu-id="85f18-293">สำหรับตัวอย่างนี้ บริษัทเฉพาะที่คือ *USMF*</span><span class="sxs-lookup"><span data-stu-id="85f18-293">For this example, the local company is *USMF*.</span></span>

<span data-ttu-id="85f18-294">เนื่องจากคุณตั้งค่าฟิลด์ **การยอมรับผลิตภัณฑ์** เป็น *ด้วยตนเอง* ในหน้า **พารามิเตอร์การจัดการการเปลี่ยนแปลงทางวิศวกรรม** สำหรับบริษัท *USMF* ต้องมีการยอมรับผลิตภัณฑ์ด้วยตนเอง ก่อนที่จะนำออกใช้กับบริษัทนั้น</span><span class="sxs-lookup"><span data-stu-id="85f18-294">Because you set the **Product acceptance** field to *Manual* on the **Engineering change management parameters** page for the *USMF* company, products must be manually accepted before they are released to that company.</span></span> <span data-ttu-id="85f18-295">กล่าวอีกอย่างหนึ่งคือ ต้องมีการทบทวนและยอมรับก่อนที่จะกลายเป็นผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-295">In other words, they must be reviewed and accepted before they become released products.</span></span>

<span data-ttu-id="85f18-296">เมื่อต้องการรีวิวผลิตภัณฑ์และนำออกใช้ในบริษัท *USMF* ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="85f18-296">To review the product and release it in the *USMF* company, follow these steps.</span></span>

1. <span data-ttu-id="85f18-297">ตั้งค่านิติบุคคลเป็น *USMF*</span><span class="sxs-lookup"><span data-stu-id="85f18-297">Set the legal entity to *USMF*.</span></span> <span data-ttu-id="85f18-298">(ใช้ตัวเลือกบริษัททางด้านขวาของแถบนำทาง)</span><span class="sxs-lookup"><span data-stu-id="85f18-298">(Use the company picker on the right side of the navigation bar.)</span></span>
1. <span data-ttu-id="85f18-299">ไปที่ **การจัดการการเปลี่ยนแปลงทางวิศวกรรม &gt; ทั่วไป &gt; การนำผลิตภัณฑ์ออกใช้ &gt; เปิดการนำผลิตภัณฑ์ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-299">Go to **Engineering change management &gt; Common &gt; Product releases &gt; Open product releases**.</span></span>

    <span data-ttu-id="85f18-300">หน้า **เปิดการนำผลิตภัณฑ์ออกใช้** แสดงผลิตภัณฑ์ *Z0001* ซึ่งมีสถานะเป็น *การยอมรับที่ค้างอยู่*</span><span class="sxs-lookup"><span data-stu-id="85f18-300">The **Open product releases** page shows product *Z0001*, which has a status of *Pending acceptance*.</span></span>

    <span data-ttu-id="85f18-301">![เปิดการนำผลิตภัณฑ์ออกใช้](media/open-product-releases.png "เปิดการนำผลิตภัณฑ์ออกใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-301">![Open product releases](media/open-product-releases.png "Open product releases")</span></span>

1. <span data-ttu-id="85f18-302">เลือกค่าในคอลัมน์ **หมายเลขผลิตภัณฑ์** เพื่อเปิดหน้า **รายละเอียดการนำผลิตภัณฑ์ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-302">Select the value in the **Product number** column to open the **Product release details** page.</span></span> <span data-ttu-id="85f18-303">โปรดสังเกตรายละเอียดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-303">Notice the following details:</span></span>

    - <span data-ttu-id="85f18-304">FastTab **ทั่วไป** จะแสดงข้อมูลเกี่ยวกับการนำผลิตภัณฑ์ออกใช้ เช่น บริษัทที่นำออกใช้ (*DEMF* สำหรับตัวอย่างนี้) ไซต์ที่นำออกใช้ (*1*) และไซต์ที่รับสินค้า (*1*)</span><span class="sxs-lookup"><span data-stu-id="85f18-304">The **General** FastTab shows information about the product release, such as the releasing company (*DEMF* for this example), the releasing site (*1*), and the receiving site (*1*).</span></span> <span data-ttu-id="85f18-305">เนื่องจากคุณไม่ได้ระบุไซต์ที่รับสินค้าในวิซาร์ด **ผลิตภัณฑ์ที่นำออกใช้** จะมีการคัดลอกค่าไซต์ที่นำออกใช้ไปยังไซต์ที่รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="85f18-305">Because you didn't specify a receiving site in the **Release products** wizard, the the releasing site value is copied to the receiving site.</span></span>
    - <span data-ttu-id="85f18-306">FastTab **รายละเอียดการนำออกใช้** แสดงข้อมูลเกี่ยวกับผลิตภัณฑ์และรุ่นที่มีการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-306">The **Release details** FastTab shows information about the product and the version that was released.</span></span> <span data-ttu-id="85f18-307">ที่นี่ คุณสามารถปรับเปลี่ยนการตั้งค่าต่างๆ เช่น วันที่มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-307">Here, you can modify settings such as the effectivity dates.</span></span>
    - <span data-ttu-id="85f18-308">FastTab **กระบวนการผลิต** จะแสดงกระบวนการผลิตของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="85f18-308">The **Route** FastTab shows the route of the product.</span></span> <span data-ttu-id="85f18-309">อย่างไรก็ตาม สำหรับตัวอย่างนี้ คุณไม่ได้นำเส้นทางใดๆ ออกใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-309">However, for this example, you didn't release any routes.</span></span>

    <span data-ttu-id="85f18-310">![รายละเอียดการนำผลิตภัณฑ์ออกใช้](media/product-release-details-2.png "รายละเอียดการนำผลิตภัณฑ์ออกใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-310">![Product release details](media/product-release-details-2.png "Product release details")</span></span>

1. <span data-ttu-id="85f18-311">เมื่อคุณทำการตรวจทานข้อมูลเสร็จเรียบร้อยแล้ว คุณพร้อมที่จะยอมรับผลิตภัณฑ์ดังกล่าว และในลักษณะนี้ ให้นำออกใช้ในบริษัท *USMF*</span><span class="sxs-lookup"><span data-stu-id="85f18-311">When you've finished reviewing the information, you're ready to accept the product and, in this way, release it in the *USMF* company.</span></span> <span data-ttu-id="85f18-312">ในบานหน้าต่างการดำเนินการ เลือก **ยอมรับ &gt; ยอมรับ**</span><span class="sxs-lookup"><span data-stu-id="85f18-312">On the Action Pane, select **Actions &gt; Accept**.</span></span>
1. <span data-ttu-id="85f18-313">ขณะนี้มีการนำออกใช้ผลิตภัณฑ์ในบริษัท *USMF*</span><span class="sxs-lookup"><span data-stu-id="85f18-313">The product is now released in the *USMF* company.</span></span> <span data-ttu-id="85f18-314">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์ &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-314">Go to **Product information management &gt;Products &gt; Released products**.</span></span> <span data-ttu-id="85f18-315">คุณควรเห็นสินค้า *Z0001*</span><span class="sxs-lookup"><span data-stu-id="85f18-315">You should see item *Z0001*.</span></span>

## <a name="use-the-product-in-transactions-in-the-local-company"></a><span data-ttu-id="85f18-316">ใช้ผลิตภัณฑ์ในธุรกรรมในบริษัทเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="85f18-316">Use the product in transactions in the local company</span></span>

<span data-ttu-id="85f18-317">ผู้จัดการข้อมูลหลักสำหรับบริษัท *USMF* ต้องการตรวจสอบให้แน่ใจว่าผลิตภัณฑ์อยู่ในสถานะ *ต้นแบบ* เพื่อให้แน่ใจว่าผู้ใช้จะได้รับการแจ้งเตือน ถ้าพวกเขาเพิ่มไปยังกระบวนการที่พวกเขากำลังทำงานอยู่โดยไม่ได้ตั้งใจ</span><span class="sxs-lookup"><span data-stu-id="85f18-317">The master data manager for the *USMF* company wants to make sure that the product is in a *Prototype* state, to ensure that users will be warned if they accidentally add it to processes that they are working on.</span></span>

1. <span data-ttu-id="85f18-318">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์ &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-318">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
1. <span data-ttu-id="85f18-319">เลือกผลิตภัณฑ์ *Z0001* เพื่อเปิดหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="85f18-319">Select product *Z0001* to open its details page.</span></span> <span data-ttu-id="85f18-320">(คุณสามารถใช้ตัวกรองเพื่อค้นหาผลิตภัณฑ์)</span><span class="sxs-lookup"><span data-stu-id="85f18-320">(You can use the filter to find the product.)</span></span>
1. <span data-ttu-id="85f18-321">บนบานหน้าต่างการดำเนินการ บนแท็บ **วิศวกร** ในกลุ่ม **การจัดการการเปลี่ยนแปลงทางวิศวกรรม** ให้เลือก **รุ่นวิศวกรรม**</span><span class="sxs-lookup"><span data-stu-id="85f18-321">On the Action Pane, on the **Engineer** tab, in the **Engineering change management** group, select **Engineering versions**.</span></span>
1. <span data-ttu-id="85f18-322">บนหน้า **รุ่นวิศวกรรม** ให้เลือกหมายเลขรุ่น *V-01* เพื่อเปิดหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="85f18-322">On the **Engineering versions** page, select version number *V-01* to open its details page.</span></span>
1. <span data-ttu-id="85f18-323">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **สถานะของวงจรการใช้** ให้เลือก **เปลี่ยนสถานะของวงจรการใช้**</span><span class="sxs-lookup"><span data-stu-id="85f18-323">On the Action Pane, on the **Product** tab, in the **Lifecycle state** group, select **Change lifecycle state**.</span></span>
1. <span data-ttu-id="85f18-324">ในกล่องโต้ตอบของรายการแบบหล่นลง **เปลี่ยนสถานะของวงจรการใช้** ให้ตั้งค่าฟิลด์ **สถานะ** เป็น *ต้นแบบ* แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="85f18-324">In the **Change lifecycle state** drop-down dialog box, set the **State** field to *Prototype*, and then select **OK**.</span></span>

    <span data-ttu-id="85f18-325">![การเปลี่ยนสถานะของวงจรการใช้](media/change-lifecycle-state.png "การเปลี่ยนสถานะของวงจรการใช้")</span><span class="sxs-lookup"><span data-stu-id="85f18-325">![Changing the lifecycle state](media/change-lifecycle-state.png "Changing the lifecycle state")</span></span>

## <a name="add-the-engineering-product-to-a-sales-order"></a><span data-ttu-id="85f18-326">เพิ่มผลิตภัณฑ์วิศวกรรมลงในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="85f18-326">Add the engineering product to a sales order</span></span>

<span data-ttu-id="85f18-327">ขณะนี้สามารถขายผลิตภัณฑ์ให้กับลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="85f18-327">The product can now be sold to a customer.</span></span> <span data-ttu-id="85f18-328">ในการเพิ่มผลิตภัณฑ์ลงในใบสั่งขาย ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="85f18-328">To add the product to a sales order, follow these steps.</span></span>

1. <span data-ttu-id="85f18-329">ไปยัง **การขายและการตลาด &gt; ใบสั่งขาย &gt; ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="85f18-329">Go to **Sales and marketing &gt; Sales orders &gt; All sales orders**.</span></span>
1. <span data-ttu-id="85f18-330">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="85f18-330">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="85f18-331">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-0002* และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="85f18-331">In the **Create sales order** dialog box, set the **Customer account** field to *US-0002*, and then select **OK**.</span></span>
1. <span data-ttu-id="85f18-332">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="85f18-332">The new sales order is opened.</span></span> <span data-ttu-id="85f18-333">บน FastTab **บรรทัดใบสั่งขาย** ให้เพิ่มแถว และตั้งค่าฟิลด์ **หมายเลขสินค้า** เป็น *Z000* สำหรับบรรทัดใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="85f18-333">On the **Sales order lines** FastTab, add a row, and set the **Item number** field to *Z000* for it.</span></span>
1. <span data-ttu-id="85f18-334">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="85f18-334">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="85f18-335">คุณได้รับข้อความแจ้งเตือนที่แจ้งให้คุณทราบว่าสินค้ามีสถานะเป็น *ต้นแบบ*</span><span class="sxs-lookup"><span data-stu-id="85f18-335">You receive a warning message that informs you that the item has a status of *Prototype*.</span></span> <span data-ttu-id="85f18-336">อย่างไรก็ตาม เนื่องจากข้อความเป็นเพียงคำเตือน ใบสั่งขายยังคงถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="85f18-336">However, because the message is just a warning, the sales order was still created.</span></span>

    <span data-ttu-id="85f18-337">![ใบสั่งขายสำหรับผลิตภัณฑ์วิศวกรรม](media/sales-order-eng-product.png "ใบสั่งขายสำหรับผลิตภัณฑ์วิศวกรรม")</span><span class="sxs-lookup"><span data-stu-id="85f18-337">![Sales order for an engineering product](media/sales-order-eng-product.png "Sales order for an engineering product")</span></span>

## <a name="request-changes-in-the-engineering-product"></a><span data-ttu-id="85f18-338">ร้องขอการเปลี่ยนแปลงในผลิตภัณฑ์วิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-338">Request changes in the engineering product</span></span>

<span data-ttu-id="85f18-339">ผลิตภัณฑ์ถูกส่งไปยังลูกค้า แต่ลูกค้าไม่ได้รับความพึงพอใจอย่างสมบูรณ์ และให้ผลป้อนกลับที่มีคำแนะนำสำหรับการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="85f18-339">The product was sent to a customer, but the customer wasn't completely satisfied and provides feedback that includes suggestions for improvement.</span></span> <span data-ttu-id="85f18-340">ในขณะที่ลูกค้ากำลังพูดกับพนักงานขายทางโทรศัพท์ พนักงานขายสามารถร้องขอการเปลี่ยนแปลงที่ลูกค้ากำลังบรรยายได้</span><span class="sxs-lookup"><span data-stu-id="85f18-340">While the customer is speaking with a sales clerk on the phone, the sales clerk can request the changes that the customer is describing.</span></span>

1. <span data-ttu-id="85f18-341">ไปยัง **การขายและการตลาด &gt; ใบสั่งขาย &gt; ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="85f18-341">Go to **Sales and marketing &gt; Sales orders &gt; All sales orders**.</span></span>
1. <span data-ttu-id="85f18-342">ค้นหาและเปิดใบสั่งขายที่คุณสร้างขึ้นในแบบฝึกหัดก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="85f18-342">Find and open the sales order that you created in the previous exercise.</span></span>
1. <span data-ttu-id="85f18-343">บน FastTab **ใบสั่งขาย** ให้เลือก **การจัดการการเปลี่ยนแปลงทางวิศวกรรม &gt; คำขอเปลี่ยนแปลงทางวิศวกรรมใหม่**</span><span class="sxs-lookup"><span data-stu-id="85f18-343">On the **Sales order lines** FastTab, select **Engineering change management &gt; New engineering change request**.</span></span>

    <span data-ttu-id="85f18-344">![การสร้างคำขอเปลี่ยนแปลงทางวิศวกรรมจากใบสั่งขาย](media/sales-order-eng-change-request.png "การสร้างคำขอเปลี่ยนแปลงทางวิศวกรรมจากใบสั่งขาย")</span><span class="sxs-lookup"><span data-stu-id="85f18-344">![Creating an engineering change request from a sales order](media/sales-order-eng-change-request.png "Creating an engineering change request from a sales order")</span></span>

1. <span data-ttu-id="85f18-345">กรอกข้อมูลคำขอเปลี่ยนแปลงทางวิศวกรรมตามผลป้อนกลับของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="85f18-345">Fill in the engineering change request, based on the customer's feedback.</span></span> <span data-ttu-id="85f18-346">สำหรับตัวอย่างนี้ ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-346">For this example, set the following values:</span></span>

    - <span data-ttu-id="85f18-347">**คำขอเปลี่ยนแปลง:** *555*</span><span class="sxs-lookup"><span data-stu-id="85f18-347">**Change request:** *555*</span></span>
    - <span data-ttu-id="85f18-348">**ชื่อ:** *Z0001 การเปลี่ยนแปลงของลูกค้า*</span><span class="sxs-lookup"><span data-stu-id="85f18-348">**Title:** *Z0001 customer change*</span></span>
    - <span data-ttu-id="85f18-349">**ระดับความสำคัญ:** *ต่ำ*</span><span class="sxs-lookup"><span data-stu-id="85f18-349">**Priority:** *low*</span></span>
    - <span data-ttu-id="85f18-350">**ประเภท:** ตั้งค่าการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="85f18-350">**Category:** set change</span></span>
    - <span data-ttu-id="85f18-351">**ความรุนแรง:** *ปานกลาง*</span><span class="sxs-lookup"><span data-stu-id="85f18-351">**Severity:** *Medium*</span></span>

1. <span data-ttu-id="85f18-352">บน FastTab **ข้อมูล** ให้เลือก **สร้าง &gt; บันทึกย่อ** เพื่อเพิ่มบันทึกย่อไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="85f18-352">On the **Information** FastTab, select **New &gt; Note** to add a note to the grid.</span></span>
1. <span data-ttu-id="85f18-353">ในฟิลด์ **คำอธิบาย** สำหรับบันทึกย่อใหม่ ให้บ่งชี้ว่าสินค้า *D0003* ควรถูกลบออกจาก BOM หรือไม่</span><span class="sxs-lookup"><span data-stu-id="85f18-353">In the **Description** field for the new note, indicate that item *D0003* should be deleted from the BOM.</span></span> <span data-ttu-id="85f18-354">ถ้าคุณต้องการเพิ่มข้อมูลเพิ่มเติมสำหรับบันทึกย่อนี้ คุณสามารถป้อนข้อความในฟิลด์ **บันทึกย่อ**</span><span class="sxs-lookup"><span data-stu-id="85f18-354">If you must add more information for the note, you can enter text in the **Notes** field.</span></span>

    <span data-ttu-id="85f18-355">![คำขอเปลี่ยนแปลงทางวิศวกรรม](media/eng-change-request.png "คำขอเปลี่ยนแปลงทางวิศวกรรม")</span><span class="sxs-lookup"><span data-stu-id="85f18-355">![Engineering change request](media/eng-change-request.png "Engineering change request")</span></span>

1. <span data-ttu-id="85f18-356">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="85f18-356">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f18-357">โปรดสังเกตว่าสินค้าได้ถูกเพิ่มโดยอัตโนมัติบน FastTab **ผลิตภัณฑ์** และจะมีการเพิ่มแหล่งที่มาของคำขอเปลี่ยนแปลงทางวิศวกรรม (ใบสั่งขาย) บน FastTab **แหล่งที่มา**</span><span class="sxs-lookup"><span data-stu-id="85f18-357">Notice that the item has automatically been added on the **Products** FastTab, and that the source of the engineering change request (the sales order) has been added on the **Source** FastTab.</span></span>

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a><span data-ttu-id="85f18-358">ทำการเปลี่ยนแปลงไปยังผลิตภัณฑ์โดยใช้ใบสั่งเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-358">Make changes to the product by using an engineering change order</span></span>

<span data-ttu-id="85f18-359">พนักงานขายรู้ว่าผลิตภัณฑ์มีความสำคัญและได้รับการออกแบบโดยเฉพาะสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="85f18-359">The sales clerk knows that the product is important and was designed especially for the customer.</span></span> <span data-ttu-id="85f18-360">ดังนั้น พนักงานขายจึงเรียกวิศวกรในบริษัท *DEMF* เพื่อแจ้งให้ทราบเกี่ยวกับคำขอเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="85f18-360">Therefore, the sales clerk calls an engineer in the *DEMF* company to notify them about the change request.</span></span> <span data-ttu-id="85f18-361">ด้วยวิธีนี้ วิศวกรจึงสามารถทำให้กระบวนการทำงานรวดเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="85f18-361">In this way, the engineer can speed up the process.</span></span>

<span data-ttu-id="85f18-362">ขณะนี้วิศวกรตรวจสอบคำขอจากลูกค้า และสร้างใบสั่งเปลี่ยนแปลงสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="85f18-362">The engineer now reviews the request from the customer and creates a change order for the product.</span></span>

1. <span data-ttu-id="85f18-363">เนื่องจากวิศวกรทำงานในบริษัท *DEMF* ให้ตั้งค่านิติบุคคลเป็น *DEMF*</span><span class="sxs-lookup"><span data-stu-id="85f18-363">Because the engineer works in the *DEMF* company, set the legal entity to *DEMF*.</span></span> <span data-ttu-id="85f18-364">(ใช้ตัวเลือกบริษัททางด้านขวาของแถบนำทาง)</span><span class="sxs-lookup"><span data-stu-id="85f18-364">(Use the company picker on the right side of the navigation bar.)</span></span>
1. <span data-ttu-id="85f18-365">ให้ไปที่ **การจัดการการเปลี่ยนแปลงทางวิศวกรรม &gt; ทั่วไป &gt; คำขอเปลี่ยนแปลงทางวิศวกรรม**</span><span class="sxs-lookup"><span data-stu-id="85f18-365">Go to **Engineering change management &gt; Common &gt; Engineering change requests**.</span></span>
1. <span data-ttu-id="85f18-366">เปิดคำขอเปลี่ยนแปลง *555*</span><span class="sxs-lookup"><span data-stu-id="85f18-366">Open change request *555*.</span></span>
1. <span data-ttu-id="85f18-367">รีวิวข้อมูล แล้วจากนั้น อนุมัติการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="85f18-367">Review the information, and then approve the change.</span></span> <span data-ttu-id="85f18-368">บนบานหน้าต่างการดำเนินการ บนแท็บ **คำขอเปลี่ยนแปลง** ในกลุ่ม **สถานะการเปลี่ยนแปลง** ให้เลือก **อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="85f18-368">On the Action Pane, on the **Change request** tab, in the **Change status** group, select **Approve**.</span></span>
1. <span data-ttu-id="85f18-369">ให้ไปที่ **การจัดการการเปลี่ยนแปลงทางวิศวกรรม &gt; ทั่วไป &gt; ใบสั่งเปลี่ยนแปลงทางวิศวกรรม**</span><span class="sxs-lookup"><span data-stu-id="85f18-369">Go to **Engineering change management &gt; Common &gt; Engineering change orders**.</span></span>
1. <span data-ttu-id="85f18-370">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างใบสั่งเปลี่ยนแปลง และตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-370">On the Action Pane, select **New** to create a change order, and set the following values for it:</span></span>

    - <span data-ttu-id="85f18-371">**ใบสั่งเปลี่ยนแปลง:** *555*</span><span class="sxs-lookup"><span data-stu-id="85f18-371">**Change order:** *555*</span></span>
    - <span data-ttu-id="85f18-372">**ชื่อ:** *Z0001 การเปลี่ยนแปลงของลูกค้า*</span><span class="sxs-lookup"><span data-stu-id="85f18-372">**Title:** *Z0001 customer change*</span></span>
    - <span data-ttu-id="85f18-373">**ประเภท:** *การเปลี่ยนแปลงของลูกค้า*</span><span class="sxs-lookup"><span data-stu-id="85f18-373">**Category:** *Customer change*</span></span>
    - <span data-ttu-id="85f18-374">**ระดับความสำคัญ:** *ต่ำ*</span><span class="sxs-lookup"><span data-stu-id="85f18-374">**Priority:** *Low*</span></span>
    - <span data-ttu-id="85f18-375">**ความรุนแรง:** *ปานกลาง*</span><span class="sxs-lookup"><span data-stu-id="85f18-375">**Severity:** *Medium*</span></span>

1. <span data-ttu-id="85f18-376">บน FastTab **ผลิตภัณฑ์ที่ได้รับผลกระทบ** ให้เลือก **สร้าง &gt; เพิ่มผลิตภัณฑ์ที่มีอยู่** เพื่อเพิ่มแถวไปยังกริด แล้วตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85f18-376">On the **Impacted products** FastTab, select **New &gt; Add existing product** to add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="85f18-377">**ผลิตภัณฑ์:** *Z0001*</span><span class="sxs-lookup"><span data-stu-id="85f18-377">**Product:** *Z0001*</span></span>
    - <span data-ttu-id="85f18-378">**ผลกระทบ:** *รุ่นใหม่*</span><span class="sxs-lookup"><span data-stu-id="85f18-378">**Impact:** *New version*</span></span>

    <span data-ttu-id="85f18-379">![การสร้างใบสั่งเปลี่ยนแปลงทางวิศวกรรม](media/eng-change-order.png "การสร้างใบสั่งเปลี่ยนแปลงทางวิศวกรรม")</span><span class="sxs-lookup"><span data-stu-id="85f18-379">![Creating an engineering change order](media/eng-change-order.png "Creating an engineering change order")</span></span>

1. <span data-ttu-id="85f18-380">โปรดสังเกตว่า เนื่องจากคุณตั้งค่าฟิลด์ **ผลกระทบ** เป็น *รุ่นใหม่* ฟิลด์ **รุ่นใหม่** บนแท็บ **รายละเอียด** ของ FastTab **รายละเอียดของผลิตภัณฑ์** จะแสดงว่าหมายเลขรุ่นใหม่จะเป็น (*V-02* สำหรับตัวอย่างนี้)</span><span class="sxs-lookup"><span data-stu-id="85f18-380">Notice that, because you set the **Impact** field to *New version*, the **New version** field on the **Details** tab of the **Product details** FastTab shows what the new version number will be (*V-02* for this example).</span></span>

    <span data-ttu-id="85f18-381">![รายละเอียดของผลิตภัณฑ์สำหรับใบสั่งเปลี่ยนแปลงทางวิศวกรรม](media/eng-change-order-product-details.png "รายละเอียดของผลิตภัณฑ์สำหรับใบสั่งเปลี่ยนแปลงทางวิศวกรรม")</span><span class="sxs-lookup"><span data-stu-id="85f18-381">![Product details for an engineering change order](media/eng-change-order-product-details.png "Product details for an engineering change order")</span></span>

1. <span data-ttu-id="85f18-382">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="85f18-382">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="85f18-383">บน FastTab **รายละเอียดของผลิตภัณฑ์** บนแท็บ **สูตรการผลิต** ให้เลือก **บรรทัด** ที่จะเปิด BOM สำหรับรุ่น *V-01* ของผลิตภัณฑ์ *Z0001*</span><span class="sxs-lookup"><span data-stu-id="85f18-383">On the **Product details** FastTab, on the **Bill of material** tab, select **Lines** to open the BOM for version *V-01* of product *Z0001*.</span></span>

    <span data-ttu-id="85f18-384">![บรรทัด BOM ของผลิตภัณฑ์วิศวกรรม](media/eng-product-bom-lines.png "บรรทัด BOM ของผลิตภัณฑ์วิศวกรรม")</span><span class="sxs-lookup"><span data-stu-id="85f18-384">![Engineering product BOM lines](media/eng-product-bom-lines.png "Engineering product BOM lines")</span></span>

1. <span data-ttu-id="85f18-385">เลือกบรรทัดสำหรับหมายเลขสินค้า *D0003* และจากนั้น ในบานหน้าต่างการดำเนินการ ให้เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="85f18-385">Select the line for item number *D0003*, and then, on the Action Pane, select **Delete**.</span></span> <span data-ttu-id="85f18-386">ค่าของ **ฟิลด์ชนิดการเปลี่ยนแปลง** สำหรับบรรทัดนี้เปลี่ยนเป็น *ลบ*</span><span class="sxs-lookup"><span data-stu-id="85f18-386">The value of the **Change type** field for this line changes to *Deleted*.</span></span>
1. <span data-ttu-id="85f18-387">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="85f18-387">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="85f18-388">![บรรทัด BOM ของผลิตภัณฑ์วิศวกรรมที่ปรับเปลี่ยน](media/eng-product-bom-lines-modified.png "บรรทัด BOM ของผลิตภัณฑ์วิศวกรรมที่ปรับเปลี่ยน")</span><span class="sxs-lookup"><span data-stu-id="85f18-388">![Modified engineering product BOM lines](media/eng-product-bom-lines-modified.png "Modified engineering product BOM lines")</span></span>

1. <span data-ttu-id="85f18-389">ปิดหน้า **บรรทัด BOM** เพื่อกลับไปที่หน้า **ใบสั่งเปลี่ยนแปลงทางวิศวกรรม**</span><span class="sxs-lookup"><span data-stu-id="85f18-389">Close the **BOM line** page to return to the **Engineering change order** page.</span></span>
1. <span data-ttu-id="85f18-390">บน FastTab **รายละเอียดผลิตภัณฑ์** บนแท็บ **สูตรการผลิต** ให้สังเกตว่าค่าของฟิลด์ **ชนิดการเปลี่ยนแปลง** สำหรับ BOM *Z0001* มีการ *เปลี่ยนแปลง* ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="85f18-390">On the **Product details** FastTab, on the **Bill of material** tab, notice that the value of the **Change type** field for BOM *Z0001* is now *Changed*.</span></span>

    <span data-ttu-id="85f18-391">![ใบสั่งเปลี่ยนแปลงทางวิศวกรรมที่มี BOM ที่เปลี่ยนไป](media/eng-change-order-changed-bom.png "ใบสั่งเปลี่ยนแปลงทางวิศวกรรมที่มี BOM ที่เปลี่ยนไป")</span><span class="sxs-lookup"><span data-stu-id="85f18-391">![Engineering change order that includes a changed BOM](media/eng-change-order-changed-bom.png "Engineering change order that includes a changed BOM")</span></span>

    <span data-ttu-id="85f18-392">ขณะนี้ต้องมีการอนุมัติใบสั่ง ก่อนที่จะสามารถประมวลผลการเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="85f18-392">The order must now be approved before the changes can be processed.</span></span> <span data-ttu-id="85f18-393">เมื่อมีการประมวลผลการเปลี่ยนแปลง จะมีการอัปเดตผลิตภัณฑ์โดยมีการเปลี่ยนแปลงที่รวมอยู่ในใบสั่งเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="85f18-393">When the changes are processed, the products are updated with the changes that are included in the engineering change order.</span></span> <span data-ttu-id="85f18-394">สำหรับตัวอย่างนี้ ผู้ที่สร้างใบสั่งเปลี่ยนแปลงทางวิศวกรรมถูกระบุเป็นผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="85f18-394">For this example, the person who creates the engineering change order has been specified as the approver.</span></span>

1. <span data-ttu-id="85f18-395">บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งเปลี่ยนแปลง** ในกลุ่ม **สถานะการเปลี่ยนแปลง** ให้เลือก **อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="85f18-395">On the Action Pane, on the **Change order** tab, in the **Change status** group, select **Approve**.</span></span>
1. <span data-ttu-id="85f18-396">เลือก **กระบวนการ** เพื่ออัปเดตข้อมูลของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="85f18-396">Select **Process** to update the product's information.</span></span>
1. <span data-ttu-id="85f18-397">เลือก **เสร็จสมบูรณ์** เพื่อทำเครื่องหมายใบสั่งเปลี่ยนแปลงเป็นเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="85f18-397">Select **Complete** to mark the change order as completed.</span></span>

## <a name="release-the-changed-product"></a><span data-ttu-id="85f18-398">นำผลิตภัณฑ์ที่เปลี่ยนแปลงออกใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-398">Release the changed product</span></span>

<span data-ttu-id="85f18-399">ขณะนี้สามารถนำผลิตภัณฑ์ออกใช้อีกครั้งไปยังบริษัท *USMF*  แล้วจากนั้น ส่งไปให้ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="85f18-399">The product can now be released again to the *USMF* company and then sent to the customer.</span></span> <span data-ttu-id="85f18-400">เมื่อต้องการนำผลิตภัณฑ์ออกใช้โดยตรงจากใบสั่งเปลี่ยนแปลงทางวิศวกรรม ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="85f18-400">To release the product directly from the engineering change order, follow these steps.</span></span>

1. <span data-ttu-id="85f18-401">เปิดใบสั่งเปลี่ยนแปลงทางวิศวกรรมที่คุณสร้างขึ้นในแบบฝึกหัดก่อนหน้านี้ ถ้าไม่ได้เปิดอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="85f18-401">Open the engineering change order that you created in the previous exercise, if it isn't already open.</span></span>
1. <span data-ttu-id="85f18-402">บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งเปลี่ยนแปลง** ในกลุ่ม **การนำผลิตภัณฑ์ออกใช้** ให้เลือก **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="85f18-402">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **Search**.</span></span>
1. <span data-ttu-id="85f18-403">ผลการค้นหาจะแสดงว่าบริษัทใดที่มีการนำผลิตภัณฑ์ที่ได้รับผลกระทบออกใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-403">The search results show which companies the affected products have been released to.</span></span> <span data-ttu-id="85f18-404">ปิดผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="85f18-404">Close the search results.</span></span>
1. <span data-ttu-id="85f18-405">บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งเปลี่ยนแปลง** ในกลุ่ม **การนำผลิตภัณฑ์ออกใช้** ให้เลือก **มุมมอง** เพื่อเปิดกล่องโต้ตอบ **การนำออกใช้** ซึ่งคุณสามารถดูผลลัพธ์ของการค้นหาก่อนหน้านี้ได้</span><span class="sxs-lookup"><span data-stu-id="85f18-405">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **View** to open the **Releases** dialog box, where you can view the results of the previous search.</span></span>
1. <span data-ttu-id="85f18-406">เลือกแต่ละบริษัทที่คุณต้องการนำผลิตภัณฑ์ออกใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-406">Select each company that you want to release products to.</span></span>
1. <span data-ttu-id="85f18-407">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **การนำออกใช้** และกลับไปยังใบสั่งเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="85f18-407">Select **OK** to close the **Releases** dialog box and return to the change order.</span></span>
1. <span data-ttu-id="85f18-408">บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งเปลี่ยนแปลง** ในกลุ่ม **การนำผลิตภัณฑ์ออกใช้** ให้เลือก **กระบวนการ** เพื่อนำผลิตภัณฑ์ที่ได้รับผลกระทบออกใช้ไปยังบริษัทที่เลือก</span><span class="sxs-lookup"><span data-stu-id="85f18-408">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **Process** to release the affected products to the selected companies.</span></span> <span data-ttu-id="85f18-409">อีกทางหนึ่งคือ เลือก **นำโครงสร้างผลิตภัณฑ์ออกใช้** เพื่อเริ่มต้นกระบวนการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="85f18-409">Alternatively, select **Release product structure** to start the release process.</span></span>
