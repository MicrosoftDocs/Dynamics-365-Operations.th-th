---
title: ไม่สามารถเลือกการเปลี่ยนแปลงสถานะสินค้าคงคลังเป็นชนิดงาน
description: คุณไม่สามารถสร้างรายการแม่แบบงานเพื่อเปลี่ยนแปลงสถานะสินค้าคงคลังได้ เนื่องจากชนิดงานสามารถใช้ได้โดยกระบวนการของระบบเท่านั้น เลือกชนิดงานที่แตกต่างกัน
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477774"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>ไม่สามารถเลือกการเปลี่ยนแปลงสถานะสินค้าคงคลังในคอลัมน์ชนิดงาน

## <a name="symptoms"></a>อาการ

เมื่อตั้งค่าคอนฟิก Microsoft Dynamics 365 Supply Chain Management คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:

> คุณไม่สามารถสร้างรายการแม่แบบงานเพื่อเปลี่ยนแปลงสถานะสินค้าคงคลังได้ เนื่องจากชนิดงานไม่ถูกต้อง เลือกชนิดงานที่แตกต่างกัน

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานนี้เกิดจากการออกแบบ ชนิดงาน *การเปลี่ยนสถานะสินค้าคงคลัง* จะใช้โดยกระบวนการของระบบเท่านั้น ซึ่งไม่สามารถตั้งค่าได้ เนื่องจากรายการของชนิดงานได้รับการแก้ไขเป็นการแจงนับ รายการพิเศษจะไม่สามารถถูกกรองออกจากเมนูแบบหล่นลง **ชนิดงาน**
