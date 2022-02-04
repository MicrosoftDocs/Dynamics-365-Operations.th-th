---
# required metadata
title: ภาพรวมของการวางแผนหลักและฟังก์ชันหลายไซต์
description: การวางแผนหลักใช้การตั้งค่าไซต์และมิติสินค้าคงคลังของคลังสินค้ามาพิจารณา
author: ChristianRytt
ms.date: 07/25/2019
ms.topic: overview
ms.prod: null
ms.technology: null
ms.search.form: 'InventLocation, InventSite'
audience: Application User
ms.reviewer: kamaybac
ms.custom:
  - '2434'
  - intro-internal
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: '2016-02-28'
ms.dyn365.ops.version: AX 7.0.0
---

# <a name="master-planning-and-multisite-functionality-overview"></a>ภาพรวมของการวางแผนหลักและฟังก์ชันหลายไซต์

[!include [banner](../includes/banner.md)]

การวางแผนหลักใช้การตั้งค่าไซต์และมิติสินค้าคงคลังของคลังสินค้ามาพิจารณา 

มิติไซต์เป็นข้อมูลบังคับ และคุณสามารถตั้งค่ามิติคลังสินค้าให้เป็นข้อมูลบังคับได้

เมื่อมิติเป็นข้อมูลบังคับ คุณต้องป้อนค่ามิติบนธุรกรรมของสินค้าคงคลังทั้งหมด ดังนั้น ในระหว่างการวางแผนหลัก คุณต้องทราบไซต์และคลังสินค้าสำหรับความต้องการเริ่มแรก มิติไซต์ยังต้องสอดคล้องในระหว่างการขยายความต้องการระดับล่าง ค่าไซต์ไม่เปลี่ยนแปลง

เมื่อไม่ได้ตั้งค่าคลังสินค้าเป็นข้อมูลบังคับ จะไม่ทราบคลังสินค้าจากความต้องการเริ่มแรก เครื่องวางแผนต้องกำหนดคลังสินค้าที่จะใช้ตามข้อมูลการตั้งค่าที่กำหนดสำหรับสินค้า คลังสินค้าแต่ละแห่ง และรายละเอียดของบรรทัดใบสั่ง

หัวข้อต่อไปนี้อธิบายวิธีการทำงานของเครื่องวางแผน เมื่อมีการกำหนดการตั้งค่าที่แตกต่างกันเพื่อกำหนดคลังสินค้าที่จะใช้

[การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า จำเป็นต้องมีคลังสินค้า](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ](master-plan-site-coverage-warehouse-mandatory.md)

[การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า ไม่จำเป็นต้องมีคลังสินค้า](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าไม่บังคับ](master-plan-site-coverage-warehouse-not-mandatory.md)

[กำหนดเวอร์ชันสูตรการผลิต](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]