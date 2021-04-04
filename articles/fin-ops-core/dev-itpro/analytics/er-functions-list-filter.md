---
title: ฟังก์ชัน FILTER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) FILTER
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
ms.openlocfilehash: 0e90db1836a93dab42be5dc91e9ea478163a1437
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559710"
---
# <a name="filter-er-function"></a><span data-ttu-id="1f001-103">ฟังก์ชัน FILTER ER</span><span class="sxs-lookup"><span data-stu-id="1f001-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f001-104">ฟังก์ชัน `FILTER` ส่งกลับรายการที่ระบุเป็นค่า *รายการเรกคอร์ด* หลังจากที่การสอบถามถูกเปลี่ยนเพื่อให้กรองตามเงื่อนไขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1f001-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f001-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="1f001-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="1f001-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="1f001-106">Arguments</span></span>

<span data-ttu-id="1f001-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="1f001-107">`list`: *Record list*</span></span>

<span data-ttu-id="1f001-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="1f001-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="1f001-109">`condition`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="1f001-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="1f001-110">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ใช้ในการกรองเรกคอร์ดของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1f001-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="1f001-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="1f001-111">Return values</span></span>

<span data-ttu-id="1f001-112">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="1f001-112">*Record list*</span></span>

<span data-ttu-id="1f001-113">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="1f001-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1f001-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1f001-114">Usage notes</span></span>

<span data-ttu-id="1f001-115">ฟังก์ชันนี้แตกต่างจากฟังก์ชัน [WHERE](er-functions-list-where.md) เนื่องจากเงื่อนไขที่ระบุจะถูกนำไปใช้กับการรายงานทางอิเล็กทรอนิกส์ (ER) ใดๆ แหล่งข้อมูลของชนิด *เรกคอร์ดตาราง* ที่ระดับฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1f001-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="1f001-116">สามารถกำหนดรายการและเงื่อนไขได้โดยใช้ตารางและความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="1f001-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="1f001-117">ถ้าอาร์กิวเมนต์หนึ่งหรือทั้งคู่ที่ถูกกำหนดค่าสำหรับฟังก์ชันนี้ (`list` และ `condition`) อนุญาตให้มีการแปลการร้องขอนี้ไปยังการเรียก SQL โดยตรง จะมีข้อยกเว้นเกิดขึ้นในเวลาออกแบบ</span><span class="sxs-lookup"><span data-stu-id="1f001-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="1f001-118">ข้อยกเว้นนี้จะแจ้งให้ผู้ใช้ทั้ง `list` หรือ `condition` ทราบว่าหรือไม่สามารถใช้เพื่อสอบถามฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1f001-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="1f001-119">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="1f001-119">Example 1</span></span>

<span data-ttu-id="1f001-120">ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่อ้างอิงถึงตาราง VendTable นิพจน์ `FILTER (Vendors, Vendors.VendGroup = "40")` จะส่งกลับรายการของเพียงแค่ผู้จัดจำหน่ายที่เป็นของกลุ่มผู้จัดจำหน่าย 40</span><span class="sxs-lookup"><span data-stu-id="1f001-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="1f001-121">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="1f001-121">Example 2</span></span>

<span data-ttu-id="1f001-122">ถ้า **ผู้จัดจำหน่าย** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่อ้างอิงถึงตาราง VendTable และถ้า **parmVendorBankGroup** ถูกตั้งค่าคอนฟิกเป็นแหล่งข้อมูล ER ที่ส่งกลับค่าเป็นชนิดข้อมูล *สตริง* นิพจน์ `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` จะส่งกลับรายการของบัญชีผู้จัดจำหน่ายที่เป็นของกลุ่มธนาคารหนึ่งๆ เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1f001-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="1f001-123">ตัวอย่างที่ 3</span><span class="sxs-lookup"><span data-stu-id="1f001-123">Example 3</span></span>

<span data-ttu-id="1f001-124">คุณป้อนแหล่งข้อมูล **DS** ของชนิด *ฟิลด์ที่มีการคำนวณ* และประกอบด้วยนิพจน์ `SPLIT ("A,B,C", ",")`</span><span class="sxs-lookup"><span data-stu-id="1f001-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="1f001-125">จากนั้นคุณป้อนนิพจน์อื่น `FILTER( DS, DS.Value = "B")`</span><span class="sxs-lookup"><span data-stu-id="1f001-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="1f001-126">เมื่อคุณพยายามที่จะบันทึกนิพจน์นี้ในโปรแกรมออกแบบสูตร ER ข้อยกเว้นต่อไปนี้จะเกิดขึ้น: "ข้อผิดพลาดการตรวจสอบ: นิพจน์รายการของฟังก์ชันตัวกรองไม่สามารถเป็นแบบสอบถามได้"</span><span class="sxs-lookup"><span data-stu-id="1f001-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f001-127">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1f001-127">Additional resources</span></span>

[<span data-ttu-id="1f001-128">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="1f001-128">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]