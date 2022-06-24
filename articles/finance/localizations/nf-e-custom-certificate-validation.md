---
title: การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e
description: บทความนี้ให้ข้อมูลเกี่ยวกับการเปิดใช้งานและการใช้ใบรับรอง NF-e แบบกำหนดเอง
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3d69aa9d6d0ce33fbed9ba1c7a7af441e14d0d07
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875917"
---
# <a name="nf-e-custom-certificate-validation"></a>การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e

[!include [banner](../includes/banner.md)]

คุณสมบัติ **วัตถุประสงค์ของการรับรองความถูกต้องของเซิร์ฟเวอร์** จากใบรับรองที่ออกโดยหน่วยงานใบรับรองหลักของบราซิล ถูกปิดอยู่ตามค่าเริ่มต้น และต้องเปิดใช้งานด้วยตนเอง ในบางกรณี การอัปเดตใบรับรองอัตโนมัติสามารถสลับคุณสมบัตินี้เป็นไม่มีการเปิดใช้งานอีกต่อไป ถ้าเหตุการณ์นี้เกิดขึ้น การเชื่อมต่อ TLS จะได้รับผลกระทบ และจะไม่สามารถได้รับความไว้วางใจอีกต่อไป ความสามารถในการออกเอกสารทางการเงินอิเล็กทรอนิกส์ของบราซิล รุ่น 55 (NF-e) ในสภาพแวดล้อมการทำงานจริงสำหรับรัฐ Minas Gerais (MG) และ Paraná (PR) ได้รับผลกระทบ

เมื่อต้องการเปิดใช้งานการแก้ไข **การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e** ให้ไปที่ **การจัดการคุณลักษณะ** คุณลักษณะนี้ช่วยให้โซลูชันอื่นสามารถตรวจสอบความถูกต้องของใบรับรอง V5 และ V10 และอนุญาตการเชื่อมต่อกับบริการเว็บที่น่าเชื่อถือ ซึ่งต้องใช้ในการส่งผ่าน NF-e และการรับการตรวจสอบจาก SEFAZ อย่างความปลอดภัย

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
