---
title: "ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ในการขาย"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ไปยัง Microsoft Dynamics 365 for Sales"
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
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: th-th
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="ab484-103">ซิงโครไนส์ผลิตภัณฑ์จาก Finance and Operations ไปยังผลิตภัณฑ์ในการขาย</span><span class="sxs-lookup"><span data-stu-id="ab484-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="ab484-104">ก่อนที่คุณจะสามารถใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ให้ทำความคุ้นเคยกับ [การรวมข้อมูล Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration)</span><span class="sxs-lookup"><span data-stu-id="ab484-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="ab484-105">หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์บัญชีจาก Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ไปยัง Microsoft Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="ab484-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="ab484-106">เท็มเพลตและงาน</span><span class="sxs-lookup"><span data-stu-id="ab484-106">Template and task</span></span>

<span data-ttu-id="ab484-107">เท็มเพลตและงานพื้นฐานต่อไปนี้จะใช้ในการซิงโครไนส์ผลิตภัณฑ์จาก Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) ไปยัง Microsoft Dynamics 365 for Sales (Sales)</span><span class="sxs-lookup"><span data-stu-id="ab484-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="ab484-108">ชื่อของเท็มเพลต: ผลิตภัณฑ์ (Fin and Ops ไปยังการขาย)</span><span class="sxs-lookup"><span data-stu-id="ab484-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="ab484-109">ชื่อของงานในโครงการ: ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ab484-109">Name of task in project: Products</span></span>

<span data-ttu-id="ab484-110">ซิงค์งานที่จำเป็นก่อนการซิงค์ผลิตภัณฑ์: ไม่มี</span><span class="sxs-lookup"><span data-stu-id="ab484-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="ab484-111">การตั้งค่าเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="ab484-111">Entity set</span></span>

| <span data-ttu-id="ab484-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="ab484-112">**Finance and Operations**</span></span> | <span data-ttu-id="ab484-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="ab484-113">**CDS**</span></span> | <span data-ttu-id="ab484-114">**ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="ab484-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="ab484-115">ผลิตภัณฑ์ที่นำออกใช้ที่สามารถขายได้</span><span class="sxs-lookup"><span data-stu-id="ab484-115">Sellable released products</span></span> | <span data-ttu-id="ab484-116">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ab484-116">Product</span></span> | <span data-ttu-id="ab484-117">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ab484-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="ab484-118">ขั้นตอนเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="ab484-118">Entity flow</span></span>

