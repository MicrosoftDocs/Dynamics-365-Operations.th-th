---
title: สินทรัพย์ภายในองค์กรสำหรับการให้บริการ
description: บทความนี้จะอธิบายวิธีการที่คุณสามารถใช้ Microsoft Dynamics 365 Field Service เพื่อให้บริการทั้งสินทรัพย์ของลูกค้าและสินทรัพย์ในสถานที่
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b3e741c85fcad2abc18879280ef7332ae091c984
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289264"
---
# <a name="in-house-assets-for-servicing"></a>สินทรัพย์ภายในองค์กรสำหรับการให้บริการ

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service ได้รับการออกแบบมาเพื่อให้บริการสินทรัพย์ของลูกค้า การจัดการสินทรัพย์สำหรับ Dynamics 365 Supply Chain Management ได้รับการออกแบบเพื่อรักษาสินทรัพย์ภายในองค์กร การรวมกันของแอปทั้งสองนี้จะช่วยให้คุณสามารถใช้ Field Service เพื่อให้บริการทั้งสินทรัพย์ของลูกค้าและสินทรัพย์ภายในองค์กร นอกจากนี้ คุณยังสามารถจัดประเภทสินทรัพย์ได้ตามตำแหน่งที่ทำงานหรือลำดับชั้น และติดตามการให้บริการในระดับที่ละเอียด

สำหรับข้อมูลเพิ่มเติม ให้ดู [รวม Dynamics 365 Field Service และ Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration)

## <a name="templates"></a>เท็มเพลต

สินทรัพย์ภายในองค์กรประกอบด้วยชุดของแผนผังตารางหลักที่ทำงานร่วมกันในระหว่างการโต้ตอบข้อมูล ดังที่แสดงในตารางต่อไปนี้

| แอปการเงินและการดำเนินงาน | แอป Customer Engagement | คำอธิบาย |
|-----------------------------|-----------------------------------|-------------|
[แบบจำลองวงจรการใช้งานของสินทรัพย์ในการจัดการสินทรัพย์](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[สถานะของวงจรการใช้ของสินทรัพย์ในการจัดการสินทรัพย์](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[ชนิดสินทรัพย์ในการจัดการสินทรัพย์](mapping-reference.md#124) | msdyn_customerassetcategories | |
[สินทรัพย์ในการจัดการสินทรัพย์](mapping-reference.md#125) | msdyn_customerassets | |
[แบบจำลองวงจรการใช้งานของตำแหน่งที่ทำงานในการจัดการสินทรัพย์](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[สถานะของวงจรการใช้ของตำแหน่งที่ทำงานในการจัดการสินทรัพย์](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[ชนิดของตำแหน่งที่ทำงานในการจัดการสินทรัพย์](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[ตำแหน่งที่ทำงานในการจัดการสินทรัพย์](mapping-reference.md#136) | msdyn_functionallocations | |
[ผู้ผลิตของการจัดการสินทรัพย์](mapping-reference.md#153) | msdyn_manufacturers | |
[แบบจำลองการจัดการสินทรัพย์](mapping-reference.md#154) | msdyn_models | |
[การรับประกันของการจัดการสินทรัพย์](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
