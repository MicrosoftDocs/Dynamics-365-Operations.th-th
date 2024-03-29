---
title: ตัวอย่างการรายงานทางอิเล็กทรอนิกส์สำหรับการตรวจสอบผู้จัดจำหน่าย
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้รูปแบบเช็คตัวอย่างการรายงานทางอิเล็กทรอนิกส์
author: mrolecki
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6863acaa264cfb8f15c34e85811a94afc67bec5e
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715274"
---
# <a name="electronic-reporting-sample-vendor-checks"></a>เช็คของผู้จัดจำหน่ายของตัวอย่างการรายงานทางอิเล็กทรอนิกส์

[!include [banner](../includes/banner.md)]

คุณสามารถใช้การรายงานทางอิเล็กทรอนิกส์ (ER) ในการจัดรูปแบบเช็คของผู้จัดจำหน่าย มีรูปแบบการตรวจสอบเฉพาะธนาคารและเฉพาะผู้ให้บริการจำนวนมากในตลาด รูปแบบเช็คตัวอย่างรวมไว้ในแบบจำลองเช็คการชำระเงินในที่เก็บเครื่องมือ ER เช็คตัวอย่างเหล่านี้จะมีป้ายชื่อ **เช็คกลาง (สหรัฐอเมริกา)** และ **เช็คต้นขั้วบนด้านล่าง (สหรัฐอเมริกา)**

## <a name="what-check-formats-are-currently-supported"></a>รูปแบบเช็คที่ได้รับการสนับสนุนในขณะนี้

คุณควรไปยังไลบรารีสินทรัพย์ที่แบ่งปันใน Microsoft Dynamics Lifecycle Services (LCS) เสมอ และดูรายการปัจจุบันของไฟล์ที่พร้อมใช้งานที่มีชนิดสินทรัพย์ของ **การตั้งค่าคอนฟิก GER** ส่วนถัดไป "ฉันต้องตั้งค่าอะไรบ้าง" มีการเชื่อมโยงไปยังบทความที่อธิบายถึงวิธีการสร้างที่เก็บ LCS เพื่อให้คุณสามารถตรวจทานการตั้งค่าคอนฟิกที่มีอยู่และนำเข้าการตั้งค่าคอนฟิกที่เลือกไว้

Microsoft Dynamics 365 Finance รวมรูปแบบตัวอย่างที่ซึ่งมีการตรวจสอบอยู่ด้านบน ซึ่งตามด้วยส่วนของการส่งเงินสองส่วน และยังมีรูปแบบตัวอย่างที่มีเช็คอยู่ตรงกลาง ระหว่างส่วนการชำระเงินผ่านธนาคารสองส่วน รูปแบบตัวอย่างเหล่านี้สอดคล้องกับรูปแบบเช็คธุรกิจแบบ Deluxe

## <a name="what-do-i-have-to-set-up"></a>ฉันจำเป็นต้องตั้งค่าอะไรบ้าง

- ก่อนที่คุณจะสามารถพิมพ์การตรวจสอบโดยใช้ ER ได้ คุณจะต้องนำเข้าการตั้งค่าคอนฟิกที่ใช้งานอยู่อย่างน้อยหนึ่งรายการลงในการตั้งค่าคอนฟิก ER ของคุณ สำหรับคำแนะนำ ให้ดูที่ [ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
- เมื่อคุณตั้งค่าคอนฟิกเช็คการจัดการเงินสดและธนาคารสำหรับบัญชีธนาคาร เลือกกล่องกาเครื่องหมาย **รูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป** และจากนั้นอกรูปแบบเช็คที่เหมาะสมเป็นการตั้งค่าคอนฟิกรูปแบบการส่งออก
- คุณต้องระบุหมายเลขของรายการบันทึกที่จะพิมพ์บนการชำระเงินผ่านธนาคาร ตรวจสอบให้แน่ใจว่าได้รวมแถวของส่วนหัวแล้วเมื่อคุณคำนวณหมายเลขนี้ สำหรับรูปแบบเช็คตัวอย่างสองรายการ จำนวนที่แนะนำของรายการบันทึกการจัดส่งคือ 17 อย่างไรก็ตาม จำนวนนี้จะแตกต่างกัน ขึ้นอยู่กับปริมาณสินค้าคงคลังเช็คของคุณและโปรแกรมควบคุมเครื่องพิมพ์ของคุณ
- เราขอแนะนำให้คุณพิมพ์เช็คทดสอบเพื่อตรวจสอบความถูกต้องของโครงร่างเช็ค เมื่อต้องการพิมพ์เช็คทดสอบ เลือกตัวเลือก **ทดลองพิมพ์** รูปแบบการตรวจสอบตัวอย่างทำงานได้ดีที่สุดเมื่อ **ขอบ** ถูกตั้งค่าเป็น **ไม่มี** ในคุณสมบัติเครื่องพิมพ์ขั้นสูง Microsoft Excel หลังจากที่มีการสร้างเช็คทดสอบ ให้เปิดใช้งานการแก้ไขของผลลัพธ์ Excel และตั้งค่าคอนฟิกโครงร่างหน้าเพื่อให้ขอบทั้งหมดถูกตั้งค่าเป็น **0** (ศูนย์) เปรียบเทียบสำเนาทดสอบของเช็คกับสินค้าคงคลังเช็คของคุณ และปรับการตั้งค่าจนกระทั่งคุณพอใจกับการจัดตำแหน่ง
- เมื่อคุณสร้างการชำระเงินสำหรับบัญชีธนาคารที่ตั้งค่าคอนฟิกไว้ในสมุดรายวันการชำระเงิน เช็คจะถูกพิมพ์โดยใช้รูปแบบที่ระบุ

สำหรับข้อมูลเพิ่มเติม ดู [แก้ไขรูปแบบการรายงานทางอิเล็กทรอนิกส์](../../fin-ops-core/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
