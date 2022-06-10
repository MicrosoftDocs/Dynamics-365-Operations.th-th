---
title: เอนทิตีใบแจ้งหนี้ของผู้จัดจำหน่าย
description: หัวข้อนี้มีข้อมูลเกี่ยวกับเอนทิตี้ใบแจ้งหนี้ของผู้จัดจำหน่าย ซึ่งเปิดใช้งานรหัสชนิดต้นทุนที่จะตั้งค่าคอนฟิกให้กับต้นทุนภายในหรือต้นทุนที่ได้รับจากภายนอก
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
ms.openlocfilehash: 4bbe0fdbf95050ebfa707224f602e5e71ddb3a8f
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813137"
---
# <a name="vendor-invoice-entities"></a>เอนทิตีใบแจ้งหนี้ของผู้จัดจำหน่าย

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

โมดูล **ต้นทุนแฝง** ช่วยให้สามารถตั้งค่าคอนฟิกรหัสชนิดต้นทุนให้กับต้นทุนภายในหรือต้นทุนที่ได้รับภายนอก ถ้าต้นทุนเป็นต้นทุนจากภายนอกธุรกิจ ใบแจ้งหนี้จะคาดหวังจากผู้ให้บริการ ใบแจ้งหนี้นี้จะได้รับการประมวลผลเป็นสมุดรายวันใบแจ้งหนี้ที่สามารถเชื่อมโยงกับการเดินทาง และสามารถกระจายค่าของใบแจ้งหนี้ในต้นทุนการเดินทางหนึ่งรายการหรือมากกว่า

เอนทิตีใบแจ้งหนี้ของผู้จัดจำหน่ายเปิดใช้งานมูลค่าของบรรทัดสมุดรายวันที่จะปันส่วนในต้นทุนของการเดินทางที่มีรหัสชนิดต้นทุนเหมือนกันร่วมกัน

ต้นทุนสามารถปันส่วนได้เฉพาะถ้ามีส่วนหัวของสมุดรายวันใบแจ้งหนี้และบรรทัดสมุดรายวันใบแจ้งหนี้อยู่เท่านั้น

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>การปันส่วนต้นทุนการเดินทางให้แก่ผู้จัดจำหน่าย (ITMLedgerJournalCostLinesVoyagesEntity)

เอนทิตีข้อมูลการปันส่วนต้นทุนการเดินทางของผู้จัดจำหน่ายช่วยให้รายการใบแจ้งหนี้ของผู้จัดจำหน่ายสามารถปันส่วนในต้นทุนอย่างน้อยหนึ่งรายการที่ใช้กับพื้นที่ต้นทุนการเดินทาง ฟังก์ชันนี้รองรับโดยเอนทิตี `ITMLedgerJournalCostLinesVoyagesEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| ยอดเงินที่ปันส่วน | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | ไม่ | ไม่ |
| หมายเลขรายการธุรกรรมต้นทุน | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขรายการสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **ใช่** | ไม่ |
| การเดินทาง | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **ใช่** | ไม่ |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>การปันส่วนต้นทุนคอนเทนเนอร์การจัดส่งของผู้จัดจำหน่าย (ITMLedgerJournalCostLinesContainersEntity)

เอนทิตีข้อมูลการปันส่วนต้นทุนคอนเทนเนอร์การจัดส่งของผู้จัดจำหน่ายช่วยให้รายการใบแจ้งหนี้ของผู้จัดจำหน่ายสามารถปันส่วนในต้นทุนอย่างน้อยหนึ่งรายการที่ใช้กับพื้นที่ต้นทุนคอนเทนเนอร์การจัดส่ง ฟังก์ชันนี้รองรับโดยเอนทิตี `ITMLedgerJournalCostLinesContainersEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| ยอดเงินที่ปันส่วน | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | ไม่ | ไม่ |
| คอนเทนเนอร์การจัดส่ง | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **ใช่** | ไม่ |
| หมายเลขรายการธุรกรรมต้นทุน | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขรายการสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **ใช่** | ไม่ |
| การเดินทาง | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **ใช่** | ไม่ |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>การปันส่วนต้นทุนใบแจ้งรายการให้แก่ผู้จัดจำหน่าย (ITMLedgerJournalCostLinesFoliosEntity)

