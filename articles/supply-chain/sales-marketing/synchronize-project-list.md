---
title: ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Supply Chain Management ไปยัง Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้โครงการจาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service
author: ChristianRytt
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5cb7f8b9a3107a7787c787ace71ab574457b1646
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828505"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="cabc9-103">ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Supply Chain Management ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="cabc9-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cabc9-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้โครงการจาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="cabc9-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="cabc9-105">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="cabc9-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cabc9-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="cabc9-106">Templates and tasks</span></span>
<span data-ttu-id="cabc9-107">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการเรียกใช้การซิงโครไนส์โครงการจาก Supply Chain Management ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="cabc9-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="cabc9-108">**เท็มเพลตในการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cabc9-108">**Template in Data integration**</span></span>
- <span data-ttu-id="cabc9-109">ผลิตภัณฑ์ (Supply Chain Management ไปยัง Field Service)</span><span class="sxs-lookup"><span data-stu-id="cabc9-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="cabc9-110">**งานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cabc9-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="cabc9-111">โครงการ</span><span class="sxs-lookup"><span data-stu-id="cabc9-111">Projects</span></span>

<span data-ttu-id="cabc9-112">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ขอโครงการจะเกิดขึ้นได้:</span><span class="sxs-lookup"><span data-stu-id="cabc9-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="cabc9-113">บัญชี (Sales ไปยัง Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="cabc9-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="cabc9-114">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="cabc9-114">Entity set</span></span>
| <span data-ttu-id="cabc9-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="cabc9-115">Field Service</span></span>           | <span data-ttu-id="cabc9-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cabc9-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="cabc9-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="cabc9-117">msdynce_externalprojects</span></span> | <span data-ttu-id="cabc9-118">โครงการ</span><span class="sxs-lookup"><span data-stu-id="cabc9-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="cabc9-119">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="cabc9-119">Entity flow</span></span>
<span data-ttu-id="cabc9-120">โครงการถูกสร้างใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cabc9-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="cabc9-121">โครงการที่มี **ชนิดโครงการ** ถูกตั้งค่าเป็น **เวลาและวัสดุ** และ **ขั้นตอนโครงการ** ถูกตั้งค่าเป็น **อยู่ระหว่างดำเนินการ** จะทำให้ข้อมูลตรงกันไปยังเอนทิตี **โครงการภายนอก** ใน Field Service ซึ่งรวมหมายเลขโครงการ ชื่อโครงการ ลำดับขั้นโครงการ และข้อมูลบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cabc9-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="cabc9-122">รายการ **โครงการภายนอก** ถูกใช้เพื่อจับคู่ใบสั่งขาย Field service กับโครงการ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cabc9-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="cabc9-123">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="cabc9-123">Field Service CRM solution</span></span>
<span data-ttu-id="cabc9-124">เอนทิตี **โครงการภายนอก** รับโครงการทั้งหมดจาก Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cabc9-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="cabc9-125">ฟิลด์ **โครงการภายนอก** ได้ถูกเพิ่มไปยังเอนทิตี **ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="cabc9-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="cabc9-126">นี่คือฟิลด์การค้นหา ดังนั้นโดยการแท็กใบสั่งงานของคุณกับโครงการ ใบสั่งขายจะถูกเชื่อมต่อไปยังโครงการภายใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cabc9-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="cabc9-127">หลังจาก **สถานะระบบ** เปลี่ยนแปลง **เปิด – อยู่ระหว่างดำเนินการ(690,970,000)** ไปยังสถานะที่สูงกว่า ฟิลด์ **โครงการภายนอก** จะถูกล็อคและคุณไม่สามารถเพิ่ม ลบ หรือเปลี่ยนแปลงค่าได้อีก</span><span class="sxs-lookup"><span data-stu-id="cabc9-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="cabc9-128">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="cabc9-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="cabc9-129">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cabc9-129">Supply Chain Management</span></span>
<span data-ttu-id="cabc9-130">เปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับโครงการเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cabc9-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cabc9-131">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cabc9-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="cabc9-132">โครงการ (Supply Chain Management ไปยัง Field Service): โครงการ</span><span class="sxs-lookup"><span data-stu-id="cabc9-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="cabc9-133">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="cabc9-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]