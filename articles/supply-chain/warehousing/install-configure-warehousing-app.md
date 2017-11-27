---
title: "ติดตั้งและตั้งค่าคอนฟิก Microsoft Dynamics 365 for Finance and Operations &#8211; คลังสินค้า"
description: "หัวข้อนี้อธิบายวิธีการติดตั้งและการตั้งค่าคอนฟิก Microsoft Dynamics 365 for Finance and Operations - คลังสินค้า"
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4b3d068ddbf6f0b28c97618f5fa10fa486f3af51
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>ติดตั้งและตั้งค่าคอนฟิก Microsoft Dynamics 365 for Finance and Operations &#8211; คลังสินค้า

[!include[banner](../includes/banner.md)]


หัวข้อนี้อธิบายวิธีการติดตั้งและการตั้งค่าคอนฟิก Microsoft Dynamics 365 for Finance and Operations - คลังสินค้า

Finance and Operations - คลังสินค้าคือแอพลิเคชันที่พร้อมใช้งานบน Google Play Store และ Windows Store สำหรับ Finance and Operations รุ่นปัจจุบัน แอพลิเคชันนี้ไว้สำหรับเป็นส่วนประกอบแบบสแตนด์อโลน ซึ่งหมายถึงการปรับใช้ด้วยตนเองบนอุปกรณ์ที่ใช้สำหรับงานคลังสินค้า เมื่อต้องการใช้แอพลิเคชันในสภาพแวดล้อมของ Finance and Operations ของคุณ อันดับแรก คุณจะต้องดาวน์โหลดแอพบนอุปกรณ์แต่ละเครื่อง และตั้งค่าคอนฟิกเพื่อเชื่อมต่อกับสภาพแวดล้อมของ Finance and Operations ของคุณ หัวข้อนี้อธิบายวิธีการติดตั้งแอพบนอุปกรณ์ของคุณ นอกจากนี้ยังอธิบายถึงวิธีการตั้งค่าคอนฟิกแอพเพื่อเชื่อมต่อกับสภาพแวดล้อม Finance and Operations ของคุณ

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น
แอพพร้อมใช้งานบนระบบปฏิบัติการ Android และ Windows เมื่อต้องการใช้แอพนี้ คุณต้องใช้ระบบปฏิบัติการที่ได้รับการสนับสนุนต่อไปนี้ที่ติดตั้งบนอุปกรณ์ของคุณอย่างใดอย่างหนึ่ง นอกจากนี้คุณยังต้องมี Finance and Operations รุ่นที่ได้รับการสนับสนุนต่อไปนี้อย่างใดอย่างหนึ่ง ใช้ข้อมูลในตารางต่อไปนี้ในการประเมินว่าสภาพแวดล้อมของฮาร์ดแวร์และซอฟต์แวร์ของคุณพร้อมที่จะสนับสนุนการติดตั้งหรือไม่

| แพลตฟอร์ม                    | เวอร์ชัน                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (ทุกรุ่น)                                                                                                                                                   |
| Finance and Operations | Microsoft Finance and Operations เวอร์ชัน 1611 <br>หรือ <br>Microsoft Dynamics AX รุ่น 7.0/7.0.1 และแพลตฟอร์ม Microsoft Dynamics AX อัพเดต 2 ด้วยโปรแกรมแก้ไขด่วน KB 3210014 |

