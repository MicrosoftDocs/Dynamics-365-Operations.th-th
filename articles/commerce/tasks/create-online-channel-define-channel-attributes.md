---
title: สร้างช่องทางออนไลน์และกำหนดลักษณะช่องทาง
description: 'ขั้นตอนนี้จะนำคุณไปสู่การสร้างช่องทางออนไลน์ใหม่และการเพิ่มมันไปยังลำดับชั้นขององค์กร '
author: jashanno
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e28e717dcf594c5079b4b6987331115356b6bdbc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798524"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="a1536-103">สร้างช่องทางออนไลน์และกำหนดลักษณะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="a1536-103">Create online channel and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1536-104">ขั้นตอนนี้จะนำคุณไปสู่การสร้างช่องทางออนไลน์ใหม่และการเพิ่มมันไปยังลำดับชั้นขององค์กร </span><span class="sxs-lookup"><span data-stu-id="a1536-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="a1536-105">คุณจะต้องสร้างลำดับชั้นขององค์กรก่อนที่คุณจะสร้างช่องทางออนไลน์ใหม่ได้ </span><span class="sxs-lookup"><span data-stu-id="a1536-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="a1536-106">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="a1536-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="a1536-107">สร้างช่องทางออนไลน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="a1536-107">Create a new online channel</span></span>
1. <span data-ttu-id="a1536-108">ไปยัง การขายปลีกและการค้า > ช่องทาง > ร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="a1536-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="a1536-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a1536-109">Click New.</span></span>
3. <span data-ttu-id="a1536-110">ในฟิลด์ชื่อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a1536-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a1536-111">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a1536-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="a1536-112">ในฟิลด์เขตเวลาของร้านค้า ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="a1536-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="a1536-113">ในฟิลด์ลูกค้าเริ่มต้น ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a1536-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="a1536-114">ในฟิลด์สมุดที่อยู่ลูกค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a1536-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="a1536-115">ในฟิลด์เงื่อนไขการชำระเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a1536-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="a1536-116">ในฟิลด์วิธีการชำระเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a1536-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="a1536-117">ในฟิลด์โพรไฟล์การแจ้งเตือนทางอีเมล์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a1536-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="a1536-118">ขยายส่วนของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="a1536-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="a1536-119">ในฟิลด์หน่วยทางธุรกิจ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a1536-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="a1536-120">ตั้งค่าสำหรับมิติเริ่มต้นอื่นๆ ทั้งหมดในลักษณะคล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="a1536-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="a1536-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="a1536-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="a1536-122">เพิ่มช่องทางออนไลน์ไปยังลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="a1536-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="a1536-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a1536-123">Close the page.</span></span>
2. <span data-ttu-id="a1536-124">ไปที่การจัดการองค์กร > องค์กร > ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="a1536-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="a1536-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a1536-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a1536-126">คลิกที่มุมมอง</span><span class="sxs-lookup"><span data-stu-id="a1536-126">Click View.</span></span>
5. <span data-ttu-id="a1536-127">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="a1536-127">Click Edit.</span></span>
    * <span data-ttu-id="a1536-128">คุณสามารถเลือกโหนดลำดับชั้นใดๆ ที่คุณต้องการแทรกช่องสัญญาณใหม่</span><span class="sxs-lookup"><span data-stu-id="a1536-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="a1536-129">คลิก แทรก</span><span class="sxs-lookup"><span data-stu-id="a1536-129">Click Insert.</span></span>
7. <span data-ttu-id="a1536-130">เลือกช่องทางการค้า</span><span class="sxs-lookup"><span data-stu-id="a1536-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="a1536-131">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="a1536-131">Click OK.</span></span>
9. <span data-ttu-id="a1536-132">คลิกที่เผยแพร่เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="a1536-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="a1536-133">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="a1536-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="a1536-134">คลิกที่เผยแพร่ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a1536-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="a1536-135">กำหนดค่าใบสั่งสำหรับการแจ้งเตือนแบบใกล้เคียงเวลาจริง</span><span class="sxs-lookup"><span data-stu-id="a1536-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="a1536-136">ไปยัง การขายปลีกและการค้า > การตั้งสำนักงานใหญ่ > พารามิเตอร์ > พารามิเตอร์การค้า</span><span class="sxs-lookup"><span data-stu-id="a1536-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="a1536-137">ตั้งค่าใช้บริการแบบเรียลไทม์สำหรับการสร้างใบสั่ง eCommerce เป็น "ใช่"</span><span class="sxs-lookup"><span data-stu-id="a1536-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="a1536-138">รันกำหนดการการกระจาย 1070 เพื่อซิงค์การเปลี่ยนแปลงไปยังฐานข้อมูลช่องทาง</span><span class="sxs-lookup"><span data-stu-id="a1536-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]