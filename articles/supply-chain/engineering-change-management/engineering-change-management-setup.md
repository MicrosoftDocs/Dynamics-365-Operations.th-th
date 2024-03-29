---
title: สร้างค่าทั่วไปสำหรับการจัดการการเปลี่ยนแปลงทางวิศวกรรม
description: บทความนี้จะอธิบายวิธีการสร้างค่าทั่วไปที่จะใช้สำหรับพารามิเตอร์ในส่วนต่างๆ ของการจัดการการเปลี่ยนแปลงทางวิศวกรรม
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 376e3f209109d36e5a18b11d81afc55ba509e3e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852547"
---
# <a name="establish-common-values-for-engineering-change-management"></a>สร้างค่าทั่วไปสำหรับการจัดการการเปลี่ยนแปลงทางวิศวกรรม

[!include [banner](../includes/banner.md)]

เมื่อคุณตั้งค่าการจัดการการเปลี่ยนแปลงทางวิศวกรรม คุณต้องสร้างคอลเลกชันที่หลากหลายของค่าที่จะใช้ในการกรอกรายละเอียดรายการแบบหล่นลงในส่วนอื่นๆ ของส่วนติดต่อผู้ใช้ (UI) คุณควรระบุค่าเหล่านี้ตามชนิดของผลิตภัณฑ์ที่คุณผลิตและต้องการธุรกิจเฉพาะของคุณ

## <a name="engineering-change-categories"></a>ประเภทการเปลี่ยนแปลงทางวิศวกรรม

คุณใช้ประเภทการเปลี่ยนแปลงทางวิศวกรรมเพื่อจัดระเบียบใบสั่งเปลี่ยนแปลงทางวิศวกรรมของคุณ เพื่อให้สามารถจัดการและรีวิวได้ง่ายขึ้น ตัวอย่างเช่น คุณอาจพบว่ามีประโยชน์ในการตั้งค่าลำดับงานที่ซึ่งแผนกเฉพาะต้องรีวิวการเปลี่ยนแปลงที่นำเสนอ โดยขึ้นอยู่กับประเภท ดังนั้น ใบสั่งการเปลี่ยนแปลงทางวิศวกรรมจึงรวมถึงฟิลด์ **ประเภท**

เมื่อต้องการสร้างคอลเลกชันของประเภทการเปลี่ยนแปลงทางวิศวกรรมที่ใช้ในบริษัทของคุณ ให้ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> การจัดการการเปลี่ยนแปลงทางวิศวกรรม \> ประเภทการเปลี่ยนแปลงทางวิศวกรรม** จากนั้น คุณสามารถใช้ปุ่มบนบานหน้าต่างการดำเนินการเพื่อเพิ่ม ลบ และแก้ไขค่า และเพื่อจัดเรียงตามลำดับที่จะปรากฏในรายการแบบหล่นลงซึ่งจะแสดงขึ้น

## <a name="engineering-change-priorities"></a>ลำดับความสำคัญของการเปลี่ยนแปลงทางวิศวกรรม

คุณใช้ระดับความสำคัญของการเปลี่ยนแปลงทางวิศวกรรมเพื่อบ่งชี้ความสำคัญหรือความเร่งด่วนของใบสั่งเปลี่ยนแปลงทางวิศวกรรม ซึ่งสามารถช่วยคุณในการติดตามความสำคัญของใบสั่งเปลี่ยนแปลงทางวิศวกรรม เพื่อให้คุณสามารถระบุว่าใบสั่งใดควรจะถูกประมวลผลเป็นอันดับแรกและเร็วเพียงใด

เมื่อต้องการสร้างคอลเลกชันของระดับความสำคัญของการเปลี่ยนแปลงทางวิศวกรรมที่ใช้ในบริษัทของคุณ ให้ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> การจัดการการเปลี่ยนแปลงทางวิศวกรรม \> ระดับความสำคัญของการเปลี่ยนแปลงทางวิศวกรรม** จากนั้น คุณสามารถใช้ปุ่มบนบานหน้าต่างการดำเนินการเพื่อเพิ่ม ลบ และแก้ไขค่า และเพื่อจัดเรียงตามลำดับที่จะปรากฏในรายการแบบหล่นลงซึ่งจะแสดงขึ้น

## <a name="engineering-change-reasons"></a>เหตุผลในการเปลี่ยนแปลงทางวิศวกรรม

เหตุผลการเปลี่ยนแปลงทางวิศวกรรมบ่งชี้ถึงสาเหตุหรือลักษณะของการเปลี่ยนแปลงในใบสั่งเปลี่ยนแปลง

เมื่อต้องการสร้างคอลเลกชันของเหตุผลของการเปลี่ยนแปลงทางวิศวกรรมที่ใช้ในบริษัทของคุณ ให้ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> การจัดการการเปลี่ยนแปลงทางวิศวกรรม \> เหตุผลของการเปลี่ยนแปลงทางวิศวกรรม** จากนั้น คุณสามารถใช้ปุ่มบนบานหน้าต่างการดำเนินการเพื่อเพิ่ม ลบ และแก้ไขค่า และเพื่อจัดเรียงตามลำดับที่จะปรากฏในรายการแบบหล่นลงซึ่งจะแสดงขึ้น

