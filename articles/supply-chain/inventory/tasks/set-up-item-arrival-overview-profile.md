---
title: ตั้งค่าโพรไฟล์ภาพรวมของการมาถึงของสินค้า
description: หัวข้อนี้มุ่งเน้นการตั้งค่าของโพรไฟล์ภาพรวมการมาถึง
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49670e4287faf3e50a824a5cbedd83ea7dbb8152
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244362"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="10873-103">ตั้งค่าโพรไฟล์ภาพรวมของการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="10873-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="10873-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="10873-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="10873-105">หัวข้อนี้มุ่งเน้นการตั้งค่าของโพรไฟล์ภาพรวมการมาถึง</span><span class="sxs-lookup"><span data-stu-id="10873-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="10873-106">โพรไฟล์ภาพรวมการมาถึงคือ ชุดของกฎที่จะใช้เมื่อผู้ใช้มีการเปิดหน้าภาพรวมของการมาถึง</span><span class="sxs-lookup"><span data-stu-id="10873-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="10873-107">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="10873-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="10873-108">โดยทั่วไปจะดำเนินการโดยเจ้าหน้าที่รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="10873-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="10873-109">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการสินค้าคงคลัง > การตั้งค่า > การกระจาย > โพรไฟล์ภาพรวมของการมาถึง**</span><span class="sxs-lookup"><span data-stu-id="10873-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="10873-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="10873-110">Select **New**.</span></span> <span data-ttu-id="10873-111">เนื่องจากคุณจะทำงานในคลังสินค้าเดียวกันตลอดเวลาในการถ่ายสินค้าจากการขนส่งเต็มรถบรรทุก คุณควรสร้างโพรไฟล์ภาพรวมการมาถึงของสินค้าเพื่อให้กระบวนการในการลงทะเบียนสินค้าที่ได้รับนั้นง่ายมากยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="10873-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="10873-112">ในฟิลด์ **ชื่อโพรไฟล์ภาพรวมของการมาถึง** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10873-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="10873-113">ในฟิลด์ **แสดงรายการ** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="10873-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="10873-114">เลือกบรรทัดที่จะแสดงสำหรับการรับสินค้าดังนี้</span><span class="sxs-lookup"><span data-stu-id="10873-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="10873-115">**ทั้งหมด** – แสดงรายการทั้งหมด โดยไม่คำนึงถึงสถานะ</span><span class="sxs-lookup"><span data-stu-id="10873-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="10873-116">**อยู่ระหว่างการดำเนินการ** – แสดงรายการสำหรับการรับสินค้าที่ความคืบหน้าเป็นเสร็จสมบูรณ์แล้ว หรือบางส่วน</span><span class="sxs-lookup"><span data-stu-id="10873-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="10873-117">ซึ่งหมายความว่า สำหรับแต่ละรายการ ทั้งการรับสินค้าปริมาณเต็มจำนวนหรือการได้รับบางส่วน ก็ให้มีการลงทะเบียนในสมุดรายวันการมาถึง</span><span class="sxs-lookup"><span data-stu-id="10873-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="10873-118">**ไม่เสร็จสมบูรณ์** – แสดงรายการสำหรับการรับสินค้าที่ความคืบหน้าเป็นไม่มี หรือบางส่วน</span><span class="sxs-lookup"><span data-stu-id="10873-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="10873-119">ยังไม่มีการลงทะเบียนปริมาณไว้หรือมีการลงทะเบียนแล้วบางส่วนในสมุดรายวันการมาถึง</span><span class="sxs-lookup"><span data-stu-id="10873-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="10873-120">ขยายหรือยุบส่วน **ตัวเลือกการมาถึง**</span><span class="sxs-lookup"><span data-stu-id="10873-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="10873-121">ในฟิลด์ **จำนวนวันข้างหน้า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="10873-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="10873-122">ขั้นตอนนี้เป็นการตั้งค่าตัวกรองเพื่อแสดงรายการสินค้าที่คาดว่าจะได้รับภายในอีกสองสามวัน (ขึ้นอยู่กับตัวเลขที่คุณกำหนด)</span><span class="sxs-lookup"><span data-stu-id="10873-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="10873-123">ในฟิลด์ **จำนวนวันย้อนหลัง** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="10873-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="10873-124">ขั้นตอนนี้เป็นการกำหนดตัวกรองเพื่อแสดงรายการสินค้าที่คาดว่าจะได้รับวันก่อนหน้าวันนี้</span><span class="sxs-lookup"><span data-stu-id="10873-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="10873-125">ในฟิลด์ **คลังสินค้า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="10873-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="10873-126">ใช้ตัวกรองคลังสินค้าหนึ่งหรือหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="10873-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="10873-127">ในฟิลด์ **โหมดการจัดส่ง** ให้เลือกค่า</span><span class="sxs-lookup"><span data-stu-id="10873-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="10873-128">ขั้นตอนนี้เป็นการกำหนดตัวกรองเพื่อแสดงเฉพาะรายการสินค้าที่ได้รับ ด้วยวิธีการจัดส่งนี้</span><span class="sxs-lookup"><span data-stu-id="10873-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="10873-129">ในฟิลด์ **ชื่อ** เลือก WHS</span><span class="sxs-lookup"><span data-stu-id="10873-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="10873-130">ในฟิลด์ **คลังสินค้า** เลือกคลังสินค้า 24</span><span class="sxs-lookup"><span data-stu-id="10873-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="10873-131">นี่เป็นคลังสินค้าเริ่มต้นที่จะใช้สำหรับการรับรายการสินค้าที่ลงทะเบียนไว้ซึ่งใช้โพรไฟล์นี้</span><span class="sxs-lookup"><span data-stu-id="10873-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="10873-132">ในฟิลด์ **สถานที่** เลือก **Baydoor**</span><span class="sxs-lookup"><span data-stu-id="10873-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="10873-133">นี่เป็นสถานที่เริ่มต้นที่จะใช้สำหรับการรับรายการสินค้าที่ลงทะเบียนไว้ซึ่งใช้โพรไฟล์นี้</span><span class="sxs-lookup"><span data-stu-id="10873-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="10873-134">ขยายหรือยุบส่วน **รายละเอียดการสอบถามการมาถึง**</span><span class="sxs-lookup"><span data-stu-id="10873-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="10873-135">ในฟิลด์ **ข้อจำกัดเกี่ยวกับไซต์** เลือกไซต์ 2</span><span class="sxs-lookup"><span data-stu-id="10873-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="10873-136">ขั้นตอนนี้เป็นการตั้งค่าตัวกรองเพื่อแสดงเฉพาะรายการสินค้าที่ได้รับ ของไซต์งานนี้</span><span class="sxs-lookup"><span data-stu-id="10873-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="10873-137">ตั้งค่าตัวเลือก **ใบสั่งซื้อ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="10873-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="10873-138">เลือกรายการสินค้าจากใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="10873-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="10873-139">ตั้งค่าตัวเลือก **โอน** ใบสั่ง เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="10873-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="10873-140">เลือกรายการสินค้าจากใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="10873-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="10873-141">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="10873-141">Select **Save**.</span></span>
18. <span data-ttu-id="10873-142">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10873-142">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]