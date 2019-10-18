---
title: การสร้างใบสั่งงาน
description: หัวข้อนี้อธิบายวิธีการสร้างใบสั่งงานในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a348bc9b7f5a24c5a3ac57113d430a92020b893
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922125"
---
# <a name="creating-work-orders"></a><span data-ttu-id="9388f-103">การสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="9388f-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="9388f-104">เมื่อคุณจัดกำหนดการงานการบำรุงรักษาเชิงป้องกัน ขั้นตอนต่อไปคือสร้างใบสั่งงานสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="9388f-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="9388f-105">ซึ่งจะกระทำโดยหนึ่งในกำหนดการการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9388f-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="9388f-106">งานที่จัดกำหนดการไว้ในกำหนดการบำรุงรักษาอาจมีชนิดข้อมูลอ้างอิงที่แตกต่างกัน:</span><span class="sxs-lookup"><span data-stu-id="9388f-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="9388f-107">ชนิดการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="9388f-107">Reference type</span></span> | <span data-ttu-id="9388f-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="9388f-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9388f-109">แผนการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9388f-109">Maintenance plans</span></span>     | <span data-ttu-id="9388f-110">งานบำรุงรักษาเชิงป้องกันตามชนิดของแผนการบำรุงรักษา "เวลา" หรือ "ตัวนับ"</span><span class="sxs-lookup"><span data-stu-id="9388f-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="9388f-111">รอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9388f-111">Maintenance rounds</span></span>    | <span data-ttu-id="9388f-112">งานบำรุงรักษาเชิงป้องกันที่มีสินทรัพย์หลายอย่างที่จำเป็นต้องมีชนิดของการบำรุงรักษาที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="9388f-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="9388f-113">คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="9388f-113">Maintenance request</span></span>   | <span data-ttu-id="9388f-114">คำขอที่สร้างขึ้นด้วยตนเองสำหรับการบำรุงรักษาหรือการซ่อมแซมสินทรัพย์ ซึ่งสามารถแปลงเป็นใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="9388f-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="9388f-115">คลิด **การจัดการสินทรัพย์** > **ทั่วไป** > **กำหนดการบำรุงรักษาทั้งหมด** หรือ **เปิดรายการกำหนดการบำรุงรักษา** หรือ **เปิดกลุ่มกำหนดการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="9388f-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="9388f-116">เลือกงานการบำรุงรักษาที่จัดกำหนดการไว้สำหรับที่คุณต้องการสร้างใบสั่งงาน แล้วคลิก **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="9388f-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="9388f-117">ในกล่องโต้ตอบ **สร้างใบสั่งงาน** จำนวนรวมของชั่วโมงที่คาดการณ์สำหรับรายการที่เลือกจะแสดงอยู่ในฟิลด์ **ชั่วโมงคาดการณ์การบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="9388f-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="9388f-118">ในส่วน **พารามิเตอร์** ให้เลือกว่าควรจะสร้างใบสั่งงานกี่ใบ</span><span class="sxs-lookup"><span data-stu-id="9388f-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="9388f-119">คุณสามารถสร้างใบสั่งงานหนึ่งใบต่อหนึ่งรายการกำหนดการบำรุงรักษา หรือจำนวนของใบสั่งงานตามการเลือกของคุณในส่วน **หนึ่งใบสั่งงานต่อ**</span><span class="sxs-lookup"><span data-stu-id="9388f-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="9388f-120">เลือก **ชนิดของใบสั่งงาน** ที่จะใช้ในใบสั่งงานทั้งหมดที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="9388f-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="9388f-121">ภาพด้านล่างแสดงตัวอย่างของกล่องโต้ตอบ **สร้างใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="9388f-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![รูปที่ 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="9388f-123">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9388f-123">Click **OK**.</span></span> <span data-ttu-id="9388f-124">หนึ่งใบสั่งงานหรือมากกว่าถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="9388f-124">One or more work orders are created.</span></span>

