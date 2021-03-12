---
title: สร้างงบประมาณตั้งต้น และจากนั้นกลับการเข้ารายการงบประมาณเบื้องต้นในภาครัฐ
description: 'หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการสร้างและย้อนกลับรายการงบประมาณเดิมโดยใช้แบบจำลองงบประมาณและค่ามิติที่มีจำนวนงบประมาณเบื้องต้น '
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 134e2ca851d72965198026107817c66a808ac705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987965"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="1c571-103">สร้างงบประมาณตั้งต้น และจากนั้นกลับการเข้ารายการงบประมาณเบื้องต้นในภาครัฐ</span><span class="sxs-lookup"><span data-stu-id="1c571-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c571-104">เมื่อคุณสร้างรายการทะเบียนงบประมาณเดิมและใช้แบบจำลองงบประมาณและค่ามิติที่ประกอบด้วยจำนวนงบประมาณเบื้องต้น คุณสามารถกลับรายการจำนวนงบประมาณเบื้องต้น </span><span class="sxs-lookup"><span data-stu-id="1c571-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="1c571-105">ขั้นตอนนี้ถูกสร้างขึ้นโดยใช้ข้อมูลของบริษัทสาธิต PSUS ในพาร์ติชันภาครัฐ </span><span class="sxs-lookup"><span data-stu-id="1c571-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="1c571-106">ไปที่การจัดทำงบประมาณ > รายการทะเบียนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="1c571-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="1c571-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="1c571-107">Click New.</span></span>
3. <span data-ttu-id="1c571-108">ในฟิลด์แบบจำลองงบประมาณ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="1c571-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1c571-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c571-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="1c571-110">ในฟิลด์รหัสงบประมาณ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="1c571-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1c571-111">ในรายการ คลิกงบประมาณเดิม</span><span class="sxs-lookup"><span data-stu-id="1c571-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="1c571-112">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="1c571-112">Click Save.</span></span>
8. <span data-ttu-id="1c571-113">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="1c571-113">Click Add line.</span></span>
9. <span data-ttu-id="1c571-114">ไม่จำเป็น: ถ้าคุณต้องการเปลี่ยนวันที่จากในส่วนหัว ให้ป้อนวันที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="1c571-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="1c571-115">วันที่นี้กำหนดรอบระยะเวลาทางบัญชีที่งบประมาณจะถูกบันทึกลงไป</span><span class="sxs-lookup"><span data-stu-id="1c571-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="1c571-116">ในฟิลด์โครงสร้างทางบัญชี ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="1c571-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="1c571-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c571-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="1c571-118">ในฟิลด์ค่ามิติ ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c571-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="1c571-119">ในฟิลด์จำนวน ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="1c571-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="1c571-120">ในฟิลด์สกุลเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="1c571-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="1c571-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1c571-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="1c571-122">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="1c571-122">Click Save.</span></span>
17. <span data-ttu-id="1c571-123">คลิกอัพเดตยอดดุลงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="1c571-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="1c571-124">ไม่จำเป็น: คุณสามารถเลือกตัวเลือกกลับรายการงบประมาณเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="1c571-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="1c571-125">หมายเหตุว่า คุณสามารถกลับรายการงบประมาณเบื้องต้นทั้งหมด หรือเฉพาะรายการงบประมาณเบื้องต้นที่มีรหัสงบประมาณที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="1c571-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="1c571-126">ในการเลือกข้อมูลที่ไม่จำเป็นต้องระบุ คลิกไอคอนปลดล็อคที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="1c571-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="1c571-127">คลิก อัพเดต ข้อมูลเพิ่มเติมจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="1c571-127">Click Update.</span></span>

