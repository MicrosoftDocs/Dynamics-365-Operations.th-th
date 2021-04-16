---
title: สร้างรายการงานและเพิ่มงาน
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างรายการงานและเพิ่มงานไปยังรายการใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a0e49d1eced3bb62e78c630b137a5b86121682f3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795248"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="a28bf-103">สร้างรายการงานและเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a28bf-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างรายการงานและเพิ่มงานไปยังรายการใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a28bf-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a28bf-105">*งาน* หมายถึง ชิ้นงานหรือการดำเนินการเฉพาะที่ผู้ใช้ต้องดำเนินการให้เสร็จสมบูรณ์ในวันหรือก่อนวันที่ครบกำหนดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a28bf-105">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="a28bf-106">ใน Dynamics 365 Commerce งานจะมีคำแนะนำและข้อมูลโดยละเอียดเกี่ยวกับผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="a28bf-106">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="a28bf-107">รวมถึงลิงก์ไปยังการดำเนินงานของฝ่ายสนับสนุน การดำเนินงานของการขายหน้าร้าน (POS) หรือหน้าไซต์ เพื่อช่วยปรับปรุงประสิทธิภาพการทำงานและจัดหาบริบทที่เจ้าของงานต้องทำงานให้เสร็จสมบูรณ์ได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a28bf-107">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="a28bf-108">*รายการงาน* เป็นชุดของงานที่ต้องทำให้เสร็จสมบูรณ์โดยเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="a28bf-108">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="a28bf-109">ตัวอย่างเช่น อาจมีรายการงานที่ผู้ปฏิบัติงานใหม่ต้องดำเนินการให้เสร็จสมบูรณ์ในระหว่างการเตรียมความพร้อม รายการงานสำหรับแคชเชียร์ที่ทำงานกะเย็น หรือรายการงานที่ต้องทำให้เสร็จสมบูรณ์เพื่อจัดเตรียมร้านสำหรับฤดูกาลวันหยุดที่กำลังจะมาถึง</span><span class="sxs-lookup"><span data-stu-id="a28bf-109">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="a28bf-110">ใน Commerce รายการงานทุกรายการที่มีวันที่เป้าหมายสามารถกำหนดให้กับร้านค้าหรือพนักงานจำนวนเท่าใดก็ได้ และคุณสามารถตั้งค่าคอนฟิกให้มีการเกิดซ้ำได้</span><span class="sxs-lookup"><span data-stu-id="a28bf-110">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="a28bf-111">ผู้จัดการและผู้ปฏิบัติงานสามารถสร้างรายการงานในฝ่ายสนับสนุนการค้า แล้วกำหนดให้กับชุดของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="a28bf-111">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="a28bf-112">สร้างรายการงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-112">Create a task list</span></span>

<span data-ttu-id="a28bf-113">ในการสร้างรายการงาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a28bf-113">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="a28bf-114">ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> การจัดการดูแลการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="a28bf-114">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="a28bf-115">เลือก **สร้าง** แล้วป้อนค่าในฟิลด์ **ชื่อ** **คำอธิบาย** และ **เจ้าของ**</span><span class="sxs-lookup"><span data-stu-id="a28bf-115">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="a28bf-116">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a28bf-116">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="a28bf-117">เพิ่มงานลงในรายการงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-117">Add tasks to a task list</span></span>

