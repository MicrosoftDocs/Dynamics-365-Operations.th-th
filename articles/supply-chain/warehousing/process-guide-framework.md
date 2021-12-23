---
title: กรอบงานคู่มือกระบวนการ
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับกรอบงานคู่มือกระบวนการสำหรับนักพัฒนาที่ขยายกระบวนการคลังสินค้าบนอุปกรณ์เคลื่อนที่ของเราใน X++
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 6882c979ad9b37eb4f95a04259b6ac0f0a0edcdc
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902057"
---
# <a name="process-guide-framework"></a>กรอบงานคู่มือกระบวนการ

[!include [banner](../includes/banner.md)]

หัวข้อนี้ให้ข้อมูลเกี่ยวกับกรอบงานคู่มือกระบวนการสำหรับนักพัฒนาที่ขยายกระบวนการคลังสินค้าบนอุปกรณ์เคลื่อนที่ใน X++ กระบวนการคลังสินค้าบนอุปกรณ์เคลื่อนที่สามารถขยายได้ เนื่องจากกระบวนการแบ่งออกเป็นขั้นตอนขนาดเล็ก ตรรกะทางธุรกิจและการสร้างอินเทอร์เฟสผู้ใช้ของแต่ละขั้นตอนถูกแยกออกเป็นแต่ละคลาส ซึ่งช่วยให้ขยายได้

## <a name="overview-of-the-existing-design"></a>ภาพรวมของการออกแบบที่มีอยู่

โฟลว์การดำเนินการคลังสินค้าบนอุปกรณ์เคลื่อนที่แสดงผ่านปลายทางบริการแบบกำหนดเองหนึ่งๆ คำขอมาถึงจากแอปบนมือถือในรูปแบบของสตริง XML ซึ่งมีข้อมูลเมตาของอินเทอร์เฟสผู้ใช้ที่แสดงอยู่ในแอปบนมือถือ และค่าที่ป้อนโดยผู้ใช้ด้วย

เมื่อได้รับคำขอ ขั้นตอนแรกคือการดีซีเรียลไลซ์ XML นี้ คลาส **WHSMobileAppServiceXMLTranslator** จะแปลง XML เป็นคอนเทนเนอร์ ซึ่งมีข้อมูลการควบคุมทั้งสองรายการ และข้อมูลของรอบเวลาด้วย

ต่อไปนี้ ข้อมูลในคอนเทนเนอร์จะใช้ในการอนุมานว่ากระบวนการคลังสินค้าใดที่ผู้ใช้ใช้อยู่ หรือกำลังจะเริ่มต้น (ซึ่งแสดงโดย การแจงนับ **WHSWorkExecuteMode**) และจากนี้จะสร้างอินสแตนซ์ของคลาสสืบทอดของ **WHSWorkExecuteDisplay** วิธีการ **displayform()** ถูกเรียกใช้ ซึ่งจะดำเนินการต่อไปนี้:

-   ประมวลผลข้อมูลจากผู้ใช้ (ถูกมอบหมายให้กับคลาส **WHSRFControlData** แต่กระบวนการบางอย่างจะใช้ตรรกะเฉพาะโดยการแทนที่วิธีการ **processControl()**)

-   ดำเนินการตรรกะทางธุรกิจ

-   เพิ่มขั้นตอน

-   สร้างคอนเทนเนอร์ที่แสดงถึงอินเทอร์เฟสผู้ใช้ใหม่ (โดยทั่วไปคือในวิธีการ **สร้าง... ()**)

จากนั้นคอนเทนเนอร์จะถูกส่งกลับไปยังผู้แปล ซึ่งหลังจากนั้นจะทำให้ XML เป็นอนุกรม และส่งกลับเป็นการตอบสนองไปยังอุปกรณ์เคลื่อนที่

แผนภาพลำดับต่อไปนี้จะแสดงภาพรวมของโฟลว์การดำเนินการ โปรดทราบว่าแผนภาพเป็นภาพรวมแบบเค้าร่างมากกว่าและไม่ใช่การแสดงรหัสจริงแบบ 1:1

