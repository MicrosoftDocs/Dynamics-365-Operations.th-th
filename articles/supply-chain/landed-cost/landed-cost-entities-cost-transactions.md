---
title: เอนทิตี้ธุรกรรมต้นทุน
description: บทความนี้มีข้อมูลเกี่ยวกับเอนทิตีธุรกรรมต้นทุน ซึ่งเปิดใช้งานค่าของต้นทุนที่จะแบ่งระหว่างเนื้อหาของพื้นที่ต้นทุนโดยผ่านการเลือกวิธีการแบ่งตามส่วน
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 3aabc1356eba27de797fa696dd928cb401d8501b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860825"
---
# <a name="cost-transaction-entities"></a>เอนทิตีธุรกรรมต้นทุน

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

## <a name="apportionment"></a>การแบ่งตามส่วน

ต้นทุนแฝงช่วยให้มูลค่าของต้นทุนสามารถแบ่งระหว่างเนื้อหาของพื้นที่ต้นทุน (การเดินทาง คอนเทนเนอร์การจัดส่ง และอื่นๆ) โดยผ่านการเลือกวิธีการแบ่งตามส่วน วิธีการแบ่งตามส่วนจะถูกกําหนดโดยเป็นส่วนหนึ่งของการตั้งค่าคอนฟิกต้นทุนอัตโนมัติที่เป็นไปตามกฎทางธุรกิจ ซึ่งดึงไว้เป็นส่วนหนึ่งของต้นทุนเมื่อสร้างรายการการเดินทาง

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>ตั้งค่าคอนฟิกการแม็ปการแบ่งตามส่วนเพื่อใช้กับเอนทิตีข้อมูล

เมื่อสร้างต้นทุนจากแหล่งที่มาภายนอก เช่น ผู้ขนส่งสินค้า แหล่งที่มาภายนอกไม่สามารถระบุวิธีการที่ต้องการเพื่อแบ่งมูลค่าต้นทุนตามส่วนได้ การแม็ปการแบ่งตามส่วนจะกําหนดวิธีการแบ่งตามส่วนเริ่มต้นให้กับรหัสชนิดต้นทุนแต่ละรหัส ตารางการแม็ปการแบ่งตามส่วนสามารถเข้าถึงได้จากหน้า **การแม็ปการแบ่งตามส่วน** ใน Microsoft Dynamics 365 Supply Chain Management (**ต้นทุนแฝง \> การตั้งค่าการคิดต้นทุน \> การแม็ปการแบ่งตามส่วน**)

ถ้ากําหนดชุดการแม็ปไว้ และต้นทุนที่ตรงกับรหัสชนิดต้นทุนจะถูกสร้างขึ้นโดยใช้เอนทิตีธุรกรรมต้นทุน วิธีการแบ่งตามส่วนที่แม็ปจะถูกใช้แทนค่าใดๆ ที่จัดเตรียมให้กับเอนทิตี

ถ้าไม่มีค่าแสดงอยู่ในตารางการแม็ป แต่มีที่ให้ค่าให้กับเอนทิตีแล้ว จะมีการใช้ค่าที่ระบุ

ถ้าไม่มีค่าอยู่ในตารางการแม็ปหรือเรกคอร์ดที่ส่งไปที่เอนทิตี การสร้างจะล้มเหลว

### <a name="apportionment-mapping-itmapportionmentmapping"></a>การแม็ปการแบ่งตามส่วน (ITMApportionmentMapping)

เอนทิตีการแม็ปการแบ่งตามส่วน (`ITMApportionmentMapping`) สร้างความสัมพันธ์การแม็ปการแบ่งตามส่วน และช่วยให้ผู้ใช้สามารถสร้างหรืออัปเดตเรกคอร์ดได้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| วิธีการแบ่งตามส่วน | ITMApportionmentMapping.ApportionmentMethod | Int | ไม่ | ไม่ |
| รหัสชนิดต้นทุน | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **ใช่** | ไม่ |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>ต้นทุนการเดินทาง (ITMCostTransVoyageEntity)

