---
title: "ซิงโครไนส์งานโครงการจาก Project Service Automation"
description: "หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์งานโดยตรงจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations"
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: th-th
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="f6cc6-103">ซิงโครไนส์งานโครงการจาก Project Service Automation โดยตรงไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6cc6-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="f6cc6-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์งานโดยตรงจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6cc6-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f6cc6-105">การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชัน พร้อมใช้งานใน Dynamics 365 for Finance and Operations รุ่น 8.0</span><span class="sxs-lookup"><span data-stu-id="f6cc6-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="f6cc6-106">โฟลว์ข้อมูลสำหรับ Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6cc6-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="f6cc6-107">โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6cc6-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="f6cc6-108">เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล ช่วยให้ทิศทางของข้อมูลเกี่ยวกับงานโครงการจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6cc6-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="f6cc6-109">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6cc6-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="f6cc6-110">[![โฟลว์ข้อมูลสำหรับ Project Service Automation กับ Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="f6cc6-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="f6cc6-111">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="f6cc6-111">Template and task</span></span>

<span data-ttu-id="f6cc6-112">เมื่อต้องการเข้าถึงเท็มเพลต ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="f6cc6-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f6cc6-113">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์งานโครงการจาก Project Service Automation ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="f6cc6-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="f6cc6-114">-**ชื่อของเท็มเพลตในการรวมข้อมูล:** งานโครงการ (PSA ไปยัง Fin and Ops) -**ชื่อของงานในโครงการ:** งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="f6cc6-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="f6cc6-115">ก่อนที่การซิงโครไนส์ของงานโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการและสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="f6cc6-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="f6cc6-116">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="f6cc6-116">Entity set</span></span>

|<span data-ttu-id="f6cc6-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f6cc6-117">Project Service Automation</span></span>               | <span data-ttu-id="f6cc6-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6cc6-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="f6cc6-119">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="f6cc6-119">Project Tasks</span></span>                           | <span data-ttu-id="f6cc6-120">เอนทิตีการรวมสำหรับงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="f6cc6-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="f6cc6-121">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="f6cc6-121">Entity flow</span></span>

<span data-ttu-id="f6cc6-122">มีการจัดการงานโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations เป็นกิจกรรมโครงการ</span><span class="sxs-lookup"><span data-stu-id="f6cc6-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f6cc6-123">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="f6cc6-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="f6cc6-124">ก่อนที่การซิงโครไนส์ของงานโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการและสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="f6cc6-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="f6cc6-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="f6cc6-125">Power Query</span></span>

<span data-ttu-id="f6cc6-126">คุณต้องใช้ Microsoft Power Query เพื่อกรองข้อมูล ถ้าเป็นไปตามเงื่อนไขเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f6cc6-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="f6cc6-127">คุณมีเรกคอร์ดเฉพาะของทรัพยากรภายในงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="f6cc6-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="f6cc6-128">ถ้าคุณต้องใช้ Power Query ให้ทำตามคำแนะนำเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f6cc6-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="f6cc6-129">เท็มเพลตโครงการงาน (PSA ไปยัง Fin and Ops) มีตัวกรองเริ่มต้น เพื่อแยกเรกคอร์ดเฉพาะของทรัพยากรจากภายในงานโครงการ โดยการตั้งค่าตัวกรองใน **IsLineTask** เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="f6cc6-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="f6cc6-130">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มตัวกรองนี้</span><span class="sxs-lookup"><span data-stu-id="f6cc6-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f6cc6-131">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f6cc6-131">Template mapping in Data integration</span></span>

<span data-ttu-id="f6cc6-132">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f6cc6-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="f6cc6-133">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6cc6-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="f6cc6-134">[![การแม็ปเท็มเพลต](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="f6cc6-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


