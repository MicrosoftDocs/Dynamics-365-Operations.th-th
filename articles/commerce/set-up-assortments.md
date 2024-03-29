---
title: ตั้งค่าการจัดประเภท
description: บทความนี้อธิบายว่าการจัดประเภทคืออะไรและอธิบายวิธีการตั้งค่าการจัดประเภทใน Dynamics 365 Commerce
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.industry: Retail
ms.search.form: RetailAssortmentDetails
ms.openlocfilehash: 26827a09962dbbb6be4e0a054e22424260592702
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271835"
---
# <a name="set-up-assortments"></a>ตั้งค่าการจัดประเภท

[!include [banner](includes/banner.md)]

บทความนี้อธิบายว่าการจัดประเภทคืออะไรและอธิบายวิธีการตั้งค่าการจัดประเภทใน Dynamics 365 Commerce

การจัดประเภทเป็นคอลเลกชันของผลิตภัณฑ์ที่เกี่ยวข้องที่คุณกำหนดให้กับช่องทางการค้า เช่น ร้านค้าจริง หรือร้านค้าออนไลน์ คุณสามารถใช้การจัดประเภทเพื่อระบุผลิตภัณฑ์ที่มีในแต่ละร้านค้า การจัดประเภทสามารถรวมประเภทของผลิตภัณฑ์ ดังนั้น ผลิตภัณฑ์ทั้งหมดที่กำหนดให้กับประเภทเฉพาะจะถูกรวมอยู่ในการจัดประเภท การจัดประเภทยังสามารถรวมผลิตภัณฑ์เฉพาะและผลิตภัณฑ์ย่อยเฉพาะ ด้วยการตั้งค่าการจัดประเภท คุณสามารถกำหนดผลิตภัณฑ์หลายพันผลิตภัณฑ์ให้กับช่องทางในเวลาเดียวกันในชุดข้อมูลใดๆที่จำเป็นต่อร้านค้าของคุณ คุณสามารถตั้งค่าการจัดประเภทผลิตภัณฑ์ได้มากตามจำนวนที่คุณต้องการ ผลิตภัณฑ์แต่ละรายการสามารถรวมอยู่ในการจัดประเภทอย่างน้อยหนึ่งรายการ และแต่ละการจัดประเภทสามารถถูกกำหนดให้กับช่องทางหนึ่งรายการขึ้นไป ตัวอย่างเช่น คุณสามารถกำหนดหนึ่งการจัดประเภทที่ประกอบด้วยชุดพื้นฐานของผลิตภัณฑ์ ร้านค้าทั้งหมดได้รับการจัดประเภทนี้ จากนั้นคุณกำหนดการจัดประเภทอีกรายการหนึ่งที่รวมเฉพาะอุปกรณ์กีฬาขนาดใหญ่ เฉพาะร้านค้าของคุณมีขนาดใหญ่จะได้รับการจัดประเภทนี้ แผนภาพต่อไปนี้แสดงวิธีการกำหนดผลิตภัณฑ์ให้กับการจัดประเภท และวิธีที่ประเภทเหล่านี้จะสามารถถูกกำหนดให้กับช่องทางได้อย่างไร

