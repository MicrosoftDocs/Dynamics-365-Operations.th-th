---
title: ลงทะเบียนสินค้าเป็นสินค้าที่เปิดใช้งานคลังสินค้าขั้นสูงโดยใช้สมุดรายวันการมาถึงของสินค้า
description: 'กระบวนงานนี้แสดงวิธีการลงทะเบียนสินค้าโดยใช้สมุดรายวันการมาถึงของสินค้า เมื่อคุณใช้กระบวนการจัดการคลังสินค้าขั้นสูง '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f05034454002fa9c4161b8f2d6cafdaeaa24d32
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977099"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>ลงทะเบียนสินค้าเป็นสินค้าที่เปิดใช้งานคลังสินค้าขั้นสูงโดยใช้สมุดรายวันการมาถึงของสินค้า

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการลงทะเบียนสินค้าโดยใช้สมุดรายวันการมาถึงของสินค้า เมื่อคุณใช้กระบวนการจัดการคลังสินค้าขั้นสูง  ซึ่งมักจะดำเนินการโดยเจ้าหน้าที่การรับสินค้า  

คุณสามารถเรียกใช้ขั้นตอนนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง  คุณต้องมีใบสั่งซื้อที่ได้รับการยืนยันที่มีรายการใบสั่งซื้อที่เปิดอยู่ก่อนที่คุณเริ่มคู่มือนี้  ต้องมีการเก็บสต็อกสินค้าในรายการ และจะต้องไม่ใช้ผลิตภัณฑ์ย่อย และต้องไม่มีมิติการติดตาม  และสินค้าจะต้องเชื่อมโยงกับกระบวนการการจัดการคลังสินค้าที่จะเปิดใช้งานกลุ่มมิติคลังสินค้า  ต้องเปิดใช้คลังสินค้าที่จะใช้สำหรับกระบวนการจัดการคลังสินค้า และสถานที่ที่คุณใช้สำหรับการรับสินค้าต้องมีการควบคุมป้ายทะเบียน ถ้าคุณกำลังใช้ USMF คุณสามารถใช้บัญชีบริษัท 1001 คลังสินค้า 51 และสินค้า M9200 เพื่อสร้าง PO ของคุณ 

จดบันทึกหมายเลขของใบสั่งซื้อที่คุณสร้าง และบันทึกหมายเลขสินค้าและไซต์ที่คุณใช้สำหรับรายการใบสั่งซื้อของคุณด้วย


## <a name="create-an-item-arrival-journal-header"></a>สร้างหัวข้อสมุดรายวันการมาถึงของสินค้า
1. ไปที่การมาถึงของสินค้า
2. คลิก สร้าง
3. ในฟิลด์ชื่อ ให้พิมพ์ค่าใดค่าหนึ่ง
    * ถ้าคุณกำลังใช้ USMF คุณสามารถพิมพ์ WHS. ถ้าคุณกำลังใช้ข้อมูลอื่นๆ สมุดรายวันที่มีชื่อที่คุณเลือกจะต้องมีคุณสมบัติดังต่อไปนี้: ตรวจสอบดูว่าสถานที่เบิกสินค้าต้องถูกตั้งค่าเป็น ไม่ และการบริหารการตรวจสอบสินค้าต้องถูกตั้งค่าเป็น ไม่  
4. ในฟิลด์หมายเลข ให้พิมพ์ค่า
5. ในฟิลด์ไซต์ ให้พิมพ์ค่า
    * เลือกไซต์ที่คุณใช้สำหรับรายการใบสั่งซื้อของคุณ  ซึ่งจะทำหน้าที่เป็นค่าเริ่มต้น ซึ่งจะเป็นค่าเริ่มต้นให้กับรายการทั้งหมดในสมุดรายวัน ถ้าคุณใช้คลังสินค้า 51 ใน USMF ให้เลือกไซต์ 5  
