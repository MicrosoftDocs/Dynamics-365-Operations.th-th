--- 
title: "การสร้างธุรกรรมค้างรับค้างจ่ายในบัญชีแยกประเภท"
description: "คู่มืองานนี้ดำเนินงานโดยการสร้างธุรกรรมคงค้างในบัญชีแยกประเภท ที่ขึ้นอยู่กับแผนงานการค้างรับค้างจ่าย"
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bfc514530149f25e6355992984b9e33f80194b2c
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="ecfbd-103">การสร้างธุรกรรมค้างรับค้างจ่ายในบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="ecfbd-103">Create ledger accrual transactions</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ecfbd-104">คำแนะนำงานนี้ระบุขั้นตอนสร้างธุรกรรมคงค้างในบัญชีแยกประเภทที่ขึ้นอยู่กับแผนงานการค้างรับค้างจ่าย</span><span class="sxs-lookup"><span data-stu-id="ecfbd-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="ecfbd-105">ไปที่บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="ecfbd-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="ecfbd-106">ในรายการ ให้ค้นหาและเลือกการหักค่าเสื่อมราคาที่ต้องการและสร้างใหม่</span><span class="sxs-lookup"><span data-stu-id="ecfbd-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="ecfbd-107">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขชุดงานสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="ecfbd-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="ecfbd-108">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ecfbd-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="ecfbd-109">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ecfbd-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="ecfbd-110">ในตัวอย่างนี้ เรากำลังกำหนดค่าใช้จ่ายสำหรับการประกันภัย </span><span class="sxs-lookup"><span data-stu-id="ecfbd-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="ecfbd-111">ซึ่งจะกลายเป็นยอดค่าใช้จ่ายประจำงวด</span><span class="sxs-lookup"><span data-stu-id="ecfbd-111">It will become a periodic expense amount.</span></span>  
6. <span data-ttu-id="ecfbd-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ecfbd-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="ecfbd-113">ในฟิลด์เดบิต ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="ecfbd-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="ecfbd-114">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ecfbd-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="ecfbd-115">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="ecfbd-115">Click Functions.</span></span>
10. <span data-ttu-id="ecfbd-116">คลิกการรับรู้บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="ecfbd-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="ecfbd-117">ในฟิลด์การระบุรายการค้างรับค้างจ่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="ecfbd-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="ecfbd-118">ในรายการ ให้ค้นหาและเลือกแบบแผนการรับรู้ที่คุณต้องการนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="ecfbd-118">In the list, find and select the accrual scheme you want to apply.</span></span>
13. <span data-ttu-id="ecfbd-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ecfbd-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="ecfbd-120">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่ </span><span class="sxs-lookup"><span data-stu-id="ecfbd-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="ecfbd-121">คลิกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ecfbd-121">Click Transactions.</span></span>
16. <span data-ttu-id="ecfbd-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ecfbd-122">Close the page.</span></span>
17. <span data-ttu-id="ecfbd-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ecfbd-123">Click OK.</span></span>
18. <span data-ttu-id="ecfbd-124">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="ecfbd-124">Click Post.</span></span>


