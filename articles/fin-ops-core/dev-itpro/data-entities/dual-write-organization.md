---
title: ลำดับชั้นขององค์กรใน Common Data Service
description: หัวข้อนี้จะอธิบายการรวมของข้อมูลเชิงองค์กรระหว่างแอพลิเคชัน Finance and Operations และ Common Data Service
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572460"
---
# <a name="organization-hierarchy-in-common-data-service"></a>ลำดับชั้นขององค์กรใน Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

เนื่องจาก Dynamics 365 Finance เป็นระบบทางการเงิน *องค์กร* เป็นแนวคิดหลัก และการตั้งค่าระบบจะเริ่มต้นด้วยการตั้งค่าคอนฟิกของลำดับชั้นขององค์กร สามารถติดตามการเงินของธุรกิจได้ที่ระดับองค์กรและที่ระดับใดก็ได้ในลำดับชั้นขององค์กร

แม้ว่า Common Data Service จะไม่มีแนวคิดของลำดับชั้นขององค์กร แต่ก็มีแนวคิดคร่าวๆ สองสามรายการ เช่น รายได้จากการขายรวม ในฐานะที่เป็นส่วนหนึ่งของการรวม Common Data Service โครงสร้างข้อมูลลำดับชั้นขององค์กรจะถูกเพิ่มไปยัง Common Data Service

## <a name="data-flow"></a>โฟลว์ข้อมูล

ระบบนิเวศทางธุรกิจที่ประกอบด้วยแอพลิเคชัน Finance and Operations และ Common Data Service จะยังคงมีลำดับชั้นขององค์กรอยู่ ลำดับชั้นขององค์กรนี้ถูกสร้างขึ้นในแอพลิเคชัน Finance and Operations แต่จะถูกเปิดเผยใน Common Data Service เพื่อวัตถุประสงค์ในการให้ข้อมูลและความสามารถในการเพิ่มฟังก์ชัน ภาพประกอบต่อไปนี้แสดงข้อมูลลำดับชั้นขององค์กรที่ถูกเปิดเผยใน Common Data Service เป็นโฟลว์ข้อมูลทางเดียวจากแอพลิเคชัน Finance and Operations ไปยัง Common Data Service

![รูปภาพของสถาปัตยกรรม](media/dual-write-data-flow.png)

## <a name="templates"></a>เท็มเพลต

แผนผังเอนทิตีลำดับชั้นขององค์กรจะพร้อมใช้งานสำหรับการซิงโครไนส์ข้อมูลแบบทางเดียวจากแอพลิเคชัน Finance and operations ไปยัง Common Data Service

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>วัตถุประสงค์ลำดับชั้นขององค์กรภายใน

เท็มเพลตนี้ให้การซิงโครไนส์แบบทางเดียวของเอนทิตีวัตถุประสงค์ลำดับชั้นขององค์กรจาก Finance and Operations ไปยังแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![architecture image](media/dual-write-purpose.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>ชนิดลำดับชั้นขององค์กรภายใน

เท็มเพลตนี้ให้การซิงโครไนส์แบบทางเดียวของเอนทิตีวัตถุประสงค์ชนิดลำดับชั้นขององค์กรจาก Finance and Operations ไปยังแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![architecture image](media/dual-write-type.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
ชื่อ | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>ลำดับชั้นขององค์กรภายใน

เท็มเพลตนี้ให้การซิงโครไนส์แบบทางเดียวของเอนทิตีลำดับชั้นที่เผยแพขององค์กรร่จาก Finance and Operations ไปยังแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![architecture image](media/dual-write-organization.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>องค์กรภายใน

ข้อมูลองค์กรภายในใน Common Data Service มาจากเอนทิตีสองรายการ **หน่วยปฏิบัติงาน** และ **นิติบุคคล**

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>หน่วยปฏิบัติงาน

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
ชื่อ | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>นิติบุคคล

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
ชื่อ | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
ไม่มี | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>บริษัท

นำเสนอข้อมูลการซิงโครไนส์แบบสองทิศทางของนิติบุคคล (บริษัท) ระหว่าง Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ

<!-- ![architecture image](media/dual-write-company.png) -->

ฟิลด์ต้นทาง | ชนิดของการแม็ป | ฟิลด์ปลายทาง
---|---|---
ชื่อ | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
