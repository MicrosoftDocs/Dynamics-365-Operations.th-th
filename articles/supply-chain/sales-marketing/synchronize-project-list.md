---
title: ซิงโครไนส์รายการโครงการจาก Finance and Operations ไปยัง Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้โครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1525888"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="524a5-103">ซิงโครไนส์รายการโครงการจาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="524a5-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="524a5-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้โครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="524a5-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="524a5-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="524a5-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="524a5-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="524a5-106">Templates and tasks</span></span>
<span data-ttu-id="524a5-107">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการทำให้ข้อมูลตรงกันของโครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="524a5-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="524a5-108">**เท็มเพลตในการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="524a5-108">**Template in Data integration**</span></span>
- <span data-ttu-id="524a5-109">โครงการ (Fin and Ops ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="524a5-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="524a5-110">**งานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="524a5-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="524a5-111">โครงการ</span><span class="sxs-lookup"><span data-stu-id="524a5-111">Projects</span></span>

<span data-ttu-id="524a5-112">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ขอโครงการจะเกิดขึ้นได้:</span><span class="sxs-lookup"><span data-stu-id="524a5-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="524a5-113">บัญชี (Sales ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="524a5-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="524a5-114">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="524a5-114">Entity set</span></span>
| <span data-ttu-id="524a5-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="524a5-115">Field Service</span></span>           | <span data-ttu-id="524a5-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="524a5-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="524a5-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="524a5-117">msdynce_externalprojects</span></span> | <span data-ttu-id="524a5-118">โครงการ</span><span class="sxs-lookup"><span data-stu-id="524a5-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="524a5-119">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="524a5-119">Entity flow</span></span>
<span data-ttu-id="524a5-120">โครงการถูกสร้างใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="524a5-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="524a5-121">โครงการที่มี **ชนิดโครงการ** ถูกตั้งค่าเป็น **เวลาและวัสดุ** และ **ขั้นตอนโครงการ** ถูกตั้งค่าเป็น **อยู่ระหว่างดำเนินการ** จะทำให้ข้อมูลตรงกันไปยังเอนทิตี **โครงการภายนอก** ใน Field Service ซึ่งรวมหมายเลขโครงการ ชื่อโครงการ ลำดับขั้นโครงการ และข้อมูลบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="524a5-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="524a5-122">รายการ **โครงการภายนอก** ถูกใช้เพื่อจับคู่ใบสั่งขาย Field service กับโครงการ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="524a5-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="524a5-123">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="524a5-123">Field Service CRM solution</span></span>
<span data-ttu-id="524a5-124">เอนทิตี **โครงการภายนอก** รับโครงการทั้งหมดจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="524a5-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="524a5-125">ฟิลด์ **โครงการภายนอก** ได้ถูกเพิ่มไปยังเอนทิตี **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="524a5-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="524a5-126">นี่คือฟิลด์การค้นหา ดังนั้นโดยการแท็กใบสั่งงานของคุณกับโครงการ ใบสั่งขายจะถูกเชื่อมต่อไปยังโครงการภายใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="524a5-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="524a5-127">หลังจาก **สถานะระบบ** เปลี่ยนแปลง **เปิด – อยู่ระหว่างดำเนินการ(690,970,000)** ไปยังสถานะที่สูงกว่า ฟิลด์ **โครงการภายนอก** จะถูกล็อคและคุณไม่สามารถเพิ่ม ลบ หรือเปลี่ยนแปลงค่าได้อีก</span><span class="sxs-lookup"><span data-stu-id="524a5-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="524a5-128">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="524a5-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="524a5-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="524a5-129">Finance and Operations</span></span>
<span data-ttu-id="524a5-130">เปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับโครงการเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="524a5-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="524a5-131">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="524a5-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="524a5-132">โครงการ (Fin and Ops ไปยัง Field Service): โครงการ</span><span class="sxs-lookup"><span data-stu-id="524a5-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="524a5-133">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="524a5-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
