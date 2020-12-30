---
title: ความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการตรวจสอบความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4457847"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="37869-103">ความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="37869-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37869-104">โดยการใช้ความพร้อมของสินค้าคงคลัง คุณสามารถตรวจสอบสินค้าคงคลังของคุณ ก่อนที่คุณจะเพิ่มผลิตภัณฑ์ลงในหน้า **ใบเสนอราคา** **ใบสั่ง** หรือ **ใบแจ้งหนี้** ใน Microsoft Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="37869-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="37869-105">ตัวอย่างเช่น คุณตรวจสอบสินค้าคงคลังและกำหนดวันเติมสินค้าเป็นงานหลักหนึ่งงานในกระบวนการ [ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด](dual-write-prospect-to-cash.md)</span><span class="sxs-lookup"><span data-stu-id="37869-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="37869-106">ถ้าคุณมีสินค้าคงคลังไม่เพียงพอ คุณสามารถประเมินวันที่จัดส่งตามการรับสินค้าและการตัดสินค้าจากคลังที่คาดการณ์</span><span class="sxs-lookup"><span data-stu-id="37869-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="37869-107">นอกจากนี้ คุณยังสามารถตรวจสอบข้อมูลที่สามารถสัญญาได้ (ATP) ของผลิตภัณฑ์ ซึ่งคุณสามารถค้นหาปริมาณ ATP ได้ในกรอบเวลาที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="37869-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="37869-108">ปริมาณสินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="37869-108">On-hand inventory</span></span>

<span data-ttu-id="37869-109">ใน Dynamics 365 Sales ปุ่ม **สินค้าคงคลังคงเหลือ** ใหม่จะถูกเพิ่มไปยังส่วนหัวของหน้า **ใบเสนอราคา** **ใบสั่ง** และ **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="37869-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="37869-110">เมื่อคุณเลือกปุ่มนี้ กล่องโต้ตอบจะปรากฏขึ้น ที่ซึ่งคุณสามารถระบุบริษัทและผลิตภัณฑ์ที่คุณต้องการตรวจสอบปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="37869-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="37869-111">กล่องโต้ตอบนี้จะแสดงข้อมูลเดียวกันกับ [ปริมาณคงคลังคงเหลือ](../../../../supply-chain/inventory/tasks/check-availability-stock.md)</span><span class="sxs-lookup"><span data-stu-id="37869-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="37869-112">กล่องโต้ตอบจะส่งคืนข้อมูลสินค้าคงคลังจาก Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="37869-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="37869-113">ข้อมูลนี้ประกอบด้วยปริมาณต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="37869-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="37869-114">ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="37869-114">On-hand quantity</span></span>
- <span data-ttu-id="37869-115">ปริมาณคงคลังคงเหลือที่จองไว้</span><span class="sxs-lookup"><span data-stu-id="37869-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="37869-116">ปริมาณคงคลังคงเหลือที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="37869-116">Available on-hand quantity</span></span>
- <span data-ttu-id="37869-117">ปริมาณที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="37869-117">Ordered quantity</span></span>
- <span data-ttu-id="37869-118">ปริมาณในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="37869-118">On-order quantity</span></span>
- <span data-ttu-id="37869-119">ปริมาณที่สั่งที่จองไว้</span><span class="sxs-lookup"><span data-stu-id="37869-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="37869-120">ปริมาณที่พร้อมใช้งานรวม</span><span class="sxs-lookup"><span data-stu-id="37869-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="37869-121">ข้อมูล ATP</span><span class="sxs-lookup"><span data-stu-id="37869-121">ATP information</span></span>

<span data-ttu-id="37869-122">ใน Sales จะมีการเพิ่มปุ่ม **ข้อมูล ATP** ใหม่ ไปยังสินค้าในสินค้าในบรรทัดบนหน้า **ใบเสนอราคา** **ใบสั่ง** และ **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="37869-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="37869-123">เมื่อคุณเลือกปุ่มนี้ กล่องโต้ตอบจะปรากฏขึ้น ที่ซึ่งคุณสามารถระบุบริษัท ผลิตภัณฑ์ ไซต์สินค้าคงคลัง คลังสินค้าคงคลัง และปริมาณในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="37869-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="37869-124">กล่องโต้ตอบนี้มีการตั้งค่าเดียวกันกับที่อธิบายไว้ในการกำหนด [สัญญาใบสั่ง](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations)</span><span class="sxs-lookup"><span data-stu-id="37869-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="37869-125">กล่องโต้ตอบจะส่งคืนข้อมูล ATP จาก Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="37869-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="37869-126">ข้อมูลนี้ประกอบด้วยปริมาณต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="37869-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="37869-127">ปริมาณ ATP</span><span class="sxs-lookup"><span data-stu-id="37869-127">ATP quantity</span></span>
- <span data-ttu-id="37869-128">ปริมาณที่รับ</span><span class="sxs-lookup"><span data-stu-id="37869-128">Receipt quantity</span></span>
- <span data-ttu-id="37869-129">ปริมาณการออกใช้</span><span class="sxs-lookup"><span data-stu-id="37869-129">Issue quantity</span></span>
- <span data-ttu-id="37869-130">ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="37869-130">On-hand quantity</span></span>
