---
title: การจัดส่งพัสดุขนาดเล็ก
description: บทความนี้แสดงข้อมูลทั่วไปเกี่ยวกับคุณลักษณะการจัดส่งพัสดุขนาดเล็ก คุณลักษณะนี้ช่วยให้ Microsoft Dynamics 365 Supply Chain Management สามารถส่งรายละเอียดเกี่ยวกับคอนเทนเนอร์ที่บรรจุให้บริษัทขนส่ง แล้วได้รับป้ายชื่อการจัดส่ง อัตราการจัดส่ง และหมายเลขการติดตามย้อนกลับจากบริษัทขนส่งนั้น
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b2adde2b81ed881a3c81193a2220fbe569069c7c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336169"
---
# <a name="small-parcel-shipping"></a>การจัดส่งพัสดุขนาดเล็ก

[!include [banner](../../includes/banner.md)]

คุณลักษณะการจัดส่งพัสดุขนาดเล็ก (SPS) ช่วยให้ Microsoft Dynamics 365 Supply Chain Management สามารถโต้ตอบกับบริษัทขนส่งโดยตรงโดยให้กรอบงานการสื่อสารผ่าน API ของบริษัทขนส่ง ฟังก์ชันนี้มีประโยชน์เมื่อคุณส่งใบสั่งขายแต่ละใบผ่านในเชิงพาณิชย์ แทนการใช้การจัดส่งคอนเทนเนอร์หรือการขนส่งน้อยกว่าที่มีการบรรทุก (LTL)

คุณลักษณะ SPS จะโต้ตอบกับบริษัทขนส่งของคุณผ่าน *กลไกจัดการอัตรา* เฉพาะ องค์กรของคุณต้องพัฒนากลไกจัดการอัตรานี้โดยร่วมมือกับบริการฮับบริษัทขนส่งหรือบริษัทขนส่งของคุณ กลไกจัดการอัตรานี้ช่วยให้ Supply Chain Management สามารถส่งรายละเอียดเกี่ยวกับคอนเทนเนอร์ที่บรรจุให้บริษัทขนส่งของคุณ แล้วได้รับป้ายชื่อการจัดส่ง อัตราการจัดส่ง และหมายเลขการติดตามย้อนกลับจากบริษัทขนส่งนั้น

อัตราค่าจัดส่งที่ส่งคืนจะถูกบวกเพิ่มเข้าไปในใบสั่งขายที่เกี่ยวข้องเป็นค่าธรรมเนียมเบ็ดเตล็ด จากนั้นคุณสามารถพิมพ์ป้ายชื่อการจัดส่งที่ส่งคืนโดยอัตโนมัติได้โดยใช้เครื่องพิมพ์ Javabra Programming Language (ZPL) และใช้กับการจัดส่งสินค้า บริษัทขนส่งจะสแกนป้ายชื่อการจัดส่งนี้เมื่อเบิกบรรจุภัณฑ์ที่คลังสินค้าของคุณ

## <a name="prepare-your-system-to-support-sps"></a>การจัดเตรียมระบบของคุณเพื่อสนับสนุน SPS

ก่อนที่คุณจะสามารถเริ่มใช้ฟังก์ชัน SPS ได้ คุณต้องเปิดคุณลักษณะ SPS ในการจัดการคุณลักษณะ เพิ่มกลไกจัดการอัตราของคุณ และตั้งค่าโมดูล **การจัดการการขนส่ง** และ **การจัดการคลังสินค้า** เพื่อสนับสนุนคุณลักษณะนี้

### <a name="turn-the-sps-feature-on-or-off"></a>เปิดหรือปิดคุณลักษณะ SPS

