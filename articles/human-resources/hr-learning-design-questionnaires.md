---
title: สร้างแบบสอบถาม
description: บทความนี้อธิบายถึงกระบวนการสร้างแบบสอบถาม
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection, HcmLearningWorkspace
audience: Application User
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: ef14dfe35e6cffc5ae2351045141d99b2fb53c16
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899656"
---
# <a name="create-questionnaires"></a>สร้างแบบสอบถาม


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

บทความนี้อธิบายถึงกระบวนการสร้างแบบสอบถาม ขั้นตอนแรกคือการ ออกแบบแบบสอบถาม เมื่อคุณออกแบบแบบสอบถาม คุณไม่เพียงเขียนคำถามและคำตอบ แต่ยังสร้างโครงสร้างที่คำตอบที่สามารถบันทึก และจัดทำตารางคำตอบได้ 

การออกแบบแบบสอบถามอย่างรอบคอบสามารถช่วยเพิ่มคุณภาพของข้อมูลที่คุณรวบรวมได้ โดยการออกแบบอย่างระมัดระวัง คุณสามารถเลือกตัวเลือกที่เหมาะสมในเวลาที่เหมาะสมได้ดีขึ้นสำหรับแบบสอบถาม เนื้อหาต่อไปนี้จะช่วยให้คุณวางแผนแบบสอบถามที่มีประสิทธิภาพได้:

-   กำหนดวัตถุประสงค์ของแบบสอบถามให้ชัดเจน เพื่อช่วยในการรับประกันว่าคำถามสนับสนุนวัตถุประสงค์
-   กำหนดบุคคลหรือกลุ่มบุคคลที่คุณควรกรอกข้อมูลแบบสอบถาม
-   เขียนคำถามที่จะปรากฏในแบบสอบถาม และรวมตัวเลือกคำตอบ ถ้าเกี่ยวข้อง
-   ตรวจสอบให้แน่ใจว่าแบบสอบถามเรียงกันตามกันทางตรรกะ เพื่อให้ยังคงเกี่ยวข้องกับผู้ตอบแบบสอบถาม
-   จัดเรียงคำถามและคำตอบในลำดับที่ควรจะแสดงต่อผู้ตอบแบบสอบถาม
-   ตัดสินใจว่า ควรประเมินผลลัพธ์อย่างไร ถ้าเกี่ยวข้อง
-   ตัดสินใจว่าคุณต้องใช้ลักษณะการทำงานเพิ่มเติมหรือไม่ ตัวอย่างเช่น กำหนดว่าผลลัพธ์ควรจะจำแนกอย่างไร ขีดจำกัดเวลาจำเป็นหรือไม่ หรือว่าคำถามทั้งหมดจะบังคับตอบหรือไม่

ระยะออกแบบรวมถึงงานสี่ประเภทที่คุณต้องดำเนินการตามลำดับนี้:

1.  ตั้งค่าข้อกำหนดเบื้องต้นตามความจำเป็น
2.  ตั้งค่ากลุ่มคำตอบและคำตอบ ถ้าเกี่ยวข้อง
3.  สร้างคำถามและความเชื่อมโยงกับกลุ่มคำตอบ
4.  ตั้งค่าแบบสอบถามเอง และแนบคำถามลงไป

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น
ข้อกำหนดเบื้องต้นบางอย่างต้องอยู่ในตำแหน่งก่อนที่คุณจะสามารถสร้างแบบสอบถาม คำตอบ และคำถามได้ อย่างไรก็ตาม ข้อกำหนดเบื้องต้นทั้งหมดไม่จำเป็นต้องใช้สำหรับงานทั้งหมดโดยสมบูรณ์

### <a name="required"></a>ต้องระบุ

| ข้อกำหนดเบื้องต้น        | คำอธิบาย                |
|---------------------|----------------------------|
| ชนิดของแบบสอบถาม | จัดประเภทแบบสอบถาม |
| ชนิดของคำถาม      | จัดประเภทแบบคำถาม      |

### <a name="optional"></a>ไม่จำเป็นต้องระบุ

| ข้อกำหนดเบื้องต้น             | คำอธิบาย                                                    |
|--------------------------|----------------------------------------------------------------|
| พารามิเตอร์แบบสอบถาม | แก้ไขการควบคุมพื้นฐานและการตั้งค่าเริ่มต้นสำหรับแบบสอบถาม |

