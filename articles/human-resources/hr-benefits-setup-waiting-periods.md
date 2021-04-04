---
title: ตั้งค่าคอนฟิกรอบระยะเวลาที่รอ
description: ใน Microsoft Dynamics 365 Human Resources วันที่กำลังรอสร้างเหตุการณ์สำคัญเพื่อใช้สำหรับแผนสวัสดิการ
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e08c0c02393506e1e292676c954bdf3850029f7
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468310"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="404a8-103">ตั้งค่าคอนฟิกรอบระยะเวลาที่รอ</span><span class="sxs-lookup"><span data-stu-id="404a8-103">Configure waiting periods</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="404a8-104">ใน Microsoft Dynamics 365 Human Resources วันที่กำลังรอสร้างเหตุการณ์สำคัญเพื่อใช้สำหรับแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="404a8-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="404a8-105">ตัวอย่างเช่น สามเดือนนับจากวันที่จ้างงาน วันแรกของเดือนแต่ละเดือน หรือหกเดือน</span><span class="sxs-lookup"><span data-stu-id="404a8-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="404a8-106">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **การตั้งค่า** ให้เลือก **ช่วงเวลาที่กำลังรอ**</span><span class="sxs-lookup"><span data-stu-id="404a8-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="404a8-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="404a8-107">Select **New**.</span></span>

3. <span data-ttu-id="404a8-108">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="404a8-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="404a8-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="404a8-109">Field</span></span> | <span data-ttu-id="404a8-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="404a8-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="404a8-111">**รหัสการรอ**</span><span class="sxs-lookup"><span data-stu-id="404a8-111">**Waiting code**</span></span> | <span data-ttu-id="404a8-112">ตัวระบุเฉพาะสำหรับช่วงเวลาที่กำลังรอ</span><span class="sxs-lookup"><span data-stu-id="404a8-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="404a8-113">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="404a8-113">**Description**</span></span> | <span data-ttu-id="404a8-114">คำอธิบายเกี่ยวกับช่วงเวลาที่กำลังรอ</span><span class="sxs-lookup"><span data-stu-id="404a8-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="404a8-115">**วิธีการรอ**</span><span class="sxs-lookup"><span data-stu-id="404a8-115">**Waiting method**</span></span> | <span data-ttu-id="404a8-116">เลือกวิธีการที่รอที่เหมาะสมจากรายการแบบหล่นลงของค่าต่างๆ</span><span class="sxs-lookup"><span data-stu-id="404a8-116">Select the appropriate waiting method from the drop-down list of values.</span></span> <span data-ttu-id="404a8-117">ตัวเลือกเป็นสุทธิ เดือนปัจจุบัน ไตรมาสปัจจุบัน ปีปัจจุบัน และสัปดาห์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="404a8-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="404a8-118">**เดือน**</span><span class="sxs-lookup"><span data-stu-id="404a8-118">**Months**</span></span> | <span data-ttu-id="404a8-119">ป้อนจำนวนเดือนที่จะเพิ่มที่วิธีการที่รอเพื่อคำนวณวันที่รอ</span><span class="sxs-lookup"><span data-stu-id="404a8-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="404a8-120">**วัน**</span><span class="sxs-lookup"><span data-stu-id="404a8-120">**Days**</span></span> | <span data-ttu-id="404a8-121">ป้อนจำนวนวันเพื่อเพิ่มที่วิธีการที่รอเพื่อคำนวณวันที่รอ</span><span class="sxs-lookup"><span data-stu-id="404a8-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="404a8-122">**จำนวนวันที่รอ**</span><span class="sxs-lookup"><span data-stu-id="404a8-122">**Waiting day**</span></span> | <span data-ttu-id="404a8-123">เลือกวันที่รอเพื่อใช้ในการคำนวณวันที่รอ</span><span class="sxs-lookup"><span data-stu-id="404a8-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="404a8-124">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="404a8-124">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]