--- 
title: "แม็ปส่วนประกอบของรูปแบบไปยังองค์ประกอบแบบจำลองข้อมูล"
description: "กระบวนงานต่อไปนี้แสดงวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถแม็ปองค์ประกอบแบบจำลองข้อมูลไปยังส่วนประกอบของการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ที่สร้างขึ้น ซึ่งจะกำหนดรูปแบบเอกสารอิเล็กทรอนิกส์สำหรับโดเมนธุรกิจการชำระเงิน"
author: NickSelin
manager: AnnBe
ms.date: 02/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: e065cfbfc645bb7ac48134fe43d87bec013e8c81
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="map-the-components-of-formats-to-data-model-elements"></a><span data-ttu-id="62a07-103">แม็ปส่วนประกอบของรูปแบบไปยังองค์ประกอบแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="62a07-103">Map the components of formats to data model elements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62a07-104">กระบวนงานต่อไปนี้แสดงวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถแม็ปองค์ประกอบแบบจำลองข้อมูลไปยังส่วนประกอบของการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ที่สร้างขึ้น ซึ่งจะกำหนดรูปแบบเอกสารอิเล็กทรอนิกส์สำหรับโดเมนธุรกิจการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="62a07-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="62a07-105">รูปแบบนี้จะใช้ในภายหลังเพื่อสร้างเอกสารอิเล็กทรอนิกส์สำหรับการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="62a07-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="62a07-106">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกรูปแบบบริษัทตัวอย่าง ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="62a07-106">In this example, you will create a format configuration for the sample company, ‘Litware, Inc.’.</span></span> <span data-ttu-id="62a07-107">ขั้นตอนเหล่านี้สามารถทำได้ในบริษัทใดๆ เนื่องจากมีการใช้การตั้งค่าคอนฟิก ER ร่วมกันสำหรับบริษัททั้งหมด</span><span class="sxs-lookup"><span data-stu-id="62a07-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="62a07-108">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ คุณต้องทำขั้นตอนอย่างแรกให้เสร็จสมบูรณ์ในคู่มืองาน "สร้างการตั้งค่าคอนฟิกรูปแบบ"</span><span class="sxs-lookup"><span data-stu-id="62a07-108">To complete these steps, you must first complete the steps in the “Create a format configuration” task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="62a07-109">การเลือกการตั้งค่าคอนฟิกรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="62a07-109">Select a format configuration</span></span>
1. <span data-ttu-id="62a07-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="62a07-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="62a07-111">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="62a07-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="62a07-112">ในแผนภูมิ ขยาย 'การชำระเงิน (แบบจำลองอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="62a07-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="62a07-113">ในแผนภูมิ เลือก 'การชำระเงิน (แบบจำลองอย่างง่าย)\BACS (แบบสมมติ UK)'</span><span class="sxs-lookup"><span data-stu-id="62a07-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="62a07-114">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="62a07-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="62a07-115">แม็ปส่วนประกอบรูปแบบไปยังองค์ประกอบแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="62a07-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="62a07-116">คลิก ขยาย/ยุบ</span><span class="sxs-lookup"><span data-stu-id="62a07-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="62a07-117">คลิกแท็บ การแม็ป</span><span class="sxs-lookup"><span data-stu-id="62a07-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="62a07-118">ในแผนภูมิ ให้ขยาย 'model'</span><span class="sxs-lookup"><span data-stu-id="62a07-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="62a07-119">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\วันที่ประมวลผล\วันที่และเวลา'</span><span class="sxs-lookup"><span data-stu-id="62a07-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="62a07-120">ในแผนภูมิ ให้เลือก 'แบบจำลอง\วันที่และเวลาประมวลผล'</span><span class="sxs-lookup"><span data-stu-id="62a07-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="62a07-121">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-121">Click Bind.</span></span>
7. <span data-ttu-id="62a07-122">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\รหัสข้อความ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="62a07-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="62a07-123">ในแผนภูมิ ให้เลือก 'แบบจำลอง\รหัสข้อความ'</span><span class="sxs-lookup"><span data-stu-id="62a07-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="62a07-124">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-124">Click Bind.</span></span>
10. <span data-ttu-id="62a07-125">ในแผนภูมิ ขยาย 'model\Payments'</span><span class="sxs-lookup"><span data-stu-id="62a07-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="62a07-126">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\จำนวนเงิน\สตริง'</span><span class="sxs-lookup"><span data-stu-id="62a07-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="62a07-127">ในแผนภูมิ ให้เลือก 'แบบจำลอง\การชำระเงิน\ยอดเงินที่แนะนำ'</span><span class="sxs-lookup"><span data-stu-id="62a07-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="62a07-128">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-128">Click Bind.</span></span>
14. <span data-ttu-id="62a07-129">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\วันที่ทำธุรกรรม\วันที่และเวลา'</span><span class="sxs-lookup"><span data-stu-id="62a07-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="62a07-130">ในแผนภูมิ ให้เลือก 'แบบจำลอง\การชำระเงิน\วันที่ทำธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="62a07-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="62a07-131">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-131">Click Bind.</span></span>
17. <span data-ttu-id="62a07-132">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\คำอธิบาย\สตริง'</span><span class="sxs-lookup"><span data-stu-id="62a07-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="62a07-133">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="62a07-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="62a07-134">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-134">Click Bind.</span></span>
20. <span data-ttu-id="62a07-135">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\สกุลเงิน\สตริง'</span><span class="sxs-lookup"><span data-stu-id="62a07-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="62a07-136">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="62a07-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="62a07-137">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-137">Click Bind.</span></span>
23. <span data-ttu-id="62a07-138">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\รหัส'</span><span class="sxs-lookup"><span data-stu-id="62a07-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="62a07-139">ในแผนภูมิ ให้เลือก 'แบบจำลอง\การชำระเงิน\End2EndID'</span><span class="sxs-lookup"><span data-stu-id="62a07-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="62a07-140">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-140">Click Bind.</span></span>
26. <span data-ttu-id="62a07-141">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="62a07-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="62a07-142">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\บัญชี'</span><span class="sxs-lookup"><span data-stu-id="62a07-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="62a07-143">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\ตัวแทน'</span><span class="sxs-lookup"><span data-stu-id="62a07-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="62a07-144">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ชื่อ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="62a07-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="62a07-145">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระ\เจ้าหนี้\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="62a07-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="62a07-146">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-146">Click Bind.</span></span>
32. <span data-ttu-id="62a07-147">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\หมายเลขเส้นทาง\สตริง'</span><span class="sxs-lookup"><span data-stu-id="62a07-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="62a07-148">ในแผนภูมิ ให้เลือก 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\ตัวแทน\หมายเลขเส้นทาง(หมายเลขเส้นทาง)'</span><span class="sxs-lookup"><span data-stu-id="62a07-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="62a07-149">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-149">Click Bind.</span></span>
35. <span data-ttu-id="62a07-150">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้จัดจำหน่าย\ธนาคาร\หมายเลขบัญชี\สตริง'</span><span class="sxs-lookup"><span data-stu-id="62a07-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="62a07-151">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\เจ้าหนี้\บัญชี\หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="62a07-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="62a07-152">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-152">Click Bind.</span></span>
38. <span data-ttu-id="62a07-153">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ชื่อ\สตริง'</span><span class="sxs-lookup"><span data-stu-id="62a07-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="62a07-154">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\ลูกหนี้'</span><span class="sxs-lookup"><span data-stu-id="62a07-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="62a07-155">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\ลูกหนี้\บัญชี'</span><span class="sxs-lookup"><span data-stu-id="62a07-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="62a07-156">ในแผนภูมิ ขยาย 'แบบจำลอง\การชำระเงิน\ลูกหนี้\ตัวแทน'</span><span class="sxs-lookup"><span data-stu-id="62a07-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="62a07-157">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระ\ลูกหนี้\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="62a07-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="62a07-158">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-158">Click Bind.</span></span>
44. <span data-ttu-id="62a07-159">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ธนาคาร\หมายเลขเส้นทาง\สตริง'</span><span class="sxs-lookup"><span data-stu-id="62a07-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="62a07-160">ในแผนภูมิ ให้เลือก 'แบบจำลอง\การชำระเงิน\ลูกหนี้\ตัวแทน\หมายเลขเส้นทาง'</span><span class="sxs-lookup"><span data-stu-id="62a07-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="62a07-161">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-161">Click Bind.</span></span>
47. <span data-ttu-id="62a07-162">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ\ผู้ชำระ\ธนาคาร\หมายเลขบัญชี\สตริง'</span><span class="sxs-lookup"><span data-stu-id="62a07-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="62a07-163">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน\ลูกหนี้\บัญชี\หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="62a07-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="62a07-164">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-164">Click Bind.</span></span>
50. <span data-ttu-id="62a07-165">ในแผนภูมิ ให้เลือก 'Xml\ข้อความ\การชำระเงิน\รายการ'</span><span class="sxs-lookup"><span data-stu-id="62a07-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="62a07-166">ในแผนภูมิ เลือก 'แบบจำลอง\การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="62a07-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="62a07-167">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="62a07-167">Click Bind.</span></span>
53. <span data-ttu-id="62a07-168">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="62a07-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="62a07-169">ตรวจสอบความถูกต้องการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="62a07-169">Validate format mapping</span></span>
1. <span data-ttu-id="62a07-170">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="62a07-170">Click Validate.</span></span>
    * <span data-ttu-id="62a07-171">ตรวจสอบการแม็ปใหม่เพื่อให้แน่ใจว่าการเชื่อมโยงข้อมูลทั้งหมดถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="62a07-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="62a07-172">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="62a07-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="62a07-173">เปลี่ยนสถานะของรุ่นปัจจุบันของการตั้งค่าคอนฟิกรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="62a07-173">Change status of the current version of format configuration</span></span>
    * <span data-ttu-id="62a07-174">ในขั้นตอนถัดไป คุณจะเปลี่ยนสถานะของการตั้งค่าคอนฟิกรูปแบบจากแบบร่างเป็นเสร็จสมบูรณ์ เพื่อทำให้พร้อมใช้งานสำหรับการสร้างเอกสารการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="62a07-174">In the next steps, you’ll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="62a07-175">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="62a07-175">Click Change status.</span></span>
