---
title: รายการของฟังก์ชั่น ER ในประเภทตรรกะ
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันตรรกะที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705106"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="fe134-103">รายการของฟังก์ชั่น ER ในประเภทตรรกะ</span><span class="sxs-lookup"><span data-stu-id="fe134-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe134-104">ฟังก์ชันตรรกะของการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อทำงานกับค่าตรรกศาสตร์เพื่อดำเนินการเปรียบเทียบมากกว่าหนึ่งในนิพจน์เดียวหรือทดสอบหลายเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="fe134-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="fe134-105">หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="fe134-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="fe134-106">รายการฟังก์ชันที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="fe134-106">List of supported functions</span></span>

| <span data-ttu-id="fe134-107">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="fe134-107">Function</span></span> | <span data-ttu-id="fe134-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="fe134-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="fe134-109">และ</span><span class="sxs-lookup"><span data-stu-id="fe134-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="fe134-110">ฟังก์ชันนี้ส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง</span><span class="sxs-lookup"><span data-stu-id="fe134-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="fe134-111">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="fe134-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="fe134-112">กรณี</span><span class="sxs-lookup"><span data-stu-id="fe134-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="fe134-113">ฟังก์ชันนี้ประเมินค่าของนิพจน์ที่ระบุกับตัวเลือกอื่นที่ระบุและส่งกลับผลลัพธ์ของตัวเลือกแรกที่เท่ากับค่าของนิพจน์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fe134-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="fe134-114">มิฉะนั้นจะส่งกลับผลลัพธ์เริ่มต้นที่เป็นตัวเลือกหากมีการระบุผลลัพธ์เริ่มต้นเป็นอาร์กิวเมนต์สุดท้ายของฟังก์ชันที่เรียกว่าไม่ได้นำหน้าด้วยตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="fe134-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="fe134-115">ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="fe134-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="fe134-116">ถ้า</span><span class="sxs-lookup"><span data-stu-id="fe134-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="fe134-117">ฟังก์ชันนี้ส่งคืนค่าที่ระบุค่าแรก หากตรงตามเงื่อนไขที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fe134-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="fe134-118">มิฉะนั้นจะส่งคืนค่าที่สองที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fe134-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="fe134-119">ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="fe134-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="fe134-120">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="fe134-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="fe134-121">ฟังก์ชันนี้ส่งกลับค่าตรรกศาสตร์ที่ถูกย้อนกลับของเงื่อนไขที่ระบุเป็นค่า *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="fe134-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="fe134-122">Or</span><span class="sxs-lookup"><span data-stu-id="fe134-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="fe134-123">ฟังก์ชันนี้ส่งกลับค่า *บูลีน* ของ **FALSE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="fe134-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="fe134-124">ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง ฟังก์ชันจะส่งกลับค่า *บูลีน* ของ **TRUE**</span><span class="sxs-lookup"><span data-stu-id="fe134-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="fe134-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="fe134-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="fe134-126">ฟังก์ชันนี้กำหนดว่า การป้อนข้อมูลที่ระบุที่ตรงกับค่าใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fe134-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="fe134-127">จะส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าอินพุตที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fe134-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="fe134-128">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="fe134-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="fe134-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="fe134-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="fe134-130">ฟังก์ชันนี้กำหนดว่า การป้อนข้อมูลที่ระบุที่ตรงกับค่า *Int64* หรือ *Integer* ใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fe134-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="fe134-131">จะส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าอินพุตที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fe134-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="fe134-132">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="fe134-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="fe134-133">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fe134-133">Additional resources</span></span>

[<span data-ttu-id="fe134-134">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="fe134-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="fe134-135">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="fe134-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="fe134-136">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="fe134-136">Electronic reporting formula language</span></span>](er-formula-language.md)
