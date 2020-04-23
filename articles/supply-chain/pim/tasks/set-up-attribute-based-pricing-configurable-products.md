---
title: ตั้งค่าการกำหนดราคาตามแอททริบิวต์สำหรับผลิตภัณฑ์ที่สามารถจัดโครงแบบ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการกำหนดราคาตามแอททริบิวต์
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7382cdfa11e89896bba9518f36eb6caab56b98f6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213066"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="c3cba-103">ตั้งค่าการกำหนดราคาตามแอททริบิวต์สำหรับผลิตภัณฑ์ที่สามารถจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="c3cba-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3cba-104">หัวข้อนี้อธิบายวิธีการตั้งค่าการกำหนดราคาตามแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="c3cba-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="c3cba-105">โดยเป็นข้อกำหนดเบื้องต้น คุณต้องมีการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีหนึ่งหรือหลายส่วนประกอบ และแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="c3cba-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="c3cba-106">ตัวอย่างนี้ใช้แบบจำลองผลิตภัณฑ์ลำโพงระดับสูงในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="c3cba-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="c3cba-107">โดยทั่วไปผู้จัดการผลิตภัณฑ์จะใช้กระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="c3cba-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="c3cba-108">สร้างแบบจำลองราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="c3cba-108">Create a new price model</span></span>
1. <span data-ttu-id="c3cba-109">เลือก **ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย** บนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="c3cba-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="c3cba-110">เลือก **แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์** ในส่วน **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="c3cba-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="c3cba-111">ในรายการ เลือกรายการ **ลำโพงระดับสูง** แต่อย่าเลือกลิงค์สำหรับชื่อ</span><span class="sxs-lookup"><span data-stu-id="c3cba-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="c3cba-112">บนบานหน้าต่างการดำเนินการ เลือก **แบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="c3cba-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="c3cba-113">เลือก **แบบจำลองราคา**</span><span class="sxs-lookup"><span data-stu-id="c3cba-113">Select **Price models**.</span></span>
6. <span data-ttu-id="c3cba-114">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c3cba-114">Select **New**.</span></span>
7. <span data-ttu-id="c3cba-115">ในฟิลด์ **ชื่อแบบจำลองราคา** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c3cba-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="c3cba-116">ใช้ชื่อที่ทำให้แบบจำลองระบุได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="c3cba-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="c3cba-117">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c3cba-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="c3cba-118">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c3cba-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="c3cba-119">เพิ่มองค์ประกอบราคา</span><span class="sxs-lookup"><span data-stu-id="c3cba-119">Add price elements</span></span>
1. <span data-ttu-id="c3cba-120">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="c3cba-120">Select **Edit**.</span></span> <span data-ttu-id="c3cba-121">แต่ละส่วนประกอบในแบบจำลองผลิตภัณฑ์สามารถมีองค์ประกอบราคาพื้นฐานหนึ่งรายการและกฎของนิพจน์ราคาจำนวนเท่าใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="c3cba-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="c3cba-122">นอกจากนี้คุณยังสามารถเพิ่มราคาในสกุลเงินที่แตกต่างกันได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="c3cba-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="c3cba-123">ในฟิลด์ **นิพจน์ราคาพื้นฐาน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c3cba-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="c3cba-124">ตัวอย่างเช่น พิมพ์ 100</span><span class="sxs-lookup"><span data-stu-id="c3cba-124">For example, type 100.</span></span> <span data-ttu-id="c3cba-125">นิพจน์ราคาพื้นฐานอาจเป็นค่าตัวเลข หรืออาจประกอบด้วยการคำนวณทางคณิตศาสตร์ที่เกี่ยวข้องกับแอททริบิวต์มากกว่าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="c3cba-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="c3cba-126">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="c3cba-126">Select **Add**.</span></span>
4. <span data-ttu-id="c3cba-127">ในฟิลด์ **ชื่อ** ให้พิมพ์ `Rosewood`</span><span class="sxs-lookup"><span data-stu-id="c3cba-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="c3cba-128">ชื่อของนิพจน์ราคาช่วยระบุว่าแสดงถึงองค์ประกอบราคาใด </span><span class="sxs-lookup"><span data-stu-id="c3cba-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="c3cba-129">ในตัวอย่างนี้ เรากำลังสร้างองค์ประกอบราคาสำหรับตัวเลือก ลำโพง Rosewood Cabinet เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="c3cba-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="c3cba-130">เลือก **แก้ไขเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="c3cba-130">Select **Edit condition**.</span></span> <span data-ttu-id="c3cba-131">เงื่อนไขราคาช่วยรับประกันว่ามีองค์ประกอบนิพจน์ราคารวมอยู่ในราคาขายถ้ามีชุดของแอททริบิวต์เฉพาะเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c3cba-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="c3cba-132">ในฟิลด์ **ConstraintBody** ให้ป้อน `CabinetFinish=="Rosewood"`</span><span class="sxs-lookup"><span data-stu-id="c3cba-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="c3cba-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c3cba-133">Select **OK**.</span></span>
8. <span data-ttu-id="c3cba-134">ในฟิลด์ **นิพจน์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c3cba-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="c3cba-135">ตัวอย่างเช่น พิมพ์ `50`</span><span class="sxs-lookup"><span data-stu-id="c3cba-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="c3cba-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c3cba-136">Close the page.</span></span>

