---
title: "ขยายฟังก์ชันของ Microsoft Dynamics 365 for Talent"
description: "ถ้าคุณได้สร้าง Microsoft PowerApps ใดๆ คุณสามารถเริ่มต้นแอพลิเคชันเหล่านั้นได้จากลิงค์ภายใน Microsoft Dynamics 365 for Talent"
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: th-th
ms.lasthandoff: 03/08/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>ขยายฟังก์ชันของ Microsoft Dynamics 365 for Talent

[!INCLUDE [banner](includes/banner.md)]

ถ้าคุณได้สร้าง Microsoft PowerApps ใดๆ คุณสามารถเริ่มต้นแอพลิเคชันเหล่านั้นได้จากลิงค์ภายใน Microsoft Dynamics 365 for Talent เพื่อตั้งค่าการเข้าถึงแอพลิเคชันของคุณ คุณจะต้องตั้งค่าข้อมูลบางอย่างใน Talent บนหน้าการตั้งค่าคอนฟิกที่คุณสามารถเปิดได้จากพื้นที่ทำงาน **การจัดการระบบ**

## <a name="configuring-embedded-powerapps-within-talent"></a>การตั้งค่าคอนฟิก PowerApps ที่ฝังอยู่ภายใน Talent
ใช้หน้า **ตั้งค่า Microsoft PowerApps ที่ฝังอยู่** เพื่อตั้งค่าคอนฟิกหน้า Talent ให้เริ่มต้นแอพลิเคชัน PowerApps เพื่อเปิดหน้า **ตั้งค่า Microsoft PowerApps ที่ฝังอยู่** เปิดพื้นที่ทำงาน **การจัดการระบบ** และจากนั้นเปิดแท็บ **ลิงค์** เลือก **Microsoft PowerApps** จากกลุ่ม **การตั้งค่า** 

มีการป้อนหรือตั้งค่าข้อมูลต่อไปนี้บนหน้านี้: 

 -  ชื่อที่เป็นคำอธิบายหรือตัวระบุสำหรับแอพลิเคชัน PowerApps แต่ละรายการ
 -  ตัวระบุเฉพาะ (GUID) สำหรับแต่ละแอพลิเคชันที่คุณเพิ่มไปยังเพจ Talent รหัสแอปจะพร้อมใช้งานบนไซต์ PowerApps [powerapps.com](http://powerapps.com/) 
 -  หน้าที่ผู้ใช้สามารถเปิดแอปหรือรายงาน ไม่ใช่เพจ Talent ทั้งหมดที่สนับสนุนรายงาน PowerApps แบบฝัง และ Power BI 

 > [!NOTE]
 >  ป้อนชื่อภายในของหน้า ไม่ใช่ชื่อที่แสดงที่ปรากฏที่ด้านบนของหน้า เพื่อค้นหาชื่อภายใน เปิดเพจที่คุณต้องการชื่อภายใน และคลิกขวาที่ใดก็ได้บนหน้านั้น เมื่อเปิดเมนู วางเมาส์ไว้เหนือรายการ **ข้อมูลฟอร์ม** ชื่อแบบฟอร์มภายในจะแสดงขึ้นถัดจากรายการ **ข้อมูลฟอร์ม** ในเมนู
 
-   ระบุตัวควบคุมแบบฟอร์มที่แอพลิเคชันสามารถดึงข้อมูลบริบทได้ ตัวอย่างเช่น แอพลิเคชันอาจใช้ข้อมูลเกี่ยวกับผู้ปฏิบัติงาน ถ้าคุณป้อนหน้า **ผู้ปฏิบัติงาน** ในฟิลด์ **บริบท** หน้า **ผู้ปฏิบัติงาน** จะเปิดขึ้น เมื่อคุณเริ่มต้นแอพลิเคชัน รายการใน **ฟิลด์บริบท** ไม่จำเป็น 
-   ตั้งค่าขนาดของกล่องโต้ตอบที่จะเรียกใช้แอพลิเคชัน PowerApps กล่องโต้ตอบถูกกำหนดเป็น "เล็ก" หรือ "ใหญ่" เพื่อเพิ่มประสิทธิภาพอินเทอร์เฟสผู้ใช้ เมื่อแอพลิเคชันของคุณสำหรับการทำงานบนโทรศัพท์หรืออุปกรณ์ใหญ่ ตามลำดับ 


คุณยังสามารถระบุว่าแอพลิเคชันจะพร้อมใช้งานสำหรับนิติบุคคลใด หรือคุณสามารถทำให้พร้อมใช้งานสำหรับนิติบุคคลทั้งหมดของคุณได้ โดยค่าเริ่มต้น แอพลิเคชัน PowerApps ของคุณ จะพร้อมใช้งานกับนิติบุคคลทั้งหมด

## <a name="opening-an-application"></a>การเปิดแอพลิเคชัน
เมื่อคุณได้ตั้งค่าคอนฟิกแอพลิเคชัน PowerApps แบบฝัง ลิงค์ไปยังแอพลิเคชันที่คุณระบุ จะถูกเพิ่มลงในหน้าภายใน Talent คลิกลิงค์เพื่อเปิดแอป 



