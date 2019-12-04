---
title: การรวมบัญชีทางการเงินออนไลน์
description: หัวข้อนี้อธิบายการรวมบัญชีทางการเงินออนไลน์ในบัญชีแยกประเภททั่วไป
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 86be6d4cc0af3f2fd92523d4ecd3825f2383fc48
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770746"
---
# <a name="online-financial-consolidations"></a><span data-ttu-id="b9931-103">การรวมบัญชีทางการเงินออนไลน์</span><span class="sxs-lookup"><span data-stu-id="b9931-103">Online financial consolidations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9931-104">หัวข้อนี้อธิบายการรวมบัญชีทางการเงินออนไลน์ในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="b9931-104">This topic describes online financial consolidations in General ledger.</span></span> <span data-ttu-id="b9931-105">ก่อนที่คุณจะอ่านหัวข้อนี้ ให้แน่ใจว่าคุณได้อ่านหัวข้อ [ภาพรวมการรวมบัญชีทางการเงินและการแปลงสกุลเงิน](financial-consolidations-currency-translation.md)</span><span class="sxs-lookup"><span data-stu-id="b9931-105">Before you read this topic, be sure to read the [Financial consolidations and currency translation overview](financial-consolidations-currency-translation.md) topic.</span></span>

<span data-ttu-id="b9931-106">หลังจากที่คุณเสร็จสิ้นการตั้งค่าของคุณ คุณป้อนรายละเอียดของการรวมบัญชีในหน้า **รวมบัญชี [ออนไลน์]**</span><span class="sxs-lookup"><span data-stu-id="b9931-106">After you've completed your setup, you enter the details of the consolidation on the **Consolidate [Online]** page.</span></span> <span data-ttu-id="b9931-107">เมื่อคุณเสร็จสิ้น คุณสามารถคลิก **ตกลง** หรือ **ชุดงาน** เพื่อประมวลผลการรวมบัญชีได้</span><span class="sxs-lookup"><span data-stu-id="b9931-107">When you've finished, you can click **OK** or **Batch** to process the consolidation.</span></span>

## <a name="criteria"></a><span data-ttu-id="b9931-108">เกณฑ์</span><span class="sxs-lookup"><span data-stu-id="b9931-108">Criteria</span></span>
<span data-ttu-id="b9931-109">ในแท็บ **เกณฑ์** ของหน้า **รวมบัญชี [ออนไลน์]** คุณกำหนดบัญชี รอบระยะเวลา และชนิดของข้อมูลที่ถูกรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-109">On the **Criteria** tab of the **Consolidate [Online]** page, you define the accounts, the periods, and the type of data that is being consolidated.</span></span>

<span data-ttu-id="b9931-110">![แท็บเกณฑ์](./media/criteria-consolidate-online.png "แท็บเกณฑ์")</span><span class="sxs-lookup"><span data-stu-id="b9931-110">![Criteria tab](./media/criteria-consolidate-online.png "Criteria tab")</span></span>

<span data-ttu-id="b9931-111">นี่เป็นคำอธิบายเกี่ยวกับฟิลด์ต่างๆ ในแท็บนี้:</span><span class="sxs-lookup"><span data-stu-id="b9931-111">Here is an explanation of the various fields on this tab:</span></span>

