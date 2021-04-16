---
title: สร้างปฏิทินและกำหนดเวลาการทำงาน
description: ปฏิทินอธิบายถึงกำลังการผลิตและเวลาการทำงานของทรัพยากรการดำเนินงาน  บทความนี้อธิบายวิธีการกำหนดปฏิทินงานตามเท็มเพลตเวลาการทำงาน
author: andreabichsel
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f28e11613cb9e10b258e1c373890505fb6e71d29
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804925"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="4ab00-104">สร้างปฏิทินและกำหนดเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="4ab00-104">Create calendars and generate working times</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="4ab00-105">ปฏิทินอธิบายถึงกำลังการผลิตและเวลาการทำงานของทรัพยากรการดำเนินงาน </span><span class="sxs-lookup"><span data-stu-id="4ab00-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="4ab00-106">บทความนี้อธิบายวิธีการกำหนดปฏิทินงานตามเท็มเพลตเวลาการทำงาน</span><span class="sxs-lookup"><span data-stu-id="4ab00-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="4ab00-107">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="4ab00-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="4ab00-108">ในหน้าแรก ให้เลือก **การจัดการรอบการใช้งานทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="4ab00-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="4ab00-109">เลือก **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="4ab00-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="4ab00-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="4ab00-110">Select **New**.</span></span>
4. <span data-ttu-id="4ab00-111">ในฟิลด์ **ปฏิทิน** ให้จัดประเภทปฏิทินของคุณ</span><span class="sxs-lookup"><span data-stu-id="4ab00-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="4ab00-112">นี่คือรหัสของปฏิทิน ซึ่งจะใช้เป็นการอ้างอิงเมื่อมีการกำหนดปฏิทินเช่น กำหนดไปยังทรัพยากรการดำเนินงานหรือกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4ab00-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="4ab00-113">ในฟิลด์ **ชื่อ** ตั้งชื่อปฏิทินของคุณ</span><span class="sxs-lookup"><span data-stu-id="4ab00-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="4ab00-114">ในฟิลด์ **วันทำงานมาตรฐานในหน่วยชั่วโมง** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="4ab00-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="4ab00-115">ตรวจสอบให้แน่ใจว่ามีการเลือกแถว จากนั้นเลือก **เลือกเวลาทำงาน** จากบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="4ab00-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="4ab00-116">เลือก **จัดสร้างเวลาทำงาน**</span><span class="sxs-lookup"><span data-stu-id="4ab00-116">Select **Compose working times**.</span></span> <span data-ttu-id="4ab00-117">สร้างชั่วโมงทำงานสำหรับแต่ละวันในรอบระยะเวลาที่คุณต้องการให้สามารถมีการจัดกำหนดการงานได้ </span><span class="sxs-lookup"><span data-stu-id="4ab00-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="4ab00-118">เมื่อเวลาผ่านไป คุณสามารถสร้างเวลาทำงานสำหรับรอบระยะเวลาเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="4ab00-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="4ab00-119">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="4ab00-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="4ab00-120">วันแรกที่ปฏิทินนี้ต้องถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="4ab00-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="4ab00-121">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="4ab00-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="4ab00-122">วันสุดท้ายที่ปฏิทินนี้ต้องถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="4ab00-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="4ab00-123">ในฟิลด์ **เท็มเพลตเวลาการทำงาน** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="4ab00-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="4ab00-124">เท็มเพลตเวลาการทำงานกำหนดชั่วโมงทำงานสำหรับแต่ละวันของสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="4ab00-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="4ab00-125">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4ab00-125">Select **OK**.</span></span>
13. <span data-ttu-id="4ab00-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4ab00-126">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]