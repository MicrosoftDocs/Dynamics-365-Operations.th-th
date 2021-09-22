---
title: ข้อผิดพลาดเกี่ยวกับค่า consumptionCost ของ BOM เมื่อพยายามสิ้นสุดใบสั่ง
description: เมื่อพยายามสิ้นสุดใบสั่งผลิต คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่าค่า consumptionCost ของ BOM ต้องเป็นค่าลบ ปัญหานี้ได้รับการแก้ไขแล้ว
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 737329d06022e899df8e4de5a27d76b21480da9e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477747"
---
# <a name="cant-end-a-production-order-because-of-a-bom-consumptioncost-value-error"></a>ไม่สามารถสิ้นสุดใบสั่งผลิตได้ เนื่องจากข้อผิดพลาดเกี่ยวกับค่า consumptionCost ของ BOM

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามสิ้นสุดใบสั่งผลิต คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:

> การคํานวณค่า consumptionCost ของ BOM ต้องเป็นค่าลบเมื่อมีการตัดสินค้าออกจากสินค้าคงคลัง

## <a name="resolution"></a>การแก้ปัญหา

มีการแก้ไขปัญหานี้ในรุ่น 10.0.15
