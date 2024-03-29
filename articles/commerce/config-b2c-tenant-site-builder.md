---
title: ตั้งค่าคอนฟิกผู้เช่า B2C ของคุณในโปรแกรมสร้างไซต์ Commerce
description: บทความนี้จะอธิบายวิธีการตั้งค่าคอนฟิกผู้เช่าของธุรกิจ-ผู้บริโภค (B2C) ในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785312"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>ตั้งค่าคอนฟิกผู้เช่า B2C ของคุณในโปรแกรมสร้างไซต์ Commerce

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายวิธีการตั้งค่าคอนฟิกผู้เช่าของธุรกิจ-ผู้บริโภค (B2C) ในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce

เมื่อการตั้งค่าของผู้เช่า Azure AD B2C ของคุณเสร็จสมบูรณ์แล้ว คุณต้องตั้งค่าคอนฟิกผู้เช่า B2c ในโปรแกรมสร้างไซต์ Commerce ขั้นตอนการตั้งค่าคอนฟิกรวมถึงการรวบรวมข้อมูลแอปพลิเคชัน B2C จากพอร์ทัล Azure การป้อนข้อมูลแอปพลิเคชัน B2C ลงในโปรแกรมสร้างไซต์ และจากนั้น เชื่อมโยงแอปพลิเคชัน B2C กับไซต์และช่องทางของคุณ

### <a name="collect-the-required-application-information"></a>รวบรวมข้อมูลแอปพลิเคชันที่จำเป็น

เมื่อต้องการรวบรวมข้อมูลแอปพลิเคชันที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้

1. ในพอร์ทัล Azure ให้ไปที่ **หน้าหลัก \> Azure AD B2C - การลงทะเบียนแอป**
1. เลือกแอปพลิเคชันของคุณ และจากนั้น ในบานหน้าต่างนำทางด้านซ้าย เลือก **ภาพรวม** เพื่อดูรายละเอียดแอปพลิเคชัน
1. จากการอ้างอิง **รหัสแอปพลิเคชัน (ไคลเอ็นต์)** ให้รวบรวมรหัสแอปพลิเคชันของแอปพลิเคชัน B2C ที่สร้างขึ้นในผู้เช่า B2C ของคุณ นี่จะถูกป้อนเป็น **GUID ของไคลเอ็นต์** ในโปรแกรมสร้างไซต์ในภายหลัง
1. เลือก **URL การเปลี่ยนเส้นทาง** และรวบรวม URL การตอบกลับที่แสดงไว้สำหรับไซต์ของคุณ (URL การตอบกลับที่ป้อนเมื่อตั้งค่า)
1. ไปที่ **หน้าหลัก \> Azure AD B2C – ขั้นตอนผู้ใช้** แล้วรวบรวมชื่อเต็มของนโยบายขั้นตอนของผู้ใช้แต่ละรายการ

รูปภาพต่อไปนี้แสดงตัวอย่างของหน้าภาพรวมของ **Azure AD B2C - การลงทะเบียนแอป**

![Azure AD B2C - หน้าภาพรวมของการลงทะเบียนแอปที่มีการเน้นรหัสแอปพลิเคชัน (ไคลเอ็นต์)](./media/ClientGUID_Application_AzurePortal.png)

รูปภาพต่อไปนี้แสดงตัวอย่างของนโยบายขั้นตอนของผู้ใช้ในหน้า **Azure AD B2C – ขั้นตอนผู้ใช้ (นโยบาย)**

