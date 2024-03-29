---
title: สร้างและกำหนดนโยบายการกระจายต้นทุนสำหรับหน่วยการควบคุมต้นทุน
description: กฎการกระจายต้นทุนถูกใช้เพื่อกระจายต้นทุนที่มีการตรวจนับทางการเงินในศูนย์ต้นทุนรวม
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: CAMCostDistributionRule
ms.openlocfilehash: 23adea279cad3fcf69cc6926d6f8dee485150221
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272412"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>สร้างและกำหนดนโยบายการกระจายต้นทุนสำหรับหน่วยการควบคุมต้นทุน

[!include [banner](../../includes/banner.md)]

กฎการกระจายต้นทุนถูกใช้เพื่อกระจายต้นทุนที่มีการตรวจนับทางการเงินในศูนย์ต้นทุนรวม นักบัญชีต้นทุนตรวจสอบให้แน่ใจว่ามีการกระจายต้นทุนไปยังศูนย์ต้นทุนโดยขึ้นอยู่กับฐานการปันส่วนที่เลือก นโยบายและกฎที่สอดคล้องกันถูกกำหนดให้กับหน่วยการควบคุมต้นทุน คู่มืองานนี้ใช้ตัวอย่างในการแสดงวิธีการสร้างนโยบายการกระจายต้นทุนและกฎที่สอดคล้องกัน


## <a name="create-a-policy"></a>สร้างนโยบาย
1. ไปที่ การบัญชีต้นทุน > นโยบาย > นโยบายการกระจายต้นทุน
2. คลิก สร้าง
3. ในฟิลด์ชื่อนโยบาย ให้พิมพ์ค่า
4. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
5. ในฟิลด์ลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า
    * เลือกองค์กร  
6. ในฟิลด์ลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า
    * เลือก CDS P/L  
7. ในฟิลด์มิติทางสถิติ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * เลือก องค์ประกอบทางสถิติ  
8. คลิก บันทึก

## <a name="create-rules-for-the-policy"></a>สร้างกฎสำหรับนโยบาย
1. คลิก สร้าง
2. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
3. ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า
    * ขยายทั้งลำดับชั้นเพื่อเลือก 094  
4. ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า
    * เลือกค่าใช้จ่ายการดำเนินงานอื่น และจากนั้นเลือกการทำความสะอาด 605110  
5. ในฟิลด์พฤติกรรมต้นทุน ให้เลือกหนึ่งตัวเลือก
    * เลือก ต้นทุนคงที่  
6. ในฟิลด์ฐานการปันส่วน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
7. คลิก สร้าง
8. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
9. ในฟิลด์โหนดลำดับชั้นมิติออบเจ็กต์ต้นทุน ให้ป้อนหรือเลือกค่า
    * ขยายทั้งลำดับชั้นเพื่อเลือก 094  
10. ในฟิลด์โหนดลำดับชั้นมิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า
    * เลือกค่าใช้จ่ายการดำเนินงานอื่น และจากนั้นเลือก 605150 ค่าเช่า  
11. ในฟิลด์พฤติกรรมต้นทุน ให้เลือกหนึ่งตัวเลือก
    * เลือก ต้นทุนคงที่  
12. ในฟิลด์ฐานการปันส่วน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
13. คลิก บันทึก

## <a name="assign-rules-to-a-cost-control-unit"></a>กำหนดกฎให้กับหน่วยการควบคุมต้นทุน
1. คลิก การกำหนดนโยบายสำหรับหน่วยควบคุมต้นทุน
2. คลิก สร้าง
3. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
4. ในฟิลด์ มีผลบังคับใช้นับจากวันที่ทางการบัญชี ให้ป้อนวันที่
    * เลือก วันที่ 1 กันยายนในปีบัญชีที่ถูกต้อง  
5. ในฟิลด์หน่วยการควบคุมต้นทุน ให้ป้อนหรือเลือกค่า
6. คลิก บันทึก



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
