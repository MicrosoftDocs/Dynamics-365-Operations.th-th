--- 
title: "รายการที่ยืมของผู้ปฏิบัติงาน"
description: "ขั้นตอนนี้แสดงวิธีการยืมสินค้ากับผู้ปฏิบัติงาน และบันทึกการส่งสินค้าคืนของผู้ปฏิบัติงาน "
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 665dd5868b9a731caf9c847b7ca33f039fe083e3
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="loan-items-to-a-worker"></a><span data-ttu-id="c5d49-103">รายการที่ยืมของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c5d49-103">Loan items to a worker</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5d49-104">ขั้นตอนนี้แสดงวิธีการยืมสินค้ากับผู้ปฏิบัติงาน และบันทึกการส่งสินค้าคืนของผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="c5d49-104">This procedure shows how to loan an item to a worker and record the worker returning an item.</span></span> <span data-ttu-id="c5d49-105">ผู้ปฏิบัติงานสามารถขอยืมสิ้นค้าผ่านทางหน้าบริการตนเองของพนักงาน </span><span class="sxs-lookup"><span data-stu-id="c5d49-105">Workers can also request loan items through their Employee self-service pages.</span></span> <span data-ttu-id="c5d49-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c5d49-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="loan-item-to-a-worker"></a><span data-ttu-id="c5d49-107">สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c5d49-107">Loan item to a worker</span></span>
1. <span data-ttu-id="c5d49-108">ไปที่ฝ่ายทรัพยากรบุคคล > ผู้ปฏิบัติงาน > ให้กู้ยืมสินค้า > อุปกรณ์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="c5d49-108">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="c5d49-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c5d49-109">Click New.</span></span>
3. <span data-ttu-id="c5d49-110">ในฟิลด์บุคคล ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c5d49-110">In the Person field, enter or select a value.</span></span>
4. <span data-ttu-id="c5d49-111">ในฟิลด์สินค้าที่ให้กู้ยืม ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c5d49-111">In the Loan item field, enter or select a value.</span></span>
5. <span data-ttu-id="c5d49-112">ในฟิลด์การส่งคืนที่วางแผนไว้ ป้อนวันที่ที่พนักงานต้องส่งคืนสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="c5d49-112">In the Planned return field, enter the date the employee needs to return the loan item.</span></span>
6. <span data-ttu-id="c5d49-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c5d49-113">Click Save.</span></span>
7. <span data-ttu-id="c5d49-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c5d49-114">Close the page.</span></span>

## <a name="return-a-loan-item"></a><span data-ttu-id="c5d49-115">ส่งคืนสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="c5d49-115">Return a loan item</span></span>
1. <span data-ttu-id="c5d49-116">ไปที่ฝ่ายทรัพยากรบุคคล > ผู้ปฏิบัติงาน > ให้กู้ยืมสินค้า > อุปกรณ์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="c5d49-116">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="c5d49-117">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="c5d49-117">Click Edit.</span></span>
3. <span data-ttu-id="c5d49-118">ในฟิลด์การส่งคืนจริง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c5d49-118">In the Actual return field, enter a date.</span></span>