6. ในฟิลด์คลังสินค้า ให้พิมพ์ค่า
    * เลือกคลังสินค้าที่ถูกต้องสำหรับไซต์ที่คุณเลือก ซึ่งจะทำหน้าที่เป็นค่าเริ่มต้น ซึ่งจะเป็นค่าเริ่มต้นให้กับรายการทั้งหมดในสมุดรายวัน ถ้าคุณกำลังใช้ค่าตัวอย่างใน USMF ให้เลือก 51  
7. ในฟิลด์ตำแหน่ง ให้พิมพ์ค่า
    * เลือกสถานที่ที่ถูกต้องในคลังสินค้าที่คุณเลือก สถานที่เก็บที่จะต้องเชื่อมโยงกับโพรไฟล์ที่ตั้ง ซึ่งเป็นถูกควบคุมโดยป้ายทะเบียน ซึ่งจะทำหน้าที่เป็นค่าเริ่มต้น ซึ่งจะเป็นค่าเริ่มต้นให้กับรายการทั้งหมดในสมุดรายวัน ถ้าคุณกำลังใช้ค่าตัวอย่างใน USMF ให้เลือก Bulk-008  
8. คลิกขวาที่ลูกศรแบบหล่นลงในฟิลด์ป้ายทะเบียน และจากนั้นให้เลือกการดูรายละเอียด
9. คลิก สร้าง
10. ในฟิลด์แผ่นป้ายทะเบียน ให้พิมพ์ค่า
    * จดบันทึกค่า  
11. คลิก บันทึก
12. ปิดหน้า
13. ในฟิลด์แผ่นป้ายทะเบียน ให้พิมพ์ค่า
    * ป้อนมูลค่าของป้ายทะเบียนที่คุณเพิ่งสร้างขึ้น  ซึ่งจะทำหน้าที่เป็นค่าเริ่มต้น ซึ่งจะเป็นค่าเริ่มต้นให้กับรายการทั้งหมดในสมุดรายวัน  
14. คลิก ตกลง

## <a name="add-a-line"></a>เพิมรายการ
1. คลิก เพิ่มรายการ
2. ในฟิลด์หมายเลขสินค้า ให้พิมพ์ค่า
    * ป้อนหมายเลขสินค้าที่คุณใช้บนรายการใบสั่งซื้อ  
3. ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข
    * ป้อนปริมาณที่คุณต้องการลงทะเบียน  
    * ฟิลด์วันที่จะกำหนดวันที่ที่ปริมาณคงเหลือของสินค้านี้จะถูกลงทะเบียนในสินค้าคงคลัง  
    * รหัสล็อตจะถูกเติมโดยระบบ ถ้ามีการระบุเฉพาะจากข้อมูลที่ให้ไว้  มิฉะนั้น คุณจะต้องเพิ่มรายการนี้ด้วยตนเอง นี่เป็นฟิลด์บังคับที่ลิงค์การลงทะเบียนนี้กับรายการเอกสารต้นทางเฉพาะที่  

## <a name="complete-the-registration"></a>ดำเนินงานการลงทะเบียนให้สมบูรณ์
1. คลิก ตรวจสอบความถูกต้อง
    * มีการตรวจสอบว่า สมุดรายวันพร้อมที่จะถูกลงรายการบัญชีหรือไม่  หากการตรวจสอบจะล้มเหลวคุณ คุณจำเป็นต้องแก้ไขข้อผิดพลาดก่อนที่คุณจะสามารถลงรายการบัญชีสมุดรายวันได้  
2. คลิก ตกลง
    * หลังจากที่คุณคลิกตกลง ตรวจสอบข้อความ  ควรมีข้อความแจ้งว่า สมุดรายวันเรียบร้อย  
3. คลิก ลงรายการบัญชี
4. คลิก ตกลง
    * หลังจากที่คุณคลิกตกลง ตรวจสอบแถบข้อความ  ควรมีข้อความแจ้งว่า การดำเนินงานสำเร็จแล้ว  
5. ปิดหน้า

