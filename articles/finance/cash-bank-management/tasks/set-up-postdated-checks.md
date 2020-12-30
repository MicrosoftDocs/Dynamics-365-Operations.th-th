---
title: ตั้งค่าเช็คลงวันที่ล่วงหน้า
description: 'หัวข้อนี้อธิบายวิธีการระบุว่าจะลงรายการบัญชีรายการสมุดรายวันสำหรับเช็คลงวันที่ล่วงหน้าหรือไม่ และระบุสมุดรายวันการลงรายการบัญชีที่จะใช้สำหรับรายการหักบัญชีและการชำระเงินของผู้จัดจำหน่าย '
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22e67aa051b5ea8267df7efac40e007d0f11a83d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448476"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="34bc0-103">ตั้งค่าเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="34bc0-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34bc0-104">หัวข้อนี้อธิบายวิธีการระบุว่าจะลงรายการบัญชีรายการสมุดรายวันสำหรับเช็คลงวันที่ล่วงหน้าหรือไม่ และระบุสมุดรายวันการลงรายการบัญชีที่จะใช้สำหรับรายการหักบัญชีและการชำระเงินของผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="34bc0-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="34bc0-105">คุณยังสามารถระบุบัญชีรอการโอนสำหรับเช็คที่ออก เช็คที่ได้รับ และภาษีหัก ณ ที่จ่าย </span><span class="sxs-lookup"><span data-stu-id="34bc0-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="34bc0-106">เช็คลงวันที่ล่วงหน้าซึ่งได้ถูกออกเพื่อชำระเงินและเพื่อรับเงินที่ชำระในอนาคต </span><span class="sxs-lookup"><span data-stu-id="34bc0-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="34bc0-107">คุณสามารถระบุได้ว่าเช็คต้องถูกสะท้อนในสมุดบัญชีก่อนวันครบกำหนดหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="34bc0-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="34bc0-108">บทบาทของกระบวนงานนี้คือเจ้าหน้าที่ฝ่ายบริหารเงิน </span><span class="sxs-lookup"><span data-stu-id="34bc0-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="34bc0-109">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="34bc0-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="34bc0-110">ตั้งค่าเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="34bc0-110">Set up postdated checks</span></span>
1. <span data-ttu-id="34bc0-111">ไปที่การจัดการเงินสดและธนาคาร > การตั้งค่า > พารามิเตอร์การจัดการเงินสดและธนาคาร</span><span class="sxs-lookup"><span data-stu-id="34bc0-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="34bc0-112">คลิกแท็บเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="34bc0-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="34bc0-113">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายการเปิดใช้งานเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="34bc0-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="34bc0-114">เลือกหรือยกเลิกรายการสมุดรายวัน สำหรับกล่องกาเครื่องหมายเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="34bc0-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="34bc0-115">ในบัญชีระหว่างโอนสำหรับเช็คที่ออก ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="34bc0-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="34bc0-116">ในบัญชีระหว่างโอนสำหรับเช็คที่ได้รับ ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="34bc0-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="34bc0-117">ในสมุดรายวันทั่วไปสำหรับฟิลด์รายการหักบัญชี ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="34bc0-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="34bc0-118">ในฟิลด์การโอนย้ายเช็คลงวันที่ล่วงหน้าไปที่สมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่ายนี้ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="34bc0-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="34bc0-119">ในฟิลด์บัญชีระหว่างโอนภาษีหัก ณ ที่จ่าย ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="34bc0-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="34bc0-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="34bc0-120">Click Save.</span></span>
11. <span data-ttu-id="34bc0-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="34bc0-121">Close the page.</span></span>
12. <span data-ttu-id="34bc0-122">ไปที่บัญชีเจ้าหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="34bc0-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="34bc0-123">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="34bc0-123">Click New.</span></span>
14. <span data-ttu-id="34bc0-124">ในฟิลด์วิธีการชำระเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="34bc0-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="34bc0-125">เลือกตัวเลือกการลงรายการบัญชีระหว่างโอนเช็คลงวันที่ล่วงหน้า เพื่อระบุว่ายอดเช็คจะถูกลงรายการบัญชีไปที่บัญชีระหว่างโอน</span><span class="sxs-lookup"><span data-stu-id="34bc0-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="34bc0-126">ในประเภทบัญชี เลือก 'ธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="34bc0-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="34bc0-127">บัญชีตรงข้ามของวิธีการชำระเงินจะเป็นธนาคาร</span><span class="sxs-lookup"><span data-stu-id="34bc0-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="34bc0-128">ในฟิลด์บัญชีบัญชีการชำระเงิน ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="34bc0-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="34bc0-129">เลือกบัญชีธนาคารที่ใช้ในการหักลบยอดเงินใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="34bc0-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="34bc0-130">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="34bc0-130">Click Save.</span></span>
19. <span data-ttu-id="34bc0-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="34bc0-131">Close the page.</span></span>

