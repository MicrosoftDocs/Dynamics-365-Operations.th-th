---
title: การอนุมัติใบแจ้งหนี้แบบเคลื่อนที่
description: หัวข้อนี้มีไว้เพื่อให้วิธีการที่ใช้ได้จริงในการออกแบบสถานการณ์สมมติแบบเคลื่อนที่โดยการใช้การอนุมัติใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับมือถือเป็นกรณีใช้
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88ba96b1d9d2f722528a4a920eabe4ab64304a7a
ms.sourcegitcommit: 4f668b23f5bfc6d6502858850d2ed59d7a79cfbb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/14/2020
ms.locfileid: "3059439"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="c18cd-103">การอนุมัติใบแจ้งหนี้แบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c18cd-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c18cd-104">ความสามารถของอุปกรณ์เคลื่อนที่ช่วยให้ผู้ใช้ประเภทธุรกิจออกแบบประสบการณ์การใช้งานแบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c18cd-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="c18cd-105">สำหรับสถานการณ์สมมติขั้นสูง แพลตฟอร์มยังช่วยให้นักพัฒนาเพิ่มความสามารถได้ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c18cd-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="c18cd-106">วิธีที่มีประสิทธิภาพมากที่สุดในการเรียนรู้แนวคิดใหม่เกี่ยวกับการเคลื่อนที่คือการผ่านกระบวนการออกแบบสถานการณ์สมมติสองสามอย่าง</span><span class="sxs-lookup"><span data-stu-id="c18cd-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="c18cd-107">หัวข้อนี้มีไว้เพื่อให้วิธีการที่ใช้ได้จริงในการออกแบบสถานการณ์สมมติแบบเคลื่อนที่โดยการใช้การอนุมัติใบแจ้งหนี้ของผู้จัดจำหน่ายสำหรับมือถือเป็นกรณีใช้</span><span class="sxs-lookup"><span data-stu-id="c18cd-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="c18cd-108">หัวข้อนี้อาจช่วยให้คุณสามารถออกแบบความผันแปรของสถานการณ์จำลองต่าง ๆ อื่น ๆ และยังสามารถใช้กับสถานการณ์จำลองอื่น ๆ ที่ไม่เกี่ยวข้องกับใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c18cd-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="c18cd-109">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="c18cd-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="c18cd-110">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="c18cd-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="c18cd-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c18cd-112">การอ่านคู่มือมือถือล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="c18cd-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="c18cd-113">แพลตฟอร์มเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c18cd-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="c18cd-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="c18cd-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="c18cd-115">สภาพแวดล้อมที่มีรุ่น 1611 และการอัพเดตแพลตฟอร์ม 3 (พฤศจิกายน 2016)</span><span class="sxs-lookup"><span data-stu-id="c18cd-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="c18cd-116">ติดตั้ง KB โปรแกรมแก้ไขด่วน 3204341</span><span class="sxs-lookup"><span data-stu-id="c18cd-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="c18cd-117">ตัวเรกคอร์ดงานสามารถบันทึกคำสั่ง Close สองรายการอย่างไม่ถูกต้องสำหรับกล่องโต้ตอบแบบหล่นลง ซึ่งมีอยู่ในการอัพเดตแพลตฟอร์ม 3 (การอัพเดตเดือนพฤศจิกายน 2016)</span><span class="sxs-lookup"><span data-stu-id="c18cd-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="c18cd-118">ติดตั้ง KB โปรแกรมแก้ไขด่วน 3207800</span><span class="sxs-lookup"><span data-stu-id="c18cd-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="c18cd-119">โปรแกรมแก้ไขด่วนนี้ทำให้สามารถดูเอกสารแนบบนไคลเอ็นต์แบบเคลื่อนที่ได้ ซึ่งรวมอยู่ในการอัพเดตแพลตฟอร์ม 3 (การอัพเดตเดือนพฤศจิกายน 2016)</span><span class="sxs-lookup"><span data-stu-id="c18cd-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="c18cd-120">ติดตั้ง KB โปรแกรมแก้ไขด่วน 3208224</span><span class="sxs-lookup"><span data-stu-id="c18cd-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="c18cd-121">รหัสแอพลิเคชันสำหรับแอพลิเคชันอนุมัติใบแจ้งหนี้ของผู้จัดจำหน่าย ซึ่งจะรวมอยู่ในรุ่น 7.0.1 (พฤษภาคม 2016)</span><span class="sxs-lookup"><span data-stu-id="c18cd-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="c18cd-122">Android หรือ iOS หรืออุปกรณ์ Windows ที่ได้มีการติดตั้งแอพสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c18cd-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="c18cd-123">ค้นหาแอพในร้านค้าแอพที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="c18cd-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="c18cd-124">คำนำ</span><span class="sxs-lookup"><span data-stu-id="c18cd-124">Introduction</span></span>
<span data-ttu-id="c18cd-125">การอนุมัติแบบเคลื่อนที่สำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายต้องใช้โปรแกรมแก้ไขด่วนสามรายการที่กล่าวถึงในส่วน "ข้อกำหนดเบื้องต้น"</span><span class="sxs-lookup"><span data-stu-id="c18cd-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="c18cd-126">โปรแกรมแก้ไขด่วนนี้ไม่ได้ให้พื้นที่ทำงานสำหรับการอนุมัติใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="c18cd-127">เมื่อต้องการเรียนรู้ว่าพื้นที่ทำงานที่อยู่ในบริบทของโทรศัพท์มือถือคืออะไร ให้อ่านคู่มือมือถือที่กล่าวถึงในส่วน "ข้อกำหนดเบื้องต้น"</span><span class="sxs-lookup"><span data-stu-id="c18cd-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="c18cd-128">พื้นที่ทำงานการอนุมัติใบแจ้งหนี้ต้องได้รับการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="c18cd-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="c18cd-129">ทุกองค์กรประสานและกำหนดกระบวนการทางธุรกิจสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c18cd-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="c18cd-130">ก่อนที่คุณจะออกแบบประสบการณ์การใช้งานมือถือสำหรับการอนุมัติใบแจ้งหนี้ของผู้จัดจำหน่าย คุณควรพิจารณาด้านต่อไปนี้ของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c18cd-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="c18cd-131">แนวความคิดนี้คือเพื่อใช้จุดข้อมูลเหล่านี้ให้มากที่สุดเพื่อปรับประสบการณ์ผู้ใช้บนอุปกรณ์ให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="c18cd-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="c18cd-132">ฟิลด์ใดบ้างจากส่วนหัวของใบแจ้งหนี้ที่ผู้ใช้จะต้องการดูในประสบการณ์การใช้งานมือถือและในลำดับใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="c18cd-133">ฟิลด์ใดบ้างจากรายการใบแจ้งหนี้ที่ผู้ใช้จะต้องการดูในประสบการณ์การใช้งานมือถือและในลำดับใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="c18cd-134">มีบรรทัดใบแจ้งหนี้ในใบแจ้งหนี้จำนวนเท่าใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="c18cd-135">ใช้กฎ 80-20 และปรับให้เหมาะสมกับ 80 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="c18cd-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="c18cd-136">ผู้ใช้จะต้องการดูการกระจายการลงบัญชี (การกำหนดรหัสใบแจ้งหนี้) บนอุปกรณ์เคลื่อนที่ในระหว่างการตรวจทานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="c18cd-137">ถ้าคำตอบของคำถามนี้คือ ใช่ ให้พิจารณาคำถามต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c18cd-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="c18cd-138">มีการกระจายการลงบัญชี (ราคารวม ภาษีขาย ค่าธรรมเนียม การแยก และอื่น ๆ) สำหรับรายการใบแจ้งหนี้จำนวนเท่าใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="c18cd-139">ใช้กฎ 80-20 อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="c18cd-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="c18cd-140">ใบแจ้งหนี้มีการกระจายการลงบัญชีในส่วนหัวของใบแจ้งหนี้ด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="c18cd-141">ถ้าเป็นเช่นนั้น กระจายการลงบัญชีเหล่านี้ควรพร้อมใช้งานบนอุปกรณ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="c18cd-142">หัวข้อนี้ไม่ได้อธิบายวิธีการแก้ไขการกระจายการลงบัญชี เนื่องจากฟังก์ชันนี้ไม่ได้รับการสนับสนุนสำหรับสถานการณ์จำลองแบบเคลื่อนที่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="c18cd-143">ผู้ใช้จะต้องการดูเอกสารแนบสำหรับใบแจ้งหนี้บนอุปกรณ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="c18cd-144">การออกแบบของประสบการณ์การใช้งานมือถือสำหรับการอนุมัติใบแจ้งหนี้จะแตกต่างกัน ขึ้นอยู่กับคำตอบของคำถามเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="c18cd-145">วัตถุประสงค์คือเพื่อปรับประสบการณ์ผู้ใช้สำหรับกระบวนการทางธุรกิจบนมือถือในองค์กรให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="c18cd-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="c18cd-146">ในส่วนที่เหลือของหัวข้อนี้ เราจะดูความแตกต่างของสถานการณ์จำลองสองรายการที่ยึดตามคำตอบที่แตกต่างกันของคำถามก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="c18cd-147">โดยเป็นคำแนะนำทั่วไป เมื่อทำงานกับตัวออกแบบเคลื่อนที่ ต้องแน่ใจว่าได้ 'เผยแพร่' การเปลี่ยนแปลงแล้วเพื่อป้องกันการสูญเสียการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="c18cd-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="c18cd-148">การออกแบบสถานการณ์จำลองการอนุมัติใบแจ้งหนี้แบบง่ายสำหรับ Contoso</span><span class="sxs-lookup"><span data-stu-id="c18cd-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c18cd-149">แอททริบิวต์สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="c18cd-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="c18cd-150">รับสาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c18cd-151">ฟิลด์ใดบ้างจากส่วนหัวของใบแจ้งหนี้ที่ผู้ใช้จะต้องการดูในประสบการณ์การใช้งานมือถือและในลำดับใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="c18cd-152">ชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c18cd-152">Vendor name</span></span></li>
<li><span data-ttu-id="c18cd-153">ผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-153">Invoice total</span></span></li>
<li><span data-ttu-id="c18cd-154">บัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-154">Invoice account</span></span></li>
<li><span data-ttu-id="c18cd-155">หมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-155">Invoice number</span></span></li>
<li><span data-ttu-id="c18cd-156">วันที่ในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-156">Invoice date</span></span></li>
<li><span data-ttu-id="c18cd-157">คำอธิบายใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-157">Invoice description</span></span></li>
<li><span data-ttu-id="c18cd-158">วันที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="c18cd-158">Due date</span></span></li>
<li><span data-ttu-id="c18cd-159">สกุลเงินในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c18cd-160">ฟิลด์ใดบ้างจากรายการใบแจ้งหนี้ที่ผู้ใช้จะต้องการดูในประสบการณ์การใช้งานมือถือและในลำดับใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="c18cd-161">ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c18cd-161">Procurement category</span></span></li>
<li><span data-ttu-id="c18cd-162">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-162">Quantity</span></span></li>
<li><span data-ttu-id="c18cd-163">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="c18cd-163">Unit price</span></span></li>
<li><span data-ttu-id="c18cd-164">ยอดเงินสุทธิของรายการ</span><span class="sxs-lookup"><span data-stu-id="c18cd-164">Line net amount</span></span></li>
<li><span data-ttu-id="c18cd-165">ยอดเงิน 1099</span><span class="sxs-lookup"><span data-stu-id="c18cd-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c18cd-166">มีบรรทัดใบแจ้งหนี้ในใบแจ้งหนี้จำนวนเท่าใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="c18cd-167">ใช้กฎ 80-20 และปรับให้เหมาะสมกับ 80 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="c18cd-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="c18cd-168">1</span><span class="sxs-lookup"><span data-stu-id="c18cd-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c18cd-169">ผู้ใช้จะต้องการดูการกระจายการลงบัญชี (การกำหนดรหัสใบแจ้งหนี้) บนอุปกรณ์เคลื่อนที่ในระหว่างการตรวจทานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="c18cd-170">ใช่</span><span class="sxs-lookup"><span data-stu-id="c18cd-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c18cd-171">มีการกระจายการลงบัญชี (ราคารวม ภาษีขาย ค่าธรรมเนียม และอื่น ๆ) สำหรับรายการใบแจ้งหนี้จำนวนเท่าใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="c18cd-172">ใช้กฎ 80-20 อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="c18cd-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="c18cd-173">ราคารวม: 2 ภาษีขาย: 0 ค่าธรรมเนียม: 0</span><span class="sxs-lookup"><span data-stu-id="c18cd-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c18cd-174">ใบแจ้งหนี้มีการกระจายการลงบัญชีในส่วนหัวของใบแจ้งหนี้ด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="c18cd-175">ถ้าเป็นเช่นนั้น กระจายการลงบัญชีเหล่านี้ควรพร้อมใช้งานบนอุปกรณ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="c18cd-176">ไม่ได้ใช้</span><span class="sxs-lookup"><span data-stu-id="c18cd-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c18cd-177">ผู้ใช้จะต้องการดูเอกสารแนบสำหรับใบแจ้งหนี้บนอุปกรณ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="c18cd-178">ใช่</span><span class="sxs-lookup"><span data-stu-id="c18cd-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="c18cd-179">สร้างพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-179">Create the workspace</span></span>

