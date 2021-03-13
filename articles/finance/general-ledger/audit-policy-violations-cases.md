---
title: กรณีและการละเมิดนโยบายการตรวจสอบ
description: บทความอธิบายถึงวิธีสร้างกรณีการตรวจสอบจากการละเมิดกฎนโยบายการตรวจสอบ นอกจากนี้ยังมีข้อมูลเกี่ยวกับวิธีการต่างๆ ที่นโยบายการตรวจสอบใช้ช่วงวันของการเลือกเอกสารการ
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ddd403bfe82b1a7d3c0c5999f89bde19f1bba5e8
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022116"
---
# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="9bce1-104">กรณีและการละเมิดนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9bce1-104">Audit policy violations and cases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bce1-105">บทความอธิบายถึงวิธีสร้างกรณีการตรวจสอบจากการละเมิดกฎนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9bce1-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="9bce1-106">นอกจากนี้ยังมีข้อมูลเกี่ยวกับวิธีการต่างๆ ที่นโยบายการตรวจสอบใช้ช่วงวันของการเลือกเอกสารการ</span><span class="sxs-lookup"><span data-stu-id="9bce1-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="9bce1-107">วิธีสร้างกรณีการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9bce1-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="9bce1-108">นโยบายการตรวจสอบถูกใช้เพื่อระบุรายงานค่าใช้จ่าย ใบสั่งซื้อ และใบแจ้งหนี้ของผู้จัดจำหน่ายที่ไม่เป็นไปทางกฎทางธุรกิจที่คุณกำหนดและตั้งค่าคอนฟิกไว้เป็นกฎนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9bce1-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="9bce1-109">นโยบายการตรวจสอบถูกรันในโหมดชุดงาน</span><span class="sxs-lookup"><span data-stu-id="9bce1-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="9bce1-110">เมื่อคุณรันนโยบายการตรวจสอบ กฎนโยบายทั้งหมดที่เป็นส่วนหนึ่งของนโยบายถูกรันพร้อมๆกัน</span><span class="sxs-lookup"><span data-stu-id="9bce1-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="9bce1-111">กฎแต่ละกฎนโยบายตรวจสอบชุดของเอกสาร</span><span class="sxs-lookup"><span data-stu-id="9bce1-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="9bce1-112">กฎนโยบายเลือกเอกสารที่อยู่ในช่วงวันของการเลือกเอกสารซึ่งตรงกับเกณฑ์ที่ระบุไว้</span><span class="sxs-lookup"><span data-stu-id="9bce1-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="9bce1-113">ตัวอย่างเช่น กฎนโยบายหนึ่งอาจเลือกรายงานค่าใช้จ่ายที่มีค่าอาหารที่เกิน 50.00</span><span class="sxs-lookup"><span data-stu-id="9bce1-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="9bce1-114">กฎนโยบายอื่นอาจเลือกใบแจ้งหนี้ของผู้จัดจำหน่ายที่ชำระแก่ผู้จัดจำหน่ายที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="9bce1-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="9bce1-115">สำหรับเอกสารแต่ละอย่างที่เลือกไว้ในชุด การละเมิดถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="9bce1-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="9bce1-116">การละเมิดคือเรกคอร์ดที่เป็นเอกสารเฉพาะ เช่น ใบแจ้งหนี้ 12345 ไม่สอดคล้องกับกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="9bce1-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="9bce1-117">เรกคอร์ดการละเมิดการตรวจสอบหลายรายการถูกรวมเข้าด้วยกันและเชื่อมโยงไปยังกรณีการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9bce1-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="9bce1-118">ตามค่าเริ่มต้น กรณีสำหรับแต่ละนโยบายการตรวจสอบจะถูกรวบรวมตามกฎนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9bce1-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="9bce1-119">ถ้าคุณต้องการใช้ คุณสามารถเลือกเงื่อนไขการจัดกลุ่มอื่นโดยการใช้หน้า **เกณฑ์การจัดกลุ่มกรณี** ได้</span><span class="sxs-lookup"><span data-stu-id="9bce1-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="9bce1-120">ตัวอย่างเช่น คุณสามารถจัดกลุ่มหัวข้อค่าใช้จ่ายโดยเรียงตามรหัสโครงการและใบแจ้งหนี้ของผู้จัดจำหน่ายตามบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9bce1-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="9bce1-121">ในกรณีนี้ การละเมิดหัวข้อค่าใช้จ่ายทั้งหมดที่มีรหัสโครงการเดียวกันจะถูกรวบรวมอยู่ในกรณีที่เหมือนกัน และใบแจ้งหนี้ของผู้จัดจำหน่ายทั้งหมดที่มีบัญชีผู้จัดจำหน่ายเดียวกันจะถูกรวบรวมไว้ในกรณีที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="9bce1-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="9bce1-122">สำหรับกฎนโยบายการตรวจสอบตามที่เป็นชนิดการสอบถาม **ทำซ้ำ** การละเมิดไม่ถูกจัดกลุ่มตามกฎนโยบายหรือ ตามเงื่อนไขที่ระบุในหน้า **เกณฑ์การจัดกลุ่มกรณี** นั้น</span><span class="sxs-lookup"><span data-stu-id="9bce1-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="9bce1-123">แทนที่ จะถูกจัดกลุ่มตามเกณฑ์ที่สร้างไว้ในกฎนโยบายการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="9bce1-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="9bce1-124">ตัวอย่างเช่น ถ้ากฎนโยบายประเมินรายงานค่าใช้จ่ายซ้ำกันของจำนวนเดียวกัน รหัสผู้ขาย และวันที่ ค่าใช้จ่ายทั้งหมดที่มีค่าเดียวกันในฟิลด์เหล่านั้นจะเป็นหนึ่งกรณี</span><span class="sxs-lookup"><span data-stu-id="9bce1-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="9bce1-125">ค่าใช้จ่ายใดๆ ที่มีค่าที่แตกต่างกันจะเป็นคนละกรณี</span><span class="sxs-lookup"><span data-stu-id="9bce1-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="9bce1-126">หลังจากกรณีการตรวจสอบถูกสร้างขึ้น กรณีนี้ถูกจัดการโดยการใช้กระบวนการทั่วไปสำหรับการจัดการกรณี</span><span class="sxs-lookup"><span data-stu-id="9bce1-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="9bce1-127">ช่วงวันที่ของการเลือกเอกสาร</span><span class="sxs-lookup"><span data-stu-id="9bce1-127">Document selection date ranges</span></span>
<span data-ttu-id="9bce1-128">เมื่อนโยบายการตรวจสอบถูกรัน แต่ละกฎนโยบายจะเลือกชนิดของเอกสารที่ระบุวันที่อยู่ในช่วงวันที่ของการเลือกเอกสาร</span><span class="sxs-lookup"><span data-stu-id="9bce1-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="9bce1-129">ช่วงวันที่ของการเลือกเอกสารถูกระบุในหน้า **ตัวเลือกเพิ่มเติม** นั้น</span><span class="sxs-lookup"><span data-stu-id="9bce1-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="9bce1-130">เอกสารจำนวนมากมีวันที่มากกว่าหนึ่งรายการที่เชื่อมโยงกัน</span><span class="sxs-lookup"><span data-stu-id="9bce1-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="9bce1-131">ฟิลด์วันที่ที่กฎนโยบายการตรวจสอบใช้ถูกระบุในหน้า **ชนิดกฏนโยบาย** นั้น</span><span class="sxs-lookup"><span data-stu-id="9bce1-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="9bce1-132">ต่อไปนี้คือวิธีการที่นโยบายการตรวจสอบใช้ในช่วงวันที่ของการเลือกเอกสาร:</span><span class="sxs-lookup"><span data-stu-id="9bce1-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="9bce1-133">นโยบายใช้รุ่นของแต่ละกฎนโยบายที่มีผลบังคับใช้ในวันสุดท้ายของช่วงวันที่ของการเลือกเอกสาร</span><span class="sxs-lookup"><span data-stu-id="9bce1-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="9bce1-134">คุณสามารถดูวันที่มีผลบังคับใช้สำหรับแต่ละกฎนโยบายในหน้ารายการ **นโยบายการตรวจสอบ** ได้</span><span class="sxs-lookup"><span data-stu-id="9bce1-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="9bce1-135">นโยบายใช้โหมดองค์กรที่เชื่อมโยงกับนโยบายในวันสุดท้ายของช่วงวันที่ของการเลือกเอกสาร</span><span class="sxs-lookup"><span data-stu-id="9bce1-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="9bce1-136">เฉพาะโหมดองค์กรที่เชื่อมโยงกับนโยบายที่ปรากฏอยู่ในขณะนี้ในหน้ารายการ **นโยบายการตรวจสอบ** นั้น</span><span class="sxs-lookup"><span data-stu-id="9bce1-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="9bce1-137">สำหรับกฎนโยบายที่ขึ้นอยู่กับชนิดการสอบถาม **ค้นหารายการ** นโยบายจะประเมินเอกสารสำหรับเอนทิตี้ที่ตรวจสอบที่มีผลบังคับใช้ในวันสุดท้ายของช่วงวันที่ของการเลือกเอกสาร</span><span class="sxs-lookup"><span data-stu-id="9bce1-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="9bce1-138">สำหรับข้อมูลเพิ่มเติม ดู [กฎนโยบายการตรวจสอบ](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="9bce1-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>



