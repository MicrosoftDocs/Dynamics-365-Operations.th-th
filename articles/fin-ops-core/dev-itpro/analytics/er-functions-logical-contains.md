---
title: ฟังก์ชัน CONTAINS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชัน CONTAINS การรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 81964681688cebf870bc9b6c59aff0b7fdd82449
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557557"
---
# <a name="contains-er-function"></a><span data-ttu-id="5346f-103">ฟังก์ชัน CONTAINS ER</span><span class="sxs-lookup"><span data-stu-id="5346f-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5346f-104">ฟังก์ชัน `CONTAINS` นี้จะระบุว่าข้อมูลป้อนเข้าที่ระบุมีข้อความที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5346f-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="5346f-105">จะส่งกลับค่า *Boolean* ของ **TRUE** หากอินพุตที่ระบุมีข้อความที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5346f-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="5346f-106">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="5346f-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5346f-107">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="5346f-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="5346f-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="5346f-108">Arguments</span></span>

<span data-ttu-id="5346f-109">`input`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="5346f-109">`input`: *String*</span></span>

<span data-ttu-id="5346f-110">พาธที่ถูกต้องของสินค้าของแหล่งข้อมูลของชนิด *สตริง* หรือค่าคงที่ของสตริง ค่าที่อาจมีอาร์กิวเมนต์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="5346f-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="5346f-111">`search text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="5346f-111">`search text`: *String*</span></span>

<span data-ttu-id="5346f-112">พาธที่ถูกต้องของสินค้าของแหล่งข้อมูลของชนิด *สตริง* หรือค่าคงที่ของสตริง ค่าที่อาจมีอาร์กิวเมนต์แรก</span><span class="sxs-lookup"><span data-stu-id="5346f-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="5346f-113">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="5346f-113">Return values</span></span>

<span data-ttu-id="5346f-114">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="5346f-114">*Boolean*</span></span>

<span data-ttu-id="5346f-115">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="5346f-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5346f-116">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="5346f-116">Usage notes</span></span>

<span data-ttu-id="5346f-117">ฟังก์ชันนี้สามารถใช้เพื่อระบุนิพจน์เงื่อนไขของฟังก์ชัน [ตัวกรองข้อมูล](er-functions-list-filter.md) เฉพาะเมื่อตั้งค่าคอนฟิกการแม็ปที่เกี่ยวข้องใน [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) เพื่อเข้าถึง [Microsoft Dataverse](../data-entities/data-integration-cds.md)</span><span class="sxs-lookup"><span data-stu-id="5346f-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="5346f-118">มิฉะนั้น ข้อยกเว้นจะเกิดขึ้นในขณะออกแบบ</span><span class="sxs-lookup"><span data-stu-id="5346f-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="5346f-119">ข้อความที่คุณได้รับจะแนะนำให้คุณใช้ฟังก์ชัน [WHERE](er-functions-list-where.md) แทนที่จะใช้ฟังก์ชัน `FILTER`</span><span class="sxs-lookup"><span data-stu-id="5346f-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="5346f-120">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="5346f-120">Example 1</span></span>

<span data-ttu-id="5346f-121">นิพจน์ `CONTAINS ("abc", "d")` จะส่งคืน **FALSE** ในขณะที่นิพจน์ `CONTAINS ("abc", "C")` ส่งคืน **TRUE**</span><span class="sxs-lookup"><span data-stu-id="5346f-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="5346f-122">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="5346f-122">Example 2</span></span>

<span data-ttu-id="5346f-123">นิพจน์ `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` จะส่งคืน **TRUE** ถ้าค่าของฟิลด์ **ที่อยู่** ของแหล่งข้อมูล **แบบจำลอง** มีสตริง **DEU**</span><span class="sxs-lookup"><span data-stu-id="5346f-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="5346f-124">มิฉะนั้น จะส่งคืน **FALSE**</span><span class="sxs-lookup"><span data-stu-id="5346f-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5346f-125">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5346f-125">Additional resources</span></span>

[<span data-ttu-id="5346f-126">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="5346f-126">Logical functions</span></span>](er-functions-category-logical.md)
