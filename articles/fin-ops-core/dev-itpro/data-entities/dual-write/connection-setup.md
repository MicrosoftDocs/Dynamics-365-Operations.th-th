---
title: คำแนะนำการตั้งค่าการรวมแบบสองทิศทาง
description: บทความนี้จะอธิบายสถานการณ์ที่ได้รับการสนับสนุนสำหรับการตั้งค่าการรวมแบบสองทิศทาง
author: RamaKrishnamoorthy
ms.date: 06/28/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b27cabf495448fcd82edd374bb59e6e5a664c7e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289758"
---
# <a name="guidance-for-dual-write-setup"></a>คำแนะนำการตั้งค่าการรวมแบบสองทิศทาง

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



คุณสามารถตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างสภาพแวดล้อมการเงินและการดำเนินงาน กับสภาพแวดล้อม Dataverse

+ **สภาพแวดล้อมการเงินและการดำเนินงาน** มีแพลตฟอร์มพื้นฐานสำหรับ **แอปการเงินและการดำเนินงาน** (เช่น Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce และ Dynamics 365 Human Resources)
+ **สภาพแวดล้อม Dataverse** ให้แพลตฟอร์มพื้นฐานสำหรับ **แอปการมีส่วนร่วมของลูกค้า** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing และ Dynamics 365 Project Service Automation)


> [!IMPORTANT]
> โมดูล Human Resources ใน Dynamics 365 Finance รองรับการเชื่อมต่อการรวมแบบสองทิศทาง แต่แอป Dynamics 365 Human Resources ไม่รองรับ

กลไกการตั้งค่าจะแตกต่างกันไป โดยขึ้นอยู่กับการบอกรับเป็นสมาชิกและสภาพแวดล้อมของคุณ

+ สำหรับอินสแตนซ์ใหม่ของแอปการเงินและการดำเนินงาน การตั้งค่าของการเชื่อมต่อการรวมแบบสองทิศทางเริ่มต้นใน Microsoft Dynamics Lifecycle Services (LCS) ถ้าคุณมีลิขสิทธิ์สำหรับ Microsoft Power Platform คุณจะได้รับสภาพแวดล้อม Dataverse ใหม่ ถ้าผู้เช่าของคุณไม่มี
+ สำหรับอินสแตนซ์ที่มีอยู่ของแอปการเงินและการดำเนินงาน การตั้งค่าของการเชื่อมต่อการรวมแบบสองทิศทางเริ่มต้นในสภาพแวดล้อมการเงินและการดำเนินงาน

ก่อนที่คุณจะเริ่มต้นการรวมแบบสองทิศทางบนเอนทิตี คุณสามารถเรียกใช้การซิงค์เริ่มต้นเพื่อจัดการกับข้อมูลที่มีอยู่ในทั้งสองด้านของแอปการเงินและการดำเนินงาน และแอปการมีส่วนร่วมของลูกค้า คุณสามารถข้ามการซิงค์เริ่มต้น ถ้าคุณไม่จำเป็นต้องซิงโครไนส์ข้อมูลระหว่างสองสภาพแวดล้อม

การซิงโครไนส์เริ่มต้นช่วยให้คุณสามารถคัดลอกข้อมูลที่มีอยู่จากแอปหนึ่งไปยังอีกแอปหนึ่งแบบสองทิศทาง มีสถานการณ์จำลองการตั้งค่าหลายสถานการณ์ โดยขึ้นอยู่กับสภาพแวดล้อมที่คุณมีอยู่แล้วและชนิดของข้อมูลที่อยู่

มีการสนับสนุนสถานการณ์จำลองของการตั้งค่าต่อไปนี้:

