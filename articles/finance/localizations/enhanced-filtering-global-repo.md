---
title: การกรองข้อมูลขั้นสูงของ RCS ในที่เก็บ RCS/ส่วนกลาง
description: บทความนี้จะอธิบายความสามารถในการกรองข้อมูลขั้นสูงสำหรับที่เก็บส่วนกลางของ RCS ซึ่งได้รับการปรับปรุงเพื่อรวมตัวกรองข้อมูลเพิ่มเติม
author: kfend
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: e0408d0561c0cfead8781b9f49fdb84d5caf179a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274526"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>ตัวเลือกการกรองข้อมูลขั้นสูงของ RCS สำหรับการค้นหาการตั้งค่าคอนฟิกในที่เก็บ RCS/ส่วนกลาง

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายความสามารถในการกรองข้อมูลขั้นสูงสำหรับที่เก็บส่วนกลางของ Regulatory Configuration Services (RCS) ซึ่งได้รับการปรับปรุงเพื่อรวมความสามารถในการกรองเงื่อนไขต่อไปนี้: 
- **ประเทศ/ภูมิภาค** - ตามรหัสประเทศ ISO  
- ชนิด **แท็ก** สำหรับ:
  - พื้นที่ฟังก์ชัน
  - พื้นที่คุณลักษณะ
  - อุตสาหกรรม 
  - เอกสารทางธุรกิจ 

เพื่อทำให้ง่ายขึ้นในการค้นหาการตั้งค่าคอนฟิกที่ระบุหรือที่เกี่ยวข้อง คุณสามารถใช้ตัวกรองโดยแยกต่างหาก หรือเป็นกลุ่ม อย่างใดอย่างหนึ่ง ตัวอย่างเช่น ถ้าต้องการค้นหาชนิดเดียวของเอกสารทางธุรกิจที่สามารถตั้งค่าคอนฟิกได้ซึ่งเกี่ยวข้องใบแจ้งหนี้ของผู้จัดจำหน่าย คุณสามารถใช้ตัวกรอง **ชนิดเอกสารทางธุรกิจ** เพื่อค้นหาชนิดของเอกสารนั้นได้ 

[![ส่วนตัวกรองสำหรับที่เก็บส่วนกลาง](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

คุณสามารถปรับปรุงการค้นหาได้ด้วยการเลือกชนิดเอกสาร ตัวอย่างเช่น 'ใบแจ้งหนี้ของผู้จัดจำหน่าย' และคลิก **ใช้ตัวกรองข้อมูล** ตัวอย่างต่อไปนี้แสดงผลลัพธ์เมื่อกรองข้อมูลใน **ชนิดเอกสารทางธุรกิจ** ด้วยชนิดเอกสารที่เพิ่ม 

[![ใช้ตัวกรองและนำเข้าสำหรับชนิดเอกสารทางธุรกิจ](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

คุณสามารถนำเข้าผลลัพธ์ที่ถูกกรองเข้าไปในที่เก็บ RCS ของผู้ใช้หรือสภาพแวดล้อม Dynamics 365 Finance อย่างใดอย่างหนึ่งทีละรายการ หรือเป็นชุด เมื่อต้องการดำเนินการนี้ ให้เลือกกลุ่มการตั้งค่าคอนฟิก และคลิก **นำเข้า**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
