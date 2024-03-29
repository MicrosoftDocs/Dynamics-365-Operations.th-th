---
title: คัดลอกเนื้อหาไปยังตำแหน่งที่ตั้งอื่น
description: หัวข้อนี้จะอธิบายวิธีการคัดลอกเนื้อหาที่มีอยู่ไปยังตำแหน่งที่ตั้ง ภายในไซต์ของโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: josaw1
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6afa871048bde22133ae083b8d56b6e99e49c401
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269273"
---
# <a name="copy-content-to-another-locale"></a>คัดลอกเนื้อหาไปยังตำแหน่งที่ตั้งอื่น

[!include[banner](../includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการคัดลอกเนื้อหาที่มีอยู่ไปยังตำแหน่งที่ตั้ง ภายในไซต์ของโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce

เมื่อคุณสร้างเนื้อหาในโปรแกรมสร้างไซต์ Commerce เนื้อหาจะถูกเชื่อมโยงกับรหัสภาษาเสมอ เช่น "en-us" คุณสามารถคัดลอกหน้าและสินทรัพย์แต่ละรายการไปยังที่ตั้งอื่นภายในไซต์ e-commerce เดียวกันได้ ด้วยการสลับที่ตั้ง เมื่อคุณแก้ไขรายการเนื้อหา แล้วสร้างตัวแปรใหม่ของสินค้า ในบางกรณี เช่น เมื่อคุณเริ่มต้นการเปิดใช้ค่าตำแหน่งที่ตั้งใหม่ทั้งหมดบนหน้าร้านค้าของคุณ ควรคัดลอกรายการเนื้อหาทั้งหมดที่มีในตำแหน่งที่ตั้งนั้นไปยังที่ตั้งใหม่ หากตำแแหน่งที่ตั้งใหม่มีภาษาพื้นฐานเหมือนกับที่มีอยู่ คุณสามารถใช้ตำแหน่งที่ตั้งที่มีอยู่เป็นตำแหน่งต้นทางสําหรับการดําเนินการคัดลอกตำแหน่งที่ตั้งได้ (ตัวอย่างเช่น "en-us" และ "en-au" ทั้งสองตำแหน่งจะใช้ภาษาอังกฤษ) ด้วยวิธีนี้ คุณช่วยลดความพยายามที่ต้องใช้ในการแปลเนื้อหาเป็นภาษาท้องถิ่นใหม่

ขั้นตอนต่อไปนี้อธิบายวิธีการเพิ่มตำแหน่งที่ตั้งใหม่ลงในช่องทางที่มีอยู่ คัดลอกรายการเนื้อหาทั้งหมดจากตำแหน่งที่ตั้งที่มีอยู่ไปยังตำแหน่งที่ตั้งใหม่ และตรวจสอบสถานะของการดําเนินงานคัดลอกตำแหน่งที่ตั้ง

## <a name="add-a-new-locale"></a>เพิ่มตำแหน่งที่ตั้งใหม่

เมื่อต้องการเพิ่มตำแหน่งที่ตั้งใหม่ในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้

1. ในโปรแกรมสร้างไซต์ ให้ไปยังไซต์ของคุณ
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าไซต์** แล้วเลือก **ช่องทาง**
1. ภายใต้ **ช่องทาง** ให้เลือกช่องทางที่จะเพิ่มตำแหน่งที่ตั้งใหม่
1. ในกล่องโต้ตอบช่องทางที่ปรากฏทางด้านขวา ให้เลือก **เพิ่มตำแหน่งที่ตั้ง**
1. ในกล่องโต้ตอบ **เพิ่มตำแหน่งที่ตั้ง** ในฟิลด์ **ตำแหน่งที่ตั้งเพื่อสนับสนุน** เลือกตำแหน่งที่ตั้ง
1. ยืนยันว่าค่า **โดเมน** ถูกต้อง
1. ภายใต้ **พาธ** ให้ป้อนพาธ URL เฉพาะ (ตัวอย่างเช่น **en-us** หรือ **ภาษาอังกฤษ-us**)
1. เลือก **ตกลง**
1. ปิดกล่องโต้ตอบช่องทาง
1. ภายใต้ **ช่องทาง** ให้ยืนยันว่าตำแหน่งที่ตั้งใหม่แสดงรายการอยู่ถัดจากช่องทางที่ถูกต้อง
1. เลือก **Save and publish**

> [!NOTE]
> ก่อนที่จะสามารถตั้งค่าคอนฟิกตำแหน่งที่ตั้งใหม่ของโปรแกรมสร้างไซต์ได้ คุณต้องเพิ่มตำแหน่งที่ตั้งนั้นลงในช่องทางร้านค้าออนไลน์ที่เชื่อมโยงใน Commerce headquarters

## <a name="copy-all-content-items-to-a-new-locale"></a>คัดลอกรายการเนื้อหาทั้งหมดไปยังตำแหน่งที่ตั้งใหม่

เมื่อต้องการคัดลอกรายการเนื้อหาทั้งหมดไปยังตำแหน่งที่ตั้งใหม่ในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้

1. ในโปรแกรมสร้างไซต์ ให้ไปยังไซต์ของคุณ
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าไซต์** แล้วเลือก **ช่องทาง**
1. บนแถบการสั่ง ให้เลือก **สร้างการคัดลอกตำแหน่งที่ตั้งจาก**
1. ในกล่องโต้ตอบ **สร้างการคัดลอกตำแหน่งที่ตั้ง** ที่จะปรากฏขึ้นทางด้านขวา ภายใต้ **ไซต์ต้นทาง** ให้ยืนยันว่ามีการเลือกไซต์ที่ถูกต้อง
1. ในฟิลด์ **ช่องทางต้นทาง** ให้เลือกช่องทางต้นทาง
1. ในฟิลด์ **ช่องทางปลายทาง** ให้เลือกช่องทางต้นทางเดียวกัน
1. ในฟิลด์ **ตำแหน่งที่ตั้งต้นทาง** ให้เลือกตำแหน่งที่ตั้งต้นทาง
1. ในฟิลด์ **ตำแหน่งที่ตั้งปลายทาง** ให้เลือกตำแหน่งที่ตั้งใหม่
1. เลือก **คัดลอกตำแหน่งที่ตั้ง** การแจ้งเตือนจะยืนยันว่าการดําเนินการคัดลอกตำแหน่งที่ตั้งเริ่มต้นแล้ว

> [!NOTE]
> คุณยังสามารถคัดลอกเนื้อหาระหว่างช่องทางต่างๆ ได้

## <a name="monitor-the-status-of-the-locale-copy"></a>ตรวจสอบสถานะของการคัดลอกตำแหน่งที่ตั้ง

หากต้องการตรวจสอบสถานะของการดําเนินการคัดลอกตำแหน่งที่ตั้ง ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ในโปรแกรมสร้างไซต์ ให้ไปยังไซต์ของคุณ
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าไซต์** แล้วเลือก **งาน**
1. ภายใต้ **งานปัจจุบัน** ให้เลือกงานที่จะตรวจสอบ รายละเอียดงานจะแสดงในกล่องโต้ตอบที่ปรากฎขึ้นบนด้านขวา
