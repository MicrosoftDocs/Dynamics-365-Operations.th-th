---
title: สร้างช่องทางออนไลน์และกำหนดลักษณะช่องทาง
description: 'ขั้นตอนนี้จะนำคุณไปสู่การสร้างช่องทางออนไลน์ใหม่และการเพิ่มมันไปยังลำดับชั้นขององค์กร '
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569532"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="7b36e-103">สร้างช่องทางออนไลน์และกำหนดลักษณะช่องทาง</span><span class="sxs-lookup"><span data-stu-id="7b36e-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7b36e-104">ขั้นตอนนี้จะนำคุณไปสู่การสร้างช่องทางออนไลน์ใหม่และการเพิ่มมันไปยังลำดับชั้นขององค์กร </span><span class="sxs-lookup"><span data-stu-id="7b36e-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="7b36e-105">คุณจะต้องสร้างลำดับชั้นขององค์กรก่อนที่คุณจะสร้างช่องทางออนไลน์ใหม่ได้ </span><span class="sxs-lookup"><span data-stu-id="7b36e-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="7b36e-106">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="7b36e-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="7b36e-107">สร้างช่องทางออนไลน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="7b36e-107">Create a new online channel</span></span>
1. <span data-ttu-id="7b36e-108">ไปที่ การขายปลีก และ การค้าขายสินค้า > ช่องทาง > ร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="7b36e-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="7b36e-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7b36e-109">Click New.</span></span>
3. <span data-ttu-id="7b36e-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="7b36e-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7b36e-111">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7b36e-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="7b36e-112">ในฟิลด์เขตเวลาของร้านค้า ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="7b36e-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="7b36e-113">ในฟิลด์ลูกค้าเริ่มต้น ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7b36e-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="7b36e-114">ในฟิลด์สมุดที่อยู่ลูกค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7b36e-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="7b36e-115">ในฟิลด์เงื่อนไขการชำระเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7b36e-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="7b36e-116">ในฟิลด์วิธีการชำระเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7b36e-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="7b36e-117">ในฟิลด์โพรไฟล์การแจ้งเตือนทางอีเมล์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7b36e-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="7b36e-118">ขยายส่วนของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="7b36e-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="7b36e-119">ในฟิลด์หน่วยทางธุรกิจ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7b36e-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="7b36e-120">ตั้งค่าสำหรับมิติเริ่มต้นอื่นๆ ทั้งหมดในลักษณะคล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="7b36e-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="7b36e-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7b36e-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="7b36e-122">เพิ่มช่องทางออนไลน์ไปยังลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7b36e-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="7b36e-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7b36e-123">Close the page.</span></span>
2. <span data-ttu-id="7b36e-124">ไปที่การจัดการองค์กร > องค์กร > ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7b36e-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="7b36e-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7b36e-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7b36e-126">คลิกที่มุมมอง</span><span class="sxs-lookup"><span data-stu-id="7b36e-126">Click View.</span></span>
5. <span data-ttu-id="7b36e-127">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="7b36e-127">Click Edit.</span></span>
    * <span data-ttu-id="7b36e-128">คุณสามารถเลือกโหนดลำดับชั้นใดๆ ที่คุณต้องการแทรกช่องสัญญาณใหม่</span><span class="sxs-lookup"><span data-stu-id="7b36e-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="7b36e-129">คลิก แทรก</span><span class="sxs-lookup"><span data-stu-id="7b36e-129">Click Insert.</span></span>
7. <span data-ttu-id="7b36e-130">คลิกที่ช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="7b36e-130">Click Retail channel.</span></span>
8. <span data-ttu-id="7b36e-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7b36e-131">Click OK.</span></span>
9. <span data-ttu-id="7b36e-132">คลิกที่เผยแพร่เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7b36e-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="7b36e-133">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="7b36e-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="7b36e-134">คลิกที่เผยแพร่ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7b36e-134">Click Publish.</span></span>

