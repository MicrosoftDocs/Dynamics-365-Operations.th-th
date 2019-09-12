---
title: สร้างและรับสินทรัพย์จากบัญชีเจ้าหนี้
description: 'คู่มือของงานนี้จะนำไปสุ่การสร้างและการซื้อสินทรัพย์ของสินทรัพย์ถาวรด้วยกระบวนการซื้อ '
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 025639e6e5bdc6b95e9c496f11f29ed8ec8d388c
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914687"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="9df79-103">สร้างและรับสินทรัพย์จากบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="9df79-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9df79-104">คู่มือของงานนี้จะนำไปสุ่การสร้างและการซื้อสินทรัพย์ของสินทรัพย์ถาวรด้วยกระบวนการซื้อ </span><span class="sxs-lookup"><span data-stu-id="9df79-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="9df79-105">มีการใช้นักบัญชีและเสมียนบัญชีเจ้าหนี้ดูแลและบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="9df79-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="9df79-106">ตั้งค่าพารามิเตอร์สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="9df79-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="9df79-107">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > สินทรัพย์ถาวร > การตั้งค่า > พารามิเตอร์สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="9df79-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="9df79-108">ขยาย fastTab **ใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="9df79-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="9df79-109">ตรวจสอบกล่องกาเครื่องหมาย **อนุญาตให้มีการซื้อสินทรัพย์จากการซื้อ**</span><span class="sxs-lookup"><span data-stu-id="9df79-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="9df79-110">กล่องกล่องกาเครื่องหมาย **สร้างสินทรัพย์ในระหว่างใบรับผลิตภัณฑ์หรือการลงรายการบัญชีใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="9df79-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="9df79-111">สร้างใบแจ้งหนี้ของผู้จัดจำหน่ายใหม่</span><span class="sxs-lookup"><span data-stu-id="9df79-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="9df79-112">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > บัญชีเจ้าหนี้ >พื้นที่ทำงาน > รายการใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9df79-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="9df79-113">คลิก **ใบแจ้งหนี้ของผู้จัดจำหน่ายใหม่**</span><span class="sxs-lookup"><span data-stu-id="9df79-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="9df79-114">ในฟิลด์ **บัญชีใบแจ้งหนี้** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="9df79-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9df79-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9df79-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9df79-116">ในฟิลด์ **หมายเลข** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9df79-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="9df79-117">ในฟิลด์ **วันที่ลงรายการบัญชี** ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="9df79-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="9df79-118">คลิก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="9df79-118">Click **Add line**.</span></span>
8. <span data-ttu-id="9df79-119">ในฟิลด์ **หมายเลขสินค้า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="9df79-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="9df79-120">สินค้าที่ไม่มีการเก็บในคลังหรือประเภทการจัดซื้ออย่างใดอย่างหนึ่่ง สามารถใช้สำหรับการซื้อสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="9df79-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="9df79-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9df79-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="9df79-122">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="9df79-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="9df79-123">รายการใบแจ้งหนี้หนึ่งรายการจะสร้างสินทรัพย์ถาวรแค่หนึ่งรายการโดยไม่คำนึงถึงปริมาณ </span><span class="sxs-lookup"><span data-stu-id="9df79-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="9df79-124">ค่าของฟิลด์ปริมาณใบแจ้งหนี้จะถูกโอนย้ายไปเป็นปริมาณสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="9df79-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="9df79-125">ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="9df79-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="9df79-126">ขยาย fastTab **รายละเอียดรายการ**</span><span class="sxs-lookup"><span data-stu-id="9df79-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="9df79-127">คลิกที่แท็บ **สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="9df79-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="9df79-128">เลือกกล่องกาเครื่องหมาย **สร้างสินทรัพย์ถาวรใหม่**</span><span class="sxs-lookup"><span data-stu-id="9df79-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="9df79-129">ในฟิลด์ **สินทรัพย์ถาวร** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="9df79-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="9df79-130">ในรายการ ให้เลือกสินทรัพย์ถาวรที่จะใช้เมื่อมีการสร้างสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="9df79-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="9df79-131">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9df79-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="9df79-132">คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="9df79-132">Click **Post**.</span></span> <span data-ttu-id="9df79-133">สินทรัพย์ถาวรจะถูกสร้างและซื้อเมื่อมีการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="9df79-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

