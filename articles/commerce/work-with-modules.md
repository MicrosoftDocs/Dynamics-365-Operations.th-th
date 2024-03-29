---
title: ใช้งานโมดูล
description: บทความนี้จะอธิบายว่าจะใช้โมดูลเมื่อไรและอย่างไรใน Microsoft Dynamics 365 Commerce
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 91188590391501042ff0503bdc3592435c30fa63
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291958"
---
# <a name="work-with-modules"></a>ใช้งานโมดูล

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายว่าจะใช้โมดูลเมื่อไรและอย่างไรใน Microsoft Dynamics 365 Commerce

โมดูลเป็นบล็อกส่วนประกอบเชิงตรรกะที่ประกอบขึ้นเป็นโครงสร้างหน้าของคุณ และมีวัตถุประสงค์และขอบเขตที่หลากหลาย โมดูลบางโมดูลเป็นคอนเทนเนอร์ระดับสูง และวัตถุประสงค์ของโมดูลคือรองรับและจัดระเบียบโมดูลอื่น ๆ (โมดูลรอง) เท่านั้น โมดูลอื่น ๆ เช่น โมดูลการจัดวางภาพอย่างง่าย มีวัตถุประสงค์ที่เฉพาะเจาะจงมาก โมดูลอื่น ๆ เช่น โมดูลแบบวงล้อ จะอยู่ระหว่างโมดูลสองประเภทนั้น

โดยค่าเริ่มต้น ไซต์ Dynamics 365 Commerce ของคุณจะมีไลบรารีโมดูลที่ช่วยให้คุณสามารถบรรลุในสถานการณ์อีคอมเมิร์ซขั้นพื้นฐานส่วนใหญ่ได้ คุณควรจะสามารถสร้างไซต์อีคอมเมิร์ซแบบครอบคลุมตั้งแต่ต้นจนจบได้โดยใช้เพียงโมดูลเหล่านี้ อย่างไรก็ตาม คุณอาจต้องการเลือกกำหนดโมดูลเหล่านี้หรือสร้างโมดูลที่กำหนดเองใหม่สำหรับความต้องการเฉพาะ ถ้าคุณต้องการสร้างโมดูลที่กำหนดเอง ชุดพัฒนาซอฟต์แวร์ (SDK) การออกแบบโมดูลมีพร้อมให้คุณใช้งานเพื่อช่วยคุณสร้างไลบรารีโมดูลที่กำหนดเอง

## <a name="container-modules-and-slots"></a>โมดูลคอนเทนเนอร์และช่อง

ดังที่ได้กล่าวถึงก่อนหน้านี้ บางโมดูลถูกออกแบบมาเพื่อรองรับโมดูลรองไว้ โมดูลเหล่านี้เรียกว่า *คอนเทนเนอร์* ซึ่งอนุญาตให้มีลำดับชั้นของโมดูลที่ซ้อนกัน โมดูลคอนเทนเนอร์จะมี *ช่อง* ช่องจะใช้ในการจัดการเค้าโครงและวัตถุประสงค์ของโมดูลรองในคอนเทนเนอร์ ตัวอย่างต่อไปนี้คือโมดูลคอนเทนเนอร์ของหน้าพื้นฐาน (โมดูลระดับบนสุดสำหรับหน้าใด ๆ) ที่กำหนดช่องสำคัญหลายช่อง:

- ช่องส่วนหัว
- ช่องส่วนหัวย่อย
- ช่องหลัก
- ช่องส่วนท้าย
- ช่องส่วนท้ายย่อย

นักพัฒนาโมดูลจะกำหนดช่องเหล่านี้ และกำหนดว่ามีโมดูลรองใดบ้างและมีโมดูลรองกี่โมดูลที่จะสามารถอยู่ในโมดูลนี้ได้ ตัวอย่างเช่น ช่องส่วนหัวอาจสนับสนุนโมดูลเดียวเท่านั้นในประเภท **โมดูลส่วนหัว** ในขณะที่ช่องเนื้อหาอาจสนับสนุนโมดูลได้ไม่จำกัดจำนวนในประเภทใดก็ได้ (ยกเว้นโมดูลคอนเทนเนอร์ของหน้าอื่น)

ในเครื่องมือการสร้าง ผู้สร้างหน้าไม่จำเป็นต้องทราบมาก่อนล่วงหน้าว่าโมดูลใดสามารถและไม่สามารถใส่ในช่องแต่ละช่องได้ เมื่อผู้สร้างหน้าเลือกช่องแล้วลองเลือกโมดูลที่จะเพิ่มเข้าไป พวกเขาจะเห็นมุมมองที่มีการกรองชนิดของโมดูลที่ได้รับการสนับสนุนในช่องนั้น

