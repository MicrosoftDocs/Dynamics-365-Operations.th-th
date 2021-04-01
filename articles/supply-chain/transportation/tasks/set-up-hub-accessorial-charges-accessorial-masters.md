---
title: ตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับและต้นแบบอุปกรณ์เสริม
description: 'ขั้นตอนนี้แสดงวิธีการสร้างต้นแบบอุปกรณ์เสริมสำหรับฮับ และใช้ต้นแบบนั้นเพื่อสร้างค่าธรรมเนียมอุปกรณ์เสริมของฮับ '
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2e9125c7a38d1dc5e6866a056fb71f25e40928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233690"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>ตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับและต้นแบบอุปกรณ์เสริม

[!include [banner](../../includes/banner.md)]

ขั้นตอนนี้แสดงวิธีการสร้างต้นแบบอุปกรณ์เสริมสำหรับฮับ และใช้ต้นแบบนั้นเพื่อสร้างค่าธรรมเนียมอุปกรณ์เสริมของฮับ  กระบวนงานดังกล่าวใช้ชุดข้อมูล USMF โดยทั่วไปผู้ประสานงานขนส่งจะเป็นผู้ตั้งค่านี้


## <a name="set-up-a-hub-master"></a>ตั้งค่าต้นแบบฮับ
1. ไปที่การจัดการการขนส่ง > การตั้งค่า > การจัดอันดับ > ต้นแบบอุปกรณ์เสริม
2. คลิก สร้าง
3. ในฟิลด์ต้นแบบอุปกรณ์เสริม ให้พิมพ์ค่า
4. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
5. ในฟิลด์ชนิดอุปกรณ์เสริม ให้เลือก 'ฮับ'
6. คลิก บันทึก
7. ปิดหน้า

## <a name="set-up-a-hub-accessorial-charge"></a>ตั้งค่าค่าธรรมเนียมอุปกรณ์เสริมของฮับ
1. ไปที่การจัดการการขนส่ง > ตั้งค่า > การจัดอันดับ > ค่าธรรมเนียมอุปกรณ์เสริมของฮับ
2. คลิก สร้าง
3. ในฟิลด์ ID อุปกรณ์เสริมของฮับ ให้พิมพ์ค่า
4. ในฟิลด์ฮับ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
5. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
6. ในฟิลด์ตำแหน่งฮับ ให้เลือกหนึ่งตัวเลือก
    * คุณสามารถสร้างค่าธรรมเนียมเป็นทั้งเบิกหรือส่ง  ค่าธรรมเนียมจะนำมาใช้กับภาคการขนส่งในเส้นทางของคุณโดยขึ้นอยู่กับการเลือกของคุณ  
7. ในฟิลด์ต้นแบบอุปกรณ์เสริม ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
8. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
    * เลือกต้นแบบที่คุณเพิ่งสร้างขึ้น  
9. คลิก บันทึก
10. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]