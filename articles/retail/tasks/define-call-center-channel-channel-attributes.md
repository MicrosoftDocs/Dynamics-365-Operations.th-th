--- 
title: "สร้างช่องทางศูนย์บริการและกำหนดลักษณะช่องทาง"
description: "กระบวนงานนี้นำไปสู่การสร้างช่องทางการขายปลีกใหม่และการกำหนดลักษณะช่องทาง"
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 7ef094535214ecf4c65f95c36a93455446d7e388
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="8cf58-103">สร้างช่องทางศูนย์บริการและกำหนดลักษณะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8cf58-103">Create call center channels and define channel attributes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8cf58-104">กระบวนงานนี้นำไปสู่การสร้างช่องทางการขายปลีกใหม่และการกำหนดลักษณะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8cf58-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="8cf58-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างงานนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="8cf58-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="8cf58-106">กระบวนงานนี้มีไว้สำหรับบทบาทของฝ่ายไอทีระบบขายปลีก</span><span class="sxs-lookup"><span data-stu-id="8cf58-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="8cf58-107">สร้างร้านค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="8cf58-107">Create new store</span></span>
1. <span data-ttu-id="8cf58-108">ไปที่ พื้นที่ทำงานทั้งหมด > การปรับใช้ช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8cf58-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="8cf58-109">คลิก ช่องทางใหม่</span><span class="sxs-lookup"><span data-stu-id="8cf58-109">Click New channel.</span></span>
3. <span data-ttu-id="8cf58-110">คลิก ร้านค้า</span><span class="sxs-lookup"><span data-stu-id="8cf58-110">Click Store.</span></span>
4. <span data-ttu-id="8cf58-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="8cf58-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8cf58-112">ในฟิลด์หมายเลขร้านค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8cf58-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="8cf58-113">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8cf58-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8cf58-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cf58-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="8cf58-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8cf58-116">ในฟิลด์เขตเวลาของร้านค้า ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="8cf58-117">ในฟิลด์โพรไฟล์ช่องทาง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8cf58-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8cf58-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="8cf58-119">ในฟิลด์ภาษา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8cf58-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="8cf58-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cf58-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="8cf58-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="8cf58-122">ในฟิลด์กลุ่มภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8cf58-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="8cf58-123">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cf58-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="8cf58-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="8cf58-125">ในฟิลด์สมุดที่อยู่ลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="8cf58-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8cf58-126">เลือกสมุดที่อยู่ที่ใช้ในการเชื่อมโยงลูกค้าไปยังร้านค้านี้</span><span class="sxs-lookup"><span data-stu-id="8cf58-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="8cf58-127">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cf58-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="8cf58-128">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="8cf58-129">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="8cf58-129">Click Select.</span></span>
22. <span data-ttu-id="8cf58-130">ในฟิลด์สมุดที่อยู่พนักงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="8cf58-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8cf58-131">เลือกสมุดที่อยู่ที่ใช้ในการเชื่อมโยงพนักงานเก็บเงินไปยังช่องทางนี้</span><span class="sxs-lookup"><span data-stu-id="8cf58-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="8cf58-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cf58-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="8cf58-133">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="8cf58-134">คลิกเลือก </span><span class="sxs-lookup"><span data-stu-id="8cf58-134">Click Select.</span></span>
26. <span data-ttu-id="8cf58-135">ในฟิลด์ลูกค้าเริ่มต้น ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8cf58-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="8cf58-136">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="8cf58-137">ขยายหรือยุบส่วนโครงร่างหน้าจอ </span><span class="sxs-lookup"><span data-stu-id="8cf58-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="8cf58-138">ในฟิลด์รหัสโครงร่างหน้าจอ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8cf58-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8cf58-139">เลือกโครงร่างหน้าจอ POS เริ่มต้นสำหรับร้านค้านี้</span><span class="sxs-lookup"><span data-stu-id="8cf58-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="8cf58-140">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cf58-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="8cf58-141">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="8cf58-142">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="8cf58-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="8cf58-143">คลิก แอตทริบิวต์ช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8cf58-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="8cf58-144">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8cf58-144">Click New.</span></span>
35. <span data-ttu-id="8cf58-145">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8cf58-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="8cf58-146">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cf58-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="8cf58-147">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="8cf58-148">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8cf58-148">Click Save.</span></span>
39. <span data-ttu-id="8cf58-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8cf58-149">Close the page.</span></span>
40. <span data-ttu-id="8cf58-150">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="8cf58-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="8cf58-151">คลิกวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="8cf58-151">Click Payment methods.</span></span>
42. <span data-ttu-id="8cf58-152">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8cf58-152">Click New.</span></span>
43. <span data-ttu-id="8cf58-153">ในฟิลด์วิธีการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8cf58-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="8cf58-154">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="8cf58-155">ขยายหรือยุบส่วนการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="8cf58-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="8cf58-156">ในฟิลด์หมายเลขบัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cf58-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="8cf58-157">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8cf58-157">Click Save.</span></span>
48. <span data-ttu-id="8cf58-158">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8cf58-158">Close the page.</span></span>
49. <span data-ttu-id="8cf58-159">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="8cf58-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="8cf58-160">คลิก การตรวจนับเงินสด</span><span class="sxs-lookup"><span data-stu-id="8cf58-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="8cf58-161">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8cf58-161">Click New.</span></span>
52. <span data-ttu-id="8cf58-162">ในฟิลด์ยอดเงินในสกุลเงินธุรกรรม ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="8cf58-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="8cf58-163">ในฟิลด์สกุลเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8cf58-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="8cf58-164">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cf58-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="8cf58-165">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="8cf58-166">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8cf58-166">Click Save.</span></span>
57. <span data-ttu-id="8cf58-167">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8cf58-167">Close the page.</span></span>
58. <span data-ttu-id="8cf58-168">ในบานหน้าต่างการดำเนินการ คลิกตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="8cf58-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="8cf58-169">คลิก การกำหนดกลุ่มรหัสที่ตั้งร้านค้า</span><span class="sxs-lookup"><span data-stu-id="8cf58-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="8cf58-170">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8cf58-170">Click New.</span></span>
61. <span data-ttu-id="8cf58-171">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="8cf58-172">ในฟิลด์กลุ่มรหัสที่ตั้ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8cf58-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="8cf58-173">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8cf58-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="8cf58-174">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8cf58-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="8cf58-175">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8cf58-175">Click Save.</span></span>
66. <span data-ttu-id="8cf58-176">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8cf58-176">Close the page.</span></span>


