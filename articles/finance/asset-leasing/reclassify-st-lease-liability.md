---
title: จัดประเภทส่วนระยะสั้นของหนี้สินสัญญาเช่าใหม่
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างรายการสมุดรายวันรายเดือนเพื่อจัดประเภทส่วนของหนี้สินสัญญาเช่าเป็นระยะสั้น
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 08ca824bb4c4a02a80f2187fb5f8fe4e8b7327c9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992925"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>จัดประเภทส่วนระยะสั้นของหนี้สินสัญญาเช่าใหม่

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการสร้างรายการสมุดรายวันรายเดือนเพื่อจัดประเภทส่วนของหนี้สินสัญญาเช่าเป็นระยะสั้น เมื่อกำหนดการที่เลือกไว้ในกระบวนการชุดงานจะเป็น **การจัดประเภทหนี้สินสัญญาเช่าระยะสั้น** จะมีการสร้างรายการสมุดรายวัน รายการนี้ใช้ในการลงรายการบัญชีส่วนของหนี้สินสัญญาเช่าปัจจุบันในวันสุดท้ายของเดือน ในเวลาเดียวกัน จะมีการลงรายการบัญชีการกลับรายการในวันแรกของเดือนถัดไป

โดยมีการแสดงผลของหนี้สินสัญญาเช่าระยะสั้นบนกำหนดการการตัดบัญชีหนี้สิน เมื่อลงรายการบัญชีรายการสมุดรายวัน คอลัมน์ **การจัดประเภทของหนี้สินสัญญาเช่าระยะสั้น** ที่สร้างจะพร้อมใช้งาน และรหัสสมุดรายวันจะถูกเติมด้วยในกำหนดการด้วย

เมื่อต้องการสร้างและลงรายการบัญชีรายการสมุดรายวันการจัดประเภทหนี้สินในระยะสั้น ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การเช่าสินทรัพย์ \> ประจำงวด \> การสร้างสมุดรายวันชุดงาน**
2. ในกล่องโต้ตอบ **การสร้างสมุดรายวันชุดงาน** ในฟิลด์ **เลือกกำหนดการ** ให้เลือก **จัดประเภทหนี้สินสัญญาเช่าระยะสั้น**
3. ในฟิลด์ **กลุ่มสัญญาเช่า** ให้เลือกกลุ่มสัญญาเช่า อีกทางหนึ่งคือ ในฟิลด์ **รหัสสมุดบัญชี** ให้เลือกรหัสสมุดบัญชี
4. เปิดพารามิเตอร์ **การลงรายการบัญชี** อีกทางหนึ่งคือ ถ้าควรสร้างรายการแล้วแต่ยังไม่ได้ลงรายการบัญชี ให้ปล่อยพารามิเตอร์นี้ปิด
5. เปิดใช้งานพารามิเตอร์ **การแสดงตัวอย่างก่อนที่จะลงรายการบัญชี** เพื่อดูรายการก่อนที่จะมีการลงรายการบัญชี
6. เลือก **ตกลง**
