--- 
title: " สร้างใบสั่งศูนย์บริการ"
description: "ขั้นตอนนี้จะสอนให้ค้นหาลูกค้า สร้างใบสั่งใหม่ ค้นหาผลิตภัณฑ์และรวบรวมการชำระเงินจากลูกค้า "
author: josaw1
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
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f702690f72b3e299f6c2744da326a23d5753eb5d
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-call-center-orders"></a><span data-ttu-id="4ba23-103"> สร้างใบสั่งศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="4ba23-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4ba23-104">ขั้นตอนนี้จะสอนให้ค้นหาลูกค้า สร้างใบสั่งใหม่ ค้นหาผลิตภัณฑ์และรวบรวมการชำระเงินจากลูกค้า </span><span class="sxs-lookup"><span data-stu-id="4ba23-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="4ba23-105">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT และมีไว้สำหรับเจ้าหน้าที่ดูแลใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="4ba23-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="4ba23-106">ความต้องการเบื้องต้น:  ผู้ใช้ที่ดำเนินการขั้นตอนนี้จะต้องถูกตั้งค่าเป็นผู้ใช้ศูนย์บริการ และแค็ตตาล็อกประจำครึ่งปี Fabrikam จะถูกเผยแพร่พร้อมกับหนึ่งรหัสแหล่งที่เป็นอย่างต่ำ</span><span class="sxs-lookup"><span data-stu-id="4ba23-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="4ba23-107">ไปที่ การขายปลีกและการค้าขายสินค้า > ลูกค้า > บริการลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4ba23-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="4ba23-108">ในฟิลด์ คำที่ใช้ค้นหา ให้ป้อนเงื่อนไขการค้นหาเพื่อค้นหาลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4ba23-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="4ba23-109">สำหรับขั้นตอนตัวอย่างนี้ ให้พิมพ์ 'คาเรน' และกดแท็บ</span><span class="sxs-lookup"><span data-stu-id="4ba23-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="4ba23-110">คลิกค้นหา</span><span class="sxs-lookup"><span data-stu-id="4ba23-110">Click Search.</span></span>
    * <span data-ttu-id="4ba23-111">เนื่องจากมีลูกค้าชื่อคาเรนในข้อมูลสาธิตเพียงคนเดียว ข้อมูลดังกล่าวจะถูกเลือกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4ba23-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="4ba23-112">คลิกใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="4ba23-112">Click New sales order.</span></span>
5. <span data-ttu-id="4ba23-113">ขยายหรือยุบส่วนหัวของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="4ba23-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="4ba23-114">เลือกรหัสแหล่งที่มาสำหรับแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="4ba23-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="4ba23-115">ถ้าหากว่าไม่มีรหัสแหล่งที่มาที่เปิดใช้งานอยู่เลย คุณสามารถปิดฟิลด์ต้นทางและข้ามขั้นตอนนี้ไปได้</span><span class="sxs-lookup"><span data-stu-id="4ba23-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="4ba23-116">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="4ba23-116">Click Add line.</span></span>
8. <span data-ttu-id="4ba23-117">ในฟิลด์หมายเลขสินค้า ให้ป้อนเงื่อนไขการค้นหาสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ba23-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="4ba23-118">สำหรับขั้นตอนตัวอย่างนี้ ให้ป้อนหมายเลขสินค้าบางส่วนว่า '8111' และกดแท็บ นี่จะทำให้หน้าต่างการค้นหาสินค้าเด้งขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="4ba23-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="4ba23-119">เลือกผลิตภัณฑ์ที่จะเพิ่มในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="4ba23-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="4ba23-120">ป้อนปริมาณการขาย</span><span class="sxs-lookup"><span data-stu-id="4ba23-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="4ba23-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4ba23-121">Click Create.</span></span>
12. <span data-ttu-id="4ba23-122">คลิกเสร็จสมบูรณ์เพื่อรวบรวมข้อมูลการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4ba23-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="4ba23-123">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="4ba23-123">Click Add.</span></span>
    * <span data-ttu-id="4ba23-124">เพิ่มการเชื่อมโยง จะอยู่ในแท็บการชำระเงิน ให้ขยายแท็บการชำระเงินถ้ามันถูกยุบอยู่</span><span class="sxs-lookup"><span data-stu-id="4ba23-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="4ba23-125">เลือกวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4ba23-125">Select the payment method.</span></span>
    * <span data-ttu-id="4ba23-126">สำหรับขั้นตอนนี้ ให้เลือกวิธีการชำระเงินสด</span><span class="sxs-lookup"><span data-stu-id="4ba23-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="4ba23-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4ba23-127">Close the page.</span></span>
16. <span data-ttu-id="4ba23-128">ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="4ba23-128">Enter the amount.</span></span>
    * <span data-ttu-id="4ba23-129">สำหรับขั้นตอนนี้ ให้ป้อนยอดเงินเท่ากับยอดดุลใบสั่งซึ่งสามารถดูได้ในหน้าสรุปใบสั่งขายทางด้านซ้ายของฟิลด์ยอดเงิน </span><span class="sxs-lookup"><span data-stu-id="4ba23-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="4ba23-130">ซึ่งจะทำให้คุณสามารถดำเนินการใบสั่งจนเสร็จสิ้นว่าชำระครบถ้วนแล้ว</span><span class="sxs-lookup"><span data-stu-id="4ba23-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="4ba23-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4ba23-131">Click OK.</span></span>
18. <span data-ttu-id="4ba23-132">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="4ba23-132">Click Submit.</span></span>


