---
title: สถานการณ์ที่ได้รับการสนับสนุนสำหรับการตั้งค่าการรวมแบบสองทิศทาง
description: หัวข้อนี้จะอธิบายสถานการณ์ที่ได้รับการสนับสนุนสำหรับการตั้งค่าการรวมแบบสองทิศทาง
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112528"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>สถานการณ์ที่ได้รับการสนับสนุนสำหรับการตั้งค่าการรวมแบบสองทิศทาง

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

คุณสามารถตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างสภาพแวดล้อม Finance and Operations และสภาพแวดล้อม Common Data Service

+ **สภาพแวดล้อม Finance and Operations** ให้แพลตฟอร์มพื้นฐานสำหรับ **แอป Finance and Operations** (ตัวอย่างเช่น Microsoft Dynamics 365 Finance Dynamics 365 Supply Chain Management Dynamics 365 Retail และ Dynamics 365 Human Resources)
+ **สภาพแวดล้อม Common Data Service** ให้แพลตฟอร์มพื้นฐานสำหรับ **แอปที่เป็นแบบโมเดลใน Dynamics 365** (Dynamics 365 Sales Dynamics 365 Customer Service Dynamics 365 Field Service Dynamics 365 Marketing และ Dynamics 365 Project Service Automation)

กลไกการตั้งค่าจะแตกต่างกันไป โดยขึ้นอยู่กับการบอกรับเป็นสมาชิกและสภาพแวดล้อมของคุณ

+ สำหรับอินสแตนซ์ใหม่ของแอป Finance and Operations การตั้งค่าของการเชื่อมต่อการรวมแบบสองทิศทางเริ่มต้นใน Microsoft Dynamics Lifecycle Services (LCS) ถ้าคุณมีลิขสิทธิ์สำหรับ Microsoft Power Platform คุณจะได้รับสภาพแวดล้อม Common Data Service ใหม่ ถ้าผู้เช่าของคุณไม่มี
+ สำหรับแอป Finance and Operations ของอินสแตนซ์ที่มีอยู่ การตั้งค่าของการเชื่อมต่อการรวมแบบสองทิศทางเริ่มต้นในสภาพแวดล้อม Finance and Operations

มีการสนับสนุนสถานการณ์จำลองของการตั้งค่าต่อไปนี้:

+ [อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่](#new-new)
+ [อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลที่มีอยู่](#new-existing)
+ [อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูลสาธิต และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่](#new-demo-new)
+ [อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูลสาธิต และอินสแตนซ์ของแอปที่เป็นแบบโมเดลที่มีอยู่](#new-demo-existing)
+ [อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่หรือที่มีอยู่](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่ไม่มีข้อมูลและอินสแตนซ์ใหม่ของแอปที่เป็นแบบโมเดลใน Dynamics 365 ให้ทำตามขั้นตอนใน [การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services](lcs-setup.md) เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์ จะเกิดการดำเนินการต่อไปนี้โดยอัตโนมัติ:

- สภาพแวดล้อม Finance and Operations ที่ใหม่และว่างเปล่าถูกเตรียมใช้งาน
- อินสแตนซ์ใหม่ที่ว่างเปล่าของแอปที่เป็นแบบโมเดลถูกเตรียมใช้งาน โดยที่มีการติดตั้งโซลูชันหลักของ CRM
- มีการสร้างการเชื่อมต่อการรวมแบบสองทิศทางสำหรับข้อมูลบริษัท DAT
- มีการเปิดใช้งานแผนผังเอนทิตีสำหรับการซิงโครไนส์ที่เริ่มใช้งานจริง

จากนั้น ทั้งสองสภาพแวดล้อมจะพร้อมสำหรับการซิงโครไนส์ข้อมูลที่เริ่มใช้งานจริง

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลที่มีอยู่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่ไม่มีข้อมูลและอินสแตนซ์ที่มีอยู่ของแอปที่เป็นแบบโมเดลใน Dynamics 365 ให้ทำตามขั้นตอนใน [การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services](lcs-setup.md) เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์ จะเกิดการดำเนินการต่อไปนี้โดยอัตโนมัติ:

- สภาพแวดล้อม Finance and Operations ที่ใหม่และว่างเปล่าถูกเตรียมใช้งาน
- มีการสร้างการเชื่อมต่อการรวมแบบสองทิศทางสำหรับข้อมูลบริษัท DAT
- มีการเปิดใช้งานแผนผังเอนทิตีสำหรับการซิงโครไนส์ที่เริ่มใช้งานจริง

จากนั้น ทั้งสองสภาพแวดล้อมจะพร้อมสำหรับการซิงโครไนส์ข้อมูลที่เริ่มใช้งานจริง

เมื่อต้องการซิงค์ข้อมูล Common Data Service ที่มีอยู่กับแอป Finance and Operations ให้ทำตามขั้นตอนต่อไปนี้

1. สร้างบริษัทใหม่ในแอป Finance and Operations
2. เพิ่มบริษัทในการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง
3. [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Common Data Service โดยใช้รหัสบริษัทองค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) แบบสามตัวอักษร

เนื่องจากการรวมแบบสองทิศทางอยู่ในโหมดการซิงโครไนส์ที่เริ่มใช้งานจริง ข้อมูลจาก Common Data Service จะเริ่มต้นโฟลว์ไปยังแอป Finance and Operations

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูลสาธิต และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่มีข้อมูลสาธิต และอินสแตนซ์ใหม่ของแอปที่เป็นแบบโมเดลใน Dynamics 365 ให้ทำตามขั้นตอนในส่วน [อินสแตนซ์ของแอป Finance and Operations ใหม่ อินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่](#new-new) ก่อนหน้าในหัวข้อนี้ เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์แล้ว ถ้าคุณต้องการซิงค์ข้อมูลสาธิตไปที่แอปที่เป็นแบบโมเดล ให้ทำตามขั้นตอนต่อไปนี้

1. เปิดแอป Finance and Operations จากหน้า LCS ลงชื่อเข้าใช้ และจากนั้น ไปที่ **การจัดการข้อมูล \> การรวมแบบสองทิศทาง**
2. รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับเอนทิตีที่คุณต้องการซิงค์ข้อมูล

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูลสาธิต และอินสแตนซ์ของแอปที่เป็นแบบโมเดลที่มีอยู่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่มีข้อมูลสาธิตและอินสแตนซ์ที่มีอยู่ของแอปที่เป็นแบบโมเดลใน Dynamics 365 ให้ทำตามขั้นตอนในส่วน [อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลที่มีอยู่](#new-existing) ก่อนหน้าในหัวข้อนี้ เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์แล้ว ถ้าคุณต้องการซิงค์ข้อมูลสาธิตไปที่แอปที่เป็นแบบโมเดล ให้ทำตามขั้นตอนต่อไปนี้

1. เปิดแอป Finance and Operations จากหน้า LCS ลงชื่อเข้าใช้ และจากนั้น ไปที่ **การจัดการข้อมูล \> การรวมแบบสองทิศทาง**
2. รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับเอนทิตีที่คุณต้องการซิงค์ข้อมูล

เมื่อต้องการซิงค์ข้อมูล Common Data Service ที่มีอยู่กับแอป Finance and Operations ให้ทำตามขั้นตอนต่อไปนี้

1. สร้างบริษัทใหม่ในแอป Finance and Operations
2. เพิ่มบริษัทในการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง
3. [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Common Data Service โดยใช้รหัสบริษัท ISO แบบสามตัวอักษร

เนื่องจากการรวมแบบสองทิศทางอยู่ในโหมดการซิงโครไนส์ที่เริ่มใช้งานจริง ข้อมูลจาก Common Data Service จะเริ่มต้นโฟลว์ไปยังแอป Finance and Operations

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอปที่เป็นแบบโมเดลใหม่หรือที่มีอยู่

การตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ที่มีอยู่ของแอป Finance and Operations และอินสแตนซ์ใหม่หรืออินสแตนซ์ที่มีอยู่ของแอปที่เป็นแบบโมเดลใน Dynamics 365 เกิดขึ้นในสภาพแวดล้อม Finance and Operation

1. ตั้งค่าการเชื่อมต่อจากแอป Finance and Operations
2. เมื่อต้องการซิงค์ข้อมูล Common Data Service ที่มีอยู่กับแอป Finance and Operations [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Common Data Service โดยใช้รหัสบริษัท ISO แบบอักษรสามตัว

เนื่องจากการรวมแบบสองทิศทางอยู่ในโหมดการซิงโครไนส์ที่เริ่มใช้งานจริง ข้อมูลจาก Common Data Service จะเริ่มต้นโฟลว์ไปยังแอป Finance and Operations
