---
title: เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน
description: หัวข้อนี้อธิบายเจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงานในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0a8fcf26da02bd42f6ee45687c585091e3b945e
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570989"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="18351-103">เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="18351-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="18351-104">หัวข้อนี้อธิบายเจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงานในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="18351-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="18351-105">ในการจัดการสินทรัพย์ คุณสามารถเชื่อมต่อเจ้าหน้าที่บำรุงรักษากับเจ้าหน้าที่บำรุงรักษาได้</span><span class="sxs-lookup"><span data-stu-id="18351-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="18351-106">(สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตำแหน่งที่ทำงาน ดู [สร้างตำแหน่งที่ทำงาน](../functional-locations/create-functional-locations.md)) ฟังก์ชันนี้อาจมีประโยชน์ ตัวอย่างเช่น คุณกำลังจัดกำหนดการงานบำรุงรักษาบนเครื่องที่ตั้งอยู่ในตำแหน่งที่ทำงาน 01 และคุณต้องการปันส่วนเจ้าหน้าที่บำรุงรักษาจากที่ตั้งเดียวกันเพื่อดำเนินการงาน</span><span class="sxs-lookup"><span data-stu-id="18351-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="18351-107">นอกจากนี้ คุณยังสามารถสร้างกลุ่มเจ้าหน้าที่บำรุงรักษา และเชื่อมโยงเจ้าหน้าที่บำรุงรักษากับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="18351-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="18351-108">ฟังก์ชันนี้จะมีประโยชน์เมื่อคุณทำการจัดกำหนดการใบสั่งงานอย่างง่าย และคุณต้องการจัดกำหนดการกลุ่มของเจ้าหน้าที่บำรุงรักษาในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="18351-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="18351-109">คุณสามารถใช้เจ้าหน้าที่บำรุงรักษาและกลุ่มเจ้าหน้าที่บำรุงรักษา เพื่อตั้งค่าเจ้าหน้าที่บำรุงรักษาที่ต้องการและเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="18351-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="18351-110">สร้างผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="18351-110">Create workers</span></span>

1. <span data-ttu-id="18351-111">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **ผู้ปฏิบัติงาน** \> **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="18351-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="18351-112">เลือก **สร้าง** เพื่อเพิ่มผู้ปฏิบัติงานลงในรายการ</span><span class="sxs-lookup"><span data-stu-id="18351-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="18351-113">ในฟิลด์ **ผู้ปฏิบัติงาน** เลือกผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="18351-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="18351-114">ตั้งค่าตัวเลือก **ใช้งานอยู่** เป็น **ใช่** เพื่อจัดกำหนดการผู้ปฏิบัติงานในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="18351-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="18351-115">บน FastTab **ทั่วไป** ฟิลด์ **ทรัพยากร** และฟิลด์ **คำอธิบาย** จะถูกกรอกข้อมูลโดยอัตโนมัติ ถ้ามีการเลือกทรัพยากรสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="18351-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="18351-116">นอกจากนี้ ฟิลด์ **ปฏิทิน** ยังจะถูกกรอกข้อมูลโดยอัตโนมัติ หากคุณได้ตั้งค่าผู้ปฏิบัติงานเป็นทรัพยากรและปันส่วนปฏิทินไปยังทรัพยากรนั้นบนหน้า **ทรัพยากร** (**การจัดการองค์กร** \> **ทรัพยากร** \> **ทรัพยากร**)</span><span class="sxs-lookup"><span data-stu-id="18351-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="18351-117">บน FastTab **กลุ่ม** ให้เลือก **เพิ่ม** แล้วจากนั้น เลือกกลุ่มเจ้าหน้าที่บำรุงรักษาสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="18351-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="18351-118">สามารถสังกัดผู้ปฏิบัติงานกับกลุ่มได้มากกว่าหนึ่งกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="18351-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="18351-119">ในการตั้งค่ามาตรฐาน  สังกัดของผู้ปฏิบัติงานกับกลุ่มจะมีผลตั้งแต่วันที่ที่คุณเพิ่มกลุ่ม และจะไม่หมดอายุ</span><span class="sxs-lookup"><span data-stu-id="18351-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="18351-120">วันที่นี้จะแสดงอยู่ในฟิลด์ **มีผลบังคับใช้**</span><span class="sxs-lookup"><span data-stu-id="18351-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="18351-121">เพื่อดูฟิลด์ **มีผลบังคับใช้** เลือก **มุมมอง** \> **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="18351-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="18351-122">ถ้าสังกัดของผู้ปฏิบัติงานกับกลุ่มควรถูกจำกัดตามรอบระยะเวลาที่ระบุ ให้ใช้ฟิลด์ **มีผลบังคับใช้** และฟิลด์ **การหมดอายุ** เพื่อกำหนดรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="18351-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="18351-123">บน FastTab **ตำแหน่งที่ทำงาน** ให้เลือก **เพิ่ม** แล้วจากนั้น เลือกตำแหน่งที่ทำงานสำหรับเจ้าหน้าที่บำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="18351-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="18351-124">นอกจากนี้ ระบุสถานที่ที่เป็นตำแหน่งที่ทำงานหลักสำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="18351-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="18351-125">เมื่อคุณเพิ่มตำแหน่งที่ทำงานให้กับผู้ปฏิบัติงาน สินทรัพย์ที่ใช้งานอยู่ทั้งหมดที่เกี่ยวข้องกับตำแหน่งที่ทำงานจะปรากฏบนรายการเมนูต่างๆ เช่น **สินทรัพย์ที่ใช้งานอยู่ของฉัน** และ **ตำแหน่งที่ทำงานที่ใช้งานอยู่ของฉัน**</span><span class="sxs-lookup"><span data-stu-id="18351-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="18351-126">นอกจากนี้ ยังปรากฏในการค้นหาสินทรัพย์ที่แสดง เมื่อคุณสร้างสินทรัพย์ใหม่ คำขอการบำรุงรักษา หรือใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="18351-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="18351-127">ฟิลด์บน FastTab **รายละเอียด** แสดงจำนวนของกลุ่มเจ้าหน้าที่บำรุงรักษาและตำแหน่งที่ทำงานที่กลุ่มเจ้าหน้าที่บำรุงรักษาที่เลือกเกี่ยวข้องด้วย</span><span class="sxs-lookup"><span data-stu-id="18351-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="18351-128">สร้างกลุ่มผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="18351-128">Create worker groups</span></span>

