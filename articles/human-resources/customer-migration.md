---
title: FAQ การย้ายลูกค้าทรัพยากรบุคคล
description: บทความนี้ตอบคําถามที่ถามบ่อยเกี่ยวกับการย้ายของ Microsoft Dynamics 365 Human Resources ไปยังโครงสร้างพื้นฐานกับแอปการเงินและการดำเนินงาน
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e11d26ebe084762a8616c8aa0aa041a87306473
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734370"
---
# <a name="human-resources-customer-migration"></a>การย้ายลูกค้าทรัพยากรบุคคล

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>ลูกค้าควร Dynamics 365 Human Resources วางแผนที่จะย้ายไปยังโครงสร้างพื้นฐานของการเงินและการดําเนินงานอย่างไร

ลูกค้า Microsoft Dynamics 365 Human Resources สองประเภทจะได้รับผลกระทบ และต้องดําเนินการเปลี่ยนแปลงเพื่อให้แน่ใจว่าลูกค้าเหล่านั้นอยู่ในโครงสร้างพื้นฐานของการเงินและการดําเนินงานล่าสุด ดังนี้

- ลูกค้าที่ใช้ Dynamics 365 Human Resources และไม่มีแอปการดําเนินงานอื่นๆ จาก Dynamics 365
- ลูกค้าที่ใช้ทั้ง Dynamics 365 Human Resources และ Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce หรือ Dynamics 365 Project Operations

ไม่ว่าจะอยู่ในประเภทใด ลูกค้าจะต้องย้ายข้อมูลไปไว้ในสภาพแวดล้อมที่สร้างขึ้นใหม่บนโครงสร้างพื้นฐานของการเงินและการดําเนินงาน และตรวจสอบความถูกต้องว่าการผสานรวมเสร็จสมบูรณ์แล้ว

ไปข้างหน้า แอปจะมี Dynamics 365 Human Resources สภาพแวดล้อมด้านการเงินและการดําเนินงานของตนเองที่แยกต่างหากจากแอปการดําเนินงานอื่นๆ ด้วยวิธีนี้ ลูกค้าจะสามารถใช้ประโยชน์จากตัวเลือกความสามารถในการขยายได้โดยไม่ต้องผสานข้อมูลปัจจุบัน Microsoft จะจัดเตรียมเครื่องมือและสภาพแวดล้อมภายในที่ลูกค้าสามารถใช้ทดสอบและตรวจสอบความถูกต้องของการย้ายข้อมูลก่อนที่จะย้ายไปยังสภาพแวดล้อมการทำงานจริง เครื่องมือนี้จะเปิดใช้งานกระบวนการอัตโนมัติที่ใกล้ที่สุดและจะพร้อมใช้งานระหว่างสิงหาคมถึงพฤศจิกายน 2022

ลูกค้าที่ใช้งานแอปอื่นๆ ในโครงสร้างพื้นฐานของการเงินและการดําเนินงานจะมีตัวเลือกในการผสานข้อมูลทรัพยากรบุคคลกับสภาพแวดล้อมที่มีอยู่ 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>ลูกค้าจะถูกย้ายไปยังโครงสร้างพื้นฐานของการเงินและการดําเนินงานเมื่อใด

การเปลี่ยนของแต่ละบริษัทจะขึ้นอยู่กับการตั้งค่าคอนฟิกและความพร้อมในปัจจุบันที่จะย้ายไปยังโครงสร้างพื้นฐานการเงินและการดำเนินงาน ขอแนะนำว่าลูกค้าจะร่วมมือกับคู่ค้า Microsoft เพื่อพิจารณาพาธที่ดีที่สุดไปข้างหน้า

- องค์กรที่ใช้โมดูล **ทรัพยากรบุคคล** ใน Dynamics 365 Finance จะสามารถเปิดใช้งานความสามารถใหม่จาก Dynamics 365 Human Resources โดยเป็นส่วนหนึ่งของกระบวนการอัปเดตเวอร์ชันเดียวปกติได้ โดยทั่วไป คุณลักษณะใหม่จะถูกวางแผนไว้ว่าจะพร้อมใช้งานโดยเริ่มต้นในมกราคม 2022
- องค์กรที่ใช้ Dynamics 365 Human Resources จะมีสิทธิ์เข้าถึงเครื่องมือที่พวกเขาสามารถใช้ในการรวมโครงสร้างพื้นฐานให้เสร็จสมบูรณ์ Microsoft จะร่วมกับลูกค้าเกี่ยวกับการเปลี่ยน ซึ่งจะช่วยป้องกันการหยุดชะงักใดๆ ในการบริการ ลูกค้าจะมีเวลา 12 เดือนเพื่อทำการเปลี่ยน เริ่มต้นจากเวลาที่เครื่องมือการย้ายพร้อมใช้งาน
- องค์กรที่ใช้ทั้งโมดูล Dynamics 365 Human Resources และโมดูล **ทรัพยากรบุคคล** สามารถย้ายโครงสร้างพื้นฐานของทรัพยากรบุคคลแบบสแตนด์อโลนไปยังโครงสร้างพื้นฐานของการเงินและการดําเนินงาน อีกตัวเลือกหนึ่งคือใช้เครื่องมือผสานเพื่อดึงสภาพแวดล้อมให้เป็นสภาพแวดล้อมเดียว ไม่มีความต้องการหรือกรอบเวลาการผสานสภาพแวดล้อมสองสภาพแวดล้อม

สำหรับข้อมูลล่าสุด ให้ดูที่ [แผนการออกใช้](/dynamics365/release-plans/)

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>ลูกค้ายังคงต้องการการรวมที่กำหนดเองระหว่าง Dynamics 365 Human Resources และโมดูลทรัพยากรบุคคลหรือไม่

- ลูกค้าที่มีสภาพแวดล้อมของ Dynamics 365 Human Resources และโครงสร้างพื้นฐานของการเงินและการดําเนินงานอื่นซึ่งรวมในปัจจุบันจะต้องดําเนินการรวมสภาพแวดล้อมทั้งสองเข้าด้วยกันต่อไปหลังจากการผสานรวม
- ลูกค้าที่เลือกที่จะรักษาสภาพแวดล้อม Dynamics 365 Human Resources ของตนให้แยกต่างหากจากสภาพแวดล้อมแอปการเงินและการดําเนินงานที่มีอยู่ของสภาพแวดล้อมจะต้องดําเนินการรวมสภาพแวดล้อมเข้าด้วยกันเพื่อให้ข้อมูลพร้อมใช้งานในสภาพแวดล้อมทั้งสอง
- ลูกค้าสามารถใช้ตัวรวมข้อมูลเพื่อคัดลอกข้อมูลระหว่างสภาพแวดล้อมทั้งสองได้อย่างต่อเนื่อง ลูกค้าที่ผสานข้อมูลในสภาพแวดล้อมเดียวหลังจากการย้ายจะไม่ต้องรวมข้อมูลอีกต่อไป เนื่องจากข้อมูลทั้งหมดจะอยู่ในฐานข้อมูลเดียว

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>โซลูชัน ISV ลูกค้าจะถูกย้ายโดยอัตโนมัติหรือไม่

ประสบการณ์การย้ายสำหรับแต่ละโซลูชันผู้ขายซอฟต์แวร์อิสระ (ISV) จะแตกต่างกันไป ทั้งนี้ขึ้นอยู่กับวิธีการรวมของโซลูชัน Microsoft จะร่วมกับ ISVs อย่างต่อเนื่องเพื่อให้แน่ใจว่าการเปลี่ยนไปยังโครงสร้างพื้นฐานการเงินและการดำเนินงานจะเป็นไปอย่างต่อเนื่อง โซลูชัน ISV หลายโซลูชันถูกสร้างขึ้นบน Dataverse โดยใช้ความสามารถ Microsoft Power Platform โซลูชันเหล่านี้จะขึ้นอยู่กับการรวม Dataverse ระหว่างสภาพแวดล้อม Dynamics 365 Human Resources และสภาพแวดล้อม Dataverse การรวม Dataverse ไม่ได้รับการสนับสนุนเป็นส่วนหนึ่งของการผสานโครงสร้างพื้นฐาน ในโครงสร้างพื้นฐานของการเงินและการดําเนินงาน มีการวางแผนแผนผังการรวมแบบสองทิศทางใหม่เพื่อแทนที่ฟังก์ชันของการรวม Dataverse

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>ตัวรวมข้อมูลที่จะย้ายข้อมูลระหว่างแอป Dynamics 365 Human Resources และแอป Dynamics 365 อื่นๆ จะได้รับผลกระทบอย่างไร

