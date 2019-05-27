---
title: ตั้งค่านโยบายงานของคลังสินค้า (ใบสมัคร พฤษภาคม 2016)
description: กระบวนการคลังสินค้าไม่รวมงานคลังสินค้าเสมอไป
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34b4255c85bb53f7e238b60559890571070953a6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569090"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="5865f-103">ตั้งค่านโยบายงานของคลังสินค้า (ใบสมัคร พฤษภาคม 2016)</span><span class="sxs-lookup"><span data-stu-id="5865f-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5865f-104">กระบวนการคลังสินค้าไม่รวมงานคลังสินค้าเสมอไป</span><span class="sxs-lookup"><span data-stu-id="5865f-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="5865f-105">โดยการกำหนดนโยบายงาน คุณสามารถป้องกันการสร้างงานสำหรับการเบิกวัตถุดิบและการสำรองสินค้าสำเร็จรูป สำหรับชุดของผลิตภัณฑ์ที่ตำแหน่งเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="5865f-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="5865f-106">บริษัทข้อมูลสาธิต USMF ถูกนำมาใช้เพื่อสร้างการบันทึกนี้</span><span class="sxs-lookup"><span data-stu-id="5865f-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="5865f-107">คำแนะนำงานนี้ต้องการแอพลิเคชัน Dynamics AX 7.0.1 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="5865f-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="5865f-108">ไปที่การจัดการคลังสินค้า > ตั้งค่า > งาน > นโยบายงาน</span><span class="sxs-lookup"><span data-stu-id="5865f-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="5865f-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5865f-109">Click New.</span></span>
3. <span data-ttu-id="5865f-110">ในฟิลด์ชื่อนโยบายงาน ให้พิมพ์ 'ไม่มีงานการย้ายเก็บ'</span><span class="sxs-lookup"><span data-stu-id="5865f-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="5865f-111">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="5865f-111">Click Save.</span></span>
5. <span data-ttu-id="5865f-112">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5865f-112">Click Add.</span></span>
6. <span data-ttu-id="5865f-113">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5865f-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="5865f-114">ในฟิลด์ชนิดใบสั่งงาน ให้เลือก 'การสำรองสินค้าที่สำเร็จแล้ว'</span><span class="sxs-lookup"><span data-stu-id="5865f-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="5865f-115">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5865f-115">Click Add.</span></span>
9. <span data-ttu-id="5865f-116">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5865f-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="5865f-117">ในฟิลด์ชนิดใบสั่งงาน ให้เลือก 'การสำรองผลิตภัณฑ์ร่วมและสินค้าพลอยได้'</span><span class="sxs-lookup"><span data-stu-id="5865f-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="5865f-118">ขยายส่วนสถานที่เก็บสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="5865f-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="5865f-119">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5865f-119">Click Add.</span></span>
13. <span data-ttu-id="5865f-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5865f-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="5865f-121">ในรายการคลังสินค้า ป้อน '51'</span><span class="sxs-lookup"><span data-stu-id="5865f-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="5865f-122">ในฟิลด์สถานที่ ให้ป้อนหรือเลือก '001'</span><span class="sxs-lookup"><span data-stu-id="5865f-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="5865f-123">ขยายส่วนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5865f-123">Expand the Products section.</span></span>
17. <span data-ttu-id="5865f-124">ในฟิลด์การเลือกผลิตภัณฑ์ ให้ป้อน 'เลือกแล้ว'</span><span class="sxs-lookup"><span data-stu-id="5865f-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="5865f-125">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="5865f-125">Click Add.</span></span>
19. <span data-ttu-id="5865f-126">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5865f-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="5865f-127">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือก 'L0101'</span><span class="sxs-lookup"><span data-stu-id="5865f-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="5865f-128">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="5865f-128">Click Save.</span></span>

