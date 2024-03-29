---
title: เพิ่มคำแนะนำในหน้าจอธุรกรรม
description: บทความนี้อธิบายวิธีการเพิ่มการควบคุมคำแนะนำไปยังหน้าจอธุรกรรมบนอุปกรณ์ point of sale (POS) โดยใช้ตัวออกแบบโครงร่างหน้าจอใน Microsoft Dynamics 365 Commerce
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4748ade8d6693666b58cbded2123d3449d191509
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862083"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>เพิ่มคำแนะนำในหน้าจอธุรกรรม

[!include [banner](includes/banner.md)]


บทความนี้อธิบายวิธีการเพิ่มการควบคุมคำแนะนำไปยังหน้าจอธุรกรรมบนอุปกรณ์ point of sale (POS) โดยใช้ตัวออกแบบโครงร่างหน้าจอใน Microsoft Dynamics 365 Commerce สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [คำแนะนำผลิตภัณฑ์ในเอกสารของ POS](product.md)


คุณสามารถแสดงคำแนะนำผลิตภัณฑ์บนอุปกรณ์ POS ของคุณได้ เมื่อคุณใช้ Commerce เมื่อต้องการแสดงคำแนะนำผลิตภัณฑ์ คุณต้องเพิ่มตัวควบคุมไปยังหน้าจอธุรกรรมโดยใช้ตัวออกแบบโครงร่างหน้าจอ 

## <a name="open-layout-designer"></a>เปิดตัวออกแบบโครงร่าง

1. ไปที่ **การขายปลีกและการค้า** &gt; **การตั้งค่าช่องทาง** &gt; **การตั้งค่า POS** &gt; **POS** &gt; **โครงร่างหน้าจอ**
2. ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาหน้าจอที่คุณต้องการเพิ่มตัวควบคุม ตัวอย่างเช่น ตัวกรองบนฟิลด์ **รหัสโครงร่างหน้าจอ** โดยใช้ค่า **F2CP16:9M**
3. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ ตัวอย่างเช่น เลือก **ชื่อ: F2CP16:9M รหัสโครงร่างหน้าจอ: F2CP16:9M**
4. คลิก **ตัวออกแบบโครงร่าง**
5. ทำตามพร้อมต์เพื่อเปิดใช้งานตัวออกแบบโครงร่าง เมื่อได้รับพร้อมต์สำหรับข้อมูลประจำตัว ให้ป้อนข้อมูลประจำตัวเดียวกันที่ถูกใช้เมื่อมีการเปิดใช้ตัวออกแบบโครงร่างจากเพจ **โครงร่างหน้าจอ**
6. เมื่อคุณเข้าสู่ระบบ หน้าที่คล้ายกับหน้าด้านล่างนี้จะปรากฏขึ้น โครงร่างจะแตกต่างกันโดยขึ้นอยู่กับการเลือกกำหนดที่ทำไว้สำหรับร้านค้าของคุณ


    [![ตัวออกแบบโครงร่าง](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>เลือกตัวเลือกการแสดง

มีตัวเลือกสองตัวสำหรับการตั้งค่าคอนฟิก เลือกตัวเลือกที่ดีที่สุดสำหรับร้านค้าของคุณ และทำตามคำแนะนำที่เหลือเพื่อทำการตั้งค่าตัวควบคุมให้เสร็จสิ้น ตัวเลือกสองตัว ได้แก่

- คำแนะนำจะปรากฏขึ้นเสมอ
- แท็บ **คำแนะนำ** จะปรากฏในกริดทางด้านขวาของหน้าจอ

### <a name="make-recommendations-always-visible"></a>ทำให้คำแนะนำปรากฏขึ้นเสมอ


1. ลดความสูงของพื้นที่รายละเอียดของรายการธุรกรรม เพื่อให้มีความสูงเท่ากับแผงสำหรับลูกค้าทางด้านซ้าย


    [![ความสูงของพื้นที่รายละเอียดของรายการธุรกรรมถูกลดลง](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. จากเมนูทางด้านซ้าย ลากและปล่อยตัวควบคุมคำแนะนำระหว่างพื้นที่รายละเอียดของบรรทัดธุรกรรมและกริดปุ่มในศูนย์กลางด้านล่างของหน้าจอธุรกรรม ปรับขนาดตัวควบคุมเพื่อให้พอดีในช่องนั้น

    [![ตัวควบคุมคำแนะนำถูกเพิ่มลงในโครงร่าง](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. คลิก **X** เพื่อบันทึกและออกจากตัวออกแบบโครงร่าง
4. ใน Commerce ไปที่ **การขายปลีกและการค้า** &gt; **การขายปลีกและการค้าไอที** &gt; **กำหนดการกระจาย**
5. ในรายการ เลือก **1090 เครื่องบันทึกเงินสด**
6. คลิก **รันทันที**


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>เพิ่มแท็บคำแนะนำไปยังกริดปุ่มทางด้านขวาของหน้าจอ

1. คลิกขวาในพื้นที่ว่างที่อยู่ด้านล่างของแท็บสุดท้ายในกริดปุ่มที่อยู่ทางด้านขวาของหน้า

2. คลิก **กำหนด**

    [![กล่องโต้ตอบการเลือกกำหนด - ตัวควบคุมแท็บ](./media/pic-5.png)](./media/pic-5.png)

3. คลิก **แท็บใหม่**
4. ค้นหาแท็บใหม่ที่คุณเพิ่งเพิ่มเข้ามา คุณอาจต้องเลื่อนลง
5. ในเมนูแบบหล่นลง **เนื้อหา** เลือก **ผลิตภัณฑ์ที่แนะนำ**

    [![การเลือกผลิตภัณฑ์ที่แนะนำในฟิลด์เนื้อหา](./media/pic-6.png)](./media/pic-6.png)

6. ในฟิลด์ **ป้ายชื่อ** พิมพ์ชื่อสำหรับแท็บคำแนะนำ ตัวอย่างเช่น พิมพ์ 'ผลิตภัณฑ์ที่แนะนำ'
7. ในฟิลด์ **รูปภาพ** ให้เลือกรูปภาพที่จะให้ปรากฏบนแท็บ
8. คลิก **ตกลง** แท็บใหม่จะปรากฏในกริดปุ่ม
9. คลิก **X** เพื่อบันทึกและออกจากตัวออกแบบโครงร่าง
10. ใน Commerce ไปที่ **การขายปลีกและการค้า** &gt; **การขายปลีกและการค้าไอที** &gt; **กำหนดการกระจาย**
11. ในรายการ เลือก **1090 เครื่องบันทึกเงินสด**
12. คลิก **รันทันที**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของคำแนะนำผลิตภัณฑ์](product-recommendations.md)

[เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce](enable-adls-environment.md)

[เปิดใช้งานคำแนะนำผลิตภัณฑ์](enable-product-recommendations.md)

[เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล](personalized-recommendations.md)

[เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล](personalization-gdpr.md)

[เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"](shop-similar-looks.md)

[เพิ่มคำแนะนำผลิตภัณฑ์ใน POS](product.md)

[ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML](modify-product-recommendation-results.md)

[สร้างคำแนะนำที่ระบุด้วยตนเอง](create-editorial-recommendation-lists.md)

[สร้างคำแนะนำที่มีข้อมูลสาธิต](product-recommendations-demo-data.md)

[FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]