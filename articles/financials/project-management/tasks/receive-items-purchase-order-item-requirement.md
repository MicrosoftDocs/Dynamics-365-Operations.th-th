---
title: รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า
description: หัวข้อนี้อธิบายวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
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
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867306"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="bde4d-103">รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="bde4d-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bde4d-104">หัวข้อนี้อธิบายวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="bde4d-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="bde4d-105">โดยการใช้ข้อกำหนดรายการแทนธุรกรรมรายการ คุณสามารถวางแผนให้กับการส่งมอบก่อนการใช้รายการจริง สร้างใบสั่งซื้อ รวมรายการในโครงงานข้อตกลงการค้า และรวมในข้อกำหนดรายการในการวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="bde4d-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="bde4d-106">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="bde4d-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="bde4d-107">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > โครงการ > โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="bde4d-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="bde4d-108">ในรายการ ให้เลือกลิงค์ในแถวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bde4d-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="bde4d-109">บนบานหน้าต่างการดำเนินการ เลือก **วางแผน**</span><span class="sxs-lookup"><span data-stu-id="bde4d-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="bde4d-110">เลือก **ข้อกำหนดสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bde4d-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="bde4d-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="bde4d-111">Select **New**.</span></span>
6. <span data-ttu-id="bde4d-112">ในแถวใหม่ ป้อนหรือเลือกค่าในฟิลด์ **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bde4d-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="bde4d-113">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="bde4d-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="bde4d-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="bde4d-114">Select **Save**.</span></span>
9. <span data-ttu-id="bde4d-115">ในบานหน้าต่างการดำเนินการ เลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="bde4d-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="bde4d-116">เลือก **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="bde4d-116">Select **Functions**.</span></span>
11. <span data-ttu-id="bde4d-117">เลือก **สร้างใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="bde4d-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="bde4d-118">เลือกกล่องกาเครื่องหมาย **รวมทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="bde4d-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="bde4d-119">ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bde4d-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="bde4d-120">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bde4d-120">Select **OK**.</span></span>
15. <span data-ttu-id="bde4d-121">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="bde4d-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="bde4d-122">ในรายการ ให้เลือกลิงค์ในแถวที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bde4d-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="bde4d-123">บนบานหน้าต่างการดำเนินการ เลือก **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="bde4d-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="bde4d-124">เลือก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="bde4d-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="bde4d-125">ในบานหน้าต่างการดำเนินการ เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="bde4d-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="bde4d-126">เลือก **ใบรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bde4d-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="bde4d-127">ในฟิลด์ **ใบรับสินค้า** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bde4d-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="bde4d-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bde4d-128">Select **OK**.</span></span>

