---
title: ฟังก์ชัน GETCURRENTCOMPANY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ GETCURRENTCOMPANY (ER)
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
ms.openlocfilehash: d91caff1a1b89e060a16833e53f3647208ed3826
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041434"
---
# <span data-ttu-id="fdae6-103"><a name="GETCURRENTCOMPANY">ฟังก์ชัน GETCURRENTCOMPANY ER</a></span><span class="sxs-lookup"><span data-stu-id="fdae6-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdae6-104">ฟังก์ชัน `GETCURRENTCOMPANY` ส่งคืนค่า *สตริง* ที่แสดงรหัสสำหรับนิติบุคคล (บริษัท) ที่ผู้ใช้ลงชื่อเข้าใช้ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="fdae6-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdae6-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="fdae6-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="fdae6-106">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="fdae6-106">Return values</span></span>

<span data-ttu-id="fdae6-107">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="fdae6-107">*String*</span></span>

<span data-ttu-id="fdae6-108">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="fdae6-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="fdae6-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="fdae6-109">Example</span></span>

<span data-ttu-id="fdae6-110">`GETCURRENTCOMPANY ()` ส่งคืน **USMF** สำหรับผู้ใช้ที่ลงชื่อเข้าใช้ไปยังบริษัท **Contoso Entertainment System USA**</span><span class="sxs-lookup"><span data-stu-id="fdae6-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdae6-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fdae6-111">Additional resources</span></span>

[<span data-ttu-id="fdae6-112">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="fdae6-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
