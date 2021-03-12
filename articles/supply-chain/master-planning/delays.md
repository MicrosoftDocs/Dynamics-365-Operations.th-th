---
title: ล่าช้า
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวันที่ที่ล่าช้าในการวางแผนหลัก วันที่ที่ล่าช้าเป็นวันครบกำหนดชำระจริงที่ได้รับธุรกรรมการ ถ้าวันเติมสินค้าแรกสุดที่การวางแผนหลักคำนวณ เป็นวันหลังจากวันที่ร้องขอ
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dcb11b3665c5d2f296f1ba2ce4708c4eff241b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977999"
---
# <a name="delays"></a><span data-ttu-id="9ee77-104">ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="9ee77-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ee77-105">หัวข้อนี้แสดงข้อมูลเกี่ยวกับวันที่ที่ล่าช้าในการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="9ee77-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="9ee77-106">วันที่ที่ล่าช้าเป็นวันครบกำหนดชำระจริงที่ได้รับธุรกรรมการ ถ้าวันเติมสินค้าแรกสุดที่การวางแผนหลักคำนวณ เป็นวันหลังจากวันที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="9ee77-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="9ee77-107">การวางแผนหลักสามารถคำนวณวันเติมสินค้าแรกสุดสำหรับธุรกรรม ขึ้นอยู่กับระยะเวลารอคอยสินค้า ความพร้อมของวัสดุ ความพร้อมใช้งานของกำลังการผลิต และพารามิเตอร์การวางแผนต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="9ee77-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="9ee77-108">ถ้าการวางแผนหลักคำนวณวันที่ใบสั่งที่อยู่ก่อนวันปัจจุบัน ใบสั่งไม่สามารถตอบสนองตามเวลาได้</span><span class="sxs-lookup"><span data-stu-id="9ee77-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="9ee77-109">ดังนั้น ใบสั่งมีความล่าช้า</span><span class="sxs-lookup"><span data-stu-id="9ee77-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="9ee77-110">ในกรณีนี้ การวางแผนหลักวางแผนการล่วงหน้าของใบสั่งจากวันปัจจุบัน และรวมระยะเวลารอคอยสินค้า</span><span class="sxs-lookup"><span data-stu-id="9ee77-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="9ee77-111">ระยะเวลารอคอยสินค้าเหล่านี้เริ่มต้นกับสินค้าส่วนประกอบระดับต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="9ee77-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="9ee77-112">ใบสั่งได้รับวันที่ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="9ee77-112">The order then receives a delayed date.</span></span> <span data-ttu-id="9ee77-113">วันล่าช้าคือวันครบกำหนดชำระจริง ตามข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="9ee77-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="9ee77-114">การวางแผนหลักคำนวณจำนวนวันที่ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="9ee77-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="9ee77-115">ในบางสถานการณ์ คุณอาจเลือกที่จะไม่คำนวณความล่าช้า เช่น เมื่อผู้ใช้ทราบว่าพวกเขาสามารถเร่งระยะเวลารอคอยสินค้า โดยการเลือกวิธีการจัดส่งอื่น</span><span class="sxs-lookup"><span data-stu-id="9ee77-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="9ee77-116">คุณสามารถกำหนดวิธีคำนวณความล่าช้าสำหรับกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="9ee77-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="9ee77-117">คุณสามารถแนบกลุ่มความครอบคลุมกับสินค้าในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="9ee77-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="9ee77-118">ในหน้า **พารามิเตอร์การวางแผนหลัก** คุณสามารถตั้งค่าเวลาเริ่มต้นสำหรับการคำนวณความล่าช้าได้</span><span class="sxs-lookup"><span data-stu-id="9ee77-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="9ee77-119">ถ้าใบสั่งซื้อถูกทำให้สมบูรณ์ภายหลัง ให้เพิ่มหนึ่งวันที่ล่าช้าเข้าไปในวันที่ล่าช้าของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="9ee77-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="9ee77-120">ในรุ่นก่อนหน้า ความล่าช้าที่คำนวณได้ถูกเรียกว่า *ข่าวสารในอนาคต* วันที่ที่ล่าช้าถูกเรียกว่า *วันที่ในอนาคต* และธุรกรรมที่ล่าช้าถูกอ้างอิงเป็น *ธุรกรรมที่มีการตั้งค่าในอนาคต*</span><span class="sxs-lookup"><span data-stu-id="9ee77-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="9ee77-121">ความล่าช้าที่จำกัดในการตั้งค่าการผลิตที่มีระดับ BOM หลายระดับ</span><span class="sxs-lookup"><span data-stu-id="9ee77-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="9ee77-122">เมื่อคุณทำงานกับความล่าช้าในการตั้งค่าการผลิตที่มีระดับ BOM หลายระดับ จำเป็นต้องทราบว่ามีเฉพาะสินค้าที่อยู่เหนือรายการโดยตรง (ในโครงสร้าง BOM) ซึ่งก่อให้เกิดการล่าช้าจะได้รับการอัพเดตด้วยความล่าช้าโดยเป็นส่วนหนึ่งของการรันการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="9ee77-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="9ee77-123">สินค้าอื่นๆ ในโครงสร้าง BOM จะไม่มีการหน่วงเวลาจนกว่าจะมีการรันการวางแผนหลักครั้งแรก เมื่อใบสั่งที่วางแผนไว้สำหรับระดับสูงสุดได้รับการอนุมัติหรือยืนยันแล้ว</span><span class="sxs-lookup"><span data-stu-id="9ee77-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="9ee77-124">เมื่อต้องการแก้ไขข้อจำกัดที่รู้จักนี้ ใบสั่งผลิตที่อยู่ด้านบนของโครงสร้าง BOM ที่มีความล่าช้าอาจได้รับการอนุมัติ (หรือยืนยัน) ก่อนที่จะรันการวางแผนหลักถัดไป</span><span class="sxs-lookup"><span data-stu-id="9ee77-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="9ee77-125">เมื่อเป็นเช่นนี้ความล่าช้าจากใบสั่งผลิตที่วางแผนไว้และได้รับการอนุมัติล่าช้าจะถูกเก็บไว้ และจะมีการอัพเดตส่วนประกอบพื้นฐานทั้งหมดตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="9ee77-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="9ee77-126">ข้อความการดำเนินการยังสามารถใช้เพื่อระบุใบสั่งที่วางแผนไว้ที่สามารถย้ายไปยังวันที่ในภายหลังได้ เนื่องจากความล่าช้าอื่นๆ ในโครงสร้าง BOM</span><span class="sxs-lookup"><span data-stu-id="9ee77-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="9ee77-127">วันที่ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9ee77-127">Desired date</span></span>

