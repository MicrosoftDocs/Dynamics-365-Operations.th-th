---
title: ตัดจำหน่ายสินทรัพย์ถาวรให้เป็นของเสีย
description: หัวข้อนี้จะอธิบายถึงขั้นตอนการตัดรายการธุรกรรมสำหรับสินทรัพย์ถาวรที่ถูกตัดจำหน่ายเป็นของเสีย
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 42eaa3df5ab09278ed96506d17e1b42d4fc2a9e1
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570275"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="1908b-103">ตัดจำหน่ายสินทรัพย์ถาวรให้เป็นของเสีย</span><span class="sxs-lookup"><span data-stu-id="1908b-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1908b-104">หัวข้อนี้จะอธิบายถึงขั้นตอนการตัดรายการธุรกรรมสำหรับสินทรัพย์ถาวรที่ถูกตัดจำหน่ายเป็นของเสีย</span><span class="sxs-lookup"><span data-stu-id="1908b-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="1908b-105">ชนิดของธุรกรรมที่สามารถตัดออกได้รวมถึงธุรกรรมการซื้อสินทรัพย์และธุรกรรมค่าเสื่อมราคาสะสมของสินทรัพย์และธุรกรรมสินทรัพย์ถาวรอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1908b-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="1908b-106">การตัดออกของธุรกรรมเหล่านี้จะมีผลกระทบต่อบัญชีงบดุล เช่นการปรับปรุงการซื้อสินทรัพย์ การปรับปรุงค่าเสื่อมราคา การประเมินค่าใหม่ และการเพิ่มและลดค่าในบัญชี</span><span class="sxs-lookup"><span data-stu-id="1908b-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="1908b-107">ธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="1908b-107">Transaction</span></span>                                         | <span data-ttu-id="1908b-108">เดบิต (Dr.)</span><span class="sxs-lookup"><span data-stu-id="1908b-108">Debit (Dr.)</span></span> | <span data-ttu-id="1908b-109">เครดิต (Cr.)</span><span class="sxs-lookup"><span data-stu-id="1908b-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="1908b-110">ค่าเสื่อมราคาสะสมของ Dr.</span><span class="sxs-lookup"><span data-stu-id="1908b-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="1908b-111">X</span><span class="sxs-lookup"><span data-stu-id="1908b-111">X</span></span>           |              |
| <span data-ttu-id="1908b-112">กำไร/ขาดทุนจากสินทรัพย์ถาวรของ Cr.</span><span class="sxs-lookup"><span data-stu-id="1908b-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="1908b-113">X</span><span class="sxs-lookup"><span data-stu-id="1908b-113">X</span></span>            |
| <span data-ttu-id="1908b-114">กำไร/ขาดทุนจากสินทรัพย์ถาวรของ Dr.</span><span class="sxs-lookup"><span data-stu-id="1908b-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="1908b-115">X</span><span class="sxs-lookup"><span data-stu-id="1908b-115">X</span></span>           |              |
| <span data-ttu-id="1908b-116">บัญชีการซื้อสินทรัพย์ถาวรของ Cr.</span><span class="sxs-lookup"><span data-stu-id="1908b-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="1908b-117">X</span><span class="sxs-lookup"><span data-stu-id="1908b-117">X</span></span>            |
| <span data-ttu-id="1908b-118">กำไร/ขาดทุนจากสินทรัพย์ถาวรของ Dr. (\[NBV\] มูลค่าสุทธิตามบัญชี)</span><span class="sxs-lookup"><span data-stu-id="1908b-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="1908b-119">X</span><span class="sxs-lookup"><span data-stu-id="1908b-119">X</span></span>           |              |
| <span data-ttu-id="1908b-120">กำไร/ขาดทุนจากสินทรัพย์ถาวรของ Cr. (NBV)</span><span class="sxs-lookup"><span data-stu-id="1908b-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="1908b-121">X</span><span class="sxs-lookup"><span data-stu-id="1908b-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="1908b-122">เราขอแนะนำให้คุณทำงานร่วมกับประธานเจ้าหน้าที่ฝ่ายการเงิน (CFO) หรือผู้ควบคุมของบริษัทของคุณอย่างใกล้ชิด เพื่อระบุบัญชีที่ถูกต้องและนำไปใช้สำหรับธุรกรรมแต่ละชนิด และเพื่อตรวจสอบว่ากระบวนการตัดจำหน่าย และธุรกรรมที่สร้างขึ้นจะเป็นไปตามการอัพเดตของบัญชีเหล่านั้นอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="1908b-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="1908b-123">ก่อนที่คุณจะตัดจำหน่ายสินทรัพย์ถาวรเป็นของเสีย คุณต้องสร้างบัญชีแยกประเภทที่สัมพันธ์กับมูลค่าการซื้อสินทรัพย์ ค่าเสื่อมราคาสำหรับปีปัจจุบันค่า ค่าเสื่อมราคาสำหรับปีก่อนหน้า และ NBV ของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1908b-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="1908b-124">ชนิดของธุรกรรมสินทรัพย์ถาวรจะแสดงรายการในหน้า **โพรไฟล์การลงบัญชีสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="1908b-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="1908b-125">ไปที่ **สินทรัพย์ถาวร \> การตั้งค่า \> โพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร** จากนั้น ให้เลือกแท็บด่วน **การตัดจำหน่าย** ให้เลือก **ของเสีย** ในฟิลด์ข้างบนกริด</span><span class="sxs-lookup"><span data-stu-id="1908b-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="1908b-126">ภาพประกอบต่อไปนี้แสดงรายการของชนิดของธุรกรรมสินทรัพย์ถาวรในหน้า **โพรไฟล์การลงบัญชีสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="1908b-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="1908b-127">[![การตัดจำหน่ายสินทรัพย์เป็นเป็นของเสีย, รูปที่ 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="1908b-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="1908b-128">ตัวอย่างต่อไปนี้คือสินทรัพย์ถาวรที่ได้มาเพิ่มในวันที่ 1 มกราคม 2018 และจะเป็นของเสียใน วันที่ 31 มีนาคม 2019</span><span class="sxs-lookup"><span data-stu-id="1908b-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="1908b-129">**ราคาทุนของสินทรัพย์:** 24,000.00 ดอลลาร์สหรัฐ (USD)</span><span class="sxs-lookup"><span data-stu-id="1908b-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="1908b-130">**อายุการใช้งาน:** สองปี</span><span class="sxs-lookup"><span data-stu-id="1908b-130">**Service life:** Two years</span></span>
- <span data-ttu-id="1908b-131">**วิธีการคิดค่าเสื่อมราคา:** อายุการใช้งานแบบเส้นตรง</span><span class="sxs-lookup"><span data-stu-id="1908b-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="1908b-132">**ยอดค่าเสื่อมราคา:** 1,000.00 USD ต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="1908b-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="1908b-133">NBV ของสินทรัพย์ถาวรจะถูกคำนวณโดยใช้สูตรดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1908b-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="1908b-134">มูลค่าตามบัญชีสุทธิ = ราคาการซื้อสินทรัพย์ – ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="1908b-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="1908b-135">ตัวอย่างต่อไปนี้ มีการซื้อสินทรัพย์ถาวรและคิดค่าเสื่อมราคาเป็นเวลา 15 เดือน ตั้งแต่เดือนมกราคม 2018 จนถึงเดือนมีนาคม 2019</span><span class="sxs-lookup"><span data-stu-id="1908b-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="1908b-136">ดังนั้น NBV ของสินทรัพย์นี้คือ 9,000.00 USD (24,000.00 USD – 15,000.00 USD)</span><span class="sxs-lookup"><span data-stu-id="1908b-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="1908b-137">[![ตัวอย่างวิธีการคิดค่าเสื่อมราคาของสินทรัพย์ถาวร](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="1908b-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="1908b-138">เมื่อต้องการสร้างสมุบันทึกการตัดจำหน่ายรายวัน ให้ไปที่ **สินทรัพย์ถาวร \> รายการสมุดรายวัน \> สมุดรายวันสินทรัพย์ถาวร** จากนั้น ในบานหน้าต่างดำเนินการ ให้เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="1908b-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="1908b-139">เลือก **การตัดจำหน่าย - ของเสีย**– จากนั้นให้เลือก ID สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="1908b-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="1908b-140">ถ้าต้องกาตัดจำหน่ายสินทรัพย์แบบเต็มจำนวน อย่าป้อนค่าใด ๆ ลงในฟิลด์**เดบิต** หรือฟิลด์ **เครดิต**</span><span class="sxs-lookup"><span data-stu-id="1908b-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="1908b-141">[![สมุดรายวันสินทรัพย์ถาวร](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="1908b-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="1908b-142">ธุรกรรมการตัดจำหน่ายสินทรัพย์ถาวรเป็นของเสีย จะเปลี่ยนแปลงค่าฟิลด์ต่าง ๆ ในสมุดบัญชีทรัพย์สินถาวรดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1908b-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="1908b-143">ในส่วน **ยอดดุล** ฟิลด์ **สถานะ** จะถูกอัพเดตเป็น **ของเสีย**</span><span class="sxs-lookup"><span data-stu-id="1908b-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="1908b-144">ในส่วน **การออกใช้** ฟิลด์ **วันที่ตัดจำหน่าย** จะถูกกำหนดเป็นวันที่ที่มีการตัดจำหน่ายสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1908b-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="1908b-145">[![รายละเอียดของสมุดรายวันสินทรัพย์ถาวร](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="1908b-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="1908b-146">ภาพประกอบต่อไปนี้แสดงยอดดุลของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="1908b-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="1908b-147">[![ยอดดุลสินทรัพย์ถาวร](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="1908b-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="1908b-148">ภาพประกอบต่อไปนี้แสดงใบสำคัญที่ถูกลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="1908b-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="1908b-149">[![มูลค่าตามบัญชีสุทธิ](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="1908b-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