2. <span data-ttu-id="62a07-176">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="62a07-176">Click Complete.</span></span>
3. <span data-ttu-id="62a07-177">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="62a07-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="62a07-178">ตัวอย่างเช่น 'version 1'</span><span class="sxs-lookup"><span data-stu-id="62a07-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="62a07-179">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="62a07-179">Click OK.</span></span>
5. <span data-ttu-id="62a07-180">เลือกรุ่นที่สมบูรณ์ของการตั้งค่าคอนฟิกปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="62a07-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="62a07-181">โปรดทราบว่าการตั้งค่าคอนฟิกถูกบันทึกเป็นรุ่น 1.1 เสร็จสมบูรณ์ ซึ่งเป็นรุ่น 1 ของรูปแบบที่เป็นไปตามรุ่น 1 ของแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="62a07-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="62a07-182">กำหนดวันที่มีผลบังคับใช้สำหรับรุ่นที่เสร็จสมบูรณ์ของรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="62a07-182">Define effective date for completed version of format</span></span>
    * <span data-ttu-id="62a07-183">รุ่นของรูปแบบแต่ละรุ่นสามารถตั้งค่าคอนฟิกเป็นพร้อมใช้งานสำหรับการใช้งานเริ่มต้นจากวันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="62a07-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="62a07-184">เมื่อมีรุ่นของรูปแบบมากกว่าหนึ่งรุ่นที่ใช้งานในวันที่เฉพาะ รูปแบบล่าสุด (ตามหมายเลขรุ่น) จะถูกเลือกสำหรับการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="62a07-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="62a07-185">ค่าวันที่รอบเวลาจะใช้สำหรับการเลือกรุ่นที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="62a07-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="62a07-186">จำกัดการเข้าถึงรูปแบบที่สร้างขึ้นจากบริษัท</span><span class="sxs-lookup"><span data-stu-id="62a07-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="62a07-187">ขยายส่วนรหัสประเทศ/ภูมิภาค ISO</span><span class="sxs-lookup"><span data-stu-id="62a07-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="62a07-188">การเข้าถึงแต่ละรูปแบบสามารถถูกจำกัด โดยการระบุประเทศ/ภูมิภาคเฉพาะที่ซึ่งมีรูปแบบที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="62a07-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="62a07-189">เมื่อรายการของประเทศ/ภูมิภาคสำหรับรูปแบบเฉพาะว่างเปล่า รูปแบบนี้จะถูกใช้ในบริษัทใดๆ ก็ได้</span><span class="sxs-lookup"><span data-stu-id="62a07-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="62a07-190">เมื่อรหัส ISO ของประเทศ/ภูมิภาคถูกแทรกเข้าไปในรายการของประเทศ/ภูมิภาค รูปแบบดังกล่าวสามารถใช้ในบริษัทที่มีที่อยู่หลักในประเทศ/ภูมิภาคนั้นๆ เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="62a07-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  


