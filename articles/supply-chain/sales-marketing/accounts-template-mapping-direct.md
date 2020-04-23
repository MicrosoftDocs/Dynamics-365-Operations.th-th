---
title: ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management
description: หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้ในการซิงโครไนส์บัญชีจาก Dynamics 365 Sales ไปยัง Supply Chain Management
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1146fce7cf620a002231a5bc9246c706b97d478d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210145"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="21b2a-103">ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21b2a-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="21b2a-104">ก่อนที่คุณจะสามารถใช้โซลูชันผู้มีแนวโน้มจะเป็นลูกค้าเงินสด คุณควรคุ้นเคยกับ [รวมข้อมูลลงใน Common Data Service สำหรับแอป](https://docs.microsoft.com/powerapps/administrator/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="21b2a-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="21b2a-105">หัวข้อนี้อธิบายแม่แบบและงานพื้นฐานที่ใช้ในการซิงโครไนส์บัญชีจาก Dynamics 365 Sales ไปยัง Dynamics 365 Supply Chain Management โดยตรง</span><span class="sxs-lookup"><span data-stu-id="21b2a-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="21b2a-106">โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="21b2a-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="21b2a-107">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="21b2a-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="21b2a-108">แม่แบบของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดที่มีให้ใช้งานร่วมกันกับคุณลักษณะการรวมข้อมูล ช่วยให้เกิดกระแสของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="21b2a-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="21b2a-109">ภาพประกอบต่อไปนี้ แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="21b2a-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="21b2a-110">[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="21b2a-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="21b2a-111">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="21b2a-111">Templates and tasks</span></span>

