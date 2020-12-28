---
title: การจัดการงานใน POS
description: หัวข้อนี้จะอธิบายถึงการจัดการงานในแอปพลิเคชันการขายหน้าร้าน (POS) Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416191"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="725a7-103">การจัดการงานใน POS</span><span class="sxs-lookup"><span data-stu-id="725a7-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="725a7-104">หัวข้อนี้จะอธิบายถึงการจัดการงานในแอปพลิเคชันการขายหน้าร้าน (POS) Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="725a7-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="725a7-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="725a7-105">Overview</span></span>

<span data-ttu-id="725a7-106">แอปพลิเคชัน POS Dynamics 365 Commerce มีลักษณะการทำงานในการจัดการงานที่ให้ผู้จัดการร้านค้าและผู้ปฏิบัติงานจัดการงานและอัปเดตสถานะของงาน</span><span class="sxs-lookup"><span data-stu-id="725a7-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="725a7-107">ผู้ปฏิบัติงานในร้านค้าสามารถเข้าถึงงานได้ด้วยการเลือกไทล์ **งาน** บนโฮมเพจของ POS หรือโดยการเลือกการแจ้งเตือนของงาน</span><span class="sxs-lookup"><span data-stu-id="725a7-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="725a7-108">ตามค่าเริ่มต้น จะมีการใช้ผู้ปฏิบัติงานในแท็บ **งานของฉัน** ซึ่งผู้ใช้จะสามารถดูงานที่ได้รับมอบหมายได้</span><span class="sxs-lookup"><span data-stu-id="725a7-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="725a7-109">อย่างไรก็ตาม ผู้ใช้สามารถสลับไปยังแท็บ **งานที่พ้นกำหนดงาน** **เปิดงาน** และ **รายการงาน** ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="725a7-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="725a7-110">การดำเนินงานสำหรับผู้จัดการร้านค้า</span><span class="sxs-lookup"><span data-stu-id="725a7-110">Task operations for store managers</span></span>

<span data-ttu-id="725a7-111">ผู้จัดการร้านค้าสามารถดำเนินงานต่อไปนี้ในแอปพลิเคชัน POS โดยใช้ปุ่มบนแถบคำสั่ง:</span><span class="sxs-lookup"><span data-stu-id="725a7-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="725a7-112">**กำหนด** – กำหนดงานที่เลือกให้กับผู้ปฏิบัติงานในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="725a7-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="725a7-113">**สถานะของงาน** – เปลี่ยนสถานะของงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="725a7-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="725a7-114">**ตัวกรอง** – โดยค่าเริ่มต้น จะมีการแสดงเฉพาะงานที่ใช้งานอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="725a7-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="725a7-115">อย่างไรก็ตาม ด้วยการใช้ตัวกรอง ผู้จัดการสามารถดูงานทั้งหมดได้ แม้กระทั่งงานที่เสร็จสมบูรณ์หรือถูกยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="725a7-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="725a7-116">**งานใหม่** – สร้างงานภายใต้รายการงานที่มีอยู่หรือสร้างงานวัตถุประสงค์เดียว</span><span class="sxs-lookup"><span data-stu-id="725a7-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="725a7-117">ผู้ปฏิบัติงานร้านค้าสามารถดำเนินงานต่อไปนี้ในแอปพลิเคชัน POS โดยใช้ปุ่มบนแถบคำสั่ง:</span><span class="sxs-lookup"><span data-stu-id="725a7-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="725a7-118">**สถานะของงาน** – เปลี่ยนสถานะของงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="725a7-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="725a7-119">**ตัวกรอง** – โดยค่าเริ่มต้น จะมีการแสดงเฉพาะงานที่ใช้งานอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="725a7-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="725a7-120">อย่างไรก็ตาม ด้วยการใช้ตัวกรอง ผู้ปฏิบัติงานสามารถดูงานทั้งหมดได้ แม้กระทั่งงานที่เสร็จสมบูรณ์หรือถูกยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="725a7-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="725a7-121">ภาพประกอบต่อไปนี้แสดงแท็บ **งานของฉัน** ในแอปพลิเคชัน Commerce POS</span><span class="sxs-lookup"><span data-stu-id="725a7-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![แท็บงานของฉันในแอปพลิเคชัน Commerce POS](media/POS-task-management.png)

<span data-ttu-id="725a7-123">ภาพประกอบต่อไปนี้แสดงแท็บ **รายการงาน**</span><span class="sxs-lookup"><span data-stu-id="725a7-123">The following illustration shows the **Task lists** tab.</span></span>

![แท็บรายการงานในแอปพลิเคชัน Commerce POS](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="725a7-125">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="725a7-125">Additional resources</span></span>

[<span data-ttu-id="725a7-126">ภาพรวมของการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="725a7-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="725a7-127">ตั้งค่าคอนฟิกการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="725a7-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="725a7-128">สร้างรายการงานและเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="725a7-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="725a7-129">กำหนดรายการงานให้กับร้านค้าหรือพนักงาน</span><span class="sxs-lookup"><span data-stu-id="725a7-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
