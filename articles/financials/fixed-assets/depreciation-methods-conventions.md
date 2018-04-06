---
title: "วิธีการคิดค่าเสื่อมราคาและแบบแผนการคิดค่าเสื่อมราคา"
description: "บทความนี้แสดงภาพรวมของแบบแผนการคิดค่าเสื่อมราคาและวิธีการคิดค่าเสื่อมราคาที่ได้รับการสนับสนุนโดย Microsoft Dynamics 365 for Finance and Operations"
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: eb38de1e7e39cb66d15bfe344f6f5fcd5d4fccd7
ms.contentlocale: th-th
ms.lasthandoff: 03/26/2018

---

# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="05383-103">วิธีการคิดค่าเสื่อมราคาและแบบแผนการคิดค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="05383-103">Depreciation methods and conventions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="05383-104">บทความนี้แสดงภาพรวมของแบบแผนการคิดค่าเสื่อมราคาและวิธีการคิดค่าเสื่อมราคาที่ได้รับการสนับสนุนโดย Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="05383-104">This article provides an overview of the depreciation conventions and depreciation methods that are supported by Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="05383-105">คุณสามารถเลือกวิธีการและแบบแผนการคิดค่าเสื่อมราคาต่างๆ ได้ </span><span class="sxs-lookup"><span data-stu-id="05383-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="05383-106">วัตถุประสงค์ของวิธีคือเพื่อ ปันส่วนค่าเสื่อมราคาของสินทรัพย์ถาวรในรอบระยะเวลาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="05383-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="05383-107">ค่าเสื่อมราคาของสินทรัพย์ถาวรคือ ราคาการซื้อสินทรัพย์ ลบด้วยมูลค่าซาก ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="05383-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="05383-108">ถ้าคุณกำลังใช้แบบแผนการคิดค่าเสื่อมราคา และคุณแก้ไขวันที่รันค่าเสื่อมราคาล่าสุดสำหรับสินทรัพย์ ซึ่งทำให้ค่าเสื่อมราคาบางค่าถูกข้ามไป ค่าเสื่อมราคาสำหรับปีที่แล้วอาจมากกว่า หรือน้อยกว่าที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="05383-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="05383-109">ค่าเสื่อมราคาถูกปรับปรุง โดยจำนวนรอบระยะเวลาการคิดค่าเสื่อมราคาที่ได้รับผลกระทบจากการปรับเปลี่ยนวันที่รันค่าเสื่อมราคาล่าสุด</span><span class="sxs-lookup"><span data-stu-id="05383-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="05383-110">ตัวอย่างเช่น ถ้าคุณกำลังใช้แบบแผนการคิดค่าเสื่อมราคาครึ่งปีในช่วงสามปี ค่าเสื่อมราคาโดยปกติเกิดขึ้นในช่วงเวลา 3 1/2 ปี</span><span class="sxs-lookup"><span data-stu-id="05383-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="05383-111">ถ้าคุณเปลี่ยนวันที่รันค่าเสื่อมราคาล่าสุดในระหว่าง 3 1/2 ปี ปีที่แล้วของการคิดค่าเสื่อมราคาย้ายจำนวนรอบระยะเวลาที่ได้รับผลกระทบออกไป</span><span class="sxs-lookup"><span data-stu-id="05383-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="05383-112">ถ้าคุณย้ายวันที่ไปสามเดือน ปีที่แล้วจะมีค่าเสื่อมราคามูลค่าเก้าเดือน โดยปกติจะเป็นค่าเสื่อมราคามูลค่าหกเดือน</span><span class="sxs-lookup"><span data-stu-id="05383-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="05383-113">คุณสามารถเลือกจากแบบแผนการคิดค่าเสื่อมราคาต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="05383-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="05383-114">ครึ่งปี</span><span class="sxs-lookup"><span data-stu-id="05383-114">Half year</span></span>
-   <span data-ttu-id="05383-115">เต็มเดือน</span><span class="sxs-lookup"><span data-stu-id="05383-115">Full month</span></span>
-   <span data-ttu-id="05383-116">กลางไตรมาส</span><span class="sxs-lookup"><span data-stu-id="05383-116">Mid quarter</span></span>
-   <span data-ttu-id="05383-117">กลางเดือน (วันที่ 1 ของเดือน)</span><span class="sxs-lookup"><span data-stu-id="05383-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="05383-118">กลางเดือน (วันที่ 15 ของเดือน)</span><span class="sxs-lookup"><span data-stu-id="05383-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="05383-119">ครึ่งปี (เริ่มต้นของปี)</span><span class="sxs-lookup"><span data-stu-id="05383-119">Half year (start of year)</span></span>
-   <span data-ttu-id="05383-120">ครึ่งปี (ปีหน้า)</span><span class="sxs-lookup"><span data-stu-id="05383-120">Half year (next year)</span></span>

