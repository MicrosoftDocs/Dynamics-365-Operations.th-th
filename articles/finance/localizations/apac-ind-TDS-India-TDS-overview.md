---
title: ภาพรวมของภาษี ณ ที่จ่าย (TDS) ของอินเดีย
description: หัวข้อนี้แสดงรายละเอียดเกี่ยวกับภาษี ณ ที่จ่าย (TDS) ของอินเดีย คู่มือ TDS ครอบคลุมฟังก์ชันของความสามารถนี้
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023641"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="949e9-104">ภาพรวมของภาษี ณ ที่จ่าย (TDS) ของอินเดีย</span><span class="sxs-lookup"><span data-stu-id="949e9-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="949e9-105">หัวข้อนี้แสดงรายละเอียดเกี่ยวกับภาษี ณ ที่จ่าย (TDS) ของอินเดีย</span><span class="sxs-lookup"><span data-stu-id="949e9-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="949e9-106">คู่มือ TDS ครอบคลุมฟังก์ชันของความสามารถนี้</span><span class="sxs-lookup"><span data-stu-id="949e9-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="949e9-107">และยังอธิบายวิธีการตั้งค่าพื้นฐานสำหรับ TDS คํานวณ TDS บนธุรกรรม กรอกข้อมูลกระบวนการชําระเงิน TDS บันทึกหมายเลขใบรับรอง TDS และสร้างการสอบถาม TDS รายงาน TDS และใบรับรอง TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="949e9-108">คู่มือประกอบด้วยหัวข้อต่างๆ ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="949e9-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="949e9-109">การตั้งค่าพื้นฐานสำหรับ TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="949e9-110">ฟังก์ชันโปรแกรมออกแบบสูตรและขีดจํากัดที่ใช้กับการคํานวณ TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="949e9-111">การคํานวณ TDS บนใบแจ้งหนี้ การชำระเงิน ตั๋วสัญญาใช้เงิน และธุรกรรมระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="949e9-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="949e9-112">กระบวนการชําระเงิน TDS ประจำงวด และการชำระจำนวน TDS ให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="949e9-113">การบันทึกและอัปเดตหมายเลขและวันที่ใบรับรอง TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="949e9-114">บทนำสู่ TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-114">Introduction to TDS</span></span>

<span data-ttu-id="949e9-115">ตามบัญชีภาษีเงินได้ 1961 ภาษีเงินได้จะถูกหักที่ต้นทางโดยผู้รับการบริการเมื่อชำระเงินล่วงหน้าหรือลงบัญชีเครดิต แล้วแต่ว่าสิ่งใดเกิดขึ้นก่อน</span><span class="sxs-lookup"><span data-stu-id="949e9-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="949e9-116">บุคคลที่เป็นผู้ที่เป็นผู้ชำระเงินต้องหักจํานวนเงินภาษี และจ่ายเฉพาะยอดเงินสุทธิให้กับผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="949e9-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="949e9-117">TDS จะใช้กับบริการที่รัฐบาลระบุ และภาษีที่หักโดยใช้อัตราที่รัฐบาลระบุเป็นรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="949e9-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="949e9-118">อัตราของการหักจะขึ้นอยู่กับสถานะของเอนทิตี้ที่ได้รับการชำระเงินหรือผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="949e9-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="949e9-119">สถานะประกอบด้วย **บุคคลธรรมดา** **ครอบครัวที่ไม่ได้แบ่งแยก** (**HUF**) **บริษัท** **ห้างหุ้นส่วน** **สมาคมของบุคคล** (**AOP**) **คณะบุคคล** (**BOI**) และ **หน่วยงานท้องถิ่น**</span><span class="sxs-lookup"><span data-stu-id="949e9-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="949e9-120">ส่วนต่อไปนี้แสดงรายการบริการที่ TDS ใช้ ตามที่รัฐบาลอินเดียระบุ</span><span class="sxs-lookup"><span data-stu-id="949e9-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="949e9-121">**ผู้พำนักอาศัย**</span><span class="sxs-lookup"><span data-stu-id="949e9-121">**Residents**</span></span>