เอนทิตีข้อมูลการปันส่วนต้นทุนใบแจ้งรายการของผู้จัดจำหน่ายช่วยให้รายการใบแจ้งหนี้ของผู้จัดจำหน่ายสามารถปันส่วนในต้นทุนอย่างน้อยหนึ่งรายการที่ใช้กับพื้นที่ต้นทุนใบแจ้งรายการ ฟังก์ชันนี้รองรับโดยเอนทิตี `ITMLedgerJournalCostLinesFoliosEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| ยอดเงินที่ปันส่วน | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | ไม่ | ไม่ |
| หมายเลขรายการธุรกรรมต้นทุน | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| ใบแจ้งรายการ | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **ใช่** | ไม่ |
| หมายเลขรายการสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **ใช่** | ไม่ |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>การปันส่วนต้นทุนใบสั่งซื้อผู้จัดจำหน่าย (ITMLedgerJournalCostLinesPurchTableEntity)

เอนทิตีข้อมูลการปันส่วนต้นทุนใบสั่งซื้อของผู้จัดจำหน่ายช่วยให้รายการใบแจ้งหนี้ของผู้จัดจำหน่ายสามารถปันส่วนในต้นทุนอย่างน้อยหนึ่งรายการที่ใช้กับพื้นที่ต้นทุนใบสั่งซื้อ ฟังก์ชันนี้รองรับโดยเอนทิตี `ITMLedgerJournalCostLinesPurchTableEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| ยอดเงินที่ปันส่วน | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | ไม่ | ไม่ |
| หมายเลขรายการธุรกรรมต้นทุน | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขรายการสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **ใช่** | ไม่ |
| ใบสั่งซื้อ | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **ใช่** | ไม่ |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>การปันส่วนต้นทุนสินค้าของผู้จัดจำหน่าย (ITMLedgerJournalCostLinesPurchLineEntity)

เอนทิตีข้อมูลการปันส่วนต้นทุนสินค้าของผู้จัดจำหน่ายของผู้จัดจำหน่ายช่วยให้รายการใบแจ้งหนี้ของผู้จัดจำหน่ายสามารถปันส่วนในต้นทุนอย่างน้อยหนึ่งรายการที่ใช้กับพื้นที่ต้นทุนสินค้าของผู้จัดจำหน่าย พื้นที่ต้นทุนสินค้าครอบคลุมต้นทุนในรายการใบสั่งซื้อ ฟังก์ชันนี้รองรับโดยเอนทิตี `ITMLedgerJournalCostLinesPurchLineEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| ยอดเงินที่ปันส่วน | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | ไม่ | ไม่ |
| หมายเลขรายการธุรกรรมต้นทุน | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขรายการสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **ใช่** | ไม่ |
| ใบสั่งซื้อ | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **ใช่** | ไม่ |
| หมายเลขรายการใบสั่งซื้อ | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **ใช่** | ไม่ |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>การปันส่วนต้นทุนรายการใบสั่งโอนย้ายของผู้จัดจำหน่าย (ITMLedgerJournalCostLinesTransferLineEntity)

เอนทิตีข้อมูลการปันส่วนต้นทุนรายการใบสั่งโอนย้ายของผู้จัดจำหน่ายช่วยให้รายการใบแจ้งหนี้ของผู้จัดจำหน่ายสามารถปันส่วนในต้นทุนอย่างน้อยหนึ่งรายการที่ใช้กับพื้นที่ต้นทุนรายการการโอนย้าย ฟังก์ชันนี้รองรับโดยเอนทิตี `ITMLedgerJournalCostLinesTransferLineEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| ยอดเงินที่ปันส่วน | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | ไม่ | ไม่ |
| หมายเลขรายการธุรกรรมต้นทุน | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขรายการสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **ใช่** | ไม่ |
| หมายเลขสมุดรายวัน | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **ใช่** | ไม่ |
| ใบสั่งโอน | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **ใช่** | ไม่ |
| หมายเลขรายการใบสั่งโอนย้าย | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **ใช่** | ไม่ |

### <a name="reference-table"></a>ตารางอ้างอิง

รายการต้นทุนการเดินทางมีการเชื่อมโยงโดยตรงกับเรกคอร์ดธุรกรรมต้นทุน เรกคอร์ดนี้ประกอบด้วยค่า **รหัสตารางอ้างอิง** ค่านี้จะไม่ซ้ำกันต่อพื้นที่ต้นทุนแต่ละพื้นที่ (การเดินทาง คอนเทนเนอร์การขนส่ง และอื่นๆ) เมื่อมีการอ้างอิงหมายเลขตารางเฉพาะกับข้อมูลที่สร้างโดยใช้เอนทิตีข้อมูล เอนทิตีจะถูกแบ่งตามค่า **รหัสตารางอ้างอิง**

