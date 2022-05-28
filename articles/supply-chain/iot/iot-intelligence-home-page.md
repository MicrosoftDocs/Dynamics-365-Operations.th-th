---
title: โฮมเพจเครื่องมือ IoT
description: หัวข้อนี้มีลิงค์ไปยังข้อมูลเกี่ยวกับเครื่องมือ IoT
author: johanhoffmann
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2386d71fde8196304fde846cbff4cd45d1edc834
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674434"
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

- **การล่าช้าในการผลิต** – สถานการณ์ดังกล่าวจะเปรียบเทียบเวลาวงจรจริงกับเวลาวงจรที่วางแผนไว้ Supply Chain Management แจ้งให้คุณทราบว่าการผลิตไม่เป็นไปตามกำหนดการ เพื่อให้คุณสามารถแทรกเพื่อเพิ่มประสิทธิภาพการดําเนินงานให้มีประสิทธิภาพสูงสุด และหลีกเลี่ยงความล่าช้าของใบสั่ง
- **การหยุดทำงานของอุปกรณ์** – สถานการณ์นี้จะเปรียบเทียบเวลาเวลาทำงานที่วัดได้กับพารามิเตอร์ที่กําหนดโดยผู้ใช้ Supply Chain Management แจ้งให้คุณทราบว่าเมื่อใดที่เกินขีดควบคุมความขัดข้อง เพื่อให้คุณสามารถจัดการได้ เช่น จัดตารางการผลิตใบสั่งผลิตใหม่ หรือสร้างใบสั่งงานการบํารุงรักษา
- **คุณภาพผลิตภัณฑ์** – สถานการณ์นี้จะเปรียบเทียบการอ่านค่าเซ็นเซอร์ เช่น ความชื้นและอุณหภูมิ กับเมตริกคุณภาพที่กําหนดโดยผู้ใช้ Supply Chain Management แจ้งให้คุณทราบว่าเมื่อใดที่การเบี่ยงเบนเกิดขึ้น เพื่อให้คุณสามารถเข้าแทรกเพื่อรักษามาตรฐานคุณภาพและลดการสิ้นเปลืองได้

ในภาพต่อไปนี้จะแสดงการโต้ตอบของฮับ Azure IoT เครื่องมือ IoT และ Supply Chain Management

![ฮับ Azure IoT เครื่องมือ IoT และ Supply Chain Management](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>การติดตามและการบำรุงรักษา

- [ตรวจสอบสถานการณ์จำลองใน Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
- [ปิดใช้งานสถานการณ์](iot-scenario-setup.md#disable-a-scenario)
- [ปรับเปลี่ยนสถานการณ์จำลองเครื่องมือ IoT ที่ใช้งานอยู่](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [ตัวเลือกการจำลอง](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]