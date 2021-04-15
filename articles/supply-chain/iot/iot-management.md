---
title: ตรวจสอบและจัดการเครื่องมือ IoT
description: หัวข้อนี้จะอธิบายถึงวิธีการตรวจสอบและจัดการเครื่องมือ IoT
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 94665b3646456b689a8e65e94b098e86e467d5e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813086"
---
# <a name="monitor-and-manage-iot-intelligence"></a>ตรวจสอบและจัดการเครื่องมือ IoT

[!include [banner](../../includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการตรวจสอบและจัดการเครื่องมือ IoT

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a> ตรวจสอบสถานการณ์จำลองใน Microsoft Dynamics 365 Supply Chain Management

คุณสามารถตรวจสอบการประมวลผลเครื่องมือ IoT จากสถานที่ต่างๆ ดังนี้:

+ **โมดูล \> การควบคุมการผลิต \> การสอบถามและรายงาน \> เครื่องมือ IoT \> การแจ้งเตือน** – ดูรายการของการแจ้งเตือนที่ยังไม่ได้แก้ไข
+ **โมดูล \> การควบคุมการผลิต \> การสอบถามและรายงาน \> เครื่องมือ IoT \> การแจ้งเตือนที่ปิด** – ดูรายการของการแจ้งเตือนที่ยังไม่ได้แก้ไขหรือถูกยกเลิก
+ **โมดูล \> การควบคุมการผลิต \> การสอบถามและรายงาน \> เครื่องมือ IoT \> คีย์การวัด** – ดูคีย์การวัดสำหรับแผนภูมิชุดเวลา **สถานะของทรัพยากร**
+ **โมดูล \> การควบคุมการผลิต \> การดำเนินการผลิต \> สถานะของทรัพยากร** – ติดตามการวัดเฉพาะโดยใช้กล่องโต้ตอบ **การตั้งค่าคอนฟิก** ถ้าสถานการณ์จำลองตรวจพบข้อยกเว้น การแจ้งเตือนจะแสดงรายละเอียดข้อยกเว้น
+ **พื้นที่ทำงาน \> การจัดการจัดการระบบการผลิต \> การแจ้งเตือน** – ดูรายการของการแจ้งเตือนที่ยังไม่ได้แก้ไข

## <a name="modify-a-running-iot-intelligence-scenario"></a>ปรับเปลี่ยนสถานการณ์จำลองเครื่องมือ IoT ที่ใช้งานอยู่

เมื่อสถานการณ์จำลองกำลังรันอยู่คุณสามารถทำการเปลี่ยนแปลงดังต่อไปนี้

+ เพิ่มข้อกำหนดของเค้าร่างเซ็นเซอร์ใหม่
+ เลือกค่าข้อมูลของสัญญาณใหม่
+ ยกเลิกการเลือกค่าข้อมูลของสัญญาณที่มีอยู่
+ เพิ่มและแม็ปค่าข้อมูลของสัญญาณใหม่
+ อัปเดตค่าขีดจำกัด

เมื่อสถานการณ์จำลองกำลังรันอยู่ ห้ามทำการเปลี่ยนแปลงดังต่อไปนี้:

+ ลบหรือปรับเปลี่ยนข้อกำหนดเค้าร่างใดๆ ที่มีการใช้งานอยู่ในปัจจุบันโดยสถานการณ์จำลองที่เปิดใช้งาน
+ เปลี่ยนเส้นทางเค้าร่างที่เลือกของสถานการณ์จำลองที่เปิดใช้งาน

## <a name="simulation-options"></a>ตัวเลือกการจำลอง

คุณสามารถจำลองสัญญาณเครื่องจักรโรงงานได้ สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อเหล่านี้:

+ [เชื่อมต่อ IoT DevKit AZ3166 กับฮับ Azure IoT](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [เชื่อมต่อกับโปรแกรมจำลอง Raspberry Pi ออนไลน์กับฮับ Azure IoT (Node.js)](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [ภาพรวมส่วนช่วยดำเนินการของโซลูชันการจำลองอุปกรณ์](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]