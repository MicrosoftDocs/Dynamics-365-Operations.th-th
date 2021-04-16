---
title: รักษาแผนการใบสั่ง
description: หัวข้อนี้จะแสดงข้อมูลเกี่ยวกับวิธีการจัดการใบสั่งที่วางแผนไว้ โดยอธิบายวิธีการปรับปรุงสถานะของแผนการใบสั่ง ยืนยัน และกรองข้อมูลสำหรับแผนการใบสั่งที่มีสถานะเดียวกันเป็นแผนการใบสั่งที่เลือก
author: roxanadiaconu
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f97dc4627f9bb3a0ac2020b966de7e58aafcedc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833676"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="5c7a7-104">รักษาแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="5c7a7-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c7a7-105">หัวข้อนี้จะแสดงข้อมูลเกี่ยวกับวิธีการจัดการใบสั่งที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="5c7a7-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="5c7a7-106">โดยอธิบายวิธีการปรับปรุงสถานะของแผนการใบสั่ง ยืนยัน และกรองข้อมูลสำหรับแผนการใบสั่งที่มีสถานะเดียวกันเป็นแผนการใบสั่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5c7a7-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="5c7a7-107">คุณสามารถจัดการแผนการใบสั่งจากพื้นที่ทำงาน **การวางแผนหลัก** รายการ **แผนการใบสั่ง** หรือ **แผนการใบสั่งผลิต**, **แผนการใบสั่งซื้อ** และรายการ **แผนการโอนย้าย**</span><span class="sxs-lookup"><span data-stu-id="5c7a7-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="5c7a7-108">สถานะของแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="5c7a7-108">Planned order status</span></span>
<span data-ttu-id="5c7a7-109">คุณสามารถใช้ฟิลด์ **สถานะ** เพื่อช่วยติดตามความคืบหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="5c7a7-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="5c7a7-110">ใช้ค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5c7a7-110">The following values are used:</span></span>

-   <span data-ttu-id="5c7a7-111">เมื่อการวางแผนหลักสร้างแผนการใบสั่ง แผนการใบสั่งมีสถานะเป็น **ยังไม่ได้ดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="5c7a7-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="5c7a7-112">ถ้าคุณเลือกที่จะไม่ยืนยันแผนการใบสั่ง คุณสามารถกำหนดสถานะให้กับแผนการใบสั่งนั้นเป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="5c7a7-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="5c7a7-113">ถ้าคุณต้องการที่จะยืนยันแผนการใบสั่ง คุณสามารถเปลี่ยนสถานะเป็น **อนุมัติแล้ว**</span><span class="sxs-lookup"><span data-stu-id="5c7a7-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="5c7a7-114">แผนการใบสั่งที่มีสถานะ **อนุมัติแล้ว** จะได้รับการยอมรับจากการวางแผนหลัก ดังนั้นจึงไม่สามารถแก้ไขหรือลบออกได้ระหว่างการวางแผนหลักภายหลังทำงาน</span><span class="sxs-lookup"><span data-stu-id="5c7a7-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="5c7a7-115">ถ้าต้องการทำให้สำเร็จตามนั้น ตรรกะการวางแผนคัดลอกแผนการใบสั่ง **ที่อนุมัติแล้ว** จากรุ่นแผนเก่าไปยังรุ่นแผนใหม่ในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="5c7a7-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="5c7a7-116">การยืนยันแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="5c7a7-116">Firming planned orders</span></span> 
<span data-ttu-id="5c7a7-117">โดยการยืนยันแผนการใบสั่ง จะมีการสร้างใบสั่งจริง</span><span class="sxs-lookup"><span data-stu-id="5c7a7-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="5c7a7-118">รายการเหล่านี้ยังสามารถเรียกได้ว่า *ถูกนำออกใช้* หรือ *ใบสั่งที่เปิด*</span><span class="sxs-lookup"><span data-stu-id="5c7a7-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="5c7a7-119">เมื่อมียืนยันแผนการใบสั่ง แผนการใบสั่งจะถูกย้ายไปยังส่วนของใบสั่งของโมดูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="5c7a7-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="5c7a7-120">คุณสามารถเลือกตัวเลือกการยืนยันตัวสองตัวเลือกจากหน้า **แผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="5c7a7-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="5c7a7-121">**ยืนยัน** – ซึ่งจะยืนยันหนึ่งหรือหลายแผนการใบสั่งที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="5c7a7-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="5c7a7-122">**ยืนยันทั้งหมด** – ซึ่งจะยืนยันแผนการใบสั่งทั้งหมดในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="5c7a7-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="5c7a7-123">การใช้ **ยืนยันทั้งหมด** คุณไม่จำเป็นต้องเลือกแผนการใบสั่ง จะมีการยืนยันแผนการใบสั่งทั้งหมดภายในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="5c7a7-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="5c7a7-124">ตัวเลือกนี้จะมีประโยชน์ถ้าคุณยืนยันแผนการใบสั่งจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="5c7a7-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="5c7a7-125">คุณสามารถติดตามแผนการใบสั่งที่ยืนยันจาก **ประวัติการยืนยัน** ภายใต้ **แบบฟอร์มแผนการใบสั่ง > ดู > ประวัติการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="5c7a7-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="5c7a7-126">การยืนยันแบบพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="5c7a7-126">Parallelize firming</span></span>
<span data-ttu-id="5c7a7-127">ถ้าคุณกำลังวางแผนที่จะยืนยันใบสั่งหลายใบในเวลาเดียวกัน การรันกำหนดการทำงานแบบขนานอาจปรับปรุงเวลาที่ใช้ในการผลิตหรือประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="5c7a7-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="5c7a7-128">ตัวเลือกนี้จะพร้อมใช้งานเมื่อยืนยันหลายแผนการใบสั่งด้วย **ยืนยัน** หรือ **ยืนยันทั้งหมด** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5c7a7-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="5c7a7-129">พารามิเตอร์ที่พร้อมใช้งานมีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5c7a7-129">The following parameters are available:</span></span>

-   <span data-ttu-id="5c7a7-130">**การยืนยันกำหนดการทำงานแบบขนาน** – ถ้า **ใช่** กระบวนการยืนยันจะถูกกำหนดการทำงานแบบขนานด้วยจำนวนเธรดที่กำหนดไว้ใน **จำนวนของเธรด**</span><span class="sxs-lookup"><span data-stu-id="5c7a7-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="5c7a7-131">**จำนวนของเธรด** –ควบคุมจำนวนเธรดที่ใช้ในการกำหนดการทำงานแบบขนานกระบวนการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="5c7a7-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="5c7a7-132">พารามิเตอร์จะแสดงเฉพาะเมื่อ **การยืนยันกำหนดการทำงานแบบขนาน** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="5c7a7-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="5c7a7-133">ตัวเลือกสำหรับ **การยืนยันแบบพร้อมกัน** จะแสดงเฉพาะเมื่อคุณมีใบสั่งที่วางแผนไว้มากกว่าหนึ่งรายการที่ถูกเลือกสำหรับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="5c7a7-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="5c7a7-134">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5c7a7-134">Additional resources</span></span>
--------

[<span data-ttu-id="5c7a7-135">ภาพรวมของแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="5c7a7-135">Master plans overview</span></span>](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]