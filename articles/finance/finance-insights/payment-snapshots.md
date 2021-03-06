---
title: ภาพรวมของสแนปช็อต (ตัวอย่าง)
description: หัวข้อนี้อธิบายถึงลักษณะการทำงานของสแนปช็อต ซึ่งช่วยให้คุณสามารถบันทึกการคาดการณ์กระแสเงินสดสำหรับการวิเคราะห์หรือการเปรียบเทียบกับค่าจริงได้ในภายหลัง เมื่อคุณสร้างการคาดการณ์กระแสเงินสด คุณสามารถบันทึกการคาดการณ์นั้นเป็น "สแนปช็อต" คุณสามารถใช้สแนปช็อตดังกล่าวเพื่อแก้ไขบัญชีที่รวมอยู่ในการคาดการณ์ หรือเปรียบเทียบการคาดการณ์ในสแนปช็อตเป็นจริงได้
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a07749533e84cb26ce59b80e4bde12c96eaf0a3f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009354"
---
# <a name="snapshots-overview-preview"></a>ภาพรวมของสแนปช็อต (ตัวอย่าง)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

สแนปช็อตช่วยให้องค์กรสามารถแก้ไขและบันทึกข้อมูลเกี่ยวกับตำแหน่งเงินสดและการคาดการณ์เงินสดได้ในเวลาเดียวกัน คุณสามารถเปรียบเทียบสแนปช็อตกับการเงินจริง ตรวจสอบผลต่า งและใช้ข้อมูลดังกล่าวเพื่อปรับปรุงการคาดการณ์กระแสเงินสดเมื่อเวลาผ่านไป เจาะจงมากขึ้น สแนปช็อตสามารถใช้ในลักษณะต่อไปนี้:

- ติดตามตำแหน่งเงินสดและการคาดการณ์เงินสดเมื่อเวลาผ่านไป
- กรองข้อมูลเพื่อแสดงชุดย่อยของนิติบุคคลที่สร้างสแนปช็อตไว้
- แก้ไขตำแหน่งเงินสดและการคาดการณ์เงินสดที่สร้างขึ้นโดยระบบ
- ดำเนินการตามวิธีการวิเคราะห์ที่ควรพิจารณาในเชิงบวก ในเชิงลบ และมุมมองที่น่าจะเป็นไปได้ของกระแสเงินสด
- เปรียบเทียบประสิทธิภาพทางการเงินจริงกับการคาดการณ์ที่บันทึกไว้ในสแนปช็อต

คุณสามารถสร้างสแนปช็อตโดยเลือก **สแนปช็อตใหม่** บนแท็บ **ตำแหน่งเงินสด** หรือแท็บ **การคาดการณ์เงินสด** บนพื้นที่ทำงาน **การคาดการณ์กระแสเงินสด** หลังจากสร้างสแนปช็อต กระแสเข้าและกระแสออกสามารถแก้ไขและบันทึกได้ สแนปช็อตที่บันทึกไว้ทั้งหมดจะพร้อมใช้งานบนแท็บ **สแนปช็อต** เมื่อต้องการเปิดสแนปช็อต ให้เลือกชื่อของสแนปช็อต

คุณสามารถแก้ไขรายรับเงินสดและรายจ่ายเงินสดในสแนปช็อตได้ตลอดเวลา เมื่อมีการแก้ไขยอดเงินกระแสเข้าหรือยอดเงินกระแสออก จะมีการจัดสัดส่วนยอดเงินที่อัปเดตแล้วให้กับบัญชีสภาพคล่องที่ทำยอดดุลดั้งเดิม เมื่อคุณเสร็จสิ้นการแก้ไขสแนปช็อต เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ

เมื่อต้องการเปรียบเทียบหลายสแนปช็อต ให้เลือก **เปรียบเทียบสแนปช็อต** คุณสามารถเปรียบเทียบสแนปช็อตสองสแนปช็อตได้ในแต่ละครั้ง เลือกสแนปช็อตสองตัวที่จะเปรียบเทียบ แล้วเลือก **ตกลง** หน้า **เปรียบเทียบสแนปช็อต** จะแสดงการเปรียบเทียบสแนปช็อตที่เลือก แผนภูมิในส่วนด้านบนของหน้าแสดงการเปรียบเทียบเงินสดระแสเงินสดเข้า ระแสเงินสดออก และยอดดุลธนาคารในรอบระยะเวลาที่ทับซ้อนกันระหว่างสแนปช็อตสองรายการ กริดในส่วนด้านล่างแสดงการเปรียบเทียบโดยละเอียดของการคาดการณ์สองครั้งสำหรับแต่ละยอดเงินสภาพคล่อง คอลัมน์ **ผลต่าง** ในกริดแสดงผลต่างระหว่างยอดดุลในรอบระยะเวลา

เมื่อต้องการเปรียบเทียบผลลัพธ์ทางการเงินจริงกับการคาดการณ์ที่บันทึกไว้เป็นสแนปช็อต ให้เลือก **เปรียบเทียบกับค่าจริง** หน้า **เปรียบเทียบสแนปช็อต** จะแสดงการเปรียบเทียบจำนวนเงินจริงและการคาดการณ์ แผนภูมิในส่วนด้านบนของหน้าแสดงการเปรียบเทียบเงินสดระแสเงินสดเข้า ระแสเงินสดออก และยอดดุลธนาคารในรอบระยะเวลาที่ทับซ้อนกันระหว่างสแนปช็อตสองรายการ กริดในส่วนด้านล่างแสดงการเปรียบเทียบโดยละเอียดของยอดดุลจริงต่อรอบระยะเวลาและยอดดุลการคาดการณ์สำหรับแต่ละยอดเงินสภาพคล่อง คอลัมน์ **ผลต่าง** ในกริดแสดงผลต่างระหว่างยอดดุลในรอบระยะเวลากับยอดดุลการคาดการณ์

#### <a name="privacy-notice"></a>ประกาศความเป็นส่วนตัว
การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด
