---
title: ฟังก์ชัน GETCURRENTCOMPANY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ GETCURRENTCOMPANY (ER)
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: fcb5ef2f218a85bab25f830db583343504c46e98
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567555"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="b288c-103">ฟังก์ชัน GETCURRENTCOMPANY ER</span><span class="sxs-lookup"><span data-stu-id="b288c-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b288c-104">ฟังก์ชัน `GETCURRENTCOMPANY` ส่งคืนค่า *สตริง* ที่แสดงรหัสสำหรับนิติบุคคล (บริษัท) ที่ผู้ใช้ลงชื่อเข้าใช้ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b288c-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="b288c-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="b288c-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="b288c-106">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="b288c-106">Return values</span></span>

<span data-ttu-id="b288c-107">*สตริง*</span><span class="sxs-lookup"><span data-stu-id="b288c-107">*String*</span></span>

<span data-ttu-id="b288c-108">ค่าข้อความที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b288c-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b288c-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b288c-109">Example</span></span>

<span data-ttu-id="b288c-110">`GETCURRENTCOMPANY ()` ส่งคืน **USMF** สำหรับผู้ใช้ที่ลงชื่อเข้าใช้ไปยังบริษัท **Contoso Entertainment System USA**</span><span class="sxs-lookup"><span data-stu-id="b288c-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b288c-111">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b288c-111">Additional resources</span></span>

[<span data-ttu-id="b288c-112">ฟังก์ชันอื่นๆ (เฉพาะโดเมนธุรกิจ)</span><span class="sxs-lookup"><span data-stu-id="b288c-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]