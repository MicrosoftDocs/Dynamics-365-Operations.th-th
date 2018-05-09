--- 
title: " สร้างและรันรายงานนอกกล่อง"
description: "ใช้คำแนะนำของงานนี้เพื่อรันรายงานนอกกล่องในศูนย์ควบคุมจากพื้นที่ทำงานต่างๆและการสอบถาม & รายงานการขายภายใต้การขายปลีก & การค้า"
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1bdd6835c89ab1095cafd4b235744d4a333d5fb5
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="4340a-103"> สร้างและรันรายงานนอกกล่อง</span><span class="sxs-lookup"><span data-stu-id="4340a-103">Generate and run out-of-box reports</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4340a-104">ใช้คำแนะนำของงานนี้เพื่อรันรายงานนอกกล่องในศูนย์ควบคุมจากพื้นที่ทำงานต่างๆและการสอบถาม & รายงานการขายภายใต้การขายปลีก & การค้า</span><span class="sxs-lookup"><span data-stu-id="4340a-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="4340a-105">การค้า ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างการบันทึกนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="4340a-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="4340a-106">บันทึกนี้มีไว้สำหรับผู้มีบทบาทผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="4340a-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="4340a-107">เปิดใช้รายงานจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="4340a-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="4340a-108">ไปที่ การขายปลีกและการค้า > ผลิตภัณฑ์และประเภท > การจัดการประเภทและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4340a-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="4340a-109">คลิกลูกศรเพื่อขยายหรือยุบส่วนรายงาน </span><span class="sxs-lookup"><span data-stu-id="4340a-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="4340a-110">คลิกรายงานผลิตภัณฑ์อันดับแรกๆ</span><span class="sxs-lookup"><span data-stu-id="4340a-110">Click Top products report.</span></span>
4. <span data-ttu-id="4340a-111">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="4340a-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="4340a-112">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="4340a-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="4340a-113">ในฟิลด์ช่องทาง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4340a-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4340a-114">ในแผนภูมิ เลือก 'การขายปลีกContoso\การขายปลีกContoso USA\ภาคกลาง\Houston'</span><span class="sxs-lookup"><span data-stu-id="4340a-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="4340a-115">ฟิลด์นี้แสดงค่าเริ่มต้นของลำดับชั้นขององค์กรขายปลีกเพื่อวัตถุประสงค์ในการรายงานการขายปลีก </span><span class="sxs-lookup"><span data-stu-id="4340a-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="4340a-116">ไปที่การจัดการองค์กร  >องค์กร > ลำดับชั้นขององค์กรเพื่อวัตถุประสงค์ในการเลือกรายงานการขายปลีกภายใต้การกำหนดลำดับชั้น ตรวจสอบชื่อลำดับชั้นสำหรับที่คอลัมน์เริ่มต้นถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="4340a-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="4340a-117">คุณจะต้องประกาศส่วนหนึ่งของข้อมูลสาธิต(ที่ใช้เพื่อบันทึกงานนี้)ร้านค้าปลีกเรียงตามภูมิภาค เป็นค่าเริ่มต้นลำดับชั้นขององค์กรเพื่อในวัตถุประสงค์การรายงานการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="4340a-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="4340a-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4340a-118">Click OK.</span></span>
9. <span data-ttu-id="4340a-119">ในฟิลด์มุมมอง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="4340a-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="4340a-120">ในฟิลด์ตาม ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="4340a-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="4340a-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4340a-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="4340a-122">เปิดใช้รายงานจากการสอบถามและรายงานการขายที่อยู่ภายใต้การขายปลีก & การเชื่อมโยงแอพลิเคชันการค้า</span><span class="sxs-lookup"><span data-stu-id="4340a-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="4340a-123">ไปที่ การขายปลีกและการค้า > การสอบถามและรายงาน > รายงานการขาย > รายงานการขายตามประเภท</span><span class="sxs-lookup"><span data-stu-id="4340a-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="4340a-124">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="4340a-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="4340a-125">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="4340a-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="4340a-126">ในฟิลด์ช่องทาง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4340a-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4340a-127">ในแผนภูมิ เลือก 'การขายปลีกContoso\การขายปลีกContoso USA\ภาคตะวันตก\Seattle'</span><span class="sxs-lookup"><span data-stu-id="4340a-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="4340a-128">ฟิลด์นี้แสดงค่าเริ่มต้นของลำดับชั้นขององค์กรขายปลีกเพื่อวัตถุประสงค์ในการรายงานการขายปลีก </span><span class="sxs-lookup"><span data-stu-id="4340a-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="4340a-129">ไปที่การจัดการองค์กร  >องค์กร > ลำดับชั้นขององค์กรเพื่อวัตถุประสงค์ในการเลือกรายงานการขายปลีกภายใต้การกำหนดลำดับชั้น ตรวจสอบชื่อลำดับชั้นสำหรับที่คอลัมน์เริ่มต้นถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="4340a-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="4340a-130">คุณจะต้องประกาศส่วนหนึ่งของข้อมูลสาธิต(ที่ใช้เพื่อบันทึกงานนี้)ร้านค้าปลีกเรียงตามภูมิภาค เป็นค่าเริ่มต้นลำดับชั้นขององค์กรเพื่อในวัตถุประสงค์การรายงานการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="4340a-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="4340a-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4340a-131">Click OK.</span></span>
7. <span data-ttu-id="4340a-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4340a-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="4340a-133">ส่งออกรายงาน HQ</span><span class="sxs-lookup"><span data-stu-id="4340a-133">Export an HQ reports</span></span>
1. <span data-ttu-id="4340a-134">ไปที่ การขายปลีกและการค้า > การสอบถามและรายงาน > รายงานการขาย > รายงานยอดขายขององค์กร</span><span class="sxs-lookup"><span data-stu-id="4340a-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="4340a-135">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="4340a-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="4340a-136">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="4340a-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="4340a-137">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4340a-137">Click OK.</span></span>
5. <span data-ttu-id="4340a-138">คลิก ส่งออก</span><span class="sxs-lookup"><span data-stu-id="4340a-138">Click Export.</span></span>
6. <span data-ttu-id="4340a-139">คลิก PDF</span><span class="sxs-lookup"><span data-stu-id="4340a-139">Click PDF.</span></span>


