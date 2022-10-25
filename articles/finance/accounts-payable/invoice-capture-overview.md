---
title: ภาพรวมของโซลูชัน Invoice Capture
description: บทความนี้แสดงข้อมูลเกี่ยวโซลูชัน Invoice Capture
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691206"
---
# <a name="invoice-capture-solution"></a>โซลูชัน Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

บทความนี้มีข้อมูลเกี่ยวกับโซลูชัน Invoice Capture ที่สร้างใบแจ้งหนี้ของผู้จัดจำหน่ายจากรูปภาพใบแจ้งหนี้ดิจิทัลโดยอัตโนมัติ

แผนกบัญชีเจ้าหนี้ (AP) จะจัดการและประมวลผลใบแจ้งหนี้ให้กับสินค้าและบริการที่ได้รับ นักบัญชี AP จะตรวจสอบความถูกต้องของข้อมูลในใบแจ้งหนี้ของผู้จัดจำหน่ายด้วยเหตุผลต่อไปนี้:

- เพื่อหลีกเลี่ยงความพยายามเพิ่มเติมถ้าต้องปรับปรุงหรือการแก้ไขในระหว่างการปิดรอบระยะเวลา
- การชำระใบแจ้งหนี้ของผู้จัดจำหน่ายภายในเวลาที่เหมาะสมและป้องกันการขาดทุนทางการเงินเนื่องจากเกิดข้อผิดพลาดหรือการฉ้อโกง

การรู้จำอักขระด้วยแสง (OCR) เป็นที่ใช้กันมากโดยอุตสาหกรรมต่างๆ ในปีที่ผ่านมา เป็นเรื่องปกติที่ข้อความที่พิมพ์จะถูกแปลงเป็นดิจิทัล จึงสามารถแก้ไขได้ทางอิเล็กทรอนิกส์ ค้นหา จัดเก็บอย่างมีขนาดและมีการแสดงทางออนไลน์ ข้อความดิจิทัลสามารถใช้ในกระบวนการของเครื่องจักร เช่น ระบบคอมพิวเตอร์ การแปลภาษาด้วยเครื่อง ข้อความเป็นคำพูด ข้อมูลหลัก และการทำเหมืองข้อความ

วิธีการล่าสุดของเทคโนโลยีปัญญาประดิษฐ์ (AI) ได้เปิดใช้งานโซลูชัน OCR สมัยใหม่เพื่ออ่านรูปแบบใบแจ้งหนี้ต่างๆ จากผู้จัดจำหน่ายต่างๆ โดยไม่ต้องมีการแทรกแซงจากมนุษย์มาก บริษัทมากขึ้นรับรู้ว่าบริษัทสามารถประหยัดความพยายามและปรับปรุงความถูกต้องโดยการประมวลผลใบแจ้งหนี้ผ่านระบบอัตโนมัติแทนการประมวลผลด้วยตนเอง

## <a name="system-landscape"></a>ภูมิทัศน์ของระบบ

ในภาพอธิบายต่อไปนี้จะแสดงส่วนประกอบและขั้นตอนหลักในโซลูชัน Invoice Capture

[![ส่วนประกอบและขั้นตอนในโซลูชัน Invoice Capture](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>บทบาทที่จำเป็น

ตารางต่อไปนี้แสดงบทบาทที่ต้องใช้ในการตั้งค่าและใช้โซลูชัน Invoice Capture

| บทบาท          | การดำเนินการ | ระบบ | ชื่อบทบาท |
|---------------|---------|---------|-----------|
| ผู้ดูแลระบบ | <ul><li>ตั้งค่าสภาพแวดล้อมใน Microsoft Power Platform</li><li>ปรับใช้โซลูชันใน Microsoft Power Platform</li><li>ตั้งค่าการเชื่อมต่อระหว่าง Dynamics 365 และ AI Builder</li><li>ตั้งค่าที่ตั้ง Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>ผู้ดูแลระบบ Dynamics 365</li><li>ผู้ดูแลระบบ Power Platform</li><li>เจ้าของข้อมูล Blob ที่จัดเก็บ</li></ul> |
| ผู้ผลิต AI      | <ul><li>รักษาโฟลว์</li><li>สร้างโมเดล AI แบบจำหนดเอง</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>ผู้สร้างพลเมือง</li></ul> |
| เสมียน AP      | <ul><li>ตรวจทานและใช้เวลาการทั้งหมดในพื้นที่การจัดเตรียมใบแจ้งหนี้ของผู้จัดจำหน่าย</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>บทบาทใหม่ของเสมียน AP ใน Power Platform</li></ul> |
| เสมียน AP      | <ul><li>ดําเนินงานรายวันในฐานะเสมียน AP</li><li>นําทางไปยังพื้นที่ที่จัดเตรียมใบแจ้งหนี้ของผู้จัดจำหน่าย</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>เจ้าหน้าที่บัญชีเจ้าหนี้</li></ul> |
  
หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการติดตั้ง Invoice Capture ดูที่ [ติดตั้ง Invoice Capture](../accounts-payable/install-invoice-capture.md)  
