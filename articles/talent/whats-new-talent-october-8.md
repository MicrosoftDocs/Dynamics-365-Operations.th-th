---
title: "มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (1 ตุลาคม 2018)"
description: "หัวข้อนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent Core HR"
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 657c19896b20a514dc5308bf7fb086085b482fec
ms.openlocfilehash: 92eb1508905309294e17b770829b1c5a22be1316
ms.contentlocale: th-th
ms.lasthandoff: 10/08/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (8 ตุลาคม 2018)

[!include [banner](includes/banner.md)]

**สร้าง 8.1.1050.0**

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a>อนุญาตให้วันที่อื่นๆ ถูกใช้ในเกณฑ์ระดับการลาหยุด (การจัดการการลางาน)

เมื่อให้รางวัลการลางานแก่พนักงาน เกณฑ์ระดับรางวัลจะกำหนดระยะเวลาหยุดพักที่พนักงานค้างรับ ในปัจจุบัน ระดับเหล่านี้จะยึดตามวันที่เริ่มต้นของพนักงานและวันที่อายุงาน ในบางสถานการณ์ องค์กรต้องการให้ระดับเหล่านี้ขึ้นอยู่กับวันที่อื่นๆ เช่น วันที่ครบรอบปี หรือวันที่จ้างงานเดิม วันที่ดังกล่าวถูกใช้ในแผนการลางานเรียบร้อยแล้ว เพื่อกำหนดเวลาที่จะเกิดการรับรู้ ความสามารถสำหรับวันที่เหมือนกันดังกล่าวจะถูกใช้เมื่อมีการลงทะเบียนพนักงานในแผน ถูกเพิ่มเพื่อกำหนดจำนวนเงินค้างรับค้างจ่าย 

## <a name="other-changes"></a>การเปลี่ยนแปลงอื่นๆ
การแก้ไขเบ็ดเตล็ดได้ถูกรวมไว้ในรุ่นนี้

## <a name="known-issue"></a>ปัญหาที่ทราบ

**ปัญหา:** เมื่อเพิ่มสิ่งที่แนบมาใหม่ไปยังผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** ถูกแรเงา **วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่า FactBoxes ในหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน (ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)

