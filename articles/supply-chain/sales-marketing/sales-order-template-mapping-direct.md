---
title: "ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงจาก Finance and Operations ไปยัง Sales"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ไปยัง Microsoft Dynamics 365 for Sales"
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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: e311b0becbb243cebdc265eccf3059eb46217dee
ms.contentlocale: th-th
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="6e533-103">ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6e533-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ไปยัง Microsoft Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="6e533-105">โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="6e533-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="6e533-106">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="6e533-107">เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล จะเปิดใช้งานขั้นตอนของข้อมูลเกี่ยวกับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="6e533-108">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="6e533-109">[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="6e533-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6e533-110">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="6e533-110">Templates and tasks</span></span>

<span data-ttu-id="6e533-111">เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน เปิด [ศูนย์การจัดการ PowerApps](https://preview.admin.powerapps.com/dataintegration)</span><span class="sxs-lookup"><span data-stu-id="6e533-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="6e533-112">เลือก **โครงการ** จากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="6e533-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="6e533-113">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="6e533-114">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ใบสั่งขาย (Fin and Ops ไปยัง Sales) - ตรง</span><span class="sxs-lookup"><span data-stu-id="6e533-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="6e533-115">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="6e533-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="6e533-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="6e533-116">OrderHeader</span></span>
    - <span data-ttu-id="6e533-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="6e533-117">OrderLine</span></span>

<span data-ttu-id="6e533-118">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ก่อน จึงจะสามารถดำเนินการซิงโครไนส์ของส่วนหัวและรายการของใบแจ้งหนี้การขายได้:</span><span class="sxs-lookup"><span data-stu-id="6e533-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="6e533-119">ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales) - ตรง</span><span class="sxs-lookup"><span data-stu-id="6e533-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="6e533-120">บัญชี (Sales ไปยัง Fin and Ops) - ตรง (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="6e533-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="6e533-121">ผู้ติดต่อไปยังลูกค้า (Sales ไปยัง Fin and Ops) - ตรง (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="6e533-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="6e533-122">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="6e533-122">Entity set</span></span>

| <span data-ttu-id="6e533-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6e533-123">Finance and Operations</span></span>  | <span data-ttu-id="6e533-124">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6e533-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="6e533-125">ส่วนหัวของใบสั่งขาย CDS</span><span class="sxs-lookup"><span data-stu-id="6e533-125">CDS sales order headers</span></span> | <span data-ttu-id="6e533-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="6e533-126">SalesOrders</span></span>       |
| <span data-ttu-id="6e533-127">รายการในใบสั่งขาย CDS</span><span class="sxs-lookup"><span data-stu-id="6e533-127">CDS sales order lines</span></span>   | <span data-ttu-id="6e533-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="6e533-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="6e533-129">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="6e533-129">Entity flow</span></span>

<span data-ttu-id="6e533-130">ใบสั่งขายจะถูกสร้างขึ้นใน Finance and Operations และซิงโครไนส์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="6e533-131">ตัวกรองในเท็มเพลตช่วยให้รับรองว่ามีเฉพาะใบสั่งขายที่เกี่ยวข้องเท่านั้นที่รวมอยู่ในการซิงโครไนส์:</span><span class="sxs-lookup"><span data-stu-id="6e533-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="6e533-132">ในใบสั่งขาย ทั้งลูกค้าที่สั่งซื้อและที่ออกใบแจ้งหนี้ที่มีต้นกำเนิดมาจาก Sales เท่านั้น จะรวมอยู่ในการซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="6e533-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="6e533-133">ใน Finance and Operations ฟิลด์ **OrderingCustomerIsExternallyMaintained** และ **InvoiceCustomerIsExternallyMaintained** ถูกใช้ในการติดตามการซิงโครไนส์ในเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e533-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="6e533-134">ใบสั่งขายใน Finance and Operations ต้องได้รับการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="6e533-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="6e533-135">เฉพาะใบสั่งขายที่ยืนยันแล้วหรือใบสั่งขายที่มีสถานะการประมวลผลสูง เช่น **จัดส่งแล้ว** หรือ **ออกใบแจ้งหนี้แล้ว** จะถูกซิงค์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="6e533-136">หลังจากสร้างหรือปรับเปลี่ยนใบสั่งขาย ชุดงาน **คำนวณยอดขายรวม** ใน Finance and Operations จะต้องถูกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="6e533-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="6e533-137">ใบสั่งขายที่ซึ่งยอดขายรวมถูกคำนวณเท่านั้น จะถูกซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="6e533-138">ในขณะนี้ ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมบนส่วนหัวของใบสั่งขาย ไม่ได้รวมอยู่ในการซิงโครไนส์จาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="6e533-139">Sales ไม่ได้สนับสนุนข้อมูลภาษีที่ระดับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="6e533-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="6e533-140">อย่างไรก็ตาม ภาษีที่เกี่ยวข้องกับค่าธรรมเนียมในระดับรายการจะรวมอยู่ในการซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="6e533-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="6e533-141">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="6e533-142">ฟิลด์ใหม่ได้ถูกเพิ่มลงในเอนทิตี้ **ใบสั่ง** และแสดงขึ้นบนหน้า:</span><span class="sxs-lookup"><span data-stu-id="6e533-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="6e533-143">**ถูกรักษาไว้ภายนอก** – ตั้งค่าตัวเลือกนี้เป็น **ใช่** เมื่อใบสั่งมาจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6e533-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="6e533-144">**สถานะการประมวลผล** – ฟิลด์นี้แสดงสถานะการประมวลผลใบสั่งใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6e533-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="6e533-145">ค่าที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6e533-145">The following values are available:</span></span>

    - <span data-ttu-id="6e533-146">ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6e533-146">Active</span></span>
    - <span data-ttu-id="6e533-147">วันที่ยืนยัน</span><span class="sxs-lookup"><span data-stu-id="6e533-147">Confirmed</span></span>
    - <span data-ttu-id="6e533-148">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="6e533-148">Packing Slip</span></span>
    - <span data-ttu-id="6e533-149">ออกใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="6e533-149">Invoiced</span></span>
    - <span data-ttu-id="6e533-150">เบิกสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="6e533-150">Picked</span></span>
    - <span data-ttu-id="6e533-151">เบิกสินค้าแล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="6e533-151">Partially Picked</span></span>
    - <span data-ttu-id="6e533-152">บรรจุแล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="6e533-152">Partially Packed</span></span>
    - <span data-ttu-id="6e533-153">จัดส่งสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="6e533-153">Shipped</span></span>
    - <span data-ttu-id="6e533-154">จัดส่งแล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="6e533-154">Partially Shipped</span></span>
    - <span data-ttu-id="6e533-155">ออกใบแจ้งหนี้แล้วบางส่วน</span><span class="sxs-lookup"><span data-stu-id="6e533-155">Partially Invoiced</span></span>
    - <span data-ttu-id="6e533-156">ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="6e533-156">Cancelled</span></span>

<span data-ttu-id="6e533-157">การตั้งค่า **มีเฉพาะผลิตภัณฑ์ที่รักษาไว้ภายนอก** ถูกใช้ในสถานการณ์จำลองใบสั่งขายอื่น (ตัวอย่างเช่นการซิงโครไนส์จาก Sales ไปยัง Finance and Operation) เพื่อติดตามว่าใบสั่งขายประกอบด้วยผลิตภัณฑ์รักษาไว้ภายนอกทั้งหมดอย่างต่อเนื่องหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6e533-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="6e533-158">ถ้าใบสั่งขายประกอบด้วยผลิตภัณฑ์ที่รักษาไว้ภายนอกทั้งหมด ผลิตภัณฑ์จะมีการจัดเก็บอยู่ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6e533-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="6e533-159">การตั้งค่านี้ช่วยรับประกันว่า คุณจะไม่พยายามซิงโครไนส์รายการใบสั่งขายที่มีผลิตภัณฑ์ที่ไม่รู้จักใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6e533-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="6e533-160">ปุ่ม **สร้างใบแจ้งหนี้** **ยกเลิกใบสั่ง** **คำนวณใหม่** **เรียกดูผลิตภัณฑ์** และ **ค้นหาที่อยู่** บนหน้า **ใบสั่งขาย** ถูกซ่อนไว้สำหรับใบสั่งที่รักษาไว้ภายนอก เนื่องจากใบแจ้งหนี้จะถูกสร้างขึ้นใน Finance and Operations และซิงค์ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="6e533-161">หน้าใบสั่งจะไม่สามารถถูกแก้ไขได้ เนื่องจากข้อมูลในใบสั่งขายจะถูกซิงโครไนส์จาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6e533-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="6e533-162">สถานะของใบสั่งขายจะยังคง **ใช้งานอยู่** เพื่อช่วยรับประกันว่า การเปลี่ยนแปลงจาก Finance and Operations สามารถดำเนินไปยังใบสั่งขายใน Sales ได้</span><span class="sxs-lookup"><span data-stu-id="6e533-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="6e533-163">เพื่อควบคุมลักษณะการทำงานนี้ ตั้งค่าค่า **Statecode \[สถานะ\]** เริ่มต้น เป็น **ใช้งานอยู่** ในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e533-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="6e533-164">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="6e533-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="6e533-165">ก่อนที่คุณจะซิงโครไนส์ใบสั่งขาย จำเป็นที่คุณต้องปรับปรุงการตั้งค่าต่อไปนี้ในระบบ:</span><span class="sxs-lookup"><span data-stu-id="6e533-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="6e533-166">การตั้งค่าใน Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-166">Setup in Sales</span></span>

- <span data-ttu-id="6e533-167">ต้องแน่ใจว่ามีการตั้งค่าสิทธิ์สำหรับทีมงานที่ผู้ใช้จากชุดการเชื่อมต่อของคุณใน Sales ถูกกำหนดให้</span><span class="sxs-lookup"><span data-stu-id="6e533-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="6e533-168">ถ้าคุณกำลังใช้ข้อมูลสาธิต โดยปกติผู้ใช้จะมีการเข้าถึงของผู้ดูแลระบบ แต่ทีมงานจะไม่มีการเข้าถึงของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="6e533-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="6e533-169">ถ้าทีมงานไม่มีการเข้าถึงของผู้ดูแลระบบด้วย เมื่อคุณรันโครงการจากการรวมข้อมูล คุณจะได้รับข้อความแสดงข้อผิดพลาดที่แจ้งว่า หลักทีมงานขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="6e533-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="6e533-170">ไปที่ **การตั้งค่า** > **ความปลอดภัย** > **ทีมงาน** เลือกทีมที่เกี่ยวข้อง เลือก  **จัดการบทบาท** และเลือกบทบาทที่มีสิทธิ์ที่เหมาะสม เช่น **ผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="6e533-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="6e533-171">ไปยัง **การตั้งค่า** > **การดูแล** > **การตั้งค่าระบบ** > **การขาย** และต้องมั่นใจว่ามีใช้การตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6e533-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="6e533-172">ตัวเลือก **ใช้ระบบคำนวณการให้รางวัล** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6e533-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="6e533-173">ฟิลด์ **วิธีการคำนวณส่วนลด** ถูกกำหนดเป็น **สินค้าในรายการ**</span><span class="sxs-lookup"><span data-stu-id="6e533-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="6e533-174">ตั้งค่าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6e533-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="6e533-175">ไปยัง **การขายและการตลาด** > **งานประจำงวด** > **คำนวณยอดขายรวม** และตั้งค่างานที่จะรันเป็นชุดงาน</span><span class="sxs-lookup"><span data-stu-id="6e533-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="6e533-176">ตั้งค่าตัวเลือก **คำนวณผลรวมสำหรับใบสั่งขาย** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6e533-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="6e533-177">ขั้นตอนนี้สำคัญ เนื่องจากเฉพาะใบสั่งขายที่ซึ่งยอดขายรวมถูกคำนวณ จะถูกซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="6e533-178">ความถี่ของชุดงานควรถูกปรับให้เข้ากับความถี่ของการซิงโครไนส์ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6e533-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="6e533-179">การตั้งค่าในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e533-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="6e533-180">งาน SalesHeader</span><span class="sxs-lookup"><span data-stu-id="6e533-180">SalesHeader task</span></span>

- <span data-ttu-id="6e533-181">ต้องแน่ใจว่าการแม็ปที่จำเป็นที่ต้องการมีอยู่สำหรับ **InvoiceCountryRegionId** ไปยัง **BillingAddress\_Country** และสำหรับ **DeliveryCountryRegionId** ไปยัง **DeliveryAddress\_Country**</span><span class="sxs-lookup"><span data-stu-id="6e533-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="6e533-182">ค่าของเท็มเพลตคือ แผนผังค่าที่แม็ปหลายประเทศหรือภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="6e533-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="6e533-183">จำเป็นต้องใช้รายการราคาเพื่อสร้างใบสั่งใน Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="6e533-184">อัพเดตแผนผังค่าสำหรับ **pricelevelid.name \[ชื่อรายการราคา\]** ไปยังรายการราคาที่ใช้ใน Sales สำหรับแต่ละสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="6e533-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="6e533-185">คุณสามารถใช้รายการราคาเริ่มต้นสำหรับสกุลเงินเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6e533-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="6e533-186">อีกทางหนึ่งคือ ถ้าคุณมีรายการราคาในหลายสกุลเงิน คุณสามารถใช้แผนผังค่าได้</span><span class="sxs-lookup"><span data-stu-id="6e533-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="6e533-187">ค่าเท็มเพลตเริ่มต้นสำหรับ **pricelevelid.name \[ชื่อรายการราคา\]** คือ **CRM Service USA (ตัวอย่าง)**</span><span class="sxs-lookup"><span data-stu-id="6e533-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="6e533-188">งาน SalesLine</span><span class="sxs-lookup"><span data-stu-id="6e533-188">SalesLine task</span></span>

- <span data-ttu-id="6e533-189">ต้องแน่ใจว่าการแม็ปที่จำเป็นต้องมีอยู่สำหรับ **DeliveryCountryRegionId** ไปยัง **DeliveryAddress\_Country**</span><span class="sxs-lookup"><span data-stu-id="6e533-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="6e533-190">ค่าของเท็มเพลตคือ แผนผังค่าที่แม็ปหลายประเทศหรือภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="6e533-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="6e533-191">ตรวจสอบให้แน่ใจว่าแผนผังค่าที่ต้องการสำหรับ **SalesUnitSymbol** ใน Finance and Operations มีอยู่</span><span class="sxs-lookup"><span data-stu-id="6e533-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="6e533-192">ค่าเท็มเพลตที่มีแผนผังค่าถูกกำหนดสำหรับ **SalesUnitSymbol** ไปยัง **Quantity\_UOM**</span><span class="sxs-lookup"><span data-stu-id="6e533-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6e533-193">การแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e533-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="6e533-194">ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการจัดส่ง** และ **วิธีการจัดส่ง** ไม่ได้รวมอยู่ในการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6e533-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="6e533-195">หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง</span><span class="sxs-lookup"><span data-stu-id="6e533-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="6e533-196">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e533-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="6e533-197">การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6e533-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="6e533-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="6e533-198">OrderHeader</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="6e533-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="6e533-200">OrderLine</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="6e533-202">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6e533-202">Related topics</span></span>

[<span data-ttu-id="6e533-203">ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="6e533-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="6e533-204">ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6e533-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="6e533-205">ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="6e533-206">ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6e533-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="6e533-207">ซิงโครไนส์ส่วนหัวและรายการของใบแจ้งหนี้การขายโดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="6e533-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




