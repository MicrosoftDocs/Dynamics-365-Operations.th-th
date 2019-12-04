---
title: ลงประกาศงานใน Broadbean จาก Attract
description: หัวข้อนี้อธิบายวิธีการใช้ Attract Dynamics 365 Talent เพื่อลงประกาศงานใน Broadbean
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
ms.openlocfilehash: 41fa057606887069a9ea0f1f2178eeaff59f33ca
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832682"
---
# <a name="post-jobs-to-broadbean-from-attract"></a>ลงประกาศงานใน Broadbean จาก Attract

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract ช่วยให้คุณได้ผู้ที่มีความสามารถพิเศษที่คุณต้องการโดยให้คุณสามารถลงประกาศงานของคุณได้โดยตรงจาก Attract ไปที่ Broadbean หลังจากคุณ [สร้างงาน](./creating-jobs-attract.md) แล้ว สิ่งที่คุณต้องทำก็คือคลิกปุ่มเพื่อนำงานของคุณไปไว้ด้านหน้าของผู้สมัครงานที่อาจเกิดขึ้นทั้งหมดใน Broadbean

การลงประกาศงานไปยัง Broadbean ต้องใช้ใบอนุญาต Broadbean ที่เหมาะสม Broadbean ให้ข้อเสนอผลิตภัณฑ์และแผนต่างๆ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการกำหนดราคาและการอนุญาตใช้งาน Broadbean [ให้ติดต่อ Broadbean](https://www.broadbean.com/contact-us/)

ถ้าคุณเป็นผู้ดูแลที่ต้องการข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกการรวม Broadbean กับ Attract ให้ดู [เปิดใช้งานการรวม Broadbean ใน Microsoft Dynamics 365 Talent - Attract](./attract-admin-job-board-settings.md)

## <a name="post-jobs-to-broadbean"></a>ลงประกาศงานใน Broadbean

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
2. บนแท็บ **การลงประกาศ** เลือกปุ่มจุดไข่ปลา (**...**) ที่สอดคล้องกับ Broadbean และจากนั้น เลือก **ดู**

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

### <a name="troubleshoot-job-posting-to-broadbean"></a>แก้ไขปัญหาการลงประกาศงานไปยัง Broadbean

ถ้าคุณมีปัญหาในการลงประกาศงานไปยัง Broadbean ลองขั้นตอนเหล่านี้

1. ตรวจสอบว่าข้อมูลประจำตัวของ Broadbean ที่คุณป้อนใน Attract ใช้ได้และถูกต้อง
2. ถ้าข้อมูลประจำตัวใช้ได้และถูกต้อง ติดต่อ [ฝ่ายสนับสนุนของ Broadbean](https://www.broadbean.com/resources/support/)
3. ถ้าปัญหายังคงอยู่ ติดต่อ [ฝ่ายสนับสนุนของ Microsoft](./talent-support.md)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[สร้าง อนุมัติ และลงรายการบัญชีงานใน Attract](./creating-jobs-attract.md)

[เปิดใช้งานการรวม Broadbean ใน Microsoft Dynamics 365 Talent - Attract](./attract-admin-job-board-settings.md)
