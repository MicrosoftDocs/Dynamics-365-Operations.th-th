---
title: เริ่มต้นใช้งานการเช่าสินทรัพย์
description: บทความนี้จะอธิบายความสามารถในการเช่าสินทรัพย์และนำไปสู่ขั้นตอนต่างๆ สำหรับการสร้างการเช่าสินทรัพย์ และดูข้อมูลสำหรับการเช่าเหล่านั้น
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeasingWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom:
- "4464"
- intro-internal
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: df4343031b3b116318f798f31adb4d1f6bed1db9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895151"
---
# <a name="asset-leasing-get-started"></a>เริ่มต้นใช้งานการเช่าสินทรัพย์

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายความสามารถในการเช่าสินทรัพย์และนำไปสู่ขั้นตอนต่างๆ สำหรับการสร้างการเช่าสินทรัพย์ และดูข้อมูลสำหรับการเช่าเหล่านั้น บทความนี้ยังกำหนดคำศัพท์ที่ใช้ในอินเทอร์เฟสผู้ใช้และคู่มือ การเช่าสินทรัพย์เป็นความสามารถขั้นสูงสำหรับการจัดการ การติดตาม และการทำธุรกรรมทางการเงินโดยอัตโนมัติสำหรับสินทรัพย์ที่เช่าใน Microsoft Dynamics 365 Finance การเช่าสินทรัพย์สอดคล้องกับมาตรฐานการบัญชีระหว่างประเทศ (IFRS 16) และมาตรฐาน US GAAP (ASC 842) การเช่าสินทรัพย์จะรวบรวมและประมวลผลข้อมูลเกี่ยวกับการเช่าและช่วยสร้างรายการสมุดรายวัน ตลอดทั้งระยะเวลาของการเช่า จากการรับรู้ครั้งแรก รายการสมุดรายวันรายเดือน ไปยังการด้อยค่าของสินทรัพย์และการสิ้นสุดการเช่า การเช่าสินทรัพย์รวมกับส่วนประกอบอื่นของ Dynamics 365 Finance รวมถึงสินทรัพย์ถาวร บัญชีเจ้าหนี้ และบัญชีแยกประเภททั่วไปอย่างราบรื่น

ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน **การจัดการคุณลักษณะ** เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้ค้นหาและเลือกคุณลักษณะที่ชื่อคุณลักษณะ **การเช่าสินทรัพย์** แล้วคลิกปุ่ม **เปิดใช้งานตอนนี้**

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับมาตรฐานการบัญชี อ้างอิงถึงเอกสารมาตรฐานสำหรับ IFRS 16 และ US GAAP ASC 842

## <a name="asset-leasing-elements"></a>องค์ประกอบของการเช่าสินทรัพย์
แผนภาพต่อไปนี้แสดงองค์ประกอบหลักของกระบวนการทางธุรกิจสำหรับการเช่า

[![องค์ประกอบของการเช่าสินทรัพย์](./media/overview-01.png)](./media/overview-01.png)

สินทรัพย์ที่เช่ามีส่วนประกอบหลักดังต่อไปนี้

- **ข้อตกลงการเช่า** - ผู้ให้เช่าเป็นเจ้าของสินทรัพย์และตกลงกับผู้เช่าเพื่อให้เช่าสินทรัพย์สำหรับรอบระยะเวลาที่ระบุในอัตราแลกเปลี่ยนสำหรับการชำระค่าเช่าเป็นงวด นอกจากสัญญาที่ถูกต้องตามกฎหมายระหว่างผู้ให้เช่าและผู้เช่า ข้อตกลงการเช่าจะจับคู่การตัดสินใจของผู้จัดการ เช่น โอกาสของตัวเลือกการต่อสัญญา และการโอนสิทธิ์ความเป็นเจ้าของ

- **การคำนวณการเช่าและการจัดประเภทตามมาตรฐานการบัญชี** -การคำนวณการเช่าและการจัดประเภทระบุมาตรฐานการบัญชีที่จะใช้ในการประเมินค่าเริ่มต้นและครั้งต่อๆ ไป รวมทั้งการทดสอบการจัดประเภทที่กำหนดว่าชนิดการเช่าจะเป็นอย่างไร การเช่าอาจเป็นสัญญาเช่าการเงิน สัญญาเช่าดำเนินงาน สัญญาเช่าระยะสั้น หรือสัญญาเช่ามูลค่าต่ำ นอกจากนี้ ระบบยังคำนวณมูลค่าปัจจุบันสุทธิของการชำระค่าเช่าขั้นต่ำในอนาคตสำหรับวัตถุประสงค์ของการประเมินค่าและการจัดประเภท

