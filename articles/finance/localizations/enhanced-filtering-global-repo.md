---
title: การกรองข้อมูลขั้นสูงของ RCS ในที่เก็บ RCS/ส่วนกลาง
description: หัวข้อนี้จะอธิบายความสามารถในการกรองข้อมูลขั้นสูงสำหรับที่เก็บส่วนกลางของ RCS ซึ่งได้รับการปรับปรุงเพื่อรวมตัวกรองข้อมูลเพิ่มเติม
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 7df49a85de484d013518217ba8ada6c61da4b6e4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/24/2020
ms.locfileid: "3287950"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>ตัวเลือกการกรองข้อมูลขั้นสูงของ RCS สำหรับการค้นหาการตั้งค่าคอนฟิกในที่เก็บ RCS/ส่วนกลาง

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะอธิบายความสามารถในการกรองข้อมูลขั้นสูงสำหรับที่เก็บส่วนกลางของ Regulatory Configuration Services (RCS) ซึ่งได้รับการปรับปรุงเพื่อรวมความสามารถในการกรองเงื่อนไขต่อไปนี้: 
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

คุณสามารถนำเข้าผลลัพธ์ที่ถูกกรองเข้าไปในที่เก็บ RCS ของผู้ใช้หรือสภาพแวดล้อม Dynamics 365 Finance อย่างใดอย่างหนึ่ง ทีละรายการ หรือเป็นชุด เมื่อต้องการดำเนินการนี้ ให้เลือกกลุ่มการตั้งค่าคอนฟิก และคลิก **นำเข้า**
