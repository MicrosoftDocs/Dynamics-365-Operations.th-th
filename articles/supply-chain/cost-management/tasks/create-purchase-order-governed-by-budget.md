---
title: สร้างใบสั่งซื้อที่ได้รับการควบคุมโดยงบประมาณ
description: ใช้กระบวนงานนี้เพื่อสร้างใบสั่งซื้อที่มีการตรวจสอบงบประมาณที่มีอยู่
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbfbbef3bd7c7398f0f17b6cddbbff8c4755638d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963724"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="6b174-103">สร้างใบสั่งซื้อที่ได้รับการควบคุมโดยงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="6b174-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b174-104">ใช้กระบวนงานนี้เพื่อสร้างใบสั่งซื้อที่มีการตรวจสอบงบประมาณที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="6b174-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="6b174-105">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="6b174-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="6b174-106">ตรวจสอบการตั้งค่าคอนฟิกการควบคุมงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="6b174-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="6b174-107">ไปที่ การจัดทำงบประมาณ > การตั้งค่า > การควบคุมงบประมาณ > การตั้งค่าคอนฟิกการควบคุมงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="6b174-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="6b174-108">คลิกแท็บ เงินงบประมาณที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="6b174-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="6b174-109">คลิกแท็บ เอกสารและสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6b174-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="6b174-110">คลิกแท็บ กำหนดกฎการควบคุมงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="6b174-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="6b174-111">คลิกแท็บ กำหนดกลุ่มงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="6b174-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="6b174-112">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6b174-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="6b174-113">สร้างส่วนหัวของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="6b174-113">Create the purchase order header</span></span>
1. <span data-ttu-id="6b174-114">ไปที่การจัดซื้อและการจัดหา > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6b174-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="6b174-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6b174-115">Click New.</span></span>
3. <span data-ttu-id="6b174-116">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6b174-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="6b174-117">ขยายส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="6b174-117">Expand the General section.</span></span>
5. <span data-ttu-id="6b174-118">ในฟิลด์ วันที่ลงบัญชี ตั้งค่าวันที่เป็น '2016-01-01'</span><span class="sxs-lookup"><span data-stu-id="6b174-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="6b174-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6b174-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="6b174-120">เพิ่มรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="6b174-120">Add a purchase order line</span></span>
1. <span data-ttu-id="6b174-121">ในฟิลด์การจัดซื้อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b174-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="6b174-122">กำหนดปริมาณเป็น '2'</span><span class="sxs-lookup"><span data-stu-id="6b174-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="6b174-123">ในฟิลด์หน่วย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6b174-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="6b174-124">ตั้งค่าราคาต่อหน่วยเป็น '10000'</span><span class="sxs-lookup"><span data-stu-id="6b174-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="6b174-125">คลิกข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6b174-125">Click Financials.</span></span>
6. <span data-ttu-id="6b174-126">คลิกกระจายยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="6b174-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="6b174-127">ในฟิลด์บัญชีแยกประเภท ให้ระบุค่า '601300-001-023--'</span><span class="sxs-lookup"><span data-stu-id="6b174-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="6b174-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6b174-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="6b174-129">ทำการตรวจสอบงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="6b174-129">Perform budget checking</span></span>
1. <span data-ttu-id="6b174-130">คลิกข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6b174-130">Click Financials.</span></span>
2. <span data-ttu-id="6b174-131">คลิก ทำการตรวจสอบงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="6b174-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="6b174-132">คลิกข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6b174-132">Click Financials.</span></span>
4. <span data-ttu-id="6b174-133">คลิก ข้อผิดพลาดหรือคำเตือนของการตรวจสอบงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="6b174-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="6b174-134">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="6b174-134">Click Close.</span></span>