- **ธุรกรรมการเช่า** - การเช่าสินทรัพย์สนับสนุนการรับรู้เริ่มต้นของสิทธิ์การใช้สินทรัพย์สำหรับการเช่าในงบดุล รวมถึงการวัดที่ตามมาสำหรับการเช่างบดุลเปิดหรือการเช่างบดุลปิด ธุรกรรมการรับรู้เริ่มต้นจะวัดมูลค่าปัจจุบันสุทธิของการชำระค่าเช่าขั้นต่ำในอนาคต ข้อมูลนี้จะใช้ในการกำหนดมูลค่าของสิทธิ์การใช้สินทรัพย์ และหนี้สินสัญญาเช่า ซึ่งส่งผลกระทบต่องบดุลขององค์กร การประเมินผลการทำธุรกรรมการเช่ารายเดือนในเวลาต่อมาจะเกี่ยวข้องกับการสะสมดอกเบี้ยในหนี้สินสัญญาเช่า ซึ่งจะเพิ่มหนี้สินสัญญาเช่า นอกจากนี้ยังมีการวัดผลรายการคงค้างของการชำระค่าเช่าที่ลดหนี้สินสัญญาเช่า และที่จะจ่ายให้แก่ผู้ให้เช่าในเวลาต่อมา การวัดผลรวมถึงการตัดบัญชีของสิทธิ์การใช้สินทรัพย์

  สำหรับการเช่างบประมาณปิด ระบบจะคำนวณค่าใช้จ่ายการเช่าแบบเส้นตรงโดยมีมูลค่าน้อยกว่า: อายุทางเศรษฐกิจของสินทรัพย์ หรือระยะเวลาของสัญญาเช่า การปรับเปลี่ยนการเช่าวัดการปรับปรุงสัญญา เช่น การต่อหรือขยายสัญญาเช่า และธุรกรรมการด้อยค่าที่ใช้สินทรัพย์ที่ใช้สิทธิ์การใช้สินทรัพย์สำหรับต้นทุนที่ไม่ได้รับคืน

  การเช่าสินทรัพย์รวมกับบัญชีแยกประเภททั่วไปเพื่อให้แน่ใจว่าธุรกรรมการเช่าที่ลงรายการบัญชีแล้วทั้งหมดจะอัพเดผังบัญชีของคุณ การเช่าสินทรัพย์รวมกับบัญชีเจ้าหนี้เพื่อติดตามใบแจ้งหนี้ของผู้ให้เช่าในบัญชีเจ้าหนี้ และใช้การชำระเงินในอนาคตจากที่นั่น การรวมกับสินทรัพย์ถาวรช่วยให้คุณสามารถติดตามการเช่าในการลงทะเบียนสินทรัพย์ถาวร และลงรายการบัญชีธุรกรรมสิทธิ์การใช้สินทรัพย์ รวมถึงการรับรู้เริ่มต้น ค่าเสื่อมราคา และการด้อยค่าของสินทรัพย์ จากภายในสินทรัพย์ถาวร   

## <a name="asset-leasing-components"></a>ส่วนประกอบของการเช่าสินทรัพย์ 
การเช่าสินทรัพย์แม็บข้อมูลการเช่า กำหนดการชำระเงิน วันที่เริ่มต้นและวันที่สิ้นสุด และความถี่ในการชำระเงิน นอกจากนี้ ยังทำให้การคำนวณสำหรับมูลค่าปัจจุบันสุทธิ การชำระค่าเช่ารายเดือน ดอกเบี้ย และการตัดบัญชีการเช่า เป็นแบบอัตโนมัติ ระบบทำการทดสอบการจัดประเภทการเช่า ทั้งนี้ขึ้นอยู่กับการตั้งค่าคอนฟิก ระบบยังสร้างและลงรายการบัญชีธุรกรรมการเช่าที่สัมพันธ์กัน ซึ่งยึดตามกรอบงานที่กำหนดโดยมาตรฐานการบัญชีที่คุณกำลังติดตาม

แผนภาพต่อไปนี้แสดงสมุดบัญชีค่าเช่า การเช่า กำหนดการชำระเงินที่คำนวณ การทดสอบการจัดประเภทสำหรับการเช่าและสมุดบัญชีการเช่า และธุรกรรมทางบัญชีที่เกี่ยวข้อง

[![การเช่า สมุดบัญชีค่าเช่า และกำหนดการชำระเงิน](./media/overview-02.png)](./media/overview-02.png)

- **สมุดบัญชีค่าเช่า** - สมุดบัญชีค่าเช่ารวมถึงข้อมูลสัญญาเช่าทั้งหมด เช่น เงื่อนไขการเช่า มูลค่ายุติธรรม และการชำระเงินตามสัญญาเช่า นอกจากนี้ยังรวมถึงมาตรฐานการบัญชีที่คุณกำลังติดตาม, ชนิดของการเช่า และขีดจำกัดที่มีการพิจารณาในการทดสอบการจัดประเภทการเช่า สมุดบัญชีค่าเช่ามีธุรกรรมการเช่าที่ลงรายการบัญชีในบัญชีแยกประเภททั่วไป 
  
- **การเช่า** - การเช่ามีข้อมูลการเช่าสินทรัพย์ซึ่งแสดงถึงรากฐานของการเช่าสินทรัพย์ แหล่งข้อมูลการเช่าเป็นสัญญาเช่า และการตัดสินใจของผู้บริหารซึ่งทั้งสองจะทำไว้ภายนอก Dynamics 365 Finance มูลค่ายุติธรรมของสินทรัพย์ คือราคาที่จะต้องชำระสำหรับสินทรัพย์ในธุรกรรม ณ วันที่ประเมิน ค่านี้อาจขึ้นอยู่กับชนิดของสินทรัพย์ สภาวะตลาด และเกณฑ์อื่นๆ ที่สามารถนำมาพิจารณาในการประเมินได้ มูลค่ายุติธรรมของสินทรัพย์จะถือเป็นสมการการทดสอบการจัดประเภท

