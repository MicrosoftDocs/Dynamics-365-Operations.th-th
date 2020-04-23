---
title: ตั้งค่าคอนฟิกรอบระยะเวลาที่รอ
description: ใน Microsoft Dynamics 365 Human Resources วันที่กำลังรอสร้างเหตุการณ์สำคัญเพื่อใช้สำหรับแผนสวัสดิการ
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: adb7842231e8092398b240a2f017c28821b13ee1
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229590"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="bcf84-103">ตั้งค่าคอนฟิกรอบระยะเวลาที่รอ</span><span class="sxs-lookup"><span data-stu-id="bcf84-103">Configure waiting periods</span></span>

<span data-ttu-id="bcf84-104">ใน Microsoft Dynamics 365 Human Resources วันที่กำลังรอสร้างเหตุการณ์สำคัญเพื่อใช้สำหรับแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="bcf84-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="bcf84-105">ตัวอย่างเช่น สามเดือนนับจากวันที่จ้างงาน วันแรกของเดือนแต่ละเดือน หรือหกเดือน</span><span class="sxs-lookup"><span data-stu-id="bcf84-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="bcf84-106">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **การตั้งค่า** ให้เลือก **ช่วงเวลาที่กำลังรอ**</span><span class="sxs-lookup"><span data-stu-id="bcf84-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="bcf84-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="bcf84-107">Select **New**.</span></span>

3. <span data-ttu-id="bcf84-108">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bcf84-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bcf84-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="bcf84-109">Field</span></span> | <span data-ttu-id="bcf84-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bcf84-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bcf84-111">**รหัสการรอ**</span><span class="sxs-lookup"><span data-stu-id="bcf84-111">**Waiting code**</span></span> | <span data-ttu-id="bcf84-112">ตัวระบุเฉพาะสำหรับช่วงเวลาที่กำลังรอ</span><span class="sxs-lookup"><span data-stu-id="bcf84-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="bcf84-113">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="bcf84-113">**Description**</span></span> | <span data-ttu-id="bcf84-114">คำอธิบายเกี่ยวกับช่วงเวลาที่กำลังรอ</span><span class="sxs-lookup"><span data-stu-id="bcf84-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="bcf84-115">**วิธีการรอ**</span><span class="sxs-lookup"><span data-stu-id="bcf84-115">**Waiting method**</span></span> | <span data-ttu-id="bcf84-116">เลือกวิธีการที่รอที่เหมาะสมจากรายการแบบหล่นลงของค่าต่างๆ</span><span class="sxs-lookup"><span data-stu-id="bcf84-116">Select the appropriate waiting method from the drop-down list of values.</span></span> <span data-ttu-id="bcf84-117">ตัวเลือกเป็นสุทธิ เดือนปัจจุบัน ไตรมาสปัจจุบัน ปีปัจจุบัน และสัปดาห์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bcf84-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="bcf84-118">**เดือน**</span><span class="sxs-lookup"><span data-stu-id="bcf84-118">**Months**</span></span> | <span data-ttu-id="bcf84-119">ป้อนจำนวนเดือนที่จะเพิ่มที่วิธีการที่รอเพื่อคำนวณวันที่รอ</span><span class="sxs-lookup"><span data-stu-id="bcf84-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="bcf84-120">**วัน**</span><span class="sxs-lookup"><span data-stu-id="bcf84-120">**Days**</span></span> | <span data-ttu-id="bcf84-121">ป้อนจำนวนวันเพื่อเพิ่มที่วิธีการที่รอเพื่อคำนวณวันที่รอ</span><span class="sxs-lookup"><span data-stu-id="bcf84-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="bcf84-122">**จำนวนวันที่รอ**</span><span class="sxs-lookup"><span data-stu-id="bcf84-122">**Waiting day**</span></span> | <span data-ttu-id="bcf84-123">เลือกวันที่รอเพื่อใช้ในการคำนวณวันที่รอ</span><span class="sxs-lookup"><span data-stu-id="bcf84-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="bcf84-124">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="bcf84-124">Select **Save**.</span></span>
