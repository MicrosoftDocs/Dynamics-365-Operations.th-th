---
title: สร้างแหล่งปฏิบัติงาน
description: 'ทรัพยากรการดำเนินงานดำเนินการกิจกรรมของโครงการหรือกระบวนการผลิต '
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b91d5ea7618010ab9d4006d643c59a7f995eb0c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981250"
---
# <a name="create-an-operations-resource"></a>สร้างแหล่งปฏิบัติงาน

[!include [banner](../../includes/banner.md)]

ทรัพยากรการดำเนินงานดำเนินการกิจกรรมของโครงการหรือกระบวนการผลิต  กระบวนงานนี้แสดงถึงวิธีการกำหนดทรัพยากรการดำเนินงาน  คุณสามารถดำเนินการขั้นตอนนี้ได้ในข้อมูลสาธิตของบริษัท USMF หรือการใช้ข้อมูลของคุณเอง

1. ไปที่ทรัพยากร
2. คลิก สร้าง
3. ในฟิลด์ทรัพยากร ให้พิมพ์ค่าใดค่าหนึ่ง
4. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า

## <a name="define-capacity-and-consumption-parameters"></a>กำหนดพารามิเตอร์กำลังการผลิตและปริมาณการใช้
1. ขยายส่วนการดำเนินงาน
2. ในฟิลด์เปอร์เซ็นต์ของเสีย ให้ป้อนหมายเลข 
3. ในฟิลด์ประเภทการตั้งค่า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * ระบุประเภทต้นทุนซึ่งกำหนดวิธีตั้งค่าสำหรับการลงบัญชีต้นทุน  
4. ในฟิลด์ประเภทเวลาที่ใช้ในการผลิต ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * ระบุประเภทต้นทุนซึ่งกำหนดวิธีการลงบัญชีต้นทุนของเวลาการดำเนินการ  
5. ในฟิลด์ประเภทปริมาณ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * ระบุประเภทต้นทุนซึ่งกำหนดวิธีการลงบัญชีสำหรับต้นทุนทรัพยากรที่ขึ้นอยู่กับปริมาณผลผลิต  
6. ในฟิลด์หน่วยกำลังการผลิต ให้เลือกหนึ่งตัวเลือก
    * ระบุหน่วยที่แสดงกำลังการผลิตของทรัพยากรการดำเนินงาน  
7. ในฟิลด์กำลังการผลิต ให้ป้อนตัวเลข
8. ในฟิลด์เปอร์เซ็นต์ประสิทธิภาพ ให้ป้อนหมายเลข
    * ระบุประสิทธิภาพที่คุณคาดหวังจากทรัพยากรการดำเนินงาน  เปอร์เซ็นต์ประสิทธิภาพปรับปริมาณที่สามารถประมวลผลได้ของทรัพยากรการดำเนินงาน และมีผลกระทบต่อเวลาที่ถูกจองไว้สำหรับทรัพยากร  
9. ในฟิลด์เปอร์เซ็นต์การจัดตารางการผลิตระดับการดำเนินงาน ให้ป้อนหมายเลข 
    * ระบุเปอร์เซ็นต์สูงสุดของกำลังการผลิตของทรัพยากรการดำเนินงานที่คุณต้องการใช้ในการจัดตารางการผลิตระดับการดำเนินงาน  
10. เลือกใช่ในฟิลด์กำลังการผลิตที่มีจำกัด
    * ตั้งค่าตัวเลือกนี้เป็นใช่ ถ้าทรัพยากรการดำเนินงานควรถูกกำหนดตามกำลังการผลิตที่แท้จริงที่พร้อมใช้งาน และถ้าการจองกำลังการผลิตที่มีอยู่ควรได้รับการพิจารณา  ถ้าตัวเลือกนี้จะตั้งค่าเป็นไม่ ทรัพยากรการดำเนินงานจะถูกถือว่ามีกำลังการผลิตมีไม่จำกัด และทรัพยากรอาจถูกจองเกินเวลา  
11. เลือกใช่ในฟิลด์ทรัพยากรที่ติดขัด

## <a name="define-working-times"></a>กำหนดเวลาทำงาน
1. ขยายส่วนปฏิทิน
2. คลิก เพิ่ม
3. ในฟิลด์ปฏิทิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * ระบุปฏิทินเวลาการทำงานที่กำหนดกำลังการผลิตของทรัพยากร (ในหน่วยชั่วโมง)  
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
5. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก

## <a name="define-resource-capabilities"></a>กำหนดความสามารถของทรัพยากร
1. ขยายส่วนความสามารถ
2. คลิก เพิ่ม
    * ความสามารถคือ ความสามารถของทรัพยากรการดำเนินงานในการดำเนินการกิจกรรมที่เฉพาะ  กลไกจัดการการจัดกำหนดการได้จัดสรรทรัพยากร โดยจัดให้ตรงกับความต้องการทรัพยากรของกิจกรรมแต่ละกิจกรรมกับความสามารถของทรัพยากรการดำเนินงานที่พร้อมใช้งาน  
3. ในฟิลด์ความสามารถ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
4. ในฟิลด์ระดับ ให้ป้อนตัวเลข
    * ระบุระดับของประสิทธิภาพโดยที่ทรัพยากรจะประมวลผลความสามารถ  
5. ในฟิลด์ระดับความสำคัญ ให้ป้อนตัวเลข
    * ระบุระดับความสำคัญของทรัพยากรการดำเนินงานเกี่ยวข้องกับความสามารถ  เมื่อต้องการจัดกำหนดการตามระดับความสำคัญ ทรัพยากรการดำเนินงานที่มีความสำคัญสูงสุดจะถูกเลือกก่อน (ตัวเลขค่าต่ำสุด)  

## <a name="assign-resource-to-resource-group"></a>กำหนดทรัพยากรให้กับกลุ่มทรัพยากร
1. ขยายส่วนกลุ่มทรัพยากร
2. คลิก เพิ่ม
    * กลุ่มทรัพยากรกำหนดไซต์ หน่วยการผลิต และบริบทคลังสินค้าสำหรับทรัพยากรการดำเนินงาน  สามารถจัดกำหนดการทรัพยากรการดำเนินงานได้เฉพาะเมื่อกำหนดให้กับกลุ่มทรัพยากร และบนไซต์ที่เป็นที่ตั้งของกลุ่มทรัพยากรเท่านั้น  
3. ในฟิลด์กลุ่มทรัพยากร ให้ป้อนหรือเลือกค่า
4. ในฟิลด์ที่ตั้งอินพุท ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * ระบุที่ตั้งคลังสินค้าเริ่มต้นจากที่ทรัพยากรการดำเนินงานกำลังใช้งานวัตถุดิบ  

