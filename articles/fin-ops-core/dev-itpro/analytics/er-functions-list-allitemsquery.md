---
title: ฟังก์ชัน ALLITEMSQUERY ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ALLITEMSQUERY
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 647019a103006c8b74bc26885c51f5372dcf0c42
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917522"
---
# <span data-ttu-id="30777-103"><a name="ALLITEMSQUERY">ฟังก์ชัน ALLITEMSQUERY ER</a></span><span class="sxs-lookup"><span data-stu-id="30777-103"><a name="ALLITEMSQUERY">ALLITEMSQUERY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30777-104">ฟังก์ชัน `ALLITEMSQUERY` ทำงานเป็นแบบสอบถาม SQL ที่เชื่อมต่อกัน</span><span class="sxs-lookup"><span data-stu-id="30777-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="30777-105">จะส่งกลับค่า *รายการเรกคอร์ด* ที่ทำให้แบนใหม่ที่ประกอบด้วยรายการของเรกคอร์ดที่แสดงถึงรายการทั้งหมดที่ตรงกับพาธที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="30777-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="30777-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="30777-106">Syntax</span></span>

```
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="30777-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="30777-107">Arguments</span></span>

<span data-ttu-id="30777-108">`path`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="30777-108">`path`: *Record list*</span></span>

<span data-ttu-id="30777-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="30777-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="30777-110">ต้องมีอย่างน้อยหนึ่งความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="30777-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="30777-111">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="30777-111">Return values</span></span>

<span data-ttu-id="30777-112">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="30777-112">*Record list*</span></span>

<span data-ttu-id="30777-113">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="30777-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="30777-114">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="30777-114">Usage notes</span></span>

<span data-ttu-id="30777-115">ต้องกำหนดพาธที่ระบุเป็นพาธแหล่งข้อมูลที่ถูกต้องขององค์ประกอบแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="30777-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="30777-116">ต้องมีอย่างน้อยหนึ่งความสัมพันธ์ด้วย</span><span class="sxs-lookup"><span data-stu-id="30777-116">It must also contain at least one relation.</span></span> <span data-ttu-id="30777-117">องค์ประกอบข้อมูล เช่น *สตริง* พาธ และ *วันที่* ควรรายงานข้อผิดพลาดในตัวสร้างนิพจน์การรายงานทางอิเล็กทรอนิกส์ (ER) ในขณะที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="30777-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="30777-118">เมื่อฟังก์ชันนี้ถูกนำไปใช้กับแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด* ที่อ้างถึงออบเจ็กของแอปพลิเคชันต์ที่สามารถเรียกโดยตรงโดยใช้ SQL (ตัวอย่างเช่น ตารางเอนทิตี หรือแบบสอบถาม) จะทำงานเป็นแบบสอบถาม SQL ที่เข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="30777-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="30777-119">มิฉะนั้นจะทำงานในหน่วยความจำเป็นฟังก์ชัน [ALLITEMS](er-functions-list-allitems.md)</span><span class="sxs-lookup"><span data-stu-id="30777-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="30777-120">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="30777-120">Example</span></span>

<span data-ttu-id="30777-121">คุณกำหนดแหล่งข้อมูลต่อไปนี้ในการแม็ปแบบจำลองของคุณ:</span><span class="sxs-lookup"><span data-stu-id="30777-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="30777-122">แหล่งข้อมูล **CustInv** ของชนิด *เรกคอร์ดของตาราง* ที่อ้างอิงถึงตาราง CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="30777-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="30777-123">แหล่งข้อมูล **FilteredInv** ของชนิด *ฟิลด์ที่มีการคำนวณ* ที่ประกอบด้วยนิพจน์ `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="30777-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="30777-124">**JourLines** ของชนิด *ฟิลด์ที่มีการคำนวณ* ที่ประกอบด้วยนิพจน์ `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="30777-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="30777-125">เมื่อคุณรันการแม็ปแบบจำลองของคุณในการเรียกแหล่งข้อมูล **JourLines** จะมีการรันคำสั่ง SQL ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="30777-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="30777-126">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="30777-126">Additional resources</span></span>

[<span data-ttu-id="30777-127">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="30777-127">List functions</span></span>](er-functions-category-list.md)
