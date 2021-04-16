---
title: ภาพรวมสินเชื่อและการเรียกเก็บเงิน
description: หัวข้อนี้แสดงภาพรวมของฟังก์ชันสำหรับสินเชื่อและการเรียกเก็บเงิน
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7929150cd9f6c28620f4c4d4cb7b57b02d27a104
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835423"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="d842e-103">ภาพรวมสินเชื่อและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d842e-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d842e-104">คุณสามารถจัดการวงเงินสินเชื่อสำหรับลูกค้าของคุณ และดำเนินกิจกรรมการเรียกเก็บเงินได้เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d842e-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="d842e-105">การจัดการสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="d842e-105">Credit management</span></span>

<span data-ttu-id="d842e-106">การจัดการเครดิตของลูกค้าช่วยให้คุณสามารถจัดการวงเงินสินเชื่อและควบคุมกระบวนการผลิตของใบสั่งขาย โดยใช้กระบวนการลงรายการบัญชีตามกฎเครดิตที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="d842e-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="d842e-107">กระบวนการการจัดการเครดิตอาจประกอบด้วยขั้นตอนใด ๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d842e-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="d842e-108">ปรับปรุงแอททริบิวต์เครดิตสำหรับลูกค้าเพื่อให้ข้อมูลเพิ่มเติมเกี่ยวกับความน่าเชื่อถือของผู้ถือบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="d842e-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="d842e-109">สร้างวงเงินสินเชื่อสำหรับลูกค้าโดยใช้การปรับปรุงวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="d842e-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="d842e-110">สร้างวงเงินสินเชื่อชั่วคราวสำหรับลูกค้าโดยใช้การปรับปรุงวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="d842e-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="d842e-111">ด้วยวิธีนี้ คุณสามารถเพิ่มหรือลดวงเงินสินเชื่อของลูกค้าได้ชั่วคราว ตามความต้องการของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="d842e-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="d842e-112">เพิ่มข้อมูลที่อาจส่งผลกระทบต่อวงเงินสินเชื่อ เช่น ข้อมูลเกี่ยวกับการประกันภัยและการค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="d842e-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="d842e-113">สร้างกลุ่มเครดิตของลูกค้าที่เชื่อมโยงกับลูกค้าด้วยกัน เพื่อให้พวกเขาสามารถใช้วงเงินสินเชื่อเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="d842e-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="d842e-114">กำหนดคะแนนความเสี่ยงให้กับลูกค้า แล้วใช้คะแนนเหล่านั้นเพื่อสร้างวงเงินสินเชื่อสำหรับลูกค้าเหล่านั้นโดยอัตโนมัติผ่านการปรับปรุงวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="d842e-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="d842e-115">สร้างกฎการบล็อคที่จะทำการระงับใบสั่งระหว่างกระบวนการลงรายการบัญชีอย่างน้อยหนึ่งรายการตามปัจจัยต่าง ๆ เช่น ความเสี่ยง เงื่อนไขการชำระเงิน วงเงินสินเชื่อ ยอดเงินที่พ้นกำหนดชำระ และเปอร์เซ็นต์ของวงเงินสินเชื่อที่ใช้</span><span class="sxs-lookup"><span data-stu-id="d842e-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="d842e-116">จัดการรายการของใบสั่งขายที่ระงับ ตรวจสอบเหตุผลสำหรับการระงับ และลดปัญหา</span><span class="sxs-lookup"><span data-stu-id="d842e-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="d842e-117">นำใบสั่งขายออกใช้ เพื่อที่พวกเขาสามารถดำเนินการต่อโดยใช้กระบวนการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d842e-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="d842e-118">ตั้งค่าลำดับงานเพื่อจัดการการอนุมัติการเปลี่ยนแปลงวงเงินสินเชื่อ และการนำใบสั่งขายออกใช้</span><span class="sxs-lookup"><span data-stu-id="d842e-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="d842e-119">การจัดการการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d842e-119">Collections management</span></span>

<span data-ttu-id="d842e-120">เพจ **การเรียกเก็บเงิน** ให้มุมมองส่วนกลางที่ข้อมูลการเรียกเก็บเงินบัญชีลูกหนี้ได้รับการจัดการ</span><span class="sxs-lookup"><span data-stu-id="d842e-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="d842e-121">ผู้จัดการฝ่ายการเรียกเก็บเงินสามารถใช้มุมมองส่วนกลางนี้ เพื่อจัดการการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="d842e-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="d842e-122">ตัวแทนเรียกเก็บเงินจะเริ่มกระบวนการเรียกเก็บเงินจากรายชื่อลูกค้าที่ถูกสร้างขึ้นโดยการใช้เกณฑ์การเรียกเก็บเงินที่กำหนดไว้ล่วงหน้าหรือจากเพจ **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="d842e-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="d842e-123">ก่อนที่คุณจะเริ่มตั้งค่าหรือทำงานกับการเรียกเก็บเงิน คุณควรทำความเข้าใจแนวคิดต่างๆต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d842e-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="d842e-124">สแนปช็อตอายุหนี้ลูกค้าประกอบด้วยข้อมูลยอดดุลอายุหนี้ ณ เวลาหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d842e-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="d842e-125">การเรียกเก็บเงินกลุ่มลูกค้าช่วยคุณจัดระเบียบงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="d842e-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="d842e-126">ตัวแทนเรียกเก็บเงินสามารถมีกลุ่มลูกค้าของตนเองได้</span><span class="sxs-lookup"><span data-stu-id="d842e-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="d842e-127">หน้ารายการจัดระเบียบการเรียกเก็บเงินลูกค้า กิจกรรม และกรณีต่างๆ</span><span class="sxs-lookup"><span data-stu-id="d842e-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="d842e-128">ข้อมูลการเรียกเก็บเงินทั้งหมดสำหรับลูกค้าอยู่บนหน้าหนึ่งหน้า และคุณสามารถดำเนินการได้จากหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="d842e-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="d842e-129">ดอกเบี้ยและค่าธรรมเนียมสามารถยกเว้น กลับมาคิด หรือกลับรายการได้ในขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="d842e-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="d842e-130">ธุรกรรมการตัดจ่ายสามารถทำได้ในขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="d842e-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="d842e-131">การชำระเงินที่มีเงินในบัญชีไม่พอ (NSF) สามารถทำได้ในขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="d842e-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="d842e-132">สำหรับคำอธิบายแนวคิดเหล่านี้ โปรดดูที่ [แนวคิดหลักของการจัดการการเรียกเก็บเงิน](./cm-collections-concepts.md)</span><span class="sxs-lookup"><span data-stu-id="d842e-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d842e-133">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d842e-133">Additional resources</span></span>

[<span data-ttu-id="d842e-134">การตั้งค่าพารามิเตอร์การจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d842e-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="d842e-135">ข้อมูลการตั้งค่าการจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d842e-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="d842e-136">เพิ่มข้อมูลการตั้งค่าการจัดการเครดิตสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d842e-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="d842e-137">กลุ่มสินเชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d842e-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="d842e-138">การปรับปรุงวงเงินเครดิตลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d842e-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="d842e-139">การระงับเครดิตสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="d842e-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="d842e-140">งานประจำงวดการจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d842e-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]