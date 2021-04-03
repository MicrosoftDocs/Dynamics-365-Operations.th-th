---
title: ฟังก์ชัน ER SPLITLIST
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) SPLITLIST
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
ms.openlocfilehash: af8c413726ca8d9f92eff18807e7fa9002fc9d37
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559149"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="20e37-103">ฟังก์ชัน ER SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="20e37-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20e37-104">ฟังก์ชัน `SPLITLIST` แบ่งรายการที่ระบุเป็นชุดย่อย (หรือชุดงาน) ซึ่งแต่ละชุดประกอบด้วยจำนวนเรกคอร์ดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="20e37-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="20e37-105">จากนั้นจะส่งกลับผลลัพธ์เป็นค่า *รายการเรกคอร์ด* ใหม่ที่ประกอบด้วยชุดงาน</span><span class="sxs-lookup"><span data-stu-id="20e37-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="20e37-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="20e37-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="20e37-107">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="20e37-107">Arguments</span></span>

<span data-ttu-id="20e37-108">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="20e37-108">`list`: *Record list*</span></span>

<span data-ttu-id="20e37-109">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="20e37-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="20e37-110">`number`: *เลขจำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="20e37-110">`number`: *Integer*</span></span>

<span data-ttu-id="20e37-111">จำนวนสูงสุดของเรกคอร์ดต่อชุดงาน</span><span class="sxs-lookup"><span data-stu-id="20e37-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="20e37-112">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="20e37-112">Return values</span></span>

<span data-ttu-id="20e37-113">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="20e37-113">*Record list*</span></span>

<span data-ttu-id="20e37-114">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="20e37-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="20e37-115">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="20e37-115">Usage notes</span></span>

<span data-ttu-id="20e37-116">รายการของชุดงานที่ส่งคืนประกอบด้วยองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="20e37-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="20e37-117">**ค่า:** *รายการ*</span><span class="sxs-lookup"><span data-stu-id="20e37-117">**Value:** *List*</span></span>

    <span data-ttu-id="20e37-118">รายการของเรกคอร์ดที่เป็นของชุดงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="20e37-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="20e37-119">**Batchnumber:** *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="20e37-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="20e37-120">หมายเลขของชุดงานปัจจุบันในรายการที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="20e37-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="20e37-121">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="20e37-121">Example</span></span>

<span data-ttu-id="20e37-122">ในภาพประกอบต่อไปนี้ แหล่งข้อมูล **รายการ** ถูกสร้างเป็นรายการเรกคอร์ดที่มีสามเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="20e37-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="20e37-123">รายการนี้จะถูกแบ่งออกเป็นชุดงาน ซึ่งแต่ละชุดงานประกอบด้วยเรกคอร์ดสองรายการ</span><span class="sxs-lookup"><span data-stu-id="20e37-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="20e37-124">ภาพประกอบต่อไปนี้แสดงโครงร่างรูปแบบที่มีการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="20e37-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="20e37-125">ในโครงร่างนี้รูปแบบ การผูกกับแหล่งข้อมูล **รายการ** ถูกสร้างเพื่อสร้างเอาท์พุทในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="20e37-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="20e37-126">เอาท์พุทนี้แสดงโหนดแต่ละโหนดสำหรับแต่ละชุดงานและเรกคอร์ดในนั้น</span><span class="sxs-lookup"><span data-stu-id="20e37-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="20e37-127">ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบที่มีการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="20e37-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="20e37-128">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="20e37-128">Additional resources</span></span>

[<span data-ttu-id="20e37-129">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="20e37-129">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]