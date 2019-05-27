---
title: ระงับและดำเนินการธุรกรรมต่อในจุดขายหน้าร้าน (POS)
description: หัวข้อนี้อธิบายวิธีการที่ผู้ใช้สามารถระงับธุรกรรมที่กำลังดำเนินการ และจากนั้นดำเนินการต่อในภายหลัง หรือในการลงทะเบียนที่แตกต่างกันโดยการใช้ Microsoft Dynamics 365 for Retail
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ffb04609318c7de4b9ef729a8e03a7f9395806b8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569555"
---
# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a><span data-ttu-id="3ba15-103">ระงับและดำเนินการธุรกรรมต่อในจุดขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="3ba15-103">Suspend and resume transactions in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="3ba15-104">ผู้ใช้จุดขายหน้าร้าน (POS) สามารถระงับธุรกรรมที่อยู่ระหว่างดำเนินการ และจากนั้นดำเนินการต่อในภายหลัง หรือบนเครื่องบันทึกเงินสดอื่น</span><span class="sxs-lookup"><span data-stu-id="3ba15-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="3ba15-105">ธุรกรรมมักจะถูกระงับเพื่อทำให้เครื่องบันทึกเงินสดว่างอย่างรวดเร็วสำหรับงานอื่น โดยไม่สูญเสียความคืบหน้าใดๆ บนธุรกรรมปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3ba15-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="3ba15-106">ตัวอย่างเช่น การเชื่อมโยงร้านค้าเริ่มต้นการประมวลผลธุรกรรมของลูกค้าบนอุปกรณ์เคลื่อนที่ แต่ต้องทำให้สมบูรณ์บนเครื่องบันทึกเงินสดที่มีลิ้นชักเงินสด</span><span class="sxs-lookup"><span data-stu-id="3ba15-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="3ba15-107">ในกรณีนี้ การเชื่อมโยงร้านค้าสามารถระงับธุรกรรมบนอุปกรณ์เคลื่อนที่ และจากนั้นเรียกคืน และดำเนินการต่อไปบนเครื่องบันทึกเงินสดได้</span><span class="sxs-lookup"><span data-stu-id="3ba15-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="3ba15-108">ตั้งค่าคอนฟิกการระงับ และดำเนินการฟังก์ชันต่อ</span><span class="sxs-lookup"><span data-stu-id="3ba15-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="3ba15-109">การดำเนินงานของ POS</span><span class="sxs-lookup"><span data-stu-id="3ba15-109">POS operations</span></span>

<span data-ttu-id="3ba15-110">[การดำเนินงาน POS](pos-operations.md) สองรายการ อนุญาตให้การสนับสนุน POS หยุดชั่วคราว และดำเนินการสถานการณ์จำลองต่อไป</span><span class="sxs-lookup"><span data-stu-id="3ba15-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="3ba15-111">คุณสามารถกำหนดการดำเนินการเหล่านี้ให้กับ [กริดปุ่ม](pos-screen-layouts.md) บนหน้าธุรกรรมหรือหน้าต้อนรับได้</span><span class="sxs-lookup"><span data-stu-id="3ba15-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="3ba15-112">503: ระงับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3ba15-112">503: Suspend transaction</span></span>
- <span data-ttu-id="3ba15-113">504: เรียกคืนธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3ba15-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="3ba15-114">เท็มเพลตใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="3ba15-114">Receipt template</span></span>

<span data-ttu-id="3ba15-115">สามารถตั้งค่าคอนฟิก POS เพื่อสร้างบันทึกที่จัดพิมพ์ เมื่อธุรกรรมถูกพักชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="3ba15-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="3ba15-116">จากนั้น สามารถใช้บันทึกนั้นเพื่อระบุ และเรียกคืนธุรกรรมในภายหลังได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="3ba15-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="3ba15-117">เมื่อต้องการเปิดใช้งาน POS เพื่อพิมพ์บันทึก คุณต้องเพิ่มรูปแบบใบเสร็จ **ระงับธุรกรรม** ไปยังโพรไฟล์ใบเสร็จของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="3ba15-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="3ba15-118">คุณสามารถออกแบบรูปแบบใบเสร็จ เพื่อให้มีการรวมหรือไม่รวมรายละเอียดเฉพาะเกี่ยวกับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3ba15-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="3ba15-119">ตัวอย่างเช่น รูปแบบสามารถมีบาร์โค้ดเพื่อสนับสนุนการสแกน</span><span class="sxs-lookup"><span data-stu-id="3ba15-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="3ba15-120">การกำหนดหมายเลขใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="3ba15-120">Receipt numbering</span></span>

<span data-ttu-id="3ba15-121">เช่นกันกับชนิดของธุรกรรมอื่นๆ ของ POS ที่สร้างใบเสร็จที่พิมพ์ คุณสามารถกำหนดลำดับหมายเลขสำหรับธุรกรรมที่ระงับในส่วน **การกำหนดหมายเลขใบเสร็จ** ของโพรไฟล์ฟังก์ชันของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="3ba15-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="3ba15-122">เป็นโมฆะเมื่อปิดกะ</span><span class="sxs-lookup"><span data-stu-id="3ba15-122">Void when closing shift</span></span>

