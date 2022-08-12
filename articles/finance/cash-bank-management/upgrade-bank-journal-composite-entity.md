---
title: อัปเดตเอนทิตี้โดยรวมของสมุดรายวันธนาคาร
description: บทความนี้แสดงรายการตามขั้นตอนต่อไปนี้เพื่อเพิ่มฟิลด์ BankTransactionType เพิ่มเติม ไปยัง BankJournalEntity โดยรวม
author: angelad116
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f8bf3bbcbd8036015757799a2e58b23fd9bd2b38
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151624"
---
# <a name="update-the-bank-journal-composite-entity"></a>อัปเดตเอนทิตี้โดยรวมของสมุดรายวันธนาคาร

[!include [banner](../includes/banner.md)]

บทความนี้แสดงรายการตามขั้นตอนต่อไปนี้เพื่อเพิ่มฟิลด์ BankTransactionType เพิ่มเติม ไปยัง BankJournalEntity โดยรวม

ใช้ขั้นตอนต่อไปนี้เพื่อเพิ่มฟิลด์ BankTransactionType เพิ่มเติมไปยัง BankJournalEntity โดยรวม

1.  คอมไพล์และซิงโครไนส์เอนทิตี้โดยรวมของสมุดรายวันธนาคาร เอนทิตี้ และตารางการจัดเตรียมต่อไปนี้:
    -   เอนทิตี้แบบรวม\\BankJournalEntity
    -   เอนทิตี้\\BankJournalHeaderEntity
    -   เอนทิตี้\\BankJournalLineEntity
    -   ตาราง\\BankJournalHeaderStaging
    -   ตาราง\\BankJournalLineStaging

2.  การจัดการข้อมูล\\โครงการข้อมูล
    -   แสดงข้อมูลชนิด **ธุรกรรมธนาคาร** บนโครงร่าง **ข้อมูลต้นทาง**
        -   รูปแบบข้อมูลต้นทาง = XML-Element
        -   ชื่อเอนทิตี้ = สมุดรายวันธนาคาร
        -   อัพโหลดไฟล์ข้อมูล = SampleBankJournalCompositeEntity.xml เวอร์ชันใหม่
        -   คลิก **ใช่** เพื่อบันทึกทับไฟล์ที่มีอยู่
        -   คลิก **ใช่** เพื่อสร้างการแม็ปตั้งแต่ต้น
        -   ตรวจสอบว่ามีการแม็ปชนิดธุรกรรมธนาคารหรือไม่
            -   คลิก **ดูแผนที่** บนเอนทิตี้ของรายการ
            -   ตรวจสอบว่ามีการแม็ปชนิดธุรกรรมธนาคารจากต้นทางไปยังการแบ่งระยะหรือไม่

3.  นำเข้าใบแจ้งยอดใหม่






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
