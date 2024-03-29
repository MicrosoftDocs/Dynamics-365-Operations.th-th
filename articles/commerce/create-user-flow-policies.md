---
title: สร้างนโยบายขั้นตอนของผู้ใช้
description: บทความนี้จะอธิบายวิธีการสร้างนโยบายขั้นตอนของผู้ใช้ในพอร์ทัล Microsoft Azure
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785311"
---
# <a name="create-user-flow-policies"></a>สร้างนโยบายขั้นตอนของผู้ใช้

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายวิธีการสร้างนโยบายขั้นตอนของผู้ใช้ในพอร์ทัล Microsoft Azure

ขั้นตอนของผู้ใช้เป็นนโยบายที่ Azure Active Directory (Azure AD) ธุรกิจ-ผู้บริโภค (B2C) ใช้เพื่อให้ประสบการณ์การใช้งานของผู้ใช้ในการลงชื่อเข้าใช้ ลงชื่อสมัคร แก้ไขโพรไฟล์ และลืมรหัสผ่าน ที่มีความปลอดภัย Dynamics 365 Commerce ใช้ขั้นตอนเหล่านี้เพื่อดำเนินการกับนโยบายเพื่อโต้ตอบกับผู้เช่าของ Azure AD B2C เมื่อผู้ใช้โต้ตอบกับนโยบายเหล่านี้ จะมีการเปลี่ยนเส้นทางไปยังผู้เช่าของ Azure AD B2C เพื่อดำเนินการ

Azure AD B2C มีชนิดขั้นตอนของผู้ใช้พื้นฐานสามชนิดดังนี้:
- ลงชื่อสมัครใช้และลงชื่อเข้าใช้
- การแก้ไขโพรไฟล์
- รีเซ็ตรหัสผ่านแล้ว

คุณสามารถเลือกที่จะใช้ขั้นตอนของผู้ใช้เริ่มต้นที่ระบุโดย Azure AD ซึ่งจะแสดงหน้าที่โฮสต์โดย Azure AD B2C อีกทางหนึ่งคือ คุณสามารถสร้างหน้า HTML เพื่อควบคุมรูปลักษณ์และความรู้สึกของประสบการณ์ขั้นตอนของผู้ใช้เหล่านี้ 

เมื่อต้องการกำหนดหน้านโยบายผู้ใช้กับหน้าที่สร้างใน Dynamics 365 Commerce ให้ดูที่ [ตั้งค่าหน้าแบบกำหนดเองสำหรับล็อกอินของผู้ใช้](custom-pages-user-logins.md) สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [กำหนดค่าอินเทอร์เฟสของประสบการณ์การใช้งานของผู้ใช้ใน Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-customize-ui)

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>การสร้างนโยบายขั้นตอนของผู้ใช้ในการลงชื่อสมัครและการลงชื่อเข้าใช้

เมื่อต้องการสร้างนโยบายขั้นตอนของผู้ใช้ในการลงชื่อสมัครและการลงชื่อเข้าใช้ ให้ทำตามขั้นตอนต่อไปนี้

1. ในพอร์ทัล Azure เลือก **ขั้นตอนของผู้ใช้ (นโยบาย)** ในบานหน้าต่างนำทางด้านซ้าย
1. ในหน้า **Azure AD B2C – ขั้นตอนของผู้ใช้ (นโยบาย)** เลือก **ขั้นตอนของผู้ใช้ใหม่**
1. เลือกนโยบาย **การลงทะเบียนและลงชื่อเข้าใช้** และจากนั้นเลือกรุ่น **แนะนำ**
1. ภายใต้ **ชื่อ** ให้ป้อนชื่อนโยบาย ชื่อนี้จะแสดงขึ้นหลังจากที่มีคำนำหน้าที่พอร์ทัลกำหนด (ตัวอย่างเช่น "B2C_1_")
1. ภายใต้ **ผู้ให้บริการข้อมูลประจำตัว** ในส่วน **บัญชีภายใน** ให้เลือก **การลงทะเบียนอีเมล** การรับรองความถูกต้องของอีเมลจะใช้ในสถานการณ์ทั่วไปของ Commerce หากคุณยังใช้การรับรองความถูกต้องของผู้ให้บริการข้อมูลประจำตัวตามสังคมด้วย คุณยังสามารถเลือกสิ่งเหล่านี้ได้ในเวลาเดียวกัน
1. ภายใต้ **การตรวจสอบความถูกต้องของ Multifactor** เลือกตัวเลือกที่เหมาะสมสำหรับบริษัทของคุณ 
1. ภายใต้ **แอตทริบิวต์และการอ้างสิทธิ์ของผู้ใช้** เลือกตัวเลือกเพื่อรวบรวมแอตทริบิวต์หรือส่งคืนการอ้างสิทธิ์ตามความเหมาะสม เลือก **แสดงเพิ่มเติม...** เพื่อเรียกดูรายการทั้งหมดของแอตทริบิวต์และตัวเลือกการอ้างสิทธิ์ Commerce ต้องมีตัวเลือกเริ่มต้นต่อไปนี้:

    | **รวบรวมแอตทริบิวต์** | **การอ้างสิทธิ์การส่งคืนสินค้า** |
    | ---------------------- | ----------------- |
    | ที่อยู่อีเมล          | ที่อยู่อีเมล   |
    | ชื่อที่กำหนด             | ชื่อที่กำหนด        |
    |                        | ตัวให้บริการข้อมูลเฉพาะตัว |
    | นามสกุล                | นามสกุล           |
    |                        | รหัสออบเจ็กต์ของผู้ใช้  |

1. เลือก **สร้าง**

รูปภาพต่อไปนี้เป็นตัวอย่างของการลงชื่อเข้าใช้ของ Azure AD B2C และขั้นตอนของผู้ใช้ในการลงทะเบียนและการลงชื่อเข้าใช้

