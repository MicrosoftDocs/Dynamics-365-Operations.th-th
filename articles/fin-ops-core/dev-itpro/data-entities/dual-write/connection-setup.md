---
title: คำแนะนำการตั้งค่าการรวมแบบสองทิศทาง
description: หัวข้อนี้จะอธิบายสถานการณ์ที่ได้รับการสนับสนุนสำหรับการตั้งค่าการรวมแบบสองทิศทาง
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 78a7cdc18476a1c523c83c92ca6f354c3ba806dc
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744864"
---
# <a name="guidance-for-dual-write-setup"></a>คำแนะนำการตั้งค่าการรวมแบบสองทิศทาง

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

คุณสามารถตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างสภาพแวดล้อม Finance and Operations และสภาพแวดล้อม Dataverse

+ **สภาพแวดล้อม Finance and Operations** ให้แพลตฟอร์มพื้นฐานสำหรับ **แอป Finance and Operations** (ตัวอย่างเช่น Microsoft Dynamics 365 Finance Dynamics 365 Supply Chain Management Dynamics 365 Commerce และ Dynamics 365 Human Resources)
+ **สภาพแวดล้อม Dataverse** ให้แพลตฟอร์มพื้นฐานสำหรับ **แอป Customer Engagement** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing และ Dynamics 365 Project Service Automation)

> [!IMPORTANT]
> โมดูล Human Resources ใน Dynamics 365 Finance รองรับการเชื่อมต่อการรวมแบบสองทิศทาง แต่แอป Dynamics 365 Human Resources ไม่รองรับ

กลไกการตั้งค่าจะแตกต่างกันไป โดยขึ้นอยู่กับการบอกรับเป็นสมาชิกและสภาพแวดล้อมของคุณ

+ สำหรับอินสแตนซ์ใหม่ของแอป Finance and Operations การตั้งค่าของการเชื่อมต่อการรวมแบบสองทิศทางเริ่มต้นใน Microsoft Dynamics Lifecycle Services (LCS) ถ้าคุณมีลิขสิทธิ์สำหรับ Microsoft Power Platform คุณจะได้รับสภาพแวดล้อม Dataverse ใหม่ ถ้าผู้เช่าของคุณไม่มี
+ สำหรับแอป Finance and Operations ของอินสแตนซ์ที่มีอยู่ การตั้งค่าของการเชื่อมต่อการรวมแบบสองทิศทางเริ่มต้นในสภาพแวดล้อม Finance and Operations

ก่อนที่คุณจะเริ่มต้นการรวมแบบสองทิศทางบนเอนทิตี คุณสามารถรันการซิงค์เริ่มต้นเพื่อจัดการกับข้อมูลที่มีอยู่ในทั้งสองด้านของแอป: Finance and Operations และแอป Customer Engagement คุณสามารถข้ามการซิงค์เริ่มต้น ถ้าคุณไม่จำเป็นต้องซิงโครไนส์ข้อมูลระหว่างสองสภาพแวดล้อม

การซิงโครไนส์เริ่มต้นช่วยให้คุณสามารถคัดลอกข้อมูลที่มีอยู่จากแอปหนึ่งไปยังอีกแอปหนึ่งแบบสองทิศทาง มีสถานการณ์จำลองการตั้งค่าหลายสถานการณ์ โดยขึ้นอยู่กับสภาพแวดล้อมที่คุณมีอยู่แล้วและชนิดของข้อมูลที่อยู่

มีการสนับสนุนสถานการณ์จำลองของการตั้งค่าต่อไปนี้:

+ [อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอป Customer Engagement ใหม่](#new-new)
+ [อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่](#new-existing)
+ [อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูล และอินสแตนซ์ของแอป Customer Engagement ใหม่](#new-data-new)
+ [อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูล และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่](#new-data-existing)
+ [อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอป Customer Engagement ใหม่](#existing-new)
+ [อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอป Customer Engagement ใหม่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่ไม่มีข้อมูล และอินสแตนซ์ใหม่ของแอป Customer Engagement ให้ทำตามขั้นตอนใน [การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services](lcs-setup.md) เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์ จะเกิดการดำเนินการต่อไปนี้โดยอัตโนมัติ:

- สภาพแวดล้อม Finance and Operations ที่ใหม่และว่างเปล่าถูกเตรียมใช้งาน
- อินสแตนซ์ใหม่ที่ว่างเปล่าของแอป Customer Engagement ถูกเตรียมใช้งาน โดยที่มีการติดตั้งโซลูชันหลักของ CRM
- มีการสร้างการเชื่อมต่อการรวมแบบสองทิศทางสำหรับข้อมูลบริษัท DAT
- มีการเปิดใช้งานแผนผังตารางสำหรับการซิงโครไนส์ที่เริ่มใช้งานจริง

จากนั้น ทั้งสองสภาพแวดล้อมจะพร้อมสำหรับการซิงโครไนส์ข้อมูลที่เริ่มใช้งานจริง

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>อินสแตนซ์ของแอป Finance and Operations ใหม่ และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่ไม่มีข้อมูล และอินสแตนซ์ที่มีอยู่ของแอป Customer Engagement ให้ทำตามขั้นตอนใน [การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services](lcs-setup.md) เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์ จะเกิดการดำเนินการต่อไปนี้โดยอัตโนมัติ:

- สภาพแวดล้อม Finance and Operations ที่ใหม่และว่างเปล่าถูกเตรียมใช้งาน
- มีการสร้างการเชื่อมต่อการรวมแบบสองทิศทางสำหรับข้อมูลบริษัท DAT
- มีการเปิดใช้งานแผนผังตารางสำหรับการซิงโครไนส์ที่เริ่มใช้งานจริง

จากนั้น ทั้งสองสภาพแวดล้อมจะพร้อมสำหรับการซิงโครไนส์ข้อมูลที่เริ่มใช้งานจริง

เมื่อต้องการซิงค์ข้อมูล Dataverse ที่มีอยู่กับแอป Finance and Operations ให้ทำตามขั้นตอนต่อไปนี้

1. สร้างบริษัทใหม่ในแอป Finance and Operations
2. เพิ่มบริษัทในการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง
3. [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Dataverse โดยใช้รหัสบริษัทองค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) แบบสามตัวอักษร
4. รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

สำหรับลิงค์ไปยังตัวอย่างและแนวทางอื่น ให้ดูที่ส่วน [ตัวอย่าง](#example) ต่อไปนี้ในหัวข้อนี้

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูล และอินสแตนซ์ของแอป Customer Engagement ใหม่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่มีข้อมูล และอินสแตนซ์ใหม่ของแอป Customer Engagement ให้ทำตามขั้นตอนในส่วน [อินสแตนซ์ของแอป Finance and Operations ใหม่ อินสแตนซ์ของแอป Customer Engagement ใหม่](#new-new) ก่อนหน้าในหัวข้อนี้ เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์แล้ว ถ้าคุณต้องการซิงค์ข้อมูลไปที่แอป Customer Engagement ให้ทำตามขั้นตอนต่อไปนี้

1. เปิดแอป Finance and Operations จากหน้า LCS ลงชื่อเข้าใช้ และจากนั้น ไปที่ **การจัดการข้อมูล \> การรวมแบบสองทิศทาง**
2. รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

สำหรับลิงค์ไปยังตัวอย่างและแนวทางอื่น ให้ดูที่ส่วน [ตัวอย่าง](#example)

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>อินสแตนซ์ของแอป Finance and Operations ใหม่ที่มีข้อมูล และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอป Finance and Operations ที่มีข้อมูล และอินสแตนซ์ใหที่มีอยู่ของแอป Customer Engagement ให้ทำตามขั้นตอนในส่วน [อินสแตนซ์ของแอป Finance and Operations ใหม่ อินสแตนซ์ของแอป Customer Engagement ที่มีอยู่](#new-existing) ก่อนหน้าในหัวข้อนี้ เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์แล้ว ถ้าคุณต้องการซิงค์ข้อมูลไปที่แอป Customer Engagement ให้ทำตามขั้นตอนต่อไปนี้

1. เปิดแอป Finance and Operations จากหน้า LCS ลงชื่อเข้าใช้ และจากนั้น ไปที่ **การจัดการข้อมูล \> การรวมแบบสองทิศทาง**
2. รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

เมื่อต้องการซิงค์ข้อมูล Dataverse ที่มีอยู่กับแอป Finance and Operations ให้ทำตามขั้นตอนต่อไปนี้

1. สร้างบริษัทใหม่ในแอป Finance and Operations
2. เพิ่มบริษัทในการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง
3. [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Dataverse โดยใช้รหัสบริษัท ISO แบบสามตัวอักษร
4. รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

สำหรับลิงค์ไปยังตัวอย่างและแนวทางอื่น ให้ดูที่ส่วน [ตัวอย่าง](#example)

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอป Customer Engagement ใหม่

การตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ที่มีอยู่ของแอป Finance and Operations และอินสแตนซ์ใหม่ของแอป Customer Engagement ที่เกิดขึ้นในสภาพแวดล้อม Finance and Operation

1. [ตั้งค่าการเชื่อมต่อจากแอป Finance and Operations](enable-dual-write.md)
2. รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

สำหรับลิงค์ไปยังตัวอย่างและแนวทางอื่น ให้ดูที่ส่วน [ตัวอย่าง](#example)

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>อินสแตนซ์ของแอป Finance and Operations ที่มีอยู่ และอินสแตนซ์ของแอป Customer Engagement ที่มีอยู่

การตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ที่มีอยู่ของแอป Finance and Operations และอินสแตนซ์ที่มีอยู่ของแอป Customer Engagement ที่เกิดขึ้นในสภาพแวดล้อม Finance and Operation

1. [ตั้งค่าการเชื่อมต่อจากแอป Finance and Operations](enable-dual-write.md)
2. เมื่อต้องการซิงค์ข้อมูล Dataverse ที่มีอยู่กับแอป Finance and Operations [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Dataverse โดยใช้รหัสบริษัท ISO แบบอักษรสามตัว
3. รันฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

สำหรับลิงค์ไปยังตัวอย่างและแนวทางอื่น ให้ดูที่ส่วน [ตัวอย่าง](#example)

## <a name="example"></a>ตัวอย่าง

สำหรับตัวอย่างเช่น ให้ดูที่ [การเปิดใช้งานลูกค้า V3 —แผนผังตารางของผู้ติดต่อ](enable-entity-map.md#enable-table-map)

สำหรับแนวทางอื่นที่ยึดตามปริมาณข้อมูลในแต่ละเอนทิตีที่ต้องรันการซิงค์เริ่มต้น ให้ดูที่ [ข้อควรพิจารณาสำหรับการซิงโครไนส์เริ่มต้น](initial-sync-guidance.md)