- **อายุการใช้งานสินทรัพย์** - ซึ่งแสดงถึงรอบระยะเวลาที่เหลือของอายุการใช้งานของสินทรัพย์ที่มีผลตั้งแต่วันที่เริ่มต้นการเช่า อายุการใช้งานของสินทรัพย์จะถือเป็นสมการการทดสอบการจัดประเภท ซึ่งแตกต่างจากอายุการใช้งานตามที่กำหนดไว้ในสินทรัพย์ถาวร

- **อัตราดอกเบี้ยเงินกู้ส่วนเพิ่ม** - นี่คืออัตราดอกเบี้ยที่จะใช้ในการคำนวณมูลค่าปัจจุบันสุทธิ ระบบจะใช้อัตราโดยปริยาย ถ้ามีการกำหนดไว้ในข้อมูลสัญญาเช่าเพื่อคำนวณมูลค่าปัจจุบันสุทธิของการชำระค่าเช่า ถ้าไม่ได้กำหนดอัตราโดยปริยาย ระบบจะใช้อัตราดอกเบี้ยเงินกู้ส่วนเพิ่ม

- **ชนิดเงินรายปี** - นี่คือการชำระค่าเช่าที่ครบกำหนดในวันที่เริ่มต้นของรอบระยะเวลาการชำระเงินหรือเมื่อสิ้นสุดรอบระยะเวลา การชำระเงินนี้อาจเป็นการชำระเงินล่วงหน้าหรือเงินรายปีที่ครบกำหนด (เมื่อเริ่มต้นของระยะเวลาการชำระค่าเช่า) หรือเงินรายปีปกติ (เมื่อสิ้นสุดรอบระยะเวลาการชำระค่าเช่า)

  เดือนแรกจะถือว่าเป็นรอบระยะเวลาที่ศูนย์สำหรับการชำระเงินล่วงหน้า เดือนแรกจะถือว่าเป็นรอบระยะเวลาที่หนึ่งสำหรับค้างการชำระเงิน

- **ช่วงการทบต้น** - นี่แสดงถึงรอบระยะเวลาที่ดอกเบี้ยถูกทบรวมต่อปี การทำเช่นนี้อาจเป็นรายเดือน (12 รอบระยะเวลาต่อปี) รายไตรมาส (4 รอบระยะเวลาต่อปี) รายครึ่งปี (2 รอบระยะเวลาต่อปี) หรือเป็นรายปี (1 รอบระยะเวลาต่อปี) จำนวนของรอบระยะเวลาจะได้รับการพิจารณาในการคำนวณมูลค่าปัจจุบันสุทธิ

- **วันที่เริ่มต้น** - นี่คือวันที่ผู้ให้เช่าทำให้สินทรัพย์พร้อมใช้งานโดยผู้เช่า การคำนวณการเช่าและธุรกรรมทั้งหมดจะขึ้นอยู่กับวันที่เริ่มต้น วันที่เริ่มต้นควรเป็นวันที่เริ่มต้นรอบระยะเวลา (แรกของเดือน) เพื่อให้แน่ใจว่ามีความถูกต้องของการคำนวณในเวลาต่อมา คุณสามารถใช้ฟิลด์ **วันที่ของลายเซ็นสัญญา** เพื่อป้อนวันที่จริงเมื่อมีการลงชื่อในสัญญา

- **ระยะเวลาของสัญญาเช่า** - นี่คือความยาวของรอบระยะเวลาการเช่า เป็นรายเดือน

> [!NOTE] 
> ข้อกำหนดของระยะเวลาของสัญญาเช่าจะขึ้นอยู่กับจำนวนรอบระยะเวลาห รือช่วงเวลา ในบรรทัดกำหนดการชำระเงิน จำนวนช่วงที่กำหนดจะถูกแปลงเป็นเดือน

- **รายการกำหนดการชำระเงิน** - ซึ่งจะจับการชำระค่าเช่าต่อรอบระยะเวลา นอกจากนี้ยังระบุว่ารอบระยะเวลาการต่ออายุจะมีผลใช้และรวมอยู่ในการประเมินเริ่มต้นของสิทธิ์การใช้สินทรัพย์ย์และหนี้สินสัญญาเช่า คุณสามารถกำหนดวันที่เริ่มต้นของกำหนดการชำระเงินของสัญญาเช่าและช่วงรอบระยะเวลาที่แสดงถึงความยาวของสัญญาเช่าซึ่งอาจเป็นวัน เดือน หรือปี

- **ความถี่ในการชำระเงิน** - ซึ่งบ่งชี้ว่าเป็นการชำระเงินเป็นรายเดือน รายไตรมาส รายครึ่งปี หรือรายปี มีการคำนวณวันที่สิ้นสุดโดยอัตโนมัติตามวันที่เริ่มต้นและจำนวนรอบระยะเวลาที่ป้อน

- **กำหนดการชำระเงิน** - นี่คือมูลค่าปัจจุบันสุทธิที่คำนวณได้ โดยยึดตามระยะเวลาที่ครอบคลุมโดยการชำระค่าเช่า จำนวนของการชำระเงิน รอบระยะเวลาการทบต้น และชนิดเงินรายปี

- **รอบระยะเวลา** - นี่คือรอบระยะเวลาการเช่าที่สะท้อนถึงชนิดของการรวมภายในและเงินรายปี ช่วงการทบต้นจะกำหนดวิธีการแบ่งรอบระยะเวลา คุณสามารถตั้งค่าช่วงการทบต้นต่อไปนี้:

  - รายเดือน 12 รอบระยะเวลาต่อปี
  - รายไตรมาส 4 รอบระยะเวลาต่อปี
  - รายครึ่งปี 2 รอบระยะเวลาต่อปี
  - รายปี 1 รอบระยะเวลาต่อปี

