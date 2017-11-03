---
title: "ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="50b7e-103">ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50b7e-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="50b7e-104">ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ให้ทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration)</span><span class="sxs-lookup"><span data-stu-id="50b7e-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="50b7e-105">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Sales (Sales) ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="50b7e-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="50b7e-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="50b7e-106">Template and task</span></span>

<span data-ttu-id="50b7e-107">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์บัญชีจาก Sales ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="50b7e-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="50b7e-108">**ชื่อของเท็มเพลต:**บัญชี (Sales ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="50b7e-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="50b7e-109">**ชื่อของงานในโครงการ:** บัญชี - บัญชี - ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="50b7e-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="50b7e-110">ซิงค์งานที่จำเป็นก่อนการซิงค์บัญชี / ลูกค้า: ไม่มี</span><span class="sxs-lookup"><span data-stu-id="50b7e-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="50b7e-111">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="50b7e-111">Entity set</span></span>

| <span data-ttu-id="50b7e-112">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="50b7e-112">Sales</span></span>    | <span data-ttu-id="50b7e-113">CDS</span><span class="sxs-lookup"><span data-stu-id="50b7e-113">CDS</span></span>     | <span data-ttu-id="50b7e-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50b7e-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="50b7e-115">บัญชี</span><span class="sxs-lookup"><span data-stu-id="50b7e-115">Accounts</span></span> | <span data-ttu-id="50b7e-116">บัญชี</span><span class="sxs-lookup"><span data-stu-id="50b7e-116">Account</span></span> | <span data-ttu-id="50b7e-117">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="50b7e-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="50b7e-118">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="50b7e-118">Entity flow</span></span>

