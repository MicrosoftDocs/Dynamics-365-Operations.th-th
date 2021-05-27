---
title: คํานวณใบแจ้งหนี้ TDS โดยใช้แบบฟอร์มใบสั่งซื้อและแบบฟอร์มใบสั่งขาย
description: หัวข้อนี้แสดงรายการขั้นตอนในการคํานวณภาษี ณ ที่จ่าย (TDS) ในใบแจ้งหนี้ชนิดต่างๆ
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023618"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="e1431-103">คํานวณใบแจ้งหนี้ TDS โดยใช้แบบฟอร์มใบสั่งซื้อและแบบฟอร์มใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="e1431-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1431-104">หัวข้อนี้แสดงรายการขั้นตอนในการคํานวณภาษี ณ ที่จ่าย (TDS) ในใบแจ้งหนี้ชนิดต่างๆ โดยใช้หน้า **ใบสั่งซื้อ** **สมุดรายวันการซื้อ** **ใบสั่งซื้อแบบล็อตใหญ่** และ **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="e1431-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="e1431-105">สร้างใบสั่งซื้อ สมุดรายวันการซื้อ ใบสั่งซื้อแบบล็อตใหญ่ หรือใบสั่งขาย โดยใช้หน้าที่แสดงรายการ</span><span class="sxs-lookup"><span data-stu-id="e1431-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="e1431-106">ป้อนรายละเอียดที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="e1431-106">Enter the required details.</span></span>

