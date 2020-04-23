---
title: การสร้างใบสั่งงาน
description: หัวข้อนี้อธิบายวิธีการสร้างใบสั่งงานในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/27/2019
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
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206138"
---
# <a name="creating-work-orders"></a><span data-ttu-id="baf10-103">การสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="baf10-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="baf10-104">เมื่อคุณจัดกำหนดการงานการบำรุงรักษาเชิงป้องกัน ขั้นตอนต่อไปคือสร้างใบสั่งงานสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="baf10-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="baf10-105">ซึ่งจะกระทำโดยหนึ่งในกำหนดการการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="baf10-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="baf10-106">งานที่จัดกำหนดการไว้ในกำหนดการบำรุงรักษาอาจมีชนิดข้อมูลอ้างอิงที่แตกต่างกัน:</span><span class="sxs-lookup"><span data-stu-id="baf10-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="baf10-107">ชนิดการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="baf10-107">Reference type</span></span> | <span data-ttu-id="baf10-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="baf10-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baf10-109">แผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="baf10-109">Maintenance plans</span></span>     | <span data-ttu-id="baf10-110">งานบำรุงรักษาเชิงป้องกันตามชนิดของแผนการบำรุงรักษา "เวลา" หรือ "ตัวนับ"</span><span class="sxs-lookup"><span data-stu-id="baf10-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="baf10-111">รอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="baf10-111">Maintenance rounds</span></span>    | <span data-ttu-id="baf10-112">งานบำรุงรักษาเชิงป้องกันที่มีสินทรัพย์หลายอย่างที่จำเป็นต้องมีชนิดของการบำรุงรักษาที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="baf10-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="baf10-113">คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="baf10-113">Maintenance request</span></span>   | <span data-ttu-id="baf10-114">คำขอที่สร้างขึ้นด้วยตนเองสำหรับการบำรุงรักษาหรือการซ่อมแซมสินทรัพย์ ซึ่งสามารถแปลงเป็นใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="baf10-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="baf10-115">คลิด **การจัดการสินทรัพย์** > **ทั่วไป** > **กำหนดการบำรุงรักษาทั้งหมด** หรือ **เปิดรายการกำหนดการบำรุงรักษา** หรือ **เปิดกลุ่มกำหนดการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="baf10-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="baf10-116">เลือกงานการบำรุงรักษาที่จัดกำหนดการไว้สำหรับที่คุณต้องการสร้างใบสั่งงาน แล้วคลิก **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="baf10-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="baf10-117">ในกล่องโต้ตอบ **สร้างใบสั่งงาน** จำนวนรวมของชั่วโมงที่คาดการณ์สำหรับรายการที่เลือกจะแสดงอยู่ในฟิลด์ **ชั่วโมงคาดการณ์การบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="baf10-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="baf10-118">ในส่วน **พารามิเตอร์** ให้เลือกว่าควรจะสร้างใบสั่งงานกี่ใบ</span><span class="sxs-lookup"><span data-stu-id="baf10-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="baf10-119">คุณสามารถสร้างใบสั่งงานหนึ่งใบต่อหนึ่งรายการกำหนดการบำรุงรักษา หรือจำนวนของใบสั่งงานตามการเลือกของคุณในส่วน **หนึ่งใบสั่งงานต่อ**</span><span class="sxs-lookup"><span data-stu-id="baf10-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="baf10-120">เลือก **ชนิดของใบสั่งงาน** ที่จะใช้ในใบสั่งงานทั้งหมดที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="baf10-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="baf10-121">ภาพด้านล่างแสดงตัวอย่างของกล่องโต้ตอบ **สร้างใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="baf10-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![รูปที่ 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="baf10-123">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="baf10-123">Click **OK**.</span></span> <span data-ttu-id="baf10-124">หนึ่งใบสั่งงานหรือมากกว่าถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="baf10-124">One or more work orders are created.</span></span>

