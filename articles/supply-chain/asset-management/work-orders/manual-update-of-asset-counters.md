---
title: การอัปเดตตัวนับสินทรัพย์ด้วยตนเอง
description: บทความนี้อธิบายการอัปเดตตัวนับสินทรัพย์ด้วยตนเองในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 30c672286c16a4353556a507019960edb93f8b1b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016607"
---
# <a name="manual-update-of-asset-counters"></a>การอัปเดตตัวนับสินทรัพย์ด้วยตนเอง

[!include [banner](../../includes/banner.md)]



ตัวนับจะใช้ในการสร้างการลงทะเบียนในสินทรัพย์ เช่น การลงทะเบียนเกี่ยวกับจำนวนชั่วโมงที่มีการดำเนินงานสินทรัพย์หรือปริมาณที่มีการผลิต

ชนิดตัวนับที่ถูกเลือกสำหรับตัวนับอาจถูกตั้งค่าให้สืบทอดค่าตัวนับ กล่าวคือ มีการตั้งค่าตัวเลือก **สืบทอดมูลค่าของตัวนับสินทรัพย์** เป็น **ใช่** บนแท็บด่วน **ทั่วไป** ของหน้า **ตัวนับ** (**การจัดการสินทรัพย์** > **การตั้งค่า** > **ชนิดสินทรัพย์** > **ตัวนับ**) ในกรณีนี้ เมื่อคุณสร้างรายการตัวนับใหม่ของชนิดนั้น สินทรัพย์รองทั้งหมดที่ใช้ชนิดตัวนับเดียวกันจะถูกอัพเดตโดยอัตโนมัติ

บนหน้า **สินทรัพย์ทั้งหมด** คุณสร้างการลงทะเบียนตัวนับชั่วโมงหรือปริมาณในสินทรัพย์ ตามการอ่านของคุณในสินทรัพย์

1. เลือก **การจัดการสินทรัพย์** > **สินทรัพย์** > **สินทรัพย์ทั้งหมด**

2. เลือกสินทรัพย์ และจากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **สินทรัพย์** ในกลุ่ม **เชิงป้องกัน** เลือก **ตัวนับ** บนหน้า **ตัวนับสินทรัพย์** แสดงรายการของการลงทะเบียนตัวนับก่อนหน้านี้ทั้งหมดที่ถูกดำเนินการในสินทรัพย์ที่เลือก

3. เลือก **สร้าง** เพื่อสร้างการลงทะเบียน รหัสสินทรัพย์ถูกป้อนโดยอัตโนมัติลงในฟิลด์ **สินทรัพย์**

4. ในฟิลด์ **ตัวนับ** เลือกตัวนับที่เกี่ยวข้อง เฉพาะตัวนับที่เกี่ยวข้องกับชนิดสินทรัพย์ที่เลือกไว้ในสินทรัพย์เท่านั้นที่พร้อมใช้งานสำหรับการเลือก หน่วยที่เกี่ยวข้องจะถูกป้อนโดยอัตโนมัติในฟิลด์ **หน่วย**

5. ในฟิลด์ **ลงทะเบียน** ให้เลือกวันที่และเวลาสำหรับการลงทะเบียนตัวนับ

6. ในฟิลด์ **ค่า** ป้อนหมายเลขตั้งแต่การลงทะเบียนตัวนับสุดท้าย อีกทางหนึ่งคือ ในฟิลด์ **มูลค่ารวม** ให้ป้อนหมายเลขการตรวจนับทั้งหมด

บันทึกคะแนนต่อไปนี้:

- ถ้าคุณได้ติดตั้งตัวนับใหม่บนสินทรัพย์ คุณต้องลงทะเบียนการเปลี่ยนแปลงบนสินทรัพย์ในหน้า **ตัวนับสินทรัพย์** หลังจากนั้นคุณต้องสร้างรายการลงทะเบียนสองรายการที่มีการลงเวลาที่เหมือนกัน รายการแรกต้องเป็นตัวนับที่คุณกำลังจะแทนที่ บนรายการที่เกี่ยวข้องกับตัวนับใหม่ ให้เลือกกล่องกาเครื่องหมาย **รีเซ็ตตัวนับ** ในฟิลด์ **รวม** หมายเลขการตรวจนับรวมคือผลรวมของตัวนับของค่าลงทะเบียนทั้งหมดบนชนิดตัวนับนั้น

- ถ้ากล่องกาเครื่องหมาย **รีเซ็ตตัวนับ** ถูกเลือกบนสินทรัพย์โดยใช้เเผนการบำรุงรักษาที่มีชนิดของช่วงเวลา "หนึ่งครั้งจาก ..." หรือ "เมื่อถึง ..." ตัวนับยังคงใช้งานอยู่บนรายการตัวนับใหม่ เนื่องจากคุณสร้างรายการตัวนับที่แยกต่างหาก และเริ่มต้นด้วยตัวนับใหม่

ภาพประกอบด้านล่างแสดงตัวอย่างของหน้า **ตัวนับสินทรัพย์**

![รูปที่ 1](media/11-work-orders.png)

บนหน้า **ตัวนับสินทรัพย์** (**การจัดการสินทรัพย์** > **การสอบถาม** > **สินทรัพย์** > **ตัวนับสินทรัพย์**) คุณสามารถทำการลงทะเบียนตัวนับในสินทรัพย์ต่างๆ ในเวลาเดียวกันได้ตามที่คุณต้องการ

>[!NOTE]
>คุณสามารถตั้งค่าช่วงเพื่อกำหนดความเบี่ยงเบนในการลงทะเบียนตัวนับด้วยตนเอง นอกจากนี้ คุณยังสามารถระบุชนิดของข้อความที่จะแสดงขึ้น ถ้าการลงทะเบียนอยู่นอกช่วงที่กำหนดไว้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าตัวนับ ให้ดูที่ [ตัวนับ](../setup-for-objects/counters.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]