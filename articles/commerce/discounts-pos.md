---
title: แสดงส่วนลดใน POS
description: หัวข้อนี้จะอธิบายถึงวิธีการที่ Microsoft Dynamics 365 Commerce ช่วยให้สมาคมร้านค้าเรียนรู้เกี่ยวกับโปรโมชั่น และวิธีการที่สามารถใช้สำหรับการเคลื่อนไหวในการเพิ่มการขายหรือการขายสินค้าชนิดอื่น
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 07/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 118e7689e5d37aae18d3823b957301ddfa89369a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982652"
---
# <a name="show-discounts-in-pos"></a>แสดงส่วนลดใน POS

[!include [banner](includes/banner.md)]

โปรโมชั่นมีบทบาทสำคัญในการสร้างแรงกระตุ้นให้กับลูกค้าที่กำลังตัดสินใจซื้อ ตัวอย่างเช่นวันหยุดสามารถสร้างยอดขายสูงสุดสำหรับร้านค้าปลีก เนื่องจากตลาดขายปลีกทั้งหมดเต็มไปด้วยโปรโมชั่นและส่วนลด ถ้าสมาคมร้านค้าทราบและทำความเข้าใจกับโปรโมชันที่พร้อมใช้งาน คุณจะสามารถใช้ประโยชน์จากโปรโมชันเหล่านั้นได้อย่างง่ายดายให้กับการเพิ่มการขายหรือการขายสินค้าชนิดอื่น หัวข้อนี้จะอธิบายถึงวิธีการที่ Microsoft Dynamics 365 Commerce ช่วยให้สมาคมร้านค้าเรียนรู้เกี่ยวกับโปรโมชั่น และวิธีการที่สามารถใช้สำหรับการเคลื่อนไหวในการเพิ่มการขายหรือการขายสินค้าชนิดอื่น

## <a name="learn-about-store-discounts"></a>เรียนรู้เกี่ยวกับส่วนลดของร้านค้า

Commerce รวมถึงการดำเนินงานที่มีชื่อว่า "ดูส่วนลดทั้งหมด" การดำเนินการนี้จะแสดงส่วนลดทั้งหมดที่กำลังรันอยู่ในร้านค้าในขณะนี้ การดำเนินงาน "ดูส่วนลดทั้งหมด" สามารถถูกแม็ปกับปุ่มในการขายหน้าร้าน (POS) และปุ่มดังกล่าวสามารถเพิ่มเข้าไปในหน้า **ยินดีต้อนรับ** หรือหน้า **ธุรกรรม** ได้ ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า **ส่วนลดทั้งหมด** ที่ถูกเปิด

![หน้าส่วนลดทั้งหมด](./media/View_all_discounts.png "หน้าส่วนลดทั้งหมด")

เมื่อต้องการแสดงส่วนลด ระบบจะค้นหาส่วนลดทั้งหมดที่ตรงกับเงื่อนไขต่อไปนี้อย่างน้อยหนึ่งเงื่อนไข

- กลุ่มราคาของส่วนลดตรงกับกลุ่มราคาของร้านค้า
- กลุ่มราคาของส่วนลดจะถูกแม็ปกับสังกัดหรือโปรแกรมตอบแทนลูกค้าสมาชิก
- กลุ่มราคาของส่วนลดจะถูกแม็ปกับแค็ตตาล็อกที่เชื่อมโยงกับร้านค้า

หน้า **ส่วนลดทั้งหมด** จะแสดงเฉพาะส่วนลดตามคูปองบางรายการเท่านั้น เนื่องจากโดยทั่วไปร้านค้าปลีกจะสร้างคูปองและส่วนลดหลายพันรายการที่เกี่ยวข้องสำหรับลูกค้าเฉพาะ และหน้านี้ไม่ได้มีไว้เพื่อแสดงส่วนลดเฉพาะลูกค้า ส่วนลดตามคูปองจะแสดงขึ้น เฉพาะเมื่อมีการเปิดใช้งานตัวเลือก **นำไปใช้โดยไม่มีรหัสคูปอง** ในส่วนหัวของคูปองแต่ละรายการ ในกรณีดังกล่าว พนักงานเก็บเงินสามารถใช้คูปองได้โดยไม่ต้องป้อนหรือสแกนรหัสคูปองหรือบาร์โค้ดใดๆ

