---
title: FAQ เกี่ยวกับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce
description: หัวข้อนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e8a3e760353b351d42aff82c0d372d2aca350cd2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343569"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>FAQ เกี่ยวกับสภาพแวดล้อมการประเมิน Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

หัวข้อนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>เราสามารถใช้สภาพแวดล้อมการประเมินของ Commerce เป็นหน้าร้านอีคอมเมิร์ซสำหรับลูกค้าที่ใช้ Retail ในปัจจุบันได้หรือไม่

ลำดับที่ สภาพแวดล้อมการประเมินของ Commerce มีไว้สำหรับการประเมินเท่านั้น ถ้าคุณต้องการสภาพแวดล้อมสำหรับลูกค้าที่ดำเนินการขายปลีกให้ติดต่อ Microsoft

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>สามารถใช้สภาพแวดล้อมการประเมินของ Commerce เพื่อเตรียมใช้งานคุณลักษณะอีคอมเมิร์ซเพิ่มเติมจากแอปพลิเคชัน/สภาพแวดล้อมที่ใช้งาน Retail ได้หรือไม่

ไม่ (ส่วนใหญ่) ส่วนประกอบการประเมิน Commerce มีอยู่เฉพาะสำหรับสภาพแวดล้อมที่ตรงกับการตั้งค่าคอนฟิกที่ระบุไว้ในคำแนะนำเกี่ยวกับข้อกำหนดเบื้องต้นและการเตรียมใช้งานเท่านั้น นอกจากนี้ ข้อมูลการสาธิตพื้นฐานที่จำเป็นจะไม่พร้อมใช้งานในสภาพแวดล้อมที่มีการปรับใช้โดยมีการนำออกใช้เริ่มต้นก่อนหน้า 10.0.8 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>ค่าใช้จ่ายอะไรบ้างที่เกี่ยวข้องในการปรับใช้สภาพแวดล้อมการประเมินของ Commerce บน Microsoft Azure ผ่าน Microsoft Dynamics Lifecycle Services (LCS)

สภาพแวดล้อมการสาธิตของศูนย์ควบคุม Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce แบบดั้งเดิม (เครื่องเสมือน \[VM\]) จะถูกโฮสต์ในการบอกรับเป็นสมาชิก Azure ของคุณ คุณสามารถใช้เครื่องคิดเลข [Azure](https://azure.microsoft.com/pricing/calculator/) เพื่อกำหนดราคา

ส่วนประกอบอื่นๆ เช่น Commerce Scale Unit, Commerce site builder และไซต์อีคอมเมิร์ซของคุณ จะพร้อมใช้งานในฐานะการให้บริการซอฟต์แวร์ (SaaS) และโฮสต์โดย Microsoft

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>ภูมิศาสตร์ Azure ใดที่ได้รับการสนับสนุนสำหรับสภาพแวดล้อมการประเมินของ Commerce ในขณะนี้

สภาพแวดล้อมการประเมินของ Commerce สามารถปรับใช้ได้เฉพาะในภูมิศาสตร์อเมริกาเหนือเท่านั้น

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>มีการดาวน์โหลดบนฮาร์ดดิสก์เสมือน (VHD) ที่มีตัวเลือกเครื่องเสมือนที่สมบูรณ์ OneBox (VM) หรือไม่?

Dynamics 365 Commerce และ Commerce Scale Unit เป็นการให้บริการซอฟต์แวร์ (SaaS) ที่สมบูรณ์ และต้องเป็นโฮสต์แบบคลาวด์

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>สามารถใช้สภาพแวดล้อมการประเมินของ Commerce ได้นานเท่าใด

สภาพแวดล้อมการประเมินของ Commerce มีการจำกัดเวลา 30 วัน นับจากวันที่ซึ่งส่วนประกอบของ SaaS เช่น Commerce Scale Unit, Commerce site builder และไซต์อีคอมเมิร์ซของคุณ จะได้รับการเตรียมใช้งาน

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>ฉันสามารถขยายขีดจำกัดเวลาสำหรับสภาพแวดล้อมการประเมินของ Commerce ได้หรือไม่

ส่วนขยายของขีดจำกัดเวลาเป็นข้อยกเว้นของบรรทัดฐาน และจะถือว่าเป็นตามแต่ละกรณี คุณควรติดต่อคู่ค้า Microsoft ของคุณสำหรับความช่วยเหลือ

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-overview.md)

[เตรียมใช้งานสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](provisioning-guide.md)

[ตั้งค่าคอนฟิกภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-post-provisioning.md)

[ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-bopis.md)

[ตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
