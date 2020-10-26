---
title: นำเข้าผู้ใช้จำนวนมาก
description: กระบวนงานนี้สามารถใช้โดยผู้ดูแลระบบเพื่อนำเข้าจำนวนผู้ใช้ปริมาณมากจาก Azure Active Directory
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa86d408727ecf2127308070fda592ff6a1fccf4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982465"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="2e5f2-103">นำเข้าผู้ใช้จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="2e5f2-103">Import users in bulk</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e5f2-104">กระบวนงานนี้สามารถใช้โดยผู้ดูแลระบบเพื่อนำเข้าจำนวนผู้ใช้ปริมาณมากจาก Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2e5f2-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="2e5f2-105">รันเป็นชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2e5f2-105">Run as a batch job</span></span>
1. <span data-ttu-id="2e5f2-106">ไปที่การดูแลระบบ > ผู้ใช้ > ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2e5f2-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="2e5f2-107">คลิก การนำเข้าชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2e5f2-107">Click Batch import.</span></span>
3. <span data-ttu-id="2e5f2-108">ขยายการดำเนินงานในส่วนเบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="2e5f2-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="2e5f2-109">เลือกใช่ในฟิลด์กระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2e5f2-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="2e5f2-110">ในฟิลด์คำอธิบายงาน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2e5f2-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="2e5f2-111">ในฟิลด์กลุ่มชุดงาน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2e5f2-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="2e5f2-112">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="2e5f2-112">This is an optional step.</span></span>  
7. <span data-ttu-id="2e5f2-113">เลือก ใช่ ในฟิลด์ส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="2e5f2-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="2e5f2-114">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="2e5f2-114">This is an optional step.</span></span>  
8. <span data-ttu-id="2e5f2-115">เลือก ใช่ ในฟิลด์งานสำคัญ</span><span class="sxs-lookup"><span data-stu-id="2e5f2-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="2e5f2-116">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="2e5f2-116">This is an optional step.</span></span>  
9. <span data-ttu-id="2e5f2-117">ในฟิลด์การตรวจสอบประเภท ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2e5f2-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="2e5f2-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2e5f2-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="2e5f2-119">รันในสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="2e5f2-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="2e5f2-120">คลิก การนำเข้าชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2e5f2-120">Click Batch import.</span></span>
2. <span data-ttu-id="2e5f2-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2e5f2-121">Click OK.</span></span>

