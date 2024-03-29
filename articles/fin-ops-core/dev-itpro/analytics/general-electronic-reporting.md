---
title: ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)
description: บทความนี้แสดงภาพรวมของเครื่องมือการรายงานทางอิเล็กทรอนิกส์ ซึ่งอธิบายแนวคิดหลัก สถานการณ์ที่สนับสนุน และรูปแบบ ที่เป็นส่วนหนึ่งของโซลูชัน
author: kfend
ms.date: 11/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941,  ""intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: e94846dd565abb6de2c1f07532d285e28307e9a2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269705"
---
# <a name="electronic-reporting-er-overview"></a>ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)

[!include [banner](../includes/banner.md)]

บทความนี้แสดงภาพรวมของเครื่องมือการรายงานทางอิเล็กทรอนิกส์ (ER) ซึ่งรวมถึงข้อมูลเกี่ยวกับแนวคิดหลัก สถานการณ์จำลองที่ ER สนับสนุน และรายการรูปแบบที่ได้รับการออกแบบและนำออกใช้เป็นส่วนหนึ่งของโซลูชัน

ER เป็นเครื่องมือที่สามารถตั้งค่าคอนฟิกได้ ซึ่งจะช่วยคุณสร้างและรักษาการรายงานและการชำระเงินทางอิเล็กทรอนิกส์ตามระเบียบบังคับ โดยเป็นไปตามแนวคิดสามอย่างต่อไปนี้

- การตั้งค่าคอนฟิกแทนการเขียนโค้ด:

    - การตั้งค่าคอนฟิกสามารถทำได้โดยผู้ใช้ธุรกิจและไม่ต้องใช้นักพัฒนา
    - โมเดลข้อมูลจะกําหนดในแง่ธุรกิจ
    - โปรแกรมแก้ไขภาพใช้ในการสร้างส่วนประกอบทั้งหมดของการตั้งค่าคอนฟิก ER
    - ภาษาที่ใช้กับการแปลงข้อมูลจะคล้ายคลึงกับภาษาที่ใช้ใน Microsoft Excel

- การตั้งค่าคอนฟิกเดียวสำหรับ Dynamics 365 Finance หลายรุ่น:

    - จัดการรูปแบบข้อมูลเฉพาะโดเมนหนึ่งที่กําหนดในแง่ธุรกิจ
    - แยกรายละเอียดการการปล่อยแอปพลิเคชันในการแมปรูปแบบข้อมูลตามรุ่น
    - รักษาการตั้งค่าคอนฟิกหนึ่งรูปแบบสำหรับหลายรุ่นของรุ่นปัจจุบันตามรูปแบบข้อมูล

- การอัปเกรดแบบง่ายหรืออัตโนมัติ:

    - รองรับการกำหนดรุ่นของการตั้งค่าคอนฟิก ER
    - ไลบรารีแอสเซท Microsoft Dynamics Lifecycle Services (LCS) สามารถใช้เป็นที่เก็บการตั้งค่าคอนฟิก ER สำหรับการแลกเปลี่ยนรุ่น
    - การแปลเป็นภาษาท้องถิ่นที่ขึ้นอยู่กับการตั้งค่าคอนฟิก ER ดั้งเดิมสามารถใช้เป็นรุ่นรองได้
    - มีแผนผังการตั้งค่าคอนฟิก ER เป็นเครื่องมือที่ช่วยควบคุมการขึ้นต่อกันของรุ่น
    - ความแตกต่างในการแปลเป็นภาษาท้องถิ่นหรือการตั้งค่าคอนฟิกส่วนที่แตกต่างจะมีการบันทึกไว้เพื่อเปิดใช้งานการอัปเกรดอัตโนมัติเป็นรุ่นใหม่ของการตั้งค่าคอนฟิก ER ดั้งเดิม
    - คุณสามารถแก้ไขข้อขัดแย้งที่จะพบได้ด้วยตนเองในระหว่างการอัปเกรดรุ่นที่มีการแปลเป็นภาษาท้องถิ่นโดยอัตโนมัติ

ER ช่วยให้คุณสามารถกำหนดโครงสร้างรูปแบบอิเล็กทรอนิกส์ แล้วอธิบายวิธีที่ควรจะเติมโครงสร้างดังกล่าวโดยใช้ข้อมูลและอัลกอริทึม คุณสามารถใช้ภาษาสูตรที่มีลักษณะคล้ายกับภาษา Excel ในการแปลงข้อมูล เพื่อให้การแมปฐานข้อมูลกับรูปแบบสามารถจัดการได้ สามารถใช้งานใหม่ได้และไม่ขึ้นกับการเปลี่ยนแปลงรูปแบบ จึงมีการใช้แนวคิดของรูปแบบข้อมูลตัวกลาง แนวคิดนี้จะแสดงรายละเอียดการดำเนินการที่มีการซ่อนไว้จากการแมปรูปแบบ และช่วยให้รูปแบบข้อมูลเดียวสามารถนำมาใช้ใหม่กับการแมปรูปแบบต่างๆ ได้

