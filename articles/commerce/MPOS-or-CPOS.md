---
title: เลือกระหว่าง Store Commerce กับ Cloud POS
description: บทความนี้อธิบายความแตกต่างที่หลักๆ ระหว่าง Store Commerce กับ Cloud POS และอธิบายปัจจัยต่างๆ ที่ผู้ค้าปลีกซึ่งใช้ Dynamics 365 Commerce ควรพิจารณาเพื่อช่วยให้ลูกค้าเลือกสินค้าได้ดีที่สุดตามความต้องการ
author: josaw1
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 0e1092c0c5c49c6a99dd441c75f545fc831c0b03
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831569"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>เลือกระหว่าง Store Commerce กับ Cloud POS

[!include [banner](includes/banner.md)]

บทความนี้อธิบายความแตกต่างที่หลักๆ ระหว่าง Store Commerce กับ Cloud POS และอธิบายปัจจัยต่างๆ ที่ผู้ค้าปลีกซึ่งใช้ Dynamics 365 Commerce ควรพิจารณาเพื่อช่วยให้ลูกค้าเลือกสินค้าได้ดีที่สุดตามความต้องการ โดยยังให้ผู้ใช้มีพื้นหลังเพิ่มเติม เคล็ดลับ และคำแนะนำสำหรับปัจจัยที่พวกเขาควรพิจารณา เมื่อพวกเขาทำการปรับใช้ Dynamics 365 Commerce โดยการตรวจทานและการทำตามคำแนะนำนี้ เป็นส่วนหนึ่งของกระบวนการปรับใช้ ผู้ใช้งานระบบสามารถหลีกเลี่ยงปัญหาที่อาจส่งผลกระทบต่อประสิทธิภาพการทำงานหรือความพึงพอใจของผู้ใช้

## <a name="insights"></a>ข้อมูลเชิงลึก

การค้าแสดงการปรับใช้และตัวเลือกโทโพโลยีที่หลากหลาย ดังนั้น ผู้ค้าปลีกสามารถเลือกส่วนประกอบและการตั้งค่าคอนฟิกที่ตรงกับความต้องการทางธุรกิจและเทคโนโลยีของพวกเขาที่สุดได้ มุมมองหนึ่งของการใช้งานที่จำเป็นต้องมีการพิจารณาอย่างระมัดระวังคือ ตัวเลือกของแพลตฟอร์มและสัดส่วนแบบฟอร์มสำหรับส่วนประกอบการขายหน้าร้าน (POS)

### <a name="pos-platform-and-form-factor-considerations"></a>ข้อควรพิจารณาของแพลตฟอร์ม POS และสัดส่วนแบบฟอร์ม

การค้าสนับสนุนตัวเลือก POS ต่อไปนี้:

- Store Commerce สำหรับ Microsoft Windows
- Store Commerce สำหรับ iOS และ Android
- Cloud POS (CPOS) ซึ่งสนับสนุนเบราว์เซอร์ Microsoft Edge และ Google Chrome
- Modern POS (MPOS) สำหรับ Microsoft Windows (MPOS จะเลิกใช้ในเดือนตุลาคม 2023) 

ในกรณีทั้งหมด POS (Store Commerce และ CPOS) ใช้รหัสแอปพลิเคชันหลักเดียวกัน จุดนี้มีความสำคัญเนื่องจากเหตุผลต่อไปนี้:

- อินเทอร์เฟสผู้ใช้ (UI) ไม่สอดคล้องกัน โดยไม่คำนึงถึงแพลตฟอร์มหรือสัดส่วนฟอร์ม
- ความสามารถในการทำงานส่วนใหญ่จะเท่ากัน โดยไม่คำนึงถึงแพลตฟอร์มหรือสัดส่วนฟอร์ม อย่างไรก็ตาม มีความแตกต่างที่สำคัญบางประการ ความแตกต่างเหล่านี้จะปรากฏในบทความนี้
- ในร้านค้าแต่ละแห่ง ความผันแปร POS สามารถถูกรวม และสามารถเรียกใช้พร้อมกันได้ ตัวอย่างเช่น สำหรับการลงทะเบียนหลัก ผู้ค้าปลีกสามารถใช้ Store Commerce บนคอมพิวเตอร์ที่ใช้ Windows ได้ อย่างไรก็ตาม ผู้ค้าปลีกสามารถเพิ่มเติมการลงทะเบียนเหล่านั้นได้ด้วยเทอร์มินัลบนเบราเซอร์หรือบนอุปกรณ์เคลื่อนที่
- การกำหนดเองและส่วนขยายสามารถถูกใช้ได้อย่างง่ายดายระหว่างแพลตฟอร์มและสัดส่วนของแบบฟอร์ม เนื่องจากมีการใช้รหัสแอปพลิเคชันหลักร่วมกัน การกำหนดเองส่วนใหญ่จะสามารถนำมาใช้ได้ครั้งเดียว แทนที่จะหลายครั้ง

### <a name="store-commerce-vs-cpos"></a>Store Commerce เทียบกับ CPOS

ถึงแม้ว่า Store Commerce และ CPOS เหมือนกันเป็นส่วนใหญ่ มีความแตกต่างที่สำคัญบางประการที่คุณต้องทำความเข้าใจ

#### <a name="store-commerce"></a>Store Commerce

Store Commerce เป็นแอปพลิเคชันเดสก์ท็อปที่ติดตั้งและให้บริการบนอุปกรณ์

- **Windows** – แอปลพิเคชัน Store Commerce สำหรับ Windows มีโค้ดของแอปพลิเคชันทั้งหมด, Commerce Runtime (CRT) และ Hardware Station (HWS)
- **iOS/Android** – บนแพลตฟอร์มเหล่านี้ แอปพลิเคชันทำหน้าที่เป็นโฮสต์สำหรับรหัสแอปพลิเคชัน CPOS กล่าวคือ โค้ดของแอปพลิเคชันมาจากเซิร์ฟเวอร์ CPOS ที่โฮสต์บน Commerce Scale Unit สำหรับข้อมูลเพิ่มเติม ดู [ภาพรวม Commerce Scale Unit](dev-itpro/retail-store-system-begin.md)

#### <a name="cpos"></a>CPOS

เนื่องจาก CPOS ทำงานในเบราเซอร์ แอปพลิเคชันไม่ได้ติดตั้งบนอุปกรณ์ เบราเซอร์เข้าถึงรหัสแอปพลิเคชันจากเซิร์ฟเวอร์ CPOS แทน ดังนั้น CPOS จึงไม่สามารถเข้าถึงฮาร์ดแวร์ POS ได้โดยตรง หรือทำงานในสถานะออฟไลน์

### <a name="store-deployment-considerations"></a>ข้อควรพิจารณาสำหรับการปรับใช้ของร้านค้า

นอกเหนือจากแพลตฟอร์มและสัดส่วนแบบฟอร์ม ผู้ค้าปลีกยังต้องเลือกตัวเลือกการปรับใช้ที่ร้านค้าอีกด้วย ตารางต่อไปนี้แสดงการตั้งค่าคอนฟิกที่พร้อมใช้งานสำหรับตัวเลือก POS แต่ละรายการ

| แอปพลิเคชัน POS            | Commerce Scale Unit | พร้อมใช้งานแบบออฟไลน์ | การสนับสนุน HWS เฉพาะที่ |
|----------------------------|---------------------|-------------------|-------------------|
| Store Commerce สำหรับ Windows | Cloud หรือ RSSU       | ใช่               | ใช่               |
| Store Commerce สำหรับ Android | Cloud หรือ RSSU       | หมายเลข                | ใช่               |
| Store Commerce สำหรับ iOS     | Cloud หรือ RSSU       | หมายเลข                | ใช่               |
| Cloud POS                  | Cloud หรือ RSSU       | หมายเลข                | หมายเลข                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

The Commerce Scale Unit เป็นส่วนประกอบที่เป็นโฮสต์ของ CRT CRT ประกอบด้วยตรรกะทางธุรกิจทั้งหมดที่ POS ใช้ และให้การเข้าถึงฐานข้อมูลช่องทาง ในขณะที่พวกเขาออนไลน์ ไคลเอ็นต์ POS ทั้งหมดในร้านค้าใช้ Commerce Scale Unit Commerce Scale Unit สามารถปรับใช้ใน cloud หรือในร้านค้าได้อย่างใดอย่างหนึ่ง

