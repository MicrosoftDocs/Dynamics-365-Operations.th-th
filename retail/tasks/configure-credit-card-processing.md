--- 
title: " ตั้งค่าคอนฟิคการประมวลผลบัตรเครดิต"
description: "กระบวนการนี้นำไปสู่วิธีการดูรายการของผู้ให้บริการชำระเงินและวิธีการตั้งค่าคอนฟิกบัญชีการชำระเงินสำหรับบัญชีลูกหนี้ "
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8e7bfbf6b51aca9cf8a7f800ac7db22c0330d00
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="589fa-103"> ตั้งค่าคอนฟิคการประมวลผลบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="589fa-103">Configure credit card processing</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="589fa-104">กระบวนการนี้นำไปสู่วิธีการดูรายการของผู้ให้บริการชำระเงินและวิธีการตั้งค่าคอนฟิกบัญชีการชำระเงินสำหรับบัญชีลูกหนี้ </span><span class="sxs-lookup"><span data-stu-id="589fa-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="589fa-105">ขั้นตอนนี้ใช้บริษัท USRT ในข้อมูลสาธิต และมีไว้สำหรับผู้ดูแลระบบและผู้เชี่ยวชาญด้าน IT</span><span class="sxs-lookup"><span data-stu-id="589fa-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="589fa-106">ดูรายการผู้ให้บริการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="589fa-106">View a list of payment providers</span></span>
1. <span data-ttu-id="589fa-107">ไปยังบัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > บริการการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="589fa-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="589fa-108">คลิกดูผู้ให้บริการที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="589fa-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="589fa-109">ตั้งค่าคอนฟิกบัญชีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="589fa-109">Configure payment account</span></span>
1. <span data-ttu-id="589fa-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="589fa-110">Click New.</span></span>
2. <span data-ttu-id="589fa-111">ในฟิลด์บริการชำระเงิน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="589fa-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="589fa-112">ในฟิลด์ตัวเชื่อมต่อการชำระเงิน ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="589fa-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="589fa-113">สลับการขยายของส่วนบัญชีบริการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="589fa-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="589fa-114">ในฟิลด์สภาพแวดล้อม ให้พิมพ์ 'PROD'</span><span class="sxs-lookup"><span data-stu-id="589fa-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="589fa-115">คลิกชนิดบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="589fa-115">Click Credit card types.</span></span>
7. <span data-ttu-id="589fa-116">ในฟิลด์สมุดรายวันของการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="589fa-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="589fa-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="589fa-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="589fa-118">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="589fa-118">Click Add.</span></span>
10. <span data-ttu-id="589fa-119">ในฟิลด์สกุลเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="589fa-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="589fa-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="589fa-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="589fa-121">ในฟิลด์สมุดรายวันของการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="589fa-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="589fa-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="589fa-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="589fa-123">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="589fa-123">Click Add.</span></span>
15. <span data-ttu-id="589fa-124">ในฟิลด์สกุลเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="589fa-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="589fa-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="589fa-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="589fa-126">คุณสามารถทำขั้นตอนเหล่านี้ซ้ำกี่ครั้งก็ได้ตามจำนวนบัตรที่คุณมี</span><span class="sxs-lookup"><span data-stu-id="589fa-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="589fa-127">ในฟิลด์สมุดรายวันของการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="589fa-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="589fa-128">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="589fa-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="589fa-129">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="589fa-129">Click Add.</span></span>
20. <span data-ttu-id="589fa-130">ในฟิลด์สกุลเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="589fa-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="589fa-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="589fa-131">Click Save.</span></span>
22. <span data-ttu-id="589fa-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="589fa-132">Close the page.</span></span>
23. <span data-ttu-id="589fa-133">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="589fa-133">Click Validate.</span></span>
24. <span data-ttu-id="589fa-134">คลิกตัวประมวลผลเริ่มต้นสำหรับกล่องกาเครื่องหมายบัตรเครดิตใหม่</span><span class="sxs-lookup"><span data-stu-id="589fa-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="589fa-135">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="589fa-135">Click Save.</span></span>


