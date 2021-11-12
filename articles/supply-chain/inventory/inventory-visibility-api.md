---
title: API สาธารณะของการแสดงผลสินค้าคงคลัง
description: หัวข้อนี้จะอธิบาย API สาธารณะที่ให้ไว้โดยการแสดงผลสินค้าคงคลัง
author: yufeihuang
ms.date: 09/30/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 1899969ddbbccafde3f7bb06a897ea7c0f2d656b
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678798"
---
# <a name="inventory-visibility-public-apis"></a>API สาธารณะของการแสดงผลสินค้าคงคลัง

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

หัวข้อนี้จะอธิบาย API สาธารณะที่ให้ไว้โดยการแสดงผลสินค้าคงคลัง

REST API สาธารณะของ Add-in การแสดงผลสินค้าคงคลัง แสดงถึงปลายทางเฉพาะสำหรับการรวมหลายแห่ง ซึ่งสนับสนุนชนิดการโต้ตอบหลักสี่ชนิด:

- การโพสต์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือไปที่ add-in จากระบบภายนอก
- การตั้งค่าหรือการแทนที่ปริมาณคงคลังคงเหลือใน Add-in จากระบบภายนอก
- การลงรายการบัญชีเหตุการณ์การจองไปที่ add-in จากระบบภายนอก
- การสอบถามปริมาณคงคลังคงเหลือปัจจุบันจากระบบภายนอก

ตารางต่อไปนี้แสดง API ที่พร้อมใช้งานในขณะนี้:

| พาธ | วิธีการ | คำอธิบาย |
|---|---|---|
| /api/environment/{environmentId}/onhand | ลงรายการบัญชี | [สร้างเหตุการณ์การเปลี่ยนแปลงคงเหลือหนึ่งเหตุการณ์](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | ลงรายการบัญชี | [สร้างเหตุการณ์การเปลี่ยนแปลงหลายเหตุการณ์](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | ลงรายการบัญชี | [ตั้งค่า/แทนที่ปริมาณคงคลังคงเหลือ](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | ลงรายการบัญชี | [สร้างเหตุการณ์การจองหนึ่งเหตุการณ์](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | ลงรายการบัญชี | [สร้างเหตุการณ์การจองหลายเหตุการณ์](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/indexquery | ดึงข้อมูล | [การสอบถามโดยใช้วิธีการลงรายการบัญชี](#query-with-post-method) |
| /api/environment/{environmentId}/onhand/indexquery | ลงรายการบัญชี | [การสอบถามโดยใช้วิธีการรับ](#query-with-get-method) |

Microsoft ได้ให้การรวบรวมการร้องขอ *Postman* แบบสำเร็จรูป คุณสามารถนําเข้าการรวบรวมนี้ไปยังซอฟต์แวร์ *Postman* ของคุณได้ โดยใช้ลิงค์ที่ใช้ร่วมกันต่อไปนี้: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>

> [!NOTE]
> ส่วนของ {environmentId} พาธคือรหัสสภาพแวดล้อมใน Microsoft Dynamics Lifecycle Services (LCS)

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>ค้นหาปลายทางตามสภาพแวดล้อม Lifecycle Services ของคุณ

ไมโครเซอร์วิสของการแสดงผลสินค้าคงคลังมีการปรับใช้บน Microsoft Azure Service Fabric ในหลายๆ ภูมิศาสตร์และหลายๆ ภูมิภาค ไม่มีปลายทางส่วนกลางที่สามารถเปลี่ยนเส้นทางคำขอของคุณไปยังพื้นที่ภูมิศาสตร์และภูมิภาคที่สอดคล้องกันโดยอัตโนมัติได้ในขณะนี้ ดังนั้น คุณต้องสร้างข้อมูลส่วนต่างๆ ลงใน URL โดยใช้รูปแบบต่อไปนี้:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

ชื่อย่อของภูมิภาคสามารถดูได้ในสภาพแวดล้อม Microsoft Dynamics Lifecycle Services (LCS) ตารางต่อไปนี้แสดงภูมิภาคที่พร้อมใช้งานในขณะนี้

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
| บราซิลใต้        | sbr               |
| สหรัฐอเมริกาภาคกลางตอนใต้    | scus              |

หมายเลขเกาะคือที่ที่มีการปรับใช้สภาพแวดล้อม LCS ของคุณบน Service Fabric ขณะนี้ไม่มีวิธีในการรับข้อมูลนี้จากฝั่งผู้ใช้

Microsoft ได้สร้างอินเทอร์เฟสผู้ใช้ (UI) ใน Power Apps ไว้ เพื่อให้คุณสามารถได้รับปลายทางที่สมบูรณ์ของไมโครเซอร์วิส สำหรับข้อมูลเพิ่มเติม ดู [ค้นหาปลายทางบริการ](inventory-visibility-configuration.md#get-service-endpoint)

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>การรับรองความถูกต้อง

โทเคนความปลอดภัยของแพลตฟอร์มจะถูกใช้ในการเรียก API สาธารณะของการแสดงผลสินค้าคงคลัง ดังนั้น คุณจึงต้องสร้างโทเคน _Azure Active Directory (Azure AD)_ โดยใช้แอพลิเคชัน Azure AD ของคุณ จากนั้นคุณต้องใช้โทเคน Azure AD เพื่อรับ _การเข้าถึงโทเคน_ จากบริการความปลอดภัย

Microsoft ได้ให้การรวบรวมโทเคน *Postman* แบบสำเร็จรูป คุณสามารถนําเข้าการรวบรวมนี้ไปยังซอฟต์แวร์ *Postman* ของคุณได้ โดยใช้ลิงค์ที่ใช้ร่วมกันต่อไปนี้: <https://www.getpostman.com/collections/496645018f96b3f0455e>

เมื่อต้องการเรียกใช้โทเคนบริการรักษาความปลอดภัย ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้พอร์ทัล Azure และใช้เพื่อค้นหาค่า `clientId` และ `clientSecret` สำหรับแอป Dynamics 365 Supply Chain Management ของคุณ
1. ดึงข้อมูลโทเค็น Azure AD (`aadToken`) โดยการส่งคำขอ HTTP ที่มีคุณสมบัติต่อไปนี้:

   - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **วิธีการ:** `GET`
   - **ตัวเนื้อหา (ข้อมูลฟอร์ม):**

     | คีย์           | มูลค่า                                |
     | ------------- | ------------------------------------ |
     | รหัส_ไคลเอนต์     | ${aadAppId}                          |
     | ข้อมูลลับ_ไคลเอ็นต์ | ${aadAppSecret}                      |
     | ชนิด_การให้สิทธิ์    | ข้อมูลประจำตัว_ไคลเอ็นต์                   |
     | ทรัพยากร      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

   คุณควรได้รับโทเคน Azure AD (`aadToken`) ในการตอบสนอง ผลลัพธ์ควรมีลักษณะคล้ายกับตัวอย่างต่อไปนี้

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "expires_on": "1610466645",
       "not_before": "1610462745",
       "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
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
       "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
       "context_type": "finops-env"
   }
   ```

   บันทึกคะแนนต่อไปนี้:

   - ค่า `client_assertion` ต้องเป็นโทเคน Azure AD (`aadToken`) ที่คุณได้รับในขั้นตอนก่อนหน้านี้
   - ค่า `context` ต้องเป็นรหัสสภาพแวดล้อม LCS ที่คุณต้องการปรับใช้ Add-in
   - ตั้งค่าอื่นๆ ทั้งหมด ตามที่แสดงในตัวอย่าง

1. ดึงข้อมูลโทเคนการเข้าถึง (`access_token`) โดยการส่งคำขอ HTTP ที่มีคุณสมบัติต่อไปนี้:

   - **URL:** `https://securityservice.operations365.dynamics.com/token`
   - **วิธีการ:** `POST`
   - **ส่วนหัว HTTP:** รวมรุ่นของ API (คีย์คือ `Api-Version` และค่าคือ `1.0`)
   - **ตัวเนื้อหา:** รวมถึงการร้องขอ JSON ที่คุณสร้างในขั้นตอนก่อนหน้านี้

   คุณควรได้รับโทเคนการเข้าถึง (`access_token`) ในการตอบสนอง คุณต้องใช้โทเคนนี้ในฐานะโทเคนผู้ถือสิทธิ์เพื่อเรียก API ของการแสดงผลสินค้าคงคลัง นี่คือตัวอย่าง

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

> [!IMPORTANT]
> เมื่อคุณใช้การรวบรวมการร้องขอ *Postman* เพื่อเรียก API สาธารณะสำหรับการแสดงผลสินค้าคงคลัง คุณต้องเพิ่มโทเคนผู้ถือของแต่ละคำขอ เมื่อต้องการค้นหาโทเคนผู้ถือ ให้เลือกแท็บ **การอนุมัติ** ภายใต้ URL คำขอ เลือกชนิด **โทเคนผู้ถือ** และคัดลอกโทเคนการเข้าถึงที่ดึงข้อมูลในขั้นตอนสุดท้าย ในส่วนต่อมาของหัวข้อนี้ `$access_token` จะใช้เพื่อแสดงถึงโทเคนที่ถูกดึงมาในขั้นตอนสุดท้าย

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>สร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ

มี API อยู่สองรายการสำหรับการสร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ:

- สร้างเรกคอร์ดหนึ่งรายการ: `/api/environment/{environmentId}/onhand`
- สร้างเรกคอร์ดหลายรายการ: `/api/environment/{environmentId}/onhand/bulk`

ตารางต่อไปนี้สรุปความหมายของแต่ละฟิลด์ในเนื้อหา JSON

| ฟิลด์ ID | คำอธิบาย |
|---|---|
| `id` | รหัสเฉพาะสำหรับเหตุการณ์การเปลี่ยนแปลงเฉพาะ รหัสนี้จะถูกใช้เพื่อให้แน่ใจว่า ถ้าการสื่อสารกับบริการล้มเหลวในระหว่างการลงรายการบัญชี เหตุการณ์เดียวกันจะไม่ถูกนับสองครั้งในระบบ หากไม่มีการส่งซ้ำ |
| `organizationId` | ตัวระบุขององค์กรที่ลิงก์ไปยังเหตุการณ์ ค่านี้จะถูกแม็ปไปยังองค์กรหรือรหัสพื้นที่ข้อมูลใน Supply Chain Management |
| `productId` | ตัวระบุของผลิตภัณฑ์ |
| `quantities` | ปริมาณที่ต้องมีการเปลี่ยนแปลงปริมาณคงคลังคงเหลือ ตัวอย่างเช่น ถ้ามีการเพิ่มสมุดบัญชีใหม่ 10 เล่มในชั้นวาง ค่านี้จะเป็น `quantities:{ shelf:{ received: 10 }}` ถ้าเอาสมุดบัญชีสามเล่มออกจากชั้นวางหรือขายแล้ว ค่านี้จะเป็น `quantities:{ shelf:{ sold: 3 }}` |
| `dimensionDataSource` | แหล่งข้อมูลของมิติที่ถูกใช้ในการลงรายการบัญชีเหตุการณ์การเปลี่ยนแปลงและการสอบถาม ถ้าคุณระบุแหล่งข้อมูล คุณสามารถใช้มิติที่กำหนดเองจากแหล่งข้อมูลที่ระบุได้ การแสดงผลสินค้าคงคลังสามารถใช้การตั้งค่าคอนฟิกมิติเพื่อแม็ปมิติที่กำหนดเองกับมิติเริ่มต้นทั่วไป ถ้าไม่มีการระบุค่า `dimensionDataSource` คุณสามารถใช้ได้เฉพาะ [มิติฐาน](inventory-visibility-configuration.md#data-source-configuration-dimension) ทั่วไปในการสอบถามของคุณเท่านั้น |
| `dimensions` | คู่คีย์/ค่าแบบไดนามิก ค่าถูกแม็ปกับมิติบางมิติใน Supply Chain Management อย่างไรก็ตาม คุณยังสามารถเพิ่มมิติที่กำหนดเอง (ตัวอย่างเช่น _ต้นทาง_) เพื่อบ่งชี้ว่าเหตุการณ์มาจากการ Supply Chain Management หรือระบบภายนอก |

> [!NOTE]
> พารามิเตอร์ `SiteId` และ `LocationId` จะสร้าง [การตั้งค่าคอนฟิกพาร์ติชัน](inventory-visibility-configuration.md#partition-configuration) ดังนั้น คุณต้องระบุในมิติเมื่อคุณสร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ ตั้งค่าหรือแทนที่ปริมาณคงคลังคงเหลือ หรือสร้างเหตุการณ์การจอง

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

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่าง ในตัวอย่างนี้ คุณลงรายการบัญชีเหตุการณ์การเปลี่ยนแปลงสำหรับผลิตภัณฑ์ *เสื้อยืดคอกลม* เหตุการณ์นี้มาจากระบบการขายหน้าร้าน (POS) และลูกค้าส่งคืนเสื้อยืดคอกลมสีแดงกลับไปที่ร้านค้าของคุณ เหตุการณ์นี้จะเพิ่มปริมาณของผลิตภัณฑ์ *เสื้อยืดคอกลม* 1 รายการ

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId": "Red"
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
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>สร้างเหตุการณ์การเปลี่ยนแปลงหลายเหตุการณ์

API นี้สามารถสร้างเรกคอร์ดหลายรายการพร้อมกันได้ ความแตกต่างระหว่าง API นี้และ [API เหตุการณ์เดียว](#create-one-onhand-change-event) ได้แก่ ค่า `Path` และค่า `Body` สำหรับ API นี้ `Body` จะมีแถวลำดับของเรกคอร์ด

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
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>ตั้งค่า/แทนที่ปริมาณคงคลังคงเหลือ

_ตั้งค่า API ปริมาณคงคลังคงเหลือ_ จะแทนที่ข้อมูลปัจจุบันสำหรับผลิตภัณฑ์ที่ระบุ

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

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่าง พฤติกรรมของ API นี้จะแตกต่างจากพฤติกรรมของ API ที่อธิบายไว้ในส่วน [สร้างเหตุการณ์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ](#create-onhand-change-event) ก่อนหน้าในหัวข้อนี้ ในตัวอย่างนี้ ปริมาณของผลิตภัณฑ์ *เสื้อยืดคอกลม* จะถูกตั้งค่าเป็น 1

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>สร้างเหตุการณ์การจอง

เมื่อต้องการใช้ API *จอง* คุณต้องเปิดคุณลักษณะการจองและทำการตั้งค่าคอนฟิกการจองให้เสร็จสมบูรณ์ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การตั้งค่าคอนฟิกการจอง (ไม่จำเป็น)](inventory-visibility-configuration.md#reservation-configuration)

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>สร้างเหตุการณ์การจองหนึ่งเหตุการณ์

การจองสินค้าสามารถทำได้โดยเทียบกับการตั้งค่าแหล่งข้อมูลที่แตกต่างกัน เมื่อต้องการตั้งค่าคอนฟิกการจองชนิดนี้ อันดับแรกให้ระบุแหล่งข้อมูลในพารามิเตอร์ `dimensionDataSource` จากนั้น ในพารามิเตอร์ `dimensions` ให้ระบุมิติตามการตั้งค่ามิติในแหล่งข้อมูลเป้าหมาย

เมื่อคุณเรียกใช้ API การจอง คุณสามารถควบคุมการตรวจสอบความถูกต้องของการจองได้โดยการระบุพารามิเตอร์ `ifCheckAvailForReserv` แบบบูลีนในเนื้อหาคำขอ ค่า `True` หมายความว่าการตรวจสอบความถูกต้องนั้นต้องระบุ ในขณะที่ค่า `False` หมายความว่าการตรวจสอบความถูกต้องนั้นไม่จำเป็น ค่าเริ่มต้นคือ `True`

ถ้าคุณต้องการยกเลิกการจองหรือยกเลิกการจองปริมาณสินค้าคงคลังที่ระบุ ให้ตั้งค่าปริมาณเป็นค่าลบและตั้งค่าพารามิเตอร์ `ifCheckAvailForReserv` เป็น `False` เพื่อข้ามการตรวจสอบความถูกต้อง

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>สร้างเหตุการณ์การจองหลายเหตุการณ์

API นี้เป็นเวอร์ชันกลุ่มของ [API เหตุการณ์เดียว](#create-one-reservation-event)

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

## <a name="query-on-hand"></a>ปริมาณคงคลังคงเหลือของการสอบถาม

API _ปริมาณคงคลังคงเหลือของการสอบถาม_ ถูกใช้เพื่อดึงข้อมูลปริมาณคงคลังคงเหลือปัจจุบันสำหรับผลิตภัณฑ์ของคุณ

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

- `organizationId` ควรมีค่าเพียงค่าเดียว แต่ยังคงเป็นแถวลำดับ
- `productId` สามารถมีค่าหนึ่งค่าหรือมากกว่า ถ้าเป็นแถวลำดับที่ว่างเปล่า ผลิตภัณฑ์ทั้งหมดจะถูกส่งกลับ
- `siteId` และ `locationId` ใช้ในการแสดงผลสินค้าคงคลังในการพาร์ทิชัน คุณสามารถระบุค่า `siteId` ใน `locationId` มากกว่าหนึ่งค่าในคำขอ *แบบสอบถามคงเหลือ* ในรุ่นปัจจุบัน คุณต้องระบุทั้งค่า `siteId` และ `locationId`

พารามิเตอร์ `groupByValues` ควรเป็นไปตามการตั้งค่าคอนฟิกของคุณเกี่ยวกับการจัดดัชนี สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ ดูที่ [การตั้งค่าคอนฟิกตามลำดับชั้นของดัชนีผลิตภัณฑ์](./inventory-visibility-configuration.md#index-configuration)

พารามิเตอร์ `returnNegative` จะควบคุมว่าผลลัพธ์มีรายการค่าลบหรือไม่

ตัวอย่างต่อไปนี้จะแสดงเนื้อหาตัวอย่าง

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
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
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>การสอบถามโดยใช้วิธีการรับ

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
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
/api/environment/{environmentId}/onhand/indexquery?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
