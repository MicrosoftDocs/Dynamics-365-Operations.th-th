---
title: ตั้งค่าคอนฟิกช่วงเวลาที่กำลังรอ
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: ec64343e0db8877e108d5fc665443ff017477ccf
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010786"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="2fe60-102">ตั้งค่าคอนฟิกช่วงเวลาที่กำลังรอ</span><span class="sxs-lookup"><span data-stu-id="2fe60-102">Configure waiting periods</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2fe60-103">ใน Microsoft Dynamics 365 Human Resources วันที่กำลังรอสร้างเหตุการณ์สำคัญเพื่อใช้สำหรับแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="2fe60-103">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="2fe60-104">ตัวอย่างเช่น สามเดือนนับจากวันที่จ้างงาน วันแรกของเดือนแต่ละเดือน หรือหกเดือน</span><span class="sxs-lookup"><span data-stu-id="2fe60-104">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="2fe60-105">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **การตั้งค่า** ให้เลือก **ช่วงเวลาที่กำลังรอ**</span><span class="sxs-lookup"><span data-stu-id="2fe60-105">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="2fe60-106">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2fe60-106">Select **New**.</span></span>

3. <span data-ttu-id="2fe60-107">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2fe60-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="2fe60-108">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="2fe60-108">Field</span></span> | <span data-ttu-id="2fe60-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2fe60-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2fe60-110">รหัสการรอ</span><span class="sxs-lookup"><span data-stu-id="2fe60-110">Waiting code</span></span> | <span data-ttu-id="2fe60-111">ตัวระบุเฉพาะสำหรับช่วงเวลาที่กำลังรอ</span><span class="sxs-lookup"><span data-stu-id="2fe60-111">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="2fe60-112">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2fe60-112">Description</span></span> | <span data-ttu-id="2fe60-113">คำอธิบายเกี่ยวกับช่วงเวลาที่กำลังรอ</span><span class="sxs-lookup"><span data-stu-id="2fe60-113">A description of the waiting period.</span></span> |
   | <span data-ttu-id="2fe60-114">วิธีการรอ</span><span class="sxs-lookup"><span data-stu-id="2fe60-114">Waiting method</span></span> | <span data-ttu-id="2fe60-115">เลือกวิธีการที่รอที่เหมาะสมจากรายการแบบหล่นของค่าต่างๆ</span><span class="sxs-lookup"><span data-stu-id="2fe60-115">Select the appropriate waiting method from the drop down list of values.</span></span> <span data-ttu-id="2fe60-116">ตัวเลือกเป็นสุทธิ เดือนปัจจุบัน ไตรมาสปัจจุบัน ปีปัจจุบัน และสัปดาห์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2fe60-116">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="2fe60-117">เดือน</span><span class="sxs-lookup"><span data-stu-id="2fe60-117">Months</span></span> | <span data-ttu-id="2fe60-118">ป้อนจำนวนเดือนที่จะเพิ่มที่วิธีการที่รอเพื่อคำนวณวันที่รอ</span><span class="sxs-lookup"><span data-stu-id="2fe60-118">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="2fe60-119">Days</span><span class="sxs-lookup"><span data-stu-id="2fe60-119">Days</span></span> | <span data-ttu-id="2fe60-120">ป้อนจำนวนวันเพื่อเพิ่มที่วิธีการที่รอเพื่อคำนวณวันที่รอ</span><span class="sxs-lookup"><span data-stu-id="2fe60-120">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="2fe60-121">จำนวนวันที่รอ</span><span class="sxs-lookup"><span data-stu-id="2fe60-121">Waiting day</span></span> | <span data-ttu-id="2fe60-122">เลือกวันที่รอเพื่อใช้ในการคำนวณวันที่รอ</span><span class="sxs-lookup"><span data-stu-id="2fe60-122">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="2fe60-123">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2fe60-123">Select **Save**.</span></span>
