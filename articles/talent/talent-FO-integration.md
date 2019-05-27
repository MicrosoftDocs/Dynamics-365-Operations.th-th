---
title: FAQ เกี่ยวกับการรวม Dynamics 365 for Talent ไปยัง Dynamics 365 for Finance and Operations
description: หัวข้อนี้อธิบายว่าข้อมูลใดจะถูกซิงโครไนส์ในการรวม Talent และ Finance and Operations
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 438c2b5689e450b9aae9c55168993f2ee84be4d5
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519263"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>FAQ เกี่ยวกับการรวม Dynamics 365 for Talent ไปยัง Dynamics 365 for Finance and Operations

[!include [banner](includes/banner.md)]

หัวข้อนี้ตอบคำถามสำหรับคำถามทั่วไปที่เกี่ยวข้องเกี่ยวกับว่าข้อมูลใดจะถูกซิงโครไนส์เมื่อ Dynamics 365 for Talent ถูกรวมกับ Dynamics 365 for Finance and Operations

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>คือข้อมูลที่ซิงโครไนซ์ทั้งหมด หรือเพียงแค่เอนทิตีข้อมูล

ด้วยทรัพยากรบุคคลหลัก (ทรัพยากรบุคคล) ชุดย่อยของข้อมูลจะมีการซิงโครไนส์ สำหรับรายการของเอนทิตี้ทั้งหมด ดู [การรวมจาก Dynamics 365 for Talent ไปยัง Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md)

สำหรับ Attract และ Onboard ข้อมูลทั้งหมดเป็นข้อมูลหลักของ Common Data Service

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>ฉันสามารถสร้างการแม็ปใหม่โดยไม่ใช้เท็มเพลได้หรือไม่

