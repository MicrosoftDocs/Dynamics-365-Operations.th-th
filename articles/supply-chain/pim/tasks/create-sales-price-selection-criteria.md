---
title: สร้างเกณฑ์การเลือกราคาขาย
description: 'กระบวนงานนี้แสดงวิธีการสร้างเกณฑ์การเลือกราคาขายสำหรับแบบจำลองราคาขายตามแอททริบิวต์ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8c60b188b7c7090546e8367455e0f58ce9359b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147698"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="d9a4b-103">สร้างเกณฑ์การเลือกราคาขาย</span><span class="sxs-lookup"><span data-stu-id="d9a4b-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9a4b-104">กระบวนงานนี้แสดงวิธีการสร้างเกณฑ์การเลือกราคาขายสำหรับแบบจำลองราคาขายตามแอททริบิวต์ </span><span class="sxs-lookup"><span data-stu-id="d9a4b-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="d9a4b-105">ขั้นตอนนี้จำเป็นต้องใช้แบบจำลองราคาขายที่มีอยู่อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="d9a4b-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="d9a4b-106">ตัวอย่างนี้ใช้แบบจำลองราคาสำหรับแบบจำลองราคาขายของโซลูชันลำโพงในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="d9a4b-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="d9a4b-107">โดยทั่วไปผู้จัดการผลิตภัณฑ์จะใช้กระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="d9a4b-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="d9a4b-108">เพิ่มเกณฑ์ใหม่สำหรับแบบจำลองราคาขายที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d9a4b-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="d9a4b-109">คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="d9a4b-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="d9a4b-110">คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d9a4b-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="d9a4b-111">ในรายการ เลือกแถวสำหรับแบบจำลองผลิตภัณฑ์โซลูชันลำโพง แต่อย่าคลิกลิงค์สำหรับชื่อแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="d9a4b-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="d9a4b-112">ในบานหน้าต่างการดำเนินการ คลิก แบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="d9a4b-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="d9a4b-113">คลิก เกณฑ์แบบจำลองราคา</span><span class="sxs-lookup"><span data-stu-id="d9a4b-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="d9a4b-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d9a4b-114">Click New.</span></span>
7. <span data-ttu-id="d9a4b-115">ในฟิลด์ชื่อ ให้พิมพ์ 'กลุ่มลูกค้า 10'</span><span class="sxs-lookup"><span data-stu-id="d9a4b-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="d9a4b-116">ใช้ชื่อของเกณฑ์แบบจำลองราคาเพื่อช่วยในการระบุเกณฑ์การเลือกที่อยู่ภายใต้</span><span class="sxs-lookup"><span data-stu-id="d9a4b-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="d9a4b-117">ในฟิลด์แบบจำลองราคา ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d9a4b-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="d9a4b-118">ในฟิลด์ชนิดใบสั่ง เลือก ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="d9a4b-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="d9a4b-119">ชนิดใบสั่งกำหนดฟิลด์ฐานข้อมูลที่จะใช้สำหรับการสอบถามเลือก</span><span class="sxs-lookup"><span data-stu-id="d9a4b-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="d9a4b-120">ในฟิลด์ ใช้ได้ตั้งแต่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="d9a4b-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="d9a4b-121">ในฟิลด์ หมดอายุวันที่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="d9a4b-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="d9a4b-122">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d9a4b-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="d9a4b-123">สร้างการสอบถามสำหรับเกณฑ์การเลือก</span><span class="sxs-lookup"><span data-stu-id="d9a4b-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="d9a4b-124">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="d9a4b-124">Click Edit.</span></span>
2. <span data-ttu-id="d9a4b-125">ในฟิลด์ตาราง ให้เลือก ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d9a4b-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="d9a4b-126">ในฟิลด์ ฟิลด์ ให้เลือก กลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d9a4b-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="d9a4b-127">ในตัวอย่างนี้ เราจะใช้กลุ่มลูกค้าเฉพาะสำหรับเกณฑ์การเลือก</span><span class="sxs-lookup"><span data-stu-id="d9a4b-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="d9a4b-128">ในฟิลด์ เกณฑ์ ให้เลือก 'กลุ่มลูกค้า 10'</span><span class="sxs-lookup"><span data-stu-id="d9a4b-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="d9a4b-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d9a4b-129">Click OK.</span></span>

