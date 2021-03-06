---
title: จัดการคุณลักษณะ
description: หัวข้อนี้อธิบายวิธีการที่ทำให้ผู้ดูแลระบบสามารถเปิดใช้งานคุณลักษณะการแสดงตัวอย่างได้ใน Microsoft Dynamics 365 Talent และจะแสดงรายการคุณลักษณะที่ถูกเปิดใช้งานสำหรับการแสดงตัวอย่างในขณะนี้
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462760"
---
# <a name="manage-features"></a>จัดการคุณลักษณะ

[!include [banner](includes/banner.md)]

เนื่องจากเป็นส่วนหนึ่งของการเปิดตัวความสามารถของการจัดการทุนมนุษย์ (HCM) สำหรับ Microsoft Dynamics 365 Human Resources เราต้องการให้ลูกค้าพบกับคุณลักษณะใหม่โดยเร็วที่สุด ผู้ดูและระบบสามารถดูและใช้งานคุณลักษณะการแสดงตัวอย่างในสภาพแวดล้อมดังกล่าวได้ คุณลักษณะเหล่านี้ใกล้จะพร้อมสำหรับความพร้อมใช้งานทั่วไป และได้ผ่านการทดสอบอย่างครอบคลุมแล้ว เรากำลังมองหาความคิดเห็นและการตรวจสอบความถูกต้องของลูกค้าในขั้นตอนสุดท้าย ก่อนที่เราจะนำคุณลักษณะเหล่านี้ออกไปใช้งานสำหรับความพร้อมใช้งานทั่วไป

