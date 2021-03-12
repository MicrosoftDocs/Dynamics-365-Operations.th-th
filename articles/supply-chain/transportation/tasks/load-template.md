---
title: เท็มเพลตการบรรทุก
description: หัวข้อนี้อธิบายวิธีการตั้งค่าเท็มเพลตโหลด และวิธีการเชื่อมโยงแม่แบบโหลดที่มีการโหลดใหม่
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0a4070a1dd5d53bb502ba2ab0c91dbdc90ded34d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005063"
---
# <a name="load-templates"></a><span data-ttu-id="24e5d-103">เท็มเพลตการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="24e5d-103">Load templates</span></span>

<span data-ttu-id="24e5d-104">เมื่อคุณสร้างการโหลดใหม่ คุณสามารถกำหนดแม่แบบการโหลดได้</span><span class="sxs-lookup"><span data-stu-id="24e5d-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="24e5d-105">แม่แบบโหลดที่ประกอบด้วยข้อมูลเกี่ยวกับเครื่องมือและการวัด เช่น ความสูง ความกว้าง ความลึก ปริมาตรของสินค้า</span><span class="sxs-lookup"><span data-stu-id="24e5d-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="24e5d-106">หัวข้อนี้อธิบายวิธีการตั้งค่าเท็มเพลตโหลด และวิธีการเชื่อมโยงแม่แบบโหลดที่มีการโหลดใหม่</span><span class="sxs-lookup"><span data-stu-id="24e5d-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="24e5d-107">ตั้งค่าเท็มเพลตจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="24e5d-107">Set up a load template</span></span>

1. <span data-ttu-id="24e5d-108">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> การสร้างการบรรทุก \> แม่แบบโหลด**</span><span class="sxs-lookup"><span data-stu-id="24e5d-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="24e5d-109">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแม่แบบใหม่หรือ **แก้ไข** เพื่อแก้ไขแม่แบบที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="24e5d-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="24e5d-110">ในแถวสำหรับแม่แบบใหม่หรือแม่แบบที่มีอยู่ ให้ตั้งค่าฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="24e5d-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="24e5d-111">**รหัสแม่แบบโหลด** - ให้ป้อนตัวระบุ (รหัส) สำหรับแม่แบบโหลด</span><span class="sxs-lookup"><span data-stu-id="24e5d-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="24e5d-112">**อุปกรณ์** – เลือกอุปกรณ์ที่ควรใช้ในการจัดส่งจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="24e5d-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="24e5d-113">**ความสูงของโหลด** **ความกว้างโหลด** และ **ความลึกโหลด** – ป้อนมิติของจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="24e5d-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="24e5d-114">**จำนวนงานในศูนย์การผลิตที่อนุญาตสูงสุด** และ **น้ำหนักโหลดที่อนุญาตสูงสุด** – ป้อนปริมาณสูงสุดที่อนุญาตและน้ำหนักของจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="24e5d-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="24e5d-115">**น้ำหนักรวมสูงสุดที่อนุญาต** – ป้อนน้ำหนักรวมสูงสุดที่อนุญาตสำหรับจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="24e5d-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="24e5d-116">น้ำหนักรวมของการโหลดรวมถึงน้ำหนักหีบห่อและน้ำหนักโหลด</span><span class="sxs-lookup"><span data-stu-id="24e5d-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="24e5d-117">**จำนวนชิ้นการขนส่งสูงสุดที่อนุญาต** – ป้อนจำนวนสูงสุดของการขนส่งสินค้าที่สามารถประกอบด้วยจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="24e5d-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="24e5d-118">**เรียงซ้อนโหลดบนพื้น** - เลือกกล่องกาเครื่องหมายนี้เพื่อใช้โหลดบนพื้น</span><span class="sxs-lookup"><span data-stu-id="24e5d-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="24e5d-119">ในกรณีที่มีการโหลดพื้นที่ กล่องถูกกองซ้อนจนติดเพดาน กำแพงชนกำแพงภายในคอนเทนเนอร์เพื่อใช้พื้นที่ให้มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="24e5d-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="24e5d-120">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="24e5d-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="24e5d-121">เชื่อมโยงเท็มเพลตโหลดกับการโหลดใหม่</span><span class="sxs-lookup"><span data-stu-id="24e5d-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="24e5d-122">ไปที่ **การจัดการการขนส่ง \> การวางแผน \> เวิร์กเบนช์การวางแผนการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="24e5d-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="24e5d-123">ในส่วนบนของหน้า ให้เลือกแท็บใดแท็บหนึ่งต่อไปนี้ โดยขึ้นอยู่กับชนิดของเอกสารต้นทางที่คุณกำลังสร้างจำนวนงานในศูนย์การผลิตสำหรับ **การจัดส่ง** **รายการขาย** **รายการโอนย้าย** หรือ **รายการใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="24e5d-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="24e5d-124">เลือกเอกสารเฉพาะที่จะวางแผนจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="24e5d-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="24e5d-125">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดหาและความต้องการ** ในกลุ่ม **เพิ่ม** เลือก **ไปยังการบรรทุกใหม่**</span><span class="sxs-lookup"><span data-stu-id="24e5d-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="24e5d-126">ในกล่องโต้ตอบ **แม่แบบการบรรทุก** ในฟิลด์ **รหัสแม่แบบการบรรทุก** เลือกแม่แบบที่จะนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="24e5d-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="24e5d-127">เลือก **ตกลง** เพื่อนำแม่แบบไปใช้</span><span class="sxs-lookup"><span data-stu-id="24e5d-127">Select **OK** to apply the template.</span></span>
