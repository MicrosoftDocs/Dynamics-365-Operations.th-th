---
title: การสร้างเท็มเพลตเวลาการทำงาน
description: เท็มเพลตเวลาการทำงานกำหนดชั่วโมงการทำงานตลอดทั้งสัปดาห์ และใช้เพื่อสร้างระยะเวลาทำงานแบบเป็นช่วงเวลา
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e8e43900fd25f0051124d761dc7b06d4f9313a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006828"
---
# <a name="create-working-time-templates"></a>การสร้างเท็มเพลตเวลาการทำงาน

[!include [banner](../../includes/banner.md)]

เท็มเพลตเวลาการทำงานกำหนดชั่วโมงการทำงานตลอดทั้งสัปดาห์ และใช้เพื่อสร้างระยะเวลาทำงานแบบเป็นช่วงเวลา ขั้นตอนนี้แสดงวิธีการกำหนดเท็มเพลตเวลาการทำงานโดยใช้เวลาทำงานที่จัดสรรตามคุณสมบัติสำหรับการจัดประเภทช่วงเวลาทำงาน  คุณสามารถดำเนินการขั้นตอนนี้ได้ในข้อมูลสาธิตของบริษัท USMF หรือการใช้ข้อมูลของคุณเอง

1. ไปที่พื้นที่ทำงานทั้งหมด > การจัดการรอบการใช้งานทรัพยากร 
2. คลิกเท็มเพลตเวลาการทำงาน 

## <a name="create-working-time-template"></a>สร้างเท็มเพลตเวลาทำงาน
1. คลิก สร้าง
2. ในฟิลด์เท็มเพลตเวลาการทำงาน พิมพ์มูลค่า 
3. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
4. ขยายส่วนวันจันทร์ 
5. คลิก เพิ่ม
6. ในฟิลด์ตั้งแต่ ให้ป้อนเวลา
    * ระบุเวลาเริ่มทำงานในตอนเช้า  
7. ในฟิลด์จนถึง ให้ป้อนเวลา 
    * ระบุเวลาที่พนักงานพักกลางวัน  
8. คลิก เพิ่ม
9. ในฟิลด์ตั้งแต่ ให้ป้อนเวลา
    * ระบุเวลาที่เริ่มทำงานหลังจากพักกลางวัน  
10. ในฟิลด์จนถึง ให้ป้อนเวลา 
    * ระบุการสิ้นสุดของวันทำงาน  

## <a name="replicate-working-times-to-all-week-days"></a>ใช้เวลาทำงานนี้กับวันทำการทั้งหมด
1. คลิกคัดลอกวัน
    * คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงวันอังคาร  
2. คลิก ตกลง
3. คลิกคัดลอกวัน
    * คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงวันพุธ  
4. ในฟิลด์จนถึงวันทำการ ให้เลือกตัวเลือก 
5. คลิก ตกลง
6. คลิกคัดลอกวัน
    * คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงวันพฤหัสบดี  
7. ในฟิลด์จนถึงวันทำการ ให้เลือกตัวเลือก 
8. คลิก ตกลง
9. คลิกคัดลอกวัน
    * คัดลอกขอบเขตของเวลาในการทำงานตั้งแต่วันจันทร์ถึงศุกร์  
10. ในฟิลด์จนถึงวันทำการ ให้เลือกตัวเลือก 
11. คลิก ตกลง

## <a name="define-time-slots-for-special-operations"></a>กำหนดช่วงเวลาสำหรับการดำเนินงานพิเศษ
1. ขยายส่วนวันศุกร์
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
3. ในฟิลด์คุณสมบัติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
5. ในฟิลด์คุณสมบัติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง 

## <a name="mark-weekend-days-as-closed-for-pickup"></a>ทำเครื่องหมายในวันสุดสัปดาห์เป็นปิดการเบิกสินค้า
1. ขยายส่วนวันเสาร์ 
2. เลือกใช่ในฟิลด์ปิดการเบิกสินค้า 
3. ขยายส่วนวันอาทิตย์ 
4. เลือกใช่ในฟิลด์ปิดการเบิกสินค้า 