การใช้คุณลักษณะนี้ ต้องเปิดคุณลักษณะนี้ในระบบของคุณก่อน เริ่มจาก Supply Chain Management เวอร์ชัน 10.0.29 คุณลักษณะนี้เป็นแบบบังคับ และไม่สามารถปิดได้ ถ้าคุณเรียกใช้รุ่นที่เก่ากว่า 10.0.29 ผู้ดูแลระบบสามารถเปิดหรือปิดฟังก์ชันนี้ได้โดยค้นหาคุณลักษณะ *การจัดส่งพัสดุขนาดเล็ก* ในพื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="deploy-and-set-up-rate-engines"></a>ปรับใช้และตั้งค่ากลไกจัดการอัตรา

Supply Chain Management ไม่มีกลไกจัดการอัตราใดๆ คุณต้องได้รับหรือสร้างกลไกจัดการอัตราใด ๆ ที่คุณต้องการ แล้วเพิ่มกลไกจัดการอัตราเหล่านั้นลงในระบบของคุณ อย่างไรก็ตาม Microsoft มีกลไกจัดการอัตราสาธิตที่คุณสามารถใช้ในการทดสอบได้

#### <a name="download-and-deploy-the-demo-rate-engine"></a>ดาวน์โหลดและปรับใช้กลไกจัดการอัตราสาธิต

ให้ดำเนินการตามขั้นตอนต่อไปนี้เพื่อรับกลไกจัดการอัตราสาธิต

1. บน GitHub ให้ดาวน์โหลด [ไลบรารีแบบไดนามิกลิงค์ (DLL) ของกลไกจัดการอัตราสาธิต](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS)
1. บนเซิร์ฟเวอร์ Supply Chain Management ของคุณ ให้บันทึก DLL ในโฟลเดอร์ **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**

#### <a name="create-and-deploy-functional-rate-engines"></a>สร้างและปรับใช้กลไกจัดการอัตราฟังก์ชัน

หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างและใช้งานกลไกจัดการอัตราฟังก์ชัน เพื่อให้สามารถใช้กลไกจัดการอัตราฟังก์ชันได้ในสภาพแวดล้อมการผลิตหรือการทดสอบ โปรดดูที่บทความต่อไปนี้

- [สร้างกลไกจัดการการจัดการขนส่งใหม่](../transportation/create-new-transportation-management-engine.md)
- [ตั้งค่ากลไกจัดการการจัดการขนส่ง](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างกลไกจัดการอัตรา SPS โปรดดูที่ประกาศบล็อกต่อไปนี้: [การจัดส่งพัสดุขนาดเล็ก: วิธีเพิ่มฟังก์ชันการจัดส่งพัสดุขนาดเล็กใน Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5)

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>การตั้งค่ากลไกจัดการอัตราใน Supply Chain Management

หลังจากที่คุณได้สร้างและปรับใช้กลไกจัดการอัตราของ SPS แล้ว ให้ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่า

1. ไปที่ **การจัดการการขนส่ง \> \> กลไกจัดการ \> กลไกจัดการอัตรา**
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด
1. บนแถวใหม่ ให้กำหนดฟิลด์ดังต่อไปนี้:

    - **กลไกจัดการการจัดอันดับ** – ป้อนชื่อเฉพาะของกลไกจัดการอัตรา ถ้าคุณจะใช้กลไกจัดการอัตราสาธิต ให้ป้อน *กลไกจัดการอัตราสาธิต*
    - **ชื่อ** – ป้อนคำอธิบายย่อเกี่ยวกับกลไกจัดการอัตรา ถ้าคุณจะใช้กลไกจัดการอัตราสาธิต ให้ป้อน *กลไกจัดการอัตราสาธิต*
    - **รหัสข้อมูลเมตาของการจัดอันดับ** – เลือกข้อมูลพื้นฐานที่ควรใช้เพื่อคํานวณอัตราของคุณ ตัวอย่างเช่น อัตราของคุณอาจมีการคํานวณตามระยะทาง ถ้าคุณกำลังใช้กลไกจัดการอัตราสาธิต คุณสามารถปล่อยฟิลด์นี้ให้ว่างไว้ได้
    - **แอสเซมบลีกลไกจัดการ** – ป้อนชื่อไฟล์ของแพคเกจ DLL ที่คุณจัดวาง ถ้าคุณจะใช้กลไกจัดการอัตราสาธิต ให้ป้อน *TMSSmallParcelShippingEngine.dll*
    - **คลาสกลไกจัดการ** – ป้อนชื่อคลาสที่สร้างขึ้นสถาปนากลไกจัดการอัตราของคุณ ถ้าคุณจะใช้กลไกจัดการอัตราสาธิต ให้ป้อน *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*

## <a name="example-scenario"></a>ตัวอย่างสถานการณ์จำลอง

สถานการณ์นี้แสดงวิธีการตั้งค่าและใช้ SPS หลังจากที่คุณได้จัดเตรียมระบบของคุณตามที่อธิบายไว้ก่อนหน้านี้ในบทความนี้ สถานการณ์นี้จะใช้กลไกจัดการอัตราสาธิตที่ได้กล่าวถึงก่อนหน้านี้

### <a name="make-demo-data-available"></a>ทำให้ข้อมูลสาธิตพร้อมใช้งาน

เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้เรกคอร์ดและค่าสาธิตที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/fin-ops/get-started/demo-data.md) มาตรฐาน นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น

