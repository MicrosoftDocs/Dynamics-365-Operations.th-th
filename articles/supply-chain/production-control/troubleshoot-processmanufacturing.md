---
title: แก้ไขปัญหาการผลิตแบบกระบวนการ
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับการผลิตแบบกระบวนการ
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966191"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="5d7a5-103">แก้ไขปัญหาการผลิตแบบกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="5d7a5-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="5d7a5-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับการผลิตแบบกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="5d7a5-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="5d7a5-105">เมื่อฉันใช้อุปกรณ์บัตรงานเพื่อรายงานปริมาณบางส่วนของงานล่าสุดในใบสั่งผลิต งานก่อนหน้านี้ทั้งหมดในใบสั่งนั้นที่มีสถานะกำลังดำเนินการจะสิ้นสุดลงโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="5d7a5-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="5d7a5-106">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="5d7a5-106">This behavior is by design.</span></span> <span data-ttu-id="5d7a5-107">บนหน้า **ใบสั่งผลิตเริ่มต้น** บนแท็บ **รายงานเมื่อเสร็จสมบูรณ์** จะมีตัวเลือกที่มีชื่อว่า **เครื่องหมายสิ้นสุดกระบวนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="5d7a5-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="5d7a5-108">ถ้ามีการตั้งค่าหัวข้อนี้เป็น *ใช่* สมุดรายวันบัตรกระบวนการผลิตมีการลงรายการบัญชีเมื่อผู้ปฏิบัติงานใช้อุปกรณ์ของบัตรงานหรือเทอร์มินัลบัตรงานเพื่อรายงานการดำเนินงานครั้งล่าสุด</span><span class="sxs-lookup"><span data-stu-id="5d7a5-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="5d7a5-109">สมุดรายวันนี้ทำเครื่องหมายการดำเนินงานทั้งหมดเป็นเสร็จสมบูรณ์แล้ว และสิ้นสุดงานการผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5d7a5-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="5d7a5-110">เมื่อตัวเลือก **เครื่องหมายสิ้นสุดกระบวนการผลิต** มีการตั้งค่าเป็น *ใช่* ระบบจะไม่พิจารณาสถานะของงานที่ผู้ปฏิบัติงานเลือกไว้เมื่อมีการรายงานการดำเนินงานครั้งล่าสุด</span><span class="sxs-lookup"><span data-stu-id="5d7a5-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="5d7a5-111">ระบบยังไม่พิจารณาว่าผู้ปฏิบัติงานมีการรายงานปริมาณทั้งหมดหรือบางส่วน</span><span class="sxs-lookup"><span data-stu-id="5d7a5-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="5d7a5-112">เมื่อมีการปิดบัญชีสินค้าคงคลัง ฉันจะได้รับข้อความเตือนต่อไปนี้: "ไม่มีการดำเนินการคำนวณการคิดต้นทุนแบบย้อนกลับที่มีวันที่ %1 สิ้นสุดรอบระยะเวลาที่ตรงกันแล้ว"</span><span class="sxs-lookup"><span data-stu-id="5d7a5-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="5d7a5-113">ในการนำออกใช้ก่อนรุ่น 10.0.13 ถ้าคุณไม่ได้ใช้โฟลว์การคิดต้นทุนการผลิตแบบ lean คุณจะได้รับข้อความเตือนที่ผิดพลาดต่อไปนี้ระหว่างการปิดบัญชีสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="5d7a5-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="5d7a5-114">คุณกำลังจะดำเนินการปิดบัญชีสินค้าคงคลังที่มีวันที่ %1</span><span class="sxs-lookup"><span data-stu-id="5d7a5-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="5d7a5-115">ไม่มีการดำเนินการคำนวณการคิดต้นทุนแบบย้อนกลับที่มีวันที่ %1 สิ้นสุดรอบระยะเวลาที่ตรงกันแล้ว</span><span class="sxs-lookup"><span data-stu-id="5d7a5-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="5d7a5-116">โปรดจำไว้ว่าไม่มีการดำเนินการคำนวณการคิดต้นทุนแบบย้อนกลับที่มีวันที่ %1 สิ้นสุดรอบระยะเวลาที่ตรงกันแล้ว</span><span class="sxs-lookup"><span data-stu-id="5d7a5-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="5d7a5-117">การประเมินค่าสินค้าคงคลัง ต้นทุนของสินค้าที่ขายและผลต่างอาจไม่ถูกต้องในบัญชีแยกประเภทย่อยหรือบัญชีแยกประเภททั่วไปจนกว่าจะมีการดำเนินการนี้</span><span class="sxs-lookup"><span data-stu-id="5d7a5-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="5d7a5-118">มีการแก้ไขปัญหานี้ในรุ่น10.0.13 และในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="5d7a5-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="5d7a5-119">สำหรับข้อมูลเพิ่มเติม ให้ดู [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296)</span><span class="sxs-lookup"><span data-stu-id="5d7a5-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>