- <span data-ttu-id="b9931-112">**คำอธิบาย** – ป้อนคำอธิบายที่ชัดเจนสำหรับรอบระยะเวลาที่คุณจะรวมไว้</span><span class="sxs-lookup"><span data-stu-id="b9931-112">**Description** – Enter a precise description for the period that you're consolidating.</span></span>
- <span data-ttu-id="b9931-113">**บัญชีหลัก** – ใช้ฟิลด์ในส่วนนี้เพื่อกำหนดบัญชีหลักที่จะถูกประมวลผล</span><span class="sxs-lookup"><span data-stu-id="b9931-113">**Main account** – Use the fields in this section to define the main accounts that will be processed.</span></span>

    - <span data-ttu-id="b9931-114">**ตั้งแต่** และ **ถึง** – ระบุช่วงของบัญชีที่จะประมวลผล</span><span class="sxs-lookup"><span data-stu-id="b9931-114">**From** and **To** – Specify a range of accounts to process.</span></span> <span data-ttu-id="b9931-115">ถ้าคุณปล่อยให้ฟิลด์เหล่านี้ว่าง บัญชีทั้งหมดจากบริษัททั้งหมดจะถูกย้ายไปยังบริษัทสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-115">If you leave these fields blank, all accounts from all companies will be moved to the consolidation company.</span></span> <span data-ttu-id="b9931-116">ดังนั้น ถ้าคุณจะรวมข้อมูลบริษัทสี่บริษัท และแต่ละบริษัทมีผังบัญชีที่แตกต่างกัน บัญชีทั้งหมดจากบริษัททั้งสี่บริษัทจะถูกสร้างในบริษัทสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-116">Therefore, if you're consolidating four companies, and each company has a different chart of accounts, all accounts from all four companies will be created in the consolidation company.</span></span>
    - <span data-ttu-id="b9931-117">**ใช้บัญชีหลักในการรวมบัญชี** – ถ้าคุณตั้งค่าตัวเลือกนี้เป็น**ใช่** ฟิลด์ **เลือกบัญชีหลักในการรวมบัญชีจาก** จะกลายเป็นพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b9931-117">**Use consolidation account** – If you set this option to **Yes**, the **Select consolidation account from** field becomes available.</span></span> <span data-ttu-id="b9931-118">ในฟิลด์นี้ ให้เลือกว่าควรมีการรวมบัญชีทั้งหมดไปยังบัญชีหลักในการรวมบัญชีที่ถูกตั้งค่าในหน้า **บัญชีหลัก** หรือว่าคุณต้องการเลือกบัญชีจากหนึ่งในกลุ่มบัญชีหลักในการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-118">In this field, select whether all accounts should be consolidated to the consolidation account that is set on the **Main accounts** page, or whether you want to select the account from one of the consolidation account groups.</span></span>
    - <span data-ttu-id="b9931-119">**กลุ่มบัญชีหลักในการรวมบัญชี** – เลือกกลุ่มที่จะใช้สำหรับการแม็ปบัญชีหลักสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-119">**Consolidation account group** – Select the group to use for the main account mapping for the consolidation.</span></span>

- <span data-ttu-id="b9931-120">**รอบระยะเวลาการรวมบัญชี** – ใช้ฟิลด์ในส่วนนี้เพื่อกำหนดรอบระยะเวลาการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-120">**Consolidation period** – Use the fields in this section to define the consolidation period.</span></span>

    - <span data-ttu-id="b9931-121">**ตั้งแต่** และ **ถึง** – ระบุช่วงของวันที่สำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-121">**From** and **To** – Specify a range of dates for the consolidation.</span></span> <span data-ttu-id="b9931-122">ถ้าคุณปล่อยให้ฟิลด์นี้ว่าง การรวมบัญชีจะถูกประมวลผลสำหรับรอบระยะเวลาทั้งหมดที่กำหนดในปฏิทินบัญชีแยกประเภทสำหรับบริษัท</span><span class="sxs-lookup"><span data-stu-id="b9931-122">If you leave these fields blank, the consolidation will be processed for all periods that are defined in the ledger calendar for the company.</span></span> <span data-ttu-id="b9931-123">เราไม่แนะนำให้คุณปล่อยให้ฟิลด์เหล่านี้ว่าง</span><span class="sxs-lookup"><span data-stu-id="b9931-123">We don't recommend that you leave these fields blank.</span></span>
    - <span data-ttu-id="b9931-124">**รวมยอดเงินจริง** – ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อรวมข้อมูลจริงของคุณ</span><span class="sxs-lookup"><span data-stu-id="b9931-124">**Include actual amounts** – Set this option to **Yes** to consolidate your actual data.</span></span>
    - <span data-ttu-id="b9931-125">**รวมยอดเงินงบประมาณ** – ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อรวมข้อมูลจากทะเบียนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="b9931-125">**Include budget amounts** – Set this option to **Yes** to consolidate data from the budget register.</span></span>
    - <span data-ttu-id="b9931-126">**สร้างยอดดุลอีกครั้งระหว่างการรวมบัญชี** – เราไม่แนะนำให้คุณตั้งค่าตัวเลือกนี้เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="b9931-126">**Rebuild balances during consolidation** – We don't recommend that you set this option to **Yes**.</span></span> <span data-ttu-id="b9931-127">ให้สร้างยอดดุลเป็นงานชุดงานที่แยกต่างหากแทน</span><span class="sxs-lookup"><span data-stu-id="b9931-127">Instead, rebuild balances as a separate batch job.</span></span>

