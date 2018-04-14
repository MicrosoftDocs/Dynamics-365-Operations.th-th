--- 
title: "ตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับและต้นแบบอุปกรณ์เสริม"
description: "ขั้นตอนนี้แสดงวิธีการสร้างต้นแบบอุปกรณ์เสริมสำหรับฮับ และใช้ต้นแบบนั้นเพื่อสร้างค่าธรรมเนียมอุปกรณ์เสริมของฮับ "
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6d09e32c9e2c41c49e376320d507593849f68cb0
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="74f5f-103">ตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับและต้นแบบอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="74f5f-103">Set up hub accessorial charges and accessorial masters</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74f5f-104">ขั้นตอนนี้แสดงวิธีการสร้างต้นแบบอุปกรณ์เสริมสำหรับฮับ และใช้ต้นแบบนั้นเพื่อสร้างค่าธรรมเนียมอุปกรณ์เสริมของฮับ </span><span class="sxs-lookup"><span data-stu-id="74f5f-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="74f5f-105">กระบวนงานดังกล่าวใช้ชุดข้อมูล USMF</span><span class="sxs-lookup"><span data-stu-id="74f5f-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="74f5f-106">โดยทั่วไปผู้ประสานงานขนส่งจะเป็นผู้ตั้งค่านี้</span><span class="sxs-lookup"><span data-stu-id="74f5f-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="74f5f-107">ตั้งค่าต้นแบบฮับ</span><span class="sxs-lookup"><span data-stu-id="74f5f-107">Set up a hub master</span></span>
1. <span data-ttu-id="74f5f-108">ไปที่การจัดการการขนส่ง > การตั้งค่า > การจัดอันดับ > ต้นแบบอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="74f5f-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="74f5f-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="74f5f-109">Click New.</span></span>
3. <span data-ttu-id="74f5f-110">ในฟิลด์ต้นแบบอุปกรณ์เสริม ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="74f5f-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="74f5f-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="74f5f-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="74f5f-112">ในฟิลด์ชนิดอุปกรณ์เสริม ให้เลือก 'ฮับ'</span><span class="sxs-lookup"><span data-stu-id="74f5f-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="74f5f-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="74f5f-113">Click Save.</span></span>
7. <span data-ttu-id="74f5f-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="74f5f-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="74f5f-115">ตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับ</span><span class="sxs-lookup"><span data-stu-id="74f5f-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="74f5f-116">ไปที่การจัดการการขนส่ง > ตั้งค่า > การจัดอันดับ > ค่าธรรมเนียมอุปกรณ์เสริมของฮับ</span><span class="sxs-lookup"><span data-stu-id="74f5f-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="74f5f-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="74f5f-117">Click New.</span></span>
3. <span data-ttu-id="74f5f-118">ในฟิลด์ ID อุปกรณ์เสริมของฮับ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="74f5f-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="74f5f-119">ในฟิลด์ฮับ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="74f5f-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="74f5f-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="74f5f-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="74f5f-121">ในฟิลด์ตำแหน่งฮับ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="74f5f-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="74f5f-122">คุณสามารถสร้างค่าธรรมเนียมเป็นทั้งเบิกหรือส่ง </span><span class="sxs-lookup"><span data-stu-id="74f5f-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="74f5f-123">ค่าธรรมเนียมจะนำมาใช้กับภาคการขนส่งในเส้นทางของคุณโดยขึ้นอยู่กับการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="74f5f-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="74f5f-124">ในฟิลด์ต้นแบบอุปกรณ์เสริม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="74f5f-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="74f5f-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="74f5f-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="74f5f-126">เลือกต้นแบบที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="74f5f-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="74f5f-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="74f5f-127">Click Save.</span></span>
10. <span data-ttu-id="74f5f-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="74f5f-128">Close the page.</span></span>


