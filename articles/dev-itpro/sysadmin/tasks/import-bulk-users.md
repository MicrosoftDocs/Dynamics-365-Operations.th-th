--- 
title: "นำเข้าผู้ใช้จำนวนมาก"
description: "ผู้ดูแลระบบใช้กระบวนงานนี้ในการนำเข้าผู้ใช้จำนวนมากจาก Azure Active Directory"
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 046b06f663f2fa4b503bcfff15c9fd7675d6acdd
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="import-users-in-bulk"></a><span data-ttu-id="2a478-103">นำเข้าผู้ใช้จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="2a478-103">Import users in bulk</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a478-104">ผู้ดูแลระบบใช้กระบวนงานนี้ในการนำเข้าผู้ใช้จำนวนมากจาก Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a478-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="2a478-105">รันเป็นชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2a478-105">Run as a batch job</span></span>
1. <span data-ttu-id="2a478-106">ไปที่การดูแลระบบ > ผู้ใช้ > ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2a478-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="2a478-107">คลิก การนำเข้าชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2a478-107">Click Batch import.</span></span>
3. <span data-ttu-id="2a478-108">ขยายการดำเนินงานในส่วนเบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="2a478-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="2a478-109">เลือกใช่ในฟิลด์กระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2a478-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="2a478-110">ในฟิลด์คำอธิบายงาน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="2a478-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="2a478-111">ในฟิลด์กลุ่มชุดงาน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2a478-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="2a478-112">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="2a478-112">This is an optional step.</span></span>  
7. <span data-ttu-id="2a478-113">เลือก ใช่ ในฟิลด์ส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="2a478-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="2a478-114">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="2a478-114">This is an optional step.</span></span>  
8. <span data-ttu-id="2a478-115">เลือก ใช่ ในฟิลด์งานสำคัญ</span><span class="sxs-lookup"><span data-stu-id="2a478-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="2a478-116">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="2a478-116">This is an optional step.</span></span>  
9. <span data-ttu-id="2a478-117">ในฟิลด์การตรวจสอบประเภท ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2a478-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="2a478-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2a478-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="2a478-119">รันในสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="2a478-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="2a478-120">คลิก การนำเข้าชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2a478-120">Click Batch import.</span></span>
2. <span data-ttu-id="2a478-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2a478-121">Click OK.</span></span>


