---
title: ฟังก์ชัน ENDSWITH ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชัน ENDSWITH การรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1155bb5446f0370d9a5c4b035a767aaeb1d46ee1
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048905"
---
# <a name="endswith-er-function"></a><span data-ttu-id="536bd-103">ฟังก์ชัน ENDSWITH ER</span><span class="sxs-lookup"><span data-stu-id="536bd-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="536bd-104">ฟังก์ชัน `ENDSWITH` นี้จะระบุว่าข้อมูลป้อนเข้าที่ระบุลงท้ายด้วยข้อความที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="536bd-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="536bd-105">จะส่งกลับค่า *Boolean* ของ **TRUE** หากอินพุตที่ระบุลงท้ายด้วยข้อความที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="536bd-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="536bd-106">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="536bd-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="536bd-107">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="536bd-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="536bd-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="536bd-108">Arguments</span></span>

<span data-ttu-id="536bd-109">`input`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="536bd-109">`input`: *String*</span></span>

<span data-ttu-id="536bd-110">พาธที่ถูกต้องของสินค้าของแหล่งข้อมูลของชนิด *สตริง* หรือค่าคงที่ของสตริง ค่าที่อาจลงท้ายด้วยอาร์กิวเมนต์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="536bd-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="536bd-111">`start text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="536bd-111">`start text`: *String*</span></span>

<span data-ttu-id="536bd-112">พาธที่ถูกต้องของสินค้าของแหล่งข้อมูลของชนิด *สตริง* หรือค่าคงที่ของสตริง ค่าที่อาจลงท้ายด้วยอาร์กิวเมนต์แรก</span><span class="sxs-lookup"><span data-stu-id="536bd-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="536bd-113">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="536bd-113">Return values</span></span>

<span data-ttu-id="536bd-114">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="536bd-114">*Boolean*</span></span>

<span data-ttu-id="536bd-115">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="536bd-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="536bd-116">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="536bd-116">Usage notes</span></span>

<span data-ttu-id="536bd-117">ฟังก์ชันนี้สามารถใช้เพื่อระบุนิพจน์เงื่อนไขของฟังก์ชัน [ตัวกรองข้อมูล](er-functions-list-filter.md) เฉพาะเมื่อตั้งค่าคอนฟิกการแม็ปที่เกี่ยวข้องใน [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) เพื่อเข้าถึง [Microsoft Dataverse](/power-platform/admin/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="536bd-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="536bd-118">มิฉะนั้น ข้อยกเว้นจะเกิดขึ้นในขณะออกแบบ</span><span class="sxs-lookup"><span data-stu-id="536bd-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="536bd-119">ข้อความที่คุณได้รับจะแนะนำให้คุณใช้ฟังก์ชัน [WHERE](er-functions-list-where.md) แทนที่จะใช้ฟังก์ชัน `FILTER`</span><span class="sxs-lookup"><span data-stu-id="536bd-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="536bd-120">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="536bd-120">Example 1</span></span>

<span data-ttu-id="536bd-121">นิพจน์ `ENDSWITH ("abc", "d")` จะส่งคืน **FALSE** ในขณะที่นิพจน์ `ENDSWITH ("abc", "C")` ส่งคืน **TRUE**</span><span class="sxs-lookup"><span data-stu-id="536bd-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="536bd-122">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="536bd-122">Example 2</span></span>

<span data-ttu-id="536bd-123">นิพจน์ `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` จะส่งคืน **TRUE** ถ้าค่าของฟิลด์ **ที่อยู่** ของแหล่งข้อมูล **แบบจำลอง** ลงท้ายด้วยสตริง **USA**</span><span class="sxs-lookup"><span data-stu-id="536bd-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="536bd-124">มิฉะนั้น จะส่งคืน **FALSE**</span><span class="sxs-lookup"><span data-stu-id="536bd-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="536bd-125">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="536bd-125">Additional resources</span></span>

[<span data-ttu-id="536bd-126">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="536bd-126">Logical functions</span></span>](er-functions-category-logical.md)
