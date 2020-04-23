---
title: ซิงโครไนส์ใบสั่งงานจากกับโครงการจาก Field Service ไปยัง Supply Chain Management
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ใบสั่งงานที่มีหมายเลขโครงการตรงกันจาก Dynamics 365 Field Service ไปยัง Dynamics 365 Supply Chain Management
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5ebf23c5c831e9dad5d13c72f82eb3eeb30da853
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215872"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="64385-103">ซิงโครไนส์ใบสั่งงานจากกับโครงการจาก Field Service ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="64385-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="64385-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ใบสั่งงานที่มีหมายเลขโครงการตรงกันจาก Dynamics 365 Field Service ไปยัง Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="64385-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="64385-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="64385-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="64385-106">เท็มเพลต **ใบสั่งงานที่มีโครงการ (Field Service ไปยัง Supply Chain Management)** ที่ใช้ เป็นไปตามเท็มเพลต **ใบสั่งงาน (Field Service ไปยัง Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="64385-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="64385-107">สำหรับข้อมูลเพิ่มเติม ดู [ซิงโครไนส์ใบสั่งงานใน Field Service กับใบสั่งขายใน Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)</span><span class="sxs-lookup"><span data-stu-id="64385-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="64385-108">หัวข้อนี้อธิบายความแตกต่างระหว่างสองเท็มเพลตเท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="64385-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="64385-109">**ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="64385-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="64385-110">**ใบสั่งงาน (Field Service ไปยัง Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="64385-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="64385-111">ความแตกต่างหลักที่ว่า เท็มเพลตนี้รวมการแม็ปของหมายเลขโครงการที่มอบหมายไปยังใบสั่งงานใน Field Service ซึ่งทำให้มั่นใจว่าใบสั่งขายที่สร้างใน Supply Chain Management รวมหมายเลขโครงการ และการออกใบแจ้งหนี้สามารถเกิดขึ้นได้ในโครงการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="64385-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="64385-112">นอกจากนี้ เท็มเพลตที่ใช้การกรองและการสอบถามขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="64385-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="64385-113">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="64385-113">Templates and tasks</span></span>

<span data-ttu-id="64385-114">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="64385-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="64385-115">ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="64385-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="64385-116">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="64385-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="64385-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="64385-117">WorkOrderHeader</span></span>
- <span data-ttu-id="64385-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="64385-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="64385-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="64385-119">WorkOrderProduct</span></span>
- <span data-ttu-id="64385-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="64385-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="64385-121">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="64385-121">Field Service CRM solution</span></span>
<span data-ttu-id="64385-122">มีการเพิ่มฟิลด์ **โครงการภายนอก** ไปยังเอนทิตีของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="64385-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="64385-123">ฟิลด์นี้คือการค้นหา และซื้อการระบุป้ายใบสั่งงานของคุณกับโครงการที่ใบสั่งขายจะถูกเชื่อมต่อไปยังโครงการภายใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="64385-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="64385-124">เมื่อ **สถานะของระบบ** เปลี่ยนแปลงจากเปิด – อยู่ระหว่างการดำเนินงาน(690,970,000) เป็นสถานะที่สูงกว่า ฟิลด์ **โครงการภายนอก** จะถูกล็อค และคุณไม่สามารถเพิ่ม ลบ หรือเปลี่ยนแปลงค่าได้</span><span class="sxs-lookup"><span data-stu-id="64385-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="64385-125">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="64385-125">Template mapping in Data integration</span></span>

<span data-ttu-id="64385-126">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="64385-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="64385-127">ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="64385-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="64385-128">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="64385-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="64385-129">ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="64385-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="64385-130">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="64385-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="64385-131">ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="64385-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="64385-132">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="64385-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="64385-133">ใบสั่งงานกับโครงการ (Field Service ไปยัง Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="64385-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="64385-134">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="64385-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
