---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (15 ตุลาคม 2018)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d48bc4bad795611ce322b5f09b78886a50c415c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306369"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-15-2018"></a>มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (15 ตุลาคม 2018)

[!include [banner](includes/banner.md)]

**สร้าง 8.1.1056**

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR


## <a name="changes"></a>การเปลี่ยนแปลง
นอกจากการแก้ไขเบ็ดเตล็ด มีการทำการปรับปรุงต่อไปนี้ในรุ่นนี้:
- ขณะนี้วันสุดท้ายที่ทำงานถูกตั้งค่า เมื่อมีการจ้างงานหรือการตั้งค่าวันที่สิ้นสุดการจ้างงาน
- การอ้างอิงการปฏิบัติตามกฎระเบียบของสหรัฐอเมริกาถูกลบออก เมื่ออยู่ในบริษัทที่ไม่ใช่สหรัฐอเมริกา (ACA ADA และ I9)
- วันที่ไม่ถูกต้อง (1/1/1900) จะถูกซ่อนบนหน้าการวิเคราะห์ในขณะนี้

## <a name="known-issue"></a>ปัญหาที่ทราบ

**ปัญหา:** เมื่อเพิ่มสิ่งที่แนบมาใหม่ไปยังผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** ถูกแรเงา **วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่า FactBoxes ในหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน (ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)
