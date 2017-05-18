---
title: "ความต้องการของระบบ"
description: "หัวข้อนี้แสดงความต้องการของระบบสำหรับรุ่นล่าสุดของ Microsoft Dynamics 365 for Operations"
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 86053196a3aad6b7b5d7830860e1af347dd969d8
ms.contentlocale: th-th
ms.lasthandoff: 04/25/2017


---

# <a name="system-requirements"></a>ความต้องการของระบบ

[!include[banner](../includes/banner.md)]


หัวข้อนี้แสดงความต้องการของระบบสำหรับรุ่นล่าสุดของ Microsoft Dynamics 365 for Operations

<a name="supported-web-browsers"></a>เว็บเบราเซอร์ที่สนับสนุน
----------------------

โปรแกรมประยุกต์บนเว็บ Microsoft Dynamics 365 for Operations สามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ที่ทำงานบนระบบปฏิบัติการที่ระบุ:

-   Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10
-   Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7
-   Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus แท็บเล็ต 10
-   Apple Safari (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) หรือ 10.12 (Sierra) หรือ Apple iPad

เมื่อต้องการค้นหารุ่นล่าสุดของแต่ละเว็บเบราเซอร์ ไปที่เว็บไซต์ของผู้ผลิตซอฟต์แวร์ **หมายเหตุ:**

-   เมื่อต้องการจับภาพรูปที่สร้างขึ้นจากตัวบันทึกงาน และรวมค่าเหล่านั้นไว้ในเอกสาร Microsoft Word คุณต้องติดตั้งส่วนขยาย Chrome ไว้ <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   ตัวแก้ไขเวิร์กโฟลว์จะเริ่มต้นการใช้งานเป็นแอพลิเคชัน ClickOnce เฉพาะ Microsoft Edge และ Internet Explorer (ในรุ่นที่สนับสนุนของ Microsoft Windows) สนับสนุนแอพลิเคชัน ClickOnce แอพลิเคชัน ClickOnce โปรแกรมแก้ไขลำดับงานต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต
-   โปรแกรมออกแบบรายงานสำหรับการรายงานทางการเงินจะถูกเริ่มต้นโดยเป็นแอพลิเคชัน ClickOnce ต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต ถ้าคุณใช้ Chrome คุณต้องติดตั้งส่วนขยาย ClickOnce เพื่อดาวน์โหลดไคลเอ็นต์โปรแกรมออกแบบรายงาน ถ้าคุณกำลังใช้ Chrome พร้อมกับโหมด incognito ให้ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานส่วนขยาย ClickOnce สำหรับโหมด incognito แล้ว
-   เมื่อต้องการแสดงตัวอย่างไฟล์ PDF เราขอแนะนำให้คุณใช้เบราว์เซอร์ที่ทันสมัย เช่น Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10 หรือ Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บนแท็บเล็ต Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus 10


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>เบราเซอร์ที่สนับสนุนสำหรับ Retail Cloud POS

โปรแกรมประยุกต์บนเว็บ Dynamics 365 for Operations สามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ที่ทำงานบนระบบปฏิบัติการที่ระบุ:

-   Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10
-   Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7
-   Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10, Windows 8.1 หรือ Windows 7

## <a name="network-requirements"></a>ข้อกำหนดของเครือข่าย
-   Dynamics 365 for Operations ได้รับการออกแบบมาสำหรับเครือข่ายที่มีเวลาแฝงน้อยกว่า 150 มิลลิวินาที (ms) นี่คือเวลาแฝงจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Microsoft Azure ที่โฮสต์ Dynamics 365 for Operations เราขอแนะนำให้คุณทดสอบเวลาแฝงบนเครือข่ายที่ <http://www.azurespeed.com>
-   ข้อกำหนดของแบนด์วิธสำหรับ Dynamics 365 for Operations ขึ้นอยู่กับสถานการณ์ของคุณ สถานการณ์ทั่วไปส่วนใหญ่จำเป็นต้องมีแบนด์วิดท์ที่มากกว่า 50 กิโลไบต์ต่อวินาที (KBps) อย่างไรก็ตาม สำหรับสถานการณ์ที่มีข้อกำหนดของน้ำหนักบรรทุกที่สร้างรายได้ที่สูง เช่น พื้นที่ทำงานหรือสถานการณ์ที่เกี่ยวข้องกับการกำหนดเองที่ครอบคลุม ระบบแนะนำให้ใช้แบนด์วิดท์ที่มากขึ้น

