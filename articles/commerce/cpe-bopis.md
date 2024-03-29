---
title: ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce
description: บทความนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกการซื้อออนไลน์ การเบิกสินค้าในร้านค้า (BOPIS) ในสภาพแวดล้อม Sandbox ของ Microsoft Dynamics 365 Commerce หลังจากที่มีการจัดเตรียมแล้ว
author: BrianShook
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 16cea7beb6ca05b5e96a9713b1217b414e27d56e
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013186"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-sandbox-environment"></a>ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกการซื้อออนไลน์ การเบิกสินค้าในร้านค้า (BOPIS) ในสภาพแวดล้อม Sandbox ของ Microsoft Dynamics 365 Commerce หลังจากที่มีการจัดเตรียมสภาพแวดล้อม

## <a name="prerequisite"></a>ข้อกำหนดเบื้องต้น

ทำตามกระบวนงานในบทความนี้ให้เสร็จสมบูรณ์ เฉพาะหลังจากที่มีการเตรียมใช้งานและการตั้งค่าคอนฟิกสภาพแวดล้อม Sandbox ของ Commerce ของคุณแล้ว สำหรับข้อมูลเกี่ยวกับวิธีการเตรียมใช้งานและตั้งค่าคอนฟิกสภาพแวดล้อมของคุณ ให้ดูที่ [เตรียมใช้งาสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](provisioning-guide.md) และ [ตั้งค่าคอนฟิกสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](./cpe-post-provisioning.md)

หลังจากที่มีการเตรียมใช้งานและการตั้งค่าคอนฟิกสภาพแวดล้อม Commerce ของคุณตั้งแต่ต้นจนจบ คุณสามารถใช้บทความนี้เพื่อเปิดใช้งานสถานการณ์จำลอง BOPIS

## <a name="configure-the-pos"></a>ตั้งค่าคอนฟิก POS

### <a name="configure-modern-pos"></a>ตั้งค่าคอนฟิก Modern POS

สถานการณ์จำลอง BOPIS ที่เกี่ยวข้องกับการชำระเงินด้วยบัตรเครดิต ต้องมีสถานีฮาร์ดแวร์ สถานีฮาร์ดแวร์ถูกสร้างขึ้นในไคลเอนต์ Modern POS for Windows และ Android ถ้าคุณกำลังใช้ Cloud POS หรือ Modern POS สำหรับ iOS ไคลเอนต์การขายหน้าร้าน (POS) ต้องมีการจับคู่กับสถานีฮาร์ดแวร์ที่ใช้ร่วมกัน บทความนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิก BOPIS สำหรับ Windows และไคลเอนต์ Android สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าสถานีฮาร์ดแวร์ที่ใช้ร่วมกัน ให้ดู [ตั้งค่าคอนฟิกและติดตั้งสถานีฮาร์ดแวร์ Retail](./retail-hardware-station-configuration-installation.md)

1. ไปยัง **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> เครื่องบันทึกเงินสด**
2. เลือกลงทะเบียน **SANFRAN-5** แล้วเลือก **แก้ไข**
3. เปลี่ยนค่าของฟิลด์ **โพรไฟล์ฮาร์ดแวร์** จาก **HW002** เป็น **HW001** แล้วเลือก **บันทึก**
4. เพื่อซิงโครไนส์การเปลี่ยนแปลง ไปที่ **การขายปลีกและการค้า \> ไอทีสำหรับการขายปลีกและการค้า \> กำหนดการกระจาย**
5. เลือกกำหนดการกระจาย **1090** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **เรียกใช้เดี๋ยวนี้**
6. เลือก **ใช่** แล้วจากนั้น **ตกลง** เพื่อเริ่มการซิงโครไนส์ข้อมูล 

### <a name="install-modern-pos"></a>ติดตั้ง Modern POS

1. ไปยัง **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> อุปกรณ์**
2. เลือกอุปกรณ์ **SANFRANCIS-5**
3. บนบานหน้าต่างการดำเนินการ เลือก **ดาวน์โหลด** และจากนั้นเลือก **ไฟล์การตั้งค่าคอนฟิก**
4. เลือก **ดาวน์โหลด** แล้วเลือก **Retail Modern POS** 
5. เมื่อการดาวน์โหลดของไฟล์ **ModernPOSSetup.exe** เสร็จสมบูรณ์ ให้เลือก **เปิดไฟล์**

    ![เปิดไฟล์](./dev-itpro/media/PAYMENTS/openfile.png)

6. เลือก **ถัดไป** เพื่อไปยังกระบวนการติดตั้ง เมื่อการติดตั้งเสร็จสมบูรณ์ ให้เลือก **ปิด**

### <a name="activate-modern-pos"></a>เรียกใช้งาน Modern POS

