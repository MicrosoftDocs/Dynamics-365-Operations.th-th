---
title: ออกแบบอินเทอร์เฟสการดำเนินการผลิต
description: หัวข้อนี้จะอธิบายวิธีการออกแบบเนื้อหาของอินเทอร์เฟสผู้ใช้สำหรับการตั้งค่าคอนฟิกแต่ละครั้ง
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 786ea9a3da98e9f1812b007d4301cb47680e6894
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077589"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="e9ee9-103">ออกแบบอินเทอร์เฟสการดำเนินการผลิต</span><span class="sxs-lookup"><span data-stu-id="e9ee9-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e9ee9-104">คุณสามารถออกแบบเนื้อหาของอินเทอร์เฟสผู้ใช้สำหรับการตั้งค่าคอนฟิกแต่ละครั้งที่ใช้โดยอินเทอร์เฟสการดำเนินการของพื้นที่การผลิต</span><span class="sxs-lookup"><span data-stu-id="e9ee9-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="e9ee9-105">ตัวอย่างเช่น ผู้ปฏิบัติงานในเซลล์ทำงานหนึ่งอาจจำเป็นต้องสามารถเปิดคำสั่งของงานบนชั้นการผลิต ในขณะที่อยู่ในเซลล์ทำงานอื่น ไม่จำเป็นต้องมีคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="e9ee9-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="e9ee9-106">ในกรณีนี้ ควรสร้างการตั้งค่าคอนฟิกสองครั้ง โดยมีปุ่มสำหรับเปิดไฟล์แนบเอกสารและรายการที่ไม่มีปุ่มนี้</span><span class="sxs-lookup"><span data-stu-id="e9ee9-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="e9ee9-107">ออกแบบแท็บ</span><span class="sxs-lookup"><span data-stu-id="e9ee9-107">Design a tab</span></span>

<span data-ttu-id="e9ee9-108">บนหน้า **ตั้งค่าคอนฟิกการดำเนินการของชั้นการผลิต** คุณสามารถสร้างและตั้งค่าคอนฟิกแท็บโดยเลือก **แท็บการออกแบบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e9ee9-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="e9ee9-109">แต่ละแท็บจะแบ่งออกเป็นสี่ส่วน ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e9ee9-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="e9ee9-110">![โครงร่างของแท็บ](media/pfe-tab-layout.png "โครงร่างของแท็บ")</span><span class="sxs-lookup"><span data-stu-id="e9ee9-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="e9ee9-111">องค์ประกอบต่อไปนี้จะแสดงในภาพประกอบ:</span><span class="sxs-lookup"><span data-stu-id="e9ee9-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="e9ee9-112">แถบเครื่องมือหลัก</span><span class="sxs-lookup"><span data-stu-id="e9ee9-112">Primary toolbar</span></span>
1. <span data-ttu-id="e9ee9-113">แถบเครื่องมือรอง</span><span class="sxs-lookup"><span data-stu-id="e9ee9-113">Secondary toolbar</span></span>
1. <span data-ttu-id="e9ee9-114">มุมมองหลัก</span><span class="sxs-lookup"><span data-stu-id="e9ee9-114">Main view</span></span>
1. <span data-ttu-id="e9ee9-115">มุมมองรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="e9ee9-115">Detailed view</span></span>

