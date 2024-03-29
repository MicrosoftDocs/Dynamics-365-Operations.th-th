---
title: สร้างกฎคัมบังการแทนที่
description: 'กระบวนงานนี้มุ่งเน้นการแทนที่กฎคัมบังที่มีอยู่ด้วยกฎคัมบังที่ใหม่ในวันที่เฉพาะ '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2db44c1b43a6dc5e0ab37a7756c4eecaab468e15
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570068"
---
# <a name="create-a-replacement-kanban-rule"></a>สร้างกฎคัมบังการแทนที่

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้มุ่งเน้นการแทนที่กฎคัมบังที่มีอยู่ด้วยกฎคัมบังที่ใหม่ในวันที่เฉพาะ  สิ่งนี้มีประโยชน์ เมื่อการเปลี่ยนแปลงในขั้นตอนการผลิตและกฎการเติมสินค้าต้องถูกทำให้สอดคล้องกันและต้องถูกจัดกำหนดการ บริษัทข้อมูลสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF กระบวนงานนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสายธารคุณค่า เมื่อพวกเขาเตรียมการผลิตสำหรับขั้นตอนการผลิตที่เปลี่ยนแปลงหรือกฎการเติมสินค้าใหม่ งานนี้แทนที่กฎคัมบัง 000022 ด้วยกฎใหม่ และเพิ่มปริมาณสูงสุดจาก 48 เป็น 100 สำหรับกฎใหม่


## <a name="select-a-kanban-rule-to-replace"></a>เลือกกฎคัมบังเพื่อแทนที่
1. ไปที่กฎคัมบัง
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกกฎคัมบัง 000022  

## <a name="create-a-replacement-kanban-rule"></a>สร้างกฎคัมบังการแทนที่
1. คลิกแทนที่กฎคัมบัง
2. ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่และเวลา
    * เลือกวันที่ในอนาคต เช่น หนึ่งสัปดาห์จากนี้  นี่คือวันที่และเวลาเมื่อกฎคัมบังใหม่กลายเป็นใช้งานอยู่ และแทนที่กฎคัมบังเก่า  
    * ถ้ากฎคัมบังเปลี่ยนแปลงพาธในขั้นตอนการผลิต กิจกรรมอื่นสามารถถูกเลือกได้   ในกระบวนงานนี้ เราจะเก็บกิจกรรมไม่ได้ดำเนินการใดๆ  
3. คลิก ตกลง
    * หมายเหตุว่า กฎคัมบังใหม่ถูกสร้างเพื่อแทนที่กฎคัมบัง 000022  
    * วันที่มีผลบังคับใช้ถูกตั้งค่าโดยขึ้นกับวันที่ที่เลื่อกเมื่อคุณแทนที่กฎคัมบัง  
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกกฎคัมบังที่ถูกแทนที่ 000022  
    * หมายเหตุว่า กฎคัมบังที่ถูกแทนที่มีวันที่เดียวกับวันที่หมดอายุ เพราะนี่คือวันที่เมื่อจะหมดอายุ  
5. ในรายการ ให้เลือกแถว 1
    * เลือกกฎคัมบังใหม่ที่อยู่บนสุดของรายการ  นี่คือกฎคัมบังที่มีหมายเลขกฎคัมบังสูงสุด  
6. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
    * คลิกหมายเลขกฎคัมบัง เพื่อเปิดกฎคัมบัง  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>แก้ไขขีดจำกัดสูงสุดสำหรับกฎคัมบังการแทนที่
1. ตั้งค่าปริมาณสูงสุดเป็น '100'
    * ขยาย FastTab ปริมาณ เพื่อดูฟิลด์ปริมาณสูงสุด  การเปลี่ยนปริมาณสูงสุดเป็น 100 จะอนุญาตให้สูงสุด 100 คัมบังถูกประมวลผลได้     นี่คือขั้นตอนสุดท้ายในงานนี้  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]