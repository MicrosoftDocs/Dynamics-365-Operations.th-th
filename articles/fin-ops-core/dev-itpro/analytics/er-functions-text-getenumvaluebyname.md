---
title: ฟังก์ชัน GETENUMVALUEBYNAME ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ GETENUMVALUEBYNAME (ER)
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743866"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="69515-103">ฟังก์ชัน GETENUMVALUEBYNAME ER</span><span class="sxs-lookup"><span data-stu-id="69515-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69515-104">ฟังก์ชัน `GETENUMVALUEBYNAME` ค้นหาค่า *Enum* เฉพาะในแหล่งข้อมูลการแจงนับที่ระบุ โดยใช้ชื่อการแจงนับที่ระบุเป็นค่า *สตริง*</span><span class="sxs-lookup"><span data-stu-id="69515-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="69515-105">ถ้าพบค่า *Enum* ฟังก์ชันจะส่งคืน</span><span class="sxs-lookup"><span data-stu-id="69515-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="69515-106">มิฉะนั้น ฟังก์ชันจะส่งกลับค่าการแจงนับ **null**</span><span class="sxs-lookup"><span data-stu-id="69515-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="69515-107">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="69515-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="69515-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="69515-108">Arguments</span></span>

<span data-ttu-id="69515-109">`enumeration data source path`: *การแจงนับ*</span><span class="sxs-lookup"><span data-stu-id="69515-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="69515-110">พาธที่ถูกต้องของแหล่งข้อมูลของหนึ่งในชนิดการแจงนับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="69515-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="69515-111">การแจงนับแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="69515-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="69515-112">การแจงนับรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="69515-112">ER format enumeration</span></span>
- <span data-ttu-id="69515-113">การแจงนับ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="69515-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="69515-114">`enumeration value text`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="69515-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="69515-115">ค่าสตริงที่แสดงชื่อของค่าการแจงนับเดียว</span><span class="sxs-lookup"><span data-stu-id="69515-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="69515-116">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="69515-116">Return values</span></span>

<span data-ttu-id="69515-117">*Enum* ที่สามารถเว้นว่างได้</span><span class="sxs-lookup"><span data-stu-id="69515-117">Nullable *Enum*</span></span>

<span data-ttu-id="69515-118">ค่าการแจงนับที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="69515-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="69515-119">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="69515-119">Usage notes</span></span>

<span data-ttu-id="69515-120">ไม่มีข้อยกเว้น หากไม่พบค่า *Enum* โดยใช้ชื่อของค่าการแจงนับที่ระบุเป็นค่า *สตริง*</span><span class="sxs-lookup"><span data-stu-id="69515-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="69515-121">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="69515-121">Example</span></span>

<span data-ttu-id="69515-122">ในแผนภาพต่อไปนี้ การแจงนับ **ReportDirection** ถูกนำมาใช้ในรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="69515-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="69515-123">โปรดทราบว่า ป้ายชื่อถูกกำหนดไว้สำหรับค่าแจงนับ</span><span class="sxs-lookup"><span data-stu-id="69515-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="69515-124">ภาพประกอบต่อไปนี้แสดงรายละเอียดเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="69515-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="69515-125">แหล่งข้อมูล **$ทิศทาง** ถูกตั้งค่าคอนฟิกในรายงาน ER</span><span class="sxs-lookup"><span data-stu-id="69515-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="69515-126">แหล่งข้อมูลนี้ถูกตั้งค่าคอนฟิกตามการแจงนับแบบจำลอง **ReportDirection**</span><span class="sxs-lookup"><span data-stu-id="69515-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="69515-127">นิพจน์ `$IsArrivals` ถูกออกแบบมาเพื่อใช้การแจงนับแบบจำลอง–ที่ขึ้นกับ **$ทิศทาง** เป็นพารามิเตอร์ของฟังก์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="69515-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="69515-128">ค่าของนิพจน์การเปรียบเทียบนี้คือ **จริง**</span><span class="sxs-lookup"><span data-stu-id="69515-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="69515-129">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="69515-129">Additional resources</span></span>

[<span data-ttu-id="69515-130">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="69515-130">Text functions</span></span>](er-functions-category-text.md)
