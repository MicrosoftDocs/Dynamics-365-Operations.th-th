---
title: กรองใบสั่งระหว่างบริษัทเพื่อหลีกเลี่ยงการซิงโครไนส์ใบสั่งและรายการใบสั่ง
description: หัวจ้อนี้อธบายวิธีการกรองใบสั่งระหว่างบริษัทเพื่อหลีกเลี่ยงการซิงโครไนส์ใบสั่งและรายการใบสั่ง
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701044"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="1f91d-103">กรองใบสั่งระหว่างบริษัทเพื่อหลีกเลี่ยงการซิงโครไนส์ใบสั่งและรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="1f91d-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f91d-104">คุณสามารถกรองใบสั่งระหว่างบริษัทเพื่อหลีกเลี่ยงการซิงโครไนส์เอนทิตี **ใบสั่ง** และ **รายการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="1f91d-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="1f91d-105">ในบางสถานการณ์ รายละเอียดของใบสั่งระหว่างบริษัทไม่จำเป็นในแอปการมีส่วนร่วมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="1f91d-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="1f91d-106">แต่ละเอนทิตี Common Data Service มาตรฐานจะถูกขยายโดยมีการอ้างอิงไปยังฟิลด์ **IntercompanyOrder** และแผนผังแบบการรวมแบบสองทิศทางได้รับการแก้ไขเพื่ออ้างอิงถึงฟิลด์เพิ่มเติมในตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1f91d-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="1f91d-107">ผลลัพธ์คือใบสั่งระหว่างบริษัทจะไม่มีการซิงโครไนส์อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="1f91d-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="1f91d-108">กระบวนการนี้จะหลีกเลี่ยงข้อมูลที่ไม่จำเป็นในแอปการมีส่วนร่วมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="1f91d-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="1f91d-109">เพิ่มการอ้างอิงถึง **IntercompanyOrder** ลงใน **หัวข้อของใบสั่งขาย CDS**</span><span class="sxs-lookup"><span data-stu-id="1f91d-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="1f91d-110">มีการเติมข้อมูลในใบสั่งระหว่างบริษัทเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1f91d-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="1f91d-111">ฟิลด์ **IntercompanyOrder** มีอยู่ใน **SalesTable**</span><span class="sxs-lookup"><span data-stu-id="1f91d-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="แม็ปการแบ่งระยะไปยังเป้าหมาย SalesOrderHeader":::
    
2. <span data-ttu-id="1f91d-113">หลังจากที่ **หัวข้อของใบสั่งขายของ CDS** ถูกขยายแล้ว ฟิลด์ **IntercompanyOrder** จะพร้อมใช้งานในการแม็ป</span><span class="sxs-lookup"><span data-stu-id="1f91d-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="1f91d-114">ใช้ตัวกรองข้อมูลกับ `INTERCOMPANYORDER == ""` เป็นสตริงการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="1f91d-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="หัวข้อของใบสั่งขาย แก้ไขการสอบถาม":::

3. <span data-ttu-id="1f91d-116">เพิ่มการอ้างอิงให้ **IntercompanyInventTransId** กับ **บรรทัดใบสั่งขาย CDS**</span><span class="sxs-lookup"><span data-stu-id="1f91d-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="1f91d-117">มีการเติมข้อมูลในใบสั่งระหว่างบริษัทเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1f91d-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="1f91d-118">ฟิลด์ **InterCompanyInventTransID** มีอยู่ใน **SalesLine**</span><span class="sxs-lookup"><span data-stu-id="1f91d-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="แม็ปการแบ่งระยะไปยังเป้าหมาย SalesOrderLine":::

4. <span data-ttu-id="1f91d-120">หลังจากที่ **รายการใบสั่งขายของ CDS** ถูกขยายแล้ว ฟิลด์ **IntercompanyInventTransId** จะพร้อมใช้งานในการแม็ป</span><span class="sxs-lookup"><span data-stu-id="1f91d-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="1f91d-121">ใช้ตัวกรองข้อมูลกับ `INTERCOMPANYINVENTTRANSID == ""` เป็นสตริงการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="1f91d-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="รายการใบสั่งขาย แก้ไขการสอบถาม":::

5. <span data-ttu-id="1f91d-123">ขยาย **หัวข้อของใบแจ้งหนี้การขาย V2** และ **บรรทัดใบแจ้งหนี้การขาย V2** ในลักษณะเดียวกับที่คุณขยายเอนทิตี Common Data Service ในขั้นตอนที่ 1 และ 2</span><span class="sxs-lookup"><span data-stu-id="1f91d-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="1f91d-124">เพิ่มการสอบถามตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="1f91d-124">Then add the filter queries.</span></span> <span data-ttu-id="1f91d-125">สตริงตัวกรองสำหรับ **หัวข้อของใบแจ้งหนี้การขาย V2** คือ `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`</span><span class="sxs-lookup"><span data-stu-id="1f91d-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="1f91d-126">สตริงตัวกรองสำหรับ **รายการใบแจ้งหนี้การขาย V2** คือ `INTERCOMPANYINVENTTRANSID == ""`</span><span class="sxs-lookup"><span data-stu-id="1f91d-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="แม็ปการแบ่งระยะไปยังเป้าหมาย หัวข้อของใบแจ้งหนี้การขาย":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="หัวข้อของใบแจ้งหนี้การขาย แก้ไขการสอบถาม":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="รายการของใบแจ้งหนี้การขาย แก้ไขการสอบถาม":::

6. <span data-ttu-id="1f91d-130">เอนทิตี **ใบเสนอราคา** ไม่มีความสัมพันธ์ระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="1f91d-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="1f91d-131">ถ้ามีบุคคลสร้างใบเสนอราคาสำหรับลูกค้าระหว่างบริษัทอย่างใดอย่างหนึ่ง คุณสามารถกำหนดลูกค้าเหล่านี้ทั้งหมดในกลุ่มลูกค้าหนึ่งกลุ่มโดยใช้ฟิลด์ **CustGroup**</span><span class="sxs-lookup"><span data-stu-id="1f91d-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="1f91d-132">หัวข้อและบรรทัดสามารถขยายเพื่อเพิ่มฟิลด์ **CustGroup** แล้วกรองเพื่อไม่รวมกลุ่มนี้</span><span class="sxs-lookup"><span data-stu-id="1f91d-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="แม็ปการแบ่งระยะไปยังเป้าหมาย หัวข้อของใบเสนอราคาการขาย":::

7. <span data-ttu-id="1f91d-134">หลังจากที่คุณขยายใช้เอนทิตี **ใบเสนอราคา** แล้ว ให้ใช้ตัวกรองข้อมูลกับ `CUSTGROUP !=  "<company>"` เป็นสตริงการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="1f91d-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="หัวข้อของใบเสนอราคาขาย แก้ไขการสอบถาม":::
