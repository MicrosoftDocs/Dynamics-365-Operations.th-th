---
title: แสดงตัวอย่างและเผยแพร่การทดสอบ
description: หัวข้อนี้อธิบายวิธีการดูตัวอย่างและเผยแพร่การทดลองจาก Dynamics 365 Commerce
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 32115378be00df771c6ff658da0c090446edf8b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009959"
---
# <a name="preview-and-publish-an-experiment"></a>แสดงตัวอย่างและเผยแพร่การทดสอบ

หัวข้อนี้อธิบายวิธีการดูตัวอย่างและเผยแพร่การทดลองใน Dynamics 365 Commerce หลังจากที่คุณ [เชื่อมต่อการทดลองและแก้ไขการเปลี่ยนแปลงของคุณแล้ว](experimentation-connect-edit.md) แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับการตั้งค่า และการรันการทดลองบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในหัวข้อที่แยกต่างหาก

[ ![การเดินทางของผู้ใช้การทดลอง - ดูตัวอย่างและเผยแพร่](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>แสดงตัวอย่างการเปลี่ยนแปลงการทดลองของคุณ
คุณสามารถแสดงตัวอย่างการเปลี่ยนแปลงของคุณ และแก้ไขต่อไปจนกว่าจะเหมือนแบบที่คุณต้องการ

เมื่อต้องการแสดงตัวอย่างการเปลี่ยนแปลงการทดลองของคุณบนไซต์ของคุณในตัวสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้

1. จากเมนูแบบหล่นลงของการเปลี่ยนแปลงด้านล่างแถบคำสั่ง เลือกเนื้อหาที่คุณต้องการแสดงตัวอย่าง 
1. บนแถบคำสั่ง ให้เลือก **แสดงตัวอย่าง** ตัวอย่างของลักษณะเนื้อหาที่จะปรากฏเมื่อการเผยแพร่แสดงขึ้น
1. เมื่อต้องการแสดงตัวอย่างรูปแบบอื่น ให้เลือกจากเมนูแบบหล่นลงของการเปลี่ยนแปลง และเลือก **แสดงตัวอย่าง** อีกครั้ง

## <a name="publish-your-experiment"></a>เผยแพร่การทดลองของคุณ
ถ้าคุณไม่ได้ใช้กลุ่มเผยแพร่เพื่อกำหนดตารางเวลา เมื่อการทดลองของคุณใช้งานจริง และคุณต้องการเผยแพร่ทันที ให้เลือก **เผยแพร่** ในแถบคำสั่ง การเปลี่ยนแปลงทั้งหมดที่เป็นของการทดลองจะถูกเผยแพร่
    
> [!IMPORTANT]
> ถ้าหน้ามี URL ที่ยังไม่ได้เผยแพร่ คุณต้องเผยแพร่ URL ก่อน หรือไม่งั้นผู้ใช้เว็บไซต์ของคุณจะไม่สามารถมองเห็นได้ สำหรับรายละเอียด ให้ดูที่ [บันทึก แสดงตัวอย่าง และเผยแพร่หน้า](save-preview-publish-page.md)
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>ใช้กลุ่มเผยแพร่เพื่อกำหนดเวลาที่การทดลองของคุณใช้งานจริง
การเปลี่ยนแปลงที่สร้างขึ้นในตัวสร้างไซต์สามารถจัดกำหนดการสำหรับการเผยแพร่โดยใช้กลุ่มเผยแพร่ ภายในกลุ่มเผยแพร่ คุณสามารถเชื่อมต่อหน้าหรือส่วนกับการทดลองของคุณได้โดยการเลือก **การทดลอง** ในบานหน้าต่างนำทางด้านซ้าย นอกจากนี้คุณยังสามารถดำเนินการนี้ได้โดยเลือก **หน้า** หรือ **ส่วน** และปฏิบัติตามคำแนะนำใน [เชื่อมต่อการทดลองและแก้ไขการเปลี่ยนแปลง](experimentation-connect-edit.md) สำหรับข้อมูลเกี่ยวกับกลุ่มเผยแพร่ ให้ดูที่ [ทำงานกับกลุ่มเผยแพร่](publish-groups.md)

เมื่อใช้กลุ่มเผยแพร่ที่มีการทดลอง มีข้อควรพิจารณาที่สำคัญบางประการที่ควรระวัง
- เมื่อคุณเพิ่มหน้าหรือส่วนต่างๆ ที่มีการทดลองรันบนกลุ่มเผยแพร่ การทดลองจะถูกลบออกจากหน้าหรือส่วนในกลุ่มเผยแพร่
- การทดลองที่มีการเชื่อมต่อกับหน้าในไซต์ที่ใช้งานจริงจะไม่พร้อมใช้งานสำหรับหน้าภายในกลุ่มเผยแพร่ และในทางกลับกันด้วย ในทำนองเดียวกัน หน้าที่มีการทดลองทำงานอยู่ในไซต์ที่ใช้งานจริงจะไม่พร้อมใช้งานสำหรับการทดลองอื่นๆ ในกลุ่มเผยแพร่ และในทางกลับกันด้วย
- เมื่อคุณเผยแพร่หรือจัดกำหนดการกลุ่มเผยแพร่ เนื้อหาทั้งหมดในกลุ่มเผยแพร่จะถูกเผยแพร่โดยไม่คำนึงว่ามีการทดสอบที่เกี่ยวข้องกับกลุ่มเผยแพร่หรือไม่
- เนื่องจากกลุ่มเผยแพร่ยังคงแสดงหลังจากที่มีการเผยแพร่ไปยังไซต์ที่ใช้งานจริง การทดลองในกลุ่มเผยแพร่จะยังคงแสดงด้วย ดังนั้น คุณจึงไม่สามารถเชื่อมโยงการทดลองอื่นๆ กับหน้าหรือส่วนเดียวกันได้ ถ้าต้องการหลีกเลี่ยงข้อจำกัดนี้ ให้ลบกลุ่มเผยแพร่ใดๆ ที่มีการทดลองการแสดง ในทำนองเดียวกัน ถ้าคุณต้องการลบการทดลองในไซต์ที่ใช้งานจริงที่มีอยู่ในกลุ่มเผยแพร่ ให้ลบออกจากกลุ่มเผยแพร่ก่อน

## <a name="previous-step"></a>ขั้นตอนก่อนหน้า
[เชื่อมต่อและแก้ไขการทดสอบ](experimentation-connect-edit.md)

## <a name="next-step"></a>ขั้นตอนต่อไป
[รันและตรวจสอบการทดลอง](experimentation-run-monitor.md)
