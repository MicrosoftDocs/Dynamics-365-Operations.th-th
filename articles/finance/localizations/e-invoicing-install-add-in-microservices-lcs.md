---
title: ติดตั้ง add-in สำหรับไมโครเซอร์วิสใน Lifecycle Services
description: บทความนี้อธิบายถึงวิธีการติดตั้ง Add-in การออกใบแจ้งหนี้อิเล็กทรอนิกส์ใน Microsoft Dynamics Lifecycle Services (LCS)
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: a837b85d4893f2915b5fbb5ffaae8eb95f19bc0e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272286"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>ติดตั้ง add-in สำหรับไมโครเซอร์วิสใน Lifecycle Services

[!include [banner](../includes/banner.md)]

การรับรองความถูกต้องในบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์กำหนดให้คุณต้องลงทะเบียนสภาพแวดล้อม Microsoft Dynamics 365 Finance หรือ Dynamics 365 Supply Chain Management ของคุณ ในแพลตฟอร์มบริการโดยติดตั้ง Add-in สำหรับสภาพแวดล้อมของคุณใน Microsoft Dynamics Lifecycle Services (LCS)

การลงทะเบียนสภาพแวดล้อม ให้ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้บัญชี LCS ของคุณ
2. บนแดชบอร์ดโครงการ ให้เลือกโครงการ LCS
2. ในโครงการ บนแดชบอร์ด **สภาพแวดล้อม** ให้เลือกโครงการที่ปรับใช้ของคุณ สภาพแวดล้อมที่คุณเลือกต้องทำงานอยู่
3. บนแท็บ **การรวม Power Platform** ในส่วน **Add-in ของสภาพแวดล้อม** ให้เลือก **ติดตั้ง Add-in ใหม่**
4. เลือก **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**
5. ในฟิลด์ **รหัสแอปพลิเคชัน AAD** ให้ป้อน **091c98b0-a1c9-4b02-b62c-7753395ccabe** ค่านี้เป็นค่าคงที่ ตรวจสอบให้แน่ใจว่าคุณป้อนรหัสเฉพาะสากล (GUID) เท่านั้น อย่าใส่สัญลักษณ์อื่นใด เช่น ช่องว่าง เครื่องหมายจุลภาค เครื่องหมายจุด หรือเครื่องหมายอัญประกาศ
6. ในฟิลด์ **รหัสผู้เช่า AAD** ป้อนรหัสผู้เช่าของบัญชีสมัครสมาชิก Azure ของคุณ ผู้เช่า Azure Active Directory (Azure AD) ที่คุณระบุควรเป็นผู้เช่าเดียวกันกับที่ใช้กับ Regulatory Configuration Service (RCS)
7. ตรวจสอบข้อกำหนดและเงื่อนไข จากนั้นเลือกกล่องกาเครื่องหมาย
8. เลือก **ติดตั้ง** หลังจากสองสามนาที สถานะควรเปลี่ยนจาก **กำลังติดตั้ง** เป็น **ติดตั้งแล้ว** คุณอาจต้องรีเฟรชหน้าเพื่อดูการเปลี่ยนแปลงนี้

การออกใบแจ้งหนี้อิเล็กทรอนิกส์พร้อมใช้งานแล้วตอนนี้

> [!NOTE]
> โดยปกติบริษัทจะมีสภาพแวดล้อม Finance หรือ Supply Chain Management หลายรายการ สภาพแวดล้อมเหล่านี้รวมถึงสภาพแวดล้อมการทำงานจริง สภาพแวดล้อมการทดสอบการยอมรับของผู้ใช้ (UAT) และสภาพแวดล้อมการพัฒนา (sandbox) คุณต้องดำเนินขั้นตอนก่อนหน้าสำหรับสภาพแวดล้อมทั้งหมดที่คุณต้องการเชื่อมต่อกับการออกใบแจ้งหนี้อิเล็กทรอนิกส์
