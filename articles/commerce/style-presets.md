---
title: การทำงานกับค่าลักษณะที่กำหนดไว้แล้ว
description: บทความนี้จะอธิบายวิธีการทำงานกับรูปแบบที่กำหนดไว้ล่วงหน้าของไซต์ในตัวสร้างไซต์ Microsoft Dynamics 365 Commerce
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ea22c4c50a25c18d25980b8d2ce9bcf8cd315e87
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267524"
---
# <a name="work-with-style-presets"></a>การทำงานกับค่าลักษณะที่กำหนดไว้แล้ว

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายวิธีการทำงานกับรูปแบบที่กำหนดไว้ล่วงหน้าของไซต์ในตัวสร้างไซต์ Microsoft Dynamics 365 Commerce

รูปแบบที่กำหนดไว้ล่วงหน้าเป็นชุดที่จัดเก็บไว้ของค่าลักษณะที่สามารถสร้างได้ทั้งหมดในชุดรูปแบบของไซต์ คุณสามารถใช้เพื่อเปลี่ยนลักษณะของไซต์จากตัวร้างไซต์ได้ทันที รูปแบบที่กำหนดไว้ล่วงหน้าอนุญาตให้ผู้สร้างตัวสร้างไซต์ Commerce เปลี่ยนแปลงอย่างรวดเร็ว แสดงตัวอย่าง และเปิดใช้งานชุดของค่าลักษณะในไซต์ของตน โดยไม่ต้องใช้ Cascading Style Sheets (CSS) หรือปรับใช้ชุดรูปแบบ ลักษณะแบบอักษร ลักษณะปุ่ม และสีของไซต์ คือตัวอย่างโดยทั่วไปของลักษณะตัวแปรที่สามารถจัดการได้ผ่านรูปแบบที่กำหนดไว้ล่วงหน้า

ชุดของลักษณะตัวแปรที่มีอยู่ในไซต์จะถูกกำหนดโดยชุดรูปแบบและไลบรารีโมดูลที่ถูกปรับใช้กับผู้เช่าของไซต์ ชุดพัฒนาซอฟต์แวร์ออนไลน์ (SDK) ของ Dynamics 365 Commerce อนุญาตให้นักพัฒนาใช้งานตัวแปรลักษณะที่สามารถสร้างได้มากเท่าที่ต้องการ (หรือบางรายการ) ตามที่พวกเขาต้องการสำหรับชุดรูปแบบที่กำหนด โดยการเปิดใช้งานตัวแปรลักษณะมากขึ้น นักพัฒนาชุดรูปแบบสามารถนำตัวเลือกสุดท้ายเกี่ยวกับลักษณะของไซต์ไปไว้ในมือของผู้เขียนตัวสร้างไซต์ ดังนั้น ผู้ที่ไม่ใช่นักพัฒนาจะสามารถอัพเดตและแสดงตัวอย่างลักษณะไซต์ได้โดยใช้ชุดเครื่องมือ นอกจากนี้ ความสามารถยังเป็นประโยชน์สำหรับสถานการณ์จำลองใดๆ ที่การเปลี่ยนแปลงโดยตรงไปยังชุดรูปแบบหรือ CSS จะทำให้เกิดค่าโสหุ้ยที่ไม่จำเป็น

