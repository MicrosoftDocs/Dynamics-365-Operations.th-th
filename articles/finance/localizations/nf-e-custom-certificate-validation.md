---
title: การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการเปิดใช้งานและการใช้ใบรับรอง NF-e แบบกำหนดเอง
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
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755602"
---
# <a name="nf-e-custom-certificate-validation"></a>การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e

[!include [banner](../includes/banner.md)]

คุณสมบัติ **วัตถุประสงค์ของการรับรองความถูกต้องของเซิร์ฟเวอร์** จากใบรับรองที่ออกโดยหน่วยงานใบรับรองหลักของบราซิล ถูกปิดอยู่ตามค่าเริ่มต้น และต้องเปิดใช้งานด้วยตนเอง ในบางกรณี การอัปเดตใบรับรองอัตโนมัติสามารถสลับคุณสมบัตินี้เป็นไม่มีการเปิดใช้งานอีกต่อไป ถ้าเหตุการณ์นี้เกิดขึ้น การเชื่อมต่อ TLS จะได้รับผลกระทบ และจะไม่สามารถได้รับความไว้วางใจอีกต่อไป ความสามารถในการออกเอกสารทางการเงินอิเล็กทรอนิกส์ของบราซิล รุ่น 55 (NF-e) ในสภาพแวดล้อมการทำงานจริงสำหรับรัฐ Minas Gerais (MG) และ Paraná (PR) ได้รับผลกระทบ

เมื่อต้องการเปิดใช้งานการแก้ไข **การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e** ให้ไปที่ **การจัดการคุณลักษณะ** คุณลักษณะนี้ช่วยให้โซลูชันอื่นสามารถตรวจสอบความถูกต้องของใบรับรอง V5 และ V10 และอนุญาตการเชื่อมต่อกับบริการเว็บที่น่าเชื่อถือ ซึ่งต้องใช้ในการส่งผ่าน NF-e และการรับการตรวจสอบจาก SEFAZ อย่างความปลอดภัย

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
