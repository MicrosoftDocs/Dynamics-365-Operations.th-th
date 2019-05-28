---
title: เนื้อหา Power BI เกี่ยวกับการจัดการสินเชื่อและการเรียกเก็บเงิน
description: หัวข้อนี้อธิบายถึงสิ่งที่จะรวมอยู่ในเนื้อหา Power BI เกี่ยวกับการจัดการสินเชื่อและการเรียกเก็บเงิน และยังอธิบายถึงวิธีการเข้าถึงรายงาน Power BI และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างเนื้อหานี้
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a80a180623d1cca77c633f12bcd92a088e089ee5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547243"
---
# <a name="credit-and-collections-management-power-bi-content"></a>เนื้อหา Power BI เกี่ยวกับการจัดการสินเชื่อและการเรียกเก็บเงิน

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายถึงสิ่งที่จะรวมอยู่ในเนื้อหา Microsoft Power BI เกี่ยวกับ **การจัดการสินเชื่อและการเรียกเก็บเงิน** และยังอธิบายถึงวิธีการเข้าถึงรายงาน Power BI และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างเนื้อหานี้

## <a name="overview"></a>ภาพรวม

เนื้อหา Power BI เกี่ยวกับ **การจัดการสินเชื่อและการเรียกเก็บเงิน** ถูกสร้างขึ้นสำหรับผู้จัดการฝ่ายสินเชื่อและการเรียกเก็บเงิน และเสมียนฝ่ายเรียกเก็บเงิน ซึ่งให้สินเชื่อหลักและเมตริกการเรียกเก็บเงิน เช่น ระยะเวลาการเก็บหนี้ถัวเฉลี่ย ยอดดุลที่พ้นกำหนดชำระ ความเสี่ยงของสินเชื่อ และลูกค้าที่เกินวงเงินสินเชื่อ ใช้ข้อมูลทางธุรกรรม และให้มุมมองรวมของสินเชื่อและการเรียกเก็บเงินระหว่างบริษัททั้งหมด ยังให้การแบ่งรายละเอียดสำหรับแต่ละบริษัท กลุ่มลูกค้า และลูกค้าอีกด้วย

เนื้อหา Power BI นี้ ประกอบด้วยหน้ารายงาน 10 หน้า:

- หน้าภาพรวมสองหน้า (หนึ่งหน้าสำหรับภาพรวมของเครดิต และหนึ่งหน้าสำหรับภาพรวมของการเรียกเก็บเงิน)
- หน้ารายละเอียดแปดหน้า ซึ่งให้รายละเอียดของเมตริกสินเชื่อและการเรียกเก็บเงินที่ถูกแบ่งย่อยระหว่างมิติต่าง ๆ

ยอดเงินทั้งหมดจะถูกแสดงในสกุลเงินของระบบ คุณสามารถตั้งค่าสกุลเงินของระบบได้ในหน้า **พารามิเตอร์ระบบ**

โดยค่าเริ่มต้น ข้อมูลสินเชื่อและการเรียกเก็บเงินสำหรับบริษัทปัจจุบันจะปรากฏขึ้น เมื่อต้องการดูข้อมูลระหว่างบริษัททั้งหมด มอบหมายหน้าที่ **CustCollectionsBICrossCompany** ให้กับบทบาท

## <a name="accessing-the-power-bi-content"></a>การเข้าถึงเนื้อหา Power BI
เนื้อหา Power BI **การจัดการสินเชื่อและการเรียกเก็บเงิน** จะปรากฏในพื้นที่ทำงาน **สินเชื่อของลูกค้าและการเรียกเก็บเงิน**

## <a name="reports-that-are-included-in-the-power-bi-content"></a>รายงานที่รวมอยู่ในเนื้อหา Power BI

