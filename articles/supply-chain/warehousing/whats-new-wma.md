---
title: มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงในแอป Warehouse Management บนอุปกรณ์เคลื่อนที่
description: บทความนี้จะแสดงรายการคุณลักษณะใหม่และคุณลักษณะที่เปลี่ยนแปลงของแอป Warehouse Management บนมือถือแต่ละรุ่นที่ปล่อยของ Microsoft Dynamics 365 Supply Chain Management
author: Mirzaab
ms.date: 04/25/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61d3ebc85d3c3d20bb17acd7364adc04cd2f3f94
ms.sourcegitcommit: e9000d0716f7fa45175b03477c533a9df2bfe96d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/13/2022
ms.locfileid: "9843692"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงในแอป Warehouse Management บนอุปกรณ์เคลื่อนที่

[!include [banner](../includes/banner.md)]

บทความนี้จะแสดงรายการคุณลักษณะ การแก้ไข การปรับปรุง และปัญหาที่พบใหม่ของแอป Warehouse Management บนมือถือแต่ละรุ่นที่ปล่อยของ Microsoft Dynamics 365 Supply Chain Management

## <a name="version-20390"></a>รุ่น 2.0.39.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:
- เสถียรภาพที่เพิ่มขึ้น 
- ฟิลด์ของหน้า **กำหนดเอง** จะไม่มีการจัดเรียงโดยอัตโนมัติอีกต่อไป ตามการตั้งค่าระดับความสำคัญหลักและระดับความสำคัญย่อยของฟิลด์เหล่านี้  
- ขณะนี้ แอปนี้ใช้การตั้งค่าระดับความสำคัญหลักและระดับความสำคัญย่อยของแต่ละฟิลด์เพื่อระบุฟิลด์หลักของหน้า ฟิลด์หลักจะแสดงอยู่ในฟิลด์ส่วนหัวของขั้นตอน 
- แก้ไขปัญหาที่คีย์บอร์ดภายในไม่ได้ซ่อนบน Android
- แก้ไขปัญหาที่สปินเนอร์ปริมาณแสดงค่าที่ถูกต้องไม่ถูกต้องในการเปิดในโฟลว์ *การย้าย* 
- แก้ไขปัญหาที่ค่าสปินเนอร์ปริมาณแบบอ่านอย่างเดียวไม่มีศูนย์กลางอย่างถูกต้อง 
- แก้ไขปัญหาที่เว็บเพจไม่เปิดจากหน้า **เกี่ยวกับ** 
- ธีมสี *อัตโนมัติ* จะมีลักษณะเริ่มต้น (อ่อนหรือเข้ม) ตามธีมสากลที่ตั้งค่าในระบบปฏิบัติการของอุปกรณ์เคลื่อนที่

## <a name="version-20370"></a>รุ่น 2.0.37.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:
- เพิ่มการตั้งค่าผู้ใช้ที่ผู้อนุญาตให้ผู้ปฏิบัติงานเลือกว่าแอปจะแสดงรูปภาพผลิตภัณฑ์ (ทั้งในส่วนหัวของบัตรและขั้นตอน เฉพาะในส่วนหัวของขั้นตอนเท่านั้น หรือไม่แสดงเลย) 
- ปรับปรุงโครงร่างหน้าจอบัตรรายละเอียดให้ดีขึ้นโดยลดขนาดของแบนเนอร์ขั้นตอน และสปินเนอร์อินพุตปริมาณ ซึ่งให้พื้นที่เพิ่มเติมเหลือไว้ของเนื้อหาอื่นๆ 
- ปรับปรุงอินเทอร์เฟสผู้ใช้เมื่อรันบนอุปกรณ์ Honeywell Thor 
- โหมดเต็มหน้าจอที่ปรับปรุงแล้ว (ใช้กับอุปกรณ์ที่มีคีย์บอร์ดฮาร์ดแวร์เท่านั้น) 
- ผลลัพธ์ที่ปรับปรุงเมื่อเรียงลำดับบัตรรายละเอียดและหน้าแบบกำหนดเองตามระดับความสำคัญหลัก หรือระดับความสำคัญรอง (DataPriority หรือ DisplaySubPriority) 
- เพิ่มการสนับสนุนให้กับภาษาอื่นๆ 
- เสถียรภาพที่ดีขึ้น 
- รูปภาพและไอคอนหลายที่ปรับปรุง 

## <a name="version-20350"></a>รุ่น 2.0.35.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:
- แก้ไขปัญหาสำหรับ Android ในกรณีแอปพลิเคชันจะขัดข้องถ้าหน้า **รายการงาน** ถูกเปิดขึ้นเมื่อไม่มีบัตรใดๆ แสดง

