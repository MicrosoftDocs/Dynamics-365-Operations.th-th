---
title: วางแผนลำดับชั้นขององค์กรของคุณ
description: ก่อนที่คุณตั้งค่าองค์กรและลำดับชั้นขององค์กร ตรวจสอบให้แน่ใจว่าคุณเข้าใจวิธีการสร้างแบบจำลองธุรกิจของคุณที่ดีที่สุด
author: sericks007
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bb0b306cca715cad64d62fff843987a8e98eb99
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108778"
---
# <a name="plan-your-organizational-hierarchy"></a>วางแผนลำดับชั้นขององค์กรของคุณ

[!include [banner](../includes/banner.md)]

ก่อนที่คุณตั้งค่าองค์กรและลำดับชั้นขององค์กร ตรวจสอบให้แน่ใจว่า คุณวางแผนว่าจะสร้างแบบจำลองธุรกิจของคุณอย่างไร รูปแบบองค์กรมีผลกระทบที่สำคัญต่อการใช้งานและกระบวนการทางธุรกิจ

ลำดับชั้นขององค์กรแสดงความสัมพันธ์ระหว่างองค์กรที่ประกอบกันเป็นธุรกิจ ดังนั้น การพิจารณาที่สำคัญที่สุดเมื่อคุณจำลององค์กรคือโครงสร้างของธุรกิจของคุณ เราขอแนะนำให้ คุณกำหนดโครงสร้างองค์กรที่ยึดตามคำติชมจากผู้บริหารและผู้จัดการอาวุโสจากขอบเขตหน้าที่ เช่นทางการเงินและการบัญชี ทรัพยากรบุคคล การดำเนินงาน การซื้อ และการขาย และการตลาด

เมื่อคุณกำลังวางแผนลำดับชั้น จะยังควรพิจารณาความสัมพันธ์ระหว่างลำดับชั้นขององค์กรและมิติทางการเงิน คุณสามารถตั้งค่าลำดับชั้นขององค์กรหลายรายการเพื่อแสดงมุมมองต่าง ๆ ของธุรกิจของคุณ โดยการใช้มิติทางการเงิน คุณสามารถสร้างรายงานที่ยึดตามมุมมองเหล่านี้ ทำงานกับคู่ค้าของคุณเพื่อสร้างลำดับชั้นที่ระบุทั้งความต้องการขององค์กรและการรายงานทางกฎหมาย

> [!NOTE]
> ถึงแม้ว่าคุณสามารถใช้มิติทางการเงินเพื่อแสดงถึงนิติบุคคลโดยไม่ได้สร้างนิติบุคคล มิติทางการเงินไม่ได้รับการออกแบบให้ระบุความต้องการทางธุรกิจหรือที่เกี่ยวกับการดำเนินงานของนิติบุคคล ฟังก์ชันการลงบัญชีระหว่างหน่วยถูกออกแบบให้ระบุได้เฉพาะรายการบัญชีที่สร้างขึ้นโดยธุรกรรมแต่ละครั้ง

> [!IMPORTANT]
> คุณไม่ควรกำหนดวิธีการจำลององค์กรที่ยึดตามข้อมูลในบทความนี้เท่านั้น เอกสารนี้มีคำแนะนำ คุณสามารถทำงานกับคู่ค้าของคุณสำหรับคำแนะนำเพิ่มเติมได้ คู่ค้าของคุณได้รับประสบการณ์ในอุตสาหกรรมต่างๆ และข้ามฐานลูกค้า

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>ตัดสินใจได้ว่าแบบจำลององค์กรภายในเป็นนิติบุคคลหรือหน่วยปฏิบัติงาน

คุณต้องมีนิติบุคคลอย่างน้อยหนึ่งรายการเพื่อแสดงถึงธุรกิจของคุณ นิติบุคคลสามารถป้อนสัญญาทางกฎหมาย และจำเป็นต้องใช้เพื่อจัดเตรียมงบการเงินที่รายงานเกี่ยวกับประสิทธิภาพ