### <a name="set-up-the-scenario"></a>ตั้งค่าสถานการณ์จำลอง

ตัวอย่างเช่น คุณต้องมีบริษัทขนส่งสาธิต กลุ่มบริษัทขนส่ง นโยบายการบรรจุ และโปรไฟล์การบรรจุ ส่วนย่อยต่อไปนี้อธิบายวิธีการจัดเตรียมเรกคอร์ดที่สถานการณ์นี้ต้องการ ในสถานการณ์การผลิต โดยทั่วไป กระบวนการตั้งค่าจะคล้ายคลึงกับกระบวนการที่อธิบายไว้ที่นี่ อย่างไรก็ตาม คุณจะตั้งค่าที่แตกต่างกัน

#### <a name="set-up-carriers"></a>ตั้งค่าบริษัทขนส่ง

ให้ดำเนินการตามขั้นตอนเหล่านี้เพื่อตั้งค่าบริษัทขนส่ง

1. ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ผู้ขนส่ง \> ผู้ขนส่งสินค้า**
1. ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อเพิ่มบริษัทขนส่ง
1. บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:

    - **บริษัทขนส่ง:** *บริษัทขนส่งสาธิต*
    - **ชื่อ:** *บริษัทขนส่งสาธิต*
    - **โหมด:** *ภาคพื้นดิน*

1. บน FastTab **ภาพรวม** ให้ตั้งค่าค่าต่อไปนี้:

    - **การเรียกใช้งานบริษัทขนส่ง:** *ใช่*
    - **การเรียกใช้งานการจัดอันดับบริษัทขนส่ง:** *ใช่*

1. บนแท็บด่วน **บริการ** ให้เลือก **สร้าง** เพื่อเพิ่มบริการไปยังกริด
1. ให้ตั้งค่าค่าต่อไปนี้สำหรับบริการใหม่:

    - **บริการบริษัทขนส่ง:** *บริการบริษัทขนส่งสาธิต*
    - **ชื่อ:** *บริการบริษัทขนส่งสาธิต*
    - **วิธีการขนส่ง:** *ภาคพื้นดิน*

    ป้อนค่าตามต้องการสำหรับฟิลด์อื่น ๆ ทั้งหมดตามจำเป็น (เมื่อคุณบันทึกเรกคอร์ดบริษัทขนส่งใหม่ วิธีการจัดส่งใหม่จะถูกสร้างขึ้น และฟิลด์ **วิธีการจัดส่ง** จะถูกตั้งค่าโดยอัตโนมัติ)

