---
title: ฟังก์ชัน FA_BALANCE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ FA_BALANCE (ER)
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: ec78b9c5bf800503023315eb893076486b0a1fb0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744330"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="4e19b-103">ฟังก์ชัน FA_BALANCE ER</span><span class="sxs-lookup"><span data-stu-id="4e19b-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e19b-104">ฟังก์ชัน `FA_BALANCE` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่ประกอบด้วยข้อมูลสำหรับยอดดุลสินทรัพย์ถาวรสำหรับสินค้าสินทรัพย์ถาวรที่ระบุ รหัสแบบจำลองมูลค่า ปีการรายงาน และวันที่ที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="4e19b-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e19b-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="4e19b-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="4e19b-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="4e19b-106">Arguments</span></span>

<span data-ttu-id="4e19b-107">`fixed asset code`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="4e19b-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="4e19b-108">ค่า *สตริง* ที่แสดงถึงรหัสของรายการสินทรัพย์ถาวรที่มีการคำนวณยอดดุล</span><span class="sxs-lookup"><span data-stu-id="4e19b-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="4e19b-109">`value model code`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="4e19b-109">`value model code`: *String*</span></span>

<span data-ttu-id="4e19b-110">ค่า *สตริง* ที่แสดงถึงรหัสของแบบจำลองค่าที่มีการคำนวณยอดดุล</span><span class="sxs-lookup"><span data-stu-id="4e19b-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="4e19b-111">`reporting year`: *ค่าการแจงนับ*</span><span class="sxs-lookup"><span data-stu-id="4e19b-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="4e19b-112">ค่าการแจงนับของการแจงนับแอพลิเคชัน **AssetYear** ที่กำหนดรอบระยะเวลาสำหรับการคำนวณยอดดุล</span><span class="sxs-lookup"><span data-stu-id="4e19b-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="4e19b-113">`reporting date`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="4e19b-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="4e19b-114">ค่า *วันที่* ที่กำหนดวันที่สำหรับการคำนวณยอดดุล</span><span class="sxs-lookup"><span data-stu-id="4e19b-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="4e19b-115">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="4e19b-115">Return values</span></span>

<span data-ttu-id="4e19b-116">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="4e19b-116">*Container (record)*</span></span>

<span data-ttu-id="4e19b-117">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="4e19b-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="4e19b-118">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="4e19b-118">Example</span></span>

<span data-ttu-id="4e19b-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` ส่งคืนคอนเทนเนอร์ข้อมูลของยอดดุลสำหรับ สินทรัพย์ถาวร **COMP-000001** ที่มีการเตรียมไว้สำหรับแบบจำลองมูลค่า **ปัจจุบัน** ในวันที่รอบเวลาของแอพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4e19b-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e19b-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4e19b-120">Additional resources</span></span>

[<span data-ttu-id="4e19b-121">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="4e19b-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]