---
title: ฟังก์ชัน CONVERTCURRENCY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CONVERTCURRENCY (ER)
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
ms.openlocfilehash: a27fd30236a61576ab9063010ea6bc38d9cf7a1e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686797"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="1e3f0-103">ฟังก์ชัน CONVERTCURRENCY ER</span><span class="sxs-lookup"><span data-stu-id="1e3f0-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e3f0-104">ฟังก์ชัน `CONVERTCURRENCY` ส่งคืนค่า *จริง* ที่แสดงผลลัพธ์ของการแปลงยอดเงินที่ระบุจากสกุลเงินต้นทางที่ระบุเป็นสกุลเงินเป้าหมายที่ระบุ โดยใช้การตั้งค่าของบริษัทที่ระบุในวันที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1e3f0-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e3f0-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="1e3f0-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="1e3f0-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="1e3f0-106">Arguments</span></span>

<span data-ttu-id="1e3f0-107">`amount`: *จำนวนเต็ม* หรือ *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="1e3f0-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="1e3f0-108">ค่าตัวเลขที่แสดงถึงยอดเงินที่ต้องถูกแปลง</span><span class="sxs-lookup"><span data-stu-id="1e3f0-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="1e3f0-109">`source currency`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1e3f0-109">`source currency`: *String*</span></span>

<span data-ttu-id="1e3f0-110">รหัสของสกุลเงินต้นทาง</span><span class="sxs-lookup"><span data-stu-id="1e3f0-110">The code of the source currency.</span></span>

<span data-ttu-id="1e3f0-111">`target currency`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1e3f0-111">`target currency`: *String*</span></span>

<span data-ttu-id="1e3f0-112">รหัสของสกุลเงินเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="1e3f0-112">The code of the target currency.</span></span>

<span data-ttu-id="1e3f0-113">`date`: *วันที่*</span><span class="sxs-lookup"><span data-stu-id="1e3f0-113">`date`: *Date*</span></span>

<span data-ttu-id="1e3f0-114">ค่า *วันที่* ที่แสดงถึงวันที่ที่ใช้ในการกำหนดอัตราแลกเปลี่ยนสำหรับการแปลง</span><span class="sxs-lookup"><span data-stu-id="1e3f0-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="1e3f0-115">`company`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1e3f0-115">`company`: *String*</span></span>

<span data-ttu-id="1e3f0-116">ค่า *สตริง* ที่แสดงถึงรหัสของบริษัทที่จัดหาการตั้งค่าที่จะใช้สำหรับการแปลง</span><span class="sxs-lookup"><span data-stu-id="1e3f0-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="1e3f0-117">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="1e3f0-117">Return values</span></span>

<span data-ttu-id="1e3f0-118">*จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="1e3f0-118">*Real*</span></span>

<span data-ttu-id="1e3f0-119">ค่าตัวเลขที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="1e3f0-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="1e3f0-120">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="1e3f0-120">Example</span></span>

<span data-ttu-id="1e3f0-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` ส่งกลับค่าหนึ่งยูโรที่เทียบเท่ากับดอลลาร์สหรัฐฯ ในวันที่รอบเวลาปัจจุบัน ตามการตั้งค่าสำหรับบริษัท **DEMF**</span><span class="sxs-lookup"><span data-stu-id="1e3f0-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e3f0-122">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1e3f0-122">Additional resources</span></span>

[<span data-ttu-id="1e3f0-123">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="1e3f0-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
