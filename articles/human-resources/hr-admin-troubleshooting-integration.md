---
title: การรวมกับคำถามที่พบบ่อยเกี่ยวกับ Finance
description: บทความนี้อธิบายว่าข้อมูลใดจะถูกซิงโครไนส์ในการรวม Human Resources และ Finance
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a6432fb5b04097d81680aed4e940e47f5ff2902
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114446"
---
# <a name="integration-with-finance-faq"></a>การรวมกับคำถามที่พบบ่อยเกี่ยวกับ Finance

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้ตอบคำถามสำหรับคำถามทั่วไปที่เกี่ยวข้องเกี่ยวกับว่าข้อมูลใดจะถูกซิงโครไนส์เมื่อ Dynamics 365 Human Resources ถูกรวมกับ Dynamics 365 Finance

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>ฉันสามารถแก้ไขผู้ใช้แอปพลิเคชัน Dynamics 365 Talent ใน Power Apps ได้หรือไม่

ลำดับที่ ถ้าคุณแก้ไขผู้ใช้แอปพลิเคชัน Human Resources การรวมระหว่างทรัพยากรบุคคลและ Dataverse อาจล้มเหลว ตารางต่อไปนี้จะแสดงการตั้งค่าเริ่มต้นสำหรับผู้ใช้แอปพลิเคชัน Talent

| ชื่อเต็ม | รหัสแอปพลิเคชัน | รหัสออบเจ็กต์ Azure AD | URI รหัสแอปพลิเคชัน |
| --- | --- | --- | --- |
| Dynamics365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![การตั้งค่าเริ่มต้นสำหรับผู้ใช้แอปพลิเคชัน Talent](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>คือข้อมูลที่ซิงโครไนซ์ทั้งหมด หรือเพียงแค่เอนทิตีข้อมูล

ชุดย่อยของข้อมูลจะมีการซิงโครไนส์ สำหรับรายการของเอนทิตีทั้งหมด ดูที่ [การรวมกับ Dynamics 365 Finance](hr-admin-integration-finance.md)

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>เพราะเหตุใดฉันจึงไม่เห็นข้อมูลใดๆ ที่มีการซิงค์กับ Dataverse

โดยค่าเริ่มต้น การรวม Dataverse จะถูกปิดใช้งานในสภาพแวดล้อมใหม่ที่ไม่มีข้อมูลสาธิตที่ระบุ โดยค่าเริ่มต้น จะมีการเปิดใช้งานในสภาพแวดล้อมใหม่ซึ่งรวมถึงข้อมูลสาธิต และการซิงโครไนส์ข้อมูลจะเริ่มต้นขึ้นเมื่อมีการจัดเตรียมสภาพแวดล้อม หลังจากที่สภาพแวดล้อมของคุณพร้อมที่จะซิงค์ข้อมูลแล้ว คุณสามารถเปิดใช้งานการรวมได้ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกการรวม Dataverse](hr-admin-integration-common-data-service.md)

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>ฉันสามารถสร้างการแม็ปใหม่โดยไม่ใช้เท็มเพลได้หรือไม่

เท็มเพลตเป็นจุดเริ่มต้น คุณสามารถสร้างเท็มเพลตของคุณเอง แต่จำเป็นต้องใช้เท็มเพลเสมอเมื่อสร้างโครงการการรวม สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวรวมข้อมูล (DI) เท็มเพลต และโครงการ ดูที่ [รวมข้อมูลลงใน Microsoft Dataverse](https://docs.microsoft.com/powerapps/administrator/data-integrator)

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>ฉันสามารถแม็ปมิติทางการเงินที่จะโอนย้ายระหว่าง Human Resources และ Finance ได้หรือไม่

ในปัจจุบันมิติทางการเงินไม่ได้อยู่ใน Dataverse สำหรับแอป และผลลัพธ์ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น เอนทิตี้นี้มีการวางแผน แต่ไม่มีเส้นเวลาการนำออกใช้ที่พร้อมใช้งานอยู่ในปัจจุบัน

สำหรับข้อมูลที่อยู่ใน Finance แต่ไม่มีอยู่ใน Human Resources ให้เชื่อมโยงสองระบบเข้าด้วยกันโดยใช้ **ตั้งค่าคอนฟิกลิงค์** ใน Human Resources

![แม็ปมิติทางการเงิน](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>ในบางครั้งเมื่อฉันนำเข้าพนักงาน รายการจะไปอยู่ที่พนักงานที่ไม่ได้ใช้งานใน Finance เพราะเหตุใด?

คุณอาจได้รับข้อผิดพลาดนี้ถ้าพนักงานไม่มีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่ใน Human Resources เมื่อต้องการแก้ไขปัญหานี้ ไปที่ **การจัดการบุคลากร \> พนักงาน \> ประวัติการจ้างงาน \> ตัวจัดการวันที่** และตรวจสอบว่ามีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่หรือไม่

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>ถ้าฉันเลือกที่จะแม็ปเฉพาะชุดย่อยของฟิลด์ การเปลี่ยนแปลงของฟิลด์ที่ไม่ได้แม็ปจะทริกเกอร์การซิงค์หรือไม่

ซิงค์ข้อมูลเป็นไปตามกำหนดการดำเนินการ การรวมจะเบิกสินค้าเรกคอร์ดถ้าฟิลด์ใดๆ ในเรกคอร์ดเปลี่ยนแปลง โดยไม่คำนึงถึงว่าฟิลด์ดังกล่าวเป็นส่วนหนึ่งของการแม็ปการรวม

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>ฉันจะส่งการเปลี่ยนแปลงของพนักงานที่ใช้งานอยู่เท่านั้น ไม่ใช่เรกคอร์ดที่สิ้นสุดการจ้างงานได้อย่างไร

ด้วยการใช้ "การสอบถามขั้นสูง" คุณสามารถกรองและปรับรูปร่างแหล่งข้อมูลก่อนที่จะส่งผ่านไปยังปลายทาง

![การสอบถามขั้นสูงของผู้ปฏิบัติงานที่ใช้งานอยู่](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>ฉันสามารถระบุฟิลด์ที่จะส่งไปยัง Finance สำหรับเอนทิตีที่เฉพาะเจาะจงได้หรือไม่

คุณสามารถเพิ่มหรือลบฟิลด์ออกจากงานรวม ไม่ใช่ฟิลด์ข้อมูลทั้งหมดที่มีอยู่ในตาราง Dataverse ที่จะถูกเติมข้อมูลจาก Human Resources
คุณสามารถเติมข้อมูลเพิ่มเติมได้ผ่าน Power Apps

![เพิ่มหรือลบฟิลด์ไปยังและออกจากงานการรวม](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>ฉันตั้งค่าการรวมเป็นชุดงาน แต่ Human Resources สูญเสียการเชื่อมต่อไปกับระบบปลายทาง ฉันจะส่งชุดการเปลี่ยนแปลงเดียวกันไปยังระบบปลายทางได้อย่างไร

ไม่จำเป็นต้องมีการตั้งค่าพิเศษสำหรับการจัดการข้อยกเว้น ตัวรวมข้อมูลจะตรวจจับและรายงานข้อผิดพลาดที่เกิดขึ้นที่ต้นทางและปลายทางโดยอัตโนมัติ และจะอนุญาตให้ลองใหม่ด้วยตนเอง อย่างไรก็ตาม คุณไม่สามารถแก้ไขข้อมูลด้วยตนเองได้ ถ้าจำเป็นต้องปรับปรุงข้อมูล ควรทำที่ต้นทางหรือปลายทางอย่างใดอย่างหนึ่ง

## <a name="can-i-set-up-bi-directional-integration"></a>ฉันสามารถตั้งค่าการรวมสองทิศทางได้หรือไม่

ไม่ใช่ การรวมในปัจจุบันเป็นทางเดียว (Human Resources ไปยัง Finance and Operations) อย่างไรก็ตาม มีเท็มเพลตเริ่มต้นที่มีอยู่เพื่อส่งข้อมูลจาก Human Resources ไปยัง Finance

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>ฉันจะอนุญาตให้ลบเรกคอร์ดโดยเป็นส่วนหนึ่งของการรวมของฉันได้หรือไม่

ไม่ได้ ตัวรวมข้อมูลจะไม่รวบรวมเรกคอร์ดที่ถูกลบสำหรับการโอนย้ายข้อมูล มีเฉพาะการสร้างข้อมูลและการปรับปรุง (UPSERT) ถูกรวมอยู่ในขณะนี้

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>ฉันสามารถเรียกใช้การดำเนินการที่มีข้อผิดพลาดได้หรือไม่ ถ้าเป็นเช่นนั้น จะส่งไฟล์ทั้งหมดหรือเฉพาะที่มีการเปลี่ยนแปลง

การเรียกใช้ครั้งแรกของตัวรวมข้อมูลจะรันแบบเต็มเสมอ การเรียกใช้ในเวลาต่อมาขึ้นอยู่กับการติดตามการเปลี่ยนแปลง เมื่อดำเนินการการรันข้อผิดพลาด จะแยกเรกคอร์ดในขอบเขตของการรัน และส่งการเปลี่ยนแปลงล่าสุดจาก Dataverse

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>เมื่อฉันบันทึกโครงการ ฉันได้รับข้อผิดพลาด: "โครงการมีข้อผิดพลาดในการแม็ป" ฉันควรทำอย่างไร

ตรวจสอบการตั้งค่าของคีย์รวมของคุณ ทำการเปลี่ยนแปลงที่จำเป็นเพื่อตั้งค่า แล้วรีเฟรชเอนทิตี้ในโครงการ

เมื่อมีการใช้เท็มเพลตเริ่มต้น คีย์รวมจะถูกนำเข้าโดยอัตโนมัติ ปัญหานี้อาจเกิดขึ้นเมื่อมีการเพิ่มงานใหม่ไปยังเท็มเพลตที่มีอยู่

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>ถ้าฉันมีนิติบุคคลซึ่งเป็นพนักงานที่มีการจ้างงานจำนวน N ราย ฉันต้องสร้างการแม็ปสำหรับแต่ละคนหรือไม่

ใช่ สำหรับแต่ละนิติบุคคลใน Finance คุณจำเป็นต้องมีโครงการรวมที่แยกต่างหากในการรวมข้อมูล

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>ฉันต้องการถ่ายโอนข้อมูลที่ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้นที่จัดเตรียมให้โดย Microsoft ฉันสามารถทำได้หรือไม่

ได้ คุณสามารถเพิ่มหรือลบฟิลด์ออกจากเท็มเพลตที่มีอยู่ คุณสามารถปรับเปลี่ยนแม่แบบเพื่อรวมข้อมูลเพิ่มเติมจากตาราง Dataverse อื่น ๆ เอนทิตีต้องอยู่ใน Dataverse สำหรับแอปเพื่อให้รวมอยู่ในเท็มเพลต 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>ฉันเพิ่งสร้างสภาพแวดล้อม Finance และ Human Resources ใหม่ และฉันได้รับข้อผิดพลาด "ค่าข้อมูลละเมิดข้อจำกัดความถูกต้อง" เพราะเหตุใด?

สาเหตุของข้อผิดพลาดนี้อาจรวม:

- การโอนย้ายข้อมูลที่เป็นผลลัพธ์ในเรกคอร์ดที่ซ้ำกันในการแยกข้อมูลลที่ต้นทาง (Dataverse)

- การโอนย้ายข้อมูลมีค่า null สำหรับฟิลด์ที่จำเป็นใน Finance and Operations ตรวจสอบข้อมูลที่อยู่ใน Dataverse และตรงตามข้อกำหนดของ Finance and Operations

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>ถ้ามีข้อผิดพลาดการดำเนินการ และรหัสพนักงานยังไม่ได้ซิงค์ ฉันจะค้นหาประวัติงานที่มีเรกคอร์ดพนักงานที่ล้มเหลวได้อย่างไร

ตัวรวมข้อมูลจะสร้างหลายโครงการใน Finance ความสัมพันธ์ระหว่างงานตัวรวมข้อมูลและโครงการ Finance คือหนึ่งต่อหนึ่ง

ติดตามเวลาจากประวัติการดำเนินการตัวรวมข้อมูลและค้นหาโครงการดัชนี -1 ใน Finance ถ้าหมายเลขงานคือ 9 ในตัวรวมข้อมูล ดัชนีใน Finance คือ 8

1. จัดดัชนีงานจากตัวรวมข้อมูล (ในตัวอย่างนี้คือ "9")

    ![จับดัชนีงานจากตัวรวมข้อมูล](media/CaptureTaskIndex.png)

2. ติดตามเวลาการดำเนินการของโครงการ

    ![ติดตามเวลาการดำเนินการของโครงการ](media/CaptureTimeOfExecution.png)

3. ใน Finance ให้ระบุดัชนี - 1 ในตัวอย่างนี้ โครงการที่มีคำเสริมท้ายเป็น "8" และเวลาการดำเนินการของดัชนีเป็น "0" โครงการจะสอดคล้องกับเวลาการดำเนินการในขั้นตอนที่ 2

    ![ระบุดัชนี](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>หลังจากการรวม Human Resources และ Finance แล้ว ฉันไม่เห็นข้อมูล Human Resources ของฉันใน Finance ฉันควรทำอย่างไร

การรวมกับ Finance มีสองขั้นตอน ก่อนอื่น ตรวจสอบว่าข้อมูล Human Resources ถูกปรับปรุงแล้ว และพร้อมใช้งานใน Dataverse นี่เป็นการซิงค์แบบเรียลไทม์แบบใกล้ และสามารถตรวจสอบใน Power Apps โดยดูข้อมูลภายในตารางข้อมูล

![ข้อมูลใน Dataverse](media/DataInCDS.png)

ถ้าข้อมูลไม่ปรากฏตามที่คาดไว้ใน Dataverse ให้ตรวจสอบว่าเอนทิตีได้รับการสนับสนุนในการรวม เพื่อรวมข้อมูลเพิ่มเติมใน Dataverse จะต้องทำการเปลี่ยนแปลงทางฝั่ง Microsoft

ถ้าเอนทิตีได้รับการสนับสนุน และข้อมูลมีอยู่ใน Dataverse ให้ตรวจสอบว่าการแม็ปถูกต้องในตัวรวมข้อมูล ถ้าการค้นหาการแม็ปตัวรวมเป็นปกติ ให้ตรวจสอบมีการรันงานการจัดการข้อมูลเสร็จเรียบร้อยแล้ว ข้อผิดพลาดอาจเกิดขึ้นในระหว่างการดำเนินการชุดงาน สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการข้อมูล ดู [การจัดการข้อมูล](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>ที่อยู่สำหรับพนักงานของฉันไม่ถูกต้อง หลังจากที่ฉันนำเข้าไปยัง Finance ฉันควรทำอย่างไร

ลำดับหมายเลขสำหรับ **รหัสสถานที่** ใช้รูปแบบเดียวกันในทั้ง Human Resources และ Finance ลำดับหมายเลขต้องไม่ซ้ำกันทั้งสองด้าน เพื่อให้ไม่มีการชนกันของที่อยู่เมื่อรวมข้อมูลจาก Dataverse ไปยัง Finance and Operations

ในระหว่างการใช้งานของ Human Resources ให้ตรวจสอบว่าลำดับหมายเลขไม่เหมือนกันใน Human Resources และ Finance ตรวจสอบว่าลำดับหมายเลขทั้งหมดไม่เหมือนกันซึ่งอาจจะรักษาข้อมูลในทั้งสองระบบ

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>เมื่อสร้างชุดการเชื่อมต่อของฉัน ฉันไม่เห็นการเชื่อมต่อในรายการแบบหล่นลงของ Connection ฉันควรทำอย่างไร

ตรวจสอบว่าขณะที่สร้างการเชื่อมต่อของคุณ คุณเลือก Dynamics 365 Finance และ Dataverse

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>เมื่อซิงค์การจ้างงาน ฉันได้รับข้อผิดพลาด "ไม่มี CompanyInfo_FK"หรือ "ไม่พบค่า '12/31/2154 11:59:59 pm' ในฟิลด์ 'วันที่สิ้นสุดการจ้างงาน' ในตารางที่เกี่ยวข้อง 'การจ้างงาน'" ฉันควรทำอย่างไร

ให้แน่ใจว่าคุณกำลังแม็ปกับนิติบุคคลที่ถูกต้อง การซิงค์นิติบุคคลไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น จึงคาดว่าแต่ละนิติบุคคลที่ปรากฏใน Human Resources และ Dataverse มีอยู่ใน Finance เช่นกัน
นอกจากนี้ ให้ตรวจสอบให้แน่ใจว่าคุณกำลังเลือกนิติบุคคลที่ถูกต้องสำหรับชุดการเชื่อมต่อที่มีการเชื่อมโยง

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>หลังจากการตั้งค่าโครงการของฉัน การแม็ปฟิลด์สำหรับ Finance จะกลายเป็นว่างเปล่า ฉันควรทำอย่างไร

รีเฟรชเอนทิตีข้อมูลใน Finance โดยไปที่ **การจัดการข้อมูล \> พารามิเตอร์กรอบงาน \> การตั้งค่าเอนทิตี \> รีเฟรชรายการเอนทิตี** ซึ่งควรใช้เวลาสองสามนาทีในการทำให้เสร็จสมบูรณ์ จากนั้นคุณควรเห็นแมปเหล่านั้น ปัญหานี้เกิดขึ้นเมื่อมีการสร้างโครงการใหม่

![ไม่มีการแม็ปฟิลด์](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

- ตัวรวมข้อมูล (DI): 

  - [รวมข้อมูลลงใน Microsoft Dataverse](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [การจัดการข้อผิดพลาดตัวรวมข้อมูลและการแก้ไขปัญหาเบื้องต้น](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [การตอบสนองคำขอ DSR สำหรับล็อกที่ระบบสร้างขึ้นใน Power Apps Microsoft Power Automate และ Dataverse](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- การจัดการข้อมูล:

  - [การจัดการข้อมูล](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
