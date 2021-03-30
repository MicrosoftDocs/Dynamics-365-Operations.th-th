---
title: สร้างใบสั่งซื้อที่ได้รับการควบคุมโดยงบประมาณ
description: ใช้กระบวนงานนี้เพื่อสร้างใบสั่งซื้อที่มีการตรวจสอบงบประมาณที่มีอยู่
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 100db102f74d477bcfde48a24828b817fd65e033
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239526"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>สร้างใบสั่งซื้อที่ได้รับการควบคุมโดยงบประมาณ

[!include [banner](../../includes/banner.md)]

ใช้กระบวนงานนี้เพื่อสร้างใบสั่งซื้อที่มีการตรวจสอบงบประมาณที่มีอยู่ การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USMF


## <a name="review-the-budget-control-configuration"></a>ตรวจสอบการตั้งค่าคอนฟิกการควบคุมงบประมาณ
1. ไปที่ การจัดทำงบประมาณ > การตั้งค่า > การควบคุมงบประมาณ > การตั้งค่าคอนฟิกการควบคุมงบประมาณ
2. คลิกแท็บ เงินงบประมาณที่มีอยู่
3. คลิกแท็บ เอกสารและสมุดรายวัน
4. คลิกแท็บ กำหนดกฎการควบคุมงบประมาณ
5. คลิกแท็บ กำหนดกลุ่มงบประมาณ
6. ปิดหน้า

## <a name="create-the-purchase-order-header"></a>สร้างส่วนหัวของใบสั่งซื้อ
1. ไปที่การจัดซื้อและการจัดหา > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด
2. คลิก สร้าง
3. ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า
4. ขยายส่วนทั่วไป
5. ในฟิลด์ วันที่ลงบัญชี ตั้งค่าวันที่เป็น '2016-01-01'
6. คลิก ตกลง

## <a name="add-a-purchase-order-line"></a>เพิ่มรายการใบสั่งซื้อ
1. ในฟิลด์การจัดซื้อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
2. กำหนดปริมาณเป็น '2'
3. ในฟิลด์หน่วย ให้ป้อนหรือเลือกค่า
4. ตั้งค่าราคาต่อหน่วยเป็น '10000'
5. คลิกข้อมูลทางการเงิน
6. คลิกกระจายยอดเงิน
7. ในฟิลด์บัญชีแยกประเภท ให้ระบุค่า '601300-001-023--'
8. ปิดหน้า

## <a name="perform-budget-checking"></a>ทำการตรวจสอบงบประมาณ
1. คลิกข้อมูลทางการเงิน
2. คลิก ทำการตรวจสอบงบประมาณ
3. คลิกข้อมูลทางการเงิน
4. คลิก ข้อผิดพลาดหรือคำเตือนของการตรวจสอบงบประมาณ
5. คลิก ปิด



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]