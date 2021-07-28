---
title: ข้อความตัวประมวลผลข้อความ
description: หัวข้อนี้มีข้อมูลเกี่ยวกับคุณลักษณะข้อความตัวประมวลผลข้อความของปริมาณงานของ scale unit
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 35fd48ef300d46d00c07f3231d780d1ba431d8ef
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350581"
---
# <a name="message-processor-messages"></a>ข้อความตัวประมวลผลข้อความ

[!include [banner](../includes/banner.md)]

จะมีการใช้ข้อความตัวประมวลผลข้อความ เมื่อรัน scale unit ของระบบคลาวด์และ edge สำหรับ [ปริมาณงานการผลิต](cloud-edge-workload-manufacturing.md) และ [ปริมาณงานการจัดการคลังสินค้า](cloud-edge-workload-warehousing.md)

มีการแลกเปลี่ยนข้อมูลจํานวนมากระหว่างสภาพแวดล้อมการปรับใช้ฮับและ scale unit เพื่อให้มีการซิงค์กันเสมอ แต่การแลกเปลี่ยนข้อมูลเหล่านี้เพียงสองสามรายการจะได้รับการประมวลผลโดย *ตัวประมวลผลข้อความ* คุณสามารถดูข้อความที่ประมวลผลโดยตัวประมวลผลข้อความได้โดยไปที่ **การจัดการระบบ > ตัวประมวลผลข้อความ > ข้อความตัวประมวลผลข้อความ**

## <a name="message-grid-columns-and-filters"></a>คอลัมน์และตัวกรองกริดข้อความ

คุณสามารถใช้ฟิลด์ที่ด้านบนของหน้า **ข้อความตัวประมวลผลข้อความ** เพื่อช่วยค้นหาข้อความเฉพาะใดๆ ที่คุณกำลังค้นหา ตัวกรองข้อมูลส่วนใหญ่เหล่านี้ตรงกับหัวข้อคอลัมน์ในกริดข้อความ ตัวกรองข้อมูลและหัวข้อคอลัมน์ต่อไปนี้พร้อมใช้งาน:

- **ชนิดข้อความ** – ระบุชนิดของข้อความ
- **คิวข้อความ** – ระบุชื่อของคิวที่จะประมวลผลข้อความ มีการระบุคิวต่อไปนี้:
  - *สเกลยูนิตกับฮับ*
  - *ฮับไปยัง Scale Unit ที่มีการดำเนินการคลังสินค้า*
  - *ฮับไปยัง Scale Unit การดำเนินการผลิต*
- **สถานะข้อความ** – ระบุสถานะของข้อความ มีสถานะต่อไปนี้อยู่:
  - *จัดคิวแล้ว* – ข้อความพร้อมแล้วที่จะถูกประมวลผลโดยตัวประมวลผลข้อความ
  - *ประมวลผลแล้ว* – ข้อความถูกประมวลผลเสร็จเรียบร้อยแล้วโดยตัวประมวลผลข้อความ
  - *ยกเลิกแล้ว* – มีการประมวลผลข้อความแล้ว แต่การประมวลผลล้มเหลว
- **เนื้อหาข้อความ** – ตัวกรองนี้ทำการค้นหาข้อความแบบเต็มของเนื้อหาข้อความ (เนื้อหาข้อความไม่ถูกแสดงในกริด) ตัวกรองจะถือว่าสัญลักษณ์พิเศษส่วนใหญ่ (เช่น "-") เป็นช่องว่าง และถือว่าอักขระพื้นที่ทั้งหมดเป็นตัวปฏิบัติการ OR แบบบูลีน T=ตัวอย่างเช่น นี่หมายความว่า ถ้าคุณค้นหาค่า `journalid` เฉพาะที่เท่ากับ "USMF-123456" ระบบจะค้นหาข้อความทั้งหมดที่มี "USMF" หรือ "123456" ซึ่งมีแนวโน้มที่จะเป็นรายการยาว ดังนั้น ควรป้อนเพียง "123456" อย่างเดียว เนื่องจากจะส่งคืนผลลัพธ์ที่เฉพาะเจาะจงมากขึ้น

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>ชนิดข้อความตัวอย่าง: ร้องขอการอัพเดตทางการเงินของการปรับปรุงสินค้าคงคลัง

ตัวอย่างเช่น **ชนิดข้อความ** *ร้องขอการอัพเดตทางการเงินของการปรับปรุงสินค้าคงคลัง* ถูกใช้ในการสร้างและลงรายการบัญชีสมุดรายวันการตรวจนับบนฮับ เมื่อผู้ปฏิบัติงานใช้แอปคลังสินค้าเพื่อ [ลงทะเบียนการปรับปรุงสินค้าคงคลัง](cloud-edge-warehouse-inventory-adjustment.md) บนปริมาณงานการจัดการคลังสินค้าของ scale unit เนื่องจากกระบวนการเฉพาะนี้มาจาก scale unit ฟิลด์ **คิวข้อความ** จะแสดงค่า *Scale unit ไปยังฮับ*

