---
title: สร้างและรันรายงานนอกกล่อง
description: ใช้คำแนะนำของงานนี้เพื่อดำเนินการรายงานนอกกล่องในศูนย์ควบคุมจากพื้นที่ทำงานต่างๆและการสอบถาม & รายงานการขายภายใต้การขายปลีกในการค้า
author: ashishmsft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db75b09f1ae1f83a88a5e5eaef0c8c1b8eab5901
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804148"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="3c0a4-103">สร้างและรันรายงานนอกกล่อง</span><span class="sxs-lookup"><span data-stu-id="3c0a4-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c0a4-104">ใช้คำแนะนำของงานนี้เพื่อดำเนินการรายงานนอกกล่องในศูนย์ควบคุมจากพื้นที่ทำงานต่างๆและการสอบถาม & รายงานการขายภายใต้การขายปลีกในการค้า</span><span class="sxs-lookup"><span data-stu-id="3c0a4-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="3c0a4-105">การค้า ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างการบันทึกนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="3c0a4-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="3c0a4-106">บันทึกนี้มีไว้สำหรับผู้มีบทบาทผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="3c0a4-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="3c0a4-107">เปิดใช้รายงานจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="3c0a4-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="3c0a4-108">ไปที่ การขายปลีกและการค้า > ผลิตภัณฑ์และประเภท > การจัดการประเภทและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3c0a4-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="3c0a4-109">คลิกลูกศรเพื่อขยายหรือยุบส่วนรายงาน </span><span class="sxs-lookup"><span data-stu-id="3c0a4-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="3c0a4-110">คลิกรายงานผลิตภัณฑ์อันดับแรกๆ</span><span class="sxs-lookup"><span data-stu-id="3c0a4-110">Click Top products report.</span></span>
4. <span data-ttu-id="3c0a4-111">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3c0a4-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="3c0a4-112">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3c0a4-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="3c0a4-113">ในฟิลด์ช่องทาง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="3c0a4-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3c0a4-114">ในแผนภูมิ เลือก 'การขายปลีกContoso\การขายปลีกContoso USA\ภาคกลาง\Houston'</span><span class="sxs-lookup"><span data-stu-id="3c0a4-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="3c0a4-115">ฟิลด์นี้แสดงค่าเริ่มต้นของลำดับชั้นขององค์กรขายปลีกเพื่อวัตถุประสงค์ในการรายงานการค้า</span><span class="sxs-lookup"><span data-stu-id="3c0a4-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="3c0a4-116">ไปที่การจัดการองค์กร  > องค์กร > วัตถุประสงค์ในการลำดับชั้นขององค์กรและเลือกรายงานการค้าและภายใต้ลำดับชั้นที่กำหนด ตรวจสอบชื่อลำดับชั้นสำหรับคอลัมน์เริ่มต้นที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="3c0a4-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="3c0a4-117">คุณจะต้องประกาศส่วนหนึ่งของข้อมูลสาธิต (ที่ใช้เพื่อบันทึกงานนี้) ร้านค้าเรียงตามภูมิภาค เป็นค่าเริ่มต้นลำดับชั้นขององค์กรเพื่อในวัตถุประสงค์การรายงาน</span><span class="sxs-lookup"><span data-stu-id="3c0a4-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="3c0a4-118">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="3c0a4-118">Click OK.</span></span>
9. <span data-ttu-id="3c0a4-119">ในฟิลด์มุมมอง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3c0a4-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="3c0a4-120">ในฟิลด์ตาม ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3c0a4-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="3c0a4-121">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="3c0a4-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="3c0a4-122">เปิดใช้รายงานจากการสอบถามและรายงานการขาย</span><span class="sxs-lookup"><span data-stu-id="3c0a4-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="3c0a4-123">ไปที่ การขายปลีกและการค้า > การสอบถามและรายงาน > รายงานการขาย > รายงานการขายตามประเภท</span><span class="sxs-lookup"><span data-stu-id="3c0a4-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="3c0a4-124">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3c0a4-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="3c0a4-125">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3c0a4-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="3c0a4-126">ในฟิลด์ช่องทาง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="3c0a4-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3c0a4-127">ในแผนภูมิ เลือก 'การขายปลีกContoso\การขายปลีกContoso USA\ภาคตะวันตก\Seattle'</span><span class="sxs-lookup"><span data-stu-id="3c0a4-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="3c0a4-128">ฟิลด์นี้แสดงค่าเริ่มต้นของลำดับชั้นขององค์กรขายปลีกเพื่อวัตถุประสงค์ในการรายงานการค้า</span><span class="sxs-lookup"><span data-stu-id="3c0a4-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="3c0a4-129">ไปที่การจัดการองค์กร  > องค์กร > วัตถุประสงค์ในการลำดับชั้นขององค์กรและเลือกรายงานการค้าและภายใต้ลำดับชั้นที่กำหนด ตรวจสอบชื่อลำดับชั้นสำหรับคอลัมน์เริ่มต้นที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="3c0a4-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="3c0a4-130">คุณจะต้องประกาศส่วนหนึ่งของข้อมูลสาธิต (ที่ใช้เพื่อบันทึกงานนี้) ร้านค้าเรียงตามภูมิภาค เป็นค่าเริ่มต้นลำดับชั้นขององค์กรเพื่อในวัตถุประสงค์การรายงาน</span><span class="sxs-lookup"><span data-stu-id="3c0a4-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="3c0a4-131">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="3c0a4-131">Click OK.</span></span>
7. <span data-ttu-id="3c0a4-132">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="3c0a4-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="3c0a4-133">ส่งออกรายงาน HQ</span><span class="sxs-lookup"><span data-stu-id="3c0a4-133">Export an HQ reports</span></span>
1. <span data-ttu-id="3c0a4-134">ไปที่ การขายปลีกและการค้า > การสอบถามและรายงาน > รายงานการขาย > รายงานยอดขายขององค์กร</span><span class="sxs-lookup"><span data-stu-id="3c0a4-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="3c0a4-135">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3c0a4-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="3c0a4-136">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="3c0a4-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="3c0a4-137">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="3c0a4-137">Click OK.</span></span>
5. <span data-ttu-id="3c0a4-138">คลิก ส่งออก</span><span class="sxs-lookup"><span data-stu-id="3c0a4-138">Click Export.</span></span>
6. <span data-ttu-id="3c0a4-139">คลิก PDF</span><span class="sxs-lookup"><span data-stu-id="3c0a4-139">Click PDF.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]