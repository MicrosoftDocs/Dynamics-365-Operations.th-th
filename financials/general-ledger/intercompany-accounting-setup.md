---
title: "การตั้งค่าการบัญชีระหว่างบริษัท"
description: "หัวข้อนี้อธิบายวิธีการตั้งค่าการบัญชีระหว่างบริษัทเพื่อให้คุณสามารถใช้สมุดรายวันระหว่างบริษัทสำหรับการปันส่วนบัญชีแยกประเภทและสมุดรายวันทางการเงิน เช่น สมุดรายวันประจำวัน สมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่าย และสมุดรายวันการชำระเงิน"
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9c5e73d97f6f52a417cb71dc5bfb57658765aaa1
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---

# <a name="intercompany-accounting-setup"></a><span data-ttu-id="ba394-103">การตั้งค่าการบัญชีระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba394-103">Intercompany accounting setup</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ba394-104">หัวข้อนี้อธิบายวิธีการตั้งค่าการบัญชีระหว่างบริษัทเพื่อให้คุณสามารถใช้สมุดรายวันระหว่างบริษัทสำหรับการปันส่วนบัญชีแยกประเภทและสมุดรายวันทางการเงิน เช่น สมุดรายวันประจำวัน สมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่าย และสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ba394-104">This topic explains how to set up intercompany accounting so that you can use intercompany journals for ledger allocations and financial journals, such as daily journals, vendor invoice journals, and payment journals.</span></span>

<span data-ttu-id="ba394-105">สมุดรายวันระหว่างบริษัทสามารถสร้างในสถานการณ์ต่าง ๆ เช่น สำหรับสมุดรายวันประจำวัน สมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่าย การปันส่วนบัญชีแยกประเภท และการชำระเงินส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="ba394-105">Intercompany journals can be created in various scenarios, such as for daily journals, vendor invoice journals, ledger allocations, and centralized payments.</span></span> <span data-ttu-id="ba394-106">เพื่อเปิดใช้งานสถานการณ์เหล่านี้ คุณต้องตั้งค่าบัญชีระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba394-106">To enable these scenarios, you must set up intercompany accounting.</span></span>

## <a name="define-main-accounts"></a><span data-ttu-id="ba394-107">กำหนดบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="ba394-107">Define main accounts</span></span>
<span data-ttu-id="ba394-108">ก่อนอื่น คุณต้องสร้างบัญชีหลักระหว่างบริษัทเพื่อใช้สำหรับการกำหนดชำระไป และครบกำหนดชำระจากรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="ba394-108">First, you must create the intercompany main accounts to use for the Due to and Due from accounting entries.</span></span> <span data-ttu-id="ba394-109">แนะนำให้ใช้บัญชีหลักเฉพาะสำหรับแต่ละบริษัท เพื่อให้การกระทบยอดและการตัดออกของรายการบัญชีระหว่างบริษัทได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="ba394-109">It's a good idea to use unique main accounts for each company, to simplify the reconciliation and elimination of intercompany accounting entries.</span></span> <span data-ttu-id="ba394-110">ถ้าคุณกำลังใช้คู่ค้าหรือสำเนามิติเพื่อระบุฝ่ายระหว่างบริษัท คุณสามารถกำหนดมิตินี้เป็นมิติคงที่บนบัญชีหลักที่กำหนดไว้ในการลงบัญชีระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba394-110">If you're using a trading partner or counterpart dimension to identify the intercompany party, you can define this dimension as a fixed dimension on the main account that is defined in Intercompany accounting.</span></span> <span data-ttu-id="ba394-111">เมื่อคุณตั้งค่าบัญชีหลัก คุณควรตั้งค่าฟิลด์ **ชนิดบัญชีหลัก** เป็น **งบดุล** ในหน้า **บัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="ba394-111">When you set up the main accounts, you should set the **Main account type** field to **Balance sheet** on the **Main accounts** page.</span></span>

## <a name="define-journal-names"></a><span data-ttu-id="ba394-112">กำหนดชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="ba394-112">Define journal names</span></span>
<span data-ttu-id="ba394-113">ถัดไป คุณต้องกำหนดชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="ba394-113">Next, you must define a journal name.</span></span> <span data-ttu-id="ba394-114">ตั้งค่าฟิลด์ **ชนิดสมุดรายวัน** เป็น **ประจำวัน** บนหน้า **ชื่อสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="ba394-114">Set the **Journal type** field to **Daily** on the **Journal names** page.</span></span> <span data-ttu-id="ba394-115">เป็นความคิดที่ดีที่จะใช้ชื่อสมุดรายวันโดยเฉพาะสำหรับการลงบัญชีระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba394-115">It's a good idea to use a specific journal name for intercompany accounting.</span></span>

