---
title: ฟังก์ชัน TEXT ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ TEXT (ER)
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d489da24d0589549153913bbc6db699e3c217e72
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682907"
---
# <a name="text-er-function"></a><span data-ttu-id="c2a83-103">ฟังก์ชัน TEXT ER</span><span class="sxs-lookup"><span data-stu-id="c2a83-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2a83-104">ฟังก์ชัน `TEXT` ส่งคืนตัวเลขที่ระบุเป็นค่า *สตริง* หลังจากที่ได้ถูกแปลงเป็นข้อความแบบสตริงที่ถูกจัดรูปแบบตามการตั้งค่าตำแหน่งที่ตั้งของเซิร์ฟเวอร์ของอินสแตนซ์ของแอพลิเคชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="c2a83-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a83-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="c2a83-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="c2a83-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="c2a83-106">Arguments</span></span>

<span data-ttu-id="c2a83-107">`number`: *จำนวนเต็ม* หรือ *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="c2a83-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="c2a83-108">หมายเลขที่ต้องถูกแปลงเป็นสตริงข้อความ</span><span class="sxs-lookup"><span data-stu-id="c2a83-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="c2a83-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="c2a83-109">Return values</span></span>

<span data-ttu-id="c2a83-110">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="c2a83-110">*String*</span></span>

<span data-ttu-id="c2a83-111">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="c2a83-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c2a83-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c2a83-112">Usage notes</span></span>

<span data-ttu-id="c2a83-113">สำหรับค่าของชนิด *จำนวนจริง* การแปลงสตริงจะถูกจำกัดเป็นทศนิยมสองตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="c2a83-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="c2a83-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c2a83-114">Example</span></span>

<span data-ttu-id="c2a83-115">ถ้าตำแหน่งที่ตั้งของเซิร์ฟเวอร์ของอินสแตนซ์ Microsoft Dynamics 365 Finance ถูกกำหนดเป็น **EN-US**, `TEXT (NOW ())` จะส่งคืนวันที่ของเซสชัน Finance ปัจจุบัน ซึ่งคือ17 ธันวาคม 2015 เป็นสตริงข้อความ **"12/17/2015 07:59:23 AM"**</span><span class="sxs-lookup"><span data-stu-id="c2a83-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="c2a83-116">`TEXT (1/3)` ส่งคืน **"0.33"**</span><span class="sxs-lookup"><span data-stu-id="c2a83-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2a83-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c2a83-117">Additional resources</span></span>

[<span data-ttu-id="c2a83-118">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="c2a83-118">Text functions</span></span>](er-functions-category-text.md)
