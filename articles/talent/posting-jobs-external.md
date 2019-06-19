---
title: ลงประกาศงานลงในไซต์การทำงานภายนอกจาก Attract
description: หัวข้อนี้อธิบายวิธีการใช้ Dynamics 365 for Talent - Attract เพื่อลงประกาศงานไปยังไซต์การสรรหาบุคลากรภายนอก
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590493"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>ลงประกาศงานลงในไซต์การทำงานภายนอกจาก Attract

[!include [banner](../includes/banner.md)]

คุณต้องการเรียกดูตำแหน่งที่เปิดของคุณ ข้างหน้าผู้สมัครที่มีคุณสมบัติหลายรายที่สุดที่เป็นไปได้ ไซต์การสรรหาบุคลากร เช่น Broadbean ช่วยให้คุณบรรลุถึงเป้าหมายนี้ Microsoft Dynamics 365 talent: ขณะนี้ Attract ช่วยให้คุณลงประกาศงานไปยัง Broadbean และ Microsoft ให้ข้อเสนอใหม่ในพื้นที่นี้ตลอดเวลา

## <a name="post-jobs-to-broadbean"></a>ลงประกาศงานไปยัง Broadbean

ก่อนที่คุณจะสามารถลงประกาศงานไปยัง Broadbean คุณต้องตั้งค่าคอนฟิกการรวม Broadbean

> [!NOTE]
> - เพื่อลงประกาศงานไปยังไซต์ภายนอก คุณต้องมี [add-on การว่าจ้างที่ครอบคลุม](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)
> - เมื่อต้องการลงรายการบัญชีงานไปยัง Broadbean ผ่าน Attract คุณต้องมีการสมัครใช้งาน Broadbean
> - คุณลักษณะนี้อยู่ในการแสดงตัวอย่างในขณะนี้ ถ้าคุณต้องการลอง คุณต้อง [เปิดในการตั้งค่าการจัดการ Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)

### <a name="configure-broadbean-integration"></a>ตั้งค่าคอนฟิกการรวม Broadbean

1. ลงชื่อเข้าใช้ Attract เป็นผู้ดูแลระบบ
2. เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) ในมุมขวาบนของหน้า และจากนั้น **ศูนย์การจัดการ**
3. บนแท็บ **การตั้งค่ากระดานงาน** ในส่วน **เปิดใช้งานการรวม Broadbean** เปิดการรวม
4. ติดต่อ Broadbean และป้อนข้อมูลของคุณใน **ชื่อผู้ใช้ รหัสไคลเอนต์ โทเคนการเข้ารหัส**

> [!WARNING]
> ข้อมูลประจำตัว Broadbean ของคุณมีความสำคัญ และเป็นความลับ ดังนั้น จึงจัดเก็บ และแบ่งปันอย่างรับผิดชอบ ผู้ที่มีบทบาทผู้ดูแลระบบใน Attract สามารถดูข้อมูลประจำตัวเหล่านี้ได้

> [!NOTE]
> Microsoft และ Attract จะไม่เกี่ยวข้องในการสร้างและการรักษาค่าเหล่านี้ เป็นความรับผิดชอบของคุณในการทำให้เป็นปัจจุบันใน Attract และในการทำงานกับ Broadbean เพื่อแก้ไขปัญหาใดๆ ที่เกี่ยวข้องกับข้อมูลประจำตัวของคุณ

### <a name="post-a-job-to-broadbean"></a>ลงประกาศงานไปยัง Broadbean

หลังจากที่มีการเปิด Broadbean ผู้สรรหาและผู้ดูแลระบบสามารถลงประกาศงานได้ คุณต้องมีการใช้ URL สำหรับงาน

1. ใน Attract เปิดงานที่คุณต้องการลงประกาศงานไปยัง Broadbean
2. ในส่วน **การลงประกาศ** เลือกปุ่ม **ลงประกาศตอนนี้** ที่สอดคล้องกับ Broadbean
3. ทำตามคำแนะนำในหน้าต่าง Broadbean

Attract ส่งผ่านข้อมูลต่อไปนี้ไปยัง Broadbean:

- รหัสคำขอ
- ตำแหน่งงาน
- คำอธิบายงาน
- สถานที่ตั้งของงาน
- นำ URL ไปใช้
- ข้อมูลผู้สรรหา

