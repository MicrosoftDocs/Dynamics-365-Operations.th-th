---
title: อีเมลต้อนรับจะไม่ถูกส่งเมื่อสร้างลูกค้าใหม่
description: บทความนี้มีแนวทางการแก้ไขปัญหาซึ่งสามารถช่วยได้ถ้าการแจ้งเตือนของอีเมลต้อนรับไม่ถูกส่งเมื่อมีการสร้างลูกค้าใหม่ใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219416"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>อีเมลต้อนรับจะไม่ถูกส่งเมื่อสร้างลูกค้าใหม่

[!include [banner](../../includes/banner.md)]

บทความนี้มีแนวทางการแก้ไขปัญหาซึ่งสามารถช่วยได้ถ้าการแจ้งเตือนของอีเมลต้อนรับไม่ถูกส่งเมื่อมีการสร้างลูกค้าใหม่ใน Microsoft Dynamics 365 Commerce

## <a name="description"></a>คำอธิบาย

เมื่อสร้างลูกค้าใหม่ใน Commerce headquarters อีเมลต้อนรับไม่ถูกส่งให้กับลูกค้า ถึงแม้ว่าการแจ้งเตือนทางอีเมลจะได้รับการตั้งค่าคอนฟิกให้กับชนิดการแจ้งเตือนทางอีเมล **สร้างลูกค้าแล้ว**

## <a name="resolution"></a>การแก้ปัญหา

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>เชื่อมโยงโปรไฟล์การแจ้งเตือนทางอีเมลภายใต้พารามิเตอร์ Commerce

1. ในศูนย์ควบคุม ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์ Commerce\> ทั่วไป**
2. ในรายการแบบหล่นลง **โปรไฟล์การแจ้งเตือนทางอีเมล** ให้เลือกโปรไฟล์การแจ้งเตือนทางอีเมลที่ประกอบด้วยการแม็ประหว่างชนิดการแจ้งเตือนของลูกค้าที่สร้างและแม่แบบอีเมลที่ลูกค้าสร้าง  

> [!NOTE] 
> เมื่อคุณเปิดใช้งานการแจ้งเตือนที่สร้างขึ้นของลูกค้า ลูกค้าที่สร้างขึ้นในช่องทางทั้งหมดภายในนิติบุคคลจะได้รับอีเมลที่สร้างขึ้นจากลูกค้า ปัจจุบัน ลูกค้าสร้างการแจ้งเตือนไม่สามารถจํากัดเพียงช่องทางเดียวได้

ดูข้อมูลเพิ่มเติมที่ [สร้างเทมเพลตอีเมลสำหรับเหตุการณ์ของธุรกรรม](../email-templates-transactions.md) 

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าโพรไฟล์การแจ้งเตือนทางอีเมล](../email-notification-profiles.md)
