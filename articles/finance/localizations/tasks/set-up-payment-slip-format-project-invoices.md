---
title: ตั้งค่ารูปแบบการบันทึกการชำระเงินสำหรับใบแจ้งหนี้โครงการ
description: ธุรกิจมักจะแนบบันทึกการชำระเงินที่ถูกพิมพ์ เพื่อออกใบแจ้งหนี้เพื่อช่วยเหลือลูกค้าและให้ข้อมูลอ้างอิงการชำระเงินสำหรับการชำระเงินและการลงรายการบัญชี
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2bcbf19ef78c521a426573ea4317c5a0e9e2cb3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214455"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a><span data-ttu-id="c6cbe-103">ตั้งค่ารูปแบบการบันทึกการชำระเงินสำหรับใบแจ้งหนี้โครงการ</span><span class="sxs-lookup"><span data-stu-id="c6cbe-103">Set up payment slip format for project invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6cbe-104">ธุรกิจมักจะแนบบันทึกการชำระเงินที่ถูกพิมพ์ เพื่อออกใบแจ้งหนี้เพื่อช่วยเหลือลูกค้าและให้ข้อมูลอ้างอิงการชำระเงินสำหรับการชำระเงินและการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cbe-104">Businesses commonly attach printed payment slips to invoices to assist customers and provide a payment reference for posting and settlement.</span></span> <span data-ttu-id="c6cbe-105">บันทึกการชำระเงินสามารถใช้สำหรับใบแจ้งหนี้ของโครงการหรือของการบริการ จดหมายเรียกเก็บเงิน ดอกเบี้ยตั๋วเงิน และรายการบัญชี นอกเหนือจากใบแจ้งหนี้การขายและใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="c6cbe-105">The payment slip can be used for project or service invoices, collection letters, interest notes, and account statements, in addition to sales invoices and free text invoices.</span></span> <span data-ttu-id="c6cbe-106">ในการประมวลผลบันทึกการชำระเงิน อันดับแรกให้ตั้งค่าหมายเลขรหัสประจำตัวเจ้าหนี้และรูปแบบการแนบบันทึกการชำระเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="c6cbe-106">To process payment slips, first set up your creditor identification number and payment slip attachment formats.</span></span>

<span data-ttu-id="c6cbe-107">กระบวนงานนี้ใช้บริษัทสาธิต DEMF</span><span class="sxs-lookup"><span data-stu-id="c6cbe-107">This procedure uses the DEMF demo company.</span></span> 

<span data-ttu-id="c6cbe-108">ฟังก์ชันนี้จะพร้อมใช้งานสำหรับนิติบุคคลที่มีที่อยู่หลักอยู่ในเดนมาร์ก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-108">This functionality is available for legal entities whose primary address is in Denmark.</span></span>