## <a name="content-modules"></a>โมดูลเนื้อหา

โมดูลเนื้อหามีองค์ประกอบที่เป็นเนื้อหาและสื่อ เช่น ข้อความ (ตัวอย่างเช่น พาดหัว ย่อหน้า และลิงก์) หรือข้อมูลอ้างอิงของสินทรัพย์ (ตัวอย่างเช่น รูปภาพ วิดีโอ และ PDF) ชนิดโมดูเนื้อหาโดยทั่วไปรวมถึงบล็อกเนื้อหา บล็อกข้อความ และโมดูลแบนเนอร์โปรโมชั่น โมดูลของสามชนิดนี้อาจประกอบด้วยข้อความหรือสื่อ และไม่ได้ต้องการโมดูลรองใด ๆ เพื่อให้บางสิ่งแสดงขึ้นบนหน้า

ส่วนมาก กิจกรรมการสร้างหน้าและเนื้อหาวันต่อวันโดยทั่วไปจะเกี่ยวข้องกับโมดูลเนื้อหา โดยส่วนใหญ่แล้วเนื่องจากโมดูลเหล่านี้จะกำหนดเนื้อหาจริงที่จะแสดงขึ้นในโมดูลคอนเทนเนอร์หลัก มีโมดูลเนื้อหาจำนวนมากที่พร้อมใช้งาน และโดยทั่วไปแล้ว โมดูลเหล่านี้จะเป็นส่วนสุดท้ายที่คุณจะเพิ่มลงในลำดับชั้นของหน้าของโมดูลที่ซ้อนกัน

แผนภาพต่อไปนี้แสดงว่าโมดูลซ้อนกันอยู่อย่างไรในช่องโมดูลคอนเทนเนอร์หลัก

