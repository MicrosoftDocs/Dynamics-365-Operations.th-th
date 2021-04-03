---
title: ฟังก์ชัน CONCATENATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CONCATENATE (ER)
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569616"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="87e07-103">ฟังก์ชัน CONCATENATE ER</span><span class="sxs-lookup"><span data-stu-id="87e07-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87e07-104">ฟังก์ชัน `CONCATENATE` ส่งกลับสตริงข้อความที่ระบุทั้งหมดเป็นค่า *สตริง* หลังจากที่ได้เข้าร่วมเป็นหนึ่งสตริง</span><span class="sxs-lookup"><span data-stu-id="87e07-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e07-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="87e07-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="87e07-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="87e07-106">Arguments</span></span>

<span data-ttu-id="87e07-107">`text 1`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="87e07-107">`text 1`: *String*</span></span>

<span data-ttu-id="87e07-108">การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *สตริง*</span><span class="sxs-lookup"><span data-stu-id="87e07-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="87e07-109">ต้องระบุอาร์กิวเมนต์นี้</span><span class="sxs-lookup"><span data-stu-id="87e07-109">This argument is required.</span></span>

<span data-ttu-id="87e07-110">`text N`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="87e07-110">`text N`: *String*</span></span>

<span data-ttu-id="87e07-111">การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *สตริง*</span><span class="sxs-lookup"><span data-stu-id="87e07-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="87e07-112">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="87e07-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="87e07-113">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="87e07-113">Return values</span></span>

<span data-ttu-id="87e07-114">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="87e07-114">*String*</span></span>

<span data-ttu-id="87e07-115">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="87e07-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="87e07-116">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="87e07-116">Example</span></span>

<span data-ttu-id="87e07-117">`CONCATENATE ("abc", "def")` ส่งกลับค่า **"abcdef"**</span><span class="sxs-lookup"><span data-stu-id="87e07-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="87e07-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="87e07-118">Usage notes</span></span>

<span data-ttu-id="87e07-119">นอกจากนี้ นิพจน์  `"abc" & "def"` ยังส่งกลับค่า **"abcdef"** ด้วย</span><span class="sxs-lookup"><span data-stu-id="87e07-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87e07-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="87e07-120">Additional resources</span></span>

[<span data-ttu-id="87e07-121">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="87e07-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]