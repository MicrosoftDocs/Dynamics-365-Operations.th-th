---
title: สร้างเกณฑ์การเลือกราคาขาย
description: 'กระบวนงานนี้แสดงวิธีการสร้างเกณฑ์การเลือกราคาขายสำหรับแบบจำลองราคาขายตามแอททริบิวต์ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920542"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="8a234-103">สร้างเกณฑ์การเลือกราคาขาย</span><span class="sxs-lookup"><span data-stu-id="8a234-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a234-104">กระบวนงานนี้แสดงวิธีการสร้างเกณฑ์การเลือกราคาขายสำหรับแบบจำลองราคาขายตามแอททริบิวต์ </span><span class="sxs-lookup"><span data-stu-id="8a234-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="8a234-105">ขั้นตอนนี้จำเป็นต้องใช้แบบจำลองราคาขายที่มีอยู่อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="8a234-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="8a234-106">ตัวอย่างนี้ใช้แบบจำลองราคาสำหรับแบบจำลองราคาขายของโซลูชันลำโพงในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="8a234-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="8a234-107">โดยทั่วไปผู้จัดการผลิตภัณฑ์จะใช้กระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="8a234-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="8a234-108">เพิ่มเกณฑ์ใหม่สำหรับแบบจำลองราคาขายที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="8a234-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="8a234-109">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="8a234-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="8a234-110">ในรายการ เลือกแถวสำหรับแบบจำลองผลิตภัณฑ์โซลูชันลำโพง แต่อย่าเลือกลิงค์สำหรับชื่อแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="8a234-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="8a234-111">บนบานหน้าต่างการดำเนินการ เลือก **แบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="8a234-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="8a234-112">เลือก **เกณฑ์แบบจำลองราคา**</span><span class="sxs-lookup"><span data-stu-id="8a234-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="8a234-113">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8a234-113">Select **New**.</span></span>
1. <span data-ttu-id="8a234-114">ในฟิลด์ **ชื่อ** ให้พิมพ์ 'กลุ่มลูกค้า 10'</span><span class="sxs-lookup"><span data-stu-id="8a234-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="8a234-115">ใช้ชื่อของเกณฑ์แบบจำลองราคาเพื่อช่วยในการระบุเกณฑ์การเลือกที่อยู่ภายใต้</span><span class="sxs-lookup"><span data-stu-id="8a234-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="8a234-116">ในฟิลด์ **แบบจำลองราคา** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="8a234-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="8a234-117">ในฟิลด์ **ชนิดใบสั่ง** เลือก *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="8a234-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="8a234-118">ชนิดใบสั่งกำหนดฟิลด์ฐานข้อมูลที่จะใช้สำหรับการสอบถามเลือก</span><span class="sxs-lookup"><span data-stu-id="8a234-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="8a234-119">ในฟิลด์ **ใช้ได้ตั้งแต่** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="8a234-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="8a234-120">ในฟิลด์ **หมดอายุวันที่** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="8a234-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="8a234-121">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8a234-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="8a234-122">สร้างการสอบถามสำหรับเกณฑ์การเลือก</span><span class="sxs-lookup"><span data-stu-id="8a234-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="8a234-123">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8a234-123">Select **Edit**.</span></span>
2. <span data-ttu-id="8a234-124">ในฟิลด์ **ตาราง** ให้เลือก *ลูกค้า*</span><span class="sxs-lookup"><span data-stu-id="8a234-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="8a234-125">ในฟิลด์ **ฟิลด์** ให้เลือก *กลุ่มลูกค้า*</span><span class="sxs-lookup"><span data-stu-id="8a234-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="8a234-126">ในตัวอย่างนี้ เราจะใช้กลุ่มลูกค้าเฉพาะสำหรับเกณฑ์การเลือก</span><span class="sxs-lookup"><span data-stu-id="8a234-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="8a234-127">ในฟิลด์ **เกณฑ์** ให้เลือก *กลุ่มลูกค้า 10*</span><span class="sxs-lookup"><span data-stu-id="8a234-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="8a234-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="8a234-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]