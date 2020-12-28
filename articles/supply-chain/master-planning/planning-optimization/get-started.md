---
title: เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน
description: หัวข้อนี้อธิบายวิธีการเริ่มใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/29/2020
ms.locfileid: "4438929"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="ca6af-103">เริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca6af-104">จากที่ [มีการประกาศก่อนหน้านี้](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) การเพิ่มประสิทธิภาพการวางแผนจะถูกจัดกำหนดการให้แทนที่กลไกจัดการการวางแผนหลักที่มีอยู่แล้วภายใน</span><span class="sxs-lookup"><span data-stu-id="ca6af-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="ca6af-105">ถ้าคุณใช้กลไกจัดการการวางแผนหลักในตัวในขณะนี้ คุณควรเริ่มต้นการวางแผนการย้ายของคุณสำหรับการเพิ่มประสิทธิภาพการวางแผนเดี๋ยวนี้</span><span class="sxs-lookup"><span data-stu-id="ca6af-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="ca6af-106">จำเป็นต้องเริ่มกระบวนการย้ายทันที เนื่องจากการดำเนินงานของคุณอาจได้รับผลกระทบเมื่อมีการบังคับใช้การยกเลิกการใช้</span><span class="sxs-lookup"><span data-stu-id="ca6af-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="ca6af-107">ในการหลีกเลี่ยงปัญหาในนาทีสุดท้าย เมื่อบังคับใช้ การยกเลิกการใช้ เราขอแนะนำให้คุณดำเนินการย้ายให้เสร็จสมบูรณ์ก่อนวันที่ 1 ธันวาคม 2020</span><span class="sxs-lookup"><span data-stu-id="ca6af-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="ca6af-108">ในขณะนี้ ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนไม่สนับสนุนคุณลักษณะทั้งหมดที่พร้อมใช้งานในกลไกจัดการการวางแผนที่สร้างขึ้นใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ca6af-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="ca6af-109">ดังนั้น จึงเป็นเรื่องสำคัญอย่างยิ่งที่คุณจะต้องประเมินว่าชุดคุณลักษณะที่พร้อมใช้งานในการเพิ่มประสิทธิภาพการวางแผนอยู่ในขณะนี้จะตรงกับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="ca6af-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="ca6af-110">ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนในขณะนี้ไม่ได้เปิดอยู่ตามค่าเริ่มต้นใน Dynamics Lifecycle Services (LCS) ดังนั้นคุณจึงมีโอกาสดำเนินการประเมินผลของคุณก่อนที่ลักษณะการทำงานดังกล่าวจะเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ca6af-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="ca6af-111">คุณต้องร้องขอข้อยกเว้นจากการย้ายการเพิ่มประสิทธิภาพการวางแผน ถ้ากระบวนการวางแผนหลักของคุณไม่รวมการผลิต (การวางแผนหลักที่สร้างแผนการใบสั่งผลิต) และคุณต้องใช้กลไกจัดการการวางแผนหลักในตัวรุ่น 10.0.15 ขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="ca6af-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="ca6af-112">การเริ่มต้นในรุ่น 10.0.16 ข้อผิดพลาดจะแสดงในสภาพแวดล้อมเมื่อรันการวางแผนหลักในตัวโดยไม่มีการสร้างแผนการใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="ca6af-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="ca6af-113">การเพิ่มประสิทธิภาพการวางแผนควรใช้สำหรับการปรับใช้ใหม่ทั้งหมดที่ไม่ได้สร้างแผนการใบสั่งผลิตในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="ca6af-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="ca6af-114">เจ้าของของสภาพแวดล้อมที่มีอยู่ซึ่งรันกลไกจัดการการวางแผนหลักในตัวโดยไม่มีการสร้างแผนการใบสั่งผลิต จะได้รับเมลที่มีรายละเอียดเกี่ยวกับกระบวนการยกเว้น</span><span class="sxs-lookup"><span data-stu-id="ca6af-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="ca6af-115">เราขอแนะนำให้คุณทำงานกับคู่ค้าในการประเมินและวางแผนการย้ายเพื่อการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="ca6af-116">ก่อนที่คุณจะเปิดการเพิ่มประสิทธิภาพการวางแผน เราขอแนะนำให้คุณประเมินผลลัพธ์ของการวิเคราะห์การปรับการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="ca6af-117">สำหรับข้อมูลเพิ่มเติมให้ดูที่ [การวิเคราะห์การปรับการเพิ่มประสิทธิภาพการวางแผน](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="ca6af-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="ca6af-118">ความพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ca6af-118">Availability</span></span>
<span data-ttu-id="ca6af-119">การเพิ่มประสิทธิภาพการวางแผนปัจจุบันพร้อมใช้งานในภูมิศาสตร์ Azure ต่อไปนี้: สหรัฐอเมริกา แคนาดา ยุโรป สหราชอาณาจักร และออสเตรเลีย</span><span class="sxs-lookup"><span data-stu-id="ca6af-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="ca6af-120">ถ้าคุณพยายามติดตั้ง Add-in จากภูมิภาคทางภูมิศาสตร์อื่น LCS จะแสดงข้อความที่ไม่สนับสนุนภูมิศาสตร์นี้</span><span class="sxs-lookup"><span data-stu-id="ca6af-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="ca6af-121">โปรดทราบว่าการเพิ่มประสิทธิภาพการวางแผนไม่สนับสนุนการปรับใช้ในสถานที่ของ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ca6af-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="ca6af-122">การให้ลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="ca6af-122">Licensing</span></span>

<span data-ttu-id="ca6af-123">ถ้าคุณสามารถรันการวางแผนหลักโดยใช้ลิขสิทธิ์ปัจจุบันของคุณ คุณไม่จำเป็นต้องซื้อลิขสิทธิ์เพิ่มเติมเพื่อเริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="ca6af-124">ติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="ca6af-124">Install the add-in</span></span>

<span data-ttu-id="ca6af-125">เมื่อต้องการใช้การเพิ่มประสิทธิภาพการวางแผน ให้ติดตั้ง Add-in ของการเพิ่มประสิทธิภาพการวางแผนสำหรับ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ca6af-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ca6af-126">คุณสามารถเข้าถึง Add-in จากโครงการ LCS ของคุณ และเปิดใช้งานฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนจากอินเทอร์เฟสผู้ใช้ (UI) Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ca6af-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="ca6af-127">ความต้องการสำหรับการเพิ่มประสิทธิภาพของการวางแผนคือ สภาพแวดล้อมที่มีความพร้อมใช้งานสูงที่เปิดใช้งาน ระดับ 2 หรือสูงกว่า (ไม่ใช่สภาพแวดล้อม OneBox) โดยมี Dynamics 365 Supply Chain Management รุ่น 10.0.7 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="ca6af-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="ca6af-128">ถ้าคุณพยายามติดตั้ง Add-in บนสภาพแวดล้อม OneBox การติดตั้งจะไม่เสร็จสมบูรณ์ และคุณจะต้องยกเลิกการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="ca6af-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="ca6af-129">ลงชื่อเข้าใช้ LCS และเปิดสภาพแวดล้อมที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ca6af-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="ca6af-130">ไปที่ **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="ca6af-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="ca6af-131">เลื่อนลงไปที่แท็บด่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="ca6af-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="ca6af-132">เลือก **การติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ca6af-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="ca6af-133">เลือก **การเพิ่มประสิทธิภาพการวางแผน**</span><span class="sxs-lookup"><span data-stu-id="ca6af-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="ca6af-134">ปฏิบัติตามคำแนะนำการติดตั้ง และยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="ca6af-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="ca6af-135">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="ca6af-135">Select **Install**.</span></span>
1. <span data-ttu-id="ca6af-136">บนแท็บด่วน **Add-in ของสภาพแวดล้อม** คุณควรเห็นว่าการเพิ่มประสิทธิภาพการวางแผนกำลังติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="ca6af-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="ca6af-137">หลังจากผ่านไปสองสามนาที **กำลังติดตั้ง** ควรเปลี่ยนเป็น **ติดตั้งแล้ว** (คุณอาจต้องรีเฟรชหน้านี้)</span><span class="sxs-lookup"><span data-stu-id="ca6af-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="ca6af-138">เมื่อติดตั้งแล้วคุณก็พร้อมแล้วที่จะเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผนใน Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ca6af-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="ca6af-139">วัตถุประสงค์หลักของการติดตั้ง add-in ของการเพิ่มประสิทธิภาพการวางแผนคือ การเชื่อมต่อบริการและสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="ca6af-139">The main purpose of installing the Planning Optimization add-in is to connect the service and the environment.</span></span> <span data-ttu-id="ca6af-140">ดังนั้น คุณต้องติดตั้ง add-in โดยแยกต่างหากสำหรับแต่ละสภาพแวดล้อมที่คุณจะใช้การเพิ่มประสิทธิภาพการวางแผน โดยไม่คำนึงถึงรหัสใดๆ ที่ถูกย้ายระหว่างสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="ca6af-140">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="ca6af-141">การรวมการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-141">Planning Optimization integration</span></span>

<span data-ttu-id="ca6af-142">เมื่อต้องการตั้งค่าคอนฟิกว่า Add-in การเพิ่มประสิทธิภาพการวางแผนควรใช้สำหรับการวางแผนหลักหรือไม่ ไปที่ **การวางแผนหลัก** \> **การตั้งค่า** \> **พารามิเตอร์การเพิ่มประสิทธิภาพการวางแผน**</span><span class="sxs-lookup"><span data-stu-id="ca6af-142">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="ca6af-143">สถานะการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="ca6af-143">Connection status</span></span>

<span data-ttu-id="ca6af-144">สถานะการเชื่อมต่อบ่งชี้สถานะปัจจุบันของการเชื่อมต่อระหว่าง Supply Chain Management และบริการการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-144">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="ca6af-145">ตารางต่อไปนี้แสดงค่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="ca6af-145">The following table shows the possible values.</span></span>

| <span data-ttu-id="ca6af-146">สถานะการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="ca6af-146">Connection status</span></span> | <span data-ttu-id="ca6af-147">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="ca6af-147">Description</span></span> | <span data-ttu-id="ca6af-148">สามารถใช้การเพิ่มประสิทธิภาพการวางแผนได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="ca6af-148">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="ca6af-149">เชื่อมต่อแล้ว</span><span class="sxs-lookup"><span data-stu-id="ca6af-149">Connected</span></span> | <span data-ttu-id="ca6af-150">มีการสร้างการเชื่อมต่อระหว่างบริการเพิ่มประสิทธิภาพของการวางแผน และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ca6af-150">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="ca6af-151">ใช่</span><span class="sxs-lookup"><span data-stu-id="ca6af-151">Yes</span></span> |
| <span data-ttu-id="ca6af-152">การเปิดใช้งานการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="ca6af-152">Enabling connection</span></span> | <span data-ttu-id="ca6af-153">คำขอเพื่อเปิดใช้งานการเชื่อมต่อกับบริการการเพิ่มประสิทธิภาพการวางแผนอยู่ระหว่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="ca6af-153">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="ca6af-154">ไม่</span><span class="sxs-lookup"><span data-stu-id="ca6af-154">No</span></span> |
| <span data-ttu-id="ca6af-155">ยกเลิกการเชื่อมต่อแล้ว</span><span class="sxs-lookup"><span data-stu-id="ca6af-155">Disconnected</span></span> | <span data-ttu-id="ca6af-156">ไม่มีการเชื่อมต่อกับบริการการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-156">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="ca6af-157">การเชื่อมต่อสามารถเปิดจาก LCS ได้ ดังที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="ca6af-157">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="ca6af-158">ไม่</span><span class="sxs-lookup"><span data-stu-id="ca6af-158">No</span></span> |
| <span data-ttu-id="ca6af-159">การปิดใช้งานการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="ca6af-159">Disabling connection</span></span> | <span data-ttu-id="ca6af-160">คำขอเพื่อปิดใช้งานการเชื่อมต่อกับบริการการเพิ่มประสิทธิภาพการวางแผนอยู่ระหว่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="ca6af-160">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="ca6af-161">ไม่</span><span class="sxs-lookup"><span data-stu-id="ca6af-161">No</span></span> |
| <span data-ttu-id="ca6af-162">กำลังเรียกสถานะ</span><span class="sxs-lookup"><span data-stu-id="ca6af-162">Getting status</span></span> | <span data-ttu-id="ca6af-163">ระบบกำลังรอข้อมูลสถานะจากบริการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-163">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="ca6af-164">ไม่</span><span class="sxs-lookup"><span data-stu-id="ca6af-164">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="ca6af-165">ตัวเลือกการใช้การเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-165">The Use Planning Optimization option</span></span>

<span data-ttu-id="ca6af-166">การตั้งค่าของตัวเลือก **ใช้การเพิ่มประสิทธิภาพการวางแผน** กำหนดว่ากลไกจัดการการวางแผนใดใช้สำหรับการวางแผนหลัก:</span><span class="sxs-lookup"><span data-stu-id="ca6af-166">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="ca6af-167">**ใช่** – การเพิ่มประสิทธิภาพการวางแผนใช้สำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="ca6af-167">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="ca6af-168">**ไม่ใช่** กลไกจัดการการวางแผน Supply Chain Management ในตัวใช้สำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="ca6af-168">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="ca6af-169">ถ้าชุดงานการวางแผนที่มีอยู่ที่สร้างไว้สำหรับกลไกจัดการการวางแผน Supply Chain Management ในตัวถูกทริกเกอร์ในขณะที่ตัวเลือก **ใช้การเพิ่มประสิทธิภาพการวางแผน** ถูกตั้งค่าเป็น **ใช่**  งานเหล่านั้นจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="ca6af-169">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="ca6af-170">รวมกับการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="ca6af-170">Integration with the setup</span></span>

<span data-ttu-id="ca6af-171">ถ้าการเพิ่มประสิทธิภาพการวางแผนถูกเปิดอยู่ การวางแผนหลักจะทำโดยใช้ Add-in การเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-171">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="ca6af-172">ในกรณีนี้ ผลลัพธ์ของการวางแผนหลักและคุณลักษณะจะได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="ca6af-172">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca6af-173">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ca6af-173">Additional resources</span></span>

[<span data-ttu-id="ca6af-174">ข้อกำหนดและเงื่อนไขสำหรับแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ca6af-174">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="ca6af-175">ภาพรวมของการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-175">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="ca6af-176">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-176">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="ca6af-177">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-177">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="ca6af-178">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-178">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="ca6af-179">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="ca6af-179">Cancel a planning job</span></span>](cancel-planning-job.md)
