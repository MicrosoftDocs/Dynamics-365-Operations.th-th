---
title: ฟังก์ชัน REVERSE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) REVERSE
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
ms.openlocfilehash: 895d5f13f065b2188f245d081fa69e7e63555dde
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686451"
---
# <a name="reverse-er-function"></a><span data-ttu-id="06f07-103">ฟังก์ชัน REVERSE ER</span><span class="sxs-lookup"><span data-stu-id="06f07-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06f07-104">ฟังก์ชัน `REVERSE` ส่งกลับรายการที่ระบุเป็นค่า *รายการเรกคอร์ด* ในลำดับการจัดเรียงแบบย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="06f07-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="06f07-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="06f07-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="06f07-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="06f07-106">Arguments</span></span>

<span data-ttu-id="06f07-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="06f07-107">`list`: *Record list*</span></span>

<span data-ttu-id="06f07-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="06f07-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="06f07-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="06f07-109">Return values</span></span>

<span data-ttu-id="06f07-110">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="06f07-110">*Record list*</span></span>

<span data-ttu-id="06f07-111">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="06f07-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="06f07-112">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="06f07-112">Example 1</span></span>

<span data-ttu-id="06f07-113">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่มีการคำนวณ* และประกอบด้วยนิพจน์ `SPLIT ("C|B|A", "|")` นิพจน์ `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` จะส่งกลับค่าข้อความ **C**</span><span class="sxs-lookup"><span data-stu-id="06f07-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="06f07-114">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="06f07-114">Example 2</span></span>

<span data-ttu-id="06f07-115">ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ที่อ้างอิงถึงตาราง VendTable นิพจน์ `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` จะส่งกลับรายการของผู้จัดจำหน่ายที่เรียงลำดับตามชื่อในลำดับจากมากไปน้อย</span><span class="sxs-lookup"><span data-stu-id="06f07-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06f07-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="06f07-116">Additional resources</span></span>

[<span data-ttu-id="06f07-117">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="06f07-117">List functions</span></span>](er-functions-category-list.md)
