---
title: ความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการตรวจสอบความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง
author: yijialuan
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9d9b7970720218fbcf2f512345ade672810440b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748576"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="235d3-103">ความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="235d3-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="235d3-104">โดยการใช้ความพร้อมของสินค้าคงคลัง คุณสามารถตรวจสอบสินค้าคงคลังของคุณ ก่อนที่คุณจะเพิ่มผลิตภัณฑ์ลงในหน้า **ใบเสนอราคา** **ใบสั่ง** หรือ **ใบแจ้งหนี้** ใน Microsoft Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="235d3-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="235d3-105">ตัวอย่างเช่น คุณตรวจสอบสินค้าคงคลังและกำหนดวันเติมสินค้าเป็นงานหลักหนึ่งงานในกระบวนการ [ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด](dual-write-prospect-to-cash.md)</span><span class="sxs-lookup"><span data-stu-id="235d3-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="235d3-106">ถ้าคุณมีสินค้าคงคลังไม่เพียงพอ คุณสามารถประเมินวันที่จัดส่งตามการรับสินค้าและการตัดสินค้าจากคลังที่คาดการณ์</span><span class="sxs-lookup"><span data-stu-id="235d3-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="235d3-107">นอกจากนี้ คุณยังสามารถตรวจสอบข้อมูลที่สามารถสัญญาได้ (ATP) ของผลิตภัณฑ์ ซึ่งคุณสามารถค้นหาปริมาณ ATP ได้ในกรอบเวลาที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="235d3-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="235d3-108">ปริมาณสินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="235d3-108">On-hand inventory</span></span>

<span data-ttu-id="235d3-109">ใน Dynamics 365 Sales ปุ่ม **สินค้าคงคลังคงเหลือ** ใหม่จะถูกเพิ่มไปยังส่วนหัวของหน้า **ใบเสนอราคา** **ใบสั่ง** และ **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="235d3-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="235d3-110">เมื่อคุณเลือกปุ่มนี้ กล่องโต้ตอบจะปรากฏขึ้น ที่ซึ่งคุณสามารถระบุบริษัทและผลิตภัณฑ์ที่คุณต้องการตรวจสอบปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="235d3-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="235d3-111">กล่องโต้ตอบนี้จะแสดงข้อมูลเดียวกันกับ [ปริมาณคงคลังคงเหลือ](../../../../supply-chain/inventory/tasks/check-availability-stock.md)</span><span class="sxs-lookup"><span data-stu-id="235d3-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="235d3-112">กล่องโต้ตอบจะส่งคืนข้อมูลสินค้าคงคลังจาก Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="235d3-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="235d3-113">ข้อมูลนี้ประกอบด้วยปริมาณต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="235d3-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="235d3-114">ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="235d3-114">On-hand quantity</span></span>
- <span data-ttu-id="235d3-115">ปริมาณคงคลังคงเหลือที่จองไว้</span><span class="sxs-lookup"><span data-stu-id="235d3-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="235d3-116">ปริมาณคงคลังคงเหลือที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="235d3-116">Available on-hand quantity</span></span>
- <span data-ttu-id="235d3-117">ปริมาณที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="235d3-117">Ordered quantity</span></span>
- <span data-ttu-id="235d3-118">ปริมาณในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="235d3-118">On-order quantity</span></span>
- <span data-ttu-id="235d3-119">ปริมาณที่สั่งที่จองไว้</span><span class="sxs-lookup"><span data-stu-id="235d3-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="235d3-120">ปริมาณที่พร้อมใช้งานรวม</span><span class="sxs-lookup"><span data-stu-id="235d3-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="235d3-121">ข้อมูล ATP</span><span class="sxs-lookup"><span data-stu-id="235d3-121">ATP information</span></span>

