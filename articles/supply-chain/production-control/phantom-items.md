---
title: สินค้าแฝง
description: หัวข้อนี้อธิบาย โดยละเอียด วิธีการที่จะสามารถใช้ชนิดรายการ Phantom สำหรับรายการของ bill of materials (BOM) และสูตรใน Dynamics 365 Supply Chain Management
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: dc69687b1dd94407b28209178e923fe5169bcdac
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211341"
---
# <a name="phantom-items"></a><span data-ttu-id="81cc5-103">สินค้าแฝง</span><span class="sxs-lookup"><span data-stu-id="81cc5-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81cc5-104">หัวข้อนี้อธิบายโดยละเอียด เกี่ยวกับวิธีที่ชนิดรายการ Phantom สามารถนำไปใช้สำหรับรายการของสูตรการผลิต (BOM) และสูตร</span><span class="sxs-lookup"><span data-stu-id="81cc5-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="81cc5-105">ในภาพประกอบต่อไปนี้ (a) คือ BOM สำหรับผลิตภัณฑ์ H และส่วน F และ G และ (b) คือแผ่นงานกระบวนการผลิตสำหรับผลิตภัณฑ์ H และส่วน F</span><span class="sxs-lookup"><span data-stu-id="81cc5-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![ผลิตภัณฑ์ H และส่วน F](media/product-H-part-F.png)


<span data-ttu-id="81cc5-107">ภาพนี้แสดงตัวอย่างของโครงสร้าง BOM ในสองระดับ</span><span class="sxs-lookup"><span data-stu-id="81cc5-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="81cc5-108">ผลิตภัณฑ์สำเร็จรูป H แสดงถึงผลิตภัณฑ์สำหรับแอสเซมบลีของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="81cc5-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="81cc5-109">แอสเซมบลีของเครื่องประกอบด้วยสองส่วน หน่วยทางไฟฟ้า (F) ที่มีวัสดุสองรายการ (A และ B) และกลุ่มของบรรจุภัณฑ์ (G) ที่มีวัสดุสองรายการ (C และ D) เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="81cc5-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="81cc5-110">มีการใช้วัสดุอื่น (E) ระหว่างแอสเซมบลีทั่วไปของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="81cc5-110">Another material (E) is used during the general assembly of the machine.</span></span>

![ผลิตภัณฑ์ H และส่วน F](media/product-H-part-B.png)

<span data-ttu-id="81cc5-112">ตัวอย่างก่อนหน้านี้แสดงถึง BOM วิศวกรรมสำหรับผลิตภัณฑ์ H โครงสร้างนี้ให้ภาพรวมที่ดีของส่วนและคอมโพเนนต์ของแอสเซมบลีของเครื่องโดยรวม</span><span class="sxs-lookup"><span data-stu-id="81cc5-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="81cc5-113">อย่างไรก็ตาม ถึงแม้ว่าตัวออกแบบผลิตภัณฑ์อาจต้องการเห็น BOM ที่แสดงในวิธีนี้ โครงสร้างนี้อาจไม่ได้แสดงถึงวิธีการที่เครื่องถูกสร้างในการควบคุมการผลิตอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="81cc5-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="81cc5-114">ตัวอย่างเช่น BOM วิศวกรรมในภาพก่อนหน้านี้บ่งชี้ว่า หน่วยทางไฟฟ้า F จะถูกประกอบเป็นส่วนที่แยกต่างหากในใบสั่งงานที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="81cc5-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="81cc5-115">อย่างไรก็ตาม ในการควบคุมการผลิต จึงอาจถูกพิจารณาว่ามีประสิทธิภาพมากขึ้นในการรวบรวมหน่วยทางไฟฟ้าเป็นส่วนหนึ่งของแอสเซมบลีของเครื่องโดยรวม ไม่ใช่เป็นใบสั่งงานที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="81cc5-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="81cc5-116">BOM วิศวกรรมนี้ยังบ่งชี้ด้วยว่า ส่วน G เป็นส่วนที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="81cc5-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="81cc5-117">อย่างไรก็ตาม ในโครงสร้างนี้ ส่วน G ไม่แสดงถึงส่วนประกอบทางกายภาพ แต่เป็นคอลเลกชันของบรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="81cc5-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="81cc5-118">ดังนั้น ถึงแม้ว่า BOM วิศวกรรมจะแสดงค่าที่มากสำหรับการออกแบบของผลิตภัณฑ์และการบำรุงรักษาของการออกแบบนั้น อาจไม่ใช่วิธีที่เป็นไปตามตรรกะที่สุดในการสนับสนุนกระบวนการการดำเนินการผลิตของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="81cc5-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="81cc5-119">ในทางกลับกัน BOM การผลิตแสดงถึงวิธีดีที่สุดสำหรับการสร้างผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="81cc5-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="81cc5-120">ภาพประกอบต่อไปนี้แสดงวิธีเปลี่ยน BOM วิศวกรรมก่อนหน้านี้เป็น BOM การผลิต</span><span class="sxs-lookup"><span data-stu-id="81cc5-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="81cc5-121">ในภาพประกอบนี้ (a) คือ BOM สำหรับผลิตภัณฑ์ H และ b เป็นแผ่นงานกระบวนการผลิตสำหรับผลิตภัณฑ์ H</span><span class="sxs-lookup"><span data-stu-id="81cc5-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="81cc5-122">ในโครงสร้างนี้ คุณสามารถดูได้ว่าไม่มีแนวคิดของส่วน F และ G และวัสดุที่ประกอบด้วยส่วนประกอบเหล่านี้มีการยกระดับเป็นระดับ BOM ถัดไป</span><span class="sxs-lookup"><span data-stu-id="81cc5-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="81cc5-123">ไม่เหมือนกับวิศวกรรม BOM ซึ่งมีแผ่นการดำเนินงานสองแผ่น BOM การผลิตมีแผ่นงานการดำเนินงานแผ่นเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="81cc5-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="81cc5-124">การดำเนินงานบรรจุภัณฑ์ที่มีการเชื่อมโยงกับส่วน G ยังได้ถูกยกระดับ และเป็นส่วนหนึ่งของแผ่นงานการดำเนินการสำหรับผลิตภัณฑ์ H ในขณะนี้ แอสเซมบลีของหน่วยทางไฟฟ้าเป็นการดำเนินงานแรก</span><span class="sxs-lookup"><span data-stu-id="81cc5-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="81cc5-125">ใบสั่งนี้เหมาะสม เนื่องจากหน่วยนี้ถูกใช้ในการดำเนินงานถัดไป ซึ่งเป็นแอสเซมบลีของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="81cc5-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="81cc5-126">การดำเนินงานสุดท้ายคือการดำเนินงานบรรจุภัณฑ์ ซึ่งใช้วัสดุบรรจุภัณฑ์สองรายการ (C และ D)</span><span class="sxs-lookup"><span data-stu-id="81cc5-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="81cc5-127">การเปลี่ยนระหว่าง Engineering BOM และ Manufacturing BOM ถูกเปิดใช้งานผ่านชนิดรายการ Phantom BOM</span><span class="sxs-lookup"><span data-stu-id="81cc5-127">The transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="81cc5-128">เมื่อคำว่า "แฝง" บ่งชี้ว่า ส่วน F และ G ได้หายไป ในขณะการเปลี่ยนระหว่างชนิด BOM สองชนิด</span><span class="sxs-lookup"><span data-stu-id="81cc5-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="81cc5-129">ในตัวอย่างนี้ ชนิดรายการ Phantom ถูกนำไปใช้กับรายการ BOM สำหรับส่วน F และ G ใน BOM วิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="81cc5-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="81cc5-130">เมื่อมีการสร้างการผลิตหรือใบสั่งชุดงาน จะมีการคัดลอก BOM วิศวกรรมไปยังการผลิตหรือใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="81cc5-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="81cc5-131">จากนั้น เมื่อมีการประเมินใบสั่ง การเปลี่ยนจาก BOM วิศวกรรมเป็น BOM การผลิตจะเกิดขึ้น ดังที่แสดงในภาพประกอบก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="81cc5-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="81cc5-132">จากแผ่นงานการดำเนินงานในแผนภาพที่สอง บรรจุภัณฑ์ C และ D เป็นข้อมูลป้อนเข้าสำหรับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="81cc5-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="81cc5-133">โครงสร้าง phantom BOM แบบหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="81cc5-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="81cc5-134">คุณสามารถใช้ชนิดรายการ Phantom ในโครงสร้าง BOM แบบหลายระดับ ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="81cc5-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="81cc5-135">ในภาพประกอบนี้ (a) คือ BOM สำหรับผลิตภัณฑ์ G และ (b) คือแผ่นงานกระบวนการผลิตสำหรับส่วน E และ F และผลิตภัณฑ์ G</span><span class="sxs-lookup"><span data-stu-id="81cc5-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![ผลิตภัณฑ์ G และส่วน F ที่มีแผ่นงานในกระบวนการผลิต](media/product-G-route-sheet-G.png)


