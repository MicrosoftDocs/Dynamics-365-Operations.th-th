---
title: ลงทะเบียนการเช็คอินและเช็คเอาท์ของพนักงานขนส่งสำหรับการนัดหมาย
description: 'กระบวนงานนี้แสดงวิธีการลงทะเบียนการเช็คอินและการเช็คเอาท์ของพนักงานขนส่ง '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSDriverLogListPage, TMSDriverCheckIn
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34074a6ad2c929085dc6fd43efa8da620ce18584
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438856"
---
# <a name="register-driver-check-in-and-check-out-for-an-appointment"></a><span data-ttu-id="8aa73-103">ลงทะเบียนการเช็คอินและเช็คเอาท์ของพนักงานขนส่งสำหรับการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="8aa73-103">Register driver check-in and check-out for an appointment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8aa73-104">กระบวนงานนี้แสดงวิธีการลงทะเบียนการเช็คอินและการเช็คเอาท์ของพนักงานขนส่ง ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="8aa73-104">This procedure shows how to register a driver check-in and a driver check-out. This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="8aa73-105">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="8aa73-105">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="8aa73-106">ก่อนจะเริ่ม ต้องมีการตั้งค่าการนัดหมายที่ตั้งค่าสำหรับโหลดเสียก่อน</span><span class="sxs-lookup"><span data-stu-id="8aa73-106">Before you start, there must be an appointment set up for a load.</span></span> <span data-ttu-id="8aa73-107">เมื่อต้องการสร้างการนัดหมาย คุณสามารถรันกระบวนงาน "กำหนดการนัดหมายสำหรับจำนวนงานในศูนย์การผลิต" เป็นข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8aa73-107">To create an appointment, you can run the "Set up an appointment for a load" procedure as a prerequisite.</span></span>


## <a name="select-an-appointment"></a><span data-ttu-id="8aa73-108">เลือกการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="8aa73-108">Select an appointment</span></span>
1. <span data-ttu-id="8aa73-109">ไปที่ การจัดการการขนส่ง > การวางแผน > การจัดกำหนดการนัดหมายที่ท่าสินค้า > การเช็คอินและเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="8aa73-109">Go to Transportation management > Planning > Dock appointment scheduling > Driver check-in and check-out.</span></span>
2. <span data-ttu-id="8aa73-110">เลือกการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="8aa73-110">Select an appointment.</span></span>

## <a name="register-driver-check-in"></a><span data-ttu-id="8aa73-111">ลงทะเบียนการเช็คอินของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="8aa73-111">Register driver check-in</span></span>
1. <span data-ttu-id="8aa73-112">คลิก การเช็คอินของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="8aa73-112">Click Driver check-in.</span></span>
2. <span data-ttu-id="8aa73-113">ในฟิลด์หมายเลขปิดท้าย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8aa73-113">In the Trailer number field, type a value.</span></span>
3. <span data-ttu-id="8aa73-114">ในฟิลด์ชื่อพนักงานขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8aa73-114">In the Driver name field, type a value.</span></span>
4. <span data-ttu-id="8aa73-115">ในฟิลด์ใบอนุญาตพนักงานขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8aa73-115">In the Driver license field, type a value.</span></span>
5. <span data-ttu-id="8aa73-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8aa73-116">Click OK.</span></span>

## <a name="register-driver-check-out"></a><span data-ttu-id="8aa73-117">ลงทะเบียนการเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="8aa73-117">Register driver check-out</span></span>
1. <span data-ttu-id="8aa73-118">คลิก การเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="8aa73-118">Click Driver check-out.</span></span>
2. <span data-ttu-id="8aa73-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8aa73-119">Click OK.</span></span>

