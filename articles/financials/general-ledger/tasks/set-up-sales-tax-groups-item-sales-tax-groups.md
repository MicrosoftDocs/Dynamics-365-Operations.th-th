--- 
title: "ตั้งค่ากลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้า"
description: "บันทึกงานนี้นำคุณไปสู่การตั้งค่ากลุ่มภาษีขายภาษีขายและกลุ่มภาษีขายตามประเภทสินค้า "
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 4488f271d55b849641dfd84a5a9c0691efb5dbad
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="bca66-103">ตั้งค่ากลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้า</span><span class="sxs-lookup"><span data-stu-id="bca66-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bca66-104">บันทึกงานนี้นำคุณไปสู่การตั้งค่ากลุ่มภาษีขายภาษีขายและกลุ่มภาษีขายตามประเภทสินค้า </span><span class="sxs-lookup"><span data-stu-id="bca66-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="bca66-105">กลุ่มภาษีขายคือ กลุ่มของรหัสภาษีขายที่แนบไปกับลูกค้าและผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="bca66-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="bca66-106">ทั้งยังแนบไปกับบัญชีแยกประเภทสำหรับธุรกรรมที่ไม่ได้ลงรายการบัญชีของผู้จัดจำหน่ายและลูกค้าเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="bca66-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="bca66-107">กลุ่มภาษีขายตามประเภทสินค้าคือ กลุ่มของรหัสภาษีขายที่แนบไปกับทรัพยากรเช่นเดียวกับผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="bca66-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="bca66-108">ภาษีขายที่ใช้กับธุรกรรมเฉพาะจะขึ้นอยู่กับรหัสภาษีขายที่รวมอยู่ในทั้งกลุ่มภาษีขาย และกลุ่มภาษีขายตามประเภทสินค้าของธุรกรรม </span><span class="sxs-lookup"><span data-stu-id="bca66-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="bca66-109">คุณสามารถคำนวณภาษีขายได้เฉพาะเมื่อมีเลือกกลุ่มภาษีขายและกลุ่มภาษีขายตามประเภทสินค้าสำหรับแต่ละธุรกรรมซึ่งต้องคำนวณหรือบันทึกภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="bca66-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="bca66-110">ไปที่ภาษี > ภาษีทางอ้อม > ภาษีขาย > กลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="bca66-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="bca66-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="bca66-111">Click New.</span></span>
3. <span data-ttu-id="bca66-112">ในฟิลด์กลุ่มภาษีขาย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bca66-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="bca66-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bca66-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bca66-114">สลับการขยายของส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="bca66-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="bca66-115">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="bca66-115">Click Add.</span></span>
7. <span data-ttu-id="bca66-116">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bca66-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="bca66-117">ในฟิลด์รหัสภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="bca66-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="bca66-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bca66-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="bca66-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bca66-119">Click Save.</span></span>
11. <span data-ttu-id="bca66-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bca66-120">Close the page.</span></span>
12. <span data-ttu-id="bca66-121">ไปที่ภาษี > ภาษีทางอ้อม > ภาษีขาย > กลุ่มภาษีขายของสินค้า</span><span class="sxs-lookup"><span data-stu-id="bca66-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="bca66-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="bca66-122">Click New.</span></span>
14. <span data-ttu-id="bca66-123">ในฟิลด์กลุ่มภาษีขายตามประเภทสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bca66-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="bca66-124">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bca66-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="bca66-125">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="bca66-125">Click Add.</span></span>
17. <span data-ttu-id="bca66-126">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bca66-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="bca66-127">ในฟิลด์รหัสภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="bca66-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="bca66-128">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bca66-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="bca66-129">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bca66-129">Click Save.</span></span>