<span data-ttu-id="81cc5-137">ภาพประกอบต่อไปนี้แสดง BOM การผลิตที่เป็นผลลัพธ์และแผ่นงานกระบวนการผลิต ถ้ารายการ BOM สำหรับส่วน E และ F ถูกตั้งค่าคอนฟิกเพื่อให้ชนิดของรายการเป็น Phantom</span><span class="sxs-lookup"><span data-stu-id="81cc5-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="81cc5-138">ในภาพประกอบนี้ (a) คือ BOM สำหรับผลิตภัณฑ์ G และ (b) เป็นแผ่นงานกระบวนการผลิตสำหรับผลิตภัณฑ์ G</span><span class="sxs-lookup"><span data-stu-id="81cc5-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![ผลิตภัณฑ์ G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="81cc5-140">เครือข่าย phantom และกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="81cc5-140">Phantom and route network</span></span>
<span data-ttu-id="81cc5-141">Phantom BOMs ยังสามารถใช้ได้สำหรับ BOM ที่มีเครือข่ายกระบวนการผลิตด้วย</span><span class="sxs-lookup"><span data-stu-id="81cc5-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="81cc5-142">ในเครือข่ายของกระบวนการผลิต การดำเนินการอย่างน้อยหนึ่งอย่างจะรันพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="81cc5-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="81cc5-143">ภาพประกอบต่อไปนี้แสดงตัวอย่างของเครือข่ายกระบวนการผลิตที่ใช้ใน BOM แบบหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="81cc5-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="81cc5-144">ในภาพประกอบนี้ (a) คือ BOM สำหรับผลิตภัณฑ์ G และส่วน F และ G และ (b) คือแผ่นงานกระบวนการผลิตสำหรับผลิตภัณฑ์ G และส่วน F ซึ่งมีเครือข่ายกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="81cc5-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![ผลิตภัณฑ์ G และส่วน F](media/product-G-part-F.png)


<span data-ttu-id="81cc5-146">ในภาพประกอบต่อไปนี้ (a) คือ BOM สำหรับผลิตภัณฑ์ G และส่วน F และ G และ (b) คือแผ่นงานกระบวนการผลิตสำหรับผลิตภัณฑ์ G และส่วน F</span><span class="sxs-lookup"><span data-stu-id="81cc5-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![ผลิตภัณฑ์ G และส่วน F ที่มีแผ่นงานในกระบวนการผลิต](media/product-G-part-F-with-route-sheet.png)
