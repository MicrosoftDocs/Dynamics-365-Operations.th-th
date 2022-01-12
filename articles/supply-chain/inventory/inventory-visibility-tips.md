---
title: เคล็ดลับการแสดงผลสินค้าคงคลัง
description: หัวข้อนี้มีบางสิ่งที่คุณควรพิจารณาเมื่อคุณตั้งค่าและใช้ Add-in ของการแสดงผลสินค้าคงคลัง
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f5fb4c7cb941b352bbc6e2fcf5347244e1c8a40c
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920820"
---
# <a name="inventory-visibility-tips"></a>เคล็ดลับการแสดงผลสินค้าคงคลัง

[!include [banner](../includes/banner.md)]

นี่คือบางสิ่งที่คุณควรพิจารณาเมื่อคุณตั้งค่าและใช้ Add-in ของการแสดงผลสินค้าคงคลัง

- ปัจจุบัน Add-in การแสดงผลสินค้าคงคลังคลังสนับสนุนสภาพแวดล้อม Microsoft Dataverse เฉพาะที่สร้างโดยใช้ Microsoft Dynamics Lifecycle Services (LCS) เท่านั้น ถ้าสภาพแวดล้อม Dataverse ของคุณถูกสร้างขึ้นในวิธีอื่น (ตัวอย่างเช่น โดยใช้ศูนย์การจัดการ Power Apps) และถ้าจะเชื่อมโยงกับสภาพแวดล้อม Dynamics 365 Supply Chain Management ของคุณ คุณต้องติดต่อทีมงานผลิตภัณฑ์การแสดงผลสินค้าคงคลังเพื่อแก้ปัญหาการแม็ปก่อน คุณสามารถติดต่อทีมงานที่ [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) ทีมจะช่วยให้คุณทราบเมื่อสภาพแวดล้อมของคุณพร้อมแล้วที่จะติดตั้งการแสดงผลสินค้าคงคลัง
- ถ้าคุณมีสภาพแวดล้อม LCS มากกว่าหนึ่งสภาพแวดล้อม ให้สร้างโปรแกรมประยุกต์ Azure Active Directory (Azure AD) ที่แตกต่างกันในแต่ละสภาพแวดล้อม ถ้าคุณใช้รหัสโปรแกรมประยุกต์และรหัสผู้เช่าเดียวกันเพื่อติดตั้ง Add-in การแสดงผลสินค้าคงคลังในสภาพแวดล้อมที่แตกต่างกัน ปัญหาโทเค็นจะเกิดขึ้นกับสภาพแวดล้อมที่เก่ากว่า เฉพาะอินสแตนซ์สุดท้ายของ Add-in การแสดงผลสินค้าคงคลังที่ติดตั้งเท่านั้นที่จะถูกต้อง
- ปัจจุบันการแสดงผลสินค้าคงคลังไม่ได้รับการสนับสนุนเฉพาะในสภาพแวดล้อมที่โฮสต์ระบบคลาวน์ ระบบสนับสนุนสภาพแวดล้อม Tier-2+ เท่านั้น
- ปัจจุบัน Application Programming Interface (API) สนับสนุนการสอบถามสินค้าแต่ละรายการสูงสุด 100 รายการตามค่า `ProductID` นอกจากนี้ `SiteID` และ `LocationID` ยังสามารถระบุหลายค่าในแต่ละการสอบถามได้ ขีดจํากัดสูงสุดจะกําหนดเป็น `NumOf(SiteID) * NumOf(LocationID) <= 100`
- แหล่งข้อมูล `fno` ถูกจองสำหรับ Supply Chain Management ถ้า Add-in การแสดงผลสินค้าคงคลังของคุณรวมกับสภาพแวดล้อม Supply Chain Management เราขอแนะนำว่าคุณควรลบการตั้งค่าคอนฟิกที่เกี่ยวข้องกับ `fno` ใน [แหล่งข้อมูล](inventory-visibility-configuration.md#data-source-configuration)
- [การตั้งค่าคอนฟิกพาร์ติชัน](inventory-visibility-configuration.md#partition-configuration) ในปัจจุบันประกอบด้วยมิติพื้นฐานสองมิติ (`SiteId` และ `LocationId`) ที่บ่งชี้ว่ามีการกระจายข้อมูลอย่างไร การดําเนินงานภายใต้พาร์ติชันเดียวกันสามารถส่งประสิทธิภาพที่สูงกว่าที่ต้นทุนต่ำกว่าได้ โซลูชันมีการตั้งค่าคอนฟิกพาร์ติชันนี้ตามค่าเริ่มต้น ดังนั้น *คุณไม่ต้องกำหนดด้วยตนเอง* อย่าเลือกกําหนดการตั้งค่าคอนฟิกพาร์ติชันเริ่มต้นเอง ถ้าคุณลบหรือเปลี่ยนแปลง คุณอาจทําให้เกิดข้อผิดพลาดที่ไม่คาดคิด
- ไม่ควรกําหนดมิติพื้นฐานที่ถูกกําหนดในการตั้งค่าคอนฟิกพาร์ติชันใน [การตั้งค่าคอนฟิกลำดับชั้นของดัชนีผลิตภัณฑ์](inventory-visibility-configuration.md#index-configuration)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
