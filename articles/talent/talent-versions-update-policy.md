---
title: ความต้องการของระบบ Talent
description: หัวข้อนี้แสดงความต้องการสำหรับ Dynamics 365 Talent
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0bd7d7051dd01834f306e165af55d740192b99e0
ms.sourcegitcommit: caeb24027831efccbc316ff8e7f9e62b42010d65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/19/2019
ms.locfileid: "2818490"
---
# <a name="talent-system-requirements"></a>ความต้องการของระบบ Talent

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงข้อกำหนดสำหรับ Microsoft Dynamics 365 Talent ซึ่งรวมถึง Attract Onboard และ Core HR นอกจากนี้ ยังกำหนดโครงร่างประเทศและภูมิภาคที่ Talent พร้อมใช้งาน รวมถึงข้อมูลเกี่ยวกับภาษาและการแปลสำหรับข้อมูล Talent นอกจากนี้ หัวข้อนี้จะแสดงนโยบายการอัพเดตสำหรับ Talent

## <a name="supported-web-browsers"></a>เว็บเบราเซอร์ที่สนับสนุน

Microsoft Dynamics 365 Talent สามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ต่อไปนี้ที่ทำงานบนระบบปฏิบัติการที่ระบุ: 

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
> * Dynamics 365 Talent ได้รับการออกแบบมาสำหรับเครือข่ายที่มีเวลาแฝง 250-300 มิลลิวินาที (ms) หรือน้อยกว่า นี่คือเวลาแฝงจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Microsoft Azure ที่โฮสต์ Talent เราขอแนะนำให้คุณทดสอบเวลาแฝงบนเครือข่ายที่ [www.azurespeed.com](https://www.azurespeed.com "การทดสอบเวลาแฝง Azure")
> * ข้อกำหนดของแบนด์วิธสำหรับ Talent ขึ้นอยู่กับสถานการณ์ของคุณ สถานการณ์ทั่วไปส่วนใหญ่จำเป็นต้องมีแบนด์วิดท์ที่มากกว่า 50 กิโลไบต์ต่อวินาที (KBps)
> 
> [!WARNING]
> อย่าคำนวณข้อกำหนดของแบนด์วิดท์จากตำแหน่งที่ตั้งของไคลเอนต์ โดยการคูณจำนวนผู้ใช้กับข้อกำหนดของแบนด์วิดท์ต่ำสุด การใช้งานที่เกิดขึ้นพร้อมกันของตำแหน่งที่ตั้งที่กำหนดเป็นสิ่งที่คำนวณได้ยาก สำหรับลูกค้าที่มีความกังวลเกี่ยวกับข้อกำหนดของแบนด์วิธ ให้ใช้ Talent รุ่นทดลองใช้

## <a name="supported-microsoft-office-applications"></a>แอพลิเคชัน Microsoft Office ที่สนับสนุน

* เมื่อต้องการเรียกใช้ Add-in ของ Microsoft Excel และ Word คุณจะต้องตั้งค่า Microsoft Office 2016 สำหรับ Windows หรือ Mac ไว้ สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับข้อกำหนดเวอร์ชัน ให้ดูที่ [การแก้ไขปัญหาการรวม Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "การแก้ไขปัญหาการรวม Office")
* เมื่อต้องการดูเอกสารที่สร้างขึ้นโดยฟังก์ชันส่งออกไปที่ Excel หรือส่งออกไปที่ Word คุณต้องติดตั้ง Microsoft Office 2007 หรือรุ่นที่ใหม่กว่าไว้

## <a name="regional-availability-languages-and-localization"></a>ความพร้อมใช้งานของภูมิภาค ภาษา และการแปลภาษา

คุณสามารถดาวน์โหลดไฟล์ PDF ของประเทศ ภูมิภาค และภาษา ที่ Talent สนับสนุนที่ [ความพร้อมใช้งานระหว่างประเทศของ Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability) 

> [!NOTE]
> ในขณะที่อินเทอร์เฟสผู้ใช้ถูกแปลเป็นภาษาอื่นๆ ข้อมูลผู้ใช้ทั้งหมดจะถูกจัดเก็บอยู่ในภาษาที่ป้อนไว้ คุณสามารถสร้างอีเมลและเท็มเพลตในภาษาอื่นๆ ได้ แต่ข้อมูล เช่น ข้อมูลการจัดกำหนดการพร้อมใช้งานเฉพาะในภาษาอังกฤษเท่านั้นในขณะนี้

ถ้าคุณเป็นนักพัฒนาที่สนใจในการสร้างการเลือกกำหนดเฉพาะประเทศหรือภูมิภาค หรือในการสร้างโซลูชันสำหรับประเทศหรือภูมิภาคที่ Microsoft ไม่สนับสนุนในขณะนี้ โปรดดู [โลกาภิวัตน์](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region)

