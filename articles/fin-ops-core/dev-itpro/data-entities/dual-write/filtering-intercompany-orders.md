---
title: กรองใบสั่งระหว่างบริษัท เพื่อหลีกเลี่ยงการซิงโครไนส์ใบสั่งและรายการใบสั่ง
description: หัวข้อนี้อธิบายวิธีการกรองใบสั่งระหว่างบริษัท เพื่อให้เอนทิตี้ ใบสั่ง และ รายการใบสั่ง ไม่ได้ซิงค์
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 9a736c8e93dfa7dbcd0739b52e2da987dcefdc0e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568113"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="3f9fe-103">กรองใบสั่งระหว่างบริษัท เพื่อหลีกเลี่ยงการซิงโครไนส์ใบสั่งและรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3f9fe-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f9fe-104">คุณสามารถกรองใบสั่งระหว่างบริษัท เพื่อให้ตาราง **ใบสั่ง** และ **รายการใบสั่ง** ไม่ได้ซิงค์</span><span class="sxs-lookup"><span data-stu-id="3f9fe-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="3f9fe-105">ในบางสถานการณ์ รายละเอียดของใบสั่งระหว่างบริษัทไม่จำเป็น ในแอปการมีส่วนร่วมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3f9fe-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="3f9fe-106">แต่ละตาราง Dataverse มาตรฐานจะถูกขยายโดยมีการอ้างอิงไปยังคอลัมน์ **IntercompanyOrder** และแผนผังแบบการรวมแบบสองทิศทางได้รับการแก้ไข เพื่อให้อ้างอิงถึงฟิลด์เพิ่มเติมในตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3f9fe-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="3f9fe-107">ดังนั้น ใบสั่งระหว่างบริษัทจึงไม่ซิงค์อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="3f9fe-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="3f9fe-108">กระบวนการนี้จะช่วยป้องกันข้อมูลที่ไม่จำเป็นในแอปการมีส่วนร่วมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3f9fe-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="3f9fe-109">ขยายตาราง **ส่วนหัวของใบสั่งขาย CDS** โดยเพิ่มการอ้างอิงลงในคอลัมน์ **IntercompanyOrder**</span><span class="sxs-lookup"><span data-stu-id="3f9fe-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="3f9fe-110">คอลัมน์นี้จะมีการเติมข้อมูลเฉพาะในใบสั่งระหว่างบริษัทเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3f9fe-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="3f9fe-111">คอลัมน์ **IntercompanyOrder** มีอยู่ในตาราง **SalesTable**</span><span class="sxs-lookup"><span data-stu-id="3f9fe-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="แม็ปการจัดเตรียมไปยังหน้าเป้าหมายให้กับส่วนหัวของใบสั่งขาย CDS":::

2. <span data-ttu-id="3f9fe-113">หลังจากที่ **ส่วนหัวข้อของใบสั่งขาย CDS** ถูกขยายแล้ว คอลัมน์ **IntercompanyOrder** จะพร้อมใช้งานในการแม็ป</span><span class="sxs-lookup"><span data-stu-id="3f9fe-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="3f9fe-114">ใช้ตัวกรองที่มี `INTERCOMPANYORDER == ""` เป็นสตริงการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="3f9fe-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="แก้ไขกล่องโต้ตอบการสอบถามเกี่ยวกับส่วนหัวของใบสั่งขาย CDS":::

3. <span data-ttu-id="3f9fe-116">ขยายตาราง **บรรทัดของใบสั่งขาย CDS** โดยเพิ่มการอ้างอิงลงในคอลัมน์ **IntercompanyInventTransId**</span><span class="sxs-lookup"><span data-stu-id="3f9fe-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="3f9fe-117">คอลัมน์นี้จะมีการเติมข้อมูลเฉพาะในใบสั่งระหว่างบริษัทเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3f9fe-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="3f9fe-118">คอลัมน์ **InterCompanyInventTransId** มีอยู่ในตาราง **SalesLine**</span><span class="sxs-lookup"><span data-stu-id="3f9fe-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="แม็ปการจัดเตรียมไปยังหน้าเป้าหมายให้กับบรรทัดของใบสั่งขาย CDS":::

4. <span data-ttu-id="3f9fe-120">หลังจากที่ **รายการใบสั่งขายของ CDS** ถูกขยายแล้ว คอลัมน์ **IntercompanyInventTransId** จะพร้อมใช้งานในการแม็ป</span><span class="sxs-lookup"><span data-stu-id="3f9fe-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="3f9fe-121">ใช้ตัวกรองที่มี `INTERCOMPANYINVENTTRANSID == ""` เป็นสตริงการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="3f9fe-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="แก้ไขกล่องโต้ตอบการสอบถามเกี่ยวกับบรรทัดของใบสั่งขาย CDS":::

5. <span data-ttu-id="3f9fe-123">ทําซ้ําขั้นตอนที่ 1 และ 2 เพื่อขยายตาราง **ส่วนหัวของใบแจ้งหนี้การขาย V2** และเพิ่มการสอบถามตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="3f9fe-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="3f9fe-124">ในกรณีนี้ ให้ใช้ `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` เป็นสตริงการสอบถามของตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="3f9fe-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="แม็ปการจัดเตรียมไปยังหน้าเป้าหมายให้กับส่วนหัวของใบแจ้งหนี้ V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="แก้ไขกล่องโต้ตอบการสอบถามเกี่ยวกับส่วนหัวของใบแจ้งหนี้การขาย V2":::

6. <span data-ttu-id="3f9fe-127">ทําซ้ําขั้นตอนที่ 3 และ 4 เพื่อขยายตาราง **บรรทัดของใบแจ้งหนี้การขาย V2** และเพิ่มการสอบถามตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="3f9fe-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="3f9fe-128">ในกรณีนี้ ให้ใช้ `INTERCOMPANYINVENTTRANSID == ""` เป็นสตริงการสอบถามของตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="3f9fe-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="แก้ไขกล่องโต้ตอบการสอบถามเกี่ยวกับบรรทัดวของใบแจ้งหนี้การขาย V2":::

7. <span data-ttu-id="3f9fe-130">ตาราง **ใบเสนอราคา** ไม่มีความสัมพันธ์ระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="3f9fe-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="3f9fe-131">ถ้ามีบุคคลสร้างใบเสนอราคาสำหรับลูกค้าระหว่างบริษัทอย่างใดอย่างหนึ่ง คุณสามารถใช้คอลัมน์ **CustGroup** เพื่อวางลูกค้าทั้งหมดเหล่านั้นลงในกลุ่มลูกค้าหนึ่งกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="3f9fe-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="3f9fe-132">คุณสามารถขยายส่วนหัวและรายการโดยเพิ่มคอลัมน์ **CustGroup** แล้วกรองข้อมูล เพื่อให้กลุ่มนั้นไม่รวมอยู่ในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="3f9fe-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="แม็ปการจัดเตรียมไปยังหน้าเป้าหมายให้กับส่วนหัวของใบเสนอราคาการขาย CDS":::

8. <span data-ttu-id="3f9fe-134">หลังจากที่ขยาย **ใบเสนอราคา** แล้ว ให้ใช้ตัวกรองที่มี `CUSTGROUP != "<company>"` เป็นสตริงการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="3f9fe-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="แก้ไขกล่องโต้ตอบการสอบถามเกี่ยวกับส่วนหัวของใบเสนอราคาการขาย CDS":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]