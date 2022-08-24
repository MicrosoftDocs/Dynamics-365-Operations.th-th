---
title: บัตรสมาชิกของลูกค้าและคะแนนรางวัล
description: บทความนี้จะอธิบายถึงการรวมข้อมูลเกี่ยวกับบัตรสมาชิกของลูกค้าและคะแนนรางวัลในการรวมแบบสองทิศทาง
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 399682b3042c32fbf6fa200213f1b4982ed97174
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289128"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>บัตรสมาชิกของลูกค้าและคะแนนรางวัล

[!include [banner](../../includes/banner.md)]



ธุรกิจจะจัดประเภทลูกค้าและให้บริการที่ซับซ้อนตามการซื้อของลูกค้าและรูปแบบการใช้จ่าย ตัวอย่างเช่น Dynamics 365 Commerce มีโครงสร้างพื้นฐานและฟังก์ชันเพื่ออำนวยความสะดวกและจัดการบัตรสมาชิกของลูกค้า คะแนนรางวัล การกำหนดราคาตามความภักดี และประสบการณ์การซื้อตามรางวัล เมื่อข้อมูลเกี่ยวกับบัตรสมาชิกของลูกค้าและคะแนนรางวัลใน Commerce ถูกซิงค์ไปยัง Dataverse แอปการมีส่วนร่วมของลูกค้าสามารถใช้ข้อมูลนั้นได้ ตัวอย่างเช่น ผู้ใช้ Dynamics 365 Customer Service สามารถใช้ข้อมูลเพื่อให้บริการแบบซับซ้อนเดียวกันผ่านทางฝ่ายช่วยเหลือ

## <a name="templates"></a>เทมเพลต

แอปการเงินและการดำเนินงาน | แอปการมีส่วนร่วมของลูกค้า     | คำอธิบาย
|-----------------------------|-----------------------------------|-------------|
[บัตรสมาชิก](mapping-reference.md#149) | msdyn_loyaltycards | เทมเพลตนี้จะซิงค์ข้อมูลเกี่ยวกับบัตรสมาชิกของลูกค้า |
[ระดับของสมาชิก](mapping-reference.md#226) | msdyn_loyaltylevels | เทมเพลตนี้จะซิงค์ข้อมูลเกี่ยวกับคะแนนรางวัลของลูกค้า |
[คะแนนรางวัลสำหรับสมาชิก](mapping-reference.md#150) | msdyn_loyaltyrewardpoints | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
