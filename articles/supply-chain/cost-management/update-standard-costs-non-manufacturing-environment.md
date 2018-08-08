---
title: "อัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมที่ไม่มีการผลิต"
description: "บทความนี้ให้คำแนะนำสำหรับวิธีการอัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมที่ไม่มีการผลิต"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 4fa545aa6903bd6f789dda20ab5755ffe9a12b88
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="b71ca-103">อัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมที่ไม่มีการผลิต</span><span class="sxs-lookup"><span data-stu-id="b71ca-103">Update standard costs in a non-manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b71ca-104">บทความนี้ให้คำแนะนำสำหรับวิธีการอัพเดตต้นทุนมาตรฐานในสภาพแวดล้อมที่ไม่มีการผลิต</span><span class="sxs-lookup"><span data-stu-id="b71ca-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="b71ca-105">คำแนะนำต่อไปนี้จะถือว่าคุณใช้วิธีการแบบสองเวอร์ชันเพื่ออัพเดตต้นทุนมาตรฐาน </span><span class="sxs-lookup"><span data-stu-id="b71ca-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="b71ca-106">ในวิธีนี้ การคำนวณต้นทุนในเวอร์ชันหนึ่งประกอบด้วย ต้นทุนมาตรฐานที่กำหนดไว้ตั้งแต่เริ่มแรกสำหรับช่วงเวลาแน่นอนไม่เปลี่ยนแปลง ในขณะที่เวอร์ชันที่สองประกอบด้วยการอัพเดตข้อมูลเพิ่มเติม </span><span class="sxs-lookup"><span data-stu-id="b71ca-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="b71ca-107">การอัพเดตแต่ละครั้งถูกป้อนเป็นเรกคอร์ดต้นทุนซึ่งถูกแนบเวอร์ชันการคิดต้นทุนที่สอง และในท้ายที่สุด จะถูกเปิดใช้งาน </span><span class="sxs-lookup"><span data-stu-id="b71ca-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="b71ca-108">อีกทางหนึ่งคือ วิธีแบบหนึ่งเวอร์ชันใช้ชุดของต้นทุนมาตรฐานที่ถูกกำหนดไว้ตั้งแต่เริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="b71ca-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="b71ca-109">วิธีแบบสองเวอร์ชันต้องการให้คุณกำหนดเวอร์ชันการคิดต้นทุนที่สอง </span><span class="sxs-lookup"><span data-stu-id="b71ca-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="b71ca-110">นี่คือคำแนะนำสำหรับการกำหนดการคิดต้นทุนนี้:</span><span class="sxs-lookup"><span data-stu-id="b71ca-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="b71ca-111">กำหนดชนิดการคำนวณต้นทุนของ **ต้นทุนมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="b71ca-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="b71ca-112">กำหนดรหัสสำคัญที่ระบุเนื้อหาของเวอร์ชันการคำนวณต้นทุน เช่น **2016-UPDATES**</span><span class="sxs-lookup"><span data-stu-id="b71ca-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="b71ca-113">ตรวจสอบให้แน่ใจว่าเนื้อหามีเรกคอร์ดต้นทุนรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="b71ca-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="b71ca-114">อนุญาตให้เรกคอร์ดต้นทุนถูกป้อนสำหรับไซต์ทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="b71ca-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="b71ca-115">ถ้าคุณระบุไซต์ เรกคอร์ดต้นทุนสามารถถูกป้อนสำหรับไซต์ดังกล่าวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b71ca-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="b71ca-116">ระบุว่าไม่มีหลักการถอยกลับเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="b71ca-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="b71ca-117">หลักการถอยกลับจะใช้เฉพาะกับการคำนวณต้นทุนสำหรับสินค้าที่ผลิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b71ca-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="b71ca-118">ในการแก้ไข เปลี่ยนแปลง หรืออัพเดตต้นทุนมาตรฐานสำหรับสินค้าใหม่ ให้ดำเนินการตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b71ca-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="b71ca-119">ใช้หน้า **เวอร์ชันการคิดต้นทุน** **ตั้งค่า** เพื่อทำให้ข้อมูลต้นทุนสามารถถูกป้อนลงในเวอร์ชันการคำนวณต้นทุนที่สองได้</span><span class="sxs-lookup"><span data-stu-id="b71ca-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="b71ca-120">และอาจป้องกันการเรียกใช้งานของต้นทุนที่เปิดค้างไว้ ดังนั้นการเรียกใช้งานจะได้รับอนุญาตหลังจากที่มีการกำหนดต้นทุนที่เปิดค้างไว้ทั้งหมดอย่างถูกต้องและเสร็จสมบูรณ์แล้ว </span><span class="sxs-lookup"><span data-stu-id="b71ca-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="b71ca-121">หรือคุณอาจป้อนวันที่เริ่มต้นในฟิลด์ **วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="b71ca-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="b71ca-122">ดังเช่นคำแนะนำทั่วไป ให้ใช้วันที่ที่คุณต้องการเปิดใช้งานการอัพเดตที่เพิ่มขึ้น </span><span class="sxs-lookup"><span data-stu-id="b71ca-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="b71ca-123">หรือปล่อยให้ฟิลด์ **วันที่เริ่มต้น** ว่างเปล่าสำหรับเวอร์ชันการคำนวณต้นทุน แล้วป้อนวันที่ในฟิลด์ **วันที่เริ่มต้น** สำหรับเรกคอร์ดต้นทุนแต่ละเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="b71ca-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="b71ca-124">ใช้หน้า **ราคาสินค้า** เพื่อป้อนการอัพเดตเป็นเรกคอร์ดต้นทุนสินค้า ที่ถูกแนบอยู่ในเวอร์ชันการคิดต้นทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="b71ca-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="b71ca-125">ใช้รายงาน **ราคาสินค้า** เพื่อตรวจสอบความสมบูรณ์และความถูกต้องของเรกคอร์ดต้นทุนสินค้า ที่ถูกแนบอยู่ในเวอร์ชันการคิดต้นทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="b71ca-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="b71ca-126">ใช้หน้า **การบำรุงรักษาเวอร์ชันการคิดต้นทุน** เพื่อเปลี่ยนแฟล็กการบล็อค เพื่ออนุญาตการเปิดใช้งานของเรกคอร์ดต้นทุนที่เปิดค้างไว้ที่ถูกแนบอยู่ในเวอร์ชันการคิดต้นทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="b71ca-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="b71ca-127">ใช้หน้า **เรียกใช้งานราคา** (ซึ่งคุณสามารถเปิดได้จากหน้า **การบำรุงรักษาเวอร์ชันการคิดต้นทุน** ) เพื่อเปิดใช้งานเรกคอร์ดต้นทุนสินค้าที่ค้างอยู่ทั้งหมดที่ถูกแนบอยู่ในเวอร์ชันการคิดต้นทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="b71ca-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="b71ca-128">คุณยังสามารถเรียกใช้งานเรกคอร์ดต้นทุนสินค้าที่ค้างอยู่สำหรับสินค้าแต่ละรายการ โดยการคลิกปุ่ม **เปิดใช้งานราคาที่ค้างอยู่** ในหน้า **ราคาสินค้า** ได้</span><span class="sxs-lookup"><span data-stu-id="b71ca-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="b71ca-129">เพื่อป้องกันการบำรุงรักษาข้อมูลเพิ่มเติม ใช้หน้า **การตั้งค่าเวอร์ชันการคิดต้นทุน** เพื่อเปลี่ยนแฟล็กการบล็อคที่ถูกแนบอยู่ในเวอร์ชันการคิดต้นทุนที่สอง</span><span class="sxs-lookup"><span data-stu-id="b71ca-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="b71ca-130">นโยบายการบล็อคจะป้องกันการป้อนรายการของต้นทุนที่เปิดค้างไว้ใหม่และการเรียกใช้งานต้นทุนที่เปิดค้างไว้</span><span class="sxs-lookup"><span data-stu-id="b71ca-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>





