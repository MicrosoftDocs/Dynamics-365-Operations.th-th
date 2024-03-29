---
title: กฎโครงแบบ
description: บทความนี้ให้ข้อมูลทั่วไปเกี่ยวกับกฎโครงแบบ กฎโครงแบบกำหนดความสัมพันธ์ระหว่างสินค้าในรายการวัสดุและส่วนประกอบ (BOM) สำหรับผลิตภัณฑ์ที่ใช้เทคโนโลยีการจัดโครงแบบตามมิติ
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ddc74777ae0cde5367667f93eb29ffb21531e02
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570788"
---
# <a name="configuration-rules"></a>กฎโครงแบบ

[!include [banner](../includes/banner.md)]

บทความนี้ให้ข้อมูลทั่วไปเกี่ยวกับกฎโครงแบบ กฎโครงแบบกำหนดความสัมพันธ์ระหว่างสินค้าในรายการวัสดุและส่วนประกอบ (BOM) สำหรับผลิตภัณฑ์ที่ใช้เทคโนโลยีการจัดโครงแบบตามมิติ

กฎโครงแบบพร้อมใช้งานเมื่อคุณกำหนดแบบจำลองการจัดโครงแบบตามมิติ กฎโครงแบบถูกใช้เพื่อบังคับใช้ หรือไม่อนุญาตในการรวมสินค้าเฉพาะในสูตรการผลิต (BOM) หลัง BOM ได้ถูกสร้างแล้วและสินค้าเกี่ยวข้องได้ถูกกำหนดให้กับกลุ่มการกำหนดค่าที่สอดคล้องกันของพวกเขา มากกว่าหนึ่งกฎโครงแบบสามารถถูกกำหนดได้ ถ้าสินค้าสองรายการอยู่ร่วมกัน ตัวดำเนินการ **ที่เลือก** ถูกใช้เพื่อให้แน่ใจว่าเป็นการรวม ถ้าสินค้าสองรายการเป็นแบบเฉพาะร่วมกัน ตัวดำเนินการ **ที่ยกเลิกการเลือก** ถูกใช้เพื่อให้แน่ใจว่าเป็นข้อยกเว้น  

**หมายเหตุ:** ข้อมูลนี้ใช้กับผลิตภัณฑ์หลักเท่านั้นที่ใช้เทคโนโลยีการจัดโครงแบบตามมิติ  

โครงแบบที่มีอยู่ไม่ได้รับผลกระทบจากการเปลี่ยนแปลงในเวลาต่อมากับกฎโครงแบบ อย่างไรก็ตาม เป็นสิ่งสำคัญที่คุณได้ตั้งค่ากฎก่อนที่คุณกำหนดโครงแบบใหม่ และให้คุณตรวจสอบกฎถ้าคุณคิดว่ากฏได้ถูกเปลี่ยนแปลง  

**หมายเหตุ:** สำหรับวิธี **ที่เลือก** กลุ่มการปรับเปลี่ยนที่ได้รับ หมายเลขสินค้า และโครงแบบที่ถูกเลือกโดยอัตโนมัติ สำหรับวิธี **ที่ยกเลิกการเลือก** กลุ่มการปรับเปลี่ยนที่ได้รับ หมายเลขสินค้า และโครงแบบไม่สามารถเลือกได้

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของการจัดโครงแบบผลิตภัณฑ์ตามมิติ](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]