---
title: " จัดประเภทกฏการกำหนดราคาเพื่อสร้างข้อตกลงทางการค้า"
description: 'กระบวนงานนี้แสดงวิธีการสร้างข้อตกลงทางการค้าราคาขายโดยใช้กฎการกำหนดราคาประเภท '
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d252982cf1e4fa2f06646d0909e6f82d16f4cfc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "355529"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="5c4ef-103"> จัดประเภทกฏการกำหนดราคาเพื่อสร้างข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="5c4ef-103">Category pricing rules to create trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5c4ef-104">กระบวนงานนี้แสดงวิธีการสร้างข้อตกลงทางการค้าราคาขายโดยใช้กฎการกำหนดราคาประเภท </span><span class="sxs-lookup"><span data-stu-id="5c4ef-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="5c4ef-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างงานนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="5c4ef-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="5c4ef-106">งานนี้มีไว้สำหรับบทบาทผู้จัดการฝ่ายจัดซื้อสินค้าขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5c4ef-106">This task is intended for the Retail merchandising manager role.</span></span>

1. <span data-ttu-id="5c4ef-107">คลิกการจัดการการกำหนดราคาและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="5c4ef-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="5c4ef-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="5c4ef-108">Click New.</span></span>
3. <span data-ttu-id="5c4ef-109">คลิกกฎราคาประเภท</span><span class="sxs-lookup"><span data-stu-id="5c4ef-109">Click Category price rule.</span></span>
4. <span data-ttu-id="5c4ef-110">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5c4ef-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="5c4ef-111">ในฟิลด์รหัสบัญชี ให้เลือกหนึ่่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="5c4ef-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="5c4ef-112">รหัสบัญชีชนิด "กลุ่ม" ได้ถูกใช้ในการตั้งค่าข้อตกลงทางการค้าราคาขายที่เฉพาะเจาะจงสำหรับช่องทาง โปรแกรมตอบแทนลูกค้าสมาชิก แค็ตตาล็อก และสังกัด</span><span class="sxs-lookup"><span data-stu-id="5c4ef-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="5c4ef-113">ในฟิลด์การเลือกบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="5c4ef-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="5c4ef-114">ในฟิลด์ประเภท ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5c4ef-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="5c4ef-115">ในฟิลด์จำนวน/เปอร์เซนต์ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="5c4ef-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="5c4ef-116">ในฟิลด์เวอร์ชันการปัดเศษ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5c4ef-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="5c4ef-117">คลิกการสร้างข้อตกลงทางการค้า</span><span class="sxs-lookup"><span data-stu-id="5c4ef-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="5c4ef-118">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="5c4ef-118">Click Next.</span></span>
12. <span data-ttu-id="5c4ef-119">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="5c4ef-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="5c4ef-120">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="5c4ef-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="5c4ef-121">เลือก ใช่ ในฟิลด์ ค้นหาถัดไป</span><span class="sxs-lookup"><span data-stu-id="5c4ef-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="5c4ef-122">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="5c4ef-122">Click Next.</span></span>
16. <span data-ttu-id="5c4ef-123">คลิก Finish</span><span class="sxs-lookup"><span data-stu-id="5c4ef-123">Click Finish.</span></span>
    * <span data-ttu-id="5c4ef-124">มีการสร้างสมุดรายวันข้อตกลงทางการค้า และเปิดขึ้นเพื่อการตรวจทาน</span><span class="sxs-lookup"><span data-stu-id="5c4ef-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="5c4ef-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5c4ef-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5c4ef-126">บัญชีสมุดรายวันข้อตกลงทางการค้าที่ได้สร้างจากประเภทกฎการกำหนดราคาไม่ได้มีการลงรายการ </span><span class="sxs-lookup"><span data-stu-id="5c4ef-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="5c4ef-127">คุณสามารถตรวจทานและแก้ไขราคาที่สร้างขึ้นก่อนที่จะมีการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c4ef-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="5c4ef-128">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="5c4ef-128">Click Edit.</span></span>
19. <span data-ttu-id="5c4ef-129">ในฟิลด์จำนวนในสกุลเงิน ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="5c4ef-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="5c4ef-130">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c4ef-130">Click Post.</span></span>
21. <span data-ttu-id="5c4ef-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="5c4ef-131">Click OK.</span></span>
22. <span data-ttu-id="5c4ef-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5c4ef-132">Close the page.</span></span>
23. <span data-ttu-id="5c4ef-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5c4ef-133">Close the page.</span></span>
24. <span data-ttu-id="5c4ef-134">คลิกแท็บกฎราคาประเภท</span><span class="sxs-lookup"><span data-stu-id="5c4ef-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="5c4ef-135">ประเภทกฎการกำหนดราคาของช่องทางเฉพาะจะแสดงในรายการนี้</span><span class="sxs-lookup"><span data-stu-id="5c4ef-135">Channel specific Category pricing rules will show in this list.</span></span>  