รอบระยะเวลาแรกจะเริ่มต้นด้วยศูนย์ ถ้าชนิดเงินรายปีเป็นเงินรายปีที่ครบกำหนด มิฉะนั้น รอบระยะเวลาแรกจะเริ่มต้นด้วยด้วยหนึ่ง ถ้าชนิดเงินรายปีเป็นยอดค้างชำระ

- **เดือน** - ซึ่งแสดงจำนวนเดือนในปฏิทินตามระยะเวลาของการเช่า ยอดการชำระเงินคือยอดเงินที่ต้องชำระตามที่กำหนดไว้ในความถี่ในการชำระเงิน มูลค่าปัจจุบันสุทธิที่คำนวณได้คือ การชำระค่าเช่าตามมูลค่าปัจจุบันสุทธิสำหรับแต่ละรอบระยะเวลา การทบต้น และอัตราดอกเบี้ยเงินกู้ส่วนเพิ่ม

> [!NOTE] 
> มูลค่าปัจจุบันสุทธิถูกคำนวณตามสมการกระแสเงินสดที่ได้รับส่วนลด

- **สมุดบัญชี** - นี่คือการตั้งค่าที่ตั้งค่าคอนฟิกไว้ล่วงหน้าซึ่งจะเชื่อมโยงกับแต่ละการเช่า สมุดบัญชีจะกำหนดมาตรฐานทางการบัญชีที่นำมาใช้ ชนิดของการเช่า และขีดจำกัดที่ใช้เป็นข้อมูลพื้นฐานสำหรับการทดสอบการจัดประเภท การทดสอบการจัดประเภทใช้เพื่อระบุชนิดของการเช่าโดยอัตโนมัติ

- **กรอบงานการบัญชี** - ซึ่งแสดงมาตรฐานทางบัญชีที่เลือก ซึ่งเป็นการใช้ IFRS 16 และ ASC 842 ซึ่งคุณจะสนับสนุน มาตรฐานทางการบัญชีจะถูกกำหนดให้กับสมุดบัญชีที่เชื่อมโยงกับการเช่า มาตรฐานทางการบัญชีจะกำหนดบัญชีแยกประเภทที่ระบุไว้ในโพรไฟล์การลงรายการบัญชี

- **ชนิดการเช่า** ซึ่งบ่งชี้ว่าจะใช้สัญญาเช่าชนิดใด อาจเป็นสัญญาเช่าการเงินหรือสัญญาเช่าดำเนินงาน ภายใต้สัญญาเช่าการเงิน ความเสี่ยงและผลตอบแทนที่เกี่ยวข้องกับสินทรัพย์ที่ให้เช่าจะถูกโอนย้ายไปยังผู้เช่า ภายใต้สัญญาเช่าดำเนินงาน ความเสี่ยงและผลตอบแทนที่เกี่ยวข้องกับสินทรัพย์ที่ให้เช่ายังคงอยู่กับผู้ให้เช่า ตัวเลือกที่สามคือการระบุรหัสประจำตัวอัตโนมัติของชนิดการเช่า ซึ่งอาจเป็นการเงินหรือการดำเนินงานตามเกณฑ์ที่กำหนดไว้ในสมุดบัญชี การการระบุรหัสประจำตัวอัตโนมัตินี้ดำเนินการในระหว่างการทดสอบการจัดประเภทการเช่าใหม่

- **ขีดจำกัด** - ใช้ในการทดสอบการจัดประเภทการเช่าเพื่อตรวจสอบว่าสินทรัพย์มีการจัดประเภทเป็นอย่างใดอย่างหนึ่งต่อไปนี้:

  - **ระยะเวลาของสัญญาเช่า** - นี่คือเปอร์เซ็นต์ของอายุการใช้งานที่จะใช้ในการทดสอบการจัดประเภท ระบบจะจัดประเภทการเช่าเป็นการเงินถ้ามีการตั้งค่าชนิดการเช่าเป็นอัตโนมัติ และถ้าระยะเวลาของสัญญาเช่าเหนือการใช้งานของสินทรัพย์มากกว่าหรือเท่ากับเปอร์เซ็นต์ที่กำหนดไว้ที่นี่

  - **มูลค่าปัจจุบันสุทธิ** - นี่คือเปอร์เซ็นต์ของมูลค่ายุติธรรมของสินทรัพย์ที่จะถูกใช้ในการทดสอบการจัดประเภท ระบบจะจัดประเภทสัญญาเช่าเป็นการเงิน ถ้ามีการตั้งค่าชนิดสัญญาเช่าเป็นอัตโนมัติ และถ้ามูลค่าปัจจุบันสุทธิของการชำระค่าเช่าในอนาคตเหนือมูลค่ายุติธรรมของสินทรัพย์มากกว่าหรือเท่ากับเปอร์เซ็นต์ที่กำหนดไว้ที่นี่

  - **การให้เช่าระยะสั้น** - ถ้าระยะเวลาของสัญญาเช่าน้อยกว่าหรือเท่ากับค่าที่กำหนดไว้ การเช่าจะถูกจัดประเภทเป็นสัญญาเช่าระยะสั้น

  - **มูลค่าต่ำ** - ถ้ามูลค่ายุติธรรมของสัญญาเช่าน้อยกว่าหรือเท่ากับค่าที่กำหนดไว้ การเช่าจะถูกจัดประเภทเป็นสัญญาเช่ามูลค่าต่ำ

  - **การจัดประเภทการเช่าและธุรกรรม** การจัดประเภทการเช่าเป็นกระบวนการอัตโนมัติในการจัดประเภทการเช่าตามขีดจำกัดที่กำหนดไว้ในสมุดบัญขีนอกเหนือจากเกณฑ์การทดสอบการจัดประเภทอื่นๆ เพื่อระบุว่าการเช่าเป็น สัญญาเช่าการเงิน สัญญาเช่าระยะสั้น หรือสัญญาเช่ามูลค่าต่ำ นอกจากนี้ยังใช้เพื่อระบุว่ากระบวนการค่าเช่ารอตัดบัญชีเป็นไปตาม

