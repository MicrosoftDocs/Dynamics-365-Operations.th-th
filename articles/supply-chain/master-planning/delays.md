---
title: ล่าช้า
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวันที่ที่ล่าช้าในการวางแผนหลัก วันที่ที่ล่าช้าเป็นวันครบกำหนดชำระจริงที่ได้รับธุรกรรมการ ถ้าวันเติมสินค้าแรกสุดที่การวางแผนหลักคำนวณ เป็นวันหลังจากวันที่ร้องขอ
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/20/2019
ms.locfileid: "878321"
---
# <a name="delays"></a><span data-ttu-id="d2a32-104">ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="d2a32-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2a32-105">หัวข้อนี้แสดงข้อมูลเกี่ยวกับวันที่ที่ล่าช้าในการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="d2a32-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="d2a32-106">วันที่ที่ล่าช้าเป็นวันครบกำหนดชำระจริงที่ได้รับธุรกรรมการ ถ้าวันเติมสินค้าแรกสุดที่การวางแผนหลักคำนวณ เป็นวันหลังจากวันที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="d2a32-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="d2a32-107">การวางแผนหลักสามารถคำนวณวันเติมสินค้าแรกสุดสำหรับธุรกรรม ขึ้นอยู่กับระยะเวลารอคอยสินค้า ความพร้อมของวัสดุ ความพร้อมใช้งานของกำลังการผลิต และพารามิเตอร์การวางแผนต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="d2a32-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="d2a32-108">ถ้าการวางแผนหลักคำนวณวันที่ใบสั่งที่อยู่ก่อนวันปัจจุบัน ใบสั่งไม่สามารถตอบสนองตามเวลาได้</span><span class="sxs-lookup"><span data-stu-id="d2a32-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="d2a32-109">ดังนั้น ใบสั่งมีความล่าช้า</span><span class="sxs-lookup"><span data-stu-id="d2a32-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="d2a32-110">ในกรณีนี้ การวางแผนหลักวางแผนการล่วงหน้าของใบสั่งจากวันปัจจุบัน และรวมระยะเวลารอคอยสินค้า</span><span class="sxs-lookup"><span data-stu-id="d2a32-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="d2a32-111">ระยะเวลารอคอยสินค้าเหล่านี้เริ่มต้นกับสินค้าส่วนประกอบระดับต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="d2a32-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="d2a32-112">ใบสั่งได้รับวันที่ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="d2a32-112">The order then receives a delayed date.</span></span> <span data-ttu-id="d2a32-113">วันล่าช้าคือวันครบกำหนดชำระจริง ตามข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d2a32-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="d2a32-114">การวางแผนหลักคำนวณจำนวนวันที่ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="d2a32-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="d2a32-115">ในบางสถานการณ์ คุณอาจเลือกที่จะไม่คำนวณความล่าช้า เช่น เมื่อผู้ใช้ทราบว่าพวกเขาสามารถเร่งระยะเวลารอคอยสินค้า โดยการเลือกวิธีการจัดส่งอื่น</span><span class="sxs-lookup"><span data-stu-id="d2a32-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="d2a32-116">คุณสามารถกำหนดวิธีคำนวณความล่าช้าสำหรับกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="d2a32-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="d2a32-117">คุณสามารถแนบกลุ่มความครอบคลุมกับสินค้าในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="d2a32-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="d2a32-118">ในหน้า **พารามิเตอร์การวางแผนหลัก** คุณสามารถตั้งค่าเวลาเริ่มต้นสำหรับการคำนวณความล่าช้าได้</span><span class="sxs-lookup"><span data-stu-id="d2a32-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="d2a32-119">ถ้าใบสั่งซื้อถูกทำให้สมบูรณ์ภายหลัง ให้เพิ่มหนึ่งวันที่ล่าช้าเข้าไปในวันที่ล่าช้าของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="d2a32-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> <span data-ttu-id="d2a32-120">[!หมายเหตุ} ในรุ่นก่อนหน้า ความล่าช้าที่คำนวณได้ถูกเรียกว่า *ข่าวสารในอนาคต* วันที่ที่ล่าช้าถูกเรียกว่า *วันที่ในอนาคต* และธุรกรรมล่าช้าถูกอ้างอิงเป็น *ธุรกรรมที่มีการตั้งค่าในอนาคต*</span><span class="sxs-lookup"><span data-stu-id="d2a32-120">[!NOTE} In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="desired-date"></a><span data-ttu-id="d2a32-121">วันที่ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d2a32-121">Desired date</span></span>

<span data-ttu-id="d2a32-122">ในหน้า **ใบสั่งที่วางแผน** ภายใต้แท็บ **ความล่าช้า** คือ **วันที่ที่ต้องการ** สำหรับใบสั่งที่วางแผน</span><span class="sxs-lookup"><span data-stu-id="d2a32-122">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="d2a32-123">วันที่ที่ต้องการของใบสั่งที่วางแผนคือ วันที่พื้นฐานสำหรับความล่าช้า ซึ่งเป็นวันที่ที่คำนวณซึ่งเท่ากับ **วันที่ที่ร้องขอ** ที่คำนวณจาก **ความต้องการสุทธิ**</span><span class="sxs-lookup"><span data-stu-id="d2a32-123">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="d2a32-124">ถ้าใบสั่งที่วางแผนคือรายการ BOM สายการผลิต หรือรายการคัมบัง วันที่ที่ต้องการเป็นไปตาม **วันที่ที่ต้องการ** และจะไม่แสดงวันที่ที่ต้องการในหน้า **ใบสั่งที่วางแผน**</span><span class="sxs-lookup"><span data-stu-id="d2a32-124">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="d2a32-125">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d2a32-125">Additional resources</span></span>
--------

[<span data-ttu-id="d2a32-126">การตั้งค่าความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="d2a32-126">Coverage settings</span></span>](coverage-settings.md)
