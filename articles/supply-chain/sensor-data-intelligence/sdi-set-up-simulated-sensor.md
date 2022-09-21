---
title: การตั้งค่าเซ็นเซอร์จำลองเพื่อการทดสอบ
description: หัวข้อนี้จะอธิบายวิธีตั้งค่าการจำลองที่คุณสามารถใช้เพื่อทดสอบ Sensor Data Intelligence โดยไม่ติดตั้งเซ็นเซอร์ทางกายภาพใดๆ
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: edfa20bec7438124844f8b6afa91ca4941b6bb56
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428460"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>การตั้งค่าเซ็นเซอร์จำลองเพื่อการทดสอบ

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

ทดสอบ Sensor Data Intelligence โดยไม่ติดตั้งเซ็นเซอร์ทางกายภาพใดๆ คุณสามารถใช้บริการ *Raspberry PI Azure IoT Online Simulator* เพื่อทดสอบสัญญาณของเซ็นเซอร์ และส่งให้โซลูชัน Internet of Things (IoT) ของคุณบน Microsoft Azure หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับโปรแกรมจำลอง โปรดดูที่ [เชื่อมต่อโปรแกรมจริงออนไลน์ Raspberry Pi กับ Azure IoT Hub (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)

## <a name="create-a-device-in-azure-iot-hub"></a>สร้างอุปกรณ์ใน Azure IoT Hub

ก่อนอื่น คุณต้องตั้งค่าอุปกรณ์เพื่อรับรองความถูกต้องของสัญญาณของเซ็นเซอร์ไปยัง Azure IoT Hub

1. ใน Azure ให้ไปที่รายการทรัพยากรของกลุ่มทรัพยากรที่คุณสร้างเพื่อใช้งานกับ Sensor Data Intelligence (ดูข้อมูลเพิ่มเติมที่ [ปรับใช้โซลูชัน IoT ใน Azure](sdi-deploy-iot-solution-on-azure.md))
1. ในรายการทรัพยากร ให้ค้นหาเรกคอร์ดที่มีการตั้งค่าฟิลด์ **ชนิด** เป็น *IoT Hub* ในคอลัมน์ **ชื่อ** เลือกชื่อเพื่อเปิดหน้ารายละเอียดสำหรับทรัพยากร
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **อุปกรณ์**
1. บนหน้า **อุปกรณ์** เลือก **เพิ่มอุปกรณ์**
1. บนหน้า **สร้างอุปกรณ์** ตั้งค่าฟิลด์ต่อไปนี้

    - **รหัสอุปกรณ์** – ป้อนชื่อของอุปกรณ์ใหม่ (ตัวอย่างเช่น *My-IoT-Device*)
    - **ชนิดการรับรองความถูกต้อง** – เลือก *คีย์สมมาตร*
    - **สร้างคีย์โดยอัตโนมัติ** – เลือกกล่องกาเครื่องหมายนี้
    - **เชื่อมต่ออุปกรณ์นี้กับ IoT hub** – เลือก *เปิดใช้งาน*

1. เลือก **บันทึก** เพื่อกลับไปที่หน้า **อุปกรณ์**
1. ค้นหาอุปกรณ์ใหม่ในรายการ ในคอลัมน์ **รหัสอุปกรณ์** เลือกชื่อเพื่อเปิดหน้ารายละเอียดสำหรับอุปกรณ์ หากคุณไม่เห็นอุปกรณ์ใหม่ในรายการ ให้รีเฟรชหน้า
1. คัดลอกค่า **สตริงการเชื่อมต่อหลัก** (ตัวอย่างเช่น โดยการเลือกปุ่ม **คัดลอกไปยังคลิปบอร์ด**) คุณจะต้องใช้ค่านี้ในภายหลังเมื่อคุณตั้งค่าการจำลอง Raspberry Pi IoT เพื่อทดสอบสัญญาณของเซ็นเซอร์ ดังนั้นจึงควรพิจารณาวางลงในไฟล์ข้อความในขณะนี้

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>เพิ่มสตริงการเชื่อมต่อ Azure ลงในโปรแกรมจำลอง Raspberry Pi IoT

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อเพิ่มสตริงการเชื่อมต่อจากอุปกรณ์ใน Azure IoT Hub ลงในสคริปต์ในบริการ Raspberry

1. เปิด [โปรแกรมจำลอง Raspberry Pi IoT](https://azure-samples.github.io/raspberry-pi-web-simulator/)
1. ในบานหน้าต่างโปรแกรมแก้ไขรหัส ให้ค้นหาบรรทัดที่มีคำสั่งต่อไปนี้

    `const connectionString = '[Your IoT hub device connection string]';`

1. แทนที่ข้อความวิธีใช้ รวมถึงวงเล็บด้วยค่า **สตริงการเชื่อมต่อหลัก** ที่คุณคัดลอกในส่วนก่อนหน้านี้ ผลลัพธ์ควรมีลักษณะคล้ายกับตัวอย่างต่อไปนี้

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>เพิ่มรหัสเซ็นเซอร์และค่าลงในส่วนข้อมูลในโปรแกรมจำลอง Raspberry Pi IoT

ตอนนี้คุณต้องตั้งค่าโปรแกรมจําลอง Raspberry Pi IoT ด้วยเซ็นเซอร์ที่จำลองและค่าที่พวกเขาจะส่งเป็นส่วนข้อมูล

- ในตัวแก้ไขโค้ดของโปรแกรมจำลอง Raspberry Pi IoT ให้ค้นหาฟังก์ชัน `getMessage` และแก้ไขให้ตรงกับรหัสต่อไปนี้ (เซ็นเซอร์มีการตั้งค่าในบรรทัด `cb()`)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > รหัสเซ็นเซอร์ที่กําหนดไว้ในโปรแกรมแก้ไขรหัสของโปรแกรมจำลอง Raspberry Pi IoT ต้องเหมือนกับรหัสของเซ็นเซอร์ที่คุณจะระบุในภายหลังให้กับสถานการณ์ใน Supply Chain Management รหัสตัวอย่างก่อนหน้านี้จะใช้รหัสเซ็นเซอร์ที่อ่านได้แบบมนุษย์ อย่างไรก็ตาม ในสถานการณ์จริง รหัสเซ็นเซอร์จะเป็นค่ารหัสเฉพาะสากล (GUID) ที่จัดหาให้โดยผู้ผลิตเซ็นเซอร์ รหัสเซ็นเซอร์ที่อ่านได้แบบมนุษย์ซึ่งใช้ในรหัสตัวอย่างนี้ยังใช้อยู่ในตัวอย่างใน [สถานการณ์คุณภาพของผลิตภัณฑ์](sdi-scenario-product-quality.md) [สถานการณ์บำรุงรักษาสินทรัพย์](sdi-scenario-asset-maintenance.md) [สถานการณ์ความล่าช้าของการผลิต](sdi-scenario-production-delays.md) และ [สถานการณ์สถานะของเครื่องจักร](sdi-scenario-equipment-downtime.md)) ดังนั้น ให้ใช้รหัสนี้หากคุณจะใช้งานในสถานการณ์ดังกล่าว

## <a name="edit-the-interval-for-sending-sensor-signals"></a>แก้ไขช่วงเวลาของการส่งข้อมูลสัญญาณเซ็นเซอร์

ขณะนี้คุณต้องกําหนดช่วงเวลาที่โปรแกรมจำลอง Raspberry Pi IoT ควรส่งสัญญาณของเซ็นเซอร์ที่สะสม

1. ในการโปรแกรมแก้ไขรหัสของโปรแกรมจำลอง Raspberry Pi IoT ให้ค้นหาการเรียกฟังก์ชันต่อไปนี้

    `setInterval(sendMessage, 2000);`

2. ตามค่าเริ่มต้น โปรแกรมจำลอง Raspberry Pi IoT จะส่งสัญญาณของเซ็นเซอร์ทุกๆ 2,000 ล้านมิลลิวินาที (สองวินาที) คุณสามารถเปลี่ยนค่าได้ตามที่คุณต้องการ

## <a name="run-the-raspberry-pi-iot-simulator"></a>รันโปรแกรมจำลอง Raspberry Pi IoT

- เลือก **รัน** เพื่อเริ่มต้นโปรแกรมจําลิง และเริ่มส่งข้อมูลเซ็นเซอร์ที่จําลอง