คุณสามารถใช้ ER เพื่อตั้งค่าคอนฟิกรูปแบบ สำหรับเอกสารอิเล็กทรอนิกส์ทั้งขาเข้าและขาออกที่สอดคล้องกับข้อกำหนดตามกฎหมายของประเทศและภูมิภาคต่างๆ ER ช่วยให้คุณสามารถจัดการรูปแบบเหล่านี้ในระหว่างรอบการใช้งาน ตัวอย่างเช่น คุณสามารถนำข้อกำหนดที่เป็นระเบียบข้อบังคับใหม่มาใช้ และสร้างเอกสารทางธุรกิจในรูปแบบที่กำหนด เพื่อแลกเปลี่ยนข้อมูลกับหน่วยงานของรัฐบาล ธนาคาร และฝ่ายอื่นๆ ทางอิเล็กทรอนิกส์ได้

กลไกจัดการ ER มีเป้าหมายที่ผู้ใช้ทางธุรกิจแทนนักพัฒนา เนื่องจากคุณตั้งค่าคอนฟิกรูปแบบ แทนที่รหัส กระบวนการสำหรับการสร้างและการปรับรูปแบบสำหรับเอกสารอิเล็กทรอนิกส์จึงรวดเร็วและง่ายขึ้น

ในปัจจุบัน ER รองรับรูปแบบ TEXT, XML, JSON, PDF, Microsoft Word, Microsoft Excel และเวิร์กชีต OPENXML

## <a name="capabilities"></a>ความสามารถ

กลไกจัดการ ER มีความสามารถต่อไปนี้:

- เป็นการแสดงให้เห็นเครื่องมือที่ใช้ร่วมกันแบบเดี่ยวสำหรับการรายงานทางอิเล็กทรอนิกส์ในโดเมนที่ต่างกันและแทนที่กลไกที่ต่างกันมากกว่า 20 รายการ ที่ทำรายงานทางอิเล็กทรอนิกส์บางชนิดสำหรับการเงินและการดำเนินงาน
- ทำให้รูปแบบของรายงานมีการป้องกันการใช้งานในปัจจุบัน (หรืออาจกล่าวได้ว่า รูปแบบดังกล่าวสามารถใช้ได้กับเวอร์ชันต่างๆ)
- สนับสนุนการสร้างรูปแบบที่กำหนดเองที่เป็นไปตามรูปแบบเดิม ทั้งยังประกอบด้วยความสามารถในการอัพเกรดรูปแบบที่กำหนดเองโดยอัตโนมัติ เมื่อมีการเปลี่ยนแปลงรูปแบบเดิมเนื่องจากความต้องการในการแปล / การกำหนดค่าด้วยตนเอง
- จะกลายเป็นเครื่องมือมาตรฐานหลักในการสนับสนุนความต้องการในการแปลในการรายงานทางอิเล็กทรอนิกส์ทั้งสำหรับ Microsoft และคู่ค้า Microsoft
- สนับสนุนความสามารถในการกระจายรูปแบบไปยังคู่ค้าและลูกค้าผ่านทาง Microsoft Dynamics Lifecycle Services (LCS)

## <a name="key-concepts"></a>แนวคิดหลัก

### <a name="main-data-flow"></a>โฟลว์ข้อมูลหลัก

