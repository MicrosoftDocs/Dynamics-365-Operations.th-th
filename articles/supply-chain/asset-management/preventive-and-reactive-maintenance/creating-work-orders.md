---
title: การสร้างใบสั่งงาน
description: หัวข้อนี้อธิบายวิธีการสร้างใบสั่งงานในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875919"
---
# <a name="creating-work-orders"></a><span data-ttu-id="bfebd-103">การสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="bfebd-103">Creating work orders</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="bfebd-104">เมื่อคุณจัดกำหนดการงานการบำรุงรักษาเชิงป้องกัน ขั้นตอนต่อไปคือสร้างใบสั่งงานสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="bfebd-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="bfebd-105">ซึ่งจะกระทำโดยหนึ่งในกำหนดการการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="bfebd-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="bfebd-106">งานที่จัดกำหนดการไว้ในกำหนดการบำรุงรักษาอาจมีชนิดข้อมูลอ้างอิงที่แตกต่างกัน:</span><span class="sxs-lookup"><span data-stu-id="bfebd-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="bfebd-107">ชนิดการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="bfebd-107">Reference type</span></span> | <span data-ttu-id="bfebd-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bfebd-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfebd-109">แผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="bfebd-109">Maintenance plans</span></span>     | <span data-ttu-id="bfebd-110">งานบำรุงรักษาเชิงป้องกันตามชนิดของแผนการบำรุงรักษา "เวลา" หรือ "ตัวนับ"</span><span class="sxs-lookup"><span data-stu-id="bfebd-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="bfebd-111">รอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="bfebd-111">Maintenance rounds</span></span>    | <span data-ttu-id="bfebd-112">งานบำรุงรักษาเชิงป้องกันที่มีสินทรัพย์หลายอย่างที่จำเป็นต้องมีชนิดของการบำรุงรักษาที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="bfebd-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="bfebd-113">คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="bfebd-113">Maintenance request</span></span>   | <span data-ttu-id="bfebd-114">คำขอที่สร้างขึ้นด้วยตนเองสำหรับการบำรุงรักษาหรือการซ่อมแซมสินทรัพย์ ซึ่งสามารถแปลงเป็นใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="bfebd-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="bfebd-115">คลิด **การจัดการสินทรัพย์** > **ทั่วไป** > **กำหนดการบำรุงรักษาทั้งหมด** หรือ **เปิดรายการกำหนดการบำรุงรักษา** หรือ **เปิดกลุ่มกำหนดการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="bfebd-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="bfebd-116">เลือกงานการบำรุงรักษาที่จัดกำหนดการไว้สำหรับที่คุณต้องการสร้างใบสั่งงาน แล้วคลิก **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="bfebd-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="bfebd-117">จำนวนรวมของชั่วโมงที่คาดการณ์สำหรับรายการที่เลือกจะแสดงอยู่ในฟิลด์ **ชั่วโมงการคาดการณ์การบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="bfebd-117">The total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="bfebd-118">ในส่วน **พารามิเตอร์** ให้เลือกว่าควรจะสร้างใบสั่งงานกี่ใบ</span><span class="sxs-lookup"><span data-stu-id="bfebd-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="bfebd-119">คุณสามารถสร้างใบสั่งงานหนึ่งใบต่อหนึ่งรายการกำหนดการบำรุงรักษา หรือจำนวนของใบสั่งงานตามการเลือกของคุณในส่วน **หนึ่งใบสั่งงานต่อ**</span><span class="sxs-lookup"><span data-stu-id="bfebd-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="bfebd-120">เลือก **ชนิดของใบสั่งงาน** ที่จะใช้ในใบสั่งงานทั้งหมดที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="bfebd-120">Select a **Work order type** that will be used on all the work orders you create.</span></span>

5. <span data-ttu-id="bfebd-121">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bfebd-121">Click **OK**.</span></span> <span data-ttu-id="bfebd-122">หนึ่งใบสั่งงานหรือมากกว่าถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="bfebd-122">One or more work orders are created.</span></span>

![รูปที่ 1](media/18-preventive-maintenance.png)