เอนทิตีต้นทุนการเดินทาง (`ITMCostTransVoyageEntity`) สร้างธุรกรรมต้นทุนการเดินทางที่ใช้ที่ระดับการเดินทาง ในระหว่างกระบวนการนําเข้า ระบบจะใช้ค่า **ประเภท** และ **วิธีการแบ่งตามส่วน** ซึ่งรวมอยู่ในเอนทิตี้เพื่อระบุว่ามูลค่าของต้นทุนถูกแยกตามส่วนในเนื้อหาของการเดินทางอย่างไร

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| วิธีการแบ่งตามส่วน | ITMCostTrans.ApportionmentMethod | Int | ไม่ | ไม่ |
| มูลค่าต้นทุน | ITMCostTrans.CostValue | Numeric(32, 6) | ไม่ | ไม่ |
| สกุลเงิน | ITMCostTrans.CurrencyCode | Nvarchar(3) | ไม่ | **ใช่** |
| หมายเลขรายการ | ITMCostTrans.LineNum | Numeric(32, 16) | **ใช่** | ไม่ |
| ชนิดต้นทุนที่เชื่อมโยง | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| ต้นทุนขั้นต่ำ | ITMCostTrans.MinCostAmount | Numeric(32, 6) | ไม่ | ไม่ |
| ประเภท | ITMCostTrans.ShipCostCategory | Int | ไม่ | ไม่ |
| รหัสชนิดต้นทุน | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| บริษัท | ITMCostTrans.ShipDataArea | Nvarchar(4) | ไม่ | **ใช่** |
| การเดินทาง | ITMCostTrans.TransRecId | Nvarchar(20) | **ใช่** | ไม่ |
| กลุ่มภาษีขายตามประเภทสินค้า | ITMCostTrans.TaxItemGroup | Nvarchar(10) | ไม่ | ไม่ |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>ต้นทุนคอนเทนเนอร์การจัดส่ง (ITMCostTransShippingContainerEntity)

เอนทิตีต้นทุนคอนเทนเนอร์การจัดส่ง (`ITMCostTransShippingContainerEntity`) สร้างต้นทุนคอนเทนเนอร์การจัดส่งที่ใช้ในระดับคอนเทนเนอร์การจัดส่ง ในระหว่างกระบวนการนําเข้า ระบบจะใช้ค่า **ประเภท** และ **วิธีการแบ่งตามส่วน** ซึ่งรวมอยู่ในเอนทิตี้เพื่อระบุว่ามูลค่าของต้นทุนถูกแยกตามส่วนในเนื้อหาของคอนเทนเนอร์การจัดส่งอย่างไร

ฟิลด์ **ค่ารวม** **ขา** และ **ขาที่เชื่อมโยง** จะระบุเฉพาะกับเรกคอร์ดที่ค่าของ **พื้นที่ต้นทุน** คือ *คอนเทนเนอร์การจัดส่ง* ดังนั้น จึงไม่มีอยู่ในเอนทิตีข้อมูลเนื่องจากพื้นที่ต้นทุนอื่นๆ

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| การรวม | ITMCostTrans.AggregatedCost | Int | ไม่ | ไม่ |
| วิธีการแบ่งตามส่วน | ITMCostTrans.ApportionmentMethod | Int | ไม่ | ไม่ |
| มูลค่าต้นทุน | ITMCostTrans.CostValue | Numeric(32, 6) | ไม่ | ไม่ |
| สกุลเงิน | ITMCostTrans.CurrencyCode | Nvarchar(3) | ไม่ | **ใช่** |
| หมายเลขรายการ | ITMCostTrans.LineNum | Numeric(32, 16) | **ใช่** | ไม่ |
| ชนิดต้นทุนที่เชื่อมโยง | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| ช่วงที่เชื่อมโยง | ITMCostTrans.LinkLegId | Nvarchar(20) | ไม่ | ไม่ |
| ต้นทุนขั้นต่ำ | ITMCostTrans.MinCostAmount | Numeric(32, 6) | ไม่ | ไม่ |
| คอนเทนเนอร์การจัดส่ง | ITMCostTrans.TransRecId | Nvarchar(20) | **ใช่** | ไม่ |
| ประเภท | ITMCostTrans.ShipCostCategory | Int | ไม่ | ไม่ |
| รหัสชนิดต้นทุน | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| บริษัท | ITMCostTrans.ShipDataArea | Nvarchar(4) | ไม่ | **ใช่** |
| การเดินทาง | ITMCostTrans.TransRecId | Nvarchar(20) | **ใช่** | ไม่ |
| ช่วง | ITMCostTrans.ShipLegId | Nvarchar(20) | ไม่ | ไม่ |
| กลุ่มภาษีขายตามประเภทสินค้า | ITMCostTrans.TaxItemGroup | Nvarchar(10) | ไม่ | ไม่ |

