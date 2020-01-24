---
title: ฟังก์ชัน JSONVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ JSONVALUE (ER)
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: d8209f8ce9d244ab7c82f897e4f59283e94e0522
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915682"
---
# <span data-ttu-id="414ed-103"><a name="JSONVALUE">ฟังก์ชัน JSONVALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="414ed-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="414ed-104">ฟังก์ชัน `JSONVALUE` แยกวิเคราะห์ข้อมูลในรูปแบบ JavaScript Object Notation (JSON) ที่เข้าถึงได้ที่พาธที่ระบุ และจะแยกค่าสเกลที่มีรหัสที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="414ed-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="414ed-105">จากนั้น จะส่งกลับค่าสเกลที่แยกเป็นค่า *สตริง*</span><span class="sxs-lookup"><span data-stu-id="414ed-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="414ed-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="414ed-106">Syntax</span></span>

```
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="414ed-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="414ed-107">Arguments</span></span>

<span data-ttu-id="414ed-108">`input`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="414ed-108">`input`: *String*</span></span>

<span data-ttu-id="414ed-109">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง* ซึ่งมีข้อมูล JSON</span><span class="sxs-lookup"><span data-stu-id="414ed-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="414ed-110">`path`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="414ed-110">`path`: *String*</span></span>

<span data-ttu-id="414ed-111">ตัวระบุของค่าสเกลของข้อมูล JSON</span><span class="sxs-lookup"><span data-stu-id="414ed-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="414ed-112">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="414ed-112">Return values</span></span>

<span data-ttu-id="414ed-113">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="414ed-113">*String*</span></span>

<span data-ttu-id="414ed-114">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="414ed-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="414ed-115">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="414ed-115">Example</span></span>

<span data-ttu-id="414ed-116">แหล่งข้อมูล **JsonField** ประกอบด้วยข้อมูลต่อไปนี้ในรูปแบบ: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**</span><span class="sxs-lookup"><span data-stu-id="414ed-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="414ed-117">ในกรณีนี้ นิพจน์ `JSONVALUE (JsonField, "BuildNumber")` ส่งกลับค่าต่อไปนี้ของชนิดข้อมูล *สตริง* : **"7.3.1234.1"**</span><span class="sxs-lookup"><span data-stu-id="414ed-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="414ed-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="414ed-118">Additional resources</span></span>

[<span data-ttu-id="414ed-119">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="414ed-119">Text functions</span></span>](er-functions-category-text.md)