![ความสัมพันธ์การจัดประเภทผลิตภัณฑ์](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะสามารถตั้งค่าการจัดประเภทและกำหนดให้กับช่องทางการค้า คุณต้องดำเนินงานต่อไปนี้

| งาน                              | คำอธิบาย |
|-----------------------------------|-------------|
| การตั้งค่าช่องทาง          | ช่องทางแสดงร้านค้าจริง ร้านค้าออนไลน์ หรือมาร์เก็ตเพลสออนไลน์ คุณต้องตั้งค่าอย่างน้อยหนึ่งช่องทาง และตั้งค่าคอนฟิกตัวเลือกสำหรับร้านค้า การจัดประเภทถูกกำหนดให้กับร้านค้าเพื่อระบุผลิตภัณฑ์ที่ร้านค้าเฉพาะมี |
| สร้างลำดับชั้นองค์กร | หลังจากที่คุณตั้งค่าช่องทางการค้าสำหรับองค์กรของคุณ คุณต้องตั้งค่าคอนฟิกลำดับชั้นขององค์กรที่แสดงถึงโครงสร้างองค์กรของช่องทางการขายปลีกของคุณ ลำดับชั้นขององค์กรสามารถใช้สำหรับการจัดประเภท การเพิ่มเติมสินค้า และการรายงาน โดยการเพิ่มช่องทางของคุณไปที่ลำดับชั้นขององค์กร คุณสามารถกำหนดการจัดประเภทไปยังกลุ่มของร้านค้า แทนที่จะกำหนดการจัดประเภทแต่ละรายการให้กับแต่ละร้านค้า คุณกำหนดการจัดประเภทไปยังโหนดองค์กรระดับสูง จากนั้น เมื่อใดที่ช่องทางใหม่ถูกเพิ่มไปที่โหนดองค์กรระดับสูง ซึ่งช่องทางรับช่วงการจัดประเภทใดๆที่ถูกกำหนดให้กับโหนดองค์กรที่สูงกว่าโดยอัตโนมัติ คุณสามารถกำหนดการจัดประเภทให้กับเฉพาะช่องทางที่มีอยู่ในลำดับชั้นขององค์กรที่กำหนดเท่านั้น ซึ่งถูกกำหนดวัตถุประสงค์ **การจัดประเภทการค้า** |
| กำหนดผลิตภัณฑ์                  | ก่อนที่คุณจะสามารถเพิ่มผลิตภัณฑ์ไปยังการจัดประเภท คุณต้องเพิ่มไปยังการค้า คุณสามารถเพิ่มผลิตภัณฑ์ได้ด้วยตนเอง หรือคุณสามารถนำเข้าจากผู้จัดจำหน่าย หลังจากที่คุณเพิ่มผลิตภัณฑ์ คุณต้องนำออกใช้กับนิติบุคคล เฉพาะผลิตภัณฑ์ที่ถูกนำออกใช้กับนิติบุคคลสามารถทำให้พร้อมใช้งานสำหรับช่องทางของคุณ คุณสามารถเพิ่มผลิตภัณฑ์ที่ยังไม่ได้นำออกใช้กับนิติบุคคลไปยังการจัดประเภท และการจัดประเภทสามารถได้รับการอนุมัติ อย่างไรก็ตาม จนกว่าผลิตภัณฑ์จะถูกนำออกใช้กับนิติบุคคล จะไม่สามารถทำให้ผลิตภัณฑ์พร้อมใช้งานสำหรับช่องทางของคุณได้ |
| ตั้งค่าการจัดประเภทตามลำดับชั้น      | เมื่อคุณสร้างผลิตภัณฑ์การค้าของคุณ คุณสามารถจัดกลุ่มและจัดประเภทรายการโดยใช้ลักษณะการทำงานตามลำดับชั้นประเภท คุณสามารถสร้างหนึ่งลำดับชั้นหลัก เพื่อจัดกลุ่มและจัดประเภทผลิตภัณฑ์ทั้งหมดที่คุณกระจายผ่านช่องทางของคุณ คุณยังสามารถสร้างการจัดประเภทลำดับชั้นแบบแยกต่างหาก แบบเพิ่มเติม เพื่อจัดกลุ่มหรือจัดประเภทผลิตภัณฑ์ของคุณสำหรับวัตถุประสงค์พิเศษ เช่น การส่งเสริมการขายหรือการจัดประเภท โดยการใช้การจัดประเภทลำดับชั้น คุณสามารถกำหนดผลิตภัณฑ์ทั้งหมดในประเภทเฉพาะไปยังการจัดประเภท ผลิตภัณฑ์ใดๆที่ถูกเพิ่มลงในประเภทที่รวมอยู่ในการจัดประเภทจะรวมอยู่ในการจัดประเภทโดยอัตโนมัติ จากนั้น ในครั้งถัดไปที่มีการดำเนินงานตัวจัดกำหนดการจัดประเภทการค้า ผลิตภัณฑ์เหล่านี้จะพร้อมใช้งานสำหรับช่องทางที่มีการกำหนดการจัดประเภท |

## <a name="setting-up-an-assortment"></a>การตั้งค่าการจัดประเภท

หลังจากที่คุณดำเนินการข้อกำหนดเบื้องต้นสำเร็จ คุณสามารถสร้างการจัดประเภทและกำหนดให้กับช่องทางของคุณ เพื่อตั้งค่าการจัดประเภท คุณต้องดำเนินการงานต่อไปนี้ให้สำเร็จ

1. สร้างการจัดประเภทใหม่หรือคัดลอกการจัดประเภทที่มีอยู่
2. เลือกช่องทางหรือกลุ่มระดับสูงของช่องทางที่ใช้การจัดประเภท
3. เพิ่มประเภทผลิตภัณฑ์ แต่ละผลิตภัณฑ์ หรือผลิตภัณฑ์ย่อยไปยังการจัดประเภท คุณสามารถรวมผลิตภัณฑ์ทั้งหมดในประเภทเฉพาะ หรือคุณสามารถแยกผลิตภัณฑ์ที่เลือกออกจากประเภทที่ถูกรวมอยู่ในการจัดประเภท
4. เผยแพร่การจัดประเภท เมื่อคุณเผยแพร่การจัดประเภท ตัวจัดกำหนดการจัดประเภทจะมีการดำเนินงานโดยอัตโนมัติ กระบวนการนี้สร้างรายการผลิตภัณฑ์ เมื่อกระบวนการนี้เสร็จสมบูรณ์ ผลิตภัณฑ์ที่จะพร้อมใช้งานสำหรับช่องทางที่กำหนดให้กับการจัดประเภทผลิตภัณฑ์ ถ้ามีการดำเนินการเปลี่ยนแปลงการจัดประเภทที่เผยแพร่แล้ว หรือช่องทางที่กำหนดให้กับการจัดประเภท การจัดประเภทต้องมีการอัพเดต เพื่ออัพเดตการจัดประเภทเมื่อมีการเปลี่ยนแปลง คุณสามารถดำเนินงานตัวจัดกำหนดการจัดประเภทให้เป็นชุดงาน


[!INCLUDE[footer-include](../includes/footer-banner.md)]
