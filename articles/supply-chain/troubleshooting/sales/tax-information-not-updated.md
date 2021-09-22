---
title: ไม่มีการอัพเดตข้อมูลภาษี ถ้ามีการเปลี่ยนแปลงที่ตั้งใบสั่งขาย
description: ถ้ามีการเปลี่ยนแปลงไซต์, คลังสินค้า, หรือที่อยู่ที่จัดส่ง ในส่วนหัวของใบสั่งขาย จะไม่มีการอัพเดตข้อมูลภาษีกรณีและปัญหาในรายการ คุณต้องทำงานนี้ด้วยตนเอง
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477744"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>ข้อมูลภาษีไม่ได้รับการอัพเดต ถ้ามีการเปลี่ยนแปลงที่ตั้งบนส่วนหัวของใบสั่งขาย

## <a name="symptoms"></a>อาการ

ถ้ามีการเปลี่ยนแปลงไซต์, คลังสินค้า, หรือที่อยู่ที่จัดส่ง ในส่วนหัวของใบสั่งขาย จะไม่มีการอัพเดตข้อมูลภาษีกรณีและปัญหาในรายการ

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานนี้เกิดจากการออกแบบ ปัญหานี้เกิดขึ้นเนื่องจากที่อยู่จัดส่ง, ไซต์, และคลังสินค้า ไม่มีการเปลี่ยนแปลงโดยอัตโนมัติในระดับรายการ คุณต้องอัปเดตด้วยตนเอง
