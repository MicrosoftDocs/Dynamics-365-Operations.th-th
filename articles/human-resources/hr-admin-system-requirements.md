---
title: ความต้องการของระบบ
description: บทความนี้อธิบายถึงข้อกำหนดสำหรับ Microsoft Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f68b8f642ada1345e7097b5e7220e222b132b1dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420796"
---
# <a name="system-requirements"></a>ความต้องการของระบบ

บทความนี้อธิบายถึงข้อกำหนดสำหรับ Microsoft Dynamics 365 Human Resources นอกจากนี้ ยังกำหนดโครงร่างประเทศและภูมิภาคที่ทรัพยากรบุคคลพร้อมใช้งาน และข้อมูลเกี่ยวกับภาษาและการแปลสำหรับข้อมูลทรัพยากรบุคคล

## <a name="supported-web-browsers"></a>เว็บเบราเซอร์ที่สนับสนุน

ทรัพยากรบุคคลสามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ต่อไปนี้ที่ทำงานบนระบบปฏิบัติการที่ระบุ: 

*   Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10
*   Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7
*   Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป)
*   Apple Safari (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป)

เมื่อต้องการค้นหารุ่นล่าสุดของแต่ละเว็บเบราเซอร์ ไปที่เว็บไซต์ของผู้ผลิตซอฟต์แวร์ 

> [!NOTE]
> * เมื่อต้องการจับภาพรูปที่สร้างขึ้นจากตัวบันทึกงาน และรวมค่าเหล่านั้นไว้ในเอกสาร Microsoft Word คุณต้องติดตั้งส่วนขยาย Chrome ไว้ 
> * ตัวแก้ไขเวิร์กโฟลว์จะเริ่มต้นการใช้งานเป็นแอพลิเคชัน ClickOnce เฉพาะ Microsoft Edge และ Internet Explorer (บนเวอร์ชันที่สนับสนุน Microsoft Windows) สนับสนุนแอพลิเคชัน ClickOnce แอพลิเคชัน ClickOnce โปรแกรมแก้ไขลำดับงานต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต
> * เมื่อต้องการแสดงตัวอย่างไฟล์ PDF เราขอแนะนำให้คุณใช้เบราว์เซอร์ที่ทันสมัย เช่น Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10 หรือ Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บนแท็บเล็ต Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus 10
>   ข้อกำหนดของเครือข่าย
> * ทรัพยากรบุคคลได้รับการออกแบบมาสำหรับเครือข่ายที่มีเวลาแฝง 250-300 มิลลิวินาที (ms) หรือน้อยกว่า นี่คือเวลาแฝงจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Microsoft Azure ที่โฮสต์ทรัพยากรบุคคล เราขอแนะนำให้คุณทดสอบเวลาแฝงบนเครือข่ายที่ [www.azurespeed.com](https://www.azurespeed.com "การทดสอบเวลาแฝง Azure")
> * ข้อกำหนดของแบนด์วิธสำหรับทรัพยากรบุคคลขึ้นอยู่กับสถานการณ์ของคุณ สถานการณ์ทั่วไปส่วนใหญ่จำเป็นต้องมีแบนด์วิดท์ที่มากกว่า 50 กิโลไบต์ต่อวินาที (KBps)
> 
> [!WARNING]
> อย่าคำนวณข้อกำหนดของแบนด์วิดท์จากตำแหน่งที่ตั้งของไคลเอนต์ โดยการคูณจำนวนผู้ใช้กับข้อกำหนดของแบนด์วิดท์ต่ำสุด การใช้งานที่เกิดขึ้นพร้อมกันของตำแหน่งที่ตั้งที่กำหนดเป็นสิ่งที่คำนวณได้ยาก สำหรับลูกค้าที่มีความกังวลเกี่ยวกับข้อกำหนดของแบนด์วิธ ให้ใช้ทรัพยากรบุคคลรุ่นทดลองใช้

## <a name="supported-microsoft-office-applications"></a>แอพลิเคชัน Microsoft Office ที่สนับสนุน

* เมื่อต้องการเรียกใช้ Add-in ของ Microsoft Excel และ Word คุณจะต้องตั้งค่า Microsoft Office 2016 สำหรับ Windows หรือ Mac ไว้ สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับข้อกำหนดเวอร์ชัน ให้ดูที่ [การแก้ไขปัญหาการรวม Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "การแก้ไขปัญหาการรวม Office")
* เมื่อต้องการดูเอกสารที่สร้างขึ้นโดยฟังก์ชันส่งออกไปที่ Excel หรือส่งออกไปที่ Word คุณต้องติดตั้ง Microsoft Office 2007 หรือรุ่นที่ใหม่กว่าไว้

## <a name="regional-availability-languages-and-localization"></a>ความพร้อมใช้งานของภูมิภาค ภาษา และการแปลภาษา

คุณสามารถดาวน์โหลดไฟล์ PDF ของประเทศ ภูมิภาค และภาษาที่ทรัพยากรบุคคลสนับสนุนที่ [ความพร้อมใช้งานระหว่างประเทศของ Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability) 

> [!NOTE]
> ในขณะที่อินเทอร์เฟสผู้ใช้ถูกแปลเป็นภาษาอื่นๆ ข้อมูลผู้ใช้ทั้งหมดจะถูกจัดเก็บอยู่ในภาษาที่ป้อนไว้ คุณสามารถสร้างอีเมลและเท็มเพลตในภาษาอื่นๆ ได้ แต่ข้อมูล เช่น ข้อมูลการจัดกำหนดการพร้อมใช้งานเฉพาะในภาษาอังกฤษเท่านั้นในขณะนี้

ถ้าคุณเป็นนักพัฒนาที่สนใจในการสร้างการเลือกกำหนดเฉพาะประเทศหรือภูมิภาค หรือในการสร้างโซลูชันสำหรับประเทศหรือภูมิภาคที่ Microsoft ไม่สนับสนุนในขณะนี้ โปรดดู [โลกาภิวัตน์](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region)


[!INCLUDE[footer-include](../includes/footer-banner.md)]