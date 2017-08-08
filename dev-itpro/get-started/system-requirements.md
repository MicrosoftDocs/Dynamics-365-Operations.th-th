---
title: "ความต้องการของระบบ"
description: "หัวข้อนี้แสดงความต้องการของระบบสำหรับรุ่นล่าสุดของ Microsoft Dynamics 365 Finance and Operations, Enterprise edition สำหรับระบบคลาวด์และการปรับใช้ในองค์กร"
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: th-th
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>ความต้องการของระบบ

[!include[banner](../includes/banner.md)]


หัวข้อนี้แสดงความต้องการของระบบสำหรับรุ่นล่าสุดของ Microsoft Dynamics 365 Finance and Operations, Enterprise edition สำหรับระบบคลาวด์และการปรับใช้ในองค์กร ก่อนที่คุณจะทำการติดตั้ง Finance and Operations เมื่อเหมาะสม ให้ตรวจสอบว่าระบบที่คุณกำลังทำงานมีคุณสมบัติตรงตามหรือสูงกว่าความต้องการต่ำสุดด้านเครือข่าย ฮาร์ดแวร์ และซอฟต์แวร์


## <a name="supported-microsoft-office-applications"></a>แอพลิเคชัน Microsoft Office ที่ได้รับการสนับสนุน
แอพลิเคชัน Office ต่อไปนี้ได้รับการสนับสนุนในระบบคลาวด์และการปรับใช้ในองค์กรของ Finance and Operations
-   เมื่อต้องการเรียกใช้ Add-in ของ Microsoft Excel และ Word คุณจะต้องตั้งค่า Microsoft Office 2016 สำหรับ Windows หรือ Mac ไว้ สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับข้อกำหนดเวอร์ชัน ให้ดูที่ [การแก้ไขปัญหาการรวม Office](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting)
-   เมื่อต้องการดูเอกสารที่สร้างขึ้นโดยฟังก์ชันส่งออกไปที่ Excel หรือส่งออกไปที่ Word คุณต้องติดตั้ง Microsoft Office 2007 หรือรุ่นที่ใหม่กว่าไว้

# <a name="system-requirements-specific-to-cloud-deployments"></a>การปรับใช้ในองค์กรเฉพาะสำหรับการปรับใช้ระบบคลาวด์
## <a name="network-requirements"></a>ข้อกำหนดของเครือข่าย
-   Finance and Operations ได้รับการออกแบบมาสำหรับเครือข่ายที่มีเวลาแฝง 250-300 มิลลิวินาที (ms) หรือน้อยกว่า นี่คือเวลาแฝงจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Microsoft Azure ที่โฮสต์ Finance and Operations เราขอแนะนำให้คุณทดสอบเวลาแฝงบนเครือข่ายที่ <http://www.azurespeed.com>
-   ข้อกำหนดของแบนด์วิธสำหรับ Finance and Operations ขึ้นอยู่กับสถานการณ์ของคุณ สถานการณ์ทั่วไปส่วนใหญ่จำเป็นต้องมีแบนด์วิดท์ที่มากกว่า 50 กิโลไบต์ต่อวินาที (KBps) อย่างไรก็ตาม สำหรับสถานการณ์ที่มีข้อกำหนดของน้ำหนักบรรทุกที่สร้างรายได้ที่สูง เช่น พื้นที่ทำงานหรือสถานการณ์ที่เกี่ยวข้องกับการกำหนดเองที่ครอบคลุม ระบบแนะนำให้ใช้แบนด์วิดท์ที่มากขึ้น

โดยทั่วไป Finance and Operations จะเหมาะสำหรับอินเทอร์เน็ต จำนวนของการเดินทางไปกลับจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Azure มีขนาดเล็กมาก และน้ำหนักบรรทุกที่สร้างรายได้ทั้งหมดจะถูกบีบอัด 

> [!WARNING]
> อย่าคำนวณข้อกำหนดของแบนด์วิดท์จากตำแหน่งที่ตั้งของไคลเอนต์ โดยการคูณจำนวนผู้ใช้กับข้อกำหนดของแบนด์วิดท์ต่ำสุด การใช้งานที่เกิดขึ้นพร้อมกันของตำแหน่งที่ตั้งที่กำหนดเป็นสิ่งที่คำนวณได้ยาก สำหรับลูกค้าที่มีความกังวลเกี่ยวกับข้อกำหนดของแบนด์วิดท์ ให้ใช้ Finance and Operations เวอร์ชันตัวอย่าง

