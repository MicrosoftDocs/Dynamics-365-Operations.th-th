---
title: แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาที่สามารถช่วยคุณแก้ไขปัญหาเกี่ยวกับการซิงโครไนส์ที่เริ่มใช้งานจริง
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59c8bd80b167cdfaa7a65e469f4dc7ebf8f50844
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744624"
---
# <a name="troubleshoot-live-synchronization-issues"></a>แก้ไขปัญหาการซิงโครไนส์ที่เริ่มใช้งานจริง

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse กล่าวคือ จะแสดงข้อมูลที่สามารถช่วยคุณแก้ไขปัญหาเกี่ยวกับการซิงโครไนส์ที่เริ่มใช้งานจริง

> [!IMPORTANT]
> ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD) ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>การซิงโครไนส์ที่เริ่มใช้งานจริงแสดงข้อผิดพลาด 403 ไม่ได้รับอนุญาต เมื่อคุณสร้างแถวในแอป Finance and Operations

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณสร้างแถวในแอป Finance and Operations:

*\[{\\"ข้อผิดพลาด\\":{\\"รหัส\\":\\"0x80072560\\",\\"ข้อความ\\":\\"ผู้ใช้ไม่ใช่สมาชิกขององค์กร\\"}}\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต"}}"*

เมื่อต้องการแก้ไขปัญหานี้ ให้ทำตามขั้นตอนใน [ข้อกำหนดของระบบและข้อกำหนดเบื้องต้น](requirements-and-prerequisites.md) เมื่อต้องการดำเนินการตามขั้นตอนดังกล่าวให้เสร็จสมบูรณ์ ผู้ใช้แอพลิเคชันการรวมแบบสองทิศทางที่สร้างขึ้นใน Dataverse ต้องมีบทบาทผู้ดูแลระบบ นอกจากนี้ ทีมงานที่เป็นเจ้าของเริ่มต้นต้องมีบทบาทผู้ดูแลระบบ

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>การซิงโครไนส์ที่เริ่มใช้งานจริงสำหรับตารางใดๆ แสดงข้อผิดพลาดที่คล้ายกันอย่างสม่ำเสมอ เมื่อคุณสร้างแถวในแอป Finance and Operations

**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ

คุณอาจได้รับข้อความแสดงข้อผิดพลาดเช่นต่อไปนี้ทุกครั้งที่คุณพยายามบันทึกข้อมูลตารางในแอป Finance and Operations:

*ไม่สามารถบันทึกการเปลี่ยนแปลงไปยังฐานข้อมูล หน่วยของงานไม่สามารถส่งธุรกรรมได้ ไม่สามารถเขียนข้อมูลไปยังเอนทิตี้ uoms ได้ เขียนไปยัง UnitOfMeasureEntity ล้มเหลว โดยมีข้อความแสดงข้อผิดพลาดว่า ไม่สามารถซิงค์กับเอนทิตี้ uoms ได้*

เมื่อต้องการแก้ไขปัญหานี้ คุณต้องตรวจสอบให้แน่ใจว่ามีข้อมูลอ้างอิงของข้อกำหนดเบื้องต้นอยู่ในทั้งแอป Finance and Operations และ Dataverse ตัวอย่างเช่น ถ้าลูกค้าที่คุณอยู่ในแอป Finance and Operations เป็นของกลุ่มลูกค้าหนึ่งๆ โปรดตรวจสอบให้แน่ใจว่ามีกลุ่มลูกค้าอยู่ใน Dataverse

ถ้ามีข้อมูลอยู่ในทั้งสองด้าน และคุณยืนยันว่าปัญหานี้ไม่เกี่ยวข้องกับข้อมูล ให้ทำตามขั้นตอนต่อไปนี้

1. หยุดตารางที่เกี่ยวข้อง
2. ลงชื่อเข้าใช้ในแอป Finance and Operations และตรวจสอบให้แน่ใจว่ามีแถวสำหรับตารางที่ล้มเหลวอยู่ในตาราง DualWriteProjectConfiguration และตาราง DualWriteProjectFieldConfiguration ตัวอย่างเช่น นี่คือลักษณะของแบบสอบถาม ถ้าตาราง **ลูกค้า** ล้มเหลว

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. ถ้ามีแถวสำหรับตารางที่ล้มเหลว แม้แต่หลังจากที่คุณหยุดการแม็ปตาราง ให้ลบแถวที่เกี่ยวข้องกับตารางที่ล้มเหลว ทำให้บันทึกของคอลัมน์ **projectname** ในตาราง DualWriteProjectConfiguration และดึงข้อมูลแถวในตาราง DualWriteProjectFieldConfiguration โดยใช้ชื่อโครงการเพื่อลบแถว
4. เริ่มต้นการแม็ปตาราง ตรวจสอบว่าข้อมูลถูกซิงค์โดยไม่มีปัญหาใดๆ หรือไม่

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>จัดการข้อผิดพลาดของสิทธิ์ในการอ่านหรือเขียน เมื่อคุณสร้างข้อมูลในแอป Finance and Operations

คุณอาจได้รับข้อความแสดงข้อผิดพลาด "คำขอไม่ถูกต้อง" ซึ่งคล้ายกับตัวอย่างต่อไปนี้ เมื่อคุณสร้างข้อมูลในแอป Finance and Operations

![ตัวอย่างของข้อความแสดงข้อผิดพลาด คำขอไม่ถูกต้อง](media/error_record_id_source.png)

เมื่อต้องการแก้ไขปัญหานี้ คุณต้องกำหนดบทบาทความปลอดภัยที่ถูกต้องให้กับทีมงานของหน่วยธุรกิจของ Dynamics 365 Sales หรือ Dynamics 365 Customer Service เพื่อเปิดใช้งานสิทธิ์ที่ขาดหายไป

1. ในแอป Finance and Operations ให้ค้นหาหน่วยธุรกิจที่ถูกแม็ปในชุดการเชื่อมต่อการรวมข้อมูล

    ![การแม็ปองค์กร](media/mapped_business_unit.png)

2. ลงชื่อเข้าใช้ในสภาพแวดล้อมในแอปที่เป็นแบบโมเดลใน Dynamics 365 นำทางไปยัง **การตั้งค่า \> การรักษาความปลอดภัย** และค้นหาทีมงานของหน่วยธุรกิจที่ถูกแม็ป

    ![ทีมงานของหน่วยธุรกิจที่ถูกแม็ป](media/setting_security_page.png)

3. เปิดหน้าสำหรับทีมงานสำหรับการแก้ไข และจากนั้น เลือก **จัดการบทบาท** เพื่อเปิดกล่องโต้ตอบ **จัดการบทบาทของทีมงาน**

    ![ปุ่มจัดการบทบาท](media/manage_team_roles.png)

4. กำหนดบทบาทที่มีสิทธิ์อ่าน/เขียนสำหรับตารางที่เกี่ยวข้อง และจากนั้น เลือก **ตกลง**

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>แก้ปัญหาการซิงโครไนส์ในสภาพแวดล้อมที่มีสภาพแวดล้อม Dataverse ที่มีการเปลี่ยนแปลงล่าสุด

**บทบาทที่จำเป็นในการแก้ไขปัญหา:** ผู้ดูแลระบบ

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณสร้างข้อมูลในแอป Finance and Operations:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**ไม่สามารถสร้างส่วนข้อความสำหรับเอนทิตี้ CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"การสร้างส่วนข้อความล้มเหลวโดยมีข้อผิดพลาด URI ที่ไม่ถูกต้อง: URI ว่างเปล่า"}\],"isErrorCountUpdated":true}*

