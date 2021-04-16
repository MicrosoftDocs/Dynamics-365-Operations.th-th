---
title: แบ่งค่าธรรมเนียมส่วนหัวตามส่วนไปยังรายการขายที่ตรงกัน
description: หัวข้อนี้อธิบายความสามารถเพิ่มเติมสำหรับการคำนวณและการนำค่าธรรมเนียมอัตโนมัติไปใช้กับใบสั่งช่องทาง Commerce โดยใช้คุณลักษณะค่าธรรมเนียมอัตโนมัติขั้นสูง
author: hhaines
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 22939e8fd63a355effecf0c16fecd20377faa3a6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791065"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a><span data-ttu-id="23df0-103">แบ่งค่าธรรมเนียมส่วนหัวตามส่วนไปยังรายการขายที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="23df0-103">Prorate header charges to matching sales lines</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="23df0-104">หัวข้อนี้อธิบายถึงฟังก์ชันสำหรับการจัดกลุ่มค่าธรรมเนียมอัตโนมัติในระดับส่วนหัว และการคิดตามสัดส่วนกับรายการค้า</span><span class="sxs-lookup"><span data-stu-id="23df0-104">This topic describes the functionality for grouping header-level auto-charges and prorating them to commerce sales lines.</span></span> <span data-ttu-id="23df0-105">ฟังก์ชันนี้จะพร้อมใช้งานสำหรับธุรกรรมที่ถูกสร้างขึ้นที่การขายหน้าร้าน (POS) ในรุ่นการขายปลีก 10.0.1 และการขายที่ถูกสร้างขึ้นในศูนย์บริการในรุ่นการขายปลีก 10.0.2</span><span class="sxs-lookup"><span data-stu-id="23df0-105">This functionality is available for transactions that are created at the point of sale (POS) in Retail version 10.0.1 and sales that are created in a call center in Retail version 10.0.2.</span></span>

<span data-ttu-id="23df0-106">ฟังก์ชันนี้จะพร้อมใช้งานได้ก็ต่อเมื่อคุณลักษณะ [ค่าธรรมเนียมอัตโนมัติขั้นสูง](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) ถูกเปิดอยู่ โดยใช้ตัวเลือกในหน้า **พารามิเตอร์ Commerce**</span><span class="sxs-lookup"><span data-stu-id="23df0-106">This functionality is available only if the [advanced auto-charges](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) feature is turned on by using the option on the **Commerce parameters** page.</span></span> <span data-ttu-id="23df0-107">นอกจากนี้ วิธีการคำนวณขั้นสูงสำหรับค่าธรรมเนียมอัตโนมัติสามารถใช้ได้กับใบสั่งขายที่สร้างขึ้นโดยช่องทางการค้า (POS ศูนย์บริการ และแพลตฟอร์มพาณิชย์อิเล็กทรอนิกส์แบบไดนามิก) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="23df0-107">Additionally, the enhanced calculation method for auto-charges can be applied only to sales orders that are created through commerce channels (the POS, a call center, and the Dynamics e-Commerce platform).</span></span>

<span data-ttu-id="23df0-108">ฟังก์ชันใหม่นี้ช่วยให้องค์กรมีความยืดหยุ่นมากขึ้นในลักษณะที่ค่าธรรมเนียมอัตโนมัติระดับส่วนหัวถูกคำนวณ และถูกนำไปใช้กับธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="23df0-108">This new functionality gives organizations more flexibility in the way that header-level auto-charges are calculated and applied to sales transactions.</span></span>

<span data-ttu-id="23df0-109">ในรุ่นของแอปก่อนหน้ารุ่น 10.0.1 ค่าธรรมเนียมอัตโนมัติระดับส่วนหัวที่มีความสัมพันธ์โหมดเฉพาะของการจัดส่งจะถูกคำนวณ ก็ต่อเมื่อมีการจับคู่กับโหมดการจัดส่งที่กำหนดไว้ในส่วนหัวของใบสั่งขายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="23df0-109">In versions of the app earlier than version 10.0.1, header-level auto-charges that have a specific mode of delivery relation are calculated only when there is a match with the mode of delivery that is defined on the sales order header.</span></span>

<span data-ttu-id="23df0-110">ตัวอย่างเช่น มีการกำหนดค่าธรรมเนียมอัตโนมัติระดับส่วนหัวสำหรับโหมดของการจัดส่ง **99** และโหมดของการจัดส่ง **11**</span><span class="sxs-lookup"><span data-stu-id="23df0-110">For example, header-level auto-charges are defined for mode of delivery **99** and mode of delivery **11**.</span></span> <span data-ttu-id="23df0-111">มีการสร้างใบสั่งขาย โหมดการจัดส่ง **99** ถูกกำหนดบนส่วนหัวของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="23df0-111">A sales order is created, and mode of delivery **99** is defined on the order header.</span></span> <span data-ttu-id="23df0-112">อย่างไรก็ตาม รายการขายบางรายการถูกตั้งค่า เพื่อให้มีการจัดส่งโดยใช้โหมดการจัดส่ง **11**</span><span class="sxs-lookup"><span data-stu-id="23df0-112">However, some of the sale lines are set up so that they're shipped by using mode of delivery **11**.</span></span> <span data-ttu-id="23df0-113">ในกรณีนี้ เฉพาะค่าธรรมเนียมระดับส่วนหัวที่จะถูกเชื่อมโยงกับโหมดการจัดส่ง **99** จะถูกพิจารณา และนำไปใช้กับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="23df0-113">In this case, only the header-level charges that are linked to mode of delivery **99** are considered and applied to the sales order.</span></span>