- <span data-ttu-id="949e9-122">เงินได้จากเงินเดือน (ภายใต้มาตรา 192)</span><span class="sxs-lookup"><span data-stu-id="949e9-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="949e9-123">เงินได้จากดอกเบี้ยในหลักทรัพย์ (ภายใต้มาตรา 193)</span><span class="sxs-lookup"><span data-stu-id="949e9-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="949e9-124">เงินได้จากเงินปันผล (ภายใต้มาตรา 194)</span><span class="sxs-lookup"><span data-stu-id="949e9-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="949e9-125">เงินได้จากดอกเบี้ย (ภายใต้มาตรา 194A)</span><span class="sxs-lookup"><span data-stu-id="949e9-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="949e9-126">เงินได้จากลอตเตอรี่ หรือรางวัล (ภายใต้มาตรา 194B)</span><span class="sxs-lookup"><span data-stu-id="949e9-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="949e9-127">การชนะแข่งม้า เป็นต้น (ภายใต้มาตรา 194BB)</span><span class="sxs-lookup"><span data-stu-id="949e9-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="949e9-128">ผู้รับเหมาและผู้รับเหมารายย่อย (ภายใต้มาตรา 194C)</span><span class="sxs-lookup"><span data-stu-id="949e9-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="949e9-129">ค่าคอมมิชชันจากประกันภัย (ภายใต้มาตรา 194D)</span><span class="sxs-lookup"><span data-stu-id="949e9-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="949e9-130">เงินได้จากเงินฝากตามแผนเงินออมแห่งชาติ (ภายใต้มาตรา 194EE)</span><span class="sxs-lookup"><span data-stu-id="949e9-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="949e9-131">เงินได้จากกองทุนรวม หรือ UTI (ภายใต้มาตรา 194F)</span><span class="sxs-lookup"><span data-stu-id="949e9-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="949e9-132">ค่าคอมมิชชัน ค่าตอบแทน เงินรางวัล เป็นต้น ของการขายหรือลอตเตอรี่ (ภายใต้มาตรา 194G)</span><span class="sxs-lookup"><span data-stu-id="949e9-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="949e9-133">การจ่ายค่าคอมมิชชันหรือค่านายหน้า (ภายใต้มาตรา 194H)</span><span class="sxs-lookup"><span data-stu-id="949e9-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="949e9-134">ค่าเช่า (ภายใต้มาตรา 194I)</span><span class="sxs-lookup"><span data-stu-id="949e9-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="949e9-135">บริการวิชาชีพ (ภายใต้มาตรา 194J)</span><span class="sxs-lookup"><span data-stu-id="949e9-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="949e9-136">เงินได้จากหน่วย (ภายใต้มาตรา 194K)</span><span class="sxs-lookup"><span data-stu-id="949e9-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="949e9-137">การจ่ายค่าคอมมิชชันในการซื้ออสังหาริมทรัพย์บางรายการ(ภายใต้มาตรา 194LA)</span><span class="sxs-lookup"><span data-stu-id="949e9-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="949e9-138">**ไม่ใช่-ผู้พำนักอาศัย**</span><span class="sxs-lookup"><span data-stu-id="949e9-138">**Non-residents**</span></span>

