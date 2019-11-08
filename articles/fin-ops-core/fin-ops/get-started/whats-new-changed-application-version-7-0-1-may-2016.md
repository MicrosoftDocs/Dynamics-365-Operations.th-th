---
title: มีอะไรใหม่หรือเปลี่ยนแปลงในแอพลิเคชัน Dynamics AX รุ่น 7.0.1 (พฤษภาคม 2016)
description: บทความนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงในแอพลิเคชัน Microsoft Dynamics AX รุ่น 7.0.1 รุ่นนี้ถูกนำออกใช้ในเดือนพฤษภาคม 2016 และมีหมายเลขรุ่นคือ 7.0.1265.23014
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 4524eb14ff06561ad186cf63654e6a716632a3f4
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627624"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="63f14-104">มีอะไรใหม่หรือเปลี่ยนแปลงในแอพลิเคชัน Dynamics AX รุ่น 7.0.1 (พฤษภาคม 2016)</span><span class="sxs-lookup"><span data-stu-id="63f14-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63f14-105">บทความนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงในแอพลิเคชัน Microsoft Dynamics AX รุ่น 7.0.1</span><span class="sxs-lookup"><span data-stu-id="63f14-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="63f14-106">รุ่นนี้ถูกนำออกใช้ในเดือนพฤษภาคม 2016 และมีหมายเลขรุ่นคือ 7.0.1265.23014</span><span class="sxs-lookup"><span data-stu-id="63f14-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="63f14-107">การรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="63f14-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="63f14-108">คุณสามารถทำอะไร</span><span class="sxs-lookup"><span data-stu-id="63f14-108">What can you do?</span></span> | <span data-ttu-id="63f14-109">ทำไมนี่เป็นสิ่งสำคัญ</span><span class="sxs-lookup"><span data-stu-id="63f14-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="63f14-110">ตั้งค่าคอนฟิกกล่องโต้ตอบเวลาที่ใช้ในการผลิตสำหรับการออกแบบรายงานการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อให้ผู้ใช้สามารถเลือกมิติทางการเงินที่พวกเขาต้องการได้</span><span class="sxs-lookup"><span data-stu-id="63f14-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="63f14-111">ระหว่าวดำเนินการ ในกล่องโต้ตอบสำหรับการรันรายงาน ER ผู้ใช้สามารถเลือกมิติทางการเงินหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="63f14-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="63f14-112">รายละเอียดของมิติทางการเงินที่เลือกจะปรากฏในเอกสารทางอิเล็กทรอนิกส์ที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="63f14-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="63f14-113">ตั้งค่าคอนฟิกการเข้าถึงมิติทางการเงินหลายรายการในระหว่างการออกแบบของรายงาน ER ผ่านการแม็ปเดียวไปยังแหล่งข้อมูลที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="63f14-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="63f14-114">สามารถใช้การตั้งค่าคอนฟิกรายงาน ER เดียวกันในการสร้างเอกสารอิเล็กทรอนิกส์ที่มีข้อมูลธุรกรรมพร้อมกับรายละเอียดของมิติทางการเงิน โดยไม่คำนึงถึงจำนวนของมิติทางการเงินที่เลือกโดยผู้ใช้หรือที่ตั้งค่าคอนฟิกสำหรับนิติบุคคลหรืออินสแตนซ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="63f14-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="63f14-115">ตั้งค่าคอนฟิกรายงาน ER เพื่อป้อนข้อมูลในคอลัมน์ที่สร้างขึ้นแบบไดนามิกของเอกสารอิเล็กทรอนิกส์ที่สร้างขึ้นในรูปแบบของแผ่นงาน OPENXML</span><span class="sxs-lookup"><span data-stu-id="63f14-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="63f14-116">รายงาน ER สามารถป้อนข้อมูลในแผ่นงาน OPENXML ที่ถูกสร้างขึ้นผ่านคอลัมน์ที่จำลองแบบตามแนวนอน</span><span class="sxs-lookup"><span data-stu-id="63f14-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="63f14-117">ดังนั้น การตั้งค่าคอนฟิกรายงาน ER เดียวกันนี้สามารถนำไปใช้ในการสร้างเอกสารอิเล็กทรอนิกส์ที่มีจำนวนคอลัมน์ที่สร้างขึ้นแบบไดนามิกที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="63f14-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="63f14-118">ตั้งค่าคอนฟิกปลายทาง ER เพื่อให้ผลลัพธ์เอาต์พุตของรูปแบบถูกนำไปยังปลายทางเฉพาะเจาะจง: ไฟล์ อีเมล หรือไฟล์เก็บถาวร (โฟลเดอร์ Microsoft SharePoint หรือที่จัดเก็บ Microsoft Azure)</span><span class="sxs-lookup"><span data-stu-id="63f14-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="63f14-119">ก่อนหน้านี้ เมื่อคุณเรียกใช้การตั้งค่าคอนฟิก ER กล่องข้อความจะปรากฏขึ้นซึ่งกำหนดให้ต้องมีการดำเนินการของผู้ใช้ในการบันทึกหรือเปิดแฟ้ม</span><span class="sxs-lookup"><span data-stu-id="63f14-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="63f14-120">ขณะนี้คุณสามารถตั้งค่าคอนฟิกล่วงหน้าให้กับปลายทางสำหรับการตั้งค่าคอนฟิกรูปแบบแต่ละรายการ และองค์ประกอบผลลัพธ์แต่ละรายการ (โฟลเดอร์หรือไฟล์) โดยแยกจากกันได้</span><span class="sxs-lookup"><span data-stu-id="63f14-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="63f14-121">ผู้ใช้ที่มีสิทธิการเข้าถึงที่เหมาะสมยังสามารถปรับเปลี่ยนการตั้งค่าปลายทางในขณะดำเนินการได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="63f14-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="63f14-122">POS – Microsoft Dynamics AX Retail</span><span class="sxs-lookup"><span data-stu-id="63f14-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="63f14-123">คุณสามารถทำอะไร</span><span class="sxs-lookup"><span data-stu-id="63f14-123">What can you do?</span></span> | <span data-ttu-id="63f14-124">ทำไมนี่เป็นสิ่งสำคัญ</span><span class="sxs-lookup"><span data-stu-id="63f14-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="63f14-125">ใช้เบราว์เซอร์ Google Chrome</span><span class="sxs-lookup"><span data-stu-id="63f14-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="63f14-126">ขณะนี้ ผู้ขายปลีกสามารถเริ่มต้น Cloud POS ได้จากเบราเซอร์ Chrome และสามารถได้รับประสบการณ์ฟังก์ชันทั้งหมดที่พร้อมใช้งานในรุ่น Microsoft Edge และ Internet Explorer ของ Cloud POS</span><span class="sxs-lookup"><span data-stu-id="63f14-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="63f14-127">การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="63f14-127">Financial reporting</span></span>

