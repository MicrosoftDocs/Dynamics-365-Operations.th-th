---
title: สร้างกลไกจัดการการจัดการขนส่งใหม่
description: บทความนี้จะอธิบายวิธีการสร้างกลไกจัดการการจัดการการขนส่งใหม่ใน Dynamics 365 Supply Chain Management
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 627972ef6afb7551bb57821ded24183f8f335e9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857270"
---
# <a name="create-a-new-transportation-management-engine"></a>สร้างกลไกจัดการการจัดการขนส่งใหม่

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการสร้างกลไกจัดการการจัดการการขนส่งใหม่ใน Dynamics 365 Supply Chain Management 

กลไกจัดการการขนส่ง (TMS) กำหนดตรรกะที่ใช้ในการสร้าง และประมวลผลอัตราการขนส่งในการจัดการการขนส่ง Supply Chain Management มีกลไกจัดการหลายชนิดที่คํานวณพารามิเตอร์ต่างๆ เช่น อัตรา เวลาในการส่งต่อ และจํานวนของโซนที่จะถูกข้ามไปในระหว่างการส่งต่อ หัวข้อนี้อธิบายวิธีการใช้สภาพแวดล้อมการพัฒนา Microsoft Visual Studio ร่วมกับเครื่องมือการพัฒนา Supply Chain Management เพื่อสร้างและปรับใช้กลไกจัดการ TMS ใหม่ จากนั้นวิธีตั้งค่ากลไกจัดการในการดําเนินงาน สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกลไกจัดการ โปรดดูที่ [กลไกจัดการการจัดการการขนส่ง](transportation-management-engines.md)

## <a name="create-a-new-tms-engine"></a>สร้างกลไกจัดการ TMS ใหม่

ส่วนนี้อธิบายวิธีการสร้างไลบรารีคลาสที่มีการใช้งานกลไกจัดการ TMS และวิธีอ้างอิงจาก Supply Chain Management

1. เมื่อต้องการปรับใช้กลไกจัดการใหม่ของคุณ คุณต้องมีแบบจำลองที่มีกลไกจัดการ บนเมนู **Dynamics 365** &gt; **การจัดการแบบจำลอง** ให้คลิก **สร้างแบบจำลอง** เพื่อสร้างแบบจำลองใหม่ ในหน้าแรกของวิซาร์ด **สร้างแบบจำลอง** ให้ตั้งชื่อแบบจำลอง **TMSEngines** 

   [![การสร้างแบบจำลอง](./media/012.png)](./media/012.png)

2. ในหน้าถัดไป ให้เลือก **สร้างแพคเกจใหม่** 

   [![สร้างแพคเกจใหม่](./media/021.png)](./media/021.png)

3. ในหน้าถัดไป ให้เลือกแบบจำลอง **ApplicationSuite** ที่จะอ้างอิง (แบบจำลอง **ApplicationPlatform** ที่เลือกไว้ล่วงหน้าแล้ว) 

   [![การเลือกแบบจำลองที่จะอ้างอิง](./media/032.png)](./media/032.png)

4. ในหน้าถัดไป ให้คลิก **เสร็จสิ้น** เพื่อยืนยันการสร้างแบบจำลองใหม่ 

   [![การสร้างแบบจำลองเสร็จสมบูรณ์](./media/042.png)](./media/042.png)

