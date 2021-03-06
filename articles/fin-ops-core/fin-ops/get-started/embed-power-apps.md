---
title: ฝังแอปพื้นที่ทำงาน จาก Power Apps
description: หัวข้อนี้อธิบายวิธีการฝังแอปพื้นที่ทำงาน จาก Microsoft Power Apps ไปยังไคลเอนต์เพื่อเสริมฟังก์ชันของผลิตภัณฑ์
author: jasongre
manager: AnnBe
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: fbdd4dd1bb0b850319b12e55b0e68d6fdc516ad6
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798388"
---
# <a name="embed-canvas-apps-from-power-apps"></a>ฝังแอปพื้นที่ทำงาน จาก Power Apps

[!include [banner](../includes/banner.md)]

Microsoft Power Apps เป็นบริการที่อนุญาตให้ทั้งนักพัฒนาและผู้ใช้ที่ไม่ใช่ทางเทคนิคสามารถสร้างแอปทางธุรกิจที่กำหนดเองได้สำหรับอุปกรณ์เคลื่อนที่ แท็บเล็ต และเว็บ โดยไม่ต้องมีการเขียนรหัส แอป Finance and Operations สนับสนุนการรวมกับ Power Apps แอปพื้นที่ทำงาน หรือระบบแวดล้อมที่กว้างขึ้น ที่คุณ องค์กรของคุณพัฒนา จะสามารถฝังตัวในแอป Finance and Operations เพื่อเพิ่มฟังก์ชันการทำงานของผลิตภัณฑ์ ตัวอย่างเช่น คุณอาจสร้างแอปพื้นที่ทำงาน จาก Power Apps เพื่อเสริมแอป Finance and Operations ด้วยข้อมูลที่ดึงมาจากระบบอื่น

เพื่อเรียนรู้เพิ่มเติมเกี่ยวกับ Power Apps ที่ฝัง ดูวิดีโอสั้นๆ [วิธีการฝัง Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY)

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>การเพิ่มแอปพื้นที่ทำงานที่ฝังจาก Power Apps ไปยังหน้าหนึ่ง

### <a name="overview"></a>ภาพรวม

