---
title: หน้าต่างเวลา
description: คุณสามารถใช้หน้าต่างเวลาเพื่อเพิ่มประสิทธิภาพการจัดกำหนดการของรายการใบสั่งบริการได้
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d79e3d3756b8dc402d6f293437209b2e108be38e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978623"
---
# <a name="time-windows"></a><span data-ttu-id="4c212-103">หน้าต่างเวลา</span><span class="sxs-lookup"><span data-stu-id="4c212-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c212-104">คุณสามารถใช้หน้าต่างเวลาเพื่อเพิ่มประสิทธิภาพการจัดกำหนดการของรายการใบสั่งบริการได้</span><span class="sxs-lookup"><span data-stu-id="4c212-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="4c212-105">คุณสามารถตั้งค่าระบบเพื่อให้สร้างใบสั่งบริการโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="4c212-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="4c212-106">โดยขึ้นอยู่กับเงื่อนไขที่ระบุโดยหน้าต่างเวลา คุณสามารถเชื่อมต่อรายการใบสั่งบริการได้มากที่สุดเท่าที่เป็นไปได้กับใบสั่งบริการที่น้อยที่สุดเท่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="4c212-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="4c212-107">หน้าต่างเวลาระบุว่า รายการใบสั่งบริการสามารถย้ายไปได้จากวันที่ที่คำนวณได้ไกลเพียงใด</span><span class="sxs-lookup"><span data-stu-id="4c212-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="4c212-108">วันที่ที่คำนวณคือ วันที่เมื่อมีการจัดกำหนดการรายการใบสั่งบริการให้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="4c212-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="4c212-109">วันที่จะขึ้นอยู่กับการตั้งค่าของช่วงและรอบระยะเวลาการให้บริการที่คุณกำหนดไว้ในหน้า **สร้างใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="4c212-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="4c212-110">คุณกำหนดหน้าต่างเวลาโดยใช้ค่าในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4c212-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="4c212-111">วิธีการ</span><span class="sxs-lookup"><span data-stu-id="4c212-111">Method</span></span> | <span data-ttu-id="4c212-112">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4c212-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c212-113">สัปดาห์</span><span class="sxs-lookup"><span data-stu-id="4c212-113">Week</span></span>   | <span data-ttu-id="4c212-114">วันที่ที่รายการใบสั่งบริการสามารถถูกย้ายไปยังวันที่เปิดใดๆ ในสัปดาห์เดียวกันกับวันที่ที่คำนวณได้แรกเริ่ม</span><span class="sxs-lookup"><span data-stu-id="4c212-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="4c212-115">เดือน</span><span class="sxs-lookup"><span data-stu-id="4c212-115">Month</span></span>  | <span data-ttu-id="4c212-116">วันที่ที่รายการใบสั่งบริการสามารถถูกย้ายไปยังวันที่เปิดใดๆ ในเดือนเดียวกันกับวันที่ที่คำนวณได้แรกเริ่ม</span><span class="sxs-lookup"><span data-stu-id="4c212-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="4c212-117">ตัวอย่างเช่น วันที่ที่คำนวณได้สำหรับรายการใบสั่งบริการคือ วันที่ 15 กุมภาพันธ์ 2017</span><span class="sxs-lookup"><span data-stu-id="4c212-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="4c212-118">รายการใบสั่งบริการสามารถถูกจัดกำหนดการสำหรับวันทำงานใดๆ ได้ ระหว่างวันที่ 1 กุมภาพันธ์และวันที่ 28 กุมภาพันธ์ 2017</span><span class="sxs-lookup"><span data-stu-id="4c212-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="4c212-119">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="4c212-119">Manual</span></span> | <span data-ttu-id="4c212-120">คุณกำหนดจำนวนวันสูงสุดก่อนหน้าหรือหลังจากวันที่ที่คำนวณได้แรกเริ่ม ซึ่งรายการใบสั่งบริการสามารถถูกย้ายได้</span><span class="sxs-lookup"><span data-stu-id="4c212-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="4c212-121">ถ้าคุณไม่ระบุหน้าต่างเวลาสำหรับรายการข้อตกลงการให้บริการ รายการใบสั่งบริการที่ได้รับมาจากข้อตกลงการให้บริการต้องมีวันที่ที่แน่นอนซึ่งได้ถูกจัดกำหนดการแรกเริ่มให้</span><span class="sxs-lookup"><span data-stu-id="4c212-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c212-122">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="4c212-122">Related topics</span></span>

[<span data-ttu-id="4c212-123">การสร้างหน้าต่างเวลา</span><span class="sxs-lookup"><span data-stu-id="4c212-123">Create time windows</span></span>](create-time-windows.md)

