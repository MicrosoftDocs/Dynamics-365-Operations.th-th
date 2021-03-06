---
title: ตั้งค่าหน้าแบบกำหนดเองสำหรับการลงชื่อเข้าใช้ของผู้ใช้
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างหน้าแบบกำหนดเองใน Microsoft Dynamics 365 Commerce ที่จัดการการลงชื่อเข้าใช้สำหรับผู้ใช้ของ Azure Active Directory (Azure AD) ที่เป็นผู้เช่าธุรกิจ-ลูกค้า (B2C)
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a55da9683c43ac75109fd256e481b02a4d565914
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970089"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>ตั้งค่าหน้าแบบกำหนดเองสำหรับการลงชื่อเข้าใช้ของผู้ใช้


[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการสร้างหน้าแบบกำหนดเองใน Microsoft Dynamics 365 Commerce ที่จัดการการลงชื่อเข้าใช้สำหรับผู้ใช้ของ Azure Active Directory (Azure AD) ที่เป็นผู้เช่าธุรกิจ-ลูกค้า (B2C)

## <a name="overview"></a>ภาพรวม

เมื่อต้องการใช้หน้าแบบกำหนดเองที่มีการสร้างใน Dynamics 365 Commerce เพื่อจัดการขั้นตอนการลงชื่อเข้า คุณต้องตั้งค่านโยบาย Azure AD ที่จะถูกอ้างอิงในสภาพแวดล้อม Commerce คุณสามารถตั้งค่าคอนฟิก "ลงทะเบียนและลงชื่อเข้าใช้" "แก้ไขโพรไฟล์" และ "รีเซ็ตรหัสผ่าน" นโยบาย B2C Azure AD โดยใช้แอพลิเคชัน B2C Azure AD ชื่อผู้เช่าและนโยบาย B2C Azure AD สามารถอ้างอิงในระหว่างกระบวนการเตรียมใช้งานที่ทำไว้สำหรับสภาพแวดล้อม Commerce โดยใช้วงจรชีวิต Microsoft Dynamics Lifecycle Services (LCS)

หน้า Commerce ที่กำหนดเองสามารถสร้างได้โดยใช้การลงชื่อเข้าใช้ ลงทะเบียน การแก้ไขโพรไฟล์บัญชี หรือโมดูลการรีเซ็ตรหัสผ่าน Url ของหน้าซึ่งเผยแพร่สำหรับหน้าแบบกำหนดเองเหล่านี้ควรจะถูกอ้างอิงในการตั้งค่าคอนฟิกนโยบาย B2C Azure AD ในพอร์ทัล Azure

## <a name="set-up-b2c-policies"></a>ตั้งค่านโยบาย B2C

หลังจากที่คุณตั้งค่าผู้เช่า B2C Azure AD ของคุณ และเชื่อมโยงกับสภาพแวดล้อม Commerce ให้ไปที่หน้า **Azure AD B2C** ในพอร์ทัล Azure จากนั้นบนเมนูภายใต้ **นโยบาย** ให้เลือก **ขั้นตอนของผู้ใช้ (นโยบาย)**

![คำสั่งขั้นตอนของผู้ใช้ (นโยบาย) บนเมนู](./media/B2C_CustomPage_PoliciesMenu.png)

ขณะนี้คุณสามารถตั้งค่าคอนฟิก "ลงทะเบียนและลงชื่อเข้าใช้" "แก้ไขโพรไฟล์" และ "รีเซ็ตรหัสผ่าน" ผู้ใช้ในขั้นตอนการลงชื่อเข้าใช้

### <a name="configure-the-sign-up-and-sign-in-policy"></a>ตั้งค่าคอนฟิกนโยบาย "การลงทะเบียนและลงชื่อเข้าใช้"

เมื่อต้องการตั้งค่าคอนฟิกนโยบาย "การลงชื่อเข้าใช้และลงทะเบียน" ให้ทำตามขั้นตอนต่อไปนี้

1. เลือก **ขั้นตอนของผู้ใช้ใหม่** จากนั้นบนแท็บ **ที่แนะนำ** เลือกนโยบาย **การลงทะเบียนและลงชื่อเข้าใช้**
1. ป้อนชื่อสำหรับนโยบาย (ตัวอย่างเช่น **B2C\_1\_SignInSignUp**)
1. ในส่วน **ตัวให้บริการข้อมูลเฉพาะตัว** เลือกผู้ให้บริการข้อมูลเฉพาะตัวที่จะใช้สำหรับนโยบาย อย่างน้อยที่สุด ต้องมีการเลือก **ลงทะเบียนอีเมล**
1. ในคอลัมน์ **รวบรวมแอททริบิวต์** เลือกกล่องกาเครื่องหมายสำหรับ **ที่อยู่อีเมล** **ชื่อที่กำหนด** และ **นามสกุล**
1. ในคอลัมน์ **การอ้างสิทธิ์การส่งคืนสินค้า** ให้เลือกกล่องกาเครื่องหมายสำหรับ **ที่อยู่อีเมล** **ชื่อที่กำหนด** **ตัวให้บริการข้อมูลเฉพาะตัว** **นามสกุล** และ **รหัสออบเจ็กต์ของผู้ใช้**

    ![แอททริบิวต์และการอ้างสิทธิ์ที่เลือก](./media/B2C_SignInSignUp_Attributes.png)

1. เลือก **ตกลง** เมื่อต้องการสร้างนโยบาย
1. ดับเบิลคลิกที่ชื่อนโยบายใหม่ จากนั้นในบานหน้าต่างนำทางให้เลือก **คุณสมบัติ**
1. ตั้งค่าตัวเลือก **เปิดใช้งานโครงร่างหน้าการบังคับใช้ JavaScript (การแสดงตัวอย่าง)** เป็น **เปิด**

    ![หน้าคุณสมบัติสำหรับนโยบายใหม่](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> ชื่อนโยบายจะถูกอ้างอิงทั้งหมดในสภาพแวดล้อม Commerce (คำนำหน้า **B2C\_1\_** จะรวมอยู่ในการอ้างอิง) ไม่สามารถเปลี่ยนชื่อนโยบายหลังจากที่สร้างขึ้นแล้ว ถ้าคุณกำลังเปลี่ยนนโยบายที่มีอยู่สำหรับสภาพแวดล้อม Commerce ของคุณ คุณสามารถลบนโยบายเดิมและสร้างนโยบายใหม่ที่มีชื่อเดียวกันได้ อีกทางหนึ่งคือถ้ามีการเตรียมใช้งานสภาพแวดล้อมแล้วคุณสามารถส่งชื่อนโยบายใหม่ผ่านการร้องขอการบริการ

คุณจะกลับไปที่นโยบายนี้เพื่อดำเนินการตั้งค่าให้เสร็จสมบูรณ์หลังจากที่คุณได้สร้างหน้าแบบกำหนดเองแล้ว เมื่อต้องการทำเช่นนี้ให้ปิดนโยบายเพื่อกลับไปที่หน้า **ขั้นตอนผู้ใช้ (นโยบาย)** ในพอร์ทัล Azure

### <a name="configure-the-profile-editing-policy"></a>ตั้งค่าคอนฟิกนโยบาย "การแก้ไขโพรไฟล์"

ในการตั้งค่าคอนฟิกนโยบาย "การแก้ไขโพรไฟล์" ให้ทำตามขั้นตอนเหล่านี้

1. เลือก **ขั้นตอนของผู้ใช้ใหม่** จากนั้นบนแท็บ **ที่แนะนำ** เลือกนโยบาย **การแก้ไขโพรไฟล์**
1. ป้อนชื่อสำหรับนโยบาย (ตัวอย่างเช่น **B2C\_1\_EditProfile**)
1. ในส่วน **ตัวให้บริการข้อมูลเฉพาะตัว** เลือกผู้ให้บริการข้อมูลเฉพาะตัวที่จะใช้สำหรับนโยบาย อย่าน้อยต้องเลือก **ลงชื่อเข้าใช้บัญชีท้องถิ่น**
1. ในคอลัมน์ **รวบรวมแอททริบิวต์** เลือกกล่องกาเครื่องหมายสำหรับ **ที่อยู่อีเมล** และ **นามสกุล**
1. ในคอลัมน์ **การอ้างสิทธิ์การส่งคืนสินค้า** ให้เลือกกล่องกาเครื่องหมายสำหรับ **ที่อยู่อีเมล** **ชื่อที่กำหนด** **ตัวให้บริการข้อมูลเฉพาะตัว** **นามสกุล** และ **รหัสออบเจ็กต์ของผู้ใช้**
1. เลือก **ตกลง** เมื่อต้องการสร้างนโยบาย
1. ดับเบิลคลิกที่ชื่อนโยบายใหม่ จากนั้นในบานหน้าต่างนำทางให้เลือก **คุณสมบัติ**
1. ตั้งค่าตัวเลือก **เปิดใช้งานโครงร่างหน้าการบังคับใช้ JavaScript (การแสดงตัวอย่าง)** เป็น **เปิด**

คุณจะกลับไปที่นโยบายนี้เพื่อดำเนินการตั้งค่าให้เสร็จสมบูรณ์หลังจากที่คุณได้สร้างหน้าแบบกำหนดเองแล้ว เมื่อต้องการทำเช่นนี้ให้ปิดนโยบายเพื่อกลับไปที่หน้า **ขั้นตอนผู้ใช้ (นโยบาย)** ในพอร์ทัล Azure

### <a name="configure-the-password-reset-policy"></a>ตั้งค่าคอนฟิกนโยบาย "รีเซ็ตรหัสผ่าน"

ในการตั้งค่าคอนฟิกนโยบาย "รีเซ็ตรหัสผ่าน" ให้ทำตามขั้นตอนเหล่านี้

1. เลือก **ขั้นตอนของผู้ใช้ใหม่** จากนั้นบนแท็บ **แสดงตัวอย่าง** เลือกนโยบาย **รีเซ็ตรหัสผ่าน v1.1**

    ![ตั้งค่านโยบายรหัสผ่าน v 1.1 ที่เลือกบนแท็บการแสดงตัวอย่าง](./media/B2C_ForgetPassword_Menu.png)

1. ป้อนชื่อสำหรับนโยบาย (ตัวอย่างเช่น **B2C\_1\_ForgetPassword**)
1. ในส่วน **ตัวให้บริการข้อมูลเฉพาะ** เลือก **รีเซ็ตรหัสผ่านโดยใช้ที่อยู่อีเมล**
1. ในคอลัมน์ **การอ้างสิทธิ์การส่งคืนสินค้า** ให้เลือกกล่องกาเครื่องหมายสำหรับ **ที่อยู่อีเมล** **ชื่อที่กำหนด** **นามสกุล** และ **รหัสออบเจ็กต์ของผู้ใช้**

    ![การเรียกร้องที่เลือก](./media/B2C_ForgetPassword_Attributes.png)

1. เลือก **ตกลง** เมื่อต้องการสร้างนโยบาย
1. ดับเบิลคลิกที่ชื่อนโยบายใหม่ จากนั้นในบานหน้าต่างนำทางให้เลือก **คุณสมบัติ**
1. ตั้งค่าตัวเลือก **เปิดใช้งานโครงร่างหน้าการบังคับใช้ JavaScript (การแสดงตัวอย่าง)** เป็น **เปิด**

คุณจะกลับไปที่นโยบายนี้เพื่อดำเนินการตั้งค่าให้เสร็จสมบูรณ์หลังจากที่คุณได้สร้างหน้าแบบกำหนดเองแล้ว เมื่อต้องการทำเช่นนี้ให้ปิดนโยบายเพื่อกลับไปที่หน้า **ขั้นตอนผู้ใช้ (นโยบาย)** ในพอร์ทัล Azure

## <a name="build-the-custom-pages"></a>สร้างหน้าแบบกำหนดเอง

เมื่อต้องการสร้างหน้าแบบกำหนดเองเพื่อจัดการการลงชื่อเข้าใช้ของผู้ใช้ให้ ให้ทำตามขั้นตอนต่อไปนี้

1. ในสภาพแวดล้อมการสร้างเครื่องมือ ให้ไปที่ไซต์ของคุณ
1. สร้างห้าเท็มเพลตและห้าหน้าต่อไปนี้:

    - เท็มเพลต **ลงชื่อเข้าใช้** และหน้าที่ใช้โมดูลลงชื่อเข้าใช้
    - เท็มเพลต **ลงทะเบียน** และหน้าที่ใช้โมดูลลงทะเบียน
    - เท็มเพลต **รีเซ็ตรหัสผ่าน** และหน้าที่ใช้โมดูลการรีเซ็ตรหัสผ่าน
    - เท็มเพลต **การตรวจสอบความถูกต้องของการรีเซ็ตรหัสผ่าน** และหน้าที่ใช้โมดูลการตรวจสอบความถูกต้องของการรีเซ็ตรหัสผ่าน
    - เท็มเพลต **การแก้ไขโพรไฟล์** และหน้าที่ใช้ในโมดูลการแก้ไขโพรไฟล์บัญชี

เมื่อคุณสร้างหน้า ให้ปฏิบัติตามคำแนะนำต่อไปนี้

- สำหรับแต่ละหน้าหรือโมดูล ให้ใช้โครงร่างและลักษณะที่ตรงกับความต้องการของธุรกิจของคุณมากที่สุด
- เผยแพร่หน้าและ Url ทั้งหมดที่ต้องใช้ในการตั้งค่า B2C Azure AD
- หลังจากเผยแพร่หน้าและ Url แล้วให้รวบรวม Url ที่ต้องใช้สำหรับการตั้งค่าคอนฟิกนโยบาย B2C Azure AD A **?preloadscripts=true** คำต่อท้ายจะถูกเพิ่มเข้าในทุก URL เมื่อมีการใช้งาน

> [!IMPORTANT]
> อย่าใช้ส่วนหัวและส่วนท้ายสากลที่มีการเชื่อมโยงที่สัมพันธ์กัน เนื่องจากหน้าเหล่านี้จะถูกโฮสต์ในโดเมน B2C Azure AD เมื่อมีการใช้งาน จะมีการใช้เฉพาะ URL สัมบูรณ์สำหรับลิงก์ทั้งหมด

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>ตั้งค่าคอนฟิกนโยบาย B2C Azure AD ด้วยข้อมูลของหน้าแบบกำหนดเอง 

ในพอร์ทัล Azure ให้กลับไปที่หน้า **B2C Azure AD** แล้วบนเมนูภายใต้ **นโยบาย** ให้เลือก **ขั้นตอนของผู้ใช้ (นโยบาย)**

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>อัพเดตราโยบาย "การลงทะเบียนและลงชื่อเข้าใช้" ด้วยข้อมูลของหน้าแบบกำหนดเอง

หากต้องการอัพเดตนโยบาย "การลงทะเบียนและลงชื่อเข้าใช้" ด้วยข้อมูลของหน้าแบบกำหนดเอง ให้ทำตามขั้นตอนต่อไปนี้

1. ในนโยบาย **ลงทะเบียนและลงชื่อเข้าใช้** ที่คุณตั้งค่าคอนฟิกก่อนหน้านี้ ในบานหน้าต่างนำทาง ให้เลือก **โครงร่างหน้า**
1. เลือกโครงร่าง **หน้าการลงทะเบียนหรือลงชื่อเข้าใช้โดยรวม**
1. ตั้งค่าตัวเลือก **ใช้เนื้อหาของหน้าแบบกำหนดเอง** เป็น **ใช่**
1. ในฟิลด์ **URI ของหน้าแบบกำหนดเอง** ให้ป้อน URL แบบเต็มในการลงชื่อเข้าใช้ รวมคำต่อท้าย **preloadscripts=true** ตัวอย่างเช่น ป้อน ``www.<my domain>.com/sign-in?preloadscripts=true``
1. ในฟิลด์ **รุ่นของโครงร่างหน้า (การแสดงตัวอย่าง)** เลือก **1.2.0**
1. เลือกโครงร่าง **หน้าการลงทะเบียนบัญชีเฉพาะที่**
1. ตั้งค่าตัวเลือก **ใช้เนื้อหาของหน้าแบบกำหนดเอง** เป็น **ใช่**
1. ในฟิลด์ **URI ของหน้าแบบกำหนดเอง** ให้ป้อน URL แบบเต็มในการลงทะเบียน รวมคำต่อท้าย **preloadscripts=true** ตัวอย่างเช่น ป้อน ``www.<my domain>.com/sign-up?preloadscripts=true``
1. ในฟิลด์ **รุ่นของโครงร่างหน้า (การแสดงตัวอย่าง)** เลือก **1.2.0**
1. ในส่วน **แอททริบิวต์ของผู้ใช้** ให้ทำตามขั้นตอนต่อไปนี้

    1. สำหรับแอททริบิวต์ **ที่อยู่อีเมล** **ชื่อที่กำหนด** และ **นามสกุล** ให้เลือก **ไม่** ในฟิลด์ **ต้องมีการตรวจสอบความถูกต้อง**
    1. สำหรับแอททริบิวต์ **ชื่อที่กำหนด** และ **นามสกุล** ให้เลือก **ไม่** ในฟิลด์ **ไม่จำเป็น**

    ![การตั้งค่าคอนฟิกของนโยบายหน้าการลงทะเบียนบัญชีภายในเครื่อง](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>อัพเดตนโยบาย "การแก้ไขโพรไฟล์" ด้วยข้อมูลของหน้าแบบกำหนดเอง

หากต้องการอัพเดตนโยบาย "การแก้ไขโพรไฟล์" ด้วยข้อมูลของหน้าแบบกำหนดเอง ให้ทำตามขั้นตอนต่อไปนี้

1. ในนโยบาย **การแก้ไขโพรไฟล์** ที่คุณตั้งค่าคอนฟิกก่อนหน้านี้ ในบานหน้าต่างนำทาง ให้เลือก **โครงร่างหน้า**
1. เลือกโครงร่าง **หน้าแก้ไขโพรไฟล์**
1. ตั้งค่าตัวเลือก **ใช้เนื้อหาของหน้าแบบกำหนดเอง** เป็น **ใช่**
1. ในฟิลด์ **URI ของหน้าแบบกำหนดเอง** ให้ป้อน URL แก้ไขโพรไฟล์แบบเต็ม รวมคำต่อท้าย **preloadscripts=true** ตัวอย่างเช่น ป้อน ``www.<my domain>.com/profile-edit?preloadscripts=true``
1. ในฟิลด์ **รุ่นของโครงร่างหน้า (การแสดงตัวอย่าง)** เลือก **1.2.0**
1. ในส่วน **แอททริบิวต์ของผู้ใช้** ให้ทำตามขั้นตอนต่อไปนี้

    1. สำหรับแอททริบิวต์ **ที่อยู่อีเมล** **ชื่อที่กำหนด** ให้เลือก **ไม่** ในฟิลด์ **ต้องมีการตรวจสอบความถูกต้อง**
    1. สำหรับแอททริบิวต์ **ชื่อที่กำหนด** และ **นามสกุล** ให้เลือก **ไม่** ในฟิลด์ **ไม่จำเป็น**

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>อัพเดตนโยบาย "การรีเซ็ตรหัสผ่าน" ด้วยข้อมูลของหน้าแบบกำหนดเอง

หากต้องการอัพเดตนโยบาย "การรีเซ็ตรหัสผ่าน" ด้วยข้อมูลของหน้าแบบกำหนดเอง ให้ทำตามขั้นตอนต่อไปนี้

1. ในนโยบาย **การรีเซ็ตรหัสผ่าน** ที่คุณตั้งค่าคอนฟิกก่อนหน้านี้ ในบานหน้าต่างนำทาง ให้เลือก **โครงร่างหน้า**
1. เลือกโครงร่าง **หน้ารหัสผ่านใหม่**
1. ตั้งค่าตัวเลือก **ใช้เนื้อหาของหน้าแบบกำหนดเอง** เป็น **ใช่**
1. ในฟิลด์ **URI ของหน้าแบบกำหนดเอง** ให้ป้อน URL รีเซ็ตพาสเวิร์ดแบบเต็ม รวมคำต่อท้าย **preloadscripts=true** ตัวอย่างเช่น ป้อน ``www.<my domain>.com/passwordreset?preloadscripts=true``
1. ในฟิลด์ **รุ่นของโครงร่างหน้า (การแสดงตัวอย่าง)** เลือก **1.2.0**
1. เลือกโครงร่าง **หน้าการตรวจสอบบัญชี**
1. ตั้งค่าตัวเลือก **ใช้เนื้อหาของหน้าแบบกำหนดเอง** เป็น **ใช่**
1. ในฟิลด์ **URI ของหน้าแบบกำหนดเอง** ให้ป้อน URL การตรวจสอบความถูกต้องของการรีเซ็ตรหัสผ่านแบบเต็ม รวมคำต่อท้าย **preloadscripts=true** ตัวอย่างเช่น ป้อน ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``
1. ในฟิลด์ **รุ่นของโครงร่างหน้า (การแสดงตัวอย่าง)** เลือก **1.2.0**



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>ปรับแต่งสตริงข้อความเริ่มต้นสำหรับป้ายชื่อและคำอธิบาย

ในไลบรารีโมดูล การลงชื่อเข้าใช้ในโมดูลจะมีการกรอกข้อมูลล่วงหน้ากับสตริงข้อความเริ่มต้นสำหรับป้ายชื่อและคำอธิบาย คุณสามารถเลือกกำหนดสตริงเหล่านี้ในชุดการพัฒนาซอฟต์แวร์ (SDK) โดยอัพเดตค่าในไฟล์ global.json สากลสำหรับลงชื่อเข้าใช้ในโมดูล

ตัวอย่างเช่นข้อความเริ่มต้นสำหรับลิงก์ลืมรหัสผ่าน คือ **ลืมรหัสผ่านใช่หรือไม่** ต่อไปนี้เป็นการแสดงข้อความเริ่มต้นนี้บนหน้าการลงชื่อเข้าใช้

![ข้อความเริ่มต้นสำหรับลิงก์รหัสผ่านที่ลืมบนหน้าลงชื่อเข้าใช้](./media/B2C_SignUp_ModuleFace.png)

อย่างไรก็ตาม ในไฟล์ global.json สำหรับโมดูลการลงชื่อเข้าใช้ในไลบรารีโมดูล คุณสามารถแก้ไขข้อความเป็น **ลืมรหัสผ่านใช่หรือไม่** ดังที่แสดงในภาพประกอบต่อไปนี้

![ข้อความลิงก์ที่อัพเดตในการลงชื่อเข้าใช้ในโมดูลไฟล์ global.json](./media/B2C_CustomizingStringsForModule.png)

หลังจากที่คุณอัปเดตไฟล์ global.json และเผยแพร่การเปลี่ยนแปลงของคุณ ข้อความลิงก์ใหม่จะปรากฏขึ้นในโมดูลการลงชื่อเข้าใช้ ทั้งใน Commerce และบนหน้าลงชื่อเข้าใช้แบบใช้งานจริง

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าคอนฟิกชื่อโดเมนของคุณ](configure-your-domain-name.md)

[ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)

[สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)

[เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์](associate-site-online-store.md)

[จัดการไฟล์ robots.txt](manage-robots-txt-files.md)

[อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก](upload-bulk-redirects.md)

[ตั้งค่าผู้เช่า B2C ใน Commerce](set-up-B2C-tenant.md)

[ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce](configure-multi-B2C-tenants.md)

[เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)](add-cdn-support.md)

[เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง](enable-store-detection.md)
