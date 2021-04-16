---
title: ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Sales
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำซิงโครไนส์ผลิตภัณฑ์จาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Sales
author: ChristianRytt
ms.date: 06/10/2019
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 29bb9d05aa939ec82595e153faf03f290e219589
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817832"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="5ec79-103">ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="5ec79-104">ก่อนที่คุณจะสามารถใช้โซลูชันผู้มีแนวโน้มจะเป็นลูกค้าเงินสด คุณควรคุ้นเคยกับ [รวมข้อมูลลงใน Microsoft Dataverse สำหรับแอป](https://docs.microsoft.com/powerapps/administrator/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="5ec79-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="5ec79-105">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5ec79-106">โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="5ec79-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5ec79-107">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="5ec79-108">แม่แบบของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดที่มีให้ใช้งานร่วมกันกับคุณลักษณะการรวมข้อมูล ช่วยให้เกิดกระแสของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="5ec79-109">ภาพประกอบต่อไปนี้ แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="5ec79-110">[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5ec79-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5ec79-111">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="5ec79-111">Templates and tasks</span></span>

<span data-ttu-id="5ec79-112">เมื่อต้องการเข้าถึงแม่แบบที่พร้อมใช้งาน ให้เปิด [Power Apps ศูนย์การจัดการ](https://admin.powerapps.com/dataintegration)</span><span class="sxs-lookup"><span data-stu-id="5ec79-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="5ec79-113">เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="5ec79-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5ec79-114">แม่แบบและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ผลิตภัณฑ์จาก Supply Chain Management ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="5ec79-115">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ผลิตภัณฑ์ (Supply Chain Management ไปยัง Sales) - ทางตรง</span><span class="sxs-lookup"><span data-stu-id="5ec79-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="5ec79-116">**ชื่อของงานในโครงการการรวมข้อมูล:** ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5ec79-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="5ec79-117">ไม่มีงานในการซิงโครไนส์จำเป็นต้องใช้ ก่อนการซิงโครไนส์ผลิตภัณฑ์จะสามารถเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="5ec79-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="5ec79-118">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="5ec79-118">Entity set</span></span>

| <span data-ttu-id="5ec79-119">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ec79-119">Supply Chain Management</span></span>    | <span data-ttu-id="5ec79-120">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="5ec79-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="5ec79-121">ผลิตภัณฑ์ที่นำออกใช้ที่สามารถขายได้</span><span class="sxs-lookup"><span data-stu-id="5ec79-121">Sellable released products</span></span> | <span data-ttu-id="5ec79-122">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5ec79-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="5ec79-123">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="5ec79-123">Entity flow</span></span>

<span data-ttu-id="5ec79-124">ผลิตภัณฑ์จะถูกจัดการใน Supply Chain Management และถูกซิงโครไนส์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="5ec79-125">เอนทิตี้ข้อมูล **ผลิตภัณฑ์ที่นำออกใช้ที่สามารถขายได้** ใน Supply Chain Management ส่งออกเฉพาะผลิตภัณฑ์ที่ *สามารถขายได้*</span><span class="sxs-lookup"><span data-stu-id="5ec79-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="5ec79-126">ผลิตภัณฑ์ที่สามารถขายได้ เป็นผลิตภัณฑ์ที่มีข้อมูลที่พวกเขาต้องการเพื่อใช้ในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="5ec79-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="5ec79-127">กฎเดียวกันนี้จะใช้เมื่อผลิตภัณฑ์ได้รับการตรวจสอบโดยการใช้ฟังก์ชัน **ตรวจสอบ** ในหน้า **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="5ec79-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="5ec79-128">มีการใช้หมายเลขผลิตภัณฑ์เป็นคีย์</span><span class="sxs-lookup"><span data-stu-id="5ec79-128">The product number is used as a key.</span></span> <span data-ttu-id="5ec79-129">ดังนั้น เมื่อผลิตภัณฑ์ย่อยถูกซิงโครไนส์กับ Sales ผลิตภัณฑ์ย่อยแต่ละรายการจะมีรหัสผลิตภัณฑ์แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="5ec79-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5ec79-130">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5ec79-131">ใน Sales ฟิลด์ **ถูกรักษาไว้ภายนอก** จะถูกเพิ่มในผลิตภัณฑ์ เพื่อบ่งชี้ว่าผลิตภัณฑ์ที่กำหนดให้ถูกรักษาไว้ภายนอก</span><span class="sxs-lookup"><span data-stu-id="5ec79-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="5ec79-132">โดยค่าเริ่มต้น ค่าจะถูกตั้งเป็น **ใช่** ระหว่างการนำเข้าไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="5ec79-133">ค่าที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5ec79-133">The following values are available:</span></span>

- <span data-ttu-id="5ec79-134">**ใช่** – ผลิตภัณฑ์สร้างจาก Supply Chain Management และจะไม่สามารถแก้ไขได้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="5ec79-135">**ไม่** – มีการป้อนผลิตภัณฑ์โดยตรงใน Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="5ec79-136">**(ว่างเปล่า)** – ผลิตภัณฑ์ที่มีอยู่แล้วใน Sales ก่อนที่โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดจะมีการเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="5ec79-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="5ec79-137">ฟิลด์ **ถูกรักษาไว้ภายนอก** จะช่วยให้มั่นใจว่าเฉพาะใบเสนอราคาและใบสั่งขายที่มีผลิตภัณฑ์ที่ถูกรักษาไว้ภายนอกจะซิงค์กับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ec79-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="5ec79-138">ผลิตภัณฑ์รักษาไว้ภายนอกจะถูกเพิ่มไปยังรายการราคาแรกที่ถูกต้องที่มีสกุลเงินเดียวกันโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="5ec79-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="5ec79-139">รายการราคามีการจัดระเบียบตามตัวอักษรตามชื่อ</span><span class="sxs-lookup"><span data-stu-id="5ec79-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="5ec79-140">ราคาขายของผลิตภัณฑ์จาก Supply Chain Management ถูกใช้เป็นราคาในรายการราคา</span><span class="sxs-lookup"><span data-stu-id="5ec79-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="5ec79-141">ดังนั้น ต้องมีรายการราคาใน Sales สำหรับสกุลเงินขายผลิตภัณฑ์ทุกๆ สกุลใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ec79-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="5ec79-142">สกุลเงินของผลิตภัณฑ์ที่สามารถขายได้ที่นำออกใช้ จะถูกตั้งค่าเป็นสกุลเงินทางบัญชีในนิติบุคคลที่ผลิตภัณฑ์ถูกส่งออกมา</span><span class="sxs-lookup"><span data-stu-id="5ec79-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="5ec79-143">การซิงโครไนส์ผลิตภัณฑ์จะไม่สำเร็จ เว้นแต่จะมีรายการราคาที่มีสกุลเงินที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="5ec79-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="5ec79-144">คุณสามารถควบคุมรายการราคาที่ใช้กับการรวม โดยการแม็ป pricelevelid.name [รายการราคาเริ่มต้น (ชื่อ)] ได้ในโครงการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5ec79-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="5ec79-145">การป้อนข้อมูลต้องเป็นอักษรตัวพิมพ์เล็กทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5ec79-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="5ec79-146">ตัวอย่างเช่น ค่าเริ่มต้นสำหรับราคาตลาดในการขายที่มีชื่อว่า 'มาตรฐาน' จะเป็น: ฟิลด์ปลายทาง: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ]</span><span class="sxs-lookup"><span data-stu-id="5ec79-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5ec79-147">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="5ec79-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="5ec79-148">ก่อนที่คุณจะรันการซิงโครไนส์เป็นครั้งแรก คุณต้องเติมข้อมูลในตารางผลิตภัณฑ์เฉพาะสำหรับผลิตภัณฑ์ที่มีอยู่ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ec79-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="5ec79-149">จะไม่มีการซิงโครไนส์ผลิตภัณฑ์ที่มีอยู่จนกว่างานนี้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="5ec79-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="5ec79-150">ใน Supply Chain Management ให้ใช้ค้นหาเพื่อค้นหา **เติมข้อมูลตารางผลิตภัณฑ์เฉพาะ**</span><span class="sxs-lookup"><span data-stu-id="5ec79-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="5ec79-151">เลือก **เติมข้อมูลตารางผลิตภัณฑ์เฉพาะ** เพื่อรันงาน</span><span class="sxs-lookup"><span data-stu-id="5ec79-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="5ec79-152">งานนี้ต้องรันเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="5ec79-152">This job must be run only one time.</span></span>

