---
title: ติดตั้งและกำหนดค่าภาพรวมแอปคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการติดตั้งและกำหนดค่า Dynamics 365 for Finance and Operations
author: MarkusFogelberg
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52882ef7542bfedebdae4a08de8404cddd01ed55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205609"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>ติดตั้งและกำหนดค่าภาพรวมแอปคลังสินค้า

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคลังสินค้าสำหรับการปรับใช้ cloud ถ้าคุณกำลังค้นหาวิธีการตั้งค่าคอนฟิกคลังสินค้าสำหรับการปรับใช้ในองค์กร โปรดดู [คลังสินค้าสำหรับการปรับใช้ในองค์กร](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md)


หัวข้อนี้อธิบายวิธีการติดตั้งและกำหนดค่า Dynamics 365 for Finance and Operations

แอปคลังสินค้ามีอยู่ใน Google Play Store และ Windows Store สำหรับ Dynamics 365 Supply Chain Management รุ่นปัจจุบัน แอพลิเคชันนี้มีไว้สำหรับเป็นส่วนประกอบแบบสแตนด์อโลน ซึ่งหมายถึงการปรับใช้ด้วยตนเองบนอุปกรณ์ที่ใช้สำหรับงานคลังสินค้า เมื่อต้องการใช้แอพลิเคชัน คุณต้องดาวน์โหลดแอปบนอุปกรณ์แต่ละเครื่องและตั้งค่าคอนฟิกเพื่อเชื่อมต่อกับสภาพแวดล้อมของ Supply Chain Management หัวข้อนี้อธิบายวิธีการติดตั้งแอพบนอุปกรณ์ของคุณ นอกจากนี้ยังอธิบายถึงวิธีการตั้งค่าคอนฟิกแอพเพื่อเชื่อมต่อกับสภาพแวดล้อม Supply Chain Management ของคุณ

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น
แอปพร้อมใช้งานในระบบปฏิบัติการ Android และ Windows เมื่อต้องการใช้แอพนี้ คุณต้องใช้ระบบปฏิบัติการที่ได้รับการสนับสนุนต่อไปนี้ที่ติดตั้งบนอุปกรณ์ของคุณอย่างใดอย่างหนึ่ง คุณต้องมีหนึ่งในรุ่นที่รองรับต่อไปนี้ด้วย ใช้ข้อมูลในตารางต่อไปนี้ในการประเมินว่าสภาพแวดล้อมของฮาร์ดแวร์และซอฟต์แวร์ของคุณพร้อมที่จะสนับสนุนการติดตั้งหรือไม่

| แพลตฟอร์ม                    | รุ่น                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0, 9.0                                                                                                                                                     |
| % 1                | Windows 10 (ทุกรุ่น)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations รุ่น 1611 <br>หรือ <br>Microsoft Dynamics AX รุ่น 7.0/7.0.1 และ Microsoft Dynamics AX การปรับปรุงแพลตฟอร์ม 2 พร้อมกับโปรแกรมแก้ไขด่วน KB 3210014 |

