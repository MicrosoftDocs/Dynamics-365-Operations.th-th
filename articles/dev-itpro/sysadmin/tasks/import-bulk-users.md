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
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 339cc1d3bcdc1dc93b796c385d2165f45f8f7ecf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548110"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="ab2cb-103">นำเข้าผู้ใช้จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="ab2cb-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ab2cb-104">กระบวนงานนี้สามารถใช้โดยผู้ดูแลระบบเพื่อนำเข้าจำนวนผู้ใช้ปริมาณมากจาก Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ab2cb-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="ab2cb-105">รันเป็นชุดงาน</span><span class="sxs-lookup"><span data-stu-id="ab2cb-105">Run as a batch job</span></span>
1. <span data-ttu-id="ab2cb-106">ไปที่การดูแลระบบ > ผู้ใช้ > ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ab2cb-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="ab2cb-107">คลิก การนำเข้าชุดงาน</span><span class="sxs-lookup"><span data-stu-id="ab2cb-107">Click Batch import.</span></span>
3. <span data-ttu-id="ab2cb-108">ขยายการดำเนินงานในส่วนเบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="ab2cb-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="ab2cb-109">เลือกใช่ในฟิลด์กระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="ab2cb-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="ab2cb-110">ในฟิลด์คำอธิบายงาน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ab2cb-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="ab2cb-111">ในฟิลด์กลุ่มชุดงาน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ab2cb-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="ab2cb-112">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="ab2cb-112">This is an optional step.</span></span>  
7. <span data-ttu-id="ab2cb-113">เลือก ใช่ ในฟิลด์ส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="ab2cb-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="ab2cb-114">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="ab2cb-114">This is an optional step.</span></span>  
8. <span data-ttu-id="ab2cb-115">เลือก ใช่ ในฟิลด์งานสำคัญ</span><span class="sxs-lookup"><span data-stu-id="ab2cb-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="ab2cb-116">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="ab2cb-116">This is an optional step.</span></span>  
9. <span data-ttu-id="ab2cb-117">ในฟิลด์การตรวจสอบประเภท ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ab2cb-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="ab2cb-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ab2cb-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="ab2cb-119">รันในสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="ab2cb-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="ab2cb-120">คลิก การนำเข้าชุดงาน</span><span class="sxs-lookup"><span data-stu-id="ab2cb-120">Click Batch import.</span></span>
2. <span data-ttu-id="ab2cb-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ab2cb-121">Click OK.</span></span>

