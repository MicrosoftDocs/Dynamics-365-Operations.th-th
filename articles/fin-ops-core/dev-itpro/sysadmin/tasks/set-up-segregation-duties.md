---
title: ตั้งค่าการแบ่งแยกหน้าที่
description: 'คุณสามารถตั้งค่ากฎเพื่อแยกงานที่ต้องดำเนินการโดยผู้ใช้ต่างๆ '
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688184"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="a3980-103">ตั้งค่าการแบ่งแยกหน้าที่</span><span class="sxs-lookup"><span data-stu-id="a3980-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3980-104">คุณสามารถตั้งค่ากฎเพื่อแยกงานที่ต้องดำเนินการโดยผู้ใช้ต่างๆ </span><span class="sxs-lookup"><span data-stu-id="a3980-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="a3980-105">แนวคิดนี้มีชื่อว่าการแบ่งแยกหน้าที่ </span><span class="sxs-lookup"><span data-stu-id="a3980-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="a3980-106">ตัวอย่างเช่น คุณอาจไม่ต้องการบุคคลเดียวกันเพื่อยืนยันการรับสินค้าและเพื่อประมวลผลการชำระเงินให้กับผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="a3980-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="a3980-107">การแบ่งแยกหน้าที่จะช่วยคุณในการลดความเสี่ยงของการฉ้อโกง และยังช่วยให้คุณตรวจพบข้อผิดพลาดหรือความผิดปกติต่างๆ </span><span class="sxs-lookup"><span data-stu-id="a3980-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="a3980-108">คุณยังสามารถใช้การแบ่งแยกหน้าที่เพื่อบังคับใช้นโยบายการควบคุมภายใน </span><span class="sxs-lookup"><span data-stu-id="a3980-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="a3980-109">ดำเนินการตามกระบวนงานต่อไปนี้เพื่อสร้างกฎให้เสร็จสมบูรณ์ </span><span class="sxs-lookup"><span data-stu-id="a3980-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="a3980-110">คุณต้องเป็นผู้ดูแลระบบเพื่อดำเนินการขั้นตอนให้เสร็จสมบูรณ์ </span><span class="sxs-lookup"><span data-stu-id="a3980-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="a3980-111">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างกระบวนงานนี้คือ DAT </span><span class="sxs-lookup"><span data-stu-id="a3980-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="a3980-112">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การดูแลระบบ > ความปลอดภัย > การแบ่งแยกหน้าที่ > กฎการแบ่งแยกหน้าที่**</span><span class="sxs-lookup"><span data-stu-id="a3980-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="a3980-113">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="a3980-113">Click **New**.</span></span>
3. <span data-ttu-id="a3980-114">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าสำหรับกฎนี้</span><span class="sxs-lookup"><span data-stu-id="a3980-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="a3980-115">ในฟิลด์ **หน้าที่แรก** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a3980-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a3980-116">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a3980-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="a3980-117">เลือกหน้าที่แรกที่ถูกควบคุมโดยกฎ</span><span class="sxs-lookup"><span data-stu-id="a3980-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="a3980-118">ในฟิลด์ **หน้าที่ที่สอง** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a3980-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="a3980-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a3980-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="a3980-120">เลือกหน้าที่รองที่ถูกควบคุมโดยกฎ</span><span class="sxs-lookup"><span data-stu-id="a3980-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="a3980-121">ในฟิลด์ **ความรุนแรง** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="a3980-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="a3980-122">เลือกความรุนแรงของความเสี่ยงที่เกิดขึ้นเมื่อผู้ใช้เดียวกันหรือบทบาทเดียวกันทำหน้าที่ทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="a3980-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="a3980-123">ในฟิลด์ **ความเสี่ยงด้านความปลอดภัย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a3980-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="a3980-124">ป้อนคำอธิบายของความเสี่ยงด้านความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="a3980-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="a3980-125">ในฟิลด์ **การลดปัญหาด้านความปลอดภัย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a3980-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="a3980-126">ป้อนคำอธิบายของการดำเนินการที่คุณใช้ในการลดความเสี่ยงด้านความปลอดภัยใน </span><span class="sxs-lookup"><span data-stu-id="a3980-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="a3980-127">ตัวอย่างเช่น คุณสามารถลดความเสี่ยงในการตรวจสอบอย่างละเอียดของกระบวนการ โดยการทำการตรวจทานจัดการรายเดือน หรือโดยการใช้ทรัพยากรร่วมกับแผนกอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a3980-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="a3980-128">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a3980-128">Click **Save**.</span></span>

