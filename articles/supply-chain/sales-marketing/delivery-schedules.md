---
title: กำหนดการจัดส่ง
description: กำหนดการจัดส่งช่วยให้คุณสามารถติดตามปริมาณในบรรทัดใบสั่งเมื่อคุณใช้การจัดส่งหลายครั้ง สำหรับใบสั่งขาย ใบเสนอราคาขาย ใบสั่งซื้อเดียว
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b50558c5da71351082d36276a3185e1f91543f2b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573476"
---
# <a name="delivery-schedules"></a>กำหนดการจัดส่ง

[!include [banner](../includes/banner.md)]

กำหนดการจัดส่งช่วยให้คุณสามารถติดตามปริมาณในบรรทัดใบสั่งเมื่อคุณใช้การจัดส่งหลายครั้ง สำหรับใบสั่งขาย ใบเสนอราคาขาย ใบสั่งซื้อเดียว

ใช้กำหนดการจัดส่งเมื่อปริมาณในรายการใบสั่งหรือใบเสนอราคาทั้งหมดต้องถูกจัดส่งในการจัดส่งหลายครั้ง การจัดส่งแต่ละครั้งจะแสดงรายการจัดส่ง รายการการจัดส่งอย่างน้อยสองรายการจะทำให้เป็นกำหนดการการจัดส่งเดียว รายการจัดส่งสามารถมีวันจัดส่ง ปริมาณ วิธีการจัดส่ง และมิติการจัดเก็บ ที่แตกต่างกัน เช่น ไซต์และคลังสินค้า  

**ตัวอย่างของกำหนดการจัดส่ง**

| สินค้า                              | มูลค่า                                    |
|-----------------------------------|------------------------------------------|
| ใบสั่งรวม (รายการใบสั่งต้นฉบับ) | เก้าอี้ 600 ตัว                               |
| กำหนดวันจัดส่งที่ร้องขอ:       | เก้าอี้ 100 ตัวต่อเดือน                     |
| กรอบเวลาจัดส่งที่ร้องขอ | 6 เดือน ในวันแรกของแต่ละเดือน |

ในสถานการณ์นี้ ลูกค้าร้องขอการจัดส่งของเก้าอี้ 600 ตัว ในชุดงานของเก้าอี้ 100 ตัว เกินรอบระยะเวลาหกเดือน การติดตามความต้องการจัดส่ง คุณต้องสร้างกำหนดการจัดส่ง ในหน้ากำหนดการจัดส่ง คุณสร้างรายการจัดส่งแยกต่างหากหกรายการ แต่ละรายการการจัดส่งประกอบด้วยเก้าอี้ 100 ตัว และระบุวันจัดส่งสำหรับเก้าอี้ 100 ตัวเหล่านั้น ในกรณีนี้ แต่ละรายการออฟเซ็ตในวันที่หนึ่งของเดือนสำหรับหกเดือนที่ต่อเนื่องกัน  

เมื่อคุณสร้างการจัดกำหนดการจัดส่ง ชนิดของรายการใบสั่งดั้งเดิมจะถูกเปลี่ยนโดยอัตโนมัติเป็น **รายการสั่งที่มีการจัดส่งหลายครั้ง** รายการชนิดนี้จะถูกอ้างถึงเป็นรายการการค้า และถูกทำเครื่องหมายด้วยไอคอน รายการจัดส่งถูกทำเครื่องหมายด้วยไอคอน ถ้าคุณเปลี่ยนปริมาณในรายการจัดส่ง รายการการค้าถูกอัพเดตเป็นปริมาณรวมของกำหนดการจัดส่ง ถ้าข้อตกลงทางการค้ามีกำหนดส่วนลดรวมสำหรับใบสั่ง กำหนดการจัดส่งจะช่วยให้มั่นใจว่าใบสั่งของคุณมีสิทธิ์ได้รับส่วนลดรวมในใบสั่ง แม้ว่าใบสั่งจะมีการแยกการจัดส่งก็ตาม  

ใบสั่งที่มีกำหนดการจัดส่งทีถูกประมวลผลแล้วสำหรับรายการการจัดส่ง การประมวลผลรวมถึงการลงรายการบัญชีบันทึกการจัดส่ง ใบรับสินค้า และการออกใบแจ้งหนี้  

พิมพ์เอกสารของใบสั่งและใบเสนอราคาที่มีกำหนดการจัดส่งแสดงเฉพาะรายการจัดส่ง ซึงจะไม่แสดงรายการเดิม (รายการการค้า) **หมายเหตุ:** นอกจากนี้ ระบบจะแสดงเฉพาะรายการจัดส่งเมื่อคุณทำการดำเนินการเหล่านี้:

-   โพสต์
-   คัดลอกหน้า
-   เลือกดูหน้ารายการและรายงาน

เมื่อคุณยืนยันใบเสนอราคาขาย ผลลัพธ์ใบสั่งขายจะแสดงกำหนดการจัดส่งทั้งหมด แม้แต่รายการใบสั่งที่มีการจัดส่งหลายครั้ง นอกจากนี้ กำหนดการจัดส่งทั้งหมดจะแสดงขึ้นในหน้าทั้งหมดหลัก เช่น ใบสั่งขาย ใบเสนอราคาขาย ใบสั่งซื้อ





[!INCLUDE[footer-include](../../includes/footer-banner.md)]