## <a name="get-the-app"></a>เรียกกลุ่มแอพลิเคชัน
-   % 1 
     - [Finance and Operations - คลังสินค้าบน Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - คลังสินค้าบน Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> แกลเลอรีแอป Zebra ได้ถูกเลิกใช้ ซึ่งหมายความว่าแอป Warehousing จะไม่พร้อมใช้งานอีกต่อไปสำหรับการดาวน์โหลดจากสถานที่นั้น

## <a name="create-a-web-service-application-in-azure-active-directory"></a>สร้างแอพลิเคชัน Web Service ใน Azure Active Directory
เพื่อเปิดใช้งานแอปให้ทำงานกับเซิร์ฟเวอร์ Supply Chain Management เฉพาะ คุณต้องลงทะเบียนแอพลิเคชัน Web Service ในผู้เช่า Azure Active Directory สำหรับ Supply Chain Management สำหรับเหตุผลด้านความปลอดภัย เราขอแนะนำให้คุณสร้างแอพบริการเว็บสำหรับแต่ละอุปกรณ์ที่คุณใช้ เพื่อสร้างแอพลิเคชัน Web Service ใน Azure Active Directory (Azure AD) ให้ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์:

1.  ในเว็บเบราเซอร์ ไปที่ <https://portal.azure.com>
2.  ป้อนชื่อและรหัสผ่านสำหรับผู้ใช้ที่มีสิทธิ์เข้าถึงการสมัครใช้งาน Azure
3.  ในพอร์ทัล Azure ในบานหน้าต่างนำทางด้านซ้าย ให้คลิก **Azure Active Directory**

    [![WMA-01-ใช้งาน-ไดเรกทอรี-ตัวอย่าง](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)

4.  ตรวจสอบว่าอินสแตนซ์ของ Active Directory เป็นรายการที่ถูกใช้โดย Supply Chain Management
5.  ในรายการ คลิก **การลงทะเบียนแอพ** 

    [![WMA-02-ใช้งาน-ไดเรกทอรี-แอพ-การลงทะเบียน](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)

6.  ในบานหน้าต่างด้านบนสุด คลิก **การลงทะเบียนใหม่** ตัวช่วยสร้าง **ลงทะเบียนแอพลิเคชัน** เริ่มทำงาน
7.  ป้อนชื่อของแอพลิเคชันและ **เลือกบัญชีในไดเรกทอรี**ขององค์กรนี้เท่านั้น คลิก **ลงทะเบียน**  

    [![WMA-03-ใช้งาน-ไดเรกทอรี-เพิ่ม-แอพลิเคชัน](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)

8.  การลงทะเบียนแอปใหม่ของคุณจะเปิดขึ้น 

    [![WMA-04-ใช้งาน-ไดเรกทอรี-ตั้งค่าคอนฟิก-แอพ](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)

9.  อย่าลืม **รหัสแอพลิเคชัน** คุณจะต้องใช้ข้อมูลนี้ในภายหลัง ในภายหลัง **รหัสแอพลิเคชัน** จะถูกเรียกว่าเป็น **รหัสไคลเอนต์**
10. คลิก**ใบรับรอง** & ความ**ลับ**ในบานหน้าต่างจัดการ คลิกที่**ลับ**ใหม่ของไคลเอนต์ 

    [![WMA-05-ใช้งาน-ไดเรกทอรี-สร้าง-คีย์](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

11. สร้างคีย์ โดยการป้อนคำอธิบายคีย์และระยะเวลาในส่วน **รหัสผ่าน** คลิก **เพิ่ม** และคัดลอกคีย์ ในภายหลังจะเรียกคีย์นี้ว่า **ข้อมูลลับไคลเอนต์** 

    [![WMA-06-ใช้งาน-ไดเรกทอรี-บันทึก-คีย์](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>สร้างและตั้งค่าคอนฟิกบัญชีผู้ใช้ใน Supply Chain Management
เพื่อเปิดใช้งาน Supply Chain Managementto เพื่อใช้แอพลิเคชัน Azure AD ของคุณ คุณต้องทำขั้นตอนการตั้งค่าคอนฟิกต่อไปนี้ให้เสร็จสมบูรณ์:

1.  สร้างผู้ใช้ที่สอดคล้องกับข้อมูลประจำตัวผู้ใช้แอพคลังสินค้า
    1.  ไปที่ **การจัดการระบบ** &gt; **ทั่วไป** &gt; **ผู้ใช้**
    2.  สร้างผู้ใช้ใหม่
    3.  กำหนดผู้ใช้อุปกรณ์เคลื่อนที่คลังสินค้าดังที่แสดงไว้ในภาพหน้าจอต่อไปนี้ 
    
        [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  เชื่อมโยงแอพลิเคชัน Azure Active Directory ของคุณกับผู้ใช้แอปคลังสินค้า
    1.  ใน Supply Chain Management ไปที่ **การดูแลระบบ** &gt; **การตั้งค่า** &gt; **แอพลิเคชัน Azure Active Directory**
    2.  สร้างบรรทัดใหม่ 
    3.  ป้อน **รหัสไคลเอนต์** (ได้รับมาในส่วนสุดท้าย) ตั้งชื่อ และเลือกผู้ใช้ที่สร้างไว้ก่อนหน้านี้ เราขอแนะนำให้คุณติดแท็กให้กับอุปกรณ์ทุกเครื่องของคุณเพื่อให้คุณสามารถลบสิทธิ์การเข้าถึง Supply Chain Management จากหน้านี้ได้อย่างง่ายดายในกรณีที่อุปกรณ์ของคุณหายไป 
    
        [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>ตั้งค่าคอนฟิกแอพลิเคชัน
คุณต้องตั้งค่าคอนฟิกแอปบนอุปกรณ์เพื่อเชื่อมต่อในเซิร์ฟเวอร์ Supply Chain Management ผ่านทางแอพลิเคชัน Azure AD เมื่อต้องการทำเช่นนี้ ให้ทำตามขั้นตอนต่อไปนี้

1.  ในแอพ ไปที่ **การตั้งค่าการเชื่อมต่อ**
2.  ล้างฟิลด์ **โหมดสาธิต** <br>

    [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)

3.  ป้อนข้อมูลต่อไปนี้ 
    + **รหัสไคลของเอนต์ Azure Active directory** - รหัสของไคลเอนต์จะได้รับในขั้นตอนที่ 9 ใน "สร้างแอพบริการเว็บใน Active Directory" 
    + **ข้อมูลลับไคลเอนต์ Azure Active directory** - ข้อมูลลับไคลเอนต์จะได้รับในขั้นตอนที่ 11 ใน "สร้างแอพบริการเว็บใน Active Directory" 
    + **ทรัพยากร Azure Active directory** - ทรัพยากรไดเรกทอรี Azure AD แสดง URL รากของ Supply Chain Management 
    
        > [!NOTE]
        > อย่าลงท้ายฟิลด์นี้ด้วยอักขระทับ (/) 

    + **ผู้เช่า Azure Active directory** - ผู้เช่าไดเรกทอรี Azure AD ที่ใช้กับเซิร์ฟเวอร์ Supply Chain Management: `https://login.windows.net/your-AD-tenant-ID` ตัวอย่างเช่น: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    
        > [!NOTE]
        > อย่าลงท้ายฟิลด์นี้ด้วยอักขระทับ (/) 
    
    + **บริษัท** - ป้อนนิติบุคคลใน Supply Chain Management ที่คุณต้องการให้แอพลิเคชันเชื่อมต่อด้วย <br>
    
    [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)

4.  เลือกปุ่ม **ย้อนกลับ** ที่มุมซ้ายด้านบนของแอพลิเคชัน ในขณะนี้แอพลิเคชันจะเชื่อมต่อกับเซิร์ฟเวอร์ Supply Chain Management ของคุณและระบบจะแสดงหน้าจอการเข้าสู่ระบบสำหรับผู้ปฏิบัติงานคลังสินค้า

    [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าแอพพลิเคชั่น Warehousing ที่จะสแกนบาร์โค้ดโดยใช้กล้องบนอุปกรณ์มือถือ ดู [สแกนบาร์โค้ดโดยใช้กล้องใน Dynamics 365 for Finance and Operations  - แอปคลังสินค้า](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>ลบการเข้าถึงออกจากอุปกรณ์
ในกรณีที่อุปกรณ์สูญหายหรือระบบถูกโจมตี คุณต้องลบการเข้าถึง Supply Chain Management ออกจากอุปกรณ์ ขั้นตอนต่อไปนี้อธิบายกระบวนการที่แนะนำในการลบการเข้าถึง

1.  ไปที่ **การจัดการระบบ** &gt; **การตั้งค่า** &gt; แอพพลิเคชั่น **Azure Active Directory**
2.  ลบบรรทัดที่สอดคล้องกับอุปกรณ์ที่คุณต้องการลบการเข้าถึง อย่าลืม **รหัสไคลเอนต์** ที่ใช้สำหรับอุปกรณ์ที่ลบออก คุณจะต้องใช้ข้อมูลนี้ในภายหลัง
3.  ล็อกอินไปยังพอร์ทัล Azure ที่ <https://portal.azure.com>
4.  คลิกไอคอน **Active Directory** บนเมนูซ้าย และให้แน่ใจว่าคุณอยู่ในไดเรกทอรีที่ถูกต้อง
5.  ในรายการ คลิก **การลงทะเบียนแอพ** แล้วคลิกแอพลิเคชันที่คุณต้องการตั้งค่าคอนฟิก หน้า **การตั้งค่า** จะปรากฏขึ้นพร้อมด้วยข้อมูลการตั้งค่าคอนฟิก
6.  ให้แน่ใจว่า **รหัสไคลเอนต์** ของแอพลิเคชันเหมือนกับในขั้นตอนที่ 2 ในส่วนนี้
7.  คลิกปุ่ม **ลบ** ในบานหน้าต่างด้านบน
8.  คลิก **ใช่** ในข้อความยืนยัน
