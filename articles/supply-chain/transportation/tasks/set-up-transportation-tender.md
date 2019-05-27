---
title: ตั้งค่าวิธีการชำระเงินการขนส่ง
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าวิธีการชำระเงินการขนส่ง '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSRouteWorkbench, TMSTransportationTender
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3429e242be5854c2e30802c633fac0d702a2e024
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573176"
---
# <a name="set-up-a-transportation-tender"></a><span data-ttu-id="63868-103">ตั้งค่าวิธีการชำระเงินการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="63868-103">Set up a transportation tender</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63868-104">กระบวนงานนี้แสดงวิธีการตั้งค่าวิธีการชำระเงินการขนส่ง </span><span class="sxs-lookup"><span data-stu-id="63868-104">This procedure shows how to set up a transportation tender.</span></span> <span data-ttu-id="63868-105">ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง </span><span class="sxs-lookup"><span data-stu-id="63868-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="63868-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="63868-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-route"></a><span data-ttu-id="63868-107">เลือก กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="63868-107">Select a route</span></span>
1. <span data-ttu-id="63868-108">ไปที่ การจัดการการขนส่ง > การวางแผน > เวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="63868-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="63868-109">ล้างข้อมูลกล่องกาเครื่องหมาย ซ่อนสินค้าที่จัดส่งและที่รับ</span><span class="sxs-lookup"><span data-stu-id="63868-109">Clear the Hide shipped and received check box.</span></span>
3. <span data-ttu-id="63868-110">เลือกบรรทัดที่มีรหัสจำนวนงานในศูนย์การผลิต 00006</span><span class="sxs-lookup"><span data-stu-id="63868-110">Select the line with Load ID 00006.</span></span>
4. <span data-ttu-id="63868-111">คลิก การจัดอันดับและการกำหนดเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="63868-111">Click Rating and routing.</span></span>
5. <span data-ttu-id="63868-112">คลิกกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="63868-112">Click Routes.</span></span>

## <a name="create-the-transportation-tender"></a><span data-ttu-id="63868-113">สร้างวิธีการชำระเงินการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="63868-113">Create the transportation tender</span></span>
1. <span data-ttu-id="63868-114">คลิก วิธีการชำระเงินการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="63868-114">Click Transportation tenders.</span></span>
2. <span data-ttu-id="63868-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="63868-115">Click New.</span></span>
3. <span data-ttu-id="63868-116">ขยายส่วน ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="63868-116">Expand the General section.</span></span>
4. <span data-ttu-id="63868-117">ในฟิลด์อัตราที่ร้องขอ ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="63868-117">In the Requested rates field, enter a number.</span></span>
5. <span data-ttu-id="63868-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="63868-118">Click Save.</span></span>
6. <span data-ttu-id="63868-119">คลิก ปรับปรุงสถานะ</span><span class="sxs-lookup"><span data-stu-id="63868-119">Click Update status.</span></span>
7. <span data-ttu-id="63868-120">คลิก ส่ง </span><span class="sxs-lookup"><span data-stu-id="63868-120">Click Submit.</span></span>
8. <span data-ttu-id="63868-121">เลือก กระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="63868-121">Select a route.</span></span>