<span data-ttu-id="a28bf-118">เมื่อต้องการเพิ่มงานไปยังรายการงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a28bf-118">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="a28bf-119">บนแท็บด่วน **งาน** ของรายการงานที่มีอยู่ ให้เลือก **สร้าง** เพื่อเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-119">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="a28bf-120">ในกล่องโต้ตอบ **สร้างงานใหม่** ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับงานนั้น</span><span class="sxs-lookup"><span data-stu-id="a28bf-120">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="a28bf-121">ในฟิลด์ **ออฟเซ็ตข้อมูลที่ครบกำหนด** ให้ป้อนค่าจำนวนเต็มค่าบวกหรือค่าลบ</span><span class="sxs-lookup"><span data-stu-id="a28bf-121">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="a28bf-122">ตัวอย่างเช่น ป้อน **-2** ถ้าควรดำเนินการงานให้เสร็จสมบูรณ์ในสองวันก่อนวันที่ครบกำหนดของรายการงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-122">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="a28bf-123">ในฟิลด์ **บันทึกย่อ** ให้ป้อนคำแนะนำโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="a28bf-123">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="a28bf-124">ในฟิลด์ **ผู้ติดต่อ** ให้ป้อนชื่อของผู้เชี่ยวชาญเรื่องตามเรื่องที่เจ้าของงานสามารถติดต่อได้ ถ้าเขาหรือเธอต้องการความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="a28bf-124">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="a28bf-125">ในฟิลด์ **ลิงก์งาน** ให้ป้อนลิงก์ตามลักษณะของงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-125">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="a28bf-126">ถึงแม้ว่าคุณจะสามารถใช้ฟิลด์ **ที่กำหนดให้** เพื่อกำหนดงานให้กับบุคคลในขณะที่คุณกำลังสร้างรายการงานได้ เราขอแนะนำว่าคุณควรหลีกเลี่ยงการกำหนดงานระหว่างการสร้างรายการงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-126">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="a28bf-127">ให้กำหนดงานหลังจากที่มีการสร้างอินสแตนซ์ของรายการสำหรับร้านค้าแต่ละร้านแทน</span><span class="sxs-lookup"><span data-stu-id="a28bf-127">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="a28bf-128">ใช้ลิงก์งานเพื่อช่วยปรับปรุงประสิทธิภาพการทำงานของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-128">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="a28bf-129">Commerce จะช่วยให้คุณสามารถเชื่อมโยงงานกับการดำเนินงานของ POS เช่น การรันรายงานการขาย การดูวิดีโอการฝึกอบรมทางออนไลน์สำหรับการปฐมนิเทศพนักงานใหม่ หรือการดำเนินงานของฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a28bf-129">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="a28bf-130">คุณลักษณะนี้จะช่วยให้เจ้าของงานได้รับข้อมูลที่จำเป็นต้องใช้ในการทำงานให้เสร็จสมบูรณ์ได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a28bf-130">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="a28bf-131">เมื่อต้องการเพิ่มลิงก์ของงานในระหว่างที่คุณสร้างงาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a28bf-131">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="a28bf-132">บนแท็บด่วน **งาน** ของรายการงานที่มีอยู่ ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a28bf-132">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="a28bf-133">ในกล่องโต้ตอบ **แก้ไขงาน** ในฟิลด์ **ลิงก์งาน** ให้เลือกตัวเลือกต่อไปนี้หนึ่งตัวเลือกขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="a28bf-133">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="a28bf-134">เลือก **รายการเมนู** เพื่อตั้งค่าคอนฟิกการดำเนินงานฝ่ายสนับสนุน เช่น "ชุดผลิตภัณฑ์"</span><span class="sxs-lookup"><span data-stu-id="a28bf-134">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="a28bf-135">เลือก **การดำเนินงาน POS** เพื่อตั้งค่าคอนฟิกการดำเนินงาน POS เช่น "รายงานการขาย"</span><span class="sxs-lookup"><span data-stu-id="a28bf-135">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="a28bf-136">เลือก **URL** เพื่อตั้งค่าคอนฟิก URL แบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="a28bf-136">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="a28bf-137">ภาพประกอบต่อไปนี้แสดงการเลือกลิงก์ของงานในกล่องโต้ตอบ **แก้ไขงาน**</span><span class="sxs-lookup"><span data-stu-id="a28bf-137">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![การเลือกลิงก์งานในกล่องโต้ตอบแก้ไขงาน](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="a28bf-139">ตั้งค่าคอนฟิกการดำเนินงาน POS เพื่อให้สามารถเชื่อมโยงกับงานได้</span><span class="sxs-lookup"><span data-stu-id="a28bf-139">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="a28bf-140">หากต้องการตั้งค่าคอนฟิกการดำเนินงาน POS เพื่อให้สามารถเชื่อมโยงกับงานได้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a28bf-140">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="a28bf-141">ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> POS \> การดำเนินการ POS**</span><span class="sxs-lookup"><span data-stu-id="a28bf-141">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="a28bf-142">เลือก **แก้ไข** ค้นหาการดำเนินงาน POS และเลือกกล่องกาเครื่องหมาย **เปิดใช้งานการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="a28bf-142">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a28bf-143">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a28bf-143">Additional resources</span></span>

[<span data-ttu-id="a28bf-144">ภาพรวมของการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-144">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="a28bf-145">ตั้งค่าคอนฟิกการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-145">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="a28bf-146">กำหนดรายการงานให้กับร้านค้าหรือพนักงาน</span><span class="sxs-lookup"><span data-stu-id="a28bf-146">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="a28bf-147">การจัดการงานใน POS</span><span class="sxs-lookup"><span data-stu-id="a28bf-147">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
