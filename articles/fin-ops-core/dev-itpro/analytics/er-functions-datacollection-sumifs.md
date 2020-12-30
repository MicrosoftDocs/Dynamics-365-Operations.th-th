---
title: ฟังก์ชัน SUMIFS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SUMIFS
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9d9ef51f3c8cb090f940670c4c3afae104268ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687973"
---
# <a name="sumifs-er-function"></a><span data-ttu-id="cb8e1-103">ฟังก์ชัน SUMIFS ER</span><span class="sxs-lookup"><span data-stu-id="cb8e1-103">SUMIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb8e1-104">ฟังก์ชัน `SUMIFS` ส่งกลับค่า *จำนวนจริง* ที่แสดงถึงผลรวมของค่าที่ส่งคืนโดยการผูกองค์ประกอบรูปแบบและการเก็บรวบรวม เมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="cb8e1-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="cb8e1-105">แต่ละเงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="cb8e1-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb8e1-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="cb8e1-106">Syntax</span></span>

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="cb8e1-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="cb8e1-107">Arguments</span></span>

<span data-ttu-id="cb8e1-108">`key name for summing`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="cb8e1-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="cb8e1-109">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ได้รับการกำหนดค่าในคุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ซึ่งค่าของการผูกจะต้องใช้สำหรับการสรุปวัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="cb8e1-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="cb8e1-110">คุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** สามารถกำหนดค่าสำหรับส่วนประกอบ **ตัวเลข** หรือส่วนประกอบ **สตริง** ของรูปแบบ ER ที่อยู่ภายใต้ส่วนประกอบของ **Common\\File** ที่ตัวเลือก **รวบรวมรายละเอียดของผลลัพธ์** เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="cb8e1-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cb8e1-111">`condition 1 range`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="cb8e1-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="cb8e1-112">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="cb8e1-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="cb8e1-113">อาร์กิวเมนต์นี้เป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="cb8e1-113">This argument is mandatory.</span></span>

<span data-ttu-id="cb8e1-114">คุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** สามารถกำหนดค่าสำหรับส่วนประกอบ **ลำดับ** หรือส่วนประกอบ **XML Element** ของรูปแบบ ER ที่อยู่ภายใต้ส่วนประกอบของ **Common\\File** ที่ตัวเลือก **รวบรวมรายละเอียดของผลลัพธ์** เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="cb8e1-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cb8e1-115">`condition 1 value`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="cb8e1-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="cb8e1-116">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="cb8e1-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="cb8e1-117">อาร์กิวเมนต์นี้เป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="cb8e1-117">This argument is mandatory.</span></span>

<span data-ttu-id="cb8e1-118">คุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** สามารถกำหนดค่าสำหรับส่วนประกอบ **ลำดับ** หรือส่วนประกอบ **XML Element** ของรูปแบบ ER ที่อยู่ภายใต้ส่วนประกอบของ **Common\\File** ที่ตัวเลือก **รวบรวมรายละเอียดของผลลัพธ์** เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="cb8e1-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cb8e1-119">`condition N range`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="cb8e1-119">`condition N range`: *String*</span></span>

<span data-ttu-id="cb8e1-120">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="cb8e1-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="cb8e1-121">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="cb8e1-121">These additional arguments are optional.</span></span>

<span data-ttu-id="cb8e1-122">คุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** สามารถกำหนดค่าสำหรับส่วนประกอบ **ลำดับ** หรือส่วนประกอบ **XML Element** ของรูปแบบ ER ที่อยู่ภายใต้ส่วนประกอบของ **Common\\File** ที่ตัวเลือก **รวบรวมรายละเอียดของผลลัพธ์** เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="cb8e1-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cb8e1-123">`condition N value`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="cb8e1-123">`condition N value`: *String*</span></span>

<span data-ttu-id="cb8e1-124">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="cb8e1-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="cb8e1-125">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="cb8e1-125">These additional arguments are optional.</span></span>

<span data-ttu-id="cb8e1-126">คุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** สามารถกำหนดค่าสำหรับส่วนประกอบ **ลำดับ** หรือส่วนประกอบ **XML Element** ของรูปแบบ ER ที่อยู่ภายใต้ส่วนประกอบของ **Common\\File** ที่ตัวเลือก **รวบรวมรายละเอียดของผลลัพธ์** เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="cb8e1-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="cb8e1-127">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="cb8e1-127">Return values</span></span>

<span data-ttu-id="cb8e1-128">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="cb8e1-128">*Real*</span></span>

<span data-ttu-id="cb8e1-129">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="cb8e1-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cb8e1-130">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cb8e1-130">Usage notes</span></span>

<span data-ttu-id="cb8e1-131">ฟังก์ชันนี้ส่งคืนค่า **0** (ศูนย์) เมื่อตัวเลือก **รวบรวมรายละเอียดผลลัพธ์** ของส่วนประกอบของ **Common\\File** ปัจจุบันถูกปิด</span><span class="sxs-lookup"><span data-stu-id="cb8e1-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="cb8e1-132">ในอาร์กิวเมนต์ `condition range` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว</span><span class="sxs-lookup"><span data-stu-id="cb8e1-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="cb8e1-133">ในอาร์กิวเมนต์ `condition value` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว</span><span class="sxs-lookup"><span data-stu-id="cb8e1-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="cb8e1-134">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cb8e1-134">Example</span></span>

<span data-ttu-id="cb8e1-135">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการใช้ฟังก์ชันนี้ ดูคู่มืองาน [ER ใช้ข้อมูลของผลลัพธ์รูปแบบสำหรับการตรวจนับและการรวม](tasks/er-format-counting-summing-1.md) ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **ซื้อ/พัฒนาบริการด้าน IT/ ส่วนประกอบโซลูชั่น**</span><span class="sxs-lookup"><span data-stu-id="cb8e1-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb8e1-136">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cb8e1-136">Additional resources</span></span>

[<span data-ttu-id="cb8e1-137">ฟังก์ชันการรวบรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cb8e1-137">Data collection functions</span></span>](er-functions-category-data-collection.md)
