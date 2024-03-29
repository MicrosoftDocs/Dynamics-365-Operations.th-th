---
title: การนำเข้า MT940 การกระทบยอดบัญชีธนาคารขั้นสูง – การอัพเกรดเอนทิตีข้อมูลแบบรวม
description: ต้องมีหมายเลขลำดับที่จะเพิ่มลงในเอนทิตีการนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940
author: angelad116
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e0cf603e04be4f8f784a32b9ef98d748d4d28e5b
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151505"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>การนำเข้า MT940 การกระทบยอดบัญชีธนาคารขั้นสูง – การอัพเกรดเอนทิตีข้อมูลแบบรวม

[!include [banner](../includes/banner.md)]

ต้องมีหมายเลขลำดับที่จะเพิ่มลงในเอนทิตีการนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940 

ใช้ขั้นตอนต่อไปนี้เพื่อเพิ่มเอนทิตีการนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940

1.  คอมไพล์และซิงโครไนส์รายการต่อไปนี้:
    -   เอนทิตีแบบรวม\\BankStatementImportEntity
    -   เอนทิตี\\BankStatementBalanceEntity
    -   เอนทิตี\\BankStatementDocumentEntity
    -   เอนทิตี\\BankStatementEntity
    -   เอนทิตี\\BankStatementLineEntity
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
            2.  ชื่อเอนทิตี = ใบแจ้งยอดจากธนาคาร
            3.  อัพโหลดไฟล์ข้อมูล = SampleBankCompositeEntity.xml เวอร์ชันใหม่
            4.  คลิก **ใช่** เพื่อบันทึกทับไฟล์ที่มีอยู่
            5.  คลิก **ใช่** เพื่อสร้างการแม็ปใหม่
            6.  ตรวจสอบว่ามีการแม็ป S **equenceNumber**
                -   คลิก **ดูแผนที่** บนเอนทิตีใบแจ้งยอด
                -   ตรวจสอบว่ามีการแม็ป **SequenceNumber** จากต้นทางไปยังการแบ่งระยะหรือไม่

3.  นำเข้าใบแจ้งยอดใหม่






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
