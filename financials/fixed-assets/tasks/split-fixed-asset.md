--- 
title: "แบ่งสินทรัพย์ถาวร"
description: "คู่มืองานนี้จะแบ่งเป็นเปอร์เซ็นต์ของสมุดบัญชีสินทรัพย์เดียวกับสมุดบัญชีสินทรัพย์ใหม่ "
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
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
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="7822f-103">แบ่งสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="7822f-103">Split a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7822f-104">คู่มืองานนี้จะแบ่งเป็นเปอร์เซ็นต์ของสมุดบัญชีสินทรัพย์เดียวกับสมุดบัญชีสินทรัพย์ใหม่ </span><span class="sxs-lookup"><span data-stu-id="7822f-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="7822f-105">มีการเข้าถึงข้อมูลบทบาทของนักบัญชีและข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="7822f-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="7822f-106">สร้างสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="7822f-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="7822f-107">ไปที่ สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="7822f-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="7822f-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7822f-108">Click New.</span></span>
3. <span data-ttu-id="7822f-109">ในฟิลด์กลุ่มสินทรัพย์ถาวร ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7822f-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="7822f-110">หมายเหตุ หมายเลขสินทรัพย์ถาวรที่จะใช้ในกระบวนการแบ่งในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="7822f-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="7822f-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="7822f-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="7822f-112">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="7822f-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="7822f-113">แบ่งสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="7822f-113">Split a fixed asset</span></span>
1. <span data-ttu-id="7822f-114">ในรายการ ค้นหาและเลือกสินทรัพย์ถาวรที่จะแบ่ง</span><span class="sxs-lookup"><span data-stu-id="7822f-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="7822f-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7822f-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="7822f-116">คลิก สมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="7822f-116">Click Books.</span></span>
    * <span data-ttu-id="7822f-117">เลือกสมุดบัญชีเพื่อแบ่งไปยังสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="7822f-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="7822f-118">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="7822f-118">Click Functions.</span></span>
5. <span data-ttu-id="7822f-119">คลิกแบ่งสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="7822f-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="7822f-120">ในฟิลด์สินทรัพย์ถาวรสิ้นสุด ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7822f-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="7822f-121">ในฟิลด์ไปยังสมุดบัญชี ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="7822f-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="7822f-122">ในฟิลด์วันที่ทำธุรกรรม ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="7822f-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="7822f-123">ในฟิลด์เปอร์เซนต์ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="7822f-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="7822f-124">ในฟิลด์ชื่อสมุดรายวัน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="7822f-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="7822f-125">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7822f-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="7822f-126">ลงรายการบัญชีธุรกรรมสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7822f-126">Post the journal transaction</span></span>
1. <span data-ttu-id="7822f-127">ไปที่สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="7822f-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="7822f-128">ในรายการ ให้เลือกสมุดรายวันที่สร้างขึ้นด้วยกระบวนการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="7822f-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="7822f-129">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="7822f-129">Click Lines.</span></span>
    * <span data-ttu-id="7822f-130">ตรวจสอบการสร้างรายการสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="7822f-130">Verify the journal lines created.</span></span>  <span data-ttu-id="7822f-131">สร้างธุรกรรมการปรับปรุงการซื้อสินทรัพย์สำหรับสินทรัพย์เดิมเพื่อลดมูลค่าตามเปอร์เซ็นต์ที่ระบุไว้ในระหว่างกระบวนการแบ่ง </span><span class="sxs-lookup"><span data-stu-id="7822f-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="7822f-132">สร้างธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ใหม่สำหรับยอดเงินเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="7822f-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="7822f-133">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="7822f-133">Click Post.</span></span>