<span data-ttu-id="05383-121">คุณสามารถเลือกจากวิธีการคิดค่าเสื่อมราคาต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="05383-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="05383-122">อายุการใช้งานแบบเส้นตรง</span><span class="sxs-lookup"><span data-stu-id="05383-122">Straight line service life</span></span>
-   <span data-ttu-id="05383-123">ยอดดุลที่ลดลง</span><span class="sxs-lookup"><span data-stu-id="05383-123">Reducing balance</span></span>
-   <span data-ttu-id="05383-124">ธรรมดา</span><span class="sxs-lookup"><span data-stu-id="05383-124">Manual</span></span>
-   <span data-ttu-id="05383-125">ตัวคูณ</span><span class="sxs-lookup"><span data-stu-id="05383-125">Factor</span></span>
-   <span data-ttu-id="05383-126">ปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="05383-126">Consumption</span></span>
-   <span data-ttu-id="05383-127">อายุการใช้งานคงเหลือแบบเส้นตรง</span><span class="sxs-lookup"><span data-stu-id="05383-127">Straight line life remaining</span></span>
-   <span data-ttu-id="05383-128">ยอดดุลที่ลดลง 200%</span><span class="sxs-lookup"><span data-stu-id="05383-128">200% reducing balance</span></span>
-   <span data-ttu-id="05383-129">ยอดดุลที่ลดลง 175%</span><span class="sxs-lookup"><span data-stu-id="05383-129">175% reducing balance</span></span>
-   <span data-ttu-id="05383-130">ยอดดุลที่ลดลง 150%</span><span class="sxs-lookup"><span data-stu-id="05383-130">150% reducing balance</span></span>
-   <span data-ttu-id="05383-131">ยอดดุลที่ลดลง 125%</span><span class="sxs-lookup"><span data-stu-id="05383-131">125% reducing balance</span></span>

 



<a name="see-also"></a><span data-ttu-id="05383-132">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="05383-132">See also</span></span>
--------

[<span data-ttu-id="05383-133">ค่าเสื่อมราคาของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="05383-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="05383-134">การคิดค่าเสื่อมราคาตามอายุการใช้งานแบบเส้นตรง</span><span class="sxs-lookup"><span data-stu-id="05383-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="05383-135">การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง</span><span class="sxs-lookup"><span data-stu-id="05383-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="05383-136">การคิดค่าเสื่อมราคาด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="05383-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="05383-137">การคิดค่าเสื่อมราคาตามอัตรา</span><span class="sxs-lookup"><span data-stu-id="05383-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="05383-138">การคิดค่าเสื่อมราคาตามปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="05383-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="05383-139">การคิดค่าเสื่อมราคาตามอายุการใช้งานคงเหลือแบบเส้นตรง</span><span class="sxs-lookup"><span data-stu-id="05383-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="05383-140">การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 125%</span><span class="sxs-lookup"><span data-stu-id="05383-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="05383-141">ค่าเสื่อมราคายอดดุลที่ลดลง 150%</span><span class="sxs-lookup"><span data-stu-id="05383-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="05383-142">การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 175%</span><span class="sxs-lookup"><span data-stu-id="05383-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="05383-143">การคิดค่าเสื่อมราคาด้วยยอดดุลที่ลดลง 200%</span><span class="sxs-lookup"><span data-stu-id="05383-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)