นิติบุคคลสามารถใช้สำหรับธุรกรรมทางธุรกิจหรือสำหรับการรวมได้ ซึ่งหมายความว่านิติบุคคลในการเงินและการดำเนินงาน ไม่จำเป็นต้องแสดงถึงเอนทิตี้ที่แท้จริงในธุรกิจของคุณ ตัวอย่างเช่น บริษัทที่เข้าร่วมในธุรกรรมสามารถมีนิติบุคคลบริษัทในเครือ ในสถานการณ์นี้ นิติบุคคลที่จำเป็นสำหรับธุรกรรม และนิติบุคคลเสมือนจำเป็นต้องรวมผลลัพธ์และยอดดุลของบริษัทในเครือนิติบุคคล

องค์กรภายในในธุรกิจของคุณ เช่น สำนักงานส่วนภูมิภาค สามารถแสดงเป็นนิติบุคคลเพิ่มเติม หรือหน่วยปฏิบัติงานของนิติบุคคลหลัก หน่วยปฏิบัติงานไม่จำเป็นต้องเป็นองค์กรที่กำหนดตามกฎหมาย หน่วยปฏิบัติงานจะใช้ในการควบคุมทรัพยากรทางเศรษฐกิจและกระบวนการในการดำเนินงานในธุรกิจ ตัวอย่างเช่น แผนกและศูนย์ต้นทุนเป็นหน่วยปฏิบัติงาน

บางฟังก์ชันทำงานแตกต่างกันขึ้นอยู่กับว่าองค์กรเป็นนิติบุคคลหรือหน่วยปฏิบัติงาน พิจารณาฟังก์ชันที่อธิบายไว้ด้านล่างอย่างรอบคอบเมื่อคุณทำการตัดสินใจ

### <a name="master-data"></a>ข้อมูลหลัก

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

ต้องตั้งค่าข้อมูลหลัก เช่น ลูกค้า เงื่อนไขการชำระเงิน หน่วยงานจัดเก็บภาษี และการสั่งซื้อสินค้าคงคลังเฉพาะไซต์สำหรับแต่ละนิติบุคคล ข้อมูลหลัก เช่น ผู้ใช้ ผลิตภัณฑ์ และข้อมูลทรัพยากรบุคคลส่วนใหญ่ จะใช้ร่วมกันระหว่างนิติบุคคลทั้งหมด

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

ข้อมูลหลักที่จะใช้ร่วมกันระหว่างหน่วยปฏิบัติงาน

### <a name="module-parameters"></a>พารามิเตอร์โมดูล

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

ต้องตั้งค่าพารามิเตอร์สำหรับโมดูล เช่น พารามิเตอร์บัญชีลูกหนี้ พารามิเตอร์บัญชีเจ้าหนี้ และพารามิเตอร์การจัดการเงินสดและธนาคาร ต่อนิติบุคคล เนื่องจากโมดูลที่มีการตั้งค่าสำหรับนิติบุคคลแยกต่างหาก แต่ละบริษัทในเครือสามารถเป็นไปตามข้อกำหนดตามกฎหมายท้องถิ่นและแนวทางปฏิบัติทางธุรกิจ ตัวอย่างเช่น ผู้เชี่ยวชาญด้านการบริการนิติบุคคล และนิติบุคคลของการผลิตสามารถมีพารามิเตอร์โมดูลแตกต่างกันถึงแม้ว่าจะรายงานไปยังบริษัทแม่เดียวกัน

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

พารามิเตอร์โมดูลที่มีการใช้ร่วมกันระหว่างหน่วยปฏิบัติงาน

### <a name="data-security"></a>ความปลอดภัยของข้อมูล

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

ข้อมูลส่วนใหญ่มีความปลอดภัยโดยอัตโนมัติตามรหัสบริษัท รหัสบริษัทเป็นตัวระบุเฉพาะสำหรับข้อมูลที่สัมพันธ์กับนิติบุคคล บริษัทสามารถเชื่อมโยงกับนิติบุคคลเดียวเท่านั้น และนิติบุคคลสามารถเชื่อมโยงกับบริษัทแห่งเดียวเท่านั้น ผู้ใช้สามารถเข้าถึงข้อมูลเฉพาะสำหรับบริษัทที่มีสิทธิ์การเข้าถึง คุณไม่จำเป็นต้องกำหนดให้รักษาความปลอดภัยข้อมูลตามรหัสบริษัท

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

