---
title: ซิงโครไนส์การประเมินโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ซิงโครไนส์การประเมินชั่วโมงโครงการและการประเมินค่าใช้จ่ายโครงการโดยตรงจาก Microsoft Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 3b885610ac9ca8645358ba8ab6d46ab82143a534
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250495"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="0e6dd-103">ซิงโครไนส์การประเมินโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0e6dd-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0e6dd-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลการประเมินชั่วโมงโครงการและการประเมินค่าใช้จ่ายโครงการจาก Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance ตรงกันโดยตรง</span><span class="sxs-lookup"><span data-stu-id="0e6dd-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="0e6dd-105">การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชันพร้อมใช้งานในรุ่น 8.0</span><span class="sxs-lookup"><span data-stu-id="0e6dd-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="0e6dd-106">การรวมรายการจริงจะพร้อมใช้งานในรุ่น 8.0.1 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="0e6dd-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="0e6dd-107">โฟลว์ข้อมูลสำหรับ Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="0e6dd-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="0e6dd-108">การรวมโซลูชั่นจาก Project Service Automation ไปยัง Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="0e6dd-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="0e6dd-109">เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูลเปิดใช้งานลำดับข้อมูลเกี่ยวกับการประมาณการชั่วโมงของโครงการและการประมาณการค่าใช้จ่ายของโครงการจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="0e6dd-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="0e6dd-110">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="0e6dd-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="0e6dd-111">[![ลำดับข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="0e6dd-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="0e6dd-112">การประเมินชั่วโมงโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="0e6dd-113">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="0e6dd-113">Template and tasks</span></span>

<span data-ttu-id="0e6dd-114">เพื่อเข้าถึงเท็มเพลตที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-114">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="0e6dd-115">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์การประมาณการชั่วโมงของโครงการจาก Project Service Automation ไปยัง Finance:</span><span class="sxs-lookup"><span data-stu-id="0e6dd-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="0e6dd-116">**ชื่อของเท็มเพลตในการรวมข้อมูล:** การประมาณการชั่วโมงของโครงการ (PSA ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="0e6dd-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="0e6dd-117">**ชื่อของงานในโครงการ:**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="0e6dd-118">ความสัมพันธ์ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0e6dd-118">Transaction relationships</span></span>
    - <span data-ttu-id="0e6dd-119">การประเมินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0e6dd-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="0e6dd-120">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="0e6dd-120">Entity set</span></span>

| <span data-ttu-id="0e6dd-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0e6dd-121">Project Service Automation</span></span> | <span data-ttu-id="0e6dd-122">การเงิน</span><span class="sxs-lookup"><span data-stu-id="0e6dd-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="0e6dd-123">งานโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-123">Project tasks</span></span>              | <span data-ttu-id="0e6dd-124">เอนทิตี้การรวมสำหรับประมาณการชั่วโมงของโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="0e6dd-125">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="0e6dd-125">Entity flow</span></span>

<span data-ttu-id="0e6dd-126">มีการจัดการการประมาณการชั่วโมงของโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance เป็นการคาดการณ์ชั่วโมงของโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0e6dd-127">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="0e6dd-127">Prerequisites</span></span>

<span data-ttu-id="0e6dd-128">ก่อนที่การซิงโครไนส์ของการประมาณการชั่วโมงของโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="0e6dd-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="0e6dd-129">Power Query</span></span>

<span data-ttu-id="0e6dd-130">ในเท็มเพลตที่การประเมินชั่วโมงโครงการ คุณต้องใช้ Microsoft Power Query for Excel เพื่อทำให้งานเหล่านี้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="0e6dd-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="0e6dd-131">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้นที่จะใช้ เมื่อการรวมสร้างการคาดการณ์ชั่วโมงใหม่</span><span class="sxs-lookup"><span data-stu-id="0e6dd-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="0e6dd-132">กรองเรกคอร์ดเฉพาะทรัพยากรใดๆ ออก ในงานที่จะไม่รวมในการคาดการณ์ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="0e6dd-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="0e6dd-133">กรองแถวของประเภทธุรกรรมว่างใดๆ ออก</span><span class="sxs-lookup"><span data-stu-id="0e6dd-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="0e6dd-134">ความล้มเหลวในการทำงานนี้ให้เสร็จสมบูรณ์อาจส่งผลต่อการคาดการณ์ชั่วโมงที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0e6dd-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="0e6dd-135">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0e6dd-135">Set the default forecast model ID</span></span>

<span data-ttu-id="0e6dd-136">ในการอัพเดตรหัสแบบจำลองการคาดการณ์เริ่มต้นในเท็มเพลต คลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป</span><span class="sxs-lookup"><span data-stu-id="0e6dd-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="0e6dd-137">จากนั้น เลือกลิงก์ **การกรองข้อมูลและแบบสอบถามขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="0e6dd-138">ถ้าคุณกำลังใช้เท็มเพลตการประเมินชั่วโมงโครงการเริ่มต้น (PSA ไปยัง Fin and Ops) เลือก **เงื่อนไขที่แทรก** ในรายการของ **ขั้นตอนที่ใช้**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="0e6dd-139">ในรายการ **ฟังก์ชัน** แทนที่ **O\_forecast** ด้วยชื่อของรหัสแบบจำลองการคาดการณ์ที่ควรจะใช้กับการรวม</span><span class="sxs-lookup"><span data-stu-id="0e6dd-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="0e6dd-140">เท็มเพลตเริ่มต้นมีรหัสแบบจำลองการคาดการณ์จากข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="0e6dd-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="0e6dd-141">ถ้าคุณกำลังสร้างเท็มเพลตใหม่ คุณต้องเพิ่มคอลัมน์นี้</span><span class="sxs-lookup"><span data-stu-id="0e6dd-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="0e6dd-142">ใน Power Query เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข** และป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **ModelID**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="0e6dd-143">ป้อนเงื่อนไขสำหรับคอลัมน์ ที่ซึ่งถ้างานโครงการไม่ใช่ null แล้ว \<ป้อนรหัสแบบจำลองการคาดการณ์\>; นอกจากนั้นเป็น null</span><span class="sxs-lookup"><span data-stu-id="0e6dd-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="0e6dd-144">กรองเรกคอร์ดเฉพาะทรัพยากรออก</span><span class="sxs-lookup"><span data-stu-id="0e6dd-144">Filter out resource-specific records</span></span>

<span data-ttu-id="0e6dd-145">เท็มเพลตการประมาณชั่วโมงของโครงการ (PSA ไปยัง Fin and Ops) มีตัวกรองเริ่มต้นที่ลบเรกคอร์ดเฉพาะทรัพยากรใดๆ ออก</span><span class="sxs-lookup"><span data-stu-id="0e6dd-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="0e6dd-146">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มตัวกรองนี้</span><span class="sxs-lookup"><span data-stu-id="0e6dd-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="0e6dd-147">เลือกลิงก์ **การสอบถามและการกรองขั้นสูง** เพื่อกรองในคอลัมน์ **msdyn\_islinetask** เพื่อให้มีการรวมเฉพาะเรกคอร์ด **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="0e6dd-148">กรองแถวของประเภทธุรกรรมว่างออก</span><span class="sxs-lookup"><span data-stu-id="0e6dd-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="0e6dd-149">คุณต้องเพิ่มตัวกรองข้อมูลเพื่อลบแถวใดๆ ที่มีประเภทธุรกรรมที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="0e6dd-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="0e6dd-150">จำเป็นต้องมีงานนี้ โดยไม่คำนึงถึงว่าคุณกำลังใช้เท็มเพลตเริ่มต้น หรือกำลังสร้างเท็มเพลตของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="0e6dd-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="0e6dd-151">ตัวกรองข้อมูลนี้ลบแถวสรุปใดๆ จาก Project Service Automation ที่อาจเป็นเหตุให้การคาดการณ์ชั่วโมงใน Finance ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0e6dd-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="0e6dd-152">เลือกลิงก์ **การสอบถามและการกรองขั้นสูง** เพื่อกรองข้อมูลเรกคอร์ด null ออก ในคอลัมน์ **msdyn\_transactioncategory\_value**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0e6dd-153">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0e6dd-153">Template mapping in Data integration</span></span>

<span data-ttu-id="0e6dd-154">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0e6dd-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="0e6dd-155">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="0e6dd-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="0e6dd-156">[![การแม็ปเท็มเพลต](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0e6dd-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="0e6dd-157">การประเมินค่าใช้จ่ายสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="0e6dd-158">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="0e6dd-158">Template and tasks</span></span>

<span data-ttu-id="0e6dd-159">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์การประมาณค่าใช้จ่ายของโครงการจาก Project Service Automation ไปยัง Finance:</span><span class="sxs-lookup"><span data-stu-id="0e6dd-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="0e6dd-160">**ชื่อของเท็มเพลตในการรวมข้อมูล:** การประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="0e6dd-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="0e6dd-161">**ชื่อของงานในโครงการ:**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="0e6dd-162">ความสัมพันธ์ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0e6dd-162">Transaction relationships</span></span> 
    - <span data-ttu-id="0e6dd-163">การประเมินค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="0e6dd-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="0e6dd-164">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="0e6dd-164">Entity set</span></span>

| <span data-ttu-id="0e6dd-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0e6dd-165">Project Service Automation</span></span> | <span data-ttu-id="0e6dd-166">การเงิน</span><span class="sxs-lookup"><span data-stu-id="0e6dd-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="0e6dd-167">การเชื่อมต่อธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0e6dd-167">Transaction Connections</span></span>    | <span data-ttu-id="0e6dd-168">เอนทิตี้การรวมสำหรับความสัมพันธ์ของธุรกรรมของโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="0e6dd-169">รายการประเมิน</span><span class="sxs-lookup"><span data-stu-id="0e6dd-169">Estimate Lines</span></span>             | <span data-ttu-id="0e6dd-170">เอนทิตี้การรวมสำหรับประมาณการค่าใช้จ่ายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="0e6dd-171">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="0e6dd-171">Entity flow</span></span>

<span data-ttu-id="0e6dd-172">มีการจัดการการประมาณการค่าใช้จ่ายของโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance เป็นการคาดการณ์ค่าใช้จ่ายของโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0e6dd-173">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="0e6dd-173">Prerequisites</span></span>

<span data-ttu-id="0e6dd-174">ก่อนที่การซิงโครไนส์ของการประมาณค่าใช้จ่ายของโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="0e6dd-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="0e6dd-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="0e6dd-175">Power Query</span></span>

<span data-ttu-id="0e6dd-176">ในเท็มเพลตการประเมินค่าใช้จ่ายของโครงการ คุณต้องใช้ Power Query เพื่อทำงานต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="0e6dd-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="0e6dd-177">กรองเพื่อรวมเฉพาะเรกคอร์ดรายการประเมินค่าใช้จ่ายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0e6dd-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="0e6dd-178">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้นที่จะใช้ เมื่อการรวมสร้างการคาดการณ์ชั่วโมงใหม่</span><span class="sxs-lookup"><span data-stu-id="0e6dd-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="0e6dd-179">แปลงชนิดการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="0e6dd-179">Transform the billing types.</span></span>
- <span data-ttu-id="0e6dd-180">แปลงชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0e6dd-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="0e6dd-181">กรองเพื่อรวมเฉพาะรายการประเมินค่าใช้จ่ายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0e6dd-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="0e6dd-182">เท็มเพลตการประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops) มีตัวกรองข้อมูลเริ่มต้น ที่รวมรายการค่าใช้จ่ายในการรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0e6dd-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="0e6dd-183">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มตัวกรองนี้</span><span class="sxs-lookup"><span data-stu-id="0e6dd-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="0e6dd-184">เลือกงาน **ความสัมพันธ์ของธุรกรรม** และจากนั้นคลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป</span><span class="sxs-lookup"><span data-stu-id="0e6dd-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="0e6dd-185">เลือกลิงก์ **การกรองข้อมูลและแบบสอบถามขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="0e6dd-186">กรองคอลัมน์ **msdyn\_transactiontype1** เพื่อให้รวมเฉพาะ **msdyn\_estimateline**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="0e6dd-187">ตั้งค่ารหัสแบบจำลองการคาดการณ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0e6dd-187">Set the default forecast model ID</span></span>

<span data-ttu-id="0e6dd-188">ในการอัพเดตรหัสแบบจำลองการคาดการณ์เริ่มต้นในเท็มเพลต เลือกงาน **การประเมินค่าใช้จ่าย** และจากนั้น คลิกลูกศร **แม็ป** เพื่อเปิดการแม็ป</span><span class="sxs-lookup"><span data-stu-id="0e6dd-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="0e6dd-189">เลือกลิงก์ **การกรองข้อมูลและแบบสอบถามขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="0e6dd-190">ถ้าคุณกำลังใช้เท็มเพลตการประเมินค่าใช้จ่ายโครงการเริ่มต้น (PSA ไปยัง Fin and Ops) ใน Power Query เลือก **เงื่อนไขที่แทรก** แรก จากส่วน **ขั้นตอนที่ใช้**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="0e6dd-191">ในรายการ **ฟังก์ชัน** แทนที่ **O\_forecast** ด้วยชื่อของรหัสแบบจำลองการคาดการณ์ที่ควรจะใช้กับการรวม</span><span class="sxs-lookup"><span data-stu-id="0e6dd-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="0e6dd-192">เท็มเพลตเริ่มต้นมีรหัสแบบจำลองการคาดการณ์จากข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="0e6dd-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="0e6dd-193">ถ้าคุณกำลังสร้างเท็มเพลตใหม่ คุณต้องเพิ่มคอลัมน์นี้</span><span class="sxs-lookup"><span data-stu-id="0e6dd-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="0e6dd-194">ใน Power Query เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข** และป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **ModelID**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="0e6dd-195">ป้อนเงื่อนไขสำหรับคอลัมน์ ที่ซึ่งถ้ารหัสรายการประเมินไม่ใช่ null แล้ว \<ป้อนรหัสแบบจำลองการคาดการณ์\>; นอกจากนั้นเป็น null</span><span class="sxs-lookup"><span data-stu-id="0e6dd-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="0e6dd-196">แปลงชนิดการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="0e6dd-196">Transform the billing types</span></span>

<span data-ttu-id="0e6dd-197">เท็มเพลตการประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops) รวมคอลัมน์แบบมีเงื่อนไขที่ถูกใช้เพื่อแปลงชนิดการเรียกเก็บเงินที่ได้รับจาก Project Service Automation ในระหว่างการรวม</span><span class="sxs-lookup"><span data-stu-id="0e6dd-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="0e6dd-198">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มคอลัมน์แบบมีเงื่อนไขนี้</span><span class="sxs-lookup"><span data-stu-id="0e6dd-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="0e6dd-199">เลือกลิงก์ **การสอบถามและการกรองขั้นสูง** เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="0e6dd-200">ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **BillingType**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="0e6dd-201">จากนั้นป้อนเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0e6dd-201">Then enter the following condition:</span></span>

<span data-ttu-id="0e6dd-202">ถ้า **msdyn\_billingtype** = 192350000 แล้ว **ไม่สามารถเรียกเก็บค่าใช้จ่ายได้**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="0e6dd-203">นอกจากนั้นถ้า **msdyn\_billingtype** = 192350001 แล้ว **สามารถเรียกเก็บค่าใช้จ่ายได้**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="0e6dd-204">นอกจากนั้นถ้า **msdyn\_billingtype** = 192350002 แล้ว **เพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="0e6dd-205">นอกจากนั้น **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="0e6dd-206">แปลงชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0e6dd-206">Transform the transaction types</span></span>

<span data-ttu-id="0e6dd-207">เท็มเพลตการประมาณการค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops) รวมคอลัมน์แบบมีเงื่อนไขที่ถูกใช้เพื่อแปลงชนิดธุรกรรมที่ได้รับจาก Project Service Automation ในระหว่างการรวม</span><span class="sxs-lookup"><span data-stu-id="0e6dd-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="0e6dd-208">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มคอลัมน์แบบมีเงื่อนไขนี้</span><span class="sxs-lookup"><span data-stu-id="0e6dd-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="0e6dd-209">เลือกลิงก์ **การสอบถามและการกรองขั้นสูง** เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="0e6dd-210">ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **TransactionType**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="0e6dd-211">จากนั้นป้อนเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0e6dd-211">Then enter the following condition:</span></span>

<span data-ttu-id="0e6dd-212">ถ้า **msdyn\_transactiontypecode** = 192350000 แล้ว **ต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="0e6dd-213">นอกจากนั้นถ้า **msdyn\_transactiontypecode** = 192350005 แล้ว **Sales**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="0e6dd-214">นอกจากนั้น **null**</span><span class="sxs-lookup"><span data-stu-id="0e6dd-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0e6dd-215">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0e6dd-215">Template mapping in Data integration</span></span>

<span data-ttu-id="0e6dd-216">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0e6dd-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="0e6dd-217">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="0e6dd-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="0e6dd-218">[![การแม็ปเท็มเพลต](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0e6dd-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="0e6dd-219">[![การแม็ปเท็มเพลต](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="0e6dd-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
