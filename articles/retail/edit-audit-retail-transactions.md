---
title: แก้ไขและตรวจสอบธุรกรรมของร้านค้าปลีก
description: หัวข้อนี้จะอธิบายถึงฟังก์ชันสำหรับการแก้ไขและการตรวจสอบความถูกต้องของธุรกรรมของร้านค้าปลีก
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: f53573b8afb2003f6796930f5877185e533a4715
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693077"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="d2a33-103">แก้ไขและตรวจสอบธุรกรรมของร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="d2a33-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d2a33-104">ลูกค้า Dynamics 365 Retail จะใช้งานแอพลิเคชันการขายหน้าร้านของ (POS) ของ Microsoft หรือของบริษัทอื่น</span><span class="sxs-lookup"><span data-stu-id="d2a33-104">Dynamics 365 Retail customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="d2a33-105">เมื่อใช้แอพลิเคชัน POS ของ Microsoft ธุรกรรมของร้านค้าปลีกจะถูกดึงลงใน Retail Headquarters จากช่องทางต่างๆ ผ่านกระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="d2a33-105">With the first-party POS application, retail store transactions are pulled into Retail Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="d2a33-106">เมื่อใช้แอพลิเคชันของบริษัทอื่น ธุรกรรมจะถูกดึงลงใน Retail Headquarters ผ่านทางการรวม</span><span class="sxs-lookup"><span data-stu-id="d2a33-106">With third-party applications, transactions are pulled into Retail Headquarters through integration.</span></span> <span data-ttu-id="d2a33-107">ในทั้งสองกรณี หลังจากที่มีการดึงข้อมูลธุรกรรมลงใน Retail Headquarters ต้องมีการดำเนินกระบวนการตรวจสอบความสอดคล้องกันที่ใช้การตรวจสอบความถูกต้องหลายอย่างกับธุรกรรม เพื่อให้มีการดึงข้อมูลธุรกรรมที่ตรวจสอบความถูกต้องเรียบร้อยแล้วเท่านั้นลงในใบแจ้งยอดที่จะลงรายการบัญชีใน Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="d2a33-107">In both cases, after transactions are pulled into Retail Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Retail Headquarters.</span></span> 

<span data-ttu-id="d2a33-108">ธุรกรรมการขายปลีกไม่ผ่านการตรวจสอบความถูกต้องด้วยหลายสาเหตุ</span><span class="sxs-lookup"><span data-stu-id="d2a33-108">Retail transactions fail validation for various reasons.</span></span> <span data-ttu-id="d2a33-109">ตัวอย่างเช่น ข้อผิดพลาดในโค้ดการรวมหรือข้อบกพร่องในแอพลิเคชัน POS อาจทำให้เกิดข้อมูลที่ไม่สอดคล้องกัน หรือข้อผิดพลาดของผู้ใช้ เช่น การลบผลิตภัณฑ์หลังจากที่มีการซิงโครไนส์กับช่องทางหรือการปิดรอบระยะเวลาทางบัญชีโดยไม่มีการลงรายการบัญชีธุรกรรมการขายปลีกสำหรับรอบระยะเวลานั้น อาจทำให้ข้อมูลไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="d2a33-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting retail transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="d2a33-110">แม้ว่าธุรกรรมเหล่านี้จะได้รับการตั้งค่าสถานะและไม่รวมอยู่ในใบแจ้งยอด แต่ธุรกรรมดังกล่าวอาจขัดขวางกระบวนการรายวันของลูกค้าในการลงรายการบัญชีการขายปลีกประจำวันให้กับฝ่ายการเงิน</span><span class="sxs-lookup"><span data-stu-id="d2a33-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily retail sales to the financials.</span></span>

<span data-ttu-id="d2a33-111">ใน Retail คุณสามารถแก้ไขธุรกรรมการขายปลีกเฉพาะที่ไม่ผ่านการตรวจสอบความถูกต้องขณะที่รักษาการตรวจสอบการเปลี่ยนแปลงทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="d2a33-111">In Retail, you can edit the specific retail transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="d2a33-112">แก้ไขและตรวจสอบธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="d2a33-112">Edit and audit transactions</span></span>

