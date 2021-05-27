---
title: แนบรหัสภาษี TDS กับกลุ่มภาษี TDS และกําหนดสูตรในการคํานวณ TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่ากลุ่มภาษี ภาษี ณ ที่จ่าย (TDS) และแนบรหัสภาษี TDS กับกลุ่มภาษี TDS การคํานวณ TDS ของกลุ่มภาษี TDS คุณต้องกําหนดสูตรของรหัสภาษี TDS ที่แนบอยู่
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023637"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="1efcd-104">แนบรหัสภาษี TDS กับกลุ่มภาษี TDS และกําหนดสูตรในการคํานวณ TDS</span><span class="sxs-lookup"><span data-stu-id="1efcd-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1efcd-105">หัวข้อนี้อธิบายวิธีการตั้งค่ากลุ่มภาษี ภาษี ณ ที่จ่าย (TDS) และแนบรหัสภาษี TDS กับกลุ่มภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="1efcd-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="1efcd-106">การคํานวณ TDS ของกลุ่มภาษี TDS คุณต้องกําหนดสูตรของรหัสภาษี TDS ที่แนบอยู่</span><span class="sxs-lookup"><span data-stu-id="1efcd-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="1efcd-107">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่ากลุ่มภาษี TDS แนบรหัสภาษี TDS กับกลุ่มภาษี และกําหนดสูตรการคํานวณ TDS</span><span class="sxs-lookup"><span data-stu-id="1efcd-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="1efcd-108">ไปที่ **ภาษี \> ภาษีทางอ้อม \> ภาษีหัก ณ ที่จ่าย \> กลุ่มภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="1efcd-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="1efcd-109">[![หน้ากลุ่มภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="1efcd-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="1efcd-110">ในบานหน้าต่างการดำเนินการ เลือก **ใหม่** เพื่อสร้างกลุ่มภาษีหัก ณ ที่จ่ายของ TDS และป้อนรายละเอียดที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="1efcd-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="1efcd-111">ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS**</span><span class="sxs-lookup"><span data-stu-id="1efcd-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="1efcd-112">บน แท็บด่วน **การตั้งค่า** เลือก **เพิ่ม** เพื่อสร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="1efcd-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="1efcd-113">ในฟิลด์ **รหัสภาษีหัก ณ ที่จ่าย** เลือกรหัสภาษี TDS สำหรับกลุ่มภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="1efcd-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="1efcd-114">ฟิลด์ **ชื่อภาษีหัก ณ ที่จ่าย** แสดงชื่อของรหัสภาษี TDS และฟิลด์ **ค่า** แสดงค่า</span><span class="sxs-lookup"><span data-stu-id="1efcd-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="1efcd-115">เมื่อต้องการละเว้นขีดจํากัด และขีดจํากัดข้อยกเว้นที่กําหนดให้กับส่วนประกอบภาษี TDS ที่แนบกับรหัสภาษี TDS ในธุรกรรม TDS ให้เลือกกล่องกาเครื่องหมาย **มองข้ามขีดจํากัดการ**</span><span class="sxs-lookup"><span data-stu-id="1efcd-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="1efcd-116">การป้องกันไม่ให้มีการคํานวณกลุ่มภาษีในธุรกรรม ให้เลือกกล่องกาเครื่องหมาย **ยกเว้น**</span><span class="sxs-lookup"><span data-stu-id="1efcd-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="1efcd-117">ในบานหน้าต่างการดำเนินกาาร ให้เลือก **โปรแกรมออกแบบ** เพื่อเปิดโปรแกรมออกแบบสูตร เพื่อให้คุณสามารถกําหนดสูตรที่ใช้คํานวณ TDS ให้กับกลุ่มภาษี TDS ได้</span><span class="sxs-lookup"><span data-stu-id="1efcd-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="1efcd-118">ในหน้า **โปรแกรมออกแบบ** แท็บ **ภาษี** จะแสดงรหัสภาษี TDS ที่ได้เลือกไว้ สำหรับกลุ่มภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="1efcd-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="1efcd-119">[![หน้าโปรแกรมออกแบบ](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="1efcd-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="1efcd-120">บนแท็บ **การคํานวณ** ให้เลือก **Alt+N** เพื่อสร้างบรรทัด</span><span class="sxs-lookup"><span data-stu-id="1efcd-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="1efcd-121">ฟิลด์ **ID** จะแสดงรหัสควาามสำคัญที่สร้างขึ้นโดยอัตโนมัติสำหรับการคำนวณ TDS</span><span class="sxs-lookup"><span data-stu-id="1efcd-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="1efcd-122">ในฟิลด์ **รหัสภาษี** เลือกรหัสภาษี TDS เพื่อกำหนดสูตรให้</span><span class="sxs-lookup"><span data-stu-id="1efcd-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="1efcd-123">รหัสภาษี TDS ทั้งหมดที่เลือกไว้สำหรับกลุ่มภาษี TDS จะพร้อมใช้งานสำหรับการเลือก ในฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="1efcd-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="1efcd-124">ในฟิลด์ **เกณฑ์ที่คิดภาษีได้** ให้เลือกเกณฑ์การคํานวณ TDS ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="1efcd-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="1efcd-125">**ยอดเงินรวม** – คํานวณ TDS ตามยอดเงินรวมของธุรกรรม (นั่นคือ ยอดเงินในใบแจ้งหนี้) โดยใช้นิพจน์การคํานวณที่กําหนดไว้ของรหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="1efcd-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="1efcd-126">**ไม่รวมยอดเงินรวม** – คํานวณ TDS ตามนิพจน์การคํานวณที่กําหนดไว้เกี่ยวกับรหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="1efcd-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1efcd-127">ฟิลด์ **เกณฑ์ที่คิดภาษีได้** ไม่สามารถตั้งค่าเป็น **ไม่รวมยอดเงินรวม** สำหรับรหัสภาษี TDS ที่มีรหัสความสำคัญ เป็น **1**</span><span class="sxs-lookup"><span data-stu-id="1efcd-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="1efcd-128">การคํานวณ TDS จะขึ้นอยู่กับสูตรที่กําหนดในฟิลด์ **นิพจน์การคํานวณ** สำหรับแต่ละรหัสที่แนบอยู่กับกลุ่มภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="1efcd-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="1efcd-129">เลือกเครื่องหมายบวก (**+**) เครื่องหมายลบ (**-**) เครื่องหมายคูณ (**\**_) หรือเครื่องหมายส่วน (_*/**) เพื่อป้อนนิพจน์การคํานวณสำหรับรหัสภาษี TDS ที่เลือก ในฟิลด์ **นิพจน์การคํานวณ**</span><span class="sxs-lookup"><span data-stu-id="1efcd-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1efcd-130">ไม่สามารถกําหนดนิพจน์การคํานวณใดๆ สำหรับรหัสภาษี TDS ที่มีรหัสความสำคัญเป็น **1**</span><span class="sxs-lookup"><span data-stu-id="1efcd-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="1efcd-131">เมื่อต้องการกําหนดนิพจน์การคํานวณของรหัสภาษี TDS ในฟิลด์ **นิพจน์การคํานวณ** ให้เพิ่มรหัสภาษีTDS ที่พร้อมใช้งานบนแท็บ **ภาษี** เมื่อต้องการเพิ่มรหัสภาษี TDS ในฟิลด์ **นิพจน์การคํานวณ** คุณสามารถใช้วิธีการใดๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1efcd-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="1efcd-132">ลากรหัสภาษีที่ต้องใช้จากแท็บ **ภาษี** ไปยังฟิลด์ **นิพจน์การคํานวณ**</span><span class="sxs-lookup"><span data-stu-id="1efcd-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="1efcd-133">ดับเบิลแท็บ (หรือดับเบิลคลิก) รหัสภาษีที่ต้องการบนแท็บ **ภาษี**</span><span class="sxs-lookup"><span data-stu-id="1efcd-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="1efcd-134">เลือกค้างไว้ (หรือคลิกขวา) รหัสภาษีที่ต้องการบนแท็บ **ภาษี** แล้วเลือก **เพิ่มรหัสภาษี**</span><span class="sxs-lookup"><span data-stu-id="1efcd-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1efcd-135">แทรกนิพจน์การคํานวณก่อนหน้าแต่ละรหัสภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="1efcd-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="1efcd-136">รหัสภาษี TDS ที่ถูกเพิ่มในนิพจน์การคํานวณจะปรากฏในวงเล็บ (\[...\])</span><span class="sxs-lookup"><span data-stu-id="1efcd-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="1efcd-137">เมื่อต้องการล้างข้อมูลนิพจน์การคํานวณที่กําหนดไว้ให้กับรหัสภาษี ในฟิลด์ **นิพจน์การคํานวณ** ให้เลือกปุ่ม **C**</span><span class="sxs-lookup"><span data-stu-id="1efcd-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="1efcd-138">เมื่อต้องการลบเรกคอร์ด บนแท็บ **การคํานวณ** ให้เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="1efcd-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="1efcd-139">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1efcd-139">Close the page.</span></span>