1. บนแท็บด่วน **โปรไฟล์การจัดอันดับ** เลือก **สร้าง** เพื่อเพิ่มโปรไฟล์การจัดอันดับไปยังตาราง
1. ให้ตั้งค่าค่าต่อไปนี้สำหรับโปรไฟล์ใหม่:

    - **โปรไฟล์การจัดอันดับ:** *บริการบริษัทขนส่งสาธิต*
    - **ชื่อ:** *บริการบริษัทขนส่งสาธิต*
    - **กลไกจัดการอัตรา:** *กลไกจัดการอัตราสาธิต*

    ป้อนค่าตามต้องการสำหรับฟิลด์อื่น ๆ ทั้งหมดตามจำเป็น

1. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าบริษัทขนส่ง ให้ดูที่ [ตั้งค่าบริษัทขนส่ง](../transportation/tasks/set-up-shipping-carriers.md)

#### <a name="set-up-carrier-service-accounts"></a>ตั้งค่าบัญชีบริการบริษัทขนส่ง

ให้ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าบัญชีบริการบริษัทขนส่ง

1. ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> การจัดอันดับ \> บัญชีบริการบริษัทขนส่ง**
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มบัญชีบริการบริษัทขนส่ง
1. ให้ตั้งค่าค่าต่อไปนี้สำหรับบัญชีใหม่:

    - **บริษัทขนส่ง:** *บริษัทขนส่งสาธิต*
    - **บริการบริษัทขนส่ง:** *บริการบริษัทขนส่งสาธิต*
    - **หมายเลขบัญชีลูกค้าของบริษัทขนส่ง:** หมายเลขบัญชีลูกค้าของบริษัทขนส่งที่ใช้ตรวจสอบความถูกต้องและพิสูจน์ตัวจริงของการเชื่อมต่อกับบริษัทขนส่ง บริษัทขนส่งของคุณจะระบุค่านี้ ถ้าคุณใช้บริการสาธิต คุณสามารถป้อนค่าหนึ่ง ๆ ได้
    - **ไซต์:** *6*
    - **คลังสินค้า:** *62*

    > [!NOTE]
    > บ่อยครั้งที่ค่า **หมายเลขบัญชีลูกค้าของบริษัทขนส่ง** เป็นค่าเดียวที่ต้องใช้ในการตรวจสอบความถูกต้องการเชื่อมต่อ อย่างไรก็ตาม ถ้าบริษัทขนส่งของคุณต้องการพารามิเตอร์การรับรองความถูกต้องเพิ่มเติม องค์กรของคุณควรเลือกเองหน้านี้เพื่อเพิ่มฟิลด์พิเศษตามความเหมาะสม

#### <a name="set-up-a-container-packing-policy"></a>ตั้งค่านโยบายการบรรจุคอนเทนเนอร์

ให้ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่านโยบายการบรรจุคอนเทนเนอร์

1. ถ้าคุณยังไม่ได้ตั้งค่านิยามเครื่องพิมพ์ ZPL ให้ใช้แอปพลิเคชันตัวแทนการกำหนดเส้นทางเอกสารเพื่อตั้งค่า สำหรับข้อมูลเพิ่มเติม ให้ดู [ภาพรวมการพิมพ์เอกสาร](../../fin-ops-core/dev-itpro/analytics/print-documents.md) และบทความที่เกี่ยวข้อง
1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คอนเทนเนอร์ \> นโยบายการบรรจุคอนเทนเนอร์**
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มนโยบายการบรรจุคอนเทนเนอร์
1. ในส่วนหัวของนโยบายใหม่ ให้ตั้งค่าค่าต่อไปนี้:

    - **นโยบายการบรรจุคอนเทนเนอร์:** *นโยบายการบรรจุสาธิต*
    - **คำอธิบาย:** ป้อนคำอธิบายเกี่ยวกับนโยบาย

