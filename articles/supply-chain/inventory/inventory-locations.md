---
title: สถานที่เก็บสินค้าคงคลัง
description: สถานที่เก็บสินค้าคงคลังจะใช้กับคลังสินค้าพื้นฐาน (WMS I) เพื่อกำหนดที่จัดเก็บสินค้าและเบิกสินค้าในคลังสินค้า WMS
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd5ad086cadd2e49585614e7650bb7e30a4e7328
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888599"
---
# <a name="inventory-locations"></a>สถานที่เก็บสินค้าคงคลัง

[!include [banner](../includes/banner.md)]

สถานที่เก็บสินค้าคงคลังจะใช้กับคลังสินค้าพื้นฐาน (WMS I) เพื่อกำหนดที่จัดเก็บสินค้าและเบิกสินค้าในคลังสินค้า WMS

บทความนี้ใช้กับลักษณะการทำงานในโมดูลการบริหารสินค้าคงคลัง ไม่นำไปใช้กับลักษณะการทำงานในโมดูลการบริหารคลังสินค้า

คำว่า สถานที่ หมายถึงสถานที่ที่สินค้าถูกเก็บและถูกนำออกมา

สำหรับแต่ละสถานที่ สถานที่ที่มีสินค้าถูกเก็บสามารถระบุได้ด้วย โดยค่าเริ่มต้น พวกเขาจะเหมือนกัน โดยปกติสินค้าจะถูกเก็บและนำสินค้าออกจากสถานที่เก็บด้านเดียวกัน แต่ก็ไม่เสมอไป ตัวอย่างเช่น สินค้าที่ถูกจัดเก็บในชั้นเก็บสินค้าของที่จัดเก็บของสดจะถูกใส่จากที่เก็บหนึ่งและถูกนำออกใช้จากอีกที่หนึ่ง อินพุตหลักถูกกำหนด โดยชื่อสถานที่ ซึ่งโดยปกติถูกกำหนด โดยระยะพิกัด: คลังสินค้า ที่เก็บ ชั้นเก็บสินค้า ชั้น และช่องเก็บ ชื่อหรือรหัสนี้สามารถป้อนด้วยตนเอง หรือสร้างจากระยะพิกัดสถานที่—ตัวอย่างเช่น 01-02-03-4 สำหรับที่เก็บ 1 ชั้นเก็บสินค้า 2 ชั้น 3 ช่องเก็บ 4 ในหน้าสถานที่เก็บสินค้าคงคลัง
คุณสมบัติของสถานที่เก็บ

สถานที่เก็บจะมีลักษณะดังต่อไปนี้
-   ขนาด (ความสูง ความกว้าง ความลึก และตามปริมาตร)
-   ตำแหน่งคลังสินค้า ที่เก็บ ชั้นเก็บสินค้า ชั้น และช่องเก็บ
-   ชนิดของสถานที่ (สถานที่เก็บสินค้าจำนวนมาก สถานที่เบิกสินค้า ท่าสินค้าขาเข้า ท่าสินค้าขาออก สถานที่ตั้งอินพุทการผลิต สถานที่ตรวจสอบ หรือซุปเปอร์มาร์เก็ตคัมบัง)

ตรวจสอบข้อความสามารถใช้ในระบบออนไลน์เพื่อตรวจสอบว่า ผู้ปฏิบัติงานได้เลือกสถานที่ที่ถูกต้องสำหรับสินค้าที่ระบุไว้ ข้อความการตรวจสอบนี้สามารถสร้างได้ด้วยตนเองหรือโดยค่าเริ่มต้น

## <a name="sort-codes"></a>รหัสการเรียงลำดับ
ใช้รหัสการเรียงลำดับเพื่อเพิ่มประสิทธิภาพในการจัดการรายการเบิกสินค้า ซึ่งอธิบายข้อมูลที่จำเป็นสำหรับการเบิกสินค้าจากสินค้าคงคลัง รวมถึงใบสั่งการเบิกสินค้า รหัสการเรียงลำดับสามารถระบุตามที่เก็บและระยะพิกัดอื่น ๆ หรือกำหนดด้วยตนเองสำหรับสถานที่

## <a name="blocked-locations"></a>สถานที่เก็บที่ถูกบล็อค
บางครั้ง คุณอาจต้องการระบุว่า สถานที่ที่ถูกบล็อคสำหรับรอบระยะเวลา ตัวอย่างเช่น ต้องอนุญาตเพื่อซ่อมแซม ในบางครั้ง คุณอาจต้องการระบุการบล็อคเฉพาะของอินพุตหรือเอาท์พุทเท่านั้น

## <a name="tree-structure"></a>โครงสร้างแผนภูมิ

ในหน้าสถานที่เก็บสินค้าคงคลัง คุณสามารถดูโครงร่างของคลังสินค้าในโครงสร้างแผนภูมิตามระยะพิกัดของสถานที่เก็บสินค้าคงคลัง ในรูปแบบการแสดงที่กำหนด

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>รักษาสถานที่เก็บสินค้าคงคลัง ผ่านทางแบบฟอร์มคลังสินค้า

เป็นไปได้ที่คัดลอกสถานที่จากคลังสินค้าหนึ่งไปยังอีกที่หนึ่ง และสร้างสถานที่ผ่านทางวิซาร์ด ก่อนที่คุณรันวิซาร์ด คุณควรตรวจสอบให้แน่ใจว่า คุณได้กำหนดชื่อสถานที่เริ่มต้นบนหน้าคลังสินค้า



## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[สร้างการจัดวางพื้นที่คลังสินค้าใหม่](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]