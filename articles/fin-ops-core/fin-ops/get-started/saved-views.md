---
title: มุมมองที่บันทึก
description: บทความนี้จะอธิบายวิธีการใช้คุณลักษณะของมุมมองที่บันทึกไว้
author: jasongre
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 571a4f403da0d20256f788c791cab273827c91b5
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799503"
---
# <a name="saved-views"></a>มุมมองที่บันทึก

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

[!INCLUDE [PEAP](../../../includes/peap-1.md)]

## <a name="introduction"></a>บทนำ

การตั้งค่าส่วนบุคคลมีบทบาทสำคัญในการอนุญาตให้ผู้ใช้และองค์กรสามารถปรับปรุงประสบการณ์การใช้งานของผู้ใช้เพื่อตอบสนองความต้องการของพวกเขา สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับการตั้งค่าส่วนบุคคล ดู [ปรับประสบการณ์ผู้ใช้เป็นแบบส่วนตัว](personalize-user-experience.md)

การตั้งค่าส่วนบุคคลแบบดั้งเดิมช่วยให้ผู้ใช้มีการตั้งค่าส่วนบุคคลสำหรับแต่ละหน้าได้เพียงชุดเดียวเท่านั้น คุณลักษณะ **มุมมองที่บันทึกไว้** ขยายบนการตั้งค่าส่วนบุคคลโดยมีวิธีที่สำคัญหลายวิธี:

- มุมมองอนุญาตให้ผู้ใช้มีชุดที่มีการตั้งชื่อหลายชุดของการตั้งค่าส่วนบุคคลสำหรับแต่ละแบบฟอร์ม ซึ่งพวกเขาสามารถสลับได้อย่างรวดเร็วตามความต้องการ การทำเช่นนี้จะช่วยให้ผู้ใช้สามารถสร้างมุมมองที่ดีที่สุดหลายอย่างของหน้า ซึ่งแต่ละมุมมองได้รับการปรับแต่งให้เหมาะสมกับความต้องการของการดำเนินงานธุรกิจเฉพาะ 
- มุมมองที่สร้างขึ้นสำหรับชนิดของหน้าเฉพาะ ยังอาจรวมถึงตัวกรองที่ผู้ใช้เพิ่มหรือการเรียงลำดับ ซึ่งช่วยให้ผู้ใช้สามารถกลับไปยังชุดข้อมูลที่ถูกกรองโดยทั่วไปได้อย่างรวดเร็ว ดูที่ส่วน [หน้าที่สนับสนุนมุมมอง](saved-views.md#what-pages-support-views) สำหรับรายละเอียดเพิ่มเติม 
- สามารถเผยแพร่มุมมองกับผู้ใช้ในบทบาทความปลอดภัยเฉพาะและนิติบุคคลเฉพาะ ดังนั้น ผู้ใช้ใดๆ ที่มีบทบาทที่ระบุและเข้าถึงนิติบุคคลที่ระบุสามารถเข้าถึงและใช้มุมมองดังกล่าวได้ ถึงแม้ว่าผู้ใช้จะไม่มีสิทธิ์ปรับแต่งได้ ความสามารถในการเผยแพร่นี้ทำให้องค์กรสามารถกำหนดมุมมองมาตรฐานขององค์กรที่ได้รับการปรับให้เหมาะสมสำหรับธุรกิจของพวกเขา สำหรับข้อมูลเพิ่มเติม ดูที่ส่วน [การจัดการการตั้งค่าส่วนบุคคลที่ระดับองค์กรกับมุมมอง](saved-views.md#managing-personalizations-at-an-organizational-level-with-views)
- ซึ่งแตกต่างจากการตั้งค่าส่วนบุคคลแบบดั้งเดิม มุมมองจะไม่ถูกบันทึกโดยอัตโนมัติ เมื่อผู้ใช้ดำเนินการการตั้งค่าส่วนบุคคลหรือกรองรายการ จำเป็นต้องมีการบันทึกที่ชัดเจนเพื่อให้ผู้ใช้มีความยืดหยุ่นในการสร้างมุมมองก่อนหรือหลังจะมีการเปลี่ยนแปลงที่เกี่ยวข้องกับมุมมองนั้น ข้อกำหนดนี้ยังช่วยให้มั่นใจว่าจะไม่มีการเปลี่ยนแปลงข้อกำหนดมุมมองโดยไม่ได้ตั้งใจโดยตัวกรองหรือบุคคลที่ไม่ได้ตั้งใจไว้สำหรับการใช้งานในระยะยาว สินค้าที่ระบบจัดเก็บโดยอัตโนมัติเป็นส่วนหนึ่งของการใช้งานหน้าทั่วไป (ตัวอย่างเช่น ความกว้างของคอลัมน์ หรือรัฐแบบขยายหรือยุบของส่วน) จะถูกบันทึกไว้สำหรับแต่ละมุมมอง
- สามารถเพิ่มมุมมองไปยังพื้นที่ทำงานเป็นไทล์ รายการ หรือลิงค์ ดังนั้น ชุดข้อมูลที่ถูกกรองอาจถูกแสดงในพื้นที่ทำงาน และผู้ใช้สามารถเชื่อมโยงชุดของการตั้งค่าเป็นแบบส่วนบุคคลที่เกี่ยวข้องกับชุดข้อมูลที่มีไทล์หรือลิงค์

## <a name="switching-between-views"></a>การสลับระหว่างมุมมอง

หลังจากที่ทำให้มุมมองสำหรับสภาพแวดล้อมพร้อมใช้งานแล้ว ที่ด้านบนของหน้าใดก็ตามที่สนับสนุนมุมมองจะรวมตัวควบคุมมุมมองที่ยุบแล้วไว้ ซึ่งแสดงชื่อของมุมมองปัจจุบัน

มีการเปลี่ยนแปลงขนาดสองรายการไปยังตัวเลือกมุมมอง: 

- **ตัวเลือกมุมมองที่มีขนาดใหญ่** – หน้าที่มีคุณลักษณะรายการอย่างชัดเจนจะมีตัวเลือกมุมมองที่ใหญ่กว่าด้วยเหตุผลสองสามประการ ที่สำคัญที่สุดคือ ตัวเลือกมุมมองที่ใหญ่ขึ้นจะบ่งชี้หน้าที่ซึ่งมุมมองนั้นสามารถมีตัวกรองและการเรียงลำดับที่ผู้ใช้กำหนด เนื่องจากตัวกรองและการเรียงลำดับถูกรวมไว้ในมุมมอง จะมีการรับประกันขนาดของตัวเลือกที่มีขนาดใหญ่กว่า เนื่องจากชื่อของมุมมองมักจะเป็นคำอธิบายที่ดีที่สุดของข้อมูลที่แสดงบนหน้าจอ และความคาดหวังคือผู้ใช้จะสลับระหว่างมุมมองต่างๆ บ่อยครั้งกว่าบนชนิดหน้าเหล่านี้ การจัดกลุ่มในกริดยังสามารถบันทึกไปยังมุมมองบนหน้าที่มีตัวเลือกมุมมองขนาดใหญ่ด้วย 
    
    [![ตัวเลือกมุมมองขนาดใหญ่ที่สนับสนุนการแก้ไขการสอบถามบนมุมมอง](./media/views-largeViewSelector.png)](./media/views-largeViewSelector.png)

- **ตัวเลือกมุมมองขนาดเล็ก** – หน้าแบบเต็มหน้าจออื่นๆ ทั้งหมด (ยกเว้นพื้นที่ทำงานและแดชบอร์ด) มีตัวเลือกมุมมองที่เล็กลงซึ่งจะปรากฏขึ้นถัดจากคำอธิบายหน้า มุมมองบนหน้าเหล่านี้จะรวมการกำหนดเป็นแบบส่วนบุคคลเท่านั้น และไม่ใช่ตัวกรองที่กำหนดโดยผู้ใช้ ในหน้าเหล่านี้ คำอธิบายหรือชื่อเรกคอร์ดมักจะเป็นข้อมูลที่สำคัญที่สุดที่ด้านบนของหน้า นอกจากนี้ ขนาดที่เล็กลงของตัวเลือกมุมมองจะสะท้อนถึงความถี่ต่ำกว่าของการสลับมุมมองที่คาดไว้ไปยังหน้าเหล่านี้ 
    
    [![ตัวเลือกมุมมองขนาดเล็กที่ไม่สนับสนุนการแก้ไขการสอบถามบนมุมมอง](./media/views-smallViewSelector.png)](./media/views-smallViewSelector.png)
 
ถ้าคุณเลือกที่ชื่อมุมมอง ตัวเลือกมุมมองจะเปิดขึ้นและแสดงรายการของมุมมองที่มีอยู่สำหรับหน้า

ถ้าคุณลักษณะ **นิติบุคคลที่ปรับปรุงแล้วของมุมมองที่บันทึกไว้** ถูกเปิดไว้ ตัวเลือกมุมมองจะแสดงมุมมองที่มีอยู่ในสองส่วน ส่วนแรกแสดงมุมมองใดๆ ที่เฉพาะเจาะจงให้กับนิติบุคคลปัจจุบัน และมุมมองที่สองจะแสดงมุมมองที่พร้อมใช้งานของนิติบุคคลทั้งหมด ส่วนแรกจะปรากฏเฉพาะเมื่อมีมุมมองเฉพาะนิติบุคคลของหน้าเท่านั้น

- **มุมมองมาตรฐาน** – มุมมอง **มาตรฐาน** เป็นมุมมองแบบสำเร็จรูปของหน้า ที่ไม่มีการใช้การกำหนดเป็นแบบส่วนบุคคล
- **มุมมองส่วนบุคคล** – มุมมองที่ไม่มีแม่กุญแจแสดงมุมมองส่วนบุคคลของคุณ รายการเหล่านี้คือมุมมองที่คุณได้สร้างขึ้น หรือผู้ดูแลระบบของคุณได้กำหนดให้กับคุณ
- **มุมมองที่ถูกล็อค** – บางมุมมอง (เช่น มุมมอง **มาตรฐาน** และมุมมองใดๆ ที่เผยแพร่ไปยังบทบาทของคุณ) มีสัญลักษณ์แม่กุญแจอยู่ถัดไปในตัวเลือกมุมมอง สัญลักษณ์นี้บ่งชี้ว่าคุณไม่สามารถแก้ไขมุมมองเหล่านั้นได้ อย่างไรก็ตาม การเปลี่ยนแปลงซึ่งสะท้อนถึงการใช้หน้าจะถูกบันทึกโดยอัตโนมัติ การเปลี่ยนแปลงเหล่านี้รวมถึงการเปลี่ยนแปลงความกว้างของคอลัมน์กริด และการเปลี่ยนแปลงเป็นสถานะที่ขยายหรือยุบของแท็บด่วน อย่างไรก็ตาม ถ้าคุณมีสิทธิ์ในการตั้งค่าส่วนบุคคล คุณสามารถใช้การดำเนินการ **บันทึกเป็น** เพื่อสร้างมุมมองส่วนบุคคลที่เป็นไปตามมุมมองที่ถูกล็อคได้
- **มุมมองใหม่** – มุมมองที่มีการเผยแพร่ซึ่งยังไม่ได้รับการเปิดมีสัญลักษณ์จุดประกายทางด้านซ้ายของชื่อมุมมอง

เมื่อต้องการสลับไปยังมุมมองอื่น ให้เปิดตัวเลือกมุมมองก่อน แล้วเลือกมุมมองที่คุณต้องการโหลด 

## <a name="creating-and-modifying-views"></a>การสร้างและการปรับเปลี่ยนมุมมอง

ซึ่งแตกต่างจากการตั้งค่าส่วนบุคคลแบบดั้งเดิม มุมมองจะไม่ถูกบันทึกโดยอัตโนมัติ เมื่อผู้ใช้ปรับแต่งหน้า หรือเมื่อผู้ใช้ใช้ตัวกรองข้อมูลกับรายการหรือเรียงลำดับ ต้องมีการดำเนินการที่ชัดแจ้งเพื่อบันทึกการเปลี่ยนแปลงเหล่านี้ลงในมุมมอง ข้อกำหนดนี้ให้ผู้ใช้มีความยืดหยุ่นในการสร้างมุมมองก่อนหรือหลังจะมีการเปลี่ยนแปลงที่เกี่ยวข้องกับมุมมองนั้น นอกจากนี้ยังช่วยให้มั่นใจว่าจะไม่มีการเปลี่ยนแปลงข้อกำหนดมุมมองโดยไม่ได้ตั้งใจโดยตัวกรองแบบครั้งเดียวหรือแบบส่วนบุคคล โปรดจำไว้ว่าสินค้าของการใช้งานหน้าทั่วไป (ตัวอย่างเช่น ความกว้างของคอลัมน์ หรือรัฐแบบขยายหรือยุบของส่วน) จะถูกบันทึกไว้โดยอัตโนมัติสำหรับแต่ละมุมมองปัจจุบัน แม้แต่สำหรับมุมมองที่ล็อค

เพื่อตรวจสอบให้แน่ใจว่าสถานะปัจจุบันของมุมมองเป็นที่รู้จัก เมื่อคุณเริ่มทำการเปลี่ยนแปลงในมุมมองโดยการดำเนินการตั้งค่าส่วนบุคคลหรือการกรองข้อมูล เครื่องหมายดอกจัน (\*) จะปรากฏขึ้นถัดจากชื่อมุมมองปัจจุบัน สัญลักษณ์นี้บ่งชี้ว่าคุณกำลังดูที่รุ่นที่ถูกปรับเปลี่ยนซึ่งไม่ได้บันทึกไว้ของมุมมองนั้น

[![การเปลี่ยนแปลงที่ไม่ได้บันทึกบนมุมมอง](./media/views-unsavedChanges.png)](./media/views-unsavedChanges.png)

ถ้าคุณต้องการบันทึกการเปลี่ยนแปลงเหล่านั้น ให้ทำตามขั้นตอนเหล่านี้

1. เลือกชื่อมุมมอง เพื่อเปิดตัวเลือกมุมมอง
2. เมื่อต้องการปรับเปลี่ยนมุมมองที่มีอยู่ เลือก **บันทึก** โปรดทราบว่าการดำเนินการนี้จะไม่พร้อมใช้งานสำหรับมุมมองที่ถูกล็อค 
3. เพื่อสร้างมุมมองใหม่:

    1. เลือก **บันทึกเป็น** 
    2. ในบานหน้าต่าง **บันทึกมุมมองเป็น** ให้ป้อนชื่อและอธิบายของมุมมองด้วยก็ได้
    3. หากคุณต้องการให้มุมมองนี้เป็นมุมมองเริ่มต้นของคุณ ให้เลือก **ปักหมุดเป็นค่าเริ่มต้น** สำหรับข้อมูลเพิ่มเติมเกี่ยวกับมุมมองเริ่มต้น โปรดดูที่ส่วน [การเปลี่ยนมุมมองเริ่มต้น](#changing-the-default-view) ต่อจากนั้น 
    4. ถ้าคุณลักษณะ **นิติบุคคลที่ปรับปรุงแล้วของมุมมองที่บันทึกไว้** ถูกเปิดไว้ คุณสามารถเลือกได้ว่าคุณต้องการให้มุมมองนี้พร้อมใช้งานเฉพาะกับนิติบุคคลทั้งหมดหรือเฉพาะชุดย่อยเท่านั้น
    5. เลือก **บันทึก**

## <a name="changing-the-default-view"></a>การเปลี่ยนแปลงมุมมองเริ่มต้น

มุมมองเริ่มต้นคือมุมมองที่ระบบพยายามเปิด เมื่อคุณเปิดหน้าเป็นครั้งแรก คุณควรตั้งค่ามุมมองเริ่มต้นเป็นมุมมองที่คุณคาดว่าจะใช้บ่อยที่สุด 

> [!NOTE]
> - ในคุณลักษณะ **มุมมองที่บันทึกไว้** พื้นฐาน จะมีมุมมองเริ่มต้นแบบครอบคลุมมุมมองเดียวทั่วทั้งนิติบุคคล ถ้าคุณเปลี่ยนมุมมองเริ่มต้น มุมมองนั้นจะมีการเปิดโดยค่าเริ่มต้น โดยไม่คำนึงถึงนิติบุคคลที่คุณกำลังอยู่ในปัจจุบัน
> - เมื่อคุณลักษณะ **นิติบุคคลที่ปรับปรุงแล้วของมุมมองที่บันทึกไว้** ถูกเปิดไว้ นิติบุคคลแต่ละแห่งสามารถมีมุมมองเริ่มต้นของตัวเองในแต่ละหน้า

หากต้องการเปลี่ยนแปลงมุมมองเริ่มต้นสำหรับหน้า ให้ทำตามขั้นตอนเหล่านี้:

1. สลับไปยังมุมมองที่คุณใช้เป็นค่าเริ่มต้น 
2. เลือกชื่อมุมมอง เพื่อเปิดตัวเลือกมุมมอง 
3. เลือก **เพิ่มเติม** แล้วจากนั้น **ปักหมุดเป็นค่าเริ่มต้น**

อีกทางหนึ่งคือ เมื่อคุณสร้างมุมมองใหม่ (โดยใช้การดำเนินการ **บันทึกเป็น**) คุณสามารถทำให้มุมมองใหม่เป็นมุมมองเริ่มต้นด้วยการตั้งค่าตัวเลือก **ปักหมุดเป็นค่าเริ่มต้น** ก่อนที่คุณจะบันทึกมุมมอง

> [!WARNING]
> ในบางกรณี การสอบถามที่เชื่อมโยงกับมุมมองเริ่มต้นจะไม่ดำเนินการ เมื่อคุณเปิดหน้าเป็นครั้งแรก ตัวอย่างเช่น ถ้าคุณเปิดหน้าผ่านไทล์ การสอบถามของไทล์จะถูกดำเนินการ โดยไม่คำนึงถึงการสอบถามที่เชื่อมโยงกับมุมมองเริ่มต้น นอกจากนี้ ถ้าคุณเปิดหน้าที่มีมุมมอง **มาตรฐาน** ที่มีการสอบถามที่กำหนดไว้แล้ว การสอบถามดั้งเดิมจะดำเนินการแทนการสอบถามของมุมมองเริ่มต้น ในกรณีนี้ คุณจะได้รับข้อความที่ให้ข้อมูลเมื่อมุมมองถูกโหลดด้วยการดำเนินการที่ฝังอยู่ ซึ่งช่วยให้คุณสามารถโหลดการสอบถามของมุมมองเริ่มต้นได้โดยตรง ถ้าคุณสลับมุมมองหลังจากการโหลดหน้าแล้ว การสอบถามมุมมองควรจะสามารถเรียกใช้ได้ตามที่คาดไว้ 

## <a name="managing-personal-views"></a>การจัดการมุมมองส่วนบุคคล

กล่องโต้ตอบ **จัดการมุมมองของฉัน** จะช่วยให้คุณสามารถทำการบำรุงรักษาพื้นฐานสำหรับมุมมองส่วนตัวของคุณ และลำดับของมุมมองในตัวเลือกมุมมอง เมื่อต้องการเปิดหน้านี้ ให้เลือกชื่อมุมมองเพื่อเปิดเมนูแบบหล่นลงของตัวเลือกมุมมอง เลือก **เพิ่มเติม** แล้วเลือก **จัดการมุมมองของฉัน**

ถ้าเปิดคุณลักษณะ **นิติบุคคลที่ปรับปรุงแล้วของมุมมองที่บันทึกไว้** ส่วน **มุมมองของฉัน** ของกล่องโต้ตอบ **จัดการมุมมองของฉัน** จะแสดงมุมมองที่พร้อมใช้งานของหน้าในส่วนต่างๆ มุมมองใดๆ ที่เฉพาะเจาะจงของนิติบุคคลปัจจุบันจะแสดงขึ้นในส่วนของตนเอง ส่วน **มุมมองส่วนกลาง** จะแสดงขึ้นเสมอ เพื่อให้คุณสามารถจัดการมุมมองที่พร้อมใช้งานกับหน้าในนิติบุคคลทั้งหมด 

สำหรับรายการของมุมมองที่พร้อมใช้งานสำหรับหน้าดังกล่าว ชุดของการดำเนินการต่อไปนี้จะพร้อมใช้งาน

- **เปลี่ยนมุมมองเริ่มต้น** – ใช้การดำเนินการ **ปักหมุดเป็นค่าเริ่มต้น** เพื่อทำให้มุมมองที่เลือกอยู่ในปัจจุบันเป็นมุมมองเริ่มต้นสำหรับหน้านี้ ถ้าเปิดคุณลักษณะ **การนําเข้ามุมมองที่บันทึกไว้** ส่วน **มุมมองส่วนกลาง** จะช่วยให้คุณสามารถสร้างมุมมองมุมมองเริ่มต้นของนิติบุคคลปัจจุบันหรือนิติบุคคลทั้งหมด
- **เรียงลำดับมุมมองของคุณใหม่** – ใช้การดำเนินการ **เลื่อนขึ้น** และ **เลื่อนลง** เพื่อจัดเรียงมุมมองของคุณใหม่ในใบสั่งเฉพาะ
- **เปลี่ยนชื่อมุมมองใหม่** – ใช้การดำเนินการ **เปลี่ยนชื่อ** เพื่อเปลี่ยนชื่อของมุมมองส่วนบุคคลที่เลือกอยู่ในขณะนี้ การดำเนินการนี้ถูกปิดสำหรับมุมมองที่ถูกล็อค 
- **ลบมุมมอง** – ให้ใช้การดำเนินการ **ลบ** เพื่อลบมุมมองที่เลือกอยู่ในปัจจุบันออกจากหน้าอย่างถาวร ไม่มีวิธีการกู้คืนมุมมองหลังจากที่คุณลบออก

การเปลี่ยนแปลงใดๆ ที่ทำในกล่องโต้ตอบนี้ จะมีผลหลังจากที่คุณเลือกปุ่ม **อัปเดต**

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>การจัดการการตั้งค่าเป็นแบบส่วนบุคคลที่ระดับองค์กรที่มีมุมมอง

เพื่อช่วยให้คุณเข้าใจวิธีการที่มุมมองที่บันทึกไว้ช่วยปรับปรุงการจัดการการตั้งค่าเป็นแบบส่วนบุคคลในระดับองค์กร ส่วนนี้จะอธิบายถึงความแตกต่างในการจัดการการตั้งค่าเป็นแบบส่วนบุคคลพร้อมกับหรือไม่พร้อมกับคุณลักษณะ **มุมมองที่ถูกบันทึก**

โดยไม่มีมุมมอง ผู้ดูแลระบบจะใช้ชุดของการตั้งค่าส่วนบุคคลสำหรับหน้ากับผู้ใช้ หรือกลุ่มของผู้ใช้ผ่านทางหน้าการตั้งค่าส่วนบุคคล ถ้าผู้ใช้เหล่านั้นมีสิทธิ์ในการตั้งค่าส่วนบุคคล การตั้งค่าส่วนบุคคลจะถูกนำไปใช้กับหน้าดังกล่าว อย่างไรก็ตาม ไม่มีความสามารถในการป้องกันผู้ใช้จากการตั้งค่าหน้าให้เป็นส่วนบุคคลเพิ่มเติม ซึ่งหมายความว่าองค์กรไม่สามารถตรวจสอบให้แน่ใจว่าผู้ใช้มีอินเทอร์เฟสผู้ใช้ที่สอดคล้องกัน ถ้าผู้ใช้เหล่านั้นใดๆ ไม่มีสิทธิ์ในการตั้งค่าเป็นแบบส่วนบุคคล การตั้งค่าเป็นแบบส่วนบุคคลที่ให้กับผู้ใช้เหล่านั้นโดยผู้ดูแลระบบไม่ได้รับการโหลด นอกจากนี้ ถ้าผู้ใช้ใหม่ได้รับการว่าจ้างในองค์กร ผู้ดูแลระบบที่จำเป็นสำหรับการโหลดชุดของการตั้งค่าส่วนบุคคลสำหรับผู้ใช้ด้วยตนเอง ไม่มีกลไกอัตโนมัติสำหรับการระบุว่า ชุดที่แน่นอนของการตั้งค่าส่วนบุคคลควรพร้อมใช้งานสำหรับผู้ใช้ในบทบาทนั้น

คุณลักษณะ **มุมมองที่บันทึก** ทำให้การจัดการเชิงองค์กรของการตั้งค่าเป็นแบบส่วนบุคคลง่ายขึ้นอย่างมาก ส่วนใหญ่แล้วเนื่องจากสามารถเผยแพร่มุมมองไปยังกลุ่มของผู้ใช้ได้ หลังจากที่มีการเผยแพร่มุมมองแล้ว ผู้ใช้ใดๆ ที่มีบทบาทความปลอดภัยที่กำหนดไว้อย่างใดอย่างหนึ่งและจะสามารถเข้าถึงนิติบุคคลที่ระบุสามารถดูและใช้มุมมองได้ แม้ว่าผู้ใช้นั้นจะไม่มีสิทธิเข้าถึงการตั้งค่าส่วนบุคคลได้ แม้ว่าผู้ใช้ทุกรายมีสำเนาของมุมมองที่เผยแพร่ที่ซึ่งสินค้าของการใช้การใช้งานหน้าโดยอัตโนมัติ ไม่มีผู้ใช้ที่สามารถบันทึกการตั้งค่าเป็นแบบส่วนบุคคล หรือการอัปเดตการสอบถามไปยังมุมมองที่เผยแพร่ กล่าวคือมุมมองที่เผยแพร่ถูกล็อค นอกจากนี้ ถ้าผู้ใช้ใหม่ได้รับบทบาทในนิติบุคคลที่มีการเผยแพร่มุมมองไป ผู้ใช้จะเห็นมุมมองที่สัมพันธ์กับบทบาทและนิติบุคคลของตนโดยอัตโนมัติ ไม่จำเป็นต้องมีการดำเนินการเพิ่มเติมใดๆ โดยผู้ดูแลระบบ ในทำนองเดียวกัน ถ้าผู้ใช้เปลี่ยนบทบาทในองค์กรหรือมีสิทธิ์เข้าถึงนิติบุคคลต่างๆ พวกเขาอาจไม่สามารถเข้าถึงมุมมองที่ถูกเผยแพร่ไว้ก่อนหน้านี้ให้กับพวกเขาได้อีกต่อไป อีกครั้ง ต้องมีการดำเนินการเพิ่มเติมโดยผู้ดูแลระบบ

การอัปเดตไปยังมุมมองที่เผยแพร่ สามารถกระจายไปยังผู้ใช้ได้โดยง่ายโดยการเผยแพร่มุมมองอีกครั้งไปยังบทบาทความปลอดภัยและนิติบุคคลที่เหมาะสม

ความสามารถในการเผยแพร่ทำให้องค์กรสามารถกำหนดมุมมองมาตรฐานขององค์กรที่ได้รับการปรับให้เหมาะสมสำหรับธุรกิจของพวกเขา ซึ่งมีเป้าหมายที่ผู้ใช้ในบทบาทความปลอดภัยเฉพาะ

## <a name="publishing-views"></a>การเผยแพร่มุมมอง

ในระหว่างกระบวนการเผยแพร่ สามารถกำหนดมุมมองให้กับบทบาทความปลอดภัยหนึ่งรายการขึ้นไปสำหรับนิติบุคคลอย่างน้อยหนึ่งรายการ ดังนั้น ผู้ใช้ใดๆ ที่มีสิทธิเข้าถึงนิติบุคคลและผู้ที่ได้รับการกำหนดให้กับบทบาทใดบทบาทหนึ่งดังกล่าวจะสามารถเข้าถึงและใช้มุมมองได้ อย่างไรก็ตาม ผู้ใช้ไม่สามารถแก้ไขมุมมอง โดยค่าเริ่มต้น ผู้ดูแลระบบมีสิทธิ์เข้าถึงไปยังการดำเนินการ **เผยแพร่** ในเมนูแบบหล่นลงของตัวเลือกมุมมอง อย่างไรก็ตาม ผู้ใช้ที่ได้รับความไว้วางใจอื่นๆ ในองค์กรของคุณอาจได้รับสิทธิ์ให้เข้าถึงเพื่อดูการเผยแพร่ผ่านบทบาท **ผู้ดูแลใหม่ที่บันทึกไว้**

หากต้องการเผยแพร่มุมมอง ทำตามขั้นตอนเหล่านี้:

1. สร้างและบันทึกสำเนาส่วนบุคคลของมุมมองที่คุณต้องการเผยแพร่ 
2. ด้วยมุมมองนั้นที่โหลดในขณะนี้ เลือกชื่อมุมมองเพื่อเปิดเมนูแบบหล่นลงของตัวเลือกมุมมอง 
3. เลือกปุ่ม **เพิ่มเติม** แล้วเลือก **เผยแพร่** กล่องโต้ตอบ **การเผยแพร่** จะเปิดขึ้น
4. ป้อนชื่อสำหรับมุมมอง ชื่อที่คุณป้อนคือ ชื่อที่ผู้ใช้ที่ได้รับมุมมองนี้จะเห็นในตัวเลือกมุมมองของพวกเขา ชื่อของมุมมองที่เผยแพร่สำหรับหน้าต้องไม่ซ้ำกัน ไม่อนุญาตให้ใช้ชื่อที่ซ้ำกัน ถึงแม้ว่าจะมีการใช้รายการของบทบาทหรือนิติบุคคลที่มีการใช้มุมมองเพื่อให้แตกต่างกัน
5. ถ้าเปิดคุณลักษณะ **การสนับสนุนการแปลของมุมมององค์กร** คุณสามารถเพิ่มการแปลให้กับชื่อมุมมองของคุณในหลายภาษาตามที่องค์กรของคุณต้องการได้ โดยเลือกปุ่ม **การแปล** ถัดจากฟิลด์ **ชื่อ** จากนั้นชื่อมุมมองจะแสดงต่อผู้ใช้ในภาษาปัจจุบัน คุณยังสามารถกําหนดภาษาเริ่มต้นเพื่อระบุการแปลที่จะแสดงต่อผู้ใช้ที่เรียกใช้ภาษาซึ่งไม่มีการกําหนดการแปลให้
5. ไม่ระบุ: ป้อนค่าอธิบายให้กับมุมมอง เพื่อให้ผู้ใช้ที่ได้รับมุมมองนี้เข้าใจวัตถุประสงค์ของมุมมองนี้ได้ดียิ่งขึ้น 
6. ตรวจสอบว่าควรเผยแพร่มุมมองเป็นมุมมองเริ่มต้นสำหรับผู้ใช้ที่เลือกหรือไม่ เมื่อทำให้มุมมองเป็นค่าเริ่มต้น ผู้ใช้จะเห็นในครั้งต่อไปที่จะเปิดหน้าเป้าหมาย มุมมองเริ่มต้นสากลเดียวของผู้ใช้ที่มีการกำหนดเป้าหมายทั้งหมดจะมีการเปลี่ยนแปลง อย่างไรก็ตาม ผู้ใช้ยังคงสามารถเปลี่ยนมุมมองเริ่มต้นของตนหลังจากที่มีการเผยแพร่เกิดขึ้นได้

    > [!NOTE]
    > โปรดทราบว่าลักษณะการทำงานต่อไปนี้เมื่อคุณเผยแพร่มุมมองเป็นมุมมองเริ่มต้น
    >
    > - ถ้าคุณเผยแพร่มุมมองเป็นมุมมองเริ่มต้นไปยังนิติบุคคลบางรายการหรือทั้งหมด ลักษณะการทำงานต่อไปนี้จะเกิดขึ้น
    >
    >    - หากเปิดเฉพาะคุณลักษณะ **มุมมองที่บันทึกไว้พื้นฐานไว้** มุมมองเริ่มต้นแบบครั้งเดียว มุมมองเริ่มต้นส่วนกลางจะเปลี่ยนแปลงไปของผู้ใช้ที่เป็นเป้าหมายทุกคน 
    >    - ** ถ้าเปิดคุณลักษณะ **นิติบุคคลที่ปรับปรุงแล้วของมุมมองที่บันทึกไว้** และคุณเผยแพร่มุมมองนั้นไปยังชุดย่อยของนิติบุคคล มุมมองเริ่มต้นของนิติบุคคลเหล่านั้นจะเปลี่ยนไปของผู้ใช้ที่เป็นเป้าหมายทุกคน
    >
    > - ถ้าผู้ใช้มีบทบาทที่มีการเผยแพร่มุมมองต่างๆ เป็นมุมมองเริ่มต้น มุมมองล่าสุดที่มีการเผยแพร่จะมีการใช้เป็นมุมมองเริ่มต้นของผู้ใช้ 
    > - การเผยแพร่จะไม่ใช้งานการมอบหมายบทบาทที่จัดสร้างโดยใช้กลุ่ม AAD 

8. เพิ่มบทบาทความปลอดภัยที่สอดคล้องกับผู้ใช้ที่ถูกกำหนดเป็นเป้าหมายโดยมุมมองนี้ 
9. ตรวจสอบว่าคุณต้องการเผยแพร่มุมมองให้กับบทบาทรองของแต่ละบทบาทความปลอดภัยที่เลือกหรือไม่ หากคุณต้องการ ให้เลือกกล่องกาเครื่องหมาย **รวมบทบาทรอง** ในแถวสำหรับบทบาทความปลอดภัยที่เหมาะสม โปรดทราบว่ากล่องกาเครื่องหมายนี้จะไม่พร้อมใช้งานสำหรับบทบาทที่ไม่มีบทบาทรอง
10. เพิ่มนิติบุคคลที่มุมมองนี้ควรจะพร้อมใช้งาน 

    > [!NOTE]
    > โปรดระวังลักษณะการทำงานต่อไปนี้ หากคุณเผยแพร่มุมมองไปยังนิติบุคคลเฉพาะ แต่คุณไม่เผยแพร่มุมมองเป็นมุมมองเริ่มต้น:
    >
    > - หากเปิดคุณลักษณะ **มุมมองที่บันทึกไว้** พื้นฐาน ตัวเลือกมุมมองของผู้ใช้ของหน้าในเริ่มแรกจะแสดงเฉพาะมุมมองของนิติบุคคลที่ระบุเท่านั้น อย่างไรก็ตาม หลังจากที่มีการโหลดมุมมองเป็นครั้งแรก จะมีตัวเลือกมุมมองสำหรับหน้าดังกล่าวเสมอ โดยไม่คำนึงถึงนิติบุคคล
    > - ถ้าเปิดคุณลักษณะ **นิติบุคคลที่ปรับปรุงแล้วของมุมมองที่บันทึกไว้** ตัวเลือกมุมมองจะแสดงมุมมองที่สำหรับนิติบุคคลที่ระบุเท่านั้น

11. เลือก **เผยแพร่**

โปรดทราบว่าในบางสภาพแวดล้อม อาจใช้เวลาสักครู่ (จนถึงหนึ่งชั่วโมง) ก่อนที่ผู้ใช้จะเห็นมุมมองที่เผยแพร่

## <a name="modifying-a-published-view"></a>การปรับเปลี่ยนมุมมองที่เผยแพร่

หลังจากที่คุณเผยแพร่มุมมองแล้ว คุณอาจพบว่าคุณต้องการเปลี่ยนมุมมอง แม้ว่าคุณจะไม่สามารถทำการเปลี่ยนแปลงที่เริ่มใช้งานจริงไปยังมุมมองที่เผยแพร่ได้ เนื่องจากมุมมองเหล่านี้ถูกล็อคไว้เพื่อแก้ไขสำหรับผู้ใช้ทั้งหมด (ซึ่งรวมถึงผู้เผยแพร่) คุณจะสามารถเผยแพร่มุมมองเพื่อทำการปรับปรุงได้

ถ้าการเปลี่ยนแปลงที่คุณต้องการทำไปยังมุมมองที่เผยแพร่ เกี่ยวข้องเฉพาะกับพารามิเตอร์การเผยแพร่เท่านั้น (ชื่อและคำอธิบายของมุมมอง หรือบทบาทความปลอดภัยที่มีการเผยแพร่มุมมอง) ให้ทำตามขั้นตอนต่อไปนี้

1. สลับไปยังมุมมองที่เผยแพร่สำหรับพารามิเตอร์ที่คุณต้องการปรับปรุง 
2. บนเมนูแบบหล่นลงของตัวเลือกมุมมอง เลือก **เผยแพร่อีกครั้ง** ถ้าคุณกำลังใช้รุ่น10.0.12 หรือก่อนหน้านี้ คุณต้องเลือก **เผยแพร่** จากนั้น **ใช่** เพื่ออัปเดตมุมมองที่มีอยู่
3. ปรับปรุงชื่อ คำอธิบาย บทบาทความปลอดภัย และนิติบุคคลสำหรับมุมมอง 
4. เลือก **เผยแพร่** ถ้าคุณเลือกมุมมองที่เผยแพร่นี้ไว้ในครั้งแรกเป็นมุมมองเริ่มต้น มุมมองนี้จะเป็นมุมมองเริ่มต้นสำหรับผู้ใช้อีกครั้ง หลังจากที่คุณเผยแพร่อีกครั้ง 

ถ้าการเปลี่ยนแปลงไปยังมุมมองที่เผยแพร่เกี่ยวข้องกับการแก้ไขการกำหนดเป็นแบบส่วนบุคคล หรือตัวกรองที่เชื่อมโยงกับมุมมอง ให้ทำตามขั้นตอนต่อไปนี้:

1. โหลดมุมมองที่เผยแพร่ที่คุณต้องการเปลี่ยนแปลง 
2. ทำการเปลี่ยนแปลงที่จำเป็นสำหรับแบบร่างเฉพาะที่
3. บนเมนูแบบหล่นลงของตัวเลือกมุมมอง เลือก **เผยแพร่อีกครั้ง**
4. เลือก **ใช่** เพื่อระบุว่าคุณต้องการเผยแพร่มุมมองร่วมกับการเปลี่ยนแปลงที่ยังไม่ได้บันทึกไว้ 
5. ปรับเปลี่ยนพารามิเตอร์การเผยแพร่ใดๆ ที่จำเป็นต้องมีการปรับปรุง แล้วเลือก **เผยแพร่** 

## <a name="managing-published-views"></a>การจัดการมุมมองที่เผยแพร่

เช่นเดียวกับการจัดการมุมมองส่วนบุคคล กล่องโต้ตอบ **จัดการมุมมองของฉัน** ทำให้ผู้ใช้มีความสามารถในการบำรุงรักษาพื้นฐานของสิทธิ์ในการเผยแพร่สำหรับมุมมองที่เผยแพร่ของหน้านั้น (นอกเหนือจากมุมมองส่วนตัวของพวกเขาเอง) เมื่อต้องการเปิดหน้านี้ ให้เลือกชื่อมุมมองเพื่อเปิดเมนูแบบหล่นลงของตัวเลือกมุมมอง เลือก **เพิ่มเติม** แล้วเลือก **จัดการมุมมองของฉัน**

แม้ว่าผู้ใช้ทุกคนมีแท็บ **มุมมองของฉัน** ซึ่งแสดงมุมมองส่วนบุคคลของพวกเขา ผู้ใช้ที่มีสิทธิ์ในการเผยแพร่จะมีแท็บ **มุมมององค์กร** ซึ่งแสดงมุมมองที่เผยแพร่แล้วและยังไม่ได้เผยแพร่ทั้งหมดสำหรับหน้านั้นอีกด้วย เนื่องจากผู้ใช้หลายรายอาจมีมุมมองการเผยแพร่ จึงจำเป็นที่คุณต้องจัดการกับรายการทั้งหมดของมุมมองที่เผยแพร่ แม้ว่าคุณจะไม่ใช่ผู้ใช้ที่เผยแพร่มุมมองนั้น

สำหรับรายการของมุมมองที่เผยแพร่ทั้งหมดสำหรับหน้า ชุดของการดำเนินการต่อไปนี้จะพร้อมใช้งาน 

- **เผยแพร่อีกครั้ง** – ใช้การดำเนินการ **เผยแพร่อีกครั้ง** เพื่อเผยแพร่มุมมองอีกครั้ง หลังจากเผยแพร่พารามิเตอร์ (ชื่อ คำอธิบาย บทบาทความปลอดภัย หรือนิติบุคคล) ถูกเปลี่ยนแปลง
- **เผยแพร่** – ใช้การดำเนินการ **เผยแพร่** เพื่อเผยแพร่มุมมองที่ไม่ได้เผยแพร่ในปัจจุบัน 
- **ยกเลิกการเผยแพร่** – ใช้การดำเนินการ **ยกเลิกการเผยแพร่** เพื่อให้มุมมองไม่มีผลบังคับใช้ มุมมองนี้จะยังคงมีอยู่ในระบบ แต่ผู้ใช้จะไม่เห็นในตัวเลือกมุมมองจนกว่าจะมีการเผยแพร่มุมมองอีกครั้ง
- **บันทึกเป็นส่วนบุคคล** – ใช้การดำเนินการ **บันทึกเป็นส่วนบุคคล** เพื่อสร้างสำเนาร่างส่วนบุคคลของมุมมองที่เผยแพร่ ความสามารถนี้สามารถช่วยให้คุณเข้าใจเนื้อหาของมุมมองที่ไม่ได้เผยแพร่ไปยังคุณ หรือที่ยังไม่ได้เผยแพร่ นอกจากนี้ คุณยังสามารถใช้เพื่อแก้ไขและเผยแพร่มุมมองอีกครั้งได้อีกด้วย
- **ลบ** – ใช้การดำเนินการ **ลบ** เพื่อลบมุมมองที่เผยแพร่หรือยังไม่ได้เผยแพร่อย่างถาวร การดำเนินการนี้จะลบมุมมองสำหรับผู้ใช้ทั้งหมดในระบบด้วย การลบมุมมองที่เผยแพร่จะมีผลบังคับใช้หลังจากปุ่ม **บันทึก** ถูกเลือกแล้ว หลังจากลบมุมมองแล้ว จะไม่สามารถกู้คืนได้ 

## <a name="managing-views-globally"></a>การจัดการมุมมองทั่วโลก

ถึงแม้ว่าความสามารถในการจัดการบางอย่างจะถูกแสดงทุกหน้า ตามที่ระบุไว้ในบทความนี้ **ผู้ดูแลระบบ** และ **ผู้ดูแลมุมมองที่บันทึกไว้** สามารถจัดการมุมมองแบบองค์รวมได้มากขึ้นสำหรับระบบผ่านหน้า **การตั้งค่าส่วนบุคคล** โดยเฉพาะอย่างยิ่ง หน้านี้มีส่วนและความสามารถดังต่อไปนี้: 

- **มุมมองที่เผยแพร่** – ส่วนนี้แสดงรายการมุมมองทั้งหมดที่ถูกเผยแพร่สำหรับองค์กรของคุณ จากที่นี่ คุณสามารถเผยแพร่มุมมองอีกครั้ง หลังจากที่คุณปรับปรุงบทบาทความปลอดภัยหรือนิติบุคคลที่ดูเป้าหมาย คุณยังสามารถเผยแพร่ ลบ หรือยกเลิกเผยแพร่มุมมองได้ คุณสามารถใช้การดำเนินการ **บันทึกเป็นส่วนบุคคล** เพื่อสร้างสำเนาส่วนบุคคลของมุมมอง เพื่อให้คุณสามารถอัปเดตมุมมองหรือได้รับความเข้าใจที่ดีขึ้นของเนื้อหา 
- **มุมมองที่ไม่ได้เผยแพร่** – ส่วนนี้จะแสดงรายการมุมมององค์กรทั้งหมดในระบบของคุณที่ยังไม่ได้เผยแพร่ในขณะนี้ มุมมองเหล่านี้ส่วนใหญ่จะเข้าสู่ระบบโดยผ่านความสามารถในการนำเข้า คุณสามารถเผยแพร่ ส่งออก หรือลบมุมมองเหล่านี้ได้ การดำเนินการ **เผยแพร่ด่วน** ที่ถูกเพิ่มในรุ่น 10.0.12 ช่วยให้มุมมองหลายมุมมองจากส่วนนี้ถูกเผยแพร่ในการดำเนินการหนึ่งรายการ โดยใช้บทบาทความปลอดภัยและการตั้งค่าคอนฟิกนิติบุคคลที่มีอยู่ คุณสามารถใช้การดำเนินการ **บันทึกเป็นส่วนบุคคล** เพื่อสร้างสำเนาส่วนบุคคลของมุมมองเหล่านี้ เพื่อให้คุณสามารถได้รับความเข้าใจที่ดีขึ้นในเนื้อหา
- **มุมมองส่วนบุคคล** – ส่วนนี้แสดงรายการมุมมองทั้งหมดที่ถูกสร้างขึ้นโดยผู้ใช้ในระบบ จากที่นี่ คุณสามารถเผยแพร่มุมมองส่วนบุคคลไปยังองค์กร หรือคัดลอกมุมมองเหล่านี้อย่างน้อยหนึ่งมุมมองให้กับผู้ใช้คนอื่นๆ ได้ นอกจากนี้ คุณยังสามารถส่งออกหรือลบมุมมองเหล่านี้ได้ตามต้องการ
- **การตั้งค่าผู้ใช้** – เลือกผู้ใช้ที่จะดู หรือปรับความสามารถของผู้ใช้ในการใช้การตั้งค่าส่วนบุคคลอย่างใดอย่างหนึ่งสำหรับทั้งระบบหรือสำหรับหน้าที่เฉพาะเจาะจงที่ผู้ใช้ได้เข้าเยี่ยมชม คุณสามารถดูและโต้ตอบกับการตั้งค่าส่วนบุคคลของผู้ใช้ในระบบได้ นอกจากนี้ คุณยังสามารถการตั้งค่าส่วนบุคคลทั้งหมดสำหรับผู้ใช้คนนั้น หรือรีเซ็ตคำบรรยายคุณลักษณะสำหรับผู้ใช้ หากคำบรรยายคุณลักษณะถูกรีเซ็ต หน้าต่างป๊อปอัปใดๆ ซึ่งแนะนำคุณลักษณะใหม่ และที่ผู้ใช้ยกเลิกก่อนหน้านี้ จะปรากฏขึ้นอีกครั้งในครั้งถัดไปที่ผู้ใช้พบคุณลักษณะเหล่านั้น
- **การตั้งค่าระบบ** – คุณสามารถปิดใช้งานการตั้งค่าส่วนบุคคลแบบชั่วคราวสำหรับผู้ใช้ทั้งหมดในระบบ ในกรณีนี้ ไม่มีการใช้การตั้งค่าส่วนบุคคลสำหรับผู้ใช้ใดๆ และหน้าทั้งหมดจะถูกรีเซ็ตเป็นสถานะเริ่มต้น ถ้าคุณเปิดใช้งานการตั้งค่าส่วนบุคคลอีกครั้งในภายหลัง การตั้งค่าส่วนบุคคลทั้งหมดจะถูกนำไปใช้อีกครั้ง คุณยังสามารถลบการทำให้เป็นแบบส่วนบุคคลอย่างถาวรสำหรับผู้ใช้ทั้งหมดในระบบได้อีกด้วย ไม่สามารถกู้คืนการตั้งค่าส่วนบุคคลที่ถูกลบได้ ดังนั้น ก่อนที่คุณจะดำเนินการงานนี้ ตรวจสอบให้แน่ใจว่าได้ส่งออกการทำให้เป็นแบบส่วนบุคคลใดๆ ที่คุณอาจต้องการในภายหลัง

ผู้ใช้ที่สามารถเข้าถึงหน้า **การตั้งค่าส่วนบุคคล** ยังสามารถนำเข้ามุมมองส่วนตัวหรือองค์กรได้โดยใช้ปุ่ม **นำเข้ามุมมอง** ในบานหน้าต่างการดำเนินการ สำหรับมุมมององค์กร คุณสามารถเลือก **เผยแพร่ทันที** เพื่อให้มุมมองพร้อมใช้งานแก่ผู้ใช้โดยไม่มีการเผยแพร่ที่ชัดแจ้งเพิ่มเติม

## <a name="known-issues"></a>ปัญหาที่ทราบ

สำหรับรายการของปัญหาที่ทราบเกี่ยวกับมุมมองที่บันทึกไว้ โปรดดูที่ [การสร้างฟอร์มที่ใช้มุมมองที่บันทึกไว้อย่างสมบูรณ์](../../dev-itpro/user-interface/understanding-saved-views.md)

## <a name="frequently-asked-questions"></a>คำถามที่ถามบ่อย

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>ฉันจะเปิดใช้งานมุมมองที่บันทึกไว้ในสภาพแวดล้อมของฉันได้อย่างไร?

> [!NOTE]
> คุณลักษณะ **มุมมองที่บันทึก** กำหนดให้เปิดใช้งานระบบการตั้งค่าส่วนบุคคลในแอปการเงินและการดำเนินงาน ถ้าการตั้งค่าส่วนบุคคลถูกปิดสำหรับสภาพแวดล้อมทั้งหมด จะมีการปิดใช้งานมุมมอง ถึงแม้ว่าคุณจะทำตามขั้นตอนด้านล่าง 

คุณสามารถเปิดและปิดคุณลักษณะ **มุมมองที่บันทึกไว้** ได้ผ่านการจัดการคุณลักษณะในสภาพแวดล้อมใดๆ หลังจากที่เปิดแล้ว มุมมองที่บันทึกไว้จะเปิดใช้งานในรอบเวลาของผู้ใช้ในเวลาต่อมาทั้งหมด

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>เกิดอะไรขึ้นกับการตั้งค่าส่วนบุคคลที่มีอยู่ เมื่อเปิดใช้งานมุมมอง? 

เมื่อเปิดใช้งานมุมมอง การตั้งค่าส่วนบุคคลใดๆ ที่มีอยู่สำหรับผู้ใช้และฟอร์มจะถูกบันทึกลงในมุมมองใหม่ซึ่งเรียกว่า **มุมมองของฉัน** ซึ่งถูกตั้งค่าเป็นมุมมองเริ่มต้นโดยอัตโนมัติ การทำเช่นนี้มีไว้เพื่อให้แน่ใจว่ามีประสบการณ์ของผู้ใช้ที่สอดคล้องกันก่อนและหลังจากที่เปิดใช้งานมุมมอง ยกเว้นตัวเลือกมุมมองที่ปรากฏบนฟอร์ม

### <a name="what-pages-support-views"></a>หน้าใดสนับสนุนมุมมอง? 

มุมมองพร้อมใช้งานเป็นส่วนมาก แต่ไม่ใช่ทุกหน้า โดยเฉพาะ มุมมองที่พร้อมใช้งานในขณะนี้บนหน้าแบบเต็มหน้าจอ ยกเว้นแดชบอร์ด ดูการสนับสนุนของพื้นที่ทำงานจะพร้อมใช้งานผ่านทางคุณลักษณะ **การสนับสนุนมุมมองที่บันทึกไว้สำหรับพื้นที่ทำงาน** หน้าแบบไม่เต็มหน้าจอส่วนใหญ่ ซึ่งรวมถึงกล่องโต้ตอบ กล่องโต้ตอบแบบหล่นลง การค้นหา และการแสดงตัวอย่างขั้นสูง ยังไม่สนับสนุนมุมมองในขณะนี้ ดูการสนับสนุนของกล่องโต้ตอบจะพร้อมใช้งานผ่านทางคุณลักษณะ **การสนับสนุนมุมมองที่บันทึกไว้สำหรับกล่องโต้ตอบ**

### <a name="who-is-allowed-to-publish-views"></a>ใครได้รับอนุญาตให้เผยแพร่มุมมอง?

เฉพาะผู้ดูแลระบบและผู้ใช้ที่ได้รับการกำหนดให้กับบทบาท **ผู้ดูแลมุมมองที่บันทึกไว้** มีสิทธิ์ในการเผยแพร่มุมมองเท่านั้น 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>เพราะเหตุใดฉันจึงไม่สามารถบันทึกตัวกรองที่มีมุมมองนี้ได้? 

มีเหตุผลบางประการที่ตัวกรองอาจไม่ปรากฏขึ้นเพื่อบันทึกพร้อมกับมุมมอง: 

- หน้านี้อาจไม่สนับสนุนการบันทึกตัวกรอง เนื่องจากเป็นส่วนหนึ่งของข้อกำหนดมุมมอง โปรดทราบว่ามีเฉพาะหน้าที่มีตัวเลือกมุมมองที่มีขนาดใหญ่เท่านั้น ที่อนุญาตให้มีการกำหนดเป็นแบบส่วนบุคคลและการปรับเปลี่ยนการสอบถามที่จะบันทึกเป็นมุมมอง ให้ดูส่วน **การสลับมุมมอง** สำหรับข้อมูลเพิ่มเติม 
- หน้าที่อยู่ในคำถามอาจไม่สามารถสนับสนุนมุมมองได้อย่างถูกต้อง เนื่องจากอาจละเว้นการสอบถามมุมมองทั้งหมด หรืออาจทำงานบนตารางชั่วคราวที่มีข้อมูลไม่สม่ำเสมอ 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>ฉันจะดูข้อมูลใดเมื่อฉันไปที่หน้า

สำหรับหน้าที่มีตัวค้นหามุมมองเล็กๆ (เฉพาะบุคคลเท่านั้นที่สามารถบันทึกไปยังมุมมอง) คุณจะเห็นข้อมูลเดียวกันกับที่คุณมีอยู่เสมอเมื่อคุณไปที่หน้า 

สำหรับหน้าที่มีตัวแบ่งมุมมองที่มีขนาดใหญ่ (ทั้งการตั้งค่าส่วนบุคคลและการสอบถามสามารถบันทึกไปยังมุมมอง) คุณจะเห็นข้อมูลโดยทั่วไปที่เชื่อมโยงกับการสอบถามที่เชื่อมโยงกับมุมมองเริ่มต้นของคุณ มีสองข้อยกเว้นหลัก:

- ถ้าคุณนำทางไปยังหน้าจากไทล์ การสอบถามของไทล์จะดำเนินการโดยไม่คำนึงถึงการสอบถามที่เชื่อมโยงกับมุมมองเริ่มต้น ถ้าคุณสร้างไทล์ดังกล่าวหลังจากที่เปิดใช้งานมุมมองแล้ว การเลือกไทล์จะเปิดหน้าที่มีมุมมองที่เกี่ยวข้องกับไทล์นั้น
- ถ้าคุณนำทางไปยังหน้าและจุดเข้าใช้งานนั้นมีการสอบถาม การสอบถามดั้งเดิมจะดำเนินการแทนการสอบถามของมุมมองเริ่มต้นในครั้งแรก คุณควรจะได้รับการแจ้งเตือนเมื่อเหตุการณ์เกิดขึ้นโดยข้อความที่ให้ข้อมูล เมื่อกำลังโหลดมุมมอง นอกจากนี้ คุณยังสามารถยืนยันได้โดยสลับไปที่มุมมองนี้ หลังจากที่โหลดหน้า เนื่องจากรายการนั้นควรอนุญาตให้การสอบถามมุมมองสามารถดำเนินการโดยไม่คำนึง

### <a name="why-is-a-view-that-was-published-for-a-specific-legal-entity-visible-in-all-legal-entities"></a>เพราะเหตุใดมุมมองที่เผยแพร่เพื่อนิติบุคคลหนึ่งๆ จึงมองเห็นได้ในนิติบุคคลทั้งหมด

หากคุณเผยแพร่มุมมองไปยังนิติบุคคลเฉพาะ แต่คุณไม่เผยแพร่มุมมองเป็นมุมมองเริ่มต้น ลักษณะการทำงานต่อไปนี้เกิดขึ้น:

- หากเปิดคุณลักษณะ **มุมมองที่บันทึกไว้** พื้นฐาน ตัวเลือกมุมมองของผู้ใช้ของหน้าในเริ่มแรกจะแสดงเฉพาะมุมมองของนิติบุคคลที่ระบุเท่านั้น อย่างไรก็ตาม หลังจากที่มีการโหลดมุมมองเป็นครั้งแรก จะมีตัวเลือกมุมมองสำหรับหน้าดังกล่าวเสมอ โดยไม่คำนึงถึงนิติบุคคล ลักษณะการทำงานนี้จะเกิดขึ้นเนื่องจากผู้ใช้จะได้รับสําเนาส่วนบุคคลของตนเองในมุมมองที่เผยแพร่เมื่อโหลดแล้ว และมุมมองส่วนตัวเป็นมุมมองส่วนกลาง
- ถ้าเปิดคุณลักษณะ **นิติบุคคลที่ปรับปรุงแล้วของมุมมองที่บันทึกไว้** ตัวเลือกมุมมองจะแสดงมุมมองที่สำหรับนิติบุคคลที่ระบุเท่านั้น ลักษณะการทำงานนี้จะเกิดขึ้นเนื่องจากคุณลักษณะเปิดใช้งานมุมมอง (รวมถึงมุมมองส่วนตัว) ที่จะเชื่อมโยงกับนิติบุคคลเฉพาะ

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

