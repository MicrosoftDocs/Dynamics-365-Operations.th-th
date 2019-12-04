---
title: ปซิงโครไนส์ระเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ซิงโครไนส์ประเภทค่าใช้จ่ายโครงการระหว่าง Microsoft Dynamics 365 Finance และ Dynamics 365 Project Service Automation
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
ms.openlocfilehash: 7b0b3721c3b0755218c834d2bf77ec976be3bdcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770323"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="15269-103">ปซิงโครไนส์ระเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="15269-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="15269-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลประเภทค่าใช้จ่ายโครงการระหว่าง Dynamics 365 Finance และ Dynamics 365 Project Service Automation ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="15269-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="15269-105">การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชันซึ่งพร้อมใช้งานในรุ่น 8.0</span><span class="sxs-lookup"><span data-stu-id="15269-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="15269-106">การรวมรายการจริงจะพร้อมใช้งานในรุ่น 8.0.1 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="15269-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="15269-107">ถ้าคุณกำลังใช้ Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้เท็มเพลตเพื่อรวมงานโครงการ ค่าใช้จ่ายประเภทธุรกรรม การประเมินชั่วโมง การประเมินค่าใช้จ่าย และค่าที่เกิดขึ้นจริงได้และสามารถตั้งค่าคอนฟิกฟังก์ชันการล็อคได้</span><span class="sxs-lookup"><span data-stu-id="15269-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="15269-108">ถ้าคุณต้องตั้งค่าการกระจายการลงบัญชี เราขอแนะนำให้ คุณติดตั้ง KB 4131710 ด้วย</span><span class="sxs-lookup"><span data-stu-id="15269-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="15269-109">โฟลว์ข้อมูลสำหรับ Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="15269-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="15269-110">Project Service Automation และ Finance integration solution ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="15269-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="15269-111">เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับประเภทธุรกรรมค่าใช้จ่ายของโครงการระหว่าง Finance และ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="15269-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="15269-112">ถ้าประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Finance ในตอนแรกโฟลว์การรวมมาจาก Finance ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="15269-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="15269-113">จากนั้น รหัสการรวมของระเภทค่าใช้จ่ายของโครงการถูกปรับปรุงผ่านทางการซิงโครไนส์จาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="15269-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="15269-114">ถ้าประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Project Service Automation ในตอนแรกโฟลว์การรวมมาจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="15269-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="15269-115">ประเภทโครงการต้องถูกตั้งค่าคอนฟิกใน Finance อยู่แล้ว ก่อนการซิงโครไนส์จาก Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="15269-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="15269-116">จากนั้น ซิงโครไนส์จาก Finance กลับไปยัง Project Service Automation และจากนั้นจาก Project Service Automation ไปยัง Finance อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="15269-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="15269-117">ด้วยวิธีนี้ คุณช่วยรับประกันว่า ประเภทถูกเชื่อมโยง และไม่มีการสร้างข้อมูลซ้ำ</span><span class="sxs-lookup"><span data-stu-id="15269-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="15269-118">โดยทั่วไป ประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Finance</span><span class="sxs-lookup"><span data-stu-id="15269-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="15269-119">อย่างไรก็ตาม ถ้าพวกเขาไม่ใช่ต้นฉบับใน Finance หรือถ้ามีการสร้างประเภทค่าใช้จ่ายใน Project Service Automation แล้ว อันดับแรก คุณต้องซิงโครไนส์โดยใช้เท็มเพลตประเภทธุรกรรมค่าใช้จ่ายโครงการ (PSA ไปยัง Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="15269-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="15269-120">จากนั้น ซิงโครไนส์โดยใช้เท็มเพลตประเภทธุรกรรมค่าใช้จ่ายของโครงการ (Fin and Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="15269-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="15269-121">จากนั้น คุณควรรันการซิงโครไนส์จาก Project Service Automation ไปยัง Finance อีกหนึ่งครั้ง</span><span class="sxs-lookup"><span data-stu-id="15269-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="15269-122">หากคุณซิงโครไนส์ครั้งแรกจาก Project Service Automation ต้องเป็นไปตามข้อกำหนดต่อไปนี้ใน Finance ก่อนที่จะรันการซิงโครไนส์:</span><span class="sxs-lookup"><span data-stu-id="15269-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="15269-123">ประเภทใช้ร่วมกันที่สอดคล้องกับประเภทโครงการที่ตั้งค่าไว้ใน Project Service Automation ต้องมีอยู่ และต้องถูกเปิดใช้งานสำหรับทั้ง **โครงการ** และ **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="15269-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="15269-124">สำหรับนิติบุคคล Finance แต่ละรายที่ต้องถูกรวม ต้องมีประเภทโครงการต่อไปนี้อยู่:</span><span class="sxs-lookup"><span data-stu-id="15269-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="15269-125">มี **ประเภทโครงการ** อยู่</span><span class="sxs-lookup"><span data-stu-id="15269-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="15269-126">**ใช้ในค่าใช้จ่าย** ถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="15269-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="15269-127">**ใช้งานอยู่ในสมุดรายวัน** ถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="15269-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="15269-128">**ชนิดธุรกรรม** ถูกตั้งค่าเป็น **ค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="15269-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="15269-129">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance</span><span class="sxs-lookup"><span data-stu-id="15269-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="15269-130">[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="15269-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="15269-131">การซิงโครไนส์ประเภทค่าใช้จ่ายโครงการจาก Finance ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="15269-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="15269-132">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="15269-132">Template and task</span></span>

<span data-ttu-id="15269-133">เพื่อเข้าถึงเท็มเพลต ในศูนย์การจัดการ Microsoft Power Apps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="15269-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="15269-134">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Finance ไปยัง Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="15269-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="15269-135">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายของโครงการ (Fin and Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="15269-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="15269-136">**ชื่อของงานในโครงการ:** ซิงค์ประเภทไปยัง PSA</span><span class="sxs-lookup"><span data-stu-id="15269-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="15269-137">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="15269-137">Entity set</span></span>

| <span data-ttu-id="15269-138">การเงิน</span><span class="sxs-lookup"><span data-stu-id="15269-138">Finance</span></span>                           | <span data-ttu-id="15269-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="15269-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="15269-140">เอนทิตี้การรวมสำหรับประเภท</span><span class="sxs-lookup"><span data-stu-id="15269-140">Integration entity for categories</span></span> | <span data-ttu-id="15269-141">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="15269-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="15269-142">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="15269-142">Entity flow</span></span>

<span data-ttu-id="15269-143">มีการจัดการประเภทค่าใช้จ่ายของโครงการใน Finance และมีการซิงโครไนส์ไปยัง Project Service Automation เป็นประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="15269-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="15269-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="15269-144">Power Query</span></span>

<span data-ttu-id="15269-145">เมื่อคุณต้องซิงโครไนส์กับ Project Service Automation คุณต้องใช้ Microsoft Power Query for Excel เพื่อตั้งค่าชนิดการเรียกเก็บเงินในประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="15269-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="15269-146">ประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin and Ops ไปยัง PSA) มีคอลัมน์เริ่มต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="15269-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="15269-147">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มคอลัมน์แบบมีเงื่อนไขใน Power Query</span><span class="sxs-lookup"><span data-stu-id="15269-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="15269-148">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="15269-148">Follow these steps.</span></span>

1. <span data-ttu-id="15269-149">คลิกลูกศรเพื่อเปิดการแม็ปของงานประเภทค่าใช้จ่ายโครงการงานในเท็มเพลตประเภทของธุรกรรมค่าใช้จ่ายโครงการ (Fin and Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="15269-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="15269-150">คลิกลิงก์ **การกรองข้อมูลและแบบสอบถามขั้นสูง** เพื่อเปิด Power Query</span><span class="sxs-lookup"><span data-stu-id="15269-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="15269-151">เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="15269-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="15269-152">ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **BillingType**</span><span class="sxs-lookup"><span data-stu-id="15269-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="15269-153">ป้อนเงื่อนไขต่อไปนี้: **ถ้า CATEGORYID ไม่เท่ากับ null แล้ว 19235001 มิฉะนั้น null**</span><span class="sxs-lookup"><span data-stu-id="15269-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="15269-154">คลิก **ตกลง** บนคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="15269-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="15269-155">ตรวจสอบให้แน่ใจว่าได้แม็ปคอลัมน์ใหม่นี้ในหน้าการแม็ป</span><span class="sxs-lookup"><span data-stu-id="15269-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="15269-156">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="15269-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="15269-157">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Finance ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="15269-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="15269-158">[![การแม็ปเท็มเพลต](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="15269-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="15269-159">การซิงโครไนส์ประเภทค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="15269-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="15269-160">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="15269-160">Template and task</span></span>

<span data-ttu-id="15269-161">เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="15269-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="15269-162">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="15269-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="15269-163">**ชื่อของงานในโครงการ:** ซิงค์ประเภทไปยัง Fin Ops</span><span class="sxs-lookup"><span data-stu-id="15269-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="15269-164">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="15269-164">Entity set</span></span>

| <span data-ttu-id="15269-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="15269-165">Project Service Automation</span></span> | <span data-ttu-id="15269-166">การเงิน</span><span class="sxs-lookup"><span data-stu-id="15269-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="15269-167">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="15269-167">Transaction categories</span></span>     | <span data-ttu-id="15269-168">เอนทิตี้การรวมสำหรับประเภท</span><span class="sxs-lookup"><span data-stu-id="15269-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="15269-169">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="15269-169">Entity flow</span></span>

<span data-ttu-id="15269-170">มีการจัดการประเภทค่าใช้จ่ายของโครงการใน Finance และมีการซิงโครไนส์ไปยัง Project Service Automation เป็นประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="15269-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="15269-171">การซิงโครไนส์กลับไปยัง Finance จะอัพเดตประเภทโครงการใน Finance and Operations ด้วยรหัสการรวมจาก Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="15269-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="15269-172">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="15269-172">Template mapping in Data integration</span></span>

<span data-ttu-id="15269-173">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="15269-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="15269-174">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance</span><span class="sxs-lookup"><span data-stu-id="15269-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="15269-175">[![การแม็ปเท็มเพลต](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="15269-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
