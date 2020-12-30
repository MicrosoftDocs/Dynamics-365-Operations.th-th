---
title: กำหนดมิติทางการเงิน
description: 'คำแนะนำงานนี้สาธิตการเพิ่มเอนทิตี้ที่ได้รับการสนับสนุนมิติทางการเงินและมิติทางการเงินที่กำหนดเอง '
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fbe739eec0cfa1e7b0276872640bd4f82be3ef7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448241"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="e0bc7-103">กำหนดมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e0bc7-103">Define financial dimensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0bc7-104">คำแนะนำงานนี้สาธิตการเพิ่มเอนทิตี้ที่ได้รับการสนับสนุนมิติทางการเงินและมิติทางการเงินที่กำหนดเอง </span><span class="sxs-lookup"><span data-stu-id="e0bc7-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="e0bc7-105">คำแนะนำการใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="e0bc7-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="e0bc7-106">สร้างเอนทิตี้สนับสนุนมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e0bc7-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="e0bc7-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > ผังบัญชี > มิติ > มิติทางการเงิน**.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="e0bc7-108">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e0bc7-108">Click **New**.</span></span>
3. <span data-ttu-id="e0bc7-109">ในฟิลด์ **ฟอร์มค่าผู้ใช้** ให้เลือกเอนทิตีที่กำหนดโดยระบบเพื่อใช้เป็นพื้นฐานของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e0bc7-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="e0bc7-110">ในฟิลด์ **ชื่อมิติ** ให้พิมพ์ค่าเพื่ออธิบายมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e0bc7-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="e0bc7-111">ชื่ออาจแตกต่างไปจากเอนทิตีิที่ระบบกำหนด แต่ไม่สามารถให้มีเว้นวรรคหรืออักขระพิเศษได้</span><span class="sxs-lookup"><span data-stu-id="e0bc7-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="e0bc7-112">คลิก **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="e0bc7-112">Click **Activate**.</span></span> <span data-ttu-id="e0bc7-113">การเรียกใช้มิติทางการเงินอัพเดตตาราง มีชื่อมิติทางการเงิน และลบมิติที่ถูกลบออก </span><span class="sxs-lookup"><span data-stu-id="e0bc7-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="e0bc7-114">คุณสามารถป้อนค่ามิติก่อนที่คุณเรียกใช้มิติทางการเงิน แต่ไม่สามารถใช้มิติทางการเงินได้จนกว่าจะมีการเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="e0bc7-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="e0bc7-115">คลิก **ปิด** ในข้อความเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="e0bc7-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="e0bc7-116">คลิก **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="e0bc7-116">Click **Activate**.</span></span> <span data-ttu-id="e0bc7-117">สามารถกำหนดเวลาการเรียกใช้มิติให้รันตามชุดงานในวันและเวลาที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="e0bc7-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="e0bc7-118">ใน **บานหน้าต่างการดำเนินการ** ให้คลิก **ค่ามิติ**</span><span class="sxs-lookup"><span data-stu-id="e0bc7-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="e0bc7-119">ค่ามิติบางรายการเป็นค่าเฉพาะบริษัท </span><span class="sxs-lookup"><span data-stu-id="e0bc7-119">Some dimension values are company specific.</span></span> <span data-ttu-id="e0bc7-120">คุณสามารถตรวจสอบได้ว่าเป็นค่าเฉพาะบริษัทซึ่งชื่อบริษัทจะแสดงให้เห็นในรายการค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="e0bc7-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="e0bc7-121">สร้างมิติทางการเงินที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="e0bc7-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="e0bc7-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e0bc7-122">Close the page.</span></span>
2. <span data-ttu-id="e0bc7-123">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e0bc7-123">Click **New**.</span></span>
3. <span data-ttu-id="e0bc7-124">ในฟิลด์ **ใช้ค่าจาก** ให้เลือก **มิติที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="e0bc7-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="e0bc7-125">ในฟิลด์ **ชื่อมิติ** ให้พิมพ์ค่าเพื่ออธิบายมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="e0bc7-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="e0bc7-126">ชื่อต้องไม่มีช่องว่างหรืออักขระพิเศษ</span><span class="sxs-lookup"><span data-stu-id="e0bc7-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="e0bc7-127">คุณยังสามารถระบุตัวพรางบัญชีเพื่อจำกัดจำนวนและชนิดของข้อมูลที่คุณสามารถป้อนสำหรับค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="e0bc7-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="e0bc7-128">คุณสามารถป้อนอักขระที่ยังคงเหมือนเดิมสำหรับแต่ละค่ามิติ เช่น ตัวอักษรหรือเครื่องหมายยัติภังค์</span><span class="sxs-lookup"><span data-stu-id="e0bc7-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="e0bc7-129">คุณสามารถป้อนเครื่องหมายตัวเลข (#) และเครื่องหมายและ (&) ให้เป็นตัวยึดตำแหน่งสำหรับตัวอักษรและตัวเลขที่จะเปลี่ยนทุกครั้งที่มีการสร้างค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="e0bc7-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="e0bc7-130">ใช้เครื่องหมายตัวเลข (#) เป็นตัวยึดตำแหน่งสำหรับตัวเลข และเครื่องหมายและ (&) เป็นตัวยึดตำแหน่งสำหรับตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="e0bc7-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="e0bc7-131">ตัวอย่าง: เพื่อจำกัดค่ามิติให้กับตัวอักษร CC และตัวเลขสามหลัก ให้คุณป้อน CC-### เป็นตัวพรางรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="e0bc7-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="e0bc7-132">คลิก **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="e0bc7-132">Click **Activate**.</span></span> <span data-ttu-id="e0bc7-133">การเรียกใช้มิติทางการเงินอัพเดตตาราง มีชื่อมิติทางการเงิน และลบมิติที่ถูกลบออก </span><span class="sxs-lookup"><span data-stu-id="e0bc7-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="e0bc7-134">คุณสามารถป้อนค่ามิติก่อนที่คุณเรียกใช้มิติทางการเงิน แต่ไม่สามารถใช้มิติทางการเงินได้จนกว่าจะมีการเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="e0bc7-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="e0bc7-135">คลิก **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="e0bc7-135">Click **Activate**.</span></span> <span data-ttu-id="e0bc7-136">สามารถกำหนดเวลาการเรียกใช้มิติให้รันตามชุดงานในวันและเวลาที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="e0bc7-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="e0bc7-137">ใน **บานหน้าต่างการดำเนินการ** ให้คลิก **ค่ามิติ**</span><span class="sxs-lookup"><span data-stu-id="e0bc7-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="e0bc7-138">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e0bc7-138">Click **New**.</span></span>
9. <span data-ttu-id="e0bc7-139">ในฟิลด์ **ค่ามิติ** ให้พิมพ์ชื่อเพื่ออธิบายค่ามิติทางการเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="e0bc7-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="e0bc7-140">ในฟิลด์ **คำอธิบาย** ให้พิมพ์คำอธิบายที่อธิบายค่ามิติทางการเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="e0bc7-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>

