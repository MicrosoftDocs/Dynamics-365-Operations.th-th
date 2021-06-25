---
title: กฎนโยบายการตรวจสอบ
description: คุณสามารถใช้นโยบายการตรวจสอบเพื่อประเมินรายงานค่าใช้จ่าย ใบแจ้งหนี้ของผู้จัดจำหน่าย และใบสั่งซื้อ เพื่อตรวจสอบให้แน่ใจว่าจะสอดคล้องกับกฎนโยบายที่คุณสร้าง  กฎทั้งหมดที่เชื่อมโยงกับนโยบายการตรวจสอบกำลังถูกรันในโหมดชุดงาน ตามกำหนดการที่คุณระบุ   กฎนโยบายแต่ละกฎเป็นอินสแตนซ์ของชนิดกฎนโยบาย  สำหรับแต่ละชนิดกฎนโยบาย กฎนโยบายเดียวเท่านั้นสามารถทำงานได้ในแต่ละครั้ง
author: panolte
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f57c3405e03651798b7e0aaf1fab84d25f33f7cc
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187879"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="a84e8-106">กฎนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a84e8-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a84e8-107">คุณสามารถใช้นโยบายการตรวจสอบเพื่อประเมินรายงานค่าใช้จ่าย ใบแจ้งหนี้ของผู้จัดจำหน่าย และใบสั่งซื้อ เพื่อตรวจสอบให้แน่ใจว่าจะสอดคล้องกับกฎนโยบายที่คุณสร้าง </span><span class="sxs-lookup"><span data-stu-id="a84e8-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="a84e8-108">กฎทั้งหมดที่เชื่อมโยงกับนโยบายการตรวจสอบกำลังถูกรันในโหมดชุดงาน ตามกำหนดการที่คุณระบุ </span><span class="sxs-lookup"><span data-stu-id="a84e8-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="a84e8-109">กฎนโยบายแต่ละกฎเป็นอินสแตนซ์ของชนิดกฎนโยบาย </span><span class="sxs-lookup"><span data-stu-id="a84e8-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="a84e8-110">สำหรับแต่ละชนิดกฎนโยบาย กฎนโยบายเดียวเท่านั้นสามารถทำงานได้ในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="a84e8-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

## <a name="queries-and-query-types"></a><span data-ttu-id="a84e8-111">การสอบถามและชนิดการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="a84e8-111">Queries and query types</span></span>