#### <a name="offline-mode"></a>โหมดออฟไลน์

Store Commerce สำหรับ Windows รองรับโหมดออฟไลน์ ในโหมดออฟไลน์ POS สามารถดำเนินการต่อในกระบวนการขายแม้ว่าจะไม่ได้เชื่อมต่อกับ Commerce Scale Unit จากนั้น สามารถซิงโครไนส์กับฐานข้อมูลช่องทาง เมื่อมีการคืนค่าการเชื่อมต่อ Store Commerce ใช้อินสแตนซ์แบบฝังของตนเองของ CRT และใช้แหล่งข้อมูลภายในเครื่องของตนเองชั่วคราว (ฐานข้อมูล SQL Server แบบออฟไลน์) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับฟังก์ชันการทำงานแบบออฟไลน์ ดู [ฟังก์ชันแบบออฟไลน์ของ POS](pos-offline-functionality.md)

### <a name="pos-peripheralhardware-considerations"></a>ข้อควรพิจารณาของอุปกรณ์พ่วง/ฮาร์ดแวร์ POS

นอกจากนี้ ผู้ค้าปลีกต้องพิจารณาถึงวิธีที่ POS จะเข้าถึงอุปกรณ์และอุปกรณ์ต่อพ่วง เช่น เครื่องพิมพ์ ลิ้นชักเงินสด และเทอร์มินัลการชำระเงิน สถานีฮาร์ดแวร์สามารถถูกจัดสรรให้กับเครื่องบันทึกเงินสด POS หรือใช้ร่วมกันระหว่างเครื่องบันทึกเงินสดในร้านค้าได้ด้วย

| แอปพลิเคชัน POS            | HWS OPOS เฉพาะที่ | อุปกรณ์ต่อพ่วงของเครือข่าย | การสนับสนุน HWS ที่ใช้ร่วมกัน |
|----------------------------|----------------|---------------------|--------------------|
| Store Commerce สำหรับ Windows | ใช่            | ใช่                 | ใช่                |
| Store Commerce สำหรับ Android | หมายเลข             | ใช่                 | ใช่                |
| Store Commerce สำหรับ iOS     | หมายเลข             | ใช่                 | ใช่                |
| Cloud POS                  | หมายเลข             | หมายเลข                  | ใช่                |

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสถานีฮาร์ดแวร์ ให้ดู [ตั้งค่าคอนฟิกและติดตั้งสถานีฮาร์ดแวร์การขายปลีก](retail-hardware-station-configuration-installation.md)

## <a name="implementation-considerations"></a>ข้อควรพิจารณาการใช้งาน

พิจารณาข้อมูลต่อไปนี้ตามที่คุณวางแผนการนำ POS ไปใช้ในร้านค้าปลีกของคุณ:

- **ความต้องการในการทำงาน** – กระบวนการทางธุรกิจหลักและความสามารถนั้นเหมือนกัน โดยไม่คำนึงถึงแพลตฟอร์ม สัดส่วนแบบฟอร์ม หรือโทโพโลยีการปรับใช้ ดังนั้น ผู้ค้าปลีกส่วนใหญ่ไม่จำเป็นต้องพิจารณาความต้องการในการทำงาน เมื่อพวกเขาวางแผนปฏิบัติการของพวกเขา
- **การเชื่อมต่อ** – ความพร้อมใช้งานบนเครือข่าย (เครือข่ายบริเวณกว้าง \[WAN\] และเครือข่ายท้องถิ่น \[LAN\]) เป็นปัจจัยหลักที่จำเป็นต้องมีการพิจารณาอย่างระมัดระวัง สิทธิประโยชน์ใดๆ ที่โซลูชัน footprint ศูนย์ โฮสต์ cloud ในกรณีของต้นทุนและความเรียบง่ายจะหายไป ถ้าระบบไม่พร้อมใช้งานสำหรับกระบวนการทางธุรกิจที่สำคัญ

    หากการเชื่อมต่อสำหรับอุปกรณ์ที่มีให้ไม่เป็นอิสระและยืดหยุ่นมากๆ หรือถ้าจำนวนที่แน่นอนของการหยุดทำงานไม่สามารถยอมรับได้แก่ผู้ขายปลีก เราขอแนะนำหนึ่งในตัวเลือกต่อไปนี้:

    - ใช้ Store Commerce ใน Windows และเปิดใช้งานโหมดออฟไลน์
    - ปรับใช้ Commerce Scale Unit ในสถานที่

    ตัวเลือกสองตัวเลือกเหล่านี้ไม่เป็นแบบเฉพาะร่วมกัน สำหรับโทโพโลยีที่เชื่อถือได้มากที่สุด ผู้ค้าปลีกสามารถปรับใช้ RSSU ท้องถิ่นเพื่อลดการขึ้นต่อกันในการเชื่อมต่ออินเทอร์เน็ต หรือความพร้อมใช้งาน Azure และพวกเขายังสามารถปรับใช้เครื่องบันทึกเงินสด POS ที่ซึ่งโหมดออฟไลน์ถูกเปิดใช้งาน ถ้ามีปัญหาเกี่ยวกับเซิร์ฟเวอร์ท้องถิ่นหรือเครือข่าย

- **อุปกรณ์ฮาร์ดแวร์/อุปกรณ์ต่อพ่วงฮาร์ดแวร์** – มุมมองสำคัญมุมมองหนึ่งของระบบ Retail POS คือ ความสามารถในการใช้อุปกรณ์ต่อพ่วง POS เช่น เครื่องพิมพ์ ลิ้นชักเงินสด และเทอร์มินัลการชำระเงิน ถึงแม้ว่าตัวเลือก POS ที่พร้อมใช้งานทั้งหมดสามารถใช้อุปกรณ์ต่อพ่วงได้ มีเฉพาะ Store Commerce สำหรับ Windows ที่สนับสนุนโดยตรง สำหรับแอปพลิเคชันอื่นๆ ทั้งหมด จำเป็นต้องใช้สถานีฮาร์ดแวร์หนึ่งรายการหรือมากกว่า ถึงแม้ว่าวิธีการนี้จะเพิ่มความยืดหยุ่น ส่วนประกอบเพิ่มเติมต้องถูกปรับใช้ ตั้งค่าคอนฟิก และให้บริการ
- **ข้อกำหนดของระบบ** – ความต้องการของระบบสำหรับแอปพลิเคชัน POS แตกต่างกัน ต้องแน่ใจว่าตรวจสอบข้อมูลล่าสุด ก่อนที่จะทำการเลือกของคุณ ตัวอย่างเช่น เนื่องจาก CPOS ทำงานในเบราเซอร์ ซึ่งสนับสนุนช่วงของระบบปฏิบัติการที่กว้าง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับข้อกำหนดของระบบ ดู [ความต้องการของระบบสำหรับการปรับใช้ cloud](../fin-ops-core/fin-ops/get-started/system-requirements.md)
- **การปรับใช้และการให้บริการ** – ความซับซ้อนของการปรับใช้และความต้องการในการบริการอาจแตกต่างกัน โดยขึ้นอยู่กับตัวเลือกแอปพลิเคชันและการปรับใช้ ตัวอย่างเช่น สำหรับการปรับใช้ CPOS ที่โฮสต์ cloud คุณไม่ต้องติดตั้งและอัพเดตในทุกอุปกรณ์ ดังนั้น วิธีการนี้จะลดความซับซ้อนและต้นทุนลงอย่างมาก อย่างไรก็ตาม ถ้าคุณปรับใช้งาน Store Commerce บนเครื่องบันทึกเงินสดทุกเครื่อง และเปิดใช้งานโหมดออฟไลน์ และนอกจากนั้น คุณยังจะปรับใช้สถานีฮาร์ดแวร์ที่ใช้ร่วมกันด้วย คุณจะเพิ่มจำนวนของปลายทางที่ต้องได้รับการจัดการอย่างมาก


[!INCLUDE[footer-include](../includes/footer-banner.md)]
