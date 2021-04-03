---
title: สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า
description: หัวข้อนี้อธิบายวิธีการตั้งค่าระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีการที่คุณกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์ที่เหมาะสม
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a4ad70a87cd8c6cab2e9853f4f6c52f574d318a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257437"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="3ba7d-103">สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="3ba7d-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3ba7d-104">หัวข้อนี้อธิบายวิธีการตั้งค่าระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีการที่คุณกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="3ba7d-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="3ba7d-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="3ba7d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3ba7d-106">ระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์ใหม่ถูกกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์สีและขนาด </span><span class="sxs-lookup"><span data-stu-id="3ba7d-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="3ba7d-107">โดยทั่วไปงานนี้อาจดำเนินการโดยผู้ออกแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3ba7d-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="3ba7d-108">สร้างระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3ba7d-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="3ba7d-109">เลือก **ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="3ba7d-110">เลือก **ระบบการตั้งชื่อสำหรับผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="3ba7d-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-111">Select **New**.</span></span>
4. <span data-ttu-id="3ba7d-112">ในฟิลด์ **ชื่อ** ป้อนชื่อระบบการตั้งชื่อที่ช่วยในการระบุกลุ่มมิติของผลิตภัณฑ์เป้าหมาย ตัวอย่างเช่น `ColorSize`</span><span class="sxs-lookup"><span data-stu-id="3ba7d-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="3ba7d-113">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3ba7d-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="3ba7d-114">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-114">Select **Add**.</span></span>
7. <span data-ttu-id="3ba7d-115">เลือกหมายเลข **ผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="3ba7d-116">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-116">Select **Add**.</span></span>
9. <span data-ttu-id="3ba7d-117">เลือก **ค่าคงที่ของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="3ba7d-118">ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3ba7d-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="3ba7d-119">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-119">Select **Add**.</span></span>
12. <span data-ttu-id="3ba7d-120">เลือก **สี**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-120">Select **Color**.</span></span>
13. <span data-ttu-id="3ba7d-121">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-121">Select **Add**.</span></span>
14. <span data-ttu-id="3ba7d-122">เลือก **ค่าคงที่ของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="3ba7d-123">ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3ba7d-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="3ba7d-124">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-124">Select **Add**.</span></span>
17. <span data-ttu-id="3ba7d-125">เลือก **ขนาด**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-125">Select **Size**.</span></span>
18. <span data-ttu-id="3ba7d-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ba7d-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="3ba7d-127">กำหนดระบบการตั้งชื่อให้กับผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="3ba7d-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="3ba7d-128">เลือก **กลุ่มมิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="3ba7d-129">เลือกกลุ่ม **มิติของผลิตภัณฑ์ SizeCol**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="3ba7d-130">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-130">Select **Edit**.</span></span>
4. <span data-ttu-id="3ba7d-131">เลือก **ใช่** ในฟิลด์ **ใช้ระบบการตั้งชื่อ**</span><span class="sxs-lookup"><span data-stu-id="3ba7d-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="3ba7d-132">ในฟิลด์ **ระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อย** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3ba7d-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="3ba7d-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ba7d-133">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]