![ภาพรวมแบบเค้าร่างของกระบวนการ](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>เหตุผลสำหรับการออกแบบใหม่

การออกแบบข้างต้นมีกรอบงานที่ธรรมดามากในการสร้างกระบวนการที่ใช้ในโฟลว์แบบเคลื่อนที่ อย่างไรก็ตาม ตามที่อธิบายไว้ข้างต้น วิธีการ **displayform()** จะมีหลายความรับผิดชอบ ซึ่งจะมอบหมายวิธีการและคลาสอื่นๆ ให้กับวิธีการและคลาสอื่นๆ แต่เมื่อขาดความรับผิดชอบของคลาสรูปธรรม จะได้รับมอบหมายในลักษณะที่ไม่สอดคล้องกันระหว่างคลาสต่างๆ นอกจากนี้ เมื่อจํานวนของสถานการณ์ที่ได้รับการสนับสนุนเพิ่มขึ้น บางคลาสเหล่านั้นอาจซับซ้อนขึ้นได้ หากต้องการทำให้น่าสนใจมากขึ้น บางคลาส/วิธีการเหล่านั้นจะถูกแทนที่และมีการใช้ใหม่ในโหมดหลายโหมด ผลลัพธ์ที่ได้คือวิธีการที่ยาวนานมากและมีความซับซ้อนของไซโคลมาติกสูง สิ่งเหล่านี้ก่อให้เกิดปัญหาการบํารุงรักษาในอดีต การแก้ไขบักในวิธีการเหล่านี้เสี่ยงและมีแนวโน้มที่จะเกิดการถดถอย
ตัวอย่างเช่น วิธีการ **processWorkLine()** ในคลาส **WhsWorkExecuteDisplay** จะมาจากหลายกระบวนการ (โดยทั่วไปคือที่ใดๆ ที่มีการดำเนินงาน)

หากต้องการทำให้ขยายได้ ตัวเลือกใดตัวเลือกหนึ่งคือการแบ่งวิธีการ **displayForm** เป็นวิธีการที่เล็กลงและให้จุดความสามารถในการเพิ่มฟังก์ชัน อย่างไรก็ตาม เนื่องจากเมทริกซ์สถานการณ์ จะเป็นเรื่องท้าทายสำหรับคู่ค้าในการเขียนส่วนขยายและตรวจสอบความถูกต้องต่อการถดถอย ไม่เพียงแต่นั้น เนื่องจากการขาดการกระจายความรับผิดชอบอย่างเป็นระบบที่ระบุไว้ข้างต้น รหัสจึงขยายเพิ่มขึ้นโดยไม่สามารถคาดการณ์ได้อย่างต่อเนื่อง ก่อให้เกิดความท้าทายในการขยายคุณภาพของการสร้าง

ดังนั้น การออกแบบใหม่เป็นตัวเลือกที่ยั่งยืน โดยมีเป้าหมายเพื่อให้มีคลาสที่กําหนดอย่างชัดเจนและมีความรับผิดชอบที่ไม่ขึ้นต่อกัน คลาสควรมีหนึ่งความรับผิดชอบ เหตุผลหนึ่งเพื่อเปลี่ยนแปลง และเหตุผลหนึ่งเพื่อที่จะขยายออกไป

## <a name="design-overview"></a>ออกแบบภาพรวม

ในกรอบงานที่ออกแบบใหม่ กลยุทธ์หลักจะแก้ไขปัญหาสองหลักการ คือ แบ่งโฟลว์การดำเนินการออกเป็นส่วนประกอบต่างๆ พร้อมความรับผิดชอบที่กําหนดไว้อย่างชัดเจน และมีจุดขยายที่กําหนดไว้อย่างชัดเจนในแต่ละส่วนประกอบ

ชื่อกรอบงานใหม่คือ "ProcessGuide" สิ่งนี้เป็นเพราะเป้าหมายของคลาสเหล่านี้คือ เพื่อแนะแนวผู้ใช้ผ่านกระบวนการทางธุรกิจ (ต่างจากไคลเอนต์สมบูรณ์ ซึ่งเป็นประสบการณ์ที่ใช้ฟอร์มที่ผู้ใช้มีความยืดหยุ่นมากขึ้นในการโต้ตอบกับข้อมูล หรือเพื่อที่ผู้ใช้จะปฏิบัติงาน)

> [!NOTE]
> รายละเอียดที่ไม่ควรระบุหนึ่งรายการคือการละเว้นข้อความนําหน้า "WHS" โดยเจตนา ในขณะที่กระบวนการบนอุปกรณ์เคลื่อนที่ถูกแนะขายสำหรับคลังสินค้าในตอนเริ่มต้น ในเวลาต่อมา จะมีขอบเขตที่ดีกว่าเพื่อสนับสนุนกระบวนการผลิตและกระบวนการการจัดการสินค้าคงคลังต่างๆ ซึ่งอาจส่งผลให้ข้อมูลอ้างอิงคลังสินค้าถูกแยกออกในชื่อของกรอบงาน

เมื่อต้องการระบุส่วนประกอบ ขั้นตอนแรกคือดูกระบวนการ เริ่มการผลิต (คลาส **WhsWorkExecuteDisplayProdStart**) ต่อไปนี้เป็นเค้าร่างของกระบวนการ

![รูปภาพของกระบวนการตามเค้าร่าง](media/production-start-process-schematic.png)

เมื่อดูที่โฟลว์การควบคุม ส่วนประกอบต่อไปนี้เป็นข้อมูลที่ต้องการ:

-   ตัวควบคุมเพื่อที่จะรวมผ่านกระบวนการทางธุรกิจทั้งหมด
-   ขั้นตอนที่รับผิดชอบการดำเนินการของขั้นตอนในกระบวนการ
-   ตัวประมวลผลข้อมูลเพื่อประมวลผลข้อมูลในขั้นตอน
-   ตัวสร้างหน้าที่รับผิดชอบการสร้างอินเทอร์เฟสผู้ใช้ให้กับขั้นตอนหนึ่งๆ
-   ตัวแทนนําทางที่รับผิดชอบการเปลี่ยนขั้นตอน
-   คลาสที่รับผิดชอบการดำเนินการกระบวนการทางธุรกิจ

ในแผนภาพโฟลว์ของกระบวนการข้างต้น ถ้าคุณเริ่มต้นขั้นตอนที่ 1 และเริ่มต้นการประมวลผลข้อมูลจากขั้นตอนก่อนหน้า แล้วจบด้วยการสร้าง UI ข้อมูลจะยังคงได้รับการประมวลผลในขั้นตอนถัดไป ซึ่งนี่ทำให้เกิดข้อต่อแน่นระหว่างขั้นตอนที่ต่อเนื่องกัน ดังนั้น เค้าร่างใหม่ระดับสูงของเราจะมีลักษณะเป็นดังนี้:

![รูปภาพของกระบวนการเค้าร่างระดับสูง](media/high-level-schematic.png)

ต่อไปนี้เป็นส่วนประกอบหลักในกระบวนการที่ออกแบบใหม่:

-   **ProcessGuideController** - คลาสนี้จะประสานการดำเนินการโดยรวมของกระบวนการทางธุรกิจ ขั้นตอนนี้จะกําหนดโรงงานที่สร้างอินสแตนซ์ขั้นตอนและตัวแทนการนําทาง ซึ่งประกอบเป็นกาดำเนินการกระบวนการในภายหลัง รวมทั้งตรรกะการล้างข้อมูลเพื่อการยกเลิกหรือออกจากกระบวนการ

-   **ProcessGuideStep** - คลาสนี้แสดงถึงขั้นตอนเดียวในกระบวนการทางธุรกิจ คลาสนี้จะประกอบด้วยการนิยามที่สร้างอินสแตนซ์โปรแกรมสร้างหน้า การดำเนินการ และตัวประมวลผลข้อมูล และรับผิดชอบการเรียกข้อมูลเหล่านั้นตามลำดับที่ถูกต้อง

-   **ProcessGuideNavigationAgent** - คลาสนี้รับผิดชอบการนําทางระหว่างขั้นตอนต่างๆ เมื่อขั้นตอนเสร็จสมบูรณ์แล้ว ตัวแทนการนําทางจะรับผิดชอบในการระบุขั้นตอนถัดไปและส่งผ่านพารามิเตอร์ใดๆ ที่ขั้นตอนก่อนหน้าอาจต้องการสื่อสารกับขั้นตอนถัดไป

-   **ProcessGuidePageBuilder** - คลาสนี้รับผิดชอบการเริ่มต้นอินเทอร์เฟสผู้ใช้

-   **ProcessGuideAction** - คลาสนี้แสดงถึงการดำเนินการ ที่แสดงเป็นปุ่มต่อผู้ใช้

-   **ProcessGuideDataProcessor** - คลาสนี้รับผิดชอบการประมวลผลข้อมูลที่ป้อนโดยผู้ใช้ในฟิลด์

## <a name="execution-flow"></a>โฟลว์การดำเนินการ

จุดเริ่มต้นโฟลว์การดำเนินการยังคงไม่เปลี่ยนแปลง ดังนั้น คำขอยังคงมาถึงที่ปลายทางเดียวกัน ตามด้วยการทำให้ XML เป็นแบบอนุกรมลงในคอนเทนเนอร์ จากนั้นคอนเทนเนอร์นี้จะถูกส่งผ่านไปยัง **getNextFormState()**

มีคลาสที่สําคัญสามประเภทที่จะบันทึก:

-  **ProcessGuideSessionStates** – มีข้อมูลสถานะของรอบเวลา – โหมด ผ่าน ตัวควบคุม และขั้นตอนที่ดำเนินการ และอื่นๆ

-  **ProcessGuidePage** – ซึ่งมีการแสดงข้อมูลเมตาของอินเทอร์เฟสผู้ใช้ที่มีชนิด

-  **ProcessGuideRequest** – ข้อมูลนี้มีสองรายการดังกล่าวเป็นสมาชิก และการแสดงคำขอที่ได้รับจากอุปกรณ์เคลื่อนที่ที่มีชนิด

คลาสเหล่านี้สร้างขึ้นโดยใช้ข้อมูลคอนเทนเนอร์ (ทั้งข้อมูลการควบคุมสถานะและที่ป้อนโดยผู้ใช้) วิธีการนี้จะให้วิธีที่ปลอดภัยในการเข้าถึงและจัดการค่าต่างๆ เมื่อเปรียบเทียบกับการเข้าถึงคอนเทนเนอร์ซ้ำในระหว่างกระบวนการ แล้วจึงให้ประโยชน์ทั้งในแง่ของความสามารถในการอ่านและประสิทธิภาพการทำงาน

ข้อมูลสถานะรอบเวลาใช้เพื่อสร้างอินสแตนซ์คลาส **ProcessGuideController** ที่ถูกต้อง เมื่อเริ่มต้นสร้างอินสแตนซ์ วิธีการ **createResponse()** ในคลาส **ProcessGuideController** จะถูกเรียกใช้ วิธีการนี้คือนจุดเข้าใช้งานไปยังตรรกะคู่มือกระบวนการ และหลังจากการดำเนินการ กลับมาพร้อมการตอบสนอง (ซึ่งแสดงอยู่ในคลาส **ProcessGuideResponse**) จากนั้นการตอบสนองจะถูกแปลงกลับไปยังคอนเทนเนอร์และส่งกลับไปยังตรรกะดั้งเดิม จากนั้นจะทำให้การตอบสนองนั้นเป็นแบบอนุกรมไปยัง XML และส่งการตอบสนองกลับไปยังอุปกรณ์เคลื่อนที่

จากนั้น ตัวควบคุมต้องค้นหาขั้นตอนถัดไปเพื่อดำเนินการ ถ้านี่เป็นจุดเริ่มต้นของกระบวนการใหม่ ตัวควบคุมจะเรียกใช้ **initialStep()** เพื่อไปยังขั้นตอนแรกในกระบวนการ หลังจากนั้น จะเรียกใช้วิธีการ **execute()** ใน **ProcessGuideStep** จากนั้น วิธีการนี้จะสร้างอินสแตนซ์คลาส **ProcessGuidePageBuilder** และเรียกใช้ **buildPage()** ซึ่งจะส่งคืนด้วยออบเจ็กต์ **ProcessGuidePage** ซึ่งเป็นการแสดงอินเทอร์เฟสผู้ใช้เสมือนที่จะนําเสนอต่อผู้ใช้ จากนั้น ขั้นตอนจะส่งผลลัพธ์กลับไปยังตัวควบคุม ซึ่งจะบันทึกสถานะรอบเวลาปัจจุบันแล้วส่งคืนผลลัพธ์กลับไปเป็น **getNextFormState()** ในรูปแบบของคลาส **ProcessGuideResponse** หลังจากนั้น การตอบสนองจะถูกแปลงกลับไปยังคอนเทนเนอร์ และทำให้ XML เป็นแบบอนุกรมและส่งการตอบสนองกลับไปยังอุปกรณ์เคลื่อนที่ในเวลาต่อมา

แผนภาพลำดับต่อไปนี้อธิบายโฟลว์การควบคุมนี้ โปรดทราบว่าโฟลว์การควบคุมนี้เป็นโฟลว์การควบคุมทั่วไป ซึ่งทำให้ง่ายขึ้นสำหรับการอธิบายการออกแบบ

![โฟลว์การควบคุมแบบง่าย](media/control-flow.png)

เมื่อผู้ใช้ใช้การดำเนินการในอุปกรณ์เคลื่อนที่โดยการคลิกปุ่ม (หรือสแกนค่า ซึ่งโดยทั่วไปจะทริกเกอร์การดำเนินการค่าเริ่มต้น) – คำขอจะมาถึงที่วิธีการ **createResponses()** ในคลาส **ProcessGuideController** ในกระบวนการผลิตเดียวกัน อย่างไรก็ตาม เวลานี้ตัวควบคุมจะทราบจากข้อมูลสถานะรอบเวลาที่ขั้นตอนที่ผู้ใช้อยู่ ดังนั้น จะสร้างอินสแตนซ์คลาส **ProcessGuideStep** ที่เหมาะสมและเรียกใช้วิธีการดำเนินการ **ProcessGuideStep** จะอ่านชื่อการดำเนินการที่เรียกโดยผู้ใช้ จากนั้นสร้างอินสแตนซ์คลาส **ProcessGuideAction** ที่เหมาะสมและเรียกใช้ **execute()**

คลาส **ProcessGuideAction** จะรับผิดชอบการดำเนินการเฉพาะ อย่างไรก็ตาม มีข้อยกเว้นที่ไม่อาจระบุสองข้อ

ข้อแรกคือคลาส **ProcessGuideOKAction** การดำเนินการนี้แสดงว่าผู้ใช้ต้องการยืนยันและดำเนินการต่อไปในกระบวนการ ด้วยเหตุนั้น – วิธีการนี้จะโทรกลับไปยังคลาส ProcessGuideStep จริงๆ ซึ่งหมายความว่าขั้นตอนจะเรียกใช้ **processData()** ใน **ProcessGuideDataProcessor** ขั้นตอนนี้ประมวลผลข้อมูลที่ผู้ใช้ป้อนไว้ แล้วอัปเดตสถานะของขั้นตอนและส่งผลลัพธ์กลับไปยังตัวควบคุม ทั้งนี้ขึ้นอยู่กับผลลัพธ์ของตัวประมวลผล ขั้นตอนนี้จะเรียกตัวสร้างหน้าเพื่อสร้างอินเทอร์เฟสผู้ใช้ที่เหมาะสม หรือตั้งค่าสถานะของขั้นตอนเป็นเสร็จสมบูรณ์ ซี่งจะสะท้อนให้เห็นในครึ่งบนของแผนภาพลำดับด้านล่างนี้

ข้อยกเว้นอีกอย่างคือการดําเนินการยกเลิก ที่ดําเนินการในคลาส **ProcessGuideCancelResetProcessAction** และ **ProcessGuideCancelExitProcessAction** การดําเนินการเหล่านี้แสดงถึงวัตถุประสงค์เพื่อยกเลิกกระบวนการ และกลับไปยังการเริ่มต้นกระบวนการหรือออกจากกระบวนการทั้งหมด คล้ายกับการดําเนินการ **ตกลง** การดำเนินการเหล่านี้ยังโทรกลับไปยังขั้นตอน ซึ่งจะส่งสัญญาณถึงวัตถุประสงค์ของ **ProcessGuideController** จากนั้นตัวควบคุมจะดําเนินการล้างข้อมูลตัวแปรสถานะที่จําเป็น และย้ายตัวควบคุมไปที่ขั้นตอนแรกในกระบวนการหรือยุติกระบวนการทั้งหมด

หลังจากขั้นตอนเสร็จสมบูรณ์แล้ว ถ้าตั้งค่าสถานะของขั้นตอนเป็น **เสร็จสมบูรณ์** ตัวควบคุมจะเริ่มต้น **ProcessGuideNavigationAgent** ซึ่งจะส่งคืนชื่อของขั้นตอนต่อไป จากนั้น ตัวควบคุมจะเริ่มต้นขั้นตอนนี้ในทันทีและเรียกวิธีการ **execute()** และวงจรจะดำเนินต่อไป โดยทั่วไปแล้ว ขั้นตอนใหม่จะเรียกใช้ **ProcessGuidePageBuilder** ที่สอดคล้องกันเพื่อสร้างอินเทอร์เฟสผู้ใช้เพื่อให้หน้าจอถัดไปนําเสนอต่อผู้ใช้ ซึ่งต่อมาถูกส่งกลับ โฟลว์นี้กล่าวถึงในครึ่งล่างของแผนภาพลำดับด้านล่างนี้

![แผนภาพลำดับ](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>การสร้างกระบวนการใหม่โดยใช้กรอบงาน ProcessGuide

วิธีที่ดีที่สุดในการอธิบายโฟลว์การควบคุมคือ โดยใช้ตัวอย่างที่มีอยู่ในโปรแกรมประยุกต์ – กระบวนการ เริ่มการผลิต

## <a name="overview-of-the-production-start-process"></a>ภาพรวมของกระบวนการเริ่มการผลิต

เริ่มต้นด้วยการทำความเข้าใจในโฟลว์ของกระบวนการ ในขั้นตอนแรก ผู้ใช้จะได้รับพร้อมต์สำหรับรหัสใบสั่งผลิต

![พร้อมต์สำหรับรหัสการผลิต](media/production-id-prompt.png)

เมื่อผู้ใช้ป้อนรหัสใบสั่งผลิต หมายเลขใบสั่งจะถูกตรวจสอบความถูกต้อง บางการตรวจสอบความถูกต้องที่จะรันจะขึ้นอยู่กับว่าใบสั่งอยู่ในคลังสินค้าเดียวกันกับที่ผู้ใช้ลงชื่อเข้าสู่ระบบหรือไม่ และสถานะของใบสั่ง หากการตรวจสอบความถูกต้องล้มเหลว ผู้ใช้จะได้รับแสดงข้อความข้อผิดพลาด ถ้าการตรวจสอบความถูกต้องเสร็จสิ้น ผู้ใช้จะได้รับแสดงรายละเอียดของใบสั่งผลิตและสินค้า

ผู้ใช้สามารถยกเลิกเพื่อกลับไปที่จุดเริ่มต้นของกระบวนการ หรือคลิก **ตกลง** เพื่อยืนยัน ในกรณีสุดท้าย ใบสั่งผลิตจะถูกตั้งเป็นสถานะ **เริ่มต้น** จะมีการลงรายการบัญชีสมุดรายวันที่ตรงกัน การควบคุมจะย้ายกลับไปยังขั้นตอนแรก และข้อความ "งานเสร็จสมบูรณ์" จะแสดงต่อผู้ใช้


## <a name="creating-the-controller"></a>การสร้างตัวควบคุม

ขั้นตอนแรกในการสร้างกระบวนการทางธุรกิจคือการสร้างคลาสตัวควบคุม ซึ่งขยายจากคลาสนามธรรม **ProcessGuideController** ซึ่งใช้ลักษณะการดําเนินการเริ่มต้นของตัวควบคุม ชื่อคลาสใหม่คือ **ProdProcessGuideProductionStartController** และตกแต่งด้วยค่า **WHSWorkExecuteMode** ของ **StartProdOrder** การเริ่มต้นที่ใช้ **SysExtension** เดียวกันซึ่งใช้ในคลาส **WHSWorkExecuteDisplay** จะถูกใช้ ซึ่งช่วยให้ตัวควบคุมสามารถเริ่มต้นเมื่อผู้ใช้ดำเนินการรายการเมนูในโหมดนี้

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> รูปแบบการตั้งชื่อของคลาสคือ **ตัวควบคุม\<FunctionalArea\>ProcessGuide\<Businessprocessname\>** นี่เป็นรูปแบบที่ใช้กับคลาสตัวควบคุมและเพื่อขยายไปยังคลาสอื่นๆ


## <a name="building-the-first-step"></a>การสร้างขั้นตอนแรก

ขั้นตอนถัดไป ในการกําหนดขั้นตอนแรก ให้คุณสร้างคลาส **ProdProcessGuidePromptProductionIdStep** โดยขยายจาก **ProcessGuideStep**

งานในการสร้างคลาสคือมอบหมายให้กับโรงงานขั้นตอน ซึ่งเรียกใช้โดยคลาสพื้นฐาน **ProcessGuideController** การใช้งานเริ่มต้นของโรงงานจะสร้างกระบวนการตามชื่อ ดังนั้น หากต้องการสร้าง **ProdProcessGuidePromptProductionIdStep** เป็นขั้นตอนแรกในตัวควบคุม คุณต้องปฏิบัติตามสองสิ่งต่อไปนี้:

-   ตกแต่งคลาส **ProdProcessGuidePromptProductionIdStep** ด้วยแอททริบิวต์ **ProcessGuideStepName**

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   ในคลาสตัวควบคุม ให้ใช้วิธีการที่เป็นนามธรรม **initialStepName()** เพื่อส่งคืนชื่อขั้นตอน

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> ค่าในแอททริบิวต์ **ProcessGuideStepName** ไม่ตรงกับชื่อคลาสตามที่แสดงข้างต้นทั้งหมด อย่างไรก็ตาม การใช้การดําเนินการนี้จะช่วยให้มีมาตรฐานและชนิดความปลอดภัยกับการอ้างอิงไขว้เมื่อใช้คลาส แนะนำการใช้แบบแผนการตั้งชื่อนี้
>
> การสร้างตาม **ProcessGuideStepName** ของขั้นตอนถูกใช้งานในคลาส **ProcessGuideStepDefaultFactory** ในกรณีที่ยากที่คุณต้องการใช้กลยุทธ์อื่นเพื่อสร้างขั้นตอน คุณต้องทำสิ่งต่อไปนี้:
> -   สร้างคลาสโรงงานใหม่ที่สืบทอดมาจาก **ProcessGuidStepAbstractFactory**
> -   หรือสร้างคลาสพารามิเตอร์ใหม่ที่ใช้อินเทอร์เฟส **ProcessGuideIStepCreationParameters** ที่มีพารามิเตอร์ที่โรงงานต้องการ
> -   ในคลาสตัวควบคุมของคุณ ให้แทนที่วิธีการ **stepFactory()** และ **stepCreationParameters()** เพื่อส่งคืนโรงงานและพารามิเตอร์ข้างบน

ขั้นตอนต่อไปคือการใช้งานฟังก์ชันของคลาส **ProdProcessGuidePromptProductionIdStep** คุณต้องใช้ตรรกะในการสร้างอินเทอร์เฟสผู้ใช้ ประมวลผลข้อมูลที่ป้อนโดยผู้ใช้ และกําหนดว่าขั้นตอนเสร็จสมบูรณ์เมื่อใด

### <a name="building-the-user-interface-for-the-first-step"></a>การสร้างอินเทอร์เฟสผู้ใช้ให้กับขั้นตอนแรก

อินเทอร์เฟสผู้ใช้มีการสร้างโดยใช้คลาสที่สืบทอดมาจากคลาสที่เป็นนามธรรม **ProcessGuidePageBuilder** สำหรับขั้นตอนนี้ ให้ตั้งชื่อคลาสเพื่อแสดงสิ่งที่ทำ – **ProdProcessGuidePromptProductionIdPageBuilder**

ระบบการสร้างของคลาสจะคล้ายกับวิธีการสร้างขั้นตอนจากตัวควบคุม 

-   ตกแต่งคลาส **ProdProcessGuidePromptProductionIdPageBuilder** ด้วยแอททริบิวต์ **ProcessGuidePageBuilderName**

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   ในคลาส **ProdProcessGuidePromptProductionIdStep** ให้ใช้วิธีการที่เป็นนามธรรม **pageBuilderName()** เพื่อส่งคืนชื่อนี้

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> เช่นเดียวกับโรงงานขั้นตอน ยังมีรูปแบบโรงงานที่เป็นนามธรรมที่ใช้กับโรงงานตัวสร้างหน้าอีกด้วย ดังนั้น ในกรณีที่ยากที่คุณต้องการใช้กลยุทธ์อื่นเพื่อสร้างตัวสร้างหน้า คุณสามารถทำสิ่งต่อไปนี้:
> - สร้างคลาสโรงงานใหม่ที่สืบทอดมาจาก **ProcessGuidePageBuilderAbstractFactory**
> - หรือสร้างคลาสพารามิเตอร์ใหม่ที่ใช้อินเทอร์เฟส **ProcessGuideIPageBuilderCreationParameters** ที่มีพารามิเตอร์ที่โรงงานต้องการ
> - ในคลาสขั้นตอนของคุณ ให้แทนที่วิธีการ **pageBuilderFactory()** และ **pageBuilderCreationParameters()** เพื่อส่งคืนโรงงานและพารามิเตอร์ข้างบน

ในการใช้อินเทอร์เฟสผู้ใช้ คุณต้องใช้หน้าที่มีกล่องข้อความหนึ่งเพื่อป้อนรหัสใบสั่งผลิต บวกด้วยปุ่ม **ตกลง** และปุ่ม **ยกเลิก** ปุ่ม **ยกเลิก** ควรออกจากกระบวนการ

ในการดําเนินการนี้ คุณต้องแทนที่วิธีการสองวิธีในคลาส **ProdProcessGuidePromptProductionIdPageBuilder**:

-   ใช้วิธีการ **addDataControls()** เพื่อเพิ่มกล่องข้อความ

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   ใช้วิธีการ **addActionControls()** เพื่อเพิ่มปุ่ม **ตกลง** และ **ยกเลิก**

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

สิ่งนี้จะเพิ่มตัวควบคุมข้อมูล ตามด้วยปุ่ม อย่างไรก็ตาม ถ้าคุณต้องการสร้างหน้าจอที่มีตัวควบคุมและปุ่มข้อมูลแยกกัน คุณสามารถแทนที่วิธีการ **addControls()** แทนเพื่อความยืดหยุ่น

สถานการณ์เพิ่มเติมที่ควรพิจารณาคือวิธีการสร้างหน้าอีกครั้งในกรณีที่การตรวจสอบความถูกต้องล้มเหลว ตัวอย่างเช่น ถ้าผู้ใช้ป้อนรหัสใบสั่งผลิตที่ไม่ถูกต้อง คลาสพื้นฐาน **ProcessGuidePageBuilder** จะใช้ลักษณะการทำงานเริ่มต้น ซึ่งสร้างอินเทอร์เฟสผู้ใช้ใหม่ ล้างข้อมูลค่าที่สแกน และเพิ่มตัวควบคุมข้อผิดพลาดที่มีข้อความแสดงข้อผิดพลาด เนื่องจากนี่เป็นลักษณะการทำงานเริ่มต้นที่คุณต้องการใช้ คุณจึงไม่ต้องการเพิ่มรหัสใดๆ ในการจัดการข้อผิดพลาด

> [!TIP]
> ถ้าคุณต้องการใช้ลักษณะการทำงาน UI แบบกำหนดเองสำหรับสถานการณ์ของข้อผิดพลาด คุณสามารถแทนที่ได้มากกว่าหนึ่งวิธีการ **rebuildFromRequestPage()**, **isErrorState()** และ **reuseRequestPageOnError()**

### <a name="processing-the-user-entered-data-in-the-first-step"></a>การประมวลผลข้อมูลที่ป้อนโดยผู้ใช้ในขั้นตอนแรก

การประมวลผลข้อมูลเสร็จสิ้นในคลาส **ProcessGuideDataProcessorDefault** ซึ่งเรียกใช้คลาส **WhsRfControlData** ดั้งเดิม ไม่ต้องมีการเปลี่ยนแปลงใดๆ กับลักษณะการทำงานเริ่มต้นนี้ และ **WhsRfControlData** มีตรรกะอยู่แล้วการตรวจสอบความถูกต้องของฟิลด์ **ProdId** ดังนั้นคุณจึงไม่จำเป็นต้องเขียนตรรกะใดๆ ในการจัดการกับฟิลด์นี้ ในกรณีที่ต้องใช้ส่วนขยายสำหรับตรรกะการตรวจสอบความถูกต้อง ให้พิจารณาใช้กลไกส่วนขยายที่ใช้ **WhsControl**

### <a name="determine-if-the-first-step-is-complete"></a>ระบุว่าขั้นตอนแรกเสร็จสมบูรณ์หรือไม่

เมื่อการตรวจสอบความถูกต้องเสร็จเรียบร้อยแล้ว ถึงเวลาที่จะทำเครื่องหมายขั้นตอนเป็นเสร็จสมบูรณ์ ขั้นตอนนี้ทำในคลาสพื้นฐาน อย่างไรก็ตาม คุณจึงต้องใช้เงื่อนไขเพื่อกำหนดการดําเนินการขั้นตอนให้เสร็จสมบูรณ์ วิธีการแทนที่ต่อไปนี้ดำเนินการนั้น

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>ขั้นตอนที่สอง: ดูรายละเอียดใบสั่งและยืนยัน

ในขั้นตอนที่สองในกระบวนการ ผู้ใช้จะได้รับแสดงหน้าจอที่มีรายละเอียดเกี่ยวกับใบสั่ง ผู้ใช้สามารถคลิกปุ่ม **ตกลง** เพื่อยืนยันการเริ่มต้นของใบสั่งผลิต หรือคลิก **ยกเลิก** เพื่อย้อนกลับไปยังจุดเริ่มต้นของกระบวนการ ตัวอย่างเช่น ตั้งชื่อขั้นตอน **ProdProcessGuideConfirmProductionOrderStep** และคลาสตัวสร้างหน้า **ProdProcessGuideConfirmProductionOrderPageBuilder**

คลาส ProdProcessGuideConfirmProductionOrderStep จะมีลักษณะดังต่อไปนี้

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

เนื่องจากผู้ใช้ไม่ได้ป้อนค่าใดๆ ที่นี่ คุณจึงไม่ต้องแทนที่วิธีการ **isComplete()** ขั้นตอนจะเสร็จสมบูรณ์เมื่อผู้ใช้คลิก **ตกลง**

คลาสตัวสร้างหน้าจะแทนที่วิธีการ **addDataControls()** เพื่อเพิ่มป้ายชื่อสามป้าย ป้ายชื่อแรกแสดงรหัสใบสั่งผลิต ป้ายที่สองมีข้อมูลสินค้า (เช่น รหัสสินค้า มิติ หรือข้อความอธิบาย) และป้ายที่สามมีปริมาณและหน่วยวัด

**addActionControls()** ถูกแทนที่เพื่อเพิ่มปุ่ม 2 – ปุ่ม **ตกลง** และปุ่ม **ยกเลิก** เพื่อยกเลิกกระบวนการ และกลับไปยังจุดเริ่มต้นของกระบวนการ

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> คุณสามารถค้นหารหัสต้นทางเดียวกันได้กับวิธีการ X++ ในหัวข้อนี้โดยใช้ Application Explorer กรองข้อมูลในชื่อคลาส แล้วคลิกขวาที่ชื่อคลาสและเลือก **ดูรหัส**

### <a name="step-3-start-the-production-order"></a>ขั้นตอนที่ 3: เริ่มใบสั่งผลิต

ขั้นตอนที่สามคือที่ที่มีการดำเนินการตรรกะทางธุรกิจของการเริ่มต้นใบสั่งผลิต ขั้นตอนนี้แตกต่างจากขั้นตอนก่อนหน้านี้บ้าง ขั้นตอนนี้ไม่มีอินเทอร์เฟสผู้ใช้ ขั้นตอนนี้จะเรียกใช้แบบเงียบเมื่อผู้ใช้คลิก **ตกลง** ในขั้นตอนก่อนหน้านี้

คลาสที่เป็นนามธรรม **ProcessGuideStepWithoutPrompt** จะใช้งานลักษณะการดําเนินการเริ่มต้นสำหรับขั้นตอนดังกล่าว ขั้นตอนปัจจุบัน ดังนั้น ควรขยายคลาส **ProcessGuideStepWithoutPrompt** และแทนที่วิธีการ **doExecute()**

ตัวอย่างรหัสต่อไปนี้แสดงคลาสและการใช้งานวิธีการ **doExecute()** วิธีการนี้จะดึงข้อมูลรหัสใบสั่งและรหัสผู้ใช้จากสถานะรอบเวลาและเรียกวิธีการในการเริ่มต้นใบสั่งผลิตนี้

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

ในกรณีของข้อยกเว้น ตรรกะการจัดการข้อยกเว้นของกรอบงานช่วยให้แน่ใจว่ากระบวนการกลับสู่ขั้นตอนก่อนหน้านี้

> [!NOTE]
> การเรียกใช้ **addProcessCompletionMessage()** จะเพิ่มข้อความ "งานเสร็จสมบูรณ์" ลงในพารามิเตอร์การนําทาง ขั้นตอนต่อไป (สมมติว่ามีอินเทอร์เฟสผู้ใช้) จะแสดงข้อความนี้ คลาสพื้นฐานจะจัดการตรรกะนี้ และไม่ต้องเพิ่มรหัสเฉพาะที่คลาสกระบวนการเพื่อให้เกิดลักษณะการทำงานดังกล่าว


### <a name="building-the-navigation-through-the-steps"></a>การสร้างการนําทางผ่านขั้นตอน

คลาสพื้นฐาน **ProcessGuideController** จะเริ่มต้นคลาส **ProcessGuideNavigationAgentDefault** ซึ่งอาศัยเส้นทางการนําทางที่กําหนดไว้ล่วงหน้า ซึ่งเป็นแผนที่ง่ายของขั้นตอนต้นทางและปลายทาง สำหรับสถานการณ์เริ่มการผลิต เนื่องจากไม่มีสาขาแบบมีเงื่อนไข การใช้งานนี้จะพอเพียง ดังนั้น คุณจึงต้องแทนที่วิธีการ **initializeNavigationRoute()** เพื่อกําหนดเส้นทางการนําทางเท่านั้น

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

มีกระบวนการซึ่งจะมีสาขาแบบมีเงื่อนไข (ตามการดำเนินการของผู้ใช้ หรือเงื่อนไขอื่น) กระบวนการดังกล่าวต้องทำดังต่อไปนี้:

-   ใช้ตัวแทนนําทางเฉพาะที่สืบทอดมาจากคลาส **ProcessGuideNavigationAgent**

-   นําโรงงานของตัวแทนการนําทางเฉพาะที่สืบทอดมาจากคลาส **ProcessGuideNavigationAgentAbstractFactory** ที่มีตรรกะเพื่อเริ่มต้นตัวแทนการนําทางที่ถูกต้องตามขั้นตอน สถานะรอบเวลา การดําเนินการของผู้ใช้ หรือตรรกะอื่นๆ ปัจจุบัน

-   หรือแทนที่ **navigationAgentCreationParameters()** ในคลาสตัวควบคุมเพื่อส่งผ่านพารามิเตอร์ที่เหมาะสม

-   แทนที่ **navigationAgentFactory()** ในตัวควบคุมเพื่อเริ่มโรงงานของตัวแทนการนําทางที่สร้างขึ้นข้างต้นในทันที

### <a name="action-classes"></a>คลาสการดำเนินการ

คลาสการดำเนินการแสดงถึงการดำเนินการของผู้ใช้ ดังนั้นตัวอย่างนี้จะใช้การดำเนินการ **ตกลง** เพื่อแสดงวิธีการสร้างการดำเนินการ

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

คลาสต้องใช้วิธีการนามธรรม 2 วิธี:

-   **label()** ซึ่งจะส่งคืนป้ายชื่อที่จะแสดงในตัวควบคุมปุ่มที่ผูกกับการดำเนินการนี้

-   **doExecute()** ซึ่งปฏิบัติการดำเนินการ ตามที่ระบุไว้ก่อนหน้านี้ ปุ่ม **ตกลง** จะเพียงแต่กลับไปยังขั้นตอนเท่านั้น อย่างไรก็ตาม การดำเนินการอื่นๆ อาจมีตรรกะที่ซับซ้อนมากขึ้นที่นี่

เริ่มการดำเนินการโดยใช้กรอบงาน **SysExtension** ตามแอททริบิวต์ **ProcessGuideActionName** คล้ายกับการเริ่มต้นของตัวสร้างหน้า คลาสขั้นตอนจะใช้โรงงานการดําเนินการเริ่มต้น และคุณสามารถแทนที่สิ่งต่อไปนี้ได้ ตัวสร้างหน้าจะเพิ่มตัวควบคุมปุ่มตามนี้

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

ในการทำเช่นนั้น จะขอให้ขั้นตอนสร้างคลาสการดำเนินการให้กับชื่อที่ส่งผ่านและผูกการดำเนินการนั้นกับปุ่ม

### <a name="summary"></a>สรุป

เพื่อสรุปทุกอย่างที่ได้อธิบายในหัวข้อนี้ ต่อไปนี้เป็นสรุปโดยครอบคลุมของรหัสที่ทางกระบวนการต้องการ:

1.  **ProdProcessGuideProductionStartController**

    1.  แทนที่ **initialStepName()** เพื่อให้มีชื่อของขั้นตอนแรก
    2.  แทนที่ **initializeNavigationRoute()** เพื่อสร้างแผนผังการนําทาง

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  แทนที่ **isComplete()** เพื่อระบุเวลาที่ถือว่าขั้นตอนเสร็จสมบูรณ์
    2.  แทนที่ **pageBuilderName()** เพื่อระบุตัวสร้างหน้าที่จะใช้

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  แทนที่ **addDataControls()** เพื่อเพิ่มกล่องข้อความ **Prod ID**
    2.  แทนที่ **addActionControls()** เพื่อเพิ่มปุ่ม **ตกลง** และ **ยกเลิก**
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  แทนที่ **pageBuilderName()** เพื่อระบุตัวสร้างหน้าที่จะใช้
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  แทนที่ **addDataControls()** เพื่อเพิ่มป้ายชื่อข้อมูลใบสั่ง สินค้า และปริมาณ

    2.  แทนที่ **addActionControls()** เพื่อเพิ่มปุ่ม **ตกลง** และ **ยกเลิก**
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > วิธีการ **generateItemInfoForProdId()** ที่ใช้ในการสร้างป้ายชื่อข้อมูลสินค้า จะถูกแยกออกจากหัวข้อนี้ วิธีการนี้จะสอบถามเกี่ยวกับตารางสองสามตารางที่จะรับรหัสสินค้า ข้อความ และมิติ ถ้าคุณต้องการเข้าใจมากขึ้นเกี่ยวกับ **generateItemInfoForProdId()** ให้ดูรหัสต้นทาง

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  แทนที่ **doExecute()** เพื่อประมวลผลการเริ่มต้นการผลิตและเพิ่มข้อความความสมบูรณ์ของกระบวนการ

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> โปรดทราบว่ารูปแบบทั่วไปมากมาย (การสร้าง UI ใหม่มีข้อผิดพลาด การตั้งค่าข้อความการเสร็จสมบูรณ์ของลักษณะการทำงาน **ตกลง** และ **ยกเลิก**) ได้รับการย้ายไปยังกรอบงาน ดังนั้นจึงบันทึกนักพัฒนาโปรแกรมประยุกต์จากการเขียนรหัสแสดงเหตุการณ์ที่มีข้อผิดพลาดซึ่งทั้งไม่สอดคล้องกัน และเสี่ยงต่อลักษณะการทำงานที่ไม่สอดคล้องกันระหว่างกระบวนการต่างๆ แม้ว่าสถานการณ์ดังกล่าวจะต้องเบี่ยงเบนจากพาธทั่วไป แต่นักพัฒนาโปรแกรมประยุกต์มีตัวเลือกในการแทนที่วิธีการที่เหมาะสม แต่ที่เป็นความเบี่ยงเบนโดยเจตนาที่ทั้งชัดแจ้งและติดตามได้


### <a name="extending-a-business-process"></a>การขยายกระบวนการทางธุรกิจ

จนถึงขณะนี้ หัวข้อนี้ได้เน้นวิธีการสร้างกระบวนการใหม่โดยใช้กรอบงาน **ProcessGuide** ในส่วนสุดท้ายนี้ คุณจะพบตัวอย่างของวิธีการขยายกระบวนการทางธุรกิจนี้

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>เพิ่มขั้นตอนในโฟลว์ (โดยใช้ ProcessGuideNavigationAgentDefault)

จะขยายที่ใด:

-   ข้อมูลรองของคลาส **ProcessGuideController** ของกระบวนการ

วิธีการขยาย:

-   ขยายวิธีการ **initializeNavigationRoute()** ในคลาสตัวควบคุม และเรียกใช้ **addFollowingStep()** ในคลาส **ProcessGuideNavigationRoute**

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>เพิ่มขั้นตอนในโฟลว์ (โดยใช้ตัวแทนการนำทางแบบกำหนดเอง)

จะขยายที่ใด:

-   ข้อมูลรองของ **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**

วิธีการขยาย:

-   สร้างคลาสรองใหม่ของ **ProcessGuideNavigationAgent** ที่จะส่งคืนชื่อขั้นตอนที่ต้องการ

-   สร้างคลาสใหม่ที่สืบทอดมาจาก **ProcessGuideNavigationAgentFactory** ที่ส่งคืนตัวแทนนําทางที่สร้างขึ้นข้างต้นแบบมีเงื่อนไข

-   ขยายวิธีการ **navigationAgentFactory()** ในคลาสตัวควบคุมเพื่อส่งคืนโรงงานที่สร้างขึ้นข้างต้นในทันที

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>เพิ่มตัวควบคุมใหม่ใน UI ของขั้นตอนที่มีอยู่ 

จะขยายที่ใด:

-   ข้อมูลรองของ **ProdProcessGuidePageBuilder** ของขั้นตอน

วิธีการขยาย:

-   ขยายวิธีการ **addDataControls()** และเพิ่มตัวควบคุมเพิ่มเติม

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>การเสร็จสิ้นการปรับปรุงอินเทอร์เฟสผู้ใช้ในขั้นตอนที่มีอยู่

จะขยายที่ใด:

-   ข้อมูลรองของ **ProdProcessGuideStep**

วิธีการขยาย:

-   สร้างคลาสรองใหม่ของคลาส **ProdProcessGuidePageBuilder** และใช้งานอินเทอร์เฟสผู้ใช้ที่ต้องการ

-   ขยายวิธีการ **pageBuildeName()** ในคลาสขั้นตอนเพื่อส่งคืน **ProcessGuidePageBuilderNameAttribute** สำหรับคลาสที่สร้างขึ้นข้างต้น

### <a name="alter-logic-when-a-step-is-considered-complete"></a>เปลี่ยนตรรกะเมื่อถือว่าขั้นตอนเสร็จสมบูรณ์

จะขยายที่ใด:

-   ข้อมูลรองของ **ProdProcessGuideStep**

วิธีการขยาย:

-   ขยายวิธีการ **isComplete()** เพื่อสร้างตรรกะเพิ่มเติม


[!INCLUDE[footer-include](../../includes/footer-banner.md)]