<span data-ttu-id="9ee77-128">ในหน้า **ใบสั่งที่วางแผน** ภายใต้แท็บ **ความล่าช้า** คือ **วันที่ที่ต้องการ** สำหรับใบสั่งที่วางแผน</span><span class="sxs-lookup"><span data-stu-id="9ee77-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="9ee77-129">วันที่ที่ต้องการของใบสั่งที่วางแผนคือ วันที่พื้นฐานสำหรับความล่าช้า ซึ่งเป็นวันที่ที่คำนวณซึ่งเท่ากับ **วันที่ที่ร้องขอ** ที่คำนวณจาก **ความต้องการสุทธิ**</span><span class="sxs-lookup"><span data-stu-id="9ee77-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="9ee77-130">ถ้าใบสั่งที่วางแผนคือรายการ BOM สายการผลิต หรือรายการคัมบัง วันที่ที่ต้องการเป็นไปตาม **วันที่ที่ต้องการ** และจะไม่แสดงวันที่ที่ต้องการในหน้า **ใบสั่งที่วางแผน**</span><span class="sxs-lookup"><span data-stu-id="9ee77-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9ee77-131">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9ee77-131">Additional resources</span></span>
--------

[<span data-ttu-id="9ee77-132">การตั้งค่าความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="9ee77-132">Coverage settings</span></span>](coverage-settings.md)