## <a name="net-framework-requirements"></a>ข้อกำหนดของ .NET Framework
Finance and Operations ต้องมี .NET Framework รุ่น 4.6.2 สำหรับแอพลิเคชันแบบคลิกครั้งเดียวทั้งหมด เช่น ตัวแทนเส้นทางของเอกสาร สำหรับคำแนะนำในการติดตั้ง ให้ดูที่ [การติดตั้ง .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx)

## <a name="supported-web-browsers"></a>เว็บเบราเซอร์ที่สนับสนุน
โปรแกรมประยุกต์บนเว็บสามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ที่ทำงานบนระบบปฏิบัติการที่ระบุ:


-   Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10
-   Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7
-   Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus แท็บเล็ต 10
-   Apple Safari (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) หรือ 10.12 (Sierra) หรือ Apple iPad

เมื่อต้องการค้นหารุ่นล่าสุดของแต่ละเว็บเบราเซอร์ ไปที่เว็บไซต์ของผู้ผลิตซอฟต์แวร์ 

> [!NOTE]
> -   จะต้องติดตั้งส่วนขยายของ Chrome เวอร์ชันก่อนวางจำหน่ายเพื่ออนุญาตให้รวบรวมภาพหน้าจอโดยตัวบันทึกงานและรวมเข้าไปใน Microsoft Word documents โดยอัตโนมัติ <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   ตัวแก้ไขเวิร์กโฟลว์จะเริ่มต้นการใช้งานเป็นแอพลิเคชัน ClickOnce เฉพาะ Microsoft Edge และ Internet Explorer (ในรุ่นที่สนับสนุนของ Microsoft Windows) สนับสนุนแอพลิเคชัน ClickOnce แอพลิเคชัน ClickOnce โปรแกรมแก้ไขลำดับงานต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต
> -   โปรแกรมออกแบบรายงานสำหรับการรายงานทางการเงินจะถูกเริ่มต้นโดยเป็นแอพลิเคชัน ClickOnce ต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต ถ้าคุณใช้ Chrome คุณต้องติดตั้งส่วนขยาย ClickOnce เพื่อที่จะดาวน์โหลดไคลเอ็นต์โปรแกรมออกแบบรายงาน ถ้าคุณกำลังใช้ Chrome พร้อมกับโหมด incognito ให้ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานส่วนขยาย ClickOnce สำหรับโหมด incognito แล้ว
> -   เมื่อต้องการแสดงตัวอย่างไฟล์ PDF เราขอแนะนำให้คุณใช้เบราว์เซอร์ เช่น Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10 หรือ Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บนแท็บเล็ต Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus 10


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>เบราเซอร์ที่สนับสนุนสำหรับ Retail Cloud POS

Retail Cloud POS สามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ที่ทำงานบนระบบปฏิบัติการที่ระบุ:

-   Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10
-   Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7
-   Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10, Windows 8.1 หรือ Windows 7

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
    -   รุ่น Windows 7 Professional, Enterprise และ Ultimate 
    
    > [!NOTE]
    > Windows 7 ได้รับการสนับสนุนเฉพาะเมื่อมีการติดตั้ง Internet Explorer 11 บนระบบด้วยตนเอง

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

# <a name="system-requirements-for-on-premises-deployments"></a>ความต้องการของระบบสำหรับการปรับใช้ในองค์กร

## <a name="network-requirements"></a>ข้อกำหนดของเครือข่าย
Finance and Operations (ในองค์กร) สามารถทำงานบนเครือข่ายที่ใช้ Internet Protocol เวอร์ชัน 4 (IPv4) หรือ Internet Protocol เวอร์ชัน 6 (IPv6) พิจารณาสภาพแวดล้อมเครือข่ายเมื่อคุณวางแผนระบบของคุณ และใช้คำแนะนำต่อไปนี้

### <a name="network-response-time"></a>เวลาในการตอบสนองเครือข่าย
ตารางต่อไปนี้แสดงรายการข้อกำหนดต่ำสุดของเครือข่าย สำหรับการเชื่อมต่อระหว่างเว็บเบราเซอร์และ Application Object Server (AOS) และการเชื่อมต่อระหว่าง AOS และฐานข้อมูลในระบบภายในองค์กร

