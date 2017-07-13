---
title: "ความต้องการของระบบ"
description: "หัวข้อนี้แสดงความต้องการของระบบสำหรับรุ่นล่าสุดของ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition"
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
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
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 724ee7ec29f8a9c4e8cc0b244193cd6c83c37f03
ms.contentlocale: th-th
ms.lasthandoff: 06/13/2017


---

# <a name="system-requirements"></a>ความต้องการของระบบ

[!include[banner](../includes/banner.md)]


หัวข้อนี้แสดงความต้องการของระบบสำหรับรุ่นล่าสุดของ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition

<a name="supported-web-browsers"></a>เว็บเบราเซอร์ที่สนับสนุน
----------------------

โปรแกรมประยุกต์บนเว็บสามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ที่ทำงานบนระบบปฏิบัติการที่ระบุ:

-   Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10
-   Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7
-   Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus แท็บเล็ต 10
-   Apple Safari (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) หรือ 10.12 (Sierra) หรือ Apple iPad

เมื่อต้องการค้นหารุ่นล่าสุดของแต่ละเว็บเบราเซอร์ ไปที่เว็บไซต์ของผู้ผลิตซอฟต์แวร์ 

**หมายเหตุ:**

-   จะต้องติดตั้งส่วนขยายของ Chrome เวอร์ชันก่อนวางจำหน่ายเพื่ออนุญาตให้รวบรวมภาพหน้าจอโดยตัวบันทึกงานและรวมเข้าไปใน Microsoft Word documents โดยอัตโนมัติ <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
-   ตัวแก้ไขเวิร์กโฟลว์จะเริ่มต้นการใช้งานเป็นแอพลิเคชัน ClickOnce เฉพาะ Microsoft Edge และ Internet Explorer (ในรุ่นที่สนับสนุนของ Microsoft Windows) สนับสนุนแอพลิเคชัน ClickOnce แอพลิเคชัน ClickOnce โปรแกรมแก้ไขลำดับงานต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต
-   โปรแกรมออกแบบรายงานสำหรับการรายงานทางการเงินจะถูกเริ่มต้นโดยเป็นแอพลิเคชัน ClickOnce ต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต ถ้าคุณใช้ Chrome คุณต้องติดตั้งส่วนขยาย ClickOnce เพื่อที่จะดาวน์โหลดไคลเอ็นต์โปรแกรมออกแบบรายงาน ถ้าคุณกำลังใช้ Chrome พร้อมกับโหมด incognito ให้ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานส่วนขยาย ClickOnce สำหรับโหมด incognito แล้ว
-   เมื่อต้องการแสดงตัวอย่างไฟล์ PDF เราขอแนะนำให้คุณใช้เบราว์เซอร์ เช่น Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10 หรือ Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บนแท็บเล็ต Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus 10


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>เบราเซอร์ที่สนับสนุนสำหรับ Retail Cloud POS

Retail Cloud POS สามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ที่ทำงานบนระบบปฏิบัติการที่ระบุ:

-   Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10
-   Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7
-   Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10, Windows 8.1 หรือ Windows 7

## <a name="network-requirements"></a>ข้อกำหนดของเครือข่าย
-   Dynamics 365 for Finance and Operations, Enterprise edition ได้รับการออกแบบมาสำหรับเครือข่ายที่มีเวลาแฝง 250-300 มิลลิวินาที (ms) หรือน้อยกว่า นี่คือเวลาแฝงจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Microsoft Azure ที่โฮสต์ Finance and Operations เราขอแนะนำให้คุณทดสอบเวลาแฝงบนเครือข่ายที่ <http://www.azurespeed.com>
-   ข้อกำหนดของแบนด์วิธที่ขึ้นอยู่กับสถานการณ์ของคุณ สถานการณ์ทั่วไปส่วนใหญ่จำเป็นต้องมีแบนด์วิดท์ที่มากกว่า 50 กิโลไบต์ต่อวินาที (KBps) อย่างไรก็ตาม สำหรับสถานการณ์ที่มีข้อกำหนดของน้ำหนักบรรทุกที่สร้างรายได้ที่สูง เช่น พื้นที่ทำงานหรือสถานการณ์ที่เกี่ยวข้องกับการกำหนดเองที่ครอบคลุม ระบบแนะนำให้ใช้แบนด์วิดท์ที่มากขึ้น

