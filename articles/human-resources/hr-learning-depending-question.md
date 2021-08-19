---
title: กำหนดคำถามโดยขึ้นอยู่กับคำตอบของคำถามก่อนหน้านี้
description: 'คำถามแบบมีเงื่อนไขอนุญาตให้คุณสามารถระบุคำถามที่ติดตามเพื่อผลจากผู้ตอบ โดยอาศัยคำตอบของคำถามก่อนหน้านี้ '
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9397b3dfa353398a5d326ae68ec8269369ebf85b7b2e61c73013db76c5dd475
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745705"
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