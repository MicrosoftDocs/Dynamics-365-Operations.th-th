---
title: ภาพรวมของไลบรารีโมดูล
description: บทความนี้แสดงภาพรวมของไลบรารีโมดูล Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d9dc07b3f6417c7e284c6555c2818c2a782d7683
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268958"
---
# <a name="module-library-overview"></a>ภาพรวมของไลบรารีโมดูล

[!include [banner](includes/banner.md)]

บทความนี้แสดงภาพรวมของไลบรารีโมดูล Microsoft Dynamics 365 Commerce

ไลบรารีโมดูล Dynamics 365 Commerce เป็นชุดของโมดูลที่สามารถใช้ในการสร้างเว็บไซต์อีคอมเมิร์ซ โมดูลมีทั้งด้านอินเทอร์เฟสผู้ใช้ (UI) และลักษณะการทำงาน

ชุดรูปแบบสามารถนำไปใช้กับโมดูลในไลบรารีโมดูล เพื่อเปลี่ยนลักษณะที่แสดง ชุดรูปแบบใช้ Cascading Style Sheets (CSS) ธีมสำหรับไซต์ e-Commerce แบบสมมติที่มีชื่อว่า "Fabrikam" ให้ไว้เป็นส่วนหนึ่งของไลบรารีโมดูล และสามารถใช้เป็นข้อมูลอ้างอิงได้

## <a name="module-library-modules"></a>โมดูลไลบรารีของโมดูล

ชนิดของโมดูลต่อไปนี้มีให้ในไลบรารีโมดูล:

- **โมดูลคอนเทนเนอร์** – โมดูลคอนเทนเนอร์เป็นโมดูลที่เรียบง่ายที่ทำหน้าที่เป็นโฮสต์สำหรับโมดูลอื่นๆ ซึ่งควบคุมโครงร่างของโมดูลที่อยู่ภายใน
- **โมดูลการตลาด** – โมดูลการตลาด ได้แก่ บล็อคเนื้อหา บล็อคข้อความ เครื่องเล่นวิดีโอ และโมดูลแบบวงล้อ โมดูลเหล่านี้ทั้งหมดสามารถใช้ในการแสดงเนื้อหาได้ ซึ่งสามารถนำไปใช้ที่หน้าไหนก็ได้ และจะถูกขับเคลื่อนด้วยข้อมูลจากระบบการจัดการเนื้อหา (CMS)
- **โมดูลส่วนหัวและส่วนท้าย** – โมดูลส่วนหัวและส่วนท้ายจะปรากฏในส่วนหัวและส่วนท้ายของหน้าไซต์ทั้งหมด คุณสามารถตั้งค่าคอนฟิกโมดูลเหล่านี้ตามต้องการได้โดยใช้คุณสมบัติ
- **โมดูลค้นหา** – ผลิตภัณฑ์จะถูกพบได้โดยใช้โมดูลการค้นหาในส่วนหัว ผลการค้นหาจะปรากฏขึ้นบนหน้าผลการค้นหา นอกจากนี้คุณยังสามารถค้นหาผลิตภัณฑ์ในหน้าประเภท ซึ่งเป็นหน้าเฉพาะสำหรับแต่ละประเภทที่ได้รับการสนับสนุน ในลำดับชั้นการนำทางของช่องทาง นอกจากนี้ คุณยังสามารถใช้โมดูลตัวคัดสรรในการกรองผลการค้นหาและหน้าประเภทได้อีกด้วย
- **โมดูลหน้ารายละเอียดผลิตภัณฑ์** – หน้ารายละเอียดของผลิตภัณฑ์ใช้หลายโมดูลเพื่อแสดงข้อมูลผลิตภัณฑ์ โมดูลในกล่องการซื้อ ให้ลูกค้าสามารถดูผลิตภัณฑ์และเพิ่มสินค้าลงในรถเข็น โมดูลอื่นๆ เช่น โมดูลข้อมูลจำเพาะด้านเทคนิค แสดงรายละเอียดของผลิตภัณฑ์ โมดูลการจัดอันดับ และความคิดเห็นสามารถใช้เพื่อดูและให้ความคิดเห็น
- **โมดูลซื้อออนไลน์ รับสินค้าที่ร้านค้า** – โมดูลซื้อออนไลน์ รับสินค้าที่ร้านค้าทำงานร่วมกับ Bing Maps คุณสามารถใช้ในการค้นหาร้านค้าใกล้เคียง ที่ลูกค้าสามารถรับสินค้าที่ซื้อได้
- **โมดูลการซื้อ** – โมดูลการซื้อรวมถึงโมดูลรถเข็น ซึ่งสามารถใช้เพื่อเพิ่มสินค้าลงในรถเข็น โมดูลการชำระเงินจะเก็บที่อยู่ในการจัดส่ง ตัวเลือกการจัดส่ง บัตรของขวัญ โปรแกรมสะสมคะแนน และข้อมูลบัตรเครดิตเพื่อให้สามารถประมวลผลใบสั่งซื้อได้ หลังจากวางใบสั่งซื้อแล้ว คุณสามารถใช้โมดูลการยืนยันใบสั่งเพื่อแสดงรายละเอียดการยืนยันได้
- **โมดูลการจัดการบัญชี** – โมดูลเข้าสู่ระบบของผู้ใช้ ให้ลูกค้าล็อกอินเข้าสู่บัญชีที่มีอยู่ และโมดูลการลงทะเบียนจะช่วยให้ผู้ใช้สามารถสร้างบัญชีใหม่ได้ หลังจากที่สร้างบัญชีแล้ว คุณสามารถใช้โมดูลบัญชีของใบสั่งซื้อเพื่อดูใบสั่งซื้อล่าสุด และโมดูลรายละเอียดใบสั่งซื้อสามารถใช้เพื่อดูรายละเอียดของใบสั่งซื้อได้
- **โมดูลคำแนะนำ** – ข้อแนะนำแสดงโดยใช้โมดูลการวางผลิตภัณฑ์ โมดูลนี้สนับสนุนรายการอัลกอริทึม และรายการที่เลือกโดยบรรณาธิการ ที่สามารถแสดงในหน้าใดก็ได้

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[โมดูลคอนเทนเนอร์](add-container-module.md)

[โมดูลกล่องการซื้อ](add-buy-box.md)

[โมดูลรถเข็น](add-cart-module.md)

[โมดูลเช็คเอาท์](add-checkout-module.md)

[โมดูลใบยืนยันคำสั่งซื้อ](order-confirmation-module.md)

[โมดูหัวข้อ](author-header-module.md)

[โมดูลของส่วนท้าย](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
