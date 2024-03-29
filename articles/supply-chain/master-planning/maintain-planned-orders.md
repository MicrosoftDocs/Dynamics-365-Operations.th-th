---
title: รักษาแผนการใบสั่ง
description: บทความนี้จะแสดงข้อมูลเกี่ยวกับวิธีการจัดการใบสั่งที่วางแผน โดยอธิบายวิธีการปรับปรุงสถานะของแผนการใบสั่ง ยืนยัน และกรองข้อมูลสำหรับแผนการใบสั่งที่มีสถานะเดียวกันเป็นแผนการใบสั่งที่เลือก
author: t-benebo
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9df39d271ae61c304f70c38a23e4249eb5920b29
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740804"
---
# <a name="maintain-planned-orders"></a>รักษาแผนการใบสั่ง

[!include [banner](../includes/banner.md)]

บทความนี้จะแสดงข้อมูลเกี่ยวกับวิธีการจัดการใบสั่งที่วางแผน โดยอธิบายวิธีการปรับปรุงสถานะของแผนการใบสั่ง ยืนยัน และกรองข้อมูลสำหรับแผนการใบสั่งที่มีสถานะเดียวกันเป็นแผนการใบสั่งที่เลือก

คุณสามารถจัดการแผนการใบสั่งจากพื้นที่ทำงาน **การวางแผนหลัก** รายการ **แผนการใบสั่ง** หรือ **แผนการใบสั่งผลิต**, **แผนการใบสั่งซื้อ** และรายการ **แผนการโอนย้าย** 

## <a name="planned-order-status"></a>สถานะของแผนการใบสั่ง
คุณสามารถใช้ฟิลด์ **สถานะ** เพื่อช่วยติดตามความคืบหน้าของคุณ ใช้ค่าต่อไปนี้

-   เมื่อการวางแผนหลักสร้างแผนการใบสั่ง แผนการใบสั่งมีสถานะเป็น **ยังไม่ได้ดำเนินการ**
-   ถ้าคุณเลือกที่จะไม่ยืนยันแผนการใบสั่ง คุณสามารถกำหนดสถานะให้กับแผนการใบสั่งนั้นเป็น **เสร็จสมบูรณ์**
-   ถ้าคุณต้องการที่จะยืนยันแผนการใบสั่ง คุณสามารถเปลี่ยนสถานะเป็น **อนุมัติแล้ว** แผนการใบสั่งที่มีสถานะ **อนุมัติแล้ว** จะได้รับการยอมรับจากการวางแผนหลัก ดังนั้นจึงไม่สามารถแก้ไขหรือลบออกได้ระหว่างการวางแผนหลักภายหลังทำงาน ถ้าต้องการทำให้สำเร็จตามนั้น ตรรกะการวางแผนคัดลอกแผนการใบสั่ง **ที่อนุมัติแล้ว** จากรุ่นแผนเก่าไปยังรุ่นแผนใหม่ในระหว่างการวางแผนหลัก

## <a name="firming-planned-orders"></a>การยืนยันแผนการใบสั่ง 
โดยการยืนยันแผนการใบสั่ง จะมีการสร้างใบสั่งจริง รายการเหล่านี้ยังสามารถเรียกได้ว่า *ถูกนำออกใช้* หรือ *ใบสั่งที่เปิด* เมื่อมียืนยันแผนการใบสั่ง แผนการใบสั่งจะถูกย้ายไปยังส่วนของใบสั่งของโมดูลที่เกี่ยวข้อง

คุณสามารถเลือกตัวเลือกการยืนยันตัวสองตัวเลือกจากหน้า **แผนการใบสั่ง**

-   **ยืนยัน** – ซึ่งจะยืนยันหนึ่งหรือหลายแผนการใบสั่งที่เลือกไว้
-   **ยืนยันทั้งหมด** – ซึ่งจะยืนยันแผนการใบสั่งทั้งหมดในตัวกรอง การใช้ **ยืนยันทั้งหมด** คุณไม่จำเป็นต้องเลือกแผนการใบสั่ง จะมีการยืนยันแผนการใบสั่งทั้งหมดภายในตัวกรอง ตัวเลือกนี้จะมีประโยชน์ถ้าคุณยืนยันแผนการใบสั่งจำนวนมาก

> [!NOTE]
> คุณสามารถติดตามแผนการใบสั่งที่ยืนยันจาก **ประวัติการยืนยัน** ภายใต้ **แบบฟอร์มแผนการใบสั่ง > ดู > ประวัติการยืนยัน**

## <a name="parallelize-firming"></a>การยืนยันแบบพร้อมกัน
ถ้าคุณกำลังวางแผนที่จะยืนยันใบสั่งหลายใบในเวลาเดียวกัน การรันกำหนดการทำงานแบบขนานอาจปรับปรุงเวลาที่ใช้ในการผลิตหรือประสิทธิภาพการทำงาน ตัวเลือกนี้จะพร้อมใช้งานเมื่อยืนยันหลายแผนการใบสั่งด้วย **ยืนยัน** หรือ **ยืนยันทั้งหมด** อย่างใดอย่างหนึ่ง พารามิเตอร์ที่พร้อมใช้งานมีดังต่อไปนี้:

-   **การยืนยันกำหนดการทำงานแบบขนาน** – ถ้า **ใช่** กระบวนการยืนยันจะถูกกำหนดการทำงานแบบขนานด้วยจำนวนเธรดที่กำหนดไว้ใน **จำนวนของเธรด**
-   **จำนวนของเธรด** –ควบคุมจำนวนเธรดที่ใช้ในการกำหนดการทำงานแบบขนานกระบวนการยืนยัน พารามิเตอร์จะแสดงเฉพาะเมื่อ **การยืนยันกำหนดการทำงานแบบขนาน** ถูกตั้งค่าเป็น **ใช่**

> [!NOTE]
> ตัวเลือกสำหรับ **การยืนยันแบบพร้อมกัน** จะแสดงเฉพาะเมื่อคุณมีใบสั่งที่วางแผนไว้มากกว่าหนึ่งรายการที่ถูกเลือกสำหรับการยืนยัน

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

- [ภาพรวมของแผนหลัก](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]