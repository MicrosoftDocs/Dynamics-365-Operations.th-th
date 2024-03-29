---
title: การกระทบยอดทางการเงินในร้านค้าปลีก
description: บทความนี้จะอธิบายการกระทบยอดทางการเงินในร้านค้าปลีกสำหรับ POS สำหรับ Microsoft Dynamics 365 Commerce
author: anpurush
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 19c0f6edd7756a611a234a162418ef5826bd5cc2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860255"
---
# <a name="financial-reconciliation-in-retail-stores"></a>การกระทบยอดทางการเงินในร้านค้าปลีก

[!include [banner](includes/banner.md)]

ใน Microsoft Dynamics 365 Commerce รุ่น 10.0.10 และรุ่นก่อนหน้านี้ ฟังก์ชันการทำงานที่มีไคลเอนต์การขายหน้าร้าน (POS) สำหรับกระบวนการสิ้นสุดวันในร้านค้าปลีกช่วยให้พนักงานร้านค้าและผู้จัดการร้านค้าทำการดำเนินงานการสิ้นสุดวัน ตัวอย่างเช่น สามารถทำการตรวจนับเงิน ปิดกะแบบซ่อน กระทบยอดธุรกรรมกะ และปิดกะ อย่างไรก็ตามไม่มีความสามารถใน POS เพื่อสรุปข้อมูลทางการเงินสำหรับกะเพื่อให้สามารถใช้ในการลงรายการบัญชีการเงินในสำนักงานใหญ่ Commerce โดยทั่วไปผู้จัดการร้านค้าต้องรับผิดชอบการทำงานนี้ให้เสร็จสมบูรณ์ ก่อนที่จะสามารถลงชื่อออกจากกะ ผู้ใช้เหล่านั้นต้องตรวจทานข้อมูลดังกล่าว ทำการแก้ไขใดๆ ที่จำเป็น และสรุปยอดรวมของกะนั้น ดังนั้นควรมีการลงรายการบัญชีสรุปยอดรวมขั้นสุดท้ายในโมดูลทางการเงินในสำนักงานใหญ่ Commerce

นอกจากนี้ใน Commerce รุ่น 10.0.10 และรุ่นก่อนหน้านี้ ผู้จัดการร้านค้าสามารถตรวจทานและทำการปรับปรุงบางอย่างไปยังรายการใบแจ้งยอดในสำนักงานใหญ่ Commerce อย่างไรก็ตามความสามารถมีจำกัดและผู้จัดการร้านค้าไม่ค่อยมีสิทธิ์เข้าถึงไคลเอนต์สำนักงานใหญ่ Commerce นอกจากนี้คุณสามารถทำการตรวจทานและปรับปรุงใบแจ้งยอดการขายปลีกทางการเงินได้เฉพาะเมื่อมีการสร้างใบแจ้งยอดในสำนักงานใหญ่ Commerce เท่านั้น อย่างไรก็ตามกระบวนการดังกล่าวโดยทั่วไปจะเป็นกระบวนการกลางคืน ผู้จัดการร้านค้าต้องรอสำหรับการลงชื่อออกกะเมื่อมีการสร้างใบแจ้งยอดการขายปลีกทางการเงินในสำนักงานใหญ่ Commerce

ใน Commerce รุ่น10.0.11 และรุ่นใหม่กว่า ผู้จัดการร้านสามารถตรวจทาน ปรับปรุง และทำการสรุปกะในไคลเอนต์ POS เอง จากนั้นข้อมูลดังกล่าวจะใช้เพื่อสร้างและลงรายการบัญชีใบแจ้งยอดการขายปลีกทางการเงินในสำนักงานใหญ่ Commerce

> [!NOTE]
> ฟังก์ชันที่เกี่ยวข้องกับการกระทบยอดทางการเงินในร้านค้าปลีกทำงานได้เฉพาะเมื่อมีการเปิดใช้งานการสร้างใบสั่งตามฟีดแบบต่อเนื่อง สำหรับข้อมูลเพิ่มเติม ดูที่ [การสร้างใบสั่งตามฟีดแบบต่อเนื่องสำหรับธุรกรรมร้านค้าปลีก](trickle-feed.md)

## <a name="set-up-financial-reconciliation"></a>ตั้งค่าการกระทบยอดทางการเงิน

ทำตามขั้นตอนต่อไปนี้เพื่อใช้ฟังก์ชันการกระทบยอดทางการเงิน

1. ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้เปิดใช้งานคุณลักษณะ **ใบแจ้งยอดการขายปลีก - การสร้างฟีดแบบต่อเนื่อง**
1. ในโพรไฟล์ฟังก์ชันของ POS สำหรับร้านค้าที่เหมาะสม ให้ตั้งค่าตัวเลือก **เปิดใช้งานการกระทบยอดทางการเงินในร้านค้า** เป็น **ใช่**

## <a name="more-information-about-financial-reconciliation"></a>ข้อมูลเพิ่มเติมเกี่ยวกับการกระทบยอดทางการเงิน