ข้อมูลจะรักษาไว้สำหรับแต่ละหน่วยปฏิบัติงาน โดยการสร้างนโยบายความปลอดภัยของข้อมูลที่กำหนดเอง นโยบายความปลอดภัยข้อมูลจะใช้ในการจำกัดการเข้าถึงข้อมูล ตัวอย่างเช่น สมมติว่าผู้ใช้สามารถสร้างใบสั่งซื้อในหน่วยปฏิบัติงานเท่านั้น คุณสามารถสร้างนโยบายความปลอดภัยเพื่อป้องกันไม่ให้ผู้ใช้เข้าถึงข้อมูลใบสั่งซื้อจากหน่วยปฏิบัติงานอื่น ๆ ปริมาตรของธุรกรรมและจำนวนของนโยบายความปลอดภัยอาจมีผลต่อประสิทธิภาพการทำงาน เมื่อคุณออกแบบนโยบายความปลอดภัย ให้ระลึกถึงประสิทธิภาพการทำงาน

### <a name="ledgers"></a>บัญชีแยกประเภท

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

แต่ละนิติบุคคลต้องมีบัญชีแยกประเภทที่แสดงผังบัญชี สกุลเงินทางบัญชี สกุลเงินการรายงาน และปฏิทินทางการเงิน งบดุลสามารถสร้างเฉพาะสำหรับนิติบุคคล สามารถใช้บัญชีหลัก มิติข้อมูล โครงสร้างทางบัญชี ผังบัญชี และกฎทางบัญชีจากนิติบุคคลมากกว่าหนึ่งรายการ

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

หน่วยปฏิบัติงานไม่สามารถมีข้อมูลบัญชีแยกประเภทของตนเอง ถ้าองค์กรภายในของคุณไม่ได้กำหนดบัญชีแยกประเภทเฉพาะ คุณสามารถจำลองบัญชีเหล่านั้นเป็นหน่วยปฏิบัติงาน จะตั้งค่าข้อมูลบัญชีแยกประเภทสำหรับนิติบุคคลหลักในลำดับชั้น คุณสามารถสร้างงบกำไรขาดทุนสำหรับหน่วยปฏิบัติงานในนิติบุคคล หรือสำหรับนิติบุคคลหลัก

### <a name="fiscal-calendars"></a>ปฏิทินทางการเงิน

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

แต่ละนิติบุคคลมีปฏิทินทางการเงินของตนเอง ถ้าองค์กรภายในของคุณใช้ปีบัญชีและปฏิทินทางการเงินที่แตกต่างกัน คุณต้องจำลององค์กรเป็นนิติบุคคล

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

หน่วยปฏิบัติงานต้องใช้ปฏิทินทางการเงินร่วมกัน ถ้าองค์กรภายในของคุณสามารถใช้ปีบัญชีและปฏิทินทางการเงินเดียวกัน คุณสามารถจำลององค์กรเป็นหน่วยปฏิบัติงาน

### <a name="consolidation"></a>การรวมบัญชี

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

คุณต้องรวมผลลัพธ์ทางการเงินสำหรับสำนักงานส่วนภูมิภาคไว้ในบริษัทรวมบริษัทเดียวเพื่อจัดเตรียมงบการเงิน

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

ไม่จำเป็นต้องรวม เนื่องจากข้อมูลถูกใช้ร่วมกันระหว่างหน่วยปฏิบัติงานอยู่แล้ว

### <a name="centralized-payments"></a>การชำระเงินส่วนกลาง

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

ต้องตั้งค่าการชำระเงินส่วนกลางเพื่อให้สามารถชำระใบแจ้งหนี้สำหรับนิติบุคคลย่อยทั้งหมดหรือจากนิติบุคคลหลักเดียว

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

การชำระเงินส่วนกลางไม่จำเป็นเนื่องจากใบแจ้งหนี้ทั้งหมดจะถูกบันทึกไว้ในนิติบุคคลเดียวกัน

### <a name="intercompany-transactions"></a>ธุรกรรมระหว่างบริษัท

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