เมื่อมีการเปิดใช้งานตัวเลือก **นำไปใช้โดยไม่มีรหัสคูปอง** สถานการณ์ต่างๆ จะพร้อมใช้งาน ตัวอย่างเช่น พนักงานเก็บเงินสามารถให้ส่วนลดเพิ่มเติมแก่ลูกค้าเพื่อวัตถุประสงค์ในการทำให้ลูกค้าพึงพอใจ หรือเนื่องจากข้อบกพร่องของผลิตภัณฑ์ ไม่จำเป็นต้องกระจายรหัสคูปองหรือบาร์โค้ดที่พิมพ์ให้กับพนักงานเก็บเงิน แต่พนักงานเก็บเงินสามารถเลือกปุ่ม **ใช้คูปอง** ได้ โดยจะนำคูปองไปใช้กับธุรกรรมโดยอัตโนมัติ ถ้ามีคูปองหลายใบสำหรับส่วนหัวขของคูปอง ระบบจะเลือกคูปองที่ใช้งานอยู่ใบแรกในธุรกรรมนั้นโดยอัตโนมัติ

ในหน้า **ส่วนลดทั้งหมด** สมาคมผู้ขายยังสามารถค้นหาส่วนลดโดยใช้คำสำคัญได้ด้วย การค้นหาคำสำคัญจะค้นหาในฟิลด์ที่มีการเก็บชื่อส่วนลดและคำอธิบายส่วนลด นอกจากนี้ สมาคมผู้ขายยังสามารถกรองส่วนลดตามการระบุว่าส่วนลดต้องมีรหัสคูปองหรือไม่

## <a name="cross-sell-and-upsell-by-using-discounts"></a>การเพิ่มการขายหรือการขายสินค้าชนิดอื่นโดยใช้ส่วนลด

ส่วนลดต่อรายการสินค้าหลายราย เช่น ส่วนลดปริมาณ ส่วนลดสำหรับการซื้อคละกัน และส่วนลดขีดจำกัด เป็นวิธีการที่ดีในการกระตุ้นให้ลูกค้าซื้อผลิตภัณฑ์เพิ่มเติมเพื่อให้ได้ส่วนลดที่มากขึ้น ดังนั้น จึงช่วยเพิ่มขนาดของรถเข็นของลูกค้าและรายได้ของผู้ค้าปลีกอีกด้วย ส่วนลดเหล่านี้อาจถูกเผยแพร่บนเว็บไซต์พาณิชย์อิเล็กทรอนิกส์ บนสื่อทางสังคม และบนแบนเนอร์ในร้านค้า

อย่างไรก็ตาม แม้ว่าจะมีการใช้วิธีการเผยแพร่เหล่านี้ทั้งหมด ลูกค้าอาจพลาดโอกาสในการใช้ประโยชน์จากโปรโมชัน เพื่อให้สมาคมการขายสามารถเรียนรู้ว่าโปรโมชันที่สามารถใช้ได้กับรายการที่เลือก หรือแม้กระทั่งรถเข็นทั้งหมด ผู้ค้าปลีกสามารถเพิ่มปุ่มสำหรับการดำเนินงาน **"ดูส่วนลดที่พร้อมใช้งาน"** ไปยังกริดปุ่มในหน้า **ธุรกรรม** ซึ่งทำให้เกิดผลลัพธ์ที่สมาคมการขายสามารถเลือกรายการธุรกรรม แล้วเลือกปุ่มเพื่อแสดงส่วนลดทั้งหมดที่พร้อมใช้งานสำหรับรายการที่เลือก นอกจากนี้ สมาคมการขายยังสามารถเลือกแท็บอื่นเพื่อแสดงส่วนลดที่ใช้กับธุรกรรมทั้งหมดได้ สิ่งสำคัญคือต้องจำว่า **การดูส่วนลดที่มีอยู่** จะไม่แสดงส่วนลดที่ใช้แล้วในรายการขายเนื่องจากมีการแสดงข้อมูลส่วนลดอยู่บนบรรทัดการขายแล้ว วัตถุประสงค์ของสถานการณ์นี้คือเพื่อแสดงเฉพาะส่วนลดที่ยังไม่ได้ใช้เท่านั้น ข้อยกเว้นนี้เป็นส่วนลดที่ใช้ตามคูปองที่ทำเครื่องหมายเป็น "ใช้โดยไม่มีรหัสคูปอง" การทำเช่นนี้ทำได้ง่ายสำหรับผู้ที่มีส่วนร่วมในการขายเพื่อลบคูปองที่ใช้แล้ว

