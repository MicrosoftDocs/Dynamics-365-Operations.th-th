--- 
title: "สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล"
description: "กระบวนงานนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ดเพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับแต่ละเรกคอร์ดใหม่"
author: sericks007
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 968f3473198de5aee0b32baf3a83839aeea73835
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="c1f1a-103">สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c1f1a-103">Create a record template to facilitate data entry</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1f1a-104">กระบวนงานนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ดเพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับแต่ละเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="c1f1a-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="c1f1a-105">ในกระบวนงานนี้ คุณจะสร้างเรกคอร์ดใหม่สำหรับแล็ปท็อปใหม่ที่ควรถูกเพิ่มในสินทรัพย์ถาวรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c1f1a-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="c1f1a-106">กระบวนงานนี้ใช้บริษัทตัวอย่าง USMF</span><span class="sxs-lookup"><span data-stu-id="c1f1a-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="c1f1a-107">ไปที่ สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="c1f1a-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="c1f1a-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c1f1a-108">Click New.</span></span>
3. <span data-ttu-id="c1f1a-109">ในฟิลด์กลุ่มสินทรัพย์ถาวร ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c1f1a-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="c1f1a-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="c1f1a-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c1f1a-111">ตัวอย่างเช่น ป้อน 'Corporate lead laptop'</span><span class="sxs-lookup"><span data-stu-id="c1f1a-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="c1f1a-112">ในฟิลด์ชื่อสำหรับค้นหา ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c1f1a-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="c1f1a-113">ตัวอย่างเช่น ป้อน 'laptop'</span><span class="sxs-lookup"><span data-stu-id="c1f1a-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="c1f1a-114">ขยายส่วนข้อมูลทางเทคนิค</span><span class="sxs-lookup"><span data-stu-id="c1f1a-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="c1f1a-115">ในฟิลด์ยี่ห้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c1f1a-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="c1f1a-116">ในฟิลด์แบบจำลอง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c1f1a-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="c1f1a-117">ในฟิลด์ปีของรุ่น ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c1f1a-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="c1f1a-118">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c1f1a-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="c1f1a-119">คลิก ข้อมูลของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c1f1a-119">Click Record info.</span></span>
12. <span data-ttu-id="c1f1a-120">คลิก เท็มเพลตผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c1f1a-120">Click User template.</span></span>
13. <span data-ttu-id="c1f1a-121">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="c1f1a-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c1f1a-122">ตัวอย่างเช่น ป้อน 'Corporate laptop'</span><span class="sxs-lookup"><span data-stu-id="c1f1a-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="c1f1a-123">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c1f1a-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c1f1a-124">ตัวอย่างเช่น ป้อน 'Corporate laptop'</span><span class="sxs-lookup"><span data-stu-id="c1f1a-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="c1f1a-125">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="c1f1a-125">Click OK.</span></span>
16. <span data-ttu-id="c1f1a-126">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="c1f1a-126">Click Close.</span></span>


