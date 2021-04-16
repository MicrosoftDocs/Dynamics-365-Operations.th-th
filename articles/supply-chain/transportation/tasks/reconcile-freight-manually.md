---
title: กระทบยอดการขนส่งด้วยตนเอง
description: 'กระบวนงานนี้แสดงวิธีการกระทบยอดการขนส่งด้วยตนเอง '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a0a5450697a09e5e54e74b35b2576eb6bbd4cdf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838525"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="78d62-103">กระทบยอดการขนส่งด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="78d62-103">Reconcile freight manually</span></span>

<span data-ttu-id="78d62-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="78d62-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="78d62-105">กระบวนงานนี้แสดงวิธีการกระทบยอดการขนส่งด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="78d62-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="78d62-106">ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง </span><span class="sxs-lookup"><span data-stu-id="78d62-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="78d62-107">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="78d62-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="78d62-108">เลือกจำนวนงานในศูนย์การผลิตที่จะกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="78d62-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="78d62-109">ไปที่ การจัดการการขนส่ง > การวางแผน > เวิร์กเบนช์การวางแผนการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="78d62-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="78d62-110">ล้างข้อมูลกล่องกาเครื่องหมาย ซ่อนสินค้าที่จัดส่งและที่รับ</span><span class="sxs-lookup"><span data-stu-id="78d62-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="78d62-111">ในรายการ เลือกจำนวนงานในศูนย์การผลิตที่มีรหัสจำนวนงานในศูนย์การผลิต 00006</span><span class="sxs-lookup"><span data-stu-id="78d62-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="78d62-112">สร้างใบแจ้งหนี้ของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="78d62-112">Create a carrier invoice</span></span>
<span data-ttu-id="78d62-113">หากคุณกระทบยอดการขนส่งด้วยตนเอง และไม่ได้รับใบแจ้งหนี้ของผู้ขนส่งโดยอัตโนมัติ คุณสามารถสร้างใบแจ้งหนี้ตามบิลการขนส่งได้</span><span class="sxs-lookup"><span data-stu-id="78d62-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="78d62-114">คลิก ข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="78d62-114">Click Related information.</span></span>
2. <span data-ttu-id="78d62-115">คลิก รายละเอียดของบิลการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="78d62-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="78d62-116">คลิก สร้างใบแจ้งหนี้บิลค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="78d62-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="78d62-117">ในฟิลด์ใบแจ้งหนี้ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="78d62-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="78d62-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="78d62-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="78d62-119">กระทบยอดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="78d62-119">Reconcile the invoice</span></span>
<span data-ttu-id="78d62-120">คุณจะต้องกระทบยอดใบแจ้งหนี้ของผู้ขนส่งและบิลการขนส่งทีละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="78d62-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="78d62-121">คลิก จับคู่บิลและใบแจ้งหนี้การขนส่ง</span><span class="sxs-lookup"><span data-stu-id="78d62-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="78d62-122">ขยายส่วนรายละเอียดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="78d62-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="78d62-123">ขยายส่วน รายละเอียดบิลการขนส่งที่ไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="78d62-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="78d62-124">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="78d62-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="78d62-125">คลิก จับคู่</span><span class="sxs-lookup"><span data-stu-id="78d62-125">Click Match.</span></span>
6. <span data-ttu-id="78d62-126">ขยายส่วน รายละเอียดบิลการขนส่งที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="78d62-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="78d62-127">ส่งใบแจ้งหนี้เพื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="78d62-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="78d62-128">คลิก ส่งเพื่ออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="78d62-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="78d62-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="78d62-129">Close the page.</span></span>
3. <span data-ttu-id="78d62-130">คลิกกล่องกาเครื่องหมาย ซ่อนรายการที่อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="78d62-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="78d62-131">คลิก สมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="78d62-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="78d62-132">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขสมุดรายวันการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="78d62-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="78d62-133">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="78d62-133">Click Lines.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]