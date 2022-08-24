---
title: การเลือกปฏิเสธการรวบรวมข้อมูลกิจกรรมบนเว็บ
description: บทความนี้อธิบายถึงวิธีการที่คุณสามารถอนุญาตให้ผู้เยี่ยมชมเว็บไซต์ของคุณเลือกใช้งานการรวบรวมข้อมูลกิจกรรมบนเว็บใน Microsoft Dynamics 365 Commerce
author: bebeale
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 81343f5033366484140f73fcc313ecd9f35e7d47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286737"
---
# <a name="opt-out-of-web-activity-event-collection"></a>การเลือกปฏิเสธการรวบรวมข้อมูลกิจกรรมบนเว็บ
[!include [banner](includes/banner.md)]

บทความนี้อธิบายวิธีที่คุณสามารถให้ลูกค้าเลือกที่จะไม่รับการรวบรวมข้อมูลกิจกรรมบนเว็บใน Microsoft Dynamics 365 Commerce

Dynamics 365 Commerce ช่วยให้ผู้ดูแลไซต์วิเคราะห์กิจกรรมบนเว็บของผู้ใช้เว็บไซต์อีคอมเมิร์ซของตน วิธีการนี้จะทำให้ผู้ใช้สามารถเข้าใจวิธีการใช้ไซต์ของตนได้ดียิ่งขึ้นและสามารถเพิ่มประสิทธิภาพให้กับไซต์เพื่อให้ประสบการณ์การใช้งานของผู้ใช้ที่ดีขึ้นและเป็นไปตามวัตถุประสงค์ทางธุรกิจ


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>วิธีที่ผู้ดูแลระบบจะใช้ประสบการณ์การปฏิเสธเข้าร่วม

ผู้ดูแลระบบมีสามวิธีที่จะใช้ประสบการณ์การปฏิเสธเข้าร่วม

### <a name="opt-out-on-behalf-of-users"></a>ปฏิเสธเข้าร่วมที่กระทำในนามของผู้ใช้อื่น

ในการจัดการลูกค้าองค์กรใน Commerce headquarters ผู้ดูแลระบบสามารถปฏิเสธเข้าร่วมในนามของผู้ใช้อื่น

1. ในไคลเอ็นต์ HQ บนหน้า **ลูกค้าทั้งหมด** ให้ค้นหาและเลือกลูกค้า
1. บนหน้ารายละเอียดลูกค้าบนแท็บด่วน **การขายปลีก** ในส่วน **ความเป็นส่วนตัว** ให้ตั้งค่าตัวเลือก **อย่าติดตามกิจกรรมของเว็บ** เป็น **ใช่**

    ![การตั้งค่าความเป็นส่วนตัว](media/Disablepersonalizationpart2.png)

1. เลือก **ตกลง** และจากนั้นปิดหน้า

### <a name="module-based-opt-out-experience"></a>ประสบการณ์การเลือกไม่ใช้การยึดตามโมดูล

ผู้ดูแลระบบสามารถอนุญาตให้ผู้ใช้ที่ได้รับการรับรองความถูกต้องเลือกที่จะไม่ใช้งานการรวบรวมข้อมูลกิจกรรมบนเว็บด้วยตัวเอง เพื่อมอบประสบการณ์การไม่เข้าร่วมนี้ ให้เพิ่มโมดูลการยกเลิกผู้ใช้ในหน้าโปรไฟล์บัญชีลูกค้า

### <a name="custom-extensions"></a>ส่วนขยายที่กำหนดเอง

ผู้ดูแลระบบสามารถสร้างส่วนขยายของตนเองเพื่อจัดการประสบการณ์การเลือกไม่ใช้สำหรับผู้ใช้ สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เรียกเซิร์ฟเวอร์การขายปลีก API](e-commerce-extensibility/call-retail-server-apis.md) และ [การเพิ่มช่องทางออนไลน์](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