1.  <span data-ttu-id="c18cd-180">ในเบราว์เซอร์ และลงชื่อเข้าใช้ไปยังแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="c18cd-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="c18cd-181">หลังจากที่คุณได้เข้าสู่ระบบ ผนวก **&mode=mobile** กับ URL ที่แสดงไว้ในฟิลด์ต่อไปนี้ และรีเฟรชหน้า: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="c18cd-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="c18cd-182">คลิกปุ่ม **การตั้งค่า** (เกียร์) ในมุมบนขวาของหน้า จากนั้นคลิก **แอพบนมือถือ**</span><span class="sxs-lookup"><span data-stu-id="c18cd-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="c18cd-183">ตัวออกแบบแอพแบบเคลื่อนที่ต้องแสดงค่าเดียวกับที่ตัวบันทึกงานแสดง</span><span class="sxs-lookup"><span data-stu-id="c18cd-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="c18cd-184">คลิก **เพิ่ม** เพื่อสร้างพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="c18cd-185">สำหรับตัวอย่างนี้ กำหนดชื่อพื้นที่ทำงานเป็น **การอนุมัติของฉัน**</span><span class="sxs-lookup"><span data-stu-id="c18cd-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="c18cd-186">ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-186">Enter a description.</span></span>
6.  <span data-ttu-id="c18cd-187">เลือกสีของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-187">Select a workspace color.</span></span> <span data-ttu-id="c18cd-188">สีของพื้นที่ทำงานจะใช้กับลักษณะโดยรวมของประสบการณ์การใช้งานมือถือสำหรับพื้นที่ทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="c18cd-189">เลือกไอคอนสำหรับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="c18cd-190">คลิก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="c18cd-190">Click **Done**</span></span>
9.  <span data-ttu-id="c18cd-191">คลิก **เผยแพร่พื้นที่ทำงาน** เพื่อบันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="c18cd-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="c18cd-192">ดูใบแจ้งหนี้ของผู้จัดจำหน่ายที่กำหนดให้กับฉัน</span><span class="sxs-lookup"><span data-stu-id="c18cd-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="c18cd-193">หน้าแรกบนมือถือที่คุณควรออกแบบคือรายการของใบแจ้งหนี้ที่ถูกกำหนดให้กับผู้ใช้เพื่อให้ตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="c18cd-194">เมื่อต้องการออกแบบหน้าบนมือถือนี้ ให้ใช้หน้า **VendMobileInvoiceAssignedToMeListPage**</span><span class="sxs-lookup"><span data-stu-id="c18cd-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="c18cd-195">ก่อนที่คุณจะทำขั้นตอนนี้เสร็จสมบูรณ์ ตรวจสอบให้แน่ใจว่ามีใบแจ้งหนี้ของผู้จัดจำหน่ายอย่างน้อยหนึ่งรายการถูกกำหนดให้คุณตรวจทาน และบรรทัดใบแจ้งหนี้มีการกระจายสองรายการ</span><span class="sxs-lookup"><span data-stu-id="c18cd-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="c18cd-196">การตั้งค่านี้สอดคล้องกับข้อกำหนดสำหรับสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="c18cd-197">ใน URL แทนชื่อของรายการเมนูด้วย **VendMobileInvoiceAssignedToMeListPage** เพื่อเปิดรุ่นของมือถือของหน้ารายการ **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่ที่กำหนดให้แก่ฉัน** ในโมดูล **บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="c18cd-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="c18cd-198">โดยขึ้นอยู่กับจำนวนของใบแจ้งหนี้ที่คุณมีในระบบของคุณที่กำหนดให้กับคุณ หน้านี้จะแสดงใบแจ้งหนี้เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="c18cd-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="c18cd-199">เมื่อต้องการค้นหาใบแจ้งหนี้ที่เฉพาะเจาะจง คุณสามารถใช้ตัวกรองด้านซ้ายมือ</span><span class="sxs-lookup"><span data-stu-id="c18cd-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="c18cd-200">อย่างไรก็ตาม เราไม่จำเป็นต้องใช้มใบแจ้งหนี้ที่เฉพาะเจาะจงสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="c18cd-201">เราเพียงแค่ต้องใช้ใบแจ้งหนี้บางรายการที่กำหนดให้กับคุณซึ่งจะช่วยให้คุณสามารถออกแบบหน้าบนมือถือได้</span><span class="sxs-lookup"><span data-stu-id="c18cd-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="c18cd-202">หน้าใหม่ที่พร้อมใช้งานได้รับการออกแบบเป็นพิเศษสำหรับการพัฒนาสถานการณ์จำลองบนมือถือสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c18cd-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="c18cd-203">ดังนั้น คุณต้องใช้หน้าเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="c18cd-204">URL ควรมีลักษณะคล้ายกับ URL ต่อไปนี้ และหลังจากที่คุณป้อนแล้ว หน้าที่แสดงในภาพประกอบต้องปรากฏ: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="c18cd-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="c18cd-205">[![หน้าใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่ซึ่งกำหนดให้กับฉัน](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="c18cd-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="c18cd-206">คลิกปุ่ม **การตั้งค่า** (เกียร์) ในมุมบนขวาของหน้า จากนั้นคลิก **แอพบนมือถือ**</span><span class="sxs-lookup"><span data-stu-id="c18cd-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="c18cd-207">เลือกพื้นที่ทำงานของคุณ และคลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="c18cd-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="c18cd-208">คลิก **เพิ่มหน้า** เพื่อสร้างหน้าบนมือถือหน้าแรก</span><span class="sxs-lookup"><span data-stu-id="c18cd-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="c18cd-209">ป้อนชื่อ เช่น **ใบแจ้งหนี้ของผู้จัดจำหน่ายของฉัน**และคำอธิบาย เช่น **ใบแจ้งหนี้ของผู้จัดจำหน่ายที่กำหนดให้กับฉันเพื่อตรวจทาน**</span><span class="sxs-lookup"><span data-stu-id="c18cd-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="c18cd-210">คลิก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="c18cd-210">Click **Done**.</span></span>
7.  <span data-ttu-id="c18cd-211">ในตัวออกแบบเคลื่อนที่ ในแท็บ **ฟิลด์** คลิก **เลือกฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="c18cd-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="c18cd-212">คอลัมน์ในหน้ารายการต้องมีลักษณะคล้ายกับภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="c18cd-213">[![คอลัมน์บนหน้าใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่ที่กำหนดให้กับฉัน](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="c18cd-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="c18cd-214">เพิ่มคอลัมน์ที่จำเป็นจากหน้ารายการที่ต้องแสดงต่อผู้ใช้ในหน้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="c18cd-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="c18cd-215">ลำดับที่คุณเพิ่มเป็นลำดับที่ฟิลด์จะถูกแสดงให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c18cd-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="c18cd-216">วิธีเดียวที่จะเปลี่ยนแปลงลำดับของฟิลด์คือโดยการเลือกฟิลด์ทั้งหมดอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="c18cd-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="c18cd-217">โดยขึ้นอยู่กับข้อกำหนดสำหรับสถานการณ์จำลองนี้ จำเป็นต้องใช้ฟิลด์แปดรายการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="c18cd-218">อย่างไรก็ตาม ผู้ใช้บางรายอาจคิดว่าฟิลด์แปดรายการนั้นมากเกินไปสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c18cd-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="c18cd-219">ดังนั้น เราจะแสดงเฉพาะฟิลด์ที่สำคัญที่สุดในมุมมองรายการมือถือ</span><span class="sxs-lookup"><span data-stu-id="c18cd-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="c18cd-220">ฟิลด์ที่เหลือจะปรากฏในมุมมองรายละเอียดที่เราจะออกแบบในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="c18cd-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="c18cd-221">ในขณะนี้ เราจะเพิ่มฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-221">For now, we will add the following fields.</span></span> <span data-ttu-id="c18cd-222">คลิกเครื่องหมายบวก (**+**) ในคอลัมน์เหล่านี้เพื่อเพิ่มลงในหน้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="c18cd-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="c18cd-223">ชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c18cd-223">Vendor name</span></span>
    - <span data-ttu-id="c18cd-224">ผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-224">Invoice total</span></span>
    - <span data-ttu-id="c18cd-225">บัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-225">Invoice account</span></span>
    - <span data-ttu-id="c18cd-226">หมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-226">Invoice number</span></span>
    - <span data-ttu-id="c18cd-227">วันที่ในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-227">Invoice date</span></span>

    <span data-ttu-id="c18cd-228">หลังจากที่มีการเพิ่มฟิลด์ หน้าบนมือถือจะต้องมีลักษณะคล้ายกับภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="c18cd-229">[![หน้าหลังจากที่มีการเพิ่มฟิลด์](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="c18cd-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="c18cd-230">คุณต้องเพิ่มคอลัมน์ต่อไปนี้ขณะนี้ เพื่อให้เราสามารถเปิดใช้งานการดำเนินการลำดับงานได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="c18cd-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="c18cd-231">แสดง ทำงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c18cd-231">Show complete task</span></span>
    - <span data-ttu-id="c18cd-232">แสดง มอบหมายงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-232">Show delegate task</span></span>
    - <span data-ttu-id="c18cd-233">แสดง เรียกงานคืน</span><span class="sxs-lookup"><span data-stu-id="c18cd-233">Show recall task</span></span>
    - <span data-ttu-id="c18cd-234">แสดง ปฏิเสธงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-234">Show reject task</span></span>
    - <span data-ttu-id="c18cd-235">แสดง งานที่ดำเนินการคำขอเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c18cd-235">Show request completion task</span></span>
    - <span data-ttu-id="c18cd-236">แสดง ส่งงานใหม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-236">Show resubmit task</span></span>

10. <span data-ttu-id="c18cd-237">คลิก **เสร็จสิ้น** เพื่อออกจากโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c18cd-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="c18cd-238">คลิก **ย้อนกลับ** และจากนั้น **เสร็จสิ้น** เพื่อออกจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="c18cd-239">คลิก **เผยแพร่พื้นที่ทำงาน** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="c18cd-240">เปิดใช้งาน **แสดงผลรวมในใบแจ้งหนี้บนรายการใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่** ในแบบฟอร์มพารามิเตอร์บัญชีเจ้าหนี้ภายใต้ **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="c18cd-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="c18cd-241">สังเกตว่าเพียงการเปิดใช้งานพารามิเตอร์นี้ ผลรวมในใบแจ้งหนี้จะถูกคำนวณเพื่อที่จะแสดงในหน้ารายการใบแจ้งหนี้ของผู้จัดจำหน่ายที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="c18cd-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="c18cd-242">นี่คือความสามารถใหม่โดยเป็นส่วนหนึ่งของข้อกำหนดเบื้องต้นโปรแกรมแก้ไขด่วน 3208224</span><span class="sxs-lookup"><span data-stu-id="c18cd-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="c18cd-243">รายละเอียดในใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c18cd-243">Vendor invoice details</span></span>

<span data-ttu-id="c18cd-244">เมื่อต้องการออกแบบหน้ารายละเอียดของใบแจ้งหนี้สำหรับมือถือ ให้ใช้หน้า **VendMobileInvoiceHeaderDetails**</span><span class="sxs-lookup"><span data-stu-id="c18cd-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="c18cd-245">สังเกตว่าหน้านี้จะแสดงใบแจ้งหนี้ที่เก่าที่สุด (ใบแจ้งหนี้ที่สร้างขึ้นก่อน) โดยขึ้นอยู่กับจำนวนใบแจ้งหนี้ที่คุณมีอยู่ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="c18cd-246">เมื่อต้องการค้นหาใบแจ้งหนี้ที่เฉพาะเจาะจง คุณสามารถใช้ตัวกรองด้านซ้ายมือ</span><span class="sxs-lookup"><span data-stu-id="c18cd-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="c18cd-247">อย่างไรก็ตาม เราไม่จำเป็นต้องใช้มใบแจ้งหนี้ที่เฉพาะเจาะจงสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="c18cd-248">เราต้องใช้ข้อมูลใบแจ้งหนี้เพียงบางอย่างเพื่อให้เราสามารถออกแบบหน้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="c18cd-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="c18cd-249">[![หน้าลำดับงาน](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="c18cd-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="c18cd-250">ใน URL แทนที่ชื่อของรายการเมนูด้วย **VendMobileInvoiceHeaderDetails** เพื่อเปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="c18cd-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="c18cd-251">เปิดตัวออกแบบเคลื่อนที่จากปุ่ม **การตั้งค่า** (เกียร์)</span><span class="sxs-lookup"><span data-stu-id="c18cd-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="c18cd-252">คลิกปุ่ม **แก้ไข** เพื่อเริ่มการทำงานของโหมดแก้ไขในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="c18cd-253">เลือกหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่ายของฉัน** ที่คุณสร้างไว้ก่อนหน้านี้ และจากนั้น คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="c18cd-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="c18cd-254">ในแท็บ **ฟิลด์** คลิกส่วนหัวของคอลัมน์ **กริด**</span><span class="sxs-lookup"><span data-stu-id="c18cd-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="c18cd-255">คลิก **คุณสมบัติ &gt; เพิ่มหน้า**</span><span class="sxs-lookup"><span data-stu-id="c18cd-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="c18cd-256">**หมายเหตุ:** เมื่อคุณคลิกส่วนหัว **กริด** และเพิ่มหน้า หน้าความสัมพันธ์พร้อมรายละเอียดถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c18cd-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="c18cd-257">ใส่ชื่อหน้า เช่น **รายละเอียดใบแจ้งหนี้**และคำอธิบาย เช่น **ดูส่วนหัวของใบแจ้งหนี้และรายละเอียดรายการ**</span><span class="sxs-lookup"><span data-stu-id="c18cd-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="c18cd-258">คลิก **เลือกฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="c18cd-258">Click **Select fields**.</span></span> <span data-ttu-id="c18cd-259">สังเกตว่าลำดับที่คุณเพิ่มเป็นลำดับที่ฟิลด์จะถูกแสดงให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c18cd-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="c18cd-260">วิธีเดียวที่จะเปลี่ยนแปลงลำดับของฟิลด์คือโดยการเลือกฟิลด์ทั้งหมดอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="c18cd-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="c18cd-261">เพิ่มฟิลด์ต่อไปนี้จากส่วนหัวโดยขึ้นอยู่กับข้อกำหนดสำหรับสถานการณ์จำลองนี้:</span><span class="sxs-lookup"><span data-stu-id="c18cd-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="c18cd-262">ชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c18cd-262">Vendor name</span></span>
   - <span data-ttu-id="c18cd-263">ผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-263">Invoice total</span></span>
   - <span data-ttu-id="c18cd-264">บัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-264">Invoice account</span></span>
   - <span data-ttu-id="c18cd-265">หมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-265">Invoice number</span></span>
   - <span data-ttu-id="c18cd-266">วันที่ในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-266">Invoice date</span></span>
   - <span data-ttu-id="c18cd-267">คำอธิบายใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-267">Invoice description</span></span>
   - <span data-ttu-id="c18cd-268">วันที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="c18cd-268">Due date</span></span>
   - <span data-ttu-id="c18cd-269">สกุลเงินในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-269">Invoice currency</span></span>

10. <span data-ttu-id="c18cd-270">เพิ่มฟิลด์ต่อไปนี้จากกริดบรรทัดบนหน้า:</span><span class="sxs-lookup"><span data-stu-id="c18cd-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="c18cd-271">ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c18cd-271">Procurement category</span></span>
    - <span data-ttu-id="c18cd-272">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-272">Quantity</span></span>
    - <span data-ttu-id="c18cd-273">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="c18cd-273">Unit price</span></span>
    - <span data-ttu-id="c18cd-274">ยอดเงินสุทธิของรายการ</span><span class="sxs-lookup"><span data-stu-id="c18cd-274">Line net amount</span></span>
    - <span data-ttu-id="c18cd-275">ยอดเงิน 1099</span><span class="sxs-lookup"><span data-stu-id="c18cd-275">1099 amount</span></span>

11. <span data-ttu-id="c18cd-276">หลังจากที่มีการเพิ่มฟิลด์ทั้งหมดจากขั้นตอนสองรายการก่อนหน้านี้ คลิก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="c18cd-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="c18cd-277">หน้าต้องมีลักษณะคล้ายกับภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="c18cd-278">[![หน้าหลังจากที่มีการเพิ่มฟิลด์](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="c18cd-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="c18cd-279">คลิก **เสร็จสิ้น** เพื่อออกจากโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c18cd-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="c18cd-280">คลิก **ย้อนกลับ** และจากนั้น **เสร็จสิ้น** เพื่อออกจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="c18cd-281">คลิก **เผยแพร่พื้นที่ทำงาน** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="c18cd-282">การดำเนินการลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-282">Workflow actions</span></span>

<span data-ttu-id="c18cd-283">เมื่อต้องการเพิ่มการดำเนินการลำดับงาน ใช้หน้า **VendMobileInvoiceHeaderDetails**</span><span class="sxs-lookup"><span data-stu-id="c18cd-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="c18cd-284">เมื่อต้องการเปิดหน้านี้ แทนชื่อของรายการเมนูใน URL ตามที่คุณได้ตั้งค่าไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="c18cd-285">จากนั้นเปิดตัวออกแบบเคลื่อนที่จากปุ่ม **การตั้งค่า** (เกียร์)</span><span class="sxs-lookup"><span data-stu-id="c18cd-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="c18cd-286">ทำตามขั้นตอนเหล่านี้เพื่อเพิ่มการดำเนินการลำดับงานในหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="c18cd-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="c18cd-287">คุณต้องมีใบแจ้งหนี้ที่กำหนดให้กับคุณที่อยู่ในสถานะที่เหมาะสมซึ่งจะทำให้การดำเนินตามการลำดับงานให้พร้อมใช้งานสำหรับคุณที่ในการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="c18cd-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="c18cd-288">บันทึกการดำเนินการลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-288">Record workflow actions</span></span>
1.  <span data-ttu-id="c18cd-289">คลิกปุ่ม **แก้ไข** เพื่อเริ่มการทำงานของโหมดแก้ไขในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="c18cd-290">เลือกหน้า **รายละเอียดใบแจ้งหนี้** ที่คุณสร้างไว้ก่อนหน้านี้ และจากนั้น คลิก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="c18cd-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="c18cd-291">บนแท็บ **การดำเนินการ** ให้คลิก **เพิ่มการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="c18cd-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="c18cd-292">ป้อนชื่อเรื่องการดำเนินการ เช่น **อนุมัติ** และคำอธิบาย เช่น **อนุมัติใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="c18cd-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="c18cd-293">สังเกตว่าชื่อเรื่องการดำเนินการที่คุณป้อนที่นี่กลายเป็นชื่อของการดำเนินการที่แสดงแก่ผู้ใช้ในแอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="c18cd-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="c18cd-294">คลิก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="c18cd-294">Click **Done**.</span></span>
6.  <span data-ttu-id="c18cd-295">คลิก **เลือกฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="c18cd-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="c18cd-296">ทำตามกระบวนการลำดับงานบนหน้า **VendMobileInvoiceHeaderDetails** และทำการดำเนินการที่คุณต้องการบันทึกให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c18cd-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="c18cd-297">ตรวจสอบให้แน่ใจว่าคุณได้ป้อนข้อคิดเห็นเกี่ยวกับลำดับงานระหว่างกระบวนการนี้ เพื่อให้ฟิลด์ข้อคิดเห็นรวมอยู่ในประสบการณ์ใช้งานมือถือ</span><span class="sxs-lookup"><span data-stu-id="c18cd-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="c18cd-298">หลังจากที่มีการรันลำดับงาน คลิก **เสร็จสิ้น** เพื่อดำเนินงานเลือกฟิลด์ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c18cd-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="c18cd-299">คลิก **เสร็จสิ้น** เพื่อออกจากโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c18cd-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="c18cd-300">คลิก **ย้อนกลับ** และจากนั้น **เสร็จสิ้น** เพื่อออกจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="c18cd-301">คลิก **เผยแพร่พื้นที่ทำงาน** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="c18cd-302">ทำซ้ำขั้นตอนก่อนหน้านี้ เพื่อบันทึกการดำเนินการลำดับงานที่จำเป็นทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c18cd-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="c18cd-303">สร้างไฟล์ .js</span><span class="sxs-lookup"><span data-stu-id="c18cd-303">Create a .js file</span></span>
1. <span data-ttu-id="c18cd-304">เปิด Notepad หรือ Microsoft Visual Studio และวางรหัสต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="c18cd-305">บันทึกไฟล์เป็นไฟล์ .js</span><span class="sxs-lookup"><span data-stu-id="c18cd-305">Save the file as a .js file.</span></span> <span data-ttu-id="c18cd-306">รหัสนี้มีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c18cd-306">This code does the following:</span></span>
    - <span data-ttu-id="c18cd-307">ซ่อนคอลัมน์ที่เกี่ยวข้องกับลำดับงานเพิ่มเติมที่เราได้เพิ่มไว้ก่อนหน้านี้ในหน้ารายการมือถือ</span><span class="sxs-lookup"><span data-stu-id="c18cd-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="c18cd-308">เราได้เพิ่มคอลัมน์เหล่านี้เพื่อให้แอพมีข้อมูลดังกล่าวในบริบทและสามารถทำขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="c18cd-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="c18cd-309">ใช้กับตรรกะเพื่อแสดงเฉพาะการดำเนินการเหล่านั้น โดยขึ้นอยู่กับขั้นตอนของลำดับงานที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="c18cd-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c18cd-310">ชื่อหน้าและตัวควบคุมอื่น ๆ ในรหัสต้องมีชื่อเหมือนกันกับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }
    ```

2.  <span data-ttu-id="c18cd-311">อัปโหลดไฟล์รหัสไปยังพื้นที่ทำงานโดยเลือกแท็บ **ตรรกะ**</span><span class="sxs-lookup"><span data-stu-id="c18cd-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="c18cd-312">คลิก **เสร็จสิ้น** เพื่อออกจากโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c18cd-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="c18cd-313">คลิก **ย้อนกลับ** และจากนั้น **เสร็จสิ้น** เพื่อออกจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="c18cd-314">คลิก **เผยแพร่พื้นที่ทำงาน** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="c18cd-315">เอกสารแนบใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c18cd-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="c18cd-316">คลิกปุ่ม **การตั้งค่า** (เกียร์) ในมุมบนขวาของหน้า จากนั้นคลิก **แอพบนมือถือ**</span><span class="sxs-lookup"><span data-stu-id="c18cd-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="c18cd-317">คลิกปุ่ม **แก้ไข** เพื่อเริ่มการทำงานของโหมดแก้ไขในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="c18cd-318">เลือกหน้า  <strong>รายละเอียดใบแจ้งหนี้ \*\*ที่คุณสร้างไว้ก่อนหน้านี้ และจากนั้น คลิก \*\*แก้ไข</strong></span><span class="sxs-lookup"><span data-stu-id="c18cd-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="c18cd-319">ตั้งค่าตัวเลือก **การจัดการเอกสาร** เป็น **ใช่** ตามที่แสดงด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="c18cd-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="c18cd-320">**หมายเหตุ:** ถ้าไม่มีข้อกำหนดในการแสดงเอกสารแนบบนอุปกรณ์เคลื่อนที่ คุณสามารถปล่อยให้ตัวเลือกนี้ถูกตั้งค่าเป็น **ไม่ใช่** ซึ่งเป็นการตั้งค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c18cd-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![การจัดการเอกสาร](./media/docmanagement-216x300.png)

5. <span data-ttu-id="c18cd-322">คลิก **เสร็จสิ้น** เพื่อออกจากโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c18cd-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="c18cd-323">คลิก **ย้อนกลับ** และจากนั้น **เสร็จสิ้น** เพื่อออกจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="c18cd-324">คลิก **เผยแพร่พื้นที่ทำงาน** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="c18cd-325">การกระจายรายการใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c18cd-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="c18cd-326">ข้อกำหนดสำหรับสถานการณ์จำลองนี้ยืนยันว่าจะมีเฉพาะการกระจายระดับบรรทัดเท่านั้น และใบแจ้งหนี้จะมีเพียงบรรทัดเดียวเสมอ</span><span class="sxs-lookup"><span data-stu-id="c18cd-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="c18cd-327">เนื่องจากนี่คือสถานการณ์จำลองที่ปกติ ประสบการณ์การใช้งานผู้ใช้บนอุปกรณ์เคลื่อนที่ก็ต้องง่ายเพียงพอที่จะให้ผู้ใช้ไม่ต้องดูรายละเอียดแนวลึกระดับต่าง ๆ เพื่อดูการกระจาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="c18cd-328">ใบแจ้งหนี้ของผู้จัดจำหน่ายใน ประกอบด้วยตัวเลือกการแสดงการกระจายทั้งหมดจากส่วนหัวของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="c18cd-329">ประสบการณ์นี้เป็นสิ่งที่เราต้องการสำหรับสถานการณ์จำลองแบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c18cd-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="c18cd-330">ดังนั้น เราจะใช้หน้า **VendMobileInvoiceAllDistributionTree** ในการออกแบบนี้ส่วนนี้ของสถานการณ์จำลองแบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c18cd-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="c18cd-331">การทราบถึงความต้องการช่วยให้เราสามารถตัดสินใจได้ว่าควรใช้หน้าเฉพาะใด และควรปรับประสบการณ์ใช้งานมือถือสำหรับผู้ใช้อย่างไรโดยแน่ชัดเมื่อเราออกแบบสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="c18cd-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="c18cd-332">ในสถานการณ์สมมติที่สอง เราจะใช้หน้าอื่นเพื่อแสดงการกระจาย เนื่องจากความต้องการสำหรับสถานการณ์จำลองนั้นแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c18cd-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="c18cd-333">ใน URL นี้ แทนชื่อของรายการเมนูตามที่คุณได้ตั้งค่าไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="c18cd-334">หน้าที่ปรากฏขึ้นควรมีลักษณะคล้ายกับภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="c18cd-335">[![หน้าการกระจายทั้งหมด](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="c18cd-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="c18cd-336">เปิดตัวออกแบบเคลื่อนที่จากปุ่ม **การตั้งค่า** (เกียร์)</span><span class="sxs-lookup"><span data-stu-id="c18cd-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="c18cd-337">คลิกปุ่ม **แก้ไข** เพื่อเริ่มการทำงานของโหมดแก้ไขในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="c18cd-338">**หมายเหตุ:** คุณจะเห็นว่าหน้าใหม่สองหน้านั้นถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c18cd-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="c18cd-339">ระบบจะสร้างหน้าเหล่านี้ เนื่องจากคุณได้เปิดใช้งานการจัดการเอกสารในส่วนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="c18cd-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="c18cd-340">คุณสามารถละเว้นหน้าใหม่เหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="c18cd-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="c18cd-341">คลิก **เพิ่มหน้า**</span><span class="sxs-lookup"><span data-stu-id="c18cd-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="c18cd-342">ใส่ชื่อหน้า เช่น **ดูการบัญชี** และคำอธิบาย เช่น **ดูการบัญชีสำหรับใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="c18cd-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="c18cd-343">คลิก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="c18cd-343">Click **Done**.</span></span>

7.  <span data-ttu-id="c18cd-344">ในแท็บ **ฟิลด์** คลิก **เลือกฟิลด์** เลือกฟิลด์ต่อไปนี้จากหน้าการกระจาย และจากนั้น คลิก **เสร็จสิ้น**:</span><span class="sxs-lookup"><span data-stu-id="c18cd-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="c18cd-345">จำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="c18cd-345">Amount</span></span>
    2.  <span data-ttu-id="c18cd-346">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="c18cd-346">Currency</span></span>
    3.  <span data-ttu-id="c18cd-347">บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="c18cd-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="c18cd-348">เราไม่ได้เลือกคอลัมน์ **คำอธิบาย** จากตารางการกระจาย เนื่องจากความต้องการสำหรับสถานการณ์จำลองนี้ยืนยันว่าราคารวมเป็นจำนวนเดียวที่จะมีการกระจาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="c18cd-349">ดังนั้น ผู้ใช้ไม่จำเป็นต้องมีฟิลด์อื่นที่จะกำหนดชนิดยอดเงินที่มีการกระจาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="c18cd-350">อย่างไรก็ตาม ในสถานการณ์จำลองต่อไป เรา **จะ** ใช้ข้อมูลนี้ เนื่องจากความต้องการสำหรับสถานการณ์จำลองนั้นระบุว่าชนิดยอดเงินอื่น ๆ มีการกระจาย (ตัวอย่างเช่น ภาษีขาย)</span><span class="sxs-lookup"><span data-stu-id="c18cd-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="c18cd-351">คลิก **เสร็จสิ้น** เพื่อออกจากโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c18cd-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="c18cd-352">คลิก **ย้อนกลับ** และจากนั้น **เสร็จสิ้น** เพื่อออกจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="c18cd-353">คลิก **เผยแพร่พื้นที่ทำงาน** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="c18cd-354">กำลังเพิ่มการนำทางไปยังหน้า "ดูการบัญชี"</span><span class="sxs-lookup"><span data-stu-id="c18cd-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="c18cd-355">ในขณะนี้หน้าบนมือถือ **ดูการบัญชี** ไม่ได้มีการเชื่อมโยงกับหน้าบนมือถือที่เราได้ออกแบบไว้</span><span class="sxs-lookup"><span data-stu-id="c18cd-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="c18cd-356">เนื่องจากผู้ใช้ควรจะสามารถนำทางไปยังหน้า **ดูการบัญชี** จากหน้า **รายละเอียดในใบแจ้งหนี้** บนอุปกรณ์เคลื่อนที่ เราต้องให้การนำทางจากหน้า **รายละเอียดใบแจ้งหนี้** ไปยังหน้า **ดูการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="c18cd-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="c18cd-357">เราสร้างการนำทางนี้โดยการใช้ตรรกะเพิ่มเติมผ่าน JavaScript</span><span class="sxs-lookup"><span data-stu-id="c18cd-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="c18cd-358">เปิดไฟล์ .js ที่คุณสร้างไว้ก่อนหน้านี้ และเพิ่มบรรทัดที่เน้นในรหัสต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="c18cd-359">รหัสนี้ทำสองสิ่ง:</span><span class="sxs-lookup"><span data-stu-id="c18cd-359">This code does two things:</span></span>
    1.  <span data-ttu-id="c18cd-360">ซึ่งจะช่วยรับประกันว่าผู้ใช้จะไม่สามารถนำทางได้โดยตรงจากพื้นที่ทำงานไปยังหน้า **ดูการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="c18cd-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="c18cd-361">จะสร้างตัวควบคุมการนำทางจากหน้า **รายละเอียดใบแจ้งหนี้** ไปยังหน้า **ดูการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="c18cd-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="c18cd-362">ชื่อหน้าและตัวควบคุมอื่น ๆ ในรหัสต้องมีชื่อเหมือนกันกับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }
    ```
    
2.  <span data-ttu-id="c18cd-363">อัปโหลดไฟล์รหัสไปยังพื้นที่ทำงานโดยเลือกแท็บ **ตรรกะ** เพื่อบันทึกทับรหัสก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="c18cd-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="c18cd-364">คลิก **เสร็จสิ้น** เพื่อออกจากโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c18cd-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="c18cd-365">คลิก **ย้อนกลับ** และจากนั้น **เสร็จสิ้น** เพื่อออกจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="c18cd-366">คลิก **เผยแพร่พื้นที่ทำงาน** เพื่อบันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="c18cd-367">การตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c18cd-367">Validation</span></span>

<span data-ttu-id="c18cd-368">จากอุปกรณ์เคลื่อนที่ของคุณ เปิดแอพ และเชื่อมต่อกับอินสแตนซ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="c18cd-369">ตรวจสอบให้แน่ใจว่าคุณลงชื่อเข้าใช้ไปยังบริษัทที่ใบแจ้งหนี้ของผู้จัดจำหน่ายมีการกำหนดให้กับคุณสำหรับการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="c18cd-370">คุณควรจะสามารถดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c18cd-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="c18cd-371">ดูพื้นที่ทำงาน **การอนุมัติของฉัน**</span><span class="sxs-lookup"><span data-stu-id="c18cd-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="c18cd-372">เข้าถึงรายละเอียดข้อมูลพื้นที่ทำงาน **การอนุมัติของฉัน** และดูหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่ายของฉัน**</span><span class="sxs-lookup"><span data-stu-id="c18cd-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="c18cd-373">เข้าถึงรายละเอียดข้อมูลหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่ายของฉัน** และดูรายการของใบแจ้งหนี้ที่กำหนดให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="c18cd-374">เข้าถึงรายละเอียดข้อมูลของหนึ่งในใบแจ้งหนี้เหล่านี้ และดูรายละเอียดส่วนหัวของใบแจ้งหนี้และรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="c18cd-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="c18cd-375">บนหน้ารายละเอียด ดูการเชื่อมโยงไปยังเอกสารแนบ และใช้การเชื่อมโยงนี้เพื่อนำทางไปยังรายการเอกสารแนบ และดูเอกสารแนบ</span><span class="sxs-lookup"><span data-stu-id="c18cd-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="c18cd-376">บนหน้ารายละเอียด ดูการเชื่อมโยงไปยังหน้า **ดูการบัญชี** และใช้การเชื่อมโยงนี้เพื่อนำทางไปยังหน้าการกระจาย และดูการกระจาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="c18cd-377">บนหน้ารายละเอียด คลิกเมนู **การดำเนินการ** ที่ด้านล่าง และทำการดำเนินการลำดับงานที่สามารถใช้กับขั้นตอนของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c18cd-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="c18cd-378">การออกแบบสถานการณ์จำลองการอนุมัติใบแจ้งหนี้ที่ซับซัอนสำหรับ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c18cd-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c18cd-379">แอททริบิวต์สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="c18cd-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="c18cd-380">รับสาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c18cd-381">ฟิลด์ใดบ้างจากส่วนหัวของใบแจ้งหนี้ที่ผู้ใช้จะต้องการดูในประสบการณ์การใช้งานมือถือและในลำดับใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="c18cd-382">ชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c18cd-382">Vendor name</span></span></li>
<li><span data-ttu-id="c18cd-383">จำนวนเงินในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-383">Invoice amount</span></span></li>
<li><span data-ttu-id="c18cd-384">บัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-384">Invoice account</span></span></li>
<li><span data-ttu-id="c18cd-385">หมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-385">Invoice number</span></span></li>
<li><span data-ttu-id="c18cd-386">วันที่ในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-386">Invoice date</span></span></li>
<li><span data-ttu-id="c18cd-387">คำอธิบายใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-387">Invoice description</span></span></li>
<li><span data-ttu-id="c18cd-388">วันที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="c18cd-388">Due date</span></span></li>
<li><span data-ttu-id="c18cd-389">สกุลเงินในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c18cd-390">ฟิลด์ใดบ้างจากรายการใบแจ้งหนี้ที่ผู้ใช้จะต้องการดูในประสบการณ์การใช้งานมือถือและในลำดับใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="c18cd-391">ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="c18cd-391">Procurement category</span></span></li>
<li><span data-ttu-id="c18cd-392">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-392">Quantity</span></span></li>
<li><span data-ttu-id="c18cd-393">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="c18cd-393">Unit price</span></span></li>
<li><span data-ttu-id="c18cd-394">ยอดเงินสุทธิของรายการ</span><span class="sxs-lookup"><span data-stu-id="c18cd-394">Line net amount</span></span></li>
<li><span data-ttu-id="c18cd-395">ยอดเงิน 1099</span><span class="sxs-lookup"><span data-stu-id="c18cd-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c18cd-396">มีบรรทัดใบแจ้งหนี้ในใบแจ้งหนี้จำนวนเท่าใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="c18cd-397">ใช้กฎ 80-20 และปรับให้เหมาะสมกับ 80 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="c18cd-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="c18cd-398">5</span><span class="sxs-lookup"><span data-stu-id="c18cd-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c18cd-399">ผู้ใช้จะต้องการดูการกระจายการลงบัญชี (การกำหนดรหัสใบแจ้งหนี้) บนอุปกรณ์เคลื่อนที่ในระหว่างการตรวจทานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="c18cd-400">ใช่</span><span class="sxs-lookup"><span data-stu-id="c18cd-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c18cd-401">มีการกระจายการลงบัญชี (ราคารวม ภาษีขาย ค่าธรรมเนียม และอื่น ๆ) สำหรับรายการใบแจ้งหนี้จำนวนเท่าใด</span><span class="sxs-lookup"><span data-stu-id="c18cd-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="c18cd-402">ใช้กฎ 80-20 อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="c18cd-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="c18cd-403">ราคารวม: 2 ภาษีขาย: 2 ค่าธรรมเนียม: 2</span><span class="sxs-lookup"><span data-stu-id="c18cd-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c18cd-404">ใบแจ้งหนี้มีการกระจายการลงบัญชีในส่วนหัวของใบแจ้งหนี้ด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="c18cd-405">ถ้าเป็นเช่นนั้น กระจายการลงบัญชีเหล่านี้ควรพร้อมใช้งานบนอุปกรณ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="c18cd-406">ไม่ได้ใช้</span><span class="sxs-lookup"><span data-stu-id="c18cd-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c18cd-407">ผู้ใช้จะต้องการดูเอกสารแนบสำหรับใบแจ้งหนี้บนอุปกรณ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c18cd-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="c18cd-408">ใช่</span><span class="sxs-lookup"><span data-stu-id="c18cd-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="c18cd-409">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c18cd-409">Next steps</span></span>

<span data-ttu-id="c18cd-410">คุณสามารถทำการเปลี่ยนแปลงต่อไปนี้ให้เสร็จสิ้นได้สำหรับสถานการณ์จำลอง 1 ขึ้นอยู่กับความต้องการสำหรับสถานการณ์จำลอง 2</span><span class="sxs-lookup"><span data-stu-id="c18cd-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="c18cd-411">คุณสามารถใช้ส่วนนี้เพื่อปรับปรุงประสบการณ์การใช้งานของแอพบนมือถือของคุณ</span><span class="sxs-lookup"><span data-stu-id="c18cd-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="c18cd-412">เนื่องจากควรมีรายการในใบแจ้งหนี้เพิ่มเติมในสถานการณ์จำลอง 2 การเปลี่ยนแปลงการออกแบบต่อไปนี้จะช่วยปรับประสบการณ์ผู้ใช้บนอุปกรณ์เคลื่อนที่ให้เหมาะสม:</span><span class="sxs-lookup"><span data-stu-id="c18cd-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="c18cd-413">แทนการดูรายการในใบแจ้งหนี้บนหน้ารายละเอียด (เช่นในสถานการณ์จำลอง 1) ผู้ใช้สามารถเลือกที่จะดูรายการบนหน้าบนมือถือแยกต่างหากได้</span><span class="sxs-lookup"><span data-stu-id="c18cd-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="c18cd-414">เนื่องจากต้องการรายการในใบแจ้งหนี้มากกว่าหนึ่งรายการในสถานการณ์จำลองนี้ ถ้าหน้า **VendMobileInvoiceAllDistributionTree** ถูกใช้ในการออกแบบหน้าการกระจายสำหรับอุปกรณ์เคลื่อนที่ (ดังเช่นในสถานการณ์จำลอง 1) ผู้ใช้อาจสับสนที่จะสร้างเชื่อมโยงรายการกับการกระจาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="c18cd-415">ดังนั้น ใช้หน้า **VendMobileInvoiceLineDistributionTree** เพื่อออกแบบหน้าการกระจาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="c18cd-416">ทางที่ดีที่สุดคือการกระจายควรแสดงอยู่ในบริบทของรายการในใบแจ้งหนี้ในสถานการณ์จำลองนี้</span><span class="sxs-lookup"><span data-stu-id="c18cd-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="c18cd-417">ดังนั้น โปรดตรวจสอบให้แน่ใจว่าผู้ใช้สามารถเข้าถึงรายการเพื่อดูหน้าการกระจาย</span><span class="sxs-lookup"><span data-stu-id="c18cd-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="c18cd-418">ใช้ความสามารถในการเชื่อมโยงหน้าเพื่อสร้างการเจาะลึก เช่นเดียวกับที่คุณดำเนินการกับส่วนหัวและหน้ารายละเอียดในสถานการณ์จำลอง 1</span><span class="sxs-lookup"><span data-stu-id="c18cd-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="c18cd-419">เนื่องจากคาดว่าจะมีชนิดยอดเงินมากกว่าหนึ่งชนิดในการกระจายในสถานการณ์จำลอง 2 (ภาษีขาย ค่าธรรมเนียม และอื่น ๆ) จึงควรแสดงคำอธิบายของชนิดยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="c18cd-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="c18cd-420">(เราละเว้นข้อมูลนี้ในสถานการณ์จำลอง 1)</span><span class="sxs-lookup"><span data-stu-id="c18cd-420">(We omitted this information in scenario 1.)</span></span>