| <span data-ttu-id="63f14-128">คุณสามารถทำอะไร</span><span class="sxs-lookup"><span data-stu-id="63f14-128">What can you do?</span></span> | <span data-ttu-id="63f14-129">ทำไมนี่เป็นสิ่งสำคัญ</span><span class="sxs-lookup"><span data-stu-id="63f14-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="63f14-130">สร้าง Data Mart การรายงานทางการเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="63f14-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="63f14-131">เมื่อคุณย้ายฐานข้อมูล Dynamics AX ระหว่างสภาพแวดล้อม หรือทำการเปลี่ยนแปลงเชิงรุกไปยังสภาพแวดล้อม ฐานข้อมูลการรายงานทางการเงินอาจต้องถูกสร้างอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="63f14-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="63f14-132">ขณะนี้มีสคริปต์ของ Windows PowerShell ให้กับคุณสำหรับการสร้างฐานข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="63f14-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="63f14-133">คุณไม่สามารถเลือกตัวเลือกผู้ออกแบบรายงานที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="63f14-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="63f14-134">ตัวเลือกตัวออกแบบรายงานหลายรายการที่ถูกใช้ในรุ่นในตลาดของ Management reporter ไม่นำไปใช้กับรุ่นนี้ของ Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="63f14-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="63f14-135">ตัวเลือกเหล่านี้เกี่ยวข้องกับการออกแบบรายงานทางการเงิน ผลผลิต และการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="63f14-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="63f14-136">ตัวเลือกเหล่านี้ได้ถูกลบออกจากผู้ออกแบบรายงานทางการเงินเพื่อป้องกันข้อผิดพลาดของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="63f14-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="63f14-137">การจัดทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="63f14-137">Financial management</span></span>

