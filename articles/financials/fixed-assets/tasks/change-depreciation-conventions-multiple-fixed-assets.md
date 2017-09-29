--- 
title: "การเปลี่ยนแบบแผนการคิดค่าเสื่อมราคาสำหรับสินทรัพย์ถาวรหลายรายการ"
description: "งานนี้อัพเดตแบบแผนการคิดค่าเสื่อมราคาสำหรับกลุ่มสินทรัพย์ถาวรที่ระบุ "
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0f711d2e18a13ab972e548d3304652dee3f2e406
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="f7f42-103">การเปลี่ยนแบบแผนการคิดค่าเสื่อมราคาสำหรับสินทรัพย์ถาวรหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="f7f42-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7f42-104">งานนี้อัพเดตแบบแผนการคิดค่าเสื่อมราคาสำหรับกลุ่มสินทรัพย์ถาวรที่ระบุ </span><span class="sxs-lookup"><span data-stu-id="f7f42-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="f7f42-105">คู่มือของงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="f7f42-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="f7f42-106">ไปที่สินทรัพย์ถาวร > งานประจำงวด > การอัพเดตโดยรวม</span><span class="sxs-lookup"><span data-stu-id="f7f42-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="f7f42-107">ในฟิลด์สมุดบัญชีค่าเสื่อมราคา ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f7f42-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f7f42-108">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7f42-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f7f42-109">ในฟิลด์การเริ่มต้นการใช้งาน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f7f42-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="f7f42-110">ในฟิลด์การสิ้นสุดการใช้งาน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f7f42-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="f7f42-111">เฉพาะสินทรัพย์ที่เป็นส่วนหนึ่งของสมุดบัญชีค่าเสื่อมราคาที่คุณเลือกและที่ได้เสนอในบริการระหว่างวันที่ดังกล่าวจะถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="f7f42-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="f7f42-112">ในฟิลด์แบบแผนการคิดค่าเสื่อมราคาปัจจุบัน ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f7f42-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="f7f42-113">จะมีการอัพเดตเฉพาะสินทรัพย์ที่มีแบบแผนการคิดค่าเสื่อมราคาปัจจุบันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f7f42-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="f7f42-114">ในฟิลด์แบบแผนการคิดค่าเสื่อมราคาใหม่ ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f7f42-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="f7f42-115">ตรวจสอบรายงานที่จะพิมพ์ไปยังปลายทางที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f7f42-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="f7f42-116">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="f7f42-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="f7f42-117">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="f7f42-117">Click Filter.</span></span>
10. <span data-ttu-id="f7f42-118">ในรายการ ให้เลือกกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="f7f42-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="f7f42-119">ในฟิลด์เงื่อนไข ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="f7f42-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="f7f42-120">เลือกกลุ่มสินทรัพย์ถาวรที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f7f42-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="f7f42-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7f42-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f7f42-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7f42-122">Click OK.</span></span>
15. <span data-ttu-id="f7f42-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f7f42-123">Click OK.</span></span>
    *  <span data-ttu-id="f7f42-124">ผลลัพธ์ของกระบวนจะปรากฏบนรายงานการอัพเดตโดยรวม</span><span class="sxs-lookup"><span data-stu-id="f7f42-124">Results of the process are shown on the Mass update report.</span></span>     


