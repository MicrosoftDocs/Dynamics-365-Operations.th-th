---
title: ฟังก์ชัน ALLITEMS ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ALLITEMS
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 47113d52e15d3d61f00b3c54229e286eb0f1a8d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745404"
---
# <a name="allitems-er-function"></a><span data-ttu-id="5ed85-103">ฟังก์ชัน ALLITEMS ER</span><span class="sxs-lookup"><span data-stu-id="5ed85-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ed85-104">ฟังก์ชัน `ALLITEMS` จะทำงานเป็นตัวเลือกในหน่วยความจำและส่งกลับ *ค่ารายการ* ที่ยุบใหม่ที่เป็นรายการของเรกคอร์ดที่แสดงถึงรายการทั้งหมดที่ตรงกับพาธที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5ed85-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed85-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="5ed85-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="5ed85-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="5ed85-106">Arguments</span></span>

<span data-ttu-id="5ed85-107">`path`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="5ed85-107">`path`: *Record list*</span></span>

<span data-ttu-id="5ed85-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="5ed85-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5ed85-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="5ed85-109">Return values</span></span>

<span data-ttu-id="5ed85-110">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="5ed85-110">*Record list*</span></span>

<span data-ttu-id="5ed85-111">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="5ed85-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5ed85-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="5ed85-112">Usage notes</span></span>

<span data-ttu-id="5ed85-113">ต้องกำหนดพาธเป็นพาธแหล่งข้อมูลที่ถูกต้องขององค์ประกอบแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="5ed85-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="5ed85-114">องค์ประกอบข้อมูล เช่น สตริงพาธ และวันที่ควรรายงานข้อผิดพลาดในตัวสร้างนิพจน์ การรายงานทางอิเล็กทรอนิกส์ (ER) ในขณะที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="5ed85-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="5ed85-115">เราไม่แนะนำให้คุณใช้ฟังก์ชันนี้สำหรับแหล่งข้อมูลธุรกรรมที่อาจมีข้อมูลจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="5ed85-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="5ed85-116">ให้พิจารณาใช้ฟังก์ชัน [ALLTEMSQUERY](er-functions-list-allitemsquery.md) แทน</span><span class="sxs-lookup"><span data-stu-id="5ed85-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="5ed85-117">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="5ed85-117">Example 1</span></span>

<span data-ttu-id="5ed85-118">ถ้าคุณป้อน `SPLIT("abcdef" , 2)` เป็นแหล่งข้อมูล **DS** นิพจน์ `COUNT( ALLITEMS (DS))` จะส่งกลับค่า **3**</span><span class="sxs-lookup"><span data-stu-id="5ed85-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="5ed85-119">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="5ed85-119">Example 2</span></span>

<span data-ttu-id="5ed85-120">ถ้าคุณป้อน **Vend** เป็นแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* ที่อ้างอิงถึงตารางโปรแกรมประยุกต์ นิพจน์ `ALLITEMS (Vend.'<Relations'.ContactPerson)` จะส่งกลับรายการเรกคอร์ดที่ปรับเป็นระนาบที่มีโครงสร้างตาราง **ContactPerson** และประกอบด้วยบุคคลที่ติดต่อทั้งหมดที่สามารถเข้าถึงได้โดยใช้ **ContactPerson.ContactForParty == VendTable.Party** ที่เกี่ยวข้องกันและที่พร้อมใช้งานสำหรับผู้จัดจำหน่ายทั้งหมดจากตารางผู้ขายที่อ้างอิง</span><span class="sxs-lookup"><span data-stu-id="5ed85-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ed85-121">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5ed85-121">Additional resources</span></span>

[<span data-ttu-id="5ed85-122">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="5ed85-122">List functions</span></span>](er-functions-category-list.md)
