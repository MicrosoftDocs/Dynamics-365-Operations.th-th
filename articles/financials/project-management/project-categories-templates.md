---
title: ปซิงโครไนส์ระเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลประเภทค่าใช้จ่ายโครงการระหว่าง Microsoft Dynamics 365 for Finance and Operations และ Microsoft Dynamics 365 for Project Service Automation ตรงกัน
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 90d640bb3eea909238b4ff032fcdb3854014e65e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838378"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="cc2b4-103">ปซิงโครไนส์ระเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc2b4-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cc2b4-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลประเภทค่าใช้จ่ายโครงการระหว่าง Microsoft Dynamics 365 for Finance and Operations และ Microsoft Dynamics 365 for Project Service Automation ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="cc2b4-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="cc2b4-105">การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชัน พร้อมใช้งานใน Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0</span><span class="sxs-lookup"><span data-stu-id="cc2b4-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="cc2b4-106">การรวมรายการจริงพร้อมใช้งานใน Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0.1 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="cc2b4-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="cc2b4-107">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้เท็มเพลตเพื่อรวมงานโครงการ ค่าใช้จ่ายประเภทธุรกรรม การประเมินชั่วโมง การประเมินค่าใช้จ่าย และค่าที่เกิดขึ้นจริงได้ และสามารถตั้งค่าคอนฟิกการล็อคฟังก์ชันได้</span><span class="sxs-lookup"><span data-stu-id="cc2b4-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="cc2b4-108">ถ้าคุณต้องตั้งค่าการกระจายการลงบัญชี เราขอแนะนำให้ คุณติดตั้ง KB 4131710 ด้วย</span><span class="sxs-lookup"><span data-stu-id="cc2b4-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="cc2b4-109">โฟลว์ข้อมูลสำหรับ Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2b4-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="cc2b4-110">โซลูชันการรวม Project Service Automation และ Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2b4-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="cc2b4-111">เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับธุรกรรมค่าใช้จ่ายของโครงการระหว่าง Finance and Operations และ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc2b4-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="cc2b4-112">ถ้าประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Finance and Operations ในตอนแรกโฟลว์การรวมมาจาก Finance and Operations ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc2b4-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="cc2b4-113">จากนั้น รหัสการรวมของระเภทค่าใช้จ่ายของโครงการถูกปรับปรุงผ่านทางการซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2b4-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="cc2b4-114">ถ้าประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Project Service Automation ในตอนแรกโฟลว์การรวมมาจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2b4-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="cc2b4-115">ประเภทโครงการต้องถูกตั้งค่าคอนฟิกใน Finance and Operations อยู่แล้ว ก่อนการซิงโครไนส์จาก Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc2b4-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="cc2b4-116">จากนั้น ซิงโครไนส์จาก Finance and Operations กลับไปยัง Project Service Automation และจากนั้นจาก Project Service Automation ไปยัง Finance and Operations อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="cc2b4-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="cc2b4-117">ด้วยวิธีนี้ คุณช่วยรับประกันว่า ประเภทถูกเชื่อมโยง และไม่มีการสร้างข้อมูลซ้ำ</span><span class="sxs-lookup"><span data-stu-id="cc2b4-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="cc2b4-118">โดยทั่วไป ประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2b4-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="cc2b4-119">อย่างไรก็ตาม ถ้าพวกเขาไม่ใช่ต้นฉบับใน Finance and Operations หรือถ้ามีการสร้างประเภทค่าใช้จ่ายใน Project Service Automation แล้ว อันดับแรก คุณต้องก่อนซิงโครไนส์โดยใช้เท็มเพลตประเภทธุรกรรมค่าใช้จ่ายโครงการ (PSA ไปยัง Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="cc2b4-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="cc2b4-120">จากนั้น ซิงโครไนส์โดยใช้เท็มเพลตประเภทธุรกรรมค่าใช้จ่ายของโครงการ (Fin and Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="cc2b4-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="cc2b4-121">จากนั้น คุณควรรันการซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations อีกหนึ่งครั้ง</span><span class="sxs-lookup"><span data-stu-id="cc2b4-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="cc2b4-122">หากคุณซิงโครไนส์ครั้งแรกจาก Project Service Automation ต้องเป็นไปตามข้อกำหนดต่อไปนี้ใน Finance and Operations ก่อนที่จะรันการซิงโครไนส์:</span><span class="sxs-lookup"><span data-stu-id="cc2b4-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="cc2b4-123">ประเภทใช้ร่วมกันที่สอดคล้องกับประเภทโครงการที่ตั้งค่าไว้ใน Project Service Automation ต้องมีอยู่ และต้องถูกเปิดใช้งานสำหรับทั้ง **โครงการ** และ **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="cc2b4-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="cc2b4-124">สำหรับนิติบุคคล Finance and Operations แต่ละรายที่ต้องถูกรวม ต้องมีประเภทโครงการต่อไปนี้อยู่:</span><span class="sxs-lookup"><span data-stu-id="cc2b4-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="cc2b4-125">มี **ประเภทโครงการ** อยู่</span><span class="sxs-lookup"><span data-stu-id="cc2b4-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="cc2b4-126">**ใช้ในค่าใช้จ่าย** ถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cc2b4-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="cc2b4-127">**ใช้งานอยู่ในสมุดรายวัน** ถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cc2b4-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="cc2b4-128">**ชนิดธุรกรรม** ถูกตั้งค่าเป็น **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="cc2b4-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="cc2b4-129">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2b4-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="cc2b4-130">[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="cc2b4-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="cc2b4-131">การซิงโครไนส์ประเภทค่าใช้จ่ายโครงการจาก Finance and Operations ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc2b4-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="cc2b4-132">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="cc2b4-132">Template and task</span></span>

<span data-ttu-id="cc2b4-133">เพื่อเข้าถึงเท็มเพลต ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="cc2b4-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="cc2b4-134">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Finance and Operations ไปยัง Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="cc2b4-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="cc2b4-135">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายของโครงการ (Fin and Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="cc2b4-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="cc2b4-136">**ชื่อของงานในโครงการ:** ซิงค์ประเภทไปยัง PSA</span><span class="sxs-lookup"><span data-stu-id="cc2b4-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="cc2b4-137">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="cc2b4-137">Entity set</span></span>

| <span data-ttu-id="cc2b4-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2b4-138">Finance and Operations</span></span>            | <span data-ttu-id="cc2b4-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc2b4-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="cc2b4-140">เอนทิตี้การรวมสำหรับประเภท</span><span class="sxs-lookup"><span data-stu-id="cc2b4-140">Integration entity for categories</span></span> | <span data-ttu-id="cc2b4-141">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cc2b4-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="cc2b4-142">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="cc2b4-142">Entity flow</span></span>

<span data-ttu-id="cc2b4-143">มีการจัดการประเภทค่าใช้จ่ายของโครงการใน Finance and Operations และมีการซิงโครไนส์ไปยัง Project Service Automation เป็นประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cc2b4-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="cc2b4-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="cc2b4-144">Power Query</span></span>

<span data-ttu-id="cc2b4-145">เมื่อคุณต้องซิงโครไนส์กับ Project Service Automation คุณต้องใช้ Microsoft Power Query for Excel เพื่อตั้งค่าชนิดการเรียกเก็บเงินในประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cc2b4-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="cc2b4-146">ประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin and Ops ไปยัง PSA) มีคอลัมน์เริ่มต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="cc2b4-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="cc2b4-147">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มคอลัมน์แบบมีเงื่อนไขใน Power Query</span><span class="sxs-lookup"><span data-stu-id="cc2b4-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="cc2b4-148">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="cc2b4-148">Follow these steps.</span></span>

1. <span data-ttu-id="cc2b4-149">คลิกลูกศรเพื่อเปิดการแม็ปของงานประเภทค่าใช้จ่ายโครงการงานในเท็มเพลตประเภทของธุรกรรมค่าใช้จ่ายโครงการ (Fin and Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="cc2b4-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="cc2b4-150">คลิกลิงก์ **การกรองข้อมูลและแบบสอบถามขั้นสูง** เพื่อเปิด Power Query</span><span class="sxs-lookup"><span data-stu-id="cc2b4-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="cc2b4-151">เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="cc2b4-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="cc2b4-152">ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **BillingType**</span><span class="sxs-lookup"><span data-stu-id="cc2b4-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="cc2b4-153">ป้อนเงื่อนไขต่อไปนี้: **ถ้า CATEGORYID ไม่เท่ากับ null แล้ว 19235001 มิฉะนั้น null**</span><span class="sxs-lookup"><span data-stu-id="cc2b4-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="cc2b4-154">คลิก **ตกลง** บนคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="cc2b4-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="cc2b4-155">ตรวจสอบให้แน่ใจว่าได้แม็ปคอลัมน์ใหม่นี้ในหน้าการแม็ป</span><span class="sxs-lookup"><span data-stu-id="cc2b4-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="cc2b4-156">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc2b4-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="cc2b4-157">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Finance and Operations ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc2b4-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="cc2b4-158">[![การแม็ปเท็มเพลต](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cc2b4-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="cc2b4-159">การซิงโครไนส์ประเภทค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2b4-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="cc2b4-160">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="cc2b4-160">Template and task</span></span>

<span data-ttu-id="cc2b4-161">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Project Service Automation ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="cc2b4-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="cc2b4-162">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="cc2b4-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="cc2b4-163">**ชื่อของงานในโครงการ:** ซิงค์ประเภทไปยัง Fin Ops</span><span class="sxs-lookup"><span data-stu-id="cc2b4-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="cc2b4-164">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="cc2b4-164">Entity set</span></span>

| <span data-ttu-id="cc2b4-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc2b4-165">Project Service Automation</span></span> | <span data-ttu-id="cc2b4-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2b4-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="cc2b4-167">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cc2b4-167">Transaction categories</span></span>     | <span data-ttu-id="cc2b4-168">เอนทิตี้การรวมสำหรับประเภท</span><span class="sxs-lookup"><span data-stu-id="cc2b4-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="cc2b4-169">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="cc2b4-169">Entity flow</span></span>

<span data-ttu-id="cc2b4-170">มีการจัดการประเภทค่าใช้จ่ายของโครงการใน Finance and Operations และมีการซิงโครไนส์ไปยัง Project Service Automation เป็นประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cc2b4-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="cc2b4-171">การซิงโครไนส์กลับไปยัง Finance and Operations จะอัพเดตประเภทโครงการใน Finance and Operations ด้วยรหัสการรวมจาก Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc2b4-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cc2b4-172">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc2b4-172">Template mapping in Data integration</span></span>

<span data-ttu-id="cc2b4-173">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc2b4-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="cc2b4-174">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc2b4-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="cc2b4-175">[![การแม็ปเท็มเพลต](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cc2b4-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