หลังจาก Broadbean ลงประกาศเสร็จสมบูรณ์ ส่วน **การลงประกาศ** ของงานใน Attract แสดงสถานะ Broadbean เป็น **ลงประกาศแล้ว**

> [!NOTE]
> - Broadbean ต้องการฟิลด์ **อุตสาหกรรม** ในขณะนี้ ฟิลด์นี้ถูกตั้งค่าเป็น **IT** ตามค่าเริ่มต้น อย่างไรก็ตาม คุณสามารถเปลี่ยนค่าเป็นอุตสาหกรรมที่ถูกต้องในหน้าต่างสำหรับการลงประกาศงาน Broadbean
> - ใช้เวลานานสำหรับ Broadbean ที่จะเสร็จสิ้นการลงประกาศงานของคุณไปยังบอร์ดงานทั้งหมดที่คุณเลือก ดังนั้น จึงอาจมีความล่าช้าเล็กน้อย ก่อนที่ Attract จะให้การปรับปรุงสถานะสำหรับงาน

### <a name="view-a-broadbean-job-posting"></a>ดูการลงประกาศงาน Broadbean

หลังจากที่คุณลงประกาศงานไปยัง Broadbean คุณสามารถดูได้จาก Attract

1. ใน Attract เปิดงานที่คุณต้องการดูใน Broadbean
2. ในส่วน **การลงประกาศ** เลือกปุ่มจุดไข่ปลา (**...**) ที่สอดคล้องกับ Broadbean และจากนั้น เลือก **ดู**

การลงประกาศงาน Broadbean ปรากฏขึ้นในหน้าต่างใหม่

### <a name="update-a-broadbean-job-posting"></a>ปรับปรุงการลงประกาศงาน Broadbean

คุณสามารถปรับปรุงการลงประกาศงาน Broadbean ได้ในสองวิธี

1. ใน Attract เปิดงานที่คุณต้องการปรับปรุง
2. ในส่วน **การลงประกาศ** เลือกปุ่ม **ปรับปรุงประกาศ** ที่สอดคล้องกับ Broadbean
3. แก้ไขการลงประกาศในหน้าต่าง Broadbean

หรือ

1. ใน Attract เปิดงานที่คุณต้องการดูใน Broadbean
2. ในส่วน **การลงประกาศ** เลือกปุ่มจุดไข่ปลา (**...**) ที่สอดคล้องกับ Broadbean และจากนั้น เลือก **ดู**
3. ในหน้าต่าง Broadbean แก้ไขรายละเอียดงาน และจากนั้น ลงประกาศงานซ้ำ รายละเอียดงานใน Attract จะไม่เปลี่ยนแปลง

### <a name="remove-a-broadbean-job-posting"></a>ลบการลงประกาศงาน Broadbean

คุณสามารถลบการลงประกาศงานจาก Broadbean ได้ตามที่คุณต้องการ

1. ใน Attract เปิดงานที่คุณต้องการลบ
2. ในส่วน **การลงประกาศ** เลือกปุ่มจุดไข่ปลา (**...**) ที่สอดคล้องกับ Broadbean และจากนั้น เลือก **ลบประกาศ**

หลังจากที่ Broadbean ลบงาน รายการ Broadbean ใน Attract มีปุ่ม **ลงประกาศตอนนี้** การมีอยู่ของปุ่มนี้บ่งชี้ว่า งานถูกลบออก และสามารถลงประกาศได้อีกครั้ง

### <a name="troubleshoot-the-broadbean-integration"></a>แก้ไขปัญหาการรวม Broadbean

ถ้าคุณมีปัญหาในการลงประกาศงานไปยัง Broadbean ลองขั้นตอนเหล่านี้

1. ตรวจสอบว่าข้อมูลประจำตัวของ Broadbean ที่คุณป้อนใน Attract ใช้ได้และถูกต้อง
2. ถ้าข้อมูลประจำตัวใช้ได้และถูกต้อง ติดต่อ [ฝ่ายสนับสนุนของ Broadbean](https://www.broadbean.com/resources/support/)
3. ถ้าปัญหายังคงอยู่ ติดต่อ [ฝ่ายสนับสนุนของ Microsoft](./talent-support.md)
