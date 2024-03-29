---
title: นำโครงสร้างผลิตภัณฑ์ออกใช้
description: บทความนี้อธิบายวิธีการที่คุณสามารถนำโครงสร้างผลิตภัณฑ์ที่เสร็จสมบูรณ์ออกใช้นอกเหนือจากการนำผลิตภัณฑ์ออกใช้ร่วมกับรุ่นวิศวกรรม ด้วยวิธีนี้ คุณสามารถตรวจสอบให้แน่ใจว่าข้อมูลผลิตภัณฑ์ที่เกี่ยวข้องกับวิศวกรรมสามารถนำมาใช้ใหม่ในนิติบุคคลที่แตกต่างกันได้
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c8359f86e5123ee40e9673971de626e1b327ac95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875494"
---
# <a name="release-product-structures"></a>นำโครงสร้างผลิตภัณฑ์ออกใช้

[!include [banner](../includes/banner.md)]

เมื่อต้องการตรวจสอบให้แน่ใจว่าข้อมูลผลิตภัณฑ์ที่เกี่ยวข้องกับวิศวกรรมสามารถนำมาใช้ใหม่ในนิติบุคคลต่าง ๆ คุณสามารถนำโครงสร้างผลิตภัณฑ์ที่เสร็จสมบูรณ์ออกใช้นอกเหนือจากการนำผลิตภัณฑ์ออกใช้ร่วมกับรุ่นวิศวกรรมได้ ดังนั้น คุณจึงสามารถนำโครงสร้างของสูตรการผลิต (BOM) หลายระดับออกใช้ด้วยกันกับโครงสร้างหลักในการดำเนินการนำออกใช้เดียว ในกรณีนี้ BOM และผลิตภัณฑ์ระดับล่างจะถูกนำออกใช้ด้วยเช่นกัน

ผลิตภัณฑ์วิศวกรรมมีการสร้างและรักษาโดยบริษัทวิศวกรรมในลักษณะที่เป็นไปตามข้อกำหนดด้านคุณภาพตามที่ได้รับการออกแบบ บริษัทที่ดำเนินงานแต่ละแห่งที่ผลิตผลิตภัณฑ์ต้องมีผลิตภัณฑ์เดียวกันและ BOM พื้นฐาน ขึ้นอยู่กับสิ่งอำนวยความสะดวกในการผลิต กระบวนการผลิตอาจถูกสร้างขึ้นภายในเครื่อง ในกรณีนี้ คุณจะไม่นำกระบวนการผลิตออกใช้ร่วมกับผลิตภัณฑ์ สำหรับนิติบุคคลที่จะขายผลิตภัณฑ์แต่จะไม่ทำการผลิต BOM อาจไม่จำเป็น

เมื่อต้องการให้กระบวนการมีประสิทธิภาพมากขึ้น ข้อมูลที่เกี่ยวข้องกับวิศวกรรมทั้งหมดสามารถนำมาใช้กับบริษัทที่ดำเนินงานอื่น ๆ ในเวลาเดียวกันได้ ข้อมูลนี้รวมถึงโครงสร้างผลิตภัณฑ์ ในระหว่างกระบวนการนำออกใช้ คุณสามารถเลือกส่วนของข้อมูลผลิตภัณฑ์ที่ควรนำออกใช้

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบริษัทวิศวกรรมและบริษัทที่ดำเนินงาน โปรดดู [บริษัทวิศวกรรมและกฎความเป็นเจ้าของข้อมูล](engineering-org-data-ownership-rules.md)

โปรดทราบว่าคุณสามารถนำทั้งผลิตภัณฑ์พื้นฐานและผลิตภัณฑ์วิศวกรรมออกใช้ร่วมกับโครงสร้างผลิตภัณฑ์ที่นำออกใช้ ในระหว่างกระบวนการนี้ โครงสร้างผลิตภัณฑ์ทั้งหมดจะถูกนำออกใช้ แม้กระทั่ง BOM และกระบวนการผลิตจากบริษัทที่มีการนำผลิตภัณฑ์ออกใช้

