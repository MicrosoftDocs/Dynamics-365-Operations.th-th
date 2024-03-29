---
title: จัดกำหนดการใบสั่งงานในวันที่และเวลาเฉพาะ
description: บทความนี้อธิบายถึงวิธีการจัดกำหนดการใบสั่งงานบนวันที่และเวลาที่ระบุในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e25d1c108e5cc90fcedc7e8f7e4bbc14052719f1
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015969"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>จัดกำหนดการใบสั่งงานในวันที่และเวลาเฉพาะ

[!include [banner](../../includes/banner.md)]

 

หากต้องจัดกำหนดการใบสั่งงานในวันที่ *และ* เวลาที่ระบุคุณ สามารถแทนที่กระบวนการจัดกำหนดการมาตรฐานในการจัดการสินทรัพย์ และสร้างกำหนดการเฉพาะสำหรับใบสั่งงาน

1. คลิก **การจัดการสินทรัพย์** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**

2. ในรายการใบสั่งงาน ให้คลิกที่รหัสใบสั่งงานในคอลัมน์ **ใบสั่งงาน**

3. คลิก **แก้ไข**

4. บนแท็บด่วน **ส่วนหัวของใบสั่งงาน** ให้ใส่วันที่เริ่มต้นและสิ้นสุด ในฟิลด์ **เริ่มต้นที่คาดไว้** และ **สิ้นสุดที่คาดไว้**

    ![รูปที่ 1](media/05-work-order-scheduling.png)

5. บนแท็บ **ทั่วไป** คลิก **กำหนดการ** เพื่อใช้กระบวนการจัดกำหนดการมาตรฐาน หรือคลิก **จัดส่ง** หากคุณต้องการมอบหมายใบสั่งงานให้กับผู้ปฏิบัติงานที่ระบุ

6. เมื่อต้องการแทนที่การจองกำลังการผลิตที่มีอยู่ใดๆ เพื่อให้แน่ใจว่าใบสั่งงานมีการจัดกำหนดการไว้ในรอบระยะเวลาที่คาวไว้ ให้ทำการเลือกเหมือนกับที่แสดงในภาพในกล่องโต้ตอบ **กำหนดการใบสั่งงาน** > ส่วน **กำลังการผลิตมีจำกัด** ซึ่งหมายความว่ากระบวนการจัดกำหนดการจะละเว้นการจองกำลังการผลิตที่มีอยู่ เนื่องจากใบสั่งงานต้องเริ่มต้นในเวลาเริ่มต้นที่คาดไว้

    ![รูปที่ 2](media/06-work-order-scheduling.png)

7. คลิก **ตกลง** เพื่อเริ่มต้นการจัดกำหนดการ

8. หากกระบวนการจัดกำหนดการมีผลในการจองซ้ำ คุณจะเห็นข้อความบนหน้าจอและคุณสามารถปรับปรุงใบสั่งงานที่เกี่ยวข้องได้

>[!NOTE]
>เมื่อต้องการจัดกำหนดการให้กับเจ้าหน้าที่บำรุงรักษาสำหรับใบสั่งงาน เจ้าหน้าที่บำรุงรักษานั้นต้องพร้อมใช้งานในวันที่และเวลาเริ่มต้นที่คาดไว้ ความพร้อมของผู้ปฏิบัติงาน ตั้งค่าใน [ปฏิทินของผู้ปฏิบัติงาน](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md) 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]