---
title: การคํานวณ TDS ในใบแจ้งหนี้จากหน้าใบแจ้งหนี้ข้อความอิสระ
description: หัวข้อนี้อธิบายวิธีการคํานวณภาษีที่หักที่ต้นทาง (TDS) ในใบแจ้งหนี้โดยใช้หน้าใบแจ้งหนี้ข้อความอิสระ
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023634"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="bc916-103">การคํานวณ TDS ในใบแจ้งหนี้จากหน้าใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="bc916-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc916-104">หัวข้อนี้อธิบายวิธีการคํานวณภาษีที่หักที่ต้นทาง (TDS) ในใบแจ้งหนี้โดยใช้หน้า **ใบแจ้งหนี้ข้อความอิสระ**</span><span class="sxs-lookup"><span data-stu-id="bc916-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="bc916-105">ไปที่ **บัญชีลูกหนี้ \> ใบแจ้งหนี้ \> ใบแจ้งหนี้ข้อความอิสระทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="bc916-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="bc916-106">[![หน้าใบแจ้งหนี้ข้อความอิสระ](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="bc916-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="bc916-107">เลือก **ใหม่** เพี่อสร้างใบแจ้งหนี้ข้อความอิสระ และป้อนข้อมูลที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="bc916-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="bc916-108">เลือกแท็บ **ใบแจ้งหนี้** ในส่วน **กลุ่มภาษีหัก ณ ที่จ่าย** ฟิลด์ **ลักษณะของผู้ถูกประเมิน** แสดงประเภทลักษณะของผู้ถูกประเมินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="bc916-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="bc916-109">ในฟิลด์ **กลุ่ม TDS** ให้ตรวจสอบหรือเปลี่ยนแปลงกลุ่ม TDS เริ่มต้นที่ถูกกําหนดไว้สำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="bc916-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bc916-110">เมื่อคุณเลือกค่าในฟิลด์ **กลุ่ม TCS** ฟิลด์ **กลุ่ม TDS** จะไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bc916-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="bc916-111">TDS จะถูกคํานวณเฉพาะเมื่อตัวเลือก **คํานวณภาษีหัก ณ ที่จ่าย** ถูกตั้งค่าเป็น **ใช่** สำหรับลูกค้าในหน้า **ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="bc916-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="bc916-112">บนแท็บ **ข้อมูลภาษี** ในส่วน **ข้อมูลบริษัท** ในฟิลด์ **ชื่อ** ให้เลือกชื่อบริษัทของที่อยู่อื่นที่ถูกตั้งค่าไว้สำหรับบริษัท</span><span class="sxs-lookup"><span data-stu-id="bc916-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="bc916-113">ในส่วน **ภาษีหัก ณ ที่จ่าย** ฟิลด์ **หมายเลขบัญชีภาษี (TAN)** แสดงหมายเลขบัญชีภาษี (TAN) สำหรับบริษัทที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bc916-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="bc916-114">บนแท็บ **รายการใบแจ้งหนี้** สร้างรายการใบแจ้งหนี้ และป้อนรายละเอียดที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="bc916-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="bc916-115">ในส่วน **กลุ่มภาษีหัก ณ ที่จ่าย** ฟิลด์ **หมายเลขบัญชีภาษี (TAN)** แสดง TAN และฟิลด์ **กลุ่ม TDS** แสดงกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="bc916-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="bc916-116">เลือก **ภาษีหัก ณ ที่จ่าย** เพื่อเปิดหน้า **ธุรกรรมภาษีหัก ณ ที่จ่าย ชั่วคราว**</span><span class="sxs-lookup"><span data-stu-id="bc916-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="bc916-117">ส่วนบนของหน้านี้จะมีฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bc916-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="bc916-118">**ยอดรวมภาษีหัก ณ ที่จ่าย** – TDS รวมที่ถูกคํานวณสำหรับธุรกรรมสำหรับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="bc916-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="bc916-119">**ค่า** – เปอร์เซ็นต์รวมที่ถูกใช้ในการคํานวณ TDS สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="bc916-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="bc916-120">เปอร์เซ็นต์รวมจะขึ้นอยู่กับสูตรที่กําหนดให้สำหรับรหัสภาษี TDS และแนบกับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="bc916-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="bc916-121">**ยอดรวมภาษีหัก ณ ที่จ่ายที่ปรับปรุง** – ยอดรวม TDS ที่ปรับปรุงสำหรับรหัสภาษีทั้งหมดในกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="bc916-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="bc916-122">**TDS** – กล่องกาเครื่องหมายที่เลือกบ่งชี้ว่ากลุ่ม TDS ถูกแนบอยู่กับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="bc916-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="bc916-123">ฟิลด์บนแท็บ **ภาพรวม**, **ทั่วไป** และ **การปรับปรุง** แสดงจำนวน TDS ที่คํานวณได้และรายละเอียดของจำนวน TDS ที่ปรับปรุง สำหรับรหัสภาษี TDS แต่ละรหัสที่แนบกับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="bc916-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="bc916-124">เลือก **ขีดจํากัด** เพื่อเปิดหน้า **ขีดจํากัด** ซึ่งคุณสามารถตรวจสอบขีดจํากัดที่กําหนดไว้สำหรับส่วนประกอบภาษี TDS ที่ถูกแนบกับรหัสภาษี TDS เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="bc916-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="bc916-125">เลือก **โปรแกรมออกแบบสูตร** เพื่อเปิดหน้า **โปรแกรมออกแบบสูตร** ซึ่งคุณสามารถตรวจทานสูตรที่กําหนดไว้สำหรับรหัสภาษี TDS เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="bc916-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="bc916-126">ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="bc916-126">Post the free text invoice.</span></span> <span data-ttu-id="bc916-127">ยอดเงิน TDS ที่ถูกคํานวณสำหรับใบแจ้งหนี้ข้อความอิสระ จะมีการลงรายการบัญชีไปยังบัญชีลูกหนี้ที่กําหนดไว้สำหรับรหัสภาษี TDS แต่ละรหัสในกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="bc916-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="bc916-128">บัญชีลูกหนี้สำหรับรหัสภาษี TDS ถูกกําหนดในหน้า **รหัสภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="bc916-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="bc916-129">เลือก **ภาษีหัก ณ ที่จ่ายที่ลงรายการบัญชี** เพื่อเปิดหน้า **ธุรกรรมภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="bc916-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="bc916-130">ฟิลด์ **ค่า** แสดงเปอร์เซ็นต์รวมที่ถูกใช้ในการคํานวณ TDS สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="bc916-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="bc916-131">ฟิลด์บนแท็บ **ภาพรวม** **ทั่วไป** และ **ยอดเงิน** แสดงยอดเงิน TDS ที่ถูกคํานวณบนรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bc916-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="bc916-132">ตรวจสอบข้อมูลการคํานวณ TDS สำหรับรหัสภาษี TDS แต่ละรหัสที่ถูกแนบกับกลุ่ม TDS</span><span class="sxs-lookup"><span data-stu-id="bc916-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
