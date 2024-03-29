---
title: ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce
description: บทความนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อม Sandbox ของ Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: 4935f5f6ee17cba9c09eb79132119a7cbc08d9ad
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270367"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-sandbox-environment"></a>ตั้งค่าคอนฟิกคุณลักษณะเพิ่มเติมสำหรับสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

บทความนี้อธิบายวิธีการตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อม Sandbox ของ Microsoft Dynamics 365 Commerce

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ถ้าคุณต้องการสาธิตคุณลักษณะอีเมลการทำธุรกรรม ต้องเป็นไปตามข้อกำหนดเบื้องต้นต่อไปนี้:

- คุณมีเซิร์ฟเวอร์อีเมลที่พร้อมใช้งาน (เซิร์ฟเวอร์ Simple Mail Transfer Protocol \[SMTP\]) ซึ่งสามารถใช้งานจากการสมัครใช้งาน Microsoft Azure ที่คุณเตรียมใช้งานสภาพแวดล้อม Sandbox
- คุณมีที่อยู่ของชื่อโดเมนเต็ม FQDN/IP ของเซิร์ฟเวอร์ หมายเลขพอร์ต SMTP และรายละเอียดการรับรองความถูกต้องที่พร้อมใช้งาน

## <a name="configure-the-image-back-end"></a>กำหนดค่าแบ็คเอนด์ของรูปภาพ

### <a name="find-your-media-base-url"></a>ค้นหา URL ที่เป็นพื้นฐานของสื่อของคุณ

