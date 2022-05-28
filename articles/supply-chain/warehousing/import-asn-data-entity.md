---
title: นําเข้า ASN ขาเข้าผ่านเอนทิตี้ข้อมูล V3
description: หัวข้อนี้อธิบายวิธีการจัดการนําเข้าประกาศการจัดส่งสินค้าขั้นสูงขาเข้า (ASN) โดยผ่านเอนทิตีข้อมูล ASN ขาเข้า
author: GalynaFedorova
ms.date: 05/11/2022
ms.topic: article
ms.search.form: WHSInboundASNV3Entity, WHSInboundASNEntity, DMFEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 44ec0230236451a413d483b3e9f3ddc58b49a0b0
ms.sourcegitcommit: 90ffd763d18f97654b9dbc9e3f71c998e6094c6b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740146"
---
# <a name="import-inbound-asns-through-the-v3-data-entity"></a>นําเข้า ASN ขาเข้าผ่านเอนทิตี้ข้อมูล V3

[!include [banner](../../includes/banner.md)]

การแจ้งเตือนการจัดส่งขั้นสูง (ASN) จะแจ้งให้ทราบเกี่ยวกับการจัดส่งสินค้าของผู้จัดจำหน่าย ซึ่งช่วยให้ผู้ส่งอธิบายถึงเนื้อหาของการจัดส่งสินค้าและข้อมูลเพิ่มเติมเกี่ยวกับการจัดส่งสินค้า เช่น สินค้าและบรรจุภัณฑ์

ASN สามารถช่วยให้พนักงานคลังสินค้าทราบถึงสิ่งที่มาถึง ดังนั้นจึงสามารถจัดเตรียมได้ นอกจากนี้ พนักงานคลังสินค้าสามารถใช้ ASN เพื่อจับคู่รายละเอียดของการจัดส่งกับใบสั่งซื้อที่เกี่ยวข้องที่สร้างขึ้นก่อนหน้านี้ได้

หัวข้อนี้จะแสดงถึงชุดของสถานการณ์จำลองที่แสดง โดยผ่านตัวอย่าง วิธีการทำงานกับไฟล์ ASN

> [!IMPORTANT]
> การนําเข้า *ASN ขาเข้า* จะใช้กับสินค้าที่เปิดใช้งานเฉพาะกับการจัดการคลังสินค้าขั้นสูง (WMS) เท่านั้น ก่อนที่คุณจะได้รับ ASN ต้องมีการลงทะเบียนใบสั่งซื้อในระบบกับผู้จัดจำหน่ายที่ส่ง ASN นั้นไป

## <a name="inbound-asn-v3-entity"></a>เอนทิตี ASN V3 ขาเข้า

คุณนําเข้า ASN ขาเข้าโดยใช้เอนทิตีข้อมูลแบบรวม *ASN V3 ขาเข้า* *ASN V3 ขาเข้า* ใช้ประโยชน์จากเอนทิตีต่อไปนี้

- ส่วนหัวของการบรรทุกขาเข้า
- ส่วนหัวของการจัดส่งขาเข้า
- โครงสร้างการบรรจุโหลดขาเข้า
- กล่องโครงสร้างการบรรจุโหลดขาเข้า
- รายการกล่องโครงสร้างการบรรจุโหลดขาเข้า
- รายการโครงสร้างการบรรจุโหลดขาเข้า

เอนทิตีข้อมูลแบบรวม *ASN V3 ขาเข้า* ที่ใช้กับสถานการณ์การรวมแบบอสมวารซึ่งใช้การนําเข้าโดยใช้ไฟล์ XML

## <a name="xml-format-for-importing-asns"></a>รูปแบบ XML สำหรับการนําเข้า ASN

Microsoft Dynamics 365 Supply Chain Management สนับสนุนรูปแบบ XML ต่อไปนี้เพื่อนําเข้า ASN แต่ละโหนดในไฟล์ XML แสดงถึงแอททริบิวต์จากแต่ละเอนทิตี

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV3Entity>
                    </WHSInboundPackingStructureCaseLineV3Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV3Entity>
                </WHSInboundLoadPackingStructureLineV3Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>ตัวอย่างเช่น

ส่วนย่อยต่อไปนี้แสดงตัวอย่างไฟล์นําเข้า ASN XML ของการจัดส่งของผู้จัดจำหน่าย

### <a name="example-1"></a>ตัวอย่างที่ 1

ตัวอย่างต่อไปนี้แสดงไฟล์ XML ในการนําเข้าการจัดส่งของผู้จัดจำหน่ายในใบสั่งซื้อใบเดียวเมื่อไม่มีรายละเอียดกรณีรวมอยู่ด้วย

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>ตัวอย่างที่ 2

ตัวอย่างต่อไปนี้แสดงไฟล์ XML ในการนําเข้าการจัดส่งของผู้จัดจำหน่ายในใบสั่งซื้อใบเดียวเมื่อมีรายละเอียดกรณีรวมอยู่ด้วย

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLine3Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>ตัวอย่างที่ 3

ตัวอย่างต่อไปนี้แสดงไฟล์ XML ในการนําเข้าการจัดส่งของผู้จัดจำหน่ายในใบสั่งซื้อหลายใบเมื่อมีรายละเอียดกรณีรวมอยู่ด้วย

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>ตรวจสอบผลลัพธ์ของการนําเข้าไฟล์ ASN

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตรวจสอบผลลัพธ์ของการนําเข้าไฟล์ ASN

1. ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**
1. ค้นหาและเปิดโหลดที่สร้างเป็นส่วนหนึ่งของการนําเข้า ASN
1. บนแท็บด่วน **โหลด** คุณควรจะเห็นค่าที่ขึ้นอยู่กับไฟล์ XML
1. บนแท็บด่วน **รายการสินค้า** คุณควรจะเห็นหมายเลขใบสั่งซื้อและรายละเอียดสินค้าที่ขึ้นอยู่กับไฟล์ XML
1. ในบานหน้าต่างการดำเนินการ บนแท็บ **จัดส่งและรับ** ในกลุ่ม **การรับ** ให้เลือก **โครงสร้างการบรรจุ** เพื่อตรวจสอบโครงสร้างการบรรจุของปริมาณงาน
1. บนแท็บด่วน **แท่นวางสินค้า** คุณควรจะเห็นป้ายทะเบียนที่ขึ้นอยู่กับไฟล์ XML
1. บนแท็บด่วน **กรณี** คุณควรจะเห็นกรณีที่ขึ้นอยู่กับไฟล์ XML
1. บนแท็บด่วน **สินค้า** คุณควรจะเห็นสินค้าและปริมาณที่ขึ้นอยู่กับไฟล์ XML

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