ชุดรูปแบบที่มีการเปิดใช้งานตัวแปรลักษณะที่สามารถสร้างได้ ต้องการรูปแบบที่กำหนดไว้ล่วงหน้าเริ่มต้น หรือพวกเขาสามารถรวมตัวเลือกที่กำหนดไว้ล่วงหน้าเพิ่มเติมได้โดยเป็นส่วนหนึ่งของแพคเกจชุดรูปแบบที่ปรับใช้ ตัวอย่างเช่น คุณสามารถปรับใช้ชุดรูปแบบซึ่งมีรูปแบบที่กำหนดไว้ล่วงหน้า "modern light" เริ่มต้น อีกทางหนึ่งคือ อาจรวมถึงตัวเลือกรูปแบบที่กำหนดไว้ล่วงหน้าเพิ่มเติม นอกเหนือจากรูปแบบที่กำหนดไว้ล่วงหน้าเริ่มต้น เช่น "modern dark" "vintage light" หรือ "vintage dark" ชุดรูปแบบที่กำหนดไว้ล่วงหน้าภายในถูกสร้างขึ้นโดยนักพัฒนาและสามารถใช้เป็นจุดเริ่มต้นสำหรับการออกแบบไซต์ใหม่

ในตัวสร้างไซต์ ผู้สร้างสามารถเลือกจากค่าที่กำหนดไว้ล่วงหน้าภายในของชุดรูปแบบ หรือพวกเขาสามารถสร้างค่าที่กำหนดไว้ล่วงหน้าและการเลือกกำหนดของพวกเขาเองได้โดยใช้ตัวแปรลักษณะที่เปิดใช้งาน สามารถแสดงตัวอย่างรูปแบบที่กำหนดไว้ล่วงหน้าในตัวสร้างไซต์ ก่อนที่จะเรียกใช้บนไซต์ที่เริ่มใช้งานจริง หลังจากที่มีการตรวจทานการเปลี่ยนแปลงลักษณะของผู้สร้าง จะมีการตั้งค่ารูปแบบที่กำหนดไว้ล่วงหน้าเป็น "ใช้งานอยู่" สำหรับไซต์ที่เริ่มใช้งานจริง

## <a name="preview-a-style-preset"></a>แสดงตัวอย่างรูปแบบที่กำหนดไว้ล่วงหน้า

เมื่อต้องการแสดงตัวอย่างรูปแบบที่กำหนดไว้ล่วงหน้าบนไซต์ของคุณในตัวสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้

