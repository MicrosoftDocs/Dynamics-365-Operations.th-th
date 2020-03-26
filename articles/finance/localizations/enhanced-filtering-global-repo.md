---
title: การกรองข้อมูลขั้นสูงในที่เก็บ RCS/ส่วนกลาง
description: หัวข้อนี้จะอธิบายความสามารถในการกรองข้อมูลขั้นสูงสำหรับที่เก็บส่วนกลางของ RCS ซึ่งได้รับการปรับปรุงเพื่อรวมตัวกรองข้อมูลเพิ่มเติม
author: JaneA07
manager: AnnBe
ms.date: 03/03/2020
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
ms.openlocfilehash: ed5a217b8844bfc76d53370ab4c4c339f5bece36
ms.sourcegitcommit: 0dcdfedec7125562f6b33deb009a3e044a1243eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/04/2020
ms.locfileid: "3099878"
---
# <a name="enhanced-filtering-options-for-finding-configurations-in-the-global-repository"></a>ตัวเลือกการกรองข้อมูลขั้นสูงสำหรับการค้นหาการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

หัวข้อนี้จะอธิบายความสามารถในการกรองข้อมูลขั้นสูงสำหรับที่เก็บส่วนกลางของ Regulatory Configuration Services (RCS) ซึ่งได้รับการปรับปรุงเพื่อรวมตัวกรองข้อมูลต่อไปนี้: 
- **ประเทศ/ภูมิภาค** - ตามรหัสประเทศ ISO  
- **ป้าย** - สำหรับพื้นที่ทำงาน/คุณลักษณะ อุตสาหกรรม ชนิดเอกสารธุรกิจ 

คุณสามารถใช้ตัวกรองโดยแยกต่างหากหรือในกลุ่ม อย่างใดอย่างหนึ่ง เพื่อค้นหาการตั้งค่าคอนฟิกที่ระบุหรือที่เกี่ยวข้อง ตัวอย่างเช่น ถ้าต้องการค้นหาเอกสารทางธุรกิจที่ตั้งค่าคอนฟิกได้ทั้งหมดที่เกี่ยวข้องกับใบแจ้งหนี้ของผู้จัดจำหน่าย คุณสามารถใช้ตัวกรองข้อมูล **ชนิดเอกสารทางธุรกิจ** ได้ 

คุณสามารถจำกัดการค้นหาเพิ่มเติมได้โดยการเลือกรหัสประเทศและการคลิก **ใช้ตัวกรองข้อมูล**  

[![ส่วนตัวกรองสำหรับที่เก็บส่วนกลาง](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

ตัวอย่างต่อไปนี้แสดงผลลัพธ์เมื่อกรองข้อมูลใน **ชนิดเอกสารทางธุรกิจ** 

[![ใช้ตัวกรองและนำเข้าสำหรับชนิดเอกสารทางธุรกิจ](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

คุณสามารถนำเข้าผลลัพธ์ที่ถูกกรองไปยังผู้ใช้ RCS หรือสภาพแวดล้อม Dynamics 365 Finance อย่างใดอย่างหนึ่ง หรือเป็นชุด (โดยการเลือกกลุ่มการตั้งค่าคอนฟิก) และการคลิก **นำเข้า**






