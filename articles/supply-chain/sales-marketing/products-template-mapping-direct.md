---
title: "ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ไปยัง Microsoft Dynamics 365 for Sales"
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: def88c291538e3ef278c51e4b87462782e222de2
ms.contentlocale: th-th
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="cbcf0-103">ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="cbcf0-104">ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดได้ คุณควรทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration)</span><span class="sxs-lookup"><span data-stu-id="cbcf0-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="cbcf0-105">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ไปยัง Microsoft Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="cbcf0-106">โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="cbcf0-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="cbcf0-107">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="cbcf0-108">เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล จะเปิดใช้งานขั้นตอนของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="cbcf0-109">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="cbcf0-110">[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="cbcf0-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cbcf0-111">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="cbcf0-111">Templates and tasks</span></span>

<span data-ttu-id="cbcf0-112">เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน เปิด [ศูนย์การจัดการ PowerApps](https://preview.admin.powerapps.com/dataintegration)</span><span class="sxs-lookup"><span data-stu-id="cbcf0-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="cbcf0-113">เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="cbcf0-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="cbcf0-114">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยัง Sales:</span><span class="sxs-lookup"><span data-stu-id="cbcf0-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="cbcf0-115">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales) - ตรง</span><span class="sxs-lookup"><span data-stu-id="cbcf0-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="cbcf0-116">**ชื่อของงานในโครงการการรวมข้อมูล:** ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cbcf0-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="cbcf0-117">ไม่มีงานในการซิงโครไนส์จำเป็นต้องใช้ ก่อนการซิงโครไนส์ผลิตภัณฑ์จะสามารถเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="cbcf0-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="cbcf0-118">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="cbcf0-118">Entity set</span></span>

| <span data-ttu-id="cbcf0-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbcf0-119">Finance and Operations</span></span>     | <span data-ttu-id="cbcf0-120">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cbcf0-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="cbcf0-121">ผลิตภัณฑ์ที่นำออกใช้ที่สามารถขายได้</span><span class="sxs-lookup"><span data-stu-id="cbcf0-121">Sellable released products</span></span> | <span data-ttu-id="cbcf0-122">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cbcf0-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="cbcf0-123">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="cbcf0-123">Entity flow</span></span>

<span data-ttu-id="cbcf0-124">ผลิตภัณฑ์จะถูกจัดการใน Finance and Operations และจะถูกซิงโครไนส์ไปยังการขาย</span><span class="sxs-lookup"><span data-stu-id="cbcf0-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="cbcf0-125">เอนทิตี้ข้อมูล **ผลิตภัณฑ์ที่นำออกใช้ที่สามารถขายได้** ใน Finance and Operations ส่งออกเฉพาะผลิตภัณฑ์ที่ *สามารถขายได้*</span><span class="sxs-lookup"><span data-stu-id="cbcf0-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="cbcf0-126">ผลิตภัณฑ์ที่สามารถขายได้ เป็นผลิตภัณฑ์ที่มีข้อมูลที่พวกเขาต้องการเพื่อใช้ในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cbcf0-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="cbcf0-127">กฎเดียวกันนี้จะใช้เมื่อผลิตภัณฑ์ได้รับการตรวจสอบโดยการใช้ฟังก์ชัน **ตรวจสอบ** ในหน้า **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="cbcf0-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="cbcf0-128">มีการใช้หมายเลขผลิตภัณฑ์เป็นคีย์</span><span class="sxs-lookup"><span data-stu-id="cbcf0-128">The product number is used as a key.</span></span> <span data-ttu-id="cbcf0-129">ดังนั้น เมื่อผลิตภัณฑ์ย่อยถูกซิงโครไนส์กับ Sales ผลิตภัณฑ์ย่อยแต่ละรายการจะมีรหัสผลิตภัณฑ์แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="cbcf0-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="cbcf0-130">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="cbcf0-131">ใน Sales ฟิลด์ **ถูกรักษาไว้ภายนอก** จะถูกเพิ่มในผลิตภัณฑ์ เพื่อบ่งชี้ว่าผลิตภัณฑ์ที่กำหนดให้ถูกรักษาไว้ภายนอก</span><span class="sxs-lookup"><span data-stu-id="cbcf0-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="cbcf0-132">โดยค่าเริ่มต้น ค่าจะถูกตั้งเป็น **ใช่** ระหว่างการนำเข้าไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="cbcf0-133">ค่าที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cbcf0-133">The following values are available:</span></span>

- <span data-ttu-id="cbcf0-134">**ใช่** – ผลิตภัณฑ์สร้างจาก Finance and Operations และจะไม่สามารถแก้ไขได้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="cbcf0-135">**ไม่** – มีการป้อนผลิตภัณฑ์โดยตรงใน Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="cbcf0-136">**(ว่างเปล่า)** – ผลิตภัณฑ์ที่มีอยู่แล้วใน Sales ก่อนที่โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดจะมีการเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cbcf0-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="cbcf0-137">ฟิลด์ **ถูกรักษาไว้ภายนอก** จะช่วยให้มั่นใจว่า เฉพาะใบเสนอราคาและใบสั่งขายที่ถูกรักษาไว้ภายนอกจะซิงค์กับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbcf0-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="cbcf0-138">ผลิตภัณฑ์รักษาไว้ภายนอกจะถูกเพิ่มไปยังรายการราคาแรกที่ถูกต้องที่มีสกุลเงินเดียวกันโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cbcf0-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="cbcf0-139">รายการราคามีการจัดระเบียบตามตัวอักษรตามชื่อ</span><span class="sxs-lookup"><span data-stu-id="cbcf0-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="cbcf0-140">ราคาขายของผลิตภัณฑ์จาก Finance and Operations ถูกใช้เป็นราคาในรายการราคา</span><span class="sxs-lookup"><span data-stu-id="cbcf0-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="cbcf0-141">ดังนั้น ต้องมีรายการราคาใน Sales สำหรับสกุลเงินขายผลิตภัณฑ์ทุกๆ สกุลใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbcf0-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="cbcf0-142">สกุลเงินของผลิตภัณฑ์ที่สามารถขายได้ที่นำออกใช้ จะถูกตั้งค่าเป็นสกุลเงินทางบัญชีในนิติบุคคลที่ผลิตภัณฑ์ถูกส่งออกมา</span><span class="sxs-lookup"><span data-stu-id="cbcf0-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> <span data-ttu-id="cbcf0-143">การซิงโครไนส์ผลิตภัณฑ์จะไม่สำเร็จ เว้นแต่จะมีราคาตลาดที่มีสกุลเงินที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="cbcf0-143">Product synchronization won't succeed unless there is a price list that has a matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="cbcf0-144">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="cbcf0-144">Preconditions and mapping setup</span></span>

- <span data-ttu-id="cbcf0-145">ก่อนที่คุณจะรันการซิงโครไนส์เป็นครั้งแรก คุณต้องเติมข้อมูลในตารางผลิตภัณฑ์เฉพาะสำหรับผลิตภัณฑ์ที่มีอยู่ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbcf0-145">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="cbcf0-146">จะไม่มีการซิงโครไนส์ผลิตภัณฑ์ที่มีอยู่จนกว่างานนี้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cbcf0-146">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="cbcf0-147">ใน Finance and Operations ให้ใช้ค้นหาเพื่อค้นหา **เติมข้อมูลตารางผลิตภัณฑ์เฉพาะ**</span><span class="sxs-lookup"><span data-stu-id="cbcf0-147">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="cbcf0-148">เลือก **เติมข้อมูลตารางผลิตภัณฑ์เฉพาะ** เพื่อรันงาน</span><span class="sxs-lookup"><span data-stu-id="cbcf0-148">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="cbcf0-149">งานนี้ต้องรันเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="cbcf0-149">This job must be run only one time.</span></span>

- <span data-ttu-id="cbcf0-150">ตรวจสอบให้แน่ใจว่ามีแผนผังค่าที่จำเป็นสำหรับการขายหน่วยวัด (UOM) ระหว่าง Finance and Operations และ Sales มีอยู่ในการแม็ปของ **SalesUnitSymbol** ไปยัง **DefaultUnit (Name)**</span><span class="sxs-lookup"><span data-stu-id="cbcf0-150">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="cbcf0-151">อัพเดตแผนผังค่าสำหรับ **กลุ่มหน่วย** (**defaultuomscheduleid.name**) เพื่อให้ตรงกับ **กลุ่มหน่วย** ใน Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-151">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="cbcf0-152">ค่าเท็มเพลตเริ่มต้นคือ **หน่วยเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="cbcf0-152">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="cbcf0-153">ตรวจสอบให้แน่ใจว่า UOM ในการขายสำหรับผลิตภัณฑ์ทั้งหมดจาก Finance and Operations มีอยู่ใน Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-153">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="cbcf0-154">ตรวจสอบให้แน่ใจว่า มีรายการราคาอยู่ใน Sales สำหรับสกุลเงินขายของผลิตภัณฑ์แต่ละสกุลใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbcf0-154">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="cbcf0-155">เมื่อมีการสร้างผลิตภัณฑ์ใน Sales สามารถมีสถานะเป็น **ร่าง** หรือ **ใช้งานอยู่** ได้</span><span class="sxs-lookup"><span data-stu-id="cbcf0-155">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="cbcf0-156">มีการควบคุมพฤติกรรมที่ **การตั้งค่า** > **การดูแลระบบ** > **การตั้งค่าระบบ** > **การขาย** ใน Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-156">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="cbcf0-157">ผลิตภัณฑ์ที่มีสถานะ **ร่าง** เมื่อมีการสร้าง ต้องถูกเรียกใช้งงานก่อน จึงจะสามารถถูกเพิ่มไปยังใบเสนอราคาหรือใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="cbcf0-157">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cbcf0-158">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cbcf0-158">Template mapping in Data integration</span></span>

<span data-ttu-id="cbcf0-159">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cbcf0-159">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="cbcf0-160">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbcf0-160">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="cbcf0-162">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="cbcf0-162">Related topics</span></span>

[<span data-ttu-id="cbcf0-163">ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="cbcf0-163">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="cbcf0-164">ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbcf0-164">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="cbcf0-165">ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbcf0-165">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="cbcf0-166">ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-166">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="cbcf0-167">ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="cbcf0-167">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




