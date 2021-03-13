---
title: ข้อกำหนดของรายงานในผู้ออกแบบรายงานทางการเงิน
description: บทความนี้แสดงข้อมูลเกี่ยวกับข้อกำหนดของรายงาน
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7d5531112cfb803912849af3af785b2a69a79f3d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093425"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="ed465-103">ข้อกำหนดของรายงานในผู้ออกแบบรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ed465-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed465-104">บทความนี้แสดงข้อมูลเกี่ยวกับข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-104">This article provides information about report definitions.</span></span> <span data-ttu-id="ed465-105">ข้อกำหนดของรายงานคือส่วนประกอบของรายงาน (หรือบล็อคส่วนประกอบ) ที่ใช้คำนิยามแถว คำนิยามคอลัมน์ และคำนิยามแผนภูมิรายงานเพิ่มเติมเพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="ed465-106">ข้อกำหนดของรายงานยังมีตัวเลือกและการตั้งค่าสำหรับการปรับแต่งรายงานด้วยตนเองอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="ed465-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="ed465-107">ข้อกำหนดของรายงานคือส่วนประกอบของรายงาน (หรือบล็อคส่วนประกอบ) ที่ใช้คำนิยามแถว คำนิยามคอลัมน์ และคำนิยามแผนภูมิรายงานเพิ่มเติมเพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="ed465-108">คำนิยามรายงานยังแสดงตัวเลือก และการตั้งค่าที่คุณสามารถกำหนดรายงานเอง</span><span class="sxs-lookup"><span data-stu-id="ed465-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="ed465-109">หลังจากที่คุณกำหนดคำนิยามแถวและคำนิยามคอลัมน์ คุณต้องรวมค่าดังกล่าวในข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="ed465-110">ณ จุดนี้ คุณยังสามารถกำหนดแง่มุมอื่นๆ ของคำนิยาม เช่นระดับรายละเอียดและวันที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="ed465-111">จากนั้นคุณสามารถบันทึกและสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-111">You can then save and generate a report.</span></span> <span data-ttu-id="ed465-112">การรายงานทางการเงินมีรายละเอียดในระดับต่าง ๆ ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ed465-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="ed465-113">การเงิน</span><span class="sxs-lookup"><span data-stu-id="ed465-113">Financial</span></span>
- <span data-ttu-id="ed465-114">การเงินและการบัญชี</span><span class="sxs-lookup"><span data-stu-id="ed465-114">Financial and Account</span></span>
- <span data-ttu-id="ed465-115">การเงิน การบัญชีและธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ed465-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="ed465-116">อย่างไรก็ตาม โดยขึ้นอยู่กับวิธีการจัดเก็บข้อมูลในระบบ Microsoft Dynamics ERP รายละเอียดธุรกรรมอาจไม่พร้อมใช้งานในรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="ed465-117">สร้างข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-117">Create a report definition</span></span>
1. <span data-ttu-id="ed465-118">ในโปรแกรมออกแบบรายงาน บนไฟล์ **เมนู** คลิก **สร้าง** แล้ว เลือก **ข้อกำหนดของรายงาน**</span><span class="sxs-lookup"><span data-stu-id="ed465-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="ed465-119">ระบุข้อมูลที่เหมาะสมบน **รายงาน** **ผลที่ได้และการกระจาย**, **หัวกระดาษและท้ายกระดาษ** และแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="ed465-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="ed465-120">เนื้อหาของข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-120">Contents of a report definition</span></span>
<span data-ttu-id="ed465-121">ตารางต่อไปนี้อธิบายถึงแท็บในข้อกำหนดของรายงานและวิธีใช้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ed465-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ed465-122">แท็บ</span><span class="sxs-lookup"><span data-stu-id="ed465-122">Tab</span></span></th>
<th><span data-ttu-id="ed465-123">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="ed465-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ed465-124">รายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-124">Report</span></span></td>
<td><span data-ttu-id="ed465-125">สร้างรายงาน ตั้งค่าคอนฟิกรายงาน หรือปรับแก้รายงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="ed465-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed465-126">ผลที่ได้และการกระจาย</span><span class="sxs-lookup"><span data-stu-id="ed465-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="ed465-127">เปลี่ยนชนิดของผลที่ได้และปลายทางของรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed465-128">หัวกระดาษและท้ายกระดาษ</span><span class="sxs-lookup"><span data-stu-id="ed465-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="ed465-129">กำหนดและจัดรูปแบบหัวกระดาษและท้ายกระดาษสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="ed465-130">ตัวอย่างเช่น คุณสามารถเพิ่มรูปภาพหรือข้อความในหัวกระดาษหรือท้ายกระดาษ</span><span class="sxs-lookup"><span data-stu-id="ed465-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="ed465-131">การรายงานทางการเงินสนับสนุนไฟล์ .bmp, .jpg และ.png สำหรับรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="ed465-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="ed465-132">คุณยังสามารถเพิ่มรหัสข้อความอัตโนมัติเพื่อแทรกข้อมูลอื่น เช่น ชื่อบริษัท ชื่อรายงาน หรือหมายเลขหน้า</span><span class="sxs-lookup"><span data-stu-id="ed465-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed465-133">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="ed465-133">Settings</span></span></td>
<td><span data-ttu-id="ed465-134">ระบุการตั้งค่าข้อกำหนดของรายงาน เช่น การตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ed465-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="ed465-135">การจัดรูปแบบและการปัดเศษยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="ed465-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="ed465-136">จัดรูปแบบรายละเอียดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-136">Format detail reports</span></span></li>
<li><span data-ttu-id="ed465-137">จัดรูปแบบแผนภูมิการรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed465-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="ed465-138">สร้างรายงานข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="ed465-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="ed465-139">ระบุการแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="ed465-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="ed465-140">ผลรวมย่อยและรายละเอียดตัวกรองบัญชี</span><span class="sxs-lookup"><span data-stu-id="ed465-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="ed465-141">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ed465-141">Additional resources</span></span>

[<span data-ttu-id="ed465-142">การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ed465-142">Financial reporting</span></span>](financial-reporting-intro.md)