การทดสอบการจัดประเภทรวมถึงการโอนความเป็นเจ้าของ ตัวเลือกการซื้อ ระยะเวลาของสัญญาเช่า มูลค่าปัจจุบันสุทธิ และสินทรัพย์ที่ไม่ซ้ำกัน แผนภาพต่อไปนี้แสดงให้เห็นถึงการทดสอบการจัดประเภทการเช่า

[![การทดสอบการจัดประเภทการเช่า](./media/overview-03.png)](./media/overview-03.png)

ชนิดของการเช่าแต่ละชนิดจะจัดการการบัญชีที่แตกต่างกันสำหรับธุรกรรมการเช่าต่างๆ ธุรกรรมรวมถึงการรับรู้ ดอกเบี้ยจ่าย กำหนดการชำระค่าเช่า และการคิดค่าเสื่อมราคา และอยู่บนพื้นฐานของมาตรฐานทางบัญชีที่คุณกำลังติดตาม (IFRS 16 หรือ ASC 842) บัญชีแยกประเภทจะถูกกำหนดภายใต้โพรไฟล์การลงรายการบัญชีการเช่าสำหรับชนิดธุรกรรมและกรอบงานการบัญชีแต่ละชนิด

## <a name="asset-leasing-transactions"></a>ธุรกรรมการเช่าสินทรัพย์

#### <a name="initial-recognition"></a>การรับรู้เมื่อเริ่มแรก 
การรับรู้เริ่มต้นของสินทรัพย์ที่ให้เช่าใช้มูลค่าปัจจุบันสุทธิที่คำนวณได้ เพื่อให้สามารถรายงานในงบดุลได้ รายการบัญชีนี้จะถูกสร้างขึ้นโดยอัตโนมัติ ธุรกรรมนี้จะเดบิตบัญชีสิทธิ์การใช้สินทรัพย์ย์ และเครดิตบัญชีหนี้สินสัญญาเช่าดำเนินงานต่อไปนี้ ถ้าสินทรัพย์ถาวรสัมพันธ์กับการเช่า รายการการรับรู้เริ่มต้นจะสะท้อนให้เห็นในรูปของการซื้อสินทรัพย์ถาวร ในสถานการณ์นี้ คุณต้องกำหนดโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวรที่จะลงรายการบัญชีไปยังบัญชีสิทธิ์การใช้สินทรัพย์ 

> [!NOTE]
> สัญญาเช่าดำเนินงานได้รับการสนับสนุนโดย US GAAP ASC 842 เท่านั้น

|     ชนิดข้อมูล                                          |     เดบิต                     |     เครดิต                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     สัญญาเช่าดำเนินงานภายใต้ US GAAP            |     สิทธิ์การใช้สินทรัพย์        |     หนี้สินสัญญาเช่าดำเนินงาน     |
|     สัญญาเช่าการเงินภายใต้ IFRS และ US GAAP      |     สิทธิ์การใช้สินทรัพย์        |     หนี้สินสัญญาเช่าการเงิน       |

#### <a name="lease-liability-amortization-interest-expense"></a>การตัดบัญชีหนี้สินสัญญาเช่า (ดอกเบี้ยจ่าย) 
ดอกเบี้ยสำหรับการเช่ามีการรับรู้โดยการคำนวณดอกเบี้ยสำหรับยอดดุลต้นงวดของค่าเช่า การชำระเงินตามระยะเวลาการให้เช่า อัตราดอกเบี้ย และรอบระยะเวลาของช่วงเวลาต่อปี ยอดดอกเบี้ยเพิ่มบัญชีหนี้สินสัญญาเช่าดำเนินงานโดยการเครดิต ซึ่งจะสะท้อนให้เห็นในงบดุลขององค์กร ธุรกรรมนี้ยังมีรายการเดบิตไปยังบัญชีค่าใช้จ่ายดอกเบี้ย ซึ่งสะท้อนให้เห็นในงบกำไรขาดทุนสำหรับสัญญาเช่าทางการเงิน และไปยังบัญชีค่าใช้จ่ายในการเช่าสำหรับสัญญาเช่าดำเนินงาน

|     ชนิดข้อมูล                                          |     เดบิต                     |     เครดิต                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     รายการหนี้สินสัญญาเช่าดำเนินงานภายใต้ US GAAP ASC 842    |     ค่าใช้จ่ายของสัญญาเช่า         |     หนี้สินสัญญาเช่าดำเนินงาน         |
|     รายการหนี้สินสัญญาเช่าการเงินภายใต้ IFRS และ US GAAP      |     ค่าใช้จ่ายดอกเบี้ย          |     หนี้สินสัญญาเช่าการเงิน           |

