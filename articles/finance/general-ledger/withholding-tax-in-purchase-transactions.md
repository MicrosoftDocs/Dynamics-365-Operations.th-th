---
title: ธุรกรรมภาษีหัก ณ ที่จ่าย ในการซื้อ
description: สำหรับผู้จัดจำหน่ายที่เสียภาษีหัก ณ ที่จ่าย คุณสามารถกําหนด **กลุ่มภาษีหัก ณ ที่จ่าย** บนหน้า **ผู้จัดจำหน่ายทั้งหมด**
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 06997e2d6b47d867e014a7d493d91015c78a5e04
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060799"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="7771d-103">ธุรกรรมภาษีหัก ณ ที่จ่าย ในการซื้อ</span><span class="sxs-lookup"><span data-stu-id="7771d-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="7771d-104">สำหรับผู้จัดจำหน่ายที่เสียภาษีหัก ณ ที่จ่าย คุณสามารถกําหนด **กลุ่มภาษีหัก ณ ที่จ่าย** บนหน้า **ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7771d-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="7771d-105">ไปที่ **บานหน้าต่างการนำทาง > โมดูล > บัญชีเจ้าหนี้ > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7771d-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="7771d-106">คลิกรหัสผู้จัดจำหน่ายที่เกี่ยวข้อง ให้คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="7771d-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="7771d-107">ในแท็บ **ใบแจ้งหนี้และการจัดส่ง** ให้ตั้งค่าฟิลด์ **คํานวณภาษีหัก ณ ที่จ่าย** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7771d-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="7771d-108">จะไม่คํานวณภาษีหัก ณ ที่จ่ายถ้าไม่ได้สลับ **การคํานวณภาษีหัก ณ ที่จ่าย** กับผู้จัดจำหน่ายรายนี้ในข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7771d-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="7771d-109">เลือกกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าใน **กลุ่มภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="7771d-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="7771d-110">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7771d-110">Click **Save**.</span></span>

<span data-ttu-id="7771d-111">ดูสินค้า/บริการที่ต้องเสียภาษีหัก ณ ที่จ่าย คุณสามารถกําหนด **กลุ่มภาษีหัก ณ ที่จ่ายตามสินค้า** เริ่มต้น **ในผลิตภัณฑ์ที่ออกใช้แล้ว** ได้</span><span class="sxs-lookup"><span data-stu-id="7771d-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="7771d-112">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="7771d-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="7771d-113">คลิกหมายเลขสินค้าที่เกี่ยวข้อง ให้คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="7771d-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="7771d-114">ในแท็บ **ซื้อ** ให้คลิก **คํานวณภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="7771d-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="7771d-115">ระบบจะไม่คํานวณภาษีหัก ณ ที่จ่าย ถ้าไม่มีการตั้งค่า **คํานวณภาษีหัก ณ ที่จ่าย** เป็น **ใช่** ให้กับสินค้านี้บนแท็บ **ซื้อ** ในหน้า **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="7771d-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="7771d-116">เลือกกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าในรายการ **กลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้า**</span><span class="sxs-lookup"><span data-stu-id="7771d-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="7771d-117">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7771d-117">Click **Save**.</span></span>

<span data-ttu-id="7771d-118">คุณสามารถมอบหมายกลุ่มภาษีหัก ณ ที่จ่ายและกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าได้ในหน้า:</span><span class="sxs-lookup"><span data-stu-id="7771d-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="7771d-119">**ใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="7771d-119">**Purchase order**</span></span>
- <span data-ttu-id="7771d-120">**ใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="7771d-120">**Vendor invoice**</span></span>
- <span data-ttu-id="7771d-121">**สมุดรายวันใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="7771d-121">**Invoice journal**</span></span>

<span data-ttu-id="7771d-122">กลุ่มภาษีหัก ณ ที่จ่ายเริ่มต้นและกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าจะถูกยกยอดไปหัก ณ ที่จ่ายในบรรทัดต่างๆ เมื่อสร้าง **ใบสั่งซื้อ** และ/หรือ **ใบแจ้งหนี้ผู้จัดจำหน่ายที่กำลังดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="7771d-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="7771d-123">สำหรับ **สมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่าย** คุณสามารถสลับไปที่ **คํานวณภาษีหัก ณ ที่จ่าย** และเลือก **กลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้า** ในแท็บ **ทั่วไป** ในสมุดรายวันได้</span><span class="sxs-lookup"><span data-stu-id="7771d-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="7771d-124">ยอดเงินชั่วคราวของภาษีหัก ณ ที่จ่ายจะพร้อมใช้งานในฟิลด์ **ภาษีหัก ณ ที่จ่ายที่ปรับแล้ว** ของแท็บ **รวม** บนหน้า **ใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="7771d-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![รวมภาษีหัก ณ ที่จ่ายรวมอยู่ในใบสั่งซื้อ](media/withholding-tax-adjusted.png)

<span data-ttu-id="7771d-126">ภาษีหัก ณ ที่จ่ายคำนวณบน **สมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="7771d-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="7771d-127">คุณสามารถปรับปรุงรหัสภาษีหัก ณ ที่จ่ายที่ใช้ได้ด้วยตนเอง รวมทั้งยอดภาษีหัก ณ ที่จ่ายจริงบนแท็บ **ภาษีหัก ณ ที่จ่าย** บนหน้า **ชำระเงินธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="7771d-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![คุณสามารถปรับปรุงการหัก ณ ที่จ่ายด้วยตนเองได้ในหน้าชำระเงินธุรกรรม](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="7771d-129">จํานวนเงินภาษีหัก ณ ที่จ่ายที่ได้รับมาจะถูกหักออกจากการจ่ายของผู้จัดจำหน่าย และลงรายการบัญชีที่ **บัญชีภาษีหัก ณ ที่จ่าย** ในใบแจ้งนี้</span><span class="sxs-lookup"><span data-stu-id="7771d-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![บัญชีภาษีหัก ณ ที่จ่ายที่แสดงใบสำคัญที่เกี่ยวข้อง](media/withholding-tax-adjusted.png)