หลังจากที่ลูกค้าย้ายไปยังโครงสร้างพื้นฐานของการเงินและการดําเนินงานแล้ว ลูกค้าจะต้องดําเนินการรวมข้อมูลระหว่างสองสภาพแวดล้อมต่อไป ลูกค้าสามารถใช้ตัวรวมข้อมูลเพื่อปฏิบัติงานการย้ายข้อมูลเหล่านี้ต่อไปได้ ลูกค้าที่วางแผนที่จะรักษาสภาพแวดล้อม Dynamics 365 Human Resources ของตนให้แยกต่างหากจากสภาพแวดล้อมแอปนการเงินและการดําเนินงานที่มีอยู่ของสภาพแวดล้อมจะต้องดําเนินการรวมข้อมูลในสภาพแวดล้อมทั้งสอง แก่ลูกค้าที่รวมสภาพแวดล้อมสองสภาพแวดล้อมไว้ในสภาพแวดล้อมเดียว ระบบจะไม่ต้องใช้การรวมระหว่างสองสภาพแวดล้อมอีกต่อไป

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>ข้อมูลจะถูกย้ายระหว่าง Dynamics 365 Human Resources บนโครงสร้างพื้นฐานการเงินและการดำเนินงานและ Dataverse หลังการย้ายหรือไม่

การรวมปัจจุบัน Dataverse ระหว่าง Dynamics 365 Human Resources และ Dataverse ไม่ได้รับการสนับสนุนเป็นส่วนหนึ่งของโครงสร้างพื้นฐานของการเงินและการดําเนินงาน มีแผนที่จะแนะทางแผนผังการรวมแบบสองทิศทางเพื่อแม็ปเอนทิตีการเงินและการดําเนินงานกับตาราง Dataverse ลูกค้าต้องตัดสินใจว่าแผนผังการรวมแบบสองทิศทางใดที่ต้องใช้ในการใช้งาน เราขอแนะนำว่าตารางเสมือนจะใช้ในการรวมและโซลูชัน ISV เว้นแต่จะมีความเป็นต้องใช้ธุรกิจที่เฉพาะเจาะจงเพื่อให้มีการข้อมูลของข้อมูลที่จะคัดลอกใน Dataverse เพื่อรันตรรกะทางธุรกิจ

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>การย้ายจะส่งผลกระทบต่อส่วนขยาย Dataverse สำหรับ Dynamics 365 Human Resources อย่างไร

ลูกค้าจะต้องย้ายไปยังสภาพแวดล้อม sandbox ก่อนที่จะย้ายสภาพแวดล้อมการทำงานจริง เมื่อลูกค้าย้ายสภาพแวดล้อม sandbox ของพวกเขา คุณจะต้องสร้างสําเนาของสภาพแวดล้อม Dataverse เพื่อเชื่อมต่อกับสภาพแวดล้อมการเงินและการดําเนินงานใหม่ที่มีการย้าย ขอแนะนำว่าลูกค้าควรคัดลอกทั้งข้อมูลและโซลูชันสําเนาในสภาพแวดล้อม เพื่อให้ตรงกับสภาพแวดล้อมการทำงานจริงปัจจุบันของลูกค้า

เมื่อลูกค้าพร้อมที่จะย้ายสภาพแวดล้อม Dynamics 365 Human Resources การทำงานจริง Microsoft จะย้ายฐานข้อมูลและที่จัดเก็บ Azure Blob โดยอัตโนมัติ ฐานข้อมูลและที่จัดเก็บที่ย้ายจะชี้งสภาพแวดล้อมใหม่บนโครงสร้างพื้นฐานการเงินและการดำเนินงานไปยัสภาพแวดล้อม Dataverse การทำงานจริงเดียวกัน ก่อนที่จะสามารถคัดลอกข้อมูลไปยังลูกค้าต่อไปยัง Dataverse ได้ ลูกค้าจะต้องเปิดใช้งานแผนผังการรวมแบบสองทิศทางใดๆ ที่ต้องใช้ในการรวม ส่วนขยาย และโซลูชัน ISV ที่สร้างขึ้นบน Dataverse นั้น

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>ส่วนประกอบ Microsoft Power Platform ที่สร้างสำหรับ Dynamics 365 Human Resources จะทำงานโดยอัตโนมัติหลังจากเสร็จสิ้นการย้ายโครงสร้างพื้นฐานหรือไม่

