---
title: แก้ไขและตรวจสอบธุรกรรมใบสั่งออนไลน์และใบสั่งของลูกค้าแบบอะซิงโครนัส
description: หัวข้อนี้อธิบายวิธีการแก้ไขและตรวจสอบธุรกรรมใบสั่งออนไลน์และใบสั่งของลูกค้าแบบอะซิงโครนัสใน Microsoft Dynamics 365 Commerce
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8fa6f7a71bae759e2b8feb3c5778200bb7bdbfe9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010162"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="ef4cf-103">แก้ไขและตรวจสอบธุรกรรมใบสั่งออนไลน์และใบสั่งของลูกค้าแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="ef4cf-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef4cf-104">หัวข้อนี้อธิบายวิธีการแก้ไขและตรวจสอบธุรกรรมใบสั่งออนไลน์และใบสั่งของลูกค้าแบบอะซิงโครนัสใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ef4cf-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ef4cf-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-105">Overview</span></span>

<span data-ttu-id="ef4cf-106">ระหว่าง Commerce รุ่น 10.0.5 และ 10.0.6 มีการเพิ่มการสนับสนุนสําหรับการแก้ไขธุรกรรมเงินสดและการขนส่ง (เช่น การขายและการส่งคืน) และธุรกรรมการจัดการเงินสด (เช่น การป้อนข้อมูลเศษเงินทอนและการลบการชำระเงิน)</span><span class="sxs-lookup"><span data-stu-id="ef4cf-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="ef4cf-107">ใน Commerce รุ่น 10.0.7 มีการเพิ่มการสนับสนุนสําหรับการแก้ไขธุรกรรมใบสั่งออนไลน์และใบสั่งของลูกค้าแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="ef4cf-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="ef4cf-108">แก้ไขและตรวจสอบธุรกรรมใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ef4cf-108">Edit and audit order transactions</span></span>

<span data-ttu-id="ef4cf-109">เมื่อต้องการแก้ไขและตรวจสอบธุรกรรมใบสั่งในศูนย์ควบคุม Commerce ให้ทําตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ef4cf-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ef4cf-110">ติดตั้ง [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview)</span><span class="sxs-lookup"><span data-stu-id="ef4cf-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="ef4cf-111">บนหน้า **พารามิเตอร์การขายปลีก** บนแท็บ **ใบสั่งของลูกค้า** บนแท็บด่วน **ใบสั่ง** ให้ระบุรหัสการระงับสำหรับ **รหัสการระงับสำหรับสําหรับข้อผิดพลาดการซิงโครไนส์ใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="ef4cf-112">เปิดพื้นที่ทำงาน **การเงินของร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="ef4cf-113">ไทล์ **ข้อผิดพลาดการซิงโครไนส์ใบสั่งออนไลน์** และ **ข้อผิดพลาดการซิงโครไนส์ใบสั่งของลูกค้า** จะให้มุมมองที่กรองไว้ล่วงหน้าของหน้าธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="ef4cf-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="ef4cf-114">แต่ละไทล์จะแสดงเรกคอร์ดธุรกรรมที่ล้มเหลวในการซิงโครไนส์สําหรับชนิดใบสั่งที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ef4cf-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="ef4cf-115">เปิดหน้า **ข้อผิดพลาดการซิงโครไนส์ใบสั่งออนไลน์** หรือหน้า **ข้อผิดพลาดการซิงโครไนส์ใบสั่งของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="ef4cf-116">เลือกเรกคอร์ดเพื่อดูรายละเอียดข้อผิดพลาดในการซิงโครไนส์</span><span class="sxs-lookup"><span data-stu-id="ef4cf-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="ef4cf-117">แท็บด่วน **สถานะการซิงโครไนส์** ให้รายละเอียดข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ef4cf-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="ef4cf-118">สถานะของใบสั่งที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="ef4cf-118">Pending order status</span></span>
    - <span data-ttu-id="ef4cf-119">รายละเอียดข้อผิดพลาดของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="ef4cf-119">Order error details</span></span>
    - <span data-ttu-id="ef4cf-120">วันที่และเวลาที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="ef4cf-120">Modified date and time</span></span>
    - <span data-ttu-id="ef4cf-121">จำนวนการลองอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ef4cf-121">Retry count</span></span>

