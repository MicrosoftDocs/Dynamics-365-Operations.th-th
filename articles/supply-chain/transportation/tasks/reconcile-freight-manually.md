--- 
title: "กระทบยอดการขนส่งด้วยตนเอง"
description: "กระบวนงานนี้แสดงวิธีการกระทบยอดการขนส่งด้วยตนเอง "
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="f1397-103">กระทบยอดการขนส่งด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="f1397-103">Reconcile freight manually</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1397-104">กระบวนงานนี้แสดงวิธีการกระทบยอดการขนส่งด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="f1397-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="f1397-105">ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง </span><span class="sxs-lookup"><span data-stu-id="f1397-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="f1397-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="f1397-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="f1397-107">เลือกจำนวนงานในศูนย์การผลิตที่จะกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="f1397-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="f1397-108">ไปที่ การจัดการการขนส่ง > การวางแผน > เวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="f1397-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="f1397-109">ล้างข้อมูลกล่องกาเครื่องหมาย ซ่อนสินค้าที่จัดส่งและที่รับ</span><span class="sxs-lookup"><span data-stu-id="f1397-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="f1397-110">ในรายการ เลือกจำนวนงานในศูนย์การผลิตที่มีรหัสจำนวนงานในศูนย์การผลิต 00006</span><span class="sxs-lookup"><span data-stu-id="f1397-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="f1397-111">สร้างใบแจ้งหนี้ของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="f1397-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="f1397-112">เมื่อคุณกระทบยอดการขนส่งด้วยตนเองและไม่ได้รับใบแจ้งหนี้ของผู้ขนส่งโดยอัตโนมัติ คุณสามารถสร้างใบแจ้งหนี้ตามบิลการขนส่งได้</span><span class="sxs-lookup"><span data-stu-id="f1397-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="f1397-113">คลิก ข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f1397-113">Click Related information.</span></span>
2. <span data-ttu-id="f1397-114">คลิก รายละเอียดของบิลการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="f1397-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="f1397-115">คลิก สร้างใบแจ้งหนี้บิลค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="f1397-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="f1397-116">ในฟิลด์ใบแจ้งหนี้ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f1397-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="f1397-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f1397-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="f1397-118">กระทบยอดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f1397-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="f1397-119">คุณจะต้องกระทบยอดใบแจ้งหนี้ของผู้ขนส่งและบิลการขนส่งทีละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f1397-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="f1397-120">คลิก จับคู่บิลและใบแจ้งหนี้การขนส่ง</span><span class="sxs-lookup"><span data-stu-id="f1397-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="f1397-121">ขยายส่วนรายละเอียดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="f1397-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="f1397-122">ขยายส่วน รายละเอียดบิลการขนส่งที่ไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="f1397-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="f1397-123">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f1397-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="f1397-124">คลิก จับคู่</span><span class="sxs-lookup"><span data-stu-id="f1397-124">Click Match.</span></span>
6. <span data-ttu-id="f1397-125">ขยายส่วน รายละเอียดบิลการขนส่งที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="f1397-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="f1397-126">ส่งใบแจ้งหนี้เพื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="f1397-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="f1397-127">คลิก ส่งเพื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="f1397-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="f1397-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f1397-128">Close the page.</span></span>
3. <span data-ttu-id="f1397-129">คลิกกล่องกาเครื่องหมาย ซ่อนรายการที่อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="f1397-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="f1397-130">คลิก สมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="f1397-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="f1397-131">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขสมุดรายวันการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="f1397-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="f1397-132">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="f1397-132">Click Lines.</span></span>


