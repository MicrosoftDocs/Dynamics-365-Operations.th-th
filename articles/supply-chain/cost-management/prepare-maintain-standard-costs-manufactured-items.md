---
title: การเตรียมการรักษาต้นทุนมาตรฐานสำหรับสินค้าที่ผลิต
description: หัวข้อนี้อธิบายขั้นตอนสำหรับการเตรียมการในการรักษาต้นทุนสำหรับสินค้าที่ผลิต
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b35e424c582c173e3fa1f4d0a335106e413b6660
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967419"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>การเตรียมการรักษาต้นทุนมาตรฐานสำหรับสินค้าที่ผลิต

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายขั้นตอนสำหรับการเตรียมการในการรักษาต้นทุนสำหรับสินค้าที่ผลิต ขั้นตอนสำหรับสินค้าที่ผลิตแตกต่างกันเล็กน้อยจากขั้นตอนสำหรับสินค้าที่ซื้อ

นโยบายที่ถูกกำหนดให้กับสินค้าที่ผลิตสามารถส่งผลต่อการคำนวณต้นทุนสำหรับสินค้าหลักที่ผลิตได้ ในการเตรียมการเพื่อรักษาต้นทุนสำหรับสินค้าที่ผลิต ให้ดำเนินการตามขั้นตอนเหล่านี้

1. กำหนดกลุ่มแบบจำลองสินค้าให้กับสินค้าที่ผลิต 

   กลุ่มแบบจำลองสินค้าระบุว่าจะมีการใช้ต้นทุนมาตรฐาน

2. กำหนดกลุ่มสินค้าให้กับสินค้าที่ผลิต 

   กลุ่มสินค้ามีบัญชีแยกประเภทที่ใช้งานกับสินค้าที่ผลิต  บัญชีแยกประเภทสำหรับสินค้าที่ผลิตที่มีแบบจำลองสินค้าคงคลังของต้นทุนมาตรฐาน รวมเอาผลต่างการผลิตต่างๆ ผลต่างการเปลี่ยนแปลงต้นทุน และการประเมินค่าต้นทุนสินค้าคงคลังใหม่

3. กำหนดหน่วยวัดสินค้าคงคลังให้กับสินค้า 

   ต้นทุนของสินค้าจะแสดงอยู่ในหน่วยวัดสินค้าคงคลังของสินค้าเสมอ

4. ไม่ต้องกำหนดกลุ่มต้นทุนให้กับสินค้าที่ผลิต นอกเสียจากว่าจะถือว่าสินค้าเป็นสินค้าที่ซื้อ

5. กำหนดกลุ่มการคำนวณสูตรการผลิต BOM ให้กับสินค้าที่ผลิต 

   กลุ่มการคำนวณ BOM ของสินค้ากำหนดเงื่อนไขการเตือนที่เกี่ยวข้อง ในวิธีนั้น เมื่อทำการคำนวณ BOM เรียบร้อยแล้ว สามารถสร้างข้อความเตือนเกี่ยวกับแหล่งที่มาที่เป็นไปได้ของข้อผิดพลาดในการคำนวณ ตัวอย่างเช่น ข้อความเตือนสามารถแจ้งให้ทราบได้ เมื่อไม่มี BOM หรือกระบวนการผลิตที่ใช้งานอยู่ กลุ่มการคำนวณ BOM มีนโยบายหยุดการกระจายที่ระบุเวลาที่ควรดำเนินการกับสินค้าที่ผลิตในฐานะสินค้าที่ซื้อ

6. ถ้าสินค้าที่ผลิตเมื่อมีต้นทุนคงที่ ให้มอบหมายปริมาณการสั่งมาตรฐาน 

   ปริมาณการสั่งมาตรฐานเป็นขนาดล็อตบัญชีสำหรับการตัดจำหน่ายต้นทุนคงที่ ตัวอย่างของต้นทุนคงที่ประกอบด้วย เวลาในการตั้งค่าในการดำเนินงานกระบวนการผลิตและปริมาณส่วนประกอบคงที่ใน BOM

7. กำหนด BOM สำหรับสินค้าที่ผลิต  

   คุณสามารถกำหนดเวอร์ชัน BOM หนึ่งหรือหลายเวอร์ชันให้กับสินค้าที่ผลิตได้  ตรวจสอบว่าเวอร์ชันที่คุณต้องการได้ถูกทำเครื่องหมายเป็น ผ่านการอนุมัติและใช้งานได้ และตรวจสอบว่ามีวันที่ที่มีผลบังคับใช้ที่คุณต้องการ เวอร์ชัน BOM สามารถเป็น ทั้งบริษัท หรือ เฉพาะไซต์

8. กำหนดสายงานการผลิตสำหรับสินค้าที่ผลิต  

   คุณสามารถกำหนดเวอร์ชันสายงานการผลิตหนึ่งหรือหลายเวอร์ชันให้กับสินค้าที่ผลิตได้  ตรวจสอบว่าเวอร์ชันที่คุณต้องการได้ถูกทำเครื่องหมายเป็น ผ่านการอนุมัติและใช้งานได้ และตรวจสอบว่ามีวันที่ที่มีผลบังคับใช้ที่คุณต้องการ เวอร์ชันกระบวนการผลิตต้องเป็นเฉพาะไซต์

ถ้าคุณต้องการใช้ข้อมูลสายงานการผลิตสำหรับวัตถุประสงค์เพื่อการคำนวณต้นทุน จะต้องมีขั้นตอนการเตรียมการเพิ่มเติม ตัวอย่างเช่น ประเภทต้นทุนที่ถูกกำหนดให้กับการดำเนินการสายงานการผลิตต้องถูกต้องและสมบูรณ์

<a name="related-topics"></a>หัวข้อที่เกี่ยวข้อง
--------

[การตัดจำหน่ายต้นทุนคงที่สำหรับสินค้าที่ผลิต](amortize-constant-costs-manufactured-item.md)

[ตั้งค่าผลิตภัณฑ์ที่สามารถถูกผลิตหรือจัดซื้อ](manufactured-items-treated-as-purchased-items.md)

