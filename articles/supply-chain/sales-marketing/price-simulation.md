---
title: การจำลองสถานการณ์ราคา
description: บทความนี้แสดงข้อมูลเกี่ยวกับการจำลองราคาสำหรับใบเสนอราคา การจำลองราคาช่วยประเมินผลของการหักเงินสำหรับราคาขายในอนาคตระหว่างกระบวนการใบเสนอราคา ก่อนที่จะยืนยันราคาเฉพาะ
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationPriceSimulation, SalesQuotationsTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d206654dcb7964ac2ed9aa9ccf7cec709e1bd38c
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689691"
---
# <a name="price-simulation"></a>การจำลองสถานการณ์ราคา

[!include [banner](../includes/banner.md)]

บทความนี้แสดงข้อมูลเกี่ยวกับการจำลองราคาสำหรับใบเสนอราคา การจำลองราคาช่วยประเมินผลของการหักเงินสำหรับราคาขายในอนาคตระหว่างกระบวนการใบเสนอราคา ก่อนที่จะยืนยันราคาเฉพาะ

การจำลองราคาสำหรับใบเสนอราคาแสดงยอดรวมใหม่ตามราคาใหม่ที่เสนอ การจำลองราคายังสามารถแสดงยอดใหม่สำหรับรายการที่ระบุที่สร้างขึ้นในใบเสนอราคาที่มีอยู่ คุณสามารถป้อนการจำลองราคาและใช้ในภายหลัง อีกทางหนึ่งคือ คุณสามารถใช้ต้นฉบับใบเสนอราคาโดยไม่มีการจำลองราคาและทำการเปลี่ยนแปลงเพิ่มเติมตามที่คุณดำเนินการตามกระบวนการขายกับลูกค้าของคุณ  

การจำลองราคาไม่เปลี่ยนแปลงราคาในใบเสนอราคา ถ้ามีการใช้การจำลองราคากับใบเสนอราคาทั้งหมด จะถือว่าเป็นส่วนลดพิเศษในส่วนหัวของใบเสนอราคา ถ้ามีการใช้การจำลองราคากับสินค้าเฉพาะ จะถือว่าเป็นส่วนลดพิเศษในรายการใบเสนอราคา ราคาขายต่อหน่วยในรายการใบเสนอราคาที่สร้างขึ้นไม่เปลี่ยนแปลงเมื่อมีการใช้การจำลองราคา แต่ เปอร์เซ็นต์ส่วนลดที่สอดคล้องกับการลดราคาของรายการใบเสนอราคาจะมีใช้ เมื่อมีใช้การจำลองราคา ราคาขายต่อหน่วยและเปอร์เซ็นต์ส่วนลดจะถูกโอนย้ายไปยังรายการใบเสนอราคาหรือส่วนหัวของใบเสนอราคา  

>[!NOTE]
>เมื่อคุณรันการจำลองราคา สกุลเงินการขายปัจจุบันเท่านั้นจะถูกใช้เพื่อสร้างแบบจำลอง อย่างไรก็ตาม เมื่อคุณดูยอดรวมของใบเสนอราคา คุณจะเห็นชุดของสกุลเงินของสกุลเงินของบริษัทและสกุลเงินการขาย  

สินค้าเสริมที่จะเพิ่มไปยังรายการใบเสนอราคาอาจทริกเกอร์ส่วนลดต่อรายการสินค้าหรือส่วนลดต่อสินค้าหลายรายการ พวกเขาอาจจะทริกเกอร์ส่วนลดรวมที่เปลี่ยนแปลงกำไรผันแปรและอัตราส่วนกำไรผันแปรของรายการใบเสนอราคาและส่วนลดทั้งหมด  

คุณสามารถรันการจำลองราคาต่าง ๆ เพื่อติดตามผลของการปรับปรุงราคาในเป้าหมายของใบเสนอราคา การรันการจำลองดังกล่าว จะช่วยให้คุณสามารถปรับปรุงราคาโดยรวมของใบเสนอราคา หรือราคาของรายการที่ระบุหนึ่งอย่างขึ้นไปในใบเสนอราคา แล้วจึงใช้การจำลองราคาที่เป็นไปได้ว่าจะช่วยคุณปิดการขายได้  

เมื่อคุณสร้างใบเสนอราคา คุณสามารถตั้งค่าการแจ้งเตือน นี่คือบางวิธีที่จะใช้ข้อความแจ้งเตือน:

-   พวกเขาสามารถทำให้คุณทราบเกี่ยวกับสถานะของใบเสนอราคาในองค์กร
-   พวกเขาสามารถทริกเกอร์การตรวจสอบใบเสนอราคาที่ระบุหรือแจ้งให้คุณทราบเมื่อเกินวงเงินส่วนลด

## <a name="price-simulation-and-discounts"></a>การจำลองราคาและส่วนลด
เพื่อรับประกันว่าส่วนลดและราคามีคำนวณอย่างถูกต้อง ต้องระวังเมื่อคุณรันการจำลองราคาในใบเสนอราคาที่มีส่วนลด เนื่องจากการจำลองราคาทั้งหมดถือเป็นส่วนลดพิเศษในรายการใบเสนอราคาที่ใช้งานอยู่หรือใบเสนอราคาทั้งหมด คุณต้องติดตามผลต่างของส่วนลด

### <a name="types-of-discounts-in-trade-agreements"></a>ชนิดของส่วนลดในข้อตกลงทางการค้า

ข้อตกลงทางการค้าใน Supply Chain Management สามารถมีชนิดของส่วนลดราคาได้สี่ชนิด ส่วนลดเหล่านี้สามารถตั้งค่าสำหรับสินค้า ลูกค้า หรือกลุ่มราคาต่างๆ และสามารถจำกัดตามวันที่ได้ เพื่อเป็นการหลีกเลี่ยงการคำนวณที่ไม่ถูกต้อง คุณต้องพิจารณาถึงข้อตกลงทางการค้าเมื่อคุณรันการจำลองราคา นี่คือส่วนลดสี่ประเภทในข้อตกลงทางการค้า:

-   **ราคาขาย**– คุณสามารถระบุราคาขายแยกต่างหากสำหรับสินค้าได้ เมื่อรายการใบเสนอราคาถูกสร้างขึ้น โปรแกรมจะค้นหาราคาขายที่ถูกต้องสำหรับสินค้าและโอนย้ายไปยังรายการใบเสนอราคา ดังนั้น ข้อตกลงทางการค้าที่มีส่วนลดชนิดนี้ไม่ส่งผลกระทบต่อการจำลองราคา ราคาขายที่ใช้ในรายการใบเสนอราคาสะท้อนถึงข้อตกลงทางการค้า
-   **ส่วนลดต่อรายการสินค้า**– ส่วนลดพิเศษที่ระบุสำหรับสินค้า ขึ้นอยู่กับปริมาณที่สั่ง ยอดเงินในรายการโดยทั่วไปจะลดลงตามส่วนลดต่อรายการสินค้าก่อนที่จะรันการจำลองราคา ดังนั้น ข้อตกลงทางการค้าที่มีส่วนลดชนิดนี้ส่งผลกระทบต่อการจำลองราคา
-   **ส่วนลดต่อสินค้าหลายรายการ**– ถ้าปริมาณรวมเกินกว่าจำนวนสูงสุดที่กำหนดไว้ ชุดสินค้าที่สั่งซึ่งกำหนดไว้ล่วงหน้าจะทริกเกอร์ส่วนลดในใบสั่งทั้งหมด ยอดเงินในรายการโดยทั่วไปจะลดลงตามส่วนลดต่อรายการสินค้าก่อนที่จะรันการจำลองราคา ดังนั้น ข้อตกลงทางการค้าที่มีส่วนลดชนิดนี้ส่งผลกระทบต่อการจำลองราคา
-   **ส่วนลดรวม**–หากจำนวนเงินรวมเกินกว่าจำนวนสูงสุดที่กำหนดไว้ ชุดสินค้าที่สั่งซึ่งกำหนดไว้ล่วงหน้าจะทริกเกอร์ส่วนลดในใบสั่งทั้งหมด ส่วนลดรวมจะถูกสร้างขึ้นโดยรายการใบเสนอราคา อย่างไรก็ตาม เนื่องจากมีใช้ส่วนลดรวมในยอดรวมใบเสนอราคาเป็นส่วนลด ซึ่งจะลดยอดเงินรวมในใบเสนอราคา ดังนั้น ข้อตกลงทางการค้าที่มีส่วนลดชนิดนี้ส่งผลกระทบต่อการจำลองราคา

### <a name="quotation-lines-and-trade-agreements"></a>รายการใบเสนอราคาและข้อตกลงทางการค้า

