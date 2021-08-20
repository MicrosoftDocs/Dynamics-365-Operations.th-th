---
title: ลำดับชั้นขององค์กรใน Dataverse
description: ในหัวข้อนี้อธิบายการรวมข้อมูลองค์กรระหว่างแอป Finance and Operations กับ Dataverse
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 30826bf69525a85bede6ec0b64ec1a579aea26a0a6c487583739ad3fcb787a28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769257"
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

แอป Finance and Operations | แอป Customer Engagement     | คำอธิบาย
-----------------------|--------------------------------|---
[นิติบุคคล](mapping-reference.md#102) | cdm_companies | มีการซิงโครไนส์ข้อมูลของนิติบุคคล (บริษัท) สองทิศทาง
[นิติบุคคล](mapping-reference.md#142) | msdyn_internalorganizations |
[หน่วยปฏิบัติงาน](mapping-reference.md#143) | msdyn_internalorganizations |
[ลำดับชั้นขององค์กร - เผยแพร่](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | แม่แบบนี้มีการซิงโครไนส์แบบทางเดียวสำหรับตารางที่เผยแพร่ของลำดับชั้นขององค์กร
[วัตถุประสงค์ลำดับชั้นขององค์กร](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | แม่แบบนี้มีการซิงโครไนส์แบบทางเดียวสำหรับตารางวัตถุประสงค์ของลำดับชั้นขององค์กร
[ชนิดลำดับชั้นขององค์กร](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | แม่แบบนี้มีการซิงโครไนส์แบบทางเดียวสำหรับตารางชนิดของลำดับชั้นขององค์กร

## <a name="internal-organization"></a>องค์กรภายใน

ข้อมูลองค์กรภายในใน Dataverse มาจากตารางสองรายการ **หน่วยปฏิบัติงาน** และ **นิติบุคคล**

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
