--- 
title: "ร่วมมือกับลูกค้าของห่วงโซ่อุปทานภายใน"
description: "กระบวนงานนี้แสดงวิธีการดูใบสั่งที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายระหว่างบริษัท "
author: roxanadiaconu
manager: AnnBe
ms.date: 10/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2ce545650ee5d6151aa65d6e15b6b7bdcd6550e6
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="176cd-103">ร่วมมือกับลูกค้าของห่วงโซ่อุปทานภายใน</span><span class="sxs-lookup"><span data-stu-id="176cd-103">Collaborate with internal supply chain customers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="176cd-104">กระบวนงานนี้แสดงวิธีการดูใบสั่งที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="176cd-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="176cd-105">บริษัทข้อมูลสาธิตที่ใช้สร้างกระบวนการนี้คือ DEMF</span><span class="sxs-lookup"><span data-stu-id="176cd-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="176cd-106">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="176cd-106">Click Master planning.</span></span>
2. <span data-ttu-id="176cd-107">ในฟิลด์แผนงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="176cd-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="176cd-108">ในฟิลด์แผน เลือกแผน 10</span><span class="sxs-lookup"><span data-stu-id="176cd-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="176cd-109">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="176cd-109">Click Run.</span></span>
4. <span data-ttu-id="176cd-110">ในฟิลด์จำนวนของเธรด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="176cd-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="176cd-111">รายการนี้แสดงถึงจำนวนเธรดคู่ขนานที่ใช้สำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="176cd-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="176cd-112">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="176cd-112">Click OK.</span></span>
    * <span data-ttu-id="176cd-113">การดำเนินการนี้อาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="176cd-113">This may take a while.</span></span>  
6. <span data-ttu-id="176cd-114">คลิกความต้องการระหว่างบริษัทที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="176cd-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="176cd-115">คลิกความต้องการระหว่างบริษัทที่วางแผนไว้ขาออก</span><span class="sxs-lookup"><span data-stu-id="176cd-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="176cd-116">หน้านี้แสดงภาพรวมของความต้องการที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายห่วงโซ่อุปทานภายใน</span><span class="sxs-lookup"><span data-stu-id="176cd-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="176cd-117">ขยายส่วนรายละเอียดความต้องการขั้นต้นน้ำ</span><span class="sxs-lookup"><span data-stu-id="176cd-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="176cd-118">ในส่วนนี้ คุณสามารถดูรายละเอียดเกี่ยวกับวิธีการตอบสนองต่อความต้องการ </span><span class="sxs-lookup"><span data-stu-id="176cd-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="176cd-119">คุณอาจต้องรอให้มีการดำเนินการการวางแผนหลักในบริษัทจัดหาวัสดุก่อนที่คุณจะสามารถดูรายละเอียดเพิ่มเติมที่นี่</span><span class="sxs-lookup"><span data-stu-id="176cd-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  


