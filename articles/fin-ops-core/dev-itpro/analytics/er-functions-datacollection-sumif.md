---
title: ฟังก์ชัน SUMIF ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SUMIF
author: NickSelin
manager: kfend
ms.date: 04/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9df7be0825203f91434d348385c1ee358ae555ea
ms.sourcegitcommit: ef6fd78c817f93610771cfb2477f52f16b882164
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2020
ms.locfileid: "3290211"
---
# <a name=""></a><span data-ttu-id="2ebc0-103"><a name="SUMIF">ฟังก์ชัน SUMIF ER</a></span><span class="sxs-lookup"><span data-stu-id="2ebc0-103"><a name="SUMIF">SUMIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ebc0-104">ฟังก์ชัน `SUMIF` ส่งกลับค่า *จำนวนจริง* ที่แสดงถึงผลรวมของค่าที่ส่งคืนโดยการผูกองค์ประกอบรูปแบบและการเก็บรวบรวม เมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="2ebc0-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="2ebc0-105">เงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="2ebc0-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebc0-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="2ebc0-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="2ebc0-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="2ebc0-107">Arguments</span></span>

<span data-ttu-id="2ebc0-108">`key name for summing`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="2ebc0-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="2ebc0-109">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ได้รับการกำหนดค่าในคุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ซึ่งค่าของการผูกจะต้องใช้สำหรับการสรุปวัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="2ebc0-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="2ebc0-110">คุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** สามารถกำหนดค่าสำหรับส่วนประกอบ **ลำดับ** หรือส่วนประกอบ **XML Element** ของรูปแบบ ER ที่อยู่ภายใต้ส่วนประกอบของ **Common\\File** ที่ตัวเลือก **รวบรวมรายละเอียดของผลลัพธ์** เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="2ebc0-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ebc0-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="2ebc0-111">Return values</span></span>

<span data-ttu-id="2ebc0-112">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="2ebc0-112">*Real*</span></span>

<span data-ttu-id="2ebc0-113">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="2ebc0-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2ebc0-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2ebc0-114">Usage notes</span></span>

<span data-ttu-id="2ebc0-115">ฟังก์ชันนี้ส่งคืนค่า **0** (ศูนย์) เมื่อตัวเลือก **รวบรวมรายละเอียดผลลัพธ์** ของส่วนประกอบของ **Common\\File** ปัจจุบันถูกปิด</span><span class="sxs-lookup"><span data-stu-id="2ebc0-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="2ebc0-116">ในอาร์กิวเมนต์ `condition range` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว</span><span class="sxs-lookup"><span data-stu-id="2ebc0-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="2ebc0-117">ในอาร์กิวเมนต์ `condition value` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว</span><span class="sxs-lookup"><span data-stu-id="2ebc0-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="2ebc0-118">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2ebc0-118">Example</span></span>

<span data-ttu-id="2ebc0-119">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการใช้ฟังก์ชันนี้ ดูคู่มืองาน [ER ใช้ข้อมูลของผลลัพธ์รูปแบบสำหรับการตรวจนับและการรวม](tasks/er-format-counting-summing-1.md) ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **ซื้อ/พัฒนาบริการด้าน IT/ ส่วนประกอบโซลูชั่น**</span><span class="sxs-lookup"><span data-stu-id="2ebc0-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="2ebc0-120">สําหรับข้อมูลและตัวอย่างเพิ่มเติมเกี่ยวกับการใช้ฟังก์ชันนี้ ให้ดูที่ [เลื่อนการดําเนินการขององค์ประกอบลําดับในรูปแบบ ER ](er-defer-sequence-element.md#Example) และ [เลื่อนการดําเนินการขององค์ประกอบ XML ในรูปแบบ ER](er-defer-xml-element.md#Example)</span><span class="sxs-lookup"><span data-stu-id="2ebc0-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ebc0-121">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2ebc0-121">Additional resources</span></span>

[<span data-ttu-id="2ebc0-122">ฟังก์ชันการรวบรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2ebc0-122">Data collection functions</span></span>](er-functions-category-data-collection.md)