<span data-ttu-id="23df0-114">ในการค้าค่าธรรมเนียมระดับส่วนหน้ามีคุณลักษณะเพิ่มเติมที่ช่วยให้คุณสามารถกำหนด [การตั้งค่าคอนฟิกค่าธรรมเนียมที่จัดระดับ](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) ที่เป็นไปตามมูลค่าของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="23df0-114">In Commerce, the header-level charges have an additional feature that lets you define a [tiered charge configuration](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) that is based on the order value.</span></span> <span data-ttu-id="23df0-115">ตัวอย่างเช่น ถ้ามูลค่าของใบสั่งอยู่ระหว่าง $50.00 และ $200.00 องค์กรอาจต้องการเรียกเก็บค่าธรรมเนียมการขนส่งเป็น $5.00</span><span class="sxs-lookup"><span data-stu-id="23df0-115">For example, if the order value is between $50.00 and $200.00, an organization might want to charge a freight charge of $5.00.</span></span> <span data-ttu-id="23df0-116">อย่างไรก็ตาม ถ้ามูลค่าของใบสั่งอยู่ระหว่าง $200.01 และ $500.00 ค่าธรรมเนียมการขนส่งอาจเป็น $4.00</span><span class="sxs-lookup"><span data-stu-id="23df0-116">However, if the order value is between $200.01 and $500.00, the freight charge might be $4.00.</span></span>

<span data-ttu-id="23df0-117">องค์กรบางแห่งต้องการประโยชน์ของการคำนวณค่าธรรมเนียมที่จัดระดับที่มีค่าธรรมเนียมระดับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="23df0-117">Some organizations want the benefits of the tiered charge calculation that is provided with header-level charges.</span></span> <span data-ttu-id="23df0-118">อย่างไรก็ตาม ในสถานการณ์จำลองที่เกี่ยวข้องกับโหมดการจัดส่งแบบผสม พวกเขายังต้องการให้แน่ใจว่า ค่าธรรมเนียมที่ถูกคำนวณเป็นไปตามการจับคู่กับโหมดการจัดส่งที่กำหนดไว้ในรายการขายแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="23df0-118">However, in scenarios that involve mixed modes of delivery, they also want to make sure that the charges that are calculated are based on a match with the mode of delivery that is defined on each sales line.</span></span>

<span data-ttu-id="23df0-119">ขณะนี้ คุณสามารถตั้งค่าคอนฟิกค่าธรรมเนียมอัตโนมัติระดับส่วนหัวได้ เพื่อให้โหมดการจัดส่งในใบสั่งทั้งหมดได้รับพิจารณา เมื่อมีการคำนวณค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="23df0-119">You can now configure header-level auto-charges so that all modes of delivery on the order are considered when charges are calculated.</span></span> <span data-ttu-id="23df0-120">ฟังก์ชันนี้จำเป็นต้องใช้ตรรกะการคำนวณที่ซับซ้อนมากขึ้นในการคำนวณค่าธรรมเนียมระดับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="23df0-120">This functionality requires a more complex calculation logic to calculate the header-level charges.</span></span> <span data-ttu-id="23df0-121">ตรรกะจัดกลุ่มสินค้าทั้งหมดเข้าด้วยกันที่มีการจัดส่งโดยใช้โหมดการจัดส่งเดียวกัน และถือว่ากลุ่มนั้นเป็นกลุ่มการคำนวณสำหรับรายการ เมื่อคำนวณค่าธรรมเนียมอัตโนมัติระดับส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="23df0-121">The logic groups together all the items that are shipped using the same mode of delivery, and it treats that group as the calculation group for the items when it calculates the header-level auto-charges.</span></span> <span data-ttu-id="23df0-122">สำหรับรายการที่มีโหมดการจัดส่งเดียวกัน ค่าธรรมเนียมอัตโนมัติจะถูกคำนวณตามมูลค่าการขายแบบรวมของรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="23df0-122">For items that have the same mode of delivery, auto-charges are calculated based on the combined sales value of the items.</span></span> <span data-ttu-id="23df0-123">ในวิธีนี้ มีการกำหนดระดับค่าธรรมเนียมอัตโนมัติที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="23df0-123">In this way, the appropriate auto-charge tier is determined.</span></span>

