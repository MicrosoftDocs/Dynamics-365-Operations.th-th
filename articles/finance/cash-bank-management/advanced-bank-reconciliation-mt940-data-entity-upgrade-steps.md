---
title: การนำเข้า MT940 การกระทบยอดบัญชีธนาคารขั้นสูง – การอัพเกรดเอนทิตี้ข้อมูลแบบรวม
description: ต้องมีหมายเลขลำดับที่จะเพิ่มลงในเอนทิตี้การนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88eb5b3c408d36620ab550b29d2e5a3278d25d8a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188475"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>การนำเข้า MT940 การกระทบยอดบัญชีธนาคารขั้นสูง – การอัพเกรดเอนทิตี้ข้อมูลแบบรวม

[!include [banner](../includes/banner.md)]

ต้องมีหมายเลขลำดับที่จะเพิ่มลงในเอนทิตี้การนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940 

ใช้ขั้นตอนต่อไปนี้เพื่อเพิ่มเอนทิตี้การนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940

1.  คอมไพล์และซิงโครไนส์รายการต่อไปนี้:
    -   เอนทิตี้แบบรวม\\BankStatementImportEntity
    -   เอนทิตี้\\BankStatementBalanceEntity
    -   เอนทิตี้\\BankStatementDocumentEntity
    -   เอนทิตี้\\BankStatementEntity
    -   เอนทิตี้\\BankStatementLineEntity
    -   ตาราง\\BankStatementStaging

2.  การจัดการข้อมูล\\โครงการข้อมูล
    1.  โครงการการนำเข้า MT940 ของจำนวนงานในศูนย์การผลิต
        1.  เปลี่ยน XSLT
            -   คลิก **ดูแผนที่**
            -   คลิก **ดูแผนที่** บนเอกสารใบแจ้งยอดจากธนาคาร
            -   คลิก **การแปลงข้อมูล**
            -   ลบไฟล์ BankReconiliation-to-Composite.xslt
            -   เพิ่ม BankReconiliation-to-Composite.xsl เวอร์ชันใหม่

        2.  แสดงข้อมูล **หมายเลขลำดับ** ในโครงร่าง **แหล่งข้อมูล**
            1.  รูปแบบข้อมูลต้นทาง = XML-Element
            2.  ชื่อเอนทิตี้ = ใบแจ้งยอดจากธนาคาร
            3.  อัพโหลดไฟล์ข้อมูล = SampleBankCompositeEntity.xml เวอร์ชันใหม่
            4.  คลิก **ใช่** เพื่อบันทึกทับไฟล์ที่มีอยู่
            5.  คลิก **ใช่** เพื่อสร้างการแม็ปใหม่
            6.  ตรวจสอบว่ามีการแม็ป S**equenceNumber**
                -   คลิก **ดูแผนที่** บนเอนทิตี้ใบแจ้งยอด
                -   ตรวจสอบว่ามีการแม็ป **SequenceNumber** จากต้นทางไปยังการแบ่งระยะหรือไม่

3.  นำเข้าใบแจ้งยอดใหม่




