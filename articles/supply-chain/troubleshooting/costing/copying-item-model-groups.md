---
title: การตั้งค่าฟิลด์ที่ขาดหายไป เมื่อมีการคัดลอกกลุ่มแบบจำลองสินค้าไปที่นิติบุคคลอื่น
description: การตั้งค่าฟิลด์ขาดหายไป เมื่อมีการคัดลอกกลุ่มแบบจำลองสินค้าไปที่นิติบุคคลอื่น
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026944"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>การตั้งค่าฟิลด์ที่ขาดหายไป เมื่อมีการคัดลอกกลุ่มแบบจำลองสินค้าไปที่นิติบุคคลอื่น

หมายเลข KB: 4612800

## <a name="symptoms"></a>อาการ

เมื่อคุณคัดลอกกลุ่มแบบจำลองสินค้าไปยังนิติบุคคล (บริษัท) อื่น โดยใช้เอนทิตี *นโยบายสินค้าคงคลังของกลุ่มแบบจำลองสินค้า* การตั้งค่าฟิลด์บางอย่าง (ตัวอย่างเช่น แบบจำลองสินค้าคงคลังและข้อความอธิบาย) จะขาดหายไปในกลุ่มแบบจำลองใหม่ในนิติบุคคลปลายทาง

## <a name="resolution"></a>ความละเอียด

เมื่อต้องการสร้างสําเนาที่สมบูรณ์ของกลุ่มแบบจำลองสินค้าไปยังนิติบุคคลอื่น คุณยังต้องเลือกทั้งนโยบายสินค้าคงคลังของกลุ่มแบบจำลองสินค้า (`InventInventoryPolicyEntity`) และนโยบายสมมติฐานกระแสต้นทุน (`InventCostFlowAssumptionPolicyEntity`) ที่สัมพันธ์กับกลุ่มแบบจำลองสินค้าด้วย
