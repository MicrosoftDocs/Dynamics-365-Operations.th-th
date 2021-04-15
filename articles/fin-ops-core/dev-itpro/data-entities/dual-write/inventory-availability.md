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
# <a name="inventory-availability-in-dual-write"></a>ความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง

[!include [banner](../../includes/banner.md)]

โดยการใช้ความพร้อมของสินค้าคงคลัง คุณสามารถตรวจสอบสินค้าคงคลังของคุณ ก่อนที่คุณจะเพิ่มผลิตภัณฑ์ลงในหน้า **ใบเสนอราคา** **ใบสั่ง** หรือ **ใบแจ้งหนี้** ใน Microsoft Dynamics 365 Sales ตัวอย่างเช่น คุณตรวจสอบสินค้าคงคลังและกำหนดวันเติมสินค้าเป็นงานหลักหนึ่งงานในกระบวนการ [ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด](dual-write-prospect-to-cash.md)

ถ้าคุณมีสินค้าคงคลังไม่เพียงพอ คุณสามารถประเมินวันที่จัดส่งตามการรับสินค้าและการตัดสินค้าจากคลังที่คาดการณ์ นอกจากนี้ คุณยังสามารถตรวจสอบข้อมูลที่สามารถสัญญาได้ (ATP) ของผลิตภัณฑ์ ซึ่งคุณสามารถค้นหาปริมาณ ATP ได้ในกรอบเวลาที่กำหนดไว้ล่วงหน้า

## <a name="on-hand-inventory"></a>ปริมาณสินค้าคงคลังคงเหลือ

ใน Dynamics 365 Sales ปุ่ม **สินค้าคงคลังคงเหลือ** ใหม่จะถูกเพิ่มไปยังส่วนหัวของหน้า **ใบเสนอราคา** **ใบสั่ง** และ **ใบแจ้งหนี้** เมื่อคุณเลือกปุ่มนี้ กล่องโต้ตอบจะปรากฏขึ้น ที่ซึ่งคุณสามารถระบุบริษัทและผลิตภัณฑ์ที่คุณต้องการตรวจสอบปริมาณคงคลังคงเหลือ กล่องโต้ตอบนี้จะแสดงข้อมูลเดียวกันกับ [ปริมาณคงคลังคงเหลือ](../../../../supply-chain/inventory/tasks/check-availability-stock.md)

กล่องโต้ตอบจะส่งคืนข้อมูลสินค้าคงคลังจาก Dynamics 365 Supply Chain Management ข้อมูลนี้ประกอบด้วยปริมาณต่อไปนี้:

- ปริมาณคงคลังคงเหลือ
- ปริมาณคงคลังคงเหลือที่จองไว้
- ปริมาณคงคลังคงเหลือที่พร้อมใช้งาน
- ปริมาณที่สั่ง
- ปริมาณในใบสั่ง
- ปริมาณที่สั่งที่จองไว้
- ปริมาณที่พร้อมใช้งานรวม

## <a name="atp-information"></a>ข้อมูล ATP

ใน Sales จะมีการเพิ่มปุ่ม **ข้อมูล ATP** ใหม่ ไปยังสินค้าในสินค้าในบรรทัดบนหน้า **ใบเสนอราคา** **ใบสั่ง** และ **ใบแจ้งหนี้** เมื่อคุณเลือกปุ่มนี้ กล่องโต้ตอบจะปรากฏขึ้น ที่ซึ่งคุณสามารถระบุบริษัท ผลิตภัณฑ์ ไซต์สินค้าคงคลัง คลังสินค้าคงคลัง และปริมาณในใบสั่ง กล่องโต้ตอบนี้มีการตั้งค่าเดียวกันกับที่อธิบายไว้ในการกำหนด [สัญญาใบสั่ง](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations)

กล่องโต้ตอบจะส่งคืนข้อมูล ATP จาก Supply Chain Management ข้อมูลนี้ประกอบด้วยปริมาณต่อไปนี้:

- ปริมาณ ATP
- ปริมาณที่รับ
- ปริมาณการออกใช้
- ปริมาณคงคลังคงเหลือ

## <a name="how-it-works"></a>วิธีการทำงาน

เมื่อคุณเลือกปุ่ม **สินค้าคงคลังคงเหลือ** บนหน้า **ใบเสนอราคา** **ใบสั่งซื้อ** หรือ **ใบแจ้งหนี้** การเรียกการรวมแบบสองทิศทางแบบสดจะเรียกใช้ API **สินค้าคงคลังคงเหลือ** API จะคํานวณปริมาณสินค้าคงคลังคงเหลือของผลิตภัณฑ์ที่ระบุ ผลลัพธ์จะถูกจัดเก็บอยู่ในตาราง **InventCDSInventoryOnHandRequestEntity** และ **InventCDSInventoryOnHandEntryEntity** และเขียนไปยัง Dataverse โดยการรวมแบบสองทิศทาง หากต้องการใช้ฟังก์ชันนี้ คุณต้องรันแผนผังการรวมแบบสองทิศทางต่อไปนี้ ข้ามการซิงโครไนส์เริ่มแรก เมื่อคุณรันแผนผัง

- รายการสินค้าคงคลังคงเหลือของ CDS (msdyn_inventoryonhandentries)
- การร้องขอสินค้าคงคลังคงเหลือของ CDS (msdyn_inventoryonhandrequests)

## <a name="templates"></a>เท็มเพลต
เท็มเพลตต่อไปนี้มีให้ใช้งานกับข้อมูลของสินค้าคงคลังคงเหลือที่จัดการอยู่

แอป Finance and Operations | แอป Customer Engagement | คำอธิบาย 
---|---|---
[รายการปริมาณสินค้าคงคลังคงเหลือของ CDS](#145) | msdyn_inventoryonhandentries |
[คำขอปริมาณสินค้าคงคลังคงเหลือของ CDS](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>รายการสินค้าคงคลังคงเหลือของ CDS (msdyn_inventoryonhandentries)

เท็มเพลตนี้ซิงโครไนส์ข้อมูลระหว่างแอป Finance and Operations และ Dataverse

ฟิลด์ Finance and Operations | ชนิดของการแม็ป | ฟิลด์ Customer Engagement | ค่าเริ่มต้น
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

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>การร้องขอสินค้าคงคลังคงเหลือของ CDS (msdyn_inventoryonhandrequests)

เท็มเพลตนี้ซิงโครไนส์ข้อมูลระหว่างแอป Finance and Operations และ Dataverse

ฟิลด์ Finance and Operations | ชนิดของการแม็ป | ฟิลด์ Customer Engagement | ค่าเริ่มต้น
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