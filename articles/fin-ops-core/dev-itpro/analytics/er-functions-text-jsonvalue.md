---
title: ฟังก์ชัน JSONVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ JSONVALUE (ER)
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 203fe1b1616f724ddf3015258306e0d9e8d4f599
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570027"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="06a29-103">ฟังก์ชัน JSONVALUE ER</span><span class="sxs-lookup"><span data-stu-id="06a29-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06a29-104">ฟังก์ชัน `JSONVALUE` แยกวิเคราะห์ข้อมูลในรูปแบบ JavaScript Object Notation (JSON) ที่เข้าถึงได้ที่พาธที่ระบุ และจะแยกค่าสเกลที่มีรหัสที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="06a29-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="06a29-105">จากนั้น จะส่งกลับค่าสเกลที่แยกเป็นค่า *สตริง*</span><span class="sxs-lookup"><span data-stu-id="06a29-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a29-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="06a29-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="06a29-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="06a29-107">Arguments</span></span>

<span data-ttu-id="06a29-108">`input`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="06a29-108">`input`: *String*</span></span>

<span data-ttu-id="06a29-109">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง* ซึ่งมีข้อมูล JSON</span><span class="sxs-lookup"><span data-stu-id="06a29-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="06a29-110">`path`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="06a29-110">`path`: *String*</span></span>

<span data-ttu-id="06a29-111">ตัวระบุของค่าสเกลของข้อมูล JSON</span><span class="sxs-lookup"><span data-stu-id="06a29-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="06a29-112">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="06a29-112">Return values</span></span>

<span data-ttu-id="06a29-113">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="06a29-113">*String*</span></span>

<span data-ttu-id="06a29-114">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="06a29-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="06a29-115">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="06a29-115">Example</span></span>

<span data-ttu-id="06a29-116">แหล่งข้อมูล **JsonField** ประกอบด้วยข้อมูลต่อไปนี้ในรูปแบบ: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**</span><span class="sxs-lookup"><span data-stu-id="06a29-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="06a29-117">ในกรณีนี้ นิพจน์ `JSONVALUE (JsonField, "BuildNumber")` ส่งกลับค่าต่อไปนี้ของชนิดข้อมูล *สตริง* : **"7.3.1234.1"**</span><span class="sxs-lookup"><span data-stu-id="06a29-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06a29-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="06a29-118">Additional resources</span></span>

[<span data-ttu-id="06a29-119">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="06a29-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]