โดยทั่วไป Dynamics 365 for Operations จะเหมาะสำหรับอินเทอร์เน็ต จำนวนของการเดินทางไปกลับจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Azure มีขนาดเล็กมาก และน้ำหนักบรรทุกที่สร้างรายได้ทั้งหมดจะถูกบีบอัด **คำเตือน:** อย่าคำนวณข้อกำหนดของแบนด์วิดท์จากตำแหน่งที่ตั้งของไคลเอนต์ โดยการคูณจำนวนผู้ใช้กับข้อกำหนดของแบนด์วิดท์ต่ำสุด การใช้งานที่เกิดขึ้นพร้อมกันของตำแหน่งที่ตั้งที่กำหนดเป็นสิ่งที่คำนวณได้ยาก สำหรับลูกค้าที่มีความกังวลเกี่ยวกับข้อกำหนดของแบนด์วิดท์ ให้ใช้ Dynamics 365 for Operations เวอร์ชันตัวอย่าง

## <a name="net-framework-requirements"></a>ข้อกำหนดของ .NET Framework
Dynamics 365 for Operations ต้องมี .NET Framework รุ่น 4.6.2 สำหรับแอพลิเคชันแบบคลิกครั้งเดียวทั้งหมด เช่น ตัวแทนเส้นทางของเอกสาร สำหรับคำแนะนำในการติดตั้ง ให้ดูที่ [การติดตั้ง .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx)

## <a name="supported-microsoft-office-applications"></a>แอพลิเคชัน Microsoft Office ที่ได้รับการสนับสนุน
-   เมื่อต้องการเรียกใช้ Add-in ของ Microsoft Excel และ Word คุณจะต้องตั้งค่า Microsoft Office 2016 สำหรับ Windows หรือ Mac ไว้ สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับข้อกำหนดเวอร์ชัน ให้ดูที่ [การแก้ไขปัญหาการรวม Office](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting)
-   เมื่อต้องการดูเอกสารที่สร้างขึ้นโดยฟังก์ชันส่งออกไปที่ Excel หรือส่งออกไปที่ Word คุณต้องติดตั้ง Microsoft Office 2007 หรือรุ่นที่ใหม่กว่าไว้

## <a name="retail-modern-pos-requirements"></a>ข้อกำหนดของ Modern POS ของการขายปลีก
### <a name="supported-operating-systems"></a>ระบบปฏิบัติการที่ได้รับการสนับสนุน

-   Modern POS ของการขายปลีก คือแอพลิเคชันแบบ 32 บิต แต่จะทำงานทั้งบนโครงสร้าง x86 และ x64
-   Modern POS ของการขายปลีก ได้รับการสนับสนุนเฉพาะในรุ่น Windows 10 Pro, Enterprise และ Enterprise Long Term Servicing Branch (LTSB)

### <a name="minimum-system-requirements"></a>ข้อกำหนดของระบบขั้นต่ำ

-   ความละเอียดต่ำสุดที่สนับสนุนคือ 1280 × 1024
-   คอมพิวเตอร์ที่มีการเรียกใช้ Modern POS ของการขายปลีก ต้องเป็นไปตามข้อกำหนดเหล่านี้:
    -   อย่างน้อยที่สุด ต้องมีตัวประมวลผลสองหลักที่รันที่ไม่น้อยกว่า 2 กิกะเฮิร์ตซ์ (GHz)
    -   ต้องมี RAM อย่างน้อยที่สุด 3 กิกะไบต์ (GB)
    -   ต้องมีการเข้าถึงอินเทอร์เน็ต