- <span data-ttu-id="949e9-139">การชำระเงินให้แก่นักกีฬาหรือสมาคมกีฬาที่มีถิ่นที่อยู่นอกประเทศ (ภายใต้มาตรา 194E)</span><span class="sxs-lookup"><span data-stu-id="949e9-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="949e9-140">ผลรวมอื่นๆ (ภายใต้มาตรา 195)</span><span class="sxs-lookup"><span data-stu-id="949e9-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="949e9-141">เงินได้ตามหน่วยงานที่มีถิ่นที่อยู่นอกประเทศ (ภายใต้มาตรา 196A)</span><span class="sxs-lookup"><span data-stu-id="949e9-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="949e9-142">เงินได้จากพันธบัตรในสกุลเงินต่างประเทศหรือหุ้นของบริษัทอินเดีย (ภายใต้มาตรา 196C)</span><span class="sxs-lookup"><span data-stu-id="949e9-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="949e9-143">เงินได้ของนักลงทุนสถาบันต่างประเทศจากหลักทรัพย์ (ภายใต้มาตรา 196D)</span><span class="sxs-lookup"><span data-stu-id="949e9-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="949e9-144">เงินเดือนและเงินได้อื่นๆ ทั้งหมดภายใต้เงินได้ (มาตรา 192)</span><span class="sxs-lookup"><span data-stu-id="949e9-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="949e9-145">ดอกเบี้ยของหลักทรัพย์ (มาตรา 193)</span><span class="sxs-lookup"><span data-stu-id="949e9-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="949e9-146">ดอกเบี้ยนอกเหนือจากดอกเบี้ยของหลักทรัพย์ (มาตรา 194A)</span><span class="sxs-lookup"><span data-stu-id="949e9-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="949e9-147">การชำระเงินให้ผู้รับเหมาและผู้รับเหมารายย่อย (มาตรา 194C)</span><span class="sxs-lookup"><span data-stu-id="949e9-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="949e9-148">การชนะรางวัลลอตเตอรี่ หรือ crossword (มาตรา 194B)</span><span class="sxs-lookup"><span data-stu-id="949e9-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="949e9-149">การชนะการแข่งม้า (มาตรา 194BB)</span><span class="sxs-lookup"><span data-stu-id="949e9-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="949e9-150">ค่าคอมมิชชันจากประกันภัยที่ครอบคลุมการชำระเงินทั้งหมดสําหรับธุรกิจประกันภัยที่ซื้อ (มาตรา 194D)</span><span class="sxs-lookup"><span data-stu-id="949e9-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="949e9-151">ดอกเบี้ยใดๆ นอกเหนือจากดอกเบี้ยในหลักทรัพย์ค้างจ่ายต่อผู้มีถิ่นที่อยู่นอกประเทศ ไม่ได้เป็นบริษัทหรือที่เป็นบริษัทต่างประเทศ (มาตรา 195)</span><span class="sxs-lookup"><span data-stu-id="949e9-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="949e9-152">การชำระเงินให้แก่นักกีฬาที่มีถิ่นที่อยู่นอกประเทศ รวมถึงสมาคมกีฬาหรือสถาบันต่างๆ</span><span class="sxs-lookup"><span data-stu-id="949e9-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="949e9-153">ในกรณีของนักกีฬาที่มีถิ่นที่อยู่นอกประเทศ การจ่ายเงินที่เกี่ยวข้องกับโฆษณา รวมทั้งบทความเกี่ยวกับการเล่นเกม/กีฬาใดๆ ในอินเดีย ในหนังสือพิมพ์ นิตยสาร และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="949e9-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="949e9-154">รวม (มาตรา 194E)</span><span class="sxs-lookup"><span data-stu-id="949e9-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="949e9-155">การชำระเงินตามแผนเงินออมของ NSS \[National Savings Scheme\] (มาตรา 194EE)</span><span class="sxs-lookup"><span data-stu-id="949e9-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="949e9-156">การชำระเงินในบัญชีของการซื้อคืนหน่วยโดยกองทุนหรือ UTI (มาตรา 194F)</span><span class="sxs-lookup"><span data-stu-id="949e9-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="949e9-157">การชำระค่าคอมมิชชันหรือค่านายหน้า (มาตรา 194H)</span><span class="sxs-lookup"><span data-stu-id="949e9-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="949e9-158">การชำระค่าเช่า (มาตรา 194I)</span><span class="sxs-lookup"><span data-stu-id="949e9-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="949e9-159">การชำระค่าธรรมเนียมหรือบริการวิชาชีพหรือทางเทคนิค (มาตรา 194J)</span><span class="sxs-lookup"><span data-stu-id="949e9-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="949e9-160">ค่าคอมมิชชันให้แก่ผู้ขาย ผู้กระจาย ผู้ซื้อและผู้ขายลอตเตอรี่ รวมถึงค่าตอบแทนหรือรางวัลของตั๋วนั้นๆ (มาตรา 194G)</span><span class="sxs-lookup"><span data-stu-id="949e9-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="949e9-161">รายได้จากหน่วยที่ซื้อในสกุลเงินต่างประเทศหรือกําไรระยะยาวที่เกิดจากการโอนย้ายหน่วยดังกล่าว ที่ซื้อในสกุลเงินต่างประเทศ (มาตรา 196B)</span><span class="sxs-lookup"><span data-stu-id="949e9-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="949e9-162">การชำระเงินใดๆ ให้แก่ผู้ที่ไม่ใช่ผู้พนักอยู่ในประเทศ ที่เกี่ยวข้องกับดอกเบี้ยหรือเงินปันผลในพันธบัตรและหุ้น (มาตรา 196C)</span><span class="sxs-lookup"><span data-stu-id="949e9-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="949e9-163">TDS จะคํานวณจากการซื้อ การขาย การส่งคืนจากการขาย ใบลดหนี้ การซื้อสินทรัพย์ถาวร การจ่ายชำระล่วงหน้า การจ่ายเงินล่วงหน้า ตั๋วสัญญาใช้เงิน ภาษีงาน และธุรกรรมระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="949e9-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="949e9-164">ในสถานการณ์ภาษีของอินเดียปัจจุบัน TDS ไม่ได้คํานวณในธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="949e9-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="949e9-165">อย่างไรก็ตาม ระบบรวมส่วนสํารองเพื่อคํานวณยอดเงิน TDS ที่สามารถกู้คืนได้ในธุรกรรมการขาย โดยเฉพาะกับธุรกรรมระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="949e9-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="949e9-166">การคํานวณ TDS จะพิจารณาขีดจำกัดและขีดจำกัดยกเว้นที่กําหนดไว้ เกี่ยวกับส่วนประกอบ TDS เสมอ</span><span class="sxs-lookup"><span data-stu-id="949e9-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="949e9-167">ต้องรันกระบวนการชําระเงิน TDS ประจำงวด และต้องชําระการชําระเงิน TDS ให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="949e9-168">สามารถบันทึกและอัปเดตหมายเลขใบรับรองและวันที่ของใบรับรอง TDS ที่ได้รับจากผู้จัดจำหน่ายหรือลูกค้า</span><span class="sxs-lookup"><span data-stu-id="949e9-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="949e9-169">นอกจากนี้ รายงานรายไตรมาสของแบบฟอร์ม 26Q และแบบฟอร์ม 27Q และใบรับรองแบบฟอร์ม 16A ของ TDS ยังสามารถสร้างขึ้นใน Finance ได้</span><span class="sxs-lookup"><span data-stu-id="949e9-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="949e9-170">การตั้งค่าและใช้งาน TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-170">Setting up and working with TDS</span></span>

