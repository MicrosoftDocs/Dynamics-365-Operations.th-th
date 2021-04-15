---
title: ฟังก์ชัน ER COUNTIF
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) COUNTIF
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: bebb3d3b810e68fa6a0d3f4deb92b750b7c9a9f3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755311"
---
# <a name="countif-er-function"></a><span data-ttu-id="bd2f1-103">ฟังก์ชัน ER COUNTIF</span><span class="sxs-lookup"><span data-stu-id="bd2f1-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd2f1-104">ฟังก์ชัน `COUNTIF` ส่งกลับค่า *จำนวนเต็ม* ที่แสดงถึงจำนวนขององค์ประกอบรูปแบบที่ถูกรวบรวมเมื่อองค์ประกอบรูปแบบถูกใช้ในการสร้างเอกสารขาออกในระหว่างการเรียกใช้รูปแบบและที่ตอบสนองเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="bd2f1-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="bd2f1-105">เงื่อนไขประกอบด้วยช่วงคีย์และค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="bd2f1-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd2f1-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="bd2f1-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="bd2f1-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="bd2f1-107">Arguments</span></span>

<span data-ttu-id="bd2f1-108">`condition range`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="bd2f1-108">`condition range`: *String*</span></span>

<span data-ttu-id="bd2f1-109">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="bd2f1-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="bd2f1-110">`condition value`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="bd2f1-110">`condition value`: *String*</span></span>

<span data-ttu-id="bd2f1-111">ค่าที่ถูกส่งกลับโดยนิพจน์ที่ถูกกำหนดค่าในคุณสมบัติ **ค่าคีย์ข้อมูลที่รวบรวม** ของส่วนประกอบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="bd2f1-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="bd2f1-112">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="bd2f1-112">Return values</span></span>

<span data-ttu-id="bd2f1-113">*จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="bd2f1-113">*Integer*</span></span>

<span data-ttu-id="bd2f1-114">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="bd2f1-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bd2f1-115">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bd2f1-115">Usage notes</span></span>

<span data-ttu-id="bd2f1-116">คุณสมบัติ **ชื่อคีย์ข้อมูลที่รวบรวม** และ **ค่าคีย์ข้อมูลที่รวบรวม** สามารถกำหนดค่าสำหรับส่วนประกอบ **ลำดับ** หรือส่วนประกอบ **XML Element** ของรูปแบบ ER ที่อยู่ภายใต้ส่วนประกอบของ **Common\\File** ที่ตัวเลือก **รวบรวมรายละเอียดของผลลัพธ์** เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="bd2f1-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="bd2f1-117">ฟังก์ชันนี้ส่งคืนค่า **0** (ศูนย์) เมื่อตัวเลือก **รวบรวมรายละเอียดผลลัพธ์** ของส่วนประกอบของ **Common\\File** ปัจจุบันถูกปิด</span><span class="sxs-lookup"><span data-stu-id="bd2f1-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="bd2f1-118">ในอาร์กิวเมนต์ `condition range` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว</span><span class="sxs-lookup"><span data-stu-id="bd2f1-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="bd2f1-119">ในอาร์กิวเมนต์ `condition value` อักขระตัวแทน **"\*"** สามารถใช้เพื่อแสดงอักขระหลายตัว</span><span class="sxs-lookup"><span data-stu-id="bd2f1-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="bd2f1-120">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="bd2f1-120">Example</span></span>

<span data-ttu-id="bd2f1-121">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการใช้ฟังก์ชันนี้ ดูคู่มืองาน [ER ใช้ข้อมูลของผลลัพธ์รูปแบบสำหรับการตรวจนับและการรวม](tasks/er-format-counting-summing-1.md) ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **ซื้อ/พัฒนาบริการด้าน IT/ ส่วนประกอบโซลูชั่น**</span><span class="sxs-lookup"><span data-stu-id="bd2f1-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd2f1-122">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bd2f1-122">Additional resources</span></span>

[<span data-ttu-id="bd2f1-123">ฟังก์ชันการรวบรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bd2f1-123">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]