<span data-ttu-id="ab484-119">ผลิตภัณฑ์จะถูกจัดการใน Finance and Operations และจะถูกซิงโครไนส์ไปยังการขาย</span><span class="sxs-lookup"><span data-stu-id="ab484-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="ab484-120">เอนทิตี้ข้อมูล **ผลิตภัณฑ์ที่นำออกใช้ที่สามารถขายได้** ใน Finance and Operations จะส่งออกผลิตภัณฑ์ที่ขายได้เท่านั้น ซึ่งหมายความว่า ผลิตภัณฑ์มีข้อมูลที่จำเป็นที่จะใช้ในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="ab484-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="ab484-121">กฎเดียวกันนี้จะใช้เมื่อผลิตภัณฑ์ได้รับการตรวจสอบด้วยฟังก์ชัน **ตรวจสอบ** ในหน้า **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="ab484-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="ab484-122">**หมายเลขผลิตภัณฑ์** จะถูกใช้เป็นคีย์ ซึ่งหมายความว่า ผลิตภัณฑ์ย่อยจะซิงโครไนส์กับ CDS และการขายที่มี **รหัสผลิตภัณฑ์** เฉพาะ ต่อ **ผลิตภัณฑ์ย่อย**</span><span class="sxs-lookup"><span data-stu-id="ab484-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ab484-123">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="ab484-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="ab484-124">ฟิลด์ใหม่ในผลิตภัณฑ์ **รักษาไว้สำหรับภายนอก** จะได้รับการเพิ่มในการขายเพื่อบ่งชี้ว่า ผลิตภัณฑ์ดังกล่าวถูกรักษาไว้จากภายนอก</span><span class="sxs-lookup"><span data-stu-id="ab484-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="ab484-125">โดยค่าเริ่มต้นจะถูกตั้งเป็น **ใช่** ระหว่างการนำเข้าไปยังการขาย</span><span class="sxs-lookup"><span data-stu-id="ab484-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="ab484-126">**รักษาไว้สำหรับภายนอก = ใช่**: ผลิตภัณฑ์เกิดจาก Finance and Operations และไม่สามารถแก้ไขได้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="ab484-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="ab484-127">**รักษาไว้สำหรับภายนอก = ไม่**: ผลิตภัณฑ์ถูกป้อนโดยตรงในการขาย</span><span class="sxs-lookup"><span data-stu-id="ab484-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="ab484-128">**รักษาไว้สำหรับภายนอก = ว่างเปล่า**: ผลิตภัณฑ์มีอยู่ในการขายก่อนที่จะเปิดใช้งานผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="ab484-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="ab484-129">ข้อมูล **รักษาไว้สำหรับภายนอก** จะใช้เพื่อให้มั่นใจว่ามีเฉพาะ **ใบเสนอราคา** และ **ใบสั่งขาย** ที่มี **ผลิตภัณฑ์รักษาไว้สำหรับภายนอก** เท่านั้นที่จะซิงค์กับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab484-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="ab484-130">ระบบจะเพิ่ม **ผลิตภัณฑ์รักษาไว้สำหรับภายนอก** โดยอัตโนมัติใน **รายการราคา** แรกที่ถูกต้องที่มีสกุลเงินเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ab484-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="ab484-131">โปรดทราบว่า รายการจะเรียงลำดับตามตัวอักษรของ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="ab484-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="ab484-132">ระบบจะใช้ราคาขายของผลิตภัณฑ์จาก Finance and Operations เป็นราคาใน **รายการราคา**</span><span class="sxs-lookup"><span data-stu-id="ab484-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="ab484-133">ซึ่งหมายความว่าจำเป็นต้องมี **รายการราคา** ในการขายสำหรับแต่ละ **สกุลเงินการขายผลิตภัณฑ์** ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab484-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="ab484-134">สกุลเงินของผลิตภัณฑ์ที่สามารถขายได้ที่นำออกใช้ จะถูกตั้งค่าเป็นสกุลเงินทางบัญชีในนิติบุคคล ที่ผลิตภัณฑ์ถูกส่งออก</span><span class="sxs-lookup"><span data-stu-id="ab484-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="ab484-135">การซิงค์ผลิตภัณฑ์จะไม่สำเร็จหากไม่มี **รายการราคา** ที่มีสกุลเงินที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="ab484-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="ab484-136">การตั้งค่าเงื่อนไขเบื้องต้นและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="ab484-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="ab484-137">ก่อนที่คุณจะรันการซิงค์แรก คุณต้องเติมข้อมูลใน **ตารางผลิตภัณฑ์เฉพาะ** สำหรับผลิตภัณฑ์ที่มีอยู่ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab484-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="ab484-138">จะไม่มีการซิงค์ผลิตภัณฑ์ที่มีอยู่จนกว่างานนี้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ab484-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="ab484-139">ใน Finance and Operations ให้ใช้ค้นหาเพื่อค้นหา **เติมข้อมูลตารางผลิตภัณฑ์เฉพาะ**</span><span class="sxs-lookup"><span data-stu-id="ab484-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="ab484-140">คลิก **เติมข้อมูลตารางผลิตภัณฑ์เฉพาะ** เพื่อรันงาน</span><span class="sxs-lookup"><span data-stu-id="ab484-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="ab484-141">งานนี้จำเป็นต้องรันเพียงครั้งเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ab484-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="ab484-142">ตรวจสอบให้แน่ใจว่ามี **ValueMap** ที่จำเป็นสำหรับการขาย **หน่วยวัด** (UOM) ใน Finance and Operations อยู่ใน **ต้นทาง -\> CDS ในการแม็ป SalesUnitSymbol / DefaultSellingUnitOfMeasure**</span><span class="sxs-lookup"><span data-stu-id="ab484-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="ab484-143">ตรวจสอบให้แน่ใจว่า **ทศนิยมที่สนับสนุน** สำหรับ UOM ตรงกับความต้องการของคุณใน **CDS -\> ปลายทาง**</span><span class="sxs-lookup"><span data-stu-id="ab484-143">Ensure that **Decimals supported** for UOM match your requirements in **CDS -\> Destination**.</span></span> <span data-ttu-id="ab484-144">ถ้าคุณต้องการให้ค่าที่แตกต่างกันต่อ UOM คุณสามารถทำได้โดยใช้ **ValueMap** จากหน่วย ตัวอย่างเช่น [แต่ละ : 0] & [ปอนด์ : 2]</span><span class="sxs-lookup"><span data-stu-id="ab484-144">If you require different values per UOM, this can be done with **ValueMap** from Unit, for example, [Each : 0] & [Pound : 2].</span></span>

    -   <span data-ttu-id="ab484-145">ค่าเท็มเพลตเริ่มต้นจะถูกกำหนดเป็น 0</span><span class="sxs-lookup"><span data-stu-id="ab484-145">Template value is defaulted to 0.</span></span>

