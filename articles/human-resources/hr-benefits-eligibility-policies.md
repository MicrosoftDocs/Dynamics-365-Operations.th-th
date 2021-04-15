---
title: นโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ
description: บทความนี้แสดงข้อมูลเกี่ยวกับสนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ ซึ่งจะช่วยคุณกำหนดผู้ที่มีสิทธิ์รับสวัสดิการเฉพาะ
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a5046f1d32fb965c7cb3793daf1ba40b9c2a1d10
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805909"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="bc43b-103">นโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bc43b-103">Benefit eligibility policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bc43b-104">บทความนี้แสดงข้อมูลเกี่ยวกับสนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ ซึ่งจะช่วยคุณกำหนดผู้ที่มีสิทธิ์รับสวัสดิการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="bc43b-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="bc43b-105">เมื่อคุณสร้างสวัสดิการ คุณตัดสินใจว่าสวัสดิการใดจะพร้อมใช้งานสำหรับพนักงานคนใด</span><span class="sxs-lookup"><span data-stu-id="bc43b-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="bc43b-106">ตารางต่อไปนี้แสดงตัวอย่างของสวัสดิการที่คุณอาจทำให้พนักงานแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="bc43b-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="bc43b-107">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bc43b-107">Benefit</span></span>          | <span data-ttu-id="bc43b-108">ผู้ที่ได้รับสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bc43b-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="bc43b-109">ประกันสุขภาพ</span><span class="sxs-lookup"><span data-stu-id="bc43b-109">Health insurance</span></span> | <span data-ttu-id="bc43b-110">พนักงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bc43b-110">All employees</span></span>                   |
| <span data-ttu-id="bc43b-111">โทรศัพท์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="bc43b-111">Mobile phone</span></span>     | <span data-ttu-id="bc43b-112">พนักงานขาย ผู้บริหารฝ่ายขาย</span><span class="sxs-lookup"><span data-stu-id="bc43b-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="bc43b-113">ด่านจอดรถ</span><span class="sxs-lookup"><span data-stu-id="bc43b-113">Parking passes</span></span>   | <span data-ttu-id="bc43b-114">ผู้บริหาร</span><span class="sxs-lookup"><span data-stu-id="bc43b-114">Executives</span></span>                      |

<span data-ttu-id="bc43b-115">ส่วนประกอบต่อไปนี้จะใช้เพื่อสร้างนโยบายสิทธิ์:</span><span class="sxs-lookup"><span data-stu-id="bc43b-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="bc43b-116">ชนิดกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="bc43b-116">Policy rule types</span></span>
-   <span data-ttu-id="bc43b-117">นโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bc43b-117">Benefit eligibility policies</span></span>

<span data-ttu-id="bc43b-118">ชนิดกฎนโยบายกำหนดพารามิเตอร์การสอบถามที่จะใช้เมื่อคุณพัฒนากฎนโยบายตามที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="bc43b-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="bc43b-119">หลังจากที่คุณสร้างชนิดกฎนโยบาย คุณสามารถสร้างนโยบายต่างๆเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bc43b-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="bc43b-120">นโยบายช่วยให้คุณสามารถสร้างชุดของกฎที่นำไปใช้กับนิติบุคคลอย่าง น้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="bc43b-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="bc43b-121">ภายในแต่ละนโยบาย คุณสามารถดูชนิดกฎนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="bc43b-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="bc43b-122">คุณกำหนดขอบเขตของกฎภายใต้นโยบาย</span><span class="sxs-lookup"><span data-stu-id="bc43b-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="bc43b-123">ตัวอย่างเช่น ถ้าคุณสร้างชนิดกฎนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการที่ชื่อว่า **ผู้บริหาร** คุณสามารถระบุกฎที่อยู่ภายใต้นโยบาย</span><span class="sxs-lookup"><span data-stu-id="bc43b-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="bc43b-124">ในตัวอย่างนี้ กฎอาจระบุว่าตำแหน่งงานใด ๆ ที่ประกอบด้วยคำ "บริหาร" ควรรวมอยู่ในกฎ</span><span class="sxs-lookup"><span data-stu-id="bc43b-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="bc43b-125">หลังจากที่คุณได้กำหนดพารามิเตอร์ของกฎหรือกฎที่รวมอยู่ในนโยบาย คุณสามารถกำหนดกฎเฉพาะหนึ่ง ๆ ให้กับสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bc43b-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>






[!INCLUDE[footer-include](../includes/footer-banner.md)]