---
title: สร้างรหัสดอกเบี้ยด้วยช่วงดอกเบี้ย
description: 'รหัสดอกเบี้ยสามารถตั้งค่าในการคำนวณยอดดอกเบี้ยที่แตกต่างกันตามช่วง '
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44b98436d6e0c40f0458dc4744b8b1d96baa8b54
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216580"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="00e2a-103">สร้างรหัสดอกเบี้ยด้วยช่วงดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="00e2a-103">Create an interest code with a range</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="00e2a-104">รหัสดอกเบี้ยสามารถตั้งค่าในการคำนวณยอดดอกเบี้ยที่แตกต่างกันตามช่วง </span><span class="sxs-lookup"><span data-stu-id="00e2a-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="00e2a-105">ขั้นตอนนี้จะแสดงวิธีการเพิ่มรหัสดอกเบี้ยและเพิ่มช่วงดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="00e2a-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="00e2a-106">ไปที่สินเชื่อและการเรียกเก็บเงิน > ดอกเบี้ย > ตั้งค่ารหัสดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="00e2a-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="00e2a-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="00e2a-107">Click New.</span></span>
3. <span data-ttu-id="00e2a-108">ในฟิลด์รหัสดอกเบี้ย ให้ป้อนชื่อรหัสดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="00e2a-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="00e2a-109">ในฟิลด์คำอธิบาย ป้อนคำอธิบายสำหรับรหัสดอกเบี้ย</span><span class="sxs-lookup"><span data-stu-id="00e2a-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="00e2a-110">เลือกเดือน</span><span class="sxs-lookup"><span data-stu-id="00e2a-110">Select Month.</span></span>
6. <span data-ttu-id="00e2a-111">ขยายส่วน รายได้</span><span class="sxs-lookup"><span data-stu-id="00e2a-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="00e2a-112">ขยายส่วน รายได้ตามสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="00e2a-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="00e2a-113">ในฟิลด์บัญชีการลงรายการบัญชีแยกประเภท ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="00e2a-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="00e2a-114">ในฟิลด์ดอกเบี้ยตามช่วง ให้เลือก 'เดือน'</span><span class="sxs-lookup"><span data-stu-id="00e2a-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="00e2a-115">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="00e2a-115">Click Add.</span></span>
11. <span data-ttu-id="00e2a-116">ในฟิลด์คำอธิบาย ให้ป้อนคำอธิบายสำหรับสกุลเงินและช่วง</span><span class="sxs-lookup"><span data-stu-id="00e2a-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="00e2a-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="00e2a-117">Click Save.</span></span>
13. <span data-ttu-id="00e2a-118">คลิกช่วงที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="00e2a-118">Click Ranges.</span></span>
14. <span data-ttu-id="00e2a-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="00e2a-119">Click New.</span></span>
15. <span data-ttu-id="00e2a-120">ป้อนค่าเริ่มต้นเป็น 0 แล้วป้อนเปอร์เซ็นต์ดอกเบี้ยสำหรับแต่ละเดือนที่จะใช้ในการคำนวณดอกเบี้ย </span><span class="sxs-lookup"><span data-stu-id="00e2a-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="00e2a-121">ตัวอย่างของเราคือ 1.5 %</span><span class="sxs-lookup"><span data-stu-id="00e2a-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="00e2a-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="00e2a-122">Click New.</span></span>
17. <span data-ttu-id="00e2a-123">ป้อนค่าถัดไปเป็น 4 ซึ่งจะเป็นเดือนแรกที่คุณสามารถคำนวณอัตราดอกเบี้ยใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="00e2a-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="00e2a-124">ป้อนเปอร์เซ็นต์ดอกเบี้ยสำหรับแต่ละเดือนที่จะใช้ในการคำนวณดอกเบี้ยซึ่งเริ่มต้นในเดือนที่ 4</span><span class="sxs-lookup"><span data-stu-id="00e2a-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="00e2a-125">สำหรับตัวอย่างนี้คือ 2.0</span><span class="sxs-lookup"><span data-stu-id="00e2a-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="00e2a-126">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="00e2a-126">Click New.</span></span>
20. <span data-ttu-id="00e2a-127">ป้อนค่าถัดไปเป็น 7 ซึ่งจะเป็นเดือนแรกที่คุณสามารถคำนวณอัตราดอกเบี้ยใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="00e2a-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="00e2a-128">ป้อนเปอร์เซ็นต์ดอกเบี้ยสำหรับแต่ละเดือนที่จะใช้ในการคำนวณดอกเบี้ยซึ่งเริ่มต้นในเดือนที่ 7</span><span class="sxs-lookup"><span data-stu-id="00e2a-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="00e2a-129">สำหรับตัวอย่างนี้คือ 2.5</span><span class="sxs-lookup"><span data-stu-id="00e2a-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="00e2a-130">คลิก "ปิด" เพื่อสิ้นสุดการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="00e2a-130">Click Close to complete the setup.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]