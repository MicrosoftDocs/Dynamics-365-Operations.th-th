---
title: ชนิดของแอททริบิวต์ของการบำรุงรักษา
description: หัวข้อนี้จะอธิบายวิธีการสร้างชนิดแอททริบิวต์ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 469bcb16bb3099ffabdccfb026f0414de0213aaa
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438781"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="a5bd7-103">ชนิดของแอททริบิวต์ของการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="a5bd7-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a5bd7-104">หัวข้อนี้จะอธิบายวิธีการสร้างชนิดแอททริบิวต์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="a5bd7-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="a5bd7-105">แอตทริบิวต์จะถูกใช้เพื่ออธิบายคุณสมบัติขององค์ประกอบต่างๆ</span><span class="sxs-lookup"><span data-stu-id="a5bd7-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="a5bd7-106">คุณสามารถตั้งค่าแอททริบิวต์ในองค์ประกอบต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="a5bd7-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="a5bd7-107">ชนิดตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a5bd7-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="a5bd7-108">สร้างตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a5bd7-108">Create functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="a5bd7-109">ชนิดสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="a5bd7-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="a5bd7-110">สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="a5bd7-110">Assets</span></span>

<span data-ttu-id="a5bd7-111">แอททริบิวต์ที่คุณสามารถตั้งค่าได้จะแตกต่างกัน โดยขึ้นอยู่กับองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="a5bd7-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="a5bd7-112">ตัวอย่างเช่น สำหรับตำแหน่งที่ทำงาน คุณสามารถตั้งค่าแอททริบิวต์สำหรับการตั้งค่าคอนฟิกและขนาดทางกายภาพของสถานที่</span><span class="sxs-lookup"><span data-stu-id="a5bd7-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="a5bd7-113">สำหรับชนิดสินทรัพย์หรือสินทรัพย์ คุณสามารถตั้งค่าแอททริบิวต์สำหรับปริมาณกลไกจัดการ การใช้พลังงาน และกำลังการผลิตสูงสุด ภายใต้เงื่อนไขที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="a5bd7-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="a5bd7-114">สร้างชนิดแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="a5bd7-114">Create attribute types</span></span>

<span data-ttu-id="a5bd7-115">คุณสามารถสร้างชนิดแอททริบิวต์ของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="a5bd7-115">You can create your own attribute types.</span></span> <span data-ttu-id="a5bd7-116">นอกจากนี้ คุณสามารถโอนย้ายมิติของผลิตภัณฑ์ไปยังหน้า **ชนิดของแอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="a5bd7-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="a5bd7-117">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **ชนิดแอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="a5bd7-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="a5bd7-118">ครั้งแรกที่คุณตั้งค่าชนิดแอททริบิวต์ ให้เลือก **สร้างมิติของผลิตภัณฑ์** เพื่อโอนย้ายมิติของผลิตภัณฑ์มาตรฐานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a5bd7-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="a5bd7-119">เลือก **สร้าง** เพื่อสร้างชนิดแอททริบิวต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="a5bd7-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="a5bd7-120">ในฟิลด์ **ชนิดของแอททริบิวต์** ให้ป้อนชื่อสำหรับชนิดของแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="a5bd7-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="a5bd7-121">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a5bd7-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="a5bd7-122">ในฟิลด์ **หน่วย** ให้เลือกหน่วยแอททริบิวต์ที่เกี่ยวข้อง ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="a5bd7-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="a5bd7-123">ในฟิลด์ **ชนิดข้อมูล** ให้เลือกชนิดข้อมูลสำหรับหน่วย</span><span class="sxs-lookup"><span data-stu-id="a5bd7-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="a5bd7-124">ถ้าคุณเลือก **สตริง** เป็นชนิดข้อมูล ให้ทำตามขั้นตอนเหล่านี้เพื่อสร้างค่าสำหรับชนิดของแอททริบิวต์:</span><span class="sxs-lookup"><span data-stu-id="a5bd7-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="a5bd7-125">เลือกชนิดของแอททริบิวต์ และจากนั้น เลือก **ค่า**</span><span class="sxs-lookup"><span data-stu-id="a5bd7-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="a5bd7-126">ในฟิลด์ **ค่าแอททริบิวต์** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="a5bd7-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="a5bd7-127">ในฟิลด์ **ชนิดแอททริบิวต์** เลือกชนิดของแอททริบิวต์ (มิติ)</span><span class="sxs-lookup"><span data-stu-id="a5bd7-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="a5bd7-128">ในฟิลด์ **ค่า** ให้ป้อนค่าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a5bd7-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="a5bd7-129">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a5bd7-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="a5bd7-130">บันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="a5bd7-130">Save the record.</span></span>
    7. <span data-ttu-id="a5bd7-131">กลับไปที่หน้า **ชนิดแอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="a5bd7-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="a5bd7-132">บันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="a5bd7-132">Save the record.</span></span>

    <span data-ttu-id="a5bd7-133">ฟิลด์ **ชนิดตำแหน่งที่ทำงาน** แสดงจำนวนของตำแหน่งที่ทำงานที่ใช้ชนิดแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="a5bd7-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="a5bd7-134">ฟิลด์ **ชนิดสินทรัพย์** จะแสดงจำนวนของชนิดสินทรัพย์ที่กำลังใช้</span><span class="sxs-lookup"><span data-stu-id="a5bd7-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
