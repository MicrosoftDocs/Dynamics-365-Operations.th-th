---
title: ฟังก์ชัน FA_SUM ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ FA_SUM (ER)
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 1c46f945a9caae2836886d051da820658e8be9af
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687707"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="0e5f2-103">ฟังก์ชัน FA_SUM ER</span><span class="sxs-lookup"><span data-stu-id="0e5f2-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e5f2-104">ฟังก์ชัน `FA_SUM` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่ประกอบด้วยข้อมูลสำหรับยอดเงินสินทรัพย์ถาวรสำหรับสินค้าสินทรัพย์ถาวรที่ระบุ รหัสแบบจำลองมูลค่า และรอบระยะเวลาของวันที่</span><span class="sxs-lookup"><span data-stu-id="0e5f2-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e5f2-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="0e5f2-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="0e5f2-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="0e5f2-106">Arguments</span></span>

<span data-ttu-id="0e5f2-107">`fixed asset code`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0e5f2-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="0e5f2-108">ค่า *สตริง* ที่แสดงถึงรหัสของรายการสินทรัพย์ถาวรที่มีการคำนวณยอดดุล</span><span class="sxs-lookup"><span data-stu-id="0e5f2-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="0e5f2-109">`value model code`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="0e5f2-109">`value model code`: *String*</span></span>

<span data-ttu-id="0e5f2-110">ค่า *สตริง* ที่แสดงถึงรหัสของแบบจำลองค่าที่มีการคำนวณยอดดุล</span><span class="sxs-lookup"><span data-stu-id="0e5f2-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="0e5f2-111">`start date`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="0e5f2-111">`start date`: *Date*</span></span>

<span data-ttu-id="0e5f2-112">ค่า *วันที่* แสดงถึงวันที่เริ่มต้นของรอบระยะเวลาที่มีการคำนวณยอดเงินสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="0e5f2-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="0e5f2-113">`end date`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="0e5f2-113">`end date`: *Date*</span></span>

<span data-ttu-id="0e5f2-114">ค่า *วันที่* แสดงถึงวันที่สิ้นสุดของรอบระยะเวลาที่มีการคำนวณยอดเงินสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="0e5f2-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="0e5f2-115">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="0e5f2-115">Return values</span></span>

<span data-ttu-id="0e5f2-116">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="0e5f2-116">*Container (record)*</span></span>

<span data-ttu-id="0e5f2-117">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="0e5f2-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="0e5f2-118">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0e5f2-118">Example</span></span>

<span data-ttu-id="0e5f2-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` ส่งกลับค่าคอนเทนเนอร์ข้อมูลสำหรับสินทรัพย์ถาวร **COMP-000001** ที่เตรียมไว้สำหรับแบบจำลองค่า **ปัจจุบัน** และสำหรับรอบระยะเวลาตั้งแต่ **Date1** ถึง **Date2**</span><span class="sxs-lookup"><span data-stu-id="0e5f2-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e5f2-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0e5f2-120">Additional resources</span></span>

[<span data-ttu-id="0e5f2-121">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="0e5f2-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
