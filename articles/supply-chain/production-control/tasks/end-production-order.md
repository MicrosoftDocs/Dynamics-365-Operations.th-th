---
title: ใบสั่งผลิตสิ้นสุด
description: 'กระบวนงานนี้แสดงวิธีการสิ้นสุดใบสั่งผลิต '
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f3e121fdc0f69ace15e0fa08bde0af739ef7d28
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977824"
---
# <a name="end-a-production-order"></a>ใบสั่งผลิตสิ้นสุด

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการสิ้นสุดใบสั่งผลิต  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF นี่เป็นขั้นตอนสุดท้ายจากเจ็ดขั้นตอนซึ่งอธิบายวงจรชีวิตของใบสั่งผลิต


## <a name="end-a-production-order"></a>ใบสั่งผลิตสิ้นสุด
1. ไปที่การควบคุมการผลิต > ใบสั่งผลิต > ใบสั่งผลิตทั้งหมด 
    * เลือกใบสั่งผลิตที่มีสถานะรายงานเมื่อเสร็จสมบูรณ์  
2. ในบานหน้าต่างการดำเนินการ ให้คลิก ใบสั่งผลิต
3. คลิกสิ้นสุด
    * ในหน้านี้ คุณสามารถยืนยันว่าคุณต้องการสิ้นสุดใบสั่งผลิต   
4. คลิกแท็บ ทั่วไป
5. ในฟิลด์วันที่ ให้ป้อนวันที่
6. ในฟิลด์วิธีการคิดค่าของเสีย ให้เลือก'การปันส่วน' 
    * เมื่อคุณเลือกวิธีการปันส่วน ต้นทุนจากวัสดุที่เป็นของเสียจะถูกเพิ่มไปยังสินค้าที่สำเร็จแล้ว  
7. คลิก ตกลง

## <a name="validate-calculation-results"></a>ตรวจสอบความถูกต้องของผลลัพธ์การคำนวณ
1. ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน
2. คลิกดูการเปรียบเทียบต้นทุน
    * หลังจากที่คุณสิ้นสุดใบสั่งผลิตแล้ว คุณสามารถเปรียบเทียบราคาต้นทุนประมาณกับราคาต้นทุนที่รับรู้ได้ เพื่อเรียกดูภาพรวมของผลต่างการผลิต  
