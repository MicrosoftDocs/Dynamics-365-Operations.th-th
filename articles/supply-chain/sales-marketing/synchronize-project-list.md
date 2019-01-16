---
title: "ซิงโครไนส์รายการโครงการจาก Finance and Operations ไปยัง Field Service"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์โครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: th-th
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="9264e-103">ซิงโครไนส์รายการโครงการจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="9264e-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9264e-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์โครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="9264e-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="9264e-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="9264e-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9264e-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="9264e-106">Templates and tasks</span></span>
<span data-ttu-id="9264e-107">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการซิงโครไนส์ของโครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="9264e-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="9264e-108">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="9264e-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="9264e-109">โครงการ (Finance and Operations ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="9264e-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="9264e-110">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="9264e-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="9264e-111">โครงการ</span><span class="sxs-lookup"><span data-stu-id="9264e-111">Projects</span></span>

<span data-ttu-id="9264e-112">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ขอโครงการจะเกิดขึ้นได้:</span><span class="sxs-lookup"><span data-stu-id="9264e-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="9264e-113">บัญชี (Sales ไปยัง Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="9264e-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="9264e-114">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="9264e-114">Entity set</span></span>
<span data-ttu-id="9264e-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9264e-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="9264e-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="9264e-116">Field Service</span></span>           | <span data-ttu-id="9264e-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9264e-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="9264e-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="9264e-118">msdynce_externalprojects</span></span> | <span data-ttu-id="9264e-119">โครงการ</span><span class="sxs-lookup"><span data-stu-id="9264e-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="9264e-120">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="9264e-120">Entity flow</span></span>
<span data-ttu-id="9264e-121">โครงการถูกสร้างใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9264e-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="9264e-122">โครงการที่มี **ชนิดโครงการ** เวลาและวัสดุ และ **ระยะโครงการ** ในกระบวนการ จะซิงโครไนซ์กับเอนทิตี **โครงการภายนอก** ใน Field Service ซึ่งรวมถึงหมายเลขโครงการ ชื่อโครงการ ระยะโครงการ และ ข้อมูลบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9264e-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="9264e-123">รายการของ **โครงการภายนอก** ใช้ในการจับคู่ใบสั่งงาน Field service กับโครงการ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9264e-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="9264e-124">โซลูชัน CRM ของ Field Service โครงการภายนอกคือเอนทิตีใหม่ที่เรียกดูโครงการทั้งหมดจากการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9264e-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="9264e-125">มีการเพิ่มฟิลด์โครงการภายนอกไปยังเอนทิตีของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="9264e-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="9264e-126">ฟิลด์นี้เป็นการค้นหา และซื้อติดป้ายลำดับงานของคุณกับโครงการที่ใบสั่งขายจะถูกเชื่อมต่อกับโครงการภายในการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="9264e-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="9264e-127">เมื่อการเปลี่ยนแปลงสถานะของระบบเปิด – อยู่ระหว่างการดำเนินงาน(690,970,000) ให้เป็นสถานะที่สูงกว่า ฟิลด์โครงการภายนอก จะถูกล็อค และคุณไม่สามารถเพิ่ม ลบ หรือเปลี่ยนแปลงค่าได้</span><span class="sxs-lookup"><span data-stu-id="9264e-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="9264e-128">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9264e-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="9264e-129">ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9264e-129">In Finance and Operations</span></span>
<span data-ttu-id="9264e-130">เปิดใช้งานการเปลี่ยนแปลงที่ติดตามสำหรับโครงการเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9264e-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9264e-131">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9264e-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="9264e-132">โครงการ (Finance and Operations ไปยัง Field Service): โครงการ</span><span class="sxs-lookup"><span data-stu-id="9264e-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="9264e-133">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="9264e-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

