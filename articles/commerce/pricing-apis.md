---
title: API การกําหนดราคาพาณิชย์
description: บทความนี้จะอธิบาย API การกำหนดราคาต่างๆ ที่ให้ไว้โดยกลไกจัดการการกำหนดราคาของ Microsoft Dynamics 365 Commerce
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294134"
---
# <a name="commerce-pricing-apis"></a>API การกําหนดราคาพาณิชย์

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบาย API การกำหนดราคาต่างๆ ที่ให้ไว้โดยกลไกจัดการการกำหนดราคาของ Microsoft Dynamics 365 Commerce

กลไกจัดการการกำหนดราคาของ Dynamics 365 Commerce มี API ของ Retail Server ต่อไปนี้ที่แอปพลิเคชันภายนอกสามารถใช้เพื่อสนับสนุนสถานการณ์การกําหนดราคาต่างๆ ได้

- **GetActivePrices** – API นี้จะได้รับราคาที่คํานวณได้ของผลิตภัณฑ์ รวมทั้งส่วนลดแบบง่าย
- **CalculateSalesDocument** – API นี้จะคํานวณราคาและส่วนลดต่อผลิตภัณฑ์ที่ปริมาณที่มอบ หากมีการซื้อพร้อมกัน
- **GetAvailablePromotions** – API นี้จะมีส่วนลดที่ใช้ได้กับผลิตภัณฑ์ในรถเข็น 
- **AddCoupons** – API นี้เพิ่มคูปองลงในรถเข็น
- **RemoveCoupons** – API นี้จะลบคูปองออกจากรถเข็น

หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้ API ของ Retail Server ในแอปพลิเคชันภายนอก โปรดดูที่ [การใช้ API ของ Retail Server ในแอปพลิเคชันภายนอก](dev-itpro/consume-retail-server-api.md)

## <a name="getactiveprices"></a>GetActivePrices

API *GetActivePrices* มีการใช้งานใน Commerce รุ่น 10.0.4 API นี้จะได้รับราคาที่คํานวณได้ของผลิตภัณฑ์ รวมทั้งส่วนลดแบบง่าย ซึ่งไม่ได้คํานวณส่วนลดต่อสินค้าหลายรายการ และสันนิษฐานว่าผลิตภัณฑ์แต่ละรายการในคำขอ API มีปริมาณเป็น 1 API นี้ยังสามารถใช้รายการผลิตภัณฑ์เป็นอินพุทและสอบถามราคาของผลิตภัณฑ์แต่ละรายการเป็นกลุ่ม

API *GetActivePrices* สนับสนุนบทบาทการค้าของ **พนักงาน** **ลูกค้า** **การไม่ระบุชื่อ** และ **แอปพลิเคชัน**

กรณีการใช้หลัก API *GetActivePrices* คือหน้ารายละเอียดผลิตภัณฑ์ (PDP) ซึ่งผู้ค้าปลีกต้องการแสดงราคาที่ดีที่สุดให้กับผลิตภัณฑ์ รวมถึงส่วนลดใดๆ ที่มีผลบังคับ

ตารางต่อไปนี้แสดงพารามิเตอร์อินพุทของ API *GetActivePrices*

| ชื่อ                                    | ชื่อย่อย | ชนิด | จำเป็น/ไม่บังคับ | คำอธิบาย |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | ต้องระบุ | |
|                                         | ChannelId | ยาว | ต้องระบุ | |
|                                         | CatalogId | ยาว | ต้องระบุ | |
| productIds                              | | IEnumerable\<long\> | ต้องระบุ | รายการของผลิตภัณฑ์ที่จะคํานวณราคา |
| activeDate                              | | DateTimeOffset | ต้องระบุ | วันที่ที่คํานวณราคา |
| customerId                              | | สตริง | ไม่จำเป็นต้องระบุ | หมายเลขรหัสลูกค้า |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | ไม่จำเป็นต้องระบุ | ระดับการเข้าร่วมและความภักดี |
|                                         | AffiliationId | ยาว | ต้องระบุ | รหัสสังกัด |
|                                         | LoyaltyTierId | ยาว | ไม่จำเป็นต้องระบุ | รหัสระดับสมาชิก |
| includeSimpleDiscountsInContextualPrice | | ค่าบูลีน | ไม่จำเป็นต้องระบุ | ตั้งค่าพารามิเตอร์นี้เป็น **จริง** เพื่อรวมส่วนลดแบบง่ายในการคํานวณการกําหนดราคา ค่าเริ่มต้นคือ **เท็จ** |
| includeVariantPriceRange                | | ค่าบูลีน | ไม่จำเป็นต้องระบุ | ตั้งค่าพารามิเตอร์นี้เป็น **จริง** เพื่อให้ได้ราคาต่ำสุดและสูงสุดระหว่างผลิตภัณฑ์ย่อยทั้งหมดของผลิตภัณฑ์หลัก ค่าเริ่มต้นคือ **เท็จ** |
| includeAttainablePricesAndDiscounts     | | ค่าบูลีน | ไม่จำเป็นต้องระบุ | ตั้งค่าพารามิเตอร์นี้เป็น **จริง** เพื่อให้ได้ราคาและส่วนลดที่บรรลุได้ ค่าเริ่มต้นคือ **เท็จ** |