> [!NOTE]
> ก่อนเสร็จสิ้นกระบวนการนี้ คุณต้องทำตามขั้นตอนใน [ตั้งค่าไซต์ของคุณใน Commerce](cpe-post-provisioning.md#set-up-your-e-commerce-sites)

1. ลงชื่อเข้าใช้ตัวสร้างไซต์ Commerce โดยใช้ URL ที่คุณจดบันทึกเวลาที่คุณเริ่มต้นอีคอมเมิร์ซในระหว่างการจัดเตรียม (โปรดดู [เริ่มต้นอีคอมเมิร์ซ](provisioning-guide.md#initialize-e-commerce))
1. เปิดไซต์ **Fabrikam**, **Adventure Works** หรือ **Adventure Works Business** ที่คุณต้องการทำงาน
1. บนเมนูด้านซ้าย ให้เลือก **ไลบรารีสื่อ**
1. เลือกสินทรัพย์ที่เป็นรูปภาพรูปเดียวใด ๆ
1. ในตัวตรวจสอบคุณสมบัติทางด้านขวา ให้ค้นหาคุณสมบัติ **URL สาธารณะ** ค่าคือ URL นี่คือตัวอย่าง:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`

1. แทนที่ตัวระบุตัวสุดท้ายใน URL (**MA1nQC** โดยใช้สตริง) **search?fileName=** นี่คือ URL ตัวอย่างหลังจากทำการเปลี่ยนแปลงนี้:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    URL นี้เป็น URL ฐานสื่อของคุณ จดบันทึก

### <a name="update-the-media-base-url"></a>อัปเดต URL พื้นฐานของสื่อ

1. ลงชื่อเข้าใช้ Commerce headquarters
1. ใช้เมนูทางด้านซ้ายเพื่อไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> โพรไฟล์ของช่องทาง**
1. เลือก **แก้ไข**
1. ภายใต้ **คุณสมบัติของโพรไฟล์** ให้แทนที่ค่าคุณสมบัติสำหรับ **URL พื้นฐานของเซิร์ฟเวอร์สื่อ** ด้วย URL พื้นฐานของสื่อที่คุณสร้างไว้ก่อนหน้านี้
1. เลือกช่องทางที่ชื่อ **scXXXXXXXXX**
1. ภายใต้ **คุณสมบัติของโพรไฟล์** เลือก **เพิ่ม**
1. สำหรับคุณสมบัติที่ถูกเพิ่ม ให้เลือก **URL ฐานของสื่อเซิร์ฟเวอร์** เป็นคีย์คุณสมบัติ ในฐานะที่เป็นค่าคุณสมบัติ ให้ป้อน URL ฐานสื่อที่คุณสร้างไว้ก่อนหน้านี้
1. เลือก **บันทึก**

## <a name="configure-and-test-the-email-server"></a>ตั้งค่าคอนฟิกและทดสอบเซิร์ฟเวอร์อีเมล

> [!NOTE]
> โปรดทราบว่าเซิร์ฟเวอร์ SMTP หรือบริการอีเมลที่คุณป้อนที่นี่ต้องสามารถเข้าถึงได้จากการสมัครใช้งาน Azure ที่คุณใช้สำหรับสภาพแวดล้อม

1. ลงชื่อเข้าใช้ Commerce headquarters
1. ใช้เมนูทางด้านซ้ายเพื่อไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์ของอีเมล**
1. บนแท็บ **การตั้งค่า SMTP** ในฟิลด์ **เซิร์ฟเวอร์อีเมลขาออก** ให้ป้อน FQDN หรือที่อยู่ IP ของบริการของเซิร์ฟเวอร์ SMTP หรืออีเมลของคุณ
1. ในฟิลด์ **หมายเลขพอร์ต SMTP** ให้ป้อนหมายเลขพอร์ต (ถ้าคุณไม่ได้ใช้ Secure Sockets Layer \[SSL\] หมายเลขพอร์ตเริ่มต้นคือ **25**)
1. ถ้าจำเป็นต้องใช้การรับรอง ให้ป้อนค่าในฟิลด์ **ชื่อผู้ใช้** และ **รหัสผ่าน**
1. เลือก **บันทึก**
1. เลือก **รีเฟรช**
1. บนแท็บ **การทดสอบอีเมล** ในฟิลด์ **ผู้ให้บริการอีเมล** เลือก **SMTP** 
1. ในฟิลด์ **ส่งไปยัง** ให้ป้อนที่อยู่อีเมลที่คุณต้องการให้อีเมลทดสอบส่งไป
1. เลือก **ส่งอีเมลทดสอบ**

## <a name="configure-email-templates"></a>ตั้งค่าเท็มเพลตของอีเมล

สำหรับแต่ละเหตุการณ์ธุรกรรมที่คุณต้องการส่งอีเมล คุณต้องอัปเดตเท็มเพลตอีเมลด้วยที่อยู่อีเมลของผู้ส่งที่ถูกต้อง

1. ลงชื่อเข้าใช้ Commerce headquarters
1. ใช้เมนูทางด้านซ้ายเพื่อไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> เท็มเพลตอีเมลขององค์กร**
1. เลือก **แสดงรายการ**
1. สำหรับแต่ละเท็มเพลตในรายการ ทำตามขั้นตอนเหล่านี้:

    1. ในฟิลด์ **อีเมลผู้ส่ง** ป้อนอยู่อีเมลของผู้ส่ง
    1. ไม่บังคับ: ในฟิลด์ **ชื่อผู้ส่ง** ให้ป้อนชื่อที่ควรใช้เป็นชื่อผู้ส่ง

1. เลือก **บันทึก**

## <a name="customize-email-templates"></a>กำหนดเท็มเพลตอีเมล

คุณอาจต้องการปรับแต่งเท็มเพลตอีเมลเพื่อให้ใช้รูปภาพที่แตกต่างกัน หรือคุณอาจต้องการปรับปรุงลิงก์ในเทมเพลตเพื่อให้ไปที่สภาพแวดล้อม Sandbox ของคุณ กระบวนการนี้จะอธิบายวิธีการดาวน์โหลดเท็มเพลตเริ่มต้น เลือกกำหนดเท็มเพลตเหล่านั้น และอัปเดตเท็มเพลตในระบบ

1. ในเว็บเบราว์เซอร์ ดาวน์โหลด [ไฟล์ .zip เทมเพลตอีเมลเริ่มต้นของการสาธิต Microsoft Dynamics 365 Commerce](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) ลงในคอมพิวเตอร์ของคุณ ไฟล์นี้จะประกอบด้วยเอกสาร HTML ต่อไปนี้

    - เท็มเพลตการยืนยันใบสั่ง
    - เท็มเพลตการออกบัตรของขวัญ
    - เท็มเพลตใบสั่งใหม่
    - เท็มเพลตใบสั่งแพ็คสินค้า
    - เท็มเพลตใบสั่งรับสินค้า

1. เลือกกำหนดเท็มเพลตโดยใช้ตัวแก้ไขข้อความหรือ HTML ดูรายการ [โทเค็นที่สนับสนุน](#supported-tokens-in-the-email-template) ภายหลังในบทความนี้
1. ลงชื่อเข้าใช้ Commerce
1. ใช้เมนูด้านซ้าย ไปที่ **โมดูล \> การจัดการองค์กร \> ตั้งค่า \> เท็มเพลตอีเมลขององค์กร**
1. ขยายรายการด้านซ้ายเพื่อดูเท็มเพลตทั้งหมด
1. สำหรับแต่ละเท็มเพลตที่คุณต้องการกำหนดเอง ให้ทำตามขั้นตอนเหล่านี้:

    1. เลือกเท็มเพลตในรายการ
    1. ภายใต้ **เนื้อหาของข้อความอีเมล** ให้เลือกรุ่นภาษาที่เหมาะสมในรายการ (ภาษาเริ่มต้นคือ **en-us**)
    1. ใต้ **เนื้อหาข้อความอีเมล** ให้เลือก **แก้ไข** บานหน้าต่าง **อัปโหลดเท็มเพลตอีเมล** ปรากฏขึ้น
    1. เลือก **เรียกดู** และค้นหาไฟล์ HTML ที่มีเนื้อหาที่กำหนดเอง
    1. เลือก **อัปโหลด** เท็มเพลตของคุณจะถูกอัปโหลดไปยังระบบ และตัวอย่างจะแสดงขึ้นมา
    1. เลือก **ตกลง**
    1. ไม่จำเป็น: กำหนดคุณสมบัติ **ชื่อเรื่อง** ของเท็มเพลต
    1. เลือก **บันทึก**

### <a name="supported-tokens-in-the-email-template"></a>โทเคนที่สนับสนุนในเท็มเพลตอีเมล์

เมื่ออีเมลถูกส่ง โทเคนเหล่านี้จะถูกแทนที่ด้วยค่าจริงที่ใช้กับลูกค้าและใบสั่งของลูกค้า

#### <a name="sales-order"></a>ใบสั่งขาย

โทเคนต่อไปนี้จะใช้กับใบสั่งขายในภาพรวม

| ชื่อของโทเคน | โทเคน |
|-------------------|-------|
| หมายเลขใบสั่ง      | %salesid% |
| ชื่อของลูกค้า   | %customername% |
| ที่อยู่ที่จัดส่ง  | %deliveryaddress% |
| ที่อยู่ที่เรียกเก็บเงิน   | %customeraddress% |
| วันที่สั่ง        | %shipdate% |
| วิธีการจัดส่ง     | %modeofdelivery% |
| ส่วนลด          | %discount% |
| ภาษีขาย         | %tax% |
| ผลรวมของใบสั่ง       | %total% |

#### <a name="sales-line"></a>รายการขาย

โทเคนต่อไปนี้จะถูกแทนที่ด้วยค่าสำหรับผลิตภัณฑ์แต่ละรายการในใบสั่ง

> [!NOTE]
> วางโทเค็น **รายการผลิตภัณฑ์ - เริ่มต้น** ที่จุดเริ่มต้นของบล็อก HTML ที่ถูกทำซ้ำสำหรับทุกผลิตภัณฑ์ และวางโทเค็น **รายการผลิตภัณฑ์ - สิ้นสุด** ที่ส่วนท้ายของบล็อก

| ชื่อของโทเคน      | โทเคน |
|------------------------|-------|
| รายการผลิตภัณฑ์ - เริ่มต้น   | \<!--%tablebegin.salesline% --\> |
| รายการผลิตภัณฑ์ - สิ้นสุด     | \<!--%tableend.salesline%--\> |
| ชื่อผลิตภัณฑ์           | %lineproductname% |
| คำอธิบาย            | %lineproductdescription% |
| ปริมาณ               | %linequantity% |
| ราคาต่อหน่วยในรายการ        | %lineprice% (ตรวจสอบ) |
| จำนวนสินค้าทั้งหมดในรายการ        | %linenetamount% |
| line discount / ส่วนลดต่อรายการสินค้า          | %linediscount% |
| วันที่จัดส่ง              | %lineshipdate% |
| วิธีการจัดซื้อ     | %linedeliverymode% |
| delivery address / ที่อยู่ที่จัดส่ง       | %linedeliveryaddress% |
| หน่วยการขายของรายการ | %lineunit% |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[เตรียมใช้งานสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](provisioning-guide.md)

[ตั้งค่าคอนฟิกสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](cpe-post-provisioning.md)

[ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อม Sandbox ของ Dynamics 365 Commerce](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[พอร์ทัล Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[เว็บไซต์ Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
