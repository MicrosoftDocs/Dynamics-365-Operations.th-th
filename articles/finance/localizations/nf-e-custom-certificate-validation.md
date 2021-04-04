---
title: การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการเปิดใช้งานและการใช้ใบรับรอง NF-e แบบกำหนดเอง
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240590"
---
# <a name="nf-e-custom-certificate-validation"></a>การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e

[!include [banner](../includes/banner.md)]

เมื่อคุณเปิดใช้งานคุณลักษณะการตรวจสอบใบรับรองแบบกำหนดเอง NF-E การตรวจสอบความถูกต้องแบบกำหนดเองอนุญาตให้มีการเชื่อมต่อกับบริการเว็บ การเชื่อมต่อนี้ต้องใช้เพื่อส่ง NF-E และรับการตรวจสอบจาก SEFAZ

คุณสมบัติ **จุดประสงค์การรับรองความถูกต้องเซิร์ฟเวอร์** จากการรับรอง V5 ออกโดยหน่วยงานใบรับรองหลักของบราซิล คุณสมบัตินี้ปิดใช้งานโดยค่าเริ่มต้น และต้องเปิดใช้งานด้วยตนเอง ในบางกรณี การอัปเดตใบรับรองอัตโนมัติสามารถสลับคุณสมบัตินี้เป็นไม่มีการเปิดใช้งานอีกต่อไป ถ้าเหตุการณ์นี้เกิดขึ้น การเชื่อมต่อ TLS จะได้รับผลกระทบ และไม่ได้รับความไว้วางใจอีกต่อไป ความสามารถในการออก NF-E ในสภาพแวดล้อมการผลิตสำหรับรัฐของ Minas Gerais (MG) และ Paraná (PR) มีผลกระทบ

การอัปเดตนี้ช่วยให้มีโซลูชันอีกวิธีหนึ่งสำหรับการตรวจสอบความถูกต้องของใบรับรอง ซึ่งหมายความว่าคุณสามารถสร้างการสื่อสารที่มีความปลอดภัยได้




[!INCLUDE[footer-include](../../includes/footer-banner.md)]