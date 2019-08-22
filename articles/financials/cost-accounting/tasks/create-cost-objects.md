---
title: 'สร้างออบเจ็กต์ต้นทุน  '
description: กระบวนงานนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินต้นทุน Dynamics 365 for Finance and Operations Enterprise edition ลงในการบัญชีต้นทุนผ่านทางตัวเชื่อมต่อข้อมูล
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f63827977f080aa78fb385c60f757ad6b710005
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841260"
---
# <a name="create-cost-objects"></a>สร้างออบเจ็กต์ต้นทุน   

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินต้นทุน Dynamics 365 for Finance and Operations Enterprise edition ลงในการบัญชีต้นทุนผ่านทางตัวเชื่อมต่อข้อมูล บริษัทสาธิต USMF ถูกนำมาใช้เพื่อสร้างกระบวนงานนี้  กระบวนงานนี้มีไว้สำหรับคุณลักษณะการลงบัญชีต้นทุนที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611


## <a name="create-new-cost-objects"></a>สร้างออบเจ็กต์ต้นทุนใหม่
1. ไปที่ การลงบัญชีต้นทุนสินค้า > มิติ > มิติออบเจ็กต์ต้นทุน
2. คลิก สร้าง
3. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
4. ในฟิลด์ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติ ให้ป้อนหรือเลือกค่า
5. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
6. คลิก บันทึก

## <a name="configure-the-data-connector"></a>ตั้งค่าคอนฟิกตัวเชื่อมต่อข้อมูล
1. คลิก ตั้งค่าคอนฟิกตัวให้บริการสมาชิกมิติ
    * เลือก CostCenter เพื่อนำเข้ามิติ CostCenter ลงในการลงบัญชีต้นทุน  
2. ในฟิลด์ชื่อมิติ เลือกศูนย์ต้นทุน
3. คลิก ตกลง

## <a name="import-cost-centers"></a>นำเข้าศูนย์ต้นทุน
1. คลิก นำเข้าสมาชิกมิติ
2. คลิก ตกลง

## <a name="view-the-imported-cost-centers"></a>ดูศูนย์ต้นทุนที่นำเข้า
1. คลิก ดูสมาชิกมิติ

