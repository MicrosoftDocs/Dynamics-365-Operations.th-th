---
title: "ตั้งค่าและปรับใช้สภาพแวดล้อมในองค์กร"
description: "หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการวางแผน ตั้งค่าและปรับใช้สภาพแวดล้อมในองค์กร"
author: kfend
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d100f6dbcbdf8f4c12ab04670fb598a88d48d84b
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: th-th
ms.lasthandoff: 08/10/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>ตั้งค่าและปรับใช้สภาพแวดล้อมในองค์กร

เอกสารนี้อธิบายวิธีการวางแผนการปรับใช้ ตั้งค่าโครงสร้างพื้นฐาน และการปรับใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (ในองค์กร)

## <a name="finance-and-operations-components"></a>ส่วนประกอบของการเงินและการดำเนินงาน (Finance and Operations)

แอพลิเคชันทางการเงินและการดำเนินงานประกอบด้วยส่วนประกอบหลักสามส่วน:

- Application Object Server (AOS)
- ข่าวกรองธุรกิจ (BI)
- การรายงานทางการเงิน/ Management Reporter

ส่วนประกอบเหล่านี้ขึ้นอยู่กับซอฟต์แวร์ระบบต่อไปนี้:

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1 ซึ่งมีคุณลักษณะดังต่อไปนี้:

    - เปิดใช้งานการค้นหาดัชนีข้อความแบบเต็ม
    - บริการรายงาน SQL Server (SSRS)
    - SQL Server Integration Services (SSIS)
    
     > [!NOTE]
     > แอพลิเคชันจะไม่ทำงานถ้าไม่ได้เปิดใช้งานการค้นหาข้อความแบบเต็ม

- SQL Server Management Studio
- โครงสร้างบริการ Microsoft Azure แบบสแตนด์อโลน
- Windows PowerShell 5.0 หรือสูงกว่า
- Active Directory Federation Services (AD FS) บน Windows Server 2016

  ตัวควบคุมโดเมนจะต้องเป็น Windows Server 2012 R2 หรือใหม่กว่า ด้วยระดับฟังก์ชันโดเมน 2012 R2 หรือมากกว่า

  สำหรับข้อมูลเพิ่มเติมเกี่ยวกับระดับฟังก์ชันโดเมน ให้ดูที่: 
  - [ระดับฟังก์ชัน Active Directory คืออะไร](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [การทำความเข้าใจเกี่ยวกับระดับฟังก์ชัน Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

บิตการเงินและการดำเนินงานจะแจกจ่ายผ่าน Microsoft Dynamics Lifecycle Services (LCS) ก่อนที่คุณจะทำการปรับใช้ คุณต้องซื้อคีย์ลิขสิทธิ์ผ่านช่องทาง [ข้อตกลงองค์กร](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) และตั้งค่าโครงการสำหรับใช้งานในองค์กรใน LCS การปรับใช้จะต้องเริ่มดำเนินการผ่านทาง LCS เท่านั้น ดูข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าโครงการในสถานที่ใน LCS ได้ที่ [สร้างโครงการสำหรับใช้งานในองค์กรใน Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md)

## <a name="authentication"></a>การรับรองความถูกต้อง

แอพลิเคชันในองค์กรจะทำงานกับ AD FS ในการโต้ตอบกับ LCS คุณต้องตั้งค่าคอนฟิก Azure Active Directory (Azure AD)

## <a name="standalone-service-fabric"></a>Service Fabric แบบสแตนด์อโลน

Finance and Operations ใช้ Service Fabric แบบสแตนด์อโลน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เอกสาร Service Fabric](/azure/service-fabric/)

## <a name="infrastructure"></a>โครงสร้างพื้นฐาน

Finance and Operations ถูกออกแบบมาให้ทำงานบนสถาปัตยกรรมแบบ Hyper-Converged การตั้งค่าคอนฟิกฮาร์ดแวร์มีองค์ประกอบดังต่อไปนี้:

- คลัสเตอร์ Service Fabric แบบสแตนด์อโลนที่ใช้เครื่องเสมือน Windows Server 2016 (VMs)
- SQL Server (สนับสนุนทั้ง SQL แบบคลัสเตอร์และแบบพร้อมใช้งานเสมอ)
- AD FS สำหรับการรับรองความถูกต้อง
- การใช้ไฟล์บล็อคข่าวสารเซิร์ฟเวอร์ (SMB) เวอร์ชัน 3 ร่วมกันสำหรับการจัดเก็บ
- ไม่จำเป็น: Microsoft Office Server 2017

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ความต้องการระบบ](../get-started/system-requirements.md) และแนวทางการกำหนดขนาด

### <a name="hardware-layout"></a>โครงร่างฮาร์ดแวร์

วางแผนโครงสร้างพื้นฐานและคลัสเตอร์ Service Fabric ของคุณตามการกำหนดขนาดที่แนะนำใน [การกำหนดฮาร์ดแวร์สำหรับสภาพแวดล้อมในองค์กร](../get-started/hardware-sizing-on-premises-environments.md) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการวางแผนคลัสเตอร์ Service Fabric ให้ดูที่ [การวางและจัดเตรียมการปรับใช้คลัสเตอร์ Service Fabric แบบสแตนด์อโลนของคุณ](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)

ตารางต่อไปนี้แสดงตัวอย่างของโครงร่างฮาร์ดแวร์ ตัวอย่างนี้ใช้ตลอดทั้งหัวข้อนี้เพื่อแสดงวิธีการตั้งค่า

> [!NOTE]
> โหนดหลักของคลัสเตอร์ Service Fabric ต้องมีอย่างน้อยสามโหนด ในตัวอย่างนี้ **OrchestratorType** ถูกกำหนดเป็นชนิดโหนหลัก

| วัตถุประสงค์ของเครื่อง                                 | ชื่อเครื่อง    | ที่อยู่ IP    |
|-------------------------------------------------|-----------------|---------------|
| ตัวควบคุมโดเมน                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| เซิร์ฟเวอร์ไฟล์                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| คลัสเตอร์ SQL Always-On                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| ลูกค้า                                          | SQLAOCLIENT1    | 10.179.108.11 |
| คลัสเตอร์ Service Fabric/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| คลัสเตอร์ Service Fabric/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| คลัสเตอร์ Service Fabric/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| คลัสเตอร์ Service Fabric/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| คลัสเตอร์ Service Fabric/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| คลัสเตอร์ Service Fabric/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| คลัสเตอร์ Service Fabri/โหนด Management Reporter | SQLAOSMR1       | 10.179.108.18 |
| คลัสเตอร์ Service Fabric/โหนด SSRS                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>การตั้งค่า

### <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

คุณต้องทำตามข้อกำหนดเบื้องต้นต่อไปนี้ ก่อนเริ่มตั้งค่า การตั้งค่าข้อกำหนดเบื้องต้นเหล่านี้อยู่นอกขอบเขตสำหรับเอกสารนี้

- มีการติดตั้งและตั้งค่าคอนฟิก Active Directory Domain Services (AD DS) ในเครือข่ายของคุณ
- มีการปรับใช้ AD FS
- มีการติดตั้ง SQL Server, SSRS และ Management Studio

### <a name="overview"></a>ภาพรวม

ในการตั้งค่าโครงสร้างพื้นฐานสำหรับ Finance and Operations จะต้องทำขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์

1. วางแผนชื่อโดเมนและโซน DNS
2. วางแผนและจัดหาใบรับรองของคุณ
3. วางแผนผู้ใช้และบัญชีบริการของคุณ
4. สร้างโซน DNS และเพิ่มเรกคอร์ด A
5. รวม VM เข้ากับโดเมน
6. เพิ่มข้อกำหนดเบื้องต้นของซอฟต์แวร์ใน VM
7. ดาวน์โหลดสคริปต์การตั้งค่าจาก LCS
8. อธิบายการตั้งค่าคอนฟิกของคุณ
9. ติดตั้งใบรับรอง
10. ตั้งค่าคลัสเตอร์ Service Fabric แบบสแตนด์อโลน
11. ตั้งค่าคอนฟิกการเชื่อมต่อ LCS สำหรับผู้เช่า
12. ตั้งค่าหน่วยจัดเก็บไฟล์
13. ตั้งค่า SQL Server
14. ตั้งค่าคอนฟิกฐานข้อมูล
15. เข้ารหัสข้อมูลประจำตัว
16. ตั้งค่า SSRS
17. ตั้งค่าคอนฟิก AD FS

