---
title: สร้างช่องทางศูนย์บริการและกำหนดลักษณะช่องทาง
description: กระบวนงานนี้นำไปสู่การสร้างช่องทางการขายปลีกใหม่และการกำหนดลักษณะช่องทาง
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4b6db1bfdaf17cd857a0a08515f1e0413994bd6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024191"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="120e4-103">กำหนดช่องทางคอลเซ็นเตอร์และกำหนดแอททริบิวต์ช่องทาง</span><span class="sxs-lookup"><span data-stu-id="120e4-103">Create call center channels and define channel attributes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="120e4-104">กระบวนการนี้จะแนะนำถึงการสร้างช่องทางการค้าใหม่และกำหนดแอตทริบิวต์ของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="120e4-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="120e4-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างงานนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="120e4-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="120e4-106">กระบวนการนี้เจาะจงสำหรับบทบาทไอทีในเชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="120e4-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="120e4-107">สร้างร้านค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="120e4-107">Create new store</span></span>
1. <span data-ttu-id="120e4-108">ไปที่ พื้นที่ทำงานทั้งหมด > การปรับใช้ช่องทาง</span><span class="sxs-lookup"><span data-stu-id="120e4-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="120e4-109">คลิก ช่องทางใหม่</span><span class="sxs-lookup"><span data-stu-id="120e4-109">Click New channel.</span></span>
3. <span data-ttu-id="120e4-110">คลิก ร้านค้า</span><span class="sxs-lookup"><span data-stu-id="120e4-110">Click Store.</span></span>
4. <span data-ttu-id="120e4-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="120e4-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="120e4-112">ในฟิลด์หมายเลขร้านค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="120e4-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="120e4-113">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="120e4-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="120e4-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="120e4-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="120e4-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="120e4-116">ในฟิลด์เขตเวลาของร้านค้า ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="120e4-117">ในฟิลด์โพรไฟล์ช่องทาง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="120e4-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="120e4-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="120e4-119">ในฟิลด์ภาษา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="120e4-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="120e4-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="120e4-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="120e4-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="120e4-122">ในฟิลด์กลุ่มภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="120e4-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="120e4-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="120e4-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="120e4-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="120e4-125">ในฟิลด์สมุดที่อยู่ลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="120e4-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="120e4-126">เลือกสมุดที่อยู่ที่ใช้ในการเชื่อมโยงลูกค้าไปยังร้านค้านี้</span><span class="sxs-lookup"><span data-stu-id="120e4-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="120e4-127">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="120e4-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="120e4-128">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="120e4-129">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="120e4-129">Click Select.</span></span>
22. <span data-ttu-id="120e4-130">ในฟิลด์สมุดที่อยู่พนักงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="120e4-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="120e4-131">เลือกสมุดที่อยู่ที่ใช้ในการเชื่อมโยงพนักงานเก็บเงินไปยังช่องทางนี้</span><span class="sxs-lookup"><span data-stu-id="120e4-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="120e4-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="120e4-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="120e4-133">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="120e4-134">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="120e4-134">Click Select.</span></span>
26. <span data-ttu-id="120e4-135">ในฟิลด์ลูกค้าเริ่มต้น ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="120e4-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="120e4-136">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="120e4-137">ขยายหรือยุบส่วนโครงร่างหน้าจอ </span><span class="sxs-lookup"><span data-stu-id="120e4-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="120e4-138">ในฟิลด์รหัสโครงร่างหน้าจอ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="120e4-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="120e4-139">เลือกโครงร่างหน้าจอ POS เริ่มต้นสำหรับร้านค้านี้</span><span class="sxs-lookup"><span data-stu-id="120e4-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="120e4-140">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="120e4-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="120e4-141">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="120e4-142">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="120e4-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="120e4-143">คลิก แอตทริบิวต์ช่องทาง</span><span class="sxs-lookup"><span data-stu-id="120e4-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="120e4-144">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="120e4-144">Click New.</span></span>
35. <span data-ttu-id="120e4-145">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="120e4-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="120e4-146">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="120e4-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="120e4-147">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="120e4-148">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="120e4-148">Click Save.</span></span>
39. <span data-ttu-id="120e4-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="120e4-149">Close the page.</span></span>
40. <span data-ttu-id="120e4-150">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="120e4-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="120e4-151">คลิกวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="120e4-151">Click Payment methods.</span></span>
42. <span data-ttu-id="120e4-152">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="120e4-152">Click New.</span></span>
43. <span data-ttu-id="120e4-153">ในฟิลด์วิธีการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="120e4-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="120e4-154">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="120e4-155">ขยายหรือยุบส่วนการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="120e4-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="120e4-156">ในฟิลด์หมายเลขบัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="120e4-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="120e4-157">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="120e4-157">Click Save.</span></span>
48. <span data-ttu-id="120e4-158">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="120e4-158">Close the page.</span></span>
49. <span data-ttu-id="120e4-159">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="120e4-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="120e4-160">คลิก การตรวจนับเงินสด</span><span class="sxs-lookup"><span data-stu-id="120e4-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="120e4-161">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="120e4-161">Click New.</span></span>
52. <span data-ttu-id="120e4-162">ในฟิลด์ยอดเงินในสกุลเงินธุรกรรม ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="120e4-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="120e4-163">ในฟิลด์สกุลเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="120e4-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="120e4-164">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="120e4-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="120e4-165">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="120e4-166">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="120e4-166">Click Save.</span></span>
57. <span data-ttu-id="120e4-167">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="120e4-167">Close the page.</span></span>
58. <span data-ttu-id="120e4-168">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="120e4-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="120e4-169">คลิก การกำหนดกลุ่มรหัสที่ตั้งร้านค้า</span><span class="sxs-lookup"><span data-stu-id="120e4-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="120e4-170">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="120e4-170">Click New.</span></span>
61. <span data-ttu-id="120e4-171">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="120e4-172">ในฟิลด์กลุ่มรหัสที่ตั้ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="120e4-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="120e4-173">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="120e4-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="120e4-174">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="120e4-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="120e4-175">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="120e4-175">Click Save.</span></span>
66. <span data-ttu-id="120e4-176">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="120e4-176">Close the page.</span></span>