เท็มเพลตเป็นจุดเริ่มต้น คุณสามารถสร้างเท็มเพลตของคุณเอง แต่จำเป็นต้องใช้เท็มเพลเสมอเมื่อสร้างโครงการการรวม สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวรวมข้อมูล (DI) เท็มเพลต และโครงการ ดูที่ [รวมข้อมูลลงใน Common Data Service](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>ฉันสามารถแม็ปมิติทางการเงินที่จะโอนย้ายระหว่าง Talent และ Finance and Operations ได้หรือไม่

ในปัจจุบันมิติทางการเงินไม่ได้อยู่ใน Common Data Service สำหรับแอป และผลลัพธ์ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น เอนทิตี้นี้มีการวางแผน แต่ไม่มีเส้นเวลาการนำออกใช้ที่พร้อมใช้งานอยู่ในปัจจุบัน

สำหรับข้อมูลที่อยู่ใน Finance and Operations แต่ไม่มีอยู่ใน Talent ให้เชื่อมโยงสองระบบเข้าด้วยกันโดยใช้ **ตั้งค่าคอนฟิกลิงค์** ใน Talent สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกการเชื่อมโยงระหว่าง Talent และ Finance and Operations ดูที่ [มีอะไรใหม่หรือมีการเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (31 ตุลาคม 2018)](whats-new-talent-october-31.md)

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>ในบางครั้งเมื่อฉันนำเข้าพนักงาน รายการจะไปอยู่ที่พนักงานที่ไม่ได้ใช้งานใน Finance and Operations เพราะเหตุใด?

คุณอาจได้รับข้อผิดพลาดนี้ถ้าพนักงานไม่มีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่ใน Talent เมื่อต้องการแก้ไขปัญหานี้ ไปที่ **การจัดการบุคลากร \> พนักงาน \> ประวัติการจ้างงาน \> ตัวจัดการวันที่** และตรวจสอบว่ามีเรกคอร์ดที่มีรายละเอียดการจ้างงานที่ใช้งานอยู่หรือไม่

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>ถ้าฉันเลือกที่จะแม็ปเฉพาะชุดย่อยของฟิลด์ การเปลี่ยนแปลงของฟิลด์ที่ไม่ได้แม็ปจะทริกเกอร์การซิงค์หรือไม่

ซิงค์ข้อมูลเป็นไปตามกำหนดการดำเนินการ การรวมจะเบิกสินค้าเรกคอร์ดถ้าฟิลด์ใดๆ ในเรกคอร์ดเปลี่ยนแปลง โดยไม่คำนึงถึงว่าฟิลด์ดังกล่าวเป็นส่วนหนึ่งของการแม็ปการรวม

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>ฉันจะส่งการเปลี่ยนแปลงของพนักงานที่ใช้งานอยู่เท่านั้น ไม่ใช่เรกคอร์ดที่สิ้นสุดการจ้างงานได้อย่างไร

ด้วยการใช้ "การสอบถามขั้นสูง" คุณสามารถกรองและปรับรูปร่างแหล่งข้อมูลก่อนที่จะส่งผ่านไปยังปลายทาง

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>ฉันสามารถระบุฟิลด์ที่จะส่งไปยัง Finance and Operations สำหรับเอนทิตี้ที่เฉพาะเจาะจงได้หรือไม่

คุณสามารถเพิ่มหรือลบฟิลด์ออกจากงานรวม ไม่ใช่ฟิลด์ข้อมูลทั้งหมดที่มีอยู่ในเอนทิตี้ Common Data Service ที่จะถูกเติมข้อมูลจาก Core HR
คุณสามารถเติมข้อมูลเพิ่มเติมได้ผ่าน PowerApps

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>ฉันตั้งค่าการรวมเป็นชุดงาน แต่ Talent สูญเสียการเชื่อมต่อไปกับระบบปลายทาง ฉันจะส่งชุดการเปลี่ยนแปลงเดียวกันไปยังระบบปลายทางได้อย่างไร

ไม่จำเป็นต้องมีการตั้งค่าพิเศษสำหรับการจัดการข้อยกเว้น ตัวรวมข้อมูลจะตรวจจับและรายงานข้อผิดพลาดที่เกิดขึ้นที่ต้นทางและปลายทางโดยอัตโนมัติ และจะอนุญาตให้ลองใหม่ด้วยตนเอง อย่างไรก็ตาม คุณไม่สามารถแก้ไขข้อมูลด้วยตนเองได้ ถ้าจำเป็นต้องปรับปรุงข้อมูล ควรทำที่ต้นทางหรือปลายทางอย่างใดอย่างหนึ่ง

## <a name="can-i-set-up-bi-directional-integration"></a>ฉันสามารถตั้งค่าการรวมสองทิศทางได้หรือไม่

ไม่ได้ การรวมเป็นแบบทิศทางเดียวในขณะนี้ (Talent ไปยัง Finance and Operations) อย่างไรก็ตาม มีเท็มเพลตเริ่มต้นที่มีอยู่เพื่อส่งข้อมูลจาก Talent ไปยัง Finance and Operations

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>ฉันจะอนุญาตให้ลบเรกคอร์ดโดยเป็นส่วนหนึ่งของการรวมของฉันได้หรือไม่

ไม่ได้ ตัวรวมข้อมูลจะไม่รวบรวมเรกคอร์ดที่ถูกลบสำหรับการโอนย้ายข้อมูล มีเฉพาะการสร้างข้อมูลและการปรับปรุง (UPSERT) ถูกรวมอยู่ในขณะนี้

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>ฉันสามารถเรียกใช้การดำเนินการที่มีข้อผิดพลาดได้หรือไม่ ถ้าเป็นเช่นนั้น จะส่งไฟล์ทั้งหมดหรือเฉพาะที่มีการเปลี่ยนแปลง

การเรียกใช้ครั้งแรกของตัวรวมข้อมูลจะรันแบบเต็มเสมอ การเรียกใช้ในเวลาต่อมาขึ้นอยู่กับการติดตามการเปลี่ยนแปลง เมื่อดำเนินการการรันข้อผิดพลาด จะแยกเรกคอร์ดในขอบเขตของการรัน และส่งการเปลี่ยนแปลงล่าสุดจาก Common Data Service

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>เมื่อฉันบันทึกโครงการ ฉันได้รับข้อผิดพลาด: "โครงการมีข้อผิดพลาดในการแม็ป" ฉันควรทำอย่างไร

ตรวจสอบการตั้งค่าของคีย์รวมของคุณ ทำการเปลี่ยนแปลงที่จำเป็นเพื่อตั้งค่า แล้วรีเฟรชเอนทิตี้ในโครงการ

เมื่อมีการใช้เท็มเพลตเริ่มต้น คีย์รวมจะถูกนำเข้าโดยอัตโนมัติ ปัญหานี้อาจเกิดขึ้นเมื่อมีการเพิ่มงานใหม่ไปยังเท็มเพลตที่มีอยู่

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>ถ้าฉันมีนิติบุคคลซึ่งเป็นพนักงานที่มีการจ้างงานจำนวน N ราย ฉันต้องสร้างการแม็ปสำหรับแต่ละคนหรือไม่

ใช่ สำหรับแต่ละนิติบุคคลใน Finance and Operations คุณจำเป็นต้องมีโครงการรวมที่แยกต่างหากในการรวมข้อมูล

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>ฉันต้องการถ่ายโอนข้อมูลที่ไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้นที่จัดเตรียมให้โดย Microsoft ฉันสามารถทำได้หรือไม่

ได้ คุณสามารถเพิ่มหรือลบฟิลด์ออกจากเท็มเพลตที่มีอยู่ คุณสามารถปรับเปลี่ยนเท็มเพลตเพื่อรวมข้อมูลเพิ่มเติมจาก Common Data Service อื่น ๆ สำหรับเอนทิตีแอป เอนทิตีต้องอยู่ใน Common Data Service สำหรับแอปเพื่อให้รวมอยู่ในเท็มเพลต 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>ฉันเพิ่งสร้างสภาพแวดล้อม Finance and Operations และ Talent ใหม่ และฉันได้รับข้อผิดพลาด "ค่าข้อมูลละเมิดข้อจำกัดความถูกต้อง" เพราะเหตุใด?

สาเหตุของข้อผิดพลาดนี้อาจรวม:

- การโอนย้ายข้อมูลที่เป็นผลลัพธ์ในเรกคอร์ดที่ซ้ำกันในการแยกข้อมูลลที่ต้นทาง (Common Data Service)

- การโอนย้ายข้อมูลมีค่า null สำหรับฟิลด์ที่จำเป็นใน Finance and Operations ตรวจสอบข้อมูลที่อยู่ใน Common Data Service และตรงตามข้อกำหนดของ Finance and Operations

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>ถ้ามีข้อผิดพลาดการดำเนินการ และรหัสพนักงานยังไม่ได้ซิงค์ ฉันจะค้นหาประวัติงานที่มีเรกคอร์ดพนักงานที่ล้มเหลวได้อย่างไร

ตัวรวมข้อมูลจะสร้างหลายโครงการใน Finance and Operations ความสัมพันธ์ระหว่างงานตัวรวมข้อมูลและโครงการ Finance and Operations คือหนึ่งต่อหนึ่ง

ติดตามเวลาจากประวัติการดำเนินการตัวรวมข้อมูลและค้นหาโครงการดัชนี -1 ใน Finance and Operations ถ้าหมายเลขงานคือ 9 ในตัวรวมข้อมูล ดัชนีใน Finance and Operations คือ 8

1. จัดดัชนีงานจากตัวรวมข้อมูล (ในตัวอย่างนี้คือ "9")

![จับดัชนีงานจากตัวรวมข้อมูล](media/CaptureTaskIndex.png)

2. ติดตามเวลาการดำเนินการของโครงการ

![ติดตามเวลาการดำเนินการของโครงการ](media/CaptureTimeOfExecution.png)

3. ใน Finance and Operations ระบุดัชนี - 1 ในตัวอย่างนี้ โครงการที่มีคำเสริมท้ายเป็น "8" และเวลาการดำเนินการของดัชนีเป็น "0" โครงการจะสอดคล้องกับเวลาการดำเนินการในขั้นตอนที่ 2

![ระบุดัชนี](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>หลังจากการรวม Talent และ Finance and Operations ฉันไม่เห็นข้อมูล Talent ของฉันใน Finance and Operations ฉันควรทำอย่างไร

การรวมกับ Finance and Operations มีสองขั้นตอน ก่อนอื่น ตรวจสอบว่ ข้อมูล Talent ถูกปรับปรุงแล้ว และพร้อมใช้งานใน Common Data Service นี่เป็นการซิงค์แบบเรียลไทม์แบบใกล้ และสามารถตรวจสอบใน PowerApps โดยดูข้อมูลภายในเอนทิตีข้อมูล

![ข้อมูลใน Common Data Service](media/DataInCDS.png)

ถ้าข้อมูลไม่ปรากฏตามที่คาดไว้ใน Common Data Service ให้ตรวจสอบว่าเอนทิตีได้รับการสนับสนุนในการรวม เพื่อรวมข้อมูลเพิ่มเติมใน Common Data Service จะต้องทำการเปลี่ยนแปลงทางฝั่ง Microsoft

ถ้าเอนทิตีได้รับการสนับสนุน และข้อมูลมีอยู่ใน Common Data Service ให้ตรวจสอบว่าการแม็ปถูกต้องในตัวรวมข้อมูล ถ้าการค้นหาการแม็ปตัวรวมเป็นปกติ ให้ตรวจสอบมีการรันงานการจัดการข้อมูลเสร็จเรียบร้อยแล้ว ข้อผิดพลาดอาจเกิดขึ้นในระหว่างการดำเนินการชุดงาน สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการข้อมูล ดู [การจัดการข้อมูล](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>ที่อยู่สำหรับพนักงานของฉันไม่ถูกต้องหลังจากที่ฉันนำเข้าไปยัง Finance and Operations ฉันควรทำอย่างไร

ลำดับหมายเลขสำหรับ **รหัสที่ตั้ง** ใช้รูปแบบเดียวกันในทั้ง Talent และ Finance and Operations ลำดับหมายเลขต้องไม่ซ้ำกันทั้งสองด้าน เพื่อให้ไม่มีการชนกันของที่อยู่เมื่อรวมข้อมูลจาก Common Data Service ไปยัง Finance and Operations

ในระหว่างการใช้งานของ Talent ให้ตรวจสอบว่าลำดับหมายเลขไม่เหมือนกันใน Talent และ Finance and Operations ตรวจสอบว่าลำดับหมายเลขทั้งหมดไม่เหมือนกันซึ่งอาจจะรักษาข้อมูลในทั้งสองระบบ

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>เมื่อสร้างชุดการเชื่อมต่อของฉัน ฉันไม่เห็นการเชื่อมต่อในรายการแบบหล่นลงของ Connection ฉันควรทำอย่างไร

ตรวจสอบว่าขณะที่สร้างการเชื่อมต่อของคุณ ให้เลือก Dynamics 365 for Finance and Operations (อยู่ในการแสดงตัวอย่าง) และ Common Data Service

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>เมื่อซิงค์การจ้างงาน ฉันได้รับข้อผิดพลาด "ไม่มี CompanyInfo_FK"หรือ "ไม่พบค่า '12/31/2154 11:59:59 pm' ในฟิลด์ 'วันที่สิ้นสุดการจ้างงาน' ในตารางที่เกี่ยวข้อง 'การจ้างงาน'" ฉันควรทำอย่างไร

ให้แน่ใจว่าคุณกำลังแม็ปกับนิติบุคคลที่ถูกต้อง การซิงค์นิติบุคคลไม่ใช่ส่วนหนึ่งของเท็มเพลตเริ่มต้น จึงคาดว่าแต่ละนิติบุคคลที่ปรากฏใน Talent และ Common Data Service มีอยู่ใน Finance and Operations เช่นกัน
นอกจากนี้ ให้ตรวจสอบให้แน่ใจว่าคุณกำลังเลือกนิติบุคคลที่ถูกต้องสำหรับชุดการเชื่อมต่อที่มีการเชื่อมโยง

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>หลังจากการตั้งค่าโครงการของฉัน การแม็ปฟิลด์สำหรับ Finance and Operations จะกลายเป็นว่างเปล่า ฉันควรทำอย่างไร

รีเฟรชเอนทิตี้ข้อมูลใน Finance and Operations โดยไปที่ **การจัดการข้อมูล \> พารามิเตอร์กรอบงาน \> การตั้งค่าเอนทิตี้ \> รีเฟรชรายการเอนทิตี้** ซึ่งควรใช้เวลาสองสามนาทีในการทำให้เสร็จสมบูรณ์ จากนั้นคุณควรเห็นแมปเหล่านั้น ปัญหานี้เกิดขึ้นเมื่อมีการสร้างโครงการใหม่

![ไม่มีการแม็ปฟิลด์](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

- ตัวรวมข้อมูล (DI): 

  - [รวมข้อมูลลงใน Common Data Service](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [การจัดการข้อผิดพลาดตัวรวมข้อมูลและการแก้ไขปัญหาเบื้องต้น](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [การตอบสนองคำขอ DSR สำหรับล็อกที่ระบบสร้างขึ้นใน PowerApps, Microsoft Flow และ Common Data Service](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- การจัดการข้อมูล:

  - [การจัดการข้อมูล](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
