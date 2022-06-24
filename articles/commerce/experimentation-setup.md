---
title: การตั้งค่าการทดสอบ
description: บทความนี้อธิบายวิธีการตั้งค่าการทดลองในบริการของบุคคลที่สาม
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946209"
---
# <a name="set-up-an-experiment"></a>การตั้งค่าการทดสอบ

หลังจากที่คุณ [กำหนดสมมติฐานและกำหนดการวัดความสำเร็จใดที่คุณต้องการใช้](experimentation-identify.md) คุณจะต้องตั้งค่าการทดลองของคุณในบริการของบุคคลที่สาม แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับการตั้งค่า และการรันการทดลองบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในบทความที่แยกต่างหาก

[ ![การเดินทางของผู้ใช้การทดสอบ - การตั้งค่า](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>ตั้งค่าการทดลองของคุณในบริการของบุคคลที่สาม
ขณะนี้คุณควรเลือกบริการของบุคคลที่สามเพื่อรันและตรวจสอบการทดลองของคุณ และตั้งค่าตัวเชื่อมต่อการทดสอบ ข้อกำหนดเบื้องต้นเหล่านี้จะแสดงรายการอยู่ใน  [การทดสอบใน Dynamics 365 Commerce](experimentation-overview.md)

ทำตามขั้นตอนที่จำเป็นในการสร้างการทดลองของคุณในบริการของบุคคลที่สาม ถ้ามีการตั้งค่าคอนฟิกตัวเชื่อมต่ออย่างถูกต้อง รายการที่สมบูรณ์ของการทดลองที่คุณตั้งค่าไว้ในบริการของบุคคลที่สามจะแสดงในตัวสร้างไซต์ Commerce ภายในประมาณ 5 นาที

## <a name="set-up-your-success-metrics"></a>ตั้งค่าตัวชี้วัดความสำเร็จของคุณ
การทดสอบทั้งหมดต้องมีตัวชี้วัดที่จะวัดผลของการเปลี่ยนแปลง และตรวจสอบความถูกต้องของสมมติฐาน ให้ทำตามขั้นตอนต่อไปนี้เพื่อเปิดใช้งานการคำนวณตัวชี้วัดในบริการของบุคคลที่สามโดยใช้เหตุการณ์ การตรวจวัดระยะไกลแบบใช้งานจริงจาก Dynamics 365 Commerce

หากต้องการตั้งค่าตัวชี้วัดความสำเร็จของคุณให้กับโมดูลสำเร็จรูป ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ในโปรแกรมสร้างไซต์ Commerce ให้เลือกแท็บ **หน้า** ในบานหน้าต่างนำทางด้านซ้าย แล้วเลือกหน้าที่คุณต้องการรวบรวมตัวชี้วัด 
1. ไปที่ส่วน **รหัสเหตุการณ์เพื่อติดตาม** ในบานหน้าต่างคุณสมบัติด้านขวาของหน้าหรือโมดูลที่คุณต้องการติดตาม
1. เลือก **ดู** รายการของรหัสเหตุการณ์การคลิกทั้งหมดจะแสดงขึ้น คัดลอกเหตุการณ์ที่คุณต้องการติดตาม และวางคีย์เหตุการณ์ลงในสถานที่ที่กำหนดไว้ในบริการของบุคคลที่สาม ถ้าคุณต้องการมากกว่าหนึ่งเหตุการณ์ ให้คัดลอกคีย์ทีละครั้ง 
1. สำหรับมุมมองหน้า ใช้ค่าแฮช SHA-256 ของชื่อหน้าของโปรแกรมสร้างไซต์ที่ผนวกเข้ากับ `.PageView` ตัวอย่างเช่น รหัสเหตุการณ์ `Homepage.PageView` จะเป็น `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`
1. ดำเนินการขั้นตอนอื่นๆ สำหรับการติดตามตัวชี้วัดตามที่จำเป็นในบริการของบุคคลที่สาม

หากต้องการคลิกโมดูลที่กำหนดเอง ให้ปฏิบัติตามขั้นตอนต่อไปนี้เมื่อต้องการใช้เหตุการณ์การคลิก:

1. จัดเตรียมออบเจ็กต์ **TelemetryContent** ของโมดูลโดยใช้ฟังก์ชันด้านล่าง ฟังก์ชันนี้จะใช้ชื่อหน้า ชื่อโมดูล และออบเจ็กต์การวัดและส่งข้อมูลทางไกลเริ่มต้นที่ให้ SDK เป็นข้อมูลป้อนเข้า

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    ดังตัวอย่างต่อไปนี้: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. สร้างข้อมูลของส่วนข้อมูลที่มีข้อมูลเกี่ยวกับสิ่งที่ต้องการรวบรวม สำหรับปุ่มและตัวควบคุมแบบคงที่อื่นๆ คุณสามารถรวม **etext** เช่น "เลือกซื้อตอนนี้" หรือ "ค้นหา" และส่วนประกอบโดยการคลิกที่คลิก เช่น การคลิกที่บัตรผลิตภัณฑ์ คุณสามารถส่ง **recid** ซึ่งเป็นรหัสเรกคอร์ดของผลิตภัณฑ์หรือรหัสผลิตภัณฑ์

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    ดังตัวอย่างจากตัวควบคุมแบบคงที่ ให้ส่งผ่านสตริงข้อความปุ่มดังที่แสดงด้านล่าง

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    ตัวอย่างเช่น การคลิกผลิตภัณฑ์ ให้ส่งผ่าน recordId ของผลิตภัณฑ์ดังที่แสดงด้านล่าง:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. เรียกใช้ฟังก์ชัน **OnClick** เพื่อลงทะเบียนเหตุการณ์

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    ดังตัวอย่างต่อไปนี้:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>ขั้นตอนก่อนหน้า
[ระบุสมมติฐานและกำหนดตัวชี้วัดสำหรับการทดสอบ](experimentation-identify.md) 


## <a name="next-step"></a>ขั้นตอนต่อไป
[เชื่อมต่อและแก้ไขการทดสอบ](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
