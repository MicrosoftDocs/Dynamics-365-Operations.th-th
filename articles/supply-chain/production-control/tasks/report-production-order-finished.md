---
title: รายงานการเสร็จงานของใบสั่งผลิต
description: 'ขั้นตอนนี้แสดงถึงวิธีการรายงานใบสั่งผลิตเมื่อเสร็จสมบูรณ์ '
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97e67ff51e4bc4533aeb2485c34cd5ec8a882bb6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "320500"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="e92c4-103">รายงานการเสร็จงานของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="e92c4-103">Report a production order as finished</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e92c4-104">ขั้นตอนนี้แสดงถึงวิธีการรายงานใบสั่งผลิตเมื่อเสร็จสมบูรณ์ </span><span class="sxs-lookup"><span data-stu-id="e92c4-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="e92c4-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="e92c4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e92c4-106">นี่เป็นขั้นตอนที่หกจากเจ็ดซึ่งอธิบายวงจรชีวิตใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="e92c4-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="e92c4-107">รายงานการเสร็จงานของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="e92c4-107">Report a production order as finished</span></span>
1. <span data-ttu-id="e92c4-108">ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="e92c4-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="e92c4-109">เลือกใบสั่งผลิตที่มีสถานะเริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="e92c4-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="e92c4-110">ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="e92c4-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="e92c4-111">คลิก รายงาน เมื่อเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="e92c4-111">Click Report as finished.</span></span>
    * <span data-ttu-id="e92c4-112">บนหน้านี้ คุณสามารถยืนยันปริมาณของผลิตภัณฑ์สำเร็จรูปที่จะรายงานเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e92c4-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="e92c4-113">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="e92c4-113">Click the General tab.</span></span>
5. <span data-ttu-id="e92c4-114">ตั้งค่าปริมาณสินค้าที่ดีเป็น '18'</span><span class="sxs-lookup"><span data-stu-id="e92c4-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="e92c4-115">กำหนดปริมาณสินค้าที่บกพร่องเป็น '2'</span><span class="sxs-lookup"><span data-stu-id="e92c4-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="e92c4-116">ในฟิลด์สาเหตุของข้อผิดพลาด เลือก 'วัสดุ'</span><span class="sxs-lookup"><span data-stu-id="e92c4-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="e92c4-117">เลือกหรือล้างจบงานกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="e92c4-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="e92c4-118">เลือกหรือยกเลิกยอมรับข้อผิดพลาดกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="e92c4-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="e92c4-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e92c4-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="e92c4-120">ตรวจสอบรายงานสมุดรายวันเมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e92c4-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="e92c4-121">ในบานหน้าต่างการดำเนินการ ให้คลิก ดู</span><span class="sxs-lookup"><span data-stu-id="e92c4-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="e92c4-122">คลิก รายงานเมื่อเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="e92c4-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="e92c4-123">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e92c4-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e92c4-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e92c4-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e92c4-125">มีการงรายการบัญชีรายงานเมื่อสมุดรายวันเสร็จสมบูรณ์ </span><span class="sxs-lookup"><span data-stu-id="e92c4-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="e92c4-126">ถ้าคุณต้องการทำการปรับปรุงสมุดรายวัน คุณสามารถสร้างสมุดรายวันใหม่ที่คุณสามารถสร้างการเปลี่ยนแปลงด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="e92c4-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

