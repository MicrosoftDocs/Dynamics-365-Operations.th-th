---
title: ไซต์และคลังสินค้าแบบรวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลไซต์และคลังสินค้าระหว่าง Finance and Operations และ Dataverse
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679331"
---
# <a name="integrated-sites-and-warehouses"></a>ไซต์และคลังสินค้าแบบรวม

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



หัวข้อนี้อธิบายการรวมของข้อมูลไซต์และคลังสินค้าระหว่าง Finance and Operations และ Dataverse ไซต์และคลังสินค้าการดำเนินงานเป็นแนวคิดทั่วไปในแอพลิเคชัน Supply Chain Management มีการใช้เพื่อจำลองห่วงโซ่อุปทานของบริษัทของคุณ

## <a name="templates"></a>เท็มเพลต

ด้วยการรวมกับ Dataverse แนวคิดเหล่านี้และข้อมูลที่เกี่ยวข้องทั้งหมดจะพร้อมใช้งานใน Dataverse โดยใช้ไซต์และตารางข้อมูลคลังสินค้าในตารางต่อไปนี้

แอป Finance and Operations | แอปพลิเคชันอื่น ๆ ของ Dynamics 365 | คำอธิบาย
--------------------------|---------------------------|---
ไซต์ | msdyn_operationalsites | 
คลังสินค้า | msdyn_warehouses | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]