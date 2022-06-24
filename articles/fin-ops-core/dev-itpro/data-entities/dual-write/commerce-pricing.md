---
title: ใช้กลไกการกำหนดราคา Dynamics 365 Commerce กับ Dynamics 365 Sales
description: บทความนี้จะอธิบายวิธีการใช้กลไกการกำหนดราคา Microsoft Dynamics 365 Commerce เพื่อสร้างใบเสนอราคาขายใน Dynamics 365 Sales
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 11a164ec15c8b7a69172a153b961011a8b324712
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881407"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>ใช้กลไกการกำหนดราคา Dynamics 365 Commerce กับ Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

บทความนี้จะอธิบายวิธีการใช้กลไกการกำหนดราคา Microsoft Dynamics 365 Commerce เพื่อสร้างใบเสนอราคาขายใน Dynamics 365 Sales

กลไกการกำหนดราคา Dynamics 365 Commerce สนับสนุนสถานการณ์จำลองการกำหนดราคาสำหรับธุรกิจต่อผู้บริโภค (B2C) ส่วนมาก เช่น การกำหนดราคาในระดับร้านค้า การกำหนดราคาที่ยึดตามความภักดีและที่ยึดตามรายได้ ส่วนลดในการซื้อคละกัน ส่วนลดปริมาณ และส่วนลดจำกัด กลไกการกำหนดราคาจะใช้กฎที่ซับซ้อนเพื่อกำหนดราคาที่ดีที่สุดสำหรับใบเสนอราคาหรือใบสั่งที่กำหนด

เมื่อคุณใช้ [การรวมแบบสองทิศทาง](./dual-write-overview.md) คุณมีสามตัวเลือกสำหรับความต้องการในการกำหนดราคาของคุณ คุณสามารถใช้การกำหนดราคาแบบคงที่ที่มาจากรายการราคาใน Dynamics 365 Sales กลไกการกำหนดราคาใน Dynamics 365 Supply Chain Management หรือกลไกการกำหนดราคาใน Dynamics 365 Commerce ในระหว่างตัวเลือกเหล่านี้ กลไกการกำหนดราคา Commerce เหมาะกับสถานการณ์ B2C ที่สุด

## <a name="use-the-commerce-pricing-engine-in-sales"></a>ใช้กลไกการกำหนดราคา Commerce ใน Sales

> [!NOTE]
> ในปัจจุบัน สามารถใช้กลไกการกำหนดราคา Commerce สำหรับการสร้างใบเสนอราคาใน Sales เท่านั้น การรวมใบสั่งขายที่มีกลไกจัดการกำหนดราคา Commerce ยังไม่พร้อมใช้งาน

เมื่อผู้ใช้เริ่มต้นใบเสนอราคาใน Sales กรอบงานการรวมแบบสองทิศทางจะคัดลอกรายละเอียดใบเสนอราคาไปยัง Commerce การเปลี่ยนแปลงใดๆ ไปยังบรรทัดใบเสนอราคาที่มีอยู่ หรือบรรทัดใบเสนอราคาที่เพิ่มใหม่ใน Sales จะถูกคัดลอกไปยัง Commerce เมื่อผู้ใช้ต้องการใช้กลไกการกำหนดราคา Commerce เพื่อกำหนดราคาใบเสนอราคา พวกเขาสามารถเลือก **การอ้างอิงราคา** เพื่ออัปเดตราคาของใบเสนอราคา โดยใช้กลไกการกำหนดราคา commerce จากนั้น ราคาจะถูกอัปเดตโดยอัตโนมัติในทั้ง Sales และ Commerce

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

- ก่อนที่คุณจะสามารถใช้กลไกการกำหนดราคา Commerce ใน Sales ได้ คุณต้องปฏิบัติตามขั้นตอนใน [ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสดในการรวมแบบสองทิศทาง](./dual-write-prospect-to-cash.md)
- คุณต้องปิดการประเมินข้อตกลงทางการค้าสำหรับการป้อนข้อมูลด้วยตนเองโดยปฏิบัติตามขั้นตอนต่อไปนี้:

    1. ในสภาพแวดล้อม Commerce ของคุณ ไปที่ **บัญชีลูกหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีลูกหนี้**
    1. บนแท็บ **ราคา** บน FastTab **การประเมินข้อตกลงทางการค้า** ให้ยกเลิกการเลือกกล่องกาเครื่องหมาย **ป้อนข้อมูลด้วยตนเอง**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสดในการรวมแบบสองทิศทาง](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]