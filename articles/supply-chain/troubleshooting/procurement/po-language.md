---
title: ใบสั่งซื้อไม่ได้สะท้อนถึงการตั้งค่าภาษาของนิติบุคคล
description: ชื่อผลิตภัณฑ์ในใบสั่งซื้อจะแสดงอยู่ในภาษาของระบบแทนที่จะเป็นภาษาที่ตั้งค่าไว้สำหรับนิติบุคคลที่มีการสร้างใบสั่งซื้อ
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
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477729"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>ใบสั่งซื้อไม่ได้สะท้อนถึงการตั้งค่าภาษาของนิติบุคคล


## <a name="symptoms"></a>อาการ

ชื่อผลิตภัณฑ์ในใบสั่งซื้อจะแสดงอยู่ในภาษาของระบบแทนที่จะเป็นภาษาที่ตั้งค่าไว้สำหรับนิติบุคคลที่มีการสร้างใบสั่งซื้อ

## <a name="reproduce-the-issue"></a>สร้างปัญหาอีกครั้ง

กระบวนการต่อไปนี้แสดงวิธีหนึ่งที่จะสร้างปัญหาอีกครั้ง

1. ตั้งค่าภาษาของระบบเป็น *EN-US* (ภาษาอังกฤษอเมริกัน)
1. ตรวจสอบให้แน่ใจว่ามีผลิตภัณฑ์ที่ภาษา *EN-US* และ *DE* (เยอรมัน) ถูกรักษาไว้สำหรับการแปลชื่อผลิตภัณฑ์
1. เปลี่ยนภาษาของนิติบุคคลที่จะเป็น *DE*
1. ในนิติบุคคลที่มีการตั้งค่าเป็นภาษา *DE* ให้สร้างใบสั่งซื้อที่มีผลิตภัณฑ์
1. โปรดสังเกตว่าชื่อผลิตภัณฑ์ยังคงแสดงอยู่ในภาษาอังกฤษแบบอเมริกัน (ภาษาของระบบ)

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานนี้เกิดจากการออกแบบ ในใบสั่งซื้อ ผลิตภัณฑ์จะแสดงอยู่ในภาษาของระบบเสมอ ใช้ภาษาของใบสั่งซื้อเมื่อสร้างสมุดรายวันการยืนยัน
