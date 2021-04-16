---
title: ร่วมมือกับลูกค้าของห่วงโซ่อุปทานภายใน
description: 'กระบวนงานนี้แสดงวิธีการดูใบสั่งที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายระหว่างบริษัท '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e663be2a24df8b208bd3902933259ac281db9f9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841754"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="4c7ce-103">ร่วมมือกับลูกค้าของห่วงโซ่อุปทานภายใน</span><span class="sxs-lookup"><span data-stu-id="4c7ce-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c7ce-104">กระบวนงานนี้แสดงวิธีการดูใบสั่งที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="4c7ce-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="4c7ce-105">บริษัทข้อมูลสาธิตที่ใช้สร้างกระบวนการนี้คือ DEMF</span><span class="sxs-lookup"><span data-stu-id="4c7ce-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="4c7ce-106">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="4c7ce-106">Click Master planning.</span></span>
2. <span data-ttu-id="4c7ce-107">ในฟิลด์แผนงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4c7ce-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="4c7ce-108">ในฟิลด์แผน เลือกแผน 10</span><span class="sxs-lookup"><span data-stu-id="4c7ce-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="4c7ce-109">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="4c7ce-109">Click Run.</span></span>
4. <span data-ttu-id="4c7ce-110">ในฟิลด์จำนวนของเธรด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="4c7ce-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="4c7ce-111">รายการนี้แสดงถึงจำนวนเธรดคู่ขนานที่ใช้สำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="4c7ce-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="4c7ce-112">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="4c7ce-112">Click OK.</span></span>
    * <span data-ttu-id="4c7ce-113">การดำเนินการนี้อาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="4c7ce-113">This may take a while.</span></span>  
6. <span data-ttu-id="4c7ce-114">คลิกความต้องการระหว่างบริษัทที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="4c7ce-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="4c7ce-115">คลิกความต้องการระหว่างบริษัทที่วางแผนไว้ขาออก</span><span class="sxs-lookup"><span data-stu-id="4c7ce-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="4c7ce-116">หน้านี้แสดงภาพรวมของความต้องการที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายห่วงโซ่อุปทานภายใน</span><span class="sxs-lookup"><span data-stu-id="4c7ce-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="4c7ce-117">ขยายส่วนรายละเอียดความต้องการขั้นต้นน้ำ</span><span class="sxs-lookup"><span data-stu-id="4c7ce-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="4c7ce-118">ในส่วนนี้ คุณสามารถดูรายละเอียดเกี่ยวกับวิธีการตอบสนองต่อความต้องการ </span><span class="sxs-lookup"><span data-stu-id="4c7ce-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="4c7ce-119">คุณอาจต้องรอให้มีการดำเนินการการวางแผนหลักในบริษัทจัดหาวัสดุก่อนที่คุณจะสามารถดูรายละเอียดเพิ่มเติมที่นี่</span><span class="sxs-lookup"><span data-stu-id="4c7ce-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]