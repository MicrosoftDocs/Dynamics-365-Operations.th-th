---
title: โมดูลการให้คะแนนและบทวิจารณ์
description: บทความนี้ครอบคลุมโมดูลการจัดอันดับและบทวิจารณ์ที่ใช้ในหน้ารายละเอียดของผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ede42caac78dc48fa6315a2d3c22f1e0f12f0810
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283599"
---
# <a name="ratings-and-reviews-modules"></a>โมดูลการให้คะแนนและบทวิจารณ์

[!include [banner](includes/banner.md)]

บทความนี้ครอบคลุมโมดูลการจัดอันดับและบทวิจารณ์ที่ใช้ในหน้ารายละเอียดของผลิตภัณฑ์ (PDPs) ใน Microsoft Dynamics 365 Commerce

การจัดอันดับและบทวิจารณ์บนเว็บไซต์อีคอมเมิร์ซช่วยให้ลูกค้าเรียนรู้เกี่ยวกับผลิตภัณฑ์ก่อนที่พวกเขาทำการตัดสินใจซื้อ และยังเป็นกลไกสำหรับการรวบรวมข้อคิดเห็นของลูกค้าเกี่ยวกับผลิตภัณฑ์ 

การให้คะแนนแสดงอยู่บนหน้ารายการผลิตภัณฑ์ หน้ารายการประเภท หน้าผลการค้นหา และหน้าไซต์อื่น ๆ 

กราฟแสดงค่าสถิติความถี่ของการให้คะแนนและบทวิจารณ์ผลิตภัณฑ์จะแสดงอยู่บน PDPs ปุ่ม **เขียนบทวิจารณ์** ช่วยให้ลูกค้าส่งการให้คะแนนและบทวิจารณ์สำหรับผลิตภัณฑ์ คุณลักษณะ PDP เหล่านี้จะถูกควบคุมโดยโมดูลการจัดอันดับและบทวิจารณ์

## <a name="ratings-and-reviews-modules-on-pdps"></a>โมดูลการให้คะแนนและบทวิจารณ์บน PDP 

สามโมดูลจะแสดงนสรุปการให้คะแนนและบทวิจารณ์บน PDP:
- โมดูลการเขียนบทวิจารณ์
- โมดูลรายการบทวิจารณ์ผลิตภัณฑ์
- โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนน
 
ภาพประกอบต่อไปนี้แสดงให้เห็นว่าโมดูลการให้คะแนนและบทวิจารณ์มีลักษณะอย่างไรบน PDP

