---
title: ฟังก์ชัน REVERSE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) REVERSE
author: NickSelin
manager: kfend
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
ms.openlocfilehash: f76582bc8b752fe0322bee8917d8649ed1c024ba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567377"
---
# <a name="reverse-er-function"></a><span data-ttu-id="87cef-103">ฟังก์ชัน REVERSE ER</span><span class="sxs-lookup"><span data-stu-id="87cef-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87cef-104">ฟังก์ชัน `REVERSE` ส่งกลับรายการที่ระบุเป็นค่า *รายการเรกคอร์ด* ในลำดับการจัดเรียงแบบย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="87cef-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="87cef-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="87cef-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="87cef-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="87cef-106">Arguments</span></span>

<span data-ttu-id="87cef-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="87cef-107">`list`: *Record list*</span></span>

<span data-ttu-id="87cef-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="87cef-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="87cef-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="87cef-109">Return values</span></span>

<span data-ttu-id="87cef-110">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="87cef-110">*Record list*</span></span>

<span data-ttu-id="87cef-111">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="87cef-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="87cef-112">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="87cef-112">Example 1</span></span>

<span data-ttu-id="87cef-113">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่มีการคำนวณ* และประกอบด้วยนิพจน์ `SPLIT ("C|B|A", "|")` นิพจน์ `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` จะส่งกลับค่าข้อความ **C**</span><span class="sxs-lookup"><span data-stu-id="87cef-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="87cef-114">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="87cef-114">Example 2</span></span>

<span data-ttu-id="87cef-115">ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ที่อ้างอิงถึงตาราง VendTable นิพจน์ `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` จะส่งกลับรายการของผู้จัดจำหน่ายที่เรียงลำดับตามชื่อในลำดับจากมากไปน้อย</span><span class="sxs-lookup"><span data-stu-id="87cef-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87cef-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="87cef-116">Additional resources</span></span>

[<span data-ttu-id="87cef-117">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="87cef-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]