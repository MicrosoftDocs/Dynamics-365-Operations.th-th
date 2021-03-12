---
title: แก้ไขปัญหาการเพิ่มประสิทธิภาพการวางแผน
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับการเพิ่มประสิทธิภาพของการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8e67a6faf52b51264555b06f56b289d19ca580d6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992581"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="e140a-103">แก้ไขปัญหาการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="e140a-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e140a-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบขณะทำงานกับการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="e140a-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="e140a-105">การติดตั้ง Add-in ของการเพิ่มประสิทธิภาพการวางแผนไม่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e140a-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="e140a-106">การเพิ่มประสิทธิภาพของการวางแผนต้องมีการเปิดใช้งาน Lifecycle Services (LCS) สภาพแวดล้อมที่มีความพร้อมใช้งานสูง ระดับ 2 หรือสูงกว่า (ไม่ใช่สภาพแวดล้อม OneBox) โดยมี Dynamics 365 Supply Chain Management รุ่น 10.0.7 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="e140a-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="e140a-107">ถ้าคุณพยายามติดตั้ง Add-in บนสภาพแวดล้อม OneBox การติดตั้งจะไม่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e140a-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="e140a-108">**การแก้ไข**: ยกเลิกการติดตั้งและใช้สภาพแวดล้อมความพร้อมใช้งานสูงระดับ 2 หรือสูงกว่า (ไม่ใช่สภาพแวดล้อม OneBox)</span><span class="sxs-lookup"><span data-stu-id="e140a-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="e140a-109">การวางแผนชุดงานล้มเหลวเมื่อเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="e140a-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="e140a-110">เมื่อคุณเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผน กลไกจัดการการวางแผนหลักที่มีอยู่แล้วจะถูกปิดใช้งานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e140a-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="e140a-111">ชุดงานการวางแผนหลักที่มีอยู่ที่สร้างไว้สำหรับกลไกจัดการการวางแผน Supply Chain Management ที่มีอยู่ในตัวจะล้มเหลวถ้าถูกทริกเกอร์ในขณะที่การเพิ่มประสิทธิภาพการวางแผนถูกเปิดใช้งาน งานเหล่านั้นจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="e140a-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="e140a-112">คุณอาจได้รับข้อความแสดงข้อผิดพลาด เช่น *การดำเนินงานนี้จะทริกเกอร์การวางแผนหลักที่ไม่ได้รับการสนับสนุนเมื่อเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผน*</span><span class="sxs-lookup"><span data-stu-id="e140a-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="e140a-113">**การแก้ไข**: ยกเลิกชุดงานการวางแผนหลักทั้งหมดที่สร้างขึ้นสำหรับกลไกจัดการการวางแผน Supply Chain Management ที่มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="e140a-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="e140a-114">ผลการเพิ่มประสิทธิภาพการวางแผนแตกต่างจากผลลัพธ์ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e140a-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="e140a-115">การเพิ่มประสิทธิภาพการวางแผนแตกต่างจากการออกแบบการวางแผนหลักที่มีอยู่ในตัวในบางพื้นที่</span><span class="sxs-lookup"><span data-stu-id="e140a-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="e140a-116">ลักษณะเช่นนี้อาจเกิดจากคุณลักษณะการทำงานที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="e140a-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="e140a-117">**การแก้ไข**: รันการวิเคราะห์การเพิ่มประสิทธิภาพของการวางแผนแล้ววิเคราะห์ผลลัพธ์ขณะอ้างอิงถึงเอกสารที่เกี่ยวข้องเพื่อให้เข้าใจถึงผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="e140a-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="e140a-118">สำหรับข้อมูลเพิ่มเติมให้ดูที่ [การวิเคราะห์การปรับการเพิ่มประสิทธิภาพการวางแผน](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="e140a-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a><span data-ttu-id="e140a-119">การวางแผนหลักไม่เคารพกรอบเวลาความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="e140a-119">Master planning doesn't respect the coverage time fence</span></span>

<span data-ttu-id="e140a-120">ซึ่งเกิดจากลักษณะการทำงานที่ค้างอยู่สำหรับการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="e140a-120">This is caused by a pending feature for Planning Optimization.</span></span>

<span data-ttu-id="e140a-121">**การแก้ไข**: จนกว่าลักษณะการทำงานที่ค้างอยู่จะพร้อมใช้งาน ให้กรองหรือลบแผนการใบสั่งเพื่อลบข้อแนะนำในการจัดหาวัสดุออกนอกกรอบเวลาความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="e140a-121">**Fix**: Until the pending feature is available, filter or delete planned orders to remove supply suggestions outside of the coverage time fence.</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="e140a-122">ไม่สามารถเปิดใช้การเพิ่มประสิทธิภาพการวางแผนได้</span><span class="sxs-lookup"><span data-stu-id="e140a-122">Can't enable Planning Optimization</span></span>

<span data-ttu-id="e140a-123">**สถานะการเชื่อมต่อ** ต้องเป็น **เชื่อมต่อ** ก่อนที่คุณจะสามารถตั้งค่า **ใช้การเพิ่มประสิทธิภาพการวางแผน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="e140a-123">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="e140a-124">สำหรับข้อมูลเพิ่มเติมให้ดูที่ [การเริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="e140a-124">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="e140a-125">**การแก้ไข**: ตรวจสอบให้แน่ใจว่าได้ติดตั้ง Add-in การเพิ่มประสิทธิภาพการวางแผนเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="e140a-125">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="e140a-126">แสดงข้อความแสดงข้อผิดพลาดในระหว่าง CTP</span><span class="sxs-lookup"><span data-stu-id="e140a-126">Error message is shown during CTP</span></span>

<span data-ttu-id="e140a-127">ถ้าคุณพยายามที่จะรันปริมาณที่สามารถสัญญาได้ (CTP) จากใบสั่งขายเมื่อมีการเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผน คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: *การดำเนินการนี้จะทริกเกอร์การวางแผนหลักที่ไม่ได้รับการสนับสนุนเมื่อเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผน*</span><span class="sxs-lookup"><span data-stu-id="e140a-127">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="e140a-128">ซึ่งนี่เกี่ยวข้องกับลักษณะการทำงานที่ค้างอยู่ซึ่งวางแผนไว้เป็นส่วนหนึ่งของการสนับสนุนสำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="e140a-128">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="e140a-129">**การแก้ไข:** หลีกเลี่ยงการคำนวณ CTP เมื่อเปิดใช้งานการเพิ่มประสิทธิภาพการวางแผนจนกว่าจะมีการสนับสนุน CTP</span><span class="sxs-lookup"><span data-stu-id="e140a-129">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e140a-130">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e140a-130">Additional resources</span></span>

[<span data-ttu-id="e140a-131">เริ่มต้นใช้งานการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="e140a-131">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="e140a-132">การวิเคราะห์ความเหมาะสมของการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="e140a-132">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
