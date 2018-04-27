---
title: "ความต้องการของระบบ Dynamics 365 for Talent และนโยบายการอัพเดต"
description: "หัวข้อนี้แสดงรายการความต้องการสำหรับ Dynamics 365 for Talent นอกจากนี้ยังระบุนโยบายการอัพเดตด้วย"
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 954f6237739defe14aaa13b19641f9f9d27b5fac
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="microsoft-dynamics-365-for-talent-system-requirements-and-update-policy"></a>ความต้องการของระบบ Microsoft Dynamics 365 for Talent และนโยบายการอัพเดต

[!INCLUDE [banner](includes/banner.md)]

หัวข้อนี้แสดงรายการความต้องการสำหรับ Microsoft Dynamics 365 for Talent นอกจากนี้ยังระบุนโยบายการอัพเดตด้วย

## <a name="supported-web-browsers"></a>เว็บเบราเซอร์ที่สนับสนุน

โปรแกรมประยุกต์บนเว็บ Microsoft Dynamics 365 for Talent สามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ที่ทำงานบนระบบปฏิบัติการที่ระบุ: 

*   Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10
*   Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7
*   Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus แท็บเล็ต 10
*   Apple Safari (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) หรือ 10.12 (Sierra) หรือ Apple iPad

เมื่อต้องการค้นหารุ่นล่าสุดของแต่ละเว็บเบราเซอร์ ไปที่เว็บไซต์ของผู้ผลิตซอฟต์แวร์ 

> [!NOTE]
> * เมื่อต้องการจับภาพรูปที่สร้างขึ้นจากตัวบันทึกงาน และรวมค่าเหล่านั้นไว้ในเอกสาร Microsoft Word คุณต้องติดตั้งส่วนขยาย Chrome ไว้ 
> * ตัวแก้ไขเวิร์กโฟลว์จะเริ่มต้นการใช้งานเป็นแอพลิเคชัน ClickOnce เฉพาะ Microsoft Edge และ Internet Explorer (ในรุ่นที่สนับสนุนของ Microsoft Windows) สนับสนุนแอพลิเคชัน ClickOnce แอพลิเคชัน ClickOnce โปรแกรมแก้ไขลำดับงานต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต
> * เมื่อต้องการแสดงตัวอย่างไฟล์ PDF เราขอแนะนำให้คุณใช้เบราว์เซอร์ที่ทันสมัย เช่น Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10 หรือ Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บนแท็บเล็ต Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus 10
>   ข้อกำหนดของเครือข่าย
> * Dynamics 365 for Talent ได้รับการออกแบบมาสำหรับเครือข่ายที่มีเวลาแฝง 250-300 มิลลิวินาที (ms) หรือน้อยกว่า นี่คือเวลาแฝงจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Microsoft Azure ที่โฮสต์ Dynamics 365 for Talent เราขอแนะนำให้คุณทดสอบเวลาแฝงบนเครือข่ายที่ [www.azurespeed.com](http://www.azurespeed.com "Azure Latency Test")
> * ข้อกำหนดของแบนด์วิธสำหรับ Dynamics 365 for Talent ขึ้นอยู่กับสถานการณ์ของคุณ สถานการณ์ทั่วไปส่วนใหญ่จำเป็นต้องมีแบนด์วิดท์ที่มากกว่า 50 กิโลไบต์ต่อวินาที (KBps)
> 
> [!WARNING]
> อย่าคำนวณข้อกำหนดของแบนด์วิดท์จากตำแหน่งที่ตั้งของไคลเอนต์ โดยการคูณจำนวนผู้ใช้กับข้อกำหนดของแบนด์วิดท์ต่ำสุด การใช้งานที่เกิดขึ้นพร้อมกันของตำแหน่งที่ตั้งที่กำหนดเป็นสิ่งที่คำนวณได้ยาก สำหรับลูกค้าที่มีความกังวลเกี่ยวกับข้อกำหนดของแบนด์วิดท์ ให้ใช้ Dynamics 365 for Talent รุ่นทดลองใช้

## <a name="supported-microsoft-office-applications"></a>แอพลิเคชัน Microsoft Office ที่ได้รับการสนับสนุน

* เมื่อต้องการเรียกใช้ Add-in ของ Microsoft Excel และ Word คุณจะต้องตั้งค่า Microsoft Office 2016 สำหรับ Windows หรือ Mac ไว้ สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับข้อกำหนดของเวอร์ชัน ให้ดูที่ [การแก้ไขปัญหาการรวมของ Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "การแก้ไขปัญหาการรวมของ Office")
* เมื่อต้องการดูเอกสารที่สร้างขึ้นโดยฟังก์ชันส่งออกไปที่ Excel หรือส่งออกไปที่ Word คุณต้องติดตั้ง Microsoft Office 2007 หรือรุ่นที่ใหม่กว่าไว้

## <a name="update-policy"></a>นโยบายการอัพเดต

Microsoft Dynamics 365 for Talent ทำหน้าที่เหมือนกับการเสนอของ Cloud มีการอัพเดต Dynamics 365 for Talent อย่างต่อเนื่อง และนำไปใช้โดยอัตโนมัติโดย Microsoft

การอัพเดตจะถูกนำออกใช้เป็นช่วงเวลาตามปกติ และจะนำไปใช้กับสภาพแวดล้อมทั้งหมด  Dynamics 365 for Talent ได้รับการสนับสนุนตาม [นโยบายของ Microsoft Support Lifecycle](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle") ซึ่งให้คำแนะนำอย่างต่อเนื่องและคาดการณ์ได้สำหรับความพร้อมในการสนับสนุนผลิตภัณฑ์

