---
title: "แสดงค่าธรรมเนียมสำหรับสินค้าที่ผลิต"
description: "ต้นทุนคงที่ของสินค้าที่ผลิตจะสะท้อนเวลาเซ็ตอัพของการดำเนินการและส่วนประกอบที่มีปริมาณคงที่หรือยอดของเสียแบบคงที่"
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9f41939554cd22045940af937f227f43ba098394
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---

# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="c5d02-103">แสดงค่าธรรมเนียมสำหรับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="c5d02-103">Display charges for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c5d02-104">ต้นทุนคงที่ของสินค้าที่ผลิตจะสะท้อนเวลาเซ็ตอัพของการดำเนินการและส่วนประกอบที่มีปริมาณคงที่หรือยอดของเสียแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="c5d02-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="c5d02-105">ยอดเงินที่คำนวณได้ของค่าธรรมเนียมของสินค้าอาจถูกแสดงพร้อมกับต้นทุนต่อหน่วยของสินค้า</span><span class="sxs-lookup"><span data-stu-id="c5d02-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="c5d02-106">อย่างไรก็ตาม บางครั้งค่าธรรมเนียมจะแสดงเป็นฟิลด์แยกต่างหาก และจะไม่ได้รวมอยู่ในต้นทุนต่อหน่วยของสินค้า</span><span class="sxs-lookup"><span data-stu-id="c5d02-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="c5d02-107">หากค่าธรรมเนียมแสดงเป็นฟิลด์แยกต่างหาก จะมีฟิลด์หนึ่งแสดงยอดรวมค่าธรรมเนียม และอีกฟิลด์หนึ่งจะแสดงขนาดล็อตต้นทุนที่ใช้ตัดยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="c5d02-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="c5d02-108">หน้าราคาสินค้า เป็นต้น จะแสดงค่าธรรมเนียมเป็นฟิลด์แยกต่างหากสองฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c5d02-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="c5d02-109">อย่างไรก็ตาม หน้าเสร็จสมบูรณ์จะแสดงยอดรวมต้นทุนต่อหน่วยของสินค้า พร้อมกับต้นทุนตัดจำหน่ายซึ่งรวมอยู่ในต้นทุนต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="c5d02-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>
<span data-ttu-id="c5d02-110">ค่าธรรมเนียมสำหรับสินค้าที่ผลิตจะรวมอยู่ในต้นทุนต่อหน่วยของสินค้าเพื่อวัตถุประสงค์ในการทำให้เป็นต้นทุนมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="c5d02-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="c5d02-111">หรืออาจรวมค่าใช้จ่ายเบ็ดเตล็ดนี้เพื่อวัตถุประสงค์ในการวางแผนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c5d02-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="c5d02-112">นโยบายในเวอร์ชันการคำนวณต้นทุนนั้นจะเป็นตัวกำหนดการรวมค่าธรรมเนียมไว้ในต้นทุนสำหรับสินค้าที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="c5d02-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="c5d02-113">เมื่อคุณเรียกใช้เรกคอร์ดต้นทุนของสินค้า คุณจะต้องอัพเดตค่าธรรมเนียมสำหรับข้อมูลต้นทุนพื้นฐานของสินค้า ซึ่งแสดงในหน้าราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="c5d02-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="c5d02-114">ค่าธรรมเนียมจะแสดงเป็นฟิลด์แยกต่างหากสองฟิลด์ และจะไม่ได้รวมอยู่ในต้นทุนต่อหน่วยของสินค้า</span><span class="sxs-lookup"><span data-stu-id="c5d02-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="c5d02-115">การเรียกใช้งานแต่ละครั้งจะอัพเดตข้อมูลต้นทุนพื้นฐานของสินค้า แม้ว่าการเรียกใช้งานจะแสดงไซต์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="c5d02-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="c5d02-116">ดังนั้น คุณจึงควรดูข้อมูลต้นทุนพื้นฐานประกอบเป็นข้อมูลอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="c5d02-116">Therefore, you should view the base cost information as reference information.</span></span>