**เนื้อหาคำขอตัวอย่าง**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**เนื้อความการตอบกลับตัวอย่าง**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

API *CalculateSalesDocument* มีการใช้งานใน Commerce รุ่น 10.0.25 API นี้จะคํานวณราคาและส่วนลดต่อผลิตภัณฑ์ที่ปริมาณที่มอบ หากมีการซื้อพร้อมกันตามลำดับ การคํานวณการกําหนดราคาที่อยู่หลัง API ของ *CalculateSalesDocument* จะพิจารณาทั้งส่วนลดต่อรายการสินค้าเดียวและส่วนลดต่อรายการสินค้าหลายบรรทัด

กรณีการใช้หลักใน API ของ *CalculateSalesDocument* คือการคํานวณการกําหนดราคาในสถานการณ์ที่บริบทรถเข็นทั้งหมดจะไม่ยังคงอยู่ (เช่น ใบเสนอราคาขาย) สถานการณ์สมทบในการขายหน้าร้าน (POS) และพาณิชย์ e-commerce ยังสามารถได้รับประโยชน์จากกรณีการใช้งานนี้ด้วย ราคารวมที่ต่ำกว่าเมื่อมีการคํานวณสินค้าในรถเข็นเป็นชุด (ตัวอย่างเช่น เพื่อแยกกลุ่ม ผลิตภัณฑ์ที่เชื่อมโยงหรือผลิตภัณฑ์ที่แนะนำ หรือผลิตภัณฑ์ที่แนะนำซึ่งถูกเพิ่มลงในรถเข็นแล้ว) อาจออกลูกค้าใหม่เพื่อเพิ่มผลิตภัณฑ์ลงในรถเข็น

รูปแบบข้อมูลของทั้งคำขอและการตอบสนองของ API *CalculateSalesDocument* คือ **รถเข็น** อย่างไรก็ตาม ในบริบทของ API นี้ แบบโมเดลข้อมูลจะตั้งชื่อเป็น **SalesDocument** เนื่องจากคุณสมบัติส่วนใหญ่จะเป็นตัวเลือก และมีเพียงสองสามอย่างเท่านั้นที่มีผลกระทบต่อการคํานวณการกําหนดราคา ฟิลด์ที่เกี่ยวข้องกับการกําหนดราคาเท่านั้นจะแสดงอยู่ในตารางต่อไปนี้ เราไม่แนะนำให้ฟิลด์อื่นๆ เกี่ยวข้องกับคำขอ API

ขอบเขตของ API *CalculateSalesDocument* คือเพียงการคํานวณราคาและส่วนลดเท่านั้น ภาษีและค่าธรรมเนียมไม่เกี่ยวข้อง

ตารางต่อไปนี้แสดงพารามิเตอร์อินพุทภายในออบเจ็กต์ที่ชื่อ **salesDocument**