-   <span data-ttu-id="ab484-146">อัพเดต **รหัสองค์กร CDS Organization_OrganizationId** ใน **ต้นทาง -\> CDS**</span><span class="sxs-lookup"><span data-stu-id="ab484-146">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="ab484-147">ค่าเท็มเพลตเริ่มต้นจะถูกกำหนดเป็น ORG001</span><span class="sxs-lookup"><span data-stu-id="ab484-147">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="ab484-148">อัพเดต **ValueMap** สำหรับ **กลุ่มหน่วย** (**defaultuomscheduleid.name**) ใน **CDS -\> ปลายทาง** ให้ตรงกับ **กลุ่มหน่วย** ในการขาย</span><span class="sxs-lookup"><span data-stu-id="ab484-148">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="ab484-149">ค่าเท็มเพลตเริ่มต้นคือ **หน่วยเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="ab484-149">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="ab484-150">ตรวจสอบให้แน่ใจว่า มี UOM ผลิตภัณฑ์ที่ขายทั้งหมดจาก Finance and Operations ในการขายที่มีค่า **รายการเบิกสินค้า CDS**</span><span class="sxs-lookup"><span data-stu-id="ab484-150">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="ab484-151">ตรวจสอบให้แน่ใจว่ามี **รายการราคา** ในการขายสำหรับแต่ละสกุลเงินขายผลิตภัณฑ์ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab484-151">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="ab484-152">สามารถสร้างผลิตภัณฑ์ขึ้นในการขายโดยมีสถานะ **ร่าง** หรือ **ใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="ab484-152">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="ab484-153">ซึ่งจะถูกควบคุมใน **การตั้งค่าระบบ** ภายใต้ **การขาย** ในการขาย</span><span class="sxs-lookup"><span data-stu-id="ab484-153">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="ab484-154">จำเป็นต้องเรียกใช้ผลิตภัณฑ์ที่สร้างขึ้นด้วยสถานะร่าง ก่อนที่จะสามารถเพิ่มผลิตภัณฑ์นี้ใน **ใบเสนอราคา** หรือ **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="ab484-154">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="ab484-155">การแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ab484-155">Template mapping in data integrator</span></span>

<span data-ttu-id="ab484-156">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปเท็มเพลตในตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ab484-156">The following illustrations show an example of a template mapping in data integrator.</span></span>

![การแม็ปเท็มเพลตในตัวรวมข้อมูล](./media/products-template-mapping-data-integrator-1.png)

![การแม็ปเท็มเพลตสำหรับผลิตภัณฑ์ในตัวรวมข้อมูล](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="ab484-159">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ab484-159">Related topics</span></span>

[<span data-ttu-id="ab484-160">ซิงโครไนส์บัญชีจาก Sales ไปยังลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab484-160">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="ab484-161">ซิงโครไนส์ผู้ติดต่อจาก Sales ไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab484-161">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="ab484-162">ซิงโครไนส์ส่วนหัวและบรรทัดของใบเสนอราคาขายจาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab484-162">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)