หัวข้อนี้อธิบายวิธีการที่ทำให้คุณสามารถเปิดใช้งานคุณลักษณะแสดงตัวอย่าง และแสดงรายการคุณลักษณะที่พร้อมใช้งานสำหรับการแสดงตัวอย่างในขณะนี้ รายการนี้จะถูกอัพเดต เมื่อคุณลักษณะถูกนำไปใช้ในความพร้อมใช้งานทั่วไป และเมื่อมีการนำคุณลักษณะใหม่ออกใช้เพื่อแสดงตัวอย่าง ไม่มีการแจ้งเตือนให้ทราบ เมื่อมีการนำคุณลักษณะใหม่มาแสดงตัวอย่าง ผู้ใช้จะเริ่มต้นเห็นคุณลักษณะ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะใหม่ๆ ใน Talent ดู [มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent](./whats-new.md) และ [บันทึกย่อประจำรุ่นของ Dynamics 365 และ Power Platform](https://docs.microsoft.com/business-applications-release-notes)

## <a name="enable-or-disable-preview-features"></a>เปิดใช้งาน หรือปิดใช้งานคุณลักษณะการแสดงตัวอย่าง

เมื่อต้องการเข้าถึงคุณลักษณะการแสดงตัวอย่าง คุณต้องเปิดใช้งานในสภาพแวดล้อมของคุณก่อน การเปิดหรือปิดใช้งานคุณลักษณะการแสดงตัวอย่างเป็นแบบเฉพาะกับสภาพแวดล้อม

> [!IMPORTANT]
> เมื่อคุณเปิดการตั้งค่า **คุณลักษณะการแสดงตัวอย่าง** คุณเปิดใช้งานคุณลักษณะการแสดงตัวอย่างสำหรับผู้ใช้ทั้งหมดในองค์กรของคุณที่อยู่ในสภาพแวดล้อมนั้น เมื่อคุณปิดการตั้งค่า คุณจะปิดใช้งานคุณลักษณะการแสดงตัวอย่าง และทำให้ไม่สามารถเข้าถึงผู้ใช้ของคุณได้ คุณลักษณะการแสดงตัวอย่างมีการสนับสนุนที่จำกัดใน Talent อาจใช้ความเป็นส่วนตัวและมาตรการด้านความปลอดภัยน้อยลง และจะไม่ถูกรวมอยู่ในข้อตกลงระดับการบริการ Talent (SLA) คุณไม่ควรใช้คุณลักษณะการแสดงตัวอย่างในการประมวลผลข้อมูลส่วนบุคคล (นั่นคือ ข้อมูลใดๆ ที่สามารถระบุตัวคุณได้) หรือในการประมวลผลข้อมูลอื่นๆ ที่ขึ้นอยู่กับความต้องการปฏิบัติตามกฎหมาย หรือตามข้อบังคับ

### <a name="attract"></a>ดึงดูด

1. ลงชื่อเข้าใช้ Microsoft Dynamics 365 Talent: Attract
2. ในเมนู **ตั้งค่า** (สัญลักษณ์เกียร์) ในมุมบนด้านขวา เลือก **ศูนย์ผู้ดูแลระบบ**
3. บนแท็บ **การจัดการคุณลักษณะ** เลือกตัวเลือกถัดจาก **คุณลักษณะการแสดงตัวอย่าง** เพื่อให้กลายเป็นสีฟ้า และกล่าวว่า **เปิด**

    ![เปิดใช้งานคุณลักษณะการแสดงตัวอย่างใน Attract](./media/attract-enable-preview-features.png)

4. เลือกหรือยกเลิกการเลือกของคุณลักษณะการแสดงตัวอย่างแต่ละรายการ ถ้าคุณไม่ได้ทำอะไรเลย คุณสามารถเปิดใช้งานคุณลักษณะการแสดงตัวอย่างทั้งหมดที่มีอยู่ได้
5. รีเฟรชเบราเซอร์ของคุณเพื่อเริ่มต้นดูคุณลักษณะใหม่ ผู้ใช้ใดๆ ที่เข้าสู่ระบบอยู่แล้ว จะเห็นคุณลักษณะในครั้งถัดไปที่พวกเขาเข้าสู่ระบบ หรือพวกเขาสามารถรีเฟรชเบราเซอร์ของพวกเขาเพื่อดูคุณลักษณะโดยทันทีได้

> [!NOTE]
> คุณลักษณะการแสดงตัวอย่างบางรายการอาจต้องการการตั้งค่าคอนฟิกเพิ่มเติม ทำตามลิงค์ที่อยู่ถัดจากคุณลักษณะการแสดงตัวอย่างเพื่อทำให้การตั้งค่าเสร็จสมบูรณ์

## <a name="feedback"></a>ผลป้อนกลับ

เราต้องการได้ยินจากคุณเกี่ยวกับประสบการณ์ของคุณกับคุณลักษณะการแสดงตัวอย่างใดๆ เหล่านี้ เราขอสนับสนุนให้คุณลงรายการบัญชีคำติชมของคุณอย่างสม่ำเสมอบนไซต์ต่อไปนี้ เมื่อคุณใช้รายการเหล่านี้หรือคุณลักษณะอื่นใดๆ :

- [ชุมชน](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – ไซต์นี้เป็นทรัพยากรที่สำคัญที่ผู้ใช้สามารถอธิบายกรณีที่ใช้ ถามคำถาม และขอความช่วยเหลือของชุมชน
- แจ้งให้เราทราบเกี่ยวกับคุณลักษณะที่คุณต้องการดูในผลิตภัณฑ์ และแจ้งให้เราทราบเกี่ยวกับการเปลี่ยนแปลงใดๆ ที่คุณคิดว่าเราควรจะทำต่อคุณลักษณะที่มีอยู่ แนะนำแนวคิดเกี่ยวกับผลิตภัณฑ์ในไซต์ต่อไปนี้:

    - [แนวคิด Attract](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [แนวคิด Onboard](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

ต้องแน่ใจว่าคุณไม่ได้รวมข้อมูลส่วนบุคคล (ข้อมูลใดๆ ที่สามารถระบุตัวคุณได้) ในความคิดเห็นของคุณ หรือการส่งการตรวจทานผลิตภัณฑ์ ข้อมูลที่ถูกรวบรวมอาจถูกวิเคราะห์เพิ่มเติม และจะไม่ถูกใช้เพื่อตอบสนองคำขอภายใต้กฎหมายความเป็นส่วนตัวที่เกี่ยวข้องได้ ข้อมูลส่วนบุคคลที่ถูกเก็บแยกต่างหากภายใต้โปรแกรมเหล่านี้มีผลต่อ [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement)

> [!TIP]
> คั่นหัวข้อนี้ และลตรวจสอบย้อนหลังบ่อยๆ เพื่อคอยติดตามสถานการณ์ปัจจุบันเกี่ยวกับคุณลักษณะการทำงานใหม่ เมื่อเรานำออกใช้

## <a name="see-also"></a>ดูเพิ่มเติมที่

- [ลอง หรือซื้อแอป Talent](https://dynamics.microsoft.com/talent/overview/)
- [มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent](./whats-new.md)
- [แผนการรีลีส](https://docs.microsoft.com/business-applications-release-notes/index)
- [รับการสนับสนุนสำหรับ Microsoft Dynamics 365 Talent](./talent-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]