---
title: ตั้งค่าการกำหนดอุปกรณ์เสริม
description: 'ขั้นตอนนี้แสดงวิธีการตั้งค่าการกำหนดอุปกรณ์เสริม '
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAccessorialAssignment
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d7f48da374a0434130f2cf95bf77a126635cd63
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016919"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="dd2e4-103">ตั้งค่าการกำหนดอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="dd2e4-103">Set up accessorial assignments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd2e4-104">ขั้นตอนนี้แสดงวิธีการตั้งค่าการกำหนดอุปกรณ์เสริม </span><span class="sxs-lookup"><span data-stu-id="dd2e4-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="dd2e4-105">โดยทั่วไปการตั้งค่านี้จะถูกดำเนินการโดยผู้ประสานงานการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="dd2e4-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="dd2e4-106">ก่อนที่คุณใช้คำแนะนำนี้ คุณต้องรันคำแนะนำ "การตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับและต้นแบบอุปกรณ์เสริม"</span><span class="sxs-lookup"><span data-stu-id="dd2e4-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="dd2e4-107">ตั้งค่าการกำหนดอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="dd2e4-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="dd2e4-108">ไปที่การจัดการการขนส่ง > การตั้งค่า > การจัดอันดับ >การกำหนดอุปกรณ์เสริม</span><span class="sxs-lookup"><span data-stu-id="dd2e4-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="dd2e4-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="dd2e4-109">Click New.</span></span>
3. <span data-ttu-id="dd2e4-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="dd2e4-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="dd2e4-111">สลับการขยายส่วนของรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="dd2e4-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="dd2e4-112">ในฟิลด์ฮับ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dd2e4-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="dd2e4-113">ในรายการ ให้เลือกฮับที่คุณได้สร้างต้นแบบอุปกรณ์เสริมเมื่อคุณเรียกใช้คู่มือ"ตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับและต้นแบบอุปกรณ์เสริม"</span><span class="sxs-lookup"><span data-stu-id="dd2e4-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="dd2e4-114">ในฟิลด์รหัสอุปกรณ์เสริมฮับ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dd2e4-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="dd2e4-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="dd2e4-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="dd2e4-116">สลับการขยายส่วนเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="dd2e4-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="dd2e4-117">ในฟิลด์เงื่อนไข คุณสามารถเลือกเกณฑ์ที่ถูกต้องว่าเมื่อใดควรใช้ค่าธรรมเนียม โดยขึ้นอยู่กับค่าต่างๆที่กำหนดให้</span><span class="sxs-lookup"><span data-stu-id="dd2e4-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="dd2e4-118">ตั้งค่าตัวเลือกให้เป็น ใช่ เสมอ</span><span class="sxs-lookup"><span data-stu-id="dd2e4-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="dd2e4-119">ในฟิลด์ระดับการกำหนดอุปกรณ์เสริม ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="dd2e4-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="dd2e4-120">สลับการขยายส่วนการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="dd2e4-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="dd2e4-121">ในฟิลด์ชนิดค่าธรรมเนียมอุปกรณ์เสริม ให้เลือก 'Flat'</span><span class="sxs-lookup"><span data-stu-id="dd2e4-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="dd2e4-122">ชนิดของค่าธรรมเนียมอุปกรณ์เสริมกำหนดวิธีคำนวณค่าธรรมเนียมจริง </span><span class="sxs-lookup"><span data-stu-id="dd2e4-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="dd2e4-123">ในตัวอย่างนี้ เป็นค่าธรรมเนียมแบบflat</span><span class="sxs-lookup"><span data-stu-id="dd2e4-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="dd2e4-124">ในฟิลด์ค่าธรรมเนียมอุปกรณ์เสริม ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="dd2e4-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="dd2e4-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="dd2e4-125">Click Save.</span></span>

