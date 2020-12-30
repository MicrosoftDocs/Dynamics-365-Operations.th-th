---
title: ส่งใบแจ้งหนี้ไปที่ระบบลำดับงานและจับคู่บรรทัดใบรับสินค้า (พรีวิว)
description: หัวข้อนี้อธิบายกระบวนการในการส่งใบแจ้งหนี้ของผู้จัดจำหน่ายไปยังระบบลำดับงาน และการจับคู่บรรทัดใบรับสินค้าที่ลงรายการบัญชีกับใบแจ้งหนี้ของผู้จัดจำหน่าย
author: abruer
manager: AnnBe
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cde164ee89b542d769d81d8d483049fb7ca001c4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448253"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines-preview"></a><span data-ttu-id="be5e3-103">ส่งใบแจ้งหนี้ไปที่ระบบลำดับงานและจับคู่บรรทัดใบรับสินค้า (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="be5e3-103">Submit invoices to the workflow system and match product receipt lines (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="be5e3-104">หัวข้อนี้อธิบายกระบวนการในการส่งใบแจ้งหนี้ของผู้จัดจำหน่ายไปยังระบบลำดับงาน และการจับคู่บรรทัดใบรับสินค้าที่ลงรายการบัญชีกับใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="be5e3-104">This topic explains the process of submitting vendor invoices to the workflow system and automatically matching posted product receipt lines to vendor invoices.</span></span>

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a><span data-ttu-id="be5e3-105">การส่งใบแจ้งหนี้ของผู้จัดจำหน่ายที่นำเข้าไปยังระบบลำดับงาน และการจับคู่บรรทัดใบรับสินค้าที่ลงรายการบัญชีไปยังรายการใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="be5e3-105">Submitting imported vendor invoices to the workflow system and matching posted product receipt lines to pending vendor invoice lines</span></span>

<span data-ttu-id="be5e3-106">เนื่องจากเป็นส่วนหนึ่งของกระบวนการออกใบแจ้งหนี้ของบัญชีเจ้าหนี้ คุณสามารถให้ระบบส่งใบแจ้งหนี้ที่นำเข้าไปยังระบบลำดับงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="be5e3-106">As part of a touchless Accounts payable invoicing process, you can have the system automatically submit an imported invoice to the workflow system.</span></span> <span data-ttu-id="be5e3-107">คุณสามารถตั้งค่าคอนฟิกกระบวนการในการส่งใบแจ้งหนี้ที่นำเข้าไปยังระบบลำดับงานบนแท็บ **ระบบอัตโนมัติของใบแจ้งหนี้ของผู้จัดจำหน่าย** ของหน้า **พารามิเตอร์บัญชีเจ้าหนี้** (**บัญชีเจ้าหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีเจ้าหนี้**)</span><span class="sxs-lookup"><span data-stu-id="be5e3-107">You can configure the process of submitting imported invoices to the workflow system on the **Vendor invoice automation** tab of the **Accounts payable parameters** page (**Accounts payable \> Setup \> Accounts payable parameters**).</span></span> <span data-ttu-id="be5e3-108">กระบวนการส่งไปที่ลำดับงานจะรันในพื้นหลัง ที่ความถี่ที่คุณระบุ (รายชั่วโมง หรือรายวัน)</span><span class="sxs-lookup"><span data-stu-id="be5e3-108">The submit-to-workflow process will run in the background, at a frequency that you specify (either hourly or daily).</span></span>

<span data-ttu-id="be5e3-109">เมื่อคุณส่งใบแจ้งหนี้ไปยังระบบลำดับงานโดยอัตโนมัติ คุณต้องเริ่มต้นด้วยใบแจ้งหนี้ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="be5e3-109">When you automatically submit invoices to the workflow system, you must begin with an imported invoice.</span></span> <span data-ttu-id="be5e3-110">เพื่อให้แน่ใจว่าสามารถประมวลผลใบแจ้งหนี้ตั้งแต่เริ่มต้นจนเสร็จสิ้นได้โดยไม่มีการขัดจังหวะด้วยตนเอง คุณต้องรวมงานการลงรายการบัญชีแบบอัตโนมัติในการตั้งค่าคอนฟิกลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="be5e3-110">To ensure that the invoice can be processed from start to finish without manual intervention, you must include an automated posting task in the workflow configuration.</span></span> <span data-ttu-id="be5e3-111">ใบแจ้งหนี้ที่เกี่ยวข้องกับใบสั่งซื้อ (POs) และใบแจ้งหนี้ที่มีประเภทการจัดซื้อที่ไม่มี PO และรายการที่ไม่มีสต็อก จะถูกส่งไปยังระบบลำดับงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="be5e3-111">Invoices that are related to purchase orders (POs), and invoices that contain a non-PO procurement category and non-stocked lines, can automatically be submitted to the workflow system.</span></span> <span data-ttu-id="be5e3-112">ใบแจ้งหนี้ที่ถูกป้อนด้วยตนเอง ต้องถูกส่งไปยังระบบลำดับงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="be5e3-112">Invoices that are manually entered must be manually submitted to the workflow system.</span></span>

<span data-ttu-id="be5e3-113">ค่า **ถูกส่งโดย** ในลำดับงานคือ รหัสผู้ใช้ที่ถูกป้อนสำหรับงานพื้นหลัง **ส่งใบแจ้งหนี้ของผู้จัดจำหน่ายไปยังลำดับงาน** บนหน้า **ระบบอัตโนมัติของกระบวนการ**</span><span class="sxs-lookup"><span data-stu-id="be5e3-113">The **Submitted by** value in the workflow is the user ID that was entered for the **Submit vendor invoices to workflow** background task on the **Process automation** page.</span></span> <span data-ttu-id="be5e3-114">ผู้ใช้ที่มีรหัสผู้ใช้ที่จะสามารถเรียกคืนใบแจ้งหนี้จากระบบลำดับงานได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="be5e3-114">The user who has that user ID will be able to recall the invoice from the workflow system as required.</span></span>

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a><span data-ttu-id="be5e3-115">การจับคู่ใบรับสินค้าที่ลงรายการบัญชีกับบรรทัดใบแจ้งหนี้ที่มีนโยบายการจับคู่สามทาง</span><span class="sxs-lookup"><span data-stu-id="be5e3-115">Matching posted product receipts to invoice lines that have a three-way matching policy</span></span>

<span data-ttu-id="be5e3-116">โดยเป็นส่วนหนึ่งของกระบวนการออกใบแจ้งหนี้ของบัญชีเจ้าหนี้ระยะไกล ระบบจะสามารถจับคู่การรับสินค้าที่ลงรายการบัญชีกับรายการใบแจ้งหนี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="be5e3-116">As part of a touchless Accounts payable invoicing process, the system can automatically match posted product receipts to invoice lines.</span></span> <span data-ttu-id="be5e3-117">ต้องมีการกำหนดนโยบายการจับคู่สามทางสำหรับงานนี้</span><span class="sxs-lookup"><span data-stu-id="be5e3-117">A three-way matching policy must be defined for this task.</span></span> <span data-ttu-id="be5e3-118">คุณลักษณะนี้จะพร้อมใช้งาน ถ้าคุณลักษณะ **ระบบอัตโนมัติของใบแจ้งหนี้ของผู้จัดจำหน่าย** ถูกเปิดใช้งานบนหน้า **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="be5e3-118">This feature is available if the **Vendor invoice automation** feature has been enabled on the **Feature management** page.</span></span>

<span data-ttu-id="be5e3-119">กระบวนการนี้จะรันจนกว่าปริมาณในใบรับสินค้าที่ตรงกันเท่ากับปริมาณในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="be5e3-119">The process will run until the matched product receipt quantity equals the invoice quantity.</span></span> <span data-ttu-id="be5e3-120">โดยเป็นส่วนหนึ่งของกระบวนการนี้ คุณสามารถระบุจำนวนครั้งสูงสุดที่ระบบควรพยายามจับคู่ใบรับสินค้ากับบรรทัดใบแจ้งหนี้ก่อนที่จะสรุปว่ากระบวนการล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="be5e3-120">As part of this process, you can specify the maximum number of times that the system should try to match product receipts to an invoice line before it concludes that the process failed.</span></span> <span data-ttu-id="be5e3-121">กระบวนการนี้จะรันในพื้นหลัง ทั้งรายชั่วโมงหรือรายวัน</span><span class="sxs-lookup"><span data-stu-id="be5e3-121">The process will run in the background, either hourly or daily.</span></span> <span data-ttu-id="be5e3-122">คุณสามารถรันกระบวนการจับคู่อัตโนมัติโดยเป็นส่วนหนึ่งของกระบวนการสำหรับการส่งใบแจ้งหนี้ไปยังระบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="be5e3-122">You can run the automated matching process as part of the process for submitting invoices to the workflow system.</span></span> <span data-ttu-id="be5e3-123">อีกทางหนึ่ง คือคุณสามารถรันเป็นกระบวนการแบบสแตนด์อโลน</span><span class="sxs-lookup"><span data-stu-id="be5e3-123">Alternatively, you can run it as a standalone process.</span></span> <span data-ttu-id="be5e3-124">คุณสามารถตั้งค่าคอนฟิกการตั้งค่าสำหรับกระบวนการจับคู่ใบรับสินค้ากับรายการใบแจ้งหนี้บนแท็บ **ระบบอัตโนมัติของใบแจ้งหนี้ของผู้จัดจำหน่าย** ของหน้า **พารามิเตอร์บัญชีเจ้าหนี้** (**บัญชีเจ้าหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีเจ้าหนี้**)</span><span class="sxs-lookup"><span data-stu-id="be5e3-124">The settings for the match-product-receipts-to-invoice-lines process are configured on the **Vendor invoice automation** tab of the **Accounts payable parameters** page (**Accounts payable \> Setup \> Accounts payable parameters**).</span></span>

<span data-ttu-id="be5e3-125">บรรทัดใบแจ้งหนี้ที่มีนโยบายการจับคู่สามทาง ที่ซึ่งปริมาณการรับสินค้าที่ตรงกันน้อยกว่าปริมาณในใบแจ้งหนี้ จะถูกรวมอยู่ในกระบวนจับคู่กับใบรับสินค้าแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="be5e3-125">Invoice lines that have a three-way matching policy, where the matched receipt quantity is less than the invoice quantity, will be included in the automated match-to-product-receipt process.</span></span>

<span data-ttu-id="be5e3-126">เมื่อต้องการดูสถานะ **การจับคู่ล่าสุด** สำหรับใบแจ้งหนี้ที่ไม่ได้เป็นส่วนหนึ่งของกระบวนการส่งไปยังลำดับงานแบบอัตโนมัติ ให้เปิดใบแจ้งหนี้จากหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="be5e3-126">To view the **Last match** status for invoices that aren't part of the automated submit-to-workflow process, open the invoice from the **Vendor invoices** page.</span></span> <span data-ttu-id="be5e3-127">เมื่อคุณดูใบแจ้งหนี้ จะมีการอัพเดตข้อมูลการตรวจสอบความถูกต้องของการจับคู่</span><span class="sxs-lookup"><span data-stu-id="be5e3-127">When you view the invoice, the matching validation information is updated.</span></span>

<span data-ttu-id="be5e3-128">บรรทัดใบแจ้งหนี้จะถูกแยกออกจากการประมวลผลแบบอัตโนมัติ ถ้าเป็นไปตามเงื่อนไขใดๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="be5e3-128">An invoice line will be excluded from the automated processing if any of the following conditions are met:</span></span>

- <span data-ttu-id="be5e3-129">ค่า **สถานะการจับคู่การรับสินค้าแบบอัตโนมัติ** ของบรรทัดใบแจ้งหนี้ **ล้มเหลว**</span><span class="sxs-lookup"><span data-stu-id="be5e3-129">The **Automated receipt match status** value of the invoice line is **Failed**.</span></span>
- <span data-ttu-id="be5e3-130">มีการใช้ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="be5e3-130">The invoice is being used.</span></span>
- <span data-ttu-id="be5e3-131">ใบแจ้งหนี้อยู่ในระบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="be5e3-131">The invoice is in the workflow system.</span></span>
