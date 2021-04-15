---
title: ฟังก์ชัน ER LISTOFFIRSTITEM
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) LISTOFFIRSTITEM
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
ms.openlocfilehash: 6dd6c84b43bea36bf922ae9348f95b450e882832
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750191"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="23f8d-103">ฟังก์ชัน ER LISTOFFIRSTITEM</span><span class="sxs-lookup"><span data-stu-id="23f8d-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23f8d-104">ฟังก์ชัน `LISTOFFIRSTITEM` ส่งกลับค่า *รายการเรกคอร์ด* ที่ประกอบด้วยเฉพาะเรกคอร์ดแรกของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="23f8d-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f8d-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="23f8d-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="23f8d-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="23f8d-106">Arguments</span></span>

<span data-ttu-id="23f8d-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="23f8d-107">`list`: *Record list*</span></span>

<span data-ttu-id="23f8d-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="23f8d-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="23f8d-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="23f8d-109">Return values</span></span>

<span data-ttu-id="23f8d-110">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="23f8d-110">*Record list*</span></span>

<span data-ttu-id="23f8d-111">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="23f8d-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="23f8d-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="23f8d-112">Example</span></span>

<span data-ttu-id="23f8d-113">นิพจน์ `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` ส่งกลับค่าข้อความ **"A"**</span><span class="sxs-lookup"><span data-stu-id="23f8d-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23f8d-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="23f8d-114">Additional resources</span></span>

[<span data-ttu-id="23f8d-115">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="23f8d-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]