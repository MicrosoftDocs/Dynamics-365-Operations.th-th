---
title: สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า
description: หัวข้อนี้อธิบายวิธีการตั้งค่าระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีการที่คุณกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์ที่เหมาะสม
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920668"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="deb84-103">สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="deb84-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="deb84-104">หัวข้อนี้อธิบายวิธีการตั้งค่าระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีการที่คุณกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="deb84-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="deb84-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="deb84-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="deb84-106">ระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์ใหม่ถูกกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์สีและขนาด </span><span class="sxs-lookup"><span data-stu-id="deb84-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="deb84-107">โดยทั่วไปงานนี้อาจดำเนินการโดยผู้ออกแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="deb84-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="deb84-108">สร้างระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="deb84-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="deb84-109">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> การตั้งค่า \> ระบบการตั้งชื่อผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="deb84-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="deb84-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="deb84-110">Select **New**.</span></span>
1. <span data-ttu-id="deb84-111">ในฟิลด์ **ชื่อ** ป้อนชื่อระบบการตั้งชื่อที่ช่วยในการระบุกลุ่มมิติของผลิตภัณฑ์เป้าหมาย ตัวอย่างเช่น `ColorSize`</span><span class="sxs-lookup"><span data-stu-id="deb84-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="deb84-112">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="deb84-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="deb84-113">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="deb84-113">Select **Add**.</span></span>
1. <span data-ttu-id="deb84-114">เลือกหมายเลข **ผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="deb84-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="deb84-115">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="deb84-115">Select **Add**.</span></span>
1. <span data-ttu-id="deb84-116">เลือก **ค่าคงที่ของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="deb84-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="deb84-117">ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="deb84-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="deb84-118">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="deb84-118">Select **Add**.</span></span>
1. <span data-ttu-id="deb84-119">เลือก **สี**</span><span class="sxs-lookup"><span data-stu-id="deb84-119">Select **Color**.</span></span>
1. <span data-ttu-id="deb84-120">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="deb84-120">Select **Add**.</span></span>
1. <span data-ttu-id="deb84-121">เลือก **ค่าคงที่ของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="deb84-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="deb84-122">ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="deb84-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="deb84-123">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="deb84-123">Select **Add**.</span></span>
1. <span data-ttu-id="deb84-124">เลือก **ขนาด**</span><span class="sxs-lookup"><span data-stu-id="deb84-124">Select **Size**.</span></span>
1. <span data-ttu-id="deb84-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="deb84-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="deb84-126">กำหนดระบบการตั้งชื่อให้กับผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="deb84-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="deb84-127">เลือก **กลุ่มมิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="deb84-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="deb84-128">เลือกกลุ่ม **มิติของผลิตภัณฑ์ SizeCol**</span><span class="sxs-lookup"><span data-stu-id="deb84-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="deb84-129">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="deb84-129">Select **Edit**.</span></span>
4. <span data-ttu-id="deb84-130">เลือก **ใช่** ในฟิลด์ **ใช้ระบบการตั้งชื่อ**</span><span class="sxs-lookup"><span data-stu-id="deb84-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="deb84-131">ในฟิลด์ **ระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อย** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="deb84-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="deb84-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="deb84-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]