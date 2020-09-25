---
title: ซิงโครไนส์ขีดความสามารถทรัพยากร
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการซิงโครไนส์ขีดความสามารถของทรัพยากรระหว่างปฏิทินและโครงการ
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760672"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="09b15-103">ซิงโครไนส์ขีดความสามารถทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="09b15-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09b15-104">กระบวนการสำหรับการซิงโครไนส์ทรัพยากร ช่วยรับประกันว่าข้อมูลปฏิทินและปฏิทินฐานจะลงไปที่การจัดกำหนดการทรัพยากรของโครงการ</span><span class="sxs-lookup"><span data-stu-id="09b15-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="09b15-105">ถ้ามีการเปลี่ยนแปลงปฏิทิน กระบวนการจะทำการอัปเดตที่จำเป็นไปที่การจัดกำหนดการของทรัพยากรของโครงการ</span><span class="sxs-lookup"><span data-stu-id="09b15-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="09b15-106">กระบวนการยังช่วยปรับปรุงประสิทธิภาพอีกด้วย เนื่องจากข้อมูลทรัพยากรปฏิทินจะถูกซิงโครไนส์ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="09b15-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="09b15-107">ดังนั้น การปรับปรุงข้อมูลการจัดกำหนดการทรัพยากรเกิดขึ้นได้เร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="09b15-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="09b15-108">เราขอแนะนำให้คุณจัดกำหนดการกระบวนการเป็นชุดงาน แทนที่จะเป็นทีละหนึ่งในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="09b15-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="09b15-109">มิฉะนั้น มีความเสี่ยงที่บุคคลจะลืมวันที่ครอบคลุมเมื่อข้อมูลถูกซิงโครไนส์ล่าสุด</span><span class="sxs-lookup"><span data-stu-id="09b15-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="09b15-110">ถ้าไม่ได้ใช้ในวันที่ครอบคลุม ช่องว่างอาจเกิดขึ้นระหว่างการซิงโครไนส์วันที่ </span><span class="sxs-lookup"><span data-stu-id="09b15-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![การซิงโครไนส์ปฏิทิน](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="09b15-112">ซิงโครไนส์การรวบรวมกำลังการผลิตสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="09b15-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="09b15-113">กระบวนการการซิงโครไนส์ถูกออกแบบมาเพื่อซิงโครไนส์ข้อมูลปฏิทินทรัพยากรทั้งหมด </span><span class="sxs-lookup"><span data-stu-id="09b15-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="09b15-114">ข้อมูลนี้ประกอบด้วย ข้อมูลปฏิทินพื้นฐานเกี่ยวกับการเปลี่ยนแปลงใดๆ ไปยังตารางกำลังการผลิตตามปฏิทินของทรัพยากรของโครงการ</span><span class="sxs-lookup"><span data-stu-id="09b15-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="09b15-115">ถ้ามีการเพิ่มทรัพยากรใหม่ในโครงการ การซิงโครไนส์จะช่วยรับประกันว่า ข้อมูลปฏิทินที่อัปเดตจะพร้อมใช้งาน </span><span class="sxs-lookup"><span data-stu-id="09b15-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="09b15-116">การซิงโครไนส์นี้สามารถทำได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="09b15-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="09b15-117">เราแนะนำให้คุณใช้ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="09b15-117">We recommend that you use a batch.</span></span> <span data-ttu-id="09b15-118">ตัวเลือกจะพร้อมใช้งานในระหว่างการซิงโครไนส์การจองกำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="09b15-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="09b15-119">เลือก **การจัดการและการบัญชีโครงการ** &gt; **งานประจำงวด** &gt; **การซิงโครไนส์กำลังการผลิต** &gt; **ซิงโครไนส์การรวบรวมกำลังการผลิตสำหรับทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="09b15-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="09b15-120">ตั้งค่าตัวเลือกในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="09b15-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="09b15-121">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="09b15-121">Option</span></span>      | <span data-ttu-id="09b15-122">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="09b15-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="09b15-123">ชนิดรอบระยะเวลาบัญชี</span><span class="sxs-lookup"><span data-stu-id="09b15-123">Period code</span></span> | <span data-ttu-id="09b15-124">เลือกรหัสช่วงวันที่บัญชีแยกประเภททั่วไปเพื่อตั้งค่าวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับกระบวนการซิงโครไนส์สำหรับกำลังการผลิตสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="09b15-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="09b15-125">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="09b15-125">Start date</span></span>  | <span data-ttu-id="09b15-126">ป้อนวันที่เริ่มต้นสำหรับกระบวนการซิงโครไนส์สำหรับกำลังการผลิตสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="09b15-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="09b15-127">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="09b15-127">End date</span></span>    | <span data-ttu-id="09b15-128">ป้อนวันที่สิ้นสุดสำหรับกระบวนการซิงโครไนส์สำหรับกำลังการผลิตสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="09b15-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="09b15-129">[![กระบวนการการซิงโครไนส์](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="09b15-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
