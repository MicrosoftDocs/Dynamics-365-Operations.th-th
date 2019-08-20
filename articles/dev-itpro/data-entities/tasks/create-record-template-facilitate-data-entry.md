---
title: สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล
description: กระบวนงานนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ดเพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับแต่ละเรกคอร์ดใหม่
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b2ba56b6146f2495fb6a53c3cef9f549b1ad837
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848218"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="dfe4b-103">สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dfe4b-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dfe4b-104">กระบวนงานนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ดเพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับแต่ละเรกคอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="dfe4b-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="dfe4b-105">ในกระบวนงานนี้ คุณจะสร้างเรกคอร์ดใหม่สำหรับแล็ปท็อปใหม่ที่ควรถูกเพิ่มในสินทรัพย์ถาวรของคุณ</span><span class="sxs-lookup"><span data-stu-id="dfe4b-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="dfe4b-106">กระบวนงานนี้ใช้บริษัทตัวอย่าง USMF</span><span class="sxs-lookup"><span data-stu-id="dfe4b-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="dfe4b-107">ไปที่ สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="dfe4b-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="dfe4b-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="dfe4b-108">Click New.</span></span>
3. <span data-ttu-id="dfe4b-109">ในฟิลด์กลุ่มสินทรัพย์ถาวร ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="dfe4b-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="dfe4b-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="dfe4b-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="dfe4b-111">ตัวอย่างเช่น ป้อน 'Corporate lead laptop'</span><span class="sxs-lookup"><span data-stu-id="dfe4b-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="dfe4b-112">ในฟิลด์ชื่อสำหรับค้นหา ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dfe4b-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="dfe4b-113">ตัวอย่างเช่น ป้อน 'laptop'</span><span class="sxs-lookup"><span data-stu-id="dfe4b-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="dfe4b-114">ขยายส่วนข้อมูลทางเทคนิค</span><span class="sxs-lookup"><span data-stu-id="dfe4b-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="dfe4b-115">ในฟิลด์ยี่ห้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dfe4b-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="dfe4b-116">ในฟิลด์แบบจำลอง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dfe4b-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="dfe4b-117">ในฟิลด์ปีของรุ่น ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dfe4b-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="dfe4b-118">ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="dfe4b-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="dfe4b-119">คลิก ข้อมูลของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="dfe4b-119">Click Record info.</span></span>
12. <span data-ttu-id="dfe4b-120">คลิก เท็มเพลตผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="dfe4b-120">Click User template.</span></span>
13. <span data-ttu-id="dfe4b-121">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="dfe4b-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="dfe4b-122">ตัวอย่างเช่น ป้อน 'Corporate laptop'</span><span class="sxs-lookup"><span data-stu-id="dfe4b-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="dfe4b-123">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="dfe4b-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="dfe4b-124">ตัวอย่างเช่น ป้อน 'Corporate laptop'</span><span class="sxs-lookup"><span data-stu-id="dfe4b-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="dfe4b-125">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="dfe4b-125">Click OK.</span></span>
16. <span data-ttu-id="dfe4b-126">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="dfe4b-126">Click Close.</span></span>

