---
title: สร้างเกณฑ์การเลือกราคาขาย
description: 'กระบวนงานนี้แสดงวิธีการสร้างเกณฑ์การเลือกราคาขายสำหรับแบบจำลองราคาขายตามแอททริบิวต์ '
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568458"
---
# <a name="create-sales-price-selection-criteria"></a>สร้างเกณฑ์การเลือกราคาขาย

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการสร้างเกณฑ์การเลือกราคาขายสำหรับแบบจำลองราคาขายตามแอททริบิวต์  ขั้นตอนนี้จำเป็นต้องใช้แบบจำลองราคาขายที่มีอยู่อย่างน้อยหนึ่งรายการ ตัวอย่างนี้ใช้แบบจำลองราคาสำหรับแบบจำลองราคาขายของโซลูชันลำโพงในบริษัทข้อมูลสาธิต USMF  โดยทั่วไปผู้จัดการผลิตภัณฑ์จะใช้กระบวนงานนี้

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>เพิ่มเกณฑ์ใหม่สำหรับแบบจำลองราคาขายที่มีอยู่

1. ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**
1. ในรายการ เลือกแถวสำหรับแบบจำลองผลิตภัณฑ์โซลูชันลำโพง แต่อย่าเลือกลิงค์สำหรับชื่อแบบจำลอง
1. บนบานหน้าต่างการดำเนินการ เลือก **แบบจำลอง**
1. เลือก **เกณฑ์แบบจำลองราคา**
1. เลือก **ใหม่**
1. ในฟิลด์ **ชื่อ** ให้พิมพ์ 'กลุ่มลูกค้า 10'
    * ใช้ชื่อของเกณฑ์แบบจำลองราคาเพื่อช่วยในการระบุเกณฑ์การเลือกที่อยู่ภายใต้  
1. ในฟิลด์ **แบบจำลองราคา** ให้ป้อนหรือเลือกค่า
1. ในฟิลด์ **ชนิดใบสั่ง** เลือก *ใบสั่งขาย*
    * ชนิดใบสั่งกำหนดฟิลด์ฐานข้อมูลที่จะใช้สำหรับการสอบถามเลือก  
1. ในฟิลด์ **ใช้ได้ตั้งแต่** ให้ป้อนวันที่
1. ในฟิลด์ **หมดอายุวันที่** ให้ป้อนวันที่
1. เลือก **บันทึก**

## <a name="create-the-query-for-the-selection-criteria"></a>สร้างการสอบถามสำหรับเกณฑ์การเลือก

1. เลือก **แก้ไข**
2. ในฟิลด์ **ตาราง** ให้เลือก *ลูกค้า*
3. ในฟิลด์ **ฟิลด์** ให้เลือก *กลุ่มลูกค้า*
    * ในตัวอย่างนี้ เราจะใช้กลุ่มลูกค้าเฉพาะสำหรับเกณฑ์การเลือก  
4. ในฟิลด์ **เกณฑ์** ให้เลือก *กลุ่มลูกค้า 10*
5. เลือก **ตกลง**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]