แอปที่สร้างไว้ใน Power Apps โฟลว์ที่สร้างขึ้นใน Power Automate และการเลือกเองของ Microsoft Power Platform อื่นๆ เป็นส่วนขยาย Dataverse ในระหว่างการย้ายสภาพแวดล้อมการทำงานจริงของลูกค้า ไม่มีผลกระทบต่อสภาพแวดล้อม Dataverse รวมถึงส่วนขยายใดๆ แอป โฟลว์ และการเลือกกําหนด Power Microsoft Platform อื่นๆ ควรยังคงใช้งานต่อไปโดยไม่ต้องการการตั้งค่าคอนฟิกเพิ่มเติม

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>จะเกิดอะไรกับเอนทิตีตารางเสมือน Dataverse สำหรับ Dynamics 365 Human Resources ระหว่างการย้าย

เมื่อลูกค้าย้ายสภาพแวดล้อม Dynamics 365 Human Resources ไปยังโครงสร้างพื้นฐานของการเงินและการดําเนินงาน สภาพแวดล้อม Dataverse จะยังคงเชื่อมต่อกับสภาพแวดล้อมที่เชื่อมต่ออยู่ในขณะนี้กับ Dynamics 365 Human Resources ตารางเสมือน Dataverse ที่สร้างในสภาพแวดล้อมจะยังคงงานต่อไปโดยไม่ต้องการการตั้งค่าคอนฟิกเพิ่มเติมใดๆ ตารางเสมือนอาจต้องมีการสร้างใหม่ในสภาพแวดล้อม Dataverse ที่เชื่อมต่อกับสภาพแวดล้อมทางการเงินและการดําเนินงานที่มีอยู่ของลูกค้า

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>การรวมที่ใช้ API ระบบติดตามผู้สมัคร (ATS) API, Payroll API, ตารางเสมือนของ Dataverse สำหรับ Dynamics 365 Human Resources หรือเอนทิตีอื่นๆ ใน Web API ของ Dataverse ทำงานหลังจากการผสานโครงสร้างพื้นฐานเสร็จสมบูรณ์อย่างไร

เมื่อลูกค้าย้ายสภาพแวดล้อม Dynamics 365 Human Resources ไปยังโครงสร้างพื้นฐานของการเงินและการดําเนินงาน สภาพแวดล้อม Dataverse จะยังคงเชื่อมต่อกับสภาพแวดล้อมที่เชื่อมต่ออยู่ในขณะนี้กับ Dynamics 365 Human Resources การรวมใดๆ ที่พัฒนาโดยเทียบกับ Web API ของ Dataverse จะยังคงใช้ต่อไปหลังจากการย้ายเสร็จสมบูรณ์

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>องค์กรของเรามีการตั้งค่าคอนฟิกความปลอดภัยที่กําหนดเองใน Dynamics 365 Human Resources ความปลอดภัยที่กำหนดเองของเราจะยังคงใช้หลังจากการย้ายโครงสร้างพื้นฐานเสร็จสมบูรณ์หรือไม่

ใช่ การตั้งค่าคอนฟิกความปลอดภัยที่กําหนดเองจะรวมอยู่ในการย้ายข้อมูล

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>เวิร์กโฟลว์ใน Dynamics 365 Human Resources จะถูกย้ายโดยอัตโนมัติหรือไม่

ใช่ จะมีการย้ายการตั้งค่าคอนฟิกเวิร์กโฟลว์ ประวัติเวิร์กโฟลว์ และเวิร์กโฟลว์ที่อยู่ดำเนินการในปัจจุบันไปโครงสร้างพื้นฐานที่รวม

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>มุมมองที่บันทึกไว้นี้ใน Dynamics 365 Human Resources จะถูกย้ายโดยอัตโนมัติหรือไม่

ใช่ มุมมองที่บันทึกไว้จะถูกย้ายไปยังโครงสร้างพื้นฐานที่รวม

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>คุณลักษณะที่เปิดใช้งานจะสามารถใช้งานใน Dynamics 365 Human Resources โดยอัตโนมัติหลังจากการผสานโครงสร้างพื้นฐานหรือไม่