## <a name="define-intercompany-accounting-setup"></a><span data-ttu-id="ba394-116">กำหนดการตั้งค่าการบัญชีระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba394-116">Define intercompany accounting setup</span></span>
<span data-ttu-id="ba394-117">ใช้หน้า **การบัญชีระหว่างบริษัท** เพื่อสร้างคู่ของนิติบุคคลที่สามารถดำเนินการด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="ba394-117">The **Intercompany accounting** page is used to create the pairs of legal entities that can transact with each other.</span></span> <span data-ttu-id="ba394-118">การตั้งค่าการบัญชีระหว่างบริษัทจะถูกใช้ร่วมกัน ดังนั้นการตั้งค่าจะมองเห็นได้จากภายในนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ba394-118">The Intercompany accounting setup is shared, so the setup is visible from within all legal entities.</span></span> <span data-ttu-id="ba394-119">เมื่อสร้างนิติบุคคลคู่ใหม่ ให้แน่ใจว่าคุณทราบว่านิติบุคคลใดที่ถูกกำหนดให้เป็นบริษัทต้นกำเนิดเทียบกับบริษัทปลายทาง</span><span class="sxs-lookup"><span data-stu-id="ba394-119">When creating a new legal entity pair, ensure that you are aware of which legal entity is defined as the originating company versus the destination company.</span></span> <span data-ttu-id="ba394-120">เมื่อป้อนธุรกรรมระหว่างบริษัท ธุรกรรมจะกำหนดว่านิติบุคคลใดจะเริ่มหรือสร้างธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ba394-120">When entering intercompany transactions, the transaction determines which legal entity is initiating or originating the transaction.</span></span> <span data-ttu-id="ba394-121">ตัวอย่างเช่น การบัญชีระหว่างบริษัทถูกตั้งค่าสำหรับ USMF (ต้นทาง) และ USSI (ปลายทาง)</span><span class="sxs-lookup"><span data-stu-id="ba394-121">For example, the intercompany accounting is setup for USMF (originating) and USSI (destination).</span></span> <span data-ttu-id="ba394-122">ถ้าผู้ใช้กำลังใช้งานอยู่ใน USSI และป้อนธุรกรรมระหว่างบริษัทกับ USMF ธุรกรรมจะไม่ลงรายการบัญชีเนื่องจากการบัญชีระหว่างบริษัทจะถูกกำหนดเฉพาะสำหรับ USMF ที่เป็นผู้ริเริ่ม</span><span class="sxs-lookup"><span data-stu-id="ba394-122">If a user is active in USSI and enters an intercompany transaction with USMF, the transaction will not post because the intercompany accounting is only defined for USMF being the originator.</span></span> <span data-ttu-id="ba394-123">ถ้าบริษัทใดสามารถริเริ่มธุรกรรม คุณจะต้องสร้างนิติบุคคลคู่ที่สองสำหรับการตั้งค่าต่างตอบแทน</span><span class="sxs-lookup"><span data-stu-id="ba394-123">If either company can originate a transaction, you will need to create a second legal entity pair for the reciprocal setup.</span></span> 

<span data-ttu-id="ba394-124">เลือก **บัญชีเดบิต (ได้รับชำระจาก)** และ **บัญชีเครดิต (ชำระแก่)** สำหรับนิติบุคคลทั้งต้นทางและปลายทาง</span><span class="sxs-lookup"><span data-stu-id="ba394-124">Select the **Debit account (Due from)** and **Credit account (Due to)** for both the originating and destination legal entity.</span></span> <span data-ttu-id="ba394-125">กำหนดว่า **ชื่อสมุดรายวัน** จะถูกใช้เมื่อสร้างธุรกรรมในบริษัทปลายทาง</span><span class="sxs-lookup"><span data-stu-id="ba394-125">Define which **Journal name** will be used when the transaction is created in the destination company.</span></span> <span data-ttu-id="ba394-126">สมุดรายวันสำหรับบริษัทต้นทางเป็นข้อมูลที่คุณทราบอยู่แล้วเนื่องจากถูกเลือกไว้โดยผู้ใช้เมื่อสร้างธุรกรรมระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba394-126">The journal for the originating company is already known because it's selected by the user when creating the intercompany transaction.</span></span> 

<span data-ttu-id="ba394-127">สุดท้าย เลือกนิติบุคคลที่จะได้รับการบัญชีสำหรับยอดเงินสนับสนุน เช่น ส่วนลดเงินสดหรือกำไร/ขาดทุนที่รับรู้จากการชำระเงินส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="ba394-127">Finally, select which legal entity will receive the accounting for supporting amounts, such as cash discount or realized gains/losses for centralized payments.</span></span> 

<span data-ttu-id="ba394-128">คุณสามารถตั้งค่าความสัมพันธ์ต่างตอบแทนได้อย่างง่ายดายบนหน้า **การบัญชีระหว่างบริษัท** โดยใช้ปุ่ม **สร้างความสัมพันธ์ต่างตอบแทน** หลังจากที่มีการสร้างนิติบุคคลคู่แรก</span><span class="sxs-lookup"><span data-stu-id="ba394-128">A reciprocal relationship can easily be set up on the **Intercompany accounting** page by using the **Create reciprocal relationship** button after the first legal entity pair is created.</span></span> <span data-ttu-id="ba394-129">เมื่อมีการสร้างคู่ต่างตอบแทน ข้อมูลสำหรับบริษัทปลายทางจะถูกคัดลอกไปยังบริษัทต้นทางและในทางกลับกัน</span><span class="sxs-lookup"><span data-stu-id="ba394-129">When the reciprocal pair is created, the information for the destination company is copied to the originating company and vice versa.</span></span> <span data-ttu-id="ba394-130">สมุดรายวันที่กำหนดไว้สำหรับบริษัทปลายทางจะยังคงอยู่</span><span class="sxs-lookup"><span data-stu-id="ba394-130">The journal defined for the destination company will remain.</span></span> <span data-ttu-id="ba394-131">องค์กรส่วนใหญ่ใช้แบบแผนการตั้งชื่อแบบเดียวกันสำหรับชื่อสมุดรายวัน เพื่อให้ชื่อสมุดรายวันเป็นชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ba394-131">Most organizations use the same naming convention for their journal names, so that the journal name is the same.</span></span> <span data-ttu-id="ba394-132">ถ้าชื่อสมุดรายวันแตกต่างกัน คำเตือนจะปรากฏขึ้นในฟิลด์เพื่อแจ้งให้คุณทราบว่าสมุดรายวันไม่มีอยู่ และคุณสามารถเลือกสมุดรายวันอื่นได้</span><span class="sxs-lookup"><span data-stu-id="ba394-132">If the journal name is different, a warning will appear on the field to notify you that the journal doesn't exist and a different journal can be selected.</span></span>