## <a name="version-20340"></a>รุ่น 2.0.34.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:
- เสถียรภาพที่ดีขึ้น
- ปรับปรุงประสิทธิภาพการทำงาน
- ปรับปรุงโครงร่างหน้าจอเพื่อให้มีพื้นที่ว่างมากขึ้นในบัตรรายละเอียด
- เพิ่มฟังก์ชัน search ที่หน้า **รายการงาน** ขณะนี้ ผู้ปฏิบัติงานสามารถสแกนหรือพิมพ์เพื่อค้นหาในฟิลด์และชื่อทั้งหมดบนหน้า
- ขณะนี้รายการการเชื่อมต่อที่พร้อมใช้งานเรียงลำดับตามตัวอักษร
- แก้ไขปัญหาที่มีการแสดงบัตรที่ซ้ำกันของสินค้าที่มีสถานะสินค้าคงคลังหลายสถานะที่สถานที่เดียวกัน
- แก้ไขปัญหาที่หน้า **รายการตัวเลือกขนาดใหญ่** ไม่ได้เลื่อนเพื่อแสดงสินค้าที่เลือกล่วงหน้า
- แก้ไขสีของแถบการค้นหาในหน้า **รายการตัวเลือกขนาดใหญ่**
- แก้ไขปัญหาที่ปุ่มเริ่มต้นที่กําหนดไว้ใน XML ไม่ได้ใช้เป็นปุ่มส่ง
- แก้ไขปัญหาที่ปุ่มในการสแกนหลายสแกนและโฟลว์การตรวจสอบความถูกต้องด่วนไม่ได้รับการอัปเดตเมื่อมีการสแกนรหัสใหม่
- เพิ่มการสนับสนุนให้กับภาษาอื่นๆ

## <a name="version-20320"></a>รุ่น 2.0.32.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- เสถียรภาพที่ดีขึ้น

## <a name="version-20310"></a>รุ่น 2.0.31.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

-   ประสิทธิภาพและเสถียรภาพขั้นสูง
-   อินเทอร์เฟสผู้ใช้ที่ปรับปรุง ช่วยให้ใช้งานรายการเลือกยาวได้เร็วขึ้นและง่ายขึ้น ขณะนี้ผู้ปฏิบัติงานสามารถค้นหารายการตามชื่อ แทนที่จะเลื่อนผ่านรายการทั้งหมด
-   แก้ไขปัญหาที่ค่าที่ป้อนไว้ล่วงหน้าถูกเขียนทับเมื่อสแกนตามอักขระ

## <a name="version-20300"></a>รุ่น 2.0.30.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- เสถียรภาพที่ดีขึ้น

## <a name="version-20280"></a>รุ่น 2.0.28.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- เสถียรภาพที่ดีขึ้น
- แนะนำความสามารถในการสแกนต่อไปแม้ในขณะที่กล่องโต้ตอบข้อผิดพลาดแสดงบนหน้าจอ
- การสนับสนุนเพิ่มเติมของ ASCII 10 ในบาร์โค้ด
- ปรับปรุงการใช้งานกล่องโต้ตอบคำแนะนำขั้นตอน
- แก้ไขปัญหาที่ในบางครั้งสามารถแสดงหน้าจอว่าง
- แก้ไขปัญหาที่รายการงานเลื่อนอย่างไม่ถูกต้องเมื่อใช้งานบน Microsoft Windows

## <a name="version-20250"></a>รุ่น 2.0.25.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- ประสิทธิภาพที่เพิ่มขึ้น
- เสถียรภาพที่เพิ่มขึ้น
- ปรับปรุงหน้า **การสอบถาม** เพื่อให้รองรับข้อความที่ยาวขึ้นในหัวข้อย่อย
- แนะนำความสามารถในการยกเลิกขั้นตอนในทันทีด้วยการแตะหรือคลิกเพียงครั้งเดียว (เมื่อ **ยกเลิก** เป็นการดำเนินการเดียวที่มีอยู่ภายใต้ **การดำเนินการเพิ่มเติม**)
- แก้ไขปัญหาที่บางครั้งโฟกัสอาจหายไประหว่างตัวควบคุมรายการในหน้า **แก้ไขการเชื่อมต่อ** และหน้าที่กำหนดเอง
- แก้ไขปัญหาที่บางครั้งปุ่มกลายเป็นไม่ตอบสนองและจะยังคงแสดงเป็น เลือกไว้ เมื่อรวมอยู่ในมุมมองการเลื่อน
- แก้ไขปัญหาที่บางครั้งสามารถใช้เค้าโครงที่ไม่ถูกต้องในหน้าหลักได้

