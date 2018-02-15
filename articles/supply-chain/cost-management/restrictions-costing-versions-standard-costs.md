---
title: "ข้อจำกัดในเวอร์ชันการคิดต้นทุนสำหรับต้นทุนมาตรฐาน"
description: "หัวข้อนี้อธิบายข้อจำกัดที่ใช้กับเวอร์ชันการคิดต้นทุนสำหรับต้นทุนมาตรฐาน"
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e14d5d11e987d2dbc841f86c39fc7e94864144d3
ms.openlocfilehash: 658575492597eed91509561f4710f07e271c53c8
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="68ce4-103">ข้อจำกัดในเวอร์ชันการคิดต้นทุนสำหรับต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="68ce4-103">Restrictions on costing versions for standard costs</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="68ce4-104">หัวข้อนี้อธิบายข้อจำกัดที่ใช้กับเวอร์ชันการคิดต้นทุนสำหรับต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="68ce4-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="68ce4-105">ข้อจำกัดต่อไปนี้จะช่วยให้มั่นใจว่าการคิดต้นทุนนั้นเป็นไปตามหลักมาตรฐาน:</span><span class="sxs-lookup"><span data-stu-id="68ce4-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="68ce4-106">ค่าธรรมเนียมต้องถูกรวมอยู่ในต้นทุนของสินค้า</span><span class="sxs-lookup"><span data-stu-id="68ce4-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="68ce4-107">ค่าธรรมเนียมสำหรับสินค้าที่ผลิต แสดงถึงต้นทุนคงที่ซึ่งตัดจำหน่ายในสูตรการผลิต (BOM) และข้อมูลกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="68ce4-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="68ce4-108">ดังนั้น จึงต้องรวมค่าธรรมเนียมในต้นทุนต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="68ce4-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="68ce4-109">ค่าธรรมเนียมสำหรับสินค้าที่ซื้อจะถูกรวมอยู่ในต้นทุนต่อหน่วยของสินค้าด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="68ce4-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="68ce4-110">การคำนวณต้นทุนมาตรฐานสำหรับสินค้าที่ผลิต ต้องยึดตามเรกคอร์ดต้นทุนในเวอร์ชันการคิดต้นทุนสำหรับต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="68ce4-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="68ce4-111">แหล่งข้อมูลต้นทุนอื่นสามารถใช้ได้กับเวอร์ชันการคิดต้นทุนสำหรับต้นทุนที่วางแผนไว้เท่านั้น เช่น ข้อตกลงทางการค้าเกี่ยวกับราคาซื้อสำหรับสินค้าที่ซื้อ</span><span class="sxs-lookup"><span data-stu-id="68ce4-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="68ce4-112">แหล่งที่มาอื่นของข้อมูลต้นทุนจะถูกกำหนดตามกลุ่มการคำนวณ BOM</span><span class="sxs-lookup"><span data-stu-id="68ce4-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="68ce4-113">การคำนวณ BOM ต้องถูกดำเนินการในโหมดการกระจายระดับเดียว</span><span class="sxs-lookup"><span data-stu-id="68ce4-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="68ce4-114">คุณสามารถคัดลอกข้อมูลต้นทุนสินค้าสำหรับต้นทุนมาตรฐานไปยังเวอร์ชันการคำนวณต้นทุนอื่นที่มีต้นทุนมาตรฐานหรือต้นทุนที่วางแผนไว้ </span><span class="sxs-lookup"><span data-stu-id="68ce4-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="68ce4-115">อย่างไรก็ตาม ข้อมูลต้นทุนสินค้าสำหรับต้นทุนที่วางแผนไว้ไม่สามารถถูกคัดลอกไปยังเวอร์ชันต้นทุนที่มีต้นทุนมาตรฐานอยู่ได้ เนื่องจากข้อจำกัดที่กล่าวถึงก่อนหน้าในหัวข้อนี้ไม่สามารถใช้กับต้นทุนที่วางแผนไว้ได้</span><span class="sxs-lookup"><span data-stu-id="68ce4-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="68ce4-116">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="68ce4-116">Related topics</span></span>
--------

[<span data-ttu-id="68ce4-117">เวอร์ชันการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="68ce4-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="68ce4-118">อัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมที่ไม่มีการผลิต</span><span class="sxs-lookup"><span data-stu-id="68ce4-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="68ce4-119">การเตรียมการรักษาต้นทุนมาตรฐานสำหรับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="68ce4-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)