## <a name="folio-costs-itmcosttransfolioentity"></a>ต้นทุนใบแจ้งรายการ (ITMCostTransFolioEntity)

เอนทิตีต้นทุนใบแจ้งรายการ (`ITMCostTransFolioEntity`) จะสร้างเรกคอร์ดธุรกรรมต้นทุนที่ใช้กับระดับใบแจ้งรายการ ในระหว่างกระบวนการนําเข้า ระบบจะใช้ค่า **ประเภท** และ **วิธีการแบ่งตามส่วน** ซึ่งรวมอยู่ในเอนทิตี้เพื่อระบุว่ามูลค่าของต้นทุนถูกแยกตามส่วนในเนื้อหาของแต่ละใบแจ้งรายการอย่างไร

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| วิธีการแบ่งตามส่วน | ITMCostTrans.ApportionmentMethod | Int | ไม่ | ไม่ |
| มูลค่าต้นทุน | ITMCostTrans.CostValue | Numeric(32, 6) | ไม่ | ไม่ |
| สกุลเงิน | ITMCostTrans.CurrencyCode | Nvarchar(3) | ไม่ | **ใช่** |
| หมายเลขรายการ | ITMCostTrans.LineNum | Numeric(32, 16) | **ใช่** | ไม่ |
| ชนิดต้นทุนที่เชื่อมโยง | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| ต้นทุนขั้นต่ำ | ITMCostTrans.MinCostAmount | Numeric(32, 6) | ไม่ | ไม่ |
| ประเภท | ITMCostTrans.ShipCostCategory | Int | ไม่ | ไม่ |
| รหัสชนิดต้นทุน | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| บริษัท | ITMCostTrans.ShipDataArea | Nvarchar(4) | ไม่ | **ใช่** |
| ใบแจ้งรายการ | ITMCostTrans.TransRecId | Nvarchar(20) | **ใช่** | ไม่ |
| กลุ่มภาษีขายตามประเภทสินค้า | ITMCostTrans.TaxItemGroup | Nvarchar(10) | ไม่ | ไม่ |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>ต้นทุนใบสั่งซื้อ (ITMCostTransPurchaseEntity)

เอนทิตีต้นทุนใบสั่งซื้อ (`ITMCostTransPurchaseEntity`) สร้างธุรกรรมต้นทุนที่ใช้กับส่วนหัวของใบสั่งซื้อ ในระหว่างกระบวนการนําเข้า ระบบจะใช้ค่า **ประเภท** และ **วิธีการแบ่งตามส่วน** ซึ่งรวมอยู่ในเอนทิตี้เพื่อระบุว่ามูลค่าของต้นทุนถูกแยกตามส่วนในเนื้อหาของแต่ละใบแจ้งรายการอย่างไร

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| วิธีการแบ่งตามส่วน | ITMCostTrans.ApportionmentMethod | Int | ไม่ | ไม่ |
| มูลค่าต้นทุน | ITMCostTrans.CostValue | Numeric(32, 6) | ไม่ | ไม่ |
| สกุลเงิน | ITMCostTrans.CurrencyCode | Nvarchar(3) | ไม่ | **ใช่** |
| หมายเลขรายการ | ITMCostTrans.LineNum | Numeric(32, 16) | **ใช่** | ไม่ |
| ชนิดต้นทุนที่เชื่อมโยง | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| ต้นทุนขั้นต่ำ | ITMCostTrans.MinCostAmount | Numeric(32, 6) | ไม่ | ไม่ |
| ใบสั่งซื้อ | ITMCostTrans.TransRecId | Nvarchar(20) | **ใช่** | ไม่ |
| ประเภท | ITMCostTrans.ShipCostCategory | Int | ไม่ | ไม่ |
| รหัสชนิดต้นทุน | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| บริษัท | ITMCostTrans.ShipDataArea | Nvarchar(4) | ไม่ | **ใช่** |
| กลุ่มภาษีขายตามประเภทสินค้า | ITMCostTrans.TaxItemGroup | Nvarchar(10) | ไม่ | ไม่ |

## <a name="item-costs-itmcosttransitementity"></a>ต้นทุนสินค้า (ITMCostTransItemEntity)

เอนทิตีต้นทุนสินค้า (`ITMCostTransItemEntity`) จะสร้างธุรกรรมต้นทุนที่ใช้กับระดับสินค้า เอนทิตีนี้ใช้เฉพาะกับสินค้าในรายการใบสั่งซื้อ มูลค่าของต้นทุนจะใช้เต็มมูลค่ากับบรรทัด

