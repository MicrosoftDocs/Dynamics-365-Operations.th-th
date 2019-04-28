---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent (27 กุมภาพันธ์ 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d8e6a02b43ad60e3a0c4382f98cb808066587da7
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/12/2019
ms.locfileid: "949908"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-27-2019"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent (27 กุมภาพันธ์ 2019)

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent

## <a name="changes-in-attract"></a>การเปลี่ยนแปลงใน Attract

รุ่นนี้มีการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract

## <a name="changes-in-onboard"></a>การเปลี่ยนแปลงในการเตรียมความพร้อม

รุ่นนี้มีการแก้ไขบักรองสำหรับ Dynamics 365 Talent: การเตรียมความพร้อม

## <a name="changes-in-core-hr"></a>การเปลี่ยนแปลงใน Core HR

การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2163

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>เพิ่มรายการเมนูฟิลด์แบบกำหนดเองไปยังการดูแลระบบ

การนำทางไปยังเมนู **ฟิลด์แบบกำหนดเอง** ได้ถูกเพิ่มไปยังพื้นที่ทำงาน **การดูแลระบบ**

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>ซ่อนการนำเข้า และสร้างตัวเลือกสำหรับแอพลิเคชันบนมือถือใหม่

ในปัจจุบัน ไม่สามารถสร้างแอพบนมือถือใหม่ใน Talent ได้ ตัวเลือกในการสร้างประสบการณ์บนมือถือใหม่ได้ถูกลบออกจากเมนู **แอปบนมือถือ**

### <a name="variable-compensation-award-dmf-entity"></a>รางวัลค่าตอบแทนผันแปร (เอนทิตีDMF)

ในรุ่นนี้ เอนทิตีกรอบงานการจัดการข้อมูล (DMF) ของ **รางวัลค่าตอบแทนผันแปร** จะพร้อมใช้งานสำหรับการส่งออกในขณะนี้

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>ที่อยู่ในสหราชอาณาจักรปรากฏในหน้าการวิเคราะห์การจัดการบุคลากรเป็นที่อยู่ของสวิส

ในรุ่นนี้ ที่อยู่จะแสดงตามเมือง รุ่นนี้แก้ไขปัญหาที่ซึ่งการแสดงภาพแสดงสถานที่ของพนักงานผิด

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>รายงาน Power BI ของพนักงานแสดงข้อผิดพลาด เมื่อวันที่อายุงานของพนักงานคือวันอธิกสุรทิน

มีการดำเนินการแก้ไขใน Microsoft Power BI ไปยังบัญชีสำหรับวันที่อายุงานที่เป็นวันที่ 29 กุมภาพันธ์

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>ค่าตอบแทนคงที่ของพนักงาน รางวัลผันแปรของพนักงาน แผนผันแปรของพนักงาน (การลงทะเบียน) อนุญาตสำหรับฟิลด์ที่กำหนดเอง

ขณะนี้ ฟิลด์ที่กำหนดเองสามารถถูกเพิ่มได้สำหรับค่าตอบแทนคงที่ของพนักงาน รางวัลผันแปรของพนักงาน แผนผันแปรของพนักงาน (การลงทะเบียน) ขณะนี้คุณสามารถติดตามข้อมูลเพิ่มเติมเกี่ยวกับแผนค่าตอบแทนคงที่และผันแปรของพนักงานได้ นอกเหนือจากข้อมูลที่พร้อมใช้งานตามค่าเริ่มต้น ฟิลด์ที่กำหนดเองสามารถถูกป้อนและถูกปรับปรุงได้ ผ่านส่วนติดต่อผู้ใช้ หรือผ่านเอนทิตีที่กำหนดไว้

### <a name="other-miscellaneous-bug-fixes"></a>การแก้ไขปัญหาบักเบ็ดเตล็ดอื่นๆ

รุ่นนี้มีการแก้ไขบักรองอื่นๆ

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="advanced-compensation-security-fixed-and-variable"></a>ความปลอดภัยของค่าตอบแทนขั้นสูง (คงที่และผันแปร)

ในองค์กรหลายองค์กร ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการอาจมีการเข้าถึงเรกคอร์ดค่าตอบแทนที่เฉพาะเจาะจงเท่านั้น เรกคอร์ดเหล่านี้อาจมีไว้สำหรับผู้บริหารหรือพนักงานในภูมิภาค การเปลี่ยนแปลงนี้จะทำให้ฝ่ายทรัพยากรบุคคล (HR) สามารถจัดการและรักษาแผนค่าตอบแทนสำหรับกลุ่มพนักงานอื่นๆ ในองค์กรได้ Security role ที่ถูกกำหนดให้กับแผนคงที่และผันแปร จะกำหนดการเข้าถึงแผนและข้อมูลพนักงานเหล่านั้นที่เกี่ยวข้องกับพวกเขา เช่น (ตัวอย่างเช่น เรกคอร์ดเงินโบนัส หรือข้อมูลเงินเดือน) เฉพาะบทบาทที่มีการเข้าถึงที่ระบุ จะสามารถดำเนินการค่าตอบแทนสำหรับพนักงานเหล่านั้นได้

### <a name="platform-update-24"></a>แพลตฟอร์ม update 24

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Microsoft Dynamics 365 for Finance and Operations การปรับปรุงแพลตฟอร์ม 24 (มีนาคม 2019) ดู [คุณลักษณะการแสดงตัวอย่างใน Finance and Operations การปรับปรุงแพลตฟอร์ม 24 (มีนาคม 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24)

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>ทำให้ค่าตอบแทนคงที่ของพนักงานพร้อมใช้งานสำหรับการมอบหมายตำแหน่งในอนาคต

เป็นเรื่องปกติที่พนักงานที่จะเข้าร่วมกับองค์กรมีวันที่เริ่มต้นในอนาคต การเปลี่ยนแปลงนี้จะทำให้มีการกำหนดค่าตอบแทนคงที่สำหรับพนักงานที่มีการมอบหมายตำแหน่งงานในอนาคต

## <a name="known-issues"></a>ปัญหาที่ทราบ

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-to-finance-and-operations"></a>การเปลี่ยนแปลงไปยังเท็มเพลตการรวม Core HR (Talent Common Data Service ไปยัง Finance and Operations)
เท็มเพลตสำหรับ Core HR ได้มีการอัพเดตเป็น "เท็มเพลตการสอบถามขั้นสูง" ดังนั้น ตามค่าเริ่มต้น การสอบถามขั้นสูงจะพร้อมใช้งานสำหรับโครงการที่สร้างขึ้นโดยใช้เท็มเพลตนี้ นอกจากนี้ ฟังก์ชันการแม็ปเริ่มต้นใดๆ จะมองเห็นได้เฉพาะในโปรแกรมแก้ไขการสอบถามขั้นสูง (ฟังก์ชันการแม็ปค่าเริ่มต้นปรากฏเป็น "FN" ในการแม็ป)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับข้อผิดพลาดในการแม็ป ดู [มีอะไรใหม่ หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (14 ธันวาคม 2018)](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14)

ในการใช้เท็มเพลตใหม่ สร้างโครงการใหม่ และเลือกเท็มเพลตการรวม Talent ใหม่

ในการปรับปรุงเท็มเพลตที่มีอยู่ของคุณ ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ปรับปรุงการแม็ปต่อไปนี้:

    - **ตำแหน่งงานไปยังตำแหน่ง:** ลบการแม็ปนี้
    - **การกำหนดงานหลักของตำแหน่งงานไปยังตำแหน่ง:** ลบการแม็ปนี้
    - **ตำแหน่งงานไปยังตำแหน่งฐาน:** เพิ่มการแม็ปใหม่จากเอนทิตี **ตำแหน่งงาน** Common Data Service ไปยังเอนทิตี Finance and Operations **ตำแหน่งฐาน** ย้ายไปที่ตำแหน่ง 7 ในลำดับ

        [![การแม็ปตำแหน่งงานไปยังตำแหน่งฐาน](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **รายละเอียดตำแหน่งงานไปยังตำแหน่ง:** เพิ่มการแม็ปใหม่จากเอนทิตี **ตำแหน่งงาน** Common Data Service ไปยังเอนทิตี Finance and Operations **รายละเอียดตำแหน่ง** ย้ายไปที่ตำแหน่ง 8 ในลำดับ

        [![การแม็ปรายละเอียดตำแหน่งงานไปยังตำแหน่ง](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **ระยะเวลาตำแหน่งงานไปยังตำแหน่ง:** เพิ่มการแม็ปใหม่จากเอนทิตี **ตำแหน่งงาน** Common Data Service ไปยังเอนทิตี Finance and Operations **ระยะเวลาตำแหน่ง**

        [![การแม็ประยะเวลาตำแหน่งงานไปยังตำแหน่ง](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **ลำดับชั้นตำแหน่งงานไปยังตำแหน่ง:** เพิ่มการแม็ปใหม่จากเอนทิตี **ตำแหน่งงาน** Common Data Service ไปยังเอนทิตี Finance and Operations **ลำดับชั้นตำแหน่ง** เลือก **การสอบถามขั้นสูง** เพื่อทำการสอบถามขั้นสูงของคุณให้พร้อมใช้งานสำหรับโครงการของคุณ

       [![ปุ่มการสอบถามขั้นสูง](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. เพิ่มการแม็ปต่อไปนี้
    
    [![การแม็ป](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom VALIDFROM cdm_validto cdm_validto = = VALIDTO
       
    2. เลือกการเชื่อมโยง **การสอบถามและการกรองขั้นสูง** ถัดจากฟิลด์ **การค้นหา**  

    3. ค้นหาคอลัมน์ **cdm_parentjobpositionid.cdm_jobpositionnumber** และเลือกปุ่มลูกศรลงทางด้านขวา

    4. ในกล่องโต้ตอบที่ปรากฏ เลือก **ลบรายการที่ว่าง**

    5. เลือก **เพิ่มคอลัมน์ \> เพิ่มคอลัมน์แบบมีเงื่อนไข** เพื่อเพิ่มการแปลงค่าเริ่มต้นสำหรับ HIERARCHYTYPENAME

        [![เพิ่มคำสั่งคอลัมน์แบบมีเงื่อนไข](./media/Add-column.png)](./media/Add-column.png)

    6. ในกล่องโต้ตอบ **เพิ่มคอลัมน์แบบมีเงื่อนไข** ป้อน **HIERARCHYTYPENAME** เป็นชื่อของคอลัมน์ใหม่
    7. ในส่วนของเงื่อนไข **ถ้า** เลือกฟิลด์ใดๆ ใช้ **เท่ากับ** เป็นความสัมพันธ์ และป้อนค่าใดๆ ในส่วนของเงื่อนไข ***แล้ว** และ **มิฉะนั้น** ระบุค่าเริ่มต้นที่ควรจะเป็น ในกรณีนี้ ป้อน **รายการ** ในทั้งสองส่วน

        [![เพิ่มกล่องโต้ตอบคอลัมน์แบบมีเงื่อนไข](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **การสอบถามและการกรองขั้นสูง**
    9. ในหน้า **งานการแม็ป** เลือกคอลัมน์ใหม่เป็นแหล่งที่มาในการสร้างการแม็ปอื่นสำหรับ HIERARCHYTYPENAME

        [![การแม็ป](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)
