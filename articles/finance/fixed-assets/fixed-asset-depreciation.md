---
title: ค่าเสื่อมราคาของสินทรัพย์ถาวร
description: บทความนี้แสดงภาพรวมของค่าเสื่อมราคาในสินทรัพย์ถาวร
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.form: AssetBonus, AssetBookTable
ms.openlocfilehash: 9761fc9846324d1c165274b72033e195bf4ea3e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275309"
---
# <a name="fixed-asset-depreciation"></a>ค่าเสื่อมราคาของสินทรัพย์ถาวร

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

บทความนี้แสดงภาพรวมของค่าเสื่อมราคาในสินทรัพย์ถาวร

ค่าเสื่อมราคาเป็นธุรกรรมประจำงวด ซึ่งโดยปกติแล้วจะลดมูลค่าของสินทรัพย์ถาวรในงบดุล และบันทึกเป็นค่าใช้จ่ายในงบกำไรขาดทุน ดังนั้น โดยปกติบัญชีหลักจะถูกใช้ในเครดิตค่าเสื่อมราคาประจำงวดในงบดุล บัญชีตรงข้ามจะเป็นบัญชีในส่วนกำไรขาดทุนของผังบัญชี

สำหรับรุ่น 10.0.24 ตัวเลือกการตั้งค่าคอนฟิกสมุดบัญชีสินทรัพย์ **คำนวณค่าเสื่อมราคาค่าบวก** ในหน้า **สมุดบัญชี** ช่วยให้ค่าเสื่อมราคาสามารถเดบิตสินทรัพย์ถาวรที่ซื้อมาด้วยมูลค่าตามบัญชีค่าลบ (เครดิต) ได้

## <a name="depreciation-adjustment"></a>การปรับปรุงค่าเสื่อมราคา
โดยปกติ เฉพาะการแก้ไขธุรกรรมค่าเสื่อมราคาที่ลงรายการบัญชีไปแล้วจะถูกลงรายการบัญชีเป็นการปรับปรุงค่าเสื่อมราคา ดังนั้น บัญชีหลักและบัญชีตรงข้ามมีการตั้งค่าลักษณะเดียวกับบัญชีสำหรับค่าเสื่อมราคา การปรับปรุงค่าเสื่อมราคาอาจเป็นค่าบวกหรือค่าลบ แต่ฟังก์ชันของบัญชีหลัก (เป็นบัญชีงบดุล) และฟังก์ชันของบัญชีตรงข้าม (โดยปกติเป็นบัญชีกำไรขาดทุน) ยังคงเหมือนเดิม

## <a name="extraordinary-depreciation"></a>ค่าเสื่อมราคาพิเศษ
ค่าเสื่อมราคาพิเศษทำงานเหมือนค่าเสื่อมราคาพื้นฐาน ดังนั้น บัญชีหลักจะถูกใช้ในการเครดิตยอดเงินค่าเสื่อมราคาไปยังงบดุล และลดมูลค่าของสินทรัพย์ถาวร บัญชีตรงข้ามจะเป็นบัญชีกำไรขาดทุน ที่คำนวณค่าเสื่อมราคาสำหรับรอบระยะเวลาทางบัญชีเป็นค่าใช้จ่าย 

ค่าเสื่อมราคาพิเศษทำงานอย่างเป็นอิสระจากค่าเสื่อมราคาพื้นฐาน เมื่อมีค่าเสื่อมราคาพิเศษเป็นชนิดธุรกรรมที่แยกออกมา คุณจะสามารถลงรายการบัญชีและรายงานค่าเสื่อมราคาพิเศษแยกต่างหากจากค่าเสื่อมราคาพื้นฐานได้

## <a name="special-depreciation-allowance"></a>การหักค่าเสื่อมราคาพิเศษ
คุณสามารถใช้การหักค่าเสื่อมราคาพิเศษช่วยให้คุณสามารถมีจำนวนเงินค่าเสื่อมราคาพิเศษในระหว่างปีแรกที่เริ่มใช้งานและคิดค่าเสื่อมราคาสินทรัพย์ จะต้องหักค่าเสื่อมราคาพิเศษก่อนที่จะคำนวณค่าเสื่อมราคาอื่น เนื่องจากมักจะไม่ทราบหลังจากมีการหักค่าเสื่อมราคาพิเศษของอายุการใช้งานของสินทรัพย์ถาวร ควรใช้การคิดค่าเสื่อมราคาชนิดนี้กับสมุดบัญชีที่ไม่ได้ลงรายการบัญชีในบัญชีแยกประเภททั่วไป คุณสามารถใช้ฟังก์ชันประจำงวด ลบธุรกรรมที่ไม่ได้ลงรายการบัญชีในบัญชีแยกประเภททั่วไป ในการลบประวัติธุรกรรมสำหรับสมุดบัญชีเหล่านี้ จากนั้นคุณสามารถลบประวัติค่าเสื่อมราคาสำหรับสมุดบัญชีสินทรัพย์ถาวร ลงรายการบัญชีการหักค่าเสื่อมราคาพิเศษเมื่อทราบ และจากนั้นลงรายบัญชีธุรกรรมค่าเสื่อมราคาที่เหลืออยู่ของปีนั้นๆ 

คุณสามารถสร้างเรกคอร์ดการหักค่าเสื่อมราคาพิเศษได้ไม่จำกัดจำนวน หลังจากที่คุณกำหนดเรกคอร์ดเหล่านั้นให้กับสมุดบัญชีกลุ่มสินทรัพย์ จะถูกนำไปใช้กับสมุดบัญชีสินทรัพย์ 

การหักค่าเสื่อมราคาพิเศษจะถูกป้อนเป็นเปอร์เซ็นต์หรือเป็นจำนวนเงินคงที่ เมื่อคุณลงรายการบัญชีข้อเสนอค่าเสื่อมราคา ธุรกรรมการหักค่าเสื่อมราคาพิเศษจะถูกลงรายการบัญชีที่สมุดบัญชีโดยเป็นธุรกรรมที่แยกต่างหากจากธุรกรรมค่าเสื่อมราคา

## <a name="depreciation-calendars"></a> ปฏิทินค่าเสื่อมราคา
สมุดบัญชีแต่ละรายการมีปฏิทินที่จะใช้เมื่อคุณคิดค่าเสื่อมราคาสินทรัพย์ถาวร โดยค่าเริ่มต้น ถ้าคุณไม่ระบุปฏิทินในสมุดบัญชี สมุดบัญชีจะใช้ปฏิทินทางการเงินของบัญชีแยกประเภท คุณต้องเลือกปฏิทินทางการเงินสำหรับสมุดบัญชีเมื่อโพรไฟล์การคิดค่าเสื่อมราคาที่เชื่อมโยงกับสมุดบัญชีใช้ปีการคิดค่าเสื่อมราคาทางบัญชี 

คุณสามารถสร้างปฏิทินที่ใช้ร่วมกันโดยใช้หน้า **ปฏิทินทางการเงิน** ในบัญชีแยกประเภททั่วไป

สำหรับข้อมูลเพิ่มเติม ดู [วิธีการคิดค่าเสื่อมราคาและแบบแผนการคิดค่าเสื่อมราคา](depreciation-methods-conventions.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
