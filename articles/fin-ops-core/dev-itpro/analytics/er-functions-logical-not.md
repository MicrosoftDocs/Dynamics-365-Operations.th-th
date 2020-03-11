---
title: ฟังก์ชัน NOT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) NOT
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041733"
---
# <span data-ttu-id="6cdff-103"><a name="NOT">ฟังก์ชัน NOT ER</a></span><span class="sxs-lookup"><span data-stu-id="6cdff-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cdff-104">ฟังก์ชัน `NOT` ส่งกลับค่าตรรกศาสตร์ที่ถูกย้อนกลับของเงื่อนไขที่ระบุเป็นค่า *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="6cdff-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cdff-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="6cdff-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="6cdff-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="6cdff-106">Arguments</span></span>

<span data-ttu-id="6cdff-107">`condition`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="6cdff-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="6cdff-108">นิพจน์แบบมีเงื่อนไขที่ถูกต้องที่ต้องย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="6cdff-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="6cdff-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="6cdff-109">Return values</span></span>

<span data-ttu-id="6cdff-110">*บูลีน*</span><span class="sxs-lookup"><span data-stu-id="6cdff-110">*Boolean*</span></span>

<span data-ttu-id="6cdff-111">ค่า *บูลีน* ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="6cdff-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="6cdff-112">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6cdff-112">Example</span></span>

<span data-ttu-id="6cdff-113">`NOT (TRUE)` ส่งกลับค่า **FALSE**</span><span class="sxs-lookup"><span data-stu-id="6cdff-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6cdff-114">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6cdff-114">Additional resources</span></span>

[<span data-ttu-id="6cdff-115">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="6cdff-115">Logical functions</span></span>](er-functions-category-logical.md)
