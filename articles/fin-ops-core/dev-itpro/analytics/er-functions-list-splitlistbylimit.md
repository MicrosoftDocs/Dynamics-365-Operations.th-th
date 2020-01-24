---
title: ฟังก์ชัน ER SPLITLISTBYLIMIT
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SPLITLISTBYLIMIT
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
ms.openlocfilehash: f9b740b7d46fcfdf0d0b08d03411017cf909265d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916188"
---
# <span data-ttu-id="5bef8-103"><a name="SPLITLISTBYLIMIT">ฟังก์ชัน ER SPLITLISTBYLIMIT</a></span><span class="sxs-lookup"><span data-stu-id="5bef8-103"><a name="SPLITLISTBYLIMIT">SPLITLISTBYLIMIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5bef8-104">ฟังก์ชัน `SPLITLISTBYLIMIT` แยกรายการที่ระบุลงในรายการใหม่ของรายการย่อย (ชุดงาน)</span><span class="sxs-lookup"><span data-stu-id="5bef8-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="5bef8-105">จำนวนของเรกคอร์ดในแต่ละชุดงานจะถูกคำนวณแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="5bef8-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="5bef8-106">จากนั้นฟังก์ชันจะส่งกลับผลลัพธ์เป็นค่า *รายการเรกคอร์ด* ใหม่ที่ประกอบด้วยชุดงาน</span><span class="sxs-lookup"><span data-stu-id="5bef8-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bef8-107">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="5bef8-107">Syntax</span></span>

```
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="5bef8-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="5bef8-108">Arguments</span></span>

<span data-ttu-id="5bef8-109">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="5bef8-109">`list`: *Record list*</span></span>

<span data-ttu-id="5bef8-110">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="5bef8-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="5bef8-111">`limit value`: *จำนวนเต็ม* หรือ *จำนวนจริง*</span><span class="sxs-lookup"><span data-stu-id="5bef8-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="5bef8-112">ค่าสูงสุดของขีดจำกัดที่ใช้ในการแบ่งรายการเดิมเป็นชุดงาน</span><span class="sxs-lookup"><span data-stu-id="5bef8-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="5bef8-113">`limit source`: *ฟิลด์*</span><span class="sxs-lookup"><span data-stu-id="5bef8-113">`limit source`: *Field*</span></span>

<span data-ttu-id="5bef8-114">เส้นทางที่ถูกต้องของเขตข้อมูลของชนิด *จำนวนรวม* หรือ *จำนวนจริง* ในรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5bef8-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="5bef8-115">ค่าของฟิลด์นี้จะกำหนดขั้นตอนที่จะเพิ่มผลรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5bef8-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="5bef8-116">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="5bef8-116">Return values</span></span>

<span data-ttu-id="5bef8-117">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="5bef8-117">*Record list*</span></span>

<span data-ttu-id="5bef8-118">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="5bef8-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5bef8-119">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="5bef8-119">Usage notes</span></span>

<span data-ttu-id="5bef8-120">รายการของชุดงานที่ส่งคืนประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5bef8-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="5bef8-121">**ค่า**: *รายการ*</span><span class="sxs-lookup"><span data-stu-id="5bef8-121">**Value**: *List*</span></span>

    <span data-ttu-id="5bef8-122">รายการของเรกคอร์ดที่เป็นของชุดงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="5bef8-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="5bef8-123">**Batchnumber**: *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="5bef8-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="5bef8-124">หมายเลขของชุดงานปัจจุบันในรายการที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="5bef8-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="5bef8-125">ขีดจำกัดจะไม่ใช้กับสินค้าเดี่ยวของรายการต้นทาง ถ้าแหล่งที่มาของขีดจำกัดเกินขีดจำกัดที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="5bef8-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="5bef8-126">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="5bef8-126">Example</span></span>

<span data-ttu-id="5bef8-127">ภาพประกอบต่อไปนี้แสดงรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="5bef8-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="5bef8-128">ภาพประกอบต่อไปนี้แสดงแหล่งข้อมูลที่ใช้สำหรับรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="5bef8-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="5bef8-129">ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="5bef8-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="5bef8-130">ในกรณีนี้ ผลลัพธ์เป็นรายการแบบธรรมดาของสินค้าโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5bef8-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="5bef8-131">ในภาพประกอบต่อไปนี้ มีการปรับปรุงรูปแบบเดียวกัน เพื่อให้แสดงรายการของสินค้าโภคภัณฑ์ในชุดงานต่างๆ หากชุดงานเดียวต้องรวมโภคภัณฑ์ และน้ำหนักรวมไม่ควรเกินขีดจำกัดที่ 9</span><span class="sxs-lookup"><span data-stu-id="5bef8-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="5bef8-132">ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบที่มีการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="5bef8-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="5bef8-133">ขีดจำกัดจะไม่ถูกใช้กับรายการสุดท้ายของรายการต้นทาง เนื่องจากค่า (**11**) ของแหล่งที่มาของขีดจำกัด (**น้ำหนัก**) เกินขีดจำกัดที่กำหนดไว้ (**9**)</span><span class="sxs-lookup"><span data-stu-id="5bef8-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="5bef8-134">หากต้องการเพิกเฉยต่อรายการย่อยระหว่างการสร้างรายงาน ใช้ฟังก์ชัน `WHERE` หรือนิพจน์ **Enabled** ขององค์ประกอบรูปแบบที่สอดคล้องกันเพื่อละเว้นตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5bef8-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bef8-135">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5bef8-135">Additional resources</span></span>

[<span data-ttu-id="5bef8-136">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="5bef8-136">List functions</span></span>](er-functions-category-list.md)
