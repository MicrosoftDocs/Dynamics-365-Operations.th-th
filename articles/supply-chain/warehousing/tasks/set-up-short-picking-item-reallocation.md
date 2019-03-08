---
title: ตั้งค่าการปันส่วนใหม่ของสินค้าสำหรับการเบิกสินค้าที่ขาด
description: 'กระบวนงานนี้แสดงวิธีการอนุญาตให้ผู้ปฏิบัติงานคลังสินค้าสามารถค้นหาสถานที่อื่นได้อย่างรวดเร็วถ้าที่สถานที่ที่พวกเขาได้รับการสั่งการมีสินค้าคงคลังไม่เพียงพอ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf56a0811c4793ee2e3eaf78c8696c3c29e984c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "361233"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="ba3da-103">ตั้งค่าการปันส่วนใหม่ของสินค้าสำหรับการเบิกสินค้าที่ขาด</span><span class="sxs-lookup"><span data-stu-id="ba3da-103">Set up short picking item reallocation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba3da-104">กระบวนงานนี้แสดงวิธีการอนุญาตให้ผู้ปฏิบัติงานคลังสินค้าสามารถค้นหาสถานที่อื่นได้อย่างรวดเร็วถ้าที่สถานที่ที่พวกเขาได้รับการสั่งการมีสินค้าคงคลังไม่เพียงพอ </span><span class="sxs-lookup"><span data-stu-id="ba3da-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="ba3da-105">สามารถใช้กระบวนการปันส่วนใหม่โดยอัตโนมัติซึ่งจะใช้คำสั่งสถานที่ในการดึงข้อมูลสินค้าถ้าพร้อมใช้งานในสถานที่อื่น</span><span class="sxs-lookup"><span data-stu-id="ba3da-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="ba3da-106">อีกทางหนึ่งคือ เมื่อมีการใช้การปันส่วนใหม่ด้วยตนเอง รายการของสถานที่ที่มีปริมาณที่พร้อมใช้งานจะแสดงบนอุปกรณ์เคลื่อนที่ ซึ่งจะอนุญาตให้ผู้ปฏิบัติงานคลังสินค้าสามารถเลือกสถานที่ที่จะใช้สินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="ba3da-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="ba3da-107">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="ba3da-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="ba3da-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="ba3da-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="ba3da-109">ตั้งค่าข้อยกเว้นของงาน</span><span class="sxs-lookup"><span data-stu-id="ba3da-109">Set up work exceptions</span></span>
1. <span data-ttu-id="ba3da-110">ไปที่การจัดการคลังสินค้า > การตั้งค่า > งาน > ข้อยกเว้นของงาน</span><span class="sxs-lookup"><span data-stu-id="ba3da-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="ba3da-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ba3da-111">Click New.</span></span>
    * <span data-ttu-id="ba3da-112">สามารถกำหนดข้อยกเว้นของงานต่างๆ ด้วยนโยบายการปันส่วนใหม่ของสินค้าที่แตกต่างกันเพื่อให้ผู้ปฏิบัติงานคลังสินค้าสามารถเลือกตามความจำเป็นในการจัดส่งสินค้าที่กำลังประมวลผลอยู่</span><span class="sxs-lookup"><span data-stu-id="ba3da-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="ba3da-113">ในฟิลด์รหัสข้อยกเว้นของงาน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ba3da-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="ba3da-114">ตั้งชื่อข้อยกเว้นของงานเพื่อระบุว่าจะใช้สำหรับอะไร </span><span class="sxs-lookup"><span data-stu-id="ba3da-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="ba3da-115">ตัวอย่างเช่น การเบิกสินค้าที่ขาดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="ba3da-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="ba3da-116">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ba3da-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ba3da-117">ในฟิลด์ชนิดข้อยกเว้น เลือก 'การเบิกสินค้าที่ขาด'</span><span class="sxs-lookup"><span data-stu-id="ba3da-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="ba3da-118">เลือกกล่องกาเครื่องหมาย ปรับปรุงสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="ba3da-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="ba3da-119">ตัวเลือกนี้หมายความว่าสินค้าคงคลังจะถูกปรับปรุงเป็น 0 ที่สถานที่ที่มีการเบิกสินค้าที่ขาด</span><span class="sxs-lookup"><span data-stu-id="ba3da-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="ba3da-120">ในฟิลด์รหัสชนิดการปรับปรุงค่าเริ่มต้น ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ba3da-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="ba3da-121">ตัวอย่างเช่น ใน USMF คุณสามารถเลือก 'Remove Res Adj Out'</span><span class="sxs-lookup"><span data-stu-id="ba3da-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="ba3da-122">ในฟิลด์การปันส่วนใหม่ของสินค้า ให้เลือก 'ด้วยตนเอง'</span><span class="sxs-lookup"><span data-stu-id="ba3da-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="ba3da-123">ถ้าคุณเลือก ด้วยตนเอง หรือ โดยอัตโนมัติและด้วยตนเอง จะต้องอนุญาตให้ผู้ปฏิบัติงานคลังสินค้าสามารถใช้การปันส่วนด้วยตนเองใหม่</span><span class="sxs-lookup"><span data-stu-id="ba3da-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="ba3da-124">ตั้งค่าผู้ปฏิบัติงานที่จะใช้การปันส่วนสินค้าด้วยตนเองใหม่</span><span class="sxs-lookup"><span data-stu-id="ba3da-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="ba3da-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ba3da-125">Close the page.</span></span>
2. <span data-ttu-id="ba3da-126"> ไปที่การจัดการคลังสินค้า > การตั้งค่า > ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="ba3da-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="ba3da-127">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="ba3da-127">Click Edit.</span></span>
4. <span data-ttu-id="ba3da-128">ในรายการนี้ ให้เลือก ผู้ปฏิบัติงาน 24</span><span class="sxs-lookup"><span data-stu-id="ba3da-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="ba3da-129">ขยายส่วน งาน</span><span class="sxs-lookup"><span data-stu-id="ba3da-129">Expand the Work section.</span></span>
6. <span data-ttu-id="ba3da-130">เลือกใช่ในฟิลด์ อนุญาตการปันส่วนสินค้าด้วยตนเองใหม่</span><span class="sxs-lookup"><span data-stu-id="ba3da-130">Select Yes in the Allow manual item reallocation field.</span></span>

