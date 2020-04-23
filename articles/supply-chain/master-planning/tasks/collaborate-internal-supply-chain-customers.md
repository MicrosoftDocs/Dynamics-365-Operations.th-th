---
title: ร่วมมือกับลูกค้าของห่วงโซ่อุปทานภายใน
description: 'กระบวนงานนี้แสดงวิธีการดูใบสั่งที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายระหว่างบริษัท '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb807a904afaba09d0dc364c06f964c135d3cfb1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208673"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="79954-103">ร่วมมือกับลูกค้าของห่วงโซ่อุปทานภายใน</span><span class="sxs-lookup"><span data-stu-id="79954-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79954-104">กระบวนงานนี้แสดงวิธีการดูใบสั่งที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="79954-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="79954-105">บริษัทข้อมูลสาธิตที่ใช้สร้างกระบวนการนี้คือ DEMF</span><span class="sxs-lookup"><span data-stu-id="79954-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="79954-106">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="79954-106">Click Master planning.</span></span>
2. <span data-ttu-id="79954-107">ในฟิลด์แผนงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="79954-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="79954-108">ในฟิลด์แผน เลือกแผน 10</span><span class="sxs-lookup"><span data-stu-id="79954-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="79954-109">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="79954-109">Click Run.</span></span>
4. <span data-ttu-id="79954-110">ในฟิลด์จำนวนของเธรด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="79954-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="79954-111">รายการนี้แสดงถึงจำนวนเธรดคู่ขนานที่ใช้สำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="79954-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="79954-112">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="79954-112">Click OK.</span></span>
    * <span data-ttu-id="79954-113">การดำเนินการนี้อาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="79954-113">This may take a while.</span></span>  
6. <span data-ttu-id="79954-114">คลิกความต้องการระหว่างบริษัทที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="79954-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="79954-115">คลิกความต้องการระหว่างบริษัทที่วางแผนไว้ขาออก</span><span class="sxs-lookup"><span data-stu-id="79954-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="79954-116">หน้านี้แสดงภาพรวมของความต้องการที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายห่วงโซ่อุปทานภายใน</span><span class="sxs-lookup"><span data-stu-id="79954-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="79954-117">ขยายส่วนรายละเอียดความต้องการขั้นต้นน้ำ</span><span class="sxs-lookup"><span data-stu-id="79954-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="79954-118">ในส่วนนี้ คุณสามารถดูรายละเอียดเกี่ยวกับวิธีการตอบสนองต่อความต้องการ </span><span class="sxs-lookup"><span data-stu-id="79954-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="79954-119">คุณอาจต้องรอให้มีการดำเนินการการวางแผนหลักในบริษัทจัดหาวัสดุก่อนที่คุณจะสามารถดูรายละเอียดเพิ่มเติมที่นี่</span><span class="sxs-lookup"><span data-stu-id="79954-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

