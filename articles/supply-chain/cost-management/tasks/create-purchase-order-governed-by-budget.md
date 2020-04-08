---
title: สร้างใบสั่งซื้อที่ได้รับการควบคุมโดยงบประมาณ
description: ใช้กระบวนงานนี้เพื่อสร้างใบสั่งซื้อที่มีการตรวจสอบงบประมาณที่มีอยู่
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0054745394d6a21599d8f07605f78ffdd7f575ab
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150550"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="5b1cb-103">สร้างใบสั่งซื้อที่ได้รับการควบคุมโดยงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b1cb-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b1cb-104">ใช้กระบวนงานนี้เพื่อสร้างใบสั่งซื้อที่มีการตรวจสอบงบประมาณที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="5b1cb-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="5b1cb-105">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="5b1cb-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="5b1cb-106">ตรวจสอบการตั้งค่าคอนฟิกการควบคุมงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b1cb-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="5b1cb-107">ไปที่ การจัดทำงบประมาณ > การตั้งค่า > การควบคุมงบประมาณ > การตั้งค่าคอนฟิกการควบคุมงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b1cb-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="5b1cb-108">คลิกแท็บ เงินงบประมาณที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="5b1cb-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="5b1cb-109">คลิกแท็บ เอกสารและสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5b1cb-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="5b1cb-110">คลิกแท็บ กำหนดกฎการควบคุมงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b1cb-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="5b1cb-111">คลิกแท็บ กำหนดกลุ่มงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b1cb-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="5b1cb-112">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5b1cb-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="5b1cb-113">สร้างส่วนหัวของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="5b1cb-113">Create the purchase order header</span></span>
1. <span data-ttu-id="5b1cb-114">ไปที่การจัดซื้อและการจัดหา > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5b1cb-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="5b1cb-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5b1cb-115">Click New.</span></span>
3. <span data-ttu-id="5b1cb-116">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="5b1cb-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="5b1cb-117">ขยายส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="5b1cb-117">Expand the General section.</span></span>
5. <span data-ttu-id="5b1cb-118">ในฟิลด์ วันที่ลงบัญชี ตั้งค่าวันที่เป็น '2016-01-01'</span><span class="sxs-lookup"><span data-stu-id="5b1cb-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="5b1cb-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5b1cb-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="5b1cb-120">เพิ่มรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="5b1cb-120">Add a purchase order line</span></span>
1. <span data-ttu-id="5b1cb-121">ในฟิลด์การจัดซื้อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5b1cb-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="5b1cb-122">กำหนดปริมาณเป็น '2'</span><span class="sxs-lookup"><span data-stu-id="5b1cb-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="5b1cb-123">ในฟิลด์หน่วย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="5b1cb-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="5b1cb-124">ตั้งค่าราคาต่อหน่วยเป็น '10000'</span><span class="sxs-lookup"><span data-stu-id="5b1cb-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="5b1cb-125">คลิกข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5b1cb-125">Click Financials.</span></span>
6. <span data-ttu-id="5b1cb-126">คลิกกระจายยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="5b1cb-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="5b1cb-127">ในฟิลด์บัญชีแยกประเภท ให้ระบุค่า '601300-001-023--'</span><span class="sxs-lookup"><span data-stu-id="5b1cb-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="5b1cb-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5b1cb-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="5b1cb-129">ทำการตรวจสอบงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b1cb-129">Perform budget checking</span></span>
1. <span data-ttu-id="5b1cb-130">คลิกข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5b1cb-130">Click Financials.</span></span>
2. <span data-ttu-id="5b1cb-131">คลิก ทำการตรวจสอบงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b1cb-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="5b1cb-132">คลิกข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="5b1cb-132">Click Financials.</span></span>
4. <span data-ttu-id="5b1cb-133">คลิก ข้อผิดพลาดหรือคำเตือนของการตรวจสอบงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5b1cb-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="5b1cb-134">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="5b1cb-134">Click Close.</span></span>

