---
title: ฟังก์ชัน CHAR ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CHAR (ER)
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a9f0f70c250592bf74b1a1df823e66803e853a64
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683002"
---
# <a name="char-er-function"></a><span data-ttu-id="716b6-103">ฟังก์ชัน CHAR ER</span><span class="sxs-lookup"><span data-stu-id="716b6-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="716b6-104">ฟังก์ชัน `CHAR` ส่งกลับค่า *สตริง* ที่นำเสนออักขระเดี่ยวที่ถูกอ้างอิงโดยหมายเลข Unicode ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="716b6-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="716b6-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="716b6-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="716b6-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="716b6-106">Arguments</span></span>

<span data-ttu-id="716b6-107">`number`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="716b6-107">`number`: *Integer*</span></span>

<span data-ttu-id="716b6-108">ตัวเลขที่สอดคล้องกับอักขระเดี่ยวที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="716b6-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="716b6-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="716b6-109">Return values</span></span>

<span data-ttu-id="716b6-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="716b6-110">*String*</span></span>

<span data-ttu-id="716b6-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="716b6-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="716b6-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="716b6-112">Usage notes</span></span>

<span data-ttu-id="716b6-113">สตริงที่ฟังก์ชันนี้ส่งคืนจะขึ้นอยู่กับการเข้ารหัสที่เลือกไว้ในองค์ประกอบรูปแบบ **FILE** หลัก</span><span class="sxs-lookup"><span data-stu-id="716b6-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="716b6-114">สำหรับรายการของการเข้ารหัสที่สนับสนุน ดู [การเข้ารหัสคลาส](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="716b6-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="716b6-115">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="716b6-115">Example</span></span>

<span data-ttu-id="716b6-116">`CHAR (255)` ส่งกลับค่า **"ÿ"**</span><span class="sxs-lookup"><span data-stu-id="716b6-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="716b6-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="716b6-117">Additional resources</span></span>

[<span data-ttu-id="716b6-118">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="716b6-118">Text functions</span></span>](er-functions-category-text.md)
