---
title: โมดูลตัวเลือกแค็ตตาล็อก
description: บทความนี้ครอบคลุมโมดูลตัวเลือกแค็ตตาล็อกและอธิบายวิธีการเพิ่มไปยังไซต์ระหว่างธุรกิจ Microsoft Dynamics 365 Commerce (B2B)
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136952"
---
# <a name="catalog-picker-module"></a>โมดูลตัวเลือกแค็ตตาล็อก

[!include [banner](includes/banner.md)]

บทความนี้ครอบคลุมโมดูลตัวเลือกแค็ตตาล็อกและอธิบายวิธีการเพิ่มไปยังไซต์ระหว่างธุรกิจ Microsoft Dynamics 365 Commerce (B2B)

โมดูลตัวเลือกแค็ตตาล็อกเป็นคอนเทนเนอร์พิเศษที่ใช้เพื่อแสดงรายการแค็ตตาล็อกผลิตภัณฑ์ทั้งหมดที่พร้อมใช้งานโดยผู้ใช้ไซต์ B2B เพื่อซื้อสินค้า ปัจจุบันแค็ตตาล็อกหลายแค็ตตาล็อกได้รับการสนับสนุนเฉพาะกับไซต์ B2B เท่านั้น

ในแผนภาพต่อไปนี้แสดงตัวอย่างของโมดูลตัวเลือกแค็ตตาล็อก