สำหรับตัวอย่างของวิธีการนำผลิตภัณฑ์ออกใช้ ให้ดูที่ [นำผลิตภัณฑ์วิศวกรรมออกใช้กับบริษัทในพื้นที่](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>ใช้ข้อมูลที่นำออกใช้สำหรับผลิตภัณฑ์เมื่อใช้โครงสร้างผลิตภัณฑ์ที่นำออกใช้

ข้อมูลต่อไปนี้จะรวมอยู่ในการนำผลิตภัณฑ์วิศวกรรมออกใช้:

- **ข้อมูลผลิตภัณฑ์** – สร้างผลิตภัณฑ์ที่นำออกใช้ใหม่
- **ข้อมูลรุ่นวิศวกรรม** – รุ่นวิศวกรรมและข้อมูลถูกสร้างหรืออัปเดต โปรดทราบว่าถ้าคุณนำรุ่นวิศวกรรมเดียวกันออกใช้อีกครั้งกับบริษัทที่ดำเนินงาน ระบบจะเขียนทับข้อมูลวิศวกรรม
- **แอททริบิวต์วิศวกรรม** – แอททริบิวต์ด้านวิศวกรรมและค่าของแอททริบิวต์ถูกสร้างหรืออัพเดต
- **สูตรการผลิตวิศวกรรม** – BOM ด้านวิศวกรรมและรายการสามารถสร้างหรืออัพเดตได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความเป็นเจ้าของข้อมูล ให้ดูที่ [ความเป็นเจ้าของผลิตภัณฑ์](product-owner.md)
- **กระบวนการผลิตด้านวิศวกรรม** – กระบวนการผลิตด้านวิศวกรรมและการดำเนินงานของแอททริบิวต์สามารถสร้างหรืออัพเดตได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความเป็นเจ้าของข้อมูล ให้ดูที่ [ความเป็นเจ้าของผลิตภัณฑ์](product-owner.md)
- **เอกสารด้านวิศวกรรม** – เอกสารทางวิศวกรรมที่เชื่อมโยงกับรุ่นวิศวกรรมจะถูกสร้างหรืออัพเดต

เมื่อคุณเปิดใช้งานการจัดการการเปลี่ยนแปลงทางวิศวกรรมบนระบบของคุณ โครงสร้างผลิตภัณฑ์ที่นำออกใช้จะพร้อมใช้งาน นอกจากนี้ ผลิตภัณฑ์มาตรฐานจะรวม BOM และกระบวนการผลิตเมื่อมีการนำออกใช้

## <a name="product-acceptance"></a>การยอมรับผลิตภัณฑ์

**การยอมรับผลิตภัณฑ์** เป็นพารามิเตอร์หลักที่มีผลกระทบต่อกระบวนการนำออกใช้ คุณสามารถตั้งค่าพารามิเตอร์นี้สำหรับแต่ละบริษัทโดยไปที่ **การจัดการการเปลี่ยนแปลงทางวิศวกรรม \> การตั้งค่า \> พารามิเตอร์การจัดการการเปลี่ยนแปลงทางวิศวกรรม** สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [พารามิเตอร์การจัดการการเปลี่ยนแปลงทางวิศวกรรม](engineering-parameters.md)

### <a name="automatic-product-acceptance"></a>การยอมรับผลิตภัณฑ์โดยอัตโนมัติ

การนำออกใช้ของผลิตภัณฑ์วิศวกรรมแต่ละรุ่นจะเริ่มต้นเมื่อใครสักคนจากบริษัทวิศวกรรมเลือกผลิตภัณฑ์ที่จะนำออกใช้ เมื่อพารามิเตอร์ **การยอมรับผลิตภัณฑ์** มีการตั้งค่าเป็น *อัตโนมัติ* ผู้ใช้ที่บริษัทวิศวกรรมจะตัดสินใจว่าควรนำข้อมูลผลิตภัณฑ์ใดไปใช้กับบริษัทที่ดำเนินงานโดยอัตโนมัติ ผลิตภัณฑ์จะถูกนำออกใช้โดยอัตโนมัติไปยังบริษัทที่เลือกในตัวช่วยสร้างการนำออกใช้

### <a name="manual-product-acceptance"></a>การยอมรับผลิตภัณฑ์ด้วยตนเอง

การนำออกใช้ของผลิตภัณฑ์วิศวกรรมแต่ละรุ่นจะเริ่มต้นเมื่อใครสักคนจากบริษัทวิศวกรรมเลือกผลิตภัณฑ์ที่จะนำออกใช้ เมื่อพารามิเตอร์ **การยอมรับผลิตภัณฑ์** มีการตั้งค่าเป็น *ด้วยตนเอง* ผู้ใช้ที่บริษัทวิศวกรรมจะตัดสินใจว่าควรนำข้อมูลผลิตภัณฑ์ใดไปใช้กับบริษัทที่ดำเนินงาน ผู้ใช้จากแต่ละบริษัทที่ดำเนินงานตรวจสอบความถูกต้องของข้อมูลผลิตภัณฑ์และตัดสินใจว่าจะยอมรับการนำออกใช้หรือไม่ ผู้ใช้ที่บริษัทที่ดำเนินงานสามารถกำหนดตัวเลือกต่อไปนี้เมื่อได้รับข้อมูล:

- ถ้าผลิตภัณฑ์ (การอัปเดต) ไม่เกี่ยวข้องกับบริษัทที่ดำเนินงาน ผู้ใช้จะสามารถเลือกที่จะไม่ยอมรับการนำออกใช้
- ผู้ใช้สามารถเปลี่ยนแม่แบบรายการสำหรับผลิตภัณฑ์ใหม่ได้
- ผู้ใช้สามารถเลือกว่าควรมีการนำผลิตภัณฑ์ออกใช้ร่วมกับ BOM และ/หรือกระบวนการผลิตหรือไม่ และกำหนดว่าควรมีการนำผลิตภัณฑ์ออกใช้เป็นอนุมัติและใช้งานอยู่หรือไม่
- ผู้ใช้สามารถเปลี่ยนแปลงวันที่เริ่มต้นที่มีผลบังคับใช้ของผลิตภัณฑ์

สำหรับตัวอย่างของวิธีการยอมรับผลิตภัณฑ์ ให้ดูที่ [ตรวจทานและยอมรับผลิตภัณฑ์ก่อนที่คุณจะนำออกใช้ในบริษัทในพื้นที่](engineering-scenarios.md#accept)

> [!NOTE]
> สำหรับผลิตภัณฑ์มาตรฐาน คุณสามารถนำออกใช้จากนิติบุคคลใด ๆ กับนิติบุคคลอื่น ๆ สำหรับผลิตภัณฑ์วิศวกรรม นิติบุคคลเดียวที่คุณสามารถนำออกใช้ได้เป็นบริษัทวิศวกรรมเท่านั้น

## <a name="release-policies"></a>นโยบายการนำออกใช้

บริษัทที่ดำเนินงานทั้งหมดไม่จำเป็นต้องใช้ข้อมูลผลิตภัณฑ์เดียวกัน โดยทั่วไป บริษัทดำเนินงานที่ผลิตผลิตภัณฑ์วิศวกรรมต้องใช้ BOM ในขณะที่บริษัทดำเนินงานที่จำหน่ายผลิตภัณฑ์ทางวิศวกรรมเท่านั้นที่ไม่จำเป็นต้องใช้ BOM คุณสามารถใช้นโยบายการนำออกใช้เพื่อสร้างพารามิเตอร์ที่จะใช้สำหรับการนำผลิตภัณฑ์ออกใช้

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับประเภทผลิตภัณฑ์วิศวกรรม ดูที่ [ประเภทผลิตภัณฑ์วิศวกรรมและรุ่นวิศวกรรม](engineering-versions-product-category.md)

ในระหว่างกระบวนการนำออกใช้ คุณสามารถมีอิทธิพลต่อการตั้งค่าได้

## <a name="create-and-manage-product-release-policies"></a>สร้างและจัดการนโยบายการนำออกใช้ของผลิตภัณฑ์

เมื่อต้องการทำงานกับนโยบายการนำออกใช้ของผลิตภัณฑ์ ให้ไปที่ **การจัดการการเปลี่ยนแปลงทางวิศวกรรม \> การตั้งค่า \> นโยบายการนำออกใช้ของผลิตภัณฑ์** จากนั้น ทำตามหนึ่งในขั้นตอนเหล่านี้

- เมื่อต้องการสร้างนโยบายใหม่ ให้เลือก **สร้าง** ในบานหน้าต่างการดำเนินการ แล้วกำหนดฟิลด์ตามที่อธิบายไว้ในส่วนย่อยต่อไปนี้
- ถ้าต้องการแก้ไขนโยบายที่มีอยู่ ให้เลือกนโยบายในบานหน้าต่างรายการ เลือก **แก้ไข** บนบานหน้าต่างการดำเนินการ แล้วกำหนดฟิลด์ตามที่อธิบายไว้ในส่วนย่อยต่อไปนี้
- ถ้าต้องการลบนโยบายที่มีอยู่ ให้เลือกนโยบายในบานหน้าต่างรายการ เลือก **แก้ไข** บนบานหน้าต่างการดำเนินการ จากนั้นบนแท็บด่วน **ทั่วไป** โปรดตรวจสอบให้แน่ใจว่าตัวเลือก **ที่ใช้งานอยู่** ตั้งค่าเป็น *ไม่* จากนั้น เลือก **ลบ** บนบานหน้าต่างการดำเนินการ

### <a name="header"></a>หัวข้อ

ตั้งค่าฟิลด์ต่อไปนี้บนส่วนหัวของนโยบายการนำออกใช้ของผลิตภัณฑ์

| ฟิลด์ | คำอธิบาย |
|---|---|
| ชื่อ | ป้อนชื่อสำหรับนโยบาย |
| คำอธิบาย | ป้อนคำอธิบายเกี่ยวกับนโยบาย |

### <a name="general-fasttab"></a>FastTab ทั่วไป

ตั้งค่าฟิลด์ต่อไปนี้บนแท็บด่วน **ทั่วไป** ของนโยบายการนำออกใช้ของผลิตภัณฑ์

| ฟิลด์ | คำอธิบาย |
|---|---|
| ชนิดผลิตภัณฑ์ | เลือกว่ามีนโยบายใช้กับผลิตภัณฑ์ของชนิด *สินค้า* หรือ *การบริการ* คุณไม่สามารถเปลี่ยนการตั้งค่านี้ได้หลังจากที่คุณบันทึกเรกคอร์ดแล้ว |
| ชนิดการผลิต | ฟิลด์นี้จะปรากฏเฉพาะเมื่อคุณได้เปิดใช้งาน [การจัดการการเปลี่ยนแปลงสูตร](manage-formula-changes.md) ในระบบของคุณเท่านั้น เลือกชนิดของการผลิตที่จะใช้นโยบายการนำออกใช้นี้<ul><li>**สินค้าร่วม** – ใช้นโยบายการนำออกใช้เพื่อจัดการสินค้าร่วม สินค้าร่วมจะถูกผลิตในระหว่างกระบวนการผลิต และไม่ได้ผลิตผลิตภัณฑ์รุ่นหรือผลิตภัณฑ์วิศวกรรม นโยบายการนำออกใช้ในผลิตภัณฑ์ร่วมสามารถช่วยให้มั่นใจว่ามีการตั้งค่าที่สําคัญ เช่น **กลุ่มมิติการจัดเก็บ** และ **กลุ่มมิติการติดตาม** มีการตั้งค่าโดยใช้เท็มเพลตผลิตภัณฑ์ที่นำออกใช้ในบริษัทก่อนการผลิต</li><li>**สินค้าพลอยได้** – ใช้นโยบายการนำออกใช้เพื่อจัดการสินค้าพลอยได้ สินค้าพลอยได้จะถูกผลิตในระหว่างกระบวนการผลิต และไม่ได้ผลิตผลิตภัณฑ์รุ่นหรือผลิตภัณฑ์วิศวกรรม นโยบายการนำออกใช้ในสินค้าพลอยได้สามารถช่วยให้มั่นใจว่ามีการตั้งค่าที่สําคัญ เช่น **กลุ่มมิติการจัดเก็บ** และ **กลุ่มมิติการติดตาม** มีการตั้งค่าโดยใช้แม่แบบผลิตภัณฑ์ที่นำออกใช้ในบริษัทก่อนการผลิต</li><li>**ไม่มี** – ใช้นโยบายนี้เพื่อจัดการผลิตภัณฑ์มาตรฐานที่ไม่ใช่ผลิตภัณฑ์ที่มีรุ่นหรือวิศวกรรม หรือสินค้าร่วมหรือสินค้าพลอยได้</li><li>**สินค้าที่วางแผน** – ใช้นโยบายการนำออกใช้ลงในสายการผลิตนี้เพื่อจัดการสินค้าการวางแผนที่ผลิตโดยใช้การผลิตตามกระบวนการ สินค้าที่วางแผนใช้สูตร ซึ่งจะคล้ายคลึงกับสินค้าตามสูตร แต่ใช้ในการผลิตสินค้าร่วมและสินค้าร่วมและสินค้าพลอยได้เท่านั้น แต่จะใช้เพื่อผลิตผลิตภัณฑ์ร่วมและสินค้าพลอยได้ที่ไม่เสร็จสิ้น</li><li>**BOM** – ใช้นโยบายการนำออกใช้เพื่อจัดการผลิตภัณฑ์วิศวกรรม ซึ่งไม่ได้ใช้สูตรและโดยทั่วไป (แต่ไม่จำเป็นต้อง)รวม BOM ด้วย</li><li>**สูตร** – ใช้นโยบายการนำออกใช้ลงในสายการผลิตนี้เพื่อจัดการสินค้าที่เสร็จสิ้นที่ผลิตโดยใช้การผลิตตามกระบวนการ สินค้าเหล่านี้จะมีสูตร แต่ไม่ใช่สูตรการผลิต</li></ul> |
| ใช้เท็มเพลต | เลือกตัวเลือกอย่างใดอย่างหนึ่งต่อไปนี้เพื่อระบุว่าควรจะใช้แม่แบบการนำออกใช้ผลิตภัณฑ์อย่างไรเมื่อมีการใช้นโยบายดังนี้<ul><li>**เสมอ** – ผลิตภัณฑ์ที่นำออกใช้แม่แบบต้องใช้สำหรับการผลิตออกใช้เสมอ ถ้าคุณเลือกตัวเลือกนี้ ให้ใช้แท็บด่วน **ผลิตภัณฑ์ทั้งหมด** เพื่อระบุแม่แบบที่ใช้สำหรับแต่ละบริษัทที่คุณนำออกใช้ด้วย ถ้าคุณไม่ได้ระบุแม่แบบสำหรับบริษัทแต่ละแห่งที่แสดงรายการอยู่บนแท็บด่วน **ผลิตภัณฑ์ทั้งหมด** คุณจะได้รับข้อผิดพลาดเมื่อพยายามบันทึกนโยบาย</li><li>**ไม่จำเป็นต้องระบุ** – ถ้ามีการระบุผลิตภัณฑ์ที่นำออกใช้แม่แบบสำหรับบริษัทที่แสดงรายการอยู่บนแท็บด่วน **ผลิตภัณฑ์ทั้งหมด** แม่แบบนี้จะมีการใช้เมื่อคุณนำออกใช้กับบริษัทนั้น มิฉะนั้น จะไม่มีการใช้แม่แบบ ถ้าคุณเลือกตัวเลือกนี้ คุณสามารถบันทึกนโยบายโดยไม่มีการกำหนดแม่แบบในบริษัททั้งหมด (ไม่มีการแจ้งเตือนแสดงขึ้น)</li><li>**ไม่เคย** – ไม่มีการใช้ผลิตภัณฑ์ที่นำออกใช้แม่แบบสำหรับบริษัทใด ๆ ที่คุณนำออกใช้ แม้ว่ามีการระบุแม่แบบสำหรับบริษัทที่แสดงรายการอยู่บนแท็บด่วน **ผลิตภัณฑ์ทั้งหมด** คอลัมน์แม่แบบจะไม่พร้อมใช้งาน</li></ul> |
| ที่ใช้งานอยู่ | ใช้ตัวเลือกนี้เพื่อรักษานโยบายการนำออกใช้ของคุณ ตั้งค่าเป็น *ใช่* สำหรับนโยบายการนำออกใช้ทั้งหมดที่คุณใช้ ตั้งค่าเป็น *ไม่* เพื่อทำเครื่องหมายนนโยบายการนำออกใช้เป็นไม่ได้ใช้งานอยู่เมื่อไม่ใช้งาน โปรดทราบว่าคุณไม่สามารถยกเลิกการเรียกใช้นโยบายการนำออกใช้ที่กำหนดให้กับประเภทผลิตภัณฑ์วิศวกรรม และคุณสามารถลบได้เฉพาะนโยบายการนำออกใช้ที่ไม่ได้ใช้งานอยู่เท่านั้น |

### <a name="all-products-fasttab"></a>แท็บด่วน ผลิตภัณฑ์ทั้งหมด

บนแท็บด่วน **ผลิตภัณฑ์ทั้งหมด** ให้เพิ่มแถวสำหรับบริษัทที่ดำเนินงานแต่ละแห่งที่คุณต้องการใช้นโยบายนี้เพื่อนำออกใช้ ใช้ปุ่มต่อไปนี้บนแท็บด่วน **ผลิตภัณฑ์ทั้งหมด** เพื่อเพิ่มและลบแถวตามที่คุณต้องการ: สำหรับแต่ละแถวที่คุณเพิ่ม ให้ตั้งค่าฟิลด์ต่อไปนี้

> [!NOTE]
> การตั้งค่าบนแท็บด่วน **ผลิตภัณฑ์ทั้งหมด** จะใช้กับผลิตภัณฑ์ทางวิศวกรรมและผลิตภัณฑ์มาตรฐาน

| ฟิลด์ | คำอธิบาย |
|---|---|
| รหัสบัญชีบริษัท | เลือกบริษัทที่จะใช้แถว พารามิเตอร์ของแถวจะใช้เมื่อมีการนำผลิตภัณฑ์ออกใช้กับบริษัทนี้ |
| ผลิตภัณฑ์ที่นำออกใช้ในเท็มเพลต | เพิ่มแม่แบบสำหรับผลิตภัณฑ์ |
| คัดลอกการอนุมัติ BOM | เลือกกล่องกาเครื่องหมายนี้เพื่อคัดลอกสถานะการอนุมัติ BOM ไปยังบริษัทที่รับ |
| คัดลอกการเปิดใช้งาน BOM | เลือกกล่องกาเครื่องหมายนี้เพื่อคัดลอกสถานะการเรียกใช้ BOM ไปยังบริษัทที่รับ |
| คัดลอกการอนุมัติกระบวนการผลิต | เลือกกล่องกาเครื่องหมายนี้เพื่อคัดลอกสถานะการอนุมัติกระบวนการผลิตไปยังบริษัทที่รับ|
| คัดลอกการเปิดใช้งานกระบวนการผลิต | เลือกกล่องกาเครื่องหมายนี้เพื่อคัดลอกสถานะการเรียกใช้กระบวนการผลิตไปยังบริษัทที่รับ |

### <a name="option-parameters-for-engineering-products-fasttab"></a>พารามิเตอร์ตัวเลือกสำหรับแท็บด่วนผลิตภัณฑ์วิศวกรรม

ทุกครั้งที่คุณเพิ่มแถวบนแท็บด่วน **ผลิตภัณฑ์ทั้งหมด** แถวที่มีค่า **รหัสบัญชีบริษัท** ที่ตรงกันจะถูกสร้างขึ้นบนแท็บด่วน **พารามิเตอร์ตัวเลือกสำหรับผลิตภัณฑ์วิศวกรรม** จากนั้น หากคุณเพิ่มแถวจากแท็บด่วน **ผลิตภัณฑ์ทั้งหมด** แถวที่มีค่า **รหัสบัญชีบริษัท** ที่ตรงกันจะถูกนำออกจากแท็บด่วน **พารามิเตอร์ตัวเลือกสำหรับผลิตภัณฑ์วิศวกรรม**

สำหรับแต่ละแถวที่แสดงอยู่บนแท็บด่วน **พารามิเตอร์ตัวเลือกสำหรับผลิตภัณฑ์วิศวกรรม** ให้ตั้งค่าฟิลด์ต่อไปนี้

> [!NOTE]
> การตั้งค่าบนแท็บด่วน **พารามิเตอร์ตัวเลือกสำหรับผลิตภัณฑ์ทางวิศวกรรม** ใช้กับผลิตภัณฑ์วิศวกรรมเท่านั้น

| ฟิลด์ | คำอธิบาย |
|---|---|
| BOM เท็มเพลต | เมื่อมีการนำผลิตภัณฑ์ที่มีการนำออกใช้ BOM บรรทัดของ BOM แม่แบบที่ระบุจะมีการเพิ่ม ฟิลด์นี้มีประโยชน์สำหรับการเพิ่มส่วนประกอบเฉพาะที่ เช่น บรรจุภัณฑ์หรือคำสั่งในภาษาท้องถิ่น |
| กระบวนการผลิตของเท็มเพลต | เมื่อมีการนำผลิตภัณฑ์ที่มีการนำออกใช้กระบวนการผลิต บรรทัดของแม่แบบที่ระบุจะมีการเพิ่ม |
| การมีผลบังคับใช้ของการคัดลอก | เลือกว่าควรมีการคัดลอกวันที่มีผลบังคับใช้จากบริษัทวิศวกรรมกับบริษัทที่ดำเนินงานเมื่อคุณนำผลิตภัณฑ์ออกใช้หรือไม่ |
| เพิ่มโดยอัตโนมัติในข้อเสนอการนำออกใช้ | เลือกกล่องกาเครื่องหมายนี้สำหรับผลิตภัณฑ์ที่จะนำออกใช้โดยอัตโนมัติในใบสั่งการเปลี่ยนแปลงทางวิศวกรรม ด้วยวิธีนี้ ผลิตภัณฑ์ที่เป็นประเภทผลิตภัณฑ์วิศวกรรมที่ใช้นโยบายการนำออกใช้นี้สามารถนำออกใช้กับบริษัทที่ดำเนินงานที่มีการตั้งค่าตัวเลือกนี้ได้โดยอัตโนมัติ (สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [จัดการการเปลี่ยนแปลงที่เกิดขึ้นกับผลิตภัณฑ์วิศวกรรม](engineering-change-management.md))

### <a name="review-each-product-when-you-release-it"></a>ตรวจทานผลิตภัณฑ์แต่ละรายการเมื่อคุณนำออกใช้

เมื่อมีการนำออกใช้ผลิตภัณฑ์วิศวกรรมที่มี BOM หรือกระบวนการผลิตแล้ว พารามิเตอร์จะมีการตั้งค่าเป็นค่าเริ่มต้น ตามที่ระบุไว้ในนโยบายการนำออกใช้ ในฐานะผู้ใช้ คุณสามารถมีอิทธิพลต่อลักษณะการทำงานนี้ในด้านการนำออกใช้เมื่อคุณใช้โครงสร้างผลิตภัณฑ์นำออกใช้

เมื่อต้องการปล่อยผลิตภัณฑ์วิศวกรรม บนหน้า **ผลิตภัณฑ์ที่นำออกใช้** ให้เลือกผลิตภัณฑ์ที่จะนำออกใช้ แล้วเลือก **นำโครงสร้างผลิตภัณฑ์ออกใช้** เพื่อเปิดตัวช่วยสร้างการนำออกใช้ หน้า **เลือกผลิตภัณฑ์วิศวกรรมเพื่อนำออกใช้** แสดงผลิตภัณฑ์ เลือกผลิตภัณฑ์เดียว แล้วเลือก **รายละเอียดการนำออกใช้** เพื่อดูรายละเอียดการนำออกใช้สำหรับผลิตภัณฑ์

บนหน้า **รายละเอียดการนำออกใช้** คุณสามารถเปลี่ยนค่าของฟิลด์ **BOM ที่ได้รับ** **คัดลอกการอนุมัติ BOM** **คัดลอกการเรียกใช้ BOM** **รับ BOM** **คัดลอกการอนุมัติกระบวนการผลิต** และ **คัดลอกการเรียกใช้กระบวนการผลิต** ในสถานการณ์จำลองการดึงข้อมูล คุณสามารถเปลี่ยนค่าของฟิลด์เดียวกันในด้านการรับสินค้า ที่มีการนำ BOM และกระบวนการผลิตออกใช้

## <a name="product-owners-and-product-releases"></a>เจ้าของผลิตภัณฑ์และผลิตภัณฑ์ที่นำออกใช้

เนื่องจากเจ้าของผลิตภัณฑ์ทราบว่านิติบุคคลใดที่จำเป็นต้องใช้ผลิตภัณฑ์ของพวกเขา ผลิตภัณฑ์สามารถนำออกใช้ได้โดยสมาชิกของกลุ่มเจ้าของผลิตภัณฑ์นั้นเท่านั้น ผู้ใช้อื่นไม่สามารถนำผลิตภัณฑ์ที่ไม่ได้เป็นเจ้าของออกใช้ได้

ลักษณะการทำงานนี้จะใช้เฉพาะเมื่อมีการเลือกผลิตภัณฑ์สำหรับการนำออกใช้โดยตรง ผลิตภัณฑ์ที่เป็นส่วนหนึ่งของโครงสร้างของผลิตภัณฑ์อื่นผ่านทาง BOM *สามารถ* นำออกใช้โดยผู้ใช้ที่ไม่ใช่เจ้าของ เมื่อผู้ใช้เหล่านั้นนำออกใช้ผลิตภัณฑ์หลัก ถ้าพวกเขาเป็นเจ้าของผลิตภัณฑ์หลัก

ตัวอย่างเช่น มีการกำหนดผลิตภัณฑ์ X ให้กับกลุ่มเจ้าของผลิตภัณฑ์ *การออกแบบตู้* ผลิตภัณฑ์ X ยังเป็นส่วนหนึ่งของ BOM ของผลิตภัณฑ์ Y ซึ่งกำหนดให้กับกลุ่มเจ้าของผลิตภัณฑ์ *ออกแบบลำโพง* ถ้าผู้ใช้จากกลุ่มเจ้าของผลิตภัณฑ์ *ออกแบบลำโพง* นำออกใช้ผลิตภัณฑ์ Y และ BOM ผลิตภัณฑ์ X จะถูกนำออกใช้ร่วมกับผลิตภัณฑ์ Y

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เจ้าของผลิตภัณฑ์](product-owner.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
