---
title: "การประมวลผลสมุดรายวันทั่วไป"
description: "บทความนี้อธิบายถึงความสามารถใน Microsoft Dynamics 365 for Finance and Operations ที่จะช่วยให้การประมวลผลสมุดรายวันทั่วไปทำได้ง่ายขึ้น และยังช่วยรับประกันว่าจะมีการรวบรวมข้อมูลที่ถูกต้องและการควบคุมภายในจะไม่ลดลง"
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: eb46613f805999753c2ab73ffb91a6fdae04c68e
ms.contentlocale: th-th
ms.lasthandoff: 03/26/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="f7724-103">การประมวลผลสมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f7724-103">General journal processing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f7724-104">บทความนี้อธิบายถึงความสามารถใน Microsoft Dynamics 365 for Finance and Operations ที่จะช่วยให้การประมวลผลสมุดรายวันทั่วไปทำได้ง่ายขึ้น และยังช่วยรับประกันว่าจะมีการรวบรวมข้อมูลที่ถูกต้องและการควบคุมภายในจะไม่ลดลง</span><span class="sxs-lookup"><span data-stu-id="f7724-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="f7724-105">ชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f7724-105">Journal names</span></span>

<span data-ttu-id="f7724-106">สิ่งที่สำคัญที่สุดในการตั้งค่าอย่างใดอย่างหนึ่งคือชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f7724-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="f7724-107">ควรกำหนดชื่อสมุดรายวันสำหรับแต่ละวัตถุประสงค์ เช่นระหว่างบริษัท ปรับปรุงตามเกณฑ์คงค้าง และแก้ไขข้อผิดพลาดได้</span><span class="sxs-lookup"><span data-stu-id="f7724-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="f7724-108">คุณสามารถกำหนดชื่อสมุดรายวันแต่ละรายการเพื่ิอช่วยให้การป้อนข้อมูลสำหรับแต่ละวัตถุประสงค์ได้โดยง่าย และปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="f7724-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="f7724-109">ในหน้า **ชื่อสมุดรายวัน** คุณสามารถตั้งค่าองค์ประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f7724-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="f7724-110">**การอนุมัติลำดับงาน**– เมื่อต้องการเพิ่มตัวควบคุมภายใน กำหนดลำดับงานสมุดรายวันที่สร้างข้อจำกัดสาระทางบัญชี สำหรับการตรวจทานและอนุมัติขั้นตอน ขึ้นอยู่กับเงื่อนไขเช่นยอดเงินเดบิตรวม</span><span class="sxs-lookup"><span data-stu-id="f7724-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="f7724-111">คุณตั้งค่าลำดับงานสำหรับสมุดรายวันทั่วไปในหน้า **ลำดับงานบัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="f7724-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="f7724-112">**ค่าเริ่มต้น**– เลือกค่าเริ่มต้นสำหรับบัญชีตรงข้าม สกุลเงิน และมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f7724-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="f7724-113">**การควบคุมสมุดรายวัน**– คุณสามารถตั้งข้อจำกัดเกี่ยวกับบริษัท และชนิดบัญชี และค่าเซ็กเมนต์ได้</span><span class="sxs-lookup"><span data-stu-id="f7724-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="f7724-114">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="f7724-114">**Examples**</span></span>