1. <span data-ttu-id="ef4cf-122">ถ้ารายละเอียดข้อผิดพลาดระบุว่าเรกคอร์ดต้องได้รับการแก้ไข ให้เลือก **Office Add-in** แล้วเลือก **แก้ไขธุรกรรมที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="ef4cf-123">ไฟล์ Excel ที่แสดงรายละเอียดของธุรกรรมที่เลือกจะถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="ef4cf-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="ef4cf-124">ถ้าธุรกรรมที่กําลังแก้ไขเป็นธุรกรรมใบสั่งออนไลน์ ไฟล์ Excel จะมีเวิร์กชีตต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ef4cf-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="ef4cf-125">**ธุรกรรม** – เวิร์กชีตนี้มีรายละเอียดส่วนหัวของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="ef4cf-126">**ธุรกรรมการขาย** – เวิร์กชีตนี้มีรายละเอียดรายการของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="ef4cf-127">**ธุรกรรมการชำระเงิน** – เวิร์กชีตนี้มีรายละเอียดของรายการชำระเงินของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="ef4cf-128">**ธุรกรรมส่วนลด** – เวิร์กชีตนี้มีรายละเอียดที่เกี่ยวข้องกับส่วนลดของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="ef4cf-129">**ธุรกรรมภาษี** – เวิร์กชีตนี้มีรายละเอียดที่เกี่ยวข้องกับภาษีของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="ef4cf-130">**ธุรกรรมค่าธรรมเนียม** – เวิร์กชีตนี้มีข้อมูลที่เกี่ยวข้องกับค่าธรรมเนียมของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="ef4cf-131">ถ้าธุรกรรมที่กําลังแก้ไขเป็นธุรกรรมใบสั่งของลูกค้าแบบอะซิงโครนัส ไฟล์ Excel จะมีเวิร์กชีตต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ef4cf-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="ef4cf-132">**รายการ** – เวิร์กชีตนี้มีรายละเอียดของส่วนหัวและรายการของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="ef4cf-133">**การชำระเงิน** – เวิร์กชีตนี้มีรายละเอียดของรายการชำระเงินของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="ef4cf-134">**ส่วนลด** – เวิร์กชีตนี้มีมีรายละเอียดที่เกี่ยวข้องกับส่วนลดของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="ef4cf-135">**ภาษี** – เวิร์กชีตนี้มีรายละเอียดที่เกี่ยวข้องกับภาษีของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="ef4cf-136">**ค่าธรรมเนียม** – เวิร์กชีตนี้มีมีข้อมูลที่เกี่ยวข้องกับค่าธรรมเนียมของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="ef4cf-137">ในไฟล์ Excel ในฟิลด์ **สถานะใบสั่งที่ค้างอยู่** ให้ป้อน **กำลังแก้ไข** แล้วเผยแพร่การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="ef4cf-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="ef4cf-138">ด้วยวิธีนี้ คุณจะป้องกันไม่ให้งาน **ซิงโครไนส์ใบสั่ง** ที่กําลังรันในโหมดชุดงานข้ามเรกคอร์ดนี้ในระหว่างการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="ef4cf-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="ef4cf-139">ในไฟล์ Excel ให้ปรับเปลี่ยนฟิลด์ที่เหมาะสมแล้วอัปโหลดข้อมูลกลับเข้าไปในศูนย์ควบคุม Commerce โดยใช้ฟังก์ชันการเผยแพร่ของ Dynamics Excel Add-in</span><span class="sxs-lookup"><span data-stu-id="ef4cf-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="ef4cf-140">หลังจากที่เผยแพร่ข้อมูล การเปลี่ยนแปลงจะปรากฏในระบบ</span><span class="sxs-lookup"><span data-stu-id="ef4cf-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="ef4cf-141">ระหว่างการเผยแพร่ จะไม่มีการตรวจสอบความถูกต้องสำหรับการเปลี่ยนแปลงที่ผู้ใช้ทำ</span><span class="sxs-lookup"><span data-stu-id="ef4cf-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="ef4cf-142">คุณสามารถดูบันทึกการตรวจสอบบัญชีที่สมบูรณ์ของการเปลี่ยนแปลงได้โดยการเลือก **ดูบันทึกการตรวจสอบ** ในหัวข้อ **ธุรกรรมการขายปลีก** สำหรับการเปลี่ยนแปลงในระดับหัวข้อและในส่วนและเรกคอร์ดที่เกี่ยวข้องในหน้าธุรกรรมที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="ef4cf-143">ตัวอย่างเช่น การเปลี่ยนแปลงทั้งหมดที่เกี่ยวข้องกับรายการขายจะแสดงขึ้นบนหน้า **ธุรกรรมการขาย** และการเปลี่ยนแปลงทั้งหมดที่เกี่ยวข้องกับการชําระเงินจะแสดงขึ้น **ธุรกรรมการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ef4cf-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="ef4cf-144">รายละเอียดการตรวจสอบต่อไปนี้ได้รับการรักษาไว้สําหรับการเปลี่ยนแปลง:</span><span class="sxs-lookup"><span data-stu-id="ef4cf-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="ef4cf-145">วันที่และเวลาที่แก้ไข</span><span class="sxs-lookup"><span data-stu-id="ef4cf-145">Modified date and time</span></span>
    - <span data-ttu-id="ef4cf-146">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="ef4cf-146">Field</span></span>
    - <span data-ttu-id="ef4cf-147">ค่าเก่า</span><span class="sxs-lookup"><span data-stu-id="ef4cf-147">Old value</span></span>
    - <span data-ttu-id="ef4cf-148">ค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="ef4cf-148">New value</span></span>
    - <span data-ttu-id="ef4cf-149">ปรับเปลี่ยนโดย</span><span class="sxs-lookup"><span data-stu-id="ef4cf-149">Modified by</span></span>

