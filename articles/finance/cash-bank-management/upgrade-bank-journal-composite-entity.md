---
title: อัพเดตเอนทิตี้โดยรวมของสมุดรายวันธนาคาร
description: จำเป็นต้องดำเนินตามขั้นตอนต่อไปนี้เพื่อเพิ่มฟิลด์ BankTransactionType เพิ่มเติมไปยัง BankJournalEntity โดยรวม
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6c990208f26dde26b7adc306198f7cd16e0e69b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978925"
---
# <a name="update-the-bank-journal-composite-entity"></a>อัพเดตเอนทิตี้โดยรวมของสมุดรายวันธนาคาร

[!include [banner](../includes/banner.md)]

จำเป็นต้องดำเนินตามขั้นตอนต่อไปนี้เพื่อเพิ่มฟิลด์ BankTransactionType เพิ่มเติมไปยัง BankJournalEntity โดยรวม

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




