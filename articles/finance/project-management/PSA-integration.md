---
title: ภาพรวมของ Project Service Automation
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับ Dynamics 365 Project Service Automation to Dynamics 365 Finance integration solution
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250564"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="8ef45-103">ภาพรวมของ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8ef45-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8ef45-104">The Project Service Automation to Finance integration solution ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Dynamics 365 Finance และ Dynamics 365 Project Service Automation ผ่าน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8ef45-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="8ef45-105">เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูลเปิดใช้งานทิศทางของโครงการ สัญญาโครงการ รายการสัญญาโครงการ เหตุการณ์สำคัญของรายการสัญญาโครงการ งานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง และการประเมินค่าใช้จ่ายจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="8ef45-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="8ef45-106">ถ้าคุณกำลังใช้รุ่น 7.3.0 คุณต้องติดตั้ง KB 4074835</span><span class="sxs-lookup"><span data-stu-id="8ef45-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="8ef45-107">จากนั้น คุณจะสามารถรวมโครงการที่มีราคาคงที่ได้</span><span class="sxs-lookup"><span data-stu-id="8ef45-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="8ef45-108">ถ้าคุณกำลังใช้รุ่น 7.3.0 และคุณกำลังนำธุรกรรมค่าธรรมเนียมมาจาก Project Service Automation คุณต้องติดตั้ง KB 4345320 เพื่อรวมค่าธรรมเนียมดังกล่าวในใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="8ef45-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="8ef45-109">ถ้าคุณกำลังใช้รุ่น 8.0 คุณจะสามารถใช้การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชันได้</span><span class="sxs-lookup"><span data-stu-id="8ef45-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="8ef45-110">ถ้าคุณกำลังใช้รุ่น 8.0.1 หรือรุ่นที่ใหม่กว่า คุณจะสามารถซิงโครไนส์ค่าที่เกิดขึ้นจริงได้</span><span class="sxs-lookup"><span data-stu-id="8ef45-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="8ef45-111">ก่อนที่คุณจะสามารถรวม Project Service Automation Finance and Operations ได้ คุณต้องตั้งค่าคอนฟิกพารามิเตอร์การรวม Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8ef45-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="8ef45-112">สำหรับข้อมูลเพิ่มเติม โปรดดู [พารามิเตอร์การรวม Project Service Automation](PSA-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="8ef45-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="8ef45-113">โซลูชันการรวมนี้เปิดใช้งานการซิงโครไนส์โดยตรงในสถานการณ์จำลองต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8ef45-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="8ef45-114">รักษาสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="8ef45-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ef45-115">สร้างโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="8ef45-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ef45-116">รักษารายการสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="8ef45-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ef45-117">รักษาเหตุการณ์สำคัญของรายการสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="8ef45-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ef45-118">รักษางานโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="8ef45-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ef45-119">รักษาประเภทธุรกรรมค่าใช้จ่ายใน Finance และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Finance ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8ef45-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="8ef45-120">สร้างการประเมินชั่วโมงของโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="8ef45-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ef45-121">สร้างการเมินค่าใช้จ่ายโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="8ef45-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8ef45-122">สร้างระยะเวลาโครงการ ค่าใช้จ่าย และค่าธรรมเนียมจริงใน Project Service Automation และสร้างธุรกรรมโครงการในสมุดรายวันการรวม Project Service Automation เพื่อที่จะสามารถลงรายการบัญชีใน Finance ได้</span><span class="sxs-lookup"><span data-stu-id="8ef45-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="8ef45-123">การซิงโครไนส์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8ef45-123">Data synchronization</span></span>

<span data-ttu-id="8ef45-124">ภาพประกอบต่อไปนี้แสดงว่าข้อมูลถูกซิงโครไนส์อย่างไรโดยเป็นส่วนหนึ่งของการรวมระหว่าง Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="8ef45-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="8ef45-125">ไม่ใช่ทุกเท็มเพลตที่พร้อมใช้งานในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="8ef45-125">Not all templates are currently available.</span></span> <span data-ttu-id="8ef45-126">เท็มเพลตจะถูกนำออกใช้เมื่อเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="8ef45-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="8ef45-127">[![การรวม Project Service Automation กับ Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="8ef45-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="8ef45-128">ความต้องการของระบบสำหรับ Finance</span><span class="sxs-lookup"><span data-stu-id="8ef45-128">System requirements for Finance</span></span>

<span data-ttu-id="8ef45-129">ในการใช้ the Project Service Automation ไปจนถึง Finance integration solution คุณต้องติดตั้ง Enterprise Edition 7.3 ที่มีการอัพเดตแพลตฟอร์ม 12 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="8ef45-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="8ef45-130">ข้อกำหนดของระบบสำหรับ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8ef45-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="8ef45-131">ในการใช้ the Project Service Automation ไปจนถึง Finance integration solution คุณต้องติดตั้งส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8ef45-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="8ef45-132">Dynamics 365 Project Service Automation รุ่น 9.0.0.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="8ef45-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="8ef45-133">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดสำหรับ Dynamics 365 Sales รุ่น 1.14.0.0 (v14) หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="8ef45-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="8ef45-134">Project Service Automation ไปจนถึง Finance solution สำหรับ Dynamics 365 Project Service Automation รุ่น 1.0.0.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="8ef45-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="8ef45-135">ติดตั้ง the Project Service Automation ไปจนถึงโซลูชันการรวม Finance ในอินสแตนซ์ Project Service Automation ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8ef45-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="8ef45-136">ดาวน์โหลด Project Service Automation ไปจนถึงโซลูชันการรวม Finance จาก [ศูนย์ดาวน์โหลด Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) และทำตามคำแนะนำที่มาพร้อมกับโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="8ef45-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
