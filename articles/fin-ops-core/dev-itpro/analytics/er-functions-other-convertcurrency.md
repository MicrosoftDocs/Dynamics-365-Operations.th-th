---
title: ฟังก์ชัน CONVERTCURRENCY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CONVERTCURRENCY (ER)
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 0f0d5bace9b62cf6f0d7576744a6cc271666bf73
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567651"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="7dc75-103">ฟังก์ชัน CONVERTCURRENCY ER</span><span class="sxs-lookup"><span data-stu-id="7dc75-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dc75-104">ฟังก์ชัน `CONVERTCURRENCY` ส่งคืนค่า *จริง* ที่แสดงผลลัพธ์ของการแปลงยอดเงินที่ระบุจากสกุลเงินต้นทางที่ระบุเป็นสกุลเงินเป้าหมายที่ระบุ โดยใช้การตั้งค่าของบริษัทที่ระบุในวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="7dc75-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc75-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="7dc75-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="7dc75-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="7dc75-106">Arguments</span></span>

<span data-ttu-id="7dc75-107">`amount`: *จำนวนเต็ม* หรือ *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="7dc75-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="7dc75-108">ค่าตัวเลขที่แสดงถึงยอดเงินที่ต้องถูกแปลง</span><span class="sxs-lookup"><span data-stu-id="7dc75-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="7dc75-109">`source currency`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="7dc75-109">`source currency`: *String*</span></span>

<span data-ttu-id="7dc75-110">รหัสของสกุลเงินต้นทาง</span><span class="sxs-lookup"><span data-stu-id="7dc75-110">The code of the source currency.</span></span>

<span data-ttu-id="7dc75-111">`target currency`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="7dc75-111">`target currency`: *String*</span></span>

<span data-ttu-id="7dc75-112">รหัสของสกุลเงินเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="7dc75-112">The code of the target currency.</span></span>

<span data-ttu-id="7dc75-113">`date`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="7dc75-113">`date`: *Date*</span></span>

<span data-ttu-id="7dc75-114">ค่า *วันที่* ที่แสดงถึงวันที่ที่ใช้ในการกำหนดอัตราแลกเปลี่ยนสำหรับการแปลง</span><span class="sxs-lookup"><span data-stu-id="7dc75-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="7dc75-115">`company`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="7dc75-115">`company`: *String*</span></span>

<span data-ttu-id="7dc75-116">ค่า *สตริง* ที่แสดงถึงรหัสของบริษัทที่จัดหาการตั้งค่าที่จะใช้สำหรับการแปลง</span><span class="sxs-lookup"><span data-stu-id="7dc75-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="7dc75-117">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="7dc75-117">Return values</span></span>

<span data-ttu-id="7dc75-118">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="7dc75-118">*Real*</span></span>

<span data-ttu-id="7dc75-119">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="7dc75-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7dc75-120">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="7dc75-120">Example</span></span>

<span data-ttu-id="7dc75-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` ส่งกลับค่าหนึ่งยูโรที่เทียบเท่ากับดอลลาร์สหรัฐฯ ในวันที่รอบเวลาปัจจุบัน ตามการตั้งค่าสำหรับบริษัท **DEMF**</span><span class="sxs-lookup"><span data-stu-id="7dc75-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7dc75-122">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7dc75-122">Additional resources</span></span>

[<span data-ttu-id="7dc75-123">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="7dc75-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]