---
title: กำหนดค่าจุดโฟกัสของภาพ
description: หัวข้อนี้จะอธิบายวิธีการปรับแต่งจุดโฟกัสของรูปภาพในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b20fbc20f18243c712595795a0b16ae417e755e6
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594343"
---
# <a name="customize-image-focal-points"></a>กำหนดค่าจุดโฟกัสของภาพ

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการปรับแต่งจุดโฟกัสของรูปภาพในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

เมื่อมีการอัพโหลดรูปภาพไปยังไลบรารีสื่อของโปรแกรมสร้างไซต์ Commerce ระบบจะพยายามระบุจุดโฟกัสของรูปภาพ ตัวอย่างเช่น ถ้ารูปภาพมีบุคคลอยู่บนนั้น ระบบจะตั้งค่าจุดโฟกัสเป็นหน้าของบุคคลตามค่าเริ่มต้น ในกรณีส่วนใหญ่ การตั้งค่าจุดโฟกัสโดยอัตโนมัติจะทำงานได้ดีสำหรับ viewports ทั้งหมด แต่บางครั้งคุณอาจต้องการปรับจุดโฟกัสเพื่อให้แน่ใจว่าจะมองเห็นส่วนเฉพาะของรูปภาพเสมอ

### <a name="define-a-custom-focal-point-for-an-image"></a>กำหนดจุดโฟกัสที่กำหนดเองสำหรับรูปภาพ

เมื่อต้องการกำหนดค่าจุดโฟกัสที่กำหนดเองสำหรับรูปภาพ ให้ทำตามขั้นตอนต่อไปนี้

1. ในบานหน้าต่างนำทางด้านซ้ายของโปรแกรมสร้างไซต์ Commerce ให้เลือก **ไลบรารีสื่อ**
1. ในหน้าต่างหลัก เลือกภาพที่คุณต้องการแก้ไข
1. บนแถบคำสั่ง ให้เลือก **แก้ไข**
1. เลือกรูปภาพเพื่อป้อน **โหมดแก้ไข**
1. ภายใต้ **โหมดแก้ไข** เลือก **เปลี่ยนจุดโฟกัส** ตัวควบคุมจุดโฟกัสแบบวงกลมจะปรากฏบนรูปภาพ
1. เลือกตัวควบคุมจุดโฟกัสเพื่อเลื่อนไปที่จุดโฟกัสที่ต้องการ
1. เมื่อคุณดำเนินการเสร็จสิ้นแล้ว บนแถบคำสั่ง ให้เลือก **บันทึก** และจากนั้น เลือก **เสร็จสิ้นการแก้ไข**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของการจัดการสินทรัพย์ดิจิทัล](dam-overview.md)

[อัพโหลดรูปภาพ](dam-upload-images.md)

[อัพโหลดวิดีโอ](dam-upload-video.md)

[อัพโหลดไฟล์](dam-upload-files.md)

[ครอบตัดรูปภาพ](dam-crop-images.md)

[อัปโหลดและให้บริการไฟล์แบบคงที่](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]