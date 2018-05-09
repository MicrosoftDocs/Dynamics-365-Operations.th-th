---
title: "นำใบสั่งผลิตออกใช้"
description: "กระบวนงานนี้แสดงวิธีการนำใบสั่งผลิตออกใช้ "
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 77dc4f1908836498568251c75efde930b4f88fcf
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="release-a-production-order"></a><span data-ttu-id="6e702-103">นำใบสั่งผลิตออกใช้</span><span class="sxs-lookup"><span data-stu-id="6e702-103">Release a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e702-104">กระบวนงานนี้แสดงวิธีการนำใบสั่งผลิตออกใช้ </span><span class="sxs-lookup"><span data-stu-id="6e702-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="6e702-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="6e702-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6e702-106">นี่เป็นขั้นตอนที่สี่จากเจ็ดขั้นตอนซึ่งอธิบายวงจรชีวิตของใบสั่งการผลิต</span><span class="sxs-lookup"><span data-stu-id="6e702-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="6e702-107">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6e702-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="6e702-108">ในกริด ให้เลือกใบสั่งผลิตที่มีสถานะเป็นจัดกำหนดการแล้ว</span><span class="sxs-lookup"><span data-stu-id="6e702-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="6e702-109">ในบานหน้าต่างการดำเนินการ คลิกที่ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="6e702-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="6e702-110">คลิกที่การนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="6e702-110">Click Release.</span></span>
    * <span data-ttu-id="6e702-111">บนหน้านี้ คุณสามารถยืนยันการนำออกใช้ของช่วงของใบสั่งผลิตที่เลือก </span><span class="sxs-lookup"><span data-stu-id="6e702-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="6e702-112">คลิกเลือกถ้าคุณต้องการเพิ่มใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="6e702-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="6e702-113">ขั้นตอนการนำออกใช้ระบุว่า เมื่อใบสั่งผลิตได้ถูกนำออกใช้ในการผลิตผลิตภัณฑ์ การดำเนินการผลิตจะสามารถรายงานความคืบหน้าในงานการผลิต </span><span class="sxs-lookup"><span data-stu-id="6e702-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="6e702-114">สามารถออกเอกสารการผลิตที่ประกอบด้วยรายละเอียดเกี่ยวกับการประมวลผลของงาน </span><span class="sxs-lookup"><span data-stu-id="6e702-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="6e702-115">งานคลังสินค้าสำหรับการจัดหาวัตถุดิบถูกสร้างขึ้นสำหรับสินค้าที่มีตั้งค่าสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6e702-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="6e702-116">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="6e702-116">Click the General tab.</span></span>
    * <span data-ttu-id="6e702-117">เลือกการผลิตที่ควรจะมีการพิมพ์รายงาน </span><span class="sxs-lookup"><span data-stu-id="6e702-117">Select which production reports should be printed.</span></span> <span data-ttu-id="6e702-118">รายงานบัตรงานพิมพ์หน้าของแต่ละงานที่ได้จัดกำหนดการไว้ และจำเป็นต้องมีใบสั่งผลิตที่ได้รับการกำหนดทีระดับของงาน </span><span class="sxs-lookup"><span data-stu-id="6e702-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="6e702-119">รายงานประกอบด้วยข้อมูลเกี่ยวกับการกำหนดการเริ่มต้นและเวลาสิ้นสุด ปริมาณการผลิต และทรัพยากรการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="6e702-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="6e702-120">รายงานงานในกระบวนการผลิตจะรวบรวมข้อมูลเดียวกันบนหน้าเดียวกัน แต่จะไม่พิมพ์หน้าแต่ละงาน </span><span class="sxs-lookup"><span data-stu-id="6e702-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="6e702-121">รายงานบัตรกระบวนการผลิตแสดงเฉพาะการดำเนินงานไม่ใช่งาน </span><span class="sxs-lookup"><span data-stu-id="6e702-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="6e702-122">ดังนั้น รายงานนี้ไม่จำเป็นต้องจัดกำหนดการงาน แต่สามารถใช้ได้เมื่อมีการจัดกำหนดการใบสั่งผลิตในระดับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="6e702-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="6e702-123">คลิกที่กล่องกาเครื่องหมายการพิมพ์บัตรกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="6e702-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="6e702-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6e702-124">Click OK.</span></span>
7. <span data-ttu-id="6e702-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e702-125">Close the page.</span></span>

