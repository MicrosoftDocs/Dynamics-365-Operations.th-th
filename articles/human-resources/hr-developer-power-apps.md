---
title: ขยาย Talent ด้วย Power Apps และ Power Automate
description: บทความนี้อธิบายถึงตัวอย่างบางอย่างของสถานการณ์สมมุติของการเพิ่มความสามารถของ Microsoft Dynamics 365 Human Resources ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4036378ca70089a9978a9bf5fb48c058a2064cdc
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689507"
---
# <a name="extend-with-power-apps-and-power-automate"></a>ขยายด้วย Power Apps และ Power Automate


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



บทความนี้อธิบายถึงตัวอย่างบางอย่างของสถานการณ์สมมุติของการเพิ่มความสามารถของ Microsoft Dynamics 365 Human Resources ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate คุณสามารถนำเข้าโซลูชันแพคเกจที่เชื่อมโยงกับแต่ละตัวอย่างไปยังสภาพแวดล้อม Power Apps ของคุณ จากนั้นคุณสามารถใช้แพคเกจเป็นคำแนะนำหรือเป็นจุดเริ่มต้นเพื่อนำสถานการณ์ที่สามารถใช้ได้กับองค์กรของคุณไปใช้

> [!IMPORTANT]
> ถ้าคุณต้องการใช้เทมเพลตและแอปที่อธิบายไว้ในหัวข้อนี้ "ตามที่เป็น" ให้แน่ใจว่าได้ทดสอบแล้วเพื่อให้แน่ใจว่าจะครอบคลุมสถานการณ์ทั้งหมดที่เกี่ยวข้องกับการนำไปใช้ของคุณโดยเฉพาะ

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

- เมื่อต้องการนำเข้าแพคเกจ ผู้ใช้ต้องมีสิทธิ์ **ผู้สร้างสภาพแวดล้อม**
- เมื่อต้องการส่งออกหรือนำเข้าแอป ผู้ใช้ต้องมีใบอนุญาตใช้ Power Apps Plan 2 หรือใบอนุญาตในการทดลองใช้ Power Apps Plan 2

## <a name="integration-with-microsoft-365-power-automate"></a>การรวมกับ Microsoft 365, Power Automate

คุณสามารถใช้แอป **การรวมกับ Microsoft 365** ในการดึงข้อมูลของทีมงานสำหรับผู้ใช้ที่ลงชื่อเข้าใช้จาก Microsoft 365 ได้ อ้างอิงผู้ปฏิบัติงานในทรัพยากรบุคคลเพื่อแยกชนิดหมายเลขประจำตัวของพนักงาน ผู้จัดการสามารถตรวจสอบวันหมดอายุของชนิดรหัสพนักงาน นอกจากนี้คุณยังสามารถส่งตัวเตือนทางอีเมลได้ถ้าชนิดรหัสพนักงานหมดอายุ Power Automate รวมกับ Power Apps เพื่อส่งจดหมายเตือนนี้ การยืนยันจะถูกส่งกลับไป Power Apps จาก Power Automate เมื่อการเตือนถูกส่งออกไป ชนิดของการระบุรหัสประจำตัว รวมถึงใบอนุญาตของพนักงานขนส่ง พาสปอร์ต และแบบฟอร์มที่ยอมรับได้อื่นๆของผู้ขับขี่

คุณสามารถขยายแอปสำหรับสถานการณ์อื่นๆ ตัวอย่างเช่น คุณสามารถใช้เพื่อแสดงข้อมูลวันหยุดพักผ่อนของทีมงาน ปฏิทินเหตุการณ์ และเหตุการณ์เฉพาะทีมงานใด ๆ

เมื่อต้องการดาวน์โหลดแอป **การรวมกับ Microsoft 365, Power Automate** ไปที่  [กาารรวมกับ Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787)  บนศูนย์ดาวน์โหลด Microsoft

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – การเชื่อมต่อและดำเนินการ SQL

เทมเพลต **Power Automate – การเชื่อมต่อและดำเนินการ SQL** เชื่อมต่อกับ Microsoft SQL Server และเปิดใช้งานให้การสอบถาม SQL เรียกใช้

ถึงแม้ว่าเทมเพลตนี้จะอ่านและอัปเดตตาราง SQL คุณสามารถขยายและใช้งานสำหรับสถานการณ์อื่นๆได้ ตัวอย่างเช่น คุณสามารถใช้เพื่อกรอกข้อมูลในตารางการจัดเตรียมใน Dataverse ด้วยเรกคอร์ดจากเซิร์ฟเวอร์ SQL และเพื่อซิงโครไนส์ตารางการจัดเตรียมเป็นระยะ ๆ โดยใช้พุชส่วนเพิ่มจากเซิร์ฟเวอร์ SQL 

การสอบถามขั้นสูงถูกรวมเข้ากับขั้นตอนในการเปิดใช้งานการแปลงข้อมูลและการผลักข้อมูลเพิ่มเติม

เมื่อต้องการดาวน์โหลดเทมเพลต **Power Automate – การเชื่อมต่อและดำเนินการ SQL** ไปที่ [Power Automate – การเชื่อมต่อและดำเนินการ SQL](https://go.microsoft.com/fwlink/?linkid=2081789) บนศูนย์ดาวน์โหลด Microsoft

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
