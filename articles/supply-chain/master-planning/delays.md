---
title: "ล่าช้า"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับวันที่ล่าช้าในการวางแผนหลัก วันที่ที่ล่าช้าเป็นวันครบกำหนดชำระจริงที่ได้รับธุรกรรมการ ถ้าวันเติมสินค้าแรกสุดที่การวางแผนหลักคำนวณ เป็นวันหลังจากวันที่ร้องขอ"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fed78a7eba16d286a81b1e9ad709142422298c91
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="delays"></a><span data-ttu-id="46110-104">ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="46110-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46110-105">บทความนี้แสดงข้อมูลเกี่ยวกับวันที่ล่าช้าในการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="46110-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="46110-106">วันที่ที่ล่าช้าเป็นวันครบกำหนดชำระจริงที่ได้รับธุรกรรมการ ถ้าวันเติมสินค้าแรกสุดที่การวางแผนหลักคำนวณ เป็นวันหลังจากวันที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="46110-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="46110-107">การวางแผนหลักสามารถคำนวณวันเติมสินค้าแรกสุดสำหรับธุรกรรม ขึ้นอยู่กับระยะเวลารอคอยสินค้า ความพร้อมของวัสดุ ความพร้อมใช้งานของกำลังการผลิต และพารามิเตอร์การวางแผนต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="46110-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="46110-108">ถ้าการวางแผนหลักคำนวณวันที่ใบสั่งที่อยู่ก่อนวันปัจจุบัน ใบสั่งไม่สามารถตอบสนองตามเวลาได้</span><span class="sxs-lookup"><span data-stu-id="46110-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="46110-109">ดังนั้น ใบสั่งมีความล่าช้า</span><span class="sxs-lookup"><span data-stu-id="46110-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="46110-110">ในกรณีนี้ การวางแผนหลักวางแผนการล่วงหน้าของใบสั่งจากวันปัจจุบัน และรวมระยะเวลารอคอยสินค้า</span><span class="sxs-lookup"><span data-stu-id="46110-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="46110-111">ระยะเวลารอคอยสินค้าเหล่านี้เริ่มต้นกับสินค้าส่วนประกอบระดับต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="46110-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="46110-112">ใบสั่งได้รับวันที่ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="46110-112">The order then receives a delayed date.</span></span> <span data-ttu-id="46110-113">วันล่าช้าคือวันครบกำหนดชำระจริง ตามข้อมูลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="46110-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="46110-114">การวางแผนหลักคำนวณจำนวนวันที่ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="46110-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="46110-115">ในบางสถานการณ์ คุณอาจเลือกที่จะไม่คำนวณความล่าช้า เช่น เมื่อผู้ใช้ทราบว่าพวกเขาสามารถเร่งระยะเวลารอคอยสินค้า โดยการเลือกวิธีการจัดส่งอื่น</span><span class="sxs-lookup"><span data-stu-id="46110-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="46110-116">คุณสามารถกำหนดวิธีคำนวณความล่าช้าสำหรับกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="46110-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="46110-117">คุณสามารถแนบกลุ่มความครอบคลุมกับสินค้าในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="46110-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="46110-118">ในหน้า **พารามิเตอร์การวางแผนหลัก** คุณสามารถตั้งค่าเวลาเริ่มต้นสำหรับการคำนวณความล่าช้าได้</span><span class="sxs-lookup"><span data-stu-id="46110-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="46110-119">ถ้าใบสั่งซื้อถูกทำให้สมบูรณ์ภายหลัง ให้เพิ่มหนึ่งวันที่ล่าช้าเข้าไปในวันที่ล่าช้าของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="46110-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="46110-120">**หมายเหตุ:** ในรุ่นก่อนหน้า ความล่าช้าที่คำนวณได้ถูกเรียกว่า *ข่าวสารในอนาคต*วันล่าช้าที่เรียกว่า *วันในอนาคต*และธุรกรรมล่าช้าที่เรียกว่า *ธุรกรรมที่มีการตั้งค่าในอนาคต*</span><span class="sxs-lookup"><span data-stu-id="46110-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="additional-resources"></a><span data-ttu-id="46110-121">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="46110-121">Additional resources</span></span>
--------

[<span data-ttu-id="46110-122">การตั้งค่าความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="46110-122">Coverage settings</span></span>](coverage-settings.md)