| มูลค่า     | เว็บเบราเซอร์ไปยัง AOS | AOS ไปยังฐานข้อมูล                                            |
|-----------|--------------------|------------------------------------------------------------|
| แบนด์วิธ | 50 KBps ต่อผู้ใช้   | 100 MBps                                                   |
| เวลาแฝง   | < 250-300 มิลลิวินาที       | < 1 มิลลิวินาที (LAN เท่านั้น) AOS และฐานข้อมูลจำเป็นต้องอยู่ร่วมกัน |

- Finance and Operations (ในองค์กร) ได้รับการออกแบบมาสำหรับเครือข่ายที่มีเวลาแฝง 250–300 มิลลิวินาที (ms) หรือน้อยกว่า เวลาแฝงนี้คือเวลาแฝงจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูลที่โฮสต์ Finance and Operations
- ข้อกำหนดของแบนด์วิธสำหรับ Finance and Operations (ในองค์กร) ขึ้นอยู่กับสถานการณ์ของคุณ สถานการณ์ทั่วไปต้องมีแบนด์วิธของมากกว่า 50 กิโลไบต์ต่อวินาที (KBps) ระหว่างเบราเซอร์และเซิร์ฟเวอร์ Finance and Operations อย่างไรก็ตาม สำหรับสถานการณ์ที่มีข้อกำหนดของน้ำหนักบรรทุกที่สร้างรายได้ที่สูง เช่น พื้นที่ทำงานหรือสถานการณ์ที่เกี่ยวข้องกับการกำหนดเองที่ครอบคลุม ระบบแนะนำให้ใช้แบนด์วิดท์ที่สูงขึ้นและขึ้นอยู่กับการใช้งาน
ไม่สนับสนุนการปรับใช้ที่ AOS และฐานข้อมูล SQL Server อยู่ในศูนย์ข้อมูลอื่น AOS และฐานข้อมูล SQL Server จำเป็นต้องอยู่ร่วมกัน โดยทั่วไป Finance and Operations จะมีประสิทธิภาพในการลดการเดินทางไปกลับระหว่างเบราเซอร์และเซิร์ฟเวอร์ จำนวนของรอบการเดินทางไปกลับจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูลอาจเป็นศูนย์หรือหนึ่งสำหรับการโต้ตอบของผู้ใช้แต่ละครั้ง และน้ำหนักบรรทุกทั้งหมดจะถูกบีบอัด

> [!WARNING]
> อย่าคำนวณข้อกำหนดของแบนด์วิดท์จากตำแหน่งที่ตั้งของไคลเอนต์ โดยการคูณจำนวนผู้ใช้กับข้อกำหนดของแบนด์วิดท์ต่ำสุด การใช้งานที่เกิดขึ้นพร้อมกันของตำแหน่งที่ตั้งที่กำหนดเป็นสิ่งที่คำนวณได้ยาก เราแนะนำให้ใช้การจำลองจากชีวิตจริงโดยเทียบกับสภาพแวดล้อมที่ไม่ใช้งานจริงของ Finance and Operations เป็นการประเมินประสิทธิภาพที่ดีที่สุดสำหรับกรณีเฉพาะของคุณ 

### <a name="lan-environments"></a>สภาพแวดล้อม LAN
ในสภาพแวดล้อมเครือข่ายท้องถิ่น (LAN) นั้น ไม่จำเป็นต้องให้ Microsoft Remote Desktop ใน Microsoft Windows Server เชื่อมต่อกับ Finance and Operations อย่างไรก็ตาม การเชื่อมต่อนี้อาจจำเป็นสำหรับการให้บริการการดำเนินงานบน VM ที่ประกอบขึ้นเป็นการปรับใช้งานเซิร์ฟเวอร์

### <a name="wan-environments"></a>สภาพแวดล้อม WAN
ในสภาพแวดล้อมเครือข่ายบริเวณกว้าง (WAN) นั้น ไม่จำเป็นต้องให้เซิร์ฟเวอร์ Remote Desktop ใน Windows Server เชื่อมต่อกับ Finance and Operations

### <a name="internet-connectivity-requirements"></a>ข้อมูลความต้องการการเชื่อมต่ออินเทอร์เน็ต
Finance and Operations (ในองค์กร) ไม่จำเป็นต้องมีการเชื่อมต่ออินเทอร์เน็ตจากสถานีงานผู้ใช้ปลายทาง อย่างไรก็ตาม คุณลักษณะบางอย่างจะไม่พร้อมใช้งานหากไม่เชื่อมต่ออินเทอร์เน็ต

