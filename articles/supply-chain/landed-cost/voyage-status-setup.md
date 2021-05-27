---
title: การตั้งค่าสถานะการเดินทาง
description: หัวข้อนี้จะอธิบายวิธีการสร้างค่าสถานะที่ผู้ใช้สามารถกําหนดให้กับการเดินทาง
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e19a54fc9de166c93fd68408ca8c8c692dc96cab
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022119"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="bb0bc-103">การตั้งค่าสถานะการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="bb0bc-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb0bc-104">ในหน้า **สถานะการเดินทาง** คุณกําหนดชุดค่าสถานะที่ผู้ใช้สามารถกําหนดให้กับการเดินทางได้</span><span class="sxs-lookup"><span data-stu-id="bb0bc-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="bb0bc-105">ผู้ใช้สามารถกําหนดค่าสถานะการเดินทางให้กับทุกระดับของการเดินทาง: การเดินทาง คอนเทนเนอร์การจัดส่ง ใบแจ้งรายการ ใบสั่งซื้อ และสินค้า (รายการการซื้อและรายการใบสั่งโอนย้าย)</span><span class="sxs-lookup"><span data-stu-id="bb0bc-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="bb0bc-106">ซึ่งใช้เพื่อวัตถุประสงค์สองอย่างคือ</span><span class="sxs-lookup"><span data-stu-id="bb0bc-106">They are used for two purposes:</span></span>

- <span data-ttu-id="bb0bc-107">แจ้งให้ผู้ใช้ทราบเกี่ยวกับสถานะของการเดินทาง คอนเทนเนอร์จัดส่ง ใบแจ้งรายการ ใบสั่งซื้อ หรือสินค้า (รายการซื้อและรายการใบสั่งโอนย้าย)</span><span class="sxs-lookup"><span data-stu-id="bb0bc-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="bb0bc-108">จํากัดการใช้พื้นที่ต้นทุนโดยป้องกันการแก้ไขหรือลบ</span><span class="sxs-lookup"><span data-stu-id="bb0bc-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="bb0bc-109">เมื่อต้องการตั้งค่าสถานะการเดินทางของคุณ ให้ไปที่ **ต้นทุนแฝง \> การตั้งค่า \> สถานะการเดินทาง**</span><span class="sxs-lookup"><span data-stu-id="bb0bc-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="bb0bc-110">คุณสามารถเพิ่ม ลบ และแก้ไขสถานะได้ใช้ปุ่มต่างๆ ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="bb0bc-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="bb0bc-111">พื้นที่ต้นทุนแต่ละพื้นที่จะมีการตั้งค่าและระดับของสถานะการเดินทางของตนเอง</span><span class="sxs-lookup"><span data-stu-id="bb0bc-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="bb0bc-112">ดังนั้น ในหน้า **สถานะการเดินทาง** ในฟิลด์ **พื้นที่ต้นทุน** คุณต้องเลือกพื้นที่ต้นทุนที่คุณต้องการดูหรือสร้างสถานะการเดินทางให้ก่อน</span><span class="sxs-lookup"><span data-stu-id="bb0bc-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="bb0bc-113">จากนั้นสำหรับแต่ละแต่ละสถานะการเดินทาง ให้ตั้งค่าฟิลด์ที่อธิบายไว้ในตารางต่อไปนี้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="bb0bc-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="bb0bc-114">โปรดทราบว่าสถานะของการเดินทางยังสามารถเปลี่ยนแปลงโดยอัตโนมัติโดยเหตุการณ์ของระบบ เช่น กฎที่สร้างขึ้นโดยการใช้ศูนย์ควบคุมการติดตาม</span><span class="sxs-lookup"><span data-stu-id="bb0bc-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="bb0bc-115">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="bb0bc-115">Field</span></span> | <span data-ttu-id="bb0bc-116">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bb0bc-116">Description</span></span> |
|---|---|
| <span data-ttu-id="bb0bc-117">สถานะการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="bb0bc-117">Voyage status</span></span> | <span data-ttu-id="bb0bc-118">ป้อนชื่อของสถานะการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="bb0bc-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="bb0bc-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bb0bc-119">Description</span></span> | <span data-ttu-id="bb0bc-120">ป้อนคำอธิบายเกี่ยวกับสถานะการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="bb0bc-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="bb0bc-121">แก้ไข</span><span class="sxs-lookup"><span data-stu-id="bb0bc-121">Modify</span></span> | <span data-ttu-id="bb0bc-122">เลือกกล่องกาเครื่องหมายนี้ถ้าผู้ใช้ได้รับอนุญาตให้แก้ไขการเดินทางที่มีสถานะนี้</span><span class="sxs-lookup"><span data-stu-id="bb0bc-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="bb0bc-123">Delete</span><span class="sxs-lookup"><span data-stu-id="bb0bc-123">Delete</span></span> | <span data-ttu-id="bb0bc-124">เลือกกล่องกาเครื่องหมายนี้ถ้าผู้ใช้ได้รับอนุญาตให้ลบการเดินทางที่มีสถานะนี้</span><span class="sxs-lookup"><span data-stu-id="bb0bc-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="bb0bc-125">จำเป็น</span><span class="sxs-lookup"><span data-stu-id="bb0bc-125">Mandatory</span></span> | <span data-ttu-id="bb0bc-126">เลือกกล่องกาเครื่องหมายนี้เพื่อเปลี่ยนแปลงสถานะการเดินทางเป็นสถานะบังคับ ดังนั้นจึงไม่สามารถข้ามได้</span><span class="sxs-lookup"><span data-stu-id="bb0bc-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="bb0bc-127">หลัก</span><span class="sxs-lookup"><span data-stu-id="bb0bc-127">Parent</span></span> | <span data-ttu-id="bb0bc-128">ใช้ฟิลด์นี้เพื่อสร้างลำดับชั้นในบรรดาค่าสถานะ</span><span class="sxs-lookup"><span data-stu-id="bb0bc-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="bb0bc-129">สถานะการเดินทางสามารถเปลี่ยนแปลงได้ (อาจเป็นด้วยตนเองหรือโดยอัตโนมัติ) เฉพาะในลำดับชั้น จากสถานะหลักเป็นสถานะรองสถานะใดสถานะหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bb0bc-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="bb0bc-130">คุณต้องตั้งค่าเฉพาะสถานะการเดินทางเฉพาะที่องค์กรของคุณใช้</span><span class="sxs-lookup"><span data-stu-id="bb0bc-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="bb0bc-131">สถานะการเดินทางโดยทั่วไป ได้แก่ *ยืนยันแล้ว* *สินค้าที่อยู่ระหว่างส่งต่อ* *ได้รับแล้ว* *พร้อมคิดต้นทุน* และ *คิดต้นทุน*</span><span class="sxs-lookup"><span data-stu-id="bb0bc-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="bb0bc-132">อย่างไรก็ตาม สถานะอื่น ๆ อาจแสดงอยู่</span><span class="sxs-lookup"><span data-stu-id="bb0bc-132">However, other statuses might be present.</span></span>
