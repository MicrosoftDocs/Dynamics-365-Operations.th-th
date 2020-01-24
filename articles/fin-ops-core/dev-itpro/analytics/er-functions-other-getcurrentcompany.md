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
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916004"
---
# <span data-ttu-id="b1c13-103"><a name="GETCURRENTCOMPANY">ฟังก์ชัน GETCURRENTCOMPANY ER</a></span><span class="sxs-lookup"><span data-stu-id="b1c13-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1c13-104">ฟังก์ชัน `GETCURRENTCOMPANY` ส่งคืนค่า *สตริง* ที่แสดงรหัสสำหรับนิติบุคคล (บริษัท) ที่ผู้ใช้ลงชื่อเข้าใช้ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b1c13-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1c13-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="b1c13-105">Syntax</span></span>

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="b1c13-106">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="b1c13-106">Return values</span></span>

<span data-ttu-id="b1c13-107">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="b1c13-107">*String*</span></span>

<span data-ttu-id="b1c13-108">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b1c13-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b1c13-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b1c13-109">Example</span></span>

<span data-ttu-id="b1c13-110">`GETCURRENTCOMPANY ()` ส่งคืน **USMF** สำหรับผู้ใช้ที่ลงชื่อเข้าใช้ไปยังบริษัท **Contoso Entertainment System USA**</span><span class="sxs-lookup"><span data-stu-id="b1c13-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1c13-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b1c13-111">Additional resources</span></span>

[<span data-ttu-id="b1c13-112">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="b1c13-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
