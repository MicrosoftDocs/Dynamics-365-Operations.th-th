---
title: ฟังก์ชัน FIRST ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FIRST
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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917361"
---
# <span data-ttu-id="4c23d-103"><a name="FIRST">ฟังก์ชัน FIRST ER</a></span><span class="sxs-lookup"><span data-stu-id="4c23d-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c23d-104">ฟังก์ชัน `FIRST` ส่งกลับเรกคอร์ดแรกของรายการที่ระบุเป็นค่า *คอนเทนเนอร์ (เรกคอร์ด)* หากรายการนั้นไม่ว่าง</span><span class="sxs-lookup"><span data-stu-id="4c23d-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="4c23d-105">ถ้ารายการว่าง ฟังก์ชันนี้จะแสดงข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="4c23d-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c23d-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="4c23d-106">Syntax</span></span>

```
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="4c23d-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="4c23d-107">Arguments</span></span>

<span data-ttu-id="4c23d-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="4c23d-108">`list`: *Record list*</span></span>

<span data-ttu-id="4c23d-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="4c23d-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4c23d-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="4c23d-110">Return values</span></span>

<span data-ttu-id="4c23d-111">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="4c23d-111">*Container (record)*</span></span>

<span data-ttu-id="4c23d-112">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="4c23d-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="4c23d-113">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="4c23d-113">Example 1</span></span>

<span data-ttu-id="4c23d-114">นิพจน์ `FIRST(SPLIT("ABC",1)).Value` ส่งกลับค่าข้อความ **"A"**</span><span class="sxs-lookup"><span data-stu-id="4c23d-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4c23d-115">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="4c23d-115">Example 2</span></span>

<span data-ttu-id="4c23d-116">นิพจน์ `FIRST(SPLIT("",1)).Value`แสดงข้อยกเว้นขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="4c23d-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c23d-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4c23d-117">Additional resources</span></span>

[<span data-ttu-id="4c23d-118">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="4c23d-118">List functions</span></span>](er-functions-category-list.md)
