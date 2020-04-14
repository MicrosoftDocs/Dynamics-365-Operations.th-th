---
title: บัตรสมาชิกของลูกค้าและคะแนนรางวัล
description: หัวข้อนี้จะอธิบายถึงการรวมข้อมูลเกี่ยวกับบัตรสมาชิกของลูกค้าและคะแนนรางวัลระหว่างแอป Finance and Operations และ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172980"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>บัตรสมาชิกของลูกค้าและคะแนนรางวัล

[!include [banner](../../includes/banner.md)]



ธุรกิจจะจัดประเภทลูกค้าและให้บริการที่ซับซ้อนตามการซื้อของลูกค้าและรูปแบบการใช้จ่าย ในชุดแอพลิเคชัน Microsoft Dynamics 365 Dynamics 365 Commerce มีโครงสร้างพื้นฐานและฟังก์ชันเพื่ออำนวยความสะดวกและจัดการบัตรสมาชิกของลูกค้า คะแนนรางวัล การกำหนดราคาตามความภักดี และประสบการณ์การซื้อตามรางวัล เมื่อข้อมูลเกี่ยวกับบัตรสมาชิกของลูกค้าและคะแนนรางวัลใน Commerce ถูกซิงค์ไปยัง Common Data service แอปที่เป็นแบบโมเดลใน Dynamics 365 สามารถใช้ข้อมูลนั้นได้ ตัวอย่างเช่น ผู้ใช้ Dynamics 365 Customer Service สามารถใช้ข้อมูลเพื่อให้บริการแบบซับซ้อนเดียวกันผ่านทางฝ่ายช่วยเหลือ

## <a name="templates"></a>เท็มเพลต

| แอป Finance and Operations | แอปที่เป็นแบบโมเดลใน Dynamics 365 | คำอธิบาย |
|-----------------------------|-----------------------------------|-------------|
| บัตรสมาชิก                | msdyn\_loyaltycards               | เท็มเพลตนี้จะซิงค์ข้อมูลเกี่ยวกับบัตรสมาชิกของลูกค้า |
| คะแนนรางวัลสำหรับสมาชิก       | msdyn\_loyaltyrewardpoints        | เท็มเพลตนี้จะซิงค์ข้อมูลเกี่ยวกับคะแนนรางวัลของลูกค้า |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
