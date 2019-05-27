---
title: ตั้งค่าคอนฟิกการออกใบแจ้งหนี้โครงการระหว่างบริษัท
description: กระบวนงานนี้แสดงวิธีการตั้งค่าการออกใบแจ้งหนี้โครงการระหว่างบริษัทสองแห่งในองค์กรของคุณ
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572430"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="09270-103">ตั้งค่าคอนฟิกการออกใบแจ้งหนี้โครงการระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="09270-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09270-104">กระบวนงานนี้แสดงวิธีการตั้งค่าการออกใบแจ้งหนี้โครงการระหว่างบริษัทสองแห่งในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="09270-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="09270-105">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="09270-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="09270-106">ไปที่บัญชีเจ้าหนี้ > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="09270-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="09270-107">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="09270-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="09270-108">ในบานหน้าต่างการดำเนินการ คลิกทั่วไป</span><span class="sxs-lookup"><span data-stu-id="09270-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="09270-109">คลิก ระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="09270-109">Click Intercompany.</span></span>
5. <span data-ttu-id="09270-110">ตั้งค่าการใช้งานเป็น ใช่ เพื่อเปิดใช้งานการค้าระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="09270-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="09270-111">ในฟิลด์บริษัทลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="09270-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="09270-112">ในฟิลด์บัญชีของฉัน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="09270-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="09270-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="09270-113">Click Save.</span></span>
9. <span data-ttu-id="09270-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="09270-114">Close the page.</span></span>
10. <span data-ttu-id="09270-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="09270-115">Close the page.</span></span>
11. <span data-ttu-id="09270-116">ไปที่ การจัดการและการบัญชีโครงการ > การตั้งค่า > พารามิเตอร์การจัดการและการบัญชีโครงการ</span><span class="sxs-lookup"><span data-stu-id="09270-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="09270-117">คลิกแท็บระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="09270-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="09270-118">เลื่อนแถบเลื่อนเป็น ใช่ เพื่อเปิดใช้งานการจัดกำหนดการและแผ่นเวลาสำหรับพนักงานระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="09270-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="09270-119">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="09270-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="09270-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="09270-120">Click New.</span></span>
16. <span data-ttu-id="09270-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="09270-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="09270-122">ในฟิลด์ นิติบุคคลที่ขอยืม ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="09270-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="09270-123">เลือกกล่องกาเครื่องหมายรายได้ค้างรับ</span><span class="sxs-lookup"><span data-stu-id="09270-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="09270-124">ในฟิลด์ประเภทแผ่นเวลาเริ่มต้น ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="09270-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="09270-125">ในฟิลด์ประเภทค่าใช้จ่ายเริ่มต้น ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="09270-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="09270-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="09270-126">Click Save.</span></span>
22. <span data-ttu-id="09270-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="09270-127">Close the page.</span></span>
23. <span data-ttu-id="09270-128">ไปที่ การจัดการและการบัญชีโครงการ > การตั้งค่า > การลงรายการบัญชี > การตั้งค่าการลงรายการบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="09270-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="09270-129">ในฟิลด์ชนิดบัญชีแยกประเภท ให้เลือกหนึ่่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="09270-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="09270-130">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="09270-130">Click New.</span></span>
26. <span data-ttu-id="09270-131">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="09270-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="09270-132">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="09270-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="09270-133">ในฟิลด์บัญชีหลัก ระบุมูลค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="09270-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="09270-134">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="09270-134">Click Save.</span></span>
30. <span data-ttu-id="09270-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="09270-135">Close the page.</span></span>
31. <span data-ttu-id="09270-136">ไปที่ การจัดการและการบัญชีโครงการ > การตั้งค่า > ราคา > ราคาโอน</span><span class="sxs-lookup"><span data-stu-id="09270-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="09270-137">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="09270-137">Click New.</span></span>
33. <span data-ttu-id="09270-138">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="09270-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="09270-139">ในฟิลด์ นิติบุคคลที่ขอยืม ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="09270-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="09270-140">ในฟิลด์แบบจำลองราคาโอน ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="09270-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="09270-141">ในฟิลด์การกำหนดราคา ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="09270-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="09270-142">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="09270-142">Click Save.</span></span>

