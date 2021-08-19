---
title: กำหนดค่าจุดโฟกัสของภาพ
description: หัวข้อนี้จะอธิบายวิธีการปรับแต่งจุดโฟกัสของภาพในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9c8a1b6de774a4d89c0ebcf46847c1b2c5b62374b3e5ac25a0bea2ff30b47510
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727617"
---
# <a name="customize-image-focal-points"></a>ปรับแต่งจุดโฟกัสของรูปภาพ

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการปรับแต่งจุดโฟกัสของภาพในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce

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