<span data-ttu-id="23df0-124">หลังจากที่มีการรับค่าธรรมเนียมระดับส่วนหัวที่เหมาะสมสำหรับรายการขายที่มีการจัดส่งโดยใช้โหมดการจัดส่งเดียวกัน ค่าธรรมเนียมที่คำนวณได้จะถูกแบ่งตามสัดส่วนจนถึงระดับรายการขาย</span><span class="sxs-lookup"><span data-stu-id="23df0-124">After the appropriate header-level charges are obtained for the sales lines that are shipped using the same mode of delivery, the calculated charges are prorated down to the sales line level.</span></span> <span data-ttu-id="23df0-125">เนื่องจากค่าธรรมเนียมเหล่านี้อยู่ในระดับรายการ และไม่ได้ถูกเก็บในระดับหัวข้อ ลิงค์เฉพาะเพิ่มเติมถูกสร้างขึ้นระหว่างรายการและค่าธรรมเนียมที่คำนวณได้สำหรับรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="23df0-125">Because these charges are at the line level and not kept at the header level, a more specific link is made between the item and the charge value that calculated for it.</span></span> <span data-ttu-id="23df0-126">ลักษณะการทำงานนี้จะมีประโยชน์ในสถานการณ์จำลองการส่งคืนบางส่วน ที่ซึ่งองค์กรต้องการขอคืนเงินเฉพาะส่วนหนึ่งของค่าธรรมเนียม แทนที่จะเป็นค่าธรรมเนียมทั้งหมดเมื่อมีการส่งคืนรายการเฉพาะบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="23df0-126">This behavior can be useful in partial return scenarios, where an organization wants to refund only part of the charge instead of the whole charge when only some items are returned.</span></span>

## <a name="scenarios"></a><span data-ttu-id="23df0-127">สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="23df0-127">Scenarios</span></span>

<span data-ttu-id="23df0-128">สถานการณ์จำลองตัวอย่างสองสถานการณ์ต่อไปนี้ ร่างวิธีการคำนวณค่าธรรมเนียมเหล่านี้ทั้งเมื่อมีการใช้ฟังก์ชันใหม่และเมื่อไม่ได้ใช้</span><span class="sxs-lookup"><span data-stu-id="23df0-128">The following two sample scenarios outline how these charges are calculated both when the new functionality is used and when it isn't used.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="23df0-129">สถานการณ์จำลอง 1</span><span class="sxs-lookup"><span data-stu-id="23df0-129">Scenario 1</span></span>

<span data-ttu-id="23df0-130">สถานการณ์จำลองนี้ร่างลักษณะการทำงานเมื่อตัวเลือก **แบ่งรายการขายที่ตรงกันตามสัดส่วน** ถูกตั้งค่าเป็น **ไม่ใช่** ในการตั้งค่าค่าธรรมเนียมอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="23df0-130">This scenario outlines the behavior when the **Pro-rate to matching sales lines** option is set to **No** in the auto-charge setup.</span></span> <span data-ttu-id="23df0-131">(ลักษณะการทำงานจะเหมือนกับลักษณะการทำงานของค่าธรรมเนียมระดับส่วนหัวในแอปรุ่นที่เก่ากว่ารุ่น 10.0.1)</span><span class="sxs-lookup"><span data-stu-id="23df0-131">(The behavior is equivalent to the behavior of header-level charges in app versions that are earlier than version 10.0.1.)</span></span>

<span data-ttu-id="23df0-132">ในสถานการณ์จำลองนี้ องค์กรได้กำหนดค่าธรรมเนียมระดับส่วนหัวสำหรับความสัมพันธ์โหมดของการจัดส่ง **99** และความสัมพันธ์โหมดของการจัดส่ง **11**</span><span class="sxs-lookup"><span data-stu-id="23df0-132">In this scenario, the organization has defined header-level charges for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="23df0-133">ไม่มีค่าธรรมเนียมอัตโนมัติถูกตั้งค่าคอนฟิกสำหรับโหมดของการจัดส่ง **21**</span><span class="sxs-lookup"><span data-stu-id="23df0-133">No auto-charges are configured for mode of delivery **21**.</span></span>

![ค่าธรรมเนียมอัตโนมัติสำหรับโหมดของการจัดส่ง 99 เมื่อปิดการแบ่งตามสัดส่วนของรายการที่ตรงกัน](media/99_disabled.png)

![ค่าธรรมเนียมอัตโนมัติสำหรับโหมดของการจัดส่ง 11 เมื่อปิดการแบ่งตามสัดส่วนของรายการที่ตรงกัน](media/11_disabled.png)

<span data-ttu-id="23df0-136">ใบสั่งขายถูกสร้างขึ้นในศูนย์บริการ และโหมดของการจัดส่งถูกกำหนดเป็น **99**</span><span class="sxs-lookup"><span data-stu-id="23df0-136">A sales order is created in the call center, and the mode of delivery is set to **99**.</span></span> <span data-ttu-id="23df0-137">ใบสั่งนี้ประกอบด้วยห้ารายการ</span><span class="sxs-lookup"><span data-stu-id="23df0-137">This order contains five items.</span></span> <span data-ttu-id="23df0-138">รายการใบสั่งสองรายการได้ถูกตั้งค่าคอนฟิกเพื่อใช้โหมดของการจัดส่ง **99** รายการสองรายการได้ถูกตั้งค่าคอนฟิกเพื่อใช้โหมดของการจัดส่ง **11** และรายการหนึ่งรายการได้ถูกตั้งค่าคอนฟิกเพื่อใช้โหมดของการจัดส่ง **21** ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="23df0-138">Two order lines have been configured to use mode of delivery **99**, two lines have been configured to use mode of delivery **11**, and one line has been configured to use mode of delivery **21**, as shown in the following table.</span></span>

