---
title: รูปแบบเค้าร่างสำหรับข้อความฮับ IoT
description: บทความนี้อธิบายวิธีการออกแบบเค้าร่างข้อความที่คุณสามารถใช้ในเครื่องมือ IoT
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6d133d520ce0a1dccb2575e352f63e6ceb2bd3f
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228646"
---
# <a name="schema-formats-for-iot-hub-messages"></a>รูปแบบเค้าร่างสำหรับข้อความฮับ IoT

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

บทความนี้อธิบายวิธีการออกแบบเค้าร่างข้อความที่คุณสามารถใช้ในเครื่องมือ IoT

## <a name="message-requirements"></a>ความต้องการของข้อความ

กฎต่อไปนี้ใช้กับการตรวจสอบข้อความในเครื่องมือ IoT:

+ เค้าร่างข้อความต้องอยู่ในรูปแบบ JavaScript Object Notation (JSON)
+ คุณสมบัติ **การประทับเวลา** UNIX โดยที่ค่าแสดงเป็นมิลลิวินาที (ms) ต้องมีอยู่ในข้อความฮับ IoT ของ Microsoft Azure
+ ข้อความจะมีการติดตามเฉพาะเมื่อประกอบด้วยคุณสมบัติทั้งหมดที่กําหนดไว้ในการตั้งค่าสถานการณ์ดังกล่าวเท่านั้น ตัวอย่างเช่น ถ้าคุณกําหนดคุณสมบัติ **รหัส** **การประทับเวลา** และ **ค่า** จะมีการตรวจสอบข้อความต่อไปนี้

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    ข้อความนี้ไม่ได้ตรวจสอบ เนื่องจากคุณสมบัติ **ค่า** ขาดหายไป

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ เครื่องมือ IoT ละเว้นคุณสมบัติในข้อความที่ไม่ได้กําหนดไว้ในการตั้งค่าคอนฟิกสถานการณ์ดังกล่าว ตัวอย่างเช่น ถ้าคุณกําหนดคุณสมบัติ **รหัส** **การประทับเวลา** และ **ค่า** เครื่องมือ IoT จะมีการตรวจสอบข้อความต่อไปนี้ทั้งหมด

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ เครื่องมือ IoT จะละเว้นข้อความที่ไม่ตรงกับเกณฑ์การตั้งค่าคอนฟิกสถานการณ์อย่างเงียบ
+ คุณสามารถกําหนดและใช้เค้าร่างข้อความได้หลายชนิด
+ ไม่ใช่ทุกชนิดที่จำเป็นต้องกําหนดเค้าร่างข้อความ เฉพาะเค้าร่างที่จะใช้กับสถานการณ์เครื่องมือ IoT เท่านั้นต้องกําหนด

## <a name="id-value-pair-schema"></a>เค้าร่างคู่ค่ารหัส

คู่ของค่ารหัสคือรูปแบบทั่วไปที่ใช้กับเค้าร่างข้อความเครื่องมือ IoT เมื่อใช้คู่ของค่ารหัส คุณตรวจสอบให้แน่ใจว่าเค้าร่างข้อความของคุณเป็นค่าเดียวกันได้ในทุกสถานการณ์ ตัวอย่างเช่น ต่อไปนี้เป็นข้อความสำหรับสถานการณ์ **การหยุดทำงานของอุปกรณ์** หรือ **การล่าช้าในการผลิต**

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

ต่อไปนี้เป็นข้อความสำหรับสถานการณ์ **คุณภาพผลิตภัณฑ์**

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

ทั้งข้อความก่อนหน้านี้จะมีคุณสมบัติ **รหัส** และ **ค่า** ค่า **รหัส** สามารถแม็ปในตาราง **ค่าข้อมูลสัญญาณ** ในระหว่างการตั้งค่าสถานการณ์ดังกล่าว สำหรับสถานการณ์ **การหยุดทำงานของอุปกรณ์** คุณจะต้องแม็ปค่า **IoTInt.Machine1225.PartOut** สำหรับสถานการณ์ **คุณภาพผลิตภัณฑ์** คุณจะต้องแม็ปค่า **IoTInt.Machine1225.Temperature**

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [คู่มือฮับ Azure IoT](/azure/iot-hub/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]