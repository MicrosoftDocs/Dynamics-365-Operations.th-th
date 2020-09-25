---
title: ประสิทธิภาพการจัดกำหนดการทรัพยากรของโครงการ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการปรับปรุงประสิทธิภาพการทำงานของการจัดกำหนดการทรัพยากรสำหรับโครงการจำนวนมาก
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760679"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="31148-103">ประสิทธิภาพการจัดกำหนดการทรัพยากรของโครงการ</span><span class="sxs-lookup"><span data-stu-id="31148-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="31148-104">ปัญหาด้านประสิทธิภาพที่เกี่ยวข้องกับการจัดกำหนดการทรัพยากรอาจเกิดขึ้นเมื่อจำนวนของโครงการมีอยู่จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="31148-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="31148-105">เมื่อต้องการปรับปรุงประสิทธิภาพของการจัดกำหนดการทรัพยากร คุณลักษณะที่มีอยู่ช่วยให้ผู้ใช้สามารถลดเวลาที่ใช้ในการเปิดใช้งานแบบฟอร์มความพร้อมของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="31148-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="31148-106">โดยเฉพาะอย่างยิ่ง การดำเนินการนี้จะเป็นการลบกระบวนการซิงโครไนส์ค่าสะสมความสามารถรองรับของทรัพยากรและใช้ตาราง **ResProjectResource** เพื่อเพิ่มความเร็วในการค้นหาทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="31148-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="31148-107">โปรดทราบว่าตาราง **ResRollup** จะไม่มีการใช้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="31148-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31148-108">ถ้ามีการขึ้นต่อกันในกระบวนการซิงโครไนส์ค่าสะสมความสามารถรองรับของทรัพยากรหรือตาราง **ResProjectResource** อย่าใช้คุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="31148-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="31148-109">เปิดใช้งานการปรับปรุงประสิทธิภาพของการจัดกำหนดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="31148-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="31148-110">เมื่อต้องการเปิดใช้งานการปรับปรุงประสิทธิภาพของการจัดกำหนดการทรัพยากร ให้ทำตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="31148-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="31148-111">ไปที่ **การจัดการคุณลักษณะ** > **ทั้งหมด** และในรายการคุณลักษณะ ให้ค้นหา **เปิดใช้งานคุณลักษณะการปรับปรุงประสิทธิภาพของการจัดกำหนดการทรัพยากรโครงการ**</span><span class="sxs-lookup"><span data-stu-id="31148-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="31148-112">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="31148-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="31148-113">ถ้าคุณไม่พบคุณลักษณะในรายการ ให้เลือก **ตรวจหาการอัปเดต** เพื่อรีเฟรชรายการ</span><span class="sxs-lookup"><span data-stu-id="31148-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="31148-114">รีเฟรชเบราว์เซอร์ของคุณ แล้วไปที่ **การจัดการและการบัญชีโครงการ** > **ประจำงวด** > **ทรัพยากรโครงการ** > **ซิงโครไนส์ความสามารถรองรับในปฏิทินทรัพยากรในบริษัททั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="31148-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="31148-115">ตั้งค่า **ลบเรกคอร์ดความสามารถรองรับที่มีอยู่** เป็น **ใช่** เพื่อลบข้อมูลก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="31148-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="31148-116">ถ้าคุณต้องการสร้างข้อมูลส่วนเพิ่ม ให้ตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="31148-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="31148-117">ในฟิลด์ **รหัสรอบระยะเวลา** ให้เลือกรอบระยะเวลาที่ควรสร้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="31148-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="31148-118">ถ้าคุณเลือกรหัสรอบระยะเวลา ไม่จำเป็นต้องกำหนดวันที่เริ่มต้นและวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="31148-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="31148-119">ถ้าคุณปล่อยฟิลด์ **รหัสรอบระยะเวลา** เว้นว่างไว้ ให้เลือกวันที่เริ่มต้นและสิ้นสุดเฉพาะเพื่อสร้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="31148-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="31148-120">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="31148-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="31148-121">การดำเนินการนี้จะกระจายข้อมูลทั่วไปไปยังตาราง **ResCalendarCapacity** ระหว่างบริษัททั้งหมดในสภาพแวดล้อมของคุณ จึงต้องรันชุดงานในนิติบุคคลเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="31148-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="31148-122">ข้อมูลในชุดงานนี้จำเป็นต้องใช้ในการคำนวณความสามารถรองรับของทรัพยากรผ่านทางปฏิทินที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="31148-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="31148-123">ไปที่ **การจัดการและการบัญชีโครงการ** > **ประจำงวด** > **ทรัพยากรโครงการ** > **เติมข้อมูลทรัพยากรโครงการในบริษัททั้งหมด** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="31148-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="31148-124">ทรัพยากรโครงการในบริษัททั้งหมดตาราง **ResProjectResource**, **ResCalendarDateTimeRange** และ **ResEffectiveDateTimeRange**</span><span class="sxs-lookup"><span data-stu-id="31148-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="31148-125">ค่าสำหรับฟิลด์ **PSAPRojSchedRole.RootActivity** จะได้รับการอัปเดตด้วย</span><span class="sxs-lookup"><span data-stu-id="31148-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="31148-126">ถ้าไม่ได้ทำงานอยู่ คุณจะได้รับคำเตือนเมื่อพยายามดำเนินการจัดกำหนดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="31148-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="31148-127">ปิดการปรับปรุงประสิทธิภาพของการจัดกำหนดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="31148-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="31148-128">ไปที่ **การจัดการคุณลักษณะ** > **ทั้งหมด** และให้ค้นหา **เปิดใช้งานคุณลักษณะการปรับปรุงประสิทธิภาพของการจัดกำหนดการทรัพยากรโครงการ**</span><span class="sxs-lookup"><span data-stu-id="31148-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="31148-129">เลือกคุณลักษณะ แล้วเลือกปุ่ม **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="31148-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="31148-130">รีเฟรชเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="31148-130">Refresh your browser.</span></span>
4. <span data-ttu-id="31148-131">ไปที่ **การจัดการและการบัญชีโครงการ** > **ประจำงวด** > **การซิงโครไนส์ความสามารถรองรับ** > **ซิงโครไนส์ค่าสะสมความสามารถรองรับของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="31148-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="31148-132">บนหน้า **การซิงโครไนส์ค่าสะสมความสามารถรองรับ** ให้ตั้งค่า **ลบเรกคอร์ดความสามารถรองรับที่มีที่มีอยู่** เป็น **ใช่** เพื่อลบข้อมูลก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="31148-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="31148-133">ถ้าคุณต้องการสร้างข้อมูลส่วนเพิ่ม ให้ตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="31148-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="31148-134">ในฟิลด์ **รหัสรอบระยะเวลา** ให้เลือกรอบระยะเวลาที่ควรสร้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="31148-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="31148-135">ถ้าคุณเลือกรหัสรอบระยะเวลา ไม่จำเป็นต้องกำหนดวันที่เริ่มต้นและวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="31148-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="31148-136">ถ้าคุณปล่อยฟิลด์ **รหัสรอบระยะเวลา** เว้นว่างไว้ ให้เลือกวันที่เริ่มต้นและสิ้นสุดเฉพาะเพื่อสร้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="31148-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="31148-137">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="31148-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="31148-138">การดำเนินการนี้จะกระจายข้อมูลทั่วไปไปยังตาราง **ResRollup** ระหว่างบริษัททั้งหมดในสภาพแวดล้อมของคุณ จึงต้องรันชุดงานในนิติบุคคลเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="31148-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="31148-139">ชุดงานนี้จำเป็นสำหรับมุมมอง **ความพร้อมของทรัพยากร** ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="31148-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="31148-140">ถ้าไม่มีการเรียกใช้ชุดงานนี้ จะมีการสร้างข้อมูล **ResRollup** แบบในทันที ซึ่งอาจใช้เวลา</span><span class="sxs-lookup"><span data-stu-id="31148-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