1. บน FastTab **ภาพรวม** ให้ตั้งค่าค่าต่อไปนี้:

    - **คลังสินค้า:** *62*
    - **สถานที่เริ่มต้นในการจัดส่งขั้นสุดท้าย:** *Baydoor*
    - **น้ำหนักต่อหน่วย:** *กก.*
    - **นโยบายการปิดคอนเทนเนอร์:** *การนำออกใช้โดยอัตโนมัติ*
    - **นโยบายการปล่อยคอนเทนเนอร์:** *พร้อมใช้งานที่สถานที่จัดส่งสุดท้าย*

1. บนแท็บด่วน **รายการคอนเทนเนอร์** ให้ตั้งค่าต่อไปนี้:

    - **รายการอัตโนมัติเมื่อปิดคอนเทนเนอร์:** *ใช่*
    - **ข้อกำหนดรายการของคอนเทนเนอร์:** *การจัดการการขนส่ง*
    - **พิมพ์เนื้อหาของคอนเทนเนอร์:** *ไม่ใช่*

1. บนแท็บด่วน **การพิมพ์ป้ายชื่อบริษัทขนส่ง** ให้ตั้งค่าต่อไปนี้:

    - **พิมพ์ป้ายชื่อการจัดส่งคอนเทนเนอร์:** *เสมอ*
    - **ชื่อเครื่องพิมพ์:** ชื่อของเครื่องพิมพ์ ZPL ที่ควรพิมพ์ป้ายชื่อการจัดส่ง

#### <a name="set-up-a-packing-profile"></a>ตั้งค่าโพรไฟล์การบรรจุ

ให้ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าโปรไฟล์การบรรจุ

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การบรรจุ \> โปรไฟล์การบรรจุ**
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **ใหม่** เพื่อเพิ่มโปรไฟล์การบรรจุไปยังกริด
1. ให้ตั้งค่าค่าต่อไปนี้สำหรับโปรไฟล์ใหม่:

    - **รหัสโปรไฟล์การบรรจุ:** *โปรไฟล์การบรรจุสาธิต*
    - **คำอธิบาย:** ป้อนคำอธิบายเกี่ยวกับโปรไฟล์
    - **นโยบายการบรรจุคอนเทนเนอร์:** *นโยบายการบรรจุสาธิต*
    - **โหมดรหัสคอนเทนเนอร์:** *อัตโนมัติ*
    - **ชนิดคอนเทนเนอร์:** *กล่องขนาดเล็ก*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>การตั้งค่าลูกค้าเพื่อใช้บริษัทขนส่ง SPS

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าลูกค้าเพื่อให้สามารถใช้บริษัทขนส่งที่คุณสร้างขึ้นได้

1. ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**
1. ในตารางนี้ ให้ค้นหาและเลือกลูกค้า *US-027*
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **ทั่วไป** ในกลุ่ม **การตั้งค่า** ให้เลือก **บัญชีลูกค้าของบริษัทขนส่ง**
1. บนหน้า **หมายเลขบัญชีลูกค้าของบริษัทขนส่ง** ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อเพิ่มบัญชีลงในกริด
1. ให้ตั้งค่าค่าต่อไปนี้สำหรับบัญชีใหม่:

    - **บริษัทขนส่ง:** *บริษัทขนส่งสาธิต*
    - **หมายเลขบัญชีลูกค้าของบริษัทขนส่ง:** *12345* (ค่าไม่สําคัญต่อสถานการณ์นี้ แต่ค่าจะอ้างอิงถึงในส่วนถัดไป)

### <a name="go-through-the-example-scenario"></a>ผ่านสถานการณ์ตัวอย่าง

หลังจากที่คุณตั้งค่าข้อมูลตัวอย่างทั้งหมดตามที่อธิบายไว้ในส่วนก่อนหน้านี้แล้ว คุณพร้อมแล้วที่จะผ่านสถานการณ์ดังกล่าว

