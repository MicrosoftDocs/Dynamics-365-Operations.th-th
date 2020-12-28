---
title: แก้ไขปัญหาการนำออกใช้บางส่วนและการจัดส่งบางส่วน
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการนำออกใช้บางส่วนและการจัดส่งบางส่วนใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645959"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>แก้ไขปัญหาการนำออกใช้บางส่วนและการจัดส่งบางส่วน

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการนำออกใช้บางส่วนและการจัดส่งบางส่วนใน Microsoft Dynamics 365 Supply Chain Management

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>สถานะนำออกใช้ของใบสั่งขายยังคงถูกนำออกใช้บางส่วนแม้หลังจากออกใบแจ้งหนี้ใบสั่งขายแล้ว

### <a name="issue-description"></a>คำอธิบายปัญหา

ใบสั่งขายเป็นใบสั่งการจัดส่ง แต่มีสินค้าหนึ่งรายการขึ้นไปที่มีวิธีการจัดส่งที่แตกต่างกัน หลังจากออกใบแจ้งหนี้ใบสั่งแล้ว ยังคงมีสถานะ *นำออกใช้แล้วบางส่วน*

ตัวอย่างเช่น ใบสั่งขายมีสองสินค้ารายการ ได้แก่ หนึ่งสำหรับการจัดส่ง และหนึ่งสำหรับการเบิกสินค้า ทั้งการจัดส่งและการเบิกสินค้าเสร็จเรียบร้อยแล้ว ดังนั้น ทั้งสองรายการได้ออกใบแจ้งหนี้แล้ว อย่างไรก็ตาม สถานะนำออกใช้ยังคงแสดงเป็น *นำออกใช้แล้วบางส่วน* ซึ่งเป็นการทำให้เข้าใจผิด

### <a name="issue-resolution"></a>การแก้ไขปัญหา

สถานะนำออกใช้ใช้เฉพาะกับรายการใบสั่งที่มีการเปิดใช้งานสินค้าสำหรับการจัดการคลังสินค้าเท่านั้น สถานะนำออกใช้ยังคงเป็น *นำออกใช้บางส่วน* ในสถานการณ์นี้ Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน อาจมีการเพิ่มส่วนขยายเป็นส่วนหนึ่งของกระบวนการบันทึกการจัดส่งและการออกใบแจ้งหนี้เพื่ออัพเดตสถานะการนำออกใช้
