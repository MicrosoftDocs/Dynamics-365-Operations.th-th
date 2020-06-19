---
title: ความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตรวบสอบความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426993"
---
# <a name="inventory-availability"></a><span data-ttu-id="6d401-103">ความพร้อมของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="6d401-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6d401-104">การใช้ความพร้อมของสินค้าคงคลัง คุณสามารถตรวจสอบสินค้าคงคลังของคุณก่อนที่คุณจะเพิ่มผลิตภัณฑ์ลงในฟอร์ม **ใบเสนอราคา** **ใบสั่ง** หรือ **ใบแจ้งหนี้** ในแอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6d401-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="6d401-105">ตัวอย่างเช่น การตรวจสอบสินค้าคงคลังและการกำหนดวันที่การเติมสินค้าเป็นงานหลักในกระบวนการ [ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด](dual-write-prospect-to-cash.md)</span><span class="sxs-lookup"><span data-stu-id="6d401-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="6d401-106">ถ้าคุณมีสินค้าคงคลังไม่เพียงพอ คุณสามารถประเมินวันที่จัดส่งตามการรับและปัญหาสินค้าคงคลังที่คาดการณ์</span><span class="sxs-lookup"><span data-stu-id="6d401-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="6d401-107">นอกจากนี้ คุณยังสามารถตรวจสอบข้อมูลที่สามารถสัญญาได้ (ATP) ของผลิตภัณฑ์ ซึ่งคุณสามารถค้นหาปริมาณ ATP ในกรอบเวลาที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="6d401-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="6d401-108">สินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="6d401-108">On-hand Inventory</span></span> 

<span data-ttu-id="6d401-109">ในส่วนหัวของฟอร์ม **ใบเสนอราคา** **ใบสั่ง** หรือ **ใบแจ้งหนี้** ใน Dynamics 365 Sales **สินค้าคงคลังคงเหลือ** ของปุ่มใหม่จะถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6d401-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="6d401-110">เมื่อคุณคลิกปุ่ม กล่องโต้ตอบจะปรากฏขึ้น และคุณสามารถระบุบริษัทและผลิตภัณฑ์ที่คุณต้องการตรวจสอบปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="6d401-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="6d401-111">ส่งคืนข้อมูลสินค้าคงคลังจาก Dynamics 365 Supply Chain Management และแสดงข้อมูลเดียวกันกับ [ปริมาณคงคลังคงเหลือ](../../../../supply-chain/inventory/tasks/check-availability-stock.md)</span><span class="sxs-lookup"><span data-stu-id="6d401-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="6d401-112">ข้อมูลรวมถึงปริมาณเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6d401-112">The information includes these quantities:</span></span>

- <span data-ttu-id="6d401-113">**ปริมาณคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="6d401-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="6d401-114">**ปริมาณคงเหลือที่จองไว้**</span><span class="sxs-lookup"><span data-stu-id="6d401-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="6d401-115">**ปริมาณคงเหลือที่พร้อมใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="6d401-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="6d401-116">**ปริมาณที่สั่ง**</span><span class="sxs-lookup"><span data-stu-id="6d401-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="6d401-117">**ปริมาณที่อยู่ระหว่างการสั่ง**</span><span class="sxs-lookup"><span data-stu-id="6d401-117">**On-order Quantity**</span></span>
- <span data-ttu-id="6d401-118">**ปริมาณที่สั่งที่จองไว้**</span><span class="sxs-lookup"><span data-stu-id="6d401-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="6d401-119">**ปริมาณที่พร้อมใช้งานรวม**</span><span class="sxs-lookup"><span data-stu-id="6d401-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="6d401-120">ข้อมูล ATP</span><span class="sxs-lookup"><span data-stu-id="6d401-120">ATP information</span></span>

<span data-ttu-id="6d401-121">ในราบการบรรทัดของฟอร์ม **ใบเสนอราคา** **ใบสั่ง** หรือ **ใบแจ้งหนี้** ใน Dynamics 365 Sales **ข้อมูล ATP** ของปุ่มใหม่จะถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6d401-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="6d401-122">เมื่อคุณคลิกปุ่ม กล่องโต้ตอบจะปรากฏขึ้น และคุณสามารถระบุบริษัท ผลิตภัณฑ์ ไซต์สินค้าคงคลัง คลังสินค้า และปริมาณการสั่ง</span><span class="sxs-lookup"><span data-stu-id="6d401-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="6d401-123">ส่งคืน **ข้อมูล ATP** จาก Supply Chain Management และแสดงการตั้งค่า descrbed ใน [สัญญาใบสั่ง](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations)</span><span class="sxs-lookup"><span data-stu-id="6d401-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="6d401-124">ข้อมูลรวมถึง **ปริมาณ ATP** **ปริมาณที่รับ** **ปริมาณการออกใช้** และ **ปริมาณคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="6d401-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