<span data-ttu-id="50b7e-119">บัญชีจะถูกจัดการใน Sales และจะถูกซิงโครไนส์ไปยัง Finance and Operations โดยเป็นลูกค้า</span><span class="sxs-lookup"><span data-stu-id="50b7e-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="50b7e-120">คุณสมบัติ **ถูกรักษาไว้สำหรับภายนอก** ในลูกค้าเหล่านี้ถูกตั้งค่าเป็น **ใช่** เพื่อติดตามลูกค้าที่มีต้นกำเนิดมาจาก Sales</span><span class="sxs-lookup"><span data-stu-id="50b7e-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="50b7e-121">ในระหว่างการออกใบแจ้งหนี้ ข้อมูลนี้จะถูกใช้เพื่อกรองข้อมูลใบแจ้งหนี้ที่ถูกซิงค์โครไนซ์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="50b7e-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="50b7e-122">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="50b7e-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="50b7e-123">ฟิลด์ **หมายเลขบัญชี** จะพร้อมใช้งานบนหน้า **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="50b7e-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="50b7e-124">ซึ่งถูกทำให้เป็นคีย์เฉพาะและธรรมชาติเพื่อสนับสนุนการรวม</span><span class="sxs-lookup"><span data-stu-id="50b7e-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="50b7e-125">คุณลักษณะคีย์ธรรมชาติของโซลูชันการจัดการความสัมพันธ์กับลูกค้า (CRM) อาจส่งผลกระทบต่อลูกค้าที่ใช้ฟิลด์ **หมายเลขบัญชี** อยู่แล้ว แต่จะไม่ส่งผลกระทบต่อลูกค้าที่ไม่ได้ใช้ค่า **หมายเลขบัญชี** สำหรับแต่ละบัญชี</span><span class="sxs-lookup"><span data-stu-id="50b7e-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="50b7e-126">ในปัจจุบัน โซลูชันการรวมไม่สนับสนุนกรณีนี้</span><span class="sxs-lookup"><span data-stu-id="50b7e-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="50b7e-127">เมื่อมีการสร้างบัญชีใหม่ ถ้าค่า **หมายเลขบัญชี** ไม่ได้มีอยู่แล้ว ระบบจะสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="50b7e-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="50b7e-128">ค่าประกอบด้วย **ACC** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ</span><span class="sxs-lookup"><span data-stu-id="50b7e-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="50b7e-129">นี่คือตัวอย่าง: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="50b7e-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="50b7e-130">เมื่อมีการใช้โซลูชันการรวมสำหรับ Sales สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **หมายเลขบัญชี** สำหรับบัญชีที่มีอยู่ใน Sales</span><span class="sxs-lookup"><span data-stu-id="50b7e-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="50b7e-131">ถ้าไม่มีค่า **หมายเลขบัญชี** ลำดับหมายเลขที่ได้อธิบายไว้ก่อนหน้านี้จะถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="50b7e-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="50b7e-132">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="50b7e-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="50b7e-133">**CustomerGroupId** ที่แม็ปจาก **CDS &gt; ปลายทาง** จะต้องถูกอัพเดตเป็นค่าที่ถูกต้องใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50b7e-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="50b7e-134">คุณสามารถระบุค่าเริ่มต้น หรือคุณสามารถตั้งค่าโดยใช้แผนผังค่า</span><span class="sxs-lookup"><span data-stu-id="50b7e-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="50b7e-135">ค่าเท็มเพลตเริ่มต้นคือ **10**</span><span class="sxs-lookup"><span data-stu-id="50b7e-135">The default template value is **10**.</span></span>
- <span data-ttu-id="50b7e-136">จำเป็นต้องมี **รหัสประเทศ/ภูมิภาคของที่อยู่** ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50b7e-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="50b7e-137">เพื่อหลีกเลี่ยงข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ปจาก **CDS &gt; ปลายทาง**</span><span class="sxs-lookup"><span data-stu-id="50b7e-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="50b7e-138">จากนั้นค่าเริ่มต้นจะถูกนำมาใช้ถ้าฟิลด์ถูกปล่อยว่างไว้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="50b7e-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="50b7e-139">เท็มเพลตเริ่มต้นสำหรับ **AddressCountryRegionISOCode** คือ **USA**</span><span class="sxs-lookup"><span data-stu-id="50b7e-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="50b7e-140">เท็มเพลตเริ่มต้นสำหรับ **DeliveryAddressCountryRegionISOCode** คือ **USA**</span><span class="sxs-lookup"><span data-stu-id="50b7e-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="50b7e-141">โดยการเพิ่มการแม็ปต่อไปนี้จาก **CDS&gt; ปลายทาง** คุณสามารถช่วยลดจำนวนการอัพเดตด้วยตนเองที่จำเป็นใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50b7e-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="50b7e-142">คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้</span><span class="sxs-lookup"><span data-stu-id="50b7e-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="50b7e-143">**SiteId** – จำเป็นต้องมีไซต์เพื่อสร้างบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50b7e-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="50b7e-144">สามารถนำไซต์เริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งได้</span><span class="sxs-lookup"><span data-stu-id="50b7e-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="50b7e-145">เท็มเพลตเริ่มต้นสำหรับ **SiteId** คือ **1**</span><span class="sxs-lookup"><span data-stu-id="50b7e-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="50b7e-146">**WarehouseId** – จำเป็นต้องมีคลังสินค้าเพื่อดำเนินการกับบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50b7e-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="50b7e-147">สามารถนำคลังสินค้าเริ่มต้นจากผลิตภัณฑ์หรือจากลูกค้าอย่างใดอย่างหนึ่งจากส่วนหน้าของใบสั่งใน Finance and Operations ได้</span><span class="sxs-lookup"><span data-stu-id="50b7e-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="50b7e-148">เท็มเพลตเริ่มต้นสำหรับ **WarehouseId** คือ **13**</span><span class="sxs-lookup"><span data-stu-id="50b7e-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="50b7e-149">**LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างใบเสนอราคาและใบสั่งขายใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50b7e-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="50b7e-150">โดยค่าเริ่มต้น จะใช้ภาษาจากส่วนหน้าของใบสั่งจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="50b7e-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="50b7e-151">เท็มเพลตเริ่มต้นสำหรับ **LanguageId** คือ **en-us**</span><span class="sxs-lookup"><span data-stu-id="50b7e-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="50b7e-152">อัพเดตรหัสองค์กรCDS (**Organization_OrganizationId**) ในการแม็ป **ต้นทาง &gt; CDS**</span><span class="sxs-lookup"><span data-stu-id="50b7e-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="50b7e-153">ค่าเท็มเพลตเริ่มต้นคือ **ORG001**</span><span class="sxs-lookup"><span data-stu-id="50b7e-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="50b7e-154">การแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="50b7e-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="50b7e-155">ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการจัดส่ง** และ **วิธีการจัดส่ง** ไม่ได้รวมอยู่ในการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="50b7e-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="50b7e-156">เมื่อต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่า</span><span class="sxs-lookup"><span data-stu-id="50b7e-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="50b7e-157">การแม็ปค่าเกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่างทั้งสองรายการ</span><span class="sxs-lookup"><span data-stu-id="50b7e-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="50b7e-158">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="50b7e-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/accounts-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตสำหรับบัญชีในตัวรวมข้อมูล](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="50b7e-161">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="50b7e-161">Related topics</span></span>

[<span data-ttu-id="50b7e-162">ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="50b7e-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="50b7e-163">ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50b7e-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="50b7e-164">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50b7e-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="50b7e-165">ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="50b7e-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="50b7e-166">ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้จาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="50b7e-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




