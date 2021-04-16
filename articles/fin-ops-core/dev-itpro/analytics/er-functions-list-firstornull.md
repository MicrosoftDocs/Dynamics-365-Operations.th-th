---
title: ฟังก์ชัน FIRSTORNULL ER
description: หัวข้อนี้อธิบายข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FIRSTORNULL
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: 1ccc094fc468470ffc857c729b6d8402796785d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753227"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="7a16f-103">ฟังก์ชัน FIRSTORNULL ER</span><span class="sxs-lookup"><span data-stu-id="7a16f-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a16f-104">ฟังก์ชัน `FIRSTORNULL` ส่งกลับเรกคอร์ดแรกของรายการที่ระบุเป็นค่า *คอนเทนเนอร์ (เรกคอร์ด)* หากเรกคอร์ดไม่ว่าง</span><span class="sxs-lookup"><span data-stu-id="7a16f-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="7a16f-105">ถ้าเรกคอร์ดว่าง ฟังก์ชันนี้จะส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่เป็น null</span><span class="sxs-lookup"><span data-stu-id="7a16f-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a16f-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="7a16f-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="7a16f-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="7a16f-107">Arguments</span></span>

<span data-ttu-id="7a16f-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="7a16f-108">`list`: *Record list*</span></span>

<span data-ttu-id="7a16f-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="7a16f-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7a16f-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="7a16f-110">Return values</span></span>

<span data-ttu-id="7a16f-111">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="7a16f-111">*Container (record)*</span></span>

<span data-ttu-id="7a16f-112">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="7a16f-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="7a16f-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="7a16f-113">Example</span></span>

<span data-ttu-id="7a16f-114">นิพจน์ `FIRSTORNULL(SPLIT("",1)).Value` ส่งกลับสตริงที่ว่างเปล่า (**""**)</span><span class="sxs-lookup"><span data-stu-id="7a16f-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a16f-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7a16f-115">Additional resources</span></span>

[<span data-ttu-id="7a16f-116">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="7a16f-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]