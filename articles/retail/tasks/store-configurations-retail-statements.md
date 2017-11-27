--- 
title: " การตั้งค่าคอนฟิกการจัดเก็บสำหรับใบแจ้งยอดการขายปลีก"
description: "กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกร้านค้าปลีกที่มีผลต่อการสร้างและลงใบแจ้งยอดของการขายปลีก "
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 45aa0caf6fcef4cc49952557a251dd78f816125e
ms.contentlocale: th-th
ms.lasthandoff: 11/14/2017

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="b95ed-103"> การตั้งค่าคอนฟิกการจัดเก็บสำหรับใบแจ้งยอดการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="b95ed-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b95ed-104">กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกร้านค้าปลีกที่มีผลต่อการสร้างและลงใบแจ้งยอดของการขายปลีก </span><span class="sxs-lookup"><span data-stu-id="b95ed-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="b95ed-105">มิติทางการเงินในร้านค้าปลีกจะถูกดำเนินการในกระบวนการอื่น </span><span class="sxs-lookup"><span data-stu-id="b95ed-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="b95ed-106">ขั้นตอนนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="b95ed-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="b95ed-107">ไปยังการขายปลีกและการค้า > ช่องทาง > ร้านค้าปลีก > ร้านค้าปลีกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b95ed-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="b95ed-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b95ed-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b95ed-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b95ed-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b95ed-110">การตั้งค่าในส่วนของใบแจ้งยอด/การปิดบัญชี มีผลกระทบต่อการสร้าง การตรวจสอบ และการลงรายการบัญชีใบแจ้งยอดสำหรับร้านค้า </span><span class="sxs-lookup"><span data-stu-id="b95ed-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="b95ed-111">เปิดส่วนใบแจ้งยอด/การปิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="b95ed-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="b95ed-112">เลือกวิธีการที่คุณต้องการใช้เพื่อจัดกลุ่มรายการใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="b95ed-112">Select the method you want to use to group the statement lines by.</span></span>  
    * <span data-ttu-id="b95ed-113">เลือก "ใช่" ถ้าควรมีเพียงใบแจ้งยอดเดียวที่ถูกสร้างขึ้นต่อวันเมื่อมีการสร้างใบแจ้งยอดจากชุดงานของการสร้างใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="b95ed-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="b95ed-114">ฟิลด์การคำนวณการตรวจนับเงินจะกำหนดว่าการตรวจนับเงินควรถูกเพิ่มรวมกันหรือไม่ หรือว่าอันล่าสุดควรจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="b95ed-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="b95ed-115">เลือกบัญชีแยกประเภทเพื่อจะลงรายการบัญชีผลต่างการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="b95ed-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="b95ed-116">ในฟิลด์การปัดเศษผลต่างสูงสุด คุณสามารถป้อนการปัดเศษผลต่างสูงสุดที่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="b95ed-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="b95ed-117">ในฟิลด์การลงรายการบัญชี คุณสามารถป้อนผลรวมสูงสุดที่ลงรายการบัญชีผลต่างที่อนุญาตสำหรับใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="b95ed-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="b95ed-118">ในฟิลด์กะ คุณสามารถป้อนผลต่างรวมสูงสุดภายในกะในใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="b95ed-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="b95ed-119">ในฟิลด์ธุรกรรม คุณสามารถป้อนผลต่างรวมสูงสุดในบรรทัดรายการใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="b95ed-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="b95ed-120">ในฟิลด์วิธีการปิดบัญชี คุณสามารถกำหนดว่าธุรกรรมที่จะถูกรวมอยู่ในใบแจ้งยอดควรเป็นส่วนหนึ่งของกะที่ปิดแล้วหรือไม่ หรือว่าสามารถจะมีเป็นธุรกรรมใดๆ ภายในช่วงวัน/เวลาที่กำหนดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b95ed-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="b95ed-121">ในฟิลด์วันสิ้นสุดธุรกิจ คุณสามารถป้อนเวลาว่าธุรกรรมที่เกิดขึ้นหลังเที่ยงคืนควรจะถูกลงรายการบัญชีรวมกับวันก่อนหน้านี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="b95ed-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="b95ed-122">เลือก "ใช่" ถ้าธุรกรรมที่เกิดขึ้นหลังเที่ยงคืนควรจะถูกลงรายการบัญชีเป็นส่วนหนึ่งของวันก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b95ed-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="b95ed-123">เลือก "ใช่" เพื่อสร้างใบแจ้งยอดขึ้นมาสำหรับแต่ละวิธีการจัดทำใบแจ้งยอดที่กำหนดไว้ </span><span class="sxs-lookup"><span data-stu-id="b95ed-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="b95ed-124">นี่จะเป็นประโยชน์ถ้าประสิทธิภาพการทำงานของการลงรายการบัญชีจำเป็นต้องได้รับการพัฒนาสำหรับร้านค้าที่มีปริมาณธุรกรรมที่สูง เพราะมันจะสร้างใบแจ้งยอดที่เล็กลงจำนวนมากที่สามารถประมวลผลพร้อมกันได้</span><span class="sxs-lookup"><span data-stu-id="b95ed-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="b95ed-125">ในฟิลด์ลูกค้าเริ่มต้น คุณสามารถเลือกบัญชีลูกค้าที่จะใช้สำหรับการขายให้แก่ลูกค้า walk-in</span><span class="sxs-lookup"><span data-stu-id="b95ed-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


