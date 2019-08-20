---
title: ดูความต้องการระหว่างบริษัทที่วางแผนไว้ขาออก
description: 'กระบวนงานนี้แสดงวิธีการดูใบสั่งที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายระหว่างบริษัท '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c45593fc36763e78ff186aeefdbf168bf168612
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835921"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="8a37b-103">ดูความต้องการระหว่างบริษัทที่วางแผนไว้ขาออก</span><span class="sxs-lookup"><span data-stu-id="8a37b-103">View outbound planned intercompany demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a37b-104">กระบวนงานนี้แสดงวิธีการดูใบสั่งที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายระหว่างบริษัท </span><span class="sxs-lookup"><span data-stu-id="8a37b-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="8a37b-105">บริษัทข้อมูลสาธิตที่ใช้สร้างกระบวนการนี้คือ DEMF</span><span class="sxs-lookup"><span data-stu-id="8a37b-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="8a37b-106">คลิกที่งานการวางแผนหลัก </span><span class="sxs-lookup"><span data-stu-id="8a37b-106">Click Master planning.</span></span>
2. <span data-ttu-id="8a37b-107">ในฟิลด์แผนงาน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8a37b-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="8a37b-108">ในฟิลด์แผน เลือกแผน 10</span><span class="sxs-lookup"><span data-stu-id="8a37b-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="8a37b-109">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="8a37b-109">Click Run.</span></span>
4. <span data-ttu-id="8a37b-110">ในฟิลด์จำนวนของเธรด ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="8a37b-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="8a37b-111">รายการนี้แสดงถึงจำนวนเธรดคู่ขนานที่ใช้สำหรับการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="8a37b-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="8a37b-112">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8a37b-112">Click OK.</span></span>
    * <span data-ttu-id="8a37b-113">การดำเนินการนี้อาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="8a37b-113">This may take a while.</span></span>  
6. <span data-ttu-id="8a37b-114">คลิกความต้องการระหว่างบริษัทที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="8a37b-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="8a37b-115">คลิกความต้องการระหว่างบริษัทที่วางแผนไว้ขาออก</span><span class="sxs-lookup"><span data-stu-id="8a37b-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="8a37b-116">หน้านี้แสดงภาพรวมของความต้องการที่วางแผนไว้ทั้งหมดที่จะดำเนินการโดยผู้จัดจำหน่ายห่วงโซ่อุปทานภายใน</span><span class="sxs-lookup"><span data-stu-id="8a37b-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="8a37b-117">ขยายส่วนรายละเอียดความต้องการขั้นต้นน้ำ</span><span class="sxs-lookup"><span data-stu-id="8a37b-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="8a37b-118">ในส่วนนี้ คุณสามารถดูรายละเอียดเกี่ยวกับวิธีการตอบสนองต่อความต้องการ </span><span class="sxs-lookup"><span data-stu-id="8a37b-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="8a37b-119">คุณอาจต้องรอให้มีการดำเนินการการวางแผนหลักในบริษัทจัดหาวัสดุก่อนที่คุณจะสามารถดูรายละเอียดเพิ่มเติมที่นี่</span><span class="sxs-lookup"><span data-stu-id="8a37b-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

