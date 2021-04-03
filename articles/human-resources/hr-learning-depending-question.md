---
title: กำหนดคำถามโดยขึ้นอยู่กับคำตอบของคำถามก่อนหน้านี้
description: 'คำถามแบบมีเงื่อนไขอนุญาตให้คุณสามารถระบุคำถามที่ติดตามเพื่อผลจากผู้ตอบ โดยอาศัยคำตอบของคำถามก่อนหน้านี้ '
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a76220647417b6ff69e2f0ab5b2fa5297db5c49
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467854"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>กำหนดคำถามโดยขึ้นอยู่กับคำตอบของคำถามก่อนหน้านี้

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



คำถามแบบมีเงื่อนไขอนุญาตให้คุณสามารถระบุคำถามที่ติดตามเพื่อผลจากผู้ตอบ โดยอาศัยคำตอบของคำถามก่อนหน้านี้  ตัวอย่างเช่น ถ้าคุณถามถึง "คุณชอบกาแฟหรือชามากกว่ากัน" คำถามการติดตามผลแบบมีตรรกะจะถูกกำหนดโดยขึ้นอยู่กับว่าผู้ตอบเลือกกาแฟหรือชาเป็นคำตอบของตน  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF


## <a name="find-the-existing-questionnaire"></a>ค้นหาแบบสอบถามที่มีอยู่
1. ไปที่แบบสอบถาม > การออกแบบ > แบบสอบถาม
2. ในรายการนี้ ให้เลือกแบบสอบถาม WorkFH

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>เพิ่มคำถามและคำถามย่อยทั้งหมดลงในแบบสอบถาม
1. คลิกคำถาม
2. คลิก สร้าง
3. ในฟิลด์คำถาม ให้เลือกคำถามหมายเลข 00016
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
5. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
6. คลิก บันทึก
7. ปิดหน้า

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>ตั้งค่าลำดับแบบสอบถามเป็นแบบมีเงื่อนไข และกำหนดคำถามให้เหมาะสม
1. คลิก แก้ไข
2. ขยายส่วนการตั้งค่า
3. ในฟิลด์คำถาม ให้เลือก'มีเงื่อนไข'
4. คลิกคำถามแบบมีเงื่อนไข
5. ในแผนภูมิ เลือก 'คำถาม\อธิบายว่าเพราะเหตุใดคุณถึงตอบคำถามก่อนหน้าแบบนั้น'
6. ในฟิลด์คำถามหลัก ให้เลือกคำถามหมายเลข 00009
7. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
8. ในฟิลด์คำตอบ ให้เรียงลำดับคำตอบโดยขึ้นอยู่กับตัวเลือกคำตอบที่คุณต้องการกำหนดคำถาม  ตัวอย่างเช่น ป้อน 1 สำหรับตัวเลือกคำตอบแรก
9. คลิกบันทึก
10. ในแผนภูมิ เลือก 'คำถาม\ฉันได้รับเงินเดือนพอประมาณสำหรับงานที่ฉันทำ'
    * โปรดสังเกตว่า แผนภูมิคำถามการอัพเดตเพื่อแสดงการขึ้นต่อกัน  



[!INCLUDE[footer-include](../includes/footer-banner.md)]