### <a name="plan-your-domain-name-and-dns-zones"></a>วางแผนชื่อโดเมนและโซน DNS

เราขอแนะนำให้คุณใช้ชื่อโดเมนที่มีการลงทะเบียนอย่างเป็นทางการสำหรับการติดตั้งการผลิต AOS ของคุณ ด้วยวิธีการนี้ ระบบจะสามารถเข้าถึงได้ภายนอกเครือข่าย ถ้าจำเป็นต้องมีการเข้าถึงจากภายนอก

ยกตัวอย่างเช่น ถ้าโดเมนของบริษัทของคุณคือ contoso.com โซนสำหรับ Finance and Operations (ในองค์กร) ของคุณอาจเป็น d365ffo.onprem.contoso.com และอาจใช้ชื่อโฮสต์ดังนี้:

- ax.d365ffo.onprem.contoso.com สำหรับเครื่อง AOS
- sf.d365ffo.onprem.contoso.com สำหรับคลัสเตอร์ Service Fabric

### <a name="plan-and-acquire-your-certificates"></a>วางแผนและจัดหาใบรับรองของคุณ

จำเป็นต้องมีใบรับรอง Secure Sockets Layer (SSL) เพื่อรักษาความปลอดภัยสำหรับคลัสเตอร์ Service Fabric และแอพลิเคชันทั้งหมดที่มีการปรับใช้ สำหรับการผลิตของคุณรวมทั้งปริมาณงาน Sandbox เราขอแนะนำให้คุณจัดหาใบรับรองจากผู้ให้บริการออกใบรับรอง (CA) เช่น [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) หรือ [GlobalSign](https://www.globalsign.com/en/ssl/) ถ้าคุณตั้งค่าโดเมนด้วย [บริการใบรับรอง Active Directory](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS ) คุณสามารถสร้างใบรับรองผ่าน AD CS ใบรับรองแต่ละใบจะต้องประกอบด้วยคีย์ส่วนตัวที่สร้างขึ้นสำหรับการแลกเปลี่ยนคีย์ และต้องสามารถส่งออกไปยังไฟล์การแลกเปลี่ยนข้อมูลส่วนบุคคล (.pfx) ได้

ใบรับรองที่ลงชื่อด้วยตนเองสามารถใช้งานเพื่อวัตถุประสงค์ในการทดสอบเท่านั้น เพื่อความสะดวก สคริปต์การตั้งค่าจะรวมสคริปต์ที่สร้างและส่งออกใบรับรองที่ลงชื่อด้วยตนเอง ตามที่ได้กล่าวไปแล้ว ใบรับรองเหล่านี้ต้องใช้สำหรับการทดสอบเท่านั้น

| วัตถุประสงค์                                      | คำอธิบาย | ข้อกำหนดเพิ่มเติม |
|----------------------------------------------|-------------|-------------------------|
| ใบรับรอง SSL สำหรับ SQL Server                   | ใบรับรองนี้ใช้ในการเข้ารหัสข้อมูลที่นำส่งผ่านเครือข่ายระหว่างอินสแตนซ์ของ SQL Server และแอพลิเคชันไคลเอนต์ | <p>ชื่อโดเมนของใบรับรองควรตรงกับชื่อโดเมนเต็ม (FQDN) ของอินสแตนซ์ SQL Server หรือตัวรอรับ</p><p>ยกตัวอย่างเช่น ถ้ามีตัวรอรับ SQL ที่โฮสต์บนเครื่อง DAX7SQLAOSQLA ดังนั้นชื่อ DNS ของใบรับรองจะเป็น DAX7SQLAOSQLA.onprem.contoso.com</p> |
| ใบรับรองเซิร์ฟเวอร์ Service Fabric            | ใบรับรองนี้จะใช้เพื่อช่วยรักษาความปลอดภัยของการสื่อสารแบบโหนดไปยังโหนระหว่างโหนด Service Fabric ใบรับรองนี้ยังใช้เป็นใบรับรองเซิร์ฟเวอร์ที่นำเสนอต่อไคลเอนต์ที่เชื่อมต่อกับคลัสเตอร์ | <p>ชื่อโดเมนของใบรับรองต้องตรงกับโซน DNS ที่โฮสต์ AOS และ Service Fabric</p><p>ยกตัวอย่างเช่นชื่อโดเมนของใบรับรองอาจเป็น \*.onprem.contoso.com หรือ \* .contoso.com</p><p>ถ้าคุณใช้ใบรับรองแบบตัวแทน อักขระตัวแทนจะใช้กับระดับเดียวเท่านั้น ต้องปรับใช้โดเมนย่อย, ชื่อเรื่องสำรอง (SAN) กับใบรับรองถ้ามีมากกว่าหนึ่งระดับ เช่น \*.contoso.com ในตัวอย่างก่อนหน้า</p> |
| ใบรับรองไคลเอนต์ Service Fabric            | ใบรับรองนี้ใช้โดยไคลเอนต์เพื่อดูและจัดการคลัสเตอร์ Service Fabric | |
| ใบรับรองการเข้ารหัส                     | ใบรับรองนี้ใช้ในการเข้ารหัสข้อมูลที่สำคัญ เช่น รหัสผ่านของ SQL Server และรหัสผ่านสำหรับบัญชีผู้ใช้ | <p>การใช้คีย์ใบรับรองต้องมีการเข้ารหัสข้อมูล (10) และไม่ควรการรับรองความถูกต้องของเซิร์ฟเวอร์หรือการรับรองความถูกต้องของไคลเอนต์</p><p>สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การจัดการความลับในแอพลิเคชัน Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management)</p> |
| ใบรับรอง AOS SSL                          | <p>ใบรับรองนี้ใช้เป็นใบรับรองเซิร์ฟเวอร์ที่นำเสนอต่อไคลเอนต์สำหรับเว็บไซต์ AOS นอกจากนี้ยังใช้เพื่อเปิดใช้งาน Windows Communication Foundation (WCF)/ใบรับรอง Simple Object Access Protocol (SOAP)</p><p>สามารถใช้ใบรับรองเซิร์ฟเวอร์ Service Fabric ที่นี่ ถ้าเป็นใบรับรองแบบตัวแทน</p> | <p>ชื่อโดเมนของใบรับรองต้องตรงกับโซน DNS ที่โฮสต์ AOS และ Service Fabric</p><p>ยกตัวอย่างเช่นชื่อโดเมนของใบรับรองอาจเป็น \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com, or \*.contoso.com</p><p>ถ้าคุณใช้ใบรับรองแบบตัวแทน ตัวแทนดังกล่าวจะใช้กับระดับเดียวเท่านั้น ต้องปรับใช้โดเมนย่อย SAN กับใบรับรองถ้ามีมากกว่าหนึ่งระดับ เช่น \*.contoso.com ในตัวอย่างก่อนหน้า</p> |
| ใบรับรองความถูกต้องรอบเวลา           | ใบรับรองนี้ใช้โดย AOS เพื่อช่วยรักษาความปลอดภัยข้อมูลรอบเวลาของผู้ใช้ | ใบรับรองนี้ยังเป็นแบบ **ใช้ไฟล์ร่วมกัน** ซึ่งจะใช้เมื่อมีการปรับใช้จาก LCS |
| ใบรับรองการเข้ารหัสข้อมูลและการลงชื่อข้อมูล | ใบรับรองเหล่านี้ใช้โดย AOS เพื่อเข้ารหัสข้อมูลสำคัญ | |
| ใบรับรองไคลเอนต์การรายงานทางการเงิน       | ใบรับรองนี้ใช้เพื่อช่วยรักษาความปลอดภัยสำหรับการสื่อสารระหว่างบริการการรายงานทางการเงินและ AOS | |
| ใบรับรองการรายงาน                        | ใบรับรองนี้ใช้เพื่อช่วยรักษาความปลอดภัยสำหรับการสื่อสารระหว่าง SSRS และ AOS | |
| ใบรับรองตัวแทนในพื้นที่ภายในองค์กร           | <p>ใบรับรองนี้ใช้เพื่อช่วยรักษาความปลอดภัยสำหรับการสื่อสารระหว่างตัวแทนในพื้นที่ที่มีโฮสต์อยู่ภายในองค์กรและ LCS</p><p>ใบรับรองนี้ช่วยให้ตัวแทนในพื้นที่สามารถดำเนินการในนามของผู้เช่า Azure AD ของคุณ และในการสื่อสารกับ LCS เพื่อประสานและตรวจสอบการปรับใช้</p> | |

