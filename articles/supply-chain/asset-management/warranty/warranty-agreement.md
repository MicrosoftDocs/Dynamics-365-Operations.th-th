---
title: ข้อตกลงการรับประกัน
description: หัวข้อนี้อธิบายถึงข้อตกลงการรับประกันในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7080af2059c9c9bcdd11ca0ee9c5e339cef69302
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021515"
---
# <a name="warranty-agreements"></a>ข้อตกลงการรับประกัน

[!include [banner](../../includes/banner.md)]

 


ในการจัดการสินทรัพย์คุณสามารถตั้งค่าเงื่อนไขการรับประกันซึ่งสามารถเชื่อมโยงกับสินทรัพย์หรือชนิดสินทรัพย์ได้ เงื่อนไขการรับประกันจะถูกสร้างขึ้นสำหรับรอบระยะเวลาที่ระบุ คุณสามารถตั้งค่าการรับประกันเพื่อให้ครอบคลุมบางส่วนทั้งหมด และคุณสามารถตั้งค่าเงื่อนไขที่เกี่ยวข้องกับชั่วโมง ค่าใช้จ่าย และสินค้าได้

ขั้นตอนแรกคือสร้างข้อตกลงการรับประกันของผู้จัดจำหน่ายที่คุณมีสำหรับอุปกรณ์ของคุณ หลังจากนั้นคุณจะแนบข้อตกลงการรับประกันกับสินทรัพย์หรือชนิดสินทรัพย์ ข้อตกลงการรับประกันของผู้จัดจำหน่ายจะใช้เพื่อวัตถุประสงค์ในการให้ข้อมูลเท่านั้น หากมีการตั้งค่าการรับประกันของผู้จัดจำหน่ายในสินทรัพย์ คุณจะเห็นรอบระยะเวลาที่ครอบคลุมการรับประกันของสินทรัพย์

## <a name="create-a-warranty-agreement"></a>สร้างข้อตกลงการรับประกัน

ข้อตกลงการรับประกันสามารถรวมรายการข้อตกลงต่างๆ เพื่อครอบคลุมการรับประกันสำหรับชั่วโมงทำงาน ค่าใช้จ่าย และสินค้า

1. เลือก **การจัดการสินทรัพย์** \> **ตั้งค่า** \> **สินทรัพย์** \> **การรับประกัน**
2. เลือก **ใหม่** เพื่อสร้างผลิตภัณฑ์
3. ในฟิลด์ **การรับประกัน** ป้อนรหัสการรับประกัน 
4. ในฟิลด์ **ชื่อ** ให้ป้อนคำอธิบาย

    บนแท็บด่วน **รายละเอียด** ฟิลด์ **สินทรัพย์** จะแสดงจำนวนของสินทรัพย์ที่ใช้งานอยู่ที่ใช้ข้อตกลงการรับประกัน

5. บนแท็บด่วน **รายการรับประกัน** ให้ทำตามขั้นตอนต่อไปนี้เพื่อเพิ่มรายการที่ควรรวมอยู่ในข้อตกลงการรับประกัน:

    1. เลือก **เพิ่มรายการ** เพื่อเพิ่มเงื่อนไขใหม่ไปยังการับประกัน มีการป้อนหมายเลขรายการตามลำดับโดยอัตโนมัติในฟิลด์ **รายการ**
    2. ในฟิลด์ **รอบระยะเวลา** ให้เลือกชนิดของรอบระยะเวลาการรับประกัน
    3. ในฟิลด์ **ช่วงเวลา** ให้ป้อนตัวเลข ฟิลด์นี้จะกำหนดจำนวนของรอบระยะเวลาที่การรับประกันควรมีผลบังคับใช้
    4. ในฟิลด์ **เปอร์เซ็นต์** ให้ป้อนเปอร์เซ็นต์ความครอบคลุมสำหรับรายการการรับประกัน เปอร์เซ็นต์บ่งชี้ว่าบริษัทของคุณครอบคลุมมากน้อยเพียงใด

![หน้าการรับประกัน](media/01-warranty.png)