## <a name="set-up-a-creditor-id-number"></a><span data-ttu-id="c6cbe-109">ตั้งค่าหมายเลขรหัสของเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="c6cbe-109">Set up a creditor ID number</span></span>
1. <span data-ttu-id="c6cbe-110">ไปที่การจัดการองค์กร > องค์กร > นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="c6cbe-110">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="c6cbe-111">ขยายหรือยุบส่วนของข้อมูลบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="c6cbe-111">Expand or collapse the Bank account information section.</span></span>
3. <span data-ttu-id="c6cbe-112">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="c6cbe-112">Click Edit.</span></span>
4. <span data-ttu-id="c6cbe-113">ในฟิลด์รหัส Fi-creditor ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c6cbe-113">In the FI-Creditor ID field, type a value.</span></span>
5. <span data-ttu-id="c6cbe-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-114">Click Save.</span></span>
6. <span data-ttu-id="c6cbe-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c6cbe-115">Close the page.</span></span>

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a><span data-ttu-id="c6cbe-116">ตั้งค่ารูปแบบบันทึกการชำระเงินสำหรับใบแจ้งหนี้, บันทึก, จดหมาย, และใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="c6cbe-116">Set up a payment slip format for invoices, notes, letters, and statements</span></span>
1. <span data-ttu-id="c6cbe-117">ไปที่บัญชีลูกหนี้ > การตั้งค่า > แบบฟอร์ม > การตั้งค่าแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="c6cbe-117">Go to Accounts receivable > Setup > Forms > Form setup.</span></span>
2. <span data-ttu-id="c6cbe-118">คลิกแท็บใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c6cbe-118">Click the Invoice tab.</span></span>
3. <span data-ttu-id="c6cbe-119">ในฟิลด์เอกสารแนบการชำระเงินที่เกี่ยวข้องในใบแจ้งหนี้ของลูกค้า ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-119">In the Associated payment attachment on customer invoice field, select an option.</span></span>
    * <span data-ttu-id="c6cbe-120">ไม่มี - ห้ามพิมพ์บันทึกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cbe-120">None – Do not print a payment slip.</span></span> <span data-ttu-id="c6cbe-121">เลือกตัวเลือกนี้เมื่อยอดการชำระเงินอยู่ในสกุลเงินอื่นนอกเหนือจากโครเนอร์เดนมาร์ก (DKK)</span><span class="sxs-lookup"><span data-stu-id="c6cbe-121">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="c6cbe-122">FIK 751 - พิมพ์บันทึกการชำระเงิน FIK 751 ถ้าคุณต้องการเขียนยอดการชำระเงินและวันที่ครบกำหนดในบันทึกการชำระเงินด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c6cbe-122">FIK 751 – Print an FIK 751 payment slip if you intend to manually write the payment amount and due date on the payment slip.</span></span>   <span data-ttu-id="c6cbe-123">FIK 752 - พิมพ์บันทึกการชำระเงิน FIK 752 ถ้าคุณต้องการใช้ บันทึกการชำระเงินที่ถูกสร้างขึ้นโดยคอมพิวเตอร์ซึ่งมียอดการชำระเงินที่พิมพ์ล่วงหน้าและวันครบกำหนดชำระ</span><span class="sxs-lookup"><span data-stu-id="c6cbe-123">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
4. <span data-ttu-id="c6cbe-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-124">Click Save.</span></span>
5. <span data-ttu-id="c6cbe-125">คลิกแท็บใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="c6cbe-125">Click the Free text invoice tab.</span></span>
6. <span data-ttu-id="c6cbe-126">ในฟิลด์เอกสารแนบการชำระเงินที่เกี่ยวข้องในใบแจ้งหนี้ข้อความอิสระ ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-126">In the Associated payment attachment on free text invoice field, select an option.</span></span>
    * <span data-ttu-id="c6cbe-127">ไม่มี - ห้ามพิมพ์บันทึกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cbe-127">None – Do not print a payment slip.</span></span> <span data-ttu-id="c6cbe-128">เลือกตัวเลือกนี้เมื่อยอดการชำระเงินอยู่ในสกุลเงินอื่นนอกเหนือจากโครเนอร์เดนมาร์ก (DKK)</span><span class="sxs-lookup"><span data-stu-id="c6cbe-128">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="c6cbe-129">FIK 751 - พิมพ์บันทึกการชำระเงิน FIK 751 ถ้าคุณต้องการเขียนยอดการชำระเงินและวันครบกำหนดในบันทึกการชำระเงินด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="c6cbe-129">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="c6cbe-130">FIK 752 - พิมพ์บันทึกการชำระเงิน FIK 752 ถ้าคุณต้องการใช้ บันทึกการชำระเงินที่ถูกสร้างขึ้นโดยคอมพิวเตอร์ซึ่งมียอดการชำระเงินที่พิมพ์ล่วงหน้าและวันครบกำหนดชำระ</span><span class="sxs-lookup"><span data-stu-id="c6cbe-130">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
7. <span data-ttu-id="c6cbe-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-131">Click Save.</span></span>
8. <span data-ttu-id="c6cbe-132">คลิกแท็บดอกเบี้ยตั๋วเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cbe-132">Click the Interest note tab.</span></span>
9. <span data-ttu-id="c6cbe-133">ในฟิลด์เอกสารแนบการชำระเงินที่เกี่ยวข้องในดอกเบี้ยตั๋วเงิน ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-133">In the Associated payment attachment on interest note field, select an option.</span></span>
    * <span data-ttu-id="c6cbe-134">ไม่มี - ห้ามพิมพ์บันทึกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cbe-134">None – Do not print a payment slip.</span></span> <span data-ttu-id="c6cbe-135">เลือกตัวเลือกนี้เมื่อยอดการชำระเงินอยู่ในสกุลเงินอื่นนอกเหนือจากโครเนอร์เดนมาร์ก (DKK)</span><span class="sxs-lookup"><span data-stu-id="c6cbe-135">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="c6cbe-136">FIK 751 - พิมพ์บันทึกการชำระเงิน FIK 751 ถ้าคุณต้องการเขียนยอดการชำระเงินและวันครบกำหนดในบันทึกการชำระเงินด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="c6cbe-136">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="c6cbe-137">FIK 752 - พิมพ์บันทึกการชำระเงิน FIK 752 ถ้าคุณต้องการใช้ บันทึกการชำระเงินที่ถูกสร้างขึ้นโดยคอมพิวเตอร์ซึ่งมียอดการชำระเงินที่พิมพ์ล่วงหน้าและวันครบกำหนดชำระ</span><span class="sxs-lookup"><span data-stu-id="c6cbe-137">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
