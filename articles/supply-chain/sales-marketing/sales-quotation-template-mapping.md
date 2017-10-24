---
title: "ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Microsoft Dynamics 365 for Sales (Sales) ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations)"
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 9117b5af3beff7290816586f63091b12e357339c
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="c6631-103">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c6631-104">ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ให้ทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration)</span><span class="sxs-lookup"><span data-stu-id="c6631-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="c6631-105">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Microsoft Dynamics 365 for Sales (Sales) ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="c6631-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="c6631-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="c6631-106">Template and tasks</span></span>

<span data-ttu-id="c6631-107">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="c6631-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="c6631-108">**ชื่อของเท็มเพลต:** ใบเสนอราคาขาย (Sales ไปยัง Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c6631-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="c6631-109">**ชื่อของงานในโครงการ:**</span><span class="sxs-lookup"><span data-stu-id="c6631-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="c6631-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="c6631-110">QuoteHeader</span></span>
    - <span data-ttu-id="c6631-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="c6631-111">QuoteLine</span></span>

<span data-ttu-id="c6631-112">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ก่อน จึงจะสามารถดำเนินการซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายได้:</span><span class="sxs-lookup"><span data-stu-id="c6631-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="c6631-113">ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales)</span><span class="sxs-lookup"><span data-stu-id="c6631-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="c6631-114">บัญชี (Sales ไปยัง Fin and Ops) (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="c6631-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="c6631-115">ผู้ติดต่อไปยังลูกค้า (Sales ไปยัง Fin and Ops) (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="c6631-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="c6631-116">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c6631-116">Entity set</span></span>

| <span data-ttu-id="c6631-117">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="c6631-117">Sales</span></span>        | <span data-ttu-id="c6631-118">CDS</span><span class="sxs-lookup"><span data-stu-id="c6631-118">CDS</span></span>           | <span data-ttu-id="c6631-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="c6631-120">ข้อความอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="c6631-120">Quotes</span></span>       | <span data-ttu-id="c6631-121">ใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="c6631-121">Quotation</span></span>     | <span data-ttu-id="c6631-122">ส่วนหัวของใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="c6631-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="c6631-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="c6631-123">QuoteDetails</span></span> | <span data-ttu-id="c6631-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="c6631-124">QuotationLine</span></span> | <span data-ttu-id="c6631-125">รายการในใบเสนอราคาขาย CDS</span><span class="sxs-lookup"><span data-stu-id="c6631-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="c6631-126">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="c6631-126">Entity flow</span></span>

<span data-ttu-id="c6631-127">ใบเสนอราคาขายจะถูกสร้างขึ้นใน Sales และซิงโครไนส์ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="c6631-128">ใบเสนอราคาขายจาก Sales จะมีการซิงโครไนส์เฉพาะเมื่อเป็นไปตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6631-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="c6631-129">ผลิตภัณฑ์ทั้งหมดในรายการในใบเสนอราคาขายมีการรักษาไว้สำหรับภายนอก</span><span class="sxs-lookup"><span data-stu-id="c6631-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="c6631-130">ใบเสนอราคาขายใช้งานอยู่หรือเปิดใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="c6631-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c6631-131">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="c6631-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="c6631-132">ฟิลด์ **มีเฉพาะผลิตภัณฑ์รักษาไว้สำหรับภายนอกเท่านั้น** ถูกเพิ่มในเอนทิตี้อ้างอิง เพื่อให้สามารถติดตามได้อย่างสม่ำเสมอว่า ใบเสนอราคาขายนั้นประกอบด้วยผลิตภัณฑ์รักษาไว้สำหรับภายนอกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c6631-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="c6631-133">ถ้าใบเสนอราคาขายมีเฉพาะผลิตภัณฑ์รักษาไว้สำหรับภายนอกเท่านั้น ผลิตภัณฑ์จะมีการจัดเก็บอยู่ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="c6631-134">ลักษณะการทำงานนี้ช่วยรับประกันว่า คุณจะไม่พยายามซิงโครไนส์รายการในใบเสนอราคาขายกับผลิตภัณฑ์ที่ไม่รู้จักใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="c6631-135">ผลิตภัณฑ์และรายการทั้งหมดในใบเสนอราคาจะได้รับการการอัพเดตด้วยข้อมูล **มีเฉพาะผลิตภัณฑ์รักษาไว้สำหรับภายนอกเท่านั้น** จากส่วนหัวของใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="c6631-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="c6631-136">ข้อมูลนี้พบได้ในฟิลด์ **ใบเสนอราคามีเฉพาะผลิตภัณฑ์รักษาไว้สำหรับภายนอกเท่านั้น** บนเอนทิตี้บรรทัดใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="c6631-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="c6631-137">ฟิลด์ **ส่วนลด**, **ค่าธรรมเนียม** และ **ภาษี** ถูกควบคุมโดยการตั้งค่าที่ซับซ้อนใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="c6631-138">ในขณะนี้ การตั้งค่านี้ยังไม่สนับสนุนการแม็ปการรวม</span><span class="sxs-lookup"><span data-stu-id="c6631-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="c6631-139">ในการออกแบบปัจจุบัน ฟิลด์ **ราคา**, **ส่วนลด**, **ค่าธรรมเนียม** และ **ภาษี** จะใช้เป็นรายการหลักและจัดการโดย Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="c6631-140">ใน Sales โซลูชันจะกำหนดให้ฟิลด์ต่อไปนี้เป็นแบบอ่านอย่างเดียว เนื่องจากค่าต่าง ๆ จะไม่ซิงโครไนส์กับ Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="c6631-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="c6631-141">**ฟิลด์อ่านอย่างเดียวบนส่วนหัวของใบเสนอราคาขาย:** %ส่วนลด, ส่วนลด, ยอดเงินค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="c6631-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="c6631-142">**ฟิลด์อ่านอย่างเดียวบนรายการในใบเสนอราคาขาย:** ภาษี</span><span class="sxs-lookup"><span data-stu-id="c6631-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c6631-143">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="c6631-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="c6631-144">ก่อนที่จะซิงค์ใบสั่งขาย จำเป็นต้องปรับปรุงระบบด้วยการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6631-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="c6631-145">การตั้งค่าใน Sales</span><span class="sxs-lookup"><span data-stu-id="c6631-145">Setup in Sales</span></span>

- <span data-ttu-id="c6631-146">ไปที่ **การตั้งค่า** &gt; **การจัดการ** &gt; **การตั้งค่าระบบ** &gt; **การขาย** และตรวจสอบให้แน่ใจว่าฟิลด์ **วิธีการคำนวณส่วนลด** กำหนดเป็น **ต่อหน่วย**</span><span class="sxs-lookup"><span data-stu-id="c6631-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="c6631-147">การตั้งค่านี้ช่วยรับประกันว่า ส่วนลดสินค้าในรายการสินค้าจาก Sales จะตรงกับการตั้งค่าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="c6631-148">มิฉะนั้น ส่วนลดจะไม่ถูกต้องใน Finance and Operations เนื่องจาก Finance and Operations จะอ่านส่วนลดเป็นส่วนลดต่อหน่วย แม้ว่าใน Sales จะระบุเป็นส่วนลดต่อรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="c6631-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="c6631-149">ตั้งค่าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="c6631-150">ไปที่ **บัญชีลูกหนี้** &gt; **การตั้งค่า** &gt; **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="c6631-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="c6631-151">บนแท็บ **ลำดับหมายเลข** ให้เลือกลำดับหมายเลขสำหรับใบเสนอราคาขาย จากนั้น คลิก **ดูรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="c6631-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="c6631-152">จากนั้น ใต้ **การตั้งค่าทั่วไป** ให้กำหนดฟิลด์ **ด้วยตนเอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c6631-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="c6631-153">ไปที่ **บัญชีลูกหนี้** &gt; **การตั้งค่า** &gt; **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="c6631-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="c6631-154">จากนั้น บนแท็ **การจัดส่งสินค้า** ให้ตั้งค่าฟิลด์ **การควบคุมวันที่จัดส่ง** เป็น **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="c6631-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="c6631-155">การตั้งค่านี้ช่วยป้องกันไม่ให้การซิงโครไนส์ใบเสนอราคาขายล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="c6631-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="c6631-156">การตั้งค่าในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c6631-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="c6631-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="c6631-157">QuoteHeader</span></span>

- <span data-ttu-id="c6631-158">จำเป็นต้องมีฟิลด์ **วันที่จัดส่งที่ร้องขอ** ใน Finance and Operations ถ้าปล่อยฟิลด์นี้ว่างไว้ การซิงโครไนส์จะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="c6631-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="c6631-159">เพื่อป้องกันปัญหานี้ ถ้าฟิลด์ถูกเว้นว่างเอาไว้ ระบบจะระบุวันที่เริ่มต้นจาก **CDS &gt; แหล่งที่มา**</span><span class="sxs-lookup"><span data-stu-id="c6631-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="c6631-160">ควรอัพเดตวันที่เป็นค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c6631-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="c6631-161">ในปัจจุบัน คุณไม่สามารถป้อนค่า อาทิเช่น **วันนี้** เพื่อแสดงถึงวันที่ของวันนี้ได้</span><span class="sxs-lookup"><span data-stu-id="c6631-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="c6631-162">คุณต้องป้อนวันที่เป็นการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c6631-162">You must enter a specific date.</span></span> <span data-ttu-id="c6631-163">ค่าเท็มเพลตเริ่มต้นสำหรับ **วันที่จัดส่งที่ร้องขอ** คือ **1/1/2020**</span><span class="sxs-lookup"><span data-stu-id="c6631-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="c6631-164">จำเป็นต้องมีฟิลด์ **รหัสประเทศ/ภูมิภาคของที่อยู่** ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="c6631-165">เพื่อช่วยป้องกันข้อผิดพลาดในการซิงโครไนส์ คุณสามารถระบุค่าเริ่มต้นที่จะใช้ถ้าฟิลด์ถูกเว้นว่างเอาไว้ใน Sales</span><span class="sxs-lookup"><span data-stu-id="c6631-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="c6631-166">ค่าเริ่มต้นนี้ยังมีประโยชน์ เนื่องจากคุณไม่จำเป็นต้องป้อนค่าด้วยตนเองในฟิลด์ **ประเทศ/ภูมิภาค** สำหรับที่อยู่ในท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="c6631-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="c6631-167">ไม่มีค่าเท็มเพลตเริ่มต้นสำหรับ **DeliveryAddressCountryRegionISOCode**</span><span class="sxs-lookup"><span data-stu-id="c6631-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="c6631-168">อัพเดตการแม็ปสำหรับ **รหัสองค์กร CDS** ใน **CDS &gt; ต้นทาง** ให้ตรงกับ **องค์กร CDS** ในเอนทิตี้องค์กร:</span><span class="sxs-lookup"><span data-stu-id="c6631-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="c6631-169">เท็มเพลตเริ่มต้นสำหรับ **Organization_OrganizationId** คือ **ORG001**</span><span class="sxs-lookup"><span data-stu-id="c6631-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="c6631-170">เท็มเพลตเริ่มต้นสำหรับ **Account_Organization_OrganizationId** คือ **ORG001**</span><span class="sxs-lookup"><span data-stu-id="c6631-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="c6631-171">เท็มเพลตเริ่มต้นสำหรับ **InvoiceAccount_OrganizationId** คือ **ORG001**</span><span class="sxs-lookup"><span data-stu-id="c6631-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="c6631-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="c6631-172">QuoteLine</span></span>

- <span data-ttu-id="c6631-173">อัพเดตการแม็ปสำหรับ **รหัสองค์กร CDS** ใน **CDS &gt; ต้นทาง** ให้ตรงกับ **องค์กร CDS** ในเอนทิตี้องค์กร:</span><span class="sxs-lookup"><span data-stu-id="c6631-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="c6631-174">เท็มเพลตเริ่มต้นสำหรับ **Organization_OrganizationId** คือ **ORG001**</span><span class="sxs-lookup"><span data-stu-id="c6631-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="c6631-175">ค่าเท็มเพลตเริ่มต้นสำหรับ **Product_Organization_Organization_OrganizationId** คือ **ORG001**</span><span class="sxs-lookup"><span data-stu-id="c6631-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="c6631-176">ค่าเท็มเพลตเริ่มต้นสำหรับ **Quotation_Organization_Organization_OrganizationId** คือ **ORG001**</span><span class="sxs-lookup"><span data-stu-id="c6631-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="c6631-177">จำเป็นต้องมีฟิลด์ **วันที่จัดส่งที่ร้องขอ** ใน Finance and Operations ถ้าปล่อยฟิลด์นี้ว่างไว้ การซิงโครไนส์จะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="c6631-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="c6631-178">เพื่อป้องกันปัญหานี้ ถ้าฟิลด์ถูกเว้นว่างเอาไว้ ระบบจะระบุวันที่เริ่มต้นจาก **CDS &gt; แหล่งที่มา**</span><span class="sxs-lookup"><span data-stu-id="c6631-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="c6631-179">ควรอัพเดตวันที่เป็นค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c6631-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="c6631-180">ในปัจจุบัน คุณไม่สามารถป้อนค่า อาทิเช่น **วันนี้** เพื่อแสดงถึงวันที่ของวันนี้ได้</span><span class="sxs-lookup"><span data-stu-id="c6631-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="c6631-181">คุณต้องป้อนวันที่เป็นการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c6631-181">You must enter a specific date.</span></span> <span data-ttu-id="c6631-182">ค่าเท็มเพลตเริ่มต้นสำหรับ **วันที่จัดส่งที่ร้องขอ** คือ **1/1/2020**</span><span class="sxs-lookup"><span data-stu-id="c6631-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="c6631-183">คุณสามารถเพิ่มการแม็ปต่อไปนี้จาก **ปลายทาง &gt; CDS** เพื่อช่วยรับประกันว่าใบเสนอราคาจะถูกนำเข้าไปที่ Finance and Operations ถ้าไม่มีข้อมูลเริ่มต้นจากลูกค้าหรือผลิตภัณฑ์:</span><span class="sxs-lookup"><span data-stu-id="c6631-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="c6631-184">**SiteId** – จำเป็นต้องมีไซต์เพื่อสร้างบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="c6631-185">ไม่มีค่าเท็มเพลตเริ่มต้นสำหรับ **SiteId**</span><span class="sxs-lookup"><span data-stu-id="c6631-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="c6631-186">**WarehouseId** – จำเป็นต้องมีคลังสินค้าเพื่อดำเนินการกับบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="c6631-187">ไม่มีค่าเท็มเพลตเริ่มต้นสำหรับ **WarehouseId**</span><span class="sxs-lookup"><span data-stu-id="c6631-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="c6631-188">ตรวจสอบให้แน่ใจว่ามีแผนผังค่าที่จำเป็นสำหรับการขายหน่วยวัด (UOM) ใน Finance and Operations อยู่ในการแม็ป **ปลายทาง &gt; CDS** สำหรับ **Quantity_UOM** กับ **SALESUNITSYMBOL**</span><span class="sxs-lookup"><span data-stu-id="c6631-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="c6631-189">การแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c6631-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="c6631-190">ฟิลด์ **ส่วนลด**, **ค่าธรรมเนียม** และ **ภาษี** ถูกควบคุมโดยการตั้งค่าที่ซับซ้อนใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="c6631-191">ในขณะนี้ การตั้งค่านี้ยังไม่สนับสนุนการแม็ปการรวม</span><span class="sxs-lookup"><span data-stu-id="c6631-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="c6631-192">ในการออกแบบปัจจุบัน ฟิลด์ **ราคา**, **ส่วนลด**, **ค่าธรรมเนียม** และ **ภาษี** จะถูกจัดการโดย Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="c6631-193">ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการขนส่ง** และ **วิธีการจัดส่ง** ไม่ได้เป็นส่วนหนึ่งของการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c6631-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="c6631-194">หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง</span><span class="sxs-lookup"><span data-stu-id="c6631-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="c6631-195">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c6631-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="c6631-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="c6631-196">QuoteHeader</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-quotation-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="c6631-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="c6631-199">QuoteLine</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-quotation-template-mapping-data-integrator-3.png)

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="c6631-202">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c6631-202">Related topics</span></span>

[<span data-ttu-id="c6631-203">ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="c6631-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="c6631-204">ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="c6631-205">ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c6631-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