| <span data-ttu-id="63f14-138">คุณสามารถทำอะไร</span><span class="sxs-lookup"><span data-stu-id="63f14-138">What can you do?</span></span> | <span data-ttu-id="63f14-139">ทำไมนี่เป็นสิ่งสำคัญ</span><span class="sxs-lookup"><span data-stu-id="63f14-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="63f14-140">สร้างไฟล์ Positive Pay สำหรับการชำระเงินบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="63f14-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="63f14-141">คุณสามารถสร้างไฟล์ Positive Pay เพื่อช่วยป้องกันการฉ้อโกงเช็ค</span><span class="sxs-lookup"><span data-stu-id="63f14-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="63f14-142">คลังสินค้าและการผลิต</span><span class="sxs-lookup"><span data-stu-id="63f14-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="63f14-143">คุณสามารถทำอะไร</span><span class="sxs-lookup"><span data-stu-id="63f14-143">What can you do?</span></span></th>
<th><span data-ttu-id="63f14-144">ทำไมนี่เป็นสิ่งสำคัญ</span><span class="sxs-lookup"><span data-stu-id="63f14-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="63f14-145">กำหนดนโยบายงานคลังสินค้าที่ควบคุมการสร้างงานสำหรับชุดของผลิตภัณฑ์ที่ตำแหน่งเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="63f14-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="63f14-146">กระบวนการคลังสินค้าไม่รวมงานเสมอไป</span><span class="sxs-lookup"><span data-stu-id="63f14-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="63f14-147">โดยการใช้นโยบายงานคลังสินค้าใหม่ คุณสามารถป้องกันการสร้างงานสำหรับการเบิกวัตถุดิบและการสำรองสินค้าสำเร็จรูป สำหรับชุดของผลิตภัณฑ์ที่ตำแหน่งเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="63f14-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="63f14-148">ระบุว่าสถานที่ของเอาท์พุทการผลิตไม่มีการควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="63f14-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="63f14-149">ขณะนี้คุณสามารถระบุได้แล้วว่าสถานที่ของเอาท์พุทการผลิตไม่มีการควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="63f14-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="63f14-150">ตัวอย่างเช่น คุณลักษณะนี้มีประโยชน์เมื่อใบสั่งผลิตขั้นต้นน้ำรายงานสินค้าเมื่อเสร็จสมบูรณ์โดยตรงไปยังตำแหน่งที่ทำหน้าที่เป็นสถานที่ของเอาท์พุทการผลิตสำหรับใบสั่งผลิตขั้นปลายน้ำ</span><span class="sxs-lookup"><span data-stu-id="63f14-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="63f14-151">รองรับ BOM ที่รวมสินค้าที่มีมิติของผลิตภัณฑ์ที่แตกต่างกันของสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="63f14-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="63f14-152">เมื่อใช้มิติของผลิตภัณฑ์หนึ่งหรือหลายรายการในการผลิต คุณอาจพบสถานการณ์ที่คุณต้องการผลิตสินค้าตามตัวแปรต่างๆ ของสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="63f14-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="63f14-153">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">บล็อกนี้</a></span><span class="sxs-lookup"><span data-stu-id="63f14-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="63f14-154">ใบสั่งผลิตที่มีโครงสร้างการหมุนเวียนในระดับแรกของ BOM จะถูกแยกออกจากการคำนวณระดับ BOM สำหรับการวางแผนด้านทรัพยากรวัสดุ</span><span class="sxs-lookup"><span data-stu-id="63f14-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="63f14-155">คุณไม่สามารถกำหนดระดับ BOM ที่ถูกต้องให้กับตัวแปรผลิตภัณฑ์สำหรับใบสั่งการผลิตที่ทำให้เกิดการหมุนเวียนในลำดับชั้น BOM ได้</span><span class="sxs-lookup"><span data-stu-id="63f14-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="63f14-156">คำนวณระดับ BOM ที่แยกต่างหากสำหรับการวางแผนด้านทรัพยากรวัสดุ และการคำนวณต้นทุน:</span><span class="sxs-lookup"><span data-stu-id="63f14-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="63f14-157">สำหรับการวางแผนด้านทรัพยากรวัสดุ ระดับ BOM จะถูกคำนวณในตาราง <strong>ReqItemLevel</strong> ใหม่</span><span class="sxs-lookup"><span data-stu-id="63f14-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="63f14-158">ใบสั่งผลิตที่สิ้นสุดแล้วจะไม่นำมารวมในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="63f14-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="63f14-159">สำหรับการคำนวณต้นทุนการผลิต ระดับ BOM จะถูกคำนวณใน <strong>InventTable</strong></span><span class="sxs-lookup"><span data-stu-id="63f14-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="63f14-160">ใบสั่งผลิตที่สิ้นสุดแล้วจะรวมในการคำนวณด้วย</span><span class="sxs-lookup"><span data-stu-id="63f14-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="63f14-161">เมื่อเรียกใช้การวางแผนด้านทรัพยากรวัสดุ ตัวอย่างเช่น การวางแผนหลัก การกำหนดเวลาและการกระจายแผน เฉพาะระดับ BOM ที่ใช้สำหรับการวางแผนด้านทรัพยากรวัสดุที่จำเป็นต้องได้รับการคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="63f14-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="63f14-162">กล่าวอีกอย่างคือ ไม่จำเป็นต้องคำนวณระดับ BOM ที่ใช้สำหรับการคำนวณการคิดต้นทุนการผลิต</span><span class="sxs-lookup"><span data-stu-id="63f14-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="63f14-163">เมื่อรันการดำเนินการคิดต้นทุน ตัวอย่างเช่น การปิดบัญชีสินค้าคงคลัง เฉพาะระดับ BOM ที่ใช้สำหรับการคำนวณการคิดต้นทุนการผลิตที่จำเป็นต้องถูกคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="63f14-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="63f14-164">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="63f14-164">Additional resources</span></span>

[<span data-ttu-id="63f14-165">มีอะไรใหม่หรือมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="63f14-165">What's new or changed</span></span>](whats-new-changed.md)

[<span data-ttu-id="63f14-166">คู่มืองานใหม่หรือที่ปรับปรุงแล้ว (พฤษภาคม 2016)</span><span class="sxs-lookup"><span data-stu-id="63f14-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
