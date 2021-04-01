---
title: " การตั้งค่าคอนฟิกการจัดเก็บสำหรับใบแจ้งยอดการขายปลีก"
description: กระบวนงานนี้นำไปสู่การตั้งค่าคอนฟิกสำหรับร้านค้าที่มีผลต่อการสร้างและลงใบแจ้งยอดของ Commerce
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1670a1a102f9288cdbd0e4cc981e3aa927d1ad9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232676"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="c68f2-103"> การตั้งค่าคอนฟิกการจัดเก็บสำหรับใบแจ้งยอดการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="c68f2-103">Store configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c68f2-104">กระบวนงานนี้นำไปสู่การตั้งค่าคอนฟิกสำหรับร้านค้าที่มีผลต่อการสร้างและลงใบแจ้งยอดของ Commerce</span><span class="sxs-lookup"><span data-stu-id="c68f2-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="c68f2-105">มิติทางการเงินในร้านค้าจะถูกครอบคลุมในกระบวนงานอื่น</span><span class="sxs-lookup"><span data-stu-id="c68f2-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="c68f2-106">ขั้นตอนนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="c68f2-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="c68f2-107">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > Retail และ Commerce > ช่องทาง > ร้านค้า > ร้านค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="c68f2-107">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="c68f2-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c68f2-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c68f2-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c68f2-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c68f2-110">คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="c68f2-110">Click **Edit**.</span></span>
5. <span data-ttu-id="c68f2-111">การตั้งค่าในแท็บด่วน **ใบแจ้งยอด/การปิด** มีผลกระทบต่อการสร้าง การตรวจสอบ และการลงรายการบัญชีใบแจ้งยอดสำหรับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="c68f2-111">The settings in the **Statement/closing** FastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="c68f2-112">ขยายแท็บด่วน **ใบแจ้งยอด/การปิดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="c68f2-112">Expand the **Statement/closing** FastTab.</span></span>  
6. <span data-ttu-id="c68f2-113">ในฟิลด์ **วิธีการจัดทำใบแจ้งยอด** เลือกวิธีการที่คุณต้องการใช้เพื่อจัดกลุ่มรายการใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="c68f2-113">In the **Statement method** field, select the method you want to use to group the statement lines by.</span></span>  
7. <span data-ttu-id="c68f2-114">เลือก "ใช่" ใน **ใบแจ้งยอดหนึ่งใบต่อวัน** ถ้าควรมีเพียงใบแจ้งยอดเดียวที่ถูกสร้างขึ้นต่อวัน เมื่อมีการสร้างใบแจ้งยอดจากชุดงานของการสร้างใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="c68f2-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="c68f2-115">ฟิลด์ **การคำนวณการตรวจนับเงิน** จะกำหนดว่าการตรวจนับเงินควรถูกเพิ่มรวมกันหรือไม่ หรือว่ารายการล่าสุดควรจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="c68f2-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="c68f2-116">ในฟิลด์ **การปัดเศษ** เลือกบัญชีแยกประเภทที่จะลงรายการบัญชีผลต่างการปัดเศษ</span><span class="sxs-lookup"><span data-stu-id="c68f2-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="c68f2-117">ในฟิลด์ **ผลต่างการปัดเศษสูงสุด** ป้อนผลต่างสูการปัดเศษงสุดที่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="c68f2-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="c68f2-118">ในฟิลด์ **การลงรายการบัญชี** ป้อนผลต่างการลงรายการบัญชีรวมสูงสุดที่อนุญาตสำหรับใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="c68f2-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="c68f2-119">ในฟิลด์ **กะ** คุณสามารถป้อนผลต่างรวมสูงสุดภายในกะในใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="c68f2-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="c68f2-120">ในฟิลด์ **ธุรกรรม** ป้อนผลต่างรวมสูงสุดในรายการใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="c68f2-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="c68f2-121">ในฟิลด์ **วิธีการปิดบัญชี** กำหนดว่าธุรกรรมที่จะถูกรวมอยู่ในใบแจ้งยอดควรเป็นส่วนหนึ่งของกะที่ปิดแล้วหรือไม่ หรือว่าสามารถจะเป็นธุรกรรมใดๆ ภายในช่วงวันที่/เวลาที่กำหนดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c68f2-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="c68f2-122">ในฟิลด์ **เวลาสิ้นสุดวันทำการ** ป้อนเวลาว่าธุรกรรมที่เกิดขึ้นหลังเที่ยงคืนควรจะถูกลงรายการบัญชีรวมกับวันก่อนหน้านี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c68f2-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="c68f2-123">เลือก "ใช่" ใน **ลงรายการบัญชีเป็นวันทำการ** ถ้าธุรกรรมที่เกิดขึ้นหลังเที่ยงคืนควรจะถูกลงรายการบัญชีเป็นส่วนหนึ่งของวันก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="c68f2-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="c68f2-124">เลือก "ใช่" ใน **แยกตามวิธีการจัดทำใบแจ้งยอด** เพื่อสร้างใบแจ้งยอดขึ้นมาสำหรับวิธีการจัดทำใบแจ้งยอดแต่ละวิธีที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="c68f2-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="c68f2-125">การดำเนินการนี้จะเป็นประโยชน์ถ้าประสิทธิภาพการทำงานของการลงรายการบัญชีจำเป็นต้องได้รับการพัฒนาสำหรับร้านค้าที่มีปริมาณธุรกรรมที่สูง เพราะจะสร้างใบแจ้งยอดที่เล็กลงจำนวนมากที่สามารถประมวลผลพร้อมกันได้</span><span class="sxs-lookup"><span data-stu-id="c68f2-125">This action can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="c68f2-126">ในแท็บด่วน **ทั่วไป** ในฟิลด์ **ลูกค้าเริ่มต้น** คุณสามารถเลือกบัญชีลูกค้าที่จะใช้สำหรับการขายให้แก่ลูกค้าที่เข้ามาในร้าน</span><span class="sxs-lookup"><span data-stu-id="c68f2-126">In the **General** FastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]