<span data-ttu-id="e9ee9-116">เมื่อต้องการสร้างและตั้งค่าคอนฟิกแท็บใหม่ ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9ee9-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="e9ee9-117">ไปที่ **การควบคุมการผลิต &gt; การตั้งค่า &gt; การดำเนินการผลิต**</span><span class="sxs-lookup"><span data-stu-id="e9ee9-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="e9ee9-118">เลือก **แท็บการออกแบบ** ในบานหน้าต่างการดำเนินการเพื่อเปิดหน้า **แท็บการออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="e9ee9-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="e9ee9-119">![หน้าแท็บการออกแบบ](media/pfe-design-tabs.png "หน้าแท็บการออกแบบ")</span><span class="sxs-lookup"><span data-stu-id="e9ee9-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="e9ee9-120">เลือก **สร้าง** บนหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e9ee9-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="e9ee9-121">ทำการตั้งค่าต่อไปนี้ในส่วนหัวของหน้า:</span><span class="sxs-lookup"><span data-stu-id="e9ee9-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="e9ee9-122">**ชื่อแท็บ** - ระบุชื่อสำหรับแท็บ</span><span class="sxs-lookup"><span data-stu-id="e9ee9-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="e9ee9-123">**มุมมองหลัก** - เลือกระหว่างรายการงานที่กำหนดไว้ล่วงหน้าสองรายการ (*งานที่ใช้งานอยู่* *งานทั้งหมด* หรือ *เครื่องจักรของฉัน*)</span><span class="sxs-lookup"><span data-stu-id="e9ee9-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="e9ee9-124">**มุมมองรายละเอียด** - เลือกระหว่างค่าว่างหรือ **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="e9ee9-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="e9ee9-125">ถ้าคุณเลือกค่าว่างเปล่าจะไม่มีมุมมองโดยละเอียดในแท็บ ถ้าคุณเลือก **งานรายละเอียด** มุมมองรายละเอียดจะมีคำอธิบายโดยละเอียดของงานที่เลือกไว้ในรายการงานในมุมมองหลัก</span><span class="sxs-lookup"><span data-stu-id="e9ee9-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="e9ee9-126">ในส่วน **แถบเครื่องมือหลัก** ให้เลือกปุ่มที่ควรมีอยู่ในแถบเครื่องมือหลัก</span><span class="sxs-lookup"><span data-stu-id="e9ee9-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="e9ee9-127">คอลัมน์ **การดำเนินการที่พร้อมใช้งาน** จะแสดงรายการของปุ่มทั้งหมดที่สามารถเพิ่มได้</span><span class="sxs-lookup"><span data-stu-id="e9ee9-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="e9ee9-128">คอลัมน์ **การดำเนินการที่เลือก** จะแสดงรายการของปุ่มทั้งหมดที่รวมอยู่ในการตั้งค่าคอนฟิกปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="e9ee9-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="e9ee9-129">ใช้ปุ่มต่าง ๆ ระหว่างคอลัมน์เพื่อย้ายรายการที่เลือกระหว่างคอลัมน์ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="e9ee9-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="e9ee9-130">ใช้ปุ่มขึ้นและลงถัดจากคอลัมน์ **การดำเนินการที่เลือก** เพื่อควบคุมใบสั่งที่จะแสดงปุ่มในอินเทอร์เฟสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="e9ee9-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="e9ee9-131">ในส่วน **แถบเครื่องมือ** **รอง** ให้เลือกปุ่มที่ควรมีอยู่ในแถบเครื่องมือรอง</span><span class="sxs-lookup"><span data-stu-id="e9ee9-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="e9ee9-132">คอลัมน์ **การดำเนินการที่พร้อมใช้งาน** จะแสดงรายการของปุ่มทั้งหมดที่สามารถเพิ่มได้</span><span class="sxs-lookup"><span data-stu-id="e9ee9-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="e9ee9-133">คอลัมน์ **การดำเนินการที่เลือก** จะแสดงรายการของปุ่มทั้งหมดที่รวมอยู่ในการตั้งค่าคอนฟิกปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="e9ee9-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="e9ee9-134">ใช้ปุ่มต่าง ๆ ระหว่างคอลัมน์เพื่อย้ายรายการที่เลือกระหว่างคอลัมน์ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="e9ee9-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="e9ee9-135">ใช้ปุ่มขึ้นและลงถัดจากคอลัมน์ **การดำเนินการที่เลือก** เพื่อควบคุมใบสั่งที่จะแสดงปุ่มในอินเทอร์เฟสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="e9ee9-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="e9ee9-136">เชื่อมโยงแท็บกับการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="e9ee9-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="e9ee9-137">หลังจากที่คุณออกแบบแท็บทั้งหมดที่คุณต้องการ คุณสามารถเชื่อมโยงกับการตั้งค่าคอนฟิกได้</span><span class="sxs-lookup"><span data-stu-id="e9ee9-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="e9ee9-138">ไปที่ **การควบคุมการผลิต &gt; การตั้งค่า &gt; ตั้งค่าคอนฟิกการดำเนินการผลิต**</span><span class="sxs-lookup"><span data-stu-id="e9ee9-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="e9ee9-139">![ตั้งค่าคอนฟิกการดำเนินการของระบบการผลิต](media/pfe-config-prod-floor-execution.png "ตั้งค่าคอนฟิกการดำเนินการของระบบการผลิต")</span><span class="sxs-lookup"><span data-stu-id="e9ee9-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="e9ee9-140">บนแท็บด่วน **การเลือกแท็บ** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="e9ee9-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="e9ee9-141">มีการเพิ่มแถวใหม่เข้าในกริด</span><span class="sxs-lookup"><span data-stu-id="e9ee9-141">A new row is added to the grid.</span></span> <span data-ttu-id="e9ee9-142">สำหรับแถวใหม่นี้ ให้เลือกชื่อของแท็บที่คุณต้องการเพิ่มลงในการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="e9ee9-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="e9ee9-143">ดำเนินการต่อเพื่อเพิ่มแท็บเพิ่มเติมตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="e9ee9-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="e9ee9-144">ใช้ปุ่ม **เลื่อนขึ้น** และ **เลื่อนลง** บนแถบเครื่องมือเพื่อจัดเรียงแท็บตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="e9ee9-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="e9ee9-145">แท็บจะแสดงจากซ้ายไปขวาตามลำดับที่แสดงไว้ในภาพข้างบน (แท็บด้านบนจะแสดงอยู่ทางด้านซ้ายมือ)</span><span class="sxs-lookup"><span data-stu-id="e9ee9-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>
