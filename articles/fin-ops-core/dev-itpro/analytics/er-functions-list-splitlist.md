---
title: ฟังก์ชัน ER SPLITLIST
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SPLITLIST
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745580"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="154df-103">ฟังก์ชัน ER SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="154df-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="154df-104">ฟังก์ชัน `SPLITLIST` แบ่งรายการที่ระบุเป็นชุดย่อย (หรือชุดงาน) ซึ่งแต่ละชุดประกอบด้วยจำนวนเรกคอร์ดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="154df-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="154df-105">จากนั้นจะส่งกลับผลลัพธ์เป็นค่า *รายการเรกคอร์ด* ใหม่ที่ประกอบด้วยชุดงาน</span><span class="sxs-lookup"><span data-stu-id="154df-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="154df-106">ไวยากรณ์ 1</span><span class="sxs-lookup"><span data-stu-id="154df-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="154df-107">ไวยากรณ์ 2</span><span class="sxs-lookup"><span data-stu-id="154df-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="154df-108">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="154df-108">Arguments</span></span>

<span data-ttu-id="154df-109">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="154df-109">`list`: *Record list*</span></span>

<span data-ttu-id="154df-110">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="154df-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="154df-111">`number`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="154df-111">`number`: *Integer*</span></span>

<span data-ttu-id="154df-112">จำนวนสูงสุดของเรกคอร์ดต่อชุดงาน</span><span class="sxs-lookup"><span data-stu-id="154df-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="154df-113">`on-demand reading flag`: *บูลีน*</span><span class="sxs-lookup"><span data-stu-id="154df-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="154df-114">ค่า *บูลีน* ที่ระบุว่าควรมีการสร้างองค์ประกอบของรายการย่อยตามความต้องการหรือไม่</span><span class="sxs-lookup"><span data-stu-id="154df-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="154df-115">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="154df-115">Return values</span></span>

<span data-ttu-id="154df-116">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="154df-116">*Record list*</span></span>

<span data-ttu-id="154df-117">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="154df-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="154df-118">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="154df-118">Usage notes</span></span>

<span data-ttu-id="154df-119">รายการของชุดงานที่ส่งคืนประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="154df-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="154df-120">**ค่า:** *รายการ*</span><span class="sxs-lookup"><span data-stu-id="154df-120">**Value:** *List*</span></span>

    <span data-ttu-id="154df-121">รายการของเรกคอร์ดที่เป็นของชุดงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="154df-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="154df-122">**Batchnumber:** *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="154df-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="154df-123">หมายเลขของชุดงานปัจจุบันในรายการที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="154df-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="154df-124">เมื่อตั้งค่าแฟล็กการอ่านตามความต้องการเป็น **จริง** รายการย่อยจะถูกสร้างขึ้นตามการร้องขอ ซึ่งอนุญาตให้ลดปริมาณการใช้หน่วยความจํา แต่อาจทําให้ประสิทธิภาพการลดลง ถ้าองค์ประกอบไม่ได้ถูกใช้ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="154df-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="154df-125">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="154df-125">Example</span></span>

<span data-ttu-id="154df-126">ในภาพประกอบต่อไปนี้ แหล่งข้อมูล **รายการ** ถูกสร้างเป็นรายการเรกคอร์ดที่มีสามเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="154df-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="154df-127">รายการนี้จะถูกแบ่งออกเป็นชุดงาน ซึ่งแต่ละชุดงานประกอบด้วยเรกคอร์ดสองรายการ</span><span class="sxs-lookup"><span data-stu-id="154df-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="154df-128">ภาพประกอบต่อไปนี้แสดงโครงร่างรูปแบบที่มีการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="154df-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="154df-129">ในโครงร่างนี้รูปแบบ การผูกกับแหล่งข้อมูล **รายการ** ถูกสร้างเพื่อสร้างเอาท์พุทในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="154df-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="154df-130">เอาท์พุทนี้แสดงโหนดแต่ละโหนดสำหรับแต่ละชุดงานและเรกคอร์ดในนั้น</span><span class="sxs-lookup"><span data-stu-id="154df-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="154df-131">ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบที่มีการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="154df-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="154df-132">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="154df-132">Additional resources</span></span>

[<span data-ttu-id="154df-133">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="154df-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
