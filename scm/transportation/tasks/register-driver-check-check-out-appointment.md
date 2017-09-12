--- 
title: "ลงทะเบียนการเช็คอินและเช็คเอาท์ของพนักงานขนส่งสำหรับการนัดหมาย"
description: "กระบวนงานนี้แสดงวิธีการลงทะเบียนการเช็คอินและการเช็คเอาท์ของพนักงานขนส่ง "
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 37b060da7a798379d845ff11be5fb220183c888f
ms.contentlocale: th-th
ms.lasthandoff: 07/27/2017

---
# <a name="register-driver-check-in-and-check-out-for-an-appointment"></a><span data-ttu-id="a95ae-103">ลงทะเบียนการเช็คอินและเช็คเอาท์ของพนักงานขนส่งสำหรับการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="a95ae-103">Register driver check-in and check-out for an appointment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a95ae-104">กระบวนงานนี้แสดงวิธีการลงทะเบียนการเช็คอินและการเช็คเอาท์ของพนักงานขนส่ง </span><span class="sxs-lookup"><span data-stu-id="a95ae-104">This procedure shows how to register a driver check-in and a driver check-out.</span></span> <span data-ttu-id="a95ae-105">โดยทั่วไปการตั้งค่านี้จะถูกดำเนินการโดยผู้ประสานงานการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a95ae-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="a95ae-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="a95ae-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="a95ae-107">ก่อนจะเริ่ม ต้องมีการตั้งค่าการนัดหมายที่ตั้งค่าสำหรับโหลดเสียก่อน</span><span class="sxs-lookup"><span data-stu-id="a95ae-107">Before you start, there must be an appointment set up for a load.</span></span> <span data-ttu-id="a95ae-108">เมื่อต้องการสร้างการนัดหมาย คุณสามารถรันกระบวนงาน "กำหนดการนัดหมายสำหรับจำนวนงานในศูนย์การผลิต" เป็นข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="a95ae-108">To create an appointment, you can run the “Set up an appointment for a load” procedure as a prerequisite.</span></span>


## <a name="select-an-appointment"></a><span data-ttu-id="a95ae-109">เลือกการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="a95ae-109">Select an appointment</span></span>
1. <span data-ttu-id="a95ae-110">ไปที่ การจัดการการขนส่ง > การวางแผน > การจัดกำหนดการนัดหมายที่ท่าสินค้า > การเช็คอินและเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a95ae-110">Go to Transportation management > Planning > Dock appointment scheduling > Driver check-in and check-out.</span></span>
2. <span data-ttu-id="a95ae-111">เลือกการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="a95ae-111">Select an appointment.</span></span>

## <a name="register-driver-check-in"></a><span data-ttu-id="a95ae-112">ลงทะเบียนการเช็คอินของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a95ae-112">Register driver check-in</span></span>
1. <span data-ttu-id="a95ae-113">คลิก การเช็คอินของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a95ae-113">Click Driver check-in.</span></span>
2. <span data-ttu-id="a95ae-114">ในฟิลด์หมายเลขปิดท้าย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a95ae-114">In the Trailer number field, type a value.</span></span>
3. <span data-ttu-id="a95ae-115">ในฟิลด์ชื่อพนักงานขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a95ae-115">In the Driver name field, type a value.</span></span>
4. <span data-ttu-id="a95ae-116">ในฟิลด์ใบอนุญาตพนักงานขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a95ae-116">In the Driver license field, type a value.</span></span>
5. <span data-ttu-id="a95ae-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="a95ae-117">Click OK.</span></span>

## <a name="register-driver-check-out"></a><span data-ttu-id="a95ae-118">ลงทะเบียนการเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a95ae-118">Register driver check-out</span></span>
1. <span data-ttu-id="a95ae-119">คลิก การเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="a95ae-119">Click Driver check-out.</span></span>
2. <span data-ttu-id="a95ae-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="a95ae-120">Click OK.</span></span>


