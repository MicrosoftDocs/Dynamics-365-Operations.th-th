---
title: ฟังก์ชั่น WHERE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) WHERE
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
ms.openlocfilehash: ca218f87eb1f9235ab475809fbbdfecf3fe0c7fb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566053"
---
# <a name="where-er-function"></a><span data-ttu-id="450cb-103">ฟังก์ชั่น WHERE ER</span><span class="sxs-lookup"><span data-stu-id="450cb-103">WHERE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="450cb-104">ฟังก์ชัน `WHERE` ส่งกลับรายการที่ระบุเป็นค่า *รายการเรกคอร์ด* หลังจากที่ถูกกรองตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="450cb-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="450cb-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="450cb-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="450cb-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="450cb-106">Arguments</span></span>

<span data-ttu-id="450cb-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="450cb-107">`list`: *Record list*</span></span>

<span data-ttu-id="450cb-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="450cb-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="450cb-109">`condition`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="450cb-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="450cb-110">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ใช้ในการกรองเรกคอร์ดของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="450cb-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="450cb-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="450cb-111">Return values</span></span>

<span data-ttu-id="450cb-112">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="450cb-112">*Record list*</span></span>

<span data-ttu-id="450cb-113">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="450cb-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="450cb-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="450cb-114">Usage notes</span></span>

<span data-ttu-id="450cb-115">ฟังก์ชันนี้แตกต่างจากฟังก์ชัน [FILTER](er-functions-list-filter.md) เนื่องจากเงื่อนไขที่ระบุจะถูกนำไปใช้กับแหล่งข้อมูล การรายงานทางอิเล็กทรอนิกส์ (ER) ใดๆ ของชนิด *รายการเรกคอร์ด* ที่แสดงในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="450cb-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="450cb-116">ถ้าอาร์กิวเมนต์ที่ถูกกำหนดค่าสำหรับฟังก์ชันนี้ (`list` และ `condition`) อนุญาตให้มีการแปลการร้องขอนี้ไปยังการเรียก SQL โดยตรงข้อความเตือนจะถูกโยนในเวลาออกแบบ</span><span class="sxs-lookup"><span data-stu-id="450cb-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="450cb-117">ข้อความนี้จะแจ้งให้ผู้ใช้ที่มีประสิทธิภาพการทำงานอาจถูกปรับปรุงถ้าฟังก์ชัน [FILTER](er-functions-list-filter.md) ถูกใช้แทน `WHERE`</span><span class="sxs-lookup"><span data-stu-id="450cb-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="450cb-118">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="450cb-118">Example 1</span></span>

<span data-ttu-id="450cb-119">ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่อ้างอิงถึงตาราง VendTable นิพจน์ `WHERE (Vendors, Vendors.VendGroup = "40")` จะส่งกลับรายการของเพียงแค่ผู้จัดจำหน่ายที่เป็นของกลุ่มผู้จัดจำหน่าย 40</span><span class="sxs-lookup"><span data-stu-id="450cb-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="450cb-120">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="450cb-120">Example 2</span></span>

<span data-ttu-id="450cb-121">ถ้าคุณป้อนแหล่งข้อมูล **DS** ของชนิดของ *ฟิลด์ที่มีการคำนวณ* และมีนิพจน์ `SPLIT ("A|B|C", "|")` นิพจน์ `WHERE( DS, DS.Value = "B")` จะส่งคืนรายการเรกคอร์ดที่มีค่าข้อความ **"B"** ในฟิลด์ **ค่า**</span><span class="sxs-lookup"><span data-stu-id="450cb-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="450cb-122">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="450cb-122">Additional resources</span></span>

[<span data-ttu-id="450cb-123">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="450cb-123">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]