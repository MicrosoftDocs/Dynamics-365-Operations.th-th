---
title: สร้างรายการงานและเพิ่มงาน
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างรายการงานและเพิ่มงานไปยังรายการใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cca5e0efd6516d02c372e8a616b6bb0c39f3088c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006221"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="0458a-103">สร้างรายการงานและเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0458a-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างรายการงานและเพิ่มงานไปยังรายการใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0458a-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0458a-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="0458a-105">Overview</span></span>

<span data-ttu-id="0458a-106">*งาน* หมายถึง ชิ้นงานหรือการดำเนินการเฉพาะที่ผู้ใช้ต้องดำเนินการให้เสร็จสมบูรณ์ในวันหรือก่อนวันที่ครบกำหนดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="0458a-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="0458a-107">ใน Dynamics 365 Commerce งานจะมีคำแนะนำและข้อมูลโดยละเอียดเกี่ยวกับผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="0458a-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="0458a-108">รวมถึงลิงก์ไปยังการดำเนินงานของฝ่ายสนับสนุน การดำเนินงานของการขายหน้าร้าน (POS) หรือหน้าไซต์ เพื่อช่วยปรับปรุงประสิทธิภาพการทำงานและจัดหาบริบทที่เจ้าของงานต้องทำงานให้เสร็จสมบูรณ์ได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="0458a-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="0458a-109">*รายการงาน* เป็นชุดของงานที่ต้องทำให้เสร็จสมบูรณ์โดยเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="0458a-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="0458a-110">ตัวอย่างเช่น อาจมีรายการงานที่ผู้ปฏิบัติงานใหม่ต้องดำเนินการให้เสร็จสมบูรณ์ในระหว่างการเตรียมความพร้อม รายการงานสำหรับแคชเชียร์ที่ทำงานกะเย็น หรือรายการงานที่ต้องทำให้เสร็จสมบูรณ์เพื่อจัดเตรียมร้านสำหรับฤดูกาลวันหยุดที่กำลังจะมาถึง</span><span class="sxs-lookup"><span data-stu-id="0458a-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="0458a-111">ใน Commerce รายการงานทุกรายการที่มีวันที่เป้าหมายสามารถกำหนดให้กับร้านค้าหรือพนักงานจำนวนเท่าใดก็ได้ และคุณสามารถตั้งค่าคอนฟิกให้มีการเกิดซ้ำได้</span><span class="sxs-lookup"><span data-stu-id="0458a-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="0458a-112">ผู้จัดการและผู้ปฏิบัติงานสามารถสร้างรายการงานในฝ่ายสนับสนุนการค้า แล้วกำหนดให้กับชุดของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="0458a-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="0458a-113">สร้างรายการงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-113">Create a task list</span></span>

<span data-ttu-id="0458a-114">ในการสร้างรายการงาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0458a-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="0458a-115">ไปที่ **การขายปลีกและการค้า \> การจัดการงาน \> การจัดการดูแลการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="0458a-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="0458a-116">เลือก **สร้าง** แล้วป้อนค่าในฟิลด์ **ชื่อ** **คำอธิบาย** และ **เจ้าของ**</span><span class="sxs-lookup"><span data-stu-id="0458a-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="0458a-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0458a-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="0458a-118">เพิ่มงานลงในรายการงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-118">Add tasks to a task list</span></span>

