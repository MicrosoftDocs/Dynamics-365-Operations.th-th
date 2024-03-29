---
title: ป้อนข้อมูลผู้สมัครและแอปพลิเคชันด้วยตนเอง
description: 'ขั้นตอนนี้แสดงวิธีการรักษาข้อมูลเกี่ยวกับผู้สมัครและใบสมัครของผู้สมัคร '
author: twheeloc
ms.date: 01/10/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d59b5a2c99813fee2e12e30e8694edf6da7391d9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909262"
---
# <a name="enter-applicant-and-application-data-manually"></a>ป้อนข้อมูลผู้สมัครและแอปพลิเคชันด้วยตนเอง

> [!NOTE]
> ฟังก์ชันการสรรหาบุคลากรในบทความนี้จะเรียกว่าโครงการสรรหาบุคลากร และมุ่งเน้นที่ผู้สมัคร ใบสมัคร และโครงการสรรหาบุคลากร  


ขั้นตอนนี้แสดงวิธีการรักษาข้อมูลเกี่ยวกับผู้สมัครและใบสมัครของผู้สมัคร  คุณสามารถป้อน และรักษาข้อมูลส่วนบุคคล วันนัดสัมภาษณ์ และเวลา การอ้างอิง ความสามารถ และคำขอที่พักสำหรับผู้สมัคร  นอกจากนี้ คุณยังสามารถปรับปรุงสถานะของใบสมัครของผู้สมัครสำหรับการจ้างงาน และสร้างจดหมายหรือข้อความอีเมลเพื่อสื่อสารกับผู้สมัครได้ เมื่อคุณสร้างเรกคอร์ดผู้สมัคร เรกคอร์ดบุคคลสำหรับผู้สมัครจะถูกสร้างขึ้นในสมุดที่อยู่สากล บริษัทข้อมูลสาธิต **USMF** ถูกนำมาใช้ในการสร้างกระบวนงานนี้

## <a name="create-a-new-applicant-record"></a>สร้างเรกคอร์ดผู้สมัครใหม่

1. ไปที่ **ทรัพยากรบุคคล \> การสรรหาบุคคลากร \> ผู้สมัคร \> ผู้สมัคร**
2. เลือก **ใหม่**
3. ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง
4. ในฟิลด์ **นามสกุล** ให้ป้อนค่า

    คุณสามารถป้อนข้อมูลผู้สมัครเพิ่มเติมถ้าพร้อมใช้งาน  ตัวอย่างเช่น ข้อมูลนี้สามารถรวมถึง ระดับการศึกษาสูงสุดของผู้สมัคร ตำแหน่งงานปัจจุบัน หรือนายจ้างก่อนหน้านี้

5. ขยายส่วน **ข้อมูลผู้ติดต่อ**
6. เลือก **เพิ่ม**
7. ในฟิลด์ **คำอธิบาย** ให้ป้อน **อีเมลที่ใช้ในการสื่อสาร**
8. ในฟิลด์ **ชนิด**  ให้เลือกหนึ่งตัวเลือก
9. ในฟิลด์ **หมายเลข/ที่อยู่ผู้ติดต่อ** ให้ป้อนค่าใดค่าหนึ่ง

    ที่อยู่ของอีเมลนี้จะใช้ในการสร้างข้อความอีเมลสื่อสารกับผู้สมัคร

10. เลือก **เพิ่ม**
11. ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า
12. ในฟิลด์ **หมายเลข/ที่อยู่ผู้ติดต่อ** ให้ป้อนค่าใดค่าหนึ่ง

    ใช้ฟิลด์นี้เพื่อป้อนข้อมูลส่วนบุคคลเพิ่มเติมเกี่ยวกับผู้สมัคร ตามที่ต้องการ ตัวอย่างเช่น ข้อมูลนี้สามารถรวมถึงวันเกิด เชื้อชาติ เพศ หรือสถานภาพการสมรสของผู้สมัคร

13. บนบานหน้าต่างการดำเนินการ เลือก **ความสามารถ**

    คุณสามารถป้อนโพรไฟล์ความสามารถของผู้สมัคร รวมทั้งทักษะของพวกเขา ประสบการณ์ทำงาน การศึกษา แบบทดสอบ หรือประกาศนียบัตร ข้อมูลนี้สามารถใช้วางแผนทักษะของผู้สมัครเพื่อทักษะที่เชื่อมโยงกับงานกำหนดไว้ในข้อมูลของบริษัทของคุณ

## <a name="create-an-application-for-the-applicant"></a>สร้างใบสมัครสำหรับผู้สมัคร

1. เลือก **ใบสมัคร**
2. เลือก **ใหม่**
3. ในฟิลด์ **โครงการสรรหาบุคลากร** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา

    การเลือกโครงการสรรหาบุคลากรทำให้คุณสามารถตรวจสอบว่าผู้สมัครจะเชื่อมโยงกับการเปิดเฉพาะที่รวมอยู่ในโครงการสรรหาบุคลากรหรือไม่

4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
5. ในรายการนี้ ให้เลือกลิงก์ในแถวที่เลือก

    โดยค่าเริ่มต้น งานและแผนกขึ้นอยู่กับโครงการสรรหาบุคลากรที่เลือก

6. เลือก **บันทึก**

    หลังจากที่คุณบันทึกใบสมัครแล้ว คุณสามารถแนบเอกสารกับใบสมัครได้ เอกสารเหล่านี้อาจรวมประสบการณ์ รางวัล และจดหมายปะหน้าของผู้สมัครด้วย

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
