---
title: สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน
description: 'ขั้นตอนนี้แสดงวิธีการยืมสินค้ากับผู้ปฏิบัติงาน และบันทึกการส่งสินค้าคืนของผู้ปฏิบัติงาน '
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPersonLoan, HcmPersonLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbe4313393df5fd716ec3c8c20d505afbe531386
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464849"
---
# <a name="loan-item-to-a-worker"></a><span data-ttu-id="e9386-103">สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="e9386-103">Loan item to a worker</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="e9386-104">ขั้นตอนนี้แสดงวิธีการยืมสินค้ากับผู้ปฏิบัติงาน และบันทึกการส่งสินค้าคืนของผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="e9386-104">This procedure shows how to loan an item to a worker and record the worker returning an item.</span></span> <span data-ttu-id="e9386-105">ผู้ปฏิบัติงานสามารถขอยืมสิ้นค้าผ่านทางหน้าบริการตนเองของพนักงาน </span><span class="sxs-lookup"><span data-stu-id="e9386-105">Workers can also request loan items through their Employee self-service pages.</span></span> <span data-ttu-id="e9386-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="e9386-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="loan-item-to-a-worker"></a><span data-ttu-id="e9386-107">สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="e9386-107">Loan item to a worker</span></span>
1. <span data-ttu-id="e9386-108">ไปที่ฝ่ายทรัพยากรบุคคล > ผู้ปฏิบัติงาน > ให้กู้ยืมสินค้า > อุปกรณ์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="e9386-108">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="e9386-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e9386-109">Click New.</span></span>
3. <span data-ttu-id="e9386-110">ในฟิลด์บุคคล ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e9386-110">In the Person field, enter or select a value.</span></span>
4. <span data-ttu-id="e9386-111">ในฟิลด์สินค้าที่ให้กู้ยืม ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e9386-111">In the Loan item field, enter or select a value.</span></span>
5. <span data-ttu-id="e9386-112">ในฟิลด์การส่งคืนที่วางแผนไว้ ป้อนวันที่ที่พนักงานต้องส่งคืนสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="e9386-112">In the Planned return field, enter the date the employee needs to return the loan item.</span></span>
6. <span data-ttu-id="e9386-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e9386-113">Click Save.</span></span>
7. <span data-ttu-id="e9386-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e9386-114">Close the page.</span></span>

## <a name="return-a-loan-item"></a><span data-ttu-id="e9386-115">ส่งคืนสินค้าที่ให้กู้ยืม</span><span class="sxs-lookup"><span data-stu-id="e9386-115">Return a loan item</span></span>
1. <span data-ttu-id="e9386-116">ไปที่ฝ่ายทรัพยากรบุคคล > ผู้ปฏิบัติงาน > ให้กู้ยืมสินค้า > อุปกรณ์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="e9386-116">Go to Human resources > Workers > Loan items > Loaned equipment.</span></span>
2. <span data-ttu-id="e9386-117">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="e9386-117">Click Edit.</span></span>
3. <span data-ttu-id="e9386-118">ในฟิลด์การส่งคืนจริง ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="e9386-118">In the Actual return field, enter a date.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]