## <a name="retail-hardware-station-requirements"></a>ข้อกำหนดของ Retail hardware station
### <a name="supported-operating-systems"></a>ระบบปฏิบัติการที่ได้รับการสนับสนุน

-   Retail hardware station คือแอพลิเคชันแบบ 32 บิต แต่จะทำงานทั้งบนโครงสร้าง x86 และ x64
-   Retail hardware station ได้รับการสนับสนุนบนระบบปฏิบัติการต่อไปนี้:
    -   รุ่น Windows 7 Professional, Enterprise และ Ultimate **หมายเหตุ:** Windows 7 ได้รับการสนับสนุนเฉพาะเมื่อมีการติดตั้ง Internet Explorer 11 บนระบบด้วยตนเอง
    -   รุ่น Windows 8.1 Update 1 Professional, Enterprise และ Embedded
    -   รุ่น Windows 10 Pro, Enterprise และ Enterprise LTSB

### <a name="minimum-system-requirements"></a>ข้อกำหนดของระบบขั้นต่ำ

คอมพิวเตอร์ต้องเป็นไปตามข้อกำหนดของระบบทั้งหมดสำหรับการติดตั้งและการใช้รายการต่อไปนี้:

-   บริการข้อมูลทางอินเทอร์เน็ต (IIS)
-   ฮาร์ดแวร์ของบุคคลที่สาม

## <a name="retail-store-scale-unit-requirements"></a>ข้อกำหนดของ Retail Store Scale Unit
### <a name="supported-operating-systems"></a>ระบบปฏิบัติการที่ได้รับการสนับสนุน

-   Retail Store Scale Unit คือแอพลิเคชันแบบ 32 บิต แต่จะทำงานทั้งบนโครงสร้าง x86 และ x64
-   Retail Store Scale Unit ได้รับการสนับสนุนบนระบบปฏิบัติการต่อไปนี้:
    -   รุ่น Windows 7 Professional, Enterprise และ Ultimate
    -   รุ่น Windows 8.1 Update 1 Professional, Enterprise และ Embedded
    -   รุ่น Windows 10 Pro, Enterprise และ Enterprise LTSB

### <a name="minimum-system-requirements"></a>ข้อกำหนดของระบบขั้นต่ำ

-   RAM ขนาด 4 GB
-   ความเร็วของ CPU สูงสุด 1.6 GHz ต่อแกน (ต้องมีอย่างต่ำสองแกน)
-   เนื้อที่ว่างอย่างน้อย 10 กิกะไบต์ (ฐานข้อมูลช่องทางอาจต้องการเนื้อที่ว่างจำนวนมาก)

### <a name="recommended-system-requirements"></a>ข้อกำหนดของระบบที่แนะนำ

-   RAM ขนาด 6 GB
-   ความเร็วของ CPU สูงสุด 2.4 GHz i7 (หรือเทียบเท่ากับ) ต่อแกน (แนะนำให้มีสี่แกน)
-   เนื้อที่ว่างอย่างน้อย 10 กิกะไบต์ (ฐานข้อมูลช่องทางอาจต้องการเนื้อที่ว่างจำนวนมาก)

## <a name="requirements-for-development-on-local-vms"></a>ข้อกำหนดสำหรับการพัฒนาบน VM เฉพาะที่
สำหรับข้อมูลเกี่ยวกับข้อกำหนดสำหรับการพัฒนาเครื่องเสมือนจริงเฉพาะที่ (VM) ให้ดูที่ [VM ที่เรียกใช้แบบ On-premises](../dev-tools/access-instances.md)

<a name="see-also"></a>ดูเพิ่มเติมที่
--------

[รับสำเนาการประเมินของ Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)