### <a name="plan-your-users-and-service-accounts"></a>วางแผนผู้ใช้และบัญชีบริการของคุณ

คุณต้องสร้างผู้ใช้หรือบัญชีบริการต่าง ๆ สำหรับ Finance and Operations (ในองค์กร) เพื่อทำงาน คุณต้องสร้างชุดบัญชีบริการที่จัดการเป็นกลุ่ม (gMSA), บัญชีโดเมน และบัญชี SQL ตารางต่อไปนี้แสดงบัญชีผู้ใช้ วัตถุประสงค์และตัวอย่างชื่อที่จะใช้ในหัวข้อนี้

| บัญชีผู้ใช้                                            | ชนิดข้อมูล           | วัตถุประสงค์ | ชื่อผู้ใช้ |
|---------------------------------------------------------|----------------|---------|-----------|
| บัญชีบริการแอพลิเคชันการรายงานทางการเงิน         | gMSA           |         | Contoso\\svc-FRAS$ |
| บัญชีบริการกระบวนการการรายงานทางการเงิน             | gMSA           |         | Contoso\\svc-FRPS$ |
| บัญชีบริการการรายงานทางการเงินแบบคลิกตัวออกแบบหนึ่งครั้ง | gMSA           |         | Contoso\\svc-FRCO$ |
| บัญชีบริการ AOS                                     | gMSA           | ควรสร้างผู้ใช้นี้สำหรับการตรวจทานในอนาคต เราวางแผนจะเปิดใช้งาน AOS เพื่อทำงานกับ gMSA ในการออกใช้ผลิตภัณฑ์ที่กำลังจะมาถึง การสร้างผู้ใช้นี้ในขณะที่ทำการตั้งค่า จะช่วยรับประกันความต่อเนื่องในการเปลี่ยนไปยัง gMSA | Contoso\\svc-AXSF$ |
| บัญชีบริการ AOS                                     | บัญชีโดเมน | AOS ใช้ผู้ใช้นี้ในการวางจำหน่ายทั่วไป | Contoso\\AXServiceUser |
| DB ผู้ใช้ที่เป็นผู้ดูแลระบบของ AOS SQL                                   | ผู้ใช้ SQL       | Finance and Operations ใช้ผู้ใช้นี้ในการรับรองความถูกต้องกับ SQL\* นอกจากนี้ ผู้ใช้นี้จะถูกแทนที่โดยผู้ใช้ gMSA ในการออกใช้ผลิตภัณฑ์ที่กำลังจะมาถึง | AXDBAdmin |
| บัญชีบริการตัวแทนการปรับใช้ในพื้นที่                  | gMSA           | บัญชีนี้ใช้โดยตัวแทนในพื้นที่เพื่อประสานการปรับใช้บนโหนดต่างๆ | Contoso\\Svc-LocalAgent$ |

\* ชื่อผู้ใช้และรหัสผ่าน SQL สำหรับการรับรองความถูกต้อง SQL มีความปลอดภัย เนื่องจากจะถูกเข้ารหัสและจัดเก็บไว้ในการใช้ไฟล์ร่วมกัน

### <a name="create-dns-zones-and-add-a-records"></a>สร้างโซน DNS และเพิ่มเรกคอร์ด A

ระบบจะรวม DNS เข้ากับ AD DS และช่วยคุณในการจัดระเบียบ จัดการและค้นหาทรัพยากรในเครือข่าย สร้างโซน Forward Lookup Zone สำหรับ DNS สำหรับชื่อโฮสต์ AOS และคลัสเตอร์ Service Fabric ในการตั้งค่าตัวอย่างนี้ ชื่อโซน DNS คือ d365ffo.onprem.contoso.com และเรกคอร์ด A/ชื่อโฮสต์ จะเป็นดังนี้:

- **ax**.d365ffo.onprem.contoso.com สำหรับเครื่อง AOS
- **sf**.d365ffo.onprem.contoso.com สำหรับคลัสเตอร์ Service Fabric

#### <a name="add-a-dns-zone"></a>เพิ่มโซน DNS

ใช้ขั้นตอนต่อไปนี้เพื่อเพิ่มโซน DNS

