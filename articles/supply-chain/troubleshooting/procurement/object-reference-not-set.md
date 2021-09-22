---
title: ข้อผิดพลาด "การอ้างอิงออบเจ็กต์ไม่ได้ถูกตั้งค่า" เกิดขึ้นในระหว่างการยืนยันใบสั่งซื้อ
description: ข้อผิดพลาด "การอ้างอิงออบเจ็กต์ไม่ได้ถูกตั้งค่า" เกิดขึ้นในระหว่างการยืนยันใบสั่งซื้อ
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 78e5e365f7197c1a0c25bf6eb63bcd5bd0f482ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477761"
---
# <a name="error-object-reference-not-set-occurs-during-purchase-order-confirmation"></a>ข้อผิดพลาด "การอ้างอิงออบเจ็กต์ไม่ได้ถูกตั้งค่า" เกิดขึ้นในระหว่างการยืนยันใบสั่งซื้อ

## <a name="symptoms"></a>อาการ

คุณจะได้รับข้อยกเว้นต่อไปนี้เมื่อยืนยันใบสั่งซื้อ:

> การอ้างอิงออบเจ็กต์ไม่ได้ถูกตั้งค่า

## <a name="cause"></a>สาเหตุ

ปัญหานี้อาจเกิดขึ้นเนื่องจากความไม่สอดคล้องกันในการกระจายใบสั่งซื้อ

## <a name="resolution"></a>การแก้ปัญหา

เมื่อต้องการยกเลิกการบล็อกปัญหานี้และรีเซ็ตใบสั่งซื้อเป็นสถานะ *แบบร่าง* ให้ไปที่การ **จัดซื้อและการจัดหา \> งานประจำงวด \> ล้างข้อมูล \> รีเซ็ตการกระจายใบสั่งซื้อ** สำหรับข้อมูลเพิ่มเติมให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [แก้ไขข้อผิดพลาดในการกระจาย PO ใน Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)
