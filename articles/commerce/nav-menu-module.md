---
title: โมดูลเมนูนำทาง
description: บทความนี้ครอบคลุมถึงโมดูลเมนูนำทางและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d58d3957749fa961b7be164a0a474ac90a23321f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281520"
---
# <a name="navigation-menu-module"></a>โมดูลเมนูนำทาง

[!include [banner](includes/banner.md)]

บทความนี้ครอบคลุมถึงโมดูลเมนูนำทางและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce

วัตถุประสงค์หลักของโมดูลนำทางเมนูคือเพื่ออนุญาตให้ผู้ใช้ไซต์สามารถเรียกดูผลิตภัณฑ์และหน้าของไซต์ตามลำดับชั้นการนำทางของช่องทางที่กำหนดไว้ในศูนย์ควบคุม Dynamics 365 Commerce สินค้าที่ได้รับการตั้งค่าคอนฟิกไว้ในโมดูลตัวเลือกเมนูนำทางจะปรากฏเป็นการนำทางในส่วนหัวของไซต์ โมดูลเมนูนำทางยังสนับสนุนรายการเมนูแบบคงที่ที่เชื่อมโยงไปยังหน้าอื่นๆ บนไซต์อีคอมเมิร์ซด้วย

คุณสามารถเพิ่มโมดูลเมนูนำทางในโมดูลส่วนหัวของหน้าได้ด้วย ในชุดรูปแบบ Fabrikam เมนูนำทางจะแสดงสองระดับตามค่าเริ่มต้น ในชุดรูปแบบชุดเริ่มต้น เมนูนำทางจะแสดงสามระดับตามค่าเริ่มต้น เมื่อต้องการเปลี่ยนแปลงจำนวนระดับ จะต้องใช้ส่วนขยายสำหรับมุมมองในชุดรูปแบบ

ภาพประกอบต่อไปนี้แสดงตัวอย่างของเมนูนำทางสำหรับไซต์ Fabrikam ที่มีการจัดประเภทตามลำดับชั้นสองระดับและรายการเมนูแบบคงที่บางส่วน
![ตัวอย่างของโมดูลเมนูการนำทาง](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>คุณสมบัติของโมดูลเมนูนำทาง

| ชื่อคุณสมบัติ             | มูลค่า                 | คำอธิบาย |
|---------------------------|-----------------------|-------------|
| ต้นทาง                  | **การขายปลีก**, **การสร้างด้วยตนเอง**, **การขายปลีกและการสร้างด้วยตนเอง** | ค่าของ **การขายปลีก** จะช่วยให้สามารถแสดงลำดับชั้นการนำทางของช่องทางจาก Commerce headquarters เพื่อแสดงบนเมนูนำทาง ค่า **การสร้างด้วยตนเอง** จะช่วยให้สามารถระบุรายการเมนูแบบคงที่ ค่าของ **การขายปลีกและการสร้างด้วยตนเอง** จะช่วยให้สามารถผสมผสานกันได้ทั้งสองอย่าง |
| แสดงรูปภาพประเภท | **จริง** หรือ **เท็จ**    | เมื่อเปิดใช้งาน คุณสมบัตินี้จะแสดงรูปภาพประเภทบนเมนูนำทางตามที่กำหนดไว้ใน Commerce headquarters สำหรับแต่ละประเภท มีการเพิ่มใน Commerce รีลีส 10.0.14 |
| แสดงรูปภาพโปรโมชั่น | **จริง** หรือ **เท็จ** | เมื่อเปิดใช้งานคุณสมบัตินี้ คุณสามารถตั้งค่าคอนฟิกโปรโมชันได้โดยใช้รูปภาพ ลิงค์ และข้อความ คุณสมบัตินี้ถูกเพิ่มลงใน Commerce รุ่น 10.0.17 แล้ว |
|เพิ่มเนื้อหาโปรโมชั่นของประเภท | ข้อความ รูปภาพ หรือลิงก์ | เมื่อเปิดใช้งานคุณสมบัติ **แสดงรูปภาพโปรโมชั่น** คุณสามารถเพิ่มข้อความ รูปภาพ หรือลิงค์เป็นเนื้อหาโปรโมชันในเมนูนําทางได้ |
| เปิดใช้งานเมนูนำทางแบบหลายระดับ | **จริง** หรือ **เท็จ** | เมื่อเปิดใช้คุณสมบัตินี้ เมนูนำทางสามารถแสดงลำดับชั้นการนำทางหลายระดับ คุณลักษณะนี้พร้อมใช้งานใน Commerce รุ่น 10.0.15 |
| จำนวนของระดับ | เลขจำนวนเต็ม | คุณสมบัตินี้กำหนดจำนวนของระดับที่ควรแสดงถ้าคุณสมบัติ **เมนูการนำทางหลายระดับ** ตั้งค่าเป็น **จริง** |
| รายการเมนูแบบคงที่| อาร์เรย์ของค่า| รายการเมนูแบบคงที่เชื่อมโยงชื่อรายการเมนูกับลิงก์ไปยังหน้าของไซต์แบบคงที่ คุณสามารถสร้างรายการเมนูด้านล่างรายการเมนูอื่นๆ ตามค่าเริ่มต้น เมนูแบบคงที่จะปรากฏที่ระดับรากและจะถูกผนวกเข้ากับลำดับชั้นการนำทางของช่องทาง ถ้ามีอยู่ |
| แสดงเมนูราก | **จริง** หรือ **เท็จ** | เมื่อเปิดใช้คุณสมบัตินี้ เมนูนำทางสามารถกำหนดได้ภายใต้รากที่กำหนดเอง (ตัวอย่างเช่น **ซื้อตอนนี้**) คุณลักษณะนี้พร้อมใช้งานใน Dynamics 365 Commerce การเผยแพร่ 10.0.15 |
| เมนูราก | สตริง | คุณสมบัตินี้สามารถใช้ในการกำหนดข้อความสำหรับรากแบบกำหนดเองถ้าคุณสมบัติ **แสดงเมนูราก** ถูกตั้งค่าเป็น **จริง** |

ภาพประกอบต่อไปนี้แสดงตัวอย่างของรูปภาพประเภทที่แสดงอยู่บนเมนูนำทางสำหรับไซต์ Fabrikam
![ตัวอย่างของโมดูลเมนูการนำทางที่มีรูปภาพประเภท](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>เพิ่มโมดูลเมนูนำทางให้กับโมดูลส่วนหัว

สำหรับรายละเอียดเกี่ยวกับวิธีการเพิ่มโมดูลเมนูนำทางให้กับโมดูลส่วนหัว ให้ดูที่ [โมดูลส่วนหัว](author-header-module.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของไลบรารีโมดูล](starter-kit-overview.md)

[โมดูลการแสดงเส้นทาง](add-breadcrumb.md)

[โมดูลตัวเลือกไซต์](site-selector.md)

[โมดูลกล่องการซื้อ](add-buy-box.md)

[การคาดการณ์ความต้องการคุกกี้](cookie-compliance.md)

[โมดูลส่วนหัว](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