#### <a name="accrued-lease-payment"></a>การชำระค่าเช่าค้างจ่าย
การชำระค่าเช่าค้างจ่ายจะมีการรับรู้เป็นการชำระเงินในอนาคต ซึ่งเนื่องมาจากการดำเนินการเป็นธุรกรรมการชำระเงินจากบัญชีธนาคารหรือบัญชีเงินสด การชำระค่าเช่าที่ต้องชำระให้จะลดหนี้สินสัญญาเช่าโดยการเดบิตบัญชีหนี้สินสัญญาเช่าของผู้จัดจำหน่ายที่มีการกำหนดผู้ให้เช่าเป็นผู้จัดจำหน่าย หรือลงรายการบัญชีด้านเครดิตให้กับบัญชีแยกประเภทของตั๋วเงินเจ้าหนี้ จะมีการดำเนินการชำระเงินให้แก่ผู้จัดจำหน่ายหรือตั๋วเจ้าหนี้ทั้งหมด

|     ชนิดข้อมูล                                          |     เดบิต                     |     เครดิต                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     สัญญาเช่าดำเนินงานภายใต้ US GAAP              |  หนี้สินสัญญาเช่าดำเนินงาน    |   หนี้สินของผู้จัดจำหน่าย (บัญชีแยกประเภทย่อย)/ตั๋วเงินเจ้าหนี้  |
|     สัญญาเช่าการเงินภายใต้ IFRS และ US GAAP        |  หนี้สินสัญญาเช่าการเงิน      |   หนี้สินของผู้จัดจำหน่าย (บัญชีแยกประเภทย่อย)/ตั๋วเงินเจ้าหนี้  |

#### <a name="asset-depreciation"></a>ค่าเสื่อมราคาของสินทรัพย์
สิทธิ์การใช้สินทรัพย์จะคิดค่าเสื่อมราคา แล้วแต่ว่าจำนวนใดจะน้อยกว่า - อายุการใช้งานของสินทรัพย์หรือระยะเวลาของสัญญาเช่า วิธีการสำหรับการคำนวณค่าเสื่อมราคาสำหรับสัญญาเช่าดำเนินงาน US GAAP (ASC 842) จะขึ้นอยู่กับความแตกต่างระหว่างค่าใช้จ่ายการเช่าแบบเส้นตรงและจำนวนดอกเบี้ย ค่าเสื่อมราคาในสัญญาเช่าการเงินจะถูกคำนวณโดยใช้วิธีการแบบเส้นตรงมาตรฐาน การคิดค่าเสื่อมราคาตามสัญญาเช่ามีผลกระทบต่องบกำไรขาดทุนโดยเดบิตดอกเบี้ยจ่าย งบดุลได้รับผลกระทบจากการเครดิตบัญชีสิทธิ์การใช้สินทรัพย์สำหรับสัญญาเช่าทางการเงินที่สะสม ถ้าการเช่าถูกลิงก์กับสินทรัพย์ถาวร ธุรกรรมค่าเสื่อมราคาจะมีการดำเนินการจากโมดูลบัญชีสินทรัพย์ถาวรเท่านั้น 

|     ชนิดข้อมูล                                          |     เดบิต                     |     เครดิต                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     สัญญาเช่าดำเนินงานภายใต้ US GAAP              |  ค่าใช้จ่ายของสัญญาเช่า                |   การคิดค่าเสื่อมราคาสะสมของสิทธิ์การใช้สินทรัพย์     |
|     สัญญาเช่าการเงินภายใต้ IFRS และ US GAAP        |   การคิดค่าเสื่อมราคาค่าใช้จ่าของสิทธิ์การใช้สินทรัพย์   |   การคิดค่าเสื่อมราคาสะสมของสิทธิ์การใช้สินทรัพย์    |

#### <a name="short-term-lease"></a>สัญญาเช่าระยะสั้น
การให้เช่าระยะสั้นเป็นค่าใช้จ่าย ซึ่งจะมีผลกระทบต่องบกำไรขาดทุนขององค์กร การชำระค่าเช่าที่สร้างขึ้น จะเดบิตบัญชีค่าใช้จ่ายในการเช่า และเครดิตบัญชีเจ้าหนี้หรือบัญชีแยกประเภทย่อยของผู้จัดจำหน่าย

|     ชนิดข้อมูล                                          |     เดบิต                     |     เครดิต                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     รายการสัญญาเช่าระยะสั้นภายใต้ IFRS และ US GAAP     |  ค่าใช้จ่ายของสัญญาเช่า                |   หนี้สินของผู้จัดจำหน่าย (บัญชีแยกประเภทย่อย)/ตั๋วเงินเจ้าหนี้  |

#### <a name="low-value-lease"></a>สัญญาเช่ามูลค่าต่ำ
สัญญาเช่ามูลค่าต่ำเป็นค่าใช้จ่ายที่มีผลกระทบต่องบกำไรขาดทุนขององค์กรของคุณ การชำระค่าเช่าที่สร้างขึ้น จะเดบิตค่าใช้จ่ายในการเช่า และเครดิตเจ้าหนี้หรือบัญชีแยกประเภทย่อยของผู้จัดจำหน่าย

