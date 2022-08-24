---
title: เรกคอร์ดลูกค้าไม่ปรากฏใน Commerce headquarters
description: บทความนี้มีคำแนะนำการแก้ไขปัญหาซึ่งสามารถช่วยได้เมื่อเรกคอร์ดลูกค้าไม่ปรากฏใน Commerce headquarters ในทันที
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: f1ad1f45abbc95cbf6d41b3c8681db781c6c9d23
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268850"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>เรกคอร์ดลูกค้าไม่ปรากฏใน Commerce headquarters

[!include [banner](../../includes/banner.md)]

บทความนี้มีคำแนะนำการแก้ไขปัญหาซึ่งสามารถช่วยได้เมื่อเรกคอร์ดลูกค้าไม่ปรากฏใน Commerce headquarters ในทันที

## <a name="description"></a>คำอธิบาย

เมื่อคุณสร้างเรกคอร์ดลูกค้าใหม่โดยใช้ขั้นตอนการลงทะเบียนในหน้าร้าน e-commerce เรกคอร์ดลูกค้าที่เกี่ยวข้องจะไม่ปรากฏขึ้นทันทีใน Commerce headquarters

## <a name="resolution"></a>ความละเอียด

### <a name="disable-customer-creation-in-async-mode"></a>ปิดใช้งานการสร้างลูกค้าในโหมด async

> [!IMPORTANT]
> หากคุณปิดใช้งานการสร้างลูกค้าแบบอะซิงโครนัส ประสิทธิภาพของระบบอาจได้รับผลกระทบ เนื่องจากการสร้างแต่ละเรกคอร์ดจะก่อให้เกิดการร้องขอแบบเรียลไทม์ไปยัง Commerce headquarters นอกจากนี้ ถ้า Commerce headquarters ไม่ทำงาน (ตัวอย่างเช่น ระหว่างขั้นตอนการให้บริการ) ขั้นตอนการสร้างลูกค้าใหม่จะก่อให้เกิดข้อผิดพลาด

เพื่อปิดใช้งานการสร้างลูกค้าในโหมด async ใน Commerce headquarters ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การขายปลีกและการพาณิชย์ \> การตั้งค่าช่องทางการขาย \> การตั้งค่าร้านค้าออนไลน์ \> โพรไฟล์ฟังก์ชัน** 
1. หากคุณยังไม่ได้ใช้โพรไฟล์ฟังก์ชันของช่องทางการขายออนไลน์ของคุณ ให้สร้างโพรไฟล์ขึ้นมา
1. ตรวจสอบให้แน่ใจว่าทางเลือก **สร้างลูกค้าในโหมด async** ถูกกำหนดเป็น **ไม่**
1. ไปที่ **การค้าปลึกและการพาณิชย์ \> ช่องทางการขาย \> ร้านค้าออนไลน์**
1. เลือกร้านค้าออนไลน์เพื่อปิดใช้งานการสร้างลูกค้าแบบอะซิงโครนัส
1. บนแท็บ **ทั่วไป** ตรวจสอบให้แน่ใจว่าได้ตั้งค่าเขตข้อมูล **โพรไฟล์ฟังก์ชัน** เป็นโพรไฟล์ฟังก์ชันที่คุณใช้กับช่องทางการขายออนไลน์ของคุณ

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าผู้เช่า B2C ใน Commerce](../set-up-b2c-tenant.md)
