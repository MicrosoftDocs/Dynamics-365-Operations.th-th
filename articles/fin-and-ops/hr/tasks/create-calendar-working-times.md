---
title: สร้างปฏิทินและกำหนดเวลาการทำงาน
description: 'ปฏิทินอธิบายถึงกำลังการผลิตและเวลาการทำงานของทรัพยากรการดำเนินงาน '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba4bd51d2102b3036307f34ab46f94f83df4f461
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "857002"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="3a9c3-103">สร้างปฏิทินและกำหนดเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3a9c3-103">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a9c3-104">ปฏิทินอธิบายถึงกำลังการผลิตและเวลาการทำงานของทรัพยากรการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="3a9c3-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="3a9c3-105">กระบวนงานนี้จะช่วยให้คุณสามารถกำหนดปฏิทินงานตามเท็มเพลตเวลาการทำงาน </span><span class="sxs-lookup"><span data-stu-id="3a9c3-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="3a9c3-106">คุณสามารถดำเนินการขั้นตอนนี้ได้ในข้อมูลสาธิตของบริษัท USMF หรือการใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="3a9c3-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="3a9c3-107">ไปที่พื้นที่ทำงานทั้งหมด > การจัดการรอบการใช้งานทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="3a9c3-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="3a9c3-108">คลิกปฏิทินการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3a9c3-108">Click Calendars.</span></span>
3. <span data-ttu-id="3a9c3-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3a9c3-109">Click New.</span></span>
4. <span data-ttu-id="3a9c3-110">ในฟิลด์ปฏิทิน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3a9c3-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="3a9c3-111">นี่คือรหัสของปฏิทิน ซึ่งจะใช้เป็นการอ้างอิงเมื่อมีการกำหนดปฏิทินเช่น กำหนดไปยังทรัพยากรการดำเนินงานหรือกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="3a9c3-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="3a9c3-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="3a9c3-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="3a9c3-113">ในฟิลด์วันทำงานมาตรฐานในหน่วยชั่วโมง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3a9c3-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="3a9c3-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3a9c3-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="3a9c3-115">คลิกเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3a9c3-115">Click Working times.</span></span>
9. <span data-ttu-id="3a9c3-116">คลิกจัดสร้างเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3a9c3-116">Click Compose working times.</span></span>
    * <span data-ttu-id="3a9c3-117">สร้างชั่วโมงทำงานสำหรับแต่ละวันในรอบระยะเวลาที่คุณต้องการให้สามารถมีการจัดกำหนดการงานได้ </span><span class="sxs-lookup"><span data-stu-id="3a9c3-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="3a9c3-118">เมื่อเวลาผ่านไป คุณสามารถสร้างเวลาทำงานสำหรับรอบระยะเวลาเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="3a9c3-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="3a9c3-119">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3a9c3-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="3a9c3-120">วันแรกที่ปฏิทินนี้ต้องถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="3a9c3-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="3a9c3-121">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3a9c3-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="3a9c3-122">วันสุดท้ายที่ปฏิทินนี้ต้องถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="3a9c3-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="3a9c3-123">ในฟิลด์เท็มเพลตเวลาการทำงาน ให้ตกลงหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="3a9c3-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="3a9c3-124">เท็มเพลตเวลาการทำงานกำหนดชั่วโมงทำงานสำหรับแต่ละวันของสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="3a9c3-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="3a9c3-125">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="3a9c3-125">Click OK.</span></span>
14. <span data-ttu-id="3a9c3-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3a9c3-126">Close the page.</span></span>

