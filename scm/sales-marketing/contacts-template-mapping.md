---
title: "ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ผู้ติดต่อ (ผู้ติดต่อ) และผู้ติดต่อ (ลูกค้า) จาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition"
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 7a856a9460d092925a34a0733f37f89354c2ddf1
ms.contentlocale: th-th
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="201cf-103">ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="201cf-104">ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ให้ทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration)</span><span class="sxs-lookup"><span data-stu-id="201cf-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="201cf-105">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์เอนทิตี้ผู้ติดต่อ (ผู้ติดต่อ) และผู้ติดต่อ (ลูกค้า) จาก Microsoft Dynamics 365 for Sales (Sales) ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="201cf-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="201cf-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="201cf-106">Templates and tasks</span></span>

<span data-ttu-id="201cf-107">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ผู้ติดต่อ (ผู้ติดต่อ) ใน Sales ไปยังผู้ติดต่อ (ลูกค้า) Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="201cf-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="201cf-108">**ชื่อของเท็มเพลต:**</span><span class="sxs-lookup"><span data-stu-id="201cf-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="201cf-109">ผู้ติดต่อไปยังผู้ติดต่อ (Sales ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="201cf-109">Contacts to Contact (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="201cf-110">ผู้ติดต่อไปยังลูกค้า (Sales ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="201cf-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="201cf-111">**ชื่อของงานในโครงการ:**</span><span class="sxs-lookup"><span data-stu-id="201cf-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="201cf-112">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="201cf-112">Contacts</span></span>
    - <span data-ttu-id="201cf-113">ผู้ติดต่อไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="201cf-113">ContactToCustomer</span></span>

<span data-ttu-id="201cf-114">จำเป็นต้องมีงานการซิงโครไนส์ต่อไปนี้ก่อนการซิงโครไนส์ผู้ติดต่อ: บัญชี (Sales ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="201cf-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="201cf-115">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="201cf-115">Entity sets</span></span>

| <span data-ttu-id="201cf-116">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="201cf-116">Sales</span></span>    | <span data-ttu-id="201cf-117">CDS</span><span class="sxs-lookup"><span data-stu-id="201cf-117">CDS</span></span>     | <span data-ttu-id="201cf-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="201cf-119">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="201cf-119">Contacts</span></span> | <span data-ttu-id="201cf-120">การติดต่อ</span><span class="sxs-lookup"><span data-stu-id="201cf-120">Contact</span></span> | <span data-ttu-id="201cf-121">ผู้ติดต่อ CDS</span><span class="sxs-lookup"><span data-stu-id="201cf-121">CDS Contacts</span></span>           |
| <span data-ttu-id="201cf-122">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="201cf-122">Contacts</span></span> | <span data-ttu-id="201cf-123">บัญชี</span><span class="sxs-lookup"><span data-stu-id="201cf-123">Account</span></span> | <span data-ttu-id="201cf-124">ลูกค้า V2</span><span class="sxs-lookup"><span data-stu-id="201cf-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="201cf-125">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="201cf-125">Entity flow</span></span>

<span data-ttu-id="201cf-126">มีการจัดการผู้ติดต่อใน Sales และซิงโครไนส์ไปยัง Common Data Service (CDS) และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="201cf-127">ผู้ติดต่อใน Sales สามารถกลายเป็น ผู้ติดต่อ ใน CDS และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="201cf-128">อีกทางหนึ่งคือ สามารถกลายเป็นบัญชีผู้ใช้ใน CDS และลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="201cf-129">เมื่อต้องการระบุว่าผู้ติดต่อควรจะเบิกสินค้าใน Sales สำหรับการซิงโครไนส์กับ CDS และ Finance and Operations (ตัวอย่างเช่น ผู้ติดต่อใน Sales &gt; ติดต่อใน CDS &gt; ผู้ติดต่อใน Finance and Operations) ระบบจะค้นหาคุณสมบัติต่อไปนี้ในผู้ติดต่อใน Sales:</span><span class="sxs-lookup"><span data-stu-id="201cf-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="201cf-130">**ซิงค์กับบัญชีใน CDS และลูกค้าใน Finance and Operations:** ผู้ติดต่อที่มีการตั้งค่า **เป็นลูกค้าที่ใช้งานอยู่** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="201cf-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="201cf-131">**ซิงค์กับผู้ติดต่อใน CDS และผู้ติดต่อใน Finance and Operations:** ผู้ติดต่อที่มีการตั้งค่า **เป็นลูกค้าที่ใช้งานอยู่** เป็น **ไม่ใช่** และ **บริษัท** (บัญชี/ผู้ติดต่อหลัก) ที่ชี้ไปยังบัญชี (ที่ไม่ใช่ผู้ติดต่อ)</span><span class="sxs-lookup"><span data-stu-id="201cf-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="201cf-132">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="201cf-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="201cf-133">มีการเพิ่มฟิลด์ **เป็นลูกค้าที่ใช้งานอยู่** ใหม่ไปยังผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="201cf-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="201cf-134">ฟิลด์นี้จะถูกใช้เพื่อแยกความแตกต่างของผู้ติดต่อที่มีกิจกรรมการขายและผู้ติดต่อที่ไม่มีกิจกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="201cf-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="201cf-135">**เป็นลูกค้าที่ใช้งานอยู่** ถูกตั้งค่าเป็น **ใช่** สำหรับผู้ติดต่อที่มีใบเสนอราคา ใบสั่ง หรือใบแจ้งหนี้ที่เกี่ยวข้องเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="201cf-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="201cf-136">เฉพาะผู้ติดต่อเหล่านั้นที่จะถูกซิงโครไนส์กับ Finance and Operations เป็นลูกค้า</span><span class="sxs-lookup"><span data-stu-id="201cf-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="201cf-137">มีการเพิ่มฟิลด์ **IsCompanyAnAccount** ใหม่ไปยังผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="201cf-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="201cf-138">ฟิลด์นี้จะถูกใช้เพื่อบ่งชี้ว่าผู้ติดต่อเชื่อมโยงกับบริษัท (บัญชี/ผู้ติดต่อหลัก) ของชนิด **บัญชี** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="201cf-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="201cf-139">ข้อมูลนี้จะถูกใช้ในการระบุผู้ติดต่อที่ควรซิงโครไนส์กับ Finance and Operations เป็นผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="201cf-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="201cf-140">มีการเพิ่มฟิลด์ **หมายเลขผู้ติดต่อ** ไปยังผู้ติดต่อเพื่อช่วยรับประกันคีย์ธรรมชาติและคีย์เฉพาะสำหรับการรวม</span><span class="sxs-lookup"><span data-stu-id="201cf-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="201cf-141">เมื่อมีการสร้างผู้ติดต่อใหม่ ค่า **หมายเลขผู้ติดต่อ** จะถูกสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="201cf-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="201cf-142">ค่าประกอบด้วย **CON** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้นแล้วจึงตามด้วยคำต่อท้ายหกอักขระ</span><span class="sxs-lookup"><span data-stu-id="201cf-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="201cf-143">นี่คือตัวอย่าง: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="201cf-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="201cf-144">เมื่อมีการเพิ่มโซลูชันการรวมสำหรับ Sales ไปยัง Sales สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **หมายเลขผู้ติดต่อ** สำหรับผู้ติดต่อที่มีอยู่โดยใช้ลำดับหมายเลขที่มีการกล่าวถึงก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="201cf-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="201cf-145">สคริปต์การอัพเกรดยังตั้งค่าฟิลด์ **เป็นลูกค้าที่ใช้งานอยู่** เป็น **ใช่** สำหรับผู้ติดต่อใด ๆ ที่มีกิจกรรมการขายอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="201cf-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="201cf-146">ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-146">In Finance and Operations</span></span> 

<span data-ttu-id="201cf-147">ผู้ติดต่อจะถูกแท็กโดยใช้คุณสมบัติ **IsContactPersonExternallyMaintained**</span><span class="sxs-lookup"><span data-stu-id="201cf-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="201cf-148">คุณสมบัตินี้บ่งชี้ว่าผู้ติดต่อที่กำหนดถูกรักษาไว้สำหรับภายนอก</span><span class="sxs-lookup"><span data-stu-id="201cf-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="201cf-149">ในกรณีนี้ ผู้ติดต่อจะถูกรักษาไว้สำหรับภายนอกใน Sales</span><span class="sxs-lookup"><span data-stu-id="201cf-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="201cf-150">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="201cf-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="201cf-151">ผู้ติดต่อไปยังผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="201cf-151">Contact to Contact</span></span>

- <span data-ttu-id="201cf-152">อัพเดต **รหัสองค์กร CDS** ในการแม็ป **ต้นทาง &gt; CDS**</span><span class="sxs-lookup"><span data-stu-id="201cf-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="201cf-153">ค่าเท็มเพลตเริ่มต้นสำหรับ **Organization_OrganizationId [รหัสองค์กร]** คือ **ORG001**</span><span class="sxs-lookup"><span data-stu-id="201cf-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="201cf-154">ค่าเท็มเพลตเริ่มต้นสำหรับ **PrimaryAccount_Organization_OrganizationId [รหัสองค์กร]** คือ **ORG001**</span><span class="sxs-lookup"><span data-stu-id="201cf-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="201cf-155">จำเป็นต้องมี **รหัสประเทศ/ภูมิภาคของที่อยู่** ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="201cf-156">เพื่อหลีกเลี่ยงข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ป **CDS &gt; Operations**</span><span class="sxs-lookup"><span data-stu-id="201cf-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="201cf-157">จากนั้นค่าเริ่มต้นจะถูกนำมาใช้ถ้าฟิลด์ถูกปล่อยว่างไว้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="201cf-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="201cf-158">เท็มเพลตเริ่มต้นสำหรับ **PrimaryAddressCountryRegionISOCode** คือ **USA**</span><span class="sxs-lookup"><span data-stu-id="201cf-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="201cf-159">ตรวจสอบให้แน่ใจว่าค่าสำหรับฟิลด์ต่อไปนี้มีอยู่ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="201cf-160">ถ้าไม่จำเป็นต้องใช้ข้อมูลใน Finance and Operations คุณสามารถลบการแม็ปออกจากการแม็ป **CDS &gt; ปลายทาง**</span><span class="sxs-lookup"><span data-stu-id="201cf-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="201cf-161">**ชื่อฟิลด์ใน Finance and Operations:** การตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="201cf-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="201cf-162">**การแม็ป:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="201cf-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="201cf-163">ผู้ติดต่อไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="201cf-163">Contact to Customer</span></span>

- <span data-ttu-id="201cf-164">อัพเดต **รหัสองค์กร CDS** ในการแม็ป **ต้นทาง &gt; CDS**</span><span class="sxs-lookup"><span data-stu-id="201cf-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="201cf-165">ค่าเท็มเพลตเริ่มต้นสำหรับ **Organization_OrganizationId [รหัสองค์กร]** คือ **ORG001**</span><span class="sxs-lookup"><span data-stu-id="201cf-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="201cf-166">จำเป็นต้องมี **รหัสประเทศ/ภูมิภาคของที่อยู่** ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="201cf-167">เพื่อหลีกเลี่ยงข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ป **CDS &gt; ปลายทาง**</span><span class="sxs-lookup"><span data-stu-id="201cf-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="201cf-168">จากนั้นค่าเริ่มต้นจะถูกนำมาใช้ถ้าฟิลด์ถูกปล่อยว่างไว้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="201cf-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="201cf-169">เท็มเพลตเริ่มต้นสำหรับ **PrimaryAddressCountryRegionISOCode** คือ **USA**</span><span class="sxs-lookup"><span data-stu-id="201cf-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="201cf-170">จำเป็นต้องมี **CustomerGroup** ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="201cf-171">เพื่อหลีกเลี่ยงข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นในการแม็ป **CDS &gt; ปลายทาง**</span><span class="sxs-lookup"><span data-stu-id="201cf-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="201cf-172">จากนั้นค่าเริ่มต้นจะถูกนำมาใช้ถ้าฟิลด์ถูกปล่อยว่างไว้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="201cf-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="201cf-173">เท็มเพลตเริ่มต้นสำหรับ **CustomerGroupId** คือ **10**</span><span class="sxs-lookup"><span data-stu-id="201cf-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="201cf-174">โดยการเพิ่มการแม็ปต่อไปนี้จาก **CDS&gt; ปลายทาง** คุณสามารถช่วยลดจำนวนการอัพเดตด้วยตนเองใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="201cf-175">คุณสามารถใช้ค่าเริ่มต้นค่าหรือแผนผังค่าจาก ตัวอย่างเช่น **ประเทศ/ภูมิภาค** หรือ **เมือง** ได้</span><span class="sxs-lookup"><span data-stu-id="201cf-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="201cf-176">**SiteId** - นอกจากนี้คุณยังสามารถกำหนดไซต์เริ่มต้นบนผลิตภัณฑ์ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="201cf-177">จำเป็นต้องมีไซต์เพื่อสร้างใบสั่งขายและใบเสนอราคาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="201cf-178">ไม่ได้กำหนดค่าเท็มเพลตสำหรับ **SiteId** ไว้</span><span class="sxs-lookup"><span data-stu-id="201cf-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="201cf-179">**WarehouseId** - นอกจากนี้คุณยังสามารถกำหนดคลังสินค้าเริ่มต้นบนผลิตภัณฑ์ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="201cf-180">จำเป็นต้องมีคลังสินค้าเพื่อสร้างใบสั่งขายและใบเสนอราคาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="201cf-181">ไม่ได้กำหนดค่าเท็มเพลตสำหรับ **WarehouseId** ไว้</span><span class="sxs-lookup"><span data-stu-id="201cf-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="201cf-182">**LanguageId** – จำเป็นต้องมีภาษาเพื่อสร้างใบเสนอราคาและใบสั่งขายใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="201cf-183">เท็มเพลตเริ่มต้นสำหรับ **LanguageId** คือ **en-us**</span><span class="sxs-lookup"><span data-stu-id="201cf-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="201cf-184">การแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="201cf-184">Template mapping in data integrator</span></span>

<span data-ttu-id="201cf-185">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="201cf-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="201cf-186">ผู้ติดต่อไปยังผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="201cf-186">Contact to Contact</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/contacts-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตสำหรับผู้ติดต่อในตัวรวมข้อมูล](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="201cf-189">ผู้ติดต่อไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="201cf-189">Contact to Customer</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/contacts-template-mapping-data-integrator-3.png)

![การแม็ปเท็มเพลตสำหรับผู้ติดต่อในตัวรวมข้อมูล](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="201cf-192">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="201cf-192">Related topics</span></span>

[<span data-ttu-id="201cf-193">ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="201cf-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="201cf-194">ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="201cf-195">ซิงโครไนส์ส่วนหัวและบรรทัดของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="201cf-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