สามารถใช้ใบสั่งขายระหว่างบริษัท ใบสั่งซื้อ การชำระเงิน หรือใบเสร็จซึ่งกันและกันได้ คุณไม่จำเป็นต้องใช้ใบสำคัญสมุดรายวัน คุณสามารถดูธุรกรรมระหว่างบริษัทในระดับบัญชีแยกประเภทย่อย (บัญชีลูกหนี้ บัญชีเจ้าหนี้) ตัวอย่างต่อไปนี้แสดงให้เห็นถึงวิธีจัดการธุรกรรมระหว่างบริษัท

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>ตัวอย่างที่ 1: ศูนย์ควบคุมให้บริการไปยังสำนักงานส่วนภูมิภาค และต้องคิดค่าใช้จ่ายของบริการเหล่านั้นกับสำนักงานส่วนภูมิภาค

ถ้าคุณจำลองสำนักงานส่วนภูมิภาคเป็นนิติบุคคล คุณมีตัวเลือกต่อไปนี้:

- ศูนย์ควบคุมสร้างรายการสมุดรายวันเพื่อคิดค่าบริการข้ามสำนักงานส่วนภูมิภาคสำหรับค่าใช้จ่าย ไม่สามารถกำหนดอายุธุรกรรม
- ศูนย์ควบคุมส่งใบสั่งซื้อสำหรับบริการไปยังสำนักงานส่วนภูมิภาค ใบสั่งขายถูกสร้างขึ้นโดยอัตโนมัติในนิติบุคคลสำหรับสำนักงานส่วนภูมิภาค กับธุรกรรมบัญชีแยกประเภทย่อยระหว่างบริษัท

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>ตัวอย่างที่ 2: ศูนย์ควบคุมจัดซื้อและชำระค่าบริการที่ส่งไปยังสำนักงานส่วนภูมิภาค

ถ้าคุณจำลองสำนักงานส่วนภูมิภาคเป็นนิติบุคคล คุณมีตัวเลือกต่อไปนี้:

- ใบแจ้งหนี้และการชำระเงินเป็นไปตามข้อบังคับของศูนย์ควบคุม ศูนย์ควบคุมสามารถสร้างรายการสมุดรายวันเพื่อคิดค่าบริการข้ามสำนักงานส่วนภูมิภาคสำหรับค่าใช้จ่าย ไม่สามารถกำหนดอายุธุรกรรม
- ใบแจ้งหนี้และการชำระเงินเป็นไปตามข้อบังคับของศูนย์ควบคุม ศูนย์ควบคุมสามารถสร้างธุรกรรมบัญชีแยกประเภทย่อยระหว่างบริษัทได้

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

ธุรกรรมระหว่างบริษัทระหว่างหน่วยปฏิบัติงานได้รับการสนับสนุนโดยใช้ใบสำคัญสมุดรายวันเท่านั้น หน่วยปฏิบัติงานไม่สามารถออก หรือได้รับใบสั่งซื้อ ใบสั่งขาย หรือใบแจ้งหนี้จากหน่วยปฏิบัติงานอื่นในนิติบุคคลเดียวกัน คุณไม่สามารถดูธุรกรรมระหว่างบริษัทในระดับบัญชีแยกประเภทย่อย (บัญชีลูกหนี้ บัญชีเจ้าหนี้) ตัวอย่างต่อไปนี้แสดงให้เห็นถึงวิธีจัดการธุรกรรมระหว่างบริษัท

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>ตัวอย่างที่ 1: ศูนย์ควบคุมให้บริการไปยังสำนักงานส่วนภูมิภาค และต้องคิดค่าใช้จ่ายของบริการเหล่านั้นกับสำนักงานส่วนภูมิภาค

ถ้าคุณจำลองสำนักงานส่วนภูมิภาคเป็นหน่วยปฏิบัติงาน ศูนย์ควบคุมจะป้อนธุรกรรมค่าใช้จ่ายและกำหนดรหัสไปยังสำนักงานส่วนภูมิภาค

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>ตัวอย่างที่ 2: ศูนย์ควบคุมจัดซื้อและชำระค่าบริการที่ส่งไปยังสำนักงานส่วนภูมิภาค

ถ้าคุณจำลองสำนักงานส่วนภูมิภาคเป็นหน่วยปฏิบัติงาน ใบแจ้งหนี้และการชำระเงินจะเป็นไปตามข้อบังคับของศูนย์ควบคุม ใบแจ้งหนี้สามารถกำหนดรหัสไปยังสำนักงานส่วนภูมิภาค ในงบกำไรขาดทุน ใช้มิติทางการเงินยอดดุลต้นทุนเพื่อรายงานค่าใช้จ่ายสำหรับสำนักงานส่วนภูมิภาค

