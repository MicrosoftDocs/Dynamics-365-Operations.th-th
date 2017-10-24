---
title: "การจัดกลุ่มระบบในรายการงานที่เปิด"
description: "หัวข้อนี้อธิบายวิธีการกรองรายการงานที่เปิดบนอุปกรณ์เคลื่อนที่"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c68d544fec985f325e6472203533f23948cc9b4
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="05e51-103">การจัดกลุ่มระบบในรายการงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="05e51-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="05e51-104">โดยการใช้ฟิลด์การจัดกลุ่มของระบบ คุณสามารถกรองข้อมูลในรายการงานที่เปิดโดยไม่ต้องแก้ไขเมนูของอุปกรณ์เคลื่อน</span><span class="sxs-lookup"><span data-stu-id="05e51-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="05e51-105">กรณีที่ใช้งานการจัดกลุ่มระบบสำหรับการกรองรายการงานบนฟิลด์หัวข้องานเดียว</span><span class="sxs-lookup"><span data-stu-id="05e51-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="05e51-106">คุณไม่สามารถใช้ระบบการจัดกลุ่มกับตัวกรองบนฟิลด์ระดับของรายการ</span><span class="sxs-lookup"><span data-stu-id="05e51-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="05e51-107">ตั้งค่าการจัดกลุ่มของระบบในรายการงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="05e51-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="05e51-108">ใช้ขั้นตอนเหล่านี้ในการตั้งค่าการจัดกลุ่มของระบบในรายการงานที่เปิด</span><span class="sxs-lookup"><span data-stu-id="05e51-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="05e51-109">จากรายการเมนูบนอุปกรณ์เคลื่อนที่ เลือก **โหมด: ทางอ้อม** และ **รหัสกิจกรรม: แสดงรายการงานที่เปิด**</span><span class="sxs-lookup"><span data-stu-id="05e51-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="05e51-110">ตัวเลือกดังต่อไปนี้สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="05e51-110">The following options become available.</span></span> <span data-ttu-id="05e51-111">ตัวเลือกเหล่านี้จำเป็นต้องใช้สำหรับการจัดกลุ่มของระบบโดยใช้รายการงานที่เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="05e51-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="05e51-112">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="05e51-112">Option</span></span>        | <span data-ttu-id="05e51-113">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="05e51-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="05e51-114">อนุญาตการจัดกลุ่มของระบบ</span><span class="sxs-lookup"><span data-stu-id="05e51-114">Allow system grouping</span></span>   | <span data-ttu-id="05e51-115">เปิดใช้งานระบบการจัดกลุ่มสำหรับรายการเมนูของรายการงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="05e51-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="05e51-116">ฟิลด์การจัดกลุ่มระบบ</span><span class="sxs-lookup"><span data-stu-id="05e51-116">System grouping field</span></span>   | <span data-ttu-id="05e51-117">พร้อมใช้งานได้ก็ต่อเมื่อ **อนุญาตงานของระบบ** ตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="05e51-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="05e51-118">เลือกฟิลด์ที่จะกำหนดวิธีการจัดกลุ่มงานการเบิกสินค้าสำหรับผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="05e51-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="05e51-119">ตัวอย่างเช่น ถ้าคุณเลือกฟิลด์ **ShipmentId** ผู้ปฏิบัติงานจะสแกนรหัสการจัดส่งเพื่อจัดกลุ่มงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="05e51-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="05e51-120">งานทั้งหมดสำหรับการจัดส่งนั้นถูกกำหนดให้กับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="05e51-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="05e51-121">ฟิลด์นี้ต้องระบุว่าคุณสร้างรายการเมนูที่ใช้งานที่มีอยู่ที่ถูกจัดกลุ่มโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="05e51-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="05e51-122">ใช้ฟิลด์ **ป้ายชื่อการจัดกลุ่มระบบ** เพื่อแจ้งให้ผู้ปฏิบัติงานทราบถึงสิ่งที่ต้องสแกน</span><span class="sxs-lookup"><span data-stu-id="05e51-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="05e51-123">ป้ายชื่อการจัดกลุ่มระบบ</span><span class="sxs-lookup"><span data-stu-id="05e51-123">System grouping label</span></span>   | <span data-ttu-id="05e51-124">พร้อมใช้งานได้ก็ต่อเมื่อ **อนุญาตงานของระบบ** ตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="05e51-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="05e51-125">ป้อนข้อมูลสำหรับผู้ปฏิบัติงานเกี่ยวกับสิ่งที่ต้องสแกนเมื่อทำการเบิกสินค้าจะจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="05e51-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="05e51-126">ตัวอย่างเช่น ถ้าคุณใช้ฟิลด์ **ShipmentId** เพื่อจัดกลุ่มงานการเบิกสินค้าโดยการจัดส่ง คุณอาจป้อน Shipment ID ในฟิลด์</span><span class="sxs-lookup"><span data-stu-id="05e51-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="05e51-127">ฟิลด์นี้ต้องระบุว่าคุณสร้างรายการเมนูที่ใช้งานที่มีอยู่ที่ถูกจัดกลุ่มโดยระบบ</span><span class="sxs-lookup"><span data-stu-id="05e51-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="05e51-128">คุณต้องเลือกฟิลด์เพื่อจัดกลุ่มตามฟิลด์ **การจัดกลุ่มระบบ**</span><span class="sxs-lookup"><span data-stu-id="05e51-128">You must also select the field to group by in the **System grouping** field.</span></span>|

