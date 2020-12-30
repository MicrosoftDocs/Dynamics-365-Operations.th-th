---
title: ฟังก์ชัน ER LISTOFFIRSTITEM
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) LISTOFFIRSTITEM
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
ms.openlocfilehash: 8ea81bce8cd6b922f3ef1d53ec0c4b2574780377
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686499"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="56f38-103">ฟังก์ชัน ER LISTOFFIRSTITEM</span><span class="sxs-lookup"><span data-stu-id="56f38-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56f38-104">ฟังก์ชัน `LISTOFFIRSTITEM` ส่งกลับค่า *รายการเรกคอร์ด* ที่ประกอบด้วยเฉพาะเรกคอร์ดแรกของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="56f38-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f38-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="56f38-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="56f38-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="56f38-106">Arguments</span></span>

<span data-ttu-id="56f38-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="56f38-107">`list`: *Record list*</span></span>

<span data-ttu-id="56f38-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="56f38-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="56f38-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="56f38-109">Return values</span></span>

<span data-ttu-id="56f38-110">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="56f38-110">*Record list*</span></span>

<span data-ttu-id="56f38-111">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="56f38-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="56f38-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="56f38-112">Example</span></span>

<span data-ttu-id="56f38-113">นิพจน์ `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` ส่งกลับค่าข้อความ **"A"**</span><span class="sxs-lookup"><span data-stu-id="56f38-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56f38-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="56f38-114">Additional resources</span></span>

[<span data-ttu-id="56f38-115">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="56f38-115">List functions</span></span>](er-functions-category-list.md)
