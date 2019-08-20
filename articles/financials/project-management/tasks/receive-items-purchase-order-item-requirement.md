---
title: รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า
description: กระบวนงานนี้แสดงวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fee2c965b0c065f00564b849ec93504336fb3f60
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838258"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="71aa7-103">รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="71aa7-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71aa7-104">กระบวนงานนี้แสดงวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="71aa7-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="71aa7-105">โดยการใช้ข้อกำหนดรายการแทนธุรกรรมรายการ คุณสามารถวางแผนให้กับการส่งมอบก่อนการใช้รายการจริง สร้างใบสั่งซื้อ รวมรายการในโครงงานข้อตกลงการค้า และรวมในข้อกำหนดรายการในการวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="71aa7-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="71aa7-106">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="71aa7-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="71aa7-107">ไปที่การจัดการโครงการและการบัญชี > โครงการ > โครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="71aa7-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="71aa7-108">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="71aa7-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="71aa7-109">ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน</span><span class="sxs-lookup"><span data-stu-id="71aa7-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="71aa7-110">คลิก ความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="71aa7-110">Click Item requirements.</span></span>
5. <span data-ttu-id="71aa7-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="71aa7-111">Click New.</span></span>
6. <span data-ttu-id="71aa7-112">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="71aa7-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="71aa7-113">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="71aa7-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="71aa7-114">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="71aa7-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="71aa7-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="71aa7-115">Click Save.</span></span>
10. <span data-ttu-id="71aa7-116">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="71aa7-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="71aa7-117">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="71aa7-117">Click Functions.</span></span>
12. <span data-ttu-id="71aa7-118">คลิก สร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="71aa7-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="71aa7-119">เลือกกล่องกาเครื่องหมาย รวม</span><span class="sxs-lookup"><span data-stu-id="71aa7-119">Select the Include check box.</span></span>
14. <span data-ttu-id="71aa7-120">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="71aa7-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="71aa7-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="71aa7-121">Click OK.</span></span>
16. <span data-ttu-id="71aa7-122">ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="71aa7-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="71aa7-123">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="71aa7-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="71aa7-124">ในบานหน้าต่างการดำเนินการ ให้คลิก ซื้อ</span><span class="sxs-lookup"><span data-stu-id="71aa7-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="71aa7-125">คลิก ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="71aa7-125">Click Confirm.</span></span>
20. <span data-ttu-id="71aa7-126">ในบานหน้าต่างการดำเนินการ ให้คลิก รับ</span><span class="sxs-lookup"><span data-stu-id="71aa7-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="71aa7-127">คลิก ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="71aa7-127">Click Product receipt.</span></span>
22. <span data-ttu-id="71aa7-128">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="71aa7-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="71aa7-129">ในฟิลด์ใบรับสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="71aa7-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="71aa7-130">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="71aa7-130">Click OK.</span></span>

