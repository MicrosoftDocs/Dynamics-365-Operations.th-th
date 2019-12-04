---
title: ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อและรายชื่อลูกค้าใน Supply Chain Management
description: หัวข้อนี้จะอธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์เอนทิตีผู้ติดต่อ (ผู้ติดต่อ) และผู้ติดต่อ (ลูกค้า) จาก Dynamics 365 Sales ไปยัง Dynamics 365 Supply Chain Management
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 141464f2ce7cb4ccfd2a8fb7a266e657e8f52015
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814132"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="3efac-103">ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อและรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="3efac-104">ก่อนที่คุณจะสามารถใช้โซลูชันผู้มีแนวโน้มจะเป็นลูกค้าเงินสด คุณควรคุ้นเคยกับ [รวมข้อมูลลงใน Common Data Service สำหรับแอป](https://docs.microsoft.com/powerapps/administrator/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="3efac-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="3efac-105">หัวข้อนี้จะอธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์เอนทิตีผู้ติดต่อ (ผู้ติดต่อ) และผู้ติดต่อ (ลูกค้า) จาก Dynamics 365 Sales ไปยัง Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="3efac-106">โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="3efac-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="3efac-107">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="3efac-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="3efac-108">แม่แบบของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดที่มีให้ใช้งานร่วมกันกับคุณลักษณะการรวมข้อมูล ช่วยให้เกิดกระแสของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="3efac-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="3efac-109">ภาพประกอบต่อไปนี้ แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Supply Chain Management และ Sales</span><span class="sxs-lookup"><span data-stu-id="3efac-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="3efac-110">[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="3efac-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3efac-111">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="3efac-111">Templates and tasks</span></span>

<span data-ttu-id="3efac-112">เมื่อต้องการเข้าถึงแม่แบบที่พร้อมใช้งาน ให้เปิด [ศูนย์การจัดการ PowerApps](https://preview.admin.powerapps.com/dataintegration)</span><span class="sxs-lookup"><span data-stu-id="3efac-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="3efac-113">เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="3efac-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3efac-114">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์เอนทิตีผู้ติดต่อ (ผู้ติดต่อ) ใน Sales ไปยังเอนทิตีผู้ติดต่อ (ลูกค้า) ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Supply Chain Management.</span></span>

- <span data-ttu-id="3efac-115">**ชื่อของเท็มเพลตในการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3efac-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="3efac-116">ผู้ติดต่อ (Sales to Supply Chain Management) - โดยตรง</span><span class="sxs-lookup"><span data-stu-id="3efac-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="3efac-117">ผู้ติดต่อไปยังลูกค้า (Sales to Supply Chain Management) - โดยตรง</span><span class="sxs-lookup"><span data-stu-id="3efac-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="3efac-118">**ชื่อของงานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3efac-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="3efac-119">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="3efac-119">Contacts</span></span>
    - <span data-ttu-id="3efac-120">ผู้ติดต่อไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3efac-120">ContactToCustomer</span></span>

<span data-ttu-id="3efac-121">ก่อนที่จะซิงโครไนส์ผู้ติดต่อ คุณต้องทำการซิงโครไนส์: บัญชี (Sales ไปยัง Supply Chain Management) ก่อน</span><span class="sxs-lookup"><span data-stu-id="3efac-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="3efac-122">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3efac-122">Entity sets</span></span>

| <span data-ttu-id="3efac-123">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3efac-123">Sales</span></span>    | <span data-ttu-id="3efac-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="3efac-125">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="3efac-125">Contacts</span></span> | <span data-ttu-id="3efac-126">ผู้ติดต่อ CDS</span><span class="sxs-lookup"><span data-stu-id="3efac-126">CDS Contacts</span></span>           |
| <span data-ttu-id="3efac-127">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="3efac-127">Contacts</span></span> | <span data-ttu-id="3efac-128">ลูกค้า V2</span><span class="sxs-lookup"><span data-stu-id="3efac-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="3efac-129">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="3efac-129">Entity flow</span></span>

<span data-ttu-id="3efac-130">ผู้ติดต่อจะถูกจัดการใน Sales และถูกซิงโครไนส์ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="3efac-131">ผู้ติดต่อใน Sales สามารถเป็นผู้ติดต่อหรือลูกค้าก็ได้ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="3efac-132">เพื่อที่จะระบุว่าผู้ติดต่อใน Sales ที่จะซิงโครไนส์ไปยัง Supply Chain Management ควรจะมีฐานะเป็นผู้ติดต่อหรือลูกค้า ระบบจะพิจารณาจากคุณสมบัติจากผู้ติดต่อใน Sales ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3efac-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="3efac-133">**การซิงโครไนส์ไปยังลูกค้าใน Supply Chain Management:** ผู้ติดต่อที่ซึ่ง **เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="3efac-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="3efac-134">**การซิงโครไนส์ไปยังผู้ติดต่อใน Supply Chain Management:** ผู้ติดต่อที่ซึ่ง **เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ไม่ใช่** และ **บริษัท** (บัญชี/ผู้ติดต่อหลัก) ชี้ไปยังบัญชี (ไม่ใช่ผู้ติดต่อ)</span><span class="sxs-lookup"><span data-stu-id="3efac-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="3efac-135">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="3efac-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="3efac-136">มีการเพิ่มฟิลด์ **เป็นลูกค้าที่ใช้งานอยู่** ใหม่ ไปยังผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="3efac-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="3efac-137">ฟิลด์นี้จะถูกใช้เพื่อแยกความแตกต่างของผู้ติดต่อที่มีกิจกรรมการขายและผู้ติดต่อที่ไม่มีกิจกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="3efac-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="3efac-138">**เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ใช่** สำหรับผู้ติดต่อที่มีใบเสนอราคา ใบสั่ง หรือใบแจ้งหนี้ที่เกี่ยวข้องเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3efac-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="3efac-139">เฉพาะผู้ติดต่อเหล่านั้นที่จะถูกซิงโครไนส์กับ Supply Chain Management ในฐานะลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3efac-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="3efac-140">มีการเพิ่มฟิลด์ **IsCompanyAnAccount** ใหม่ ไปยังผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="3efac-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="3efac-141">ฟิลด์นี้บ่งชี้ว่าผู้ติดต่อถูกเชื่อมโยงกับบริษัท (บัญชี/ผู้ติดต่อหลัก) ของชนิด **บัญชี** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3efac-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="3efac-142">ข้อมูลนี้จะถูกใช้ในการระบุผู้ติดต่อที่จะซิงโครไนส์กับ Supply Chain Management ในฐานะผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="3efac-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="3efac-143">มีการเพิ่มฟิลด์ **หมายเลขผู้ติดต่อ** ไปยังผู้ติดต่อ เพื่อช่วยรับประกันคีย์ธรรมชาติและคีย์เฉพาะสำหรับการรวม</span><span class="sxs-lookup"><span data-stu-id="3efac-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="3efac-144">เมื่อมีการสร้างผู้ติดต่อใหม่ ค่า **หมายเลขผู้ติดต่อ** จะถูกสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="3efac-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="3efac-145">ค่าประกอบด้วย **CON** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ</span><span class="sxs-lookup"><span data-stu-id="3efac-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="3efac-146">นี่คือตัวอย่าง: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="3efac-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="3efac-147">เมื่อมีการใช้งานโซลูชันการรวมสำหรับ Sales สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **หมายเลขผู้ติดต่อ** สำหรับผู้ติดต่อที่มีอยู่โดยใช้ลำดับหมายเลขที่มีการกล่าวถึงก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3efac-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="3efac-148">สคริปต์การอัพเกรดยังตั้งค่าฟิลด์ **เป็นลูกค้าที่ใช้งานอยู่** เป็น **ใช่** สำหรับผู้ติดต่อใด ๆ ที่มีกิจกรรมการขายอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="3efac-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="3efac-149">ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-149">In Supply Chain Management</span></span>

<span data-ttu-id="3efac-150">ผู้ติดต่อจะถูกแท็กโดยใช้คุณสมบัติ **IsContactPersonExternallyMaintained**</span><span class="sxs-lookup"><span data-stu-id="3efac-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="3efac-151">คุณสมบัตินี้บ่งชี้ว่าผู้ติดต่อที่กำหนดถูกรักษาไว้ภายนอก</span><span class="sxs-lookup"><span data-stu-id="3efac-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="3efac-152">ในกรณีนี้ ผู้ติดต่อที่ถูกรักษาไว้ภายนอกจะถูกรักษาไว้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="3efac-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="3efac-153">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="3efac-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="3efac-154">ผู้ติดต่อไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3efac-154">Contact to customer</span></span>

- <span data-ttu-id="3efac-155">**CustomerGroup** จำเป็นต้องใช้ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="3efac-156">เพื่อช่วยในการป้องกันข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ปได้</span><span class="sxs-lookup"><span data-stu-id="3efac-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="3efac-157">จากนั้นค่าเริ่มต้นจะถูกนำมาใช้ถ้าฟิลด์ถูกปล่อยว่างไว้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="3efac-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="3efac-158">ค่าเท็มเพลตเริ่มต้นคือ **10**</span><span class="sxs-lookup"><span data-stu-id="3efac-158">The default template value is **10**.</span></span>

- <span data-ttu-id="3efac-159">โดยการเพิ่มการแม็ปต่อไปนี้ คุณสามารถช่วยลดจำนวนการอัพเดตที่จำเป็นด้วยตนเองใน Supply Chain Management ได้</span><span class="sxs-lookup"><span data-stu-id="3efac-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="3efac-160">คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้</span><span class="sxs-lookup"><span data-stu-id="3efac-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="3efac-161">**SiteId** – นอกจากนี้คุณยังสามารถกำหนดไซต์เริ่มต้นบนผลิตภัณฑ์ใน Supply Chain Management ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="3efac-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="3efac-162">จำเป็นต้องมีไซต์เพื่อสร้างใบสั่งขายและใบเสนอราคาใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="3efac-163">ไม่ได้กำหนดค่าเท็มเพลตสำหรับ **SiteId** ไว้</span><span class="sxs-lookup"><span data-stu-id="3efac-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="3efac-164">**WarehouseId** – นอกจากนี้คุณยังสามารถกำหนดคลังสินค้าเริ่มต้นบนผลิตภัณฑ์ใน Supply Chain Management ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="3efac-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="3efac-165">จำเป็นต้องมีคลังสินค้าเพื่อสร้างใบสั่งขายและใบเสนอราคาใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="3efac-166">ไม่ได้กำหนดค่าเท็มเพลตสำหรับ **WarehouseId** ไว้</span><span class="sxs-lookup"><span data-stu-id="3efac-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="3efac-167">**LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างรายการใบเสนอราคาและใบสั่งขายใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="3efac-168">ค่าเท็มเพลตเริ่มต้นสำหรับคือ **en-us**</span><span class="sxs-lookup"><span data-stu-id="3efac-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3efac-169">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3efac-169">Template mapping in Data integration</span></span>

<span data-ttu-id="3efac-170">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3efac-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="3efac-171">การแม็ปจะช่วยแสดงให้เห็นว่า ข้อมูลฟิลด์ใดที่จะถูกซิงโครไนส์จาก Sales ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-171">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="3efac-172">ผู้ติดต่อไปยังผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="3efac-172">Contact to contact</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="3efac-174">ผู้ติดต่อไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3efac-174">Contact to customer</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="3efac-176">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3efac-176">Related topics</span></span>

[<span data-ttu-id="3efac-177">ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด</span><span class="sxs-lookup"><span data-stu-id="3efac-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="3efac-178">ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="3efac-179">ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="3efac-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="3efac-180">การซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Sales และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3efac-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="3efac-181">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Supply Chain Management ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="3efac-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)


