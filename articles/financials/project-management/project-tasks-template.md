---
title: ซิงโครไนส์งานโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลงานโครงการจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations ตรงกันโดยตรง
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557935"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="09f91-103">ซิงโครไนส์งานโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09f91-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="09f91-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลงานโครงการจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations ตรงกันโดยตรง</span><span class="sxs-lookup"><span data-stu-id="09f91-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="09f91-105">การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชัน พร้อมใช้งานใน Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0</span><span class="sxs-lookup"><span data-stu-id="09f91-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="09f91-106">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้เท็มเพลตเพื่อรวมงานโครงการ ค่าใช้จ่ายประเภทธุรกรรม การประเมินชั่วโมง การประเมินค่าใช้จ่าย และค่าที่เกิดขึ้นจริงได้ และสามารถตั้งค่าคอนฟิกการล็อคฟังก์ชันได้</span><span class="sxs-lookup"><span data-stu-id="09f91-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="09f91-107">ถ้าคุณต้องรีเซ็ตการกระจายการลงบัญชี เราขอแนะนำให้ คุณติดตั้ง KB 4131710 ด้วย</span><span class="sxs-lookup"><span data-stu-id="09f91-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="09f91-108">การรวมรายการจริงพร้อมใช้งานใน Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0.1 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="09f91-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="09f91-109">โฟลว์ข้อมูลสำหรับ Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09f91-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="09f91-110">โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09f91-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="09f91-111">เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล ช่วยให้ทิศทางของข้อมูลเกี่ยวกับงานโครงการจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09f91-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="09f91-112">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09f91-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="09f91-113">[![โฟลว์ข้อมูลสำหรับ Project Service Automation กับ Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="09f91-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="09f91-114">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="09f91-114">Template and task</span></span>

<span data-ttu-id="09f91-115">เพื่อเข้าถึงเท็มเพลต ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="09f91-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="09f91-116">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์งานโครงการจาก Project Service Automation ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="09f91-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="09f91-117">**ชื่อของเท็มเพลตในการรวมข้อมูล:** งานของโครงการ (PSA ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="09f91-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="09f91-118">**ชื่อของงานในโครงการ:** งานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="09f91-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="09f91-119">ก่อนที่การซิงโครไนส์ของงานโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการและสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="09f91-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="09f91-120">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="09f91-120">Entity set</span></span>

| <span data-ttu-id="09f91-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="09f91-121">Project Service Automation</span></span> | <span data-ttu-id="09f91-122">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09f91-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="09f91-123">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="09f91-123">Project Tasks</span></span>              | <span data-ttu-id="09f91-124">เอนทิตี้การรวมสำหรับงานของโครงการ</span><span class="sxs-lookup"><span data-stu-id="09f91-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="09f91-125">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="09f91-125">Entity flow</span></span>

<span data-ttu-id="09f91-126">มีการจัดการงานโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations เป็นกิจกรรมโครงการ</span><span class="sxs-lookup"><span data-stu-id="09f91-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="09f91-127">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="09f91-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="09f91-128">ก่อนที่การซิงโครไนส์ของงานโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการและสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="09f91-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="09f91-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="09f91-129">Power Query</span></span>

<span data-ttu-id="09f91-130">คุณต้องใช้ Microsoft Power Query for Excel เพื่อกรองข้อมูล ถ้าเป็นไปตามเงื่อนไขนี้:</span><span class="sxs-lookup"><span data-stu-id="09f91-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="09f91-131">คุณมีเรกคอร์ดเฉพาะทรัพยากรในงานโครงการ</span><span class="sxs-lookup"><span data-stu-id="09f91-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="09f91-132">ถ้าคุณต้องใช้ Power Query ให้ทำตามคำแนะนำนี้:</span><span class="sxs-lookup"><span data-stu-id="09f91-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="09f91-133">เท็มเพลตงานโครงการ (PSA ไปยัง Fin and Ops) มีตัวกรองเริ่มต้นที่แยกเรกคอร์ดเฉพาะทรัพยากรจากงานโครงการ โดยการตั้งค่าตัวกรองใน **IsLineTask** เป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="09f91-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="09f91-134">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มตัวกรองนี้</span><span class="sxs-lookup"><span data-stu-id="09f91-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="09f91-135">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="09f91-135">Template mapping in Data integration</span></span>

<span data-ttu-id="09f91-136">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="09f91-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="09f91-137">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09f91-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="09f91-138">[![การแม็ปเท็มเพลต](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="09f91-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