### <a name="local-tax-requirements"></a>ข้อกำหนดภาษีท้องถิ่น

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

นิติบุคคลต้องอยู่ภายใต้กฎหมายภาษีของหน่วยงานจัดเก็บภาษีในประเทศ/ภูมิภาคที่มีการลงทะเบียนนิติบุคคล ตัวอย่างเช่น นิติบุคคลที่ลงทะเบียนในเดนมาร์กต้องอยู่ภายใต้กฎหมายและข้อบังคับด้านภาษีของเดนมาร์ก นิติบุคคลสามารถอยู่ในประเทศ/ภูมิภาคเดียวเท่านั้น ประเทศ/ภูมิภาคที่คุณเลือกสำหรับที่อยู่หลักของนิติบุคคลจะควบคุมคุณลักษณะเฉพาะประเทศ/ภูมิภาคที่สามารถใช้ได้สำหรับนิติบุคคลนั้น ตัวอย่างเช่น ถ้าที่อยู่หลักของนิติบุคคลอยู่ในเดนมาร์ก คุณลักษณะที่เกี่ยวข้องกับกฎหมายและข้อบังคับด้านภาษีของเดนมาร์กจะสามารถใช้ได้ ดังนั้น ถ้าองค์กรของคุณอยู่ในประเทศ/ภูมิภาคที่แตกต่างกัน และต้องการตัวเลือกภาษีท้องถิ่นอื่น คุณต้องตั้งค่าองค์กรเป็นนิติบุคคลแยกต่างหาก

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

หน่วยปฏิบัติงานใช้บริบทประเทศของนิติบุคคลหลัก หน่วยปฏิบัติงานในนิติบุคคลเดียวกันไม่สามารถมีข้อกำหนดเฉพาะประเทศ/ภูมิภาคอื่น ถ้าองค์กรของคุณอยู่ในประเทศ/ภูมิภาคเดียวกัน และใช้ตัวเลือกภาษีเดียวกัน คุณสามารถตั้งค่าเป็นหน่วยปฏิบัติงาน

### <a name="statutory-reporting-for-a-countryregion"></a>การรายงานตามกฎหมายสำหรับประเทศ/ภูมิภาค

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

สำหรับประเทศ/ภูมิภาคที่ถูกสนับสนุน รายงานตามกฎหมายส่วนใหญ่สามารถสร้างได้ 

> [!NOTE]
> ชั้นของการลงรายการบัญชีในบัญชีแยกประเภททั่วไปช่วยให้คุณสามารถทำการปรับปรุงรายการสำหรับบริษัทแม่ที่ใช้มาตรฐานการบัญชีที่แตกต่างจากบริษัทลูก ตัวอย่างเช่น สำหรับบริษัทที่ใช้แนวทางการบัญชีที่เป็นที่ยอมรับโดยทั่วไปในสหราชอาณาจักร (UK GAAP) คุณสามารถทำการเปลี่ยนแปลงรายการในชั้นของการลงรายการบัญชี สามารถรวมรายการเหล่านี้ลงในบริษัทแม่ที่ใช้หลักการบัญชีที่เป็นที่ยอมรับโดยทั่วไป (GAAP) ในสหรัฐอเมริกา รายการที่ปรับเปลี่ยนจะไม่ส่งผลกระทบต่อการรายงาน UK GAAP

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

ต้องสร้างรายงานตามกฎหมายโดยใช้แอพลิเคชันอื่น คุณต้องแน่ใจว่ามีการรวบรวมข้อมูลในแอปการเงินและการดำเนินงาน เพื่อสนับสนุนความต้องการของแต่ละหน่วยปฏิบัติงาน ซึ่งจะแตกต่างจากความต้องการของศูนย์ควบคุม

### <a name="currency"></a>สกุลเงิน

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

ถ้าองค์กรของคุณต้องใช้สกุลเงินหลักอื่นๆ คุณต้องจำลององค์กรเป็นนิติบุคคล สกุลเงินหลักจะตั้งค่าตามนิติบุคคล อย่างไรก็ตาม คุณสามารถป้อนธุรกรรมได้ในหลายสกุลเงิน

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

