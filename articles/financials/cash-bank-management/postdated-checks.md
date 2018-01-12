---
title: "เช็คลงวันที่ล่วงหน้า"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับการสนับสนุนสำหรับเช็คลงวันที่ล่วงหน้าใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition เช็คลงวันที่ล่วงหน้าเป็นเช็คที่ถูกออก เพื่อทำและรับการชำระเงินในวันที่ในอนาคต  ดังนั้นจึงไม่สามารถจ่ายเช็คได้จนกว่าถึงวันที่ระบุ"
author: twheeloc
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: 68d3029f750e2f2feb5912bbb64bfe105b9d9718
ms.contentlocale: th-th
ms.lasthandoff: 01/12/2018

---

# <a name="postdated-checks"></a><span data-ttu-id="5c0a9-105">เช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="5c0a9-105">Postdated checks</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5c0a9-106">บทความนี้แสดงข้อมูลเกี่ยวกับการสนับสนุนสำหรับเช็คลงวันที่ล่วงหน้าใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="5c0a9-106">This article provides information about support for postdated checks in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="5c0a9-107">เช็คลงวันที่ล่วงหน้าเป็นเช็คที่ถูกออก เพื่อทำและรับการชำระเงินในวันที่ในอนาคต </span><span class="sxs-lookup"><span data-stu-id="5c0a9-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="5c0a9-108">ดังนั้นจึงไม่สามารถจ่ายเช็คได้จนกว่าถึงวันที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5c0a9-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="5c0a9-109">Microsoft Dynamics 365 for Finance and Operations สนับสนุนวงจรการจัดการแบบเต็มสำหรับเช็คลงวันที่ล่วงหน้าทั้งในบัญชีลูกหนี้และบัญชีเจ้าหนี้ ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5c0a9-109">Microsoft Dynamics 365 for Finance and Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c0a9-110">สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="5c0a9-110">Scenario</span></span></th>
<th><span data-ttu-id="5c0a9-111">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="5c0a9-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c0a9-112">ตั้งค่าเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="5c0a9-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="5c0a9-113">คุณต้องตั้งค่าวิธีการชำระเงินใหม่ และระบุชุดคำสั่งการชำระเงิน สำหรับการล้างข้อมูลบัญชีสำหรับเช็คที่ออก เช็คที่ได้รับ และภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="5c0a9-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0a9-114">ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าที่สำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5c0a9-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="5c0a9-115">ลงทะเบียนรายละเอียดเกี่ยวกับเช็คลงวันที่ล่วงหน้าที่คุณออกให้กับผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="5c0a9-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="5c0a9-116">เมื่อมีการลงรายการบัญชีการชำระเงิน หนี้สินของผู้จัดจำหน่ายมีการรับรู้ แต่บัญชีธนาคารยังไม่ได้ลงเครดิต </span><span class="sxs-lookup"><span data-stu-id="5c0a9-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="5c0a9-117">บัญชีระหว่างโอนจึงใช้สำหรับวัตถุประสงค์นี้ลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="5c0a9-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0a9-118">ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="5c0a9-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="5c0a9-119">ลงทะเบียนรายละเอียดของเช็คลงวันที่ล่วงหน้าที่คุณได้รับจากลูกค้า </span><span class="sxs-lookup"><span data-stu-id="5c0a9-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="5c0a9-120">เมื่อมีการลงรายการบัญชีการชำระเงิน หนี้ของลูกค้าเป็นเครดิต แต่บัญชีธนาคารยังไม่ได้ถูกเดบิต </span><span class="sxs-lookup"><span data-stu-id="5c0a9-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="5c0a9-121">บัญชีระหว่างโอนจึงใช้สำหรับวัตถุประสงค์นี้ลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="5c0a9-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0a9-122">ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าทดแทน สำหรับลูกค้าหรือผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5c0a9-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="5c0a9-123">ถ้าเช็คฉบับเดิมของคุณที่จ่ายให้ผู้จัดจำหน่ายหรือจากลูกค้า สูญหายหรือเสียหาย คุณสามารถออกเช็คลงวันที่ล่วงหน้าฉบับใหม่ได้ </span><span class="sxs-lookup"><span data-stu-id="5c0a9-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="5c0a9-124">เมื่อคุณลงทะเบียนรายละเอียดเช็ค จะให้การอ้างอิงถึงเช็คฉบับเดิมและระบุว่าเช็คใหม่เป็นฉบับทดแทนฉบับเดิม</span><span class="sxs-lookup"><span data-stu-id="5c0a9-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="5c0a9-125">คุณยังสามารถลงรายการบัญชีเช็คใหม่ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="5c0a9-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0a9-126">โอนเช็คลงวันที่ล่วงหน้าของลูกค้าให้กับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5c0a9-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="5c0a9-127">เมื่อคุณได้รับเช็คลงวันที่ล่วงหน้าจากลูกค้า คุณสามารถโอนย้ายเช็คนั้นไปยังผู้จัดจำหน่ายให้เป็นการชำระเงินได้</span><span class="sxs-lookup"><span data-stu-id="5c0a9-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0a9-128">ชำระเช็คลงวันที่ล่วงหน้าสำหรับลูกค้าหรือผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5c0a9-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="5c0a9-129">ชำระเช็คลงวันที่ล่วงหน้าที่ถูกลงรายการบัญชีไปยังบัญชีระหว่างกาล สำหรับลูกค้าหรือผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="5c0a9-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="5c0a9-130">เมื่อเช็คเติบโตเต็มที่ในตอนสุดท้าย เมื่อมีการชำระเช็ค ธนาคารจะถูกเดบิตหรือเครดิตในตอนท้าย เทียบกับบัญชีระหว่างโอนที่ถูกใช้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="5c0a9-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c0a9-131">ยกเลิกเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5c0a9-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="5c0a9-132">คุณสามารถยกเลิกเช็คลงวันที่ล่วงหน้าที่ลงรายการบัญชีได้ในสถานการณ์เหล่านี้: - เช็คถูกตีกลับโดยธนาคาร</span><span class="sxs-lookup"><span data-stu-id="5c0a9-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="5c0a9-133">- มีการใช้เช็คกับใบแจ้งหนี้ที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5c0a9-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="5c0a9-134">- มีการชำระเงินสดแทนเช็ค</span><span class="sxs-lookup"><span data-stu-id="5c0a9-134">- A cash payment is made against the check.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c0a9-135">หยุดการชำระเงินสำหรับเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="5c0a9-135">Stop payment for a postdated check</span></span></td>
<td><span data-ttu-id="5c0a9-136">คุณสามารถหยุดการชำระเงินในเช็คลงวันที่ล่วงหน้า ที่ถูกออกให้แก่ผู้จัดจำหน่าย ด้วยเหตุผลเช่น เงินในบัญชีไม่เพียงพอ การเปลี่ยนแปลงเงื่อนไขของข้อตกลงกับผู้จัดจำหน่าย จัดส่งสินค้าที่มีข้อบกพร่องโดยผู้จัดจำหน่าย หรือส่งคืนสินค้าให้แก่ผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="5c0a9-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="5c0a9-137">คุณสามารถหยุดการชำระเงินได้เฉพาะในเช็คที่ยังไม่ได้ขึ้นเงินเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5c0a9-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
</tr>
</tbody>
</table>



<span data-ttu-id="5c0a9-138">สำหรับข้อมูลเพิ่มเติม ให้ดูที่หัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5c0a9-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="5c0a9-139">ตั้งค่าเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="5c0a9-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="5c0a9-140">ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="5c0a9-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="5c0a9-141">ชำระเช็คลงวันที่ล่วงหน้าจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="5c0a9-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="5c0a9-142">ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5c0a9-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="5c0a9-143">ชำระเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="5c0a9-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)




