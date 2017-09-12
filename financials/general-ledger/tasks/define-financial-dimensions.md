--- 
title: "กำหนดมิติทางการเงิน"
description: "คำแนะนำงานนี้สาธิตการเพิ่มเอนทิตี้ที่ได้รับการสนับสนุนมิติทางการเงินและมิติทางการเงินที่กำหนดเอง "
author: aprilolson
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
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0b72acf763f0f6dbc64c3e00986bc9eb0e366bb5
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="define-financial-dimensions"></a><span data-ttu-id="ce644-103">กำหนดมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ce644-103">Define financial dimensions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce644-104">คำแนะนำงานนี้สาธิตการเพิ่มเอนทิตี้ที่ได้รับการสนับสนุนมิติทางการเงินและมิติทางการเงินที่กำหนดเอง </span><span class="sxs-lookup"><span data-stu-id="ce644-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="ce644-105">คำแนะนำการใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="ce644-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="ce644-106">สร้างเอนทิตี้สนับสนุนมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ce644-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="ce644-107">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > มิติ > มิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ce644-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="ce644-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ce644-108">Click New.</span></span>
3. <span data-ttu-id="ce644-109">ในฟิลด์ค่าผู้ใช้ ให้เลือกเอนทิตี้กำหนดโดยระบบใช้เป็นพื้นฐานของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ce644-109">In the User values from field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="ce644-110">ในฟิลด์ชื่อมิติ ให้พิมพ์ค่าเพื่ออธิบายมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ce644-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="ce644-111">ชื่ออาจแตกต่างไปจากเอนทิตีิที่ระบบกำหนด แต่ไม่สามารถให้มีเว้นวรรคหรืออักขระพิเศษได้</span><span class="sxs-lookup"><span data-stu-id="ce644-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="ce644-112">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="ce644-112">Click Activate.</span></span>
    * <span data-ttu-id="ce644-113">การเรียกใช้มิติทางการเงินอัพเดตตาราง มีชื่อมิติทางการเงิน และลบมิติที่ถูกลบออก </span><span class="sxs-lookup"><span data-stu-id="ce644-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="ce644-114">คุณสามารถป้อนค่ามิติก่อนที่คุณเรียกใช้มิติทางการเงิน แต่ไม่สามารถใช้มิติทางการเงินได้จนกว่าจะมีการเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="ce644-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="ce644-115">คลิกปิดในข้อความที่เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ce644-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="ce644-116">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="ce644-116">Click Activate.</span></span>
    * <span data-ttu-id="ce644-117">สามารถกำหนดเวลาการเรียกใช้มิติให้รันตามชุดงานในวันและเวลาที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="ce644-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="ce644-118">คลิกค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="ce644-118">Click Dimension values.</span></span>
    * <span data-ttu-id="ce644-119">ค่ามิติบางรายการเป็นค่าเฉพาะบริษัท </span><span class="sxs-lookup"><span data-stu-id="ce644-119">Some dimension values are company specific.</span></span> <span data-ttu-id="ce644-120">คุณสามารถตรวจสอบได้ว่าเป็นค่าเฉพาะบริษัทซึ่งชื่อบริษัทจะแสดงให้เห็นในรายการค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="ce644-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="ce644-121">สร้างมิติทางการเงินที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ce644-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="ce644-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ce644-122">Close the page.</span></span>
2. <span data-ttu-id="ce644-123">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ce644-123">Click New.</span></span>
3. <span data-ttu-id="ce644-124">ในฟิลด์ ใช้ค่าจาก เลือก <Custom dimension></span><span class="sxs-lookup"><span data-stu-id="ce644-124">In the Use values from field, select <Custom dimension>.</span></span>
4. <span data-ttu-id="ce644-125">ในฟิลด์ชื่อมิติ ให้พิมพ์ค่าเพื่ออธิบายมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ce644-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="ce644-126">ชื่อต้องไม่มีช่องว่างหรืออักขระพิเศษ</span><span class="sxs-lookup"><span data-stu-id="ce644-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="ce644-127">คุณยังสามารถระบุตัวพรางบัญชีเพื่อจำกัดจำนวนและชนิดของข้อมูลที่คุณสามารถป้อนสำหรับค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="ce644-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="ce644-128">คุณสามารถป้อนอักขระที่ยังคงเหมือนเดิมสำหรับแต่ละค่ามิติ เช่น ตัวอักษรหรือเครื่องหมายยัติภังค์</span><span class="sxs-lookup"><span data-stu-id="ce644-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="ce644-129">คุณสามารถป้อนเครื่องหมายตัวเลข (#) และเครื่องหมายและ (&) ให้เป็นตัวยึดตำแหน่งสำหรับตัวอักษรและตัวเลขที่จะเปลี่ยนทุกครั้งที่มีการสร้างค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="ce644-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="ce644-130">ใช้เครื่องหมายตัวเลข (#) เป็นตัวยึดตำแหน่งสำหรับตัวเลข และเครื่องหมายและ (&) เป็นตัวยึดตำแหน่งสำหรับตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="ce644-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="ce644-131">ตัวอย่าง: เพื่อจำกัดค่ามิติให้กับตัวอักษร CC และตัวเลขสามหลัก ให้คุณป้อน CC-### เป็นตัวพรางรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="ce644-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="ce644-132">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="ce644-132">Click Activate.</span></span>
    * <span data-ttu-id="ce644-133">การเรียกใช้มิติทางการเงินอัพเดตตาราง มีชื่อมิติทางการเงิน และลบมิติที่ถูกลบออก </span><span class="sxs-lookup"><span data-stu-id="ce644-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="ce644-134">คุณสามารถป้อนค่ามิติก่อนที่คุณเรียกใช้มิติทางการเงิน แต่ไม่สามารถใช้มิติทางการเงินได้จนกว่าจะมีการเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="ce644-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="ce644-135">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="ce644-135">Click Activate.</span></span>
    * <span data-ttu-id="ce644-136">สามารถกำหนดเวลาการเรียกใช้มิติให้รันตามชุดงานในวันและเวลาที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="ce644-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="ce644-137">คลิกค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="ce644-137">Click Dimension values.</span></span>
8. <span data-ttu-id="ce644-138">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ce644-138">Click New.</span></span>
9. <span data-ttu-id="ce644-139">ในฟิลด์ค่ามิติ ให้พิมพ์ชื่อเพื่ออธิบายมิติทางการเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="ce644-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="ce644-140">ในฟิลด์คำอธิบาย ให้พิมพ์คำอธิบายที่อธิบายค่ามิติทางการเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="ce644-140">In the Description field, type a description that describes your financial dimension value.</span></span>


