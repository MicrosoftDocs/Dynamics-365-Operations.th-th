---
title: "การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ"
description: "หัวข้อนี้อธิบายวิธีการวางแผนสินค้าที่มีไซต์เป็นมิติความครอบคลุม คลังสินค้าเป็นมิติบังคับ"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a1bf8f2253c63e4b6ca8fee02ec6b1cfb8aad73c
ms.contentlocale: th-th
ms.lasthandoff: 05/25/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ

[!include[banner](../includes/banner.md)]


หัวข้อนี้อธิบายวิธีการวางแผนสินค้าที่มีไซต์เป็นมิติความครอบคลุม คลังสินค้าเป็นมิติบังคับ

สถานการณ์จำลองการวางแผนหลักนี้มีเงื่อนไขดังต่อไปนี้

-   มิติไซต์มีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ การตั้งค่านี้ไม่สามารถแก้ไขได้
-   มิติคลังสินค้ามีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ
-   มิติไซต์ตั้งค่าสำหรับการวางแผนความครอบคลุม อาจมีการตั้งค่ามิติอื่นสำหรับการวางแผนความครอบคลุมด้วย อย่างไรก็ตาม การตั้งค่าเหล่านั้นไม่ได้รับผลกระทบจากฟังก์ชันหลายไซต์
-   มิติคลังสินค้าไม่ได้ตั้งค่าสำหรับการวางแผนความครอบคลุม ดังนั้น การจัดหาวัสดุและความต้องการถูกรวมโดยไซต์ และอาจรวมถึงมิติความครอบคลุมที่วางแผนอื่นด้วย

รูปภาพต่อไปนี้แสดงวิธีการประมวลผลการวางแผนหลัก พารามิเตอร์ที่มีการอ้างอิงในรูปภาพ และตำแหน่งของพารามิเตอร์เหล่านั้นมีดังต่อไปนี้
-   มีการกำหนดความครอบคลุมสินค้าสำหรับสินค้า คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้** เลือกสินค้า และคลิก **วางแผน &gt; ความครอบคลุมสินค้า**
-   มีการกำหนดความสัมพันธ์ในการเติมสินค้าสำหรับคลังสินค้า  คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า** บนแท็บ **การวางแผนหลัก** ดูกลุ่มฟิลด์ **คลังสินค้าหลัก**
-   ใบสั่งประเภทใบสั่งเริ่มต้นถูกตั้งค่าเป็นการผลิต ใบสั่งซื้อ หรือคัมบัง คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้** เลือกสินค้า และคลิก **วางแผน &gt; การตั้งค่าใบสั่งเริ่มต้น** ในฟอร์ม **การตั้งค่าใบสั่งเริ่มต้น** ดูฟิลด์ **ประเภทใบสั่งเริ่มต้น**

![ความต้องการความครอบคลุมไซต์ที่จำเป็นต้องมีคลังสินค้า](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a>ดูเพิ่มเติมที่
--------

[การวางแผนหลักและฟังก์ชันหลายไซต์](master-plan-multisite-functionality.md)

[การวางแผนหลัก- ความครอบคลุมไซต์และคลังสินค้า ข้อมูลบังคับคลังสินค้า](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[การวางแผนหลัก - ความครอบคลุมไซต์ ข้อมูลบังคับคลังสินค้า](master-plan-site-coverage-warehouse-mandatory.md)

[การวางแผนหลัก - ความครอบคลุมไซต์และคลังสินค้า คลังสินค้าไม่ใช่ข้อมูลบังคับ](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[การวางแผนหลัก - วิธีการกำหนดเวอร์ชัน BOM](master-plan-bom-version-determined.md)




