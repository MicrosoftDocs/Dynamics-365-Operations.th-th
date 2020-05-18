---
title: เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน
description: หัวข้อนี้อธิบายวิธีการเริ่มใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
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
ms.openlocfilehash: ce1bbb18e9a448e84d001a4195421d2b0e4af5be
ms.sourcegitcommit: c0d37fdd70f3dec4605fdee6f981f84a49be9b9e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/06/2020
ms.locfileid: "3339889"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="179ff-103">เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="179ff-104">ในขณะนี้ ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนไม่สนับสนุนคุณลักษณะทั้งหมดที่พร้อมใช้งานในกลไกจัดการการวางแผนที่สร้างขึ้นใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="179ff-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="179ff-105">ดังนั้น จึงเป็นเรื่องสำคัญอย่างยิ่งที่คุณจะต้องประเมินว่าชุดคุณลักษณะที่พร้อมใช้งานในการเพิ่มประสิทธิภาพการวางแผนอยู่ในขณะนี้จะตรงกับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="179ff-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="179ff-106">โดยค่าเริ่มต้น งานฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนจะไม่เปิดใช้ใน Dynamics Lifecycle Services (LCS) โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="179ff-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="179ff-107">ดังนั้น คุณจึงมีโอกาสดำเนินการประเมินผลของคุณก่อนที่จะเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="179ff-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="179ff-108">ในที่สุด การเพิ่มประสิทธิภาพของการวางแผนจะแทนที่กลไกจัดการการวางแผน Supply Chain Management ในตัวที่มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="179ff-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="179ff-109">ก่อนที่คุณจะเปิดการเพิ่มประสิทธิภาพการวางแผน เราขอแนะนำให้คุณประเมินผลลัพธ์ของการวิเคราะห์การปรับการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="179ff-110">สำหรับข้อมูลเพิ่มเติมให้ดูที่ [การวิเคราะห์การปรับการเพิ่มประสิทธิภาพการวางแผน](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="179ff-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="179ff-111">ความพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="179ff-111">Availability</span></span>
<span data-ttu-id="179ff-112">การเพิ่มประสิทธิภาพการวางแผนปัจจุบันพร้อมใช้งานในภูมิศาสตร์ Azure ต่อไปนี้: สหรัฐอเมริกา แคนาดา ยุโรป สหราชอาณาจักร และออสเตรเลีย</span><span class="sxs-lookup"><span data-stu-id="179ff-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="179ff-113">ถ้าคุณพยายามติดตั้ง Add-in จากภูมิภาคทางภูมิศาสตร์อื่น LCS จะแสดงข้อความที่ไม่สนับสนุนภูมิศาสตร์นี้</span><span class="sxs-lookup"><span data-stu-id="179ff-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="179ff-114">โปรดทราบว่าการเพิ่มประสิทธิภาพการวางแผนไม่สนับสนุนการปรับใช้ในสถานที่ของ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="179ff-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="179ff-115">การให้ลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="179ff-115">Licensing</span></span>

<span data-ttu-id="179ff-116">ถ้าคุณสามารถรันการวางแผนหลักโดยใช้ลิขสิทธิ์ปัจจุบันของคุณ คุณไม่จำเป็นต้องซื้อลิขสิทธิ์เพิ่มเติมเพื่อเริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="179ff-117">ติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="179ff-117">Install the add-in</span></span>

<span data-ttu-id="179ff-118">เมื่อต้องการใช้การเพิ่มประสิทธิภาพการวางแผน ให้ติดตั้ง Add-in ของการเพิ่มประสิทธิภาพการวางแผนสำหรับ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="179ff-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="179ff-119">คุณสามารถเข้าถึง Add-in จากโครงการ LCS ของคุณ และเปิดใช้งานฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนจากอินเทอร์เฟสผู้ใช้ (UI) Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="179ff-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="179ff-120">ความต้องการสำหรับการเพิ่มประสิทธิภาพของการวางแผนคือ สภาพแวดล้อมที่มีความพร้อมใช้งานสูงที่เปิดใช้งาน ระดับ 2 หรือสูงกว่า (ไม่ใช่สภาพแวดล้อม OneBox) โดยมี Dynamics 365 Supply Chain Management รุ่น 10.0.7 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="179ff-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="179ff-121">ถ้าคุณพยายามติดตั้ง Add-in บนสภาพแวดล้อม OneBox การติดตั้งจะไม่เสร็จสมบูรณ์ และคุณจะต้องยกเลิกการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="179ff-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="179ff-122">ลงชื่อเข้าใช้ LCS และเปิดสภาพแวดล้อมที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="179ff-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="179ff-123">ไปที่ **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="179ff-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="179ff-124">เลื่อนลงไปที่แท็บด่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="179ff-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="179ff-125">เลือก **การติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="179ff-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="179ff-126">เลือก **การเพิ่มประสิทธิภาพการวางแผน**</span><span class="sxs-lookup"><span data-stu-id="179ff-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="179ff-127">ปฏิบัติตามคำแนะนำการติดตั้ง และยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="179ff-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="179ff-128">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="179ff-128">Select **Install**.</span></span>
1. <span data-ttu-id="179ff-129">บนแท็บด่วน **Add-in ของสภาพแวดล้อม** คุณควรเห็นว่าการเพิ่มประสิทธิภาพการวางแผนกำลังติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="179ff-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="179ff-130">หลังจากผ่านไปสองสามนาที **กำลังติดตั้ง** ควรเปลี่ยนเป็น **ติดตั้งแล้ว** (คุณอาจต้องรีเฟรชหน้านี้)</span><span class="sxs-lookup"><span data-stu-id="179ff-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="179ff-131">เมื่อติดตั้งแล้วคุณก็พร้อมแล้วที่จะเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผนใน Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="179ff-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="179ff-132">การรวมการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-132">Planning Optimization integration</span></span>