<span data-ttu-id="21b2a-112">เมื่อต้องการเข้าถึงแม่แบบที่พร้อมใช้งาน ให้เปิด [Power Apps ศูนย์การจัดการ](https://preview.admin.powerapps.com/dataintegration)</span><span class="sxs-lookup"><span data-stu-id="21b2a-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="21b2a-113">เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="21b2a-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="21b2a-114">แม่แบบและงานพื้นฐานต่อไปนี้ จะถูกใช้ในการซิงโครไนส์บัญชีจาก Sales ไปยัง Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="21b2a-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="21b2a-115">**ชื่อของเท็มเพลตในการรวมข้อมูล:** บัญชี (Sales ไปยัง Fin and Ops) - ตรง</span><span class="sxs-lookup"><span data-stu-id="21b2a-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="21b2a-116">**ชื่อของงานในโครงการ:** บัญชี - ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="21b2a-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="21b2a-117">ไม่มีงานในการซิงโครไนส์จำเป็นต้องใช้ ก่อนการซิงโครไนส์บัญชี/ลูกค้าจะสามารถเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="21b2a-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="21b2a-118">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="21b2a-118">Entity set</span></span>

| <span data-ttu-id="21b2a-119">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="21b2a-119">Sales</span></span>    | <span data-ttu-id="21b2a-120">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21b2a-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="21b2a-121">บัญชี</span><span class="sxs-lookup"><span data-stu-id="21b2a-121">Accounts</span></span> | <span data-ttu-id="21b2a-122">ลูกค้า V2</span><span class="sxs-lookup"><span data-stu-id="21b2a-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="21b2a-123">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="21b2a-123">Entity flow</span></span>

<span data-ttu-id="21b2a-124">บัญชีที่ได้รับการจัดการใน Sales จะถูกซิงโครไนส์ไปยัง Supply Chain Management ในฐานะลูกค้า</span><span class="sxs-lookup"><span data-stu-id="21b2a-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="21b2a-125">คุณสมบัติ **ถูกรักษาไว้สำหรับภายนอก** ในลูกค้าเหล่านี้ถูกตั้งค่าเป็น **ใช่** เพื่อติดตามลูกค้าที่มีต้นกำเนิดมาจาก Sales</span><span class="sxs-lookup"><span data-stu-id="21b2a-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="21b2a-126">ในระหว่างการออกใบแจ้งหนี้ ข้อมูลนี้จะถูกใช้เพื่อกรองข้อมูลใบแจ้งหนี้ที่ถูกซิงค์โครไนซ์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="21b2a-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="21b2a-127">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="21b2a-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="21b2a-128">ฟิลด์ **หมายเลขบัญชี** จะพร้อมใช้งานบนหน้า **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="21b2a-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="21b2a-129">ซึ่งถูกทำให้เป็นคีย์เฉพาะและธรรมชาติ เพื่อสนับสนุนการรวม</span><span class="sxs-lookup"><span data-stu-id="21b2a-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="21b2a-130">คุณลักษณะคีย์ธรรมชาติของโซลูชันการจัดการความสัมพันธ์กับลูกค้า (CRM) อาจส่งผลกระทบต่อลูกค้าที่ใช้ฟิลด์ **หมายเลขบัญชี** อยู่แล้ว แต่จะไม่ส่งผลกระทบต่อลูกค้าที่ไม่ได้ใช้ค่า **หมายเลขบัญชี** สำหรับแต่ละบัญชี</span><span class="sxs-lookup"><span data-stu-id="21b2a-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="21b2a-131">ในปัจจุบัน โซลูชันการรวมไม่สนับสนุนกรณีนี้</span><span class="sxs-lookup"><span data-stu-id="21b2a-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="21b2a-132">เมื่อมีการสร้างบัญชีใหม่ ถ้าค่า **หมายเลขบัญชี** ไม่ได้มีอยู่แล้ว ระบบจะสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="21b2a-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="21b2a-133">ค่าประกอบด้วย **ACC** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ</span><span class="sxs-lookup"><span data-stu-id="21b2a-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="21b2a-134">นี่คือตัวอย่าง: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="21b2a-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="21b2a-135">เมื่อมีการใช้โซลูชันการรวมสำหรับ Sales สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **หมายเลขบัญชี** สำหรับบัญชีที่มีอยู่ใน Sales</span><span class="sxs-lookup"><span data-stu-id="21b2a-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="21b2a-136">ถ้าไม่มีค่า **หมายเลขบัญชี** ลำดับหมายเลขที่ได้กล่าวถึงก่อนหน้านี้จะถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="21b2a-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="21b2a-137">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="21b2a-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="21b2a-138">การแม็ป **CustomerGroupId** จะต้องถูกอัพเดตเพื่อให้เป็นค่าที่ถูกต้องใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21b2a-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="21b2a-139">คุณสามารถระบุค่าเริ่มต้น หรือคุณสามารถตั้งค่าโดยใช้แผนผังค่า</span><span class="sxs-lookup"><span data-stu-id="21b2a-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="21b2a-140">ค่าเท็มเพลตเริ่มต้นคือ **10**</span><span class="sxs-lookup"><span data-stu-id="21b2a-140">The default template value is **10**.</span></span>

- <span data-ttu-id="21b2a-141">โดยการเพิ่มการแม็ปต่อไปนี้ คุณสามารถช่วยลดจำนวนการอัพเดตที่จำเป็นด้วยตนเองใน Supply Chain Management ได้</span><span class="sxs-lookup"><span data-stu-id="21b2a-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="21b2a-142">คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้</span><span class="sxs-lookup"><span data-stu-id="21b2a-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="21b2a-143">**SiteId** – จำเป็นต้องมีไซต์เพื่อสร้างรายการใบเสนอราคาและใบสั่งขายใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21b2a-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="21b2a-144">สามารถนำไซต์เริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งได้</span><span class="sxs-lookup"><span data-stu-id="21b2a-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="21b2a-145">ค่าเท็มเพลตเริ่มต้นคือ **1**</span><span class="sxs-lookup"><span data-stu-id="21b2a-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="21b2a-146">**WarehouseId** – จำเป็นต้องมีคลังสินค้าเพื่อดำเนินการกับรายการใบเสนอราคาและใบสั่งขายใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21b2a-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="21b2a-147">สามารถนำคลังสินค้าเริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งใน Supply Chain Management ได้</span><span class="sxs-lookup"><span data-stu-id="21b2a-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="21b2a-148">ค่าเท็มเพลตเริ่มต้นคือ **13**</span><span class="sxs-lookup"><span data-stu-id="21b2a-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="21b2a-149">**LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างรายการใบเสนอราคาและใบสั่งขายใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21b2a-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="21b2a-150">โดยค่าเริ่มต้น จะใช้ภาษาจากส่วนหน้าของใบสั่งจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="21b2a-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="21b2a-151">ค่าเท็มเพลตเริ่มต้นคือ **en-us**</span><span class="sxs-lookup"><span data-stu-id="21b2a-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="21b2a-152">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="21b2a-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="21b2a-153">ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการจัดส่ง** และ **วิธีการจัดส่ง** ไม่ได้รวมอยู่ในการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="21b2a-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="21b2a-154">หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง</span><span class="sxs-lookup"><span data-stu-id="21b2a-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="21b2a-155">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="21b2a-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="21b2a-156">การแม็ปจะช่วยแสดงให้เห็นว่า ข้อมูลฟิลด์ใดที่จะถูกซิงโครไนส์จาก Sales ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21b2a-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="21b2a-158">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="21b2a-158">Related topics</span></span>


[<span data-ttu-id="21b2a-159">ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด</span><span class="sxs-lookup"><span data-stu-id="21b2a-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="21b2a-160">ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21b2a-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="21b2a-161">ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21b2a-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="21b2a-162">การซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Sales และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="21b2a-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="21b2a-163">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Supply Chain Management ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="21b2a-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