ฟิลด์ **ยอดการปรับปรุง** และ **การปรับปรุงมูลค่า** จะระบุเฉพาะที่พื้นที่ต้นทุนระดับบรรทัด ดังนั้น จึงไม่มีอยู่ในเอนทิตีข้อมูลเนื่องจากพื้นที่ต้นทุนอื่นๆ

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| ยอดเงินที่มีการปรับปรุง | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | ไม่ | ไม่ |
| มูลค่าต้นทุน | ITMCostTrans.CostValue | Numeric(32, 6) | ไม่ | ไม่ |
| สกุลเงิน | ITMCostTrans.CurrencyCode | Nvarchar(3) | ไม่ | **ใช่** |
| หมายเลขรายการ | ITMCostTrans.LineNum | Numeric(32, 16) | **ใช่** | ไม่ |
| ชนิดต้นทุนที่เชื่อมโยง | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| ต้นทุนขั้นต่ำ | ITMCostTrans.MinCostAmount | Numeric(32, 6) | ไม่ | ไม่ |
| ใบสั่งซื้อ | ITMCostTrans.TransRecId | Nvarchar(20) | **ใช่** | ไม่ |
| หมายเลขรายการใบสั่งซื้อ | ITMCostTrans.TransRecId | Nvarchar(20) | **ใช่** | ไม่ |
| ประเภท | ITMCostTrans.ShipCostCategory | Int | ไม่ | ไม่ |
| รหัสชนิดต้นทุน | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| บริษัท | ITMCostTrans.ShipDataArea | Nvarchar(4) | ไม่ | **ใช่** |
| กลุ่มภาษีขายตามประเภทสินค้า | ITMCostTrans.TaxItemGroup | Nvarchar(10) | ไม่ | ไม่ |
| การปรับปรุงค่า | ITMCostTrans.ValueAdjustmentMethod | Int | ไม่ | ไม่ |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>ต้นทุนรายการโอนย้าย (ITMCostTransTransferLineEntity)

เอนทิตีต้นทุนรายการโอนย้าย (`ITMCostTransTransferLineEntity`) สร้างธุรกรรมต้นทุนที่ใช้กับระดับของรายการใบสั่งโอนย้าย มูลค่าของต้นทุนเหล่านี้จะใช้เต็มมูลค่ากับรายการใบสั่งโอนย้าย

ฟิลด์ **ยอดการปรับปรุง** และ **การปรับปรุงมูลค่า** จะระบุเฉพาะที่พื้นที่ต้นทุนระดับบรรทัด ดังนั้น จึงไม่มีอยู่ในเอนทิตีข้อมูลเนื่องจากพื้นที่ต้นทุนอื่นๆ

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| ยอดเงินที่มีการปรับปรุง | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | ไม่ | ไม่ |
| มูลค่าต้นทุน | ITMCostTrans.CostValue | Numeric(32, 6) | ไม่ | ไม่ |
| สกุลเงิน | ITMCostTrans.CurrencyCode | Nvarchar(3) | ไม่ | **ใช่** |
| หมายเลขรายการ | ITMCostTrans.LineNum | Numeric(32, 16) | **ใช่** | ไม่ |
| ชนิดต้นทุนที่เชื่อมโยง | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| ต้นทุนขั้นต่ำ | ITMCostTrans.MinCostAmount | Numeric(32, 6) | ไม่ | ไม่ |
| ประเภท | ITMCostTrans.ShipCostCategory | Int | ไม่ | ไม่ |
| รหัสชนิดต้นทุน | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | ไม่ | ไม่ |
| บริษัท | ITMCostTrans.ShipDataArea | Nvarchar(4) | ไม่ | **ใช่** |
| ใบสั่งโอน | ITMCostTrans.TransRecId | Nvarchar(20) | **ใช่** | ไม่ |
| หมายเลขรายการใบสั่งโอนย้าย | ITMCostTrans.TransRecId | Nvarchar(20) | **ใช่** | ไม่ |
| กลุ่มภาษีขายตามประเภทสินค้า | ITMCostTrans.TaxItemGroup | Nvarchar(10) | ไม่ | ไม่ |
| การปรับปรุงค่า | ITMCostTrans.ValueAdjustmentMethod | Int | ไม่ | ไม่ |

### <a name="transaction-table"></a>ตารางธุรกรรม

