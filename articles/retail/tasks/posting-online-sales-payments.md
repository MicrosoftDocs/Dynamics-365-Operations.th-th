--- 
title: " ลงรายการบัญชีการขายออนไลน์และการชำระเงิน"
description: "กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบสั่งขายและการชำระเงินสำหรับธุรกรรมของร้านค้าออนไลน์ "
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b1ec55edb0799ff141c77575ce53ab0313d9cca9
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="037d3-103"> ลงรายการบัญชีการขายออนไลน์และการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="037d3-103">Post online sales and payments</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="037d3-104">กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบสั่งขายและการชำระเงินสำหรับธุรกรรมของร้านค้าออนไลน์ </span><span class="sxs-lookup"><span data-stu-id="037d3-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="037d3-105">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="037d3-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="037d3-106">ไปยังพื้นที่ทำงานทั้งหมด > การเงินของร้านค้าปลีก </span><span class="sxs-lookup"><span data-stu-id="037d3-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="037d3-107">คลิกซิงโครไนส์ใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="037d3-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="037d3-108">ในฟิลด์ลำดับชั้นขององค์กร ให้เลือก 'ร้านค้าปลีกโดยเรียงตามภูมิภาค'</span><span class="sxs-lookup"><span data-stu-id="037d3-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="037d3-109">เลือกอย่างใดอย่างหนึ่งระหว่างร้านค้าออนไลน์ หรือเลือกโหนด ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า</span><span class="sxs-lookup"><span data-stu-id="037d3-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="037d3-110">คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก </span><span class="sxs-lookup"><span data-stu-id="037d3-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="037d3-111">คลิกรันในแท็บเบื้องหลัง </span><span class="sxs-lookup"><span data-stu-id="037d3-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="037d3-112">เลือกหรือไม่เลือกกล่องกาเครื่องหมายการประมวลผลชุดงาน</span><span class="sxs-lookup"><span data-stu-id="037d3-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="037d3-113">คลิกการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="037d3-113">Click Recurrence.</span></span>
7. <span data-ttu-id="037d3-114">เลือกตัวเลือกไม่มีวันที่สิ้นสุด </span><span class="sxs-lookup"><span data-stu-id="037d3-114">Select the No end date option.</span></span>
8. <span data-ttu-id="037d3-115">ในฟิลด์ตรวจนับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="037d3-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="037d3-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="037d3-116">Click OK.</span></span>
10. <span data-ttu-id="037d3-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="037d3-117">Click OK.</span></span>


