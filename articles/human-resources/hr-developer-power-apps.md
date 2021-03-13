---
title: ขยาย Talent ด้วย Power Apps และ Power Automate
description: บทความนี้อธิบายถึงตัวอย่างบางอย่างของสถานการณ์การเพิ่มความสามารถของ Microsoft Dynamics 365 Human Resources ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate
author: negudava
manager: tfehr
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6885c67f42ead34b5e10cc1b1a80a88fd2d59b9
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115377"
---
# <a name="extend-with-power-apps-and-power-automate"></a>ขยายด้วย Power Apps และ Power Automate

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

บทความนี้อธิบายถึงตัวอย่างบางอย่างของสถานการณ์การเพิ่มความสามารถของ Microsoft Dynamics 365 Human Resources ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate คุณสามารถนำเข้าโซลูชันแพคเกจที่เชื่อมโยงกับแต่ละตัวอย่างไปยังสภาพแวดล้อม Power Apps ของคุณ จากนั้นคุณสามารถใช้แพคเกจเป็นคำแนะนำหรือเป็นจุดเริ่มต้นเพื่อนำสถานการณ์ที่สามารถใช้ได้กับองค์กรของคุณไปใช้

> [!IMPORTANT]
> ถ้าคุณต้องการใช้แม่แบบและแอปที่อธิบายไว้ในหัวข้อนี้ "ตามที่เป็น" ให้แน่ใจว่าได้ทดสอบแล้วเพื่อให้แน่ใจว่าจะครอบคลุมสถานการณ์ทั้งหมดที่เกี่ยวข้องกับการนำไปใช้ของคุณโดยเฉพาะ

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

- เมื่อต้องการนำเข้าแพคเกจ ผู้ใช้ต้องมีสิทธิ์ **ผู้สร้างสภาพแวดล้อม**
- เมื่อต้องการส่งออกหรือนำเข้าแอป ผู้ใช้ต้องมีใบอนุญาตใช้ Power Apps Plan 2 หรือใบอนุญาตในการทดลองใช้ Power Apps Plan 2

## <a name="integration-with-microsoft-365-power-automate"></a>การรวมกับ Microsoft 365, Power Automate

คุณสามารถใช้แอป **การรวมกับ Microsoft 365** ในการดึงข้อมูลของทีมงานสำหรับผู้ใช้ที่ลงชื่อเข้าใช้จาก Microsoft 365 อ้างอิงผู้ปฏิบัติงานในทรัพยากรบุคคลเพื่อแยกชนิดหมายเลขประจำตัวของพนักงาน ผู้จัดการสามารถตรวจสอบวันหมดอายุของชนิดรหัสพนักงาน นอกจากนี้คุณยังสามารถส่งตัวเตือนทางอีเมลได้ถ้าชนิดรหัสพนักงานหมดอายุ Power Automate รวมกับ Power Apps เพื่อส่งจดหมายเตือนนี้ การยืนยันจะถูกส่งกลับไป Power Apps จาก Power Automate เมื่อการเตือนถูกส่งออกไป ชนิดของการระบุรหัสประจำตัว รวมถึงใบอนุญาตของพนักงานขนส่ง พาสปอร์ต และแบบฟอร์มที่ยอมรับได้อื่นๆของผู้ขับขี่

คุณสามารถขยายแอปสำหรับสถานการณ์อื่นๆ ตัวอย่างเช่น คุณสามารถใช้เพื่อแสดงข้อมูลวันหยุดพักผ่อนของทีมงาน ปฏิทินเหตุการณ์ และเหตุการณ์เฉพาะทีมงานใด ๆ

เมื่อต้องการดาวน์โหลดแอป **การรวมกับ Microsoft 365, Power Automate** ให้ไปที่ [การรวมกับ Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) บนศูนย์ดาวน์โหลด Microsoft

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – การเชื่อมต่อและดำเนินการ SQL

แม่แบบ **Power Automate – การเชื่อมต่อและดำเนินการ SQL** เชื่อมต่อกับ Microsoft SQL Server และเปิดใช้งานให้การสอบถาม SQL รัน

ถึงแม้ว่าแม่แบบนี้จะอ่านและอัปเดตตาราง SQL คุณสามารถขยายและใช้งานสำหรับสถานการณ์อื่นๆได้ ตัวอย่างเช่น คุณสามารถใช้เพื่อกรอกข้อมูลในตารางการจัดเตรียมใน Dataverse ด้วยเรกคอร์ดจากเซิร์ฟเวอร์ SQL และเพื่อซิงโครไนส์ตารางการจัดเตรียมเป็นระยะ ๆ โดยใช้พุชส่วนเพิ่มจากเซิร์ฟเวอร์ SQL 

การสอบถามขั้นสูงถูกรวมเข้ากับขั้นตอนในการเปิดใช้งานการแปลงข้อมูลและการผลักข้อมูลเพิ่มเติม

เมื่อต้องการดาวน์โหลดแม่แบบ **Power Automate – การเชื่อมต่อและดำเนินการ SQL** ไปที่ [Power Automate – การเชื่อมต่อและดำเนินการ SQL](https://go.microsoft.com/fwlink/?linkid=2081789) บนศูนย์ดาวน์โหลด Microsoft

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>