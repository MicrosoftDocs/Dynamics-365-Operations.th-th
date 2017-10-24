--- 
title: "สร้างและรับสินทรัพย์จากบัญชีเจ้าหนี้"
description: "คู่มือของงานนี้จะนำไปสุ่การสร้างและการซื้อสินทรัพย์ของสินทรัพย์ถาวรด้วยกระบวนการซื้อ "
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: 9149378047fc22efbd401b7af86df07c1403e4f5
ms.openlocfilehash: cfe920b2ef493ab3ae36a9557001086ed99c3e4e
ms.contentlocale: th-th
ms.lasthandoff: 10/05/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="eccd9-103">สร้างและรับสินทรัพย์จากบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="eccd9-103">Create and acquire assets from accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eccd9-104">คู่มือของงานนี้จะนำไปสุ่การสร้างและการซื้อสินทรัพย์ของสินทรัพย์ถาวรด้วยกระบวนการซื้อ </span><span class="sxs-lookup"><span data-stu-id="eccd9-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span> <span data-ttu-id="eccd9-105">มีการใช้นักบัญชีและเสมียนบัญชีเจ้าหนี้และบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="eccd9-105">It uses the Accountant and Accounts payable clerks and the demo company USMF.</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="eccd9-106">ตั้งค่าพารามิเตอร์สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="eccd9-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="eccd9-107">ไปที่สินทรัพย์ถาวร > การตั้งค่า > พารามิเตอร์สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="eccd9-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="eccd9-108">ขยายหรือยุบส่วนใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="eccd9-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="eccd9-109">ตรวจสอบการอนุญาตให้มีการซื้อสินทรัพย์จากกล่องกาเครื่องหมายการซื้อ</span><span class="sxs-lookup"><span data-stu-id="eccd9-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="eccd9-110">ตรวจสอบสร้างสินทรัพย์ในระหว่างกล่องกาเครื่องหมายใบรับสินค้าหรือการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="eccd9-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="eccd9-111">สร้างใบแจ้งหนี้ของผู้จัดจำหน่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="eccd9-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="eccd9-112">ไปที่บัญชีเจ้าหนี้ > พื้นที่ทำงาน > รายการใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="eccd9-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="eccd9-113">คลิกใบแจ้งหนี้ของผู้จัดจำหน่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="eccd9-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="eccd9-114">ในฟิลด์บัญชีใบแจ้งหนี้ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="eccd9-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="eccd9-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="eccd9-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="eccd9-116">ในฟิลด์หมายเลข ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="eccd9-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="eccd9-117">ในฟิลด์วันที่ลงรายการบัญชี ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="eccd9-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="eccd9-118">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="eccd9-118">Click Add line.</span></span>
8. <span data-ttu-id="eccd9-119">ในฟิลด์หมายเลขสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="eccd9-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="eccd9-120">สินค้าที่ไม่มีการเก็บในคลังหรือประเภทการจัดซื้ออย่างใดอย่างหนึ่่ง สามารถใช้สำหรับการซื้อสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="eccd9-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="eccd9-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="eccd9-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="eccd9-122">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="eccd9-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="eccd9-123">รายการใบแจ้งหนี้หนึ่งรายการจะสร้างสินทรัพย์ถาวรแค่หนึ่งรายการโดยไม่คำนึงถึงปริมาณ </span><span class="sxs-lookup"><span data-stu-id="eccd9-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="eccd9-124">ค่าของฟิลด์ปริมาณใบแจ้งหนี้จะถูกโอนย้ายไปเป็นปริมาณสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="eccd9-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="eccd9-125">ในฟิลด์ ราคาต่อหน่วย ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="eccd9-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="eccd9-126">ขยายหรือยุบส่วนรายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="eccd9-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="eccd9-127">คลิกที่แท็บสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="eccd9-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="eccd9-128">เลือกกล่องกาเครื่องหมายสร้างสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="eccd9-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="eccd9-129">ในฟิลด์สินทรัพย์ถาวร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="eccd9-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="eccd9-130">ในรายการ ให้เลือกสินทรัพย์ถาวรที่จะใช้เมื่อมีการสร้างสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="eccd9-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="eccd9-131">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="eccd9-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="eccd9-132">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="eccd9-132">Click Post.</span></span>
    * <span data-ttu-id="eccd9-133">สินทรัพย์ถาวรจะถูกสร้างและซื้อเมื่อมีการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="eccd9-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  


