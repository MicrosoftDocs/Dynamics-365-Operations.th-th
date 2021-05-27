---
title: โซนตรวจสอบสินค้าสำหรับความไม่สอดคล้องกัน
description: หัวข้อนี้จะอธิบายวิธีการสร้างและใช้โซนตรวจสอบสินค้าของความไม่สอดคล้องกัน
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f4b9dfc7882af4570bf1908784b8d114396402
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021815"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="23fbe-103">โซนตรวจสอบสินค้าสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="23fbe-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23fbe-104">หัวข้อนี้จะอธิบายวิธีการสร้างและใช้โซนตรวจสอบสินค้าของความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="23fbe-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="23fbe-105">คุณใช้หน้า **โซนตรวจสอบสินค้า** เพื่อกำหนดโซนที่สามารถกำหนดให้กับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="23fbe-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="23fbe-106">เมื่อคุณสร้างความไม่สอดคล้องกัน คุณสามารถตั้งค่าฟิลด์ **โซนตรวจสอบสินค้า** และ **ชนิดการตรวจสอบสินค้า** บนแท็บ **ทั่วไป** ของหน้า **ความไม่สอดคล้องกัน** ได้</span><span class="sxs-lookup"><span data-stu-id="23fbe-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="23fbe-107">โดยทั่วไป ฟิลด์ **โซนตรวจสอบสินค้า** จะบ่งชี้พื้นที่หรือที่ตั้งที่สินค้าตั้งอยู่</span><span class="sxs-lookup"><span data-stu-id="23fbe-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="23fbe-108">ฟิลด์ **ชนิดการตรวจสอบสินค้า** จะกําหนดสินค้าเป็น *การใช้งานที่จำกัด* หรือ *การใช้งานที่ใช้ไม่ได้*</span><span class="sxs-lookup"><span data-stu-id="23fbe-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="23fbe-109">เมื่อคุณพิมพ์รายงานความไม่สอดคล้องกันหรือรายงานการแก้ไขความไม่สอดคล้องกัน คุณสามารถดูโซนตรวจสอบสินค้าที่สินค้าตั้งอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="23fbe-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="23fbe-110">คุณยังสามารถพิมพ์ป้ายความไม่สอดคล้องกันของความไม่สอดคล้องกันได้</span><span class="sxs-lookup"><span data-stu-id="23fbe-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="23fbe-111">รายงานนี้แสดงโซนตรวจสอบสินค้าที่กำหนดไว้และข้อมูลเกี่ยวกับการใช้งาน เพื่อให้คำแนะนำวิธีการจัดการกับวัสดุที่บกพร่อง</span><span class="sxs-lookup"><span data-stu-id="23fbe-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="23fbe-112">โซนตรวจสอบสินค้าอาจสอดคล้องกับสถานที่เก็บสินค้าคงคลังหรือทรัพยากรการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="23fbe-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="23fbe-113">ตัวอย่างของโซนการตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="23fbe-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="23fbe-114">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="23fbe-114">Example 1</span></span>

<span data-ttu-id="23fbe-115">คุณทำงานที่บริษัทผู้ผลิตอุปกรณ์อิเล็กทรอนิกส์ ซึ่งผลิตและแจกจ่ายโทรทัศน์ ลําโพง และตัวเล่นสื่อ</span><span class="sxs-lookup"><span data-stu-id="23fbe-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="23fbe-116">ในกรณีนี้ คุณสามารถตั้งค่าคอนฟิกโซนตรวจสอบสินค้าเพื่อแสดงถึงผลิตภัณฑ์แต่ละชนิดได้</span><span class="sxs-lookup"><span data-stu-id="23fbe-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="23fbe-117">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="23fbe-117">Example 2</span></span>

<span data-ttu-id="23fbe-118">ช่องเก็บสามช่องเก็บและชั้นเก็บสินค้าสองชั้นใช้ในการจัดเก็บสินค้าที่ไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="23fbe-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="23fbe-119">ในกรณีนี้ คุณสามารถตั้งค่าคอนฟิกโซนตรวจสอบสินค้าได้ห้าโซน หนึ่งโซนต่อช่องเก็บแต่ละช่องเก็บและชั้นเก็บสินค้าแต่ละชั้น</span><span class="sxs-lookup"><span data-stu-id="23fbe-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="23fbe-120">สร้างโซนตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="23fbe-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="23fbe-121">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การจัดการคุณภาพ \> โซนการตรวจสอบสินค้า**</span><span class="sxs-lookup"><span data-stu-id="23fbe-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="23fbe-122">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="23fbe-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="23fbe-123">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="23fbe-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="23fbe-124">**โซนตรวจสอบสินค้า** – ป้อนรหัสหรือชื่อเฉพาะของโซนตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="23fbe-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="23fbe-125">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของโซนตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="23fbe-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="23fbe-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="23fbe-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23fbe-127">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="23fbe-127">Additional resources</span></span>

- [<span data-ttu-id="23fbe-128">ภาพรวมของการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="23fbe-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="23fbe-129">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="23fbe-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="23fbe-130">ผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="23fbe-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="23fbe-131">ชนิดของปัญหาสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="23fbe-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="23fbe-132">ชนิดของการวินิจฉัยสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="23fbe-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="23fbe-133">ค่าธรรมเนียมคุณภาพสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="23fbe-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="23fbe-134">การดำเนินงานสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="23fbe-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="23fbe-135">การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="23fbe-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
