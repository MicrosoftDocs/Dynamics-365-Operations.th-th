---
title: โฮมเพจเครื่องมือ IoT
description: หัวข้อนี้มีลิงค์ไปยังข้อมูลเกี่ยวกับเครื่องมือ IoT
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782692"
---
# <a name="iot-intelligence-home-page"></a>โฮมเพจเครื่องมือ IoT

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> ขณะนี้คุณลักษณะนี้พร้อมใช้งานเฉพาะในประเทศ/ภูมิภาคต่อไปนี้เท่านั้น:
>
> - US (สหรัฐอเมริกา)
> - EU (สหภาพยุโรป)
> - AU (ออสเตรเลีย)
> - CA (แคนาดา)
> - UK (สหราชอาณาจักร)

เครื่องมือ IoT เป็น Add-in ของ Microsoft Dynamics 365 Supply Chain Management โดยรวมสัญญาณ Internet of Things (IoT) เข้ากับข้อมูลใน Supply Chain Management เพื่อสร้างข้อมูลเชิงลึกที่สามารถนำไปใช้ได้

เครื่องมือ IoT สนับสนุนสถานการณ์ต่อไปนี้:

+ **การล่าช้าในการผลิต** – สถานการณ์ดังกล่าวจะเปรียบเทียบเวลาวงจรจริงกับเวลาวงจรที่วางแผนไว้ Supply Chain Management แจ้งให้คุณทราบว่าการผลิตไม่เป็นไปตามกำหนดการ เพื่อให้คุณสามารถแทรกเพื่อเพิ่มประสิทธิภาพการดําเนินงานให้มีประสิทธิภาพสูงสุด และหลีกเลี่ยงความล่าช้าของใบสั่ง
+ **การหยุดทำงานของอุปกรณ์** – สถานการณ์นี้จะเปรียบเทียบเวลาเวลาทำงานที่วัดได้กับพารามิเตอร์ที่กําหนดโดยผู้ใช้ Supply Chain Management แจ้งให้คุณทราบว่าเมื่อใดที่เกินขีดควบคุมความขัดข้อง เพื่อให้คุณสามารถจัดการได้ เช่น จัดตารางการผลิตใบสั่งผลิตใหม่ หรือสร้างใบสั่งงานการบํารุงรักษา
+ **คุณภาพผลิตภัณฑ์** – สถานการณ์นี้จะเปรียบเทียบการอ่านค่าเซ็นเซอร์ เช่น ความชื้นและอุณหภูมิ กับเมตริกคุณภาพที่กําหนดโดยผู้ใช้ Supply Chain Management แจ้งให้คุณทราบว่าเมื่อใดที่การเบี่ยงเบนเกิดขึ้น เพื่อให้คุณสามารถเข้าแทรกเพื่อรักษามาตรฐานคุณภาพและลดการสิ้นเปลืองได้

ในภาพต่อไปนี้จะแสดงการโต้ตอบของฮับ Azure IoT เครื่องมือ IoT และ Supply Chain Management

![ฮับ Azure IoT เครื่องมือ IoT และ Supply Chain Management](media/iot_intelligence.png)

## <a name="setup"></a>ตั้งค่า

คุณสามารถตั้งค่าและตั้งค่าคอนฟิกเครื่องมือ IoT โดยไม่เขียนโค้ดใดๆ ต่อไปนี้เป็นขั้นตอนพื้นฐาน

1. [ตั้งค่าทรัพยากร Azure](iot-azure-setup.md) – สร้างฮับ IoT แคช Redis และ Key Vault ที่สามารถเข้าถึงได้จาก Supply Chain Management
2. [รูปแบบเค้าร่างข้อความของฮับ IoT](iot-schema-format.md) – ตั้งค่าคอนฟิกอุปกรณ์ให้ส่งข้อความไปยังฮับ IoT และกําหนดรูปแบบข้อความ JavaScript Object Notation (JSON)
3. ในการจัดการคุณลักษณะ ให้เปิดใช้งานแฟล็กคุณลักษณะเครื่องมือ IoT 
4. [ติดตั้ง Add-in ของเครื่องมือ IoT ใน Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – ติดตั้ง Add-in LCS และตั้งค่าคอนฟิกข้อมูลลับ Azure
5. [ตั้งค่าเมตริก](iot-metrics-setup.md) – ตั้งค่าเมตริกใน Supply Chain Management
6. [การตั้งค่าสถานการณ์](iot-scenario-setup.md) – ตั้งค่าสถานการณ์ใน Supply Chain Management

## <a name="tracking-and-maintenance"></a>การติดตามและการบำรุงรักษา

+ [ตรวจสอบสถานการณ์จำลองใน Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
+ [ปิดใช้งานสถานการณ์](iot-scenario-setup.md#disable-a-scenario)
+ [ถอนการติดตั้ง Add-in](iot-lcs-setup.md#uninstall-addin)
+ [ปรับเปลี่ยนสถานการณ์จำลองเครื่องมือ IoT ที่ใช้งานอยู่](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [ตัวเลือกการจำลอง](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]