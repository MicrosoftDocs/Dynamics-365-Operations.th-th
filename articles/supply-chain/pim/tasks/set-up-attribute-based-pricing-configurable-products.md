---
title: ตั้งค่าการกำหนดราคาตามแอททริบิวต์สำหรับผลิตภัณฑ์ที่สามารถจัดโครงแบบ
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าการกำหนดราคาตามแอททริบิวต์ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8568b5f4933ae58bc2d55a169c798668e03bed2a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573291"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="bd35a-103">ตั้งค่าการกำหนดราคาตามแอททริบิวต์สำหรับผลิตภัณฑ์ที่สามารถจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="bd35a-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bd35a-104">กระบวนงานนี้แสดงวิธีการตั้งค่าการกำหนดราคาตามแอททริบิวต์ </span><span class="sxs-lookup"><span data-stu-id="bd35a-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="bd35a-105">โดยเป็นข้อกำหนดเบื้องต้น คุณต้องมีการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีหนึ่งหรือหลายส่วนประกอบ และแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="bd35a-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="bd35a-106">ตัวอย่างนี้ใช้แบบจำลองผลิตภัณฑ์ลำโพงระดับสูงในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="bd35a-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="bd35a-107">โดยทั่วไปผู้จัดการผลิตภัณฑ์จะใช้กระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="bd35a-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="bd35a-108">สร้างแบบจำลองราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="bd35a-108">Create a new price model</span></span>
1. <span data-ttu-id="bd35a-109">คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="bd35a-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="bd35a-110">คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bd35a-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="bd35a-111">ในรายการ เลือกบรรทัดลำโพงระดับสูง แต่อย่าคลิกการเชื่อมโยงของชื่อ</span><span class="sxs-lookup"><span data-stu-id="bd35a-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="bd35a-112">ในบานหน้าต่างการดำเนินการ คลิก แบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="bd35a-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="bd35a-113">คลิก แบบจำลองราคา</span><span class="sxs-lookup"><span data-stu-id="bd35a-113">Click Price models.</span></span>
6. <span data-ttu-id="bd35a-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="bd35a-114">Click New.</span></span>
7. <span data-ttu-id="bd35a-115">ในฟิลด์ชื่อแบบจำลองราคา ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bd35a-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="bd35a-116">ใช้ชื่อที่ทำให้แบบจำลองระบุได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="bd35a-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="bd35a-117">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bd35a-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="bd35a-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bd35a-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="bd35a-119">เพิ่มองค์ประกอบราคา</span><span class="sxs-lookup"><span data-stu-id="bd35a-119">Add price elements</span></span>
1. <span data-ttu-id="bd35a-120">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="bd35a-120">Click Edit.</span></span>
    * <span data-ttu-id="bd35a-121">แต่ละส่วนประกอบในแบบจำลองผลิตภัณฑ์สามารถมีองค์ประกอบราคาพื้นฐานหนึ่งรายการและกฎของนิพจน์ราคาจำนวนเท่าใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="bd35a-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="bd35a-122">นอกจากนี้คุณยังสามารถเพิ่มราคาในสกุลเงินที่แตกต่างกันได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="bd35a-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="bd35a-123">ในฟิลด์นิพจน์ราคาพื้นฐาน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bd35a-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="bd35a-124">ตัวอย่างเช่น พิมพ์ 100</span><span class="sxs-lookup"><span data-stu-id="bd35a-124">For example, type 100.</span></span>   <span data-ttu-id="bd35a-125">นิพจน์ราคาพื้นฐานอาจเป็นค่าตัวเลข หรืออาจประกอบด้วยการคำนวณทางคณิตศาสตร์ที่เกี่ยวข้องกับแอททริบิวต์มากกว่าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="bd35a-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="bd35a-126">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="bd35a-126">Click Add.</span></span>
4. <span data-ttu-id="bd35a-127">ในฟิลด์ชื่อ ให้พิมพ์ ‘Rosewood’</span><span class="sxs-lookup"><span data-stu-id="bd35a-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="bd35a-128">ชื่อของนิพจน์ราคาช่วยระบุว่าแสดงถึงองค์ประกอบราคาใด </span><span class="sxs-lookup"><span data-stu-id="bd35a-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="bd35a-129">ในตัวอย่างนี้ เรากำลังสร้างองค์ประกอบราคาสำหรับตัวเลือก ลำโพง Rosewood Cabinet เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="bd35a-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="bd35a-130">คลิก แก้ไขเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="bd35a-130">Click Edit condition.</span></span>
    * <span data-ttu-id="bd35a-131">เงื่อนไขราคาช่วยรับประกันว่ามีองค์ประกอบนิพจน์ราคารวมอยู่ในราคาขายถ้ามีชุดของแอททริบิวต์เฉพาะเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bd35a-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="bd35a-132">ในฟิลด์ ConstraintBody ให้ป้อน 'CabinetFinish=="Rosewood"'</span><span class="sxs-lookup"><span data-stu-id="bd35a-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="bd35a-133">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bd35a-133">Click OK.</span></span>
8. <span data-ttu-id="bd35a-134">ในฟิลด์นิพจน์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bd35a-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="bd35a-135">ตัวอย่างเช่น พิมพ์ 50</span><span class="sxs-lookup"><span data-stu-id="bd35a-135">For example, type 50.</span></span>  
9. <span data-ttu-id="bd35a-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bd35a-136">Close the page.</span></span>
10. <span data-ttu-id="bd35a-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bd35a-137">Close the page.</span></span>

