---
title: "ข้อกำหนดของรายงานในผู้ออกแบบรายงานทางการเงิน"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับข้อกำหนดของรายงาน ข้อกำหนดของรายงานคือส่วนประกอบของรายงาน (หรือบล็อคส่วนประกอบ) ที่ใช้คำนิยามแถว คำนิยามคอลัมน์ และคำนิยามแผนภูมิรายงานเพิ่มเติมเพื่อสร้างรายงาน ข้อกำหนดของรายงานยังมีตัวเลือกและการตั้งค่าสำหรับการปรับแต่งรายงานด้วยตนเองอีกด้วย"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 58030df8db467f754ec93ecc3f41585b20f03893
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="88049-105">ข้อกำหนดของรายงานในผู้ออกแบบรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="88049-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="88049-106">บทความนี้แสดงข้อมูลเกี่ยวกับข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-106">This article provides information about report definitions.</span></span> <span data-ttu-id="88049-107">ข้อกำหนดของรายงานคือส่วนประกอบของรายงาน (หรือบล็อคส่วนประกอบ) ที่ใช้คำนิยามแถว คำนิยามคอลัมน์ และคำนิยามแผนภูมิรายงานเพิ่มเติมเพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="88049-108">ข้อกำหนดของรายงานยังมีตัวเลือกและการตั้งค่าสำหรับการปรับแต่งรายงานด้วยตนเองอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="88049-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="88049-109">ข้อกำหนดของรายงานคือส่วนประกอบของรายงาน (หรือบล็อคส่วนประกอบ) ที่ใช้คำนิยามแถว คำนิยามคอลัมน์ และคำนิยามแผนภูมิรายงานเพิ่มเติมเพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="88049-110">คำนิยามรายงานยังแสดงตัวเลือก และการตั้งค่าที่คุณสามารถกำหนดรายงานเอง</span><span class="sxs-lookup"><span data-stu-id="88049-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="88049-111">หลังจากที่คุณกำหนดคำนิยามแถวและคำนิยามคอลัมน์ คุณต้องรวมค่าดังกล่าวในข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="88049-112">ณ จุดนี้ คุณยังสามารถกำหนดแง่มุมอื่นๆ ของคำนิยาม เช่นระดับรายละเอียดและวันที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="88049-113">จากนั้นคุณสามารถบันทึกและสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-113">You can then save and generate a report.</span></span> <span data-ttu-id="88049-114">การรายงานทางการเงินมีรายละเอียดในระดับต่าง ๆ ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88049-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="88049-115">การเงิน</span><span class="sxs-lookup"><span data-stu-id="88049-115">Financial</span></span>
-   <span data-ttu-id="88049-116">การเงินและการบัญชี</span><span class="sxs-lookup"><span data-stu-id="88049-116">Financial and Account</span></span>
-   <span data-ttu-id="88049-117">การเงิน การบัญชีและธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="88049-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="88049-118">อย่างไรก็ตาม ขึ้นอยู่กับวิธีเก็บข้อมูลในระบบ Microsoft Dynamics ERP รายละเอียดธุรกรรมอาจไม่มีอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="88049-119">สร้างข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-119">Create a report definition</span></span>
1.  <span data-ttu-id="88049-120">ในโปรแกรมออกแบบรายงาน บนไฟล์ **เมนู** คลิก **สร้าง**แล้ว เลือก **ข้อกำหนดของรายงาน**</span><span class="sxs-lookup"><span data-stu-id="88049-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="88049-121">ระบุข้อมูลที่เหมาะสมบน **รายงาน** **ผลที่ได้และการกระจาย**, **หัวกระดาษและท้ายกระดาษ**และแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="88049-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="88049-122">เนื้อหาของข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-122">Contents of a report definition</span></span>
<span data-ttu-id="88049-123">ตารางต่อไปนี้อธิบายถึงแท็บในข้อกำหนดของรายงานและวิธีใช้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="88049-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88049-124">แท็บ</span><span class="sxs-lookup"><span data-stu-id="88049-124">Tab</span></span></th>
<th><span data-ttu-id="88049-125">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="88049-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88049-126">รายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-126">Report</span></span></td>
<td><span data-ttu-id="88049-127">สร้างรายงาน ตั้งค่าคอนฟิกรายงาน หรือปรับแก้รายงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="88049-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88049-128">ผลที่ได้และการกระจาย</span><span class="sxs-lookup"><span data-stu-id="88049-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="88049-129">เปลี่ยนชนิดของผลที่ได้และปลายทางของรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88049-130">หัวกระดาษและท้ายกระดาษ</span><span class="sxs-lookup"><span data-stu-id="88049-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="88049-131">กำหนดและจัดรูปแบบหัวกระดาษและท้ายกระดาษสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="88049-132">ตัวอย่างเช่น คุณสามารถเพิ่มรูปภาพหรือข้อความในหัวกระดาษหรือท้ายกระดาษ</span><span class="sxs-lookup"><span data-stu-id="88049-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="88049-133">การรายงานทางการเงินสนับสนุนไฟล์ .bmp, .jpg และ.png สำหรับรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="88049-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="88049-134">คุณยังสามารถเพิ่มรหัสข้อความอัตโนมัติเพื่อแทรกข้อมูลอื่น เช่น ชื่อบริษัท ชื่อรายงาน หรือหมายเลขหน้า</span><span class="sxs-lookup"><span data-stu-id="88049-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88049-135">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="88049-135">Settings</span></span></td>
<td><span data-ttu-id="88049-136">ระบุการตั้งค่าข้อกำหนดของรายงาน เช่น การตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="88049-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="88049-137">การจัดรูปแบบและการปัดเศษยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="88049-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="88049-138">จัดรูปแบบรายละเอียดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-138">Format detail reports</span></span></li>
<li><span data-ttu-id="88049-139">จัดรูปแบบแผนภูมิการรายงาน</span><span class="sxs-lookup"><span data-stu-id="88049-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="88049-140">สร้างรายงานข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="88049-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="88049-141">ระบุการแปลงสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="88049-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="88049-142">ผลรวมย่อยและรายละเอียดตัวกรองบัญชี</span><span class="sxs-lookup"><span data-stu-id="88049-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="88049-143">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="88049-143">See also</span></span>
--------

[<span data-ttu-id="88049-144">การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="88049-144">Financial reporting</span></span>](financial-reporting-intro.md)




