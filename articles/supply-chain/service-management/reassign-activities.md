---
title: "การกำหนดกิจกรรมอีกครั้ง"
description: "หัวข้อนี้อธิบายวิธีการกำหนดกิจกรรมการบริการจากผู้ปฏิบัติงานหนึ่งให้ผู้ปฏิบัติงานอื่น "
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMADispatchBoard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 215b10cc0733c1beab52fa39e09c83d40a6297a3
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---


# <a name="reassign-activities"></a><span data-ttu-id="0f7f1-103">การกำหนดกิจกรรมอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="0f7f1-103">Reassign activities</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0f7f1-104">หัวข้อนี้อธิบายวิธีการกำหนดกิจกรรมการบริการจากผู้ปฏิบัติงานหนึ่งให้ผู้ปฏิบัติงานอื่น </span><span class="sxs-lookup"><span data-stu-id="0f7f1-104">This topic describes how to reassign service activities from one worker to another worker.</span></span> <span data-ttu-id="0f7f1-105">คุณสามารถกำหนดกิจกรรมการบริการจากผู้ปฏิบัติงานหนึ่งให้ผู้ปฏิบัติงานอื่นแม้ว่าจะกำหนดให้กับทีมงานจัดส่งที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="0f7f1-105">You can reassign service activities from one worker to another worker even if those workers are assigned to different dispatch teams.</span></span>

<span data-ttu-id="0f7f1-106">ใช้ขั้นตอนต่อไปนี้เพื่อมอบหมายกิจกรรมให้ผู้ปฏิบัติงานอื่น</span><span class="sxs-lookup"><span data-stu-id="0f7f1-106">Use the following steps to reassign an activity to another worker:</span></span>

1.  <span data-ttu-id="0f7f1-107">คลิก **การจัดการงานบริการ** \> **งานประจำงวด** \> **บอร์ดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="0f7f1-107">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>

2.  <span data-ttu-id="0f7f1-108">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ป้อนวันที่เพื่อกำหนดรอบระยะเวลาที่คุณต้องการดูกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="0f7f1-108">In the **From date** and **To date** fields, enter dates to define the time period to view activities for.</span></span>

3.  <span data-ttu-id="0f7f1-109">เลือกว่าจะดูกิจกรรมที่ปิดและข้อมูลสำหรับทีมงานที่เกี่ยวข้องกับการจัดส่งและคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0f7f1-109">Select whether to view closed activities and dispatch information for related teams, and then click **OK**.</span></span>

4.  <span data-ttu-id="0f7f1-110">ในแบบฟอร์ม **บอร์ดการจัดส่ง** คลิก **ขั้นสูง** เพื่อแสดงเฉพาะแผนภูมิ Gantt ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="0f7f1-110">In the **Dispatch board** form, click **Advanced** to display only the Gantt chart at the top of the page.</span></span> <span data-ttu-id="0f7f1-111">คลิก **แบบง่าย** เพื่อแสดงแผนภูมิ Gantt และแท็บในแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="0f7f1-111">Click **Simple** to display the Gantt chart and the tabs in the form.</span></span>

5.  <span data-ttu-id="0f7f1-112">ขยายรายชื่อของทีมงานการจัดส่งแต่ละทีม</span><span class="sxs-lookup"><span data-stu-id="0f7f1-112">Expand each dispatch team list.</span></span>

6.  <span data-ttu-id="0f7f1-113">ใช้ขั้นตอนมใดๆ ต่อไปนี้เพื่อมอบหมายกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="0f7f1-113">Use either of the following steps to reassign an activity:</span></span>
    
      - <span data-ttu-id="0f7f1-114">เลือกรูปภาพที่มีรหัสสีแสดงถึงกิจกรรมการบริการที่กำหนด </span><span class="sxs-lookup"><span data-stu-id="0f7f1-114">Select a color-coded graphic that represents the service activity to reassign.</span></span> <span data-ttu-id="0f7f1-115">กดปุ่ม SHIFT แล้วย้ายรูปภาพที่มีรหัสสีไปยังแถวของพนักงานรายอื่น</span><span class="sxs-lookup"><span data-stu-id="0f7f1-115">Press the SHIFT key, and then move the color-coded graphic to the row for another employee.</span></span>
    
      - <span data-ttu-id="0f7f1-116">บนแท็บ **ทั้งหมด** แท็บ **ทีม** แท็บ **ยังไม่ได้จัดส่ง** หรือแท็บ **ที่เกี่ยวข้อง** ในฟิลด์ **ผู้ปฏิบัติงาน** ป้อนชื่อของผู้ปฏิบัติงานที่จะแทนผู้ปฏิบัติงานปัจจุบันสำหรับกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="0f7f1-116">On the **All** tab, **Team** tab, **Undispatched** tab, or **Related** tab, in the **Worker** field, enter the name of the worker who is replacing the current worker for the activity.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f7f1-117">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="0f7f1-117">See also</span></span>

[<span data-ttu-id="0f7f1-118">กิจกรรมการบริการ</span><span class="sxs-lookup"><span data-stu-id="0f7f1-118">Service activities</span></span>](service-activities.md)

[<span data-ttu-id="0f7f1-119">บอร์ดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0f7f1-119">Dispatch board</span></span>](dispatch-board.md)




