---
title: Project Service Automation
description: "โซลูชันนี้ใช้คุณลักษณะการรวมข้อมูลในการซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Microsoft Dynamics 365 for Finance and Operations และ Microsoft Dynamics 365 for Project Service Automation ผ่าน Common Data Service (CDS)"
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: th-th
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="ab3f6-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ab3f6-103">Project Service Automation</span></span>

<span data-ttu-id="ab3f6-104">โซลูชันการรวม Project Service Automation กับ Finance and Operations ใช้คุณลักษณะการรวมข้อมูลในการซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Microsoft Dynamics 365 for Finance and Operations และ Microsoft Dynamics 365 for Project Service Automation ผ่าน Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="ab3f6-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="ab3f6-105">เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมเปิดใช้งานทิศทางของโครงการ สัญญาโครงการ รายการสัญญาโครงการ เหตุการณ์สำคัญของรายการสัญญาโครงการ งานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง และการประเมินค่าใช้จ่ายจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab3f6-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="ab3f6-106">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 คุณต้องติดตั้ง KB 4074835</span><span class="sxs-lookup"><span data-stu-id="ab3f6-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="ab3f6-107">ซึ่งจะทำให้คุณสามารถรวมโครงการที่มีราคาคงที่ได้</span><span class="sxs-lookup"><span data-stu-id="ab3f6-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="ab3f6-108">ถ้าคุณกำลังใช้ Dynamics 365 for Finance and Operations รุ่น 8.0 คุณจะสามารถใช้การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชันได้</span><span class="sxs-lookup"><span data-stu-id="ab3f6-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="ab3f6-109">ถ้าคุณกำลังใช้ Dynamics 365 for Finance and Operations รุ่น 8.0.1 คุณจะสามารถซิงโครไนส์ค่าที่เกิดขึ้นจริงได้</span><span class="sxs-lookup"><span data-stu-id="ab3f6-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="ab3f6-110">ถ้าคุณกำลังใช้ Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้เท็มเพลตเพื่อรวมงานโครงการ ค่าใช้จ่ายประเภทธุรกรรม การประเมินชั่วโมง การประเมินค่าใช้จ่าย และค่าที่เกิดขึ้นจริงได้ และสามารถตั้งค่าคอนฟิกการล็อคฟังก์ชันได้</span><span class="sxs-lookup"><span data-stu-id="ab3f6-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="ab3f6-111">ถ้าคุณต้องตั้งค่าการกระจายการลงบัญชี เราขอแนะนำให้ คุณติดตั้ง KB 4131710 ด้วย</span><span class="sxs-lookup"><span data-stu-id="ab3f6-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="ab3f6-112">ก่อนที่คุณจะสามารถรวม Project Service Automation กับ Finance and Operations ได้ คุณต้องตั้งค่าคอนฟิกพารามิเตอร์การรวม Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ab3f6-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="ab3f6-113">สำหรับข้อมูลเพิ่มเติม โปรดดูพารามิเตอร์การรวม Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ab3f6-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="ab3f6-114">โซลูชันการรวมนี้เปิดใช้งานการซิงโครไนส์โดยตรงในสถานการณ์จำลองต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ab3f6-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="ab3f6-115">รักษาสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab3f6-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="ab3f6-116">สร้างโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab3f6-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="ab3f6-117">รักษารายการสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab3f6-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="ab3f6-118">รักษาเหตุการณ์สำคัญของรายการสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab3f6-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="ab3f6-119">รักษางานโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab3f6-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="ab3f6-120">รักษาประเภทธุรกรรมค่าใช้จ่ายใน Finance and Operations และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Finance and Operations ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ab3f6-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="ab3f6-121">สร้างการประมาณการชั่วโมงของโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab3f6-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="ab3f6-122">สร้างการประมาณการค่าใช้จ่ายของโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab3f6-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="ab3f6-123">การซิงโครไนส์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ab3f6-123">Data synchronization</span></span>
<span data-ttu-id="ab3f6-124">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลที่เป็นส่วนหนึ่งของการรวมระหว่าง Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab3f6-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="ab3f6-125">ไม่ใช่ทุกเท็มเพลตที่พร้อมใช้งานในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="ab3f6-125">Not all templates are currently available.</span></span> <span data-ttu-id="ab3f6-126">เท็มเพลตจะถูกนำออกใช้เมื่อเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="ab3f6-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="ab3f6-127">[![การรวม Project Service Automation กับ Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="ab3f6-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="ab3f6-128">ความต้องการของระบบสำหรับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab3f6-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="ab3f6-129">ในการใช้โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations คุณต้องติดตั้ง Microsoft Dynamics 365 for Finance and Operations, Enterprise edition รุ่น 7.3 ที่มีการอัพเดตแพลตฟอร์ม 12 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="ab3f6-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="ab3f6-130">ข้อกำหนดของระบบสำหรับ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ab3f6-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="ab3f6-131">ในการใช้โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations คุณต้องติดตั้งส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ab3f6-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="ab3f6-132">Microsoft Dynamics 365 for Project Service Automation รุ่น 9.0.0.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="ab3f6-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="ab3f6-133">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Dynamics 365 for Sales เวอร์ชัน 1.14.0.0 (v14) หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="ab3f6-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="ab3f6-134">โซลูชัน Project Service Automation ไปยัง Operations solution สำหรับ Dynamics 365 for Project Service Automation รุ่น 1.0.0.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="ab3f6-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="ab3f6-135">ติดตั้งโซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ในอินสแตนซ์ Project Service Automation ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ab3f6-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



