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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6134ae7eb1a8044cf906f2a8d02eb153522a6cf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041940"
---
# <span data-ttu-id="34349-103"><a name="REVERSE">ฟังก์ชัน REVERSE ER</a></span><span class="sxs-lookup"><span data-stu-id="34349-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34349-104">ฟังก์ชัน `REVERSE` ส่งกลับรายการที่ระบุเป็นค่า *รายการเรกคอร์ด* ในลำดับการจัดเรียงแบบย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="34349-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="34349-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="34349-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="34349-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="34349-106">Arguments</span></span>

<span data-ttu-id="34349-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="34349-107">`list`: *Record list*</span></span>

<span data-ttu-id="34349-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="34349-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="34349-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="34349-109">Return values</span></span>

<span data-ttu-id="34349-110">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="34349-110">*Record list*</span></span>

<span data-ttu-id="34349-111">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="34349-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="34349-112">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="34349-112">Example 1</span></span>

<span data-ttu-id="34349-113">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่คำนวณได้* และประกอบด้วยนิพจน์ `SPLIT ("C|B|A", "|")` นิพจน์ `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` จะส่งกลับค่าข้อความ **C**</span><span class="sxs-lookup"><span data-stu-id="34349-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="34349-114">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="34349-114">Example 2</span></span>

<span data-ttu-id="34349-115">ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ที่อ้างอิงถึงตาราง VendTable นิพจน์ `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` จะส่งกลับรายการของผู้จัดจำหน่ายที่เรียงลำดับตามชื่อในลำดับจากมากไปน้อย</span><span class="sxs-lookup"><span data-stu-id="34349-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34349-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="34349-116">Additional resources</span></span>

[<span data-ttu-id="34349-117">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="34349-117">List functions</span></span>](er-functions-category-list.md)
