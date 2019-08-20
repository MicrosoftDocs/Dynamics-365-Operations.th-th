---
title: สร้างชนิดการร้องขอ และเกณฑ์การให้คะแนนสำหรับ RFQ
description: 'คำแนะนำนี้แสดงวิธีการสร้างชนิดการร้องขอ และการเชื่อมโยงกับวิธีการให้คะแนน '
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a3e0d00d674af913953d7fd01183b0289c20d3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844130"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="7a2bc-103">สร้างชนิดการร้องขอ และเกณฑ์การให้คะแนนสำหรับ RFQ</span><span class="sxs-lookup"><span data-stu-id="7a2bc-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a2bc-104">คำแนะนำนี้แสดงวิธีการสร้างชนิดการร้องขอ และการเชื่อมโยงกับวิธีการให้คะแนน </span><span class="sxs-lookup"><span data-stu-id="7a2bc-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="7a2bc-105">นอกจากนี้ยังแสดงวิธีการใช้ชนิดการร้องขอในคำขอใบเสนอราคา (RFQ) ซึ่งจะกำหนดวิธีการให้คะแนนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7a2bc-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="7a2bc-106">โดยทั่วไปงานเหล่านี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7a2bc-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="7a2bc-107">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="7a2bc-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="7a2bc-108">คุณต้องมีวิธีการให้คะแนนที่พร้อมใช้ก่อนที่จะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7a2bc-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="7a2bc-109">สร้างชนิดการร้องขอ</span><span class="sxs-lookup"><span data-stu-id="7a2bc-109">Create a solicitation type</span></span>
1. <span data-ttu-id="7a2bc-110">ไปที่การจัดซื้อและการจัดหา > การตั้งค่า > คำขอใบเสนอราคา > ชนิดการร้องขอ</span><span class="sxs-lookup"><span data-stu-id="7a2bc-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="7a2bc-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a2bc-111">Click New.</span></span>
3. <span data-ttu-id="7a2bc-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="7a2bc-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7a2bc-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7a2bc-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7a2bc-114">ในฟิลด์วิธีการให้คะแนน เลือกวิธีการให้คะแนนที่คุณต้องการใช้สำหรับชนิดการร้องขอนี้</span><span class="sxs-lookup"><span data-stu-id="7a2bc-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="7a2bc-115">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7a2bc-115">Click Save.</span></span>
7. <span data-ttu-id="7a2bc-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a2bc-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="7a2bc-117">ใช้ชนิดของการร้องขอ</span><span class="sxs-lookup"><span data-stu-id="7a2bc-117">Use the solicitation type</span></span>
1. <span data-ttu-id="7a2bc-118">ไปที่การจัดซื้อและการจัดหา > คำขอใบเสนอราคา > คำขอใบเสนอราคาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7a2bc-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="7a2bc-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7a2bc-119">Click New.</span></span>
3. <span data-ttu-id="7a2bc-120">ในฟิลด์ชนิดการร้องขอ เลือกชนิดการร้องขอที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="7a2bc-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="7a2bc-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7a2bc-121">Click OK.</span></span>
5. <span data-ttu-id="7a2bc-122">คลิกเกณฑ์การให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="7a2bc-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="7a2bc-123">เกณฑ์การให้คะแนนที่แสดงมาจากวิธีการให้คะแนนที่คุณเชื่อมโยงกับชนิดการร้องขอ </span><span class="sxs-lookup"><span data-stu-id="7a2bc-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="7a2bc-124">คุณสามารถเลือกที่จะเพิ่ม หรือลบเงื่อนไขบนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7a2bc-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="7a2bc-125">และยังสามารถเพิ่มเงื่อนไขใหม่ได้โดยการคัดลอกออกจากวิธีการให้คะแนนอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="7a2bc-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="7a2bc-126">คลิกคัดลอกเกณฑ์</span><span class="sxs-lookup"><span data-stu-id="7a2bc-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="7a2bc-127">ในฟิลด์วิธีการให้คะแนน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7a2bc-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="7a2bc-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="7a2bc-128">Click OK.</span></span>
9. <span data-ttu-id="7a2bc-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7a2bc-129">Close the page.</span></span>

