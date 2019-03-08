---
title: ซิงโครไนส์ใบแจ้งหนี้ข้อตกลงใน Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Finance and Operations
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลใบแจ้งหนี้ข้อตกลงใน Microsoft Dynamics 365 for Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Microsoft Dynamics 365 for Finance and Operations ตรงกัน
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "333265"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="ba6fb-103">ซิงโครไนส์ใบแจ้งหนี้ของข้อตกลงใน Field Service กับใบแจ้งหนี้ข้อความอิสระใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ba6fb-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ba6fb-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลใบแจ้งหนี้ข้อตกลงใน Microsoft Dynamics 365 for Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Microsoft Dynamics 365 for Finance and Operations ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="ba6fb-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ba6fb-105">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="ba6fb-105">Templates and tasks</span></span>

<span data-ttu-id="ba6fb-106">เท็มเพลตต่อไปนี้และงานพื้นฐานถูกใช้ในการรันการซิงโครไนส์ของใบแจ้งหนี้ข้อตกลงจาก Field Service กับใบแจ้งหนี้ข้อความอิสระใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ba6fb-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="ba6fb-107">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="ba6fb-108">ใบแจ้งหนี้ข้อตกลง (Field Service ไปยัง Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="ba6fb-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="ba6fb-109">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="ba6fb-110">ส่วนหัวของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ba6fb-110">Invoice headers</span></span>
- <span data-ttu-id="ba6fb-111">รายการในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ba6fb-111">Invoice lines</span></span>

<span data-ttu-id="ba6fb-112">จำเป็นต้องทำการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ของใบแจ้งหนี้ข้อตกลงจะเกิดขึ้นได้:</span><span class="sxs-lookup"><span data-stu-id="ba6fb-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="ba6fb-113">บัญชี (Sales ไปยัง Fin and Ops) – โดยตรง</span><span class="sxs-lookup"><span data-stu-id="ba6fb-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="ba6fb-114">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="ba6fb-114">Entity set</span></span>

| <span data-ttu-id="ba6fb-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="ba6fb-115">Field Service</span></span>  | <span data-ttu-id="ba6fb-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ba6fb-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="ba6fb-117">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ba6fb-117">invoices</span></span>       | <span data-ttu-id="ba6fb-118">ส่วนหัวใบแจ้งหนี้แบบข้อความอิสระของลูกค้า CDS</span><span class="sxs-lookup"><span data-stu-id="ba6fb-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="ba6fb-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="ba6fb-119">invoicedetails</span></span> | <span data-ttu-id="ba6fb-120">รายการใบแจ้งหนี้แบบข้อความอิสระของลูกค้า CDS</span><span class="sxs-lookup"><span data-stu-id="ba6fb-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="ba6fb-121">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="ba6fb-121">Entity flow</span></span>

<span data-ttu-id="ba6fb-122">ใบแจ้งหนี้ที่ถูกสร้างจากข้อตกลงใน Field Service สามารถทำข้อมูลให้ตรงกันกับ Finance and Operations ผ่านทางโครงการการรวมข้อมูล Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="ba6fb-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="ba6fb-123">การปรับปรุงไปยังใบแจ้งหนี้เหล่านี้จะซิงโครไนส์กับใบแจ้งหนี้ข้อความอิสระใน Finance and Operations ถ้าสถานะการบัญชีของใบแจ้งหนี้ข้อความอิสระเป็น **อยู่ระหว่างดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="ba6fb-124">หลังจากใบแจ้งหนี้ข้อความอิสระถูกลงรายการบัญชีใน Finance and Operations และสถานะการบัญชีถูกอัพเดตเป็น **เสร็จสมบูรณ์** คุณไม่สามารถซิงโครไนส์การอัพเดตจาก Field Service ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="ba6fb-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="ba6fb-125">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="ba6fb-125">Field Service CRM solution</span></span>

<span data-ttu-id="ba6fb-126">ฟิลด์ **มีรายการพร้อมกับจุดเริ่มต้นของข้อตกลง** ได้ถูกเพิ่มไปยังเอนทิตี **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="ba6fb-127">ฟิลด์นี้ช่วยรับประกันว่า เฉพาะใบแจ้งหนี้ที่สร้างขึ้นจากข้อตกลงจะถูกซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="ba6fb-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="ba6fb-128">ค่าเป็น **จริง** ถ้าใบแจ้งหนี้ประกอบด้วยรายการใบแจ้งหนี้อย่างน้อยหนึ่งรายการที่เกิดจากข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="ba6fb-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="ba6fb-129">ฟิลด์ **มีจุดเริ่มต้นของข้อตกลง** ได้ถูกเพิ่มไปยังเอนทิตี **รายการใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="ba6fb-130">ฟิลด์นี้ช่วยรับประกันว่า เฉพาะรายการใบแจ้งหนี้ที่สร้างขึ้นจากข้อตกลงจะถูกซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="ba6fb-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="ba6fb-131">ค่าเป็น **จริง** ถ้ารายการใบแจ้งหนี้เกิดจากข้อตกลงนั้น</span><span class="sxs-lookup"><span data-stu-id="ba6fb-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="ba6fb-132">**วันที่ในใบแจ้งหนี้** เป็นฟิลด์บังคับใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ba6fb-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="ba6fb-133">ดังนั้น ฟิลด์ต้องมีค่าใน Field Service ก่อนที่การซิงโครไนส์จะเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="ba6fb-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="ba6fb-134">เพื่อให้ตรงกับความต้องการนี้ จะมีการเพิ่มตรรกะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ba6fb-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="ba6fb-135">ถ้าฟิลด์ **วันที่ใบแจ้งหนี้** ว่างเปล่าในเอนทิตี **ใบแจ้งหนี้** (นั่นคือ ถ้ามีไม่มีค่า) จะถูกกำหนดเป็นวันที่ปัจจุบัน เมื่อมีการเพิ่มรายการใบแจ้งหนี้ที่เกิดจากข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="ba6fb-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="ba6fb-136">ผู้ใช้สามารถเปลี่ยนฟิลด์ **วันที่ใบแจ้งหนี้** ได้</span><span class="sxs-lookup"><span data-stu-id="ba6fb-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="ba6fb-137">อย่างไรก็ตาม เมื่อผู้ใช้พยายามบันทึกใบแจ้งหนี้ที่เกิดจากข้อตกลง เขาหรือเธอได้รับข้อผิดพลาดในกระบวนการทางธุรกิจ ถ้าฟิลด์ **วันที่ในใบแจ้งหนี้** ว่างเปล่าบนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ba6fb-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="ba6fb-138">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="ba6fb-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="ba6fb-139">ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ba6fb-139">In Finance and Operations</span></span>

<span data-ttu-id="ba6fb-140">ต้องตั้งค่าจุดเริ่มต้นของใบแจ้งหนี้สำหรับการรวม เพื่อแยกแยะใบแจ้งหนี้ข้อความอิสระใน Finance and Operations ที่สร้างขึ้นจากใบแจ้งหนี้ข้อตกลงใน Field Service</span><span class="sxs-lookup"><span data-stu-id="ba6fb-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="ba6fb-141">เมื่อใบแจ้งหนี้มีจุดเริ่มต้นของใบแจ้งหนี้ของชนิด **การรวมใบแจ้งหนี้ข้อตกลง** ฟิลด์ **หมายเลขใบแจ้งหนี้ภายนอก** จะแสดงบนส่วนหัว **ใบแจ้งหนี้การขาย**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="ba6fb-142">นอกจากการปรากฏในส่วนหัวของใบแจ้งหนี้ ข้อมูล **หมายเลขใบแจ้งหนี้ภายนอก** สามารถใช้เพื่อช่วยในการรับประกันว่า ใบแจ้งหนี้ที่สร้างขึ้นจากใบแจ้งหนี้ของข้อตกลงของ Field Service จะถูกกรองออกได้ในระหว่างการซิงโครไนส์ใบแจ้งหนี้จาก Finance and Operations ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="ba6fb-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="ba6fb-143">ไปยัง **บัญชีลูกหนี้** \> **ตั้งค่า** \> **รหัสจุดเริ่มต้นในใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="ba6fb-144">เลือก **สร้าง** เพื่อสร้างจุดเริ่มต้นของใบแจ้งหนี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="ba6fb-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="ba6fb-145">ในฟิลด์ **จุดเริ่มต้นในใบแจ้งหนี้** ป้อนชื่อสำหรับจุดเริ่มต้นของใบแจ้งหนี้ เช่น **FS**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="ba6fb-146">ในฟิลด์ **คำอธิบาย** ป้อนคำอธิบาย เช่น **ใบแจ้งหนี้ของข้อตกลงของ Field Service**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="ba6fb-147">เลือกกล่องกาเครื่องหมาย **การกำหนดชนิดของจุดเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="ba6fb-148">ตั้งค่าฟิลด์ **ชนิดจุดเริ่มต้นในใบแจ้งหนี้** เป็น **การรวมใบแจ้งหนี้ข้อตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="ba6fb-149">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="ba6fb-150">ในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ba6fb-150">In the Data Integration project</span></span>

<span data-ttu-id="ba6fb-151">งาน: **รายการใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="ba6fb-152">ตรวจสอบให้แน่ใจว่า ค่าเริ่มต้นสำหรับฟิลด์  Finance and Operations **ค่าที่แสดงบัญชีหลัก** ถูกอัพเดตเพื่อให้ตรงกับค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ba6fb-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="ba6fb-153">ค่าเท็มเพลตเริ่มต้นคือ **401100**</span><span class="sxs-lookup"><span data-stu-id="ba6fb-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ba6fb-154">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ba6fb-154">Template mapping in Data integration</span></span>

<span data-ttu-id="ba6fb-155">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ba6fb-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a><span data-ttu-id="ba6fb-156">ใบแจ้งหนี้ข้อตกลง (Field Service ไปยัง Fin และ Ops): ส่วนหัวใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ba6fb-156">Agreement invoices (Field Service to Fin and Ops): Invoice headers</span></span>

<span data-ttu-id="ba6fb-157">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="ba6fb-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a><span data-ttu-id="ba6fb-158">ใบแจ้งหนี้ข้อตกลง (Field Service ไปยัง Fin และ Ops): รายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ba6fb-158">Agreement invoices (Field Service to Fin and Ops): Invoice lines</span></span>

<span data-ttu-id="ba6fb-159">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="ba6fb-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
