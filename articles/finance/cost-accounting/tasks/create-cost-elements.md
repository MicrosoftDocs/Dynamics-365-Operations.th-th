---
title: 'สร้างองค์ประกอบต้นทุน  '
description: 'มีหลายวิธีในการสร้างองค์ประกอบต้นทุนในการลงบัญชีต้นทุน '
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779701"
---
# <a name="create-cost-elements"></a>สร้างองค์ประกอบต้นทุน   

[!include [banner](../../includes/banner.md)]

มีหลายวิธีในการสร้างองค์ประกอบต้นทุนในการลงบัญชีต้นทุน  กระบวนงานนี้แสดงวิธีการสร้างองค์ประกอบต้นทุนโดยการนำเข้าบัญชีหลักผ่านตัวเชื่อมต่อข้อมูล บริษัทสาธิต USMF ถูกนำมาใช้เพื่อสร้างกระบวนงานนี้  กระบวนงานนี้มีไว้สำหรับคุณลักษณะการลงบัญชีต้นทุนที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611


## <a name="create-new-cost-elements"></a>สร้างองค์ประกอบต้นทุนใหม่
1. ไปที่ **การลงบัญชีต้นทุน > มิติ > มิติองค์ประกอบต้นทุน**
2. คลิก **สร้าง**
3. ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง
4. ในฟิลด์ **ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติs** ให้ป้อนหรือเลือกค่า
5. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
6. คลิก **บันทึก**

## <a name="configure-the-data-connector"></a>ตั้งค่าคอนฟิกตัวเชื่อมต่อข้อมูล
1. คลิก **ตั้งค่าคอนฟิกตัวให้บริการสมาชิกมิติ**
2. ในฟิลด์ **ผังบัญชี** ให้ป้อนหรือเลือกค่า
    * เลือก **ใช้ร่วมกัน** เพื่อใช้ผังบัญชีร่วมกัน  
3. คลิก **สร้าง**
4. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * คุณสามารถใช้ตัวกรองบัญชีเพื่อให้ตรงกับเกณฑ์ของคุณ  
5. ในฟิลด์ **จากบัญชีลูกค้า** ให้ป้อนหรือเลือกค่า
6. ในฟิลด์ **ถึงบัญชีลูกค้า** ให้ป้อนหรือเลือกค่า
7. คลิก **ตกลง** 

## <a name="import-main-accounts"></a>นำเข้าบัญชีหลัก
1. คลิก **นำเข้าสมาชิกมิติ**
    * บัญชีหลักจะถูกนำเข้าไปยังการลงบัญชีต้นทุนสินค้า และใช้เป็นองค์ประกอบต้นทุน  
2. คลิก **ตกลง** 

## <a name="view-the-imported-accounts-as-cost-elements"></a>ดูบัญชีที่นำเข้าเป็นองค์ประกอบต้นทุน
1. คลิก **ดูสมาชิกมิติ**
    * ดูบัญชีแยกประเภทที่นำเข้าเป็นองค์ประกอบต้นทุนในธุรกิจของคุณที่ต้นทุนสามารถไปได้  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
