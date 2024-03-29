---
title: ตั้งค่าคอนฟิกสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce
description: บทความนี้อธิบายวิธีการตั้งค่าคอนฟิกสภาพแวดล้อม Sandbox ของ Microsoft Dynamics 365 Commerce หลังจากจัดเตรียมแล้ว
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ae6a8c63721ac32f525e1846a10c0b2caeb08f9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270384"
---
# <a name="configure-a-dynamics-365-commerce-sandbox-environment"></a>ตั้งค่าคอนฟิกสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

บทความนี้อธิบายวิธีการตั้งค่าคอนฟิกสภาพแวดล้อม Sandbox ของ Microsoft Dynamics 365 Commerce หลังจากจัดเตรียมแล้ว

ดำเนินการกระบวนงานในบทความนี้ให้เสร็จสมบูรณ์ เฉพาะหลังจากที่มีการเตรียมใช้งานสภาพแวดล้อม Sandbox ของ Commerce ของคุณแล้ว สำหรับข้อมูลเกี่ยวกับวิธีจัดเตรียมสภาพแวดล้อม Sandbox ของ Commerce ของคุณ ดูที่ [เตรียมใช้งานสภาพแวดล้อม Sandbox ของ Commerce](provisioning-guide.md)

หลังจากที่สภาพแวดล้อม Sandbox ของ Commerce ของคุณถูกเตรียมใช้งานอย่างทั่วถึง ขั้นตอนการตั้งค่าคอนฟิกหลังการเตรียมใช้งานเพิ่มเติมต้องเสร็จสมบูรณ์ก่อนที่คุณจะสามารถเริ่มต้นใช้งานสภาพแวดล้อม เพื่อดำเนินการขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ คุณต้องใช้ Microsoft Dynamics Lifecycle Services (LCS) และ Dynamics 365 Commerce

## <a name="before-you-start"></a>ก่อนที่คุณจะเริ่ม

