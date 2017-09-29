--- 
title: "ตั้งค่าวิธีการชำระเงินการขนส่ง"
description: "กระบวนงานนี้แสดงวิธีการตั้งค่าวิธีการชำระเงินการขนส่ง "
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8ccd82b3249e99dd2884fb257f3e65261ab64d96
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-transportation-tender"></a><span data-ttu-id="26323-103">ตั้งค่าวิธีการชำระเงินการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="26323-103">Set up a transportation tender</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26323-104">กระบวนงานนี้แสดงวิธีการตั้งค่าวิธีการชำระเงินการขนส่ง </span><span class="sxs-lookup"><span data-stu-id="26323-104">This procedure shows how to set up a transportation tender.</span></span> <span data-ttu-id="26323-105">ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง </span><span class="sxs-lookup"><span data-stu-id="26323-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="26323-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="26323-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-route"></a><span data-ttu-id="26323-107">เลือก กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="26323-107">Select a route</span></span>
1. <span data-ttu-id="26323-108">ไปที่ การจัดการการขนส่ง > การวางแผน > เวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="26323-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="26323-109">ล้างข้อมูลกล่องกาเครื่องหมาย ซ่อนสินค้าที่จัดส่งและที่รับ</span><span class="sxs-lookup"><span data-stu-id="26323-109">Clear the Hide shipped and received check box.</span></span>
3. <span data-ttu-id="26323-110">เลือกบรรทัดที่มีรหัสจำนวนงานในศูนย์การผลิต 00006</span><span class="sxs-lookup"><span data-stu-id="26323-110">Select the line with Load ID 00006.</span></span>
4. <span data-ttu-id="26323-111">คลิก การจัดอันดับและการกำหนดเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="26323-111">Click Rating and routing.</span></span>
5. <span data-ttu-id="26323-112">คลิกกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="26323-112">Click Routes.</span></span>

## <a name="create-the-transportation-tender"></a><span data-ttu-id="26323-113">สร้างวิธีการชำระเงินการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="26323-113">Create the transportation tender</span></span>
1. <span data-ttu-id="26323-114">คลิก วิธีการชำระเงินการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="26323-114">Click Transportation tenders.</span></span>
2. <span data-ttu-id="26323-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="26323-115">Click New.</span></span>
3. <span data-ttu-id="26323-116">ขยายส่วน ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="26323-116">Expand the General section.</span></span>
4. <span data-ttu-id="26323-117">ในฟิลด์อัตราที่ร้องขอ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="26323-117">In the Requested rates field, enter a number.</span></span>
5. <span data-ttu-id="26323-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="26323-118">Click Save.</span></span>
6. <span data-ttu-id="26323-119">คลิก ปรับปรุงสถานะ</span><span class="sxs-lookup"><span data-stu-id="26323-119">Click Update status.</span></span>
7. <span data-ttu-id="26323-120">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="26323-120">Click Submit.</span></span>
8. <span data-ttu-id="26323-121">เลือก กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="26323-121">Select a route.</span></span>