<span data-ttu-id="a84e8-112">เมื่อคุณสร้างกฎนโยบายการตรวจสอบ คุณเลือกชนิดของกฎนโยบายก่อน </span><span class="sxs-lookup"><span data-stu-id="a84e8-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="a84e8-113">ชนิดกฎนโยบายระบุการสอบถาม Application Object Tree (AOT) เพื่อใช้เป็นจุดเริ่มต้นสำหรับการสร้างกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="a84e8-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="a84e8-114">นอกจากนี้มันยังระบุชนิดของการสอบถามที่จะใช้สำหรับกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="a84e8-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="a84e8-115">แบบสอบถามกำหนดเอกสารต้นทางที่กฎนโยบายประเมินไว้</span><span class="sxs-lookup"><span data-stu-id="a84e8-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="a84e8-116">มันยังระบุในฟิลด์ในเอกสารต้นทางที่ระบุทั้งนิติบุคคลและวันที่ใช้เมื่อเลือกเอกสารถูกเลือกมาตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a84e8-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="a84e8-117">ชนิดการสอบถามจะควบคุมฟิลด์เริ่มต้นในหน้าของการสอบถามและหน้ากฏนโยบาลการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a84e8-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="a84e8-118">ตารางต่อไปนี้จะแสดงชนิดของการสอบถามที่พร้อมใช้งานสำหรับกฎนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a84e8-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a84e8-119">ชนิดการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="a84e8-119">Query type</span></span></th>
<th><span data-ttu-id="a84e8-120">วัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="a84e8-120">Purpose</span></span></th>
<th><span data-ttu-id="a84e8-121">ข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a84e8-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a84e8-122">แบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="a84e8-122">Conditional</span></span></td>
<td><span data-ttu-id="a84e8-123">ประเมินแอททริบิวต์ของเอกสารต้นทางโดยเทียบกับค่าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a84e8-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a84e8-124">รวม</span><span class="sxs-lookup"><span data-stu-id="a84e8-124">Aggregate</span></span></td>
<td><span data-ttu-id="a84e8-125">ประเมินเอกสารต้นทางหรือรายการเอกสารต้นทางหลายรายการเทียบกับกฎนโยบาย โดยการรวมค่าที่เป็นตัวเลข</span><span class="sxs-lookup"><span data-stu-id="a84e8-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a84e8-126">การสุ่มตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a84e8-126">Sampling</span></span></td>
<td><span data-ttu-id="a84e8-127">สุ่มเลือกเปอร์เซ็นต์ที่ระบุของเอกสารต้นทางเพื่อประเมินหาการละเมิดนโยบาย</span><span class="sxs-lookup"><span data-stu-id="a84e8-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="a84e8-128">เมื่อคุณเลือกตัวเลือกนี้ ใช้แบบหน้ากฎนโยบายการตรวจสอบเพื่อระบุเปอร์เซ็นต์ของเอกสารที่จะสุ่มเลือกสำหรับการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a84e8-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a84e8-129">ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="a84e8-129">Duplicate</span></span></td>
<td><span data-ttu-id="a84e8-130">ประเมินเอกสารต้นทางเพื่อกำหนดว่าเอกสารดังกล่าวจะมีรายการที่ซ้ำกันในฟิลด์ที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a84e8-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="a84e8-131">เมื่อคุณเลือกตัวเลือกนี้ ใช้หน้ากฎนโยบายการตรวจสอบเพื่อระบุจำนวนวันที่จะเพิ่มลงในจุดเริ่มต้นของช่วงวันที่เลือกเอกสาร เมื่อมีเอกสารถูกประเมินสำหรับรายการที่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="a84e8-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a84e8-132">ค้นหารายการ</span><span class="sxs-lookup"><span data-stu-id="a84e8-132">List search</span></span></td>
<td><span data-ttu-id="a84e8-133">ประเมินเอกสารต้นทางสำหรับเอนทิตี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="a84e8-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="a84e8-134">เอกสารรากของการสอบถามกำหนดเอกสารที่จะถูกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a84e8-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="a84e8-135">แบบสอบถามต้องเป็นแบบสอบถามรายการที่มีการอ้างอิงไปยังตาราง dirpartytable</span><span class="sxs-lookup"><span data-stu-id="a84e8-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="a84e8-136">ตัวเลือกนี้สามารถใช้ได้เฉพาะกับการสอบถาม AOT ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a84e8-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="a84e8-137"><span class="ui">AuditPolicyExpenseList</span> (พนักงานที่ตรวจสอบรายงานค่าใช้จ่าย)</span><span class="sxs-lookup"><span data-stu-id="a84e8-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="a84e8-138"><span class="ui">AuditPolicyPurchList</span> (ผู้จัดจำหน่ายที่ตรวจสอบใบสั่งซื้อ)</span><span class="sxs-lookup"><span data-stu-id="a84e8-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="a84e8-139"><span class="ui">AuditPolicyVendInvoiceList</span> (ผู้จัดจำหน่ายที่ตรวจสอบใบแจ้งหนี้ของผู้จัดจำหน่าย)</span><span class="sxs-lookup"><span data-stu-id="a84e8-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="a84e8-140">เมื่อคุณเลือกตัวเลือกนี้ ให้ระบุเอนทิตี้ที่ตรวจสอบในหน้ากฏนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a84e8-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a84e8-141">ค้นหาคำสำคัญ</span><span class="sxs-lookup"><span data-stu-id="a84e8-141">Keyword search</span></span></td>
<td><span data-ttu-id="a84e8-142">ประเมินเอกสารต้นทางเพื่อกำหนดว่าเอกสารดังกล่าวจะมีคำเฉพาะหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a84e8-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="a84e8-143">เมื่อคุณเลือกตัวเลือกนี้ ให้ป้อนคำที่ค้นหาในหน้ากฏนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="a84e8-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="a84e8-144">หน้ากฎนโยบายการตรวจสอบยังรวมไปถึงตัวเลือกที่อนุญาตให้คุณระบุตารางและฟิลด์ที่จะประเมินหาคำที่คุณป้อนไว้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="a84e8-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="a84e8-145">พารามิเตอร์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="a84e8-145">Common parameters</span></span>
<span data-ttu-id="a84e8-146">กฎนโยบายทั้งหมดของนโยบายการตรวจสอบเฉพาะจะใช้ข้อมูลพารามิเตอร์ชุดงานเดียวกันและช่วงวันที่ของการเลือกเอกสารเดียวกันร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="a84e8-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="a84e8-147">พารามิเตอร์เหล่านี้จะถูกระบุไว้สำหรับนโยบายในหน้าตัวเลือกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a84e8-147">These parameters are specified for the policy in the Additional options page.</span></span>



## <a name="additional-resources"></a><span data-ttu-id="a84e8-148">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a84e8-148">Additional resources</span></span>

<span data-ttu-id="a84e8-149">[ตรวจสอบการละเมิดนโยบายและกรณี](audit-policy-violations-cases.md)
[กำหนดนโยบายการตรวจสอบสำหรับเอกสารต้นทาง](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="a84e8-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]