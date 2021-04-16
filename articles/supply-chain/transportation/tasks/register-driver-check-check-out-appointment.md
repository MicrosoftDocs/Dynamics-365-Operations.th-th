---
title: ลงทะเบียนการเช็คอินและเช็คเอาท์ของพนักงานขนส่งสำหรับการนัดหมาย
description: 'กระบวนงานนี้แสดงวิธีการลงทะเบียนการเช็คอินและการเช็คเอาท์ของพนักงานขนส่ง '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSDriverLogListPage, TMSDriverCheckIn
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1f97612f308063edeaca2c31eafa3caa5c42a31
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838501"
---
# <a name="register-driver-check-in-and-check-out-for-an-appointment"></a><span data-ttu-id="9fe2c-103">ลงทะเบียนการเช็คอินและเช็คเอาท์ของพนักงานขนส่งสำหรับการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="9fe2c-103">Register driver check-in and check-out for an appointment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9fe2c-104">กระบวนงานนี้แสดงวิธีการลงทะเบียนการเช็คอินและการเช็คเอาท์ของพนักงานขนส่ง ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe2c-104">This procedure shows how to register a driver check-in and a driver check-out. This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="9fe2c-105">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="9fe2c-105">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="9fe2c-106">ก่อนจะเริ่ม ต้องมีการตั้งค่าการนัดหมายที่ตั้งค่าสำหรับโหลดเสียก่อน</span><span class="sxs-lookup"><span data-stu-id="9fe2c-106">Before you start, there must be an appointment set up for a load.</span></span> <span data-ttu-id="9fe2c-107">เมื่อต้องการสร้างการนัดหมาย คุณสามารถรันกระบวนงาน "กำหนดการนัดหมายสำหรับจำนวนงานในศูนย์การผลิต" เป็นข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9fe2c-107">To create an appointment, you can run the "Set up an appointment for a load" procedure as a prerequisite.</span></span>


## <a name="select-an-appointment"></a><span data-ttu-id="9fe2c-108">เลือกการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="9fe2c-108">Select an appointment</span></span>
1. <span data-ttu-id="9fe2c-109">ไปที่ การจัดการการขนส่ง > การวางแผน > การจัดกำหนดการนัดหมายที่ท่าสินค้า > การเช็คอินและเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe2c-109">Go to Transportation management > Planning > Dock appointment scheduling > Driver check-in and check-out.</span></span>
2. <span data-ttu-id="9fe2c-110">เลือกการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="9fe2c-110">Select an appointment.</span></span>

## <a name="register-driver-check-in"></a><span data-ttu-id="9fe2c-111">ลงทะเบียนการเช็คอินของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe2c-111">Register driver check-in</span></span>
1. <span data-ttu-id="9fe2c-112">คลิก การเช็คอินของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe2c-112">Click Driver check-in.</span></span>
2. <span data-ttu-id="9fe2c-113">ในฟิลด์หมายเลขปิดท้าย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9fe2c-113">In the Trailer number field, type a value.</span></span>
3. <span data-ttu-id="9fe2c-114">ในฟิลด์ชื่อพนักงานขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9fe2c-114">In the Driver name field, type a value.</span></span>
4. <span data-ttu-id="9fe2c-115">ในฟิลด์ใบอนุญาตพนักงานขนส่ง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9fe2c-115">In the Driver license field, type a value.</span></span>
5. <span data-ttu-id="9fe2c-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9fe2c-116">Click OK.</span></span>

## <a name="register-driver-check-out"></a><span data-ttu-id="9fe2c-117">ลงทะเบียนการเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe2c-117">Register driver check-out</span></span>
1. <span data-ttu-id="9fe2c-118">คลิก การเช็คเอาท์ของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="9fe2c-118">Click Driver check-out.</span></span>
2. <span data-ttu-id="9fe2c-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="9fe2c-119">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]