- สำหรับลูกค้าที่ใช้โมดูล **ทรัพยากรบุคคล** คุณลักษณะที่พร้อมใช้งานใน Dynamics 365 Human Resources จะจัดการผ่านทางคุณลักษณะการจัดการเท่านั้น โดยปกติแล้ว คุณลักษณะเหล่านี้จะไม่เปิดใช้งานโดยค่าเริ่มต้น คุณลักษณะใดๆ ที่ต้องเปิดใช้งานตามค่าเริ่มต้นจะถูกบันทึก
- สำหรับลูกค้าที่ใช้ Dynamics 365 Human Resources คุณลักษณะจะพร้อมใช้งานในโครงสร้างพื้นฐาน คุณลักษณะใดๆ ที่ไม่พร้อมใช้งานจะถูกบันทึก คีย์การจัดการคุณลักษณะทุกคีย์ที่เปิดใช้งานในสภาพแวดล้อม Dynamics 365 Human Resources ปัจจุบันจะเปิดใช้งานในโครงสร้างพื้นฐานที่ผสาน สำหรับข้อมูลเพิ่มเติม ดูที่ [ภาพรวมการจัดการคุณลักษณะ](/fin-ops/get-started/feature-management-overview.md)

## <a name="what-happens-to-byod-databases-during-the-migration"></a>เกิดอะไรขึ้นกับฐานข้อมูล BYOD ระหว่างการย้าย

นําเข้าและส่งออกการตั้งค่าคอนฟิกเพื่อนําเข้าฐานข้อมูลของคุณเอง (BYOD) จะถูกย้ายไปยังโครงสร้างพื้นฐานการเงินและการดำเนินงาน

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>มีผลกระทบกับภูมิภาค Azure เมื่อย้ายสภาพแวดล้อมของลูกค้าหรือไม่

สภาพแวดล้อม Dynamics 365 Human Resources จะอยู่ในภูมิภาค Azure เดียวกันของการย้าย หากมีความต้องการที่จะย้ายสภาพแวดล้อมไปยังภูมิภาคอื่นของ Azure ลูกค้าจะต้องปฏิบัติตามขั้นตอนมาตรฐานเพื่อย้ายไปยังภูมิภาคใหม่หลังจากการย้ายข้อมูลเสร็จสมบูรณ์

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>เกิดอะไรขึ้นกับที่จัดเก็บข้อมูลดิบ Azure ของฉันระหว่างการย้าย

การส่งออกใดๆ ที่ตั้งค่าคอนฟิกในปัจจุบันสำหรับที่จัดเก็บข้อมูลดิบ Azure ในแอปการเงินและการดำเนินงานจะรักษาการตั้งค่าคอนฟิกเดียวกันไว้หลังจากการย้ายข้อมูล

> [!NOTE]
> แผนผังการรวมแบบสองทิศทางต้องเปิดใช้งานเพื่อเขียนข้อมูลจากสภาพแวดล้อมทรัพยากรบุคคลต่อไปใน Dataverse

ลูกค้าที่ต้องการส่งออกข้อมูลทรัพยากรบุคคลไปยังที่จัดเก็บข้อมูลดิบสามารถเปิดใช้งานคุณลักษณะนี้ได้หลังจากที่การย้ายไปยังโครงสร้างพื้นฐานของการเงินและการดําเนินงานเสร็จสมบูรณ์ สำหรับข้อมูลเพิ่มเติม ดูที่ [ที่จัดเก็บข้อมูลดิบ - ศูนย์สถาปัตยกรรม Azure](/azure/architecture/data-guide/scenarios/data-lake)

ลูกค้าสามารถเชื่อมโยงสภาพแวดล้อมทางการเงินและการดําเนินงานต่างๆ กับที่จัดเก็บข้อมูลดิบเดียวกันได้ อย่างไรก็ตาม แต่ละสภาพแวดล้อมจะชี้ไปที่โฟลเดอร์และคอนเทนเนอร์อื่น ลูกค้าที่วางแผนที่จะรวมสภาพแวดล้อมในภายหลังควรวางแผนแนวทางของตนอย่างรอบคอบ
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>ต้องย้ายข้อมูลใดถ้าลูกค้าใช้โมดูลทรัพยากรบุคคลอยู่ในขณะนี้

ลูกค้าที่ใช้โมดูล **ทรัพยากรบุคคล** จะมีฟังก์ชันคุณลักษณะใหม่จาก Dynamics 365 Human Resources ที่ใช้กับสภาพแวดล้อมโดยผ่านกระบวนการอัปเดตรุ่นหนึ่ง ลูกค้าสามารถคาดว่าจะเห็นฟังก์ชันใหม่ในสภาพแวดล้อมของพวกเขา เมื่อฟังก์ชันนั้นพร้อมใช้งานในแต่ละการอัปเดต ลูกค้าสามารถใช้การจัดการคุณลักษณะเพื่อเปิดใช้งานคุณลักษณะ ลูกค้าควรวางแผนที่จะตรวจสอบความถูกต้องของลักษณะการลองใหม่เหล่านี้โดยใช้กระบวนการที่ได้ใช้งานแล้วและใช้เพื่อตรวจสอบความถูกต้องของการอัปเดตอื่นๆ ในสภาพแวดล้อมเหล่านั้น

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>เกิดอะไรขึ้นกับการรวมแบบกำหนดเองกับระบบภายนอก

ลูกค้าจะต้องย้ายการรวมไปยังสภาพแวดล้อมการเงินและการดําเนินงาน เนื่องจากจุดสิ้นสุดของสภาพแวดล้อมนี้แตกต่างกัน ลูกค้าจึงอาจต้องอัปเดตหรือเปลี่ยนการรวมเพื่อให้ชี้ไปยังสภาพแวดล้อมใหม่ งานนี้จะเป็นกระบวนการที่ด้วยตนเองเป็นหลัก และการเปลี่ยนแปลงที่ต้องใช้จะขึ้นอยู่กับสถาปัตยกรรมของการรวม ลูกค้าควรร่วมมือกับคู่ค้าของ Microsoft เพื่อพิจารณาแนวทางที่ดีที่สุดในการเคลื่อนย้ายการรวม

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>เกิดอะไรขึ้นกับส่วนขยาย Microsoft Power Platform (Dataverse) ถ้าลูกค้ารวมสภาพแวดล้อม Dynamics 365 Human Resources ที่มีสภาพแวดล้อมการเงินและการดําเนินงานที่มีอยู่

หากลูกค้าตัดสินใจที่จะผสานสภาพแวดล้อม Dynamics 365 Human Resources และสภาพแวดล้อมด้านการเงินและการดําเนินงานที่มีอยู่ให้เป็นอินสแตนซ์ Dataverse เดียวหลังการย้าย สภาพแวดล้อม Dataverse ของลูกค้าจะต้องถูกรวมเป็นส่วนหนึ่งของกระบวนการผสาน งานนี้จะต้องปรับใช้แอปใดๆ ที่สร้างโดยใช้ Power Apps และการกำหนดอื่นอีกครั้งในสภาพแวดล้อมใหม่

## <a name="what-will-happen-to-documents-during-the-migration"></a>จะเกิดอะไรกับเอกสารระหว่างการย้าย

เมื่อลูกค้าย้ายสภาพแวดล้อม Dynamics 365 Human Resources ไปยังโครงสร้างพื้นฐานของการเงินและการดําเนินงาน เอกสารจะยังคงอยู่ในที่จัดเก็บเอกสารที่มีอยู่ และจะได้รับการแม็ปกับสภาพแวดล้อมใหม่ในโครงสร้างพื้นฐานของการเงินและการดําเนินงานโดยอัตโนมัติ

ในการนำออกใช้ในอนาคต จะมีจัดเตรียมเอนทิตีข้อมูลใหม่ให้ หลังจากที่มีการเปลี่ยนแปลงดังกล่าว ลูกค้าที่เลือกที่จะผสานสภาพแวดล้อม Dynamics 365 Human Resources ของตนกับสภาพแวดล้อมด้านการเงินและการดําเนินงานที่มีอยู่จะสามารถส่งออกเอกสารและย้ายเอกสารไปไว้ในสภาพแวดล้อมที่มีอยู่ได้

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>หลังจากการย้าย เกิดอะไรขึ้นกับชุดงานที่เราได้ตั้งค่าคอนฟิกใน Dynamics 365 Human Resources

