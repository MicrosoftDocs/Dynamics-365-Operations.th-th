---
title: ธุรกรรมภาษีหัก ณ ที่จ่าย ในการขาย
description: หัวข้อนี้แสดงรายการขั้นตอนเพื่อหลีกเลี่ยงการคํานวณภาษีหัก ณ ที่จ่ายของลูกค้าที่เลือก สำหรับลูกค้าที่ระบุภาษีหัก ณ ที่จ่ายในการชำระเงินให้คุณ คุณสามารถกําหนดกลุ่มภาษีหัก ณ ที่จ่ายเริ่มต้นได้
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
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060801"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="cf868-104">ธุรกรรมภาษีหัก ณ ที่จ่าย ในการขาย</span><span class="sxs-lookup"><span data-stu-id="cf868-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="cf868-105">หัวข้อนี้แสดงรายการขั้นตอนเพื่อหลีกเลี่ยงการคํานวณภาษีหัก ณ ที่จ่ายของลูกค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cf868-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="cf868-106">สำหรับลูกค้าที่ระบุภาษีหัก ณ ที่จ่ายในการชำระเงินให้คุณ คุณสามารถกําหนด **กลุ่มภาษีหัก ณ ที่จ่าย** บนหน้า **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="cf868-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="cf868-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="cf868-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="cf868-108">คลิกรหัสลูกค้าที่เกี่ยวข้อง ให้คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="cf868-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="cf868-109">ในแท็บ **ใบแจ้งหนี้และการจัดส่ง** ให้ตั้งค่าฟิลด์ **คํานวณภาษีหัก ณ ที่จ่าย** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cf868-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="cf868-110">จะไม่คํานวณภาษีหัก ณ ที่จ่ายถ้าไม่ได้สลับ **การคํานวณภาษีหัก ณ ที่จ่าย** กับลูกค้ารายนี้ในข้อมูลหลัก</span><span class="sxs-lookup"><span data-stu-id="cf868-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="cf868-111">เลือกกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าใน **กลุ่มภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="cf868-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="cf868-112">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cf868-112">Click **Save**.</span></span>

<span data-ttu-id="cf868-113">ดูสินค้า/บริการที่ต้องเสียภาษีหัก ณ ที่จ่าย คุณสามารถกําหนด **กลุ่มภาษีหัก ณ ที่จ่ายตามสินค้า** เริ่มต้น **ในผลิตภัณฑ์ที่ออกใช้แล้ว** ได้</span><span class="sxs-lookup"><span data-stu-id="cf868-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="cf868-114">ไปยัง **บานหน้าต่างนำทาง > โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="cf868-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="cf868-115">คลิกหมายเลขสินค้าที่เกี่ยวข้อง ให้คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="cf868-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="cf868-116">ในแท็บ **ขาย** ให้คลิก **คํานวณภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="cf868-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="cf868-117">ระบบจะไม่คํานวณภาษีหัก ณ ที่จ่าย ถ้าไม่มีการตั้งค่า **คํานวณภาษีหัก ณ ที่จ่าย** เป็น **ใช่** ให้กับสินค้านี้บนแท็บ **ผลิตภัณฑ์ที่ออกใช้แล้ว** ในหน้า **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="cf868-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="cf868-118">เลือกกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าในรายการ **กลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้า**</span><span class="sxs-lookup"><span data-stu-id="cf868-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="cf868-119">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="cf868-119">Click **Save**.</span></span>

<span data-ttu-id="cf868-120">คุณสามารถมอบหมายกลุ่มภาษีหัก ณ ที่จ่ายและกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าได้โดยใช้หน้า **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="cf868-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="cf868-121">กลุ่มภาษีหัก ณ ที่จ่ายเริ่มต้นและกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าจะถูกใช้เป็นรายการเริ่มต้นในบรรทัดใบสั่งขาย เมื่อคุณสร้างใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="cf868-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="cf868-122">การคํานวณภาษีหัก ณ ที่จ่ายและลงรายการบัญชีโดยใช้ **สมุดรายวันการจ่ายของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="cf868-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="cf868-123">คุณสามารถปรับปรุงรหัสภาษีหัก ณ ที่จ่ายที่ใช้ได้ด้วยตนเอง รวมทั้งยอดภาษีหัก ณ ที่จ่ายจริงบนแท็บ **ภาษีหัก ณ ที่จ่าย** บนหน้า **ชำระเงินธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="cf868-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="cf868-124">จํานวนเงินภาษีหัก ณ ที่จ่ายที่คํานวณได้จะถูกหักออกจากการจ่ายของลูกค้า และลงรายการบัญชีที่บัญชี **การชดเชยภาษีหัก ณ ที่จ่าย** ในใบแจ้งนี้</span><span class="sxs-lookup"><span data-stu-id="cf868-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>