## <a name="material-disposal-codes"></a>รหัสการจัดการวัสดุ

คุณใช้รหัสการตัดจำหน่ายวัสดุเพื่อจัดประเภทวัสดุที่ใช้ในสินค้าสำเร็จรูปของคุณ หรือส่วนประกอบที่ต้องตัดจำหน่ายในลักษณะเฉพาะ หรือต้องมีการปฏิบัติบางอย่างก่อนจึงจะสามารถเพิ่มไปยังถังขยะปกติของคุณได้ เมื่อคุณเพิ่มผลิตภัณฑ์ที่เกี่ยวข้องไปยังใบสั่งเปลี่ยนแปลงทางวิศวกรรม คุณสามารถกำหนดรหัสการตัดจำหน่ายเป็นส่วนหนึ่งของรายละเอียดการเปลี่ยนแปลง

เมื่อต้องการสร้างคอลเลกชันของรหัสการตัดจำหน่ายวัสดุที่ใช้ในบริษัทของคุณ ให้ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> การจัดการการเปลี่ยนแปลงทางวิศวกรรม \> รหัสการตัดจำหน่ายวัสดุ** จากนั้น คุณสามารถใช้ปุ่มบนบานหน้าต่างการดำเนินการเพื่อเพิ่ม ลบ และแก้ไขค่า และเพื่อจัดเรียงตามลำดับที่จะปรากฏในรายการแบบหล่นลงซึ่งจะแสดงขึ้น

## <a name="received-customer-approval"></a>การอนุมัติของลูกค้าที่ได้รับ

เมื่อคุณออกแบบผลิตภัณฑ์สำหรับลูกค้าเฉพาะ การออกแบบและข้อมูลจำเพาะมักจะต้องมีการตรวจสอบความถูกต้อง ก่อนที่จะสามารถตั้งค่าผลิตภัณฑ์เป็นพร้อม ฟิลด์ **การอนุมัติของลูกค้าที่ได้รับ** จะช่วยให้คุณสามารถระบุระยะห่างของผลิตภัณฑ์ในกระบวนการอนุมัติลูกค้า และ/หรือ ได้รับการอนุมัติแล้วหรือไม่

เมื่อต้องการสร้างคอลเลกชันของค่าการอนุมัติของลูกค้าที่ได้รับที่ใช้ในบริษัทของคุณ ให้ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> การจัดการการเปลี่ยนแปลงทางวิศวกรรม \> การอนุมัติของลูกค้าที่ได้รับ** จากนั้น คุณสามารถใช้ปุ่มบนบานหน้าต่างการดำเนินการเพื่อเพิ่ม ลบ และแก้ไขค่า และเพื่อจัดเรียงตามลำดับที่จะปรากฏในรายการแบบหล่นลงซึ่งจะแสดงขึ้น

## <a name="engineering-change--environmental-health-and-safety-codes"></a>การเปลี่ยนแปลงด้านวิศวกรรม – รหัสสุขภาพและความปลอดภัยด้านสิ่งแวดล้อม

ถ้าต้องคำนึงถึงกฎระเบียบของสุขภาพและความปลอดภัยด้านสิ่งแวดล้อมมาตรฐาน หรือกฎระเบียบหรือกระบวนงานเฉพาะของบริษัทในการผลิตของผลิตภัณฑ์ คุณสามารถใช้รหัสสุขภาพและความปลอดภัยด้านสิ่งแวดล้อมเพื่อกำหนด ในใบสั่งเปลี่ยนแปลงทางวิศวกรรม คุณสามารถบ่งชี้ว่าจะใช้รหัสใดกับการผลิตผลิตภัณฑ์ ในขณะที่คุณแก้ไขรายละเอียดของผลิตภัณฑ์ที่ได้รับผลกระทบ

เมื่อต้องการสร้างคอลเลกชันของค่าสุขภาพและความปลอดภัยที่ใช้ในบริษัทของคุณ ให้ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> การจัดการการเปลี่ยนแปลงทางวิศวกรรม \> การเปลี่ยนแปลงทางวิศวกรรม - รหัสสุขภาพและความปลอดภัยด้านสิ่งแวดล้อม** จากนั้น คุณสามารถใช้ปุ่มบนบานหน้าต่างการดำเนินการเพื่อเพิ่ม ลบ และแก้ไขค่า และเพื่อจัดเรียงตามลำดับที่จะปรากฏในรายการแบบหล่นลงซึ่งจะแสดงขึ้น

## <a name="engineering-change-severities"></a>ความรุนแรงของการเปลี่ยนแปลงทางวิศวกรรม