<span data-ttu-id="d2a33-113">ใน Retail รุ่น 10.0.5 ธุรกรรมเงินสดและการขนส่ง เช่น การขายและการส่งคืนเป็นธุรกรรมเดียวที่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="d2a33-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="d2a33-114">การแก้ไขใบสั่งของลูกค้าหรือใบสั่งออนไลน์ไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d2a33-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="d2a33-115">ใน Retail รุ่น 10.0.6 ขึ้นไป มีการสนับสนุนการแก้ไขธุรกรรมการจัดการเงินสดด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d2a33-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="d2a33-116">ติดตั้ง Add-in ของ Dynamics Excel</span><span class="sxs-lookup"><span data-stu-id="d2a33-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="d2a33-117">ไปยังพื้นที่ทำงาน **การเงินของร้านค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="d2a33-117">Go to the **Retail store financials** workspace.</span></span> <span data-ttu-id="d2a33-118">ไทล์ **ความล้มเหลวในการตรวจสอบความถูกต้องของธุรกรรม** แสดงมุมมองที่ถูกกรองไว้ล่วงหน้าของแบบฟอร์มธุรกรรมการขายปลีกที่ล้มเหลวสำหรับกฎการตรวจสอบความถูกต้องอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="d2a33-118">The **Transaction validation failures** tile provides a pre-filtered view of the Retail transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="d2a33-119">เปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="d2a33-119">Open the form.</span></span> <span data-ttu-id="d2a33-120">คลิกที่เรกคอร์ดที่การตรวจสอบความถูกต้องล้มเหลว คลิก **Add-in ของ Office** แล้วคลิก **แก้ไขธุรกรรมที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="d2a33-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="d2a33-121">ไฟล์ Excel ที่มีรายละเอียดของธุรกรรมที่เลือกจะเปิดขึ้น พร้อมกับมีแผ่นงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d2a33-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="d2a33-122">รายการ: แผ่นงานนี้มีรายการหัวข้อและผลิตภัณฑ์และข้อมูลที่เกี่ยวข้องสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="d2a33-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="d2a33-123">การชำระเงิน: แผ่นงานนี้มีรายละเอียดของรายการการชำระเงินสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="d2a33-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="d2a33-124">ส่วนลด: แผ่นงานนี้มีรายละเอียดที่เกี่ยวข้องกับส่วนลดสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="d2a33-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="d2a33-125">ภาษี: แผ่นงานนี้มีรายละเอียดที่เกี่ยวข้องกับภาษีสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="d2a33-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="d2a33-126">ค่าธรรมเนียม: แผ่นงานนี้มีข้อมูลที่เกี่ยวข้องกับค่าธรรมเนียมสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="d2a33-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="d2a33-127">ในไฟล์ Excel คุณสามารถปรับเปลี่ยนฟิลด์ที่เหมาะสมแล้วอัพโหลดข้อมูลกลับเข้าไปใน Retail Headquarters โดยใช้ฟังก์ชันเผยแพร่ของ Add-in ของ Dynamics Excel</span><span class="sxs-lookup"><span data-stu-id="d2a33-127">In the Excel file, you modify the appropriate fields and then upload the data back into Retail Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="d2a33-128">เมื่อเผยแพร่แล้ว การเปลี่ยนแปลงจะปรากฏในระบบ</span><span class="sxs-lookup"><span data-stu-id="d2a33-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="d2a33-129">ระหว่างการเผยแพร่ จะไม่มีการตรวจสอบความถูกต้องของการเปลี่ยนแปลงที่ผู้ใช้ทำ</span><span class="sxs-lookup"><span data-stu-id="d2a33-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="d2a33-130">คุณสามารถดูบันทึกการตรวจสอบบัญชีที่สมบูรณ์ของการเปลี่ยนแปลงได้โดยคลิก **ดูบันทึกการตรวจสอบ** ในหัวข้อ **ธุรกรรมการขายปลีก** สำหรับการเปลี่ยนแปลงในระดับหัวข้อและในส่วนและเรกคอร์ดที่เกี่ยวข้องในหน้าธุรกรรมที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="d2a33-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="d2a33-131">ตัวอย่างเช่น การเปลี่ยนแปลงทั้งหมดที่เกี่ยวข้องกับรายการขายจะปรากฏบนหน้า **ธุรกรรมการขาย** การเปลี่ยนแปลงที่เกี่ยวข้องกับการชำระเงินจะปรากฏในหน้า **ธุรกรรมการชำระเงิน** ฯลฯ รายละเอียดการตรวจสอบที่มีการเก็บรักษาไว้สำหรับการเปลี่ยนแปลงมีดังนี้</span><span class="sxs-lookup"><span data-stu-id="d2a33-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="d2a33-132">วันที่และเวลาที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="d2a33-132">Modified date and time</span></span>
   - <span data-ttu-id="d2a33-133">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="d2a33-133">Field</span></span> 
   - <span data-ttu-id="d2a33-134">ค่าเก่า</span><span class="sxs-lookup"><span data-stu-id="d2a33-134">Old value</span></span>
   - <span data-ttu-id="d2a33-135">ค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="d2a33-135">New value</span></span>
   - <span data-ttu-id="d2a33-136">แก้ไขโดย</span><span class="sxs-lookup"><span data-stu-id="d2a33-136">Modified by</span></span>