![รวบรวมชื่อของโฟลว์ของนโยบาย B2C แต่ละรายการ](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>ป้อนข้อมูลแอปพลิเคชันของผู้เช่า Azure AD B2C ของคุณลงใน Commerce

คุณต้องป้อนรายละเอียดของผู้เช่า Azure AD ผู้เช่า ลงในโปรแกรมสร้างไซต์ Commerce ก่อนที่จะเชื่อมโยงผู้เช่า B2C กับไซต์ของคุณ

เมื่อต้องการเพิ่มข้อมูลแอปพลิเคชันของผู้เช่า Azure AD B2C ลงใน Commerce ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้ในฐานะผู้ดูแลระบบในโปรแกรมสร้างไซต์ Commerce สำหรับสภาพแวดล้อมของคุณ
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** เพื่อขยาย
1. ภายใต้ **การตั้งค่าผู้เช่า** เลือก **การตั้งค่าการรับรองความถูกต้องของไซต์** 
1. ในหน้าต่างหลักถัดจาก **โพรไฟล์การรับรองความถูกต้องของไซต์** ให้เลือก **จัดการ** (ถ้าผู้เช่าของคุณปรากฎในรายการโพรไฟล์การรับรองความถูกต้องของไซต์ แสดงว่ามีการเพิ่มโดยผู้ดูแลระบบแล้ว ตรวจสอบว่ารายการในขั้นตอนที่ 6 ข้างล่างนี้ตรงกับรายการสำหรับการตั้งค่า B2C ที่กำหนดของคุณหรือไม่ โพรไฟล์ใหม่ยังสามารถสร้างโดยใช้ผู้เช่าหรือแอปพลิเคชัน Azure AD B2C ที่คล้ายกันโดยมีความแตกต่างเล็กน้อย เช่น รหัสนโยบายผู้ใช้ที่แตกต่างกัน)
1. เลือก **เพิ่มโพรไฟล์การรับรองความถูกต้องของไซต์**
1. ป้อนรายการที่จำเป็นต่อไปนี้ในฟอร์มที่แสดง โดยใช้ค่าจากผู้เช่า B2C และแอปพลิเคชันของคุณ ฟิลด์ที่ไม่จำเป็น (ฟิลด์ที่ไม่มีเครื่องหมายดอกจัน) อาจถูกปล่อยว่างไว้

    - **ชื่อแอปพลิเคชัน**: ชื่อสำหรับแอปพลิเคชัน B2C ของคุณ ตัวอย่างเช่น "Fabrikam B2C"
    - **ชื่อผู้เช่า**: ชื่อของผู้เช่า B2C ของคุณ (ตัวอย่างเช่น ใช้ "fabrikam" ถ้าโดเมนปรากฏเป็น "fabrikam.onmicrosoft.com" สำหรับผู้เช่า B2C) 
    - **รหัสนโยบายของการลืมรหัสผ่าน**: รหัสนโยบายของขั้นตอนผู้ใช้ในการลืมรหัสผ่าน ตัวอย่างเช่น "B2C_1_PasswordReset"
    - **รหัสนโยบายของการลงทะเบียนและการลงชื่อเข้าใช้** รหัสนโยบายของขั้นตอนผู้ใช้ในการลงทะเบียนและการลงชื่อเข้าใช้ ตัวอย่างเช่น "B2C_1_signup_signin"
    - **GUID ของไคลเอ็นต์**: รหัสแอปพลิเคชัน B2C ตัวอย่างเช่น "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6"
    - **รหัสนโยบายของการแก้ไขโพรไฟล์**: รหัสนโยบายของขั้นตอนของผู้ใช้ในการแก้ไขโพรไฟล์ ตัวอย่างเช่น "B2C_1A_ProfileEdit"

1. เลือก **ตกลง** ขณะนี้คุณควรดูชื่อของแอปพลิเคชัน B2C ของคุณที่ปรากฏในรายการ
1. เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณ

ควรใช้ฟิลด์ **โดเมนที่กำหนดเองสำหรับการเข้าสู่ระบบ** ซึ่งไม่บังคับเฉพาะเมื่อคุณตั้งค่าโดเมนที่กำหนดเองของผู้เช่า Azure AD B2C เท่านั้น สำหรับรายละเอียดเพิ่มเติมและข้อควรพิจารณาเกี่ยวกับการใช้ฟิลด์ **โดเมนที่กำหนดเองสำหรับการเข้าสู่ระบบ** ดูที่ [ข้อมูล B2C เพิ่มเติม](additional-b2c-info.md)

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>เชื่อมโยงแอปพลิเคชัน B2C กับไซต์และช่องทางของคุณ

> [!WARNING]
> - ถ้าไซต์ของคุณเชื่อมโยงกับแอปพลิเคชัน B2C อยู่แล้ว การเปลี่ยนไปยังแอปพลิเคชัน B2C อื่นจะลบการอ้างอิงปัจจุบันที่สร้างขึ้นสำหรับผู้ใช้ที่ลงชื่อสมัครในสภาพแวดล้อมนี้แล้ว ถ้ามีการเปลี่ยนแปลง ข้อมูลประจำตัวใดๆ ที่เชื่อมโยงกับแอปพลิเคชัน B2C ที่กำหนดไว้ในปัจจุบันจะไม่พร้อมใช้งานสำหรับผู้ใช้ 
> - ปรับปรุงเฉพาะแอปพลิเคชัน B2C ถ้าคุณกำลังตั้งค่าแอปพลิเคชัน B2C ของช่องทางเป็นครั้งแรก หรือถ้าคุณต้องการให้ผู้ใช้ลงชื่อสมัครอีกครั้งโดยใช้ข้อมูลประจำตัวใหม่ไปยังช่องทางนี้กับแอปพลิเคชัน B2C ใหม่ ใช้ความระมัดระวังเมื่อเชื่อมโยงช่องทางไปยังแอปพลิเคชัน B2C และมีการระบุชื่อแอปพลิเคชันอย่างชัดแจ้ง ถ้าช่องทางไม่เชื่อมโยงกับแอปพลิเคชัน B2C ในขั้นตอนด้านล่าง ผู้ใช้ที่ลงชื่อเข้าใช้ในช่องทางดังกล่าวสำหรับไซต์ของคุณจะถูกป้อนลงในแอปพลิเคชัน B2C ที่แสดงเป็น **ค่าเริ่มต้น** ในรายการ **การตั้งค่าผู้เช่า \> การตั้งค่า B2C** ของแอปพลิเคชัน

เพื่อเชื่อมโยงแอปพลิเคชัน B2C กับไซต์และช่องทางของคุณ ให้ทำตามขั้นตอนเหล่านี้

1. นำทางไปยังไซต์ของคุณในโปรแกรมสร้างไซต์ Commerce
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าไซต์** เพื่อขยาย
1. ด้านล่าง **การตั้งค่าไซต์** เลือก **ช่องทาง**
1. ในหน้าต่างหลักภายใต้ **ช่องทาง** เลือกช่องทางของคุณ
1. ในบานหน้าต่างคุณสมบัติช่องทางทางด้านขวา ให้เลือกชื่อแอปพลิเคชัน B2C ของคุณจากเมนูแบบหล่นลงของ **เลือกแอปพลิเคชัน B2C**
1. เลือก **ปิด** แล้วเลือก **บันทึกและเผยแพร่**

## <a name="next-steps"></a>ขั้นตอนถัดไป

เมื่อต้องการดําเนินการตั้งค่าผู้เช่า B2C ใน Commerce ต่อไป ให้ดําเนินการ [ข้อมูล B2C เพิ่มเติม](additional-b2c-info.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าผู้เช่า B2C ใน Commerce](set-up-b2c-tenant.md)

[สร้างหรือเชื่อมโยงกับผู้เช่า Azure AD B2C ที่มีอยู่ในพอร์ทัล Azure](create-link-aad-b2c-tenant.md)

[สร้างแอปพลิเคชัน B2C](create-b2c-app.md)

[สร้างนโยบายขั้นตอนของผู้ใช้](create-user-flow-policies.md)

[เพิ่มผู้ให้บริการข้อมูลประจำตัวทางสังคม (เลือกกำหนดได้)](add-social-identity-providers.md)

[อัปเดต Commerce headquarters ด้วยข้อมูล Azure AD B2C ใหม่](update-hq-aad-b2c-info.md)

[ข้อมูล B2C เพิ่มเติม](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