<span data-ttu-id="949e9-171">ต่อไปนี้เป็นภาพรวมของกระบวนการตั้งค่าและใช้งาน TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="949e9-172">**ตั้งค่า TDS**</span><span class="sxs-lookup"><span data-stu-id="949e9-172">**TDS setup:**</span></span>

    - <span data-ttu-id="949e9-173">การตั้งค่าพารามิเตอร์:</span><span class="sxs-lookup"><span data-stu-id="949e9-173">Parameter setup:</span></span>

        - <span data-ttu-id="949e9-174">ในพารามิเตอร์บัญชีแยกประเภททั่วไป ให้เรียกใช้พารามิเตอร์ที่เกี่ยวข้องกับ TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="949e9-175">ในพารามิเตอร์บัญชีแยกประเภททั่วไป ให้ตั้งค่าลำดับหมายเลขสำหรับการชำระภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="949e9-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="949e9-176">ตั้งค่าพารามิเตอร์บัญชีเจ้าหนี้และบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="949e9-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="949e9-177">การตั้งค่าพื้นฐาน:</span><span class="sxs-lookup"><span data-stu-id="949e9-177">Basic setup:</span></span>

        - <span data-ttu-id="949e9-178">ตั้งค่าหมายเลขจดทะเบียน TDS ให้กับบริษัท ลูกค้า และผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="949e9-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="949e9-179">ตั้งค่ากลุ่มองค์ประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="949e9-180">ตั้งค่าองค์ประกอบ TDS แนบกลุ่มองค์ประกอบ TDS กับองค์ประกอบเหล่านั้น และกําหนดขีดจำกัด และขีดจำกัดข้อยกเว้นของกลุ่มเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="949e9-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="949e9-181">ตั้งค่าหน่วยงานจัดเก็บภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="949e9-182">ตั้งค่ารอบระยะเวลาการจ่าย TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="949e9-183">ตั้งค่ารหัสภาษี TDS และแนบองค์ประกอบของ TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="949e9-184">ตั้งค่ากลุ่มภาษี TDS และแนบรหัสภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="949e9-185">โปรแกรมออกแบบสูตร ให้กําหนดสูตรเพื่อคํานวณ TDS ให้กับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="949e9-186">บันทึกหมายเลขใบรับรองการยินยอม TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="949e9-187">บัญชีแยกประเภทและการตั้งค่าบริษัท:</span><span class="sxs-lookup"><span data-stu-id="949e9-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="949e9-188">ตั้งค่าบัญชีแยกประเภทของบัญชีเจ้าหนี้และบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="949e9-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="949e9-189">ตั้งค่าหมายเลขบัญชีการหักภาษีและการเรียกเก็บเงิน (TAN) และประเภทชนิดผู้หักบัญชีของบริษัท</span><span class="sxs-lookup"><span data-stu-id="949e9-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="949e9-190">การตั้งค่าอื่นๆ:</span><span class="sxs-lookup"><span data-stu-id="949e9-190">Other setup:</span></span>

        - <span data-ttu-id="949e9-191">ตั้งค่ากำหนดการชำระเงินที่รวมการปันส่วน TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="949e9-192">ตั้งค่าชนิดค่าธรรมเนียมการชำระเงิยเพื่อชำระให้แก่หน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="949e9-193">ตั้งค่าข้อมูลเกี่ยวกับกลุ่ม TDS หมายเลขบัญชีถาวร (PANs) และ TANs ของผู้จัดจำหน่ายและลูกค้า</span><span class="sxs-lookup"><span data-stu-id="949e9-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="949e9-194">**การคำนวณ TDS ในธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="949e9-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="949e9-195">ใบแจ้งหนี้และการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="949e9-195">Invoices and payments</span></span>
    - <span data-ttu-id="949e9-196">ตั๋วสัญญาใช้เงิน</span><span class="sxs-lookup"><span data-stu-id="949e9-196">Promissory notes</span></span>
    - <span data-ttu-id="949e9-197">การชำระเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="949e9-197">Advance payments</span></span>
    - <span data-ttu-id="949e9-198">การชำระเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="949e9-198">Prepayments</span></span>