1. บนเดสก์ท็อป Windows ให้เลือกปุ่ม **เริ่มต้น** แล้วป้อน **Retail Modern POS**
2. เลือกแอปพลิเคชัน **Retail Modern POS** เพื่อเริ่มต้นการเรียกใช้งาน
3. เลือก **ถัดไป** ฟิลด์ **URL ของเซิร์ฟเวอร์** **รหัสอุปกรณ์** และ **หมายเลขเครื่องบันทึกเงินสด** ควรถูกกำหนดไว้ล่วงหน้าโดยใช้ข้อมูลจากไฟล์การตั้งค่าคอนฟิกที่คุณดาวน์โหลดไว้ในกระบวนงานก่อนหน้านี้
4. เลือก **เปิดใช้งาน**
5. กล่องโต้ตอบการรับรองความถูกต้องจะปรากฏขึ้น เลือกบัญชีที่ใช้ที่อยู่อีเมลที่เกี่ยวข้องก่อนหน้านี้กับผู้ปฏิบัติงาน **000713 - Andrew Collette**

    > [!NOTE]
    > ถ้าคุณยังไม่ได้เชื่อมโยงผู้ปฏิบัติงานกับข้อมูลประจำตัวของคุณ การเรียกใช้งานจะไม่ประสบความสำเร็จ ในกรณีนี้ ให้ทำตามขั้นตอนภายใต้ส่วน "เชื่อมโยงผู้ปฏิบัติงานกับรหัสประจำตัวของคุณ" ในบทความ [ตั้งค่าคอนฟิกสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](cpe-post-provisioning.md#associate-a-worker-with-your-identity)
    
6. เมื่อคุณได้รับข้อความแจ้งให้องค์กรของคุณสามารถจัดการอุปกรณ์ได้ ให้เลือก **แอปนี้เท่านั้น**
7. เมื่อการเรียกใช้งานเสร็จสมบูรณ์ ให้เลือก **เริ่มต้นใช้งาน**

### <a name="enable-bopis-in-modern-pos"></a>เปิดใช้งาน BOPIS ใน Modern POS

1. ลงชื่อเข้าใช้ Modern POS โดยใช้ **000713** เป็นรหัสผู้ปฏิบัติงานและ **123** เป็นรหัสผ่าน
2. ในขณะที่วิดีโอการฝึกปฏิบัติบทนำกำลังเล่นอยู่ ให้เลือกกล่องกาเครื่องหมายสองกล่องที่มุมล่างซ้ายของกล่องโต้ตอบ แล้วปิดกล่องโต้ตอบ
3. ถ้าคุณไม่ได้รับพร้อมท์ให้ปิดกะ ให้เลื่อนไปที่ด้านขวาบนหน้า **ยินดีต้อนรับ** ให้เลือก **ปิดกะ** แล้วลงชื่อกลับเข้าสู่ POS
4. หลังจากที่คุณลงชื่อเข้าใช้แล้ว เมื่อคุณได้รับข้อความแจ้ง ให้เลือก **ทำการดำเนินงานที่ไม่มีลิ้นชัก**
5. บนหน้า **ยินดีต้อนรับ** เลื่อนไปทางขวา และเลือกการดำเนินการ **เลือกสถานีฮาร์ดแวร์**
6. เลือก **จัดการ** ตั้งค่าตัวเลือก **ใช้สถานีฮาร์ดแวร์** เป็น **เปิด** แล้วเลือก **ตกลง**
7. ลงชื่อออกจาก POS และจากนั้น เข้าสู่ระบบกลับเข้าไปใหม่
8. หลังจากที่คุณลงชื่อเข้าใช้แล้ว ให้เลือก **เปิดกะใหม่** แล้วเลือก **ลิ้นชัก**

## <a name="complete-a-bopis-scenario"></a>ดำเนินการสถานการณ์จำลอง BOPIS ให้เสร็จสมบูรณ์

### <a name="create-a-storefront-order-for-in-store-pickup"></a>สร้างใบสั่งหน้าร้านสำหรับการเบิกสินค้าในร้านค้า

1. ไปที่ URL ที่คุณระบุไว้ในขั้นตอน [เริ่มต้นอีคอมเมิร์ซ](./provisioning-guide.md#initialize-e-commerce) ในระหว่างการตั้งค่าคอนฟิกสภาพแวดล้อม
2. เลือกสินค้า และเลือก **เพิ่มไปยังรถเข็น**
3. บนหน้าถุงช้อปปิ้ง ให้เลือก **เบิกสินค้านี้** สำหรับรายการใบสั่งที่คุณเพิ่งเพิ่ม
4. ในกล่องโต้ตอบ **เลือกร้านค้า** ให้ป้อน **San Francisco** แล้วเลือกปุ่ม **ค้นหา**
5. ในรายการของผลลัพธ์ ให้ค้นหาร้านค้า San Francisco และเลือก **เบิกสินค้าที่นี่**
6. บนหน้าถุงช้อปปิ้ง ให้เลือก **เช็คเอาท์ในฐานะผู้เยี่ยมชม** 

    > [!NOTE]
    > เมื่อต้องการดำเนินการเช็คเอาท์ต่อไป คุณต้องยอมรับการแจ้งเตือนเกี่ยวกับคุกกี้ การแจ้งเตือนนี้จะปรากฏเป็นแบนเนอร์ที่ด้านบนของหน้าเช็คเอาท์

7. สำหรับวิธีการชำระเงินด้วยบัตรเครดิต ให้ป้อนรายละเอียดต่อไปนี้:

    - **ชื่อผู้ถือบัตร:** ป้อนชื่อใดๆ
    - **หมายเลขบัตร:** ป้อน **4111-1111-1111-1111**
    - **วันหมดอายุ:** ป้อน **10/20**
    - **รหัสค่าการตรวจสอบความถูกต้องของบัตร (CVV):** ป้อน **737**

    > [!IMPORTANT]
    > ห้ามลองใช้ข้อมูลบัตรเครดิตจริงในไซต์ทดสอบไม่ว่าในสถานการณ์ใดๆ ก็ตาม

8. ดำเนินการเช็คเอาท์ต่อโดยป้อนรายละเอียดของที่อยู่ในการเรียกเก็บเงิน แล้วเลือก **บันทึกและดำเนินการต่อ**
9. เมื่อใบสั่งพร้อมใช้งานแล้ว ให้เลือก **เช็คเอาท์**

### <a name="synchronize-online-orders-to-the-back-office"></a>ซิงโครไนส์ใบสั่งออนไลน์ไปยังฝ่ายสนับสนุน

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการซิงโครไนส์ใบสั่งออนไลน์ ให้ดูที่ [การลงรายการบัญชีการขายและการชำระเงินออนไลน์](./tasks/posting-online-sales-payments.md)

### <a name="pick-up-an-order-in-the-store"></a>เบิกสินค้าในร้านค้า

1. ลงชื่อเข้าใช้ POS
2. บนหน้าจอ **ยินดีต้อนรับ** ให้เลือก **การเติมสินค้าตามใบสั่ง**
3. ในรายการของสินค้าสำหรับการเบิกสินค้า ให้เลือกรายการจากใบสั่งที่ถูกวางออนไลน์
4. ในขณะที่เลือกรายการใบสั่งแล้ว ให้เลือก **เบิกสินค้า**

    มีการเพิ่มสินค้าในรายการลงในหน้าจอธุรกรรม และ **$0.00** แสดงเป็นยอดดุลที่ครบกำหนด

5. เลือกยอดดุลที่ครบกำหนดชำระ **$0.00** หรือเลือกวิธีการชำระเงินใดๆ เพื่อสรุปธุรกรรม

## <a name="troubleshooting"></a>การแก้ไขปัญหา

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>ใบสั่งออนไลน์ที่ดึงข้อมูลใน POS มียอดดุลที่ครบกำหนดที่ไม่ใช่ศูนย์

เมื่อมีการดึงข้อมูลใบสั่งสำหรับการเบิกสินค้าในร้านค้า ถ้ายอดดุลที่ครบกำหนดไม่ใช่ 0 (ศูนย์) โปรดตรวจสอบให้แน่ใจว่ามีการใช้ Modern POS และสถานีฮาร์ดแวร์ใช้งานอยู่ ถ้ามีการใช้ Cloud POS หรือ Modern POS สำหรับ iOS ให้ตรวจสอบให้แน่ใจว่ามีการใช้งานสถานีฮาร์ดแวร์ที่ใช้ร่วมกันอยู่ ต้องมีฟอร์มของสถานีฮาร์ดแวร์ที่ใช้งานอยู่บางฟอร์มเพื่อดึงข้อมูลการชำระเงินที่ทำผ่านระบบออนไลน์

### <a name="general-issues-with-payment-capture"></a>ปัญหาทั่วไปเกี่ยวกับการบันทึกการชำระเงิน

สำหรับปัญหาทั่วไปทั้งหมด คุณควรปรึกษาล็อกเหตุการณ์ Modern POS หรือ Internet Information Services (IIS) Hardware Station เป็นขั้นตอนแรกเสมอ คุณสามารถค้นหาล็อกเหล่านี้ภายใต้โหนดต่อไปนี้ในล็อกเหตุการณ์ของ Windows:

- ล็อกแอปพลิเคชันและบริการ \> Microsoft \> Dynamics \> Commerce-ModernPOS
- ล็อกแอปพลิเคชันและบริการ \> Microsoft \> Dynamics \> Commerce-Hardware Station

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[เตรียมใช้งานสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](provisioning-guide.md)

[ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[พอร์ทัล Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[เว็บไซต์ Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)

[ตัวเชื่อมต่อการชำระเงิน Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3)

[การบันทึกเครื่องมือการชำระเงินออนไลน์ด้วยตัวเชื่อมต่อ Adyen](./dev-itpro/adyen-connector-listpi.md)

[ภาพรวมของการชำระเงินผ่านช่องทาง Omni](./omni-channel-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