เมื่อคุณสร้างหรือปรับรายการใบเสนอราคา จะมีคำนวณส่วนลดต่อรายการสินค้าโดยอัตโนมัติ ราคาขายที่เกี่ยวข้องที่พบสำหรับสินค้า ตามข้อตกลงทางการค้า

## <a name="price-simulation-examples"></a>ตัวอย่างการจำลองราคา
ตัวอย่างต่อไปนี้ใช้การจำลองราคาสำหรับหัวข้อใบเสนอราคาและสินค้ารายการเดียว

### <a name="price-simulation-for-quotation-headers"></a>การจำลองราคาสำหรับส่วนหัวของใบเสนอรา

คุณสร้างใบเสนอราคาที่มีรายการต่อไปนี้

-   สินค้า BR-12 10 หน่วย (ราคาต้นทุนต่อหน่วย USD 9.52 และราคาขายต่อหน่วย USD 15.32)
-   สินค้า BR-14 12 หน่วย (ราคาต้นทุนต่อหน่วย USD 7.48 และราคาขายต่อหน่วย USD 13.75)

ตารางต่อไปนี้แสดรายการใบเสนอราคา

|    &nbsp;                  | การคำนวณ                          | ผลลัพธ์   |
|----------------------------|--------------------------------------|----------|
| ปริมาณการขาย             | 10 หน่วย + 12 หน่วย                  | 22 หน่วย |
| มูลค่าการขายเป็น USD         | (10 × 15.32) + (12 × 13.75)          | 318.20   |
| มูลค่าต้นทุนเป็น USD          | (10 × 9.52) + (12 × 7.48)            | 184.96   |
| กำไรผันแปรเป็น USD | 318.20 – 184.96                      | 133.24   |
| อัตราส่วนกำไรส่วนเกิน         | (\[318.20 – 184.96\] ÷ 318.20) × 100 | 41.87%   |

คุณรันการจำลองราคาและใช้ส่วนลดรวม 15 เปอร์เซ็นต์สำหรับใบเสนอราคาทั้งหมด หรือส่วนหัวของใบเสนอราคา ตารางต่อไปนี้แสดงยอดรวมใหม่ของใบเสนอราคาหลังจากที่รันการจำลองราคา

|     &nbsp;                                           | การคำนวณ                               | ผลลัพธ์   |
|------------------------------------------------------|-------------------------------------------|----------|
| ปริมาณการขาย                                       | 10 หน่วย + 12 หน่วย                       | 22 หน่วย |
| มูลค่าการขายเดิมเป็น USD                               | (10 × 15.32) + (12 × 13.75)               | 318.20   |
| มูลค่าต้นทุนเดิมเป็น USD                                | (10 × 9.52) + (12 × 7.48)                 | 184.96   |
| กำไรผันแปรเดิมเป็น USD                       | 318.20 – 184.96                           | 133.24   |
| อัตราส่วนกำไรผันแปรเดิม                               | (\[318.20 – (10 × 9.52)\] ÷ 318.20) × 100 | 41.87%   |
| การจำลองราคาส่วนลดรวม 15% เป็น USD | (15 × 318.2) ÷ 100                        | 47.73    |
| มูลค่าการขายใหม่เป็น USD                               | 318.20 – 47.73                            | 270.47   |
| กำไรผันแปรใหม่เป็น USD                       | 270.47 – 184.96                           | 85.51    |
| อัตรากำไรส่วนเกินใหม่                               | \[(270.47 – 184.96) ÷ 270.47\] × 100      | 31.61%   |

### <a name="price-simulation-for-single-line-items"></a>การจำลองราคาสำหรับสินค้าในรายการเดียว

คุณสร้างใบเสนอราคาที่มีรายการต่อไปนี้

-   สินค้า BR-12 10 หน่วย (ราคาต้นทุนต่อหน่วย USD 9.52 และราคาขายต่อหน่วย USD 15.32)
-   สินค้า BR-14 12 หน่วย (ราคาต้นทุนต่อหน่วย USD 7.48 และราคาขายต่อหน่วย USD 13.75)

ตารางต่อไปนี้แสดรายการใบเสนอราคา