1. ลงชื่อเข้าใช้ [พอร์ทัล LCS](https://lcs.dynamics.com)
1. ไปที่โครงการของคุณ
1. เลือกสภาพแวดล้อมของคุณในรายการ
1. ในข้อมูลสภาพแวดล้อมทางด้านขวา เลือก **เข้าสู่ระบบสภาพแวดล้อม** คุณจะถูกส่งไปยัง Commerce Headquarters
1. ตรวจสอบให้มั่นใจว่านิติบุคคล **USRT** ถูกเลือกไว้แล้วในมุมบนขวา นิติบุคคลนี้ได้รับการตั้งค่าคอนฟิกล่วงหน้าในข้อมูลสาธิต
1. ไปที่ **พารามิเตอร์ Commerce \> พารามิเตอร์การตั้งค่าคอนฟิก** และตรวจสอบให้แน่ใจว่ามีรายการสำหรับ **ProductSearch.UseAzureSearch** และตั้งค่าเป็น **จริง** ถ้ารายการนี้ขาดหายไป ให้เพิ่มและตั้งค่าเป็น **จริง**
1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าศูนย์ควบคุม \> ตัวกำหนดตารางทำงานการค้า \> เริ่มต้นตัวจัดกำหนดการการค้า** บนเมนูลอย **เริ่มต้นตัวกำหนดตารางทำงานการค้า** ตรวจสอบให้แน่ใจว่าได้ตั้งค่าตัวเลือก **ลบการตั้งค่าคอนฟิกที่มีอยู่** เป็น **ใช่** แล้วเลือก **ตกลง**
1. เพื่อให้ช่องทางร้านค้าและอีคอมเมิร์ซทำงานอย่างถูกต้อง คุณต้องเพิ่มช่องทางร้านค้าและอีคอมเมิร์ซเหล่านั้นลงใน Commerce Scale Unit ไปที่ **การขายปลีกและการค้า \> การตั้งค่า Headquarters \> ตัวจัดกำหนดการการค้า \> ฐานข้อมูลช่องทาง** และเลือก Commerce Scale Unit ในบานหน้าต่างทางซ้าย บนแท็บด่วน **ช่องทางการขายปลีก** ให้เพิ่ม **ร้านค้าออนไลน์ AW**, **ร้านค้าออนไลน์ของธุรกิจ AW** และช่องทาง **ร้านค้าออนไลน์เพิ่มเติมของ Fabrikam** หากคุณวางแผนที่จะใช้ช่องทางอีคอมเมิร์ซเหล่านั้น หรือคุณยังสามารถเพิ่มร้านค้าปลีกได้ถ้าคุณจะใช้การขายหน้าร้าน (POS) (ตัวอย่างเช่น **ซีแอตเทิล**, **ซานฟรานซิสโก** และ/หรือ **ซานโฮเซ**)
1. เพื่อให้แน่ใจว่าการเปลี่ยนแปลงทั้งหมดมีการซิงโครไนส์กับฐานข้อมูลช่องทาง ให้เลือก **ฐานข้อมูลช่องทาง \> การซิงค์ข้อมูลแบบสมบูรณ์** สำหรับ Commerce Scale Unit

ในระหว่างกิจกรรมหลังการเตรียมใช้งานใน Commerce Headquarters ตรวจสอบให้แน่ใจว่ามีการเลือกนิติบุคคล **USRT** เสมอ

## <a name="configure-the-point-of-sale"></a>ตั้งค่าคอนฟิกการขายหน้าร้าน

### <a name="associate-a-worker-with-your-identity"></a>เชื่อมโยงผู้ปฏิบัติงานกับข้อมูลเฉพาะตัวของคุณ

เพื่อเชื่อมโยงผู้ปฏิบัติงานกับข้อมูลเฉพาะตัวของคุณ ให้ทำตามขั้นตอนเหล่านี้ใน Commerce Headquarters

1. ใช้เมนูบนด้านซ้าย ไปที่ **โมดูล \> การขายปลีกและการค้า \> พนักงาน \> ผู้ปฏิบัติงาน**
1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดต่อไปนี้ **000713 - Andrew Collette** ผู้ใช้ตัวอย่างนี้เชื่อมโยงกับร้านค้าในซานฟรานซิสโกที่จะใช้ในส่วนถัดไป
1. บนบานหน้าต่างการดำเนินการ เลือก **Commerce**
1. เลือก **เชื่อมโยงข้อมูลเฉพาะตัวที่มีอยู่**
1. ในฟิลด์ **อีเมล** ทางขวาของ **ค้นหาโดยใช้อีเมล** ให้ป้อนที่อยู่อีเมลของคุณ
1. เลือก **ค้นหา**
1. เลือกเรกคอร์ดที่มีชื่อของคุณ
1. เลือก **ตกลง**
1. เลือก **บันทึก**

### <a name="activate-cloud-pos"></a>เรียกใช้ Cloud POS

ถ้าต้องการเปิดใช้งาน Cloud POS ให้ทำตามขั้นตอนเหล่านี้ใน LCS

1. บนเมนูด้านบน ให้เลือก **สภาพแวดล้อมที่ใช้ Cloud**
1. เลือกสภาพแวดล้อมของคุณในรายการ
1. ในข้อมูลสภาพแวดล้อมทางด้านขวา เลือก **เข้าสู่ระบบการขายหน้าร้านระบบคลาวด์**
1. เลือก **ถัดไป** เพื่อเปิดกล่องโต้ตอบ **ก่อนที่คุณจะเริ่มต้น**
1. ปล่อยฟิลด์ **URL ของเซิร์ฟเวอร์** ตามที่เป็นอยู่ เลือก **ถัดไป**
1. เข้าสู่ระบบโดยใช้บัญชี Microsoft Azure Active Directory (Azure AD) ของคุณ
1. ภายใต้ **ชื่อร้านค้า** เลือก **San Francisco** แล้วจากนั้น เลือก **ถัดไป**
1. ภายใต้ **ลงทะเบียนและอุปกรณ์** เลือก **SANFRAN-1**
1. เลือก **เปิดใช้งาน** คุณได้ออกจากระบบและนำไปยังหน้าลงชื่อเข้าใช้ POS
1. ขณะนี้คุณสามารถลงชื่อเข้าสู่ประสบการณ์ Cloud POS ได้โดยใช้รหัสผู้ปฏิบัติงาน **000713** และรหัสผ่าน **123**

## <a name="set-up-your-e-commerce-sites"></a>ตั้งค่าไซต์อีคอมเมิร์ซของคุณ

มีไซต์อีคอมเมิร์ซสาธิตอยู่สามไซต์ คือ Fabrikam, Adventure Works และ Adventure Works Business ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกไซต์สาธิตแต่ละไซต์

1. ลงชื่อเข้าใช้ตัวสร้างไซต์โดยใช้ URL ที่คุณจดบันทึกเวลาที่คุณเริ่มต้นอีคอมเมิร์ซในระหว่างการจัดเตรียม (โปรดดู [เริ่มต้นอีคอมเมิร์ซ](provisioning-guide.md#initialize-e-commerce))
1. เลือกไซต์ (**Fabrikam**, **Adventure Works** หรือ **Adventure Works Business**) เพื่อเปิดกล่องโต้ตอบการตั้งค่าไซต์
1. เลือกโดเมนที่คุณป้อนเมื่อคุณเริ่มต้น Commerce
1. ในศูนย์ควบคุม ให้เลือกช่องทางร้านค้าออนไลน์ที่ตั้งค่าคอนฟิกไว้ล่วงหน้า (**ร้านค้าออนไลน์แบบขยายของ Fabrikam**, **ร้านค้าออนไลน์ AW** หรือ **ร้านค้าออนไลน์ AW Business**) ที่ตรงกับช่องทางเริ่มต้น
1. เลือก **en-us** เป็นภาษาเริ่มต้น 
1. ตั้งค่าคอนฟิกฟิลด์ของพาธ สามารถเว้นว่างไว้ได้สำหรับไซต์เดียว แต่จะต้องกำหนดค่าหากใช้ชื่อโดเมนเดียวกันสำหรับหลายไซต์ ตัวอย่างเช่น หากชื่อโดเมนคือ `https://www.constoso.com` คุณสามารถใช้พาธที่ว่างเปล่าสำหรับ Fabrikam (`https://contoso.com`) และใช้"aw" สำหรับ Adventure Works (`https://contoso.com/aw`) และ "awbusiness" สำหรับไซต์ Adventure Works Business (`https://contoso.com/awbusiness`)
1. เลือก **ตกลง** รายการของหน้าบนไซต์จะปรากฏขึ้น
1. หรือทําซ้ำขั้นตอนที่ 2-7 เพื่อตั้งค่าคอนฟิกไซต์สาธิตอื่นๆ หากต้องการ

## <a name="enable-jobs"></a>เปิดใช้งานงานต่าง ๆ

ในการเปิดใช้งานงานใน Commerce ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้สภาพแวดล้อมศูนย์ควบคุม
1. ใช้เมนูด้านซ้ายเพื่อไปที่ **การขายปลีกและการค้า \> การสอบถามและรายงาน \> ชุดงาน**

    ขั้นตอนที่เหลือของขั้นตอนนี้ต้องเสร็จสมบูรณ์สำหรับแต่ละงานต่อไปนี้:

    * ประมวลผลการแจ้งเตือนทางอีเมลของใบสั่งของการขายปลีก
    * ความพร้อมใช้งานของผลิตภัณฑ์
    * P-0001
    * ซิงโครไนส์งานใบสั่ง

1. ใช้ตัวกรองด่วนเพื่อค้นหางานโดยใช้ชื่อ
1. ถ้าสถานะของงานคือ **กำลังดำเนินการ** ให้ทำตามขั้นตอนเหล่านี้:

    1. เลือกเรกคอร์ด
    1. ในบานหน้าต่างการดำเนินการ บนแท็บ **ชุดงาน** เลือก **เปลี่ยนสถานะ**
    1. เลือก **การยกเลิก** และจากนั้น เลือก **ตกลง**

1. ถ้าสถานะของงานคือ **ระงับ** ให้ทำตามขั้นตอนเหล่านี้:

    1. เลือกเรกคอร์ด
    1. ในบานหน้าต่างการดำเนินการ บนแท็บ **ชุดงาน** เลือก **เปลี่ยนสถานะ**
    1. เลือก **กำลังรอ** แล้วจากนั้น เลือก **ตกลง**

อีกทางหนึ่งคือ คุณยังสามารถตั้งค่าช่วงการเกิดซ้ำเป็นหนึ่ง (1) นาทีสำหรับงานต่อไปนี้:

* ประมวลผลงานการแจ้งเตือนทางอีเมลของใบสั่งการขายปลีก
* งาน P-0001
* ซิงโครไนส์งานใบสั่ง

### <a name="run-full-data-synchronization"></a>รันการซิงโครไนส์ข้อมูลแบบสมบูรณ์

หากต้องการรันการซิงโครไนส์ข้อมูลแบบสมบูรณ์ใน Commerce ให้ทำตามขั้นตอนเหล่านี้ใน Commerce Headquarters

1. ใช้เมนูด้านซ้ายเพื่อไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าศูนย์ควบคุม \> ตัวจัดกำหนดการของ Commerce \> ฐานข้อมูลช่องทาง**
1. เลือกช่องทางที่ชื่อ **scXXXXXXXXX**
1. ในบานหน้าต่างการดำเนินการ เลือก **การซิงค์ข้อมูลแบบสมบูรณ์**
1. ป้อนค่า **9999** ที่กำหนดการการกระจาย
1. เลือก **ตกลง**
1. เลือก **ตกลง**

### <a name="test-credit-card-information-to-do-test-purchases"></a>ทดสอบข้อมูลบัตรเครดิตเพื่อทำการทดสอบการซื้อ

เมื่อต้องการทำการทดสอบธุรกรรมบนไซต์ คุณสามารถใช้ข้อมูลบัตรเครดิตทดสอบดังต่อไปนี้:

- **หมายเลขบัตร:** 4111-1111-1111-1111
- **วันหมดอายุ:** 10/30
- **รหัสค่าการตรวจสอบความถูกต้องของบัตร (CVV):** 737

> [!IMPORTANT]
> ห้ามลองใช้ข้อมูลบัตรเครดิตจริงในไซต์ทดสอบไม่ว่าในสถานการณ์ใดๆ ก็ตาม

## <a name="next-steps"></a>ขั้นตอนถัดไป

หลังจากขั้นตอนการเตรียมใช้งานและการตั้งค่าคอนฟิกเสร็จสมบูรณ์แล้ว คุณสามารถเริ่มใช้สภาพแวดล้อม Sandbox ของคุณ ใช้ URL ของตัวสร้างไซต์ Commerce เพื่อไปยังประสบการณ์การสร้าง ใช้ URL ของไซต์ Commerce เพื่อไปยังประสบการณ์ไซต์ของลูกค้าขายปลีก

หากต้องการตั้งค่าคอนฟิกคุณสมบัติเพิ่มเติมของสภาพแวดล้อม Sandbox ของ Commerce ของคุณ ให้ดูที่ [ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อม Sandbox ของ Commerce](cpe-optional-features.md)

เพื่อให้ผู้ใช้อีคอมเมิร์ซสามารถลงชื่อเข้าใช้ไซต์อีคอมเมิร์ซได้ คุณต้องตั้งค่าคอนฟิกเพิ่มเติมเพื่อเปิดใช้งานการรับรองความถูกต้องของไซต์ผ่านทาง Azure Active Directory แบบธุรกิจกับผู้บริโภค (B2C) สำหรับคำแนะนำ โปรดดู [ตั้งค่าผู้เช่า B2C ใน Commerce](set-up-b2c-tenant.md)

## <a name="troubleshooting"></a>การแก้ไขปัญหา

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>รายการช่องทางของโปรแกรมสร้างไซต์ว่างเปล่าเมื่อตั้งค่าคอนฟิกไซต์

ถ้าโปรแกรมสร้างไซต์ไม่แสดงช่องทางร้านค้าออนไลน์ใดๆ ศูนย์ควบคุมจะตรวจสอบให้แน่ใจว่ามีการเพิ่มช่องทางเข้าใน Commerce Scale Unit ตามที่อธิบายไว้ในส่วน [ก่อนที่คุณจะเริ่มต้น](#before-you-start) ด้านบนหรือไม่ นอกจากนี้ ให้เรียกใช้ **เริ่มต้นตัวจัดกำหนดการการค้า** ด้วยค่า **ลบการตั้งค่าคอนฟิกที่มีอยู่** เป็น **ใช่**  เมื่อขั้นตอนเหล่านี้เสร็จสมบูรณ์แล้ว บนหน้า **ฐานข้อมูลช่องทาง** (**การขายปลีกและการค้า \> การตั้งค่าศูนย์ควบคุม \> ตัวจัดกำหนดการการค้า \> ฐานข้อมูลช่องทาง**) เรียกใช้งาน **9999** บน Commerce Scale Unit

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>ชื่อสีไม่ได้แสดงอยู่ในหน้าประเภท แต่แสดงอยู่ในหน้ารายละเอียดผลิตภัณฑ์ (PDP)

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อให้มั่นใจว่าสีและขนาดตั้งค่าให้สามารถปรับปรุงได้

1. ในศูนย์ควบคุม ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ประเภทช่องทางและคุณลักษณะของผลิตภัณฑ์**
1. ในบานหน้าต่างด้านซ้าย เลือกช่องทางร้านค้าออนไลน์ แล้วเลือก **ตั้งค่าข้อมูลเมตาของคุณลักษณะ**
1. ตั้งค่าตัวเลือก **แสดงแอตทริบิวต์สำหรับช่องทาง** เป็น **ใช่** ตั้งค่าตัวเลือก **สามารถปรับได้** เป็น **ใช่** แล้วเลือก **บันทึก** 
1. กลับไปที่หน้าช่องทางร้านค้าออนไลน์ แล้วเลือก **เผยแพร่การอัปเดตช่องทาง**
1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าศูนย์ควบคุม \> ตัวจัดกำหนดการการค้า \> ฐานข้อมูลช่องทาง** และเรียกใช้งาน **9999** บน Commerce Scale Unit

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>ลักษณะทางธุรกิจจะไม่เปิดสำหรับไซต์ธุรกิจของ AdventureWorks

ในศูนย์ควบคุม ตรวจสอบให้แน่ใจว่าช่องทางร้านค้าออนไลน์ได้รับการตั้งค่าคอนฟิก **ชนิดลูกค้า** เป็น **B2B** หาก **ชนิดลูกค้า** ตั้งค่าเป็น **B2C** ต้องสร้างช่องทางใหม่เนื่องจากช่องทางที่มีอยู่ไม่สามารถแก้ไขได้ 

ข้อมูลสาธิตที่จัดส่งใน Commerce เวอร์ชัน 10.0.26 และก่อนหน้านี้มีบักที่ช่องทาง **ร้านค้าออนไลน์สำหรับธุรกิจ AW** ตั้งค่าคอนฟิกไม่ถูกต้อง วิธีแก้ไขคือการสร้างช่องทางใหม่ที่มีการตั้งค่าและการตั้งค่าคอนฟิกเดียวกัน ยกเว้ น **ชนิดลูกค้า** ซึ่งควรตั้งค่าเป็น **B2B**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[เตรียมใช้งานสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](provisioning-guide.md)

[ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](cpe-optional-features.md)

[ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[พอร์ทัล Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[เว็บไซต์ Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)

[ตั้งค่าผู้เช่า B2C ใน Commerce](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