โดยทั่วไป Finance and Operations จะเหมาะสำหรับอินเทอร์เน็ต จำนวนของการเดินทางไปกลับจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Azure มีขนาดเล็กมาก และน้ำหนักบรรทุกที่สร้างรายได้ทั้งหมดจะถูกบีบอัด 

**คำเตือน:** อย่าคำนวณข้อกำหนดของแบนด์วิดท์จากตำแหน่งที่ตั้งของไคลเอนต์ โดยการคูณจำนวนผู้ใช้กับข้อกำหนดของแบนด์วิดท์ต่ำสุด การใช้งานที่เกิดขึ้นพร้อมกันของตำแหน่งที่ตั้งที่กำหนดเป็นสิ่งที่คำนวณได้ยากมาก สำหรับลูกค้าที่มีความกังวลเกี่ยวกับข้อกำหนดของแบนด์วิดท์ ให้ใช้ Finance and Operations เวอร์ชันตัวอย่าง

## <a name="net-framework-requirements"></a>ข้อกำหนดของ .NET Framework
จำเป็นต้องมี .NET Framework รุ่น 4.6.2 สำหรับแอพลิเคชัน ClickOnce ทั้งหมด เช่น ตัวแทนเส้นทางของเอกสาร สำหรับคำแนะนำในการติดตั้ง ให้ดูที่ [การติดตั้ง .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx)

## <a name="supported-microsoft-office-applications"></a>แอพลิเคชัน Microsoft Office ที่ได้รับการสนับสนุน
-   เมื่อต้องการเรียกใช้ Add-in ของ Microsoft Excel และ Word คุณจะต้องตั้งค่า Microsoft Office 2016 สำหรับ Windows หรือ Mac ไว้ สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับข้อกำหนดเวอร์ชัน ให้ดูที่ [การแก้ไขปัญหาการรวม Office](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting)
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

## <a name="connector-requirements"></a>ข้อกำหนดของตัวเชื่อมต่อ
### <a name="supported-operating-systems"></a>ระบบปฏิบัติการที่ได้รับการสนับสนุน

-   ตัวเชื่อมต่อสำหรับ Microsoft Dynamics AX มีตัวติดตั้งแยกต่างหากสองแบบ **Async Server Connector service** และ **Real-time service for Dynamics AX 2012 R3**
-   ส่วนประกอบทั้งสองเป็นแอพพลิเคชั่นแบบ 32 บิต แต่จะทำงานทั้งบนโครงสร้าง x86 และ x64
-   ทั้งสองส่วนประกอบที่ได้รับการสนับสนุนบนระบบปฏิบัติการต่อไปนี้:
    -   รุ่น Windows 7 Professional, Enterprise และ Ultimate
    -   รุ่น Windows 8.1 Update 1 Professional, Enterprise และ Embedded
    -   รุ่น Windows 10 Pro, Enterprise และ Enterprise LTSB
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>ข้อกำหนดของระบบขั้นต่ำ

-   แนะนำให้ใช้ RAM 2 กิกะไบต์, RAM 4 กิกะไบต์
-   ความเร็วของ CPU สูงสุด 1.6 GHz ต่อแกน (ต้องมีอย่างต่ำสองแกน)
-   เนื้อที่ว่างอย่างน้อย 10 กิกะไบต์ (ฐานข้อมูลช่องทางอาจต้องการเนื้อที่ว่างจำนวนมาก)

## <a name="requirements-for-development-on-local-vms"></a>ข้อกำหนดสำหรับการพัฒนาบน VM เฉพาะที่
สำหรับข้อมูลเกี่ยวกับข้อกำหนดสำหรับการพัฒนาเครื่องเสมือนจริงเฉพาะที่ (VM) ให้ดูที่ [VM ที่เรียกใช้แบบ On-premises](../dev-tools/access-instances.md)

<a name="see-also"></a>ดูเพิ่มเติมที่
--------

[รับสำเนาการประเมิน-v' Dynamics 365 for Finance and Operations, Enterprise Edition](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)





