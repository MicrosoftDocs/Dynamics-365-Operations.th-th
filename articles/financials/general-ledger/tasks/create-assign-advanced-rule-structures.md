---
title: สร้างและกำหนดโครงสร้างกฎขั้นสูง
description: 'คำแนะนำงานนี้ระบุขั้นตอนการสร้างและการกำหนดโครงสร้างกฎขั้นสูงให้กับโครงสร้างทางบัญชี '
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd62254c20cf5d77677d03c7d7335fb793d7f5f2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558917"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="7aa8d-103">สร้างและกำหนดโครงสร้างกฎขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7aa8d-104">คำแนะนำงานนี้ระบุขั้นตอนการสร้างและการกำหนดโครงสร้างกฎขั้นสูงให้กับโครงสร้างทางบัญชี </span><span class="sxs-lookup"><span data-stu-id="7aa8d-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="7aa8d-105">คำแนะนำนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="7aa8d-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="7aa8d-106">สร้างโครงสร้างกฎขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="7aa8d-107">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > โครงสร้าง > โครงสร้างกฎขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="7aa8d-108">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="7aa8d-109">ในฟิลด์โครงสร้างกฎขั้นสูง ให้พิมพ์ชื่อเพื่ออธิบายโครงสร้างกฎ</span><span class="sxs-lookup"><span data-stu-id="7aa8d-109">In the Advanced rule structure field, type a name to descritbe the rule structure.</span></span>
4. <span data-ttu-id="7aa8d-110">ในฟิลด์คำอธิบาย ให้พิมพ์ค่าเพื่ออธิบายโครงสร้าง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="7aa8d-111">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7aa8d-111">Click OK.</span></span>
6. <span data-ttu-id="7aa8d-112">คลิก เพิ่มเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="7aa8d-112">Click Add segment.</span></span>
7. <span data-ttu-id="7aa8d-113">ในรายการเซ็กเมนต์ ให้เลือกมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="7aa8d-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="7aa8d-114">ตัวอย่างเช่น ร้านค้า</span><span class="sxs-lookup"><span data-stu-id="7aa8d-114">For example, Store.</span></span>  
8. <span data-ttu-id="7aa8d-115">คลิก เพิ่มเซ็กเมนต์</span><span class="sxs-lookup"><span data-stu-id="7aa8d-115">Click Add segment.</span></span>
9. <span data-ttu-id="7aa8d-116">ในรายการ คลิกลิงค์ของโครงสร้างกฎขั้นสูงเพื่อดู</span><span class="sxs-lookup"><span data-stu-id="7aa8d-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="7aa8d-117">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="7aa8d-117">Click Activate.</span></span>
11. <span data-ttu-id="7aa8d-118">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="7aa8d-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="7aa8d-119">ใช้โครงสร้างกฎขั้นสูงเพื่อโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="7aa8d-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="7aa8d-120">ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="7aa8d-120">Close the form.</span></span>
2. <span data-ttu-id="7aa8d-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7aa8d-121">Close the page.</span></span>
3. <span data-ttu-id="7aa8d-122">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > โครงสร้าง > ตั้งค่าคอนฟิกโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="7aa8d-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="7aa8d-123">ในรายการ ให้ค้นหาและเลือกโครงสร้างทางบัญชีที่คุณต้องการนำกฎขั้นสูงไปใช้</span><span class="sxs-lookup"><span data-stu-id="7aa8d-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="7aa8d-124">คลิกชื่อของโครงสร้างทางบัญชีเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="7aa8d-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="7aa8d-125">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="7aa8d-125">Click Edit.</span></span>
    * <span data-ttu-id="7aa8d-126">คุณสามารถคลิกฎขั้นสูง และระบบจะขอให้คุณวางโครงสร้างทางบัญชีในโหมดแบบร่าง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="7aa8d-127">คลิกกฎขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="7aa8d-128">คลิกที่สร้างเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="7aa8d-129">ในฟิลด์กฎชั้นสูง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="7aa8d-130">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="7aa8d-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="7aa8d-131">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-131">Click Create.</span></span>
12. <span data-ttu-id="7aa8d-132">คลิก เพิ่มเกณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="7aa8d-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="7aa8d-133">ในฟิลด์สถานที่ ให้เลือกบัญชีหลักหรือมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="7aa8d-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="7aa8d-134">ในฟิลด์ผู้ปฏิบัติงาน ให้เลือกตัวเลือก เช่น อยู่ระหว่าง และ รวม</span><span class="sxs-lookup"><span data-stu-id="7aa8d-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="7aa8d-135">ในฟิลด์ค่า ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="7aa8d-136">ในฟิลด์ผ่าน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="7aa8d-137">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7aa8d-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="7aa8d-138">ในรายการ ให้ค้นหาโครงสร้างกฎขั้นสูงที่คุณต้องการใช้เมื่อคุณพบเงื่อนไขที่ป้อนเข้าไป</span><span class="sxs-lookup"><span data-stu-id="7aa8d-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="7aa8d-139">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="7aa8d-139">Click Add.</span></span>
20. <span data-ttu-id="7aa8d-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7aa8d-140">Close the page.</span></span>
21. <span data-ttu-id="7aa8d-141">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="7aa8d-141">Click Activate.</span></span>
22. <span data-ttu-id="7aa8d-142">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="7aa8d-142">Click Activate.</span></span>

