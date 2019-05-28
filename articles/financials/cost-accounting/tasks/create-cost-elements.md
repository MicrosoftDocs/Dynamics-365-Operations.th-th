---
title: 'สร้างองค์ประกอบต้นทุน  '
description: 'มีหลายวิธีในการสร้างองค์ประกอบต้นทุนในการลงบัญชีต้นทุน '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbaf4f7533d51d554d838e8e9e2aa05ca451298a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543806"
---
# <a name="create-cost-elements"></a>สร้างองค์ประกอบต้นทุน   

[!include [task guide banner](../../includes/task-guide-banner.md)]

มีหลายวิธีในการสร้างองค์ประกอบต้นทุนในการลงบัญชีต้นทุน  กระบวนงานนี้แสดงวิธีการสร้างองค์ประกอบต้นทุนโดยการนำเข้าบัญชีหลักผ่านตัวเชื่อมต่อข้อมูล บริษัทสาธิต USMF ถูกนำมาใช้เพื่อสร้างกระบวนงานนี้  กระบวนงานนี้มีไว้สำหรับคุณลักษณะการลงบัญชีต้นทุนที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611


## <a name="create-new-cost-elements"></a>สร้างองค์ประกอบต้นทุนใหม่
1. ไปที่ การลงบัญชีต้นทุนสินค้า > มิติ > มิติองค์ประกอบต้นทุน
2. คลิก สร้าง
3. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
4. ในฟิลด์ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติ ให้ป้อนหรือเลือกค่า
5. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
6. คลิก บันทึก

## <a name="configure-the-data-connector"></a>ตั้งค่าคอนฟิกตัวเชื่อมต่อข้อมูล
1. คลิก ตั้งค่าคอนฟิกตัวให้บริการสมาชิกมิติ
2. ในฟิลด์ผังบัญชี ให้ป้อนหรือเลือกค่า
    * เลือก ใช้ร่วมกัน เพื่อใช้ผังบัญชีร่วมกัน  
3. คลิก สร้าง
4. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * คุณสามารถใช้ตัวกรองบัญชีเพื่อให้ตรงกับเกณฑ์ของคุณ  
5. ในฟิลด์จากบัญชีลูกค้า ให้ป้อนหรือเลือกค่า
6. ในฟิลด์ถึงบัญชีลูกค้า ให้ป้อนหรือเลือกค่า
7. คลิก ตกลง

## <a name="import-main-accounts"></a>นำเข้าบัญชีหลัก
1. คลิก นำเข้าสมาชิกมิติ
    * บัญชีหลักจะถูกนำเข้าไปยังการลงบัญชีต้นทุนสินค้า และใช้เป็นองค์ประกอบต้นทุน  
2. คลิก ตกลง

## <a name="view-the-imported-accounts-as-cost-elements"></a>ดูบัญชีที่นำเข้าเป็นองค์ประกอบต้นทุน
1. คลิก ดูสมาชิกมิติ
    * ดูบัญชีแยกประเภทที่นำเข้าเป็นองค์ประกอบต้นทุนในธุรกิจของคุณที่ต้นทุนสามารถไปได้  

