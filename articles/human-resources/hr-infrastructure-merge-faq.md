---
title: คำถามที่ถามบ่อยเกี่ยวกับการผสานโครงสร้างพื้นฐานของ Dynamics 365 Human Resources
description: หัวข้อนี้ตอบคําถามที่ถามบ่อยเกี่ยวกับการผสานโครงสร้างพื้นฐานของ Microsoft Dynamics 365 Human Resources กับแอปการเงินและการดำเนินงาน
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e43aaad2f5b80996eb0fc10f550f073aec67fe5d
ms.sourcegitcommit: 26c726bd0b00935e3d2c31fdc5a3b2ae03a8a2b0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661471"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>คำถามที่ถามบ่อยเกี่ยวกับการผสานโครงสร้างพื้นฐานของ Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



หัวข้อนี้ตอบคําถามที่ถามบ่อยเกี่ยวกับการผสานโครงสร้างพื้นฐานของ Microsoft Dynamics 365 Human Resources กับแอปการเงินและการดำเนินงาน

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>การผสานโครงสร้างพื้นฐาน Dynamics 365 Human Resources คืออะไร

Dynamics 365 Human Resources เป็นแอปพลิเคชันแบบสแตนด์อโลนที่ใช้โครงสร้างพื้นฐานที่แตกต่างจากแอปการเงินและการดำเนินงานอื่นๆ เช่น Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce และ Dynamics 365 Project Operations การผสานโครงสร้างพื้นฐานจะนำ Dynamics 365 Human Resources ไปยังโครงสร้างพื้นฐานเดียวกันกับแอปการเงินและการดำเนินงานอื่นๆ

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>ค่าและประโยชน์ของการผสานโครงสร้างพื้นฐาน

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>องค์กรของฉันใช้ Dynamics 365 Human Resources ในการจัดการดําเนินงานด้าน HR เราจะเห็นประโยชน์อะไรจากการเปลี่ยนแปลงเหล่านี้

- การเปลี่ยนแปลงเหล่านี้ลบความสับสนที่เกิดจากความสามารถด้านทรัพยากรบุคคล (HR) หลายชุดใน Dynamics 365
- และให้ทั้งความสามารถในการเพิ่มฟังก์ชัน Microsoft Power Platform และวิธีเพิ่มตัวเลือกตรรกะและคุณลักษณะทางธุรกิจ
- โดยจะมีความสอดคล้องระหว่างแอป Dynamics 365 Human Resources กับแอปการเงินและการดำเนินงานอื่นๆ ในแง่ของ Application Lifecycle Management (ALM), Microsoft Dynamics Lifecycle Services (LCS), ความพร้อมใช้งานทางภูมิศาสตร์ ความสามารถในการเพิ่มฟังก์ชัน และอื่นๆ
- ซึ่งช่วยให้คุณสามารถใช้ประโยชน์จากบริการและเครื่องมือที่ใช้ร่วมกัน และลดต้นทุนได้

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>องค์กรของฉันใช้โมดูล Human Resources ใน Dynamics 365 Finance, Supply Chain Management, Commerce หรือ Project Operations เราจะเห็นประโยชน์อะไรจากการเปลี่ยนแปลงเหล่านี้

ขณะนี้ ความสามารถและการลงทุนที่ทำใน Dynamics 365 Human Resources จะพร้อมใช้งานกับลูกค้าที่ไม่ได้ใช้โมดูล HR ใน Dynamics 365 Finance ความสามารถบางอย่างเหล่านี้รวมถึงการจัดการการลางานและการขาดงาน การจัดการสวัสดิการ และการจัดการงาน

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>ฉันจะสูญเสียคุณลักษณะหรือความสามารถใดๆ ที่ฉันใช้ขณะนี้หรือไม่

