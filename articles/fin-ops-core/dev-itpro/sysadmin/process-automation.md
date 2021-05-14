---
title: ระบบอัตโนมัติของกระบวนการ
description: หัวข้อนี้จะแสดงรายละเอียดเกี่ยวกับวิธีการทำงานของระบบอัตโนมัติของกระบวนการเพื่อให้สามารถจัดกำหนดการของกระบวนการที่จะรันโดยเซิร์ฟเวอร์ชุดงานได้อย่างง่าย
author: RyanCCarlson2
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: a8722adfe410f15bc379f9b550f0618c881f067d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920840"
---
# <a name="process-automation"></a><span data-ttu-id="74ab2-103">ระบบอัตโนมัติของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="74ab2-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="74ab2-104">ระบบอัตโนมัติของกระบวนการอนุญาตการจัดกำหนดการของกระบวนการที่จะรันโดยเซิร์ฟเวอร์ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="74ab2-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="74ab2-105">มุมมองปฏิทินที่มีการปรับปรุงของงานที่จัดกำหนดการไว้ อนุญาตให้ผู้ใช้สามารถดูและดำเนินการกับงานที่จัดกำหนดการและการดำเนินงานที่เสร็จสิ้นได้</span><span class="sxs-lookup"><span data-stu-id="74ab2-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="74ab2-106">การจัดการ</span><span class="sxs-lookup"><span data-stu-id="74ab2-106">Administration</span></span>

<span data-ttu-id="74ab2-107">พบหน้าการดูแลจากศูนย์กลางสำหรับระบบอัตโนมัติของกระบวนการทั้งหมดในโมดูลการจัดการระบบภายใต้เมนู **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="74ab2-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="74ab2-108">หน้านี้จะแสดงรายการะบบอัตโนมัติของกระบวนการ (ชุด) ทั้งหมดที่ตั้งค่าไว้ในระบบ</span><span class="sxs-lookup"><span data-stu-id="74ab2-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="74ab2-109">นอกจากนี้ยังจะช่วยให้คุณสามารถเพิ่มระบบอัตโนมัติของกระบวนการใหม่จากหน้านี้ได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="74ab2-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="74ab2-110">หลังจากที่มีการตั้งค่าชุดงานแล้ว คุณสามารถจัดการแต่ละชุดจากรายการนี้ได้</span><span class="sxs-lookup"><span data-stu-id="74ab2-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="74ab2-111">คุณสามารถเลือกที่จะแก้ไขทั้งชุดได้ ให้ลบทั้งชุดนั้น ดูการเกิดเหตุการณ์ทั้งหมดในมุมมองรายการ หรือปิดใช้งานชุดงานถ้าคุณต้องการหยุดงานที่จัดกำหนดการชั่วคราวสักพักหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="74ab2-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="74ab2-112">กระบวนการใดๆ ที่ปิดใช้งานในการจัดการคุณลักษณะจะไม่แสดงเมื่อปิดใช้งานคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="74ab2-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="74ab2-113">นอกจากนี้ กลไกจัดการการจัดกำหนดการอัตโนมัติของกระบวนการจะไม่จัดกำหนดการเหตุการณ์หรือกระบวนการแบบเบื้องหลังใดๆ สำหรับคุณลักษณะที่ปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="74ab2-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="74ab2-114">การเปิดใช้งานคุณลักษณะใหม่จะทำให้เหตุการณ์หรือกระบวนการแบบเบื้องหลังใดๆ ที่จัดกำหนดการไว้อดีตทำงานทันที</span><span class="sxs-lookup"><span data-stu-id="74ab2-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span> <span data-ttu-id="74ab2-115">กลไกจัดการการจัดตารางการผลิตระบบอัตโนมัติของกระบวนการอาศัยชุดงานของระบบ **ประมวลผลงานของระบบสำรวจอัตโนมัติ** เพื่อรัน</span><span class="sxs-lookup"><span data-stu-id="74ab2-115">The process automation scheduling engine relies on the system batch job, **Process automation polling system job** to run.</span></span> <span data-ttu-id="74ab2-116">งานไม่ควรมีการเปลี่ยนแปลงหรือแก้ไขเมื่อใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="74ab2-116">The job shouldn't be altered or tampered with at any time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="74ab2-117">มุมมองปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="74ab2-117">Calendar view</span></span>

<span data-ttu-id="74ab2-118">ประโยชน์ที่สำคัญอย่างหนึ่งของการดำเนินการอัตโนมัติของกระบวนการคือความสามารถในการดูงานที่จัดกำหนดการไว้ในมุมมองปฏิทินอย่างง่าย</span><span class="sxs-lookup"><span data-stu-id="74ab2-118">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="74ab2-119">มุมมองนี้จะช่วยให้คุณสามารถดูงานสำหรับหนึ่งสัปดาห์พร้อมกันได้</span><span class="sxs-lookup"><span data-stu-id="74ab2-119">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="74ab2-120">คุณจะเห็นมุมมองนี้ที่ด้านขวาของหน้า **ระบบอัตโนมัติของกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="74ab2-120">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="74ab2-121">ฟิลด์นี้จะถูกเติมด้วยงานที่จัดกำหนดการไว้สำหรับชุดงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="74ab2-121">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="74ab2-122">[![ปฎิทินระบบอัตโนมัติของกระบวนการ](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="74ab2-122">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="74ab2-123">การเปลี่ยนแปลงที่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="74ab2-123">Occurrence changes</span></span>

<span data-ttu-id="74ab2-124">แต่ละเหตุการณ์สามารถแก้ไขได้โดยไม่มีผลกระทบต่อเหตุการณ์อื่นๆ ที่กำหนดโดยชุดข้อมูลที่มีต้นกำเนิดมา</span><span class="sxs-lookup"><span data-stu-id="74ab2-124">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="74ab2-125">สามารถแก้ไขเหตุการณ์ของงานที่จัดกำหนดการไว้ได้จากมุมมองปฏิทิน โดยเลือกปุ่ม **ดู/แก้ไข** และการเลือก **เหตุการณ์**</span><span class="sxs-lookup"><span data-stu-id="74ab2-125">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="74ab2-126">หน้านี้จะให้คุณสามารถเข้าถึงการตั้งค่าทั้งหมดที่แสดงอยู่ในวิซาร์ดการตั้งค่าชุดข้อมูลและช่วยให้คุณสามารถเปลี่ยนแปลงการตั้งค่าครั้งเดียวสำหรับการเกิดขึ้นที่เลือกได้</span><span class="sxs-lookup"><span data-stu-id="74ab2-126">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="74ab2-127">การเกิดขึ้นของงานที่จัดกำหนดการอาจปิดโดยการเลือกปุ่ม **ปิดใช้งาน** จากมุมมองปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="74ab2-127">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="74ab2-128">เอกสารประกอบสำหรับนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="74ab2-128">Developer documentation</span></span>

<span data-ttu-id="74ab2-129">กรอบงานการทำงานอัตโนมัติทำให้นักพัฒนาขยายโครงสร้างการทำงานอัตโนมัติของกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="74ab2-129">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="74ab2-130">เอกสาร [กรอบงานการทำงานอัตโนมัติ](../process-automation/process-automation-framework.md) จะให้ข้อมูลเกี่ยวกับวิธีการที่คุณสามารถสร้างกระบวนการแบบกำหนดเอง ซึ่งคุณต้องรันโดยเซิร์ฟเวอร์ชุดงานที่มีการจัดกำหนดการด้วยวิซาร์ดการทำงานอัตโนมัติของกระบวนการและจะปรากฏในมุมมองปฏิทินโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="74ab2-130">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
