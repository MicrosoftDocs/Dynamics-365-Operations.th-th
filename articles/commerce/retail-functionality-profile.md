---
title: สร้างโพรไฟล์ฟังก์ชันการขายปลีก
description: บทความนี้อธิบายวิธีการสร้างโพรไฟล์ฟังก์ชันการทำงานใน Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f006aaf594f1df097f80c77794e34f9b831e9949
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280253"
---
# <a name="create-a-retail-functionality-profile"></a>สร้างโพรไฟล์ฟังก์ชันการขายปลีก

[!include [banner](includes/banner.md)]

บทความนี้อธิบายวิธีการสร้างโพรไฟล์ฟังก์ชันการทำงานใน Microsoft Dynamics 365 Commerce

โพรไฟล์ฟังก์ชันการทำงานของการค้ามอบความสามารถในการตั้งค่าต่างๆ ที่ใช้สำหรับช่องทางออนไลน์ ช่องทางแต่ละช่องต้องระบุโพรไฟล์ฟังก์ชันการทำงาน

## <a name="create-a-functionality-profile"></a>สร้างโพรไฟล์ฟังก์ชัน

เมื่อต้องการสร้างโพรไฟล์ฟังก์ชันการทำงาน ให้ทำตามขั้นตอนเหล่านี้

1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> ตั้งค่าช่องทาง \> โพรไฟล์ POS \> โพรไฟล์ฟังก์ชัน**
1. บนหน้าต่างการดำเนินการ เลือก **สร้าง**
1. ในฟิลด์ **โพรไฟล์** ให้ป้อนรหัสของโพรไฟล์ ("FN006" ในรูปภาพตัวอย่างด้านล่าง)
1. ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า ("โพรไฟล์ Adventure Works" ในรูปภาพตัวอย่างด้านล่าง)
1. ในส่วน **ทั่วไป** ให้เลือกประเทศสำหรับระบบภาษา **ISO**
1. ในส่วน **ทั่วไป** ให้แก้ไขการตั้งค่าอื่น ๆ ตามต้องการ
1. ในส่วน **ทั่วไป** ให้เลือก **รหัสโพรไฟล์ใบเสร็จ** สำหรับใบเสร็จทางอีเมล
1. ในส่วน **ฟังก์ชัน** ให้แก้ไขการตั้งค่าตามต้องการ
1. ในส่วน **จำนวน** ให้แก้ไขการตั้งค่าตามต้องการ
1. ในส่วน **รหัสข้อมูล** ให้แก้ไขการตั้งค่าตามต้องการ
1. ในส่วน **การกำหนดหมายเลขใบเสร็จ** ให้แก้ไขการตั้งค่าตามต้องการ 
  
ภาพต่อไปนี้แสดงตัวอย่างของโปรไฟล์ฟังก์ชันการทำงาน
  
![ตัวอย่างโพรไฟล์ฟังก์ชันการทำงาน](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[รหัสข้อมูลและกลุ่มรหัสข้อมูล](info-codes-retail.md)           

[สร้างสมุดที่อยู่ใหม่](new-address-book.md) 

[ภาพรวมโครงร่างหน้าจอ](pos-screen-layouts.md)       

[ตั้งค่าคอนฟิกและติดตั้ง Retail Hardware Station](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
