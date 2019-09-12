---
title: ภาพรวมของ Project Service Automation
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับโซลูชันการรวม Project Service Automation ไปยัง Finance and Operations โซลูชันการรวมนี้ใช้คุณลักษณะการรวมข้อมูลในการซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Microsoft Dynamics 365 for Finance and Operations และ Microsoft Dynamics 365 for Project Service Automation ผ่าน Common Data Service
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85dde35033122ad234ec8efd1bddf64b950578ef
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865639"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="17df0-104">ภาพรวมของ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="17df0-104">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="17df0-105">โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Microsoft Dynamics 365 for Finance and Operations และ Microsoft Dynamics 365 for Project Service Automation ผ่าน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="17df0-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="17df0-106">เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูลเปิดใช้งานทิศทางของโครงการ สัญญาโครงการ รายการสัญญาโครงการ เหตุการณ์สำคัญของรายการสัญญาโครงการ งานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง และการประเมินค่าใช้จ่ายจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17df0-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="17df0-107">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้เท็มเพลตเพื่อรวมงานโครงการ ค่าใช้จ่ายประเภทธุรกรรม การประเมินชั่วโมง การประเมินค่าใช้จ่าย และค่าที่เกิดขึ้นจริงได้ และสามารถตั้งค่าคอนฟิกการล็อคฟังก์ชันได้</span><span class="sxs-lookup"><span data-stu-id="17df0-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="17df0-108">ถ้าคุณต้องตั้งค่าการกระจายการลงบัญชี เราขอแนะนำให้ คุณติดตั้ง KB 4131710 ด้วย</span><span class="sxs-lookup"><span data-stu-id="17df0-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="17df0-109">ถ้าคุณกำลังใช้ Finance and Operations 7.3.0 คุณต้องติดตั้ง KB 4074835</span><span class="sxs-lookup"><span data-stu-id="17df0-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="17df0-110">จากนั้น คุณจะสามารถรวมโครงการที่มีราคาคงที่ได้</span><span class="sxs-lookup"><span data-stu-id="17df0-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="17df0-111">ถ้าคุณกำลังใช้ Finance and Operations 7.3.0 และคุณกำลังนำธุรกรรมค่าธรรมเนียมมาจาก Project Service Automation คุณต้องติดตั้ง KB 4345320 เพื่อรวมค่าธรรมเนียมดังกล่าวในใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="17df0-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="17df0-112">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0 คุณจะสามารถใช้การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชันได้</span><span class="sxs-lookup"><span data-stu-id="17df0-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="17df0-113">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0.1 หรือรุ่นที่ใหม่กว่า คุณจะสามารถซิงโครไนส์ค่าที่เกิดขึ้นจริงได้</span><span class="sxs-lookup"><span data-stu-id="17df0-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="17df0-114">ก่อนที่คุณจะสามารถรวม Project Service Automation กับ Finance and Operations ได้ คุณต้องตั้งค่าคอนฟิกพารามิเตอร์การรวม Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="17df0-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="17df0-115">สำหรับข้อมูลเพิ่มเติม โปรดดู [พารามิเตอร์การรวม Project Service Automation](PSA-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="17df0-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="17df0-116">โซลูชันการรวมนี้เปิดใช้งานการซิงโครไนส์โดยตรงในสถานการณ์จำลองต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="17df0-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="17df0-117">รักษาสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17df0-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="17df0-118">สร้างโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17df0-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="17df0-119">รักษารายการสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17df0-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="17df0-120">รักษาเหตุการณ์สำคัญของรายการสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17df0-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="17df0-121">รักษางานโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17df0-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="17df0-122">รักษาประเภทธุรกรรมค่าใช้จ่ายใน Finance and Operations และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Finance and Operations ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="17df0-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="17df0-123">สร้างการประมาณการชั่วโมงของโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17df0-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="17df0-124">สร้างการประมาณการค่าใช้จ่ายของโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17df0-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="17df0-125">สร้างโครงการเวลา ค่าใช้จ่าย และค่าธรรมเนียมจริงใน Project Service Automation และสร้างธุรกรรมโครงการในสมุดรายวันการรวม Project Service Automation เพื่อที่จะสามารถลงรายการบัญชีใน Finance and Operations ได้</span><span class="sxs-lookup"><span data-stu-id="17df0-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="17df0-126">การซิงโครไนส์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="17df0-126">Data synchronization</span></span>

<span data-ttu-id="17df0-127">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลที่เป็นส่วนหนึ่งของการรวมระหว่าง Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17df0-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="17df0-128">ไม่ใช่ทุกเท็มเพลตที่พร้อมใช้งานในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="17df0-128">Not all templates are currently available.</span></span> <span data-ttu-id="17df0-129">เท็มเพลตจะถูกนำออกใช้เมื่อเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="17df0-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="17df0-130">[![การรวม Project Service Automation กับ Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="17df0-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="17df0-131">ความต้องการของระบบสำหรับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="17df0-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="17df0-132">ในการใช้โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations คุณต้องติดตั้ง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition รุ่น 7.3 ที่มีการอัพเดตแพลตฟอร์ม 12 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="17df0-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="17df0-133">ข้อกำหนดของระบบสำหรับ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="17df0-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="17df0-134">ในการใช้โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations คุณต้องติดตั้งส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="17df0-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="17df0-135">Microsoft Dynamics 365 for Project Service Automation รุ่น 9.0.0.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="17df0-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="17df0-136">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Microsoft Dynamics 365 for Sales เวอร์ชัน 1.14.0.0 (v14) หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="17df0-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="17df0-137">โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations สำหรับ Microsoft Dynamics 365 for Project Service Automation รุ่น 1.0.0.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="17df0-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="17df0-138">ติดตั้งโซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ในอินสแตนซ์ Project Service Automation ของคุณ</span><span class="sxs-lookup"><span data-stu-id="17df0-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="17df0-139">ดาวน์โหลดโซลูชันการรวม Project Service Automation ไปยัง Finance and Operations จาก [ศูนย์ดาวน์โหลด Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) และทำตามคำแนะนำที่มาพร้อมกับโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="17df0-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