1. <span data-ttu-id="ef4cf-150">หลังจากที่คุณได้ทําการเปลี่ยนแปลงและเผยแพร่ ให้เลือก **ซิงโครไนส์ใบสั่ง** เพื่อเริ่มกระบวนการซิงโครไนส์ทันที</span><span class="sxs-lookup"><span data-stu-id="ef4cf-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="ef4cf-151">อีกวิธีคือ คุณสามารถรอกระบวนการซิงโครไนส์ที่กําลังรันในโหมดชุดงานเพื่อประมวลผลธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="ef4cf-152">ตามค่าเริ่มต้น หลังจากซิงค์ใบสั่งเรียบร้อยแล้ว ใบสั่งจะมีการกำหนดไว้ในสถานะระงับ ตามรหัสการระงับที่กําหนดไว้ในพารามิเตอร์ Commerce</span><span class="sxs-lookup"><span data-stu-id="ef4cf-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="ef4cf-153">การระงับใบสั่งจะต้องถูกลบออกก่อนจึงจะสามารถประมวลผลใบสั่งต่อไปได้สําหรับการดำเนินการกับใบสั่งหรือการดําเนินงานอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="ef4cf-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef4cf-154">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ef4cf-154">Additional resources</span></span>

[<span data-ttu-id="ef4cf-155">แก้ไขและตรวจสอบธุรกรรมเงินสดและการขนส่งและการจัดการเงินสด</span><span class="sxs-lookup"><span data-stu-id="ef4cf-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="ef4cf-156">แก้ไขมิติทางการเงินสำหรับธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="ef4cf-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="ef4cf-157">สร้างเวิร์กบุ๊ก Excel เพื่อแก้ไขธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="ef4cf-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="ef4cf-158">เพิ่มฟิลด์ลงในเวิร์กบุ๊ก Excel เพื่อแก้ไขธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="ef4cf-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
