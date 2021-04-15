---
title: การจัดการงานใน POS
description: หัวข้อนี้จะอธิบายถึงการจัดการงานในแอปพลิเคชันการขายหน้าร้าน (POS) ใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 38ee9db94b3b222e8c0ce5d0883f47bd5d3e7d22
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796933"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="4e770-103">การจัดการงานใน POS</span><span class="sxs-lookup"><span data-stu-id="4e770-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4e770-104">หัวข้อนี้จะอธิบายถึงการจัดการงานในแอปพลิเคชันการขายหน้าร้าน (POS) ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4e770-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="4e770-105">แอปพลิเคชัน POS Dynamics 365 Commerce มีลักษณะการทำงานในการจัดการงานที่ให้ผู้จัดการร้านค้าและผู้ปฏิบัติงานจัดการงานและอัปเดตสถานะของงาน</span><span class="sxs-lookup"><span data-stu-id="4e770-105">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="4e770-106">ผู้ปฏิบัติงานในร้านค้าสามารถเข้าถึงงานได้ด้วยการเลือกไทล์ **งาน** บนโฮมเพจของ POS หรือโดยการเลือกการแจ้งเตือนของงาน</span><span class="sxs-lookup"><span data-stu-id="4e770-106">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="4e770-107">ตามค่าเริ่มต้น จะมีการใช้ผู้ปฏิบัติงานในแท็บ **งานของฉัน** ซึ่งผู้ใช้จะสามารถดูงานที่ได้รับมอบหมายได้</span><span class="sxs-lookup"><span data-stu-id="4e770-107">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="4e770-108">อย่างไรก็ตาม ผู้ใช้สามารถสลับไปยังแท็บ **งานที่พ้นกำหนดงาน** **เปิดงาน** และ **รายการงาน** ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="4e770-108">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="4e770-109">การดำเนินงานสำหรับผู้จัดการร้านค้า</span><span class="sxs-lookup"><span data-stu-id="4e770-109">Task operations for store managers</span></span>

<span data-ttu-id="4e770-110">ผู้จัดการร้านค้าสามารถดำเนินงานต่อไปนี้ในแอปพลิเคชัน POS โดยใช้ปุ่มบนแถบคำสั่ง:</span><span class="sxs-lookup"><span data-stu-id="4e770-110">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="4e770-111">**กำหนด** – กำหนดงานที่เลือกให้กับผู้ปฏิบัติงานในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="4e770-111">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="4e770-112">**สถานะของงาน** – เปลี่ยนสถานะของงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4e770-112">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="4e770-113">**ตัวกรอง** – โดยค่าเริ่มต้น จะมีการแสดงเฉพาะงานที่ใช้งานอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4e770-113">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="4e770-114">อย่างไรก็ตาม ด้วยการใช้ตัวกรอง ผู้จัดการสามารถดูงานทั้งหมดได้ แม้กระทั่งงานที่เสร็จสมบูรณ์หรือถูกยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="4e770-114">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="4e770-115">**งานใหม่** – สร้างงานภายใต้รายการงานที่มีอยู่หรือสร้างงานวัตถุประสงค์เดียว</span><span class="sxs-lookup"><span data-stu-id="4e770-115">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="4e770-116">ผู้ปฏิบัติงานร้านค้าสามารถดำเนินงานต่อไปนี้ในแอปพลิเคชัน POS โดยใช้ปุ่มบนแถบคำสั่ง:</span><span class="sxs-lookup"><span data-stu-id="4e770-116">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="4e770-117">**สถานะของงาน** – เปลี่ยนสถานะของงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4e770-117">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="4e770-118">**ตัวกรอง** – โดยค่าเริ่มต้น จะมีการแสดงเฉพาะงานที่ใช้งานอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4e770-118">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="4e770-119">อย่างไรก็ตาม ด้วยการใช้ตัวกรอง ผู้ปฏิบัติงานสามารถดูงานทั้งหมดได้ แม้กระทั่งงานที่เสร็จสมบูรณ์หรือถูกยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="4e770-119">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="4e770-120">ภาพประกอบต่อไปนี้แสดงแท็บ **งานของฉัน** ในแอปพลิเคชัน Commerce POS</span><span class="sxs-lookup"><span data-stu-id="4e770-120">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![แท็บงานของฉันในแอปพลิเคชัน Commerce POS](media/POS-task-management.png)

<span data-ttu-id="4e770-122">ภาพประกอบต่อไปนี้แสดงแท็บ **รายการงาน**</span><span class="sxs-lookup"><span data-stu-id="4e770-122">The following illustration shows the **Task lists** tab.</span></span>

![แท็บรายการงานในแอปพลิเคชัน Commerce POS](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="4e770-124">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4e770-124">Additional resources</span></span>

[<span data-ttu-id="4e770-125">ภาพรวมของการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="4e770-125">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="4e770-126">ตั้งค่าคอนฟิกการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="4e770-126">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="4e770-127">สร้างรายการงานและเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="4e770-127">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="4e770-128">กำหนดรายการงานให้กับร้านค้าหรือพนักงาน</span><span class="sxs-lookup"><span data-stu-id="4e770-128">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
