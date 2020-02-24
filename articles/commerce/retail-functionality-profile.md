---
title: สร้างโพรไฟล์ฟังก์ชันของการขายปลีก
description: หัวข้อนี้จะอธิบายวิธีการสร้างโพรไฟล์ฟังก์ชันของการขายปลีกใหม่ Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9fb0fd63b11e55f2b153fc9c135f148a6e343057
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002854"
---
# <a name="create-a-retail-functionality-profile"></a>สร้างโพรไฟล์ฟังก์ชันของการขายปลีก


[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการสร้างโพรไฟล์ฟังก์ชันของการขายปลีกใหม่ Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

โพรไฟล์ฟังก์ชันของการขายปลีก มอบความสามารถในการตั้งค่าต่าง ๆ ที่ใช้สำหรับช่องทางออนไลน์ ช่องทางการขายปลีกแต่ละช่องต้องระบุโพรไฟล์ฟังก์ชันของการขายปลีก

## <a name="create-a-retail-functionality-profile"></a>สร้างโพรไฟล์ฟังก์ชันของการขายปลีก

เมื่อต้องการสร้างโพรไฟล์ฟังก์ชันของการขายปลีก ให้ทำตามขั้นตอนเหล่านี้

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
  
รูปภาพต่อไปนี้แสดงตัวอย่างของโพรไฟล์ฟังก์ชันของการขายปลีก
  
![ตัวอย่างโพรไฟล์ฟังก์ชันของการขายปลีก](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[รหัสข้อมูลและกลุ่มรหัสข้อมูล](info-codes-retail.md)           

[สร้างสมุดที่อยู่ใหม่](new-address-book.md) 

[ภาพรวมโครงร่างหน้าจอ](pos-screen-layouts.md)       

[ตั้งค่าคอนฟิกและติดตั้ง Retail Hardware Station](retail-hardware-station-configuration-installation.md) 