|      &nbsp;                          | การคำนวณ                          | ผลลัพธ์   |
|--------------------------------------|--------------------------------------|----------|
| ปริมาณการขาย                       | 10 หน่วย + 12 หน่วย                  | 22 หน่วย |
| มูลค่าการขายเป็น USD สำหรับ BR-12         | 10 × 15.32                           | 153.20   |
| มูลค่าการขายเป็น USD สำหรับ BR-14         | 12 × 13.75                           | 165.00   |
| มูลค่าต้นทุนเป็น USD สำหรับ BR-12          | 10 × 9.52                            | 95.20    |
| มูลค่าต้นทุนเป็น USD สำหรับ BR-14          | 12 × 7.48                            | 89.76    |
| กำไรผันแปรเป็น USD สำหรับ BR-12 | 153.20 – 95.20                       | 58.00    |
| กำไรผันแปรเป็น USD สำหรับ BR-14 | 165.00 – 89.76                       | 75.24    |
| อัตราส่วนกำไรผันแปรเป็น USD สำหรับ BR-12  | \[(153.20 – 95.20) ÷ 153.20\] × 100  | 37.86    |
| อัตราส่วนกำไรผันแปรเป็น USD สำหรับ BR-14  | \[(165.00 – 89.76) ÷ 165.00\] × 100  | 45.60    |
| ยอดรวมมูลค่าการขายเป็น USD             | (10 × 15.32) + (12 × 13.75)          | 318.20   |
| ยอดรวมมูลค่าต้นทุนเป็น USD              | (10 × 9.52) + (12 × 7.48)            | 184.96   |
| ยอดรวมกำไรผันแปรเป็น USD     | 318.20 – 184.96                      | 133.24   |
| ยอดรวมอัตราส่วนกำไรผันแปร             | \[(318.20 – 184.96) ÷ 318.20\] × 100 | 41.87%   |

คุณรันการจำลองราคาและใช้ส่วนลดรวม 10 เปอร์เซ็นต์กับหน่วย BR-12 ตารางต่อไปนี้แสดงยอดรวมใหม่ของใบเสนอราคาหลังจากที่รันการจำลองราคาสำหรับรายการสินค้าเดียว

|    &nbsp;                                         | การคำนวณ                             | ผลลัพธ์   |
|---------------------------------------------------|-----------------------------------------|----------|
| ปริมาณการขาย                                    | 10 หน่วย + 12 หน่วย                     | 22 หน่วย |
| มูลค่าการขายเดิมเป็น USD สำหรับ BR-12                  | 10 × 15.32                              | 153.20   |
| การจำลองราคาส่วนลด 10 เปอร์เซ็นต์สำหรับ BR-12 | (10 × 153.2) ÷ 100                      | 15.32    |
| มูลค่าการขายใหม่เป็น USD สำหรับ BR-12                  | (10 × 15.32) – 15.32                    | 137.88   |
| มูลค่าการขายเป็น USD สำหรับ BR-14                      | 12 × 13.75                              | 165.00   |
| มูลค่าต้นทุนเป็น USD สำหรับ BR-12                       | 10 × 9.52                               | 95.20    |
| มูลค่าต้นทุนเป็น USD สำหรับ BR-14                       | 12 × 7.48                               | 89.76    |
| กำไรผันแปรใหม่เป็น USD สำหรับ BR-12          | 137.88 – 95.20                          | 42.68    |
| กำไรผันแปรเป็น USD สำหรับ BR-14              | 165.00 – 89.76                          | 75.24    |
| อัตราส่วนกำไรผันแปรใหม่เป็น USD สำหรับ BR-12           | \[(137.88 – 95.20) ÷ 137.88\] × 100     | 30.95    |
| อัตราส่วนกำไรผันแปรเป็น USD สำหรับ BR-14               | \[(165.00 – 89.76) ÷ 165.00\] × 100     | 45.60    |
| ยอดรวมมูลค่าการขายใหม่เป็น USD                      | \[(10 × 15.32) – 15.32\] + (12 × 13.75) | 302.88   |
| ยอดรวมมูลค่าต้นทุนเป็น USD                           | (10 × 9.52) + (12 × 7.48)               | 184.96   |
| ยอดรวมกำไรผันแปรใหม่เป็น USD              | 302.88 – 184.96                         | 117.92   |
| อัตราส่วนกำไรส่วนเกินรวมใหม่                      | \[(302.88 – 184.96) ÷ 302.88\] × 100    | 38.93%   |

การจำลองราคาจะมีผลต่อรายการที่ถูกใช้เท่านั้นและลดยอดรวมของรายการนั้น





[!INCLUDE[footer-include](../../includes/footer-banner.md)]