เมื่อมีการเปิดใช้งานฟังก์ชันการกระทบยอดทางการเงินไว้ บางพารามิเตอร์ที่กำหนดไว้บนแท็บด่วน **ใบแจ้งยอด/การปิด** ของหน้า **ร้านค้าปลีก** ในสำนักงานใหญ่ Commerce จะถูกซิงค์ไปยังฐานข้อมูลช่องทาง มีการบังคับใช้ชุดเงื่อนไขการคำนวณและขีดจำกัดยอดเงินเดียวกันที่ใช้สำหรับใบแจ้งยอดการขายปลีก

เมื่อมีการเรียกใช้การดำเนินงาน **ปิดกะ** ระบบจะตรวจสอบว่ายอดเงินที่คำนวณได้ของระบบและยอดเงินที่ประกาศตรงกัน ถ้าแตกต่างกันและผลต่างเกินกว่าขีดจำกัดที่กำหนด ผู้ใช้จะได้รับการแจ้งเตือนและสามารถทำการปรับปรุงที่จำเป็นได้

สามารถทำการปรับปรุงสำหรับการชำระเงินแต่ละครั้งได้ เมื่อเลือกวิธีการชำระเงินแล้ว ผู้ใช้จะสามารถดูผลรวมสำหรับชนิดธุรกรรมต่างๆ และแก้ไขยอดรวมสำหรับชนิดธุรกรรมที่ระบุได้ ในระหว่างการแก้ไข ระบบจะแสดงยอดเงินที่คำนวณเดิมและยอดเงินที่แทนที่สำหรับชนิดธุรกรรมนั้น นอกจากนี้ผู้ใช้ยังสามารถบันทึกหมายเหตุเป็นส่วนหนึ่งของกระบวนการแก้ไขได้ด้วย สามารถใช้หมายเหตุสำหรับวัตถุประสงค์ในการตรวจสอบ

ผู้ใช้สามารถละเว้นพร้อมต์และข้อความการตรวจสอบความถูกต้องและสามารถดำเนินการต่อเพื่อปิดกะ อย่างไรก็ตามถ้าผู้ใช้ละเว้นพร้อมท์ การตรวจสอบความถูกต้องจะเกิดปัญหาเดียวกันและจะต้องได้รับการแก้ไขเมื่อลงรายการบัญชีใบแจ้งยอดทางการเงินในสำนักงานใหญ่ Commerce

การดำเนินการ **ปิดกะ** ใน POS ยังตรวจสอบว่ามีการซิงค์ธุรกรรมทั้งหมดในฐานข้อมูลออฟไลน์ไปยังฐานข้อมูลช่องทาง ถ้ามีธุรกรรมใดๆ ที่ไม่ได้ซิงค์ ผู้ใช้จะได้รับข้อความเตือน เนื่องจากสถานการณ์นี้อาจทำให้ยอดเงินของระบบถูกคำนวณอย่างไม่ถูกต้อง ในสถานการณ์นี้ ผู้ใช้สามารถสิ้นสุดการดำเนินงาน **ปิดกะ** และลองซิงค์ธุรกรรมแบบออฟไลน์กับฐานข้อมูลช่องทาง อีกทางหนึ่งคือผู้ใช้สามารถปรับปรุงยอดเงินที่มีการคำนวณจากระบบด้วยตนเองให้กับบัญชีสำหรับธุรกรรมที่ยังไม่ได้ซิงค์ เพื่อให้มีสรุปหมายเลขทางการเงินที่ถูกต้องและมีการลงรายการบัญชี 

เมื่อมีการใช้การสร้าการลงรายการบัญชีใบแจ้งยอดของฟีดแบบต่อเนื่อง เพื่อให้การลงรายการบัญชีธุรกรรมถูกแยกออกจากการลงรายการบัญชีของการเงิน คุณสามารถเลือกที่จะปรับปรุงยอดเงินที่คำนวณได้ของระบบสำหรับธุรกรรมแบบออฟไลน์ที่ขาดหายไป ด้วยวิธีนี้ คุณต้องตรวจสอบให้แน่ใจว่ามีการลงบัญชีและลงรายการบัญชีอย่างถูกต้องเสมอ ไม่ว่าจะมีธุรกรรมที่ขาดหายไปหรือไม่ สามารถซิงค์ธุรกรรมแบบออฟไลน์กับศูนย์ควบคุมฐานข้อมูลช่องทางและ Commerce แล้วลงรายการบัญชีในภายหลังแยกต่างหากจากการลงรายการบัญชีทางการเงิน

รายละเอียดของการกระทบยอดทางการเงินสำหรับกะจะถูกซิงค์กับสำนักงานใหญ่ Commerce โดยใช้งาน P

ใบแจ้งยอดการขายปลีกทางการเงินในสำนักงานใหญ่ Commerce ไม่คำนวณผลรวมเพื่อแสดงรายละเอียดเกี่ยวกับรายการใบแจ้งยอด แทนที่จะใช้ยอดเงินขั้นสุดท้ายในไคลเอนต์ POS เพื่อสร้างและลงรายการบัญชีใบแจ้งยอดการขายปลีกทางการเงิน


[!INCLUDE[footer-include](../includes/footer-banner.md)]