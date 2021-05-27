---
title: ลิงค์การลงชื่อเข้าใช้จะเปลี่ยนเส้นทางกลับไปยังไซต์อีคอมเมิร์ซ
description: หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อลิงค์การลงชื่อเข้าใช้เปลี่ยนเส้นทางกลับไปที่ไซต์อีคอมเมิร์ซ แทนที่จะไปที่หน้าลงชื่อเข้าใช้
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a1d0ae4e487c391020947c607d5d7cb5d1ba6af4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020614"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>ลิงค์การลงชื่อเข้าใช้จะเปลี่ยนเส้นทางกลับไปยังไซต์อีคอมเมิร์ซ

[!include [banner](../../includes/banner.md)]

หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อลิงค์การลงชื่อเข้าใช้เปลี่ยนเส้นทางกลับไปที่ไซต์อีคอมเมิร์ซ แทนที่จะไปที่หน้าลงชื่อเข้าใช้

## <a name="description"></a>คำอธิบาย

หลังจากที่คุณตั้งค่าคอนฟิกผู้เช่า Microsoft Azure Active Directory B2C (Azure AD B2C) ใหม่ในโปรแกรมสร้างไซต์ Commerce แล้ว ผู้ใช้ที่เลือกลิงค์  **การลงชื่อเข้าใช้** จะเปลี่ยนเส้นทางกลับไปที่หน้าเชื่อมโยงสินค้าอีคอมเมิร์ซหลักโดยไม่ไปที่หน้าการลงชื่อเข้าใช้

## <a name="resolution"></a>ความละเอียด

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>ยืนยันว่าการตอบ URL ได้รับการตั้งค่าคอนฟิกในแอปพลิเคชัน Azure AD B2C อย่างถูกต้อง

ในการยืนยันว่าการตอบ URL ได้รับการตั้งค่าคอนฟิกในแอปพลิเคชัน Azure AD B2C อย่างถูกต้อง ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ [พอร์ทัล Azure](https://portal.azure.com/)
1. เลือกแอปพลิเคชัน Azure AD B2C ที่คุณสร้างขึ้นเพื่อการเข้าถึงไซต์ของคุณ
1. เลือกแอปพลิเคชันที่คุณสร้างขึ้นระหว่างการตั้งค่า Azure AD B2C
1. ภายใต้ **การตอบ URL** ตรวจสอบให้แน่ใจว่ารายการมีรายการทั้ง URL โดเมนไซต์และ URL ที่สร้างขึ้นโดยอีคอมเมิร์ซดังที่แสดงในตัวอย่างในภาพต่อไปนี้

    ![รายการการตอบ URL Azure AD B2C](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> ทั้ง URL โดเมนไซต์และ URL ที่สร้างโดยอีคอมเมิร์ซต้องอยู่ในรูปแบบ URL ที่ถูกต้องซึ่งไม่รวมเครื่องหมายทับนำหน้าหรือต่อท้าย

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ลงทะเบียนแอปพลิเคชันเว็บใน Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[ตั้งค่าผู้เช่า B2C ใน Commerce](../set-up-b2c-tenant.md)