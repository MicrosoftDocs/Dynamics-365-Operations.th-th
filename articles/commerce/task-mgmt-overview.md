---
title: ภาพรวมของการจัดการงาน
description: หัวข้อนี้แสดงภาพรวมของการจัดการงานสำหรับผู้จัดการและผู้ปฏิบัติงานใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: 6fbd0ead6d73f4b032bdc3805fce87ec9c802535
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006171"
---
# <a name="task-management-overview"></a><span data-ttu-id="6b039-103">ภาพรวมของการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="6b039-103">Task management overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b039-104">หัวข้อนี้แสดงภาพรวมของการจัดการงานสำหรับผู้จัดการและผู้ปฏิบัติงานใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6b039-104">This topic provides an overview of task management for managers and workers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6b039-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="6b039-105">Overview</span></span>

<span data-ttu-id="6b039-106">ในสภาพแวดล้อมการขายปลีก ยากเสมอที่จะทำให้แน่ใจว่างานจะดำเนินการโดยบุคคลที่ถูกต้องในเวลาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="6b039-106">In a retail environment, it's always difficult to make sure that tasks are performed by the right person at the right time.</span></span> <span data-ttu-id="6b039-107">ผู้ขายปลีกต้องสามารถแจ้งให้ผู้ปฏิบัติงานทราบเกี่ยวกับงานที่กำลังจะมาถึงและระบุบริบททางธุรกิจที่เกี่ยวข้อง เพื่อให้สามารถดำเนินงานให้เสร็จสมบูรณ์ได้อย่างถูกต้องและทันเวลา</span><span class="sxs-lookup"><span data-stu-id="6b039-107">Retailers must be able to notify workers about upcoming tasks and provide related business context, so that the tasks can be completed correctly and on time.</span></span>

<span data-ttu-id="6b039-108">การจัดการงานเป็นคุณลักษณะที่มีประสิทธิภาพในการทำงาน Dynamics 365 Commerce ที่ช่วยให้ผู้จัดการและผู้ปฏิบัติงานสร้างรายการงาน จัดการเงื่อนไขการกำหนด ติดตามสถานะของงาน และรวมการดำเนินงานเหล่านี้ระหว่างฝ่ายสนับสนุน Commerce กับแอปพลิเคชันการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="6b039-108">Task management is a productivity feature in Dynamics 365 Commerce that lets managers and workers create task lists, manage assignment criteria, track task status, and integrate these operations between Commerce back office and point of sale (POS) applications.</span></span>

<span data-ttu-id="6b039-109">บทบาทศูนย์ควบคุมสามารถใช้การจัดการงานเพื่อสร้างรายการงานสำหรับร้านค้าปลีก และเพื่อติดตามสถานะโดยร้านค้าหรือผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="6b039-109">Headquarters personas can use task management to create task lists for retail stores, and to track status by store or worker.</span></span> <span data-ttu-id="6b039-110">นอกจากนี้ ยังสามารถสร้างงานที่เกิดซ้ำได้ (ตัวอย่างเช่น "รายการตรวจสอบการปิดบัญชีคืนวันพฤหัสบดี")</span><span class="sxs-lookup"><span data-stu-id="6b039-110">They can also create recurrent tasks (for example, "Thursday night closing checklist").</span></span>

<span data-ttu-id="6b039-111">ผู้จัดการร้านค้าสามารถใช้การจัดการงานเพื่อกำหนดงานให้กับผู้ปฏิบัติงานแต่ละคน ส่งการแจ้งเตือนเกี่ยวกับงานที่กำลังจะมาถึงหรืองานที่เลยกำหนด อัปเดตสถานะของงาน และสร้างงานวัตถุประสงค์เดียวในแอปพลิเคชัน POS</span><span class="sxs-lookup"><span data-stu-id="6b039-111">Store managers can use task management to assign tasks to individual workers, send notifications about upcoming tasks or tasks that are past due, update task status, and create single-purpose tasks in the POS application.</span></span> <span data-ttu-id="6b039-112">ผู้ปฏิบัติงานสามารถดูการแจ้งเตือน ดูรายละเอียดของงาน และอัปเดตสถานะของงานที่ POS</span><span class="sxs-lookup"><span data-stu-id="6b039-112">Workers can then see notifications, view task details, and update task status at the POS.</span></span>

<span data-ttu-id="6b039-113">ภาพประกอบต่อไปนี้แสดงสถาปัตยกรรมแนวคิดของการจัดการงานใน Commerce</span><span class="sxs-lookup"><span data-stu-id="6b039-113">The following illustration shows the conceptual architecture of task management in Commerce.</span></span>

![สถาปัตยกรรมแนวคิดเกี่ยวกับการจัดการงาน](media/Tasks-management-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="6b039-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6b039-115">Additional resources</span></span>

[<span data-ttu-id="6b039-116">ตั้งค่าคอนฟิกการจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="6b039-116">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="6b039-117">สร้างรายการงานและเพิ่มงาน</span><span class="sxs-lookup"><span data-stu-id="6b039-117">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="6b039-118">กำหนดรายการงานให้กับร้านค้าหรือพนักงาน</span><span class="sxs-lookup"><span data-stu-id="6b039-118">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="6b039-119">การจัดการงานใน POS</span><span class="sxs-lookup"><span data-stu-id="6b039-119">Task management in POS</span></span>](task-mgmt-POS.md)
