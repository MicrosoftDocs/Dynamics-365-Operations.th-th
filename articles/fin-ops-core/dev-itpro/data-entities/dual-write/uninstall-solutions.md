---
title: ถอนการติดตั้งโซลูชันการประสานรวมของแอปพลิเคชันการรวมแบบสองทิศทาง
description: บทความนี้อธิบายวิธีการถอนการติดตั้งโซลูชันการประสานรวมของแอปพลิเคชันการรวมแบบสองทิศทาง
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 676802ddabac69db4947cf806e9103f67cece3de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870387"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>ถอนการติดตั้งโซลูชันการประสานรวมของแอปพลิเคชันการรวมแบบสองทิศทาง

[!include [banner](../../includes/banner.md)]

บทความนี้อธิบายวิธีการถอนการติดตั้งโซลูชันการประสานรวมของแอปพลิเคชันการรวมแบบสองทิศทาง

ลูกค้าบางรายติดตั้งแพคเกจการประสานรวมของแอปพลิเคชันการรวมแบบสองทิศทางโดยไม่ได้ตั้งใจ ทำให้มีการติดตั้งโซลูชันหลายตัวในสภาพแวดล้อม Microsoft Dataverse การติดตั้งโซลูชันพิเศษในแพคเกจอาจทําให้เกิดปัญหาที่ไม่คาดคิดและไม่พึงประสงค์

เมื่อต้องการแก้ปัญหาที่เกี่ยวข้องกับการติดตั้งแพคเกจการประสานรวมของแอปพลิเคชันการรวมแบบสองทิศทาง ให้ถอนการติดตั้งโซลูชันการรวมแบบสองทิศทางที่ไม่ต้องการตามลำดับต่อไปนี้

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (ถ้ามี)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (เมื่อต้องการถอนการติดตั้งโซลูชันนี้ คุณต้องเปิดตั๋วการสนับสนุนกับ Microsoft)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

ถ้ามีการติดตั้งโซลูชันฝ่ายและสมุดที่อยู่สากลแล้ว ให้ถอนการติดตั้งโซลูชันในลำดับต่อไปนี้:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. ฝ่าย
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
