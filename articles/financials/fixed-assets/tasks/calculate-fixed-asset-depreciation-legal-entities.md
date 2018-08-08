--- 
title: "คำนวณค่าเสื่อมราคาสินทรัพย์ถาวรในนิติบุคคล"
description: "กระบวนงานนี้แสดงวิธีตั้งค่า และรันกระบวนการคิดค่าเสื่อมราคาสำหรับหลายนิติบุคคล"
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 4221acf200f41ca39803bcd56c1b05e0d87bd948
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="93749-103">คำนวณค่าเสื่อมราคาสินทรัพย์ถาวรในนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="93749-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93749-104">สามารถรันการคิดค่าเสื่อมราคาสินทรัพย์ถาวรในนิติบุคคลในขั้นตอนเดียวได้</span><span class="sxs-lookup"><span data-stu-id="93749-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="93749-105">กระบวนงานนี้แสดงวิธีตั้งค่า และรันกระบวนการสำหรับหลายนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="93749-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="93749-106">ซึ่งใช้บทบาทของนักบัญชี</span><span class="sxs-lookup"><span data-stu-id="93749-106">It uses the accountant role.</span></span>  

<span data-ttu-id="93749-107">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="93749-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="93749-108">ขั้นตอน (16) งานย่อย: ตั้งค่าสมุดรายวันการรันค่าเสื่อมราคาระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="93749-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="93749-109">ก่อนอื่น คุณต้องตั้งค่าสมุดรายวันที่จะใช้ในการคำนวณในการรันค่าเสื่อมราคาระหว่างบริษัทในนิติบุคคลแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="93749-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="93749-110">ไปที่สินทรัพย์ถาวร > การตั้งค่า > พารามิเตอร์สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="93749-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="93749-111">ขยายส่วนข้อเสนอสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="93749-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="93749-112">สร้างเรกคอร์ดที่มีชื่อสมุดรายวันที่จะถูกใช้สำหรับชั้นของการลงรายการบัญชีแต่ละชั้นในนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="93749-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="93749-113">ถ้าสมุดบัญชีไม่ลงรายการบัญชีในบัญชีแยกประเภททั่วไป จึงไม่มีชั้นของการลงรายการบัญชีควรถูกเลือกด้วยสมุดรายวันที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="93749-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="93749-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="93749-114">Click Add.</span></span> 
4. <span data-ttu-id="93749-115">ในฟิลด์ชั้นของการลงรายการบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93749-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="93749-116">ในฟิลด์ชื่อสมุดรายวัน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93749-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="93749-117">ทำซ้ำการตั้งค่าสมุดรายวันบนหน้าพารามิเตอร์สินทรัพย์ถาวร ในนิติบุคคลแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="93749-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="93749-118">งานย่อย: คำนวณค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="93749-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="93749-119">ใช้หน้า สร้างข้อเสนอค่าเสื่อมราคา เพื่อเริ่มต้นการรันค่าเสื่อมราคาของคุณระหว่างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="93749-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="93749-120">ไปที่สินทรัพย์ถาวร > รายการสมุดรายวัน > สร้างข้อเสนอค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="93749-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="93749-121">ในฟิลด์ชั้นของการลงรายการบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93749-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="93749-122">ชื่อสมุดรายวันจะเริ่มต้นจากพารามิเตอร์สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="93749-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="93749-123">ซึ่งสามารถถูกเปลี่ยนได้ที่นี่สำหรับนิติบุคคลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="93749-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="93749-124">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="93749-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="93749-125">เลือกนิติบุคคลที่จะถูกรวมในการรันค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="93749-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="93749-126">จะมีการแสดงเฉพาะนิติบุคคลกับสมุดรายวันที่ตั้งค่าสำหรับข้อเสนอสินทรัพย์ถาวร บนหน้าพารามิเตอร์สินทรัพย์ถาวรในรายการ</span><span class="sxs-lookup"><span data-stu-id="93749-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="93749-127">เมื่อเปิดใช้งาน ตัวเลือก ลงรายการบัญชีสมุดรายวัน จะลงรายการสมุดรายวันการคิดค่าเสื่อมราคาโดยอัตโนมัติ เมื่อถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="93749-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="93749-128">เมื่อไม่มีการเลือก สมุดรายวันจะถูกสร้างขึ้น แต่ไม่ได้ลงรายการบัญชี ดังนั้นคุณสามารถทบทวนรายละเอียดได้ก่อนลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="93749-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="93749-129">เลือก ใช่ ในฟิลด์ ลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="93749-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="93749-130">ฟิลด์กรองข้อมูลรวมสินทรัพย์ถาวร กลุ่ม และสมุดบัญชีทั้งหมด สำหรับนิติบุคคลที่ถูกเลือกสำหรับการรันค่าเสื่อมราคานี้</span><span class="sxs-lookup"><span data-stu-id="93749-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="93749-131">ตัวเลือกการประมวลผลชุดงานถูกเปิดใช้งานโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="93749-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="93749-132">เมื่อตัวเลือกนี้ถูกเปิดใช้งาน การสร้างสมุดรายวันค่าเสื่อมราคาและการลงรายการบัญชีจะทำงานในเบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="93749-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="93749-133">คลิกสร้างสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="93749-133">Click Create journal.</span></span> 
10. <span data-ttu-id="93749-134">คุณต้องดูสมุดรายวันค่าเสื่อมราคาที่สร้างขึ้นในนิติบุคคลที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="93749-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="93749-135">ไปที่สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="93749-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

