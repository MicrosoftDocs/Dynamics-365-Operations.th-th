---
title: ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen
description: หัวข้อนี้มีคำแนะนำในการแก้ไขปัญหาซึ่งสามารถให้ความช่วยเหลือคุณเมื่อคุณมีปัญหาเกี่ยวกับ Microsoft Dynamics 365 Payment Connector สําหรับ Adyen
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: f01db3fa670355696c094be544775a3abc557a70
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585548"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a>ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen

[!include [banner](../../includes/banner.md)]

หัวข้อนี้มีคำแนะนำในการแก้ไขปัญหาซึ่งสามารถให้ความช่วยเหลือคุณเมื่อคุณมีปัญหาเกี่ยวกับ Microsoft Dynamics 365 Payment Connector สําหรับ Adyen

## <a name="description"></a>คำอธิบาย

คุณมีปัญหาเกี่ยวกับ Dynamics 365 Payment Connector สำหรับ Adyen ในพื้นที่ต่อไปนี้และคุณต้องการความช่วยเหลือจากทีมงาน Adyen

- การตั้งค่าคอนฟิกของการขายหน้าร้าน (POS) การขายหน้าร้านแบบสมัยใหม่ (MPOS) ศูนย์บริการ หรือ Dynamics 365 Commerce
- หมายเลขอ้างอิงของ Adyen Payment Service (PSP) (ตัวอย่างเช่น ถ้าคุณมีคำถามเกี่ยวกับการปฏิเสธ รวมถึงการปฏิเสธการคีย์ด้วยตนเอง \[MKE\])
- สิ่งที่ไม่ได้อยู่ในสภาพแวดล้อมการทดสอบหรือสภาพแวดล้อมของผู้ขายที่ใช้งานจริง

## <a name="resolution"></a>ความละเอียด

ใช้เท็มเพลตอีเมลต่อไปนี้เพื่อเริ่มกระบวนการให้ความช่วยเหลือกับทีม Adyen เพื่อเร่งการแก้ไขปัญหาเบื้องต้น ให้ตรวจสอบให้แน่ใจว่าอีเมลมีรายละเอียดที่ต้องใช้ทั้งหมด

| ฟิลด์        | มูลค่า |
|--------------|-------|
| ไปยัง           | `support@adyen.com` |
| Cc           | |
| บรรทัดหัวเรื่อง | คำขอการสนับสนุน Microsoft Dynamics |
| เนื้อหา         | <p>สวัสดี ฝ่ายสนับสนุน</p><p>กรุณาให้ความช่วยเหลือเกี่ยวกับปัญหาต่อไปนี้</p><ul><li>บัญชีผู้ขาย</li><li>สภาพแวดล้อม (การทดสอบ/การผลิต)</li><li>ช่องทาง (POS/ศูนย์บริการ/Commerce e-commerce)</li><li>หมายเลขอ้างอิง PSP ถ้าปัญหามีความเกี่ยวข้องกับธุรกรรมหนึ่งๆ (คุณสามารถค้นหาหมายเลขอ้างอิง PSP บนใบเสร็จ ใน Adyen Customer Area หรือในเมนูธุรกรรมบนเทอร์มินัล POS)</li><li>ภาพหน้าจอหรือรูปภาพของข้อความแสดงข้อผิดพลาด ถ้ามี</li><li>บันทึกตัวแสดงเหตุการณ์ (ในรูปแบบ .txt)</li><li>อธิบายปัญหาและขั้นตอนการแก้ไขปัญหาที่คุณพยายามแล้ว</li></ul> |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ยอมรับการชำระเงินโดยตัวเชื่อมต่อ Adyen สำหรับ Dynamics 365 Commerce](https://www.adyen.com/partners/dynamics-365-commerce)

[ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen](../dev-itpro/adyen-connector.md)

[ตั้งค่าตัวเชื่อมต่อการชำระเงิน Adyen สำหรับ Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
