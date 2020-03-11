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
ms.openlocfilehash: 86c8a0ae21ffeb6268efbbd198f7c709c2ad54f6
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042124"
---
# <span data-ttu-id="2c022-103"><a name="FIRSTORNULL">ฟังก์ชัน FIRSTORNULL ER</a></span><span class="sxs-lookup"><span data-stu-id="2c022-103"><a name="FIRSTORNULL">FIRSTORNULL ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c022-104">ฟังก์ชัน `FIRSTORNULL` ส่งกลับเรกคอร์ดแรกของรายการที่ระบุเป็นค่า *คอนเทนเนอร์ (เรกคอร์ด)* หากเรกคอร์ดไม่ว่าง</span><span class="sxs-lookup"><span data-stu-id="2c022-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="2c022-105">ถ้าเรกคอร์ดว่าง ฟังก์ชันนี้จะส่งกลับค่า*คอนเทนเนอร์ (เรกคอร์ด)* ที่เป็น null</span><span class="sxs-lookup"><span data-stu-id="2c022-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c022-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="2c022-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="2c022-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="2c022-107">Arguments</span></span>

<span data-ttu-id="2c022-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="2c022-108">`list`: *Record list*</span></span>

<span data-ttu-id="2c022-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="2c022-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c022-110">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="2c022-110">Return values</span></span>

<span data-ttu-id="2c022-111">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="2c022-111">*Container (record)*</span></span>

<span data-ttu-id="2c022-112">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="2c022-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="2c022-113">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2c022-113">Example</span></span>

<span data-ttu-id="2c022-114">นิพจน์ `FIRSTORNULL(SPLIT("",1)).Value` ส่งกลับสตริงที่ว่างเปล่า (**""**)</span><span class="sxs-lookup"><span data-stu-id="2c022-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c022-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2c022-115">Additional resources</span></span>

[<span data-ttu-id="2c022-116">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="2c022-116">List functions</span></span>](er-functions-category-list.md)
