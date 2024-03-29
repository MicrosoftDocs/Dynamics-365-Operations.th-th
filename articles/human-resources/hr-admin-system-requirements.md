---
title: ความต้องการของระบบ
description: บทความนี้แสดงความต้องการของระบบสำหรับ Microsoft Dynamics 365 Human Resources
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b07d14dfe0e6b53c9489c284520a24b97d9887fa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879350"
---
# <a name="system-requirements"></a>ความต้องการของระบบ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้แสดงความต้องการของระบบสำหรับ Microsoft Dynamics 365 Human Resources นอกจากนี้ ยังกำหนดโครงร่างประเทศและภูมิภาคที่ทรัพยากรบุคคลพร้อมใช้งาน และข้อมูลเกี่ยวกับภาษาและการแปลสำหรับข้อมูลทรัพยากรบุคคล

## <a name="supported-web-browsers"></a>เว็บเบราเซอร์ที่สนับสนุน

ผู้ใช้สามารถเข้าถึง Microsoft Dynamics 365 Human Resources โดยใช้ในเว็บเบราเซอร์ใดก็ได้ต่อไปนี้ที่ทำงานบนระบบปฏิบัติการที่ระบุ: 

*   Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10
*   Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7
*   Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป)
*   Apple Safari (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป)

เมื่อต้องการค้นหารุ่นล่าสุดของแต่ละเว็บเบราเซอร์ ไปที่เว็บไซต์ของผู้ผลิตซอฟต์แวร์ 

## <a name="special-considerations"></a>ข้อควรพิจารณาพิเศษ

* หากต้องการเปิดใช้งานตัวบันทึกงานรวบรวมภาพหน้าจอและรวมเข้าไปในเอกสาร Microsoft Word ที่ถูกสร้างขึ้น คุณต้องติดตั้งส่วนขยายของ Chrome รุ่นก่อนวางจำหน่าย
* ตัวแก้ไขเวิร์กโฟลว์จะเริ่มต้นการใช้งานเป็นแอปพลิเคชัน ClickOnce เฉพาะ Microsoft Edge และ Internet Explorer (บนเวอร์ชันที่สนับสนุน Microsoft Windows) สนับสนุนแอปพลิเคชัน ClickOnce แอปพลิเคชัน ClickOnce โปรแกรมแก้ไขลำดับงานต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต
* เมื่อต้องการแสดงตัวอย่างไฟล์ PDF เราขอแนะนำให้คุณใช้เบราว์เซอร์ที่ทันสมัย เช่น Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10 หรือ Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บนแท็บเล็ต Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus 10

## <a name="network-requirements"></a>ข้อกำหนดของเครือข่าย

* ทรัพยากรบุคคลได้รับการออกแบบมาสำหรับเครือข่ายที่มีเวลาแฝง 250-300 มิลลิวินาที (ms) หรือน้อยกว่า นี่คือเวลาแฝงจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Microsoft Azure ที่โฮสต์ทรัพยากรบุคคล เราขอแนะนำให้คุณทดสอบเวลาแฝงบนเครือข่ายที่ [www.azurespeed.com](https://www.azurespeed.com "การทดสอบเวลาแฝง Azure")
* ข้อกำหนดของแบนด์วิธสำหรับทรัพยากรบุคคลขึ้นอยู่กับสถานการณ์ของคุณ สถานการณ์ทั่วไปจำเป็นต้องมีแบนด์วิดท์ที่มากกว่า 50 กิโลไบต์ต่อวินาที (KBps)
 
> [!WARNING]
> อย่าคำนวณข้อกำหนดของแบนด์วิดท์จากตำแหน่งที่ตั้งของไคลเอนต์ โดยการคูณจำนวนผู้ใช้กับข้อกำหนดของแบนด์วิดท์ต่ำสุด การใช้งานที่เกิดขึ้นพร้อมกันของตำแหน่งที่ตั้งที่กำหนดเป็นสิ่งที่คำนวณได้ยาก สำหรับลูกค้าที่มีความกังวลเกี่ยวกับข้อกำหนดของแบนด์วิธ ให้ใช้ทรัพยากรบุคคลรุ่นทดลองใช้

## <a name="supported-microsoft-office-applications"></a>แอปพลิเคชัน Microsoft Office ที่สนับสนุน

* เมื่อต้องการเรียกใช้ Add-in ของ Microsoft Excel และ Word คุณจะต้องตั้งค่า Microsoft Office 2016 สำหรับ Windows หรือ Mac ไว้ สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับข้อกำหนดเวอร์ชัน ให้ดูที่ [การแก้ไขปัญหาการรวม Office](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "การแก้ไขปัญหาการรวม Office")
* เมื่อต้องการดูเอกสารที่สร้างขึ้นโดยฟังก์ชันส่งออกไปที่ Excel หรือส่งออกไปที่ Word คุณต้องติดตั้ง Microsoft Office 2007 หรือรุ่นที่ใหม่กว่าไว้

## <a name="regional-availability-languages-and-localization"></a>ความพร้อมใช้งานของภูมิภาค ภาษา และการแปลภาษา

คุณสามารถดาวน์โหลดไฟล์ PDF ของประเทศ ภูมิภาค และภาษาที่ทรัพยากรบุคคลสนับสนุนที่ [ความพร้อมใช้งานระหว่างประเทศของ Microsoft Dynamics 365](/dynamics365/get-started/availability) 

> [!NOTE]
> ในขณะที่อินเทอร์เฟสผู้ใช้ถูกแปลเป็นภาษาอื่นๆ ข้อมูลผู้ใช้ทั้งหมดจะถูกจัดเก็บอยู่ในภาษาที่ป้อนไว้ คุณสามารถสร้างอีเมลและเท็มเพลตในภาษาอื่นๆ ได้ แต่ข้อมูล เช่น ข้อมูลการจัดกำหนดการพร้อมใช้งานเฉพาะในภาษาอังกฤษเท่านั้นในขณะนี้

ถ้าคุณเป็นนักพัฒนาที่สนใจในการสร้างการเลือกกำหนดเฉพาะประเทศหรือภูมิภาค หรือในการสร้างโซลูชันสำหรับประเทศหรือภูมิภาคที่ Microsoft ไม่สนับสนุนในขณะนี้ โปรดดู [โลกาภิวัตน์](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