![ตัวอย่างของโมดูลตัวเลือกแค็ตตาล็อกที่แสดงรายการแค็ตตาล็อกผลิตภัณฑ์สามประเภท](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>เพิ่มโมดูลตัวเลือกแค็ตตาล็อกไปที่ไซต์ของคุณ

เมื่อต้องการเพิ่มโมดูลตัวเลือกแค็ตตาล็อกไปที่ไซต์ของคุณในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้

### <a name="create-a-catalog-picker-page"></a>สร้างหน้าตัวเลือกแค็ตตาล็อก

อย่างแรก สร้างหน้าตัวเลือกแค็ตตาล็อก

1. ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่
1. ในกล่องโต้ตอบ **สร้างหน้าใหม่** ภายใต้ **ชื่อหน้า** ให้ป้อน **ตัวเลือกแค็ตตาล็อก**
1. ภายใต้ **URL ของหน้า** ให้ป้อน URL สำหรับหน้า และจากนั้น เลือก **ตกลง**

    ![สร้างกล่องโต้ตอบหน้าใหม่](./media/Create-catalog-picker-page.png)

1. ภายใต้ **เลือกแม่แบบ** ให้เลือก **เนื้อหาทั่วไป** แล้วเลือก **ถัดไป**
1. ภายใต้ **เลือกเค้าโครง** ให้เลือก **เค้าโครงแบบยืดหยุ่น** แล้วเลือก **ถัดไป**
1. ภายใต้ **ตรวจทานและเสร็จสิ้น** ให้ตรวจทานการตั้งค่าคอนฟิกหน้า ถ้าคุณต้องการแก้ไขข้อมูลหน้า ให้เลือก **ย้อนกลับ** ถ้าข้อมูลหน้าถูกต้อง ให้เลือก **สร้างหน้า**
1. ภายใต้ **ตัวเลือกแค็ตตาล็อก** เลือก **ช่องหลัก** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**

    ![การเพิ่มโมดูลลงในช่องหลักภายใต้ตัวเลือกแค็ตตาล็อก](./media/Author-web-page-catalog-picker-1.png)

1. ในกล่องโต้ตอบ **เลือกโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**
1. เลือกช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**
1. ในกล่องโต้ตอบ **เลือกโมดูล** ให้เลือกโมดูล **ตัวเลือกแค็ตตาล็อก** แล้วเลือก **ตกลง**
1. ในบานหน้าต่างคุณสมบัติ **ตัวเลือกแค็ตตาล็อก** ภายใต้ **หัวข้อ** เลือก **แค็ตตาล็อก** แล้วป้อนหัวข้อของหน้าตัวเลือกแค็ตตาล็อก
1. ภายใต้ **ระดับหัวเรื่อง** ให้เลือกระดับหัวเรื่อง และจากนั้นเลือก **ตกลง**
1. ภายใต้ **ข้อความตกแต่ง** ให้ป้อนข้อความที่จะปรากฏขึ้นที่ด้านบนของหน้าตัวเลือกแค็ตตาล็อก
1. เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่

### <a name="add-a-link-on-your-account-page"></a>เพิ่มลิงค์ในหน้าบัญชีของคุณ

ถัดไป ให้เพิ่มการอ้างอิงไปที่หน้าตัวเลือกแค็ตตาล็อกของคุณในหน้า **บัญชีของฉัน**

1. ไปที่ **หน้า** ค้นหาและเลือกหน้า **บัญชีของฉัน** ของไซต์ของคุณ แล้วเลือก **แก้ไข**
1. ภายใต้ช่อง **หลัก** ของหน้า ให้เลือกช่อง **ไทล์ทั่วไปเกี่ยวกับบัญชี** 
1. ในบานหน้าต่างคุณสมบัติ **ไทล์ทั่วไปเกี่ยวกับบัญชี** ภายใต้ **ลิงค์** ให้เลือก **เพิ่มลิงค์การดำเนินการ** แล้วเลือก **ลิงค์การดำเนินการ**
1. ในกล่องโต้ตอบ **ลิงค์การดำเนินการ** ภายใต้ **ข้อความลิงค์** ให้ป้อนข้อความลิงค์ของลิงค์ไปที่หน้าตัวเลือกแค็ตตาล็อกของคุณ
1. ภายใต้ **เป้าหมายลิงค์** ให้เลือก **เพิ่มลิงค์**
1. ในกล่องโต้ตอบ **เพิ่มลิงก์** ให้เลือก **หน้าที่กำหนดเอง** แล้วเลือก **ถัดไป**
1. ภายใต้ **ชื่อ** ให้เลือกหน้าตัวเลือกแค็ตตาล็อกของคุณ เลือก **นำไปใช้** แล้วเลือก **ตกลง**
1. เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่

รูปภาพประกอบต่อไปนี้จะแสดงตัวอย่างของหน้าบัญชีที่มีการอ้างอิงถึงหน้าแค็ตตาล็อก

![หน้าบัญชีของฉันที่มีลิงค์ไปยังแค็ตตาล็อก](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>เพิ่มลิงค์จากส่วนหัว

สุดท้าย ให้เพิ่มลิงค์จากส่วนหัวของไซต์ของคุณลงในแค็ตตาล็อกของคุณ

1. ไปที่ **ส่วนย่อย** ค้นหาและเลือกส่วนหัวข้อของไซต์ของคุณ แล้วเลือก **แก้ไข**
1. เลือกช่อง **ส่วนหัว** 
1. ในบานหน้าต่างคุณสมบัติ **ส่วนหัว** ภายใต้ **ลิงก์บัญชีของฉัน** ให้เลือก **เพิ่มลิงค์การดำเนินการ** แล้วเลือก **ลิงค์การดำเนินการ**
1. ในกล่องโต้ตอบ **ลิงค์การดำเนินการ** ภายใต้ **ข้อความลิงค์** ให้ป้อนข้อความลิงค์ของลิงค์ไปที่หน้าตัวเลือกแค็ตตาล็อกของคุณ
1. ภายใต้ **เป้าหมายลิงค์** ให้เลือก **เพิ่มลิงค์**
1. ในกล่องโต้ตอบ **เพิ่มลิงก์** ให้เลือก **หน้าที่กำหนดเอง** แล้วเลือก **ถัดไป**
1. ภายใต้ **ชื่อ** ให้เลือกหน้าตัวเลือกแค็ตตาล็อกของคุณ เลือก **นำไปใช้** แล้วเลือก **ตกลง**
1. เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วนของส่วนหัว และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่

รูปภาพประกอบต่อไปนี้จะแสดงตัวอย่างของส่วนหัวเว็บไซต์อีคอมเมิร์ซที่มีลิงค์ถึงแค็ตตาล็อก B2B

![ส่วนหัวของเว็บไซต์อีคอมเมิร์ซที่มีลิงค์แบบหล่นลงไปยังแค็ตตาล็อก](./media/catalog-in-header.png)


## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม 

[สร้างแค็ตตาล็อก Commerce สำหรับไซต์ B2B](catalogs-b2b-sites.md)

[ผลกระทบของความสามารถในการเพิ่มฟังก์ชันของแค็ตตาล็อก Commerce สำหรับการปรับแต่ง B2B](catalogs-b2b-sites-dev.md)

[คำถามที่ถามบ่อยเกี่ยวกับแค็ตตาล็อก Commerce สำหรับ B2B](catalogs-b2b-sites-FAQ.md)

[หน้าและโมดูลการจัดการบัญชี](account-management.md)

[โมดูลส่วนหัว](author-header-module.md)