สำหรับชนิดข้อความนี้ ปริมาณงาน scale unit จะบันทึกข้อความเป็นส่วนหนึ่งของการดําเนินงานปรับปรุงสินค้าคงคลังของแอปคลังสินค้า จากนั้น ข้อมูลข้อความจะถูกโอนย้ายไปยังฮับเป็นส่วนหนึ่งของกระบวนการเดียวกันที่ใช้กับ [สถาปัตยกรรมของ Commerce Data Exchange](../../commerce/commerce-architecture.md) จะมีการอัพเดตข้อความเพื่อแสดง **สถานะข้อความ** เป็น *จัดคิวแล้ว* จากนั้น ตัวประมวลผลข้อความจะพยายามประมวลผลข้อความและอัพเดต **สถานะข้อความ** เป็น *ประมวลผลแล้ว* เมื่อสำเร็จ หรือ *ยกเลิกแล้ว* เมื่อล้มเหลว

## <a name="view-the-message-log-message-content-and-details"></a>ดูล็อกข้อความ เนื้อหาข้อความ และรายละเอียด

คุณสามารถค้นหารายละเอียดเกี่ยวกับข้อความได้โดยเลือกข้อความนั้นในกริด แล้วจากนั้น เปิดแท็บ **ล็อก** หรือ **เนื้อหาข้อความ** ภายใต้กริดข้อความ โดยที่เหตุการณ์การประมวลผลแต่ละเหตุการณ์จะแสดงขึ้น

**เนื้อหาของข้อความ** จะขึ้นอยู่กับ **ชนิดของข้อความ** และดังนั้นจึงมีความยาวข้อความที่แตกต่างกัน ข้อความเนื้อหาของข้อความทั่วไปจะขึ้นต้นด้วย **{** และลงท้ายด้วย **}** และในระหว่างนั้น มีชื่อฟิลด์ เช่น `journalId` ซึ่งตามด้วย **:** และค่า เช่น *USMF-123456*

แถบเครื่องมือบนแท็บ **ล็อก** จะรวมปุ่มต่อไปนี้:

- **ล็อก** – แสดงผลลัพธ์ของการประมวลผล ซึ่งมีประโยชน์โดยเฉพาะอย่างยิ่งในการเข้าใจเหตุผลสำหรับการประมวลผลความล้มเหลวสำหรับข้อความที่มี **ผลลัพธ์ของการประมวลผล** เป็น *ล้มเหลว*
- **กลุ่มงาน** – การดําเนินการประมวลผลข้อความหลายรายการสามารถรันเป็นส่วนหนึ่งของกระบวนการชุดงานเดียวกันได้ เลือกปุ่มนี้เพื่อดูข้อมูลโดยละเอียดนี้ ตัวอย่างเช่น คุณสามารถดูว่ามีการอ้างอิงที่ต้องการให้ระบบประมวลผลข้อความบางข้อความในลำดับเฉพาะหรือไม่

## <a name="message-processor-batch-job"></a>งานของชุดงานตัวประมวลผลข้อความ

เมื่อรันการปรับใช้ระบบคลาวด์และ edge ชุดงาน *ตัวประมวลผลข้อความ* จะได้รับการเริ่มต้นโดยอัตโนมัติ เมื่อมีการสร้างข้อความใหม่เพื่อการประมวลผล ดังนั้นคุณจึงไม่ควรจะต้องจัดกำหนดการงานนี้ด้วยตนเอง

ถ้าจําเป็น คุณสามารถเข้าถึงชุดงานได้โดยไปที่ **การจัดการระบบ > ตัวประมวลผลข้อความ > ตัวประมวลผลข้อความ**

## <a name="manually-process-or-cancel-a-message"></a>ประมวลผลหรือยกเลิกข้อความด้วยตนเอง

ถ้าจําเป็น คุณสามารถประมวลผลหรือยกเลิกข้อความด้วยตนเองได้ตามสถานะปัจจุบัน เมื่อต้องการทำเช่นนั้น ให้เลือกข้อความในกริด แล้วจากนั้น เลือก **กระบวนการ** หรือ **ยกเลิก** ในบานหน้าต่างการดำเนินการ

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>ตั้งค่าเหตุการณ์ทางธุรกิจเพื่อจัดส่งข้อความแจ้งเตือนสำหรับผลลัพธ์ของการประมวลผลที่ล้มเหลว