![การตั้งค่านโยบายในการลงทะเบียนและการลงชื่อเข้าใช้](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>สร้างนโยบายขั้นตอนของผู้ใช้ในการแก้ไขโพรไฟล์

เมื่อต้องการสร้างนโยบายขั้นตอนของผู้ใช้ในการแก้ไขโพรไฟล์ ให้ทำตามขั้นตอนต่อไปนี้

1. ในพอร์ทัล Azure เลือก **ขั้นตอนของผู้ใช้ (นโยบาย)** ในบานหน้าต่างนำทางด้านซ้าย
1. ในหน้า **Azure AD B2C – ขั้นตอนของผู้ใช้ (นโยบาย)** เลือก **ขั้นตอนของผู้ใช้ใหม่**
1. เลือก **การแก้ไขโปรไฟล์** แล้วเลือกรุ่น **แนะนำ**
1. ภายใต้ **ชื่อ** ให้ป้อนขั้นตอนของผู้ใช้ในการแก้ไขโพรไฟล์ ชื่อนี้จะแสดงขึ้นหลังจากที่มีคำนำหน้าที่พอร์ทัลกำหนด (ตัวอย่างเช่น "B2C_1_")
1. ภายใต้ **ผู้ให้บริการข้อมูลประจำตัว** ในส่วน **บัญชีภายใน** ให้เลือก **การลงชื่อเข้าใช้อีเมล**
1. ภายใต้ **แอตทริบิวต์ของผู้ใช้** เลือกกล่องกาเครื่องหมายใดๆ ต่อไปนี้:
    
    | **รวบรวมแอตทริบิวต์** | **การอ้างสิทธิ์การส่งคืนสินค้า** |
    | ---------------------- | ----------------- |
    |                        | ที่อยู่อีเมล   |
    | ชื่อที่กำหนด             | ชื่อที่กำหนด        |
    |                        | ตัวให้บริการข้อมูลเฉพาะตัว |
    | นามสกุล                | นามสกุล           |
    |                        | รหัสออบเจ็กต์ของผู้ใช้  |
    
1. เลือก **สร้าง**

รูปภาพต่อไปนี้แสดงตัวอย่างของขั้นตอนของผู้ใช้ในการแก้ไขโพรไฟล์ของ Azure AD B2C

![ตัวอย่างของผังลำดับผู้ใช้ในการแก้ไขโพรไฟล์ Azure AD B2C](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>สร้างนโยบายขั้นตอนของผู้ใช้ในการรีเซ็ตรหัสผ่าน

เมื่อต้องการสร้างนโยบายขั้นตอนของผู้ใช้ในการรีเซ็ตรหัสผ่าน ให้ทำตามขั้นตอนต่อไปนี้

1. ในพอร์ทัล Azure เลือก **ขั้นตอนของผู้ใช้ (นโยบาย)** ในบานหน้าต่างนำทางด้านซ้าย
1. ในหน้า **Azure AD B2C – ขั้นตอนของผู้ใช้ (นโยบาย)** เลือก **ขั้นตอนของผู้ใช้ใหม่**
1. เลือก **รีเซ็ตรหัสผ่าน** แล้วเลือกรุ่น **แนะนำ**
1. ภายใต้ **ชื่อ** ให้ป้อนชื่อสำหรับขั้นตอนของผู้ใช้ในการรีเซ็ตรหัสผ่าน
1. ภายใต้ **ตัวให้บริการข้อมูลเฉพาะ** เลือก **รีเซ็ตรหัสผ่านโดยใช้ที่อยู่อีเมล**
1. เลือก **สร้าง**
1. ภายใต้ **การเรียกร้องสิทธิ์ในแอปพลิเคชัน** เลือกกล่องกาเครื่องหมายต่อไปนี้:
    - **ที่อยู่อีเมล**
    - **ชื่อที่กำหนด**
    - **นามสกุล**
    - **รหัสออบเจ็กต์ของผู้ใช้**
1. เลือก **สร้าง**

รูปภาพต่อไปนี้แสดงตำแหน่งที่จะตั้งค่า **รีเซ็ตรหัสผ่านโดยใช้ที่อยู่อีเมล** ในขั้นตอนของผู้ใช้ในการรีเซ็ตรหัสผ่านของ Azure AD B2C

![ตั้งค่า "รีเซ็ตรหัสผ่านโดยใช้ที่อยู่อีเมล" ในนโยบายการรีเซ็ตรหัสผ่าน](./media/B2CImage_13.png)

## <a name="next-steps"></a>ขั้นตอนถัดไป

เมื่อต้องการดําเนินการตั้งค่าผู้เช่า B2C ใน Commerce ต่อไป ให้ดําเนินการ [เพิ่มผู้ให้บริการข้อมูลประจำตัวทางสังคม](add-social-identity-providers.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าผู้เช่า B2C ใน Commerce](set-up-b2c-tenant.md)

[สร้างหรือเชื่อมโยงกับผู้เช่า Azure AD B2C ที่มีอยู่ในพอร์ทัล Azure](create-link-aad-b2c-tenant.md)

[สร้างแอปพลิเคชัน B2C](create-b2c-app.md)

[เพิ่มผู้ให้บริการข้อมูลประจำตัวทางสังคม (เลือกกำหนดได้)](add-social-identity-providers.md)

[อัปเดต Commerce headquarters ด้วยข้อมูล Azure AD B2C ใหม่](update-hq-aad-b2c-info.md)

[ตั้งค่าคอนฟิกผู้เช่า B2C ของคุณในโปรแกรมสร้างไซต์ Commerce](config-b2c-tenant-site-builder.md)

[ข้อมูล B2C เพิ่มเติม](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