6. <span data-ttu-id="d2a33-137">หลังจากที่ทำการเปลี่ยนแปลงและเผยแพร่แล้ว ให้เรียกใช้ตัวเลือก **ตรวจสอบความถูกต้องของธุรกรรมร้านค้า** อีกครั้งเพื่อตรวจสอบว่าการเปลี่ยนแปลงที่คุณทำไว้มีความสอดคล้องกันและถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d2a33-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="d2a33-138">คุณสามารถแก้ไขได้เฉพาะธุรกรรมที่ไม่ผ่านการตรวจสอบความถูกต้องเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d2a33-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="d2a33-139">หากคุณต้องการแก้ไขธุรกรรมที่ผ่านการตรวจสอบความถูกต้อง ให้เปลี่ยนสถานะการตรวจสอบความถูกต้องของธุรกรรมที่คุณต้องการเปลี่ยนเป็น **ผิดพลาด** หรือ **ไม่มี** แล้วคุณจะสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="d2a33-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="d2a33-140">แก้ไขธุรกรรมจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="d2a33-140">Bulk edit transactions</span></span>

<span data-ttu-id="d2a33-141">ใน Retail รุ่น10.0.6 ขึ้นไป ตัวเลือกในการแก้ไขธุรกรรมขายปลีกจำนวนมากที่ระดับใบแจ้งยอดได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d2a33-141">In Retail version 10.0.6 and higher, the option to bulk edit retail transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="d2a33-142">ใช้ Add-in ของ Excel เพื่อเปิดใบแจ้งยอดที่มีธุรกรรมที่คุณต้องการแก้ไขโดยใช้ขั้นตอนที่ 1-3 ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="d2a33-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="d2a33-143">เลือกตัวเลือกใดตัวเลือกหนึ่งด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="d2a33-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="d2a33-144">**แก้ไขธุรกรรมเงินสดและการขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="d2a33-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="d2a33-145">ตัวเลือกนี้ช่วยให้คุณสามารถแก้ไขธุรกรรมเงินสดและการขนส่งทั้งหมดที่รวมอยู่ในใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="d2a33-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="d2a33-146">แผ่นงาน Excel ที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d2a33-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="d2a33-147">**ธุรกรรม**: แผ่นงานนี้มีข้อมูลระดับหัวข้อทั้งหมดสำหรับธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="d2a33-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="d2a33-148">**ธุรกรรมการขาย**: แผ่นงานนี้มีข้อมูลระดับรายการทั้งหมดสำหรับธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="d2a33-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="d2a33-149">**ธุรกรรมการชำระเงิน**: แผ่นงานนี้มีข้อมูลรายการการชำระเงินทั้งหมดสำหรับธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="d2a33-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="d2a33-150">**ธุรกรรมส่วนลด**: แผ่นงานนี้มีข้อมูลรายการส่วนลดทั้งหมดสำหรับธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="d2a33-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="d2a33-151">**ธุรกรรมภาษี**: แผ่นงานนี้มีข้อมูลรายการภาษีทั้งหมดสำหรับธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="d2a33-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="d2a33-152">**ธุรกรรมค่าธรรมเนียม**: แผ่นงานนี้มีข้อมูลรายการค่าธรรมเนียมทั้งหมดสำหรับธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="d2a33-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="d2a33-153">**แก้ไขธุรกรรมการจัดการเงินสด**</span><span class="sxs-lookup"><span data-stu-id="d2a33-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="d2a33-154">ตัวเลือกนี้ช่วยให้คุณสามารถแก้ไขธุรกรรมการจัดการเงินสดทั้งหมดที่รวมอยู่ในใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="d2a33-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="d2a33-155">แผ่นงาน Excel ที่พร้อมใช้งานมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d2a33-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="d2a33-156">**ธุรกรรม**: แผ่นงานนี้มีข้อมูลระดับหัวข้อทั้งหมดสำหรับธุรกรรมการจัดการเงินสด</span><span class="sxs-lookup"><span data-stu-id="d2a33-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="d2a33-157">**ธุรกรรมการชำระเงินธนาคาร**: แผ่นงานนี้มีรายละเอียดธุรกรรมการนำเงินฝากธนาคารทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d2a33-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="d2a33-158">**ธุรกรรมการชำระเงินที่เข้าเซฟ**: แผ่นงานนี้มีรายละเอียดธุรกรรมการนำเงินฝากเข้าเซฟทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d2a33-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="d2a33-159">**การตรวจนับเงิน**: แผ่นงานนี้มีรายละเอียดธุรกรรมการตรวจนับเงินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d2a33-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="d2a33-160">**ธุรกรรมรายได้-ค่าใช้จ่าย**: แผ่นงานนี้มีรายละเอียดรายละเอียดรายละเอียดของรายการธุรกรรมรายได้-ค่าใช้จ่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d2a33-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="d2a33-161">**ธุรกรรมการชำระเงิน**: แผ่นงานนี้มีข้อมูลที่เกี่ยวข้องกับการชำระเงินสำหรับการดำเนินการ **ชำระเงินตามใบแจ้งหนี้** และธุรกรรมธุรกรรมรายได้-ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d2a33-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="d2a33-162">การตรวจสอบความถูกต้องจะไม่มีการดำเนินการเมื่อคุณเผยแพร่ธุรกรรมที่แก้ไขจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="d2a33-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="d2a33-163">คุณต้องตรวจสอบให้แน่ใจว่าการแก้ไขทั้งหมดของคุณถูกต้องและความถูกต้องของข้อมูลในแผ่นงานมีการรักษาไว้</span><span class="sxs-lookup"><span data-stu-id="d2a33-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="d2a33-164">ตัวอย่างเช่น หากคุณต้องการเปลี่ยนแปลงวันที่ของธุรกรรมเพื่อจัดการสถานการณ์ที่มีการปิดรอบระยะเวลาทางบัญชีหรือสินค้าคงคลังสำหรับธุรกรรมการขายปลีกที่เปิดค้างไว้ คุณต้องเปลี่ยนวันที่ในแผ่นงาน Excel ทั้งหมดที่มีคอลัมน์ **วันที่ทำการ**</span><span class="sxs-lookup"><span data-stu-id="d2a33-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open retail transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="d2a33-165">เมื่อต้องการตรวจสอบความถูกต้องของธุรกรรมหลังจากแก้ไขแล้ว คุณสามารถใช้ **ตรวจสอบความถูกต้องของธุรกรรมซ้ำ** ในหน้า **ใบแจ้งยอดการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="d2a33-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Retail statements** page.</span></span>
