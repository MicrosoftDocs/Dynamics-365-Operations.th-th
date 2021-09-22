---
title: ปริมาณไม่ถูกต้องเมื่องานการเบิกสินค้ามี LPs หลายตัว
description: เมื่อมีงานการเบิกสินค้าที่มีป้ายทะเบียนหลายใบในสถานที่เดียว ปริมาณไม่ถูกต้องสำหรับหน่วย ea ตรวจสอบว่าฟิลด์ต่อไปนี้ถูกต้อง
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477699"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>ปริมาณไม่ถูกต้องเมื่อมีหลายงานการเบิกสินค้ามี LPs ในที่ตั้งเดียว

## <a name="symptoms"></a>อาการ

เมื่อมีงานการเบิกสินค้าที่มีป้ายทะเบียนหลายใบในสถานที่เดียว ปริมาณไม่ถูกต้องสำหรับหน่วย *ea* และคุณได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:

> ปริมาณไม่ถูกต้องสำหรับหน่วย 1%

## <a name="resolution"></a>การแก้ปัญหา

ตรวจสอบว่ามีการตั้งค่า **รหัสกลุ่มลำดับของหน่วย** และ **การแปลงหน่วย** บนผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยที่นำออกใช้อย่างถูกต้อง

โปรดสังเกตว่าข้อความแสดงข้อผิดพลาดได้รับการปรับปรุงในรุ่น 10.0.15 เพื่อแสดงปริมาณที่คาดไว้ (โปรดดูที่ [4581627 KB](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)) ข้อความแสดงข้อผิดพลาดใหม่คือ:

> ปริมาณไม่ถูกต้อง ที่คาดไว้ %1 %2
