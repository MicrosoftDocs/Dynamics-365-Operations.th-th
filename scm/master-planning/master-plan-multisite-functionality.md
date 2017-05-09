---
title: "การวางแผนหลักและฟังก์ชันหลายไซต์"
description: "การวางแผนหลักใช้การตั้งค่าไซต์และมิติสินค้าคงคลังของคลังสินค้ามาพิจารณา"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19eeee753c15cf2670948ce2c615a112813c16ad
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-and-multisite-functionality"></a>การวางแผนหลักและฟังก์ชันหลายไซต์

การวางแผนหลักใช้การตั้งค่าไซต์และมิติสินค้าคงคลังของคลังสินค้ามาพิจารณา 

มิติไซต์เป็นข้อมูลบังคับ และคุณสามารถตั้งค่ามิติคลังสินค้าให้เป็นข้อมูลบังคับได้

เมื่อมิติเป็นข้อมูลบังคับ คุณต้องป้อนค่ามิติบนธุรกรรมของสินค้าคงคลังทั้งหมด ดังนั้น ในระหว่างการวางแผนหลัก คุณต้องทราบไซต์และคลังสินค้าสำหรับความต้องการเริ่มแรก มิติไซต์ยังต้องสอดคล้องในระหว่างการขยายความต้องการระดับล่าง ค่าไซต์ไม่เปลี่ยนแปลง

เมื่อไม่ได้ตั้งค่าคลังสินค้าเป็นข้อมูลบังคับ จะไม่ทราบคลังสินค้าจากความต้องการเริ่มแรก กลไกจัดการการวางแผนต้องกำหนดคลังสินค้าที่จะใช้ตามข้อมูลการตั้งค่าที่กำหนดสำหรับสินค้า คลังสินค้าแต่ละแห่ง และรายละเอียดของรายการใบสั่ง

บทความ wiki ต่อไปนี้อธิบายวิธีการทำงานของกลไกจัดการการวางแผน เมื่อมีการกำหนดการตั้งค่าที่แตกต่างกัน เพื่อกำหนดคลังสินค้าที่จะใช้

[การวางแผนหลัก- ความครอบคลุมไซต์และคลังสินค้า ข้อมูลบังคับคลังสินค้า](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[การวางแผนหลัก - ความครอบคลุมไซต์ ข้อมูลบังคับคลังสินค้า](master-plan-site-coverage-warehouse-mandatory.md)

[การวางแผนหลัก - ความครอบคลุมไซต์และคลังสินค้า คลังสินค้าไม่ใช่ข้อมูลบังคับ](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[การวางแผนหลัก - ความครอบคลุมไซต์ คลังสินค้าไม่ใช่ข้อมูลบังคับ](master-plan-site-coverage-warehouse-not-mandatory.md)

[การวางแผนหลัก - วิธีการกำหนดเวอร์ชัน BOM](master-plan-bom-version-determined.md)