เรกคอร์ดธุรกรรมต้นทุนสัมพันธ์กับพื้นที่ต้นทุนของการมอบหมายหมายเลขตารางธุรกรรม (`TransTableId`) เมื่อต้องใช้หมายเลขรหัสตารางเฉพาะ เอนทิตีจะถูกแบ่งตามค่าเหล่านี้ เพื่อให้มีเอนทิตีอยู่ต่อพื้นที่ต้นทุนแต่ละพื้นที่

ค่าสำหรับตารางธุรกรรม (`TransTableId`) จะเป็นแบบโดยนัยในการเลือกเอนทิตีธุรกรรมต้นทุน

### <a name="calculated-fields"></a>ฟิลด์ที่คำนวณได้

ฟิลด์ต่อไปนี้ไม่พร้อมให้แทรกหรืออัปเดตเมื่อใช้เอนทิตีธุรกรรมต้นทุน เนื่องจากฟิลด์เหล่านี้จะถูกตั้งค่าเฉพาะเมื่อมีการใช้การกิจกรรมเฉพาะกับเรกคอร์ดการเดินทางเท่านั้น:

- **ต้นทุนที่ประเมิน** – ฟิลด์นี้จะถูกตั้งค่าไว้เมื่อลงรายการบัญชีใบแจ้งหนี้เพื่อการเดินทาง (ใบสั่งซื้อ) หรือได้รับการโอนย้าย
- **สกุลเงินต้นทุนที่ประเมิน** – ฟิลด์นี้จะถูกตั้งค่าไว้เมื่อลงรายการบัญชีใบแจ้งหนี้เพื่อการเดินทาง (ใบสั่งซื้อ) หรือได้รับการโอนย้าย
- **ต้นทุนจริง** – ฟิลด์นี้จะถูกตั้งค่าไว้เมื่อลงรายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย ซึ่งเชื่อมโยงกับต้นทุน

### <a name="find-auto-costs"></a>ค้นหาต้นทุนอัตโนมัติ

ปุ่ม **ค้นหาต้นทุนอัตโนมัติ** ที่พร้อมใช้งานต่อพื้นที่ต้นทุนแต่ละพื้นที่ (การเดินทาง คอนเทนเนอร์การจัดส่ง และอื่นๆ) จะกําหนดวิธีการอัปเดตธุรกรรมต้นทุนของพื้นที่ต้นทุนนั้นจากข้อมูลในตารางการตั้งค่าคอนฟิก เมื่อคุณเลือกปุ่มใดพื้นที่หนึ่งต้นทุน ระบบจะล้างข้อมูลต้นทุนที่มีอยู่ของพื้นที่ต้นทุนนั้นและสร้างเรกคอร์ดใหม่ ตามการตั้งค่าคอนฟิกปัจจุบันของตารางการตั้งค่าต้นทุนอัตโนมัติ

เรกคอร์ดธุรกรรมต้นทุนที่สร้างโดยใช้เอนทิตีข้อมูลจะถูกแฟล็กเป็นนําเข้า เรกคอร์ดเหล่านี้จะไม่ถูกลบเมื่อคุณเลือก **ค้นหาต้นทุนอัตโนมัติ** เนื่องจากจะไม่ถูกสร้างใหม่จากตารางการตั้งค่าต้นทุนอัตโนมัติ อย่างไรก็ตาม เรกคอร์ดธุรกรรมต้นทุนที่มีแฟล็กเป็นนําเข้ายังคงสามารถลบออกได้

### <a name="linked-fields"></a>ฟิลด์ที่เชื่อมโยง

ธุรกรรมต้นทุนแต่ละธุรกรรมสามารถเชื่อมโยงกับเรกคอร์ดอื่นในพื้นที่ต้นทุนเดียวกันได้ มีการเชื่อมต่อนี้ผ่านฟิลด์ **ชนิดต้นทุนที่เชื่อมโยง** ซึ่งช่วยให้สามารถคํานวณมูลค่าต้นทุนเป็นเปอร์เซ็นต์ของต้นทุนอื่นได้

ฟิลด์ **ชนิดต้นทุนที่เชื่อมโยง** สามารถตรวจสอบความถูกต้องได้ เฉพาะเมื่อเรกคอร์ดที่อ้างอิงมีการประมวลผลก่อน หรือถ้ามีอยู่แล้วในตาราง ความต้องการเดียวกันนี้จะใช้กับฟิลด์ **ขาที่เชื่อมโยง** ที่ใช้กับต้นทุนในพื้นที่ต้นทุนของคอนเทนเนอร์การจัดส่งเท่านั้น