5. ในโซลูชันใหม่ ให้สร้างโครงการ Supply Chain Management ใหม่ และตั้งชื่อโครงการ **TMSThirdParty** ในคุณสมบัติของโครงการ ให้ตั้งค่าแบบจำลองของโครงการเป็น **TMSEngines**
6. เพิ่ม C\# ไลบรารีคลาสใหม่ลงในโซลูชันของคุณ และตั้งชื่อเป็น **ThirdPartyTMSEngines**
7. ในโครงการ ThirdPartyTMSEngines ให้เพิ่มการอ้างอิงไปยัง แอสเซมบลีเฉพาะเกี่ยวกับ Supply Chain Management:
   -   แอสเซมบลีแอปพลิเคชันที่เปิดใช้งานชนิด X++ ที่จะอ้างอิง ไม่พบแอสเซมบลีเหล่านี้ในที่ตั้งต่อไปนี้ \[รากของแพคเกจ\] คือพาธของที่ตั้งที่มีการจัดวางแอสเซมบลีที่จัดวางทั้งหมด เช่น C:\\แพคเกจ

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   แอสเซมบลีกรอบงานที่เปิดใช้งานการเข้าถึงข้อมูล LINQ และฟังก์ชันเสริม การรวบรวมเหล่านี้ทั้งหมดสามารถพบได้ใน \[รากของแพคเกจ\]\\ช่องเก็บ

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   แอสเซมบลี TMS หลัก (ซึ่งมีกลไกจัดการ) และแอสเซมบลีพื้นฐาน TMS (ซึ่งมีตัวช่วยเหลือ ค่าคงที่ นิยามคลาสการโอนย้ายข้อมูล และอื่นๆ) ไม่พบแอสเซมบลีเหล่านี้ในที่ตั้งต่อไปนี้

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. เปลี่ยนชื่อ C\# คลาส ที่สร้างขึ้นโดยอัตโนมัติในโครงการ ThirdPartyTMSEngine เป็น **SampleRatingEngine**
9. ใช้กลไกจัดการ เนื่องจากเราได้สร้างกลไกจัดการอัตราในตัวอย่างนี้ เรารับมาจากคลาสพื้นฐานที่กลไกจัดการอัตรา คลาสพื้นฐานจะใช้อินเทอร์เฟสกลไกจัดการอัตราส่วนใหญ่ (**TMSFwkIRateEngine**) เราเพิ่งใช้วิธีการอัตรา เพื่อให้ตัวอย่างนี้ง่าย เราจะให้วิธีนี้ลงทะเบียนอัตราที่มีรหัสแบบฮาร์ด 100 คุณสามารถสร้างกลไกจัดการที่ใช้อินเทอร์เฟสกลไกจัดการใดๆ เช่น **TMSFwkIAccessorialEngine** อินเทอร์เฟสกลไกจัดการทั้งหมดถูกกําหนดใน X++

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. สร้างโซลูชัน
11. เพิ่มการอ้างอิงใหม่ในโครงการ TMSThirdParty การอ้างอิงควรชี้ไปที่โครงการ ThirdPartyTMSEngines เมื่อคุณดำเนินการเสร็จสิ้นแล้ว โซลูชันของคุณควรมีลักษณะเช่นนี้ 

    [![โซลูชัน ซึ่งรวมถึงการอ้างอิงถึงโครงการ TMSThirdParty](./media/052.png)](./media/052.png)

