---
title: ชำระเงิน TDS ให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS และสร้าง TDS challan
description: หัวข้อนี้อธิบายวิธีการชำระเงินภาษีที่หักที่ต้นทาง (TDS) ให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023635"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="afc94-103">ชำระเงิน TDS ให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS และสร้าง TDS challan</span><span class="sxs-lookup"><span data-stu-id="afc94-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afc94-104">หัวข้อนี้อธิบายวิธีการชำระเงินภาษีที่หักที่ต้นทาง (TDS) ให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="afc94-105">ไปที่ **บัญชีเจ้าหนี้ \> การชำระเงิน \> สมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="afc94-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="afc94-106">[![หน้าในสมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่าย](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="afc94-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="afc94-107">บนหน้า **สมุดรายวันการชำระเงินของผู้จัดจำหน่าย** เลือก **สร้าง** เพื่อสร้างบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afc94-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="afc94-108">ในฟิลด์ **บัญชี** เลือกผู้จัดจำหน่ายของหน่วยงาน TDS เพื่อทำการชำระเงินให้</span><span class="sxs-lookup"><span data-stu-id="afc94-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="afc94-109">เลือก **ธุรกรรมการชําระเงิน** เพื่อเปิดหน้า **ธุรกรรมการชําระเงิน** ที่ซึ่งคุณสามารถดูธุรกรรม TDS ที่ชําระแล้วสำหรับผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="afc94-110">ธุรกรรม TDS ที่ชําระแล้วสำหรับรอบระยะเวลาการชำระเงิน จะแสดงในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="afc94-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="afc94-111">ธุรกรรม TDS ที่ลักษณะของประเภทผู้ถูกประเมินเป็น **บริษัท** ถูกแสดงเป็นรายการธุรกรรมเดียว</span><span class="sxs-lookup"><span data-stu-id="afc94-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="afc94-112">ธุรกรรม TDS ที่ลักษณะของประเภทผู้ถูกประเมินคือ **HUF**, **บริษัท**, **บุคคล**, **AOP**, **BOI**, **หน่วยงานท้องถิ่น** หรือ **อื่นๆ** ถูกแสดงเป็นรายการธุรกรรมเดียว</span><span class="sxs-lookup"><span data-stu-id="afc94-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="afc94-113">ฟิลด์ **ยอดเงิน** แสดงยอดเงินรวมของ TDS ที่ครบกําหนดชําระให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="afc94-114">เลือก **ธุรกรรมภาษีหัก ณ ที่จ่าย** เพื่อดูธุรกรรม TDS ต่างๆ ที่รวมอยู่ในเรกคอร์ดการชําระเงิน</span><span class="sxs-lookup"><span data-stu-id="afc94-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="afc94-115">คุณสามารถดูการแบ่งธุรกรรม TDS แต่ละธุรกรรมที่รวมอยู่ในกระบวนการชําระเงินสำหรับรอบระยะเวลาการชำระเงินบนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="afc94-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="afc94-116">บนแท็บ **ภาพรวม** ให้เลือกกล่องกาเครื่องหมาย **ทำเครื่องหมาย** สำหรับธุรกรรม TDS เพื่อชำระเงินให้กับผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="afc94-117">แท็บ **ภาพรวม** แสดงข้อมูลต่อไปนี้ของธุรกรรม TDS ที่เปิดแต่ละธุรกรรม:</span><span class="sxs-lookup"><span data-stu-id="afc94-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="afc94-118">**วันที่** – วันที่ของธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="afc94-119">**ใบสำคัญ** – หมายเลขใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="afc94-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="afc94-120">**แหล่งที่มา** – โมดูลที่มีการลงรายการบัญชีธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="afc94-121">**ผู้จัดจำหน่าย/ลูกค้า** – หมายเลขบัญชีของลูกค้าหรือผู้จัดจำหน่ายที่ TDS ไม่ถูกหักออก</span><span class="sxs-lookup"><span data-stu-id="afc94-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="afc94-122">**ชื่อของผู้ถูกหัก/ฝ่าย** – ชื่อของผู้จัดจำหน่ายหรือลูกค้าที่จะหัก TDS ออก</span><span class="sxs-lookup"><span data-stu-id="afc94-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="afc94-123">**ธรรมชาติของผู้ถูกประเมิน** – ธรรมชาติของประเภทผู้ถูกประเมินที่ผู้ถูกหักลดเป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="afc94-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="afc94-124">**จำนวน** – ยอดที่ TDS คำนวณได้จากยอดเงินใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="afc94-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="afc94-125">**ยอดภาษี** – ยอดเงิน TDS ที่คํานวณได้สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="afc94-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="afc94-126">ล้างข้อมูลกล่องกาเครื่องหมาย **ทำเครื่องหมาย** สำหรับธุรกรรม TDS ใดๆ ที่ไม่ควรถูกการชำระเงินให้กับผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="afc94-127">บนแท็บ **ทั่วไป** ฟิลด์ **PAN** จะแสดงหมายเลขบัญชีถาวร (PAN) ของผู้ถูกหัก</span><span class="sxs-lookup"><span data-stu-id="afc94-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="afc94-128">ฟิลด์ **วันที่** แสดงวันที่ของการคํานวณ TDS และฟิลด์ **ค่า** แสดงเปอร์เซ็นต์รวมที่ใช้เพื่อคํานวณ TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="afc94-129">เลือก **ใบสำคัญ** เพื่อดูรายการใบสำคัญสำหรับธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="afc94-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="afc94-130">Close the page.</span></span>
10. <span data-ttu-id="afc94-131">เลือก **ส่วนประกอบภาษีหัก ณ ที่จ่าย** เพื่อเปิดหน้า **ส่วนประกอบภาษีหัก ณ ที่จ่าย** ที่ซึ่งคุณสามารถดู TDS ที่คํานวณได้ต่อส่วนประกอบภาษี TDS สำหรับรหัสภาษี TDS เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="afc94-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="afc94-132">บนแท็บ **ภาพรวม** ฟิลด์ **ส่วนประกอบภาษี** แสดงส่วนประกอบภาษี TDS ที่ใช้สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="afc94-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="afc94-133">ฟิลด์ **ยอดเงิน** แสดงยอดเงิน TDS ที่คํานวณได้สำหรับส่วนประกอบภาษี TDS ในสกุลเงินฐาน</span><span class="sxs-lookup"><span data-stu-id="afc94-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="afc94-134">ฟิลด์ **ยอดเงินสะสม** แสดงยอดเงิน TDS รวมที่คํานวณได้สำหรับส่วนประกอบภาษี TDS สำหรับธุรกรรมที่ชำระแล้วทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="afc94-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="afc94-135">บนแท็บ **ยอดเงิน** ส่วน **สกุลเงินเริ่มต้น** จะแสดงยอดเงิน TDS ที่คํานวณได้สำหรับส่วนประกอบภาษี TDS ในสกุลเงินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afc94-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="afc94-136">ส่วน **สกุลเงินรอง** แสดงยอดเงินในสกุลเงินรอง</span><span class="sxs-lookup"><span data-stu-id="afc94-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="afc94-137">ปิดหน้า **ส่วนประกอบภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="afc94-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="afc94-138">ในหน้า **การแก้ไขธุรกรรมที่เปิด** ในฟิลด์ **ยอดเงิน** ให้สังเกตว่ายอดเงินรวมที่จะชําระให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS สำหรับรอบระยะเวลาเดอะเซตเทิลเมนต์จะมีการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="afc94-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="afc94-139">เมื่อต้องการชําระธุรกรรม TDS ของรอบระยะเวลาการชําระเงิน TDS ที่แตกต่างกันให้กับผู้จัดจำหน่ายของหน่วยงาน TDS ให้เลือกกล่องกาเครื่องหมาย **ทำเครื่องหมาย** สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="afc94-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="afc94-140">ปิดหน้า **การแก้ไขธุรกรรมที่เปิดค้างไว้**</span><span class="sxs-lookup"><span data-stu-id="afc94-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="afc94-141">ถ้ามีการเลือกธุรกรรมเพียงสองสามรายการสำหรับการชําระเงินในหน้า **ธุรกรรมภาษีหัก ณ ที่จ่าย** ยอดเงิน TDS รวมของธุรกรรมที่เลือกจะมีการอัพเดตในฟิลด์ **การแก้ไข** บนหน้า **การแก้ไขธุรกรรมที่เปิดค้างไว้**</span><span class="sxs-lookup"><span data-stu-id="afc94-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="afc94-142">จะมีการอัพเดตยอดเงินที่มีการแก้ไขบนบรรทัดสมุดรายวันบนหน้า **ใบสำคัญสมุดรายวัน** และหน้า **การแก้ไขธุรกรรมที่เปิดค้างไว้** ถูกปิด</span><span class="sxs-lookup"><span data-stu-id="afc94-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="afc94-143">บนหน้า **ใบสำคัญสมุดรายวัน** ฟิลด์ **เดบิต** แสดงยอดเงินรวมที่จะชำระให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="afc94-144">ป้อนรายละเอียดบัญชีตรงข้าม</span><span class="sxs-lookup"><span data-stu-id="afc94-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="afc94-145">ถ้าธุรกรรม TDS มีหมายเลขบัญชีภาษีที่แตกต่างกัน (TAN) บรรทัดสมุดรายวันจะถูกสร้างขึ้นต่อ TAN บนหน้า **ใบสำคัญสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="afc94-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="afc94-146">บนแท็บ **ค่าธรรมเนียมการชำระเงิน** ในฟิลด์ **รหัสค่าธรรมเนียม** ให้เลือกรหัสค่าธรรมเนียมที่มีชนิดค่าธรรมเนียมเป็น **ดอกเบี้ย** หรือ **อื่นๆ** เพื่อคิดค่าธรรมเนียมการชำระเงินสำหรับการชำระเงินที่ล่าช้าซึ่งจ่ายให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="afc94-147">บนแท็บ **ข้อมูลภาษี** ในส่วน **ข้อมูลบริษัท** ฟิลด์ **ชื่อ** จะแสดงชื่อบริษัท</span><span class="sxs-lookup"><span data-stu-id="afc94-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="afc94-148">ในส่วน **ภาษีหักณ ที่จ่าย** ฟิลด์ **หมายเลขบัญชีภาษี (TAN)** แสดง TAN ที่ถูกแนบกับรายการธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="afc94-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="afc94-149">ตรวจสอบความถูกต้องและลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="afc94-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="afc94-150">เลือก **ภาษีหัก ณ ที่จ่าย \> ข้อมูล Challan** เพื่อป้อนรายละเอียด Challan สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="afc94-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="afc94-151">ฟิลด์ **ใบสำคัญ** แสดงหมายเลขใบสำคัญของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="afc94-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="afc94-152">เลือกกล่องกาเครื่องหมาย **TDS ที่ฝากโดยใช้รายการสมุด** ถ้ามีการฝากยอดเงิน TDS โดยใช้รายการสมุด</span><span class="sxs-lookup"><span data-stu-id="afc94-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="afc94-153">ในฟิลด์ **หมายเลข Challan** ให้ป้อนหมายเลข Challan ที่ใช้ในการชำระเงินให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="afc94-154">ในฟิลด์ **วันที่** ให้ป้อนวันที่ challan</span><span class="sxs-lookup"><span data-stu-id="afc94-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="afc94-155">ในฟิลด์ **ชื่อธนาคาร** ให้เลือกชื่อของธนาคารที่ควรมีการฝากยอดเงิน TDS ที่ค้างจ่ายให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="afc94-156">ฟิลด์นี้จะแสดงรายการบัญชีธนาคารทั้งหมดที่ตั้งค่าไว้ให้กับผู้จัดจำหน่ายของหน่วยงาน TDS ที่ **บัญชีเจ้าหนี้ \> ผู้จัดจำหน่ายทั้งหมด \> การตั้งค่า \> บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="afc94-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="afc94-157">ในฟิลด์ **รหัส BSR** ให้ป้อนรหัส Basic Statistical Return (BSR) ของธนาคาร</span><span class="sxs-lookup"><span data-stu-id="afc94-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="afc94-158">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="afc94-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="afc94-159">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="afc94-159">Example</span></span>

<span data-ttu-id="afc94-160">รอบระยะเวลาที่ 04/01/2009 ถูกชำระสำหรับกลุ่มส่วนประกอบ TDS ของ **การเช่า** โดยใช้กระบวนการชําระเงิน TDS ประจำงวด</span><span class="sxs-lookup"><span data-stu-id="afc94-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="afc94-161">ยอดเงิน TDS รวมของ 141,625.00 นี้ถูกลงรายการบัญชีไปยังบัญชีหน่วยงานของผู้จัดจำหน่าย TDS สำหรับรอบระยะเวลาการชําระเงิน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="afc94-162">คุณสามารถดูจํานวนเงินนี้ในฟิลด์ **ยอดเงิน** บนหน้า **การแก้ไขธุรกรรมที่เปิดค้างไว้** สำหรับผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="afc94-163">ถ้าคุณเลือก **ธุรกรรมภาษีหัก ณ ที่จ่าย** เพื่อดูธุรกรรม TDS ต่างๆ ที่ชำระแล้วสำหรับรอบระยะเวลา ข้อมูลต่อไปนี้จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="afc94-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="afc94-164">จำนวนเงิน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="afc94-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="afc94-165">16,995.00</span></span>  |
| <span data-ttu-id="afc94-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="afc94-166">22,660.00</span></span>  |
| <span data-ttu-id="afc94-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="afc94-167">28,325.00</span></span>  |
| <span data-ttu-id="afc94-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="afc94-168">16,995.00</span></span>  |
| <span data-ttu-id="afc94-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="afc94-169">28,325.00</span></span>  |
| <span data-ttu-id="afc94-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="afc94-170">16,995.00</span></span>  |
| <span data-ttu-id="afc94-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="afc94-171">11,330.00</span></span>  |

<span data-ttu-id="afc94-172">สำหรับยอดเงิน TDS เฉพาะ คุณสามารถเลือก **ส่วนประกอบภาษีหัก ณ ที่จ่าย** เพื่อดู TDS ที่คํานวณได้ต่อส่วนประกอบภาษี TDS สำหรับรหัสภาษี TDS เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="afc94-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="afc94-173">ตัวอย่างเช่น คุณเลือก **ส่วนประกอบภาษีหัก ณ ที่จ่าย** สำหรับยอดเงิน TDS 16,995.00</span><span class="sxs-lookup"><span data-stu-id="afc94-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="afc94-174">ยอดเงินภาษีที่ถูกคํานวณต่อส่วนประกอบสำหรับธุรกรรมจะถูกแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="afc94-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="afc94-175">ส่วนประกอบภาษี</span><span class="sxs-lookup"><span data-stu-id="afc94-175">Tax component</span></span> | <span data-ttu-id="afc94-176">จำนวน</span><span class="sxs-lookup"><span data-stu-id="afc94-176">Amount</span></span>    | <span data-ttu-id="afc94-177">ยอดเงินสะสม</span><span class="sxs-lookup"><span data-stu-id="afc94-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="afc94-178">TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-178">TDS</span></span>           | <span data-ttu-id="afc94-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="afc94-179">1,5000.00</span></span> | <span data-ttu-id="afc94-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="afc94-180">125,000.00</span></span>         |
| <span data-ttu-id="afc94-181">การเก็บเงินเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="afc94-181">Surcharge</span></span>     | <span data-ttu-id="afc94-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="afc94-182">1,500.00</span></span>  | <span data-ttu-id="afc94-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="afc94-183">12,500.00</span></span>          |
| <span data-ttu-id="afc94-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="afc94-184">PE-Cess</span></span>       | <span data-ttu-id="afc94-185">330.00</span><span class="sxs-lookup"><span data-stu-id="afc94-185">330.00</span></span>    | <span data-ttu-id="afc94-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="afc94-186">2,750.00</span></span>           |
| <span data-ttu-id="afc94-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="afc94-187">SHE Cess</span></span>      | <span data-ttu-id="afc94-188">165.00</span><span class="sxs-lookup"><span data-stu-id="afc94-188">165.00</span></span>    | <span data-ttu-id="afc94-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="afc94-189">1,375.00</span></span>           |

<span data-ttu-id="afc94-190">ถ้าคุณเลือกเฉพาะยอดเงิน TDS 16,995.00, 22,660.00 และ 2,8325.00 เท่านั้นสำหรับการชําระเงินบนหน้า **ธุรกรรมภาษีหัก ณ ที่จ่าย** ยอดเงินรวมสำหรับการชําระเงินจะแสดงขึ้นเป็น **67,980.00** ในฟิลด์ **การแก้ไข** ในหน้า **การแก้ไขธุรกรรมที่เปิดค้างไว้**</span><span class="sxs-lookup"><span data-stu-id="afc94-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="afc94-191">ถ้าธุรกรรมนี้ถูกทำเครื่องหมายสำหรับการชําระเงิน และหน้า **การแก้ไขธุรกรรมที่เปิดค้างไว้** ถูกปิดอยู่ จํานวนเงิน **67,980.00** จะแสดงขึ้นในฟิลด์ **เดบิต** บนหน้า **ใบสำคัญสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="afc94-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="afc94-192">ขณะนี้คุณสามารถลงรายการบัญชีสมุดรายวัน และสร้าง TDS challan</span><span class="sxs-lookup"><span data-stu-id="afc94-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="afc94-193">การปรับปรุงการชำระเงินล่วงหน้าที่จ่ายให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="afc94-194">หากต้องการปรับปรุงการชําระเงินล่วงหน้าที่จ่ายให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS เป็นการชําระเงินจริง ให้ไปที่ **บัญชีเจ้าหนี้ \> ผู้จัดจำหน่าย \> ผู้จัดจำหน่ายทั้งหมด \> การแก้ไขธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="afc94-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="afc94-195">ถ้าการชำระเงินจริงที่จ่ายเกินการชำระเงินล่วงหน้า ระบบจะสร้างหมายเลข challan สองหมายเลขขึ้นสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="afc94-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="afc94-196">อย่างไรก็ตาม ระบบจะแสดงเฉพาะหมายเลข challan แรกเท่านั้นในการสอบถาม TDS</span><span class="sxs-lookup"><span data-stu-id="afc94-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
