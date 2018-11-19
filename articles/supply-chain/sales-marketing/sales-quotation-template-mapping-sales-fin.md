---
title: "ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Sales ไปยัง Finance and Operations"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations"
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: efe943f5c874ed041ce7984272ebc19f57cca6ef
ms.contentlocale: th-th
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="b52a3-103">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b52a3-104">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Microsoft Dynamics 365 for Sales ไปยัง Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="b52a3-105">ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดได้ คุณควรทำความคุ้นเคยกับ [รวมข้อมูลลงใน Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)</span><span class="sxs-lookup"><span data-stu-id="b52a3-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b52a3-106">โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="b52a3-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b52a3-107">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="b52a3-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="b52a3-108">เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล จะเปิดใช้งานโฟลว์ของข้อมูลสำหรับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="b52a3-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="b52a3-109">ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="b52a3-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="b52a3-110">[![โฟลว์ข้อมูลทในผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b52a3-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="b52a3-111">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="b52a3-111">Template and tasks</span></span>

<span data-ttu-id="b52a3-112">เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Sales ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b52a3-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="b52a3-113">**ชื่อของเท็มเพลตในการรวมข้อมูล:** ใบเสนอราคาขาย (Sales ไปยัง Fin and Ops) - ตรง</span><span class="sxs-lookup"><span data-stu-id="b52a3-113">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="b52a3-114">**ชื่อของงานในโครงการการรวมข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="b52a3-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="b52a3-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="b52a3-115">QuoteHeader</span></span>
    - <span data-ttu-id="b52a3-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="b52a3-116">QuoteLine</span></span>

<span data-ttu-id="b52a3-117">จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ก่อน จึงจะสามารถดำเนินการซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายได้:</span><span class="sxs-lookup"><span data-stu-id="b52a3-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="b52a3-118">ผลิตภัณฑ์ (Fin and Ops ไปยัง Sales) - ตรง</span><span class="sxs-lookup"><span data-stu-id="b52a3-118">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="b52a3-119">บัญชี (Sales ไปยัง Fin and Ops) - ตรง (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="b52a3-119">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="b52a3-120">ผู้ติดต่อไปยังลูกค้า (Sales ไปยัง Fin and Ops) - ตรง (ถ้าใช้)</span><span class="sxs-lookup"><span data-stu-id="b52a3-120">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="b52a3-121">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="b52a3-121">Entity set</span></span>

| <span data-ttu-id="b52a3-122">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="b52a3-122">Sales</span></span>        | <span data-ttu-id="b52a3-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-123">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="b52a3-124">ข้อความอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="b52a3-124">Quotes</span></span>       | <span data-ttu-id="b52a3-125">ส่วนหัวของใบเสนอราคาขาย CDS</span><span class="sxs-lookup"><span data-stu-id="b52a3-125">CDS sales quotation header</span></span> |
| <span data-ttu-id="b52a3-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="b52a3-126">QuoteDetails</span></span> | <span data-ttu-id="b52a3-127">รายการในใบเสนอราคาขาย CDS</span><span class="sxs-lookup"><span data-stu-id="b52a3-127">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="b52a3-128">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="b52a3-128">Entity flow</span></span>

<span data-ttu-id="b52a3-129">ใบเสนอราคาขายจะถูกสร้างขึ้นใน Sales และซิงโครไนส์ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-129">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="b52a3-130">ใบเสนอราคาขายจาก Sales จะมีการซิงโครไนส์เฉพาะเมื่อเป็นไปตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b52a3-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="b52a3-131">ผลิตภัณฑ์ใบเสนอราคาทั้งหมดในใบเสนอราคาขายถูกรักษาไว้ภายนอก</span><span class="sxs-lookup"><span data-stu-id="b52a3-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="b52a3-132">หลังจากที่คุณคลิก **เปิดใช้งานใบเสนอราคา** ใบเสนอราคาขายใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b52a3-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b52a3-133">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="b52a3-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b52a3-134">ฟิลด์ **มีเฉพาะผลิตภัณฑ์ที่รักษาไว้ภายนอกเท่านั้น** ถูกเพิ่มในเอนทิตี้ **ใบเสนอราคา** เพื่อให้สามารถติดตามได้อย่างสม่ำเสมอว่า ใบเสนอราคาขายนั้นประกอบด้วยผลิตภัณฑ์ที่รักษาไว้ภายนอกเท่านั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b52a3-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="b52a3-135">ถ้าใบเสนอราคาขายมีเฉพาะผลิตภัณฑ์รักษาไว้สำหรับภายนอกเท่านั้น ผลิตภัณฑ์จะมีการจัดเก็บอยู่ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-135">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="b52a3-136">ลักษณะการทำงานนี้ช่วยรับประกันว่า คุณจะไม่พยายามซิงโครไนส์รายการในใบเสนอราคาขายที่มีผลิตภัณฑ์ที่ไม่รู้จักใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="b52a3-137">ผลิตภัณฑ์และรายการทั้งหมดในใบเสนอราคาจะได้รับการการอัพเดตด้วยข้อมูล **มีเฉพาะผลิตภัณฑ์ที่รักษาไว้ภายนอกเท่านั้น** จากส่วนหัวของใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="b52a3-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="b52a3-138">ข้อมูลนี้พบได้ในฟิลด์ **ใบเสนอราคามีเฉพาะผลิตภัณฑ์ที่รักษาไว้ภายนอกเท่านั้น** บนเอนทิตี้ **QuoteDetails**</span><span class="sxs-lookup"><span data-stu-id="b52a3-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="b52a3-139">ส่วนลดสามารถถูกเพิ่มไปยังผลิตภัณฑ์ในใบเสนอราคา และจะถูกซิงโครไนส์ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-139">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="b52a3-140">ฟิลด์ **ส่วนลด** **ค่าธรรมเนียม** และ **ภาษี** ในส่วนหัวถูกควบคุมโดยการตั้งค่าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="b52a3-141">ในขณะนี้ การตั้งค่านี้ยังไม่สนับสนุนการแม็ปการรวม</span><span class="sxs-lookup"><span data-stu-id="b52a3-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="b52a3-142">ในการออกแบบปัจจุบัน ฟิลด์ **ราคา** **ส่วนลด** **ค่าธรรมเนียม** และ **ภาษี** จะถูกรักษาและจัดการใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="b52a3-143">ใน Sales โซลูชันจะกำหนดให้ฟิลด์ต่อไปนี้เป็นแบบอ่านอย่างเดียว เนื่องจากค่าต่าง ๆ จะไม่ซิงโครไนส์กับ Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b52a3-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="b52a3-144">ฟิลด์แบบอ่านอย่างเดียวในส่วนหัวของใบเสนอราคาขาย: **ส่วนลด %** **ส่วนลด** และ **ยอดเงินค่าขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="b52a3-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="b52a3-145">ฟิลด์แบบอ่านอย่างเดียวในใบเสนอราคาผลิตภัณฑ์: **ภาษี**</span><span class="sxs-lookup"><span data-stu-id="b52a3-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b52a3-146">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="b52a3-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="b52a3-147">ก่อนที่ใบเสนอราคาขายจะถูกซิงโครไนส์ จำเป็นที่คุณจะต้องปรับปรุงการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b52a3-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="b52a3-148">การตั้งค่าใน Sales</span><span class="sxs-lookup"><span data-stu-id="b52a3-148">Setup in Sales</span></span>

- <span data-ttu-id="b52a3-149">ต้องแน่ใจว่ามีการตั้งค่าสิทธิ์สำหรับทีมงานที่ผู้ใช้จากชุดการเชื่อมต่อของคุณใน Sales ถูกกำหนดให้</span><span class="sxs-lookup"><span data-stu-id="b52a3-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="b52a3-150">ถ้าคุณกำลังใช้ข้อมูลสาธิต โดยปกติผู้ใช้จะมีการเข้าถึงของผู้ดูแลระบบ แต่ทีมงานจะไม่มีการเข้าถึงของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="b52a3-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="b52a3-151">ถ้าทีมงานไม่มีการเข้าถึงของผู้ดูแลระบบ เมื่อคุณรันโครงการจากการรวมข้อมูล คุณจะได้รับข้อความแสดงข้อผิดพลาดที่แจ้งว่า หลักทีมงานขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="b52a3-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="b52a3-152">เมื่อต้องการตั้งค่าสิทธิ์สำหรับทีมงาน ไปที่ **การตั้งค่า** &gt; **ความปลอดภัย** &gt; **ทีมงาน** และเลือกทีมที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b52a3-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="b52a3-153">เลือก **จัดการบทบาท** แล้วเลือกบทบาทที่มีสิทธิ์ที่เหมาะสม เช่น **ผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="b52a3-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="b52a3-154">ไปยัง **การตั้งค่า** &gt; **การจัดการ** &gt; **การตั้งค่าระบบ** &gt; **Sales** และต้องมั่นใจว่ามีใช้การตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b52a3-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="b52a3-155">ตัวเลือก **ใช้ระบบคำนวณการให้รางวัล** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="b52a3-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="b52a3-156">ฟิลด์ **วิธีการคำนวณส่วนลด** ถูกกำหนดเป็น **สินค้าในรายการ**</span><span class="sxs-lookup"><span data-stu-id="b52a3-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="b52a3-157">การตั้งค่าในโครงการการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b52a3-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="b52a3-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="b52a3-158">QuoteHeader</span></span>

- <span data-ttu-id="b52a3-159">ต้องแน่ใจว่าการแม็ปที่ต้องการ มีอยู่สำหรับ **Shipto\_country** ไปยัง **DeliveryAddressCountryRegionISOCode**</span><span class="sxs-lookup"><span data-stu-id="b52a3-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="b52a3-160">ในแผนผังค่า คุณสามารถกำหนดค่าเริ่มต้นที่จะใช้ หากค่าถูกปล่อยให้ว่างเปล่าได้</span><span class="sxs-lookup"><span data-stu-id="b52a3-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="b52a3-161">เพียงปล่อยด้านซ้ายให้ว่าง และตั้งค่าด้านขวาเป็นประเทศหรือภูมิภาคที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b52a3-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="b52a3-162">ด้วยวิธีนี้ คุณไม่ต้องพิมพ์ประเทศหรือภูมิภาคสำหรับใบสั่งระดับชาติ</span><span class="sxs-lookup"><span data-stu-id="b52a3-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="b52a3-163">ค่าของเท็มเพลตคือแผนผังค่า ที่ซึ่งมีการแม็ปหลายประเทศหรือภูมิภาค และที่ซึ่งค่าว่างเท่ากับค่าของ **US**</span><span class="sxs-lookup"><span data-stu-id="b52a3-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="b52a3-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="b52a3-164">QuoteLine</span></span>

- <span data-ttu-id="b52a3-165">ตรวจสอบให้แน่ใจว่าแผนผังค่าที่ต้องการ ซึ่งมีอยู่สำหรับ **SalesUnitSymbol** ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-165">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="b52a3-166">ตรวจสอบให้แน่ใจว่า มีการกำหนดหน่วยที่จำเป็นใน Sales</span><span class="sxs-lookup"><span data-stu-id="b52a3-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="b52a3-167">ค่าเท็มเพลตที่มีแผนผังค่าถูกกำหนดสำหรับ **oumid.name** ไปยัง **SalesUnitSymbol**</span><span class="sxs-lookup"><span data-stu-id="b52a3-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="b52a3-168">ไม่จำเป็น: คุณสามารถเพิ่มการแม็ปต่อไปนี้เพื่อช่วยรับรองว่า รายการใบเสนอราคาขายจะถูกนำเข้าไปที่ Finance and Operations ถ้าไม่มีข้อมูลเริ่มต้นจากลูกค้าหรือผลิตภัณฑ์:</span><span class="sxs-lookup"><span data-stu-id="b52a3-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="b52a3-169">**SiteId** – จำเป็นต้องมีไซต์เพื่อสร้างบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="b52a3-170">ไม่มีค่าเท็มเพลตเริ่มต้นสำหรับ **SiteId**</span><span class="sxs-lookup"><span data-stu-id="b52a3-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="b52a3-171">**WarehouseId** – จำเป็นต้องมีคลังสินค้าเพื่อดำเนินการกับบรรทัดใบสั่งขายและใบเสนอราคาใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="b52a3-172">ไม่มีค่าเท็มเพลตเริ่มต้นสำหรับ **WarehouseId**</span><span class="sxs-lookup"><span data-stu-id="b52a3-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="b52a3-173">การแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b52a3-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="b52a3-174">ฟิลด์ **ส่วนลด**, **ค่าธรรมเนียม** และ **ภาษี** ถูกควบคุมโดยการตั้งค่าที่ซับซ้อนใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="b52a3-175">ในขณะนี้ การตั้งค่านี้ยังไม่สนับสนุนการแม็ปการรวม</span><span class="sxs-lookup"><span data-stu-id="b52a3-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="b52a3-176">ในการออกแบบปัจจุบัน ฟิลด์ **ราคา**, **ส่วนลด**, **ค่าธรรมเนียม** และ **ภาษี** จะถูกจัดการโดย Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b52a3-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="b52a3-177">ฟิลด์ **เงื่อนไขการชำระเงิน**, **เงื่อนไขการขนส่ง**, **เงื่อนไขการจัดส่ง**, **วิธีการขนส่ง** และ **วิธีการจัดส่ง** ไม่ได้เป็นส่วนหนึ่งของการแม็ปเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b52a3-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="b52a3-178">หากต้องการแม็ปฟิลด์เหล่านี้ คุณต้องตั้งค่าการแม็ปค่าที่เกี่ยวข้องกับข้อมูลในองค์กรที่เอนทิตี้ซิงโครไนส์ระหว่าง</span><span class="sxs-lookup"><span data-stu-id="b52a3-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="b52a3-179">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b52a3-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="b52a3-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="b52a3-180">QuoteHeader</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="b52a3-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="b52a3-182">QuoteLine</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="b52a3-184">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="b52a3-184">Related topics</span></span>

[<span data-ttu-id="b52a3-185">ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="b52a3-185">Prospect to cash</span></span>](prospect-to-cash.md)