- <span data-ttu-id="5ec79-153">ตรวจสอบให้แน่ใจว่ามีแผนผังค่าที่จำเป็นสำหรับการขายหน่วยวัด (UOM) ระหว่าง Supply Chain Management และ Sales มีอยู่ในการแม็ปของ **SalesUnitSymbol** ไปยัง **DefaultUnit (Name)**</span><span class="sxs-lookup"><span data-stu-id="5ec79-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="5ec79-154">อัพเดตแผนผังค่าสำหรับ **กลุ่มหน่วย** (**defaultuomscheduleid.name**) เพื่อให้ตรงกับ **กลุ่มหน่วย** ใน Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="5ec79-155">ค่าเท็มเพลตเริ่มต้นคือ **หน่วยเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="5ec79-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="5ec79-156">ตรวจสอบให้แน่ใจว่า UOM ในการขายสำหรับผลิตภัณฑ์ทั้งหมดจาก Supply Chain Management มีอยู่ใน Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="5ec79-157">ตรวจสอบให้แน่ใจว่า รายการราคามีอยู่ใน Sales สำหรับสกุลเงินขายของผลิตภัณฑ์แต่ละสกุลใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ec79-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="5ec79-158">เมื่อมีการสร้างผลิตภัณฑ์ใน Sales สามารถมีสถานะเป็น **ร่าง** หรือ **ใช้งานอยู่** ได้</span><span class="sxs-lookup"><span data-stu-id="5ec79-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="5ec79-159">มีการควบคุมพฤติกรรมที่ **การตั้งค่า** > **การดูแลระบบ** > **การตั้งค่าระบบ** > **การขาย** ใน Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="5ec79-160">ผลิตภัณฑ์ที่มีสถานะ **ร่าง** เมื่อมีการสร้าง ต้องถูกเรียกใช้งงานก่อน จึงจะสามารถถูกเพิ่มไปยังใบเสนอราคาหรือใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="5ec79-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5ec79-161">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5ec79-161">Template mapping in Data integration</span></span>

<span data-ttu-id="5ec79-162">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5ec79-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ec79-163">การแม็ปจะช่วยแสดงให้เห็นว่า ข้อมูลฟิลด์ใดที่จะถูกซิงโครไนส์จาก Sales ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ec79-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="5ec79-165">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="5ec79-165">Related topics</span></span>

[<span data-ttu-id="5ec79-166">ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด</span><span class="sxs-lookup"><span data-stu-id="5ec79-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="5ec79-167">ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ec79-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="5ec79-168">ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ec79-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="5ec79-169">การซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Sales และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ec79-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="5ec79-170">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Supply Chain Management ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="5ec79-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]