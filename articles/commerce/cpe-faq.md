---
title: FAQ เกี่ยวกับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce
description: หัวข้อนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416027"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>FAQ เกี่ยวกับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

หัวข้อนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce

**เราสามารถใช้สภาพแวดล้อมการประเมินของ Commerce เป็นหน้าร้านอีคอมเมิร์ซสำหรับลูกค้าที่ใช้ Retail ในปัจจุบันได้หรือไม่**

ลำดับที่ สภาพแวดล้อมการประเมินของ Commerce มีไว้สำหรับการประเมินเท่านั้น ถ้าคุณต้องการสภาพแวดล้อมสำหรับลูกค้าที่ดำเนินการขายปลีกให้ติดต่อ Microsoft

**สามารถใช้สภาพแวดล้อมการประเมินของ Commerce เพื่อเตรียมใช้งานคุณลักษณะอีคอมเมิร์ซเพิ่มเติมจากแอปพลิเคชัน/สภาพแวดล้อมที่ใช้งาน Retail ได้หรือไม่**

ไม่ (ส่วนใหญ่) ส่วนประกอบการประเมิน Commerce มีอยู่เฉพาะสำหรับสภาพแวดล้อมที่ตรงกับการตั้งค่าคอนฟิกที่ระบุไว้ในคำแนะนำเกี่ยวกับข้อกำหนดเบื้องต้นและการเตรียมใช้งานเท่านั้น นอกจากนี้ ข้อมูลการสาธิตพื้นฐานที่จำเป็นจะไม่พร้อมใช้งานในสภาพแวดล้อมที่มีการปรับใช้โดยมีการนำออกใช้เริ่มต้นก่อนหน้า 10.0.8 

**ค่าใช้จ่ายอะไรบ้างที่เกี่ยวข้องในการปรับใช้สภาพแวดล้อมการประเมินของ Commerce บน Microsoft Azure ผ่าน Microsoft Dynamics Lifecycle Services (LCS)**

สภาพแวดล้อมการสาธิตของศูนย์ควบคุม Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce แบบดั้งเดิม (เครื่องเสมือน \[VM\]) จะถูกโฮสต์ในการบอกรับเป็นสมาชิก Azure ของคุณ คุณสามารถใช้เครื่องคิดเลข [Azure](https://azure.microsoft.com/pricing/calculator/) เพื่อกำหนดราคา

ส่วนประกอบอื่นๆ เช่น Commerce Scale Unit, Commerce site builder และไซต์อีคอมเมิร์ซของคุณ จะพร้อมใช้งานในฐานะการให้บริการซอฟต์แวร์ (SaaS) และโฮสต์โดย Microsoft

**ภูมิศาสตร์ Azure ใดที่ได้รับการสนับสนุนสำหรับสภาพแวดล้อมการประเมินของ Commerce ในขณะนี้**

สภาพแวดล้อมการประเมินของ Commerce สามารถปรับใช้ได้เฉพาะในภูมิศาสตร์อเมริกาเหนือเท่านั้น

**มีการดาวน์โหลดบนฮาร์ดดิสก์เสมือน (VHD) ที่มีตัวเลือกเครื่องเสมือนที่สมบูรณ์ OneBox (VM) หรือไม่?**

Dynamics 365 Commerce และ Commerce Scale Unit เป็นการให้บริการซอฟต์แวร์ (SaaS) ที่สมบูรณ์ และต้องเป็นโฮสต์แบบคลาวด์

**สามารถใช้สภาพแวดล้อมการประเมินของ Commerce ได้นานเท่าใด**

สภาพแวดล้อมการประเมินของ Commerce มีการจำกัดเวลา 30 วัน นับจากวันที่ซึ่งส่วนประกอบของ SaaS เช่น Commerce Scale Unit, Commerce site builder และไซต์อีคอมเมิร์ซของคุณ จะได้รับการเตรียมใช้งาน

**ฉันสามารถขยายขีดจำกัดเวลาสำหรับสภาพแวดล้อมการประเมินของ Commerce ได้หรือไม่**

ส่วนขยายของขีดจำกัดเวลาเป็นข้อยกเว้นของบรรทัดฐาน และจะถือว่าเป็นตามแต่ละกรณี คุณควรติดต่อคู่ค้า Microsoft ของคุณสำหรับความช่วยเหลือ

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-overview.md)

[เตรียมใช้งานสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](provisioning-guide.md)

[ตั้งค่าคอนฟิกภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-post-provisioning.md)

[ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-bopis.md)

[ตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-optional-features.md)
