---
title: เชื่อมต่อการทดลองและแก้ไขรูปแบบการทดลอง
description: บทความนี้อธิบายวิธีการเชื่อมต่อการทดลองในบริการของบุคคลที่สามกับ Dynamics 365 Commerce และวิธีการแก้ไขรูปแบบการทดลอง
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942833"
---
# <a name="connect-an-experiment-and-edit-variations"></a>เชื่อมต่อการทดลองและแก้ไขรูปแบบการทดลอง

บทความนี้อธิบายวิธีการเชื่อมต่อการทดลองของคุณใน Commerce และทำการเปลี่ยนแปลงรูปแบบของคุณ เพื่อให้สอดคล้องกับสมมติฐานของคุณ 

แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับการตั้งค่า และการรันการทดลองบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในบทความที่แยกต่างหาก

[ ![การเดินทางของผู้ใช้การทดสอบ - เชื่อมต่อและแก้ไข](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

หลังจากที่คุณ [ตั้งค่าการทดลองของคุณ](experimentation-setup.md) ในบริการของบุคคลที่สามแล้ว คุณจะเชื่อมต่อการทดลองใน Dynamics 365 Commerce และแก้ไขรูปแบบการทดลอง

## <a name="connect-your-experiment"></a>เชื่อมต่อการทดลองของคุณ
เมื่อต้องการเชื่อมต่อการทดลองของคุณ คุณจะเปิดใช้งานตัวช่วยสร้าง **การทดสอบการเชื่อมต่อ** ตัวช่วยสร้างจะแนะนำให้คุณทราบถึงขั้นตอนต่างๆ ที่จำเป็นในการเชื่อมต่อการทดลองของคุณ เมื่อคุณดำเนินการตัวช่วยสร้าง การทดลองของคุณจะได้รับการเชื่อมต่อและมีการสร้างรูปแบบ และพร้อมที่จะแก้ไข

เมื่อต้องการเริ่มต้นใช้งานเชื่อมต่อการทดลองของคุณบนไซต์ของคุณในตัวสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้

1. เมื่อต้องการเปิดใช้งานตัวช่วยสร้าง **การทดลองการเชื่อมต่อ** ให้เลือก **การทดลอง** ในบานหน้าต่างนำทางด้านซ้าย แล้วเลือก **เชื่อมต่อ** อีกทางหนึ่งคือ คุณสามารถเข้าถึงตัวช่วยสร้างจากหน้าหรือตัวแก้ไขส่วน โดยการแก้ไขและเลือก **การทดสอบการเชื่อมต่อ** บนแถบคำสั่ง

    > [!NOTE]
    > - หน้าสามารถเชื่อมต่อกับหนึ่งการทดลองเท่านั้นในแต่ละครั้ง เมื่อต้องการเชื่อมต่อหน้ากับการทดลองอื่น ให้ลบการทดลองที่มีการเชื่อมต่อกับหน้าในขณะนี้ก่อน
    > - คุณสามารถทดลองได้เฉพาะกับหน้าที่มีเค้าโครงแบบกำหนดเองเท่านั้น ถ้าหน้าของคุณมีโครงร่างที่กําหนดล่วงหน้า ให้แปลงเป็นโครงร่างแบบกําหนดเองก่อน คุณสามารถสิ่งนี้ได้โดยไปที่หน้าและเลือก **แปลงเป็นโครงร่างแบบกําหนดเอง** บนแถบคำสั่ง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโครงร่าง โปรดดูที่ [โครงร่างที่ กําหนดล่วงหน้าและโครงร่างที่กําหนดเอง](templates-layouts-overview.md#preset-and-custom-layouts) 

1. ถ้าคุณเชื่อมต่อกับการทดลองจากแท็บ **การทดลอง** ในบานหน้าต่างนําทางด้านซ้าย ให้เลือกชื่อการทดลองจากรายการที่ปรากฏ
1. เลือกหน้าหรือส่วนที่คุณต้องการรันการทดลองของคุณ
1. ในขั้นตอนสุดท้ายของตัวช่วยสร้าง ให้เลือก **สร้างรูปแบบและออกจากตัวช่วยสร้าง** การเปลี่ยนแปลงสร้างสำหรับการทดลอง 

> [!NOTE]
> ถ้าคุณต้องการกำหนดตารางเวลาเมื่อมีการเผยแพร่การทดลองของคุณไปยังไซต์ที่ใช้งานจริง ให้ตรวจสอบให้แน่ใจว่าเนื้อหาที่คุณต้องการเชื่อมโยงกับการทดลองมีอยู่ในกลุ่มเผยแพร่ *ก่อน* ที่คุณจะเชื่อมต่อการทดลอง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกลุ่มเผยแพร่ ให้อ้างอิงถึง [ทำงานกับกลุ่มเผยแพร่](publish-groups.md)

## <a name="edit-your-variations"></a>แก้ไขการเปลี่ยนแปลงของคุณ

เมื่อคุณออกจากวิซาร์ด **เชื่อมต่อการทดลอง** การเปลี่ยนแปลงจะถูกสร้างขึ้นให้คุณ ทำตามขั้นตอนด้านล่างเพื่อแก้ไขการเปลี่ยนแปลงเพื่อให้สะท้อนถึงตัวเลือกที่คุณต้องการตรวจสอบในสมมติฐานการทดลอง

1. ในมุมมองตัวแก้ไข ให้ใช้เมนูแบบหล่นลงของการเปลี่ยนแปลงใต้แถบคำสั่งเพื่อแก้ไขคการเปลี่ยนแปลงแต่ละแบบตามสมมติฐานดั้งเดิมของคุณ นอกจากนี้คุณอาจต้องการสร้างรูปแบบการควบคุมหรือพื้นฐานโดยไม่ทำการเปลี่ยนแปลงหนึ่งรูปแบบ
1. เลือกโมดูลที่จะทดลอง ให้เลือกจุดไข่ปลา (...) แล้วเลือก **เพิ่มในการทดลอง**

> [!NOTE]
> พิจารณาสร้างรูปแบบการควบคุมหรือพื้นฐานโดยไม่ทำการเปลี่ยนแปลงหนึ่งรูปแบบ

## <a name="previous-step"></a>ขั้นตอนก่อนหน้า
[การตั้งค่าการทดสอบ](experimentation-setup.md) 


## <a name="next-step"></a>ขั้นตอนต่อไป
[แสดงตัวอย่างและเผยแพร่การทดสอบ](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