<span data-ttu-id="179ff-133">เมื่อต้องการตั้งค่าคอนฟิกว่า Add-in การเพิ่มประสิทธิภาพการวางแผนควรใช้สำหรับการวางแผนหลักหรือไม่ ไปที่ **การวางแผนหลัก** \> **การตั้งค่า** \> **พารามิเตอร์การเพิ่มประสิทธิภาพการวางแผน**</span><span class="sxs-lookup"><span data-stu-id="179ff-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="179ff-134">สถานะการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="179ff-134">Connection status</span></span>

<span data-ttu-id="179ff-135">สถานะการเชื่อมต่อบ่งชี้สถานะปัจจุบันของการเชื่อมต่อระหว่าง Supply Chain Management และบริการการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="179ff-136">ตารางต่อไปนี้แสดงค่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="179ff-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="179ff-137">สถานะการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="179ff-137">Connection status</span></span> | <span data-ttu-id="179ff-138">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="179ff-138">Description</span></span> | <span data-ttu-id="179ff-139">สามารถใช้การเพิ่มประสิทธิภาพการวางแผนได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="179ff-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="179ff-140">เชื่อมต่อแล้ว</span><span class="sxs-lookup"><span data-stu-id="179ff-140">Connected</span></span> | <span data-ttu-id="179ff-141">มีการสร้างการเชื่อมต่อระหว่างบริการเพิ่มประสิทธิภาพของการวางแผน และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="179ff-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="179ff-142">ใช่</span><span class="sxs-lookup"><span data-stu-id="179ff-142">Yes</span></span> |
| <span data-ttu-id="179ff-143">การเปิดใช้งานการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="179ff-143">Enabling connection</span></span> | <span data-ttu-id="179ff-144">คำขอเพื่อเปิดใช้งานการเชื่อมต่อกับบริการการเพิ่มประสิทธิภาพการวางแผนอยู่ระหว่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="179ff-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="179ff-145">ไม่</span><span class="sxs-lookup"><span data-stu-id="179ff-145">No</span></span> |
| <span data-ttu-id="179ff-146">ยกเลิกการเชื่อมต่อแล้ว</span><span class="sxs-lookup"><span data-stu-id="179ff-146">Disconnected</span></span> | <span data-ttu-id="179ff-147">ไม่มีการเชื่อมต่อกับบริการการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="179ff-148">การเชื่อมต่อสามารถเปิดจาก LCS ได้ ดังที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="179ff-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="179ff-149">ไม่</span><span class="sxs-lookup"><span data-stu-id="179ff-149">No</span></span> |
| <span data-ttu-id="179ff-150">การปิดใช้งานการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="179ff-150">Disabling connection</span></span> | <span data-ttu-id="179ff-151">คำขอเพื่อปิดใช้งานการเชื่อมต่อกับบริการการเพิ่มประสิทธิภาพการวางแผนอยู่ระหว่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="179ff-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="179ff-152">ไม่</span><span class="sxs-lookup"><span data-stu-id="179ff-152">No</span></span> |
| <span data-ttu-id="179ff-153">กำลังเรียกสถานะ</span><span class="sxs-lookup"><span data-stu-id="179ff-153">Getting status</span></span> | <span data-ttu-id="179ff-154">ระบบกำลังรอข้อมูลสถานะจากบริการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="179ff-155">ไม่</span><span class="sxs-lookup"><span data-stu-id="179ff-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="179ff-156">ตัวเลือกการใช้การเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="179ff-157">การตั้งค่าของตัวเลือก **ใช้การเพิ่มประสิทธิภาพการวางแผน** กำหนดว่ากลไกจัดการการวางแผนใดใช้สำหรับการวางแผนหลัก:</span><span class="sxs-lookup"><span data-stu-id="179ff-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="179ff-158">**ใช่** – การเพิ่มประสิทธิภาพการวางแผนใช้สำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="179ff-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="179ff-159">**ไม่ใช่** กลไกจัดการการวางแผน Supply Chain Management ในตัวใช้สำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="179ff-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="179ff-160">ถ้าชุดงานการวางแผนที่มีอยู่ที่สร้างไว้สำหรับกลไกจัดการการวางแผน Supply Chain Management ในตัวถูกทริกเกอร์ในขณะที่ตัวเลือก **ใช้การเพิ่มประสิทธิภาพการวางแผน** ถูกตั้งค่าเป็น **ใช่**  งานเหล่านั้นจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="179ff-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="179ff-161">รวมกับการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="179ff-161">Integration with the setup</span></span>

<span data-ttu-id="179ff-162">ถ้าการแสดงตัวอย่างการเพิ่มประสิทธิภาพการวางแผนเปิดอยู่ การวางแผนหลักจะทำโดยใช้ Add-in การเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="179ff-163">ในกรณีนี้ ผลลัพธ์ของการวางแผนหลักและคุณลักษณะจะได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="179ff-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="179ff-164">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="179ff-164">Additional resources</span></span>

[<span data-ttu-id="179ff-165">ข้อกำหนดและเงื่อนไขสำหรับแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="179ff-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="179ff-166">ภาพรวมของการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="179ff-167">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="179ff-168">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="179ff-169">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="179ff-170">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="179ff-170">Cancel a planning job</span></span>](cancel-planning-job.md)