- <span data-ttu-id="b9931-128">**แบบจำลองงบประมาณ** – ถ้าคุณได้เลือกที่จะรวมข้อมูลงบประมาณ ใช้ฟิลด์ในส่วนนี้เพื่อกำหนดแบบจำลองงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="b9931-128">**Budget models** – If you've selected to consolidate budget data, use the fields in this section to define the budget models.</span></span>

    - <span data-ttu-id="b9931-129">**ตั้งแต่** และ **ถึง** – ระบุช่วงของแบบจำลองที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="b9931-129">**From** and **To** – Specify the range of models to use.</span></span>
    - <span data-ttu-id="b9931-130">**ชนิดอัตรางบประมาณ** – เลือกชนิดของอัตรางบประมาณที่จะใช้สำหรับการแปลงสกุลเงินของข้อมูลงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="b9931-130">**Budget rate type** – Select the type of budget rate to use for currency translation of budget data.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="b9931-131">มิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="b9931-131">Financial dimensions</span></span>
<span data-ttu-id="b9931-132">ในแท็บ **มิติทางการเงิน** คุณกำหนดมิติที่ควรถูกรวมในบริษัทสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-132">On the **Financial dimensions** tab, you define the dimensions that should be included in the consolidation company.</span></span> <span data-ttu-id="b9931-133">เมื่อต้องการเลือกมิติ ตั้งค่าฟิลด์ **ข้อมูลจำเพาะ** เป็น **มิติ** แล้วจากนั้น กำหนดลำดับของมิติในบริษัทสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-133">To select a dimension, set the **Specification** field to **Dimension**, and then define the order of the dimension in the consolidation company.</span></span>

<span data-ttu-id="b9931-134">![แท็บมิติทางการเงิน](./media/financial-dimensions-cons.png "แท็บมิติทางการเงิน")</span><span class="sxs-lookup"><span data-stu-id="b9931-134">![Financial dimensions tab](./media/financial-dimensions-cons.png "Financial dimensions tab")</span></span>

<span data-ttu-id="b9931-135">โดยไม่คำนึงถึงใบสั่งที่คุณกำหนด **บัญชีหลัก** จะเป็นเซ็กเมนต์แรกเสมอ</span><span class="sxs-lookup"><span data-stu-id="b9931-135">Regardless of the order that you define, **Main account** will always be the first segment.</span></span>

## <a name="legal-entities"></a><span data-ttu-id="b9931-136">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="b9931-136">Legal entities</span></span>
<span data-ttu-id="b9931-137">ในแท็บ **นิติบุคคล** คุณกำหนดบริษัทที่ควรจะถูกรวมในบริษัทสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-137">On the **Legal entities** tab, you define the companies that should be included in the consolidation company.</span></span> <span data-ttu-id="b9931-138">คุณยังสามารถกำหนดเปอร์เซ็นต์ความเป็นเจ้าของของบริษัทเหล่านั้นได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b9931-138">You also define the ownership percentage of those companies.</span></span> <span data-ttu-id="b9931-139">ถ้าคุณระบุความเป็นเจ้าของน้อยกว่า 100 เปอร์เซ็นต์ เปอร์เซ็นต์ที่ระบุจะถูกสะสมไปยังบริษัทสำหรับการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-139">If you specify less than 100-percent ownership, the specified percentage will be rolled up to the consolidation company.</span></span> <span data-ttu-id="b9931-140">สำหรับความแตกต่างในการแปลงใดๆ ฟิลด์ **ชนิดบัญชีสำหรับผลต่างการแปลง** จะถูกใช้เพื่อเลือกบัญชีหลักจากการตั้งค่าในหน้า **บัญชีสำหรับธุรกรรมอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="b9931-140">For any translation differences, the **Account type for conversion differences** field is used to select the main account from the setup on the **Accounts for automatic transactions** page.</span></span>

<span data-ttu-id="b9931-141">![แท็บนิติบุคคล](./media/legal-entities-cons.png "แท็บนิติบุคคล")</span><span class="sxs-lookup"><span data-stu-id="b9931-141">![Legal entities tab](./media/legal-entities-cons.png "Legal entities tab")</span></span>

<span data-ttu-id="b9931-142">![หน้าบัญชีสำหรับธุรกรรมอัตโนมัติ](./media/accounts-for-automatic-cons.png "หน้าบัญชีสำหรับธุรกรรมอัตโนมัติ")</span><span class="sxs-lookup"><span data-stu-id="b9931-142">![Accounts for automatic transactions page](./media/accounts-for-automatic-cons.png "Accounts for automatic transactions page")</span></span>

## <a name="elimination"></a><span data-ttu-id="b9931-143">การตัดออก</span><span class="sxs-lookup"><span data-stu-id="b9931-143">Elimination</span></span>
<span data-ttu-id="b9931-144">ในแท็บ **การตัดออก** คุณมีตัวเลือกสามตัวเลือกสำหรับการประมวลผลการตัดออก:</span><span class="sxs-lookup"><span data-stu-id="b9931-144">On the **Elimination** tab, you have three options for processing eliminations:</span></span>

- <span data-ttu-id="b9931-145">เลือกกฎการตัดออก และจากนั้น ในฟิลด์ **ตัวเลือกข้อเสนอ** เลือก **ข้อเสนออย่างเดียว**</span><span class="sxs-lookup"><span data-stu-id="b9931-145">Select the elimination rule, and then, in the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="b9931-146">ตัวเลือกนี้จะประมวลผลการตัดออกในระหว่างกระบวนการรวมบัญชี แต่จะไม่ลงรายการบัญชีทุกอย่างในขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="b9931-146">This option will process the elimination during the consolidation process, but it won't post everything in one step.</span></span> <span data-ttu-id="b9931-147">คุณสามารถลงรายการบัญชีสมุดรายวันได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="b9931-147">You can post the journal later.</span></span>
- <span data-ttu-id="b9931-148">เลือกกฎการตัดออก และจากนั้น ในฟิลด์ **ตัวเลือกข้อเสนอ** เลือก **ลงรายการบัญชีอย่างเดียว**</span><span class="sxs-lookup"><span data-stu-id="b9931-148">Select the elimination rule, and then, in the **Proposal options** field, select **Post only**.</span></span> <span data-ttu-id="b9931-149">ตัวเลือกนี้จะประมวลผลการตัดออกในระหว่างกระบวนการรวมบัญชี และจะลงรายการบัญชีทุกอย่างในขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="b9931-149">This option will process the elimination during the consolidation process and will post everything in one step.</span></span>
- <span data-ttu-id="b9931-150">รันข้อเสนอการตัดออกโดยแยกต่างหากจากกระบวนการรวมบัญชี โดยใช้สมุดรายวันการตัดออก</span><span class="sxs-lookup"><span data-stu-id="b9931-150">Run an elimination proposal separately from the consolidation process by using the elimination journal.</span></span>

<span data-ttu-id="b9931-151">![แท็บการตัดออก](./media/elimination-cons-onl.png "แท็บการตัดออก")</span><span class="sxs-lookup"><span data-stu-id="b9931-151">![Elimination tab](./media/elimination-cons-onl.png "Elimination tab")</span></span>

<span data-ttu-id="b9931-152">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตัดออก ให้ดูที่ [กฎการตัดออก](./elimination-rules.md)</span><span class="sxs-lookup"><span data-stu-id="b9931-152">For more information about eliminations, see [Elimination rules](./elimination-rules.md).</span></span>

## <a name="currency-translation"></a><span data-ttu-id="b9931-153">การแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="b9931-153">Currency translation</span></span>
<span data-ttu-id="b9931-154">ในแท็บ **การแปลงสกุลเงิน** คุณกำหนดนิติบุคคล บัญชีและชนิดอัตราแลกเปลี่ยน และอัตรา</span><span class="sxs-lookup"><span data-stu-id="b9931-154">On the **Currency translation** tab, you define the legal entity, account and exchange rate type, and rate.</span></span> <span data-ttu-id="b9931-155">ตัวเลือกสามตัวเลือกพร้อมใช้งานในฟิลด์ **ใช้อัตราแลกเปลี่ยนจาก** :</span><span class="sxs-lookup"><span data-stu-id="b9931-155">Three options are available in the **Apply exchange rate from** field:</span></span>