10. <span data-ttu-id="c6cbe-138">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-138">Click Save.</span></span>
11. <span data-ttu-id="c6cbe-139">คลิกแท็บจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cbe-139">Click the Collection letter tab.</span></span>
12. <span data-ttu-id="c6cbe-140">ในฟิลด์เอกสารแนบการชำระเงินที่เกี่ยวข้องในจดหมายเรียกเก็บเงิน ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-140">In the Associated payment attachment on collection letter field, select an option.</span></span>
    * <span data-ttu-id="c6cbe-141">ไม่มี - ห้ามพิมพ์บันทึกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cbe-141">None – Do not print a payment slip.</span></span> <span data-ttu-id="c6cbe-142">เลือกตัวเลือกนี้เมื่อยอดการชำระเงินอยู่ในสกุลเงินอื่นนอกเหนือจากโครเนอร์เดนมาร์ก (DKK)</span><span class="sxs-lookup"><span data-stu-id="c6cbe-142">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="c6cbe-143">FIK 751 - พิมพ์บันทึกการชำระเงิน FIK 751 ถ้าคุณต้องการเขียนยอดการชำระเงินและวันครบกำหนดในบันทึกการชำระเงินด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="c6cbe-143">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="c6cbe-144">FIK 752 - พิมพ์บันทึกการชำระเงิน FIK 752 ถ้าคุณต้องการใช้ บันทึกการชำระเงินที่ถูกสร้างขึ้นโดยคอมพิวเตอร์ซึ่งมียอดการชำระเงินที่พิมพ์ล่วงหน้าและวันครบกำหนดชำระ</span><span class="sxs-lookup"><span data-stu-id="c6cbe-144">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
13. <span data-ttu-id="c6cbe-145">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-145">Click Save.</span></span>
14. <span data-ttu-id="c6cbe-146">คลิกแท็บรายงานสรุปยอดบัญชี</span><span class="sxs-lookup"><span data-stu-id="c6cbe-146">Click the Account statement tab.</span></span>
15. <span data-ttu-id="c6cbe-147">ในฟิลด์เอกสารแนบการชำระเงินที่เกี่ยวข้องในรายงานสรุปยอดบัญชี ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-147">In the Associated payment attachment on account statement field, select an option.</span></span>
    * <span data-ttu-id="c6cbe-148">ไม่มี - ห้ามพิมพ์บันทึกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c6cbe-148">None – Do not print a payment slip.</span></span> <span data-ttu-id="c6cbe-149">เลือกตัวเลือกนี้เมื่อยอดการชำระเงินอยู่ในสกุลเงินอื่นนอกเหนือจากโครเนอร์เดนมาร์ก (DKK)</span><span class="sxs-lookup"><span data-stu-id="c6cbe-149">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="c6cbe-150">FIK 751 - พิมพ์บันทึกการชำระเงิน FIK 751 ถ้าคุณต้องการเขียนยอดการชำระเงินและวันครบกำหนดในบันทึกการชำระเงินด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="c6cbe-150">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="c6cbe-151">FIK 752 - พิมพ์บันทึกการชำระเงิน FIK 752 ถ้าคุณต้องการใช้ บันทึกการชำระเงินที่ถูกสร้างขึ้นโดยคอมพิวเตอร์ซึ่งมียอดการชำระเงินที่พิมพ์ล่วงหน้าและวันครบกำหนดชำระ</span><span class="sxs-lookup"><span data-stu-id="c6cbe-151">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
16. <span data-ttu-id="c6cbe-152">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c6cbe-152">Click Save.</span></span>
17. <span data-ttu-id="c6cbe-153">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c6cbe-153">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]