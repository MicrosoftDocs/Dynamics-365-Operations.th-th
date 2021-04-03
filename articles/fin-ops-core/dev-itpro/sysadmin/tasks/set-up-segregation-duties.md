---
title: ตั้งค่าการแบ่งแยกหน้าที่
description: 'คุณสามารถตั้งค่ากฎเพื่อแยกงานที่ต้องดำเนินการโดยผู้ใช้ต่างๆ '
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c1521d6bbbe12964fef0942fcc4943f12a4360a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562508"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="dcd56-103">ตั้งค่าการแบ่งแยกหน้าที่</span><span class="sxs-lookup"><span data-stu-id="dcd56-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcd56-104">คุณสามารถตั้งค่ากฎเพื่อแยกงานที่ต้องดำเนินการโดยผู้ใช้ต่างๆ </span><span class="sxs-lookup"><span data-stu-id="dcd56-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="dcd56-105">แนวคิดนี้มีชื่อว่าการแบ่งแยกหน้าที่ </span><span class="sxs-lookup"><span data-stu-id="dcd56-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="dcd56-106">ตัวอย่างเช่น คุณอาจไม่ต้องการบุคคลเดียวกันเพื่อยืนยันการรับสินค้าและเพื่อประมวลผลการชำระเงินให้กับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="dcd56-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="dcd56-107">การแบ่งแยกหน้าที่จะช่วยคุณในการลดความเสี่ยงของการฉ้อโกง และยังช่วยให้คุณตรวจพบข้อผิดพลาดหรือความผิดปกติต่างๆ </span><span class="sxs-lookup"><span data-stu-id="dcd56-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="dcd56-108">คุณยังสามารถใช้การแบ่งแยกหน้าที่เพื่อบังคับใช้นโยบายการควบคุมภายใน </span><span class="sxs-lookup"><span data-stu-id="dcd56-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="dcd56-109">ดำเนินการตามกระบวนงานต่อไปนี้เพื่อสร้างกฎให้เสร็จสมบูรณ์ </span><span class="sxs-lookup"><span data-stu-id="dcd56-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="dcd56-110">คุณต้องเป็นผู้ดูแลระบบเพื่อดำเนินการขั้นตอนให้เสร็จสมบูรณ์ </span><span class="sxs-lookup"><span data-stu-id="dcd56-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="dcd56-111">ไปที่ **การดูแลระบบ** > **ความปลอดภัย** > **การแบ่งแยกหน้าที่** > **กฎการแบ่งแยกหน้าที่**</span><span class="sxs-lookup"><span data-stu-id="dcd56-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="dcd56-112">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="dcd56-112">Click **New**.</span></span>
3. <span data-ttu-id="dcd56-113">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าสำหรับกฎนี้</span><span class="sxs-lookup"><span data-stu-id="dcd56-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="dcd56-114">ในฟิลด์ **หน้าที่แรก** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dcd56-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="dcd56-115">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="dcd56-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="dcd56-116">เลือกหน้าที่แรกที่ถูกควบคุมโดยกฎ</span><span class="sxs-lookup"><span data-stu-id="dcd56-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="dcd56-117">ในฟิลด์ **หน้าที่ที่สอง** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dcd56-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="dcd56-118">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="dcd56-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="dcd56-119">เลือกหน้าที่รองที่ถูกควบคุมโดยกฎ</span><span class="sxs-lookup"><span data-stu-id="dcd56-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="dcd56-120">ในฟิลด์ **ความรุนแรง** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="dcd56-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="dcd56-121">เลือกความรุนแรงของความเสี่ยงที่เกิดขึ้นเมื่อผู้ใช้เดียวกันหรือบทบาทเดียวกันทำหน้าที่ทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="dcd56-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="dcd56-122">ในฟิลด์ **ความเสี่ยงด้านความปลอดภัย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dcd56-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="dcd56-123">ป้อนคำอธิบายของความเสี่ยงด้านความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="dcd56-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="dcd56-124">ในฟิลด์ **การลดปัญหาด้านความปลอดภัย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dcd56-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="dcd56-125">ป้อนคำอธิบายของการดำเนินการที่คุณใช้ในการลดความเสี่ยงด้านความปลอดภัยใน </span><span class="sxs-lookup"><span data-stu-id="dcd56-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="dcd56-126">ตัวอย่างเช่น คุณสามารถลดความเสี่ยงในการตรวจสอบอย่างละเอียดของกระบวนการ โดยการทำการตรวจทานจัดการรายเดือน หรือโดยการใช้ทรัพยากรร่วมกับแผนกอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="dcd56-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="dcd56-127">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dcd56-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="dcd56-128">ไม่มีการตรวจสอบการปฏิบัติตามกฎการแบ่งแยกหน้าที่เมื่อคุณสร้างกฎ</span><span class="sxs-lookup"><span data-stu-id="dcd56-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="dcd56-129">คุณสามารถสร้างกฎที่สร้างความขัดแย้งให้กับบทบาทที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="dcd56-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="dcd56-130">การมอบหมายบทบาทผู้ใช้ที่มีอยู่ยังสามารถขัดแย้งกับกฎใหม่ด้วย</span><span class="sxs-lookup"><span data-stu-id="dcd56-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="dcd56-131">คุณต้องตรวจสอบความถูกต้องของการปฏิบัติตามกฎระเบียบหลังจากที่คุณสร้างหรือปรับเปลี่ยนกฎ</span><span class="sxs-lookup"><span data-stu-id="dcd56-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="dcd56-132">สำหรับข้อมูลเพิ่มเติม ให้ดู [ระบุและแก้ไขความขัดแย้งในการแบ่งแยกหน้าที่](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="dcd56-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]