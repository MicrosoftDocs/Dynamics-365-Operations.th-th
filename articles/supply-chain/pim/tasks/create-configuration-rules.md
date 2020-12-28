---
title: สร้างกฏการปรับเปลี่ยน
description: 'กระบวนงานนี้สร้างกฎการจัดโครงสร้างที่จะใช้สำหรับการจัดโครงแบบตามมิติ เพื่อบังคับและป้องกันชุดบางอย่างของรายการ BOM '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bc0af4d95e9430d0b5c8b7fc9a4ade076802044
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438487"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="06ac0-103">สร้างกฏการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="06ac0-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06ac0-104">กระบวนงานนี้สร้างกฎการจัดโครงสร้างที่จะใช้สำหรับการจัดโครงแบบตามมิติ เพื่อบังคับและป้องกันชุดบางอย่างของรายการ BOM </span><span class="sxs-lookup"><span data-stu-id="06ac0-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="06ac0-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="06ac0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="06ac0-106">นี่เป็นกระบวนงานที่เจ็ดจากแปดกระบวนงาน ที่อธิบายวิธีการสร้างชุดสำหรับการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="06ac0-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="06ac0-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > สูตรและสูตรการผลิต > สูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="06ac0-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="06ac0-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="06ac0-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="06ac0-109">ให้ค้นหาและเลือก BOM หรับการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="06ac0-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="06ac0-110">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="06ac0-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="06ac0-111">คลิกเปลี่ยนมุมมอง</span><span class="sxs-lookup"><span data-stu-id="06ac0-111">Click Change view.</span></span>
5. <span data-ttu-id="06ac0-112">คลิกมุมมองหัวข้อ </span><span class="sxs-lookup"><span data-stu-id="06ac0-112">Click Header view.</span></span>
    * <span data-ttu-id="06ac0-113">เปิดมุมมองหัวข้อเพื่อเข้าถึงแท็บด่วนกระบวนการผลิตที่ปรับเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="06ac0-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="06ac0-114">ขยายหรือยุบส่วนกระบวนการผลิตที่ปรับเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="06ac0-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="06ac0-115">แท็บด่วนกระบวนการผลิตที่ปรับเปลี่ยนได้ต้องอยู่ในโหมดการขยาย</span><span class="sxs-lookup"><span data-stu-id="06ac0-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="06ac0-116">คลิกกฎการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="06ac0-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="06ac0-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="06ac0-117">Click New.</span></span>
9. <span data-ttu-id="06ac0-118">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="06ac0-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="06ac0-119">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="06ac0-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="06ac0-120">สินค้าในกลุ่มการปรับเปลี่ยนปัจจุบันจะแสดงขึ้น </span><span class="sxs-lookup"><span data-stu-id="06ac0-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="06ac0-121">เลือกรายการที่แสดงถึงเงื่อนไขในกฎ</span><span class="sxs-lookup"><span data-stu-id="06ac0-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="06ac0-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="06ac0-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="06ac0-123">ในฟิลด์วิธีการ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="06ac0-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="06ac0-124">เป็นไปได้ที่จะบังคับใช้การเลือกหรือยกเลิกการเลือกของสินค้าจากกลุ่มการปรับเปลี่ยนอื่น</span><span class="sxs-lookup"><span data-stu-id="06ac0-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="06ac0-125">ในฟิลด์กลุ่มที่ได้รับมา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="06ac0-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="06ac0-126">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="06ac0-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="06ac0-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="06ac0-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="06ac0-128">เลือกกลุ่มการปรับเปลี่ยนที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="06ac0-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="06ac0-129">ในฟิลด์หมายเลขสินค้าที่ได้รับมา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="06ac0-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="06ac0-130">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="06ac0-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="06ac0-131">เลือกหมายเลขสินค้าที่จะเลือกหรือยกเลิกการเลือกขึ้นอยู่กับวิธีการเลือก</span><span class="sxs-lookup"><span data-stu-id="06ac0-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="06ac0-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="06ac0-132">Close the page.</span></span>

