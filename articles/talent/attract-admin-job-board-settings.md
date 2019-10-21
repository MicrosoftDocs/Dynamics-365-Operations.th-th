---
title: เปิดใช้งานการรวม Broadbean ใน Microsoft Dynamics 365 Talent - Attract
description: หัวข้อนี้อธิบายถึงวิธีการตั้งค่าคอนฟิก Microsoft Dynamics 365 Talent - Attract เพื่อลงรายการบัญชีงานไปยังบอร์ดงานภายนอก เช่น Broadbean
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 808f91fb4b68ba9b5cee54d86423d23232df23a4
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008604"
---
# <a name="enable-broadbean-integration"></a>เปิดใช้งานการรวม Broadbean

[!include[banner](../includes/banner.md)]

คุณต้องการเรียกดูตำแหน่งที่เปิดของคุณ ข้างหน้าผู้สมัครที่มีคุณสมบัติหลายรายที่สุดที่เป็นไปได้ ไซต์การสรรหาบุคลากร เช่น Broadbean ช่วยให้คุณบรรลุถึงเป้าหมายนี้ Microsoft Dynamics 365 Talent: Attract: ตอนนี้สามารถช่วยให้คุณลงประกาศงานไปยัง Broadbean ได้แล้ว และ Microsoft ได้ให้ข้อเสนอใหม่ในพื้นที่นี้ตลอดเวลา

> [!NOTE]
> - เพื่อลงประกาศงานไปยังไซต์ภายนอก คุณต้องมี [add-on การว่าจ้างที่ครอบคลุม](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)
> - เมื่อต้องการลงรายการบัญชีงานไปยัง Broadbean ผ่าน Attract คุณต้องมีการสมัครใช้งาน Broadbean
> - คุณลักษณะนี้อยู่ในการแสดงตัวอย่างในขณะนี้ ถ้าคุณต้องการลอง คุณต้อง [เปิดในการตั้งค่าการจัดการ Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)

## <a name="configure-broadbean-integration"></a>ตั้งค่าคอนฟิกการรวม Broadbean

1. ลงชื่อเข้าใช้ Attract เป็นผู้ดูแลระบบ

2. เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) ในมุมขวาบนของหน้า และจากนั้น **ศูนย์การจัดการ**

3. ติดต่อ Broadbean และป้อนข้อมูลของคุณใน **ชื่อผู้ใช้** **รหัสไคลเอนต์** และฟิลด์ **โทเคนการเข้ารหัส**

4. เลือก **บันทึก**

> [!WARNING]
> ข้อมูลประจำตัว Broadbean ของคุณมีความสำคัญ และเป็นความลับ ดังนั้น จึงจัดเก็บ และแบ่งปันอย่างรับผิดชอบ ผู้ที่มีบทบาทผู้ดูแลระบบใน Attract สามารถดูข้อมูลประจำตัวเหล่านี้ได้

> [!NOTE]
> Microsoft และ Attract จะไม่เกี่ยวข้องในการสร้างและการรักษาค่าเหล่านี้ เป็นความรับผิดชอบของคุณในการทำให้เป็นปัจจุบันใน Attract และในการทำงานกับ Broadbean เพื่อแก้ไขปัญหาใดๆ ที่เกี่ยวข้องกับข้อมูลประจำตัวของคุณ