2. <span data-ttu-id="e1431-107">เลือกแท็บ **การตั้งค่า** เพื่อดูลักษณะการประเมินของผู้จัดจำหน่ายหรือลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e1431-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="e1431-108">ข้อมูลนี้จะแสดงรายการอยู่ในฟิลด์ **ลักษณะการประเมิน** ภายใต้กลุ่มฟิลด์ **กลุ่มภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e1431-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="e1431-109">ในฟิลด์ **กลุ่ม TDS** ให้ดูหรือแก้ไขกลุ่ม TDS เริ่มต้นที่กําหนดไว้สำหรับผู้จัดจำหน่ายหรือลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e1431-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e1431-110">ฟิลด์ **กลุ่ม TCS** ไม่พร้อมใช้งาน เมื่อคุณเลือกกลุ่ม TDS ในฟิลด์ **กลุ่ม TDS**</span><span class="sxs-lookup"><span data-stu-id="e1431-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="e1431-111">TDS จะถูกคํานวณเฉพาะถ้ามีการเลือกกล่องกาเครื่องหมาย **คํานวณภาษีหัก ณ ที่จ่าย** เฉพาะกับผู้จัดจำหน่ายหรือลูกค้า บนหน้า **ผู้จัดจำหน่ายทั้งหมด** หรือ **ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="e1431-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="e1431-112">สร้างบรรทัดสินค้าบนแท็บ **รายการ** และป้อนรายละเอียดที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="e1431-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="e1431-113">เลือกแท็บ **การตั้งค่า** (ระดับบรรทัด) เพื่อดูหรือเปลี่ยนกลุ่ม TDS ที่กําหนดในระดับหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="e1431-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="e1431-114">กลุ่ม TDS จะแสดงอยู่ในฟิลด์ **กลุ่ม TDS** ซึ่งอยู่ภายใต้กลุ่มฟิลด์ **กลุ่มภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e1431-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="e1431-115">เลือกแท็บ **ข้อมูลภาษี** และเลือกที่อยู่อื่น ที่ตั้งค่าไว้ให้กับชื่อบริษัทที่แสดงในฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="e1431-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="e1431-116">ชื่อบริษัทที่แสดงในฟิลด์ **ชื่อ** ซึ่งอยู่ภายใต้กลุ่มฟิลด์ **ข้อมูลบริษัท**</span><span class="sxs-lookup"><span data-stu-id="e1431-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="e1431-117">TAN ของชื่อบริษัทที่เลือกจะแสดงขึ้นในฟิลด์ **หมายเลขบัญชีภาษี** (**TAN**) ภายใต้กลุ่มฟิลด์ **ภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e1431-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="e1431-118">เลือก **ภาษีหัก ณ ที่จ่าย** เพื่อเปิดหน้า **ธุรกรรมภาษีหัก ณ ที่จ่าย ชั่วคราว**</span><span class="sxs-lookup"><span data-stu-id="e1431-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="e1431-119">ดูฟิลด์ต่อไปนี้บนบานหน้าต่างด้านบนของหน้า **ธุรกรรมภาษีหัก ณ ที่จ่ายชั่วคราว**</span><span class="sxs-lookup"><span data-stu-id="e1431-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="e1431-120">**หัก ณ ที่จ่าย** **ภาษี** **จำนวน** **ใน** **ยอดรวม** - TDS รวมที่คํานวณได้สำหรับธุรกรรมของกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="e1431-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="e1431-121">**ค่า** - เปอร์เซ็นต์รวมที่ใช้ในการคํานวณ TDS ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="e1431-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="e1431-122">เปอร์เซ็นต์รวมจะขึ้นอยู่กับสูตรที่กําหนดให้กับรหัสภาษี TDS ที่แนบกับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="e1431-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="e1431-123">**ยอดรวมภาษีหัก ณ ที่จ่ายที่ปรับปรุง** - ยอดรวม TDS ที่ปรับปรุงของรหัสภาษีทั้งหมดในกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="e1431-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="e1431-124">**TDS** - ถ้าเลือกไว้ กลุ่ม TDS จะถูกแนบกับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="e1431-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="e1431-125">ฟิลด์บนแท็บ **ภาพรวม** **ทั่วไป** และ **การปรับปรุง** บนหน้า **ธุรกรรมภาษีหัก ณ ที่จ่ายชั่วคราว** แสดงจำนวน TDS ที่คํานวณได้ และรายละเอียดจำนวน TDS ที่ปรับปรุง สำหรับแต่ละรหัสภาษี TDS ที่แนบกับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="e1431-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="e1431-126">เลือก **ขีดจำกัด** เพื่อเปิดหน้า **ขีดจำกัด**</span><span class="sxs-lookup"><span data-stu-id="e1431-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="e1431-127">ดูขีดจํากัดที่กําหนดไว้ให้กับส่วนประกอบภาษี TDS ที่แนบกับรหัสภาษี TDS เฉพาะ บนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e1431-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="e1431-128">เลือก **โปรแกรมออกแบบสูตร** เพื่อเปิดหน้า **โปรแกรมออกแบบสูตร**</span><span class="sxs-lookup"><span data-stu-id="e1431-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="e1431-129">ดูสูตรที่กําหนดไว้สำหรับรหัสภาษี TDS ที่ระบุ บนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e1431-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="e1431-130">ลงรายการบัญชีใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="e1431-130">Post the invoice.</span></span> <span data-ttu-id="e1431-131">ระบบลงรายการบัญชีจำนวน TDS ที่คํานวณได้จากใบแจ้งหนี้การซื้อในบัญชีเจ้าหนี้ และมีการลงรายการบัญชีจำนวน TDS ที่คํานวณในใบแจ้งหนี้การขายที่บัญชีลูกหนี้ ซึ่งกําหนดไว้สำหรับรหัสภาษี TDS แต่ละรหัส ในกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="e1431-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="e1431-132">บัญชีเจ้าหนี้หรือบัญชีลูกหนี้ที่มีรหัสภาษี TDS ถูกกําหนดในหน้า **รหัสภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e1431-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="e1431-133">เลือกปุ่ม **การสอบถาม** ปุ่ม **> ใบแจ้งหนี้ > ภาษีหัก ณ ที่จ่ายที่ลงรายการบัญชี** เพื่อเปิดหน้า **ธุรกรรมภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e1431-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="e1431-134">คุณสามารถดูเปอร์เซ็นต์รวมที่ใช้ในการคํานวณ TDS ของธุรกรรม ในฟิลด์ **ค่า**</span><span class="sxs-lookup"><span data-stu-id="e1431-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="e1431-135">ฟิลด์บนแท็บ **ภาพรวม** **ทั่วไป** และ **จำนวน** บนหน้า  **ธุรกรรมภาษีหัก ณ ที่จ่าย** แสดงข้อมูลของ TDS ที่คํานวณไว้ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="e1431-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="e1431-136">ดูข้อมูลการคํานวณ TDS ของแต่ละรหัสภาษี TDS ที่แนบกับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="e1431-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