ชุดงานจะต้องได้รับการตั้งค่าคอนฟิกใหม่ในสภาพแวดล้อมการเงินและการดําเนินงาน ลูกค้าต้องประเมินชุดงานแต่ละชุดและเปรียบเทียบกับรายการชุดงานปัจจุบันในสภาพแวดล้อมทางการเงินและการดําเนินงาน ลูกค้าควรวิเคราะห์การจัดตารางการผลิตชุดงานโดยรวมด้วยเมื่อรวมชุดงานสองชุด เพื่อตัดสินว่าควรมีการเปลี่ยนแปลงที่จัดตาราง ระดับความสำคัญ หรือกลุ่มชุดงานหรือไม่

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>การย้ายจะส่งผลกระทบต่อโครงการ LCS ของ Dynamics 365 Human Resources อย่างไร

ลูกค้าต้องสร้างโครงการ Microsoft Dynamics Lifecycle Service (LCS) ใหม่ และต้องเลือกแอปการเงินและการดําเนินงานเป็นผลิตภัณฑ์และ **การใช้งาน** เป็นชนิดโครงการ นอกจากนี้ ฟิลด์ใหม่เกี่ยวกับชนิดโครงการย่อยจะพร้อมใช้งานเมื่อสร้างโครงการ LCS ลูกค้าต้องเลือกตัวเลือกสำหรับหารย้าย Dynamics 365 Human Resources เพื่อย้ายโครงการ LCS ของฝ่ายทรัพยากรบุคคลที่มีอยู่ไปยังโครงสร้างพื้นฐานของการเงินและการดําเนินงาน

คุณลักษณะของโครงการ LCS การเงินและการดําเนินงานแตกต่างจากคุณลักษณะของโครงการ LCS ของฝ่ายทรัพยากรบุคคล

หากต้องการใช้งานจริง ลูกค้าใหม่ต้องกรอกข้อมูลงานต่อไปนี้ให้ครบถ้วน:

- เตรียมความพร้อมของโครงการให้เสร็จสมบูรณ์
- ทำระเบียบวิธีให้เสร็จสมบูรณ์
- กรอกตัวประมาณการสมัครใช้งาน
- ทำกระบวนการความพร้อมในการไปใช้งานจริงให้เสร็จสมบูร

## <a name="how-will-the-business-process-modeler-be-migrated"></a>ตัวทำแบบจำลองกระบวนการทางธุรกิจจะย้ายอย่างไร

ลูกค้าจะต้องส่งออกไลบรารีตัวทำแบบจำลองกระบวนการทางธุรกิจจากโครงการ LCS ของทรัพยากรบุคคลและนําเข้าไปยังโครงการ LCS ของการเงินและการดําเนินงาน นอกจากนี้ ลูกค้าต้องอัปเดตการตั้งค่าวิธีใช้ในแอปพลิเคชันเพื่อชี้ไปที่โครงการ LCS ใหม่

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>การย้ายจะมีผลต่อกระบวนการอัปเดตบริการอย่างไร

เมื่อย้ายข้อมูลแล้ว ลูกค้าจะมีความยืดหยุ่นมากขึ้นสำหรับการจัดการอายุการใช้งานแอปพลิเคชัน (ALM) และการอัปเดตบริการ การอัปเดตบริการจะไม่มีผลกับสภาพแวดล้อม Human Resources อีกต่อไปโดยอัตโนมัติ แต่บริการจะเป็นไปตามกระบวนการและฟังก์ชันการอัปเดตบริการรุ่นหนึ่งและฟังก์ชัน และตัวเลือกการตั้งค่าคอนฟิกของการอัปเดตผ่าน LCS จะเปิดใช้งาน

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>ลูกค้าจะได้รับความช่วยเหลือ FastTrack ในการผสานโครงสร้างพื้นฐานหรือไม่

Microsoft ยังคงนิยามเครื่องมือและทรัพยากรที่พร้อมใช้งานจาก FastTrack เพื่อช่วยในการผสาน

## <a name="licensing-impact"></a>ผลกระทบของการให้สิทธิ์การใช้งาน

หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับผลกระทบต่อการให้สิทธิ์การใช้งาน โปรดดูที่ [การผสานโครงสร้างพื้นฐาน Dynamics 365 Human Resources](hr-infrastructure-merge.md#licensing)
