---
title: ตั้งค่าชนิดค่าใช้จ่าย
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าชนิดค่าใช้จ่ายในการเช่าสินทรัพย์
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3ab31b16c6ae07466d7655832701e71092064fe1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969514"
---
# <a name="set-up-expense-types"></a>ตั้งค่าชนิดค่าใช้จ่าย

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการตั้งค่าชนิดค่าใช้จ่ายในการเช่าสินทรัพย์ ต้นทุนที่ไม่ได้แสดงไว้โดยกำหนดการชำระเงินจะเรียกว่า *ต้นทุนค่าใช้จ่าย* ตัวอย่างของต้นทุนเหล่านี้ได้แก่ ภาษีทรัพย์สิน ต้นทุนการบำรุงรักษาพื้นที่ทั่วไป และค่าใช้จ่ายในการประกันภัย

## <a name="add-an-administrative-expense-type"></a>เพิ่มชนิดค่าใช้จ่ายในการบริหารงาน

1. ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> ชนิดค่าใช้จ่าย**
2. เลือก **ใหม่**
3. ในฟิลด์ที่เหมาะสม ให้ป้อนชนิดค่าใช้จ่ายใหม่และคำอธิบาย

## <a name="assign-accounts-to-administrative-costs"></a>กำหนดบัญชีให้กับต้นทุนการจัดการ

ถัดไป คุณควรเชื่อมโยงบัญชีที่มีชนิดค่าใช้จ่าย บัญชีเหล่านี้จะถูกเดบิตเมื่อลงรายการบัญชีรายการกำหนดการค่าใช้จ่าย มีการระบุบัญชีตรงข้ามบนรายการ **กำหนดการชำระเงินค่าใช้จ่ายในการจัดการสินทรัพย์** ในแต่ละสัญญาเช่า

1. ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การเช่าสินทรัพย์**
2. บนแท็บ **บัญชี** บนแท็บด่วน **ค่าใช้จ่ายในการจัดการสินทรัพย์** ในฟิลด์ **ชนิดค่าใช้จ่าย** ให้เลือกชนิดค่าใช้จ่าย
3. เลือก **เพิ่ม**
4. ในฟิลด์ **ชนิดสมุดบัญชี** ให้เลือกชนิดของสมุดบัญชีที่จะเชื่อมโยงกับต้นทุนการจัดการ

    > [!NOTE]
    > ชนิดของสมุดบัญชีหลายชนิดสามารถเชื่อมโยงกับบัญชีค่าใช้จ่ายเดียวกันได้

5. ในฟิลด์ **รหัสบัญชี** ให้ระบุว่าควรใช้สัญญาเช่าอย่างไรกับสมุดบัญชี

    - **ทั้งหมด** – นำสมุดบัญชีไปใช้กับสัญญาเช่าทั้งหมด
    - **กลุ่ม** – นำสมุดบัญชีไปใช้กับกลุ่มสัญญาเช่าเฉพาะ
    - **ตาราง** – นำสมุดบัญชีไปใช้กับสัญญาเช่าเฉพาะ

6. ถ้าคุณเลือก **กลุ่ม** หรือ **ตาราง** ในฟิลด์ **รหัสบัญชี** เลือกหมายเลขบัญชีหรือหมายเลขกลุ่มในฟิลด์ **หมายเลขบัญชี/กลุ่ม**
7. ในฟิลด์ที่เหมาะสม ให้เลือกบัญชีหลักของสัญญาเช่าทางการเงินและบัญชีหลักของการเช่าดำเนินงาน

เมื่อคุณดำเนินการขั้นตอนต่อไปนี้เสร็จสมบูรณ์แล้ว คุณสามารถเพิ่มค่าใช้จ่ายผ่านทางรายการ **กำหนดการชำระเงินค่าใช้จ่ายในการจัดการสินทรัพย์** ในหน้า **รายละเอียดสัญญาเช่า** ของสัญญาเช่าที่เลือก อีกทางหนึ่งคือ คุณสามารถเพิ่มค่าใช้จ่ายเมื่อคุณสร้างสัญญาเช่าใหม่