12. สร้างโซลูชัน ตรวจสอบว่าไลบรารีใหม่ปรากฏในโหนด **การอ้างอิง** ใน Application Explorer หรือไม่ 

    [![ไลบรารีใหม่ในโหนดการอ้างอิงของ Application Explorer](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>ปรับใช้กลไกจัดการ TMS เป็นแพคเกจ

วิธีการหนึ่งในการปรับใช้กลไกจัดการ TMS ของบุคคลที่สาม คือผ่านแพคเกจการปรับใช้ วิธีการนี้ได้รับการแนะนำให้ใช้ในสภาพแวดล้อมการทำงานจริง ในสภาพแวดล้อมการพัฒนา คุณสามารถคัดลอกแอสเซมบลีได้ด้วยตนเอง ตามที่อธิบายไว้ในส่วนถัดไป "ตั้งค่ากลไกจัดการ TMS ใน Supply Chain Management" ในการปรับใช้กลไกจัดการเป็นแพคเกจ ให้ทำตามขั้นตอนเหล่านี้

1. บนเมนู **Dynamics 365** &gt; **ปรับใช้** ให้คลิก <strong>สร้างแพคเกจการปรับใช้</strong>
2. ในกล่องโต้ตอบ **สร้างแพคเกจการปรับใช้** ให้เลือกแบบจำลอง TMSEngines และป้อนพาธที่คุณต้องการจัดเก็บไฟล์แพคเกจของคุณ 

   [![การเลือกแบบจำลอง TMSEngines](./media/071.png)](./media/071.png)

3. ตอนนี้คุณสามารถปรับใช้แพคเกจไปยังสภาพแวดล้อมเป้าหมายได้ สำหรับบทช่วยสอน ให้ดู [ติดตั้งแพคเกจที่ปรับใช้ได้](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md)

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>ตั้งค่ากลไกจัดการ TMS ใน Supply Chain Management

ส่วนนี้อธิบายวิธีการตั้งค่า Supply Chain Management เพื่อใช้กลไกจัดการ TMS และแสดงวิธีการใช้กลไกจัดการใหม่ที่เราได้สร้างขึ้นในการแสดงข้อมูลอัตรา ตัวอย่างในส่วนนี้ใช้บริษัทข้อมูลสาธิต USMF

1. สร้างกลไกจัดการใหม่ตามที่อธิบายไว้ในส่วน "สร้างกลไกจัดการ TMS ใหม่"
2. สร้างโซลูชันของคุณ
3. คัดลอกแอสเซมบลีผลลัพธ์ไปยังที่ตั้งฐานสองของของเซิร์ฟเวอร์ Supply Chain Management ช่องเก็บ \[AOSWebRoot \] **หมายเหตุ:** ขั้นตอนนี้เกี่ยวข้องเฉพาะในสภาพแวดล้อมการพัฒนาเท่านั้น ในสภาพแวดล้อมการทำงานจริง คุณควรปรับใช้ผ่านแพคเกจการปรับใช้ สำหรับคำแนะนำ ให้ดูที่ส่วนก่อนหน้านี้ "ปรับใช้กลไกจัดการ TMS เป็นแพคเกจ"
4. ใน Supply Chain Management ในหน้า **กลไกจัดการอัตรา** ให้สร้างกลไกการจัดอันดับใหม่ กลไกจัดการควรชี้ไปที่แอสเซมบลีกลไกจัดการที่ผลิตโดยการสร้างไลบรารีคลาสกลไกจัดการและคลาสกลไกจัดการที่คุณใช้งาน 

   [![การสร้างกลไกจัดการการจัดอันดับใหม่ในหน้ากลไกจัดการอัตรา](./media/081.png)](./media/081.png)

5. สร้างผู้ขนส่งสินค้าที่ใช้กลไกจัดการอัตราตัวอย่าง เนื่องจากกลไกจัดการของเราไม่ได้ใช้ข้อมูลใดๆ คุณจึงไม่ต้องกําหนดต้นแบบอัตรา 

   [![การสร้างผู้ขนส่งสินค้าใหม่](./media/092.png)](./media/092.png)

6. บนหน้า **จัดอันดับเวิร์กเบนช์กระบวนการผลิต** ให้คลิก **จัดอันดับร้านค้า** คุณควรเห็นอัตรา 100.00 จาก SampleCarrier ดังที่แสดงในภาพหน้าจอต่อไปนี้ ในตัวอย่างนี้ เราคือการแสดงข้อมูลอัตราของเส้นทางจากคลังสินค้า 24 ไปยังลูกค้า US-004 แต่เนื่องจากอัตรามีรหัสแบบฮาร์ด คุณจะเห็นอัตรา 100.00 เสมอ

   [![จัดอันดับเวิร์กเบนช์กระบวนการผลิต](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>เคล็ดลับและเทคนิค

- ถ้าคุณใช้เครื่องมือการพัฒนาสำหรับ Supply Chain Management การเพิ่มโครงการใหม่ลงในโซลูชันของคุณก็จะเป็นประโยชน์ ถ้าคุณตั้งค่าโครงการนี้เป็นโครงการเริ่มต้นของคุณและเริ่มต้นรอบเวลาการดีบัก คุณสามารถดีบักทั้งรหัส X++ และ C\# ในรอบเวลาการดีบักเดียวกัน
- ทุกครั้งที่คุณเปลี่ยนแปลงและคอมไพล์โครงการ ThirdPartyTMSEngines ของคุณใหม่ คุณต้องคัดลอกแอสเซมบลีผลลัพธ์ไปยังที่ตั้งฐานสอง หรือปรับใช้ผ่านแพคเกจการปรับใช้ด้วยตนเอง มิฉะนั้น คุณอาจรันโดยใช้แอสเซมบลีเก่า
- หลังจากที่คุณดําเนินการ TMS เฉพาะ ใน Supply Chain Management แล้ว กระบวนการของผู้ปฏิบัติงาน Internet Information Services (IIS) อาจล็อคแอสเซมบลี ThirdPartyTMSEngines เพื่อให้ไม่สามารถอัปเดตแอสเซมบลีได้ ในกรณีนี้ ให้เริ่มกระบวนการ w3svc ใหม่

### <a name="whitepaper"></a>เอกสารทางเทคนิค

สำหรับข้อมูลเพิ่มเติม ดาวน์โหลดเอกสารทางเทคนิคต่อไปนี้ (ซึ่งเขียนขึ้นเพื่อสนับสนุน AX2012 แต่ยังคงใช้สำหรับ Dynamics 365 Supply Chain Management)

- [การดําเนินการและการใช้งานกลไกจัดการการจัดการการขนส่ง](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]