<span data-ttu-id="235d3-122">ใน Sales จะมีการเพิ่มปุ่ม **ข้อมูล ATP** ใหม่ ไปยังสินค้าในสินค้าในบรรทัดบนหน้า **ใบเสนอราคา** **ใบสั่ง** และ **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="235d3-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="235d3-123">เมื่อคุณเลือกปุ่มนี้ กล่องโต้ตอบจะปรากฏขึ้น ที่ซึ่งคุณสามารถระบุบริษัท ผลิตภัณฑ์ ไซต์สินค้าคงคลัง คลังสินค้าคงคลัง และปริมาณในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="235d3-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="235d3-124">กล่องโต้ตอบนี้มีการตั้งค่าเดียวกันกับที่อธิบายไว้ในการกำหนด [สัญญาใบสั่ง](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations)</span><span class="sxs-lookup"><span data-stu-id="235d3-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="235d3-125">กล่องโต้ตอบจะส่งคืนข้อมูล ATP จาก Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="235d3-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="235d3-126">ข้อมูลนี้ประกอบด้วยปริมาณต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="235d3-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="235d3-127">ปริมาณ ATP</span><span class="sxs-lookup"><span data-stu-id="235d3-127">ATP quantity</span></span>
- <span data-ttu-id="235d3-128">ปริมาณที่รับ</span><span class="sxs-lookup"><span data-stu-id="235d3-128">Receipt quantity</span></span>
- <span data-ttu-id="235d3-129">ปริมาณการออกใช้</span><span class="sxs-lookup"><span data-stu-id="235d3-129">Issue quantity</span></span>
- <span data-ttu-id="235d3-130">ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="235d3-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="235d3-131">วิธีการทำงาน</span><span class="sxs-lookup"><span data-stu-id="235d3-131">How it works</span></span>

<span data-ttu-id="235d3-132">เมื่อคุณเลือกปุ่ม **สินค้าคงคลังคงเหลือ** บนหน้า **ใบเสนอราคา** **ใบสั่งซื้อ** หรือ **ใบแจ้งหนี้** การเรียกการรวมแบบสองทิศทางแบบสดจะเรียกใช้ API **สินค้าคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="235d3-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="235d3-133">API จะคํานวณปริมาณสินค้าคงคลังคงเหลือของผลิตภัณฑ์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="235d3-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="235d3-134">ผลลัพธ์จะถูกจัดเก็บอยู่ในตาราง **InventCDSInventoryOnHandRequestEntity** และ **InventCDSInventoryOnHandEntryEntity** และเขียนไปยัง Dataverse โดยการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="235d3-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="235d3-135">หากต้องการใช้ฟังก์ชันนี้ คุณต้องรันแผนผังการรวมแบบสองทิศทางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="235d3-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="235d3-136">ข้ามการซิงโครไนส์เริ่มแรก เมื่อคุณรันแผนผัง</span><span class="sxs-lookup"><span data-stu-id="235d3-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="235d3-137">รายการสินค้าคงคลังคงเหลือของ CDS (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="235d3-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="235d3-138">การร้องขอสินค้าคงคลังคงเหลือของ CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="235d3-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="235d3-139">เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="235d3-139">Templates</span></span>
<span data-ttu-id="235d3-140">เท็มเพลตต่อไปนี้มีให้ใช้งานกับข้อมูลของสินค้าคงคลังคงเหลือที่จัดการอยู่</span><span class="sxs-lookup"><span data-stu-id="235d3-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="235d3-141">แอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="235d3-141">Finance and Operations apps</span></span> | <span data-ttu-id="235d3-142">แอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="235d3-142">Customer engagement app</span></span> | <span data-ttu-id="235d3-143">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="235d3-143">Description</span></span> 
---|---|---
[<span data-ttu-id="235d3-144">รายการปริมาณสินค้าคงคลังคงเหลือของ CDS</span><span class="sxs-lookup"><span data-stu-id="235d3-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="235d3-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="235d3-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="235d3-146">คำขอปริมาณสินค้าคงคลังคงเหลือของ CDS</span><span class="sxs-lookup"><span data-stu-id="235d3-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="235d3-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="235d3-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="235d3-148">รายการสินค้าคงคลังคงเหลือของ CDS (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="235d3-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="235d3-149">เท็มเพลตนี้ซิงโครไนส์ข้อมูลระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="235d3-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="235d3-150">ฟิลด์ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="235d3-150">Finance and Operations field</span></span> | <span data-ttu-id="235d3-151">ชนิดของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="235d3-151">Map type</span></span> | <span data-ttu-id="235d3-152">ฟิลด์ Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="235d3-152">Customer engagement field</span></span> | <span data-ttu-id="235d3-153">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="235d3-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="235d3-154">การร้องขอสินค้าคงคลังคงเหลือของ CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="235d3-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="235d3-155">เท็มเพลตนี้ซิงโครไนส์ข้อมูลระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="235d3-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="235d3-156">ฟิลด์ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="235d3-156">Finance and Operations field</span></span> | <span data-ttu-id="235d3-157">ชนิดของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="235d3-157">Map type</span></span> | <span data-ttu-id="235d3-158">ฟิลด์ Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="235d3-158">Customer engagement field</span></span> | <span data-ttu-id="235d3-159">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="235d3-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]