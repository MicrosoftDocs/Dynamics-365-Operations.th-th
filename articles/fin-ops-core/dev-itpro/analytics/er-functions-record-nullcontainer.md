---
title: ฟังก์ชัน NULLCONTAINER ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ NULLCONTAINER (ER)
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: d08a4a12d2b142744d3f35c6f1088ec25158c97c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563233"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="f3109-103">ฟังก์ชัน NULLCONTAINER ER</span><span class="sxs-lookup"><span data-stu-id="f3109-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3109-104">ฟังก์ชัน `NULLCONTAINER` ส่งกลับค่า *คอนเทนเนอร์ (เรกคอร์ด)* ที่เป็น null ซึ่งมีโครงสร้างเดียวกันกับรายการเรกคอร์ดหรือเรกคอร์ดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f3109-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3109-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="f3109-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="f3109-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="f3109-106">Arguments</span></span>

<span data-ttu-id="f3109-107">`list`: *รายการเรกคอร์ด* หรือ *คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="f3109-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="f3109-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *รายการเรกคอร์ด* หรือ *คอนเทนเนอร์ (เรกคอร์ด)* อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f3109-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f3109-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="f3109-109">Return values</span></span>

<span data-ttu-id="f3109-110">*คอนเทนเนอร์ (เรกคอร์ด)*</span><span class="sxs-lookup"><span data-stu-id="f3109-110">*Container (record)*</span></span>

<span data-ttu-id="f3109-111">ค่าเรกคอร์ดที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="f3109-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f3109-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f3109-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="f3109-113">ฟังก์ชันนี้ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="f3109-113">This function is obsolete.</span></span> <span data-ttu-id="f3109-114">ใช้ฟังก์ชัน `EMPTYRECORD` แทน</span><span class="sxs-lookup"><span data-stu-id="f3109-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="f3109-115">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [EMPTYRECORD](er-functions-record-emptyrecord.md)</span><span class="sxs-lookup"><span data-stu-id="f3109-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="f3109-116">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f3109-116">Example</span></span>

<span data-ttu-id="f3109-117">`NULLCONTAINER (SPLIT ("abc", 1))` ส่งคืนเรกคอร์ดที่ว่างเปล่าใหม่ที่มีโครงสร้างเดียวกันกับรายการที่ถูกส่งคืนโดยฟังก์ชัน `SPLIT`</span><span class="sxs-lookup"><span data-stu-id="f3109-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="f3109-118">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [SPLIT](er-functions-list-split.md)</span><span class="sxs-lookup"><span data-stu-id="f3109-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3109-119">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f3109-119">Additional resources</span></span>

[<span data-ttu-id="f3109-120">ฟังก์ชันเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="f3109-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]