---
title: สร้างและกำหนดโครงสร้างกฎขั้นสูง
description: บทความนี้อธิบายวิธีการสร้างและกำหนดโครงสร้างกฎขั้นสูงให้กับโครงสร้างทางบัญชี
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72688642936f9428c96aebb34bf9f240dd48b46b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896332"
---
# <a name="create-and-assign-advanced-rule-structures"></a>สร้างและกำหนดโครงสร้างกฎขั้นสูง

[!include [banner](../../includes/banner.md)]

บทความนี้อธิบายวิธีการสร้างและกำหนดโครงสร้างกฎขั้นสูงให้กับโครงสร้างทางบัญชี คำแนะนำนี้ใช้บริษัทสาธิต USMF

## <a name="create-an-advanced-rule-structure"></a>สร้างโครงสร้างกฎขั้นสูง
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > ผังบัญชี > โครงสร้าง > โครงสร้างกฎขั้นสูง**
2. เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง
3. ในฟิลด์ **โครงสร้างกฎขั้นสูง** ให้พิมพ์ชื่อเพื่ออธิบายโครงสร้างกฎ
4. เลือก **ตกลง**
5. เลือก **เพิ่มเซ็กเมนต์**
6. ในรายการเซ็กเมนต์ ให้เลือกมิติทางการเงิน ตัวอย่างเช่น **ร้านค้า**  
7. เลือก **เพิ่มเซ็กเมนต์**
8. เลือก **เปิดใช้งาน**

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>ใช้โครงสร้างกฎขั้นสูงเพื่อโครงสร้างทางบัญชี
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > ผังบัญชี > โครงสร้าง > ตั้งค่าคอนฟิกโครงสร้างทางบัญชี**
2. ในรายการ ให้ค้นหาและเลือกโครงสร้างทางบัญชีที่คุณต้องการนำกฎขั้นสูงไปใช้
3. เลือก **แก้ไข** นอกจากนี้ คุณสามารถเลือก **กฎขั้นสูง** และระบบจะขอให้คุณวางโครงสร้างทางบัญชีใน **โหมดแบบร่าง**  
4. เลือก **กฎขั้นสูง**
5. เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง
6. ในฟิลด์ **กฎชั้นสูง** ให้พิมพ์ค่าใดค่าหนึ่ง
7. ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง
8. เลือก **สร้าง**
9. คลิก **เพิ่มเกณฑ์ใหม่**
10. ในฟิลด์ **สถานที่** ให้เลือกบัญชีหลักหรือมิติทางการเงิน
11. ในฟิลด์ **ผู้ปฏิบัติงาน** ให้เลือกตัวเลือก เช่น **อยู่ระหว่าง** และ **ประกอบด้วย**
12. ในฟิลด์ **ค่า** ให้พิมพ์ค่าใดค่าหนึ่ง
13. ในฟิลด์ **ผ่าน** ให้พิมพ์ค่าใดค่าหนึ่ง
14. เลือก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง
15. ในรายการ ให้ค้นหาโครงสร้างกฎขั้นสูงที่คุณต้องการใช้เมื่อคุณพบเงื่อนไขที่ป้อนเข้าไป
16. เลือก **เพิ่ม**
17. ปิดหน้า
18. เลือก **เปิดใช้งาน**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
