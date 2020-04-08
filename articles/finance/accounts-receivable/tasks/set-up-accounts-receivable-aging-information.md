---
title: ตั้งค่าและสร้างข้อมูลอายุหนี้ของบัญชีลูกหนี้
description: 'คู่มือนี้จะช่วยคุณตั้งค่าข้อกำหนดรอบระยะเวลาอายุหนี้ ยอดดุลลูกค้าตามอายุหนี้ และดูยอดดุลในรายการยอดดุลตามอายุหนี้และหน้าการเรียกเก็บเงิน '
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e3c1ec73da27a08aa7a6cd859d1adac772916e4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140198"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="704eb-103">ตั้งค่าและสร้างข้อมูลอายุหนี้ของบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="704eb-103">Set up and generate accounts receivable aging information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="704eb-104">คู่มือนี้จะช่วยคุณตั้งค่าข้อกำหนดรอบระยะเวลาอายุหนี้ ยอดดุลลูกค้าตามอายุหนี้ และดูยอดดุลในรายการยอดดุลตามอายุหนี้และหน้าการเรียกเก็บเงิน </span><span class="sxs-lookup"><span data-stu-id="704eb-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="704eb-105">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="704eb-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="704eb-106">สร้างข้อกำหนดรอบระยะเวลาอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="704eb-106">Create an aging period definition</span></span>
1. <span data-ttu-id="704eb-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล > สินเชื่อและการเรียกเก็บเงิน > การตั้งค่า > ข้อกำหนดรอบระยะเวลาอายุหนี้**</span><span class="sxs-lookup"><span data-stu-id="704eb-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Aging period definitions**.</span></span>
2. <span data-ttu-id="704eb-108">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="704eb-108">Click **New**.</span></span>
3. <span data-ttu-id="704eb-109">ในฟิลด์ **ข้อกำหนดรอบระยะเวลาอายุหนี้** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="704eb-109">In the **Aging period definition** field, type a value.</span></span>
4. <span data-ttu-id="704eb-110">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="704eb-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="704eb-111">คลิก **เพิ่มที่ด้านล่าง** เพื่อแทรกรอบระยะเวลาอายุหนี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="704eb-111">Click **Add below** to insert a new aging period.</span></span>
6. <span data-ttu-id="704eb-112">ในฟิลด์ **รอบระยะเวลา** ให้ป้อนคำอธิบายที่จะแสดงบนรายงานอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="704eb-112">In the **Period** field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="704eb-113">ในฟิลด์ **หน่วย** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="704eb-113">In the **Unit** field, enter a number.</span></span>
8. <span data-ttu-id="704eb-114">ในฟิลด์ **ช่วงเวลา** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="704eb-114">In the **Interval** field, select an option.</span></span> <span data-ttu-id="704eb-115">รอบระยะเวลาบัญชีแยกประเภทที่ตรงกับรอบระยะเวลาปฏิทินบัญชีแยกประเภทของคุณ </span><span class="sxs-lookup"><span data-stu-id="704eb-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="704eb-116">วัน สัปดาห์ เดือน ไตรมาส และปี จะกำหนดขนาดของช่วงเวลาตามชนิดของวันที่ </span><span class="sxs-lookup"><span data-stu-id="704eb-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="704eb-117">ไม่จำกัดการเลือกธุรกรรมทั้งหมดก่อนหรือหลังจากรอบระยะเวลาก่อนหน้า ขึ้นอยู่กับว่าเป็นรอบระยะเวลาแรกหรือสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="704eb-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="704eb-118">ในฟิลด์ **ตัวบ่งชี้อายุหนี้** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="704eb-118">In the **Aging indicator** field, select an option.</span></span>
10. <span data-ttu-id="704eb-119">เลือกรอบระยะเวลาที่ด้านบนของกริด </span><span class="sxs-lookup"><span data-stu-id="704eb-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="704eb-120">อัพเดตคำอธิบายเพื่ออธิบายรอบระยะเวลาที่เก่าที่สุดในการกำหนดรอบระยะเวลาอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="704eb-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="704eb-121">ในฟิลด์ **รอบระยะเวลา** ให้ป้อนคำอธิบายใหม่ของรอบระยะเวลาอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="704eb-121">In the **Period** field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="704eb-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="704eb-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="704eb-123">อายุหนี้ของยอดดุล</span><span class="sxs-lookup"><span data-stu-id="704eb-123">Age the balances</span></span>
1. <span data-ttu-id="704eb-124">ไปที่ **สินเชื่อและการเรียกเก็บเงิน > งานประจำงวด > ยอดดุลของลูกค้าตามอายุหนี้**</span><span class="sxs-lookup"><span data-stu-id="704eb-124">Go to **Credit and collections > Periodic tasks > Age customer balances**.</span></span>
2. <span data-ttu-id="704eb-125">ในฟิลด์ **ข้อกำหนดรอบระยะเวลาอายุหนี้** ให้เลือกข้อกำหนดรอบระยะเวลาอายุหนี้ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="704eb-125">In the **Aging period definition** field, select the aging period definition that you created.</span></span>
    + <span data-ttu-id="704eb-126">คุณสามารถมีหนึ่งสแนปช็อตที่ใช้งานอยู่สำหรับแต่ละการกำหนดรอบระยะเวลาอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="704eb-126">You can have one active snapshot for each aging period definition.</span></span>  
    + <span data-ttu-id="704eb-127">ลูกค้าทั้งหมดถูกประมวลผลโดยค่าเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="704eb-127">All customers are processed by default.</span></span> <span data-ttu-id="704eb-128">คุณสามารถใช้การเลือกนี้ในการคำนวณกลุ่มลูกค้าเดี่ยว</span><span class="sxs-lookup"><span data-stu-id="704eb-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    + <span data-ttu-id="704eb-129">เลือกวันที่จากธุรกรรมที่คุณจะใช้สำหรับอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="704eb-129">Select the date from the transaction that you will use for the aging.</span></span>  
    + <span data-ttu-id="704eb-130">เลือกวันที่ "ณ วันที่" สำหรับอายุหนี้ </span><span class="sxs-lookup"><span data-stu-id="704eb-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="704eb-131">ค่าเริ่มต้นเป็นวันนี้ แต่ถ้าคุณเปลี่ยนฟิลด์นี้เป็นวันที่ที่เลือก คุณจะสามารถเลือกวันที่คุณต้องการ </span><span class="sxs-lookup"><span data-stu-id="704eb-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="704eb-132">สำหรับการประมวลผลชุดงานจะใช้วันที่ของวันนี้</span><span class="sxs-lookup"><span data-stu-id="704eb-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="704eb-133">ขยายช่วง **บริษัท**</span><span class="sxs-lookup"><span data-stu-id="704eb-133">Expand the **Company** range.</span></span> <span data-ttu-id="704eb-134">คุณสามารถเลือกบริษัทที่จะถูกรวมอยู่ในสแนปช็อต </span><span class="sxs-lookup"><span data-stu-id="704eb-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="704eb-135">บริษัทปัจจุบันจะถูกเลือกโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="704eb-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="704eb-136">คลิก **ตกลง** เพื่อประมวลผลสแนปช็อต</span><span class="sxs-lookup"><span data-stu-id="704eb-136">Click **Ok** to process the snapshot.</span></span> <span data-ttu-id="704eb-137">ซึ่งจะใช้เวลารสักครู่ ดังนั้นให้รอจนตัวเลื่อนหายไปและเช็คศูนย์กลางข้อความสำหรับข้อความ</span><span class="sxs-lookup"><span data-stu-id="704eb-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="704eb-138">ดูยอดดุลในรายการยอดดุลตามอายุหนี้และในหน้าการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="704eb-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="704eb-139">ไปที่ **สินเชื่อและการเรียกเก็บเงิน > การเรียกเก็บเงิน > ยอดดุลตามอายุหนี้**</span><span class="sxs-lookup"><span data-stu-id="704eb-139">Go to **Credit and collections > Collections > Aged balances**.</span></span> <span data-ttu-id="704eb-140">หน้ารายการแสดงยอดดุลสำหรับลูกค้า </span><span class="sxs-lookup"><span data-stu-id="704eb-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="704eb-141">ไอคอนอายุหนี้แสดงรอบระยะเวลาอายุหนี้สำหรับธุรกรรมที่เก่าที่สุด</span><span class="sxs-lookup"><span data-stu-id="704eb-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="704eb-142">เลือกลูกค้าที่มียอดดุล</span><span class="sxs-lookup"><span data-stu-id="704eb-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="704eb-143">ขยายพื้นที่กล่องแสดง **ข้อมูลย่ออายุหนี้** เพื่อดูยอดดุลตามอายุหนี้</span><span class="sxs-lookup"><span data-stu-id="704eb-143">Expand the **Aging fact** box area to view the aged balances.</span></span> <span data-ttu-id="704eb-144">การกำหนดรอบระยะเวลาอายุหนี้สำหรับกล่องแสดงข้อมูลย่อจะนำมาจากค่าเริ่มต้นของข้อกำหนดรอบระยะเวลาอายุหนี้ที่ระบุในพารามิเตอร์ </span><span class="sxs-lookup"><span data-stu-id="704eb-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="704eb-145">คุณสามารถเปลี่ยนโดยใช้เมนูการรวบรวม</span><span class="sxs-lookup"><span data-stu-id="704eb-145">You can change it using the Collect menu.</span></span>  