#### <a name="create-a-sales-order-and-process-the-work"></a>สร้างผลใบสั่งขายและประมวลผลงาน

ให้ปฏิบัติตามขั้นตอนเหล่านี้ในการสร้างใบสั่งขาย

1. ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**
1. เลือก **สร้าง** เพื่อสร้างใบสั่งขาย
1. ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-027*
1. เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ
1. มีการเปิดใบสั่งขายใหม่ บนแท็บด่วน **ส่วนหน้าของใบสั่งขาย** ให้ตั้งค่าฟิลด์ **หมายเลขบัญชีลูกค้าของบริษัทขนส่ง** เป็นค่าที่คุณเลือกไว้ของลูกค้ารายนี้ก่อนหน้านี้ (*12345*)
1. ในส่วน **บรรทัดใบสั่งขาย** ให้เพิ่มรายการขาย และตั้งค่าต่อไปนี้ให้กับบรรทัดใบสั่งขาย

    - **หมายเลขสินค้า:** *A0002*
    - **ปริมาณ:** *1*
    - **ไซต์:** *6*
    - **คลังสินค้า:** *62*

1. สลับไปยังมุมมอง **ส่วนหัว**
1. บนแท็บด่วน **การจัดส่ง** ให้ตั้งค่าค่าต่อไปนี้:

    - **บริษัทขนส่ง:** *บริษัทขนส่งสาธิต*
    - **บริการบริษัทขนส่ง:** *บริการบริษัทขนส่งสาธิต*

1. สลับกลับไปยังมุมมอง **รายการ** หากคุณได้รับพร้อมต์ให้อัพเดตวิธีการจัดส่งรายการขาย ให้เลือก **ใช่**
1. ในส่วน **บรรทัดใบสั่งขาย** ให้เลือกบรรทัดใบสั่งที่คุณตั้งค่าไว้ก่อนหน้านี้ แล้วเลือก **สินค้าคงคลัง \> การจอง**
1. บนหน้า **การจอง** ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า
1. ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**

    งานถูกสร้างเพื่อย้ายสินค้าจากสถานที่เบิกสินค้าไปยังสถานีบรรจุ

1. ในส่วน **รายการในใบสั่งขาย** ให้เลือก **คลังสินค้า \> รายละเอียดการจัดส่ง**
1. บนหน้า **รายละเอียดการจัดส่ง** ให้บันทึกรหัสการจัดส่ง คุณจะต้องใช้บรรจุภัณฑ์เมื่อคุณบรรจุสินค้าที่สถานีบรรจุสินค้า
1. ปิดหน้า **รายละเอียดการจัดส่ง** เพื่อส่งคืนไปยังใบสั่งขาย
1. จดบันทึกหมายเลขใบสั่งขาย แล้วไปที่ **การจัดการคลังสินค้า \> งาน \> งานทั้งหมด**
1. ใช้หมายเลขใบสั่งขายเพื่อค้นหาและเลือกงานที่สร้างขึ้นแล้วของใบสั่ง
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **งาน** เลือก **ทำงานให้เสร็จสมบูรณ์**
1. ในหน้า **การเสร็จสมบูรณ์ของงาน** ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้ จากนั้น ในบานหน้าต่างการดำเนินการ เลือก **ตรวจสอบความถูกต้องของงาน**
1. หากงานผ่านการตรวจสอบความถูกต้อง ให้เลือก **ทำงานให้เสร็จสมบูรณ์** บนบานหน้าต่างการดำเนินการ

    งานถูกกําหนดเป็นเสร็จสมบูรณ์แล้วเพื่อจําลองการย้ายสินค้าไปยังสถานีบรรจุสินค้า

#### <a name="pack-the-shipment"></a>การบรรจุการจัดส่ง

