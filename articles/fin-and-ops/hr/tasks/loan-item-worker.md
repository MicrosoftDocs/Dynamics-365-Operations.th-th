---
title: สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน
description: 'ขั้นตอนนี้แสดงวิธีการยืมสินค้ากับผู้ปฏิบัติงาน และบันทึกการส่งสินค้าคืนของผู้ปฏิบัติงาน '
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPersonLoan, HcmPersonLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9041a24a7197c350a38339408197f643f2b9b6dd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "332230"
---
# <a name="loan-item-to-a-worker"></a><span data-ttu-id="c38ce-103">สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c38ce-103">Loan item to a worker</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c38ce-104">ขั้นตอนนี้แสดงวิธีการยืมสินค้ากับผู้ปฏิบัติงาน และบันทึกการส่งสินค้าคืนของผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="c38ce-104">This procedure shows how to loan an item to a worker and record the worker returning an item.</span></span> <span data-ttu-id="c38ce-105">ผู้ปฏิบัติงานสามารถขอยืมสิ้นค้าผ่านทางหน้าบริการตนเองของพนักงาน </span><span class="sxs-lookup"><span data-stu-id="c38ce-105">Workers can also request loan items through their Employee self-service pages.</span></span> <span data-ttu-id="c38ce-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="c38ce-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="loan-item-to-a-worker"></a><span data-ttu-id="c38ce-107">สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c38ce-107">Loan item to a worker</span></span>
1. <span data-ttu-id="c38ce-108">ไปที่ฝ่ายทรัพยากรบุคคล > ผู้ปฏิบัติงาน > ให้กู้ยืมสินค้า > อุปกรณ์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="c38ce-108">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="c38ce-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c38ce-109">Click New.</span></span>
3. <span data-ttu-id="c38ce-110">ในฟิลด์บุคคล ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c38ce-110">In the Person field, enter or select a value.</span></span>
4. <span data-ttu-id="c38ce-111">ในฟิลด์สินค้าที่ให้กู้ยืม ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c38ce-111">In the Loan item field, enter or select a value.</span></span>
5. <span data-ttu-id="c38ce-112">ในฟิลด์การส่งคืนที่วางแผนไว้ ป้อนวันที่ที่พนักงานต้องส่งคืนสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="c38ce-112">In the Planned return field, enter the date the employee needs to return the loan item.</span></span>
6. <span data-ttu-id="c38ce-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c38ce-113">Click Save.</span></span>
7. <span data-ttu-id="c38ce-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c38ce-114">Close the page.</span></span>

## <a name="return-a-loan-item"></a><span data-ttu-id="c38ce-115">ส่งคืนสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="c38ce-115">Return a loan item</span></span>
1. <span data-ttu-id="c38ce-116">ไปที่ฝ่ายทรัพยากรบุคคล > ผู้ปฏิบัติงาน > ให้กู้ยืมสินค้า > อุปกรณ์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="c38ce-116">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="c38ce-117">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="c38ce-117">Click Edit.</span></span>
3. <span data-ttu-id="c38ce-118">ในฟิลด์การส่งคืนจริง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c38ce-118">In the Actual return field, enter a date.</span></span>

