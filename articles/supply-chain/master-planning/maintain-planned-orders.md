---
title: รักษาแผนการใบสั่ง
description: หัวข้อนี้จะแสดงข้อมูลเกี่ยวกับวิธีการจัดการใบสั่งที่วางแผนไว้ โดยอธิบายวิธีการปรับปรุงสถานะของแผนการใบสั่ง ยืนยัน และกรองข้อมูลสำหรับแผนการใบสั่งที่มีสถานะเดียวกันเป็นแผนการใบสั่งที่เลือก
author: roxanadiaconu
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bccb632255eac975dc150cf322d4c579ff2f24
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813787"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="ca38f-104">รักษาแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca38f-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca38f-105">หัวข้อนี้จะแสดงข้อมูลเกี่ยวกับวิธีการจัดการใบสั่งที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="ca38f-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="ca38f-106">โดยอธิบายวิธีการปรับปรุงสถานะของแผนการใบสั่ง ยืนยัน และกรองข้อมูลสำหรับแผนการใบสั่งที่มีสถานะเดียวกันเป็นแผนการใบสั่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ca38f-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="ca38f-107">คุณสามารถจัดการแผนการใบสั่งจากพื้นที่ทำงาน **การวางแผนหลัก** รายการ **แผนการใบสั่ง** หรือ **แผนการใบสั่งผลิต**, **แผนการใบสั่งซื้อ**และรายการ **แผนการโอนย้าย**</span><span class="sxs-lookup"><span data-stu-id="ca38f-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="ca38f-108">สถานะของแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca38f-108">Planned order status</span></span>
<span data-ttu-id="ca38f-109">คุณสามารถใช้ฟิลด์ **สถานะ** เพื่อช่วยติดตามความคืบหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="ca38f-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="ca38f-110">ใช้ค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ca38f-110">The following values are used:</span></span>

-   <span data-ttu-id="ca38f-111">เมื่อการวางแผนหลักสร้างแผนการใบสั่ง แผนการใบสั่งมีสถานะเป็น **ยังไม่ได้ดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="ca38f-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="ca38f-112">ถ้าคุณเลือกที่จะไม่ยืนยันแผนการใบสั่ง คุณสามารถกำหนดสถานะให้กับแผนการใบสั่งนั้นเป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="ca38f-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="ca38f-113">ถ้าคุณต้องการที่จะยืนยันแผนการใบสั่ง คุณสามารถเปลี่ยนสถานะเป็น **อนุมัติแล้ว**</span><span class="sxs-lookup"><span data-stu-id="ca38f-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="ca38f-114">แผนการใบสั่งที่มีสถานะ **อนุมัติแล้ว** จะได้รับการยอมรับจากการวางแผนหลัก ดังนั้นจึงไม่สามารถแก้ไขหรือลบออกได้ระหว่างการวางแผนหลักภายหลังทำงาน</span><span class="sxs-lookup"><span data-stu-id="ca38f-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="ca38f-115">การยืนยันแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ca38f-115">Firming planned orders</span></span> 
<span data-ttu-id="ca38f-116">โดยการยืนยันแผนการใบสั่ง จะมีการสร้างใบสั่งจริง</span><span class="sxs-lookup"><span data-stu-id="ca38f-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="ca38f-117">สิ่งเหล่านี้ยังสามารถเรียกได้ว่า *นำออกใช้* หรือ *ใบสั่งที่เปิด*</span><span class="sxs-lookup"><span data-stu-id="ca38f-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="ca38f-118">เมื่อมียืนยันแผนการใบสั่ง แผนการใบสั่งจะถูกย้ายไปยังส่วนของใบสั่งของโมดูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ca38f-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="ca38f-119">คุณสามารถเลือกตัวเลือกการยืนยันตัวสองตัวเลือกจากหน้า **แผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="ca38f-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="ca38f-120">**ยืนยัน** – ซึ่งจะยืนยันหนึ่งหรือหลายแผนการใบสั่งที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="ca38f-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="ca38f-121">**ยืนยันทั้งหมด** – ซึ่งจะยืนยันแผนการใบสั่งทั้งหมดในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="ca38f-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="ca38f-122">การใช้ **ยืนยันทั้งหมด** คุณไม่จำเป็นต้องเลือกแผนการใบสั่ง จะมีการยืนยันแผนการใบสั่งทั้งหมดภายในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="ca38f-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="ca38f-123">ตัวเลือกนี้จะมีประโยชน์ถ้าคุณยืนยันแผนการใบสั่งจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="ca38f-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="ca38f-124">คุณสามารถติดตามแผนการใบสั่งที่ยืนยันจาก **ประวัติการยืนยัน** ภายใต้ **แบบฟอร์มแผนการใบสั่ง > ดู > ประวัติการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="ca38f-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="ca38f-125">การยืนยันแบบพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="ca38f-125">Parallelize firming</span></span>
<span data-ttu-id="ca38f-126">ถ้าคุณกำลังวางแผนที่จะยืนยันใบสั่งหลายใบในเวลาเดียวกัน การรันกำหนดการทำงานแบบขนานอาจปรับปรุงเวลาที่ใช้ในการผลิตหรือประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="ca38f-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="ca38f-127">ตัวเลือกนี้จะพร้อมใช้งานเมื่อยืนยันหลายแผนการใบสั่งด้วย **ยืนยัน** หรือ **ยืนยันทั้งหมด** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ca38f-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="ca38f-128">พารามิเตอร์ที่พร้อมใช้งานมีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ca38f-128">The following parameters are available:</span></span>

-   <span data-ttu-id="ca38f-129">**การยืนยันกำหนดการทำงานแบบขนาน** – ถ้า **ใช่** กระบวนการยืนยันจะถูกกำหนดการทำงานแบบขนานด้วยจำนวนเธรดที่กำหนดไว้ใน **จำนวนของเธรด**</span><span class="sxs-lookup"><span data-stu-id="ca38f-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="ca38f-130">**จำนวนของเธรด** –ควบคุมจำนวนเธรดที่ใช้ในการกำหนดการทำงานแบบขนานกระบวนการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="ca38f-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="ca38f-131">พารามิเตอร์จะแสดงเฉพาะเมื่อ **การยืนยันกำหนดการทำงานแบบขนาน** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ca38f-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="ca38f-132">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ca38f-132">Additional resources</span></span>
--------

[<span data-ttu-id="ca38f-133">ภาพรวมของแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="ca38f-133">Master plans overview</span></span>](master-plans.md)



