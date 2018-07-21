---
title: "ซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Project Service Automation"
description: "หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการระหว่าง Microsoft Dynamics 365 for Finance and Operations และ Dynamics 365 for Project Service Automation"
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: th-th
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="6f063-103">ปซิงโครไนส์ระเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6f063-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="6f063-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการระหว่าง Microsoft Dynamics 365 for Finance and Operations และ Dynamics 365 for Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6f063-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="6f063-105">การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชัน พร้อมใช้งานใน Dynamics 365 for Finance and Operations รุ่น 8.0</span><span class="sxs-lookup"><span data-stu-id="6f063-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="6f063-106">โฟลว์ข้อมูลสำหรับ Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f063-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="6f063-107">โซลูชันการรวม Project Service Automation และ Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f063-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="6f063-108">เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับธุรกรรมค่าใช้จ่ายของโครงการระหว่าง Finance and Operations และ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6f063-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="6f063-109">ถ้าประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Finance and Operations ในตอนแรกโฟลว์การรวมมาจาก Finance and Operations ไปยัง Project Service Automation และจากนั้น อัพเดตรหัสการรวมของประเภทค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f063-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="6f063-110">ถ้าประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Project Service Automation ในตอนแรกโฟลว์การรวมมาจาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f063-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="6f063-111">ประเภทโครงการต้องถูกตั้งค่าคอนฟิกใน Finance and Operations อยู่แล้ว ก่อนการซิงโครไนส์จาก Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6f063-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="6f063-112">จากนั้น ซิงโครไนส์จาก Finance and Operations กลับไปยัง Project Service Automation และจากนั้นจาก Project Service Automation ไปยัง Finance and Operations อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="6f063-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="6f063-113">ซึ่งช่วยให้มั่นใจว่าประเภทจะถูกเชื่อมโยง และไม่มีการสร้างข้อมูลซ้ำ</span><span class="sxs-lookup"><span data-stu-id="6f063-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="6f063-114">โดยทั่วไป ประเภทค่าใช้จ่ายโครงการจะเป็นต้นฉบับใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f063-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="6f063-115">ถ้านั่นไม่ใช่สถานการณ์ของคุณ หรือคุณมีประเภทค่าใช้จ่ายที่สร้างขึ้นใน Project Service Automation อยู่แล้ว คุณต้องซิงค์โดยใช้ประเภทธุรกรรมค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops) และจากนั้น ซิงค์โดยใช้ประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin and Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="6f063-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="6f063-116">จากนั้น คุณควรรันการซิงค์จาก PSA ไปยัง Fin and Ops อีกหนึ่งครั้ง</span><span class="sxs-lookup"><span data-stu-id="6f063-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="6f063-117">ถ้าในตอนแรกการซิงโครไนส์มาจาก Project Service Automation ประเภทโครงการต้องถูกตั้งค่าใน Finance and Operations อยู่แล้ว และประเภทโครงการใดๆ ที่จำเป็นต้องซิงค์กับประเภทธุรกรรม Project Service Automation ต้องถูกตั้งค่าเป็น **ใช้งานอยู่ในสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="6f063-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="6f063-118">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f063-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="6f063-119">[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="6f063-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="6f063-120">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="6f063-120">Templates and tasks</span></span>

<span data-ttu-id="6f063-121">เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="6f063-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="6f063-122">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Finance and Operations ไปยัง Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="6f063-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="6f063-123">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายของโครงการ (Fin and Ops ไปยัง PSA)</span><span class="sxs-lookup"><span data-stu-id="6f063-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="6f063-124">**ชื่อของงานในโครงการ:** ซิงค์ประเภทไปยัง PSA</span><span class="sxs-lookup"><span data-stu-id="6f063-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="6f063-125">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="6f063-125">Entity set</span></span>

| <span data-ttu-id="6f063-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f063-126">Finance and Operations</span></span>               | <span data-ttu-id="6f063-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6f063-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="6f063-128">เอนทิตี้การรวมสำหรับประเภท</span><span class="sxs-lookup"><span data-stu-id="6f063-128">Integration entity for categories</span></span>    | <span data-ttu-id="6f063-129">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="6f063-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="6f063-130">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="6f063-130">Entity flow</span></span>

<span data-ttu-id="6f063-131">มีการจัดการประเภทค่าใช้จ่ายของโครงการใน Finance and Operations และมีการซิงโครไนส์ไปยัง Project Service Automation เป็นประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="6f063-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="6f063-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="6f063-132">Power Query</span></span>

<span data-ttu-id="6f063-133">คุณต้องใช้ Microsoft Power Query เพื่อตั้งค่าชนิดการเรียกเก็บเงินในประเภทธุรกรรม เมื่อซิงโครไนส์กับ Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6f063-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="6f063-134">ประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin and Ops ไปยัง PSA) มีคอลัมน์เริ่มต้นและการแม็ปที่มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="6f063-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="6f063-135">ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มคอลัมน์แบบมีเงื่อนไขใน Power Query</span><span class="sxs-lookup"><span data-stu-id="6f063-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="6f063-136">เปิดแบบฟอร์มการสอบถามขั้นสูงและการกรองจากภายในการแม็ปงานประเภทค่าใช้จ่ายโครงการ</span><span class="sxs-lookup"><span data-stu-id="6f063-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="6f063-137">เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="6f063-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="6f063-138">ตั้งชื่อคอลัมน์ใหม่ เช่น BillingType</span><span class="sxs-lookup"><span data-stu-id="6f063-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="6f063-139">ป้อนเงื่อนไขต่อไปนี้: ถ้า **CATEGORYID ไม่เท่ากับ null แล้ว 19235001 มิฉะนั้น null**</span><span class="sxs-lookup"><span data-stu-id="6f063-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="6f063-140">คลิก **ตกลง** บนคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="6f063-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="6f063-141">ตรวจสอบให้แน่ใจว่าแม็ปคอลัมน์ใหม่นี้ในหน้าการแม็ป</span><span class="sxs-lookup"><span data-stu-id="6f063-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="6f063-142">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6f063-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="6f063-143">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Finance and Operations ไปยัง Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6f063-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="6f063-144">[![การแม็ปเท็มเพลต](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="6f063-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="6f063-145">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Project Service Automation ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="6f063-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="6f063-146">-**ชื่อของเท็มเพลตในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายโครงการ (PSA ไปยัง Fin and Ops) -**ชื่อของงานในโครงการ:** ซิงค์ประเภทไปยัง Fin Ops</span><span class="sxs-lookup"><span data-stu-id="6f063-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="6f063-147">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="6f063-147">Entity set</span></span>

| <span data-ttu-id="6f063-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6f063-148">Project Service Automation</span></span>      | <span data-ttu-id="6f063-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f063-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="6f063-150">ประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="6f063-150">Transaction categories</span></span>          | <span data-ttu-id="6f063-151">เอนทิตี้การรวมสำหรับประเภท</span><span class="sxs-lookup"><span data-stu-id="6f063-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="6f063-152">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="6f063-152">Entity flow</span></span>

<span data-ttu-id="6f063-153">มีการจัดการประเภทค่าใช้จ่ายของโครงการใน Finance and Operations และมีการซิงโครไนส์ไปยัง Project Service Automation เป็นประเภทธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="6f063-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="6f063-154">การซิงโครไนส์กลับไปยัง Finance and Operations อัพเดตรหัสการรวมจาก Project Service Automation ในประเภทโครงการ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f063-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="6f063-155">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6f063-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="6f063-156">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6f063-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="6f063-157">[![การแม็ปเท็มเพลต](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="6f063-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