ก่อนที่จะฝังแอปพื้นที่ทำงาน จาก Power Apps ลงในไคลเอนต์ คุณต้องค้นหาหรือสร้างแอปที่มีภาพหรือฟังก์ชันการทำงานที่ต้องการ หัวข้อนี้จะไม่มีคำอธิบายโดยละเอียดเกี่ยวกับกระบวนการสำหรับการสร้างแอป ถ้าคุณเป็นมือใหม่สำหรับ Power Apps ดูที่ [คู่มือ Power Apps](https://docs.microsoft.com/powerapps/)

การเข้าถึงแอปพื้นที่ทำงานที่เฉพาะเจาะจงบนหน้า มีอยู่สองวิธีเมื่อคุณพร้อมที่จะฝังแอป คุณสามารถเลือกวิธีการที่เหมาะสมกับสถานการณ์จำลองของคุณได้ดีกว่า วิธีการแรกคือ โดยใช้ปุ่ม **Power Apps** ที่ได้ถูกเพิ่มลงในบานหน้าต่างการดำเนินการมาตรฐาน แอปที่คุณเพิ่มโดยใช้วิธีการนี้จะปรากฏเป็นรายการบนปุ่มเมนู **Power Apps** เมื่อคุณเลือกหนึ่งรายการ บานหน้าต่างด้านข้างที่มีแอปฝังอยู่จะปรากฎขึ้น อีกทางเลือกหนึ่ง คุณสามารถเลือกที่จะฝังแอปลงบนหน้าโดยตรงในแท็บใหม่ แท็บด่วน หรือเบลด หรือเป็นส่วนใหม่ในพื้นที่ทำงาน

เมื่อคุณตั้งค่าคอนฟิกแอปพื้นที่ทำงานที่ฝังไว้ คุณสามารถเลือกฟิลด์เดียวที่คุณต้องการส่งเป็นบริบทไปยังแอป ขั้นตอนนี้เปิดการใช้งานให้แอปสามารถตอบสนอง ตามข้อมูลที่คุณกำลังดูอยู่

> [!NOTE]
> ขณะนี้คุณไม่สามารถใช้กลไกนี้ในการฝังแอปที่เป็นแบบจำลองได้  

### <a name="details"></a>รายละเอียด

กระบวนงานต่อไปนี้แสดงวิธีการฝังแอปพื้นที่ทำงาน จาก Power Apps ลงในเว็บไคลเอ็นต์

1. ไปที่หน้าที่คุณต้องการฝังแอปพื้นที่ทำงาน หน้านี้จะเป็นหน้าเดียวกับหน้าที่มีข้อมูลใดที่จำเป็นต้องส่งผ่านไปยังแอปเหมือนกับข้อมูลป้อนเข้า
2. เปิดบานหน้าต่าง **เพิ่มแอปจาก Power Apps** :

    - คลิก **ตัวเลือก** แล้วจึงเลือก **ปรับหน้านี้ให้เป็นแบบส่วนตัว** ใต้เมนู **แทรก** เลือก **Power Apps** สุดท้ายให้เลือกขอบเขตที่คุณต้องการเพิ่มแอป หากคุณต้องการฝังแอปภายใต้ปุ่มเมนู Power Apps ให้เลือกบานหน้าต่างการดำเนินการ หากคุณต้องการฝังแอปลงบนหน้าโดยตรงให้เลือกแท็บ FastTab แผ่นหรือส่วนที่เหมาะสม (ถ้าคุณอยู่ในพื้นที่ทำงาน)
    - หากแอปเข้าถึงได้โดยใช้ปุ่มเมนู Power Apps อีกวิธีหนึ่งคุณสามารถคลิกปุ่มเมนู **Power Apps** ในบานหน้าต่างการดำเนินการมาตรฐาน แล้วเลือก **เพิ่มแอป**

3. กำหนดค่าแอปที่ฝังไว้:

    - ฟิลด์ **ชื่อ** บ่งชี้ข้อความแสดงปุ่มหรือแท็บที่จะมีแอปที่ฝังอยู่ บ่อยครั้งคุณอาจต้องการทำชื่อแอปในฟิลด์นี้ซ้ำ
    - ฟิลด์ **รหัสของแอป** บ่งชี้ถึงรหัสเฉพาะสากล (GUID) สำหรับแอปพื้นที่ทำงานที่คุณต้องการฝัง ในการดึงค่านี้ ให้หาแอปใน [make.powerapps.com](https://make.powerapps.com) จากนั้นหาในฟิลด์ **รหัสแอป** ภายใต้ **รายละเอียด**
    - สำหรับ **บริบทการป้อนข้อมูลสำหรับแอป** คุณสามารถเลือกฟิลด์ที่มีข้อมูลที่คุณต้องการส่งผ่านไปยังแอปเป็นข้อมูลป้อนเข้า ดูส่วนต่อไปในหัวข้อนี้ที่มีชื่อว่า [การสร้างแอปที่ใช้ประโยชน์ข้อมูลที่ส่งจากแอป Finance and Operations](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) สำหรับรายละเอียดเกี่ยวกับวิธีที่แอปสามารถเข้าถึงข้อมูลที่ส่งมาจากแอป Finance and Operations
    - เลือกขนาด **แอปพลิเคชัน** ที่ตรงกับชนิดของแอปที่คุณฝังไว้อยู่ เลือก **Thin** สำหรับแอปที่สร้างขึ้นสำหรับอุปกรณ์มือถือและ **Wide** สำหรับแอปที่สร้างขึ้นสำหรับแท็บเล็ต สิ่งนี้ทำให้แน่ใจว่ามีการจัดสรรพื้นที่เพียงพอสำหรับแอปที่ฝังไว้
    - FastTab **เอนทิตีทางกฎหมาย** ให้ความสามารถในการเลือกแอปที่พร้อมใช้งานสำหรับเอนทิตีทางกฎหมาย ค่าเริ่มต้น คือ การทำให้แอปสามารถเข้าถึงเอนทิตีทางกฎหมายได้ทั้งหมด ตัวเลือกนี้จะมีพร้อมใช้งานเมื่อคุณลักษณะ [มุมมองที่บันทึกไว้](saved-views.md) ถูกปิดใช้งาน 

4. หลังจากการยืนยันว่าการตั้งค่าคอนฟิกถูกต้อง คลิก **แทรก** เพื่อฝัง PowerApp บนหน้า คุณจะได้รับแจ้งให้รีเฟรชเบราว์เซอร์เพื่อดูแอปใบสั่งที่ฝังอยู่

## <a name="sharing-an-embedded-app"></a>การใช้แอปที่ฝังไว้ร่วมกัน

หลังจากคุณฝังแอปพื้นที่ทำงานลงในหน้าและยืนยันว่าแอปทำงานอย่างถูกต้องกับบริบทข้อมูลที่ส่งผ่านจากหน้านั้น คุณอาจต้องการแบ่งปันแอปกับผู้ใช้รายอื่นในระบบ เมื่อต้องการใช้แอปพื้นที่ทำงานที่ฝัง ให้ทำตามขั้นตอนต่อไปนี้

1. [แบ่งปันแอปพื้นที่ทำงาน](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) กับผู้ใช้ที่เหมาะสม เพื่อให้สามารถเข้าถึงแอปใน Power Apps 

2. ตรวจสอบให้แน่ใจว่าผู้ใช้ที่กำหนดการตั้งค่าเป็นแบบส่วนบุคคลที่เหมาะสม เพื่อให้แอปที่ฝังปรากฏขึ้นเมื่อผู้ใช้เหล่านั้นดูหน้าดังกล่าว คุณสามารถใช้อย่างใดอย่างหนึ่งต่อไปนี้:

    - ขอแนะนำ: ให้ใช้คุณลักษณะ [มุมมองที่บันทึกไว้](saved-views.md) เพื่อสร้างและเผยแพร่มุมมองที่มีแอปที่ฝัง วิธีการนี้ช่วยให้มั่นใจว่าผู้ใช้ทั้งหมดที่มีบทบาทความปลอดภัยที่เป็นเป้าหมายโดยมุมมองที่เผยแพร่ จะเห็นแอปในแอป Finance and Operations 
    - ถ้าคุณไม่มีคุณลักษณะมุมมองที่บันทึกไว้เปิดใช้งาน คุณสามารถตั้งค่าผู้ดูแลระบบให้ผลักการตั้งค่าเป็นแบบส่วนบุคคลที่มีแอปฝังกับผู้ใช้ทั้งหมดหรือชุดย่อยของผู้ใช้ทั้งหมดได้ อีกทางหนึ่งคือ คุณสามารถส่งออกการตั้งค่าเป็นแบบส่วนบุคคลของหน้าของคุณ และส่งไปยังผู้ใช้อย่างน้อยหนึ่งราย แต่ละผู้ใช้เหล่านั้นสามารถนำเข้าการตั้งค่าเป็นแบบส่วนบุคคลได้ แถบเครื่องมือการตั้งค่าส่วนบุคคลมีการดำเนินการที่ทำให้คุณสามารถส่งออกและนำเข้าการตั้งค่าส่วนบุคคล 
    
> [!NOTE]
> ถ้าแอปพื้นที่ทำงานถูกแชร์กับผู้ใช้ภายนอก ผู้ใช้เหล่านั้นไม่สามารถใช้แอปที่ฝังไว้ภายในแอป Finance and Operations ได้ อย่างไรก็ตาม ผู้ใช้สามารถเข้าถึงแอปได้โดยตรงภายใน Power Apps ผู้ใช้ภายนอกรวมถึงผู้ใช้และผู้ใช้ที่ไม่ได้เป็นสมาชิกของ Microsoft 365 Azure Directory ที่แแอป Finance and Operations ที่ปรับใช้

ดู [กำหนดประสบการณ์ผู้ใช้เป็นแบบส่วนบุคคล](personalize-user-experience.md) สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับความสามารถในการกำหนดประสบการณ์ผู้ใช้เป็นแบบส่วนบุคคลในผลิตภัณฑ์และวิธีการใช้

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>การสร้างแอปพื้นที่ทำงานที่ใช้ข้อมูลที่ส่งจากแอป Finance and Operations

เมื่อคุณสร้างแอปพื้นที่ทำงานที่จะฝังในแอป Finance and Operations ส่วนหนึ่งที่สำคัญของกระบวนการจะใช้ข้อมูลป้อนเข้าจากแอป Finance and Operations จากประสบการณ์การพัฒนา Power Apps ข้อมูลที่ป้อนเข้าที่ส่งผ่านจากแอป Finance and Operations สามารถเข้าถึงได้โดยใช้ตัวแปร **Param("EntityId")**

ตัวอย่างเช่น ในฟังก์ชั่น OnStart ของแอป คุณสามารถตั้งค่าข้อมูลป้อนเข้าจากแอป Finance and Operations เป็นตัวแปรดังนี้:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>การดูแอปพื้นที่ทำงาน

ในการดูแอปพื้นที่ทำงานที่ฝังในหน้าในแอป Finance and Operations เพียงแค่ไปที่หน้าที่มีแอปที่ฝังไว้ โปรดจำไว้ว่าแอปสามารถเข้าถึงได้โดยใช้ปุ่ม **Power Apps** ในบานหน้าต่างการดำเนินการมาตรฐาน อีกทางเลือกหนึ่ง แอปสามารถปรากฎบนหน้าโดยตรงเป็นแท็บใหม่ หรือแท็บด่วน หรือเบลด หรือเป็นส่วนใหม่ในพื้นที่ทำงาน เมื่อผู้ใช้ลองโหลดแอปบนหน้าครั้งแรก จะมีการแจ้งเตือนให้ล็อกอินเข้าสู่ระบบ ขั้นตอนนี้จะช่วยให้มั่นใจว่าผู้ใช้มีสิทธิการได้รับอนุญาตที่เหมาะสมที่จะใช้แอป

## <a name="editing-an-embedded-app"></a>การแก้ไขแอปที่ฝังไว้

หลังจากที่ฝังแอปลงบนหน้า คุณอาจต้องทำการเปลี่ยนแปลงบางอย่างในการกำหนดค่าของแอป ตัวอย่างเช่น คุณอาจต้องการแก้ไขป้ายชื่อที่เชื่อมโยงกับแอปที่ฝังอยู่หรือสร้างแอปรุ่นใหม่ และคุณจำเป็นต้องปรับปรุงรหัสแอปให้บ่งชี้ไปที่การปรับปรุงล่าสุด

ทำตามขั้นตอนเหล่านี้เพื่อแก้ไขการกำหนดค่าของแอปที่ฝังอยู่:

1. ไปที่บานหน้าต่าง **การแก้ไขแอป**

    - หากเข้าถึงแอปที่ฝังไว้ผ่านปุ่มเมนู Power Apps ให้คลิกขวาที่ปุ่มเมนู Power Apps และเลือก **ปรับให้เป็นแบบส่วนตัว** เลือกแอปที่คุณต้องการกำหนดค่าจากเมนูแบบหล่นลง **เลือกแอป** 
    - หากแอปที่ฝังไว้ปรากฏบนเพจโดยตรง ให้เลือก **ตัวเลือก** แล้วจึงเลือก **ปรับหน้านี้ให้เป็นแบบส่วนตัว** ใช้เครื่องมือ **เลือก** คลิกแอปที่ฝังไว้

2. ทำการปรับเปลี่ยนที่จำเป็นสำหรับการกำหนดค่าแอป แล้วคลิก **บันทึก** 

## <a name="removing-an-app"></a>ลบแอป

หลังจากที่ฝังแอปลงบนหน้า มีสองวิธีในการลบ หากจำเป็น:

- ไปที่บานหน้าต่าง **แก้ไขแอป** โดยใช้คำแนะนำก่อนหน้าจากส่วน [การแก้ไขแอปที่ฝังไว้](#editing-an-embedded-app) ในหัวข้อนี้ ยืนยันว่าบานหน้าต่างได้แสดงข้อมูลสำหรับแอปที่ฝังไว้ที่คุณต้องการลบ แล้วคลิกปุ่ม **ลบ** 
- เนื่องจากแอปที่ฝังอยู่นั้นถูกบันทึกเป็นข้อมูลส่วนบุคคล การล้างข้อมูลส่วนบุคคลในหน้าของคุณจะลบแอปที่ฝังไว้ในหน้านั้นด้วย โปรดทราบว่า การล้างการตั้งค่าส่วนบุคคลของเพจเป็นแบบถาวร และไม่สามารถยกเลิกได้ หากต้องการลบการตั้งค่าส่วนบุคคลของคุณในหน้า ให้เลือก **ตัวเลือก** แล้วจึง **ปรับหน้านี้ให้เป็นแบบส่วนตัว** และสุดท้ายคลิกปุ่ม **ล้างข้อมูล** หลังจากการรีเฟรชเบราเซอร์ของคุณ การกำหนดเป็นแบบส่วนบุคคลก่อนหน้านี้ทั้งหมดสำหรับหน้านี้จะถูกเอาออก ดู [กำหนดประสบการณ์ผู้ใช้นี้เป็นแบบส่วนบุคคล](personalize-user-experience.md) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการปรับปรุงหน้าโดยใช้การกำหนดเป็นแบบส่วนบุคคล

## <a name="appendix"></a>ภาคผนวก

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[นักพัฒนา] กำหนดที่ๆ สามารถฝังแอปไว้ได้

ตามค่าเริ่มต้น ผู้ใช้สามารถฝังแอปในหน้าใดก็ได้ภายใต้ปุ่มเมนู Power Apps หรือฝังโดยตรงบนหน้าในแท็บใหม่ FastTab แผ่นหรือเป็นส่วนใหม่ในพื้นที่ทำงาน อย่างไรก็ตามหากจำเป็น นักพัฒนาสามารถกำหนดค่าคุณลักษณะนี้เพื่ออนุญาตให้ฝังแอปเฉพาะบางหน้าได้โดยใช้วิธีการดังต่อไปนี้:

- **isPowerAppPersonalizationEnabled** – หากวิธีนี้คืนค่าเท็จสำหรับหน้าเฉพาะ ปุ่มเมนู Power Apps จะไม่ปรากฏขึ้น และผู้ใช้จะไม่สามารถฝังแอปที่ใดก็ได้ในหน้านี้รวมถึงที่เป็นแท็บ
- **isPowerAppTabPersonalizationEnabled** – หากวิธีนี้คืนค่าเท็จสำหรับหน้าเฉพาะ ผู้ใช้จะไม่สามารถฝังแอปโดยตรงบนหน้าที่เป็นแท็บ FastTab หรือส่วนรูปแบบพาโนรามา ผู้ใช้จะยังคงสามารถฝังแอปผ่านปุ่มเมนู Power Apps หากการฝังได้รับอนุญาตบนหน้านั้น

ตัวอย่างต่อไปนี้แสดงคลาสใหม่ที่มีสองวิธีที่จำเป็นในการกำหนดค่าที่ที่สามารถฝังแอปได้

```powerapps
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
