---
title: สร้างและกำหนดนโยบายพฤติกรรมต้นทุนสำหรับหน่วยการควบคุมต้นทุน
description: พฤติกรรมต้นทุนคือการจัดประเภทของต้นทุนคงที่หรือต้นทุนผันแปร
author: twheeloc
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 653bfb69c4ca118c700755cb95a6b349d2c6bbad
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735155"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>สร้างและกำหนดนโยบายพฤติกรรมต้นทุนสำหรับหน่วยการควบคุมต้นทุน

[!include [banner](../../includes/banner.md)]

พฤติกรรมต้นทุนคือการจัดประเภทของต้นทุนคงที่หรือต้นทุนผันแปร นโยบายและกฎที่สอดคล้องกันต้องถูกกำหนดให้กับหน่วยการควบคุมต้นทุนสำหรับนโยบายเพื่อให้เริ่มมีผลบังคับใช้ ใช้กระบวนงานนี้เพื่อสร้างนโยบายและกำหนดนโยบายหน่วยควบคุมต้นทุน


## <a name="create-a-cost-behavior-hierarchy"></a>สร้างลำดับชั้นพฤติกรรมต้นทุน
1. ไปยัง **การบัญชีต้นทุน > มิติ > ลำดับชั้นของมิติ**
2. คลิก **สร้าง**
3. คลิก **สร้าง**
4. ในฟิลด์ **ชื่อลำดับชั้นมิติ** พิมพ์ 'ลำดับชั้นพฤติกรรมต้นทุน'
5. ในฟิลด์ **มิติ** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * เลือกองค์ประกอบต้นทุน  
6. คลิก **บันทึก**
7. คลิก **ดูลำดับชั้น**
8. คลิก **สร้าง**
9. ในฟิลด์ **ชื่อโหนด** ให้พิมพ์ค่า
    * ป้อนอัตราคงที่  
10. ในแผนภูมิ เลือก 'ลำดับชั้นพฤติกรรมต้นทุน'
11. คลิก **สร้าง**
12. ในฟิลด์ **ชื่อโหนด** ให้พิมพ์ค่า
    * ป้อนต้นทุนผันแปร  
13. คลิก **บันทึก**
14. ในแผนภูมิ เลือก 'ลำดับชั้นพฤติกรรมต้นทุน\ต้นทุนคงที่'
15. คลิก **สร้าง**
16. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
17. ในฟิลด์ **สมาชิกมิติเริ่มต้น** ให้ป้อนหรือเลือกค่า
    * ช่วงของสมาชิกมิติอาจประกอบด้วยช่องว่าง แต่สมาชิกจะต้องไม่ทับซ้อนกัน  
18. ในฟิลด์ **สมาชิกมิติสิ้นสุด** ให้ป้อนหรือเลือกค่า
    * ช่วงของสมาชิกมิติอาจประกอบด้วยช่องว่าง แต่สมาชิกจะต้องไม่ทับซ้อนกัน  
19. ในแผนภูมิ เลือก 'ลำดับชั้นพฤติกรรมต้นทุน\ต้นทุนผันแปร'
20. คลิก **สร้าง**
21. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
22. ในฟิลด์ **สมาชิกมิติเริ่มต้น** ให้ป้อนหรือเลือกค่า
    * ช่วงของสมาชิกมิติอาจประกอบด้วยช่องว่าง แต่สมาชิกจะต้องไม่ทับซ้อนกัน  
23. ในฟิลด์ **สมาชิกมิติสิ้นสุด** ให้ป้อนหรือเลือกค่า
    * ช่วงของสมาชิกมิติอาจประกอบด้วยช่องว่าง แต่สมาชิกจะต้องไม่ทับซ้อนกัน  
24. คลิก **บันทึก**

## <a name="create-the-policy-and-rules"></a>สร้างนโยบายและกฎ
1. ไปที่ **การบัญชีต้นทุน > นโยบาย > นโยบายพฤติกรรมต้นทุน**
2. คลิก **สร้าง**
3. ในฟิลด์ **ชื่อนโยบาย** ให้พิมพ์ค่า
4. ในฟิลด์ **ลำดับชั้นมิติองค์ประกอบต้นทุน** ให้ป้อนหรือเลือกค่า
    * เลือกลำดับชั้นของนโยบายที่คุณเพิ่งสร้างขึ้น  
5. ในฟิลด์ **ลำดับชั้นมิติออบเจ็กต์ต้นทุน** ให้ป้อนหรือเลือกค่า
    * เลือกองค์กร  
6. คลิก **บันทึก**
7. คลิก **สร้าง**
8. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
9. ในฟิลด์ **โหนดลำดับชั้นมิติองค์ประกอบต้นทุน** ให้ป้อนหรือเลือกค่า
    * ขยายทั้งลำดับชั้นเพื่อเลือกต้นทุนผันแปร  
10. ในฟิลด์ **โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน** ให้ป้อนหรือเลือกค่า
    * โดยค่าเริ่มต้น เปอร์เซ็นต์ผันแปรเท่ากับ 100 เปอร์เซ็นต์  
11. คลิก **การกำหนดนโยบายสำหรับหน่วยควบคุมต้นทุน**
12. คลิก **สร้าง**
13. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
14. ในฟิลด์ **มีผลบังคับใช้นับจากวันที่ทางการบัญชี** ให้ป้อนวันที่
    * กฎมีผลบังคับวันที่ และผู้ใช้หรือระบบอาจยกเลิกการใช้กฎได้ถ้ามีการสร้างเวอร์ชันใหม่  
15. ในฟิลด์ **หน่วยการควบคุมต้นทุน** ให้ป้อนหรือเลือกค่า
16. คลิก **บันทึก**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