<span data-ttu-id="f7724-115">ชื่อสมุดรายวันหนึ่งๆสามารถใช้ได้เฉพาะสำหรับการปรับปรุงใดๆเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f7724-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="f7724-116">ในกรณีนี้ คุณสามารถระบุเป็นชนิด **บัญชีแยกประเภทเท่านั้น** ที่ใช้ระหว่างบริษัททั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="f7724-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="f7724-117">[![ชนิดบัญชีควบคุมสมุดรายวัน](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="f7724-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="f7724-118">ชื่อสมุดรายวันสามารถใช้สำหรับเซกเมนต์เฉพาะ หรือช่วงสำหรับบัญชีหลักเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f7724-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="f7724-119">[![เซ็กเมนต์การควบคุมสมุดรายวัน](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="f7724-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="f7724-120">ตัวเลือก **กลับรายการอัตโนมัติ** จะพร้อมใช้งานในสมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f7724-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="f7724-121">ตัวอย่างเช่น คุณมีการปรับปรุงตามเกณฑ์คงค้างที่เอกสารจริงยังไม่มีการประมวลผล ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7724-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="f7724-122">[![กลับรายการสมุดรายวันทั่วไป](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="f7724-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="f7724-123">Microsoft Excel add-in สำหรับรายการสมุดรายวันให้เพิ่มระดับการทำงานอัตโนมัติ และทำให้การป้อนข้อมูลง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="f7724-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="f7724-124">**บรรทัดที่เปิดค้างไว้ในการดำเนินการ Excel**ที่มีอยู่ในหน้า **สมุดรายวันทั่วไป** และ **ใบสำคัญสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="f7724-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="f7724-125">ในหน้า **สมุดรายวันประจำงวด** คุณสามารถตั้งค่าสมุดรายวันที่เกิดซ้ำเพื่อทำการประมวลผลสมุดรายวันได้</span><span class="sxs-lookup"><span data-stu-id="f7724-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="f7724-126">คุณสามารถใช้เท็มเพลตใบสำคัญได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="f7724-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="f7724-127">ในหน้า **สมุดรายวันทั่วไป** พบการดำเนินการ **บันทึก** และการดำเนินการ **เลือกเท็มเพลตใบสำคัญ** ได้ในหน้า  **ใบสำคัญสมุดรายวัน** ภายใต้ **ฟังก์ชัน** สำหรับบรรทัดใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="f7724-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="f7724-128">ตั้งค่าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f7724-128">Related setup</span></span>
<span data-ttu-id="f7724-129">การตั้งค่าต่อไปนี้ไม่ใช่เฉพาะสำหรับสมุดรายวันทั่วไป แต่จะช่วยรับประกันว่า การป้อนข้อมูลเป็นข้อมูลนั้นถูกต้อง และง่าย</span><span class="sxs-lookup"><span data-stu-id="f7724-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="f7724-130">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="f7724-130">Main account</span></span>

<span data-ttu-id="f7724-131">การตั้งค่าบัญชีหลักแสดงหลายตัวเลือกสำหรับการประมวลผลสมุดรายวันทั่วไป:</span><span class="sxs-lookup"><span data-stu-id="f7724-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="f7724-132">**ข้อกำหนด DC/CR** – ใช้ตัวเลือกนี้ถ้าบัญชีหลักถูกจำกัดโดยธุรกรรมเดบิตหรือเครดิต</span><span class="sxs-lookup"><span data-stu-id="f7724-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="f7724-133">การตั้งค่าจะตรวจสอบเมื่อมีการตรวจสอบ หรือการลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f7724-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="f7724-134">**บัญชีตรงข้ามเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="f7724-134">**Default offset account**</span></span>
-   <span data-ttu-id="f7724-135">**ระงับแล้ว** – ระงับบัญชีหลัก สำหรับการป้อนข้อมูลระหว่างบริษัททั้งหมด หรือ สำหรับบริษัท/นิติบุคคล เฉพาะราย</span><span class="sxs-lookup"><span data-stu-id="f7724-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="f7724-136">**ไม่อนุญาตป้อนข้อมูลด้วยตนเอง**– ป้องกันไม่ให้ผู้ใช้ป้อนค่าสำหรับบัญชีในสมุดรายวันด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="f7724-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="f7724-137">**เริ่มต้น/ตรวจสอบความถูกต้องของรหัสสกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="f7724-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="f7724-138">**แทนนิติบุคคล**– ตั้งค่านี้เป็นข้อมูลเฉพาะ บริษัท/นิติบุคคล เฉพาะรายที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="f7724-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="f7724-139">**เริ่มต้น/ตรวจสอบความถูกต้องของกลุ่มภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="f7724-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="f7724-140">**มิติเริ่มต้น**– **ไม่คงที่** หรือ **ค่าคงที่**</span><span class="sxs-lookup"><span data-stu-id="f7724-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="f7724-141">**ค่าคงที่** จะช่วยรับประกันว่า การลงรายการบัญชีทั้งหมดสำหรับบัญชีหลักนี้ใช้ค่ามิติใด ๆ ที่ถูกตั้งค่าเป็น **Fixed**เสมอ</span><span class="sxs-lookup"><span data-stu-id="f7724-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="f7724-142">**การตรวจสอบความถูกต้องของการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="f7724-142">**Posting validation**</span></span>
    -   <span data-ttu-id="f7724-143">**ตรวจสอบผู้ใช้**– ตัวเลือกนี้ควบคุมผู้ใช้ที่ได้รับอนุญาตให้ลงรายการบัญชีไปยังบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="f7724-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="f7724-144">**การลงชนิดการตรวจสอบความถูกต้อง**– ตัวเลือกนี้ควบคุมผู้ใช้ที่ได้รับอนุญาตให้ลงรายการบัญชีไปยังบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="f7724-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="f7724-145">โครงสร้างทางบัญชีและโครงสร้างกฎขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="f7724-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="f7724-146">โครงสร้างทางบัญชีและโครงสร้างกฎขั้นสูงเป็นเรื่องสำคัญอย่างยิ่งในการรับประกันว่า จะรวบรวมข้อมูลที่จำเป็นสำหรับการรายงานทางการเงินและติดตามประสิทธิภาพทางการเงินในระหว่างการประมวลผลสมุดรายวันทั่วไปและเอกสารใด ๆ</span><span class="sxs-lookup"><span data-stu-id="f7724-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="f7724-147">โครงสร้างทางบัญชีและโครงสร้างกฎขั้นสูงช่วยให้คุณสามารถปรับแต่งประสบการณ์การป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f7724-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="f7724-148">คุณสามารถป้อนข้อมูลสำหรับมิติทางการเงินที่เกี่ยวข้องในสถานการณ์แต่ละสถานการณ์ และสามารถบังคับความต้องการที่ได้กำหนดและปรับแก้ข้อมูลที่รวบรวมไว้ให้ถูกต้องอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="f7724-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="f7724-149">สำหรับข้อมูลเพิ่มเติม ให้ดูที่หัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f7724-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="f7724-150">[การวางแผน: ผังบัญชี](plan-chart-of-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="f7724-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="f7724-151">สร้างกฎขั้นสูงสำหรับสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f7724-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="f7724-152">สร้างรายการสมุดรายวันโดยใช้เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="f7724-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="f7724-153">สร้างตรวจสอบความถูกต้องของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f7724-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="f7724-154">ลงรายการบัญชีสมุดรายวันประจำงวด</span><span class="sxs-lookup"><span data-stu-id="f7724-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="f7724-155">ประมวลผลสมุดรายวันการปันส่วนบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="f7724-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



