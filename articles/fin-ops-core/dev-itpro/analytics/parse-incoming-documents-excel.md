---
title: แยกวิเคราะห์เอกสารขาเข้าในรูปแบบ Excel
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อแยกวิเคราะห์เนื้อหาที่มีในไฟล์ Microsoft Excel ขาเข้า
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3f83271327df186d407516ff1a197800ffc8c78c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249367"
---
# <a name="parse-incoming-documents-in-excel-format"></a>แยกวิเคราะห์เอกสารที่กำลังจะมาถึงในรูปแบบ Excel

[!include[banner](../includes/banner.md)]

คุณสามารถออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อแยกวิเคราะห์ไฟล์ Microsoft Excel ขาเข้าที่แสดงข้อมูลในสมุดงาน Microsoft Excel (ไฟล์ในรูปแบบ XLSX) จากนั้นคุณสามารถใช้เนื้อหาจากไฟล์เหล่านี้เพื่ออัพเดตข้อมูลแอพลิเคชันได้ สิ่งนี้มีประโยชน์ ถ้าคุณ:

- ออกแบบแบบจำลองและรูปแบบใหม่ และต้องการทดสอบในขณะทำงาน ในกรณีนี้ Excel จะจำลองข้อมูลแอพลิเคชันจริง
- จัดการข้อมูลนอกเหนือจากแอพลิเคชันของคุณใน Excel และต้องการนำเข้าข้อมูลนี้เพื่อส่งรายงานเฉพาะ

เพื่อเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ เล่นคู่มืองาน **ER นำเข้าข้อมูลจากไฟล์ Microsoft Excel (ส่วนที่ 1: ออกแบบรูปแบบ)** และ **ER นำเข้าข้อมูลจากไฟล์ Microsoft Excel (ส่วนที่ 2: นำเข้าข้อมูล)** (ส่วนของ 7.5.4.3 รับ/พัฒนาองค์ประกอบบริการ/โซลูชันด้าน IT (10677) กระบวนการทางธุรกิจ) คู่มืองานเหล่านี้จะแนะนำวิธีในการแยกวิเคราะห์ไฟล์ Excel ขาเข้า โดยใช้รูปแบบ ER เพื่อนำเข้าข้อมูลจากเอกสารขาเข้าและอัพเดตข้อมูลแอพลิเคชัน คุณสามารถดาวน์โหลดไฟล์คู่มืองานได้จาก [ศูนย์ดาวน์โหลด Microsoft](https://go.microsoft.com/fwlink/?linkid=874684)

ดาวน์โหลดไฟล์ต่อไปนี้เพื่อดำเนินการคู่มืองานที่กล่าวถึงด้านบนให้เสร็จสมบูรณ์

| คำอธิบายเนื้อหา                         | ไฟล์                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| ไฟล์ขาเข้าในรูปแบบ XLSX - เท็มเพลต    | [1099import template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| ไฟล์ขาเข้าในรูปแบบ XLSX - ข้อมูลตัวอย่าง | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

ถ้าคุณยังไม่ได้เล่นคู่มืองานต่อไปนี้ [ER สร้างการตั้งค่าคอนฟิกที่จำเป็นเพื่อนำเข้าข้อมูลจากไฟล์ภายนอก](./tasks/er-required-configurations-import-data.md) ในแอพลิเคชัน Finance and Operations ปัจจุบัน ดาวน์โหลดไฟล์ต่อไปนี้

| คำอธิบายเนื้อหา    | ไฟล์                                                            |
|------------------------|-----------------------------------------------------------------|
| การตั้งค่าคอนฟิกแบบจำลอง ER | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |
