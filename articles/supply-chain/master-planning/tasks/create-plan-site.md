---
title: สร้างแผนสำหรับไซต์
description: 'ผู้วางแผนการผลิตคำนวณความต้องการทางวัสดุและกำลังการผลิต สำหรับการผลิตสินค้าเฉพาะ '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52721d948554d4853f9e1d4dec45e45e619a4829
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438501"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="acf52-103">สร้างแผนสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="acf52-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="acf52-104">ผู้วางแผนการผลิตคำนวณความต้องการทางวัสดุและกำลังการผลิต สำหรับการผลิตสินค้าเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="acf52-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="acf52-105">หลังจากมีการสร้างคำแนะนำในการจัดหา จะพบใบสั่งสำหรับไซต์ที่กำลังวางแผนและยืนยันใบสั่ง ซึ่งเริ่มจากใบสั่งด่วน</span><span class="sxs-lookup"><span data-stu-id="acf52-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="acf52-106">ใบสั่งด่วนส่วนมากคือใบสั่งที่ต้องการการยืนยันในวันที่ปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="acf52-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="acf52-107">ใช้บริษัทข้อมูลสาธิต USMF เพื่อดำเนินงานเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="acf52-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="acf52-108">สร้างแผนวัสดุและกำลังผลิตสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="acf52-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="acf52-109">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="acf52-109">Click Master planning.</span></span>
    * <span data-ttu-id="acf52-110">คุณต้องนำทางไปยังแดชบอร์ดเริมต้น</span><span class="sxs-lookup"><span data-stu-id="acf52-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="acf52-111">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="acf52-111">Click Run.</span></span>
3. <span data-ttu-id="acf52-112">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="acf52-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="acf52-113">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="acf52-113">Click Filter.</span></span>
5. <span data-ttu-id="acf52-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="acf52-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="acf52-115">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="acf52-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="acf52-116">ตัวอย่าง : D0001</span><span class="sxs-lookup"><span data-stu-id="acf52-116">Example: D0001</span></span>  
7. <span data-ttu-id="acf52-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="acf52-117">Click OK.</span></span>
8. <span data-ttu-id="acf52-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="acf52-118">Click OK.</span></span>
    * <span data-ttu-id="acf52-119">กระบวนการนี้อาจใช้เวลาหนึ่งถึงสองนาที</span><span class="sxs-lookup"><span data-stu-id="acf52-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="acf52-120">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="acf52-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="acf52-121">ระบุใบสั่งที่วางแผนไว้ด่วนสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="acf52-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="acf52-122">เปิดตัวกรองคอลัมน์หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="acf52-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="acf52-123">ใช้ตัวกรองในฟิลด์ "หมายเลขสินค้า" ด้วยค่า "D0001" โดยใช้ตัวดำเนินการตัวกรอง "เริ่มต้นด้วย"</span><span class="sxs-lookup"><span data-stu-id="acf52-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="acf52-124">เปิดตัวกรองคอลัมน์วันที่ของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="acf52-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="acf52-125">ใช้ตัวกรองในฟิลด์ "วันที่ใบสั่ง" ที่มีค่าของวันที่ปัจจุบัน โดยใช้ตัวดำเนินการตัวกรอง "ตรงทุกประการ"</span><span class="sxs-lookup"><span data-stu-id="acf52-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="acf52-126">ยืนยันใบสั่งด่วนสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="acf52-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="acf52-127">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="acf52-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="acf52-128">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="acf52-128">Click Firm.</span></span>
3. <span data-ttu-id="acf52-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="acf52-129">Click OK.</span></span>

