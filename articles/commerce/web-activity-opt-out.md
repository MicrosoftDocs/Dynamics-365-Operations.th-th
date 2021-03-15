---
title: การเลือกปฏิเสธการรวบรวมข้อมูลกิจกรรมบนเว็บ
description: หัวข้อนี้จะอธิบายถึงวิธีการที่คุณสามารถอนุญาตให้ผู้เยี่ยมชมเว็บไซต์ของคุณเลือกใช้งานการรวบรวมข้อมูลกิจกรรมบนเว็บใน Microsoft Dynamics 365 Commerce
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c396060017db6d7ce830b350f242d3097876e50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012324"
---
# <a name="opt-out-of-web-activity-event-collection"></a>การเลือกปฏิเสธการรวบรวมข้อมูลกิจกรรมบนเว็บ
[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีที่คุณสามารถให้ลูกค้าเลือกที่จะไม่รับการรวบรวมข้อมูลกิจกรรมบนเว็บใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

Dynamics 365 Commerce ช่วยให้ผู้ดูแลไซต์วิเคราะห์กิจกรรมบนเว็บของผู้ใช้เว็บไซต์อีคอมเมิร์ซของตน วิธีการนี้จะทำให้ผู้ใช้สามารถเข้าใจวิธีการใช้ไซต์ของตนได้ดียิ่งขึ้นและสามารถเพิ่มประสิทธิภาพให้กับไซต์เพื่อให้ประสบการณ์การใช้งานของผู้ใช้ที่ดีขึ้นและเป็นไปตามวัตถุประสงค์ทางธุรกิจ


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>วิธีที่ผู้ดูแลระบบจะใช้ประสบการณ์การปฏิเสธเข้าร่วม

ผู้ดูแลระบบมีสามวิธีที่จะใช้ประสบการณ์การปฏิเสธเข้าร่วม

### <a name="opt-out-on-behalf-of-users"></a>ปฏิเสธเข้าร่วมที่กระทำในนามของผู้ใช้อื่น

ในการจัดการลูกค้าองค์กรในศูนย์ควบคุม Commerce ผู้ดูแลระบบสามารถปฏิเสธเข้าร่วมในนามของผู้ใช้อื่น

1. ในไคลเอนต์ HQ บนหน้า **ลูกค้าทั้งหมด** ให้ค้นหาและเลือกลูกค้า
1. บนหน้ารายละเอียดลูกค้าบนแท็บด่วน **การขายปลีก** ในส่วน **ความเป็นส่วนตัว** ให้ตั้งค่าตัวเลือก **อย่าติดตามกิจกรรมของเว็บ** เป็น **ใช่**

    ![การตั้งค่าความเป็นส่วนตัว](media/Disablepersonalizationpart2.png)

1. เลือก **ตกลง** และจากนั้นปิดหน้า

### <a name="module-based-opt-out-experience"></a>ประสบการณ์การเลือกไม่ใช้การยึดตามโมดูล

ผู้ดูแลระบบสามารถอนุญาตให้ผู้ใช้ที่ได้รับการรับรองความถูกต้องเลือกที่จะไม่ใช้งานการรวบรวมข้อมูลกิจกรรมบนเว็บด้วยตัวเอง เพื่อมอบประสบการณ์การไม่เข้าร่วมนี้ ให้เพิ่มโมดูลการยกเลิกผู้ใช้ในหน้าโปรไฟล์บัญชีลูกค้า

### <a name="custom-extensions"></a>ส่วนขยายที่กำหนดเอง

ผู้ดูแลระบบสามารถสร้างส่วนขยายของตนเองเพื่อจัดการประสบการณ์การเลือกไม่ใช้สำหรับผู้ใช้ สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เรียกเซิร์ฟเวอร์การขายปลีก API](e-commerce-extensibility/call-retail-server-apis.md) และ [การเพิ่มช่องทางออนไลน์](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]