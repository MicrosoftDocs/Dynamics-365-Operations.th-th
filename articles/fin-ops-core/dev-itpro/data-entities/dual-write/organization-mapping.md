---
title: ลำดับชั้นขององค์กรใน Dataverse
description: ในหัวข้อนี้อธิบายการรวมข้อมูลองค์กรระหว่างแอป Finance and Operations กับ Dataverse
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680083"
---
# <a name="organization-hierarchy-in-dataverse"></a>ลำดับชั้นขององค์กรใน Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

เนื่องจาก Dynamics 365 Finance เป็นระบบทางการเงิน *องค์กร* เป็นแนวคิดหลัก และการตั้งค่าระบบจะเริ่มต้นด้วยการตั้งค่าคอนฟิกของลำดับชั้นขององค์กร สามารถติดตามการเงินของธุรกิจได้ที่ระดับองค์กรและที่ระดับใดก็ได้ในลำดับชั้นขององค์กร

แม้ว่า Dataverse จะไม่มีแนวคิดของลำดับชั้นขององค์กร แต่ก็มีแนวคิดคร่าวๆ สองสามรายการ เช่น รายได้จากการขายรวม ในฐานะที่เป็นส่วนหนึ่งของการรวม Dataverse โครงสร้างข้อมูลลำดับชั้นขององค์กรจะถูกเพิ่มไปยัง Dataverse

## <a name="data-flow"></a>โฟลว์ข้อมูล

ระบบแวดล้อมทางธุรกิจที่ประกอบด้วยแอป Finance and Operations และ Dataverse จะยังคงมีลำดับชั้นขององค์กรต่อไป ลำดับชั้นขององค์กรนี้สร้างขึ้นบนแอป Finance and Operations แต่เปิดเผยใน Dataverse เพื่อวัตถุประสงค์ในการให้ข้อมูลและการขยาย ภาพประกอบต่อไปนี้แสดงข้อมูลลำดับชั้นขององค์กรที่เปิดเผยใน Dataverse เป็นโฟลว์ข้อมูลทางเดียวจากแอป Finance and Operations ไปยัง Dataverse

![รูปภาพของสถาปัตยกรรม](media/dual-write-data-flow.png)

แผนผังตารางลำดับชั้นขององค์กรพร้อมใช้งานสำหรับการทำข้อมูลทางเดียวให้ตรงกันจากแอป Finance and Operations ไปยัง Dataverse

## <a name="templates"></a>เท็มเพลต

ข้อมูลผลิตภัณฑ์ ประกอบด้วยข้อมูลทั้งหมดที่เกี่ยวข้องกับผลิตภัณฑ์ และคำนิยามของผลิตภัณฑ์ เช่น มิติของผลิตภัณฑ์ หรือการติดตาม และมิติการจัดเก็บ ดังที่ตารางต่อไปนี้แสดง ชุดข้อมูลของแผนผังตารางถูกสร้างเพื่อซิงค์ผลิตภัณฑ์และข้อมูลที่เกี่ยวข้อง

แอป Finance and Operations | แอปพลิเคชันอื่น ๆ ของ Dynamics 365 | คำอธิบาย
-----------------------|--------------------------------|---
วัตถุประสงค์ลำดับชั้นขององค์กร | msdyn_internalorganizationhierarchypurposes | เท็มเพลตนี้มีการซิงโครไนส์แบบทางเดียวสำหรับเอนทิตีวัตถุประสงค์ของลำดับชั้นขององค์กร
ชนิดลำดับชั้นขององค์กร | msdyn_internalorganizationhierarchytypes | เท็มเพลตนี้มีการซิงโครไนส์แบบทางเดียวสำหรับเอนทิตีชนิดของลำดับชั้นขององค์กร
ลำดับชั้นขององค์กรที่เผยแพร่ | msdyn_internalorganizationhierarchies | เท็มเพลตนี้มีการซิงโครไนส์แบบทางเดียวสำหรับเอนทิตีที่เผยแพร่ของลำดับชั้นขององค์กร
หน่วยปฏิบัติงาน | msdyn_internalorganizations |
นิติบุคคล | msdyn_internalorganizations |
นิติบุคคล | cdm_companies | มีการซิงโครไนส์ข้อมูลของนิติบุคคล (บริษัท) สองทิศทาง

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>องค์กรภายใน

ข้อมูลองค์กรภายในใน Dataverse มาจากตารางสองรายการ **หน่วยปฏิบัติงาน** และ **นิติบุคคล**

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
