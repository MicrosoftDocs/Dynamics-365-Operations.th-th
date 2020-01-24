---
title: ฟังก์ชัน FIRSTORNULL ER
description: หัวข้อนี้อธิบายข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FIRSTORNULL
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 075b2e064641061adf5404591a784311b6d28697
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917338"
---
# <span data-ttu-id="46850-103"><a name="FIRSTORNULL">ฟังก์ชัน FIRSTORNULL ER</a></span><span class="sxs-lookup"><span data-stu-id="46850-103"><a name="FIRSTORNULL">FIRSTORNULL ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46850-104">ฟังก์ชัน `FIRSTORNULL` ส่งกลับเรกคอร์ดแรกของรายการที่ระบุเป็นค่า *คอนเทนเนอร์ (เรกคอร์ด)* หากเรกคอร์ดไม่ว่าง</span><span class="sxs-lookup"><span data-stu-id="46850-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="46850-105">ถ้าเรกคอร์ดว่าง ฟังก์ชันนี้จะส่งกลับค่า*คอนเทนเนอร์ (เรกคอร์ด)* ที่เป็น null</span><span class="sxs-lookup"><span data-stu-id="46850-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="46850-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="46850-106">Syntax</span></span>

```
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="46850-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="46850-107">Arguments</span></span>

<span data-ttu-id="46850-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="46850-108">`list`: *Record list*</span></span>

<span data-ttu-id="46850-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="46850-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="46850-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="46850-110">Return values</span></span>

<span data-ttu-id="46850-111">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="46850-111">*Container (record)*</span></span>

<span data-ttu-id="46850-112">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="46850-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="46850-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="46850-113">Example</span></span>

<span data-ttu-id="46850-114">นิพจน์ `FIRSTORNULL(SPLIT("",1)).Value` ส่งกลับสตริงที่ว่างเปล่า (**""**)</span><span class="sxs-lookup"><span data-stu-id="46850-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46850-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="46850-115">Additional resources</span></span>

[<span data-ttu-id="46850-116">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="46850-116">List functions</span></span>](er-functions-category-list.md)
