---
title: ซิงโครไนส์การประเมินโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลการประเมินชั่วโมงโครงการและการประเมินค่าใช้จ่ายโครงการจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations ตรงกันโดยตรง
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
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556563"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="66692-103">ซิงโครไนส์การประเมินโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="66692-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="66692-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลการประเมินชั่วโมงโครงการและการประเมินค่าใช้จ่ายโครงการจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Dynamics 365 for Finance and Operations ตรงกันโดยตรง</span><span class="sxs-lookup"><span data-stu-id="66692-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="66692-105">การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชัน พร้อมใช้งานใน Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0</span><span class="sxs-lookup"><span data-stu-id="66692-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="66692-106">การรวมรายการจริงพร้อมใช้งานใน Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0.1 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="66692-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="66692-107">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้เท็มเพลตเพื่อรวมงานโครงการ ค่าใช้จ่ายประเภทธุรกรรม การประเมินชั่วโมง การประเมินค่าใช้จ่าย และค่าที่เกิดขึ้นจริงได้ และสามารถตั้งค่าคอนฟิกการล็อคฟังก์ชันได้</span><span class="sxs-lookup"><span data-stu-id="66692-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="66692-108">ถ้าคุณต้องตั้งค่าการกระจายการลงบัญชี เราขอแนะนำให้ คุณติดตั้ง KB 4131710 ด้วย</span><span class="sxs-lookup"><span data-stu-id="66692-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="66692-109">โฟลว์ข้อมูลสำหรับ Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="66692-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="66692-110">โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="66692-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="66692-111">เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับการประมาณการชั่วโมงของโครงการและการประมาณการค่าใช้จ่ายของโครงการจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="66692-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="66692-112">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="66692-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="66692-113">[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="66692-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="66692-114">การประเมินชั่วโมงโครงการ</span><span class="sxs-lookup"><span data-stu-id="66692-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="66692-115">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="66692-115">Template and tasks</span></span>

<span data-ttu-id="66692-116">เพื่อเข้าถึงเท็มเพลตที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="66692-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="66692-117">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์การประมาณการชั่วโมงของโครงการจาก Project Service Automation ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="66692-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="66692-118">**ชื่อของเท็มเพลตในการรวมข้อมูล:** การประมาณการชั่วโมงของโครงการ (PSA ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="66692-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="66692-119">**ชื่อของงานในโครงการ:**</span><span class="sxs-lookup"><span data-stu-id="66692-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="66692-120">ความสัมพันธ์ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="66692-120">Transaction relationships</span></span>
    - <span data-ttu-id="66692-121">การประเมินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="66692-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="66692-122">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="66692-122">Entity set</span></span>

| <span data-ttu-id="66692-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="66692-123">Project Service Automation</span></span> | <span data-ttu-id="66692-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="66692-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="66692-125">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="66692-125">Project tasks</span></span>              | <span data-ttu-id="66692-126">เอนทิตี้การรวมสำหรับประมาณการชั่วโมงของโครงการ</span><span class="sxs-lookup"><span data-stu-id="66692-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="66692-127">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="66692-127">Entity flow</span></span>

<span data-ttu-id="66692-128">มีการจัดการการประมาณการชั่วโมงของโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations เป็นการคาดการณ์ชั่วโมงของโครงการ</span><span class="sxs-lookup"><span data-stu-id="66692-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="66692-129">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="66692-129">Prerequisites</span></span>

<span data-ttu-id="66692-130">ก่อนที่การซิงโครไนส์ของการประมาณการชั่วโมงของโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="66692-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="66692-131">Power Query</span><span class="sxs-lookup"><span data-stu-id="66692-131">Power Query</span></span>

<span data-ttu-id="66692-132">ในเท็มเพลตที่การประเมินชั่วโมงโครงการ คุณต้องใช้ Microsoft Power Query for Excel เพื่อทำให้งานเหล่านี้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="66692-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="66692-133">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้นที่จะใช้ เมื่อการรวมสร้างการคาดการณ์ชั่วโมงใหม่</span><span class="sxs-lookup"><span data-stu-id="66692-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="66692-134">กรองเรกคอร์ดเฉพาะทรัพยากรใดๆ ออก ในงานที่จะไม่รวมในการคาดการณ์ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="66692-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="66692-135">กรองแถวของประเภทธุรกรรมว่างใดๆ ออก</span><span class="sxs-lookup"><span data-stu-id="66692-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="66692-136">ความล้มเหลวในการทำงานนี้ให้เสร็จสมบูรณ์อาจส่งผลต่อการคาดการณ์ชั่วโมงที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="66692-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="66692-137">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="66692-137">Set the default forecast model ID</span></span>

<span data-ttu-id="66692-138">ในการอัพเดตรหัสแบบจำลองการคาดการณ์เริ่มต้นในเท็มเพลต คลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป</span><span class="sxs-lookup"><span data-stu-id="66692-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="66692-139">จากนั้น เลือกลิงก์ **การกรองข้อมูลและแบบสอบถามขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="66692-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="66692-140">ถ้าคุณกำลังใช้เท็มเพลตการประเมินชั่วโมงโครงการเริ่มต้น (PSA ไปยัง Fin and Ops) เลือก **เงื่อนไขที่แทรก** ในรายการของ **ขั้นตอนที่ใช้**</span><span class="sxs-lookup"><span data-stu-id="66692-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="66692-141">ในรายการ **ฟังก์ชัน** แทนที่ **O\_forecast** ด้วยชื่อของรหัสแบบจำลองการคาดการณ์ที่ควรจะใช้กับการรวม</span><span class="sxs-lookup"><span data-stu-id="66692-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="66692-142">เท็มเพลตเริ่มต้นมีรหัสแบบจำลองการคาดการณ์จากข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="66692-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="66692-143">ถ้าคุณกำลังสร้างเท็มเพลตใหม่ คุณต้องเพิ่มคอลัมน์นี้</span><span class="sxs-lookup"><span data-stu-id="66692-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="66692-144">ใน Power Query เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข** และป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **ModelID**</span><span class="sxs-lookup"><span data-stu-id="66692-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="66692-145">ป้อนเงื่อนไขสำหรับคอลัมน์ ที่ซึ่งถ้างานโครงการไม่ใช่ null แล้ว \<ป้อนรหัสแบบจำลองการคาดการณ์\>; นอกจากนั้นเป็น null</span><span class="sxs-lookup"><span data-stu-id="66692-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="66692-146">กรองเรกคอร์ดเฉพาะทรัพยากรออก</span><span class="sxs-lookup"><span data-stu-id="66692-146">Filter out resource-specific records</span></span>

<span data-ttu-id="66692-147">เท็มเพลตการประมาณชั่วโมงของโครงการ (PSA ไปยัง Fin and Ops) มีตัวกรองเริ่มต้นที่ลบเรกคอร์ดเฉพาะทรัพยากรใดๆ ออก</span><span class="sxs-lookup"><span data-stu-id="66692-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="66692-148">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มตัวกรองนี้</span><span class="sxs-lookup"><span data-stu-id="66692-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="66692-149">เลือกลิงก์ **การสอบถามและการกรองขั้นสูง** เพื่อกรองในคอลัมน์ **msdyn\_islinetask** เพื่อให้มีการรวมเฉพาะเรกคอร์ด **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="66692-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="66692-150">กรองแถวของประเภทธุรกรรมว่างออก</span><span class="sxs-lookup"><span data-stu-id="66692-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="66692-151">คุณต้องเพิ่มตัวกรองข้อมูลเพื่อลบแถวใดๆ ที่มีประเภทธุรกรรมที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="66692-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="66692-152">จำเป็นต้องมีงานนี้ โดยไม่คำนึงถึงว่าคุณกำลังใช้เท็มเพลตเริ่มต้น หรือกำลังสร้างเท็มเพลตของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="66692-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="66692-153">ตัวกรองข้อมูลนี้ลบแถวสรุปใดๆ จาก Project Service Automation ที่อาจทำให้การคาดการณ์ชั่วโมงใน Finance and Operations ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="66692-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="66692-154">เลือกลิงก์ **การสอบถามและการกรองขั้นสูง** เพื่อกรองข้อมูลเรกคอร์ด null ออก ในคอลัมน์ **msdyn\_transactioncategory\_value**</span><span class="sxs-lookup"><span data-stu-id="66692-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="66692-155">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="66692-155">Template mapping in Data integration</span></span>

<span data-ttu-id="66692-156">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="66692-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="66692-157">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="66692-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="66692-158">[![การแม็ปเท็มเพลต](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="66692-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="66692-159">การประเมินค่าใช้จ่ายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="66692-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="66692-160">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="66692-160">Template and tasks</span></span>

<span data-ttu-id="66692-161">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์การประมาณการค่าใช้จ่ายของโครงการจาก Project Service Automation ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="66692-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="66692-162">**ชื่อของเท็มเพลตในการรวมข้อมูล:** การประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="66692-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="66692-163">**ชื่อของงานในโครงการ:**</span><span class="sxs-lookup"><span data-stu-id="66692-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="66692-164">ความสัมพันธ์ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="66692-164">Transaction relationships</span></span> 
    - <span data-ttu-id="66692-165">การประเมินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="66692-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="66692-166">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="66692-166">Entity set</span></span>

| <span data-ttu-id="66692-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="66692-167">Project Service Automation</span></span> | <span data-ttu-id="66692-168">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="66692-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="66692-169">การเชื่อมต่อธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="66692-169">Transaction Connections</span></span>    | <span data-ttu-id="66692-170">เอนทิตี้การรวมสำหรับความสัมพันธ์ของธุรกรรมของโครงการ</span><span class="sxs-lookup"><span data-stu-id="66692-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="66692-171">รายการประเมิน</span><span class="sxs-lookup"><span data-stu-id="66692-171">Estimate Lines</span></span>             | <span data-ttu-id="66692-172">เอนทิตี้การรวมสำหรับประมาณการค่าใช้จ่ายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="66692-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="66692-173">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="66692-173">Entity flow</span></span>

<span data-ttu-id="66692-174">มีการจัดการการประมาณการค่าใช้จ่ายของโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations เป็นการคาดการณ์ค่าใช้จ่ายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="66692-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="66692-175">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="66692-175">Prerequisites</span></span>

<span data-ttu-id="66692-176">ก่อนที่การซิงโครไนส์ของการประมาณค่าใช้จ่ายของโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="66692-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="66692-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="66692-177">Power Query</span></span>

<span data-ttu-id="66692-178">ในเท็มเพลตการประเมินค่าใช้จ่ายของโครงการ คุณต้องใช้ Power Query เพื่อทำงานต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="66692-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="66692-179">กรองเพื่อรวมเฉพาะเรกคอร์ดรายการประเมินค่าใช้จ่ายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="66692-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="66692-180">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้นที่จะใช้ เมื่อการรวมสร้างการคาดการณ์ชั่วโมงใหม่</span><span class="sxs-lookup"><span data-stu-id="66692-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="66692-181">แปลงชนิดการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="66692-181">Transform the billing types.</span></span>
- <span data-ttu-id="66692-182">แปลงชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="66692-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="66692-183">กรองเพื่อรวมเฉพาะรายการประเมินค่าใช้จ่ายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="66692-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="66692-184">เท็มเพลตการประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops) มีตัวกรองข้อมูลเริ่มต้น ที่รวมรายการค่าใช้จ่ายในการรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="66692-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="66692-185">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มตัวกรองนี้</span><span class="sxs-lookup"><span data-stu-id="66692-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="66692-186">เลือกงาน **ความสัมพันธ์ของธุรกรรม** และจากนั้นคลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป</span><span class="sxs-lookup"><span data-stu-id="66692-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="66692-187">เลือกลิงก์ **การกรองข้อมูลและแบบสอบถามขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="66692-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="66692-188">กรองคอลัมน์ **msdyn\_transactiontype1** เพื่อให้รวมเฉพาะ **msdyn\_estimateline**</span><span class="sxs-lookup"><span data-stu-id="66692-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="66692-189">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="66692-189">Set the default forecast model ID</span></span>

<span data-ttu-id="66692-190">ในการอัพเดตรหัสแบบจำลองการคาดการณ์เริ่มต้นในเท็มเพลต เลือกงาน **การประเมินค่าใช้จ่าย** และจากนั้น คลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป</span><span class="sxs-lookup"><span data-stu-id="66692-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="66692-191">เลือกลิงก์ **การกรองข้อมูลและแบบสอบถามขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="66692-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="66692-192">ถ้าคุณกำลังใช้เท็มเพลตการประเมินค่าใช้จ่ายโครงการเริ่มต้น (PSA ไปยัง Fin and Ops) ใน Power Query เลือก **เงื่อนไขที่แทรก** แรก จากส่วน **ขั้นตอนที่ใช้**</span><span class="sxs-lookup"><span data-stu-id="66692-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="66692-193">ในรายการ **ฟังก์ชัน** แทนที่ **O\_forecast** ด้วยชื่อของรหัสแบบจำลองการคาดการณ์ที่ควรจะใช้กับการรวม</span><span class="sxs-lookup"><span data-stu-id="66692-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="66692-194">เท็มเพลตเริ่มต้นมีรหัสแบบจำลองการคาดการณ์จากข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="66692-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="66692-195">ถ้าคุณกำลังสร้างเท็มเพลตใหม่ คุณต้องเพิ่มคอลัมน์นี้</span><span class="sxs-lookup"><span data-stu-id="66692-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="66692-196">ใน Power Query เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข** และป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **ModelID**</span><span class="sxs-lookup"><span data-stu-id="66692-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="66692-197">ป้อนเงื่อนไขสำหรับคอลัมน์ ที่ซึ่งถ้ารหัสรายการประเมินไม่ใช่ null แล้ว \<ป้อนรหัสแบบจำลองการคาดการณ์\>; นอกจากนั้นเป็น null</span><span class="sxs-lookup"><span data-stu-id="66692-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="66692-198">แปลงชนิดการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="66692-198">Transform the billing types</span></span>

<span data-ttu-id="66692-199">เท็มเพลตการประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops) รวมคอลัมน์แบบมีเงื่อนไขที่ถูกใช้เพื่อแปลงชนิดการเรียกเก็บเงินที่ได้รับจาก Project Service Automation ในระหว่างการรวม</span><span class="sxs-lookup"><span data-stu-id="66692-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="66692-200">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มคอลัมน์แบบมีเงื่อนไขนี้</span><span class="sxs-lookup"><span data-stu-id="66692-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="66692-201">เลือกลิงก์ **การสอบถามและการกรองขั้นสูง** เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="66692-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="66692-202">ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **BillingType**</span><span class="sxs-lookup"><span data-stu-id="66692-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="66692-203">จากนั้นป้อนเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="66692-203">Then enter the following condition:</span></span>

<span data-ttu-id="66692-204">ถ้า **msdyn\_billingtype** = 192350000 แล้ว **ไม่สามารถเรียกเก็บค่าใช้จ่ายได้**</span><span class="sxs-lookup"><span data-stu-id="66692-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="66692-205">นอกจากนั้นถ้า **msdyn\_billingtype** = 192350001 แล้ว **สามารถเรียกเก็บค่าใช้จ่ายได้**</span><span class="sxs-lookup"><span data-stu-id="66692-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="66692-206">นอกจากนั้นถ้า **msdyn\_billingtype** = 192350002 แล้ว **เพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="66692-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="66692-207">นอกจากนั้น **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="66692-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="66692-208">แปลงชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="66692-208">Transform the transaction types</span></span>

<span data-ttu-id="66692-209">เท็มเพลตการประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops) รวมคอลัมน์แบบมีเงื่อนไขที่ถูกใช้เพื่อแปลงชนิดธุรกรรมที่ได้รับจาก Project Service Automation ในระหว่างการรวม</span><span class="sxs-lookup"><span data-stu-id="66692-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="66692-210">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มคอลัมน์แบบมีเงื่อนไขนี้</span><span class="sxs-lookup"><span data-stu-id="66692-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="66692-211">เลือกลิงก์ **การสอบถามและการกรองขั้นสูง** เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="66692-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="66692-212">ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **TransactionType**</span><span class="sxs-lookup"><span data-stu-id="66692-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="66692-213">จากนั้นป้อนเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="66692-213">Then enter the following condition:</span></span>

<span data-ttu-id="66692-214">ถ้า **msdyn\_transactiontypecode** = 192350000 แล้ว **ต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="66692-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="66692-215">นอกจากนั้นถ้า **msdyn\_transactiontypecode** = 192350005 แล้ว **Sales**</span><span class="sxs-lookup"><span data-stu-id="66692-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="66692-216">นอกจากนั้น **null**</span><span class="sxs-lookup"><span data-stu-id="66692-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="66692-217">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="66692-217">Template mapping in Data integration</span></span>

<span data-ttu-id="66692-218">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="66692-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="66692-219">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="66692-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="66692-220">[![การแม็ปเท็มเพลต](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="66692-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="66692-221">[![การแม็ปเท็มเพลต](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="66692-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
