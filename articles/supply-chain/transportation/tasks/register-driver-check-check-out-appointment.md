--- 
title: "ลงทะเบียนการเช็คอินและเช็คเอาท์ของพนักงานขนส่งสำหรับการนัดหมาย"
description: "กระบวนงานนี้แสดงวิธีการลงทะเบียนการเช็คอินและการเช็คเอาท์ของพนักงานขนส่ง "
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSDriverLogListPage, TMSDriverCheckIn
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 557d4d1942d190760f6a3b3d0e0aca0769f8d385
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="register-driver-check-in-and-check-out-for-an-appointment"></a><span data-ttu-id="aaed6-103">ลงทะเบียนการเช็คอินและเช็คเอาท์ของพนักงานขนส่งสำหรับการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="aaed6-103">Register driver check-in and check-out for an appointment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aaed6-104">กระบวนงานนี้แสดงวิธีการลงทะเบียนการเช็คอินและการเช็คเอาท์ของพนักงานขนส่ง ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="aaed6-104">This procedure shows how to register a driver check-in and a driver check-out. This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="aaed6-105">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="aaed6-105">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="aaed6-106">ก่อนจะเริ่ม ต้องมีการตั้งค่าการนัดหมายที่ตั้งค่าสำหรับโหลดเสียก่อน</span><span class="sxs-lookup"><span data-stu-id="aaed6-106">Before you start, there must be an appointment set up for a load.</span></span> <span data-ttu-id="aaed6-107">เมื่อต้องการสร้างการนัดหมาย คุณสามารถรันกระบวนงาน "กำหนดการนัดหมายสำหรับจำนวนงานในศูนย์การผลิต" เป็นข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="aaed6-107">To create an appointment, you can run the “Set up an appointment for a load” procedure as a prerequisite.</span></span>


## <a name="select-an-appointment"></a><span data-ttu-id="aaed6-108">เลือกการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="aaed6-108">Select an appointment</span></span>
1. <span data-ttu-id="aaed6-109">ไปที่ การจัดการการขนส่ง > การวางแผน > การจัดกำหนดการนัดหมายที่ท่าสินค้า > การเช็คอินและเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="aaed6-109">Go to Transportation management > Planning > Dock appointment scheduling > Driver check-in and check-out.</span></span>
2. <span data-ttu-id="aaed6-110">เลือกการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="aaed6-110">Select an appointment.</span></span>

## <a name="register-driver-check-in"></a><span data-ttu-id="aaed6-111">ลงทะเบียนการเช็คอินของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="aaed6-111">Register driver check-in</span></span>
1. <span data-ttu-id="aaed6-112">คลิก การเช็คอินของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="aaed6-112">Click Driver check-in.</span></span>
2. <span data-ttu-id="aaed6-113">ในฟิลด์หมายเลขปิดท้าย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="aaed6-113">In the Trailer number field, type a value.</span></span>
3. <span data-ttu-id="aaed6-114">ในฟิลด์ชื่อพนักงานขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="aaed6-114">In the Driver name field, type a value.</span></span>
4. <span data-ttu-id="aaed6-115">ในฟิลด์ใบอนุญาตพนักงานขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="aaed6-115">In the Driver license field, type a value.</span></span>
5. <span data-ttu-id="aaed6-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aaed6-116">Click OK.</span></span>

## <a name="register-driver-check-out"></a><span data-ttu-id="aaed6-117">ลงทะเบียนการเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="aaed6-117">Register driver check-out</span></span>
1. <span data-ttu-id="aaed6-118">คลิก การเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="aaed6-118">Click Driver check-out.</span></span>
2. <span data-ttu-id="aaed6-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="aaed6-119">Click OK.</span></span>


