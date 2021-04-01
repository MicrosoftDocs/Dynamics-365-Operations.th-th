---
title: เพิ่มข้อจำกัดนิพจน์ไปที่แบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีที่คุณสามารถเพิ่มข้อจำกัดนิพจน์ใหม่ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์ '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81026d8622d3f03b3b87747800f4845cda823569
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256170"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>เพิ่มข้อจำกัดนิพจน์ไปที่แบบจำลองการจัดโครงแบบผลิตภัณฑ์

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีที่คุณสามารถเพิ่มข้อจำกัดนิพจน์ใหม่ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์  แสดงวิธีการกำหนดว่าการป้องกันมุมต้องใช้กับลำโพง ถ้าผู้ใช้เลือกเป็นตะแกรงด้านหน้าเป็นโลหะ  กระบวนงานใช้ส่วนประกอบลำโพงขั้นสูงในบริษัทสาธิต USMF


## <a name="create-an-expression-constraint"></a>สร้างข้อจำกัดนิพจน์
1. คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย
2. คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์
3. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * ตัวอย่างนี้ใช้แบบจำลองลำโพงระดับสูง  
4. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
5. ขยายส่วนข้อจำกัด
6. คลิก เพิ่ม
7. คลิก สร้าง
8. ในฟิลด์ชื่อ ให้พิมพ์ค่า 

## <a name="enter-expression"></a>ป้อนนิพจน์
1. คลิกแก้ไขนิพจน์
    * ถ้าคุณปลดล็อคอินเทอร์เฟสผู้ใช้ในงานที่บันทึกไว้ในขั้นตอนนี้ คุณจะสามารถใช้ IntelliSense และรายการของสัญลักษณ์เพื่อสร้างนิพจน์ข้อจำกัด  
2. ในฟิลด์ ConstraintBody ให้ป้อน ' Implies [FrontGrill == "โลหะ" CornerProtection] '
    * ตรรกะนิพจน์นี้กล่าวว่า ถ้าตะแกรงด้านหน้าเป็นโลหะ จะต้องเลือกตัวเลือกการป้องกันมุม  
3. คลิก ตรวจสอบความถูกต้อง
    * ฟังก์ชันการตรวจสอบดำเนินการโดยใช้นิพจน์ข้อจำกัดและตรวจสอบหาข้อผิดพลาดทางไวยากรณ์  
4. คลิก ปิด
5. คลิก ตกลง



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]