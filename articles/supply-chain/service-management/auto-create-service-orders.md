---
title: สร้างใบสั่งบริการโดยอัตโนมัติ
description: คุณสามารถสร้างใบสั่งบริการที่ขึ้นกับข้อตกลงการให้บริการได้ สำหรับรอบระยะเวลาที่มีผลบังคับใช้ของข้อตกลงการให้บริการ
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53369ef2b7ff93ae4f0523accbc31cc88575a383
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010683"
---
# <a name="automatically-create-service-orders"></a>สร้างใบสั่งบริการโดยอัตโนมัติ 

[!include [banner](../includes/banner.md)]


คุณสามารถสร้างใบสั่งบริการที่ขึ้นกับข้อตกลงการให้บริการได้ สำหรับรอบระยะเวลาที่มีผลบังคับใช้ของข้อตกลงการให้บริการ

ใบสั่งบริการที่คุณสร้างจากข้อตกลงการให้บริการจะถูกแนบกับข้อตกลงการให้บริการทั้งหมด

ใบสั่งบริการมีการสร้างขึ้นโดยอัตโนมัติจากการตั้งค่าต่อไปนี้

  - ช่วงเวลาของข้อตกลงการให้บริการที่ถูกตั้งค่าในรายการข้อตกลงการให้บริการ ช่วงเวลาของข้อตกลงการให้บริการบ่งชี้ความถี่ที่มีการสร้างรายการใบสั่งบริการ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ช่วงเวลาการให้บริการ](service-intervals.md)

  - รอบระยะเวลาที่คุณระบุเพื่อกำหนดรอบระยะเวลาการบริการในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ในแบบฟอร์ม **สร้างใบสั่งบริการ** สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างใบสั่งบริการโดยอัตโนมัติ](create-service-orders-automatically.md)

  - ตัวเลือก **รวมใบสั่งบริการ** บนส่วนหัวของข้อตกลงการให้บริการ ตัวเลือกนี้กำหนดว่าจะมีการสร้างรายการใบสั่งบริการจากข้อตกลงการให้บริการ จะรวมใบสั่งบริการตามพนักงาน ภารกิจการให้บริการ วัตถุที่ให้บริการ หรือข้อตกลงการให้บริการ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รวมใบสั่งบริการ](combine-service-orders.md)

  - ตัวเลือก **กรอบเวลา** ในรายการข้อตกลงการให้บริการ กรอบเวลากำหนดว่ารายการใบสั่งบริการสามารถย้ายไปได้ไกลเพียงใด เมื่อคำนึงถึงวันที่ที่คำนวณได้ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [หน้าต่างเวลา](time-windows.md)


> [!NOTE]
> <P>ถ้าวันที่ถูกระบุสำหรับใบสั่งบริการไม่เปิดขึ้นในปฏิทินที่คุณได้เลือกไว้ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการงานบริการ</STRONG> ข้อความจะแจ้งว่า มีความขัดแย้งของปฏิทิน คุณสามารถละเว้นข้อความนี้ได้อย่างปลอดภัย; และจะมีการสร้างใบสั่งบริการขึ้น แม้ว่าวันจะปิดอยู่ในปฏิทิน</P>

## <a name="example-1"></a>ตัวอย่างที่ 1

ข้อตกลงการให้บริการมีผลตั้งแต่วันที่ 1 มกราคม 2012 จนถึงวันที่ 31 ธันวาคม 2012 ถ้ารอบระยะเวลาการให้บริการที่คุณระบุในแบบฟอร์ม **สร้างใบสั่งบริการ** เริ่มตั้งแต่ 1 พฤศจิกายน 2012 จนถึงวันที่ 1 กุมภาพันธ์ 2013 จะมีการสร้างใบสั่งบริการตั้งแต่ 1 พฤศจิกายน 2012 จนถึงวันที่ 31 ธันวาคม 2012

## <a name="example-2"></a>ตัวอย่างที่ 2

ข้อตกลงการให้บริการมีผลตั้งแต่วันที่ 1 มกราคม 2012 จนถึงวันที่ 31 ธันวาคม 2012 รายการข้อตกลงการให้บริการสองรายการถูกแนบไปยังข้อตกลงการให้บริการ รายการข้อตกลงการให้บริการแรกมีวันที่เริ่มต้นเมื่อวันที่ 2 มกราคม 2012 และวันที่สิ้นสุดเมื่อวันที่ 1 มีนาคม 2012 รายการข้อตกลงการให้บริการที่สองมีวันที่เริ่มต้นเมื่อวันที่ 1 เมษายน 2012 และวันที่สิ้นสุดเมื่อวันที่ 31 ธันวาคม 2012 คุณระบุรอบระยะเวลาในแบบฟอร์ม **สร้างใบสั่งบริการ** ที่เริ่มตั้งแต่วันที่ 1 ตุลาคม 2012 จนถึงวันที่ 31 ธันวาคม 2012 ดังนั้น ใบสั่งบริการจะถูกสร้างสำหรับรายการข้อตกลงที่สองเท่านั้น เนื่องจากวันที่เริ่มต้นและวันที่สิ้นสุดของรายการข้อตกลงแรกสิ้นสุดก่อนรอบระยะเวลาที่คุณระบุไว้สำหรับใบสั่งบริการ

  