1. ลงชื่อเข้าใช้ไปยังเครื่องตัวควบคุมโดเมน คลิก **เริ่มต้น** และเริ่มต้นโปรแกรมจัดการ DNS โดยพิมพ์ **dnsmgmt.msc**
2. คลิกขวาที่ชื่อตัวควบคุมโดเมน แล้วคลิก **โซนใหม่** \> **ถัดไป**
3. เลือก **โซนหลัก**
4. เลือกกล่องกาเครื่องหมาย **จัดเก็บโซนใน Active Directory (พร้อมใช้งานเฉพาะเมื่อเซิร์ฟเวอร์ DNS เป็นตัวควบคุมโดเมนแบบเขียนได้** ทิ้งเอาไว้ และจากนั้น คลิก **ถัดไป**
5. เลือก **ไปยังเซิร์ฟเวอร์ DNS ทั้งหมดที่ทำงานบนตัวควบคุมโดเมนในโดเมนนี้: Contoso.com** แล้ว คลิก **ถัดไป**
6. เลือก **Forward Lookup Zone** แล้ว คลิก **ถัดไป**
7. ป้อนชื่อโซนสำหรับการตั้งค่าของคุณ แล้วคลิก **ถัดไป** ยกตัวอย่างเช่น ป้อน **d365ffo.onprem.contoso.com**
8. เลือก **ไม่อนุญาตให้มีกาอัพเดตแบบไดนามิก** แล้วคลิก **ถัดไป**

#### <a name="set-up-an-a-record-for-aos"></a>ตั้งค่าเรกคอร์ด A สำหรับ AOS

ในโซน DNS ใหม่ สร้างเรกคอร์ด A โดยใช้ชื่อ **ax.d365ffo.onprem.contoso.com** สำหรับ **แต่ละ** โหนคลัสเตอร์ Service Fabric ของชนิด **AOSNodeType** อย่าสร้างเรกคอร์ด A สำหรับชนิดโหนดอื่น

1. คลิกขวาที่โซนใหม่ และจากนั้นคลิก **โฮสต์ใหม่**
2. ป้อนชื่อและที่อยู่ IP ของโหนด Service Fabric (เช่น 10.179.108.12) จากนั้น คลิก **เพิ่มโฮสต์**

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>ตั้งค่าเรกคอร์ด A สำหรับ Orchestrator

ในโซน DNS ใหม่ สร้างเรกคอร์ด A โดยใช้ชื่อ **sf.d365ffo.onprem.contoso.com** สำหรับ **แต่ละ** โหนคลัสเตอร์ Service Fabric ของชนิด **OrchestratorType** อย่าสร้างเรกคอร์ด A สำหรับชนิดโหนดอื่น

1. คลิกขวาที่โซนใหม่ และจากนั้นคลิก **โฮสต์ใหม่**
2. ป้อนชื่อและที่อยู่ IP ของโหนด Service Fabric (เช่น 10.179.108.15) จากนั้น คลิก **เพิ่มโฮสต์**

#### <a name="join-vms-to-the-domain"></a>รวม VM เข้ากับโดเมน

รวมแต่ละ VM เข้ากับโดเมน โดยดำเนินการตามขั้นตอนใน [วิธีการรวม Windows Server 2016 กับโดเมน Active Directory](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html) อีกทางหนึ่งคือ ใช้สคริปต์ของ Windows PowerShell

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
หลังจากที่รวม VM เข้ากับโดเมนแล้ว ให้เพิ่มบัญชีบริการ AOS ($ Contoso\svc AXSF, Contoso\svc AXSF$) ไปยังกลุ่มผู้ดูแลระบบเฉพาะที่ คุณสามารถตรวจสอบบทความ [เพิ่มสมาชิกเข้าในกลุ่มเฉพาะที่](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) เพื่อศึกษาวิธีการทำงาน

#### <a name="disable-user-access-control"></a>ปิดใช้งานการควบคุมการเข้าถึงของผู้ใช้ 

ดำเนินการสคริปต์ต่อไปนี้เพื่อปิดใช้งานการควบคุมการเข้าถึงของผู้ใช้ใน **ทุก** โหน Service Fabric
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> คุณต้องรีบูตโหนดหลังจากสคริปต์เสร็จสิ้นเรียบร้อยแล้ว

#### <a name="add-prerequisite-software-to-vms"></a>เพิ่มข้อกำหนดเบื้องต้นของซอฟต์แวร์ใน VM

ตารางต่อไปนี้แสดงรายการข้อกำหนดเบื้องต้นของซอฟต์แวร์ที่ต้องใช้กับเครื่องในแต่ละชนิดของโหนด

> [!NOTE]
> คุณต้องเริ่มต้นคอมพิวเตอร์ของคุณใหม่หลังจากที่ติดตั้งส่วนประกอบแล้ว

| ชนิดโหนด | ส่วนประกอบ | คำสั่ง |
|-----------|-----------|---------|
| AOS       | SNAC – โปรแกรมควบคุม ODBC | ดู [โปรแกรมควบคุม Microsoft ODBC 13.1 สำหรับ SQL Server - Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339) |
| AOS       | Microsoft .NET Framework เวอร์ชัน 2.0 – 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework เวอร์ชัน 4.0 – 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | บริการข้อมูลทางอินเทอร์เน็ต (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual C ++ แพ็คเกจแบบแจกจ่ายต่อได้สำหรับ Microsoft Visual Studio 2013 | ดู [Microsoft Visual C++ แพ็คเกจแบบแจกจ่ายต่อได้สำหรับ Microsoft Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560) |
| AOS       | Microsoft Access Database Engine 2010 แบบแจกจ่ายต่อได้ | ดู [Microsoft Access Database Engine 2010 แบบแจกจ่ายต่อได้](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | .NET Framework เวอร์ชัน 2.0 – 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework เวอร์ชัน 4.0 – 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Server Reporting Services 2016 ในโหมด **ดั้งเดิม** | |
| MR        | .NET Framework เวอร์ชัน 2.0 – 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework เวอร์ชัน 4.0 – 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual C++ แพ็คเกจแบบแจกจ่ายต่อได้สำหรับ Visual Studio 2013 | ดู [Microsoft Visual C++ แพ็คเกจแบบแจกจ่ายต่อได้สำหรับ Microsoft Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560) |

#### <a name="download-setup-scripts-from-lcs"></a>ดาวน์โหลดสคริปต์การตั้งค่าจาก LCS

เรามีสคริปต์จำนวนมากสำหรับช่วยปรับปรุงประสบการณ์การตั้งค่า ทำตามขั้นตอนเหล่านี้เพื่อดาวน์โหลดสคริปต์การตั้งค่าจาก LCS

1. ลงชื่อเข้าใช้ใน LCS (<https://lcs.dynamics.com/v2>)
2. บนแดชบอร์ด คลิกที่ไทล์ **ไลบรารีแอสเซทที่ใช้ร่วมกัน**
3. คลิกแท็บ **แบบจำลอง**
4. ในกริด เลือกแถว **ไลบรารีแอสเซทที่ใช้ร่วมกัน - สคริปต์สำหรับการปรับใช้ในองค์กร**
5. คลิก **เวอร์ชัน** และดาวน์โหลดสคริปต์เวอร์ชันล่าสุด

### <a name="describe-your-configuration"></a>อธิบายการตั้งค่าคอนฟิกของคุณ

ส่วนนี้แสดงข้อมูลเกี่ยวกับสคริปต์ที่คุณต้องรัน สคริปต์มีการอธิบายไว้ในในลำดับที่ที่คุณต้องรัน ในการรันสคริปต์ ให้กรอกข้อมูลในไฟล์เท็มเพลตที่ $(downloadPath)\\ConfigTemplate.xml ไฟล์ ConfigTemplate.xml อธิบายคลัสเตอร์ Service Fabric, ใบรับรองที่ใช้ในการตั้งค่าคอนฟิก และบัญชีที่ต้องได้รับอนุญาตให้เข้าถึงใบรับรองที่เกี่ยวข้อง ในตัวอย่างที่ให้ มีการป้อนค่าสำหรับโครงสร้างพื้นฐานตัวอย่างตามที่อธิบายไว้ในหัวข้อนี้ ไฟล์เท็มเพลตจะนำมาใช้ในส่วนถัดไป

#### <a name="create-the-domain-account-for-a-service-user"></a>สร้างบัญชีโดเมนสำหรับผู้ใช้การบริการ

รันคำสั่งต่อไปนี้เพื่อสร้างบัญชีโดเมนผู้ใช้ contoso\\AXServiceUser

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>สร้าง gMSAs

1. เปลี่ยนไดเรกทอรีเป็น **$(DownloadPath)** และรันคำสั่ง Windows PowerShell ต่อไปนี้

    > [!NOTE]
    > สคริปต์นี้จะไม่สร้างผู้ใช้ แต่จะพิมพ์คำสั่งที่จะสั่งรันด้วยตนเองบนเครื่องตัวควบคุมโดเมน

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. คัดลอกผลลัพธ์ของคำสั่งลงในหน้าต่าง Windows PowerShell ตรวจสอบให้แน่ใจว่าลบตัวแบ่งบรรทัดออกแล้ว และรันรายการบนเครื่องตัวควบคุมโดเมน Active Directory โดยขยายสิทธิผู้ดูแล (คลิกขวาและคลิก **รันในฐานะผู้ดูแลระบบ**)
3. รันสคริปต์ต่อไปนี้บนเครื่องตัวควบคุมโดเมน Active Directory เพื่อการตรวจสอบความถูกต้องว่ามีการสร้างบัญเรียบร้อยแล้ว ตรวจสอบให้แน่ใจว่า คุณรันสคริปต์หลังจากแทนรูปแบบที่ตรงกับข้อกำหนดการตั้งชื่อของบัญชีบริการแล้ว

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. รันสคริป Export-AddGMSAsONVMScript.ps1 บนเครื่องไคลเอนต์ สคริปต์นี้สร้างสคริปต์ที่จะรันบน VM Service Fabric แต่ละหน่วย และเพิ่มสคริปต์เหล่านี้ในโฟลเดอร์ที่ตรงกับแต่ละชื่อ VM

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>หยุด IIS

ใช้ Remote Desktop Protocol (RDP) เพื่อเชื่อมต่อกับแต่ละ VM Service Fabric และทำขั้นตอนที่ต้องดำเนินการด้วยตนเองให้เสร็จสมบูรณ์ [เริ่มต้นหรือหยุดเว็บเซิร์ฟเวอร์ (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx) อีกทางหนึ่งคือ ใช้สคริปต์ Windows PowerShell ต่อไปนี้ โดยใช้ RDP เพื่อเชื่อมต่อกับแต่ละ VM Service Fabric

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_ควรติดตั้งคุณลักษณะ IIS แต่ปิดใช้งานเนื่องจากมีการขึ้นต่อกันบางอย่างกับ IIS dll ในผลิตภัณฑ์_

### <a name="install-certificates"></a>ติดตั้งใบรับรอง

1. ถ้าคุณได้รับใบรับรองที่แสดงรายการเอาไว้ก่อนหน้าในหัวข้อนี้จาก CA ถูกต้อง ให้กรอกข้อมูลในชื่อไฟล์.pfx และรหัสประจำตัวสำหรับใบรับรองในไฟล์ ConfigTemplate.xml ตั้งค่าแอททริบิวต์ **generateSelfSignedCert** เป็น **เท็จ** และแอททริบิวต์ **สามารถส่งออก** เป็น **เท็จ** คัดลอกไฟล์.pfx ไปที่โฟลเดอร์ใบรับรอง $(DownloadPath)\\InfrastructureScripts\\
2. ถ้าคุณกำลังใช้ใบรับรองที่ลงชื่อด้วยตนเอง (เพื่อวัตถุประสงค์ในการทดสอบเท่านั้น) ให้รันสคริปต์ต่อไปนี้ ในการสร้างใบรับรองที่ลงชื่อด้วยตนเอง ในไฟล์ ConfigTemplate.xml ให้ตรวจสอบให้แน่ใจว่ามีการตั้งค่า **generateSelfSignedCert** เป็น **จริง** และ **สามารถส่งออก** เป็น **จริง** สคริปต์จะอัพเดต XML โดยใช้รหัสประจำตัวสำหรับใบรับรอง

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. ส่งออกใบรับรองใหม่โดยใช้คีย์ส่วนตัว (ไฟล์.pfx) ใช้สคริปต์ต่อไปนี้เพื่อสร้างและรันคำสั่งการส่งออกใน Windows PowerShell ไฟล์.pfx จะถูกใส่ไว้ในโฟลเดอร์ใบรับรอง

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > ต้องทำการติดตั้งใบรับรอง และต้องมีใบรับรองใน:\\CurrentUser\\ของฉัน ใบรับรองต้องสามารถส่งออกได้เช่นกัน

    ถ้าคุณใช้ใบรับรองที่ลงชื่อเอง ให้ข้ามไปยังส่วนถัดไป คุณไม่จำเป็นต้องทำกระบวนงานนี้ให้เสร็จสมบูรณ์

4. หลังจากที่คุณส่งออกหรือคัดลอกไฟล์.pfx ไปยังโฟลเดอร์ใบรับรอง $(DownloadPath)\\InfrastructureScripts\\แล้ว ให้รันคำสั่งต่อไปนี้เพื่อสร้างสคริปต์ที่จะนำไปใส่ในโฟลเดอร์ที่ตรงกับ VM

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. คัดลอกสคริปต์ในแต่ละโฟลเดอร์ไปยัง VM ที่ตรงกับชื่อโฟลเดอร์
6. ในแต่ละ VM รันสคริปต์ต่อไปนี้ตามลำดับที่สคริปต์ปรากฏ

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>ตั้งค่าคลัสเตอร์ Service Fabric แบบสแตนด์อโลน

1. รันคำสั่งต่อไปนี้เพื่อสร้างไฟล์ ClusterConfig.json

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    สำหรับข้อมูลเพิ่มเติม ดู [ขั้นตอน 1B: สร้างคลัสเตอร์หลายเครื่อง](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [รักษาความปลอดภัยในคลัสเตอร์แบบสแตนด์อโลนบน Windows โดยใช้ใบรับรอง X.509](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) และ [สร้างคลัสเตอร์สแตนด์อโลนที่รันบน Windows Server](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)

2. ดาวน์โหลด [แพคเกจการติดตั้ง Service Fabric แบบสแตนด์อโลน](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) ไปยังหนึ่งในโหนด Service Fabric ของคุณ หลังจากดาวน์โหลดไฟล์ Zip แล้ว ให้ปลดบล็อคโดยคลิกขวาที่ไฟล์ Zip แล้ว คลิก **คุณสมบัติ** ในกล่องโต้ตอบ เลือกกล่องกาเครื่องหมาย **ปลดบล็อค** ทางด้านขวาล่าง
3. คัดลอกไฟล์ Zip ไปยังหนึ่งในโหนดคลัสเตอร์ Service Fabric และ Unzip ไฟล์
4. รันคำสั่งต่อไปนี้เพื่อสร้างกฎไฟร์วอลล์ขาเข้าบนพอร์ต 443 และ 445 ในโหนดทั้งหมด

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. รันคำสั่งต่อไปนี้เพื่อสร้างกฎไฟร์วอลล์ขาเข้าบนพอร์ต 80 สำหรับโหนด SSRS เท่านั้น

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. คัดลอกไฟล์ ClusterConfig.json ของคุณไปยังบริเวณที่คุณ Unzip และติดตั้ง Service Fabric แบบสแตนด์อโลน
7. นำทางไปยังบริเวณที่คุณ Unzip และติดตั้งใน Windows PowerShell โดยใช้ขยายสิทธิผู้ดูแล และรันคำสั่งต่อไปนี้เพื่อทดสอบ ClusterConfig

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. ถ้าการทดสอบเสร็จสมบูรณ์ รันคำสั่งต่อไปนี้เพื่อปรับใช้คลัสเตอร์

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. หลังจากสร้างคลัสเตอร์แล้ว ให้เปิดโปรแกรมตรวจดู Service Fabric บนเครื่องไคลเอนต์ใด ๆ เพื่อตรวจสอบความถูกต้องในการติดตั้ง:

    1. ติดตั้งใบรับรองไคลเอนต์ Service Fabric ใน CurrentUser\\ของฉัน ถ้ายังไม่ได้ทำการติดตั้ง
    2. ไปที่ **ตั้งค่า IE** \> **โหมดความเข้ากันได้** และล้างกล่องกาเครื่องหมาย **แสดงผลเว็บไซต์อินทราเน็ตในโหมดความเข้ากันได้**
    3. ไปที่ `https://sf.d365ffo.onprem.contoso.com:19080` ซึ่งมีชื่อโฮสต์ของคลัสเตอร์ Service Fabric ตามที่ระบุในโซนเป็น sf.d365ffo.onprem.contoso.com ถ้าไม่มีการตั้งค่าคอนฟิกการทำให้เครื่องรู้จักชื่อ DNS ให้ใช้ที่อยู่ IP ของเครื่อง
    4. เลือกใบรับรองไคลเอนต์ หน้า **โปรแกรมตรวจดู Service Fabric** จะปรากฏขึ้น

### <a name="configure-lcs-connectivity-for-the-tenant"></a>ตั้งค่าคอนฟิกการเชื่อมต่อ LCS สำหรับผู้เช่า

การปรับใช้และการให้บริการของ Finance and Operations จะประสานกันผ่าน LCS โดยใช้ตัวแทนในพื้นที่ภายในองค์กร หากต้องการสร้างการเชื่อมต่อจาก LCS ไปยังผู้เช่า Finance and Operations คุณต้องตั้งค่าคอนฟิกใบรับรองที่ช่วยให้ตัวแทนในพื้นที่สามารถดำเนินการในนามของผู้เช่า Azure AD ของคุณได้ (ตัวอย่างเช่น Contoso.Onmicrosoft.com)

ใช้ใบรับรองตัวแทนตัวแทนในพื้นที่ที่คุณได้รับจาก CA หรือใบรับรองที่ลงชื่อด้วยตนเองที่คุณสร้างขึ้นโดยใช้สคริปต์

เฉพาะบัญชีผู้ใช้ที่มีบทบาทไดเรกทอรีเป็น Global Administrator จึงจะสามารถเพิ่มใบรับรองในการอนุมัติ LCS โดยค่าเริ่มต้น บุคคลที่ลงทะเบียนสำหรับ Microsoft Office 365 สำหรับองค์กรของคุณ จะเป็น Global Administrator สำหรับไดเรกทอรี

> [!NOTE]
> คุณต้องตั้งค่าคอนฟิกใบรับรองเพียงหนึ่งครั้งสำหรับแต่ละผู้เช่าเท่านั้น สภาพแวดล้อมในองค์กรทั้งหมดสามารถใช้ใบรับรองเดียวกันในการเชื่อมต่อกับ LCS

1. ดาวน์โหลดและติดตั้ง Azure PowerShell เวอร์ชันล่าสุดบนเครื่องไคลเอนต์ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ติดตั้งและตั้งค่าคอนฟิก Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0)
2. ลงชื่อเข้าใช้ใน [พอร์ทัล Azure ของลูกค้า](https://portal.azure.com) เพื่อตรวจสอบว่าคุณมีบทบาทไดเรกทอรีเป็น Global Administrator
3. รันสคริปต์ต่อไปนี้จาก $(DownloadPath)\\InfrastructureScripts

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>ตั้งค่าหน่วยจัดเก็บไฟล์

คุณต้องตั้งค่าการใช้ไฟล์ SMB 3.0 พร้อมใช้งานสูงร่วมกันสองไฟล์ ดูข้อมูลเกี่ยวกับวิธีการเปิดใช้งาน SMB 3.0 ได้ที่[การปรับปรุงความปลอดภัย SMB](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1)
การเจรจาต่อรองด้วยภาษาพื้นเมืองอย่างปลอดภัยไม่สามารถตรวจสอบหรือป้องกันการลดระดับจาก SMB 2.0 หรือ 3.0 เป็น SMB 1.0 ได้ ด้วยเหตุนี้และการใช้ประโยชน์จากความสามารถที่สมบูรณ์ของการเข้ารหัส SMB เราขอแนะนำเป็นอย่างยิ่งให้คุณปิดใช้งานเซิร์ฟเวอร์ SMB 1.0

> [!NOTE]
> เพื่อช่วยในการรับประกันว่าข้อมูลของคุณจะได้รับการปกป้องขณะที่อยู่ในสภาพแวดล้อมของคุณ คุณต้องเปิดใช้งานการเข้ารหัส BitLocker Drive Encryption ในทุกเครื่อง สำหรับข้อมูลเกี่ยวกับวิธีการเปิดใช้งาน BitLocker ดูที่ [BitLocker: วิธีการปรับใช้บน Windows Server 2012 และรุ่นใหม่กว่า](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server)

- การใช้ไฟล์ร่วมกันที่จัดเก็บเอกสารผู้ใช้ที่อัพโหลดไปยัง AOS (ยกตัวอย่างเช่น \\\\DAX7SQLAOFILE1\\aos-การจัดเก็บ)
- การใช้ไฟล์ร่วมกันซึ่งจัดเก็บไฟล์รุ่นล่าสุดและไฟล์การตั้งค่าคอนฟิกเพื่อประสานการปรับใช้ (ยกตัวอย่างเช่น \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > พยายามให้พาธการใช้ไฟล์ร่วมกันนี้มีความยาวสั้นที่สุด เพื่อหลีกเลี่ยงไม่ให้เกินความยาวพาธสูงสุดบนไฟล์ที่จะวางการใช้ไฟล์ร่วมกัน

1. บนเครื่องการใช้ไฟล์ร่วมกัน ให้รันคำสั่งต่อไปนี้

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>ตั้งค่า \\\\DAX7SQLAOFILE1\\aos-การจัดเก็บการใช้ไฟล์ร่วมกัน

2. ใน Server Manager เลือก **บริการไฟล์และการจัดเก็บ** \> **ที่ใช้ร่วมกัน**
3. คลิก **งาน** \> **ที่ใช้ร่วมกันใหม่** เพื่อสร้างการใช้ร่วมกันใหม่โดยใช้ชื่อ **aos-การจัดเก็บ**
4. อนุญาต **การปรับเปลี่ยน** สิทธิ์สำหรับแต่ละเครื่องในคลัสเตอร์ Service Fabric ยกเว้น **OrchestratorNodeType**
5. อนุญาต **การปรับเปลี่ยน** สิทธิ์สำหรับผู้ใช้โดเมนผู้ใช้ AOS (contoso\\AXServiceUser) และผู้ใช้ gMSA (contoso\\svc-AXSF)

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>ตั้งค่า \\\\DAX7SQLAOFILE1\\ตัวแทนการใช้ไฟล์ร่วมกัน

6. กลับไปที่ Server Manager เลือก **บริการไฟล์และการจัดเก็บ** \> **ที่ใช้ร่วมกัน**
7. คลิก **งาน** \> **ที่ใช้ร่วมกันใหม่** เพื่อสร้างการใช้ร่วมกันใหม่โดยใช้ชื่อ **ตัวแทน**
8. อนุญาตสิทธิ์ **การควบคุมทั้งหมด** ให้กับผู้ใช้ gMSA สำหรับตัวแทนการปรับใช้ในพื้นที่ (contoso\\svc-LocalAgent$)

### <a name="set-up-sql-server"></a>ตั้งค่า SQL Server

1. ติดตั้ง SQL Server 2016 SP1 ที่มีความพร้อมใช้งานสูง โดยเป็นคลัสเตอร์ SQL ที่รวม Storage Area Network (SAN) หรือในการตั้งค่าคอนฟิก Always-On  ตรวจสอบว่ามีการติดตั้ง **Database Engine, Reporting Services, การค้นหาข้อความแบบเต็ม** และ **เครื่องมือการจัดการ**
> [!NOTE]
> โปรดตรวจสอบว่ามีการตั้งค่า SQL Always On ตาม [หน้าเลือกการซิงโครไนส์ข้อมูลเริ่มต้น (วิซาร์ดกลุ่มความพร้อมใช้งานแบบ Always On)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) และตาม [การเตรียมฐานข้อมูลรองด้วยตนเอง](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. รันบริการ SQL ในฐานะผู้ใช้โดเมน
3. จัดหาใบรับรอง SSL จาก CA เพื่อตั้งค่าคอนฟิก Finance and Operations เพื่อวัตถุประสงค์ในการทดสอบ คุณสามารถสร้างและใช้งานใบรับรองที่ลงชื่อด้วยตนเอง

**ใบรับรองที่ลงชื่อด้วยตนเองสำหรับอินสแตนซ์ SQL แบบคลัสเตอร์**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**ใบรับรองที่ลงชื่อด้วยตนเองสำหรับอินสแตนซ์ SQL แบบ Always-On**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. โดยใช้ใบรับรอง ให้ทำขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ [วิธีการเปิดใช้งานการเข้ารหัส SSL สำหรับอินสแตนซ์ของ SQL Server โดยใช้ Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) เพื่อตั้งค่าคอนฟิก SSL บน SQL Server
5. สำหรับแต่ละโหนดของคลัสเตอร์ ให้ทำตามขั้นตอนต่อไปนี้ ตรวจสอบให้แน่ใจว่า คุณทำการเปลี่ยนแปลงบนโหนดที่ไม่ได้ใช้งานอยู่ และตั้งค่า Failover กลับไปหลังจากที่ทำการเปลี่ยนแปลงแล้ว

    1. นำเข้าใบรับรองใน LocalMachine\\ของฉัน
    2. อนุญาตสิทธิ์ใบรับรองให้กับบัญชีบริการที่ใช้ในการรันบริการ SQL ใน Microsoft Management Console (MMC) คลิกขวาที่ใบรับรอง (certlm.msc) แล้วคลิก **งาน** \> **จัดการคีย์ส่วนตัว**
    3. เพิ่มรหัสประจำตัวใบรับรองไปที่ HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\ใบรับรอง
    4. ใน Microsoft SQL Server Configuration Manager ตั้งค่า **ForceEncryption** เป็น **ใช่**

6. ส่งออกคีย์สาธารณะของใบรับรอง (ไฟล์.cer) และติดตั้งในจุดที่เชื่อถือได้ของแต่ละโหนด Service Fabric

### <a name="configure-the-orchestratordata-database"></a>การตั้งค่าคอนฟิกฐานข้อมูล OrchestratorData

1.  สร้างฐานข้อมูลว่างเปล่า และตั้งชื่อเป็น **OrchestratorData** ตัวแทนในพื้นที่ภายในองค์กรจะใช้ฐานข้อมูลนี้เพื่อประสานการปรับใช้
2.  อนุญาตตัวแทนการปรับใช้ gMSA ในพื้นที่ (svc-LocalAgent$) **db\_เจ้าของ** สิทธิ์บนฐานข้อมูล:

    1. ในแผนภูมิ ขยายชื่อเซิร์ฟเวอร์ ขยาย **ความปลอดภัย** \> **ล็อกอิน** แล้วคลิกขวา และคลิก **ล็อกอินใหม่**

        ![คำสั่งล็อกอินใหม่](./media/OPSetup_01_NewLogin.png)


    2. ค้นหาบัญชีบริการ **svc-LocalAgent$** คลิก **สถาน** และเลือก **ทั้งไดเรกทอรี** แล้วคลิก **ชนิดออบเจ็กต์** และเลือก **บัญชีบริการ**

        ![เลือกผู้ใช้ บัญชีบริการหรือกล่องโต้ตอบแบบกลุ่ม](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. ตั้งค่า **Assign ServerRole** เป็น **สาธารณะ**
    4. กำหนด **db\_เจ้าของ** สิทธิ์บทบาทในฐานข้อมูลเป็นฐานข้อมูล OrchestratorData

### <a name="configure-the-finance-and-operations-database"></a>ตั้งค่าคอนฟิกฐานข้อมูล Finance and Operations

1. ลงชื่อเข้าใช้ใน LCS (<https://lcs.dynamics.com/v2>)
2. บนแดชบอร์ด คลิกที่ไทล์ **ไลบรารีแอสเซทที่ใช้ร่วมกัน**
3. คลิกแท็บ **แบบจำลอง** 
4. ในกริด คลิกแถว **Dynamics 365 for Operations on-premises, Enterprise edition - ข้อมูลสาธิต** เพื่อดาวน์โหลด Zip
5. ใน Zip จะมีข้อมูลว่างเปล่าและไฟล์ demo data .bak เลือกไฟล์.bak ที่เหมาะสม ตามความต้องการของคุณ ยกตัวอย่างเช่น ถ้าต้องการข้อมูลสาธิต ให้คืนค่าไฟล์ AxBootstrapDB_Demodata.bak 
6. คืนค่าฐานข้อมูล AxBootstrapDB_DemoData.bak
7. เปลี่ยนชื่อฐานข้อมูล **AXDBRAIN**
8. รันการสอบถามต่อไปนี้บนฐานข้อมูลที่มีการคืนค่า

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. อัพเดตไฟล์ฐานข้อมูล:

    1. คลิกขวาที่ฐานข้อมูล แล้วคลิก **คุณสมบัติ**
    2. คลิก **ไฟล์** เพื่อเปลี่ยนแปลงคุณสมบัติของไฟล์ฐานข้อมูล
    3. ในฟิลด์ **ขนาดเริ่มต้น (MB)** ป้อนค่าที่มากกว่า 5,120

        ![กล่องโต้ตอบคุณสมบัติฐานข้อมูล](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. สำหรับ **AXDBBuild\_ข้อมูล** ตั้งค่าฟิลด์ **Autogrowth/Maximize** เป็น **200** เมกะไบต์ (MB)
    5. สำหรับ **AXDBBuild\_ล็อก** ตั้งค่าฟิลด์ **Autogrowth/Maximize** เป็น **500** เมกะไบต์ (MB)

        ![เปลี่ยนกล่องโต้ตอบ Autogrowth](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. สร้างผู้ใช้ใหม่ที่มีการเปิดใช้งาน การรับรองความถูกต้อง SQL (axdbadmin)
6. ใช้ข้อมูลในตารางต่อไปนี้ในการแม็ปผู้ใช้และบทบาทฐานข้อมูล

    | ผู้ใช้             | ชนิดข้อมูล    | บทบาทฐานข้อมูล |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_เจ้าของ     |
    | svc-LocalAgent$  | gMSA    | db\_เจ้าของ     |
    | svc-FRPS$        | gMSA    | db\_เจ้าของ     |
    | svc-FRAS$        | gMSA    | db\_เจ้าของ     |
    | axdbadmin        | SqlUser | db\_เจ้าของ     |

7. ให้สิทธิการเข้าถึงแก่ผู้ใช้ svc-AXSF$ และผู้ใช้ SQL axdbadmin สำหรับบทบาทต่อไปนี้ในฐานข้อมูล tempdb:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. ใน Management Studio รันคำสั่ง Transact SQL (T SQL) ต่อไปนี้:

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. โดยรันคำสั่งต่อไปนี้:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>ตั้งค่าคอนฟิกฐานข้อมูล Financial Reporting

1.  สร้างฐานข้อมูลว่างเปล่า และตั้งชื่อเป็น **FinancialReporting**
2.  ใช้ข้อมูลในตารางต่อไปนี้ในการแม็ปผู้ใช้และบทบาทฐานข้อมูล

    | ผู้ใช้             | ชนิดข้อมูล | บทบาทฐานข้อมูล |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_เจ้าของ     |
    | svc-FRPS$        | gMSA | db\_เจ้าของ     |
    | svc-FRAS$        | gMSA | db\_เจ้าของ     |

### <a name="encrypt-credentials"></a>เข้ารหัสข้อมูลประจำตัว

1. บนเครื่องไคลเอนต์ใด ๆ ให้ติดตั้งใบรับรองการเข้ารหัสบน LocalMachine\\ที่เก็บใบรับรองของฉัน
2. ให้สิทธิ์การอ่านคีย์ส่วนตัวของใบรับรองนี้แก่ผู้ใช้ปัจจุบัน
3. สร้างไฟล์ Credentials.json ตามที่แสดงไว้ที่นี่

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** เป็นรหัสผ่านผู้ใช้โดเมนที่มีการเข้ารหัสสำหรับผู้ใช้โดเมน AOS (contoso\\axserviceuser)
    - **SqlUser** คือ ผู้ใช้ SQL ที่มีการเข้ารหัส (axdbadmin) ซึ่งมีสิทธิ์เข้าถึงฐานข้อมูล Finance and Operations (AXDBRAIN) และ **SqlPassword** เป็นรหัสผ่าน SQL ที่เข้ารหัส

4. คัดลอกไฟล์.json ไปยังการใช้ไฟล์ SMB ร่วมกัน \\\\AX7SQLAOFILE1\\ตัวแทน\\ข้อมูลประจำตัว\\Credentials.json
5. อัพเดตไฟล์ Credentials.json ด้วยค่าที่มีการเข้ารหัส

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. ใน Credentials.json แทนที่ **\<encryptedDomainUserPassword\>** ด้วยรหัสผ่านโดเมนที่มีการเข้ารหัส
    2. แทนที่ **\<encryptedSqlUser\>** ด้วยผู้ใช้ SQL Finance and Operations ที่มีการเข้ารหัส
    3. แทนที่ **\<encryptedSqlPassword\>** ด้วยรหัสผ่าน SQL Finance and Operations ที่มีการเข้ารหัส
    
### <a name="set-up-ssrs"></a>ตั้งค่า SSRS

1.  ก่อนที่คุณเริ่มต้น ตรวจสอบให้แน่ใจว่า มีการติดตั้งส่วนประกอบตามข้อกำหนดเบื้องต้นที่ระบุไว้ในตอนต้นของหัวข้อนี้
2.  ทำตามขั้นตอนเพื่อ [ตั้งค่าคอนฟิก SQL Server Reporting Services สำหรับการปรับใช้ในองค์กร](../analytics/configure-ssrs-on-premises.md)

### <a name="configure-ad-fs"></a>ตั้งค่าคอนฟิก AD FS

ก่อนที่คุณสามารถทำกระบวนงานนี้ให้เสร็จสมบูรณ์ ต้องปรับใช้ AD FS บน Windows Server 2016 สำหรับข้อมูลเกี่ยวกับวิธีการปรับใช้ AD FS ดูที่ [คำแนะนำการปรับใช้ Windows Server 2016 และคำแนะนำการปรับใช้ 2012 R2 AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide)

ต้องมีการตั้งค่าคอนฟิก Finance and Operations เพิ่มเติม นอกเหนือจากการตั้งค่าคอนฟิกเริ่มต้นนอกกล่องของ AD FS สำหรับขั้นตอนต่อไปนี้ Windows PowerShell รันบนเครื่องที่มีการติดตั้งบริการบทบาท AD FS บัญชีผู้ใช้ต้องมีสิทธิ์เพียงพอในการดูแล AD FS ยกตัวอย่างเช่น ผู้ใช้ต้องมีบัญชีผู้ดูแลโดเมน

1. กำหนดตัวระบุ AD FS ให้ตรงกับผู้ออกโทเค็น AD FS

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. คุณควรปิดใช้งาน Windows Integrated Authentication (WIA) สำหรับการเชื่อมต่อการรับรองความถูกต้องของอินทราเน็ต ยกเว้นว่าคุณได้ตั้งค่าคอนฟิก AD FS สำหรับสภาพแวดล้อมแบบผสม ดูข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิก WIA เพื่อให้สามารถใช้กับ AD FS ได้ที่ [การตั้งค่าคอนฟิกเบราเซอร์เพื่อใช้ Windows Integrated Authentication (WIA) กับ AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia)

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. สำหรับการลงชื่อเข้าใช้ ที่อยู่อีเมลของผู้ใช้ต้องเป็นอินพุตการรับรองความถูกต้องที่ยอมรับได้

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

เพื่อให้ AD FS เชื่อถือ Finance and Operations สำหรับการแลกเปลี่ยนการรับรองความถูกต้อง คุณต้องทำการลงทะเบียนรายการแอพลิเคชันใน FS AD ใต้กลุ่มแอพลิเคชัน AD FS เพื่อเพิ่มความเร็วกระบวนการการตั้งค่าและช่วยลดข้อผิดพลาด คุณสามารถใช้สคริปต์ต่อไปนี้สำหรับการลงทะเบียน คัดลอกสคริปต์ Publish-ADFSApplicationGroup.ps1 และไดเรกทอรี D365FO-OP ไปยังเครื่องที่มีการติดตั้งบริการบทบาท AD FS จากนั้น ให้รันสคริปต์โดยใช้บัญชีผู้ใช้ เช่น บัญชีผู้ดูแลระบบ ที่มีสิทธิ์เพียงพอในการดูแล AD FS สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้สคริปต์ ให้ดูเอกสารตามที่แสดงรายการในสคริปต์ จดบันทึกค่ารหัสไคลเอนต์ที่ระบุไว้ในผลลัพธ์ เนื่องจากจะมีการขอข้อมูลนี้ใน LCS ในขั้นตอนต่อไป

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

คอนโซลการจัดการ AD FS ควรมีลักษณะตามภาพประกอบต่อไปนี้ หากต้องการเปิด Server Manager ให้คลิก **เครื่องมือ** \> **การจัดการ AD FS** แล้วคลิก **กลุ่มแอพลิเคชัน** ที่ด้านล่างซ้ายของมุมมองแผนภูมิ ดับเบิลคลิกกลุ่มแอพลิเคชัน เพื่อดูรายละเอียดเพิ่มเติม

![คุณสมบัติของกลุ่มแอพลิเคชัน](./media/OPSetup_05_ApplicatioGroupProperties.png)

ท้ายสุด เพื่อการตรวจสอบความถูกต้อง ให้ตรวจสอบให้แน่ใจว่าคุณสามารถเข้าถึง URL AD FS OpenID Configuration บนโหนด Service Fabric ของชนิด **AOSNodeType** โดยไปที่ `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` ในเว็บเบราเซอร์ ถ้าคุณได้รับข้อความแจ้งว่า ไซต์ไม่ปลอดภัย แสดงว่าคุณยังไม่ได้เพิ่มใบรับรอง AD FS SSL ของคุณไปยังที่จัดเก็บหน่วยงานที่ออกใบรับรองหลักที่เชื่อถือได้ ขั้นตอนนี้มีอธิบายอยู่ในคู่มือการปรับใช้ AD FS ถ้าคุณสามารถเข้าถึง URL จะมีการส่งคืนไฟล์ JavaScript Object Notation (JSON) ที่มีการตั้งค่าคอนฟิก AD FS ของคุณ และคุณจะเห็นว่า URL AD FS ของคุณได้รับความเชื่อถือ

โดยใช้การตั้งค่านี้ ถือว่าโครงสร้างพื้นฐานเสร็จสมบูรณ์แล้ว ส่วนต่อไปนี้อธิบายวิธีการนำทางไปยัง [LCS](https://lcs.dynamics.com) เพื่อตั้งค่าตัวเชื่อมต่อของคุณและปรับใช้ 365 Dynamics สำหรับสภาพแวดล้อม Finance and Operations

## <a name="configure-connector-and-install-on-premises-local-agent"></a>ตั้งค่าคอนฟิกตัวเชื่อมต่อและติดตัวแทนในพื้นที่ภายในองค์กร

1. ลงชื่อเข้าใช้ใน [LCS](https://lcs.dynamics.com/) และเปิดโครงการปรับใช้ภายในองค์กร
2. บนเมนู hamburger คลิก **การตั้งค่าโครงการ**

    ![คำสั่งการตั้งค่าโครงการ](./media/OPSetup_06_ProjectSettings.png)

3. คลิก **ตัวเชื่อมต่อ On-Premises**
4. คลิก **เพิ่ม** เพื่อสร้างตัวเชื่อมต่อใหม่
5. บนแท็บ **ตั้งค่าโครงสร้างพื้นฐานของโฮสต์** ให้ดาวน์โหลดตัวติดตั้งเอเจนต์

    ![ปุ่มดาวน์โหลดตัวติดตั้งเอเจนต์ บนแท็บตั้งค่าโครงสร้างพื้นฐานของโฮสต์](./media/OPSetup_07_DownloadAgentInstaller.png)

6. ตรวจสอบว่าไฟล์ Zip ไม่ถูกบล็อค คลิกขวาที่ไฟล์ แล้วคลิก **คุณสมบัติ** และเลือก **ยกเลิกการบล็อค**
7. Unzip ตัวติดตั้งเอเจนต์บนหนึ่งในโหนด Service fabric ของชนิด **OrchestratorType**
8. บนแท็บ **ตั้งค่าคอนฟิกเอเจนต์** ป้อนการตั้งค่าของการตั้งค่าคอนฟิก
9. บันทึกการตั้งค่าคอนฟิกและคลิก **ดาวน์โหลดการตั้งค่าคอนฟิก** เพื่อดาวน์โหลดไฟล์การตั้งค่าคอนฟิก localagent config.json

    ![ดาวน์โหลดปุ่มการตั้งค่าคอนฟิกปุ่มบนแท็บตั้งค่าคอนฟิกเอเจนต์](./media/OPSetup_08_DownloadConfigurations.png)

10. คัดลอกไฟล์ localagent-config.json ไปยังเครื่องที่เป็นที่มีแพคเกจตัวติดตั้งเอเจนต์อยู่
11. ในหน้าต่างพร้อมท์คำสั่ง รันคำสั่งต่อไปนี้ โดยนำทางไปยังโฟลเดอร์ที่มีตัวติดตั้งเอเจนต์อยู่

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > ผู้ใช้ที่รันคำสั่งนี้ต้องมีสิทธิ์ **db\_เจ้าของ** บนฐานข้อมูล OrchestratorData
    
12. หลังจากติดตั้งตัวแทนในพื้นที่เสร็จเรียบร้อยแล้ว ให้นำทางกลับไปยังตัวเชื่อมต่อ On-Premises ของคุณใน LCS
13. บนแท็บ **ตรวจสอบความถูกต้องของการตั้งค่า** ให้คลิกปุ่ม **ส่งข้อความถึงตัวแทน** ซึ่งจะทดสอบการเชื่อมต่อ LCS กับตัวแทนในพื้นที่ของคุณ เมื่อสร้างการเชื่อมต่อเรียบร้อยแล้ว หน้าจะมีลักษณะตามรูปภาพด้านล่าง

     ![ตรวจสอบความถูกต้องตัวแทน](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>ปรับใช้สภาพแวดล้อม Dynamics 365 for Finance and Operations (ในองค์กร) ของคุณ

1. นำทางไปยังโครงการสำหรับใช้งานในองค์กรของคุณใน LCS แล้วไปที่ **สภาพแวดล้อม**, **Sandbox** และคลิกที่ **ตั้งค่าคอนฟิก**
2. เลือก **โทโพโลยีของสภาพแวดล้อม** ของคุณและดำเนินการโดยใช้วิซาร์ เพื่อเริ่มต้นการปรับใช้
3. ตัวแทนในพื้นที่จะรับการร้องขอการปรับใช้ ดำเนินการการปรับใช้และสื่อสารกลับมายัง LCS เมื่อพร้อม