1. ในบานหน้าต่างนำทางด้านซ้ายสำหรับไซต์ของคุณ ให้ไปที่ **การตั้งค่าไซต์ \> ออกแบบ**
1. บนแท็บ **รูปแบบที่กำหนดไว้ล่วงหน้า** ที่ด้านบนของตัวแก้ไขการออกแบบ ในรายการ **ค่าที่กำหนดไว้ล่วงหน้าที่พร้อมใช้งาน** เลือกค่าที่กำหนดไว้ล่วงหน้า แล้วจากนั้น เลือก **ดู** เพื่อไปที่ตัวแก้ไขที่กำหนดไว้ล่วงหน้า

    ถ้าในขณะนี้ไม่มีค่าที่กำหนดไว้ล่วงหน้าในรายการ **ค่าที่กำหนดไว้ล่วงหน้าที่พร้อมใช้งาน** ดู [สร้างรูปแบบที่กำหนดไว้ล่วงหน้าแบบกำหนดเอง](#create-a-custom-style-preset) สำหรับข้อมูลเกี่ยวกับวิธีการสร้างรูปแบบที่กำหนดไว้ล่วงหน้าแบบกำหนดเอง

    > [!NOTE]
    > ค่าที่กำหนดไว้ล่วงหน้าที่รวมอยู่ในชุดรูปแบบจะแสดงด้วยป้ายชื่อ **ภายใน** รูปแบบที่กำหนดไว้ล่วงหน้าภายในเหล่านี้เป็นแบบอ่านอย่างเดียว เมื่อต้องการคัดลอกรูปแบบที่กำหนดไว้ล่วงหน้าภายในเป็นค่าที่กำหนดไว้ล่วงหน้าที่สามารถกำหนดเองได้ใหม่ ให้เลือกปุ่มจุดไข่ปลา (**...**) สำหรับค่าที่ตั้งไว้ล่วงหน้า แล้วจากนั้น เลือก **บันทึกเป็น**

1. บนแถบคำสั่ง ให้เลือก **แสดงตัวอย่าง**
1. เลือก URL จากไซต์ของคุณเพื่อแสดงตัวอย่างรูปแบบที่กำหนดไว้ล่วงหน้า แล้วจากนั้น เลือก **ตกลง**
1. เลือกตัวแปร URL ของช่องทางเฉพาะและตำแหน่งที่ตั้งเฉพาะเพื่อแสดงตัวอย่างโดยเลือกชื่อของตัวแปร มีการเปิดหน้าต่างเบราว์เซอร์ของการแสดงตัวอย่างใหม่ ซึ่งรูปแบบที่กำหนดไว้ล่วงหน้าที่เลือกจะถูกนำไปใช้กับหน้าที่ระบุ

> [!NOTE]
> URL การแสดงตัวอย่างถาวรและมีการพิสูจน์ตัวจริง ดังนั้น คุณสามารถคัดลอก วาง และส่งไปยังผู้ปฏิบัติงานที่ได้รับการพิสูจน์ตัวจริงรายอื่นๆ สำหรับการตรวจทาน ก่อนที่คุณจะตั้งค่าเป็น "ใช้งานอยู่" บนไซต์ที่เริ่มใช้งานจริงของคุณ นอกจากนี้ URL การแสดงตัวอย่างยังเป็นประโยชน์สำหรับการตรวจสอบลักษณะบนอุปกรณ์ต่างๆ ในเบราว์เซอร์ที่แตกต่างกัน และบนหน้าจอที่แตกต่างกัน

> [!TIP]
> ขณะที่คุณแก้ไขรูปแบบที่กำหนดไว้ล่วงหน้า คุณอาจพบว่ามีประโยชน์ที่จะออกจากหน้าต่างเบราว์เซอร์สำหรับการแสดงตัวอย่างสำหรับเปิดในหน้าต่างเบราเซอร์ที่แยกต่างหาก เพื่อให้คุณสามารถตรวจสอบความถูกต้องของการเปลี่ยนแปลงของคุณได้อย่างรวดเร็ว หลังจากที่คุณบันทึกการเปลี่ยนแปลงไปยังรูปแบบที่กำหนดไว้ล่วงหน้า ให้รีเฟรชหน้าต่างเบราเซอร์การแสดงตัวอย่างที่เปิดเพื่อตรวจสอบประสบการณ์การใช้งานของผู้ใช้

## <a name="create-a-custom-style-preset"></a>สร้างรูปแบบที่กำหนดไว้ล่วงหน้าแบบกำหนดเอง

เมื่อต้องการสร้างรูปแบบที่กำหนดไว้ล่วงหน้าแบบกำหนดเองในตัวสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้

1. ในบานหน้าต่างนำทางด้านซ้ายสำหรับไซต์ของคุณ ให้ไปที่ **การตั้งค่าไซต์ \> ออกแบบ**
1. บนแท็บ **รูปแบบที่กำหนดไว้ล่วงหน้า** ที่ด้านบนของตัวแก้ไขการออกแบบ บนแถบคำสั่ง ให้เลือก **ค่าที่กำหนดไว้ล่วงหน้าใหม่**
1. ป้อนชื่อและคำอธิบายสำหรับค่าที่กำหนดไว้ล่วงหน้าใหม่ และจากนั้น เลือก **บันทึก** ค่าที่กำหนดไว้ล่วงหน้าที่สามารถเลือกกำหนดได้ใหม่ถูกสร้างขึ้นซึ่งใช้ค่าเริ่มต้นของชุดรูปแบบเป็นจุดเริ่มต้น

> [!NOTE]
> นอกจากนี้ คุณยังสามารถสร้างรูปแบบที่กำหนดไว้ล่วงหน้าแบบกำหนดเองใหม่จากรูปแบบที่กำหนดไว้ล่วงหน้าใดๆ ที่มีอยู่ โดยเลือกปุ่มจุดไข่ปลา (**...**) สำหรับค่าที่กำหนดไว้ล่วงหน้านั้น แล้วจากนั้น เลือก **บันทึกเป็น** อีกทางหนึ่งคือ เลือก **บันทึกเป็น** บนแถบคำสั่งในตัวแก้ไขที่กำหนดไว้ล่วงหน้า

## <a name="modify-global-and-module-type-style-values"></a>ปรับเปลี่ยนค่าลักษณะของชนิดสากลและโมดูล

ตัวแปรลักษณะของชุดรูปแบบบางรายการมีการใช้ร่วมกันระหว่างโมดูลหลายชนิด ตัวแปรลักษณะเหล่านี้เรียกว่า ตัวแปรลักษณะ *สากล* ตัวอย่างประกอบด้วยสีไซต์หลัก ลักษณะแบบอักษรเริ่มต้น และลักษณะปุ่มต่างๆ ด้วยการตั้งค่าตัวแปรสากล คุณอาจเปลี่ยนลักษณะที่ปรากฏในโมดูลต่างๆ ที่แตกต่างกันหลายชนิด

ค่าลักษณะบางค่าอาจจะมีลักษณะเฉพาะสำหรับชนิดโมดูล หรืออาจต้องแทนที่ค่าเริ่มต้นสากล ถ้าชุดรูปแบบของไซต์มีการใช้ตัวแปรลักษณะชนิดโมดูล ผู้สร้างตัวสร้างไซต์สามารถเลือกกำหนดรูปแบบของชนิดโมดูลได้โดยอิสระจากการตั้งค่าสากล ตัวแปรชนิดโมดูลสามารถเพิ่มหรือแทนที่ตัวแปรลักษณะสากลในชุดรูปแบบได้

> [!NOTE]
> ลำดับชั้นของค่าลักษณะในไซต์ทำหน้าที่ในลักษณะต่อไปนี้ ค่าของลักษณะที่ปรากฏห่างออกไปจากทางด้านขวาจะแทนที่ค่าของลักษณะทางด้านซ้าย
>
> ค่าเริ่มต้นของชุดรูปแบบ \< ค่ารูปแบบสากล \< ค่ารูปแบบของชนิดโมดูล \< CSS แทนที่

เมื่อต้องการเปลี่ยนค่าของชนิดสากลหรือโมดูลที่ตั้งค่าไว้ล่วงหน้าของลักษณะในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้

1. ในบานหน้าต่างนำทางด้านซ้ายสำหรับไซต์ของคุณ ให้ไปที่ **การตั้งค่าไซต์ \> ออกแบบ**
1. บนแท็บ **รูปแบบที่กำหนดไว้ล่วงหน้า** ที่ด้านบนของตัวแก้ไขการออกแบบ ให้เลือก **มุมมอง** สำหรับรูปแบบที่กำหนดไว้ล่วงหน้าใดๆ เพื่อให้ไปที่ตัวแก้ไขที่กำหนดไว้ล่วงหน้า
1. เลือก **การแสดงตัวอย่าง** และจากนั้น ปฏิบัติตามขั้นตอนการเลือก URL เพื่อเปิดการแสดงตัวอย่างหน้าต่างแบบเต็มเบราว์เซอร์สำหรับค่าที่ตั้งไว้ล่วงหน้าของคุณ เปิดหน้าต่างเบราเซอร์การแสดงตัวอย่างนี้ทิ้งไว้
1. ในตัวแก้ไขที่กำหนดไว้ล่วงหน้า ให้เลือก **แก้ไข** ที่ด้านขวาบน
1. ใช้ตัวควบคุมลักษณะตัวแปรในตัวแก้ไขเพื่อเปลี่ยนค่าลักษณะส่วนกลางบางอย่าง
1. ที่ด้านบนของตัวแก้ไข บนแท็บ **โมดูล** ทางด้านขวาของแท็บ **ส่วนกลาง** ให้เลือกชนิดโมดูลที่ต้องถูกกำหนดลักษณะ
1. ใช้ตัวควบคุมลักษณะเพื่อเปลี่ยนค่าบางค่าสำหรับชนิดโมดูล
1. เมื่อคุณพร้อมที่จะแสดงตัวอย่างการเปลี่ยนแปลงของคุณ ให้เลือก **บันทึก** บนแถบคำสั่ง
1. กลับไปที่หน้าต่างเบราว์เซอร์ของการแสดงตัวอย่างเปิด และรีเฟรช การแสดงตัวอย่างหน้าต่างเบราว์เซอร์แบบเต็ม มีประโยชน์สำหรับการตรวจสอบการเปลี่ยนแปลงรูปแบบที่จุดสั่งหยุดมุมมองต่างๆ ในเบราว์เซอร์ที่แตกต่างกัน และบนแพลตฟอร์มอุปกรณ์ต่างๆ
1. เมื่อการเปลี่ยนแปลงทั้งหมดเสร็จสมบูรณ์แล้วและตรวจสอบความถูกต้องแล้ว ให้เลือก **เสร็จสิ้นการแก้ไข** ในมุมขวาบนของตัวแก้ไข

> [!NOTE]
> ถ้าคุณกำลังแก้ไขลักษณะที่กำหนดไว้ล่วงหน้าซึ่งเปิดใช้งานอยู่บนไซต์ของคุณ คุณจะเห็นป้ายชื่อ **ใช้งานอยู่** สีน้ำเงินในตัวแก้ไข ป้ายชื่อนี้จะบ่งชี้ว่าการตั้งค่าล่วงหน้าเริ่มใช้งานจริงบนเว็บไซต์ของคุณในขณะนี้ ถ้าคุณเปลี่ยนการตั้งค่าล่วงหน้าที่ใช้งานอยู่ ให้เลือก **เผยแพร่** เพื่อผลักดันการเปลี่ยนแปลงเหล่านั้นไปยังไซต์ที่เริ่มใช้งานจริงของคุณ

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>ทำให้รูปแบบที่กำหนดไว้ล่วงหน้าถูกเปิดใช้งานเว็บไซต์ที่เริ่มใช้งานจริงของคุณ

เมื่อต้องการตั้งค่ารูปแบบที่กำหนดไว้ล่วงหน้าเป็นรูปแบบที่กำหนดไว้ล่วงหน้าใหม่ที่ใช้งานอยู่บนไซต์ของคุณ ให้ทำตามขั้นตอนเหล่านี้

- เลือก **ปุ่มกำหนดเป็นใช้งานอยู่** ในหนึ่งในตำแหน่งเหล่านี้:

    - แถบคำสั่งในตัวแก้ไขรูปแบบที่กำหนดไว้ล่วงหน้า
    - เมนูจุดไข่ปลา (**...**) สำหรับค่าที่กำหนดไว้ล่วงหน้าใดๆ ที่พร้อมใช้งานในมุมมองหลักบนแท็บ **รูปแบบที่กำหนดไว้ล่วงหน้า** ที่ **การตั้งค่าไซต์ \> ออกแบบ**

ค่าลักษณะของค่าที่กำหนดไว้ล่วงหน้าจะทำงานในเว็บไซต์ที่เชื่อมต่อกับสาธารณะของคุณโดยตรง

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[เพิ่มโลโก้](add-logo.md)

[เลือกชุดรูปแบบของไซต์](select-site-theme.md)

[ทำงานกับไฟล์การแก้ไข CSS](css-override-files.md)

[เพิ่มไอคอนประจำไซต์](add-favicon.md)

[เพิ่มข้อความสงวนลิขสิทธิ์](add-copyright-notice.md)

[เพิ่มภาษาลงในไซต์ของคุณ](add-languages-to-site.md)

[เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
