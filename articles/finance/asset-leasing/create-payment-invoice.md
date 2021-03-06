---
title: สร้างใบแจ้งหนี้การชำระเงิน
description: หัวข้อนี้อธิบายวิธีการสร้างใบแจ้งหนี้ค่าเช่ารายเดือน คุณสามารถสร้างใบแจ้งหนี้สำหรับการเช่าแต่ละครั้ง หรือคุณสามารถใช้กระบวนการชุดงานเพื่อสร้างใบแจ้งหนี้สำหรับการเช่าหลายครั้งได้
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
ms.openlocfilehash: 303fb0e70530fdc29cb129736b01c0e0e8d02075
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969589"
---
# <a name="create-payment-invoices"></a>สร้างใบแจ้งหนี้การชำระเงิน

[!include [banner](../includes/banner.md)]

คุณสามารถสร้างใบแจ้งหนี้รายเดือนสำหรับการเช่าแต่ละครั้ง หรือคุณสามารถใช้กระบวนการชุดงานเพื่อสร้างใบแจ้งหนี้สำหรับการเช่าหลายครั้งได้ ขั้นตอนต่อไปนี้แสดงวิธีการสร้างการชำระค่าเช่าแต่ละรายการเมื่อมีการเปิดใช้งานพารามิเตอร์ **การชำระเงินให้แก่ผู้จัดจำหน่าย** บนหน้า **การตั้งค่าสมุดบัญชีการเช่า**

1. บนหน้า **สรุปการเช่า** เลือกการเช่าที่จะปรับปรุง แล้วเลือก **สมุดบัญชี \> กำหนดการชำระเงิน**
2. เลือกการชำระเงินที่ต้องทำ แล้วเลือก **สร้างสมุดรายวัน** คุณได้รับข้อความแจ้งว่ามีการสร้างสมุดรายวันสำหรับการชำระเงินที่เลือก
3. เลือก **สมุดรายวันใบแจ้งหนี้** แล้วเลือกใบแจ้งหนี้ที่ต้องชำระ
4. บนแท็บ **บรรทัด** ให้ตรวจสอบรายการสมุดรายวันก่อนที่คุณจะลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป

    > [!NOTE]
    > โดยค่าเริ่มต้น บรรทัดใบแจ้งหนี้ของผู้จัดจำหน่ายที่สร้างขึ้นจะใช้โปรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายจากหน้า **พารามิเตอร์บัญชีเจ้าหนี้**

5. เลือกสมุดรายวันที่ถูกต้อง แล้วเลือกใบแจ้งหนี้ที่ต้องชำระ

    สำหรับตัวอย่างนี้ พารามิเตอร์ **การชำระเงินให้แก่ผู้จัดจำหน่าย** เปิดใช้งานในสมุดบัญชีการเช่า ใบแจ้งหนี้จะอยู่ในสมุดรายวันใบแจ้งหนี้ ส่วน **ภาพรวม** แสดงสรุปของรายการสมุดรายวัน และส่วน **บรรทัด** จะแสดงรายละเอียดของบรรทัดสมุดรายวันที่แท้จริง

    > [!NOTE]
    > ถ้ามีการปิดพารามิเตอร์ **การชำระเงินให้แก่ผู้จัดจำหน่าย** รายการสมุดรายวันการชำระเงินจะแสดงรายการอยู่บนหน้า **การเช่าสินทรัพย์** สำหรับสมุดบัญชีการเช่าและระบบจะสร้างรายการเงินประกันสินทรัพย์แทนใบแจ้งหนี้ จะมีการลงรายการบัญชีการชำระค่าเช่าในชื่อสมุดรายวันที่ระบุไว้ในฟิลด์ **สมุดรายวันการเช่ารายเดือน**

6. หลังจากที่มีการลงรายการบัญชีธุรกรรมแล้ว คุณสามารถดูข้อมูลธุรกรรมและมูลค่าตามบัญชีของหนี้สินสัญญาเช่าโดยการเลือก **ธุรกรรมหนี้สิน** ในสมุดบัญชีการเช่า

    ในกำหนดการชำระเงิน กล่องกาเครื่องหมาย **ลงรายการบัญชีสมุดรายวัน** จะถูกเลือก และบรรทัดจะแสดงหมายเลขสมุดรายวันใบแจ้งหนี้ หลังจากที่มีการสร้างสมุดรายวันการชำระเงินและรายการสำหรับสมุดรายวันนั้นแล้ว คุณต้องย้อนกลับรายการก่อนจึงจะสามารถสร้างใหม่ได้