| <span data-ttu-id="23df0-139">สินค้า</span><span class="sxs-lookup"><span data-stu-id="23df0-139">Item</span></span>  | <span data-ttu-id="23df0-140">ปริมาณในรายการ</span><span class="sxs-lookup"><span data-stu-id="23df0-140">Line quantity</span></span> | <span data-ttu-id="23df0-141">วิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="23df0-141">Delivery mode</span></span> | <span data-ttu-id="23df0-142">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="23df0-142">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="23df0-143">81331</span><span class="sxs-lookup"><span data-stu-id="23df0-143">81331</span></span> | <span data-ttu-id="23df0-144">1</span><span class="sxs-lookup"><span data-stu-id="23df0-144">1</span></span>             | <span data-ttu-id="23df0-145">11</span><span class="sxs-lookup"><span data-stu-id="23df0-145">11</span></span>            | <span data-ttu-id="23df0-146">$10</span><span class="sxs-lookup"><span data-stu-id="23df0-146">$10</span></span>            |
| <span data-ttu-id="23df0-147">81332</span><span class="sxs-lookup"><span data-stu-id="23df0-147">81332</span></span> | <span data-ttu-id="23df0-148">1</span><span class="sxs-lookup"><span data-stu-id="23df0-148">1</span></span>             | <span data-ttu-id="23df0-149">99</span><span class="sxs-lookup"><span data-stu-id="23df0-149">99</span></span>            | <span data-ttu-id="23df0-150">$50</span><span class="sxs-lookup"><span data-stu-id="23df0-150">$50</span></span>            |
| <span data-ttu-id="23df0-151">81333</span><span class="sxs-lookup"><span data-stu-id="23df0-151">81333</span></span> | <span data-ttu-id="23df0-152">2</span><span class="sxs-lookup"><span data-stu-id="23df0-152">2</span></span>             | <span data-ttu-id="23df0-153">11</span><span class="sxs-lookup"><span data-stu-id="23df0-153">11</span></span>            | <span data-ttu-id="23df0-154">$30</span><span class="sxs-lookup"><span data-stu-id="23df0-154">$30</span></span>            |
| <span data-ttu-id="23df0-155">81334</span><span class="sxs-lookup"><span data-stu-id="23df0-155">81334</span></span> | <span data-ttu-id="23df0-156">3</span><span class="sxs-lookup"><span data-stu-id="23df0-156">3</span></span>             | <span data-ttu-id="23df0-157">99</span><span class="sxs-lookup"><span data-stu-id="23df0-157">99</span></span>            | <span data-ttu-id="23df0-158">$10</span><span class="sxs-lookup"><span data-stu-id="23df0-158">$10</span></span>            |
| <span data-ttu-id="23df0-159">81334</span><span class="sxs-lookup"><span data-stu-id="23df0-159">81334</span></span> | <span data-ttu-id="23df0-160">3</span><span class="sxs-lookup"><span data-stu-id="23df0-160">3</span></span>             | <span data-ttu-id="23df0-161">21</span><span class="sxs-lookup"><span data-stu-id="23df0-161">21</span></span>            | <span data-ttu-id="23df0-162">$5</span><span class="sxs-lookup"><span data-stu-id="23df0-162">$5</span></span>             |

<span data-ttu-id="23df0-163">ในสถานการณ์จำลองนี้ มีการประเมินใบสั่งทั้งหมดตามตารางค่าธรรมเนียมอัตโนมัติสำหรับโหมดการจัดส่ง **99**</span><span class="sxs-lookup"><span data-stu-id="23df0-163">In this scenario, the whole order is evaluated against the auto-charge table for mode of delivery **99**.</span></span> <span data-ttu-id="23df0-164">ผลรวมทั้งหมดของรายการขายทั้งหมดจะถูกใช้เพื่อกำหนดระดับที่ตรงกันในการตั้งค่าคอนฟิกค่าธรรมเนียมอัตโนมัติ และมีการใช้ค่าธรรมเนียมนี้ในระดับส่วนหัวของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="23df0-164">The full total of all sales lines is used to determine a matching tier in the auto-charge configuration, and this charge is applied at the order header level.</span></span> <span data-ttu-id="23df0-165">ในตัวอย่างนี้ ยอดรวมในใบสั่งคือ $165.00 และค่าธรรมเนียมการขนส่ง $15.00 ถูกนำไปใช้กับส่วนหัวของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="23df0-165">In this example, the order total is $165.00, and the $15.00 freight charge is applied to the order header.</span></span> <span data-ttu-id="23df0-166">ค่าธรรมเนียมอัตโนมัติที่ถูกตั้งค่าคอนฟิกสำหรับโหมดการจัดส่ง **11** ไม่เคยถูกอ้างอิง หรือนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="23df0-166">Auto-charges that are configured for mode of delivery **11** are never referenced or applied.</span></span>

<span data-ttu-id="23df0-167">ในสถานการณ์จำลองนี้ เมื่อลูกค้าส่งคืนสินค้าบางรายการในใบสั่ง และถ้า [รหัสค่าธรรมเนียมถูกตั้งค่าคอนฟิกเพื่อให้สามารถขอคืนเงินได้](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2) ค่าธรรมเนียมระดับส่วนหัวรวมจะถูกนำไปใช้กับการคืนเงินอย่างเป็นระบบ แม้ว่าจะสามารถส่งคืนสินค้าได้บางอย่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="23df0-167">In this scenario, if a customer returns some of the items on the order, and if the [charge code has been configured so that it will be refunded](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), the total header-level charge is systematically applied to the refund, even if only some of the items are returned.</span></span>

### <a name="scenario-2"></a><span data-ttu-id="23df0-168">สถานการณ์จำลอง 2</span><span class="sxs-lookup"><span data-stu-id="23df0-168">Scenario 2</span></span>

<span data-ttu-id="23df0-169">ในสถานการณ์จำลองนี้ มีการกำหนดค่าธรรมเนียมระดับส่วนหัวสำหรับความสัมพันธ์โหมดของการจัดส่ง **99** และความสัมพันธ์โหมดของการจัดส่ง **11**</span><span class="sxs-lookup"><span data-stu-id="23df0-169">In this scenario, header-level charges are defined for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="23df0-170">อย่างไรก็ตาม ตัวเลือก **แบ่งตามส่วนไปยังรายการขายที่ตรงกัน** ถูกตั้งค่าเป็น **ใช่** สำหรับตารางค่าธรรมเนียมอัตโนมัติเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="23df0-170">However, the **Pro-rate to matching sales lines** option is set to **Yes** for these auto-charge tables.</span></span>

![ค่าธรรมเนียมอัตโนมัติสำหรับโหมดของการจัดส่ง 99 เมื่อเปิดการแบ่งตามสัดส่วนของรายการที่ตรงกัน](media/99_enabled.png)

![ค่าธรรมเนียมอัตโนมัติสำหรับโหมดของการจัดส่ง 11 เมื่อเปิดการแบ่งตามสัดส่วนของรายการที่ตรงกัน](media/11_enabled.png)

<span data-ttu-id="23df0-173">สถานการณ์จำลองนี้ใช้ใบสั่งขายเดียวกันที่ประกอบด้วยห้ารายการ</span><span class="sxs-lookup"><span data-stu-id="23df0-173">This scenario uses the same sales order that contains five lines.</span></span> <span data-ttu-id="23df0-174">โหมดของการจัดส่งในส่วนหัวใบสั่งถูกตั้งค่าเป็น **99** แต่มีโหมดของการจัดส่งสำหรับรายการแต่ละรายการบนใบสั่งขายถูกตั้งค่าคอนฟิกดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="23df0-174">The mode of delivery on the order header is set to **99**, but the mode of delivery for each item on the sales order is configured as shown in the following table.</span></span>

| <span data-ttu-id="23df0-175">สินค้า</span><span class="sxs-lookup"><span data-stu-id="23df0-175">Item</span></span>  | <span data-ttu-id="23df0-176">ปริมาณในรายการ</span><span class="sxs-lookup"><span data-stu-id="23df0-176">Line quantity</span></span> | <span data-ttu-id="23df0-177">วิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="23df0-177">Delivery mode</span></span> | <span data-ttu-id="23df0-178">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="23df0-178">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="23df0-179">81331</span><span class="sxs-lookup"><span data-stu-id="23df0-179">81331</span></span> | <span data-ttu-id="23df0-180">1</span><span class="sxs-lookup"><span data-stu-id="23df0-180">1</span></span>             | <span data-ttu-id="23df0-181">11</span><span class="sxs-lookup"><span data-stu-id="23df0-181">11</span></span>            | <span data-ttu-id="23df0-182">$10</span><span class="sxs-lookup"><span data-stu-id="23df0-182">$10</span></span>            |
| <span data-ttu-id="23df0-183">81332</span><span class="sxs-lookup"><span data-stu-id="23df0-183">81332</span></span> | <span data-ttu-id="23df0-184">1</span><span class="sxs-lookup"><span data-stu-id="23df0-184">1</span></span>             | <span data-ttu-id="23df0-185">99</span><span class="sxs-lookup"><span data-stu-id="23df0-185">99</span></span>            | <span data-ttu-id="23df0-186">$50</span><span class="sxs-lookup"><span data-stu-id="23df0-186">$50</span></span>            |
| <span data-ttu-id="23df0-187">81333</span><span class="sxs-lookup"><span data-stu-id="23df0-187">81333</span></span> | <span data-ttu-id="23df0-188">2</span><span class="sxs-lookup"><span data-stu-id="23df0-188">2</span></span>             | <span data-ttu-id="23df0-189">11</span><span class="sxs-lookup"><span data-stu-id="23df0-189">11</span></span>            | <span data-ttu-id="23df0-190">$30</span><span class="sxs-lookup"><span data-stu-id="23df0-190">$30</span></span>            |
| <span data-ttu-id="23df0-191">81334</span><span class="sxs-lookup"><span data-stu-id="23df0-191">81334</span></span> | <span data-ttu-id="23df0-192">3</span><span class="sxs-lookup"><span data-stu-id="23df0-192">3</span></span>             | <span data-ttu-id="23df0-193">99</span><span class="sxs-lookup"><span data-stu-id="23df0-193">99</span></span>            | <span data-ttu-id="23df0-194">$10</span><span class="sxs-lookup"><span data-stu-id="23df0-194">$10</span></span>            |
| <span data-ttu-id="23df0-195">81334</span><span class="sxs-lookup"><span data-stu-id="23df0-195">81334</span></span> | <span data-ttu-id="23df0-196">3</span><span class="sxs-lookup"><span data-stu-id="23df0-196">3</span></span>             | <span data-ttu-id="23df0-197">21</span><span class="sxs-lookup"><span data-stu-id="23df0-197">21</span></span>            | <span data-ttu-id="23df0-198">$5</span><span class="sxs-lookup"><span data-stu-id="23df0-198">$5</span></span>             |