ถ้าองค์กรของคุณสามารถใช้สกุลเงินหลักเดียว คุณสามารถจำลององค์กรเป็นหน่วยปฏิบัติงาน หน่วยปฏิบัติงานต้องใช้สกุลเงินหลักร่วมกัน อย่างไรก็ตาม คุณสามารถป้อนธุรกรรมและสร้างรายงานได้ในหลายสกุลเงิน

### <a name="year-end-closing"></a>การปิดบัญชีสิ้นปี

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

ถ้ากฎหมายและแนวทางปฏิบัติด้านบัญชีแตกต่างกันในประเทศ/ภูมิภาคที่เป็นที่ตั้งขององค์กรของคุณ คุณอาจจำเป็นต้องมีกระบวนงานสิ้นปีที่แตกต่างกันสำหรับแต่ละองค์กร ซึ่งหมายความว่าคุณต้องจำลององค์กรเป็นนิติบุคคล แต่ละนิติบุคคลมีกระบวนงานสิ้นปีของตนเอง

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

ถ้ากฎหมายและแนวทางปฏิบัติด้านบัญชีเหมือนกันในประเทศ/ภูมิภาคที่เป็นที่ตั้งขององค์กรของคุณ คุณสามารถใช้กระบวนงานสิ้นปีเดียวได้ ซึ่งหมายความว่าคุณสามารถจำลององค์กรเป็นหน่วยปฏิบัติงาน หน่วยปฏิบัติงานทั้งหมดต้องใช้กระบวนงานการปิดบัญชีสิ้นปีเดียวกัน

### <a name="number-sequences"></a>ลำดับหมายเลข

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

สามารถตั้งค่าลำดับหมายเลขสำหรับการอ้างอิงบางอย่างสำหรับแต่ละนิติบุคคล ลำดับหมายเลขบางรายการสามารถใช้ร่วมกันได้

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

สามารถตั้งค่าลำดับหมายเลขสำหรับการอ้างอิงบางอย่างสำหรับแต่ละหน่วยปฏิบัติงาน ลำดับหมายเลขบางรายการสามารถใช้ร่วมกันได้

### <a name="products"></a>ผลิตภัณฑ์

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

มีการใช้คำนิยามผลิตภัณฑ์ร่วมกัน และจะต้องถูกนำออกใช้กับนิติบุคคลแต่ละรายการก่อนที่จะสามารถรวมอยู่ในธุรกรรม แต่ละนิติบุคคลมีผลิตภัณฑ์ที่นำออกใช้ของตนเองที่สามารถรวมอยู่ในเอกสารธุรกรรม ถ้าองค์กรภายในของคุณต้องใช้ชุดผลิตภัณฑ์ต่างกัน คุณต้องจำลององค์กรเป็นนิติบุคคล

> [!NOTE]
> แม้ว่าจะใช้นิยามผลิตภัณฑ์ร่วมกัน แต่ในแต่ละนิติบุคคลที่ผลิตภัณฑ์ออกใช้แล้ว คุณสามารถระบุพารามิเตอร์การขาย การซื้อ และการเก็บสต็อกที่แตกต่างกันสำหรับสินค้าที่แต่ละไซต์สินค้าคงคลัง

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

หน่วยปฏิบัติงานทั้งหมดใช้ชุดผลิตภัณฑ์ร่วมกัน ถ้าองค์กรภายในของคุณสามารถใช้ชุดผลิตภัณฑ์เดียวกันร่วมกัน คุณสามารถจำลององค์กรเป็นหน่วยปฏิบัติงานได้

### <a name="inquiry-and-reporting"></a>การสอบถามและรายงาน

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>ถ้าจำลององค์กรเป็นนิติบุคคล

คุณต้องเปลี่ยนบริษัทด้วยตนเองเพื่อป้อนธุรกรรมและดำเนินการสอบถามในนิติบุคคลหลายรายการ เนื่องจากขอบเขตความปลอดภัยของข้อมูล การสอบถามและการรายงานที่รวบรวมไว้อาจเป็นทรัพยากรที่ละเอียดและใช้เวลามาก

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>ถ้าจำลององค์กรเป็นหน่วยปฏิบัติงาน

