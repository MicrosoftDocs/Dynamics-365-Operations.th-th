---
title: ฟังก์ชัน GUIDVALUE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ GUIDVALUE (ER)
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685966"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="df118-103">ฟังก์ชัน GUIDVALUE ER</span><span class="sxs-lookup"><span data-stu-id="df118-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df118-104">ฟังก์ชัน `GUIDVALUE` แปลงอินพุตที่ระบุของชนิด *สตริง* เป็นรายการข้อมูลของชนิด *GUID*</span><span class="sxs-lookup"><span data-stu-id="df118-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="df118-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="df118-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="df118-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="df118-106">Arguments</span></span>

<span data-ttu-id="df118-107">`input`: *สตริง*</span><span class="sxs-lookup"><span data-stu-id="df118-107">`input`: *String*</span></span>

<span data-ttu-id="df118-108">พาธที่ถูกต้องของแหล่งข้อมูลของชนิด *สตริง*</span><span class="sxs-lookup"><span data-stu-id="df118-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="df118-109">ส่งคืนค่า</span><span class="sxs-lookup"><span data-stu-id="df118-109">Return values</span></span>

<span data-ttu-id="df118-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="df118-110">*GUID*</span></span>

<span data-ttu-id="df118-111">ค่าตัวระบุที่ไม่ซ้ำกันส่วนกลาง (GUID) ที่เป็นผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="df118-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="df118-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="df118-112">Usage notes</span></span>

<span data-ttu-id="df118-113">เพื่อทำการแปลงในทิศทางตรงกันข้าม (นั่นคือ การแปลงระบุข้อมูลป้อนเข้าที่ระบุของชนิดข้อมูล *GUID* เป็นรายการข้อมูลของชนิดข้อมูล *สตริง*) คุณสามารถใช้ฟังก์ชัน [TEXT](er-functions-text-text.md) ได้</span><span class="sxs-lookup"><span data-stu-id="df118-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="df118-114">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="df118-114">Example</span></span>

<span data-ttu-id="df118-115">คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:</span><span class="sxs-lookup"><span data-stu-id="df118-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="df118-116">แหล่งข้อมูล **myID** ของชนิด *ฟิลด์ที่มีการคำนวณ* ที่มีนิพจน์`GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="df118-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="df118-117">แหล่งข้อมูล **ผู้ใช้** ของชนิด *เรกคอร์ดของตาราง* ที่อ้างอิงถึงตาราง UserInfo</span><span class="sxs-lookup"><span data-stu-id="df118-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="df118-118">จากนั้นคุณสามารถใช้นิพจน์ เช่น `FILTER (Users, Users.objectId = myID)` เพื่อกรองตาราง UserInfo โดยฟิลด์ **objectId** ของชนิดข้อมูล *GUID*</span><span class="sxs-lookup"><span data-stu-id="df118-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df118-119">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="df118-119">Additional resources</span></span>

[<span data-ttu-id="df118-120">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="df118-120">Text functions</span></span>](er-functions-category-text.md)