## <a name="version-20240"></a>รุ่น 2.0.24.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- หน้าสแกนเนอร์ที่ปรับปรุงแล้วเพื่อเปิดใช้งานตัวเลือกการสแกนบนหน้า **รายละเอียด**
- ท่าทางสัมผัสที่ปรับปรุงแล้ว เช่น หน้าจอสัมผัส/หน้าจอแตะ
- ปัญหาประสิทธิภาพที่ปรับปรุงแล้วของ Android
- การจัดวางส่วนหัวหลายหัวข้อคงที่เพื่อให้บัตรเพิ่มเติมแสดงบนหน้า **การสอบถาม** ได้
- การเลื่อนที่ปรับปรุงแล้วเพื่อให้ระยะการเลื่อนเลื่อนน้อยลงจึงเปิดใช้งาน
- การกดค้างที่เพิ่มเพื่อแสดงข้อความเพิ่มเติมในหน้า **การสอบถาม**
- ข้อมูลรหัสอุปกรณ์ที่ขาดหายไปแบบคงที่ของ Android
- เสถียรภาพที่เพิ่มขึ้น
- จัดโครงร่างการเข้าสู่ระบบให้เหมาะสม
- เพิ่มปัดด้านขวาเพื่อปิดหน้าป๊อปอัพกล่องโต้ตอบบนแป้นกดหมายเลข หน้า **รายละเอียด** และหน้าป้อนข้อมูล

## <a name="version-20220"></a>รุ่น 2.0.22.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- แก้ไขปัญหาระบบขัดข้องหลายอย่าง
- แก้ไขปัญหาที่อักขระบางตัวไม่เป็นที่รู้จักเมื่อสแกนหรือพิมพ์บนหน้าเริ่มต้น
- แก้ไขปัญหาที่การพิมพ์แบ็คสเปซในหน้าเริ่มต้นจะลบอักขระสองตัวพร้อมกัน
- แก้ไขปัญหาที่ฟิลด์ **เรียงลำดับตาม** บนหน้า **รายการงาน** แสดงค่าที่ไม่ถูกต้อง โดยไม่สอดคล้องกับลำดับการจัดเรียงที่แท้จริงของการ์ด
- แก้ไขปัญหาที่แสดงโครงร่างไม่ถูกต้องหลังจากปรับขนาดหน้าต่างแอปในขณะที่ทำงานอยู่บน Microsoft Windows
- แก้ไขปัญหาที่การเลื่อนรายการในรายการป๊อปอัพอาจส่งผลให้สินค้าบางรายการที่เหลือถูกซ่อนหรือบิดเบี้ยว
- ออกแบบหน้าการลงชื่อเข้าใช้ใหม่เพื่อให้แสดงฟิลด์ชื่อผู้ใช้และรหัสผ่านในหน้าเดียวกันเมื่อเรียกใช้บนจอแสดงผลที่มีขนาดใหญ่กว่า
- ปรับปรุงวิธีที่การควบคุมตอบสนองต่อการแตะอย่างรวดเร็ว
- เพิ่มมุมมองบันทึกข้อผิดพลาดในแอป
- เพิ่มการปรับปรุงความสามารถในการเข้าถึงหลายอย่าง (ปรับปรุงคำบรรยาย แก้ไขตัวยึดที่ขาดหายไปบน Android เปิดใช้งานการป้อนข้อมูลด้วยคีย์บอร์ดสำหรับการควบคุมแถบเลื่อน และอื่นๆ)

## <a name="version-20200"></a>รุ่น 2.0.20.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- แก้ไขปัญหาระบบขัดข้องหลายอย่าง
- แก้ไขปัญหาที่จะแสดงค่าที่ไม่ถูกต้องบนบัตรในหน้า **รายการงาน**
- ปรับปรุงประสบการณ์การเลื่อนและการตัดปัญหาการเลื่อนในหน้า **รายการงาน** และ **การสอบถามรายการ** ใน Android
- เพิ่มปุ่มออกในหน้าลงชื่อเข้าใช้ ซึ่งใช้ในการออกจากแอปพลิเคชัน

## <a name="version-20190"></a>รุ่น 2.0.19.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- ปรับปรุงขั้นตอนการสอบถามข้อมูลทั่วไป
- ปรับปรุงปัญหาเล็กน้อยในหน้า **รายการงาน** และ **การสอบถามข้อมูล**
- ลดการใช้แบตเตอรี่
- ขจัดขีดจํากัดของจํานวนฟิลด์ของบัตรงาน
- ปรับปรุงความสูงของบัตรงานเพื่อให้บัตรงานทั้งหมดมีขนาดเดียว โดยไม่พิจารณาจํานวนฟิลด์ในบัตรแต่ละใบ
- แก้ไขปัญหาอักขระช่องว่างในบาร์โค้ดถูกตัดออก
- เพิ่มการตั้งค่า **ลักษณะปุ่ม** ซึ่งช่วยให้คุณสลับระหว่างมุมมองของแถบเลื่อนกับมุมมองปุ่มได้บนอุปกรณ์ทุกชนิด
- แก้ไขปัญหาต่างๆ ที่อาจเป็นสาเหตุให้แอปขัดข้อง
- ตั้งค่าโฟกัสอัตโนมัติบนกล่องข้อความแรกในหน้าที่กำหนดเอง
- การปรับปรุงความสามารถในการเข้าถึงที่เกี่ยวข้องกับความสว่าง ความคมชัด การบรรยาย และข้อความตัวยึดที่ขาดหายไป