| ไคลเอนต์เบราเซอร์ | สถานการณ์อินทราเน็ตที่ไม่มีการเชื่อมต่ออินเทอร์เน็ตเป็นจุดออกแบบสำหรับตัวเลือกการปรับใช้ในองค์กร คุณลักษณะบางอย่างที่จำเป็นต้องใช้บริการระบบคลาวด์จะไม่พร้อมใช้งาน เช่นวิธีใช้และไลบรารีคู่มืองานใน LCS |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| เซิร์ฟเวอร์         | ระดับ AOS หรือ Service Fabric ต้องสามารถสื่อสารกับ LCS ได้ ไคลเอ็นต์เบราเซอร์ในองค์กรไม่จำเป็นต้องเชื่อมต่อกับอินเทอร์เน็ต                                                                                |
| การตรวจวัดระยะไกล      | ข้อมูลการตรวจวัดระยะไกลอาจสูญถ้าการเชื่อมต่อถูกขัดจังหวะเป็นเวลานาน การขัดจังหวะในการเชื่อมต่อกับ LCS จะไม่มีผลกระทบต่อฟังก์ชันการทำงานของแอพลิเคชันในองค์กร                                                |
| LCS            | จำเป็นต้องมีการเชื่อมต่อกับ LCS สำหรับการปรับใช้ การปรับใช้รหัสและการให้บริการการดำเนินงาน                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>ข้อมูลการตรวจวัดระยะไกลโอนย้ายไปยังระบบคลาวด์
ข้อมูลการตรวจวัดระยะไกลส่วนใหญ่จะจัดเก็บไว้ภายในเครื่อง และสามารถเข้าถึงได้โดยใช้ตัวแสดงเหตุการณ์ใน Microsoft Windows เซ็ตย่อยขนาดเล็กของเหตุการณ์การตรวจวัดระยะไกลจะถูกโอนย้ายไปยังไปป์ไลน์ Microsoft telemetry ในระบบคลาวด์เพื่อประกอบการวินิจฉัย ภายในข้อมูลการตรวจวัดระยะไกลที่ส่งไปยัง Microsoft จะไม่มีข้อมูลของลูกค้าและข้อมูลที่ระบุถึงตัวบุคคล ชื่อ VM จะถูกส่งไปยัง Microsoft เพื่อช่วยในการจัดการสภาพแวดล้อมและการวินิจฉัยจากพอร์ทัล LCS

## <a name="domain-requirements"></a>ข้อกำหนดโดเมน
พิจารณาข้อกำหนดโดเมนต่อไปนี้เมื่อคุณติดตั้ง Finance and Operations (ในองค์กร):

- ส่วนประกอบของเครื่องเสมือนที่โฮสต์ Finance and Operations (ในองค์กร) จะต้องเป็นสมาชิกของโดเมน Active Directory ต้องตั้งค่าคอนฟิก Active Directory Domain Services (AD DS) ไว้ในโหมดดั้งเดิม
- ส่วนประกอบของเครื่องเสมือนที่รัน Finance and Operations (ในองค์กร) ต้องมีการเข้าถึงการตั้งค่าคอนฟิกในระหว่าง Active Directory Domain Services 
- ตัวควบคุมโดเมนจะต้องรันบน Microsoft Windows Server 2016

## <a name="hardware-requirements"></a>ข้อกำหนดของฮาร์ดแวร์
ส่วนนี้อธิบายถึงฮาร์ดแวร์ที่จำเป็นในการรัน Finance and Operations (ในองค์กร)
ขึ้นอยู่กับการตั้งค่าคอนฟิกระบบ องค์ประกอบของข้อมูล และแอพลิเคชันและคุณลักษณะที่คุณเลือกใช้ ข้อกำหนดของฮาร์ดแวร์ตามจริงจะแตกต่างกันไป นี่คือบางอย่างของปัจจัยที่อาจส่งผลกระทบต่อการตัดสินใจเลือกฮาร์ดแวร์ที่เหมาะสมสำหรับ Finance and Operations (ในองค์กร):

