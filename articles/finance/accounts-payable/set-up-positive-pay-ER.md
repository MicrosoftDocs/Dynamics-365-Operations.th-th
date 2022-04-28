---
title: ตั้งค่าและสร้างไฟล์ Positive Pay โดยใช้การรายงานทางอิเล็กทรอนิกส์
description: หัวข้อนี้อธิบายวิธีการตั้งค่า positive pay โดยใช้การรายงานทางอิเล็กทรอนิกส์
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544519"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>ตั้งค่าไฟล์ Positive Pay โดยใช้การรายงานทางอิเล็กทรอนิกส์

ตั้งค่า Positive Pay เพื่อสร้างรายการอิเล็กทรอนิกส์ของเช็คที่ได้รับไปยังธนาคาร  จากนั้น เมื่อเช็คถูกนำเสนอให้แก่ธนาคารแล้ว ธนาคารจะเปรียบเทียบเช็คกับรายการของเช็ค  ถ้าเช็คตรงกับเช็คในรายการ ธนาคารจะเคลียร์เช็ค  ถ้าเช็คไม่ตรงกัน ธนาคารจะระงับเช็คไว้เพื่อตรวจสอบ

## <a name="set-up-the-electronic-reporting-configuration"></a>สร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์

1. ไปที่ **พื้นที่ทำงาน \> การรายงานทางอิเล็กทรอนิกส์**
2. บนไทล์สำหรับผู้ให้บริการตั้งค่าคอนฟิก **Microsoft** ให้เลือก **ที่เก็บ**
3. เลือก **ส่วนกลาง** แล้วเลือก **เปิด**
4. ถ้าต้องสร้างการเชื่อมต่อกับที่เก็บ ให้เลือกลิงก์สีเงินในกล่องโต้ตอบ
5. ในรายการ การตั้งค่าคอนฟิก ให้ค้นหาและเลือก **รูปแบบ Positive pay \> รูปแบบ Positive pay**
6. บนแท็บด่วน **รุ่น** ให้เลือกรุ่นล่าสุด แล้วเลือก **นำเข้า**

## <a name="set-up-a-positive-pay-format"></a>ตั้งค่ารูปแบบของ Positive Pay

1. ไปที่ **การจัดการเงินสดและธนาคาร \> การตั้งค่า \> รูปแบบ Positive pay**
2. เลือก **ใหม่**
3. ตั้งค่าฟิลด์ **รูปแบบการชำระเงิน** และ **คำอธิบาย**
4. เลือกกล่องกาเครื่องหมาย **รูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป**
5. ตั้งค่าฟิลด์ **ส่งออกการตั้งค่าคอนฟิกรูปแบบ** เป็นรูปแบบ **รูปแบบ Positive pay**

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>กำหนดรูปแบบ Positve Pay ให้กับบัญชีธนาคาร

1. ไปที่ **การจัดการเงินสดและธนาคาร \> บัญชีธนาคาร \> บัญชีธนาคาร**
2. เปิดบัญชีธนาคาร
3. บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าฟิลด์ **รูปแบบ Positive pay** เป็นรูปแบบที่สร้างไว้ก่อนหน้านี้
4. ตั้งค่าฟิลด์ **วันที่เริ่มต้นของ Positive pay** เป็นวันที่ปัจจุบัน

## <a name="generate-a-positive-pay-file"></a>สร้างไฟล์ Positive Pay

1. ไปที่ **การจัดการเงินสดและธนาคาร \> บัญชีธนาคาร \> บัญชีธนาคาร**
2. เปิดบัญชีธนาคารที่มีการตั้งค่า Positive Pay
3. เลือก **จัดการการชำระเงิน \> Positive pay \> ไฟล์ Positive pay**
4. ตั้งค่าฟิลด์ **วันที่ตัดยอด** ตรวจสอบว่ามีการสร้างขึ้นก่อนวันที่นี้จะถูกรวมไว้

ไฟล์ XML ที่ได้จะถูกดาวน์โหลด