## <a name="version-20170"></a>รุ่น 2.0.17.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- แก้ไขปัญหาที่บาร์โค้ดถูกสแกนอย่างไม่ถูกต้อง
- แก้ไขปัญหาการสแกน GS1 ของกล้องสแกนเนอร์
- แก้ไขปัญหาการสแกน GS1 ของเครื่องสแกนบาร์โค้ดในอุปกรณ์ Zebra
- ปรับปรุงขั้นตอนการสอบถามการข้ามตำแหน่ง ดังนั้นการเลือกบัตรในการข้ามตำแหน่งจะกลับไปยังขั้นตอนหลัก
- เพิ่มการสนับสนุนขั้นตอนการสอบถามข้อมูลทั่วไป
- เพิ่มข้อความเพื่อแจ้งให้ผู้ใช้ทราบเกี่ยวกับการเปลี่ยนแปลงสถานะการเชื่อมต่อเครือข่าย
- ปรับสิทธิ์ในที่เก็บข้อมูลให้สอดคล้องกับนโยบายความเป็นส่วนตัวของที่เก็บข้อมูลใน Android 10
- สำหรับขั้นตอนที่ต้องการ ตอนนี้สปินเนอร์ปริมาณมีตําแหน่งที่ช่วยให้ผู้ใช้สามารถส่งค่าตัวเลขที่ว่างเปล่าได้
- แก้ไขปัญหาการวางแนวสปินเนอร์ปริมาณ
- แก้ไขปัญหาที่สปินเนอร์ปริมาณจะข้ามไปยังค่าที่ไม่ถูกต้อง
- แก้ไขปัญหาที่การป้อนข้อมูลไปยังหน้าหลักจะหายไป เมื่อเติมข้อมูลจากหน้ารายละเอียด
- แก้ไขปัญหาที่ข้อความตัวยึดจะถือเป็นค่าที่เลือกครั้งแรกในรายการเลือก
- ตอนนี้ปุ่ม "ส่ง" ในขั้นตอนการยืนยันจะเปิดใช้งานโดยอัตโนมัติ หากมีการเลือกค่าไว้ล่วงหน้า
- แก้ไขบัตรรายละเอียดที่จะแสดงบรรทัดให้มากที่สุดเท่าที่จะเป็นไปได้ของฟิลด์ข้อความที่มีหลายบรรทัด
- แก้ไขความสูงของปุ่ม "ส่ง" และ "การดำเนินการเพิ่มเติม" ดังนั้นขณะนี้ผู้ใช้จึงใช้พื้นที่น้อยลงบนหน้าจอ
- เพิ่มชื่อรายการเลือกที่หายไป
- แก้ไขปัญหาที่ปุ่มย้อนกลับไม่ทำงาน
- เพิ่มการแก้ไขและการปรับปรุงการนําทางบนคีย์บอร์ดหลายอย่าง รวมถึงบนหน้าต่อไปนี้
  - การเข้าสู่ระบบของผู้ใช้
  - เลือกการเชื่อมต่อ
  - แก้ไขการเชื่อมต่อ
- แก้ไขการเลื่อนเมื่อใช้การนําทางบนคีย์บอร์ด
- ปรับปรุงการเข้าถึงขั้นสูง รวมถึงการปรับปรุงต่อไปนี้
  - แก้ไขการมองเห็นสีและความคมชัด
  - ป้องกันการเสียโฟกัสจากคีย์บอร์ดเมื่อปิดหน้าป็อปอัพ
  - เพิ่มข้อความแสดงข้อผิดพลาดให้กับคำบรรยาย
  - เพิ่มขนาดของค่าตัวยึดในแบนเนอร์ขั้นตอน
- แก้ไขตัวอย่างของหน้าดั้งเดิมที่กำหนดเองในโหมดสาธิต

## <a name="version-20150"></a>รุ่น 2.0.15.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- ปรับปรุงประสิทธิภาพโดยการแก้ไขปัญหาหน่วยความจำรั่วไหล
- แก้ไขปัญหาที่ค่าฟิลด์บางค่าไม่ได้รับการอัปเดตอย่างถูกต้องเมื่อเลือกในหน้ารายละเอียด

