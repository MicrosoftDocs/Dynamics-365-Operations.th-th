---
title: กำหนดช่องทางคอลเซ็นเตอร์และกำหนดแอททริบิวต์ช่องทาง
description: กระบวนงานนี้นำไปสู่การสร้างช่องทางใหม่และการกำหนดแอททริบิวต์ช่องทาง
author: mugunthanm
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b053ea3a5792d016cfe4850f07c65de97fbfc9e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802706"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="be4f5-103">กำหนดช่องทางคอลเซ็นเตอร์และกำหนดแอททริบิวต์ช่องทาง</span><span class="sxs-lookup"><span data-stu-id="be4f5-103">Create call center channels and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be4f5-104">กระบวนการนี้จะแนะนำถึงการสร้างช่องทางการค้าใหม่และกำหนดแอตทริบิวต์ของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="be4f5-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="be4f5-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างงานนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="be4f5-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="be4f5-106">กระบวนการนี้เจาะจงสำหรับบทบาทไอทีในเชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="be4f5-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="be4f5-107">สร้างร้านค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="be4f5-107">Create new store</span></span>
1. <span data-ttu-id="be4f5-108">ไปที่ พื้นที่ทำงานทั้งหมด > การปรับใช้ช่องทาง</span><span class="sxs-lookup"><span data-stu-id="be4f5-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="be4f5-109">คลิก ช่องทางใหม่</span><span class="sxs-lookup"><span data-stu-id="be4f5-109">Click New channel.</span></span>
3. <span data-ttu-id="be4f5-110">คลิก ร้านค้า</span><span class="sxs-lookup"><span data-stu-id="be4f5-110">Click Store.</span></span>
4. <span data-ttu-id="be4f5-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="be4f5-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="be4f5-112">ในฟิลด์หมายเลขร้านค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="be4f5-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="be4f5-113">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be4f5-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="be4f5-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be4f5-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="be4f5-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="be4f5-116">ในฟิลด์เขตเวลาของร้านค้า ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="be4f5-117">ในฟิลด์โพรไฟล์ช่องทาง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be4f5-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="be4f5-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="be4f5-119">ในฟิลด์ภาษา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be4f5-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="be4f5-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be4f5-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="be4f5-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="be4f5-122">ในฟิลด์กลุ่มภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be4f5-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="be4f5-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be4f5-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="be4f5-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="be4f5-125">ในฟิลด์สมุดที่อยู่ลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="be4f5-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="be4f5-126">เลือกสมุดที่อยู่ที่ใช้ในการเชื่อมโยงลูกค้าไปยังร้านค้านี้</span><span class="sxs-lookup"><span data-stu-id="be4f5-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="be4f5-127">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be4f5-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="be4f5-128">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="be4f5-129">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="be4f5-129">Click Select.</span></span>
22. <span data-ttu-id="be4f5-130">ในฟิลด์สมุดที่อยู่พนักงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="be4f5-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="be4f5-131">เลือกสมุดที่อยู่ที่ใช้ในการเชื่อมโยงพนักงานเก็บเงินไปยังช่องทางนี้</span><span class="sxs-lookup"><span data-stu-id="be4f5-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="be4f5-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be4f5-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="be4f5-133">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="be4f5-134">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="be4f5-134">Click Select.</span></span>
26. <span data-ttu-id="be4f5-135">ในฟิลด์ลูกค้าเริ่มต้น ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be4f5-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="be4f5-136">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="be4f5-137">ขยายหรือยุบส่วนโครงร่างหน้าจอ </span><span class="sxs-lookup"><span data-stu-id="be4f5-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="be4f5-138">ในฟิลด์รหัสโครงร่างหน้าจอ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be4f5-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="be4f5-139">เลือกโครงร่างหน้าจอ POS เริ่มต้นสำหรับร้านค้านี้</span><span class="sxs-lookup"><span data-stu-id="be4f5-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="be4f5-140">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be4f5-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="be4f5-141">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="be4f5-142">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="be4f5-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="be4f5-143">คลิก แอตทริบิวต์ช่องทาง</span><span class="sxs-lookup"><span data-stu-id="be4f5-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="be4f5-144">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="be4f5-144">Click New.</span></span>
35. <span data-ttu-id="be4f5-145">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be4f5-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="be4f5-146">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be4f5-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="be4f5-147">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="be4f5-148">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="be4f5-148">Click Save.</span></span>
39. <span data-ttu-id="be4f5-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="be4f5-149">Close the page.</span></span>
40. <span data-ttu-id="be4f5-150">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="be4f5-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="be4f5-151">คลิกวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="be4f5-151">Click Payment methods.</span></span>
42. <span data-ttu-id="be4f5-152">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="be4f5-152">Click New.</span></span>
43. <span data-ttu-id="be4f5-153">ในฟิลด์วิธีการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be4f5-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="be4f5-154">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="be4f5-155">ขยายหรือยุบส่วนการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="be4f5-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="be4f5-156">ในฟิลด์หมายเลขบัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be4f5-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="be4f5-157">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="be4f5-157">Click Save.</span></span>
48. <span data-ttu-id="be4f5-158">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="be4f5-158">Close the page.</span></span>
49. <span data-ttu-id="be4f5-159">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="be4f5-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="be4f5-160">คลิก การตรวจนับเงินสด</span><span class="sxs-lookup"><span data-stu-id="be4f5-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="be4f5-161">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="be4f5-161">Click New.</span></span>
52. <span data-ttu-id="be4f5-162">ในฟิลด์ยอดเงินในสกุลเงินธุรกรรม ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="be4f5-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="be4f5-163">ในฟิลด์สกุลเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be4f5-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="be4f5-164">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be4f5-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="be4f5-165">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="be4f5-166">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="be4f5-166">Click Save.</span></span>
57. <span data-ttu-id="be4f5-167">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="be4f5-167">Close the page.</span></span>
58. <span data-ttu-id="be4f5-168">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="be4f5-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="be4f5-169">คลิก การกำหนดกลุ่มรหัสที่ตั้งร้านค้า</span><span class="sxs-lookup"><span data-stu-id="be4f5-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="be4f5-170">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="be4f5-170">Click New.</span></span>
61. <span data-ttu-id="be4f5-171">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="be4f5-172">ในฟิลด์กลุ่มรหัสที่ตั้ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="be4f5-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="be4f5-173">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="be4f5-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="be4f5-174">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be4f5-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="be4f5-175">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="be4f5-175">Click Save.</span></span>
66. <span data-ttu-id="be4f5-176">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="be4f5-176">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]