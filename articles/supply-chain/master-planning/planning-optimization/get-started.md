---
title: เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน
description: หัวข้อนี้อธิบายวิธีการเริ่มใช้ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774059"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="047c1-103">เริ่มต้นด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="047c1-104">ในขณะนี้ ฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนไม่สนับสนุนคุณลักษณะทั้งหมดที่พร้อมใช้งานในกลไกจัดการการวางแผนที่สร้างขึ้นใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="047c1-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="047c1-105">ดังนั้น จึงเป็นเรื่องสำคัญอย่างยิ่งที่คุณจะต้องประเมินว่าชุดคุณลักษณะที่พร้อมใช้งานในการเพิ่มประสิทธิภาพการวางแผนอยู่ในขณะนี้จะตรงกับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="047c1-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="047c1-106">โดยค่าเริ่มต้น งานฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนจะไม่เปิดใช้ใน Dynamics Lifecycle Services (LCS) โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="047c1-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="047c1-107">ดังนั้น คุณจึงมีโอกาสดำเนินการประเมินผลของคุณก่อนที่จะเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="047c1-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="047c1-108">ในที่สุด การเพิ่มประสิทธิภาพของการวางแผนจะแทนที่กลไกจัดการการวางแผน Supply Chain Management ในตัวที่มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="047c1-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="047c1-109">ก่อนที่คุณจะเปิดการเพิ่มประสิทธิภาพการวางแผน เราขอแนะนำให้คุณประเมินผลลัพธ์ของการวิเคราะห์การปรับการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="047c1-110">สำหรับข้อมูลเพิ่มเติมให้ดูที่ [การวิเคราะห์การปรับการเพิ่มประสิทธิภาพการวางแผน](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="047c1-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="047c1-111">การให้ลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="047c1-111">Licensing</span></span>

<span data-ttu-id="047c1-112">ถ้าคุณสามารถรันการวางแผนหลักโดยใช้ลิขสิทธิ์ปัจจุบันของคุณ คุณไม่จำเป็นต้องซื้อลิขสิทธิ์เพิ่มเติมเพื่อเริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="047c1-113">ติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="047c1-113">Install the add-in</span></span>

<span data-ttu-id="047c1-114">เมื่อต้องการใช้การเพิ่มประสิทธิภาพการวางแผน ให้ติดตั้ง Add-in ของการเพิ่มประสิทธิภาพการวางแผนสำหรับ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="047c1-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="047c1-115">คุณสามารถเข้าถึง Add-in จากโครงการ LCS ของคุณ และเปิดใช้งานฟังก์ชันการเพิ่มประสิทธิภาพการวางแผนจากอินเทอร์เฟสผู้ใช้ (UI) Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="047c1-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="047c1-116">ลงชื่อเข้าใช้ LCS และเปิดสภาพแวดล้อมที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="047c1-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="047c1-117">ไปที่ **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="047c1-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="047c1-118">เลือก **เก็บรักษา** หรือเลื่อนลงไปที่แท็บด่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="047c1-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="047c1-119">เลือก **การติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="047c1-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="047c1-120">เลือก **การเพิ่มประสิทธิภาพการวางแผน**</span><span class="sxs-lookup"><span data-stu-id="047c1-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="047c1-121">ปฏิบัติตามคำแนะนำการติดตั้ง และยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="047c1-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="047c1-122">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="047c1-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="047c1-123">การรวมการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-123">Planning Optimization integration</span></span>

<span data-ttu-id="047c1-124">เมื่อต้องการตั้งค่าคอนฟิกว่าควรใช้การเพิ่มประสิทธิภาพการวางแผนสำหรับการวางแผนหลักหรือไม่ ไปที่ **การวางแผนหลัก** \> **การตั้งค่า** \> **การรวมการเพิ่มประสิทธิภาพการวางแผนหลัก** \> **การรวมพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="047c1-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="047c1-125">สถานะการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="047c1-125">Connection status</span></span>

<span data-ttu-id="047c1-126">สถานะการเชื่อมต่อบ่งชี้สถานะปัจจุบันของการเชื่อมต่อระหว่าง Supply Chain Management และบริการการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="047c1-127">ตารางต่อไปนี้แสดงค่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="047c1-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="047c1-128">สถานะการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="047c1-128">Connection status</span></span> | <span data-ttu-id="047c1-129">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="047c1-129">Description</span></span> | <span data-ttu-id="047c1-130">สามารถใช้การเพิ่มประสิทธิภาพการวางแผนได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="047c1-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="047c1-131">เชื่อมต่อแล้ว</span><span class="sxs-lookup"><span data-stu-id="047c1-131">Connected</span></span> | <span data-ttu-id="047c1-132">มีการสร้างการเชื่อมต่อระหว่างบริการเพิ่มประสิทธิภาพของการวางแผน และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="047c1-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="047c1-133">ใช่</span><span class="sxs-lookup"><span data-stu-id="047c1-133">Yes</span></span> |
| <span data-ttu-id="047c1-134">การเปิดใช้งานการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="047c1-134">Enabling connection</span></span> | <span data-ttu-id="047c1-135">คำขอเพื่อเปิดใช้งานการเชื่อมต่อกับบริการการเพิ่มประสิทธิภาพการวางแผนอยู่ระหว่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="047c1-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="047c1-136">ไม่</span><span class="sxs-lookup"><span data-stu-id="047c1-136">No</span></span> |
| <span data-ttu-id="047c1-137">ยกเลิกการเชื่อมต่อแล้ว</span><span class="sxs-lookup"><span data-stu-id="047c1-137">Disconnected</span></span> | <span data-ttu-id="047c1-138">ไม่มีการเชื่อมต่อกับบริการการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="047c1-139">การเชื่อมต่อสามารถเปิดจาก LCS ได้ ดังที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="047c1-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="047c1-140">ไม่</span><span class="sxs-lookup"><span data-stu-id="047c1-140">No</span></span> |
| <span data-ttu-id="047c1-141">การปิดใช้งานการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="047c1-141">Disabling connection</span></span> | <span data-ttu-id="047c1-142">คำขอเพื่อปิดใช้งานการเชื่อมต่อกับบริการการเพิ่มประสิทธิภาพการวางแผนอยู่ระหว่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="047c1-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="047c1-143">ไม่</span><span class="sxs-lookup"><span data-stu-id="047c1-143">No</span></span> |
| <span data-ttu-id="047c1-144">กำลังเรียกสถานะ</span><span class="sxs-lookup"><span data-stu-id="047c1-144">Getting status</span></span> | <span data-ttu-id="047c1-145">ระบบกำลังรอข้อมูลสถานะจากบริการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="047c1-146">ไม่</span><span class="sxs-lookup"><span data-stu-id="047c1-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="047c1-147">ตัวเลือกการใช้การเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="047c1-148">การตั้งค่าของตัวเลือก **ใช้การเพิ่มประสิทธิภาพการวางแผน** กำหนดว่ากลไกจัดการการวางแผนใดใช้สำหรับการวางแผนหลัก:</span><span class="sxs-lookup"><span data-stu-id="047c1-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="047c1-149">**ใช่** – การเพิ่มประสิทธิภาพการวางแผนใช้สำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="047c1-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="047c1-150">**ไม่ใช่** กลไกจัดการการวางแผน Supply Chain Management ในตัวใช้สำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="047c1-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="047c1-151">ถ้าชุดงานการวางแผนที่มีอยู่ที่สร้างไว้สำหรับกลไกจัดการการวางแผน Supply Chain Management ในตัวถูกทริกเกอร์ในขณะที่ตัวเลือก **ใช้การเพิ่มประสิทธิภาพการวางแผน** ถูกตั้งค่าเป็น **ใช่**  งานเหล่านั้นจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="047c1-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="047c1-152">รวมกับการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="047c1-152">Integration with the setup</span></span>

<span data-ttu-id="047c1-153">ถ้าการแสดงตัวอย่างการเพิ่มประสิทธิภาพการวางแผนเปิดอยู่ การวางแผนหลักจะทำโดยใช้ Add-in การเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="047c1-154">ในกรณีนี้ ผลลัพธ์ของการวางแผนหลักและคุณลักษณะจะได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="047c1-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="047c1-155">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="047c1-155">Related resources</span></span>

[<span data-ttu-id="047c1-156">ข้อกำหนดและเงื่อนไขสำหรับแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="047c1-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="047c1-157">ภาพรวมการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="047c1-158">การวิเคราะห์การปรับให้เหมาะสมกับการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="047c1-159">ดูประวัติการวางแผนและล็อกการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="047c1-160">ใช้ตัวกรองกับแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="047c1-161">ยกเลิกงานการวางแผน</span><span class="sxs-lookup"><span data-stu-id="047c1-161">Cancel a planning job</span></span>](cancel-planning-job.md)