จะมีพาริตี้ตามฟังก์ชันระหว่าง Dynamics 365 Human Resources กับโมดูล HR และในแอปการเงินและการดำเนินงาน Dynamics 365 Human Resources จะมีความสำคัญเหนือกว่าสำหรับคุณลักษณะที่คล้ายคลึงกัน สำหรับข้อมูลเพิ่มเติม ดูที่ [ภาพรวมการจัดการคุณลักษณะ](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="will-the-experience-change-for-my-users"></a>ประสบการณ์จะเปลี่ยนแปลงสำหรับผู้ใช้ของฉันหรือไม่

ความสามารถด้าน HR ใหม่จะมีการจัดการผ่านการจัดการคุณลักษณะ ลูกค้าจะตัดสินใจว่าต้องการใช้หรือไม่ ในบางกรณี อาจมีการแก้ไขความสามารถ ในกรณีดังกล่าว จะมีคู่มือประกอบ

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>การเปลี่ยนแปลงนี้จะมีผลกระทบอย่างไรต่อฉันหากฉันเป็นลูกค้าปัจจุบัน และฉันใช้ทั้งโมดูล HR บนโครงสร้างพื้นฐานของการเงินและการดำเนินงานและ Dynamics 365 Human Resources ผ่านการรวมที่กำหนดเอง

การรวมที่กำหนดเองระหว่าง Dynamics 365 Human Resources และโมดูล HR ใน Dynamics 365 Finance จะไม่จำเป็นอีกต่อไป ข้อมูล HR ทั้งหมดจะอยู่ในฐานข้อมูลเดียวกับแอปการเงินและการดำเนินงานอื่นๆ

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>การย้ายจาก Dynamics 365 Human Resources ไปยังแอปการเงินและการดำเนินงาน

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>องค์กรของฉันใช้ Dynamics 365 Human Resources ในการจัดการดําเนินงานด้าน HR เราต้องวางแผนอะไรเพื่อย้ายไปยังประสบการณ์ใหม่

หากองค์กรของคุณใช้ Dynamics 365 Human Resources แต่ไม่ได้ใช้แอปการเงินและการดำเนินงานอื่น สภาพแวดล้อมทรัพยากรบุคคลของคุณจะถูกย้ายไปยังโครงสร้างพื้นฐานใหม่ กระบวนการย้ายข้อมูลมากจะเป็นแบบอัตโนมัติ กระบวนการจะอยู่เพื่อย้ายฐานข้อมูลของคุณและซิงโครไนส์กับโครงสร้างพื้นฐานใหม่

นอกจากนี้ เครื่องมือจะพร้อมสำหรับให้คุณสามารถทดสอบกระบวนการย้าย และตรวจสอบความถูกต้องของข้อมูลและประสบการณ์ของคุณ ก่อนที่คุณจะย้ายสภาพแวดล้อมการทำงานจริง

หากองค์กรของคุณใช้ทั้งแอป Dynamics 365 Human Resources และแอปการเงินและการดำเนินงานอื่น คุณควรวางแผนเวลาเพิ่มเติมในการตรวจสอบความถูกต้องเพื่อให้แน่ใจว่าข้อมูลของคุณถูกย้ายไปยังสภาพแวดล้อมใหม่อย่างถูกต้อง การย้ายไปยังโครงสร้างพื้นฐานใหม่จะผสานข้อมูลจากสภาพแวดล้อมทรัพยากรบุคคลกับสภาพแวดล้อมการเงินและการดำเนินงานของคุณ ข้อมูลที่มีความขัดแย้งจะต้องใช้ข้อมูลป้อนเข้าของผู้ใช้เพื่อกําหนดว่าควรจะแก้ไขความขัดแย้งอย่างไร ผู้ใช้และผู้ดูแลระบบต้องจัดการการแมปข้อมูลที่มีความขัดแย้งและทดสอบการย้ายในสภาพแวดล้อม Sandbox ก่อนการย้ายสภาพแวดล้อมการทำงานจริง

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>องค์กรของฉันใช้โมดูล Human Resources ใน Dynamics 365 Finance, Supply Chain Management, Commerce หรือ Project Operations เราต้องวางแผนอะไรเพื่อย้ายไปยังประสบการณ์ใหม่

สำหรับองค์กรที่ใช้โมดูล HR ในแอปการเงินและการดำเนินงาน ฟังก์ชันคุณลักษณะใหม่จาก Dynamics 365 Human Resources จะใช้กับสภาพแวดล้อมของคุณโดยผ่านกระบวนการอัปเดตรุ่นหนึ่ง คุณสามารถคาดว่าจะเห็นฟังก์ชันใหม่ในสภาพแวดล้อมของคุณ เมื่อฟังก์ชันนั้นพร้อมใช้งานในแต่ละการอัปเดต คุณสามารถใช้การจัดการคุณลักษณะเพื่อเปิดคุณลักษณะใหม่ได้ อย่างไรก็ตาม คุณควรวางแผนเพื่อตรวจสอบความถูกต้องของคุณลักษณะเหล่านี้ ปฏิบัติตามกระบวนการที่คุณมีเพื่อตรวจสอบความถูกต้องของการอัปเดตอื่นๆ ในสภาพแวดล้อมของคุณ หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้การอัปเดตกับแอปการเงินและการดำเนินงาน ดูที่ [ภาพรวมรุ่นเดียว](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md)

### <a name="when-will-my-organization-be-migrated"></a>องค์กรของฉันจะย้ายเมื่อใด

การย้ายของแต่ละองค์กรจะขึ้นอยู่กับการตั้งค่าคอนฟิกและความพร้อมในปัจจุบันที่จะย้ายไปยังโครงสร้างพื้นฐานใหม่ วันที่เหล่านี้อาจเปลี่ยนแปลงได้

- องค์กรที่ปัจจุบันใช้โมดูล HR ในแอปการเงินและการดำเนินงานจะได้รับฟังก์ชัน HR สำหรับ Dynamics 365 Human Resources โดยเป็นส่วนหนึ่งของกระบวนการอัปเดตรุ่นหนึ่งปกติ โดยทั่วไป คุณลักษณะใหม่จะถูกวางแผนไว้ว่าจะพร้อมใช้งานโดยเริ่มต้นในมกราคม 2022
- องค์กรที่ใช้ Dynamics 365 Human Resources อยู่เท่านั้นจะสามารถเข้าถึงเครื่องมือการย้ายเพื่อให้องค์กรสามารถเริ่มต้นการทดสอบและเริ่มต้นการย้ายในกลางปี 2022 วันที่ที่ต้องย้ายไปยังโครงสร้างพื้นฐานใหม่ยังไม่ได้กำหนด อย่างไรก็ตาม จะมีเวลาอย่างน้อยหนึ่งปีหลังจากวันที่ที่เครื่องมือการย้ายพร้อมใช้งาน
- องค์กรที่ใช้ทั้ง Dynamics 365 Human Resources และแอปการเงินและการดำเนินงานอื่นอยู่ในขณะนี้จะสามารถเข้าถึงเครื่องมือการย้ายเพื่อให้องค์กรสามารถเริ่มต้นการทดสอบและเริ่มต้นการย้ายในปลายปี 2022 วันที่ที่ต้องย้ายไปยังโครงสร้างพื้นฐานใหม่ยังไม่ได้กำหนด อย่างไรก็ตาม จะมีเวลาอย่างน้อยหนึ่งปีหลังจากวันที่ที่เครื่องมือการย้ายพร้อมใช้งาน

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะใหม่สำหรับ Dynamics 365 Human Resources ดูที่ [มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงในทรัพยากรบุคคล](./hr-admin-whats-new.md)

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>องค์กรของฉันยังไม่เผยแพร่บน Dynamics 365 Human Resources เราควรใช้งานโมดูล Human Resources ในแอปการเงินและการดำเนินงานหรือใช้งานแอป Dynamics 365 Human Resources บนโครงสร้างพื้นฐานดั้งเดิม

สินค้าที่สําคัญที่ควรพิจารณาคือฟังก์ชัน HR ที่เป็นสิ่งที่ต้องการ และฟังก์ชันนั้นจะพร้อมใช้งานบนโครงสร้างพื้นฐานใหม่เมื่อใด หากองค์กรต้องการฟังก์ชันหลักในการจัดการบุคลากร ที่พร้อมใช้งานในปัจจุบันในโมดูล HR ของแอปการเงินและการดำเนินงานในโครงสร้างพื้นฐานใหม่ พาริตี้คุณลักษณะระหว่างโมดูล HR ของแอปการเงินและการดำเนินงานกับแอป Dynamics 365 Human Resources คาดว่าจะมีใช้งานในรุ่น 10.0.25 ซึ่งโดยทั่วไปแล้วจะมีให้ใช้งานในเดือนมีนาคม 2022 คุณลักษณะการรวม เช่น แอป Teams และการรวมเอนทิตี Dataverse จะพร้อมใช้งานในการออกใช้ในภายหลัง

หากฟังก์ชันของ HR ขององค์กรพร้อมใช้งานบนโครงสร้างพื้นฐานใหม่ภายในกรอบเวลาที่องค์กรจะใช้งานจริง อาจช่วยให้ใช้งานจริงบนโมดูล Human Resources ในแอปการเงินและการดำเนินงานได้ง่ายขึ้น ซึ่งจะส่งผลให้การย้ายง่ายขึ้น เนื่องจากจะเป็นการอัปเกรดแอปพลิเคชันมาตรฐานของแอปพลิเคชัน Dynamics 365 Human Resources และลูกค้าจะอยู่บนโครงสร้างพื้นฐานใหม่อยู่แล้ว หากองค์กรตัดสินใจที่จะใช้งานแอปพลิเคชัน Dynamics 365 Human Resources บนโครงสร้างพื้นฐานเดิม การย้ายสภาพแวดล้อมจะต้องย้ายไปที่โครงสร้างพื้นฐานใหม่ ซึ่งสามารถหลีกเลี่ยงการใช้ได้บนโครงสร้างพื้นฐานใหม่

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>ฉันใช้ความสามารถใหม่ที่พร้อมใช้งานเฉพาะใน Dynamics 365 Human Resources (เช่น **การลางานและการหยุดงาน** และ **การจัดการสวัสดิการ**) ขณะนี้ความสามารถเหล่านี้จะพร้อมใช้งานในโมดูล Human Resources บนโครงสร้างพื้นฐานของการเงินและการดำเนินงานด้วยหรือไม่

ใช่ โมดูลทั้งหมดจาก Dynamics 365 Human Resources จะใช้งานเช่นเดียวกับในแอปการเงินและการดำเนินงานและจะมีพาริตี้คุณลักษณะ 100 เปอร์เซ็นต์ ในฐานะส่วนหนึ่งของกลยุทธ์การย้ายโดยรวมของลูกค้าที่ปัจจุบันใช้ความสามารถเหล่านี้ใน HR ข้อมูลลูกค้าจะถูกย้ายเพื่อที่จะยังคงทำงานบนโครงสร้างพื้นฐานของการเงินและการดำเนินงาน

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>ฉันใช้ความสามารถการจัดการสวัสดิการ Dynamics 365 Human Resources ใหม่ ฉันสร้างการรวมที่กำหนดเองเข้ากับโมดูล HR ในโครงสร้างพื้นฐานของการเงินและการดำเนินงาน เพื่อให้ฉันใช้ประโยชน์จากความสามารถด้านค่าจ้างโดยการใช้ข้อมูลสวัสดิการ ต้องระบุการรวมที่กำหนดเองเหล่านี้เพื่อดำเนินการต่อหรือไม่

เนื่องจากเป็นส่วนหนึ่งของการผสานโครงสร้างพื้นฐาน ข้อมูล HR จะถูกพาไปยังฐานข้อมูลเดียวกันกับแอปการเงินและการดำเนินงานอื่นๆ คุณจะไม่ต้องมีการรวมระหว่างโมดูลในแอปการเงินและการดำเนินงานอีกต่อไป

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>องค์กรของฉันใช้โซลูชัน ISV หนึ่งโซลูชันหรือมากกว่ากับ Dynamics 365 Human Resources โซลูชัน ISV ของเราจะถูกย้ายโดยอัตโนมัติหรือไม่

ประสบการณ์การย้ายสำหรับแต่ละโซลูชันผู้ขายซอฟต์แวร์อิสระ (ISV) จะแตกต่างกันไป ทั้งนี้ขึ้นอยู่กับวิธีการรวมของโซลูชัน Microsoft จะร่วมกับ ISVs อย่างต่อเนื่องเพื่อให้แน่ใจว่าการเปลี่ยนไปยังโครงสร้างพื้นฐานใหม่จะเป็นไปอย่างต่อเนื่อง

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>องค์กรของฉันใช้การรวม LinkedIn Talent Hub กับ Dynamics 365 Human Resources การรวมนี้จะยังคงทำงานต่อไปหลังจากการเปลี่ยนแปลงโครงสร้างพื้นฐานเสร็จสมบูรณ์หรือไม่

ไม่ การรวม LinkedIn Talent Hub จะไม่ทำงานต่อไปหลังจากย้ายไปยังโครงสร้างพื้นฐานใหม่ บริการการรวม LinkedIn Talent Hub จะถูกถอนด้วยโครงสร้างพื้นฐาน Dynamics 365 Human Resources ดั้งเดิม

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>องค์กรของฉันใช้แอป Human Resources ใน Teams แอปจะยังคงทำงานต่อไปหลังจากการเปลี่ยนแปลงโครงสร้างพื้นฐานเสร็จสมบูรณ์หรือไม่

ใช่ แอป Human Resources ใน Teams จะยังคงทำงานต่อไปหลังจากย้ายไปยังโครงสร้างพื้นฐานใหม่

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>องค์กรของฉันมีการตั้งค่าคอนฟิกความปลอดภัยที่กําหนดเองใน Dynamics 365 Human Resources ความปลอดภัยที่กำหนดเองของเราจะยังคงใช้หลังจากการเปลี่ยนแปลงโครงสร้างพื้นฐานเสร็จสมบูรณ์หรือไม่

ใช่ การตั้งค่าคอนฟิกความปลอดภัยที่กําหนดเองจะรวมอยู่ในการย้ายข้อมูลไปยังโครงสร้างพื้นฐานใหม่

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>เราใช้งานตัวรวมข้อมูลเพื่อย้ายข้อมูลระหว่าง Dynamics 365 Human Resources กับแอปการเงินและการดำเนินงาน ข้อมูลที่จะรวมในปัจจุบันจะได้รับผลกระทบอย่างไร

ข้อมูล HR ที่ปัจจุบันเป็นต้นฉบับใน Dynamics 365 Human Resources มีการซิงโครไนส์กับ Dataverse จากนั้นตัวรวมข้อมูลสามารถใช้การซิงโครไนส์กับแอปการเงินและการดำเนินงานแบบทางเดียวได้ หลังจากการย้ายข้อมูลไปยังโครงสร้างพื้นฐานใหม่ ข้อมูล HR จะเป็นข้อมูลเริ่มต้นในแอปการเงินและการดำเนินงาน ตัวรวมข้อมูลจะไม่ต้องใช้ในการซิงโครไนส์ข้อมูลระหว่างแอปการเงินและการดำเนินงานกับ Human Resources อีกต่อไป

ตารางข้อมูลดั้งเดิมของ Dataverse ปัจจุบันใน Human Resources จะซิงโครไนส์ข้อมูลจากสภาพแวดล้อมบนโครงสร้างพื้นฐานใหม่ต่อไป เอนทิตีจะถูกแปลงเพื่อสนับสนุนการรวมแบบสองทิศทาง การรวมข้อมูลอื่นใดที่ตั้งค่าคอนฟิกผ่านตัวรวมข้อมูลโดยเทียบกับตารางเหล่านี้กับตารางอื่นๆ ของแอ Dynamics 365 จะใช้งานต่อไปตามที่ตั้งค่าคอนฟิกไว้ในปัจจุบัน

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>เราใช้งานการรวมแบบสองทิศทางเพื่อย้ายข้อมูล HR ระหว่าง Dataverse กับแอปการเงินและการดำเนินงานอื่นๆ การย้ายไปยังโครงสร้างพื้นฐานใหม่จะส่งผลกระทบต่อข้อมูลที่ถูกรวมในปัจจุบันอย่างไร

ข้อมูล HR จะเป็นข้อมูลเริ่มต้นในแอปการเงินและการดำเนินงานในสภาพแวดล้อมบนโครงสร้างพื้นฐานใหม่ จากนั้นจะมีการใช้การรวมแบบสองทิศทางเพื่อย้ายข้อมูล HR ระหว่างสภาพแวดล้อมใหม่และสภาพแวดล้อม Dataverse

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>เราได้สร้างการรวมที่กำหนดเองจาก Dynamics 365 Human Resources ไปยังระบบภายนอกหนึ่งระบบหรือมากกว่า เราจะต้องพัฒนาการรวมใหม่หลังจากการเปลี่ยนแปลงโครงสร้างพื้นฐานเสร็จสมบูรณ์หรือไม่

ขึ้นอยู่กับปลายทางการรวม สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเทคโนโลยีการรวมที่พร้อมใช้งานในแอปการเงินและการดำเนินงาน และวิธีเลือกเทคโนโลยีการรวมที่ดีที่สุด ดูที่ [ภาพรวมการรวม](../fin-ops-core/dev-itpro/data-entities/integration-overview.md)

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>เราได้ขยาย Dataverse สำหรับ Dynamics 365 Human Resources แล้ว ส่วนขยายเหล่านี้จะถูกย้ายโดยอัตโนมัติหรือไม่

หากสภาพแวดล้อม Dynamics 365 Human Resources และการเงินและการดำเนินงานที่จะรวมในสภาพแวดล้อมในโครงสร้างพื้นฐานใหม่เชื่อมต่อกับสภาพแวดล้อม Dataverse เดียวกัน แอปทั้งสองจะเชื่อมต่อกับสภาพแวดล้อม Dataverse เดียวกันต่อไปหลังจากการย้ายข้อมูล การย้ายข้อมูลจะไม่ต้องใช้ในส่วนขยาย Dataverse ใดๆ

อย่างไรก็ตาม หากสภาพแวดล้อม Dynamics 365 Human Resources และการเงินและการดำเนินงานที่ปัจจุบันเชื่อมต่อกับสภาพแวดล้อม Dataverse ต่างกัน สภาพแวดล้อม Dataverse ทั้งสองจะต้องรวมกันเพื่อให้เชื่อมต่อกับสภาพแวดล้อมเดียวบนโครงสร้างพื้นฐานใหม่ สำหรับการรวม Dataverse นี้ ตาราง Dataverse มาตรฐานของโซลูชัน Human Resources สามารถเชื่อมต่อและซิงโครไนส์ใหม่กับสภาพแวดล้อม Dataverse ใหม่ได้ ส่วนขยายใดๆ ไปยังสภาพแวดล้อม Dataverse จะไม่ถูกย้ายโดยอัตโนมัติ แต่ต้องถูกปรับใช้ใหม่ในสภาพแวดล้อมใหม่ ขอแนะนำให้คุณใช้โซลูชันที่มีการจัดการเพื่อจัดการส่วนขยาย Dataverse ของคุณ สำหรับข้อมูลเพิ่มเติม ดูที่ [บทนําเกี่ยวกับโซลูชัน](/powerapps/developer/data-platform/introduction-solutions)

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>เราได้ตั้งค่าคอนฟิกโฟลว์ Microsoft Power Automate และ/หรือ Microsoft Power Apps เพื่อทำงานกับ Dynamics 365 Human Resources ส่วนประกอบ Microsoft Power Platform เหล่านี้จะถูกย้ายและใช้งานโดยอัตโนมัติหลังจากเสร็จสิ้นการเปลี่ยนแปลงโครงสร้างพื้นฐานหรือไม่

โฟลว์ Power Apps, Power Automate และการกำหนด Microsoft Power Platform อื่นๆ จะคล้ายกับส่วนขยาย Dataverse การย้ายไปยังโครงสร้างพื้นฐานใหม่จะใช้งานโดยอัตโนมัติหรือไม่จะขึ้นอยู่กับว่าแอป Human Resources และแอปการเงินและการดำเนินงานเชื่อมโยงกับสภาพแวดล้อม Power Apps เดียวกันก่อนการย้ายหรือไม่

หากแอปเชื่อมต่อกับสภาพแวดล้อม Power Apps เดียวกันอยู่ในขณะนี้ แอปเหล่านั้นจะยังคงเชื่อมต่อกับสภาพแวดล้อม Power Apps นั้นต่อไปหลังจากการย้ายข้อมูลไปยังโครงสร้างพื้นฐานใหม่ ในกรณีนี้ โฟลว์ Power Apps, Power Automate และการกําหนด Microsoft Power Platform อื่นๆ จะยังคงทำงานต่อไปโดยไม่มีการตั้งค่าคอนฟิกเพิ่มเติม ขอแนะนำให้คุณใช้โซลูชันที่มีการจัดการเพื่อจัดการส่วนขยายแอปพลิเคชันของคุณบน Dataverse สำหรับข้อมูลเพิ่มเติม ดูที่ [บทนําเกี่ยวกับโซลูชัน](/powerapps/developer/data-platform/introduction-solutions)

อย่างไรก็ตาม หากแอป Human Resources และแอปการเงินและการดำเนินงานเชื่อมโยงกับสภาพแวดล้อม Power Apps แยกต่างหาก แอปนั้นจะต้องถูกรวมเป็นส่วนหนึ่งของการย้ายข้อมูล งานนี้จะต้องปรับใช้ Power Apps และการกำหนดอื่นอีกครั้งในสภาพแวดล้อมใหม่

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>เราได้เปิดใช้งานตารางเสมือน Dataverse สำหรับ Dynamics 365 Human Resources จะเกิดอะไรกับตารางเหล่านี้ระหว่างการย้าย

หลังจากการย้าย ถ้าสภาพแวดล้อมในโครงสร้างพื้นฐานใหม่ยังคงเชื่อมต่อกับสภาพแวดล้อม Dataverse ที่เชื่อมต่อ Dynamics 365 Human Resources อยู่ในขณะนี้ ตารางเสมือน Dataverse ที่สร้างขึ้นในสภาพแวดล้อมนั้นจะยังคงทำงานต่อไปโดยไม่มีการตั้งค่าคอนฟิกเพิ่มเติม

อย่างไรก็ตาม ถ้าสภาพแวดล้อมในโครงสร้างพื้นฐานใหม่เชื่อมต่อกับสภาพแวดล้อม Dataverse อื่นหลังจากการย้าย ตารางเสมือนจะต้องถูกสร้างใหม่ในสภาพแวดล้อม Dataverse ใหม่

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>เราได้พัฒนาการรวมโดยใช้ API ระบบติดตามผู้สมัคร (ATS) API, PAYROLL API, ตารางเสมือน Dataverse สำหรับ Dynamics 365 Human Resources หรือเอนทิตีอื่นใน Web API ของ Dataverse การรวมเหล่านี้จะยังคงทำงานต่อไปหลังจากการเปลี่ยนแปลงโครงสร้างพื้นฐานเสร็จสมบูรณ์หรือไม่

หลังจากการย้าย ถ้าสภาพแวดล้อมในโครงสร้างพื้นฐานใหม่ยังคงเชื่อมต่อกับสภาพแวดล้อม Dataverse ที่เชื่อมต่อ Dynamics 365 Human Resources อยู่ในขณะนี้ การรวมใดๆ ที่ปรับใช้กับ Web API Dataverse จะยังคงทำงานต่อไปหลังการย้ายเสร็จสิ้น

อย่างไรก็ตาม หากสภาพแวดล้อมในโครงสร้างพื้นฐานใหม่เชื่อมต่อกับสภาพแวดล้อม Dataverse ต่างกันหลังการย้าย การรวมใดๆ ที่ปรับใช้กับ Web API Dataverse จะต้องกำหนดค่าใหม่เพื่อให้เชื่อมต่อกับสภาพแวดล้อม Dataverse ใหม่

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>มีผลกระทบกับภูมิภาค Azure เมื่อย้ายสภาพแวดล้อมของฉันหรือไม่

คาดว่าสภาพแวดล้อม Human Resources จะยังคงอยู่ในภูมิภาค Azure เดียวกันในระหว่างการย้าย ข้อยกเว้นเพียงอย่างเดียวจะเกิดขึ้นถ้าสภาพแวดล้อม Human Resources จะถูกผสานกับสภาพแวดล้อมการเงินและการดำเนินงานที่อยู่ในภูมิภาคแตกต่างกัน ในกรณีนี้ สภาพแวดล้อม Human Resources จะถูกย้ายไปยังภูมิภาค Azure ของสภาพแวดล้อมการเงินและการดำเนินงาน

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>องค์กรของฉันขึ้นอยู่กับลำดับงานใน Dynamics 365 Human Resources ของกระบวนการทางธุรกิจหนึ่งกระบวนการหรือมากกว่า ลำดับงานนี้จะถูกย้ายโดยอัตโนมัติหรือไม่

ใช่ จะมีการย้ายการตั้งค่าคอนฟิกลำดับงาน ประวัติลำดับงาน และลำดับงานที่อยู่ดำเนินการในปัจจุบัน

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>การฝึกอบรมและทรัพยากรใดที่จะพร้อมใช้งานเพื่อช่วยในกระบวนการย้าย

คู่มือแบบเต็มจะได้รับการจัดเตรียมไว้เพื่ออธิบายแต่ละขั้นตอนของกระบวนการย้ายโดยละเอียด ทรัพยากรการฝึกอบรมเพิ่มเติม เช่น วิดีโอและศูนย์บริการอาจพร้อมใช้งานได้ ทั้งนี้ขึ้นอยู่กับความต้องการ

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>องค์กรของฉันสร้างมุมมองที่บันทึกไว้ใน Dynamics 365 Human Resources เพื่อปรับปรุงการใช้งานของอินเทอร์เฟสมากขึ้น มุมมองที่บันทึกไว้นี้จะถูกย้ายโดยอัตโนมัติหรือไม่

ใช่ มุมมองที่บันทึกไว้จะถูกย้ายไปยังโครงสร้างพื้นฐานใหม่

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>เราจะใช้ Ceridian กับ Dynamics 365 Human Resources การรวม Ceridian จะพร้อมใช้งานหลังจากการเปลี่ยนแปลงโครงสร้างพื้นฐานเสร็จสมบูรณ์หรือไม่ 

การรวมกับ Ceridian จะถูกย้ายไปยังการรวมโดยใช้ API ของค่าจ้าง การรวมโดยใช้ไฟล์ที่มีอยู่ในปัจจุบันใน Dynamics 365 Human Resources จะไม่ถูกย้ายไปยังโครงสร้างพื้นฐานของการเงินและการดำเนินงาน สำหรับข้อมูลเพิ่มเติม ดูที่ [บทนําเกี่ยวกับ API บัญชีเงินเดือน](./hr-admin-integration-payroll-api-introduction.md)

### <a name="how-will-the-migration-affect-the-service-update-process"></a>การย้ายจะมีผลต่อกระบวนการอัปเดตบริการอย่างไร

เมื่อย้ายข้อมูลแล้ว ลูกค้าจะมีความยืดหยุ่นมากขึ้นในแง่ของ ALM และการอัปเดตบริการ การอัปเดตบริการจะไม่มีผลกับสภาพแวดล้อม Human Resources อีกต่อไปโดยอัตโนมัติ แต่บริการจะเป็นไปตามกระบวนการและฟังก์ชันการอัปเดตบริการรุ่นหนึ่ง ดังนั้น ตัวเลือกการตั้งค่าคอนฟิกเพื่อการอัปเดตจะสามารถใช้งานได้ผ่าน LCS สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของรุ่นหนึ่ง](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md)

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>การย้ายจะส่งผลกระทบต่อโครงการ LCS ของฉันของ Dynamics 365 Human Resources อย่างไร

การย้ายไปยังโครงสร้างพื้นฐานใหม่จะย้ายการจัดการสภาพแวดล้อม Dynamics 365 Human Resources ของคุณไปยังโครงการดําเนินการของการเงินและการดำเนินงานใน LCS หากการย้ายผสาน Dynamics 365 Human Resources กับสภาพแวดล้อมการเงินและการดำเนินงานปัจจุบัน โครงการ Human Resources LCS ของคุณจะถูกรวมไว้ในโครงการดําเนินการ LCS ของแอปการเงินและการดำเนินงาน หากปัจจุบันคุณใช้เพียง Dynamics 365 Human Resources โครงการดําเนินการ LCS ใหม่จะถูกสร้าง และโครงการ Human Resources LCS ที่มีอยู่ของคุณจะถูกย้ายไปยังโครงการใหม่

โครงการใหม่จะเป็นโครงการชนิดเดียวกันกับที่แอปการเงินและการดำเนินงานใช้ ซึ่งจะมีคุณลักษณะและฟังก์ชันเดียวกันนี้ในการจัดการสภาพแวดล้อม สำหรับข้อมูลเพิ่มเติม ให้ดู [ทรัพยากร Lifecycle Services](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>เราได้เชื่อมโยงการบันทึกงานของเรากับ Business Process Modeler ใน Human Resources Business Process Modeler จะย้ายและผสานไว้ใน LCS อย่างไร

ไลบรารีกระบวนการทางธุรกิจของโครงการ LCS จะถูกย้ายไปยังโครงการ LCS ใหม่สำหรับ Human Resources

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>ปัจจุบันองค์กรของฉันใช้เฉพาะ Dynamics 365 Human Resources เท่านั้น มีทรัพยากรใดที่พร้อมใช้งานเพื่อให้เราสามารถเรียนรู้เพิ่มเติมเกี่ยวกับความสามารถด้านการพัฒนาหลังจากที่การเปลี่ยนแปลงโครงสร้างพื้นฐานเสร็จสมบูรณ์

ทั้งตัวเลือกความสามารถในการเพิ่มฟังก์ชัน Microsoft Power Platform และตัวเลือกความสามารถในการเพิ่มฟังก์ชันการเงินและการดำเนินงานจะพร้อมใช้งานและสามารถใช้กับการพัฒนาได้ สำหรับข้อมูลเพิ่มเติม ดูที่ [พัฒนาและกำหนดโฮมเพจ](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md)

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>เราได้เปิดใช้งานคุณลักษณะใน Dynamics 365 Human Resources คุณลักษณะเหล่านี้จะถูกเปิดใช้งานโดยอัตโนมัติระหว่างการย้ายหรือไม่

คุณลักษณะเปิดใช้งานโดยอัตโนมัติในโครงสร้างพื้นฐานใหม่จะถูกกําหนดแยกกันหรือไม่ ข้อมูลนี้จะถูกรวมไว้ในคู่มือคุณลักษณะ

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>เกิดอะไรขึ้นกับฐานข้อมูล BYOD ของฉันระหว่างการย้าย

นําเข้าและส่งออกการตั้งค่าคอนฟิกเพื่อนําเข้าฐานข้อมูลของคุณเอง (BYOD) จะถูกย้ายไปยังโครงสร้างพื้นฐานใหม่

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>เกิดอะไรขึ้นกับ Azure Data Lake ของฉันระหว่างการย้าย

การส่งออกใดๆ ที่ตั้งค่าคอนฟิกในปัจจุบันสำหรับ Azure Data Lake Storage ในแอปการเงินและการดำเนินงานจะรักษาการตั้งค่าคอนฟิกเดียวกันไว้หลังจากการย้ายข้อมูล

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>ขณะนี้เราใช้ Dynamics AX 2012 เครื่องมือการอัปเกรดที่พร้อมใช้งานในปัจจุบันจะใช้เพื่ออัปเกรดโมดูล HR ใน AX 2012 ไปยัง Dynamics 365 Human Resources หรือไม่

ใช่ Dynamics 365 Human Resources จะรวมอยู่ในโค้ดพื้นฐานที่ผสานและโครงสร้างพื้นฐานของแอปการเงินและการดำเนินงาน การอัปเกรดจาก Dynamics AX 2012 เป็น Dynamics 365 Human Resources จะใช้พาธการอัปเกรดและเครื่องมือเดียวกันกับที่ใช้ในการอัปเกรดเป็นแอปการเงินและการดำเนินงานรุ่นล่าสุด

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>เราจะใช้การจัดการเอกสารกับ Dynamics 365 Human Resources จะเกิดอะไรกับเอกสารระหว่างการย้าย

เอกสารจะยังคงอยู่ในที่จัดเก็บเอกสารปัจจุบัน โดยจะแมปใหม่ไปยังสภาพแวดล้อมในโครงสร้างพื้นฐานใหม่

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>เกิดอะไรขึ้นกับชุดงานที่เราได้ตั้งค่าคอนฟิกใน Dynamics 365 Human Resources หลังจากการย้าย

ชุดงานที่ใช้ได้จะถูกย้ายไปยังโครงสร้างพื้นฐานใหม่โดยอัตโนมัติ

## <a name="licensing-impact"></a>ผลกระทบของการให้สิทธิ์การใช้งาน

คู่มือนี้จะไม่ใช้แทนหรือแทนที่เอกสารทางกฎหมายใดๆ ที่ครอบคลุมสิทธิ์การใช้

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>องค์กรของฉันใช้ Dynamics 365 Human Resources ในการจัดการดําเนินงานด้าน HR การให้สิทธิ์การใช้งานหรือต้นทุนของเราเปลี่ยนแปลงหรือไม่

ลูกค้าที่มีสิทธิ์การใช้งาน Dynamics 365 Human Resources ที่ซื้อจะไม่ได้รับผลกระทบ ไม่มีการย้ายการให้สิทธิ์การใช้งานระหว่างลูกค้าเหล่านี้ หน่วยการเก็บสต็อกสินค้า Sandbox เพิ่มเติม (SKU) เฉพาะของ Human Resources จะใช้ไม่ได้อีกต่อไป แต่ลูกค้าสามารถเลือกซื้อแอปการเงินและการดำเนินงาน Sandbox ระดับ 2 เท่านั้นที่ต้นทุนต่ำกว่าเล็กน้อยได้ ลูกค้าปัจจุบันที่ซื้อ Human Resources Sandbox จะย้ายไปยังแอปการเงินและการดำเนินงาน Sandbox ระดับ 2 โดยไม่มีค่าใช้จ่ายเพิ่มเติม

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>องค์กรของฉันใช้โมดูล Human Resources ใน Dynamics 365 Finance, Supply Chain Management, Commerce หรือ Project Operations การให้สิทธิ์การใช้งานหรือต้นทุนของฉันเปลี่ยนแปลงหรือไม่

ผู้ใช้ปัจจุบันของแอป Dynamics 365 และผู้ใช้ Dynamics 365 Finance, Supply Chain Management, Commerce และ Project Operations แบบสแตนด์อโลนสามารถเข้าถึง Human Resources ซึ่งเป็นส่วนหนึ่งของสิทธิ์การใช้งานเหล่านั้นได้จนถึงเดือนกุมภาพันธ์ 2025 หรือจนกว่าข้อตกลงการให้สิทธิ์การใช้งานปัจจุบันจะหมดอายุ แล้วแต่ว่าข้อใดเกิดก่อน คุณสามารถเลือกที่จะย้ายไปยังสิทธิ์การใช้งานของ Human Resources ได้ก่อนหน้า หากช่วยให้คุณสามารถประหยัดต้นทุนได้ดีขึ้น เริ่มต้นจากเดือนกุมภาพันธ์ 2025 ลูกค้า CSP และ EA ปัจจุบันทั้งหมดต้องย้อนกลับโมดูล HR และซื้อสิทธิ์การใช้งาน Human Resources เพื่อใช้ประโยชน์จากความสามารถใหม่ที่จะมาถึงแอปการเงินและการดำเนินงาน

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>องค์กรของฉันใช้ Dynamics 365 Finance, Supply Chain Management, Commerce หรือ Project Operations เราจะต้องซื้อสภาพแวดล้อมเพิ่มเติมเพื่อสนับสนุนการผสานโครงสร้างพื้นฐานหรือไม่

ไม่ สภาพแวดล้อมเพิ่มเติมไม่จำเป็นสำหรับสนับสนุนการเปลี่ยนแปลงโครงสร้างพื้นฐาน