ค่าสำหรับตารางอ้างอิง (`RefTableId`) และชนิดธุรกรรม (`TransType`) จะเป็นแบบโดยนัยในการเลือกเอนทิตีรายการซื้อของต้นทุนแฝงหรือเอนทิตีรายการโอนย้ายต้นทุนแฝง

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>รายการสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่าย (VendorInvoiceJournalLineEntity)

ก่อนที่ค่ารายการสมุดรายวันจะสามารถปันส่วนให้กับต้นทุนหนึ่งรายการหรือมากกว่าในโมดูล **ต้นทุนแฝง** รายการสมุดรายวันต้องเชื่อมโยงกับพื้นที่ต้นทุน เพื่อสนับสนุนฟังก์ชันนี้ โมดูล **ต้นทุนแฝง** จะเพิ่มฟิลด์ใหม่บางฟิลด์ในตารางรายการสมุดรายวัน (`LedgerJournalTrans`)

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>ฟิลด์ที่เพิ่มในเอนทิตีรายการสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่าย

ตารางต่อไปนี้แสดงรายการฟิลด์ที่โมดูล **ต้นทุนแฝง** เพิ่มในเอนทิตีรายการสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่าย (`VendorInvoiceJournalLineEntity`) ฟิลด์เหล่านี้ช่วยให้ระบบสามารถสร้างรายการสมุดรายวันและปันส่วนต้นทุนเทียบกับรายการสมุดรายวันได้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| พื้นที่ต้นทุน | LedgerJournalTrans.ITMCostArea | Int | ไม่ | ไม่ |
| รหัสชนิดต้นทุน | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | ไม่ | ไม่ |

### <a name="mainoffset-account"></a>บัญชีหลัก/ตรงข้าม

บัญชีหลัก/บัญชีตรงข้ามของรายการสมุดรายวันใบแจ้งหนี้ที่เชื่อมโยงกับการเดินทางของต้นทุนแฝงจะกําหนดโดยรหัสชนิดต้นทุน เมื่อรหัสชนิดต้นทุนรวมอยู่ในรายการสมุดรายวันใบแจ้งหนี้ บัญชีรอการโอนจะถูกใช้เป็นบัญชีหลักหรือบัญชีตรงข้าม ทั้งนี้ขึ้นอยู่กับสถานการณ์ดังกล่าว

- **สมุดรายวันบรรทัดเดียว** – ถ้ากําหนดบัญชีหลัก (กล่าวอีกอย่างคือ บัญชีผู้จัดจำหน่าย) และระบุรหัสชนิดต้นทุนไว้ ค่าบัญชีรอการโอนสำหรับรหัสชนิดต้นทุนนั้นที่จะป้อนในบัญชีตรงข้าม
- **สมุดรายวันหลายบรรทัด** – ถ้าไม่ได้กําหนดบัญชีหลัก แต่ระบุรหัสชนิดต้นทุนไว้ ค่าบัญชีรอการโอนสำหรับรหัสชนิดต้นทุนนั้นที่จะป้อนในบัญชีหลัก รายการสมุดรายวันที่ให้เครดิตผู้จัดจำหน่ายจะไม่อ้างอิงรหัสชนิดต้นทุน

## <a name="sequencing"></a>การจัดลำดับ

เนื่องจากความเชื่อมโยงกันระหว่างตารางบรรทัดสมุดรายวันและสมุดรายวัน คุณต้องสร้างเรกคอร์ดการเดินทางก่อน บรรทัดการเดินทางสามารถสร้างขึ้นได้เฉพาะหลังจากการเดินทาง คอนเทนเนอร์ขนส่ง และใบแจ้งรายการได้ถูกสร้างขึ้นแล้วเท่านั้น

เมื่อต้องการปันส่วนใบแจ้งหนี้การเดินทาง ระบบต้องประมวลผลเอนทิตีตามลำดับดังนี้

1. ส่วนหัวของสมุดรายวันใบแจ้งหนี้ (`VendInvoiceJournalHeaderEntity`)
1. รายการสมุดรายวันใบแจ้งหนี้ (`VendInvoiceJournalLineEntity`)
1. การปันส่วนต้นทุนแฝง (`ITMLedgerJournalEntities`)
