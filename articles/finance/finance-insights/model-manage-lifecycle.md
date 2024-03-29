---
title: วงจรการใช้งานการจัดการโมเดล
description: บทความนี้จะอธิบายวิธีรักษาแบบจำลองการเรียนรู้ของเครื่องขององค์กรของคุณเพื่อเพิ่มประสิทธิภาพสูงสุดการคาดการณ์ที่พวกเขาสร้างขึ้น
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 526916929e4bc079f9cea82d8ea9f80813e89b83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880916"
---
# <a name="model-management-lifecycle"></a>วงจรการใช้งานการจัดการโมเดล

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีรักษาแบบจำลองการเรียนรู้ของเครื่องขององค์กรของคุณเพื่อเพิ่มประสิทธิภาพสูงสุดการคาดการณ์ที่พวกเขาสร้างขึ้น

ขอแนะนำว่าคุณควรฝึกฝนโมเดล AI ในสภาพแวดล้อม Sandbox แล้วจากนั้น ใช้โซลูชันที่มีการจัดการเพื่อปรับใช้กับสภาพแวดล้อมการทำงานจริง วิธีการนี้ช่วยให้มั่นใจว่าการควบคุมที่ถูกต้องพร้อมสำหรับการจัดการวงจรการใช้งานของแบบจำลอง

เนื่องจากโมเดล AI ยึดตามข้อมูลใบแจ้งหนี้และข้อมูลลูกค้าที่พร้อมใช้งาน จึงเป็นเรื่องสําคัญที่สภาพแวดล้อม sandbox จะมีสําเนาข้อมูลการผลิตล่าสุด คุณสามารถเริ่มการฝึกอบรมแบบจำลองของคุณโดยปฏิบัติตามขั้นตอนต่างๆ ใน [ใช้การคาดการณ์การชำระเงินของลูกค้า](use-customer-payment-predictions.md) หลังจากที่มีการฝึกฝนแบบจำลองอีกครั้งแล้ว ให้ประเมินผลลัพธ์ตามที่อธิบายไว้ใน [ประเมินแบบจำลองการคาดการณ์การชำระเงินของลูกค้าเริ่มต้น](evaluate-payment-prediction.md) ใช้ข้อมูลใน [ปรับปรุงแบบจำลองการคาดการณ์](improve-model.md) เพื่อลองใช้กับชุดของคุณลักษณะและตัวกรองที่สามารถช่วยปรับปรุงแบบจำลองได้

เมื่อคุณพอใจกับผลลัพธ์ของการฝึกอบรมแล้ว ให้ปฏิบัติตามขั้นตอนใน [จัดสรรโมเดล AI ของคุณ](/ai-builder/distribute-model) เพื่อเปลี่ยนแบบจำลองเป็นสภาพแวดล้อมการทำงานจริงของคุณ