หน้า **ส่วนลดทั้งหมด** แสดงเฉพาะส่วนลดที่ไม่ได้แข่งขันกับส่วนลดที่นำมาใช้ใดๆ ลักษณะการทำงานนี้จะช่วยให้มั่นใจว่า ถ้าสมาคมการขายแจ้งให้ลูกค้าทราบเกี่ยวกับส่วนลด และลูกค้าทำการดำเนินการที่จำเป็น (ตัวอย่างเช่น ลูกค้าซื้อสินค้าอีกหนึ่งรายการเพื่อรับส่วนลด 10 เปอร์เซ็นต์) จะมีการใช้ส่วนลดกับธุรกรรม ส่วนลดตามคูปองจะแสดงขึ้นเฉพาะเมื่อมีการเปิดใช้งานตัวเลือก **นำไปใช้โดยไม่มีรหัสคูปอง**

ในสถานการณ์จำลองแบบง่ายที่ซึ่งส่วนลดทั้งหมดมีระดับความสำคัญเดียวกัน โหมดการเกิดพร้อมกันของส่วนลดเป็น **รวม** การควบคุมการเกิดพร้อมกันของส่วนลดถูกตั้งค่าเป็น **ราคาที่ดีที่สุดและความซับซ้อนภายในระดับความสำคัญ ไม่มีความซับซ้อนในระดับความสำคัญ** หน้า **ส่วนลดทั้งหมด** จะแสดงส่วนลดที่มีอยู่ทั้งหมดสำหรับผลิตภัณฑ์ เนื่องจากส่วนลดทั้งหมดถูกรวมและไม่แข่งขันกันเอง

ภาพประกอบต่อไปนี้แสดงตรรกะที่กำหนดส่วนลดที่ถูกแสดงในสถานการณ์ขั้นสูง เช่น สถานการณ์จำลองที่ซึ่งโหมดการเกิดพร้อมกันของส่วนลดคือ **ราคาที่ดีที่สุ** หรือ **พิเศษ** และมีการใช้ระดับความสำคัญสองรายการขึ้นไป ในสถานการณ์เหล่านี้ ส่วนลดที่แสดงจะได้รับผลกระทบเพิ่มเติมโดยขึ้นอยู่กับว่ามีการตั้งค่าการควบคุมการเกิดพร้อมกันของส่วนลดเป็น **ราคาที่ดีที่สุดและความซับซ้อนภายในระดับความสำคัญ ไม่มีความซับซ้อนในระดับความสำคัญ** หรือ **ราคาที่ดีที่สุดเฉพาะภายในระดับความสำคัญ มีความซับซ้อนในระดับความสำคัญเสมอ**

ภาพประกอบต่อไปนี้แสดงตรรกะที่ใช้ เมื่อมีการตั้งค่าตัวควบคุมการเกิดพร้อมกันของส่วนลดเป็น **ราคาที่ดีที่สุดและความซับซ้อนภายในระดับความสำคัญ ไม่มีความซับซ้อนในระดับความสำคัญ**

![ตรรกะสำหรับราคาที่ดีที่สุดและความซับซ้อนภายในระดับความสำคัญ ไม่มีความซับซ้อนในระดับความสำคัญ](./media/Model_1.png "ตรรกะสำหรับราคาที่ดีที่สุดและความซับซ้อนภายในระดับความสำคัญ ต้องไม่มีความซับซ้อนในระดับความสำคัญ")

ภาพประกอบต่อไปนี้แสดงตรรกะที่ใช้เมื่อมีการตั้งค่าตัวควบคุมการเกิดพร้อมกันของส่วนลดเป็น **ราคาที่ดีที่สุดเฉพาะภายในระดับความสำคัญ มีความซับซ้อนในระดับความสำคัญเสมอ**

![ตรรกะสำหรับราคาที่ดีที่สุดเฉพาะภายในระดับความสำคัญ มีความซับซ้อนในระดับความสำคัญเสมอ](./media/Model_2.png "ตรรกะสำหรับราคาที่ดีที่สุดเฉพาะภายในระดับความสำคัญ มีความซับซ้อนในระดับความสำคัญเสมอ")
