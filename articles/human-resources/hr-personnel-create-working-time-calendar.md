---
title: สร้างปฏิทินและกำหนดเวลาการทำงาน
description: ปฏิทินอธิบายถึงกำลังการผลิตและเวลาการทำงานของทรัพยากรการดำเนินงาน  บทความนี้อธิบายวิธีการกำหนดปฏิทินงานตามเท็มเพลตเวลาการทำงาน
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5c630297a8962d1bb383110881b2acdc872b9cd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420689"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="19e5b-104">สร้างปฏิทินและกำหนดเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="19e5b-104">Create calendars and generate working times</span></span>



<span data-ttu-id="19e5b-105">ปฏิทินอธิบายถึงกำลังการผลิตและเวลาการทำงานของทรัพยากรการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="19e5b-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="19e5b-106">บทความนี้อธิบายวิธีการกำหนดปฏิทินงานตามเท็มเพลตเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="19e5b-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="19e5b-107">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="19e5b-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="19e5b-108">ในหน้าแรก ให้เลือก **การจัดการรอบการใช้งานทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="19e5b-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="19e5b-109">เลือก **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="19e5b-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="19e5b-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="19e5b-110">Select **New**.</span></span>
4. <span data-ttu-id="19e5b-111">ในฟิลด์ **ปฏิทิน** ให้จัดประเภทปฏิทินของคุณ</span><span class="sxs-lookup"><span data-stu-id="19e5b-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="19e5b-112">นี่คือรหัสของปฏิทิน ซึ่งจะใช้เป็นการอ้างอิงเมื่อมีการกำหนดปฏิทินเช่น กำหนดไปยังทรัพยากรการดำเนินงานหรือกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="19e5b-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="19e5b-113">ในฟิลด์ **ชื่อ** ตั้งชื่อปฏิทินของคุณ</span><span class="sxs-lookup"><span data-stu-id="19e5b-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="19e5b-114">ในฟิลด์ **วันทำงานมาตรฐานในหน่วยชั่วโมง** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="19e5b-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="19e5b-115">ตรวจสอบให้แน่ใจว่ามีการเลือกแถว จากนั้นเลือก **เลือกเวลาทำงาน** จากบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="19e5b-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="19e5b-116">เลือก **จัดสร้างเวลาทำงาน**</span><span class="sxs-lookup"><span data-stu-id="19e5b-116">Select **Compose working times**.</span></span> <span data-ttu-id="19e5b-117">สร้างชั่วโมงทำงานสำหรับแต่ละวันในรอบระยะเวลาที่คุณต้องการให้สามารถมีการจัดกำหนดการงานได้ </span><span class="sxs-lookup"><span data-stu-id="19e5b-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="19e5b-118">เมื่อเวลาผ่านไป คุณสามารถสร้างเวลาทำงานสำหรับรอบระยะเวลาเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="19e5b-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="19e5b-119">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="19e5b-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="19e5b-120">วันแรกที่ปฏิทินนี้ต้องถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="19e5b-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="19e5b-121">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="19e5b-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="19e5b-122">วันสุดท้ายที่ปฏิทินนี้ต้องถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="19e5b-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="19e5b-123">ในฟิลด์ **เท็มเพลตเวลาการทำงาน** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="19e5b-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="19e5b-124">เท็มเพลตเวลาการทำงานกำหนดชั่วโมงทำงานสำหรับแต่ละวันของสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="19e5b-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="19e5b-125">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="19e5b-125">Select **OK**.</span></span>
13. <span data-ttu-id="19e5b-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="19e5b-126">Close the page.</span></span>