- จำนวนธุรกรรมต่อชั่วโมง
- จำนวนผู้ใช้ที่เกิดขึ้นพร้อมกัน

## <a name="minimum-infrastructure-requirements"></a>ข้อกำหนดโครงสร้างพื้นฐานต่ำสุด
Finance and Operations (ในองค์กร) ใช้ Microsoft Azure Service Fabric ในการโฮสต์ AOS, ชุดงาน, การจัดการข้อมูล, Management Reporter และบริการ Orchestrator สภาพแวดล้อม ไม่มีการโฮสต์ Microsoft SQL Server Reporting Services (SSRS) ในคลัสเตอร์ Service Fabric
ต้องตั้งค่า SQL Server ในการตั้งค่า HADRON พร้อมใช้งานสูงที่มีอย่างน้อยสองโหนดสำหรับการใช้งานการผลิต
ภาพประกอบต่อไปนี้แสดงจำนวนโหนดต่ำสุดที่แนะนำในคลัสเตอร์ Service Fabric ของคุณ

[![จำนวนโหนดที่สำหรับคลัสเตอร์ Service Fabric](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>ข้อมูลความต้องการเกี่ยวกับโพรเซสเซอร์และ RAM
ตารางต่อไปนี้แสดงจำนวนโพรเซสเซอร์และหน่วยความจำเข้าถึงโดยสุ่ม (RAM) ที่จำเป็นสำหรับแต่ละบทบาทที่จำเป็นในการรันตัวเลือกการปรับใช้นี้ สำหรับข้อมูลเพิ่มเติม ให้อ่านคำแนะนำเกี่ยวกับความต้องการต่ำสุดสำหรับคลัสเตอร์ Service Fabric แบบสแตนด์อโลน [วางแผนและจัดเตรียมคลัสเตอร์ Service Fabric ของคุณ](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)

> [!NOTE]
> ในกรณีที่มีการติดตั้งซอฟต์แวร์อื่น ๆ ของ Microsoft บนคอมพิวเตอร์เครื่องเดียวกัน ระบบต้องสอดคล้องกับข้อกำหนดของฮาร์ดแวร์สำหรับซอฟต์แวร์นั้นด้วย เราขอแนะนำว่า คุณควรจำกัดการใช้ทรัพยากรของแอพลิเคชันเซิร์ฟเวอร์อื่น ๆ ในคอมพิวเตอร์เครื่องเดียวกับ AOS ให้อยู่ภายใน RAM 1 กิกะไบต์ (GB)

**ปรับขนาดตามบทบาทและชนิดโทโพโลยี**

| โทโพโลยี   | บทบาท (ชนิดของโหนด)              | จำนวนแกนประมวลผลที่แนะนำ | หน่วยความจำที่แนะนำ (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| การผลิต | AOS, การจัดการข้อมูล, ชุดงาน   | 8                           | 24                      |
|            | Management Reporter           | 4 ชั่วโมง                           | 16                      |
|            | SQL Server Reporting Services | 4 ชั่วโมง                           | 16                      |
|            | Orchestrator                  | 4 ชั่วโมง                           | 16                      |
| Sandbox    | AOS, การจัดการข้อมูล, ชุดงาน   | 4 ชั่วโมง                           | 24                      |
|            | Management Reporter           | 4 ชั่วโมง                           | 16                      |
|            | SQL Server Reporting Services | 4 ชั่วโมง                           | 16                      |
|            | Orchestrator                  | 4 ชั่วโมง                           | 16                      |

**ขนาดต่ำสุดที่ประเมินสำหรับการผลิตและการปรับใช้ Sandbox**\*

| โทโพโลยี                                  | บทบาท                          | จำนวนของอินสแตนซ์ |
|-------------------------------------------|-------------------------------|---------------------|
| การผลิต                                | AOS (การจัดการข้อมูล, ชุดงาน)  | 3                   |
|                                           | Management Reporter           | 2                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator\*\*                | 3                   |
| Sandbox                                   | AOS, การจัดการข้อมูล, ชุดงาน   | 2                   |
|                                           | Management Reporter           | 1                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator                  | 3                   |
| *สรุปการผลิตและโทโพโลยี Sandbox* |                               | 16                  |

\*ตัวเลขเหล่านี้มีตรวจสอบความถูกต้องโดยลูกค้าแสดงตัวอย่างของเรา และสามารถปรับปรุงตามความจำเป็น โดยอ้างอิงจากข้อคิดเห็นของลูกค้า

\*\*Orchestrator ถูกกำหนดเป็นชนิดโหนหลัก และจะใช้เพื่อรันบริการ Service Fabric เช่นกัน

**การประเมิน Backend SQL Server และ AD ขั้นต้น**

[![การประเมิน Backend SQL Server และ AD ขั้นต้น](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*ขนาดของ SQL Server จะขึ้นอยู่กับปริมาณงานเป็นอย่างมาก สำหรับข้อมูลเพิ่มเติม ให้ดูส่วน [ขนาดฮาร์ดแวร์สำหรับสภาพแวดล้อมในองค์กร](#Hardware-sizing-for-on-premises-environments)

## <a name="storage"></a>ที่จัดเก็บ

- **AOS** - Finance and Operations (ในองค์กร) จะใช้บล็อคข่าวสารเซิร์ฟเวอร์ (SMB) 3.0 ที่ใช้ร่วมกันในการจัดเก็บข้อมูลที่ไม่มีโครงสร้าง สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [พื้นที่จัดเก็บโดยตรงใน Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview)
- **SQL** – ตัวเลือกที่ใช้การได้:
    - การตั้งค่าไดรฟ์โซลิดสเทต (SSD) พร้อมใช้งานสูง
    - Storage Area Network (SAN) ที่มีประสิทธิภาพสำหรับความสามารถประมวลผล OLTP
    - ที่จัดเก็บแบบแนบโดยตรง (DAS) ประสิทธิภาพสูง 
- **SQL และ IOPS การจัดการข้อมูล** – ที่จัดเก็บสำหรับทั้งการจัดการข้อมูลและ SQL Server ควรมีอย่างน้อย 2000 การดำเนินงานอินพุต/เอาพุตต่อวินาที (IOPS) IOPS การผลิตนั้นขึ้นอยู่กับหลายปัจจัย สำหรับข้อมูลเพิ่มเติม ให้ดูส่วน "ขนาดฮาร์ดแวร์สำหรับสภาพแวดล้อมในองค์กร" 
- **IOPS เครื่องเสมือน** – เครื่องเสมือนแต่ละเครื่องควรมีอย่างน้อย 100 write IOPS

## <a name="virtual-host-requirements"></a>ความต้องการโฮสต์เสมือน
เมื่อคุณตั้งค่าโฮสต์เสมือนสำหรับสภาพแวดล้อม Finance and Operations (ในองค์กร) ให้อ้างอิงคำแนะนำต่อไปนี้: [วางแผนและจัดเตรียมคลัสเตอร์ Service Fabric ของคุณ](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) และ [การอธิบายคลัสเตอร์ Service Fabric](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description) โฮสต์เสมือนแต่ละระบบควรมีแกนประมวลผลเพียงพอสำหรับขนาดโครงสร้างพื้นฐานที่จะสร้างขึ้น อาจเป็นไปได้ที่จะมีการตั้งค่าคอนฟิกขั้นสูงหลายชุด ในกรณีที่ SQL Server อยู่บนฮาร์ดแวร์จริง แต่องค์ประกอบอื่น ๆ จะถูกสร้างขึ้นบนระบบเสมือน ถ้า SQL Server ถูกสร้างขึ้นบนระบบเสมือน ระบบย่อยดิสก์ ควรจะเป็น SAN ด่วนหรือเทียบเท่า ในทุกกรณี โปรดตรวจสอบให้แน่ใจว่าการตั้งค่าพื้นฐานของโฮสต์เสมือนมีความพร้อมใช้งานสูงและซ้ำซ้อน ในทุกกรณี เมื่อมีการใช้ระบบเสมือน ไม่ควรมีการทำสแนปช็อต VM

## <a name="software-requirements-for-all-server-computers"></a>ข้อกำหนดของซอฟต์แวร์สำหรับคอมพิวเตอร์เซิร์ฟเวอร์ทั้งหมด
ซอฟต์แวร์ต่อไปนี้ต้องมีอยู่บนคอมพิวเตอร์ก่อน จึงจะสามารถติดตั้งส่วนประกอบ Finance and Operations (ในองค์กร) ได้:

- Microsoft .NET Framework 4.5.1 หรือสูงกว่า
- Service Fabric สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [วางแผนและจัดเตรียมคลัสเตอร์ Service Fabric ของคุณ](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)

## <a name="supported-server-operating-systems"></a>ระบบปฏิบัติการของเซิร์ฟเวอร์ที่สนับสนุน
ตารางต่อไปนี้แสดงรายการระบบปฏิบัติการเซิร์ฟเวอร์ที่สนับสนุนสำหรับส่วนประกอบ Finance and Operations

| ระบบปฏิบัติการ                                     | บันทึก                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter หรือมาตรฐาน | ข้อกำหนดเหล่านี้ใช้สำหรับฐานข้อมูลและคลัสเตอร์ Service Fabric ที่โฮสต์ AOS |

## <a name="software-requirements-for-database-servers"></a>ข้อกำหนดของซอฟต์แวร์สำหรับเซิร์ฟเวอร์ฐานข้อมูล

- เฉพาะ SQL Server 2016 เวอร์ชัน 64 บิต เท่านั้นที่ได้รับการสนับสนุน
- ในสภาพแวดล้อมการผลิต เราขอแนะนำให้คุณติดตั้งโปรแกรมปรับปรุงสะสม (CU) ล่าสุดสำหรับ SQL Server เวอร์ชันที่คุณกำลังใช้
- Finance and Operations (ในองค์กร) สนับสนุนการเรียง Unicode ที่ตรงตามตัวพิมพ์ใหญ่เล็ก ตรงตามอักขระการออกเสียง ตรงตามตัวคะนะ และไม่ตรงตามความกว้าง การเรียงต้องตรงตามที่ตั้ง Windows ของคอมพิวเตอร์ที่รันอินสแตนซ์ AOS ถ้าคุณกำลังตั้งค่าการติดตั้งใหม่ เราขอแนะนำให้คุณเลือกการเรียง Windows แทนการเรียง SQL Server ดูข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเลือกการเรียงสำหรับฐานข้อมูล SQL Server ได้ที่ [เอกสาร SQL Server](/sql/sql-server/sql-server-technical-documentation)
ตารางต่อไปนี้แสดงเวอร์ชัน SQL Server ที่สนับสนุนสำหรับฐานข้อมูล Finance and Operations สำหรับข้อมูลเพิ่มเติม ให้ดูความต้องการขั้นต่ำของฮาร์ดแวร์สำหรับ [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016)

| ความต้องการ                                                      | บันทึก                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition หรือ Enterprise Edition | สำหรับความต้องการของฮาร์ดแวร์สำหรับ SQL Server 2016 ให้ดูที่ [ความต้องการฮาร์ดแวร์และซอฟต์แวร์สำหรับการติดตั้ง SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server) |

## <a name="software-requirements-for-client-computers"></a>ข้อกำหนดของซอฟต์แวร์สำหรับคอมพิวเตอร์ไคลเอนท์ทั้งหมด
เว็บแอพลิเคชัน Finance and Operations สามารถรันบนอุปกรณ์ใด ๆ ที่มีเว็บเบราเซอร์ที่รองรับ HTML5.0 ชุดอุปกรณ์เฉพาะ/เบราเซอร์ที่ Microsoft ยืนยันประกอบด้วย:

- Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10
- Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7
- Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus แท็บเล็ต 10
- Apple Safari (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) หรือ 10.12 (Sierra) หรือ Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>ข้อกำหนดของซอฟต์แวร์สำหรับสำหรับ Active Directory Federation Services 
Active Directory Federation Services (AD FS) บน Windows Server 2016

ตัวควบคุมโดเมนจะต้องเป็น Windows Server 2012 R2 หรือใหม่กว่า โดยมีระดับฟังก์ชันโดเมน 2012 R2 หรือมากกว่า

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับระดับฟังก์ชันโดเมน ให้ดูที่: 
- [ระดับฟังก์ชัน Active Directory คืออะไร](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [การทำความเข้าใจเกี่ยวกับระดับฟังก์ชัน Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>ข้อกำหนดของฮาร์ดแวร์และซอฟต์แวร์สำหรับองค์ประกอบของระบบการขายปลีก
Finance and Operations (ในองค์กร) ไม่มีองค์ประกอบของระบบการขายปลีกในขณะนี้

<a name="see-also"></a>ดูเพิ่มเติมที่
--------

[รับสำเนาการประเมิน-v' Dynamics 365 for Finance and Operations, Enterprise Edition](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

