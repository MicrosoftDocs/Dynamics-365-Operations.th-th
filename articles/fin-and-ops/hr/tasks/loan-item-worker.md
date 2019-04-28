---
title: สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน
description: 'ขั้นตอนนี้แสดงวิธีการยืมสินค้ากับผู้ปฏิบัติงาน และบันทึกการส่งสินค้าคืนของผู้ปฏิบัติงาน '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPersonLoan, HcmPersonLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 000d589ed4c17d9259866daf69a5abe879c61e09
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "858479"
---
# <a name="loan-item-to-a-worker"></a><span data-ttu-id="7231c-103">สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="7231c-103">Loan item to a worker</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7231c-104">ขั้นตอนนี้แสดงวิธีการยืมสินค้ากับผู้ปฏิบัติงาน และบันทึกการส่งสินค้าคืนของผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="7231c-104">This procedure shows how to loan an item to a worker and record the worker returning an item.</span></span> <span data-ttu-id="7231c-105">ผู้ปฏิบัติงานสามารถขอยืมสิ้นค้าผ่านทางหน้าบริการตนเองของพนักงาน </span><span class="sxs-lookup"><span data-stu-id="7231c-105">Workers can also request loan items through their Employee self-service pages.</span></span> <span data-ttu-id="7231c-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="7231c-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="loan-item-to-a-worker"></a><span data-ttu-id="7231c-107">สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="7231c-107">Loan item to a worker</span></span>
1. <span data-ttu-id="7231c-108">ไปที่ฝ่ายทรัพยากรบุคคล > ผู้ปฏิบัติงาน > ให้กู้ยืมสินค้า > อุปกรณ์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="7231c-108">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="7231c-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7231c-109">Click New.</span></span>
3. <span data-ttu-id="7231c-110">ในฟิลด์บุคคล ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7231c-110">In the Person field, enter or select a value.</span></span>
4. <span data-ttu-id="7231c-111">ในฟิลด์สินค้าที่ให้กู้ยืม ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7231c-111">In the Loan item field, enter or select a value.</span></span>
5. <span data-ttu-id="7231c-112">ในฟิลด์การส่งคืนที่วางแผนไว้ ป้อนวันที่ที่พนักงานต้องส่งคืนสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="7231c-112">In the Planned return field, enter the date the employee needs to return the loan item.</span></span>
6. <span data-ttu-id="7231c-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="7231c-113">Click Save.</span></span>
7. <span data-ttu-id="7231c-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7231c-114">Close the page.</span></span>

## <a name="return-a-loan-item"></a><span data-ttu-id="7231c-115">ส่งคืนสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="7231c-115">Return a loan item</span></span>
1. <span data-ttu-id="7231c-116">ไปที่ฝ่ายทรัพยากรบุคคล > ผู้ปฏิบัติงาน > ให้กู้ยืมสินค้า > อุปกรณ์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="7231c-116">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="7231c-117">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="7231c-117">Click Edit.</span></span>
3. <span data-ttu-id="7231c-118">ในฟิลด์การส่งคืนจริง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="7231c-118">In the Actual return field, enter a date.</span></span>

