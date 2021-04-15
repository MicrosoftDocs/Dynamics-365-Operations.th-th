---
title: สร้างงบประมาณเบื้องต้นสำหรับภาครัฐ
description: 'คุณสามารถสร้างรายการทะเบียนงบประมาณเบื้องต้นสำหรับแบบจำลองงบประมาณเฉพาะและค่ามิติ '
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c7937402f63db23c2b42d61c584c17dce5e1bf10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811226"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="106dd-103">สร้างงบประมาณเบื้องต้นสำหรับภาครัฐ</span><span class="sxs-lookup"><span data-stu-id="106dd-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="106dd-104">คุณสามารถสร้างรายการทะเบียนงบประมาณเบื้องต้นสำหรับแบบจำลองงบประมาณเฉพาะและค่ามิติ </span><span class="sxs-lookup"><span data-stu-id="106dd-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="106dd-105">หลังจากที่มีอนุมัติงบประมาณจริง คุณสามารถสร้างรายการทะเบียนงบประมาณเดิม </span><span class="sxs-lookup"><span data-stu-id="106dd-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="106dd-106">ขั้นตอนนี้ถูกสร้างขึ้นโดยใช้ข้อมูลของบริษัทสาธิต PSUS ในพาร์ติชันภาครัฐ </span><span class="sxs-lookup"><span data-stu-id="106dd-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="106dd-107">ไปที่การจัดทำงบประมาณ > รายการทะเบียนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="106dd-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="106dd-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="106dd-108">Click New.</span></span>
3. <span data-ttu-id="106dd-109">ในฟิลด์แบบจำลองงบประมาณ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="106dd-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="106dd-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="106dd-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="106dd-111">ในฟิลด์รหัสงบประมาณ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="106dd-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="106dd-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="106dd-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="106dd-113">ในฟิลด์รหัสเหตุผล ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="106dd-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="106dd-114">ในรายการนี้ คลิกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="106dd-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="106dd-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="106dd-115">Click Save.</span></span>
10. <span data-ttu-id="106dd-116">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="106dd-116">Click Add line.</span></span>
    * <span data-ttu-id="106dd-117">ไม่จำเป็น: ถ้าคุณต้องการเปลี่ยนวันที่จากในส่วนหัว ให้ป้อนวันที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="106dd-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="106dd-118">วันที่นี้กำหนดรอบระยะเวลาทางบัญชีที่งบประมาณจะถูกบันทึกลงไป</span><span class="sxs-lookup"><span data-stu-id="106dd-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="106dd-119">เมื่อดูคู่มืองาน เพื่อเติมข้อมูลฟิลด์อื่น คลิกปลดล็อคที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="106dd-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="106dd-120">ในฟิลด์โครงสร้างทางบัญชี ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="106dd-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="106dd-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="106dd-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="106dd-122">ในฟิลด์ค่ามิติ ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="106dd-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="106dd-123">ในฟิลด์จำนวน ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="106dd-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="106dd-124">คุณยังสามารถป้อนชนิดของจำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="106dd-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="106dd-125">ในฟิลด์สกุลเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="106dd-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="106dd-126">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="106dd-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="106dd-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="106dd-127">Click Save.</span></span>
18. <span data-ttu-id="106dd-128">คลิกอัพเดตยอดดุลงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="106dd-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="106dd-129">คลิก อัพเดต ข้อมูลเพิ่มเติมจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="106dd-129">Click Update.</span></span>
    * <span data-ttu-id="106dd-130">เมื่อต้องการดูผลลัพธ์ของการอัพเดต คลิกรายละเอียดข้อความบนแถบสีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="106dd-130">To see the results of the update, click Message details on the blue bar.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]