<span data-ttu-id="23df0-199">เนื่องจากการตั้งค่าคอนฟิกค่าธรรมเนียมอัตโนมัติถูกตั้งค่าให้แบ่งตามสัดส่วนไปยังรายการขายที่ตรงกัน ระบบจะดำเนินการขั้นตอนการคำนวณต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="23df0-199">Because the auto-charge configuration is set to prorate to matching sales lines, the system performs the following calculation steps.</span></span>

1. <span data-ttu-id="23df0-200">รายการทั้งหมดที่มีโหมดการจัดส่งเดียวกันจะถูกจัดกลุ่มเข้าด้วยกัน และระบบจะคำนวณมูลค่าผลิตภัณฑ์รวมของรายการในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="23df0-200">All items that have the same mode of delivery are grouped together, and the system calculates the total product value of the items in the group.</span></span>

    <span data-ttu-id="23df0-201">**โหมดการจัดส่ง 11**</span><span class="sxs-lookup"><span data-stu-id="23df0-201">**Delivery mode 11**</span></span>

    - <span data-ttu-id="23df0-202">รายการ 81331 ปริมาณ 1 = $10</span><span class="sxs-lookup"><span data-stu-id="23df0-202">Item 81331, quantity 1 = $10</span></span>
    - <span data-ttu-id="23df0-203">รายการ 81333 ปริมาณ 2 = $60 สุทธิ ($30 ต่อหน่วย)</span><span class="sxs-lookup"><span data-stu-id="23df0-203">Item 81333, quantity 2 = $60 net ($30 per unit)</span></span>
    - <span data-ttu-id="23df0-204">**มูลค่ารวมผลิตภัณฑ์สำหรับโหมดการจัดส่ง 11 = $70**</span><span class="sxs-lookup"><span data-stu-id="23df0-204">**Total product value for delivery mode 11 = $70**</span></span>

    <span data-ttu-id="23df0-205">**โหมดการจัดส่ง 99**</span><span class="sxs-lookup"><span data-stu-id="23df0-205">**Delivery mode 99**</span></span>

    - <span data-ttu-id="23df0-206">รายการ 81332 ปริมาณ 1 = $50</span><span class="sxs-lookup"><span data-stu-id="23df0-206">Item 81332, quantity 1 = $50</span></span>
    - <span data-ttu-id="23df0-207">รายการ 81334 ปริมาณ 3 = $30 สุทธิ</span><span class="sxs-lookup"><span data-stu-id="23df0-207">Item 81334, quantity 3 = $30 net</span></span>
    - <span data-ttu-id="23df0-208">**มูลค่ารวมผลิตภัณฑ์สำหรับโหมดการจัดส่ง 99 = $80**</span><span class="sxs-lookup"><span data-stu-id="23df0-208">**Total product value for delivery mode 99 = $80**</span></span>

    <span data-ttu-id="23df0-209">**โหมดการจัดส่ง 21**</span><span class="sxs-lookup"><span data-stu-id="23df0-209">**Delivery mode 21**</span></span>

    - <span data-ttu-id="23df0-210">รายการ 81334 ปริมาณ 3 = $15 สุทธิ</span><span class="sxs-lookup"><span data-stu-id="23df0-210">Item 81334, quantity 3 = $15 net</span></span>
    - <span data-ttu-id="23df0-211">**มูลค่ารวมผลิตภัณฑ์สำหรับโหมดการจัดส่ง 21 = $15**</span><span class="sxs-lookup"><span data-stu-id="23df0-211">**Total product value for delivery mode 21 = $15**</span></span>

