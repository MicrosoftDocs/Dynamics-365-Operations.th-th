---
title: การตั้งค่าคอนฟิกการแสดงผลสินค้าคงคลัง
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกการแสดงผลสินค้าคงคลัง
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345044"
---
# <a name="inventory-visibility-configuration"></a>การตั้งค่าคอนฟิกการแสดงผลสินค้าคงคลัง

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกการแสดงผลสินค้าคงคลัง

## <a name="introduction"></a><a name="introduction"></a>บทนำ

ก่อนที่คุณจะเริ่มต้นใช้งานการแสดงผลสินค้าคงคลัง คุณต้องทำการตั้งค่าคอนฟิกต่อไปนี้ให้เสร็จสมบูรณ์ตามที่อธิบายไว้ในหัวข้อนี้:

- [การตั้งค่าคอนฟิกแหล่งข้อมูล](#data-source-configuration)
- [การตั้งค่าคอนฟิกพาร์ติชัน](#partition-configuration)
- [การตั้งค่าคอนฟิกตามลำดับชั้นของดัชนีผลิตภัณฑ์](#index-configuration)
- [การตั้งค่าคอนฟิกการจอง (ไม่จำเป็นต้องระบุ)](#reservation-configuration)
- [ตัวอย่างการตั้งค่าคอนฟิกเริ่มต้น](#default-configuration-sample)

> [!NOTE]
> คุณสามารถดูและแก้ไขการตั้งค่าคอนฟิกการแสดงผลสินค้าคงคลังใน [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration) หลังจากที่การตั้งค่าคอนฟิกเสร็จสิ้น ให้เลือก **อัพเดตการตั้งค่าคอนฟิก** ในแอป

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>การตั้งค่าคอนฟิกแหล่งข้อมูล

แหล่งข้อมูลแสดงถึงระบบที่เป็นที่มาของข้อมูลของคุณ ตัวอย่างได้แก่ `fno` (ซึ่งหมายถึง "แอป Dynamics 365 Finance and Operations") และ `pos` (ซึ่งหมายถึง "การขายหน้าร้าน")

การตั้งค่าคอนฟิกแหล่งข้อมูลประกอบด้วยส่วนต่อไปนี้:

- มิติ (การแม็ปมิติ)
- การวัดทางกายภาพ
- การวัดที่คำนวณ

> [!NOTE]
> แหล่งข้อมูล `fno` ถูกจองสำหรับ Dynamics 365 Supply Chain Management

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>มิติ (การแม็ปมิติ)

วัตถุประสงค์ของการตั้งค่าคอนฟิกมิติคือ การกำหนดมาตรฐานการรวมหลายระบบสำหรับการลงรายการบัญชีเหตุการณ์และการสอบถาม โดยยึดตามชุดมิติ

การแสดงผลสินค้าคงคลังสนับสนุนมิติพื้นฐานทั่วไปต่อไปนี้

| ชนิดมิติ | มิติพื้นฐาน |
|---|---|
| สินค้า | `ColorId` |
| สินค้า | `SizeId` |
| สินค้า | `StyleId` |
| สินค้า | `ConfigId` |
| การติดตาม | `BatchId` |
| การติดตาม | `SerialId` |
| ที่ตั้ง | `LocationId` |
| ที่ตั้ง | `SiteId` |
| สถานะของสินค้าคงคลัง | `StatusId` |
| คลังสินค้าเฉพาะ | `WMSLocationId` |
| คลังสินค้าเฉพาะ | `WMSPalletId` |
| คลังสินค้าเฉพาะ | `LicensePlateId` |
| อื่นๆ | `VersionId` |
| สินค้าคงคลัง (แบบกำหนดเอง) | `InventDimension1` ผ่าน `InventDimension12` |
| เบอร์ต่อ | `ExtendedDimension1` ผ่าน `ExtendedDimension8` |

> [!NOTE]
> ชนิดของมิติที่แสดงรายการอยู่ในตารางก่อนหน้านี้ใช้สำหรับการอ้างอิงเท่านั้น คุณไม่ต้องกําหนดรายการเหล่านั้นในการแสดงผลสินค้าคงคลัง
>
> มิติสินค้าคงคลัง (แบบกำหนดเอง) อาจถูกจองไว้สำหรับ Supply Chain Management ในกรณีดังกล่าว คุณสามารถใช้มิติแบบขยายแทนได้

ระบบภายนอกสามารถเข้าถึงการแสดงผลสินค้าคงคลังผ่าน RESTful APIs สำหรับการรวม การแสดงผลสินค้าคงคลังช่วยให้คุณสามารถตั้งค่าคอนฟิก _แหล่งข้อมูลภายนอก_ และการแม็ปจาก _มิติภายนอก_ ไปยัง _มิติพื้นฐาน_ นี่เป็นตัวอย่างของตารางการแม็ปมิติ

| มิติภายนอก | มิติพื้นฐาน |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

โดยการตั้งค่าคอนฟิกการแม็ปมิติ คุณสามารถส่งมิติภายนอกไปยังการแสดงผลสินค้าคงคลังโดยตรงได้ จากนั้น การแสดงผลสินค้าคงคลังจะแปลงมิติภายนอกเป็นมิติพื้นฐานโดยอัตโนมัติ

### <a name="physical-measures"></a>การวัดทางกายภาพ

การวัดทางกายภาพจะปรับเปลี่ยนปริมาณและสะท้อนสถานะของสินค้าคงคลัง คุณสามารถกําหนดการวัดทางกายภาพของคุณเองได้ตามความต้องการของคุณ

การแสดงผลสินค้าคงคลังจะแสดงรายการของการวัดทางกายภาพเริ่มต้นที่เชื่อมโยงกับ Supply Chain Management (แหล่งข้อมูล `fno`) ตารางต่อไปนี้แสดงตัวอย่างของการวัดทางกายภาพ

| ชื่อการวัดทางกายภาพ | คำอธิบาย |
|---|---|
| `NotSpecified` | ไม่ได้ระบุ |
| `Arrived` | มาถึงแล้ว |
| `AvailOrdered` | ปริมาณที่สั่งแล้ว |
| `AvailPhysical` | ที่มีอยู่จริง |
| `Deducted` | หักบัญชี |
| `OnOrder` | OnOrder |
| `Ordered` | ที่สั่งไว้ |
| `PhysicalInvent` | สินค้าคงคลังที่มีอยู่จริง |
| `Picked` | รับสินค้าแล้ว |
| `PostedQty` | ปริมาณที่ลงรายการบัญชี |
| `QuotationIssue` | ออกใช้ใบเสนอราคา |
| `QuotationReceipt` | การรับใบเสนอราคา |
| `Received` | ที่ได้รับ |
| `Registered` | ลงทะเบียนแล้ว |
| `ReservOrdered` | สำรองตามใบสั่งแล้ว |
| `ReservPhysical` | ที่จองจริง |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>การวัดที่มีการคำนวณ

การวัดที่มีการคํานวณจะให้สูตรการคํานวณที่ปรับแต่งซึ่งประกอบด้วยชุดของการวัดทางกายภาพ ฟังก์ชันนี้จะช่วยให้คุณสามารถกำหนดชุดของการวัดทางกายภาพที่จะถูกเพิ่ม และ/หรือ ชุดของการวัดทางกายภาพที่จะถูกลบ เพื่อสร้างการวัดที่กำหนดเอง

ตัวอย่างเช่น คุณมีผลลัพธ์การสอบถามต่อไปนี้

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

จากนั้น คุณตั้งค่าคอนฟิกการวัดที่มีการคํานวณที่ชื่อว่า `MyCustomAvailableforReservation` ตามที่แสดงไว้ในตารางต่อไปนี้ การวัดที่มีการคํานวณนี้จะถูกใช้โดยระบบปริมาณการใช้

| ระบบปริมาณการใช้วัสดุ | การวัดที่คำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ | ชนิดการคำนวณ |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

เมื่อมีการใช้สูตรการคำนวณนี้ ผลลัพธ์การสอบถามใหม่จะรวมการวัดที่กำหนดเอง

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

ผลลัพธ์ `MyCustomAvailableforReservation` ที่ขึ้นอยู่กับการตั้งค่าการคำนวณในการวัดที่กำหนดเองคือ 100 + 50 + 80 + 90 + 30 – 10 – 20 – 60 – 40 = 220

## <a name="partition-configuration"></a><a name="partition-configuration"></a>การตั้งค่าคอนฟิกพาร์ติชัน

การตั้งค่าคอนฟิกพาร์ติชันประกอบด้วยชุดของมิติพื้นฐาน โดยจะกําหนดรูปแบบการกระจายข้อมูล การดําเนินงานข้อมูลในพาร์ติชันเดียวกันสนับสนุนประสิทธิภาพระดับสูง และไม่ต้องใช้ต้นทุนมากเกินไป ดังนั้น รูปแบบพาร์ติชันที่ดีจึงสามารถจัดสรรประโยชน์ที่สําคัญได้

การแสดงผลสินค้าคงคลังมีการตั้งค่าคอนฟิกพาร์ติชันเริ่มต้นต่อไปนี้

| มิติพื้นฐาน | ลำดับชั้น |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> การตั้งค่าคอนฟิกพาร์ติชันเริ่มต้นใช้สำหรับการอ้างอิงเท่านั้น คุณไม่ต้องกําหนดในการแสดงผลสินค้าคงคลัง ในปัจจุบัน ไม่สนับสนุนการอัพเกรดการตั้งค่าคอนฟิกพาร์ติชัน

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>การตั้งค่าคอนฟิกตามลำดับชั้นของดัชนีผลิตภัณฑ์

ส่วนใหญ่แล้ว การสอบถามปริมาณคงคลังคงเหลือจะไม่อยู่ที่ระดับ "รวม" สูงสุดเท่านั้น แต่คุณยังอาจต้องการดูผลลัพธ์ที่ถูกรวมตามมิติสินค้าคงคลังด้วย

การแสดงผลสินค้าคงคลังช่วยให้คุณมีความยืดหยุ่นได้โดยการอนุญาตให้คุณตั้งค่า _ดัชนี_ ดัชนีเหล่านี้จะขึ้นอยู่กับมิติหรือชุดของมิติ ดัชนีประกอบด้วย *หมายเลขชุด* *มิติ* และ *ลำดับชั้น* ตามที่กําหนดไว้ในตารางต่อไปนี้

| ชื่อ | คำอธิบาย |
|---|---|
| หมายเลขชุด | มิติที่เป็นของชุดเดียวกัน (ดัชนี) จะถูกจัดกลุ่มเข้าด้วยกัน และจะมีการปันส่วนหมายเลขชุดเดียวกันให้แก่มิติเหล่านั้น |
| มิติ | มิติพื้นฐานที่มีการรวมผลลัพธ์การสอบถาม |
| ลำดับชั้น | ลำดับชั้นถูกใช้ในการกําหนดชุดมิติที่สนับสนุนที่สามารถสอบถามได้ ตัวอย่างเช่น คุณตั้งค่าชุดมิติที่มีลำดับในลำดับชั้นเป็น `(ColorId, SizeId, StyleId)` ในกรณีนี้ ระบบจะสนับสนุนการสอบถามในชุดมิติสี่ชุด ชุดแรกว่างเปล่า ชุดที่สองคือ `(ColorId)` ชุดที่สามคือ `(ColorId, SizeId)` และชุดที่สี่คือ `(ColorId, SizeId, StyleId)` ระบบไม่สนับสนุนชุดข้อมูลอื่นๆ สำหรับข้อมูลเพิ่มเติม โปรดดูตัวอย่างต่อไปนี้ |

### <a name="example"></a>ตัวอย่าง

ส่วนนี้จะแสดงตัวอย่างที่แสดงวิธีการที่ลำดับชั้นทำงาน

คุณมีสินค้าต่อไปนี้ในสินค้าคงคลังของคุณ

| สินค้า | ColorId | SizeId | StyleId | ปริมาณ |
|---|---|---|---|---|
| เสื้อยืดคอกลม | สีดำ | ขนาดเล็ก | กว้าง | 1 |
| เสื้อยืดคอกลม | สีดำ | ขนาดเล็ก | เป็นประจำ | 2 |
| เสื้อยืดคอกลม | สีดำ | ใหญ่ | กว้าง | 3 |
| เสื้อยืดคอกลม | สีดำ | ใหญ่ | เป็นประจำ | 4 |
| เสื้อยืดคอกลม | สีแดง | ขนาดเล็ก | กว้าง | 5 |
| เสื้อยืดคอกลม | สีแดง | ขนาดเล็ก | เป็นประจำ | 6 ชั่วโมง |
| เสื้อยืดคอกลม | สีแดง | ใหญ่ | เป็นประจำ | 7 |

นี่คือดัชนี

| หมายเลขชุด | มิติ | ลำดับชั้น |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

ดัชนีช่วยให้คุณสามารถสอบถามปริมาณคงคลังคงเหลือได้ในลักษณะต่อไปนี้:

- `()` – จัดกลุ่มตามทั้งหมด

    - เสื้อยืดคอกลม, 28

- `(ColorId)` – จัดกลุ่มตาม `ColorId`

    - เสื้อยืดคอกลม, สีดำ, 10
    - เสื้อยืดคอกลม, สีแดง, 18

- `(ColorId, SizeId)` – จัดกลุ่มตามชุดข้อมูลของ `ColorId` และ `SizeId`

    - เสื้อยืดคอกลม, สีดำ, ขนาดเล็ก, 3
    - เสื้อยืดคอกลม, สีดำ, ขนาดใหญ่, 7
    - เสื้อยืดคอกลม, สีแดง, ขนาดเล็ก, 11
    - เสื้อยืดคอกลม, สีแดง, ขนาดใหญ่, 7

- `(ColorId, SizeId, StyleId)` – จัดกลุ่มตามชุดข้อมูลของ `ColorId`, `SizeId` และ `StyleId`

    - เสื้อยืดคอกลม, สีดำ, ขนาดเล็ก, กว้าง, 1
    - เสื้อยืดคอกลม, สีดำ, ขนาดเล็ก, ปกติ, 2
    - เสื้อยืดคอกลม, สีดำ, ขนาดใหญ่, กว้าง, 3
    - เสื้อยืดคอกลม, สีดำ, ขนาดใหญ่, ปกติ, 4
    - เสื้อยืดคอกลม, สีแดง, ขนาดเล็ก, กว้าง, 5
    - เสื้อยืดคอกลม, สีแดง, ขนาดเล็ก, ปกติ, 6
    - เสื้อยืดคอกลม, สีแดง, ขนาดใหญ่, ปกติ, 7

> [!NOTE]
> ไม่ควรกําหนดมิติพื้นฐานที่ถูกกําหนดในการตั้งค่าคอนฟิกพาร์ติชันในการตั้งค่าคอนฟิกดัชนี

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>การตั้งค่าคอนฟิกการจอง (ไม่จำเป็นต้องระบุ)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

ต้องใช้การตั้งค่าคอนฟิกการจอง ถ้าคุณต้องการใช้คุณลักษณะการจองแบบชั่วคราว การตั้งค่าคอนฟิกจะประกอบด้วยส่วนพื้นฐานสองส่วน:

- การแม็ปการจองแบบชั่วคราว
- ลำดับชั้นการจองแบบชั่วคราว

### <a name="soft-reservation-mapping"></a>การแม็ปการจองแบบชั่วคราว

เมื่อคุณทำการจอง คุณอาจต้องการทราบว่าปริมาณคงคลังคงเหลือพร้อมสำหรับการจองในปัจจุบันหรือไม่ การตรวจสอบความถูกต้องจะเชื่อมโยงกับการวัดที่มีการคํานวณซึ่งแสดงถึงสูตรการคํานวณของชุดของการวัดทางกายภาพ

ตัวอย่างเช่น การวัดการจองจะขึ้นอยู่กับการวัดทางกายภาพ `SoftReservOrdered` จากแหล่งข้อมูล `iv` (การแสดงผลสินค้าคงคลัง) ในกรณีนี้ คุณสามารถตั้งค่าการวัดที่มีการคํานวณ `AvailableToReserve` ของแหล่งข้อมูล `iv` ดังที่แสดงไว้ที่นี่

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `AvailPhysical` |
| การเพิ่มขึ้น | `pos` | `Inbound` |
| การลบ | `pos` | `Outbound` |
| การลบ | `iv` | `SoftReservOrdered` |

จากนั้น ตั้งค่าการแม็ปการจองแบบชั่วคราวเพื่อจัดเตรียมการแม็ปจากการวัดการจอง `SoftReservOrdered` ไปยังการวัดที่มีการคํานวณ `AvailableToReserve`

| แหล่งข้อมูลการวัดทางกายภาพ | การวัดทางกายภาพ | แหล่งข้อมูลที่พร้อมสำหรับการจอง | การวัดที่มีการคำนวณที่พร้อมสำหรับการจอง |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

ขณะนี้ เมื่อคุณทำการจองใน `SoftReservOrdered` การแสดงผลสินค้าคงคลังจะค้นหา `AvailableToReserve` โดยอัตโนมัติ และสูตรการคำนวณที่เกี่ยวข้องจะตรวจสอบความถูกต้องของการจอง

ตัวอย่างเช่น คุณมีปริมาณคงคลังคงเหลือต่อไปนี้ในการแสดงผลสินค้าคงคลัง

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

ในกรณีนี้ การคำนวณจะนำไปใช้:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

ดังนั้น หากคุณพยายามทำการจองใน `iv.SoftReservOrdered` ปริมาณจะน้อยกว่าหรือเท่ากับ `AvailableToReserve` (10) คุณสามารถทำการจองได้

### <a name="soft-reservation-hierarchy"></a>ลำดับชั้นการจองแบบชั่วคราว

ลำดับชั้นการจองจะอธิบายถึงลำดับของมิติที่ต้องระบุเมื่อจอง โดยจะทำงานในลักษณะเดียวกับที่ลำดับชั้นของดัชนีผลิตภัณฑ์จะทำงานสำหรับการสอบถามปริมาณคงคลังคงเหลือ

ลำดับชั้นการจองไม่ได้ขึ้นอยู่กับลำดับชั้นของดัชนีผลิตภัณฑ์ ความเป็นอิสระนี้จะช่วยให้คุณสามารถดําเนินการจัดการประเภท โดยที่ผู้ใช้สามารถแบ่งมิติออกเป็นรายละเอียด เพื่อระบุความต้องการในการใช้การจองที่ละเอียดมากขึ้น

นี่เป็นตัวอย่างของลำดับชั้นของการจองแบบชั่วคราว

| มิติพื้นฐาน | ลำดับชั้น |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

ในตัวอย่างนี้ คุณสามารถทำการจองในลำดับมิติต่อไปนี้:

- `()` – ไม่มีการระบุมิติ
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

ลำดับมิติที่ถูกต้องควรเป็นไปตามลำดับชั้นการจองอย่างเคร่งครัด มิติต่อมิติ ตัวอย่างเช่น ลำดับในลำดับชั้น `(SiteId, LocationId, SizeId)` ไม่ถูกต้อง เนื่องจาก `ColorId` ขาดหายไป

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>ตัวอย่างการตั้งค่าคอนฟิกเริ่มต้น

ในระหว่างขั้นการเริ่มต้น การแสดงผลสินค้าคงคลังจะตั้งค่าการตั้งค่าคอนฟิกเริ่มต้น คุณสามารถปรับเปลี่ยนการตั้งค่าคอนฟิกได้ตามที่คุณต้องการ

### <a name="data-source-configuration"></a>การตั้งค่าคอนฟิกแหล่งข้อมูล

#### <a name="configuration-of-the-iv-data-source"></a>การตั้งค่าคอนฟิกของแหล่งข้อมูล iv

ส่วนนี้อธิบายวิธีการตั้งค่าคอนฟิกแหล่งข้อมูล `iv`

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>การวัดทางกายภาพที่ตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล iv

การวัดทางกายภาพต่อไปนี้ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv`:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>การวัดที่มีการคำนวณ OrderedTotal

การวัดที่มีการคำนวณ `OrderedTotal` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `Ordered` |
| การเพิ่มขึ้น | `fno` | `Arrived` |
| การเพิ่มขึ้น | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>การวัดที่มีการคำนวณ OnHand

การวัดที่มีการคำนวณ `OnHand` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `PhysicalInvent` |
| การเพิ่มขึ้น | `iom` | `OnHand` |
| การเพิ่มขึ้น | `erp` | `Unrestricted` |
| การเพิ่มขึ้น | `erp` | `QualityInspection` |
| การเพิ่มขึ้น | `pos` | `PosInbound` |
| การลบ | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>การวัดที่มีการคำนวณ ReservedTotal

การวัดที่มีการคำนวณ `ReservedTotal` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `ReservPhysical` |
| การเพิ่มขึ้น | `fno` | `ReservOrdered` |
| การเพิ่มขึ้น | `iv` | `SoftReservPhysical` |
| การเพิ่มขึ้น | `iv` | `SoftReservOrdered` |
| การเพิ่มขึ้น | `iv` | `ReservPhysical` |
| การเพิ่มขึ้น | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>การวัดที่มีการคำนวณ SoftReserved

การวัดที่มีการคำนวณ `SoftReserved` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `iv` | `SoftReservPhysical` |
| การเพิ่มขึ้น | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>การวัดที่มีการคำนวณ HardReserved

การวัดที่มีการคำนวณ `HardReserved` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `ReservPhysical` |
| การเพิ่มขึ้น | `fno` | `ReservOrdered` |
| การเพิ่มขึ้น | `iv` | `ReservPhysical` |
| การเพิ่มขึ้น | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>การวัดที่มีการคำนวณ OpenOrder

การวัดที่มีการคำนวณ `OpenOrder` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `OnOrder` |
| การเพิ่มขึ้น | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>การวัดที่มีการคำนวณ OnHandAvailable

การวัดที่มีการคำนวณ `OnHandAvailable` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `PhysicalInvent` |
| การเพิ่มขึ้น | `iom` | `OnHand` |
| การเพิ่มขึ้น | `erp` | `Unrestricted` |
| การเพิ่มขึ้น | `erp` | `QualityInspection` |
| การเพิ่มขึ้น | `pos` | `PosInbound` |
| การลบ | `fno` | `ReservPhysical` |
| การลบ | `iv` | `SoftReservPhysical` |
| การลบ | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>การวัดที่มีการคำนวณ AvailableToReserve

การวัดที่มีการคำนวณ `AvailableToReserve` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `PhysicalInvent` |
| การเพิ่มขึ้น | `iom` | `OnHand` |
| การเพิ่มขึ้น | `erp` | `Unrestricted` |
| การเพิ่มขึ้น | `erp` | `QualityInspection` |
| การเพิ่มขึ้น | `pos` | `PosInbound` |
| การเพิ่มขึ้น | `fno` | `Ordered` |
| การเพิ่มขึ้น | `fno` | `Arrived` |
| การเพิ่มขึ้น | `iv` | `Ordered` |
| การลบ | `fno` | `ReservPhysical` |
| การลบ | `fno` | `ReservOrdered` |
| การลบ | `iv` | `SoftReservPhysical` |
| การลบ | `iv` | `SoftReservOrdered` |
| การลบ | `iv` | `ReservPhysical` |
| การลบ | `iv` | `ReservOrdered` |
| การลบ | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>การวัดที่มีการคำนวณ InventorySupply

การวัดที่มีการคำนวณ `InventorySupply` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `Ordered` |
| การเพิ่มขึ้น | `fno` | `Arrived` |
| การเพิ่มขึ้น | `iv` | `Ordered` |
| การเพิ่มขึ้น | `fno` | `PhysicalInvent` |
| การเพิ่มขึ้น | `iom` | `OnHand` |
| การเพิ่มขึ้น | `erp` | `Unrestricted` |
| การเพิ่มขึ้น | `erp` | `QualityInspection` |
| การเพิ่มขึ้น | `pos` | `PosInbound` |
| การลบ | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>การวัดที่มีการคำนวณ InventoryDemand

การวัดที่มีการคำนวณ `InventoryDemand` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iv` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `OnOrder` |
| การเพิ่มขึ้น | `iom` | `OnOrder` |
| การเพิ่มขึ้น | `iv` | `SoftReservPhysical` |
| การเพิ่มขึ้น | `iv` | `SoftReservOrdered` |
| การเพิ่มขึ้น | `fno` | `ReservPhysical` |
| การเพิ่มขึ้น | `fno` | `ReservOrdered` |
| การเพิ่มขึ้น | `iv` | `ReservPhysical` |
| การเพิ่มขึ้น | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>การตั้งค่าคอนฟิกของแหล่งข้อมูล fno

ส่วนนี้อธิบายวิธีการตั้งค่าคอนฟิกแหล่งข้อมูล `fno`

##### <a name="dimension-mappings-for-the-fno-data-source"></a>การแม็ปมิติสำหรับแหล่งข้อมูล fno

การแม็ปมิติที่แสดงรายการอยู่ในตารางต่อไปนี้ได้รับการตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `fno`

| มิติภายนอก | มิติพื้นฐาน |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>การวัดทางกายภาพที่ตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล fno

การวัดทางกายภาพต่อไปนี้ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `fno`:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>การตั้งค่าคอนฟิกของแหล่งข้อมูล pos

ส่วนนี้อธิบายวิธีการตั้งค่าคอนฟิกแหล่งข้อมูล `pos`

##### <a name="physical-measures-for-the-pos-data-source"></a>การวัดทางกายภาพสำหรับแหล่งข้อมูล pos

การวัดทางกายภาพต่อไปนี้ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `pos`:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>การวัดที่มีการคำนวณ AvailQuantity

การวัดที่มีการคำนวณ `AvailQuantity` ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `pos` ตามที่แสดงไว้ในตารางต่อไปนี้

| ชนิดการคำนวณ | แหล่งข้อมูล | การวัดทางกายภาพ |
|---|---|---|
| การเพิ่มขึ้น | `fno` | `AvailPhysical` |
| การเพิ่มขึ้น | `pos` | `PosInbound` |
| การลบ | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>การตั้งค่าคอนฟิกของแหล่งข้อมูล iom

การวัดทางกายภาพต่อไปนี้ได้รับการตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `iom` (Intelligent Order Management):

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>การตั้งค่าคอนฟิกของแหล่งข้อมูล erp

การวัดทางกายภาพต่อไปนี้ได้รับการตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล `erp` (การวางแผนทรัพยากรองค์กร):

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>การตั้งค่าคอนฟิกพาร์ติชัน

ตารางต่อไปนี้แสดงการตั้งค่าคอนฟิกพาร์ติชันเริ่มต้น

| มิติพื้นฐาน | ลำดับชั้น |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>การตั้งค่าคอนฟิกดัชนี

ตารางต่อไปนี้แสดงการตั้งค่าคอนฟิกดัชนีเริ่มต้น

| หมายเลขชุด | มิติ | ลำดับชั้น |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>การตั้งค่าคอนฟิกการจอง

ส่วนนี้อธิบายการตั้งค่าคอนฟิกการจองเริ่มต้น

#### <a name="reservation-mapping"></a>การแม็ปการจอง

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

ตารางต่อไปนี้แสดงการแม็ปการจองเริ่มต้น

| แหล่งข้อมูลการวัดทางกายภาพ | การวัดทางกายภาพ | แหล่งข้อมูลที่พร้อมสำหรับการจอง | การวัดที่มีการคำนวณที่พร้อมสำหรับการจอง |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>ลำดับชั้นการจอง

ตารางต่อไปนี้แสดงลำดับชั้นของการจองเริ่มต้น

| มิติพื้นฐาน | ลำดับชั้น |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 ชั่วโมง |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | วันที่ 15 ก.ย. |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
