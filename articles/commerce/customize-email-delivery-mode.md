---
title: ปรับแต่งอีเมลของธุรกรรมตามวิธีการจัดส่ง
description: บทความนี้จะอธิบายวิธีการตั้งค่าเท็มเพลตอีเมลที่กำหนดเองสำหรับชนิดการแจ้งเตือนและวิธีการจัดส่งที่เฉพาะเจาะจงใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 0c0bd218c10a373d142ddcc7780c5339569f7a07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275716"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>ปรับแต่งอีเมลของธุรกรรมตามวิธีการจัดส่ง

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายวิธีการตั้งค่าเท็มเพลตอีเมลที่กำหนดเองสำหรับชนิดการแจ้งเตือนและวิธีการจัดส่งที่เฉพาะเจาะจงใน Microsoft Dynamics 365 Commerce

ตอนนี้อีเมลของธุรกรรมสามารถกำหนดเองได้สำหรับการรวมกันของชนิดการแจ้งเตือน (ตัวอย่างเช่น **ใบสั่งที่สร้าง** **ใบสั่งที่บรรจุ** หรือ  **ใบสั่งที่ออกใบแจ้งหนี้แล้ว**) และวิธีการจัดส่ง (ตัวอย่างเช่น ข้ามคืน การรับสินค้าในร้านค้า หรือการรับสินค้าหน้าร้านค้า) อีเมล์ธุรกรรมที่กำหนดเองช่วยให้ร้านค้าปลีกสามารถให้คำสั่งของลูกค้าของตนมีประสบการณ์การทำงานที่เหมาะสมกับวิธีการจัดส่งของใบสั่ง ตัวอย่างเช่น เหตุการณ์ "ใบสั่งบรรจุ" สามารถกำหนดเองเพื่อให้มีคำแนะนำในการรับสินค้าหน้าร้าน สำหรับลูกค้าที่เลือกรับสินค้าหน้าร้าน อีกทางหนึ่งคือ ผู้ขนส่งและข้อมูลการจัดส่งสำหรับลูกค้าที่เลือกว่าจะจัดส่งสินค้าตามใบสั่งซื้อไปให้หรือไม่

> [!NOTE]
> เมื่อต้องการใช้ฟังก์ชันสำหรับอีเมล์ธุรกรรมที่กำหนดเอง คุณต้องเปิดใช้งานคุณลักษณะ **การกำหนดเท็มเพลตอีเมลธุรกรรมตามโหมดการจัดส่ง** โดยไปที่ **พื้นที่ทำงาน \> การจัดการคุณลักษณะ** ใน Commerce headquarters

อีเมลอาจถูกปรับแต่งตามวิธีการจัดส่งสำหรับชนิดการแจ้งเตือนต่อไปนี้:

- **การยกเลิกใบสั่ง** – ชนิดการแจ้งเตือนทางอีเมลนี้เป็นชนิดใหม่
- **สร้างใบสั่งแล้ว**
- **ยืนยันใบสั่งแล้ว**
- **ใบแจ้งหนี้ใบสั่ง** – ชนิดการแจ้งเตือนทางอีเมลนี้เป็นชนิดใหม่ คุณสามารถใช้แทนชนิดของการแจ้งเตือน **การจัดส่งสินค้าตามใบสั่ง** ที่จะส่งการแจ้งเตือนสำหรับเหตุการณ์ใบแจ้งหนี้ที่มีวิธีการจัดส่งของการจัดส่ง (ไม่ใช่การเบิกสินค้า การดำเนินการ หรือโหมดอิเล็กทรอนิกส์ของการจัดส่ง)
- **การเบิกสินค้าตามใบสั่ง**
- **ใบสั่งที่บรรจุ**
- **ใบสั่งที่พร้อมสำหรับการเบิกสินค้า** – ชนิดการแจ้งเตือนนี้สามารถกำหนดตามวิธีการจัดส่งได้เฉพาะเมื่อคุณลักษณะ **สนับสนุนสำหรับคุณลักษณะการจัดส่งสินค้าในการจัดส่งหลายครั้ง** มีการเปิดใช้งานการเท่านั้น ในกรณีนี้ ชนิดการแจ้งเตือนนี้มีหน้าที่เทียบเท่ากับชนิดของการแจ้งเตือน **ใบสั่งที่บรรจุ**
- **การชำระเงินล้มเหลว**
- **สร้างใบสั่งเปลี่ยนสินค้าแล้ว**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>ตั้งค่าคอนฟิกเท็มเพลตอีเมลสำหรับการจัดส่งเฉพาะ

สำหรับขั้นตอนนี้ สมมติฐานคือคุณสร้างเท็มเพลตอีเมลที่กำหนดเองใหม่ของคุณใหม่ และเพิ่มเท็มเพลตในหน้า **เท็มเพลตอีเมลขององค์กรแล้ว** สำหรับข้อมูลเกี่ยวกับวิธีการสร้างและการอัปโหลดเท็มเพลตอีเมล โปรดดูที่ [การสร้างเท็มเพลตอีเมล์สำหรับเหตุการณ์ธุรกรรม](email-templates-transactions.md)

เมื่อต้องการตั้งค่าคอนฟิกเท็มเพลตอีเมลสำหรับการจัดส่งที่เฉพาะเจาะจงใน Commerce headquarters ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **โพรไฟล์การแจ้งเตือนทางอีเมลของ Commerce**
1. ภายใต้ **การตั้งค่าการแจ้งเตือนเหตุการณ์การขายปลีก** ให้เลือกชนิดของการแจ้งเตือนที่มีอยู่
1. ในขณะที่ชนิดการแจ้งเตือนยังคงถูกเลือกอยู่ ให้เลือก **ตั้งค่าคอนฟิกวิธีการจัดส่ง**
1. ในกล่องโต้ตอบ **วิธีการจัดส่ง** เลือก **ใหม่**
1. ในแถวใหม่ ในฟิลด์ **วิธีการจัดส่ง** เลือกวิธีการจัดส่ง
1. ในฟิลด์ **รหัสอีเมล์** เลือกเท็มเพลตอีเมลเพื่อแม็ปกับวิธีการจัดส่ง
1. เลือกกล่องกาเครื่องหมาย **ใช้งาน**
1. ทำซ้ำขั้นตอนที่ 4 ถึง 7 เพื่อเพิ่มวิธีการจัดส่ง
1. เมื่อคุณได้ทำเสร็จสิ้นแล้ว เลือก **ตกลง**

> [!NOTE]
> - เมื่อมีการจัดส่งสินค้ามากกว่าหนึ่งโหมดอยู่ระหว่างรายการในใบสั่งขาย จะมีการใช้เท็มเพลตเริ่มต้น เท็มเพลตเริ่มต้นคือเท็มเพลตที่แม็ปกับชนิดของการแจ้งเตือนบนหน้า **โพรไฟล์การแจ้งเตือนทางอีเมลของ Commerce**
> - ถ้าใบสั่งขายมีวิธีการจัดส่งที่ยังไม่ได้ตั้งค่าคอนฟิกสำหรับเท็มเพลตอีเมลที่กำหนดเอง จะมีการใช้เท็มเพลตอีเมล์เริ่มต้น

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[สร้างใบสั่งของศูนย์บริการ](tasks/create-call-center-orders.md)

[เปลี่ยนวิธีการจัดส่งใน POS](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
