---
title: นับจำนวนสินค้าคงคลังในคลังสินค้า
description: หัวข้อนี้อธิบายกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลัง เพื่อนับสินค้าเฉพาะที่สถานที่ในคลังสินค้า
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a7f85cb91f36004a6bd6da714e7baa460a83a66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000116"
---
# <a name="count-inventory-in-a-warehouse"></a>นับจำนวนสินค้าคงคลังในคลังสินค้า

[!include [banner](../../includes/banner.md)]

หัวข้อนี้อธิบายกระบวนการของการสร้างและการลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลัง เพื่อนับสินค้าเฉพาะที่สถานที่ในคลังสินค้า กระบวนงานดังกล่าวใช้กับฟังก์ชัน "คลังสินค้าพื้นฐาน" ซึ่งพร้อมใช้งานในโมดูลการจัดการสินค้าคงคลัง และไม่ใช้กับฟังก์ชันคลังสินค้าที่พร้อมใช้งานในโมดูลการจัดการคลังสินค้า คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง ถ้าคุณกำลังใช้ข้อมูลของคุณเอง โปรดตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าผลิตภัณฑ์และสถานที่แล้ว และคุณได้สร้างชื่อสมุดรายวันสินค้าคงคลังสำหรับสมุดรายวันการตรวจนับแล้ว การนับสินค้าคงคลังจะดำเนินการปกติโดยพนักงานคลังสินค้า


## <a name="create-an-inventory-counting-journal"></a>สร้างสมุดรายวันการตรวจนับสินค้าคงคลัง
1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการสินค้าคงคลัง > รายการสมุดรายวัน > การนับสินค้า > การนับ**
2. เลือก **ใหม่**
3. ในฟิลด์ **ชื่อ** ให้เลือกชื่อสมุดรายวันการตรวจนับสินค้าคงคลังที่คุณต้องการใช้จากรายการแบบหล่นลง บางฟิลด์อื่นๆ จะถูกเติมข้อมูลตามการตั้งค่าของชื่อสมุดรายวันการตรวจนับสินค้าคงคลังที่คุณเลือก  
4. ในฟิลด์ **ผู้ปฏิบัติงาน** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
5. ในรายการ **เลือก** ผู้ปฏิบัติงานที่คุณต้องการใช้
6. เลือก **ตกลง**

## <a name="create-journal-lines"></a>สร้างรายการสมุดรายวัน
1. เลือก **ใหม่**
2. ในฟิลด์ **หมายเลขสินค้า** ให้เลือกเรกคอร์ดที่ต้องการจากรายการแบบหล่นลง ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือก **A0001**  
3. ในฟิลด์ **ไซต์** ให้เลือกเรกคอร์ดที่ต้องการจากรายการแบบหล่นลง ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือกไซต์ **2**
4. ในฟิลด์ **คลังสินค้า** ให้เลือกเรกคอร์ดที่ต้องการจากรายการแบบหล่นลง ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือกคลังสินค้า **24**  
5. ในฟิลด์ **สถานที่** ให้เลือกเรกคอร์ดที่ต้องการจากรายการแบบหล่นลง ถ้าคุณกำลังใช้บริษัทข้อมูลสาธิต USMF เลือกสถานที่ **BULK-001**  
6. ในฟิลด์ตรวจนับ ให้ป้อนตัวเลข ถ้าคุณป้อนจำนวนที่ตรวจนับที่แตกต่างกับจำนวนที่แสดงในฟิลด์ **คงคลังคงเหลือ** ฟิลด์ **ปริมาณ** จะถูกปรับปรุงเพื่อแสดงความขัดแย้ง  
7. เลือก **บันทึก**

## <a name="post-the-inventory-counting-journal"></a>ลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลัง
1. เลือก **ลงรายการบัญชี** เมื่อคุณลงรายการบัญชีสมุดรายวันการตรวจนับสินค้าคงคลัง ถ้าจำนวนที่ตรวจนับแตกต่างจากจำนวนที่รายงานในฟิลด์ **คงคลังคงเหลือ** การรับสินค้าสินค้าคงคลัง หรือการตัดสินค้าจากคลังจะลงถูกรายการบัญชี ระดับสินค้าคงคลังและค่าจะถูกเปลี่ยน และธุรกรรมบัญชีแยกประเภทจะถูกสร้างขึ้น
2. เลือก **ตกลง**

## <a name="view-inventory-transactions"></a>ดูธุรกรรมสินค้าคงคลัง
1. เลือก **สินค้าคงคลัง**
2. เลือก **ธุรกรรม** ที่นี่คุณสามารถดูธุรกรรมที่เกี่ยวข้องใดๆ ซึ่งจะถูกสร้างเมื่อคุณลงรายการบัญชีในสมุดรายวันการตรวจนับสินค้าคงคลัง   