คุณไม่จำเป็นต้องเปลี่ยนบริษัทเพื่อเข้าถึงข้อมูลจากหลายหน่วยปฏิบัติงาน การสอบถามและการรายงานรวม รวมทั้งการสอบถามในภูมิภาคแต่ละรายการจะง่ายกว่าและรวดเร็วกว่า

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>แนวทางปฏิบัติที่ดีที่สุดสำหรับการจำลององค์กรและลำดับชั้น

พิจารณาแนวทางปฏิบัติที่ดีที่สุดต่อไปนี้เมื่อคุณใช้ลำดับชั้นขององค์กร:

- สร้างแผนกเพื่อจำลองส่วนร่วมระหว่างนิติบุคคลกับหน่วยธุรกิจ จากนั้นคุณสามารถรวมข้อมูลจากแผนกไปยังนิติบุคคลสำหรับการรายงานตามกฎหมาย และจากแผนกไปยังหน่วยธุรกิจสำหรับการรายงานภายใน แผนกต่างๆ สามารถทำหน้าที่เป็นศูนย์กำไร ถ้าคุณใช้แผนก คุณไม่จำเป็นต้องใช้นิติบุคคลและหน่วยธุรกิจเป็นมิติข้อมูลในโครงสร้างทางบัญชี คุณสามารถใช้เฉพาะแผนกเป็นมิติข้อมูลได้ อย่างไรก็ตาม คุณต้องใช้ทั้งศูนย์ต้นทุนและแผนกเป็นมิติข้อมูลในโครงสร้างทางบัญชีหากศูนย์ต้นทุนถูกใช้เป็นตัวสะสมต้นทุนเท่านั้น และแผนกถูกใช้สำหรับการรับรู้รายได้
- จำลองหลายลำดับชั้นสำหรับหน่วยปฏิบัติงานถ้าคุณมีข้อจำกัดที่ซับซ้อนสำหรับการรายงานกำไรและขาดทุน
- ในนิติบุคคลเดียว อย่าจำลองหลายลำดับชั้นสำหรับวัตถุประสงค์ด้านลำดับชั้นเดียว
- อย่างสร้างลำดับชั้นสำหรับทุกวัตถุประสงค์ โดยปกติ คุณสามารถใช้หนึ่งลำดับชั้นสำหรับหลายวัตถุประสงค์ ตัวอย่างเช่น หนึ่งลำดับขั้นสามารถกำหนดนโยบายทั้งหมดที่เกี่ยวข้องกับวัตถุประสงค์
- สร้างลำดับชั้นให้สมดุล ในลำดับชั้น โหนดทั้งหมดที่มีระยะห่างจากโหนดรากเดียวกันถูกกำหนดเป็นระดับ ลำดับชั้นแบบสมดุล เพียงหนึ่งชนิดของหน่วยปฏิบัติงานสามารถเกิดขึ้นในแต่ละระดับ และระยะห่างจากโหนดรากไปแต่ละระดับจะสอดคล้องกัน ถ้ามีระดับกลางระหว่างแผนก และนิติบุคคล หรือหน่วยธุรกิจ ตัวยึดองค์กรอาจจำเป็นเพื่อสร้างลำดับชั้นแบบสมดุล
- อย่าจำลองลำดับชั้นของหน่วยปฏิบัติงานถ้าโครงสร้างสำหรับนิติบุคคลเป็นโครงสร้างของการดำเนินงานของคุณด้วย ลำดับชั้นผสมของนิติบุคคลและหน่วยปฏิบัติงานอาจใช้เพื่อวัตถุประสงค์ทั้งสอง
- ก่อนที่คุณจำลองสถานการณ์ปรับโครงสร้างหลัก ใช้วันที่ที่มีผลบังคับใช้ของลำดับชั้นเพื่อดำเนินการวิเคราะห์ผลกระทบและทดสอบการยืนยัน
- ใช้โหมดแบบร่างเพื่อเปลี่ยนลำดับชั้นก่อนที่คุณเผยแพร่รุ่นใหม่ในสภาพแวดล้อมการผลิต
- จำกัดจำนวนผู้ที่มีสิทธิ์ในการเพิ่มหรือลบองค์กรออกจากลำดับชั้นในสภาพแวดล้อมการผลิต จำนวนต่ำกว่าช่วยลดโอกาสที่จะเกิดข้อผิดพลาด และต้องทำการแก้ไข


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

