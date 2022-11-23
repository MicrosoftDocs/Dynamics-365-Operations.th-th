---
title: ตั้งค่าผู้เช่า B2C ใน Commerce
description: บทความนี้จะอธิบายวิธีการตั้งค่าผู้เช่าของธุรกิจ-ผู้บริโภค (B2C) ของ Azure Active Directory (Azure AD) ของคุณสำหรับการตรวจสอบความถูกต้องของไซต์ของผู้ใช้ใน Microsoft Dynamics 365 Commerce
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785165"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>ตั้งค่าผู้เช่า B2C ใน Commerce

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายวิธีการตั้งค่าผู้เช่าของธุรกิจ-ผู้บริโภค (B2C) ของ Azure Active Directory (Azure AD) ของคุณสำหรับการตรวจสอบความถูกต้องของไซต์ของผู้ใช้ใน Dynamics 365 Commerce

Dynamics 365 Commerce ใช้ Azure AD B2C เพื่อสนับสนุนข้อมูลประจำตัวของผู้ใช้และขั้นตอนการตรวจสอบความถูกต้อง ผู้ใช้สามารถลงชื่อสมัคร ลงชื่อเข้าใช้ และรีเซ็ตรหัสผ่านของพวกเขาได้ผ่านขั้นตอนเหล่านี้ Azure AD B2C จัดเก็บข้อมูลการตรวจสอบความถูกต้องของผู้ใช้ที่สำคัญ เช่น ชื่อผู้ใช้ และรหัสผ่าน เรกคอร์ดผู้ใช้ในผู้เช่าของ B2C จะจัดเก็บเรกคอร์ดบัญชีเฉพาะที่ของ B2C หรือเรกคอร์ดผู้ให้บริการข้อมูลเฉพาะตัวทางสังคมของ B2C เรกคอร์ด B2C เหล่านี้จะเชื่อมโยงกลับไปยังเรกคอร์ดลูกค้าในสภาพแวดล้อม Commerce

> [!WARNING] 
> Azure AD B2C จะถอนโฟลว์ของผู้ใช้เก่า (ดั้งเดิม) ในวันที่ 1 สิงหาคม 2021 ดังนั้นคุณจึงควรวางแผนย้ายโฟลว์ของผู้ใช้ไปที่รุ่นที่แนะนำใหม่ รุ่นใหม่จะมีคุณลักษณะพาริตี้และคุณลักษณะใหม่ ควรใช้ไลบรารีโมดูลของ Commerce รุ่น 10.0.15 หรือสูงกว่ากับโฟลว์ผู้ใช้ B2C ที่แนะนำ สำหรับข้อมูลเพิ่มเติม ให้ดู [โฟลว์ผู้ใช้ใน Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview)
 
 > [!NOTE]
 > สภาพแวดล้อมการประเมิน Commerce มาพร้อมกับผู้เช่า Azure AD B2C ที่โหลดไว้ล่วงหน้าเพื่อวัตถุประสงค์ในการสาธิต การโหลดผู้เช่า Azure AD B2C ของคุณเองโดยใช้ขั้นตอนด้านล่างไม่เป็นข้อมูลที่ต้องระบุในสภาพแวดล้อมการประเมิน

> [!TIP]
> นอกจากนี้ คุณยังสามารถป้องกันผู้ใช้ไซต์ของคุณและเพิ่มประสิทธิภาพให้กับผู้เช่า B2C Azure AD ด้วยการคุ้มครองเอกลักษณ์และการเข้าถึงแบบมีเงื่อนไขของ Azure AD หากต้องการทบทวนความสามารถที่พร้อมใช้งานของผู้เช่า B2C Premium P1 และผู้เช่าค่าจ้างพิเศษ P2 ของ Azure AD ดูที่ [การคุ้มครองเอกลักษณ์และการเข้าถึงแบบมีเงื่อนไขของ Azure AD B2C](/azure/active-directory-b2c/conditional-access-identity-protection-overview)

## <a name="dynamics-environment-prerequisites"></a>ข้อกำหนดเบื้องต้นของสภาพแวดล้อม Dynamics

ก่อนที่คุณจะเริ่มต้น โปรดตรวจสอบให้แน่ใจว่าสภาพแวดล้อม Dynamics 365 Commerce และช่องทาง e-commerce ของคุณได้รับการตั้งค่าคอนฟิกอย่างเหมาะสม โดยปฏิบัติตามข้อกําหนดเบื้องต้นต่อไปนี้

- ตั้งค่า **AllowAnonymousAccess** ของการดําเนินงาน POS เป็น "1" ใน Commerce headquarters:
    1. ไปที่ **การดําเนินงาน POS**
    1. ในการดําเนินงาน คลิกขวาและเลือก **กำหนดให้เป็นส่วนตัว**
    1. เลือก **เพิ่มฟิลด์**
    1. ในรายการของคอลัมน์ที่มีอยู่ ให้เลือกคอลัมน์ **AllowAnonymousAccess** เพื่อเพิ่ม
    1. เลือก **ปรับปรุง**
    1. สำหรับการดําเนินงาน **612** "ลูกค้าเพิ่ม" ให้เปลี่ยน **AllowAnonymousAccess** เป็น "1"
    1. เรียกใช้งาน **1090 (เครื่องบันทึกเงินสด)**
- ตั้งค่าแอตทริบิวต์ **ด้วยตนเอง** ของบัญชีลูกค้าตามลำดับหมายเลขเป็น **ไม่** ใน Commerce headquarters:
    1. ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์บัญชีลูกหนี้**
    1. เลือก **ลำดับหมายเลข**
    1. ในแถว **บัญชีลูกค้า** ให้ดับเบิลคลิกที่ค่า **รหัสลำดับหมายเลข**
    1. บน FastTab **ทั่วไป** ของลำดับหมายเลข ให้ตั้งค่า **ด้วยตนเอง** เป็น **ไม่**

หลังจากการปรับใช้ของสภาพแวดล้อม Dynamics 365 Commerce ของคุณ ขอแนะนำให้ [เตรียมใช้งานข้อมูลเบื้องต้น](enable-configure-retail-functionality.md) ในสภาพแวดล้อมด้วย

## <a name="next-steps"></a>ขั้นตอนถัดไป

หากต้องการดําเนินการตั้งค่าผู้เช่า B2C ใน Commerce ต่อไป ให้ดําเนินงาน [สร้างหรือลิงค์ไปยังผู้เช่า Azure AD B2C ที่มีอยู่ ในพอร์ทัล Azure](create-link-aad-b2c-tenant.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[สร้างหรือเชื่อมโยงกับผู้เช่า Azure AD B2C ที่มีอยู่ในพอร์ทัล Azure](create-link-aad-b2c-tenant.md)

[สร้างแอปพลิเคชัน B2C](create-b2c-app.md)

[สร้างนโยบายขั้นตอนของผู้ใช้](create-user-flow-policies.md)

[เพิ่มผู้ให้บริการข้อมูลประจำตัวทางสังคม (เลือกกำหนดได้)](add-social-identity-providers.md)

[อัปเดต Commerce headquarters ด้วยข้อมูล Azure AD B2C ใหม่](update-hq-aad-b2c-info.md)

[ตั้งค่าคอนฟิกผู้เช่า B2C ของคุณในโปรแกรมสร้างไซต์ Commerce](config-b2c-tenant-site-builder.md)

[ข้อมูล B2C เพิ่มเติม](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
