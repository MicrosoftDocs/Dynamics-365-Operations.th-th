---
title: ฟังก์ชัน FIRST ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FIRST
author: NickSelin
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
ms.openlocfilehash: d30c8481866ccf3f7080197b37586a0460a4ad2c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746590"
---
# <a name="first-er-function"></a><span data-ttu-id="18dec-103">ฟังก์ชัน FIRST ER</span><span class="sxs-lookup"><span data-stu-id="18dec-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18dec-104">ฟังก์ชัน `FIRST` ส่งกลับเรกคอร์ดแรกของรายการที่ระบุเป็นค่า *คอนเทนเนอร์ (เรกคอร์ด)* หากรายการนั้นไม่ว่าง</span><span class="sxs-lookup"><span data-stu-id="18dec-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="18dec-105">ถ้ารายการว่าง ฟังก์ชันนี้จะแสดงข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="18dec-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="18dec-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="18dec-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="18dec-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="18dec-107">Arguments</span></span>

<span data-ttu-id="18dec-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="18dec-108">`list`: *Record list*</span></span>

<span data-ttu-id="18dec-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="18dec-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="18dec-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="18dec-110">Return values</span></span>

<span data-ttu-id="18dec-111">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="18dec-111">*Container (record)*</span></span>

<span data-ttu-id="18dec-112">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="18dec-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="18dec-113">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="18dec-113">Example 1</span></span>

<span data-ttu-id="18dec-114">นิพจน์ `FIRST(SPLIT("ABC",1)).Value` ส่งกลับค่าข้อความ **"A"**</span><span class="sxs-lookup"><span data-stu-id="18dec-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="18dec-115">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="18dec-115">Example 2</span></span>

<span data-ttu-id="18dec-116">นิพจน์ `FIRST(SPLIT("",1)).Value`แสดงข้อยกเว้นขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="18dec-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18dec-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="18dec-117">Additional resources</span></span>

[<span data-ttu-id="18dec-118">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="18dec-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]