![โมดูลการให้คะแนนและรีวิวบน PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> สำหรับข้อมูลเกี่ยวกับวิธีการทำเท็มเพลตและเค้าโครง PDP ให้เหมาะสม เพื่อให้คุณสามารถใช้การตั้งค่าสำหรับโมดูลการให้คะแนนและบทวิจารณ์ร่วมกันระหว่างหลาย PDP บนไซต์อีคอมเมิร์ซของคุณ โปรดดูที่ [ภาพรวมเท็มเพลตและเค้าโครง](templates-layouts-overview.md)

ภาพประกอบต่อไปนี้แสดงว่ากล่องโต้ตอบ **เพิ่มโมดูล** แสดงโมดูลการให้คะแนนและบทวิจารณ์อย่างไรใน Dynamics 365 Commerce
![กล่องโต้ตอบเพิ่มโมดูล](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>โมดูลการเขียนบทวิจารณ์

โมดูลการเขียนบทวิจารณ์จะมีปุ่ม **เขียนบทวิจารณ์** ที่ช่วยให้ผู้ใช้ลงชื่อเข้าใช้ กำหนดการให้คะแนน และเขียนบทวิจารณ์ของผลิตภัณฑ์ โมดูลนี้ยังช่วยให้ผู้ใช้แก้ไขการให้คะแนนหรือบทวิจารณ์ที่พวกเขาได้ส่งก่อนหน้านี้ได้ โดยทั่วไปแล้ว โมดูลจะปรากฏขึ้นด้านบนของโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนและโมดูลรายการบทวิจารณ์ผลิตภัณฑ์บน PDP
ภาพประกอบต่อไปนี้แสดงกล่องตอบโต้ **เขียนบทวิจารณ์** ที่ปรากฏขึ้นเมื่อลูกค้าเลือก **เขียนบทวิจารณ์** ลูกค้าสามารถใช้กล่องโต้ตอบนี้เพื่อส่งการให้คะแนนและบทวิจารณ์ได้

![กล่องโต้ตอบเขียนรีวิว](media/rnr-eCommerce-write-review-module.png)

ตารางต่อไปนี้แสดงคุณสมบัติของโมดูลการเขียนบทวิจารณ์ที่จำเป็นต้องตั้งค่าในเครื่องมือการสร้าง

| ชื่อคุณสมบัติ | มูลค่า        | คำอธิบายคุณสมบัติ                 |
|---------------|--------------|--------------------------------------|
| ชื่อ          | การเขียนบทวิจารณ์ | ชื่อของโมดูลการเขียนบทวิจารณ์ |

### <a name="ratings-histogram-module"></a>โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนน

โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนแสดงกราฟแสดงค่าสถิติความถี่ของการให้คะแนน โดยทั่วไปแล้ว โมดูลนี้จะปรากฏขึ้นระหว่างโมดูลการเขียนบทวิจารณ์และโมดูลรายการบทวิจารณ์ผลิตภัณฑ์บน PDP
โมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนไม่ต้องมีการตั้งค่า คุณเพียงแค่ต้องเพิ่มโมดูลในเท็มเพลต ภาพประกอบต่อไปนี้แสดงให้เห็นว่าเท็มเพลต PDP ใน Dynamics 365 Commerce จะมีลักษณะอย่างไรโมดูลต่าง ๆ การให้คะแนนและบทวิจารณ์มีการตั้งค่าสำหรับแสดงบน PDP
![เท็มเพลต PDP เมื่อมีการตั้งค่าคอนฟิกการให้คะแนนและรีวิวสำหรับการแสดงผลบน PDP](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>โมดูลรายการบทวิจารณ์ผลิตภัณฑ์

โมดูลรายการบทวิจารณ์ผลิตภัณฑ์แสดงรายการของบทวิจารณ์ผลิตภัณฑ์พร้อมด้วยตัวเลือกการเรียงลำดับ การกรองข้อมูล และการแบ่งหน้า โดยทั่วไปแล้ว โมดูลนี้จะปรากฏขึ้นหลังจากโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนบน PDP
ตารางต่อไปนี้แสดงคุณสมบัติของโมดูลรายการบทวิจารณ์ผลิตภัณฑ์ที่จำเป็นต้องตั้งค่าในเครื่องมือการสร้าง

| ชื่อคุณสมบัติ              | มูลค่า | คำอธิบายคุณสมบัติ |
|----------------------------|-------| ---------------------|
| บทวิจารณ์ที่แสดงในแต่ละหน้า | 10    | จำนวนบทวิจารณ์ที่ควรจะแสดงออกมาในแต่ละครั้งบน PDP ปุ่ม **ถัดไป** และ **ก่อนหน้า** จะมีอยู่ เพื่อให้ผู้ใช้สามารถย้ายไปยังหน้าต่าง ๆ ของบทวิจารณ์ |

#### <a name="ratings-histogram--summary-view"></a>กราฟแสดงค่าสถิติความถี่ของการให้คะแนน - มุมมองสรุป

โมดูลรายการบทวิจารณ์ผลิตภัณฑ์มีช่องที่คุณสามารถเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนได้ ภาพประกอบต่อไปนี้แสดงว่าคุณสามารถเพิ่มโมดูลกราฟแสดงค่าสถิติความถี่ของการให้คะแนนในโมดูลรายการบทวิจารณ์ผลิตภัณฑ์ใน Dynamics 365 Commerce ได้อย่างไร

![การเพิ่มโมดูลฮิสโตแกรมการให้คะแนนในโมดูลรายการบทวิจารณ์ผลิตภัณฑ์](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของไลบรารีโมดูล](starter-kit-overview.md)

[โมดูลคอนเทนเนอร์](add-container-module.md)

[โมดูลรถเข็น](add-cart-module.md)

[โมดูลเช็คเอาท์](add-checkout-module.md)

[โมดูลการยืนยันใบสั่ง](order-confirmation-module.md)

[โมดูหัวข้อ](author-header-module.md)

[โมดูลของส่วนท้าย](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
