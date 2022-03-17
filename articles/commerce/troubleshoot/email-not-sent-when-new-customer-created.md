---
title: อีเมลต้อนรับจะไม่ถูกส่งเมื่อสร้างลูกค้าใหม่
description: หัวข้อนี้มีแนวทางการแก้ไขปัญหาซึ่งสามารถช่วยได้ถ้าการแจ้งเตือนของอีเมลต้อนรับไม่ถูกส่งเมื่อมีการสร้างลูกค้าใหม่ใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349969"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>อีเมลต้อนรับจะไม่ถูกส่งเมื่อสร้างลูกค้าใหม่

[!include [banner](../../includes/banner.md)]

หัวข้อนี้มีแนวทางการแก้ไขปัญหาซึ่งสามารถช่วยได้ถ้าการแจ้งเตือนของอีเมลต้อนรับไม่ถูกส่งเมื่อมีการสร้างลูกค้าใหม่ใน Microsoft Dynamics 365 Commerce

## <a name="description"></a>คำอธิบาย

เมื่อสร้างลูกค้าใหม่ในศูนย์ควบคุม Commerce อีเมลต้อนรับไม่ถูกส่งให้กับลูกค้า ถึงแม้ว่าการแจ้งเตือนทางอีเมลจะได้รับการตั้งค่าคอนฟิกให้กับชนิดการแจ้งเตือนทางอีเมล **สร้างลูกค้าแล้ว**

## <a name="resolution"></a>การแก้ปัญหา

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>ตั้งค่ารหัสอีเมลที่ถูกต้องในชนิดการแจ้งเตือนทางอีเมลของลูกค้าที่สร้างขึ้น

หากต้องการตั้งค่า **รหัสอีเมล** ที่ถูกต้องให้กับชนิดการแจ้งเตือนทางอีเมล **สร้างลูกค้าแล้ว** ในศูนย์ควบคุม ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> โพรไฟล์การแจ้งเตือนทางอีเมลของ Commerce**
1. ในหน้าต่างการนำทางทางด้านซ้าย เลือกโพรไฟล์การแจ้งเตือนทางอีเมล
1. ภายใต้ **การตั้งค่าการแจ้งเตือนเหตุการณ์การขายปลีก** สำหรับชนิดการแจ้งเตือนทางอีเมล **สร้างลูกค้าแล้ว** ให้ตั้งค่าฟิลด์ **รหัสอีเมล** เป็น **NewCust**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าโพรไฟล์การแจ้งเตือนทางอีเมล](../email-notification-profiles.md)
