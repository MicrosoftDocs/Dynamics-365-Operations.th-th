---
title: สินทรัพย์ภายในองค์กรสำหรับการให้บริการ
description: หัวข้อนี้จะอธิบายวิธีการที่คุณสามารถใช้ Microsoft Dynamics 365 Field Service เพื่อให้บริการทั้งสินทรัพย์ของลูกค้าและสินทรัพย์ในสถานที่
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941425"
---
# <a name="in-house-assets-for-servicing"></a>สินทรัพย์ภายในองค์กรสำหรับการให้บริการ

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service ได้รับการออกแบบมาเพื่อให้บริการสินทรัพย์ของลูกค้า การจัดการสินทรัพย์สำหรับ Dynamics 365 Supply Chain Management ได้รับการออกแบบเพื่อรักษาสินทรัพย์ภายในองค์กร การรวมกันของแอปทั้งสองนี้จะช่วยให้คุณสามารถใช้ Field Service เพื่อให้บริการทั้งสินทรัพย์ของลูกค้าและสินทรัพย์ภายในองค์กร นอกจากนี้ คุณยังสามารถจัดประเภทสินทรัพย์ได้ตามตำแหน่งที่ทำงานหรือลำดับชั้น และติดตามการให้บริการในระดับที่ละเอียด

สำหรับข้อมูลเพิ่มเติม ให้ดู [รวม Dynamics 365 Field Service และ Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration)

## <a name="templates"></a>เท็มเพลต

สินทรัพย์ภายในองค์กรประกอบด้วยชุดของแผนผังตารางหลักที่ทำงานร่วมกันในระหว่างการโต้ตอบข้อมูล ดังที่แสดงในตารางต่อไปนี้

| แอป Finance and Operations | แอปที่เป็นแบบโมเดลใน Dynamics 365 | คำอธิบาย |
|-----------------------------|-----------------------------------|-------------|
| แบบจำลองวงจรการใช้งานของสินทรัพย์ในการจัดการสินทรัพย์ | msdyn\_assetlifecyclemodels | |
| สถานะของวงจรการใช้ของสินทรัพย์ในการจัดการสินทรัพย์ | msdyn\_assetlifecyclestates | |
| สินทรัพย์ในการจัดการสินทรัพย์ | msdyn\_customerassets | |
| ชนิดสินทรัพย์ในการจัดการสินทรัพย์ | msdyn\_customerassetcategories | |
| แบบจำลองวงจรการใช้งานของตำแหน่งที่ทำงานในการจัดการสินทรัพย์ | msdyn\_functionallocationlifecyclemodels | |
| สถานะของวงจรการใช้ของตำแหน่งที่ทำงานในการจัดการสินทรัพย์ | msdyn\_functionallocationlifecyclestates | |
| ตำแหน่งที่ทำงานในการจัดการสินทรัพย์ | msdyn\_functionallocations | |
| ชนิดของตำแหน่งที่ทำงานในการจัดการสินทรัพย์ | msdyn\_functionallocationtypes | |
| ผู้ผลิตของการจัดการสินทรัพย์ | msdyn\_manufacturers | |
| แบบจำลองการจัดการสินทรัพย์ | msdyn\_models | |
| การรับประกันของการจัดการสินทรัพย์ | msdyn\_warranties | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]