นอกจากการกรองค่า **สถานะข้อความ** *ยกเลิกแล้ว* เพื่อสอบถามข้อความที่ล้มเหลว คุณสามารถตั้งค่า [เหตุการณ์ทางธุรกิจ](../../fin-ops-core/dev-itpro/business-events/home-page.md) บนฮับ เพื่อแจ้งเตือนคุณเรื่องผลลัพธ์ของการประมวลผลที่ล้มเหลว เมื่อต้องการทำเช่นนั้น ให้เรียกใช้เหตุการณ์ทางธุรกิจที่ชื่อ *ข้อความของตัวประมวลผลข้อความที่ประมวลผล*  บนหน้า **แค็ตตาล็อกเหตุการณ์ทางธุรกิจ** (**การจัดการระบบ > การตั้งค่า > เหตุการณ์ทางธุรกิจ > แค็ตตาล็อกเหตุการณ์ทางธุรกิจ**)

เนื่องจากเป็นส่วนหนึ่งของกระบวนการเรียกใช้ คุณจะได้รับการแนะนำให้ระบุว่าเหตุการณ์นี้เฉพาะเจาะจงสำหรับนิติบุคคลหนึ่งรายหรือนิติบุคคลทั้งหมด และระบุ **ชื่อปลายทาง** ซึ่งต้องถูกกําหนดไว้ก่อน

>[!NOTE]
> หาก **เมื่อเหตุการณ์ทางธุรกิจเกิดขึ้น** ถูกตั้งค่าเป็น *Microsoft Power Automate* (ตัวอย่างเช่น แทนที่จะเป็น *HTTPS*) **ชื่อปลายทาง** จะถูกสร้างขึ้นโดยอัตโนมัติใน Supply Chain Management ตามการตั้งค่า *Microsoft Power Automate*

### <a name="microsoft-power-automate-example"></a>ตัวอย่าง Microsoft Power Automate

ในตัวอย่างนี้ ใช้ **เมื่อเกิดเหตุการณ์ทางธุรกิจเกิดขึ้น** กับ *Microsoft Power Automate* ส่งอีเมลที่มีข้อความ InfoLog และไฮเปอร์ลิงค์ เพื่อเปิดหน้า **ข้อความตัวประมวลผลข้อความ** สำหรับข้อความที่ล้มเหลวเฉพาะในการปรับใช้ฮับ หากจำเป็น คุณสามารถเพิ่มตรรกะพิเศษเพื่อส่งการแจ้งเตือนพร้อมกันโดยใช้ช่องทางต่างๆ และควบคุมผู้รับตามข้อมูลเหตุการณ์ได้

1. ใน [Power Automate](https://preview.flow.microsoft.com) ให้สร้างโฟลว์ระบบคลาวด์แบบอัตโนมัติใหม่เพื่อทริกเกอร์โฟลว์ **เมื่อเหตุการณ์ทางธุรกิจเกิดขึ้น - Fin & Ops App (Dynamics 365)** ตามด้วย **แยกวิเคราะห์ JSON** และ **ส่งอีเมล** ดังที่แสดงในภาพอธิบายต่อไปนี้

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate โฟลว์ระบบคลาวด์แบบอัตโนมัติ":::

1. ในขั้นตอน **เมื่อเหตุการณ์ทางธุรกิจเกิดขึ้น** คุณสามารถค้นหาหรือป้อน **อินสแตนซ์** ของฮับที่ตามด้วย **ประเภท** แล้วจากนั้น **เหตุการณ์ทางธุรกิจ** *ประมวลผลข้อความตัวประมวลผลข้อความแล้ว* ตามที่แสดงไว้ในภาพอธิบายต่อไปนี้

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate ขั้นตอนเมื่อเหตุการณ์ทางธุรกิจเกิดขึ้น":::

1. สำหรับขั้นตอน **แยกวิเคราะห์ JSON** ป้อน **เค้าร่าง** ที่กำหนดฟิลด์แบบขยาย คุณสามารถใช้ตัวเลือก *ดาวน์โหลดเค้าร่าง* ในหน้า **แค็ตตาล็อกเหตุการณ์ทางธุรกิจ** ใน Supply Chain Management หรือเริ่มต้นโดยการวางในข้อความเค้าร่างตัวอย่าง ข้อความตัวอย่างนี้จะให้ไว้หลังจากภาพประกอบต่อไปนี้

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate ขั้นตอนแยกวิเคราะห์ JSON":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. ในขั้นตอน **ส่งอีเมล** คุณสามารถเลือกฟิลด์แต่ละฟิลด์ หรือเริ่มต้นโดยการวางตัวอย่างเนื้อหาอีเมลลงในฟิลด์ **เนื้อหา** ตัวอย่างนี้จะให้ไว้หลังจากภาพประกอบต่อไปนี้

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate ขั้นตอนส่งอีเมล":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. เมื่อคุณบันทึกเหตุการณ์ทางธุรกิจ เหตุการณ์ทางธุรกิจนั้นจะถูกเรียกใช้งานโดยอัตโนมัติและพร้อมใช้งานโดยเป็นส่วนหนึ่งของ Supply Chain Management