![โมดูลที่ซ้อนกัน](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>เพิ่มหรือลบโมดูล

กระบวนงานต่อไปนี้จะอธิบายวิธีการเพิ่มและลบโมดูล

### <a name="add-a-module"></a>เพิ่มโมดูล

เมื่อต้องการเพิ่มโมดูลไปที่ช่องหรือคอนเทนเนอร์ในหน้าหน้าหนึ่ง ให้ทำตามขั้นตอนต่อไปนี้

1. ในบานหน้าต่างเค้าร่างทางด้านซ้ายหรือโดยตรงในพื้นที่ทำงานหลัก ให้เลือกคอนเทนเนอร์หรือช่องที่สามารถเพิ่มโมดูลรองได้

    > [!NOTE]
    > ผู้ออกแบบโมดูลจะกำหนดรายการของชนิดโมดูลที่สามารถเพิ่มเข้าไปในช่องโมดูลเฉพาะได้ ผู้สร้างแม่แบบจะสามารถจำกัดตัวเลือกโมดูลที่อนุญาตเพื่อช่วยรับประกันประสิทธิภาพโปรแกรมค้นหา (SEO) และประสิทธิภาพของการสร้างให้สอดคล้องกันระหว่างหน้าทั้งหมดที่สร้างขึ้นจากแม่แบบแต่ละแม่แบบโดยเฉพาะ เมื่อเพิ่มโมดูลที่ไปช่อง กล่องโต้ตอบ **เพิ่มโมดูล** นี้จะถูกกรองโดยอัตโนมัติ เพื่อให้แสดงเฉพาะโมดูลที่สนับสนุนในคอนเทนเนอร์หรือช่องที่เลือกเท่านั้น รายการของโมดูลที่อนุญาตนี้จะถูกกำหนดโดยแม่แบบของหน้าหรือข้อกำหนดของโมดูลคอนเทนเนอร์

1. ถ้าใช้บานหน้าต่างเค้าร่าง ให้เลือกจุดไข่ปลา (**...**) ถัดจากชื่อโมดูล แล้วเลือก **เพิ่มโมดูล** ถ้าใช้ตัวควบคุมโดยตรงภายในพื้นที่ทำงาน ให้เลือกสัญลักษณ์เครื่องหมายบวก (**+**) ในช่องว่างเปล่าหรือที่อยู่ติดกับโมดูลที่เลือกในปัจจุบัน แล้วเลือก **เพิ่มโมดูล**

    > [!NOTE]
    > ถ้าคอนเทนเนอร์หรือช่องไม่สนับสนุนโมดูลรองใหม่ ตัวเลือก **เพิ่มโมดูล** จะใช้งานไม่ได้

1. ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้ค้นหาและเลือกโมดูลที่จะเพิ่มในหน้าของคุณ

    > [!TIP]
    > **บล็อกเนื้อหา** เป็นชนิดโมดูลที่ดีสำหรับผู้เริ่มต้นที่จะทำงาน

1. เลือก **ตกลง** เพื่อเพิ่มโมดูลที่เลือกลงในคอนเทนเนอร์หรือช่องที่เลือกไว้บนหน้าของคุณ

### <a name="remove-a-module"></a>ลบโมดูล

เมื่อต้องการลบโมดูลใดโมดูลหนึ่งออกจากช่องหรือคอนเทนเนอร์บนหน้า ให้ทำตามขั้นตอนต่อไปนี้

1. ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้เลือกปุ่มจุดไข่ปลา (**...**) ที่อยู่ถัดจากชื่อโมดูลที่ต้องการลบ แล้วเลือกสัญลักษณ์ถังขยะ อีกทางหนึ่งคือ ในพื้นที่ทำงานหลัก คุณสามารถเลือกสัญลักษณ์ถังขยะบนแถบเครื่องมือของโมดูลที่เลือก
1. เมื่อพร้อมต์ให้ยืนยันว่าคุณต้องการลบโมดูลหรือไม่ ให้เลือก **ตกลง**

## <a name="move-a-module-to-a-new-position"></a>ย้ายโมดูลไปตำแหน่งใหม่

เมื่อต้องการย้ายโมดูลไปตำแหน่งใหม่ภายในหน้าของคุณ ให้ใช้วิธีการใดวิธีการหนึ่งต่อไปนี้

### <a name="move-a-module-using-the-outline-pane"></a>ย้ายโมดูลโดยใช้บานหน้าต่างเค้าร่าง

เมื่อต้องการย้ายโมดูลโดยใช้บานหน้าต่างเค้าร่าง ให้ทำตามขั้นตอนต่อไปนี้

1. เลือกและกดโมดูลที่คุณต้องการย้ายในบานหน้าต่างเค้าร่างค้างไว้ แล้วลากโมดูลไปยังตำแหน่งใหม่ในเค้าร่าง เส้นสีน้ำเงินในเค้าร่างและบนพื้นที่ทำงานจะบ่งชี้ว่าสามารถวางโมดูลได้ที่ใด
1. ปล่อยโมดูลลงในตำแหน่งใหม่

### <a name="move-a-module-directly-within-the-canvas"></a>ย้ายโมดูลในภายในพื้นที่ทำงานโดยตรง

เมื่อต้องการย้ายโมดูลโดยตรงภายในพื้นที่ทำงาน ให้ทำตามขั้นตอนต่อไปนี้

1. เลือกโมดูลที่คุณต้องการย้ายในพื้นที่ทำงาน 
1. เลือกสัญลักษณ์ลูกศรชี้ขึ้นหรือลงในแถบเครื่องมือของโมดูล แล้วลากลูกศรไปยังตำแหน่งใหม่บนหน้า เส้นสีน้ำเงินในพื้นที่ทำงานและเค้าร่างจะบ่งชี้ว่าสามารถวางโมดูลได้ที่ใด ถ้าโมดูลไม่สามารถย้ายขึ้นหรือลงได้ สัญลักษณ์ลูกศรจะเป็นสีเทา 
1. ปล่อยโมดูลลงในตำแหน่งใหม่

### <a name="move-a-module-using-the-ellipsis-menu"></a>ย้ายโมดูลโดยใช้เมนูจุดไข่ปลา

เมื่อต้องการย้ายโมดูลโดยใช้เมนูจุดไข่ปลา ให้ทำตามขั้นตอนต่อไปนี้

1. เลือกโมดูลในเค้าร่างหรือพื้นที่ทำงาน
1. เลือกจุดไข่ปลา (**...**) ที่อยู่ถัดจากชื่อของโมดูลในบานหน้าต่างเค้าร่าง หรือแถบเครื่องมือของโมดูลในพื้นที่ทำงาน
1. ถ้าโมดูลสามารถเคลื่อนย้ายขึ้นหรือลงภายในคอนเทนเนอร์หรือช่อง คุณจะเห็นตัวเลือกสำหรับ **เลื่อนขึ้น** หรือ **เลื่อนลง** เลือกตัวเลือกการย้ายที่ต้องการ เพื่อย้ายโมดูลขึ้นหรือลงที่สัมพันธ์กับระดับเดียวกัน

## <a name="configure-modules"></a>ตั้งค่าโมดูล

กระบวนงานต่อไปนี้จะอธิบายวิธีการตั้งค่าโมดูลเนื้อหาและโมดูลคอนเทนเนอร์

### <a name="configure-a-content-module"></a>ตั้งค่าโมดูลเนื้อหา

เมื่อต้องการตั้งค่าโมดูลเนื้อหาบนหน้าใดหน้าหนึ่ง ให้ทำตามขั้นตอนต่อไปนี้

1. ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้ขยายแผนภูมิและเลือกโมดูลเนื้อหาใดๆ (ตัวอย่างเช่น **บล็อกเนื้อหา**) อีกทางหนึ่งคือ คุณสามารถเลือกโมดูลในพื้นที่ทำงานหลักได้
1. ในบานหน้าต่างคุณสมบัติโมดูลที่ด้านขวา ให้ป้อนคุณสมบัติสำหรับตัวควบคุมโมดูลที่ต้องการ
1. บนแถบคำสั่ง ให้เลือก **บันทึก** การทำเช่นนี้จะเป็นการรีเฟรชพื้นที่ทำงานของการแสดงตัวอย่างด้วย

### <a name="edit-module-text-properties"></a>แก้ไขคุณสมบัติข้อความของโมดูล

คุณสมบัติข้อความของโมดูลที่ไม่ใช่แบบอ่านอย่างเดียวสามารถแก้ไขได้โดยตรงในพื้นที่ทำงาน

เมื่อต้องการแก้ไขคุณสมบัติข้อความของโมดูล ให้ทำตามขั้นตอนต่อไปนี้

1. เลือกตัวควบคุมข้อความในพื้นที่ทำงาน แล้ววางเคอร์เซอร์ไว้ตรงจุดที่คุณต้องการแก้ไขข้อความ
1. ป้อนเนื้อหาข้อความของคุณ
1. เลือกที่ใดก็ได้ภายนอกเนื้อหาของข้อความ เพื่อแก้ไขเนื้อหาอื่นๆ ต่อไป

### <a name="inline-image-selection"></a>การเลือกรูปแบบอินไลน์

รูปภาพของโมดูลที่ไม่ใช่แบบอ่านอย่างเดียวสามารถเปลี่ยนได้โดยตรงจากพื้นที่ทำงาน

เมื่อต้องการเลือกรูปภาพใหม่สำหรับโมดูลเนื้อหา ให้ทำตามขั้นตอนต่อไปนี้

1. ในพื้นที่ทำงาน ให้คลิกรูปภาพสองครั้ง การทำเช่นนี้จะเรีบกหน้าต่างตัวเลือกสื่อ
1. ค้นหาและเลือกรูปภาพใหม่ที่คุณต้องการใช้ แล้วเลือก **ตกลง** ขณะนี้มีการแสดงรูปภาพใหม่ในพื้นที่ทำงาน

### <a name="configure-a-container-module"></a>การตั้งค่าโมดูลคอนเทนเนอร์

เมื่อต้องการตั้งค่าคอนเทนเนอร์บนหน้าใดหน้าหนึ่ง ให้ทำตามขั้นตอนต่อไปนี้

1. เลือกโมดูลคอนเทนเนอร์โมดูลหนึ่งบนหน้าของคุณ (ตัวอย่างเช่น โมดูลคอนเทนเนอร์แบบวงล้อหรือแบบลื่นไหล)
1. ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้ขยายตัวควบคุมที่ซ้อนกันอยู่ โดยเลือกหัวข้อและตั้งค่าการควบคุมใด ๆ ที่จำเป็น
1. ในบานหน้าต่างเค้าร่างทางด้านซ้าย ให้เลือกปุ่มจุดไข่ปลาที่อยู่ถัดจากชื่อคอนเทนเนอร์หรือชื่อของช่องใด ๆ ในคอนเทนเนอร์ แล้วเลือก **เพิ่มโมดูล** จากนั้น เพิ่มโมดูลรองให้กับคอนเทนเนอร์ที่เลือก สำหรับข้อมูลเพิ่มเติม โปรดดูที่ส่วน [ทำงานกับโมดูล](#add-a-module) ที่กล่าวถึงก่อนหน้านี้ในบทความนี้
1. ถ้ามีโมดูลรองหลายโมดูลอยู่ระดับเดียวกันในคอนเทนเนอร์หลัก คุณสามารถเปลี่ยนลำดับการแสดงผลในคอนเทนเนอร์หลักได้ เลือกปุ่มจุดไข่ปลาสำหรับโมดูล แล้วใช้ปุ่มลูกศรขึ้นและปุ่มลูกศรลง

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของเท็มเพลตและเค้าโครง](templates-layouts-overview.md)

[ใช้งานเท็มเพลต](work-with-templates.md)

[ใช้งานเค้าโครงที่กำหนดไว้ล่วงหน้า](work-with-layouts.md)

[ใช้งานส่วนย่อย](work-with-fragments.md)

[เพิ่มโมดูลคอนเทนเนอร์ไปยังหน้า](add-container-module.md)

[ทำงานกับกลุ่มการเผยแพร่](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
