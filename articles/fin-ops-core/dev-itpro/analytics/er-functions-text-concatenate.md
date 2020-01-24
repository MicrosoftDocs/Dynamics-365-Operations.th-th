---
title: ฟังก์ชัน CONCATENATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ CONCATENATE (ER)
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915774"
---
# <span data-ttu-id="1c104-103"><a name="CONCATENATE">ฟังก์ชัน CONCATENATE ER</a></span><span class="sxs-lookup"><span data-stu-id="1c104-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c104-104">ฟังก์ชัน `CONCATENATE` ส่งกลับสตริงข้อความที่ระบุทั้งหมดเป็นค่า *สตริง* หลังจากที่ได้เข้าร่วมเป็นหนึ่งสตริง</span><span class="sxs-lookup"><span data-stu-id="1c104-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c104-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="1c104-105">Syntax</span></span>

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="1c104-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="1c104-106">Arguments</span></span>

<span data-ttu-id="1c104-107">`text 1`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1c104-107">`text 1`: *String*</span></span>

<span data-ttu-id="1c104-108">การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1c104-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="1c104-109">ต้องระบุอาร์กิวเมนต์นี้</span><span class="sxs-lookup"><span data-stu-id="1c104-109">This argument is required.</span></span>

<span data-ttu-id="1c104-110">`text N`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1c104-110">`text N`: *String*</span></span>

<span data-ttu-id="1c104-111">การอ้างอิงถึงแหล่งข้อมูลของชนิดข้อมูล *สตริง*</span><span class="sxs-lookup"><span data-stu-id="1c104-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="1c104-112">อาร์กิวเมนต์เพิ่มเติมเหล่านี้เป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="1c104-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="1c104-113">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="1c104-113">Return values</span></span>

<span data-ttu-id="1c104-114">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="1c104-114">*String*</span></span>

<span data-ttu-id="1c104-115">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="1c104-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1c104-116">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="1c104-116">Example</span></span>

<span data-ttu-id="1c104-117">`CONCATENATE ("abc", "def")` ส่งกลับค่า **"abcdef"**</span><span class="sxs-lookup"><span data-stu-id="1c104-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1c104-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1c104-118">Usage notes</span></span>

<span data-ttu-id="1c104-119">นอกจากนี้ นิพจน์  `"abc" & "def"` ยังส่งกลับค่า **"abcdef"** ด้วย</span><span class="sxs-lookup"><span data-stu-id="1c104-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c104-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1c104-120">Additional resources</span></span>

[<span data-ttu-id="1c104-121">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="1c104-121">Text functions</span></span>](er-functions-category-text.md)