<span data-ttu-id="0458a-119">เมื่อต้องการเพิ่มงานไปยังรายการงาน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="0458a-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="0458a-120">บนแท็บด่วน **งาน** ของรายการงานที่มีอยู่ ให้เลือก **สร้าง** เพื่อเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="0458a-121">ในกล่องโต้ตอบ **สร้างงานใหม่** ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับงานนั้น</span><span class="sxs-lookup"><span data-stu-id="0458a-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="0458a-122">ในฟิลด์ **ออฟเซ็ตข้อมูลที่ครบกำหนด** ให้ป้อนค่าจำนวนเต็มค่าบวกหรือค่าลบ</span><span class="sxs-lookup"><span data-stu-id="0458a-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="0458a-123">ตัวอย่างเช่น ป้อน **-2** ถ้าควรดำเนินการงานให้เสร็จสมบูรณ์ในสองวันก่อนวันที่ครบกำหนดของรายการงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="0458a-124">ในฟิลด์ **บันทึกย่อ** ให้ป้อนคำแนะนำโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="0458a-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="0458a-125">ในฟิลด์ **ผู้ติดต่อ** ให้ป้อนชื่อของผู้เชี่ยวชาญเรื่องตามเรื่องที่เจ้าของงานสามารถติดต่อได้ ถ้าเขาหรือเธอต้องการความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="0458a-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="0458a-126">ในฟิลด์ **ลิงก์งาน** ให้ป้อนลิงก์ตามลักษณะของงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="0458a-127">ถึงแม้ว่าคุณจะสามารถใช้ฟิลด์ **ที่กำหนดให้** เพื่อกำหนดงานให้กับบุคคลในขณะที่คุณกำลังสร้างรายการงานได้ เราขอแนะนำว่าคุณควรหลีกเลี่ยงการกำหนดงานระหว่างการสร้างรายการงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="0458a-128">ให้กำหนดงานหลังจากที่มีการสร้างอินสแตนซ์ของรายการสำหรับร้านค้าแต่ละร้านแทน</span><span class="sxs-lookup"><span data-stu-id="0458a-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="0458a-129">ใช้ลิงก์งานเพื่อช่วยปรับปรุงประสิทธิภาพการทำงานของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="0458a-130">Commerce จะช่วยให้คุณสามารถเชื่อมโยงงานกับการดำเนินงานของ POS เช่น การรันรายงานการขาย การดูวิดีโอการฝึกอบรมทางออนไลน์สำหรับการปฐมนิเทศพนักงานใหม่ หรือการดำเนินงานของฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="0458a-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="0458a-131">คุณลักษณะนี้จะช่วยให้เจ้าของงานได้รับข้อมูลที่จำเป็นต้องใช้ในการทำงานให้เสร็จสมบูรณ์ได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="0458a-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="0458a-132">เมื่อต้องการเพิ่มลิงก์ของงานในระหว่างที่คุณสร้างงาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0458a-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="0458a-133">บนแท็บด่วน **งาน** ของรายการงานที่มีอยู่ ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="0458a-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="0458a-134">ในกล่องโต้ตอบ **แก้ไขงาน** ในฟิลด์ **ลิงก์งาน** ให้เลือกตัวเลือกต่อไปนี้หนึ่งตัวเลือกขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="0458a-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="0458a-135">เลือก **รายการเมนู** เพื่อตั้งค่าคอนฟิกการดำเนินงานฝ่ายสนับสนุน เช่น "ชุดผลิตภัณฑ์"</span><span class="sxs-lookup"><span data-stu-id="0458a-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="0458a-136">เลือก **การดำเนินงาน POS** เพื่อตั้งค่าคอนฟิกการดำเนินงาน POS เช่น "รายงานการขาย"</span><span class="sxs-lookup"><span data-stu-id="0458a-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="0458a-137">เลือก **URL** เพื่อตั้งค่าคอนฟิก URL แบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="0458a-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="0458a-138">ภาพประกอบต่อไปนี้แสดงการเลือกลิงก์ของงานในกล่องโต้ตอบ **แก้ไขงาน**</span><span class="sxs-lookup"><span data-stu-id="0458a-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![การเลือกลิงก์งานในกล่องโต้ตอบแก้ไขงาน](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="0458a-140">ตั้งค่าคอนฟิกการดำเนินงาน POS เพื่อให้สามารถเชื่อมโยงกับงานได้</span><span class="sxs-lookup"><span data-stu-id="0458a-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="0458a-141">หากต้องการตั้งค่าคอนฟิกการดำเนินงาน POS เพื่อให้สามารถเชื่อมโยงกับงานได้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="0458a-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="0458a-142">ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> POS \> การดำเนินการ POS**</span><span class="sxs-lookup"><span data-stu-id="0458a-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="0458a-143">เลือก **แก้ไข** ค้นหาการดำเนินงาน POS และเลือกกล่องกาเครื่องหมาย **เปิดใช้งานการจัดการงาน**</span><span class="sxs-lookup"><span data-stu-id="0458a-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0458a-144">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0458a-144">Additional resources</span></span>

[<span data-ttu-id="0458a-145">ภาพรวมของการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="0458a-146">ตั้งค่าคอนฟิกการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="0458a-147">กำหนดรายการงานให้กับร้านค้าหรือพนักงาน</span><span class="sxs-lookup"><span data-stu-id="0458a-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="0458a-148">การจัดการงานใน POS</span><span class="sxs-lookup"><span data-stu-id="0458a-148">Task management in POS</span></span>](task-mgmt-POS.md)