นี่คือลักษณะของข้อผิดพลาดในแอปที่เป็นแบบโมเดลใน Dynamics 365:

*เกิดข้อผิดพลาดที่ไม่คาดคิดจากรหัส ISV (ErrorType = ClientError) ข้อยกเว้นที่ไม่คาดคิดจากปลั๊กอิน (ดำเนินการ): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: ล้มเหลวในการประมวลผลบัญชีเอนทิตี้ - (ความพยายามในการเชื่อมต่อล้มเหลว เนื่องจากฝ่ายที่เชื่อมต่อไม่ได้ตอบสนองอย่างถูกต้องหลังจากระยะเวลาหนึ่ง หรือการเชื่อมต่อที่สร้างล้มเหลว เนื่องจากโฮสต์ที่เชื่อมต่อล้มเหลวในการตอบสนอง*

ข้อผิดพลาดนี้จะเกิดขึ้นเมื่อสภาพแวดล้อม Dataverse ถูกรีเซ็ตอย่างไม่ถูกต้องในเวลาเดียวกับที่คุณพยายามที่จะสร้างข้อมูลในแอป Finance and Operations

เพื่อแก้ไขปัญหา ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้ใน เครื่องเสมือน Finance and Operations (VM) เปิด SQL Server Management STUDIO (SSMS) และค้นหาแถวในตาราง DUALWRITEPROJECTCONFIGURATIONENTITY ที่ซึ่ง **Internalentityname** เท่ากับ **ลูกค้า V3** และ **externalentityname** เท่ากับ **บัญชี** นี่คือลักษณะของแบบสอบถาม

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. ใช้ชื่อโครงการจากผลลัพธ์ของการสอบถามก่อนหน้านี้ เพื่อรันการสอบถามต่อไปนี้

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. ตรวจสอบให้แน่ใจว่าคอลัมน์ **externalenvironmentURL** มี Dataverse หรือ URL ของแอปที่ถูกต้อง ลบแถวที่ซ้ำกันใดๆ ที่ชี้ไปที่ URL Dataverse ที่ไม่ถูกต้อง ลบแถวที่สอดคล้องกันในตาราง DUALWRITEPROJECTFIELDCONFIGURATION และ DUALWRITEPROJECTCONFIGURATION
4. หยุดการแม็ปตาราง แล้วเริ่มการทำงานใหม่


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]