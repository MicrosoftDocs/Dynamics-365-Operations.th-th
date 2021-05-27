---
title: คํานวณ TDS บนใบแจ้งหนี้โดยใช้สมุดรายวัน
description: หัวข้อนี้แสดงรายการขั้นตอนในการคํานวณภาษี ณ ที่จ่าย (TDS) ในสมุดรายวัน
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023642"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="8ee47-103">คํานวณ TDS บนใบแจ้งหนี้โดยใช้สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ee47-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ee47-104">หัวข้อนี้แสดงรายการขั้นตอนในการคํานวณภาษี ณ ที่จ่าย (TDS) ในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ee47-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="8ee47-105">เริ่มต้นด้วยการเปิดหน้า **สมุดรายวันทั่วไป** (**บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป**)</span><span class="sxs-lookup"><span data-stu-id="8ee47-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="8ee47-106">[![สมุดรายวันทั่วไป](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="8ee47-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="8ee47-107">สร้างบรรทัดสมุดรายวันโดยใช้แบบฟอร์มสมุดรายวันที่แสดงรายการอยู่ในตาราง</span><span class="sxs-lookup"><span data-stu-id="8ee47-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="8ee47-108">เลือกชนิดบัญชีและชนิดบัญชีตรงข้าม และป้อนจำนวนของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="8ee47-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="8ee47-109">บนหน้า **สมุดรายวันการอนุมัติใบแจ้งหนี้** ให้เลือก **ค้นหาใบสำคัญ** และเลือกใบแจ้งหนี้ที่จะคํานวณ TDS</span><span class="sxs-lookup"><span data-stu-id="8ee47-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="8ee47-110">ดูใบแจ้งหนี้ที่สร้างขึ้นในหน้า **ทะเบียนใบแจ้งหนี้** หรือหน้า **ค้าหาใบสำคัญ**</span><span class="sxs-lookup"><span data-stu-id="8ee47-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="8ee47-111">บนแท็บ **ทั่วไป** ของหน้า **ใบสำคัญสมุดรายวัน** ให้ดูหรือแก้ไขกลุ่ม TDS เริ่มต้นที่กําหนดไว้ให้กับผู้จัดจำหน่ายหรือลูกค้า ในฟิลด์ **กลุ่ม TDS**</span><span class="sxs-lookup"><span data-stu-id="8ee47-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="8ee47-112">จำนวน TDS ที่คํานวณในบรรทัดสมุดรายวันจะขึ้นอยู่กับสูตรที่กําหนดไว้ของรหัสภาษี TDS ที่แสดงรายการอยู่ในฟิลด์ **กลุ่ม TDS**</span><span class="sxs-lookup"><span data-stu-id="8ee47-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="8ee47-113">ฟิลด์ **กลุ่มภาษีหัก ณ ที่จ่าย** และ **กลุ่ม TCS** จะไม่พร้อมใช้งานเมื่อคุณเลือกกลุ่ม TDS ในฟิลด์ **กลุ่ม TDS**</span><span class="sxs-lookup"><span data-stu-id="8ee47-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="8ee47-114">ฟิลด์ **กลุ่มภาษีหัก ณ ที่จ่าย** จะพร้อมใช้งานในหน้า **สมุดรายวันทั่วไป** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8ee47-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="8ee47-115">TDS จะถูกคํานวณเฉพาะถ้ามีการเลือกกล่องกาเครื่องหมาย **คํานวณภาษีหัก ณ ที่จ่าย** เฉพาะกับผู้จัดจำหน่ายหรือลูกค้า ในหน้า **ผู้จัดจำหน่ายทั้งหมด** หรือ **ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8ee47-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="8ee47-116">เลือกแท็บ **ข้อมูลภาษี** เลือกที่อยู่อื่นของบริษัทที่ตั้งค่าไว้ให้กับบริษัทในฟิลด์นี้ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="8ee47-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="8ee47-117">คุณสามารถดูชื่อบริษัทในฟิลด์ **ชื่อ** ซึ่งอยู่ภายใต้กลุ่มฟิลด์ **ข้อมูลบริษัท**</span><span class="sxs-lookup"><span data-stu-id="8ee47-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="8ee47-118">ดูประเภทลักษณะของการประเมินของผู้จัดจำหน่ายหรือลูกค้า ในฟิลด์ **ลักษณะของการประเมิน** ซึ่งอยู่ภายใต้กลุ่มฟิลด์ **ภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="8ee47-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="8ee47-119">ในฟิลด์ **หมายเลขบัญชีภาษี** (**TAN**) ดู TAN ของชื่อบริษัทที่เลือก ที่แสดงอยู่</span><span class="sxs-lookup"><span data-stu-id="8ee47-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="8ee47-120">เลือก **ภาษีหัก ณ ที่จ่าย** ในเมนู **ภาษีหัก ณ ที่จ่าย** เพื่อเปิดหน้า **ธุรกรรมภาษีหัก ณ ที่จ่ายชั่วคราว**</span><span class="sxs-lookup"><span data-stu-id="8ee47-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="8ee47-121">ฟิลด์ต่อไปนี้จะแสดงอยู่ในบานหน้าต่างด้านบนของหน้า **ธุรกรรมภาษีหัก ณ ที่จ่ายชั่วคราว**</span><span class="sxs-lookup"><span data-stu-id="8ee47-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="8ee47-122">**ยอดรวมภาษีหัก ณ ที่จ่าย** - TDS รวมที่คํานวณได้สำหรับธุรกรรมของกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="8ee47-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="8ee47-123">**ค่า** - เปอร์เซ็นต์รวมที่ใช้ในการคํานวณ TDS ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="8ee47-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="8ee47-124">เปอร์เซ็นต์รวมจะขึ้นอยู่กับสูตรที่กําหนดให้กับรหัสภาษี TDS ที่แนบกับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="8ee47-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="8ee47-125">**ยอดรวมภาษีหัก ณ ที่จ่ายที่ปรับปรุง** - ยอดรวม TDS ที่ปรับปรุงของรหัสภาษีทั้งหมดในกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="8ee47-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="8ee47-126">**TDS** - ถ้าเลือกไว้ กลุ่ม TDS จะถูกแนบกับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="8ee47-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="8ee47-127">ฟิลด์บนแท็บ **ภาพรวม** **ทั่วไป** และ **การปรับปรุง** บนหน้า **ธุรกรรมภาษีหัก ณ ที่จ่ายชั่วคราว** แสดงจำนวน TDS ที่คํานวณได้ และรายละเอียดจำนวน TDS ที่ปรับปรุง สำหรับแต่ละรหัสภาษี TDS ที่แนบกับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="8ee47-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="8ee47-128">เลือก **ขีดจำกัด** เพื่อเปิดหน้า **ขีดจำกัด**</span><span class="sxs-lookup"><span data-stu-id="8ee47-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="8ee47-129">ดูขีดจํากัดและขีดจํากัดข้อยกเว้นที่กําหนดไว้ให้กับส่วนประกอบภาษี TDS ที่แนบกับรหัสภาษี TDS เฉพาะ บนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="8ee47-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="8ee47-130">เลือก **โปรแกรมออกแบบสูตร** เพื่อเปิดฟอร์ม **โปรแกรมออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="8ee47-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="8ee47-131">ดูสูตรที่กําหนดไว้สำหรับรหัสภาษี TDS ที่ระบุในหน้านี้</span><span class="sxs-lookup"><span data-stu-id="8ee47-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="8ee47-132">ปิดหน้า **โปรแกรมออกแบบสูตร** และหน้า **ธุรกรรมภาษีหัก ณ ที่จ่ายชั่วคราว** เพื่อกลับไปที่หน้า **ใบสำคัญสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="8ee47-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="8ee47-133">ป้อนรายละเอียดที่จำเป็นอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="8ee47-133">Enter the other required details.</span></span> <span data-ttu-id="8ee47-134">ตรวจสอบความถูกต้องและลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="8ee47-134">Validate and post the journal.</span></span> <span data-ttu-id="8ee47-135">มีการลงรายการบัญชีจำนวน TDS ที่คํานวณได้จากใบแจ้งหนี้การซื้อไปยังบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="8ee47-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="8ee47-136">จำนวน TDS ที่คํานวณในใบแจ้งหนี้การขายจะมีการลงรายการบัญชีไปยังบัญชีลูกหนี้ ที่กําหนดไว้ให้กับรหัสภาษี TDS แต่ละรหัสในกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="8ee47-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="8ee47-137">บัญชีเจ้าหนี้หรือบัญชีลูกหนี้ที่มีรหัสภาษี TDS ถูกกําหนดในหน้า **รหัสภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="8ee47-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="8ee47-138">เลือก **ภาษีหัก ณ ที่จ่ายที่ลงรายการบัญชี** เพื่อเปิดหน้า **หัก ณ ที่จ่าย** **ภาษี** **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="8ee47-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="8ee47-139">ในฟิลด์ **ค่า** จะมีการแสดงเปอร์เซ็นต์รวมที่ใช้ในการคํานวณ TDS ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="8ee47-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="8ee47-140">ฟิลด์บนแท็บ **ภาพรวม** **ทั่วไป** และ **จำนวน** ในหน้าธุรกรรมภาษีหัก ณ ที่จ่าย แสดงจำนวน TDS ที่คํานวณได้และรายละเอียดจำนวน TDS ที่ปรับปรุง สำหรับแต่ละรหัสภาษี TDS ที่แนบกับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="8ee47-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
