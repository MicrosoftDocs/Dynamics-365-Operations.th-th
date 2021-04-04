---
title: การซิงโครไนส์ข้อตกลงของใบแจ้งหนี้ใน Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Supply Chain Management
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการซิงโครไนส์ข้อตกลงตามใบแจ้งหนี้ใน Dynamics 365  Field Service เป็นใบแจ้งหนี้ข้อความอิสระใน Dynamics 365 Supply Chain Management
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 0942ce83060c186212d7f425f8dbd0a4ca2c09e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252785"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="69f91-103">การซิงโครไนส์ข้อตกลงของใบแจ้งหนี้ใน Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="69f91-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="69f91-104">หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลใบแจ้งหนี้ข้อตกลงใน Dynamics 365 Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Dynamics 365 Supply Chain Management ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="69f91-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="69f91-105">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="69f91-105">Templates and tasks</span></span>

<span data-ttu-id="69f91-106">เท็มเพลตต่อไปนี้และงานพื้นฐานจะถูกใช้ในการดำเนินการซิงโครไนส์ข้อตกลงตามใบแจ้งหนี้จาก Field Service เป็นใบแจ้งหนี้ข้อความอิสระใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="69f91-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="69f91-107">**ชื่อของเท็มเพลตในการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="69f91-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="69f91-108">ข้อตกลงตามใบแจ้งหนี้ (Field Service ไปยัง Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="69f91-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="69f91-109">**ชื่อของงานในโครงการการรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="69f91-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="69f91-110">ส่วนหัวของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="69f91-110">Invoice headers</span></span>
- <span data-ttu-id="69f91-111">รายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="69f91-111">Invoice lines</span></span>

<span data-ttu-id="69f91-112">จำเป็นต้องทำการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ของใบแจ้งหนี้ข้อตกลงจะเกิดขึ้นได้:</span><span class="sxs-lookup"><span data-stu-id="69f91-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="69f91-113">รายการ (ยอดขาย ที่ส่งไป Supply Chain Management) - โดยตรง</span><span class="sxs-lookup"><span data-stu-id="69f91-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="69f91-114">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="69f91-114">Entity set</span></span>

| <span data-ttu-id="69f91-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="69f91-115">Field Service</span></span>  | <span data-ttu-id="69f91-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="69f91-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="69f91-117">ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="69f91-117">invoices</span></span>       | <span data-ttu-id="69f91-118">Dataverse ส่วนหัวใบแจ้งหนี้แบบข้อความอิสระของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="69f91-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="69f91-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="69f91-119">invoicedetails</span></span> | <span data-ttu-id="69f91-120">Dataverse รายการใบแจ้งหนี้แบบข้อความอิสระของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="69f91-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="69f91-121">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="69f91-121">Entity flow</span></span>

<span data-ttu-id="69f91-122">ใบแจ้งหนี้ที่ถูกสร้างจากข้อตกลงใน Field Service สามารถซิงโครไนส์ไปยัง Supply Chain Management ผ่านทางโครงการการรวมข้อมูล Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="69f91-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="69f91-123">การอัพเดตใบแจ้งหนี้เหล่านี้จะซิงโครไนส์กับใบแจ้งหนี้ข้อความอิสระใน Supply Chain Management ถ้าสถานะการบัญชีของใบแจ้งหนี้ข้อความอิสระเป็น **อยู่ระหว่างดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="69f91-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="69f91-124">หลังจากใบแจ้งหนี้ข้อความอิสระถูกลงรายการบัญชีใน Supply Chain Management และสถานะการบัญชีถูกอัพเดตเป็น **เสร็จสมบูรณ์** คุณจะไม่สามารถซิงโครไนส์การอัพเดตจาก Field Service ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="69f91-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="69f91-125">โซลูชัน CRM ของ Field Service</span><span class="sxs-lookup"><span data-stu-id="69f91-125">Field Service CRM solution</span></span>

<span data-ttu-id="69f91-126">คอลัมน์ **มีรายการพร้อมกับจุดเริ่มต้นของข้อตกลง** ได้ถูกเพิ่มไปยังตาราง **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="69f91-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="69f91-127">คอลัมน์นี้ช่วยรับประกันว่า เฉพาะใบแจ้งหนี้ที่สร้างขึ้นจากข้อตกลงจะถูกซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="69f91-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="69f91-128">ค่าเป็น **จริง** ถ้าใบแจ้งหนี้ประกอบด้วยรายการใบแจ้งหนี้อย่างน้อยหนึ่งรายการที่เกิดจากข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="69f91-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="69f91-129">คอลัมน์ **มีจุดเริ่มต้นของข้อตกลง** ได้ถูกเพิ่มไปยังตาราง **บรรทัดใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="69f91-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="69f91-130">คอลัมน์นี้ช่วยรับประกันว่า เฉพาะบรรทัดใบแจ้งหนี้ที่สร้างขึ้นจากข้อตกลงจะถูกซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="69f91-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="69f91-131">ค่าเป็น **จริง** ถ้ารายการใบแจ้งหนี้เกิดจากข้อตกลงนั้น</span><span class="sxs-lookup"><span data-stu-id="69f91-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="69f91-132">**วันที่ในใบแจ้งหนี้** เป็นฟิลด์บังคับใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="69f91-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="69f91-133">ดังนั้น คอลัมน์ต้องมีค่าใน Field Service ก่อนที่การซิงโครไนส์จะเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="69f91-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="69f91-134">เพื่อให้ตรงกับความต้องการนี้ จะมีการเพิ่มตรรกะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="69f91-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="69f91-135">ถ้าคอลัมน์ **วันที่ใบแจ้งหนี้** ว่างเปล่าในตาราง **ใบแจ้งหนี้** (นั่นคือ ถ้ามีไม่มีค่า) จะถูกกำหนดเป็นวันที่ปัจจุบัน เมื่อมีการเพิ่มรายการใบแจ้งหนี้ที่เกิดจากข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="69f91-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="69f91-136">ผู้ใช้สามารถเปลี่ยนตาราง **วันที่ใบแจ้งหนี้** ได้</span><span class="sxs-lookup"><span data-stu-id="69f91-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="69f91-137">อย่างไรก็ตาม เมื่อผู้ใช้พยายามบันทึกใบแจ้งหนี้ที่เกิดจากข้อตกลง เขาหรือเธอได้รับข้อผิดพลาดในกระบวนการทางธุรกิจ ถ้าคอลัมน์ **วันที่ในใบแจ้งหนี้** ว่างเปล่าบนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="69f91-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="69f91-138">การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="69f91-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="69f91-139">ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="69f91-139">In Supply Chain Management</span></span>

<span data-ttu-id="69f91-140">ต้องตั้งค่าจุดเริ่มต้นของใบแจ้งหนี้สำหรับการรวม เพื่อแยกแยะใบแจ้งหนี้ข้อความอิสระใน Supply Chain Management ที่สร้างขึ้นจากข้อตกลงตามใบแจ้งหนี้ใน Field Service</span><span class="sxs-lookup"><span data-stu-id="69f91-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="69f91-141">เมื่อใบแจ้งหนี้มีจุดเริ่มต้นของใบแจ้งหนี้ของชนิด **การรวมใบแจ้งหนี้ข้อตกลง** ฟิลด์ **หมายเลขใบแจ้งหนี้ภายนอก** จะแสดงบนส่วนหัว **ใบแจ้งหนี้การขาย**</span><span class="sxs-lookup"><span data-stu-id="69f91-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="69f91-142">นอกจากที่จะปรากฎด้านบนของใบแจ้งหนี้แล้ว ข้อมูล **หมายเลขใบแจ้งหนี้ภายนอก** สามารถใช้ในการรับประกันว่า ใบแจ้งหนี้ที่สร้างขึ้นจากข้อตกลงตามใบแจ้งหนี้ใน Field Service จะถูกคัดกรองออกไปในระหว่างการซิงโครไนส์ใบแจ้งหนี้จาก Supply Chain Management ไปยัง Field Service</span><span class="sxs-lookup"><span data-stu-id="69f91-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="69f91-143">ไปยัง **บัญชีลูกหนี้** \> **ตั้งค่า** \> **รหัสจุดเริ่มต้นในใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="69f91-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="69f91-144">เลือก **สร้าง** เพื่อสร้างจุดเริ่มต้นของใบแจ้งหนี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="69f91-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="69f91-145">ในฟิลด์ **จุดเริ่มต้นในใบแจ้งหนี้** ป้อนชื่อสำหรับจุดเริ่มต้นของใบแจ้งหนี้ เช่น **FS**</span><span class="sxs-lookup"><span data-stu-id="69f91-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="69f91-146">ในฟิลด์ **คำอธิบาย** ป้อนคำอธิบาย เช่น **ใบแจ้งหนี้ของข้อตกลงของ Field Service**</span><span class="sxs-lookup"><span data-stu-id="69f91-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="69f91-147">เลือกกล่องกาเครื่องหมาย **การกำหนดชนิดของจุดเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="69f91-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="69f91-148">ตั้งค่าฟิลด์ **ชนิดจุดเริ่มต้นในใบแจ้งหนี้** เป็น **การรวมใบแจ้งหนี้ข้อตกลง**</span><span class="sxs-lookup"><span data-stu-id="69f91-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="69f91-149">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="69f91-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="69f91-150">ในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="69f91-150">In the Data Integration project</span></span>

<span data-ttu-id="69f91-151">งาน: **รายการใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="69f91-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="69f91-152">ตรวจสอบให้แน่ใจว่า ค่าเริ่มต้นของฟิลด์ Supply Chain Management **ค่าที่แสดงบัญชีหลัก** ถูกอัพเดตให้ตรงกับค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="69f91-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="69f91-153">ค่าเท็มเพลตเริ่มต้นคือ **401100**</span><span class="sxs-lookup"><span data-stu-id="69f91-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="69f91-154">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="69f91-154">Template mapping in Data integration</span></span>

<span data-ttu-id="69f91-155">ภาพประกอบต่อไปนี้แสดงการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="69f91-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="69f91-156">ข้อตกลงตามใบแจ้งหนี้ (Field Service ไปยัง Supply Chain Management): หัวเรื่องใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="69f91-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="69f91-157">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="69f91-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="69f91-158">ข้อตกลงตามใบแจ้งหนี้ (Field Service ไปยัง Supply Chain Management): ลำดับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="69f91-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="69f91-159">[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="69f91-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]