1. <span data-ttu-id="18351-129">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **ผู้ปฏิบัติงาน** \> **กลุ่มเจ้าหน้าที่บำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="18351-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="18351-130">เลือก **สร้าง** เพื่อเพิ่มกลุ่มผู้ปฏิบัติงานลงในรายการ</span><span class="sxs-lookup"><span data-stu-id="18351-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="18351-131">ในฟิลด์ **กลุ่มเจ้าหน้าที่บำรุงรักษา** ให้ป้อนรหัสกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="18351-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="18351-132">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="18351-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="18351-133">บน FastTab **ผู้ปฏิบัติงาน** ให้เลือก **เพิ่ม** แล้วจากนั้น เลือกกลุ่มเจ้าหน้าที่บำรุงรักษาสำหรับกลุ่มผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="18351-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="18351-134">สำหรับข้อมูลเกี่ยวกับฟิลด์ **มีผลบังคับใช้** และฟิลด์ **การหมดอายุ** ให้ดูที่ขั้นตอนที่ 6 ในกระบวนงานก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="18351-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="18351-135">ถ้ากลุ่มทรัพยากรควรเกี่ยวข้องกับกลุ่มเจ้าหน้าที่บำรุงรักษาที่เลือก ให้เลือก **คัดลอกจากกลุ่มทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="18351-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="18351-136">ในฟิลด์ **กลุ่ม** ให้เลือกกลุ่มทรัพยากรที่จะคัดลอกการตั้งค่าปฏิทินมา</span><span class="sxs-lookup"><span data-stu-id="18351-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="18351-137">จากนั้น ในฟิลด์ **กลุ่มผู้ปฏิบัติงาน** ให้เลือกกลุ่มผู้ปฏิบัติงานที่จะคัดลอกการตั้งค่าปฏิทินของกลุ่มทรัพยากรไป</span><span class="sxs-lookup"><span data-stu-id="18351-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="18351-138">ขั้นตอนนี้จะเกี่ยวข้องเฉพาะเมื่อคุณต้องการให้เจ้าหน้าที่บำรุงรักษาใช้ปฏิทินที่เกี่ยวข้องกับทรัพยากร (ศูนย์ควบคุมงาน) ในระหว่างการจัดกำหนดการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="18351-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="18351-139">ฟิลด์บน FastTab **รายละเอียด** แสดงจำนวนของเจ้าหน้าที่บำรุงรักษาที่ได้ถูกตั้งค่าในกลุ่มเจ้าหน้าที่บำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="18351-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>
