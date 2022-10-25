---
title: ติดตั้งโซลูชัน Invoice Capture
description: บทความนี้มีข้อมูลเกี่ยวกับวิธีการติดตั้งโซลูชัน Invoice Capture และรวมกับ Microsoft Dynamics 365 Finance
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691224"
---
# <a name="install-the-invoice-capture-solution"></a>ติดตั้งโซลูชัน Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> ถ้าคุณติดตั้งโซลูชันแสดงตัวอย่างส่วนตัว คุณต้องถอนการติดตั้งโซลูชันเก่าก่อนที่คุณจะต่อ

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะติดตั้งโซลูชัน Invoice Capture คุณต้องดำเนินการข้อกำหนดเบื้องต้นต่อไปนี้ให้เสร็จสมบูรณ์:

1. ให้ลงทะเบียนแอปพลิเคชัน และเพิ่มข้อมูลลับไคลเอนต์ลงใน Microsoft Azure Active Directory (Azure AD) ภายใต้การบอกรับเป็นสมาชิก Azure ของคุณ หากต้องการข้อมูลเพิ่มเติม โปรดดู [ลงทะเบียนแอปพลิเคชันเว็บด้วย AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad)

    > [!NOTE]
    > จดบันทึก **รหัสแอปพลิเคชัน (ไคลเอนต์)** **ข้อมูลลับไคลเอนต์** และ **รหัสผู้เช่า** เนื่องจากคุณจะต้องใช้ในภายหลัง

2. ลงทะเบียนแอปพลิเคชัน Azure ในสภาพแวดล้อม Dynamics 365 Finance หากต้องการข้อมูลเพิ่มเติม โปรดดู [ลงทะเบียนแอปพลิเคชันภายนอกของคุณ](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application)

## <a name="install-and-set-up-the-solution"></a>ติดตั้งและตั้งค่าโซลูชัน

เมื่อต้องการติดตั้งโซลูชัน Invoice Capture ให้ไปที่ AppSource และเลือกลิงค์เพื่อดูรุ่นตัวอย่างของ [Dynamics 365 Invoice Capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture) หลังจากการติดตั้งเสร็จสมบูรณ์แล้ว คุณจะเห็นโซลูชันที่ติดตั้งในสภาพแวดล้อมที่เลือกใน Power Apps

เพื่อให้การตั้งค่านี้เสร็จสมบูรณ์ ให้ปฏิบัติดังนี้

1. ดาวน์โหลด [โซลูชันผู้ช่วย](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) เพื่อตั้งค่ารายละเอียดต่อไปนี้:

    - การสื่อสารระหว่าง Microsoft Power Platform และสภาพแวดล้อม Finance
    - การอ้างอิงการเชื่อมต่อสำหรับ Dataverse และ Office 365 Outlook ที่จะใช้โดยช่องทาง

2. ใน Power Apps ให้ไปที่สภาพแวดล้อมของคุณ และเลือก **นําเข้าโซลูชัน**
3. เลือก **เรียกดู** เลือกแพคเกจโซลูชันผู้ช่วยที่คุณดาวน์โหลด แล้วเลือก **ถัดไป**
4. เลือก **ถัดไป**
5. กําหนดการเชื่อมต่อที่มีอยู่ หรือสร้างการเชื่อมต่อใหม่ด้วยการเลือก **การเชื่อมต่อใหม่**
6. หลังจากที่นําเข้าแพคเกจเสร็จเรียบร้อยแล้ว ให้เปิด **Dynamics 365 Invoice Capture – เครื่องมือการติดตั้ง**
7. รันโฟลว์ระบบคลาวด์เพื่อตั้งค่าการเชื่อมต่อระหว่างโซลูชัน Invoice Capture ใน Microsoft Power Platform และ Finance
8. เลือก **เรียกใช้** และระบุพารามิเตอร์ต่อไปนี้:

    - **URL ของ Dynamics 365 Finance** – URL ของสภาพแวดล้อม Finance ที่คุณต้องการรวมไว้ด้วย
    - **รหัสผู้เช่า** – รหัสผู้เช่าสำหรับสภาพแวดล้อม Finance
    - **รหัสไคลเอนต์** – รหัสแอปพลิเคชัน Azure ที่ลงทะเบียนไว้
    - **ข้อมูลลับไคลเอนต์** – ข้อมูลลับไคลเอนต์ที่สร้างขึ้นสำหรับแอปพลิเคชัน Azure
