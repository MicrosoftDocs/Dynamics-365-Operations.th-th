---
title: ตั้งค่าการปันส่วนใหม่ของสินค้าสำหรับการเบิกสินค้าที่ขาด
description: กระบวนงานนี้แสดงวิธีการอนุญาตให้ผู้ปฏิบัติงานคลังสินค้าสามารถค้นหาสถานที่สำรองได้อย่างรวดเร็ว ถ้ามีสินค้าคงคลังไม่เพียงพอที่สถานที่ที่พวกเขาได้รับการสั่งการให้ไป
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e860a54c2306f8140947b77cdcb538160a84e06f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216824"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="8b3c8-103">ตั้งค่าการปันส่วนใหม่ของสินค้าสำหรับการเบิกสินค้าที่ขาด</span><span class="sxs-lookup"><span data-stu-id="8b3c8-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b3c8-104">กระบวนงานนี้แสดงวิธีการอนุญาตให้ผู้ปฏิบัติงานคลังสินค้าสามารถค้นหาสถานที่สำรองได้อย่างรวดเร็ว ถ้ามีสินค้าคงคลังไม่เพียงพอที่สถานที่ที่พวกเขาได้รับการสั่งการให้ไป</span><span class="sxs-lookup"><span data-stu-id="8b3c8-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn't sufficient inventory at the location they've been directed to.</span></span> <span data-ttu-id="8b3c8-105">สามารถใช้กระบวนการปันส่วนใหม่แบบอัตโนมัติ ซึ่งจะใช้คำสั่งสถานที่ในการดึงข้อมูลสินค้า ถ้าพร้อมใช้งานในสถานที่อื่น</span><span class="sxs-lookup"><span data-stu-id="8b3c8-105">It's possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they're available at another location.</span></span> <span data-ttu-id="8b3c8-106">อีกทางหนึ่งคือ เมื่อมีการใช้การปันส่วนใหม่ด้วยตนเอง รายการของสถานที่ที่มีปริมาณที่พร้อมใช้งานจะแสดงบนอุปกรณ์เคลื่อนที่ ซึ่งจะอนุญาตให้ผู้ปฏิบัติงานคลังสินค้าสามารถเลือกสถานที่ที่จะใช้สินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="8b3c8-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="8b3c8-107">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="8b3c8-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="8b3c8-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="8b3c8-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="8b3c8-109">ตั้งค่าข้อยกเว้นของงาน</span><span class="sxs-lookup"><span data-stu-id="8b3c8-109">Set up work exceptions</span></span>
1. <span data-ttu-id="8b3c8-110">ใน **บานหน้าต่างนำทาง** ไปที่ **การจัดการคลังสินค้า > การตั้งค่า > งาน > ข้อยกเว้นของงาน**</span><span class="sxs-lookup"><span data-stu-id="8b3c8-110">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="8b3c8-111">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8b3c8-111">Click **New**.</span></span> <span data-ttu-id="8b3c8-112">สามารถกำหนดข้อยกเว้นของงานต่างๆ ด้วยนโยบายการปันส่วนใหม่ของสินค้าที่แตกต่างกัน เพื่อให้ผู้ปฏิบัติงานคลังสินค้าสามารถเลือกได้ตามความจำเป็นในการจัดส่งสินค้าที่กำลังประมวลผลอยู่</span><span class="sxs-lookup"><span data-stu-id="8b3c8-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="8b3c8-113">ในฟิลด์ **รหัสข้อยกเว้นของงาน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8b3c8-113">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="8b3c8-114">ตั้งชื่อข้อยกเว้นของงานเพื่อระบุว่าจะใช้สำหรับอะไร</span><span class="sxs-lookup"><span data-stu-id="8b3c8-114">Give the work exception a title to indicate what it's used for.</span></span> <span data-ttu-id="8b3c8-115">ตัวอย่างเช่น การเบิกสินค้าที่ขาดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="8b3c8-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="8b3c8-116">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8b3c8-116">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="8b3c8-117">ในฟิลด์ชนิด **ข้อยกเว้น** เลือก 'การเบิกสินค้าที่ขาด'</span><span class="sxs-lookup"><span data-stu-id="8b3c8-117">In the **Exception** type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="8b3c8-118">เลือกกล่องกาเครื่องหมาย **ปรับปรุงสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="8b3c8-118">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="8b3c8-119">ตัวเลือกนี้หมายความว่าสินค้าคงคลังจะถูกปรับปรุงเป็น 0 ที่สถานที่ที่มีการเบิกสินค้าที่ขาด</span><span class="sxs-lookup"><span data-stu-id="8b3c8-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="8b3c8-120">ในฟิลด์ **รหัสชนิดการปรับปรุงค่าเริ่มต้น** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="8b3c8-120">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="8b3c8-121">ตัวอย่างเช่น ใน USMF คุณสามารถเลือก 'Remove Res Adj Out'</span><span class="sxs-lookup"><span data-stu-id="8b3c8-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="8b3c8-122">ในฟิลด์ **การปันส่วนใหม่ของสินค้า** ให้เลือก 'ด้วยตนเอง'</span><span class="sxs-lookup"><span data-stu-id="8b3c8-122">In the **Item reallocation** field, select 'Manual'.</span></span> <span data-ttu-id="8b3c8-123">ถ้าคุณเลือก ด้วยตนเอง หรือ โดยอัตโนมัติและด้วยตนเอง จะต้องอนุญาตให้ผู้ปฏิบัติงานคลังสินค้าสามารถใช้การปันส่วนด้วยตนเองใหม่</span><span class="sxs-lookup"><span data-stu-id="8b3c8-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="8b3c8-124">ตั้งค่าผู้ปฏิบัติงานที่จะใช้การปันส่วนสินค้าด้วยตนเองใหม่</span><span class="sxs-lookup"><span data-stu-id="8b3c8-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="8b3c8-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8b3c8-125">Close the page.</span></span>
2. <span data-ttu-id="8b3c8-126">ใน **บานหน้าต่างนำทาง** ไปที่ **การจัดการคลังสินค้า > การตั้งค่า > งาน > ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="8b3c8-126">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="8b3c8-127">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8b3c8-127">Click **Edit**.</span></span>
4. <span data-ttu-id="8b3c8-128">ในรายการนี้ ให้เลือก ผู้ปฏิบัติงาน 24</span><span class="sxs-lookup"><span data-stu-id="8b3c8-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="8b3c8-129">ขยาย fastTab **งาน**</span><span class="sxs-lookup"><span data-stu-id="8b3c8-129">Expand the **Work** fastTab.</span></span>
6. <span data-ttu-id="8b3c8-130">เลือก 'ใช่' ในฟิลด์ **อนุญาตการปันส่วนสินค้าด้วยตนเองใหม่**</span><span class="sxs-lookup"><span data-stu-id="8b3c8-130">Select 'Yes' in the **Allow manual item reallocation** field.</span></span>

