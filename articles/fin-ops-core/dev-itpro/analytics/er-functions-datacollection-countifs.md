---
title: ฟังก์ชัน ER COUNTIFS
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) COUNTIFS
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 554750b2dae5ec1f0fcf6fdbdf439b4dbe4fa615
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681145"
---
# <a name="countifs-er-function"></a><span data-ttu-id="f56fa-103">ฟังก์ชัน ER COUNTIFS</span><span class="sxs-lookup"><span data-stu-id="f56fa-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f56fa-104">ฟังก์ชัน `COUNTIFS` ส่งกลับค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนขององค์ประกอบรูปแบบที่ถูกรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f56fa-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="f56fa-105">แต่ละเงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="f56fa-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f56fa-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="f56fa-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="f56fa-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="f56fa-107">Arguments</span></span>

<span data-ttu-id="f56fa-108">`condition 1 range`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="f56fa-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="f56fa-109">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="f56fa-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="f56fa-110">อาร์กิวเมนต์นี้เป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="f56fa-110">This argument is mandatory.</span></span>

<span data-ttu-id="f56fa-111">`condition 1 value`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="f56fa-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="f56fa-112">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="f56fa-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="f56fa-113">อาร์กิวเมนต์นี้เป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="f56fa-113">This argument is mandatory.</span></span>

<span data-ttu-id="f56fa-114">`condition N range`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="f56fa-114">`condition N range`: *String*</span></span>

<span data-ttu-id="f56fa-115">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="f56fa-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="f56fa-116">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f56fa-116">These additional arguments are optional.</span></span>

<span data-ttu-id="f56fa-117">`condition N value`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="f56fa-117">`condition N value`: *String*</span></span>

<span data-ttu-id="f56fa-118">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="f56fa-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="f56fa-119">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f56fa-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="f56fa-120">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="f56fa-120">Return values</span></span>

<span data-ttu-id="f56fa-121">*จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="f56fa-121">*Integer*</span></span>

<span data-ttu-id="f56fa-122">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="f56fa-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f56fa-123">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f56fa-123">Usage notes</span></span>

<span data-ttu-id="f56fa-124">คุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** และ **ค่าคีย์ข้อมูลที่รวบรวม** สามารถกำหนดค่าสำหรับส่วนประกอบ **ลำดับ** หรือส่วนประกอบ **XML Element** ของรูปแบบ ER ที่อยู่ภายใต้ส่วนประกอบของ **Common\\File** ที่ตัวเลือก **รวบรวมรายละเอียดของผลลัพธ์** เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="f56fa-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="f56fa-125">ฟังก์ชันนี้ส่งคืนค่า **0** (ศูนย์) เมื่อตัวเลือก **รวบรวมรายละเอียดผลลัพธ์** ของส่วนประกอบของ **Common\\File** ปัจจุบันถูกปิด</span><span class="sxs-lookup"><span data-stu-id="f56fa-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="f56fa-126">ในอาร์กิวเมนต์ `condition range` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว</span><span class="sxs-lookup"><span data-stu-id="f56fa-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="f56fa-127">ในอาร์กิวเมนต์ `condition value` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว</span><span class="sxs-lookup"><span data-stu-id="f56fa-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="f56fa-128">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f56fa-128">Example</span></span>

<span data-ttu-id="f56fa-129">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการใช้ฟังก์ชันนี้ ดูคู่มืองาน [ER ใช้ข้อมูลของผลลัพธ์รูปแบบสำหรับการตรวจนับและการรวม](tasks/er-format-counting-summing-1.md) ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **ซื้อ/พัฒนาบริการด้าน IT/ ส่วนประกอบโซลูชั่น**</span><span class="sxs-lookup"><span data-stu-id="f56fa-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f56fa-130">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f56fa-130">Additional resources</span></span>

[<span data-ttu-id="f56fa-131">ฟังก์ชันการรวบรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f56fa-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