## <a name="get-the-app"></a>เรียกกลุ่มแอพลิเคชัน
-   Windows (UWP): - [Finance and Operations - คลังสินค้าบน Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android:
    - [Finance and Operations - คลังสินค้าบน Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations - คลังสินค้าบน Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-active-directory"></a>สร้างแอพบริการเว็บใน Active Directory
เมื่อต้องการเปิดใช้งานแอพเพื่อโต้ตอบกับเซิร์ฟเวอร์ Finance and Operations คุณต้องลงทะเบียนแอพลิเคชันบริการเว็บใน Azure Active Directory สำหรับผู้เช่า Dynamics 365 for Finance and Operations สำหรับเหตุผลด้านความปลอดภัย เราขอแนะนำให้คุณสร้างแอพบริการเว็บสำหรับแต่ละอุปกรณ์ที่คุณใช้ เมื่อต้องการสร้างแอพบริการเว็บใน Azure Active Directory (Azure AD) ให้ดำเนินการขั้นตอนต่อไปนี้:

1.  ในเว็บเบราว์เซอร์ ไปที่ <https://manage.windowsazure.com>
2.  ป้อนชื่อและรหัสผ่านสำหรับผู้ใช้ที่มีสิทธิ์เข้าถึงการสมัครใช้งาน Azure
3.  ในพอร์ทัล Azure ในบานหน้าต่างนำทางด้านซ้าย คลิก **Active Directory**[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  ในกริด เลือกอินสแตนซ์ของ Active Directory ที่ถูกใช้โดย Finance and Operations
5.  บนแถบเครื่องมือด้านบน คลิก **แอพลิเคชัน** [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  ในบานหน้าต่างด้านล่าง ให้คลิก **เพิ่ม** ตัวช่วยสร้าง **เพิ่มแอพลิเคชัน** เริ่มทำงาน
7.  ป้อนชื่อสำหรับแอพลิเคชันและเลือก **เว็บแอพลิเคชันและ/หรือ API เว็บ** [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  ป้อน URL เข้าสู่ระบบ ซึ่งเป็น URL ของแอพบนเว็บ URL นี้จะเหมือนกับ URL การปรับใช้ของคุณ แต่ใช้ oauth จะถูกเพิ่มที่จุดสิ้นสุด ป้อนรหัส URI รหัสแอพ ค่านี้เป็นข้อบังคับ แต่ไม่จำเป็นสำหรับการรับรองความถูกต้อง ตรวจสอบให้แน่ใจว่า URI รหัสแอพนี้ไม่ใช่ URI ที่จำลองขึ้น อย่างเช่น https://contosooperations/wmapp เนื่องจากการใช้ URL การปรับใช้ของคุณอาจก่อให้เกิดปัญหาในการลงชื่อในแอพลิเคชัน AAD อื่น ๆ เช่น Excel Add-in [![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)
9.  ไปที่แท็บ **ตั้งค่าคอนฟิก** [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. เลื่อนลงมาจนกว่าคุณจะเห็นส่วน **สิทธิ์ไปยังแอพอื่น ๆ** คลิก **เพิ่มแอพลิเคชัน** [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. เลือก **Microsoft Dynamics ERP** ในรายการ คลิกปุ่ม **ตรวจสอบเสร็จสมบูรณ์** ที่มุมขวาบนของหน้า [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. ในรายการ **มอบหมายสิทธิ์** เลือกกล่องกาเครื่องหมายทั้งหมด คลิก **บันทึก** [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. จดบันทึกข้อมูลต่อไปนี้:
    -   **รหัสไคลเอนต์** - เมื่อคุณเลื่อนหน้าขึ้น คุณจะเห็น **รหัสไคลเอนต์** แสดงอยู่
    -   **คีย์** - ในส่วน **คีย์** สร้างคีย์โดยการเลือกระยะเวลาและคัดลอกคีย์ ในภายหลังจะเรียกคีย์นี้ว่า **ข้อมูลลับไคลเอนต์**

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>สร้างและตั้งค่าคอนฟิกบัญชีผู้ใช้ใน Finance and Operations
เมื่อต้องการเปิดใช้งาน Finance and Operations เพื่อใช้แอพพลิเคชัน Azure AD ของคุณ คุณจำเป็นต้องดำเนินตามขั้นตอนการตั้งค่าคอนฟิกต่อไปนี้:

1.  สร้างบัญชีผู้ใช้ใหม่ใน Azure Active Directory สำหรับผู้เช่า Finance and Operations วัตถุประสงค์ของบัญชีผู้ใช้นี้คือเพื่อเข้าถึงบริการแบบกำหนดเองเฉพาะของแอพคลังสินค้า ซึ่งเซิร์ฟเวอร์ Finance and Operations แสดง หลังจากเสร็จสิ้นขั้นตอนนี้ คุณจะได้รับข้อมูลประจำตัวผู้ใช้ WMDP ซึ่งประกอบด้วยที่อยู่อีเมล WMDP และรหัสผ่าน WMDP เมื่อต้องการเรียนรู้เกี่ยวกับขั้นตอนพื้นฐานสำหรับการเพิ่มผู้ใช้ใน Azure AD และ Finance and Operations ให้ดูบทสอนนี้: [ลงทะเบียนเพื่อสมัครใช้งาน Finance and Operations](../../dev-itpro/dev-tools/sign-up-preview-subscription.md)
2.  สร้างผู้ใช้ Finance and Operations ที่สอดคล้องกับข้อมูลประจำตัวผู้ใช้แอพคลังสินค้า
    1.  ใน Finance and Operations ไปที่ **การจัดการระบบ** &gt; **ทั่วไป** &gt; **ผู้ใช้**
    2.  สร้างผู้ใช้ใหม่
    3.  กำหนดผู้ใช้อุปกรณ์เคลื่อนที่คลังสินค้าดังที่แสดงไว้ในภาพหน้าจอต่อไปนี้ [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  เชื่อมโยงแอพลิเคชัน Azure Active Directory ของคุณกับผู้ใช้แอพคลังสินค้า
    1.  ใน Finance and Operations ไปที่ **การจัดการระบบ** &gt; **การตั้งค่า** &gt; **แอพลิเคชัน Azure Active Directory**
    2.  สร้างบรรทัดใหม่ 
    3.  ป้อน **รหัสไคลเอนต์** (ได้รับมาในส่วนสุดท้าย) ตั้งชื่อ และเลือกผู้ใช้ที่สร้างไว้ก่อนหน้านี้ เราขอแนะนำให้คุณติดแท็กให้กับอุปกรณ์ทุกเครื่องของคุณเพื่อให้คุณสามารถลบสิทธิ์การเข้าถึง Finance and Operations จากหน้านี้ได้อย่างง่ายดายในกรณีที่อุปกรณ์ของคุณหายไป [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>ตั้งค่าคอนฟิกแอพลิเคชัน
คุณต้องตั้งค่าคอนฟิกแอพบนอุปกรณ์เพื่อเชื่อมต่อกับเซิร์ฟเวอร์ Finance and Operations ผ่านทางแอพลิเคชัน Azure AD เมื่อต้องการทำเช่นนี้ ให้ทำตามขั้นตอนต่อไปนี้

1.  ในแอพ ไปที่ **การตั้งค่าการเชื่อมต่อ**
2.  ล้างฟิลด์ **โหมดสาธิต** <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  ป้อนข้อมูลต่อไปนี้ 
    + **รหัสไคลของเอนต์ Azure Active Directory** - รหัสของไคลเอนต์จะได้รับในขั้นตอนที่ 13 ใน "สร้างแอพบริการเว็บใน Active Directory" 
    + **ข้อมูลลับไคลเอนต์ Azure Active Directory** - ข้อมูลลับไคลเอนต์จะได้รับในขั้นตอนที่ 13 ใน "สร้างแอพบริการเว็บใน Active Directory" 
    + **ทรัพยากร Azure Active Directory** - ทรัพยากร Azure AD Directory แสดง URL รากของ Finance and Operations **หมายเหตุ**: อย่าลงท้ายฟิลด์นี้ด้วยอักขระทับ (/) 
    + **ผู้เช่า Azure Active directory** - ผู้เช่า Azure AD Directory ที่ใช้กับเซิร์ฟเวอร์ Finance and Operations: https://login.windows.net/your-AD-tenant-ID ตัวอย่าง: https://login.windows.net/contosooperations.onmicrosoft.com
    <br>**หมายเหตุ**: อย่าลงท้ายฟิลด์นี้ด้วยอักขระทับ (/) 
    + **บริษัท** - ป้อนนิติบุคคลใน Finance and Operations ที่คุณต้องการให้แอพลิเคชันเชื่อมต่อด้วย <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  เลือกปุ่ม **ย้อนกลับ** ที่มุมซ้ายด้านบนของแอพลิเคชัน ในขณะนี้แอพลิเคชันจะเชื่อมต่อกับเซิร์ฟเวอร์ Finance and Operations ของคุณและระบบจะแสดงหน้าจอการเข้าสู่ระบบสำหรับผู้ปฏิบัติงานคลังสินค้า <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>ลบการเข้าถึงออกจากอุปกรณ์
ในกรณีที่อุปกรณ์สูญหายหรือระบบถูกโจมตี คุณต้องลบการเข้าถึง Finance and Operations ออกจากอุปกรณ์ ขั้นตอนต่อไปนี้อธิบายกระบวนการที่แนะนำในการลบการเข้าถึง

1.  ใน Finance and Operations ไปที่ **การจัดการระบบ** &gt; **การตั้งค่า** &gt; **แอพลิเคชัน Azure Active Directory**
2.  ลบบรรทัดที่สอดคล้องกับอุปกรณ์ที่คุณต้องการลบการเข้าถึง บันทึก **รหัสไคลเอนต์** ที่ใช้สำหรับอุปกรณ์ที่ถูกลบออก
3.  เข้าสู่ระบบในพอร์ทัล Azure แบบคลาสสิกใน <https://manage.windowsazure.com>
4.  คลิกไอคอน **Active Directory** บนเมนูด้านซ้าย แล้วคลิกไดเรกทอรีที่ต้องการ
5.  บนเมนูด้านบน คลิก **แอพลิเคชัน** แล้วคลิกแอพลิเคชันที่คุณต้องการตั้งค่าคอนฟิก หน้า **เริ่มต้นอย่างรวดเร็ว** จะแสดงพร้อมกับข้อมูลการเซ็นชื่อเดียวและการตั้งค่าคอนฟิกอื่น ๆ
6.  คลิกแท็บ **ตั้งค่าคอนฟิก** เลื่อนลงและตรวจสอบให้แน่ใจว่า **รหัสไคลเอนต์** ของแอพลิเคชันเหมือนกับในขั้นตอนที่ 2 ในส่วนนี้
7.  คลิกปุ่ม **ลบ** ในแถบคำสั่ง
8.  คลิก **ใช่** ในข้อความยืนยัน