<span data-ttu-id="3ba15-123">คุณสามารถใช้ตัวเลือก **ยกเลิกเมื่อปิดกะ** เพื่อกำหนดให้ผู้ใช้ทำให้เสร็จสมบูรณ์ หรือยกเลิกธุรกรรมที่ระงับใดๆ ก่อนที่พวกเขาจะปิดกะของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="3ba15-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="3ba15-124">ในระหว่างการดำเนินงาน **ปิดกะ** POS จะพร้อมต์ผู้ใช้ให้ดู หรือยกเลิกธุรกรรมที่ระงับคงค้างใดๆ</span><span class="sxs-lookup"><span data-stu-id="3ba15-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="3ba15-125">ระงับและดำเนินการธุรกรรมต่อ</span><span class="sxs-lookup"><span data-stu-id="3ba15-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="3ba15-126">ระงับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3ba15-126">Suspend a transaction</span></span>

<span data-ttu-id="3ba15-127">ผู้ใช้ที่มีสิทธิ์เพียงพอ และที่มีโครงร่างหน้าจอที่มีการดำเนินงาน **ระงับธุรกรรม** สามารถระงับธุรกรรม เพื่อให้สามารถเรียกได้ในภายหลัง หรือบนเครื่องบันทึกเงินสดอื่น</span><span class="sxs-lookup"><span data-stu-id="3ba15-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="3ba15-128">สามารถระงับธุรกรรมได้เฉพาะเมื่อ **ไม่** ประกอบด้วยชนิดของรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3ba15-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="3ba15-129">รายการการชำระเงินที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="3ba15-129">Active payment lines</span></span>
- <span data-ttu-id="3ba15-130">รายการบัตรของขวัญ (อาจออกบัตรของขวัญ หรือเพิ่มไปยังยอดดุลของบัตรของขวัญ)</span><span class="sxs-lookup"><span data-stu-id="3ba15-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="3ba15-131">ธุรกรรมที่ระงับไม่มีผลต่อข้อมูลการขายหรือข้อมูลความพร้อมใช้งานสินค้าคงคลังสำหรับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="3ba15-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="3ba15-132">ดำเนินงานธุรกรรมที่ระงับต่อ</span><span class="sxs-lookup"><span data-stu-id="3ba15-132">Resume a suspended transaction</span></span>

<span data-ttu-id="3ba15-133">สามารถเรียกคืนและดำเนินการธุรกรรมที่ระงับต่อในร้านค้าเดียวกันได้ โดยผู้ใช้ใดๆ ที่มีสิทธิ์เพียงพอ และที่มีโครงร่างที่รวมการดำเนินงาน **เรียกคืนธุรกรรม** ได้</span><span class="sxs-lookup"><span data-stu-id="3ba15-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="3ba15-134">เมื่อต้องการเรียกคืนธุรกรรมที่ระงับอย่างรวดเร็วและง่ายดาย สแกนบาร์โค้ดในบันทึกที่พิมพ์ ขณะที่คุณกำลังดูรายการของธุรกรรมจากการดำเนินงาน **เรียกคืนธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="3ba15-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="3ba15-135">ข้อควรพิจารณาสำหรับโหมดออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="3ba15-135">Considerations for offline mode</span></span>

- <span data-ttu-id="3ba15-136">ไม่สามารถดำเนินการธุรกรรมที่ถูกพักชั่วคราวใดๆ ต่อในโหมดออฟไลน์ได้ ขณะที่ POS อยู่ในโหมดออนไลน์ เนื่องจากข้อมูลไม่ตรงกับฐานข้อมูลแบบออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="3ba15-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="3ba15-137">ถ้าคุณระงับธุรกรรม ขณะที่ POS อยู่ในโหมดออฟไลน์ คุณสามารถเรียกคืนได้ในโหมดออฟไลน์ โดยที่ POS ไม่สลับไปยังโหมดออนไลน์ตลอดเวลานับตั้งแต่คุณระงับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3ba15-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="3ba15-138">เมื่อ POS ถูกสลับไปยังโหมดออนไลน์ ข้อมูลเกี่ยวกับธุรกรรมที่ระงับจะมีการย้ายไปยังฐานข้อมูลออนไลน์ และถูกลบออกจากฐานข้อมูลออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="3ba15-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="3ba15-139">ดังนั้น ธุรกรรมที่สามารถดำเนินต่อได้ในโหมดออนไลน์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3ba15-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="3ba15-140">ถ้าคุณสลับ POS กลับไปยังโหมดออฟไลน์ คุณจะไม่สามารถกลับมาทำงานดังกล่าวธุรกรรมที่ระงับได้ เนื่องจากรายการเหล่านั้นถูกลบออกจากฐานข้อมูลออฟไลน์แล้ว</span><span class="sxs-lookup"><span data-stu-id="3ba15-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="3ba15-141">ยกเลิกธุรกรรมที่ระงับ</span><span class="sxs-lookup"><span data-stu-id="3ba15-141">Void a suspended transaction</span></span>

<span data-ttu-id="3ba15-142">คุณสามารถยกเลิกธุรกรรมที่ระงับได้ โดยการเรียกคืนธุรกรรม และจากนั้น ดำเนินการดำเนินงาน **ยกเลิกธุรกรรม** หรือโดยการเลือกธุรกรรมในรายการ **เรียกคืนธุรกรรม** และเลือก **ยกเลิก** บนแถบแอป</span><span class="sxs-lookup"><span data-stu-id="3ba15-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="3ba15-143">อีกทางหนึ่งคือ คุณสามารถตั้งค่าคอนฟิกร้านค้าเพื่อพร้อมท์ผู้ใช้ให้ยกเลิกธุรกรรมที่ระงับ เมื่อพวกเขาปิดกะของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="3ba15-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
