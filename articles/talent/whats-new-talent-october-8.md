---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent - Core HR (8 ตุลาคม 2018)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือถูกเปลี่ยนแปลงใน Microsoft Dynamics 365 Talent - Core HR
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 30c148a1bf27a221c1d4feacbe89cabfc412872c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462715"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-8-2018"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent - Core HR (8 ตุลาคม 2018)

**สร้าง 8.1.1050.0**

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a>อนุญาตให้วันที่อื่นๆ ถูกใช้ในเกณฑ์ระดับการลาหยุด (การจัดการการลางาน)

เมื่อให้รางวัลการลางานแก่พนักงาน เกณฑ์ระดับรางวัลจะกำหนดระยะเวลาหยุดพักที่พนักงานค้างรับ ในปัจจุบัน ระดับเหล่านี้จะยึดตามวันที่เริ่มต้นของพนักงานและวันที่อายุงาน ในบางสถานการณ์ องค์กรต้องการให้ระดับเหล่านี้ขึ้นอยู่กับวันที่อื่นๆ เช่น วันที่ครบรอบปี หรือวันที่จ้างงานเดิม วันที่ดังกล่าวถูกใช้ในแผนการลางานเรียบร้อยแล้ว เพื่อกำหนดเวลาที่จะเกิดการรับรู้ ความสามารถสำหรับวันที่เหมือนกันดังกล่าวจะถูกใช้เมื่อมีการลงทะเบียนพนักงานในแผน ถูกเพิ่มเพื่อกำหนดจำนวนเงินค้างรับค้างจ่าย 

## <a name="other-changes"></a>การเปลี่ยนแปลงอื่นๆ
การแก้ไขเบ็ดเตล็ดได้ถูกรวมไว้ในรุ่นนี้

## <a name="known-issue"></a>ปัญหาที่ทราบ

**ปัญหา:** เมื่อเพิ่มสิ่งที่แนบมาใหม่ไปยังผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** ถูกแรเงา **วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่า FactBoxes ในหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน (ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)
