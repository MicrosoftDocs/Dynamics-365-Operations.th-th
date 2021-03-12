---
title: อนุมัติแผนการใบสั่ง
description: หัวข้อนี้จะอธิบายการอนุมัติแผนการใบสั่งที่ได้รับการสนับสนุนในการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c29ede7ad8916a97b4a04b68f41961f79810e0c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983580"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="c77eb-103">อนุมัติแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="c77eb-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c77eb-104">หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการอัปเดตสถานะของแผนการใบสั่งในการเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="c77eb-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="c77eb-105">โปรดทราบว่าการอนุมัติแผนการใบสั่งเป็นขั้นตอนที่เลือกได้ในวิธีการสร้างใบสั่งที่ยืนยันจากแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="c77eb-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="c77eb-106">ขอแนะนำให้อนุมัติแผนการใบสั่งที่ปรับเปลี่ยน มิฉะนั้นการแก้ไขจะถูกละเว้นและเขียนทับโดยการเรียกใช้การวางแผนครั้งถัดไป</span><span class="sxs-lookup"><span data-stu-id="c77eb-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![ลำดับของแผนการใบสั่ง](media/approved-planned-orders-1.png)

<span data-ttu-id="c77eb-108">ฟิลด์ **สถานะ** ช่วยให้คุณสามารถติดตามความคืบหน้าโดยใช้ค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c77eb-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="c77eb-109">**ยังไม่ได้ดำเนินการ:** เมื่อการวางแผนหลักสร้างแผนการใบสั่ง แผนการใบสั่งมีสถานะเป็น *ยังไม่ได้ดำเนินการ*</span><span class="sxs-lookup"><span data-stu-id="c77eb-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="c77eb-110">แผนการใบสั่งที่มีสถานะนี้จะถูกลบในระหว่างการเรียกใช้การวางแผนครั้งถัดไป</span><span class="sxs-lookup"><span data-stu-id="c77eb-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="c77eb-111">**เสร็จสมบูรณ์:** ถ้าคุณตัดสินใจที่จะไม่ยืนยันแผนการใบสั่ง คุณสามารถเปลี่ยนสถานะเป็น *เสร็จสมบูรณ์* เพื่อระบุว่าคุณจะประเมินแผนการใบสั่งนี้เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="c77eb-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="c77eb-112">โปรดทราบว่าระบบมีการจัดการกับสถานะ *ยังไม่ได้ดำเนินการ* และ *เสร็จสมบูรณ์* แบบเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c77eb-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="c77eb-113">**อนุมัติแล้ว:** ถ้าคุณต้องการรักษาการแก้ไขหรือการวางแผนเพื่อยืนยันแผนการใบสั่ง ให้เปลี่ยนสถานะเป็น *อนุมัติแล้ว*</span><span class="sxs-lookup"><span data-stu-id="c77eb-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="c77eb-114">แผนการใบสั่งที่มีสถานะ *อนุมัติแล้ว* ได้รับการพิจารณามีการกำหนดแบบคงที่และตามที่คาดไว้โดยการวางแผนหลัก ดังนั้นจึงไม่สามารถแก้ไขหรือลบออกได้ระหว่างการวางแผนหลักภายหลังทำงาน</span><span class="sxs-lookup"><span data-stu-id="c77eb-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="c77eb-115">ถ้าต้องการทำให้สำเร็จตามนั้น ตรรกะการวางแผนคัดลอกแผนการใบสั่ง *ที่อนุมัติแล้ว* จากรุ่นแผนเก่าไปยังรุ่นแผนใหม่ในระหว่างการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="c77eb-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="c77eb-116">โปรดทราบแผนการใบสั่งที่ *อนุมัติแล้ว* จะถือเป็นการกำหนดภายในแผนหลักเฉพาะเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c77eb-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="c77eb-117">คุณสามารถจัดการแผนการใบสั่งจากพื้นที่ทำงาน **การวางแผนหลัก** รายการ **แผนการใบสั่ง** หรือ **แผนการใบสั่งผลิต**, **แผนการใบสั่งซื้อ** และรายการ **แผนการโอนย้าย**</span><span class="sxs-lookup"><span data-stu-id="c77eb-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>