คุณใช้ความรุนแรงในการเปลี่ยนแปลงทางวิศวกรรมเพื่อระบุระดับของผลกระทบที่ใช้กับผลิตภัณฑ์ในใบสั่งเปลี่ยนแปลงทางวิศวกรรม

เมื่อต้องการสร้างคอลเลกชันของความรุนแรงในการเปลี่ยนแปลงทางวิศวกรรมที่ใช้ในบริษัทของคุณ ให้ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> การจัดการการเปลี่ยนแปลงทางวิศวกรรม \> ความรุนแรงในการเปลี่ยนแปลงทางวิศวกรรม** จากนั้น คุณสามารถใช้ปุ่มบนบานหน้าต่างการดำเนินการเพื่อเพิ่ม ลบ และแก้ไขค่า และเพื่อจัดเรียงตามลำดับที่จะปรากฏในรายการแบบหล่นลงซึ่งจะแสดงขึ้น

คุณสามารถสร้างกฎที่ใช้กับระดับความรุนแรงแต่ละระดับที่คุณสร้างขึ้นได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนดกฎเหล่านี้ ให้ดูที่หัวข้อถัดไป

## <a name="engineering-change-severity-rule-sets"></a>ชุดกฎความรุนแรงของการเปลี่ยนแปลงทางวิศวกรรม

คุณใช้ชุดกฎความรุนแรงของการเปลี่ยนแปลงทางวิศวกรรมเพื่อสร้างกลุ่มของกฎที่คุณสามารถใช้เพื่อคำนวณความรุนแรงของใบสั่งเปลี่ยนแปลงโดยอัตโนมัติ โดยยึดตามชนิดของการเปลี่ยนแปลงในผลิตภัณฑ์ที่ได้รับผลกระทบ เมื่อต้องการใช้กฎความรุนแรง ให้เปิดหน้า **พารามิเตอร์การจัดการการเปลี่ยนแปลงทางวิศวกรรม** และตั้งค่าฟิลด์ **กฎความรุนแรง** เพื่อ *คำนวณ* หรือ *คำนวณโดยอัตโนมัติ*

เมื่อระบบประเมินความรุนแรง จะประมวลผลกฎตามลำดับที่ปรากฏบนหน้า จากบนลงล่าง สำหรับกฎที่จะเลือกและมีการกำหนดระดับความสำคัญไว้ กฎทั้งหมดในชุดกฎต้องเป็นไปตามความต้องการ

เมื่อต้องการตั้งค่ากฎที่ใช้กับระดับความรุนแรงของการเปลี่ยนแปลงแต่ละระดับที่คุณได้กำหนดไว้ ให้ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> การจัดการการเปลี่ยนแปลงวิศวกรรม \> ชุดกฎความรุนแรงของการเปลี่ยนแปลงวิศวกรรม** จากนั้น ทำตามหนึ่งในขั้นตอนเหล่านี้

- เมื่อต้องการสร้างชุดกฎใหม่ ให้เลือก **สร้าง** ในบานหน้าต่างการดำเนินการ แล้วกำหนดฟิลด์ตามที่อธิบายไว้ในส่วนนี้ในภายหลัง
- ถ้าต้องการแก้ไขชุดกฎที่มีอยู่ ให้เลือกในบานหน้าต่างรายการ เลือก **แก้ไข** บนบานหน้าต่างการดำเนินการ แล้วจากนั้น กำหนดฟิลด์ตามที่อธิบายไว้ในส่วนนี้ในภายหลัง
- ถ้าต้องการลบชุดกฎที่มีอยู่ ให้เลือกชุดกฎนั้นในบานหน้าต่างรายการ แล้วจากนั้น เลือก **ลบ** ในบานหน้าต่างการดำเนินการ
- เมื่อต้องการจัดเรียงรายการของชุดกฎใหม่ ให้เลือกชุดกฎในบานหน้าต่างรายการ แล้วจากนั้น ใช้ปุ่ม  **ขึ้น** และ **ลง** ในบานหน้าต่างการดำเนินการเพื่อเปลี่ยนตำแหน่ง

สำหรับชุดกฎแต่ละชุด ตั้งค่าฟิลด์ต่อไปนี้:

- **ความรุนแรง** – เลือกระดับความร้ายแรงเพื่อสร้างกฎ คุณสามารถใช้หน้า **ความรุนแรงในการเปลี่ยนแปลงทางวิศวกรรม** เพื่อสร้างและตั้งชื่อระดับ (สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วนก่อนหน้านี้)

ใช้ปุ่มบน FastTab **กฎ** เพื่อเพิ่มหรือลบกฎสำหรับการตั้งค่าความรุนแรงปัจจุบัน แต่ละกฎมีฟิลด์ **กฎ** และฟิลด์ **ชื่อ** กฎจะถูกสร้างขึ้นโดยระบบและระบุชนิดของการเปลี่ยนแปลงที่ผลิตภัณฑ์สามารถมีได้ ชื่อจะบ่งชี้ชนิดของการเปลี่ยนแปลง


[!INCLUDE[footer-include](../../includes/footer-banner.md)]