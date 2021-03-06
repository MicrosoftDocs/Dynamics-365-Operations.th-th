---
title: แบ่งไฟล์ XML ที่สร้างตามขนาดไฟล์และปริมาณเนื้อหา
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการแบ่งไฟล์ที่สร้างตามขนาดไฟล์และปริมาณสินค้าในเนื้อหา
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: d60266aba42f502e7707bdace921cfee4526b6ae
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682882"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>แบ่งไฟล์ XML ที่สร้างตามขนาดไฟล์และปริมาณเนื้อหา

[!include[banner](../includes/banner.md)]

คุณสามารถออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารขาออกในรูปแบบ XML ได้ บางครั้ง เอกสารเหล่านั้นสามารถได้รับการยอมรับ เมื่อพวกเขาเป็นไปตามเกณฑ์ที่ระบุ เช่น ขนาดไฟล์สูงสุด หรือจำนวนสูงสุดของโหนด XML บางโหนด คุณสามารถออกแบบรูปแบบ ER ที่จะสร้างเอกสารทางอิเล็กทรอนิกส์ที่ตอบสนองความต้องการที่ผู้รับของเหล่านั้นระบุ

- สำหรับองค์ประกอบรูปแบบไฟล์ คุณสามารถกำหนดขีดจำกัดในขนาดไฟล์เป็นนิพจน์ ER ได้ ถ้าเกินขีดจำกัดที่กำหนดไว้ เมื่อมีการสร้างรายงาน ER ER เสร็จสิ้นการสร้างไฟล์ปัจจุบัน และจากนั้นจะย้ายไปที่การสร้างไฟล์ถัดไป
- สำหรับรูปแบบองค์ประกอบไฟล์ XML ใดๆ คุณสามารถกำหนดขีดจำกัดในจำนวนขององค์ประกอบเป็นนิพจน์ ER ได้ ถ้าจำนวนของโหนด XML ในไฟล์ที่สร้างเกินขีดจำกัดที่กำหนดไว้ เมื่อมีการรันรายงาน ER ER เสร็จสิ้นการสร้างไฟล์ปัจจุบัน และจากนั้นจะย้ายไปที่การสร้างไฟล์ถัดไป
- สำหรับองค์ประกอบรูปแบบลำดับ XML ใดๆ คุณสามารถกำหนดขีดจำกัดในจำนวนขององค์ประกอบรองเป็นนิพจน์ ER ได้ ถ้าจำนวนของโหนด XML ที่ซ้อนกันขององค์ประกอบรูปแบบในไฟล์ที่สร้างเกินขีดจำกัดที่กำหนดไว้ เมื่อมีการรันรายงาน ER ER เสร็จสิ้นการสร้างไฟล์ปัจจุบัน และจากนั้นจะย้ายไปที่การสร้างไฟล์ถัดไป
- คุณสามารถทำเครื่องหมายรูปแบบองค์ประกอบ XML ใดๆ เป็นไม่สามารถหยุดได้ ด้วยวิธีนี้ คุณสามารถทำให้รายการที่ซ้อนกันของโหนด XML ที่สร้างขึ้นภายใต้องค์ประกอบรูปแบบอยู่ในไฟล์เดียวที่สร้างขึ้น

นอกเหนือจากการใช้องค์ประกอบ XML และองค์ประกอบรูปแบบลำดับ XML เพื่อเพิ่มโหนด XML ไปยังไฟล์ที่สร้างขึ้น คุณสามารถใช้องค์ประกอบรูปแบบ XML ดิบได้ อย่างไรก็ตาม โหนดที่คุณเพิ่มโดยใช้องค์ประกอบรูปแบบ XML ดิบ จะไม่ได้รับการพิจารณา เมื่อมีการคำนวณจำนวนของโหนดที่จะประเมินข้อจำกัดเกี่ยวกับจำนวนขององค์ประกอบ

ถ้าคุณตั้งค่าคอนฟิกปลายทางของไฟล์สำหรับองค์ประกอบรูปแบบไฟล์ที่มีการตั้งค่าคอนฟิก เพื่อแบ่งผลลัพธ์ที่สร้างขึ้นทุกครั้งที่เกินขีดจำกัดเฉพาะ แต่ละส่วนของผลลัพธ์ที่สร้างขึ้นถูกส่งไปที่ปลายทางไฟล์ที่ตั้งค่าคอนฟิกเป็นไฟล์แต่ละไฟล์ ในการตั้งชื่อไฟล์ที่สร้างโดยแบ่งผลลัพธ์โดยไม่ซ้ำกัน คุณต้องตั้งค่าคอนฟิกนิพจน์ ER สำหรับองค์ประกอบรูปแบบไฟล์ ถ้าคุณรวมแหล่งข้อมูล ER ของชนิดลำดับหมายเลข ระบบจะเพิ่มลำดับหมายเลขสำหรับแต่ละส่วนของผลลัพธ์ที่แบ่ง

หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะนี้ เล่นคู่มืองาน **ER แบ่งไฟล์ XML ตามขนาดไฟล์หรือปริมาณรายการเนื้อหา** ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 จัดหา/พัฒนาส่วนประกอบของบริการ/โซลูชันด้านไอที (10677)** และคุณสามารถดาวน์โหลดได้จาก [ศูนย์ดาวน์โหลด Microsoft](https://go.microsoft.com/fwlink/?linkid=874684) คู่มืองานนี้จะแนะนำคุณตลอดกระบวนการตั้งค่าคอนฟิกรูปแบบ ER ที่จะแบ่งไฟล์ที่สร้างตามขีดจำกัดในขนาดไฟล์และปริมาณสินค้าเนื้อหา เพื่อดำเนินการคู่มืองานให้เสร็จสมบูรณ์ คุณต้องดาวน์โหลดไฟล์ต่อไปนี้:

- [การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER - XmlFilesSplittingModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [การตั้งค่าคอนฟิกรูปแบบ ER - XmlFilesSplittingFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม
[ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-destinations.md)

[โปรแกรมออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]