| ชื่อ             | ชื่อย่อย | ชนิด | จำเป็น/ไม่บังคับ | คำอธิบาย |
|------------------|----------|------|-------------------|-------------|
| รหัส               | | สตริง | ต้องระบุ | รหัสของเอกสารการขาย |
| CartLines        | | IList\<CartLine\> | ไม่จำเป็นต้องระบุ | รายการของบรรทัดที่จะคํานวณราคาและส่วนลด |
|                  | รหัสผลิตภัณฑ์ | ยาว | ต้องใช้ในขอบเขตของ CartLine | รหัสเรกคอร์ดผลิตภัณฑ์ |
|                  | ItemId | สตริง | ไม่จำเป็นต้องระบุ | ตัวระบุสินค้า ถ้ามีการระบุค่า ค่าต้องตรงกับค่าของพารามิเตอร์ **ProductId** |
|                  | InventoryDimensionId | สตริง | ไม่จำเป็นต้องระบุ | ตัวระบุมิติสินค้าคงคลัง หากมีการระบุค่า ชุดค่า **ItemId** และ **InventoryDimensionId** ต้องตรงกับค่าของพารามิเตอร์ **ProductId** |
|                  | ปริมาณ | ทศนิยม | ต้องใช้ในขอบเขตของ CartLine | ปริมาณของสินค้า |
|                  | UnitOfMeasureSymbol | สตริง | ไม่จำเป็นต้องระบุ | หน่วยของผลิตภัณฑ์ ตามค่าเริ่มต้น ถ้าไม่ได้แสดงค่า API จะใช้หน่วยการขายของผลิตภัณฑ์ |
| CustomerId       | | สตริง | ไม่จำเป็นต้องระบุ | หมายเลขรหัสลูกค้า |
| LoyaltyCardId    | | สตริง | ไม่จำเป็นต้องระบุ | ตัวระบุบัตรสมาชิก บัญชีลูกค้าใดๆ ที่เชื่อมโยงกับบัตรสมาชิกต้องตรงกับค่าของพารามิเตอร์ **CustomerId** (ถ้ามีให้ไว้) จะไม่พิจารณาบัตรสมาชิกถ้าไม่พบหรือสถานะบัตรสมาชิก **ถูกบล็อค** |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | ไม่จำเป็นต้องระบุ | ระดับการเข้าร่วมบัตรสมาชิก หากมีค่า **CustomerId** และ/หรือ **LoyaltyCardId** รายการระดับสมาชิกที่เกี่ยวข้องจะถูกรวมกับรายการที่ระบุในค่า **AffiliationLines** |
|                  | AffiliationId | ยาว | ต้องใช้ในขอบเขตของ AffiliationLoyaltyTier | รหัสเรกคอร์ดสังกัด |
|                  | LoyaltyTierId | ยาว | ต้องใช้ในขอบเขตของ AffiliationLoyaltyTier | รหัสเรกคอร์ดระดับสมาชิก |
|                  | AffiliationTypeValue | int | ต้องใช้ในขอบเขตของ AffiliationLoyaltyTier | ค่าที่ระบุว่ารายการสังกัดเป็นชนิด **ทั่วไป** (**0**) หรือชนิด **สมาชิก** (**1**) ถ้าพารามิเตอร์นี้ถูกตั้งค่าเป็น **0** API จะรับค่า **AffiliationId** เป็นตัวระบุและละเว้นค่า **LoyaltyTierId** ถ้าพารามิเตอร์นี้ถูกตั้งค่าเป็น **1** API จะรับค่า **LoyaltyTierId** เป็นตัวระบุและละเว้นค่า **AffiliationId** |
|                  | ReasonCodeLines | คอลเลกชัน\<ReasonCodeLine\> | ต้องใช้ในขอบเขตของ AffiliationLoyaltyTier | รายการรหัสเหตุผล พารามิเตอร์นี้จะไม่มีผลกระทบต่อการคํานวณการกําหนดราคา แต่เป็นพารามิเตอร์ที่บังคับโดยเป็นส่วนหนึ่งของออบเจ็กต์ **AffiliationLoyaltyTier** |
|                  | CustomerId | สตริง | ต้องใช้ในขอบเขตของ AffiliationLoyaltyTier | หมายเลขรหัสลูกค้า |
| คูปอง          | | IList\<Coupon\> | ไม่จำเป็นต้องระบุ | คูปองที่ใช้ไม่ได้ (ไม่ได้ใช้งาน หมดอายุ หรือหาไม่พบ) จะไม่ได้รับการพิจารณาในการคํานวณการกําหนดราคา |
|                  | รหัส | สตริง | ต้องใช้ในขอบเขตของ Coupon | รหัสคูปอง |
|                  | CodeId | สตริง | ไม่จำเป็นต้องระบุ | ตัวระบุรหัสคูปอง ถ้ามีการระบุค่า ค่าต้องตรงกับค่าของพารามิเตอร์ **Code** |
|                  | DiscountOfferId | สตริง | ไม่จำเป็นต้องระบุ | รหัสส่วนลด ถ้ามีการระบุค่า ค่าต้องตรงกับค่าของพารามิเตอร์ **Code** |

**เนื้อหาคำขอตัวอย่าง**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

ออบเจ็กต์รถเข็นทั้งหมดจะถูกส่งคืนเป็นเนื้อหาการตอบสนอง ในการตรวจสอบราคาและส่วนลด คุณควรโฟกัสที่ฟิลด์ในตารางต่อไปนี้

| ชื่อ           | ชื่อย่อย | ชนิด | คำอธิบาย |
|----------------|----------|------|--------------|
| NetPrice       | | ทศนิยม | ราคาสุทธิของเอกสารการขายทั้งหมดก่อนที่จะใช้ส่วนลด |
| DiscountAmount | | ทศนิยม | ยอดส่วนลดรวมของเอกสารการขายทั้งหมด |
| TotalAmount    | | ทศนิยม | ยอดรวมของเอกสารการขายทั้งหมด |
| CartLines      | | IList\<CartLine\> | บรรทัดที่คํานวณได้ที่รวมรายละเอียดราคาและส่วนลด |
|                | ราคา | ทศนิยม | ราคาต่อหน่วยของผลิตภัณฑ์ |
|                | NetPrice | ทศนิยม | ราคาสุทธิของรายการก่อนที่จะใช้ส่วนลด (= *ราคา* &times; *ปริมาณ*) |
|                | DiscountAmount | ทศนิยม | ยอดส่วนลด |
|                | TotalAmount | ทศนิยม | ผลลัพธ์การกําหนดราคารวมสุดท้ายของรายการ |
|                | PriceLines | IList\<PriceLine\> | รายละเอียดราคา รวมทั้งแหล่งที่มาของราคา (ราคาพื้นฐาน การปรับปรุงราคา หรือข้อตกลงทางการค้า) และยอดเงิน |
|                | DiscountLines | IList\<DiscountLine\> | รายละเอียดส่วนลด |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

รถเข็นที่มีรายการรถเข็นหลายรายการ API *GetAvailablePromotions* จะส่งคืนส่วนลดที่เกี่ยวข้องทั้งหมดต่อรายการรถเข็น 

กรณีการใช้หลักใน API *GetAvailablePromotions* คือหน้ารถเข็น ผู้ค้าปลีกต้องการใช้ส่วนลดหรือคูปองที่มีอยู่ของรถเข็นปัจจุบัน

ตารางต่อไปนี้แสดงพารามิเตอร์อินพุทของ API *GetAvailablePromotions*

| ชื่อ        | ชนิด | จำเป็น/ไม่บังคับ | คำอธิบาย |
|-------------|------|-------------------|-------------|
| คีย์         | สตริง | ต้องระบุ | รหัสรถเข็น |
| cartLineIds | IEnumerable\<string\> | ไม่จำเป็นต้องระบุ | ตั้งค่าพารามิเตอร์เพื่อส่งคืนส่วนลดต่อรายการในรถเข็นที่เลือกเท่านั้น |

**เนื้อความการตอบกลับตัวอย่าง**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

API *AddCoupons* สนับสนุนการเพิ่มรายการคูปองลงในรถเข็น ส่งคืนออบเจ็กต์รถเข็นหลังจากที่เพิ่มคูปอง

ตารางต่อไปนี้แสดงพารามิเตอร์อินพุทของ API *AddCoupons*

| ชื่อ                 | ชนิด | จำเป็น/ไม่บังคับ | คำอธิบาย |
|----------------------|------|-------------------|-------------|
| คีย์                  | สตริง | ต้องระบุ | รหัสรถเข็น |
| couponCodes          | IEnumerable\<string\> | ต้องระบุ | รหัสคูปองที่จะเพิ่มลงในรถเข็น |
| isLegacyDiscountCode | ค่าบูลีน | ไม่จำเป็นต้องระบุ | ตั้งค่าพารามิเตอร์นี้เป็น **จริง** เพื่อบ่งชี้ว่าคูปองเป็นรหัสส่วนลดที่สืบทอดมา ค่าเริ่มต้นคือ **เท็จ** |

## <a name="removecoupons"></a>RemoveCoupons

API *RemoveCoupons* สนับสนุนการลบรายการคูปองออกจากรถเข็น ส่งคืนออบเจ็กต์รถเข็นหลังจากที่ลบคูปอง

ตารางต่อไปนี้แสดงพารามิเตอร์อินพุทของ API *RemoveCoupons*

| ชื่อ        | ชนิด | จำเป็น/ไม่บังคับ | คำอธิบาย |
|-------------|------|-------------------|-------------|
| คีย์         | สตริง | ต้องระบุ | รหัสรถเข็น |
| couponCodes | IEnumerable\<string\> | ต้องระบุ | รหัสคูปองที่จะลบออกจากรถเข็น |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