|     ชนิดข้อมูล                                          |     เดบิต                     |     เครดิต                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     รายการสัญญาเช่ามูลค่าต่ำภายใต้ IFRS และ US GAAP      |  ค่าใช้จ่ายของสัญญาเช่า                |   หนี้สินของผู้จัดจำหน่าย (บัญชีแยกประเภทย่อย)/ตั๋วเงินเจ้าหนี้  |


#### <a name="index-revaluation"></a>การประเมินค่าดัชนีใหม่
นี่เป็นบัญชีการเช่าสินทรัพย์สำหรับการชำระเงินค่าเช่าผันแปรที่วัดโดยอัตราดัชนี การเปลี่ยนแปลงการชำระเงินค่าเช่าที่เกิดจากความผันผวนของอัตราดัชนีถือเป็นการปรับปรุงการเช่าภายใต้ IFRS 16 หนี้สินสัญญาเช่าและสิทธิ์การใช้สินทรัพย์จะได้รับการปรับปรุงให้เป็นไปตามบัญชีสำหรับการชำระเงินใหม่ 

|     ชนิดข้อมูล                                          |     เดบิต                             |     เครดิต                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   การประเมินค่าดัชนีใหม่ภายใต้ IFRS ในกรณีที่มีการเพิ่มขึ้น  |  สิทธิ์การใช้สินทรัพย์       |   หนี้สินสัญญาเช่าดำเนินงาน |
|   การประเมินค่าดัชนีใหม่ภายใต้ IFRS ในกรณีที่มีการลดลง  |  หนี้สินสัญญาเช่าดำเนินงาน  |   สิทธิ์การใช้สินทรัพย์      |

เมื่อการชำระเงินเปลี่ยนแปลงเนื่องจากการเปลี่ยนแปลงในอัตราดัชนี เฉพาะการชำระเงินผันแปรเท่านั้นที่จะเปลี่ยน เว้นแต่มีการเปลี่ยนแปลงเพิ่มเติมของกระแสเงินสด เช่น การเปลี่ยนแปลงระยะเวลาของสัญญาเช่าที่เกี่ยวข้องกับอัตราดอกเบี้ยภายใต้ US GAAP ASC 842

#### <a name="lease-adjustment"></a>การปรับปรุงสัญญาเช่า
การเช่าสินทรัพย์จะช่วยให้คุณสามารถปรับปรุงการเช่าได้หากมีการปรับเปลี่ยนระยะเวลาของสัญญาเช่า การเช่าจะถูกขยาย หรือหากมีกรณีเพิ่มเติมที่การเช่าต้องมีการปรับปรุง มีการลงรายการบัญชีการปรับปรุงการเช่าเพื่อเพิ่มหรือลดสิทธิ์การใช้สินทรัพย์และหนี้สินสัญญาเช่า กระบวนการปรับปรุงใช้ carryover ยอดดุลสิ้นงวดของการการตัดบัญชีหนี้สินและยอดดุลสินทรัพย์ ณ วันที่ปรับปรุง เมื่อมีการเชื่อมโยงการเช่ากับสินทรัพย์ถาวร การปรับปรุงสิทธิ์การใช้สินทรัพย์จะมีการลงรายการบัญชีโดยใช้รหัสที่กำหนดไว้ในสินทรัพย์ถาวร 

|     ชนิดข้อมูล                                          |     เดบิต                             |     เครดิต                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   รายการการปรับปรุงการเช่าสำหรับ IFRS และ US GAAP ในกรณีที่มีการเพิ่มขึ้น     |  สิทธิ์การใช้สินทรัพย์       |   หนี้สินสัญญาเช่าดำเนินงาน |
|   รายการการปรับปรุงการเช่าสำหรับ IFRS และ US GAAP ในกรณีที่มีการลดลง     |  หนี้สินสัญญาเช่าดำเนินงาน  |   สิทธิ์การใช้สินทรัพย์      |


#### <a name="lease-impairment"></a>การด้อยค่าของสินทรัพย์ที่เช่า
การทำเช่นนี้แสดงถึงการลดยอดดุลของสิทธิ์การใช้สินทรัพย์ ระบุยอดการด้อยค่าของสินทรัพย์ วันที่ธุรกรรม และรอบระยะเวลาที่เหลือ สิทธิ์การใช้สินทรัพย์ที่เหลืออยู่จะถูกตัดให้สั้นลงแบบเส้นตรง ตรรกะการด้อยค่าของสินทรัพย์พิจารณาค่า carryover ของสินทรัพย์ที่มีอยู่ในกำหนดการการคิดค่าเสื่อมราคาสินทรัพย์  

|     ชนิดข้อมูล                                          |     เดบิต                             |     เครดิต                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   รายการการด้อยค่าของสินทรัพย์สำหรับ IFRS และ US GAAP           |  ค่าใช้จ่ายการด้อยค่าของสินทรัพย์                   |    สิทธิ์การใช้สินทรัพย์     |

>[!NOTE]
> ถ้าการเช่าเชื่อมโยงกับสินทรัพย์ถาวร ควรมีการลงรายการบัญชีการด้อยค่าของสิค่าเช่าจากสินทรัพย์ถาวร เนื่องจากมีการรันการคิดค่าเสื่อมราคาสินทรัพย์จากโมดูลสินทรัพย์ถาวร

