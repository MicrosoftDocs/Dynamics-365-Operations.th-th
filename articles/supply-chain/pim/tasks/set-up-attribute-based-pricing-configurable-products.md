---
title: ตั้งค่าการกำหนดราคาตามแอททริบิวต์สำหรับผลิตภัณฑ์ที่สามารถจัดโครงแบบ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการกำหนดราคาตามแอททริบิวต์
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921252"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="cb3ff-103">ตั้งค่าการกำหนดราคาตามแอททริบิวต์สำหรับผลิตภัณฑ์ที่สามารถจัดโครงแบบ</span><span class="sxs-lookup"><span data-stu-id="cb3ff-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb3ff-104">หัวข้อนี้อธิบายวิธีการตั้งค่าการกำหนดราคาตามแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="cb3ff-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="cb3ff-105">โดยเป็นข้อกำหนดเบื้องต้น คุณต้องมีการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีหนึ่งหรือหลายส่วนประกอบ และแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="cb3ff-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="cb3ff-106">ตัวอย่างนี้ใช้แบบจำลองผลิตภัณฑ์ลำโพงระดับสูงในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="cb3ff-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="cb3ff-107">โดยทั่วไปผู้จัดการผลิตภัณฑ์จะใช้กระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="cb3ff-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="cb3ff-108">สร้างแบบจำลองราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="cb3ff-108">Create a new price model</span></span>

1. <span data-ttu-id="cb3ff-109">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="cb3ff-110">ในรายการ เลือกรายการ **ลำโพงระดับสูง** แต่อย่าเลือกลิงค์สำหรับชื่อ</span><span class="sxs-lookup"><span data-stu-id="cb3ff-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="cb3ff-111">บนบานหน้าต่างการดำเนินการ เลือก **แบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="cb3ff-112">เลือก **แบบจำลองราคา**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-112">Select **Price models**.</span></span>
1. <span data-ttu-id="cb3ff-113">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-113">Select **New**.</span></span>
1. <span data-ttu-id="cb3ff-114">ในฟิลด์ **ชื่อแบบจำลองราคา** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="cb3ff-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="cb3ff-115">ใช้ชื่อที่ทำให้แบบจำลองระบุได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="cb3ff-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="cb3ff-116">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cb3ff-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="cb3ff-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="cb3ff-118">เพิ่มองค์ประกอบราคา</span><span class="sxs-lookup"><span data-stu-id="cb3ff-118">Add price elements</span></span>

1. <span data-ttu-id="cb3ff-119">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-119">Select **Edit**.</span></span> <span data-ttu-id="cb3ff-120">แต่ละส่วนประกอบในแบบจำลองผลิตภัณฑ์สามารถมีองค์ประกอบราคาพื้นฐานหนึ่งรายการและกฎของนิพจน์ราคาจำนวนเท่าใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="cb3ff-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="cb3ff-121">นอกจากนี้คุณยังสามารถเพิ่มราคาในสกุลเงินที่แตกต่างกันได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="cb3ff-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="cb3ff-122">ในฟิลด์ **นิพจน์ราคาพื้นฐาน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="cb3ff-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="cb3ff-123">ตัวอย่างเช่น พิมพ์ 100</span><span class="sxs-lookup"><span data-stu-id="cb3ff-123">For example, type 100.</span></span> <span data-ttu-id="cb3ff-124">นิพจน์ราคาพื้นฐานอาจเป็นค่าตัวเลข หรืออาจประกอบด้วยการคำนวณทางคณิตศาสตร์ที่เกี่ยวข้องกับแอททริบิวต์มากกว่าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="cb3ff-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="cb3ff-125">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-125">Select **Add**.</span></span>
4. <span data-ttu-id="cb3ff-126">ในฟิลด์ **ชื่อ** ให้พิมพ์ `Rosewood`</span><span class="sxs-lookup"><span data-stu-id="cb3ff-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="cb3ff-127">ชื่อของนิพจน์ราคาช่วยระบุว่าแสดงถึงองค์ประกอบราคาใด </span><span class="sxs-lookup"><span data-stu-id="cb3ff-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="cb3ff-128">ในตัวอย่างนี้ เรากำลังสร้างองค์ประกอบราคาสำหรับตัวเลือก ลำโพง Rosewood Cabinet เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="cb3ff-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="cb3ff-129">เลือก **แก้ไขเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-129">Select **Edit condition**.</span></span> <span data-ttu-id="cb3ff-130">เงื่อนไขราคาช่วยรับประกันว่ามีองค์ประกอบนิพจน์ราคารวมอยู่ในราคาขายถ้ามีชุดของแอททริบิวต์เฉพาะเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cb3ff-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="cb3ff-131">ในฟิลด์ **ConstraintBody** ให้ป้อน `CabinetFinish=="Rosewood"`</span><span class="sxs-lookup"><span data-stu-id="cb3ff-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="cb3ff-132">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-132">Select **OK**.</span></span>
8. <span data-ttu-id="cb3ff-133">ในฟิลด์ **นิพจน์** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="cb3ff-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="cb3ff-134">ตัวอย่างเช่น พิมพ์ `50`</span><span class="sxs-lookup"><span data-stu-id="cb3ff-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="cb3ff-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cb3ff-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]