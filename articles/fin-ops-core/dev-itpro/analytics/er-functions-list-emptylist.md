---
title: ฟังก์ชัน ER EMPTYLIST
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) EMPTYLIST
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746686"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="1f96c-103">ฟังก์ชัน ER EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="1f96c-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f96c-104">ฟังก์ชัน `EMPTYLIST` ส่งคืนค่า *รายการเรกคอร์ด* ที่ว่างเปล่าโดยใช้รายการที่ระบุเป็นแหล่งข้อมูลสำหรับโครงสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="1f96c-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f96c-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="1f96c-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="1f96c-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="1f96c-106">Arguments</span></span>

<span data-ttu-id="1f96c-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="1f96c-107">`list`: *Record list*</span></span>

<span data-ttu-id="1f96c-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="1f96c-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1f96c-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="1f96c-109">Return values</span></span>

<span data-ttu-id="1f96c-110">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="1f96c-110">*Record list*</span></span>

<span data-ttu-id="1f96c-111">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="1f96c-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="1f96c-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="1f96c-112">Example</span></span>

<span data-ttu-id="1f96c-113">`EMPTYLIST (SPLIT ("abc", 1))` ส่งคืนรายการที่ว่างเปล่าใหม่ที่มีโครงสร้างเดียวกันกับรายการที่ถูกส่งคืนโดยฟังก์ชัน `SPLIT` ที่ใช้</span><span class="sxs-lookup"><span data-stu-id="1f96c-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f96c-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1f96c-114">Additional resources</span></span>

[<span data-ttu-id="1f96c-115">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="1f96c-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]