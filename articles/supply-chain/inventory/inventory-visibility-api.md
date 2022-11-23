---
title: API สาธารณะสำหรับ Inventory Visibility
description: บทความนี้จะอธิบาย API สาธารณะที่ให้ไว้โดยการแสดงผลสินค้าคงคลัง
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762846"
---
# <a name="inventory-visibility-public-apis"></a>API สาธารณะสำหรับ Inventory Visibility

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบาย API สาธารณะที่ให้ไว้โดยการแสดงผลสินค้าคงคลัง

REST API สาธารณะของ Add-in การแสดงผลสินค้าคงคลัง แสดงถึงปลายทางเฉพาะสำหรับการรวมหลายแห่ง ซึ่งสนับสนุนชนิดการโต้ตอบหลักสี่ชนิด:

- การโพสต์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือไปที่ add-in จากระบบภายนอก
- การตั้งค่าหรือการแทนที่ปริมาณคงคลังคงเหลือใน Add-in จากระบบภายนอก
- การลงรายการบัญชีเหตุการณ์การจองไปที่ add-in จากระบบภายนอก
- การสอบถามปริมาณคงคลังคงเหลือปัจจุบันจากระบบภายนอก

ตารางต่อไปนี้แสดง API ที่พร้อมใช้งานในขณะนี้:

| พาธ | วิธีการ | คำอธิบาย |
|---|---|---|
| /api/environment/{environmentId}/onhand | ลงรายการบัญชี | [สร้างเหตุการณ์การเปลี่ยนแปลงคงเหลือหนึ่งเหตุการณ์](#create-one-onhand-change-event)|
| /api/environment/{environmentId}/onhand/bulk | ลงรายการบัญชี | [สร้างเหตุการณ์การเปลี่ยนแปลงหลายเหตุการณ์](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | ลงรายการบัญชี | [ตั้งค่า/แทนที่ปริมาณคงคลังคงเหลือ](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | ลงรายการบัญชี | [สร้างเหตุการณ์การจองชั่วคราวหนึ่งเหตุการณ์](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | ลงรายการบัญชี | [สร้างเหตุการณ์การจองชั่วคราวหลายเหตุการณ์](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/unreserve | ลงรายการบัญชี | [ย้อนกลับเหตุการณ์การจองชั่วคราวหนึ่งเหตุการณ์](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | ลงรายการบัญชี | [ย้อนกลับเหตุการณ์การจองชั่วคราวหลายเหตุการณ์](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | ลงรายการบัญชี | [สร้างการเปลี่ยนแปลงปริมาณคงเหลือตามกำหนดการหนึ่งเหตุการณ์](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | ลงรายการบัญชี | [สร้างการเปลี่ยนแปลงปริมาณคงเหลือตามวันที่](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | ลงรายการบัญชี | [สอบถามโดยใช้วิธีการประกาศ](#query-with-post-method) (แนะนำ) |
| /api/environment/{environmentId}/onhand | ดึงข้อมูล | [การสอบถามโดยใช้วิธีการรับ](#query-with-get-method) |
| /api/environment/{environmentId}/onhand/exactquery | ลงรายการบัญชี | [แยกการสอบถามโดยใช้วิธีการประกาศ](#exact-query-with-post-method) |
| /api/environment/{environmentId}/allocation<wbr>/allocate | ลงรายการบัญชี | [สร้างเหตุการณ์การปันส่วนหนึ่งเหตุการณ์](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/unallocate | ลงรายการบัญชี | [สร้างเหตุการณ์การไม่ได้ปันส่วนหนึ่งเหตุการณ์](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/reallocate | ลงรายการบัญชี | [สร้างเหตุการณ์การปันส่วนปริมาณใหม่หนึ่งเหตุการณ์](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/consume | ลงรายการบัญชี | [สร้างเหตุการณ์การใช้หนึ่งเหตุการณ์](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/query | ลงรายการบัญชี | [ผลลัพธ์การปันส่วนการสอบถาม](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> ส่วนของ {environmentId} พาธคือรหัสสภาพแวดล้อมใน Microsoft Dynamics Lifecycle Services
> 
> API จำนวนมากสามารถส่งคืนเรกคอร์ดได้สูงสุด 512 เรกคอร์ดต่อการร้องขอแต่ละครั้ง

Microsoft ได้ให้การรวบรวมการร้องขอ *Postman* แบบสำเร็จรูป คุณสามารถนําเข้าการรวบรวมนี้ไปยังซอฟต์แวร์ *Postman* ของคุณได้ โดยใช้ลิงค์ที่ใช้ร่วมกันต่อไปนี้: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>ค้นหาปลายทางตามสภาพแวดล้อม Lifecycle Services ของคุณ

ไมโครเซอร์วิสของการแสดงผลสินค้าคงคลังมีการปรับใช้บน Microsoft Azure Service Fabric ในหลายๆ ภูมิศาสตร์และหลายๆ ภูมิภาค ไม่มีปลายทางส่วนกลางที่สามารถเปลี่ยนเส้นทางคำขอของคุณไปยังพื้นที่ภูมิศาสตร์และภูมิภาคที่สอดคล้องกันโดยอัตโนมัติได้ในขณะนี้ ดังนั้น คุณต้องสร้างข้อมูลส่วนต่างๆ ลงใน URL โดยใช้รูปแบบต่อไปนี้:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

ชื่อย่อของภูมิภาคสามารถดูได้ในสภาพแวดล้อม Lifecycle Services ตารางต่อไปนี้แสดงภูมิภาคที่พร้อมใช้งานในขณะนี้

| ภูมิภาคของ Azure        | ชื่อย่อของภูมิภาค |
| ------------------- | ----------------- |
| ออสเตรเลียตะวันออก      | eau               |
| ออสเตรเลียตะวันออกเฉียงใต้ | seau              |
| แคนาดากลาง      | cca               |
| แคนาดาตะวันออก         | eca               |
| ยุโรปเหนือ        | neu               |
| ยุโรปตะวันตก         | weu               |
| สหรัฐอเมริกาตะวันออก             | eus               |
| สหรัฐอเมริกาตะวันตก             | wus               |
| สหราชอาณาจักรใต้            | suk               |
| สหราชอาณาจักรตะวันตก             | wuk               |
| ญี่ปุ่นตะวันออก          | ejp               |
| ญี่ปุ่นตะวันตก          | wjp               |
| อินเดียกลาง       | Cin               |
| อินเดียใต้         | Sin               |
| สวิตเซอร์แลนด์ เหนือ   | Nch               |
| สวิตเซอร์แลนด์ตะวันตก    | Wch               |
| ฝรั่งเศสใต้        | Sfr               |
| เอเชียตะวันออก           | Eas               |
| เอเชียตะวันออกเฉียงใต้     | Seas              |
| สหรัฐอาหรับเอมิเรตส์เหนือ           | Nae               |
| นอร์เวย์ฝั่งตะวันออก         | Eno               |
| นอร์เวย์ฝั่งตะวันตก         | Wno               |
| แอฟริกาใต้ตะวันตก   | Wza               |
| แอฟริกาใต้ตอนเหนือ  | Nza               |

หมายเลขเกาะคือที่ที่มีการปรับใช้สภาพแวดล้อม Lifecycle Services ของคุณบน Service Fabric ขณะนี้ไม่มีวิธีในการรับข้อมูลนี้จากฝั่งผู้ใช้

Microsoft ได้สร้างอินเทอร์เฟสผู้ใช้ (UI) ใน Power Apps ไว้ เพื่อให้คุณสามารถได้รับปลายทางที่สมบูรณ์ของไมโครเซอร์วิส สำหรับข้อมูลเพิ่มเติม ดู [ค้นหาปลายทางบริการ](inventory-visibility-configuration.md#get-service-endpoint)

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>การรับรองความถูกต้อง

โทเคนความปลอดภัยของแพลตฟอร์มจะถูกใช้ในการเรียก API สาธารณะของการแสดงผลสินค้าคงคลัง ดังนั้น คุณจึงต้องสร้างโทเคน *Azure Active Directory (Azure AD)* โดยใช้แอปพลิเคชัน Azure AD ของคุณ จากนั้นคุณต้องใช้โทเคน Azure AD เพื่อรับ *การเข้าถึงโทเคน* จากบริการความปลอดภัย

Microsoft ได้ให้การรวบรวมโทเค็น *Postman* แบบสำเร็จรูป คุณสามารถนําเข้าการรวบรวมนี้ไปยังซอฟต์แวร์ *Postman* ของคุณได้ โดยใช้ลิงค์ที่ใช้ร่วมกันต่อไปนี้: <https://www.getpostman.com/collections/496645018f96b3f0455e>

เมื่อต้องการเรียกใช้โทเค็นบริการรักษาความปลอดภัย ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้พอร์ทัล Azure และใช้เพื่อค้นหาค่า `clientId` และ `clientSecret` สำหรับแอป Dynamics 365 Supply Chain Management ของคุณ
1. ดึงข้อมูลโทเค็น Azure AD (`aadToken`) โดยการส่งคำขอ HTTP ที่มีคุณสมบัติต่อไปนี้:

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **วิธีการ:** `GET`
    - **ตัวเนื้อหา (ข้อมูลฟอร์ม):**

        | คีย์           | มูลค่า                                            |
        | ------------- | -------------------------------------------------|
        | รหัส_ไคลเอนต์     | ${aadAppId}                                      |
        | ข้อมูลลับ_ไคลเอ็นต์ | ${aadAppSecret}                                  |
        | ชนิด_การให้สิทธิ์    | ข้อมูลประจำตัว_ไคลเอ็นต์                               |
        | ขอบเขต         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

    คุณควรได้รับโทเค็น Azure AD (`aadToken`) ในการตอบสนอง ผลลัพธ์ควรมีลักษณะคล้ายกับตัวอย่างต่อไปนี้

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. สร้างคำขอ JavaScript Object Notation (JSON) ที่มีลักษณะคล้ายกับตัวอย่างต่อไปนี้

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type": "aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope": "https://inventoryservice.operations365.dynamics.com/.default",
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    บันทึกคะแนนต่อไปนี้:

    - ค่า `client_assertion` ต้องเป็นโทเค็น Azure AD (`aadToken`) ที่คุณได้รับในขั้นตอนก่อนหน้านี้
    - ค่า `context` ต้องเป็นรหัสสภาพแวดล้อม Lifecycle Services ที่คุณต้องการปรับใช้ Add-in
    - ตั้งค่าอื่นๆ ทั้งหมด ตามที่แสดงในตัวอย่าง

1. ดึงข้อมูลโทเค็นการเข้าถึง (`access_token`) โดยการส่งคำขอ HTTP ที่มีคุณสมบัติต่อไปนี้:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **วิธีการ:** `POST`
    - **ส่วนหัว HTTP:** รวมรุ่นของ API (คีย์คือ `Api-Version` และค่าคือ `1.0`)
    - **ตัวเนื้อหา:** รวมถึงการร้องขอ JSON ที่คุณสร้างในขั้นตอนก่อนหน้านี้

    คุณควรได้รับโทเค็นการเข้าถึง (`access_token`) ในการตอบสนอง คุณต้องใช้โทเค็นนี้ในฐานะโทเค็นผู้ถือสิทธิ์เพื่อเรียก API ของการแสดงผลสินค้าคงคลัง นี่คือตัวอย่าง

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

> [!IMPORTANT]
> เมื่อคุณใช้การรวบรวมการร้องขอ *Postman* เพื่อเรียก API สาธารณะสำหรับการแสดงผลสินค้าคงคลัง คุณต้องเพิ่มโทเค็นผู้ถือของแต่ละคำขอ เมื่อต้องการค้นหาโทเค็นผู้ถือ ให้เลือกแท็บ **การอนุมัติ** ภายใต้ URL คำขอ เลือกชนิด **โทเค็นผู้ถือ** และคัดลอกโทเค็นการเข้าถึงที่ดึงข้อมูลในขั้นตอนสุดท้าย ในส่วนต่อมาของบทความนี้ `$access_token` จะใช้เพื่อแสดงถึงโทเค็นที่ถูกดึงมาในขั้นตอนสุดท้าย

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>สร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ

มี API อยู่สองรายการสำหรับการสร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ:

- สร้างเรกคอร์ดหนึ่งรายการ: `/api/environment/{environmentId}/onhand`
- สร้างเรกคอร์ดหลายรายการ: `/api/environment/{environmentId}/onhand/bulk`

ตารางต่อไปนี้สรุปความหมายของแต่ละฟิลด์ในเนื้อหา JSON

| ฟิลด์ ID | คำอธิบาย |
|---|---|
| `id` | รหัสเฉพาะสำหรับเหตุการณ์การเปลี่ยนแปลงเฉพาะ ถ้าการส่งอีกครั้งเกิดขึ้นเนื่องจากความล้มเหลวของบริการ ID นี้จะถูกใช้เพื่อให้แน่ใจว่าเหตุการณ์เดียวกันจะไม่ถูกนับสองครั้งในระบบ |
| `organizationId` | ตัวระบุขององค์กรที่ลิงก์ไปยังเหตุการณ์ ค่านี้จะถูกแมปไปยังองค์กรหรือรหัสพื้นที่ข้อมูลใน Supply Chain Management |
| `productId` | ตัวระบุของผลิตภัณฑ์ |
| `quantities` | ปริมาณที่ต้องมีการเปลี่ยนแปลงปริมาณคงคลังคงเหลือ ตัวอย่างเช่น ถ้ามีการเพิ่มสมุดบัญชีใหม่ 10 เล่มในชั้นวาง ค่านี้จะเป็น `quantities:{ shelf:{ received: 10 }}` ถ้าเอาสมุดบัญชีสามเล่มออกจากชั้นวางหรือขายแล้ว ค่านี้จะเป็น `quantities:{ shelf:{ sold: 3 }}` |
| `dimensionDataSource` | แหล่งข้อมูลของมิติที่ถูกใช้ในการลงรายการบัญชีเหตุการณ์การเปลี่ยนแปลงและการสอบถาม ถ้าคุณระบุแหล่งข้อมูล คุณสามารถใช้มิติที่กำหนดเองจากแหล่งข้อมูลที่ระบุได้ การแสดงผลสินค้าคงคลังสามารถใช้การตั้งค่าคอนฟิกมิติเพื่อแมปมิติที่กำหนดเองกับมิติเริ่มต้นทั่วไป ถ้าไม่มีการระบุค่า `dimensionDataSource` คุณสามารถใช้ได้เฉพาะ [มิติฐาน](inventory-visibility-configuration.md#data-source-configuration-dimension) ทั่วไปในการสอบถามของคุณเท่านั้น |
| `dimensions` | คู่คีย์/ค่าแบบไดนามิก ค่าถูกแมปกับมิติบางมิติใน Supply Chain Management อย่างไรก็ตาม คุณยังสามารถเพิ่มมิติที่กำหนดเอง (ตัวอย่างเช่น *ต้นทาง*) เพื่อบ่งชี้ว่าเหตุการณ์มาจากการ Supply Chain Management หรือระบบภายนอก |

> [!NOTE]
> พารามิเตอร์ `siteId` และ `locationId` จะสร้าง [การตั้งค่าคอนฟิกพาร์ติชัน](inventory-visibility-configuration.md#partition-configuration) ดังนั้น คุณต้องระบุในมิติเมื่อคุณสร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ ตั้งค่าหรือแทนที่ปริมาณคงคลังคงเหลือ หรือสร้างเหตุการณ์การจอง

ส่วนย่อยต่อไปนี้แสดงตัวอย่างที่แสดงวิธีการใช้ API เหล่านี้

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>สร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือหนึ่งเหตุการณ์

API นี้จะสร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือเหตุการณ์เดียว

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่าง ในตัวอย่างนี้ บริษัทมีระบบขายหน้าร้าน (POS) ที่ดำเนินการธุรกรรมในร้านค้า และการเปลี่ยนแปลงสินค้าคงคลัง ลูกค้าได้ส่งคืนเสื้อยืดสีแดงให้ร้านของคุณ ในการแสดงการเปลี่ยนแปลง คุณลงรายการบัญชีเหตุการณ์การเปลี่ยนแปลงรายการเดียวสำหรับผลิตภัณฑ์ *เสื้อยืด* เหตุการณ์นี้จะเพิ่มปริมาณของผลิตภัณฑ์ *เสื้อยืดคอกลม* 1 รายการ

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่างโดยไม่มี `dimensionDataSource` ในกรณีนี้ `dimensions` จะเป็น [มิติพื้นฐาน](inventory-visibility-configuration.md#data-source-configuration-dimension) ถ้าตั้งค่า `dimensionDataSource` ไว้ `dimensions` อาจเป็นมิติแหล่งข้อมูลหรือมิติพื้นฐาน

```json
{
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>สร้างเหตุการณ์การเปลี่ยนแปลงหลายเหตุการณ์

API นี้สามารถสร้างเหตุการณ์การเปลี่ยนแปลง เหมือนกับที่ [API เหตุการณ์เดียว](#create-one-onhand-change-event) สามารถทำได้ ความแตกต่างเดียวคือ API นี้สามารถสร้างเรกคอร์ดหลายรายการพร้อมกันได้ ดังนั้น ค่า `Path` และ `Body` จะแตกต่างกัน สำหรับ API นี้ `Body` จะมีแถวลำดับของเรกคอร์ด จำนวนเรกคอร์ดสูงสุดคือ 512 ดังนั้น API กลุ่มการเปลี่ยนแปลงปริมาณคงคลังคงเหลือสามารถสนับสนุนเหตุการณ์การเปลี่ยนแปลงได้มากถึง 512 การเปลี่ยนแปลงในคราวเดียว 

ตัวอย่างเช่น เครื่อง POS ของร้านค้าปลีกประมวลผลธุรกรรมสองรายการต่อไปนี้:

- ใบสั่งส่งคืนสินค้าหนึ่งรายการของเสื้อยืดสีแดงหนึ่งตัว
- ธุรกรรมการขายหนึ่งรายการของเสื้อยืดสีดำสามตัว

ในกรณีนี้ คุณสามารถรวมการอัปเดตสินค้าคงคลังในการเรียก API ครั้งเดียว

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
        ...
    ]
```

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่าง

```json
[
    {
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>ตั้งค่า/แทนที่ปริมาณคงคลังคงเหลือ

*ตั้งค่า API ปริมาณคงคลังคงเหลือ* จะแทนที่ข้อมูลปัจจุบันสำหรับผลิตภัณฑ์ที่ระบุ ฟังก์ชันนี้เป็นใช้ทั่วไปในการทำการอัปเดตการนับสินค้าคงคลัง ตัวอย่างเช่น ในระหว่างการนับสินค้าคงคลังประจำวัน ร้านค้าอาจพบว่าปริมาณสินค้าคงคลังคงเหลือจริงสำหรับเสื้อยืดสีแดงคือ 100 ดังนั้น ประมาณขาเข้าของระบบ POS ต้องอัปเดตเป็น 100 โดยไม่คำนึงถึงปริมาณเดิมก่อนหน้า คุณสามารถใช้ API นี้แทนที่ค่าที่มีอยู่

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่าง พฤติกรรมของ API นี้จะแตกต่างจากพฤติกรรมของ API ที่อธิบายไว้ในส่วน [สร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ](#create-onhand-change-event) ก่อนหน้าในบทความนี้ ในตัวอย่างนี้ ปริมาณของผลิตภัณฑ์ *เสื้อยืดคอกลม* จะถูกตั้งค่าเป็น 1

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>สร้างเหตุการณ์การจอง

เมื่อต้องการใช้ API *การจอง* คุณต้องเปิดคุณลักษณะการจอง และทำการตั้งค่าคอนฟิกการจองให้เสร็จสมบูรณ์ สำหรับข้อมูลเพิ่มเติม (รวมถึงกระแสข้อมูลและสถานการณ์ตัวอย่าง) โปรดดูที่ [การกำหนดค่าการจอง (ไม่บังคับ)](inventory-visibility-configuration.md#reservation-configuration)

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>สร้างเหตุการณ์การจองหนึ่งเหตุการณ์

การจองสินค้าสามารถทำได้โดยเทียบกับการตั้งค่าแหล่งข้อมูลที่แตกต่างกัน เมื่อต้องการตั้งค่าคอนฟิกการจองชนิดนี้ อันดับแรกให้ระบุแหล่งข้อมูลในพารามิเตอร์ `dimensionDataSource` จากนั้น ในพารามิเตอร์ `dimensions` ให้ระบุมิติตามการตั้งค่ามิติในแหล่งข้อมูลเป้าหมาย

เมื่อคุณเรียกใช้ API การจอง คุณสามารถควบคุมการตรวจสอบความถูกต้องของการจองได้โดยการระบุพารามิเตอร์ `ifCheckAvailForReserv` แบบบูลีนในเนื้อหาคำขอ ค่า `True` หมายความว่าการตรวจสอบความถูกต้องนั้นต้องระบุ ในขณะที่ค่า `False` หมายความว่าการตรวจสอบความถูกต้องนั้นไม่จำเป็น ค่าเริ่มต้นคือ `True`

ถ้าคุณต้องการย้อนกลับการจองหรือยกเลิกการจองปริมาณสินค้าคงคลังที่ระบุ ให้ตั้งค่าปริมาณเป็นค่าลบ และตั้งค่าพารามิเตอร์ `ifCheckAvailForReserv` เป็น `False` เพื่อข้ามการตรวจสอบความถูกต้อง นอกจากนี้ยังมี API ยกเลิกการจองที่จัดสรรที่จะเหมือนกันด้วย ความแตกต่างอยู่ที่วิธีการเรียก API ทั้งสองเท่านั้น เป็นการง่ายที่จะย้อนกลับเหตุการณ์การจองเฉพาะโดยใช้ `reservationId` ที่มี API *ยกเลิกการจอง* สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [ยกเลิกเหตุการณ์การจองหนึ่งรายการ](#reverse-reservation-events)

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่าง

```json
{
    "id": "reserve-0",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

ตัวอย่างต่อไปนี้แสดงการตอบสนองที่เสร็จเรียบร้อยแล้ว

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>สร้างเหตุการณ์การจองหลายเหตุการณ์

API นี้เป็นเวอร์ชันกลุ่มของ [API เหตุการณ์เดียว](#create-reservation-events)

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="reverse-reservation-events"></a>ย้อนกลับเหตุการณ์การจอง

API *Unreservs* ใช้เป็นการดําเนินงานย้อนกลับในเหตุการณ์ [*การจอง*](#create-reservation-events) ซึ่งให้วิธีการย้อนกลับเหตุการณ์การจองที่ระบุโดย `reservationId` หรือลดปริมาณการจองได้

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>ย้อนกลับเหตุการณ์การจองหนึ่งเหตุการณ์

เมื่อสร้างการจองแล้ว `reservationId` จะถูกรวมในเนื้อหาการตอบสนอง คุณต้องระบุ `reservationId` เดียวกันเพื่อยกเลิกการจอง และรวม `organizationId` เดียวกัน และ `dimensions` ถูกใช้สำหรับการเรียก API การจอง ในขั้นสุดท้าย ให้ระบุค่า `OffsetQty` ที่แสดงถึงจํานวนของรายการที่จะว่าง จากการจองก่อนหน้านี้ การจองสามารถย้อนกลับทั้งหมดหรือบางส่วนได้ ขึ้นอยู่กับ `OffsetQty` ที่ระบุ ตัวอย่างเช่น หากมีการจองสินค้าไว้ *100* หน่วย คุณสามารถระบุ `OffsetQty: 10` เป็นยกเลิกการจอง *10* ของยอดที่จองไว้เริ่มต้น

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

รหัสต่อไปนี้จะแสดงตัวอย่างของเนื้อหา

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

รหัสต่อไปนี้แสดงตัวอย่างของเนื้อหาการตอบสนองที่เสร็จเรียบร้อยแล้ว

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> ในเนื้อหาการตอบสนอง เมื่อ `OffsetQty` น้อยกว่าหรือเท่ากับปริมาณการจอง `processingStatus` จะเป็น "*สำเร็จ*" และ `totalInvalidOffsetQtyByReservId` จะเป็น *0*
>
> ถ้า `OffsetQty` มากกว่าจำนวนที่จองไว้ `processingStatus` จะเป็น "*partialSuccess*" และ `totalInvalidOffsetQtyByReservId` จะเป็นผลต่างระหว่าง `OffsetQty` และจำนวนที่จองไว้
>
>ตัวอย่างเช่น ถ้าการจองมีปริมาณเป็น *10* และ `OffsetQty` มีค่าเป็น *12* `totalInvalidOffsetQtyByReservId` จะเป็น *2*

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>ย้อนกลับเหตุการณ์การจองหลายเหตุการณ์

API นี้เป็นเวอร์ชันกลุ่มของ [API เหตุการณ์เดียว](#reverse-one-reservation-event)

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [      
        {
            id: string,
            organizationId: string,
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>ปริมาณคงคลังคงเหลือของการสอบถาม

ใช้ API *ปริมาณคงคลังคงเหลือของการสอบถาม* เพื่อดึงข้อมูลปริมาณคงคลังคงเหลือปัจจุบันสำหรับผลิตภัณฑ์ของคุณ คุณสามารถใช้ API นี้เมื่อใดก็ตามที่คุณต้องทราบสต็อก เช่น เมื่อคุณต้องการทบทวนระดับสต็อกผลิตภัณฑ์บนเว็บไซต์ e-commerce ของคุณ หรือเมื่อคุณต้องการตรวจสอบความพร้อมใช้งานของผลิตภัณฑ์ทั่วทั้งภูมิภาค หรือในร้านค้าและคลังสินค้าใกล้เคียง ปัจจุบัน API สนับสนุนการสอบถามสินค้าแต่ละรายการสูงสุด 5000 รายการตามค่า `productID` นอกจากนี้ `siteID` และ `locationID` ยังสามารถระบุหลายค่าในแต่ละการสอบถามได้ ขีดจํากัดสูงสุดจะกําหนดโดยสมการต่อไปนี้:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>การสอบถามโดยใช้วิธีการลงรายการบัญชี

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

ในส่วนเนื้อหาของคำขอนี้ `dimensionDataSource` ยังคงเป็นพารามิเตอร์ที่ไม่บังคับ ถ้าไม่ได้ตั้งค่าไว้ `filters` จะถือว่าเป็น *มิติพื้นฐาน* มีสี่ฟิลด์ที่ต้องใช้สำหรับ `filters`: `organizationId`, `productId`, `siteId` และ `locationId`

- `organizationId` ควรมีค่าเพียงค่าเดียว แต่ยังคงเป็นอาร์เรย์
- `productId` สามารถมีค่าหนึ่งค่าหรือมากกว่า ถ้าเป็นแถวลำดับที่ว่างเปล่า ผลิตภัณฑ์ทั้งหมดจะถูกส่งกลับ
- `siteId` และ `locationId` ใช้ในการแสดงผลสินค้าคงคลังในการพาร์ทิชัน คุณสามารถระบุค่า `siteId` ใน `locationId` มากกว่าหนึ่งค่าในคำขอ *แบบสอบถามคงเหลือ* ในรุ่นปัจจุบัน คุณต้องระบุทั้งค่า `siteId` และ `locationId`

เราแนะนำให้คุณใช้พารามิเตอร์ `groupByValues` เพื่อให้เป็นไปตามการตั้งค่าคอนฟิกของคุณเกี่ยวกับการจัดดัชนี สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ ดูที่ [การตั้งค่าคอนฟิกตามลำดับชั้นของดัชนีผลิตภัณฑ์](./inventory-visibility-configuration.md#index-configuration)

พารามิเตอร์ `returnNegative` จะควบคุมว่าผลลัพธ์มีรายการค่าลบหรือไม่

> [!NOTE]
> ถ้าคุณได้เปิดใช้งานคุณลักษณะการจัดกำหนดการการเปลี่ยนแปลงปริมาณคงเหลือและปริมาณที่ให้สัญญาได้ (ATP) การสอบถามของคุณยังสามารถรวมพารามิเตอร์ `QueryATP` แบบบูลีน ซึ่งควบคุมว่าผลการสอบถามรวมข้อมูล ATP หรือไม่ สำหรับข้อมูลเพิ่มเติมและตัวอย่าง ดูที่ [กำหนดการการเปลี่ยนแปลงปริมาณคงเหลือและปริมาณที่ให้สัญญาได้ของการมองเห็นสินค้าคงคลัง](inventory-visibility-available-to-promise.md)

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่าง ซึ่งแสดงว่าคุณสามารถสอบถามปริมาณคงคลังคงเหลือจากสถานที่เก็บต่างๆ (คลังสินค้า) ได้

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

ตัวอย่างต่อไปนี้แสดงวิธีการสอบถามผลิตภัณฑ์ทั้งหมดในไซต์และที่ตั้งเฉพาะ

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>การสอบถามโดยใช้วิธีการรับ

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

ต่อไปนี้เป็นตัวอย่าง URL การรับ คำขอรับนี้ไม่เหมือนกับตัวอย่างการลงรายการบัญชีที่ระบุไว้ก่อนหน้านี้

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a>การสอบถามปริมาณคงคลังคงเหลือที่แน่นอน

การสอบถามคงคลังคงเหลือที่แน่นอนจะคล้ายกับการสอบถามคงเหลือปกติ แต่ช่วยให้คุณสามารถระบุลำดับการแมประหว่างไซต์และที่ตั้งได้ ตัวอย่างเช่น คุณมีไซต์สองไซต์ต่อไปนี้:

- ไซต์ 1 ซึ่งมีการแม็ปกับที่ตั้ง A
- ไซต์ 2 ซึ่งมีการแม็ปกับที่ตั้ง B

หากต้องการสอบถามปริมาณคงคลังคงเหลือปกติ หากคุณระบุ `"siteId": ["1","2"]` และ `"locationId": ["A","B"]` การมองเห็นสินค้าคงคลังจะสอบถามผลลัพธ์ในไซต์และที่ตั้งต่อไปนี้โดยอัตโนมัติ:

- ไซต์ 1 ที่ตั้ง A
- ไซต์ 1 ที่ตั้ง B
- ไซต์ 2 ที่ตั้ง A
- ไซต์ 2 ที่ตั้ง B

ตามที่คุณเห็น การสอบถามคงเหลือปกติจะไม่รับรู้ได้ว่าที่ตั้ง A มีอยู่ในไซต์ 1 เท่านั้น และมีที่ตั้ง B อยู่ในไซต์ 2 เท่านั้น ดังนั้นจึงสร้างการสอบถามที่ซ้อนกัน เพื่อให้สามารถรองรับการแมปตามลำดับนี้ คุณสามารถใช้การสอบถามคงเหลือที่แน่นอน และระบุการแมปที่ตั้งในเนื้อหาการสอบถามได้ ในกรณีนี้ คุณจะได้รับการสอบถามและรับผลลัพธ์เฉพาะไซต์ 1 ที่ตั้ง A และไซต์ 2 ที่ตั้ง B เท่านั้น

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a>แยกการสอบถามโดยใช้วิธีการประกาศ

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

ในส่วนเนื้อหาของคำขอนี้ `dimensionDataSource` จะเป็นพารามิเตอร์ที่ไม่บังคับ ถ้าไม่ได้ตั้งค่าไว้ `dimensions` ใน `filters` จะถือเป็น *มิติพื้นฐาน* มีสี่ฟิลด์ที่ต้องใช้สำหรับ `filters`: `organizationId`, `productId`, `dimensions` และ `values`

- `organizationId` ควรมีค่าเพียงค่าเดียว แต่ยังคงเป็นอาร์เรย์
- `productId` สามารถมีค่าหนึ่งค่าหรือมากกว่า ถ้าเป็นแถวลำดับที่ว่างเปล่า ผลิตภัณฑ์ทั้งหมดจะถูกส่งกลับ
- ในอาร์เรย์ `dimensions` ต้องระบุ `siteId` และ `locationId` แต่อาจปรากฏพร้อมกับองค์ประกอบอื่นในลำดับใดๆ
- `values` อาจมีทูเพิลของค่าเฉพาะหนึ่งค่าหรือมากกว่าที่สัมพันธ์กับ `dimensions`

`dimensions` ใน `filters` จะถูกเพิ่มลงใน `groupByValues` โดยอัตโนมัติ

พารามิเตอร์ `returnNegative` จะควบคุมว่าผลลัพธ์มีรายการค่าลบหรือไม่

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่าง

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

ตัวอย่างต่อไปนี้แสดงวิธีการสอบถามผลิตภัณฑ์ทั้งหมดในไซต์และที่ตั้งหลายแห่ง

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>ปริมาณที่ให้สัญญาได้

คุณสามารถตั้งค่าการมองเห็นสินค้าคงคลังเพื่อให้คุณสามารถจัดกำหนดการเปลี่ยนแปลงปริมาณคงเหลือในอนาคตและคํานวณปริมาณ ATP ได้ ATP คือปริมาณของสินค้าที่พร้อมใช้งานและสามารถสัญญากับลูกค้าในรอบเวลาถัดไป การใช้การคํานวณ ATP จะเพิ่มความสามารถในการเติมสินค้าตามใบสั่งของคุณมากขึ้น สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเปิดใช้งานลักษณะ และวิธีการทำงานกับการมองเห็นสินค้าคงคลังผ่าน API หลังจากเปิดใช้งานคุณลักษณะ ดูที่ [กำหนดการการเปลี่ยนแปลงปริมาณคงเหลือและปริมาณที่ให้สัญญาได้ของการมองเห็นสินค้าคงคลัง](inventory-visibility-available-to-promise.md#api-urls)

## <a name="allocation"></a>การปันส่วน

API ที่เกี่ยวข้องกับการปันส่วนจะอยู่ใน [การปันส่วนการมองเห็นสินค้าคงคลัง](inventory-visibility-allocation.md#using-allocation-api)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
