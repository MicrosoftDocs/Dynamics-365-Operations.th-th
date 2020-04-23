---
title: จัดกำหนดการใบสั่งงานในวันที่และเวลาเฉพาะ
description: หัวข้อนี้อธิบายถึงวิธีการจัดกำหนดการใบสั่งงานบนวันที่และเวลาที่ระบุในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e81ea13a3463965c6e4785dac32f536d2e94a7ba
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215274"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="69ea5-103">จัดกำหนดการใบสั่งงานในวันที่และเวลาเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="69ea5-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="69ea5-104">หากต้องจัดกำหนดการใบสั่งงานในวันที่ *และ* เวลาที่ระบุคุณ สามารถแทนที่กระบวนการจัดกำหนดการมาตรฐานในการจัดการสินทรัพย์ และสร้างกำหนดการเฉพาะสำหรับใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="69ea5-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="69ea5-105">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="69ea5-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="69ea5-106">ในรายการใบสั่งงาน ให้คลิกที่รหัสใบสั่งงานในคอลัมน์ **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="69ea5-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="69ea5-107">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="69ea5-107">Click **Edit**.</span></span>

4. <span data-ttu-id="69ea5-108">บนแท็บด่วน **ส่วนหัวของใบสั่งงาน** ให้ใส่วันที่เริ่มต้นและสิ้นสุด ในฟิลด์ **เริ่มต้นที่คาดไว้** และ **สิ้นสุดที่คาดไว้**</span><span class="sxs-lookup"><span data-stu-id="69ea5-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

    ![รูปที่ 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="69ea5-110">บนแท็บ **ทั่วไป** คลิก **กำหนดการ** เพื่อใช้กระบวนการจัดกำหนดการมาตรฐาน หรือคลิก **จัดส่ง** หากคุณต้องการมอบหมายใบสั่งงานให้กับผู้ปฏิบัติงานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="69ea5-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to assign the work order to a specific worker.</span></span>

6. <span data-ttu-id="69ea5-111">เมื่อต้องการแทนที่การจองกำลังการผลิตที่มีอยู่ใดๆ เพื่อให้แน่ใจว่าใบสั่งงานมีการจัดกำหนดการไว้ในรอบระยะเวลาที่คาวไว้ ให้ทำการเลือกเหมือนกับที่แสดงในภาพในกล่องโต้ตอบ **กำหนดการใบสั่งงาน** > ส่วน **กำลังการผลิตมีจำกัด**</span><span class="sxs-lookup"><span data-stu-id="69ea5-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="69ea5-112">ซึ่งหมายความว่ากระบวนการจัดกำหนดการจะละเว้นการจองกำลังการผลิตที่มีอยู่ เนื่องจากใบสั่งงานต้องเริ่มต้นในเวลาเริ่มต้นที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="69ea5-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

    ![รูปที่ 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="69ea5-114">คลิก **ตกลง** เพื่อเริ่มต้นการจัดกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="69ea5-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="69ea5-115">หากกระบวนการจัดกำหนดการมีผลในการจองซ้ำ คุณจะเห็นข้อความบนหน้าจอและคุณสามารถปรับปรุงใบสั่งงานที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="69ea5-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="69ea5-116">เมื่อต้องการจัดกำหนดการให้กับเจ้าหน้าที่บำรุงรักษาสำหรับใบสั่งงาน เจ้าหน้าที่บำรุงรักษานั้นต้องพร้อมใช้งานในวันที่และเวลาเริ่มต้นที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="69ea5-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="69ea5-117">ความพร้อมของผู้ปฏิบัติงาน ตั้งค่าใน [ปฏิทินของผู้ปฏิบัติงาน](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md)</span><span class="sxs-lookup"><span data-stu-id="69ea5-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 

