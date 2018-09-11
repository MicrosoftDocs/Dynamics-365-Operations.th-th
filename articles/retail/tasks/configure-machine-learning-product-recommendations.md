--- 
title: " ตั้งค่าคอนฟิกสำหรับคำแนะนำผลิตภัณฑ์ที่ใช้ Machine Learning"
description: "กระบวนงานนี้จะรีเฟรชข้อมลในที่จัดเก็บเอนทิตี้ซึ่งระบบ Machine Learning นำไปใช้ซึ่งสนับสนุนคำแนะนำผลิตภัณฑ์ และจากนั้นจะเปิดใช้งานคำแนะนำผลิตภัณฑ์บนไคลเอนต์ POS "
author: ashishmsft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 277ffb879b80fe57deeaa2b52c1543baaf820274
ms.contentlocale: th-th
ms.lasthandoff: 02/07/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a> ตั้งค่าคอนฟิกสำหรับคำแนะนำผลิตภัณฑ์ที่ใช้ Machine Learning

[!include[task guide banner](../includes/task-guide-banner.md)]

กระบวนงานนี้จะรีเฟรชข้อมลในที่จัดเก็บเอนทิตี้ซึ่งระบบ Machine Learning นำไปใช้ซึ่งสนับสนุนคำแนะนำผลิตภัณฑ์ และจากนั้นจะเปิดใช้งานคำแนะนำผลิตภัณฑ์บนไคลเอนต์ POS  กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต

1. ไปที่ การจัดการระบบ > การตั้งค่า > ที่จัดเก็บเอนทิตี้
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ด 'RetailSales'
3. คลิก รีเฟรช
4. คลิก ตกลง
5. ปิดหน้า
6. ไปที่การขายปลีกและการค้า > การตั้งค่าศูนย์ควบคุม > พารามิเตอร์ > พารามิเตอร์การขายปลีก
7. คลิกแท็บ Machine Learning
8. เลือก 'ใช่' ในฟิลด์ เปิดใช้งานคำแนะนำผลิตภัณฑ์
    * ถ้าคุณได้รับข้อความ "ไม่สามารถดึงข้อมูลแบบจำลองคำแนะนำ" อาจเป็นเพราะคุณรีเฟรชที่จัดเก็บเอนทิตี้เมื่อเร็วๆ นี้ และระบบอาจยังปรับข้อมูลใหม่ไม่เสร็จสิ้น  โปรดรอ 2-3 ชั่วโมงแล้วลองอีกครั้ง  
9. คลิก บันทึก
10. ปิดหน้า


