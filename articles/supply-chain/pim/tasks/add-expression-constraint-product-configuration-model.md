---
title: เพิ่มข้อจำกัดนิพจน์ไปที่แบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีที่คุณสามารถเพิ่มข้อจำกัดนิพจน์ใหม่ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์ '
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77e8b991a2615a8f5d238acc4655f231edb6ca98
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569660"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>เพิ่มข้อจำกัดนิพจน์ไปที่แบบจำลองการจัดโครงแบบผลิตภัณฑ์

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีที่คุณสามารถเพิ่มข้อจำกัดนิพจน์ใหม่ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์  แสดงวิธีการกำหนดว่าการป้องกันมุมต้องใช้กับลำโพง ถ้าผู้ใช้เลือกเป็นตะแกรงด้านหน้าเป็นโลหะ  กระบวนงานใช้ส่วนประกอบลำโพงขั้นสูงในบริษัทสาธิต USMF

## <a name="create-an-expression-constraint"></a>สร้างข้อจำกัดนิพจน์

1. ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**
3. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * ตัวอย่างนี้ใช้แบบจำลองลำโพงระดับสูง  
4. ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก
5. ขยายส่วน **ข้อจำกัด**
6. เลือก **เพิ่ม**
7. เลือก **สร้าง**
8. ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง

## <a name="enter-expression"></a>ป้อนนิพจน์

1. เลือก **แก้ไขนิพจน์**
    * ถ้าคุณปลดล็อคอินเทอร์เฟสผู้ใช้ในงานที่บันทึกไว้ในขั้นตอนนี้ คุณจะสามารถใช้ IntelliSense และรายการของสัญลักษณ์เพื่อสร้างนิพจน์ข้อจำกัด  
2. ในฟิลด์ **ConstraintBody** ให้ป้อน 'Implies[FrontGrill=="Metal", CornerProtection] '
    * ตรรกะนิพจน์นี้กล่าวว่า ถ้าตะแกรงด้านหน้าเป็นโลหะ จะต้องเลือกตัวเลือกการป้องกันมุม  
3. เลือก **ตรวจสอบความถูกต้อง**
    * ฟังก์ชันการตรวจสอบดำเนินการโดยใช้นิพจน์ข้อจำกัดและตรวจสอบหาข้อผิดพลาดทางไวยากรณ์  
4. เลือก **ปิด**
5. เลือก **ตกลง**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]