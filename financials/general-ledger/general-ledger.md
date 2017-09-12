---
title: "บัญชีแยกประเภททั่วไปและโฮมเพจการรายงานทางการเงิน"
description: "ใช้บัญชีแยกประเภททั่วไปเพื่อกำหนด และจัดการเรกคอร์ดทางการเงินของนิติบุคคล  บัญชีแยกประเภททั่วไปมีการลงทะเบียนของรายการเดบิตและเครดิต รายการเหล่านี้มีการจัดประเภทโดยใช้บัญชีที่อยู่ในผังบัญชี"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: th-th
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="431b8-105">บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="431b8-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="431b8-106">ใช้บัญชีแยกประเภททั่วไปเพื่อกำหนด และจัดการเรกคอร์ดทางการเงินของนิติบุคคล </span><span class="sxs-lookup"><span data-stu-id="431b8-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="431b8-107">บัญชีแยกประเภททั่วไปมีการลงทะเบียนของรายการเดบิตและเครดิต</span><span class="sxs-lookup"><span data-stu-id="431b8-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="431b8-108">รายการเหล่านี้มีการจัดประเภทโดยใช้บัญชีที่อยู่ในผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="431b8-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="431b8-109">คุณสามารถปันส่วนหรือกระจายยอดเงินอย่างน้อยหนึ่งบัญชีหรือชุดบัญชีและมิติตามกฎการปันส่วน </span><span class="sxs-lookup"><span data-stu-id="431b8-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="431b8-110">มีอยู่สองชนิดของการปันส่วน: คงที่ และผันแปร</span><span class="sxs-lookup"><span data-stu-id="431b8-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="431b8-111">นอกจากนี้คุณยังสามารถชำระธุรกรรมระหว่างบัญชีแยกประเภท และการประเมินค่ายอดเงินสกุลเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="431b8-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="431b8-112">เมื่อสิ้นสุดปีบัญชี คุณต้องสร้างธุรกรรมปิดปี และจัดเตรียมบัญชีสำหรับปีบัญชีถัดไป</span><span class="sxs-lookup"><span data-stu-id="431b8-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="431b8-113">คุณสามารถใช้ฟังก์ชันการรวมบัญชีเพื่อรวมผลลัพธ์ทางการเงินสำหรับนิติบุคคลบริษัทในเครือหลายรายเป็นผลลัพธ์สำหรับองค์กรรวมเดียว</span><span class="sxs-lookup"><span data-stu-id="431b8-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="431b8-114">บริษัทในเครืออาจอยู่ภายในฐานข้อมูล Microsoft Dynamics 365 for Finance and Operations เดียวกันหรือในฐานข้อมูลที่แยกต่างจากกันก็ได้</span><span class="sxs-lookup"><span data-stu-id="431b8-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="431b8-115">ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="431b8-115">Sales tax</span></span>
<span data-ttu-id="431b8-116">บริษัททุกแห่งจัดเก็บและชำระภาษีให้กับหน่วยงานจัดเก็บภาษีต่างๆ </span><span class="sxs-lookup"><span data-stu-id="431b8-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="431b8-117">กฎและอัตราแตกต่างกันไปตามประเทศ/ภูมิภาค รัฐ เขต และเมือง</span><span class="sxs-lookup"><span data-stu-id="431b8-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="431b8-118">นอกจากนี้ กฎต้องมีการอัพเดเป็นระยะ ๆ เมื่อหน่วยงานจัดเก็บภาษีเปลี่ยนแปลงข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="431b8-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="431b8-119">รหัสภาษีการขายประกอบด้วยข้อมูลพื้นฐานเกี่ยวกับยอดภาษีที่คุณรวบรวมและชำระแก่หน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="431b8-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="431b8-120">เมื่อคุณตั้งค่ารหัสภาษีขาย คุณจะกำหนดจำนวนเงินหรือเปอร์เซ็นต์ที่ต้องรวบรวมไว้</span><span class="sxs-lookup"><span data-stu-id="431b8-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="431b8-121">คุณยังสามารถกำหนดวิธีการต่าง ๆ ที่จำนวนเงินหรือเปอร์เซ็นต์ดังกล่าวจะใช้กับจำนวนเงินธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="431b8-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="431b8-122">หัวข้อในส่วนนี้แสดงข้อมูลเกี่ยวกับวิธีการตั้งค่ารหัสภาษีขาย สำหรับวิธีการและอัตราที่หน่วยงานจัดเก็บภาษีของคุณกำหนด</span><span class="sxs-lookup"><span data-stu-id="431b8-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







