---
title: สร้างแผนสำหรับไซต์
description: 'ผู้วางแผนการผลิตคำนวณความต้องการทางวัสดุและกำลังการผลิต สำหรับการผลิตสินค้าเฉพาะ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf3016e289248acafc3bc6b79d853fd9de8c5417
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841658"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="2d9b5-103">สร้างแผนสำหรับไซต์</span><span class="sxs-lookup"><span data-stu-id="2d9b5-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2d9b5-104">ผู้วางแผนการผลิตคำนวณความต้องการทางวัสดุและกำลังการผลิต สำหรับการผลิตสินค้าเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="2d9b5-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="2d9b5-105">หลังจากมีการสร้างคำแนะนำในการจัดหา จะพบใบสั่งสำหรับไซต์ที่กำลังวางแผนและยืนยันใบสั่ง ซึ่งเริ่มจากใบสั่งด่วน</span><span class="sxs-lookup"><span data-stu-id="2d9b5-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="2d9b5-106">ใบสั่งด่วนส่วนมากคือใบสั่งที่ต้องการการยืนยันในวันที่ปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="2d9b5-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="2d9b5-107">ใช้บริษัทข้อมูลสาธิต USMF เพื่อดำเนินงานเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2d9b5-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="2d9b5-108">สร้างแผนวัสดุและกำลังผลิตสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d9b5-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="2d9b5-109">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="2d9b5-109">Click Master planning.</span></span>
    * <span data-ttu-id="2d9b5-110">คุณต้องนำทางไปยังแดชบอร์ดเริมต้น</span><span class="sxs-lookup"><span data-stu-id="2d9b5-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="2d9b5-111">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="2d9b5-111">Click Run.</span></span>
3. <span data-ttu-id="2d9b5-112">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="2d9b5-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="2d9b5-113">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="2d9b5-113">Click Filter.</span></span>
5. <span data-ttu-id="2d9b5-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2d9b5-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="2d9b5-115">ในฟิลด์กรณี ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="2d9b5-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="2d9b5-116">ตัวอย่าง : D0001</span><span class="sxs-lookup"><span data-stu-id="2d9b5-116">Example: D0001</span></span>  
7. <span data-ttu-id="2d9b5-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2d9b5-117">Click OK.</span></span>
8. <span data-ttu-id="2d9b5-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2d9b5-118">Click OK.</span></span>
    * <span data-ttu-id="2d9b5-119">กระบวนการนี้อาจใช้เวลาหนึ่งถึงสองนาที</span><span class="sxs-lookup"><span data-stu-id="2d9b5-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="2d9b5-120">รีเฟรชหน้า</span><span class="sxs-lookup"><span data-stu-id="2d9b5-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="2d9b5-121">ระบุใบสั่งที่วางแผนไว้ด่วนสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d9b5-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="2d9b5-122">เปิดตัวกรองคอลัมน์หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d9b5-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="2d9b5-123">ใช้ตัวกรองในฟิลด์ "หมายเลขสินค้า" ด้วยค่า "D0001" โดยใช้ตัวดำเนินการตัวกรอง "เริ่มต้นด้วย"</span><span class="sxs-lookup"><span data-stu-id="2d9b5-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="2d9b5-124">เปิดตัวกรองคอลัมน์วันที่ของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="2d9b5-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="2d9b5-125">ใช้ตัวกรองในฟิลด์ "วันที่ใบสั่ง" ที่มีค่าของวันที่ปัจจุบัน โดยใช้ตัวดำเนินการตัวกรอง "ตรงทุกประการ"</span><span class="sxs-lookup"><span data-stu-id="2d9b5-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="2d9b5-126">ยืนยันใบสั่งด่วนสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="2d9b5-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="2d9b5-127">ในรายการนี้ ทำเครื่องหมายหรือยกเลิกการทำเครื่องหมายทุกแถว</span><span class="sxs-lookup"><span data-stu-id="2d9b5-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="2d9b5-128">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="2d9b5-128">Click Firm.</span></span>
3. <span data-ttu-id="2d9b5-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2d9b5-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]