- <span data-ttu-id="b9931-156">**วันที่ในการรวมบัญชี** – วันที่ของการรวมบัญชีที่จะใช้เพื่อเรียกดูอัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="b9931-156">**Consolidation date** – The date of the consolidation will be used to get the exchange rate.</span></span> <span data-ttu-id="b9931-157">อัตรานี้จะเท่ากับอัตราตำแหน่งหรือสิ้นเดือน</span><span class="sxs-lookup"><span data-stu-id="b9931-157">This rate is equivalent to the spot or month-end rate.</span></span> <span data-ttu-id="b9931-158">คุณจะเห็นการแสดงตัวอย่างของอัตรา แต่คุณไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="b9931-158">You will see a preview of the rate, but you can't edit it.</span></span>
- <span data-ttu-id="b9931-159">**วันที่ในการทำธุรกรรม** – วันที่ของธุรกรรมแต่ละรายการจะถูกใช้เพื่อเลือกอัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="b9931-159">**Transaction date** – The date of each transaction will be used to select an exchange rate.</span></span> <span data-ttu-id="b9931-160">ตัวเลือกนี้มักใช้สำหรับสินทรัพย์ถาวร และมักจะเรียกว่าอัตราในอดีต</span><span class="sxs-lookup"><span data-stu-id="b9931-160">This option is most often used for fixed assets and is often referred to as a historical rate.</span></span> <span data-ttu-id="b9931-161">คุณไม่สามารถดูตัวอย่างของอัตราได้ เนื่องจากจะเป็นอัตราหลายๆ อัตราสำหรับธุรกรรมต่างๆ ในช่วงบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9931-161">You can't see a preview of the rate, because there will be many rates for the various transactions in the account range.</span></span>
- <span data-ttu-id="b9931-162">**อัตราที่ผู้ใช้กำหนด** – หลังจากที่คุณเลือกตัวเลือกนี้ คุณสามารถป้อนอัตราแลกเปลี่ยนที่คุณต้องการได้</span><span class="sxs-lookup"><span data-stu-id="b9931-162">**User defined rate** – After you select this option, you can enter the exchange rate that you want.</span></span> <span data-ttu-id="b9931-163">ตัวเลือกนี้สามารถเป็นประโยชน์สำหรับอัตราแลกเปลี่ยนเฉลี่ย หรือถ้าคุณกำลังรวมกับอัตราแลกเปลี่ยนคงที่</span><span class="sxs-lookup"><span data-stu-id="b9931-163">This option can be useful for average exchange rates or if you're consolidating against a fixed exchange rate.</span></span>

<span data-ttu-id="b9931-164">![แท็บชนิดการแปลงสกุลเงิน](./media/currency-translation-cons-online.png "แท็บชนิดการแปลงสกุลเงิน")</span><span class="sxs-lookup"><span data-stu-id="b9931-164">![Currency translation tab](./media/currency-translation-cons-online.png "Currency translation tab")</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9931-165">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b9931-165">Additional resources</span></span>

<span data-ttu-id="b9931-166">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการรวมบัญชีและการแปลสกุลเงิน ดูหัวข้อหลักของหัวข้อนี้ [ภาพรวมการรวมบัญชีทางการเงินและการแปลงสกุลเงิน](./financial-consolidations-currency-translation.md)</span><span class="sxs-lookup"><span data-stu-id="b9931-166">For more information about consolidation and currency translations, see the parent topic of this topic, [Financial consolidations and currency translation overview](./financial-consolidations-currency-translation.md).</span></span>

<span data-ttu-id="b9931-167">สำหรับข้อมูลเกี่ยวกับสถานการณ์ที่คุณอาจสร้างการรวมบัญชีงบการเงิน ดู [สร้างงบการเงินที่รวมบัญชี](./generating-consolidated-financial-statements.md)</span><span class="sxs-lookup"><span data-stu-id="b9931-167">For information about scenarios where you might generate consolidate financial statements, see [Generate consolidated financial statements](./generating-consolidated-financial-statements.md).</span></span>
