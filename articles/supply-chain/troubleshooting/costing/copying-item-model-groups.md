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
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="481cc-103">การตั้งค่าฟิลด์ที่ขาดหายไป เมื่อมีการคัดลอกกลุ่มแบบจำลองสินค้าไปที่นิติบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="481cc-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="481cc-104">หมายเลข KB: 4612800</span><span class="sxs-lookup"><span data-stu-id="481cc-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="481cc-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="481cc-105">Symptoms</span></span>

<span data-ttu-id="481cc-106">เมื่อคุณคัดลอกกลุ่มแบบจำลองสินค้าไปยังนิติบุคคล (บริษัท) อื่น โดยใช้เอนทิตี *นโยบายสินค้าคงคลังของกลุ่มแบบจำลองสินค้า* การตั้งค่าฟิลด์บางอย่าง (ตัวอย่างเช่น แบบจำลองสินค้าคงคลังและข้อความอธิบาย) จะขาดหายไปในกลุ่มแบบจำลองใหม่ในนิติบุคคลปลายทาง</span><span class="sxs-lookup"><span data-stu-id="481cc-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="481cc-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="481cc-107">Resolution</span></span>

<span data-ttu-id="481cc-108">เมื่อต้องการสร้างสําเนาที่สมบูรณ์ของกลุ่มแบบจำลองสินค้าไปยังนิติบุคคลอื่น คุณยังต้องเลือกทั้งนโยบายสินค้าคงคลังของกลุ่มแบบจำลองสินค้า (`InventInventoryPolicyEntity`) และนโยบายสมมติฐานกระแสต้นทุน (`InventCostFlowAssumptionPolicyEntity`) ที่สัมพันธ์กับกลุ่มแบบจำลองสินค้าด้วย</span><span class="sxs-lookup"><span data-stu-id="481cc-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