2. <span data-ttu-id="23df0-212">ระบบค้นหาการตั้งค่าคอนฟิกสำหรับค่าธรรมเนียมอัตโนมัติในระดับส่วนหัว ที่ตรงกับลูกค้าและการตั้งค่าโหมดการจัดส่งสำหรับกลุ่มของรายการแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="23df0-212">The system looks for the configuration for header-level auto-charges that matches the customer and mode of delivery settings for each group of items.</span></span> <span data-ttu-id="23df0-213">ถ้าพบการตั้งค่าคอนฟิก ระบบดูในการตั้งค่าคอนฟิกที่จัดระดับเพื่อค้นหาค่าธรรมเนียมที่ควรจะถูกนำไปใช้ โดยขึ้นอยู่กับค่าผลิตภัณฑ์รวมของรายการในโหมดของกลุ่มการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="23df0-213">If the configuration is found, the system looks in the tiered configuration to find the charge that should be applied, based on the total product value of items in the mode of delivery group.</span></span>

    <span data-ttu-id="23df0-214">**โหมดการจัดส่ง 11**</span><span class="sxs-lookup"><span data-stu-id="23df0-214">**Delivery mode 11**</span></span>

    - <span data-ttu-id="23df0-215">มูลค่าผลิตภัณฑ์รวม = $70</span><span class="sxs-lookup"><span data-stu-id="23df0-215">Total product value = $70</span></span>
    - <span data-ttu-id="23df0-216">**มูลค่าของค่าธรรมเนียม = $7**</span><span class="sxs-lookup"><span data-stu-id="23df0-216">**Charge value = $7**</span></span>

    <span data-ttu-id="23df0-217">**โหมดการจัดส่ง 99**</span><span class="sxs-lookup"><span data-stu-id="23df0-217">**Delivery mode 99**</span></span>

    - <span data-ttu-id="23df0-218">มูลค่าผลิตภัณฑ์รวม = $80</span><span class="sxs-lookup"><span data-stu-id="23df0-218">Total product value = $80</span></span>
    - <span data-ttu-id="23df0-219">**มูลค่าของค่าธรรมเนียม = $15**</span><span class="sxs-lookup"><span data-stu-id="23df0-219">**Charge value = $15**</span></span>

    <span data-ttu-id="23df0-220">**โหมดการจัดส่ง 21**</span><span class="sxs-lookup"><span data-stu-id="23df0-220">**Delivery mode 21**</span></span>

    - <span data-ttu-id="23df0-221">มูลค่าผลิตภัณฑ์รวม = $15</span><span class="sxs-lookup"><span data-stu-id="23df0-221">Total product value = $15</span></span>
    - <span data-ttu-id="23df0-222">**มูลค่าของค่าธรรมเนียม = $0** (ไม่มีการตั้งค่าคอนฟิกค่าธรรมเนียมอัตโนมัติสำหรับชุดข้อมูลนี้ของลูกค้าและโหมดการจัดส่ง)</span><span class="sxs-lookup"><span data-stu-id="23df0-222">**Charge value = $0** (No auto-charges have been configured for this combination of a customer and a mode of delivery.)</span></span>

    ![ค่าธรรมเนียมโหมดการจัดส่ง 11 แบ่งออกเป็นระดับที่เน้น](media/step2mode11.png)

    ![ค่าธรรมเนียมโหมดการจัดส่ง 99 แบ่งออกเป็นระดับที่เน้น](media/step2mode99.png)

