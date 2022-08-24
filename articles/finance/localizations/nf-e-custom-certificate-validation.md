---
title: การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e
description: บทความนี้ให้ข้อมูลเกี่ยวกับการเปิดใช้งานและการใช้ใบรับรอง NF-e แบบกำหนดเอง
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288558"
---
# <a name="nf-e-custom-certificate-validation"></a>การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e

[!include [banner](../includes/banner.md)]

คุณสมบัติ **วัตถุประสงค์ของการรับรองความถูกต้องของเซิร์ฟเวอร์** จากใบรับรองที่ออกโดยหน่วยงานใบรับรองหลักของบราซิล ถูกปิดอยู่ตามค่าเริ่มต้น และต้องเปิดใช้งานด้วยตนเอง ในบางกรณี การอัปเดตใบรับรองอัตโนมัติสามารถสลับคุณสมบัตินี้เป็นไม่มีการเปิดใช้งานอีกต่อไป ถ้าเหตุการณ์นี้เกิดขึ้น การเชื่อมต่อ TLS จะได้รับผลกระทบ และจะไม่สามารถได้รับความไว้วางใจอีกต่อไป ความสามารถในการออกเอกสารทางการเงินอิเล็กทรอนิกส์ของบราซิล รุ่น 55 (NF-e) ในสภาพแวดล้อมการทำงานจริงสำหรับรัฐ Minas Gerais (MG) และ Paraná (PR) ได้รับผลกระทบ

เมื่อต้องการเปิดใช้งานการแก้ไข **การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e** ให้ไปที่ **การจัดการคุณลักษณะ** คุณลักษณะนี้ช่วยให้โซลูชันอื่นสามารถตรวจสอบความถูกต้องของใบรับรอง V5 และ V10 และอนุญาตการเชื่อมต่อกับบริการเว็บที่น่าเชื่อถือ ซึ่งต้องใช้ในการส่งผ่าน NF-e และการรับการตรวจสอบจาก SEFAZ อย่างความปลอดภัย

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
