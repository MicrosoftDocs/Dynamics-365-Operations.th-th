---
title: ความสามารถในการเพิ่มฟังก์ชันการแจงนับฐานเพศ
description: บทความนี้แสดงภาพรวมของความสามารถในการเพิ่มฟังก์ชันการแจงนับฐานเพศ (enum)
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749323"
---
# <a name="gender-base-enum-extensibility"></a>ความสามารถในการเพิ่มฟังก์ชันการแจงนับฐานเพศ

การแจงนับ **เพศ** (enum) สามารถขยายได้แล้ว บทความนี้อธิบายการเปลี่ยนแปลงที่คุณต้องทำในฐานโค้ดถ้าคุณวางแผนที่จะขยายการแจงนับ **เพศ**

## <a name="gender-vs-hcmpersongender"></a>เพศเปรียบเทียบกับ HcmPersonGender

มีการแจงนับเกี่ยวกับค่าเพศอยู่สองรายการดังนี้

- **เพศ** (แพลตฟอร์มของแอปพลิเคชัน)
- **HcmPersonGender** (PersonnelManagement)

การแจงนับ **เพศ** ใช้ใน Microsoft Dynamics 365 Finance ส่วน **HcmPersonGender**  ใช้เฉพาะกับฟังก์ชันการจัดการทุนมนุษย์ (HCM) เท่านั้น ถ้าคุณใช้ฟังก์ชัน HCM และคุณทำการเปลี่ยนแปลงการแจงนับ **เพศ** คุณควรพิจารณาทำการเปลี่ยนแปลงเดียวกันกับ **HcmPersonGender** ตัวอย่างเช่น ถ้าคุณเพิ่ม **Transgender** ในการแจงนับ **เพศ** ให้เพิ่ม **Transgender** ในการแจงนับ **HcmPersonGender** ด้วย

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (คลาส)

มีการสร้างคลาส **HcmPersonGenderTranformUtil** ใหม่เพื่อให้สามารถแปลระหว่างตัวแจงฐานสองตัว ในคลาสนี้ จะมีสองวิธี: **convertGenderToHcmPersonGender** และ **convertHcmPersonGenderToGender** คุณควรสร้างส่วนขยายโดยใช้คลาส **Chain of Command** หรือ **ตัวจัดการเหตุการณ์** และขยายทั้งสองวิธีเพื่อแมปค่าใหม่ที่เพิ่มลงในการแจงนับฐาน

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (คลาส)

**PayrollStateWageTaxPrepDP** เป็นคลาสตัวให้บริการข้อมูลสำหรับรายงาน SQL Server Reporting Services (SSRS) ของ **การจัดเตรียมภาษีค่าจ้างของรัฐสำหรับบัญชีค่าจ้าง** สำหรับสหรัฐอเมริกา มีค่าสามค่า: **ชาย**, **หญิง** และ **ไม่ระบุ** ในวิธีการ **populatePayrollStateWageTaxPrepTmp** มีคำสั่งสลับที่ใช้แมปค่าของการแจงนับ **HcmPersonGender** กับหนึ่งในสามฟิลด์: **IsMale**, **IsFemale** หรือ **IsUnspecifiedGender** ค่าเริ่มต้นสำหรับคำสั่งสลับคือ **IsUnspecifiedGender** ถ้าคุณเพิ่มค่าใดๆ ในการแจงนับ **HcmPersonGender** เพื่อการแมปที่แตกต่างกัน คุณต้องสร้างส่วนขยายโดยใช้คลาส **Chain of Command** กับวิธีการ **populatePayrollStateWageTaxPrepTmp** เพื่อเปลี่ยนค่าตามความต้องการ

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (คลาส)

คลาสการรวม **smmOutlookSync_Contact** เชื่อมโยงค่าไปยังและจาก **Outlook** และ **ผู้ติดต่อ** **Outlook** รองรับสามค่า: **ชาย**, **หญิง** และ **ไม่ระบุ** คลาสมีสองวิธีในการช่วยในการแมป **เพศ** กับ **OutlookGenders** วิธีการเริ่มต้นคือ **NonSpecific/UnSpecified** หากคุณสร้างค่าเพิ่มเติมสำหรับการแจงนับ **เพศ** คุณควรสร้างส่วนขยายโดยใช้คลาส **Chain of Command** กับทั้งสองวิธีการและแมปตามต้องการ
