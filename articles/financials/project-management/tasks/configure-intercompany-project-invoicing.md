---
title: ตั้งค่าคอนฟิกการออกใบแจ้งหนี้โครงการระหว่างบริษัท
description: หัวข้อนี้แสดงวิธีการตั้งค่าการออกใบแจ้งหนี้โครงการระหว่างบริษัทสองแห่งในองค์กรของคุณ
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c89b17c09a4f145b5a4ca9cdd127b4e635447d4b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867330"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="b04e3-103">ตั้งค่าคอนฟิกการออกใบแจ้งหนี้โครงการระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="b04e3-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b04e3-104">หัวข้อนี้แสดงวิธีการตั้งค่าการออกใบแจ้งหนี้โครงการระหว่างบริษัทสองแห่งในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="b04e3-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="b04e3-105">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="b04e3-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b04e3-106">ในบานหน้าต่างการนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b04e3-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="b04e3-107">ในรายการ **ผู้จัดจำหน่ายทั้งหมด** ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b04e3-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="b04e3-108">ในบานหน้าต่างการดำเนินการ เลือก **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="b04e3-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="b04e3-109">เลือก **ระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="b04e3-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="b04e3-110">ตั้งค่า **ใช้งานอยู่** เป็น **ใช่** เพื่อเปิดใช้งานการค้าระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="b04e3-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="b04e3-111">ในฟิลด์ **บริษัทลูกค้า** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b04e3-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="b04e3-112">ในฟิลด์ **บัญชีของฉัน** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b04e3-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="b04e3-113">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b04e3-113">Select **Save**.</span></span>
9. <span data-ttu-id="b04e3-114">ปิดหน้าเพื่อกลับไปที่โฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="b04e3-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="b04e3-115">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการและการบัญชีโครงการ > การตั้งค่า > พารามิเตอร์การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="b04e3-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="b04e3-116">เลือกแท็บ **ระหว่างบริษัท**</span><span class="sxs-lookup"><span data-stu-id="b04e3-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="b04e3-117">เลื่อนแถบเลื่อนเป็น **ใช่** เพื่อเปิดใช้งานการจัดกำหนดการและแผ่นเวลาของทรัพยากรระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="b04e3-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="b04e3-118">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b04e3-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="b04e3-119">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="b04e3-119">Select **New**.</span></span>
15. <span data-ttu-id="b04e3-120">ในฟิลด์ **นิติบุคคลที่ขอยืม** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b04e3-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="b04e3-121">เลือกกล่องกาเครื่องหมาย **รายได้ค้างรับ**</span><span class="sxs-lookup"><span data-stu-id="b04e3-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="b04e3-122">ในฟิลด์ **ประเภทแผ่นเวลาเริ่มต้น** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b04e3-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="b04e3-123">ในฟิลด์ **ประเภทค่าใช้จ่ายเริ่มต้น** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b04e3-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="b04e3-124">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b04e3-124">Select **Save**.</span></span>
20. <span data-ttu-id="b04e3-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b04e3-125">Close the page.</span></span>
21. <span data-ttu-id="b04e3-126">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > การลงรายการบัญชี > การตั้งค่าการลงรายการบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="b04e3-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="b04e3-127">ในฟิลด์ **ชนิดบัญชีแยกประเภท** ให้เลือกหนึ่่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="b04e3-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="b04e3-128">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="b04e3-128">Select **New**.</span></span>
24. <span data-ttu-id="b04e3-129">ในฟิลด์ **บัญชีหลัก** ของแถวใหม่ ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b04e3-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="b04e3-130">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b04e3-130">Select **Save**.</span></span>
26. <span data-ttu-id="b04e3-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b04e3-131">Close the page.</span></span>
27. <span data-ttu-id="b04e3-132">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > การตั้งค่า > ราคา > ราคาโอน**</span><span class="sxs-lookup"><span data-stu-id="b04e3-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="b04e3-133">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="b04e3-133">Select **New**.</span></span>
29. <span data-ttu-id="b04e3-134">ในฟิลด์ **วันที่มีผลบังคับใช้** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="b04e3-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="b04e3-135">ในฟิลด์ **นิติบุคคลที่ขอยืม** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b04e3-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="b04e3-136">ในฟิลด์ **แบบจำลองราคาโอน** ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="b04e3-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="b04e3-137">ในฟิลด์ **การกำหนดราคา** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b04e3-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="b04e3-138">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="b04e3-138">Select **Save**.</span></span>

