---
title: มีการสร้างแผนการใบสั่งขึ้นสำหรับสินค้าในสต็อกพร้อมด้วยใบสั่งผลิต
description: มีการสร้างแผนการใบสั่งถึงแม้ว่าคุณจะมีสินค้าอยู่ในสินค้าคงคลังและใบสั่งผลิตมีอยู่แล้ว
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477789"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>มีการสร้างแผนการใบสั่งขึ้นสำหรับสินค้าในสต็อกพร้อมด้วยใบสั่งผลิต

## <a name="symptoms"></a>อาการ

มีการสร้างแผนการใบสั่งถึงแม้ว่าคุณจะมีสินค้าอยู่ในสินค้าคงคลังและใบสั่งผลิตมีอยู่แล้ว

## <a name="resolution"></a>การแก้ปัญหา

คุณอาจสามารถแก้ไขปัญหานี้ได้โดยการเพิ่มค่า **จำนวนวันค่าบวก** สำหรับกลุ่มที่เกี่ยวข้องในหน้า **กลุ่มความครอบคลุม** การเปลี่ยนแปลงนี้จะทำให้ระบบตรวจสอบว่าสามารถใช้ปริมาณคงคลังคงเหลือสำหรับความต้องการได้หรือไม่ ใบสั่งที่วางแผนไว้ใหม่จะไม่ถูกสร้างขึ้นสำหรับสินค้าที่อยู่ในสินค้าคงคลัง
