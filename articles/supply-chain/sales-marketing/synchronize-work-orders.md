---
title: ซิงโครไนส์ใบสั่งงานที่มีโครงการจาก Field Service ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ใบสั่งงานที่มีหมายเลขโครงการตรงกันจาก Microsoft Dynamics 365 for Field Service ไปยัง Microsoft Dynamics 365 for Finance and Operations
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2019
ms.locfileid: "836453"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="f25a9-103">ซิงโครไนส์ใบสั่งงานที่มีโครงการจาก Field Service ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f25a9-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f25a9-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ใบสั่งงานที่มีหมายเลขโครงการตรงกันจาก Microsoft Dynamics 365 for Field Service ไปยัง Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f25a9-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="f25a9-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="f25a9-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="f25a9-106">เท็มเพลต **ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Fin and Ops)** ที่ใช้ เป็นไปตามเท็มเพลต **ใบสั่งงาน (Field Service ไปยัง Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="f25a9-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="f25a9-107">สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์ใบสั่งงานใน Field Service กับใบสั่งขายใน Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)</span><span class="sxs-lookup"><span data-stu-id="f25a9-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="f25a9-108">หัวข้อนี้อธิบายความแตกต่างระหว่างสองเท็มเพลตเท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="f25a9-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="f25a9-109">**ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="f25a9-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="f25a9-110">**ใบสั่งงาน (Field Service ไปยัง Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="f25a9-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="f25a9-111">ความแตกต่างหลักที่ว่า เท็มเพลตนี้รวมการแม็ปของหมายเลขโครงการที่มอบหมายไปยังใบสั่งงานใน Field Service ซึ่งทำให้มั่นใจว่าใบสั่งขายที่สร้างใน Finance and Operations รวมหมายเลขโครงการและการออกใบแจ้งหนี้สามารถเกิดขึ้นได้ในโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f25a9-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="f25a9-112">นอกจากนี้ เท็มเพลตที่ใช้การกรองและการสอบถามขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="f25a9-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f25a9-113">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="f25a9-113">Templates and tasks</span></span>

<span data-ttu-id="f25a9-114">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="f25a9-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="f25a9-115">ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f25a9-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="f25a9-116">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="f25a9-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="f25a9-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="f25a9-117">WorkOrderHeader</span></span>
- <span data-ttu-id="f25a9-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="f25a9-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="f25a9-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="f25a9-119">WorkOrderProduct</span></span>
- <span data-ttu-id="f25a9-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="f25a9-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="f25a9-121">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="f25a9-121">Field Service CRM solution</span></span>
<span data-ttu-id="f25a9-122">มีการเพิ่มฟิลด์ **โครงการภายนอก** ไปยังเอนทิตีของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f25a9-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="f25a9-123">ฟิลด์นี้เป็นการค้นหา และซื้อการระบุป้ายใบสั่งงานของคุณกับโครงการที่มีโครงการที่ใบสั่งขายจะถูกเชื่อมต่อกับโครงการภายใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f25a9-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="f25a9-124">เมื่อ **สถานะของระบบ** เปลี่ยนแปลงจากเปิด – อยู่ระหว่างการดำเนินงาน(690,970,000) เป็นสถานะที่สูงกว่า ฟิลด์ **โครงการภายนอก** จะถูกล็อค และคุณไม่สามารถเพิ่ม ลบ หรือเปลี่ยนแปลงค่าได้</span><span class="sxs-lookup"><span data-stu-id="f25a9-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f25a9-125">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f25a9-125">Template mapping in Data integration</span></span>

<span data-ttu-id="f25a9-126">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f25a9-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="f25a9-127">ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Fin and Ops): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="f25a9-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="f25a9-128">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="f25a9-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="f25a9-129">ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Fin and Ops): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="f25a9-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="f25a9-130">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="f25a9-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="f25a9-131">ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Fin and Ops): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="f25a9-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="f25a9-132">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="f25a9-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="f25a9-133">ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Fin and Ops): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="f25a9-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="f25a9-134">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="f25a9-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