3. <span data-ttu-id="949e9-199">**การชำระบัญชี TDS**</span><span class="sxs-lookup"><span data-stu-id="949e9-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="949e9-200">กระบวนการชําระเงิน TDS ประจำงวด</span><span class="sxs-lookup"><span data-stu-id="949e9-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="949e9-201">การชำระเงิน TDS ให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS และการสร้าง TDS challan</span><span class="sxs-lookup"><span data-stu-id="949e9-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="949e9-202">**การสอบถาม ใบแจ้งยอด และใบรับรอง TDS:**</span><span class="sxs-lookup"><span data-stu-id="949e9-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="949e9-203">บันทึกและอัปเดตหมายเลขและวันที่ใบรับรอง TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="949e9-204">สร้างการสอบถาม TDS และการสอบถาม TDS ที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="949e9-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="949e9-205">สร้าง TDS แบบฟอร์ม 27A แบบฟอร์ม 26Q และแบบฟอร์ม 27Q และรายงานรายไตรมาส e-TDS</span><span class="sxs-lookup"><span data-stu-id="949e9-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="949e9-206">สร้างใบรับรอง TDS แบบฟอร์ม 16A</span><span class="sxs-lookup"><span data-stu-id="949e9-206">Generate a Form 16A TDS certificate.</span></span>