+ [อินสแตนซ์ของแอปการเงินและการดำเนินงานใหม่กับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าใหม่](#new-new)
+ [อินสแตนซ์ของแอปการเงินและการดำเนินงานใหม่กับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าที่มีอยู่](#new-existing)
+ [อินสแตนซ์ของแอปการเงินและการดำเนินงานใหม่ที่มีข้อมูลกับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าใหม่](#new-data-new)
+ [อินสแตนซ์ของแอปการเงินและการดำเนินงานใหม่ที่มีข้อมูลกับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าที่มีอยู่](#new-data-existing)
+ [อินสแตนซ์ของแอปการเงินและการดำเนินงานที่มีอยู่กับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าใหม่](#existing-new)
+ [อินสแตนซ์ของแอปการเงินและการดำเนินงานที่มีอยู่กับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าที่มีอยู่](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>อินสแตนซ์ของแอปการเงินและการดำเนินงานใหม่กับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าใหม่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอปการเงินและการดำเนินงานที่ไม่มีข้อมูลกับอินสแตนซ์ใหม่ของแอปการมีส่วนร่วมของลูกค้า ให้ทำตามขั้นตอนใน [การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services](lcs-setup.md) เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์ จะเกิดการดำเนินการต่อไปนี้โดยอัตโนมัติ:

- สภาพแวดล้อมการเงินและการดําเนินงานใหม่ที่ว่างเปล่าถูกเตรียมใช้งานไว้
- อินสแตนซ์ใหม่ที่ว่างเปล่าของแอปการมีส่วนร่วมของลูกค้า ถูกเตรียมใช้งาน โดยที่มีการติดตั้งโซลูชันหลักของ CRM
- มีการสร้างการเชื่อมต่อการรวมแบบสองทิศทางสำหรับข้อมูลบริษัท DAT
- มีการเปิดใช้งานแผนผังตารางสำหรับการซิงโครไนส์ที่เริ่มใช้งานจริง

จากนั้น ทั้งสองสภาพแวดล้อมจะพร้อมสำหรับการซิงโครไนส์ข้อมูลที่เริ่มใช้งานจริง

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>อินสแตนซ์ของแอปการเงินและการดำเนินงานใหม่กับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าที่มีอยู่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอปการเงินและการดำเนินงานที่ไม่มีข้อมูลกับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าที่มีอยู่ ให้ทำตามขั้นตอนใน [การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services](lcs-setup.md) เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์ จะเกิดการดำเนินการต่อไปนี้โดยอัตโนมัติ:

- สภาพแวดล้อมการเงินและการดําเนินงานใหม่ที่ว่างเปล่าถูกเตรียมใช้งานไว้
- มีการสร้างการเชื่อมต่อการรวมแบบสองทิศทางสำหรับข้อมูลบริษัท DAT
- มีการเปิดใช้งานแผนผังตารางสำหรับการซิงโครไนส์ที่เริ่มใช้งานจริง

จากนั้น ทั้งสองสภาพแวดล้อมจะพร้อมสำหรับการซิงโครไนส์ข้อมูลที่เริ่มใช้งานจริง

เมื่อต้องการซิงค์ข้อมูล Dataverse ที่มีอยู่กับแอปการเงินและการดำเนินงาน ให้ทำตามขั้นตอนต่อไปนี้

1. สร้างบริษัทใหม่ในแอปการเงินและการดำเนินงาน
2. เพิ่มบริษัทในการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง
3. [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Dataverse โดยใช้รหัสบริษัทองค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) แบบสามตัวอักษร
4. เรียกใช้ฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

สำหรับลิงค์ไปยังตัวอย่างและแนวทางอื่น ให้ดูที่ส่วน [ตัวอย่าง](#example) ต่อไปนี้ในบทความนี้

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>อินสแตนซ์ของแอปการเงินและการดำเนินงานใหม่ที่มีข้อมูลกับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าใหม่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอปการเงินและการดำเนินงานที่มีข้อมูลกับอินสแตนซ์ใหม่ของแอปการมีส่วนร่วมของลูกค้า ให้ทำตามขั้นตอนในส่วน [อินสแตนซ์ของแอปการเงินและการดำเนินงานใหม่กับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าใหม่](#new-new) ก่อนหน้าในบทความนี้ เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์แล้ว ถ้าคุณต้องการซิงค์ข้อมูลไปที่แอปการมีส่วนร่วมของลูกค้า ให้ทำตามขั้นตอนต่อไปนี้

1. เปิดแอปการเงินและการดำเนินงานจากหน้า LCS ลงชื่อเข้าใช้ และจากนั้น ไปที่ **การจัดการข้อมูล \> การรวมแบบสองทิศทาง**
2. เรียกใช้ฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

สำหรับลิงค์ไปยังตัวอย่างและแนวทางอื่น ให้ดูที่ส่วน [ตัวอย่าง](#example)

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>อินสแตนซ์ของแอปการเงินและการดำเนินงานใหม่ที่มีข้อมูลกับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าที่มีอยู่

เมื่อต้องการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ใหม่ของแอปการเงินและการดำเนินงานที่มีข้อมูลกับอินสแตนซ์ที่มีอยู่ของแอปการมีส่วนร่วมของลูกค้า ให้ทำตามขั้นตอนในส่วน [อินสแตนซ์ของแอปการเงินและการดำเนินงานใหม่กับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าที่มีอยู่](#new-existing) ก่อนหน้าในบทความนี้ เมื่อการตั้งค่าการเชื่อมต่อเสร็จสมบูรณ์แล้ว ถ้าคุณต้องการซิงค์ข้อมูลไปที่แอปการมีส่วนร่วมของลูกค้า ให้ทำตามขั้นตอนต่อไปนี้

1. เปิดแอปการเงินและการดำเนินงานจากหน้า LCS ลงชื่อเข้าใช้ และจากนั้น ไปที่ **การจัดการข้อมูล \> การรวมแบบสองทิศทาง**
2. เรียกใช้ฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

เมื่อต้องการซิงค์ข้อมูล Dataverse ที่มีอยู่กับแอปการเงินและการดำเนินงาน ให้ทำตามขั้นตอนต่อไปนี้

1. สร้างบริษัทใหม่ในแอปการเงินและการดำเนินงาน
2. เพิ่มบริษัทในการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง
3. [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Dataverse โดยใช้รหัสบริษัท ISO แบบสามตัวอักษร
4. เรียกใช้ฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

สำหรับลิงค์ไปยังตัวอย่างและแนวทางอื่น ให้ดูที่ส่วน [ตัวอย่าง](#example)

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>อินสแตนซ์ของแอปการเงินและการดำเนินงานที่มีอยู่กับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าใหม่

การตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ที่มีอยู่ของแอปการเงินและการดำเนินงานกับอินสแตนซ์ใหม่ของแอปการมีส่วนร่วมของลูกค้าที่เกิดขึ้นในสภาพแวดล้อมการเงินและการดำเนินงาน

1. [ตั้งค่าการเชื่อมต่อจากแอปการเงินและการดำเนินงาน](enable-dual-write.md)
2. เรียกใช้ฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

สำหรับลิงค์ไปยังตัวอย่างและแนวทางอื่น ให้ดูที่ส่วน [ตัวอย่าง](#example)

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>อินสแตนซ์ของแอปการเงินและการดำเนินงานที่มีอยู่กับอินสแตนซ์ของแอปการมีส่วนร่วมของลูกค้าที่มีอยู่

การตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างอินสแตนซ์ที่มีอยู่ของแอปการเงินและการดำเนินงานกับอินสแตนซ์ที่มีอยู่ของแอปการมีส่วนร่วมของลูกค้าที่เกิดขึ้นในสภาพแวดล้อมการเงินและการดำเนินงาน

1. [ตั้งค่าการเชื่อมต่อจากแอปการเงินและการดำเนินงาน](enable-dual-write.md)
2. เมื่อต้องการซิงค์ข้อมูล Dataverse ที่มีอยู่กับแอปการเงินและการดำเนินงาน [เริ่มต้นระบบ](bootstrap-company-data.md) ข้อมูล Dataverse โดยใช้รหัสบริษัท ISO แบบอักษรสามตัว
3. เรียกใช้ฟังก์ชัน **การซิงค์เริ่มต้น** สำหรับตารางคุณต้องการซิงค์ข้อมูล

สำหรับลิงค์ไปยังตัวอย่างและแนวทางอื่น ให้ดูที่ส่วน [ตัวอย่าง](#example)

## <a name="example"></a>ตัวอย่าง

สำหรับตัวอย่างเช่น ให้ดูที่ [การเปิดใช้งานลูกค้า V3 —แผนผังตารางของผู้ติดต่อ](enable-entity-map.md#enable-table-map)

สำหรับแนวทางอื่นที่ยึดตามปริมาณข้อมูลในแต่ละเอนทิตีที่ต้องเรียกใช้การซิงค์เริ่มต้น ให้ดูที่ [ข้อควรพิจารณาสำหรับการซิงโครไนส์เริ่มต้น](initial-sync-guidance.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