## <a name="version-20140"></a>รุ่น 2.0.14.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- แก้ไขปัญหาที่ปิดใช้งานปุ่มส่งค่าเริ่มต้น

## <a name="version-20130"></a>รุ่น 2.0.13.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- ปรับปรุงการเลื่อนระหว่างหน้าต่างๆ ให้เคลื่อนไหวราบรื่นขึ้น
- การตอบสนองแบบตอบกลับแบบคงที่ในการปัดและหน้าจอหยุดค้างเป็นครั้งคราว
- ปรับปรุงข้อความโหมดมืดและชุดสีพื้นหลังเพื่อความสามารถในการอ่านที่ดีขึ้น
- แก้ไขปัญหาที่ข้อความบางข้อความอาจเล็กมากเมื่อปรับขนาดหน้าต่างแอปใหม่
- แก้ไขปัญหาที่อาจทําให้แอปขัดข้องเป็นบางครั้งเมื่อสแกนบาร์โค้ด
- เพิ่มความเป็นไปได้ในการเปลี่ยนตัวเลื่อนเป็นปุ่ม
- แก้ไขปัญหาที่อาจทําให้แอปแสดงข้อความแสดงข้อผิดพลาด "AADSTS7000215: มีการระบุข้อมูลลับของไคลเอ็นต์ที่ไม่ถูกต้อง"
- แก้ไขภาพเคลื่อนไหวคำแนะนำที่แสดงวิธีการปิดหน้าโดยใช้รูปแบบการปัดนิ้วลง
- เพิ่มความเป็นไปได้ในการปิดหน้าโดยใช้รูปแบบการตวัดนิ้วลง
- แก้ไขปัญหาที่ชื่อรายการแบบหล่นลงไม่แสดงบนหน้า **การตั้งค่าของผู้ใช้**
- แก้ไขปัญหาการแปลเป็นภาษาท้องถิ่นซึ่งแอปไม่สามารถรับรู้เครื่องหมายจุลภาค (,) เป็นตัวแบ่งทศนิยม
- ความสามารถในการเข้าถึงที่ดีขึ้น
- แก้ไขการนําทางในหน้า **การเชื่อมต่อใหม่** เพื่อให้ความสามารถในการเข้าถึงที่ดีขึ้น
- แก้ไขปัญหาที่คีย์บอร์ดภายใน (บนหน้าจอ) ไม่ปรากฏขึ้นเมื่อเลือกฟิลด์ป้อนข้อมูล
- แก้ไขปัญหาที่อาจทำให้แอปขัดข้องหากผู้ใช้ปรับขนาดหน้าต่างอย่างรวดเร็ว
- แก้ไขปัญหาที่บางครั้งการกดแป้นพิมพ์แบบเร็วๆ ถูกตีความเป็นการกดค้าง
- แก้ไขปัญหาที่โครงร่างแอปอาจเสียหายได้เนื่องจากการปรับแต่งฟิลด์ที่ที่ทำใน Supply Chain Management
- แก้ไขปัญหาที่สถานที่สินค้าแสดงไม่ถูกต้อง
- แก้ไขปัญหาเกี่ยวกับการเบิกสินค้าที่ขาดสำหรับลำดับงานของผลิตภัณฑ์ย่อย
- เอาการตรวจสอบความถูกต้องของฟิลด์ที่มีค่าเริ่มต้นที่กําหนดล่วงหน้าโดยไม่จําเป็นออก
- ปรับปรุงประสิทธิภาพการทำงาน
- เพิ่มการตั้งค่าใหม่ที่ช่วยให้ผู้ใช้สามารถเลือกวิธีการกรองและจัดลำดับฟิลด์ในหน้าบัตร

## <a name="version-20110"></a>รุ่น 2.0.11.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- การสนับสนุนที่เพิ่มให้กับฟิลด์ที่เลื่อนระดับ
- การสนับสนุนที่เพิ่มให้กับการนําทางคีย์บอร์ดฮาร์ดแวร์
- ความสามารถในการเข้าถึงที่ดีขึ้น
- บัตรรายละเอียดขั้นสูง
- การข้ามตำแหน่งขั้นสูงของขั้นตอนรายการเมนู
- การปรับปรุงอินเทอร์เฟสผู้ใช้รอง
- แก้ไขปัญหาที่อาจทําให้แอปขัดข้องเมื่อสแกนบาร์โค้ด
- แก้ไขปัญหาต่างๆ ที่อาจเป็นสาเหตุให้ระบบหยุดตอบสนอง

