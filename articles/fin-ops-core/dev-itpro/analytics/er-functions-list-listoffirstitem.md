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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041986"
---
# <span data-ttu-id="72f7e-103"><a name="LISTOFFIRSTITEM">ฟังก์ชัน ER LISTOFFIRSTITEM</a></span><span class="sxs-lookup"><span data-stu-id="72f7e-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72f7e-104">ฟังก์ชัน `LISTOFFIRSTITEM` ส่งกลับค่า *รายการเรกคอร์ด* ที่ประกอบด้วยเฉพาะเรกคอร์ดแรกของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="72f7e-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f7e-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="72f7e-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="72f7e-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="72f7e-106">Arguments</span></span>

<span data-ttu-id="72f7e-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="72f7e-107">`list`: *Record list*</span></span>

<span data-ttu-id="72f7e-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="72f7e-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="72f7e-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="72f7e-109">Return values</span></span>

<span data-ttu-id="72f7e-110">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="72f7e-110">*Record list*</span></span>

<span data-ttu-id="72f7e-111">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="72f7e-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="72f7e-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="72f7e-112">Example</span></span>

<span data-ttu-id="72f7e-113">นิพจน์ `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` ส่งกลับค่าข้อความ **"A"**</span><span class="sxs-lookup"><span data-stu-id="72f7e-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72f7e-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="72f7e-114">Additional resources</span></span>

[<span data-ttu-id="72f7e-115">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="72f7e-115">List functions</span></span>](er-functions-category-list.md)
