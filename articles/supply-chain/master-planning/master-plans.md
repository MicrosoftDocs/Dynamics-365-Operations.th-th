---
title: ภาพรวมของแผนหลัก
description: ใช้แผนหลักต่างๆ เพื่อสนับสนุนการดำเนินงานประจำวันของบริษัทของคุณ จำลองกลยุทธ์การวางแผนต่างๆ ที่คุณต้องการตรวจสอบ และนำนโยบายของบริษัทมาปฏิบัติ ตัวอย่างเช่น นโยบายเกี่ยวกับประสิทธิภาพการทำงานภายในหรือความพึงพอใจของลูกค้า
author: roxanadiaconu
manager: tfehr
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: 7911
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c41013cee8620e7961fae18da9fad308c9075e84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999942"
---
# <a name="master-plans-overview"></a>ภาพรวมของแผนหลัก

[!include [banner](../includes/banner.md)]

ใช้แผนหลักต่างๆ เพื่อสนับสนุนการดำเนินงานประจำวันของบริษัทของคุณ จำลองกลยุทธ์การวางแผนต่างๆ ที่คุณต้องการตรวจสอบ และนำนโยบายของบริษัทมาปฏิบัติ ตัวอย่างเช่น นโยบายเกี่ยวกับประสิทธิภาพการทำงานภายในหรือความพึงพอใจของลูกค้า 

คุณสามารถตั้งค่าคอนฟิกแผนหลักในหน้า **แผนหลัก**

มีแผนอยู่สองชนิดด้วยกัน ดังนี้
-   **แผนถาวร**– การคำนวณการวางแผนหลักใช้ข้อมูลปัจจุบันเพื่อสร้างแผนความต้องการสุทธิ แผนนี้จะไม่เปลี่ยนแปลงจนกว่าคุณจะเรียกใช้งานการวางแผนหลักในครั้งถัดไป หรือเปลี่ยนแปลงแผนด้วยตนเอง นี่คือแผนการดำเนินการที่บุคลากรบริษัทต่างๆ เช่น ผู้ซื้อ หรือผู้วางแผนการผลิต สามารถใช้เป็นหลักในการตัดสินใจและดำเนินการกิจกรรมประจำวันของพวกเขา
-   **แผนชั่วคราว**– แผนนี้เริ่มการทำงานกับแผนความต้องการสุทธิเดียวกันซึ่งถูกสร้างขึ้นโดยการวางแผนหลัก อย่างไรก็ตาม คุณสามารถอัพเดตแผนชั่วคราวทุกครั้งที่ข้อมูลหลักเปลี่ยนแปลง อาจเป็นอย่างนี้เมื่อคุณสร้างใบสั่งขายใหม่ ตัวอย่างเช่น ช่วยให้คุณสามารถตรวจสอบเครือข่ายใบสั่งที่มีเปลี่ยนแปลงและความพร้อมของสินค้าปราศจากการรบกวนแผนถาวรที่ผู้อื่นกำลังใช้สำหรับกระบวนการทำงานของพวกเขา

บริษัทอาจเลือกที่จะทำงานกับแผนชั่วคราวเท่านั้น หรืออาจใช้ทั้งแผนถาวร และแผนชั่วคราว นอกจากนี้ คุณสามารถตั้งค่าคอนฟิกแผนหลักใดๆเพื่อสะท้อนถึงกลยุทธ์เฉพาะ หรือจัดการปัญหาหนึ่ง ๆ ตัวอย่างมีดังนี้:
-   กำหนดระดับสินค้าคงคลังที่สูงขึ้นเพื่อเพื่อรับประกันว่าไม่มีขาดแคลนสต็อก
-   กำหนดค่าเผื่อความปลอดภัยที่นานขึ้นเพื่อป้องกันปัญหาจากผู้จัดจำหน่ายที่เชื่อถือไม่ได้

คุณยังสามารถตั้งค่าแผนชั่วคราวที่เริ่มต้นเพื่อให้แผนนี้ถูกอัพเดทด้วยแผนความต้องการใหม่ทุกครั้งที่คุณรันการวางแผนหลัก คุณสามารถระบุการตั้งค่าเหล่านี้ในหน้า **พารามิเตอร์การวางแผนหลัก**



<a name="additional-resources"></a>ทรัพยากรเพิ่มเติม
--------

[การตั้งค่าความครอบคลุม](coverage-settings.md)

[การแยกการวางแผนทางเทคนิคและปฏิบัติสำหรับการจัดกำหนดการหลัก](https://blogs.msdn.com/b/axmfg/archive/2012/10/12/separating-tactical-and-operative-planning-for-master-scheduling.aspx)

[การวางแผนหลัก: ใช้แผนแบบคงที่ แผนหลักแบบไดนามิก หรือใช้แผนเดียว](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)



