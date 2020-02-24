---
title: " การตั้งค่าคอนฟิกการชำระเงินสำหรับใบแจ้งยอดการขายปลีก"
description: กระบวนการนี้แสดงให้เห็นถึงการกำหนดค่าสำหรับวิธีการชำระเงินของร้านค้าเชิงพาณิชย์ที่มีผลต่อการสร้างและโพสต์คำชี้แจง
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72425526a4425eeb5cb7539f9633bda5657ca99e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024182"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="e28d4-103"> การตั้งค่าคอนฟิกการชำระเงินสำหรับใบแจ้งยอดการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="e28d4-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e28d4-104">กระบวนการนี้แสดงให้เห็นถึงการกำหนดค่าสำหรับวิธีการชำระเงินของร้านค้าเชิงพาณิชย์ที่มีผลต่อการสร้างและโพสต์คำชี้แจง</span><span class="sxs-lookup"><span data-stu-id="e28d4-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="e28d4-105">การบันทึกนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="e28d4-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="e28d4-106">ไปยัง การขายปลีกและการค้า > ช่องทาง > ร้านค้า > ร้านค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e28d4-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="e28d4-107">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="e28d4-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e28d4-108">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e28d4-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e28d4-109">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="e28d4-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="e28d4-110">คลิกวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="e28d4-110">Click Payment methods.</span></span>
6. <span data-ttu-id="e28d4-111">ขยายหรือยุบส่วนการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="e28d4-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="e28d4-112">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="e28d4-112">Click Edit.</span></span>
    * <span data-ttu-id="e28d4-113">เลือกว่ายอดเงินที่ได้รับสำหรับวิธีการชำระเงินนี้ควรจะถูกลงไปยังบัญชีแยกประเภทหรือบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="e28d4-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="e28d4-114">เลือกบัญชีที่ยอดเงินที่ได้รับสำหรับวิธีการชำระเงินนี้ควรจะถูกลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="e28d4-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="e28d4-115">เลือกบัญชีที่จะลงรายการบัญชีผลต่างที่เป็นไปได้ระหว่างยอดเงินรวมของธุรกรรมที่ได้รับและยอดเงินที่ตรวจนับสำหรับวิธีการชำระเงินนี้</span><span class="sxs-lookup"><span data-stu-id="e28d4-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="e28d4-116">ในฟิลด์นี้ คุณสามารถป้อนยอดเงินเพื่อควบคุมเมื่อยอดเงินที่แตกต่างควรถูกลงรายการบัญชีไปยังบัญชีอื่น </span><span class="sxs-lookup"><span data-stu-id="e28d4-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="e28d4-117">คุณสามารถใช้ข้อมูลนี้ในการติดตามความแตกต่างที่มาก</span><span class="sxs-lookup"><span data-stu-id="e28d4-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="e28d4-118">เลือกบัญชีที่จะลงรายการบัญชีผลต่างที่เป็นไปได้ระหว่างยอดเงินรวมของธุรกรรมที่ได้รับ และยอดเงินที่ตรวจนับ เมื่อมันเกินค่าที่กำหนดไว้ในฟิลด์ "ยอดเงินผลต่างสูงสุด"</span><span class="sxs-lookup"><span data-stu-id="e28d4-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="e28d4-119">เลือก "ใช่" เพื่อลงรายการบัญชียอดการนำเงินฝากธนาคารไปยังบัญชีแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="e28d4-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="e28d4-120">ในฟิลด์นี้ คุณสามารถเลือกได้ว่าควรจะลงรายการยอดรวมนำเงินฝากธนาคารไปยังบัญชีแยกประเภทหรือบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="e28d4-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="e28d4-121">เลือกบัญชีที่จะลงรายการบัญชียอดการนำเงินฝากธนาคารเข้าไป</span><span class="sxs-lookup"><span data-stu-id="e28d4-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="e28d4-122">เลือกชนิดธุรกรรมธนาคารที่จะใช้เมื่อลงรายการบัญชียอดเงินฝากธนาคารไปยังบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="e28d4-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="e28d4-123">เลือก "ใช่" เพื่อลงรายการบัญชียอดการนำเงินฝากเข้าเซฟไปยังบัญชีแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="e28d4-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="e28d4-124">เลือกว่าควรจะลงรายการยอดรวมนำเงินฝากเข้าเซฟไปยังบัญชีแยกประเภทหรือบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="e28d4-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="e28d4-125">เลือกบัญชีเพื่อลงรายการบัญชียอดการนำเงินฝากเข้าเซฟเข้าไป</span><span class="sxs-lookup"><span data-stu-id="e28d4-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="e28d4-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e28d4-126">Click Save.</span></span>

