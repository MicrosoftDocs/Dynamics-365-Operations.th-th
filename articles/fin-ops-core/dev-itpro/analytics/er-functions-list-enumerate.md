---
title: ฟังก์ชัน ENUMERATE ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ (ER) ENUMERATE
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
ms.openlocfilehash: d34904571ee6de8b36a0840a9470f16858489163
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042160"
---
# <span data-ttu-id="74c6f-103"><a name="ENUMERATE">ฟังก์ชัน ENUMERATE ER</a></span><span class="sxs-lookup"><span data-stu-id="74c6f-103"><a name="ENUMERATE">ENUMERATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74c6f-104">ฟังก์ชัน `ENUMERATE` ส่งกลับค่า *รายการเรกคอร์ด* ใหม่ที่ประกอบด้วยเฉพาะเรกคอร์ดที่ระบุรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="74c6f-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c6f-105">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="74c6f-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="74c6f-106">อาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="74c6f-106">Arguments</span></span>

<span data-ttu-id="74c6f-107">`list`: *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="74c6f-107">`list`: *Record list*</span></span>

<span data-ttu-id="74c6f-108">พาธที่ถูกต้องของรายการแหล่งข้อมูลของชนิดข้อมูล *รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="74c6f-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="74c6f-109">ค่าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="74c6f-109">Return values</span></span>

<span data-ttu-id="74c6f-110">*รายการเรกคอร์ด*</span><span class="sxs-lookup"><span data-stu-id="74c6f-110">*Record list*</span></span>

<span data-ttu-id="74c6f-111">รายการผลลัพธ์ของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="74c6f-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="74c6f-112">บันทึกย่อการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="74c6f-112">Usage notes</span></span>

<span data-ttu-id="74c6f-113">รายการของเรกคอร์ดที่ระบุที่ถูกส่งกลับแสดงองค์ประกอบเพิ่มเติมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="74c6f-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="74c6f-114">เรกคอร์ดของฟิลด์ส่วนประกอบ (**ค่า**)</span><span class="sxs-lookup"><span data-stu-id="74c6f-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="74c6f-115">ดัชนีเรกคอร์ดปัจจุบัน (คอมโพเนนต์ **หมายเลข**)</span><span class="sxs-lookup"><span data-stu-id="74c6f-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="74c6f-116">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="74c6f-116">Example</span></span>

<span data-ttu-id="74c6f-117">ในแผนภาพต่อไปนี้ แหล่งข้อมูล **ที่ระบุ** ถูกสร้างเป็นรายการที่ระบุของเรกคอร์ดผู้จัดจำหน่ายจากแหล่งข้อมูล **ผู้จัดจำหน่าย** ที่อ้างอิงถึงตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="74c6f-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="74c6f-118">ภาพประกอบต่อไปนี้แสดงรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="74c6f-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="74c6f-119">ในรูปแบบนี้ การผูกข้อมูลถูกสร้างเพื่อสร้างเอาท์พุทในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="74c6f-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="74c6f-120">เอาท์พุทนี้แสดงผู้จัดจำหน่ายแต่ละรายเป็นโหนดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="74c6f-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="74c6f-121">ภาพประกอบต่อไปนี้แสดงผลลัพธ์ เมื่อมีการรันรูปแบบที่มีการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="74c6f-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="74c6f-122">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="74c6f-122">Additional resources</span></span>

[<span data-ttu-id="74c6f-123">ฟังก์ชันรายการ</span><span class="sxs-lookup"><span data-stu-id="74c6f-123">List functions</span></span>](er-functions-category-list.md)
