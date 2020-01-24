---
title: ฟังก์ชัน ER EMPTYLIST
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) EMPTYLIST
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
ms.openlocfilehash: a60bc948ff6223b6e3acccd0ba40bf64f238aac2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917407"
---
# <span data-ttu-id="5ed51-103"><a name="EMPTYLIST">ฟังก์ชัน ER EMPTYLIST</a></span><span class="sxs-lookup"><span data-stu-id="5ed51-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ed51-104">ฟังก์ชัน `EMPTYLIST` ส่งคืนค่า *รายการเรกคอร์ด* ที่ว่างเปล่าโดยใช้รายการที่ระบุเป็นแหล่งข้อมูลสำหรับโครงสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="5ed51-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed51-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="5ed51-105">Syntax</span></span>

```
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="5ed51-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="5ed51-106">Arguments</span></span>

<span data-ttu-id="5ed51-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="5ed51-107">`list`: *Record list*</span></span>

<span data-ttu-id="5ed51-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="5ed51-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5ed51-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="5ed51-109">Return values</span></span>

<span data-ttu-id="5ed51-110">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="5ed51-110">*Record list*</span></span>

<span data-ttu-id="5ed51-111">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="5ed51-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="5ed51-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="5ed51-112">Example</span></span>

<span data-ttu-id="5ed51-113">`EMPTYLIST (SPLIT ("abc", 1))` ส่งคืนรายการที่ว่างเปล่าใหม่ที่มีโครงสร้างเดียวกันกับรายการที่ถูกส่งคืนโดยฟังก์ชัน `SPLIT` ที่ใช้</span><span class="sxs-lookup"><span data-stu-id="5ed51-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ed51-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5ed51-114">Additional resources</span></span>

[<span data-ttu-id="5ed51-115">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="5ed51-115">List functions</span></span>](er-functions-category-list.md)
