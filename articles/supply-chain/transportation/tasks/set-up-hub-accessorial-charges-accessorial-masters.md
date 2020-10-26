---
title: ตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับและต้นแบบอุปกรณ์เสริม
description: 'ขั้นตอนนี้แสดงวิธีการสร้างต้นแบบอุปกรณ์เสริมสำหรับฮับ และใช้ต้นแบบนั้นเพื่อสร้างค่าธรรมเนียมอุปกรณ์เสริมของฮับ '
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSHubAccessorial,TMSAccessorialMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82cd18c7109b5a0287ee2eb8b7adf901c97ec7c7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982635"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="d8548-103">ตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับและต้นแบบอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="d8548-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8548-104">ขั้นตอนนี้แสดงวิธีการสร้างต้นแบบอุปกรณ์เสริมสำหรับฮับ และใช้ต้นแบบนั้นเพื่อสร้างค่าธรรมเนียมอุปกรณ์เสริมของฮับ </span><span class="sxs-lookup"><span data-stu-id="d8548-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="d8548-105">กระบวนงานดังกล่าวใช้ชุดข้อมูล USMF</span><span class="sxs-lookup"><span data-stu-id="d8548-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="d8548-106">โดยทั่วไปผู้ประสานงานขนส่งจะเป็นผู้ตั้งค่านี้</span><span class="sxs-lookup"><span data-stu-id="d8548-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="d8548-107">ตั้งค่าต้นแบบฮับ</span><span class="sxs-lookup"><span data-stu-id="d8548-107">Set up a hub master</span></span>
1. <span data-ttu-id="d8548-108">ไปที่การจัดการการขนส่ง > การตั้งค่า > การจัดอันดับ > ต้นแบบอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="d8548-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="d8548-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d8548-109">Click New.</span></span>
3. <span data-ttu-id="d8548-110">ในฟิลด์ต้นแบบอุปกรณ์เสริม ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d8548-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="d8548-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d8548-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d8548-112">ในฟิลด์ชนิดอุปกรณ์เสริม ให้เลือก 'ฮับ'</span><span class="sxs-lookup"><span data-stu-id="d8548-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="d8548-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d8548-113">Click Save.</span></span>
7. <span data-ttu-id="d8548-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d8548-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="d8548-115">ตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับ</span><span class="sxs-lookup"><span data-stu-id="d8548-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="d8548-116">ไปที่การจัดการการขนส่ง > ตั้งค่า > การจัดอันดับ > ค่าธรรมเนียมอุปกรณ์เสริมของฮับ</span><span class="sxs-lookup"><span data-stu-id="d8548-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="d8548-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d8548-117">Click New.</span></span>
3. <span data-ttu-id="d8548-118">ในฟิลด์ ID อุปกรณ์เสริมของฮับ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d8548-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="d8548-119">ในฟิลด์ฮับ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="d8548-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d8548-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d8548-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d8548-121">ในฟิลด์ตำแหน่งฮับ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d8548-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="d8548-122">คุณสามารถสร้างค่าธรรมเนียมเป็นทั้งเบิกหรือส่ง </span><span class="sxs-lookup"><span data-stu-id="d8548-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="d8548-123">ค่าธรรมเนียมจะนำมาใช้กับภาคการขนส่งในเส้นทางของคุณโดยขึ้นอยู่กับการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="d8548-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="d8548-124">ในฟิลด์ต้นแบบอุปกรณ์เสริม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="d8548-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d8548-125">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d8548-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d8548-126">เลือกต้นแบบที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="d8548-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="d8548-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d8548-127">Click Save.</span></span>
10. <span data-ttu-id="d8548-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d8548-128">Close the page.</span></span>

