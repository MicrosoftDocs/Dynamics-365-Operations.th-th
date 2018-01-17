---
title: "ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition"
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 03afaa48469453c6aa07a7a84a2c115b05ba4573
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="85783-103">ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="85783-103">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="85783-104">ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดได้ คุณควรทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration)</span><span class="sxs-lookup"><span data-stu-id="85783-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="85783-105">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีโดยตรงจาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="85783-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="85783-106">โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="85783-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="85783-107">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="85783-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span>  <span data-ttu-id="85783-108">เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล จะเปิดใช้งานขั้นตอนของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="85783-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="85783-109">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="85783-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="85783-110">[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="85783-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="85783-111">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="85783-111">Templates and tasks</span></span>

<span data-ttu-id="85783-112">เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน เปิด [ศูนย์การจัดการ PowerApps](https://preview.admin.powerapps.com/dataintegration)</span><span class="sxs-lookup"><span data-stu-id="85783-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="85783-113">เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="85783-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="85783-114">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์บัญชีจาก Sales ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="85783-114">The following template and underlying task are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="85783-115">**ชื่อของเท็มเพลตในการรวมข้อมูล:** บัญชี (Sales ไปยัง Fin and Ops) - ตรง</span><span class="sxs-lookup"><span data-stu-id="85783-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="85783-116">**ชื่อของงานในโครงการ:** บัญชี - ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="85783-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="85783-117">ไม่มีงานในการซิงโครไนส์จำเป็นต้องใช้ ก่อนการซิงโครไนส์บัญชี/ลูกค้าจะสามารถเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="85783-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="85783-118">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="85783-118">Entity set</span></span>

| <span data-ttu-id="85783-119">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="85783-119">Sales</span></span>    | <span data-ttu-id="85783-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="85783-120">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="85783-121">บัญชี</span><span class="sxs-lookup"><span data-stu-id="85783-121">Accounts</span></span> | <span data-ttu-id="85783-122">ลูกค้า V2</span><span class="sxs-lookup"><span data-stu-id="85783-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="85783-123">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="85783-123">Entity flow</span></span>

<span data-ttu-id="85783-124">บัญชีจะถูกจัดการใน Sales และจะถูกซิงโครไนส์ไปยัง Finance and Operations ในฐานะลูกค้า</span><span class="sxs-lookup"><span data-stu-id="85783-124">Accounts are managed in Sales and synchronized to Finance and Operations as customers.</span></span> <span data-ttu-id="85783-125">คุณสมบัติ **ถูกรักษาไว้สำหรับภายนอก** ในลูกค้าเหล่านี้ถูกตั้งค่าเป็น **ใช่** เพื่อติดตามลูกค้าที่มีต้นกำเนิดมาจาก Sales</span><span class="sxs-lookup"><span data-stu-id="85783-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="85783-126">ในระหว่างการออกใบแจ้งหนี้ ข้อมูลนี้จะถูกใช้เพื่อกรองข้อมูลใบแจ้งหนี้ที่ถูกซิงค์โครไนซ์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="85783-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="85783-127">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="85783-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="85783-128">ฟิลด์ **หมายเลขบัญชี** จะพร้อมใช้งานบนหน้า **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="85783-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="85783-129">ซึ่งถูกทำให้เป็นคีย์เฉพาะและธรรมชาติ เพื่อสนับสนุนการรวม</span><span class="sxs-lookup"><span data-stu-id="85783-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="85783-130">คุณลักษณะคีย์ธรรมชาติของโซลูชันการจัดการความสัมพันธ์กับลูกค้า (CRM) อาจส่งผลกระทบต่อลูกค้าที่ใช้ฟิลด์ **หมายเลขบัญชี** อยู่แล้ว แต่จะไม่ส่งผลกระทบต่อลูกค้าที่ไม่ได้ใช้ค่า **หมายเลขบัญชี** สำหรับแต่ละบัญชี</span><span class="sxs-lookup"><span data-stu-id="85783-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="85783-131">ในปัจจุบัน โซลูชันการรวมไม่สนับสนุนกรณีนี้</span><span class="sxs-lookup"><span data-stu-id="85783-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="85783-132">เมื่อมีการสร้างบัญชีใหม่ ถ้าค่า **หมายเลขบัญชี** ไม่ได้มีอยู่แล้ว ระบบจะสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="85783-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="85783-133">ค่าประกอบด้วย **ACC** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ</span><span class="sxs-lookup"><span data-stu-id="85783-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="85783-134">นี่คือตัวอย่าง: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="85783-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="85783-135">เมื่อมีการใช้โซลูชันการรวมสำหรับ Sales สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **หมายเลขบัญชี** สำหรับบัญชีที่มีอยู่ใน Sales</span><span class="sxs-lookup"><span data-stu-id="85783-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="85783-136">ถ้าไม่มีค่า **หมายเลขบัญชี** ลำดับหมายเลขที่ได้กล่าวถึงก่อนหน้านี้จะถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="85783-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="85783-137">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="85783-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="85783-138">การแม็ป **CustomerGroupId** จะต้องถูกอัพเดตเป็นค่าที่ถูกต้องใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="85783-138">The **CustomerGroupId** mapping must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="85783-139">คุณสามารถระบุค่าเริ่มต้น หรือคุณสามารถตั้งค่าโดยใช้แผนผังค่า</span><span class="sxs-lookup"><span data-stu-id="85783-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="85783-140">ค่าเท็มเพลตเริ่มต้นคือ **10**</span><span class="sxs-lookup"><span data-stu-id="85783-140">The default template value is **10**.</span></span>

- <span data-ttu-id="85783-141">โดยการเพิ่มการแม็ปต่อไปนี้ คุณสามารถช่วยลดจำนวนการอัพเดตด้วยตนเองที่จำเป็นใน Finance and Operations ได้</span><span class="sxs-lookup"><span data-stu-id="85783-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="85783-142">คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้</span><span class="sxs-lookup"><span data-stu-id="85783-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="85783-143">**SiteId** – จำเป็นต้องมีไซต์เพื่อสร้างบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="85783-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="85783-144">สามารถนำไซต์เริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งได้</span><span class="sxs-lookup"><span data-stu-id="85783-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="85783-145">ค่าเท็มเพลตเริ่มต้นคือ **1**</span><span class="sxs-lookup"><span data-stu-id="85783-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="85783-146">**WarehouseId** – จำเป็นต้องมีคลังสินค้าเพื่อดำเนินการกับบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="85783-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="85783-147">สามารถนำคลังสินค้าเริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งใน Finance and Operations ได้</span><span class="sxs-lookup"><span data-stu-id="85783-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span>

        <span data-ttu-id="85783-148">ค่าเท็มเพลตเริ่มต้นคือ **13**</span><span class="sxs-lookup"><span data-stu-id="85783-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="85783-149">**LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างใบเสนอราคาและใบสั่งขายใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="85783-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="85783-150">โดยค่าเริ่มต้น จะใช้ภาษาจากส่วนหน้าของใบสั่งจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="85783-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="85783-151">ค่าเท็มเพลตเริ่มต้นคือ **en-us**</span><span class="sxs-lookup"><span data-stu-id="85783-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="85783-152">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="85783-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="85783-153">ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการจัดส่ง** และ **วิธีการจัดส่ง** ไม่ได้รวมอยู่ในการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="85783-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="85783-154">หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง</span><span class="sxs-lookup"><span data-stu-id="85783-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="85783-155">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="85783-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="85783-156">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="85783-156">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="85783-158">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="85783-158">Related topics</span></span>


[<span data-ttu-id="85783-159">ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="85783-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="85783-160">ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="85783-160">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="85783-161">ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="85783-161">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="85783-162">ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="85783-162">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)

[<span data-ttu-id="85783-163">ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="85783-163">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)


