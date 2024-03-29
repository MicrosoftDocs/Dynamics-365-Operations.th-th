---
title: การจัดส่งบางส่วนของการบรรทุกเพื่อขนส่ง
description: บทความนี้อธิบายวิธีการที่คุณสามารถจัดส่งโหลดได้บางส่วน และเลื่อนการวางแผนกำลังการผลิตสำหรับโหลด
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 09e35b8ee39b3635938f46e174e6ba98db7fa627
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907042"
---
# <a name="partial-shipment-of-a-transport-load"></a>การจัดส่งบางส่วนของการบรรทุกเพื่อขนส่ง

[!include[banner](../includes/banner.md)]

ด้วยการตั้งค่าการจัดส่งบางส่วนของโหลด คุณสามารถจัดการกับโหลดที่ซึ่งไม่สามารถกำหนดกำลังการผลิตได้ จนกว่าจะมีการเพิ่มรายการการขายไปยังโหลด จากนั้น กระบวนการสามารถได้รับการดำเนินการขั้นสุดท้าย เมื่อทราบจำนวนแท่นวางสินค้าที่แน่นอน ดังนั้น คุณไม่ต้องตัดสินใจว่า แท่นวางสินค้าใดที่จะถูกกำหนดให้กับการขนส่งใด จนกว่าถึงช่วงเวลาที่การขนส่งกำลังโหลดสินค้าคงคลังที่แบ่งระยะตามจริง

คุณลักษณะนี้ให้ทางเลือกในการบังคับโครงสร้างที่แข็งมากขึ้น ที่ซึ่งคุณต้องกำหนดว่าแท่นวางสินค้าใดที่จะถูกกำหนดให้กับการขนส่งใด ก่อนที่จะสร้างงานการเบิกสินค้าหรืองานการโหลด ผู้ใช้สามารถตั้งค่าคอนฟิกโหลดแต่ละรายการแทนได้ สำหรับการยืนยันการจัดส่งบางส่วน จากนั้น กระบวนการโหลดของการขนส่งสำหรับโหลดเหล่านั้นอาจเกิดขึ้นได้ ดังนั้น แผนกการวางแผนการขนส่งสามารถวางแผนโหลดได้ โดยต้องไม่พิจารณาถึงกำลังการผลิตของการขนส่งแต่ละรายการ

ในขณะที่กำลังโหลด ผู้ปฏิบัติงานสามารถกำหนดโหลดการขนส่งใหม่ที่มีการโหลดแท่นวางสินค้า อีกทางหนึ่งคือ สามารถระบุโหลดการขนส่งที่มีอยู่ได้ ข้อมูลนี้สามารถบันทึกได้ผ่านอุปกรณ์เคลื่อนที่ ดังนั้น ผู้ปฏิบัติงานคลังสินค้าหลายรายสามารถโหลดสินค้าคงคลังจากโหลดเดียวกัน หรือโหลดที่แตกต่างกันไปยังรถบรรทุกเดียวกันได้ จากนั้น สามารถจัดส่งโหลดทั้งหมดหรือบางส่วนได้

> [!NOTE] 
> เพื่อที่จะโหลดสินค้าคงคลังจากโหลดไปยังโหลดการขนส่งเฉพาะ และจัดส่งสินค้าบางส่วน งานต้องถูกสร้างขึ้น โดยใช้คลาสการโหลดในเท็มเพลตงาน งานของการเบิกสินค้าแบบธรรมดาของชนิด **การเบิกสินค้า** ไม่สามารถโหลดไปยังโหลดการขนส่งได้ เช่น รถบรรทุก

## <a name="set-up-transport-loads-for-partial-shipment"></a>ตั้งค่าโหลดการขนส่งสำหรับการจัดส่งเป็นบางส่วน

การตั้งค่าสำหรับการจัดส่งบางส่วนในโหลด ประกอบด้วยกระบวนงานสองรายการต่อไปนี้

### <a name="set-the-loading-strategy"></a>ตั้งค่ากลยุทธ์การโหลด

คุณต้องเปิดใช้งานการโหลดบางส่วน โดยการตั้งค่ากลยุทธ์การโหลด คุณสามารถตั้งค่ากลยุทธ์การโหลดได้ หลังจากที่คุณสร้างโหลด

1. เลือก **การบริหารคลังสินค้า** \> **โหลด** \> **โหลดทั้งหมด**
2. เลือกโหลด แล้วจากนั้นคลิก **ส่วนหัว**
3. ในฟิลด์ **กลยุทธ์การโหลด** เลือก **การจัดส่งโหลดบางส่วนที่ได้รับอนุญาต**

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>สร้างรายการเมนูสำหรับการโหลดที่โหลดการขนส่ง

คุณต้องสร้างรายการเมนูใหม่ที่เปิดใช้งานโหลดการขนส่งที่จะถูกโหลด โหลดการขนส่งช่วยให้คุณสามารถจัดกลุ่มรายการงานได้จากโหลดหนึ่งหรือหลายการ จากนั้น ทุกสิ่งที่เพิ่มเข้าไปยังโหลดการขนส่งสามารถจัดส่งได้ โดยใช้เครื่องสแกนเคลื่อนที่

1. เลือก **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **อุปกรณ์เคลื่อนที่** \> **รายการเมนูอุปกรณ์เคลื่อนที่**
2. เลือก **สร้าง** และจากนั้นในฟิลด์ **โหมด** เลือก **งาน**
3. ตั้งค่าตัวเลือก **ใช้งานที่มีอยู่** เป็น **ใช่**
4. บนแท็บ **ทั่วไป** ในฟิลด์ **สั่งการโดย** เลือก **การโหลดการขนส่ง**
5. ในการยืนยันการจัดส่งบนสแกนเนอร์เคลื่อนที่ ในฟิลด์ **ชนิดการยืนยันการจัดส่งที่ได้รับอนุญาต** เลือก **โหลดการขนส่ง**

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>ยืนยันการจัดส่งของโหลดการขนส่งจากไคลเอนต์

การตั้งค่านี้ช่วยให้สามารถคุณยืนยันโหลดการขนส่ง ที่มีการโหลดเต็มจำนวนหรือโหลดที่มีการโหลดบางส่วนที่จะจัดส่ง

1. เลือก **การบริหารคลังสินค้า** \> **โหลด** \> **โหลดการขนส่ง**
2. บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดส่งและรับ** ในกลุ่ม **ยืนยัน** เลือก **การขนส่ง**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]