## <a name="version-20100"></a>รุ่น 2.0.10.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- ภาพเคลื่อนไหวที่เพิ่มเมื่อเลื่อนผ่านรายการและหน้า
- ขณะนี้ข้อความตัดอย่างถูกต้องในหน้าข้อผิดพลาดการเชื่อมต่อ
- ขณะนี้กล่องคำสั่งผสมที่ไม่มีค่าเริ่มต้นแสดงอย่างถูกต้อง
- ขณะนี้ข้อมูลในพื้นที่หัวข้อย่อยแสดงอยู่ในหน้ารายละเอียดทั้งหมดเท่านั้น
- ฟิลด์ป้อนข้อมูลว่างเปล่าจะไม่แสดงบนบัตรรายละเอียดอีกต่อไป
- ค่าการยืนยันจะไม่ซ้ำบนบัตรรายละเอียดอีกต่อไป
- แก้ไขปัญหาต่างๆ ที่เป็นสาเหตุให้ระบบหยุดตอบสนอง

## <a name="version-2090"></a>รุ่น 2.0.9.0

รุ่นนี้จะแก้ไขปัญหาที่แอปสามารถหยุดตอบสนองถ้าหน้าผู้ใช้ขึ้นจากด้านบนของรายการ

## <a name="version-2080"></a>รุ่น 2.0.8.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- การสนับสนุนที่เพิ่มสำหรับ [คุณลักษณะคําแนะนำตามขั้นตอน](mobile-app-titles-instructions.md) ที่แนะนําใน Supply Chain Management รุ่น 10.0.21
- ภาพเคลื่อนไหวข้อแนะนำที่เพิ่มเพื่อแสดงผู้ใช้ว่าผู้ใช้สามารถปิดการมีทับซ้อนได้โดยการเลื่อนลง
- การสนับสนุนที่เพิ่มให้กับคีย์ฟังก์ชันในรายการการดำเนินการและเมนู ผู้ใช้สามารถกดปุ่มฟังก์ชันใดๆ เป็นเวลาสามวินาทีเพื่อเข้าดูรายการของการสั่งที่พร้อมใช้งานได้
- แก้ไขปัญหาที่เป็นสาเหตุให้ข้อความแสดงข้อผิดพลาดต่อไปนี้แสดงบนบางอุปกรณ์: "ไม่พบมุมมองที่เหมาะสมของขนาดที่ระบุ"
- แก้ไขปัญหาที่โหมดเต็มหน้าจอไม่สามารถใช้งานได้เสมอเมื่อมีการใช้คีย์บอร์ดบนหน้าจอ
- แก้ไขปัญหาที่การเลื่อนหน้าไม่ทำงานบนอุปกรณ์ Windows
- แก้ไขปัญหาต่างๆ ที่เป็นสาเหตุให้ระบบหยุดตอบสนอง

## <a name="version-2070"></a>รุ่น 2.0.7.0

### <a name="new-features-fixes-and-improvements-in-version-2070"></a>คุณลักษณะใหม่ การแก้ไข และการปรับปรุงในรุ่น 2.0.7.0

- เพิ่มส่วนไปยังหน้า **เกี่ยวกับ** ที่ตรวจสอบแอปรุ่นล่าสุด
- ทําให้การตวัดและปัดระหว่างหน้าทําได้ง่ายขึ้น
- เปลี่ยนไอคอนสําหรับปุ่มจากน้อยไปมาก/มากไปหาน้อยในรายการงาน
- ลดระยะขอบบนบัตร **รายละเอียด** เพื่อให้พอดีกับข้อมูลเพิ่มเติม
- ใช้การปรับปรุงประสิทธิภาพต่าง ๆ เพื่อลดปัญหาของแอปให้ช้าลงเมื่อเวลาผ่านไป
- ถ้ามีตัวควบคุมมากกว่าขนาดที่พอดีกับหน้าจอ ส่งผลให้มีการแบ่งหน้า ตัวควบคุมสปินเนอร์จะไม่เลื่อนไปทางเดียวกับเพจอีกต่อไป
- จัดลําดับความสําคัญในการแสดงค่าที่สแกนล่าสุดมากกว่าการแสดงชื่องาน ดังนั้นถ้าค่าแสกนทับซ้อนกัน ชื่องานจะถูกตัดออก
- แก้ไขปัญหาต่างๆ ที่เป็นสาเหตุให้ระบบหยุดตอบสนอง
- ข้อความในสถานที่ต่าง ๆ จะไม่ถูกตัดออกในบางภาษาอีกต่อไป
- ตอนนี้แอปทํางานในโหมดเต็มหน้าจอตามค่าเริ่มต้น
- แก้ไขปัญหาที่บางครั้งอาจทําให้การสแกนถูกเพิกเฉยในหน้าหลักกับอุปกรณ์บางชนิด

### <a name="known-issues-in-version-2070"></a>ปัญหาที่ทราบในรุ่น 2.0.7.0

- ในอุปกรณ์บางอย่าง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้เมื่อคุณเริ่มแอปหรือเริ่มงาน: "ไม่พบมุมมองที่เหมาะสมสําหรับขนาดที่ระบุ" หากคุณเห็นข้อความแสดงข้อผิดพลาดนี้บนอุปกรณ์ใด ๆ ของคุณ คุณต้องดาวน์เกรดแอป Warehouse Management บนมือถือเป็นรุ่น 2.0.6.0 บนอุปกรณ์นั้นและรออัปเกรดจนกว่าจะมีการเปิดตัวแอปรุ่นถัดไป

## <a name="version-2060"></a>รุ่น 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>คุณลักษณะใหม่ การแก้ไข และการปรับปรุงในรุ่น 2.0.6.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- ตอนนี้ โหมดสาธิตจะแสดงป้ายชื่อทั้งหมดในภาษาของอุปกรณ์
- คุณมีโอกาสน้อยที่จะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ไม่พบมุมมองที่เหมาะสมเกี่ยวกับขนาดที่ระบุ"
- เพิ่มความสูงต่ำสุดของบัตรงานแล้ว (ในกรณีที่มีการตั้งค่าคอนฟิกฟิลด์สามฟิลด์ขึ้นไปให้ปรากฏในรายการงาน)
- ปรับปรุงค่าเผื่อ (เลือน) ที่ด้านล่างของบัตรรายละเอียดแล้ว
- ขณะนี้สัญลักษณ์ในไฟล์ XML ที่ถูกแลกเปลี่ยนกับเซิร์ฟเวอร์ได้รับการจัดการอย่างง่ายดาย (ตัวอย่างเช่น ขณะนี้การจัดการอักขระที่ไม่สามารถพิมพ์ได้แสดงขึ้นในขณะนี้จะไม่ทําให้แอปหยุดตอบสนองอีกต่อไป)
- ข้อผิดพลาด HTTP (เช่น "ข้อผิดพลาด 503") เมื่อส่งคำขอเซิร์ฟเวอร์ได้รับการจัดการอย่างง่ายดายแล้วในขณะนี้
- ในขณะที่มีข้อผิดพลาดแสดงอยู่ รายการตัวเลือกจะไม่แสดงขึ้นโดยอัตโนมัติอีกต่อไปในตัวควบคุมกล่องคำสั่งผสม
- แอปไม่หยุดตอบสนองอีกต่อไปเนื่องจากการวางแนวการแสดงผลที่เลือกไว้ในการตั้งค่าผู้ใช้
- ขณะนี้ รูปภาพผลิตภัณฑ์จะแสดงอยู่ในสภาพแวดล้อมระบบบริการตนเอง (การเปลี่ยนแปลงนี้จะใช้กับรุ่นความละเอียดต่ำเท่านั้น บริการจัดการไฟล์ไม่สนับสนุนรูปภาพขนาดเต็มในสภาพแวดล้อมระบบบริการตนเอง)
- ปัญหาที่เกี่ยวข้องการเบิกสินค้าที่ขาดที่เป็นปริมาณศูนย์ถูกแก้ไขแล้ว
- แอปไม่หยุดตอบสนองอีกต่อไปเมื่อบัตรรายละเอียดแสดงฟิลด์ที่เหมือนกันหลายฟิลด์

### <a name="known-issues-in-version-2060"></a>ปัญหาที่ทราบในรุ่น 2.0.6.0

เกิดปัญหาที่ทราบต่อไปนี้อยู่ในรุ่นนี้:

- แอป (โดยเฉพาะรายการงาน) จะช้าลงในช่วงเวลาหนึ่ง
- **รุ่นของ Windows:** เมื่อมีการใช้ IND ในการสแกนบน Windows ผลลัพธ์ที่ไม่สอดคล้องกันจะทําให้สัญลักษณ์ที่สแกนผสมกัน

## <a name="version-2050"></a>รุ่น 2.0.5.0

รุ่นนี้แนะนำคุณลักษณะ การแก้ไข และการปรับปรุง:

- ข้อมูลลับของไคลเอนต์ไม่ซ่อนอยู่ในการตั้งค่าการเชื่อมต่ออีกต่อไป
- ขณะนี้คุณสามารถกดข้อความยาวใดๆ เพื่อดูข้อความทั้งหมดได้
- ข้อความแสดงข้อผิดพลาดเมื่อสิทธิ์การจัดเก็บขาดหายไปปรับปรุงแล้ว
- มีการเพิ่มลำดับการควบคุมใหม่ให้กับบางโฟลว์
- ปุ่มส่งไม่พร้อมใช้งานอีกต่อไปอย่างไม่ถูกต้องเนื่องจากขนาดของหน้าต่าง
- ขณะนี้ตัวเลือกสามารถดําเนินการต่อบนหน้าจอที่เล็กลงเมื่อมีการใช้ปุ่มที่ใหญ่ขึ้น
- การมีปุ่มวางทับสี่ปุ่มไม่ถูกตัดออกอีกต่อไป
- ขณะนี้แป้นพิมพ์สนับสนุนปุ่มลบ
- ปัญหาความสว่างที่อาจเกิดขึ้นเมื่อกดแป้นพิมพ์ได้รับการแก้ไขแล้ว
- ปัญหาข้อมูลสาธิตต่างๆ ได้รับการแก้ไขแล้ว
- ปัญหาที่ฟิลด์ตัวเลขได้รับผลกระทบในหน้ารายละเอียดมีการแก้ไขแล้ว
- แป้นพิมพ์หน้าจอจะไม่หายไปอีกต่อไปในบางอุปกรณ์
- อินเทอร์เฟสผู้ใช้ (UI) ต่างๆ ได้รับการแก้ไขแล้ว เช่น การตั้งค่าภายนอกที่ได้รับผลกระทบจากสีพื้นหลังและการวางตําแหน่ง
- UI ภาษารัสเซียได้รับการปรับปรุงแล้ว
- ปัญหาต่างๆ ที่เป็นสาเหตุให้ระบบหยุดตอบสนองได้รับการแก้ไข
- ปัญหาที่เกี่ยวข้องกับการเปิดเครื่องคิดเลขอีกครั้งได้รับการแก้ไขแล้ว
- **รุ่น Android:** ปัญหาที่ทำให้ Android 4.4 หยุดตอบสนองเมื่อเริ่มต้นได้รับการแก้ไขแล้ว
- **รุ่น Android:** การปรับสเกลขั้นต่ำลดลงเป็น 50 เปอร์เซ็นต์

## <a name="version-2040"></a>รุ่น 2.0.4.0

รุ่น 2.0.4.0 เป็นรายการนำออกใช้แรกที่พร้อมใช้งานแอป Warehouse Management บนมือถือ

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>คุณลักษณะใหม่ การแก้ไข และการปรับปรุงในรุ่น 2.0.4.0

รุ่นนี้จะแนะนำคุณลักษณะ การแก้ไข และการปรับปรุงใหม่ต่อไปนี้ซึ่งไม่พร้อมใช้งานในรุ่นการแสดงตัวอย่าง

- ถ้าบัตรรายละเอียดมีป้ายชื่อสองตัวที่มีข้อมูลเหมือนกัน ป้ายชื่อใดป้ายชื่อหนึ่งจะถูกซ่อนไว้
- ขณะนี้อักขระพิเศษจะแสดงขึ้นตามค่าเริ่มต้น และตัวเลือกเพื่อซ่อนอักขระเหล่านั้นถูกลบออกจากการตั้งค่าผู้ใช้แล้ว
- ขณะนี้ปุ่มส่งที่ปิดใช้งานอยู่จะแสดงเป็นไม่พร้อมใช้งานในมุมมองที่ยกแบบย่อ
- การเปลี่ยนแปลงตรรกะการจัดลำดับของตัวควบคุมช่วยให้มั่นใจว่ามาตราส่วนมีความต่อเนื่องมากขึ้นระหว่างอุปกรณ์ต่างๆ ดังนั้นจึงมีความต้องการน้อยกว่าในการปรับสเกลแบบอักษรหรือปุ่ม
- ธีมรูปแบบสีเริ่มต้นเปลี่ยนเป็น *เข้ม*
- ไอคอนที่ขาดหายไปของปุ่มส่งที่ปิดใช้งานได้ถูกเพิ่มในมุมมอง ribbon แล้ว
- ขณะนี้ข้อยกเว้นการหมดเวลาจะพาคุณไปยังหน้าการเชื่อมต่อแทนการแสดงข้อผิดพลาดในรายการ
- หากไม่มีการดำเนินการการส่ง (เช่น **ตกลง** **ใช่** **ยอมรับ** **ทำแล้ว** หรือ **เสร็จสิ้น**) ปุ่มส่งจะถูกปิดใช้งาน
- ปรับปรุงเสถียรภาพของแอปแล้ว
- มีการแก้ไขความเสี่ยงด้านความปลอดภัย [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701)
- **รุ่นของ Windows:** ปัญหาใน Windows ซึ่งเมนูไม่ตอบสนองหลังจากที่ปรับขนาดหน้าต่างใหม่ได้รับการแก้ไขแล้ว

### <a name="known-issue-in-version-2040"></a>ปัญหาที่ทราบในรุ่น 2.0.4.0

เกิดปัญหาที่ทราบต่อไปนี้อยู่ในรุ่นนี้:

- รุ่นนี้มีปัญหากับอุปกรณ์ที่ใช้ Android 4.4 คุณอาจพบปัญหาเมื่อคุณใช้แอปใน Android รุ่นนี้