เนื้อหา Power BI **CustCollectionsBICrossCompany** มีรายงานที่ประกอบด้วยชุดของเมตริก เมตริกเหล่านี้จะถูกแสดงภาพข้อมูลโดยเป็นแผนภูมิ ไทล์ และตาราง ตารางต่อไปนี้แสดงภาพรวมของการแสดงภาพประกอบในเนื้อหา **CustCollectionsBICrossCompany** ใน Power BI

| หน้ารายงาน                 | การแสดงภาพ |
|-----------------------------|---------------|
| ภาพรวมการเรียกเก็บเงิน        | <ul><li>เลยกำหนดชำระของลูกค้า</li><li>เกินวงเงินสินเชื่อของลูกค้า</li><li>DSO 30 วัน</li><li>กรณีที่เปิด</li><li>จำนวนวันเฉลี่ยที่จะปิดกรณี</li><li>กิจกรรมที่เปิด</li><li>จำนวนวันเฉลี่ยที่จะปิดกิจกรรม</li><li>เปิดดอกเบี้ยตั๋วเงิน</li><li>เปิดจดหมายเรียกเก็บเงิน</li><li>ระงับลูกค้า</li><li>ระงับการขาย</li><li>ยอดดุลตามอายุหนี้</li><li>ยอดเงินในสถานะการเรียกเก็บเงิน</li><li>ยอดเงินสำหรับรหัสการเรียกเก็บเงิน</li><li>การตัดจ่ายตามเหตุผล</li><li>ยอดดุลครบกำหนดตามภูมิภาค</li><li>การชำระเงินที่คาดไว้</li></ul> |
| ภาพรวมสินเชื่อ             | <ul><li>เลยกำหนดชำระของลูกค้า</li><li>วงเงินสินเชื่อเทียบกับยอดดุลที่ครบกำหนด</li><li>กริดลูกค้าที่เกินวงเงินสินเชื่อ</li><li>ลูกค้าเกินวงเงินสินเชื่อสำหรับบริษัท</li><li>สินเชื่อที่ใช้เทียบกับวงเงินสินเชื่อทั้งหมด</li><li>วงเงินสินเชื่อเทียบกับสินเชื่อที่ใช้ตามภูมิภาค</li><li>ลูกค้าสำหรับการจัดอันดับความน่าเชื่อถือ</li></ul> |
| วงเงินสินเชื่อ                | <ul><li>วงเงินสินเชื่อ</li><li>รายละเอียดวงเงินสินเชื่อ</li><li>วงเงินสินเชื่อสำหรับลูกค้าแต่ละราย</li><li>วงเงินสินเชื่อสำหรับกลุ่มลูกค้า</li><li>วงเงินสินเชื่อในการจัดอันดับความน่าเชื่อถือสำหรับบริษัท</li><li>วงเงินสินเชื่อเทียบกับสินเชื่อที่ใช้ตามภูมิภาค</li></ul> |
| เกินวงเงินสินเชื่อของลูกค้า | <ul><li>เกินวงเงินสินเชื่อของลูกค้า</li><li>รายละเอียดลูกค้าที่เกินวงเงินสินเชื่อ</li><li>ลูกค้าเกินวงเงินสินเชื่อสำหรับบริษัท</li><li>ลูกค้าที่เกินวงเงินสินเชื่อสำหรับกลุ่มลูกค้าแต่ละกลุ่ม</li><li>เกินวงเงินสินเชื่อของลูกค้าตามภูมิภาค</li></ul> |
| เลยกำหนดชำระของลูกค้า          | <ul><li>เลยกำหนดชำระของลูกค้า</li><li>รายละเอียดลูกค้าที่เลยกำหนดชำระ</li><li>ลูกค้าที่เลยกำหนดชำระสำหรับแต่ละบริษัท</li><li>ลูกค้าที่เลยกำหนดชำระสำหรับกลุ่มลูกค้าแต่ละกลุ่ม</li><li>ลูกค้าที่เลยกำหนดชำระตามภูมิภาค</li></ul> |
| ยอดดุลตามอายุหนี้               | <ul><li>ยอดดุลตามอายุหนี้</li><li>รายละเอียดยอดดุลตามอายุหนี้</li><li>ยอดดุลตามอายุหนี้ต่อบริษัท</li><li>ยอดดุลตามอายุหนี้ต่อกลุ่มลูกค้า</li></ul> |
| การชำระเงินที่คาดไว้           | <ul><li>การชำระเงินที่คาดไว้</li><li>รายละเอียดการชำระเงินที่คาดไว้</li><li>การชำระเงินที่คาดไว้สำหรับบริษัท</li><li>การชำระเงินที่คาดไว้สำหรับกลุ่มลูกค้า</li><li>การชำระเงินที่คาดไว้ตามภูมิภาค</li></ul> |
| การตัดจ่าย                  | <ul><li>การตัดจ่ายโดยเรียงตามภูมิภาค</li><li>รายละเอียดการตัดจ่าย</li><li>การตัดจ่ายโดยเรียงตามบัญชีหลัก</li><li>การตัดจ่ายสำหรับแต่ละบริษัท</li><li>การตัดจ่ายสำหรับกลุ่มลูกค้าแต่ละกลุ่ม</li><li>การตัดจ่ายโดยเรียงตามภูมิภาค</li></ul> |
| สถานะการเรียกเก็บเงิน          | <ul><li>มีข้อโต้แย้ง</li><li>ผิดสัญญาว่าจะชำระ</li><li>สัญญาว่าจะชำระ</li><li>รายละเอียดสถานะการเรียกเก็บเงิน</li><li>ยอดเงินในสถานะการเรียกเก็บเงิน</li><li>กรณีที่เปิด</li><li>กิจกรรมที่เปิด</li></ul> |
| จดหมายเรียกเก็บเงิน         | <ul><li>ยอดเงินสำหรับรหัสการเรียกเก็บเงิน</li><li>รายละเอียดยอดเงินสำหรับรหัสการเรียกเก็บเงิน</li><li>จำนวนจดหมายเรียกเก็บเงินสำหรับแต่ละบริษัท</li><li>จำนวนจดหมายเรียกเก็บเงินสำหรับกลุ่มลูกค้าแต่ละกลุ่ม</li><li>จำนวนจดหมายเรียกเก็บเงินตามภูมิภาค</li></ul> |

