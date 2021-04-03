---
title: สินทรัพย์ภายในองค์กรสำหรับการให้บริการ
description: หัวข้อนี้จะอธิบายถึงวิธีการที่คุณสามารถใช้ Microsoft Dtnamics 365 Field Service เพื่อให้บริการทั้งสินทรัพย์ของลูกค้าและสินทรัพย์ภายในองค์กร
author: RamaKrishnamoorthy
manager: AnnBe
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
ms.openlocfilehash: d4d681b2362c90b69007ea44c01c886f96cc1db1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568089"
---
# <a name="in-house-assets-for-servicing"></a>สินทรัพย์ภายในองค์กรสำหรับการให้บริการ

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service ได้รับการออกแบบมาเพื่อให้บริการสินทรัพย์ของลูกค้า การจัดการสินทรัพย์สำหรับ Dynamics 365 Supply Chain Management ได้รับการออกแบบเพื่อรักษาสินทรัพย์ภายในองค์กร การรวมกันของแอปทั้งสองนี้จะช่วยให้คุณสามารถใช้ Field Service เพื่อให้บริการทั้งสินทรัพย์ของลูกค้าและสินทรัพย์ภายในองค์กร นอกจากนี้ คุณยังสามารถจัดประเภทสินทรัพย์ได้ตามตำแหน่งที่ทำงานหรือลำดับชั้น และติดตามการให้บริการในระดับที่ละเอียด

สำหรับข้อมูลเพิ่มเติม ให้ดู [รวม Dynamics 365 Field Service และ Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration)

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