---
title: เชื่อมโยงสินทรัพย์ถาวรกับสัญญาเช่า
description: หัวข้อนี้จะอธิบายวิธีการเชื่อมโยงสินทรัพย์ถาวรที่มีอยู่กับสัญญาเช่าใหม่
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 274fcc73b48282a8025a210dd488105500609d5a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971439"
---
# <a name="associate-fixed-assets-with-leases"></a>เชื่อมโยงสินทรัพย์ถาวรกับสัญญาเช่า

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการเชื่อมโยงสินทรัพย์ถาวรที่มีอยู่กับสัญญาเช่าใหม่ เมื่อคุณเชื่อมโยงสินทรัพย์ถาวรกับสัญญาเช่า มูลค่าของสิทธิ์การใช้สินทรัพย์ (ROU) ที่การรับรู้เริ่มต้น จะเป็นต้นทุนการซื้อสินทรัพย์ถาวร

ก่อนที่คุณจะสามารถเชื่อมโยงสินทรัพย์ถาวรกับสัญญาเช่า คุณต้องสร้างเรกคอร์ดสำหรับสินทรัพย์ถาวรในสินทรัพย์ถาวร หลังจากนั้น บนหน้า **สรุปสัญญาเช่า** คุณต้องสร้างสัญญาเช่าและลิงค์สินทรัพย์กับสัญญาเช่านั้น

1. เพิ่มสัญญาเช่าโดยทำตามขั้นตอนใน [เพิ่มหรือคัดลอกสัญญาเช่า](add-lease.md) บนหน้า **เพิ่มสัญญาเช่า** ในฟิลด์ **หมายเลขสินทรัพย์ถาวร** ให้เลือกสินทรัพย์ที่ยังไม่ได้ซื้อมา
2. เลือก **สมุดบัญชี** และยืนยันกำหนดการชำระเงิน
3. เลือก **การรับรู้เริ่มต้น**
4. เลือก **สมุดรายวันการเช่าสินทรัพย์**

    รายการสมุดรายวันการรับรู้เริ่มต้นสำหรับสัญญาเช่า จะเดบิตสินทรัพย์ถาวรสำหรับยอดเงินที่โดยปกติจะถูกเดบิตไปที่บัญชีสิทธิ์การใช้สินทรัพย์

    ขณะนี้คุณสามารถดูชนิดธุรกรรมและสมุดบัญชีสำหรับสินทรัพย์ถาวร

5. เลือก  **รายละเอียดของสมุดรายวัน**
6. เลือก **รายการ** เพื่อดูรายการแต่ละบรรทัดสำหรับรายการสมุดรายวัน
7. เลือกบรรทัดสมุดรายวันที่มีสินทรัพย์ แล้วจากนั้น เลือกแท็บ **สินทรัพย์ถาวร**

    แท็บ **สินทรัพย์ถาวร** จะแสดงชนิดของธุรกรรมและสมุดบัญชี โดยค่าเริ่มต้น จะมีการตั้งค่าฟิลด์ **ชนิดธุรกรรม** เป็น **การซื้อสินทรัพย์** และฟิลด์ **สมุดบัญชี** ถูกกำหนดเป็นสมุดบัญชีปัจจุบันสำหรับสินทรัพย์ถาวร

หลังจากที่คุณลงรายการบัญชีสมุดรายวันการรับรู้เริ่มต้น ธุรกรรมจะปรากฏเป็นธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ถาวร ถ้าต้องการดูตารางธุรกรรม ให้ไปที่ **สินทรัพย์ถาวร \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร** เลือกสินทรัพย์ที่เหมาะสม และจากนั้น เลือก **การประเมินค่า** คุณควรเห็นว่าสมุดรายวันการรับรู้เริ่มต้นได้สร้างธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ถาวรที่ระบุ

ขณะนี้สามารถคิดค่าเสื่อมราคาสินทรัพย์ถาวรได้โดยใช้ฟังก์ชันการคิดค่าเสื่อมราคามาตรฐานในสินทรัพย์ถาวร สำหรับข้อมูลเพิ่มเติมเกี่ยวกับค่าเสื่อมราคา ดูที่ [วิธีการคิดค่าเสื่อมราคาและแบบแผนการคิดค่าเสื่อมราคา](../fixed-assets/depreciation-methods-conventions.md)

> [!NOTE]
> ถ้าคุณเชื่อมโยงสินทรัพย์ถาวรกับสัญญาเช่า ปุ่ม **ค่าเสื่อมราคาสินทรัพย์** และ **การด้อยค่าของสินทรัพย์ของสัญญาเช่า** ถูกปิดใช้งานในการเช่าสินทรัพย์ คุณสามารถดูธุรกรรมค่าเสื่อมราคาของสินทรัพย์และการด้อยค่าของสินทรัพย์ของสัญญาเช่าจากสินทรัพย์ถาวรได้ ปุ่ม **ธุรกรรมสินทรัพย์** ซึ่งเปิดฟอร์มการสอบถาม จะถูกปิดใช้งานด้วย นอกจากนี้ คุณยังสามารถเปิดฟอร์มการสอบถาม **ธุรกรรมสินทรัพย์** ในสินทรัพย์ถาวรได้ด้วย  