สามารถกรองข้อมูลและตรึงแผนภูมิและไทล์ในรายงานเหล่านี้ทั้งหมดไปยังแดชบอร์ดได้ ดูข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกรองข้อมูลและตรึงใน Power BI ได้ที่ [สร้างและตั้งค่าคอนฟิกแดชบอร์ด](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/) คุณยังสามารถใช้ฟังก์ชันส่งออกข้อมูลพื้นฐาน เพื่อส่งออกข้อมูลพื้นฐานที่มีการสรุปในการแสดงภาพ

## <a name="understanding-the-data-model-and-entities"></a>การทำความเข้าใจเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้

ข้อมูลดังต่อไปนี้ถูกใช้ในการกรอกรายงานในเนื้อหา Power BI เกี่ยวกับ **การจัดการสินเชื่อและการเรียกเก็บเงิน** ข้อมูลนี้จะแสดงเป็นหน่วยวัดรวมที่มีการแบ่งระยะในที่จัดเก็บเอนทิตี้ ที่จัดเก็บเอนทิตี้คือฐานข้อมูล Microsoft SQL Server ที่ได้รับการปรับให้เหมาะสมสำหรับการวิเคราะห์ สำหรับข้อมูลเพิ่มเติม ดู [ภาพรวมของการรวม Power BI กับร้านค้าเอนทิตี](../../dev-itpro/analytics/power-bi-integration-entity-store.md)