**สกุลเงินแบบคู่** สามารถลงรายการบัญชีธุรกรรมการเช่าในสกุลเงินอื่นที่ไม่ใช่สกุลเงินการลงบัญชีและการรายงาน อัตราแลกเปลี่ยนสกุลเงินจะกำหนดในบัญชีแยกประเภททั่วไปในวันที่เริ่มต้น คุณสามารถเปลี่ยนอัตราแลกเปลี่ยนได้โดยการตั้งค่าฟิลด์ **อัตราคงที่** เป็น **ใช่** เมื่อคุณสร้างการเช่า เมื่อคุณป้อนธุรกรรมการให้เช่า ธุรกรรมการรับรู้เริ่มต้นและธุรกรรมค่าเสื่อมราคาในเวลาต่อมาจะใช้อัตราแลกเปลี่ยน ณ วันที่เริ่มต้น ธุรกรรมการชำระเงินและดอกเบี้ยในเวลาต่อมา จะใช้อัตราแลกเปลี่ยนปัจจุบันที่ใช้งานอยู่ 

## <a name="create-an-asset-lease"></a>สร้างการเช่าสินทรัพย์
ดำเนินขั้นตอนต่อไปนี้เพื่อสร้างการเช่าใหม่ 

1. เมื่อต้องการใช้ **การเช่าสินทรัพย์** คุณต้องเปิดใช้งานในพื้นที่ทำงาน **การจัดการคุณลักษณะ** จากพื้นที่ทำงาน **การจัดการคุณลักษณะ** เลือก **ทั้งหมด** เพื่อให้คุณลักษณะทั้งหมดแสดงรายการอยู่บนหน้า เลือก **การเช่าสินทรัพย์** และจากนั้นเลือก **เปิดใช้งานตอนนี้**
2. ไปที่ **การเช่าสินทรัพย์ > ทั่วไป > สรุปการเช่า** ป้อนค่าฟิลด์ที่จำเป็นในแท็บด่วน **ทั่วไป** 
   - **รายละเอียดสัญญาเช่า**
   - **อายุการใช้งานของสินทรัพย์ (เดือน)**
   - **กลุ่มสัญญาเช่า**
   - **อัตราดอกเบี้ยเงินกู้ส่วนเพิ่ม (%)**
   - **ช่วงเวลาการทบต้น**
   - **ชนิดเงินรายปี**
   - **สกุลเงิน**
   - **วันที่เริ่มต้น**

3. เลื่อนไปที่แท็บด่วน **บรรทัดกำหนดการชำระเงิน** แล้วป้อนบรรทัดการชำระเงิน จากนั้นเลือก **สร้างกำหนดการ**

4. เลือก **สมุดบัญชี** 

5. สลับไปยังแท็บด่วน **ทั่วไป** **สิทธิ์การใช้สินทรัพย์** และ **หนี้สินสัญญาเช่า** จะถูกคำนวณ 

6. ย้ายไปที่แท็บด่วน **การทดสอบการจัดประเภทการเช่า** เพื่อตรวจสอบค่าในฟิลด์ **ชนิดการเช่า** 

   **ชนิดของการเช่า** แบบอัตโนมัติ จะถูกจัดประเภทตามเงื่อนไขที่กำหนดไว้ในหน้า **สมุดบัญชี**

7.  ไปที่ **กำหนดการชำระเงิน** ภายใต้ส่วน **ฟังก์ชัน**  

   หน้า **กำหนดการชำระเงิน** จะแสดงรายการกำหนดการชำระเงินในอนาคตสำหรับรหัสการเช่า เลือก **ยืนยันกำหนดการ** เพื่อให้สามารถลงรายการบัญชีธุรกรรม **การรับรู้เริ่มต้น** ได้ 

[![ฟังก์ชันการรับรู้เริ่มต้น](./media/overview-13.png)](./media/overview-13.png)

8. เลือก **การรับรู้เริ่มต้น** เพื่อสร้างสมุดรายวันการรับรู้เริ่มต้น 

9. เลือก **สมุดรายวันการเช่าสินทรัพย์** ที่จะลงรายการบัญชีธุรกรรมการรับรู้เริ่มต้น 

   จากกำหนดการชำระเงิน คุณสามารถเปิดหน้ารายละเอียดที่แสดงรายการธุรกรรมสิทธิ์การใช้สินทรัพย์ 
 
   **กำหนดการการตัดบัญชีหนี้สินสัญญาเช่า** แสดงยอดดอกเบี้ยที่คำนวณได้สำหรับแต่ละรอบระยะเวลา
   
10. สร้างสมุดรายวัน แล้วไปที่ **สมุดรายวันการเช่าสินทรัพย์** **กำหนดการตัดบัญชีหนี้สินสัญญาเช่า** ยังแสดงในธุรกรรมดอกเบี้ย

   หน้า **กำหนดการคิดค่าเสื่อมราคาสินทรัพย์** แสดงธุรกรรมค่าเสื่อมราคาสำหรับรหัสการเช่าที่เลือก 

   [![หน้าธุรกรรมสินทรัพย์ ROU](./media/overview-20.png)](./media/overview-20.png)

   หน้า **ธุรกรรมสินทรัพย์ ROU** แสดงรายการการรับรู้เริ่มต้น ต้นทุนค่าเสื่อมราคาสะสม และยอดดุลสินทรัพย์ 

   หน้า **ธุรกรรมหนี้สินสัญญาเช่า** แสดงการรับรู้เริ่มต้น การชำระเงินดอกเบี้ยค่าเช่า ชำระเงินค่าเช่า และยอดดุลของหนี้สินสัญญาเช่า 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
