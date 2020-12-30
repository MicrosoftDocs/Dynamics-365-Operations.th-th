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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a37b3341b05fde1283a21a0c52faec26cd1a7030
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686205"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="4fa27-103">รายการของฟังก์ชั่น ER ในประเภทตรรกะ</span><span class="sxs-lookup"><span data-stu-id="4fa27-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fa27-104">ฟังก์ชันตรรกะของการรายงานทางอิเล็กทรอนิกส์ (ER) สามารถใช้เพื่อทำงานกับค่าตรรกศาสตร์เพื่อดำเนินการเปรียบเทียบมากกว่าหนึ่งในนิพจน์เดียวหรือทดสอบหลายเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="4fa27-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="4fa27-105">หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4fa27-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="4fa27-106">รายการฟังก์ชันที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="4fa27-106">List of supported functions</span></span>

| <span data-ttu-id="4fa27-107">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="4fa27-107">Function</span></span> | <span data-ttu-id="4fa27-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4fa27-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4fa27-109">และ</span><span class="sxs-lookup"><span data-stu-id="4fa27-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="4fa27-110">ฟังก์ชันนี้ส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง</span><span class="sxs-lookup"><span data-stu-id="4fa27-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="4fa27-111">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="4fa27-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="4fa27-112">กรณี</span><span class="sxs-lookup"><span data-stu-id="4fa27-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="4fa27-113">ฟังก์ชันนี้ประเมินค่าของนิพจน์ที่ระบุกับตัวเลือกอื่นที่ระบุและส่งกลับผลลัพธ์ของตัวเลือกแรกที่เท่ากับค่าของนิพจน์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4fa27-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="4fa27-114">มิฉะนั้นจะส่งกลับผลลัพธ์เริ่มต้นที่เป็นตัวเลือกหากมีการระบุผลลัพธ์เริ่มต้นเป็นอาร์กิวเมนต์สุดท้ายของฟังก์ชันที่เรียกว่าไม่ได้นำหน้าด้วยตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="4fa27-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="4fa27-115">ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="4fa27-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="4fa27-116">ถ้า</span><span class="sxs-lookup"><span data-stu-id="4fa27-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="4fa27-117">ฟังก์ชันนี้ส่งคืนค่าที่ระบุค่าแรก หากตรงตามเงื่อนไขที่ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4fa27-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="4fa27-118">มิฉะนั้นจะส่งคืนค่าที่สองที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4fa27-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="4fa27-119">ค่าที่ถูกส่งกลับอาจเป็นค่าใดๆ ของชนิดข้อมูลที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="4fa27-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="4fa27-120">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="4fa27-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="4fa27-121">ฟังก์ชันนี้ส่งกลับค่าตรรกศาสตร์ที่ถูกย้อนกลับของเงื่อนไขที่ระบุเป็นค่า *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="4fa27-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="4fa27-122">Or</span><span class="sxs-lookup"><span data-stu-id="4fa27-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="4fa27-123">ฟังก์ชันนี้ส่งกลับค่า *บูลีน* ของ **FALSE** ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="4fa27-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="4fa27-124">ถ้าเงื่อนไขที่ระบุทั้งหมดเป็นจริง ฟังก์ชันจะส่งกลับค่า *บูลีน* ของ **TRUE**</span><span class="sxs-lookup"><span data-stu-id="4fa27-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="4fa27-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="4fa27-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="4fa27-126">ฟังก์ชันนี้กำหนดว่า การป้อนข้อมูลที่ระบุที่ตรงกับค่าใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4fa27-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="4fa27-127">จะส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าอินพุตที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4fa27-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="4fa27-128">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="4fa27-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="4fa27-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="4fa27-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="4fa27-130">ฟังก์ชันนี้กำหนดว่า การป้อนข้อมูลที่ระบุที่ตรงกับค่า *Int64* หรือ *Integer* ใดๆ ของสินค้าที่ระบุในรายการที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4fa27-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="4fa27-131">จะส่งกลับค่า *บูลีน* ของ **TRUE** ถ้าอินพุตที่ระบุตรงกับผลลัพธ์ของการเรียกใช้นิพจน์ที่ระบุสำหรับอย่างน้อยหนึ่งเรกคอร์ดของรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4fa27-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="4fa27-132">มิฉะนั้น จะส่งคืนค่า *บูลีน* เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="4fa27-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="4fa27-133">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4fa27-133">Additional resources</span></span>

[<span data-ttu-id="4fa27-134">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4fa27-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="4fa27-135">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4fa27-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="4fa27-136">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4fa27-136">Electronic reporting formula language</span></span>](er-formula-language.md)