### <a name="questionnaire-types"></a>ชนิดของแบบสอบถาม

เมื่อคุณสร้างแบบสอบถาม จำเป็นต้องกำหนด **ชนิดของแบบสอบถาม** ด้วย **ชนิดของแบบสอบถาม** จะช่วยให้คุณจัดการและจัดประเภทแบบสอบถามได้ง่ายขึ้น ใช้ชนิดแบบสอบถามเพื่อจัดประเภทแบบสอบถาม และแยกแยะออกจากกัน ตัวอย่างเช่น ถ้าคุณมีแบบสอบถามเป็นจำนวนมากให้เลือก คุณสามารถกรองข้อมูลแบบสอบถามโดยใช้ชนิดในแบบฟอร์มเพื่อช่วยให้สามารถค้นหาแบบสอบถามที่ระบุได้ง่ายขึ้น ต่อไปนี้เป็นตัวอย่างของชนิดแบบสอบถาม:

-   การพัฒนาทรัพยากรบุคคล
-   การสำรวจลูกค้า
-   กระบวนการตรวจทาน

### <a name="question-types"></a>ชนิดของคำถาม

เมื่อคุณสร้างคำถาม จำเป็นต้องกำหนด **ชนิดของคำถาม** ด้วย 

ใช้ **ชนิดของคำถาม** เพื่อจัดประเภทคำถามสำหรับการรายงาน **ชนิดของคำถาม** ยังช่วยให้สามารถค้นหาคำถามได้ง่ายขึ้น เนื่องจากคุณสามารถใช้ชนิดเป็นตัวกรองในหน้า **คำถาม** ได้ ต่อไปนี้เป็นตัวอย่างของชนิดคำถาม:

-   ทรัพยากรบุคคล
-   การบริหารธุรกิจ
-   การประเมินผลหลักสูตร

### <a name="questionnaire-parameters"></a>พารามิเตอร์แบบสอบถาม

พารามิเตอร์แบบสอบถามนั้นไม่จำเป็นต้องระบุ คุณอาจไม่ใช้ ขึ้นอยู่กับความต้องการของบริษัทของคุณ 

พารามิเตอร์แบบสอบถามกำหนดตัวตน รหัสลำดับหมายเลข และชนิดการอ้างอิงของแบบสอบถาม เมื่อองค์กรกระจายแบบสอบถาม ตัวเลือกเพื่ออนุญาตให้ผู้ตอบไม่ระบุชื่ออาจต้องนำมาพิจารณา 

รหัสลำดับหมายเลขจะใช้ในการจัดระเบียบคำถามและคำตอบ ตามรหัสลำดับหมายเลขเหล่านี้ ค่าจะกำหนดโดยอัตโนมัติให้กับสินค้า 

คุณควรกำหนดพารามิเตอร์ทั้งหมดก่อนที่คุณจะเริ่มสร้างข้อมูลของคุณ คุณสามารถปรับเปลี่ยนการตั้งค่าพารามิเตอร์แบบสอบถามได้ตลอดเวลา

## <a name="questionnaire-components"></a>ส่วนประกอบของแบบสอบถาม
แบบสอบถามประกอบด้วยสามองค์ประกอบหลัก: กลุ่มคำตอบที่ประกอบด้วยคำตอบสำหรับคำถามเลือกตอบหลายตัวเลือก คำถาม และแบบสอบถามเอง คุณสามารถเลือกจัดกลุ่มคำถามในแบบสอบถามเป็นกลุ่มผลลัพธ์ได้ กลุ่มผลคะแนนช่วยให้คุณสามารถจัดประเภทคำถาม และให้การวิเคราะห์เพิ่มเติมในแบบสอบถาม 

