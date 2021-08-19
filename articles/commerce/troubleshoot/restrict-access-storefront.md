---
title: จํากัดการเข้าถึงหน้าร้านในระหว่างการทดสอบหรือการพัฒนา
description: หัวข้อนี้อธิบายวิธีการจํากัดการเข้าถึงหน้าร้าน Microsoft Dynamics 365 Commerce ในขณะที่ทำการทดสอบภายในหรือการพัฒนา
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
ms.openlocfilehash: db3317c01cab2e123f3c2927c359f9e00b98bd8a2d5e851c2c20cb4763db1c49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716794"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>จํากัดการเข้าถึงหน้าร้านในระหว่างการทดสอบหรือการพัฒนา

[!include [banner](../../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการจํากัดการเข้าถึงหน้าร้าน Microsoft Dynamics 365 Commerce ในขณะที่ทำการทดสอบภายในหรือการพัฒนา

## <a name="description"></a>คำอธิบาย

ในระหว่างทำการทดสอบภายในหรือการพัฒนา คุณอาจต้องการจํากัดการเข้าถึงไซต์ของคุณ เพื่อป้องกันไม่ให้ผู้ใช้ภายนอกเข้าถึงหน้าของหน้าร้านที่เผยแพร่อยู่ได้

## <a name="resolution"></a>ความละเอียด

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>ตั้งค่า Azure AD B2C โดยใช้โฟลว์ผู้ใช้มาตรฐาน

หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีตั้งค่าคอนฟิก Azure Active Directory B2C (Azure AD B2C) ให้กับไซต์ e-commerce ของคุณ โปรดดูที่ [ตั้งค่าผู้เช่า B2C ใน Commerce](../set-up-b2c-tenant.md)

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>จํากัดการเข้าถึงหน้าของหน้าร้านของผู้ใช้และบล็อคการสร้างผู้ใช้ใหม่

หากต้องการจํากัดการเข้าถึงหน้าของหน้าร้านของผู้ใช้โปรแกรมสร้างไซต์ Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ไซต์ของคุณ
1. เลือก **หน้า** แล้วเลือกหน้าที่จะจํากัดการเข้าถึงของผู้ใช้
1. เลือกโมดูลหรือช่องส่วนย่อย แล้วเลือก **แก้ไข**
1. ในบานหน้าต่างคุณสมบัติ ให้เลือก **ต้องลงชื่อเข้าใช้หรือไม่** แล้วเลือก **เสร็จสิ้นการแก้ไข**
1. เลือก **เผยแพร่**

เมื่อต้องการบล็อคการสร้างผู้ใช้ใหม่ใน Azure AD ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ไปที่ [พอร์ทัล Azure](https://portal.azure.com/)
1. เลือกแอปพลิเคชัน Azure AD B2C ที่คุณสร้างขึ้นเพื่อการเข้าถึงไซต์ของคุณ
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **โฟลว์ผู้ใช้**
1. ที่ด้านบนของหน้า **โฟลว์ผู้ใช้** เลือก **โฟลว์ผู้ใช้ใหม่**
1. บนหน้า **เลือกชนิดโฟลว์ผู้ใช้** ให้เลือก **แสดงตัวอย่าง**
1. ตรงกลางของหน้า ให้เลือก **ลงชื่อเข้าใช้ v2** จากนั้นให้ปฏิบัติตามขั้นตอนใน [การตั้งค่าผู้เช่า B2C ใน Commerce](../set-up-b2c-tenant.md) เพื่อตั้งค่าคอนฟิกโฟลว์ตามโฟลว์มาตรฐานของผู้ใช้ Azure AD  B2C ของไซต์ของคุณในระหว่างการทดสอบหรือการพัฒนา

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าผู้เช่า B2C ใน Commerce](../set-up-b2c-tenant.md)

[ตั้งค่าหน้าแบบกำหนดเองสำหรับการลงชื่อเข้าใช้ของผู้ใช้](../custom-pages-user-logins.md)
