--- 
title: "ตั้งค่าภาษีหัก ณ ที่จ่าย"
description: "ภาษีหัก ณ ที่จ่ายคือ ภาษีสำหรับผู้จัดจำหน่ายที่ไม่ได้สร้างธุรกรรมภาษีขาย "
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc4c0745235052cb4145bc7083fef1a88c8bb5c9
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="fe761-103">ตั้งค่าภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe761-103">Set up withholding tax</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fe761-104">ภาษีหัก ณ ที่จ่ายคือ ภาษีสำหรับผู้จัดจำหน่ายที่ไม่ได้สร้างธุรกรรมภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="fe761-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="fe761-105">ภาษีหัก ณ ที่จ่ายที่มีการคำนวณจากการชำระเงินของผู้จัดจำหน่ายถือเป็นหนี้สิน </span><span class="sxs-lookup"><span data-stu-id="fe761-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="fe761-106">ดังนั้น เฉพาะบัญชีงบดุลหรือบัญชีหนี้สินเท่านั้นที่เป็นบัญชีที่ใช้ได้สำหรับการลงบัญชีภาษีหัก ณ ที่จ่าย </span><span class="sxs-lookup"><span data-stu-id="fe761-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="fe761-107">คู่มืองานนี้แสดงวิธีการตั้งค่าภาษี ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe761-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="fe761-108">ไปที่ภาษี > ภาษีทางอ้อม > ภาษีหัก ณ ที่จ่าย > รหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe761-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="fe761-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fe761-109">Click New.</span></span>
3. <span data-ttu-id="fe761-110">ในฟิลด์รหัสภาษีหัก ณ ที่จ่าย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fe761-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="fe761-111">ในฟิลด์ชื่อของภาษีหัก ณ ที่จ่าย ให้ป้อนชื่อของรหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe761-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="fe761-112">ในฟิลด์บัญชีหลัก ให้เลือกบัญชีหลักสำหรับการลงรายการบัญชีภาระภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe761-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="fe761-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fe761-113">Click Save.</span></span>
7. <span data-ttu-id="fe761-114">คลิกที่ค่า</span><span class="sxs-lookup"><span data-stu-id="fe761-114">Click Values.</span></span>
8. <span data-ttu-id="fe761-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fe761-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="fe761-116">ในฟิลด์ค่า ให้ป้อนเปอร์เซ็นต์ที่ใช้สำหรับการคำนวณภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe761-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="fe761-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fe761-117">Click Save.</span></span>
11. <span data-ttu-id="fe761-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe761-118">Close the page.</span></span>
12. <span data-ttu-id="fe761-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fe761-119">Click Save.</span></span>
13. <span data-ttu-id="fe761-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe761-120">Close the page.</span></span>
14. <span data-ttu-id="fe761-121">ไปที่ภาษี > ภาษีทางอ้อม > ภาษีหัก ณ ที่จ่าย > กลุ่มรหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe761-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="fe761-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fe761-122">Click New.</span></span>
16. <span data-ttu-id="fe761-123">ในฟิลด์กลุ่มภาษีหัก ณ ที่จ่าย ให้ป้อนตัวระบุของกลุ่มภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe761-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="fe761-124">ในฟิลด์คำอธิบาย ให้ป้อนชื่อของกลุ่มภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe761-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="fe761-125">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fe761-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="fe761-126">ในฟิลด์รหัสภาษีหัก ณ ที่จ่าย ให้เลือกรหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="fe761-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="fe761-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fe761-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="fe761-128">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fe761-128">Click Save.</span></span>


