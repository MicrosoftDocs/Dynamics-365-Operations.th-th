---
title: รายการของฟังก์ชั่น ER ในประเภทคณิตศาสตร์
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันคณิตศาสตร์ที่รองรับในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 8288c2cbf16ae0d73a065e323b5e8214252889a1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686158"
---
# <a name="list-of-er-functions-in-the-mathematical-category"></a><span data-ttu-id="2d20c-103">รายการของฟังก์ชั่น ER ในประเภทคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="2d20c-103">List of ER functions in the mathematical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d20c-104">ฟังก์ชันทางคณิตศาสตร์ของการรายงานอิเล็กทรอนิกส์ (ER) สามารถใช้ในการคำนวณคณิตศาสตร์ทั่วไปมากมาย</span><span class="sxs-lookup"><span data-stu-id="2d20c-104">Electronic reporting (ER) mathematical functions can be used to do many common mathematical calculations.</span></span> <span data-ttu-id="2d20c-105">หัวข้อนี้แสดงสรุปของฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2d20c-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="2d20c-106">รายการฟังก์ชันที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="2d20c-106">List of supported functions</span></span>

| <span data-ttu-id="2d20c-107">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="2d20c-107">Function</span></span> | <span data-ttu-id="2d20c-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2d20c-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="2d20c-109">Abs</span><span class="sxs-lookup"><span data-stu-id="2d20c-109">Abs</span></span>](er-functions-mathematical-abs.md)             | <span data-ttu-id="2d20c-110">ฟังก์ชันนี้ส่งกลับค่าเงินเต็ม (โมดูล) ของจำนวนที่ระบุเป็นค่า *จริง*</span><span class="sxs-lookup"><span data-stu-id="2d20c-110">This function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="2d20c-111">กล่าวคือ ส่งคืนหมายเลขโดยไม่มีเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="2d20c-111">In other words, it returns the number without its sign.</span></span> |
| [<span data-ttu-id="2d20c-112">กำลัง</span><span class="sxs-lookup"><span data-stu-id="2d20c-112">Power</span></span>](er-functions-mathematical-power.md)         | <span data-ttu-id="2d20c-113">ฟังก์ชันนี้ส่งกลับค่า *จริง* ที่แสดงถึงผลของการเพิ่มจำนวนบวกที่ระบุให้กับพลังงานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="2d20c-113">This function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span> |
| [<span data-ttu-id="2d20c-114">Round</span><span class="sxs-lookup"><span data-stu-id="2d20c-114">Round</span></span>](er-functions-mathematical-round.md)         | <span data-ttu-id="2d20c-115">ฟังก์ชันนี้ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษเป็นจำนวนทศนิยมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="2d20c-115">This function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span> |
| [<span data-ttu-id="2d20c-116">RoundDown</span><span class="sxs-lookup"><span data-stu-id="2d20c-116">RoundDown</span></span>](er-functions-mathematical-rounddown.md) | <span data-ttu-id="2d20c-117">ฟังก์ชันนี้ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษลงเป็นจำนวนทศนิยมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="2d20c-117">This function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span> |
| [<span data-ttu-id="2d20c-118">RoundUp</span><span class="sxs-lookup"><span data-stu-id="2d20c-118">RoundUp</span></span>](er-functions-mathematical-roundup.md)     | <span data-ttu-id="2d20c-119">ฟังก์ชันนี้ส่งคืนหมายเลขที่ระบุเป็นค่า *จริง* หลังจากที่ได้ถูกปัดเศษขึ้นเป็นจำนวนทศนิยมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="2d20c-119">This function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2d20c-120">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2d20c-120">Additional resources</span></span>

[<span data-ttu-id="2d20c-121">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="2d20c-121">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="2d20c-122">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="2d20c-122">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="2d20c-123">ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="2d20c-123">Electronic reporting formula language</span></span>](er-formula-language.md)
