---
title: อัพเดตคู่มือการเตรียมความพร้อมใน Dynamics 365 for Talent - Onboard
description: หัวข้อนี้อธิบายถึงวิธีการอัพเดตคู่มือการเตรียมความพร้อมใน Microsoft Dynamics 365 for Talent - Onboard และวิธีการส่งการเปลี่ยนแปลงไปยังคู่มือที่มีอยู่
author: andreabichsel
manager: ''
ms.date: 06/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d2be450685724510db2f0fd2af8545f8f40278e7
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731664"
---
# <a name="update-onboarding-guides-in-dynamics-365-for-talent-onboard"></a>อัพเดตคู่มือการเตรียมความพร้อมใน Dynamics 365 for Talent: Onboard

[!include [banner](includes/banner.md)]

ถ้าคุณต้องทำการเปลี่ยนแปลงคู่มือการเตรียมความพร้อมใน Microsoft Dynamics 365 for Talent: Onboard คุณสามารถอัพเดตได้และส่งการเปลี่ยนแปลง ถึงแม้ว่าคุณจะได้ส่งคู่มือนี้แล้ว คุณมีตัวเลือกสำหรับการอัพเดตคู่มือการเตรียมความพร้อมสองตัวเลือก

- แก้ไขคู่มือการเตรียมความพร้อมโดยตรง และบันทึกการเปลี่ยนแปลงของคุณ
- แก้ไขเท็มเพลการเตรียมความพร้อม แล้วส่งการเปลี่ยนแปลงไปยังคู่มือการเตรียมความพร้อมทั้งหมดที่สร้างขึ้นแล้ว

## <a name="edit-an-onboarding-guide-directly"></a>แก้ไขคู่มือการเตรียมความพร้อมโดยตรง

1. บนเมนูด้านซ้าย ให้เลือก **คู่มือ**
2. เลือกคู่มือที่คุณต้องการแก้ไข
3. ทำการเปลี่ยนแปลงที่ต้องการทั้งหมด แล้วเลือกปุ่ม **บันทึก** (สัญลักษณ์ดิสก์)

    ![[การบันทึกการเปลี่ยนแปลงไปยังคู่มือการเตรียมความพร้อม](./media/onboard-save.png)](./media/onboard-save.png)

Onboard จะส่งอีเมลที่ระบุว่าการเปลี่ยนแปลงนั้นมีอะไรบ้างไปยังพนักงานใหม่โดยอัตโนมัติ สำหรับการระบุรหัสประจำตัวอย่างง่าย ป้าย **ใหม่** สีแดงจะปรากฏขึ้นถัดจากการเปลี่ยนแปลงแต่ละรายการ

## <a name="update-multiple-guides-by-editing-the-onboarding-template"></a>อัพเดตคู่มือหลายรายการโดยการแก้ไขเท็มเพลตการเตรียมความพร้อม

1. บนเมนูด้านซ้าย ให้เลือก **เท็มเพลต**
2. ภายใต้ **เท็มเพลตของฉัน** เลือกเท็มเพลตที่คุณต้องการแก้ไข
3. ทำการเปลี่ยนแปลงที่ต้องการทั้งหมด แล้วเลือกปุ่ม **บันทึก** (สัญลักษณ์ดิสก์)
4. เมื่อต้องการส่งการเปลี่ยนแปลงของคุณไปยังคู่มือทั้งหมดที่สร้างขึ้นตามเท็มเพลต ให้เลือก **ส่งการเปลี่ยนแปลงเหล่านี้**

    ![[การส่งการเปลี่ยนแปลงในเท็มเพลตการเตรียมความพร้อมไปยังคู่มือทั้งหมดที่สร้างขึ้นแล้ว](./media/onboard-push-changes.png)](./media/onboard-push-changes.png)

การเปลี่ยนแปลงจะมองเห็นได้โดยพนักงานใหม่ที่เปิดคู่มือการเตรียมความพร้อม อย่างไรก็ตาม Onboard จะไม่ส่งการแจ้งเตือนทางอีเมลให้กับพนักงานใหม่เพื่อแจ้งว่ามีการเปลี่ยนแปลงคู่มือการเตรียมความพร้อมของตน สำหรับการระบุรหัสประจำตัวอย่างง่าย ป้าย **ใหม่** สีแดงจะปรากฏขึ้นถัดจากการเปลี่ยนแปลงแต่ละรายการ 