ให้ทำตามขั้นตอนเหล่านี้เพื่อบรรจุการจัดส่ง

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> ผู้ปฏิบัติงาน** และตรวจสอบให้แน่ใจว่าบัญชีผู้ใช้ของคุณเชื่อมโยงกับบัญชีผู้ปฏิบัติงานในการจัดการคลังสินค้า
1. ไปที่ **การจัดการคลังสินค้า \> การเบิกสินค้าและการบรรจุลงตู้บรรจุสินค้า \> บรรจุ**
1. ในกล่องโต้ตอบ **เลือกสถานีบรรจุ** ให้ตั้งค่าต่อไปนี้:

    - **ไซต์:** *6*
    - **คลังสินค้า:** *62*
    - **สถานที่:** *บรรจุ*
    - **รหัสโปรไฟล์การบรรจุ:** *โปรไฟล์การบรรจุสาธิต*

1. เลือก **ตกลง**
1. หน้า **บรรจุ** ปรากฏขึ้น ในสถานการณ์สถานการณ์การผลิต ผู้ปฏิบัติงานจะสแกนป้ายทะเบียนหรือรหัสการจัดส่ง อย่างไรก็ตาม ในสถานการณ์นี้ ให้เปิดหน้า **การจัดส่งสินค้าทั้งหมด** และค้นหาหมายเลขการจัดส่งของการจัดส่งที่คุณเพิ่งสร้างขึ้น แล้วป้อนค่านี้ในฟิลด์ **ป้ายทะเบียนหรือการจัดส่ง** บนหน้า **บรรจุ** หรือป้อนรหัสการจัดส่งที่คุณจดบันทึกไว้ก่อนหน้านี้
1. บนหน้าต่างการดำเนินการ เลือก **คอนเทนเนอร์ใหม่**
1. กล่องโต้ตอบที่ปรากฏจะแสดงรายละเอียดเกี่ยวกับคอนเทนเนอร์ใหม่ ปล่อยค่าเริ่มต้น แล้วเลือก **ตกลง**
1. บนหน้า **บรรจุ** บนแท็บด่วน **การบรรจุสินค้า** ในฟิลด์ **ตัวระบุ** ให้เลือก *A0002* เพื่อบรรจุสินค้านั้น สินค้าจะถูกเพิ่มลงในคอนเทนเนอร์
1. บนบานหน้าต่างการดำเนินการ เลือก **คอนเทนเนอร์สำหรับการจัดส่ง**

    บนหน้า **คอนเทนเนอร์สำหรับการจัดส่ง** ที่ปรากฏจะมีแถวของคอนเทนเนอร์ที่คุณเพิ่งสร้างขึ้น อย่างไรก็ตาม ฟิลด์ **รหัสรายการคอนเทนเนอร์** ในแถวนั้นว่างเปล่าในปัจจุบัน เนื่องจากคุณยังไม่ได้รับป้ายชื่อการจัดส่งและหมายเลขการติดตามจากบริษัทขนส่ง

1. บนหน้าต่างการดำเนินการ เลือก **ปิดคอนเทนเนอร์**
1. ในกล่องโต้ตอบ **ปิดคอนเทนเนอร์** ให้ตั้งค่าฟิลด์ **น้ำหนักรวม** เป็น *1 กก.* แล้วเลือก **ตกลง**

    ตอนนี้ ควรพิมพ์ป้ายชื่อการจัดส่งบนเครื่องพิมพ์ ZPL ที่คุณเลือกไว้ก่อนหน้านี้ ผลลัพธ์ควรมีลักษณะคล้ายกับตัวอย่างต่อไปนี้

    ![ป้ายชื่อการจัดส่งตัวอย่าง](media/sps-label-example.png "ตัวอย่างป้ายชื่อการจัดส่ง")

1. โปรดสังเกตว่า ค่า **รหัสรายการคอนเทนเนอร์** และ **การขนส่งรวม** ถูกเพิ่มเมื่อได้รับจากบริษัทขนส่ง


[!INCLUDE[footer-include](../../includes/footer-banner.md)]