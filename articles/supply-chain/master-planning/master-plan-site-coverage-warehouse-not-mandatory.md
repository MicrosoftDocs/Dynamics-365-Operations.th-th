---
title: การวางแผนหลักสำหรับความครอบคลุมไซต์ที่ไม่จำเป็นต้องมีคลังสินค้า
description: บทความนี้อธิบายวิธีการวางแผนสินค้าที่มีไซต์เป็นชุดมิติความครอบคลุม
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b03bd1970aa7a2f3276186a0a9f8c2cd2880956
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741161"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>การวางแผนหลักสำหรับความครอบคลุมไซต์ที่ไม่จำเป็นต้องมีคลังสินค้า

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการวางแผนสินค้าที่มีไซต์เป็นชุดมิติความครอบคลุม

สถานการณ์จำลองการวางแผนหลักนี้มีเงื่อนไขดังต่อไปนี้

-   มิติไซต์มีการตั้งค่าเป็นข้อมูลบังคับ และต้องป้อนบนธุรกรรมความต้องการ
-   ไม่ได้ตั้งค่ามิติคลังสินค้าเป็นข้อมูลบังคับ คุณอาจจะทราบคลังสินค้า แต่มันไม่ได้ใช้ในการคำนวณการวางแผนหลัก
-   มิติไซต์ตั้งค่าสำหรับการวางแผนความครอบคลุม
-   มิติคลังสินค้าไม่ได้ตั้งค่าสำหรับการวางแผนความครอบคลุม ดังนั้น การจัดหาวัสดุและความต้องการถูกรวมโดยไซต์ และอาจรวมถึงมิติความครอบคลุมที่วางแผนอื่นด้วย

รูปภาพต่อไปนี้แสดงวิธีการประมวลผลการวางแผนหลัก พารามิเตอร์ที่มีการอ้างอิงในรูปภาพ และตำแหน่งของพารามิเตอร์เหล่านั้นมีดังต่อไปนี้
-   มีการกำหนดความครอบคลุมสินค้าสำหรับสินค้า คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้** เลือกสินค้า และคลิก **วางแผน &gt; ความครอบคลุมสินค้า**
-   มีการกำหนดความสัมพันธ์ในการเติมสินค้าสำหรับคลังสินค้า  คลิก **การบริหารสินค้าคงคลัง &gt; การตั้งค่า &gt; แบ่งสินค้าคงคลัง &gt; คลังสินค้า** บนแท็บ **การวางแผนหลัก** ดูกลุ่มฟิลด์ **คลังสินค้าหลัก**
-   ใบสั่งประเภทใบสั่งเริ่มต้นที่ถูกตั้งค่าเป็นการผลิต ใบสั่งซื้อหรือคัมบัง คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์&gt; ผลิตภัณฑ์ที่นำออกใช้** เลือกสินค้า และคลิก **วางแผน &gt; การตั้งค่าใบสั่งเริ่มต้น** ในฟอร์ม **การตั้งค่าใบสั่งเริ่มต้น** ดูฟิลด์ **ประเภทใบสั่งเริ่มต้น**

![ความต้องการความครอบคลุมไซต์ที่ไม่จำเป็นต้องมีคลังสินค้า](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ภาพรวมของการวางแผนหลักและฟังก์ชันหลายไซต์](master-plan-multisite-functionality.md)
- [การวางแผนหลักสำหรับความครอบคลุมไซต์และคลังสินค้า จำเป็นต้องมีคลังสินค้า](master-plan-site-coverage-warehouse-mandatory.md)
- [การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าบังคับ](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [การวางแผนหลักสำหรับความครอบคลุมไซต์ คลังสินค้าไม่บังคับ](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [กำหนดเวอร์ชันสูตรการผลิต](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]