[![โฟลว์ข้อมูลหลักของ ER](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="component"></a>ส่วนประกอบ

ER สนับสนุนชนิดของส่วนประกอบต่อไปนี้:

- แบบจำลองข้อมูล
- การแมปแบบจำลอง
- รูปแบบ
- เมตาดาต้า

สำหรับข้อมูลเพิ่มเติม โปรดดู [ส่วนประกอบการรายงานทางอิเล็กทรอนิกส์](er-overview-components.md)

### <a name="configuration"></a><a name="Configuration"></a>การจัดโครงแบบ

การตั้งค่าคอนฟิก ER คือ wrapper ของส่วนประกอบ ER เฉพาะ ส่วนประกอบอาจเป็นส่วนประกอบของแบบจำลองข้อมูล หรือส่วนประกอบรูปแบบ การตั้งค่าคอนฟิกอาจประกอบด้วยเวอร์ชันต่าง ๆ ของส่วนประกอบ ER การตั้งค่าคอนฟิกแต่ละรายการถูกทำเครื่องหมายว่าเป็นเจ้าของ โดยผู้ให้บริการการตั้งค่าคอนฟิกเฉพาะ เวอร์ชัน **ร่าง** ของส่วนประกอบการตั้งค่าคอนฟิกสามารถแก้ไขได้ เมื่อเจ้าของการตั้งค่าคอนฟิกได้รับเลือกให้เป็นผู้ให้บริการ ณ ปัจจุบัน ในการตั้งค่า ER ในแอพพลิเคชั่น

การตั้งค่าคอนฟิกแบบจำลองแต่ละรายการประกอบด้วยส่วนประกอบแบบจำลองข้อมูล การตั้งค่าคอนฟิกรูปแบบใหม่สามารถได้จากการตั้งค่าคอนฟิกแบบจำลองข้อมูลที่เฉพาะเจาะจง ในแผนภูมิการตั้งค่าคอนฟิก การตั้งค่าคอนฟิกที่ถูกสร้างขึ้นจะแสดงเป็นข้อมูลรองของการตั้งค่าคอนฟิกแบบจำลองข้อมูลเดิม

การตั้งค่าคอนฟิกรูปแบบที่ถูกสร้างขึ้น ประกอบด้วยส่วนประกอบของรูปแบบ ส่วนประกอบแบบจำลองข้อมูลของการตั้งค่าคอนฟิกแบบจำลองเดิม จะถูกแทรกโดยอัตโนมัติไปยังส่วนประกอบรูปแบบของการตั้งค่าคอนฟิกรูปแบบรองโดยเป็นแหล่งข้อมูลเริ่มต้น

การตั้งค่าคอนฟิกของ ER ถูกใช้ร่วมกันสำหรับบริษัทแอพพลิเคชั่น

### <a name="provider"></a><a name="Provider"></a>ผู้ให้บริการ

ผู้ให้บริการ ER คือ ตัวระบุฝ่ายที่ใช้เพื่อบ่งชี้ผู้เขียน (เจ้าของ) ของการตั้งค่าคอนฟิก ER แต่ละรายการ ER ช่วยให้คุณสามารถจัดการรายการของผู้ให้บริการการตั้งค่าคอนฟิก การตั้งค่าคอนฟิกรูปแบบที่ถูกนำออกใช้สำหรับเอกสารทางอิเล็กทรอนิกส์โดยเป็นส่วนหนึ่งของโซลูชันการเงินและการดำเนินงานถูกทำเครื่องหมายว่าเป็นเจ้าของโดยผู้ให้บริการการตั้งค่าคอนฟิก **Microsoft**

เมื่อต้องการเรียนรู้วิธีการลงทะเบียนผู้ให้บริการ ER ใหม่ เล่นคู่มืองาน **ER สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งาน** (เป็นส่วนหนึ่งของ **7.5.4.3 IT จัดหา/พัฒนาบริการด้านไอที/องค์ประกอบโซลูชัน (10677)** กระบวนการทางธุรกิจ)

### <a name="repository"></a><a name="Repository"></a>ที่เก็บ

ที่เก็บ ER เก็บการตั้งค่าคอนฟิก ER ประเภทของที่เก็บ ER ต่อไปนี้ได้รับการสนับสนุนแล้วในขณะนี้: 

- ไลบรารี LCS ที่ใช้ร่วมกัน
- โครงการ LCS
- ระบบไฟล์
- RCS
- ทรัพยากรของ Operations
- ที่เก็บส่วนกลาง

ที่เก็บ **ไลบรารี LCS ที่ใช้ร่วมกัน** ให้สิทธิ์การเข้าถึงรายการของการตั้งค่าคอนฟิกภายในไลบรารีสินทรัพย์ที่ใช้ร่วมกันใน Lifecycle Services (LCS) ที่เก็บ ER ชนิดนี้สามารถลงทะเบียนสำหรับผู้ให้บริการ Microsoft เท่านั้น จาก LCS Shared asset library คุณสามารถนำเข้าการตั้งค่าคอนฟิก ER รุ่นล่าสุดลงในอินสแตนซ์ปัจจุบัน

ที่เก็บข้อมูล **โครงการ LCS** มอบการเข้าถึงรายการของการตั้งค่าคอนฟิกของโครงการ LCS ที่เฉพาะเจาะจง (ไลบรารีสินทรัพย์โครงการ LCS) ที่ได้ถูกเลือกไว้เมื่อมีการลงทะเบียนที่เก็บข้อมูล ER ยินยอมให้คุณอัพโหลดการตั้งค่าคอนฟิกที่ใช้ร่วมกันจากอินสแตนซ์ปัจจุบันไปยังที่เก็บ **โครงการ LCS** โดยเฉพาะ นอกจากนี้คุณยังสามารถนำเข้าการตั้งค่าคอนฟิกจากที่เก็บ **โครงการ LCS** ลงในอินสแตนซ์ของแอปการเงินและการดำเนินงานปัจจุบันได้ด้วย

ที่เก็บ **ระบบไฟล์** ให้สิทธิ์เข้าถึงรายการของการตั้งค่าคอนฟิกที่มีอยู่เป็นไฟล์ xml ในโฟลเดอร์เฉพาะของระบบไฟล์ภายในของเครื่องที่มีการโฮสต์บริการ AOS มีการเลือกโฟลเดอร์ที่จำเป็นในขั้นตอนการลงทะเบียนที่เก็บ คุณสามารถนำเข้าการตั้งค่าคอนฟิกจากที่เก็บ **ระบบไฟล์** ลงในอินสแตนซ์ปัจจุบันได้ 

โปรดทราบว่า ที่เก็บชนิดนี้สามารถเข้าถึงได้ในสภาพแวดล้อมดังต่อไปนี้:

- สภาพแวดล้อมที่ใช้ Cloud ปรับใช้สำหรับวัตถุประสงค์การพัฒนา (ที่ประกอบด้วยรุ่นทดสอบของชุดโปรแกรมที่แนบ)
- สภาพแวดล้อมที่ปรับใช้เฉพาะที่ (ในสถานที่)

สำหรับข้อมูลเพิ่มเติม โปรดดู [นำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](./electronic-reporting-import-ger-configurations.md)

ที่เก็บข้อมูล **RCS** มอบการเข้าถึงไปยังรายการของการตั้งค่าคอนฟิกของอินสแตนซ์เฉพาะของ [บริการการตั้งค่าคอนฟิก (RCS)](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) ที่ได้ถูกเลือกไว้ในขั้นตอนการลงทะเบียนที่เก็บข้อมูล ER จะช่วยให้คุณนำเข้าการตั้งค่าคอนฟิกที่เสร็จสมบูรณ์แล้วหรือที่ใช้ร่วมกันจากอินสแตนซ์ RCS ที่เลือกลงในอินสแตนซ์ปัจจุบัน คุณจึงสามารถใช้ค่านั้นสำหรับการรายงานทางอิเล็กทรอนิกส์

สำหรับข้อมูลเพิ่มเติม โปรดดู [นำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จาก RCS](./rcs-download-configurations.md)

ที่เก็บข้อมูล **ที่เก็บข้อมูลส่วนกลาง** จะให้การเข้าถึงไปยังรายการของการตั้งค่าคอนฟิกภายในที่เก็บข้อมูลส่วนกลางใน [บริการการตั้งค่าคอนฟิก](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) ที่เก็บ ER ชนิดนี้สามารถลงทะเบียนสำหรับผู้ให้บริการ Microsoft เท่านั้น จากที่เก็บข้อมูลส่วนกลาง คุณสามารถนำเข้าการตั้งค่าคอนฟิก ER รุ่นล่าสุดลงในอินสแตนซ์ปัจจุบัน

สำหรับข้อมูลเพิ่มเติม โปรดดู [นำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จากที่เก็บข้อมูลส่วนกลางของบริการการตั้งค่าคอนฟิก](./er-download-configurations-global-repo.md)

ที่เก็บ **ทรัพยากรการดำเนินงาน** ให้การเข้าถึงไปยังรายการของการตั้งค่าคอนฟิกที่ Microsoft ในฐานะที่เป็นผู้ให้บริการการตั้งค่าคอนฟิกของ ER โดยการเผยแพร่ในเบื้องต้นในฐานะที่เป็นส่วนหนึ่งของแอพพลิเคชั่นโซลูชัน การตั้งค่าคอนฟิกเหล่านี้สามารถนำเข้าไปยังอินสแตนซ์ปัจจุบันและใช้สำหรับรายงานทางอิเล็กทรอนิกส์หรือการแสดงคู่มืองานตัวอย่าง ทั้งยังสามารถถูกใช้สำหรับการแปลเป็นภาษาท้องถิ่นและการเลือกกำหนดเพิ่มเติมได้อีกด้วย โปรดทราบว่ารุ่นล่าสุดที่มาพร้อมกับการตั้งค่าคอนฟิก Microsoft ER ต้องได้รับการนำเข้าจากไลบรารีสินทรัพย์ LCS ที่ใช้ร่วมกันโดยใช้ที่เก็บ ER ที่สอดคล้อง

ที่เก็บข้อมูล **โครงการ LCS** **ระบบไฟล์** และ **Regulatory Configuration Services (RCS)** ที่จำเป็น สามารถลงทะเบียนแยกกันสำหรับผู้ให้บริการการตั้งค่าคอนฟิกของอินสแตนซ์ปัจจุบัน ที่เก็บแต่ละที่สามารถใช้ได้เฉพาะกับผู้ให้บริการการตั้งค่าคอนฟิกเฉพาะ

## <a name="supported-scenarios"></a>สถานการณ์จำลองที่ได้รับการสนับสนุน

### <a name="building-a-data-model"></a>การสร้างแบบจำลองของข้อมูล

ER มอบผู้ออกแบบแบบจำลองที่คุณสามารถใช้ในการสร้างแบบจำลองข้อมูลสำหรับโดเมนธุรกิจหนึ่งๆ เอนทิตีทางธุรกิจเฉพาะโดเมนทั้งหมดและความสัมพันธ์ระหว่างกัน สามารถถูกนำเสนอในแบบจำลองข้อมูลให้เป็นโครงสร้างตามลำดับชั้นได้ 

เมื่อต้องการทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่นคู่มืองาน **แบบจำลองข้อมูลเฉพาะโดเมนการออกแบบ ER** (ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 ส่วนประกอบกระบวนได้รับ/พัฒนาการบริการ/โซลูชันด้านไอที (10677)** )

### <a name="translating-data-model-content"></a>การแปลเนื้อหาแบบจำลองข้อมูล

เนื้อหารูปแบบข้อมูล (สัญลักษณ์และคำอธิบาย) สามารถแปลเป็นภาษาอื่นๆ ที่แอพพลิเคชั่นสนับสนุน คุณอาจต้องการแปลเนื้อหาแบบจำลองข้อมูลสำหรับเหตุผลต่อไปนี้:

- ในขณะออกแบบ เพื่อทำให้เนื้อหาเข้าใจได้ง่ายมากขึ้นสำหรับผู้ออกแบบรูปแบบที่พูดภาษาอื่น และผู้ที่จะใช้แบบจำลองข้อมูลสำหรับการแมปข้อมูลของส่วนประกอบรูปแบบ
- ในขณะเวลารัน เพื่อทำให้เนื้อหาง่ายต่อผู้ใช้งานมากขึ้นโดยการนำเสนอพร้อมต์และความช่วยเหลือสำหรับพารามิเตอร์ในเวลาดำเนินงาน และข้อความการตรวจสอบที่มีการตั้งค่าคอนฟิก (ข้อผิดพลาดและคำเตือน) ในภาษาที่ผู้ใช้ที่ลงชื่อเข้าใช้ในขณะนี้ต้องการ

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>การตั้งค่าคอนฟิกการแมปแบบจำลองข้อมูลสำหรับเอกสารขาออก

ER แสดงโปรแกรมออกแบบการแมปแบบจำลองที่ช่วยให้ผู้ใช้แมปแบบจำลองข้อมูลที่ออกแบบไปยังแหล่งข้อมูลเฉพาะของแอพพลิเคชั่น โดยขึ้นอยู่กับการแมป ข้อมูลจะสามารถถูกนำเข้าขณะเวลารันจากแหล่งข้อมูลที่เลือกไปยังแบบจำลองข้อมูล จากนั้น จะมีการใช้รูปแบบข้อมูลเป็นแหล่งข้อมูลนามธรรมของรูปแบบ ER ที่สร้างเอกสารอิเล็กทรอนิกส์ขาออก 

เมื่อต้องการทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่น **ER กำหนดการแมปแบบจำลอง และเลือกแหล่งข้อมูล** และคู่มืองาน **ER แมปแบบจำลองข้อมูลไปยังแหล่งข้อมูลที่เลือก** (ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 ได้รับ/พัฒนาส่วนประกอบบริการ/โซลูชันทางด้าน IT (10677)**)

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>การตั้งค่าคอนฟิกการแมปแบบจำลองข้อมูลสำหรับเอกสารขาเข้า

ER แสดงโปรแกรมออกแบบการแมปแบบจำลอง ที่ช่วยให้ผู้ใช้สามารถแมปแบบจำลองข้อมูลที่พวกเขาออกแบบไปยังเป้าหมายเฉพาะ ตัวอย่างเช่น แบบจำลองข้อมูลสามารถถูกแมปกับส่วนประกอบข้อมูลที่สามารถอัปเดตได้ของ (ตาราง เอนทิตีข้อมูล และมุมมอง) โดยขึ้นอยู่กับการแมป ข้อมูลจะมีการอัปเดตขณะดำเนินการ โดยการใช้ข้อมูลจากแบบจำลองข้อมูล ในฐานะที่เป็นการจัดเก็บนามธรรมของรูปแบบ ER แบบจำลองข้อมูลจะถูกเติมด้วยข้อมูลที่นำเข้าจากเอกสารอิเล็กทรอนิกส์ขาเข้า 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>การจัดเก็บส่วนประกอบแบบจำลองที่ได้ออกแบบไว้ให้เป็นการตั้งค่าคอนฟิกแบบจำลอง

ER สามารถจัดเก็บแบบจำลองข้อมูลที่ออกแบบไว้รวมกับการแมปข้อมูลที่เชื่อมโยงเป็นการตั้งค่าคอนฟิกแบบจำลองของอินสแตนซ์ปัจจุบัน ภาพประกอบต่อไปนี้แสดงตัวอย่างของชนิดของการตั้งค่าคอนฟิกแบบจำลองข้อมูล (การตั้งค่าคอนฟิกแบบจำลองการชำระเงิน)

เมื่อต้องการทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่นคู่มืองาน **ER แมปแบบจำลองข้อมูลไปยังแหล่งข้อมูลที่เลือกไว้** (ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 ส่วนประกอบกระบวนได้รับ/พัฒนาการบริการ/โซลูชันด้านไอที (10677)** )

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>การสร้างรูปแบบที่ใช้แบบจำลองข้อมูลเป็นพื้นฐาน

ER สนับสนุนผู้ออกแบบรูปแบบที่คุณสามารถใช้ในการสร้างรูปแบบของเอกสารอิเล็กทรอนิกส์สำหรับโดเมนทางธุรกิจที่เลือก โดยการเลือกส่วนประกอบแบบจำลองให้เป็นฐาน โปรแกรมออกแบบรูปแบบ ER เดียวกันทำให้คุณสามารถแมปรูปแบบที่คุณสร้างไปยังการแมปแบบจำลองข้อมูลของโดเมนเป็นแหล่งข้อมูลได้ 

เมื่อต้องการทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่นคู่มืองาน **รูปแบบเฉพาะโดเมนการออกแบบ ER** (ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 ส่วนประกอบกระบวนได้รับ/พัฒนาการบริการ/โซลูชันด้านไอที (10677)** )

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>การสร้างการตั้งค่าคอนฟิกเพื่อสร้างเอกสารอิเล็กทรอนิกส์ในรูปแบบของแผ่นงาน OPENXML

ตัวออกแบบรูปแบบ ER สามารถถูกใช้ในการสร้างเอกสารอิเล็กทรอนิกส์ในรูปแบบของแผ่นงาน OPENXML 

เมื่อต้องการทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่นคู่มืองาน **ER สร้างการตั้งค่าคอนฟิกสำหรับรายงานในรูปแบบ OPENXML** (ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 ส่วนประกอบกระบวนได้รับ/พัฒนาการบริการ/โซลูชันด้านไอที (10677)** ) ในฐานะที่เป็นส่วนหนึ่งของขั้นตอนคู่มืองานสำหรับการนำเข้าเทมเพลต ใช้ [เทมเพลตของรายงานการชำระเงิน (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx) ไฟล์ Excel เป็นเทมเพลต

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>การสร้างการตั้งค่าคอนฟิกเพื่อสร้างเอกสารอิเล็กทรอนิกส์ในรูปแบบของเอกสาร Word

ตัวออกแบบรูปแบบ ER สามารถถูกใช้ในการสร้างเอกสารอิเล็กทรอนิกส์ในรูปแบบของเอกสาร Word ภาพประกอบต่อไปนี้แสดงตัวอย่างของรูปแบบชนิดนี้ สังเกตว่า รูปแบบนี้ใช้การตั้งค่าคอนฟิก ER ที่มีอยู่อีกครั้ง ซึ่งแต่เดิมถูกออกแบบเพื่อสร้างเอาท์พุทรายงานในรูปแบบ OPENXML

เมื่อต้องการทำความคุ้นเคยกับรายละเอียดของสถานการณ์จำลองนี้ เล่นการออกแบบ ER การตั้งค่าคอนฟิกสำหรับการสร้างรายงานในคู่มืองานในรูปแบบ Microsoft WORD (ส่วนหนึ่งของ 7.5.4.3 จัดหา/พัฒนาบริการด้านไอที/องค์ประกอบโซลูชัน (10677) กระบวนการทางธุรกิจ) ในฐานะที่เป็นส่วนหนึ่งของขั้นตอนคู่มืองานสำหรับการนำเข้าเทมเพลต ใช้ไฟล์ Word ต่อไปนี้เป็นเทมเพลตสำหรับรูปแบบ ER:

- [เทมเพลตของรายงานการชำระเงิน (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [เทมเพลตที่กำหนดขอบเขตของรายงานการชำระเงิน (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>การสร้างการตั้งค่าคอนฟิกเพื่อนำเข้าข้อมูลจากเอกสารอิเล็กทรอนิกส์ขาเข้า

ตัวออกแบบรูปแบบ ER สามารถถูกใช้เพื่ออธิบายเอกสารอิเล็กทรอนิกส์ที่วางแผนไว้ สำหรับการนำเข้าข้อมูลในรูปแบบ XML หรือข้อความ มีการใช้รูปแบบถูกออกแบบมาเพื่อแยกวิเคราะห์เอกสารขาเข้า ตัวออกแบบการแมปรูปแบบ ER สามารถถูกใช้เพื่อกำหนดการผูกข้อมูลองค์ประกอบของรูปแบบที่ถูกออกแบบมาให้กับแบบจำลองข้อมูล 

เมื่อต้องการทำความคุ้นเคยกับรายละเอียดของสถานการณ์นี้ เล่นสร้างการตั้งค่าคอนฟิก ER ที่จำเป็นในการนำเข้าข้อมูลจากไฟล์ภายนอก (ส่วนหนึ่งของ 7.5.4.3 จัดหา/พัฒนา บริการด้านไอที/องค์ประกอบโซลูชัน (10677) กระบวนการทางธุรกิจ) ใช้ไฟล์ต่อไปนี้เพื่อเล่นคู่มือนี้:

- [การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [การตั้งค่าคอนฟิกรูปแบบ ER (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [ตัวอย่างของเอกสารขาเข้าในรูปแบบ XML (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [ตัวอย่างของสมุดงานในการจัดการข้อมูลของเอกสารขาเข้า (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>การจัดเก็บส่วนประกอบรูปแบบที่ได้ออกแบบไว้ในการตั้งค่าคอนฟิกรูปแบบ

ER สามารถจัดเก็บรูปแบบที่ออกแบบไว้รวมกับการแมปข้อมูลที่มีการตั้งค่าคอนฟิกให้เป็นการตั้งค่าคอนฟิกรูปแบบของอินสแตนซ์ปัจจุบัน ภาพประกอบก่อนหน้านี้แสดงตัวอย่างของการตั้งค่าคอนฟิกรูปแบบชนิดนี้ (**BACS (สหราชอาณาจักร)** ซึ่งเป็นข้อมูลรองของการตั้งค่าคอนฟิก **รูปแบบการชำระเงิน**) เมื่อต้องการทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่นคู่มืองาน **รูปแบบเฉพาะโดเมนการออกแบบ ER** (ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 ส่วนประกอบกระบวนได้รับ/พัฒนาการบริการ/โซลูชันด้านไอที (10677)** )

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>การตั้งค่าคอนฟิกทางการเงินเพื่อเริ่มต้นการใช้รูปแบบที่มีการสร้างไว้ภายใน

แอพพลิเคชั่นสามารถตั้งค่าคอนฟิกเพื่อเริ่มต้นการใช้รูปแบบที่สร้างไว้เพื่อสร้างรายงานทางอิเล็กทรอนิกส์ การอ้างอิงถึงการตั้งค่าคอนฟิกรูปแบบที่สร้างไว้ควรจะถูกกำหนดในการตั้งค่าของโดเมนเฉพาะ ตัวอย่างเช่น เมื่อต้องการเริ่มต้นการใช้การตั้งค่าคอนฟิกรูปแบบ ER สำหรับการชำระเงินของผู้จัดจำหน่ายทางอิเล็กทรอนิกส์ในรูปแบบ BACS การตั้งค่าคอนฟิกรูปแบบควรถูกอ้างอิงในวิธีการชำระเงินที่ระบุ

เพื่อทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่นคู่มืองาน **ER ใช้รูปแบบในการสร้างเอกสารทางอิเล็กทรอนิกส์สำหรับการชำระเงิน** (ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 ได้รับ/พัฒนาส่วนประกอบบริการ/โซลูชันทางด้าน IT (10677)** )

## <a name="handling-er-components"></a>การจัดการส่วนประกอบ ER

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>การเผยแพร่องค์ประกอบ ER ใน LCS เพื่อนำเสนอภายนอก (การแปล)

เจ้าของส่วนประกอบ (แบบจำลองหรือรูปแบบ) ที่สร้างขึ้นสามารถใช้ ER สำหรับการเผยแพร่เวอร์ชันที่เสร็จสมบูรณ์ของส่วนประกอบไปยัง LCS ต้องมีการระบุที่เก็บของชนิด **โครงการ LCS** สำหรับผู้ให้บริการการตั้งค่าคอนฟิก ER ปัจจุบัน เมื่อสถานะของเวอร์ชันที่เสร็จสมบูรณ์ของส่วนประกอบถูกเปลี่ยนแปลงจาก **เสร็จสมบูรณ์แล้ว** ไปเป็น **ใช้ร่วมกัน** เวอร์ชันนั้นได้รับการเผยแพร่ใน LCS เมื่อส่วนประกอบได้รับการเผยแพร่ไปยัง LCS เจ้าของส่วนประกอบนั้นจะกลายเป็นผู้ให้บริการเพื่อสนับสนุนองค์ประกอบนั้น ตัวอย่างเช่น ถ้าส่วนประกอบรูปแบบนี้มีวัตถุประสงค์เพื่อสร้างเอกสารทางอิเล็กทรอนิกส์ที่จำเป็นตามกฎหมาย (ตัวอย่างเช่น ให้สอดคล้องกับสถานการณ์จำลองการแปล) บริการนี้สันนิษฐานให้รักษารูปแบบนี้ที่สอดคล้องกับการเปลี่ยนแปลงทางกฎหมาย และผู้ให้บริการจะออกใช้ส่วนประกอบเวอร์ชันใหม่เมื่อใดก็ตามที่มีความต้องการทางกฎหมายใหม่ เมื่อต้องการทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่นคู่มืองาน **ER อัพโหลดการตั้งค่าคอนฟิกลงใน Lifecycle Services**(ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 ส่วนประกอบกระบวนได้รับ/พัฒนาการบริการ/โซลูชันด้านไอที (10677)** )

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>การนำเข้าส่วนประกอบ ER จาก LCS เพื่อใช้เป็นการภายใน

ER ช่วยให้คุณสามารถนำเข้าส่วนประกอบ ER จาก LCS ไปยังอินสแตนซ์ปัจจุบันได้ ต้องมีการระบุที่เก็บของชนิด **โครงการ LCS** เมื่อส่วนประกอบของ ER ได้ถูกนำเข้าจาก LCS ไปยังอินสแตนซ์ปัจจุบัน เจ้าของอินสแตนซ์จะกลายเป็นผู้ใช้บริการที่มาจากเจ้าของ (ผู้เขียน) เอกสารที่มีการนำเข้า ตัวอย่างเช่น ถ้าส่วนประกอบรูปแบบนี้มีวัตถุประสงค์เพื่อสร้างเอกสารอิเล็กทรอนิกส์เฉพาะจากแอพพลิเคชั่นในรูปแบบเฉพาะของบางประเทศ/ภูมิภาค (สถานการณ์การแปล) จะถือว่าผู้ใช้บริการจะสามารถได้รับการอัปเดตใดๆ ที่กระทำกับรูปแบบนั้น เพื่อให้สอดคล้องกับความต้องการทางกฎหมาย เมื่อต้องการทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่นคู่มืองาน **ER นำเข้าการตั้งค่าคอนฟิกจาก Lifecycle Services** (ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 ส่วนประกอบกระบวนได้รับ/พัฒนาการบริการ/โซลูชันด้านไอที (10677)** )

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>การสร้างรูปแบบที่เลือกอีกรูปแบบหนึ่งให้เป็นพื้นฐาน (การเลือกกำหนด)

ER ทำให้คุณสามารถสร้าง (สืบทอดมา) ส่วนประกอบใหม่จากส่วนประกอบ (พื้นฐาน) รุ่นปัจจุบันที่ถูกนำเข้าจาก LCS ตัวอย่างเช่น ผู้ใช้ต้องการสืบทอดรูปแบบใหม่เพื่อดำเนินการข้อกำหนดพิเศษบางอย่างสำหรับเอกสารอิเล็กทรอนิกส์ (เช่น ฟิลด์เพิ่มเติมหรือคำอธิบายที่ครอบคลุม) เพื่อสนับสนุนสถานการณ์จำลองที่กำหนดเอง เพื่อทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่นคู่มืองาน **ER อัพเกรดรูปแบบโดยการใช้เวอร์ชันพื้นฐานใหม่** (ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 ได้รับ/พัฒนาส่วนประกอบบริการ/โซลูชันทางด้าน IT (10677)** )

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>การอัพเกรดรูปแบบที่เลือกเวอร์ชันใหม่ของรูปแบบพื้นฐาน (ปรับใช้ซ้ำ)

ER ทำให้คุณสามารถนำการเปลี่ยนแปลงมาใช้โดยอัตโนมัติ ของเวอร์ชันล่าสุดของส่วนประกอบพื้นฐานในเวอร์ชันแบบร่างปัจจุบันของส่วนประกอบที่ได้รับมา กระบวนการนี้เรียกว่า *การปรับใช้ซ้ำ* ตัวอย่างเช่น การเปลี่ยนแปลงข้อบังคับใหม่ทีได้นำไปใช้ในเวอร์ชันล่าสุดของรูปแบบที่มีการนำเข้าจาก LCS สามารถรวมโดยอัตโนมัติในเวอร์ชันที่กำหนดเองของเอกสารทางอิเล็กทรอนิกส์รูปแบบนี้ การเปลี่ยนแปลงใด ๆ ที่ไม่สามารถรวมกันโดยอัตโนมัติได้จะถูกพิจารณาว่าเป็นข้อขัดแย้ง ความขัดแย้งเหล่านี้จะแสดงสำหรับการแก้ปัญหาด้วยตนเองในเครื่องมือผู้ออกแบบสำหรับส่วนประกอบที่เหมาะสม เพื่อทำความคุ้นเคยกับสถานการณ์นี้ในรายละเอียด เล่นคู่มืองาน **ER อัพเกรดรูปแบบโดยการใช้เวอร์ชันพื้นฐานใหม่ของรูปแบบนั้น** (ส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.5.3 จัดหา/พัฒนาส่วนประกอบของบริการแ/โซลูชันด้านไอทีที่มีการเปลี่ยนแปลง (10683)**)

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>รายการของการตั้งค่าคอนฟิก ER ที่นำออกใช้ใน Finance

รายการของการตั้งค่าคอนฟิก ER ของ Finance มีการอัปเดตอย่างต่อเนื่อง เปิด [ที่เก็บส่วนกลาง](er-download-configurations-global-repo.md) เพื่อตรวจทานรายการการตั้งค่าคอนฟิก ER ที่ได้รับการสนับสนุนในปัจจุบัน บนแท็บด่วน **รายละเอียดการยกเลิก** คุณสามารถทบทวนข้อมูลเกี่ยวกับการตั้งค่าคอนฟิกที่ถูกยกเลิก หรือไม่ได้เก็บรักษาไว้อีกต่อไป 

![เนื้อหาของที่เก็บส่วนกลางในหน้าที่เก็บการตั้งค่าคอนฟิก](./media/er-overview-03.gif)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ส่วนประกอบการรายงานทางอิเล็กทรอนิกส์](er-overview-components.md)
- [สร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-configuration.md)
- [จัดการวงจรชีวิตการตั้งค่าคอนฟิกรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