3. <span data-ttu-id="23df0-225">ระบบจะคำนวณมูลค่าของค่าธรรมเนียมที่ควรใช้กับแต่ละรายการ ตามตรรกะการแบ่งตามส่วนซึ่งถือว่าค่าตามสัดส่วนของรายการสัมพันธ์กับมูลค่าผลิตภัณฑ์รวมของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="23df0-225">The system calculates the charge value that should be applied to each line, based on proration logic that considers the proportional value of the line in relation to the group's total product value.</span></span>

    <span data-ttu-id="23df0-226">**โหมดการจัดส่ง 11**</span><span class="sxs-lookup"><span data-stu-id="23df0-226">**Delivery mode 11**</span></span>

    - <span data-ttu-id="23df0-227">มูลค่าของค่าธรรมเนียม = $7</span><span class="sxs-lookup"><span data-stu-id="23df0-227">Charge value = $7</span></span>
    - <span data-ttu-id="23df0-228">มูลค่าผลิตภัณฑ์กลุ่ม = $70</span><span class="sxs-lookup"><span data-stu-id="23df0-228">Group product value = $70</span></span>
    - <span data-ttu-id="23df0-229">มูลค่าของรายการ 1 = $10 (= 14.2857 เปอร์เซ็นต์ของมูลค่ากลุ่ม)</span><span class="sxs-lookup"><span data-stu-id="23df0-229">Line 1 value = $10 (= 14.2857 percent of the group value)</span></span>
    - <span data-ttu-id="23df0-230">มูลค่าของรายการ 3 = $60 (= 85.7143 เปอร์เซ็นต์ของมูลค่ากลุ่ม)</span><span class="sxs-lookup"><span data-stu-id="23df0-230">Line 3 value = $60 (= 85.7143 percent of the group value)</span></span>
    - <span data-ttu-id="23df0-231">**รายการค่าธรรมเนียมสำหรับรายการที่ 1 = $1**</span><span class="sxs-lookup"><span data-stu-id="23df0-231">**Line charge for line 1 = $1**</span></span>
    - <span data-ttu-id="23df0-232">**รายการค่าธรรมเนียมสำหรับรายการที่ 3 = $6**</span><span class="sxs-lookup"><span data-stu-id="23df0-232">**Line charge for line 3 = $6**</span></span>

    <span data-ttu-id="23df0-233">**โหมดการจัดส่ง 99**</span><span class="sxs-lookup"><span data-stu-id="23df0-233">**Delivery mode 99**</span></span>

    - <span data-ttu-id="23df0-234">มูลค่าของค่าธรรมเนียม = $15</span><span class="sxs-lookup"><span data-stu-id="23df0-234">Charge value = $15</span></span>
    - <span data-ttu-id="23df0-235">มูลค่าผลิตภัณฑ์กลุ่ม = $80</span><span class="sxs-lookup"><span data-stu-id="23df0-235">Group product value = $80</span></span>
    - <span data-ttu-id="23df0-236">มูลค่าของรายการ 2 = $50 (= 62.5 เปอร์เซ็นต์ของมูลค่ากลุ่ม)</span><span class="sxs-lookup"><span data-stu-id="23df0-236">Line 2 value = $50 (= 62.5 percent of the group value)</span></span>
    - <span data-ttu-id="23df0-237">มูลค่าของรายการ 4 = $30 (= 37.5 เปอร์เซ็นต์ของมูลค่ากลุ่ม)</span><span class="sxs-lookup"><span data-stu-id="23df0-237">Line 4 value = $30 (= 37.5 percent of the group value)</span></span>
    - <span data-ttu-id="23df0-238">**รายการค่าธรรมเนียมสำหรับรายการที่ 2 = $9.38**</span><span class="sxs-lookup"><span data-stu-id="23df0-238">**Line charge for line 2 = $9.38**</span></span>
    - <span data-ttu-id="23df0-239">**รายการค่าธรรมเนียมสำหรับรายการที่ 4 = $5.62**</span><span class="sxs-lookup"><span data-stu-id="23df0-239">**Line charge for line 4 = $5.62**</span></span>

    <span data-ttu-id="23df0-240">**โหมดการจัดส่ง 21**</span><span class="sxs-lookup"><span data-stu-id="23df0-240">**Delivery mode 21**</span></span>

    - <span data-ttu-id="23df0-241">มูลค่าของค่าธรรมเนียม = $0</span><span class="sxs-lookup"><span data-stu-id="23df0-241">Charge value = $0</span></span>
    - <span data-ttu-id="23df0-242">มูลค่าผลิตภัณฑ์กลุ่ม = $15</span><span class="sxs-lookup"><span data-stu-id="23df0-242">Group product value = $15</span></span>
    - <span data-ttu-id="23df0-243">มูลค่าของรายการ 5 = $15 (= 100 เปอร์เซ็นต์ของมูลค่ากลุ่ม)</span><span class="sxs-lookup"><span data-stu-id="23df0-243">Line 5 value = $15 (= 100 percent of the group value)</span></span>
    - <span data-ttu-id="23df0-244">**ค่าธรรมเนียมรายการสำหรับรายการ 5 = $0**</span><span class="sxs-lookup"><span data-stu-id="23df0-244">**Line charge for line 5 = $0**</span></span>

<span data-ttu-id="23df0-245">ดังนั้น สำหรับตัวอย่างนี้ รายการ 81334 จะถูกกำหนดค่าธรรมเนียมการขนส่งเป็น $5.62</span><span class="sxs-lookup"><span data-stu-id="23df0-245">Therefore, for this example, item 81334 will be assigned a freight charge of $5.62.</span></span> <span data-ttu-id="23df0-246">คุณสามารถดูค่าธรรมเนียมเหล่านี้ได้ในหน้า **รักษาค่าธรรมเนียม** สำหรับรายการขาย</span><span class="sxs-lookup"><span data-stu-id="23df0-246">You can view these charges on the **Maintain charges** page for the sales line.</span></span> <span data-ttu-id="23df0-247">ภาพประกอบต่อไปนี้แสดงลักษณะของหน้านี้สำหรับรายการ 81334</span><span class="sxs-lookup"><span data-stu-id="23df0-247">The following illustration shows what this page looks like for item 81334.</span></span>

![ค่าธรรมเนียมตามสัดส่วนในรายการขายสำหรับรายการ 81334](media/proratedlinecharge.png)

<span data-ttu-id="23df0-249">เมื่อมีการใช้วิธีของการคำนวณนี้ในสถานการณ์จำลองการส่งคืนบางส่วน ถ้ารหัสค่าธรรมเนียมสามารถคืนเงินได้ เฉพาะบางส่วนของค่าธรรมเนียมที่ถูกปันส่วนให้กับรายการนั้นจะสามารถขอคืนได้ เมื่อมีการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="23df0-249">When this method of calculation is used in a partial return scenario, if the charge code is refundable, only the part of the charge that is allocated to that line will be refunded when the item is returned.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23df0-250">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="23df0-250">Additional resources</span></span>

[<span data-ttu-id="23df0-251">ค่าธรรมเนียมอัตโนมัติขั้นสูงของช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="23df0-251">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="23df0-252">เปิดใช้งานและตั้งค่าคอนฟิกค่าธรรมเนียมอัตโนมัติตามช่องทาง</span><span class="sxs-lookup"><span data-stu-id="23df0-252">Enable and configure auto charges by channel</span></span>](auto-charges-by-channel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]