[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### <a name="answer-groups-and-answers"></a>กลุ่มคำตอบและคำตอบ

ผู้ตอบแบบสอบถามสามารถตอบคำถามได้สองวิธี ขึ้นอยู่กับลักษณะของคำถาม ดังนี้

-   คำถามปลายเปิดไม่จำเป็นต้องตอบรับในรูปแบบที่กำหนดไว้ ผู้ตอบสามารถพิมพ์คำตอบเป็นข้อความ หมายเลข วัน หรือเวลา โดยปกติ คำถามเหล่านี้กำหนดให้ผู้ตอบให้ข้อมูลแบบอัตนัยในคำตอบ เช่น ความคิดเห็น การประเมินค่า หรือการประเมิน
-   คำถามปลายปิดจำเป็นต้องให้ผู้ตอบเลือกคำตอบในรายการคำตอบที่ถูกต้องที่เป็นไปได้

เพื่อสร้างรายการของคำตอบที่เป็นไปได้สำหรับคำถามปลายปิด คุณสามารถสร้างคำตอบในแบบหน้า **กลุ่มคำตอบ** ได้ 

กลุ่มคำตอบและคำตอบเป็นองค์ประกอบที่สร้างเนื้อหาหลักของข้อมูลที่สร้างคำถามขึ้นมา หลังจากที่คุณสร้างกลุ่มคำตอบ คุณสามารถเชื่อมโยงกลุ่มคำตอบกับคำถามในฟิลด์ **กลุ่มคำตอบ** ในหน้า **คำถาม** ได้ 

**กลุ่มคำตอบ** หนึ่ง ๆ จะสามารถใช้กับคำถามได้มากกว่าหนึ่งข้อบนแบบสอบถามชุดเดียวกัน และยังสามารถใช้ได้กับแบบสอบถามมากกว่าหนึ่งชุดด้วย 

> [!NOTE]
> ถ้าคุณปรับเปลี่ยนข้อความคำตอบในกลุ่มคำตอบที่ได้ใช้ในแบบสอบถามที่เสร็จสมบูรณ์แล้ว จะประเมินข้อมูลได้ยาก และผลลัพธ์ของแบบสอบถามอาจไม่สามารถใช้ได้อีกต่อไป ถ้าคุณต้องเปลี่ยนกลุ่มคำตอบ พิจารณาสร้างกลุ่มคำตอบใหม่แทนการเปลี่ยนแปลงกลุ่มคำตอบที่มีอยู่ คุณไม่สามารถลบกลุ่มคำตอบที่แนบกับคำถามหรือคำตอบ หรือได้ตอบไปแล้วได้

### <a name="questions"></a>คำถาม

แบบสอบถามต้องมีคำถาม คำถามสามารถเป็นได้ทั้งแบบปลายเปิดหรือปลายปิด

-   การตอบรับของคำถามแบบปลายเปิดไม่ได้ควบคุม และผู้ตอบสามารถพิมพ์คำตอบของตนได้
-   คำถามปลายปิดต้องมีรายการตัวเลือกของคำตอบที่กำหนดไว้ล่วงหน้า และสามารถจัดโครงสร้างคำถามเพื่อให้ผู้ตอบเลือกคำตอบหลายรายการได้ คำถามควรออกแบบมาเพื่อให้ได้รับข้อมูลที่เฉพาะเจาะจงจากผู้ตอบคำถาม และต้องเชื่อมโยงกับกลุ่มคำตอบที่มีตัวเลือกคำตอบสำหรับแต่ละคำถามปลายปิด 

    > [!NOTE]
    > ก่อนที่คุณจะสามารถตั้งค่าคำถามปลายปิด คุณต้องสร้างกลุ่มคำตอบและคำตอบก่อน

คำถามที่สามารถจัดเรียงเป็นลำดับชั้นของคำถามแบบมีเงื่อนไข เพื่อให้คำถามรองขึ้นอยู่กับคำตอบที่ผู้ตอบเลือกสำหรับคำถามก่อนหน้านี้ คุณสามารถเขียนคำถามก่อน และจากนั้น จัดเรียงตามลำดับชั้นของคำถามในภายหลัง

## <a name="setting-up-questionnaires"></a>การตั้งค่าชนิดแบบสอบถาม

> [!NOTE]
> ก่อนที่คุณจะสามารถตั้งค่าแบบสอบถาม คุณต้องตั้งค่าคำตอบ คำถาม และข้อกำหนดเบื้องต้นก่อน 

สำหรับแต่ละแบบสอบถาม คุณสามารถระบุข้อมูลต่อไปนี้:

-   เวลารวมหรือขีดจำกัดเวลาสำหรับการตอบคำถามบังคับ
-   คำถามทั้งหมดเป็นคำถามบังคับหรือไม่
-   คำนวณคะแนนในแบบสอบถามหรือไม่
-   วิธีการจัดประเภทผลลัพธ์
-   แบบสอบถามจะพร้อมใช้งานสำหรับชุดของผู้ตอบที่จำกัดหรือไม่
-   ให้แสดงเทมเพลตแบบฟอร์มเป็นพื้นหลังของแบบสอบถามแต่ละหน้าหรือไม่
-   หมายเหตุเพิ่มเติมจำเป็นในการชี้แจงวัตถุประสงค์ของแบบสอบถามสำหรับผู้ตอบหรือไม่
-   คุณต้องการแสดงคำถามตามลำดับที่กำหนด หรือเลือกคำถามจากกลุ่มโดยสุ่ม
-   ระบุว่าจะถามคำถามหากได้รับการตอบสนองที่ระบุสำหรับคำตอบก่อนหน้านี้เท่านั้นหรือไม่

### <a name="set-up-a-questionnaire"></a>ตั้งค่าแบบสอบถาม

หน้าหลักที่คุณใช้ในการตั้งค่าแบบสอบถามคือหน้า **แบบสอบถาม** เมื่อต้องการตั้งค่าแบบสอบถาม ดำเนินการงานต่อไปนี้ให้เสร็จสมบูรณ์ตามลำดับ:

1.  สร้างแบบสอบถาม
2.  ทำตามหนึ่งในขั้นตอนเหล่านี้เพื่อแนบคำถามกับแบบสอบถาม:
    -   ถ้าคุณกำลังใช้กลุ่มผลลัพธ์ คุณสามารถแนบคำถามกับแบบสอบถามโดยใช้กลุ่มผลลัพธ์ อันดับแรก ตั้งค่ากลุ่มผลคะแนนสำหรับแบบสอบถาม และเพิ่มคำถามไปยังกลุ่มผลคะแนน
    -   ถ้าคุณไม่ได้กำลังใช้กลุ่มผลลัพธ์ คุณสามารถแนบคำถามกับแบบสอบถามได้โดยตรง

3.  การตั้งค่าลำดับชั้นของคำถามแบบมีเงื่อนไข หากจำเป็น
4.  ทดสอบแบบสอบถาม

ในหน้า **แบบสอบถาม** คลิก **ตรวจสอบ** เพื่อทดสอบว่าแบบสอบถามรวบรวมไว้อย่างถูกต้อง อย่างไรก็ตาม ควรกรอกแบบสอบถามให้เสร็จสมบูรณ์ และทดสอบด้วยตนเองก่อนที่จะกระจายแบบสอบถาม

### <a name="modify-a-questionnaire"></a>การแก้ไขแบบสอบถาม

คุณสามารถดำเนินการงานต่อไปนี้ให้เสร็จสมบูรณ์ในหน้า **แบบสอบถาม** ได้:

-   การแก้ไขข้อมูลในแบบสอบถาม เช่น กลุ่มผลคะแนนและคำถาม
-   การลบและเพิ่มคำถาม
-   ทำการเปลี่ยนแปลงในกลุ่มผลคะแนนและหมายเลขลำดับ 

> [!CAUTION]
> ต้องระวังเมื่อคุณเปลี่ยนแบบสอบถามที่มีการตอบไปแล้ว  การเปลี่ยนแปลงสามารถทำให้สถิติมีความถูกต้องแม่นยำลดลงได้ ซึ่งอาจส่งผลให้พื้นฐานการประเมินไม่ดีลดความแม่นยำงของสถิติ ให้ลองพิจารณาถึงการสร้างคำถามใหม่ แทนการเปลี่ยนแปลงคำถามเดิมที่มีการตอบไปแล้ว

ในแบบสอบถาม คุณไม่สามารถลบชนิดของคำถามต่อไปนี้:

-   คำถามที่แนบกับแบบสอบถาม
-   คำถามที่มีการตอบไปแล้ว และปรากฏในกล่องโต้ตอบ **คำตอบ** แล้ว

### <a name="result-groups"></a>กลุ่มผลคะแนน

**กลุ่มผลลัพธ์** จะไม่จำเป็นต้องระบุเมื่อคุณแนบคำถามกับแบบสอบถาม 

กลุ่มผลคะแนนจะใช้ในการคำนวณคะแนน และจัดประเภทผลลัพธ์ของแบบสอบถาม ถ้าคุณใช้กลุ่มผลคะแนน คุณสามารถดำเนินการงานต่อไปนี้:

-   ประเมินผลลัพธ์แบบสอบถาม โดยใช้สถิติคะแนน
-   ประเมินของคะแนนของผู้ตอบแบบสอบถามสำหรับกลุ่มผลคะแนนแต่ละกลุ่มที่คุณตั้งค่า
-   สร้างสถิติสำหรับกลุ่มผลคะแนนแต่ละกลุ่ม เพื่อช่วยคุณในการวิเคราะห์ผลคะแนน
-   พิมพ์รายงานที่แสดงผลลัพธ์สำหรับแต่ละกลุ่มผลคะแนน และคะแนน/ข้อความที่ไม่จำเป็นต้องระบุ ซึ่งจะเป็นไปตามคะแนนที่ทำได้ในแต่ละกลุ่มผลคะแนน

> [!NOTE]
> ก่อนที่คุณจะสามารถตั้งค่าบัญชีเจ้าหนี้ คุณต้องดำเนินขั้นตอนต่อไปนี้ให้ครบถ้วน:

-   ตั้งค่าคำถามปลายปิด สำหรับคำถามปลายปิด ชนิดของข้อมูลป้อนเข้าในหน้า **คำถาม** ต้องเป็น **กล่องกาเครื่องหมาย** **ปุ่มทางเลือก** หรือ **กล่องคำสั่งผสม**
-   กำหนดคะแนนสำหรับคำตอบในกลุ่มคำตอบที่กำหนดให้กับแต่ละคำถาม
-   ตั้งค่าแบบสอบถาม

เมื่อต้องการแนบคำถามกับแบบสอบถามโดยใช้กลุ่มผลคะแนน ให้ตั้งค่ากลุ่มผลคะแนนสำหรับแบบสอบถาม แล้วจึงเพิ่มคำถามให้กับกลุ่มผลคะแนน ถ้าคุณไม่ใช้กลุ่มผลลัพธ์ คุณสามารถแนบคำถามกับแบบสอบถามได้โดยตรง 

คุณสามารถตั้งค่ากลุ่มผลลัพธ์หลายกลุ่ม เพื่อประเมินคะแนนที่ผู้ตอบแบบสอบถามได้รับคะแนนในแต่ละประเภท หลังจากแบบสอบถามเสร็จสมบูรณ์ คุณสามารถดูคะแนนที่ทำได้ของแต่ละกลุ่มผลคะแนน 

> [!TIP]
> เมื่อต้องการประเมินแบบสอบถามโดยใช้คะแนน แต่ไม่ได้แยกประเภท คุณสามารถเพิ่มคำถามทั้งหมดให้กับกลุ่มผลคะแนนเดียวกัน 

สำหรับแต่ละกลุ่มผลคะแนน คุณสามารถตั้งค่าข้อความที่ผู้ตอบได้รับหลังจากที่สมบูรณ์แบบสอบถามตามคะแนนที่ทำได้ ข้อความที่แสดงอาจแตกต่างกัน ขึ้นอยู่กับคะแนนที่ผู้ตอบได้รับในกลุ่มผลคะแนน การใช้ข้อความตามผลคะแนน คุณต้องกำหนดช่วงคะแนนและคำอธิบายของแต่ละช่วง เมื่อผู้ตอบได้รับคะแนนในช่วงคะแนนที่ระบุ ข้อความเฉพาะสำหรับช่วงคะแนนดังกล่าวจะรวมอยู่ในรายงานผลลัพธ์ 

เนื่องจากกลุ่มผลคะแนนเกี่ยวข้องกับคะแนนที่เชื่อมโยงกับชุดของคำถามที่เจาะจงในแบบสอบถาม คุณสามารถใช้กลุ่มผลคะแนนที่เฉพาะเจาะจงกลุ่มเดียวเท่านั้นสำหรับหนึ่งแบบสอบถาม

#### <a name="example-pointstexts-for-result-group-3"></a>ตัวอย่าง: คะแนน/ข้อความสำหรับกลุ่มผลคะแนน 3

คุณกำลังใช้แบบสอบถามสำหรับการทดสอบความเป็นผู้นำ ซึ่งมี 15 คำถามในสามประเภท คุณสร้างกลุ่มผลคะแนนสามกลุ่ม และเพิ่มคำถามห้าคำถามไปยังแต่ละกลุ่มผลคะแนน จากนั้น รวมคะแนนในสามกลุ่มดังนี้ กลุ่มผลคะแนนสามกลุ่มมีดังนี้:

-   ความสามารถด้านความคิดสร้างสรรค์
-   ความสามารถด้านความเป็นผู้นำ
-   ความสามารถด้านเทคนิค

เมื่อต้องการใช้ข้อความตามผลคะแนน ให้ตั้งค่าช่วงข้อความสำหรับกลุ่มผลคะแนนแต่ละกลุ่ม แต่ละคำถามจะได้รับสองคะแนน ดังนั้น รวมคะแนนสูงสุดในแต่ละกลุ่มผลลัพธ์คือ 10 

ตารางต่อไปนี้แสดงข้อความตามจุดที่คุณกำหนดสำหรับกลุ่มผลคะแนน "ความสามารถด้านความเป็นผู้นำ"

| ช่วงคะแนน | ข้อความ                                       |
|----------------|--------------------------------------------|
| 1 ถึง 3         | คุณมีความสามารถด้านความเป็นผู้นำปานกลาง     |
| 4 ถึง 7         | คุณมีความสามารถด้านความเป็นผู้นำดี        |
| 8 ถึง 10        | คุณมีความสามารถด้านความเป็นผู้นำโดดเด่น |

คุณสามารถตั้งค่าช่วงคะแนนและข้อความสำหรับแต่ละกลุ่มผลลัพธ์ในแบบสอบถาม มีการแสดงข้อความที่ตรงกับคะแนนของผู้ตอบแต่ละราย สำหรับแต่ละกลุ่มผลคะแนน 

> [!NOTE]
> คุณสามารถเปลี่ยนช่วงคะแนนและข้อความได้ อย่างไรก็ตาม ถ้าแบบสอบถามเสร็จสมบูรณ์แล้ว การเปลี่ยนแปลงอาจก่อให้เกิดความแตกต่างระหว่างรายงานผลลัพธ์ก่อนหน้านี้ และรายงานผลลัพธ์ใหม่ได้

### <a name="conditional-question-hierarchies"></a>ลำดับชั้นของคำถามแบบมีเงื่อนไข

ไม่จำเป็นต้องระบุลำดับชั้นของคำถามแบบมีเงื่อนไขเมื่อคุณตั้งค่าแบบสอบถาม 

> [!NOTE]
> ก่อนที่คุณจะสามารถตั้งค่าลำดับชั้นของคำถามแบบมีเงื่อนไข คำถามที่มีการกำหนดกลุ่มคำตอบต้องแนบอยู่กับแบบสอบถามแล้ว 

เมื่อต้องการคำถามแบบมีเงื่อนไขเพื่อสร้าลำดับชั้นของคำถามแบบมีเงื่อนไข คุณสามารถกำหนดลำดับชั้นในการแสดงคำถาม ขึ้นอยู่กับการเลือกตอบแต่ละคำถามของผู้ตอบ โดยการกำหนดลำดับของคำถามตามคำตอบของผู้ตอบ คุณสามารถปรับเปลี่ยนแบบสอบถาม ตามที่ผู้ตอบตอบได้

#### <a name="examples"></a>ตัวอย่างเช่น

นิติบุคคลเสนอทั้งสินค้าและบริการแก่ลูกค้า ตามที่เกิดขึ้นในกรณีดังกล่าวโดยทั่วไป ลูกค้าบางรายซื้อเฉพาะสินค้า บางรายการซื้อเพียงบริการ และบางรายการซื้อทั้งสินค้าและบริการ ดังนั้น เมื่อนิติบุคคลกระจายแบบสำรวจความพึงพอใจของลูกค้า จะใช้เป็นโครงสร้างแบบมีเงื่อนไขกับแบบสอบถาม เพื่อให้ลูกค้าที่ซื้อบริการเท่านั้นไม่จำเป็นต้องตอบคำถามเกี่ยวกับสินค้า 

อีกทางหนึ่งคือ คุณตั้งค่าแบบสอบถาม หากผู้ตอบเลือกคำตอบ A สำหรับคำถามข้อ 1 คำถาม 2 จะเป็นอันดับถัดไปในลำดับคำถาม อย่างไรก็ตาม ถ้าผู้ตอบเลือกคำตอบ B สำหรับคำถามข้อ 1 คำถาม 5 จะเป็นอันดับถัดไป

[!INCLUDE[footer-include](../includes/footer-banner.md)]
