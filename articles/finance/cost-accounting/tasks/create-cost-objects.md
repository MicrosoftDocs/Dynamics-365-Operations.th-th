---
title: 'สร้างออบเจ็กต์ต้นทุน  '
description: กระบวนการนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินของศูนย์ต้นทุน ลงในบัญชีต้นทุนสินค้าผ่านตัวเชื่อมต่อข้อมูล
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734143"
---
# <a name="create-cost-objects"></a>สร้างออบเจ็กต์ต้นทุน   

[!include [banner](../../includes/banner.md)]

กระบวนการนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินของศูนย์ต้นทุน ลงในบัญชีต้นทุนสินค้าผ่านตัวเชื่อมต่อข้อมูล บริษัทสาธิต USMF ถูกนำมาใช้เพื่อสร้างกระบวนงานนี้  


## <a name="create-new-cost-objects"></a>สร้างออบเจ็กต์ต้นทุนใหม่
1. ไปที่ **การลงบัญชีต้นทุน > มิติ > มิติออบเจ็กต์ต้นทุน**
2. คลิก **สร้าง**
3. ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง
4. ในฟิลด์ **ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติs** ให้ป้อนหรือเลือกค่า
5. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
6. คลิก **บันทึก**

## <a name="configure-the-data-connector"></a>ตั้งค่าคอนฟิกตัวเชื่อมต่อข้อมูล
1. คลิก **ตั้งค่าคอนฟิกตัวให้บริการสมาชิกมิติ**
    * เลือก CostCenter เพื่อนำเข้ามิติ CostCenter ลงในการลงบัญชีต้นทุน  
2. ในฟิลด์ **ชื่อมิติ** เลือกศูนย์ต้นทุน
3. คลิก **ตกลง** 

## <a name="import-cost-centers"></a>นำเข้าศูนย์ต้นทุน
1. คลิก **นำเข้าสมาชิกมิติ**
2. คลิก **ตกลง** 

## <a name="view-the-imported-cost-centers"></a>ดูศูนย์ต้นทุนที่นำเข้า
1. คลิก **ดูสมาชิกมิติ**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
