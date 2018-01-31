---
title: "นโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับสนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ ซึ่งจะช่วยคุณกำหนดผู้ที่มีสิทธิ์รับสวัสดิการเฉพาะ"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 5c0af3d9446b4f8ae80eeb44494f1ef1e6667e55
ms.contentlocale: th-th
ms.lasthandoff: 01/31/2018

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="bbb24-103">นโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bbb24-103">Benefit eligibility policies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="bbb24-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับสนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ ซึ่งจะช่วยคุณกำหนดผู้ที่มีสิทธิ์รับสวัสดิการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="bbb24-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="bbb24-105">เมื่อคุณสร้างสวัสดิการ คุณตัดสินใจว่าสวัสดิการใดจะพร้อมใช้งานสำหรับพนักงานคนใด</span><span class="sxs-lookup"><span data-stu-id="bbb24-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="bbb24-106">ตารางต่อไปนี้แสดงตัวอย่างของสวัสดิการที่คุณอาจทำให้พนักงานแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="bbb24-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="bbb24-107">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bbb24-107">Benefit</span></span>          | <span data-ttu-id="bbb24-108">ผู้ที่ได้รับสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bbb24-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="bbb24-109">ประกันสุขภาพ</span><span class="sxs-lookup"><span data-stu-id="bbb24-109">Health insurance</span></span> | <span data-ttu-id="bbb24-110">พนักงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bbb24-110">All employees</span></span>                   |
| <span data-ttu-id="bbb24-111">โทรศัพท์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="bbb24-111">Mobile phone</span></span>     | <span data-ttu-id="bbb24-112">พนักงานขาย ผู้บริหารฝ่ายขาย</span><span class="sxs-lookup"><span data-stu-id="bbb24-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="bbb24-113">ด่านจอดรถ</span><span class="sxs-lookup"><span data-stu-id="bbb24-113">Parking passes</span></span>   | <span data-ttu-id="bbb24-114">ผู้บริหาร</span><span class="sxs-lookup"><span data-stu-id="bbb24-114">Executives</span></span>                      |

<span data-ttu-id="bbb24-115">ส่วนประกอบต่อไปนี้จะใช้เพื่อสร้างนโยบายสิทธิ์:</span><span class="sxs-lookup"><span data-stu-id="bbb24-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="bbb24-116">ชนิดกฎนโยบาย</span><span class="sxs-lookup"><span data-stu-id="bbb24-116">Policy rule types</span></span>
-   <span data-ttu-id="bbb24-117">นโยบายเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bbb24-117">Benefit eligibility policies</span></span>

<span data-ttu-id="bbb24-118">ชนิดกฎนโยบายกำหนดพารามิเตอร์การสอบถามที่จะใช้เมื่อคุณพัฒนากฎนโยบายตามที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="bbb24-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="bbb24-119">หลังจากที่คุณสร้างชนิดกฎนโยบาย คุณสามารถสร้างนโยบายต่างๆเกี่ยวกับสิทธิ์ในสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bbb24-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="bbb24-120">นโยบายช่วยให้คุณสามารถสร้างชุดของกฎที่นำไปใช้กับนิติบุคคลอย่าง น้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="bbb24-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="bbb24-121">ภายในแต่ละนโยบาย คุณสามารถดูชนิดกฎนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="bbb24-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="bbb24-122">คุณกำหนดขอบเขตของกฎภายใต้นโยบาย</span><span class="sxs-lookup"><span data-stu-id="bbb24-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="bbb24-123">ตัวอย่างเช่น ถ้าคุณสร้างชนิดกฎนโยบายเกี่ยวกับสิทธิ์ในสวัสดิการที่ชื่อว่า **ผู้บริหาร**คุณสามารถระบุกฎที่อยู่ภายใต้นโยบาย</span><span class="sxs-lookup"><span data-stu-id="bbb24-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="bbb24-124">ในตัวอย่างนี้ กฎอาจระบุว่า ตำแหน่งงานใด ๆ ที่ประกอบด้วยคำ "บริหาร" ควรรวมอยู่ในกฎ</span><span class="sxs-lookup"><span data-stu-id="bbb24-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="bbb24-125">หลังจากที่คุณได้กำหนดพารามิเตอร์ของกฎหรือกฎที่รวมอยู่ในนโยบาย คุณสามารถกำหนดกฎเฉพาะหนึ่ง ๆ ให้กับสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bbb24-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="see-also"></a><span data-ttu-id="bbb24-126">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="bbb24-126">See also</span></span>
--------

[<span data-ttu-id="bbb24-127">การกำหนดและจัดการโปรแกรมสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bbb24-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)