|                   เอนทิตี้                    |      การวัดแบบรวมหลัก      |             แหล่งข้อมูล              |                           ฟิลด์                            |                                    คำอธิบาย                                     |
|---------------------------------------------|--------------------------------------|--------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities AveragecClosedTime  |            smmActivities             | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) |     จำนวนกิจกรรมที่ปิดและเวลาเฉลี่ยที่จะปิดกิจกรรมเหล่านั้น     |
|       CustCollectionsBIActivitiesOpen       |            ActivityNumber            |            smmActivities             |                   Count(ActivityNumber)                    |                           จำนวนของกิจกรรมที่เปิด                            |
|        CustCollectionsBIAgedBalances        |             AgedBalances             |  CustCollectionsBIAgedBalancesView   |                 Sum(SystemCurrencyBalance)                 |                             ผลรวมของยอดดุลตามอายุหนี้                              |
|        CustCollectionsBIBalancesDue         |         SystemCurrencyAmount         |   CustCollectionsBIBalanceDueView    |                 Sum(SystemCurrencyAmount)                  |                           ยอดเงินที่พ้นกำหนดชำระ                            |
|    CustCollectionsBICaseAverageCloseTIme    |  NumOfCases CaseAverageClosedTime   |      CustCollectionsCaseDetail       | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) |        จำนวนกิจกรรมที่ปิดและเวลาเฉลี่ยที่จะปิดกิจกรรมเหล่านั้น        |
|         CustCollectionsBICasesOpen          |                CaseId                |      CustCollectionsCaseDetail       |                       Count(CaseId)                        |                              จำนวนของกรณีที่เปิด                              |
|      CustCollectionsBICollectionLetter      |         CollectionLetterNum          |       CustCollectionLetterJour       |                 Count(CollectionLetterNum)                 |                       จำนวนของจดหมายเรียกเก็บเงินที่เปิด                        |
|   CustCollectionsBICollectionLetterAmount   |       CollectionLetterAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                     ยอดดุลของจดหมายเรียกเก็บเงินที่ลงรายการบัญชีแล้ว                      |
|      CustCollectionsBICollectionStatus      |       CollectionStatusAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                ยอดดุลของธุรกรรมที่มีสถานะการเรียกเก็บเงิน                 |
|           CustCollectionsBICredit           | CreditExposed AmountOverCreditLimit |     CustCollectionsBICreditView      |       Sum(CreditExposed) Sum(AmountOverCreditLimit)       | ผลรวมของความเสี่ยงเครดิตและยอดเงินที่ลูกค้าเกินวงเงินสินเชื่อ |
|         CustCollectionsBICustOnHold         |               บล็อค                |      CustCollectionsBICustTable      |                       Count(Blocked)                       |                     จำนวนของลูกค้าที่ระงับ                      |
|            CustCollectionsBIDSO             |                DSO30                 |       CustCollectionsBIDSOView       |                  AverageOfChildren(DSO30)                  |                        ระยะเวลาการเก็บหนี้ถัวเฉลี่ยนาน 30 วัน                         |
|      CustCollectionsBIExpectedPayment       |           ExpectedPayment            | CustCollectionsBIExpectedPaymentView |                 Sum(SystemCurrencyAmounts)                 |                 ผลรวมของการชำระเงินที่คาดไว้ภายในปีถัดไป                 |
|        CustCollectionsBIInterestNote        |             InterestNote             |           CustInterestJour           |                    Count(InterestNote)                     |                จำนวนของดอกเบี้ยตั๋วเงินที่ได้มีการสร้าง                |
|        CustCollectionsBISalesOnHold         |               SalesId                |              SalesTable              |                       Count(SalesId)                       |                 จำนวนของใบสั่งขายรวมที่ระงับ                 |
|          CustCollectionsBIWriteOff          |            WriteOffAmount            |    CustCollectionsBIWriteOffView     |                 Sum(SystemCurrencyAmount)                  |                ผลรวมของธุรกรรมที่มีการตัดบัญชี                 |

