---
title: การรายงานทางการเงิน
description: การรายงานทางการเงินยินยอมให้ผู้เชี่ยวชาญทางการเงินและผู้เชี่ยวชาญทางธุรกิจสามารถสร้าง รักษา ปรับใช้ และดูงบการเงินได้
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b6682295aa53acd5d3d6964c56ff7bcfcd59379d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568810"
---
# <a name="financial-reporting"></a><span data-ttu-id="fd5b6-103">การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-103">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd5b6-104">การรายงานทางการเงินสำหรับแอพพลิเคชั่นยินยอมให้ผู้เชี่ยวชาญทางการเงินและผู้เชี่ยวชาญทางธุรกิจสามารถสร้าง รักษา ปรับใช้ และดูงบการเงินได้</span><span class="sxs-lookup"><span data-stu-id="fd5b6-104">Financial reporting for the application allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="fd5b6-105">ซึ่งสามารถใช้งานได้เกินกว่าข้อจำกัดการรายงานดั้งเดิมเพื่อช่วยให้คุณสามารถออกแบบรายงานชนิดต่างๆ ได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-105">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="fd5b6-106">รายงานทางการเงินประกอบด้วยการสนับสนุนมิติ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-106">Financial reporting includes dimension support.</span></span> <span data-ttu-id="fd5b6-107">ดังนั้น เซ็กเมนต์บัญชีหรือมิติพร้อมใช้งานทันที</span><span class="sxs-lookup"><span data-stu-id="fd5b6-107">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="fd5b6-108">ไม่จำเป็นต้องมีเครื่องมือเพิ่มเติมหรือขั้นตอนการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="fd5b6-108">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="fd5b6-109">การตั้งค่าการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-109">Financial reporting setup</span></span>
<span data-ttu-id="fd5b6-110">หน้า **ตั้งค่าการรายงานทางการเงิน** มีรายการของมิติทางการเงินทั้งหมดในระบบ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-110">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="fd5b6-111">**บัญชีแยกประเภททั่วไป** \> **การตั้งค่าบัญชีแยกประเภท** \> **การตั้งค่าการรายงานทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="fd5b6-111">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="fd5b6-112">หน้า **การตั้งค่าการรายงานทางการเงิน** มีสองส่วน ซึ่งระบุข้อมูลที่คุณรายงานในการรายงานทางการเงิน:</span><span class="sxs-lookup"><span data-stu-id="fd5b6-112">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="fd5b6-113">**แท็บมิติ** - เนื่องจากบริษัทต่างๆ ใช้โครงสร้างทางบัญชีและมิติที่ต่างกัน ไม่มีวิธีการกำหนดใบสั่งที่ผู้ใช้ต้องการดูมิติทางการเงินทั้งหมดในรายงาน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-113">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="fd5b6-114">หน้านี้ช่วยให้คุณสามารถตั้งค่าใบสั่งที่คุณต้องการให้มิติทางการเงินไปปรากฏขึ้น เมื่อคุณสร้าง และดูรายงานในการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-114">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="fd5b6-115">**แท็บแอททริบิวต์** คือที่ซึ่งคุณสามารถเลือกได้ว่าคุณต้องการความสามารถในการใช้ **ผู้จัดจำหน่าย** และ **ลูกค้า** เป็นแอททริบิวต์สำหรับการออกแบบรายงานและการกรองข้อมูลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd5b6-115">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="fd5b6-116">การรายงานเกี่ยวกับผู้จัดจำหน่ายและลูกค้าจะมีประโยชน์ เฉพาะถ้าคุณไม่ได้ป้อนผู้จัดจำหน่ายหรือลูกค้าหลายรายการในใบสำคัญเดียว เมื่อลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="fd5b6-116">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="fd5b6-117">การเลือกผู้จัดจำหน่ายและ/หรือลูกค้า จะเพิ่มเวลาเพิ่มเติมในการรวม</span><span class="sxs-lookup"><span data-stu-id="fd5b6-117">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="fd5b6-118">ส่วนประกอบของการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-118">Financial reporting components</span></span>
<span data-ttu-id="fd5b6-119">ส่วนประกอบต่อไปนี้ของการรายงานทางการเงินทำให้ง่ายต่อการใช้เพื่อสร้าง ดู และจัดกำหนดการรายงาน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-119">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="fd5b6-120">ส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-120">Component</span></span>        | <span data-ttu-id="fd5b6-121">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-121">Functions</span></span> | <span data-ttu-id="fd5b6-122">ข้อมูลเพิ่มเติม:</span><span class="sxs-lookup"><span data-stu-id="fd5b6-122">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="fd5b6-123">โปรแกรมออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-123">Report Designer</span></span>  | <span data-ttu-id="fd5b6-124">สร้างส่วนประกอบรายงานที่อาจถูกรวมเพื่อกำหนด และสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-124">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="fd5b6-125">วิซาร์ดรายงานจะแนะนำผู้ใช้ที่มีประสบการณ์น้อยผ่านกระบวนการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-125">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="fd5b6-126">ผู้ใช้ขั้นสูงสามารถสร้างส่วนประกอบรายงานใหม่ หรือปรับเปลี่ยนส่วนประกอบที่มีอยู่เพื่อตอบสนองความต้องการ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-126">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="fd5b6-127">รายงานกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-127">Report schedules</span></span> | <span data-ttu-id="fd5b6-128">จัดกำหนดการรายงานเดี่ยวหรือกลุ่มของรายงานเพื่อสร้างเป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-128">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="fd5b6-129">สร้างรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-129">Generate financial reports</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="fd5b6-130">ลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-130">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="fd5b6-131">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-131">Feature</span></span></th>
<th><span data-ttu-id="fd5b6-132">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="fd5b6-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fd5b6-133">รายงานความยืดหยุ่นในการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-133">Report design flexibility</span></span></td>
<td><span data-ttu-id="fd5b6-134">Report Designer มีคุณลักษณะตัวเลือกการรายงานดังต่อไปนี้ เมื่อคุณออกแบบรายงาน:</span><span class="sxs-lookup"><span data-stu-id="fd5b6-134">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="fd5b6-135">บันทึกชุดข้อมูลมิติ และนำมิติมาใช้ใหม่สำหรับรายงานหลายฉบับ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-135">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="fd5b6-136">ควบคุมวิธีการจัดรูปแบบและการแสดงคำอธิบายเกี่ยวกับมิติ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-136">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="fd5b6-137">ระบุบัญชีหรือมิติที่มีการตัดออกจากส่วนประกอบรายงาน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-137">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="fd5b6-138">ส่วนหัวของรูปแบบสำหรับการคาดการณ์สะสม</span><span class="sxs-lookup"><span data-stu-id="fd5b6-138">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="fd5b6-139">การทำงานร่วมกันกับรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-139">Financial report collaboration</span></span></td>
<td><span data-ttu-id="fd5b6-140">คุณลักษณะต่อไปนี้ช่วยให้คุณสามารถจัดการการสร้างและการเผยแพร่รายงานได้:</span><span class="sxs-lookup"><span data-stu-id="fd5b6-140">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="fd5b6-141">กำหนดการรายงานเพื่อสร้างอยู่บนพื้นฐานรายวัน รายสัปดาห์ รายเดือน หรือรายปี โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-141">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="fd5b6-142">ส่งออกไปยังรูปแบบอ่านอย่างเดียว XPS ซึ่งให้ความปลอดภัยของเอกสารมากขึ้น ด้วยลายเซ็นดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="fd5b6-142">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="fd5b6-143">ส่งออกไปยังเวิร์กชีต Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="fd5b6-143">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="fd5b6-144">เพื่อแบ่งปันรายงาน คุณสามารถสร้างข้อความอีเมล์ที่ประกอบด้วยลิงค์ไปที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-144">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="fd5b6-145">การดูรายงานเชิงโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="fd5b6-145">Interactive report viewing</span></span></td>
<td><span data-ttu-id="fd5b6-146">คุณลักษณะแบบโต้ตอบช่วยให้คุณสามารถดำเนินงานต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="fd5b6-146">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="fd5b6-147">เปลี่ยนวันที่รายงานของรายงานที่คุณกำลังดู</span><span class="sxs-lookup"><span data-stu-id="fd5b6-147">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="fd5b6-148">เปลี่ยนสกุลเงินของรายงานที่คุณกำลังดู</span><span class="sxs-lookup"><span data-stu-id="fd5b6-148">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="fd5b6-149">ดูรายงานในมุมมองสรุปหรือมุมมองโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="fd5b6-149">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="fd5b6-150">เพิ่มตัวกรองมิติเพื่อจำกัดเนื้อหารายงานไปยังมิติหรือชุดของมิติที่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="fd5b6-150">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="fd5b6-151">เพิ่มตัวกรองแอททริบิวต์เพื่อจำกัดเนื้อหารายงานไปยังแอททริบิวต์หรือชุดของแอททริบิวต์ที่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="fd5b6-151">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="fd5b6-152">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fd5b6-152">Additional resources</span></span>
[<span data-ttu-id="fd5b6-153">สร้างรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="fd5b6-153">Generate financial reports</span></span>](generate-financial-report.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]